	Locate binary, source, manual page.

```bash
# whereis [options] name
# -b: locate binary file
# -m: locate manual file
whereis -bm python3
```

Output:

```text
python3: /usr/bin/python3 /usr/lib/python3 /etc/python3 /usr/share/python3 /usr/share/man/man1/python3.1.gz
```

- `/usr/bin/python3`: The location of the Python 3 binary (the executable program)
- `/usr/lib/python3`: The directory containing Python 3 libraries (reusable code used by Python programs)
- `/etc/python3`: A directory containing Python 3 configuration files
- `/usr/share/python3`: A directory containing shared Python 3 data
- `/usr/share/man/man1/python3.1.gz`: The location of the Python 3 manual page
