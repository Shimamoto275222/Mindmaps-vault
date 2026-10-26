## 1. Biến đặc biệt

| Biến | Ý nghĩa |
| --- | --- |
| `$0` | tên script (đúng như lúc gọi, vd `./run.sh`) |
| `$1` … `$9` | tham số thứ 1 … 9 |
| `${10}` | từ tham số thứ 10 phải có `{}` (`$10` = `$1` + chữ `0`) |
| ⭐ `$#` | số tham số (không tính `$0`) |
| ⭐ `"$@"` | tất cả tham số, giữ nguyên từng cái |
| `"$*"` | tất cả tham số, gộp thành 1 chuỗi |
| `$?` | exit status của lệnh vừa chạy |
| `$$` | PID của script |

```bash
#!/bin/bash
# my_shopping.sh
echo "Item 3: $3 | Tổng: $# tham số"
echo "A $5 costs just $6."
```

```bash
$ ./my_shopping.sh apple 5 banana 8 "Fruit Basket" 15
Item 3: banana | Tổng: 6 tham số
A Fruit Basket costs just 15.
```

## 2. ⭐ `"$@"` vs `"$*"`

```bash
# ./demo.sh one "two three"
for a in "$@"; do echo "[$a]"; done   # 2 vòng: [one] [two three]  ✅
for a in "$*"; do echo "[$a]"; done   # 1 vòng: [one two three]
for a in $@;   do echo "[$a]"; done   # 3 vòng: [one] [two] [three]  ← vỡ tham số
```

→ Duyệt hoặc chuyển tiếp tham số: luôn dùng `"$@"`.

## 3. shift

`shift` bỏ `$1`, dồn `$2 → $1`, `$3 → $2`…, `$#` giảm 1.

```bash
while [[ $# -gt 0 ]]; do
    echo "Tham số: $1"
    shift
done
```

## 4. Kiểm tra số tham số

```bash
if [[ $# -ne 2 ]]; then
    echo "Cách dùng: $(basename "$0") <nguồn> <đích>" >&2
    exit 1
fi
```

> Trong function, `$1`, `$#`, `$@` là tham số **của function**, không phải của script → [[Function]]

Xem thêm: [[Good_script]] (mẫu xử lý option `-v`, `-o`)
