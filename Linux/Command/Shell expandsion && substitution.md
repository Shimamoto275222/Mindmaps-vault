
## 1. Cơ chế Expansion (Mở rộng)

Mỗi khi bạn nhấn `Enter`, shell sẽ quét qua dòng lệnh và thay thế các ký tự đặc biệt bằng một giá trị cụ thể. Lệnh `echo` là công cụ tốt nhất để quan sát cơ chế này.

  

### Pathname Expansion (Mở rộng đường dẫn / Wildcards)

Shell tự động tìm kiếm các tập tin khớp với mẫu (pattern).

```bash

# Hiển thị tất cả tập tin kết thúc bằng .txt

echo *.txt

  

# Hiển thị các tập tin bắt đầu bằng chữ 'D' viết hoa

echo D*

```

  

### Tilde Expansion (Mở rộng dấu ngã)

Ký tự `~` đại diện cho thư mục nhà (home directory) của người dùng hiện tại.

```bash

# Hiển thị đường dẫn thư mục home của bạn

echo ~

  

# Hiển thị đường dẫn thư mục home của người dùng 'john'

echo ~john

```

  

### Arithmetic Expansion (Mở rộng toán học)

Shell có thể tính toán các biểu thức số nguyên bằng cú pháp `$(( biểu_thức ))`.

```bash

# Tính toán cơ bản

echo $((2 + 2))

  

# Phép tính phức tạp hơn

echo $(((5 * 4) / 2))

```

  

### Brace Expansion (Mở rộng dấu ngoặc nhọn)

Tạo ra nhiều chuỗi văn bản dựa trên một khuôn mẫu có sẵn trong `{ }`. Rất hữu ích để tạo nhanh hàng loạt thư mục hoặc tập tin.

```bash

# Tạo các chuỗi từ A đến Z

echo {A..Z}

  

# Tạo danh sách năm và tháng

echo 2026-{01..12}

  

# Kết hợp văn bản ngẫu nhiên

echo Front-{A,B,C}-Back

```

  

### Parameter Expansion (Mở rộng tham số / Biến số)

Shell thay thế tên biến bằng giá trị lưu trữ bên trong nó.

```bash

# Xem giá trị của biến môi trường USER

echo $USER

  

# Xem đường dẫn hệ thống lưu trong biến PATH

echo $PATH

```

  

### Command Substitution (Thay thế lệnh)

Cho phép lấy kết quả đầu ra (output) của một lệnh để làm tham số cho một lệnh khác, sử dụng cú pháp `$(lệnh)`.

```bash

# Hiển thị ngày giờ hiện tại thông qua echo

echo "Hôm nay là $(date)"

  

# Liệt kê chi tiết tập tin thực thi của lệnh cp

ls -l $(which cp)

```

  

---

  

## 2. Cơ chế Quoting (Trích dẫn)

Quoting được sử dụng để kiểm soát hoặc vô hiệu hóa các ký tự đặc biệt, giữ nguyên định dạng của văn bản thô.

  

### Double Quotes (Nháy kép `" "`)

Nháy kép vô hiệu hóa hầu hết các ký tự đặc biệt (như khoảng trắng, dấu `*`, `~`), nhưng **giữ lại hiệu lực** cho dấu `$` (Parameter Expansion), `$(( ))` (Arithmetic Expansion), và `$( )` (Command Substitution).

```bash

# Giữ nguyên các khoảng trắng dư thừa

echo "Từ thứ nhất         Từ thứ hai"

  

# Dấu * mất tác dụng tìm kiếm tập tin, in ra ký tự *

echo "*"

  

# Biến số vẫn được mở rộng bên trong nháy kép

echo "Tên tôi là $USER"

```

  

### Single Quotes (Nháy đơn `' '`)

Nháy đơn **vô hiệu hóa hoàn toàn** tất cả các cơ chế mở rộng của shell. Mọi ký tự bên trong nháy đơn đều biến thành văn bản thô thuần túy.

```bash

# Không mở rộng biến, in ra chuỗi nguyên bản

echo '$USER'  # Kết quả: $USER

  

# Không thực thi lệnh bên trong

echo '$(date)' # Kết quả: $(date)

```

  

### Escape Character (Ký tự thoát `\`)

Dấu gạch chéo ngược `\` dùng để loại bỏ ý nghĩa đặc biệt của **chỉ một ký tự** ngay sau nó.

```bash

# In ra dấu $ thay vì hiểu là biến số

echo "Giá của sản phẩm là \$100"

  

# Dùng để viết các ký tự đặc biệt trong tên file có khoảng trắng

hoanthanh\ file.txt

```