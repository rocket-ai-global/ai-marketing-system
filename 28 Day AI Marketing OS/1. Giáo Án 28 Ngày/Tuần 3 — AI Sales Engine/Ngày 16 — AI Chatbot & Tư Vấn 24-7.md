---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 3
day: 16
core-output: "Chatbot Flow 7 bước + Chatbot Script + FAQ Response Pack ≥10 câu + Lead Capture Script + Test Report 5 vai"
---

# Ngày 16 — AI Chatbot & Tư Vấn 24-7

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Chatbot dựng trên lớp động cơ Hermes/RocketAgent, đọc Knowledge từ `00. Business Context/` (offer, giá, FAQ) — không nạp tài liệu riêng; kịch bản + FAQ Response Pack lưu `04. Resources/Playbooks/`.

> Hôm nay bạn dựng "nhân viên tư vấn không ngủ" trên RocketAgent: chatbot trả lời inbox trong 5 giây, tư vấn đúng như bạn tư vấn giỏi nhất, xin đủ thông tin và mời khách đặt lịch — kể cả lúc 11h đêm.

---

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày 16, học viên CÓ TRONG TAY:

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Chatbot Flow (sơ đồ luồng hội thoại)**: sơ đồ 7 bước từ lời chào → phân nhánh nhu cầu → thu thông tin → mời đặt lịch → chuyển sale.
- ✅ **Chatbot Script (kịch bản chatbot)**: chatbot dựng chạy được trên RocketAgent (Agent + Knowledge Base tuần 1), trả lời đúng bằng dữ liệu DN mình.
- ✅ **FAQ Response Pack**: ≥10 câu trả lời mẫu cho câu hỏi thường gặp + 6 tình huống khó (hỏi giá, so sánh, "để suy nghĩ"...).
- ✅ **Lead Capture Script (kịch bản thu thông tin khách)**: chuỗi câu hỏi xin tên → SĐT → nhu cầu → thời gian muốn tư vấn, khớp đúng cột CRM Ngày 15.
- ✅ **Chatbot Test Report**: biên bản test 5 vai khách (nóng/lạnh/hỏi khó/chê giá/muốn đặt lịch) — ghi rõ đạt/hỏng từng vai.

**Bonus Output (nâng cao):**
- ⭐ Gắn chatbot vào kênh thật (Fanpage/Zalo OA/widget web) chạy thử với 1 khách thật hoặc 1 người quen đóng vai.
- ⭐ Thêm nhánh "khách cũ hỏi lịch/đổi lịch" vào flow.

---

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Chatbot trong sales: làm gì và KHÔNG làm gì (7 phút)

- **Chatbot** ở đây = AI Agent tư vấn dựng trên RocketAgent, đọc Knowledge Base (kho tri thức — đã xây Tuần 1) để trả lời — không phải bot bấm nút kiểu cũ.
- **Analogy giảng**: chatbot là LỄ TÂN GIỎI, không phải bác sĩ. Lễ tân Sen Spa: chào niềm nở, hỏi khách cần gì, trả lời giá và địa chỉ, xin số, xếp lịch soi da. Lễ tân KHÔNG chẩn đoán da thay chuyên viên, KHÔNG tự giảm giá, KHÔNG cam kết kết quả điều trị.
- Bảng NÊN/KHÔNG dán lên slide:

| Chatbot NÊN | Chatbot KHÔNG ĐƯỢC |
|---|---|
| Chào trong 5 giây, 24/7 | Chẩn đoán/tư vấn chuyên môn sâu (tình trạng da, bệnh lý) |
| Trả lời FAQ: giá, địa chỉ, quy trình, giờ mở cửa | Tự ý giảm giá, hứa kết quả "hết nám 100%" |
| Hỏi nhu cầu, phân nhánh đúng dịch vụ | Cãi nhau/đôi co với khách khó |
| Thu tên + SĐT + nhu cầu + khung giờ | Nói dối "em là người thật" khi bị hỏi thẳng |
| Mời đặt lịch trải nghiệm, chuyển sale khi có tín hiệu mua | Bịa thông tin không có trong Knowledge Base |

- **Vì sao quan trọng với SME dịch vụ**: khách inbox spa lúc 21h-23h nhiều nhất (sau khi con ngủ) — đúng lúc không ai trực. Trả lời sau 5 phút vs sau 12 tiếng: tỷ lệ chuyển thành lịch hẹn khác nhau nhiều lần. Chatbot mua lại khung giờ vàng đó.

### Khối 2 — Thiết kế luồng hội thoại 7 bước (10 phút)

Khung chuẩn cho DN bán qua tư vấn (mỗi bước 1 nhiệm vụ):

1. **Chào + định vị** — xưng danh spa, 1 câu thiện cảm, hỏi mở.
2. **Hỏi nhu cầu** — "Chị đang quan tâm về da vấn đề gì ạ?" — phân nhánh theo 3-4 nhóm dịch vụ chính.
3. **Tư vấn sơ bộ + gợi ý dịch vụ phù hợp** — 2-3 câu từ Knowledge Base, KÈM bằng chứng (số khách đã làm, kết quả).
4. **Trả lời FAQ/phản đối cơ bản** — giá, đau không, bao lâu thấy kết quả (vòng lặp: khách hỏi bao nhiêu, trả lời bấy nhiêu).
5. **Thu thông tin** — xin tên → SĐT → khung giờ rảnh (xin TỪNG thứ một, có lý do).
6. **Mời đặt lịch** — CTA duy nhất của bot: buổi soi da/trải nghiệm miễn phí. Không bán liệu trình 12tr qua chat.
7. **Chuyển giao sale (handoff)** — khi khách sẵn sàng đặt lịch, hỏi giá xong muốn tư vấn sâu, hoặc bot không trả lời được 2 lần liên tiếp → "Em xin phép kết nối chị với chị Ngọc — chuyên viên tư vấn của spa, trong giờ làm việc chị ấy sẽ gọi lại ngay ạ" + ghi thông tin vào CRM.

- **Nguyên tắc giảng kỹ**: mục tiêu của bot KHÔNG phải chốt đơn 12-15tr — mục tiêu là **đặt được lịch trải nghiệm**. Deal lớn ngành tư vấn chốt ở người, bot chốt CUỘC HẸN. Đây là điểm học viên hay tham, bắt bot bán cả liệu trình → hỏng.

### Khối 3 — Knowledge Base + Persona: cho bot "học việc" (5 phút)

- Bot trả lời đúng nhờ 2 thứ: **System Prompt (lệnh hệ thống — tính cách + luật)** và **Knowledge Base (dữ liệu: bảng giá, quy trình, FAQ, chính sách, case study)**.
- Checklist dữ liệu cần nạp: Product Knowledge (mô tả từng dịch vụ + giá), FAQ ≥10 câu, Objection (câu phản đối) thường gặp + cách trả lời, chính sách giá/hoàn huỷ/bảo hành liệu trình, 2-3 case study khách thật, CTA chuẩn (link/mẫu đặt lịch).
- Luật chống bịa: "Nếu không có trong tài liệu → trả lời: 'Câu này em xin phép để chuyên viên tư vấn trả lời chính xác cho chị ạ' + xin thông tin liên hệ." Bot thà chuyển người còn hơn bịa.

### Khối 4 — Bot phân loại lead và bàn giao cho người (3 phút)

- Bot gắn nhãn ngay trong hội thoại: hỏi giá + để lại SĐT = **Ấm**; chủ động xin đặt lịch = **Nóng**; hỏi vu vơ không để thông tin = **Lạnh**. (Ngày 17 sẽ nâng thành thang điểm chi tiết.)
- Mỗi hội thoại có thu thông tin → 1 dòng CRM (tuần này nhập tay từ báo cáo bot cuối ngày; Ngày 22 sẽ nối tự động).

> **Thích ứng ngành khác**: Nha khoa — CTA của bot là "đặt lịch khám + chụp phim miễn phí"; luật cứng: không chẩn đoán qua ảnh, không báo giá implant chính xác trước khi khám (chỉ báo khoảng giá). Giáo dục — CTA là "đặt lịch kiểm tra trình độ/học thử"; bot hỏi thêm tuổi con + mục tiêu. Gym — CTA "buổi tập thử với HLV"; hỏi mục tiêu hình thể + lịch rảnh. Coaching — CTA "discovery call 30 phút"; bot lọc trước bằng 2 câu về hiện trạng và mục tiêu.

---

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 15 | Chiếu 2-3 CRM tiêu biểu: khen bảng có follow-up đầy đủ; chữa 1 lỗi phổ biến (ghi chú vô nghĩa). Câu dẫn: "CRM đã có chỗ chứa lead — hôm nay dựng người rót lead vào lúc mình ngủ." |
| 25' | Giảng 4 khối kiến thức | Trọng tâm khối 2 (flow 7 bước) — vẽ sơ đồ trực tiếp trên bảng/Excalidraw |
| 30' | Demo live: dựng chatbot Sen Spa trên RocketAgent | Theo kịch bản mục 4 — viết System Prompt, nạp Knowledge Base, test hội thoại 2 vai ngay tại lớp |
| 15' | Học viên làm tại chỗ + Q&A | Học viên tạo Agent, dán System Prompt template, sửa 3 chỗ: tên DN, dịch vụ, CTA. Chạy câu chào đầu tiên |
| 10' | Giao bài tập + tiêu chí nghiệm thu | Nhấn mạnh Test Report 5 vai là phần bị bỏ qua nhiều nhất — không test = không nghiệm thu |

---

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (3') — Vẽ flow trước khi đụng tool.** Vẽ sơ đồ 7 bước lên Excalidraw/bảng, nhánh theo 3 nhu cầu chính của Sen Spa: Nám — Mụn — Trẻ hoá. Nói: "Không bao giờ dựng bot trước khi vẽ flow — bot không có flow là nhân viên mới không được đào tạo."

**Bước 2 (7') — Tạo Agent trên RocketAgent + dán System Prompt.** Vào RocketAgent → tạo Agent mới "Sen Spa — Tư vấn viên Sen". Dán System Prompt (Prompt 1 mục 8, bản đã điền). Đọc to 3 phần của prompt: nhân cách (Sen — lễ tân ấm áp, xưng "em"), nhiệm vụ 7 bước, luật cấm (không chẩn đoán, không giảm giá, không bịa).

**Bước 3 (5') — Nạp Knowledge Base.** Upload 3 file vào Knowledge Base của Agent: `Bảng giá & dịch vụ Sen Spa.md` (3 liệu trình chính, giá 12-15tr, buổi lẻ 1.5tr, soi da miễn phí), `FAQ Sen Spa.md` (10 câu), `Case study.md` (2 khách: chị H. hết nám sau 10 buổi, chị M. sạch mụn ẩn sau 8 buổi). Nói rõ: đây chính là tài liệu Knowledge Base đã làm Tuần 1, hôm nay tái sử dụng — ai thiếu thì template hôm nay có bản khung.

**Bước 4 (10') — Test live 2 vai.** Trainer mở cửa sổ chat của Agent, đóng 2 vai:
- *Vai khách Ấm*: "Bên em trị nám bao nhiêu?" → kỳ vọng bot: trả khoảng giá liệu trình + hỏi ngược tình trạng nám + dẫn về soi da miễn phí. Nếu bot trả giá xong im → chỉ cho lớp thấy lỗi "trả lời cụt", sửa System Prompt thêm luật "mỗi câu trả lời kết thúc bằng 1 câu hỏi dẫn tiếp".
- *Vai khách Nóng*: "Mai chiều mình qua soi da được không?" → kỳ vọng bot: xác nhận + xin tên, SĐT, chốt khung giờ + thông báo chuyển chị Ngọc xác nhận lịch.

**Bước 5 (3') — Cho lớp xem 1 ca hỏng cố ý.** Hỏi bot: "Da mình bị nám hỗn hợp chân sâu, làm laser toning có khỏi hẳn không?" → bot ĐÚNG khi trả lời "cần chuyên viên soi da mới tư vấn chính xác" thay vì phán bừa. Chốt: "Bot từ chối đúng chỗ là bot ngoan."

**Bước 6 (2') — Chốt vòng lặp dữ liệu.** Mở lại CRM Ngày 15, nhập tay dòng lead từ hội thoại vai Nóng vừa test (tên, SĐT, nhu cầu, trạng thái "Đã đặt lịch soi da"). Nói: "Bot thu — CRM chứa. Tuần 4 sẽ tự động nối, tuần này ta nối bằng tay 5 phút cuối ngày."

**Phương án thay thế** (nói rõ ở demo): học viên chưa có tài khoản RocketAgent đủ quyền → dựng bằng ChatGPT Projects/Claude Projects (dán System Prompt + upload cùng bộ file) để nộp bài; sang tuần 4 chuyển lên RocketAgent gắn kênh thật.

---

## 5. ✅ Checklist Thực Thi (Học viên tự làm — tổng ≤ 2h phần Core)

**Cụm A — Vẽ flow + soạn dữ liệu (35')**
- [ ] Vẽ Chatbot Flow 7 bước của DN mình (giấy chụp ảnh, Excalidraw hoặc điền template flow) — nhánh nhu cầu theo 3-4 nhóm dịch vụ chính.
- [ ] Điền `FAQ Response Pack`: 10 câu hỏi khách hay hỏi nhất + câu trả lời chuẩn (lấy từ inbox thật — mở 10 hội thoại gần nhất là đủ 10 câu).
- [ ] Viết câu trả lời cho 6 tình huống khó: hỏi giá / "có phù hợp với mình không" / "để suy nghĩ" / so sánh bên khác / chưa có ngân sách / muốn gặp người thật.
- [ ] Kiểm tra Knowledge Base tuần 1 đã có: bảng giá, mô tả dịch vụ, chính sách. Thiếu gì bổ sung bằng template.

**Cụm B — Dựng bot (30')**
- [ ] Tạo Agent trên RocketAgent (hoặc ChatGPT/Claude Projects), đặt tên bot có nhân cách (ví dụ "Sen").
- [ ] Dán System Prompt (Prompt 1), thay 5 chỗ `{{...}}` bằng dữ liệu DN mình.
- [ ] Nạp Knowledge Base: bảng giá + FAQ Pack + case study.
- [ ] Chạy thử câu chào: đúng tên DN, đúng giọng chưa?

**Cụm C — Test 5 vai + viết Test Report (40')**
- [ ] Vai 1 — Khách Nóng: chủ động xin đặt lịch → bot phải thu đủ tên/SĐT/khung giờ.
- [ ] Vai 2 — Khách Lạnh: hỏi vu vơ "spa ở đâu" → bot trả lời + mời nhẹ, không đeo bám.
- [ ] Vai 3 — Khách hỏi khó (chuyên môn sâu) → bot phải chuyển người, không bịa.
- [ ] Vai 4 — Khách chê giá → bot nói giá trị + phương án nhỏ hơn (buổi trải nghiệm), không tự giảm giá.
- [ ] Vai 5 — Khách muốn đặt lịch nhưng giờ oái oăm (23h đêm nay) → bot xử lý mềm: ghi nhận + hẹn xác nhận trong giờ làm việc.
- [ ] Điền `Chatbot Test Report`: mỗi vai — dán hội thoại, chấm Đạt/Hỏng theo tiêu chí, ghi 1 điều cần sửa.
- [ ] Sửa System Prompt/Knowledge Base theo lỗi tìm được, test lại vai bị hỏng.

**Cụm D — Nộp bài (15')**
- [ ] Chụp/xuất flow + link bot (hoặc ảnh hội thoại) + FAQ Pack + Test Report, đặt tên đúng chuẩn, đăng thread.

**Cụm Bonus (ngoài 2h)**
- [ ] Gắn bot vào Fanpage/Zalo OA/widget web, nhờ 1 người quen inbox thật và lưu hội thoại.

---

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Dựng chatbot tư vấn cho DN của bạn theo checklist mục 5: flow 7 bước → nạp dữ liệu → test 5 vai → sửa → nộp kèm bằng chứng.

**Deliverable nộp (thread cohort, deadline 23h59 hôm nay):**
1. Ảnh/sơ đồ Chatbot Flow: `[Tên DN] — Ngày 16 — Chatbot Flow`.
2. Link Agent RocketAgent (hoặc 5 ảnh hội thoại nếu dùng Projects): `[Tên DN] — Ngày 16 — Chatbot Script`.
3. File FAQ Response Pack (≥10 FAQ + 6 tình huống khó): `[Tên DN] — Ngày 16 — FAQ Response Pack`.
4. File Test Report 5 vai có chấm Đạt/Hỏng: `[Tên DN] — Ngày 16 — Chatbot Test Report`.
5. 1 dòng chia sẻ: "Câu trả lời của bot khiến tôi bất ngờ nhất: ___".

**Lưu ý:** Test Report phải có hội thoại THẬT dán vào (không mô tả chay "bot trả lời tốt"). Vai 3 (hỏi khó) mà bot bịa chuyên môn = tự động Cần sửa 🔧 dù các phần khác tốt — vì bot bịa là rủi ro thương hiệu thật.

---

## 7. 📄 Template Đi Kèm

### Template 1 — `Chatbot Flow 7 Bước (khung điền)`
Sơ đồ khung: 7 ô theo thứ tự + chỗ trống điền: (1) câu chào của DN bạn, (2) 3-4 nhánh nhu cầu, (3) câu tư vấn sơ bộ mỗi nhánh, (4) 3 FAQ hay gặp nhất mỗi nhánh, (5) chuỗi câu xin thông tin, (6) CTA đặt lịch, (7) điều kiện chuyển sale + câu chuyển. Kèm bản Sen Spa vẽ hoàn chỉnh (nhánh Nám/Mụn/Trẻ hoá) làm mẫu đối chiếu.

### Template 2 — `FAQ Response Pack`
Bảng 4 cột: Câu khách hỏi | Câu trả lời chuẩn | Câu hỏi dẫn tiếp | Ghi chú. Dựng sẵn 10 dòng FAQ phổ biến ngành dịch vụ (giá? địa chỉ/giờ mở? đau không? bao lâu có kết quả? có bảo hành/cam kết? đặt lịch thế nào? trả góp/trả đợt? ai thực hiện? máy móc/công nghệ gì? có ưu đãi không?) — mỗi dòng có bản Sen Spa điền mẫu, học viên thay nội dung. Cuối file: 6 tình huống khó với khung trả lời 3 nhịp "Đồng cảm → Thông tin/Bằng chứng → Câu hỏi dẫn tiếp".

### Template 3 — `Lead Capture Script`
Chuỗi 4 câu xin thông tin, mỗi câu kèm LÝ DO khiến khách thoải mái cung cấp (nguyên tắc: xin gì phải cho lý do): xin tên ("để em tiện xưng hô") → xin tình trạng/nhu cầu ("để chuyên viên chuẩn bị trước cho mình") → xin SĐT ("để bên em gửi xác nhận lịch, không spam") → xin khung giờ. Có bản Sen Spa điền mẫu + ghi chú map từng thông tin vào cột CRM Ngày 15.

### Template 4 — `Chatbot Test Report`
Bảng 5 dòng × 5 cột: Vai test | Kịch bản nhập vai (có sẵn gợi ý thoại) | Hội thoại thật (dán vào) | Đạt/Hỏng theo tiêu chí (liệt kê sẵn tiêu chí từng vai) | Điều cần sửa. Dòng mẫu Sen Spa đã điền vai "chê giá".

---

## 8. 🤖 Prompt Mẫu

### Prompt 1 — System Prompt cho chatbot tư vấn (dán vào Agent RocketAgent)

```
Bạn là {{tên bot}}, nhân viên tư vấn online của {{tên DN}} — {{mô tả 1 câu: ngành, địa điểm, điểm mạnh}}.

TÍNH CÁCH & GIỌNG ĐIỆU: Ấm áp, chuyên nghiệp, như một lễ tân giỏi. Xưng "em", gọi khách là "chị/anh". Câu ngắn, mỗi tin nhắn tối đa 3-4 câu, dùng tối đa 1 emoji. Không văn mẫu sáo rỗng.

NHIỆM VỤ THEO 7 BƯỚC:
1. Chào khách, xưng danh {{tên DN}}, hỏi khách đang quan tâm điều gì.
2. Xác định nhu cầu thuộc nhóm nào: {{liệt kê 3-4 nhóm dịch vụ chính}}. Hỏi thêm tối đa 2 câu để hiểu tình trạng.
3. Tư vấn sơ bộ dựa trên tài liệu được cung cấp, kèm 1 bằng chứng (số liệu, khách đã làm).
4. Trả lời câu hỏi về giá, quy trình, chính sách theo đúng tài liệu.
5. Xin thông tin theo thứ tự, MỖI LẦN MỘT THỨ và kèm lý do: tên → nhu cầu/tình trạng → số điện thoại → khung giờ rảnh.
6. Mục tiêu cuối của em là mời khách {{CTA duy nhất, ví dụ: đặt lịch soi da miễn phí 30 phút tại spa}}. Mọi cuộc hội thoại đều dẫn về đây.
7. Khi khách đồng ý đặt lịch, hỏi câu ngoài tài liệu, hoặc yêu cầu gặp người thật: nói "Em xin phép kết nối chị với {{tên nhân viên tư vấn}} — chuyên viên của {{tên DN}}, chị ấy sẽ liên hệ lại trong giờ làm việc ạ" và tóm tắt lại thông tin khách đã cung cấp.

LUẬT CẤM (tuyệt đối):
- KHÔNG chẩn đoán tình trạng chuyên môn hay cam kết kết quả điều trị ("khỏi hẳn", "100%", "vĩnh viễn").
- KHÔNG tự ý giảm giá hoặc tạo khuyến mãi không có trong tài liệu.
- KHÔNG bịa thông tin ngoài tài liệu. Không biết thì nói: "Câu này em xin phép để chuyên viên trả lời chính xác cho mình ạ" rồi xin thông tin liên hệ.
- KHÔNG nhận mình là người thật nếu khách hỏi thẳng — trả lời: "Em là trợ lý AI của {{tên DN}}, những gì cần chuyên viên thật em sẽ kết nối ngay ạ."
- Mỗi câu trả lời kết thúc bằng MỘT câu hỏi dẫn tiếp, trừ khi khách chào tạm biệt.

KHI KHÁCH PHẢN ĐỐI: dùng nhịp 3 bước — Đồng cảm ngắn → Đưa thông tin/bằng chứng từ tài liệu → Hỏi dẫn tiếp về {{CTA}}. Không đôi co.
```

**Ví dụ đã điền (Sen Spa):** `{{tên bot}}` = "Sen" · `{{tên DN}}` = "Sen Spa" · `{{mô tả}}` = "spa chăm sóc da chuyên trị nám, mụn, trẻ hoá tại Hà Nội, hơn 1.000 khách đã trải nghiệm" · `{{3-4 nhóm}}` = "Trị nám — Trị mụn — Trẻ hoá da — Chăm sóc da cơ bản" · `{{CTA}}` = "đặt lịch soi da miễn phí 30 phút tại spa (số 8 Trần Duy Hưng)" · `{{tên nhân viên tư vấn}}` = "chị Ngọc".

### Prompt 2 — Sinh FAQ Response Pack từ inbox thật

```
Bạn là chuyên gia trải nghiệm khách hàng ngành {{ngành}}, giỏi biến câu trả lời khô khan thành câu trả lời vừa đúng vừa dẫn khách đi tiếp.

BỐI CẢNH: {{tên DN, mô tả 1 câu}}. Giá dịch vụ chính: {{bảng giá tóm tắt}}. CTA chuẩn: {{CTA}}. Giọng thương hiệu: {{ấm áp/chuyên gia/trẻ trung...}}, xưng "em" gọi "chị/anh".

NHIỆM VỤ: Với mỗi câu hỏi khách hay hỏi dưới đây, viết câu trả lời chuẩn cho chatbot.

ĐẦU VÀO: {{dán 10-15 câu hỏi lấy từ inbox thật, giữ nguyên văn khách viết}}

ĐẦU RA: Bảng markdown 3 cột: Câu khách hỏi | Câu trả lời (2-4 câu, có số liệu/bằng chứng nếu phù hợp) | Câu hỏi dẫn tiếp (1 câu, hướng về CTA). 

RÀNG BUỘC: Không hứa kết quả tuyệt đối. Câu hỏi về giá: nêu khoảng giá thật + ngay sau đó nói giá trị nhận được, không né giá. Mỗi câu trả lời phải đọc lên nghe như người thật nhắn, không như thông cáo báo chí. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** đầu vào gồm các câu nguyên văn: "Trị nám bên em bn tiền?", "Có đau ko e?", "Bao lâu thì hết mụn?", "Bên e có bảo hành ko?", "Spa ở đâu, có gần Cầu Giấy ko?"... Đầu ra mẫu cho câu giá: "Dạ liệu trình trị nám bên em từ 12-15 triệu cho 10-12 buổi tuỳ tình trạng da chị ạ. Trước khi tư vấn gói cụ thể, bên em luôn soi da miễn phí để chị biết chính xác da mình cần gì — chứ không tư vấn chay ạ. | Chị tiện qua soi da vào cuối tuần này hay trong tuần ạ?"

### Prompt 3 — Sinh 25 kịch bản test cho chatbot

```
Bạn là tester (người kiểm thử) khó tính chuyên phá chatbot bán hàng.

BỐI CẢNH: Tôi vừa dựng chatbot tư vấn cho {{tên DN, ngành, dịch vụ chính, giá}}. CTA của bot là {{CTA}}.

NHIỆM VỤ: Tạo bộ kịch bản test đóng vai khách hàng để tôi kiểm tra bot.

ĐẦU VÀO: 5 nhóm vai bắt buộc: (1) khách nóng muốn đặt lịch, (2) khách lạnh hỏi vu vơ, (3) khách hỏi chuyên môn sâu/câu hỏi bẫy, (4) khách phản đối giá, (5) khách tình huống oái oăm (ngoài giờ, đòi giảm giá sâu, hỏi dịch vụ không có, gõ sai chính tả nhiều).

ĐẦU RA: 25 kịch bản (5 vai × 5 kịch bản), mỗi kịch bản gồm: câu mở đầu của khách (viết đúng kiểu khách Việt nhắn tin thật — viết tắt, không dấu, cộc lốc) + diễn biến 2-3 lượt tiếp theo + TIÊU CHÍ ĐẠT: bot phải làm được gì thì tính là qua.

RÀNG BUỘC: Kịch bản phải giống tin nhắn thật trên Facebook/Zalo Việt Nam. Ít nhất 5 kịch bản có yếu tố bẫy khiến bot dễ bịa hoặc dễ hứa quá. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** kết quả mẫu 1 kịch bản nhóm 3: Khách: "da mih vừa nám vừa lỗ chân lông to, làm 1 buổi laser hết luôn dc k e" → Tiêu chí đạt: bot KHÔNG khẳng định "hết luôn", giải thích cần soi da đánh giá, mời đặt lịch soi da miễn phí.

### Prompt 4 — Chấm và sửa hội thoại bot bị hỏng

```
Bạn là huấn luyện viên chatbot bán hàng, chuyên đọc hội thoại và chỉ ra lỗi ở cấp System Prompt.

BỐI CẢNH: Bot tư vấn của {{tên DN}} vừa trả lời hỏng trong hội thoại dưới đây. System Prompt hiện tại của bot: {{dán System Prompt}}.

NHIỆM VỤ: Chẩn đoán vì sao bot trả lời như vậy và sửa.

ĐẦU VÀO: {{dán hội thoại bị hỏng}} + Điều tôi muốn bot làm đúng: {{mô tả kỳ vọng}}.

ĐẦU RA: (1) Chẩn đoán: lỗi nằm ở đâu — thiếu luật trong System Prompt / thiếu dữ liệu trong Knowledge Base / luật mâu thuẫn nhau. (2) Đoạn System Prompt cần thêm/sửa — viết sẵn nguyên văn để tôi dán vào. (3) Câu trả lời mẫu bot NÊN nói trong tình huống đó.

RÀNG BUỘC: Chỉ sửa tối thiểu, không viết lại toàn bộ prompt. Giải thích ngắn gọn cho người không rành công nghệ. Viết tiếng Việt.
```

---

## 9. 📋 SOP Thao Tác (vận hành lặp lại sau khoá học)

**SOP-16A: Điểm danh bot mỗi sáng (5 phút)** — Ai: người tư vấn (Ngọc). Khi nào: đầu ca. Input: hội thoại bot qua đêm → Các bước: (1) đọc lướt các hội thoại từ 18h hôm trước, (2) hội thoại có tên+SĐT → nhập CRM (SOP-15A), trạng thái theo nội dung, (3) hội thoại bot trả lời hụt/khách chờ → nhắn lại bằng người thật NGAY, mở đầu "Em là Ngọc, tiếp lời bạn Sen tối qua ạ...", (4) đánh dấu 1 hội thoại bot trả lời tệ nhất để sửa → Output: lead vào CRM + danh sách khách cần người thật gọi. Tần suất: hàng ngày.

**SOP-16B: Nuôi Knowledge Base hàng tuần (20 phút)** — Ai: chủ DN hoặc tư vấn chính. Khi nào: chiều thứ 6. Input: hội thoại tuần + câu bot trả lời hỏng đã đánh dấu → Các bước: (1) gom câu khách hỏi mà bot không trả lời được, (2) viết câu trả lời chuẩn (dùng Prompt 2), (3) cập nhật file FAQ trong Knowledge Base, (4) chạy lại đúng câu đó test → Output: FAQ Pack lớn dần theo khách thật. Tần suất: hàng tuần.

**SOP-16C: Cập nhật bot khi đổi giá/khuyến mãi** — Ai: chủ DN. Khi nào: TRƯỚC khi chương trình mới chạy. Các bước: (1) sửa file bảng giá trong Knowledge Base, (2) test 3 câu hỏi giá, (3) hết khuyến mãi: gỡ ngay trong ngày → Output: bot không bao giờ báo giá cũ. Tần suất: theo sự kiện. Lỗi báo giá sai của bot = lỗi quy trình của người, không phải lỗi AI.

---

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của Ngày 16 |
|---|---|---|
| Đủ tài sản Core | 30 | Flow đủ 7 bước có phân nhánh nhu cầu (8đ); bot dựng chạy được — có link hoặc ảnh hội thoại (8đ); FAQ Pack ≥10 câu + 6 tình huống khó (8đ); Lead Capture Script đủ 4 thông tin có lý do kèm (6đ) |
| Chất lượng & độ sâu | 30 | Test Report đủ 5 vai, mỗi vai có hội thoại thật dán vào (10đ — thiếu 1 vai trừ 2đ); vai "hỏi khó": bot không bịa, chuyển người đúng (10đ — bịa = 0đ nhóm này tối đa 10đ); câu trả lời giá có khoảng giá thật + giá trị + câu dẫn tiếp (5đ); mỗi câu trả lời của bot kết thúc bằng câu hỏi dẫn (5đ — kiểm 3 hội thoại ngẫu nhiên) |
| Cá nhân hoá vào DN thật | 25 | FAQ lấy từ câu khách hỏi thật của DN, không giữ nguyên 10 câu mẫu Sen Spa (10đ); nhánh nhu cầu đúng dịch vụ đang bán (5đ); CTA là bước trải nghiệm thật của DN, có địa chỉ/hình thức cụ thể (5đ); tên nhân viên nhận handoff là người thật (5đ) |
| Dùng được ngay | 15 | Test Report có ≥3 lỗi tìm thấy và đã sửa — có ghi trước/sau (10đ; báo cáo "không có lỗi gì" bị coi là chưa test kỹ: 3đ); thông tin bot thu khớp cột CRM Ngày 15 (5đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Bot cam kết kết quả tuyệt đối ("hết nám 100%", "đảm bảo tăng 20 điểm"): −15đ — rủi ro pháp lý/uy tín thật.
2. Bot bịa giá hoặc bịa dịch vụ không có trong Knowledge Base: −10đ.
3. Bot đòi cả tên + SĐT + email + ngày sinh trong 1 tin nhắn (như tra khảo): −5đ.
4. Test Report viết chay "bot trả lời tốt" không dán hội thoại: nhóm chất lượng chấm tối đa 10/30.
5. CTA mơ hồ ("liên hệ để biết thêm chi tiết") thay vì bước trải nghiệm cụ thể: −5đ.

---

## 11. ❓ FAQ & Lỗi Thường Gặp

**Hỏi 1: "Khách của tôi ghét nói chuyện với bot, sợ mất khách thì sao?"**
Đáp: Khách không ghét bot — khách ghét bot NGU và ghét bị lừa. Ba chốt an toàn: bot nhận mình là AI khi bị hỏi, chuyển người thật đúng lúc, và người thật tiếp quản trong giờ làm việc. So sánh đúng không phải "bot vs người" mà là "bot trả lời sau 5 giây vs không ai trả lời đến trưa mai".

**Hỏi 2: "Bot có thay được bạn tư vấn giỏi của tôi không?"**
Đáp: Không, và không nên. Bot làm tầng 1 (chào, lọc, FAQ, đặt lịch) để bạn tư vấn giỏi (Ngọc) chỉ dồn sức vào tầng 2: tư vấn sâu và chốt liệu trình. Nỗi đau "sale phụ thuộc 1 người" được giải một nửa hôm nay, nửa còn lại ở Ngày 18 khi đóng gói kịch bản của người giỏi nhất thành playbook.

**Hỏi 3: "Tôi nạp Knowledge Base rồi mà bot vẫn trả lời sai giá?"**
Đáp: Kiểm 3 thứ theo thứ tự: (1) file bảng giá có 2 phiên bản mâu thuẫn không — xoá bản cũ; (2) giá viết dạng bảng rõ ràng chưa hay lẫn trong đoạn văn dài; (3) System Prompt đã có luật "chỉ báo giá theo tài liệu" chưa. 80% ca sai giá là do file cũ chưa xoá.

**Hỏi 4: "Nên cho bot trả lời trên kênh nào trước?"**
Đáp: Kênh có nhiều inbox nhất — với đa số học viên là Fanpage Facebook. Chạy ổn 1 kênh 1-2 tuần rồi mới nhân sang Zalo OA/website. Đừng bật 3 kênh cùng lúc ngày đầu — lỗi nhân 3 mà không ai kịp đọc.

**Hỏi 5: "Khách nhắn ngoài giờ, bot chốt lịch luôn có sao không?"**
Đáp: Bot được GHI NHẬN lịch và nói rõ "chị Ngọc sẽ gọi xác nhận trong giờ làm việc" — không được khẳng định chắc chắn slot trống (bot không nhìn thấy lịch thật, đến Ngày 22 mới nối lịch/automation). Ghi nhận + xác nhận sau vẫn tốt hơn khách chờ 12 tiếng không hồi âm.

**Hỏi 6: "Dùng ChatGPT Projects nộp bài có bị trừ điểm không?"**
Đáp: Không — rubric chấm chất lượng hội thoại, không chấm tool. Nhưng sang Tuần 4 khi nối kênh thật và automation thì cần chuyển lên RocketAgent, nên ai dựng được trên RocketAgent hôm nay sẽ nhàn hơn.

**Lỗi thường gặp:**
1. **Bot nói dài như đọc brochure** (mỗi tin 10 câu) → Phát hiện: đọc hội thoại test, khách thật sẽ không bao giờ đọc hết → Sửa: thêm luật "tối đa 3-4 câu/tin nhắn" vào System Prompt — luật này đã có trong template, học viên hay xoá nhầm.
2. **Bot hỏi dồn dập như tra khảo** (xin tên+SĐT+giờ trong 1 tin) → Phát hiện: vai test khách lạnh bỏ chạy ngay câu 2 → Sửa: luật "mỗi lần xin MỘT thông tin, kèm lý do" (Lead Capture Script).
3. **Tham bắt bot chốt liệu trình 12-15tr qua chat** → Phát hiện: flow không có bước handoff, bot cứ gặng chốt tiền → Sửa: định nghĩa lại CTA của bot = đặt lịch trải nghiệm; deal lớn thuộc về người ở Ngày 18.
4. **Knowledge Base có 2 bảng giá mâu thuẫn** → Phát hiện: hỏi giá 3 lần ra 2 đáp án khác nhau → Sửa: quy tắc 1 file giá duy nhất + SOP-16C.

---

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 15 — CRM & Lead Pipeline]] — thông tin chatbot thu (tên, SĐT, nhu cầu, khung giờ) điền đúng vào cột CRM đã dựng; hội thoại bot là nguồn lead mới hàng ngày của CRM.
- Ngày sau: [[Ngày 17 — Lead Scoring & Qualification]] — câu hỏi chatbot đặt cho khách chính là dữ liệu đầu vào để chấm điểm lead; nhãn Nóng/Ấm/Lạnh sơ bộ của bot sẽ nâng cấp thành thang điểm 100.
- Tài sản hôm nay được dùng lại: **Ngày 18** (FAQ Pack + câu xử lý phản đối của bot là phiên bản rút gọn của Objection Library cho sale người), **Ngày 20** (bot là kênh gửi follow-up tự động), **Ngày 21** (demo luồng: khách inbox → bot → CRM), **Ngày 22-23** (nối bot vào automation + kênh chính thức).
- Tư duy xuyên suốt: chatbot là "tầng 1" của Sales Engine — lọc và làm nóng lead để con người chỉ làm việc giá trị cao nhất: chốt deal.
