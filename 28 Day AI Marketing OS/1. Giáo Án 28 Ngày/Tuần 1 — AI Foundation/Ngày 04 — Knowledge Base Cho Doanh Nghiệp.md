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

### 0.4. 10 NHÓM tri thức & bảng mapping vào Vault SME (MỘT chuẩn duy nhất)

**Nguyên tắc hợp nhất — tránh nhầm lẫn của phiên bản cũ:** 10 NHÓM dưới đây là **khung NỘI DUNG** — checklist "não AI cần biết những gì". Chúng **KHÔNG phải 10 thư mục mới phải tạo trên Google Drive**. Nơi lưu vật lý duy nhất là **Vault SME** (framework bàn giao `ai-marketing-system/`) — một nguồn sự thật. Mỗi nhóm có sẵn "địa chỉ nhà" trong vault:

| # | Nhóm tri thức | AI dùng để làm gì | Vị trí thật trong Vault SME |
|---|---|---|---|
| 01 | Business Overview (tổng quan DN) | Hiểu DN là ai, bán gì, cho ai | `00. Business Context/` — Chân Dung Doanh Nghiệp, Business Model Canvas, Baseline & Mục Tiêu |
| 02 | Product & Service (sản phẩm, giá, chính sách) | Trả lời đúng về sản phẩm, không bịa giá | `00. Business Context/Sản Phẩm & Dịch Vụ/` — 1 file/sản phẩm + các file Chính Sách · media gốc → `_Media/` |
| 03 | Customer Avatar (chân dung khách) | Viết content, chatbot, sale script đúng insight | `00. Business Context/MHKD/Phân Khúc Khách Hàng/PK*.md` — avatar + PDFO + journey Ngày 02 |
| 04 | Offer & Sales Message | Tạo bài bán hàng, landing page, pitch | Offer → `00. Business Context/Sản Phẩm & Dịch Vụ/` · Sales Message Pack → `04. Resources/Playbooks/` |
| 05 | Marketing Assets (giọng thương hiệu, content) | Tạo content mới đúng giọng | `00. Business Context/Brand Voice — Giọng Thương Hiệu.md` · content đã đăng → `03. Areas/Brand & Content/` |
| 06 | Sales Assets (kịch bản tư vấn, báo giá) | Tư vấn, follow-up, chốt đơn | `04. Resources/Playbooks/` |
| 07 | FAQ & Objection | Chatbot/CSKH trả lời nhất quán | `04. Resources/Playbooks/FAQ & Objection Database — [Tên DN].md` |
| 08 | SOP & Operation (quy trình vận hành) | Checklist, nhắc việc, onboarding nhân viên | `04. Resources/Playbooks/` (file `SOP — ...`) |
| 09 | Case Study (feedback, chứng thực) | Social proof, landing page, sales deck | `04. Resources/Feedback & Chứng Thực/` |
| 10 | Reports & Metrics (KPI, số liệu) | Đo kết quả, dashboard, CEO Copilot | `03. Areas/Analytics & Reporting/` |

**Google Drive còn vai trò gì?** Chỉ một: **kho media GỐC** (ảnh/video dung lượng lớn, file scan, file thiết kế). Vault nhúng/link tới media đó; mọi tri thức dạng chữ sống trong vault. KHÔNG duy trì cây thư mục tri thức song song trên Drive — hai cây là hai nguồn sự thật, và hai nguồn sự thật là mầm của mọi lỗi "AI báo giá cũ".

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

### 0.6. Ví dụ thực tế (case MSX)

Khách hỏi chatbot:

> "Trà Mẩy Gòm An Giấc giá bao nhiêu?"

Nếu không có Knowledge Base, AI có thể trả lời:

> "Giá trà thảo mộc trên thị trường thường dao động từ vài chục đến vài trăm nghìn một hộp tùy thương hiệu."

Nghe hợp lý nhưng vô dụng — và nguy hiểm nếu AI "đoán" một con số.

Nếu có Knowledge Base, AI trả lời:

> "Dạ Trà Mẩy Gòm An Giấc là trà thảo mộc buổi tối của Mẫu Sơn Xanh, 1 hộp 359.000đ; mua 3 tặng 1 là 1.015.000đ; đơn từ 500.000đ được miễn phí giao hàng ạ. Anh/chị định dùng buổi tối cho mình hay mua làm quà, để em tư vấn đúng hơn ạ?"

Khác biệt là: **câu trả lời có dữ liệu đúng, có chính sách, có bước bán hàng tiếp theo.**

### 0.7. Ghi chú product hoá (nội bộ RocketAI)

→ Đã tách sang [[Ghi Chú Product — AI Business Brain (tách từ giáo án Ngày 04)]] — chiến lược sản phẩm nội bộ RocketAI, không thuộc nội dung giảng dạy.

---

## 1. 🎯 Mục Tiêu Ngày Học

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Knowledge Base trong Vault SME** — 10 nhóm tri thức map đủ vào đúng vị trí vault theo bảng mục 0.4 (một nguồn sự thật); tài sản Ngày 1-3 nằm đúng chỗ; nhóm còn thiếu có `_Cần bổ sung.md` hoặc tag `can-bo-sung`. Google Drive chỉ giữ media gốc.
- ✅ **Data Access & Security Rule (quy tắc truy cập & bảo mật dữ liệu)** — file `00. Business Context/Data Access & Security Rule — [Tên DN].md`: 3 tầng Public/Internal/Restricted, ai được xem/sửa nhóm dữ liệu nào, dữ liệu nào KHÔNG được nạp vào AI. Ví dụ sống: [[Data Access & Security Rule — MSX]].
- ✅ **Product Knowledge Document (tài liệu tri thức sản phẩm)** — chuẩn hóa 100% sản phẩm/dịch vụ đang bán, mỗi sản phẩm 1 file 9 trường trong `Sản Phẩm & Dịch Vụ/` — nguồn sự thật duy nhất về sản phẩm & giá.
- ✅ **FAQ & Objection Database (kho câu hỏi thường gặp & phản đối)** — ≥30 cặp Hỏi-Đáp chuẩn (≥20 FAQ + ≥10 objection kèm câu trả lời mẫu), trong đó ≥10 câu lấy từ inbox thật — lưu tại `04. Resources/Playbooks/`.
- ✅ **3 tài liệu lõi đã nạp lên RocketAgent** (Chân Dung Doanh Nghiệp, Product Knowledge, FAQ & Objection) — kiểm chứng bằng ảnh chụp 3 câu hỏi test.

> **Track công cụ (chọn 1 — KHÔNG làm cả 3):** **A — RocketAgent** (mặc định, đã có tài khoản) · **B — Claude/ChatGPT Projects** (chưa có tài khoản RocketAgent) · **C — Hermes/Jarvis** đọc thẳng vault (gói OS Installed). Nghiệm thu như nhau: ảnh chụp 3 câu test.

**Bonus Output (nâng cao — không bắt buộc, không trừ điểm):**
- ⭐ **Sales Knowledge Base** — kịch bản tư vấn hiện tại (bóc băng cách bạn/nhân viên giỏi nhất đang nói), báo giá mẫu, quy trình chốt → `04. Resources/Playbooks/`.
- ⭐ **Marketing Knowledge Base** — 5-10 bài viết cũ tốt nhất + đặc tả giọng thương hiệu (bổ sung vào `Brand Voice — Giọng Thương Hiệu.md`); thư viện ảnh/video theo chủ đề (media gốc ở Drive, vault giữ link).

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Knowledge Base là gì & vì sao AI cần "bộ não dữ liệu" (5')
- **Ý chính:** AI mặc định biết mọi thứ về thế giới nhưng KHÔNG BIẾT GÌ về doanh nghiệp bạn: giá của bạn, chính sách của bạn, cách bạn xưng hô với khách. Knowledge Base = bộ tài liệu chuẩn để AI "nhập học" về DN. Chất lượng câu trả lời của AI = chất lượng Knowledge Base × chất lượng câu lệnh.
- **Cách giảng:** Analogy nhân viên mới: "Tuyển bạn nhân viên giỏi nhất thế giới, nhưng ngày đầu đi làm không đưa bảng giá, không đưa quy trình — bạn ấy tư vấn kiểu gì? Knowledge Base chính là 'sổ tay nhân viên mới' cho AI."
- **Demo phản chứng 60 giây:** hỏi AI trống (chưa gắn KB) "Trà Mẩy Gòm An Giấc của Mẫu Sơn Xanh giá bao nhiêu?" → AI bịa hoặc né; hỏi lại AI đã gắn KB MSX → trả lời đúng 359.000đ/hộp kèm combo. Đó là lý do của cả ngày hôm nay.

### Khối 2 — Nguyên tắc "một nguồn sự thật" & dữ liệu sạch (7')
- **Ý chính:** Mỗi loại thông tin chỉ sống ở MỘT file (giá chỉ ở Product Knowledge — không rải rác 5 nơi). Dữ liệu AI đọc tốt: file text/doc có tiêu đề rõ, bảng gọn, mỗi mục một ý; dữ liệu AI đọc kém: ảnh chụp bảng giá, file scan, tin nhắn rời rạc, file trùng lặp nhiều phiên bản.
- **Cách giảng:** Quy tắc 4 SẠCH: (1) đúng chỗ — theo bảng mapping 10 nhóm → Vault SME (mục 0.4); (2) đúng tên — `[Tên tài liệu] — [Tên DN/phiên bản/ngày]`; (3) không trùng — bản cũ chuyển vào `05. Archive/` của vault (lưu trữ, không xoá); (4) có chủ — mỗi tài liệu ghi ai chịu trách nhiệm cập nhật.
- **Ví dụ MSX:** Trước chuẩn hóa, giá Trà Mẩy Gòm An Giấc "sống" ở 4 nơi: website, bảng giá in cho hội chợ đợt trước, đoạn tin nhắn Zalo nhân viên gửi khách, trí nhớ mỗi người một số. Hôm nay hợp nhất thành 1 file `Trà Mẩy Gòm An Giấc.md` trong `Sản Phẩm & Dịch Vụ/` — 359.000đ/hộp — mọi nơi khác trỏ về.

### Khối 3 — Đồng bộ & bảo mật: AI đọc đúng, người dùng đúng quyền (5')
- **Ý chính:** Knowledge Base không chỉ là nơi chứa file; nó là "não bộ vận hành" của doanh nghiệp. Não này phải đồng bộ, có phân quyền và có ranh giới dữ liệu. Không phải tài liệu nào cũng nạp lên Agent, và không phải nhân sự nào cũng được sửa nguồn sự thật.
- **Quy tắc 3 tầng dữ liệu:** (1) **Public/khách hàng xem được** — FAQ, bảng giá công khai, thông tin dịch vụ; (2) **Internal/nội bộ** — SOP, script sale, báo cáo KPI, chỉ nhân sự liên quan xem; (3) **Restricted/hạn chế** — dữ liệu cá nhân khách hàng, tài chính chi tiết, hợp đồng, bệnh án/tình trạng nhạy cảm; chỉ đưa vào AI khi đã ẩn thông tin định danh hoặc có quyền rõ.
- **Cách giảng:** Agent làm việc 24/7 nên sai quyền là rủi ro 24/7. Bảo mật không làm hệ thống chậm hơn; bảo mật giúp chủ DN dám dùng AI vào việc thật. Ví dụ sống để chiếu trong lớp: [[Data Access & Security Rule — MSX]] — bảng phân quyền 8 nhóm dữ liệu của một DN thật, kèm mục "dữ liệu được/không được dùng để demo".
- **Cảnh báo pháp lý (Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân):** SĐT, địa chỉ, lịch sử mua, tình trạng sức khỏe của khách là dữ liệu cá nhân được pháp luật bảo vệ — KHÔNG nạp vào AI/chatbot khi chưa ẩn định danh và chưa có sự đồng ý của khách.

### Khối 4 — 10 nhóm tri thức & bảng mapping vào Vault SME (8')
- **Ý chính:** 10 nhóm tri thức là khung NỘI DUNG (não AI cần biết gì): 01 Business Overview · 02 Product & Service · 03 Customer Avatar · 04 Offer & Sales Message · 05 Marketing Assets · 06 Sales Assets · 07 FAQ & Objection · 08 SOP & Operation · 09 Case Study · 10 Reports & Metrics. Nơi lưu vật lý là Vault SME theo bảng mapping mục 0.4 — KHÔNG tạo cây thư mục song song trên Google Drive (Drive chỉ giữ media gốc). Một thông tin = một địa chỉ.
- **Cách giảng:** Tin tốt: nhóm 01, 03, 04 đã XONG từ Ngày 1-3 và đã nằm đúng chỗ — BMC + Chân Dung DN trong `00. Business Context/` (Ngày 01), PDFO + Journey trong `MHKD/Phân Khúc Khách Hàng/` (Ngày 02), Offer trong `Sản Phẩm & Dịch Vụ/` (Ngày 03). Hôm nay xây nhóm 02 và 07 (nặng nhất) + Security Rule; các nhóm còn lại gom được gì bỏ nấy, bổ sung dần (05 đầy lên ở tuần 2, 06 ở tuần 3, 10 ở tuần 4).
- **Mẹo:** nhóm nào chưa có gì → tạo file `_Cần bổ sung.md` tại vị trí tương ứng, hoặc gắn tag `can-bo-sung` vào file thiếu dữ liệu (như vault MSX làm với 3 sản phẩm tạm hết hàng) — đây chính là Improvement List (danh sách cải thiện) cho [[Ngày 06 — AI Business Brain]].

### Khối 5 — Biến tri thức ngầm thành tài liệu: kỹ thuật "AI phỏng vấn + bóc băng" (5')
- **Ý chính:** Tài sản quý nhất của SME không nằm trong file nào — nằm trong ĐẦU người giỏi nhất (cách founder tư vấn, cách nhân viên kỳ cựu xử lý khách khó). Cách rút ra nhanh: (1) để AI phỏng vấn mình từng câu (như Prompt 1 Ngày 01), hoặc (2) ghi âm 1 buổi tư vấn thật/1 lần kể lại → dán transcript (bản gỡ băng) cho AI chuẩn hóa thành tài liệu.
- **Ví dụ RocketAI (dịch vụ tư vấn B2B):** founder RocketAI ghi âm 15' buổi tư vấn thật với chị Mai (chủ Spa ABC, 10 nhân viên) về gói OS, dùng tính năng chuyển giọng nói thành văn bản của điện thoại, dán transcript vào Prompt 4 → ra Kịch Bản Tư Vấn B2B v1: discovery → demo agent → trình bày 3 gói (Transfer 12tr / Installed 25tr / Managed 50tr+) → xử lý "để chị tính lại ngân sách" → chốt lịch audit (Bonus hôm nay, tài sản chính của Tuần 3).

> **Thích ứng ngành khác:** Spa/thẩm mỹ — nhóm 02 bắt buộc có chống chỉ định từng liệu trình kèm câu từ chối khéo (khách mang thai, da đang viêm → hẹn tư vấn trực tiếp); Nha khoa — thêm tài liệu "chỉ định & chống chỉ định" từng dịch vụ vào nhóm 02 (AI phải biết khi nào TỪ CHỐI tư vấn và hẹn bác sĩ); Giáo dục — nhóm 02 gồm lộ trình khóa, giáo trình mẫu, chuẩn đầu ra; nhóm 09 là điểm số/thành tích học viên; Gym/Coaching — nhóm 02 thêm gói PT theo buổi, chính sách bảo lưu (objection số 1). Mọi ngành giữ nguyên khung 10 nhóm + bảng mapping Vault SME.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 03 | Chiếu 1 offer tốt (cam kết đo được) + 1 lỗi "hứa quá tay"/khan hiếm giả. Nhắc: hôm nay bắt đầu dùng RocketAgent — ai chưa có tài khoản quay lại [[Ngày 00 — Install Pack & Baseline]] làm ngay; chưa kịp thì hôm nay đi Track B (Claude/ChatGPT Projects). |
| 25' | Giảng kiến thức trọng tâm | 5 khối mục 2, kèm demo phản chứng 60 giây ở Khối 1. |
| 30' | Demo thực hành live | Dựng Knowledge Base MSX ngay trong vault demo `ai-marketing-system-msx-demo`: tour bảng mapping 10 nhóm → chuẩn hóa Product Knowledge (Trà Mẩy Gòm An Giấc) → sinh FAQ database từ 12 câu FAQ thật trên website → nạp lên RocketAgent → test (kịch bản mục 4). |
| 15' | Học viên làm tại chỗ + Q&A | Học viên mở Vault SME của mình, đối chiếu bảng mapping 10 nhóm: tài sản Ngày 1-3 đã nằm đúng chỗ chưa, nhóm nào còn trống. Gõ vào chat: "Đã đối chiếu đủ 10 nhóm + tên 3 loại tài liệu mình ĐANG CÓ sẵn nhiều nhất". |
| 10' | Giao bài tập | Chiếu deliverable + rubric. Nhấn mạnh: FAQ lấy từ inbox THẬT, không sáng tác. |

**Checklist chuẩn bị của trainer:** tài khoản RocketAgent demo đã đăng nhập, KB trống sẵn sàng nạp · vault demo `ai-marketing-system-msx-demo` mở sẵn (hồ sơ 6 sản phẩm + [[FAQ & Objection Database — MSX]] + [[Data Access & Security Rule — MSX]]) · 12 câu FAQ thật từ website mausonxanh.com + 5 đoạn inbox mẫu MSX cho demo FAQ · quay sẵn video 3' "đăng ký & nạp file lên RocketAgent" phát cho người thao tác chậm · [[Template 4.1 — Knowledge Base 10 Thư Mục & Data Security Rule]], [[Template 4.2 — Product Knowledge Document]], [[Template 4.3 — FAQ & Objection Database]] ghim sẵn.

## 4. 🎬 Kịch Bản Demo (Case chính: 🍵 MSX — vault demo sống)

**Bước 1 (4') — Tour bảng mapping & gom tài sản về đúng chỗ.**
- Làm gì: Mở vault demo `ai-marketing-system-msx-demo`. Chiếu bảng mapping 10 nhóm (mục 0.4) rồi chỉ từng "địa chỉ": BMC + Chân Dung DN nằm sẵn trong `00. Business Context/` (Ngày 01), PDFO/Journey trong `MHKD/Phân Khúc Khách Hàng/` (Ngày 02), Offer trong `Sản Phẩm & Dịch Vụ/` (Ngày 03). Kéo 1 file để lạc chỗ về đúng vị trí làm mẫu.
- Kết quả trông như thế nào: học viên thấy 3/10 nhóm đã đầy từ 3 ngày trước, và thấy rõ hôm nay chỉ phải xây nhóm 02 + 07 + Security Rule.
- Điểm nhấn: "3 ngày qua anh chị đã xây Knowledge Base mà không biết. Hôm nay chỉ dọn nhà và lấp 2 phòng trống."

**Bước 2 (10') — Chuẩn hóa Product Knowledge Document.**
- Làm gì: MSX có 6 sản phẩm nhưng dữ liệu thô rải rác (website, bảng giá, trí nhớ). Paste Prompt 1 — AI phỏng vấn từng sản phẩm một. Trainer trả lời vai chủ DN cho **Trà Mẩy Gòm An Giấc** (359.000đ/hộp · mua 3 tặng 1: 1.015.000đ · 9 thành phần thảo mộc · pha 1 túi 2,5g với 150–200ml nước sôi, uống buổi tối · KHÔNG tư vấn như thuốc ngủ), rồi tua nhanh — chiếu 2 hồ sơ làm sẵn: [[Trà Hoa Sâm Nam]] (369.000đ) và [[Viên Sâm Nam Hà Thủ Ô Mật Ong Vừng]] (599.000đ).
- Kết quả: mỗi sản phẩm 1 file 9 trường trong `Sản Phẩm & Dịch Vụ/` + các file chính sách chung (giao hàng, thanh toán, đổi trả). 3 sản phẩm tạm hết hàng (Viên Sâm Nam Nhàu, 2 loại Chanh Rừng) gắn tag `can-bo-sung` — AI không được bịa giá cho hàng chưa có giá mới.
- Điểm nhấn: mục "Lưu ý an toàn & ranh giới tư vấn" — AI cần biết khi nào nói KHÔNG (phụ nữ có thai/cho con bú, người bệnh nền, trẻ dưới 12 tuổi → khuyên tham khảo bác sĩ, không tư vấn như thuốc). Đây là phần cứu uy tín thương hiệu — và là ranh giới pháp lý với sản phẩm sức khỏe.

**Bước 3 (8') — Sinh FAQ & Objection Database từ câu hỏi thật.**
- Làm gì: Dán 12 câu FAQ thật từ website mausonxanh.com + 5 đoạn inbox mẫu + Product Knowledge + Offer vào Prompt 2. AI gom nhóm câu trùng, sinh 30+ cặp Q&A đúng giọng "em – anh/chị" ấm áp bản địa, mỗi câu kết bằng 1 câu dẫn tiếp. Đối chiếu kết quả với bản chuẩn [[FAQ & Objection Database — MSX]] (21 FAQ + 10 objection thật).
- Kết quả: bảng — # | Câu hỏi/Phản đối | Trả lời chuẩn | Nguồn | Xử lý đặc biệt (khi nào chuyển người thật) — lưu `04. Resources/Playbooks/`.
- Điểm nhấn: câu O08 "Trà này có chữa mất ngủ không?" — câu trả lời chuẩn KHÔNG nhận chữa bệnh ("trà thảo mộc buổi tối, hỗ trợ nhịp thư giãn; mất ngủ kéo dài nên gặp chuyên gia y tế"). FAQ không chỉ để trả lời — mà để DẪN khách đi tiếp một bước và giữ DN an toàn.

**Bước 4 (5') — Nạp 3 tài liệu lõi lên RocketAgent.**
- Làm gì: Vào RocketAgent → mục Knowledge Base → tạo bộ "MSX KB" → upload 3 file (Chân Dung Doanh Nghiệp, Product Knowledge, FAQ & Objection) → chờ hệ thống xử lý xong (trạng thái hiển thị đã nạp).
- Kết quả: 3 tài liệu trạng thái sẵn sàng trong RocketAgent.
- *Theo track:* Track B → tạo 1 Project trong ChatGPT/Claude Projects, upload 3 file tương tự — sang [[Ngày 06 — AI Business Brain]] vẫn chuyển được lên RocketAgent. Track C → Hermes đọc thẳng vault, không cần upload; chỉ cần kiểm tra 3 file nằm đúng vị trí mapping.

**Bước 5 (3') — Test 3 câu "khám sức khỏe" Knowledge Base.**
- Làm gì: Hỏi AI (đã gắn KB): (1) "Trà Mẩy Gòm An Giấc giá bao nhiêu, mua 3 hộp có ưu đãi gì?" — kỳ vọng: đúng 359.000đ/hộp, combo mua 3 tặng 1 là 1.015.000đ, không bịa; (2) "Tôi đang mang thai uống được không?" — kỳ vọng: trả lời theo Lưu ý an toàn — khuyên tham khảo bác sĩ, không khẳng định bừa; (3) "Trà này khác gì trà ngoài chợ?" — kỳ vọng: trả lời bằng USP (nguyên liệu Mẫu Sơn 800–1.541m, OCOP 3★, không chất bảo quản), không nói xấu ai.
- Kết quả: 2/3 câu tốt, 1 câu thiếu → ghi vào `_Cần bổ sung.md`.
- Điểm nhấn: "Test — thiếu — bổ sung — test lại. Vòng lặp này chính là nghề nuôi AI, [[Ngày 06 — AI Business Brain]] làm kỹ."

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core theo template ≤2h)

> ⏱ Mỗi cụm ghi 2 số: **dùng template điền sẵn · lần đầu tự làm**. Tổng Core: **theo template ~95' · lần đầu tự làm có thể tới ~2h35-3h**. Quá giờ: làm theo thứ tự ưu tiên A→E; Bonus không bắt buộc, không trừ điểm.

**Cụm A — Map 10 nhóm & gom tài sản trong Vault SME (⏱ template 15' · lần đầu 25'):**
- [ ] Mở Vault SME, đối chiếu bảng mapping 10 nhóm ([[Template 4.1 — Knowledge Base 10 Thư Mục & Data Security Rule]]): tài sản Ngày 1-3 đã nằm đúng vị trí chưa — lệch thì kéo về đúng chỗ (8')
- [ ] Gom mọi file sẵn có (bảng giá, ảnh, bài viết cũ) vào đúng vị trí mapping — media gốc để Google Drive, vault chỉ giữ chữ + link; nhóm trống tạo `_Cần bổ sung.md` hoặc gắn tag `can-bo-sung` (7')

**Cụm B — Data Access & Security Rule (⏱ template 5' · lần đầu 10'):**
- [ ] Copy khung 3 tầng từ Template 4.1 → điền bản tối thiểu: ai được xem/sửa nhóm dữ liệu nào, dữ liệu nào KHÔNG nạp AI khi chưa ẩn định danh (4')
- [ ] Đánh dấu ít nhất 3 loại dữ liệu Restricted của DN mình (VD: SĐT khách, hồ sơ sức khỏe, hợp đồng, doanh thu chi tiết) (1')

**Cụm C — Product Knowledge Document (⏱ template 30' · lần đầu 50' — Prompt 1 phỏng vấn ~10-15'/sản phẩm lần đầu):**
- [ ] Chạy Prompt 1, trả lời phỏng vấn TỪNG sản phẩm/dịch vụ đang bán — mỗi sản phẩm 1 file 9 trường lưu vào `Sản Phẩm & Dịch Vụ/`; DN >6 sản phẩm: hôm nay làm hết nhóm chủ lực, phần còn lại tag `can-bo-sung` (17')
- [ ] Rà số liệu: giá, quy cách, thời lượng phải đúng 100% — sai 1 số là chatbot báo sai giá cho khách thật (8')
- [ ] Điền chính sách chung (thanh toán, giao hàng, đổi/trả) + mục lưu ý an toàn/trường hợp từ chối (5')

**Cụm D — FAQ & Objection Database (⏱ template 30' · lần đầu 45'):**
- [ ] Mở inbox/Zalo/comment, chép 10-15 câu hỏi thật khách đã hỏi (8')
- [ ] Chạy Prompt 2 (đầu vào: câu hỏi thật + Product Knowledge + Offer + PDFO Map) (8')
- [ ] Rà 30 cặp Q&A: sửa câu "không phải giọng mình", đánh dấu câu phải chuyển người thật, lưu vào `04. Resources/Playbooks/` (14')

**Cụm E — Nạp theo track & test (⏱ template 10' · lần đầu 20'):**
- [ ] Track A: upload 3 tài liệu lõi lên RocketAgent KB · Track B: upload vào ChatGPT/Claude Projects · Track C: kiểm tra 3 file nằm đúng vị trí để Hermes đọc (5')
- [ ] Test 3 câu khám sức khỏe (giá + trường hợp đặc biệt + so sánh); chụp màn hình; câu sai → bổ sung KB → test lại (5')

**Cụm F — Nộp bài (⏱ 5' · 5'):**
- [ ] Nộp `[Tên DN] — Ngày 04 — Knowledge Base Report` vào thread cohort trước 23h59

**Bonus (không bắt buộc):** ghi âm mình/nhân viên giỏi nhất kể lại 1 ca tư vấn điển hình 10-15' → chạy Prompt 4 chuẩn hóa thành kịch bản tư vấn (lưu `04. Resources/Playbooks/`) · gom 5-10 bài viết cũ tốt nhất → chạy Prompt 3 rút "đặc tả giọng thương hiệu" (bổ sung vào `Brand Voice — Giọng Thương Hiệu.md`).

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Dựng Knowledge Base cho doanh nghiệp bạn ngay trong Vault SME: (1) 10 nhóm tri thức map đủ vào đúng vị trí vault (bảng mục 0.4), tài sản Ngày 1-3 nằm đúng chỗ, nhóm thiếu có `_Cần bổ sung.md`/tag `can-bo-sung`, (2) Data Access & Security Rule 3 tầng, (3) Product Knowledge Document phủ 100% sản phẩm/dịch vụ đang bán (9 trường/sản phẩm), (4) FAQ & Objection Database ≥30 cặp (≥20 FAQ + ≥10 objection) trong đó ≥10 câu lấy từ inbox thật, (5) 3 tài liệu lõi đã nạp theo track của bạn + ảnh chụp 3 câu test.

**Deliverable nộp:**
- 1 file tổng hợp: `[Tên DN] — Ngày 04 — Knowledge Base Report` (Google Docs bật "Anyone with the link") gồm: ảnh chụp cây Vault SME sau khi map + nội dung Security Rule + 3 tài liệu lõi (dán nội dung hoặc đính kèm file) + 3 ảnh chụp test + danh sách `_Cần bổ sung`
- Ví dụ: `Mẫu Sơn Xanh — Ngày 04 — Knowledge Base Report`

**Deadline:** 23h59 cùng ngày, nộp vào thread cohort ngày 04. Phiếu thực hành từng bước cho học viên: [[Bài Tập Ngày 4 — Knowledge Base]].

## 7. 📄 Template Đi Kèm

**[[Template 4.1 — Knowledge Base 10 Thư Mục & Data Security Rule]].** Khung 10 nhóm tri thức + bảng mapping vào Vault SME (copy nguyên văn) + quy ước đặt tên file + mẫu file `_Cần bổ sung.md` (3 cột: tài liệu thiếu | ai cung cấp được | hạn bổ sung) + khung Data Access & Security Rule 3 tầng — bảng phân quyền 4 cột: Nhóm dữ liệu | Ai được xem | Ai được sửa | Có được nạp vào Agent không? (`Có / Có sau khi ẩn thông tin / Không`). *Kèm bản mẫu MSX rút từ [[Data Access & Security Rule — MSX]].*

**[[Template 4.2 — Product Knowledge Document]].** Mỗi sản phẩm/dịch vụ 1 file 9 trường: Tên chính thức | Giá & gói (lẻ/combo, đã gồm gì) | Dành cho ai / vấn đề gì | Cách dùng hoặc 1 lần trải nghiệm diễn ra thế nào | Quy cách/lộ trình (thành phần, hoặc số buổi & giãn cách) | Kết quả kỳ vọng theo mốc (viết thận trọng) | Lưu ý an toàn & trường hợp từ chối (kèm câu từ chối khéo) | Chuẩn bị trước – chăm sóc sau / bảo quản & hạn dùng | 3 câu hỏi hay gặp riêng của sản phẩm này. Cuối: khối Chính sách chung (thanh toán, giao hàng, đổi/trả, bảo hành/bảo lưu). *Kèm bản mẫu điền đủ 9 trường: Trà Mẩy Gòm An Giấc (MSX).*

**[[Template 4.3 — FAQ & Objection Database]].** Bảng 5 cột: # | Câu hỏi/Phản đối (nguyên văn giọng khách) | Câu trả lời chuẩn (3-5 câu, kết bằng 1 câu dẫn tiếp) | Nguồn (inbox thật / website / tự bổ sung) | Xử lý đặc biệt (trả lời thẳng / chuyển người thật / cần hỏi lại gì). Chia 2 phần: A. FAQ (≥20) — 4 chủ đề: giá & ưu đãi · sản phẩm, cách dùng & hiệu quả · an toàn & trường hợp đặc biệt · giao nhận, thanh toán & đổi trả; B. Objection (≥10) — đúng các objection trong PDFO Map Ngày 02. Cuối: danh sách "🚨 chuyển người thật". *Kèm bản mẫu trích từ [[FAQ & Objection Database — MSX]] (dữ liệu thật).*

### Trích bản điền mẫu Template 4.3 — MSX (dữ liệu thật)

| # | Câu hỏi/Phản đối | Câu trả lời chuẩn | Nguồn | Xử lý đặc biệt |
|---|---|---|---|---|
| F05 | "Trà Mẩy Gòm An Giấc giá bao nhiêu?" | "Dạ 1 hộp là 359.000đ; mua 3 tặng 1 là 1.015.000đ; mua 6 tặng 2 là 2.029.000đ ạ. Đơn từ 500.000đ được miễn phí giao hàng — anh/chị muốn em lên đơn combo nào ạ?" | Website | Trả lời thẳng + CTA |
| F08 | "Phụ nữ có thai dùng được không?" | "Dạ với phụ nữ có thai/đang cho con bú, MSX khuyên anh/chị tham khảo ý kiến bác sĩ trước khi sử dụng ạ. Em gửi bảng thành phần để anh/chị đối chiếu cùng bác sĩ nhé." | Website | AI không tự tư vấn chắc chắn; khách hỏi sâu → chuyển người thật |
| O01 | "Đắt hơn trà thường quá." | "Dạ đúng là MSX không định vị như trà phổ thông ạ. Khác biệt nằm ở vùng nguyên liệu Mẫu Sơn 800–1.541m, công thức thảo mộc và chứng nhận OCOP 3★. Anh/chị có thể bắt đầu bằng 1 hộp dùng thử trước ạ." | Inbox thật | Từ chối lần 2 → gợi ý sản phẩm hợp ngân sách hơn |
| O08 | "Trà này có chữa mất ngủ không?" | "Dạ MSX không tư vấn sản phẩm như thuốc ạ. Trà Mẩy Gòm là trà thảo mộc buổi tối, vị dịu, hỗ trợ nhịp thư giãn trước khi ngủ. Nếu mất ngủ kéo dài, anh/chị nên gặp chuyên gia y tế — em gửi cách dùng chuẩn để mình tham khảo nhé." | Inbox thật | Ranh giới y tế — không hứa hẹn điều trị |

## 8. 🤖 Prompt Mẫu

### Prompt 1 — AI phỏng vấn để chuẩn hóa Product Knowledge

```
[VAI TRÒ] Bạn là chuyên gia quản trị tri thức (knowledge management) cho SME, giỏi đặt câu hỏi để rút toàn bộ thông tin sản phẩm/dịch vụ từ chủ doanh nghiệp ra thành tài liệu chuẩn.

[BỐI CẢNH] Tôi cần xây Product Knowledge Document — nguồn sự thật duy nhất về mọi sản phẩm/dịch vụ, để nạp cho AI trả lời khách. Thông tin hiện nằm rải rác trong đầu tôi, website, bảng giá cũ và tin nhắn.

[NHIỆM VỤ] Phỏng vấn tôi TỪNG SẢN PHẨM/DỊCH VỤ MỘT. Với mỗi cái, hỏi lần lượt 9 mục (mỗi lần 1 câu, chờ tôi trả lời): (1) tên chính thức; (2) giá — lẻ/combo/gói, đã gồm và chưa gồm gì; (3) dành cho ai, giải quyết vấn đề gì; (4) cách dùng hoặc 1 lần trải nghiệm diễn ra thế nào — liều lượng/các bước, thời lượng; (5) quy cách hoặc lộ trình — thành phần/khối lượng, hoặc số buổi & giãn cách; (6) kết quả kỳ vọng theo mốc thời gian — nhắc tôi nếu tôi nói quá tuyệt đối; (7) lưu ý an toàn — trường hợp KHÔNG nên dùng / phải từ chối hoặc khuyên gặp chuyên gia; (8) chuẩn bị trước – chăm sóc sau, hoặc cách bảo quản & hạn dùng; (9) 3 câu khách hay hỏi nhất riêng về sản phẩm này. Xong 1 sản phẩm, xuất khối tài liệu chuẩn rồi hỏi "còn sản phẩm nào không?". Kết thúc: hỏi thêm khối chính sách chung (thanh toán, giao hàng, đổi/trả, bảo hành/bảo lưu) và xuất toàn bộ.

[DỮ LIỆU ĐẦU VÀO] Danh sách sản phẩm/dịch vụ của tôi: {{liệt kê tên + giá nếu nhớ}}. Dữ liệu thô sẵn có: {{dán nội dung website/bảng giá cũ/ghi chú nếu có}}.

[ĐỊNH DẠNG ĐẦU RA] Mỗi sản phẩm 1 khối 9 đề mục thống nhất — để tôi lưu mỗi khối thành 1 file riêng trong `00. Business Context/Sản Phẩm & Dịch Vụ/`; cuối cùng khối "Chính sách chung" (lưu thành các file chính sách riêng); toàn bộ dạng văn bản có tiêu đề rõ (không cần bảng phức tạp) để nạp vào Knowledge Base.

[RÀNG BUỘC] Tuyệt đối không tự điền số liệu tôi chưa cung cấp — thiếu thì ghi "[cần bổ sung]". Mục 6: tự động viết lại các cụm tuyệt đối ("hết hẳn", "khỏi 100%", "chữa dứt điểm") thành mô tả thận trọng có mốc. Tiếng Việt.
```

**Ví dụ đã điền (MSX):** `{{Danh sách sản phẩm}}` → "1) Trà Mẩy Gòm An Giấc 359.000đ/hộp; 2) Trà Hoa Sâm Nam 369.000đ/hộp; 3) Viên Sâm Nam Hà Thủ Ô Mật Ong Vừng 599.000đ/hộp; 4) Viên Sâm Nam Nhàu — tạm hết hàng; 5) Chanh Rừng Mật Ong — tạm hết hàng; 6) Chanh Rừng Ngâm Muối — tạm hết hàng." `{{Dữ liệu thô}}` → dán mô tả sản phẩm từ website mausonxanh.com + ghi chú "combo mua 3 tặng 1, mua 6 tặng 2". Kết quả: 3 hồ sơ đủ giá + 3 hồ sơ gắn `[cần bổ sung]` — AI không bịa giá cho hàng tạm hết.

### Prompt 2 — Sinh FAQ & Objection Database từ inbox thật

```
[VAI TRÒ] Bạn là trưởng nhóm chăm sóc khách hàng cho SME, chuyên xây kho câu trả lời chuẩn cho đội tư vấn và chatbot.

[BỐI CẢNH] Tôi cần FAQ & Objection Database ≥30 cặp Hỏi-Đáp để: nhân viên trả lời thống nhất, và nạp cho AI/chatbot. Tôi có sẵn câu hỏi thật từ inbox và các tài liệu chuẩn.

[NHIỆM VỤ] (1) Gom nhóm các câu hỏi thật tôi cung cấp (câu trùng ý gộp làm một, giữ cách diễn đạt tự nhiên nhất). (2) Bổ sung cho đủ ≥20 FAQ phủ 4 chủ đề: giá & ưu đãi · sản phẩm, cách dùng & hiệu quả · an toàn & trường hợp đặc biệt · giao nhận, thanh toán & đổi trả (ngành dịch vụ: lịch hẹn & địa điểm). (3) Viết ≥10 câu xử lý objection dựa đúng danh sách phản đối trong bản đồ tâm lý. (4) Mỗi câu trả lời: 3-5 câu, đúng số liệu từ Product Knowledge, đúng giọng thương hiệu, kết bằng 1 câu dẫn khách đi tiếp (đặt lịch/để lại số/nhận tài liệu). (5) Đánh dấu các câu AI/nhân viên mới KHÔNG được tự trả lời mà phải chuyển người phụ trách (khiếu nại, tình trạng y khoa phức tạp, đòi hoàn tiền).

[DỮ LIỆU ĐẦU VÀO] Câu hỏi thật từ inbox: {{dán 10-15 câu nguyên văn}}. Product Knowledge Document: {{dán}}. Core Offer: {{dán phần chính}}. Objection từ PDFO Map: {{dán}}. Giọng thương hiệu: {{VD MSX: ấm áp, bản địa, xưng "em" — gọi khách "anh/chị", không nói như thuốc chữa bệnh}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng 5 cột: # | Câu hỏi/Phản đối | Câu trả lời chuẩn | Nguồn (inbox thật/website/bổ sung) | Xử lý đặc biệt. Phần A: FAQ theo 4 chủ đề. Phần B: Objection. Cuối: danh sách "🚨 Bắt buộc chuyển người thật".

[RÀNG BUỘC] Giá và chính sách phải khớp 100% Product Knowledge — nếu 2 nguồn tôi đưa mâu thuẫn, dừng lại hỏi tôi. Không hứa hẹn y khoa tuyệt đối. Câu trả lời không dài quá 80 từ (khách đọc trên điện thoại). Tiếng Việt.
```

**Ví dụ đã điền (MSX):** `{{Câu hỏi thật}}` → "1) 'trà này có chất bảo quản không' · 2) 'phụ nữ có thai dùng được không' · 3) 'bao lâu nhận được hàng' · 4) 'có COD không em' · 5) 'phí ship bao nhiêu' · 6) 'uống bao lâu thì thấy dễ ngủ hơn' · 7) 'có giảm giá không' · 8) 'đắt hơn trà thường quá' · 9) 'trà này có chữa mất ngủ không' · 10) 'mua làm quà có hộp đẹp không' · 11) 'lấy sỉ được không' · 12) 'nguyên liệu lấy từ đâu, có sạch không'..." — đúng 12 câu thật từ website + inbox MSX; kết quả chuẩn để đối chiếu: [[FAQ & Objection Database — MSX]].

### Prompt 3 (Bonus) — Rút "đặc tả giọng thương hiệu" từ bài viết cũ

```
[VAI TRÒ] Bạn là chuyên gia phân tích văn phong thương hiệu (brand voice analyst).

[BỐI CẢNH] Tôi muốn mọi nội dung AI viết sau này đều đúng "giọng" của tôi. Tôi có các bài viết/tin nhắn cũ do chính tôi viết được khách phản hồi tốt.

[NHIỆM VỤ] Phân tích các mẫu văn bản dưới đây và xuất "Đặc tả giọng thương hiệu" gồm: (1) xưng hô với khách; (2) 5 đặc điểm giọng văn (kèm ví dụ trích từ bài của tôi); (3) 10 từ/cụm từ đặc trưng tôi hay dùng; (4) 5 điều KHÔNG BAO GIỜ viết (từ sáo rỗng, kiểu câu không hợp); (5) 1 đoạn văn mẫu 80-100 từ viết đúng giọng đó về chủ đề tôi chỉ định — để làm mẫu đối chiếu.

[DỮ LIỆU ĐẦU VÀO] 3-5 bài viết/tin nhắn cũ tốt nhất của tôi: {{dán nguyên văn}}. Chủ đề đoạn mẫu: {{VD: nhắc khách pha Trà Mẩy Gòm An Giấc đúng cách trong tuần đầu}}.

[ĐỊNH DẠNG ĐẦU RA] Tài liệu 5 mục, ≤350 từ, tiêu đề "Đặc Tả Giọng Thương Hiệu — [Tên DN]" — bổ sung vào file `00. Business Context/Brand Voice — Giọng Thương Hiệu.md` (nhóm 05).

[RÀNG BUỘC] Đặc điểm phải rút từ bài thật kèm trích dẫn, không mô tả chung chung ("thân thiện, chuyên nghiệp"). Tiếng Việt.
```

**Ví dụ đã điền (MSX):** dán 3 caption tốt nhất trên fanpage Mẫu Sơn Xanh → output tiêu biểu: xưng "em – anh/chị"; đặc điểm "hay mở đầu bằng hình ảnh vùng cao ('Sương sớm trên đỉnh Mẫu Sơn...')"; từ đặc trưng: "dược liệu vùng cao Mẫu Sơn", "thảo mộc tự nhiên", "đồng hành cùng thói quen mỗi ngày", "lối vào cuộc sống xanh"; cấm: "thần dược", "chữa khỏi", "cam kết 100%", chèn >3 emoji/bài.

### Prompt 4 (Bonus) — Bóc băng buổi tư vấn thành kịch bản chuẩn

```
[VAI TRÒ] Bạn là chuyên gia đóng gói quy trình bán hàng, biến cách tư vấn của nhân viên giỏi nhất thành kịch bản cả đội dùng được.

[BỐI CẢNH] Nhân viên tư vấn giỏi nhất của tôi chốt tốt nhưng làm theo bản năng — nghỉ là mất nghề. Tôi có bản ghi âm/gỡ băng lời kể của bạn ấy về cách tư vấn một ca điển hình.

[NHIỆM VỤ] Từ transcript (bản gỡ băng) dưới đây, chuẩn hóa thành Kịch Bản Tư Vấn v1 gồm: (1) trình tự các bước tư vấn (đặt tên từng bước); (2) câu nói mẫu ở mỗi bước (giữ nguyên những câu đắt giá của người kể — đánh dấu ⭐); (3) các câu hỏi khai thác nhu cầu được dùng; (4) cách xử lý từng phản đối xuất hiện trong transcript; (5) thời điểm & cách chốt; (6) danh sách "khoảnh khắc vàng" — những việc nhỏ tạo niềm tin (VD: demo kết quả ngay trên thiết bị của khách). Cuối cùng: liệt kê những gì transcript CHƯA nói rõ, thành câu hỏi để tôi hỏi thêm người đó.

[DỮ LIỆU ĐẦU VÀO] Transcript: {{dán bản gỡ băng — dùng chức năng voice-to-text của điện thoại}}. Bối cảnh ca: {{VD: chủ spa 10 nhân viên hỏi gói cài đặt AI, đã xem demo}}.

[ĐỊNH DẠNG ĐẦU RA] Kịch bản 6 phần đánh số; câu nói mẫu trong ngoặc kép; phần cuối "Câu hỏi bổ sung cho [tên nhân viên]".

[RÀNG BUỘC] Không sáng tác thêm bước không có trong transcript (thiếu thì ghi "[chưa có dữ liệu]"). Giữ nguyên văn phong nói của người kể trong các câu mẫu. Tiếng Việt.
```

**Ví dụ đã điền (RocketAI — dịch vụ tư vấn B2B):** dán 15' founder RocketAI kể lại buổi tư vấn chị Mai (chủ Spa ABC, 10 nhân viên, ~500tr/tháng) → kịch bản 6 bước: hỏi thăm tình hình content & CSKH hiện tại → đo "số giờ/tuần đang đốt vào việc lặp lại" → demo agent trả lời inbox ngay trên điện thoại của khách → trình bày 3 gói (Transfer 12tr / Installed 25tr / Managed 50tr+) theo mức "tự làm – làm cùng – làm hộ" → xử lý "để chị tính lại ngân sách" (⭐ câu đắt: "Mình không cần quyết hôm nay chị ạ — em gửi bản audit 3 điểm rò rỉ doanh thu của spa mình, chị xem thấy đúng thì mình nói chuyện tiếp") → chốt lịch buổi audit 30'.

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-04: Duy trì Knowledge Base sống**
- **Khi nào:** 15' mỗi chiều thứ Sáu (cố định lịch) + ngay khi có thay đổi giá/chính sách/dịch vụ mới.
- **Ai làm:** Chủ DN hoặc 1 người được giao làm "thủ thư KB" (nhân viên CSKH/lễ tân kiêm được).
- **Input:** Câu hỏi mới trong tuần mà FAQ chưa có · thay đổi giá/chính sách · case study mới · nội dung mới đã đăng.
- **Các bước:** (1) Quét inbox tuần, chép câu hỏi chưa có trong FAQ → thêm cặp Q&A mới vào `04. Resources/Playbooks/` (dùng Prompt 2 rút gọn); (2) Có thay đổi giá/chính sách → sửa hồ sơ sản phẩm trong `Sản Phẩm & Dịch Vụ/` TRƯỚC, các tài liệu khác trỏ theo (một nguồn sự thật); (3) Khách có kết quả/feedback tốt → xin phép lưu lại (chụp màn hình tin nhắn đồng ý) + 3 câu cảm nhận → thêm vào `04. Resources/Feedback & Chứng Thực/`; (4) File mới thay file cũ trên RocketAgent (xóa bản cũ khỏi KB, nạp bản mới — Track C: Hermes tự đọc bản mới trong vault); (5) Gạch mục đã xong trong `_Cần bổ sung.md`, gỡ tag `can-bo-sung` khi file đủ dữ liệu.
- **Output:** KB luôn khớp thực tế; AI không bao giờ báo giá cũ.
- **Tần suất:** hàng tuần. Quy tắc vàng: "Sửa ở KB trước, mọi nơi khác theo sau."

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | 10 nhóm tri thức map đủ vào Vault SME đúng bảng mapping, tài sản Ngày 1-3 đúng chỗ, nhóm thiếu có đánh dấu (6đ) · Data Access & Security Rule 3 tầng, ≥3 dữ liệu Restricted (6đ) · Product Knowledge phủ 100% sản phẩm đang bán, mỗi sản phẩm đủ 9 trường (6đ) · FAQ & Objection ≥30 cặp (≥20 FAQ + ≥10 objection) (6đ) · 3 tài liệu lõi đã nạp theo track — có ảnh chụp (6đ) |
| Chất lượng & độ sâu | 30 | ≥10 câu hỏi lấy từ inbox thật, giữ văn nói tự nhiên (10đ) · 100% câu trả lời FAQ kết bằng 1 câu dẫn tiếp (10đ) · có mục lưu ý an toàn/trường hợp từ chối + danh sách "🚨 chuyển người thật" ≥3 tình huống (10đ) |
| Cá nhân hoá vào DN thật | 25 | Giá & chính sách trong FAQ khớp 100% Product Knowledge — mentor đối chiếu chéo 5 cặp ngẫu nhiên, lệch 1 chỗ −5 (15đ) · câu trả lời đúng giọng DN, không phải văn AI mặc định (10đ) |
| Dùng được ngay | 15 | 3 câu test khám sức khỏe: AI trả lời đúng ≥2/3 (đúng giá, không bịa, biết từ chối/chuyển ca đặc biệt) (10đ) · file nằm đúng vị trí mapping, đặt tên đúng quy ước, report mở được (5đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Hai tài liệu ghi 2 giá khác nhau cho cùng sản phẩm/dịch vụ (vi phạm "một nguồn sự thật"): −10.
2. FAQ toàn câu tự sáng tác kiểu sách vở, không có câu inbox thật nào: −8.
3. Nạp file ảnh chụp bảng giá/scan mờ lên KB thay vì file chữ: −5.
4. Không có mục lưu ý an toàn/trường hợp từ chối (AI sẽ tư vấn cả ca không được phép — với sản phẩm sức khỏe còn là rủi ro pháp lý): −8.
5. Không test sau khi nạp (nộp bài thiếu ảnh test): −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Tôi gần như không có tài liệu gì sẵn — mọi thứ trong đầu tôi. Có làm kịp không?**
→ Đây là tình trạng của 80% học viên, và là lý do Prompt 1 dạng PHỎNG VẤN: bạn chỉ cần trả lời câu hỏi như đang nói chuyện, AI gõ hộ. Lần đầu mỗi sản phẩm mất ~10-15'; DN có ≤6 sản phẩm/dịch vụ là kịp trong buổi tối. Nhiều hơn: hôm nay làm nhóm chủ lực, phần còn lại tag `can-bo-sung`.

**Q2: Vault SME, Google Drive, RocketAgent — cái nào là "kho chính"?**
→ MỘT nguồn sự thật duy nhất: **Vault SME** — mọi tri thức dạng chữ soạn/sửa tại đây, theo bảng mapping mục 0.4. **Google Drive** chỉ giữ media GỐC (ảnh/video nặng, file scan) — vault link tới. **RocketAgent KB** = bản CHỐT nạp cho AI đọc. Quy trình chuẩn: sửa trong vault → nạp bản chốt lên RocketAgent. Không bao giờ sửa trực tiếp trên RocketAgent rồi quên sửa vault.

**Q3: Tài liệu có thông tin nhạy cảm (giá vốn, lương, công thức) có nên nạp cho AI không?**
→ KHÔNG nạp vào KB dùng cho chatbot khách hàng. Quy tắc: KB tuần này chỉ chứa thông tin bạn sẵn sàng cho KHÁCH biết (tầng Public trong Security Rule). Dữ liệu nội bộ nhạy cảm đánh dấu Internal/Restricted, tuần 4 mới bàn đến AI nội bộ với phân quyền.

**Q4: FAQ nên viết câu trả lời dài hay ngắn?**
→ ≤80 từ/câu — khách đọc trên điện thoại. Câu cần giải thích dài (quy trình, cơ chế) → trả lời ngắn + hẹn gửi tài liệu/mời tư vấn. Nhớ công thức: Trả lời đúng → Đồng cảm/bằng chứng → 1 câu dẫn tiếp.

**Q5: Ảnh/feedback thật của khách có đưa vào KB không?**
→ Có — vào `04. Resources/Feedback & Chứng Thực/`, NHƯNG bắt buộc có đồng ý của khách (xin qua tin nhắn, chụp màn hình lưu kèm — đây cũng là yêu cầu của Nghị định 13/2023/NĐ-CP về dữ liệu cá nhân). Mô tả ca bằng chữ (bối cảnh → sản phẩm/phác đồ dùng → cảm nhận theo mốc) để AI kể lại được; ảnh gốc để `_Media/`/Drive, người thật gửi khi cần.

**Q6: Bao lâu thì Knowledge Base "đủ"?**
→ Không bao giờ "đủ" — chỉ có "đủ để chạy". Chuẩn hôm nay: 3 tài liệu lõi + 30 FAQ là đủ cho [[Ngày 06 — AI Business Brain]]. Sau đó KB sống theo SOP-04, mỗi tuần dày thêm một chút.

**Lỗi thường gặp:**
1. **Đổ cả kho file cũ lên RocketAgent cho "nhiều dữ liệu"** — file trùng lặp, bảng giá cũ chồng bảng giá mới → AI trả lời tiền hậu bất nhất. *Phát hiện:* hỏi giá 2 lần ra 2 số. *Sửa:* KB chỉ nạp bản CHỐT; bản cũ vào `05. Archive/` của vault, không nạp.
2. **Viết Product Knowledge bằng ngôn ngữ quảng cáo** ("công nghệ độc quyền đẳng cấp 5 sao") — AI học theo và tư vấn sáo rỗng. *Phát hiện:* đọc 1 khối sản phẩm không tìm thấy đủ 5 con số (giá, quy cách, liều/buổi, thời gian, mốc). *Sửa:* tách bạch — Product Knowledge là TÀI LIỆU KỸ THUẬT (số liệu, quy trình); văn quảng cáo đã có ở Offer Ngày 03.
3. **Quên cập nhật khi đổi giá** — chatbot báo giá cũ cho khách thật, mất uy tín. *Phát hiện:* đặt lịch nhắc; mỗi lần in bảng giá mới phải có mục "đã sửa KB chưa?". *Sửa:* áp SOP-04 quy tắc "sửa KB trước, mọi nơi khác theo sau"; giao đích danh 1 người làm thủ thư.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 03 — Offer, Định Vị & Thông Điệp Bán Hàng]] · Ngày sau: [[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]]
- Tài sản hôm nay được dùng lại ở:
	- **Knowledge Base trong Vault SME** → xương sống của toàn hệ thống: mọi prompt Ngày 05 lấy dữ liệu từ đây; [[Ngày 06 — AI Business Brain]] đứng trên KB này; chatbot (Tuần 3) và AI CSKH (Tuần 4) cùng dùng.
	- **Product Knowledge Document** → nguồn sự thật cho chatbot báo giá (Tuần 3), proposal & báo giá tự động (Tuần 3).
	- **FAQ & Objection Database** → não của chatbot tư vấn (Tuần 3), kịch bản xử lý từ chối (Tuần 3), nội dung chuỗi email/tin nhắn nuôi dưỡng (Tuần 4).
	- **Đặc tả giọng thương hiệu (Bonus)** → khối [GIỌNG] gắn vào mọi prompt content (Ngày 05 & Tuần 2).
	- **Kịch bản tư vấn bóc băng (Bonus)** → nguyên liệu chính của Sales Playbook (Tuần 3) — làm sớm hôm nay, tuần 3 nhàn.
