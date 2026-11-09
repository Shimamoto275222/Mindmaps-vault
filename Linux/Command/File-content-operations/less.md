
```bash
# less [file]
# view file content page by page (better than `more`: scroll back, search, fast on big files)
less /etc/passwd
ls -l /usr/bin | less

# show line numbers
-N

# case-insensitive search
-i

# don't wrap long lines (scroll left/right with arrows)
-S

# open and jump to first match (also works with `more`)
less +/ERROR large_log.txt
```

## Navigation
> Keys below are pressed **inside** less, not typed as command arguments.

```bash
# --- Scroll ---
Space / f / PgDn    # next page
b / PgUp            # previous page
d                   # half page down
u                   # half page up
j / ↓ / Enter       # next line
k / ↑               # previous line

# --- Jump ---
g / Home            # start of file
G / End             # end of file
50g                 # go to line 50
50p                 # go to 50% of file

# --- Search ---
/pattern            # search forward
?pattern            # search backward
n                   # next match
N                   # previous match
&pattern            # show only lines matching pattern

# --- Other ---
F                   # follow mode, like `tail -f` (Ctrl+C to stop)
v                   # open file in $EDITOR
h                   # help
q                   # quit
```
