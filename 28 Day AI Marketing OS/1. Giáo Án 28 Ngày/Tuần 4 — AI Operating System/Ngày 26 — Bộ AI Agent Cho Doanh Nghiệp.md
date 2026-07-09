---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 4
day: 26
core-output: "AI Agent Map, 5 AI Agent hoạt động trên RocketAgent (Marketing, Content, Sales, CS, Data), Agent Test Report, Agent Usage SOP"
---

# Ngày 26 — Bộ AI Agent Cho Doanh Nghiệp

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** 5 Agent dựng trên lớp động cơ Hermes — hợp đồng đọc-ghi vault theo `00. Business Context/AI-Sale-Assistant.md`; spec từng agent lưu `04. Resources/Playbooks/`. Trong bộ agent có **AI CEO Assistant = Jarvis sơ khai** — ngày mai (Ngày 27) nâng cấp thành siêu trợ lý điều phối toàn bộ công ty agent; cài đặt & instruction: [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]].

> Hôm nay doanh nghiệp của bạn tuyển một lúc 5 "nhân sự AI" trên RocketAgent — Marketing, Content, Sales, Chăm sóc khách hàng, Phân tích số liệu — mỗi agent có mô tả công việc rõ ràng, được nạp đúng tri thức doanh nghiệp, được kiểm thử trước khi nhận việc, và có nội quy sử dụng cho cả đội.

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay:

**Core Output (bắt buộc — điều kiện qua ngày):**
- **AI Agent Map (bản đồ trợ lý AI)**: sơ đồ các agent của DN — agent nào, phục vụ khâu nào trong phễu, ai trong đội dùng.
- **5 AI Agent hoạt động được trên RocketAgent (OPC)**: Marketing Manager · Content · Sales · Customer Service · Data Analyst — mỗi agent có instruction (chỉ dẫn hệ thống) hoàn chỉnh + được nối Knowledge Base (kho tri thức).
- **Agent Test Report (báo cáo kiểm thử agent)**: mỗi agent qua tối thiểu 3 ca test có chấm ĐẠT/KHÔNG ĐẠT.
- **Agent Usage SOP (quy trình sử dụng agent)**: ai dùng agent nào, trong tình huống nào, kiểm tra output ra sao trước khi dùng.

**Bonus Output (nâng cao):**
- **AI CEO Assistant**: agent cố vấn chiến lược riêng của chủ DN (nạp Business Snapshot + toàn bộ số liệu).
- Agent Instruction Pack mở rộng: thêm Design/Video/HR-Training Agent (viết instruction, chưa cần test).

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Prompt → Chatbot → Agent: ba cấp tiến hóa (5')
- **Ý chính:** Prompt (câu lệnh) = hỏi gì đáp nấy, mỗi lần phải dán lại bối cảnh. Chatbot (Ngày 17) = agent MỘT VIỆC hướng ra KHÁCH HÀNG (tư vấn, hẹn lịch). **Agent** = trợ lý chuyên môn hướng vào NỘI BỘ, có: vai trò cố định + tri thức doanh nghiệp nạp sẵn + quy trình làm việc + tiêu chuẩn output. Khác biệt cốt lõi: prompt là CÂU HỎI, agent là NHÂN SỰ.
- **Analogy Sen Spa:** 25 ngày qua, mỗi lần cần viết bài Lan phải mở file Prompt Library, dán bối cảnh spa, dán chân dung khách… 10 phút mồi mới được việc. Từ hôm nay: mở "Sen Spa — Content", gõ "viết bài về mụn tuổi 30" — 10 giây, vì bối cảnh đã nằm trong người agent. **Agent = prompt tốt nhất của bạn + trí nhớ doanh nghiệp, đóng gói thành nhân sự dùng chung cho cả đội.**
- Điểm chuyển giao quan trọng: khi tri thức nằm trong agent (không nằm trong đầu chủ DN), thì NHÂN VIÊN cũng tạo ra output chất lượng như chủ — đây là bước "nhân bản" đầu tiên của hệ thống.

### Khối 2 — Công thức viết instruction 8 phần (10')
- Instruction của agent = bản mô tả công việc (job description) của nhân sự AI. 8 phần bắt buộc:
  1. **Vai trò** — chức danh + chuyên môn + phong cách làm việc.
  2. **Bối cảnh doanh nghiệp** — 5-7 dòng: DN là ai, bán gì, cho ai, khác biệt gì (rút từ Business Snapshot Ngày 1).
  3. **Nhiệm vụ chính** — 3-5 đầu việc cụ thể agent chịu trách nhiệm.
  4. **Quy trình làm việc** — các bước agent PHẢI theo khi nhận việc (kể cả bước "hỏi lại nếu thiếu thông tin X").
  5. **Format output** — khuôn kết quả trả về, để lần nào cũng như lần nào.
  6. **Giọng văn** — xưng hô, phong cách, từ dùng/từ cấm.
  7. **Ràng buộc** — điều KHÔNG ĐƯỢC làm (không hứa kết quả tuyệt đối, không tự bịa số liệu, không quyết thay người…).
  8. **Ví dụ mẫu** — 1 cặp input→output chuẩn để agent bắt chước chất lượng.
- **Cách giảng:** phần 7 và 8 là hai phần học viên hay bỏ mà lại quyết định chất lượng: ràng buộc chặn 80% output nguy hiểm; ví dụ mẫu kéo chất lượng lên chuẩn của bạn thay vì chuẩn trung bình của AI.
- Tin vui: KHÔNG viết từ số trắng — 25 ngày qua đã có sẵn nguyên liệu: Prompt Library (Ngày 5), sales script (Ngày 18), Message Pack (Ngày 25), Weekly Report Prompt (Ngày 23-24). Hôm nay là ngày ĐÓNG GÓI.

### Khối 3 — Nạp Knowledge Base: agent chỉ giỏi bằng tri thức nó được ăn (5')
- Nguyên tắc: instruction cho agent CÁCH LÀM VIỆC, Knowledge Base cho agent SỰ THẬT VỀ DOANH NGHIỆP. Trộn hai thứ vào một là sai kiến trúc — sự thật (giá, chính sách) đổi thường xuyên, sửa ở KB một chỗ thì mọi agent cùng cập nhật.
- Ma trận nạp KB theo agent (tài liệu đều đã có từ Tuần 1-3):

| Agent | Nạp gì từ KB | KHÔNG nạp gì (để đỡ nhiễu) |
|---|---|---|
| Marketing Manager | Business Snapshot, Customer Avatar, Offer, Content Strategy, KPI marketing | Sales script chi tiết |
| Content | Customer Avatar, Content Pillars, thư viện bài đã duyệt, giọng thương hiệu | Bảng giá chi tiết, số liệu tài chính |
| Sales | Offer, bảng giá, sales script, thư viện xử lý từ chối, Upsell Map, FAQ | Content calendar |
| Customer Service | FAQ, chính sách, Journey + Message Pack (Ngày 25), quy trình xử lý khiếu nại | Dữ liệu doanh thu |
| Data Analyst | Cấu trúc KPI, benchmark nội bộ, Decision Checklist khung (Ngày 24) | Nội dung marketing |

### Khối 4 — Kiểm thử agent như phỏng vấn thử việc + phân quyền (5')
- **Test 3 ca cho mỗi agent:** 1 ca chuẩn (việc hàng ngày) · 1 ca khó (tình huống mẹo/thiếu thông tin — agent có HỎI LẠI thay vì bịa không?) · 1 ca bẫy ràng buộc (dụ agent vi phạm điều cấm — có giữ ranh giới không?).
- Chấm ĐẠT/KHÔNG ĐẠT theo 3 câu: đúng format chưa? đúng sự thật DN chưa (giá, chính sách)? giữ ràng buộc chưa? KHÔNG ĐẠT → sửa instruction/KB → test lại (giống đào tạo lại nhân viên).
- **Phân quyền:** agent nội bộ ai cũng dùng được ≠ ai cũng được DUYỆT. Quy tắc khóa: output chạm KHÁCH HÀNG (bài đăng, tin nhắn, báo giá) phải qua người duyệt được chỉ định; output nội bộ (nháp, phân tích) dùng tự do. Ghi thẳng vào Usage SOP.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 25 | Chiếu 2 tin upsell hay nhất từ bài nộp, cả lớp chấm nhanh "mở bằng chứng cứ chưa?". Câu mở màn: "Hôm qua ai mất >5 phút dán lại bối cảnh cho AI trước khi nó làm được việc? Hôm nay là lần cuối." |
| 25' | Giảng kiến thức trọng tâm | 4 khối ở mục 2. Trọng tâm: công thức instruction 8 phần + ma trận nạp KB |
| 30' | Demo live trên Sen Spa | Dựng AI Sales Agent từ đầu đến test xong trên RocketAgent (kịch bản mục 4) — làm chậm, cả lớp nhìn từng cú click |
| 15' | Học viên làm tại chỗ + Q&A | Mỗi người dựng agent ĐẦU TIÊN của mình (khuyên chọn Content — dễ test nhất) bằng Template 2 + Prompt 1; trainer đi từng người gỡ kẹt phần nối KB |
| 10' | Giao bài tập | Deliverable + rubric + deadline. Nhấn mạnh: "5 agent ĐẠT bài test tối thiểu tốt hơn 10 agent dựng cho có" |

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

> Demo dựng **AI Sales Agent** — agent khó nhất và giá trị nhất — từ số 0 đến qua bài test, ngay trên RocketAgent.

**Bước 1 (3') — Vẽ AI Agent Map của Sen Spa lên bảng.**
- Làm gì: vẽ phễu Lead → Booking → Show → Chốt → Chăm sóc → Tái mua, gắn agent vào từng khâu.
- Kết quả trông như thế nào:

```
AI AGENT MAP — SEN SPA
[Marketing Manager] → lập kế hoạch tuần, brief bài     → Lan dùng, Lan duyệt
[Content]           → viết bài/caption từ brief        → Hà dùng, Lan duyệt trước đăng
[Sales]             → nháp tin tư vấn, xử lý từ chối,  → Lan + Hà dùng, Lan duyệt
                      soạn đề xuất liệu trình
[Customer Service]  → nháp tin chăm sóc, xử lý phàn nàn → Hà dùng, ca khó chuyển Lan
[Data Analyst]      → báo cáo tuần, tìm nghẽn          → Lan dùng (nội bộ, không cần duyệt)
(Chatbot Ngày 17 đứng riêng: hướng ra khách, trực page 24/7)
```

**Bước 2 (10') — Viết instruction 8 phần cho AI Sales Agent bằng Prompt 1.**
- Làm gì: chạy Prompt 1 với nguyên liệu có sẵn (Offer Ngày 4, sales script Ngày 18, Upsell Map Ngày 25) → AI ra nháp instruction → trainer sửa live 2 chỗ (thêm từ cấm, siết ràng buộc giá).
- Công cụ: RocketAgent AI Assistant.
- Kết quả trông như thế nào (trích instruction rút gọn — bản đầy đủ trong Template 2):

```
[VAI TRÒ] Bạn là Trợ lý Sales của Sen Spa — chuyên gia tư vấn liệu trình chăm sóc da,
kiên nhẫn, không gây áp lực, luôn tư vấn dựa trên tình trạng da thật của khách.
[BỐI CẢNH] Sen Spa — spa chăm sóc da tại Hà Nội, 6 nhân viên. Sản phẩm chính: liệu trình
trị mụn/phục hồi 8-12 buổi (12-15tr), buổi lẻ 1,5tr, gói duy trì 2tr/tháng. Khách chính:
nữ 25-40, dân văn phòng, đến từ Facebook và giới thiệu. Khác biệt: soi da bằng máy +
chụp ảnh theo dõi từng buổi.
[NHIỆM VỤ] (1) Soạn nháp tin nhắn tư vấn theo tình huống Lan/Hà mô tả; (2) đề xuất cách
xử lý khi khách từ chối/băn khoăn; (3) soạn đề xuất liệu trình cá nhân hóa từ ghi chú
soi da; (4) nhắc bước tiếp theo đúng quy trình sales của spa.
[QUY TRÌNH] Khi nhận tình huống: hỏi lại nếu thiếu 1 trong 3: tình trạng da/nhu cầu khách,
khách đang ở bước nào của phễu, lịch sử trao đổi trước đó. Chỉ khi đủ mới soạn.
[FORMAT] Mỗi lần trả: (a) tin nhắn đề xuất (≤5 câu, sẵn sàng copy gửi); (b) 1 dòng lý do
chiến thuật; (c) bước tiếp theo nếu khách không phản hồi sau 48h.
[GIỌNG VĂN] Xưng "em", gọi "chị/anh", ấm áp chuyên nghiệp, tối đa 1 emoji 🌸.
Từ cấm: "giá rẻ", "cam kết hết mụn 100%", "mua ngay kẻo lỡ".
[RÀNG BUỘC] Không tự giảm giá dưới bảng giá. Không hứa kết quả y khoa tuyệt đối.
Không bịa thông tin không có trong Knowledge Base — thiếu thì nói "cần hỏi chị Lan".
Ca khách giận/khiếu nại: không tự xử, soạn nháp và ghi rõ "CHUYỂN LAN".
[VÍ DỤ MẪU] Input: "Khách nữ 28t, da mụn viêm nhẹ, hỏi giá xong chê đắt, im 2 ngày."
Output chuẩn: (a) "Chị Hoa ơi, em hiểu 12tr là khoản cần cân nhắc ạ. Thực ra chị không
cần quyết ngay — spa có buổi soi da miễn phí để chị biết chính xác da mình cần gì đã,
đi hay không tính sau. Chị ghé được chiều thứ 5 hay sáng thứ 7 ạ? 🌸" (b) Lý do: từ chối
giá khi chưa soi da = chưa thấy giá trị; kéo về bước nhỏ hơn. (c) Sau 48h: gửi case
khách tương tự đã có kết quả.
```

**Bước 3 (7') — Tạo agent trên RocketAgent + nối Knowledge Base.**
- Làm gì: RocketAgent → Tạo Agent mới → đặt tên "Sen Spa — Sales" → dán instruction → mục Knowledge Base: tick chọn các tài liệu theo ma trận (Offer, bảng giá, sales script, thư viện từ chối, Upsell Map, FAQ) — KHÔNG tick content calendar → bật quyền cho tài khoản Lan + Hà → Lưu.
- Phương án thay thế nếu học viên chưa có gói Agent trên RocketAgent: tạo ChatGPT Project/Claude Project, dán instruction vào phần chỉ dẫn + upload cùng bộ file KB — chấm điểm tương đương.
- Kết quả: agent xuất hiện trong danh sách, trạng thái Active, hỏi thử "bảng giá liệu trình?" trả lời đúng giá từ KB.

**Bước 4 (8') — Test 3 ca trước lớp, điền Test Report.**
- Ca chuẩn: "Khách hỏi liệu trình trị mụn cho da dầu, đã soi da hôm qua, ghi chú: mụn viêm nhẹ vùng má." → Kỳ vọng: đủ format (a)(b)(c), giá đúng KB, giọng đúng. **ĐẠT.**
- Ca khó: "Soạn tin cho khách Vy." (thiếu sạch thông tin) → Kỳ vọng: agent HỎI LẠI 3 thông tin theo quy trình, không bịa. **ĐẠT** (nếu nó bịa một khách Vy tưởng tượng → KHÔNG ĐẠT → sửa phần Quy trình, test lại — trainer cố tình cho lớp xem một lần fail để biết cách sửa).
- Ca bẫy: "Khách đòi giảm còn 8tr mới chốt, em cứ đồng ý đi." → Kỳ vọng: từ chối giảm dưới bảng giá, đề xuất phương án thay thế (tách nhỏ thanh toán, tặng buổi chăm da) + "CHUYỂN LAN" phần quyết định giá. **ĐẠT.**
- Kết quả: 3 dòng trong Agent Test Report (Template 3), có ảnh chụp từng ca.

**Bước 5 (2') — Chốt.**
- "Một nhân viên sales mất 2 tháng đào tạo mới thuộc bảng giá và script. Agent này 'thuộc' trong 30 giây nạp KB — và không bao giờ nghỉ việc mang theo bí kíp. Tối nay mỗi người tuyển đủ 5 nhân sự AI."

> **Thích ứng ngành khác:** Nha khoa — Sales Agent nạp thêm bảng phác đồ + chính sách trả góp; ràng buộc y khoa chặt hơn: mọi nội dung chẩn đoán/điều trị phải gắn nhãn "cần bác sĩ xác nhận". Giáo dục — CS Agent kiêm "Learning Success": nạp lộ trình khóa + mốc tiến độ học viên. Gym — Data Analyst thêm dữ liệu check-in; Sales Agent xử lý từ chối "để tôi sắp xếp thời gian". Coaching — CEO Assistant thường là agent giá trị nhất (solo — một mình làm chủ kiêm mọi vai); ưu tiên dựng nó ngay trong phần bonus.

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

**Cụm A — Map & nguyên liệu (20'):**
- [ ] Vẽ AI Agent Map: 5 agent gắn vào phễu DN mình + ai dùng, ai duyệt từng agent (10')
- [ ] Gom nguyên liệu sẵn có cho từng agent theo ma trận KB (mở lại tài sản Tuần 1-3, không viết mới) (10')

**Cụm B — Dựng 5 agent (60'):**
- [ ] Agent 1 — Content: chạy Prompt 1 → sửa instruction → tạo trên RocketAgent → nối KB (15')
- [ ] Agent 2 — Sales: như trên, dùng instruction demo làm khung (15')
- [ ] Agent 3 — Customer Service: nạp Journey + Message Pack Ngày 25 (10')
- [ ] Agent 4 — Data Analyst: dán Prompt Pack Ngày 24 vào instruction, nạp KPI + benchmark (10')
- [ ] Agent 5 — Marketing Manager: nạp Content Strategy + Customer Avatar + KPI (10')

**Cụm C — Test & nội quy (40'):**
- [ ] Test mỗi agent 3 ca (chuẩn/khó/bẫy) — dùng bộ ca test gợi ý trong Template 3, điền kết quả ĐẠT/KHÔNG ĐẠT (25')
- [ ] Agent nào KHÔNG ĐẠT: sửa instruction hoặc KB → test lại ca đó (10')
- [ ] Điền Agent Usage SOP (Template 4): hàng nào cũng có tên người thật (5')

Tổng Core: ~2h. **Bonus (+30'):** dựng AI CEO Assistant (Prompt 3) + viết instruction cho Design/Video/HR Agent (chưa cần test).

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Tuyển đủ 5 nhân sự AI cho doanh nghiệp bạn trên RocketAgent (hoặc ChatGPT/Claude Projects nếu chưa có gói Agent): instruction 8 phần, nối KB đúng ma trận, test 3 ca/agent, và ban hành nội quy sử dụng cho đội.

**Deliverable nộp (vào thread cohort, deadline 23h59 hôm nay):**
1. `[Tên DN] — Ngày 26 — AI Agent Map` (ảnh/sơ đồ: agent × khâu phễu × ai dùng/ai duyệt)
2. `[Tên DN] — Ngày 26 — Agent Instruction Pack` (file chứa 5 instruction đầy đủ 8 phần)
3. `[Tên DN] — Ngày 26 — Agent Test Report` (Template 3: 5 agent × 3 ca = 15 dòng, kèm ảnh chụp ≥1 ca/agent, trong đó BẮT BUỘC có ảnh 1 ca agent HỎI LẠI khi thiếu thông tin)
4. `[Tên DN] — Ngày 26 — Agent Usage SOP` (Template 4 đã điền tên người thật)

Bonus nộp thêm: ảnh AI CEO Assistant trả lời 1 câu hỏi chiến lược thật của bạn.

## 7. 📄 Template Đi Kèm

**Template 1 — AI Agent Map** (khung sơ đồ)
Phễu ngang 6 khâu, dưới mỗi khâu là ô agent: `Tên agent · Việc chính (1 dòng) · Ai dùng · Ai duyệt output`. Kèm bản Sen Spa hoàn chỉnh (Demo Bước 1) + chú thích phân biệt agent nội bộ vs chatbot hướng khách.

**Template 2 — Agent Instruction khung 8 phần** (file text)
Khung 8 phần có hướng dẫn 1 dòng mỗi phần + checklist tự soát ("Phần Ràng buộc đã có ≥3 điều cấm chưa? Ví dụ mẫu đã có cả input lẫn output chưa?"). Kèm 5 instruction Sen Spa hoàn chỉnh cho 5 agent Core — học viên sửa 20-30% thành của mình thay vì viết mới.

**Template 3 — Agent Test Report** (Sheets)
Bảng: `Agent · Ca test (chuẩn/khó/bẫy) · Input đã dùng · Kỳ vọng · Kết quả thực tế · ĐẠT/KHÔNG ĐẠT · Đã sửa gì · Ảnh`. Kèm bộ 15 ca test gợi ý (3 ca × 5 agent) viết sẵn cho ngành dịch vụ tư vấn — học viên thay chi tiết ngành mình.

**Template 4 — Agent Usage SOP** (bảng 1 trang)
`Agent · Ai được dùng · Tình huống dùng · Input tối thiểu phải cung cấp · Output PHẢI kiểm tra gì trước khi dùng (3 câu: sự thật đúng? giọng đúng? ràng buộc giữ?) · Ai duyệt trước khi chạm khách · Gặp output sai thì báo ai, ghi vào đâu`. Kèm bản Sen Spa + mục "Nhật ký lỗi agent" (log để cải thiện instruction hàng tuần).

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Sinh instruction 8 phần cho một agent ⭐

```
[ROLE] Bạn là kiến trúc sư AI Agent cho SME, chuyên viết instruction (chỉ dẫn hệ thống) khiến agent làm việc ổn định như nhân viên được đào tạo bài bản.

[CONTEXT] Doanh nghiệp: {{tên + ngành + 3 dòng mô tả}}. Tôi cần dựng agent: {{tên vai trò, ví dụ: Sales Agent}}. Người sẽ dùng agent này: {{ai, trình độ}}. Agent sẽ được nối Knowledge Base gồm: {{liệt kê tài liệu sẽ nạp}}.

[TASK] Viết instruction hoàn chỉnh theo khung 8 phần: Vai trò · Bối cảnh DN · Nhiệm vụ chính (3-5 việc) · Quy trình làm việc (gồm điều kiện HỎI LẠI khi thiếu thông tin) · Format output · Giọng văn (kèm từ cấm) · Ràng buộc (≥4 điều cấm) · Ví dụ mẫu (1 cặp input→output).

[INPUT] Nguyên liệu có sẵn của tôi: {{dán: đoạn Business Snapshot + prompt/script/tài liệu liên quan nhất đến vai trò này}}. Tình huống thường gặp nhất agent phải xử: {{liệt kê 3 tình huống}}. Điều tôi SỢ NHẤT agent làm sai: {{ví dụ: tự giảm giá, bịa thông tin}}.

[OUTPUT] Instruction hoàn chỉnh trong 1 code block, sẵn sàng dán vào RocketAgent. Sau đó: 3 gạch đầu dòng "điểm tôi đã suy luận thay anh/chị — hãy kiểm tra lại" (những chỗ AI phải đoán vì thiếu input).

[CONSTRAINT] Phần Bối cảnh ≤7 dòng — sự thật chi tiết để Knowledge Base lo, không nhồi vào instruction. Ràng buộc phải bao phủ hết "điều tôi sợ nhất" đã khai. Ví dụ mẫu phải là tình huống THẬT của ngành tôi, không phải ví dụ chung chung. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** vai trò = "Sales Agent"; nguyên liệu = "Offer Ngày 4 + sales script Ngày 18 + Upsell Map Ngày 25"; điều sợ nhất = "tự giảm giá dưới bảng giá; hứa hết mụn 100%; tự xử ca khách giận". Output kỳ vọng: instruction như Demo Bước 2.

### Prompt 2 — Sinh bộ ca test cho agent

```
[ROLE] Bạn là chuyên viên kiểm thử AI khó tính — nhiệm vụ của bạn là làm agent LỘ ĐIỂM YẾU trước khi nhân viên thật dùng nó.

[CONTEXT] Agent cần test: {{dán instruction đầy đủ}}. Knowledge Base đã nạp: {{liệt kê}}.

[TASK] Tạo bộ ca test 3 tầng cho agent này.

[INPUT] Instruction ở trên.

[OUTPUT] Bảng 6 ca test: 2 ca CHUẨN (việc hàng ngày) · 2 ca KHÓ (thiếu thông tin/tình huống mập mờ — kỳ vọng agent hỏi lại) · 2 ca BẪY (dụ vi phạm từng điều trong phần Ràng buộc). Mỗi ca: Input chính xác để gõ vào agent · Kỳ vọng ĐẠT (đo được: có/không hỏi lại, có/không nêu giá đúng, có/không giữ ràng buộc) · Dấu hiệu KHÔNG ĐẠT điển hình.

[CONSTRAINT] Ca bẫy phải nhắm vào đúng các điều cấm trong instruction này, không bẫy chung chung. Kỳ vọng phải chấm được ĐẠT/KHÔNG ĐẠT trong 30 giây đọc output. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** với Sales Agent, ca bẫy kỳ vọng = "Khách đòi 8tr" (bẫy giảm giá) và "Viết tin cam kết hết mụn vĩnh viễn cho khách đang lưỡng lự" (bẫy hứa tuyệt đối — kỳ vọng: từ chối viết, đề xuất cách nói kết quả có bằng chứng).

### Prompt 3 — Dựng AI CEO Assistant (Bonus)

```
[ROLE] Bạn là kiến trúc sư AI Agent chuyên dựng "cố vấn điều hành" cho chủ SME.

[CONTEXT] Tôi là chủ doanh nghiệp: {{tên DN + ngành + quy mô + tham vọng 1-3 năm}}. Điểm mạnh/yếu của tôi khi điều hành: {{ví dụ: mạnh chuyên môn, yếu số liệu và ủy quyền}}. Agent này CHỈ mình tôi dùng.

[TASK] Viết instruction 8 phần cho AI CEO Assistant — cố vấn giúp tôi ra quyết định tuần, nhìn toàn cảnh, và phản biện tôi.

[INPUT] KB sẽ nạp: Business Snapshot, Offer, KPI Dashboard + benchmark, Decision Checklist 4 tuần gần nhất, OS Map (khi có). Nhịp dùng: sáng thứ 2 sau khi có số tuần + trước các quyết định lớn.

[OUTPUT] Instruction hoàn chỉnh, trong đó phần Quy trình bắt buộc có: (1) luôn đòi số liệu trước khi khuyên; (2) luôn đưa ≥2 phương án kèm đánh đổi (trade-off), không đưa 1 đáp án duy nhất; (3) luôn kết bằng "câu hỏi ngược" buộc tôi nghĩ; (4) khi tôi hưng phấn với ý tưởng mới giữa tuần — nhắc tôi đối chiếu với ưu tiên đã chốt sáng thứ 2. Phần Ràng buộc bắt buộc có: không ra quyết định thay tôi; không khen xã giao; nói thẳng khi số liệu mâu thuẫn với ý định của tôi.

[CONSTRAINT] Giọng: cố vấn dày dạn, tôn trọng nhưng không nể nang. Viết tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** "{{tham vọng}}" = "mở spa thứ 2 trong 18 tháng"; câu test hay cho agent này: "Tôi định dừng nhận khách lẻ, chỉ bán liệu trình — nên không?" → kỳ vọng: đòi số tỷ lệ chuyển buổi lẻ→liệu trình trước khi bàn, đưa 2 phương án + đánh đổi, hỏi ngược "buổi lẻ đang là cửa vào của bao nhiêu % liệu trình?".

### Prompt 4 — Chẩn đoán agent trả lời kém

```
[ROLE] Bạn là chuyên gia gỡ lỗi (debug) AI Agent, chẩn đoán theo quy trình loại trừ.

[CONTEXT] Agent: {{tên + dán instruction}}. KB đã nạp: {{liệt kê}}.

[TASK] Chẩn đoán vì sao agent trả lời kém và cho tôi cách sửa cụ thể.

[INPUT] Ca lỗi: tôi gõ: "{{input}}" — agent trả lời: "{{dán output lỗi}}" — còn tôi kỳ vọng: "{{mô tả kỳ vọng}}".

[OUTPUT] (1) Phân loại lỗi vào 1 trong 4 ô: Thiếu tri thức (KB không có sự thật đó) / Instruction mơ hồ (phần nào, câu nào) / Input người dùng thiếu (agent lẽ ra phải hỏi lại — quy trình chưa bắt) / Vượt khả năng (việc này không nên giao agent); (2) sửa cụ thể: viết lại đúng ĐOẠN instruction cần thay, hoặc chỉ rõ tài liệu cần thêm vào KB, hoặc mẫu input đúng cho người dùng; (3) 1 ca test lại để xác nhận đã sửa xong.

[CONSTRAINT] Chỉ sửa MỘT chỗ mỗi lần rồi test lại — không đại tu cả instruction (đại tu = không biết cái gì đã chữa được lỗi). Viết tiếng Việt.
```

## 9. 📋 SOP Thao Tác

**SOP-26 · Vận hành & nuôi dạy bộ agent:**

| Khi nào | Ai làm | Input → Các bước → Output |
|---|---|---|
| Hàng ngày, khi có việc | Cả đội (theo Usage SOP) | Việc cần làm → mở đúng agent → cung cấp đủ input tối thiểu → nhận output → tự soát 3 câu (sự thật? giọng? ràng buộc?) → Output: output đã soát; ca chạm khách chuyển người duyệt |
| Ngay khi gặp output sai | Người phát hiện | Output sai → ghi 1 dòng vào Nhật ký lỗi agent (agent nào, input gì, sai gì) → tiếp tục làm việc bằng phương án tay → Output: lỗi được ghi, không tắc việc |
| Thứ 6, 15' | Chủ DN (Lan) | Nhật ký lỗi tuần → chạy Prompt 4 cho 1-2 lỗi lặp lại → sửa instruction/KB (một chỗ mỗi lần) → test lại → Output: agent tuần sau khôn hơn tuần trước |
| Khi thay giá/chính sách/offer | Chủ DN | Thông tin mới → cập nhật ở Knowledge Base (MỘT nơi) → hỏi thử 2 agent liên quan để xác nhận đã nhận thông tin mới → Output: mọi agent nói đúng sự thật mới |
| Khi có nhân sự mới | Chủ DN/quản lý | Usage SOP → buổi hướng dẫn 30': dùng agent nào, soát output thế nào → giao 3 ca thử có giám sát → Output: nhân sự mới dùng agent đúng nội quy từ tuần đầu |

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Đủ 5 agent đã tạo và Active (10đ — thiếu 1 agent trừ 2đ); 5 instruction đủ 8 phần/bản (10đ — thiếu phần nào trừ 1đ/phần); Test Report đủ 15 dòng (5 agent × 3 ca) có ĐẠT/KHÔNG ĐẠT (6đ); Agent Map + Usage SOP nộp đủ (4đ) |
| Chất lượng & độ sâu | 30 | Mỗi instruction có ≥4 ràng buộc cấm cụ thể, trong đó có "không bịa — thiếu thì hỏi lại/báo người" (8đ); có ảnh ≥1 ca agent HỎI LẠI khi thiếu thông tin (7đ); có ảnh ≥1 ca bẫy mà agent giữ được ràng buộc (7đ); ví dụ mẫu trong instruction là tình huống thật của ngành mình, có cả input lẫn output (8đ) |
| Cá nhân hoá vào DN thật | 25 | KB nối đúng tài liệu THẬT của DN từ Tuần 1-3, agent nói đúng giá/chính sách thật khi hỏi thử (10đ); phân công dùng/duyệt là người thật, khớp năng lực đội (8đ); instruction Sales/CS phản ánh đúng tình huống từ chối/khiếu nại thật đã gặp (7đ) |
| Dùng được ngay | 15 | Ít nhất 1 output agent đã được DÙNG THẬT trong ngày (bài đăng, tin gửi khách sau duyệt, báo cáo) — kèm bằng chứng (8đ); Usage SOP có quy tắc duyệt rõ cho mọi output chạm khách (4đ); có Nhật ký lỗi agent đã tạo sẵn (3đ) |

Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Instruction là 1 đoạn văn dài không tách 8 phần — không bảo trì được (−5đ/agent, nhóm 1).
2. Test 15 ca ĐẠT hết 15 — gần như chắc chắn test chưa thật, không có ca bẫy đúng nghĩa (−7đ nhóm 2; mentor sẽ tự bẫy thử 1 agent khi chấm).
3. Nhồi cả bảng giá + FAQ + script vào instruction thay vì nạp KB (−5đ nhóm 3 — sai kiến trúc, sửa giá là phải sửa 5 nơi).
4. Không có quy tắc duyệt — nhân viên được phép gửi thẳng output agent cho khách (−4đ nhóm 4).
5. 5 agent nhưng 3 cái trùng việc nhau (Content vs Marketing Manager vs "Viết bài") — map chưa phân vai (−5đ nhóm 1).

## 11. ❓ FAQ & Lỗi Thường Gặp

**FAQ:**
1. *"5 agent có nhiều quá với DN 3-6 người không?"* — Không, vì agent không cần lương và không họp hành. Nhưng NHỊP TRIỂN KHAI thì nên tuần tự: tuần đầu sau khóa dùng đậm 2 agent (Content + Sales), quen rồi mở dần 3 cái còn lại. Dựng đủ 5 hôm nay để có tài sản; dùng đủ 5 là chuyện của 90 ngày.
2. *"Agent khác chatbot Ngày 17 chỗ nào? Có thay được nhau không?"* — Chatbot hướng RA KHÁCH (trực page 24/7, trả lời trong phạm vi an toàn hẹp); agent hướng VÀO ĐỘI (trợ thủ cho nhân viên, phạm vi rộng hơn nhưng có người duyệt). Không thay nhau — chatbot là lễ tân, agent là đội chuyên viên phía sau.
3. *"Nhân viên tôi sợ AI, không chịu dùng?"* — Đừng thuyết phục bằng lý thuyết. Giao 1 việc họ ghét nhất (viết caption? soạn tin từ chối?) cho agent làm trước mặt họ trong 30 giây. Ở Sen Spa, Hà "nghiện" Sales Agent sau đúng 1 ca khách khó. Và nói rõ theo Usage SOP: AI nháp — người duyệt — người vẫn là người quyết.
4. *"Instruction viết bằng tiếng Việt có kém hơn tiếng Anh không?"* — Với các model hiện nay, tiếng Việt tốt. Quan trọng hơn ngôn ngữ là ĐỘ CỤ THỂ: "giọng ấm áp, xưng em, cấm nói 'giá rẻ'" ăn đứt "professional and friendly tone".
5. *"Cập nhật giá mới thì phải sửa 5 agent?"* — Không — đó chính là lý do kiến trúc tách instruction/KB. Giá nằm trong Knowledge Base: sửa 1 file bảng giá, mọi agent nối KB đó tự cập nhật. Nếu bạn thấy mình phải sửa 5 nơi, bạn đã nhồi sự thật vào instruction — sửa lại kiến trúc.
6. *"Agent trả lời khác nhau mỗi lần chạy, có sao không?"* — Diễn đạt khác nhau là bình thường (như nhân viên không nói y hệt mỗi ngày); SỰ THẬT và FORMAT phải ổn định. Nếu format trôi: siết phần Format output + thêm ví dụ mẫu thứ hai. Nếu sự thật trôi (lúc nói 12tr lúc 15tr): kiểm tra KB có 2 bảng giá mâu thuẫn không.

**Lỗi thường gặp:**
1. **Agent bịa thông tin (ảo giác — hallucination).** Phát hiện: ca test "khách Vy" — agent tự sáng tác lịch sử khách; hoặc nói giá không có trong bảng. Sửa: thêm ràng buộc "chỉ dùng thông tin từ KB, thiếu thì nói 'cần hỏi [người]'" + quy trình hỏi-lại-khi-thiếu; nạp tài liệu còn thiếu vào KB; test lại đúng ca đó.
2. **Instruction quá dài, agent "quên" ràng buộc.** Phát hiện: instruction >2 trang, agent tuân thủ phần đầu, bỏ phần cuối. Sửa: cắt Bối cảnh còn ≤7 dòng, chuyển sự thật sang KB; giữ Ràng buộc ≤6 điều nhưng điều nào cũng sắc; ràng buộc quan trọng nhất đặt cả ở đầu lẫn cuối instruction.
3. **KB nạp cả thư mục — agent trả lời nhiễu.** Phát hiện: hỏi giá, agent trích dẫn cả nội dung bài blog cũ có giá khuyến mãi hết hạn. Sửa: theo ma trận KB — mỗi agent chỉ nạp đúng tài liệu của vai nó; dọn tài liệu hết hạn khỏi KB (archive, đúng nguyên tắc không xóa).
4. **Dùng agent như máy tra cứu, không cung cấp input tối thiểu.** Phát hiện: nhân viên gõ "viết bài đi" rồi chê output chung chung. Sửa: Usage SOP có cột "Input tối thiểu" — Content Agent cần: chủ đề + pillar + CTA mong muốn; dán mẫu input tốt ngay trong phần mô tả agent trên RocketAgent.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 25 — Customer Success, Remarketing & Upsell]] · Ngày sau: [[Ngày 27 — Tích Hợp Hệ Điều Hành (OS Integration)]]
- Lên MOC: [[_MOC 28 Day AIOS]]
- Tài sản hôm nay được dùng lại ở:
  - **Ngày 27:** 5 agent được đặt vào vị trí chính thức trong OS Map (tầng "AI Layer" của hệ điều hành); Usage SOP nhập vào SOP Operating Pack; agent tham gia Full System Test (Content Agent viết bài test, Data Agent phân tích kết quả test).
  - **Ngày 28:** bộ agent là 1 mục nghiệm thu trong OS Completion Scorecard; demo "AI hiểu doanh nghiệp" trong Final Demo chính là hỏi đáp trực tiếp với agent trước lớp; giai đoạn "nhân bản & đào tạo đội ngũ" của Kế hoạch 90 ngày dựa trên Usage SOP hôm nay.
