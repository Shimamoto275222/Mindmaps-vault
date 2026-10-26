## 1. Cú pháp

```bash
name() {
    lệnh
}

function name {     # cách viết khác (chỉ có ở bash)
    lệnh
}
```

- Khai báo **trước** khi gọi
- Gọi như một lệnh, **không** có ngoặc: `name arg1 arg2`

```bash
greet() {
    echo "Xin chào, $1!"
}
greet "Linux"       # Xin chào, Linux!
```

## 2. Tham số

Bên trong function, `$1`, `$2`, `$#`, `"$@"` là tham số **của function**, không phải của script (`$0` vẫn là tên script).

```bash
sum() {
    echo $(( $1 + $2 ))
}
sum 3 5             # 8
```

## 3. Trả kết quả

- `return n` → chỉ trả **exit status** (0–255), dùng cho đúng / sai
- Không có `return` → exit status của lệnh cuối cùng trong function
- Muốn trả **dữ liệu** → in ra bằng `echo` / `printf`, nơi gọi lấy bằng `$(...)`

```bash
is_even() {
    (( $1 % 2 == 0 ))           # exit status của lệnh này = kết quả function
}
if is_even 4; then echo "chẵn"; fi

get_ext() {
    echo "${1##*.}"
}
ext=$(get_ext "photo.jpg")      # jpg
```

> [!warning]
> Mọi thứ function in ra stdout đều bị `$(...)` gom vào kết quả → thông báo / log trong function phải ghi ra stderr (`>&2`).

## 4. ⭐ Biến `local`

Biến trong function mặc định là **global** → dễ ghi đè biến bên ngoài. Luôn khai báo `local`.

```bash
name="global"
change() {
    local name="local"          # chỉ tồn tại trong function
    echo "Trong: $name"
}
change                          # Trong: local
echo "Ngoài: $name"             # Ngoài: global
```

## 5. Lỗi hay gặp

- `return "abc"` → lỗi `numeric argument required`; `return 256` → thành `0` (chỉ giữ 0–255)
- `local x=$(cmd)` → `$?` luôn là `0` (exit status của `local`, không phải của `cmd`) → tách thành `local x; x=$(cmd)`
- Đặt tên function trùng lệnh có sẵn (`ls`, `test`…) → che mất lệnh đó

Xem thêm: [[Script_arguments]] · [[Good_script]] (chia script thành function + `main`)
