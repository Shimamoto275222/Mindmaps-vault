
## 1. Mở / Lưu / Thoát

- `vi file.txt` → mở file (chưa có thì tạo mới)
- ⭐ `:w` → lưu (chữ **thường** — `:W` sẽ báo lỗi)
- `:w ten-moi.txt` → lưu thành file khác (vẫn đang sửa file cũ)
- ⭐ `:q` → thoát (báo lỗi nếu chưa lưu)
- ⭐ `:q!` → thoát, **bỏ** mọi thay đổi
- ⭐ `:wq` → lưu rồi thoát
- ⭐ `ZZ` → lưu rồi thoát (không cần `:`)

## 2. Vào Insert mode

- ⭐ `i` → gõ **trước** con trỏ
- `a` → gõ **sau** con trỏ
- ⭐ `A` → gõ ở **cuối dòng**
- `o` → mở dòng mới **bên dưới**
- `O` → mở dòng mới **bên trên**

Gõ xong → `Esc`.

## 3. Di chuyển con trỏ

- `h` `j` `k` `l` → trái · xuống · lên · phải (hoặc phím mũi tên)
- ⭐ `w` / `W` → đầu từ kế tiếp (`W` bỏ qua dấu câu)
- ⭐ `b` / `B` → đầu từ phía trước (`B` bỏ qua dấu câu)
- `0` → đầu dòng
- `^` → ký tự khác khoảng trắng đầu tiên của dòng
- `$` → cuối dòng
- `Ctrl-f` / `Ctrl-b` → xuống / lên 1 trang
- ⭐ `số` + `G` → đến dòng số đó (vd `20G`; `1G` = dòng đầu)
- ⭐ `G` → dòng cuối file

## 4. Xóa (= cắt)

- ⭐ `x` → 1 ký tự tại con trỏ (`3x` = 3 ký tự)
- ⭐ `dd` → dòng hiện tại (`5dd` = 5 dòng)
- `dW` → từ con trỏ đến đầu từ kế tiếp
- `d$` → từ con trỏ đến cuối dòng
- `d0` → từ con trỏ về đầu dòng
- `d^` → từ con trỏ về ký tự không trắng đầu dòng
- `dG` → từ dòng hiện tại đến cuối file
- `d20G` → từ dòng hiện tại đến dòng 20

> Công thức: **`d` + lệnh di chuyển** → xóa đúng đoạn mà lệnh di chuyển đi qua.

## 5. Copy / Paste / Undo

- `yy` → copy dòng hiện tại (`5yy` = 5 dòng)
- `yW`, `y$`, `y0`, `y^`, `yG`, `y20G` → copy theo cùng quy tắc như `d`
- `p` → dán **sau** con trỏ / **dưới** dòng hiện tại
- `P` → dán **trước** con trỏ / **trên** dòng hiện tại
- `J` → nối dòng dưới vào dòng hiện tại
- ⭐ `u` → undo

> Cái gì bị `d` xóa cũng nằm trong bộ nhớ → `dd` + `p` = **di chuyển** dòng.

## 6. Tìm kiếm & Thay thế

- `fa` → nhảy tới ký tự `a` kế tiếp **trong dòng**; `;` lặp lại
- `/chuoi` → tìm `chuoi` trong file; `n` = kết quả kế tiếp
- `:%s/cu/moi/g` → thay **mọi** `cu` → `moi` trong cả file
- `:%s/cu/moi/gc` → như trên nhưng **hỏi xác nhận** từng chỗ

Giải nghĩa `:%s/cu/moi/g`:

- `%` = phạm vi toàn file (= `1,$`; hoặc `1,5` = dòng 1→5)
- `s` = substitute
- `g` = thay mọi chỗ trên mỗi dòng (thiếu `g` → chỉ chỗ đầu tiên mỗi dòng)

Khi có `c`, trả lời: `y` thay · `n` bỏ qua · `a` thay tất cả · `q`/`Esc` dừng · `l` thay chỗ này rồi dừng.

## 7. Làm việc với nhiều file

- `vi a.txt b.txt` → mở nhiều file cùng lúc
- `:bn` / `:bp` → sang file kế tiếp / trước đó
- `:buffers` → liệt kê các file đang mở
- `:buffer 2` → chuyển đến file số 2
- `:e c.txt` → mở thêm file khác
- `:r c.txt` → chèn toàn bộ nội dung `c.txt` vào dưới con trỏ

> Copy giữa 2 file: `yy` ở file A → `:bn` → `p` ở file B.
> Phải `:w` trước khi chuyển file, hoặc dùng `:bn!` để bỏ qua cảnh báo.

## 8. Gợi ý luyện tập

- Chạy `vimtutor` trong terminal — bài thực hành ~30 phút, đi đúng các lệnh trên.
