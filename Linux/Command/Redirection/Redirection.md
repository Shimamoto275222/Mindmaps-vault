## 1. File descriptor (fd)

| fd  | Tên    | Mặc định trỏ tới |
| --- | ------ | ---------------- |
| `0` | stdin  | bàn phím         |
| `1` | stdout | màn hình         |
| `2` | stderr | màn hình         |

## 2. Cú pháp

| Viết              | Nghĩa                                     |
| ----------------- | ----------------------------------------- |
| `> file`          | stdout → file (ghi đè)                    |
| `>> file`         | stdout → file (nối thêm)                  |
| `2> file`         | stderr → file                             |
| ⭐ `2> /dev/null` | bỏ thông báo lỗi                          |
| ⭐ `> file 2>&1`  | cả stdout + stderr → file                 |
| `&> file`         | như trên (cách viết riêng của bash)       |
| ⭐ `>&2`          | stdout → stderr (= `1>&2`)                |
| `< file`          | stdin ← file                              |
| `<<"EOF"`         | stdin ← nhiều dòng gõ trực tiếp (heredoc) |
| `cmd1 \| cmd2`    | stdout của `cmd1` → stdin của `cmd2`      |
| `cmd \| tee file` | vừa ghi file vừa hiện màn hình            |

Cách đọc `n>&m`: **fd `n` trỏ tới chỗ fd `m` đang trỏ**. Không ghi `n` thì `>` = fd `1`, `<` = fd `0`.

> [!warning] Bẫy
>
> - Thiếu `&`: `>2` tạo **file tên "2"**, không phải stderr
> - Thứ tự xử lý từ trái sang phải:
>   - `cmd > f 2>&1` → cả hai vào file ✅
>   - `cmd 2>&1 > f` → stderr đã trỏ ra màn hình trước khi stdout đổi sang file → lỗi vẫn hiện màn hình ❌

## 3. Trong function / `$( )`

`$( )` nối fd `1` vào biến, fd `2` giữ nguyên → log trong function phải ghi `>&2`.

```bash
get_square() {
    echo "đang tính..." >&2      # ra màn hình
    echo $(( $1 * $1 ))          # vào biến
}

x=$(get_square 5)                # x=25, log hiện màn hình
x=$(get_square 5 2>/dev/null)    # bỏ log
x=$(get_square 5 2>&1)           # gộp log vào x
```

Xem thêm: [[Function]], [[Good_script]]
