
# `ip address` — Địa chỉ IP trên interface

## Dùng để làm gì

Xem và quản lý **địa chỉ IP** (tầng Internet / tầng 3) được gán lên các interface.

Kết quả gồm mọi thông tin của `ip link` **cộng thêm** địa chỉ IPv4/IPv6. Đây là lệnh dùng nhiều nhất để trả lời câu hỏi: _"Máy tôi đang có IP gì?"_

Viết tắt: `ip address` = `ip addr` = `ip a`

## Các lệnh hay dùng

```bash
ip address show              # tất cả interface, dạng đầy đủ
ip -br addr                  # dạng gọn
ip -br -c addr               # dạng gọn, có màu
ip addr show dev eth0        # chỉ một interface
ip -4 addr                   # chỉ IPv4
ip -6 addr                   # chỉ IPv6

sudo ip addr add 192.168.50.10/24 dev eth1   # thêm địa chỉ
sudo ip addr del 192.168.50.10/24 dev eth1   # xóa địa chỉ
```

## Đọc kết quả dạng gọn (`ip -br addr`)

```
lo        UNKNOWN   127.0.0.1/8 ::1/128
eth0      UP        10.0.0.123/24 metric 100 fe80::216:3eff:fe02:c3dc/64
docker0   DOWN      172.17.0.1/16
```

|Cột|Ý nghĩa|
|---|---|
|1|Tên interface|
|2|Trạng thái|
|3+|Các địa chỉ IPv4 và IPv6, kèm prefix (`/24`, `/64`)|

## Đọc kết quả dạng đầy đủ (`ip addr show`)

```
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 00:16:3e:02:c3:dc brd ff:ff:ff:ff:ff:ff
    inet 10.0.0.123/24 brd 10.0.0.255 scope global dynamic eth0
       valid_lft 315000000sec preferred_lft 315000000sec
    inet6 fe80::216:3eff:fe02:c3dc/64 scope link
       valid_lft forever preferred_lft forever
```

Hai dòng đầu giống `ip link`. Phần mới:

|Phần|Ý nghĩa|
|---|---|
|`inet`|Địa chỉ IPv4|
|`inet6`|Địa chỉ IPv6|
|`10.0.0.123/24`|Địa chỉ IP và độ dài prefix (subnet mask)|
|`brd 10.0.0.255`|Địa chỉ broadcast của mạng|
|`scope`|Phạm vi sử dụng của địa chỉ, xem bên dưới|
|`dynamic`|Địa chỉ được cấp qua **DHCP** (không có chữ này → IP tĩnh)|
|`valid_lft`|Thời gian còn hiệu lực của địa chỉ|
|`preferred_lft`|Thời gian địa chỉ còn được ưu tiên dùng làm nguồn|

## ⭐ Các thông tin cần chú ý

### 1. Địa chỉ IP và prefix

`10.0.0.123/24` nghĩa là:

- IP của máy: `10.0.0.123`
- Mạng: `10.0.0.0/24` → các máy từ `10.0.0.1` đến `10.0.0.254` cùng mạng LAN, gửi trực tiếp không qua router.
- `/24` tương đương subnet mask `255.255.255.0`.

Khi gán địa chỉ này, kernel **tự động tạo route** `10.0.0.0/24 dev eth0 proto kernel` (xem trong `ip route`).

### 2. Loại địa chỉ — nhận biết nhanh

|Địa chỉ|Loại|Ghi chú|
|---|---|---|
|`127.0.0.1/8`, `::1/128`|Loopback|Máy tự nói chuyện với chính nó|
|`10.x.x.x`, `172.16–31.x.x`, `192.168.x.x`|IPv4 private|Không đi thẳng ra Internet, cần NAT qua router|
|`172.17.0.1/16` trên `docker0`|Mạng Docker|Gateway cho các container|
|`fe80::/64`|IPv6 link-local|Tự sinh trên mọi interface, chỉ dùng trong cùng đoạn mạng|
|`2xxx:...`|IPv6 toàn cục|Có cái này mới ra Internet bằng IPv6 được|

### 3. `scope`

|Giá trị|Ý nghĩa|
|---|---|
|`global`|Dùng được cho mọi đích, kể cả ngoài mạng|
|`link`|Chỉ dùng trong cùng đoạn mạng (ví dụ `fe80::`)|
|`host`|Chỉ dùng trong chính máy (ví dụ `127.0.0.1`)|

Mẹo: nếu `ip -6 addr` chỉ có địa chỉ `scope link` mà không có `scope global` → máy **không có IPv6 ra Internet**, và `ip -6 route` sẽ không có default route.

### 4. `dynamic` — IP do DHCP cấp

- Có `dynamic` → địa chỉ được cấp tự động, có thời hạn (`valid_lft`), có thể thay đổi khi khởi động lại hoặc hết hạn.
- Ví dụ thực tế: môi trường lab mỗi phiên lại nhận IP khác (`10.0.0.123`, `10.0.0.150`, `10.0.0.20`...).
- `forever` → địa chỉ tĩnh hoặc tự sinh, không hết hạn.

### 5. Một interface có thể có nhiều địa chỉ

Một interface có thể vừa có IPv4 vừa có IPv6, hoặc có nhiều IPv4 cùng lúc. Mỗi địa chỉ là một dòng `inet` / `inet6` riêng.

## Ghi nhớ

- `ip address` = "interface đang mang địa chỉ IP gì".
- Nhìn 3 thứ: **địa chỉ + prefix**, **scope**, **dynamic hay tĩnh**.