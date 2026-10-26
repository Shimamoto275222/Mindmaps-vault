## 1. Gán & đọc biến

```bash
PRICE_PER_APPLE=5                # KHÔNG có dấu cách quanh =
greeting='Hello        world!'
today=$(date +%F)                # kết quả của lệnh
total=$((PRICE_PER_APPLE * 3))   # kết quả phép tính → 15

echo $PRICE_PER_APPLE            # đọc giá trị: thêm $ phía trước
```

- `PRICE = 5` → lỗi `PRICE: command not found` (shell hiểu là chạy lệnh `PRICE`)
- Tên biến: chữ, số, `_`, không bắt đầu bằng số, phân biệt hoa/thường
- Mọi giá trị đều là chuỗi; biến chưa gán = chuỗi rỗng (không báo lỗi)

## 2. Escape `\$`

```bash
echo "The price of an Apple today is: \$HK $PRICE_PER_APPLE"
# The price of an Apple today is: $HK 5
```

## 3. `${var}` — tách tên biến khỏi chữ phía sau

```bash
MyFirstLetters=ABC
echo "${MyFirstLetters}DEFGHIJ"   # ABCDEFGHIJ
echo "$MyFirstLettersDEFGHIJ"     # (rỗng) — shell tìm biến tên MyFirstLettersDEFGHIJ
```

## 4. ⭐ Luôn bọc biến bằng nháy kép

```bash
echo $greeting      # Hello world!          — bị tách từ, mất khoảng trắng
echo "$greeting"    # Hello        world!   — giữ nguyên
```

> [!warning]
> `file="my report.txt"; rm $file` → xoá 2 file `my` và `report.txt`. Phải viết `rm "$file"`.

## 5. export / readonly / unset

```bash
export city="Hanoi"   # biến môi trường → tiến trình con cũng thấy
readonly PI=3.14      # hằng số, gán lại sẽ báo lỗi
unset city            # xoá biến
```

Biến có sẵn: `$HOME`, `$USER`, `$PATH`, `$PWD`. Xem tất cả: `printenv`.

Xem thêm: [[Parameter_expansion]] · [[Shell_expansion_and_substitution]] (quoting)
