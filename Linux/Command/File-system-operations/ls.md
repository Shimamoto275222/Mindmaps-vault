Liệt kê nội dung thư mục.

```bash
# ls [options] [file/dir...]
# không có đối số → thư mục hiện tại
# -a: all, hiện cả file/thư mục ẩn
# -A: all, nhưng bỏ . và ..
# -l: long format
# -R: recursive
# -t: sắp xếp theo thời gian sửa (modification)
# -r: reverse, đảo thứ tự (vd -tr)
# -d: chỉ hiện chính thư mục, không hiện nội dung bên trong
ls -la
ls -lA /etc
ls -R src/
ls -ltr /var/log    # file sửa gần nhất nằm cuối
ls -ld /etc
```
