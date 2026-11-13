---
paths:
  - "Linux/Command/**/*.md"
---

# Ghi chú lệnh Linux (`Linux/Command/`)

Mẫu tham khảo: `Linux/Command/Text-processing/cut.md`, `grep.md`, `wc.md`.

## Cấu trúc file

1. Dòng đầu: 1 câu tiếng Việt mô tả lệnh làm gì.
2. Khối `bash` cú pháp: `# cmd [options] [file...]`, thêm `# không có file → đọc từ stdin` nếu lệnh đọc stdin, kèm 1 ví dụ chạy.
3. Các mục `## N. <nhóm>` đánh số từ 1, mỗi mục 1 khối `bash`: comment option trước (`# -x: mô tả`, có tham số thì `# -f N: mô tả`), ví dụ chạy sau.
4. Có pipe với lệnh khác (`sort`, `uniq`, `grep`…) → gom vào mục "Kết hợp với lệnh khác" ở gần cuối.
5. Bẫy hay gặp → dòng `⚠️ …` ở cuối file hoặc cuối mục liên quan.

## Quy ước

- Chỉ ghi option hay dùng, bỏ option hiếm gặp.
- Mô tả bằng tiếng Việt; tên lệnh, option, thuật ngữ (stdin, delimiter, field, pattern…) giữ tiếng Anh.
- Output minh hoạ: ngắn → `# → ...` cuối dòng lệnh; dài / nhiều dòng → khối ` ```text ` riêng.
- Ví dụ đáng nhớ → đánh ⭐ ở tiêu đề mục (vd `## 2. ⭐ Phân tích access.log với -d '"'`).
- Liên kết sang ghi chú khác bằng `[[Tên]]` (vd `Cú pháp regex: xem [[Regex]]`).
- Được bảo "format lại" → chỉ sửa định dạng, KHÔNG thêm nội dung.
