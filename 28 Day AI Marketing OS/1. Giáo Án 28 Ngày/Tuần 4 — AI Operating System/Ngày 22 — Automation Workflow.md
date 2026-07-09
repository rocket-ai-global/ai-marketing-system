---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 4
day: 22
core-output: "Automation Workflow Map (5 luồng), Lead Capture Automation chạy được, Sales Follow-up Automation chạy được, Automation Test Report"
---

# Ngày 22 — Automation Workflow

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Workflow dựng trên lớp động cơ Hermes/RocketAgent; sơ đồ workflow vẽ `.canvas` (skill `json-canvas`) lưu `03. Areas/` để cả đội đọc được.

> Hôm nay doanh nghiệp của bạn có bộ luồng tự động hóa đầu tiên: lead mới không bao giờ bị bỏ quên, sale không bao giờ quên follow-up, khách mua xong không bao giờ bị bỏ rơi — mà không cần thuê thêm người.

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay:

**Core Output (bắt buộc — điều kiện qua ngày):**
- **Automation Workflow Map (bản đồ luồng tự động hóa)**: sơ đồ 5 luồng tự động quan trọng nhất của doanh nghiệp mình, vẽ theo khung Trigger–Condition–Action, có ghi rõ ai nhận thông báo và dữ liệu lưu ở đâu.
- **Lead Capture Automation (tự động hóa thu lead)** CHẠY ĐƯỢC: khách điền form → vào CRM → nhận tin xác nhận → sale được nhắc. Test bằng lead giả thành công.
- **Sales Follow-up Automation (tự động hóa nhắc bám đuổi)** CHẠY ĐƯỢC: lead chưa chốt → hệ thống tự nhắc người phụ trách đúng lịch (24h – 3 ngày – 7 ngày).
- **Automation Test Report (báo cáo kiểm thử)**: bảng ghi kết quả test từng luồng — chạy đúng/sai ở bước nào.

**Bonus Output (nâng cao):**
- **Customer Onboarding Automation (tự động hóa chăm sóc sau mua)**: khách mua → chuỗi tin ngày 0/3/7/14 (sẽ hoàn thiện tiếp ở Ngày 25).
- Luồng "đánh thức khách ngủ đông" (khách >60 ngày không tương tác).

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Automation là gì và vì sao chủ SME cần nó (5')
- **Ý chính:** Automation (tự động hóa) = giao những việc LẶP LẠI, CÓ QUY TẮC RÕ cho máy làm, để việc luôn được làm đúng giờ, không phụ thuộc trí nhớ con người.
- **Cách giảng — analogy Sen Spa:** "Chị Lan có 6 nhân viên. Không ai trong số đó có nhiệm vụ 'nhớ nhắn tin lại cho khách hỏi giá hôm thứ 3 tuần trước'. Kết quả: Sen Spa mất trung bình 10/45 lead mỗi tháng chỉ vì QUÊN. 10 lead × tỷ lệ chốt 30% × liệu trình 12tr = **36 triệu/tháng bay hơi vì trí nhớ**. Automation là nhân viên lễ tân không bao giờ ngủ, không bao giờ quên, lương 0 đồng."
- Chốt tư duy: automation không thay con người tư vấn — nó đảm bảo con người **không bỏ sót cơ hội để tư vấn**.

### Khối 2 — Nên và không nên tự động hóa cái gì (5')
Bảng hai cột, giảng nhanh bằng ví dụ Sen Spa:

| ✅ NÊN tự động | ❌ KHÔNG nên tự động |
|---|---|
| Tin xác nhận khi khách điền form ("Sen Spa đã nhận thông tin của chị…") | Tư vấn chốt liệu trình 12-15tr (cần người thật) |
| Nhắc sale gọi lead mới trong 15 phút | Xử lý khiếu nại, khách giận |
| Nhắc follow-up lead chưa chốt (24h/3 ngày/7 ngày) | Trả lời câu hỏi y khoa/da liễu chuyên sâu |
| Nhắc lịch hẹn trước 24h và 2h | Thương lượng giá |
| Tin chăm sóc sau buổi trị liệu (ngày 0/3/7) | Tin nhắn cần cảm xúc thật (chia buồn, sự cố) |
| Gắn tag nguồn lead, cập nhật trạng thái CRM | Quyết định chiến lược |

- **Quy tắc vàng:** *"Chỉ tự động hóa quy trình đã chạy tay ổn ít nhất 1 tuần."* Tự động hóa một quy trình lộn xộn = làm việc sai nhanh hơn.

### Khối 3 — Ngôn ngữ chung của mọi automation: Trigger – Condition – Action (8')
- **Trigger (điểm kích hoạt):** sự kiện làm luồng bắt đầu chạy. Ví dụ: "khách điền form", "trạng thái CRM đổi thành Đã mua", "đến 9h sáng thứ 2".
- **Condition (điều kiện):** bộ lọc quyết định rẽ nhánh. Ví dụ: "NẾU nguồn = Facebook Ads thì gắn tag FB; NẾU lead score ≥ 8 thì báo ngay cho Lan".
- **Action (hành động):** việc máy làm. Ví dụ: thêm dòng vào Google Sheets, gửi tin Zalo, gửi thông báo cho sale.
- **Cách giảng:** mọi luồng, dù phức tạp đến đâu, đều đọc được thành 1 câu: **"KHI [trigger], NẾU [condition], THÌ [action], VÀ báo cho [người], LƯU vào [nơi]."** Cho cả lớp đọc to câu này 1 lần — đây là câu thần chú của cả ngày.
- Bổ sung 2 trường bắt buộc khi vẽ luồng: **Owner (người nhận thông báo/chịu trách nhiệm)** và **Error handling (khi lỗi thì sao)** — ví dụ: nếu tin Zalo gửi thất bại → hệ thống báo cho Hà gọi điện tay.

### Khối 4 — Bộ công cụ VN-friendly, không cần code (7')
- **Nguyên tắc:** dùng công cụ ĐANG CÓ, luồng đơn giản nhất chạy được. Không dạy Zapier/n8n trong khóa này — SME Việt cần luồng sống được 6 tháng không cần kỹ thuật viên.
- Bộ 3 công cụ chuẩn của khóa:
  1. **RocketAgent (OPC) workflow**: trigger từ chatbot/form → gắn tag, cập nhật CRM, gửi thông báo. Đây là xương sống.
  2. **Zalo OA (Official Account — tài khoản chính thức Zalo)**: kênh gửi tin xác nhận, nhắc lịch, chăm sóc — người Việt mở Zalo nhiều hơn email 10 lần.
  3. **Google Sheets**: nơi lưu dữ liệu CRM (đã dựng ở Ngày 16) + cột "Ngày follow-up tiếp theo" làm bộ nhắc.
- **Phương án thay thế khi RocketAgent chưa có tính năng tương ứng:** nhắc việc bằng Google Calendar (lặp lại), tin nhắn mẫu lưu sẵn trong Zalo OA (tin nhắn nhanh), checklist giấy dán quầy lễ tân cho bước thủ công. Ghi rõ trong Workflow Map bước nào là **máy làm** và bước nào là **người làm theo nhắc** — luồng "bán tự động" vẫn tính là đạt.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 21 | Khoe 2-3 Sales Playbook tốt nhất từ Demo Day 3; nhắc các bạn 🔧 nộp bản sửa. Câu hỏi mở màn: "Tuần trước ai QUÊN follow-up ít nhất 1 lead? Giơ tay." (thường là cả lớp) |
| 25' | Giảng kiến thức trọng tâm | 4 khối ở mục 2. Trọng tâm: câu thần chú Trigger–Condition–Action và bảng nên/không nên |
| 30' | Demo live trên Sen Spa | Dựng Lead Capture Automation + Sales Follow-up Automation chạy thật (kịch bản mục 4), test bằng lead giả ngay trên màn hình |
| 15' | Học viên làm tại chỗ + Q&A | Mỗi người viết xong câu thần chú cho 2 luồng đầu tiên của DN mình vào Template 1; trainer đi từng người duyệt trigger |
| 10' | Giao bài tập | Chiếu deliverable + rubric + deadline 23h59. Nhấn mạnh: "Luồng chạy được 80% ăn đứt sơ đồ đẹp 100% nằm trên giấy" |

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

> Bối cảnh demo: Sen Spa — spa chăm sóc da tại Hà Nội, chủ là chị Lan, 6 nhân viên (Lan kiêm tư vấn chốt liệu trình; Hà — lễ tân kiêm trực fanpage/Zalo; 4 kỹ thuật viên). AOV 1.5tr/buổi, liệu trình 8-12 buổi giá 12-15tr. Lead từ Facebook + giới thiệu. Tài sản đã có từ tuần trước: form lead magnet "Cẩm nang phục hồi da sau mụn 7 ngày" (Ngày 12), CRM Google Sheets (Ngày 16), chatbot RocketAgent (Ngày 17).

**Bước 1 (5') — Vẽ Workflow Map luồng 1 trên màn hình.**
- Làm gì: mở Template 1, điền luồng "Lead mới điền form" bằng câu thần chú.
- Công cụ: Google Sheets/slide trắng.
- Kết quả trông như thế nào:

```
LUỒNG 1 — LEAD MỚI ĐIỀN FORM (Sen Spa)
KHI:   khách điền form "Cẩm nang phục hồi da sau mụn"
NẾU:   số điện thoại hợp lệ (10 số)
THÌ:   (1) thêm dòng vào CRM Sheets, cột Nguồn = "FB - Lead magnet"
       (2) gửi tin Zalo xác nhận + link tài liệu (trong 1 phút)
       (3) gắn tag "lead-moi" trên RocketAgent
BÁO:   Hà nhận thông báo → gọi lại trong 15 phút giờ hành chính
LƯU:   CRM Sheets, tab "Lead", trạng thái = "Mới"
LỖI:   tin Zalo gửi fail → RocketAgent báo Hà nhắn tay theo mẫu M1
```

**Bước 2 (8') — Dựng luồng đó chạy thật trên RocketAgent.**
- Làm gì: vào RocketAgent → mục Workflow → tạo workflow mới → chọn trigger "Form submitted" → thêm action "Update CRM/Sheet" → action "Send Zalo message" (dán tin mẫu M1 bên dưới) → action "Notify staff" chọn Hà.
- Công cụ: RocketAgent (OPC). Nếu tính năng nối Sheets chưa bật: demo phương án thay thế — form Google Forms ghi thẳng vào Sheets, Hà nhận email thông báo mặc định của Forms, tin Zalo gửi bằng tin nhắn nhanh lưu sẵn.
- Kết quả: workflow hiện 4 khối nối nhau trên màn hình, trạng thái "Active".

Tin mẫu M1 (tin xác nhận):
> "Sen Spa chào chị {{tên}} ạ 🌸 Spa đã nhận đăng ký của chị. Đây là Cẩm nang phục hồi da sau mụn 7 ngày chị nhé: {{link}}. Trong hôm nay bạn Hà bên spa sẽ gọi chị 1 cuộc ngắn (2-3 phút) để hỏi tình trạng da và gửi chị lộ trình phù hợp. Chị tiện nghe máy khung giờ nào ạ?"

**Bước 3 (7') — Dựng Sales Follow-up Automation.**
- Làm gì: trong CRM Sheets thêm 2 cột "Ngày liên hệ cuối" + "Follow-up tiếp theo" (công thức: ngày cuối +1, +3, +7 tùy trạng thái). RocketAgent đặt lịch quét 8h30 sáng: lead nào đến hạn → gửi danh sách cho Lan + Hà qua Zalo.
- Kết quả: mỗi sáng Lan nhận 1 tin: "Hôm nay cần follow-up 4 lead: [tên — trạng thái — ghi chú lần trước]". Không ai phải nhớ gì cả.

**Bước 4 (7') — Test bằng lead giả, điền Test Report ngay.**
- Làm gì: trainer tự điền form bằng SĐT phụ → cả lớp quan sát: dòng mới xuất hiện trong Sheets? Tin Zalo đến trong 1 phút? Hà nhận thông báo?
- Kết quả: điền 1 dòng vào Automation Test Report (Template 3): luồng 1 — 3/3 bước PASS (đạt), hoặc ghi rõ bước fail.

**Bước 5 (3') — Chốt thông điệp.**
- "Sen Spa vừa bịt lỗ rò 36 triệu/tháng trong 30 phút. Tối nay các bạn bịt lỗ của mình."

> **Thích ứng ngành khác:** Nha khoa — trigger quan trọng nhất là "đặt lịch khám" → nhắc lịch trước 24h/2h (giảm no-show — khách hẹn nhưng không đến). Giáo dục/coaching — trigger "đăng ký học thử" → gửi tài liệu + nhắc trước buổi học thử. Gym — trigger "hết hạn gói tập còn 7 ngày" → luồng gia hạn. Bản chất Trigger–Condition–Action không đổi, chỉ đổi sự kiện.

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

**Cụm A — Chọn & vẽ 5 luồng (45'):**
- [ ] Liệt kê các điểm "hay quên/hay sót" trong 7 tình huống: lead mới điền form · lead inbox cần tư vấn · lead nóng · khách đã mua · khách cần chăm lại · khách lâu không tương tác · khách cần upsell (bán thêm) (10')
- [ ] Chọn đúng 5 luồng ưu tiên (bắt buộc có: lead mới + follow-up sale; còn lại tự chọn theo chỗ đau nhất) (5')
- [ ] Điền Template 1 cho cả 5 luồng theo câu thần chú KHI–NẾU–THÌ–BÁO–LƯU–LỖI (30')

**Cụm B — Dựng 2 luồng chạy thật (45'):**
- [ ] Dựng Lead Capture Automation: form → CRM → tin xác nhận → thông báo người phụ trách (25')
- [ ] Dựng Sales Follow-up Automation: thêm cột follow-up vào CRM + đặt nhắc sáng hàng ngày (20')

**Cụm C — Test & báo cáo (30'):**
- [ ] Tự đóng vai khách: điền form bằng SĐT phụ, đi hết luồng (10')
- [ ] Điền Automation Test Report: từng bước PASS/FAIL, ảnh chụp màn hình bằng chứng (15')
- [ ] Sửa 1 lỗi lớn nhất phát hiện được, test lại (5')

Tổng Core: ~2h. **Bonus (+30'):** dựng luồng Customer Onboarding (khách mua → tin ngày 0/3/7) — dùng lại tin mẫu M4-M6 trong Template 2.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Trên doanh nghiệp của bạn: (1) hoàn thiện Automation Workflow Map 5 luồng; (2) đưa 2 luồng (Lead Capture + Sales Follow-up) vào chạy thật; (3) test bằng lead giả và lập Test Report.

**Deliverable nộp (vào thread cohort, deadline 23h59 hôm nay):**
1. `[Tên DN] — Ngày 22 — Automation Workflow Map` (file/link Template 1 đã điền 5 luồng)
2. `[Tên DN] — Ngày 22 — Video Test Automation` (video quay màn hình ≤3 phút: điền form giả → chỉ vào dòng CRM mới + tin xác nhận đã đến + thông báo sale nhận được)
3. `[Tên DN] — Ngày 22 — Automation Test Report` (Template 3 đã điền, kèm ≥3 ảnh chụp màn hình)

Bonus nộp thêm: `[Tên DN] — Ngày 22 — Onboarding Automation` (ảnh luồng + 3 tin mẫu).

## 7. 📄 Template Đi Kèm

**Template 1 — Automation Workflow Map** (Google Sheets/bảng Markdown)
Mỗi luồng 1 khối, các trường: `Tên luồng · KHI (trigger) · NẾU (condition) · THÌ (action 1-2-3) · BÁO (owner + thời hạn phản ứng) · LƯU (nơi lưu dữ liệu) · LỖI (phương án khi fail) · Máy làm hay người làm theo nhắc?`. Có sẵn 5 luồng Sen Spa điền mẫu (luồng 1 như mục 4; luồng 2 "inbox cần tư vấn" — chatbot không trả lời được 2 lượt → chuyển Hà; luồng 3 "lead nóng ≥8 điểm" — báo thẳng Lan trong 5'; luồng 4 "khách chốt liệu trình" — tin cảm ơn + lịch buổi 1 + hướng dẫn trước buổi; luồng 5 "khách 60 ngày không quay lại" — tin hỏi thăm + ưu đãi tái khám da miễn phí).

**Template 2 — Bộ Tin Nhắn Tự Động (Message Pack)**
8 tin mẫu đã viết sẵn cho Sen Spa, học viên thay {{tên spa}}, {{sản phẩm}}, {{link}}: M1 xác nhận form · M2 xác nhận booking (đặt lịch hẹn) · M3 nhắc lịch trước 24h · M4 cảm ơn sau mua · M5 hỏi trải nghiệm ngày 3 · M6 giá trị bổ sung ngày 7 · M7 đánh thức khách ngủ đông · M8 nhắc follow-up nội bộ gửi sale (format: tên — trạng thái — việc cần làm).

**Template 3 — Automation Test Report**
Bảng: `Luồng · Bước · Kỳ vọng · Kết quả thực tế · PASS/FAIL · Ảnh bằng chứng · Lỗi & cách sửa · Ngày test · Người test`. Kèm 1 luồng Sen Spa điền mẫu có cả dòng FAIL ("tin Zalo không gửi do khách chưa quan tâm OA → sửa: thêm bước mời quan tâm OA vào form cảm ơn").

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Thiết kế 5 workflow ưu tiên cho doanh nghiệp

```
[ROLE] Bạn là chuyên gia tự động hóa vận hành cho SME ngành dịch vụ bán qua tư vấn, hiểu rõ nguồn lực mỏng của doanh nghiệp nhỏ Việt Nam.

[CONTEXT] Doanh nghiệp của tôi:
- Tên & ngành: {{tên DN, ngành}}
- Quy mô: {{số nhân viên, ai trực page/Zalo, ai tư vấn chốt}}
- Phễu hiện tại: {{mô tả đường đi của khách từ lead đến mua}}
- Công cụ đang dùng: RocketAgent, Zalo OA, Google Sheets CRM
- Những chỗ đang hay QUÊN/SÓT: {{liệt kê 3-5 chỗ đau}}

[TASK] Đề xuất đúng 5 workflow tự động hóa ưu tiên nhất, xếp theo tác động doanh thu giảm dần.

[INPUT] Danh sách 7 tình huống chuẩn: lead mới điền form, lead inbox cần tư vấn, lead nóng, khách đã mua, khách cần chăm lại, khách lâu không tương tác, khách cần upsell.

[OUTPUT] Với mỗi workflow, viết đúng format:
- Tên luồng + 1 câu lý do ưu tiên (ước tính tiền đang mất)
- KHI (trigger) / NẾU (condition) / THÌ (tối đa 3 action) / BÁO (ai, phản ứng trong bao lâu) / LƯU (ở đâu) / LỖI (phương án dự phòng)
- Gắn nhãn từng action: [MÁY] hoặc [NGƯỜI-THEO-NHẮC]

[CONSTRAINT] Chỉ dùng RocketAgent + Zalo OA + Google Sheets. Không đề xuất Zapier/n8n/Make. Mỗi luồng tối đa 3 action — nếu cần hơn, tách luồng. Viết tiếng Việt, ngắn gọn để chủ DN đọc 5 phút hiểu ngay.
```

**Ví dụ đã điền (Sen Spa):** `{{tên DN, ngành}}` = "Sen Spa — spa chăm sóc da, Hà Nội"; `{{quy mô}}` = "6 người: Lan (chủ, tư vấn chốt), Hà (lễ tân + trực page/Zalo), 4 kỹ thuật viên"; `{{phễu}}` = "Lead FB/giới thiệu → inbox/form → booking → tư vấn tại spa → chốt liệu trình 8-12 buổi 12-15tr → tái mua/upsell"; `{{chỗ đau}}` = "quên gọi lại lead sau 24h; khách hẹn rồi không đến không ai nhắc; khách xong liệu trình không ai mời gói duy trì; inbox ngoài giờ sáng hôm sau mới trả lời".

### Prompt 2 — Viết bộ tin nhắn tự động đúng giọng thương hiệu

```
[ROLE] Bạn là copywriter (người viết quảng cáo) chuyên viết tin nhắn Zalo/Messenger cho ngành dịch vụ chăm sóc cá nhân tại Việt Nam.

[CONTEXT] Doanh nghiệp: {{tên DN + mô tả 2 câu}}. Khách hàng chính: {{chân dung ngắn}}. Giọng thương hiệu: {{ví dụ: thân tình như người quen, gọi khách là "chị", dùng emoji tiết chế}}.

[TASK] Viết 8 tin nhắn tự động: (1) xác nhận điền form + gửi tài liệu, (2) xác nhận đặt lịch, (3) nhắc lịch trước 24h, (4) cảm ơn sau mua + hướng dẫn, (5) hỏi trải nghiệm ngày 3, (6) gửi giá trị bổ sung ngày 7, (7) đánh thức khách 60 ngày không quay lại, (8) tin nhắc việc nội bộ gửi cho sale.

[INPUT] Sản phẩm/dịch vụ chính: {{tên + giá}}. Tài liệu lead magnet: {{tên}}. Ưu đãi tái kích hoạt được phép dùng: {{ví dụ: 1 buổi soi da miễn phí}}.

[OUTPUT] Mỗi tin: tiêu đề nội bộ + nội dung ≤4 câu + biến {{tên khách}}/{{link}} đặt đúng chỗ + thời điểm gửi. Tin 1-7 kết bằng 1 câu hỏi mở để khách dễ trả lời.

[CONSTRAINT] Không viết như thông báo hành chính. Không dùng "Quý khách". Tin nhắc lịch phải có nút đường lùi ("nếu chị bận, nhắn em đổi lịch giúp ạ"). Không hứa hẹn kết quả điều trị tuyệt đối (từ cấm: "cam kết hết mụn 100%").
```

**Ví dụ đã điền (Sen Spa):** giọng = "thân tình, gọi khách là 'chị', xưng 'em/Sen Spa', 1 emoji hoa 🌸 mỗi tin"; ưu đãi tái kích hoạt = "buổi soi da + tư vấn phục hồi miễn phí trị giá 300k". Kết quả kỳ vọng: 8 tin kiểu tin M1 ở mục 4.

### Prompt 3 — Tạo kế hoạch kiểm thử automation

```
[ROLE] Bạn là tester (người kiểm thử) khó tính chuyên phá automation của SME trước khi khách thật phá.

[CONTEXT] Tôi vừa dựng các workflow sau: {{dán Workflow Map 5 luồng}}. Công cụ: RocketAgent + Zalo OA + Google Sheets.

[TASK] Tạo kế hoạch test đầy đủ cho 2 luồng đang chạy thật (Lead Capture + Sales Follow-up).

[INPUT] Nội dung 2 luồng ở trên.

[OUTPUT] Bảng test case (kịch bản kiểm thử): STT · Kịch bản · Bước thao tác · Kỳ vọng · Cách xác nhận (nhìn vào đâu). Bao gồm tối thiểu: 1 ca "đường vui" (mọi thứ đúng), 3 ca dữ liệu xấu (SĐT sai/thiếu, điền form 2 lần, tên có ký tự lạ), 2 ca thời gian (điền form 11h đêm, ngày lễ), 1 ca lỗi kênh (khách chưa quan tâm Zalo OA).

[CONSTRAINT] Tối đa 12 test case. Mỗi ca phải chỉ rõ "nhìn vào đâu để biết PASS" — không chấp nhận kỳ vọng mơ hồ kiểu "hệ thống hoạt động tốt". Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** ca lỗi kênh cho Sen Spa = "khách điền form nhưng chưa từng quan tâm Zalo OA Sen Spa → kỳ vọng: hệ thống báo Hà trong 5 phút để nhắn tay qua Messenger; nhìn vào: thông báo trong nhóm Zalo nội bộ 'Sen Spa Vận Hành'".

### Prompt 4 — Chẩn đoán luồng bị lỗi

```
[ROLE] Bạn là kỹ sư tự động hóa kiên nhẫn, chuyên hướng dẫn người không rành công nghệ sửa lỗi từng bước.

[CONTEXT] Workflow của tôi: {{dán mô tả luồng theo KHI-NẾU-THÌ-BÁO-LƯU}}. Hiện tượng lỗi: {{mô tả: bước nào chạy, bước nào không, ảnh chụp màn hình nếu có}}.

[TASK] Chẩn đoán nguyên nhân khả dĩ và cho tôi các bước kiểm tra theo thứ tự dễ → khó.

[INPUT] Hiện tượng ở trên + công cụ: RocketAgent, Zalo OA, Google Sheets.

[OUTPUT] (1) 3-5 nguyên nhân khả dĩ xếp theo xác suất; (2) với mỗi nguyên nhân: cách kiểm tra trong ≤3 bước, bấm vào đâu, nhìn thấy gì thì kết luận gì; (3) nếu tất cả đều không phải: 1 phương án chạy tay tạm thời để không mất lead trong lúc chờ sửa.

[CONSTRAINT] Không dùng thuật ngữ kỹ thuật chưa giải thích. Mỗi bước kiểm tra viết như hướng dẫn cho người lần đầu dùng máy tính. Luôn ưu tiên "không mất lead" hơn "sửa triệt để ngay".
```

## 9. 📋 SOP Thao Tác

**SOP-22 · Vận hành & bảo trì automation** — dùng lặp lại sau khóa học:

| Khi nào | Ai làm | Input → Các bước → Output |
|---|---|---|
| Mỗi sáng 8h30 (hàng ngày) | Lễ tân/sale (Sen Spa: Hà) | Tin nhắc tự động → mở danh sách follow-up đến hạn → gọi/nhắn theo tin mẫu → cập nhật trạng thái CRM → Output: 0 lead quá hạn cuối ngày |
| Thứ 6 hàng tuần, 15' | Chủ DN (Lan) | CRM + Test Report → soi 3 câu: có lead nào kẹt >3 ngày không ai chạm? tin tự động nào bị khách phàn nàn? luồng nào fail trong tuần? → Output: ≤3 việc sửa cho tuần sau |
| Khi thêm sản phẩm/kênh mới | Chủ DN + người trực kênh | Điền Template 1 cho luồng mới → chạy tay 1 tuần → tự động hóa → test bằng lead giả → Output: luồng mới có dòng trong Test Report |
| Mỗi quý | Chủ DN | Toàn bộ Workflow Map → tắt luồng không còn dùng, gộp luồng trùng → Output: Map gọn, mọi luồng đều sống |

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Workflow Map đủ 5 luồng, mỗi luồng đủ 6 trường KHI/NẾU/THÌ/BÁO/LƯU/LỖI (12đ — thiếu 1 trường/luồng trừ 1đ); video test ≤3 phút cho thấy đủ 3 bằng chứng: dòng CRM mới + tin xác nhận + thông báo sale (12đ — thiếu 1 bằng chứng trừ 4đ); Test Report ≥6 test case có kết quả PASS/FAIL (6đ) |
| Chất lượng & độ sâu | 30 | Trigger cụ thể, kiểm chứng được — không chấp nhận "khi có khách quan tâm" (10đ); mỗi luồng có xử lý LỖI thực tế, không để trống hoặc ghi "báo admin" chung chung (10đ); từng action gắn nhãn [MÁY]/[NGƯỜI-THEO-NHẮC] đúng thực tế công cụ đang có (10đ) |
| Cá nhân hoá vào DN thật | 25 | Dùng form/CRM/kênh THẬT của DN mình, không dùng nguyên dữ liệu Sen Spa (10đ); 5 luồng chọn theo chỗ đau đã nêu, có ghi ước tính thiệt hại khi không tự động (8đ); tin nhắn tự động đúng xưng hô + giọng thương hiệu DN (7đ) |
| Dùng được ngay | 15 | 2 luồng Core đang ở trạng thái BẬT tại thời điểm nộp (8đ); tin nhắc follow-up nội bộ chỉ rõ tên người nhận thật trong đội (4đ); có phương án chạy tay khi công cụ lỗi (3đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Sơ đồ đẹp nhưng không có gì chạy thật — video test là bắt buộc (−12đ nhóm 1).
2. Trigger mơ hồ: "khi khách có nhu cầu" (−5đ/luồng, nhóm 2).
3. Tự động hóa cả bước tư vấn chốt sale bằng tin nhắn hàng loạt (−10đ nhóm 2 — vi phạm bảng nên/không nên).
4. Copy nguyên 8 tin Sen Spa, còn nguyên chữ "Sen Spa"/"chị" trong ngành xưng hô khác (−7đ nhóm 3).
5. Test Report toàn PASS, 0 ca dữ liệu xấu (−4đ nhóm 1 — test chưa thật).

## 11. ❓ FAQ & Lỗi Thường Gặp

**FAQ:**
1. *"Tôi không có Zalo OA, dùng Messenger được không?"* — Được. Nguyên tắc: dùng kênh khách bạn đang ở đông nhất. Zalo OA chỉ là mặc định vì tỷ lệ mở tin cao; luồng KHI-NẾU-THÌ giữ nguyên, đổi action gửi tin sang Messenger/SMS.
2. *"RocketAgent gói của tôi chưa có workflow tự động, làm sao đạt Core?"* — Dùng mô hình "người-theo-nhắc": Google Forms tự ghi vào Sheets (miễn phí, tự động thật), tin xác nhận là tin nhắn nhanh lưu sẵn Hà bấm gửi trong 15', nhắc follow-up bằng cột công thức + xem Sheet mỗi sáng theo SOP. Gắn nhãn [NGƯỜI-THEO-NHẮC] trung thực — vẫn đạt điểm, vì hệ thống nằm ở QUY TRÌNH, không nằm ở tool.
3. *"Tự động nhắn nhiều thế khách có khó chịu không?"* — Đếm lại: khách mới nhận 2 tin (xác nhận + 1 nhắc), khách mua nhận 3-4 tin trong 14 ngày, tin nào cũng có giá trị (tài liệu, nhắc lịch, hỏi thăm). Khó chịu đến từ tin VÔ NGHĨA lặp lại, không phải từ số lượng. Quy tắc: mỗi tin phải trả lời được "khách nhận được gì từ tin này?".
4. *"Nên tự động hóa hết 7 tình huống luôn cho nhanh?"* — Không. Tuần này 2 luồng chạy thật + 3 luồng trên giấy. Mỗi tuần sau khóa bật thêm 1 luồng. Bật 7 luồng cùng lúc = không biết luồng nào gây lỗi khi có vấn đề.
5. *"Nhân viên sợ automation làm mất việc của họ?"* — Cho nhân viên xem bảng nên/không nên: máy làm phần NHỚ và NHẮC, người làm phần TƯ VẤN và QUAN HỆ — phần được trả lương cao hơn. Ở Sen Spa, Hà thoát khỏi việc ghi chép tay và có thêm giờ gọi lead nóng.
6. *"Khách điền form lúc 11h đêm, tin tự động gửi luôn có sao không?"* — Tin xác nhận tự động gửi ngay là bình thường (khách vừa bấm gửi, đang chờ). Nhưng CUỘC GỌI thì đặt điều kiện giờ hành chính: NẾU ngoài 8h-19h THÌ đưa vào danh sách gọi 8h30 sáng mai.

**Lỗi thường gặp:**
1. **Tin Zalo không đến khách.** Phát hiện: Test Report ca "khách chưa quan tâm OA" fail; khách bảo không nhận được gì. Sửa: Zalo OA chỉ nhắn được người đã quan tâm/tương tác — thêm bước "mời quan tâm OA" vào trang cảm ơn của form, và luôn có đường lùi báo người trực nhắn tay.
2. **Lead trùng — khách điền form 2 lần thành 2 dòng CRM, bị gọi 2 lần.** Phát hiện: lọc CRM theo SĐT thấy trùng. Sửa: thêm điều kiện "NẾU SĐT đã tồn tại THÌ cập nhật dòng cũ + gắn tag 'quan tâm lại', không tạo dòng mới, không gửi lại tin xác nhận".
3. **Nhắc follow-up dồn cục — sáng thứ 2 sale nhận 30 việc nhắc, tê liệt.** Phát hiện: tin nhắc dài hơn 10 dòng. Sửa: giới hạn danh sách nhắc 10 lead/ngày xếp theo lead score giảm dần; lead nguội hơn đẩy sang luồng nuôi dưỡng tự động thay vì nhắc gọi.
4. **Sửa tên cột trong Google Sheets làm automation chết im lặng.** Phát hiện: đột nhiên vài ngày không có lead mới vào Sheet dù ads vẫn chạy. Sửa: khóa hàng tiêu đề (protect range), ghi vào SOP "không đổi tên cột"; mỗi sáng Hà kiểm tra chéo số form mới vs số dòng mới.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 21 — Sales Engine Review & Demo Day 3]] · Ngày sau: [[Ngày 23 — KPI Dashboard]]
- Lên MOC: [[_MOC 28 Day AIOS]]
- Tài sản hôm nay được dùng lại ở:
  - **Ngày 23:** dữ liệu automation ghi vào CRM/Sheets chính là nguồn số liệu nuôi KPI Dashboard.
  - **Ngày 25:** Customer Onboarding Automation (bonus hôm nay) được nâng cấp thành Customer Success Journey đầy đủ 0-90 ngày.
  - **Ngày 26:** tin nhắc follow-up nội bộ trở thành đầu vào cho AI Sales Agent và AI CRM Agent.
  - **Ngày 27:** 5 luồng hôm nay là các "mạch máu" nối các khối trong OS Map; Test Report hôm nay là tiền thân của Full System Test.
  - **Ngày 28:** Automation là 1 mục nghiệm thu trong OS Completion Scorecard.
