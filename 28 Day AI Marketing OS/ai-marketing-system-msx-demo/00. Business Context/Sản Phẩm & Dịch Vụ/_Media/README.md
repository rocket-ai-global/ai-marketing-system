---
tags: [readme, product, media]
created: 2026-07-07
up:
  - "[[_MOC Sản Phẩm & Dịch Vụ]]"
---

# _Media — Hình ảnh & Video sản phẩm/dịch vụ

> Nơi lưu **tài nguyên gốc** (hình, video, PDF, bảng giá...) đi kèm từng sản phẩm/dịch vụ. File `.md` mô tả sản phẩm vẫn nằm **phẳng** ở thư mục cha `Sản Phẩm & Dịch Vụ/`; media nặng gom về đây để thư mục sản phẩm gọn và dễ tra.

## Quy ước
- **1 thư mục con / 1 sản phẩm**, đặt trùng tên file `.md` sản phẩm. Ví dụ:
  ```
  Sản Phẩm & Dịch Vụ/
  ├─ Gói Massage Trị Liệu.md          ← hồ sơ sản phẩm
  └─ _Media/
     └─ Gói Massage Trị Liệu/         ← media của đúng gói đó
        ├─ hinh/                       ← ảnh sản phẩm, ảnh gói, infographic giá
        │  ├─ 01-anh-chinh.jpg
        │  └─ 02-bang-gia.png
        └─ video/                      ← video demo, review, hướng dẫn
           └─ demo-quy-trinh.mp4
  ```
- **Đặt tên file** không dấu, không khoảng trắng, có số thứ tự: `01-mo-ta-ngan.jpg`.
- **Nhúng vào hồ sơ sản phẩm** bằng embed Obsidian trong mục *Hình ảnh & Video*:
  `![[_Media/Gói Massage Trị Liệu/hinh/01-anh-chinh.jpg]]`
- **Ảnh review/testimonial của khách** KHÔNG để đây — để ở [[_MOC Feedback & Chứng Thực]] (`04. Resources/Feedback & Chứng Thực/Media/`), vì đó là bằng chứng xã hội dùng chung, không phải tài nguyên gốc của sản phẩm.
- File nặng (video) đã được git bỏ qua hay chưa tuỳ `.gitignore`; nếu repo phình to, cân nhắc thêm `*.mp4` vào `.gitignore` và lưu video ở kho ngoài, chỉ để link.
