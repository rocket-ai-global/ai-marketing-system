---
tags: [guide]
created: 2026-07-06
---

# Vault SME — Hướng Dẫn Kiến Trúc

> Kiến trúc này ghép **PARA** (Projects, Areas, Resources, Archive — tổ chức theo tính hành động/actionability) với **AI Brain** của Dan Martell (lớp quan hệ thực thể — entity layer: People, Companies, Meetings, Decisions). Mục tiêu: vận hành Sale & Marketing cho 1 doanh nghiệp SME, để AI hiểu đúng ngữ cảnh (ai, công ty nào, quyết định gì) thay vì chỉ biết việc gì đang làm.

## Vì sao ghép 2 mô hình

- **PARA** trả lời: *việc này có đang active không, hay chỉ là tài liệu tham khảo?*
- **AI Brain** trả lời: *việc này liên quan đến ai, công ty nào, quyết định nào trong quá khứ?*
- PARA thuần dễ bị "mồ côi quan hệ" (không biết deal này của khách nào). AI Brain thuần dễ bị "mồ côi trạng thái" (không biết cái gì đang cháy deadline). Ghép lại giải quyết cả hai.

## Cấu trúc thư mục

```
00. Inbox/              ← capture thô, cuối ngày dọn về 0
01. Projects/           ← có deadline cụ thể (chiến dịch, launch)
02. Areas/              ← trách nhiệm liên tục, không deadline
  ├─ Sales Pipeline & CRM/
  ├─ Marketing Channels/
  ├─ Brand & Content/
  │    └─ Content Đã Đăng/          ← nhật ký content thực tế đã lên sóng, 1 file/post
  ├─ Customer Success & Retention/
  └─ Analytics & Reporting/
       ├─ Báo Cáo Ngày/
       ├─ Báo Cáo Tuần/
       ├─ Báo Cáo Quý/
       └─ Tương Tác Mạng Xã Hội/    ← follower, reach, engagement rate theo kênh
03. Resources/          ← tham khảo, tái sử dụng
  ├─ Playbooks/
  ├─ Templates/
  ├─ Frameworks/
  ├─ Market & Competitor Research/
  │    └─ Đối Thủ/                  ← 1 file/đối thủ, nhật ký cập nhật theo thời gian
  └─ Knowledge/
04. Archive/            ← đã đóng, không xoá

People/                 ← Leads, Customers, Team, Partners — 1 file/người
Companies/              ← Customer accounts, Đối thủ, Vendor/Agency
Sản Phẩm & Dịch Vụ/     ← 1 file/sản phẩm hoặc gói: tính năng, giá, USP
Meetings/               ← biên bản sale call, discovery call, standup
Decisions/              ← quyết định giá, kênh ads, ngân sách, pivot
Daily/                  ← nhật ký 3–5 dòng/ngày
MOC/                    ← mục lục sống, tổng hợp xuyên thư mục

Chân Dung Doanh Nghiệp.md          ← định vị, ICP, tone thương hiệu
Business Model Canvas — [Tên].md   ← 9 khối BMC đầy đủ (Osterwalder)
AI-Sale-Assistant.md               ← vai trò & nguyên tắc phản hồi của AI
```

## Nguyên tắc vận hành

1. **Note nào cũng phải link ra ngoài** — một biên bản trong `Meetings/` phải link tới `People/` (ai họp), `Companies/` (công ty nào), và `Projects/` hoặc `Areas/` liên quan. Không có note mồ côi.
2. **`Areas/` là nơi sống hàng ngày.** Khi một `Project` đóng lại, kết quả/bài học phải link về `Area` tương ứng — giống nguyên tắc Active→CORE của MindMirror.
3. **Hai file định danh quyết định giọng AI:** [[Chân Dung Doanh Nghiệp]] (định vị, ICP, tone thương hiệu) và [[AI-Sale-Assistant]] (vai trò AI khi soạn content/trả lời khách). Điền 2 file này trước tiên.
4. **Automation ban đêm (tuỳ chọn):** cron job quét `00. Inbox/` và `Meetings/` mới trong ngày → tự tạo file `People/`/`Companies/` nếu tên xuất hiện nhưng chưa có hồ sơ → cập nhật liên kết vào `MOC/` → gộp file trùng lặp.

## Cách bắt đầu

1. Điền [[Chân Dung Doanh Nghiệp]] và [[AI-Sale-Assistant]] — hoặc gọi skill `/business-model-canvas` để được phỏng vấn và tự tạo [[Business Model Canvas — [Tên Doanh Nghiệp]]] + bản vẽ trực quan.
2. Tạo hồ sơ từng sản phẩm/gói trong `Sản Phẩm & Dịch Vụ/` — đây là thứ Sale và Marketing sẽ tham chiếu liên tục.
3. Đổ toàn bộ ghi chú/khách hàng/deal cũ vào `00. Inbox/`, dọn dần sang đúng thư mục theo bảng dưới.
4. Mỗi tuần mở `MOC/` để xem toàn cảnh pipeline và content calendar.

| Nội dung đầu vào | Chuyển vào |
|---|---|
| Deal/khách hàng mới | `People/` + `Companies/` |
| Sản phẩm/gói mới ra mắt | `Sản Phẩm & Dịch Vụ/` |
| Ghi âm/note cuộc gọi sale | `Meetings/` |
| Ý tưởng chiến dịch có deadline | `01. Projects/` |
| Quy trình lặp lại (báo cáo tuần, chăm sóc khách) | `02. Areas/` |
| Kịch bản, template, nghiên cứu đối thủ | `03. Resources/` |
