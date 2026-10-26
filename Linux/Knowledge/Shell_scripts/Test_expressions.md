## 1. Exit status

- Mỗi lệnh khi kết thúc trả về exit status: ⭐ `0` = thành công = **true**, khác `0` = **false**
- `$?` = exit status của lệnh vừa chạy; script trả về bằng `exit n`, function bằng `return n`
- `if` / `while` chạy một **lệnh** rồi xét exit status → lệnh nào cũng làm điều kiện được

```bash
if grep -q root /etc/passwd; then echo "Có user root"; fi
```

## 2. Ba cách viết điều kiện

| Dạng | Dùng cho | Ghi chú |
| --- | --- | --- |
| `[ expr ]` (= `test expr`) | file, chuỗi, số | POSIX, chạy mọi shell. `[` là một lệnh → bắt buộc có dấu cách: `[ "$a" = 1 ]` |
| ⭐ `[[ expr ]]` | như `[ ]` + wildcard `==`, regex `=~` | Của bash, không bị tách từ → an toàn hơn |
| ⭐ `(( expr ))` | số nguyên | Viết `<` `>` `==` như toán, biến không cần `$` |

## 3. Kiểm tra file

| Biểu thức | True khi |
| --- | --- |
| `-e f` | tồn tại |
| ⭐ `-f f` | là file thường |
| ⭐ `-d f` | là thư mục |
| `-L f` | là symlink |
| `-r` / `-w` / `-x` | có quyền đọc / ghi / thực thi |
| `-s f` | kích thước > 0 |
| `f1 -nt f2` | `f1` mới hơn `f2` |

## 4. So sánh chuỗi

| Biểu thức | True khi |
| --- | --- |
| ⭐ `-z s` | chuỗi rỗng |
| ⭐ `-n s` | chuỗi khác rỗng |
| `s1 == s2` / `s1 != s2` | bằng / khác |
| `[[ $s == *.txt ]]` | khớp wildcard (pattern **không** để trong nháy) |
| `[[ $s =~ ^[0-9]+$ ]]` | khớp regex; nhóm bắt được nằm trong mảng `BASH_REMATCH` |

## 5. So sánh số nguyên

| `[ ]` / `[[ ]]` | `(( ))` | Ý nghĩa |
| --- | --- | --- |
| `-eq` / `-ne` | `==` / `!=` | bằng / khác |
| `-lt` / `-le` | `<` / `<=` | nhỏ hơn / ≤ |
| `-gt` / `-ge` | `>` / `>=` | lớn hơn / ≥ |

> [!warning]
> `[[ 10 > 9 ]]` → **false**, vì `>` trong `[[ ]]` so sánh **chuỗi**. So số thì dùng `-gt` hoặc `(( 10 > 9 ))`.

## 6. Kết hợp điều kiện

```bash
[[ $n -ge 1 && $n -le 100 ]]     # AND
(( n < 1 || n > 100 ))           # OR
[[ ! -d backup ]]                # NOT

# && / || giữa các lệnh = if viết tắt
[[ -d backup ]] || mkdir backup  # chưa có thì tạo
cd /some/dir || exit 1           # cd lỗi thì thoát
```

## 7. Lỗi hay gặp

- `[$a = 1]` → thiếu dấu cách → `[1: command not found`
- `[ $a = x ]` khi `a` rỗng → `unary operator expected` → viết `"$a"` hoặc dùng `[[ ]]`
- `[[ $a=x ]]` → thiếu dấu cách quanh `=` → **luôn true**
- `[ 10 > 9 ]` → `>` thành redirect, tạo ra file tên `9`

Xem thêm: [[Flow_control]]
