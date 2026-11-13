In đường dẫn tuyệt đối của thư mục hiện tại (print working directory).

```bash
# pwd [-L | -P]
# không option → -L (pwd của bash)
# -L (logical) : hiện đường dẫn đã dùng để đi tới thư mục hiện tại, giữ nguyên tên symbolic link
# -P (physical): hiện thư mục thật trên đĩa sau khi resolve symbolic link
ln -s /var/log ~/logs
cd ~/logs
pwd -L    # → /home/user1/logs
pwd -P    # → /var/log
```
