Copy file / thư mục (lệnh `cp`).

```bash
# cp [options] source dest
# cp [options] source... dir    (nhiều nguồn → đích phải là thư mục)
# -u: chỉ copy khi file nguồn mới hơn file đích, hoặc file đích chưa tồn tại
# -r: copy thư mục đệ quy
# -v: verbose, giải thích đang làm gì
cp file.txt backup.txt
cp -r src/ /tmp/src_backup
cp -uv *.md /backup/
```
