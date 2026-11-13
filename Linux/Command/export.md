Đưa shell variable vào environment để các process con (lệnh, script chạy từ shell này) nhìn thấy.

```bash
# export NAME[=value]
foo=hello          # shell variable, chưa được export
printenv foo       # → (không in gì)
set | grep ^foo    # → foo=hello

export foo         # giờ foo đã nằm trong environment
printenv foo       # → hello
```
