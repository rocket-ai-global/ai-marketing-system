---
tags: [guide]
created: 2026-07-06
---

# Vault SME — Hướng Dẫn Kiến Trúc

> Kiến trúc này ghép **PARA** (Projects, Areas, Resources, Archive — tổ chức theo tính hành động/actionability) với **AI Brain** của Dan Martell (lớp quan hệ thực thể — entity layer: People, Companies, Meetings, Decisions), cộng thêm một lớp **Business Context** riêng ở gốc. Mục tiêu tổng thể: sắp xếp toàn bộ dữ liệu doanh nghiệp thành cấu trúc mà AI agent (Hermes agent, coding agent...) đọc hiểu được ngay, để vận hành Sale & Marketing cho 1 doanh nghiệp SME — AI hiểu đúng ngữ cảnh (công ty là ai, ai là khách, quyết định gì đã chốt) thay vì chỉ biết việc gì đang làm. Xem thêm mục "Mục tiêu tổng thể" trong [[CLAUDE]].

## Vì sao ghép 2 mô hình

- **PARA** trả lời: *việc này có đang active không, hay chỉ là tài liệu tham khảo?*
- **AI Brain** trả lời: *việc này liên quan đến ai, công ty nào, quyết định nào trong quá khứ?*
- PARA thuần dễ bị "mồ côi quan hệ" (không biết deal này của khách nào). AI Brain thuần dễ bị "mồ côi trạng thái" (không biết cái gì đang cháy deadline). Ghép lại giải quyết cả hai.

## Cấu trúc thư mục

```
00. Business Context/   ← NGUỒN SỰ THẬT DUY NHẤT về công ty — đọc trước tiên, mọi agent (Hermes, coding agent...) vào đây trước khi làm content/sale/marketing
  ├─ Chân Dung Doanh Nghiệp.md              ← định vị, ICP
  ├─ Brand Voice — Giọng Thương Hiệu.md     ← giọng nói, từ nên/tránh dùng, câu mẫu
  ├─ Business Model Canvas — [Tên].md       ← 9 khối BMC đầy đủ (Osterwalder)
  ├─ Business Model Canvas.canvas           ← bản vẽ trực quan BMC
  ├─ Đánh Giá Mô Hình Kinh Doanh — [Tên].md ← tính nhất quán, PMF
  ├─ MHKD/                                  ← trang chi tiết từng phân khúc/giá trị cốt lõi
  ├─ AI-Sale-Assistant.md                   ← vai trò & nguyên tắc phản hồi của AI
  └─ Sản Phẩm & Dịch Vụ/                    ← 1 file/sản phẩm hoặc gói: tính năng, giá, USP

01. Inbox/              ← capture thô, cuối ngày dọn về 0
02. Projects/           ← có deadline cụ thể (chiến dịch, launch)
03. Areas/              ← trách nhiệm liên tục, không deadline
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
04. Resources/          ← tham khảo, tái sử dụng
  ├─ Playbooks/
  ├─ Templates/
  ├─ Frameworks/
  ├─ Market & Competitor Research/
  │    └─ Đối Thủ/                  ← 1 file/đối thủ, nhật ký cập nhật theo thời gian
  └─ Knowledge/
05. Archive/            ← đã đóng, không xoá

People/                 ← Leads, Customers, Team, Partners — 1 file/người
Companies/              ← Customer accounts, Đối thủ, Vendor/Agency
Meetings/               ← biên bản sale call, discovery call, standup
Decisions/              ← quyết định giá, kênh ads, ngân sách, pivot
Daily/                  ← nhật ký 3–5 dòng/ngày
MOC/                    ← mục lục sống, tổng hợp xuyên thư mục
```

## Nguyên tắc vận hành

1. **Note nào cũng phải link ra ngoài** — một biên bản trong `Meetings/` phải link tới `People/` (ai họp), `Companies/` (công ty nào), và `Projects/` hoặc `Areas/` liên quan. Không có note mồ côi.
2. **`Areas/` là nơi sống hàng ngày.** Khi một `Project` đóng lại, kết quả/bài học phải link về `Area` tương ứng — giống nguyên tắc Active→CORE của MindMirror.
3. **`00. Business Context/` quyết định giọng và ngữ cảnh AI:** [[Chân Dung Doanh Nghiệp]] (định vị, ICP), [[Brand Voice — Giọng Thương Hiệu]] (tone), [[AI-Sale-Assistant]] (vai trò AI khi soạn content/trả lời khách). Điền các file này trước tiên — mọi skill sale/marketing khác đều tham chiếu ngược lại đây.
4. **Automation ban đêm (tuỳ chọn):** cron job quét `01. Inbox/` và `Meetings/` mới trong ngày → tự tạo file `People/`/`Companies/` nếu tên xuất hiện nhưng chưa có hồ sơ → cập nhật liên kết vào `MOC/` → gộp file trùng lặp.

## Công cụ cần cài đặt

Một số skill (ví dụ `phan-tich-doi-thu` khi nâng cấp lên `competitor-profiling`, hoặc các skill research/scrape khác) cần các CLI/API sau. Không bắt buộc cho việc dùng vault cơ bản — chỉ cài khi skill cụ thể yêu cầu:

- **Apify** — scrape dữ liệu mạng xã hội/web quy mô lớn. Lấy token tại https://console.apify.com/account/integrations.
- **Firecrawl** — crawl/parse trang web thành markdown sạch cho các skill cần đọc nhiều trang. Lấy API key tại https://www.firecrawl.dev/app/api-keys.

**Lưu key ở đâu:** tất cả API key lưu trong file `.env` ở gốc vault (đã có sẵn trong `.gitignore`, không commit lên git). Mỗi dòng 1 biến dạng `TEN_BIEN=gia_tri`, ví dụ:

```
APIFY_TOKEN=
FIRECRAWL_API_KEY=
```

Không dán key trực tiếp vào skill, note, hay bất kỳ file nào khác trong vault.

## Cách bắt đầu

1. Điền [[Chân Dung Doanh Nghiệp]], [[Brand Voice — Giọng Thương Hiệu]] và [[AI-Sale-Assistant]] (trong `00. Business Context/`) — hoặc gọi skill `/mo-hinh-kinh-doanh` để được phỏng vấn và tự tạo [[Business Model Canvas — [Tên Doanh Nghiệp]]] + bản vẽ trực quan.
2. Tạo hồ sơ từng sản phẩm/gói trong `00. Business Context/Sản Phẩm & Dịch Vụ/` — đây là thứ Sale và Marketing sẽ tham chiếu liên tục.
3. Đổ toàn bộ ghi chú/khách hàng/deal cũ vào `01. Inbox/`, dọn dần sang đúng thư mục theo bảng dưới.
4. Mỗi tuần mở `MOC/` để xem toàn cảnh pipeline và content calendar.

| Nội dung đầu vào | Chuyển vào |
|---|---|
| Deal/khách hàng mới | `People/` + `Companies/` |
| Sản phẩm/gói mới ra mắt | `00. Business Context/Sản Phẩm & Dịch Vụ/` |
| Ghi âm/note cuộc gọi sale | `Meetings/` |
| Ý tưởng chiến dịch có deadline | `02. Projects/` |
| Quy trình lặp lại (báo cáo tuần, chăm sóc khách) | `03. Areas/` |
| Kịch bản, template, nghiên cứu đối thủ | `04. Resources/` |
