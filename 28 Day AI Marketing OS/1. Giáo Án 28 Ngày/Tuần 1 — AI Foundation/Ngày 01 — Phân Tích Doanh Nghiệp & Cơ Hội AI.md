---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 1
day: 1
core-output: "Business Model Canvas 9 khối · Business Snapshot 1 trang · Business Process Map · Top 10 AI Use Cases · Mục tiêu 28 ngày (1 mục tiêu chính + 3 chỉ số)"
---

# Ngày 01 — Business Model Canvas & Cơ Hội AI

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Chạy `/mo-hinh-kinh-doanh` — Claude phỏng vấn 9 khối BMC rồi TỰ SINH Chân Dung Doanh Nghiệp, Business Model Canvas + `.canvas`, và từng file PK/GT vào `00. Business Context/`. Prompt mẫu bên dưới là phương án B khi chưa cài xong vault.

> Hôm nay bạn dựng "bản đồ hệ gen" của doanh nghiệp: Business Model Canvas 9 khối, mô hình khách hàng-doanh thu-kênh-vận hành, dòng chảy từ marketing đến chăm sóc khách, và 10 đầu việc sẽ được AI hóa trong 28 ngày tới.

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay (không phải "hiểu", mà là file thật):

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Business Model Canvas (BMC) 9 khối** — bản đồ mô hình kinh doanh: phân khúc khách hàng, giá trị cốt lõi, kênh, quan hệ khách hàng, dòng doanh thu, nguồn lực, hoạt động, đối tác, chi phí.
- ✅ **Business Snapshot (bản chụp doanh nghiệp)** — 1 trang mô tả mô hình kinh doanh hiện tại: bán gì, cho ai, giá bao nhiêu, kênh nào, đau ở đâu.
- ✅ **Business Process Map (sơ đồ quy trình kinh doanh)** — dòng chảy khách hàng từ lúc biết đến DN → tư vấn → mua → chăm sóc → mua lại, kèm ghi chú "điểm nghẽn" ở từng bước.
- ✅ **Top 10 AI Use Cases (10 đầu việc ưu tiên AI hóa)** — chấm điểm bằng khung ICE và xếp hạng.
- ✅ **Mục tiêu 28 ngày** — 1 mục tiêu chính + 3 chỉ số đo được.

**Bonus Output (nâng cao — làm nếu còn thời gian):**
- ⭐ **AI Opportunity Map (bản đồ cơ hội AI) đầy đủ** — quét cả 5 khu vực (Marketing, Sales, CSKH, Vận hành, Đo lường), mỗi khu vực ≥3 cơ hội.
- ⭐ Ước lượng chi phí thời gian hiện tại (giờ/tuần) cho từng đầu việc sẽ AI hóa.

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Tổng quan AI Marketing & Sales OS™ (5')
- **Ý chính:** Sau 28 ngày, học viên không "biết AI" mà SỞ HỮU một hệ điều hành: Marketing → Thu lead (khách hàng tiềm năng) → Tư vấn → Chốt sale → Chăm sóc → Upsell (bán thêm) → Đo lường → Tối ưu.
- **Cách giảng:** Chiếu sơ đồ vòng tròn 8 bước. Analogy: "AI OS giống như tuyển một đội nhân viên số làm việc 24/7 — nhưng nhân viên mới thì phải đào tạo. 28 ngày này là 28 ngày đào tạo đội nhân viên đó bằng chính dữ liệu doanh nghiệp của anh chị."
- **Ví dụ Sen Spa:** Chị Lan chủ Sen Spa có 6 nhân viên, không ai chuyên marketing. AI OS sẽ đóng vai: 1 nhân viên content, 1 nhân viên trực page, 1 trợ lý sale, 1 nhân viên CSKH — tổng lương 0 đồng.

### Khối 2 — Business Model Canvas: bản đồ hệ gen của doanh nghiệp (8')
- **Ý chính:** Trước khi dựng Agent, AI phải hiểu doanh nghiệp kiếm tiền bằng mô hình nào. BMC 9 khối giúp gom toàn bộ logic kinh doanh vào một trang: bán cho ai, hứa giá trị gì, đi qua kênh nào, quan hệ ra sao, thu tiền từ đâu, cần nguồn lực/hoạt động/đối tác nào, và chi phí nằm ở đâu.
- **Cách giảng:** BMC là "hồ sơ nhân sự đầu vào" cho toàn bộ đội Agent. Nếu BMC mơ hồ, Content Agent viết lệch khách; Sales Agent tư vấn sai offer; Data Agent đo sai chỉ số. Nếu BMC rõ, mọi Agent dùng cùng một bản sự thật.
- **Ví dụ Sen Spa:** Customer Segments = nữ 28-45 có nám/mụn/lão hóa; Value Proposition = phác đồ da cá nhân hóa + theo dõi bằng ảnh/soi da; Channels = Facebook + giới thiệu + Zalo; Revenue Streams = buổi lẻ, liệu trình, gói duy trì; Key Activities = tư vấn, trị liệu, follow-up, chăm sóc sau liệu trình.

### Khối 3 — Tư duy AI First Business (5')
- **Ý chính:** Không hỏi "AI làm được gì?" mà hỏi "Việc gì trong DN của tôi đang lặp lại, tốn thời gian, phụ thuộc con người — và có dữ liệu để AI học?"
- **Cách giảng:** Công thức nhận diện việc nên AI hóa = **Lặp lại + Có quy luật + Có dữ liệu mẫu**. Việc KHÔNG nên AI hóa ngay: việc cần chạm tay khách (soi da, trị liệu), việc pháp lý, quyết định chiến lược.
- **Ví dụ Sen Spa:** Trả lời inbox "giá bao nhiêu chị ơi" lặp lại 30 lần/tuần → AI hóa được. Soi da trực tiếp cho khách → không.

### Khối 4 — Nhìn doanh nghiệp như một hệ thống + 5 khu vực AI tác động (7')
- **Ý chính:** DN = chuỗi các trạm mà khách hàng đi qua. Doanh thu rơi rớt ở TRẠM YẾU NHẤT, không phải trạm mạnh nhất. 5 khu vực AI tác động: (1) Marketing, (2) Sales, (3) Chăm sóc khách hàng, (4) Vận hành nội bộ, (5) Đo lường & ra quyết định.
- **Cách giảng:** Analogy đường ống nước: "Nước (khách) chảy qua 5 đoạn ống. Vá đoạn thủng to nhất trước." Vẽ live sơ đồ ống của Sen Spa và hỏi cả lớp: "Đoạn nào đang thủng?"
- **Ví dụ Sen Spa:** Ống Marketing nhỏ giọt (lead ít), ống Sales phụ thuộc 1 bạn tư vấn giỏi tên Hương (Hương nghỉ = tắt nước), ống Follow-up (theo dõi tiếp) thủng hoàn toàn (khách hỏi giá xong không ai nhắn lại).

### Khối 5 — Lập bản đồ cơ hội AI & khung ưu tiên ICE (5')
- **Ý chính:** Liệt kê rộng (mọi việc có thể AI hóa) rồi lọc hẹp bằng khung **ICE**: **Impact (tác động** đến doanh thu/thời gian**)** · **Confidence (độ tự tin** làm được**)** · **Ease (độ dễ** triển khai**)** — mỗi tiêu chí chấm 1-5, tổng tối đa 15.
- **Cách giảng:** Không chọn theo cảm hứng. Quy tắc: trong Top 10 phải có ≥4 use case thuộc Marketing/Sales (vì đây là chương trình Marketing & Sales OS), và ≥7 use case nằm trong lộ trình 28 ngày (content, chatbot, kịch bản sale, follow-up, dashboard...).
- **Ví dụ Sen Spa:** "AI trả lời inbox báo giá" = I:5, C:4, E:4 → 13 điểm, xếp #1. "AI phân tích ảnh da khách" = I:3, C:2, E:1 → 6 điểm, loại khỏi Top 10.

> **Thích ứng ngành khác:** Nha khoa — điểm nghẽn thường ở "khách sợ đau, cần tư vấn kỹ trước khi đến"; Giáo dục — nghẽn ở "phụ huynh cần nói chuyện nhiều lần mới chốt"; Gym/Coaching — nghẽn ở "khách đăng ký trải nghiệm rồi biến mất". Cùng khung 5 khu vực + ICE, chỉ thay dữ liệu.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + khởi động cohort | Giới thiệu lộ trình 28 ngày, quy ước nộp bài (23h59, thread cohort), quy ước Demo Day. Hỏi nhanh 3 học viên: "DN anh chị đang đau nhất ở đâu?" — ghi lên bảng làm chất liệu. |
| 25' | Giảng kiến thức trọng tâm | 5 khối ở mục 2, đúng thứ tự. Luôn neo về ví dụ Sen Spa. |
| 30' | Demo thực hành live | Làm thật BMC + Business Snapshot + Process Map + Top 10 cho Sen Spa bằng prompt mẫu (kịch bản mục 4). Chiếu màn hình, chạy prompt thật. |
| 15' | Học viên làm tại chỗ + Q&A | Học viên mở Template 1.0, điền nhanh 2 khối đầu của BMC (Customer Segments + Value Proposition). Trainer + mentor đảo phòng/đọc chat sửa nhanh. |
| 10' | Giao bài tập | Chiếu đề bài + deliverable + rubric (mục 6, 10). Nhấn mạnh: Core ≤2h, đừng cầu toàn AI Opportunity Map. |

**Checklist chuẩn bị của trainer (trước buổi live 30'):**
- [ ] Slide: sơ đồ vòng tròn 8 bước AI OS · sơ đồ "đường ống nước" 5 khu vực · dữ liệu nền Sen Spa · khung ICE.
- [ ] Tab trình duyệt mở sẵn: RocketAgent (hoặc ChatGPT) đã đăng nhập, 6 prompt mẫu để trong file text sẵn sàng copy.
- [ ] Chạy thử trước cả 6 prompt với dữ liệu Sen Spa 1 lần — lưu lại output tốt để phòng khi live AI trả kết quả kém thì chiếu bản dự phòng.
- [ ] Link 5 template (quyền xem + tạo bản sao) dán sẵn vào chat/thread cohort.
- [ ] Mở thread "Ngày 01 — Nộp bài" trong cohort, ghim quy ước đặt tên file.

**Nhịp điều phối cần giữ:**
- Phần demo (30') là trái tim buổi học — nếu cháy giờ, cắt Khối 1-2 phần giảng (đã có trong tài liệu), KHÔNG cắt demo.
- Khi học viên làm tại chỗ (15'), yêu cầu mỗi người gõ vào chat 1 dòng: "Tên DN + vấn đề lớn nhất" — vừa điểm danh vừa lấy dữ liệu cho mentor phân nhóm kèm.

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Dữ liệu nền Sen Spa (chiếu slide trước khi demo):** Sen Spa — spa chăm sóc da tại Hà Nội (Đống Đa). Chủ: chị Lan. 6 nhân viên: 1 lễ tân, 1 tư vấn viên giỏi (Hương), 4 kỹ thuật viên. Dịch vụ: chăm sóc da cơ bản, trị mụn, trị nám, trẻ hóa da. AOV (Average Order Value — giá trị đơn trung bình) 1.5tr/buổi lẻ; liệu trình 8-12 buổi giá 12-15tr. Khách đến từ Facebook + giới thiệu. Đau: lead ít, không follow-up, sale phụ thuộc mình Hương.

**Bước 1 (7') — Tạo Business Model Canvas bằng AI phỏng vấn ngược.**
- Làm gì: Mở RocketAgent (hoặc ChatGPT/Claude nếu học viên chưa có tài khoản), paste Prompt 0 (mục 8). AI hỏi lần lượt 9 khối BMC; trainer đóng vai chị Lan trả lời nhanh bằng dữ liệu Sen Spa.
- Kết quả trông như thế nào: 1 canvas 9 khối, mỗi khối 3-5 bullet đủ cụ thể để AI dùng làm bối cảnh gốc.
- Điểm nhấn khi giảng: "Đây là bản đồ gốc. Từ hôm nay, mọi Agent đều phải đọc BMC trước khi làm việc."

**Bước 2 (5') — Tạo Business Snapshot từ BMC.**
- Làm gì: Mở RocketAgent (hoặc ChatGPT/Claude nếu học viên chưa có tài khoản), paste Prompt 1 (mục 8). AI sẽ hỏi lần lượt 10 câu; trainer đóng vai chị Lan trả lời miệng, gõ nhanh.
- Kết quả trông như thế nào: 1 trang Business Snapshot có đủ 10 trường (xem Template 1.1), câu chữ gọn, số liệu thật ("50-60 tin nhắn/tháng, chốt ~10 khách").
- Điểm nhấn khi giảng: "AI hỏi giỏi hơn chúng ta tự viết — vì nó không bỏ sót trường nào."

**Bước 3 (7') — Vẽ Business Process Map.**
- Làm gì: Paste Prompt 2, đầu vào là Business Snapshot vừa tạo. AI xuất sơ đồ dạng text: `Facebook Ads/Post → Inbox → Hương tư vấn → Hẹn lịch soi da → Đến spa → Mua buổi lẻ → (đôi khi) lên liệu trình → Hết liệu trình → không ai chăm tiếp`.
- Kết quả: bảng 2 cột "Bước — Điểm nghẽn". Trainer khoanh đỏ 3 nghẽn: inbox trả lời chậm ngoài giờ, không follow-up khách hỏi giá, không có quy trình tái ký liệu trình.
- Điểm nhấn: "Mỗi mũi tên là một chỗ khách rơi rớt. Ba chỗ khoanh đỏ này chính là tiền đang chảy ra ngoài."

**Bước 4 (6') — Quét cơ hội AI theo 5 khu vực.**
- Làm gì: Paste Prompt 3. AI liệt kê ~15-20 cơ hội chia theo 5 khu vực.
- Kết quả: bảng có cột Khu vực | Cơ hội | Việc hiện tại ai làm | AI thay được bao nhiêu %.
- Điểm nhấn: đọc to 2-3 dòng bất ngờ (VD: "AI viết tin nhắn chúc mừng khách hoàn thành buổi 5/10 kèm ảnh tiến triển da" — học viên thường không nghĩ tới).

**Bước 5 (4') — Chấm ICE, chốt Top 10.**
- Làm gì: Paste Prompt 4. AI chấm ICE từng cơ hội, xếp hạng, đề xuất Top 10.
- Kết quả Sen Spa (đọc to Top 5): 1) AI trả lời inbox + báo giá 24/7 (13đ) · 2) Chuỗi tin nhắn follow-up khách hỏi giá chưa chốt (13đ) · 3) AI viết content Facebook 12 bài/tháng (12đ) · 4) Chuẩn hóa kịch bản tư vấn của Hương thành script AI (12đ) · 5) Dashboard đếm lead-hẹn-chốt hàng tuần (11đ).
- Điểm nhấn: "Cả 5 cái này đều nằm trong lộ trình 28 ngày — tuần 2 làm content, tuần 3 làm chatbot + sale script, tuần 4 làm follow-up + dashboard."

**Bước 6 (1') — Viết mục tiêu 28 ngày.**
- Làm gì: Paste Prompt 5. AI đề xuất mục tiêu SMART (Specific-Measurable-Achievable-Relevant-Time-bound — cụ thể, đo được, khả thi, liên quan, có hạn).
- Kết quả Sen Spa: "Trong 28 ngày: tăng lead từ Facebook từ 50 → 80 tin nhắn/tháng; tỷ lệ khách hỏi giá được follow-up từ 0% → 100%; có 1 chatbot tư vấn + 1 bộ kịch bản sale không phụ thuộc Hương."

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core ≤ 2h)

**Cụm A — Business Model Canvas + Business Snapshot (35'):**
- [ ] Mở Template 1.0, đọc bản Sen Spa BMC điền mẫu (5')
- [ ] Chạy Prompt 0, trả lời đủ 9 khối BMC cho DN mình (12')
- [ ] Rà BMC: mỗi khối có ít nhất 3 bullet cụ thể, không viết chung chung kiểu "mọi người đều là khách" (5')
- [ ] Mở Template 1.1, đọc bản Sen Spa điền mẫu (3')
- [ ] Chạy Prompt 1 từ BMC vừa hoàn thiện để rút Business Snapshot 1 trang (5')
- [ ] Dán kết quả vào Template 1.1, sửa số liệu cho đúng thực tế — KHÔNG để số AI bịa (5')

**Cụm B — Business Process Map (20'):**
- [ ] Chạy Prompt 2 với Business Snapshot làm đầu vào (8')
- [ ] Rà từng bước: có đúng trình tự thực tế của DN mình không, sửa tay (7')
- [ ] Khoanh/đánh dấu 🔴 tối thiểu 3 điểm nghẽn (5')

**Cụm C — Top 10 AI Use Cases (30'):**
- [ ] Chạy Prompt 3 quét cơ hội 5 khu vực (8')
- [ ] Gạch bỏ cơ hội không thực tế với DN mình, bổ sung cơ hội AI bỏ sót (7')
- [ ] Chạy Prompt 4 chấm ICE, rà lại điểm — bạn hiểu DN hơn AI, được phép sửa điểm (10')
- [ ] Chốt Top 10 vào Template 1.3 (5')

**Cụm D — Mục tiêu 28 ngày (15'):**
- [ ] Chạy Prompt 5, chọn 1 mục tiêu chính + 3 chỉ số (10')
- [ ] Điền vào Template 1.4, tự hỏi: "Con số này tôi đo bằng cách nào?" (5')

**Cụm E — Nộp bài (10'):**
- [ ] Đặt tên file đúng quy ước, nộp vào thread cohort trước 23h59

**Bonus (nếu còn sức):** hoàn thiện AI Opportunity Map đủ 5 khu vực ≥15 cơ hội + ước lượng giờ/tuần đang tốn cho mỗi việc trong Top 10.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Làm cho CHÍNH doanh nghiệp của bạn (không làm cho DN giả định): (1) Business Model Canvas 9 khối, (2) Business Snapshot 1 trang, (3) Business Process Map có đánh dấu ≥3 điểm nghẽn, (4) Top 10 AI Use Cases có điểm ICE, (5) Mục tiêu 28 ngày với 3 chỉ số đo được.

**Deliverable nộp (1 file duy nhất, 4 phần, Google Docs hoặc PDF):**
- `[Tên DN] — Ngày 01 — AI Foundation Snapshot`
- Ví dụ: `Sen Spa — Ngày 01 — AI Foundation Snapshot`

**Deadline:** 23h59 cùng ngày. Nộp link vào thread cohort ngày 01. Bài nộp muộn được chấm nhưng không được chữa live hôm sau.

## 7. 📄 Template Đi Kèm

**Template 1.0 — Business Model Canvas.** 9 khối chuẩn: Customer Segments | Value Propositions | Channels | Customer Relationships | Revenue Streams | Key Resources | Key Activities | Key Partners | Cost Structure. Mỗi khối có sẵn câu hỏi gợi ý + bản Sen Spa điền mẫu. Đây là tài liệu gốc sẽ được đưa vào thư mục `01. Business Overview` của Knowledge Base Ngày 04.

**Template 1.1 — Business Snapshot (1 trang).** Các trường: Tên DN & địa điểm | Sản phẩm/dịch vụ chính (kèm giá) | Khách hàng chính (1-2 câu) | AOV & sản phẩm giá trị cao nhất | Biên lợi nhuận ước tính | Kênh bán chính | Kênh marketing chính | Đội ngũ (số người, ai làm sale/marketing) | 3 vấn đề lớn nhất | Doanh thu tháng gần nhất (tùy chọn, có thể ghi khoảng). *Bản điền mẫu Sen Spa nằm ngay trong template.*

**Template 1.2 — Business Process Map.** Cấu trúc: bảng 4 cột — Bước (theo dòng khách hàng) | Ai/công cụ đang xử lý | Điều gì đang ổn | 🔴 Điểm nghẽn. Kèm dòng flow tổng: `Kênh → Lead → Tư vấn → Mua → Sử dụng → Chăm sóc → Mua lại/Giới thiệu`.

**Template 1.3 — Top 10 AI Use Cases.** Bảng 7 cột: # | Đầu việc AI hóa | Khu vực (M/S/CS/Ops/Data) | Impact (1-5) | Confidence (1-5) | Ease (1-5) | Tổng ICE. Dưới bảng: 3 dòng "Use case này sẽ được xây ở ngày nào trong 28 ngày" (trainer map giúp buổi sau nếu học viên chưa biết).

**Template 1.4 — Mục tiêu 28 ngày.** Trường: Mục tiêu chính (1 câu, có con số + thời hạn) | Chỉ số 1/2/3 (hiện tại → mục tiêu → cách đo) | Lý do mục tiêu này quan trọng nhất lúc này (2-3 câu).

*(Cả 4 template đều có sẵn bản Sen Spa điền mẫu để học viên "nhìn bài đúng" trước khi điền — dựng sẵn 80%, học viên điền 20%.)*

### Bản điền mẫu Template 1.1 — Sen Spa (chiếu trong buổi live)

> **Tên DN & địa điểm:** Sen Spa — spa chăm sóc da, Đống Đa, Hà Nội. Hoạt động 4 năm.
> **Sản phẩm/dịch vụ chính:** Buổi chăm sóc da cơ bản 1.5tr · Liệu trình trị mụn 8 buổi 12tr · Liệu trình trị nám 10 buổi 15tr · Liệu trình trẻ hóa 12 buổi 15tr.
> **Khách hàng chính:** Nữ 28-45, nhân viên văn phòng & chủ kinh doanh nhỏ tại Hà Nội, thu nhập 15-40tr/tháng, quan tâm nám - mụn - lão hóa.
> **AOV & sản phẩm giá trị cao nhất:** AOV 1.5tr/buổi lẻ; giá trị cao nhất là liệu trình nám 15tr — chiếm ~60% doanh thu.
> **Biên lợi nhuận ước tính:** ~45-50% (ước lượng, chưa tách chi phí chính xác).
> **Kênh bán chính:** Tư vấn trực tiếp tại spa + inbox fanpage.
> **Kênh marketing chính:** Fanpage Facebook (đăng không đều, 3-4 bài/tháng) + khách cũ giới thiệu. ~50-60 tin nhắn mới/tháng, chốt ~10 khách.
> **Đội ngũ:** 6 người — 1 lễ tân, 1 tư vấn viên (Hương — người duy nhất chốt sale tốt), 4 kỹ thuật viên. Marketing: chị Lan tự đăng bài khi rảnh.
> **3 vấn đề lớn nhất:** (1) lead ít và không đều; (2) khách hỏi giá xong không ai follow-up; (3) sale phụ thuộc hoàn toàn vào Hương.
> **Doanh thu tháng gần nhất:** khoảng 180-220tr.

### Bản điền mẫu Template 1.3 — Top 10 của Sen Spa (rút gọn 5 dòng đầu)

| # | Đầu việc AI hóa | Khu vực | I | C | E | Tổng |
|---|---|---|---|---|---|---|
| 1 | AI trực inbox + báo giá 24/7 | Sales | 5 | 4 | 4 | 13 |
| 2 | Chuỗi follow-up khách hỏi giá chưa chốt (3 chạm/7 ngày) | Sales | 5 | 4 | 4 | 13 |
| 3 | AI viết 12 bài Facebook/tháng theo lịch content | Marketing | 4 | 4 | 4 | 12 |
| 4 | Chuẩn hóa kịch bản tư vấn của Hương thành script | Sales | 4 | 4 | 4 | 12 |
| 5 | Báo cáo tuần: inbox → hẹn → chốt trên 1 trang | Đo lường | 4 | 4 | 3 | 11 |

*(Dòng 6-10 của Sen Spa: tin nhắn nhắc lịch & chăm sau buổi · gợi ý upsell buổi 5/10 · kịch bản video trước-sau · trả lời FAQ tự động · SOP đón khách. Học viên xem bản đầy đủ trong template.)*

## 8. 🤖 Prompt Mẫu

### Prompt 0 — AI phỏng vấn để tạo Business Model Canvas

```
[VAI TRÒ] Bạn là chuyên gia Business Model Canvas và AIOS cho SME dịch vụ. Nhiệm vụ của bạn là phỏng vấn chủ doanh nghiệp để dựng BMC 9 khối đủ rõ cho đội AI Agent dùng làm bối cảnh gốc.

[BỐI CẢNH] Tôi đang cài AI Marketing & Sales OS vận hành bằng Agent cho doanh nghiệp. Trước khi dựng Agent, tôi cần Business Model Canvas rõ ràng để AI hiểu mô hình kinh doanh, khách hàng mục tiêu, offer, kênh bán, nguồn lực và dòng tiền.

[NHIỆM VỤ] Hỏi tôi lần lượt 9 khối BMC, mỗi lần chỉ hỏi 1 nhóm câu hỏi rồi chờ tôi trả lời:
1. Customer Segments — khách hàng mục tiêu là ai, nhóm nào mang nhiều tiền nhất?
2. Value Propositions — khách mua kết quả gì, vì sao chọn tôi thay vì đối thủ?
3. Channels — khách biết đến, tương tác, mua và nhận dịch vụ qua kênh nào?
4. Customer Relationships — tôi nuôi dưỡng, tư vấn, chăm sóc, giữ chân khách ra sao?
5. Revenue Streams — tôi thu tiền từ sản phẩm/gói nào, giá/AOV/LTV thế nào?
6. Key Resources — tài sản, dữ liệu, con người, thương hiệu, công cụ quan trọng nhất là gì?
7. Key Activities — các hoạt động lõi phải làm tốt mỗi tuần để tạo doanh thu?
8. Key Partners — ai/công cụ/đối tác giúp tôi vận hành và bán hàng?
9. Cost Structure — chi phí lớn nhất, chi phí biến đổi, chi phí đang lãng phí?

[ĐỊNH DẠNG ĐẦU RA] Sau khi hỏi đủ 9 khối, xuất Business Model Canvas dạng bảng 9 khối. Mỗi khối có 3-5 bullet cụ thể, có số liệu nếu tôi cung cấp. Cuối bảng thêm mục "Hàm ý cho AIOS": 5 đầu việc Agent nên ưu tiên từ BMC này.

[RÀNG BUỘC] Không tự bịa số liệu. Nếu thiếu, ghi "[cần bổ sung]". Tránh câu chung chung. Nếu tôi nói "mọi người đều là khách", hãy ép tôi chọn 1-2 phân khúc ưu tiên. Viết tiếng Việt, súc tích.
```

### Prompt 1 — AI phỏng vấn ngược để tạo Business Snapshot

```
[VAI TRÒ] Bạn là một chuyên gia tư vấn chiến lược cho doanh nghiệp nhỏ (SME) ngành dịch vụ tại Việt Nam, giỏi đặt câu hỏi để rút ra bức tranh kinh doanh rõ ràng.

[BỐI CẢNH] Tôi là chủ một doanh nghiệp dịch vụ, đang tham gia chương trình 28 ngày xây hệ thống AI Marketing & Sales. Hôm nay tôi cần một bản Business Snapshot (bản chụp doanh nghiệp) 1 trang.

[NHIỆM VỤ] Hãy phỏng vấn tôi LẦN LƯỢT TỪNG CÂU MỘT (hỏi xong chờ tôi trả lời rồi mới hỏi tiếp) theo đúng 10 chủ đề: (1) tên DN + địa điểm + ngành; (2) danh sách sản phẩm/dịch vụ chính kèm giá; (3) khách hàng chính là ai; (4) giá trị đơn trung bình và sản phẩm giá trị cao nhất; (5) biên lợi nhuận ước tính; (6) kênh bán hàng chính; (7) kênh marketing chính và hiệu quả hiện tại (số lead/tháng); (8) đội ngũ — ai đang làm marketing, ai làm sale; (9) 3 vấn đề lớn nhất hiện nay; (10) doanh thu tháng gần nhất hoặc khoảng doanh thu. Sau câu 10, tổng hợp thành Business Snapshot.

[DỮ LIỆU ĐẦU VÀO] Thông tin ban đầu về doanh nghiệp của tôi: {{2-3 câu giới thiệu ngắn về DN của bạn}}

[ĐỊNH DẠNG ĐẦU RA] Sau khi phỏng vấn xong: một bản Business Snapshot dài đúng 1 trang, có 10 đề mục in đậm tương ứng 10 chủ đề, mỗi mục 1-3 câu, giữ nguyên số liệu tôi cung cấp.

[RÀNG BUỘC] Không tự bịa số liệu — nếu tôi trả lời "không biết", ghi rõ "[cần bổ sung]". Nếu câu trả lời của tôi mơ hồ, hỏi lại 1 câu làm rõ trước khi sang chủ đề tiếp theo. Viết tiếng Việt, giọng ngắn gọn.
```

**Ví dụ đã điền (Sen Spa):** `{{2-3 câu giới thiệu ngắn}}` → "Tôi là Lan, chủ Sen Spa — spa chăm sóc da ở Đống Đa, Hà Nội. Spa có 6 nhân viên, bán buổi chăm sóc da lẻ 1.5tr và liệu trình trị mụn/nám 8-12 buổi giá 12-15tr. Khách chủ yếu từ Facebook và người quen giới thiệu."

### Prompt 2 — Vẽ Business Process Map + chỉ điểm nghẽn

```
[VAI TRÒ] Bạn là chuyên gia thiết kế quy trình kinh doanh (business process) cho SME dịch vụ bán qua tư vấn.

[BỐI CẢNH] Tôi vừa hoàn thành Business Snapshot của doanh nghiệp mình. Tôi cần nhìn thấy toàn bộ dòng chảy khách hàng để biết tiền đang rơi rớt ở đâu.

[NHIỆM VỤ] Từ Business Snapshot dưới đây: (1) vẽ Business Process Map dạng chuỗi text theo dòng khách hàng: Kênh → Lead → Tư vấn → Mua → Sử dụng → Chăm sóc → Mua lại/Giới thiệu, mô tả đúng cách DN tôi ĐANG vận hành (kể cả bước đang thiếu — ghi rõ "KHÔNG CÓ"); (2) lập bảng 4 cột: Bước | Ai/công cụ đang xử lý | Đang ổn ở điểm gì | Điểm nghẽn; (3) chọn ra 3 điểm nghẽn nghiêm trọng nhất, giải thích vì sao mỗi nghẽn làm mất tiền, ước lượng mức thiệt hại tương đối.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán toàn bộ Business Snapshot từ Prompt 1}}

[ĐỊNH DẠNG ĐẦU RA] Phần 1: dòng flow bằng mũi tên. Phần 2: bảng markdown 4 cột. Phần 3: danh sách "🔴 Top 3 điểm nghẽn" — mỗi nghẽn 3 dòng: hiện tượng / vì sao mất tiền / mất khoảng bao nhiêu cơ hội mỗi tháng.

[RÀNG BUỘC] Chỉ dựa trên dữ liệu tôi đưa, không suy diễn thêm dịch vụ DN không có. Với bước "KHÔNG CÓ", tự động coi là ứng viên điểm nghẽn. Tiếng Việt, tối đa 500 từ.
```

**Ví dụ đã điền (Sen Spa):** dán Business Snapshot Sen Spa → AI trả về flow `FB Post/Ads + Giới thiệu → Inbox fanpage (~55 tin/tháng) → Hương tư vấn (giờ hành chính) → Hẹn soi da → Đến spa, mua buổi lẻ 1.5tr → KTV chăm sóc → KHÔNG CÓ follow-up sau buổi lẻ → ~30% tự lên liệu trình → KHÔNG CÓ quy trình tái ký & xin giới thiệu` và Top 3 nghẽn: inbox ngoài giờ không ai trả lời (mất ~15 lead/tháng), khách hỏi giá không được nhắn lại (mất ~20 cơ hội/tháng), hết liệu trình không tái ký (mất ~5 khách cũ/tháng).

### Prompt 3 — Quét cơ hội AI hóa theo 5 khu vực

```
[VAI TRÒ] Bạn là chuyên gia chuyển đổi AI cho SME ngành dịch vụ bán qua tư vấn (spa, nha khoa, giáo dục, gym, coaching) tại Việt Nam, hiểu rõ giới hạn thực tế: chủ DN bận, không rành công nghệ, ngân sách thấp.

[BỐI CẢNH] Doanh nghiệp của tôi đã có Business Snapshot và Process Map kèm điểm nghẽn. Tôi cần bản đồ đầy đủ những việc AI có thể làm thay hoặc làm cùng con người trong DN.

[NHIỆM VỤ] Liệt kê 15-20 cơ hội AI hóa, chia theo đúng 5 khu vực: (1) Marketing, (2) Sales, (3) Chăm sóc khách hàng, (4) Vận hành nội bộ, (5) Đo lường & ra quyết định. Ưu tiên các cơ hội trực tiếp vá 3 điểm nghẽn tôi nêu. Mỗi khu vực tối thiểu 3 cơ hội.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán Business Snapshot}}. Top 3 điểm nghẽn: {{dán 3 điểm nghẽn từ Prompt 2}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng markdown 5 cột: Khu vực | Cơ hội AI hóa (tên ngắn + 1 câu mô tả) | Việc này hiện ai đang làm / hay không ai làm | AI thay được ~bao nhiêu % | Vá điểm nghẽn nào (ghi số 1/2/3 hoặc "—").

[RÀNG BUỘC] Chỉ đề xuất việc khả thi với công cụ phổ thông (chatbot, AI viết content, AI phân tích bảng tính) — không đề xuất giải pháp cần lập trình riêng hay phần cứng. Không đề xuất AI thay việc phải chạm tay khách. Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** kết quả tiêu biểu — Marketing: AI viết 12 bài FB/tháng theo lịch; AI viết kịch bản video ngắn quay trước-sau. Sales: AI trực inbox báo giá 24/7; AI soạn kịch bản tư vấn chuẩn từ cách nói của Hương; AI viết tin follow-up 3 chạm. CSKH: AI nhắn nhắc lịch + chăm sau buổi; AI gợi ý upsell khi khách xong buổi 5/10. Vận hành: AI viết SOP đón khách; AI tóm tắt phản hồi khách theo tuần. Đo lường: AI tổng hợp số inbox-hẹn-chốt thành báo cáo tuần.

### Prompt 4 — Chấm ICE và chốt Top 10

```
[VAI TRÒ] Bạn là cố vấn ưu tiên hóa danh mục dự án cho chủ SME, nghiêm khắc với việc "ôm đồm".

[BỐI CẢNH] Tôi có danh sách 15-20 cơ hội AI hóa. Trong 28 ngày tôi chỉ triển khai được 10. Chương trình của tôi tập trung Marketing & Sales.

[NHIỆM VỤ] (1) Chấm mỗi cơ hội theo ICE: Impact — tác động đến doanh thu/tiết kiệm thời gian (1-5); Confidence — độ chắc chắn làm được với dữ liệu hiện có (1-5); Ease — độ dễ với người không rành công nghệ (1-5). (2) Xếp hạng theo tổng điểm. (3) Đề xuất Top 10, đảm bảo: ≥4 use case thuộc Marketing/Sales; ≥7 use case nằm trong nhóm chuẩn của lộ trình (content, hình ảnh/video, chatbot tư vấn, phân loại lead, kịch bản sale, follow-up tự động, CSKH, báo cáo/dashboard). (4) Với mỗi use case trong Top 10, ghi 1 câu "kết quả kỳ vọng sau 28 ngày".

[DỮ LIỆU ĐẦU VÀO] Danh sách cơ hội: {{dán bảng từ Prompt 3}}. Bối cảnh thêm: {{1-2 câu về nguồn lực — VD: chỉ mình tôi làm, mỗi ngày có 2h}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng: # | Use case | Khu vực | I | C | E | Tổng | Kết quả kỳ vọng. Sau bảng: 2-3 dòng giải thích vì sao các use case bị loại.

[RÀNG BUỘC] Điểm phải có căn cứ từ dữ liệu tôi đưa (VD: Impact 5 vì vá nghẽn mất 20 cơ hội/tháng). Không cho hai use case trùng bản chất cùng vào Top 10. Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** Top 3 kết quả — #1 AI trực inbox báo giá 24/7 (I5 C4 E4 = 13; kỳ vọng: 100% inbox được trả lời <1 phút); #2 Chuỗi follow-up khách hỏi giá (I5 C4 E4 = 13; kỳ vọng: 100% khách hỏi giá nhận đủ 3 chạm trong 7 ngày); #3 AI viết content FB (I4 C4 E4 = 12; kỳ vọng: 12 bài/tháng đăng đều).

### Prompt 5 — Viết mục tiêu 28 ngày SMART

```
[VAI TRÒ] Bạn là huấn luyện viên mục tiêu cho chủ SME, chuyên biến mong muốn mơ hồ thành mục tiêu SMART (cụ thể — đo được — khả thi — liên quan — có thời hạn).

[BỐI CẢNH] Tôi bắt đầu chương trình 28 ngày xây AI Marketing & Sales OS. Tôi cần 1 mục tiêu chính + 3 chỉ số để cuối chương trình biết mình thành công hay không.

[NHIỆM VỤ] Từ dữ liệu dưới đây, đề xuất 3 phương án mục tiêu chính (an toàn / cân bằng / tham vọng), mỗi phương án kèm đúng 3 chỉ số dạng "hiện tại → mục tiêu → cách đo". Sau đó khuyến nghị 1 phương án và giải thích trong 3 câu.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán}}. Top 10 AI Use Cases: {{dán}}. Mong muốn cá nhân của tôi: {{1-2 câu — VD: tôi muốn bớt phụ thuộc nhân viên giỏi}}.

[ĐỊNH DẠNG ĐẦU RA] 3 khối phương án, mỗi khối: Mục tiêu chính (1 câu có con số + mốc 28 ngày) + bảng 3 chỉ số (Chỉ số | Hiện tại | Mục tiêu | Cách đo). Cuối: "Khuyến nghị" 3 câu.

[RÀNG BUỘC] Chỉ số phải đo được bằng công cụ chủ DN đang có (đếm inbox, sổ hẹn, doanh thu) — không dùng chỉ số cần tool phức tạp. Mục tiêu doanh thu tăng không quá 30% trong 28 ngày (thực tế). Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** phương án cân bằng được chọn — "Sau 28 ngày, Sen Spa có hệ thống AI vận hành marketing-sale giúp tăng lead Facebook từ 55 → 80 tin nhắn/tháng." Chỉ số: (1) tin nhắn mới/tháng: 55 → 80, đo bằng hộp thư fanpage; (2) % khách hỏi giá được follow-up đủ 3 chạm: 0% → 100%, đo bằng CRM/sheet; (3) số kịch bản tư vấn chuẩn hóa không phụ thuộc Hương: 0 → 5 kịch bản, đếm file.

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-01: Rà soát cơ hội AI hóa hàng quý**
- **Khi nào:** Ngày đầu mỗi quý (hoặc khi DN mở dịch vụ mới / thêm kênh mới).
- **Ai làm:** Chủ DN (30-45').
- **Input:** Business Snapshot quý trước + số liệu 3 tháng (lead, tỷ lệ chốt, doanh thu).
- **Các bước:** (1) Cập nhật Business Snapshot — sửa số liệu mới; (2) Chạy lại Prompt 2 xem điểm nghẽn có dịch chuyển không; (3) Chạy Prompt 3 + 4, so Top 10 mới với Top 10 cũ; (4) Chọn 1-2 use case mới để triển khai trong quý; (5) Lưu bản mới vào thư mục Knowledge Base `01. Business Overview` (sẽ tạo ở Ngày 04).
- **Output:** Business Snapshot phiên bản mới + Top 10 cập nhật + 1-2 use case triển khai quý này.
- **Tần suất:** 4 lần/năm.

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Đủ 4 phần trong 1 file (mỗi phần thiếu −8): Business Snapshot đủ 10 trường (10đ) · Process Map đủ chuỗi từ Kênh đến Mua lại (10đ) · Top 10 use case có đủ điểm I/C/E từng dòng (5đ) · Mục tiêu 28 ngày có 1 mục tiêu + 3 chỉ số (5đ) |
| Chất lượng & độ sâu | 30 | Process Map đánh dấu ≥3 điểm nghẽn kèm lý do mất tiền (10đ) · ≥7/10 use case thuộc nhóm lộ trình 28 ngày (10đ) · cả 3 chỉ số có đủ bộ ba "hiện tại → mục tiêu → cách đo" (10đ) |
| Cá nhân hoá vào DN thật | 25 | Có ≥5 con số thật của DN (giá, số lead/tháng, số nhân sự, AOV, doanh thu/khoảng doanh thu) (15đ) · không còn placeholder kiểu "[cần bổ sung]"/văn mẫu AI chung chung — kiểm tra bằng cách đọc 3 dòng bất kỳ phải thấy tên DN/ngành cụ thể (10đ) |
| Dùng được ngay | 15 | Top 10 xếp hạng rõ #1-#10, không đồng hạng tràn lan (>3 cặp đồng hạng = trừ) (8đ) · file đặt tên đúng quy ước, chia sẻ mở được không cần xin quyền (7đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Dán nguyên output AI chưa sửa — số liệu bịa (VD: AI ghi "100 lead/tháng" trong khi thực tế 50): −10.
2. Top 10 toàn use case ngoài lộ trình (app riêng, AI phân tích ảnh y khoa...): −10.
3. Mục tiêu không đo được ("tăng nhận diện thương hiệu"): −8.
4. Process Map chỉ có flow mũi tên, không có điểm nghẽn: −8.
5. Nộp 4 file rời thay vì 1 file 4 phần: −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Tôi không biết chính xác biên lợi nhuận / số lead mỗi tháng thì điền sao?**
→ Điền KHOẢNG ước lượng ("40-60 tin nhắn/tháng", "biên ~50%") kèm ghi chú "ước lượng". Cấm bỏ trống, cấm để AI bịa. Việc bạn không đo được chính là một điểm nghẽn — ghi nó vào Process Map.

**Q2: Doanh nghiệp tôi có 2-3 mảng (vừa spa vừa bán mỹ phẩm), làm cho mảng nào?**
→ Chọn 1 mảng đóng góp doanh thu lớn nhất hoặc bạn muốn tăng trưởng nhất, làm xuyên suốt 28 ngày cho mảng đó. Mảng phụ chỉ nhắc 1 dòng trong Snapshot.

**Q3: Tôi chưa có tài khoản RocketAgent / chưa quen công cụ AI nào?**
→ Hôm nay dùng ChatGPT hoặc Claude bản web miễn phí đều chạy được toàn bộ 5 prompt. RocketAgent bắt buộc từ Ngày 04 (Knowledge Base) — đăng ký trước theo hướng dẫn trong nhóm.

**Q4: Top 10 của tôi có nên cho use case "AI chấm công / AI kế toán" không?**
→ Không nên chiếm chỗ — chương trình này xây Marketing & Sales OS. Ghi các ý đó vào mục "Bãi đỗ ý tưởng" cuối file để làm sau 28 ngày.

**Q5: Tôi làm dịch vụ B2B (tư vấn, agency), khung này có áp dụng được không?**
→ Được — dòng khách vẫn là Kênh → Lead → Tư vấn → Chốt → Triển khai → Tái ký. Chỉ khác: chu kỳ chốt dài hơn, thay "inbox fanpage" bằng "Zalo/email/referral".

**Q6: 2 tiếng không đủ làm hết thì sao?**
→ Ưu tiên đúng thứ tự A → D trong checklist. Bonus (AI Opportunity Map đầy đủ) bỏ qua không bị trừ điểm.

**Q7: AI trả lời tiếng Anh hoặc lẫn tiếng Anh thì làm sao?**
→ Thêm vào cuối prompt dòng: "Trả lời hoàn toàn bằng tiếng Việt." Nếu vẫn lẫn, gõ tiếp: "Viết lại toàn bộ bằng tiếng Việt." Đây là lý do mọi prompt mẫu của chương trình đều có ràng buộc ngôn ngữ sẵn — đừng xóa dòng Constraint (ràng buộc).

**Q8: Tôi có cần nộp cả lịch sử chat với AI không?**
→ Không. Chỉ nộp file thành phẩm 4 phần. Nhưng NÊN lưu link chat lại cho mình — Ngày 05 sẽ dạy cách biến các đoạn chat tốt thành prompt library (thư viện câu lệnh).

**Lỗi thường gặp:**
1. **Snapshot viết như bài PR** ("spa uy tín hàng đầu, dịch vụ tận tâm") — *Phát hiện:* không có con số nào trong 3 dòng liên tiếp. — *Sửa:* mỗi mục phải có ít nhất 1 con số hoặc danh từ cụ thể; chạy lại Prompt 1 và trả lời bằng số.
2. **Process Map vẽ quy trình LÝ TƯỞNG thay vì quy trình THẬT** — *Phát hiện:* map có bước "gửi email chăm sóc định kỳ" nhưng DN chưa từng gửi email nào. — *Sửa:* nguyên tắc "vẽ cái đang có, kể cả cái xấu"; bước chưa có ghi "KHÔNG CÓ".
3. **Chấm ICE cả 10 use case đều 14-15 điểm** — *Phát hiện:* không có use case nào dưới 12. — *Sửa:* ép phân phối — tối đa 3 use case được ≥13; tự hỏi "nếu chỉ được làm 1 cái, tôi làm cái nào?" rồi chấm lại từ đó xuống.

## 12. 🔁 Kết Nối

- Ngày trước: — (ngày khai giảng, xem [[_MOC 28 Day AIOS]]) · Ngày sau: [[Ngày 02 — Chân Dung Khách Hàng & Customer Journey]]
- Tài sản hôm nay được dùng lại ở:
	- **Business Snapshot** → đầu vào Prompt phỏng vấn Avatar (Ngày 02), tài liệu số 1 của Knowledge Base (Ngày 04), phần mở đầu Instruction của AI Business Brain (Ngày 06).
	- **Business Process Map** → khung thiết kế Customer Journey (Ngày 02) và điểm đặt chatbot/follow-up (Tuần 3-4).
	- **Top 10 AI Use Cases** → checklist nghiệm thu toàn chương trình; Demo Day 1 (Ngày 07) sẽ đối chiếu tiến độ theo danh sách này.
	- **Mục tiêu 28 ngày** → thước đo trong Foundation Scorecard (Ngày 07) và Dashboard (Tuần 4).
