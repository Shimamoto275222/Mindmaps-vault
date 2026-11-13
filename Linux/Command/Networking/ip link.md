Xem và điều khiển các **network interface** của kernel ở tầng Link (tầng 2): tên interface, trạng thái bật/tắt, địa chỉ MAC, MTU, các cờ.

`ip link` **không hiển thị địa chỉ IP** → muốn xem IP dùng `ip address`.

Interface là khái niệm của kernel, không nhất thiết là card mạng thật: `lo` (loopback), `docker0` (bridge ảo), `veth...` (cặp interface ảo của container) đều là interface.

```bash
# ip [options] link show [dev IFACE]
# ip link set IFACE {up | down | mtu N}
ip -br link
```

## 1. Các lệnh hay dùng

```bash
ip link show                 # liệt kê tất cả interface (dạng đầy đủ)
ip -br link                  # dạng gọn, mỗi interface một dòng
ip -br -c link               # dạng gọn, có màu
ip link show dev eth0        # chỉ xem một interface
ip -s link show dev eth0     # kèm thống kê gói tin gửi/nhận, lỗi

sudo ip link set eth0 up     # bật interface
sudo ip link set eth0 down   # tắt interface (đừng làm với eth0 trên máy remote!)
sudo ip link set eth0 mtu 1400
```

## 2. Đọc kết quả dạng gọn (`ip -br link`)

```text
lo        UNKNOWN   00:00:00:00:00:00 <LOOPBACK,UP,LOWER_UP>
eth0      UP        00:16:3e:02:c3:dc <BROADCAST,MULTICAST,UP,LOWER_UP>
docker0   DOWN      02:42:60:99:4a:96 <NO-CARRIER,BROADCAST,MULTICAST,UP>
```

|Cột|Ý nghĩa|
|---|---|
|1|Tên interface|
|2|Trạng thái hoạt động (operstate)|
|3|Địa chỉ MAC|
|4|Các cờ (flags)|

## 3. Đọc kết quả dạng đầy đủ (`ip link show`)

```text
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP mode DEFAULT group default qlen 1000
    link/ether 00:16:3e:02:c3:dc brd ff:ff:ff:ff:ff:ff
```

|Phần|Ý nghĩa|
|---|---|
|`2:`|Số thứ tự (index) của interface trong kernel|
|`eth0`|Tên interface|
|`<...>`|Các cờ, xem bảng bên dưới|
|`mtu 1500`|Kích thước tối đa một gói tin (byte). 1500 là chuẩn Ethernet|
|`qdisc fq_codel`|Thuật toán xếp hàng gói tin khi gửi đi|
|`state UP`|Trạng thái hoạt động|
|`qlen 1000`|Độ dài hàng đợi gửi|
|`link/ether`|Loại liên kết (Ethernet) và địa chỉ MAC|
|`brd ff:ff:...`|Địa chỉ MAC broadcast|

## 4. ⭐ Các thông tin cần chú ý

### 1. Trạng thái (`state`)

|Giá trị|Ý nghĩa|
|---|---|
|`UP`|Interface hoạt động bình thường|
|`DOWN`|Interface bị tắt, hoặc bật nhưng không có kết nối|
|`UNKNOWN`|Kernel không xác định được. **Bình thường với `lo`**|

### 2. Cờ `UP` và `LOWER_UP` — phân biệt quan trọng

|Cờ|Ý nghĩa|
|---|---|
|`UP`|Interface đã được **bật về mặt phần mềm** (`ip link set ... up`)|
|`LOWER_UP`|Có **kết nối vật lý thực sự** (cáp cắm, link thông)|
|`NO-CARRIER`|Đã bật nhưng **không có tín hiệu**: rút cáp, hoặc bridge chưa có gì nối vào|

Cách chẩn đoán nhanh:

- Có `UP` + `LOWER_UP` → tầng Link ổn, nếu mạng hỏng thì tìm lỗi ở tầng trên (IP, route).
- Có `UP` nhưng `NO-CARRIER` → vấn đề vật lý: cáp, switch, Wi-Fi chưa kết nối.
- Không có `UP` → interface chưa được bật.

Ví dụ: `docker0` có `UP` nhưng `NO-CARRIER` và state `DOWN` → **không có container nào đang chạy**. Đây không phải lỗi.

### 3. Địa chỉ MAC

- Định danh của interface ở tầng Link, dùng trong frame Ethernet.
- 3 byte đầu cho biết nhà sản xuất. Ví dụ `00:16:3e` là dải của Xen → máy ảo trên cloud; `02:42` là MAC do Docker sinh ra.
- `lo` có MAC toàn số 0 vì không phải card thật.

### 4. MTU

- Thông thường là 1500. Nếu thấy giá trị lạ (1450, 9001...) thường do mạng ảo, VPN, hoặc jumbo frame.
- MTU không khớp giữa hai đầu có thể gây lỗi khó hiểu: ping nhỏ được nhưng tải trang web bị treo.

## 5. Ghi nhớ

- `ip link` = "card mạng có tồn tại không, có bật không, có cắm không".
- Khi gỡ lỗi mạng, kiểm tra `ip link` **đầu tiên**, rồi mới tới `ip address` và `ip route`.
- Thay đổi bằng `ip link set` là **tạm thời**, mất sau khi reboot hoặc bị trình quản lý mạng (NetworkManager, systemd-networkd) ghi đè.
