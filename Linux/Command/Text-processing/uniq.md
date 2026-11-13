Lọc các dòng trùng **liền nhau** trong file text (hoặc stdin), thường dùng ngay sau [[sort]].

```bash
# uniq [options] [input [output]]
# không có input → đọc từ stdin
sort file.txt | uniq
```

## 1. Các option chính

Input `fruits.txt`:

```text
apple
banana
apple
cherry
banana
apple
```

```bash
# -c: thêm số lần xuất hiện vào đầu mỗi dòng (count)
# -d: chỉ in các dòng bị trùng, mỗi dòng 1 lần
# -u: chỉ in các dòng KHÔNG trùng (xuất hiện đúng 1 lần)
# -i: so sánh không phân biệt hoa thường
sort fruits.txt | uniq       # → apple, banana, cherry
sort fruits.txt | uniq -c    # → 3 apple, 2 banana, 1 cherry (số đứng đầu dòng)
sort fruits.txt | uniq -d    # → apple, banana
sort fruits.txt | uniq -u    # → cherry
```

## 2. ⭐ Không phân biệt hoa thường (`-i`)

Input `names.txt` (các dòng đã liền nhau):

```text
Alice
alice
ALICE
bob
```

```bash
uniq names.txt       # → Alice, alice, ALICE, bob (khác hoa thường = khác dòng)
uniq -i names.txt    # → Alice, bob (giữ dòng đầu tiên của mỗi nhóm)
uniq -ic names.txt   # → 3 Alice, 1 bob

# file chưa sort: sort -f (không phân biệt hoa thường) để các dòng cùng chữ đứng liền nhau
sort -f names.txt | uniq -i
```

## 3. Kết hợp với lệnh khác

```bash
# top 10 dòng xuất hiện nhiều nhất (kèm số lần)
sort access.log | uniq -c | sort -nr | head -n 10

# đếm số IP khác nhau trong access log
cut -d ' ' -f1 access.log | sort | uniq | wc -l
```

⚠️ `uniq` chỉ so các dòng **liền nhau** → không `sort` trước thì dòng trùng nằm cách xa vẫn bị giữ lại: `uniq fruits.txt` vẫn in đủ 6 dòng.
