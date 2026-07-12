---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 1
day: 2
core-output: "Customer Avatar Profile 1 chân dung chính (8 trường + Mức nhận thức + ≥3 câu nguyên văn) · Pain-Desire-Fear-Objection Map (≥5 mục/nhóm + ≥3 cặp Fear↔Objection) · Customer Journey Map 7 giai đoạn × 4 cột"
---

# Ngày 02 — Chân Dung Khách Hàng & Customer Journey

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Đào sâu từng phân khúc trong `00. Business Context/MHKD/Phân Khúc Khách Hàng/PK*.md` — PDFO Map + Journey ghi thẳng vào file PK tương ứng; bộ câu hỏi khảo sát lưu `04. Resources/Templates/`.

> Hôm nay bạn xây "hồ sơ mật" về khách hàng mục tiêu: họ đau gì, muốn gì, sợ gì, viện cớ gì — và vẽ hành trình 7 giai đoạn từ lúc họ chưa biết mình có vấn đề đến lúc mua lại và giới thiệu. Đây là nhiên liệu cho MỌI content, chatbot, kịch bản sale phía sau.

## 1. 🎯 Mục Tiêu Ngày Học

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **Customer Avatar Profile (hồ sơ chân dung khách hàng)** — 1 chân dung chính, đủ 8 trường nhân khẩu + bối cảnh (trong đó trường "Câu nói vàng" chứa ≥3 câu nguyên văn của khách thật), cộng trường thứ 9: **Mức nhận thức** (1 trong 5 mức — xem Khối 3).
- ✅ **Pain–Desire–Fear–Objection Map (bản đồ Nỗi đau – Mong muốn – Nỗi sợ – Phản đối)** — mỗi nhóm tối thiểu 5 mục, viết bằng NGÔN NGỮ KHÁCH HÀNG (câu khách thật sự nói), không phải ngôn ngữ chủ DN + **≥3 cặp Fear↔Objection được nối** (AI sẽ tạo dư 7 mục/4 cặp để bạn lọc — xem Prompt 2).
- ✅ **Customer Journey Map (bản đồ hành trình khách hàng)** — **bảng chuẩn 7 giai đoạn × 4 cột: Giai đoạn / Khách nghĩ gì / DN cần làm gì / Kênh** + đánh dấu ⚡ ≥2 giai đoạn DN đang bỏ trống.

**Bonus Output (nâng cao):**
- ⭐ **Mở rộng "Câu nói vàng" lên 10 câu nguyên văn** — kho hook content cho Tuần 2.
- ⭐ **Bộ 30 câu hỏi nghiên cứu khách hàng** — 10 phỏng vấn khách cũ, 10 khảo sát khách tiềm năng, 10 cho đội sale khai thác nhu cầu.
- ⭐ Chân dung phụ thứ 2 (nếu DN có 2 tệp khách rõ rệt).

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Customer Avatar là gì & vì sao thiếu nó thì AI viết dở (5')
- **Ý chính:** Customer Avatar (chân dung khách hàng) = bản mô tả MỘT con người đại diện cho tệp khách tốt nhất, cụ thể đến mức "gọi được tên". AI không viết dở — AI thiếu dữ liệu. Cho AI avatar mơ hồ ("phụ nữ quan tâm làm đẹp") thì nhận content mơ hồ.
- **Cách giảng:** Chiếu 2 output AI cạnh nhau — cùng 1 prompt viết bài, một bên input "người quan tâm sức khỏe", một bên input avatar chị Hương đầy đủ (xem mục 4). Sự khác biệt tự nói lên tất cả.
- **Ví dụ 🍵 MSX:** MSX Group (Mẫu Sơn Xanh — học viên thật của chương trình, bán trà thảo mộc & dược liệu Mẫu Sơn online, xem [[Case Study Mẫu — RocketAI & MSX Group]]). Khách tốt nhất của MSX không phải "người quan tâm sức khỏe 25-60" mà là "**chị Hương, 40 tuổi, nhân viên văn phòng Hà Nội**, khó ngủ vì căng thẳng công việc, từng mua trà thảo mộc trôi nổi uống vài lần rồi bỏ, chỉ xuống tiền khi chắc nguồn gốc — vì còn mua cho bố mẹ".
- **Đối chiếu B2B 🚀 RocketAI (công ty của người dạy — bán dịch vụ cài hệ thống AI cho SME):** avatar khách của RocketAI là chị Mai, 35 tuổi, chủ Spa ABC 10 nhân viên, doanh thu ~500tr/tháng. B2B khác B2C ở chỗ **người mua ≠ người dùng**: chị Mai quyết định chi tiền nhưng nhân viên spa mới là người dùng hệ thống hằng ngày — avatar chính luôn là người RA QUYẾT ĐỊNH (xem FAQ Q5).

### Khối 2 — Bộ tứ Pain–Desire–Fear–Objection (8')
- **Ý chính:** 4 lớp tâm lý quyết định mua hàng: **Pain (nỗi đau)** — điều đang khó chịu hằng ngày; **Desire (mong muốn)** — kết quả + con người họ muốn trở thành; **Fear (nỗi sợ)** — điều ngăn họ hành động; **Objection (phản đối)** — lý do cụ thể họ nói ra để từ chối. Pain viết content thu hút, Desire viết offer, Fear viết bảo chứng, Objection viết kịch bản sale.
- **Cách giảng:** Phân biệt Fear và Objection bằng ví dụ MSX: Fear = "sợ hàng thảo mộc trôi nổi, công dụng bị thổi phồng" (cảm xúc ngầm, ít khi nói ra); Objection = "sao đắt hơn trà ngoài siêu thị?" (câu nói ra miệng). Objection là mặt nạ của Fear — kịch bản sale phải xử lý cả hai.
- **Quy tắc vàng:** Viết bằng câu khách NÓI, trong ngoặc kép. "Dạo này ngủ không sâu, sáng dậy vẫn mệt" mạnh gấp 10 lần "khách hàng có nhu cầu cải thiện giấc ngủ".

### Khối 3 — Phân nhóm theo mức độ nhận thức (5 Levels of Awareness) (5')
- **Ý chính:** 5 mức nhận thức (theo Eugene Schwartz): (1) Unaware (chưa biết mình có vấn đề) → (2) Problem Aware (biết vấn đề) → (3) Solution Aware (biết có giải pháp) → (4) Product Aware (biết sản phẩm của bạn) → (5) Most Aware (chỉ chờ lý do mua). Mỗi mức cần một loại nội dung khác nhau.
- **Ví dụ MSX:** Mức 2 cần bài "5 lý do dân văn phòng sau 35 tuổi ngủ không sâu"; mức 4 cần review khách thật + chứng nhận OCOP 3★ + video vùng nguyên liệu Mẫu Sơn; gửi bảng giá combo cho người mức 2 = đốt tiền.
- **Nối vào deliverable:** mức nhận thức của avatar được ghi thành trường thứ 9 trong [[Template 2.1 — Customer Avatar Profile]] (Prompt 1 tự đề xuất, bạn xác nhận/sửa) — Tuần 2 dùng đúng trường này để chọn loại content mở đầu.

### Khối 4 — Customer Journey 7 giai đoạn (7')
- **Ý chính:** 7 giai đoạn: Chưa biết vấn đề → Nhận ra vấn đề → Tìm giải pháp → So sánh lựa chọn → Ra quyết định mua → Sử dụng → Mua lại/Giới thiệu. Mỗi giai đoạn trả lời 3 câu: khách đang nghĩ/cảm thấy gì? · DN cần đưa nội dung/hành động gì? · qua kênh nào?
- **Cách giảng:** Journey chính là "bản thiết kế" của toàn bộ hệ thống 28 ngày: tuần 2 (content) phục vụ giai đoạn 1-3, tuần 3 (chatbot + sale) phục vụ giai đoạn 4-5, tuần 4 (follow-up + CSKH) phục vụ giai đoạn 6-7. Vẽ journey hôm nay = vẽ sơ đồ nhà trước khi xây.

> **Thích ứng ngành khác:** Nha khoa — Fear số 1 là "sợ đau/sợ hỏng răng thật", journey thường thêm bước "đến khám tư vấn miễn phí". Giáo dục — người mua (phụ huynh) khác người dùng (con), phải làm 2 avatar liên kết. Gym/Coaching — Pain gắn với "đã từng thử và bỏ cuộc", Objection số 1 là "không có thời gian". Khung 4 lớp tâm lý + 7 giai đoạn giữ nguyên.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 01 | Chiếu 2-3 bài tiêu biểu: 1 bài tốt (chỉ ra vì sao — nhiều số thật), 1-2 bài lỗi điển hình (Snapshot viết như bài PR, ICE toàn 14-15). Nhắc học viên 🔧 sửa trong 24h. |
| 25' | Giảng kiến thức trọng tâm | 4 khối ở mục 2. Dành nhiều thời gian nhất cho Khối 2 (bộ tứ tâm lý). |
| 30' | Demo thực hành live | Xây avatar chị Mai + PDFO Map + Journey Map cho Sen Spa (kịch bản mục 4). |
| 15' | Học viên làm tại chỗ + Q&A | Học viên chạy Prompt 1 với Business Snapshot của mình, đọc avatar AI tạo ra và gõ vào chat: "1 điểm AI đoán đúng + 1 điểm AI đoán sai về khách của tôi". |
| 10' | Giao bài tập | Chiếu deliverable + rubric. Nhấn mạnh quy tắc "ngôn ngữ khách hàng trong ngoặc kép". |

**Checklist chuẩn bị của trainer:** slide 2 output AI đối chứng (Khối 1) · slide 5 mức nhận thức · bảng journey trống 7 cột để điền live · 4 prompt chạy thử trước với Sen Spa, lưu output dự phòng · link Template 2.1-2.4 ghim sẵn.

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (8') — Tạo Customer Avatar nháp từ Business Snapshot.**
- Làm gì: Paste Prompt 1 (mục 8) kèm Business Snapshot Sen Spa (Ngày 01). AI tạo chân dung "chị Mai".
- Kết quả trông như thế nào: hồ sơ 8 trường — Tên gọi: chị Mai · Tuổi: 36 · Nghề: trưởng phòng hành chính · Thu nhập: ~25tr/tháng · Gia đình: chồng + 2 con nhỏ · Bối cảnh: nám gò má 3 năm, nặng hơn sau sinh bé thứ 2; từng dùng kem trộn bị dị ứng; lướt Facebook 21h-23h sau khi con ngủ · Nơi tìm thông tin: hội nhóm làm đẹp, review bạn bè · Khả năng chi: sẵn sàng 15tr NẾU tin là hiệu quả.
- Điểm nhấn: "AI tạo bản NHÁP tốt trong 2 phút — nhưng nó đoán. Bước tiếp theo mới là bước ăn tiền: đối chiếu với khách thật."

**Bước 2 (5') — Kiểm chứng bằng dữ liệu thật (bước học viên hay bỏ qua nhất).**
- Làm gì: Mở hộp thư fanpage Sen Spa (mô phỏng bằng 5 đoạn inbox mẫu chuẩn bị sẵn), đối chiếu: khách thật nhắn "cho em hỏi trị nám bên mình bao nhiêu tiền ạ, em bôi bao nhiêu thứ rồi không hết". Sửa avatar theo ngôn ngữ thật.
- Kết quả: avatar chị Mai phiên bản 2 — có 3 câu trích nguyên văn từ inbox thật.
- Điểm nhấn: "Quy tắc 3 nguồn: AI đoán + inbox/comment thật + trí nhớ của bạn về 5 khách gần nhất. Thiếu nguồn thật, avatar chỉ là tiểu thuyết."

**Bước 3 (8') — Đào bộ tứ Pain–Desire–Fear–Objection.**
- Làm gì: Paste Prompt 2. AI xuất bảng 4 cột, mỗi cột 7-8 mục, kèm câu nói mẫu.
- Kết quả (đọc to vài dòng): Pain — "họp online toàn phải bật filter, gặp trực tiếp thì ngại"; Desire — "đi họp lớp cấp 3 không cần trang điểm dày"; Fear — "sợ lại mất chục triệu mà đâu vẫn hoàn đấy như lần kem trộn"; Objection — "để em về bàn với chồng", "nhà em xa quá không biết có theo được 10 buổi không".
- Điểm nhấn: khoanh cặp Fear↔Objection tương ứng — "để em hỏi chồng" thực chất là "sợ quyết định sai một mình". Tuần 3 kịch bản sale sẽ xử lý theo cặp này.

**Bước 4 (7') — Vẽ Customer Journey Map 7 giai đoạn.**
- Làm gì: Paste Prompt 3. AI điền bảng 7 hàng × 4 cột (Giai đoạn | Khách nghĩ gì | DN cần làm gì | Kênh).
- Kết quả mẫu (giai đoạn 3 — Tìm giải pháp): Khách nghĩ: "laser, thuốc uống, spa — cái nào hợp mình, cái nào lừa đảo?" · DN cần: bài so sánh trung thực các phương pháp + video khách thật kể trải nghiệm · Kênh: Facebook + Google.
- Điểm nhấn: chỉ vào cột "DN cần làm gì" và nói: "Đây chính là đề bài content tuần 2. Hôm nay vẽ journey = tuần sau không phải nghĩ 'hôm nay đăng gì'."

**Bước 5 (2') — Đóng gói.**
- Làm gì: Dán 3 kết quả vào Template 2.1-2.3, đặt tên file `Sen Spa — Ngày 02 — Customer Avatar & Journey`.
- Điểm nhấn: nhắc lại Bonus (bộ 30 câu hỏi — Prompt 4) dành cho ai muốn khảo sát khách thật trong tuần.

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core ≤ 2h)

**Cụm A — Avatar nháp bằng AI (25'):**
- [ ] Chạy Prompt 1 với Business Snapshot của bạn (Ngày 01) (10')
- [ ] Đọc kỹ, sửa những gì AI đoán sai so với khách thật của bạn (15')

**Cụm B — Kiểm chứng bằng dữ liệu thật (25'):**
- [ ] Mở inbox/comment/Zalo, đọc lại 10 hội thoại khách gần nhất (15')
- [ ] Chép nguyên văn ≥5 câu khách nói (đau, hỏi giá, từ chối) vào mục "Câu nói vàng" (10')

**Cụm C — Pain–Desire–Fear–Objection Map (30'):**
- [ ] Chạy Prompt 2 (đầu vào: avatar đã sửa + 5 câu nói vàng) (10')
- [ ] Rà từng mục: gạch mục không đúng khách của bạn, mỗi nhóm giữ ≥5 mục đúng (15')
- [ ] Nối ≥3 cặp Fear ↔ Objection tương ứng (5')

**Cụm D — Customer Journey Map (25'):**
- [ ] Chạy Prompt 3, nhận bảng 7 giai đoạn (10')
- [ ] Sửa cột "Kênh" theo kênh bạn THẬT SỰ có (đừng giữ kênh bạn không dùng) (10')
- [ ] Đánh dấu ⚡ 2 giai đoạn DN bạn đang bỏ trống hoàn toàn (5')

**Cụm E — Nộp bài (15'):**
- [ ] Gộp vào 1 file theo Template, đặt tên đúng quy ước, nộp thread cohort trước 23h59

**Bonus:** chạy Prompt 4 tạo bộ 30 câu hỏi nghiên cứu; gửi 3 câu đầu cho 2 khách cũ thân thiết ngay tối nay; làm avatar phụ thứ 2 nếu có tệp khách thứ hai rõ rệt.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Xây cho doanh nghiệp của bạn: (1) Customer Avatar Profile 1 chân dung chính đủ 8 trường + ≥3 câu nói nguyên văn của khách thật, (2) Pain–Desire–Fear–Objection Map mỗi nhóm ≥5 mục viết bằng ngôn ngữ khách hàng + ≥3 cặp Fear↔Objection được nối, (3) Customer Journey Map đủ 7 giai đoạn × 3 cột (khách nghĩ gì / DN cần làm gì / kênh) + đánh dấu 2 giai đoạn đang bỏ trống.

**Deliverable nộp (1 file, 3 phần):**
- `[Tên DN] — Ngày 02 — Customer Avatar & Journey`
- Ví dụ: `Sen Spa — Ngày 02 — Customer Avatar & Journey`

**Deadline:** 23h59 cùng ngày, nộp link vào thread cohort ngày 02.

## 7. 📄 Template Đi Kèm

**Template 2.1 — Customer Avatar Profile.** Các trường: Tên gọi đại diện | Tuổi | Nghề nghiệp & vai trò (trong gia đình/công ty) | Thu nhập | Bối cảnh sống (2-3 câu: tình trạng vấn đề, đã thử gì, thất bại gì) | Hành vi online (dùng kênh nào, giờ nào, tin ai) | Khả năng chi & điều kiện xuống tiền | Câu nói vàng (≥3 câu nguyên văn). *Kèm bản chị Mai điền mẫu đầy đủ.*

**Template 2.2 — Pain–Desire–Fear–Objection Map.** Bảng 4 cột × ≥5 hàng; mỗi ô = 1 câu ngôn ngữ khách hàng trong ngoặc kép + 1 dòng diễn giải. Cuối bảng: mục "Cặp Fear↔Objection" (≥3 cặp, dạng: Objection nói ra ← Fear ẩn sau).

**Template 2.3 — Customer Journey Map.** Bảng 7 hàng (7 giai đoạn) × 4 cột: Giai đoạn | Khách nghĩ/cảm thấy gì | DN cần đưa nội dung/hành động gì | Kênh chạm. Hàng nào DN đang bỏ trống đánh dấu ⚡. *Kèm bản Sen Spa điền mẫu.*

**Template 2.4 (Bonus) — Bộ câu hỏi nghiên cứu khách hàng.** 3 khối × 10 câu: phỏng vấn khách cũ (tập trung "vì sao anh/chị chọn mình") · khảo sát khách tiềm năng (tập trung pain + rào cản) · câu hỏi cho đội sale khai thác nhu cầu (dạng mở, theo trình tự SPIN — Situation, Problem, Implication, Need-payoff: bối cảnh, vấn đề, hệ quả, nhu cầu).

### Trích bản điền mẫu Template 2.2 — Sen Spa (mỗi nhóm 3/5+ dòng)

| Pain (nỗi đau) | Desire (mong muốn) | Fear (nỗi sợ) | Objection (phản đối nói ra) |
|---|---|---|---|
| "Họp online toàn phải bật filter, gặp trực tiếp thì ngại lắm" | "Chỉ mong ra đường không cần đánh nền dày" | "Sợ mất thêm chục triệu nữa mà nám vẫn hoàn nám" | "Để em về bàn với chồng đã" |
| "Bôi đủ thứ kem 3 năm nay, tốn cả đống tiền mà càng đậm" | "Đi họp lớp tự tin, ai cũng khen trẻ ra" | "Sợ spa dụ ký gói to rồi bỏ bê mình" | "15 triệu hơi quá tay với em" |
| "Chồng em bảo sao mặt em dạo này xỉn thế" | "Muốn kết quả nhìn thấy được sau 1-2 tháng" | "Sợ máy móc trôi nổi làm hỏng da nặng hơn" | "Nhà em xa, sợ không theo nổi 10 buổi" |

**Cặp nối mẫu:** "Để em về bàn với chồng" ← sợ quyết định sai một mình sau lần mất tiền kem trộn · "15 triệu hơi quá tay" ← sợ mất tiền vô ích lần nữa (không phải không có tiền — chị Mai thu nhập 25tr).

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Tạo Customer Avatar nháp từ Business Snapshot

```
[VAI TRÒ] Bạn là chuyên gia nghiên cứu khách hàng cho SME ngành dịch vụ bán qua tư vấn tại Việt Nam, giỏi biến dữ liệu kinh doanh thành chân dung khách hàng sống động.

[BỐI CẢNH] Tôi cần một Customer Avatar (chân dung khách hàng) chi tiết để làm nền cho toàn bộ content, chatbot và kịch bản bán hàng. Đây là bản NHÁP — tôi sẽ kiểm chứng lại bằng dữ liệu khách thật.

[NHIỆM VỤ] Từ Business Snapshot dưới đây, xây 1 chân dung khách hàng LÝ TƯỞNG NHẤT (người dễ mua nhất, giá trị cao nhất) theo đúng 8 trường: (1) tên gọi đại diện; (2) tuổi; (3) nghề nghiệp & vai trò trong gia đình/công ty; (4) thu nhập; (5) bối cảnh sống — tình trạng vấn đề hiện tại, đã thử giải pháp gì, thất bại ra sao; (6) hành vi online — kênh, khung giờ, tin ai; (7) khả năng chi & điều kiện để xuống tiền; (8) 5 câu nói mà người này có thể nhắn cho doanh nghiệp (văn nói tự nhiên, có thể sai chính tả nhẹ như tin nhắn thật). Cuối cùng, xếp người này vào 1 trong 5 mức nhận thức (Unaware → Most Aware) và giải thích 1 câu.

[DỮ LIỆU ĐẦU VÀO] Business Snapshot: {{dán Business Snapshot Ngày 01}}. Mô tả nhanh 2-3 khách gần nhất đã mua gói lớn: {{2-3 câu, VD: khách A 34 tuổi kế toán mua liệu trình nám, khách B 41 tuổi bán hàng online mua trẻ hóa}}.

[ĐỊNH DẠNG ĐẦU RA] Hồ sơ 8 đề mục in đậm; mục 8 để dạng danh sách 5 câu trong ngoặc kép; kết bằng dòng "Mức nhận thức: X — vì...".

[RÀNG BUỘC] Viết cụ thể như tả một người có thật, không dùng từ chung chung ("có nhu cầu làm đẹp", "quan tâm chất lượng"). Thu nhập và khả năng chi phải khớp logic với mức giá trong Snapshot. Tiếng Việt, ≤400 từ.
```

**Ví dụ đã điền (Sen Spa):** `{{2-3 khách gần nhất}}` → "Khách gần nhất: chị 36 tuổi trưởng phòng hành chính mua liệu trình nám 15tr sau 2 lần đến soi da; chị 33 tuổi bán mỹ phẩm online mua gói mụn 12tr, hỏi rất kỹ về máy móc; chị 42 tuổi nội trợ chồng làm xây dựng, mua trẻ hóa, được bạn thân giới thiệu."

### Prompt 2 — Đào Pain–Desire–Fear–Objection Map

```
[VAI TRÒ] Bạn là chuyên gia tâm lý người mua (buyer psychology) ngành dịch vụ chăm sóc cá nhân tại Việt Nam.

[BỐI CẢNH] Tôi đã có Customer Avatar được kiểm chứng một phần bằng tin nhắn khách thật. Tôi cần bản đồ 4 lớp tâm lý để viết content (dùng Pain), viết offer (dùng Desire), viết bảo chứng (dùng Fear) và viết kịch bản xử lý từ chối (dùng Objection).

[NHIỆM VỤ] Từ avatar và các câu nói thật dưới đây, lập bảng 4 nhóm, mỗi nhóm 7 mục: (1) Pain — nỗi đau đang diễn ra hằng ngày (mất tiền, mất thời gian, xấu hổ, bất tiện); (2) Desire — kết quả muốn đạt VÀ hình ảnh bản thân muốn trở thành trong mắt người khác; (3) Fear — nỗi sợ ngầm khiến trì hoãn (sợ mất tiền vô ích, sợ bị lừa, sợ đau, sợ bị phán xét); (4) Objection — câu từ chối cụ thể nói ra miệng. Mỗi mục gồm: 1 câu ngôn ngữ khách hàng trong ngoặc kép + 1 dòng diễn giải cho người viết content. Sau bảng, nối 4 cặp Objection ↔ Fear ẩn sau nó.

[DỮ LIỆU ĐẦU VÀO] Customer Avatar: {{dán avatar đã sửa}}. Câu nói nguyên văn của khách thật: {{dán ≥5 câu chép từ inbox/comment/Zalo}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng markdown 4 cột × 7 hàng. Sau bảng: mục "Cặp Objection ↔ Fear" 4 dòng, định dạng: "[câu từ chối]" ← [nỗi sợ thật] → gợi ý 1 hướng xử lý.

[RÀNG BUỘC] Ưu tiên tuyệt đối các câu nói thật tôi cung cấp — phát triển từ đó thay vì sáng tác mới hoàn toàn. Không viết mục nào bằng văn marketing ("trải nghiệm đẳng cấp"). Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{≥5 câu thật}}` → "1) 'cho em hỏi trị nám bên mình bao nhiêu tiền ạ, em bôi bao nhiêu thứ rồi không hết' · 2) 'bên em có cam kết gì k chị, em sợ mất tiền lắm rồi' · 3) 'để em xem lịch đã, dạo này em bận lắm' · 4) 'giá đó là trọn gói chưa chị hay còn phát sinh' · 5) 'em ở Long Biên hơi xa, không biết có theo được không'."

### Prompt 3 — Vẽ Customer Journey Map 7 giai đoạn

```
[VAI TRÒ] Bạn là chuyên gia thiết kế hành trình khách hàng (customer journey) cho SME dịch vụ bán qua tư vấn.

[BỐI CẢNH] Tôi cần bản đồ hành trình để biết đặt nội dung gì, ở kênh nào, tại thời điểm nào — đây sẽ là khung cho hệ thống content (tuần 2), chatbot + kịch bản sale (tuần 3) và follow-up + chăm sóc (tuần 4) của tôi.

[NHIỆM VỤ] Từ avatar, bản đồ tâm lý và quy trình hiện tại dưới đây, lập Customer Journey Map đúng 7 giai đoạn: (1) Chưa biết vấn đề; (2) Nhận ra vấn đề; (3) Tìm giải pháp; (4) So sánh lựa chọn; (5) Ra quyết định mua; (6) Sử dụng sản phẩm/dịch vụ; (7) Mua lại hoặc giới thiệu. Mỗi giai đoạn điền 4 cột: Khách đang nghĩ/cảm thấy gì (1-2 câu, giọng khách hàng) | Nội dung/hành động DN cần đưa ra (cụ thể: dạng bài viết/video/tin nhắn/cuộc gọi nào) | Kênh chạm | Hiện tại DN đã làm gì ở bước này (đối chiếu Process Map — ghi "BỎ TRỐNG" nếu chưa có gì).

[DỮ LIỆU ĐẦU VÀO] Customer Avatar: {{dán}}. Pain–Desire–Fear–Objection Map: {{dán}}. Business Process Map hiện tại (Ngày 01): {{dán}}.

[ĐỊNH DẠNG ĐẦU RA] Bảng markdown 7 hàng × 5 cột (thêm cột Giai đoạn). Sau bảng: "⚡ 2 giai đoạn cần vá gấp nhất" + lý do 1 câu mỗi giai đoạn.

[RÀNG BUỘC] Cột "Nội dung/hành động" phải đủ cụ thể để tuần sau viết được ngay (VD: "bài so sánh laser vs thuốc vs spa, giọng trung thực" — không viết "cung cấp nội dung giá trị"). Cột Kênh chỉ dùng kênh DN đang có hoặc sẽ xây trong 28 ngày. Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** output giai đoạn 5 (Ra quyết định mua) — Khách nghĩ: "15 triệu... làm thì muốn làm mà sợ phí tiền, hay để tháng sau" · DN cần: kịch bản tư vấn xử lý cặp "hỏi chồng ← sợ quyết sai" + cam kết theo lộ trình rõ ràng + ưu đãi có hạn chót thật · Kênh: tư vấn trực tiếp tại spa + Zalo · Hiện tại: chỉ mình Hương xử lý theo bản năng — chưa có kịch bản → ⚡ vá gấp.

### Prompt 4 (Bonus) — Bộ 30 câu hỏi nghiên cứu khách hàng

```
[VAI TRÒ] Bạn là chuyên gia nghiên cứu thị trường định tính, chuyên thiết kế câu hỏi phỏng vấn không dẫn dắt (non-leading) cho SME Việt Nam.

[BỐI CẢNH] Tôi muốn kiểm chứng Customer Avatar bằng dữ liệu thật sau chương trình. Tôi cần 3 bộ câu hỏi cho 3 tình huống: gọi điện/gặp khách cũ, khảo sát khách tiềm năng qua form/tin nhắn, và cho nhân viên tư vấn dùng khi khai thác nhu cầu.

[NHIỆM VỤ] Tạo đúng 30 câu: (A) 10 câu phỏng vấn khách cũ — đào "hành trình trước khi mua": lúc quyết định mua điều gì thuyết phục nhất, suýt từ chối vì gì, so sánh với ai; (B) 10 câu khảo sát khách tiềm năng — đào pain và rào cản, KHÔNG nhắc đến sản phẩm của tôi; (C) 10 câu cho tư vấn viên theo trình tự SPIN (Situation - Problem - Implication - Need-payoff: bối cảnh → vấn đề → hệ quả → nhu cầu), sắp đúng thứ tự dùng trong buổi tư vấn.

[DỮ LIỆU ĐẦU VÀO] Customer Avatar: {{dán}}. Sản phẩm chủ lực: {{tên + giá}}.

[ĐỊNH DẠNG ĐẦU RA] 3 khối A/B/C, mỗi khối 10 câu đánh số; khối C ghi chú nhãn S/P/I/N ở đầu mỗi câu.

[RÀNG BUỘC] Câu hỏi mở (không trả lời được bằng có/không), không dẫn dắt ("Chị thấy dịch vụ mình tuyệt vời chứ?" = cấm), văn nói tự nhiên đúng xưng hô ngành dịch vụ Việt Nam. Mỗi câu ≤25 từ.
```

**Ví dụ đã điền (Sen Spa):** khối A câu mẫu — "Trước khi đến Sen Spa, chị đã thử những cách nào để xử lý nám rồi ạ?"; "Điều gì khiến chị quyết định ký liệu trình 10 buổi thay vì làm thử 1-2 buổi?"; khối C câu S — "Chị mô tả giúp em tình trạng da hiện tại và nó bắt đầu từ khi nào ạ?"

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-02: Cập nhật Customer Avatar hàng tháng bằng dữ liệu thật**
- **Khi nào:** Ngày cuối mỗi tháng (30').
- **Ai làm:** Chủ DN hoặc nhân viên tư vấn chính.
- **Input:** 20 hội thoại inbox/Zalo gần nhất + ghi chú của tư vấn viên về các ca chốt/trượt trong tháng.
- **Các bước:** (1) Chép 5-10 câu nói mới đáng chú ý của khách vào mục "Câu nói vàng"; (2) Đối chiếu với PDFO Map — có pain/objection MỚI nào chưa có trong bảng không; (3) Nếu có, thêm vào bảng và chuyển cho AI Business Brain (cập nhật Knowledge Base — quy trình Ngày 04); (4) Ghi 1 dòng nhật ký: "Tháng này khách thay đổi gì".
- **Output:** PDFO Map phiên bản mới + Knowledge Base được cập nhật.
- **Tần suất:** 12 lần/năm. Đây là lý do avatar của bạn ngày càng sắc còn đối thủ vẫn đoán mò.

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Avatar đủ 8 trường (10đ) · PDFO Map đủ 4 nhóm × ≥5 mục/nhóm (10đ) · Journey đủ 7 giai đoạn × 3 cột trở lên (10đ) |
| Chất lượng & độ sâu | 30 | ≥3 câu nói nguyên văn của khách THẬT trong ngoặc kép (10đ) · ≥3 cặp Fear↔Objection được nối và hợp logic (10đ) · cột "DN cần làm gì" của Journey đủ cụ thể để viết content ngay — kiểm tra: chọn ngẫu nhiên 2 ô, mỗi ô phải nêu được dạng bài/tin nhắn cụ thể (10đ) |
| Cá nhân hoá vào DN thật | 25 | Avatar khớp logic với giá & dữ liệu Snapshot Ngày 01 (thu nhập ↔ khả năng chi ↔ mức giá) (10đ) · ngôn ngữ khách mang dấu vết ngành/vùng miền thật, không phải văn mẫu AI (10đ) · có đánh dấu ⚡ 2 giai đoạn đang bỏ trống đúng với thực trạng DN (5đ) |
| Dùng được ngay | 15 | 1 file 3 phần đúng template, đặt tên đúng quy ước (7đ) · người ngoài đọc avatar 2 phút có thể mô tả lại khách hàng này là ai (mentor kiểm tra bằng cách đọc lướt) (8đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Avatar là "mọi người": khoảng tuổi rộng 25-50, nghề "đa dạng" — không phải MỘT con người: −10.
2. PDFO viết bằng ngôn ngữ chủ DN/marketing ("khách hàng có nhu cầu cải thiện sắc tố") thay vì ngôn ngữ khách: −8.
3. Không có câu nói thật nào — toàn bộ do AI sáng tác: −10.
4. Journey cột "Kênh" liệt kê kênh DN không hề có (TikTok, email) mà không có kế hoạch xây: −5.
5. Fear và Objection trùng nhau hoàn toàn (copy cột này sang cột kia): −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: DN tôi có nhiều tệp khách (khách lẻ + khách doanh nghiệp), làm avatar nào trước?**
→ Làm avatar cho tệp sinh ra nhiều doanh thu nhất hoặc tệp bạn muốn tăng trưởng trong 28 ngày (khớp Mục tiêu Ngày 01). Tệp thứ 2 là Bonus, đừng làm 2 cái làng nhàng thay vì 1 cái sắc.

**Q2: Tôi mới mở, chưa có nhiều khách thật để chép "câu nói vàng"?**
→ Ba nguồn thay thế: (1) comment/inbox trên fanpage đối thủ cùng ngách, (2) hội nhóm Facebook nơi khách mục tiêu tụ tập (đọc các bài hỏi xin review), (3) 2-3 người quen đúng chân dung — nhắn hỏi trực tiếp bằng câu hỏi khối B của Prompt 4.

**Q3: Avatar AI tạo ra nghe rất hợp lý — tôi cứ dùng luôn được không?**
→ Không. "Nghe hợp lý" là bẫy nguy hiểm nhất của AI. Bắt buộc bước kiểm chứng (Cụm B checklist): 10 hội thoại thật. Nếu 7/10 hội thoại khớp avatar → dùng; nếu không → sửa avatar theo hội thoại, không sửa hội thoại theo avatar.

**Q4: Journey 7 giai đoạn có quá dài với dịch vụ giá thấp không?**
→ Với buổi lẻ 1.5tr, giai đoạn 3-4 (tìm giải pháp, so sánh) diễn ra nhanh — vài ngày. Nhưng với liệu trình 15tr thì đủ 7 bước và kéo dài hàng tuần. Vẽ journey theo SẢN PHẨM GIÁ TRỊ CAO NHẤT — vì đó là thứ cần hệ thống nhất.

**Q5: Người mua và người dùng khác nhau (mẹ mua cho con gái, chồng trả tiền cho vợ) thì avatar là ai?**
→ Avatar chính = người RA QUYẾT ĐỊNH chi tiền. Người dùng ghi thành 1 trường phụ trong bối cảnh. Ngành giáo dục: avatar = phụ huynh, con = người dùng; objection của phụ huynh ("sợ con không theo được") khác hẳn của con.

**Q6: Có cần khảo sát khách thật xong mới nộp bài không?**
→ Không — khảo sát thật là việc của cả tuần (Bonus). Hôm nay nộp avatar bản "AI + inbox cũ + trí nhớ". Dữ liệu khảo sát về sau cập nhật theo SOP-02.

**Lỗi thường gặp:**
1. **Avatar quá hoàn hảo, không có mâu thuẫn** — khách thật luôn mâu thuẫn (muốn kết quả nhanh nhưng ngại đến đều; kêu đắt nhưng vừa mua iPhone). *Phát hiện:* đọc avatar không thấy điểm nào "khó chiều". *Sửa:* thêm trường "mâu thuẫn nội tâm" — hỏi AI: "người này có mâu thuẫn gì giữa mong muốn và hành vi?"
2. **Nhầm Pain với Fear** — Pain là đau ĐANG diễn ra ("da xỉn phải bật filter"), Fear là sợ điều CHƯA xảy ra ("sợ mất tiền vô ích"). *Phát hiện:* cột Pain có chữ "sợ". *Sửa:* câu nào có "sợ/lo/ngại" chuyển sang Fear, Pain chỉ giữ hiện trạng.
3. **Journey viết theo góc nhìn DN thay vì khách** — cột "khách nghĩ gì" ghi "khách được tư vấn nhiệt tình". *Phát hiện:* câu không thể đọc lên bằng giọng khách hàng. *Sửa:* ép mọi ô cột 2 bắt đầu bằng suy nghĩ ngôi thứ nhất: "Mình...", "Không biết có...".

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 01 — Phân Tích Doanh Nghiệp & Cơ Hội AI]] · Ngày sau: [[Ngày 03 — Offer, Định Vị & Thông Điệp Bán Hàng]]
- Tài sản hôm nay được dùng lại ở:
	- **Customer Avatar + PDFO Map** → đầu vào trực tiếp của Offer & thông điệp (Ngày 03 — Desire viết Big Promise, Fear viết Guarantee, Objection viết Risk Reversal), tài liệu `03. Customer Avatar` trong Knowledge Base (Ngày 04), dữ liệu huấn luyện chatbot tư vấn (Tuần 3).
	- **Câu nói vàng** → hook content (Tuần 2), câu mở kịch bản sale (Tuần 3).
	- **Customer Journey Map** → khung lịch content theo mức nhận thức (Tuần 2), điểm đặt chatbot ở giai đoạn 4-5 (Tuần 3), chuỗi follow-up + chăm sóc giai đoạn 6-7 (Tuần 4).
	- **Bộ 30 câu hỏi** → nhân viên sale dùng ngay (Tuần 3 sẽ đóng vào kịch bản tư vấn chuẩn).
