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

> **2 case study thật, 0 case bịa** (xem [[Case Study Mẫu — RocketAI & MSX Group]]): 🍵 **MSX Group / Mẫu Sơn Xanh** — học viên thật của chương trình, bán trà thảo mộc & dược liệu Mẫu Sơn online (B2C sản phẩm) — là ví dụ xuyên suốt. 🚀 **RocketAI Solutions** — công ty của người dạy, bán dịch vụ cài hệ thống AI cho SME (B2B dịch vụ) — dùng để đối chiếu khi mô hình B2B khác B2C.

### Khối 1 — Tổng quan AI Marketing & Sales OS™ (5')
- **Ý chính:** Sau 28 ngày, học viên không "biết AI" mà SỞ HỮU một hệ điều hành: Marketing → Thu lead (khách hàng tiềm năng) → Tư vấn → Chốt sale → Chăm sóc → Upsell (bán thêm) → Đo lường → Tối ưu.
- **Cách giảng:** Chiếu sơ đồ vòng tròn 8 bước. Analogy: "AI OS giống như tuyển một đội nhân viên số làm việc 24/7 — nhưng nhân viên mới thì phải đào tạo. 28 ngày này là 28 ngày đào tạo đội nhân viên đó bằng chính dữ liệu doanh nghiệp của anh chị."
- **Ví dụ 🍵 MSX:** MSX bán 6 dòng trà & viên dược liệu Mẫu Sơn qua website + Facebook + TikTok + Zalo. AI OS sẽ đóng vai: 1 nhân viên content kể chuyện vùng nguyên liệu, 1 nhân viên trực inbox 24/7, 1 trợ lý tư vấn sản phẩm theo nhu cầu, 1 nhân viên nhắc khách mua lại đúng chu kỳ hết hộp — tổng lương 0 đồng.

### Khối 2 — Business Model Canvas: bản đồ hệ gen của doanh nghiệp (8')
- **Ý chính:** Trước khi dựng Agent, AI phải hiểu doanh nghiệp kiếm tiền bằng mô hình nào. BMC 9 khối giúp gom toàn bộ logic kinh doanh vào một trang: bán cho ai, hứa giá trị gì, đi qua kênh nào, quan hệ ra sao, thu tiền từ đâu, cần nguồn lực/hoạt động/đối tác nào, và chi phí nằm ở đâu.
- **Cách giảng:** BMC là "hồ sơ nhân sự đầu vào" cho toàn bộ đội Agent. Nếu BMC mơ hồ, Content Agent viết lệch khách; Sales Agent tư vấn sai offer; Data Agent đo sai chỉ số. Nếu BMC rõ, mọi Agent dùng cùng một bản sự thật.
- **Ví dụ 🍵 MSX:** Customer Segments = 3 phân khúc rõ rệt (người dùng chăm sóc sức khỏe tự nhiên 28-55 tuổi đô thị · người mua quà biếu · đại lý/quà tặng doanh nghiệp); Value Propositions = dược liệu Mẫu Sơn nguồn gốc rõ ràng + OCOP 3★ + câu chuyện bản địa Dao/Tày/Nùng; Channels = website mausonxanh.com, Facebook, TikTok, Zalo OA, hội chợ OCOP, đại lý; Revenue Streams = bán lẻ + combo mua 3 tặng 1 + đơn sỉ đại lý (từ 50 sản phẩm) + quà tặng doanh nghiệp; Key Activities = thu hái - chế biến - kiểm soát chất lượng - content giáo dục thị trường - tư vấn & xử lý đơn.
- **Đối chiếu B2B 🚀 RocketAI:** cùng 9 khối nhưng nội dung khác hẳn — Revenue Streams không phải bán lẻ mà là 3 gói dịch vụ chuyển giao (OS Transfer 12tr / OS Installed 25tr / OS Managed 50tr+); Channels không phải TikTok/ads mà là cộng đồng, webinar và giới thiệu; AOV cao gấp ~25 lần MSX nhưng số khách ít hơn nhiều. **Bài học:** đừng copy BMC của người khác ngành — copy KHUNG, điền dữ liệu của mình.

### Khối 3 — Tư duy AI First Business (5')
- **Ý chính:** Không hỏi "AI làm được gì?" mà hỏi "Việc gì trong DN của tôi đang lặp lại, tốn thời gian, phụ thuộc con người — và có dữ liệu để AI học?"
- **Cách giảng:** Công thức nhận diện việc nên AI hóa = **Lặp lại + Có quy luật + Có dữ liệu mẫu**. Việc KHÔNG nên AI hóa ngay: việc cần bàn tay/giác quan con người (thu hái, nếm thử, kiểm định chất lượng), việc pháp lý, quyết định chiến lược.
- **Ví dụ 🍵 MSX:** Trả lời inbox "trà này khác gì trà ngoài chợ?", "có chất bảo quản không?", "bà bầu dùng được không?" lặp lại hàng chục lần mỗi tuần → AI hóa được. Nếm thử mẻ trà mới, kiểm tra độ ẩm nguyên liệu → không.

> ⚠️ **Ranh giới bắt buộc với ngành sức khỏe:** MSX (và mọi DN dược liệu/thực phẩm chức năng/spa/y tế) dùng ngôn ngữ **"hỗ trợ", "đồng hành cùng thói quen"** — TUYỆT ĐỐI không cam kết chữa bệnh, không hứa kết quả tuyệt đối. Nội dung liên quan bệnh nền, trẻ em, phụ nữ mang thai phải khuyến nghị hỏi bác sĩ. Luật này đi xuyên 28 ngày và bị trừ điểm nặng nếu vi phạm (xem rubric Ngày 03).

### Khối 4 — Nhìn doanh nghiệp như một hệ thống + 5 khu vực AI tác động (7')
- **Ý chính:** DN = chuỗi các trạm mà khách hàng đi qua. Doanh thu rơi rớt ở TRẠM YẾU NHẤT, không phải trạm mạnh nhất. 5 khu vực AI tác động: (1) Marketing, (2) Sales, (3) Chăm sóc khách hàng, (4) Vận hành nội bộ, (5) Đo lường & ra quyết định.
- **Cách giảng:** Analogy đường ống nước: "Nước (khách) chảy qua 5 đoạn ống. Vá đoạn thủng to nhất trước." Vẽ live sơ đồ ống của MSX và hỏi cả lớp: "Đoạn nào đang thủng?"
- **Ví dụ 🍵 MSX:** Ống Marketing chảy phập phù (3 bài/tuần, đăng khi rảnh, lead phụ thuộc 8tr tiền ads); ống Sales rò ban đêm (inbox phản hồi trung bình ~3 tiếng, đêm không ai trực — khách hỏi 22h hôm sau mới trả lời); ống Chăm sóc gần như tắc (chỉ 18% khách quay lại dù điểm hài lòng 4,7/5 — không ai nhắc khách khi hộp trà sắp hết).

### Khối 5 — Lập bản đồ cơ hội AI & khung ưu tiên ICE (5')
- **Ý chính:** Liệt kê rộng (mọi việc có thể AI hóa) rồi lọc hẹp bằng khung **ICE**: **Impact (tác động** đến doanh thu/thời gian**)** · **Confidence (độ tự tin** làm được**)** · **Ease (độ dễ** triển khai**)** — mỗi tiêu chí chấm 1-5, tổng tối đa 15.
- **Cách giảng:** Không chọn theo cảm hứng. Quy tắc: trong Top 10 phải có ≥4 use case thuộc Marketing/Sales (vì đây là chương trình Marketing & Sales OS), và ≥7 use case nằm trong lộ trình 28 ngày (content, chatbot, kịch bản sale, follow-up, dashboard...).
- **Ví dụ 🍵 MSX:** "Chatbot trực inbox + trả FAQ 24/7" = I:5, C:4, E:4 → 13 điểm, xếp #1. "AI tự phân tích thành phần hoạt chất trong mẻ dược liệu" = I:3, C:2, E:1 → 6 điểm, loại khỏi Top 10.

> **Thích ứng ngành khác:** Spa/Thẩm mỹ — điểm nghẽn thường ở "khách hỏi giá xong im, không ai nhắn lại"; Nha khoa — nghẽn ở "khách sợ đau, cần tư vấn kỹ trước khi đến"; Giáo dục — nghẽn ở "phụ huynh cần nói chuyện nhiều lần mới chốt"; Gym/Coaching — nghẽn ở "khách đăng ký trải nghiệm rồi biến mất". Cùng khung 5 khu vực + ICE, chỉ thay dữ liệu.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + khởi động cohort | Giới thiệu lộ trình 28 ngày, quy ước nộp bài (23h59, thread cohort), quy ước Demo Day. Hỏi nhanh 3 học viên: "DN anh chị đang đau nhất ở đâu?" — ghi lên bảng làm chất liệu. |
| 25' | Giảng kiến thức trọng tâm | 5 khối ở mục 2, đúng thứ tự. Luôn neo về ví dụ MSX; chỉ mở RocketAI ra khi cần đối chiếu B2B. |
| 30' | Demo thực hành live | Làm thật BMC + Business Snapshot + Process Map + Top 10 cho MSX bằng prompt mẫu (kịch bản mục 4). Chiếu màn hình, chạy prompt thật. |
| 15' | Học viên làm tại chỗ + Q&A | Học viên mở Template 1.0, điền nhanh 2 khối đầu của BMC (Customer Segments + Value Proposition). Trainer + mentor đảo phòng/đọc chat sửa nhanh. |
| 10' | Giao bài tập | Chiếu đề bài + deliverable + rubric (mục 6, 10). Nhấn mạnh: Core ≤2h, đừng cầu toàn AI Opportunity Map. |

**Checklist chuẩn bị của trainer (trước buổi live 30'):**
- [ ] Slide: sơ đồ vòng tròn 8 bước AI OS · sơ đồ "đường ống nước" 5 khu vực · dữ liệu nền MSX · khung ICE.
- [ ] Mở sẵn vault demo `ai-marketing-system-msx-demo/` — để chiếu BMC MSX thật khi học viên hỏi "bản hoàn chỉnh trông thế nào".
- [ ] Tab trình duyệt mở sẵn: RocketAgent (hoặc ChatGPT) đã đăng nhập, 6 prompt mẫu để trong file text sẵn sàng copy.
- [ ] Chạy thử trước cả 6 prompt với dữ liệu MSX 1 lần — lưu lại output tốt để phòng khi live AI trả kết quả kém thì chiếu bản dự phòng.
- [ ] Link 5 template (quyền xem + tạo bản sao) dán sẵn vào chat/thread cohort.
- [ ] Mở thread "Ngày 01 — Nộp bài" trong cohort, ghim quy ước đặt tên file.

**Nhịp điều phối cần giữ:**
- Phần demo (30') là trái tim buổi học — nếu cháy giờ, cắt Khối 1-2 phần giảng (đã có trong tài liệu), KHÔNG cắt demo.
- Khi học viên làm tại chỗ (15'), yêu cầu mỗi người gõ vào chat 1 dòng: "Tên DN + vấn đề lớn nhất" — vừa điểm danh vừa lấy dữ liệu cho mentor phân nhóm kèm.

## 4. 🎬 Kịch Bản Demo (Ví dụ 🍵 MSX Group)

**Dữ liệu nền MSX (chiếu slide trước khi demo):** Mẫu Sơn Xanh (MSX Group) — Công ty CP Lối vào Mẫu Sơn Xanh, dược liệu & trà thảo mộc, gốc từ thôn Bó Pằm, xã Mẫu Sơn, Lạng Sơn (độ cao 800-1.541m). Founder: Nguyễn Hoàng Hưng. Sản phẩm chủ lực: Trà Hoa Sâm Nam 369k/hộp · Trà Mẩy Gòm An Giấc 359k/hộp · Viên Sâm Nam Hà Thủ Ô 599k/hộp. Combo mua 3 tặng 1. Sỉ từ 50 sản phẩm. Chứng nhận OCOP 3★. Kênh: website + Facebook + TikTok + Zalo OA + hội chợ + đại lý. Vận chuyển: Viettel Post.

> 🧪 **(Số demo minh hoạ)** — các con số vận hành dưới đây lấy từ bản mẫu `Baseline & Mục Tiêu 28 Ngày — MSX (mẫu)` trong vault demo: minh hoạ hợp lý theo quy mô DN, **không phải số kinh doanh thật của MSX**. Trainer nói rõ điều này với lớp — đây cũng chính là bài học về tính trung thực số liệu.
>
> Lead mới/tháng: **85** · Tỷ lệ chốt: **22%** · Doanh thu/tháng: **95tr** (bán lẻ ~48tr + đại lý/quà tặng B2B ~47tr) · AOV: **520k** · Giờ marketing thủ công của chủ: **12h/tuần** · Content: **3 bài/tuần** · Phản hồi inbox: **~3 giờ** · Khách quay lại: **18%** · Ads: **8tr/tháng** · Điểm hài lòng: **4,7/5**.

**Bước 1 (7') — Tạo Business Model Canvas bằng AI phỏng vấn ngược.**
- Làm gì: Mở RocketAgent (hoặc ChatGPT/Claude nếu học viên chưa có tài khoản), paste Prompt 0 (mục 8). AI hỏi lần lượt 9 khối BMC; trainer đóng vai founder MSX trả lời nhanh bằng dữ liệu nền.
- Kết quả trông như thế nào: 1 canvas 9 khối, mỗi khối 3-5 bullet đủ cụ thể để AI dùng làm bối cảnh gốc. Đối chiếu ngay với bản hoàn chỉnh `Business Model Canvas — Mẫu Sơn Xanh.md` trong vault demo.
- Điểm nhấn khi giảng: "Đây là bản đồ gốc. Từ hôm nay, mọi Agent đều phải đọc BMC trước khi làm việc."

**Bước 2 (5') — Tạo Business Snapshot từ BMC.**
- Làm gì: Paste Prompt 1 (mục 8). AI sẽ hỏi lần lượt 10 câu; trainer đóng vai founder MSX trả lời miệng, gõ nhanh.
- Kết quả trông như thế nào: 1 trang Business Snapshot có đủ 10 trường (xem Template 1.1), câu chữ gọn, số liệu thật ("85 lead/tháng, chốt 22%").
- Điểm nhấn khi giảng: "AI hỏi giỏi hơn chúng ta tự viết — vì nó không bỏ sót trường nào."

**Bước 3 (7') — Vẽ Business Process Map.**
- Làm gì: Paste Prompt 2, đầu vào là Business Snapshot vừa tạo. AI xuất sơ đồ dạng text: `Facebook/TikTok/Website → Inbox + Zalo + form → Tư vấn (giờ hành chính) → Chốt đơn → Viettel Post giao hàng → Khách dùng hết hộp (~25 ngày) → KHÔNG AI NHẮC → im lặng`.
- Kết quả: bảng 2 cột "Bước — Điểm nghẽn". Trainer khoanh đỏ 3 nghẽn: inbox đêm không ai trực (phản hồi ~3h), content phập phù nên lead phụ thuộc tiền ads, không có cơ chế nhắc mua lại theo chu kỳ dùng hết hộp.
- Điểm nhấn: "Mỗi mũi tên là một chỗ khách rơi rớt. Ba chỗ khoanh đỏ này chính là tiền đang chảy ra ngoài."
- **Khác biệt B2C sản phẩm vs B2B dịch vụ (nói 30 giây):** phễu của MSX **không có bước 'khách đến nơi'** — thay vào đó có bước **GIAO HÀNG** (rủi ro riêng: hoàn đơn COD, giao chậm). Phễu 🚀 RocketAI thì ngược lại: ít khách hơn, chu kỳ chốt dài hàng tuần, có bước 'gửi proposal & ký hợp đồng'. **Học viên phải vẽ phễu THẬT của mình, không mượn phễu ngành khác.**

**Bước 4 (6') — Quét cơ hội AI theo 5 khu vực.**
- Làm gì: Paste Prompt 3. AI liệt kê ~15-20 cơ hội chia theo 5 khu vực.
- Kết quả: bảng có cột Khu vực | Cơ hội | Việc hiện tại ai làm | AI thay được bao nhiêu %.
- Điểm nhấn: đọc to 2-3 dòng bất ngờ (VD: "AI nhắn khách đúng ngày hộp trà sắp hết, kèm mẹo pha ngon hơn" — học viên thường không nghĩ tới, mà đây lại là mỏ tiền lớn nhất của MSX: tái mua 18% → 30%).

**Bước 5 (4') — Chấm ICE, chốt Top 10.**
- Làm gì: Paste Prompt 4. AI chấm ICE từng cơ hội, xếp hạng, đề xuất Top 10.
- Kết quả MSX (đọc to Top 5): 1) Chatbot trực inbox + FAQ 24/7 (13đ) · 2) Nhắc mua lại theo chu kỳ hết hộp (13đ) · 3) AI Content Factory 7 bài/tuần theo pillar câu chuyện Mẫu Sơn (12đ) · 4) Chuỗi follow-up khách hỏi giá chưa chốt (12đ) · 5) Dashboard inbox → đơn → doanh thu hàng tuần (11đ).
- Điểm nhấn: "Cả 5 cái này đều nằm trong lộ trình 28 ngày — tuần 2 làm content, tuần 3 làm chatbot + follow-up, tuần 4 làm nhắc mua lại + dashboard."

**Bước 6 (1') — Viết mục tiêu 28 ngày.**
- Làm gì: Paste Prompt 5. AI đề xuất mục tiêu SMART (Specific-Measurable-Achievable-Relevant-Time-bound — cụ thể, đo được, khả thi, liên quan, có hạn).
- Kết quả MSX: "Trong 28 ngày: tăng lead tự nhiên từ 85 → 130/tháng bằng content + chatbot 24/7, KHÔNG tăng ngân sách quảng cáo (giữ 8tr/tháng); rút thời gian phản hồi inbox từ ~3 giờ xuống <15 phút; nâng content từ 3 → 7 bài/tuần."

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core ≤ 2h)

**Cụm A — Business Model Canvas + Business Snapshot (35'):**
- [ ] Mở Template 1.0, đọc bản MSX BMC điền mẫu (5')
- [ ] Chạy Prompt 0, trả lời đủ 9 khối BMC cho DN mình (12')
- [ ] Rà BMC: mỗi khối có ít nhất 3 bullet cụ thể, không viết chung chung kiểu "mọi người đều là khách" (5')
- [ ] Mở Template 1.1, đọc bản MSX điền mẫu (3')
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

**Deliverable nộp (1 file duy nhất, 5 phần, Google Docs hoặc PDF):**
- `[Tên DN] — Ngày 01 — AI Foundation Snapshot`
- Ví dụ: `Mẫu Sơn Xanh — Ngày 01 — AI Foundation Snapshot`

**Deadline:** 23h59 cùng ngày. Nộp link vào thread cohort ngày 01. Bài nộp muộn được chấm nhưng không được chữa live hôm sau.

## 7. 📄 Template Đi Kèm

**Template 1.0 — Business Model Canvas.** 9 khối chuẩn: Customer Segments | Value Propositions | Channels | Customer Relationships | Revenue Streams | Key Resources | Key Activities | Key Partners | Cost Structure. Mỗi khối có sẵn câu hỏi gợi ý + bản MSX điền mẫu (đối chiếu bản đầy đủ trong vault demo: `00. Business Context/Business Model Canvas — Mẫu Sơn Xanh.md`). Đây là tài liệu gốc sẽ được đưa vào thư mục `01. Business Overview` của Knowledge Base Ngày 04.

**Template 1.1 — Business Snapshot (1 trang).** Các trường: Tên DN & địa điểm | Sản phẩm/dịch vụ chính (kèm giá) | Khách hàng chính (1-2 câu) | AOV & sản phẩm giá trị cao nhất | Biên lợi nhuận ước tính | Kênh bán chính | Kênh marketing chính | Đội ngũ (số người, ai làm sale/marketing) | 3 vấn đề lớn nhất | Doanh thu tháng gần nhất (tùy chọn, có thể ghi khoảng). *Bản điền mẫu MSX nằm ngay trong template.*

**Template 1.2 — Business Process Map.** Cấu trúc: bảng 4 cột — Bước (theo dòng khách hàng) | Ai/công cụ đang xử lý | Điều gì đang ổn | 🔴 Điểm nghẽn. Kèm dòng flow tổng: `Kênh → Lead → Tư vấn → Mua → Sử dụng → Chăm sóc → Mua lại/Giới thiệu`. **Lưu ý:** DN sản phẩm (như MSX) thay bước "Sử dụng" bằng "Giao hàng → Sử dụng"; DN dịch vụ có bước "khách đến nơi"; DN B2B có bước "gửi proposal → ký hợp đồng".

**Template 1.3 — Top 10 AI Use Cases.** Bảng 7 cột: # | Đầu việc AI hóa | Khu vực (M/S/CS/Ops/Data) | Impact (1-5) | Confidence (1-5) | Ease (1-5) | Tổng ICE. Dưới bảng: 3 dòng "Use case này sẽ được xây ở ngày nào trong 28 ngày" (trainer map giúp buổi sau nếu học viên chưa biết).

**Template 1.4 — Mục tiêu 28 ngày.** Trường: Mục tiêu chính (1 câu, có con số + thời hạn) | Chỉ số 1/2/3 (hiện tại → mục tiêu → cách đo) | Lý do mục tiêu này quan trọng nhất lúc này (2-3 câu). *Nối thẳng với `Baseline & Mục Tiêu 28 Ngày.md` đã điền ở Ngày 00 — không đặt mục tiêu tách rời khỏi 10 số gốc.*

*(Cả 5 template đều có sẵn bản MSX điền mẫu để học viên "nhìn bài đúng" trước khi điền — dựng sẵn 80%, học viên điền 20%.)*

### Bản điền mẫu Template 1.1 — 🍵 MSX Group (chiếu trong buổi live)

> 🧪 *(Số demo minh hoạ — không phải số kinh doanh thật của MSX)*
>
> **Tên DN & địa điểm:** Mẫu Sơn Xanh (MSX Group) — Công ty CP Lối vào Mẫu Sơn Xanh; dược liệu & trà thảo mộc; gốc câu chuyện tại thôn Bó Pằm, xã Mẫu Sơn, Lạng Sơn. Khởi nguồn 2024.
> **Sản phẩm/dịch vụ chính:** Trà Hoa Sâm Nam 369k/hộp · Trà Mẩy Gòm An Giấc 359k/hộp · Viên Sâm Nam Hà Thủ Ô Mật Ong Vừng 599k/hộp · combo mua 3 tặng 1 · đơn sỉ đại lý từ 50 sản phẩm (chiết khấu bậc số lượng). *(3 dòng chanh rừng/viên nhàu tạm hết hàng.)*
> **Khách hàng chính:** 3 phân khúc — ① người tiêu dùng chăm sóc sức khỏe tự nhiên (28-55, đô thị, mua online, đọc review kỹ trước khi mua); ② người mua quà biếu sức khỏe (Tết, đối tác, cha mẹ); ③ đại lý & quà tặng doanh nghiệp.
> **AOV & sản phẩm giá trị cao nhất:** AOV bán lẻ 520k/đơn; sản phẩm giá trị cao nhất là Viên Sâm Nam 599k; **đơn sỉ/quà tặng B2B đóng góp ~47tr/tháng — gần một nửa doanh thu**.
> **Biên lợi nhuận ước tính:** ~40-45% với bán lẻ, thấp hơn với đơn sỉ (ước lượng, chưa tách chi phí chính xác).
> **Kênh bán chính:** Website mausonxanh.com + inbox Facebook + Zalo OA (0822.928.988) + hội chợ OCOP + đại lý.
> **Kênh marketing chính:** Facebook (2 bài/tuần) + TikTok (1 video/tuần) — đăng không đều, khi rảnh mới đăng. Ads Meta ~8tr/tháng. Tổng ~85 lead mới/tháng (inbox FB 52 + Zalo 21 + form web 12), chốt 22%.
> **Đội ngũ:** Founder Nguyễn Hoàng Hưng tự làm phần lớn marketing (~12h/tuần) + đội vận hành thu hái/đóng gói/xử lý đơn. Không có nhân sự marketing chuyên trách.
> **3 vấn đề lớn nhất:** (1) inbox phản hồi chậm ~3 giờ, đêm không ai trực; (2) content phập phù (3 bài/tuần, tốn 12h của founder) → lead phụ thuộc tiền ads; (3) chỉ 18% khách quay lại dù điểm hài lòng 4,7/5 — không có cơ chế nhắc mua lại khi khách dùng hết hộp (~25 ngày).
> **Doanh thu tháng gần nhất:** ~95tr (bán lẻ online ~48tr + đại lý/quà tặng B2B ~47tr).

### Bản điền mẫu Template 1.3 — Top 10 của 🍵 MSX (rút gọn 5 dòng đầu)

| # | Đầu việc AI hóa | Khu vực | I | C | E | Tổng |
|---|---|---|---|---|---|---|
| 1 | Chatbot trực inbox + trả FAQ sản phẩm 24/7 | Sales | 5 | 4 | 4 | 13 |
| 2 | Nhắc khách mua lại đúng chu kỳ hết hộp (~25 ngày) | CSKH | 5 | 4 | 4 | 13 |
| 3 | AI Content Factory 7 bài/tuần theo pillar câu chuyện Mẫu Sơn | Marketing | 4 | 4 | 4 | 12 |
| 4 | Chuỗi follow-up khách hỏi giá chưa chốt (3 chạm/7 ngày) | Sales | 4 | 4 | 4 | 12 |
| 5 | Dashboard tuần: inbox → đơn → doanh thu trên 1 trang | Đo lường | 4 | 4 | 3 | 11 |

*(Dòng 6-10 của MSX: kịch bản video ngắn kể chuyện vùng nguyên liệu cho TikTok · landing page riêng từng sản phẩm + lead magnet · agent phân loại lead sỉ/đại lý B2B · kịch bản xử lý phản đối "sao đắt hơn trà ngoài chợ" · proposal quà tặng doanh nghiệp mùa Tết. Học viên xem bản đầy đủ trong template.)*

## 8. 🤖 Prompt Mẫu

### Prompt 0 — AI phỏng vấn để tạo Business Model Canvas

```
[VAI TRÒ] Bạn là chuyên gia Business Model Canvas và AIOS cho SME Việt Nam. Nhiệm vụ của bạn là phỏng vấn chủ doanh nghiệp để dựng BMC 9 khối đủ rõ cho đội AI Agent dùng làm bối cảnh gốc.

[BỐI CẢNH] Tôi đang cài AI Marketing & Sales OS vận hành bằng Agent cho doanh nghiệp. Trước khi dựng Agent, tôi cần Business Model Canvas rõ ràng để AI hiểu mô hình kinh doanh, khách hàng mục tiêu, offer, kênh bán, nguồn lực và dòng tiền.

[NHIỆM VỤ] Hỏi tôi lần lượt 9 khối BMC, mỗi lần chỉ hỏi 1 nhóm câu hỏi rồi chờ tôi trả lời:
1. Customer Segments — khách hàng mục tiêu là ai, nhóm nào mang nhiều tiền nhất?
2. Value Propositions — khách mua kết quả gì, vì sao chọn tôi thay vì đối thủ?
3. Channels — khách biết đến, tương tác, mua và nhận sản phẩm/dịch vụ qua kênh nào?
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
[VAI TRÒ] Bạn là một chuyên gia tư vấn chiến lược cho doanh nghiệp nhỏ (SME) tại Việt Nam, giỏi đặt câu hỏi để rút ra bức tranh kinh doanh rõ ràng.

[BỐI CẢNH] Tôi là chủ một doanh nghiệp nhỏ, đang tham gia chương trình 28 ngày xây hệ thống AI Marketing & Sales. Hôm nay tôi cần một bản Business Snapshot (bản chụp doanh nghiệp) 1 trang.

[NHIỆM VỤ] Hãy phỏng vấn tôi LẦN LƯỢT TỪNG CÂU MỘT (hỏi xong chờ tôi trả lời rồi mới hỏi tiếp) theo đúng 10 chủ đề: (1) tên DN + địa điểm + ngành; (2) danh sách sản phẩm/dịch vụ chính kèm giá; (3) khách hàng chính là ai; (4) giá trị đơn trung bình và sản phẩm giá trị cao nhất; (5) biên lợi nhuận ước tính; (6) kênh bán hàng chính; (7) kênh marketing chính và hiệu quả hiện tại (số lead/tháng); (8) đội ngũ — ai đang làm marketing, ai làm sale; (9) 3 vấn đề lớn nhất hiện nay; (10) doanh thu tháng gần nhất hoặc khoảng doanh thu. Sau câu 10, tổng hợp thành Business Snapshot.

[DỮ LIỆU ĐẦU VÀO] Thông tin ban đầu về doanh nghiệp của tôi: {{2-3 câu giới thiệu ngắn về DN của bạn}}

[ĐỊNH DẠNG ĐẦU RA] Sau khi phỏng vấn xong: một bản Business Snapshot dài đúng 1 trang, có 10 đề mục in đậm tương ứng 10 chủ đề, mỗi mục 1-3 câu, giữ nguyên số liệu tôi cung cấp.

[RÀNG BUỘC] Không tự bịa số liệu — nếu tôi trả lời "không biết", ghi rõ "[cần bổ sung]". Nếu câu trả lời của tôi mơ hồ, hỏi lại 1 câu làm rõ trước khi sang chủ đề tiếp theo. Viết tiếng Việt, giọng ngắn gọn.
```

**Ví dụ đã điền (🍵 MSX):** `{{2-3 câu giới thiệu ngắn}}` → "Tôi là Hưng, founder Mẫu Sơn Xanh — công ty dược liệu & trà thảo mộc từ vùng Mẫu Sơn, Lạng Sơn. Chúng tôi bán 6 dòng sản phẩm (trà túi lọc, viên dược liệu cô đặc, đặc sản chanh rừng), giá 359k-599k/hộp, đạt OCOP 3★. Khách mua online qua website, Facebook, Zalo; ngoài ra có kênh đại lý và quà tặng doanh nghiệp."

**Ví dụ đối chiếu B2B (🚀 RocketAI):** `{{2-3 câu giới thiệu ngắn}}` → "Tôi là Tony, CEO Rocket AI Solutions — chúng tôi chuyển giao hệ điều hành AI Marketing & Sales cho SME Việt trong 28 ngày. 3 gói: OS Transfer 12tr, OS Installed 25tr, OS Managed 50tr+. Khách là chủ spa/dịch vụ 5-15 nhân viên, doanh thu 300-800tr/tháng." — *Cùng 1 prompt, nhưng Snapshot ra sẽ khác hẳn ở AOV, số lead, chu kỳ chốt.*

### Prompt 2 — Vẽ Business Process Map + chỉ điểm nghẽn

```
[VAI TRÒ] Bạn là chuyên gia thiết kế quy trình kinh doanh (business process) cho SME Việt Nam.

[BỐI CẢNH] Tôi vừa hoàn thành Business Snapshot của doanh nghiệp mình. Tôi cần nhìn thấy toàn bộ dòng chảy khách hàng để biết tiền đang rơi rớt ở đâu.

[NHIỆM VỤ] Từ Business Snapshot dưới đây: (1) vẽ Business Process Map dạng chuỗi text theo dòng khách hàng: Kênh → Lead → Tư vấn → Mua → Nhận hàng/Sử dụng → Chăm sóc → Mua lại/Giới thiệu, mô tả đúng cách DN tôi ĐANG vận hành (kể cả bước đang thiếu — ghi rõ "KHÔNG CÓ"); (2) lập bảng 4 cột: Bước | Ai/công cụ đang xử lý | Đang ổn ở điểm gì | Điểm nghẽn; (3) chọn ra 3 điểm nghẽn nghiêm trọng nhất, giải thích vì sao mỗi nghẽn làm mất tiền, ước lượng mức thiệt hại tương đối.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán toàn bộ Business Snapshot từ Prompt 1}}

[ĐỊNH DẠNG ĐẦU RA] Phần 1: dòng flow bằng mũi tên. Phần 2: bảng markdown 4 cột. Phần 3: danh sách "🔴 Top 3 điểm nghẽn" — mỗi nghẽn 3 dòng: hiện tượng / vì sao mất tiền / mất khoảng bao nhiêu cơ hội mỗi tháng.

[RÀNG BUỘC] Chỉ dựa trên dữ liệu tôi đưa, không suy diễn thêm sản phẩm/dịch vụ DN không có. Với bước "KHÔNG CÓ", tự động coi là ứng viên điểm nghẽn. Phễu phải khớp mô hình thật của tôi: DN bán sản phẩm có bước GIAO HÀNG; DN dịch vụ có bước KHÁCH ĐẾN NƠI; DN B2B có bước GỬI PROPOSAL & KÝ HỢP ĐỒNG — đừng áp nhầm phễu ngành khác. Tiếng Việt, tối đa 500 từ.
```

**Ví dụ đã điền (🍵 MSX):** dán Business Snapshot MSX → AI trả về flow `FB/TikTok + Website + Hội chợ → Inbox FB (52) + Zalo OA (21) + form web (12) = 85 lead/tháng → Tư vấn tay, giờ hành chính (phản hồi ~3h, đêm không ai trực) → Chốt 22% (~19 đơn) → Viettel Post giao hàng → Khách dùng hết hộp ~25 ngày → KHÔNG CÓ nhắc mua lại → chỉ 18% quay lại` và Top 3 nghẽn: inbox đêm không ai trực (mất lead giờ vàng 21-23h), content phập phù nên lead phụ thuộc 8tr ads/tháng, không nhắc mua lại (mỏ tiền lớn nhất — 82% khách hài lòng nhưng không quay lại).

### Prompt 3 — Quét cơ hội AI hóa theo 5 khu vực

```
[VAI TRÒ] Bạn là chuyên gia chuyển đổi AI cho SME Việt Nam (bán sản phẩm online, dịch vụ tư vấn, spa, nha khoa, giáo dục, gym), hiểu rõ giới hạn thực tế: chủ DN bận, không rành công nghệ, ngân sách thấp.

[BỐI CẢNH] Doanh nghiệp của tôi đã có Business Snapshot và Process Map kèm điểm nghẽn. Tôi cần bản đồ đầy đủ những việc AI có thể làm thay hoặc làm cùng con người trong DN.

[NHIỆM VỤ] Liệt kê 15-20 cơ hội AI hóa, chia theo đúng 5 khu vực: (1) Marketing, (2) Sales, (3) Chăm sóc khách hàng, (4) Vận hành nội bộ, (5) Đo lường & ra quyết định. Ưu tiên các cơ hội trực tiếp vá 3 điểm nghẽn tôi nêu. Mỗi khu vực tối thiểu 3 cơ hội.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán Business Snapshot}}. Top 3 điểm nghẽn: {{dán 3 điểm nghẽn từ Prompt 2}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng markdown 5 cột: Khu vực | Cơ hội AI hóa (tên ngắn + 1 câu mô tả) | Việc này hiện ai đang làm / hay không ai làm | AI thay được ~bao nhiêu % | Vá điểm nghẽn nào (ghi số 1/2/3 hoặc "—").

[RÀNG BUỘC] Chỉ đề xuất việc khả thi với công cụ phổ thông (chatbot, AI viết content, AI phân tích bảng tính) — không đề xuất giải pháp cần lập trình riêng hay phần cứng. Không đề xuất AI thay việc cần bàn tay/giác quan con người (thu hái, nếm thử, kiểm định, trị liệu). Nếu DN thuộc ngành sức khỏe/dược liệu/thực phẩm: mọi cơ hội liên quan nội dung phải giữ ngôn ngữ "hỗ trợ", không cam kết chữa bệnh. Tiếng Việt.
```

**Ví dụ đã điền (🍵 MSX):** kết quả tiêu biểu — Marketing: AI viết 7 bài/tuần theo 5 pillar câu chuyện Mẫu Sơn; AI viết kịch bản video ngắn quay vùng nguyên liệu cho TikTok. Sales: chatbot trực inbox + FAQ 24/7; kịch bản xử lý phản đối "sao đắt hơn trà ngoài chợ"; chuỗi follow-up khách hỏi giá chưa chốt. CSKH: nhắc mua lại đúng chu kỳ hết hộp; hướng dẫn cách pha & bảo quản sau khi giao hàng. Vận hành: agent phân loại lead sỉ/đại lý B2B; AI soạn proposal quà tặng doanh nghiệp. Đo lường: dashboard inbox → đơn → doanh thu theo tuần.

### Prompt 4 — Chấm ICE và chốt Top 10

```
[VAI TRÒ] Bạn là cố vấn ưu tiên hóa danh mục dự án cho chủ SME, nghiêm khắc với việc "ôm đồm".

[BỐI CẢNH] Tôi có danh sách 15-20 cơ hội AI hóa. Trong 28 ngày tôi chỉ triển khai được 10. Chương trình của tôi tập trung Marketing & Sales.

[NHIỆM VỤ] (1) Chấm mỗi cơ hội theo ICE: Impact — tác động đến doanh thu/tiết kiệm thời gian (1-5); Confidence — độ chắc chắn làm được với dữ liệu hiện có (1-5); Ease — độ dễ với người không rành công nghệ (1-5). (2) Xếp hạng theo tổng điểm. (3) Đề xuất Top 10, đảm bảo: ≥4 use case thuộc Marketing/Sales; ≥7 use case nằm trong nhóm chuẩn của lộ trình (content, hình ảnh/video, chatbot tư vấn, phân loại lead, kịch bản sale, follow-up tự động, CSKH, báo cáo/dashboard). (4) Với mỗi use case trong Top 10, ghi 1 câu "kết quả kỳ vọng sau 28 ngày".

[DỮ LIỆU ĐẦU VÀO] Danh sách cơ hội: {{dán bảng từ Prompt 3}}. Bối cảnh thêm: {{1-2 câu về nguồn lực — VD: chỉ mình tôi làm, mỗi ngày có 2h}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng: # | Use case | Khu vực | I | C | E | Tổng | Kết quả kỳ vọng. Sau bảng: 2-3 dòng giải thích vì sao các use case bị loại.

[RÀNG BUỘC] Điểm phải có căn cứ từ dữ liệu tôi đưa (VD: Impact 5 vì vá nghẽn khiến 82% khách không quay lại). Không cho hai use case trùng bản chất cùng vào Top 10. Tối đa 3 use case được ≥13 điểm — ép phân hóa, không cho cả bảng 14-15. Tiếng Việt.
```

**Ví dụ đã điền (🍵 MSX):** Top 3 kết quả — #1 Chatbot trực inbox + FAQ 24/7 (I5 C4 E4 = 13; kỳ vọng: phản hồi <15 phút, 24/7, không mất lead giờ đêm); #2 Nhắc mua lại theo chu kỳ hết hộp (I5 C4 E4 = 13; kỳ vọng: tỷ lệ khách quay lại 18% → 30%); #3 AI Content Factory (I4 C4 E4 = 12; kỳ vọng: 7 bài/tuần đăng đều, founder chỉ tốn 3h thay vì 12h).

### Prompt 5 — Viết mục tiêu 28 ngày SMART

```
[VAI TRÒ] Bạn là huấn luyện viên mục tiêu cho chủ SME, chuyên biến mong muốn mơ hồ thành mục tiêu SMART (cụ thể — đo được — khả thi — liên quan — có thời hạn).

[BỐI CẢNH] Tôi bắt đầu chương trình 28 ngày xây AI Marketing & Sales OS. Tôi cần 1 mục tiêu chính + 3 chỉ số để cuối chương trình biết mình thành công hay không.

[NHIỆM VỤ] Từ dữ liệu dưới đây, đề xuất 3 phương án mục tiêu chính (an toàn / cân bằng / tham vọng), mỗi phương án kèm đúng 3 chỉ số dạng "hiện tại → mục tiêu → cách đo". Sau đó khuyến nghị 1 phương án và giải thích trong 3 câu.

[DỮ LIỆU ĐẦU VÀO] Baseline 10 số đã điền ở Ngày 00: {{dán}}. Business Snapshot: {{dán}}. Top 10 AI Use Cases: {{dán}}. Mong muốn cá nhân của tôi: {{1-2 câu — VD: tôi muốn bớt phụ thuộc tiền quảng cáo}}.

[ĐỊNH DẠNG ĐẦU RA] 3 khối phương án, mỗi khối: Mục tiêu chính (1 câu có con số + mốc 28 ngày) + bảng 3 chỉ số (Chỉ số | Hiện tại | Mục tiêu | Cách đo). Cuối: "Khuyến nghị" 3 câu.

[RÀNG BUỘC] Chỉ số phải LẤY TỪ 10 số baseline Ngày 00 (không tự chế chỉ số mới không có số gốc) và đo được bằng công cụ chủ DN đang có (đếm inbox, sổ đơn, doanh thu). Cách đo ở Ngày 28 phải y hệt cách đo ở Ngày 00. Mục tiêu doanh thu tăng không quá 30% trong 28 ngày (thực tế). Tiếng Việt.
```

**Ví dụ đã điền (🍵 MSX):** phương án cân bằng được chọn — "Sau 28 ngày, MSX tăng lead tự nhiên từ 85 → 130/tháng bằng hệ thống content kể chuyện Mẫu Sơn + chatbot 24/7, KHÔNG tăng ngân sách quảng cáo (giữ 8tr/tháng)." Chỉ số: (1) lead mới/tháng: 85 → 130, đo bằng inbox FB + Zalo OA + form web; (2) thời gian phản hồi inbox: ~3 giờ → <15 phút, đo bằng chỉ số phản hồi Fanpage + log chatbot; (3) content/tuần: 3 → 7 bài, đếm bài đăng FB + TikTok + Zalo. *(Đối chiếu bản đầy đủ: `Baseline & Mục Tiêu 28 Ngày — MSX (mẫu)` trong vault demo.)*

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-01: Rà soát cơ hội AI hóa hàng quý**
- **Khi nào:** Ngày đầu mỗi quý (hoặc khi DN mở dòng sản phẩm mới / thêm kênh mới).
- **Ai làm:** Chủ DN (30-45').
- **Input:** Business Snapshot quý trước + số liệu 3 tháng (lead, tỷ lệ chốt, doanh thu).
- **Các bước:** (1) Cập nhật Business Snapshot — sửa số liệu mới; (2) Chạy lại Prompt 2 xem điểm nghẽn có dịch chuyển không; (3) Chạy Prompt 3 + 4, so Top 10 mới với Top 10 cũ; (4) Chọn 1-2 use case mới để triển khai trong quý; (5) Lưu bản mới vào thư mục Knowledge Base `01. Business Overview` (sẽ tạo ở Ngày 04).
- **Output:** Business Snapshot phiên bản mới + Top 10 cập nhật + 1-2 use case triển khai quý này.
- **Tần suất:** 4 lần/năm.

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Đủ 5 phần trong 1 file (mỗi phần thiếu −6): BMC đủ 9 khối, mỗi khối ≥3 bullet (6đ) · Business Snapshot đủ 10 trường (8đ) · Process Map đủ chuỗi từ Kênh đến Mua lại (8đ) · Top 10 use case có đủ điểm I/C/E từng dòng (4đ) · Mục tiêu 28 ngày có 1 mục tiêu + 3 chỉ số (4đ) |
| Chất lượng & độ sâu | 30 | Process Map đánh dấu ≥3 điểm nghẽn kèm lý do mất tiền (10đ) · ≥7/10 use case thuộc nhóm lộ trình 28 ngày (10đ) · cả 3 chỉ số có đủ bộ ba "hiện tại → mục tiêu → cách đo" VÀ lấy từ 10 số baseline Ngày 00 (10đ) |
| Cá nhân hoá vào DN thật | 25 | Có ≥5 con số thật của DN (giá, số lead/tháng, số nhân sự, AOV, doanh thu/khoảng doanh thu) (15đ) · không còn placeholder kiểu "[cần bổ sung]"/văn mẫu AI chung chung — kiểm tra bằng cách đọc 3 dòng bất kỳ phải thấy tên DN/ngành cụ thể (10đ) |
| Dùng được ngay | 15 | Top 10 xếp hạng rõ #1-#10, không đồng hạng tràn lan (>3 cặp đồng hạng = trừ) (8đ) · file đặt tên đúng quy ước, chia sẻ mở được không cần xin quyền (7đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Dán nguyên output AI chưa sửa — số liệu bịa (VD: AI ghi "200 lead/tháng" trong khi thực tế 85): −10.
2. Top 10 toàn use case ngoài lộ trình (app riêng, AI phân tích hoạt chất, phần cứng...): −10.
3. Mục tiêu không đo được ("tăng nhận diện thương hiệu"): −8.
4. Process Map chỉ có flow mũi tên, không có điểm nghẽn: −8.
5. **Mượn phễu ngành khác** (DN bán sản phẩm online mà vẽ bước "khách đến cửa hàng tư vấn"): −8.
6. Nộp 5 file rời thay vì 1 file 5 phần: −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Tôi không biết chính xác biên lợi nhuận / số lead mỗi tháng thì điền sao?**
→ Điền KHOẢNG ước lượng ("70-90 lead/tháng", "biên ~40%") kèm ghi chú "ước lượng". Cấm bỏ trống, cấm để AI bịa. Việc bạn không đo được chính là một điểm nghẽn — ghi nó vào Process Map. *(Bản mẫu MSX làm đúng cách này: mỗi số đều ghi rõ nguồn lấy, số chưa chắc thì ghi "ước lượng".)*

**Q2: Doanh nghiệp tôi có 2-3 mảng (vừa bán lẻ vừa bán sỉ đại lý), làm cho mảng nào?**
→ Chọn 1 mảng đóng góp doanh thu lớn nhất hoặc bạn muốn tăng trưởng nhất, làm xuyên suốt 28 ngày cho mảng đó. Mảng phụ chỉ nhắc 1 dòng trong Snapshot. *(MSX là ví dụ đúng tình huống này: bán lẻ 48tr vs đại lý/B2B 47tr — gần bằng nhau. MSX chọn bán lẻ online làm trục 28 ngày vì đó là nơi hệ thống AI tạo đòn bẩy lớn nhất; kênh đại lý giữ nguyên cách làm cũ trong 28 ngày này.)*

**Q3: Tôi chưa có tài khoản RocketAgent / chưa quen công cụ AI nào?**
→ Hôm nay dùng ChatGPT hoặc Claude bản web miễn phí đều chạy được toàn bộ 5 prompt. RocketAgent bắt buộc từ Ngày 04 (Knowledge Base) — đăng ký trước theo hướng dẫn trong nhóm.

**Q4: Top 10 của tôi có nên cho use case "AI chấm công / AI kế toán" không?**
→ Không nên chiếm chỗ — chương trình này xây Marketing & Sales OS. Ghi các ý đó vào mục "Bãi đỗ ý tưởng" cuối file để làm sau 28 ngày.

**Q5: Tôi làm B2B (tư vấn, agency, bán sỉ), khung này có áp dụng được không?**
→ Được — dòng khách vẫn là Kênh → Lead → Tư vấn → Chốt → Triển khai → Tái ký. Chỉ khác: chu kỳ chốt dài hơn, có thêm bước "gửi proposal & ký hợp đồng", AOV cao hơn nhiều nhưng số lead ít hơn. Xem case 🚀 RocketAI trong [[Case Study Mẫu — RocketAI & MSX Group]] để đối chiếu — đó chính là một DN B2B thật.

**Q6: 2 tiếng không đủ làm hết thì sao?**
→ Ưu tiên đúng thứ tự A → D trong checklist. Bonus (AI Opportunity Map đầy đủ) bỏ qua không bị trừ điểm.

**Q7: AI trả lời tiếng Anh hoặc lẫn tiếng Anh thì làm sao?**
→ Thêm vào cuối prompt dòng: "Trả lời hoàn toàn bằng tiếng Việt." Nếu vẫn lẫn, gõ tiếp: "Viết lại toàn bộ bằng tiếng Việt." Đây là lý do mọi prompt mẫu của chương trình đều có ràng buộc ngôn ngữ sẵn — đừng xóa dòng Constraint (ràng buộc).

**Q8: Tôi có cần nộp cả lịch sử chat với AI không?**
→ Không. Chỉ nộp file thành phẩm 5 phần. Nhưng NÊN lưu link chat lại cho mình — Ngày 05 sẽ dạy cách biến các đoạn chat tốt thành prompt library (thư viện câu lệnh).

**Lỗi thường gặp:**
1. **Snapshot viết như bài PR** ("thương hiệu dược liệu uy tín hàng đầu, tâm huyết với sức khỏe cộng đồng") — *Phát hiện:* không có con số nào trong 3 dòng liên tiếp. — *Sửa:* mỗi mục phải có ít nhất 1 con số hoặc danh từ cụ thể; chạy lại Prompt 1 và trả lời bằng số.
2. **Process Map vẽ quy trình LÝ TƯỞNG thay vì quy trình THẬT** — *Phát hiện:* map có bước "gửi email chăm sóc định kỳ" nhưng DN chưa từng gửi email nào. — *Sửa:* nguyên tắc "vẽ cái đang có, kể cả cái xấu"; bước chưa có ghi "KHÔNG CÓ".
3. **Chấm ICE cả 10 use case đều 14-15 điểm** — *Phát hiện:* không có use case nào dưới 12. — *Sửa:* ép phân phối — tối đa 3 use case được ≥13; tự hỏi "nếu chỉ được làm 1 cái, tôi làm cái nào?" rồi chấm lại từ đó xuống.
4. **Mượn phễu của ngành khác** — *Phát hiện:* DN bán hàng online mà Process Map có bước "khách đến cửa hàng, nhân viên tư vấn trực tiếp"; hoặc DN dịch vụ mà có bước "giao hàng Viettel Post". — *Sửa:* vẽ lại từ chính hành trình khách của bạn tuần trước; nếu bí, kể lại 1 ca khách gần nhất từ lúc họ biết đến DN cho tới lúc trả tiền.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 00 — Install Pack & Baseline]] — mang theo Baseline 10 số đã điền; mục tiêu 28 ngày hôm nay phải suy ra từ chính 10 số đó · Ngày sau: [[Ngày 02 — Chân Dung Khách Hàng & Customer Journey]]
- Case study dùng trong bài: [[Case Study Mẫu — RocketAI & MSX Group]] · Vault demo đối chiếu: `ai-marketing-system-msx-demo/`
- Tài sản hôm nay được dùng lại ở:
	- **Business Snapshot** → đầu vào Prompt phỏng vấn Avatar (Ngày 02), tài liệu số 1 của Knowledge Base (Ngày 04), phần mở đầu Instruction của AI Business Brain (Ngày 06).
	- **Business Process Map** → khung thiết kế Customer Journey (Ngày 02) và điểm đặt chatbot/follow-up (Tuần 3-4).
	- **Top 10 AI Use Cases** → checklist nghiệm thu toàn chương trình; Demo Day 1 (Ngày 07) sẽ đối chiếu tiến độ theo danh sách này.
	- **Mục tiêu 28 ngày** → thước đo trong Foundation Scorecard (Ngày 07) và Dashboard (Tuần 4); đo lại ở Ngày 28 bằng đúng cách đo đã ghi.
