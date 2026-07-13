---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 3
day: 20
core-output: "Follow-up Sequence 14 ngày (7 chạm) + Message Library ≥18 tin theo 6 tình huống + Sales Reminder System chạy trên CRM + Follow-up KPI Sheet"
---

# Ngày 20 — Sales Follow-up Automation

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Follow-up Sequence 14 ngày lưu `04. Resources/Playbooks/`; nhắc tự động chạy trên lớp động cơ Hermes; mỗi lần chăm sóc ghi vào file khách tại `People/`.

> Hôm nay bạn xây "lưới vét doanh thu": chuỗi follow-up 14 ngày với tin nhắn viết sẵn cho mọi tình huống + hệ thống nhắc việc để KHÔNG MỘT KHÁCH NÀO rơi khỏi phễu chỉ vì bị quên — nỗi đau số 1 của chính bạn.

---

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày 20, học viên CÓ TRONG TAY:

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Follow-up Sequence 14 ngày (chuỗi chăm sóc 14 ngày)**: kịch bản 7 lần chạm (Ngày 0-1-3-5-7-10-14) cho lead sau tư vấn/báo giá — mỗi chạm có mục tiêu và nội dung riêng.
- ✅ **Follow-up Message Library**: ≥18 tin nhắn viết sẵn cho 6 tình huống (lead mới điền form / inbox rồi im / đã tư vấn chưa mua / đã nhận báo giá / từ chối vì giá / hẹn quay lại sau).
- ✅ **Sales Reminder System (hệ thống nhắc chăm khách)**: CRM nâng cấp để tự tô màu lead quá hạn + nghi thức xử lý hàng ngày — chạy được ngay bằng Google Sheets, chưa cần tool phức tạp.
- ✅ **Follow-up KPI Sheet**: bảng đo 5 chỉ số hiệu quả follow-up, cài sẵn công thức.

**Bonus Output (nâng cao):**
- ⭐ **Follow-up Automation Map**: sơ đồ đánh dấu chạm nào NGƯỜI gửi, chạm nào MÁY gửi — bản thiết kế cho Ngày 22 đấu nối tự động thật.
- ⭐ Cài 1 automation đơn giản chạy thật: tin cảm ơn/xác nhận tự động khi có lead mới (chatbot RocketAgent hoặc trả lời tự động của Fanpage/Zalo OA).

---

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Follow-up: mỏ tiền bị bỏ quên (6 phút)

- **Follow-up (theo đuổi/chăm sóc sau tiếp xúc)** = mọi lần chủ động chạm lại khách sau một sự kiện (điền form, tư vấn, nhận báo giá, từ chối). Thống kê kinh điển ngành sales: phần lớn giao dịch chốt sau lần chạm thứ 5, nhưng phần lớn người bán bỏ cuộc sau 1-2 lần. Khoảng trống giữa 2 con số đó chính là doanh thu rơi vãi.
- Nỗi đau Sen Spa (mở bằng chính bài toán Ngày 15): trong 20 lead khai quật từ inbox, có những khách như chị Hương — hỏi giá, spa trả lời, khách im, spa CŨNG im. Không phải khách từ chối — CHƯA AI HỎI LẠI. Với AOV liệu trình 12tr, mỗi tháng chỉ cần follow-up "cứu" thêm 2 khách = 24tr — bằng cả tháng lương của 2 nhân viên.
- Đổi khung tư duy cho học viên (nói thẳng): follow-up không phải "làm phiền khách" — im lặng sau khi khách đã bỏ thời gian nghe tư vấn mới là bỏ rơi khách. Phiền hay không nằm ở NỘI DUNG mỗi lần chạm: chạm để đòi ("chị chốt chưa?") là phiền; chạm để cho (ảnh kết quả, mẹo chăm da, giải đáp lo lắng) là chăm sóc.

### Khối 2 — Chuỗi 14 ngày / 7 chạm: giải phẫu từng nhịp (10 phút)

Chuỗi chuẩn cho lead SAU TƯ VẤN/BÁO GIÁ (tình huống giá trị nhất — các tình huống khác là biến thể rút gọn):

| Chạm | Ngày | Mục tiêu | Nội dung (ví dụ Sen Spa) | Ai gửi |
|---|---|---|---|---|
| 1 | Ngày 0 | Xác nhận + giữ nhiệt | Tin cảm ơn + gửi proposal (chính là Tin 1 Ngày 19) | Người |
| 2 | Ngày 1 | Cho giá trị, không đòi hỏi | Ảnh trước-sau của khách cùng tình trạng + 1 mẹo chăm da đúng ca khách | Máy được |
| 3 | Ngày 3 | Hỏi lại nhẹ + gỡ vướng | Tin 2 Ngày 19: hỏi cảm nhận + gỡ đúng điều khách lăn tăn | Người |
| 4 | Ngày 5 | Xử lý phản đối chủ động | Nội dung đánh đúng phản đối đã ghi trong CRM (kẹt giá → phương án chia đợt) | Người |
| 5 | Ngày 7 | Bằng chứng xã hội | Case study/video khách thật cùng vấn đề + kết quả theo mốc thời gian | Máy được |
| 6 | Ngày 10 | Mời lại có lý do mới | Lý do quay lại: suất ưu đãi tháng, chỗ trống lịch tuần sau, dịch vụ bổ sung | Người |
| 7 | Ngày 14 | Đóng vòng lịch sự | "Tin cuối chuỗi": tôn trọng quyết định + cửa luôn mở + chuyển nuôi dài hạn | Máy được |

- 4 nguyên tắc thiết kế chạm: (1) **Cho trước, hỏi sau** — tối thiểu 2 chạm thuần cho giá trị, không CTA đòi chốt; (2) **Mỗi chạm một lý do mới** — không lặp "chị ơi xem chưa"; (3) **Cá nhân hoá theo phản đối** — chạm 4 là chạm quyết định, phải đánh đúng cái vướng ghi trong CRM; (4) **Có điểm dừng** — sau chạm 7 chuyển sang nuôi dài hạn (content, remarketing), không bám đuổi vô hạn. Tin "đóng vòng" tử tế thường lại là tin được trả lời nhiều nhất.
- Liên kết Follow-up Rule Ngày 17: chuỗi trên áp cho lead Nóng/sau tư vấn. Lead Ấm: rút còn 4 chạm (0-3-7-14), nội dung nghiêng về giá trị. Lead Lạnh: không vào chuỗi cá nhân — để content Tuần 2 và remarketing nuôi.

### Khối 3 — Reminder System: máy nhắc người trước, máy nhắn khách sau (5 phút)

- 2 tầng tự động hoá — dạy đúng thứ tự: **Tầng 1 (hôm nay): máy nhắc NGƯỜI** — CRM tô màu lead đến hạn, người gửi tin bằng tay (copy từ Library, sửa 1-2 chi tiết). **Tầng 2 (Ngày 22): máy nhắn KHÁCH** — automation gửi các chạm "Máy được" theo trigger (điểm kích hoạt).
- Vì sao không nhảy thẳng tầng 2: automation gửi tin dở là NHÂN BẢN cái dở với tốc độ máy. Phải chạy tay chuỗi tin vài ngày, biết tin nào được trả lời, rồi mới trao cho máy. "Tự động hoá một quy trình tốt = nhân đôi doanh thu; tự động hoá một quy trình tồi = nhân đôi thảm hoạ."
- Reminder System trên Google Sheets: cột "Ngày follow-up tiếp theo" (Ngày 15) + cột mới "Chạm số mấy" + định dạng có điều kiện: đến hạn hôm nay = vàng, quá hạn = đỏ. Nghi thức sáng (SOP-15B) nâng cấp: xử lý hết dòng đỏ và vàng trước 10h.

### Khối 4 — Đo hiệu quả follow-up: 5 chỉ số (4 phút)

1. **Tỷ lệ phản hồi** = số lead trả lời ÷ số lead được follow-up (chuẩn tốt: ≥30% với lead sau tư vấn).
2. **Tỷ lệ đặt lịch lại** = số lead đặt/quay lại lịch ÷ số lead được follow-up.
3. **Tỷ lệ chốt sau follow-up** = số chốt trong nhóm đã từng im lặng ÷ số lead nhóm đó — CON SỐ CHỨNG MINH TIỀN của hệ thống hôm nay.
4. **Thời gian chốt trung bình** = số ngày từ lead mới → chốt.
5. **Lý do chưa mua** — đếm theo nhóm phản đối (giá / thời gian / niềm tin / hỏi người nhà) → nguyên liệu quay lại sửa offer và script.

> **Thích ứng ngành khác**: Nha khoa — chạm 2 gửi "điều gì xảy ra nếu trì hoãn X" viết giọng bác sĩ khách quan; nhịp có thể giãn hơn với ca lớn (khách cần thời gian thu xếp tài chính). Giáo dục — chuỗi bám theo mốc năm học/khai giảng ("lớp tháng 8 còn 3 chỗ" — chỉ khi có thật); chạm 5 là video buổi học thử. Gym — chuỗi ngắn hơn (10 ngày) vì cảm hứng tập giảm rất nhanh, chạm 2 nên là lời động viên + lịch tuần này. Coaching — giãn nhịp (0-2-5-9-14), chạm giá trị là bài viết/case sâu, tôn trọng không gian suy nghĩ của khách deal lớn.

---

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 19 | Chúc mừng ai đã GỬI proposal thật; hỏi cả lớp: "Ai từng mất khách chỉ vì quên nhắn lại? Kể 1 ca." — lấy 2 câu chuyện làm nhiên liệu vào bài |
| 25' | Giảng 4 khối kiến thức | Trọng tâm khối 2 — đi từng chạm của bảng 7 chạm; nhấn nguyên tắc "cho trước, hỏi sau" |
| 30' | Demo live: dựng chuỗi cho chị Hương + bật reminder | Theo kịch bản mục 4 |
| 15' | Học viên làm tại chỗ + Q&A | Học viên lọc CRM ra danh sách lead "đang im lặng" của chính mình — đếm và ước tính giá trị (con số này gây sốc và tạo động lực làm bài) |
| 10' | Giao bài tập + tiêu chí nghiệm thu | Nhấn: bài hôm nay có phần GỬI THẬT 3 tin — không chỉ viết |

---

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (4') — Đếm tiền đang rơi.** Mở CRM Sen Spa, lọc trạng thái "Đã tư vấn" + "Đã gửi báo giá" + "Đang cân nhắc" có "Lần liên hệ gần nhất" > 3 ngày → ra 6 lead. Nói: "6 người × liệu trình 12tr × tỷ lệ cứu được 20% ≈ 14tr đang nằm trong danh sách này. Hôm nay đi nhặt."

**Bước 2 (8') — Sinh Follow-up Sequence cho 1 khách cụ thể.** Chọn chị Hương (hỏi giá trị nám rồi im sau khi nghe 12tr — phản đối ngầm: giá). Chạy Prompt 1 (mục 8): dán hồ sơ CRM + Objection Library (Ngày 18) + case study. AI xuất chuỗi 7 chạm cá nhân hoá. Đọc to chạm 2 (cho giá trị: ảnh trước-sau khách nám + mẹo che nám an toàn khi ra nắng) và chạm 4 (gỡ giá: gói 8 buổi 9.5tr chia 2 đợt). Chỉ rõ: "Không tin nào hỏi 'chị chốt chưa' — nhưng cả chuỗi đều dẫn về buổi hẹn."

**Bước 3 (6') — Xây Message Library 6 tình huống.** Chạy Prompt 2 → bảng 18 tin cho 6 tình huống. Đọc to 2 tin đối lập nhau để lớp thấy sự khác biệt: tin cho "lead mới điền form" (nhanh, xác nhận, đặt lịch ngay) vs tin cho "khách từ chối vì giá" (tôn trọng, để cửa mở, quà giá trị nhỏ). "Một tin cho mọi tình huống = không tình huống nào trúng."

**Bước 4 (7') — Bật Reminder System trên CRM.** Thêm cột "Chạm số mấy" vào CRM; bật định dạng có điều kiện: hạn hôm nay = vàng, quá hạn = đỏ (làm live 2 phút — template đã cài sẵn, chỉ demo cho hiểu nó từ đâu ra). Điền ngày cho 6 lead ở Bước 1 theo chuỗi. Chạy thử nghi thức sáng: "8h sáng mai Ngọc mở bảng — 2 dòng đỏ, 1 dòng vàng, mở Library, copy đúng tin tình huống, sửa tên + 1 chi tiết cá nhân, gửi. 15 phút xong 3 khách."

**Bước 5 (5') — Vẽ Automation Map (bản thiết kế cho Ngày 22).** Vẽ nhanh sơ đồ: trạng thái CRM đổi thành "Đã gửi báo giá" → [MÁY] chờ 1 ngày → gửi chạm 2 → khách trả lời? → CÓ: [NGƯỜI] tiếp quản / KHÔNG: [MÁY] ngày 3 nhắc [NGƯỜI] gửi chạm 3... Tô 2 màu: xanh = máy, cam = người. "Thứ 2 tuần sau (Ngày 22) ta đấu điện cho sơ đồ này trên RocketAgent — hôm nay cứ chạy 'thủ công có hệ thống' đã ra tiền rồi."

**Bước 6 (3') — Mở KPI Sheet.** Chỉ 5 chỉ số + công thức cài sẵn, điền tay tuần đầu: mỗi lần follow-up tick 1 ô "đã gửi", khách trả lời tick "phản hồi". "Cuối tuần sau, anh chị sẽ có con số 'follow-up cứu được bao nhiêu tiền' — con số đó sẽ khiến anh chị không bao giờ bỏ hệ thống này."

---

## 5. ✅ Checklist Thực Thi (Học viên tự làm — tổng ≤ 2h phần Core)

**Cụm A — Kiểm kê lead đang im lặng (15')**
- [ ] Lọc CRM: trạng thái Đã liên hệ / Đã tư vấn / Đã gửi báo giá / Đang cân nhắc, có "Lần liên hệ gần nhất" quá 3 ngày.
- [ ] Đếm số lead + nhân AOV ước tính giá trị đang rơi — ghi con số này (sẽ nộp).
- [ ] Chọn 3 lead "đáng cứu nhất" (điểm cao nhất Ngày 17) để gửi thật hôm nay.

**Cụm B — Dựng Sequence + Library (50')**
- [ ] Chạy Prompt 1 → chuỗi 14 ngày / 7 chạm chuẩn của DN mình (viết cho tình huống "sau tư vấn/báo giá").
- [ ] Rà 4 nguyên tắc: ≥2 chạm thuần giá trị? mỗi chạm lý do mới? chạm 4 đánh trúng phản đối phổ biến nhất của khách mình? có tin đóng vòng ngày 14?
- [ ] Chạy Prompt 2 → Message Library ≥18 tin / 6 tình huống. Sửa giọng cho giống mình nhắn (đọc to 3 tin bất kỳ).
- [ ] Đánh dấu vào mỗi chạm: [NGƯỜI] hay [MÁY] gửi được.

**Cụm C — Bật Reminder + gửi thật (35')**
- [ ] Thêm cột "Chạm số mấy" + bật định dạng màu quá hạn trên CRM (template cài sẵn — copy quy tắc theo hướng dẫn 5 bước kèm file).
- [ ] Điền lịch chạm cho toàn bộ lead đang im lặng ở Cụm A theo chuỗi (lead đã im 7 ngày → vào thẳng chạm 3-4, không bắt đầu lại từ 0).
- [ ] **GỬI THẬT 3 tin** cho 3 lead đã chọn — đúng tình huống, có sửa chi tiết cá nhân.
- [ ] Ghi kết quả vào CRM + KPI Sheet (đã gửi 3, phản hồi ___ — cập nhật tiếp trong 48h).

**Cụm D — Nộp bài (15')**
- [ ] Xuất Sequence + Library + ảnh CRM có màu nhắc việc + ảnh 3 tin đã gửi, đặt tên chuẩn, đăng thread.

**Cụm Bonus (ngoài 2h)**
- [ ] Vẽ Automation Map 2 màu người/máy (mẫu ở template) — nộp thêm để Ngày 22 đấu nối nhanh hơn.
- [ ] Bật 1 automation thật: tin xác nhận tự động khi có lead mới trên Fanpage/Zalo OA/RocketAgent.

---

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Xây hệ thống follow-up cho DN bạn: chuỗi 14 ngày + thư viện tin nhắn 6 tình huống + reminder trên CRM — và GỬI THẬT 3 tin follow-up cho 3 lead đang im lặng có điểm cao nhất.

**Deliverable nộp (thread cohort, deadline 23h59 hôm nay):**
1. File Follow-up Sequence 14 ngày: `[Tên DN] — Ngày 20 — Follow-up Sequence`.
2. File Message Library ≥18 tin: `[Tên DN] — Ngày 20 — Message Library`.
3. Ảnh CRM có cột "Chạm số mấy" + màu vàng/đỏ nhắc việc: `[Tên DN] — Ngày 20 — Reminder System`.
4. Ảnh 3 tin ĐÃ GỬI THẬT (che SĐT khách): `[Tên DN] — Ngày 20 — Sent Proof`.
5. File KPI Sheet đã điền dòng đầu: `[Tên DN] — Ngày 20 — KPI Sheet`.
6. 1 dòng chia sẻ: "Số lead đang im lặng của tôi: ___, giá trị ước tính: ___đ. Đã gửi 3 tin, phản hồi tính đến giờ nộp: ___."

**Lưu ý:** phản hồi của khách KHÔNG tính vào điểm (ngoài tầm kiểm soát trong vài giờ) — nhưng GỬI hay chưa gửi thì tính. Ai nhận được phản hồi/đặt lịch từ 3 tin này, đăng vào thread — đây là những "quả ngọt đầu tiên" sẽ demo ở Ngày 21.

---

## 7. 📄 Template Đi Kèm

### Template 1 — `Follow-up Sequence 14 Ngày`
Bảng 7 chạm × 6 cột: Chạm | Ngày | Mục tiêu | Nội dung/tin nhắn | Người hay Máy | Điều kiện dừng (khách trả lời thì thoát chuỗi, người tiếp quản). Bản Sen Spa điền mẫu trọn vẹn cho ca chị Hương (phản đối giá). Kèm 2 biến thể rút gọn: chuỗi lead Ấm 4 chạm, chuỗi khách cũ tái kích hoạt 3 chạm.

### Template 2 — `Follow-up Message Library`
6 tình huống × 3 tin (18 tin), mỗi tin có: bối cảnh dùng | nội dung mẫu Sen Spa | chỗ {{cá nhân hoá}} bắt buộc sửa trước khi gửi. Sáu tình huống: (1) lead mới điền form — phản hồi trong 5-15 phút; (2) inbox rồi im; (3) đã tư vấn chưa mua; (4) đã nhận báo giá; (5) từ chối vì giá; (6) hẹn "để sau/qua Tết". Mỗi tình huống có ghi chú "điều tuyệt đối tránh" (ví dụ tình huống 5: tránh giảm giá ngay trong tin đầu).

### Template 3 — `Reminder System (nâng cấp CRM)`
File hướng dẫn 5 bước có ảnh chụp màn hình: thêm cột "Chạm số mấy" → chọn vùng → Format → Conditional formatting → 2 quy tắc màu (đến hạn = vàng, quá hạn = đỏ) + công thức dán sẵn chỉ việc copy. Kèm quy ước nghi thức sáng nâng cấp (đỏ trước, vàng sau, xong trước 10h).

### Template 4 — `Follow-up KPI Sheet`
Bảng tuần × 5 chỉ số: số lead được follow-up / tỷ lệ phản hồi / tỷ lệ đặt lịch lại / số chốt sau follow-up (+ giá trị đ) / phân bố lý do chưa mua (5 nhóm đếm). Công thức % cài sẵn; dòng ví dụ Sen Spa tuần 1: gửi 12, phản hồi 5 (42%), đặt lịch 2, chốt 1 (12tr), lý do: giá 3 - thời gian 1 - hỏi chồng 1.

### Template 5 — `Automation Map (khung vẽ — Bonus)`
Sơ đồ khối có sẵn ký hiệu: ô trigger (trạng thái CRM đổi / form mới / không phản hồi X ngày) → ô hành động [MÁY] xanh / [NGƯỜI] cam → ô điều kiện rẽ nhánh. Bản Sen Spa vẽ mẫu luồng "Đã gửi báo giá". Dùng lại nguyên bản ở Ngày 22.

---

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Sinh Follow-up Sequence 14 ngày cá nhân hoá

```
Bạn là chuyên gia thiết kế chuỗi chăm sóc khách hàng (follow-up sequence) cho ngành dịch vụ Việt Nam, trường phái "cho giá trị trước, mời mua sau", tuyệt đối không đeo bám gây khó chịu.

BỐI CẢNH: {{tên DN, dịch vụ, giá, bước trải nghiệm}}. Kênh nhắn chính: {{Zalo/Messenger}}. Xưng hô: {{em — chị/anh}}. Bằng chứng có thể gửi: {{case study, ảnh trước-sau, video, review}}. Chính sách có thể dùng: {{chia đợt, gói nhỏ, ưu đãi đang có thật}}.

NHIỆM VỤ: Viết chuỗi follow-up 14 ngày / 7 chạm (Ngày 0-1-3-5-7-10-14) cho tình huống: khách {{đã tư vấn + nhận báo giá nhưng chưa quyết}}. Phản đối chính của khách: {{dán từ CRM, ví dụ: kẹt tổng chi phí}}.

ĐẦU RA: Bảng 7 chạm: Chạm | Ngày | Mục tiêu | Tin nhắn hoàn chỉnh sẵn gửi (có chỗ {{tên khách}}) | Người hay Máy nên gửi | Điều kiện thoát chuỗi. Cấu trúc bắt buộc: chạm 2 và 5 thuần CHO GIÁ TRỊ không CTA bán; chạm 4 xử lý đúng phản đối đã nêu; chạm 7 là tin đóng vòng tôn trọng + chuyển nuôi dài hạn.

RÀNG BUỘC: Mỗi tin ≤ 5 câu, giọng nhắn tin thật, mỗi chạm một lý do mới — không tin nào lặp ý "chị xem chưa". Không tạo khan hiếm giả. Không giảm giá trần trụi — chỉ đổi cấu trúc (gói nhỏ, chia đợt) theo chính sách tôi cho. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{phản đối}}` = "nghe giá 12tr xong im — khả năng kẹt tổng chi phí". Chạm 4 mẫu AI trả về: "Chị Hương ơi, em chợt nghĩ đến chị vì tháng này bên em có phương án liệu trình 8 buổi 9.5tr, chia 2 đợt — mỗi đợt chưa đến 5tr ạ. Nhiều chị bắt đầu gọn như vậy rồi nâng cấp sau khi thấy da chuyển. Chị muốn em giữ 1 suất soi da tuần này để xem gói này có hợp da mình không ạ?"

### Prompt 2 — Sinh Message Library 6 tình huống

```
Bạn là người viết tin nhắn chăm sóc khách hàng cho {{tên DN, ngành}}, viết như một người tư vấn có tâm nhắn cho từng khách — không như hệ thống gửi hàng loạt.

BỐI CẢNH: Dịch vụ + giá: {{tóm tắt}}. Kênh: {{Zalo/Messenger}}. Xưng hô: {{em — chị/anh}}. Tài sản có thể đính kèm: {{ảnh kết quả, cẩm nang, video, link đặt lịch}}.

NHIỆM VỤ: Viết Message Library gồm 6 tình huống × 3 tin (tin đầu / tin sau 2-3 ngày nếu im / tin đóng): (1) Lead mới vừa điền form — gửi trong 15 phút; (2) Khách inbox hỏi rồi im; (3) Khách đã tư vấn nhưng chưa mua; (4) Khách đã nhận báo giá; (5) Khách từ chối vì giá; (6) Khách hẹn "để sau / qua Tết / lương về".

ĐẦU RA: 18 tin đánh số theo tình huống (1a/1b/1c... 6a/6b/6c), mỗi tin: bối cảnh 1 dòng + nội dung hoàn chỉnh có {{tên khách}} và chỗ {{chi tiết cá nhân hoá}} + ghi chú nên đính kèm gì.

RÀNG BUỘC: Mỗi tin ≤ 5 câu. Tình huống 5: tin đầu KHÔNG giảm giá — đồng cảm + phương án cấu trúc; tình huống 6: tin đầu đồng ý hẹn một cách tôn trọng + xin phép chạm lại đúng mốc khách nói. Không tin nào mở đầu bằng "Dạ chị ơi chị xem tin chưa ạ". Viết tiếng Việt.
```

### Prompt 3 — Cá nhân hoá tin trước khi gửi (dùng hằng ngày, 30 giây/tin)

```
Bạn là trợ lý cá nhân hoá tin nhắn follow-up.

ĐẦU VÀO: (1) Tin mẫu từ Library: {{dán tin}}. (2) Hồ sơ khách từ CRM: {{tên, nhu cầu, ghi chú hội thoại gần nhất, phản đối, lần chạm trước đã nói gì}}. (3) Diễn biến mới (nếu có): {{ví dụ: khách vừa xem story spa hôm qua}}.

NHIỆM VỤ: Viết lại tin mẫu thành tin cá nhân hoá cho ĐÚNG khách này.

ĐẦU RA: 2 phiên bản tin (khác nhau ở câu mở), mỗi bản ≤ 5 câu, sẵn copy gửi.

RÀNG BUỘC: Phải nhắc đúng 1 chi tiết riêng của khách (điều họ nói, tình trạng của họ) — nếu hồ sơ không đủ chi tiết để cá nhân hoá, nói thẳng "hồ sơ thiếu, cần bổ sung X" thay vì viết chung chung. Không lặp nguyên văn lời chạm trước. Viết tiếng Việt.
```

### Prompt 4 — Phân tích "lý do chưa mua" cuối tuần

```
Bạn là chuyên gia phân tích dữ liệu bán hàng cho SME.

BỐI CẢNH: {{tên DN}}. Tuần này tôi follow-up {{số}} lead, dưới đây là kết quả từng lead.

ĐẦU VÀO: {{dán từ CRM: tên | nhóm điểm | chạm đã gửi | có phản hồi không | phản hồi nói gì | kết quả (chốt/hẹn/im/từ chối) | lý do nếu biết}}

ĐẦU RA: (1) Điền 5 chỉ số KPI: tỷ lệ phản hồi, tỷ lệ đặt lịch, tỷ lệ chốt sau follow-up, thời gian chốt trung bình (nếu đủ dữ liệu), phân bố lý do chưa mua theo 5 nhóm (giá / thời điểm / niềm tin / hỏi người khác / khác). (2) Nhận định: tin/chạm nào đang được phản hồi tốt nhất — kém nhất. (3) Đề xuất đúng 2 việc tuần sau: 1 tin cần viết lại (kèm bản viết lại) + 1 nhóm khách cần cách tiếp cận khác.

RÀNG BUỘC: Kết luận phải dẫn từ số liệu tôi đưa, không phỏng đoán ngoài dữ liệu. Nếu mẫu quá nhỏ (<10 lead), ghi rõ "dữ liệu chưa đủ kết luận, đây là tín hiệu sớm". Viết tiếng Việt.
```

---

## 9. 📋 SOP Thao Tác (vận hành lặp lại sau khoá học)

**SOP-20A: Nghi thức follow-up sáng (nâng cấp SOP-15B, 20 phút)** — Ai: người tư vấn (Ngọc). Khi nào: 8h30 hàng ngày. Input: CRM có màu → Các bước: (1) xử lý dòng ĐỎ (quá hạn) trước, VÀNG sau; (2) mỗi dòng: xem "Chạm số mấy" + tình huống → mở Library lấy đúng tin → chạy Prompt 3 hoặc tự sửa 1 chi tiết cá nhân → gửi; (3) cập nhật: chạm +1, ngày follow-up mới theo chuỗi, tick KPI Sheet; (4) khách ĐÃ TRẢ LỜI ở bất kỳ chạm nào → thoát chuỗi, người tiếp quản theo Playbook Ngày 18 → Output: 0 dòng đỏ trước 10h. Tần suất: hàng ngày.

**SOP-20B: Đưa lead mới vào chuỗi** — Ai: người tư vấn. Khi nào: ngay khi lead đổi trạng thái (tư vấn xong / gửi báo giá / từ chối). Các bước: (1) chọn chuỗi đúng tình huống, (2) điền "Chạm số mấy" = 1 và ngày chạm kế, (3) ghi phản đối chính vào CRM (nguyên liệu cho chạm 4) → Output: không lead nào "ngoài chuỗi". Tần suất: mỗi sự kiện.

**SOP-20C: Review KPI follow-up chiều thứ 6 (30 phút)** — Ai: chủ DN (Lan) + người tư vấn. Các bước: (1) chốt số tuần vào KPI Sheet, (2) chạy Prompt 4, (3) quyết định 2 việc tuần sau (viết lại 1 tin kém + đổi cách tiếp cận 1 nhóm), (4) cập nhật Library — ghi ngày phiên bản → Output: hệ thống follow-up tự tốt lên mỗi tuần. Tần suất: hàng tuần.

**SOP-20D: Tái kích hoạt khách cũ hàng tháng** — Ai: người tư vấn. Khi nào: ngày 5 hàng tháng. Input: CRM lọc "Chăm sóc lại" + khách cũ ≥60 ngày không tương tác → Các bước: (1) chọn 10-20 khách, (2) dùng chuỗi tái kích hoạt 3 chạm (Template 1), lý do chạm là dịch vụ mới/ưu đãi tháng/quà tri ân có thật, (3) ghi kết quả → Output: dòng doanh thu từ data cũ — chi phí marketing bằng 0. Tần suất: hàng tháng.

---

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của Ngày 20 |
|---|---|---|
| Đủ tài sản Core | 30 | Sequence đủ 7 chạm × 6 cột, đúng nhịp 0-1-3-5-7-10-14 (10đ); Library ≥18 tin đủ 6 tình huống (10đ); ảnh CRM có cột chạm + màu nhắc việc hoạt động (5đ); KPI Sheet có đủ 5 chỉ số + đã điền dòng đầu (5đ) |
| Chất lượng & độ sâu | 30 | ≥2 chạm thuần giá trị không CTA bán (8đ); chạm 4 xử lý đúng 1 phản đối cụ thể có thật của khách mình (8đ); không tin nào trùng ý "xem chưa ạ" — kiểm cả chuỗi (7đ); có tin đóng vòng ngày 14 tôn trọng + chuyển nuôi (7đ) |
| Cá nhân hoá vào DN thật | 25 | Đã kiểm kê lead im lặng thật: có con số lead + giá trị ước tính (7đ); tin nhắn dùng bằng chứng thật của DN (ảnh kết quả/case/review có thật — không placeholder "[đính kèm ảnh]" bỏ trống) (8đ); tình huống 6 tin viết theo mùa vụ/văn hoá khách của ngành mình (5đ); lịch chạm đã điền cho ≥5 lead thật trong CRM (5đ) |
| Dùng được ngay | 15 | ĐÃ GỬI THẬT 3 tin — có ảnh (10đ; viết mà chưa gửi = 0đ mục này); 3 tin gửi đúng tình huống + có chi tiết cá nhân hoá, không bắn nguyên văn mẫu (5đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Cả 7 chạm đều đòi chốt ("chị chốt sớm kẻo hết ưu đãi" × 7 phiên bản): −10đ — vi phạm cho-trước-hỏi-sau.
2. Gửi 3 tin nguyên văn mẫu Sen Spa (còn nguyên chữ "soi da" trong khi DN là trung tâm tiếng Anh): −10đ.
3. Tạo khan hiếm giả ("chỉ còn 1 suất duy nhất hôm nay") không có thật: −8đ.
4. Chuỗi không có điều kiện thoát — khách trả lời rồi máy/người vẫn bắn tiếp theo lịch: −5đ.
5. Giảm giá trần trụi ngay tin đầu cho khách từ chối vì giá: −5đ.

---

## 11. ❓ FAQ & Lỗi Thường Gặp

**Hỏi 1: "Nhắn 7 lần trong 14 ngày có bị coi là spam làm phiền không?"**
Đáp: Nhìn lại cấu trúc: 7 chạm nhưng chỉ 3-4 chạm có lời mời, còn lại là CHO (ảnh kết quả, mẹo, case study) — và khách trả lời là thoát chuỗi ngay. Người ta khó chịu với 2 tin vô nghĩa hơn là 7 tin có giá trị. Ngoài ra khách đã tư vấn/nhận báo giá là người ĐANG cân nhắc — họ thường biết ơn vì được nhắc đúng lúc.

**Hỏi 2: "Tôi ngại nhắn lại khách đã im 2-3 tuần, cảm giác như đi xin?"**
Đáp: Đổi tư thế bằng nội dung: đừng nhắn "chị còn quan tâm không ạ" (tư thế xin) — nhắn "bên em vừa có kết quả khách cùng tình trạng với chị, gửi chị tham khảo" (tư thế cho). Với khách im quá 14 ngày, vào thẳng tin kiểu chạm 5 hoặc tin tái kích hoạt, không cần xin lỗi vì đã lâu không nhắn.

**Hỏi 3: "Khi nào thì dùng automation gửi tự động thay vì gửi tay?"**
Đáp: Quy tắc phân vai trong Automation Map: MÁY gửi tốt các chạm giá trị 1 chiều (xác nhận, tài liệu, case study — chạm 1 nếu template hoá, 2, 5, 7); NGƯỜI gửi các chạm cần đọc tình huống (3, 4, 6 — hỏi lại, gỡ phản đối, mời lại). Và chỉ trao cho máy tin đã được kiểm chứng bằng tay có phản hồi tốt. Ngày 22 sẽ đấu nối phần máy.

**Hỏi 4: "Khách bảo 'để qua Tết' thì cứ chờ qua Tết thật à?"**
Đáp: Tôn trọng mốc + giữ ấm nhẹ: xác nhận hẹn ("vậy ra Tết em nhắn mình nha chị") + đặt follow-up đúng mốc trong CRM + TRONG lúc chờ vẫn để khách trong luồng nuôi chung (content, chúc Tết — không bán). Ra đúng mốc, nhắn kèm lý do mới. Sai lầm là hoặc quên hẳn, hoặc phá hẹn nhắn dồn trước mốc.

**Hỏi 5: "Follow-up bằng gọi điện hay nhắn tin tốt hơn?"**
Đáp: Nhắn trước — gọi sau khi có tín hiệu. Khách Việt ít nghe số lạ nhưng đọc gần hết tin Zalo. Ngoại lệ: lead Rất nóng (Ngày 17) và khách đã hẹn gọi thì GỌI thẳng — nhắn tin với lead 90 điểm là phí độ nóng. Kênh nào khách bắt đầu, ưu tiên kênh đó.

**Hỏi 6: "Tôi không có ảnh trước-sau/case study để gửi ở chạm 2 và 5 thì sao?"**
Đáp: Kho bằng chứng là tài sản Tuần 2 — quay lại dùng: review chụp màn hình, video cảm nhận khách, con số (X khách đã dùng). Chưa có gì thật thì chạm giá trị đổi thành mẹo chuyên môn hữu ích (checklist, hướng dẫn) — TUYỆT ĐỐI không bịa case study. Và ghi việc "xây kho bằng chứng" vào tuần tới: mỗi khách hài lòng xin 1 review/1 ảnh.

**Lỗi thường gặp:**
1. **Xây chuỗi xong không đưa lead cũ vào** (chỉ áp cho lead mới từ nay) → Phát hiện: cột "Chạm số mấy" trống ở các lead đang im lặng → Sửa: Cụm A của checklist chính là việc này — lead im 7+ ngày vào thẳng chạm 3-4.
2. **Quên tắt chuỗi khi khách đã trả lời/đã chốt** → khách vừa đặt cọc xong lại nhận tin "chị còn băn khoăn gì không ạ" → Phát hiện: khách trả lời "ơ em nhắn nhầm à?" → Sửa: điều kiện thoát ghi ngay trong Sequence + bước 4 của SOP-20A; khi chốt → đổi trạng thái CRM là việc ĐẦU TIÊN.
3. **Tin nhắn dài như email công văn** → Phát hiện: tin > 5 câu, có "Kính gửi quý khách" → Sửa: ràng buộc ≤5 câu có sẵn trong prompt; đọc to trước khi gửi — không giống mình nói thì viết lại.
4. **Đo KPI bằng cảm giác ("thấy cũng có phản hồi")** → Phát hiện: KPI Sheet trống sau 2 tuần → Sửa: tick ngay lúc gửi/lúc nhận phản hồi (2 giây/lần), đưa vào SOP-20A bước 3; số không ghi lúc nóng sẽ không bao giờ được ghi.

---

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 19 — Proposal, Báo Giá & Hợp Đồng]] — tin gửi proposal + tin nhắc 48h hôm qua chính là chạm 1 và 3 của chuỗi; trạng thái "Đã gửi báo giá" là điểm khởi động chuỗi quan trọng nhất.
- Ngày sau: [[Ngày 21 — Sales Engine Review & Demo Day 3]] — chuỗi follow-up là mắt xích cuối của luồng demo "lead vào → bot → chấm điểm → tư vấn → proposal → follow-up → chốt/nuôi"; phản hồi từ 3 tin gửi thật hôm nay là "kết quả sống" để khoe ở Demo Day.
- Tài sản hôm nay được dùng lại: **Ngày 22** (Automation Map là bản vẽ thi công — các chạm [MÁY] được đấu nối chạy tự động trên RocketAgent), **Ngày 24** (chuỗi chăm sóc SAU BÁN + upsell xây theo đúng khung chuỗi hôm nay), **Ngày 25-26** (5 chỉ số KPI Sheet đổ vào dashboard tổng).
- Tư duy xuyên suốt: CRM (Ngày 15) là bộ nhớ, scoring (Ngày 17) là bộ lọc, follow-up là NHỊP TIM — hệ thống bán hàng sống hay chết nằm ở việc nhịp này có đập đều hàng ngày không. Từ hôm nay, "quên khách" không còn là lỗi của trí nhớ — chỉ có thể là lỗi của việc không mở CRM.
