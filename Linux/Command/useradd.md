Tạo user mới.

```bash
# sudo useradd [options] user
# -m: đảm bảo tạo kèm home dir
# -d: đặt home dir
# -U: tạo primary group cùng tên
sudo useradd user1
sudo useradd -m user1
sudo useradd -d /home/user1 user1
sudo useradd -m -U user1
```
