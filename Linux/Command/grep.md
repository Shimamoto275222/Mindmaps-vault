Cú pháp regex: xem [[Regex]]

```bash
# grep [options] pattern [file...]
# không có file → đọc từ stdin
grep root /etc/passwd
ps aux | grep ssh
```

## 1. Chọn kiểu pattern

```bash
# -G: BRE (mặc định)
# -E: ERE (giống egrep)
# -F: fixed string, không hiểu regex (giống fgrep) - nhanh, an toàn khi search chuỗi có . * [
# -P: PCRE (\d, lazy, lookahead...)
grep -E 'error|warn' app.log
grep -F '1.2.3.4' access.log
grep -P '\d{3}-\d{4}' phones.txt
```

## 2. Điều khiển việc match

```bash
# -i: không phân biệt hoa thường
# -v: đảo ngược - in dòng KHÔNG match
# -w: match nguyên từ (cat không match concat)
# -x: match nguyên dòng
# -e: chỉ định pattern, dùng nhiều lần = OR, hoặc khi pattern bắt đầu bằng -
# -f: đọc danh sách pattern từ file (mỗi dòng 1 pattern)
grep -i 'error' app.log
grep -v '^#' config            # bỏ dòng comment
grep -v -e '^#' -e '^$' config # bỏ comment và dòng trống
grep -w 'cat' file
grep -e '-v' file
grep -f patterns.txt file
```

## 3. Điều khiển output

```bash
# -o: chỉ in phần match, không in cả dòng
# -n: in số dòng
# -c: đếm số dòng match
# -l: chỉ in tên file có match
# -L: chỉ in tên file KHÔNG có match
# -H / -h: luôn in / không in tên file trước mỗi dòng
# -m N: dừng sau N dòng match
# --color=auto: tô màu phần match
grep -n 'TODO' *.py
grep -c 'GET' access.log
grep -l 'password' *.conf
grep -oE '[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+' access.log   # lấy ra các IP
```

## 4. Context xung quanh dòng match

```bash
# -A N: thêm N dòng sau (After)
# -B N: thêm N dòng trước (Before)
# -C N: thêm N dòng trước và sau (Context)
grep -A 3 'Exception' app.log
grep -C 2 'FATAL' app.log
```

## 5. Search đệ quy trong thư mục

```bash
# -r: đệ quy (không follow symlink)
# -R: đệ quy, follow symlink
# --include / --exclude: lọc file theo glob
# --exclude-dir: bỏ qua thư mục
grep -rn 'main' src/
grep -rn --include='*.md' 'regex' .
grep -r --exclude-dir={.git,node_modules} 'TODO' .
```

## 6. Dùng trong script

```bash
# -q: không in gì, chỉ trả exit status
# -s: ẩn lỗi file không tồn tại / không đọc được
# exit status: 0 = có match, 1 = không match, 2 = lỗi
if grep -q '^admin:' /etc/passwd; then
    echo "user admin tồn tại"
fi
```

⭐ Combo hay dùng:

```bash
grep -rniw 'pattern' .          # đệ quy + số dòng + không phân biệt hoa thường + nguyên từ
grep -oP 'port=\K\d+' config    # lấy giá trị sau port=
grep -vE '^\s*(#|$)' config     # xem config bỏ comment và dòng trống
```
