
```bash 
foo=hello          # shell variable, not exported
printenv foo       # (nothing)
set | grep ^foo    # foo=hello

export foo         # now it's in the environment
printenv foo       # hello
```

