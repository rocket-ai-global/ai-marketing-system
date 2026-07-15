---
up:
  - "[[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]]"
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-12
tags: [project, aios, bai-tap]
week: 1
day: 5
---

# 📋 Bài Tập Ngày 5 — Hệ Thống Prompt & Template

> **Triết lý hôm nay: 50 prompt khung được PHÁT SẴN — bạn KHÔNG viết prompt nào từ đầu.** Việc của bạn chỉ có 3 nhịp: chế tạo 2 khối ngữ cảnh → "đóng dấu" 2 khối vào 20 prompt → test 10 prompt. Bản mẫu hoàn chỉnh của học viên thật để đối chiếu: [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]].

---

## 1. 🎯 Hôm nay bạn tạo ra gì

**Core Output (bắt buộc — điều kiện qua ngày):**

| # | Tài sản | Chuẩn nghiệm thu |
|---|---------|------------------|
| 1 | **Prompt Library v1 (thư viện câu lệnh phiên bản 1)** | ≥50 prompt trên file quản lý **7 cột**: Mã \| Tên prompt \| Nhóm (M/S/CS/OPS) \| Dùng khi nào \| Prompt đầy đủ \| Trạng thái test \| Ghi chú kết quả — trong đó **≥20 prompt đã cá nhân hoá** cho DN bạn (đã dán 2 khối + điền dữ liệu thật) |
| 2 | **10 prompt đã test** | Chạy thật từng cái, chấm Đạt/Chưa đạt, **ghi 1 dòng kết quả mỗi prompt**, phủ ≥3 nhóm |
| 3 | **2 khối ngữ cảnh chuẩn** | `[BỐI CẢNH DN]` 7 dòng ≤130 từ + `[GIỌNG]` 4 dòng ≤80 từ — đặt ở đầu file thư viện |

**Bonus Output (không bắt buộc, không trừ điểm):**
- ⭐ Prompt Usage Guide (hướng dẫn dùng prompt) 1 trang — khung: [[Template 5.3 — Prompt Usage Guide]]
- ⭐ Cá nhân hoá nốt 30 prompt còn lại
- ⭐ Tự tạo 3-5 prompt cho tình huống đặc thù DN bạn (dùng Prompt 5 "prompt sinh prompt" trong giáo án, mục 8)

---

## 2. 📥 Chuẩn bị

**Input từ các ngày trước (mở sẵn 4 tài liệu — đây là nguyên liệu của 2 khối ngữ cảnh):**

| Tài liệu | Từ ngày | Dùng cho |
|----------|:---:|----------|
| Business Snapshot (trong file 5 phần) | 01 | Dòng 1, 3, 4 khối `[BỐI CẢNH DN]` |
| Customer Avatar + PDFO Map (bản đồ Pain–Desire–Fear–Objection) | 02 | Dòng 2, 5 khối `[BỐI CẢNH DN]` + input test S03 |
| Core Offer Document | 03 | Dòng 3, 6, 7 khối `[BỐI CẢNH DN]` |
| Đặc tả giọng thương hiệu (Bonus Ngày 04 — chưa có thì dùng Prompt B bên dưới) | 04 | Khối `[GIỌNG]` |

**Template cần mở (wikilink):**
- [[Template 5.1 — Prompt Library 50 Prompt Khung]] — file bạn copy và làm trực tiếp trên đó
- [[Template 5.2 — Khối Ngữ Cảnh Chuẩn]] — khung 2 khối + 2 bản điền mẫu RocketAI & MSX
- [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]] — "đáp án mẫu" để đối chiếu TRƯỚC KHI nộp

**Track công cụ (bạn thuộc track nào thì test trên nhánh đó, KHÔNG làm cả 3):**

| Track | Test prompt ở đâu |
|-------|-------------------|
| **A — RocketAgent** (mặc định) | Chạy prompt trong Assistant — KB đã nạp Ngày 04 |
| **B — Claude/ChatGPT Projects** | Chạy trong Project đã upload 3 tài liệu lõi Ngày 04 |
| **C — Hermes/Jarvis** (Hermes là agent AI của Rocket vận hành qua Telegram — gói OS Installed hoặc Bonus) | Nhắn prompt trực tiếp cho Hermes — xem [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]] |

**Trong Vault SME:** lưu bản Prompt Library của bạn vào `04. Resources/Prompt Library/`.

---

## 3. ✅ Các bước

> ⏱ Mỗi cụm ghi 2 số: **dùng template điền sẵn / lần đầu tự làm**. Tổng: **110' theo template · lần đầu có thể tới ~2h30**. Quá giờ → làm theo thứ tự A→D; Bonus bỏ qua được, không trừ điểm.

### Cụm A — Chế tạo 2 khối ngữ cảnh (⏱ dùng template: 20' · lần đầu: 30')

**1.** [ ] Chạy **Prompt A** — dán Snapshot + Avatar + Offer của bạn vào chỗ `{{}}` → nhận khối `[BỐI CẢNH DN]` 7 dòng (10')

```
[VAI TRÒ] Bạn là chuyên gia tối ưu câu lệnh AI (prompt engineer) cho SME, giỏi nén thông tin doanh nghiệp thành khối ngữ cảnh ngắn mà đủ.

[BỐI CẢNH] Tôi sẽ dán khối ngữ cảnh này vào đầu MỌI câu lệnh AI của doanh nghiệp từ nay về sau, nên nó phải chứa đúng những thông tin giúp AI tạo nội dung chính xác, đúng khách hàng, đúng offer và an toàn pháp lý.

[NHIỆM VỤ] Từ 3 tài liệu dưới đây, viết khối [BỐI CẢNH DN] đúng 7 dòng: (1) DN là ai, ở đâu, quy mô; (2) khách mục tiêu — 1 dòng nén từ avatar; (3) sản phẩm chủ lực + giá + cam kết chính; (4) kênh bán & marketing chính; (5) nỗi sợ/rào cản lớn nhất của khách; (6) điểm khác biệt (USP) quan trọng nhất; (7) điều KHÔNG BAO GIỜ hứa/nói. Sau đó tự kiểm: đọc khối này có tự trả lời được 3 câu "bán gì – cho ai – khác gì" trong 10 giây không; nếu không, viết lại.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán}}. Customer Avatar (bản rút gọn): {{dán}}. Core Offer Document: {{dán phần chính}}.

[ĐỊNH DẠNG ĐẦU RA] Một khối văn bản 7 dòng liền mạch bắt đầu bằng nhãn "[BỐI CẢNH DN]", không gạch đầu dòng, ≤130 từ — để dán gọn vào prompt khác.

[RÀNG BUỘC] Chỉ dùng dữ kiện có trong 3 tài liệu. Ưu tiên con số (giá, thời hạn, quy mô). Không tính từ quảng cáo. Tiếng Việt.
```

**2.** [ ] Chạy **Prompt B** — dán 3-5 mẫu văn bản bạn tự viết → nhận khối `[GIỌNG]` 4 dòng (đã có bản Ngày 04 thì rút từ đó, bỏ qua prompt này) (7')

```
[VAI TRÒ] Bạn là chuyên gia phân tích văn phong thương hiệu.

[BỐI CẢNH] Tôi cần khối [GIỌNG] 4 dòng để dán vào mọi câu lệnh AI, giúp mọi nội dung ra đúng "chất" của tôi thay vì giọng AI mặc định.

[NHIỆM VỤ] Phân tích các mẫu văn bản tôi tự viết dưới đây và nén thành khối [GIỌNG] đúng 4 dòng: (1) xưng hô với khách; (2) 2-3 đặc điểm giọng nổi bật nhất (kèm 1 ví dụ trích nguyên văn); (3) 5 từ/cụm từ đặc trưng nên dùng; (4) 3-5 điều cấm (từ sáo rỗng, kiểu câu, mức emoji). Nếu mẫu quá ít để kết luận, hỏi tôi 3 câu về sở thích văn phong rồi mới viết.

[DỮ LIỆU ĐẦU VÀO] 3-5 mẫu tôi tự viết (caption, tin nhắn tư vấn tôi ưng ý): {{dán nguyên văn}}.

[ĐỊNH DẠNG ĐẦU RA] Khối 4 dòng bắt đầu bằng nhãn "[GIỌNG]", ≤80 từ.

[RÀNG BUỘC] Đặc điểm phải có bằng chứng từ mẫu, không phán chung chung ("thân thiện, chuyên nghiệp"). Tiếng Việt.
```

**3.** [ ] Đọc to 2 khối — chỗ nào sai thực tế thì sửa tay. Tự kiểm 10 giây: đọc khối có trả lời được "bán gì – cho ai – khác gì" không? Đối chiếu 2 bản mẫu trong [[Template 5.2 — Khối Ngữ Cảnh Chuẩn]] (3')

### Cụm B — "Đóng dấu" 2 khối vào 20 prompt (⏱ dùng template: 45' · lần đầu: 60')

**4.** [ ] Copy [[Template 5.1 — Prompt Library 50 Prompt Khung]] thành file mới: `[Tên DN] — Ngày 05 — Prompt Library v1`; dán 2 khối vào phần đầu file (2')
**5.** [ ] Chọn 20 prompt bạn sẽ dùng nhiều nhất trong 2 tuần tới — gợi ý phân bổ: 7 Marketing + 6 Sales + 4 CSKH + 3 OPS (8')
**6.** [ ] Với từng prompt đã chọn: dán khối vào chỗ `{{[BỐI CẢNH DN]}}` và `{{[GIỌNG]}}`, điền các chỗ `{{...}}` còn lại bằng dữ liệu thật của DN (35')

> 💡 **Mẹo giảm tải:** viết 2 khối MỘT lần → nhân bản hàng loạt. Copy 2 khối, tìm mọi chỗ `{{[BỐI CẢNH DN]}}`/`{{[GIỌNG]}}` và dán đè — tuyệt đối không viết lại bối cảnh cho từng prompt. Đây là lý do 20 prompt chỉ mất 45 phút.

### Cụm C — Test 10 prompt (⏱ dùng template: 35' · lần đầu: 45')

**7.** [ ] Chọn 10/20 prompt quan trọng nhất — **phủ ≥3 nhóm** — chạy thật từng cái với dữ liệu thật, trên track công cụ của bạn (25')
**8.** [ ] Chấm Đạt/Chưa đạt theo 2 câu hỏi: *dùng được ngay không? cần sửa tay bao nhiêu %?* → ghi 1 dòng kết quả vào cột test (xem 10 dòng test mẫu trong [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]]) (5')
**9.** [ ] Prompt Chưa đạt → sửa theo **quy tắc chẩn đoán** rồi chạy lại 1 lần, ghi chú "đã sửa gì" (5'):

| Triệu chứng output | Sửa ở phần nào |
|--------------------|----------------|
| Sai **KIỂU** (dài quá, sai format, sai bố cục) | **Output / Constraint** |
| Sai **NỘI DUNG** (sai giá, sai dữ kiện, lạc khách hàng) | **Context / Input** |
| **NÔNG** (đúng nhưng chung chung, thiếu chuyên môn) | **Role / Task** |

### Cụm D — Nộp bài (⏱ 10')

**10.** [ ] Tự chấm theo mục 5 bên dưới → đối chiếu lần cuối với [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]] → nộp link vào thread cohort trước 23h59

---

## 4. 📤 Nộp bài

- **Deliverable:** link file Prompt Library v1 (Google Sheets/Notion/Markdown — quyền xem "Anyone with the link")
- **Tên file chuẩn:** `[Tên DN] — Ngày 05 — Prompt Library v1` · Ví dụ: `MSX Group — Ngày 05 — Prompt Library v1`
- **Nơi nộp:** thread cohort Ngày 05
- **Deadline: 23h59 cùng ngày.** AI Grader chấm trong 1h sáng hôm sau; bài 🔧/🔴 được mentor chấm sâu.

---

## 5. 🔍 Tự chấm nhanh (trước khi nộp — theo rubric giáo án)

| # | Tiêu chí | Đạt? |
|---|----------|:---:|
| 1 | File đủ **50 prompt**, đủ **7 cột** quản lý? |  |
| 2 | **≥20 prompt** đã dán 2 khối + điền hết dữ liệu? **Kiểm bằng Ctrl+F ký tự `{{`** trong 20 prompt đã khai cá nhân hoá — còn sót `{{` = chưa đạt (mentor kiểm đúng cách này, −10đ) |  |
| 3 | `[BỐI CẢNH DN]` đúng 7 dòng, ≤130 từ, chứa **≥4 con số thật** khớp tài liệu Ngày 1-4? |  |
| 4 | `[GIỌNG]` 4 dòng, ≤80 từ, đặc điểm có ví dụ trích từ văn bản thật của bạn? |  |
| 5 | **≥10 prompt** có trạng thái test + 1 dòng kết quả riêng (không ghi "Đạt" suông)? |  |
| 6 | Test phủ **≥3 nhóm** (không dồn 10 cái vào 1 nhóm)? |  |
| 7 | **≥1 prompt Chưa đạt** đã sửa theo quy tắc chẩn đoán → chạy lại thành Đạt, có ghi "đã sửa gì"? |  |
| 8 | Constraint an toàn còn NGUYÊN (không xoá khi cá nhân hoá) · tên file đúng chuẩn · quyền xem đã mở? |  |

> Đủ 8/8 → thường đạt ⭐ (≥80đ). Thiếu tiêu chí nào → sửa ngay trước khi nộp, đừng nộp bài 🔧.

---

## 6. ⚠️ Lỗi thường gặp (từ giáo án mục 10-11)

| ❌ Lỗi | Hậu quả | ✅ Cách sửa |
|--------|---------|------------|
| "Cá nhân hoá" chỉ bằng thay tên DN, khối bối cảnh vẫn chung chung không số liệu | −10đ | Khối phải chứa ≥4 con số thật (giá, quy mô, thời hạn); đọc vào thấy ngay bán gì – cho ai – khác gì |
| Test khống: cột test ghi "Đạt" hàng loạt, không có ghi chú kết quả | −10đ | Mỗi prompt test = 1 dòng kết quả riêng (input gì, output ra sao, cần sửa gì) — xem bảng mẫu 5.1A |
| Xoá/sửa Constraint an toàn (quảng cáo y tế, cam kết) khi cá nhân hoá | −10đ + bắt buộc khôi phục | Constraint an toàn là phần CẤM SỬA — chỉ được điền chỗ trống |
| Khối `[BỐI CẢNH DN]` dài cả trang (nhồi nguyên Snapshot) | −5đ | Chưng cất đúng 7 dòng ≤130 từ — Prompt A đã ép chuẩn này, đừng tự nối thêm |
| Điền `{{}}` mơ hồ (`{{chủ đề}}` = "viết về AI") | Output lan man, nhạt | Mỗi `{{}}` trả lời 1 câu hỏi cụ thể ("vì sao chủ spa làm content 4h/ngày mà khách vẫn không đến") |
| Nhồi 3 nhiệm vụ vào 1 prompt | Cả 3 đều nửa vời | 1 prompt = 1 sản phẩm đầu ra; chuỗi việc thì chạy lần lượt, output cái trước làm Input cái sau |

---

## 7. 🔗 Kết nối

- **2 khối ngữ cảnh** → lõi của Instruction Document Ngày 06 (viết instruction nhanh gấp đôi) + system prompt chatbot Tuần 3
- **Prompt Library v1** → các Assistant Ngày 06 chính là các cụm prompt này "cài cứng" vào vai; Tuần 2 dùng nhóm M hằng ngày; Tuần 3 nhóm S; Tuần 4 nhóm CS + OPS
- **Kết quả test 10 prompt** → Improvement List đầu vào cho Ngày 06
- **Usage Guide (Bonus)** → tài liệu đào tạo nhân viên trong bộ chuyển giao Ngày 28; bảo trì thư viện mỗi chiều thứ Sáu theo SOP-05 (giáo án mục 9)
- Giáo án: [[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]] · Template: [[Template 5.1 — Prompt Library 50 Prompt Khung]] · [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]] · [[Template 5.2 — Khối Ngữ Cảnh Chuẩn]] · [[Template 5.3 — Prompt Usage Guide]]
