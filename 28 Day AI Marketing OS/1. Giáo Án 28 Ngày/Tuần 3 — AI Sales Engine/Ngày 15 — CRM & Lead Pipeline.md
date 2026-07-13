---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 3
day: 15
core-output: "CRM Base (Google Sheets/RocketAgent) + Lead Pipeline 9 trạng thái + 20 lead thật đã nhập + CRM Usage SOP 1 trang"
---

# Ngày 15 — CRM & Lead Pipeline

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** CRM notes-based CÓ SẴN trong vault: mỗi khách 1 file `People/` (ghi PK), công ty → `Companies/`; pipeline tại `03. Areas/Sales Pipeline & CRM/` + dashboard `.base` (skill `obsidian-bases`); toàn cảnh tại `MOC/MOC Sales Pipeline.md`.

> Hôm nay bạn xây "két sắt khách hàng" cho doanh nghiệp: một CRM đơn giản mà mọi lead đi vào đều được ghi lại, có trạng thái, có người phụ trách, có ngày follow-up — không còn lead nào chết trong inbox.

---

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày 15, học viên CÓ TRONG TAY:

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **CRM Base**: 1 bảng CRM chạy được trên Google Sheets (hoặc CRM trong RocketAgent nếu đã quen), có đủ 12 trường dữ liệu chuẩn.
- ✅ **Lead Pipeline (đường ống khách hàng tiềm năng)**: 9 trạng thái từ "Lead mới" → "Đã chốt", viết đúng theo phễu của doanh nghiệp mình.
- ✅ **20 lead thật đã nhập** (lead cũ trong inbox Facebook/Zalo + khách cũ + khách đang hỏi) — để CRM có dữ liệu sống ngay hôm nay.
- ✅ **CRM Usage SOP**: 1 trang quy định "ai nhập, khi nào nhập, nhập gì" cho đội ngũ.

**Bonus Output (nâng cao):**
- ⭐ Nhập đủ 40 lead (20 lead cũ + 10 khách cũ + 10 khách tiềm năng mới).
- ⭐ Dashboard mini: bộ lọc theo trạng thái + bảng đếm lead theo nguồn (dùng hàm COUNTIF có sẵn trong template).

---

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — CRM là gì và vì sao SME mất tiền vì không có nó (7 phút giảng)

- **CRM (Customer Relationship Management — quản lý quan hệ khách hàng)** = nơi DUY NHẤT lưu toàn bộ khách hàng và trạng thái của họ. Không phải phần mềm đắt tiền — với SME, một bảng Google Sheets kỷ luật tốt hơn một Salesforce bỏ hoang.
- **Analogy giảng**: Inbox Facebook của Sen Spa giống cái rổ đựng cá — cá nhảy vào rồi nhảy ra, không ai đếm. CRM là bể cá có ngăn: con nào mới vào, con nào sắp bắt được, con nào cần cho ăn thêm — nhìn 1 phát biết ngay.
- **Con số đánh thức** (dùng khi giảng): Sen Spa mỗi tháng có ~60 người inbox hỏi. Bạn tư vấn giỏi nhất (Ngọc) chỉ nhớ và theo được ~15 người. 45 người còn lại trôi mất. Nếu chỉ 10% trong số 45 người đó chốt liệu trình 12tr → **54 triệu/tháng đang rơi vãi vì không có CRM**. Đây không phải chi phí công nghệ — đây là tiền nhặt lại.

### Khối 2 — Lead Pipeline: 9 trạng thái chuẩn cho doanh nghiệp bán qua tư vấn (8 phút)

Pipeline = các "trạm" mà một khách hàng đi qua từ lúc là người lạ đến lúc trả tiền. Với ngành dịch vụ bán qua tư vấn, dùng 9 trạng thái:

| # | Trạng thái | Nghĩa là gì (ví dụ Sen Spa) |
|---|---|---|
| 1 | Lead mới | Vừa inbox/điền form, chưa ai trả lời |
| 2 | Đã liên hệ | Đã nhắn/gọi ít nhất 1 lần, chờ phản hồi |
| 3 | Đã đặt lịch | Đã book buổi trải nghiệm/soi da tại spa |
| 4 | Đã tư vấn | Đã đến spa, đã được tư vấn liệu trình |
| 5 | Đã gửi báo giá | Đã nhận bảng giá liệu trình 8-12 buổi |
| 6 | Đang cân nhắc | Nói "để suy nghĩ/hỏi chồng" — cần follow-up |
| 7 | Đã chốt | Đã thanh toán/đặt cọc liệu trình |
| 8 | Không phù hợp | Sai tệp (ví dụ hỏi dịch vụ spa không có) |
| 9 | Chăm sóc lại | Từ chối tạm thời — nuôi dưỡng, mời lại sau 30-90 ngày |

- **Quy tắc vàng**: mỗi lead LUÔN ở đúng 1 trạng thái. Trạng thái chỉ đi tiến hoặc rẽ sang 8/9 — không "quên" ở giữa.
- **Điểm giảng quan trọng**: trạng thái 3 (Đã đặt lịch) là trạm riêng của ngành dịch vụ tư vấn — với spa/nha khoa/gym, "kéo được khách đến cơ sở" là 50% trận đánh. Không gộp nó vào "Đã liên hệ".

### Khối 3 — 12 trường dữ liệu khách hàng chuẩn (5 phút)

Họ tên · SĐT · Kênh liên hệ (link Facebook/Zalo) · Nguồn lead · Nhu cầu · Ngân sách dự kiến · Mức độ quan tâm (Nóng/Ấm/Lạnh — mai học chấm điểm chi tiết ở Ngày 17) · Người phụ trách · Trạng thái pipeline · Lần liên hệ gần nhất · **Ngày follow-up tiếp theo** · Ghi chú.

- Nhấn mạnh: cột **"Ngày follow-up tiếp theo"** là cột ăn tiền nhất cả bảng. Mỗi sáng mở CRM, lọc cột này = biết hôm nay phải nhắn ai. Không có cột này, CRM chỉ là danh bạ.

### Khối 4 — Nguồn lead và cách "đổ" lead vào CRM (5 phút)

- Liệt kê nguồn lead của SME Việt: Facebook (inbox + comment), Zalo OA/cá nhân, TikTok, Website/Landing page (đã xây Tuần 2), Giới thiệu (referral), Sự kiện/workshop, Data cũ (sổ tay, file excel rời, danh bạ điện thoại).
- Cách đổ lead giai đoạn đầu: **nhập tay có kỷ luật** (cuối mỗi ca, 10 phút). Đừng vội automation — Ngày 22 (Tuần 4) sẽ nối form/chatbot tự đổ vào CRM. Hôm nay cần thói quen + cấu trúc đúng trước.
- Nếu dùng CRM trong RocketAgent: tạo pipeline và trường tương ứng trong module CRM; nếu RocketAgent chưa bật module này cho tài khoản học viên → Google Sheets là phương án chuẩn, chuyển vào sau không mất gì.

> **Thích ứng ngành khác**: Nha khoa — trạng thái 3 là "Đã đặt lịch khám/chụp phim"; Giáo dục — "Đã đặt lịch học thử"; Gym — "Đã đặt buổi tập trải nghiệm"; Coaching — "Đã đặt discovery call (cuộc gọi khám phá)". Trường "Nhu cầu" đổi theo ngành: nha khoa = tình trạng răng, giáo dục = trình độ con + mục tiêu, gym = mục tiêu hình thể.

---

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Demo Day 2 | Chiếu 2-3 Marketing Engine tiêu biểu hôm qua; nhắc: "Tuần 2 tạo lead — tuần này biến lead thành tiền. Hỏi cả lớp: ai đang trả lời khách bằng trí nhớ?" |
| 25' | Giảng 4 khối kiến thức | Theo mục 2. Chốt bằng con số 54tr/tháng rơi vãi của Sen Spa |
| 30' | Demo live: dựng CRM Sen Spa từ template | Theo kịch bản mục 4 — mở template, đổi pipeline, nhập 5 lead thật, chạy bộ lọc "hôm nay nhắn ai" |
| 15' | Học viên làm tại chỗ + Q&A | Học viên copy template, sửa 9 trạng thái theo phễu của mình, nhập 3 lead đầu tiên ngay tại lớp. Trainer đảo phòng hỗ trợ |
| 10' | Giao bài tập + tiêu chí nghiệm thu | Chiếu rubric mục 10, nhấn deadline 23h59, deliverable đặt tên đúng chuẩn |

---

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

Trainer làm live, chia sẻ màn hình, dữ liệu Sen Spa mẫu. Mục tiêu demo: học viên thấy "từ số 0 đến CRM chạy được" mất đúng 30 phút.

**Bước 1 (3') — Mở "hiện trường vụ án".** Mở ảnh chụp inbox Facebook giả lập của Sen Spa: 8 hội thoại, 3 cái khách hỏi giá xong không ai trả lời tiếp. Nói: "Đây là 3 khách × 12tr liệu trình = 36tr đang nằm chết. Giờ mình nhặt lại."

**Bước 2 (5') — Copy template CRM.** Mở `Template CRM — Sen Spa (mẫu)` → File → Make a copy. Chỉ rõ 3 sheet: `CRM` (bảng chính), `Pipeline & Quy ước` (định nghĩa 9 trạng thái), `Dashboard mini`. Công cụ: Google Sheets. Kết quả: học viên thấy bảng có sẵn 12 cột, dropdown trạng thái đã cài.

**Bước 3 (5') — Việt hoá pipeline theo phễu Sen Spa.** Vào sheet `Pipeline & Quy ước`, đọc to 9 trạng thái, sửa trạng thái 3 thành "Đã đặt lịch soi da" và trạng thái 7 thành "Đã cọc/thanh toán liệu trình". Giải thích: pipeline phải nói ngôn ngữ của doanh nghiệp bạn, không nói ngôn ngữ sách giáo khoa.

**Bước 4 (10') — Nhập 5 lead thật từ inbox.** Nhập live 5 lead mẫu, vừa nhập vừa nói tiêu chí điền từng cột:

| Họ tên | Nguồn | Nhu cầu | Trạng thái | Follow-up tiếp theo | Ghi chú |
|---|---|---|---|---|---|
| Chị Hương | FB inbox | Nám lâu năm, hỏi giá | Đã liên hệ | 09/07 | Hỏi giá xong im — gửi ảnh kết quả khách nám |
| Chị Mai | Giới thiệu (KH Thu) | Mụn ẩn, muốn đến xem | Đã đặt lịch soi da | 10/07 (nhắc lịch) | Hẹn 10/07 15h, bạn của khách VIP |
| Chị Trang | FB comment | Hỏi trẻ hoá da | Lead mới | 08/07 (hôm nay) | Mới comment tối qua, chưa ai rep |
| Cô Lan Anh | Data cũ | Làm 1 buổi lẻ 3 tháng trước | Chăm sóc lại | 15/07 | Mời gói trải nghiệm mới |
| Chị Quỳnh | Zalo | Đã tư vấn, chê giá | Đang cân nhắc | 11/07 | Phản đối giá — gửi phương án trả 2 đợt |

**Bước 5 (4') — Chạy "nghi thức buổi sáng".** Dùng bộ lọc (Data → Create a filter) trên cột "Follow-up tiếp theo" = hôm nay → còn lại 1 dòng (chị Trang). Nói: "Sáng nào Ngọc cũng mở bảng, lọc 1 phát, biết ngay hôm nay nhắn ai. Hết cảnh 'em quên chị ơi'."

**Bước 6 (3') — Xem Dashboard mini.** Mở sheet `Dashboard mini`: bảng COUNTIF đếm lead theo trạng thái + theo nguồn. Chỉ vào: "FB inbox 12 lead, giới thiệu 5 lead nhưng giới thiệu chốt 3/5 — biết ngay nên xin referral nhiều hơn."

**Kết quả cuối demo**: 1 CRM sống, 5 lead thật, 1 thao tác lọc buổi sáng, 1 dashboard đếm tự động. Chốt câu: "Bài tập tối nay của các anh chị y hệt 30 phút vừa rồi — chỉ khác là bằng khách của chính mình."

---

## 5. ✅ Checklist Thực Thi (Học viên tự làm — tổng ≤ 2h phần Core)

**Cụm A — Dựng khung CRM (25')**
- [ ] Copy `Template CRM` về Drive của mình, đổi tên `[Tên DN] — CRM`.
- [ ] Liệt kê nguồn lead thực tế của DN mình (ít nhất 3, tối đa 7) vào sheet `Pipeline & Quy ước`.
- [ ] Sửa 9 trạng thái pipeline theo ngôn ngữ phễu của mình (đặc biệt trạng thái 3 và 7).
- [ ] Kiểm tra dropdown trạng thái hoạt động trên sheet `CRM`.

**Cụm B — Đổ dữ liệu thật (45')**
- [ ] Mở inbox Facebook/Zalo, lướt 30 ngày gần nhất, nhập **10 lead cũ** (khách từng hỏi mà chưa chốt).
- [ ] Nhập **5 khách hàng cũ** (đã từng mua) — trạng thái "Chăm sóc lại".
- [ ] Nhập **5 lead đang nói chuyện dở** — điền đúng trạng thái hiện tại.
- [ ] Với TỪNG lead: điền cột "Ngày follow-up tiếp theo" (không được để trống).

**Cụm C — Viết SOP sử dụng (30')**
- [ ] Mở `Template CRM Usage SOP`, trả lời 5 câu: khi nào tạo lead mới / khi nào đổi trạng thái / ai chịu trách nhiệm nhập / ghi chú gì sau mỗi lần tư vấn / quá bao lâu không phản hồi thì phải follow-up.
- [ ] Điền tên người phụ trách CRM cụ thể (tên thật, không ghi "nhân viên").

**Cụm D — Tự nghiệm thu (15')**
- [ ] Lọc thử theo trạng thái: ra đúng danh sách không?
- [ ] Lọc "Follow-up tiếp theo ≤ hôm nay": có biết mai phải nhắn ai không?
- [ ] Dashboard mini: có đếm đúng lead theo nguồn không?
- [ ] Chụp 2 ảnh màn hình (bảng CRM + dashboard) để nộp.

**Cụm Bonus (ngoài 2h)**
- [ ] Nhập đủ 40 lead (thêm 10 lead cũ + 10 khách tiềm năng mới từ comment/số điện thoại rời).

---

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Dựng CRM cho doanh nghiệp CỦA BẠN theo checklist mục 5: khung CRM 12 cột + pipeline 9 trạng thái đã việt hoá + tối thiểu 20 lead thật + SOP sử dụng 1 trang.

**Deliverable nộp (vào thread cohort, deadline 23h59 hôm nay):**
1. Link Google Sheets (mở quyền view cho mentor) — đặt tên file: `[Tên DN] — Ngày 15 — CRM Base`.
2. File/ảnh SOP: `[Tên DN] — Ngày 15 — CRM Usage SOP`.
3. 2 ảnh màn hình: (a) bảng CRM có ≥20 dòng lead, (b) kết quả lọc "follow-up hôm nay/ngày mai".
4. 1 dòng chia sẻ trong thread: "Số lead tôi nhặt lại được từ inbox cũ: ___ lead, ước tính giá trị: ___ đ."

**Lưu ý:** lead phải là NGƯỜI THẬT của DN bạn. Mentor sẽ kiểm tra xác suất 2-3 dòng (tên + ghi chú có logic không). Nhập lead giả = làm lại 🔴.

---

## 7. 📄 Template Đi Kèm

### Template 1 — `CRM Base (Google Sheets)` 
3 sheet, dựng sẵn 80%:
- **Sheet `CRM`**: 12 cột — Họ tên | SĐT | Link FB/Zalo | Nguồn lead (dropdown) | Nhu cầu | Ngân sách dự kiến | Mức quan tâm (Nóng/Ấm/Lạnh) | Người phụ trách | Trạng thái (dropdown 9 mục) | Lần liên hệ gần nhất | **Ngày follow-up tiếp theo** | Ghi chú. Có sẵn 5 dòng Sen Spa điền mẫu (đúng bảng ở mục 4 Bước 4) + định dạng có điều kiện: trạng thái "Lead mới" tô đỏ nhạt, follow-up quá hạn tô vàng.
- **Sheet `Pipeline & Quy ước`**: bảng 9 trạng thái + cột "Nghĩa là gì với DN tôi" (đã điền mẫu Sen Spa) + danh sách nguồn lead.
- **Sheet `Dashboard mini`**: COUNTIF theo trạng thái + theo nguồn, cài sẵn công thức — học viên không phải gõ hàm.

### Template 2 — `CRM Usage SOP (1 trang)`
Các trường: Người chịu trách nhiệm chính | Khi nào TẠO lead mới (mặc định: trong vòng 15' sau khi khách inbox lần đầu) | Khi nào ĐỔI trạng thái (ngay sau sự kiện, không dồn cuối tuần) | Sau mỗi lần tư vấn ghi chú gì (nhu cầu, phản đối, bước tiếp theo, ngày follow-up) | Quy tắc follow-up (không ai được "im" quá 3 ngày với lead Nóng/Ấm) | Lịch kiểm CRM hàng tuần (chủ DN duyệt sáng thứ 2, 15'). Có bản Sen Spa điền mẫu: "Ngọc nhập lead trong ca; Lan duyệt CRM 8h30 sáng thứ 2."

### Template 3 — `Phiếu Khai Quật Inbox` (checklist phụ)
Hướng dẫn 6 bước lướt inbox Facebook/Zalo 30 ngày để "khai quật" lead cũ: mở tab tin nhắn chưa trả lời → tìm từ khoá "giá", "bao nhiêu", "địa chỉ" → mỗi hội thoại khớp = 1 dòng CRM.

---

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Thiết kế pipeline theo phễu doanh nghiệp

```
Bạn là chuyên gia tư vấn vận hành bán hàng cho SME Việt Nam ngành dịch vụ bán qua tư vấn.

BỐI CẢNH: Doanh nghiệp của tôi: {{mô tả DN: ngành, sản phẩm chính, giá trung bình}}. 
Hành trình khách hàng hiện tại của tôi: {{mô tả từ lúc khách biết đến lúc mua, và sau khi mua}}.
Kênh khách liên hệ chính: {{Facebook/Zalo/website...}}.

NHIỆM VỤ: Thiết kế Lead Pipeline (đường ống khách hàng) cho CRM của tôi, dựa trên khung 9 trạng thái chuẩn: Lead mới / Đã liên hệ / Đã đặt lịch / Đã tư vấn / Đã gửi báo giá / Đang cân nhắc / Đã chốt / Không phù hợp / Chăm sóc lại.

ĐẦU VÀO: thông tin bối cảnh ở trên.

ĐẦU RA: Bảng markdown 4 cột: (1) Tên trạng thái đã việt hoá theo ngôn ngữ ngành tôi, (2) Định nghĩa — khi nào lead vào trạng thái này, (3) Hành động tiếp theo bắt buộc của sale, (4) Thời hạn tối đa được nằm ở trạng thái này trước khi phải follow-up.

RÀNG BUỘC: Giữ đúng 9 trạng thái, không thêm bớt. Tên trạng thái ≤ 5 từ. Hành động phải cụ thể (nhắn gì, gọi khi nào), không chung chung kiểu "chăm sóc khách". Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{mô tả DN}}` = "Sen Spa — spa chăm sóc da tại Hà Nội, 6 nhân viên, dịch vụ chính là liệu trình trị nám/mụn/trẻ hoá 8-12 buổi giá 12-15tr, buổi lẻ 1.5tr." · `{{hành trình}}` = "Khách thấy bài Facebook hoặc được bạn bè giới thiệu → inbox hỏi → được mời đến soi da miễn phí → tư vấn liệu trình tại spa → cân nhắc → chốt → làm 8-12 buổi → được mời gói duy trì." · `{{kênh}}` = "90% inbox Facebook, 10% Zalo."

### Prompt 2 — Khai quật và cấu trúc lead từ inbox cũ

```
Bạn là trợ lý sales operations (vận hành bán hàng) tỉ mỉ.

BỐI CẢNH: Tôi là chủ {{loại hình DN}}, đang chuyển các hội thoại cũ trong inbox {{Facebook/Zalo}} vào CRM. CRM của tôi có các cột: Họ tên, Nguồn, Nhu cầu, Ngân sách dự kiến, Mức quan tâm (Nóng/Ấm/Lạnh), Trạng thái (Lead mới/Đã liên hệ/Đã đặt lịch/Đã tư vấn/Đã gửi báo giá/Đang cân nhắc/Đã chốt/Không phù hợp/Chăm sóc lại), Ngày follow-up tiếp theo, Ghi chú.

NHIỆM VỤ: Đọc các đoạn hội thoại tôi dán dưới đây, trích xuất thành dòng dữ liệu CRM.

ĐẦU VÀO:
{{dán 1-10 đoạn hội thoại, mỗi đoạn ghi rõ tên khách và ngày nhắn gần nhất}}

ĐẦU RA: Bảng markdown đúng các cột CRM ở trên, mỗi hội thoại 1 dòng. Cột "Ghi chú" tóm tắt ≤ 20 từ: khách cần gì, vướng gì, lần cuối nói gì. Cột "Ngày follow-up tiếp theo" đề xuất ngày cụ thể tính từ hôm nay {{ngày hôm nay}}, kèm lý do trong ngoặc.

RÀNG BUỘC: Không bịa thông tin không có trong hội thoại — trường nào thiếu ghi "?". Mức quan tâm suy luận từ hành vi (hỏi giá + hỏi địa chỉ = Ấm trở lên; hẹn lịch = Nóng). Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** dán hội thoại — "Khách: Chị Hương, nhắn 02/07: 'Bên em trị nám bao nhiêu 1 liệu trình?' → Spa: 'Dạ liệu trình 10 buổi 12tr ạ' → khách seen, không trả lời." AI trả về: Hương | FB inbox | Trị nám | ? | Ấm | Đã liên hệ | 09/07 (đã im 7 ngày — gửi ảnh kết quả khách nám kèm ưu đãi soi da) | Hỏi giá liệu trình nám rồi im sau khi nghe 12tr.

### Prompt 3 — Viết CRM Usage SOP cho đội ngũ

```
Bạn là chuyên gia xây SOP (Standard Operating Procedure — quy trình vận hành chuẩn) cho doanh nghiệp nhỏ, viết ngắn gọn để nhân viên bận rộn đọc 2 phút là làm được.

BỐI CẢNH: {{tên DN}}, {{số nhân viên}} nhân viên, người trực page/tư vấn là {{tên + vai trò}}. Chúng tôi vừa dựng CRM trên Google Sheets với pipeline: {{dán 9 trạng thái của bạn}}.

NHIỆM VỤ: Viết CRM Usage SOP 1 trang cho đội ngũ.

ĐẦU VÀO: bối cảnh trên + quy tắc khung: lead mới phải vào CRM trong 15 phút; đổi trạng thái ngay sau sự kiện; lead Nóng không được im quá 24h, lead Ấm không quá 3 ngày; chủ DN duyệt CRM sáng thứ 2.

ĐẦU RA: SOP gồm 5 mục: (1) Ai làm gì — bảng phân vai theo tên thật, (2) Khi nào tạo lead mới, (3) Khi nào đổi trạng thái — liệt kê theo từng trạng thái, (4) Ghi chú bắt buộc sau mỗi lần tư vấn — 4 ý phải có, (5) Nhịp kiểm tra hàng tuần. Mỗi mục ≤ 5 gạch đầu dòng.

RÀNG BUỘC: Dùng tên thật đã cho, không dùng "nhân viên A". Mọi quy tắc phải có con số (thời hạn, tần suất). Không quá 350 từ. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{tên DN}}` = "Sen Spa" · `{{số nhân viên}}` = 6 · `{{tên + vai trò}}` = "Ngọc — tư vấn chính kiêm trực page; Lan — chủ spa". Kết quả mẫu: "Ngọc: nhập lead trong 15' sau inbox đầu tiên, cập nhật trạng thái ngay sau mỗi buổi soi da... Lan: 8h30 thứ 2 lọc cột follow-up quá hạn, hỏi Ngọc từng dòng vàng."

### Prompt 4 — Kiểm tra sức khoẻ CRM sau khi nhập

```
Bạn là auditor (kiểm toán viên) dữ liệu CRM khó tính.

BỐI CẢNH: Tôi vừa nhập {{số lượng}} lead vào CRM cho {{tên DN, ngành}}. 

NHIỆM VỤ: Rà soát dữ liệu tôi dán dưới đây và chỉ ra lỗi.

ĐẦU VÀO: {{dán 10-20 dòng CRM, có thể copy thẳng từ Google Sheets}}

ĐẦU RA: (1) Bảng lỗi: dòng nào | lỗi gì | sửa thế nào. (2) Đếm: bao nhiêu dòng thiếu "Ngày follow-up tiếp theo", bao nhiêu dòng ghi chú vô nghĩa (< 5 từ hoặc không nói khách cần gì), bao nhiêu dòng trạng thái mâu thuẫn với ghi chú (ví dụ ghi chú nói "đã gửi giá" mà trạng thái là "Đã liên hệ"). (3) 3 việc cần làm ngay xếp theo ưu tiên.

RÀNG BUỘC: Chỉ soi 3 loại lỗi trên + trùng lặp SĐT. Không khen xã giao. Viết tiếng Việt.
```

---

## 9. 📋 SOP Thao Tác (vận hành lặp lại sau khoá học)

**SOP-15A: Nhập lead mới** — Ai: người trực page/tư vấn (Sen Spa: Ngọc). Khi nào: trong 15 phút sau tin nhắn đầu tiên của khách. Input: hội thoại inbox → Các bước: (1) mở CRM, (2) kiểm tra trùng SĐT/tên, (3) thêm dòng, điền tối thiểu 7 cột (tên, kênh, nguồn, nhu cầu, mức quan tâm, trạng thái, follow-up tiếp theo), (4) trả lời khách → Output: 1 dòng CRM đủ chuẩn. Tần suất: mỗi lead, hàng ngày.

**SOP-15B: Nghi thức buổi sáng 10 phút** — Ai: người tư vấn. Khi nào: đầu ca sáng. Input: CRM → Các bước: (1) lọc "Ngày follow-up ≤ hôm nay", (2) xử lý từng dòng theo thứ tự Nóng → Ấm → Lạnh, (3) sau mỗi lần nhắn/gọi: cập nhật "Lần liên hệ gần nhất" + đặt ngày follow-up mới + ghi chú 1 dòng → Output: 0 lead quá hạn cuối ngày. Tần suất: hàng ngày.

**SOP-15C: Duyệt CRM đầu tuần** — Ai: chủ DN (Lan). Khi nào: 8h30 sáng thứ 2, 15 phút. Input: CRM + Dashboard mini → Các bước: (1) đếm lead mới tuần trước theo nguồn, (2) soi các dòng follow-up quá hạn (tô vàng) và hỏi người phụ trách, (3) soi trạng thái "Đang cân nhắc" > 7 ngày, (4) ghi 1 quyết định tuần này (ví dụ: đẩy thêm bài về nguồn đang chốt tốt) → Output: CRM sạch + 1 quyết định. Tần suất: hàng tuần.

---

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của Ngày 15 |
|---|---|---|
| Đủ tài sản Core | 30 | CRM có đủ 12 cột chuẩn (10đ); pipeline đủ 9 trạng thái + dropdown chạy được (10đ); SOP nộp đủ trả lời 5 câu hỏi (10đ) |
| Chất lượng & độ sâu | 30 | ≥20 lead thật đã nhập (10đ — dưới 20: trừ 1đ/lead thiếu); 100% dòng có "Ngày follow-up tiếp theo" (10đ — mỗi ô trống trừ 2đ); ghi chú mỗi lead ≥ 5 từ và nói rõ khách cần gì/vướng gì (10đ — chấm mẫu 5 dòng ngẫu nhiên, mỗi dòng hỏng trừ 2đ) |
| Cá nhân hoá vào DN thật | 25 | Tên trạng thái 3 & 7 đã việt hoá theo phễu ngành mình, không giữ nguyên chữ mẫu Sen Spa (10đ); nguồn lead liệt kê đúng kênh DN đang có, ≥3 nguồn (5đ); SOP có tên người thật + con số thời hạn cụ thể (10đ) |
| Dùng được ngay | 15 | Lọc "follow-up hôm nay" ra kết quả đúng — có ảnh chứng minh (5đ); dashboard đếm đúng theo nguồn (5đ); link mở được quyền view (5đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Lead giả/copy nguyên mẫu Sen Spa vào bài nộp: −20đ và yêu cầu làm lại phần dữ liệu.
2. Cột "Ngày follow-up tiếp theo" bỏ trống hàng loạt: −2đ/ô (tối đa −10đ).
3. Ghi chú vô nghĩa kiểu "khách hỏi", "đang chờ": −2đ/dòng chấm mẫu.
4. Pipeline chế thêm 12-15 trạng thái cho "hoành tráng": −5đ (phức tạp = không ai dùng).
5. Không mở quyền view link: −5đ và không được chấm phần trong file cho đến khi mở.

---

## 11. ❓ FAQ & Lỗi Thường Gặp

**Hỏi 1: "Tôi có nên mua phần mềm CRM xịn luôn không, làm Sheets chi cho cực?"**
Đáp: Chưa. Vấn đề của bạn hôm nay là THÓI QUEN và CẤU TRÚC, không phải công cụ. Sheets kỷ luật 4 tuần rồi hãy nâng cấp — lúc đó chuyển dữ liệu sang CRM RocketAgent hoặc tool khác mất 1 buổi vì cấu trúc đã đúng.

**Hỏi 2: "Khách inbox Facebook không cho số điện thoại thì nhập kiểu gì?"**
Đáp: Vẫn nhập — dán link hội thoại vào cột "Link FB/Zalo", SĐT ghi "?". Cột SĐT có sau khi bạn hỏi ở bước tư vấn (Ngày 16 chatbot sẽ tự hỏi giúp bạn).

**Hỏi 3: "Nhân viên tôi lười nhập thì sao?"**
Đáp: 3 lớp: (1) SOP quy định nhập trong 15' + có tên người chịu trách nhiệm; (2) nghi thức thứ 2 của chủ DN — nhân viên biết bảng ĐƯỢC XEM thì sẽ nhập; (3) quy tắc "không có trong CRM = không tính là lead của em" khi tính thưởng.

**Hỏi 4: "Lead từ 2-3 năm trước có nên nhập không?"**
Đáp: Chỉ nhập khách CŨ ĐÃ MUA (vào "Chăm sóc lại" — mỏ vàng tái mua/upsell) và lead ≤ 6 tháng. Lead hỏi 1 câu từ 2 năm trước: bỏ, nhập vào chỉ làm bẩn dữ liệu.

**Hỏi 5: "Một khách hỏi cho cả mẹ và con thì nhập 1 hay 2 dòng?"**
Đáp: 2 dòng — mỗi NGƯỜI SẼ TRẢ TIỀN/SỬ DỤNG là 1 dòng, ghi chú liên kết "mẹ chị X". Đơn vị của CRM là con người, không phải cuộc hội thoại.

**Hỏi 6: "Trạng thái 'Không phù hợp' với 'Chăm sóc lại' khác gì nhau?"**
Đáp: "Không phù hợp" = vĩnh viễn sai tệp (hỏi dịch vụ không có, ngoài khu vực phục vụ) — không bao giờ đụng lại. "Chăm sóc lại" = đúng tệp nhưng chưa đúng lúc (hết ngân sách quý này, mới sinh em bé) — có ngày follow-up cụ thể, thường 30-90 ngày.

**Lỗi thường gặp:**
1. **Dồn nhập CRM vào cuối tuần** → Phát hiện: cột "Lần liên hệ gần nhất" toàn cùng 1 ngày → Sửa: quay lại quy tắc 15 phút, đặt CRM làm tab ghim trên trình duyệt điện thoại.
2. **Nhầm pipeline với mức quan tâm** (điền "Nóng" vào cột trạng thái) → Phát hiện: dropdown báo lỗi hoặc giá trị ngoài danh sách → Sửa: giảng lại — trạng thái = khách Ở ĐÂU trong phễu; mức quan tâm = khách NÓNG cỡ nào. Hai trục khác nhau, Ngày 17 sẽ chấm điểm trục thứ hai.
3. **Ghi chú viết cho mình đọc, người khác không hiểu** ("ok r", "mai ck") → Phát hiện: đưa dòng ghi chú cho người khác trong team đọc, không hiểu = hỏng → Sửa: khuôn ghi chú 4 ý của SOP: cần gì / vướng gì / đã hứa gì / bước tiếp theo.

---

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 14 — Marketing Engine Review & Demo Day 2]] — lead từ Marketing Engine tuần 2 (landing page, lead magnet, content) chính là dữ liệu đầu vào đổ về CRM hôm nay.
- Ngày sau: [[Ngày 16 — AI Chatbot & Tư Vấn 24-7]] — chatbot sẽ là "người nhập liệu tự động" đầu tiên: thông tin chatbot thu được điền thẳng vào các cột CRM vừa dựng.
- Tài sản hôm nay được dùng lại: **Ngày 17** (cột Mức quan tâm nâng cấp thành Lead Scoring, CRM thêm cột Điểm), **Ngày 20** (cột "Ngày follow-up tiếp theo" thành xương sống của Follow-up Automation), **Ngày 21** (demo luồng lead chạy xuyên CRM), **Ngày 22** (nối form/chatbot tự đổ vào CRM) và **Ngày 25-26** (dashboard đo lường lấy số từ CRM).
- Tư duy xuyên suốt: CRM là "bộ nhớ" của toàn bộ Sales Engine — mọi thứ xây trong tuần này (chatbot, scoring, script, proposal, follow-up) đều đọc và ghi vào bảng này.
