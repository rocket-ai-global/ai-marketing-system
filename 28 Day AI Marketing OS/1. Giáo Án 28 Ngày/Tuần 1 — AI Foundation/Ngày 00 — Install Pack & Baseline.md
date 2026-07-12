---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-12
tags: [project, aios, giao-an]
week: 1
day: 0
core-output: Obsidian + Vault SME mở được · tài khoản AI chạy lệnh đầu tiên · Baseline điền đủ 10 số
---

# 📦 Ngày 00 — Install Pack & Baseline

> Ngày TRƯỚC khai giảng — bạn tự làm ở nhà theo 6 video V0.1–V0.6 trong Install Pack (bộ cài đặt), gửi kèm thư mời nhập học ≥5 ngày trước Ngày 1. Không có buổi live. Mục đích: khi bước vào Ngày 1, **máy đã chạy, số đã đo** — cả cohort (khoá học theo nhóm) không mất phút nào cho chuyện cài đặt. Thông số chuẩn theo [[_Chuẩn Đồng Bộ Tuần 1]].

## 1. 🎯 Mục Tiêu (Core Output)

Hoàn thành đủ 3 điều kiện — đây chính là "vé vào cửa" Ngày 1:

- ✅ **Obsidian + Vault SME mở được** — thấy cây thư mục, mở được `README.md`.
- ✅ **Tài khoản AI chạy được lệnh đầu tiên** — agent đọc vault và trả lời được "vault này là gì".
- ✅ **`Baseline & Mục Tiêu 28 Ngày.md` điền đủ 10 số** + 1 mục tiêu chính + 3 chỉ số. *Không có số này, Ngày 28 không chứng minh được gì.*

**Bonus (không bắt buộc, không trừ điểm):** Track C — Hermes/Jarvis test xong 4 mục Definition of Done (định nghĩa hoàn thành).

## 2. 📚 Kiến Thức Trọng Tâm

### 2.1 Kiến trúc 2 lớp — slide duy nhất bạn cần nhớ hôm nay

```
🧠 VAULT SME (Obsidian)          = NÃO — doanh nghiệp bạn BIẾT GÌ
        │  agent đọc não, không có nguồn sự thật thứ hai
        ▼
⚙️ ROCKETAGENT / HERMES          = ĐỘNG CƠ — AI HÀNH ĐỘNG thế nào
   (Assistant, chatbot, Jarvis)
```

> **Business Brain (bộ não kinh doanh) = KB trong Vault SME (não — biết gì) + Master Instruction (luật — hành xử thế nào), vận hành trên lớp động cơ.**

28 ngày tới bạn làm đúng 2 việc lặp lại: **nạp não** (điền vault) và **lắp động cơ** (dựng agent đọc vault). Vault trống thì agent "ngơ" — đó là lý do mọi bài tập Tuần 1 đều là nạp não.

### 2.2 Bạn thuộc track (nhánh công cụ) nào?

| Track | Dành cho | Lớp động cơ ⚙️ |
|---|---|---|
| **A — RocketAgent** (mặc định) | Mọi học viên được cấp tài khoản | Assistant trên RocketAgent, KB nạp từ vault |
| **B — Claude/ChatGPT Projects** | Chưa có tài khoản RocketAgent | Project + upload 3 tài liệu lõi |
| **C — Hermes/Jarvis qua Telegram** | Gói OS Installed (Rocket cài sẵn) hoặc Bonus | Theo [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]] |

Bạn chỉ làm **một** track — không phải cả 3. Ngày 0 mọi track đều làm Bước 1–5; riêng Track C làm thêm Bước 6.

### 2.3 Nhịp học 1 ngày (từ Ngày 1 trở đi)

Live 19h30 (dạy tư duy + chữa bài) → làm bài ≤2h theo đường template → **nộp thread cohort trước 23h59** → AI Grader (AI chấm bài) chấm trong 1h sáng hôm sau → office hours (giờ hỗ trợ trực tiếp) buổi trưa. Tên file nộp: `[Tên DN] — Ngày XX — [Tên tài sản]`. Video V-số là "mentor thao tác" cho khung giờ 21h–23h khi không hỏi được ai.

## 3. ✅ Checklist Thực Thi Từng Bước

> Làm trên **máy tính** (không làm trên điện thoại). Mỗi bước bám 1 video — mở video, xem đến đâu làm đến đó. ⏱ ghi 2 số: *theo video* / *lần đầu tự mò*.

**Bước 1 — Xem "Đây là hệ thống bạn sẽ có sau 28 ngày" (V0.1)** — ⏱ 10' / 10'
- [ ] Xem tour vault MSX demo (`ai-marketing-system-msx-demo/` — case thật: Mẫu Sơn Xanh, dược liệu Lạng Sơn) đã vận hành đầy đủ: Business Context, 30 bài content, pipeline lead, agent trả lời "khách chê giá thì nói sao?" đúng từ vault.
- [ ] Ghi nhớ 1 câu: *"28 ngày tới, mỗi ngày tôi lắp 1 mảnh của cái này cho DN mình."*

**Bước 2 — Cài Obsidian + mở Vault SME (V0.2)** — ⏱ 10' / 20'
- [ ] Tải Obsidian (Mac/Windows theo đúng hệ máy) → cài đặt.
- [ ] Giải nén vault bàn giao → **Open folder as vault** → chọn ĐÚNG thư mục `ai-marketing-system` (không chọn thư mục cha).
- [ ] Bấm "Trust author & enable plugins" (tin tưởng plugin) khi Obsidian hỏi.
- [ ] Kiểm tra: mở được `README.md`, thấy đủ cây thư mục `00. Business Context/` → `05. Archive/`.

**Bước 3 — Tài khoản AI + lệnh đầu tiên (V0.3)** — ⏱ 15' / 30'
- [ ] Cài Claude Code (hoặc app Claude) → đăng nhập bằng tài khoản được cấp.
- [ ] Mở terminal (cửa sổ dòng lệnh) NGAY TRONG thư mục vault.
- [ ] Gõ lệnh đầu tiên: *"đọc README và nói vault này là gì"*.
- [ ] Thấy agent trả lời đúng nội dung vault = cài thành công. **Chụp màn hình lại** — đây là bằng chứng nộp bài.

**Bước 4 — Tour cấu trúc Vault SME: não nằm ở đâu (V0.4)** — ⏱ 15' / 20'
- [ ] Đi theo 3 lớp dữ liệu trong vault của mình, đối chiếu bản MSX demo: ① `00. Business Context/` — nguồn sự thật, "hộ khẩu doanh nghiệp" ② PARA `01 → 05` — dòng công việc ③ Entity `People/ Companies/ Meetings/ Decisions/` + `Nhật Ký CEO/` — ai, cái gì, quyết định nào.
- [ ] Thuộc 2 quy tắc vàng: **1 vault = 1 công ty duy nhất** · **không note mồ côi** (note nào cũng phải link ra ngoài).

**Bước 5 — Điền Baseline & Mục Tiêu 28 Ngày (V0.5)** — ⏱ 30' / 60'
- [ ] Mở `00. Business Context/Baseline & Mục Tiêu 28 Ngày.md` trong vault.
- [ ] Điền đủ **10 số đo gốc** (mỗi số: giá trị / nguồn lấy / ngày đo) — xem bản mẫu MSX trong video để biết "điền đúng trông như thế nào".
- [ ] Không có số chính xác → điền **ước lượng tốt nhất** + ghi nguồn "ước lượng", KHÔNG để trống.
- [ ] Viết 1 mục tiêu chính + 3 chỉ số (hiện tại → mục tiêu → cách đo). Ô "Ngày 28 đo lại" để trống.

**Bước 6 — Track C: Hermes Agent + Jarvis "chào sếp" (V0.6)** — ⏱ 15' (gói OS Installed — chỉ test) / 60–90' (tự cài)
- [ ] Gói OS Installed: Rocket đã cài sẵn — bạn chỉ xem video để hiểu + chạy 4 mục Definition of Done: hỏi *"Jarvis, doanh nghiệp của tôi bán gì, cho ai?"* qua Telegram · hỏi giá dịch vụ chủ lực · hỏi 1 câu ngoài KB (phải từ chối, không bịa) · sáng hôm sau kiểm tra agent còn chạy.
- [ ] Tự cài: theo đúng 6 bước trong [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]] — nạp Master Instruction bản RÚT GỌN (Danh tính + Não + Luật ứng xử). Jarvis lúc này còn "ngơ" vì vault trống — **7 ngày tới bạn nạp não cho nó.**

**⏱ Tổng:** Track A/B ~80' theo video · lần đầu tự mò có thể tới 2h20 — quá giờ: ưu tiên Bước 2 → 3 → 5 (3 điều kiện vào Ngày 1), Bước 1 và 4 xem bù sau. Track C cộng thêm theo gói.

## 4. 📤 Deliverable & Cách Xác Nhận Hoàn Thành

Nộp vào thread (luồng bài nộp) cohort: `[Tên DN] — Ngày 00 — Install Pack & Baseline`, gồm **3 bằng chứng**:

| # | Bằng chứng | Xác nhận điều kiện |
|---|---|---|
| 1 | Ảnh màn hình Obsidian mở Vault SME (thấy cây thư mục + `README.md`) | Obsidian + Vault SME mở được |
| 2 | Ảnh agent trả lời lệnh đầu tiên | Tài khoản AI chạy được |
| 3 | Ảnh/file `Baseline & Mục Tiêu 28 Ngày.md` đã điền đủ 10 số + mục tiêu | Baseline hoàn thành |

Track C (gói OS Installed) thêm: ảnh Jarvis trả lời trên Telegram (4 mục Definition of Done).

**Điều kiện vào Ngày 1:** đủ 3 bằng chứng, nộp **trước ngày khai giảng ≥1 ngày**. Chưa đủ → chưa vào Ngày 1; nhắn thread #setup-support để được kèm 1:1 — kẹt cài đặt là chuyện bình thường, giấu kẹt mới là vấn đề.

## 5. 📖 GLOSSARY — Bảng Thuật Ngữ Toàn Chương Trình

> Gặp từ lạ ở bất kỳ ngày nào — quay về bảng này. Quy tắc chung: thuật ngữ tiếng Anh luôn kèm nghĩa tiếng Việt trong ngoặc ở lần dùng đầu trong mỗi tài liệu.

| Thuật ngữ | Nghĩa dễ hiểu |
|---|---|
| **ICE** | Impact·Confidence·Ease (tác động · độ tự tin · độ dễ) — thang chấm điểm để xếp hạng Top 10 cơ hội AI ở Ngày 1: việc nào vừa lợi vừa dễ thì làm trước. |
| **LTV** | Lifetime Value (giá trị vòng đời khách hàng) — tổng số tiền một khách mang lại trong suốt thời gian họ còn mua của bạn. |
| **CRM** | Customer Relationship Management (quản lý quan hệ khách hàng) — hệ thống lưu thông tin và lịch sử từng khách để chăm đúng người, đúng lúc. |
| **SOP** | Standard Operating Procedure (quy trình vận hành chuẩn) — tài liệu từng bước để ai làm theo cũng ra cùng một kết quả. |
| **PDFO** | Pain·Desire·Fear·Objection (nỗi đau · mong muốn · nỗi sợ · lời phản đối) — 4 nhóm insight khách hàng bạn lập bản đồ ở Ngày 2. |
| **BMC** | Business Model Canvas (mô hình kinh doanh 9 khối) — bức tranh 1 trang về cách doanh nghiệp tạo ra, trao và thu về giá trị; dựng ở Ngày 1. |
| **KB** | Knowledge Base (kho tri thức) — toàn bộ dữ liệu doanh nghiệp đã sắp xếp để AI đọc hiểu được; xây ở Ngày 4, nằm trong Vault SME. |
| **Cohort** | Khoá học theo nhóm — cả lớp cùng vào cùng ra, học cùng nhịp 28 ngày, chấm chéo và demo cho nhau xem. |
| **Thread** | Luồng trò chuyện theo chủ đề trong group lớp — mỗi ngày có 1 thread riêng để nộp bài trước 23h59. |
| **Demo Day** | Ngày trình diễn nghiệm thu — bạn chạy THẬT hệ thống trước cả lớp (Ngày 7, 14, 21, 28); không phải thi, là nghiệm thu + học chéo. |
| **RocketAgent** | Nền tảng AI Agent của Rocket — lớp động cơ ⚙️ mặc định (Track A): nơi bạn dựng Assistant và nạp KB từ vault. |
| **Hermes** | Engine (động cơ phần mềm) agent mã nguồn mở chạy 24/7 trên máy của bạn — "cơ thể" cho mọi agent ở Track C. |
| **Jarvis** | Siêu trợ lý điều hành — một Hermes Agent được trao vai điều phối: nhận lệnh của bạn qua Telegram, cài từ Ngày 0 và "khôn dần" theo từng bài tập. |
| **AI Grader** | AI chấm bài — chấm bài nộp trong 1h sáng hôm sau theo rubric (thang chấm điểm) 100đ; bài 🔧/🔴 có mentor chấm sâu thêm. |
| **Elite Builders** | Cộng đồng doanh nhân – nhà xây dựng hệ thống AI của Rocket — nơi cohort sinh hoạt, chia sẻ case và nhận quyền lợi chương trình. |
| **Vault SME** | "Két tri thức" doanh nghiệp — thư mục Obsidian `ai-marketing-system/` chứa toàn bộ não 🧠 của DN bạn; nguồn sự thật duy nhất cho mọi agent. |
| **Track A/B/C** | 3 nhánh công cụ lớp động cơ: A = RocketAgent (mặc định) · B = Claude/ChatGPT Projects · C = Hermes/Jarvis qua Telegram. Mỗi người chỉ theo 1 nhánh. |

## 6. ⚠️ FAQ & Lỗi Cài Đặt Thường Gặp

| Triệu chứng | Nguyên nhân | Cách sửa |
|---|---|---|
| Mở vault thấy toàn thư mục lạ, không thấy `README.md` | **Mở nhầm thư mục cha** khi "Open folder as vault" | Đóng vault → Open folder as vault lại → chọn đúng thư mục `ai-marketing-system` |
| Ghi chú hiện ô vuông, tiếng Việt vỡ chữ | Font mặc định thiếu glyph tiếng Việt | Settings → Appearance → đổi Font (video V0.2 chỉ đúng chỗ bấm) |
| Dataview/template không chạy, vault "trông trống trơn" | Chưa bấm "Trust author & enable plugins" khi mở vault | Settings → Community plugins → bật lại toàn bộ plugin đi kèm vault |
| Agent báo lỗi xác thực / bắt đăng nhập mãi | **Chưa đăng nhập** đúng tài khoản được cấp | Đăng xuất → đăng nhập lại bằng đúng email trong thư mời; vẫn kẹt → thread #setup-support |
| Agent nói "không tìm thấy README" | Terminal đang đứng **sai thư mục** (không phải thư mục vault) | Mở terminal ngay trong thư mục vault (V0.3 có thao tác cho cả Mac & Windows) |
| Cài được nhưng không kết nối, chỉ quay vòng | **Mạng công ty chặn** dịch vụ AI | Thử phát 4G từ điện thoại hoặc mạng khác; nếu do firewall công ty → nhờ IT mở |
| "Tôi không rành kỹ thuật, sợ làm hỏng" | — | Gói OS Installed: Rocket cài sẵn toàn bộ. Track B chỉ cần trình duyệt. Không ai bị bỏ lại vì cài đặt. |
| "Tôi không có số chính xác để điền Baseline" | Chưa từng đo | Điền ước lượng tốt nhất + ghi nguồn "ước lượng" — số gần đúng vẫn hơn ô trống; Ngày 28 đo lại cùng một cách. |
| Jarvis (Track C) trả lời ngô nghê, lạc đề | Vault còn trống — não chưa được nạp | Bình thường ở Ngày 0. Sau mỗi bài tập Tuần 1, hỏi lại Jarvis 2 câu — nó sẽ khôn dần lên. |

## 7. 🔗 Kết Nối

- **Ngày tiếp theo:** [[Ngày 01 — Phân Tích Doanh Nghiệp & Cơ Hội AI]] — mang theo Baseline đã điền; mục tiêu 28 ngày ở Ngày 1 sẽ đối chiếu thẳng với 10 số này.
- Chuẩn thông số: [[_Chuẩn Đồng Bộ Tuần 1]] · Video hướng dẫn: [[_Kế Hoạch Video Tuần 1 — Hướng Dẫn Học Viên]] (V0.1–V0.6)
- Track C: [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]] · Bản đồ thao tác: [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]]
- File Baseline được dùng lại ở: Ngày 1 (mục tiêu), Ngày 7 (Foundation Gate câu 5), Ngày 28 (đo lại & chứng minh kết quả).
