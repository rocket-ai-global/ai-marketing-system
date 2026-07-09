---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 4
day: 23
core-output: "KPI List 3 nhóm (≤15 chỉ số), KPI Dashboard V1 trên Google Sheets có dữ liệu thật, Data Source Map, Weekly AI Report Template"
---

# Ngày 23 — KPI Dashboard

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Dashboard dùng khung CÓ SẴN `03. Areas/Analytics & Reporting/` (6 miền đo + Báo Cáo Ngày/Tuần/Quý): copy file `[Mẫu]`, bỏ tiền tố, đổi kỳ — không dựng sheet mới.

> Hôm nay doanh nghiệp của bạn có một bảng điều khiển: mỗi sáng thứ 2 nhìn 1 màn hình 5 phút là biết tuần trước kiếm được bao nhiêu, lead rơi ở đâu, và tuần này cần bơm lực vào chỗ nào — thay vì điều hành bằng cảm giác.

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay:

**Core Output (bắt buộc — điều kiện qua ngày):**
- **KPI List (danh sách chỉ số hiệu suất chính)**: tối đa 15 chỉ số chia 3 nhóm Marketing / Sales / Chăm sóc khách hàng, mỗi chỉ số có định nghĩa cách đếm + nguồn lấy số + tần suất cập nhật.
- **KPI Dashboard (bảng điều khiển) Version 1** trên Google Sheets: đã đổ dữ liệu THẬT (hoặc ước lượng trung thực) của 4 tuần gần nhất, có công thức tự tính các tỷ lệ chuyển đổi.
- **Data Source Map (bản đồ nguồn dữ liệu)**: bảng chỉ rõ mỗi con số lấy từ đâu, ai nhập, mất bao nhiêu phút.
- **Weekly AI Report Template (mẫu báo cáo AI hàng tuần)**: prompt đã cá nhân hóa, dán số liệu tuần vào là ra báo cáo phân tích.

**Bonus Output (nâng cao):**
- **Decision Dashboard (bảng ra quyết định)**: thêm cột ngưỡng đèn 🟢/🟡/🔴 cho từng chỉ số + hành động định sẵn khi đèn đỏ.
- Biểu đồ phễu (funnel chart) trực quan trong Sheets.

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Vì sao chủ SME cần dashboard, và dashboard KHÔNG phải là gì (5')
- **Ý chính:** "Cái gì không đo được thì rất khó tối ưu." Dashboard = đồng hồ taplo ô tô của doanh nghiệp: không lái xe bằng cách mở nắp capo nhìn động cơ, mà nhìn 5-7 đồng hồ chính.
- **Analogy Sen Spa:** trước khóa học, khi được hỏi "tháng này bao nhiêu lead?", chị Lan trả lời "chắc cũng nhiều, Facebook thấy tương tác tốt". Cảm giác "tương tác tốt" của Lan tháng trước = 45 lead nhưng chỉ 5 khách chốt liệu trình — tiền nằm ở chỗ Lan KHÔNG nhìn thấy.
- Dashboard KHÔNG phải: phần mềm đắt tiền, báo cáo 20 trang, hay việc của "người làm data". Nó là 1 tab Google Sheets, nhập 10 phút/ngày.

### Khối 2 — Chọn KPI: quy tắc "15 chỉ số, 3 tầng phễu" (8')
- **Ý chính:** SME chết vì đo QUÁ NHIỀU chứ không phải quá ít. Tối đa 15 chỉ số, bám đúng phễu của ngành dịch vụ tư vấn: **Lead → Booking (đặt lịch hẹn) → Show (đến nơi) → Chốt → Tái mua**.
- Bộ KPI chuẩn ngành dịch vụ tư vấn (giảng bằng bảng Sen Spa):

| Nhóm | Chỉ số | Cách đếm (định nghĩa chặt) |
|---|---|---|
| Marketing | Số bài đăng | Bài đăng lên trong tuần, mọi kênh |
| Marketing | Lượt tiếp cận (reach) | Từ trình quản lý trang FB, cộng các bài trong tuần |
| Marketing | Số inbox mới | Hội thoại MỚI trong tuần (không đếm khách cũ nhắn lại) |
| Marketing | Số lead | Người để lại SĐT (form/inbox/gọi) — có SĐT mới tính lead |
| Marketing | Chi phí/lead | Tiền ads ÷ số lead từ ads (chỉ tính khi chạy ads) |
| Marketing | Tỷ lệ chuyển đổi landing page | Lead từ form ÷ lượt xem trang |
| Sales | Số lead được liên hệ trong 24h | Đếm từ CRM, cột "Ngày liên hệ đầu" |
| Sales | Số booking | Lịch hẹn được xác nhận |
| Sales | Tỷ lệ booking | Booking ÷ lead |
| Sales | Số show | Khách thực sự đến spa |
| Sales | Số chốt + Doanh thu | Đơn ký trong tuần; doanh thu THU VỀ (tiền vào tài khoản) |
| Sales | Tỷ lệ chốt · AOV | Chốt ÷ show · Doanh thu ÷ số đơn |
| Chăm sóc | Tỷ lệ tái mua/tái đặt lịch | Khách cũ quay lại trong tháng ÷ tổng khách cũ đến hạn |
| Chăm sóc | Số referral (khách được giới thiệu) | Lead có nguồn = "giới thiệu" |
| Chăm sóc | Điểm hài lòng · Số khiếu nại | Trung bình khảo sát sau buổi (1-5) · đếm ca phàn nàn |

- **Cách giảng định nghĩa chặt:** hỏi lớp "inbox hỏi giá rồi im — có tính là lead không?". Tranh luận 1 phút rồi chốt: LEAD = CÓ SĐT. Không định nghĩa chặt thì tuần sau mỗi nhân viên đếm một kiểu, dashboard thành rác.

### Khối 3 — Thiết kế dashboard 1 màn hình (7')
- Cấu trúc chuẩn 4 vùng trên 1 tab Sheets:
  1. **Vùng tổng quan (trên cùng):** Doanh thu tuần · Lead tuần · Tỷ lệ booking · Tỷ lệ chốt — 4 số to.
  2. **Vùng phễu:** bảng Lead → Booking → Show → Chốt theo tuần, kèm % chuyển đổi từng nấc.
  3. **Vùng kênh:** lead chia theo nguồn (FB organic / FB ads / Giới thiệu / Khác).
  4. **Vùng chăm sóc:** tái mua, referral, hài lòng, khiếu nại.
- Nguyên tắc: **cột = tuần, hàng = chỉ số** (nhìn ngang thấy xu hướng 4 tuần); số nhập tay tô nền vàng nhạt, số công thức tự tính để trắng — ai cũng biết ô nào được đụng vào.

### Khối 4 — Data Source Map: số ở đâu ra và ai nhập (5')
- **Ý chính:** dashboard chết vì KHÔNG AI NHẬP SỐ, không phải vì thiếu công thức. Mỗi chỉ số phải trả lời 4 câu: *Lấy từ đâu? Ai nhập? Khi nào? Mất mấy phút?*
- Ví dụ Sen Spa: reach/inbox — Hà lấy từ Meta Business Suite chiều thứ 7, 10 phút; lead/booking/show/chốt — tự đếm bằng công thức COUNTIF từ CRM Sheets (Ngày 16 + automation Ngày 22 đã ghi tự động); doanh thu — Lan đối chiếu tài khoản ngân hàng chiều thứ 7, 10 phút. **Tổng chi phí vận hành dashboard: ~25 phút/tuần.**
- Chốt tư duy: automation Ngày 22 chính là "ống dẫn số" — càng nhiều luồng tự ghi vào CRM, dashboard càng ít phải nhập tay.

### Khối 5 — Dùng AI đọc số thay cho chủ DN (đệm cho Ngày 24) (3')
- Dashboard trả lời "CHUYỆN GÌ đang xảy ra". AI report trả lời "TẠI SAO và LÀM GÌ". Hôm nay chỉ cần cài xong Weekly AI Report Template và chạy thử 1 lần; phân tích sâu để dành Ngày 24.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 22 | Chiếu 2 video test automation tốt nhất; chỉ ra 1 lỗi hay gặp nhất trong bài nộp (thường: trigger mơ hồ). Câu mở màn: "Không nhìn sổ sách — tuần trước DN bạn có bao nhiêu lead? Viết ra giấy." (chốc nữa so với số thật) |
| 25' | Giảng kiến thức trọng tâm | 5 khối ở mục 2. Trọng tâm: định nghĩa chặt từng chỉ số + quy tắc 15 chỉ số |
| 30' | Demo live trên Sen Spa | Dựng dashboard từ template trắng → đổ 4 tuần dữ liệu → công thức % → chạy Weekly AI Report (kịch bản mục 4) |
| 15' | Học viên làm tại chỗ + Q&A | Mỗi người khoanh 12-15 chỉ số của mình trên Template 1 và điền Data Source Map cho 5 chỉ số đầu; trainer duyệt định nghĩa "lead" của từng người |
| 10' | Giao bài tập | Deliverable + rubric + deadline. Nhấn mạnh: "Số ước lượng trung thực vẫn hơn ô trống — điền 'khoảng 40, sẽ đo chính xác từ tuần này' là hợp lệ" |

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

> Dữ liệu demo: 4 tuần gần nhất của Sen Spa (chuẩn bị sẵn trong template, trainer chỉ việc dán).

**Bước 1 (5') — Mở Template 2, giới thiệu 4 vùng, dán dữ liệu 4 tuần.**
- Làm gì: dán bảng số Sen Spa vào vùng nhập liệu (nền vàng).
- Công cụ: Google Sheets.
- Kết quả trông như thế nào:

| Chỉ số | T1 | T2 | T3 | T4 |
|---|---|---|---|---|
| Bài đăng | 5 | 6 | 5 | 6 |
| Reach | 12.400 | 15.100 | 9.800 | 14.200 |
| Inbox mới | 32 | 38 | 25 | 35 |
| Lead (có SĐT) | 11 | 13 | 8 | 13 |
| Liên hệ trong 24h | 7 | 9 | 8 | 13 |
| Booking | 4 | 5 | 3 | 6 |
| Show | 3 | 4 | 2 | 5 |
| Chốt liệu trình | 1 | 2 | 1 | 2 |
| Doanh thu (tr) | 38 | 52 | 31 | 55 |
| Khách cũ tái đặt lịch | 6 | 5 | 7 | 6 |
| Lead nguồn giới thiệu | 2 | 3 | 1 | 3 |

**Bước 2 (8') — Viết công thức tỷ lệ, cả lớp làm theo từng phím.**
- Làm gì: tỷ lệ booking `=Booking/Lead`, tỷ lệ show `=Show/Booking`, tỷ lệ chốt `=Chốt/Show`, format %. Dùng COUNTIF đếm lead từ CRM: `=COUNTIFS(CRM!C:C,">="&ngày_đầu_tuần,CRM!C:C,"<="&ngày_cuối_tuần)` — giải thích chậm: "đếm số dòng trong tab CRM có ngày tạo nằm trong tuần".
- Kết quả: hàng % hiện ra — booking/lead của Sen Spa 4 tuần: 36% → 38% → 38% → 46%. Trainer chỉ vào tuần 4: "Tuần Sen Spa bật automation liên hệ 24h (Ngày 22), tỷ lệ booking nhảy lên 46%. Số kể chuyện đấy."

**Bước 3 (5') — Điền Data Source Map trước mặt lớp.**
- Làm gì: điền 4 câu (từ đâu/ai/khi nào/mấy phút) cho từng hàng. Chỉ ra hàng nào automation Ngày 22 đã tự ghi (lead, liên hệ 24h) — không ai phải nhập.
- Kết quả: bảng Data Source Map hoàn chỉnh, tổng thời gian nhập tay = 25'/tuần.

**Bước 4 (9') — Chạy Weekly AI Report lần đầu.**
- Làm gì: copy Prompt 3 (đã điền sẵn cho Sen Spa) → dán bảng 4 tuần vào chỗ {{dữ liệu}} → chạy trong RocketAgent AI Assistant (hoặc ChatGPT/Claude Projects).
- Kết quả trông như thế nào: báo cáo 1 trang gồm — Tóm tắt tuần 4 (doanh thu 55tr, +77% so T3); 2 điểm sáng (tỷ lệ booking 46% cao nhất tháng; reach hồi phục); 2 điểm tối (tỷ lệ chốt kẹt ~40%, tuần 3 sụt cả phễu do chỉ đăng 5 bài và reach giảm); 1 cảnh báo (lead giới thiệu chỉ 1-3/tuần dù khách hài lòng — chưa có cơ chế xin referral); 3 việc tuần tới.
- Trainer chốt: "5 phút AI đọc số thay bạn. Ngày 24 ta sẽ dạy AI đọc SÂU hơn nữa."

**Bước 5 (3') — Bonus: bật ngưỡng đèn.**
- Làm gì: thêm cột "Ngưỡng" + định dạng có điều kiện: tỷ lệ booking <30% → đỏ; 30-40% → vàng; >40% → xanh.
- Kết quả: dashboard tự đổi màu khi dán số tuần mới.

> **Thích ứng ngành khác:** Nha khoa — thêm chỉ số "tỷ lệ no-show" (khách hẹn không đến) và "kế hoạch điều trị được chấp nhận ÷ kế hoạch tư vấn". Giáo dục — phễu là Lead → Học thử → Ghi danh; thêm "tỷ lệ hoàn thành khóa". Gym — thêm "tỷ lệ gia hạn" và "số buổi check-in/hội viên/tuần" (chỉ báo sớm của rời bỏ). Coaching — phễu Lead → Cuộc gọi khám phá → Ký hợp đồng. Khung 4 vùng và quy tắc 15 chỉ số giữ nguyên.

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

**Cụm A — Chốt KPI List (30'):**
- [ ] Từ Template 1, gạch bỏ chỉ số không hợp DN mình, giữ 12-15 chỉ số đủ 3 nhóm (10')
- [ ] Viết định nghĩa cách đếm cho TỪNG chỉ số — chuẩn "nhân viên mới đọc là đếm đúng" (15')
- [ ] Đánh dấu ⭐ vào 4 chỉ số sẽ đặt ở vùng tổng quan (5')

**Cụm B — Dựng Dashboard V1 (50'):**
- [ ] Copy Template 2 về Drive của mình, sửa tên chỉ số theo KPI List (10')
- [ ] Đổ dữ liệu 4 tuần gần nhất: lấy từ CRM/Meta Suite/sổ thu chi; số không có thì ước lượng trung thực + đánh dấu `(ước tính)` (25')
- [ ] Kiểm tra công thức %: đúng công thức, không lỗi chia 0, format % (10')
- [ ] Tô nền vàng ô nhập tay, khóa hàng tiêu đề (5')

**Cụm C — Data Source Map + AI Report (40'):**
- [ ] Điền Data Source Map đủ 4 câu cho mọi chỉ số; tính tổng phút/tuần — nếu >45' thì cắt bớt chỉ số (15')
- [ ] Cá nhân hóa Prompt 3 (điền bối cảnh DN mình), lưu thành Weekly AI Report Template của DN (10')
- [ ] Chạy AI Report với số 4 tuần vừa đổ, đọc và ghi lại 1 insight (điều nhận ra) khiến bạn bất ngờ (15')

Tổng Core: ~2h. **Bonus (+30'):** thêm ngưỡng đèn 🟢🟡🔴 + viết hành động định sẵn khi đèn đỏ cho 4 chỉ số ⭐; vẽ biểu đồ phễu.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Dựng KPI Dashboard V1 cho doanh nghiệp của bạn với dữ liệu 4 tuần gần nhất, kèm KPI List có định nghĩa, Data Source Map, và chạy Weekly AI Report đầu tiên.

**Deliverable nộp (vào thread cohort, deadline 23h59 hôm nay):**
1. `[Tên DN] — Ngày 23 — KPI Dashboard V1` (link Google Sheets, quyền xem cho mentor; gồm tab Dashboard + tab KPI List + tab Data Source Map)
2. `[Tên DN] — Ngày 23 — AI Report Tuần Đầu` (file/ảnh báo cáo AI đã chạy + 3 dòng tự viết: "1 insight bất ngờ nhất với tôi là… vì trước giờ tôi tưởng…")

Bonus nộp thêm: ảnh Decision Dashboard có ngưỡng đèn.

## 7. 📄 Template Đi Kèm

**Template 1 — KPI Menu ngành dịch vụ tư vấn** (bảng chọn)
25 chỉ số chia 3 nhóm, mỗi chỉ số: `Tên · Định nghĩa cách đếm · Nguồn lấy · Tần suất · Dành cho ai (mọi DN / có chạy ads / có landing page)`. Học viên gạch–giữ thay vì nghĩ từ đầu. Có cột ví dụ giá trị thật của Sen Spa.

**Template 2 — KPI Dashboard V1** (Google Sheets, 4 tab)
- Tab `Dashboard`: 4 vùng (Tổng quan / Phễu / Kênh / Chăm sóc), cột theo tuần, công thức % viết sẵn, định dạng có điều kiện cài sẵn (tắt mặc định).
- Tab `KPI List`: đổ từ Template 1.
- Tab `Data Source Map`: các cột `Chỉ số · Lấy từ đâu · Ai nhập · Khi nào · Phút/tuần · Tự động hay tay`.
- Tab `Sen Spa (mẫu)`: toàn bộ dashboard Sen Spa 4 tuần điền sẵn làm chuẩn đối chiếu.

**Template 3 — Weekly AI Report Template** (file text)
Prompt 3 dạng khung + bản đã điền Sen Spa + ô trống dán số liệu, kèm hướng dẫn 3 bước: mở dashboard → copy bảng tuần → dán vào prompt → chạy.

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Chọn bộ KPI phù hợp doanh nghiệp

```
[ROLE] Bạn là giám đốc vận hành (COO) dày dạn của các chuỗi dịch vụ SME Việt Nam, nổi tiếng vì bắt doanh nghiệp đo ÍT chỉ số nhưng đúng chỉ số.

[CONTEXT] Doanh nghiệp: {{tên, ngành, mô tả 2 câu}}. Phễu bán hàng: {{các nấc phễu thực tế}}. Kênh marketing đang chạy: {{FB organic/ads/Zalo/giới thiệu…}}. Người sẽ nhập số: {{ai, rành công nghệ mức nào}}. Thời gian tối đa cho việc đo lường: 30 phút/tuần.

[TASK] Chọn cho tôi bộ KPI tối đa 15 chỉ số chia 3 nhóm (Marketing / Sales / Chăm sóc), và chỉ ra 4 chỉ số quan trọng nhất đặt lên vùng tổng quan.

[INPUT] Menu 25 chỉ số chuẩn: {{dán Template 1}}.

[OUTPUT] Bảng: Nhóm · Chỉ số · Định nghĩa cách đếm (1 câu, chặt đến mức nhân viên mới đếm đúng) · Nguồn lấy số · Vì sao DN này cần nó (1 câu). Cuối bảng: 4 chỉ số ⭐ + lý do; danh sách chỉ số tôi NÊN BỎ dù thấy hấp dẫn + lý do.

[CONSTRAINT] Không quá 15 chỉ số — nếu muốn thêm phải chỉ ra chỉ số nào bỏ đi. Không đề xuất chỉ số cần công cụ trả phí mới đo được. Ưu tiên chỉ số automation/CRM đã tự ghi được. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{phễu}}` = "Lead (FB + giới thiệu) → Booking → Show tại spa → Tư vấn → Chốt liệu trình 12-15tr → Tái mua/upsell"; `{{người nhập số}}` = "Hà, lễ tân, dùng tốt điện thoại, mới học Google Sheets". Kết quả kỳ vọng: đúng bảng 15 chỉ số ở mục 2, 4 chỉ số ⭐ = Doanh thu, Lead, Tỷ lệ booking, Tỷ lệ chốt.

### Prompt 2 — Thiết kế cấu trúc dashboard trên Google Sheets

```
[ROLE] Bạn là chuyên gia Google Sheets chuyên dựng dashboard cho người không rành công nghệ.

[CONTEXT] Tôi có KPI List sau: {{dán KPI List đã chốt}}. CRM của tôi là 1 Google Sheets có các cột: {{liệt kê cột CRM: Ngày tạo, Tên, SĐT, Nguồn, Trạng thái, Ngày liên hệ đầu, Ngày hẹn, Giá trị đơn…}}.

[TASK] Thiết kế cấu trúc tab Dashboard: bố cục 4 vùng (Tổng quan / Phễu / Kênh / Chăm sóc), cột theo tuần, và viết giúp tôi công thức cho các ô tự tính.

[INPUT] KPI List + cấu trúc CRM ở trên.

[OUTPUT] (1) Sơ đồ bố cục dạng bảng chữ (ô nào đặt gì); (2) danh sách công thức: ô → công thức đầy đủ (COUNTIFS/SUMIFS từ tab CRM) → giải thích 1 câu bằng lời thường; (3) danh sách ô nhập tay cần tô vàng; (4) hướng dẫn 3 bước cài định dạng có điều kiện cho 4 chỉ số chính.

[CONSTRAINT] Chỉ dùng hàm cơ bản: COUNTIF(S), SUMIF(S), IFERROR, chia. Mọi công thức % bọc IFERROR để không hiện lỗi khi chia 0. Không dùng QUERY, không App Script. Giải thích như cho người lần đầu viết công thức.
```

**Ví dụ đã điền (Sen Spa):** cột CRM = "A: Ngày tạo · B: Tên · C: SĐT · D: Nguồn · E: Trạng thái (Mới/Đã liên hệ/Booking/Show/Chốt/Không mua) · F: Ngày liên hệ đầu · G: Ngày hẹn · H: Giá trị đơn". Công thức mẫu kỳ vọng: `=IFERROR(COUNTIFS(CRM!$E:$E,"Booking",CRM!$A:$A,">="&B$2,CRM!$A:$A,"<="&B$3)/B$6,"")`.

### Prompt 3 — Weekly AI Report (báo cáo tuần tự động) ⭐ template chính

```
[ROLE] Bạn là giám đốc phân tích kinh doanh riêng của tôi — chủ một doanh nghiệp {{ngành}} quy mô nhỏ, bận, cần kết luận thẳng, không cần lý thuyết.

[CONTEXT] Doanh nghiệp: {{tên + mô tả 2 câu + AOV + sản phẩm chính}}. Phễu chuẩn: {{các nấc}}. Mức chuẩn (benchmark) nội bộ tôi kỳ vọng: {{ví dụ: tỷ lệ booking ≥35%, tỷ lệ chốt ≥40%, liên hệ trong 24h = 100%}}.

[TASK] Đọc số liệu tuần này (so với 3 tuần trước) và viết báo cáo tuần cho tôi.

[INPUT] Bảng KPI 4 tuần:
{{dán bảng từ dashboard, cột = tuần}}
Ghi chú định tính tuần này (nếu có): {{ví dụ: tuần này có 1 KTV nghỉ, chạy thêm 1 bài ads}}

[OUTPUT] Báo cáo đúng 6 mục, tổng ≤1 trang:
1. TÓM TẮT 3 CÂU: doanh thu, xu hướng chung, điều đáng chú ý nhất.
2. 2-3 ĐIỂM SÁNG: chỉ số nào tốt lên, kèm số cụ thể và % thay đổi.
3. 2-3 ĐIỂM TỐI: chỉ số nào xấu đi hoặc dưới benchmark, kèm số.
4. NGHI VẤN NGUYÊN NHÂN: với mỗi điểm tối, nêu 1-2 giả thuyết VÀ chỉ rõ cần kiểm tra thêm dữ liệu gì để xác nhận — không khẳng định bừa.
5. 3 VIỆC TUẦN TỚI: cụ thể, mỗi việc ghi rõ nhắm vào chỉ số nào.
6. CẢNH BÁO: chỉ số nào lệch >30% so trung bình 3 tuần trước (tăng hay giảm đều nêu).

[CONSTRAINT] Mọi nhận định phải kèm con số. Cấm câu sáo rỗng kiểu "cần cố gắng hơn". Nếu dữ liệu thiếu hoặc mâu thuẫn, nói thẳng ở đầu báo cáo. Không đề xuất việc cần >2h/ngày hoặc cần thuê thêm người. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** benchmark = "tỷ lệ booking ≥35%, show ≥75%, chốt ≥40%, 100% lead được liên hệ trong 24h"; ghi chú tuần = "tuần này bật automation follow-up từ thứ 3". Output kỳ vọng: báo cáo như Bước 4 mục Demo.

### Prompt 4 — Cài ngưỡng đèn cảnh báo (Bonus)

```
[ROLE] Bạn là cố vấn vận hành thực chiến cho SME dịch vụ.

[CONTEXT] Doanh nghiệp: {{tên + ngành + AOV}}. Bộ KPI và số trung bình 4 tuần: {{dán bảng}}.

[TASK] Đặt ngưỡng đèn 🟢/🟡/🔴 cho từng chỉ số và viết "hành động định sẵn" khi đèn đỏ.

[INPUT] Bảng KPI ở trên + benchmark ngành nếu bạn biết (nói rõ đó là ước lượng chung, không phải chuẩn tuyệt đối).

[OUTPUT] Bảng: Chỉ số · Ngưỡng 🟢 · Ngưỡng 🟡 · Ngưỡng 🔴 · Hành động định sẵn khi 🔴 (1 câu, bắt đầu bằng động từ, chỉ rõ ai làm) · Căn cứ đặt ngưỡng (từ số trung bình của tôi hay benchmark ngành).

[CONSTRAINT] Ngưỡng phải xuất phát từ số THẬT của tôi (ví dụ 🔴 = thấp hơn 20% so trung bình 4 tuần), không bê nguyên benchmark ngành. Hành động định sẵn phải làm được trong tuần, không phải dự án. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** hành động khi tỷ lệ booking 🔴 (<30%) = "Hà nghe lại 5 cuộc gọi lead gần nhất, đối chiếu kịch bản booking Ngày 18, báo Lan điểm lệch trong ngày thứ 2".

## 9. 📋 SOP Thao Tác

**SOP-23 · Vận hành dashboard hàng tuần:**

| Khi nào | Ai làm | Input → Các bước → Output |
|---|---|---|
| Hàng ngày, 5' cuối ngày | Lễ tân/sale (Hà) | CRM + sổ hẹn → cập nhật trạng thái lead trong CRM (nguồn số tự chảy về dashboard) → Output: CRM đúng đến cuối ngày |
| Thứ 7, 25' | Người nhập số (Hà) + Chủ DN (Lan phần doanh thu) | Meta Suite + CRM + tài khoản ngân hàng → điền cột tuần mới theo Data Source Map → soát ô nào trống/bất thường → Output: cột tuần mới đầy đủ |
| Sáng thứ 2, 15' | Chủ DN (Lan) | Dashboard + Weekly AI Report Template → dán bảng 4 tuần vào prompt → chạy → đọc → chốt 3 việc tuần → dán 3 việc vào nhóm Zalo nội bộ → Output: báo cáo tuần + 3 việc có tên người phụ trách |
| Cuối tháng, 15' | Chủ DN | 4 báo cáo tuần → xem lại ngưỡng đèn có còn hợp lý → chỉnh ngưỡng theo mặt bằng mới → Output: ngưỡng cập nhật |

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Dashboard có đủ 4 vùng, 12-15 chỉ số đủ 3 nhóm (10đ); có dữ liệu đủ 4 cột tuần, ô thiếu ghi rõ `(ước tính)` hoặc `(bắt đầu đo từ tuần này)` — ô trống không chú thích trừ 1đ/ô (10đ); có tab KPI List + tab Data Source Map + đã chạy AI Report lần 1 (10đ) |
| Chất lượng & độ sâu | 30 | 100% chỉ số có định nghĩa cách đếm chặt — mentor test bằng câu "nhân viên mới đọc xong đếm đúng không?" (10đ); công thức % đúng và chạy được, có IFERROR, không hard-code (gõ số đè lên ô công thức) (10đ); Data Source Map đủ 4 câu mọi chỉ số, tổng ≤45'/tuần (10đ) |
| Cá nhân hoá vào DN thật | 25 | Số liệu là của DN mình, các nấc phễu đúng thực tế DN — không bê nguyên phễu spa nếu là ngành khác (10đ); 4 chỉ số ⭐ hợp lý với chỗ đau đã nêu từ Ngày 22 (8đ); phần "1 insight bất ngờ" là nhận định thật, có dẫn con số từ dashboard (7đ) |
| Dùng được ngay | 15 | Link Sheets mở được, đúng quyền xem (4đ); ô nhập tay tô vàng + hàng tiêu đề đã khóa (4đ); Weekly AI Report Template đã cá nhân hóa và lưu sẵn, có ghi tên người + lịch chạy trong SOP (7đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Tham 25+ chỉ số "cho đủ" — vi phạm quy tắc 15 (−5đ nhóm 2, mentor yêu cầu cắt).
2. Định nghĩa lỏng: "Lead = người quan tâm" (−3đ/chỉ số, nhóm 2).
3. Dashboard trắng tinh, hẹn "tuần sau có số" — sai tinh thần bài: ước lượng trung thực vẫn hơn (−10đ nhóm 1).
4. Copy nguyên số Sen Spa làm số của mình (−10đ nhóm 3, yêu cầu làm lại phần dữ liệu).
5. AI Report chạy bằng prompt gốc chưa điền bối cảnh DN → báo cáo chung chung (−5đ nhóm 4).

## 11. ❓ FAQ & Lỗi Thường Gặp

**FAQ:**
1. *"Tôi không có số 4 tuần trước, giờ mới bắt đầu đo?"* — Điền 3 loại: số tra lại được (doanh thu từ tài khoản ngân hàng, bài đăng đếm trên page, inbox trong Meta Suite tra được 30 ngày); số ước lượng trung thực ghi `(ước tính)`; số chịu thì ghi `bắt đầu đo tuần này`. Dashboard sống từ hôm nay quan trọng hơn quá khứ hoàn hảo.
2. *"Sao không dùng Looker Studio/Power BI cho chuyên nghiệp?"* — Vì người vận hành là bạn và lễ tân, không phải data analyst (chuyên viên phân tích dữ liệu). Google Sheets đủ cho SME <50 nhân sự; khi nào 25'/tuần nhập liệu thành 2h/tuần thì mới đáng nâng cấp. Nâng tool trước khi có thói quen đọc số = mua máy chạy bộ đắt tiền để treo quần áo.
3. *"Doanh thu tính lúc khách ký liệu trình hay lúc tiền về?"* — Khóa này chuẩn hóa: **doanh thu = tiền THU VỀ trong tuần**. Khách ký liệu trình 12tr trả trước 6tr → tuần này ghi 6tr. Muốn theo dõi cả giá trị ký thì thêm 1 hàng riêng "Giá trị hợp đồng ký mới" — không trộn hai khái niệm vào một ô.
4. *"Khách vừa từ ads vừa được bạn giới thiệu — tính nguồn nào?"* — Quy ước "nguồn chạm cuối trước khi để lại SĐT" và ghi quy ước đó vào KPI List. Quan trọng là NHẤT QUÁN, không phải tuyệt đối đúng.
5. *"Nhân viên có nên thấy dashboard không?"* — Nên, trừ hàng lợi nhuận nếu bạn chưa muốn. Ở Sen Spa, Hà thấy tỷ lệ booking của chính mình mỗi tuần — con số minh bạch thay đổi hành vi nhanh hơn mọi cuộc họp nhắc nhở.
6. *"Bao lâu thì số liệu bắt đầu 'nói' được điều gì đó?"* — Xu hướng cần tối thiểu 4 điểm dữ liệu (4 tuần). Tháng đầu đừng vội kết luận từ 1 tuần xấu — hãy dùng để kiểm tra thói quen nhập số đã chạy chưa.

**Lỗi thường gặp:**
1. **Gõ số đè lên ô công thức.** Phát hiện: tỷ lệ % không đổi dù số gốc đổi; ô công thức mất dấu `=`. Sửa: tô vàng ô nhập tay ngay từ đầu, bảo vệ (protect) vùng công thức, dạy người nhập "chỉ đụng ô vàng".
2. **Mỗi người đếm một kiểu.** Phát hiện: số inbox tuần này gấp 3 tuần trước dù reach không đổi — hóa ra tuần này đếm cả khách cũ nhắn lại. Sửa: quay lại KPI List, đọc to định nghĩa trong buổi họp thứ 2, in định nghĩa dán cạnh máy lễ tân.
3. **Dashboard bỏ hoang sau 2 tuần.** Phát hiện: cột tuần mới trống vào sáng thứ 2. Sửa: gắn việc nhập số vào automation nhắc việc Ngày 22 (RocketAgent nhắc Hà 16h thứ 7); rút gọn số chỉ số nhập tay; chủ DN PHẢI dùng số trong họp thứ 2 — số được dùng thì số mới được nhập.
4. **Phễu lệch nấc — đếm booking nhiều hơn lead.** Phát hiện: tỷ lệ >100%. Sửa: kiểm tra lệch thời gian (lead tuần trước booking tuần này là bình thường — chấp nhận và ghi chú trong KPI List; theo dõi xu hướng 4 tuần thay vì soi 1 tuần).

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 22 — Automation Workflow]] · Ngày sau: [[Ngày 24 — AI Analytics & Decision Support]]
- Lên MOC: [[_MOC 28 Day AIOS]]
- Tài sản hôm nay được dùng lại ở:
  - **Ngày 24:** bảng 4 tuần trong dashboard là INPUT trực tiếp cho AI Analytics và phân tích điểm nghẽn phễu — không có dashboard hôm nay thì Ngày 24 không có gì để phân tích.
  - **Ngày 26:** Weekly AI Report Template được nâng cấp thành AI Data Analyst Agent chạy trên RocketAgent.
  - **Ngày 27:** dashboard là khối "Đo lường" trong OS Map; SOP-23 được nhúng vào Weekly Operating Rhythm (nhịp thứ 7 + sáng thứ 2).
  - **Ngày 28:** số liệu dashboard dùng để so kết quả với baseline Ngày 0 (lead/tháng, tỷ lệ booking, doanh thu) và đặt mục tiêu 90 ngày.
