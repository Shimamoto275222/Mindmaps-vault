Sắp xếp các dòng của file text (hoặc stdin) rồi in ra.

```bash
# sort [options] [file...]
# không có file → đọc từ stdin
sort names.txt
```

## 1. Các option chính

```bash
# -n     : sắp xếp theo số (numeric sort)
# -t c   : ký tự phân tách field (delimiter), mặc định là khoảng trắng
# -k N   : sắp xếp theo field N (tính tới cuối dòng)
# -k N,N : chỉ dùng đúng field N
# -r     : sắp xếp ngược (reverse)
# -u     : bỏ dòng trùng sau khi sắp xếp
sort -n numbers.txt
sort -r names.txt
sort -u names.txt
```

## 2. ⭐ Sắp xếp theo field

Input `~/project/student_records.txt` (Tên:Tuổi):

```text
David Lee:21
Alice Johnson:18
Charlie Brown:19
Bob Smith:20
Eve Wilson:18
```

```bash
# theo tuổi tăng dần
sort -t: -k2,2n ~/project/student_records.txt

# theo tuổi giảm dần, cùng tuổi thì theo tên A→Z
# chữ sau -k (n, r) chỉ áp dụng cho key đó
sort -t: -k2,2nr -k1,1 ~/project/student_records.txt
```

Output của lệnh thứ 2:

```text
David Lee:21
Bob Smith:20
Charlie Brown:19
Alice Johnson:18
Eve Wilson:18
```

⚠️ `-k2` = từ field 2 **tới cuối dòng** → muốn chỉ so field 2 phải ghi `-k2,2`.
⚠️ Thiếu `-n` thì so theo chữ → `10` đứng trước `9`.
