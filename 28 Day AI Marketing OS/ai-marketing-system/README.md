# Vault SME — Bản Đồ Dữ Liệu Cho Agent

> Vault Obsidian PARA + AI Brain cho **DUY NHẤT 1 doanh nghiệp SME**. Mục tiêu: sắp xếp dữ liệu doanh nghiệp thành cấu trúc mà AI agent (Hermes agent, coding agent...) đọc hiểu ngay — phục vụ **sản xuất content đúng giọng thương hiệu** và **quản lý sale & marketing**.
>
> Agent đọc file này để biết **vào đâu lấy gì**. Chi tiết kiến trúc & nguyên tắc vận hành: [[Vault SME — Hướng Dẫn]]. Quy tắc bắt buộc khi làm việc: `CLAUDE.md`.

## 🚀 Bắt đầu từ đâu (dành cho người dùng mới)

> Vừa mở vault này lần đầu? Làm theo thứ tự dưới. Cách chạy: gõ **`/tên-skill`** trong Claude, hoặc chỉ cần nói việc muốn làm — Claude tự nhận skill. Nếu không biết trả lời, cứ nói "bạn hỏi tôi đi", Claude sẽ phỏng vấn từng câu.

**Bước 1 — Khai báo doanh nghiệp (làm TRƯỚC TIÊN, bắt buộc).** Mọi việc content/sale/marketing sau này đều đọc ngược về đây, nên phải điền `00. Business Context/` trước.
1. Gõ **`/mo-hinh-kinh-doanh`** → Claude phỏng vấn 9 ô mô hình kinh doanh, tự sinh `Chân Dung Doanh Nghiệp`, `Business Model Canvas` (+ sơ đồ `.canvas`), và các file phân khúc/giá trị trong `MHKD/`.
2. Gõ **`/hoan-tat-business-context`** → Claude quét xem còn thiếu gì (Brand Voice, Chân Dung CEO, AI-Sale-Assistant, Sản Phẩm & Dịch Vụ) và hỏi/phỏng vấn để điền nốt.
3. Nếu thương hiệu **gắn với cá nhân CEO** → điền `Chân Dung CEO — [Tên].md` và bắt đầu ghi `Nhật Ký CEO/` (chuyện thật, quan điểm) để Claude viết content đúng chất bạn.

**Bước 2 — Đổ dữ liệu đang có vào vault.** Ghi âm/note cũ → `01. Inbox/`; khách/deal đang có → `People/` + `Companies/`; sản phẩm/gói → `00. Business Context/Sản Phẩm & Dịch Vụ/` (hình/video để `_Media/[tên]/`).

**Bước 3 — Bắt đầu vận hành hằng ngày.**
- Viết content → lưu `03. Areas/Brand & Content/Content Đã Đăng/` (Claude lấy giọng từ `Brand Voice` + `Nhật Ký CEO/`).
- Cuối tuần ghi số liệu → `03. Areas/Analytics & Reporting/` (chọn đúng miền: tương tác / traffic / quảng cáo / hiệu suất content / CSKH chat).
- Khách khen/góp ý → `04. Resources/Feedback & Chứng Thực/`.

**Bước 4 — Đào sâu khi cần (sau khi Business Context đã đủ).** `/phan-tich-doi-thu` (đối thủ) · `/nghien-cuu-thi-truong` (validate ngách) · `/thiet-ke-offer` (đóng gói bán) · `/kiem-tra-seo` · `/do-luong-tracking` · `/thu-nghiem-ab`. Danh sách skill đầy đủ: `.claude/skills/README.md`.

> **Quy tắc vàng:** vault này chỉ cho **1 công ty**. Đừng tạo thư mục công ty con — mọi sản phẩm/phân khúc đều là file riêng trong cùng `00. Business Context/`. Không note mồ côi: note nào cũng link ra ngoài (xem mục 4).

## Tóm tắt 1 dòng cho agent

- **Lấy ngữ cảnh doanh nghiệp** → `00. Business Context/`
- **Hồ sơ + hình/video sản phẩm** → `00. Business Context/Sản Phẩm & Dịch Vụ/` (media ở `_Media/[tên]/`)
- **Lưu content mới tạo/đã đăng** → `03. Areas/Brand & Content/Content Đã Đăng/`
- **Lưu số liệu / báo cáo đo lường** → `03. Areas/Analytics & Reporting/` (chọn đúng miền: tương tác / traffic / quảng cáo / hiệu suất content / CSKH chat)
- **Feedback / chứng thực khách (testimonial, review, case study, góp ý)** → `04. Resources/Feedback & Chứng Thực/`
- **Giọng thật của CEO để viết content (story, quan điểm)** → `Nhật Ký CEO/`
- **Tra khách / đối thủ** → `People/`, `Companies/`, `04. Resources/Market & Competitor Research/Đối Thủ/`

## 3 lớp dữ liệu

| Lớp | Trả lời câu hỏi | Thư mục |
|---|---|---|
| **Business Context** | Công ty là ai, bán gì, nói giọng gì? (nền, ít đổi) | `00. Business Context/` |
| **PARA** | Việc này đang active hay chỉ tham khảo? | `01.` → `05.` |
| **Entity (AI Brain)** | Liên quan ai, công ty nào, quyết định nào? | `People/ Companies/ Meetings/ Decisions/` |

## 1. `00. Business Context/` — đọc TRƯỚC TIÊN (nguồn sự thật duy nhất)

| File | Agent cần gì thì đọc |
|---|---|
| `Chân Dung Doanh Nghiệp.md` | Định vị, ICP (khách lý tưởng) — "chúng tôi là ai, bán cho ai" |
| `Chân Dung CEO — [Tên].md` | Personal brand CEO (story, giá trị, chuyên môn, persona) — dùng khi thương hiệu gắn với cá nhân CEO |
| `Brand Voice — Giọng Thương Hiệu.md` | Giọng nói, từ nên/tránh dùng, câu mẫu — "viết như thế nào" |
| `Business Model Canvas — [Tên].md` (+ `.canvas`) | 9 khối mô hình kinh doanh — "kiếm tiền cách nào" |
| `Đánh Giá Mô Hình Kinh Doanh — [Tên].md` | Mô hình có nhất quán/khả thi không, bằng chứng PMF |
| `MHKD/` | Chi tiết từng phân khúc khách hàng + từng giá trị cốt lõi |
| `AI-Sale-Assistant.md` | AI được/không được tự làm gì trong vault này |
| `Sản Phẩm & Dịch Vụ/` | Hồ sơ từng gói: tính năng, **giá**, USP. Hình/video để ở `_Media/[tên sản phẩm]/`; feedback khách link từ `04. Resources/Feedback & Chứng Thực/` |

**Việc → file cần đọc:**
- Viết content/ads/email → `Brand Voice` + `Chân Dung Doanh Nghiệp`
- Tư vấn giá, đóng gói offer → `Sản Phẩm & Dịch Vụ/` + `Business Model Canvas`
- Xác định khách mục tiêu → `Chân Dung Doanh Nghiệp` (ICP) + `MHKD/Phân Khúc Khách Hàng/`
- Cần bằng chứng xã hội (proof, review, case study) → `04. Resources/Feedback & Chứng Thực/`

## 2. Lớp PARA (`01`–`05`) — dòng công việc

```
01. Inbox/      → capture thô, cuối ngày dọn về 0
02. Projects/   → việc CÓ deadline (chiến dịch, launch)
03. Areas/      → trách nhiệm LIÊN TỤC, không deadline  ← content & đo lường ở đây
04. Resources/  → tái sử dụng (playbook, template, nghiên cứu đối thủ)
05. Archive/    → đã đóng, không xoá
```

## 3. ⭐ Content đã tạo hàng ngày + kết quả đo lường (nằm trong `03. Areas/`)

### Content đã tạo/đăng — 1 file / 1 post
```
03. Areas/Brand & Content/
└─ Content Đã Đăng/
   └─ YYYY-MM-DD — [Kênh] — [Tên post].md
```

### Kết quả đo lường / báo cáo

Chia **2 trục**: báo cáo *theo thời gian* (tổng hợp) và *theo miền đo lường* (đo sâu — báo cáo định kỳ rút từ đây lên).

```
03. Areas/Analytics & Reporting/
├─ Báo Cáo Ngày/ | Tuần/ | Quý/          ← tổng hợp theo thời gian
├─ Tương Tác Mạng Xã Hội/                ← on-platform: reach, engagement, follower theo kênh
├─ Hiệu Quả Traffic Mạng Xã Hội/         ← off-platform: social → click ra web → chuyển đổi
├─ Hiệu Quả Quảng Cáo/                   ← paid: CPM/CTR/CPL/CPA/ROAS theo chiến dịch & creative
├─ Hiệu Suất Content/                    ← pivot theo Loại content · Format · Hook
└─ Chăm Sóc Khách Hàng/                  ← CSKH chat: phễu chat→chốt, tốc độ rep, lý do inbox
```

Mỗi miền có `_MOC` + file `[Mẫu]` — copy mẫu, bỏ tiền tố `[Mẫu]`, đổi kỳ. Đo *Hiệu Suất Content* cần gắn `content_pillar`/`format`/`hook` vào frontmatter mỗi bài trong `Content Đã Đăng/`.

**Vòng khép kín:** viết content → lưu `Brand & Content/Content Đã Đăng/` → số liệu post/kênh đó → ghi `Analytics & Reporting/`. Hai bên **link chéo** để agent biết content nào chạy tốt, không phải đoán.

### Các Area còn lại
```
03. Areas/Sales Pipeline & CRM/          → trạng thái deal, giai đoạn bán
03. Areas/Marketing Channels/            → từng kênh marketing đang chạy
03. Areas/Customer Success & Retention/  → chăm sóc & giữ khách sau bán
```

## 4. Lớp Entity — ai / công ty / quyết định

```
People/      → 1 file/người (lead, khách, team, đối tác)
Companies/   → 1 file/công ty (khách hàng, đối thủ, vendor)
Meetings/    → biên bản sale call, discovery call
Decisions/   → quyết định giá/kênh/ngân sách (cần xác nhận chủ DN)
Daily/       → nhật ký 3–5 dòng/ngày (công việc/vận hành)
Nhật Ký CEO/ → nhật ký cá nhân CEO: story, quan điểm, giọng thật → nuôi content có hồn (AI đọc để viết đúng chất CEO)
MOC/         → mục lục sống: Sales Pipeline, Content Calendar
```

**Nguyên tắc không note mồ côi:** một biên bản `Meetings/` phải link tới `People/` (ai họp) + `Companies/` (công ty nào) + `02. Projects/` hoặc `03. Areas/` liên quan.

---

## 5. Ví dụ khai báo dữ liệu — doanh nghiệp vừa làm spa vừa bán trà

> **Nguyên tắc:** vault = 1 công ty duy nhất. Nhưng 1 công ty **được phép có nhiều dòng sản phẩm và nhiều phân khúc khách hàng** — mỗi thứ tách thành 1 file riêng trong cùng `00. Business Context/`. **Không** tạo thư mục công ty con hay vault riêng cho từng mảng.

Giả sử "Spa Thảo Mộc" vừa cung cấp **dịch vụ spa** vừa bán **trà thảo mộc** đóng gói. Dữ liệu khai báo như sau:

| Loại thông tin | Lưu ở đâu | Ví dụ file |
|---|---|---|
| Định danh công ty, định vị chung, tone | `00. Business Context/Chân Dung Doanh Nghiệp.md` | (1 file duy nhất cho cả công ty) |
| Giọng thương hiệu | `00. Business Context/Brand Voice — Giọng Thương Hiệu.md` | (1 file) |
| **Từng dịch vụ/sản phẩm** (mỗi cái 1 file) | `00. Business Context/Sản Phẩm & Dịch Vụ/` | `Gói Massage Trị Liệu.md`, `Gói Chăm Sóc Da Mặt.md`, `Trà Thảo Mộc Detox.md`, `Trà Hoa Cúc Ngủ Ngon.md` |
| **Từng phân khúc khách hàng** (mỗi cái 1 file) | `00. Business Context/MHKD/Phân Khúc Khách Hàng/` | `PK1 — Nữ văn phòng 25-40 đi spa thư giãn.md`, `PK2 — Khách mua trà chăm sóc sức khoẻ tại nhà.md` |
| Từng giá trị cốt lõi | `00. Business Context/MHKD/Giá Trị Cốt Lõi/` | `GT1 — Thư giãn phục hồi bằng liệu pháp thảo mộc.md`, `GT2 — Trà sạch chuẩn hoá theo công thức spa.md` |
| Bức tranh tổng hợp 9 khối (nối spa + trà) | `00. Business Context/Business Model Canvas — Spa Thảo Mộc.md` (+ `.canvas`) | (1 file, có 2 phân khúc & 2 dòng doanh thu) |

**Vì sao tách file thay vì gộp:** spa (dịch vụ tại chỗ) và trà (bán lẻ mang về) thường là **2 phân khúc khách khác nhau, 2 dòng doanh thu khác nhau** — tách ra để agent viết content cho đúng đối tượng ("bài này bán trà cho khách mua tại nhà" ≠ "bài này mời đặt lịch spa"). File `Business Model Canvas` là chỗ nối chúng lại thành 1 bức tranh.

### Cây thư mục sau ~1 tháng vận hành (tháng 7/2026)

Đây là vault "Spa Thảo Mộc" khi đã dùng thật một tháng — để thấy dữ liệu **chảy vào đâu** khi làm việc hàng ngày:

```
00. Business Context/                         ← NGỮ CẢNH NỀN (ít đổi) — agent đọc trước tiên
├─ Chân Dung Doanh Nghiệp.md                  ← định vị, ICP tổng, đã điền đầy đủ
├─ Brand Voice — Giọng Thương Hiệu.md         ← "ấm áp, gần gũi, chuyên gia thảo mộc" + câu mẫu
├─ Business Model Canvas — Spa Thảo Mộc.md    ← 9 khối: 2 phân khúc, 2 dòng doanh thu (spa + trà)
├─ Business Model Canvas.canvas               ← bản vẽ 9 khối
├─ Đánh Giá Mô Hình Kinh Doanh — Spa Thảo Mộc.md
├─ MHKD/
│  ├─ _MHKD Spa Thảo Mộc — Tổng Quan.md       ← hub liệt kê 3 PK + 2 GT
│  ├─ Phân Khúc Khách Hàng/
│  │  ├─ PK1 — Nữ văn phòng 25-40 đi spa thư giãn.md
│  │  ├─ PK2 — Khách mua trà chăm sóc sức khoẻ tại nhà.md
│  │  └─ PK3 — Doanh nghiệp mua trà làm quà tặng.md
│  └─ Giá Trị Cốt Lõi/
│     ├─ GT1 — Thư giãn phục hồi bằng liệu pháp thảo mộc.md
│     └─ GT2 — Trà sạch chuẩn hoá theo công thức spa.md
└─ Sản Phẩm & Dịch Vụ/
   ├─ _MOC Sản Phẩm & Dịch Vụ.md
   ├─ Gói Massage Trị Liệu Thảo Mộc.md         ← hồ sơ .md để phẳng
   ├─ Gói Chăm Sóc Da Mặt Thải Độc.md
   ├─ Trà Thảo Mộc Detox.md
   ├─ Combo Trà Quà Tặng Doanh Nghiệp.md
   └─ _Media/                                  ← hình/video đi kèm, 1 thư mục/sản phẩm
      └─ Gói Massage Trị Liệu Thảo Mộc/
         ├─ hinh/01-anh-chinh.jpg
         └─ video/demo-quy-trinh.mp4

01. Inbox/                                     ← dọn gần sạch, còn 1-2 note thô chờ phân loại
└─ Ý tưởng livestream bán trà cuối tháng.md

02. Projects/                                  ← việc CÓ deadline
├─ _MOC Projects.md
└─ [2026-07] Chiến Dịch Hè — Combo Spa + Trà Detox.md   ← link tới content & thử nghiệm bên dưới

03. Areas/                                     ← VẬN HÀNH HÀNG NGÀY (content + đo lường ở đây)
├─ Brand & Content/
│  ├─ _MOC Brand & Content.md
│  └─ Content Đã Đăng/                         ← 1 file / 1 post, tích luỹ dần cả tháng
│     ├─ 2026-07-01 — Facebook — Ưu đãi khai trương gói massage.md
│     ├─ 2026-07-03 — TikTok — Review quy trình xông hơi thảo dược.md
│     ├─ 2026-07-05 — Instagram — Trà detox buổi sáng.md
│     ├─ 2026-07-08 — Facebook — Combo quà tặng doanh nghiệp.md
│     ├─ 2026-07-12 — TikTok — Khách kể trải nghiệm chăm sóc da.md
│     ├─ 2026-07-18 — Facebook — Flash sale trà hoa cúc.md
│     ├─ 2026-07-22 — Zalo OA — Nhắc lịch chăm sóc định kỳ.md
│     └─ 2026-07-28 — Instagram — Behind the scenes pha trà.md
├─ Analytics & Reporting/                      ← SỐ LIỆU / ĐO LƯỜNG (2 trục: thời gian + miền)
│  ├─ _MOC Analytics & Reporting.md
│  ├─ Tracking Plan.md                         ← từ skill /do-luong-tracking
│  ├─ Báo Cáo Ngày/  Tuần/  Quý/               ← tổng hợp theo thời gian
│  │  └─ Tuần 28-2026.md
│  ├─ Tương Tác Mạng Xã Hội/                   ← on-platform: reach/engagement/follower
│  │  ├─ Facebook — 2026-07.md
│  │  └─ TikTok — 2026-07.md
│  ├─ Hiệu Quả Traffic Mạng Xã Hội/            ← social → click ra web → chuyển đổi
│  │  └─ Traffic MXH Tuần 28-2026.md
│  ├─ Hiệu Quả Quảng Cáo/                      ← CPL/CPA/ROAS theo chiến dịch
│  │  └─ Báo Cáo QC — Combo Hè Tháng 7-2026.md
│  ├─ Hiệu Suất Content/                       ← pivot theo Loại · Format · Hook
│  │  └─ Hiệu Suất Content Tháng 7-2026.md
│  ├─ Chăm Sóc Khách Hàng/                     ← CSKH chat: phễu chat→chốt, tốc độ rep
│  │  └─ CSKH Chat Tuần 28-2026.md
│  └─ [2026-07-10] Thử Nghiệm — CTA "Đặt lịch" vs "Gọi ngay".md   ← từ skill /thu-nghiem-ab
├─ Marketing Channels/
│  ├─ _MOC Marketing Channels.md
│  ├─ [2026-07-02] SEO Audit — spathaomoc.vn.md ← từ skill /kiem-tra-seo
│  ├─ Facebook Page.md
│  ├─ TikTok.md
│  ├─ Zalo OA.md
│  └─ Google Maps & Local.md
├─ Sales Pipeline & CRM/
│  ├─ _MOC Sales Pipeline & CRM.md
│  └─ Pipeline Tháng 7-2026.md                 ← trạng thái deal đang chạy
└─ Customer Success & Retention/
   ├─ _MOC Customer Success & Retention.md
   └─ Kịch Bản Chăm Sóc Sau Liệu Trình.md

04. Resources/                                 ← TÁI SỬ DỤNG
├─ Market & Competitor Research/
│  └─ Đối Thủ/
│     ├─ _MOC Đối Thủ.md
│     ├─ Spa Sen Tây Hồ.md                     ← từ skill /phan-tich-doi-thu
│     └─ Trà Thảo Mộc ABC.md
├─ Feedback & Chứng Thực/                      ← testimonial, review, case study, góp ý (bằng chứng dùng chung)
│  ├─ _MOC Feedback & Chứng Thực.md
│  ├─ Testimonial — Chị Hương (PK1).md         ← type: testimonial
│  ├─ Case Study — Công ty ABC (PK3).md        ← type: case-study
│  └─ Media/                                   ← ảnh screenshot review, video khách quay
├─ Playbooks/
│  └─ Kịch Bản Xử Lý Từ Chối Giá.md
├─ Templates/
└─ Frameworks/

05. Archive/                                   ← đã đóng, không xoá
└─ [2026-06] Chiến Dịch Ra Mắt Trà Hoa Cúc.md

People/                                        ← KHÁCH THẬT (từng người) — link về phân khúc
├─ _MOC People.md
├─ Nguyễn Thị Hương — Khách VIP (PK1).md
├─ Trần Thị Lan — Lead trà detox (PK2).md
└─ Phạm Văn Minh — Mua sỉ quà tặng (PK3).md
Companies/
├─ _MOC Companies.md
└─ Công ty TNHH ABC — Khách mua trà quà tặng (PK3).md
Meetings/
├─ _MOC Meetings.md
└─ 2026-07-08 — Sale Call — Công ty ABC đặt trà quà tặng.md
Decisions/
├─ _MOC Decisions.md
└─ 2026-07-05 — Giá Combo Spa + Trà Mùa Hè.md
Daily/                                         ← nhật ký công việc
├─ 2026-07-06.md
└─ 2026-07-28.md
Nhật Ký CEO/                                   ← nhật ký cá nhân CEO → nguyên liệu content thật
├─ _Hướng Dẫn Nhật Ký CEO.md
├─ 2026-07-15 — Nhật ký.md                     ← chuyện khách kể ở spa → #hat-giong-content
└─ 2026-07-22 — Nhật ký.md                     ← quan điểm về "trà sạch" → #quan-diem
MOC/
├─ MOC Content Calendar.md                     ← lịch content xuyên các kênh
└─ MOC Sales Pipeline.md                       ← toàn cảnh pipeline
```

**Đọc cây trên theo dòng chảy công việc:**
1. Viết bài đăng Facebook về combo trà → lưu `03. Areas/Brand & Content/Content Đã Đăng/2026-07-08 — ...md`, viết đúng giọng lấy từ `00. Business Context/Brand Voice`.
2. Cuối tuần tổng hợp reach/engagement bài đó → `03. Areas/Analytics & Reporting/Báo Cáo Tuần/Tuần 28-2026.md` + `Tương Tác Mạng Xã Hội/Facebook — 2026-07.md`.
3. Một khách doanh nghiệp hỏi mua trà quà tặng → tạo `Companies/Công ty TNHH ABC ...md` + biên bản `Meetings/2026-07-08 — Sale Call ...md`, cả hai link về `PK3`.
4. Chốt giá combo hè → ghi `Decisions/2026-07-05 — Giá Combo ...md` (chủ DN xác nhận trước).

**Lưu ý phân biệt — phân khúc (chân dung nhóm) vs khách thật (từng người):**
- **Phân khúc khách hàng** = mô tả *một nhóm* khách lý tưởng (persona) → `00. Business Context/MHKD/Phân Khúc Khách Hàng/PK*.md`. Ngữ cảnh nền, agent đọc để biết viết cho ai.
- **Khách hàng cụ thể** = *một người/công ty* có thật đang mua → `People/`, `Companies/`. Dữ liệu vận hành — mỗi hồ sơ ghi rõ thuộc phân khúc nào (ví dụ tên file kèm `(PK3)` như trên, hoặc link `[[PK3 — ...]]` trong nội dung).

Cách chạy nhanh: gõ `/mo-hinh-kinh-doanh` → skill phỏng vấn 9 khối rồi tự sinh toàn bộ file trong `00. Business Context/` (kể cả từng file PK/GT trong `MHKD/`). Các file vận hành (`03. Areas/`, `People/`, `Meetings/`...) sinh dần khi làm việc thật hoặc khi chạy các skill tương ứng.

---

_Tra cứu nghiên cứu đối thủ, playbook, template tái dùng → `04. Resources/`. Việc đã đóng → `05. Archive/` (chuyển vào, không xoá)._
