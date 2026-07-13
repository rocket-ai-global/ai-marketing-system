---
tags: [guide, journal, ceo]
created: 2026-07-07
---

# Nhật Ký CEO — Hướng Dẫn

> **Vì sao có folder này:** với nhiều SME, thương hiệu **gắn liền với cá nhân người sáng lập/CEO**. Content thật, có hồn đến từ chuyện thật, quan điểm thật, cách nói riêng của CEO — không phải từ template. Folder này là **kho nguyên liệu giọng cá nhân** để AI (và người viết) khai thác khi sản xuất content, thay vì bịa cho "nghe hay".

## Khác gì với `Daily/`?
| | `Daily/` | `Nhật Ký CEO/` (folder này) |
|---|---|---|
| Nội dung | Nhật ký **công việc** 3–5 dòng: hôm nay làm gì, quyết định gì | Chuyện/cảm xúc/quan điểm **cá nhân** của CEO — nguyên liệu giọng & câu chuyện |
| Ai đọc lại | AI ghép ngữ cảnh vận hành | AI **viết content đúng chất CEO** (story, quan điểm, giọng) |
| Độ riêng tư | Thấp | Có thể cao → xem mục Quyền riêng tư |

Giọng thương hiệu chuẩn hoá vẫn ở [[Brand Voice — Giọng Thương Hiệu]]; folder này là **nguồn thô** nuôi giọng đó.

## Viết gì mỗi lần (không cần đủ hết, viết cái nào có cái đó)
- **Câu chuyện / khoảnh khắc** hôm nay: gặp ai, chuyện gì, chi tiết cụ thể (chi tiết mới tạo được content thật).
- **Cảm xúc / suy nghĩ thật** — chưa lọc, kể cả bực bội, nghi ngờ, tự hào.
- **Quan điểm / góc nhìn ("hot take")** về ngành, nghề, khách hàng, đối thủ.
- **Bài học / sai lầm / lần đổi ý** — before→after trong suy nghĩ.
- **Cách nói riêng** — câu cửa miệng, từ hay dùng, ví von riêng (đưa dần vào [[Brand Voice — Giọng Thương Hiệu]]).
- **Hạt giống content** — chuyện trên có thể thành bài gì, kênh nào.

## Quy ước để AI lọc được
- Tên file: `YYYY-MM-DD — Nhật ký.md`.
- Đánh dấu trong bài bằng tag để tra nhanh:
  - `#hat-giong-content` — đoạn có thể phát triển thành content
  - `#quan-diem` — góc nhìn/lập trường dùng làm bài "chính kiến"
  - `#cau-chuyen` — mẩu chuyện kể được
  - `#giong-noi` — câu/cách diễn đạt đặc trưng CEO
- Frontmatter `rieng_tu: yes` cho mục **không được dùng công khai**; AI chỉ khai thác đoạn `rieng_tu: no`.

## Quyền riêng tư (quan trọng)
Nhật ký cá nhân có thể chứa chuyện riêng. Nếu CEO không muốn commit lên git, thêm `Nhật Ký CEO/` vào `.gitignore`. Dù vậy vẫn nên viết trong vault để AI nội bộ đọc được — chỉ là không đẩy lên remote.

## Liên kết
- Giọng thương hiệu (đích đến): [[Brand Voice — Giọng Thương Hiệu]]
- Sản xuất content: [[_MOC Brand & Content]]
- Hồ sơ CEO (nếu có): [[People/]]
