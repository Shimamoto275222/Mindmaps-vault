
# `systemctl` — Quản lý dịch vụ với systemd

## Dùng để làm gì

`systemctl` là công cụ điều khiển **systemd**, chương trình đầu tiên chạy khi Linux khởi động (PID 1) và quản lý mọi dịch vụ trên máy.

Dùng để: bật/tắt/khởi động lại dịch vụ, cho dịch vụ tự chạy khi boot, xem trạng thái và lỗi của dịch vụ.

Lưu ý: chỉ có trên hệ thống dùng systemd (Ubuntu, Debian, Fedora, RHEL, Arch...). **Không chạy trong container Docker thông thường** (không có systemd), và trên WSL cần bật systemd trong `/etc/wsl.conf`.

## Khái niệm: Unit

systemd quản lý mọi thứ dưới dạng **unit**. Tên unit có đuôi cho biết loại:

|Loại|Ví dụ|Ý nghĩa|
|---|---|---|
|`.service`|`nginx.service`, `ssh.service`|Dịch vụ / chương trình chạy nền|
|`.socket`|`ssh.socket`|Socket kích hoạt dịch vụ khi có kết nối|
|`.timer`|`apt-daily.timer`|Hẹn giờ chạy (thay cho cron)|
|`.target`|`multi-user.target`|Nhóm unit, tương tự "runlevel"|
|`.mount`|`home.mount`|Điểm mount|

Với `.service` có thể bỏ đuôi: `systemctl status nginx` = `systemctl status nginx.service`.

## Các lệnh hay dùng

### Điều khiển dịch vụ (có hiệu lực ngay)

```bash
sudo systemctl start nginx       # khởi động
sudo systemctl stop nginx        # dừng
sudo systemctl restart nginx     # dừng rồi khởi động lại
sudo systemctl reload nginx      # nạp lại cấu hình, không ngắt dịch vụ (nếu dịch vụ hỗ trợ)
sudo systemctl reload-or-restart nginx
```

### Tự chạy khi khởi động máy

```bash
sudo systemctl enable nginx          # bật tự chạy khi boot (KHÔNG khởi động ngay)
sudo systemctl enable --now nginx    # bật tự chạy + khởi động ngay
sudo systemctl disable nginx         # tắt tự chạy khi boot
sudo systemctl disable --now nginx   # tắt tự chạy + dừng ngay
sudo systemctl mask nginx            # khóa hẳn, không ai start được (kể cả unit khác)
sudo systemctl unmask nginx
```

### Xem trạng thái

```bash
systemctl status nginx               # ⭐ trạng thái chi tiết + vài dòng log gần nhất
systemctl is-active nginx            # in active / inactive / failed (tiện cho script)
systemctl is-enabled nginx           # in enabled / disabled / masked / static
systemctl list-units --type=service              # các service đang được nạp
systemctl list-units --type=service --state=running
systemctl --failed                   # ⭐ các unit bị lỗi
systemctl list-unit-files --type=service         # mọi service và trạng thái enable
```

### Xem và sửa unit file

```bash
systemctl cat nginx                  # ⭐ xem nội dung unit file (kèm các file ghi đè)
sudo systemctl edit nginx            # tạo file ghi đè (drop-in), an toàn hơn sửa file gốc
sudo systemctl daemon-reload         # ⭐ bắt buộc sau khi sửa unit file bằng tay
systemctl list-dependencies nginx    # unit này phụ thuộc những gì
```

## Đọc kết quả `systemctl status`

```
● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor preset: enabled)
     Active: active (running) since Thu 2026-11-05 09:12:31 UTC; 2h 5min ago
       Docs: man:nginx(8)
    Process: 1203 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
   Main PID: 1205 (nginx)
      Tasks: 3 (limit: 4557)
     Memory: 5.2M
        CPU: 48ms
     CGroup: /system.slice/nginx.service
             ├─1205 "nginx: master process /usr/sbin/nginx -g daemon on; master_process on;"
             └─1206 "nginx: worker process"

Nov 05 09:12:31 labex systemd[1]: Starting A high performance web server...
Nov 05 09:12:31 labex systemd[1]: Started A high performance web server...
```

|Dòng|Ý nghĩa|
|---|---|
|`●`|Chấm tròn: xanh = đang chạy, trắng = không chạy, đỏ = lỗi|
|`Loaded:`|Đường dẫn unit file; **enabled/disabled** (có tự chạy khi boot không)|
|`vendor preset`|Mặc định của nhà phân phối khi mới cài|
|`Active:`|**Trạng thái hiện tại** và thời điểm bắt đầu|
|`Process:`|Các lệnh phụ đã chạy (ví dụ kiểm tra cấu hình trước khi start) và kết quả|
|`Main PID:`|Tiến trình chính của dịch vụ|
|`Tasks / Memory / CPU`|Tài nguyên dịch vụ đang dùng|
|`CGroup:`|Cây tiến trình thuộc dịch vụ|
|Các dòng cuối|**Log gần nhất** (lấy từ journal)|

## ⭐ Các thông tin cần chú ý

### 1. `enabled` và `active` là hai việc khác nhau

|Nghĩa|Lệnh thay đổi|
|---|---|---|
|**enabled** / disabled|Có **tự chạy khi boot** hay không|`enable` / `disable`|
|**active** / inactive|**Đang chạy ngay lúc này** hay không|`start` / `stop`|

Có đủ 4 kết hợp. Lỗi thường gặp:

- `start` mà quên `enable` → reboot xong dịch vụ không chạy.
- `enable` mà quên `start` → dịch vụ chưa chạy cho tới lần boot sau. → Dùng `enable --now` để làm cả hai.

Các giá trị khác của dòng `Loaded:`:

- `static`: không enable được trực tiếp, chỉ chạy khi unit khác gọi tới.
- `masked`: bị khóa hoàn toàn.

### 2. Dòng `Active:`

|Giá trị|Ý nghĩa|
|---|---|
|`active (running)`|Đang chạy bình thường|
|`active (exited)`|Chạy một lần và đã xong thành công (dịch vụ kiểu oneshot). Bình thường|
|`active (waiting)`|Đang chờ sự kiện (thường là timer)|
|`inactive (dead)`|Không chạy (đã dừng hoặc chưa start)|
|`activating (auto-restart)`|Vừa chết, systemd đang chờ để khởi động lại → nghi bị crash liên tục|
|`failed`|**Lỗi**: start thất bại hoặc tiến trình chết bất thường|

### 3. Mã thoát khi lỗi

```
Active: failed (Result: exit-code) since ...
Process: 2101 ExecStart=/usr/sbin/nginx (code=exited, status=1/FAILURE)
```

|Thông tin|Gợi ý|
|---|---|
|`Result: exit-code`|Chương trình tự thoát với mã lỗi → xem log để biết lý do|
|`Result: signal`|Bị giết bởi tín hiệu (ví dụ `SIGKILL`, `SIGSEGV` = crash)|
|`Result: timeout`|Không khởi động xong trong thời gian cho phép|
|`Result: start-limit-hit`|Khởi động lại thất bại quá nhiều lần liên tiếp, systemd ngừng thử|
|`Result: oom-kill`|Bị kernel giết vì hết bộ nhớ|

Với `start-limit-hit`, sửa lỗi xong cần chạy `sudo systemctl reset-failed nginx` rồi mới start lại được.

### 4. Log trong `status` bị cắt ngắn

`status` chỉ hiện vài dòng cuối và có thể cắt dòng dài. Muốn xem đầy đủ:

```bash
systemctl status nginx -l --no-pager   # không cắt dòng
journalctl -u nginx -e                 # xem toàn bộ log của dịch vụ
```

## Cấu trúc unit file (cơ bản)

```ini
[Unit]
Description=My web app
After=network.target              # chạy sau khi mạng sẵn sàng

[Service]
ExecStart=/usr/bin/node /opt/app/server.js
User=www-data
Restart=on-failure                # tự khởi động lại khi lỗi
Environment=PORT=3000

[Install]
WantedBy=multi-user.target        # enable = chạy khi hệ thống vào chế độ nhiều người dùng
```

Vị trí unit file:

- `/lib/systemd/system/` hoặc `/usr/lib/systemd/system/`: do gói cài đặt tạo, **không sửa trực tiếp**.
- `/etc/systemd/system/`: của quản trị viên, ưu tiên cao hơn. Đặt unit tự viết và file ghi đè ở đây.

Sửa xong luôn chạy: `sudo systemctl daemon-reload` rồi `restart`.

## Ghi nhớ

- `systemctl` = "dịch vụ có chạy không, có tự chạy khi boot không, và điều khiển nó".
- Lệnh đầu tiên khi dịch vụ có vấn đề: `systemctl status <tên>`.
- Phân biệt **enabled** (khi boot) và **active** (ngay bây giờ).
- Sửa unit file → `daemon-reload`.
- Status chỉ cho manh mối; log đầy đủ xem bằng `journalctl -u <tên>`.