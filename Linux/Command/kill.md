
# Các signal cơ bản của lệnh `kill`

## Cú pháp

kill [-SIGNAL] PID
kill -l          # liệt kê tất cả signal

Có thể gọi signal theo số (`-9`), tên đầy đủ (`-SIGKILL`) hoặc tên rút gọn (`-KILL`).

## Bảng signal hay dùng

| Số  | Tên     | Mặc định  | Ý nghĩa / Khi nào dùng                                                  |
| --- | ------- | --------- | ----------------------------------------------------------------------- |
| 1   | SIGHUP  | Terminate | Terminal bị đóng; nhiều daemon (nginx, sshd…) dùng để **reload config** |
| 2   | SIGINT  | Terminate | Ngắt từ bàn phím (**Ctrl+C**)                                           |
| 3   | SIGQUIT | Core dump | Thoát và tạo core dump (**Ctrl+\\**)                                    |
| 9   | SIGKILL | Terminate | **Buộc dừng ngay**, không thể bắt/bỏ qua; dùng khi process treo         |
| 15  | SIGTERM | Terminate | **Mặc định của `kill`**; yêu cầu dừng lịch sự, cho phép dọn dẹp         |
| 18  | SIGCONT | Continue  | Tiếp tục process đang bị tạm dừng                                       |
| 19  | SIGSTOP | Stop      | Tạm dừng process, không thể bắt/bỏ qua                                  |
| 20  | SIGTSTP | Stop      | Tạm dừng từ bàn phím (**Ctrl+Z**), có thể bắt được                      |
| 10  | SIGUSR1 | Terminate | Signal tùy ứng dụng định nghĩa (vd: xoay vòng log)                      |
| 12  | SIGUSR2 | Terminate | Signal tùy ứng dụng định nghĩa                                          |

> Lưu ý: số của SIGUSR1/2, SIGSTOP, SIGCONT, SIGTSTP có thể khác trên một số kiến trúc/hệ điều hành (vd: macOS, MIPS). Dùng **tên signal** để an toàn hơn.

## Ví dụ

kill 1234              # gửi SIGTERM (15)
kill -9 1234           # buộc dừng
kill -HUP $(pidof nginx)   # reload nginx
kill -STOP 1234        # tạm dừng
kill -CONT 1234        # chạy tiếp
killall -TERM firefox  # gửi theo tên process
pkill -9 -f "python app.py"  # gửi theo pattern

## Thứ tự nên dùng khi dừng process

1. `kill PID` (SIGTERM) và chờ vài giây
2. `kill -INT PID` nếu chưa dừng
3. `kill -9 PID` (SIGKILL) là phương án cuối cùng, vì process không kịp dọn dẹp (file tạm, lock, kết nối…)