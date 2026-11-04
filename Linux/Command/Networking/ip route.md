
# `ip route` — Bảng định tuyến

## Dùng để làm gì

Xem và quản lý **bảng định tuyến** của kernel (tầng Internet / tầng 3). Bảng này quyết định: _gói tin tới một đích nào đó sẽ được gửi qua gateway nào, ra interface nào._

Bảng định tuyến là của **kernel, dùng chung cho cả máy**, không nằm trong interface. Interface chỉ xuất hiện như đích đến của quyết định định tuyến (`dev eth0`).

`ip route` **không chứa địa chỉ MAC**. Ánh xạ IP → MAC nằm ở bảng neighbor/ARP (`ip neigh`).

Viết tắt: `ip route` = `ip r`

## Các lệnh hay dùng

```bash
ip route show                # bảng định tuyến IPv4
ip -6 route show             # bảng định tuyến IPv6
ip route | grep default      # xem default gateway
ip route get 8.8.8.8         # một đích cụ thể sẽ đi đường nào
ip neigh                     # bảng ARP: IP → MAC của hàng xóm

sudo ip route add default via 10.0.0.253 dev eth0
sudo ip route add 192.168.100.0/24 via 10.0.0.5
sudo ip route del 192.168.100.0/24
```

Lưu ý: `-br` gần như không có tác dụng với `ip route`, output vẫn ở dạng đầy đủ.

## Ví dụ kết quả

```
default via 10.0.0.253 dev eth0 proto dhcp src 10.0.0.20 metric 100
10.0.0.0/24 dev eth0 proto kernel scope link src 10.0.0.20 metric 100
10.0.0.253 dev eth0 proto dhcp scope link src 10.0.0.20 metric 100
100.100.2.136 via 10.0.0.253 dev eth0 proto dhcp src 10.0.0.20 metric 100
100.100.2.138 via 10.0.0.253 dev eth0 proto dhcp src 10.0.0.20 metric 100
172.17.0.0/16 dev docker0 proto kernel scope link src 172.17.0.1 linkdown
```

## Ý nghĩa các trường

|Trường|Ý nghĩa|
|---|---|
|Đầu dòng (`default`, `10.0.0.0/24`...)|**Đích**: một mạng, một máy, hoặc `default` (mọi đích còn lại)|
|`via 10.0.0.253`|**Next hop**: gửi qua gateway này. Không có `via` → gửi trực tiếp|
|`dev eth0`|Interface đi ra|
|`proto`|Ai tạo ra route này, xem bên dưới|
|`scope link`|Đích nằm trực tiếp trên đoạn mạng, không cần qua router|
|`src 10.0.0.20`|IP nguồn sẽ dùng khi gửi theo route này|
|`metric 100`|Độ ưu tiên: nhiều route cùng đích thì **metric nhỏ hơn được chọn**|
|`linkdown`|Interface của route đang không hoạt động → route tạm không dùng được|

### `proto` — nguồn gốc của route

|Giá trị|Ý nghĩa|
|---|---|
|`kernel`|Kernel tự tạo khi gán địa chỉ IP lên interface|
|`dhcp`|Tạo từ thông tin DHCP server cấp|
|`static`|Do người/cấu hình thêm cố định|
|`ra`|IPv6: học được từ Router Advertisement|
|`boot`|Thêm thủ công bằng `ip route add` (mặc định)|

## ⭐ Các thông tin cần chú ý

### 1. Default route — quan trọng nhất

```
default via 10.0.0.253 dev eth0
```

- Mọi gói tin không khớp route cụ thể nào (ví dụ ra Internet) đều gửi tới gateway `10.0.0.253`.
- **Không có default route → máy không ra được ngoài mạng nội bộ.**
- Router/gateway của máy chính là địa chỉ sau `via` ở dòng này.

### 2. Route có `via` và không có `via`

|Kiểu|Ví dụ|Nghĩa|
|---|---|---|
|Có `via`|`default via 10.0.0.253 dev eth0`|Đích ở xa, gửi qua gateway|
|Không có `via`|`10.0.0.0/24 dev eth0 scope link`|Đích cùng mạng, gửi thẳng tới máy đó|

### 3. Đọc từng dòng trong ví dụ

|Route|Giải thích|
|---|---|
|`default via 10.0.0.253`|Đường ra Internet, do DHCP cấp|
|`10.0.0.0/24 dev eth0 proto kernel`|Mạng LAN, kernel tự tạo khi gán IP `10.0.0.20/24`|
|`10.0.0.253 dev eth0 scope link`|Đảm bảo luôn tới được chính gateway|
|`100.100.2.136/138 via 10.0.0.253`|Route tới DNS server nội bộ của nhà cung cấp cloud, do DHCP đẩy xuống|
|`172.17.0.0/16 dev docker0 ... linkdown`|Mạng container Docker, đang tạm không dùng vì không có container nào chạy|

### 4. Route chọn theo nguyên tắc "khớp cụ thể nhất"

Khi một đích khớp nhiều route, kernel chọn route có **prefix dài nhất** (cụ thể nhất). Ví dụ gửi tới `10.0.0.5`: khớp cả `default` (/0) và `10.0.0.0/24` → chọn `/24`. Dùng `ip route get <IP>` để kernel trả lời trực tiếp thay vì tự đoán.

### 5. Kết hợp với `ip neigh` (ARP)

Khi gửi gói tin tới `8.8.8.8`, kernel làm:

1. Tra `ip route` → dùng `default` → next hop `10.0.0.253`, ra `eth0`.
2. Tra `ip neigh` → MAC của `10.0.0.253` là gì (chưa biết thì gửi ARP hỏi).
3. Đóng frame: **MAC đích = MAC của gateway**, **IP đích vẫn là `8.8.8.8`**.

```
10.0.0.253 dev eth0 lladdr ee:ff:ff:ff:ff:ff REACHABLE
```

- Nhiều route nhưng thường chỉ có ít mục ARP: các route qua cùng một gateway dùng chung **một** mục ARP của gateway.
- Mục ARP chỉ xuất hiện khi máy **thực sự giao tiếp** với hàng xóm đó, và tự hết hạn sau một thời gian.
- Trạng thái thường gặp: `REACHABLE` (đang liên lạc được), `STALE` (lâu chưa xác nhận lại), `FAILED` / `INCOMPLETE` (hỏi ARP mà không ai trả lời).

### 6. IPv6 không có default route

```
::1 dev lo proto kernel metric 256 pref medium
fe80::/64 dev eth0 proto kernel metric 256 pref medium
```

- Chỉ có các route kernel tự tạo → máy **không có IPv6 ra Internet**.
- Thường do mạng không cung cấp IPv6: không có Router Advertisement, máy chỉ có địa chỉ link-local `fe80::`.
- Không phải lỗi cấu hình trên máy.

## Lưu ý khi thực hành

- Route thêm bằng `ip route add` là **tạm thời**, mất khi reboot hoặc bị trình quản lý mạng ghi đè.
- **Không xóa default route trên máy remote**, bạn sẽ mất kết nối.
- Gateway trên cloud có thể không trả lời ping; ping gateway thất bại chưa chắc là mạng hỏng, thử thêm `ping 8.8.8.8`.

## Ghi nhớ

- `ip route` = "gói tin sẽ được gửi đi đâu".
- Nhìn đầu tiên: **có default route không, gateway là gì**.
- `ip route` trả lời _"gửi qua ai"_, `ip neigh` trả lời _"MAC của người đó là gì"_.
- Thứ tự gỡ lỗi mạng: `ip link` → `ip address` → `ip route` → `ip neigh`.