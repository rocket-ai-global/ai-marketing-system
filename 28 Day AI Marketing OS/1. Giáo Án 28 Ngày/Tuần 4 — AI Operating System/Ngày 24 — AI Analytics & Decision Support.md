---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 4
day: 24
core-output: "Funnel Bottleneck Analysis trên số liệu thật, AI Analytics Report, Weekly Decision Checklist, AI Decision Prompt Pack (4 prompt)"
---

# Ngày 24 — AI Analytics & Decision Support

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Cho agent đọc `03. Areas/Analytics & Reporting/` để ra khuyến nghị tuần; thử nghiệm bằng `/thu-nghiem-ab` (có cảnh báo traffic thấp cho SME); báo cáo lưu `Báo Cáo Tuần/`.

> Hôm nay bạn biến AI thành cố vấn phân tích riêng: dashboard cho biết CHUYỆN GÌ đang xảy ra, còn hôm nay hệ thống của bạn trả lời được VÌ SAO nó xảy ra và TUẦN TỚI NÊN LÀM GÌ — bằng quy trình lặp lại được, không phải bằng linh cảm.

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay:

**Core Output (bắt buộc — điều kiện qua ngày):**
- **Funnel Bottleneck Analysis (phân tích điểm nghẽn phễu)**: xác định được ĐÚNG 1 điểm nghẽn lớn nhất trong phễu của DN mình bằng số liệu, kèm 2 giả thuyết nguyên nhân và cách kiểm chứng.
- **AI Analytics Report (báo cáo phân tích AI)**: báo cáo phân tích sâu chạy trên số liệu 4 tuần thật của DN (sâu hơn Weekly Report Ngày 23: có so nấc phễu với mức chuẩn, có giả thuyết, có kiểm chứng).
- **Weekly Decision Checklist (checklist ra quyết định hàng tuần)**: 5 câu hỏi quyết định cố định chủ DN trả lời mỗi sáng thứ 2, đã điền lần đầu.
- **AI Decision Prompt Pack (bộ prompt hỗ trợ quyết định)**: 4 prompt đã cá nhân hóa, lưu thành file dùng lại hàng tuần.

**Bonus Output (nâng cao):**
- **Business Review Meeting SOP (quy trình họp review hiệu suất)**: agenda 30 phút cố định cho họp tuần với đội ngũ.
- **AI Decision Assistant**: dựng luồng "dán số → AI phân tích → đề xuất → chủ DN duyệt" thành assistant riêng trên RocketAgent (tiền thân của AI Data Analyst Agent Ngày 26).

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Ba tầng trưởng thành dữ liệu: Nhìn → Hiểu → Quyết (5')
- **Ý chính:** Tầng 1 — Dashboard: *chuyện gì xảy ra* (Ngày 23). Tầng 2 — Analytics (phân tích): *vì sao xảy ra*. Tầng 3 — Decision support (hỗ trợ quyết định): *nên làm gì*. Đa số SME kẹt ở tầng 1: có số, nhìn số, rồi… vẫn quyết theo cảm tính.
- **Analogy Sen Spa:** dashboard báo "tỷ lệ chốt tuần này 33%, thấp hơn benchmark 40%". Phản xạ cảm tính của Lan: "chắc do khách dạo này khó" → không làm gì. Phản xạ tầng 2-3: "nghẽn ở nấc show→chốt; giả thuyết 1: khách show là loại lead nào? giả thuyết 2: ai tư vấn các ca không chốt?" → soi CRM thấy 3/5 ca không chốt do Hà tư vấn thay khi Lan bận → quyết định: Hà chỉ tư vấn khi có checklist chốt + ca >10tr chuyển Lan.
- Chốt tư duy: **AI không ra quyết định thay bạn — AI làm nhanh phần đọc số và đặt giả thuyết, bạn giữ phần QUYẾT và CHỊU TRÁCH NHIỆM.**

### Khối 2 — Đọc phễu và tìm điểm nghẽn: quy tắc "nấc rơi sâu nhất so với chuẩn" (8')
- Cách tìm nghẽn trong 3 bước:
  1. Viết phễu thành dãy số 4 tuần: Reach → Inbox → Lead → Booking → Show → Chốt.
  2. Tính % chuyển đổi từng nấc, so với mức chuẩn nội bộ (hoặc mức tham khảo ngành).
  3. Nghẽn = nấc có **độ hụt so với chuẩn × giá trị tiền** lớn nhất — không phải nấc có % thấp nhất.
- Mức tham khảo ngành dịch vụ tư vấn (nói rõ: đây là khoảng tham khảo để khởi động, số chuẩn thật là trung bình 4-8 tuần của chính DN):

| Nấc | Khoảng tham khảo | Câu hỏi chẩn đoán khi hụt |
|---|---|---|
| Reach → Inbox | 0,15–0,3% | Nội dung có gây đủ lý do để nhắn không? Có lời mời hành động (CTA) không? |
| Inbox → Lead (có SĐT) | 30–40% | Người trực có xin SĐT đúng kịch bản không? Chatbot có hỏi xin số không? |
| Lead → Booking | 30–45% | Gọi lại trong 24h chưa? Lời mời booking có lý do đủ mạnh (soi da miễn phí) không? |
| Booking → Show | 70–85% | Có nhắc lịch 24h + 2h trước không? Đặt lịch có cọc/cam kết gì không? |
| Show → Chốt | 30–50% | Ai tư vấn? Có dùng sales script Ngày 18? Khách từ chối vì gì (ghi trong CRM)? |
- **Cách giảng:** chiếu 2 phễu có cùng doanh thu nhưng nghẽn khác nhau → hỏi lớp "bơm tiền ads vào phễu nào là đốt tiền?" (phễu nghẽn ở show→chốt: thêm lead chỉ thêm lãng phí — phải sửa khâu chốt trước).

### Khối 3 — Từ phân tích đến quyết định: 5 câu hỏi cố định (7')
- **Ý chính:** quyết định chất lượng đến từ CÂU HỎI cố định, không phải từ cảm hứng. Mỗi sáng thứ 2 trả lời đúng 5 câu:
  1. **Nội dung/kênh nào TĂNG?** (cái gì đang chạy tốt → làm thêm)
  2. **Cái gì GIẢM/DỪNG?** (cái gì ngốn công sức mà không ra số)
  3. **Offer (gói chào bán) có cần CHỈNH không?** (khách từ chối vì gì — giá, thời gian, niềm tin?)
  4. **Khâu SALE cải thiện điểm nào?** (1 điểm duy nhất, đo được)
  5. **Follow-up/chăm sóc tối ưu gì?** (nhìn số tái mua, phản hồi tin nhắn)
- Mỗi câu trả lời phải có: quyết định 1 câu + căn cứ số liệu + người làm + hạn + chỉ số sẽ xác nhận sau 1-2 tuần.
- Quy tắc chống quá tải: **mỗi tuần tối đa 3 quyết định thay đổi.** Đổi 7 thứ cùng lúc = không biết thứ gì tạo ra kết quả.

### Khối 4 — Kỹ thuật làm việc với AI trên số liệu: chống ảo giác (5')
- 4 quy tắc bắt buộc khi cho AI đọc số:
  1. **Đưa đủ bối cảnh**: ngành, AOV, benchmark, ghi chú định tính tuần (KTV nghỉ, chạy ads mới…) — AI không biết những gì bạn không kể.
  2. **Bắt AI phân biệt SỰ KIỆN và GIẢ THUYẾT**: sự kiện = con số; giả thuyết = phỏng đoán nguyên nhân, phải kèm "cần kiểm tra gì để xác nhận".
  3. **Cấm AI khẳng định nguyên nhân khi thiếu dữ liệu** — ràng buộc này viết thẳng vào prompt.
  4. **Số nhỏ thì nói xu hướng, đừng nói %**: 1 chốt → 2 chốt là "+100%" nghe kịch tính nhưng vô nghĩa thống kê với mẫu nhỏ. Với SME, nhìn 4 tuần cộng dồn.

### Khối 5 — Nhịp họp review dữ liệu hàng tuần (đệm cho SOP) (3')
- Khung họp 30': 10' đọc số (chiếu dashboard + AI report) → 10' tranh luận giả thuyết → 10' chốt tối đa 3 quyết định theo checklist 5 câu, ghi tên người + hạn. Không họp quá 30' — họp dữ liệu dài là họp không có dữ liệu.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 23 | Chiếu 2 dashboard tốt nhất; đọc to 3 "insight bất ngờ" hay nhất từ bài nộp. Câu mở màn: "Nhìn dashboard của mình hôm qua, ai chỉ được ĐÚNG 1 nấc phễu đang thủng nặng nhất? Nói bằng số." |
| 25' | Giảng kiến thức trọng tâm | 5 khối ở mục 2. Trọng tâm: quy tắc tìm nghẽn khối 2 + 5 câu hỏi quyết định khối 3 |
| 30' | Demo live trên Sen Spa | Chạy trọn vòng: số 4 tuần → AI phân tích → tìm nghẽn → điền Decision Checklist → giao việc (kịch bản mục 4) |
| 15' | Học viên làm tại chỗ + Q&A | Mỗi người dán số 4 tuần của mình vào Prompt 1, chạy, và khoanh điểm nghẽn số 1; trainer duyệt từng người: "nghẽn này đáng bao nhiêu tiền/tháng?" |
| 10' | Giao bài tập | Deliverable + rubric + deadline. Nhấn mạnh: "Nộp 1 điểm nghẽn ĐÚNG đáng giá hơn 5 điểm nghẽn liệt kê cho có" |

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

> Dùng lại đúng bảng số 4 tuần của Sen Spa từ dashboard Ngày 23 (Lead 11-13-8-13, Booking 4-5-3-6, Show 3-4-2-5, Chốt 1-2-1-2, Doanh thu 38-52-31-55tr…).

**Bước 1 (7') — Chạy Prompt 1 (Funnel Bottleneck Analysis) trên số Sen Spa.**
- Làm gì: copy Prompt 1 đã điền sẵn → dán bảng 4 tuần → chạy trong RocketAgent AI Assistant (hoặc Claude/ChatGPT Projects).
- Công cụ: RocketAgent AI Assistant + dashboard Sheets mở song song.
- Kết quả trông như thế nào (tóm tắt output kỳ vọng):

```
PHỄU SEN SPA — CỘNG DỒN 4 TUẦN
Inbox 130 → Lead 45 (34,6% ~ chuẩn 30-40% ✅)
Lead 45 → Booking 18 (40% ~ chuẩn 30-45% ✅)
Booking 18 → Show 14 (77,8% ~ chuẩn 70-85% ✅)
Show 14 → Chốt 6 (42,9% ~ chuẩn 30-50% ✅) 
→ Từng nấc đều "đạt chuẩn"… NHƯNG: 45 lead/4 tuần với reach 51.500 
   = Reach→Inbox chỉ 0,25%, và ĐẦU PHỄU MỎNG là trần của mọi thứ phía sau.
ĐIỂM NGHẼN #1: lượng lead tuyệt đối thấp (11/tuần) so với công suất spa 
   (4 KTV có thể phục vụ gấp đôi số liệu trình hiện tại).
ĐIỂM NGHẼN #2 (theo tiền): Show→Chốt 42,9% nhưng 8 ca không chốt × 12tr 
   = 96tr cơ hội/4 tuần — mỗi 5 điểm % cải thiện ở đây = ~14tr/tháng.
```
- Trainer dừng lại giảng: "Thấy chưa — từng nấc đều xanh mà vẫn nghèo. Nghẽn không phải lúc nào cũng là % đỏ; có khi là TRẦN đầu phễu, có khi là nấc % vàng nhưng dính nhiều tiền nhất."

**Bước 2 (8') — Đào giả thuyết cho nghẽn Show→Chốt bằng Prompt 2.**
- Làm gì: dán thêm dữ liệu định tính từ CRM: 8 ca không chốt — lý do ghi trong CRM: 4 "để chị suy nghĩ", 2 "giá cao", 1 "nhà xa", 1 không ghi. Người tư vấn: Lan 3 ca, Hà 5 ca.
- Kết quả: AI phân ra sự kiện vs giả thuyết:
  - Sự kiện: 5/8 ca không chốt do Hà tư vấn; 4/8 lý do "suy nghĩ thêm" (từ chối mềm — thường là chưa đủ niềm tin/chưa rõ giá trị).
  - Giả thuyết A: Hà chưa dùng sales script xử lý từ chối (kiểm chứng: nghe lại ghi chú 5 ca của Hà, đối chiếu script Ngày 18).
  - Giả thuyết B: khách "suy nghĩ" không được follow-up trong 48h (kiểm chứng: soi cột follow-up của 4 ca đó trong CRM — automation Ngày 22 có chạy không).
- Trainer nhấn: AI KHÔNG nói "nguyên nhân là Hà tư vấn kém" — nó nói "cần nghe lại 5 ca để xác nhận". Đó là chuẩn output đúng.

**Bước 3 (8') — Điền Weekly Decision Checklist trước mặt lớp.**
- Làm gì: mở Template 2, trả lời 5 câu cho Sen Spa dựa trên phân tích trên.
- Kết quả trông như thế nào:

| Câu hỏi | Quyết định tuần này | Căn cứ | Ai — Hạn | Chỉ số xác nhận |
|---|---|---|---|---|
| Tăng gì? | Tăng 2 bài/tuần dạng "kết quả khách thật" (bài mang lại nhiều inbox nhất tháng) | 2 bài case thật kéo 40% inbox của tháng | Lan duyệt, Hà đăng — T4 | Inbox/tuần ≥40 |
| Giảm gì? | Dừng đăng bài "kiến thức chung chung" thứ 4 hàng tuần | 4 bài loại này: 0 inbox | Hà — ngay | Không giảm reach >10% |
| Chỉnh offer? | Chưa chỉnh — chưa đủ bằng chứng "giá cao" (chỉ 2/8 ca) | Từ chối chính là "suy nghĩ thêm", không phải giá | — | Theo dõi thêm 2 tuần |
| Sale cải thiện gì? | Nghe lại 5 ca của Hà, kèm 1 buổi role-play script từ chối mềm | 5/8 ca không chốt là của Hà | Lan + Hà — T5 | Tỷ lệ chốt ca Hà tư vấn ≥40% trong 4 tuần tới |
| Follow-up tối ưu gì? | Bật tin follow-up 48h riêng cho khách "suy nghĩ thêm" (mẫu M8) | 4 ca "suy nghĩ" chưa ai chạm lại | Hà — T3 | ≥50% ca "suy nghĩ" được chạm lại trong 48h |

- Đếm: đúng 3 thay đổi lớn (2 nội dung + 1 sale) — các dòng còn lại là theo dõi. Đúng quy tắc "tối đa 3".

**Bước 4 (5') — Bonus: đóng vòng lặp thành AI Decision Assistant trên RocketAgent.**
- Làm gì: tạo AI Assistant mới trên RocketAgent, dán Prompt 1 + Prompt 3 vào phần instruction (chỉ dẫn hệ thống), đặt tên "Sen Spa — Cố Vấn Số Liệu". Từ nay Lan chỉ dán bảng tuần vào là ra phân tích + checklist gợi ý.
- Kết quả: assistant trả lời đúng format mỗi lần, không cần dán lại prompt dài. Ghi chú: đây chính là phôi của AI Data Analyst Agent sẽ hoàn thiện Ngày 26.

**Bước 5 (2') — Chốt thông điệp.**
- "Quy trình vừa rồi mất 25 phút. Làm mỗi tuần, 12 tuần liên tục — bạn sẽ ra quyết định giỏi hơn 90% đối thủ đang điều hành bằng cảm giác."

> **Thích ứng ngành khác:** Nha khoa — nấc tiền nặng nhất thường là "kế hoạch điều trị được tư vấn → chấp nhận"; phân tích thêm theo loại dịch vụ (niềng, implant, tổng quát). Giáo dục — nghẽn kinh điển là "học thử → ghi danh"; soi theo giáo viên đứng lớp học thử. Gym — nghẽn "hết hạn → gia hạn"; phân tích theo tần suất check-in tháng cuối. Coaching — nghẽn "cuộc gọi khám phá → ký"; soi lại chất lượng lọc lead trước cuộc gọi. Quy tắc "độ hụt × giá trị tiền" áp dụng nguyên xi.

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

**Cụm A — Chuẩn bị dữ liệu (20'):**
- [ ] Xuất bảng 4 tuần từ dashboard Ngày 23 (copy vùng phễu + kênh + chăm sóc) (5')
- [ ] Gom dữ liệu định tính: lý do không mua trong CRM, ai tư vấn ca nào, ghi chú tuần (10')
- [ ] Viết 3 dòng benchmark nội bộ (hoặc lấy khoảng tham khảo ở mục 2 nếu chưa có số riêng) (5')

**Cụm B — Phân tích với AI (45'):**
- [ ] Chạy Prompt 1: xác định phễu cộng dồn 4 tuần + điểm nghẽn theo quy tắc "độ hụt × tiền" (15')
- [ ] Tự kiểm tra lại số AI tính (ít nhất 2 phép %) — AI có thể tính sai, bạn là người ký (5')
- [ ] Chạy Prompt 2 cho điểm nghẽn số 1: tách sự kiện/giả thuyết, chốt 2 giả thuyết + cách kiểm chứng cho mỗi giả thuyết (15')
- [ ] Lưu cả 2 output thành AI Analytics Report (thêm 3 dòng tự viết: "Tôi đồng ý/không đồng ý với AI ở điểm… vì…") (10')

**Cụm C — Ra quyết định (35'):**
- [ ] Điền Weekly Decision Checklist đủ 5 câu, mỗi câu đủ 5 cột (quyết định/căn cứ/ai/hạn/chỉ số xác nhận) (20')
- [ ] Soát quy tắc: tối đa 3 thay đổi lớn — thừa thì cắt, chuyển sang "tuần sau" (5')
- [ ] Lưu 4 prompt đã cá nhân hóa (Prompt 1-4 điền sẵn bối cảnh DN) vào 1 file = AI Decision Prompt Pack (10')

**Cụm D — Giao việc (10'):**
- [ ] Gửi 3 quyết định tuần này vào nhóm nội bộ, mỗi việc gắn tên người + hạn (10')

Tổng Core: ~1h50'. **Bonus (+30'):** viết Business Review Meeting SOP (dựa khung mục 9) + dựng AI Decision Assistant trên RocketAgent như demo Bước 4.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Chạy trọn quy trình phân tích → quyết định trên số liệu 4 tuần THẬT của doanh nghiệp bạn: tìm điểm nghẽn số 1, lập báo cáo AI Analytics, điền Decision Checklist tuần này và giao việc thật cho đội.

**Deliverable nộp (vào thread cohort, deadline 23h59 hôm nay):**
1. `[Tên DN] — Ngày 24 — Funnel Bottleneck Analysis` (file gồm: bảng phễu cộng dồn 4 tuần + điểm nghẽn số 1 + con số "nghẽn này đáng bao nhiêu tiền/tháng" + 2 giả thuyết + cách kiểm chứng từng giả thuyết)
2. `[Tên DN] — Ngày 24 — AI Analytics Report` (output AI + 3 dòng phản biện của chính bạn)
3. `[Tên DN] — Ngày 24 — Weekly Decision Checklist` (Template 2 điền đủ 5 câu × 5 cột + ảnh chụp tin giao việc trong nhóm nội bộ)
4. `[Tên DN] — Ngày 24 — AI Decision Prompt Pack` (1 file chứa 4 prompt đã điền bối cảnh DN mình)

Bonus nộp thêm: `[Tên DN] — Ngày 24 — Business Review SOP` và/hoặc ảnh AI Decision Assistant trên RocketAgent.

## 7. 📄 Template Đi Kèm

**Template 1 — Funnel Bottleneck Worksheet** (bảng tính)
Các cột: `Nấc phễu · Số 4 tuần cộng dồn · % chuyển đổi · Chuẩn nội bộ/tham khảo · Độ hụt (điểm %) · Giá trị tiền của nấc (số ca hụt × AOV) · Xếp hạng nghẽn`. Kèm bản Sen Spa điền sẵn (như Demo Bước 1) và ghi chú cách tính "tiền của nghẽn".

**Template 2 — Weekly Decision Checklist** (bảng 5×5)
5 hàng câu hỏi cố định × 5 cột: `Quyết định (1 câu) · Căn cứ số liệu · Ai làm · Hạn · Chỉ số xác nhận sau 1-2 tuần`. Dòng nhắc in đậm trên đầu: "TỐI ĐA 3 THAY ĐỔI LỚN/TUẦN". Kèm bản Sen Spa điền mẫu (Demo Bước 3).

**Template 3 — AI Analytics Report khung chuẩn** (file text)
Khung 7 mục: Phạm vi dữ liệu → Phễu cộng dồn → Điểm nghẽn xếp hạng theo tiền → Sự kiện → Giả thuyết + cách kiểm chứng → Khuyến nghị → Phản biện của chủ DN (bắt buộc tự viết ≥3 dòng). Kèm bản Sen Spa hoàn chỉnh.

**Template 4 — Business Review Meeting Agenda 30'** (bonus)
`10' đọc số (ai chiếu, chiếu gì) → 10' tranh luận giả thuyết (luật: phản bác phải kèm số) → 10' chốt ≤3 quyết định (điền thẳng vào Template 2)`. Kèm luật họp: đến muộn không đợi, không số không phát biểu, quá 30' tự giải tán.

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Funnel Bottleneck Analysis (phân tích điểm nghẽn phễu) ⭐

```
[ROLE] Bạn là chuyên gia phân tích phễu bán hàng cho SME ngành dịch vụ bán qua tư vấn, cực kỳ kỷ luật với dữ liệu: chỉ khẳng định điều con số chứng minh được.

[CONTEXT] Doanh nghiệp: {{tên + ngành + AOV + giá trị đơn chính}}. Phễu: {{các nấc theo thứ tự}}. Công suất phục vụ tối đa: {{ví dụ: số ca/liệu trình có thể nhận thêm mỗi tháng}}. Chuẩn nội bộ/tham khảo từng nấc: {{dán bảng chuẩn}}.

[TASK] Phân tích phễu 4 tuần, tìm và xếp hạng điểm nghẽn.

[INPUT] Bảng số liệu 4 tuần theo từng nấc:
{{dán bảng từ dashboard}}

[OUTPUT] Đúng 5 phần:
1. Bảng phễu CỘNG DỒN 4 tuần: nấc · số · % chuyển đổi · so chuẩn (✅/⚠️/🔴).
2. Kiểm tra TRẦN ĐẦU PHỄU: lượng lead tuyệt đối so với công suất — có phải nghẽn không?
3. Xếp hạng tối đa 3 điểm nghẽn theo GIÁ TRỊ TIỀN (số ca hụt so chuẩn × giá trị đơn), ghi rõ phép tính.
4. Với nghẽn #1: 2-3 giả thuyết nguyên nhân, mỗi giả thuyết kèm "dữ liệu cần kiểm tra để xác nhận" cụ thể (nhìn vào cột nào của CRM, nghe lại cái gì, hỏi ai).
5. 1 cảnh báo về chất lượng dữ liệu nếu có (số lệch nấc, mẫu quá nhỏ, tuần bất thường).

[CONSTRAINT] Phân biệt rõ SỰ KIỆN (có số) và GIẢ THUYẾT (phỏng đoán) — cấm khẳng định nguyên nhân khi chưa có dữ liệu xác nhận. Số mẫu <10 thì nói xu hướng, không nói %. Mọi phép tính hiển thị công thức để tôi kiểm tra lại. Viết tiếng Việt, ≤1,5 trang.
```

**Ví dụ đã điền (Sen Spa):** `{{công suất}}` = "4 KTV, tối đa ~12 liệu trình mới/tháng, hiện chỉ chốt 6/tháng"; kết quả kỳ vọng như Demo Bước 1 — nghẽn #1 là trần đầu phễu (11 lead/tuần), nghẽn #2 theo tiền là Show→Chốt (96tr cơ hội/4 tuần).

### Prompt 2 — Đào sâu một điểm nghẽn (5 Whys có kỷ luật dữ liệu)

```
[ROLE] Bạn là cố vấn vận hành theo trường phái "hỏi Vì Sao 5 lần" (5 Whys) nhưng chỉ chấp nhận câu trả lời có bằng chứng.

[CONTEXT] Doanh nghiệp: {{tên + ngành}}. Điểm nghẽn đã xác định: {{ví dụ: Show→Chốt 42,9%, 8 ca không chốt trong 4 tuần}}.

[TASK] Đào nguyên nhân gốc của điểm nghẽn này.

[INPUT] Dữ liệu định tính liên quan:
- Lý do không mua ghi trong CRM: {{liệt kê}}
- Ai xử lý từng ca: {{liệt kê}}
- Quy trình hiện tại của khâu này: {{mô tả ngắn hoặc dán SOP}}
- Ghi chú khác: {{tùy chọn}}

[OUTPUT] (1) Bảng tách SỰ KIỆN vs GIẢ THUYẾT từ dữ liệu trên; (2) chuỗi Vì Sao tối đa 5 tầng cho 2 nhánh giả thuyết mạnh nhất — dừng ngay ở tầng nào thiếu dữ liệu và ghi "cần kiểm chứng: [việc cụ thể ≤30 phút]"; (3) đề xuất 1-2 hành động kiểm chứng NHANH tuần này trước khi sửa lớn.

[CONSTRAINT] Không kết luận về năng lực cá nhân khi chỉ có <10 ca dữ liệu — chỉ được đề xuất quan sát thêm. Hành động kiểm chứng phải ≤30 phút thực hiện. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** input = "8 ca không chốt: 4 'suy nghĩ thêm', 2 'giá cao', 1 'nhà xa', 1 không ghi; Lan tư vấn 3, Hà tư vấn 5; quy trình: tư vấn tại spa sau buổi soi da, dùng sales script Ngày 18". Output kỳ vọng: 2 nhánh như Demo Bước 2 + kiểm chứng "nghe lại ghi chú 5 ca của Hà (20')".

### Prompt 3 — Điền nháp Weekly Decision Checklist

```
[ROLE] Bạn là trợ lý điều hành của chủ SME — nhiệm vụ của bạn là ĐỀ XUẤT NHÁP để chủ DN duyệt, không phải quyết thay.

[CONTEXT] Doanh nghiệp: {{tên + ngành + đội ngũ: ai làm gì}}. Phân tích tuần này: {{dán output Prompt 1 + Prompt 2}}.

[TASK] Điền nháp checklist 5 câu hỏi quyết định tuần.

[INPUT] 5 câu cố định: (1) Tăng gì? (2) Giảm/dừng gì? (3) Chỉnh offer không? (4) Sale cải thiện điểm nào? (5) Follow-up/chăm sóc tối ưu gì?

[OUTPUT] Bảng 5 hàng × 5 cột: Quyết định đề xuất (1 câu) · Căn cứ số liệu (trích số cụ thể) · Ai làm (chọn từ đội ngũ đã cho) · Hạn (trong tuần) · Chỉ số xác nhận sau 1-2 tuần. Nếu câu nào CHƯA đủ bằng chứng để thay đổi, ghi "Giữ nguyên — theo dõi thêm [chỉ số] trong [x] tuần" — đó cũng là một quyết định hợp lệ.

[CONSTRAINT] Tối đa 3 thay đổi lớn, còn lại phải là "giữ nguyên/theo dõi". Mỗi việc giao phải khớp vai trò thật của người trong đội (không giao lễ tân viết chiến lược). Không đề xuất việc cần ngân sách mới >{{ngưỡng, ví dụ 2tr}}/tuần khi chưa hỏi tôi. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** đội ngũ = "Lan (chủ, tư vấn chốt, duyệt nội dung), Hà (lễ tân, trực page/Zalo, đăng bài), 4 KTV (trị liệu, xin feedback khách)". Output kỳ vọng: bảng như Demo Bước 3.

### Prompt 4 — Cảnh báo bất thường nhanh (chạy giữa tuần)

```
[ROLE] Bạn là hệ thống cảnh báo sớm cho doanh nghiệp nhỏ — nói ít, chỉ kêu khi cần.

[CONTEXT] Doanh nghiệp {{tên + ngành}}. Mức trung bình 4 tuần của các chỉ số chính: {{dán: lead/tuần, booking/tuần, inbox/tuần…}}.

[TASK] So số 3 ngày đầu tuần này với nhịp bình thường, chỉ báo những gì LỆCH đáng kể.

[INPUT] Số 3 ngày đầu tuần: {{dán số}}.

[OUTPUT] Tối đa 3 dòng cảnh báo, mỗi dòng: chỉ số · số hiện tại vs nhịp thường (quy đổi cùng đơn vị thời gian) · mức lệch · 1 việc kiểm tra ngay hôm nay (≤15 phút). Nếu mọi thứ trong nhịp bình thường: trả lời đúng 1 câu "Không có gì bất thường, cứ chạy tiếp."

[CONSTRAINT] Không suy diễn nguyên nhân — chỉ báo lệch + việc kiểm tra. Lệch <20% so nhịp thường thì bỏ qua (nhiễu tự nhiên của số nhỏ). Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** "Nhịp thường: 11 lead/tuần (~1,6/ngày), 35 inbox/tuần (~5/ngày). Số T2-T4 tuần này: 1 lead, 4 inbox." → Output kỳ vọng: "Lead 3 ngày = 1 (nhịp thường ~4,7) — lệch −79%. Kiểm tra ngay: form trên landing page còn hoạt động không (tự điền thử, 5')". Đây chính là ca "automation chết im lặng" của Ngày 22.

## 9. 📋 SOP Thao Tác

**SOP-24 · Nhịp phân tích & ra quyết định:**

| Khi nào | Ai làm | Input → Các bước → Output |
|---|---|---|
| Sáng thứ 2, 25' (ngay sau SOP-23) | Chủ DN | Dashboard đã có cột tuần mới → chạy Prompt 1 (10') → tự kiểm 2 phép tính → điền Decision Checklist, cắt còn ≤3 thay đổi (10') → gửi giao việc vào nhóm (5') → Output: checklist tuần + tin giao việc |
| Thứ 4, 5' | Chủ DN | Số 3 ngày đầu tuần → chạy Prompt 4 → Output: 0-3 cảnh báo, mỗi cảnh báo 1 việc kiểm tra trong ngày |
| Thứ 6, 30' (nếu có đội ≥3 người) | Cả đội | AI Analytics Report → họp theo Template 4 (10-10-10) → Output: biên bản = chính Template 2 đã điền |
| 2 tuần/lần | Chủ DN | Checklist 2 tuần trước → dò cột "chỉ số xác nhận": quyết định nào ĐÃ tạo kết quả, quyết định nào không → Output: 1 dòng bài học ghi vào cuối file Prompt Pack |
| Mỗi quý | Chủ DN | 12 checklist tuần → cập nhật chuẩn nội bộ từng nấc phễu bằng trung bình quý → Output: bảng benchmark mới dán vào Prompt 1 |

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Bottleneck Analysis đủ 4 thành phần: phễu cộng dồn + nghẽn #1 + giá trị tiền của nghẽn (có phép tính) + 2 giả thuyết kèm cách kiểm chứng (12đ — thiếu 1 thành phần trừ 3đ); AI Analytics Report có đủ 7 mục khung Template 3 (8đ); Decision Checklist đủ 5 hàng × 5 cột, không ô trống (6đ); Prompt Pack đủ 4 prompt đã điền bối cảnh (4đ) |
| Chất lượng & độ sâu | 30 | Nghẽn chọn theo quy tắc "độ hụt × tiền", có phép tính kiểm tra lại được — không chọn theo "% thấp nhất" một cách máy móc (10đ); giả thuyết tách bạch khỏi sự kiện, mỗi giả thuyết có việc kiểm chứng ≤30' (10đ); phần phản biện AI ≥3 dòng, có chỉ ra ít nhất 1 điểm bạn nghĩ khác AI hoặc 1 chỗ AI thiếu bối cảnh (10đ) |
| Cá nhân hoá vào DN thật | 25 | Chạy trên số 4 tuần thật từ dashboard của mình (10đ); người được giao việc là người thật trong đội, đúng vai trò (8đ); quyết định khớp với nghẽn đã tìm ra — không ra quyết định "tăng ads" khi nghẽn nằm ở khâu chốt (7đ) |
| Dùng được ngay | 15 | Đã gửi tin giao việc thật (ảnh chụp) (7đ); tuân thủ ≤3 thay đổi lớn (4đ); mỗi quyết định có chỉ số xác nhận đo được sau 1-2 tuần (4đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Bê nguyên output AI làm bài nộp, phần phản biện viết "AI phân tích rất đúng" (−10đ nhóm 2).
2. Liệt kê 5 điểm nghẽn dàn hàng ngang, không xếp hạng theo tiền, không chọn #1 (−6đ nhóm 2).
3. Quyết định không ăn nhập với phân tích — phân tích ra nghẽn chốt sale, quyết định lại là "làm thêm video TikTok" (−7đ nhóm 3).
4. Giả thuyết khẳng định như sự thật: "nguyên nhân là nhân viên tư vấn yếu" trên 5 ca dữ liệu (−5đ nhóm 2).
5. Checklist 5 câu nhưng cả 5 đều là thay đổi lớn (−4đ nhóm 4 — vi phạm quy tắc 3).

## 11. ❓ FAQ & Lỗi Thường Gặp

**FAQ:**
1. *"Số của tôi quá nhỏ (5-10 lead/tuần), phân tích % có nghĩa gì không?"* — % theo tuần thì không, nhưng CỘNG DỒN 4 tuần (20-40 lead) bắt đầu có nghĩa, và dữ liệu ĐỊNH TÍNH (lý do từ chối, ai tư vấn) thì có nghĩa ngay từ ca thứ 5. Số nhỏ là lý do để phân tích kỹ từng ca, không phải lý do bỏ phân tích.
2. *"AI phân tích có tin được không? Nó từng tính sai % cho tôi."* — Đúng, AI có thể tính sai — vì vậy checklist bắt bạn tự kiểm 2 phép tính, và prompt bắt AI hiển thị công thức. Quy tắc: AI đề xuất, số liệu làm chứng, BẠN ký. Sai sót của AI dễ bắt hơn nhiều so với sai sót của cảm tính — vì AI trình bày ra giấy.
3. *"Tuần nào cũng phân tích thì lấy đâu ra thời gian làm việc khác?"* — Toàn bộ SOP-24 là 25' sáng thứ 2 + 5' thứ 4. So sánh: một quyết định sai (bơm 10tr ads vào phễu nghẽn ở khâu chốt) đốt của bạn nhiều hơn 30'/tuần × 1 năm.
4. *"Điểm nghẽn của tôi là thứ tôi không sửa được ngay (ví dụ: chính tôi là người tư vấn và tôi hết giờ)?"* — Đó là phát hiện giá trị nhất khóa này: nghẽn là CÔNG SUẤT CHỦ. Quyết định hợp lệ: chuẩn hóa để ủy quyền (sales script + checklist chốt cho nhân viên — tài sản Ngày 18), hoặc nâng giá/lọc lead kỹ hơn để mỗi ca tư vấn đáng tiền hơn. Ghi thẳng vào checklist.
5. *"Benchmark ngành lấy đâu ra? Có chuẩn không?"* — Khoảng tham khảo trong giáo án là điểm khởi động từ kinh nghiệm cohort, KHÔNG phải chân lý. Sau 8 tuần vận hành, benchmark thật của bạn = trung bình của chính bạn, và mục tiêu = tốt hơn chính mình tháng trước 10%.
6. *"Họp review mà đội tôi chỉ có 2 người thì sao?"* — Bỏ cuộc họp, giữ NGHI THỨC: 2 người cùng nhìn dashboard 15' sáng thứ 2, điền chung checklist. Nghi thức quan trọng hơn hình thức họp.

**Lỗi thường gặp:**
1. **Phân tích xong… để đấy (analysis paralysis — tê liệt vì phân tích).** Phát hiện: 2 tuần liên tiếp có report nhưng cột "Ai — Hạn" trống hoặc không ai làm. Sửa: luật "report chưa giao việc = report chưa xong"; rubric yêu cầu ảnh tin giao việc là vì vậy.
2. **Đổi quá nhiều thứ cùng lúc.** Phát hiện: checklist tuần có 5-6 thay đổi; 2 tuần sau không biết cái gì tạo ra kết quả. Sửa: quay về quy tắc 3; mỗi thay đổi phải có "chỉ số xác nhận" riêng.
3. **Nhìn nhầm nhiễu thành xu hướng.** Phát hiện: hoảng loạn đổi chiến lược vì 1 tuần xấu (tuần 3 của Sen Spa: nghỉ lễ, reach giảm cả thị trường). Sửa: luôn so với trung bình 4 tuần; thêm cột "ghi chú định tính tuần" vào dashboard để nhớ bối cảnh.
4. **Cho AI số liệu mà quên bối cảnh định tính.** Phát hiện: AI đề xuất "tăng tần suất đăng bài" đúng tuần cả đội đi du lịch. Sửa: mục {{ghi chú định tính}} trong prompt là bắt buộc điền, kể cả khi ghi "không có gì đặc biệt".

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 23 — KPI Dashboard]] · Ngày sau: [[Ngày 25 — Customer Success, Remarketing & Upsell]]
- Lên MOC: [[_MOC 28 Day AIOS]]
- Tài sản hôm nay được dùng lại ở:
  - **Ngày 25:** nếu phân tích hôm nay chỉ ra nghẽn ở tái mua/khách cũ (như Sen Spa: lead giới thiệu chỉ 1-3/tuần), Ngày 25 chính là ngày sửa nghẽn đó.
  - **Ngày 26:** Prompt Pack hôm nay trở thành instruction của AI Data Analyst Agent; AI Decision Assistant (bonus) được chuẩn hóa thành agent chính thức.
  - **Ngày 27:** SOP-24 nhập vào Weekly Operating Rhythm (nhịp thứ 2 + thứ 4 + thứ 6); vòng "Đo lường → Tối ưu" trong OS Map chính là quy trình hôm nay.
  - **Ngày 28:** Decision Checklist 4 tuần đầu sau khóa là công cụ chính của giai đoạn "30 ngày tối ưu conversion" trong Kế hoạch 90 ngày.
