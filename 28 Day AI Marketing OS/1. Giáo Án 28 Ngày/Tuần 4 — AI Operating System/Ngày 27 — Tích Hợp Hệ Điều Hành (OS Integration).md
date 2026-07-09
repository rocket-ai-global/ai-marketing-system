---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 4
day: 27
core-output: "AI Marketing & Sales OS Map, End-to-End Customer Flow, Weekly Operating Rhythm, Full System Test Report"
---

# Ngày 27 — Tích Hợp Hệ Điều Hành (OS Integration)

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** OS Map vẽ `.canvas` (skill `json-canvas`); SOP Operating Pack lưu `04. Resources/Playbooks/`; nhịp vận hành hàng ngày ghi `Daily/`. **Đỉnh của ngày lắp ráp = KÍCH HOẠT JARVIS** — siêu trợ lý điều hành nhận lệnh CEO qua Telegram/Zalo, điều phối 5 agent (Ngày 26), tự gửi Morning Brief 8h / Evening Report 20h: nạp Master Instruction + phân quyền + chạy 10 ca test theo [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]]. Demo tốt nghiệp Ngày 28 mở màn bằng Morning Brief của chính Jarvis học viên.

> Hôm nay là ngày lắp ráp: 26 ngày tài sản rời rạc được nối thành MỘT hệ điều hành — vẽ được trên 1 trang giấy, chạy theo 1 nhịp tuần cố định, và được kiểm thử từ đầu đến cuối bằng một chiến dịch test thật trước khi demo tốt nghiệp ngày mai.

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay:

**Core Output (bắt buộc — điều kiện qua ngày):**
- **AI Marketing & Sales OS Map (sơ đồ hệ điều hành)**: 1 trang duy nhất vẽ đủ 12 khối tài sản + mũi tên dữ liệu nối chúng, kèm chú thích ai/agent nào vận hành khối nào.
- **End-to-End Customer Flow (luồng khách hàng đầu-cuối)**: đường đi của MỘT khách từ lần đầu thấy nội dung → mua → được chăm → tái mua → giới thiệu, chỉ rõ ở mỗi bước: hệ thống làm gì, người làm gì, dữ liệu ghi vào đâu.
- **Weekly Operating Rhythm (nhịp vận hành tuần)**: lịch tuần cố định T2→CN — việc gì, ai làm, bao nhiêu phút, dùng SOP/agent nào.
- **Full System Test Report (báo cáo kiểm thử toàn hệ thống)**: kết quả chạy 1 chiến dịch test xuyên suốt 9 trạm, ghi PASS/FAIL từng trạm.

**Bonus Output (nâng cao):**
- **SOP Operating Pack đầy đủ**: gom 8 SOP (tạo content, đăng bài, xử lý lead, tư vấn, gửi proposal, follow-up, chăm sau mua, review dashboard) vào 1 tài liệu vận hành duy nhất có mục lục.
- Bảng phân vai RACI rút gọn (ai Làm — ai Duyệt — ai được Báo) cho toàn hệ thống.

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — "Hệ điều hành doanh nghiệp" nghĩa là gì (5')
- **Ý chính:** Operating System (hệ điều hành) của doanh nghiệp = tập hợp: TÀI SẢN (công cụ, nội dung, dữ liệu) + LUỒNG (cách dữ liệu và khách hàng chảy qua các tài sản) + NHỊP (lịch lặp lại hàng tuần) + VAI (ai chịu trách nhiệm gì). Thiếu 1 trong 4 thì chỉ là "đống công cụ".
- **Analogy Sen Spa:** 26 ngày qua Lan xây được 12 "căn phòng" (content, landing page, CRM, chatbot, automation, dashboard, agent…). Hôm nay xây HÀNH LANG nối các phòng + treo LỊCH TRỰC + bảng PHÂN CÔNG. Một spa có 12 phòng đẹp mà không có hành lang thì khách lạc, nhân viên dẫm chân nhau.
- Bài kiểm tra "đã thành OS chưa" (3 câu): (1) Vẽ được toàn hệ thống trên 1 trang? (2) Nhân viên mới nhìn lịch tuần biết làm gì mỗi sáng? (3) Chủ đi vắng 1 tuần, lead có còn được xử lý đúng?

### Khối 2 — OS Map: 12 khối, 4 tầng (8')
- Cấu trúc chuẩn của OS Map — 4 tầng từ trên xuống:

| Tầng | Khối | Từ ngày |
|---|---|---|
| 1. Thu hút (Marketing) | Content · Landing page + Lead form · Lead magnet | Tuần 2 |
| 2. Chuyển đổi (Sales) | Chatbot · CRM + Lead scoring · Sales script + Proposal · Follow-up | Tuần 3 |
| 3. Giữ & nhân (Retention) | Customer Success + Upsell · Referral | Ngày 25 |
| 4. Nền & não (Foundation + AI) | Knowledge Base · Bộ AI Agent · Automation · Dashboard + AI Analytics | Tuần 1 + 22-26 |
- **Quy tắc vẽ:** mỗi mũi tên là một DÒNG DỮ LIỆU có thật, trả lời được "cái gì chảy qua đây, bằng cơ chế nào?" (ví dụ: Form → CRM: "thông tin lead, qua automation luồng 1 Ngày 22"). Mũi tên không trả lời được = chỗ đứt của hệ thống — chính là cái cần phát hiện hôm nay.
- Vòng lặp quan trọng nhất phải nhìn thấy trên map: **Dashboard → AI Analytics → Quyết định → chỉnh tầng 1-3 → dữ liệu mới về Dashboard** (vòng tự tối ưu) và **Khách hài lòng → Referral → Lead mới** (vòng tự nhân).

### Khối 3 — End-to-End Customer Flow: kể chuyện một khách đi hết hệ thống (5')
- **Ý chính:** OS Map là ảnh chụp từ trên xuống; Customer Flow là thước phim theo chân MỘT khách. Viết dạng bảng dòng thời gian: `Bước · Khách thấy/làm gì · Hệ thống làm gì (khối nào, tự động?) · Người làm gì · Dữ liệu ghi đâu`.
- **Cách giảng:** kể chuyện "chị Mai gặp Sen Spa" (chi tiết ở Demo) — học viên nghe một mạch 12 bước sẽ hiểu vì sao từng tài sản 26 ngày qua tồn tại. Chỗ nào kể đến mà ấp úng ("ờ… chỗ này chắc Hà tự nhớ") = lỗ hổng cần vá.

### Khối 4 — Weekly Operating Rhythm: hệ thống sống bằng nhịp, không bằng hứng (4')
- Khung nhịp chuẩn (đã gặp từng mảnh ở SOP các ngày trước — hôm nay ghép lại):
  - **T2 sáng:** đọc số + quyết định (SOP-23/24, 40') → kế hoạch content & sales tuần.
  - **T3-T5:** sản xuất + đăng (SOP content) · xử lý lead + follow-up (tự động nhắc mỗi sáng) · chăm sóc theo mốc (SOP-25 thứ 3, upsell thứ 5).
  - **T6:** review nhanh giữa tuần + nuôi agent (SOP-26, 15') + họp 30' nếu có đội.
  - **T7:** nhập số dashboard (25') + tối ưu 1 thứ nhỏ.
  - **CN:** nghỉ / xem trước lịch tuần mới 10'.
- Tổng thời gian vai chủ DN: **~3h/tuần** cho toàn bộ điều hành hệ thống — con số phải nói to trước lớp, vì đây là lời hứa của cả chương trình.

### Khối 5 — Full System Test: một chiến dịch giả, chín trạm thật (3')
- Test toàn hệ thống = thả 1 "khách test" vào đầu phễu và theo dấu qua 9 trạm: (1) đăng nội dung → (2) khách bấm/điền form → (3) lead vào CRM đúng tag → (4) chatbot/tin xác nhận phản hồi → (5) sale nhận thông báo → (6) follow-up kích hoạt đúng lịch → (7) proposal/booking gửi được → (8) số liệu hiện lên dashboard → (9) AI phân tích ra báo cáo. Mỗi trạm PASS/FAIL kèm ảnh — FAIL không phải thất bại, là món quà: phát hiện hôm nay rẻ hơn phát hiện khi khách thật rơi.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 26 | Chiếu 2 ca test agent "bẫy" hay nhất; nhắc nộp lại các instruction 🔧. Câu mở màn: "Ai vẽ được TOÀN BỘ hệ thống mình đã xây lên 1 trang giấy trong 5 phút? Thử luôn — 5 phút, giấy bút." (đa số vẽ thiếu → đó là bài hôm nay) |
| 25' | Giảng kiến thức trọng tâm | 5 khối ở mục 2. Trọng tâm: 12 khối 4 tầng + quy tắc "mũi tên phải trả lời được" |
| 30' | Demo live trên Sen Spa | Vẽ OS Map → kể Customer Flow chị Mai → chạy Full System Test 9 trạm rút gọn (kịch bản mục 4) |
| 15' | Học viên làm tại chỗ + Q&A | Mỗi người vẽ OS Map nháp trên Template 1, khoanh đỏ các mũi tên "chưa trả lời được"; trainer đi từng người đếm mũi tên đỏ (đó là việc tối nay) |
| 10' | Giao bài tập | Deliverable + rubric + deadline. Nhấn mạnh: "Ngày mai demo tốt nghiệp — Full System Test tối nay chính là buổi tổng duyệt. Trạm nào FAIL, sửa tối nay, đừng để nó FAIL trước cả lớp" |

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (8') — Vẽ OS Map Sen Spa lên 1 trang (Template 1).**
- Làm gì: đặt 12 khối vào 4 tầng, vẽ mũi tên và VIẾT NHÃN lên từng mũi tên.
- Công cụ: Template 1 (slide/Excalidraw/giấy chụp lại đều hợp lệ).
- Kết quả trông như thế nào (bản chữ của map):

```
TẦNG 1 — THU HÚT:  Content (bài/video) ──"link+CTA"──> Landing page/Form + Lead magnet
TẦNG 2 — CHUYỂN ĐỔI:  Form ──automation L1──> CRM ──lead score──> Sales (script+proposal)
   Chatbot ──"lead từ inbox + tag"──> CRM;  CRM ──automation L2──> Follow-up (nhắc 8h30)
TẦNG 3 — GIỮ & NHÂN:  CRM "Đã mua" ──automation L4──> CS Journey ──buổi 5-6──> Upsell
   CS ──"khách 5/5, sau 7 ngày"──> Referral ──"voucher đôi"──> LEAD MỚI (vòng về tầng 1)
TẦNG 4 — NỀN & NÃO:  Knowledge Base ──> 5 Agent + Chatbot (tri thức)
   CRM/Form/Zalo ──"số liệu"──> Dashboard ──T2 hàng tuần──> AI Analytics ──> QUYẾT ĐỊNH
   ──"≤3 thay đổi"──> quay lại điều chỉnh Tầng 1-3   [vòng tự tối ưu]
```
- Trainer chỉ vào 2 vòng lặp (tự tối ưu, tự nhân) và 1 mũi tên cố tình để đứt: "Chatbot → CRM ở Sen Spa hiện là Hà chép tay cuối ngày — mũi tên NGƯỜI làm, hợp lệ, nhưng phải ghi nhãn trung thực. Map đẹp mà nhãn dối là hệ thống dối."

**Bước 2 (7') — Kể End-to-End Customer Flow: "12 bước của chị Mai" (Template 2).**
- Làm gì: điền bảng dòng thời gian, kể liền mạch:
  1. Mai lướt FB, thấy bài "Da mụn tuổi 30" (Content — Hà đăng theo calendar T3).
  2. Bấm link, điền form nhận cẩm nang (Landing page + Lead magnet).
  3. Automation L1: Mai vào CRM, tag "FB-Lead magnet", tin Zalo xác nhận trong 1' (máy).
  4. Hà nhận thông báo, gọi Mai trong 15', ghi chú "da mụn viêm, quan tâm liệu trình" (người).
  5. Lead score 8/10 → báo Lan; Mai đặt lịch soi da thứ 5 (CRM + booking).
  6. Tin nhắc lịch tự động trước 24h + 2h (automation) → Mai đến (show).
  7. Lan tư vấn theo sales script + ảnh soi da; Mai "suy nghĩ thêm" → CRM cập nhật, follow-up 48h kích hoạt.
  8. Tin 48h gửi case khách tương tự (Sales Agent soạn, Lan duyệt) → Mai chốt liệu trình 12tr.
  9. Automation L4: tin chào mừng + cẩm nang + lịch 8 buổi (máy); CS Journey bắt đầu.
  10. Buổi 5-6: ảnh da cải thiện 70% → Lan chào gói duy trì (Upsell Map) → Mai đồng ý thêm 2tr/tháng.
  11. Buổi 8 + 7 ngày: điểm hài lòng 5/5 → Hà gửi voucher referral đôi → bạn của Mai điền form. **Vòng khép: khách sinh khách.**
  12. Suốt hành trình: mọi trạng thái ghi CRM → cuối tuần lên dashboard → sáng T2 Lan đọc AI report — thấy "referral tuần này: 2" và mỉm cười.
- Kết quả: bảng 12 dòng × 5 cột, mỗi dòng rõ máy/người/dữ liệu.

**Bước 3 (12') — Full System Test rút gọn, live.**
- Làm gì: trainer đóng vai "khách test Nguyễn Thị Thử": điền form thật trên landing page Sen Spa → cả lớp theo dấu qua 9 trạm trên màn hình chia đôi (trái: điện thoại khách, phải: CRM + RocketAgent + Zalo của spa) → điền Template 4 từng trạm.
- Kết quả trông như thế nào (trích report):

| Trạm | Kỳ vọng | Kết quả | PASS/FAIL |
|---|---|---|---|
| 1. Đăng nội dung | Bài test có link form | Đã đăng chế độ giới hạn | ✅ |
| 2. Form | Điền được trên điện thoại | OK, 40 giây | ✅ |
| 3. CRM | Dòng mới + tag đúng trong 1' | OK | ✅ |
| 4. Tin xác nhận | Zalo đến trong 1' | ĐẾN SAU 9' — hàng đợi chậm | 🔴 FAIL |
| 5. Thông báo sale | Hà nhận trong 5' | OK | ✅ |
| 6. Follow-up | Xuất hiện trong danh sách nhắc 8h30 mai | Kiểm tra sáng mai, tạm ✅ có điều kiện | ⚠️ |
| 7-9 | Proposal gửi được · số lên dashboard · AI report chạy | OK / OK / OK | ✅ |
- Trainer xử lý FAIL trạm 4 ngay trước lớp bằng Prompt 3 (chẩn đoán điểm đứt) → tìm ra nguyên nhân → sửa → test lại trạm 4 → ✅. Thông điệp: "Quy trình sửa quan trọng hơn việc không có lỗi."

**Bước 4 (3') — Chốt nhịp tuần.**
- Chiếu Weekly Operating Rhythm của Sen Spa (Template 3 điền sẵn), cộng tổng giờ từng người: Lan 3h10'/tuần, Hà 5h/tuần (trong giờ làm sẵn có), KTV 10'/khách. "Đây là toàn bộ chi phí vận hành một hệ điều hành marketing-sales. Rẻ hơn một nhân viên part-time."

> **Thích ứng ngành khác:** cấu trúc 4 tầng + 9 trạm test giữ nguyên cho mọi ngành dịch vụ tư vấn; thứ thay đổi là TÊN các bước trong Customer Flow (nha khoa: form → đặt lịch khám → chụp phim → tư vấn phác đồ → điều trị nhiều buổi; giáo dục: form → học thử → tư vấn lộ trình → ghi danh → học → thi → khoe kết quả → referral phụ huynh). Ngành chu kỳ dài (coaching, giáo dục) thêm mốc "renewal/tái ký" vào tầng 3.

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

**Cụm A — OS Map (35'):**
- [ ] Đặt 12 khối của DN mình vào 4 tầng trên Template 1; khối nào CHƯA có thì vẫn vẽ, đánh dấu ⬜ "chưa xây" — trung thực (10')
- [ ] Vẽ mũi tên + viết nhãn cho TỪNG mũi tên: cái gì chảy, cơ chế gì (automation số mấy / người nào / chưa có) (15')
- [ ] Khoanh đỏ mũi tên đứt (không trả lời được) → chọn 1-2 mũi tên đỏ QUAN TRỌNG NHẤT, vá ngay bằng phương án người-theo-nhắc (10')

**Cụm B — Customer Flow + Nhịp tuần (40'):**
- [ ] Điền End-to-End Customer Flow ≥10 bước cho khách điển hình của mình (Template 2) — kể được một mạch không ấp úng (20')
- [ ] Điền Weekly Operating Rhythm (Template 3): mọi ô có tên người + số phút; cộng tổng giờ từng người, vai chủ DN ≤4h/tuần (20')

**Cụm C — Full System Test (45'):**
- [ ] Chuẩn bị: tạo "khách test" bằng SĐT phụ; đăng bài test chế độ giới hạn hoặc dùng link form trực tiếp (10')
- [ ] Chạy 9 trạm theo Template 4, chụp ảnh từng trạm (25')
- [ ] Trạm FAIL: chẩn đoán bằng Prompt 3, sửa được thì sửa + test lại; chưa sửa được tối nay thì ghi rõ nguyên nhân + kế hoạch sửa vào report (10')

Tổng Core: ~2h. **Bonus (+40'):** gom 8 SOP các ngày trước vào SOP Operating Pack có mục lục (dùng Prompt 4 để chuẩn hóa format) + bảng phân vai Làm-Duyệt-Báo.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Lắp ráp hệ điều hành của DN bạn: vẽ OS Map 1 trang, viết Customer Flow đầu-cuối, chốt nhịp vận hành tuần, và chạy Full System Test 9 trạm — sửa các trạm FAIL trước Demo Day ngày mai.

**Deliverable nộp (vào thread cohort, deadline 23h59 hôm nay):**
1. `[Tên DN] — Ngày 27 — OS Map` (ảnh/file 1 trang: 12 khối 4 tầng, mũi tên có nhãn, khối chưa xây đánh dấu ⬜, mũi tên đỏ còn lại ghi chú kế hoạch vá)
2. `[Tên DN] — Ngày 27 — Customer Flow` (Template 2, ≥10 bước × 5 cột)
3. `[Tên DN] — Ngày 27 — Weekly Rhythm` (Template 3, có tổng giờ từng người)
4. `[Tên DN] — Ngày 27 — Full System Test Report` (Template 4: 9 trạm PASS/FAIL + ảnh từng trạm + phần xử lý FAIL)

Bonus nộp thêm: `[Tên DN] — Ngày 27 — SOP Operating Pack` (8 SOP + mục lục).

## 7. 📄 Template Đi Kèm

**Template 1 — OS Map khung 4 tầng** (slide/Excalidraw)
Khung 4 tầng × 12 ô khối đặt sẵn vị trí, mũi tên nét đứt gợi ý sẵn các kết nối chuẩn — học viên xác nhận/sửa nhãn thay vì vẽ từ giấy trắng. Chú giải ký hiệu: nét liền = tự động; nét đứt = người làm theo nhắc; đỏ = đứt; ⬜ = khối chưa xây. Kèm bản Sen Spa hoàn chỉnh.

**Template 2 — End-to-End Customer Flow** (Sheets)
Bảng: `Bước · Khách thấy/làm gì · Hệ thống làm gì (khối nào, [MÁY]/[NGƯỜI]) · Người nào làm gì · Dữ liệu ghi vào đâu`. Kèm 12 bước chị Mai điền sẵn.

**Template 3 — Weekly Operating Rhythm** (Sheets, dạng lịch tuần)
Lưới T2→CN × khung giờ; mỗi ô việc: `Tên việc · SOP/agent dùng · Ai · Phút`. Hàng cuối: tổng phút/người/tuần. Kèm bản Sen Spa (Lan 3h10', Hà 5h) + phiên bản rút gọn cho DN solo (chủ kiêm hết: 6h/tuần).

**Template 4 — Full System Test Report** (Sheets)
9 trạm × cột: `Trạm · Kỳ vọng (đo được: trong bao lâu, hiện ở đâu) · Kết quả thực tế · PASS/FAIL/⚠️ · Ảnh · Nguyên nhân nếu FAIL · Đã sửa? Test lại lúc nào`. Kèm bản Sen Spa có trạm 4 FAIL và đã xử lý — làm mẫu cách ghi FAIL trung thực.

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Rà soát OS Map, tìm điểm đứt ⭐

```
[ROLE] Bạn là kiến trúc sư hệ thống vận hành cho SME dịch vụ, mắt nghề chuyên soi "mũi tên đứt" — những chỗ dữ liệu hoặc khách hàng rơi giữa hai khối.

[CONTEXT] Doanh nghiệp: {{tên + ngành + quy mô đội}}. Tôi vừa vẽ OS Map, mô tả bằng chữ như sau (khối nào chưa xây tôi ghi ⬜, mũi tên người làm tôi ghi [NGƯỜI]):
{{dán mô tả map: các khối + các mũi tên kèm nhãn}}

[TASK] Rà soát map và tìm mọi điểm đứt/điểm yếu.

[INPUT] Mô tả map ở trên + nhịp tuần dự kiến: {{dán tóm tắt Weekly Rhythm}}.

[OUTPUT] (1) Danh sách MŨI TÊN THIẾU: các kết nối chuẩn của mô hình 4 tầng mà map tôi chưa có (đối chiếu: content→form, form→CRM, chatbot→CRM, CRM→follow-up, mua→CS, CS→referral→lead, dữ liệu→dashboard→quyết định→điều chỉnh); (2) danh sách MŨI TÊN MONG MANH: đang phụ thuộc 1 người duy nhất hoặc trí nhớ — kèm rủi ro cụ thể "nếu người này nghỉ 1 tuần thì…"; (3) xếp hạng 3 điểm cần vá trước, mỗi điểm 1 phương án vá NHANH (dùng automation/nhắc việc sẵn có, không thêm tool mới); (4) 1 nhận xét về vòng lặp: map đã có vòng tự tối ưu và vòng referral chưa?

[CONSTRAINT] Không đề xuất công cụ mới ngoài RocketAgent/Zalo/Sheets. Không chê bai khối ⬜ chưa xây — chỉ đánh giá kết nối giữa các khối ĐANG có. Viết tiếng Việt, ≤1 trang.
```

**Ví dụ đã điền (Sen Spa):** map dán vào như Demo Bước 1 (chatbot→CRM ghi [NGƯỜI] Hà chép tay cuối ngày). Output kỳ vọng: điểm mong manh #1 = "chatbot→CRM phụ thuộc Hà chép tay — Hà nghỉ là lead inbox rơi; vá nhanh: bật tính năng RocketAgent tự đẩy hội thoại có SĐT vào Sheet, hoặc nhắc việc 2 lần/ngày thay vì cuối ngày".

### Prompt 2 — Viết End-to-End Customer Flow từ tài sản có sẵn

```
[ROLE] Bạn là chuyên gia thiết kế trải nghiệm khách hàng (CX) cho ngành dịch vụ bán qua tư vấn.

[CONTEXT] Doanh nghiệp: {{tên + ngành}}. Khách điển hình: {{chân dung 2 câu}}. Các tài sản đang có: {{liệt kê 12 khối, khối nào chưa có ghi rõ}}. Phễu: {{các nấc}}.

[TASK] Viết End-to-End Customer Flow: theo chân 1 khách giả định có tên, từ lần đầu thấy nội dung đến khi giới thiệu bạn (vòng khép kín).

[INPUT] Chi tiết vận hành: {{ai trực page, ai tư vấn, automation nào đang bật, mốc CS Journey}}.

[OUTPUT] Bảng 10-14 bước × 5 cột: Bước · Khách thấy/làm gì · Hệ thống làm gì [MÁY/NGƯỜI] · Người nào làm gì · Dữ liệu ghi đâu. Viết như kể chuyện có tên khách thật (tự đặt tên). Sau bảng: chỉ ra 2 bước RỦI RO RƠI KHÁCH cao nhất và vì sao.

[CONSTRAINT] Mỗi bước phải khớp tài sản tôi ĐANG có — không viết bước dùng thứ chưa xây (nếu cần thì ghi "⬜ tương lai"). Bước cuối bắt buộc khép vòng về lead mới hoặc tái mua. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** output kỳ vọng = 12 bước chị Mai như Demo Bước 2; 2 bước rủi ro = bước 7 ("suy nghĩ thêm" — rơi nếu follow-up không chạy) và bước 6 (booking→show — rơi nếu quên nhắc lịch).

### Prompt 3 — Chẩn đoán trạm FAIL trong Full System Test

```
[ROLE] Bạn là kỹ sư trực chiến hệ thống, chuyên xử lý sự cố theo nguyên tắc "khôi phục dòng chảy trước, sửa gốc sau".

[CONTEXT] Tôi đang chạy Full System Test 9 trạm. Hệ thống: RocketAgent + Zalo OA + Google Sheets + landing page {{nền tảng}}. Trạm FAIL: {{số + tên trạm}}.

[TASK] Chẩn đoán và hướng dẫn tôi sửa.

[INPUT] Kỳ vọng của trạm: {{ví dụ: tin Zalo xác nhận đến trong 1 phút}}. Thực tế: {{ví dụ: đến sau 9 phút}}. Các trạm trước đó: {{PASS/FAIL}}. Ảnh/mô tả thêm: {{tùy chọn}}.

[OUTPUT] (1) 3 nguyên nhân khả dĩ xếp theo xác suất, mỗi cái kèm cách kiểm tra ≤3 bước (bấm đâu, nhìn gì); (2) phương án CHẠY TẠM ngay hôm nay để khách thật không bị ảnh hưởng (thường là chuyển bước này sang [NGƯỜI-THEO-NHẮC]); (3) cách sửa gốc + cách test lại xác nhận; (4) 1 dòng đánh giá: lỗi này có chặn Demo Day ngày mai không, hay demo được với phương án tạm.

[CONSTRAINT] Ưu tiên tuyệt đối: không mất lead thật trong lúc sửa. Hướng dẫn từng bước cho người không rành công nghệ. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** trạm 4, tin đến sau 9' — output kỳ vọng: nguyên nhân #1 "gửi qua hàng đợi broadcast thay vì tin phản hồi tức thời — kiểm tra loại tin trong cấu hình RocketAgent"; chạy tạm: "Hà canh thông báo trạm 5 (đang PASS) và nhắn tay trong 5'"; đánh giá: "không chặn demo".

### Prompt 4 — Chuẩn hóa 8 SOP thành Operating Pack (Bonus)

```
[ROLE] Bạn là chuyên gia văn bản hóa quy trình cho SME — biến các ghi chú rời thành sổ tay vận hành nhân viên mới đọc là làm được.

[CONTEXT] Doanh nghiệp: {{tên + ngành + đội ngũ}}. Tôi có 8 SOP viết rải rác qua 4 tuần: {{dán 8 SOP: tạo content, đăng bài, xử lý lead, tư vấn, gửi proposal, follow-up, chăm sau mua, review dashboard}}.

[TASK] Chuẩn hóa 8 SOP về MỘT format thống nhất và gom thành SOP Operating Pack.

[INPUT] 8 SOP ở trên + Weekly Rhythm: {{dán lịch tuần}}.

[OUTPUT] (1) Mục lục pack; (2) mỗi SOP viết lại theo format thống nhất: Tên · Khi nào chạy (khớp với ô nào trong lịch tuần) · Ai làm · Input cần có · Các bước (đánh số, mỗi bước 1 hành động) · Output chuẩn · Lỗi hay gặp + cách xử lý · Agent/công cụ dùng; (3) bảng đối chiếu SOP × ô lịch tuần — SOP nào không nằm trong lịch tuần thì cảnh báo "SOP mồ côi" (sẽ không ai chạy).

[CONSTRAINT] Mỗi SOP ≤1 trang. Không thêm bước mới ngoài những gì SOP gốc có — chỉ chuẩn hóa, chỗ thiếu thì đánh dấu [CẦN BỔ SUNG] để tôi tự điền. Viết tiếng Việt.
```

## 9. 📋 SOP Thao Tác

**SOP-27 · Bảo trì hệ điều hành (meta-SOP — quy trình chăm sóc các quy trình):**

| Khi nào | Ai làm | Input → Các bước → Output |
|---|---|---|
| Hàng tuần (đã phân bổ trong Weekly Rhythm) | Cả đội | Lịch tuần → chạy đúng nhịp T2 số liệu / T3-T5 triển khai / T6 review / T7 nhập số → Output: một tuần vận hành đúng nhịp |
| Tháng đầu sau khóa: 2 tuần/lần | Chủ DN | OS Map → chạy lại Full System Test 9 trạm (30') → cập nhật Test Report → Output: phát hiện đứt gãy trước khách hàng |
| Từ tháng 2: mỗi tháng 1 lần | Chủ DN | OS Map + Test 9 trạm + Nhật ký lỗi agent → vá/tối ưu 1-2 điểm → Output: map cập nhật, ngày sửa ghi ở góc map |
| Khi thêm sản phẩm/kênh/nhân sự | Chủ DN | Thay đổi → cập nhật OS Map + Customer Flow + ô lịch tuần liên quan + KB → chạy test 9 trạm cho nhánh mới → Output: hệ thống nở ra có kiểm soát |
| Khi 1 người nghỉ/thay | Chủ DN | Weekly Rhythm + SOP Pack → bàn giao theo đúng các ô lịch có tên người đó → người mới chạy thử 1 tuần có giám sát → Output: hệ thống không phụ thuộc cá nhân |

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | OS Map đủ 12 khối 4 tầng trên 1 trang, khối chưa xây có đánh dấu ⬜ (8đ); 100% mũi tên có nhãn cơ chế [MÁY]/[NGƯỜI]/đỏ (8đ); Customer Flow ≥10 bước × 5 cột, bước cuối khép vòng (7đ); Test Report đủ 9 trạm có PASS/FAIL + ảnh từng trạm (7đ) |
| Chất lượng & độ sâu | 30 | Map có đủ 2 vòng lặp (tự tối ưu + referral) nhìn thấy được (8đ); mọi trạm FAIL đều có nguyên nhân + phương án (sửa xong hoặc kế hoạch sửa có hạn) — FAIL có xử lý KHÔNG bị trừ điểm, FAIL bỏ trống bị trừ (8đ); Weekly Rhythm mọi ô có người + phút, tổng giờ chủ DN ≤4h/tuần (8đ); 2 bước "rủi ro rơi khách" trong Flow được chỉ ra kèm lý do (6đ) |
| Cá nhân hoá vào DN thật | 25 | 12 khối là tài sản thật đã xây 26 ngày qua của chính DN (link/ảnh kiểm chứng được ngẫu nhiên 3 khối) (10đ); Customer Flow đúng hành trình ngành mình, không bê nguyên 12 bước spa (8đ); tên người trong Rhythm là đội thật, khớp vai từ Usage SOP Ngày 26 (7đ) |
| Dùng được ngay | 15 | Full System Test chạy bằng form/CRM/kênh THẬT, ảnh chụp là hệ thống thật không phải mockup (8đ); ≥1 mũi tên đỏ đã được vá ngay trong ngày (4đ); lịch tuần đã được gửi cho đội (ảnh tin nhắn nhóm) (3đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Map "trang trí": mọi mũi tên đều vẽ nét liền tự động trong khi thực tế nửa số đó là người làm — nhãn dối (−8đ nhóm 1).
2. Test Report 9/9 PASS không ảnh — mentor mặc định chưa chạy test thật (−7đ nhóm 4, yêu cầu chạy lại có ảnh).
3. Weekly Rhythm dồn 100% việc vào chủ DN dù có đội 5 người (−5đ nhóm 3 — chưa phân vai).
4. Customer Flow viết ở thì tương lai ("hệ thống SẼ gửi...") cho những khối đã xây — chứng tỏ chưa chạy thử (−5đ nhóm 2).
5. Vẽ thêm khối/tool chưa hề có mà không đánh dấu ⬜ (−4đ nhóm 3).

## 11. ❓ FAQ & Lỗi Thường Gặp

**FAQ:**
1. *"Một số khối của tôi chưa xây xong (ví dụ chưa có video assets) — hôm nay có làm được không?"* — Được và PHẢI làm: OS Map trung thực với ⬜ chính là bản đồ nợ tài sản để đưa vào kế hoạch 90 ngày (Ngày 28). Điều kiện tối thiểu để test 9 trạm chạy được: form + CRM + 1 kênh tin nhắn + dashboard — các thứ này Core các ngày trước đã bắt buộc có.
2. *"DN tôi một mình tôi làm hết (solo), phân vai kiểu gì?"* — Dùng bản Rhythm solo trong Template 3: phân vai theo KHUNG GIỜ thay vì con người ("8h30-9h: tôi đội mũ sale xử lý danh sách nhắc; 14h-15h thứ 3: tôi đội mũ content"). Agent Ngày 26 chính là "nhân sự" của bạn — solo là người hưởng lợi lớn nhất từ tầng AI.
3. *"Test 9 trạm có cần đăng bài công khai không? Tôi ngại khách thật thấy bài test."* — Không cần: đăng chế độ giới hạn (chỉ mình tôi/bạn bè), hoặc bỏ qua kênh đăng và bắt đầu từ trạm 2 bằng link form trực tiếp — ghi chú trong report "trạm 1 test riêng". Trạm 1 chỉ cần chứng minh: bài có link đúng.
4. *"Nhịp tuần đẹp trên giấy nhưng tuần nào cũng có việc đột xuất phá nhịp?"* — Nhịp tuần là XƯƠNG SỐNG chứ không phải xiềng xích: 2 ô bất khả xâm phạm là T2 sáng (đọc số + quyết định) và T7 (nhập số) — mất 2 ô này là mù; các ô khác xê dịch trong tuần được. Nếu 3 tuần liền phá nhịp cùng một ô → ô đó đặt sai giờ, sửa lịch chứ đừng tự trách.
5. *"OS này có chạy được khi tôi mở chi nhánh 2 / thêm dòng dịch vụ mới?"* — Đó chính là giá trị lớn nhất của việc văn bản hóa hôm nay: nhân bản = copy OS Map + SOP Pack + KB, đổi dữ liệu địa điểm/sản phẩm, tuyển người chạy theo Rhythm. Chi tiết nằm ở giai đoạn 3 của Kế hoạch 90 ngày (Ngày 28).
6. *"Tôi thấy hệ thống nhiều mảnh quá, sợ vận hành không nổi?"* — Nhìn lại con số của Rhythm: tổng giờ vai chủ ~3h/tuần, và 26 ngày qua bạn ĐÃ vận hành từng mảnh rồi — hôm nay chỉ xếp chúng vào lịch. Tháng đầu chỉ cần giữ 3 thứ: nhịp T2, danh sách nhắc hàng sáng, nhập số T7. Còn lại hệ thống tự nhắc bạn.

**Lỗi thường gặp:**
1. **Map vẽ hệ thống "ước mơ" thay vì hệ thống thật.** Phát hiện: khi mentor hỏi "mũi tên này chạy bằng gì?" thì trả lời "em định sẽ…". Sửa: quy ước ⬜ và nét đứt [NGƯỜI] — vẽ lại trung thực; map thật xấu hơn nhưng dùng được, map đẹp mà ảo thì Demo Day sẽ lộ.
2. **Test 9 trạm bằng trí tưởng tượng.** Phát hiện: report không ảnh, thời gian ghi tròn trịa "1 phút" ở mọi trạm. Sửa: bắt buộc SĐT phụ + ảnh chụp từng trạm; trạm 6 (follow-up hôm sau) cho phép ⚠️ "chờ xác nhận sáng mai" — trung thực hơn là ✅ khống.
3. **Nhịp tuần không khớp SOP đã có.** Phát hiện: SOP-25 nói "thứ 3 chăm sóc, thứ 5 upsell" nhưng lịch tuần lại dồn cả vào thứ 6. Sửa: dùng bảng đối chiếu SOP × ô lịch (Prompt 4) — mọi SOP phải có nhà trong lịch, mọi ô lịch phải chỉ về 1 SOP; phát hiện "SOP mồ côi" thì hoặc xếp lịch cho nó, hoặc thừa nhận không làm và archive.
4. **Vá mũi tên đứt bằng cách... thêm tool mới.** Phát hiện: học viên đòi cài thêm phần mềm thứ 4, thứ 5 vào đêm trước Demo Day. Sửa: luật của ngày 27 — chỉ được vá bằng 3 công cụ sẵn có hoặc [NGƯỜI-THEO-NHẮC]; tool mới là quyết định của giai đoạn 2 kế hoạch 90 ngày, có số liệu rồi mới mua.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 26 — Bộ AI Agent Cho Doanh Nghiệp]] · Ngày sau: [[Ngày 28 — Final Demo, Nghiệm Thu & Kế Hoạch 90 Ngày]]
- Lên MOC: [[_MOC 28 Day AIOS]]
- Tài sản hôm nay được dùng lại ở:
  - **Ngày 28 (ngay ngày mai):** OS Map là slide xương sống của Final Demo Deck; Full System Test Report là căn cứ chấm phần "hệ thống chạy thật" trong OS Completion Scorecard; các khối ⬜ và mũi tên đỏ chưa vá trở thành đầu việc của 30 ngày đầu trong Kế hoạch 90 ngày; Weekly Operating Rhythm chính là "chế độ lái" mà học viên cam kết chạy từ tuần sau.
  - **Sau khóa học:** SOP-27 (bảo trì hệ điều hành) là quy trình sống còn — hệ thống không được bảo trì sẽ mục sau 2-3 tháng; SOP Operating Pack (bonus) là tài liệu bàn giao khi tuyển nhân sự mới hoặc nhân bản chi nhánh.
