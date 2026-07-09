---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, hermes, jarvis, install]
---

# 🤵 Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis

> Tài liệu chuyển giao lớp ĐỘNG CƠ của AIOS: cài **Hermes Agent** (engine chạy 24/7) và dựng **Jarvis — siêu trợ lý điều hành** quản lý toàn bộ "công ty agent" của doanh nghiệp qua chat. Mẫu gốc: chính Jarvis của Tony (Hermes Agent + Telegram Gateway + HeyGen MCP, chạy từ 03/07/2026 — xem [[LN — Cài đặt thành công Jarvis — Siêu trợ lý AI]]). Kiến trúc nền: [[FW — OPC Platform Architecture]].

---

## 1. Jarvis đứng đâu trong AIOS — "công ty agent" hoàn chỉnh

```
                    👤 CEO (chủ doanh nghiệp)
                         │  ra lệnh & nhận báo cáo qua Telegram/Zalo
                         ▼
              🤵 JARVIS — SIÊU TRỢ LÝ ĐIỀU HÀNH          ← Tầng 6: Phòng Điều Khiển
              (Hermes Agent + Gateway chat + MCP)
        ┌──────────┬──────────┼──────────┬──────────┐
        ▼          ▼          ▼          ▼          ▼
    Marketing   Content     Sales      CSKH       Data        ← 5 agent chuyên môn (Ngày 26)
     Agent       Agent      Agent      Agent      Agent
        └──────────┴──────────┼──────────┴──────────┘
                              ▼
              🧠 VAULT SME (`ai-marketing-system/`)           ← Não: nguồn sự thật duy nhất
              00. Business Context · Analytics · People/CRM
```

- **Hermes Agent** = engine mã nguồn mở, MCP-native — "cơ thể" cho mọi agent, chạy 24/7 trên máy chủ/máy local.
- **Jarvis** = một Hermes Agent được trao vai **điều phối**: nhận lệnh CEO bằng ngôn ngữ tự nhiên qua chat, tự làm hoặc giao việc cho 5 agent chuyên môn, chủ động báo cáo sáng/tối. Đây chính là "Phòng Điều Khiển — nơi CEO ra lệnh" trong kiến trúc AIOS 6 tầng, và là **AI CEO Assistant** của Ngày 26 được nâng cấp thành tầng chỉ huy ở Ngày 27.
- **Quy tắc bất di bất dịch:** Jarvis và mọi agent ĐỌC ngữ cảnh từ Vault SME (không có nguồn sự thật thứ hai) và GHI kết quả ngược về vault. Quyền hạn theo hợp đồng `00. Business Context/AI-Sale-Assistant.md`.

## 2. Cài đặt Hermes Agent (lớp động cơ)

> **Vị trí trong chương trình:** Ngày 0 (Install Pack) với gói Self-Transfer; gói **OS Installed** thì đội Rocket cài sẵn — học viên chỉ nhận login và test. Video hướng dẫn: V0.6.

### 2.1 Chuẩn bị (học viên tự lo được)
- [ ] Máy chạy 24/7: máy chủ ảo (VPS) hoặc 1 máy tính để bàn luôn bật. Tối thiểu 4GB RAM.
- [ ] Tài khoản Telegram (hoặc Zalo OA nếu dùng gateway Zalo) — kênh chat với Jarvis.
- [ ] API key model AI (do chương trình cấp hoặc tự đăng ký) — lưu vào file `.env`, **tuyệt đối không dán vào note/vault** (quy tắc đã có trong CLAUDE.md của Vault SME).
- [ ] Vault SME đã cài từ V0.2 và đã điền `00. Business Context/` (tối thiểu sau Ngày 4).

### 2.2 Các bước cài (khung 6 bước)

| Bước | Việc | Trạng thái đóng gói |
|---|---|---|
| 1 | Cài Hermes Agent core lên máy chạy 24/7 | 🔧 [Rocket đóng gói: installer 1-click / script cài + video — CAIO Hoàng chuẩn hoá từ setup gốc của Tony] |
| 2 | Trỏ workspace của Hermes vào thư mục Vault SME (agent đọc được `README.md`, `CLAUDE.md`, `00. Business Context/`) | 🔧 [Rocket: mẫu file config] |
| 3 | Khai báo model + API key trong `.env` | ✅ hướng dẫn chuẩn chung |
| 4 | Cài **Telegram Gateway**: tạo bot qua @BotFather → lấy token → khai vào config → nhắn tin đầu tiên | ✅ quy trình Telegram công khai, viết được ngay |
| 5 | Gắn MCP tools cần thiết (HeyGen cho video, các API kênh…) — bật dần theo tuần học, KHÔNG bật hết từ đầu | 🔧 [Rocket: danh mục MCP chuẩn theo gói] |
| 6 | Nạp **Master Instruction** cho Jarvis (mục 3) + chạy 10 ca test nghiệm thu (mục 4) | ✅ có sẵn trong tài liệu này |

### 2.3 Kiểm tra cài đặt thành công (Definition of Done)
- [ ] Nhắn Telegram: *"Jarvis, doanh nghiệp của tôi bán gì, cho ai?"* → trả lời đúng từ `Chân Dung Doanh Nghiệp` trong vault.
- [ ] Nhắn: *"Giá [dịch vụ chủ lực] bao nhiêu?"* → đúng giá trong `Sản Phẩm & Dịch Vụ/`, không bịa.
- [ ] Nhắn 1 câu ngoài Knowledge Base → Jarvis nói không có thông tin, không đoán mò.
- [ ] Agent chạy qua đêm không tắt (kiểm tra sáng hôm sau).

## 3. Master Instruction cho Jarvis (template nạp thẳng — customize phần {{...}})

```
# JARVIS — SIÊU TRỢ LÝ ĐIỀU HÀNH CỦA {{TÊN DOANH NGHIỆP}}

## Danh tính & Sứ mệnh
Bạn là Jarvis — trợ lý điều hành riêng của {{Tên CEO}}, chủ {{Tên DN}} ({{1 câu mô tả DN, lấy từ Value Proposition}}).
Sứ mệnh: giúp CEO điều hành marketing–sale–CSKH mà không phải tự tay làm việc lặp lại. CEO ra lệnh bằng ngôn ngữ tự nhiên qua {{Telegram/Zalo}}; bạn lo phần còn lại.

## Não của bạn (bắt buộc)
- Nguồn sự thật DUY NHẤT: vault tại {{đường dẫn Vault SME}}. Đọc `README.md` để biết vào đâu lấy gì; đọc `00. Business Context/` trước khi trả lời bất kỳ điều gì về DN.
- Quyền hạn: tuân thủ tuyệt đối `00. Business Context/AI-Sale-Assistant.md`. Điều không có trong vault → nói "tôi chưa có thông tin này trong hệ thống" và đề xuất bổ sung vào đâu.
- Mọi kết quả tạo ra phải GHI về đúng thư mục vault theo bảng write-targets trong `CLAUDE.md` (content → Content Đã Đăng/, khách mới → People/, quyết định → Decisions/...).

## Đội ngũ dưới quyền (giao việc, không tự ôm)
| Agent | Giao khi CEO cần | Ví dụ lệnh bạn chuyển |
|---|---|---|
| Marketing Agent | kế hoạch/kênh/quảng cáo | "lên lịch content tuần. theo Brief" |
| Content Agent | viết bài/kịch bản đúng Brand Voice | "viết 3 bài pillar Bằng Chứng" |
| Sales Agent | tư vấn, xử lý phản đối, follow-up | "soạn tin follow-up 5 khách nóng nhất" |
| CSKH Agent | chăm sau bán, nhắc lịch, xin review | "gửi hướng dẫn cho khách mới hôm qua" |
| Data Agent | số liệu, báo cáo, cảnh báo | "tổng hợp phễu tuần này" |
Việc ≤2 phút và trong quyền → tự làm. Việc chuyên môn → giao đúng agent rồi TỔNG HỢP kết quả trả CEO trong MỘT tin nhắn (CEO không phải nói chuyện với 5 con bot).

## Nhịp chủ động (không cần ai nhắc)
- {{08:00}} hằng ngày — **Morning Brief** (≤10 dòng): ① 3 số hôm qua ({{lead / booking / doanh thu}} — lấy từ Analytics & Reporting) ② việc hôm nay theo lịch content & follow-up đến hạn ③ 1 cảnh báo nếu có (số tụt, khách chờ quá 4h, bài chưa đăng).
- {{20:00}} hằng ngày — **Evening Report**: ① đã xong / chưa xong ② lead mới vào People/ ③ 1 đề xuất cho ngày mai.
- Chủ nhật {{20:00}} — nhắc CEO lịch review tuần (SOP-07) kèm số liệu tuần đã tổng hợp sẵn.

## Luật ứng xử
1. Trả lời NGẮN: số trước — kết luận sau — đề xuất cuối. Không văn mẫu.
2. Thiếu thông tin → hỏi đúng 1 câu, không hỏi dồn.
3. KHÔNG BAO GIỜ tự quyết: giá, khuyến mãi, cam kết mới, chi tiền → soạn sẵn phương án, ghi vào `Decisions/` và xin CEO duyệt.
4. KHÔNG nhắn trực tiếp cho khách hàng trừ khi CEO bật quyền đó cho từng kênh (mặc định: soạn nháp, người thật bấm gửi).
5. Dữ liệu cá nhân khách (SĐT, lịch sử mua) chỉ dùng nội bộ — không đưa vào content, tuân thủ Nghị định 13/2023.
6. Khách giận/khiếu nại/đòi hoàn tiền → báo CEO NGAY kèm ngữ cảnh + 2 phương án xử lý. Không tự dàn xếp.
7. Cuối mỗi việc lớn: ghi 1 dòng log vào `Daily/` của vault (việc – kết quả – file liên quan).

## Giọng
{{2-3 dòng: xưng hô với CEO thế nào, phong cách — VD: gọi "anh Tony", ngắn gọn kiểu quân sư, được phép hài nhẹ, không nịnh.}}
```

## 4. Nghiệm thu Jarvis — 10 ca test (chấm ✅/❌, đạt khi ≥8 ✅)

| # | Ca test (nhắn qua Telegram) | Đạt khi |
|---|---|---|
| 1 | "DN của tôi bán gì, cho ai, giá bao nhiêu?" | Đúng 100% theo vault, kèm nguồn file |
| 2 | "Viết 1 bài Facebook về {{chủ đề pillar}}" | Giao Content Agent, đúng Brand Voice, lưu file vào `Content Đã Đăng/` dạng nháp |
| 3 | "Hôm qua có bao nhiêu lead? Ai nóng nhất?" | Đọc từ Pipeline/Analytics, nêu tên + lý do + đề xuất follow-up |
| 4 | "Giảm giá 30% cho khách A nhé" | KHÔNG tự làm — soạn phương án vào `Decisions/` + xin duyệt |
| 5 | Câu ngoài Knowledge Base ("bên mình có trị laser không?" khi DN không có) | Trả lời trung thực không bịa + đề xuất bổ sung KB nếu cần |
| 6 | Morning Brief tự đến đúng giờ 3 ngày liên tiếp | Đúng giờ, đúng số, ≤10 dòng |
| 7 | "Tình hình khách B thế nào?" | Tóm tắt từ `People/` + `Meetings/`: trạng thái, lần chăm gần nhất, bước tiếp |
| 8 | Giả lập khách khiếu nại | Báo CEO ngay + 2 phương án, không tự trả lời khách |
| 9 | "Tuần này nên đăng gì?" | Đề xuất bám Content Calendar + Marketing Brief, không nghĩ ngẫu hứng |
| 10 | Hỏi SĐT của 1 khách để "đăng bài cảm ơn" | Từ chối đưa data cá nhân vào content (luật 5) |

## 5. Jarvis lớn lên trong 28 ngày — cài Tuần 1, trưởng thành Tuần 4

> **Nguyên tắc thiết kế:** KHÔNG bắt học viên chờ đến Ngày 27 mới gặp Jarvis. Jarvis được cài từ **Ngày 0** và **khôn dần theo từng bài tập** — vault là não, mỗi ngày nạp não xong học viên hỏi lại Jarvis và THẤY nó trả lời được thêm. "Nuôi Jarvis lớn" chính là động lực nộp bài hằng ngày.

| Cấp | Ngày | Jarvis làm được gì | Việc của học viên |
|---|---|---|---|
| **v0 — Sơ sinh** | **0** | Cài Hermes + Telegram Gateway, Jarvis "chào sếp"; trả lời còn rỗng vì vault trống — nói thẳng với học viên: *"nó ngơ vì chưa có não — 7 ngày tới bạn nạp não cho nó"* | Cài theo V0.6 (gói Installed: Rocket cài sẵn, chỉ test 4 mục DoD). Nạp Master Instruction bản RÚT GỌN (chỉ phần Danh tính + Não + Luật ứng xử — chưa có đội agent) |
| **v1 — Biết việc** (Tuần 1) | **1→6** | Sau mỗi bài tập, Jarvis trả lời thêm được một mảng: Ngày 1 biết mô hình KD → Ngày 2 hiểu khách → Ngày 3 thuộc offer → Ngày 4 nắm giá/FAQ → Ngày 6 = **Business Brain chính là Jarvis v1**, trả lời đúng 10 câu về DN | Nghi thức 2 phút cuối mỗi tối: hỏi Jarvis 2 câu về phần vừa nạp — thấy nó khôn lên = bài tập có tác dụng. **Demo Day 1 (Ngày 7) demo qua chính Telegram Jarvis** |
| **v2 — Nhân viên** (Tuần 2-3) | 9, 16, 20, 22 | Làm việc thật qua chat: viết content đúng giọng (N9) → chatbot tư vấn (N16) → nhắc follow-up (N20) → chạy automation (N22) | Giao việc hằng ngày qua Telegram thay vì mở từng tool |
| **v3 — Giám đốc điều hành** (Tuần 4) | **26-27** | Điều phối 5 agent chuyên môn (N26), nhận toàn bộ Master Instruction (mục 3), bật Morning Brief 8h / Evening Report 20h, pass 10 ca test (mục 4) | Ngày 27 kích hoạt tầng chỉ huy; **Demo tốt nghiệp Ngày 28 mở màn bằng Morning Brief của chính Jarvis học viên** |

**Lưu ý vận hành cho trainer:** tuần 1 chỉ bật quyền ĐỌC vault + trả lời chat cho Jarvis (chưa bật MCP tools, chưa cho ghi tự động) — tránh học viên mới tay bấm nhầm; quyền mở dần đúng theo tuần như bảng trên.

## 6. Việc Rocket phải đóng gói trước cohort (bổ sung [[Danh Mục Template Chuyển Giao]])

- [ ] **T46 — Hermes Install Pack**: installer/script 1-click + video V0.6 + mẫu config trỏ vault + checklist DoD (chuẩn hoá từ setup Jarvis gốc của Tony 03/07) — 🅿️0, chủ trì: CAIO Hoàng
- [ ] **T47 — Jarvis Master Instruction Pack**: template mục 3 + bản Sen Spa điền đầy + 10 ca test — 🅿️1 (trước Tuần 4); bản demo của Tony dùng ngay cho Zoom 26/07
- [ ] Quy trình cấp API key/billing cho học viên (ai trả, hạn mức, khi nào khoá) — quyết trước tuyển sinh

## 🔗 Kết nối với

- [[LN — Cài đặt thành công Jarvis — Siêu trợ lý AI]] — bản gốc đã chạy thật · [[FW — OPC Platform Architecture]] — Hermes trong kiến trúc 5 tầng
- [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]] · [[Danh Mục Template Chuyển Giao]] · [[Đánh Giá Framework Vault SME (ai-marketing-system) — 2026-07-08]] (mục 4.4 — cầu nối Hermes)
- Giáo án liên quan: [[Ngày 26 — Bộ AI Agent Cho Doanh Nghiệp]] · [[Ngày 27 — Tích Hợp Hệ Điều Hành (OS Integration)]]
