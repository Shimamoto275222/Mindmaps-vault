## 1. Đầu file

```bash
#!/usr/bin/env bash
#
# backup.sh — Nén một thư mục thành file .tar.gz
# Cách dùng: backup.sh [-v] [-o thư_mục_đích] <thư_mục_nguồn>

set -euo pipefail
```

- Shebang `#!/usr/bin/env bash` (tìm bash theo `PATH`) hoặc `#!/bin/bash`; muốn chạy bằng `sh` thì chỉ được dùng cú pháp POSIX
- Comment mô tả script làm gì + cách dùng

## 2. ⭐ Strict mode: `set -euo pipefail`

| Option | Tác dụng |
| --- | --- |
| `-e` | một lệnh lỗi → dừng script ngay |
| `-u` | dùng biến chưa gán → báo lỗi và dừng (bắt lỗi gõ sai tên biến) |
| `-o pipefail` | pipe bị coi là lỗi nếu **bất kỳ** lệnh nào trong pipe lỗi (mặc định chỉ xét lệnh cuối) |

Lưu ý khi bật:

- Lệnh được phép lỗi → `cmd || true`
- Tham số không bắt buộc → `${1:-}` (không thì `-u` báo lỗi)
- `((count++))` khi `count=0` trả về exit status 1 → `-e` dừng script → dùng `count=$((count + 1))`

## 3. Quote & cú pháp hiện đại

- ⭐ Luôn quote: `"$var"`, `"$@"`, `"${arr[@]}"`
- `$(cmd)` thay cho `` `cmd` ``
- `[[ ]]` cho chuỗi / file, `(( ))` cho số
- In dữ liệu bất kỳ → `printf '%s\n' "$x"` (hành vi của `echo` với `-n`, `-e`, `\` khác nhau giữa các hệ thống)

## 4. Biến

- `UPPER_CASE` cho hằng số & biến môi trường, `lower_case` cho biến nội bộ → không vô tình ghi đè `PATH`, `HOME`, `USER`…
- `readonly` cho hằng số, `local` cho biến trong function
- Gom cấu hình (đường dẫn, số ngày giữ backup…) lên đầu file

## 5. Chia thành function + `main`

```bash
main() {
    parse_args "$@"
    check_deps
    do_backup
}

main "$@"   # dòng cuối cùng
```

- Dễ đọc, dễ sửa từng phần
- Bash đọc hết các function rồi mới chạy `main` → không chạy nửa vời nếu file bị cắt cụt hay đang sửa dở

## 6. Báo lỗi đúng cách

```bash
log() { printf '[%s] %s\n' "$(date +%T)" "$*" >&2; }
die() { log "LỖI: $*"; exit 1; }

[[ -d $src ]] || die "Không tìm thấy thư mục: $src"
```

- Thông báo / log → **stderr** (`>&2`); stdout chỉ dành cho kết quả (để còn pipe sang lệnh khác)
- Exit code có ý nghĩa: `0` thành công, `1` lỗi, `2` sai cách dùng
- Có hàm `usage()` và hỗ trợ `-h`

## 7. Kiểm tra sớm, thất bại sớm

```bash
[[ $# -ge 1 ]] || { usage >&2; exit 2; }        # đủ tham số chưa
command -v rsync >/dev/null || die "Cần cài rsync"   # lệnh phụ thuộc có chưa
[[ $EUID -eq 0 ]] || die "Cần chạy bằng sudo"        # đủ quyền chưa
```

## 8. Dọn dẹp: `mktemp` + `trap`

```bash
tmp=$(mktemp)              # file tạm tên ngẫu nhiên, không đè file có sẵn
trap 'rm -f "$tmp"' EXIT   # tự xoá khi script kết thúc, kể cả khi lỗi giữa chừng
```

## 9. Thói quen an toàn

- `cd "$dir" || exit 1` — cd lỗi mà chạy tiếp là làm việc ở sai thư mục
- ⭐ `rm -rf "${dir:?}/"*` — nếu `dir` rỗng thì dừng, thay vì thành `rm -rf /*`
- Duyệt file bằng glob `for f in *.log`, **không** parse output của `ls`
- Đọc file từng dòng: `while IFS= read -r line; do …; done < file`
- Chạy lại nhiều lần không hỏng (idempotent): `mkdir -p`, kiểm tra tồn tại trước khi tạo / xoá

## 10. Kiểm tra & debug

- ⭐ **ShellCheck**: `shellcheck script.sh` → bắt lỗi thiếu quote, biến sai tên, cú pháp nguy hiểm (`sudo apt install shellcheck`, có cả extension VS Code)
- `bash -n script.sh` → chỉ kiểm tra cú pháp, không chạy
- `bash -x script.sh` (hoặc `set -x` … `set +x` quanh đoạn cần soi) → in từng lệnh trước khi chạy
- Thử với dữ liệu "xấu": tên file có dấu cách, thiếu tham số, thư mục rỗng

## 11. Mẫu script

```bash
#!/usr/bin/env bash
#
# backup.sh — Nén một thư mục thành file .tar.gz kèm ngày giờ
# Cách dùng: backup.sh [-v] [-o thư_mục_đích] <thư_mục_nguồn>

set -euo pipefail

readonly SCRIPT_NAME="${0##*/}"

verbose=0
outdir="."
src=""

usage() {
    cat <<EOF
Cách dùng: $SCRIPT_NAME [-v] [-o thư_mục_đích] <thư_mục_nguồn>
  -v   in chi tiết
  -o   nơi lưu file backup (mặc định: thư mục hiện tại)
  -h   hiện hướng dẫn
EOF
}

log() { printf '[%s] %s\n' "$(date +%T)" "$*" >&2; }
die() { log "LỖI: $*"; exit 1; }

parse_args() {
    while [[ $# -gt 0 ]]; do
        case "$1" in
            -v) verbose=1 ;;
            -o) outdir="${2:?Thiếu giá trị cho -o}"; shift ;;
            -h) usage; exit 0 ;;
            -*) usage >&2; exit 2 ;;
            *)  break ;;
        esac
        shift
    done
    [[ $# -eq 1 ]] || { usage >&2; exit 2; }
    src="$1"
}

main() {
    parse_args "$@"
    [[ -d $src ]] || die "Không tìm thấy thư mục: $src"
    command -v tar >/dev/null || die "Cần cài tar"
    mkdir -p "$outdir"

    local name archive
    name=$(basename "$src")
    archive="$outdir/${name}_$(date +%Y%m%d_%H%M%S).tar.gz"

    if (( verbose )); then
        log "Nén $src → $archive"
    fi
    tar -czf "$archive" -C "$(dirname "$src")" "$name"
    log "Xong: $archive"
}

main "$@"
```

Xem thêm: [[Flow_control]] · [[Test_expressions]] · [[Script_arguments]] · [[Function]]
