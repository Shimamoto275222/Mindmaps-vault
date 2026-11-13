Chuyển sang user khác (switch user) ngay trong terminal hiện tại.

```bash
# su [-] [user]
# không có user → chuyển sang root
# - : login shell, nạp environment của user đích

# chuyển sang user1
su - user1

# chuyển sang admin
# sudo -i tốt hơn vì tự nạp environment của admin
sudo -i
sudo su
```
