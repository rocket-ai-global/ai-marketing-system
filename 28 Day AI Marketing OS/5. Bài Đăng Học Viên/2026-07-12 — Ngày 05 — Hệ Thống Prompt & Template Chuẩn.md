---
created: 2026-07-12
tags: [aios, cohort, bai-dang-nhom, day5, prompt-library]
program: 28 Day AIOS
day: 5
topic: Hệ Thống Prompt & Template Chuẩn
status: ready-to-send
related_templates:
  - "[[Template 5.1 — Prompt Library 50 Prompt Khung]]"
  - "[[Template 5.1A — Bản Mẫu MSX Prompt Library v1]]"
---

# 🚀 NGÀY 05 — HỆ THỐNG PROMPT & TEMPLATE CHUẨN

Chào cả nhà,

Hôm nay chúng ta bước sang **Ngày 05 của hành trình 28 Day AIOS**.

Chủ đề hôm nay là:

> **Xây Prompt Library — thư viện câu lệnh chuẩn để AI làm việc nhất quán cho doanh nghiệp.**

4 ngày đầu, anh/chị đã xây nền:

- **Ngày 01:** Business Snapshot, Business Model Canvas, AI Opportunity Map
- **Ngày 02:** Customer Avatar, Pain–Desire–Fear–Objection, Customer Journey
- **Ngày 03:** Offer, định vị, thông điệp bán hàng
- **Ngày 04:** Knowledge Base — bộ não dữ liệu cho AI

Hôm nay, chúng ta dùng toàn bộ tài sản đó để tạo ra:

> **Một bộ prompt chuẩn giúp AI làm marketing, sales, CSKH và quản trị lặp lại được — không hỏi AI kiểu ngẫu hứng nữa.**

---

## 1. Vì sao cần Prompt Library?

Rất nhiều anh/chị đang dùng AI theo kiểu:

> “Viết cho tôi một bài Facebook.”  
> “Soạn giúp tôi tin nhắn bán hàng.”  
> “Làm cho tôi kịch bản video.”

Cách này có thể ra kết quả tạm được, nhưng có 5 vấn đề:

1. Mỗi lần hỏi một kiểu, kết quả một kiểu
2. Nhân viên không biết dùng lại
3. Không đo được prompt nào hiệu quả
4. AI dễ viết sai giọng thương hiệu
5. AI dễ bịa giá, bịa chính sách nếu thiếu ngữ cảnh

Prompt Library giải quyết vấn đề này.

Hiểu đơn giản:

> **Prompt Library là “sổ tay câu lệnh chuẩn” để mọi người trong doanh nghiệp dùng AI theo cùng một quy trình.**

Giống như công thức món ăn:

- Đầu bếp giỏi có thể nấu theo cảm giác
- Nhưng nếu muốn mở chuỗi, phải có công thức chuẩn

Doanh nghiệp cũng vậy.

Nếu chủ doanh nghiệp dùng AI một mình thì hỏi ngẫu hứng vẫn được.  
Nhưng nếu muốn giao cho team marketing, sales, CSKH cùng dùng AI, thì phải có prompt chuẩn.

---

## 2. Hôm nay học viên cần tạo gì?

Hôm nay anh/chị cần tạo:

```text
[Tên DN] — Ngày 05 — Prompt Library v1
```

Trong đó có 4 phần chính:

1. Khối `[BỐI CẢNH DN]`
2. Khối `[GIỌNG]`
3. Prompt Library 50 prompt khung
4. Bảng test ít nhất 10 prompt

---

## 3. Prompt chuẩn gồm 6 phần

Từ hôm nay, mọi prompt quan trọng nên có cấu trúc:

```text
[VAI TRÒ]
AI đóng vai ai?

[BỐI CẢNH]
Doanh nghiệp là ai, bán gì, bán cho ai?

[NHIỆM VỤ]
AI cần làm việc gì?

[DỮ LIỆU ĐẦU VÀO]
Mình đưa cho AI dữ liệu gì?

[ĐỊNH DẠNG ĐẦU RA]
Muốn AI trả kết quả theo dạng nào?

[RÀNG BUỘC]
AI không được làm gì, phải giữ giọng gì, giới hạn gì?
```

Ví dụ prompt yếu:

```text
Viết cho tôi bài Facebook về trà thảo mộc.
```

Prompt chuẩn hơn:

```text
[VAI TRÒ]
Bạn là copywriter mạng xã hội cho thương hiệu dược liệu/trà thảo mộc Việt Nam.

[BỐI CẢNH]
Mẫu Sơn Xanh là doanh nghiệp trà thảo mộc và dược liệu vùng cao Mẫu Sơn, Lạng Sơn...

[NHIỆM VỤ]
Viết 1 bài Facebook giải thích vì sao trà thảo mộc Mẫu Sơn không nên so trực tiếp với trà phổ thông.

[DỮ LIỆU ĐẦU VÀO]
Sản phẩm: Trà Mẩy Gòm An Giấc
Giá: 359.000đ/hộp
Insight: khách sợ sản phẩm thảo mộc đắt nhưng không khác gì hàng phổ thông

[ĐỊNH DẠNG ĐẦU RA]
Bài 180–230 từ, xuống dòng thoáng, có CTA cuối bài.

[RÀNG BUỘC]
Không nói chữa mất ngủ, không cam kết hiệu quả 100%, không chê đối thủ.
```

Khác biệt rất lớn.

---

## 4. Hai khối quan trọng nhất hôm nay

### A. Khối `[BỐI CẢNH DN]`

Đây là phần tóm tắt doanh nghiệp để dán vào đầu mọi prompt.

Nó giúp AI biết:

- Doanh nghiệp là ai
- Bán gì
- Bán cho ai
- Giá/offer chính là gì
- Kênh bán hàng chính
- Khách sợ điều gì
- Điểm khác biệt là gì
- Điều gì không được hứa

Mẫu:

```text
[BỐI CẢNH DN]
Doanh nghiệp: [Tên DN], ngành [ngành], địa bàn [địa bàn], quy mô [quy mô].
Khách mục tiêu chính: [1–2 nhóm khách hàng quan trọng nhất].
Sản phẩm/offer chủ lực: [tên sản phẩm/gói], giá [giá], kết quả/kỳ vọng chính [kết quả].
Kênh bán/marketing chính: [Facebook/Zalo/TikTok/Website/Referral/Offline...].
Nỗi sợ/rào cản lớn nhất của khách: [fear/objection chính].
Điểm khác biệt: [USP quan trọng nhất].
Điều không bao giờ hứa/nói: [cam kết cấm, claim y tế/pháp lý, giá chưa xác nhận...].
```

### B. Khối `[GIỌNG]`

Đây là phần giúp AI viết đúng “chất” thương hiệu.

Mẫu:

```text
[GIỌNG]
Xưng hô: [em/anh/chị/mình...].
Tính cách giọng: [ấm áp/thẳng thắn/chuyên gia/gần gũi...].
Từ/cụm từ nên dùng: [5 cụm từ đặc trưng].
Điều cấm: [từ sáo rỗng, emoji quá nhiều, cam kết quá đà, chê bai đối thủ...].
```

Nếu không có khối `[GIỌNG]`, AI rất dễ viết kiểu chung chung:

> “Sản phẩm chất lượng cao, uy tín, giá tốt, được nhiều khách hàng tin dùng.”

Nghe rất AI và không có bản sắc.

---

## 5. Bài tập hôm nay

### Bài nộp cuối ngày

Anh/chị nộp file:

```text
[Tên DN] — Ngày 05 — Prompt Library v1
```

Ví dụ:

```text
Mẫu Sơn Xanh — Ngày 05 — Prompt Library v1
RocketAI Solutions — Ngày 05 — Prompt Library v1
An Nhiên Spa — Ngày 05 — Prompt Library v1
```

---

## 6. Output bắt buộc

### Output 1 — Khối `[BỐI CẢNH DN]`

Viết đúng 7 dòng theo mẫu.

Nguồn lấy dữ liệu:

- Ngày 01 — Business Snapshot
- Ngày 02 — Customer Avatar
- Ngày 03 — Offer
- Ngày 04 — Knowledge Base

Yêu cầu:

- Có số liệu thật nếu có
- Không viết chung chung
- Đọc vào phải trả lời được 3 câu:
  - Bán gì?
  - Cho ai?
  - Khác gì?

### Output 2 — Khối `[GIỌNG]`

Viết 4 dòng:

- Xưng hô
- Tính cách giọng
- Từ/cụm từ nên dùng
- Điều cấm

Nguồn lấy dữ liệu:

- Bài viết cũ
- Tin nhắn tư vấn cũ
- Brand Voice nếu đã có
- Cách chủ doanh nghiệp hay nói với khách

### Output 3 — Prompt Library 50 prompt

Không cần viết từ đầu.

Anh/chị dùng file template được phát:

```text
Template 5.1 — Prompt Library 50 Prompt Khung
```

Trong file này đã có sẵn 50 prompt chia thành 4 nhóm:

| Nhóm | Số prompt | Dùng cho |
|---|---:|---|
| Marketing | 15 | Content, ads, video, landing page, calendar |
| Sales | 15 | Tư vấn, xử lý từ chối, proposal, báo giá, follow-up |
| CSKH | 10 | FAQ, khiếu nại, chăm sóc, upsell, xin review |
| Quản trị/Ops | 10 | Báo cáo, SOP, kế hoạch tuần, phân tích số liệu |

Anh/chị chọn ít nhất **20 prompt quan trọng nhất** để cá nhân hóa trước.

### Output 4 — Cá nhân hóa ít nhất 20 prompt

Cá nhân hóa nghĩa là:

- Dán `[BỐI CẢNH DN]`
- Dán `[GIỌNG]`
- Điền các chỗ `{{...}}` bằng dữ liệu thật
- Thay ví dụ chung bằng sản phẩm/khách hàng/offer thật của doanh nghiệp

Không đạt nếu chỉ thay tên doanh nghiệp.

Ví dụ chưa đạt:

```text
Viết bài Facebook cho [Tên DN] về sản phẩm.
```

Ví dụ đạt:

```text
Viết bài Facebook cho Mẫu Sơn Xanh về Trà Mẩy Gòm An Giấc, giá 359.000đ/hộp, dành cho người muốn tạo thói quen thư giãn buổi tối, không hứa chữa mất ngủ.
```

### Output 5 — Test ít nhất 10 prompt

Chọn 10 prompt quan trọng nhất, chạy thật với dữ liệu doanh nghiệp mình.

Sau đó ghi vào bảng:

```markdown
| # | Mã prompt | Input đã dùng | Output dùng được ngay? | Cần sửa gì? | Trạng thái |
|---|---|---|:---:|---|---|
| 1 | M01 | ... | Có/Không | ... | Đạt/Chưa đạt |
```

Yêu cầu:

- Test ít nhất 10 prompt
- Nên phủ ít nhất 3 nhóm: Marketing, Sales, CSKH/Ops
- Prompt nào chưa đạt phải ghi rõ cần sửa gì
- Không được ghi “Đạt” hàng loạt cho có

Nhớ:

> **Prompt chưa test = chưa có.**

---

## 7. Hướng dẫn làm trong 90–120 phút

### Bước 1 — Mở tài liệu

Mở 2 file:

```text
Template 5.1 — Prompt Library 50 Prompt Khung
Template 5.1A — Bản Mẫu MSX Prompt Library v1
```

File 5.1 là bản khung.  
File 5.1A là bản Mẫu Sơn Xanh đã điền mẫu để xem cách làm.

### Bước 2 — Tạo bản của doanh nghiệp mình

Copy template thành:

```text
[Tên DN] — Ngày 05 — Prompt Library v1
```

### Bước 3 — Điền `[BỐI CẢNH DN]`

Dùng dữ liệu từ bài Ngày 1–4.

Nếu chưa biết viết, dùng prompt này:

```text
Bạn là chuyên gia prompt cho SME.

Tôi sẽ dán dữ liệu Ngày 1–4 của doanh nghiệp. Hãy giúp tôi chưng cất thành khối [BỐI CẢNH DN] đúng 7 dòng.

Yêu cầu:
1. Chỉ dùng dữ liệu tôi cung cấp.
2. Có con số cụ thể nếu có.
3. Không viết quảng cáo chung chung.
4. Đọc vào phải trả lời được: bán gì, cho ai, khác gì.
5. Dòng cuối ghi rõ điều không bao giờ được hứa/nói.

Dữ liệu:
[ Dán Business Snapshot + Customer Avatar + Offer + Knowledge Base ]
```

### Bước 4 — Điền `[GIỌNG]`

Dùng prompt:

```text
Bạn là chuyên gia phân tích giọng thương hiệu.

Từ các mẫu nội dung/tin nhắn dưới đây, hãy tạo khối [GIỌNG] 4 dòng:
1. Xưng hô với khách
2. Tính cách giọng
3. 5 từ/cụm từ nên dùng
4. Điều cấm khi viết

Không phán chung chung. Nếu nói “ấm áp” hoặc “chuyên gia”, hãy chỉ rõ thể hiện qua cách viết nào.

Mẫu nội dung:
[ Dán 3–5 bài viết/tin nhắn cũ mà tôi thấy đúng giọng ]
```

### Bước 5 — Chọn 20 prompt cần dùng nhất

Gợi ý chọn:

| Nhóm | Số lượng nên chọn |
|---|---:|
| Marketing | 7 |
| Sales | 6 |
| CSKH | 4 |
| Quản trị/Ops | 3 |

Tổng: 20 prompt.

Nếu doanh nghiệp đang cần content mạnh, chọn nhiều Marketing hơn.  
Nếu đang thiếu sales, chọn nhiều Sales hơn.

### Bước 6 — Test 10 prompt

Chọn 10 prompt quan trọng nhất và chạy thử thật.

Gợi ý test:

| Nhóm | Prompt nên test |
|---|---|
| Marketing | M01, M04, M07 |
| Sales | S01, S03, S06 |
| CSKH | CS01, CS03 |
| Ops | OPS01, OPS05 |

---

## 8. Tiêu chí đạt bài hôm nay

Bài đạt khi có:

- File đúng tên
- Có `[BỐI CẢNH DN]` 7 dòng
- Có `[GIỌNG]` 4 dòng
- Có đủ 50 prompt khung
- Có ít nhất 20 prompt đã cá nhân hóa
- Có ít nhất 10 prompt đã test
- Prompt test phủ ít nhất 3 nhóm
- Có ghi rõ prompt nào đạt/chưa đạt/cần sửa gì

---

## 9. Lỗi thường gặp cần tránh

### Lỗi 1 — Chỉ thay tên doanh nghiệp

Không đạt.

Prompt phải có dữ liệu thật:

- Sản phẩm
- Giá
- Khách hàng
- Offer
- Objection
- Giọng thương hiệu
- Điều cấm

### Lỗi 2 — Khối `[BỐI CẢNH DN]` dài cả trang

Không đạt.

Khối này phải ngắn, nén, dùng lại được.

Mục tiêu:

> AI đọc 7 dòng là hiểu doanh nghiệp trong 10 giây.

### Lỗi 3 — Prompt không có ràng buộc

Nếu không có constraint, AI dễ viết sai.

Ví dụ ngành sức khỏe/làm đẹp/dược liệu phải có ràng buộc:

```text
Không hứa chữa bệnh.
Không cam kết 100%.
Không bịa chứng nhận.
Không dùng claim y tế nếu chưa có dữ liệu.
```

### Lỗi 4 — Không test prompt

Không chạy thử thì không biết prompt dùng được hay không.

Prompt Library chỉ có giá trị khi đã test với dữ liệu thật.

### Lỗi 5 — Test toàn Marketing

Nên test đủ ít nhất 3 nhóm:

- Marketing
- Sales
- CSKH hoặc Ops

Vì sau này AIOS không chỉ viết content, mà còn hỗ trợ bán hàng và vận hành.

---

## 10. Tài liệu đi kèm hôm nay

Anh/chị dùng 2 tài liệu chính:

### Tài liệu 1 — Bản khung

```text
Template 5.1 — Prompt Library 50 Prompt Khung
```

Dùng để copy và làm bài của doanh nghiệp mình.

### Tài liệu 2 — Bản mẫu thực tế

```text
Template 5.1A — Bản Mẫu MSX Prompt Library v1
```

Đây là bản Mẫu Sơn Xanh đã điền mẫu, gồm:

- `[BỐI CẢNH DN]` đã điền
- `[GIỌNG]` đã điền
- 20 prompt đã cá nhân hóa
- 10 prompt đã test mẫu
- 4 prompt mẫu viết đầy đủ

Hãy mở bản MSX trước nếu chưa biết làm thế nào.

---

## 11. Bài nộp

Nộp vào thread Ngày 05:

```text
[Tên DN] — Ngày 05 — Prompt Library v1
```

Kèm:

1. Link file Prompt Library
2. Ảnh chụp hoặc trích 2 khối:
   - `[BỐI CẢNH DN]`
   - `[GIỌNG]`
3. Danh sách 20 prompt đã cá nhân hóa
4. Bảng 10 prompt đã test

---

## 12. Deadline

**Deadline:** 23:59 hôm nay.

---

## 13. Câu chốt hôm nay

> **Ngày 4 xây bộ não dữ liệu cho AI.  
> Ngày 5 tạo bộ câu lệnh chuẩn để AI dùng bộ não đó làm việc.**

Từ hôm nay, đừng hỏi AI ngẫu hứng nữa.

Hãy bắt đầu xây **Prompt Library** như một tài sản vận hành của doanh nghiệp.
