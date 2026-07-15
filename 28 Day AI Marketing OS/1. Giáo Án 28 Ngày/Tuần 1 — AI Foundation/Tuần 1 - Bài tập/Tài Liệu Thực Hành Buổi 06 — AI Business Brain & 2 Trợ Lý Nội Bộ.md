---
created: 2026-07-13
tags: [aios, student-handout, day6, ai-business-brain, assistant]
program: 28 Day AIOS
week: 1
day: 6
status: ready-to-send
up:
  - "[[Bài Tập Ngày 6 — AI Business Brain]]"
related_templates:
  - "[[Template 6.1 — AI Instruction Document]]"
  - "[[Template 6.1A — Bản Mẫu MSX AI Business Brain]]"
  - "[[Template 6.2 — Test Case Report 6 Ca Chuẩn]]"
  - "[[Template 6.3 — Improvement List]]"
---
# Tài Liệu Thực Hành Buổi 06 — AI Business Brain & 2 Trợ Lý Nội Bộ

> **Mục tiêu:** sau buổi này, doanh nghiệp của anh/chị có 1 **AI Business Brain v1** và 2 trợ lý vận hành **nội bộ**: **Sales Assistant** + **Marketing Assistant**. Hai trợ lý này giúp team làm việc nhanh và đúng dữ liệu hơn; chưa phải chatbot public cho khách tự dùng.

---

## 0. Bức tranh hệ thống

```text
Ngày 04: Knowledge Base
        ↓
Ngày 05: Prompt Library + Brand Voice
        ↓
Ngày 06: AI Business Brain + Sales Assistant + Marketing Assistant
        ↓
Ngày 07: Demo Brain + Foundation Scorecard
        ↓
Tuần 2: Dùng Marketing Assistant để chạy Content / Lead Magnet / Landing Page
        ↓
Tuần 3: Dùng Sales Assistant để chạy Lead / Follow-up / Proposal
```

Công thức cần nhớ:

```text
Knowledge Base = AI biết gì
Master Instruction = AI hành xử thế nào
Business Brain = Knowledge Base + Master Instruction
Assistant = Business Brain + vai trò cụ thể
```

---

## 1. Chuẩn bị dữ liệu trước khi tạo Brain

Trước khi mở RocketAgent/ChatGPT/Claude/Hermes, hãy gom đủ tối thiểu 5 nhóm dữ liệu:

| Nhóm dữ liệu | Có chưa? | File/nguồn |
|---|:---:|---|
| Business Overview — doanh nghiệp là ai, bán gì, cho ai | ⬜ |  |
| Product/Service Knowledge — sản phẩm, gói, giá, chính sách | ⬜ |  |
| Customer Avatar — khách chính, pain, desire, objection | ⬜ |  |
| FAQ & Objection — câu hỏi/thắc mắc/từ chối thường gặp | ⬜ |  |
| Brand Voice — giọng viết, cách xưng hô, từ nên/không nên dùng | ⬜ |  |

> Nếu thiếu giá, chính sách, sản phẩm, điều cấm: **không được bịa để điền cho đủ**. Ghi vào Improvement List.

---

## 2. Viết Master Instruction — “hiến pháp” của AI

Mở:

```text
Template 6.1 — AI Instruction Document
```

Điền 7 phần dưới đây.

### 2.1. Danh tính

Copy mẫu:

```text
Bạn là trợ lý AI của [Tên doanh nghiệp].
Bạn hỗ trợ đội ngũ nội bộ trong các việc: marketing, sales, tư vấn, chăm sóc khách hàng và vận hành.
Bạn chỉ dùng dữ liệu trong Knowledge Base của doanh nghiệp, không trả lời như một chuyên gia đại trà.
```

### 2.2. Nhiệm vụ & thứ tự ưu tiên

Copy mẫu:

```text
Thứ tự ưu tiên của bạn:
1. Chính xác theo Knowledge Base.
2. An toàn, không vượt phạm vi tư vấn.
3. Đúng giọng thương hiệu.
4. Hữu ích cho người dùng nội bộ.
5. Dẫn đến bước tiếp theo rõ ràng.
6. Nếu thiếu dữ liệu, nói rõ chưa có đủ thông tin và đề xuất bổ sung/chuyển người thật.
```

### 2.3. Nguồn sự thật

Điền bảng:

| Nguồn | File/link | AI dùng để làm gì? |
|---|---|---|
| Business Overview |  | Hiểu doanh nghiệp |
| Product/Service Knowledge |  | Giá, gói, chính sách |
| Customer Avatar |  | Viết đúng người, đúng pain |
| FAQ & Objection |  | Trả lời câu hỏi, xử lý từ chối |
| Brand Voice |  | Giữ đúng giọng thương hiệu |

Rule bắt buộc:

```text
Thông tin sống như giá, chính sách, tồn kho, cam kết, ưu đãi chỉ lấy từ file nguồn. Nếu không có trong nguồn, AI phải nói chưa có đủ dữ liệu.
```

### 2.4. AI được phép làm

Gợi ý tick:

- [ ] Trả lời FAQ theo Knowledge Base.
- [ ] Gợi ý câu trả lời inbox cho team sales/CSKH.
- [ ] Xử lý từ chối theo Objection Library.
- [ ] Viết content, hook, script theo Brand Voice.
- [ ] Tóm tắt nhu cầu khách từ dữ liệu team đưa vào.
- [ ] Đề xuất bước tiếp theo cho lead/campaign.
- [ ] Chỉ ra dữ liệu còn thiếu cần bổ sung.

### 2.5. AI không được phép làm

Bắt buộc có tối thiểu 5 điều cấm. Chọn và sửa theo ngành:

- [ ] Không tự tạo giá, ưu đãi, chính sách mới.
- [ ] Không hứa kết quả tuyệt đối.
- [ ] Không bịa số liệu, chứng nhận, case study, tồn kho.
- [ ] Không nói xấu đối thủ.
- [ ] Không tiết lộ dữ liệu nội bộ/khách hàng.
- [ ] Không tư vấn y tế/pháp lý/tài chính nếu doanh nghiệp không có thẩm quyền.
- [ ] Không gửi câu trả lời trực tiếp cho khách nếu chưa có người thật duyệt.
- [ ] Điều cấm đặc thù ngành: ...

### 2.6. Giọng thương hiệu

Dán khối `[GIỌNG]` đã làm ở Ngày 05.

Mẫu:

```text
Xưng hô: ...
Giọng: ...
Nên dùng từ: ...
Không nên dùng từ: ...
Độ dài câu trả lời: ...
CTA mặc định: ...
```

### 2.7. Leo thang/chuyển người thật

Điền bảng:

| Tình huống | AI nói gì? | Chuyển cho ai? | Thời hạn |
|---|---|---|---|
| Khách hỏi ngoài Knowledge Base | “Thông tin này em chưa có đủ dữ liệu xác nhận...” | Người phụ trách | Trong ngày |
| Khách khiếu nại/hoàn tiền |  | CSKH/founder | 24h |
| Câu hỏi nhạy cảm/y tế/pháp lý/tài chính |  | Người có thẩm quyền | Ngay |
| Lead nóng muốn mua/báo giá custom |  | Sales/founder | 2–24h |

---

## 3. Tạo AI Business Brain v1

### Track A — RocketAgent

1. Tạo assistant/project mới:

```text
[Tên DN] — Business Brain v1
```

2. Nạp Knowledge Base:

```text
Business Overview
Product/Service Knowledge
FAQ & Objection
Brand Voice
```

3. Dán Master Instruction.
4. Lưu.
5. Test câu khởi động:

```text
Bên mình bán gì, bán cho ai, offer/giá chính là gì?
```

### Track B — ChatGPT/Claude Project

1. Tạo Project mới:

```text
[Tên DN] — Business Brain v1
```

2. Upload 3–5 tài liệu lõi.
3. Dán Master Instruction vào phần hướng dẫn project.
4. Test câu khởi động như trên.

### Track C — Hermes/Jarvis

1. Đặt/để các file trong Vault SME.
2. Đảm bảo Jarvis đọc được đúng folder/file.
3. Gửi prompt test:

```text
Jarvis, dùng dữ liệu trong vault [Tên DN].
Tóm tắt doanh nghiệp bán gì, cho ai, offer/giá chính là gì.
Nếu thiếu dữ liệu, nói rõ thiếu gì.
```

---

## 4. Tạo Sales Assistant nội bộ

Tên gợi ý:

```text
[Tên DN] — Sales Assistant v1
```

Dùng cùng Business Brain, thêm lớp vai sau:

```text
Bạn là Sales Assistant nội bộ của [Tên DN].
Bạn hỗ trợ founder/sales/CSKH chuẩn bị câu trả lời cho khách, xử lý từ chối, follow-up, chấm lead và chuẩn bị sales call.

Nguyên tắc:
- Không gửi trực tiếp cho khách; output là bản nháp để người thật duyệt.
- Không tự tạo giá, ưu đãi, cam kết, chính sách.
- Không hứa kết quả tuyệt đối.
- Luôn dựa trên Knowledge Base và Objection Library.
- Output nên ngắn, rõ, dùng được trong inbox/call/follow-up.
- Mỗi câu trả lời nên có CTA nhỏ phù hợp.

Output mặc định:
1. Tóm tắt tình huống khách.
2. Mức độ fit/nóng của lead nếu có dữ liệu.
3. 2–3 gợi ý câu trả lời.
4. Bước tiếp theo nên làm.
5. Dữ liệu còn thiếu cần hỏi thêm.
```

### Test Sales Assistant

Copy test:

```text
Khách nói: “Gói này đắt quá, bên khác rẻ hơn nhiều.”
Hãy gợi ý 3 cách trả lời cho sales,
đúng giọng thương hiệu,
không giảm giá bừa,
không hứa kết quả tuyệt đối,
và kết bằng CTA nhỏ.
```

Đạt nếu:

- [ ] Không bịa giá/chính sách.
- [ ] Không chê đối thủ.
- [ ] Có đồng cảm.
- [ ] Giữ đúng giá trị/USP.
- [ ] Có CTA rõ.

---

## 5. Tạo Marketing Assistant nội bộ

Tên gợi ý:

```text
[Tên DN] — Marketing Assistant v1
```

Dùng cùng Business Brain, thêm lớp vai sau:

```text
Bạn là Marketing Assistant nội bộ của [Tên DN].
Bạn hỗ trợ founder/marketing/content team tạo nội dung đúng customer avatar, offer, brand voice và mục tiêu kinh doanh.

Nguyên tắc:
- Không viết chung chung.
- Luôn gắn output với persona, pain, offer và CTA.
- Không dùng claim chưa có trong Knowledge Base.
- Không hứa kết quả tuyệt đối.
- Nếu thiếu insight/giá/case/bằng chứng, hãy nói rõ cần bổ sung.

Output mặc định:
1. Persona mục tiêu.
2. Insight/pain đang đánh vào.
3. Ý tưởng/hook/content.
4. CTA.
5. Dữ liệu cần kiểm tra trước khi đăng.
```

### Test Marketing Assistant

Copy test:

```text
Dựa trên Customer Avatar chính và offer chủ lực của doanh nghiệp,
viết 5 hook Facebook để kéo đúng tệp khách hàng.
Yêu cầu:
- đúng brand voice,
- không nói chung chung,
- không hứa quá đà,
- mỗi hook có CTA nhỏ.
```

Đạt nếu:

- [ ] Đúng persona.
- [ ] Đúng pain/offer.
- [ ] Đúng giọng thương hiệu.
- [ ] Không bịa claim.
- [ ] Có CTA.

---

## 6. Chạy 6 test case nghiệm thu

Dùng:

```text
Template 6.2 — Test Case Report 6 Ca Chuẩn
```

| # | Test | Prompt mẫu | Kỳ vọng |
|---:|---|---|---|
| 1 | Hỏi giá/sản phẩm | “Bên mình có gói/sản phẩm nào, giá bao nhiêu?” | Đúng giá, đúng gói, CTA nhỏ |
| 2 | So sánh đối thủ | “Bên mình khác gì [đối thủ/giải pháp khác]?” | Nói USP, không chê đối thủ |
| 3 | Chê đắt | “Sao bên mình đắt vậy?” | Đồng cảm, giữ giá trị, không giảm giá bừa |
| 4 | Ngoài Knowledge Base | “Bên mình có chính sách X không?” nếu KB chưa có | Nói chưa có dữ liệu, chuyển người thật |
| 5 | Viết content | “Viết 1 bài Facebook cho offer chính” | Đúng persona/brand/CTA |
| 6 | Chạm điều cấm | Hỏi claim nhạy cảm/ngành nhạy cảm | Từ chối đúng ranh giới, chuyển người thật |

Chấm:

```text
✅ dùng được ngay
⚠️ đúng hướng nhưng cần sửa
❌ sai / bịa / vi phạm điều cấm
```

---

## 7. Truy nguyên lỗi và vá Brain

Khi AI sai, hỏi:

```text
Lỗi này do thiếu dữ liệu trong Knowledge Base hay do Instruction chưa rõ?
```

| Loại lỗi | Sửa ở đâu? | Ví dụ |
|---|---|---|
| Sai giá/sản phẩm | Product/Service Knowledge | Bổ sung bảng giá đúng |
| Bịa chính sách | Policy/FAQ | Ghi rõ chưa có/không áp dụng |
| Hứa quá đà | Instruction phần “Không được phép” | Thêm câu cấm claim |
| Sai giọng | Brand Voice | Thêm ví dụ nên/không nên dùng |
| Content chung chung | Customer Avatar/Offer | Bổ sung pain/USP/CTA |

Sau khi sửa, test lại các ca ⚠️/❌ và ghi vào:

```text
Template 6.3 — Improvement List
```

---

## 8. Bài nộp cuối ngày

Tạo file:

```text
[Tên DN] — Ngày 06 — AI Business Brain Report
```

Nộp theo cấu trúc:

```markdown
# [Tên DN] — Ngày 06 — AI Business Brain Report

## 1. Link AI Instruction Document
- Link/file:

## 2. AI Business Brain v1
- Nền tảng dùng:
- Tên Brain:
- Ảnh/link test câu khởi động:
- Kết quả: ✅ / ⚠️ / ❌

## 3. Sales Assistant
- Tên assistant:
- Ảnh/link test ca chê đắt:
- Kết quả:

## 4. Marketing Assistant
- Tên assistant:
- Ảnh/link test viết hook/content:
- Kết quả:

## 5. Test Case Report 6 ca
- Link/file:
- Số ca ✅ vòng 1:
- Số ca ✅ sau vòng 2:

## 6. Improvement List
| # | Lỗi/thiếu dữ liệu | Sửa ở đâu | Owner | Deadline | Trạng thái |
|---|---|---|---|---|---|
| 1 |  |  |  |  |  |
```

---

## 9. Tiêu chí đạt Ngày 06

- [ ] Instruction đủ 7 phần.
- [ ] Có ≥5 điều cấm, ≥1 điều cấm đặc thù ngành.
- [ ] Có ≥3 tình huống chuyển người thật.
- [ ] Business Brain chạy được trên 1 nền tảng.
- [ ] Sales Assistant test được ít nhất 1 ca.
- [ ] Marketing Assistant test được ít nhất 1 ca.
- [ ] Chạy đủ 6 test case.
- [ ] Có Improvement List ≥5 mục.
- [ ] Có bằng chứng ảnh/link.
- [ ] Sửa lại ít nhất 1 lỗi và test lại.

---

## 10. Câu nhớ cuối buổi

> **Ngày 06 không phải để tạo nhiều bot. Ngày 06 là để tạo một bộ não đúng dữ liệu, rồi gắn hai vai nội bộ đầu tiên: Sales và Marketing. Brain đúng thì tuần 2 chạy marketing mới đúng; Brain sai thì tuần 2 sẽ khuếch đại lỗi.**
