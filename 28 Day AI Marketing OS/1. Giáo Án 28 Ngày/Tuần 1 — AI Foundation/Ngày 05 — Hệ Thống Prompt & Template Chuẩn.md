---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 1
day: 5
core-output: "Prompt Library v1 ≥50 prompt (≥20 đã cá nhân hóa) · 10 prompt đã test có ghi kết quả · Khối ngữ cảnh chuẩn [BỐI CẢNH DN] + [GIỌNG]"
---

# Ngày 05 — Hệ Thống Prompt & Template Chuẩn

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes — Hermes là agent AI của Rocket vận hành qua Telegram, dành cho gói OS Installed). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Nạp bộ 50 prompt khung ([[Template 5.1 — Prompt Library 50 Prompt Khung]]) vào `04. Resources/Prompt Library/` — học viên chỉ thay ~20% dữ liệu DN mình, không viết prompt từ đầu. Bản mẫu đã điền hoàn chỉnh của học viên thật để đối chiếu: [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]].

> Hôm nay bạn xây "tủ công cụ câu lệnh": một Prompt Library (thư viện câu lệnh) ≥50 prompt chuẩn hóa theo khung Role–Context–Task–Input–Output–Constraint, để bạn và nhân viên dùng AI nhất quán như dùng quy trình — hết cảnh mỗi lần hỏi AI một kiểu, ra kết quả một kiểu.

## 1. 🎯 Mục Tiêu Ngày Học

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Prompt Library v1 (thư viện câu lệnh phiên bản 1)** — ≥50 prompt trên file quản lý chuẩn (bộ 50 prompt khung được PHÁT SẴN — học viên không viết từ số 0), trong đó **≥20 prompt đã cá nhân hóa** cho DN mình (gắn khối bối cảnh + giọng + dữ liệu thật).
- ✅ **10 prompt đã test** — chạy thật, chấm Đạt/Chưa đạt, ghi 1 dòng kết quả mỗi prompt.
- ✅ **Khối ngữ cảnh chuẩn** — 2 đoạn văn bản tái sử dụng: `[BỐI CẢNH DN]` và `[GIỌNG]` — dán vào đầu mọi prompt về sau.

**Bonus Output (nâng cao):**
- ⭐ **Prompt Usage Guide (hướng dẫn dùng prompt)** — 1 trang quy ước cho nhân viên: dùng prompt nào khi nào, được sửa gì, cấm gì (khung: [[Template 5.3 — Prompt Usage Guide]]).
- ⭐ Cá nhân hoá nốt 30 prompt còn lại; tạo 3-5 prompt riêng cho tình huống đặc thù của DN.

**Track công cụ (theo [[_Chuẩn Đồng Bộ Tuần 1]] — bạn thuộc track nào thì test prompt trên nhánh đó, KHÔNG làm cả 3):**

| Track | Bạn là ai | Test prompt ở đâu |
|---|---|---|
| **A — RocketAgent** (mặc định) | Được cấp tài khoản RocketAgent | Chạy prompt trong Assistant — KB đã nạp Ngày 04 |
| **B — Claude/ChatGPT Projects** | Chưa có tài khoản RocketAgent | Chạy trong Project đã upload 3 tài liệu lõi Ngày 04 |
| **C — Hermes/Jarvis qua Telegram** | Gói OS Installed (Rocket cài sẵn) hoặc Bonus | Nhắn prompt trực tiếp cho Hermes — xem [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]] |

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Vì sao phải CHUẨN HÓA prompt (5')
- **Ý chính:** Hỏi AI ngẫu hứng = mỗi lần một kết quả, không giao được cho nhân viên, không cải tiến được. Prompt chuẩn hóa = quy trình làm việc: cùng đầu vào → cùng chất lượng đầu ra, ai chạy cũng được, hỏng thì biết sửa ở dòng nào.
- **Cách giảng:** Analogy công thức món ăn: "Đầu bếp giỏi nấu ngon không cần công thức — nhưng CHUỖI nhà hàng cần công thức để 100 quán vị như nhau. Anh chị đang xây chuỗi, không phải nấu ăn tài tử." Demo đối chứng 60 giây: "viết bài về AI cho spa" (prompt 1 dòng) vs prompt chuẩn đủ 6 phần — chiếu 2 output cạnh nhau.
- **Ví dụ RocketAI:** Trước khi chuẩn hoá, Tony viết content tuyển học viên bằng cách chat ngẫu hứng với AI — mỗi lần mô tả lại RocketAI từ đầu, bài lúc hay lúc dở. Sau khi có thư viện: mở thư viện → chọn M01 → điền 2 chỗ trống → 3 phút có bài đúng giọng thực chiến.

### Khối 2 — Giải phẫu khung Role–Context–Task–Input–Output–Constraint (8')
- **Ý chính:** 6 phần của một prompt chuẩn: **Role (vai trò)** — AI đóng vai ai (chuyên gia gì, cho ngành nào); **Context (bối cảnh)** — DN nào, khách nào, đang ở tình huống gì; **Task (nhiệm vụ)** — làm gì, các bước; **Input (dữ liệu đầu vào)** — chỗ `{{điền}}` dữ liệu thật; **Output (định dạng đầu ra)** — bảng/script/độ dài/cấu trúc; **Constraint (ràng buộc)** — cấm gì, giọng gì, giới hạn gì.
- **Cách giảng:** Học viên đã DÙNG khung này 4 ngày nay (mọi prompt Ngày 1-4 đều 6 phần) — hôm nay mới gọi tên và tự viết. Quy tắc sửa prompt: output sai KIỂU → sửa Output/Constraint; output sai NỘI DUNG → sửa Context/Input; output nông → sửa Role/Task.
- **Ví dụ RocketAI:** Mổ xẻ prompt M01 "viết bài Facebook" trên slide: tô màu 6 phần, chỉ ra nếu xoá Constraint "không hứa con số doanh thu/lead" thì bài tuyển học viên biến thành bài hứa hươu — mất uy tín ngay. Với học viên ngách spa/nha khoa, Constraint tương đương là "không hứa kết quả y khoa" (xoá là vi phạm quảng cáo).

### Khối 3 — Khối ngữ cảnh tái sử dụng: [BỐI CẢNH DN] và [GIỌNG] (7')
- **Ý chính:** 80% phần Context và Constraint giống nhau ở mọi prompt → tách thành 2 khối văn bản chuẩn, viết MỘT lần, dán vào MỌI prompt: `[BỐI CẢNH DN]` = 5-7 dòng chưng cất từ Snapshot + Avatar + Offer (Ngày 1-3); `[GIỌNG]` = 4-5 dòng từ đặc tả giọng thương hiệu (Ngày 04). Đây là "con dấu" của DN đóng lên mọi câu lệnh.
- **Cách giảng:** Đây chính là bí quyết làm 50 prompt trong 1 buổi tối: bộ khung đã phát sẵn, học viên chỉ chế tạo 2 khối này rồi "đóng dấu" hàng loạt.
- **Ví dụ RocketAI:** Khối `[BỐI CẢNH DN]` của RocketAI (chiếu nguyên văn — xem mục 4, Bước 1); bản B2C tương ứng của MSX xem [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]].

### Khối 4 — Tổ chức thư viện & quy trình test (5')
- **Ý chính:** Thư viện quản lý trên 1 file bảng (Google Sheets/Notion) 7 cột: Mã | Tên prompt | Nhóm (M/S/CS/OPS) | Dùng khi nào | Prompt đầy đủ | Trạng thái test | Ghi chú kết quả. Đánh mã theo phòng ban: M01-M15 (Marketing), S01-S15 (Sales), CS01-CS10 (chăm sóc khách hàng), OPS01-OPS10 (vận hành/quản trị). Quy trình test 3 bước: chạy với dữ liệu thật → chấm Đạt/Chưa đạt theo 2 câu hỏi ("dùng được ngay không? cần sửa tay bao nhiêu %?") → ghi 1 dòng kết quả.
- **Cách giảng:** "Prompt chưa test = chưa có. Giống SOP chưa ai làm thử — chỉ là giấy."

> **Thích ứng ngành khác:** Bộ 50 prompt khung dùng chung cho mọi ngành — chỉ khối `[BỐI CẢNH DN]` và `[GIỌNG]` là khác nhau. Spa/thẩm mỹ & nha khoa: thêm Constraint pháp lý quảng cáo y tế vào MỌI prompt marketing (chính là ngách của khách hàng RocketAI — chị Mai, chủ Spa ABC — nên demo hôm nay vẫn "chạm" bạn); Giáo dục: thêm ràng buộc "người đọc là phụ huynh, không phải học viên"; B2C sản phẩm: đối chiếu trọn bộ bản mẫu MSX ([[Template 5.1A — Bản Mẫu MSX Prompt Library v1]]); Coaching/B2B dịch vụ: đổi các prompt "đặt lịch soi da" thành "đặt lịch demo/discovery call (buổi gọi tìm hiểu)".

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 04 | Chiếu 1 KB tốt (FAQ từ inbox thật, có mục từ chối khéo) + lỗi "2 giá trong 2 tài liệu". Hỏi nhanh: "Ai đã test 3 câu khám sức khỏe? AI trả lời sai chỗ nào?" |
| 25' | Giảng kiến thức trọng tâm | 4 khối mục 2. Trọng tâm: Khối 2 (giải phẫu 6 phần) + Khối 3 (khối ngữ cảnh). |
| 30' | Demo thực hành live | Chế tạo 2 khối ngữ cảnh RocketAI → đóng dấu vào 3 prompt khung → test → sửa 1 prompt bị lỗi (kịch bản mục 4). |
| 15' | Học viên làm tại chỗ + Q&A | Học viên viết nháp khối `[BỐI CẢNH DN]` của mình (chạy Prompt 1), dán bản nháp vào chat cho trainer nhận xét nhanh 3-4 bản. |
| 10' | Giao bài tập | Chiếu deliverable + rubric. Nhấn mạnh: KHÔNG viết 50 prompt từ đầu — bộ khung đã phát, việc của bạn là cá nhân hóa 20 + test 10. |

**Checklist chuẩn bị của trainer:** file "Prompt Library — 50 Prompt Khung" ([[Template 5.1 — Prompt Library 50 Prompt Khung]] — bản phát học viên, cột prompt đầy đủ, cột cá nhân hoá trống) · 2 khối ngữ cảnh RocketAI đã điền sẵn để demo (mục 4) · [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]] mở sẵn (bản mẫu học viên hoàn chỉnh để đối chiếu) · slide giải phẫu 6 phần có tô màu · 2 output đối chứng prompt 1 dòng vs prompt chuẩn · [[Template 5.2 — Khối Ngữ Cảnh Chuẩn]] + [[Template 5.3 — Prompt Usage Guide]] mở sẵn.

## 4. 🎬 Kịch Bản Demo (Ví dụ RocketAI)

> Case DẠY = 🚀 RocketAI (demo live, dữ liệu từ [[Demo Case Study — Rocket AI BMC Mẫu]]). Bản mẫu học viên hoàn chỉnh để đối chiếu = 🍵 [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]] — cùng cách làm, áp lên DN B2C sản phẩm.

**Bước 1 (7') — Chế tạo khối [BỐI CẢNH DN] bằng Prompt 1.**
- Làm gì: Paste Prompt 1 (mục 8) với đầu vào là Snapshot + Avatar + Offer của RocketAI. AI chưng cất thành khối 7 dòng.
- Kết quả trông như thế nào (đọc to nguyên văn):
> `[BỐI CẢNH DN] RocketAI Solutions — công ty dịch vụ B2B tại Việt Nam, 4 founder, chuyên chuyển giao hệ điều hành AI Marketing & Sale cho SME. Khách mục tiêu: chủ spa/thẩm mỹ nữ 30-45 tuổi tự điều hành (đại diện: chị Mai, 35t, Spa ABC, 10 nhân viên, ~500tr/tháng). Sản phẩm chủ lực: AI Marketing & Sale OS™ — OS Transfer 12tr / OS Installed 25tr / OS Managed 50tr+; cam kết bằng văn bản: sau 28 ngày hệ thống không chạy → hoàn học phí. Kênh: video Facebook của founder, buổi demo Zoom, khách cũ giới thiệu. Nỗi sợ lớn nhất của khách: "AI phức tạp quá, tôi không rành công nghệ" — sợ mua phải khoá học lý thuyết. Điểm khác biệt: cài hệ thống chạy thật + mentor 1:10 + RocketAgent chạy 24/7, không dạy suông. Không bao giờ hứa: con số doanh thu/lead cụ thể, "AI thay thế hoàn toàn con người".`
- Điểm nhấn: "7 dòng này là 4 ngày công sức của anh chị được nén lại. Từ giờ AI nào đọc 7 dòng này cũng hiểu RocketAI trong 10 giây."

**Bước 2 (5') — Chế tạo khối [GIỌNG].**
- Làm gì: Lấy output Prompt 3 Ngày 04 (đặc tả giọng thương hiệu RocketAI), rút thành khối 4 dòng (đọc to nguyên văn):
> `[GIỌNG] Xưng "Rocket" hoặc "em" với khách, gọi "anh/chị". Thực chiến, thẳng thắn, minh bạch — chứng minh bằng số liệu và demo, không lên gân. Từ đặc trưng: hệ thống chạy thật, chuyển giao, hệ điều hành AI, cam kết bằng văn bản, 10x. Cấm: "thần kỳ", hứa con số doanh thu, thuật ngữ kỹ thuật không giải thích, quá 1 emoji/đoạn.`
- Kết quả: khối `[GIỌNG]` 4 dòng dán được vào mọi prompt.
- Điểm nhấn: ai chưa làm Bonus Ngày 04 → dùng Prompt 2 hôm nay (rút giọng nhanh từ 3 bài đăng/tin nhắn cũ, 5 phút).

**Bước 3 (8') — "Đóng dấu" hàng loạt: cá nhân hóa prompt khung M01.**
- Làm gì: Mở file 50 prompt khung, lấy M01 (viết bài Facebook). Prompt khung có sẵn chỗ trống `{{[BỐI CẢNH DN]}}`, `{{[GIỌNG]}}`, `{{chủ đề bài}}` — dán 2 khối vào, điền chủ đề "vì sao chủ spa làm content 4h/ngày mà khách vẫn không đến". Chạy.
- Kết quả: bài Facebook 200 từ đúng giọng thực chiến, mở bằng nỗi đau "4 tiếng mỗi ngày cho content", kết bằng CTA "inbox DEMO nhận buổi demo Zoom", không một lời hứa doanh thu.
- Điểm nhấn: bấm giờ — từ mở thư viện đến có bài: dưới 4 phút. "Đây là tốc độ vận hành từ tuần sau."

**Bước 4 (7') — Test và chấm 2 prompt nữa (S03 xử lý từ chối, CS02 tin nhắn chăm sau buổi).**
- Làm gì: Chạy S03 với objection thật của chị Mai: "25 triệu cao quá — chị tự mày mò ChatGPT cũng được mà"; chạy CS02 cho học viên (chủ spa) vừa hoàn thành Tuần 1 của chương trình 28 ngày. Chấm từng cái theo 2 câu hỏi: dùng ngay được không / phải sửa tay bao nhiêu %.
- Kết quả: S03 Đạt (sửa <10%); CS02 Chưa đạt — tin nhắn dài 200 từ như email. 
- Điểm nhấn: sửa lỗi CS02 LIVE bằng quy tắc chẩn đoán Khối 2: sai KIỂU → thêm Constraint "≤60 từ, dạng tin nhắn Zalo, 1 emoji tối đa" → chạy lại → Đạt. Ghi cả 3 dòng kết quả vào cột test của file thư viện.

**Bước 5 (3') — Tour nhanh toàn thư viện.**
- Làm gì: Lướt qua 4 nhóm trong file khung: M01-M15 (bài FB, email, kịch bản video, quảng cáo, content calendar, phân tích insight, landing page...), S01-S15 (kịch bản tư vấn, xử lý từ chối, proposal, báo giá, follow-up, phân loại khách, tóm tắt lịch sử tư vấn...), CS01-CS10 (trả lời FAQ, xử lý khiếu nại, tin chăm sóc, kịch bản gọi lại, gợi ý upsell/cross-sell...), OPS01-OPS10 (tóm tắt báo cáo, phân tích số liệu, kế hoạch tuần, đánh giá hiệu suất, viết SOP...).
- Điểm nhấn: "Về nhà anh chị KHÔNG viết gì từ đầu — chọn 20 prompt sẽ dùng nhiều nhất, đóng dấu 2 khối, test 10 cái."

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core ≤2h theo đường template)

> ⏱ Mỗi cụm ghi 2 số: **dùng template điền sẵn / lần đầu tự làm**. Tổng: **110' theo template · lần đầu có thể tới ~2h30** — quá giờ: làm theo thứ tự ưu tiên A→D; Bonus không bắt buộc, không trừ điểm.

**Cụm A — Chế tạo 2 khối ngữ cảnh (⏱ dùng template: 20' · lần đầu: 30'):**
- [ ] Chạy Prompt 1 tạo khối `[BỐI CẢNH DN]` từ Snapshot + Avatar + Offer của bạn (10')
- [ ] Chạy Prompt 2 tạo khối `[GIỌNG]` (dùng bản Ngày 04 nếu đã có) (7')
- [ ] Đọc to 2 khối — chỗ nào sai thực tế thì sửa tay (3')

**Cụm B — Cá nhân hóa 20 prompt (⏱ dùng template: 45' · lần đầu: 60'):**
- [ ] Tạo bản sao file "Prompt Library — 50 Prompt Khung" (2')
- [ ] Chọn 20 prompt bạn sẽ dùng nhiều nhất trong 2 tuần tới (gợi ý phân bổ: 7 Marketing + 6 Sales + 4 CSKH + 3 OPS) (8')
- [ ] Dán 2 khối vào từng prompt, điền các chỗ `{{...}}` còn lại bằng dữ liệu thật (35')
- 💡 **Mẹo giảm tải:** viết 2 khối MỘT lần → nhân bản hàng loạt (copy 2 khối, tìm mọi chỗ `{{[BỐI CẢNH DN]}}`/`{{[GIỌNG]}}` và dán đè) — tuyệt đối không viết lại bối cảnh cho từng prompt.

**Cụm C — Test 10 prompt (⏱ dùng template: 35' · lần đầu: 45'):**
- [ ] Chọn 10/20 prompt quan trọng nhất (phủ ≥3 nhóm), chạy thật từng cái (25')
- [ ] Chấm Đạt/Chưa đạt + ghi 1 dòng kết quả vào cột test (5')
- [ ] Prompt Chưa đạt: sửa theo quy tắc chẩn đoán (sai KIỂU → Output/Constraint; sai NỘI DUNG → Context/Input; NÔNG → Role/Task), chạy lại 1 lần (5')

**Cụm D — Nộp bài (⏱ 10' · lần đầu: 10'):**
- [ ] Nộp link file Prompt Library (quyền xem) vào thread cohort trước 23h59

**Bonus (không tính vào 2h):** viết Prompt Usage Guide 1 trang ([[Template 5.3 — Prompt Usage Guide]]); cá nhân hoá nốt 30 prompt còn lại; tự viết 3-5 prompt cho tình huống đặc thù DN bạn (theo khung 6 phần, dùng Prompt 5).

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Hoàn thiện Prompt Library v1 cho doanh nghiệp bạn: (1) file thư viện đủ 50 prompt khung với 7 cột quản lý, (2) ≥20 prompt đã cá nhân hóa (gắn khối `[BỐI CẢNH DN]` + `[GIỌNG]` + dữ liệu thật của DN), (3) ≥10 prompt đã test — cột trạng thái ghi Đạt/Chưa đạt + 1 dòng kết quả, prompt chưa đạt phải có phiên bản sửa, (4) 2 khối ngữ cảnh chuẩn đặt ở đầu file (sheet riêng hoặc khối đầu trang).

**Deliverable nộp:**
- Link file: `[Tên DN] — Ngày 05 — Prompt Library v1` (Google Sheets/Notion, quyền xem)
- Ví dụ: `MSX Group — Ngày 05 — Prompt Library v1` — bản hoàn chỉnh đúng chuẩn của học viên thật: [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]]. Đối chiếu bài của bạn với bản này TRƯỚC KHI nộp.

**Deadline:** 23h59 cùng ngày, nộp vào thread cohort ngày 05.

## 7. 📄 Template Đi Kèm

**Template 5.1 — File "Prompt Library — 50 Prompt Khung" (tài sản phát sẵn quan trọng nhất hôm nay).** Google Sheets/Markdown 7 cột: Mã | Tên prompt | Nhóm | Dùng khi nào | Prompt đầy đủ (khung 6 phần, có chỗ `{{[BỐI CẢNH DN]}}` `{{[GIỌNG]}}` và các `{{trường dữ liệu}}`) | Trạng thái test (Đạt/Chưa đạt/Chưa test) | Ghi chú kết quả. Link template: [[Template 5.1 — Prompt Library 50 Prompt Khung]]. Danh mục 50 prompt:

- **Marketing (M01-M15):** bài Facebook theo angle · bài kể chuyện khách hàng · email/tin nhắn broadcast · kịch bản video ngắn 30-60s · kịch bản livestream · nội dung quảng cáo (3 phiên bản A/B) · content calendar (lịch nội dung) tháng · phân tích insight từ comment/inbox · viết landing page theo StoryBrand · lead magnet (mồi thu hút) · caption ảnh trước-sau đúng luật · trả lời comment · brief ảnh cho designer/AI ảnh · biến 1 bài dài thành 5 định dạng · tối ưu bài cũ.
- **Sales (S01-S15):** kịch bản tư vấn đầy đủ theo SPIN · mở đầu cuộc tư vấn · xử lý từ chối (điền objection bất kỳ) · proposal (đề xuất) · báo giá cá nhân hóa · tin follow-up 3 chạm · phân loại lead nóng/ấm/lạnh từ hội thoại · tóm tắt lịch sử tư vấn 1 khách · kịch bản gọi điện hẹn lịch · tin nhắn "cứu" khách im lặng · so sánh khéo với đối thủ · chốt kèm khan hiếm thật · xin giới thiệu (referral) · tái ký/gia hạn · kịch bản khảo sát nhu cầu nhanh.
- **CSKH (CS01-CS10):** trả lời FAQ theo KB · tin chăm sau buổi/lần dùng đầu · xử lý khiếu nại theo mức độ · kịch bản gọi lại khách bỏ ngang · nhắc lịch không gây phiền · chúc mừng mốc (buổi 5/10, sinh nhật) · gợi ý upsell đúng lúc · gợi ý cross-sell (bán chéo) · xin review/feedback · tin nhắn "hâm nóng" khách lâu không quay lại.
- **OPS (OPS01-OPS10):** tóm tắt báo cáo tuần từ số liệu thô · phân tích số liệu marketing-sale · kế hoạch tuần cho chủ DN · đánh giá hiệu suất nhân viên theo tiêu chí · viết SOP từ mô tả miệng · soạn nội dung đào tạo nhân viên mới · biên bản & việc cần làm sau họp · soạn tin tuyển dụng · checklist mở/đóng ca · phân tích quyết định (nên/không nên).

**Template 5.1A — Bản mẫu dự án thực tế MSX (bản "nhìn là hiểu" để đối chiếu).** File đã điền hoàn chỉnh từ học viên thật Mẫu Sơn Xanh/MSX Group: có sẵn `[BỐI CẢNH DN]`, `[GIỌNG]`, 20 prompt đã cá nhân hóa và 10 dòng test mẫu. Đây là "đáp án mẫu" — bài của bạn phải đạt cùng độ cụ thể (đọc prompt thấy ngay: bán gì, cho ai, khác gì, cấm nói gì). Link: [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]].

**Template 5.2 — Khối ngữ cảnh chuẩn.** 2 ô điền: `[BỐI CẢNH DN]` (khung 7 dòng, ≤130 từ: DN & địa bàn | khách mục tiêu | sản phẩm chủ lực + giá + cam kết | kênh | nỗi sợ lớn nhất của khách | điểm khác biệt | điều không bao giờ hứa) và `[GIỌNG]` (4 dòng, ≤80 từ: xưng hô | 2-3 đặc điểm | từ đặc trưng | điều cấm). *Kèm 2 bản điền mẫu nguyên văn: RocketAI (như mục 4) + MSX.* Link: [[Template 5.2 — Khối Ngữ Cảnh Chuẩn]].

**Template 5.3 (Bonus) — Prompt Usage Guide 1 trang.** Các mục: 5 prompt dùng hằng ngày là gì, ai dùng nhóm nào khi nào | quy trình 4 bước: chọn prompt → điền `{{}}` → chạy → RÀ TRƯỚC KHI DÙNG (người chịu trách nhiệm cuối là người, không phải AI) | được sửa: trường Input, chủ đề | cấm sửa: Constraint an toàn (quảng cáo y tế, cam kết) | quy tắc thêm/sửa/gộp prompt + nhịp bảo trì thứ Sáu theo SOP-05 | gặp output sai → báo ai, ghi vào đâu. *Kèm bản mẫu MSX.* Link: [[Template 5.3 — Prompt Usage Guide]].

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Chưng cất khối [BỐI CẢNH DN]

```
[VAI TRÒ] Bạn là chuyên gia tối ưu câu lệnh AI (prompt engineer) cho SME, giỏi nén thông tin doanh nghiệp thành khối ngữ cảnh ngắn mà đủ.

[BỐI CẢNH] Tôi sẽ dán khối ngữ cảnh này vào đầu MỌI câu lệnh AI của doanh nghiệp từ nay về sau, nên nó phải chứa đúng những thông tin giúp AI tạo nội dung chính xác, đúng khách hàng, đúng offer và an toàn pháp lý.

[NHIỆM VỤ] Từ 3 tài liệu dưới đây, viết khối [BỐI CẢNH DN] đúng 7 dòng: (1) DN là ai, ở đâu, quy mô; (2) khách mục tiêu — 1 dòng nén từ avatar; (3) sản phẩm chủ lực + giá + cam kết chính; (4) kênh bán & marketing chính; (5) nỗi sợ/rào cản lớn nhất của khách; (6) điểm khác biệt (USP) quan trọng nhất; (7) điều KHÔNG BAO GIỜ hứa/nói. Sau đó tự kiểm: đọc khối này có tự trả lời được 3 câu "bán gì – cho ai – khác gì" trong 10 giây không; nếu không, viết lại.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán}}. Customer Avatar (bản rút gọn): {{dán}}. Core Offer Document: {{dán phần chính}}.

[ĐỊNH DẠNG ĐẦU RA] Một khối văn bản 7 dòng liền mạch bắt đầu bằng nhãn "[BỐI CẢNH DN]", không gạch đầu dòng, ≤130 từ — để dán gọn vào prompt khác.

[RÀNG BUỘC] Chỉ dùng dữ kiện có trong 3 tài liệu. Ưu tiên con số (giá, số buổi, giới hạn suất). Không tính từ quảng cáo. Tiếng Việt.
```

**Ví dụ đã điền (RocketAI):** output chính là khối 7 dòng ở mục 4 Bước 1 — dùng nguyên văn làm mẫu đối chiếu. Bản B2C: khối [BỐI CẢNH DN] của MSX trong [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]].

### Prompt 2 — Rút nhanh khối [GIỌNG] (cho ai chưa làm Bonus Ngày 04)

```
[VAI TRÒ] Bạn là chuyên gia phân tích văn phong thương hiệu.

[BỐI CẢNH] Tôi cần khối [GIỌNG] 4 dòng để dán vào mọi câu lệnh AI, giúp mọi nội dung ra đúng "chất" của tôi thay vì giọng AI mặc định.

[NHIỆM VỤ] Phân tích các mẫu văn bản tôi tự viết dưới đây và nén thành khối [GIỌNG] đúng 4 dòng: (1) xưng hô với khách; (2) 2-3 đặc điểm giọng nổi bật nhất (kèm 1 ví dụ trích nguyên văn); (3) 5 từ/cụm từ đặc trưng nên dùng; (4) 3-5 điều cấm (từ sáo rỗng, kiểu câu, mức emoji). Nếu mẫu quá ít để kết luận, hỏi tôi 3 câu về sở thích văn phong rồi mới viết.

[DỮ LIỆU ĐẦU VÀO] 3-5 mẫu tôi tự viết (caption, tin nhắn tư vấn tôi ưng ý): {{dán nguyên văn}}.

[ĐỊNH DẠNG ĐẦU RA] Khối 4 dòng bắt đầu bằng nhãn "[GIỌNG]", ≤80 từ.

[RÀNG BUỘC] Đặc điểm phải có bằng chứng từ mẫu, không phán chung chung ("thân thiện, chuyên nghiệp"). Tiếng Việt.
```

**Ví dụ đã điền (RocketAI):** dán 3 bài Facebook cũ của Tony (bài tuyển học viên, bài kể chuyện cài hệ thống) → output chính là khối [GIỌNG] 4 dòng ở mục 4 Bước 2 — chú ý đặc điểm nào cũng có bằng chứng từ bài thật ("chứng minh bằng số liệu và demo" rút từ thói quen chèn ảnh dashboard vào mọi bài).

### Prompt 3 — Prompt khung M01: Viết bài Facebook theo angle (mẫu tiêu biểu của thư viện)

```
[VAI TRÒ] Bạn là copywriter mạng xã hội cho SME tại Việt Nam, viết bài Facebook tự nhiên như người thật chia sẻ, tuân thủ quy định quảng cáo của ngành trong [BỐI CẢNH DN].

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 1 bài Facebook theo angle (góc truyền thông) được chỉ định: mở bằng hook chạm đúng tâm lý trong 2 dòng đầu (trước dấu "Xem thêm") → thân bài dẫn dắt bằng ví dụ/câu chuyện đời thường, cài 1 thông tin chuyên môn dễ hiểu → kết bằng CTA được chỉ định. Đề xuất kèm 1 dòng brief (mô tả ngắn) hình ảnh minh họa.

[DỮ LIỆU ĐẦU VÀO] Chủ đề bài: {{chủ đề}}. Angle: {{chọn: nỗi đau / mong muốn / bằng chứng / kẻ thù chung / khẩn cấp}}. Chất liệu tâm lý liên quan: {{dán 1-2 dòng Pain/Desire/Fear tương ứng từ PDFO Map}}. CTA: {{VD: inbox "DEMO" nhận buổi demo hệ thống 30 phút}}.

[ĐỊNH DẠNG ĐẦU RA] Bài 150-250 từ, xuống dòng thoáng theo kiểu Facebook, tối đa 3 emoji cả bài, kèm 3 hashtag và 1 dòng brief ảnh.

[RÀNG BUỘC] {{[GIỌNG]}}. Không hứa kết quả tuyệt đối, không dùng "số 1", không bịa số liệu/chứng nhận, không kể chuyện khách thật khi chưa xin phép. 2 dòng đầu không nhắc tên thương hiệu (hook trước, thương hiệu sau).
```

**Ví dụ đã điền (RocketAI):** `{{chủ đề}}` = "vì sao chủ spa làm content 4h/ngày mà khách vẫn không đến"; `{{angle}}` = nỗi đau; `{{chất liệu}}` = "'Marketing phụ thuộc một tay chủ' + sợ AI phức tạp, không rành công nghệ"; `{{CTA}}` = "inbox DEMO đăng ký buổi demo Zoom 26/07" → bài mở đầu: "4 tiếng mỗi ngày cho content — mà lịch hẹn vẫn trống một nửa. Chị có thấy mình trong câu đó không? Vấn đề không nằm ở chỗ chị viết chưa đủ hay, mà ở chỗ một mình chị đang gánh việc của cả một hệ thống..."

### Prompt 4 — Prompt khung S03: Xử lý từ chối (mẫu tiêu biểu nhóm Sales)

```
[VAI TRÒ] Bạn là chuyên gia huấn luyện sale ngành dịch vụ tư vấn giá trị cao, theo trường phái đồng cảm — không dồn ép, xử lý từ chối bằng cách gọi đúng nỗi sợ phía sau.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Khách vừa đưa ra lời từ chối dưới đây trong cuộc tư vấn. Hãy viết: (1) chẩn đoán 1 dòng — nỗi sợ thật phía sau câu từ chối này là gì (đối chiếu cặp Objection↔Fear tôi cung cấp); (2) 3 phương án phản hồi theo 3 mức: nhẹ nhàng gợi mở / đưa bằng chứng / mời hành động nhỏ hơn — mỗi phương án ≤80 từ, dạng lời nói/tin nhắn tự nhiên; (3) 1 câu hỏi mở để giữ cuộc hội thoại nếu khách vẫn từ chối; (4) dấu hiệu nào thì DỪNG — không đeo bám.

[DỮ LIỆU ĐẦU VÀO] Câu từ chối của khách (nguyên văn): {{dán}}. Bối cảnh cuộc tư vấn: {{khách đã xem gì, đang cân nhắc gói nào}}. Cặp Objection↔Fear liên quan: {{dán từ PDFO Map Ngày 02}}.

[ĐỊNH DẠNG ĐẦU RA] 4 mục đánh số; các câu thoại trong ngoặc kép.

[RÀNG BUỘC] {{[GIỌNG]}}. Không giảm giá để chốt (chỉ dùng ưu đãi có sẵn trong offer). Không phủ nhận cảm xúc khách ("chị đừng lo" = cấm; thay bằng công nhận rồi dẫn chứng). Không nói xấu lựa chọn khác của khách.
```

**Ví dụ đã điền (RocketAI):** `{{câu từ chối}}` = "25 triệu cao quá — chị tự mày mò ChatGPT cũng được mà"; `{{bối cảnh}}` = "chị Mai đã xem demo Zoom, đang cân nhắc gói OS Installed 25tr, lưỡng lự ở bước chốt"; `{{cặp}}` = "'tự làm được' ← sợ mất tiền cho khoá học lý thuyết, cuối cùng vẫn phải tự làm" → phương án 2 mẫu: "Dạ đúng là ChatGPT ai cũng dùng được chị ạ. Khác biệt nằm ở chỗ: Rocket không bán khoá học — Rocket cài hệ thống chạy thật trên chính spa của chị trong 28 ngày, kèm cam kết bằng văn bản: hệ thống không chạy thì hoàn học phí. Chị muốn em gửi video một hệ thống đang chạy của spa 10 nhân viên giống bên mình không?"

### Prompt 5 — Tự viết prompt mới theo khung 6 phần (prompt sinh prompt)

```
[VAI TRÒ] Bạn là prompt engineer chuyên viết câu lệnh chuẩn khung Role–Context–Task–Input–Output–Constraint cho SME.

[BỐI CẢNH] Thư viện của tôi có 50 prompt khung nhưng doanh nghiệp tôi có tình huống đặc thù chưa có prompt nào phủ. Tôi cần bạn viết prompt mới đúng chuẩn thư viện để nhân viên tôi dùng lặp lại.

[NHIỆM VỤ] Từ mô tả tình huống của tôi: (1) hỏi lại tối đa 3 câu nếu thiếu thông tin quan trọng (đầu ra mong muốn, ai dùng, tần suất); (2) viết 1 prompt hoàn chỉnh 6 phần, trong đó Context dùng placeholder {{[BỐI CẢNH DN]}}, Constraint dùng {{[GIỌNG]}} + các ràng buộc an toàn phù hợp; các dữ liệu biến thiên đặt trong {{chỗ trống có tên rõ nghĩa}}; (3) tạo 1 ví dụ đã điền với dữ liệu tôi cung cấp; (4) đề xuất mã + tên + nhóm (M/S/CS/OPS) + mô tả "dùng khi nào" để tôi dán vào thư viện.

[DỮ LIỆU ĐẦU VÀO] Tình huống cần prompt: {{mô tả việc lặp lại bạn muốn AI làm}}. Ví dụ dữ liệu thật 1 lần dùng: {{dán}}.

[ĐỊNH DẠNG ĐẦU RA] Prompt mới trong code block + ví dụ đã điền + 1 dòng thông tin thư viện (Mã | Tên | Nhóm | Dùng khi nào).

[RÀNG BUỘC] Prompt mới phải chạy được ngay khi điền chỗ trống, không phụ thuộc hội thoại trước. Tiếng Việt.
```

**Ví dụ đã điền (RocketAI):** `{{tình huống}}` = "Sau mỗi buổi demo Zoom, tôi muốn AI soạn email tóm tắt buổi demo + đề xuất gói phù hợp (Transfer/Installed/Managed) cho khách từ ghi chú của tôi, trong 1 lần chạy" → AI hỏi lại về định dạng ghi chú → xuất prompt mới mã S16 "Email tóm tắt & đề xuất gói sau demo".

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-05: Vận hành & nuôi Prompt Library**
- **Khi nào:** Dùng hằng ngày; bảo trì 20' mỗi chiều thứ Sáu (ghép cùng SOP-04).
- **Ai làm:** Mọi người dùng theo Usage Guide; chủ DN/thủ thư bảo trì.
- **Input:** Nhu cầu nội dung/tình huống hằng ngày; ghi chú "output lỗi" của người dùng trong tuần.
- **Các bước (dùng hằng ngày):** (1) Mở thư viện, lọc theo nhóm → chọn prompt theo cột "dùng khi nào"; (2) Điền các `{{chỗ trống}}` — không sửa phần Constraint an toàn; (3) Chạy, RÀ trước khi dùng (người duyệt cuối là người, không phải AI); (4) Output lỗi → ghi 1 dòng vào cột Ghi chú.
- **Các bước (bảo trì thứ Sáu):** (1) Đọc các ghi chú lỗi tuần → sửa prompt theo quy tắc chẩn đoán (sai kiểu → Output/Constraint, sai nội dung → Context/Input); (2) Tình huống mới lặp ≥2 lần trong tuần → dùng Prompt 5 sinh prompt mới, thêm mã mới; (3) Cập nhật khối [BỐI CẢNH DN] nếu offer/giá đổi (đồng bộ với KB theo SOP-04); (4) Đánh dấu prompt 30 ngày không ai dùng → cân nhắc gộp/xóa.
- **Output:** Thư viện sống, ngày càng khớp DN; nhân viên mới vào nghề chỉ cần Usage Guide + thư viện là làm được việc.
- **Tần suất:** hằng ngày + hằng tuần.

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | File thư viện đủ 50 prompt, đủ 7 cột quản lý (10đ) · ≥20 prompt đã cá nhân hóa — đếm số prompt có khối [BỐI CẢNH DN] + [GIỌNG] đã dán và chỗ trống đã điền (10đ) · 2 khối ngữ cảnh chuẩn hoàn chỉnh ([BỐI CẢNH DN] 7 dòng, [GIỌNG] 4 dòng) (10đ) |
| Chất lượng & độ sâu | 30 | ≥10 prompt có trạng thái test + 1 dòng ghi chú kết quả mỗi prompt (15đ) · ≥1 prompt Chưa đạt được sửa và chạy lại thành Đạt (thể hiện biết quy tắc chẩn đoán — có ghi chú "đã sửa gì") (10đ) · phân bổ test phủ ≥3 nhóm (không test 10 cái toàn Marketing) (5đ) |
| Cá nhân hoá vào DN thật | 25 | Khối [BỐI CẢNH DN] chứa ≥4 con số thật của DN và khớp tài liệu Ngày 1-4 (10đ) · khối [GIỌNG] có ví dụ trích từ văn bản thật của DN (5đ) · 20 prompt cá nhân hóa không còn chỗ trống `{{}}` chưa điền — mentor kiểm bằng tìm kiếm ký tự "{{" trong các prompt đã khai là cá nhân hóa (10đ) |
| Dùng được ngay | 15 | Chọn ngẫu nhiên 1 prompt Đạt, mentor chạy lại y nguyên — output dùng được (sửa tay <20%) (10đ) · file đặt tên đúng, quyền xem mở (5đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. "Cá nhân hóa" chỉ bằng cách thay tên DN, khối bối cảnh vẫn chung chung không số liệu: −10.
2. Cột test ghi "Đạt" hàng loạt nhưng không có ghi chú kết quả nào (test khống): −10.
3. Xóa/sửa Constraint an toàn (quy định quảng cáo y tế) khi cá nhân hóa: −10 và bắt buộc khôi phục.
4. Khối [BỐI CẢNH DN] dài cả trang (nhồi nguyên Snapshot thay vì chưng cất 7 dòng): −5.
5. 10 prompt test đều cùng 1 nhóm: −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Đã có Knowledge Base trên RocketAgent rồi, sao prompt vẫn phải có khối [BỐI CẢNH DN]?**
→ Hai tầng bổ trợ nhau: KB = kho tra cứu chi tiết (AI tìm khi cần); khối bối cảnh = "kim chỉ nam" luôn nằm trong tầm mắt AI ở mọi câu lệnh, kể cả khi bạn dùng AI NGOÀI RocketAgent (ChatGPT trên điện thoại, nhờ nhân viên chạy). Ngày 06 hai tầng này sẽ hợp nhất trong AI Business Brain.

**Q2: 50 prompt nhiều quá, tôi chỉ cần 10 cái có được không?**
→ Core chỉ yêu cầu cá nhân hóa 20 + test 10 — đúng tinh thần "dùng ít mà chắc". Nhưng giữ đủ 50 khung trong file: tuần 2-4 chương trình sẽ gọi đến chúng (VD tuần 2 dùng M05 content calendar, tuần 3 dùng S01 kịch bản tư vấn), lúc đó bạn chỉ việc đóng dấu thêm.

**Q3: Prompt chạy hôm nay tốt, mai chạy lại ra khác — có sao không?**
→ AI có tính ngẫu nhiên, khác 10-20% câu chữ là bình thường; miễn ĐÚNG KIỂU + ĐÚNG NỘI DUNG + ĐÚNG GIỌNG. Nếu lệch hẳn chất lượng → siết Output (định dạng, độ dài) và Constraint chặt hơn. Định dạng bắt buộc phải cố định thì cho ví dụ mẫu ngay trong prompt.

**Q4: Nhân viên tôi có được tự sửa prompt trong thư viện không?**
→ Theo Usage Guide: được ĐIỀN chỗ trống và đề xuất sửa (ghi vào cột Ghi chú); KHÔNG tự sửa bản gốc — chỉ thủ thư/chủ DN sửa vào chiều thứ Sáu. Nếu không giữ quy tắc này, sau 1 tháng thư viện nát như file Excel dùng chung không khóa.

**Q5: Dùng thư viện này trên RocketAgent hay ChatGPT?**
→ Cả hai. Prompt chuẩn 6 phần chạy được trên mọi nền tảng AI. Trong RocketAgent, các prompt hay dùng nhất sẽ được gắn vào Assistant/Agent ở Ngày 06 và tuần 3-4 (thành nút bấm thay vì copy-paste).

**Q6: Tôi viết prompt bằng tiếng Việt, AI có hiểu kém hơn tiếng Anh không?**
→ Với các AI hiện đại, prompt tiếng Việt cho ngữ cảnh Việt (khách Việt, văn nói Việt) thường ra kết quả TỐT HƠN vì không qua tầng dịch. Toàn bộ thư viện chương trình là tiếng Việt — cứ yên tâm dùng.

**Lỗi thường gặp:**
1. **Điền chỗ trống bằng dữ liệu mơ hồ** — `{{chủ đề}}` điền "viết về AI" → output lan man. *Phát hiện:* output đúng giọng nhưng nội dung nhạt, chung chung. *Sửa:* chỗ trống điền càng hẹp càng tốt ("vì sao chủ spa làm content 4h/ngày mà khách vẫn không đến" thay vì "về AI marketing"); quy tắc: mỗi `{{}}` trả lời 1 câu hỏi cụ thể.
2. **Nhồi 3 nhiệm vụ vào 1 prompt** ("viết bài + làm lịch tháng + viết quảng cáo") → cả 3 đều nửa vời. *Phát hiện:* phần Task có >1 động từ chính không liên quan nhau. *Sửa:* 1 prompt = 1 sản phẩm đầu ra; chuỗi việc thì chạy lần lượt 2-3 prompt, lấy output cái trước làm Input cái sau.
3. **Tin AI 100%, bỏ bước rà** — bài đăng có số liệu sai/câu vi phạm quảng cáo lên thẳng fanpage. *Phát hiện:* (muộn) khi khách/đối thủ chỉ ra. *Sửa:* luật cứng trong Usage Guide: mọi output chạm KHÁCH THẬT (đăng bài, gửi tin) phải qua mắt người trước; checklist rà 10 giây: số đúng chưa — có hứa quá không — đúng giọng không.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 04 — Knowledge Base Cho Doanh Nghiệp]] · Ngày sau: [[Ngày 06 — AI Business Brain]]
- Tài sản hôm nay được dùng lại ở:
	- **Khối [BỐI CẢNH DN] + [GIỌNG]** → lõi của Instruction Document cho AI Business Brain (Ngày 06 — viết instruction nhanh gấp đôi nhờ 2 khối này), system prompt của chatbot (Tuần 3).
	- **Prompt Library v1** → 5 AI Assistant Ngày 06 chính là các cụm prompt này được "cài cứng" vào vai; Tuần 2 dùng nhóm M hằng ngày (content engine); Tuần 3 dùng nhóm S (sales playbook, chatbot); Tuần 4 dùng nhóm CS + OPS (follow-up, dashboard).
	- **Kết quả test 10 prompt** → Improvement List đầu vào cho Ngày 06 (prompt nào cần KB dày hơn mới chạy tốt).
	- **Prompt Usage Guide (Bonus)** → tài liệu đào tạo nhân viên trong bộ chuyển giao cuối chương trình (Ngày 28).
