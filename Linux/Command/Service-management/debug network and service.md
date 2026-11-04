
# Case debug: "Website không truy cập được"

Một tình huống rất thường gặp khi quản trị server Linux, kết hợp các lệnh đã học: `systemctl`, `journalctl`, `ss`, `ip`, `ping`.

> Output trong case này là ví dụ minh họa. Khi tự thực hành, chi tiết (PID, thời gian, IP) sẽ khác.

## Tình huống

Server chạy **nginx** để phục vụ website. Sau khi cài thêm vài phần mềm và khởi động lại máy, người dùng báo website không vào được.

```bash
$ curl http://10.0.0.20
curl: (7) Failed to connect to 10.0.0.20 port 80 after 0 ms: Connection refused
```

`Connection refused` nghĩa là gói tin **tới được máy**, nhưng **không có chương trình nào nghe port 80** (hoặc firewall từ chối chủ động). Nếu là mạng hỏng, ta thường thấy timeout chứ không phải refused.

## Tư duy chung: đi từ dưới lên theo tầng

|Bước|Câu hỏi|Lệnh|
|---|---|---|
|1|Mạng có thông không? (tầng Link, Internet)|`ip -br addr`, `ip route`, `ping`|
|2|Dịch vụ có đang chạy không?|`systemctl status`|
|3|Vì sao nó không chạy?|`journalctl -u`|
|4|Có nghe đúng port, đúng địa chỉ không? (tầng Transport)|`ss -tulpn`|
|5|Ứng dụng có trả lời đúng không? (tầng Application)|`curl`|

Nguyên tắc: **xác nhận tầng dưới ổn rồi mới lên tầng trên**, tránh mất thời gian sửa nhầm chỗ.

---

## Bước 1 — Kiểm tra mạng

```bash
$ ip -br addr
lo        UNKNOWN   127.0.0.1/8 ::1/128
eth0      UP        10.0.0.20/24 metric 100 fe80::216:3eff:fe04:3f69/64

$ ip route | grep default
default via 10.0.0.253 dev eth0 proto dhcp src 10.0.0.20 metric 100

$ ping -c 2 8.8.8.8
2 packets transmitted, 2 received, 0% packet loss
```

**Kết luận:** `eth0` UP, có IP `10.0.0.20`, có default route, ra Internet được → **mạng ổn**. Kết hợp với lỗi `Connection refused`, vấn đề nằm ở dịch vụ.

## Bước 2 — Kiểm tra dịch vụ

```bash
$ systemctl status nginx
× nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor preset: enabled)
     Active: failed (Result: exit-code) since Thu 2026-11-05 09:12:33 UTC; 3min ago
    Process: 2101 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=1/FAILURE)
        CPU: 21ms

Nov 05 09:12:31 labex systemd[1]: Starting A high performance web server...
Nov 05 09:12:33 labex systemd[1]: nginx.service: Control process exited, code=exited, status=1/FAILURE
Nov 05 09:12:33 labex systemd[1]: Failed to start A high performance web server.
```

**Đọc:**

- `enabled` → nginx **có được cấu hình tự chạy khi boot**. Vậy không phải do quên enable.
- `Active: failed (Result: exit-code)` → nginx **đã thử khởi động nhưng tự thoát với lỗi**.
- Các dòng log ở đây chỉ là của `systemd[1]`, chỉ nói "thất bại", **chưa nói vì sao** → cần xem log đầy đủ.

## Bước 3 — Tìm nguyên nhân trong log

```bash
$ journalctl -u nginx -b --no-pager
Nov 05 09:12:31 labex systemd[1]: Starting A high performance web server...
Nov 05 09:12:31 labex nginx[2101]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Nov 05 09:12:32 labex nginx[2101]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Nov 05 09:12:33 labex nginx[2101]: nginx: [emerg] still could not bind()
Nov 05 09:12:33 labex systemd[1]: nginx.service: Control process exited, code=exited, status=1/FAILURE
Nov 05 09:12:33 labex systemd[1]: Failed to start A high performance web server.
```

**Đọc:** dòng quan trọng là dòng của chính `nginx[2101]`, mức `[emerg]`:

> `bind() to 0.0.0.0:80 failed (98: Address already in use)`

→ nginx muốn nghe port 80 nhưng **port đã bị chương trình khác chiếm**.

## Bước 4 — Tìm ai đang chiếm port 80

```bash
$ sudo ss -tlnp 'sport = :80'
State  Recv-Q Send-Q Local Address:Port Peer Address:Port Process
LISTEN 0      511          0.0.0.0:80        0.0.0.0:*     users:(("apache2",pid=980,fd=4),("apache2",pid=979,fd=4))
```

**Đọc:** `apache2` (một web server khác) đang nghe `0.0.0.0:80`. Nhiều khả năng Apache được cài kèm theo khi cài phần mềm khác (ví dụ cài PHP), và được bật tự chạy. Sau khi reboot, Apache khởi động **trước** nginx và chiếm port.

Xác nhận:

```bash
$ systemctl is-enabled apache2
enabled
$ systemctl is-active apache2
active
```

## Bước 5 — Sửa lỗi

Không cần Apache → dừng và tắt tự chạy để lần boot sau không tái diễn:

```bash
sudo systemctl disable --now apache2
```

Khởi động lại nginx:

```bash
sudo systemctl start nginx
```

(Nếu systemctl báo `start-limit-hit` vì đã thất bại nhiều lần, chạy `sudo systemctl reset-failed nginx` trước.)

## Bước 6 — Kiểm chứng

```bash
$ systemctl is-active nginx
active

$ sudo ss -tlnp 'sport = :80'
LISTEN 0      511          0.0.0.0:80        0.0.0.0:*     users:(("nginx",pid=3120,fd=6),("nginx",pid=3119,fd=6))

$ curl -I http://10.0.0.20
HTTP/1.1 200 OK
Server: nginx/1.24.0
```

- nginx `active`, chính nginx đang nghe port 80 trên `0.0.0.0` (mọi địa chỉ) → máy khác vào được.
- `curl` nhận `200 OK` → website hoạt động.

Cuối cùng, nên **reboot thử** (nếu được phép) để chắc chắn sau khởi động mọi thứ vẫn đúng: `systemctl is-enabled nginx` phải là `enabled`, `apache2` là `disabled`.

---

## Các biến thể thường gặp của case này

Cùng quy trình trên, nhưng nguyên nhân khác:

|Dấu hiệu|Nguyên nhân|Hướng xử lý|
|---|---|---|
|`status` là `inactive (dead)` + `disabled`|Dịch vụ chưa được enable, reboot xong không chạy|`sudo systemctl enable --now nginx`|
|Log có `[emerg] unknown directive` hoặc `syntax error`|Sai cú pháp file cấu hình|Kiểm tra bằng `sudo nginx -t`, sửa file, rồi `restart`|
|Log có `Permission denied`|Sai quyền file/thư mục, hoặc chạy port < 1024 không có quyền|Kiểm tra quyền bằng `ls -l`, user trong unit file|
|`ss` thấy nghe `127.0.0.1:80` thay vì `0.0.0.0:80`|Dịch vụ chỉ nghe localhost: trên máy curl được, máy khác không vào được|Sửa địa chỉ listen trong cấu hình|
|Dịch vụ chạy, nghe `0.0.0.0:80`, nhưng từ ngoài bị **timeout**|Firewall chặn (`ufw`, `firewalld`, security group trên cloud)|`sudo ufw status`, kiểm tra security group|
|`status` là `activating (auto-restart)` lặp lại|Dịch vụ crash liên tục và được tự khởi động lại|`journalctl -u <tên> -f` để bắt lỗi lúc nó chết|

## Mẹo phân biệt nhanh lỗi phía client

|Lỗi khi kết nối|Ý nghĩa thường gặp|Nhìn vào đâu|
|---|---|---|
|`Connection refused`|Tới được máy, nhưng **không ai nghe port**|`systemctl status`, `ss -tulpn`|
|Timeout (treo rồi hết giờ)|Gói tin **bị chặn hoặc không tới nơi**|Firewall, `ip route`, `ping`, `traceroute`|
|`Could not resolve host`|Lỗi **DNS**|Thử bằng IP; `/etc/resolv.conf`|
|Nhận được `502 Bad Gateway`|nginx chạy, nhưng **ứng dụng phía sau** (backend) lỗi|`systemctl status` và `journalctl` của backend|

## Tóm tắt quy trình

```
curl lỗi
 └─ ip addr / ip route / ping   → mạng ổn?
     └─ systemctl status        → dịch vụ chạy không? enabled không?
         └─ journalctl -u       → vì sao lỗi? (tìm dòng của chính chương trình)
             └─ ss -tulpn       → ai nghe port? nghe địa chỉ nào?
                 └─ sửa → start → kiểm chứng lại bằng ss + curl
```