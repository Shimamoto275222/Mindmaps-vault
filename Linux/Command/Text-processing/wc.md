Đếm số dòng, từ, ký tự (hoặc byte) của file text.

```bash
# wc [options] [file...]
# không có file → đọc từ stdin
# không option → in cả 3: dòng, từ, byte + tên file
wc /etc/passwd
```

## 1. Các option chính

```bash
# -l: đếm số dòng (thực chất đếm ký tự xuống dòng \n)
# -w: đếm số từ (phân tách bởi khoảng trắng)
# -m: đếm số ký tự (ký tự nhiều byte như tiếng Việt UTF-8 tính là 1)
# -c: đếm số byte
wc -l /etc/passwd
wc -w file.txt
wc -m file.txt
```

## 2. Chỉ lấy con số (dùng trong script)

```bash
# truyền file làm tham số → output kèm tên file
wc -l /etc/passwd      # → 35 /etc/passwd
# đọc từ stdin → chỉ in con số
wc -l < /etc/passwd    # → 35
```

## 3. Kết hợp với lệnh khác

```bash
# đếm số dòng match (tương đương grep -c)
grep 'error' app.log | wc -l
# đếm số mục (file + thư mục) trong thư mục hiện tại
ls | wc -l
# nhiều file → thêm dòng total ở cuối
wc -l *.log
```

⚠️ `-l` đếm số ký tự `\n` → dòng cuối không có `\n` sẽ không được tính.
