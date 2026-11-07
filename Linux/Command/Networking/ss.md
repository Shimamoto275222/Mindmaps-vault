
# `ss` — Xem socket và kết nối mạng

## Dùng để làm gì

Liệt kê các **socket** trên máy: dịch vụ nào đang **lắng nghe** (listen) trên port nào, những **kết nối** nào đang mở, tới đâu.

`ss` làm việc ở **tầng Transport (TCP/UDP)**: nơi có port, khác với `ip` (tầng Link/Internet) và `ping` (ICMP).

Dùng để trả lời: _"Dịch vụ web/SSH có đang chạy và nghe đúng port không?"_, _"Máy đang kết nối tới đâu?"_

`ss` là bản thay thế hiện đại của `netstat` (gói `net-tools`, đã cũ), nhanh hơn và thường có sẵn trong gói `iproute2` cùng với `ip`.

## Các tùy chọn cơ bản

| Tùy chọn    | Ý nghĩa                                                              |
| ----------- | -------------------------------------------------------------------- |
| `-t`        | TCP                                                                  |
| `-u`        | UDP                                                                  |
| `-l`        | Chỉ socket đang **lắng nghe**                                        |
| `-a`        | Tất cả (cả lắng nghe lẫn đã kết nối)                                 |
| `-n`        | Hiện số (IP, port), không đổi sang tên → nhanh và rõ                 |
| `-p`        | Hiện **tiến trình** sở hữu socket (cần `sudo` để thấy của user khác) |
| `-4` / `-6` | Chỉ IPv4 / IPv6                                                      |
| `-s`        | Thống kê tổng hợp                                                    |

## Các lệnh hay dùng

```bash
sudo ss -tulpn               # ⭐ lệnh quan trọng nhất: dịch vụ nào nghe port nào
ss -tan                      # mọi kết nối TCP
ss -tn                       # chỉ kết nối TCP đã thiết lập (mặc định không có -a, -l)
ss -s                        # thống kê tổng
ss -tlnp 'sport = :22'       # ai đang nghe port 22
ss -tn state established     # chỉ kết nối đang hoạt động
ss -tn dst 8.8.8.8           # kết nối tới một IP cụ thể
ss -tn '( dport = :443 )'    # kết nối ra port 443
```

Mẹo nhớ `-tulpn`: **t**cp, **u**dp, **l**isten, **p**rocess, **n**umeric.

## Đọc kết quả `sudo ss -tulpn`

```
Netid State  Recv-Q Send-Q  Local Address:Port  Peer Address:Port Process
udp   UNCONN 0      0       127.0.0.53%lo:53         0.0.0.0:*     users:(("systemd-resolve",pid=512,fd=13))
udp   UNCONN 0      0      10.0.0.20%eth0:68         0.0.0.0:*     users:(("systemd-network",pid=480,fd=19))
tcp   LISTEN 0      4096    127.0.0.53%lo:53         0.0.0.0:*     users:(("systemd-resolve",pid=512,fd=14))
tcp   LISTEN 0      128           0.0.0.0:22         0.0.0.0:*     users:(("sshd",pid=801,fd=3))
tcp   LISTEN 0      511         127.0.0.1:3000       0.0.0.0:*     users:(("node",pid=1530,fd=20))
tcp   LISTEN 0      128              [::]:22            [::]:*     users:(("sshd",pid=801,fd=4))
```

|Cột|Ý nghĩa|
|---|---|
|`Netid`|Loại socket: `tcp`, `udp`, `unix`...|
|`State`|Trạng thái kết nối, xem bên dưới|
|`Recv-Q` / `Send-Q`|Hàng đợi nhận / gửi, xem bên dưới|
|`Local Address:Port`|Địa chỉ và port **phía máy mình**|
|`Peer Address:Port`|Địa chỉ và port **phía bên kia**. `*` = chưa có ai (đang chờ)|
|`Process`|Tên chương trình, PID, file descriptor|

## ⭐ Các thông tin cần chú ý

### 1. Địa chỉ đang lắng nghe — ai kết nối vào được?

Đây là điểm **quan trọng nhất** khi đọc `ss -tulpn`:

|Local Address|Ý nghĩa|
|---|---|
|`0.0.0.0:22`|Nghe trên **mọi IPv4** của máy → máy khác kết nối vào được|
|`[::]:22`|Nghe trên **mọi IPv6** (thường kèm cả IPv4)|
|`*:80`|Nghe trên mọi địa chỉ|
|`127.0.0.1:3000`|**Chỉ nghe localhost** → chỉ chương trình trên chính máy này kết nối được|
|`127.0.0.53%lo:53`|DNS resolver nội bộ của systemd, chỉ trên `lo`|
|`10.0.0.20:8080`|Chỉ nghe trên một IP cụ thể|

Lỗi kinh điển: chạy web app trong container hoặc VM, từ ngoài vào không được → kiểm tra `ss` thấy app nghe `127.0.0.1` thay vì `0.0.0.0`.

### 2. Trạng thái (`State`)

|State|Ý nghĩa|
|---|---|
|`LISTEN`|Dịch vụ TCP đang **chờ kết nối**|
|`ESTAB`|Kết nối **đang hoạt động**|
|`TIME-WAIT`|Kết nối vừa đóng, đang chờ hết hạn. Nhiều cái là bình thường với server bận|
|`CLOSE-WAIT`|Phía kia đã đóng nhưng **chương trình của mình chưa đóng**. Nhiều và tăng dần → nghi lỗi trong ứng dụng|
|`SYN-SENT`|Đang cố kết nối đi, chưa có trả lời. Kẹt lâu → đích không phản hồi/bị chặn|
|`SYN-RECV`|Nhận yêu cầu kết nối, đang bắt tay. Rất nhiều → có thể bị tấn công SYN flood|
|`UNCONN`|Socket UDP (UDP không có kết nối nên không có LISTEN/ESTAB)|

### 3. `Recv-Q` và `Send-Q`

Ý nghĩa khác nhau tùy trạng thái:

|Trạng thái|`Recv-Q`|`Send-Q`|
|---|---|---|
|`LISTEN`|Số kết nối đang chờ được ứng dụng chấp nhận|Kích thước tối đa hàng đợi đó (backlog)|
|`ESTAB`|Dữ liệu đã nhận nhưng ứng dụng **chưa đọc**|Dữ liệu đã gửi nhưng **chưa được xác nhận**|

- Bình thường cả hai gần bằng **0**.
- `Recv-Q` lớn và tăng → ứng dụng xử lý không kịp.
- `Send-Q` lớn kéo dài → mạng chậm hoặc phía kia không nhận kịp.

### 4. Cột `Process`

- Cho biết **chương trình nào** đang giữ port: `sshd`, `nginx`, `node`...
- Không thấy cột này hoặc trống → thiếu `sudo` (không xem được tiến trình của user khác).
- Hữu ích khi gặp lỗi `Address already in use`: tìm xem ai đang chiếm port.

```bash
sudo ss -tlnp 'sport = :8080'
```

### 5. Port thường gặp

|Port|Dịch vụ|
|---|---|
|22|SSH|
|53|DNS|
|67/68|DHCP (68 là phía client, thấy trên máy nhận IP động)|
|80 / 443|HTTP / HTTPS|
|3306 / 5432|MySQL / PostgreSQL|
|6379|Redis|

## Đọc kết nối đang hoạt động (`ss -tn`)

```
State  Recv-Q Send-Q   Local Address:Port    Peer Address:Port
ESTAB  0      0            10.0.0.20:22      100.104.12.7:51432
ESTAB  0      0            10.0.0.20:41822   142.250.66.78:443
```

- Dòng 1: port local là **22** (port dịch vụ) → có người đang **SSH vào** máy này từ `100.104.12.7`.
- Dòng 2: port local là số cao ngẫu nhiên, port phía kia là **443** → máy này đang **kết nối ra** một website HTTPS.

Quy tắc: bên nào dùng **port dịch vụ cố định** là server, bên dùng **port cao ngẫu nhiên** (32768–60999) là client.

## Ghi nhớ

- `ss` = "dịch vụ nào đang nghe, kết nối nào đang mở" (tầng Transport, có port).
- Lệnh cần nhớ: `sudo ss -tulpn`.
- Nhìn 3 thứ: **địa chỉ nghe** (`0.0.0.0` hay `127.0.0.1`), **State**, **Process**.
- Quy trình gỡ lỗi "không truy cập được dịch vụ": `ping` (tới được máy chưa) → `ss -tulpn` trên server (dịch vụ có nghe đúng port, đúng địa chỉ không) → firewall.