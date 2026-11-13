Tìm vị trí binary, source, manual page.

```bash
# whereis [options] name
# -b: tìm file binary
# -m: tìm file manual
whereis -bm python3
```

Output:

```text
python3: /usr/bin/python3 /usr/lib/python3 /etc/python3 /usr/share/python3 /usr/share/man/man1/python3.1.gz
```

- `/usr/bin/python3`: vị trí binary của Python 3 (chương trình thực thi)
- `/usr/lib/python3`: thư mục chứa thư viện Python 3 (code dùng lại cho các chương trình Python)
- `/etc/python3`: thư mục chứa file cấu hình của Python 3
- `/usr/share/python3`: thư mục chứa dữ liệu dùng chung của Python 3
- `/usr/share/man/man1/python3.1.gz`: vị trí manual page của Python 3
