---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 3
day: 17
core-output: "Lead Scoring Model (bảng điểm hành vi + thông tin) + Qualification Form 5 câu + Follow-up Rule 4 nhóm + AI Lead Analysis Prompt đã chạy trên 10 lead thật"
---

# Ngày 17 — Lead Scoring & Qualification

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Lead Scoring Sheet đặt tại `03. Areas/Sales Pipeline & CRM/` (module bổ sung của chương trình); điểm + nhóm nóng/ấm/lạnh ghi vào từng file `People/`.

> Hôm nay bạn xây "máy đo nhiệt độ khách hàng": mỗi lead có một con số 0-100 cho biết ai cần gọi NGAY, ai cần nuôi thêm — để 2 tiếng bán hàng mỗi ngày dồn đúng vào người sắp trả tiền.

---

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày 17, học viên CÓ TRONG TAY:

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Lead Scoring Model (mô hình chấm điểm khách hàng tiềm năng)**: bảng điểm 2 nhóm — điểm hành vi + điểm thông tin — với thang 4 mức Lạnh/Ấm/Nóng/Rất nóng, hiệu chỉnh theo DN mình.
- ✅ **Lead Qualification Form (form sàng lọc khách)**: 5 câu hỏi lọc lead cài vào chatbot/form đặt lịch.
- ✅ **Follow-up Rule**: quy tắc xử lý cho từng nhóm lead (Rất nóng gọi trong bao lâu, Lạnh đưa đi đâu) — 1 bảng in dán được cạnh màn hình.
- ✅ **AI Lead Analysis Prompt** đã chạy thật: chấm điểm ≥10 lead trong CRM bằng AI, điền kết quả vào cột "Điểm" mới của CRM.

**Bonus Output (nâng cao):**
- ⭐ **Lead Priority Dashboard**: sheet lọc tự động "Top 5 lead cần xử lý hôm nay" theo điểm giảm dần.
- ⭐ Chạy AI phân tích cả 20-40 lead trong CRM và so kết quả AI với cảm nhận của mình.

---

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Lead Scoring là gì, vì sao chủ SME bận rộn cần nó nhất (6 phút)

- **Lead Scoring (chấm điểm khách hàng tiềm năng)** = gán mỗi lead một con số thể hiện xác suất mua, dựa trên hành vi + thông tin của họ. Điểm cao = ưu tiên trước.
- **Analogy giảng**: phòng cấp cứu bệnh viện. Không khám theo thứ tự đến — khám theo mức nguy kịch (triage — phân loại ưu tiên). Sale cũng vậy: 30 lead trong CRM, chỉ có 2 giờ — phải "cấp cứu" người sắp mua trước.
- **Nỗi đau Sen Spa để mở bài**: Ngọc có 30 lead, chăm theo trí nhớ và cảm tính — hay nhắn cho người "dễ nói chuyện" thay vì người "sắp mua". Chị Quỳnh (đã tư vấn, chê giá — thực chất RẤT nóng) bị bỏ quên 5 ngày, trong khi Ngọc mải rep một bạn hỏi vu vơ chưa từng đến spa. Scoring thay cảm tính bằng con số.
- **MQL vs SQL** (dạy nhanh, đừng sa lầy thuật ngữ): MQL (Marketing Qualified Lead — lead đạt chuẩn marketing) = có quan tâm thật, đáng NUÔI (ví dụ: tải tài liệu, xem video). SQL (Sales Qualified Lead — lead đạt chuẩn bán hàng) = đáng để sale GỌI (hỏi giá, đặt lịch, có ngân sách). Ranh giới trong model hôm nay: 60 điểm.

### Khối 2 — Xây bảng điểm: hành vi + thông tin (10 phút)

Điểm lead = **điểm hành vi** (khách LÀM gì) + **điểm thông tin** (khách LÀ ai). Bảng chuẩn khởi điểm (học viên hiệu chỉnh theo ngành):

**Điểm hành vi:**

| Hành vi | Điểm | Ví dụ Sen Spa |
|---|---|---|
| Đặt lịch tư vấn/trải nghiệm | +40 | Book buổi soi da |
| Inbox hỏi giá | +25 | "Trị nám bao nhiêu?" |
| Điền form | +20 | Form "Nhận tư vấn da miễn phí" (landing page Tuần 2) |
| Trả lời khảo sát/qualification form | +20 | Trả lời 5 câu sàng lọc |
| Tải tài liệu (lead magnet) | +15 | Tải "Cẩm nang trị nám tại nhà" |
| Xem video bán hàng/livestream | +10 | Xem video khách review liệu trình |
| Không phản hồi 7 ngày | −15 | Seen không rep 1 tuần |

**Điểm thông tin (khung BANT rút gọn — Budget/Authority/Need/Timing: ngân sách/quyền quyết định/nhu cầu/thời điểm):**

| Thông tin | Điểm | Ví dụ Sen Spa |
|---|---|---|
| Đúng tệp khách mục tiêu | +15 | Nữ 28-45, ở Hà Nội, có vấn đề da rõ |
| Có ngân sách (nói ra hoặc suy đoán được) | +20 | "Tầm 10-15tr thì làm được không?" |
| Có nhu cầu trong 30 ngày | +20 | "Muốn đẹp trước đám cưới tháng sau" |
| Là người quyết định | +20 | Tự trả tiền cho mình (spa: đa số Có) |
| Chưa rõ nhu cầu | −10 | "Cho xin giá tất cả dịch vụ" |

**Thang 4 mức và ý nghĩa hành động:**

| Điểm | Nhóm | Hành động |
|---|---|---|
| 81-100 | 🔴 Rất nóng | Sale gọi trong 1 giờ (giờ hành chính) |
| 61-80 | 🟠 Nóng | Nhắn cá nhân hoá + mời đặt lịch trong 24h |
| 31-60 | 🟡 Ấm | Đưa vào chuỗi nuôi dưỡng (content, case study) — Ngày 20 |
| 0-30 | 🔵 Lạnh | Remarketing/nuôi dài hạn, KHÔNG tốn giờ sale |

- **Điểm giảng quan trọng**: con số khởi điểm không cần "đúng tuyệt đối" — cần NHẤT QUÁN. Sau 2-4 tuần nhìn lại: nếu có khách 30 điểm chốt và khách 85 điểm rơi thường xuyên → chỉnh trọng số. Model sống, không phải tượng đá.

### Khối 3 — Qualification Form: hỏi 5 câu để khách tự lộ nhiệt độ (5 phút)

- Thay vì đoán, HỎI. 5 câu chuẩn cho ngành tư vấn (cài vào chatbot Ngày 16 hoặc form đặt lịch): (1) Vấn đề/nhu cầu chính là gì? (chọn 3-4 nhóm) (2) Tình trạng này bao lâu rồi / đã thử cách nào chưa? (3) Mong muốn đạt kết quả trong bao lâu? (4) Khoảng đầu tư dự kiến? (hỏi khéo bằng khoảng chọn) (5) Khung giờ tiện để được tư vấn?
- Kỹ thuật hỏi ngân sách không sỗ sàng: cho khoảng chọn — "Để tư vấn gói phù hợp, chị dự kiến đầu tư khoảng: dưới 5tr / 5-10tr / 10-20tr / trên 20tr?" — khách chọn khoảng dễ hơn khai số.
- Mỗi đáp án gắn sẵn điểm → khách điền xong là có điểm thô, không cần ai ngồi chấm.

### Khối 4 — Dùng AI làm "trợ lý chấm điểm" (4 phút)

- Việc AI làm tốt: đọc hội thoại lộn xộn → chấm điểm theo bảng của bạn + GIẢI THÍCH vì sao + gợi ý câu follow-up + dự đoán phản đối sắp gặp. Người vẫn duyệt số cuối — AI đề xuất, người quyết.
- Demo tư duy: AI không thay bảng điểm — AI áp bảng điểm của BẠN nhanh gấp 50 lần bạn. Không có bảng điểm thì AI cũng chấm cảm tính như Ngọc.

> **Thích ứng ngành khác**: Nha khoa — "Authority" quan trọng khi khách hỏi cho con/bố mẹ (+20 nếu là người chi trả); hành vi "gửi ảnh răng" +25. Giáo dục — người quyết là phụ huynh, thêm câu form "ai là người quyết định việc học của con"; timing theo mùa tuyển sinh +20. Gym — "đăng ký tập thử" tương đương đặt lịch +40. Coaching — ngân sách và quyền quyết định chiếm trọng số cao hơn (nâng Budget lên +25), vì deal lớn và khách cá nhân dễ "thích nhưng không đủ tiền".

---

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 16 | Chiếu 2 hội thoại chatbot tiêu biểu (1 xử lý phản đối giá hay, 1 handoff mượt). Câu dẫn: "Bot đang gom lead về — nhưng lead nào gọi trước? Hôm nay trả lời bằng con số." |
| 25' | Giảng 4 khối kiến thức | Trọng tâm khối 2 — chiếu bảng điểm, hỏi lớp "hành vi nào của khách NGÀNH BẠN đáng +40?" lấy 3-4 câu trả lời |
| 30' | Demo live: chấm điểm 5 lead Sen Spa bằng tay + bằng AI | Theo kịch bản mục 4 |
| 15' | Học viên làm tại chỗ + Q&A | Học viên mở CRM của mình, thêm cột "Điểm" + "Nhóm", tự chấm tay 3 lead đầu theo bảng mẫu |
| 10' | Giao bài tập + tiêu chí nghiệm thu | Nhấn: phải chạy AI trên ≥10 lead THẬT và ghi lại 1 ca AI chấm khác mình nghĩ |

---

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (5') — Chấm tay 2 lead để "cảm" bảng điểm.** Mở CRM Sen Spa (Ngày 15), thêm 2 cột: `Điểm` và `Nhóm`. Chấm to rõ từng dòng:
- Chị Quỳnh: đã đến soi da (+40 đặt lịch, đã thực hiện), hỏi giá (+25), đúng tệp (+15), chê giá nhưng hỏi trả góp — tức có ngân sách một phần (+10, hiệu chỉnh), nhu cầu trong 30 ngày (+20) → vượt 100, chốt 100 = 🔴 Rất nóng. Nói: "Người chê giá SAU KHI tư vấn là người muốn mua — đây là lead bị Ngọc bỏ quên 5 ngày."
- Chị Trang: comment hỏi (+10 tương tác), chưa rõ nhu cầu (−10), chưa để SĐT → 0-10 điểm = 🔵 Lạnh. "Đừng để Ngọc mất 30 phút mỗi ngày cho lead này — để chatbot và content nuôi."

**Bước 2 (8') — Chạy AI chấm 5 lead một lúc.** Mở RocketAgent AI Assistant (hoặc Claude/ChatGPT), dán Prompt 3 (mục 8) kèm bảng điểm Sen Spa + 5 dòng lead copy từ CRM (kèm ghi chú hội thoại). AI trả về bảng: điểm từng lead + giải thích + hành động đề xuất + phản đối dự đoán. Đối chiếu với 2 lead vừa chấm tay — trùng khớp → lớp tin model.

**Bước 3 (5') — Soi 1 ca AI chấm "lệch" và xử lý.** AI chấm cô Lan Anh (khách cũ làm 1 buổi lẻ) chỉ 35 điểm vì "không phản hồi lâu". Trainer phân tích: khách CŨ đã từng trả tiền — bảng điểm thiếu tiêu chí "đã từng mua +25". Sửa bảng điểm live, chạy lại → cô Lan Anh lên 60 = Ấm-Nóng. Bài học: model sai thì sửa MODEL, không sửa tay từng con số — sửa tay là quay lại cảm tính.

**Bước 4 (7') — Điền kết quả vào CRM + dựng Lead Priority Dashboard.** Copy điểm vào cột `Điểm`, cột `Nhóm` tự nhảy màu theo định dạng có điều kiện (cài sẵn trong template). Mở sheet `Ưu tiên hôm nay`: công thức lọc sẵn top lead theo điểm giảm dần trong nhóm chưa chốt. Kết quả: "Sáng mai Ngọc mở sheet này — dòng 1 là chị Quỳnh, gọi lúc 9h."

**Bước 5 (5') — Viết Follow-up Rule dán tường.** Điền bảng quy tắc 4 nhóm (mẫu template 3): Rất nóng → Ngọc gọi trong 1h + kịch bản "gỡ phản đối giá"; Nóng → nhắn Zalo cá nhân hoá trong 24h; Ấm → vào chuỗi nuôi 14 ngày (sẽ viết Ngày 20); Lạnh → mời follow Fanpage + remarketing, không nhắn tay. In ra, dán cạnh máy Ngọc.

---

## 5. ✅ Checklist Thực Thi (Học viên tự làm — tổng ≤ 2h phần Core)

**Cụm A — Hiệu chỉnh Lead Scoring Model (30')**
- [ ] Copy `Template Lead Scoring Model`, giữ khung điểm chuẩn.
- [ ] Sửa ví dụ từng dòng theo ngành mình (hành vi "đặt lịch" của bạn là gì? "tài liệu" của bạn là gì?).
- [ ] Thêm/bớt tối đa 3 tiêu chí đặc thù ngành (ví dụ: khách cũ đã mua +25; gửi ảnh tình trạng +25).
- [ ] Tự kiểm tra: một khách ĐIỂN HÌNH ĐÃ CHỐT gần đây của bạn chấm theo bảng này được bao nhiêu? (Phải ≥61 — nếu không, trọng số đang sai, chỉnh lại.)

**Cụm B — Chấm điểm lead thật (35')**
- [ ] Thêm 2 cột `Điểm` + `Nhóm` vào CRM Ngày 15 (template có sẵn cột, copy sang).
- [ ] Tự chấm tay 3 lead để hiểu bảng.
- [ ] Chạy AI Lead Analysis Prompt (Prompt 3) với ≥10 lead — dán bảng điểm + dữ liệu lead từ CRM.
- [ ] Đối chiếu: ghi lại ít nhất 1 ca AI chấm khác cảm nhận của bạn + kết luận ai đúng, vì sao.
- [ ] Điền điểm + nhóm vào CRM đủ ≥10 dòng.

**Cụm C — Qualification Form + Follow-up Rule (40')**
- [ ] Điền `Template Qualification Form`: 5 câu + đáp án dạng lựa chọn + điểm gắn mỗi đáp án.
- [ ] Cài 5 câu này vào chatbot Ngày 16 (thêm vào phần "hỏi nhu cầu" của System Prompt) HOẶC vào form đặt lịch trên landing page Tuần 2 — chọn 1 kênh làm thật.
- [ ] Điền `Follow-up Rule` 4 nhóm: hành động — ai làm — trong bao lâu — kênh nào. Mỗi ô phải có con số thời hạn.
- [ ] Test: nhập vai 1 khách trả lời 5 câu form → cộng điểm → rơi đúng nhóm kỳ vọng không?

**Cụm D — Nộp bài (15')**
- [ ] Chụp CRM có cột điểm ≥10 dòng, xuất Model + Form + Rule, đặt tên chuẩn, đăng thread.

**Cụm Bonus (ngoài 2h)**
- [ ] Chạy AI trên toàn bộ CRM (20-40 lead), dựng sheet `Ưu tiên hôm nay` lọc top 5 theo điểm.

---

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Xây Lead Scoring Model cho DN của bạn, chấm điểm tối thiểu 10 lead thật trong CRM bằng AI, cài Qualification Form vào 1 kênh thật (chatbot hoặc form), và ban hành Follow-up Rule cho đội ngũ.

**Deliverable nộp (thread cohort, deadline 23h59 hôm nay):**
1. File Lead Scoring Model đã hiệu chỉnh: `[Tên DN] — Ngày 17 — Lead Scoring Model`.
2. Ảnh CRM có cột Điểm + Nhóm với ≥10 lead đã chấm: `[Tên DN] — Ngày 17 — CRM Scored`.
3. Ảnh chụp kết quả AI chấm (nguyên văn phần giải thích của AI cho 2-3 lead): `[Tên DN] — Ngày 17 — AI Lead Analysis`.
4. File Qualification Form + Follow-up Rule: `[Tên DN] — Ngày 17 — Form & Rule`.
5. 1 dòng chia sẻ: "Lead bị tôi đánh giá sai nhất: ___ — tôi tưởng ___ nhưng điểm nói ___."

**Lưu ý:** mục 5 (ca đánh giá sai) là phần mentor đọc kỹ nhất — nó chứng minh bạn thật sự đối chiếu model với trực giác, không chạy prompt cho có.

---

## 7. 📄 Template Đi Kèm

### Template 1 — `Lead Scoring Model`
1 trang gồm: bảng điểm hành vi 7 dòng (khung điểm chuẩn + cột "Ví dụ của DN tôi" để trống) + bảng điểm thông tin 5 dòng (khung BANT rút gọn) + 3 dòng trống "tiêu chí đặc thù ngành tôi" + thang 4 mức kèm hành động. Bản Sen Spa điền mẫu đầy đủ ở trang 2 (đúng bảng mục 2, có thêm dòng hiệu chỉnh "khách cũ đã mua +25" từ demo).

### Template 2 — `Lead Qualification Form`
5 câu chuẩn, mỗi câu: nội dung hỏi (viết 2 phiên bản — bản cho form + bản văn nói cho chatbot) | 3-4 đáp án lựa chọn | điểm từng đáp án. Bản Sen Spa điền mẫu: câu ngân sách viết dạng "Chị dự kiến đầu tư cho làn da khoảng: dưới 5tr (0đ) / 5-10tr (+10) / 10-20tr (+20) / trên 20tr (+20)".

### Template 3 — `Follow-up Rule (bảng dán tường)`
Bảng 4 dòng × 5 cột: Nhóm lead | Hành động cụ thể | Ai làm | Thời hạn | Kênh. Bản Sen Spa: 🔴 Rất nóng | Gọi điện + kịch bản gỡ phản đối | Ngọc | ≤1h giờ hành chính | Điện thoại; 🟠 Nóng | Tin nhắn cá nhân hoá + mời lịch soi da | Ngọc | ≤24h | Zalo/FB; 🟡 Ấm | Vào chuỗi nuôi 14 ngày | Bot/Sen | tự động | FB/Zalo; 🔵 Lạnh | Mời follow page, remarketing | Không tốn giờ sale | — | Quảng cáo.

### Template 4 — `CRM cột mở rộng` (bổ sung vào CRM Ngày 15)
2 cột mới `Điểm` + `Nhóm` kèm định dạng có điều kiện 4 màu + sheet `Ưu tiên hôm nay` với công thức SORT/FILTER cài sẵn (lọc trạng thái chưa chốt, sắp theo điểm giảm dần, lấy top 10).

---

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Hiệu chỉnh Lead Scoring Model theo ngành

```
Bạn là chuyên gia sales operations cho SME ngành dịch vụ bán qua tư vấn tại Việt Nam.

BỐI CẢNH: {{tên DN, ngành, dịch vụ chính, giá trung bình, hành trình khách: từ kênh nào → bước trải nghiệm → chốt}}. Tệp khách mục tiêu: {{mô tả}}.

NHIỆM VỤ: Hiệu chỉnh Lead Scoring Model cho DN tôi từ khung chuẩn dưới đây.

ĐẦU VÀO — khung chuẩn: Hành vi: đặt lịch +40, inbox hỏi giá +25, điền form +20, trả lời khảo sát +20, tải tài liệu +15, xem video +10, im lặng 7 ngày −15. Thông tin: đúng tệp +15, có ngân sách +20, nhu cầu trong 30 ngày +20, là người quyết định +20, chưa rõ nhu cầu −10. Thang: 0-30 Lạnh / 31-60 Ấm / 61-80 Nóng / 81-100 Rất nóng.

ĐẦU RA: (1) Bảng điểm đã hiệu chỉnh — mỗi dòng thêm cột "Ví dụ cụ thể ở DN tôi" (hành vi đó trông như thế nào trong inbox/form của tôi). (2) Đề xuất 2-3 tiêu chí ĐẶC THÙ ngành tôi kèm điểm và lý do. (3) Chấm thử 1 khách điển hình đã chốt của tôi: {{mô tả 1 khách gần nhất đã mua — họ đã làm gì trước khi mua}} — nếu khách này dưới 61 điểm, chỉ ra trọng số nào cần tăng.

RÀNG BUỘC: Giữ thang 0-100 và 4 mức. Tổng không quá 15 tiêu chí. Không thêm tiêu chí không đo được (ví dụ "có vẻ quan tâm"). Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{khách điển hình đã chốt}}` = "Chị Thu: thấy bài Facebook review khách trị nám → inbox hỏi giá → được mời soi da → đến soi da → nghe tư vấn → phân vân 2 ngày → chốt liệu trình 12tr." AI chấm: hỏi giá +25, đặt lịch +40, đúng tệp +15, nhu cầu rõ +20 = 100 → model chuẩn với ca chốt điển hình.

### Prompt 2 — Viết Qualification Form 5 câu gắn điểm

```
Bạn là chuyên gia thiết kế form khảo sát bán hàng, giỏi hỏi những câu khách sẵn lòng trả lời mà vẫn lộ đủ thông tin sàng lọc.

BỐI CẢNH: {{tên DN, ngành, dịch vụ chính + khoảng giá từng dịch vụ}}. Form này sẽ đặt ở: {{chatbot / form đặt lịch trên landing page}}. Giọng thương hiệu: {{mô tả}}.

NHIỆM VỤ: Viết Lead Qualification Form 5 câu theo khung: (1) nhu cầu chính, (2) tình trạng/đã thử gì, (3) thời điểm mong muốn có kết quả, (4) khoảng đầu tư dự kiến, (5) khung giờ tiện tư vấn.

ĐẦU RA: Với mỗi câu: (a) phiên bản viết cho form (ngắn, có 3-4 đáp án chọn), (b) phiên bản văn nói cho chatbot hỏi tự nhiên, (c) điểm gắn cho từng đáp án theo thang tôi cung cấp: {{dán phần điểm thông tin trong Scoring Model của bạn}}.

RÀNG BUỘC: Câu hỏi ngân sách phải dùng khoảng chọn, có 1 câu đệm lý do trước khi hỏi ("để tư vấn gói phù hợp..."). Không câu nào khiến khách cảm thấy bị thẩm vấn. Tối đa 15 từ mỗi câu hỏi. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** kết quả mẫu câu 3 bản chatbot: "Chị muốn da cải thiện rõ trước dịp nào không ạ — ví dụ cưới hỏi, du lịch, hay không gấp ạ?" — đáp án "trong 1 tháng tới" +20, "2-3 tháng" +10, "chưa gấp" 0.

### Prompt 3 — AI Lead Analysis: chấm điểm hàng loạt lead từ CRM (prompt chủ lực)

```
Bạn là trợ lý sales operations, nhiệm vụ duy nhất: áp dụng ĐÚNG bảng điểm được giao để chấm lead — không chấm theo cảm tính riêng.

BỐI CẢNH: Tôi là chủ {{tên DN, ngành}}. Bảng điểm của tôi:
{{dán toàn bộ Lead Scoring Model: bảng hành vi + bảng thông tin + thang 4 mức}}

NHIỆM VỤ: Chấm điểm từng lead dưới đây.

ĐẦU VÀO — danh sách lead (từ CRM, mỗi dòng gồm tên, nguồn, nhu cầu, trạng thái, ghi chú hội thoại, ngày liên hệ gần nhất; hôm nay là {{ngày}}):
{{dán 10-40 dòng lead}}

ĐẦU RA: Bảng markdown: Tên lead | Điểm (kèm phép cộng chi tiết: tiêu chí nào +bao nhiêu) | Nhóm (Lạnh/Ấm/Nóng/Rất nóng) | Hành động tiếp theo (1 câu cụ thể: nhắn gì/gọi khi nào) | Phản đối dự đoán (1 câu: khả năng cao khách sẽ vướng gì). Sau bảng: TOP 3 lead cần xử lý NGAY hôm nay + lý do.

RÀNG BUỘC: Chỉ dùng tiêu chí trong bảng điểm — thông tin không có thì không cộng, ghi "thiếu dữ liệu: X" ở cột điểm. Điểm trần 100, sàn 0. Không tự thêm tiêu chí. Hành động tiếp theo phải khớp Follow-up Rule theo nhóm. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** dán 5 lead từ CRM Ngày 15. Kết quả mẫu dòng chị Quỳnh: "Quỳnh | 100 (đặt lịch đã thực hiện +40, hỏi giá +25, đúng tệp +15, ngân sách một phần +10, nhu cầu 30 ngày +20, trần 100) | 🔴 Rất nóng | Gọi 9h sáng mai, mở đầu bằng phương án chia 2 đợt thanh toán | Dự đoán: vẫn kẹt tổng ngân sách — chuẩn bị gói 8 buổi 9.5tr làm phương án B."

### Prompt 4 — Khám sức khoẻ model sau 2 tuần chạy

```
Bạn là chuyên gia phân tích dữ liệu bán hàng, chuyên phát hiện model chấm điểm bị lệch.

BỐI CẢNH: {{tên DN}} đã chạy Lead Scoring Model này {{số tuần}} tuần: {{dán model}}.

NHIỆM VỤ: Đánh giá model có đang phản ánh đúng thực tế chốt đơn không.

ĐẦU VÀO: Dữ liệu kết quả (từ CRM): {{dán danh sách: tên lead | điểm đã chấm | kết quả thực tế: đã chốt / đang cân nhắc / mất}}

ĐẦU RA: (1) Bảng đối chiếu: nhóm điểm nào chốt bao nhiêu %, nhóm nào lệch kỳ vọng (kỳ vọng: Rất nóng chốt ≥40%, Nóng ≥20%, Ấm ≤15%, Lạnh ≤5%). (2) Liệt kê các ca "điểm thấp nhưng chốt" và "điểm cao nhưng mất" + điểm chung của chúng. (3) Đề xuất tối đa 3 chỉnh sửa trọng số kèm lý do từ dữ liệu.

RÀNG BUỘC: Chỉ đề xuất chỉnh khi có ≥2 ca cùng mẫu hình — 1 ca lẻ không đủ bằng chứng. Không đề xuất đập model xây lại. Viết tiếng Việt.
```

---

## 9. 📋 SOP Thao Tác (vận hành lặp lại sau khoá học)

**SOP-17A: Chấm điểm lead mới cuối ngày (10 phút)** — Ai: người tư vấn (Ngọc). Khi nào: cuối ca, sau khi nhập lead vào CRM (SOP-15A). Input: các dòng lead mới/có tương tác mới hôm nay → Các bước: (1) copy các dòng đó + bảng điểm vào Prompt 3, (2) chạy AI, đọc phần giải thích — thấy vô lý thì chỉnh tay và ghi chú lý do, (3) điền Điểm + Nhóm vào CRM, (4) lead 🔴 Rất nóng phát sinh → báo ngay người phụ trách (không đợi mai) → Output: 100% lead mới có điểm trong ngày. Tần suất: hàng ngày.

**SOP-17B: Phân việc theo nhiệt độ mỗi sáng** — Ai: người tư vấn. Khi nào: đầu ca, ngay sau SOP-15B. Input: sheet `Ưu tiên hôm nay` → Các bước: (1) xử lý hết 🔴 trước 10h, (2) nhắn 🟠 trước 12h, (3) 🟡 kiểm tra đang ở đúng chuỗi nuôi chưa, (4) 🔵 không đụng → Output: giờ vàng buổi sáng dồn cho lead nóng. Tần suất: hàng ngày.

**SOP-17C: Hiệu chỉnh model 2 tuần/lần (30 phút)** — Ai: chủ DN (Lan). Khi nào: chiều thứ 6, tuần chẵn. Input: CRM cột điểm + kết quả chốt/mất → Các bước: (1) chạy Prompt 4, (2) duyệt tối đa 3 chỉnh sửa, (3) cập nhật file Model + thông báo đội, (4) ghi 1 dòng nhật ký thay đổi cuối file model → Output: model bám thực tế. Tần suất: 2 tuần/lần.

---

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của Ngày 17 |
|---|---|---|
| Đủ tài sản Core | 30 | Scoring Model đủ 2 bảng (hành vi + thông tin) + thang 4 mức (10đ); Qualification Form đủ 5 câu có đáp án + điểm gắn từng đáp án (10đ); Follow-up Rule đủ 4 nhóm × 5 cột (10đ) |
| Chất lượng & độ sâu | 30 | ≥10 lead thật đã chấm, có cột Điểm + Nhóm trong CRM (10đ — thiếu 1 lead trừ 1đ); kết quả AI có phép cộng chi tiết từng tiêu chí, không phải con số trần trụi (10đ); có ghi lại ≥1 ca AI chấm lệch trực giác + kết luận (10đ — mục này viết chay "AI chấm đúng hết" = 3đ) |
| Cá nhân hoá vào DN thật | 25 | Có ≥2 tiêu chí đặc thù ngành tự thêm, khác bản mẫu Sen Spa (10đ); ví dụ từng dòng bảng điểm viết theo hành vi thật của khách DN mình (5đ); đã kiểm chứng bằng 1 khách đã chốt thật — khách đó ≥61 điểm theo model (10đ) |
| Dùng được ngay | 15 | Form đã cài thật vào chatbot hoặc landing page — có ảnh chứng minh (10đ; chỉ nộp file word chưa cài = 3đ); Follow-up Rule mọi ô đều có con số thời hạn + tên người thật (5đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Model 25-30 tiêu chí "cho chắc": −5đ — không ai vận hành nổi, quá 15 tiêu chí là trừ.
2. Chấm điểm nhưng KHÔNG có hành động khác nhau theo nhóm (Nóng và Lạnh đều "nhắn tin hỏi thăm"): −10đ — điểm mà không đổi hành vi là trang trí.
3. Câu hỏi ngân sách hỏi trần trụi "Chị có bao nhiêu tiền?": −5đ.
4. Điểm trong CRM là số AI trả về nhưng không lưu phần giải thích: −5đ (mất khả năng kiểm tra).
5. Khách điển hình đã chốt chấm theo model chỉ được 40 điểm mà không chỉnh model: −10đ (model không phản ánh thực tế mà vẫn nộp).

---

## 11. ❓ FAQ & Lỗi Thường Gặp

**Hỏi 1: "DN tôi mỗi tháng chỉ 20-30 lead, có cần scoring không hay cứ chăm hết?"**
Đáp: Càng ít lead càng cần — vì mỗi lead nóng bị bỏ quên là % doanh thu lớn. Với 20-30 lead, giá trị của scoring không phải "bỏ bớt lead" mà là THỨ TỰ và THỜI HẠN: ai gọi trong 1h, ai được phép để 3 ngày. Chị Quỳnh 100 điểm bị quên 5 ngày chính là ca này.

**Hỏi 2: "Điểm số +40, +25 lấy đâu ra, có nghiên cứu gì không?"**
Đáp: Là quy ước khởi điểm hợp lý theo mức độ cam kết của hành vi (đặt lịch > hỏi giá > tải tài liệu). Model đúng dần nhờ SOP-17C: 2 tuần đối chiếu với ca chốt/mất thật rồi chỉnh. Sai số ban đầu là bình thường — nhất quán quan trọng hơn chính xác.

**Hỏi 3: "Khách Việt hay ngại nói ngân sách, câu 4 trong form có làm khách bỏ form không?"**
Đáp: Hỏi khoảng chọn + câu đệm lý do thì tỷ lệ trả lời cao. Nếu vẫn lo: để câu ngân sách là KHÔNG bắt buộc — khách bỏ qua thì không cộng điểm phần đó, nhưng khách TRẢ LỜI thì cực kỳ đáng giá. Đừng vì 20% khách ngại mà bỏ dữ liệu của 80% còn lại.

**Hỏi 4: "AI chấm khác tôi nghĩ thì tin ai?"**
Đáp: Đọc phép cộng chi tiết của AI trước. AI sai kiểu 1: thiếu thông tin (bạn biết khách này là bạn của khách VIP, AI không biết) → bổ sung ghi chú vào CRM rồi chấm lại. AI sai kiểu 2: model thiếu tiêu chí (ca cô Lan Anh — khách cũ) → sửa model. Bạn "cảm thấy" khác mà không chỉ ra được thuộc kiểu nào → khả năng cao trực giác đang thiên vị "khách dễ nói chuyện".

**Hỏi 5: "Lead âm điểm (im 7 ngày liên tục) thì xoá khỏi CRM à?"**
Đáp: Không xoá (nguyên tắc archive). Rơi xuống 🔵 Lạnh → chuyển trạng thái "Chăm sóc lại", để remarketing và chiến dịch tái kích hoạt định kỳ lo. Chi phí bằng 0, thỉnh thoảng vẫn nở ra đơn.

**Hỏi 6: "MQL/SQL tôi cứ lẫn lộn, có cần nhớ không?"**
Đáp: Không cần nhớ thuật ngữ — nhớ ranh giới hành động: dưới 60 điểm = việc của MARKETING (content nuôi, bot chăm), từ 61 = việc của SALE (người thật nhắn/gọi). Nói với đội bằng tiếng Việt: "lead nuôi" và "lead gọi".

**Lỗi thường gặp:**
1. **Chấm điểm một lần rồi để mốc** (lead có hành vi mới nhưng điểm không đổi) → Phát hiện: cột Điểm không đổi cả tuần dù ghi chú có tương tác mới → Sửa: gắn chấm điểm vào SOP cuối ngày (SOP-17A) — chấm là việc hàng ngày, không phải bài tập một lần.
2. **Đưa tiêu chí không đo được vào model** ("khách có vẻ thiện chí") → Phát hiện: hai người chấm cùng lead ra hai số khác nhau → Sửa: mỗi tiêu chí phải trả lời được bằng CÓ/KHÔNG từ dữ liệu trong CRM.
3. **Follow-up Rule viết xong không ai làm theo** → Phát hiện: lead 🔴 phát sinh hôm qua, cột "Lần liên hệ gần nhất" vẫn trống → Sửa: rule phải có TÊN người + con số giờ, và chủ DN soi đúng 1 chỉ số này trong nghi thức thứ 2 (SOP-15C): "có lead Rất nóng nào quá hạn 1h không?"

---

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 16 — AI Chatbot & Tư Vấn 24-7]] — câu trả lời khách đưa cho chatbot (nhu cầu, khung giờ, phản ứng với giá) chính là dữ liệu hành vi để chấm điểm; Qualification Form hôm nay cài ngược vào bot.
- Ngày sau: [[Ngày 18 — Sales Script & Consulting Playbook]] — điểm và phần "phản đối dự đoán" của từng lead quyết định sale mở cuộc tư vấn thế nào; lead Rất nóng có kịch bản vào thẳng vấn đề, lead Ấm có kịch bản khai thác từ đầu.
- Tài sản hôm nay được dùng lại: **Ngày 20** (Follow-up Rule 4 nhóm là bộ não của chuỗi follow-up tự động — mỗi nhóm một chuỗi tin khác nhau), **Ngày 21** (demo luồng: bot hỏi → chấm điểm → sale nhận lead nóng), **Ngày 25-26** (tỷ lệ chốt theo nhóm điểm là chỉ số trên dashboard đo lường).
- Tư duy xuyên suốt: scoring biến câu hỏi "hôm nay chăm ai?" từ cảm tính thành con số — đây là điều kiện để tuần 4 tự động hoá được việc phân việc cho người và cho máy.
