Liệt kê **từng router (hop)** mà gói tin đi qua trên đường tới đích, kèm độ trễ tới mỗi hop.

Dùng để trả lời: _"Gói tin bị nghẽn hoặc mất ở đâu trên đường đi?"_, điều mà `ping` không cho biết.

```bash
# traceroute [options] DEST
traceroute -n 8.8.8.8
```

## 1. Nguyên lý hoạt động

traceroute lợi dụng trường **TTL** trong header IP:

1. Gửi gói với `TTL=1` → router đầu tiên trừ TTL về 0, hủy gói và gửi lại thông báo **ICMP Time Exceeded** → biết được hop 1.
2. Gửi gói với `TTL=2` → router thứ hai trả lời → biết hop 2.
3. Tăng dần TTL cho tới khi tới được đích (đích trả lời bằng ICMP Port Unreachable hoặc Echo Reply).

Mỗi hop được thử **3 lần**, nên mỗi dòng có 3 giá trị thời gian.

Trên Linux, traceroute mặc định gửi gói **UDP** tới port cao (33434+). Windows (`tracert`) dùng ICMP.

## 2. Cài đặt

Nhiều hệ thống tối giản không có sẵn:

```bash
sudo apt install traceroute      # Debian/Ubuntu
```

Lựa chọn thay thế thường có sẵn: `tracepath` (không cần root), `mtr` (traceroute + ping liên tục).

## 3. Các lệnh hay dùng

```bash
traceroute 8.8.8.8               # mặc định (UDP)
traceroute -n 8.8.8.8            # không phân giải tên → nhanh hơn nhiều
sudo traceroute -I 8.8.8.8       # dùng ICMP (giống Windows)
sudo traceroute -T -p 443 example.com   # dùng TCP tới port 443, xuyên firewall tốt hơn
traceroute -m 20 8.8.8.8         # tối đa 20 hop (mặc định 30)
traceroute -w 2 8.8.8.8          # chờ mỗi phản hồi tối đa 2 giây
traceroute -q 1 8.8.8.8          # chỉ thử 1 lần mỗi hop

tracepath -n 8.8.8.8             # tương tự, kèm thông tin MTU
mtr -n 8.8.8.8                   # theo dõi liên tục, thống kê mất gói từng hop
mtr -n -r -c 20 8.8.8.8          # chạy 20 lượt rồi in báo cáo
```

## 4. Đọc kết quả

```text
traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 60 byte packets
 1  10.0.0.253  0.512 ms  0.480 ms  0.455 ms
 2  * * *
 3  11.73.4.21  1.210 ms  1.198 ms  1.302 ms
 4  116.251.80.5  2.034 ms  1.987 ms  2.110 ms
 5  72.14.215.85  35.402 ms  35.380 ms  35.511 ms
 6  8.8.8.8  35.920 ms  35.874 ms  35.903 ms
```

|Phần|Ý nghĩa|
|---|---|
|`30 hops max`|Số hop tối đa sẽ thử|
|`60 byte packets`|Kích thước gói dò|
|Số đầu dòng|Thứ tự hop (= giá trị TTL đã dùng)|
|IP / tên|Router đã trả lời ở hop đó|
|3 giá trị `ms`|Độ trễ đi và về của 3 lần thử|
|`* * *`|Không nhận được phản hồi trong thời gian chờ|

## 5. ⭐ Các thông tin cần chú ý

### 1. Hop đầu tiên = default gateway

Hop 1 luôn là gateway của máy, chính là địa chỉ sau `via` trong `default via ...` của `ip route`. Ví dụ ở trên: `10.0.0.253`.

Nếu hop 1 đã `* * *` mãi → vấn đề nằm ngay trong mạng nội bộ hoặc gateway không trả lời.

### 2. `* * *` — không phải lúc nào cũng là lỗi

|Tình huống|Ý nghĩa|
|---|---|
|`* * *` ở giữa, nhưng các hop sau vẫn hiện bình thường|Router đó **không trả lời ICMP** (cấu hình chặn hoặc giới hạn), gói vẫn đi qua được. **Bình thường**, đặc biệt trong mạng cloud|
|Từ một hop trở đi **toàn bộ** là `* * *`|Gói bị chặn/mất từ đó, hoặc firewall chặn UDP/ICMP. Thử lại với `-I` hoặc `-T`|
|Không bao giờ tới đích, nhưng ping đích lại được|Đích/firewall chặn kiểu gói traceroute đang dùng. Thử `-I` hoặc `-T -p 443`|

### 3. Độ trễ — tìm chỗ tăng đột biến

- Độ trễ thường **tăng dần** theo hop.
- Một bước nhảy lớn (ví dụ từ ~2 ms lên ~35 ms ở hop 5) thường là lúc gói **đi ra khỏi khu vực**: sang nhà mạng khác, qua cáp quốc tế.
- Một hop có độ trễ cao nhưng **các hop sau lại thấp hơn** → không phải nghẽn thật, chỉ là router đó xử lý gói ICMP chậm (ưu tiên thấp). Chỉ lo khi độ trễ cao **kéo dài tới tận đích**.

### 4. Địa chỉ IP lạ ở các hop

- `10.x.x.x`, `11.x.x.x`, `100.64–127.x.x`... → mạng nội bộ của nhà cung cấp cloud hoặc nhà mạng.
- Các IP ở cuối hành trình thường thuộc nhà mạng hoặc dịch vụ đích.
- Bỏ `-n` để xem tên (reverse DNS), đôi khi tên chứa gợi ý về vị trí hoặc nhà mạng, nhưng sẽ chậm hơn.

### 5. Ba giá trị thời gian khác IP

Đôi khi một hop hiện nhiều IP khác nhau trên cùng một dòng: gói được **cân bằng tải** qua nhiều đường song song. Không phải lỗi.

## 6. So sánh nhanh

|Công cụ|Ưu điểm|
|---|---|
|`traceroute`|Linh hoạt, chọn được UDP/ICMP/TCP|
|`tracepath`|Không cần root, cho biết MTU trên đường đi|
|`mtr`|Chạy liên tục, thống kê mất gói từng hop → tốt nhất để chẩn đoán mạng chập chờn|

## 7. Ghi nhớ

- `traceroute` = "gói tin đi qua những đâu, chậm hoặc mất ở chặng nào".
- Hop 1 là default gateway.
- `* * *` ở giữa thường vô hại; chỉ đáng lo khi kéo dài tới cuối.
- Luôn dùng `-n` cho nhanh, trừ khi cần xem tên.
