Tìm file/thư mục trong cây thư mục theo nhiều tiêu chí (tên, loại, size, thời gian, quyền...) rồi thực hiện action trên kết quả.
Chỉ cần tìm binary / man page của 1 lệnh: xem [[whereis]]

```bash
# find [path...] [expression]
# không có path → mặc định là . (thư mục hiện tại)
find ~ -name "*.txt"
```

## 1. Tìm theo tên

```bash
# -name : so khớp tên file theo glob, phân biệt hoa thường
# -iname: giống -name nhưng không phân biệt hoa thường
# -path : so khớp theo cả đường dẫn
find . -name "*.txt"
find . -iname "readme*"
find . -path "*/src/*" -name "*.js"
```

⚠️ Luôn để pattern trong dấu nháy `"*.txt"` → nếu không, shell sẽ expand `*` trước khi find nhận được.

## 2. Tìm theo loại (`-type`)

```bash
# f: regular file
# d: directory
# l: symbolic link
# b: block device
# c: character device
find . -type f -name "*.txt"
find . -type d -name "config"
find /etc -type l
```

## 3. Tìm theo size, thời gian, quyền, owner

```bash
# -size n[c|k|M|G]: c = byte, k = KB, M = MB, G = GB
#                   +n = lớn hơn n, -n = nhỏ hơn n
# -mtime n : nội dung bị sửa cách đây n ngày (+n: hơn n ngày, -n: trong vòng n ngày)
# -mmin n  : giống -mtime nhưng tính theo phút
# -newer f : được sửa sau file f
# -empty   : file / thư mục rỗng
# -perm m  : quyền đúng bằng m (vd: 0644)
# -user u / -group g : thuộc user / group
find . -type f -size +100M
find /var/log -mtime -7
find . -mmin -30
find . -type f -newer config.txt
find . -type d -empty
find . -type f -perm 0777
find /home -user root
```

## 4. Kết hợp điều kiện (operators)

```bash
# các test đứng cạnh nhau = AND (ngầm định)
# -and / -a : AND
# -or  / -o : OR
# -not / !  : NOT
# \( \)     : nhóm điều kiện, phải escape vì ( ) có nghĩa với shell
find . -type f -name "*.log" -size +10M
find . -type f -not -name "*.md"
find . -type f \( -name "*.jpg" -o -name "*.png" \)
find ~ \( -type f -not -perm 0600 \) -or \( -type d -not -perm 0700 \)
```

⭐ Có `-o` thì gần như luôn cần `\( \)`: `find . -type f -name "*.jpg" -o -name "*.png"` sẽ hiểu là `(file .jpg) OR (.png bất kỳ, kể cả thư mục)`.

## 5. Action trên kết quả

```bash
# -print : in đường dẫn (mặc định khi không có action)
# -ls    : in chi tiết giống ls -dils
# -delete: xoá file match, KHÔNG hỏi lại
# -exec cmd {} \; : chạy cmd cho TỪNG file, {} = đường dẫn file hiện tại
# -exec cmd {} +  : gộp nhiều file vào 1 lần chạy cmd (nhanh hơn)
# -ok cmd {} \;   : giống -exec nhưng hỏi xác nhận trước mỗi file
find . -name "*.tmp" -delete
find . -type f -name "*.sh" -exec chmod +x {} \;
find . -type f -name "*.log" -exec rm {} +
find . -name "*.bak" -ok rm {} \;
```

⚠️ find đánh giá expression từ trái sang phải → `-delete` phải đặt **cuối**. `find . -delete -name "*.tmp"` sẽ xoá TẤT CẢ.
→ Chạy với `-print` trước để kiểm tra, đúng rồi mới đổi sang `-delete`.

## 6. Kết hợp với xargs

```bash
# xargs: nhận danh sách từ stdin → biến thành argument cho lệnh khác
find . -type f -name "*.log" | xargs rm

# tên file có khoảng trắng → dùng -print0 + xargs -0 (phân tách bằng ký tự null)
find . -type f -name "*.log" -print0 | xargs -0 rm
find . -name "*.py" -print0 | xargs -0 grep -n "TODO"
```

## 7. Giới hạn phạm vi tìm

```bash
# -maxdepth n: chỉ đi sâu tối đa n cấp (1 = chỉ trong thư mục hiện tại)
# -mindepth n: bỏ qua các cấp nhỏ hơn n (1 = bỏ qua chính thư mục gốc)
# -xdev / -mount: không đi sang filesystem khác (bỏ qua mount point)
# -prune: không đi vào thư mục match
# các option -maxdepth, -mindepth, -xdev nên đặt trước các test
find . -maxdepth 1 -type f
find / -xdev -name "core"
find . -name node_modules -prune -o -type f -name "*.js" -print
```

⭐ Combo hay dùng:

```bash
find / -name "nginx.conf" 2>/dev/null                    # tìm toàn hệ thống, ẩn lỗi Permission denied
find /var/log -type f -name "*.log" -mtime +30 -delete    # xoá log cũ hơn 30 ngày
find . -type f -size +100M -exec ls -lh {} +              # liệt kê file > 100MB
find . -type f \( -name "*.jpg" -o -name "*.png" \) | wc -l   # đếm số ảnh
```
