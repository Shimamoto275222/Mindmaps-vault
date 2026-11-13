Xem nội dung file theo từng trang (tốt hơn `more`: cuộn ngược được, tìm kiếm được, nhanh với file lớn).

```bash
# less [file]
less /etc/passwd
ls -l /usr/bin | less
```

## 1. Các option chính

```bash
# -N: hiện số dòng
# -i: tìm kiếm không phân biệt hoa thường
# -S: không wrap dòng dài (cuộn trái/phải bằng phím mũi tên)
# +/pattern: mở file và nhảy tới match đầu tiên (dùng được cả với `more`)
less +/ERROR large_log.txt
```

## 2. Phím điều hướng

Các phím dưới đây bấm **bên trong** less, không phải gõ làm argument của lệnh.

```bash
# --- Cuộn ---
Space / f / PgDn    # trang tiếp
b / PgUp            # trang trước
d                   # xuống nửa trang
u                   # lên nửa trang
j / ↓ / Enter       # dòng tiếp
k / ↑               # dòng trước

# --- Nhảy ---
g / Home            # đầu file
G / End             # cuối file
50g                 # tới dòng 50
50p                 # tới vị trí 50% file

# --- Tìm kiếm ---
/pattern            # tìm xuôi
?pattern            # tìm ngược
n                   # match tiếp theo
N                   # match trước đó
&pattern            # chỉ hiện các dòng match pattern

# --- Khác ---
F                   # follow mode, giống `tail -f` (Ctrl+C để dừng)
v                   # mở file bằng $EDITOR
h                   # trợ giúp
q                   # thoát
```
