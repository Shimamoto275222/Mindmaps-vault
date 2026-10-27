
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

## 7. PCRE

PCRE (`grep -P`, Perl, Python, JS...): mapping với BRE/ERE, greedy/lazy, `(?:)`, named group, lookahead/lookbehind, `\K`... xem [[Regex_PCRE]]
