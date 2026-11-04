
# `ping` — Kiểm tra kết nối tới một máy

## Dùng để làm gì

Gửi gói **ICMP Echo Request** tới một máy và chờ **Echo Reply**, để biết:

- Máy đích có liên lạc được không.
- Độ trễ (thời gian đi và về) là bao nhiêu.
- Có mất gói tin không.

ICMP thuộc **tầng Internet (tầng 3)**, không dùng TCP/UDP, không có port. → Ping được **không có nghĩa** một dịch vụ cụ thể (web, SSH...) đang hoạt động. → Ping không được **chưa chắc** máy đích chết: nhiều máy/firewall/gateway cloud chặn ICMP.

## Các lệnh hay dùng

```bash
ping 8.8.8.8                 # ping liên tục, dừng bằng Ctrl+C
ping -c 4 8.8.8.8            # chỉ gửi 4 gói rồi dừng
ping -c 4 google.com         # ping theo tên miền (kiểm tra luôn DNS)
ping -4 google.com           # bắt buộc dùng IPv4
ping -6 google.com           # bắt buộc dùng IPv6
ping -i 0.5 8.8.8.8          # gửi mỗi 0.5 giây (mặc định 1 giây)
ping -W 2 8.8.8.8            # chờ phản hồi tối đa 2 giây
ping -s 1000 8.8.8.8         # gói dữ liệu 1000 byte (mặc định 56)
ping -I eth0 8.8.8.8         # gửi ra một interface cụ thể
ping -M do -s 1472 8.8.8.8   # cấm phân mảnh, dùng để dò MTU
```

## Đọc kết quả

```
PING 10.0.0.150 (10.0.0.150) 56(84) bytes of data.
64 bytes from 10.0.0.150: icmp_seq=1 ttl=64 time=0.036 ms
64 bytes from 10.0.0.150: icmp_seq=2 ttl=64 time=0.033 ms
64 bytes from 10.0.0.150: icmp_seq=3 ttl=64 time=0.033 ms
^C
--- 10.0.0.150 ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2003ms
rtt min/avg/max/mdev = 0.033/0.034/0.036/0.001 ms
```

### Dòng đầu

|Phần|Ý nghĩa|
|---|---|
|`10.0.0.150 (10.0.0.150)`|Tên đích và IP đã phân giải được|
|`56(84) bytes`|56 byte dữ liệu; 84 = 56 + 8 (header ICMP) + 20 (header IP)|

### Mỗi dòng phản hồi

|Phần|Ý nghĩa|
|---|---|
|`64 bytes`|Kích thước gói trả về (56 dữ liệu + 8 header ICMP)|
|`from 10.0.0.150`|Ai trả lời|
|`icmp_seq=1`|Số thứ tự gói. **Số bị nhảy cóc → có gói bị mất**|
|`ttl=64`|TTL còn lại của gói trả lời|
|`time=0.036 ms`|Độ trễ đi và về (RTT)|

### Phần thống kê

|Phần|Ý nghĩa|
|---|---|
|`transmitted / received`|Số gói gửi đi / nhận về|
|`% packet loss`|Tỷ lệ mất gói|
|`min/avg/max`|Độ trễ nhỏ nhất / trung bình / lớn nhất|
|`mdev`|Độ dao động của độ trễ (jitter). Càng nhỏ càng ổn định|

## ⭐ Các thông tin cần chú ý

### 1. Độ trễ (`time`) — đoán khoảng cách

|Độ trễ|Thường là|
|---|---|
|~0.01–0.05 ms|**Chính máy mình** (gói không ra khỏi máy, đi qua `lo`)|
|~0.1–1 ms|Máy cùng mạng LAN / cùng datacenter|
|~vài–vài chục ms|Cùng quốc gia / khu vực|
|~100+ ms|Liên lục địa|

Ví dụ: ping `10.0.0.150` ra `0.03 ms` vì đó là IP của chính `eth0`. Kiểm chứng: `ip route get 10.0.0.150` → `local ... dev lo`.

### 2. TTL — đoán số hop và hệ điều hành

TTL ban đầu thường là: **64** (Linux, macOS), **128** (Windows), **255** (thiết bị mạng).

Mỗi router đi qua trừ TTL đi 1, nên:

- `ttl=64` từ máy Linux → không qua router nào (cùng mạng, hoặc chính mình).
- `ttl=117` → có thể máy Windows (128) cách khoảng 11 hop.
- `ttl=55` → có thể máy Linux (64) cách khoảng 9 hop.

Đây chỉ là ước lượng, vì TTL ban đầu có thể bị cấu hình khác.

### 3. Mất gói (`packet loss`)

- `0%` → bình thường.
- Mất vài phần trăm → mạng chập chờn, quá tải, Wi-Fi yếu.
- `100%` → không liên lạc được, **hoặc** đích chặn ICMP.

### 4. Các thông báo lỗi và ý nghĩa

|Thông báo|Ý nghĩa|Kiểm tra|
|---|---|---|
|`Network is unreachable`|Kernel **không có route** tới đích|`ip route` — thiếu default route?|
|`Destination Host Unreachable`|Có route, nhưng **không tìm được MAC** của đích/gateway (ARP thất bại)|`ip neigh` — thấy `FAILED`/`INCOMPLETE`?|
|`Temporary failure in name resolution`|Lỗi **DNS**, không đổi được tên ra IP|Thử ping bằng IP; xem `/etc/resolv.conf`|
|Không có dòng nào, chỉ treo|Gói đi được nhưng không có trả lời: bị firewall chặn hoặc đích không tồn tại|Thử đích khác, thử `traceroute`|
|`Time to live exceeded`|Gói hết TTL giữa đường, có thể vòng lặp định tuyến|`traceroute`|

### 5. Quy trình kiểm tra mạng bằng ping

Đi từ gần ra xa, bước nào hỏng thì lỗi nằm ở đó:

```bash
ping -c 2 127.0.0.1        # 1. TCP/IP stack của máy hoạt động?
ping -c 2 10.0.0.20        # 2. IP của chính mình (xem bằng ip addr)
ping -c 2 10.0.0.253       # 3. Gateway (xem bằng ip route | grep default)
ping -c 2 8.8.8.8          # 4. Internet bằng IP
ping -c 2 google.com       # 5. Internet bằng tên → kiểm tra DNS
```

- Bước 4 được mà bước 5 không → lỗi DNS.
- Gateway trên cloud có thể không trả lời ping; nếu bước 3 thất bại mà bước 4 vẫn được thì mạng vẫn ổn.

## Ghi nhớ

- `ping` = "có tới được không, mất bao lâu".
- Nhìn 3 thứ: **có phản hồi không**, **time**, **packet loss**.
- Ping là công cụ tầng 3: không thay thế được việc kiểm tra dịch vụ (dùng `ss`, `curl`, `nc` cho việc đó).