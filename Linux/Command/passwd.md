Đổi password của user, cập nhật password trong file `/etc/shadow`.

```bash
# passwd [options] [user]
# không có user → đổi password của chính mình
# -l: khoá user
# -u: mở khoá user
sudo passwd user1
sudo passwd -l user1
sudo passwd -u user1
```
