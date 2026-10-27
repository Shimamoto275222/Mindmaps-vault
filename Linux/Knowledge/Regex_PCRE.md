BRE / ERE cơ bản: xem [[Regex]] · Option của grep: xem [[grep]]

## 1. Tổng quan

**PCRE** (Perl Compatible Regular Expression): kiểu regex của Perl, Python, JavaScript, PHP... Trong Linux dùng qua `grep -P` hoặc `perl -ne` / `perl -pe`.

⭐ Cú pháp PCRE gần giống ERE (không cần escape `( ) { } ? +`), thêm shorthand và nhiều tính năng mà POSIX không có.

```bash
# grep -P cần locale UTF-8, nếu không sẽ báo lỗi:
# "grep: -P supports only unibyte and UTF-8 locales"
export LC_ALL=C.UTF-8
```

## 2. Mapping BRE / ERE ↔ PCRE

### Phần giống nhau

| Chức năng | BRE | ERE | PCRE |
|---|---|---|---|
| Đầu / cuối dòng | `^` `$` | `^` `$` | `^` `$` |
| Ký tự bất kỳ | `.` | `.` | `.` (không match newline) |
| 0+ lần | `*` | `*` | `*` |
| 1+ lần | `\+` (GNU) | `+` | `+` |
| 0 hoặc 1 lần | `\?` (GNU) | `?` | `?` |
| Lặp n..m lần | `\{n,m\}` | `{n,m}` | `{n,m}` |
| Group | `\(abc\)` | `(abc)` | `(abc)` |
| Back-reference | `\1` | `\1` (GNU) | `\1` |

Alternation: BRE `a\|b` (GNU), ERE và PCRE đều là `a|b`.

### Character class

| Ý nghĩa               | POSIX (BRE/ERE)        | PCRE      |
| --------------------- | ---------------------- | --------- |
| Chữ số                | `[[:digit:]]`          | `\d`      |
| Không phải số         | `[^[:digit:]]`         | `\D`      |
| Ký tự "word"          | `[[:alnum:]_]`         | `\w`      |
| Không phải word       | `[^[:alnum:]_]`        | `\W`      |
| Whitespace            | `[[:space:]]`          | `\s`      |
| Không phải whitespace | `[^[:space:]]`         | `\S`      |
| Ranh giới từ          | `\<` `\>` (GNU)        | `\b`      |
| Tab / newline         | không có (gõ tab thật) | `\t` `\n` |

PCRE vẫn hiểu POSIX class bên trong `[ ]`, vd `[[:upper:]]`. GNU grep cũng hỗ trợ `\w \s \b` ở BRE/ERE, nhưng không hỗ trợ `\d`.

```bash
# Cùng một pattern ở 3 kiểu
grep    '^[[:digit:]]\{3\}-[[:digit:]]\{4\}$' file   # BRE
grep -E '^[[:digit:]]{3}-[[:digit:]]{4}$'     file   # ERE
grep -P '^\d{3}-\d{4}$'                       file   # PCRE
```

### Chỉ PCRE mới có

| Cú pháp                 | Ý nghĩa                                      | Chi tiết |
| ----------------------- | -------------------------------------------- | -------- |
| `*?` `+?` `??` `{n,m}?` | Lazy (non-greedy): match ngắn nhất có thể    | mục 3    |
| `(?:abc)`               | Group không capture                          | mục 4    |
| `(?<name>abc)`          | Named group                                  | mục 5    |
| `(?=abc)` / `(?!abc)`   | Lookahead: phía sau là / không là `abc`      | mục 6    |
| `(?<=abc)` / `(?<!abc)` | Lookbehind: phía trước là / không là `abc`   | mục 6    |
| `(?i)`                  | Bật không phân biệt hoa thường trong pattern | mục 7    |
| `\K`                    | Bỏ phần đã match trước đó khỏi kết quả       | mục 7    |

## 3. Greedy và Lazy `*?` `+?` `??` `{n,m}?`

**Greedy** (mặc định, BRE/ERE/PCRE đều vậy): quantifier ăn **nhiều nhất có thể**, rồi nhả dần (backtrack) cho tới khi phần còn lại của pattern match được.

**Lazy** (chỉ PCRE, thêm `?` sau quantifier): ăn **ít nhất có thể**, rồi lấy thêm từng ký tự cho tới khi phần còn lại match được.

| Greedy  | Lazy     | Lazy nghĩa là                          |
| ------- | -------- | -------------------------------------- |
| `*`     | `*?`     | 0+ lần, thử 0 trước                    |
| `+`     | `+?`     | 1+ lần, thử 1 trước                    |
| `?`     | `??`     | 0 hoặc 1 lần, thử 0 trước              |
| `{n,m}` | `{n,m}?` | n..m lần, thử n trước                  |

Cách engine chạy với `<b>.*?</b>` trên `<b>a</b><b>c</b>`:

1. Match `<b>`
2. `.*?` lấy 0 ký tự → thử `</b>` tại `a` → fail
3. `.*?` lấy thêm 1 ký tự (`a`) → thử `</b>` → match → kết quả `<b>a</b>`

Với `.*` (greedy): `.*` ăn hết tới cuối dòng, rồi nhả dần từ phải sang tới khi gặp `</b>` cuối cùng → kết quả cả chuỗi `<b>a</b><b>c</b>`.

### Từng quantifier

```bash
echo '<b>a</b><b>c</b>' | grep -oP '<b>.*</b>'    # <b>a</b><b>c</b>
echo '<b>a</b><b>c</b>' | grep -oP '<b>.*?</b>'   # <b>a</b>  và  <b>c</b>

echo 'xaaay'  | grep -oP 'xa+'       # xaaa
echo 'xaaay'  | grep -oP 'xa+?'      # xa

echo 'colour' | grep -oP 'colou?'    # colou
echo 'colour' | grep -oP 'colou??'   # colo

echo '123456' | grep -oP '\d{2,4}'   # 1234, 56
echo '123456' | grep -oP '\d{2,4}?'  # 12, 34, 56
```

### Ví dụ thực tế

```bash
# Lấy giá trị trong dấu ngoặc kép
echo 'name="Alice" role="admin"' | grep -oP 'name=".*"'    # name="Alice" role="admin"  ← ăn quá tay
echo 'name="Alice" role="admin"' | grep -oP 'name=".*?"'   # name="Alice"

# Path: greedy lấy tới dấu / cuối cùng, lazy dừng ở dấu / đầu tiên tìm được
echo '/home/user/docs/file.txt' | grep -oP '^.*/'     # /home/user/docs/   (giống dirname)
echo '/home/user/docs/file.txt' | grep -oP '^/.*?/'   # /home/

# Lấy domain từ URL
echo 'https://example.com/a/b' | grep -oP 'https?://.+/'    # https://example.com/a/
echo 'https://example.com/a/b' | grep -oP 'https?://.+?/'   # https://example.com/

# Xoá HTML tag - sed không có lazy nên dùng perl
echo '<p>Hi <b>you</b></p>' | perl -pe 's/<.*>//g'      # (rỗng) ← xoá cả dòng
echo '<p>Hi <b>you</b></p>' | perl -pe 's/<.*?>//g'     # Hi you
echo '<p>Hi <b>you</b></p>' | sed 's/<[^>]*>//g'        # Hi you  ← cách POSIX
```

### Lazy vẫn phải nhường cho phần còn lại của pattern

```bash
# In ra group1|group2
echo 12345 | perl -ne 'print "$1|$2\n" if /(\d+)(\d)/'     # 1234|5  greedy lấy nhiều nhất
echo 12345 | perl -ne 'print "$1|$2\n" if /(\d+?)(\d)/'    # 1|2     lazy lấy ít nhất
echo 12345 | perl -ne 'print "$1|$2\n" if /(\d+?)(\d)$/'   # 1234|5  có $ → lazy buộc phải lấy thêm
```

⭐ Lưu ý:
- Lazy chỉ khác greedy khi **phía sau còn pattern** để dừng lại. `a+?` đứng cuối pattern luôn chỉ match 1 ký tự `a`; `a*?` đứng cuối match chuỗi rỗng.
- Lazy không đổi **vị trí bắt đầu**: engine vẫn lấy match bắt đầu sớm nhất (leftmost), lazy chỉ ảnh hưởng độ dài.
- BRE/ERE không có lazy. Cách thay thế là dùng negated class: `"[^"]*"` cho kết quả giống `".*?"`, và thường nhanh hơn vì không phải backtrack.

## 4. Group không capture `(?:abc)`

`(abc)` làm 2 việc: **gom nhóm** (để áp quantifier / alternation) và **capture** (lưu lại thành `\1`, `$1`...).
`(?:abc)` chỉ **gom nhóm**, không capture → không chiếm số thứ tự group.

Dùng khi cần ngoặc chỉ để gom nhóm, không cần lấy lại giá trị.

```bash
# Gom nhóm để lặp
echo 'ababab x' | grep -oP '(?:ab)+'     # ababab

# Gom nhóm cho alternation
grep -P '^(?:GET|POST) /api' access.log
```

Khác biệt thấy rõ khi dùng back-reference / replace, vì số thứ tự group thay đổi:

```bash
# (Mr|Ms) là group 1 → tên là group 2
echo 'Mr. Smith, Ms. Jane' | perl -pe 's/(Mr|Ms)\. (\w+)/$2/g'    # Smith, Jane

# (?:Mr|Ms) không capture → tên thành group 1
echo 'Mr. Smith, Ms. Jane' | perl -pe 's/(?:Mr|Ms)\. (\w+)/$1/g'  # Smith, Jane

# Với back-reference \1
echo 'the cat cat' | grep -oP '(?:the) (\w+) \1'    # the cat cat  (\1 = cat)
echo 'the cat cat' | grep -oP '(the) (\w+) \1'      # không match  (\1 = the)
```

⭐ Trong pattern dài nhiều ngoặc, dùng `(?:)` cho các ngoặc chỉ để gom nhóm → số `\1 \2` dễ đếm hơn, và engine chạy nhanh hơn một chút.

## 5. Named group `(?<name>abc)`

Đặt tên cho group thay vì đếm số. Back-reference bằng `\k<name>`, trong perl lấy giá trị bằng `$+{name}`.

```bash
# Tìm từ bị lặp liền nhau
echo 'this is is a test test' | grep -oP '\b(?<w>\w+) \k<w>\b'   # is is, test test

# Lấy năm/tháng
echo '2026-10-28' | perl -ne 'print "$+{y}/$+{m}\n" if /(?<y>\d{4})-(?<m>\d{2})/'   # 2026/10
```

## 6. Lookahead / Lookbehind

Kiểm tra phía trước/sau có (hoặc không có) pattern, nhưng **không đưa phần đó vào kết quả** (zero-width).

| Cú pháp    | Tên                 | Match khi                    |
| ---------- | ------------------- | ---------------------------- |
| `X(?=Y)`   | positive lookahead  | X đứng **trước** Y           |
| `X(?!Y)`   | negative lookahead  | X **không** đứng trước Y     |
| `(?<=Y)X`  | positive lookbehind | X đứng **sau** Y             |
| `(?<!Y)X`  | negative lookbehind | X **không** đứng sau Y       |

```bash
# Lookahead
echo 'price 100 USD, 200 EUR' | grep -oP '\d+(?= USD)'     # 100
echo 'price 100 USD, 200 EUR' | grep -oP '\d+(?! USD)\b'   # 200

# Lookbehind
echo 'cost $30 and 40' | grep -oP '(?<=\$)\d+'       # 30
echo 'cost $30 and 40' | grep -oP '(?<!\$)\b\d+'     # 40

# Nhiều lookahead ở đầu = điều kiện AND: password ≥ 8 ký tự, có số, có chữ hoa
grep -P '^(?=.*\d)(?=.*[A-Z]).{8,}$' passwords.txt
```

Lookbehind trong PCRE phải có độ dài cố định: `(?<=ab|cd)` được, `(?<=a+)` lỗi.

## 7. `(?i)` và `\K`

```bash
# (?i): không phân biệt hoa thường, giống grep -i nhưng đặt trong pattern
printf 'Error\nERROR x\nerror\n' | grep -oP '(?i)error'   # Error, ERROR, error

# \K: match cả pattern nhưng chỉ giữ phần sau \K
echo 'version: 1.2.3' | grep -oP 'version: \K[\d.]+'   # 1.2.3
grep -oP 'port=\K\d+' config                           # giống (?<=port=)\d+
```

⭐ `\K` khác lookbehind: phần trước `\K` được phép dài thay đổi (`\w+=\K\d+` hợp lệ, `(?<=\w+=)\d+` thì lỗi).
