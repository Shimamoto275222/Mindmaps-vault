> Điều kiện của `if` / `while` thực chất là **exit status** của một lệnh (`0` = true). Cách viết điều kiện: [[Test_expressions]]

## 1. if

```bash
if điều_kiện; then
    lệnh
elif điều_kiện; then
    lệnh
else
    lệnh
fi
```

```bash
score=75
if (( score >= 90 )); then
    echo "Giỏi"
elif (( score >= 50 )); then
    echo "Đạt"          # ← in ra
else
    echo "Trượt"
fi
```

## 2. while / until

```bash
while điều_kiện; do     # lặp KHI điều kiện còn đúng
    lệnh
done

until điều_kiện; do     # lặp CHO ĐẾN KHI điều kiện đúng
    lệnh
done
```

```bash
count=1
while (( count <= 3 )); do
    echo "Lần $count"   # Lần 1, Lần 2, Lần 3
    count=$((count + 1))
done
```

## 3. for

```bash
for biến in danh_sách; do       # danh_sách: a b c | {1..5} | *.txt | "$@" | "${arr[@]}"
    lệnh
done

for (( i = 0; i < n; i++ )); do # dạng C
    lệnh
done
```

```bash
for f in *.txt; do
    echo "File: $f"
done
```

## 4. case

```bash
case "$biến" in
    pattern1)            lệnh ;;
    pattern2 | pattern3) lệnh ;;    # nhiều pattern cho 1 nhánh
    *)                   lệnh ;;    # mặc định — đặt cuối
esac
```

```bash
read -p "Tiếp tục? [y/n] " answer
case "$answer" in
    [yY] | [yY][eE][sS]) echo "OK" ;;
    [nN] | [nN][oO])     echo "Huỷ" ;;
    *)                   echo "Không hiểu" ;;
esac
```

## 5. break / continue

- `break` → thoát vòng lặp
- `continue` → bỏ qua phần còn lại, sang vòng kế tiếp

Xem thêm: [[Test_expressions]] · [[Good_script]]
