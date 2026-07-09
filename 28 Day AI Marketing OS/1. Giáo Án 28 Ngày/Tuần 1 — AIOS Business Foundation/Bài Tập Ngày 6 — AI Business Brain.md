---
created: 2026-07-09
tags: [project, aios, assignment, day6]
up:
  - "[[_MOC 28 Day AIOS]]"
---

# 📋 Bài Tập Ngày 6 — AI BUSINESS BRAIN

> **Mục tiêu:** Biến Knowledge Base (Ngày 4) + Prompt Library (Ngày 5) thành "bộ não AI" hiểu doanh nghiệp, trả lời như 1 nhân viên thực thụ. Đây là nền tảng để tạo AI Agent ở các tuần sau.

---

## 📝 BÀI NỘP (4 output — nộp trước 22:00)

### Output 1: AI Instruction Document

```markdown
## AI Identity
- **Tên AI:** 
- **Vai trò:** (VD: Trợ lý Marketing cho Spa ABC)
- **Doanh nghiệp:** 
- **Ngành:** 

## AI Rules
- **AI ĐƯỢC PHÉP:**
  1. 
  2. 
  3. 
- **AI KHÔNG ĐƯỢC PHÉP:**
  1. 
  2. 
  3. 

## Voice & Tone
- **Giọng văn:** (thân thiện / chuyên nghiệp / trẻ trung...)
- **Xưng hô:** (anh/chị/em với khách hàng)
- **Độ dài:** (ngắn gọn ≤3 câu / chi tiết)
- **Ngôn ngữ:** (tiếng Việt, có emoji, không dùng từ kỹ thuật...)

## Data Sources
- Sản phẩm: → link đến Product Knowledge
- Khách hàng: → link đến Customer Avatar
- FAQ: → link đến FAQ Database
- Sales: → link đến Sales Knowledge Base
```

### Output 2: 5 AI Assistants

Tạo 5 AI Agent, mỗi agent có:

```markdown
## 1. AI Marketing Assistant
- **Nhiệm vụ:** Viết content, tạo ý tưởng, lên lịch đăng bài
- **Prompt khởi tạo:** 
- **Test:** "Viết 1 bài Facebook về [sản phẩm] cho [đối tượng]"
- **Kết quả test:** (copy output)

## 2. AI Sales Assistant
- **Nhiệm vụ:** Tư vấn KH, xử lý phản đối, tạo báo giá
- **Prompt khởi tạo:** 
- **Test:** "KH nói 'Đắt quá, thôi em không lấy đâu' — trả lời sao?"
- **Kết quả test:** 

## 3. AI Content Assistant
- **Nhiệm vụ:** Viết kịch bản video, caption, email
- **Prompt khởi tạo:** 
- **Test:** "Viết kịch bản video 30s về [sản phẩm]"
- **Kết quả test:** 

## 4. AI Customer Service Assistant
- **Nhiệm vụ:** Trả lời FAQ, xử lý khiếu nại, chăm sóc KH
- **Prompt khởi tạo:** 
- **Test:** "KH hỏi 'Bảo hành thế nào?'"
- **Kết quả test:** 

## 5. AI Strategy Assistant
- **Nhiệm vụ:** Phân tích dữ liệu, gợi ý chiến lược, báo cáo
- **Prompt khởi tạo:** 
- **Test:** "Phân tích dữ liệu bán hàng tháng này và gợi ý tháng sau"
- **Kết quả test:** 
```

### Output 3: Test Case Report

Test AI với 5 tình huống thực tế:

| # | Tình huống | AI trả lời | Đúng/Sai? | Cần sửa gì? |
|---|-----------|-----------|:---:|-----------|
| 1 | KH hỏi giá sản phẩm | | | |
| 2 | KH hỏi so sánh với đối thủ | | | |
| 3 | KH từ chối vì đắt | | | |
| 4 | KH chưa hiểu sản phẩm | | | |
| 5 | Nhân viên cần viết bài FB | | | |

### Output 4: Improvement List

```markdown
## Dữ liệu cần bổ sung
1. 
2. 
3. 

## Câu trả lời cần sửa
1. Câu hỏi:  | AI trả lời sai:  | Sửa thành: 
2. ...

## Prompt cần tinh chỉnh
1. 
2. 

## Tính năng cần thêm
1. 
2. 
```

---

## ⚡ HƯỚNG DẪN NHANH (100 phút)

| Bước | Làm gì | Mất |
|:---:|--------|:---:|
| 1 | Viết AI Instruction (identity, rules, voice) | 15' |
| 2 | Tạo AI Marketing Assistant + test | 15' |
| 3 | Tạo AI Sales Assistant + test | 15' |
| 4 | Tạo AI Content + CS + Strategy Assistants + test | 25' |
| 5 | Chạy 5 test case → điền Test Case Report | 15' |
| 6 | Lập Improvement List | 15' |

---

## 🎯 TIÊU CHÍ ĐẠT

| Tiêu chí | Yêu cầu |
|----------|---------|
| AI Identity | Đủ role, rules, voice, data sources |
| 5 AI Assistants | Mỗi agent có prompt khởi tạo + 1 test |
| Test Cases | Đủ 5 tình huống → có đánh giá đúng/sai |
| Improvement | Liệt kê ≥3 việc cần cải thiện |
