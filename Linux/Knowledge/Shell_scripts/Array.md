## 1. Khai báo & truy cập

```bash
NAMES=(John Eric Jessica)   # cách nhau bằng dấu cách, KHÔNG dùng dấu phẩy
NUMBERS=()                  # mảng rỗng

echo ${NAMES[1]}       # Eric           (index từ 0)
echo ${NAMES[-1]}      # Jessica        phần tử cuối
echo ${NAMES[@]}       # John Eric Jessica
echo ${#NAMES[@]}      # 3              số phần tử
echo ${!NAMES[@]}      # 0 1 2          danh sách index
echo ${NAMES[@]:1:2}   # Eric Jessica   cắt: từ index 1, lấy 2
```

- `@` = tất cả phần tử · `#` phía trước = đếm · `!` phía trước = lấy index
- ⚠️ Bắt buộc có `{}`: `$NAMES[1]` → `John[1]`

## 2. Thêm / sửa / xoá

```bash
NUMBERS+=(1)         # thêm vào cuối → (1)
NUMBERS+=(2 3)       # → (1 2 3)
NUMBERS[0]=10        # sửa → (10 2 3)
unset 'NUMBERS[1]'   # xoá → (10 3), index còn lại là 0 2 (KHÔNG dồn lên)
```

- ⚠️ `NUMBERS+=4` (thiếu ngoặc) → nối chuỗi vào phần tử đầu thành `104`

## 3. Duyệt mảng

```bash
FRUITS=("red apple" banana)

for f in "${FRUITS[@]}"; do echo "$f"; done                  # theo giá trị
for i in "${!FRUITS[@]}"; do echo "$i: ${FRUITS[i]}"; done   # theo index
```

- ⭐ Luôn viết `"${arr[@]}"` có nháy — thiếu nháy thì `red apple` bị tách thành 2

## 4. Tạo mảng từ file / lệnh

```bash
files=(*.txt)                  # từ wildcard
mapfile -t lines < notes.txt   # mỗi dòng → 1 phần tử
```

## 5. Associative array (key là chuỗi)

```bash
declare -A capital=([vn]=Hanoi [jp]=Tokyo)   # bắt buộc declare -A
capital[fr]=Paris
echo "${capital[vn]}"                         # Hanoi
for k in "${!capital[@]}"; do echo "$k → ${capital[$k]}"; done   # thứ tự không đảm bảo
```

Xem thêm: [[Script_arguments]] (`"$@"` vs `"$*"` — giống `"${arr[@]}"` vs `"${arr[*]}"`)
