---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, video, production]
week: 1
---

# 🎬 Kế Hoạch Video Tuần 1 — Hướng Dẫn Học Viên

> Danh mục video Tony/đội ngũ phải sản xuất để học viên đạt mục tiêu Tuần 1. Nguyên tắc phân vai: **buổi live dạy TƯ DUY + chữa bài — video dạy THAO TÁC từng bước**. Học viên làm bài lúc 21h-23h đêm không thể hỏi ai: video chính là "mentor thao tác" thay thế, xem đến đâu làm đến đó.

**Mục đích Tuần 1 — hiểu sâu & kiểm chứng, không phải "làm đủ bài":** hiểu sâu doanh nghiệp và mô hình kinh doanh (BMC), nắm chân dung khách hàng tiềm năng bằng insight THẬT, và **kiểm chứng offer đã phù hợp chưa** (Foundation Gate 5 câu — Ngày 07). Có đủ nền này thì các module sau mới hiệu quả: content Tuần 2 viết đúng insight, chatbot Tuần 3 tư vấn đúng khách. Mọi video dưới đây phục vụ mục đích đó.

**Tài sản phải cầm về:** BMC 9 khối + Business Snapshot → Chân dung khách + PDFO + Journey → Offer + Sales Message Pack → Knowledge Base 10 thư mục đã nạp RocketAgent → Prompt Library ≥50 (≥20 cá nhân hoá) → AI Business Brain v1 + 2 Assistant → Demo 5-7' + Foundation Scorecard + **Foundation Gate 5/5**.

---

## 0. Nguyên tắc sản xuất (đọc trước khi quay)

1. **1 video = 1 thao tác trọn vẹn**, ≤15 phút. Học viên tua lại được, không phải xem 1 tiếng tìm 1 bước.
2. **Quay trên vault demo 🍵 MSX đã điền đầy** (`ai-marketing-system-msx-demo/` — case thật: Mẫu Sơn Xanh, dược liệu Lạng Sơn) — vault này **đã build sẵn**, không còn dependency chặn. Học viên thấy "kết quả trông như thế nào" bằng dữ liệu thật, không phải placeholder. 🚀 RocketAI chỉ mở ra khi cần đối chiếu B2B (theo mapping [[_Chuẩn Đồng Bộ Tuần 1]]).
3. **Cấu trúc chuẩn mỗi video (4 phần):**
   - 0:00–0:30 — *Kết quả cuối*: chiếu ngay cái sẽ có sau video ("xem này, xong video bạn có file BMC như này")
   - 0:30–x — *Từng bước*: thao tác chậm, đọc to lệnh gõ, zoom chỗ click
   - x–x+2' — *3 lỗi thường gặp* của bước này + cách nhận ra & sửa (lấy từ mục 11 giáo án)
   - Cuối — *Checklist 30 giây*: "trước khi tắt video, bạn phải có: ✅…✅…" (khớp rubric chấm điểm)
4. **Quay 1 lần, dùng mọi cohort** — không nói ngày tháng/cohort cụ thể trong video; các thứ hay đổi (link nộp bài, lịch) để trong tin nhắn cohort, không nói trong video.
5. **Kỹ thuật:** screencast OBS/Loom 1080p · mic rõ tiếng · caption tiếng Việt (học viên xem đêm không bật loa) · chapter timestamps trong mô tả · đặt tên file `V[ngày].[thứ tự] — [Tên]`.
6. **Video ≠ giáo án đọc lại.** Không giảng lý thuyết trong video (đã có live) — vào thẳng thao tác.

---

## 1. Danh mục video (19 video · ~3h tổng)

### 📦 Ngày 0 — Install Pack (gửi trước khai giảng ≥5 ngày, xem bắt buộc)

| Mã | Video | Dài | Phục vụ |
|---|---|---|---|
| V0.1 | **Đây là hệ thống bạn sẽ có sau 28 ngày** — tour vault MSX hoàn chỉnh | 10' | Động lực + hình dung đích |
| V0.2 | Cài Obsidian + mở Vault SME (Mac & Windows) | 8' | Điều kiện vào Ngày 1 |
| V0.3 | Cài Claude Code + đăng nhập + chạy lệnh đầu tiên trong vault | 10' | Điều kiện vào Ngày 1 |
| V0.4 | Tour cấu trúc Vault SME: não của doanh nghiệp nằm ở đâu | 10' | Nền cho mọi ngày |
| V0.5 | Cách học – cách nộp bài – điền Baseline & Mục Tiêu 28 Ngày | 7' | Baseline (điều kiện có case study) |
| V0.6 | Cài Hermes Agent + Telegram Gateway — "Jarvis chào sếp" | 12' | Lớp động cơ sẵn sàng (gói Installed: Rocket cài sẵn, học viên chỉ xem để hiểu + test) |

**Outline chi tiết:**
- **V0.1:** Mở vault MSX đã vận hành (`ai-marketing-system-msx-demo/`) → lướt `00. Business Context/` (BMC Mẫu Sơn Xanh, Brand Voice, 6 sản phẩm) → mở `Content Đã Đăng/` xem 30 bài → mở `MOC Sales Pipeline` xem lead đang chảy → hỏi agent 3 câu ("khách chê trà này đắt hơn trà ngoài chợ thì trả lời sao?") agent trả lời đúng từ vault → chốt: "28 ngày tới, mỗi ngày bạn lắp 1 mảnh của cái này cho DN mình". **Kiến trúc 2 lớp: vault = não 🧠, RocketAgent/Hermes = động cơ ⚙️** — vẽ 1 slide duy nhất.
- **V0.2:** Tải Obsidian → giải nén vault bàn giao → Open folder as vault → tin tưởng plugin → kiểm tra: mở được `README.md`, thấy cây thư mục. Lỗi hay gặp: mở nhầm thư mục cha, font tiếng Việt.
- **V0.3:** Cài Claude Code (hoặc app Claude) → đăng nhập tài khoản được cấp → mở terminal trong thư mục vault → gõ thử "đọc README và nói vault này là gì" → thấy agent trả lời = cài thành công. Lỗi: chưa đăng nhập, mở sai thư mục, mạng công ty chặn.
- **V0.4:** Đi theo 3 lớp dữ liệu: `00. Business Context/` (nguồn sự thật — "hộ khẩu doanh nghiệp") → PARA `01→05` (dòng công việc) → Entity `People/Companies/Meetings/Decisions` (ai-cái gì-quyết định nào) + `Nhật Ký CEO/` (chất liệu content có hồn). Nêu 2 quy tắc vàng: 1 vault = 1 công ty duy nhất · không note mồ côi.
- **V0.5:** Nhịp 1 ngày (live 19h30 → làm bài ≤2h → nộp trước 23h59 → AI Grader chấm sáng → office hours trưa) → format tên bài nộp → demo điền `Baseline & Mục Tiêu 28 Ngày.md` bằng bản mẫu MSX trong vault demo (lead/tháng 85, tỷ lệ chốt 22%, doanh thu 95tr, giờ marketing thủ công 12h/tuần) — nói rõ đây là **số demo minh hoạ**, và nhấn: *không có số này thì Ngày 28 không chứng minh được gì*.
- **V0.6:** Theo 6 bước của [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]]: cài Hermes core lên máy chạy 24/7 → trỏ workspace vào Vault SME → khai API key vào `.env` (cấm dán key vào note) → tạo bot Telegram qua @BotFather, nối gateway → nhắn câu đầu tiên "Jarvis, doanh nghiệp của tôi bán gì?" và thấy nó trả lời từ vault → chạy 4 mục Definition of Done. Kết video bằng cảnh Jarvis của Tony gửi Morning Brief thật — "cuối chương trình, cái này là của bạn".

### 🧩 Ngày 1 — Business Model Canvas & Cơ Hội AI

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V1.1 | **Chạy `/mo-hinh-kinh-doanh` từ A-Z** (demo 🍵 MSX full) | 15' | BMC 9 khối + Business Snapshot |
| V1.2 | Duyệt & sửa kết quả AI sinh + chốt Top 10 cơ hội AI | 8' | Process Map + Top 10 Use Cases + Mục tiêu 28 ngày |

- **V1.1:** Gõ `/mo-hinh-kinh-doanh` → trả lời phỏng vấn 9 khối bằng dữ liệu MSX (đọc to cách trả lời NGẮN mà đủ; demo cả tình huống "không biết trả lời — nói 'bạn hỏi tôi đi'") → xem file tự sinh: `Chân Dung Doanh Nghiệp`, `Business Model Canvas` + mở `.canvas` bản vẽ, từng file PK/GT trong `MHKD/` → đối chiếu với bản hoàn chỉnh sẵn có trong vault demo + checklist rubric. **Chèn 60 giây đối chiếu 🚀 RocketAI:** cùng 9 khối nhưng B2B khác B2C ở Revenue Streams (gói dịch vụ 12-50tr thay vì bán lẻ 520k) và Channels (cộng đồng/referral thay vì TikTok/ads) — nhắc học viên: copy KHUNG, không copy nội dung.
- **V1.2:** Đọc lại BMC bằng 3 câu hỏi duyệt (số đúng chưa? khối nào AI đoán mò? thiếu dòng doanh thu nào?) → sửa trực tiếp 1 khối sai làm mẫu → từ BMC rút Business Process Map (marketing→sale→CSKH hiện tại) → chấm Top 10 việc AI hoá theo 2 trục (tăng doanh thu × dễ làm) → viết Mục tiêu 28 ngày: 1 mục tiêu chính + 3 chỉ số.

### 🎯 Ngày 2 — Chân Dung Khách Hàng & Journey

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V2.1 | Đào sâu file PK: PDFO Map + Journey 7 giai đoạn (demo PK1 🍵 MSX — chị Hương) | 10' | Avatar + PDFO ≥5 mục/nhóm + Journey |
| V2.2 | Moi insight thật: đưa "câu nói vàng" của khách vào AI | 6' | Chất liệu PDFO không bịa |

- **V2.1:** Mở `MHKD/Phân Khúc Khách Hàng/PK1...md` (đã sinh từ Ngày 1) → dùng prompt trong giáo án đào PDFO (mỗi nhóm ≥5, mỗi mục 1 câu nói thật của khách) → vẽ Journey 7 giai đoạn ngay trong file PK → cách phát hiện avatar "là mọi người" (lỗi trừ điểm nặng nhất).
- **V2.2:** Lấy 3-5 tin nhắn khách thật (ẩn tên) → paste vào AI yêu cầu rút pain/fear/objection đúng NGÔN NGỮ khách → đối chiếu: cái AI đoán vs cái khách nói thật khác nhau thế nào → ghi ngược vào PK.

### 💎 Ngày 3 — Offer & Thông Điệp

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V3.1 | Chạy `/thiet-ke-offer`: 3 phương án → chọn → đóng gói đủ 7 khối | 12' | Core Offer Document |
| V3.2 | Sinh Sales Message Pack + phản biện bằng "khách đa nghi ảo" | 8' | Message Pack + offer đã vá lỗ hổng |

- **V3.1:** Ngày 3 là ngày **so offer B2C vs B2B** — chạy skill 2 lần. Lần 1 với offer 🍵 MSX (combo trà mua 3 tặng 1, ~1tr) → lần 2 với offer 🚀 RocketAI (gói OS Transfer 12tr) → nhận 3 phương án mỗi bên (an toàn/cân bằng/táo bạo) → khung quyết định "cam kết nào tôi gánh được vận hành" → đóng gói: tên offer, promise, 3 bonus (mỗi bonus trỏ 1 nỗi lo trong PDFO), cam kết đo được, lý do mua ngay THẬT → lưu vào `Sản Phẩm & Dịch Vụ/`. **Cảnh báo ngành sức khoẻ (bắt buộc, dùng chính MSX làm ví dụ):** dùng ngôn ngữ "hỗ trợ / đồng hành cùng thói quen" — KHÔNG hứa chữa bệnh, không hứa kết quả tuyệt đối.
- **V3.2:** Sinh pack (hook/headline/CTA/5 angle/10 ads) → lọc bỏ câu "không phải giọng mình" → chạy prompt khách-đa-nghi tấn công offer → sửa 2 điểm hở làm mẫu → lưu `04. Resources/Playbooks/`.

### 📚 Ngày 4 — Knowledge Base

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V4.1 | Chạy `/hoan-tat-business-context` — audit thiếu gì điền nấy | 8' | Brand Voice, Chân Dung CEO, AI-Sale-Assistant đủ |
| V4.2 | Đổ dữ liệu cũ vào đúng chỗ + nạp 3 tài liệu lõi lên RocketAgent | 10' | KB 10 thư mục + Security Rule + nạp RocketAgent |

- **V4.1:** Chạy skill → nó tự phát hiện file nào còn placeholder → trả lời phỏng vấn điền Brand Voice (từ nên/tránh dùng, câu mẫu) và Chân Dung CEO → xem file hoàn chỉnh.
- **V4.2:** Kéo-thả dữ liệu cũ: ảnh/bảng giá → `Sản Phẩm & Dịch Vụ/_Media/`, 30 cặp FAQ/Objection → `04. Resources/Playbooks/`, feedback khách → `Feedback & Chứng Thực/` → điền Data Access & Security Rule (cái gì AI KHÔNG được trả lời: giá vốn, data cá nhân khách — Nghị định 13) → thao tác nạp 3 tài liệu lõi lên RocketAgent (⚙️ lớp động cơ) và test hỏi 1 câu.

### 🤖 Ngày 5 — Prompt Library

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V5.1 | Nạp bộ 50 prompt + cá nhân hoá bằng khối [BỐI CẢNH DN] + [GIỌNG] | 10' | Library ≥50, ≥20 cá nhân hoá |
| V5.2 | Test prompt như tester: chấm Đạt/Chưa đạt + tinh chỉnh | 6' | 10 prompt đã test có ghi kết quả |

- **V5.1:** Copy bộ 50 prompt phát sẵn vào `04. Resources/Prompt Library/` → viết 1 lần 2 khối chuẩn: `[BỐI CẢNH DN]` (rút từ Business Snapshot) + `[GIỌNG]` (rút từ Brand Voice) → demo ghép khối vào 3 prompt marketing/sales/CSKH — "cá nhân hoá 20 prompt thực chất là dán 2 khối này".
- **V5.2:** Chạy 1 prompt → chấm bằng 3 câu (đúng yêu cầu? dùng được ngay? giống giọng mình?) → sửa constraint khi output sai → ghi kết quả 1 dòng vào file quản lý.

### 🧠 Ngày 6 — AI Business Brain

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V6.1 | Viết Master Instruction + dựng Brain trên RocketAgent | 12' | Business Brain v1 (KB + Instruction) |
| V6.2 | Tạo 2 Assistant (Sales + Marketing) + Test 6 tình huống | 10' | 2 Assistant + Test Case Report |

- **V6.1:** Điền `AI-Sale-Assistant.md` (AI là ai, được/không được làm gì, giọng, ưu tiên) → đưa lên RocketAgent làm Master Instruction ⚙️ → nguyên tắc "não chỉ biết cái trong KB": demo hỏi 1 câu ngoài KB để thấy nó từ chối đúng cách.
- **V6.2:** Tạo Assistant Sales + Marketing trỏ về cùng KB → chạy 6 tình huống test của giáo án (khách hỏi giá / so sánh / chê đắt / cần viết bài / phân tích / câu cấm) → ghi Test Case Report: cái nào sai → thiếu dữ liệu gì → bổ sung vào KB → test lại. "Vòng lặp sửa não" này là kỹ năng quan trọng nhất Ngày 6.

### 🏆 Ngày 7 — Demo Day 1

| Mã | Video | Dài | Phục vụ output |
|---|---|---|---|
| V7.1 | Cách demo 5-7' + xem 1 bài demo mẫu (🍵 MSX) đạt điểm ⭐ | 8' | Business Brain Demo |
| V7.2 | Tự chấm Foundation Scorecard + viết Marketing Brief cho Tuần 2 | 6' | Scorecard + Brief |

- **V7.1:** Format demo chuẩn: *Tôi đã xây gì (1') → chạy thử sống: hỏi Brain 3 câu khó nhất (3') → số liệu baseline & mục tiêu (1') → 1 điều kẹt nhất (1')* → chiếu nguyên 1 bài demo mẫu 6' trên vault MSX → 3 lỗi demo hay gặp (nói lý thuyết, không dám hỏi câu khó, quá giờ).
- **V7.2:** Mở Foundation Scorecard tự chấm từng mục → **chạy Foundation Gate 5 câu kiểm chứng độ khớp** (mô hình nhất quán? insight thật? OFFER PHÙ HỢP CHƯA? một nguồn sự thật? đo được?) — demo trên MSX cả tình huống fail câu 3 và cách sửa offer trước khi vào content → ghi kết quả vào `Đánh Giá Mô Hình Kinh Doanh` → điền Marketing Brief (chủ đề, sản phẩm đẩy, kênh ưu tiên, tệp ưu tiên) làm đầu vào Tuần 2.

---

## 2. Thứ tự sản xuất (theo dependency)

| Đợt | Quay | Deadline | Ghi chú |
|---|---|---|---|
| **Đợt 0 — điều kiện quay** | ✅ Vault demo 🍵 MSX **đã build sẵn** (`ai-marketing-system-msx-demo/`) — chỉ còn thiếu **bộ 50 prompt** + file **Baseline** trong vault gốc | trước khi quay bất kỳ video nào | Dependency cũ ("build Sen Spa trước") **đã gỡ bỏ** — vault MSX là bản thật, quay được ngay. Thiếu 50 prompt + Baseline thì V0.5 và V5.x vẫn phải chiếu placeholder |
| **Đợt 1** | V0.1 → V0.6 (Install Pack) | ≥5 ngày trước khai giảng | Gửi kèm thư mời nhập học; ai chưa cài xong không vào Ngày 1. V0.6 cần T46 (Hermes Install Pack) đóng gói xong trước |
| **Đợt 2** | V1.x, V3.x, V6.x | trước khai giảng | 3 ngày nặng thao tác nhất — rủi ro nghẽn support cao nhất |
| **Đợt 3** | V2.x, V4.x, V5.x, V7.x | trước Ngày 2 | Có thể quay trong tuần đầu cohort chạy nếu thiếu thời gian |

**Ước lượng công quay:** 18 video × (30' chuẩn bị + 2 lần quay + 30' hậu kỳ nhẹ) ≈ **3-4 ngày làm việc tập trung** cho người đã thuộc hệ thống. Có thể giao mentor quay Đợt 3 theo outline này — không nhất thiết Tony quay hết (giọng Tony giữ cho V0.1 + V7.1 là đủ "truyền lửa").

## 3. Checklist nghiệm thu mỗi video (trước khi phát hành)

- [ ] Mở đầu ≤30s đã chiếu kết quả cuối
- [ ] Mọi thao tác đều nhìn thấy trên màn hình (không nói suông "các bạn vào chỗ kia")
- [ ] Có đoạn "3 lỗi thường gặp" khớp mục FAQ/Lỗi của giáo án ngày đó
- [ ] Kết thúc bằng checklist khớp rubric chấm điểm (học viên biết mình "đạt" trông như thế nào)
- [ ] ≤15 phút · có caption · có chapter · tên file đúng `V[ngày].[thứ tự]`
- [ ] Không nhắc ngày tháng/cohort/link cụ thể (để dùng lại mọi cohort)

## 🔗 Kết nối với

- Giáo án tuần này: [[Ngày 01 — Phân Tích Doanh Nghiệp & Cơ Hội AI]] → [[Ngày 07 — Foundation Review & Demo Day 1]]
- [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]] (video bám đúng cột 🧠/⚙️ của từng ngày)
- [[Hệ Thống Chấm Chữa & Support Hàng Ngày]] (video là tầng support số 0 — trước cả mentor)
- [[Đánh Giá Framework Vault SME (ai-marketing-system) — 2026-07-08]] (Install Pack = việc 🔴 #1)
