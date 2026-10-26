## 1. Cú pháp

```bash
read [options] [biến...]
```

```bash
read -r name            # chờ người dùng gõ + Enter → lưu vào $name
echo "Chào $name"

read -r                 # không ghi tên biến → lưu vào $REPLY
echo "$REPLY"
```

Nhiều biến → tách theo khoảng trắng, **biến cuối nhận toàn bộ phần còn lại**:

```bash
read -r a b c           # gõ: one two three four
# a=one   b=two   c="three four"
# gõ ít từ hơn số biến → các biến thừa rỗng
```

## 2. Options thường dùng

| Option | Ý nghĩa |
| --- | --- |
| ⭐ `-p "text"` | hiện lời nhắc (prompt) |
| ⭐ `-r` | giữ nguyên dấu `\` (raw) — **nên luôn dùng** |
| `-s` | không hiện ký tự đang gõ (mật khẩu) |
| `-n N` | đọc đủ `N` ký tự là dừng, không cần Enter |
| `-t giây` | timeout — hết giờ thì `read` trả exit status khác 0 |
| `-a mảng` | đọc các từ vào mảng |
| `-e` | sửa dòng đang gõ bằng phím mũi tên, Tab (Readline) |
| `-i "text"` | điền sẵn giá trị gợi ý (đi kèm `-e`) |

> Vì sao luôn dùng `-r`: gõ `C:\new\data` → `read x` cho ra `C:newdata` (mất `\`), `read -r x` giữ nguyên `C:\new\data`.

```bash
read -rp "Tên đăng nhập: " user
read -rsp "Mật khẩu: " pass; echo        # -s không xuống dòng → echo thêm 1 dòng trống
read -rn 1 -p "Tiếp tục? [y/n] " yn; echo
read -ra words -p "Nhập vài từ: "; echo "Có ${#words[@]} từ"
read -re -i "$HOME" -p "Thư mục: " dir

if read -rt 5 -p "Nhập trong 5 giây: " ans; then
    echo "Bạn nhập: $ans"
else
    echo; echo "Hết giờ"
fi
```

## 3. Tách theo ký tự khác: `IFS`

```bash
IFS=: read -r user _ uid _ <<< "root:x:0:0:root:/root:/bin/bash"
echo "$user $uid"       # root 0
```

- `IFS=:` đặt ngay trước `read` → chỉ áp dụng cho lệnh đó
- `<<< "chuỗi"` (here-string) → đưa chuỗi vào làm input cho `read`

## 4. ⚠️ Không pipe vào `read`

```bash
echo "hello" | read -r text
echo "$text"            # (rỗng) — vế sau | chạy trong subshell, biến mất khi xong

read -r text <<< "hello"
echo "$text"            # hello
```

## 5. Kiểm tra dữ liệu nhập

Hỏi lại cho đến khi nhập đúng:

```bash
while true; do
    read -rp "Nhập số từ 1-10: " n
    if [[ $n =~ ^([1-9]|10)$ ]]; then
        break
    fi
    echo "'$n' không hợp lệ, nhập lại." >&2
done
echo "Bạn chọn $n"
```

## 6. Menu: `select`

```bash
PS3="Chọn món: "                          # lời nhắc của select
select item in "Phở" "Bún chả" "Thoát"; do
    case "$item" in
        "Thoát") break ;;
        "")      echo "Lựa chọn không hợp lệ" ;;   # gõ số ngoài danh sách → item rỗng
        *)       echo "Bạn chọn: $item (số $REPLY)" ;;
    esac
done
```

```text
1) Phở
2) Bún chả
3) Thoát
Chọn món: 2
Bạn chọn: Bún chả (số 2)
```

- `select` tự đánh số và lặp lại lời nhắc cho đến khi gặp `break`
- Số người dùng gõ nằm trong `$REPLY`, giá trị tương ứng nằm trong biến (`item`)

Xem thêm: [[Flow_control]] (`case`, `while`) · [[Array]] (`read -a`) · [[Good_script]] (đọc file từng dòng bằng `while read`)
