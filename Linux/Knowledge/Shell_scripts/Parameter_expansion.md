## 1. Giá trị mặc định

| Cú pháp | `var` rỗng / chưa gán | `var` có giá trị |
| --- | --- | --- |
| ⭐ `${var:-x}` | dùng `x` | dùng `$var` |
| `${var:=x}` | dùng `x` **và gán** `var=x` | dùng `$var` |
| `${var:?msg}` | báo lỗi `msg` & **thoát script** | dùng `$var` |
| `${var:+x}` | rỗng | dùng `x` |

```bash
dir="${1:-.}"                      # tham số 1, không có thì dùng "."
: "${API_KEY:?Chưa đặt API_KEY}"   # thiếu biến → dừng script (':' = lệnh không làm gì)
```

## 2. Xử lý chuỗi

### Cắt đầu / cuối chuỗi: `#` và `%`

`#`, `%` là **toán tử cắt chuỗi** (không phải expression), phía sau là một **pattern**:

```text
${ file  %   .*  }
   │     │   └── pattern: "." rồi đến chuỗi bất kỳ
   │     └────── toán tử: cắt phần CUỐI khớp pattern
   └──────────── tên biến
```

| Toán tử | Cắt ở | Lấy đoạn khớp |
| --- | --- | --- |
| `#` | đầu chuỗi | ngắn nhất |
| `##` | đầu chuỗi | dài nhất |
| `%` | cuối chuỗi | ngắn nhất |
| `%%` | cuối chuỗi | dài nhất |

Từng bước với `file="photo.backup.jpg"`:

| Cú pháp | Đoạn khớp pattern | Phần còn lại |
| --- | --- | --- |
| `${file#*.}` | `photo.` | `backup.jpg` |
| `${file##*.}` | `photo.backup.` | `jpg` |
| `${file%.*}` | `.jpg` | `photo.backup` |
| `${file%%.*}` | `.backup.jpg` | `photo` |

> [!warning] Pattern là wildcard, KHÔNG phải regex
> - `.` là dấu chấm thật, không phải "ký tự bất kỳ" như trong regex
> - `*` là "chuỗi bất kỳ", không phải "lặp lại ký tự phía trước"
> - `?` là đúng 1 ký tự bất kỳ

### Bảng tổng hợp

Ví dụ `file="photo.backup.jpg"`:

| Cú pháp | Kết quả | Ý nghĩa |
| --- | --- | --- |
| `${#file}` | `16` | độ dài |
| `${file:0:5}` | `photo` | cắt từ vị trí 0, lấy 5 ký tự |
| `${file#*.}` | `backup.jpg` | cắt đầu, ngắn nhất |
| ⭐ `${file##*.}` | `jpg` | cắt đầu, dài nhất → lấy đuôi file |
| ⭐ `${file%.*}` | `photo.backup` | cắt cuối, ngắn nhất → bỏ đuôi file |
| `${file%%.*}` | `photo` | cắt cuối, dài nhất |
| `${file/o/0}` | `ph0to.backup.jpg` | thay lần đầu |
| `${file//o/0}` | `ph0t0.backup.jpg` | thay tất cả |
| `${file^^}` / `${file,,}` | `PHOTO.BACKUP.JPG` / `photo.backup.jpg` | viết hoa / viết thường |

> Mẹo: trên bàn phím `#` nằm bên **trái** `$` → cắt đầu chuỗi; `%` nằm bên **phải** → cắt cuối chuỗi.

```bash
f="holiday.jpeg"
mv "$f" "${f%.jpeg}.jpg"     # holiday.jpeg → holiday.jpg
```

### Cùng ký hiệu, khác nghĩa

| Viết | Nghĩa |
| --- | --- |
| `${#file}` | `#` **trước** tên biến → độ dài chuỗi |
| `${file#pat}` | `#` **sau** tên biến → cắt đầu chuỗi |
| `$#` | số tham số |
| `# ...` | comment |
| `$(( 10 % 3 ))` | trong `$(( ))`, `%` là chia lấy dư → `1` |

Xem thêm: [[Shell_variables]]
