Đổi owner (user) và group của file / thư mục.

```bash
# sudo chown [user]:[group] [file/dir]
# bỏ :group → chỉ đổi user; chỉ ghi :group → chỉ đổi group
# -R: đổi ownership đệ quy
sudo chown user1:dev report.txt
sudo chown -R www-data:www-data /var/www/html
```
