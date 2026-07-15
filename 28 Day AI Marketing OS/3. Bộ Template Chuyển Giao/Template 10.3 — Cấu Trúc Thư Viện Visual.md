---
up:
  - "[[Danh Mục Template Chuyển Giao]]"
created: 2026-07-15
tags: [project, aios, template]
---

# Template 10.3 — Cấu Trúc Thư Viện Visual

> Dùng cho **[[Ngày 10 — AI Design & Visual Asset]]**. Tạo cây thư mục này **1 lần** trên Google Drive (hoặc trong vault SME `Sản Phẩm & Dịch Vụ/_Media/`) — dùng lại cả năm. Lý do: [[Ngày 13 — Phân Phối Nội Dung & Content Automation]] sẽ lấy visual từ đây để xếp lịch; nhân sự nhận bàn giao sau này mở folder là làm được ngay.
>
> 🔴 **Luật bất di bất dịch:** mỗi visual **luôn lưu 2 bản** — file **Canva gốc** (sửa được) + file **PNG** (đăng được). Chỉ có PNG = tuần sau muốn sửa 1 chữ phải làm lại từ đầu.

## 1. Cây thư mục chuẩn

```
Visual Library/
├── 01 Brand Kit/           ← logo PNG · file T10.1 · ảnh chụp Brand Kit đã cài trong Canva
├── 02 Banner/              ← 2 banner 1080×1080 (PNG) + link Canva gốc
├── 03 Poster-Infographic/  ← 2 file 1080×1350 (PNG) + link Canva gốc
├── 04 Thumbnail/           ← 2 thumbnail 1080×1920 cho đúng 2 video N11
├── 05 Feedback-Case/       ← (Bonus) khung ảnh feedback, ảnh khách nhận hàng
├── 06 Prompt đã dùng/      ← prompts.md — dán nguyên prompt đã chạy (chạy lại tuần sau trong 5')
└── README.md               ← quy tắc đặt tên + luật "luôn lưu Canva gốc + PNG"
```

## 2. Quy tắc đặt tên file

**Công thức:** `[DN]-[loại]-[chủ đề]-[phiên bản]`

| Thành phần | Giá trị hợp lệ | Ví dụ |
|---|---|---|
| `[DN]` | mã ngắn của doanh nghiệp | `MSX` |
| `[loại]` | `banner` · `poster` · `infographic` · `thumbnail` · `feedback` | `banner` |
| `[chủ đề]` | mô tả ngắn không dấu, nối bằng gạch | `combo3tang1` |
| `[phiên bản]` | `v1`, `v2`… (sửa lớn thì tăng số) | `v1` |

**Ví dụ đầy đủ:** `MSX-banner-combo3tang1-v1.png` · `MSX-infographic-sosanh-359k-v1.png` · `MSX-thumbnail-1541met-v1.png`

> 💡 Tên file **không dấu, không khoảng trắng** — tránh lỗi khi upload lên nền tảng lịch đăng / quảng cáo.

## 3. Quy tắc "2 bản" — gốc + PNG

| Bản | Định dạng | Lưu ở đâu | Vai trò |
|---|---|---|---|
| **Gốc** | Link Canva (không tải về được bản gốc → dán link) | trong file `README.md` hoặc ghi chú cạnh PNG | Sửa 1 chữ / đổi màu / nhân bản trong 30 giây |
| **Xuất bản** | **PNG** (đúng kích thước kênh) | đúng folder loại (02/03/04) | File thật để đăng — kéo thẳng vào lịch N13 |

## 4. Đóng vòng truy nguyên (làm sau khi lưu file)

1. Kéo 6 PNG vào đúng folder 02/03/04.
2. Dán 2 (hoặc nhiều) prompt đã dùng vào `06 Prompt đã dùng/prompts.md`.
3. Mở **Content Bank N9 → điền cột "Visual"**: 6 bài ↔ 6 link visual; **4 bài còn lại ghi rõ** *"ảnh thật: [loại ảnh]"*.
4. Mở **[[Template 10.2 — Bảng Kế Hoạch Visual]] → điền cột `Link Canva` + `Link PNG`**, rà lại `Mã nguồn` + `Message Pack` 6/6 dòng. *Vòng tròn khép — mỗi ảnh biết mình sinh ra từ đâu, không có ảnh mồ côi.*

## 5. 🍵 Bản MSX — 3 file demo đã lưu

```
Visual Library/
├── 02 Banner/              ← MSX-banner-combo3tang1-v1.png
├── 03 Poster-Infographic/  ← MSX-infographic-sosanh-359k-v1.png
└── 04 Thumbnail/           ← MSX-thumbnail-1541met-v1.png
```

## 6. Tiêu chí đạt

- Đủ 7 mục cây thư mục (01–06 + README).
- **6 PNG** đặt tên đúng công thức + **6 link Canva gốc** đã lưu.
- `06 Prompt đã dùng` có nội dung (không rỗng).
- Content Bank: 6 bài có link visual + 4 bài ghi rõ ảnh thật.

> **Thích ứng ngành:** cây thư mục dùng chung mọi ngành — chỉ đổi mã `[DN]` và tên chủ đề. **B2B (RocketAI):** thêm folder `07 Screenshot hệ thống/` cho ảnh chụp dashboard chạy thật. **Nhiều dòng sản phẩm:** tách `02 Banner/` theo sản phẩm (`02 Banner/TraAnGiac/`…). Nguyên tắc **2 bản (gốc + PNG)** và **đặt tên không dấu** giữ nguyên 100%.

## 🔗 Kết nối

- [[Ngày 10 — AI Design & Visual Asset]] · [[Bài Tập Ngày 10 — AI Design & Visual Asset]]
- Đi cùng: [[Template 10.1 — Visual Brand Kit 1 trang]] · [[Template 10.2 — Bảng Kế Hoạch Visual]]
- Đầu ra dùng ở: [[Ngày 11 — AI Video & Audio Factory]] (2 thumbnail) · [[Ngày 13 — Phân Phối Nội Dung & Content Automation]] (xếp lịch)
