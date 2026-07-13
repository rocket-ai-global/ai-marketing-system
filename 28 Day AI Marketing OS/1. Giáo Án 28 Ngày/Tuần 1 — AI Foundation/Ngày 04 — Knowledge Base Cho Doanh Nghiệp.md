---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 1
day: 4
core-output: "Knowledge Base trong Vault SME theo 10 nhóm tri thức · Data Access & Security Rule 3 tầng · Product Knowledge Document phủ 100% sản phẩm · FAQ & Objection Database ≥30 cặp Q&A · 3 tài liệu lõi đã nạp lên RocketAgent"
---

# Ngày 04 — Knowledge Base Cho Doanh Nghiệp

> 👩‍🏫 **File này là giáo án cho trainer/mentor.** Học viên nhận: [[Bài Tập Ngày 4 — Knowledge Base]] + mục 5-8 và 11 của file này.

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent và Hermes — Hermes là trợ lý AI chạy nền trên máy tính, đọc thẳng Vault SME và tương tác qua Telegram). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Chạy `/hoan-tat-business-context` — audit thiếu gì hỏi nấy. Đổ dữ liệu cũ đúng chỗ: media sản phẩm → `Sản Phẩm & Dịch Vụ/_Media/`, FAQ/Objection → `04. Resources/Playbooks/`, feedback khách → `04. Resources/Feedback & Chứng Thực/`.

> Hôm nay bạn xây "kho dữ liệu chuẩn" — Knowledge Base (cơ sở tri thức) — để AI hết trả lời chung chung: gom mọi thứ về sản phẩm, khách hàng, offer, câu hỏi thường gặp vào 10 NHÓM tri thức nằm đúng vị trí trong Vault SME (một nguồn sự thật), rồi nạp 3 tài liệu lõi lên RocketAgent. Không có ngày hôm nay thì chatbot tuần 3 chỉ là con vẹt.

## 0. 🧠 Giải Thích Sâu — Knowledge Base Là Gì?

### 0.1. Định nghĩa đơn giản

**Knowledge Base** là “bộ não dữ liệu” của doanh nghiệp để AI có thể hiểu đúng về doanh nghiệp đó.

Nếu không có Knowledge Base, AI chỉ biết kiến thức chung ngoài xã hội. Nó **không biết**:

- Sản phẩm/dịch vụ của doanh nghiệp tên gì
- Giá bao nhiêu
- Chính sách thanh toán, đổi trả, bảo hành thế nào
- Khách hàng hay hỏi gì
- Câu nào được phép trả lời tự động
- Câu nào phải chuyển cho người thật
- Giọng thương hiệu của doanh nghiệp ra sao
- Quy trình bán hàng/chăm sóc khách hiện tại như thế nào

> **Knowledge Base = toàn bộ tài liệu chuẩn hoá để AI trở thành “nhân viên hiểu doanh nghiệp”.**

Cách nói cho học viên:

> “AI giống một nhân viên rất giỏi nhưng mới vào công ty ngày đầu. Nếu anh chị không đưa bảng giá, sản phẩm, chính sách, câu hỏi khách hay hỏi, quy trình tư vấn, thì nó sẽ tự đoán. Mà AI tự đoán trong kinh doanh là rất nguy hiểm. Knowledge Base chính là sổ tay nhân viên mới cho AI. Ngày hôm nay, chúng ta xây sổ tay đó.”

Câu chốt:

> **Không có Knowledge Base, AI chỉ là người ngoài thông minh. Có Knowledge Base, AI mới trở thành nhân viên của doanh nghiệp bạn.**

### 0.2. Vì sao Ngày 04 cực kỳ quan trọng?

Ba ngày đầu học viên đã tạo ra các tài sản nền:

| Ngày | Tài sản tạo ra |
|---|---|
| Ngày 01 | Business Snapshot, BMC, AI Opportunity Map |
| Ngày 02 | Customer Avatar, PDFO Map (Pain–Desire–Fear–Objection — bản đồ Đau/Khát khao/Nỗi sợ/Phản đối), Customer Journey |
| Ngày 03 | Offer, định vị, thông điệp bán hàng |

Nhưng các tài sản này vẫn đang rời rạc. **Ngày 04 là ngày gom tất cả thành một bộ não có cấu trúc.**

Nếu không làm Ngày 04, sang Tuần 2–3 sẽ dễ bị lỗi:

- AI viết content chung chung
- Chatbot trả lời sai giá hoặc sai chính sách
- Sales script không đúng insight khách hàng
- Nhân viên mỗi người tư vấn một kiểu
- Dữ liệu nằm lung tung trong Zalo, Drive, trí nhớ chủ doanh nghiệp
- Không thể scale thành agent thật

Vì vậy, Ngày 04 là điểm chuyển từ:

> “Tôi có vài bài tập rời rạc”  
> sang  
> “Doanh nghiệp tôi có một bộ não AI đọc được.”

### 0.3. Knowledge Base khác gì Google Drive bình thường?

Google Drive bình thường chỉ là nơi chứa file. Knowledge Base thì khác vì có 4 tiêu chuẩn:

#### 1. Có cấu trúc

Không ném file lung tung. Mọi thứ phải nằm đúng chỗ trong Vault SME:

- Giá & hồ sơ sản phẩm → `00. Business Context/Sản Phẩm & Dịch Vụ/`
- Câu hỏi khách hay hỏi → `04. Resources/Playbooks/FAQ & Objection Database`
- Chân dung khách → `00. Business Context/MHKD/Phân Khúc Khách Hàng/`
- Kịch bản tư vấn → `04. Resources/Playbooks/`
- Case study khách hàng → `04. Resources/Feedback & Chứng Thực/`

#### 2. Có “một nguồn sự thật”

Một thông tin chỉ được có **một bản đúng nhất**.

Ví dụ sai (tình huống minh họa thường gặp trước khi chuẩn hóa):

- Bảng giá in cho hội chợ đợt trước ghi một số
- Tin nhắn Zalo nhân viên gửi khách ghi số khác
- Website ghi số khác nữa
- Mỗi nhân viên nhớ một con số "khoảng chừng"

AI đọc vào sẽ loạn.

Ví dụ đúng (case MSX):

> Giá Trà Mẩy Gòm An Giấc chỉ nằm trong hồ sơ sản phẩm `00. Business Context/Sản Phẩm & Dịch Vụ/Trà Mẩy Gòm An Giấc.md` — **359.000đ/hộp**. Các nơi khác nếu cần thì trỏ về file đó.

#### 3. AI đọc được

AI đọc tốt:

- File markdown/doc/text rõ ràng
- Có tiêu đề
- Có bảng gọn
- Mỗi phần một ý
- Số liệu rõ ràng

AI đọc kém:

- Ảnh chụp bảng giá mờ
- File scan
- Tin nhắn rời rạc
- File tên linh tinh
- Nhiều phiên bản mâu thuẫn

#### 4. Có phân quyền và bảo mật

Không phải dữ liệu nào cũng nạp vào AI.

| Loại dữ liệu | Có nên nạp AI? |
|---|---|
| FAQ công khai | Có |
| Bảng giá công khai | Có |
| Thông tin sản phẩm | Có |
| Script sales nội bộ | Có, nhưng giới hạn quyền |
| Số điện thoại khách | Không hoặc phải ẩn |
| Doanh thu chi tiết | Hạn chế |
| Hợp đồng, hồ sơ nhạy cảm | Không nạp bừa |

### 0.4. Cây 10 thư mục Knowledge Base chuẩn

```text
[Tên DN] — Knowledge Base
│
├── 01. Business Overview
├── 02. Product & Service
├── 03. Customer Avatar
├── 04. Offer & Sales Message
├── 05. Marketing Assets
├── 06. Sales Assets
├── 07. FAQ & Objection
├── 08. SOP & Operation
├── 09. Case Study
└── 10. Reports & Metrics
```

| Thư mục | Vai trò | AI dùng để làm gì |
|---|---|---|
| `01. Business Overview` | Tổng quan doanh nghiệp | Hiểu doanh nghiệp là ai, bán gì, cho ai |
| `02. Product & Service` | Sản phẩm/dịch vụ, giá, chính sách | Trả lời đúng về sản phẩm, không bịa giá |
| `03. Customer Avatar` | Chân dung khách, pain/desire/fear/objection | Viết content, chatbot, sale script đúng insight |
| `04. Offer & Sales Message` | Offer, USP, thông điệp bán hàng | Tạo bài bán hàng, landing page, pitch |
| `05. Marketing Assets` | Bài viết, ảnh, video, brand voice | Tạo content mới đúng giọng thương hiệu |
| `06. Sales Assets` | Script tư vấn, báo giá, proposal | Tư vấn, follow-up, chốt đơn |
| `07. FAQ & Objection` | Câu hỏi thường gặp & xử lý từ chối | Chatbot/CSKH trả lời nhất quán |
| `08. SOP & Operation` | Quy trình vận hành | Tạo checklist, nhắc việc, onboarding nhân viên |
| `09. Case Study` | Feedback, testimonial, before/after | Tạo social proof, landing page, sales deck |
| `10. Reports & Metrics` | KPI, lead, conversion, doanh thu | Đo kết quả, tạo dashboard, CEO Copilot |

### 0.5. Knowledge Base là nền để sinh Agent

Học viên cần hiểu quan hệ này:

```text
Knowledge Base = Não
Prompt = Cách giao việc
Agent = Nhân sự AI
Workflow = Quy trình làm việc
Tool/API = Tay chân thao tác
Dashboard = Mắt đo lường
```

Nếu không có Knowledge Base, Agent chỉ là chatbot thông minh nhưng không hiểu doanh nghiệp. Khi có Knowledge Base, ta mới sinh được:

| Agent | Cần đọc phần nào |
|---|---|
| Marketing Agent | Business Overview, Avatar, Offer, Marketing Assets |
| Sales Agent | Product, Offer, Sales Assets, FAQ |
| CSKH Agent | Product, FAQ, SOP, Case Study |
| CEO Copilot | Reports, Business Overview, Metrics |
| Content Agent | Avatar, Brand Voice, Content Pillar |
| Onboarding Agent | SOP, Product, Internal Docs |

Vì vậy Ngày 04 không chỉ là “dọn file”. Nó là:

> **Ngày tạo bộ não để toàn bộ AI Agent phía sau có dữ liệu mà vận hành.**

### 0.6. Ví dụ thực tế

Khách hỏi chatbot:

> “Gói 28 Day AIOS giá bao nhiêu?”

Nếu không có Knowledge Base, AI có thể trả lời:

> “Giá thường dao động từ vài triệu đến vài chục triệu tùy chương trình.”

Nghe hợp lý nhưng vô dụng.

Nếu có Knowledge Base, AI trả lời:

> “Dạ gói 28 Day AIOS hiện có 3 mức: Transfer, Installed và Managed. Mức cơ bản dành cho chủ SME muốn tự triển khai theo hướng dẫn; mức cao hơn có mentor/agent hỗ trợ setup. Anh/chị muốn em gửi bảng so sánh 3 gói không ạ?”

Khác biệt là: **câu trả lời có dữ liệu, có định vị, có bước bán hàng tiếp theo.**

### 0.7. Với RocketAI Platform: Product hoá thành AI Business Brain

Sau này RocketAI không nên chỉ nói “upload tài liệu cho chatbot đọc”. Nên product hoá Knowledge Base thành **AI Business Brain** gồm:

1. Business Profile
2. Customer Brain
3. Product Brain
4. Offer Brain
5. Sales Brain
6. Marketing Brain
7. Operation Brain
8. Metrics Brain

Luồng platform:

```text
AI Business Brain
      ↓
Marketing Agent
Sales Agent
CSKH Agent
Ops Agent
CEO Copilot
```

Đây là nền để RocketAI mở rộng thành platform agent đa ngành.

---

## 1. 🎯 Mục Tiêu Ngày Học

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Knowledge Base Folder (thư mục cơ sở tri thức)** — cây 10 thư mục chuẩn trên Google Drive (hoặc máy tính), đã gom tài liệu hiện có vào đúng chỗ.
- ✅ **Data Access & Security Rule (quy tắc truy cập & bảo mật dữ liệu)** — ai được xem/sửa/tải/nạp tài liệu nào vào RocketAgent; dữ liệu nào không được đưa vào AI.
- ✅ **Product Knowledge Document (tài liệu tri thức sản phẩm)** — 1 file chuẩn hóa TOÀN BỘ dịch vụ: tên, giá, thành phần, quy trình, chính sách — nguồn sự thật duy nhất về sản phẩm.
- ✅ **FAQ & Objection Database (kho câu hỏi thường gặp & phản đối)** — ≥30 cặp Hỏi-Đáp chuẩn, gồm ≥20 FAQ + ≥10 objection kèm câu trả lời mẫu.
- ✅ **3 tài liệu lõi đã nạp lên RocketAgent** (Business Overview, Product Knowledge, FAQ) — kiểm tra bằng 3 câu hỏi thử.

**Bonus Output (nâng cao):**
- ⭐ **Sales Knowledge Base** — kịch bản tư vấn hiện tại (ghi lại cách bạn/nhân viên giỏi nhất đang nói), báo giá mẫu, quy trình chốt.
- ⭐ **Marketing Knowledge Base** — 5-10 bài viết cũ tốt nhất, đặc tả giọng thương hiệu, thư viện ảnh/video theo chủ đề.

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Knowledge Base là gì & vì sao AI cần "bộ não dữ liệu" (5')
- **Ý chính:** AI mặc định biết mọi thứ về thế giới nhưng KHÔNG BIẾT GÌ về doanh nghiệp bạn: giá của bạn, chính sách của bạn, cách bạn xưng hô với khách. Knowledge Base = bộ tài liệu chuẩn để AI "nhập học" về DN. Chất lượng câu trả lời của AI = chất lượng Knowledge Base × chất lượng câu lệnh.
- **Cách giảng:** Analogy nhân viên mới: "Tuyển bạn nhân viên giỏi nhất thế giới, nhưng ngày đầu đi làm không đưa bảng giá, không đưa quy trình — bạn ấy tư vấn kiểu gì? Knowledge Base chính là 'sổ tay nhân viên mới' cho AI."
- **Demo phản chứng 60 giây:** hỏi AI trống "Liệu trình nám ở Sen Spa giá bao nhiêu?" → AI bịa hoặc né. Đó là lý do của cả ngày hôm nay.

### Khối 2 — Nguyên tắc "một nguồn sự thật" & dữ liệu sạch (7')
- **Ý chính:** Mỗi loại thông tin chỉ sống ở MỘT file (giá chỉ ở Product Knowledge — không rải rác 5 nơi). Dữ liệu AI đọc tốt: file text/doc có tiêu đề rõ, bảng gọn, mỗi mục một ý; dữ liệu AI đọc kém: ảnh chụp bảng giá, file scan, tin nhắn rời rạc, file trùng lặp nhiều phiên bản.
- **Cách giảng:** Quy tắc 4 SẠCH: (1) đúng chỗ — theo cây 10 thư mục; (2) đúng tên — `[Số thư mục]. [Tên tài liệu] — [phiên bản/ngày]`; (3) không trùng — bản cũ chuyển vào thư mục `_Archive` (lưu trữ); (4) có chủ — mỗi tài liệu ghi ai chịu trách nhiệm cập nhật.
- **Ví dụ Sen Spa:** Bảng giá đang tồn tại ở 4 nơi: ảnh in treo tường, file cũ 2023 trong máy, đoạn tin nhắn Hương gửi khách, trí nhớ chị Lan — và 4 bản KHÁC NHAU. Hôm nay hợp nhất thành 1.

### Khối 3 — Đồng bộ & bảo mật: AI đọc đúng, người dùng đúng quyền (5')
- **Ý chính:** Knowledge Base không chỉ là nơi chứa file; nó là "não bộ vận hành" của doanh nghiệp. Não này phải đồng bộ, có phân quyền và có ranh giới dữ liệu. Không phải tài liệu nào cũng nạp lên Agent, và không phải nhân sự nào cũng được sửa nguồn sự thật.
- **Quy tắc 3 tầng dữ liệu:** (1) **Public/khách hàng xem được** — FAQ, bảng giá công khai, thông tin dịch vụ; (2) **Internal/nội bộ** — SOP, script sale, báo cáo KPI, chỉ nhân sự liên quan xem; (3) **Restricted/hạn chế** — dữ liệu cá nhân khách hàng, tài chính chi tiết, hợp đồng, bệnh án/tình trạng nhạy cảm; chỉ đưa vào AI khi đã ẩn thông tin định danh hoặc có quyền rõ.
- **Cách giảng:** Agent làm việc 24/7 nên sai quyền là rủi ro 24/7. Bảo mật không làm hệ thống chậm hơn; bảo mật giúp chủ DN dám dùng AI vào việc thật.

### Khối 4 — Cây 10 thư mục chuẩn (8')
- **Ý chính:** 10 thư mục chuẩn của chương trình: `01. Business Overview` (tổng quan DN) · `02. Product & Service` (sản phẩm dịch vụ) · `03. Customer Avatar` (chân dung khách) · `04. Offer & Sales Message` (offer & thông điệp) · `05. Marketing Assets` (tài sản marketing) · `06. Sales Assets` (tài sản bán hàng) · `07. FAQ & Objection` (hỏi đáp & phản đối) · `08. SOP & Operation` (quy trình vận hành) · `09. Case Study` (câu chuyện khách thành công) · `10. Reports & Metrics` (báo cáo & số liệu).
- **Cách giảng:** Tin tốt: thư mục 01, 03, 04 đã XONG từ Ngày 1-3 — BMC + Snapshot vào 01, Avatar/Journey vào 03, Offer/Message vào 04. Hôm nay xây mới 02 và 07 (nặng nhất), các thư mục còn lại gom được gì bỏ nấy, bổ sung dần trong 3 tuần tới (05 đầy lên ở tuần 2, 06 ở tuần 3, 10 ở tuần 4).
- **Mẹo:** thư mục nào chưa có gì, tạo 1 file `_Cần bổ sung.md` ghi danh sách thiếu — đây chính là Improvement List (danh sách cải thiện) cho Ngày 06.

### Khối 5 — Biến tri thức ngầm thành tài liệu: kỹ thuật "AI phỏng vấn + bóc băng" (5')
- **Ý chính:** Tài sản quý nhất của DN dịch vụ không nằm trong file nào — nằm trong ĐẦU người giỏi nhất (cách Hương tư vấn, cách chị Lan xử lý khách khó). Cách rút ra nhanh: (1) để AI phỏng vấn mình từng câu (như Prompt 1 Ngày 01), hoặc (2) ghi âm 1 buổi tư vấn thật/1 lần kể lại → dán transcript (bản gỡ băng) cho AI chuẩn hóa thành tài liệu.
- **Ví dụ Sen Spa:** Chị Lan nhờ Hương kể lại cách tư vấn ca khách nám điển hình trong 10 phút, ghi âm bằng điện thoại, dùng tính năng chuyển giọng nói thành văn bản, dán vào Prompt 4 → ra kịch bản tư vấn chuẩn hóa đầu tiên (Bonus hôm nay, tài sản chính của Tuần 3).

> **Thích ứng ngành khác:** Nha khoa — thêm tài liệu "chỉ định & chống chỉ định" từng dịch vụ vào 02 (AI phải biết khi nào TỪ CHỐI tư vấn và hẹn bác sĩ); Giáo dục — 02 gồm lộ trình khóa, giáo trình mẫu, chuẩn đầu ra; 09 là điểm số/thành tích học viên. Gym/Coaching — 02 thêm gói PT theo buổi, chính sách bảo lưu (objection số 1). Mọi ngành giữ nguyên cây 10 thư mục.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 03 | Chiếu 1 offer tốt (cam kết đo được) + 1 lỗi "hứa quá tay"/khan hiếm giả. Nhắc: hôm nay bắt đầu dùng RocketAgent — ai chưa có tài khoản làm ngay theo link ghim. |
| 25' | Giảng kiến thức trọng tâm | 5 khối mục 2, kèm demo phản chứng 60 giây ở Khối 1. |
| 30' | Demo thực hành live | Dựng Knowledge Base Sen Spa: tạo cây thư mục → chuẩn hóa Product Knowledge → sinh FAQ database → nạp lên RocketAgent → test (kịch bản mục 4). |
| 15' | Học viên làm tại chỗ + Q&A | Học viên tạo cây 10 thư mục + kéo BMC/Snapshot/Avatar/Offer Ngày 1-3 vào đúng chỗ. Gõ vào chat: "Đã tạo xong 10 thư mục + tên 3 loại tài liệu mình ĐANG CÓ sẵn nhiều nhất". |
| 10' | Giao bài tập | Chiếu deliverable + rubric. Nhấn mạnh: FAQ lấy từ inbox THẬT, không sáng tác. |

**Checklist chuẩn bị của trainer:** tài khoản RocketAgent demo đã đăng nhập, KB trống sẵn sàng nạp · file Product Knowledge Sen Spa hoàn chỉnh (làm trước) để đối chiếu · 10 đoạn inbox mẫu của Sen Spa cho demo FAQ · quay sẵn video 3' "đăng ký & nạp file lên RocketAgent" phát cho người thao tác chậm · link Template 4.1-4.3 ghim sẵn.

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (4') — Tạo cây 10 thư mục & gom tài sản có sẵn.**
- Làm gì: Trên Google Drive, tạo thư mục `Sen Spa — Knowledge Base`, tạo 10 thư mục con đúng tên chuẩn (copy từ Template 4.1). Kéo 4 file Ngày 1-3 vào: BMC + Snapshot → 01, Avatar/Journey → 03, Offer → 04.
- Kết quả trông như thế nào: cây thư mục gọn, 3 thư mục đã có file, 7 thư mục còn trống có file `_Cần bổ sung.md`.
- Điểm nhấn: "3 ngày qua anh chị đã xây Knowledge Base mà không biết. Hôm nay chỉ dọn nhà và lấp chỗ trống."

**Bước 2 (10') — Chuẩn hóa Product Knowledge Document.**
- Làm gì: Chị Lan có dữ liệu thô: ảnh bảng giá cũ, vài dòng ghi chú. Paste Prompt 1 — AI phỏng vấn từng dịch vụ một (tên → giá → thành phần buổi → quy trình → chống chỉ định → chính sách). Trainer trả lời vai chị Lan cho 2 dịch vụ đầu, tua nhanh phần còn lại (chiếu bản làm sẵn).
- Kết quả: 1 file có 4 dịch vụ, mỗi dịch vụ 1 khối chuẩn cùng cấu trúc + phần chính sách chung (thanh toán, hoàn/hủy, bảo lưu, trả góp).
- Điểm nhấn: mục "chống chỉ định & câu từ chối khéo" — AI cần biết khi nào nói KHÔNG (khách mang thai, da đang viêm nặng → hẹn tư vấn trực tiếp), đây là phần cứu uy tín spa.

**Bước 3 (8') — Sinh FAQ & Objection Database từ inbox thật.**
- Làm gì: Dán 10 đoạn inbox mẫu của Sen Spa + Product Knowledge + Offer vào Prompt 2. AI gom nhóm câu hỏi trùng, sinh 30+ cặp Q&A, mỗi câu trả lời viết đúng giọng "chị em thân tình" và kết bằng 1 câu dẫn tiếp (mời soi da / xin số Zalo).
- Kết quả: bảng 3 cột — Câu hỏi/Phản đối | Trả lời chuẩn | Ghi chú (khi nào chuyển người thật).
- Điểm nhấn: mỗi câu trả lời có CTA nhỏ ở cuối — "FAQ không chỉ để trả lời, mà để DẪN khách đi tiếp một bước".

**Bước 4 (5') — Nạp 3 tài liệu lõi lên RocketAgent.**
- Làm gì: Vào RocketAgent → mục Knowledge Base → tạo bộ "Sen Spa KB" → upload 3 file (Business Overview, Product Knowledge, FAQ & Objection) → chờ hệ thống xử lý xong (trạng thái hiển thị đã nạp).
- Kết quả: 3 tài liệu trạng thái sẵn sàng trong RocketAgent.
- *Phương án thay thế:* nếu học viên chưa có RocketAgent → tạo 1 Project trong ChatGPT/Claude Projects, upload 3 file tương tự — sang Ngày 06 vẫn chuyển được lên RocketAgent.

**Bước 5 (3') — Test 3 câu "khám sức khỏe" Knowledge Base.**
- Làm gì: Hỏi AI (đã gắn KB): (1) "Liệu trình nám bên mình giá bao nhiêu, gồm những gì?" — kỳ vọng: đúng 15tr, đủ thành phần, không bịa; (2) "Em đang cho con bú có làm được không?" — kỳ vọng: trả lời theo mục chống chỉ định, hẹn tư vấn trực tiếp; (3) "Bên em có gì khác spa X?" — kỳ vọng: trả lời bằng USP, không nói xấu đối thủ.
- Kết quả: 2/3 câu tốt, 1 câu thiếu → ghi vào `_Cần bổ sung.md`. 
- Điểm nhấn: "Test — thiếu — bổ sung — test lại. Vòng lặp này chính là nghề nuôi AI, Ngày 06 làm kỹ."

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core ≤ 2h)

**Cụm A — Dựng khung & gom tài sản (15'):**
- [ ] Tạo thư mục `[Tên DN] — Knowledge Base` + 10 thư mục con đúng tên chuẩn (8')
- [ ] Kéo BMC + Snapshot + Avatar/Journey + Offer Ngày 1-3 vào thư mục 01/03/04; gom mọi file sẵn có (bảng giá, ảnh, bài viết cũ) vào đúng thư mục — chưa cần đẹp, đúng chỗ trước (7')

**Cụm A2 — Phân quyền & bảo mật (5'):**
- [ ] Điền Data Access & Security Rule bản tối thiểu: ai được xem/sửa từng nhóm thư mục, tài liệu nào không được nạp vào AI nếu chưa ẩn thông tin nhạy cảm (4')
- [ ] Đánh dấu ít nhất 3 loại dữ liệu Restricted của DN mình (VD: SĐT khách, hồ sơ da/bệnh án, hợp đồng, doanh thu chi tiết) (1')

**Cụm B — Product Knowledge Document (35'):**
- [ ] Chạy Prompt 1, trả lời phỏng vấn cho TỪNG dịch vụ đang bán (22')
- [ ] Rà số liệu: giá, thời lượng, số buổi phải đúng 100% — sai 1 số là chatbot báo sai giá cho khách thật (8')
- [ ] Điền phần chính sách chung + chống chỉ định/trường hợp từ chối (5')

**Cụm C — FAQ & Objection Database (30'):**
- [ ] Mở inbox/Zalo, chép 10-15 câu hỏi thật khách đã hỏi (8')
- [ ] Chạy Prompt 2 (đầu vào: câu hỏi thật + Product Knowledge + Offer + PDFO Map) (8')
- [ ] Rà 30 cặp Q&A: sửa câu trả lời nào "không phải giọng mình", đánh dấu các câu phải chuyển người thật (14')

**Cụm D — Nạp lên RocketAgent & test (10'):**
- [ ] Upload 3 tài liệu lõi lên RocketAgent Knowledge Base (hoặc ChatGPT/Claude Projects) (5')
- [ ] Test 3 câu khám sức khỏe (giá + trường hợp đặc biệt + so sánh); chụp màn hình kết quả (5')

**Cụm E — Nộp bài (5'):**
- [ ] Nộp link thư mục KB (quyền xem) + 3 ảnh test vào thread cohort trước 23h59

**Bonus:** ghi âm mình/nhân viên giỏi nhất kể lại 1 ca tư vấn điển hình 10' → chạy Prompt 4 chuẩn hóa thành kịch bản tư vấn (bỏ vào 06); gom 5-10 bài viết cũ tốt nhất + chạy Prompt 3 rút "đặc tả giọng thương hiệu" (bỏ vào 05).

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Dựng Knowledge Base cho doanh nghiệp bạn: (1) cây 10 thư mục chuẩn đã gom tài liệu hiện có, thư mục trống có file `_Cần bổ sung.md`, (2) Data Access & Security Rule, (3) Product Knowledge Document phủ 100% dịch vụ đang bán, (4) FAQ & Objection Database ≥30 cặp (≥20 FAQ + ≥10 objection) trong đó ≥10 câu lấy từ inbox thật, (5) 3 tài liệu lõi đã nạp lên RocketAgent + ảnh chụp 3 câu test.

**Deliverable nộp:**
- Link thư mục: `[Tên DN] — Knowledge Base` (bật quyền xem cho mentor)
- File tổng hợp: `[Tên DN] — Ngày 04 — Knowledge Base Report` (gồm: ảnh cây thư mục + link 3 tài liệu lõi + 3 ảnh chụp test + danh sách `_Cần bổ sung`)
- Ví dụ: `Sen Spa — Ngày 04 — Knowledge Base Report`

**Deadline:** 23h59 cùng ngày, nộp vào thread cohort ngày 04.

## 7. 📄 Template Đi Kèm

**Template 4.1 — Cây thư mục Knowledge Base + Data Access & Security Rule.** Danh sách 10 tên thư mục chuẩn (copy nguyên văn) + quy ước đặt tên file + mẫu file `_Cần bổ sung.md` (3 cột: tài liệu thiếu | ai cung cấp được | hạn bổ sung). Kèm bảng phân quyền 4 cột: Nhóm dữ liệu | Ai được xem | Ai được sửa | Có được nạp vào Agent không? (`Có / Có sau khi ẩn thông tin / Không`).

**Template 4.2 — Product Knowledge Document.** Mỗi dịch vụ 1 khối gồm các trường: Tên dịch vụ | Giá (lẻ/gói, đã gồm gì) | Dành cho ai / vấn đề gì | Thành phần 1 buổi (các bước, thời lượng) | Số buổi & giãn cách | Kết quả kỳ vọng theo mốc (viết thận trọng) | Chống chỉ định & trường hợp từ chối (kèm câu từ chối khéo) | Chuẩn bị trước – chăm sóc sau | Câu hỏi hay gặp riêng của dịch vụ này. Cuối file: khối Chính sách chung (thanh toán, trả đợt, hoàn/hủy, bảo lưu, chuyển nhượng). *Kèm bản Sen Spa điền mẫu 2 dịch vụ.*

**Template 4.3 — FAQ & Objection Database.** Bảng 4 cột: # | Câu hỏi/Phản đối (nguyên văn giọng khách) | Câu trả lời chuẩn (3-5 câu, kết bằng 1 câu dẫn tiếp) | Xử lý đặc biệt (trả lời thẳng / chuyển người thật / cần hỏi lại thông tin gì). Chia 2 phần: A. FAQ (≥20) — nhóm theo chủ đề: giá & thanh toán, quy trình & hiệu quả, an toàn & chống chỉ định, lịch & địa điểm; B. Objection (≥10) — đúng các objection trong PDFO Map Ngày 02.

### Trích bản điền mẫu Template 4.3 — Sen Spa

| # | Câu hỏi/Phản đối | Câu trả lời chuẩn | Xử lý đặc biệt |
|---|---|---|---|
| A1 | "Trị nám bên mình bao nhiêu tiền ạ?" | "Dạ chị ơi, liệu trình nám chuyên sâu bên em là 15tr cho 10 buổi (đã gồm soi da định kỳ + phác đồ chăm tại nhà), có hỗ trợ chia 2 đợt ạ. Mỗi tình trạng nám cần phác đồ khác nhau, chị inbox 'SOI DA' để em giữ cho chị suất soi da miễn phí tháng này nhé — xem tình trạng rồi mới tư vấn đúng được ạ." | Trả lời thẳng, luôn kèm CTA soi da |
| A7 | "Em đang mang thai làm được không chị?" | "Dạ chị đang mang thai thì bên em xin phép KHÔNG thực hiện các dịch vụ công nghệ để an toàn tuyệt đối cho mẹ và bé ạ. Chị lưu thông tin, sau sinh 6 tháng bên em kiểm tra da lại miễn phí cho chị nhé." | Từ chối chuẩn + giữ liên hệ; không tư vấn thêm |
| B3 | "15 triệu hơi quá tay với em" | "Dạ em hiểu ạ, 15tr là khoản đáng cân nhắc mà. Tính ra mỗi buổi 1tr5 kèm soi da và phác đồ riêng — chị đang mất bao nhiêu mỗi tháng cho kem với che khuyết điểm rồi ạ? Bên em có chia 2 đợt, và cam kết mốc buổi 5 bằng ảnh soi da nên chị không phải 'đặt cược' như mua kem trôi nổi ạ." | Nếu vẫn từ chối lần 2 → mời gói lẻ trải nghiệm + chuyển tư vấn viên |

## 8. 🤖 Prompt Mẫu

### Prompt 1 — AI phỏng vấn để chuẩn hóa Product Knowledge

```
[VAI TRÒ] Bạn là chuyên gia quản trị tri thức (knowledge management) cho SME dịch vụ, giỏi đặt câu hỏi để rút toàn bộ thông tin sản phẩm từ chủ doanh nghiệp ra thành tài liệu chuẩn.

[BỐI CẢNH] Tôi cần xây Product Knowledge Document — nguồn sự thật duy nhất về mọi dịch vụ, để nạp cho AI trả lời khách. Thông tin hiện nằm rải rác trong đầu tôi, bảng giá cũ và tin nhắn.

[NHIỆM VỤ] Phỏng vấn tôi TỪNG DỊCH VỤ MỘT. Với mỗi dịch vụ, hỏi lần lượt 9 mục (mỗi lần 1 câu, chờ tôi trả lời): (1) tên chính thức; (2) giá — lẻ/gói, đã gồm và chưa gồm gì; (3) dành cho ai, giải quyết vấn đề gì; (4) một buổi/lần sử dụng diễn ra thế nào — các bước, thời lượng; (5) trọn gói bao nhiêu buổi, giãn cách; (6) kết quả kỳ vọng theo mốc thời gian — nhắc tôi nếu tôi nói quá tuyệt đối; (7) trường hợp KHÔNG nên dùng / phải từ chối; (8) khách cần chuẩn bị gì trước và chăm sóc gì sau; (9) 3 câu khách hay hỏi nhất riêng về dịch vụ này. Xong 1 dịch vụ, xuất khối tài liệu chuẩn rồi hỏi "còn dịch vụ nào không?". Kết thúc: hỏi thêm khối chính sách chung (thanh toán, trả đợt, hoàn/hủy, bảo lưu) và xuất toàn bộ file hoàn chỉnh.

[DỮ LIỆU ĐẦU VÀO] Danh sách tên dịch vụ của tôi: {{liệt kê tên các dịch vụ + giá nếu nhớ}}. Dữ liệu thô sẵn có: {{dán bảng giá cũ/ghi chú nếu có}}.

[ĐỊNH DẠNG ĐẦU RA] Mỗi dịch vụ 1 khối 9 đề mục thống nhất; cuối file khối "Chính sách chung"; toàn bộ ở dạng văn bản có tiêu đề rõ (không cần bảng phức tạp) để nạp vào Knowledge Base.

[RÀNG BUỘC] Tuyệt đối không tự điền số liệu tôi chưa cung cấp — thiếu thì ghi "[cần bổ sung]". Mục 6: tự động viết lại các cụm tuyệt đối ("hết hẳn", "trắng 100%") thành mô tả thận trọng có mốc. Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{Danh sách dịch vụ}}` → "1) Chăm sóc da cơ bản 1.5tr/buổi; 2) Liệu trình trị mụn 8 buổi 12tr; 3) Liệu trình trị nám 10 buổi 15tr; 4) Liệu trình trẻ hóa 12 buổi 15tr." `{{Dữ liệu thô}}` → dán ảnh bảng giá 2023 đã gõ lại + ghi chú "giá nám đã tăng từ 13tr lên 15tr từ 3/2026".

### Prompt 2 — Sinh FAQ & Objection Database từ inbox thật

```
[VAI TRÒ] Bạn là trưởng nhóm chăm sóc khách hàng ngành dịch vụ làm đẹp, chuyên xây kho câu trả lời chuẩn cho đội tư vấn và chatbot.

[BỐI CẢNH] Tôi cần FAQ & Objection Database ≥30 cặp Hỏi-Đáp để: nhân viên trả lời thống nhất, và nạp cho AI/chatbot. Tôi có sẵn câu hỏi thật từ inbox và các tài liệu chuẩn.

[NHIỆM VỤ] (1) Gom nhóm các câu hỏi thật tôi cung cấp (câu trùng ý gộp làm một, giữ cách diễn đạt tự nhiên nhất). (2) Bổ sung cho đủ ≥20 FAQ phủ 4 chủ đề: giá & thanh toán · quy trình & hiệu quả · an toàn & trường hợp đặc biệt · lịch hẹn & địa điểm. (3) Viết ≥10 câu xử lý objection dựa đúng danh sách phản đối trong bản đồ tâm lý. (4) Mỗi câu trả lời: 3-5 câu, đúng số liệu từ Product Knowledge, đúng giọng thương hiệu, kết bằng 1 câu dẫn khách đi tiếp (đặt lịch/để lại số/nhận tài liệu). (5) Đánh dấu các câu AI/nhân viên mới KHÔNG được tự trả lời mà phải chuyển người phụ trách (khiếu nại, tình trạng y khoa phức tạp, đòi hoàn tiền).

[DỮ LIỆU ĐẦU VÀO] Câu hỏi thật từ inbox: {{dán 10-15 câu nguyên văn}}. Product Knowledge Document: {{dán}}. Core Offer: {{dán phần chính}}. Objection từ PDFO Map: {{dán}}. Giọng thương hiệu: {{VD: chị em thân tình, xưng "em" với khách, không kiểu cách}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng 4 cột: # | Câu hỏi/Phản đối | Câu trả lời chuẩn | Xử lý đặc biệt. Phần A: FAQ theo 4 chủ đề. Phần B: Objection. Cuối: danh sách "🚨 Bắt buộc chuyển người thật".

[RÀNG BUỘC] Giá và chính sách phải khớp 100% Product Knowledge — nếu 2 nguồn tôi đưa mâu thuẫn, dừng lại hỏi tôi. Không hứa hẹn y khoa tuyệt đối. Câu trả lời không dài quá 80 từ (khách đọc trên điện thoại). Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{Câu hỏi thật}}` → "1) 'trị nám bao nhiêu tiền ạ' · 2) 'có đau không chị, da em mỏng lắm' · 3) 'em cho con bú được làm không' · 4) 'giá này trọn gói chưa hay còn phát sinh' · 5) 'làm 1 buổi có thấy khác không hay phải hết liệu trình' · 6) 'bên mình dùng máy gì, có giấy tờ không' · 7) 'chủ nhật có mở không em' · 8) 'em ở Long Biên xa quá' · 9) 'thôi để em suy nghĩ thêm' · 10) 'bên kia đang giảm 50% sao bên em đắt thế'..."

### Prompt 3 (Bonus) — Rút "đặc tả giọng thương hiệu" từ bài viết cũ

```
[VAI TRÒ] Bạn là chuyên gia phân tích văn phong thương hiệu (brand voice analyst).

[BỐI CẢNH] Tôi muốn mọi nội dung AI viết sau này đều đúng "giọng" của tôi. Tôi có các bài viết/tin nhắn cũ do chính tôi viết được khách phản hồi tốt.

[NHIỆM VỤ] Phân tích các mẫu văn bản dưới đây và xuất "Đặc tả giọng thương hiệu" gồm: (1) xưng hô với khách; (2) 5 đặc điểm giọng văn (kèm ví dụ trích từ bài của tôi); (3) 10 từ/cụm từ đặc trưng tôi hay dùng; (4) 5 điều KHÔNG BAO GIỜ viết (từ sáo rỗng, kiểu câu không hợp); (5) 1 đoạn văn mẫu 80-100 từ viết đúng giọng đó về chủ đề tôi chỉ định — để làm mẫu đối chiếu.

[DỮ LIỆU ĐẦU VÀO] 3-5 bài viết/tin nhắn cũ tốt nhất của tôi: {{dán nguyên văn}}. Chủ đề đoạn mẫu: {{VD: nhắc khách chăm da sau buổi trị nám đầu tiên}}.

[ĐỊNH DẠNG ĐẦU RA] Tài liệu 5 mục, ≤350 từ, tiêu đề "Đặc Tả Giọng Thương Hiệu — [Tên DN]" — lưu vào thư mục 05. Marketing Assets.

[RÀNG BUỘC] Đặc điểm phải rút từ bài thật kèm trích dẫn, không mô tả chung chung ("thân thiện, chuyên nghiệp"). Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** dán 3 caption cũ của chị Lan → output tiêu biểu: xưng "em – chị/nàng"; đặc điểm "hay mở đầu bằng câu hỏi đời thường ('Sáng nay soi gương chị thấy gì?')"; từ đặc trưng: "da khỏe từ gốc", "đều màu", "phác đồ riêng"; cấm: "thần thánh", "cam kết 100%", chèn >1 emoji/câu.

### Prompt 4 (Bonus) — Bóc băng buổi tư vấn thành kịch bản chuẩn

```
[VAI TRÒ] Bạn là chuyên gia đóng gói quy trình bán hàng, biến cách tư vấn của nhân viên giỏi nhất thành kịch bản cả đội dùng được.

[BỐI CẢNH] Nhân viên tư vấn giỏi nhất của tôi chốt tốt nhưng làm theo bản năng — nghỉ là mất nghề. Tôi có bản ghi âm/gỡ băng lời kể của bạn ấy về cách tư vấn một ca điển hình.

[NHIỆM VỤ] Từ transcript (bản gỡ băng) dưới đây, chuẩn hóa thành Kịch Bản Tư Vấn v1 gồm: (1) trình tự các bước tư vấn (đặt tên từng bước); (2) câu nói mẫu ở mỗi bước (giữ nguyên những câu đắt giá của người kể — đánh dấu ⭐); (3) các câu hỏi khai thác nhu cầu được dùng; (4) cách xử lý từng phản đối xuất hiện trong transcript; (5) thời điểm & cách chốt; (6) danh sách "khoảnh khắc vàng" — những việc nhỏ tạo niềm tin (VD: cho khách xem ảnh soi da của chính họ). Cuối cùng: liệt kê những gì transcript CHƯA nói rõ, thành câu hỏi để tôi hỏi thêm người đó.

[DỮ LIỆU ĐẦU VÀO] Transcript: {{dán bản gỡ băng — dùng chức năng voice-to-text của điện thoại}}. Bối cảnh ca: {{VD: khách nữ 35 tuổi hỏi liệu trình nám, đã soi da}}.

[ĐỊNH DẠNG ĐẦU RA] Kịch bản 6 phần đánh số; câu nói mẫu trong ngoặc kép; phần cuối "Câu hỏi bổ sung cho [tên nhân viên]".

[RÀNG BUỘC] Không sáng tác thêm bước không có trong transcript (thiếu thì ghi "[chưa có dữ liệu]"). Giữ nguyên văn phong nói của người kể trong các câu mẫu. Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** dán 10' Hương kể → kịch bản 6 bước: chào & hỏi thăm bối cảnh → soi da & giải thích bằng ảnh → kể ca tương tự → trình bày phác đồ theo mốc → xử lý "để em hỏi chồng" (⭐ câu của Hương: "Chị chụp bảng phác đồ này về cho anh xem luôn, em ghi rõ mốc buổi 5 cam kết gì để anh yên tâm ạ") → chốt lịch buổi 1.

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-04: Duy trì Knowledge Base sống**
- **Khi nào:** 15' mỗi chiều thứ Sáu (cố định lịch) + ngay khi có thay đổi giá/chính sách/dịch vụ mới.
- **Ai làm:** Chủ DN hoặc 1 người được giao làm "thủ thư KB" (lễ tân kiêm được).
- **Input:** Câu hỏi mới trong tuần mà FAQ chưa có · thay đổi giá/chính sách · case study mới · nội dung mới đã đăng.
- **Các bước:** (1) Quét inbox tuần, chép câu hỏi chưa có trong FAQ → thêm cặp Q&A mới (dùng Prompt 2 rút gọn); (2) Có thay đổi giá/chính sách → sửa Product Knowledge TRƯỚC, các tài liệu khác trỏ theo (một nguồn sự thật); (3) Khách hoàn thành liệu trình đẹp → xin phép chụp ảnh + 3 câu cảm nhận → thêm vào 09. Case Study; (4) File mới thay file cũ trên RocketAgent (xóa bản cũ khỏi KB, nạp bản mới); (5) Gạch các mục đã xong trong `_Cần bổ sung.md`.
- **Output:** KB luôn khớp thực tế; AI không bao giờ báo giá cũ.
- **Tần suất:** hàng tuần. Quy tắc vàng: "Sửa ở KB trước, mọi nơi khác theo sau."

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Cây đủ 10 thư mục đúng tên chuẩn (5đ) · Product Knowledge phủ 100% dịch vụ đang bán, mỗi dịch vụ đủ 9 trường (10đ) · FAQ & Objection ≥30 cặp (≥20 FAQ + ≥10 objection) (10đ) · 3 tài liệu lõi đã nạp lên RocketAgent/Projects — có ảnh chụp (5đ) |
| Chất lượng & độ sâu | 30 | ≥10 câu hỏi lấy từ inbox thật, giữ văn nói tự nhiên (10đ) · 100% câu trả lời FAQ kết bằng 1 câu dẫn tiếp (10đ) · có mục chống chỉ định/trường hợp từ chối + danh sách "🚨 chuyển người thật" ≥3 tình huống (10đ) |
| Cá nhân hoá vào DN thật | 25 | Giá & chính sách trong FAQ khớp 100% Product Knowledge — mentor đối chiếu chéo 5 cặp ngẫu nhiên, lệch 1 chỗ −5 (15đ) · câu trả lời đúng giọng DN, không phải văn AI mặc định (10đ) |
| Dùng được ngay | 15 | 3 câu test khám sức khỏe: AI trả lời đúng ≥2/3 (đúng giá, không bịa, biết từ chối ca đặc biệt) (10đ) · link thư mục mở được, file đặt tên đúng quy ước (5đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Hai tài liệu ghi 2 giá khác nhau cho cùng dịch vụ (vi phạm "một nguồn sự thật"): −10.
2. FAQ toàn câu tự sáng tác kiểu sách vở, không có câu inbox thật nào: −8.
3. Nạp file ảnh chụp bảng giá/scan mờ lên KB thay vì file chữ: −5.
4. Không có mục chống chỉ định/từ chối (AI sẽ tư vấn cả ca không được phép): −8.
5. Không test sau khi nạp (nộp bài thiếu ảnh test): −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Tôi gần như không có tài liệu gì sẵn — mọi thứ trong đầu tôi. Có làm kịp không?**
→ Đây là tình trạng của 80% học viên, và là lý do Prompt 1 dạng PHỎNG VẤN: bạn chỉ cần trả lời câu hỏi như đang nói chuyện, AI gõ hộ. 2h là đủ cho DN có ≤6 dịch vụ. DN nhiều dịch vụ hơn: hôm nay làm 3 dịch vụ chủ lực, phần còn lại ghi vào `_Cần bổ sung.md`.

**Q2: Nên dùng Google Drive hay đưa hết thẳng lên RocketAgent?**
→ Cả hai, vai trò khác nhau: Drive = kho gốc đầy đủ (cả ảnh, video, file thô); RocketAgent KB = bản chưng cất dạng văn bản cho AI đọc. Quy trình chuẩn: soạn/sửa trên Drive → nạp bản chốt lên RocketAgent.

**Q3: Tài liệu có thông tin nhạy cảm (giá vốn, lương, công thức) có nên nạp cho AI không?**
→ KHÔNG nạp vào KB dùng cho chatbot khách hàng. Quy tắc: KB tuần này chỉ chứa thông tin bạn sẵn sàng cho KHÁCH biết. Dữ liệu nội bộ nhạy cảm để riêng thư mục có khóa, tuần 4 mới bàn đến AI nội bộ với phân quyền.

**Q4: FAQ nên viết câu trả lời dài hay ngắn?**
→ ≤80 từ/câu — khách đọc trên điện thoại. Câu cần giải thích dài (quy trình, cơ chế) → trả lời ngắn + hẹn gửi tài liệu/mời soi da. Nhớ công thức: Trả lời đúng → Đồng cảm/bằng chứng → 1 câu dẫn tiếp.

**Q5: Ảnh trước–sau của khách có đưa vào KB không?**
→ Có — vào 09. Case Study, NHƯNG bắt buộc có đồng ý của khách (xin qua tin nhắn, chụp màn hình lưu kèm). Mô tả ca bằng chữ (tình trạng ban đầu → phác đồ → kết quả mốc nào) để AI kể lại được; ảnh để người thật gửi.

**Q6: Bao lâu thì Knowledge Base "đủ"?**
→ Không bao giờ "đủ" — chỉ có "đủ để chạy". Chuẩn hôm nay: 3 tài liệu lõi + 30 FAQ là đủ cho AI Business Brain Ngày 06. Sau đó KB sống theo SOP-04, mỗi tuần dày thêm một chút.

**Lỗi thường gặp:**
1. **Đổ cả kho file cũ lên RocketAgent cho "nhiều dữ liệu"** — file trùng lặp, bảng giá cũ chồng bảng giá mới → AI trả lời tiền hậu bất nhất. *Phát hiện:* hỏi giá 2 lần ra 2 số. *Sửa:* KB chỉ nạp bản CHỐT; bản cũ vào `_Archive` trên Drive, không nạp.
2. **Viết Product Knowledge bằng ngôn ngữ quảng cáo** ("công nghệ độc quyền đẳng cấp 5 sao") — AI học theo và tư vấn sáo rỗng. *Phát hiện:* đọc 1 khối dịch vụ không tìm thấy đủ 5 con số (giá, phút, buổi, giãn cách, mốc). *Sửa:* tách bạch — Product Knowledge là TÀI LIỆU KỸ THUẬT (số liệu, quy trình); văn quảng cáo đã có ở Offer Ngày 03.
3. **Quên cập nhật khi đổi giá** — chatbot báo giá cũ cho khách thật, mất uy tín. *Phát hiện:* đặt lịch nhắc; mỗi lần in bảng giá mới phải có mục "đã sửa KB chưa?". *Sửa:* áp SOP-04 quy tắc "sửa KB trước, mọi nơi khác theo sau"; giao đích danh 1 người làm thủ thư.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 03 — Offer, Định Vị & Thông Điệp Bán Hàng]] · Ngày sau: [[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]]
- Tài sản hôm nay được dùng lại ở:
	- **Knowledge Base Folder** → xương sống của toàn hệ thống: mọi prompt Ngày 05 lấy dữ liệu từ đây; AI Business Brain (Ngày 06) đứng trên KB này; chatbot (Tuần 3) và AI CSKH (Tuần 4) cùng dùng.
	- **Product Knowledge Document** → nguồn sự thật cho chatbot báo giá (Tuần 3), proposal & báo giá tự động (Tuần 3).
	- **FAQ & Objection Database** → não của chatbot tư vấn (Tuần 3), kịch bản xử lý từ chối (Tuần 3), nội dung chuỗi email/tin nhắn nuôi dưỡng (Tuần 4).
	- **Đặc tả giọng thương hiệu (Bonus)** → khối [GIỌNG] gắn vào mọi prompt content (Ngày 05 & Tuần 2).
	- **Kịch bản tư vấn bóc băng (Bonus)** → nguyên liệu chính của Sales Playbook (Tuần 3) — làm sớm hôm nay, tuần 3 nhàn.
