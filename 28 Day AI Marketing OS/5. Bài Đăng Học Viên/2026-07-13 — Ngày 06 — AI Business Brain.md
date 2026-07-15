---
created: 2026-07-13
tags: [aios, cohort, bai-dang-hoc-vien, day6, ai-business-brain]
program: 28 Day AIOS
day: 6
topic: AI Business Brain
status: ready-to-send
related_assets:
  - "[[Tài Liệu Thực Hành Buổi 06 — AI Business Brain & 2 Trợ Lý Nội Bộ]]"
related_templates:
  - "[[Template 6.1 — AI Instruction Document]]"
  - "[[Template 6.1A — Bản Mẫu MSX AI Business Brain]]"
  - "[[Template 6.2 — Test Case Report 6 Ca Chuẩn]]"
  - "[[Template 6.3 — Improvement List]]"
---
# 🧠 NGÀY 06 — AI BUSINESS BRAIN & 2 TRỢ LÝ NỘI BỘ

Chào cả nhà,

Hôm nay chúng ta bước sang **Ngày 06 của 28 Day AIOS**.

5 ngày vừa rồi, anh/chị đã tạo các mảnh nền tảng:

| Ngày | Tài sản đã có |
|---:|---|
| 01 | Business Snapshot + AI Opportunity Map |
| 02 | Customer Avatar + Customer Journey |
| 03 | Offer + Sales Message |
| 04 | Knowledge Base cho doanh nghiệp |
| 05 | Prompt Library + Context Block + Brand Voice |

Hôm nay, chúng ta **lắp các mảnh đó thành một bộ não AI chạy được**.

> **Mục tiêu Ngày 06:** tạo **AI Business Brain v1** và 2 trợ lý vận hành **nội bộ** đầu tiên: **Sales Assistant** + **Marketing Assistant**.

---

## 1. Hiểu đúng: hôm nay chưa phải tạo chatbot public cho khách

Sales Assistant và Marketing Assistant hôm nay là **trợ lý nội bộ**.

| Trợ lý | Ai dùng? | Dùng để làm gì? |
|---|---|---|
| **Sales Assistant** | Founder / sales / tư vấn viên | Gợi ý cách trả lời khách, xử lý từ chối, follow-up, chấm lead, chuẩn bị call |
| **Marketing Assistant** | Founder / marketing / content team | Viết content, hook, script video, lịch bài, landing copy, lead magnet |

Nghĩa là:

```text
AI gợi ý → người thật duyệt/sửa → người thật gửi/đăng/sử dụng.
```

Hôm nay **chưa bắt buộc nhúng bot ra website/Zalo/Messenger cho khách tự chat**. Việc đó là lớp nâng cao sau khi Brain đã đủ chắc.

---

## 2. Công thức hệ thống

```text
Knowledge Base
+ Master Instruction
= AI Business Brain

AI Business Brain
+ Vai Sales
= Sales Assistant

AI Business Brain
+ Vai Marketing
= Marketing Assistant
```

Nói đơn giản:

- **Knowledge Base** = AI biết gì về doanh nghiệp.
- **Master Instruction** = AI được/không được làm gì, nói giọng nào, ưu tiên gì.
- **Sales/Marketing Assistant** = cùng một bộ não, nhưng mặc áo vai trò khác nhau.

---

## 3. Hôm nay cần tạo 5 output

### Output 1 — AI Instruction Document

Dùng:

```text
Template 6.1 — AI Instruction Document
```

Instruction phải đủ 7 phần:

1. AI là ai?
2. Nhiệm vụ & thứ tự ưu tiên.
3. Nguồn sự thật lấy từ đâu?
4. AI được phép làm gì?
5. AI không được phép làm gì?
6. Giọng thương hiệu.
7. Khi nào chuyển người thật?

Yêu cầu tối thiểu:

```text
≥5 điều cấm
≥1 điều cấm đặc thù ngành
≥3 tình huống chuyển người thật
```

---

### Output 2 — AI Business Brain v1

Tạo trên một trong các nền tảng:

```text
RocketAgent / ChatGPT Project / Claude Project / Hermes-Jarvis
```

Nạp tối thiểu 3 tài liệu lõi:

```text
Business Overview
Product / Service Knowledge
FAQ & Objection
```

Test câu khởi động:

```text
Bên mình bán gì, bán cho ai, offer/giá chính là gì?
```

Nếu AI trả lời sai giá/sản phẩm/đối tượng khách hàng → chưa đạt.

---

### Output 3 — Sales Assistant nội bộ

Tạo 1 trợ lý dùng cho sales/founder/tư vấn viên.

Nhiệm vụ:

```text
Chấm lead
Gợi ý cách trả lời inbox
Xử lý từ chối
Soạn follow-up
Chuẩn bị sales call
Tóm tắt nhu cầu khách
Đề xuất bước tiếp theo
```

Test mẫu:

```text
Khách nói: “Gói này đắt quá, bên khác rẻ hơn.”
Hãy gợi ý 3 cách trả lời đúng giọng thương hiệu,
không giảm giá bừa,
không hứa kết quả quá đà,
và kết bằng một CTA nhỏ.
```

---

### Output 4 — Marketing Assistant nội bộ

Tạo 1 trợ lý dùng cho marketing/content/founder.

Nhiệm vụ:

```text
Viết bài Facebook
Tạo hook video
Viết script ngắn
Lên content calendar
Viết landing copy
Tạo lead magnet
Tái chế nội dung
```

Test mẫu:

```text
Dựa trên Customer Avatar chính và offer chủ lực,
viết 5 hook Facebook để kéo đúng tệp khách hàng,
giọng đúng thương hiệu,
không nói chung chung,
có CTA rõ.
```

---

### Output 5 — Test Case Report + Improvement List

Dùng:

```text
Template 6.2 — Test Case Report 6 Ca Chuẩn
Template 6.3 — Improvement List
```

6 ca test bắt buộc:

| # | Ca test | Kiểm tra điều gì? |
|---:|---|---|
| 1 | Hỏi giá/sản phẩm | AI có trả lời đúng giá/offer không |
| 2 | So sánh/đối thủ | AI có nói USP, không chê đối thủ không |
| 3 | Chê đắt | Sales Assistant có xử lý objection đúng không |
| 4 | Hỏi ngoài Knowledge Base | AI có biết nói “chưa có đủ dữ liệu” không |
| 5 | Nhờ viết content | Marketing Assistant có viết đúng persona/brand/CTA không |
| 6 | Câu chạm điều cấm | AI có biết dừng và chuyển người thật không |

Chấm từng ca:

```text
✅ Dùng được ngay
⚠️ Đúng hướng nhưng cần sửa
❌ Sai / bịa / vi phạm điều cấm
```

Quan trọng: nếu AI sai, **không xấu hổ**. Lỗi đó chính là nguyên liệu để vá Brain.

---

## 4. Bản mẫu xem trước khi làm

Mở bản mẫu:

```text
Template 6.1A — Bản Mẫu MSX AI Business Brain
```

Đây là ví dụ Mẫu Sơn Xanh đã có:

- danh tính AI
- nguồn sự thật
- điều cấm về sức khỏe/dược liệu
- giọng thương hiệu
- tình huống chuyển người thật
- test Sales Assistant
- test Marketing Assistant

---

## 5. Lỗi cần tránh

- Tạo assistant khi chưa có Knowledge Base.
- Dán hết giá/sản phẩm vào Instruction thay vì để trong Product Knowledge.
- Không ghi điều cấm → AI dễ hứa quá đà.
- Tạo 5 assistant giống hệt nhau, không có vai trò riêng.
- Test toàn câu dễ, không test câu khách chê đắt / hỏi ngoài dữ liệu.
- Thấy AI sai nhưng không ghi vào Improvement List.
- Nhầm Sales/Marketing Assistant nội bộ với chatbot public cho khách dùng.

---

## 6. Bài nộp hôm nay

Tên file:

```text
[Tên DN] — Ngày 06 — AI Business Brain Report
```

Nộp đủ 5 phần:

1. Link **AI Instruction Document**.
2. Ảnh/link **AI Business Brain** trả lời câu khởi động.
3. Ảnh/link **Sales Assistant** xử lý 1 ca chê đắt.
4. Ảnh/link **Marketing Assistant** viết 1 output content.
5. **Test Case Report 6 ca** + **Improvement List ≥5 mục**.

---

## 7. Deadline

```text
23:59 hôm nay
```

> Ngày 06 là vé vào Demo Day. Nếu Brain chưa chạy và chưa test, Ngày 07 sẽ không có gì để demo.

Chúc cả nhà dựng được **bộ não AI đầu tiên cho chính doanh nghiệp mình** hôm nay.
