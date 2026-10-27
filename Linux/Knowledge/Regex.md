## 1. Tổng quan

Regular expression (regex) = pattern mô tả một tập chuỗi text. POSIX chia làm 2 loại:

- **BRE** (Basic Regular Expression): mặc định của `grep`, `sed`, `vim`
- **ERE** (Extended Regular Expression): `grep -E` (`egrep`), `sed -E`, `awk`

⭐ Khác biệt chính: ERE thêm metacharacter `( ) { } ? + |`. Trong BRE các ký tự này là ký tự thường, muốn dùng chức năng thì phải escape bằng `\`.

## 2. Từ BRE đến ERE

| Chức năng       | BRE        | ERE        |
| --------------- | ---------- | ---------- |
| Đầu / cuối dòng | `^` `$`    | `^` `$`    |
| Ký tự bất kỳ    | `.`        | `.`        |
| 0+ lần          | `*`        | `*`        |
| 1+ lần          | `\+` (GNU) | `+`        |
| 0 hoặc 1 lần    | `\?` (GNU) | `?`        |
| Lặp n..m lần    | `\{n,m\}`  | `{n,m}`    |
| Group           | `\(abc\)`  | `(abc)`    |
| Back-reference  | `\1`       | `\1` (GNU) |

Alternation (hoặc): BRE viết `a\|b` (GNU), ERE viết `a|b`.

## 3. Metacharacter dùng chung

```bash
grep '^root' /etc/passwd     # dòng bắt đầu bằng root
grep 'bash$' /etc/passwd     # dòng kết thúc bằng bash
grep '^$' file               # dòng trống
grep 'h.t' file              # hat, hot, h1t...
grep 'ab*c' file             # ac, abc, abbc...
grep '\.txt' file            # dấu . thật (escape)
```

## 4. Bracket expression `[ ]`

```bash
grep '[bg]zip' file          # bzip hoặc gzip
grep '[^bg]zip' file         # ^ đứng đầu trong [ ] = phủ định
grep '^[A-Z]' file           # bắt đầu bằng chữ hoa
grep '^[-AZ]' file           # - đặt đầu = ký tự - thường
```

⭐ Nên dùng POSIX character class thay cho range (range `[A-Z]` phụ thuộc locale):

| Class | Ý nghĩa |
|---|---|
| `[:alnum:]` | chữ + số |
| `[:alpha:]` | chữ |
| `[:digit:]` | số `0-9` |
| `[:upper:]` / `[:lower:]` | chữ hoa / thường |
| `[:space:]` | whitespace (space, tab, newline...) |
| `[:punct:]` | dấu câu |
| `[:xdigit:]` | hex `0-9A-Fa-f` |

```bash
grep '^[[:upper:]]' file     # chú ý: 2 lớp ngoặc [[ ]]
```

## 5. Metacharacter của ERE

```bash
grep -E 'AAA|BBB' file              # AAA hoặc BBB
grep -E '^(bz|gz|zip)' file         # group + alternation
grep -E '^\(?[0-9]{3}\)? [0-9]{3}-[0-9]{4}$' phones.txt
                                    # (555) 123-4567 hoặc 555 123-4567
grep -E '^([[:alpha:]]+ ?)+$' file  # một hoặc nhiều từ cách nhau bởi space
```

So sánh cùng một pattern:

```bash
grep    '^[0-9]\{3\}-[0-9]\{4\}$' file   # BRE
grep -E '^[0-9]{3}-[0-9]{4}$'     file   # ERE - gọn hơn
```

## 6. Lệnh hay dùng với regex

`grep` và các option: xem [[grep]]

```bash
grep -E 'a|b' file            # chi tiết ở note grep
sed -E 's/(\w+) (\w+)/\2 \1/' # đổi chỗ 2 từ bằng back-reference
find . -regex '.*\.md'        # regex match toàn bộ path
locate --regex 'bin/(bz|gz|zip)'
less                          # gõ /pattern để search bằng regex
```

## 7. Mapping BRE / ERE ↔ PCRE

**PCRE** (Perl Compatible Regular Expression): kiểu regex của Perl, Python, JavaScript, PHP... Trong Linux dùng qua `grep -P`.

⭐ Cú pháp PCRE gần giống ERE (không cần escape `( ) { } ? +`), thêm shorthand và nhiều tính năng mà POSIX không có.

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

### Chỉ PCRE mới có

| Cú pháp                 | Ý nghĩa                                      |
| ----------------------- | -------------------------------------------- |
| `*?` `+?` `??` `{n,m}?` | Lazy (non-greedy): match ngắn nhất có thể    |
| `(?:abc)`               | Group không capture                          |
| `(?<name>abc)`          | Named group                                  |
| `(?=abc)` / `(?!abc)`   | Lookahead: phía sau là / không là `abc`      |
| `(?<=abc)` / `(?<!abc)` | Lookbehind: phía trước là / không là `abc`   |
| `(?i)`                  | Bật không phân biệt hoa thường trong pattern |
| `\K`                    | Bỏ phần đã match trước đó khỏi kết quả       |

```bash
# Cùng một pattern ở 3 kiểu
grep    '^[[:digit:]]\{3\}-[[:digit:]]\{4\}$' file   # BRE
grep -E '^[[:digit:]]{3}-[[:digit:]]{4}$'     file   # ERE
grep -P '^\d{3}-\d{4}$'                       file   # PCRE

# Lookbehind / \K: lấy giá trị sau "port="
grep -oP '(?<=port=)\d+' config
grep -oP 'port=\K\d+' config
```

### Lazy quantifier `*?` `+?` `??` `{n,m}?`

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

```bash
# (cần locale UTF-8 cho grep -P)
echo '<b>a</b><b>c</b>' | grep -oP '<b>.*</b>'    # <b>a</b><b>c</b>
echo '<b>a</b><b>c</b>' | grep -oP '<b>.*?</b>'   # <b>a</b>  và  <b>c</b>

echo 'xaaay'  | grep -oP 'xa+'       # xaaa
echo 'xaaay'  | grep -oP 'xa+?'      # xa

echo 'colour' | grep -oP 'colou?'    # colou
echo 'colour' | grep -oP 'colou??'   # colo

echo '123456' | grep -oP '\d{2,4}'   # 1234, 56
echo '123456' | grep -oP '\d{2,4}?'  # 12, 34, 56

echo '"a" and "b"' | grep -oP '".*?"'   # "a", "b"
```

⭐ Lưu ý:
- Lazy chỉ khác greedy khi **phía sau còn pattern** để dừng lại. `a+?` đứng cuối pattern luôn chỉ match 1 ký tự `a`; `a*?` đứng cuối match chuỗi rỗng.
- Lazy không đổi **vị trí bắt đầu**: engine vẫn lấy match bắt đầu sớm nhất (leftmost), lazy chỉ ảnh hưởng độ dài.
- BRE/ERE không có lazy. Cách thay thế là dùng negated class: `"[^"]*"` cho kết quả giống `".*?"`, và thường nhanh hơn vì không phải backtrack.
