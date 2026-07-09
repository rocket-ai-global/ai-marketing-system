---
created: 2026-07-09
tags: [project, aios, assignment, day4]
up:
  - "[[_MOC 28 Day AIOS]]"
---

# 📋 Bài Tập Ngày 4 — KNOWLEDGE BASE CHO DOANH NGHIỆP

> **Mục tiêu:** Thu thập & chuẩn hoá dữ liệu nội bộ để AI có thể hiểu doanh nghiệp, trả lời nhất quán như 1 nhân viên thực thụ. Không có Knowledge Base → AI nói chung chung. Có KB tốt → AI thành trợ lý marketing/sale/CSKH cực mạnh.

---

## 📝 BÀI NỘP (4 output — nộp trước 22:00)

### Output 1: Product Knowledge Document

```markdown
## Danh sách sản phẩm/dịch vụ

| # | Tên SP/DV | Mô tả | Giá | Thời gian | Đối tượng |
|---|-----------|-------|-----|-----------|-----------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

## Chính sách
- **Thanh toán:** 
- **Bảo hành/Đổi trả:** 
- **Giao hàng/Triển khai:** 

## FAQ (ít nhất 15 câu)
1. Q:  | A: 
2. Q:  | A: 
...
```

### Output 2: Sales Knowledge Base

```markdown
## Kịch bản tư vấn hiện tại
(Nhập nguyên văn kịch bản sale đang dùng)

## Xử lý phản đối (Objection Handling)

| KH nói | Mình trả lời |
|--------|-------------|
| "Đắt quá" | |
| "Để em suy nghĩ" | |
| "Có chắc hiệu quả không?" | |
| "Thôi em tự làm được" | |
| "Để em hỏi chồng/vợ đã" | |

## Quy trình chốt sale
1. 
2. 
3. 

## Quy trình follow-up
- Sau 1 ngày: 
- Sau 3 ngày: 
- Sau 7 ngày: 
- Sau 14 ngày: 
```

### Output 3: Marketing Knowledge Base

```markdown
## Content đã có
- **Bài viết Facebook:** (liệt kê 5-10 bài tiêu biểu)
- **Video:** (liệt kê 3-5 video)
- **Hình ảnh quảng cáo:** (liệt kê)
- **Landing page cũ:** (link)
- **Email mẫu:** (copy)

## Phong cách content
- **Giọng văn:** (thân thiện / chuyên nghiệp / hài hước...)
- **Màu sắc thương hiệu:** 
- **Logo:** (đính kèm file)
- **Hashtag thường dùng:** 
```

### Output 4: Tổ chức thư mục KB

Tạo cấu trúc thư mục trong Vault SME:

```markdown
📁 Knowledge Base/
├── 📁 01. Business Overview/
│   └── Tầm nhìn, Sứ mệnh, Giá trị cốt lõi, Đội ngũ
├── 📁 02. Product & Service/
│   └── Danh sách SP, mô tả, giá, chính sách
├── 📁 03. Customer Avatar/
│   └── Chân dung KH, Pain, Desire, Journey
├── 📁 04. Offer & Sales Message/
│   └── Core Offer, USP, Sales Script
├── 📁 05. Marketing Assets/
│   └── Bài viết cũ, video, hình ảnh, landing page
├── 📁 06. Sales Assets/
│   └── Kịch bản tư vấn, xử lý phản đối, proposal mẫu
├── 📁 07. FAQ & Objection/
│   └── FAQ database, Objection matrix
├── 📁 08. SOP & Operation/
│   └── Quy trình nội bộ, CSKH, xử lý khiếu nại
├── 📁 09. Case Study/
│   └── Khách hàng thành công, testimonial
└── 📁 10. Reports & Metrics/
    └── Báo cáo, số liệu, KPI
```

> ✅ **Chụp màn hình** thư mục đã tạo trong Vault → nộp

---

## ⚡ HƯỚNG DẪN NHANH (90 phút)

| Bước | Làm gì | Mất |
|:---:|--------|:---:|
| 1 | Thu thập dữ liệu sản phẩm + FAQ | 20' |
| 2 | Thu thập dữ liệu bán hàng (kịch bản, phản đối, follow-up) | 20' |
| 3 | Thu thập dữ liệu marketing (content cũ, phong cách) | 20' |
| 4 | Tổ chức thư mục KB trong Vault + chụp màn hình | 20' |
| 5 | Kiểm tra: mỗi folder có ít nhất 1 file? FAQ đủ 15 câu? | 10' |

---

## 🎯 TIÊU CHÍ ĐẠT

| Tiêu chí | Yêu cầu |
|----------|---------|
| Product Knowledge | Đủ danh sách SP + giá + chính sách + ≥15 FAQ |
| Sales KB | Đủ kịch bản + 5 objection + quy trình chốt + follow-up |
| Marketing KB | Đủ content mẫu + phong cách + brand assets |
| Tổ chức KB | Đủ 10 folder, mỗi folder có ít nhất 1 file |
