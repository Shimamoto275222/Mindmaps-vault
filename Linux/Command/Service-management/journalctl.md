systemd thu thập log từ kernel, từ mọi dịch vụ và từ quá trình khởi động vào một nơi gọi là **journal**. `journalctl` là công cụ để đọc và lọc journal đó.

Dùng để trả lời: _"Vì sao dịch vụ này lỗi?"_, _"Lúc máy boot đã xảy ra gì?"_, _"Trong 10 phút qua có lỗi gì?"_

Khác với file log văn bản truyền thống trong `/var/log/`, journal lưu ở dạng nhị phân có cấu trúc, nên lọc theo dịch vụ, thời gian, mức độ rất dễ.

```bash
# journalctl [options] [FIELD=value...]
# không option → toàn bộ journal, cũ nhất trước
journalctl -u nginx -e
```

## 1. Quyền đọc log

- Người dùng thường chỉ thấy log của chính mình.
- Muốn thấy log hệ thống: dùng `sudo`, hoặc thêm user vào nhóm `adm` / `systemd-journal`.

## 2. Các lệnh hay dùng

### Theo dịch vụ

```bash
journalctl -u nginx              # ⭐ toàn bộ log của dịch vụ nginx
journalctl -u nginx -e           # nhảy tới cuối (log mới nhất)
journalctl -u nginx -n 50        # 50 dòng cuối
journalctl -u nginx -f           # ⭐ theo dõi trực tiếp (như tail -f), Ctrl+C để thoát
journalctl -u nginx -u php-fpm   # nhiều dịch vụ cùng lúc
```

### Theo thời gian

```bash
journalctl --since "10 min ago"
journalctl --since "1 hour ago" --until "30 min ago"
journalctl --since today
journalctl --since "2026-11-05 09:00" --until "2026-11-05 10:00"
```

### Theo lần khởi động

```bash
journalctl -b                    # từ lần boot hiện tại
journalctl -b -1                 # lần boot trước (cần journal lưu lâu dài)
journalctl --list-boots          # danh sách các lần boot
journalctl -k                    # chỉ log kernel (giống dmesg)
```

### Theo mức độ nghiêm trọng

```bash
journalctl -p err                # mức err trở lên (err, crit, alert, emerg)
journalctl -p warning -b         # cảnh báo trở lên kể từ lần boot này
journalctl -p err -u nginx --since today
```

### Định dạng và tiện ích

```bash
journalctl -u nginx -x           # thêm giải thích cho một số thông điệp
journalctl -u nginx --no-pager   # in thẳng ra, không qua trình xem (tiện để grep)
journalctl -u nginx -o short-precise   # thời gian chính xác tới micro giây
journalctl -u nginx -o json-pretty     # xem toàn bộ trường dữ liệu của mỗi bản ghi
journalctl _PID=1205             # lọc theo PID
journalctl _COMM=sshd            # lọc theo tên chương trình
journalctl --disk-usage          # journal đang chiếm bao nhiêu dung lượng
sudo journalctl --vacuum-time=7d # xóa log cũ hơn 7 ngày
```

Các bộ lọc **kết hợp được với nhau**: `journalctl -u nginx -p err --since "1 hour ago"`.

## 3. Trình xem mặc định

Khi không có `-f` hay `--no-pager`, journalctl mở log trong trình xem `less`:

|Phím|Tác dụng|
|---|---|
|`Space` / `b`|Trang tiếp / trang trước|
|`G` / `g`|Cuối / đầu|
|`/từ khóa`|Tìm xuống, `n` để tới kết quả tiếp|
|`→` / `←`|Cuộn ngang (dòng dài bị cắt)|
|`q`|Thoát|

## 4. Đọc kết quả

```text
Nov 05 09:12:31 labex systemd[1]: Starting A high performance web server...
Nov 05 09:12:31 labex nginx[2101]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Nov 05 09:12:33 labex systemd[1]: nginx.service: Control process exited, code=exited, status=1/FAILURE
Nov 05 09:12:33 labex systemd[1]: nginx.service: Failed with result 'exit-code'.
Nov 05 09:12:33 labex systemd[1]: Failed to start A high performance web server.
```

|Phần|Ý nghĩa|
|---|---|
|`Nov 05 09:12:31`|Thời điểm ghi log|
|`labex`|Hostname của máy|
|`systemd[1]` / `nginx[2101]`|**Ai ghi log** và PID của nó|
|Phần còn lại|Nội dung thông điệp|

## 5. ⭐ Các thông tin cần chú ý

### 1. Phân biệt log của systemd và log của chính chương trình

Trong ví dụ trên:

- Các dòng `systemd[1]` chỉ cho biết **kết quả**: dịch vụ khởi động thất bại.
- Dòng `nginx[2101]` mới cho biết **nguyên nhân**: port 80 đã bị chiếm.

→ Khi debug, **bỏ qua các dòng "Failed to start" của systemd và tìm dòng của chính chương trình ngay phía trên**. Đó thường là dòng có giá trị nhất.

### 2. Mức độ nghiêm trọng (priority)

|Số|Tên|Ý nghĩa|
|---|---|---|
|0|`emerg`|Hệ thống không dùng được|
|1|`alert`|Phải xử lý ngay|
|2|`crit`|Nghiêm trọng|
|3|`err`|Lỗi|
|4|`warning`|Cảnh báo|
|5|`notice`|Bình thường nhưng đáng chú ý|
|6|`info`|Thông tin|
|7|`debug`|Gỡ lỗi chi tiết|

`-p err` hiện mức 3 trở xuống (0–3). Khi xem trong terminal, lỗi thường được tô đỏ, cảnh báo tô vàng/đậm.

⚠️ Không phải chương trình nào cũng gắn đúng mức độ. Một số chương trình ghi mọi thứ ở mức `info`, nên lọc bằng `-p err` có thể bỏ sót lỗi thật. Khi nghi ngờ, xem log đầy đủ của dịch vụ.

### 3. Từ khóa nên tìm trong log

Khi đọc log dài, tìm các từ: `error`, `failed`, `fatal`, `emerg`, `denied`, `permission`, `not found`, `refused`, `timeout`, `Address already in use`, `No such file`.

```bash
journalctl -u nginx --no-pager | grep -iE "error|fail|denied"
```

### 4. Log có thể mất sau khi reboot

- Nếu thư mục `/var/log/journal/` tồn tại → journal **lưu lâu dài**, xem được log các lần boot trước.
- Nếu chỉ có `/run/log/journal/` → journal **lưu trong RAM**, mất khi reboot, `journalctl -b -1` báo không có dữ liệu.

Bật lưu lâu dài:

```bash
sudo mkdir -p /var/log/journal
sudo systemctl restart systemd-journald
```

### 5. Không phải log nào cũng vào journal

Một số chương trình vẫn tự ghi file riêng, ví dụ nginx ghi lỗi chi tiết vào `/var/log/nginx/error.log`, Apache vào `/var/log/apache2/`. Nếu journal không đủ thông tin, kiểm tra thêm `/var/log/<tên dịch vụ>/`.

## 6. Ghi nhớ

- `journalctl` = "chuyện gì đã xảy ra" (log), còn `systemctl status` = "tình trạng hiện tại" (trạng thái).
- Ba lệnh dùng nhiều nhất: `journalctl -u <tên> -e`, `journalctl -u <tên> -f`, `journalctl -p err -b`.
- Tìm dòng log **của chính chương trình** ngay trước các dòng "Failed" của systemd.
- Kết hợp bộ lọc dịch vụ + thời gian + mức độ để thu hẹp nhanh.
