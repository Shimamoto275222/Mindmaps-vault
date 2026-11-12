Cắt/trích xuất cột (field) hoặc ký tự từ mỗi dòng của file text.

```bash
# cut [options] [file...]
# không có file → đọc từ stdin
cut -d ':' -f1 /etc/passwd     # lấy username
```

## 1. Các option chính

```bash
# -d 'c': delimiter - ký tự phân tách (mặc định là TAB), chỉ được 1 ký tự
# -f N  : lấy field thứ N sau khi phân tách
# -f 1,3 / -f 2-4 / -f 3- : nhiều field, khoảng, từ field 3 đến hết
# -c N  : cắt theo vị trí ký tự thay vì field
# -s    : bỏ qua dòng không chứa delimiter
# --complement : lấy tất cả TRỪ các field đã chọn
cut -d ',' -f1,3 data.csv
cut -c 1-10 file.txt
cut -d ':' -f1 --complement /etc/passwd
```

## 2. ⭐ Phân tích access.log với `-d '"'`

Dùng dấu ngoặc kép `"` làm delimiter → lấy được các phần nằm giữa các cặp `"` trong log Nginx/Apache.

```bash
cut -d '"' -f2 access.log
```

- `-d '"'`: phân tách theo dấu `"` → mỗi dòng bị chia thành nhiều field
- `-f2`: lấy field thứ 2 = nội dung trong cặp `"` đầu tiên → **request** (HTTP method, URL, protocol)

Ví dụ 1 dòng log Nginx:

```text
127.0.0.1 - - [11/Nov/2026:18:29:00 +0700] "GET /index.html HTTP/1.1" 200 3426 "-" "Mozilla/5.0"
```

Các field khi tách theo `"`:

```bash
# -f1: trước " thứ 1          → 127.0.0.1 - - [11/Nov/2026:18:29:00 +0700]
# -f2: giữa " thứ 1 và thứ 2  → GET /index.html HTTP/1.1      (request)
# -f3: giữa " thứ 2 và thứ 3  →  200 3426                     (status, size)
# -f4: giữa " thứ 3 và thứ 4  → -                             (referer)
# -f6: cặp " thứ 3            → Mozilla/5.0                   (User-Agent)
```

Output của `cut -d '"' -f2 access.log`:

```text
GET /index.html HTTP/1.1
```

## 3. Kết hợp với sort, uniq

```bash
# top 10 request được gọi nhiều nhất (kèm số lần)
cut -d '"' -f2 access.log | sort | uniq -c | sort -nr | head -n 10

# thống kê User-Agent (trình duyệt / bot) - field 6 nếu log format chuẩn
cut -d '"' -f6 access.log | sort | uniq -c
```

⚠️ Vị trí field phụ thuộc vào log format cấu hình trên server → kiểm tra 1 dòng log trước khi chọn `-f`.
