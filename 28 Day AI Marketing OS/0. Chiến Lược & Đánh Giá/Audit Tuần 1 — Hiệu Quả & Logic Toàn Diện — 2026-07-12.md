---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-12
tags: [project, aios, audit]
---

# 🔬 Audit Tuần 1 — Hiệu Quả & Logic Toàn Diện — 2026-07-12

> Audit sâu toàn bộ Tuần 1: 7 giáo án + 6 bài tập + INDEX + checklist + case study + kế hoạch video + đối chiếu vault (`ai-marketing-system/` và `ai-marketing-system-msx-demo/`). Mỗi ngày được phân tích độc lập rồi đối chiếu chéo toàn chuỗi. Kế thừa [[Audit 28 Day AIOS — Logic & Khả Năng x10 — 2026-07-11]].

---

## 1. KẾT LUẬN TỔNG — BỨC TRANH LỚN

> **Giáo án Tuần 1 (7 file bài giảng) là bộ tài liệu chất lượng cao, chuỗi logic chặt. Nhưng Tuần 1 XÉT NHƯ MỘT HỆ THỐNG thì chưa chạy được — vì đang tồn tại 2 thế hệ giáo trình song song mâu thuẫn nhau, và ~30 tài sản được giáo án hứa nhưng chưa tồn tại.**

| Tầng | Trạng thái | Điểm |
|---|---|:---:|
| Giáo án 7 ngày (đứng riêng) | ✅ Rất tốt — chuỗi feed-forward chặt, rubric đo được, prompt chuẩn | 8.5/10 |
| Bài tập ↔ Giáo án | 🔴 Lệch thế hệ toàn diện — 6/6 ngày không khớp | 2.5/10 |
| Case study (Sen Spa vs MSX/RocketAI) | 🔴 Chưa chốt — giáo án một đằng, chiến lược một nẻo | 3/10 |
| Tài sản bàn giao (template, baseline, video) | 🔴 Hứa nhiều, tồn tại ít | 2/10 |
| Khả thi thời gian cho chủ SME | 🟠 Cam kết ≤2h, thực tế 2.5–6h/ngày | 5/10 |

## 2. BẢNG ĐIỂM 7 NGÀY (từ phân tích độc lập từng ngày)

| Ngày | Logic nội bộ | Khả thi thời gian | Giá trị output | Khớp bài giảng–bài tập |
|:---:|:---:|:---:|:---:|:---:|
| 01 | 7 | 6 | 9 | — (không có file bài tập) |
| 02 | 7 | 6 | 9 | 3 |
| 03 | 5 | 4 | 9 | 2 |
| 04 | 6 | 4 | 9 | 3 |
| 05 | 7 | 6 | 9 | 2 |
| 06 | 6 | 5 | 9 | 3 |
| 07 | 5 | 5 | 9 | 2 |

> Giá trị output đồng loạt 9/10 — nội dung ĐÚNG thứ SME cần. Vấn đề không nằm ở "dạy gì" mà ở **đồng bộ hoá và đóng gói**.

---

## 3. BA ĐỨT GÃY HỆ THỐNG (phải vá trước cohort)

### 🔴 Đứt gãy #1 — Folder `Tuần 1 - Bài tập/` là THẾ HỆ CŨ, mâu thuẫn giáo án trên mọi thông số

Bộ bài tập (07-09, gốc từ folder `Tuần 1 — AIOS Business Foundation 1/` đã xoá) chưa được viết lại theo giáo án mới. Học viên làm theo bài tập sẽ **trượt rubric giáo án** và ngược lại:

| Thông số | Giáo án (chuẩn mới) | Bài tập (cũ) |
|---|---|---|
| Deadline | **23h59** (khớp [[Hệ Thống Chấm Chữa & Support Hàng Ngày]]) | 22:00 |
| Nơi nộp | Thread cohort, tên file `[Tên DN] — Ngày XX — ...` | File .md trong Vault / AI Grader |
| Prompt Library | 50 khung phát sẵn, cá nhân hoá 20, test 10 | Tự viết 30 từ số 0, test 3 |
| FAQ | ≥30 cặp (≥10 từ inbox thật) | ≥20 câu |
| Test Business Brain | 6 ca, chấm 3 mức + truy nguyên lỗi | 10 ca, chấm Đúng/Sai |
| AI Assistant | 2 (Sales + Marketing) — FAQ Q5 nói rõ 5 là thừa | Bắt buộc đủ 5 |
| Foundation Gate | 5 câu kiểm chứng độ KHỚP mô hình–khách–offer | 5 câu đếm tài sản (dễ hơn nhiều) |
| Chấm | Rubric 100đ/ngày, 4 mức | Checklist định tính / ≥35/50 |
| Cách làm | Pipeline prompt đóng sẵn (chuyển giao) | Điền tay, không dùng prompt nào của giáo án |

**Nguy hiểm nhất:** Bài Tập Ngày 3 đưa ví dụ mẫu ✅ "Giảm 2kg trong 14 ngày hoặc hoàn 100%", "Da sáng mịn sau 7 ngày — hoặc hoàn tiền", CTA "Còn 5 suất" — **chính là thứ giáo án CẤM và trừ điểm nặng nhất** (hứa kết quả y khoa tuyệt đối −15, khan hiếm giả −10). Học viên làm đúng mẫu bài tập = vi phạm compliance (tuân thủ quy định) ngành sức khoẻ.

**Lỗi lẻ trong bộ bài tập:** wikilink gãy (`[[Bài Tập Ngày 2 — Chân Dung Khách Hàng]]`, `[[Bài Tập Ngày 2 — Chân Dung KH]]` — sai tên file thật) · ký tự Trung Quốc sót "完整的" trong Bài Tập Ngày 7 · ngưỡng "≥26/33 = 80%" sai toán (26/33 = 78,8%, phải là 27) · audit "Ngày 1" trong khi không tồn tại Bài Tập Ngày 1 · file trùng `Checklist Review BMC — Tuần 1 1.md` (2 bản lệch chuẩn: FAQ ≥10 vs ≥12, journey 5-7 vs 7 giai đoạn).

### 🔴 Đứt gãy #2 — Case study chưa chốt: giáo án dạy Sen Spa, chiến lược tuyên bố bỏ Sen Spa

- [[Case Study Kép — RocketAI + MSX Group]] (11/07) chốt: *"Bỏ hoàn toàn Sen Spa (case bịa). RocketAI để DẠY. MSX Group để BÁN."*
- Nhưng **toàn bộ 7/7 giáo án Tuần 1 (và cả 21 giáo án Tuần 2-4) vẫn dùng Sen Spa xuyên suốt** — demo, prompt mẫu, template mẫu, rubric.
- [[_Kế Hoạch Video Tuần 1 — Hướng Dẫn Học Viên]] vẫn yêu cầu *"build xong bản Sen Spa demo điền đầy TRƯỚC khi quay bất kỳ video nào"* — trong khi vault demo thực tế đã build là **MSX** (`ai-marketing-system-msx-demo/`).
- Bộ bài tập + INDEX + Checklist mới lại dùng RocketAI + MSX.

→ Ba nhóm tài liệu trỏ 3 hướng khác nhau. Học viên xem demo Sen Spa, đối chiếu bản mẫu MSX, đọc bài tập RocketAI — không biết "nhìn bài đúng" ở đâu.

### 🔴 Đứt gãy #3 — Tài sản được hứa nhưng CHƯA TỒN TẠI (tham chiếu treo)

| Tài sản giáo án hứa | Nơi hứa | Trạng thái |
|---|---|---|
| Template 1.0–1.4 (BMC, Snapshot, Process Map, Top 10, Mục tiêu) | Ngày 01 — "link ghim sẵn" | ❌ Không có file |
| Template 2.1–2.4 (Avatar, PDFO, Journey, Bộ câu hỏi) | Ngày 02 | ❌ Không có file |
| Template 3.1–3.4 (Offer, Value Prop, Message Pack, Landing) | Ngày 03 | ❌ Không có file |
| Template 4.1–4.3 (Cây KB + Security Rule, Product Knowledge, FAQ) | Ngày 04 | ❌ Không có file |
| Template 5.2–5.3 (Khối ngữ cảnh, Usage Guide) | Ngày 05 | ❌ (chỉ 5.1 + 5.1A tồn tại ✅) |
| Template 6.1–6.3, 7.1–7.3 | Ngày 06-07 | ⚠️ Chỉ nội tuyến trong giáo án |
| `Baseline & Mục Tiêu 28 Ngày.md` | Ngày 0/7/28 + Foundation Gate câu 5 | ❌ Không tồn tại trong vault nào |
| `Đánh Giá Mô Hình Kinh Doanh — [Tên DN].md` | Ngày 07 (ghi kết quả Gate) | ❌ Không tồn tại |
| Folder `04. Resources/Prompt Library/` | Ngày 05 | ❌ Không có trong cả 2 vault |
| Giáo án Ngày 0 (Install Pack) | Video plan + Bản Đồ Vault | ❌ Chưa có file giáo án |
| Bài Tập Ngày 1 | INDEX ("toàn bộ bài tập") | ❌ INDEX bỏ sót Ngày 1 |
| 19 video hướng dẫn | INDEX ghi "học viên nhận" | ❌ Chưa quay (kẹt dependency vault demo) |

---

## 4. LỖI LOGIC NỘI BỘ TỪNG GIÁO ÁN (sửa nhanh, dưới 1 buổi)

| Ngày | Lỗi | Mức |
|:---:|---|:---:|
| 01 | **BMC là Core Output #1 nhưng rubric chấm 0 điểm** (deliverable ghi "4 phần" trong khi đề bài 5 phần) — học viên bỏ BMC vẫn đạt 100đ | 🔴 |
| 01 | Toán rubric lệch (thiếu 1 phần −8 × 4 = 32 > quỹ 30đ) · giảng 30' nhưng agenda cấp 25' · "cả 4 template" nhưng liệt kê 5 | 🟡 |
| 02 | Journey lúc 3 cột, lúc 4 cột (Template 2.3), lúc 5 cột (Prompt 3) — không nói bảng nào là chuẩn cuối | 🟠 |
| 02 | 5 Levels of Awareness giảng 5' nhưng không nối vào deliverable/rubric | 🟡 |
| 03 | **"7 khối offer" định nghĩa 3 kiểu khác nhau** (mục tiêu 6 mục, Khối 2 một danh sách khác, Prompt 2 đòi "9 mục", rubric theo danh sách thứ ba) | 🔴 |
| 04 | **2 cây thư mục mâu thuẫn trong 1 file**: cây 10 folder Google Drive (mục 0.4) vs cấu trúc Vault SME (callout đầu) — không có mapping; mỉa mai vì bài dạy "một nguồn sự thật" | 🔴 |
| 04 | Mục 0.7 (chiến lược nội bộ RocketAI) lạc đối tượng trong giáo án; file trộn 3 đối tượng đọc (trainer / học viên / product team) | 🟠 |
| 05 | Khối Template 5.1A chen giữa câu dẫn "Danh mục 50 prompt:" và danh sách của nó (vết chỉnh sửa dở) · Bonus "10-20" vs "nốt 30" | 🟡 |
| 06 | **3 định nghĩa "Business Brain" không hoà giải**: (a) bot mới trên RocketAgent + KB + Instruction; (b) vault + CLAUDE.md + Claude Code, "KHÔNG dựng bot mới"; (c) "chính là Jarvis v1" test qua Telegram — học viên không biết theo đoạn nào, làm 1 hay cả 3 track | 🔴 |
| 07 | Scorecard 25 tiêu chí bỏ sót Data Access & Security Rule (Core N4) + Value Proposition Statement (Core N3); chỉ nghiệm thu 1/2 Assistant | 🟠 |
| 07 | 60' cho 8 demo × 7' = 56' — không còn biên độ chuyển màn hình/phản biện; vỡ trận nếu cohort ≥10 người | 🟠 |

## 5. KHẢ THI THỜI GIAN — CAM KẾT vs THỰC TẾ

Blueprint quy định Core ≤2h/ngày. Mọi giáo án đều "cộng khớp trên giấy" nhưng **đúng 120' với 0 phút dự phòng**, và ước tính từng bước theo tốc độ người thạo công cụ:

| Ngày | Cam kết | Thực tế ước tính (SME không rành công nghệ) | Bước ngốn nhất |
|:---:|:---:|:---:|---|
| 01 | ≤2h | 3–4.5h | Prompt 0 phỏng vấn BMC 9 khối (12' → thực tế 40-60') |
| 02 | ≤2h | 2.5–3.5h | Lục 10 hội thoại inbox thật (25' → 45-60') |
| 03 | ≤2h | 2.5–3h (4.5h nếu theo bài tập) | Lọc 25-30 câu thông điệp theo "giọng mình" |
| 04 | ≤2h | 4–6h nếu làm đủ cả 2 file | Prompt 1 phỏng vấn từng dịch vụ × 9 trường |
| 05 | ≤2h | 3–4h | Cá nhân hoá 20 prompt (35') + test 10 prompt bằng dữ liệu thật (25') |
| 06 | ≤2h | 3–4h | Vòng test → truy nguyên → vá → chạy lại (kỹ năng debug mới) |
| 07 | 125' + 90' live | 4–6h cả ngày | Cụm E vá nợ tồn đọng cả tuần |

→ Với North-star **completion rate ≥70%**, đây là rủi ro lớn thứ hai sau đứt gãy #1. Giải pháp không phải cắt nội dung mà là: (a) sửa cam kết thành "2–3h", (b) video thao tác (đúng vai trò 19 video), (c) vault demo điền sẵn 80% đúng như [[Audit 28 Day AIOS — Logic & Khả Năng x10 — 2026-07-11]] đã chỉ.

## 6. ĐIỂM MẠNH — GIỮ NGUYÊN, KHÔNG ĐỤNG VÀO

1. **Chuỗi tài sản feed-forward chặt bậc nhất:** Ngày 7 truy xuất gần 100% đúng thông số từ Ngày 1-6 (50 prompt, 30 FAQ, 6 test, 7 khối, 8 trường, ICE…). Mỗi ngày ghi rõ tài sản được dùng lại ở đâu.
2. **Foundation Gate** — đo độ KHỚP mô hình–khách–offer thay vì đếm bài nộp; luật "fail câu 3 → sửa offer TRƯỚC khi viết content" là quyết định thiết kế đắt giá nhất tuần.
3. **Chống ảo giác AI có hệ thống** (quy tắc 3 nguồn, 7/10 hội thoại khớp, −10đ nếu toàn AI bịa) + **compliance ngành sức khoẻ** nhúng từ kiến thức → prompt → rubric.
4. **Nghiệm thu test-driven** (Ngày 6: 6 ca chuẩn, truy nguyên 2 loại lỗi, "nộp cả ảnh test thất bại — lỗi là dữ liệu quý").
5. **Prompt mẫu chuẩn 6 khối + ví dụ điền sẵn** cho mọi prompt; **SOP mỗi ngày** biến bài học thành nghi thức vận hành sau khoá (SOP-07 review 52 lần/năm).

## 7. KẾ HOẠCH VÁ — THEO THỨ TỰ ƯU TIÊN

### P0 — Trước khi tuyển sinh (ước 1-2 ngày tập trung, phần lớn AI làm được)

1. **Viết lại 6 file bài tập (Ngày 2-7) + tạo Bài Tập Ngày 1** — sinh trực tiếp từ mục 5 (Checklist) + 6 (Bài tập) + 10 (Rubric) của giáo án tương ứng. Xoá toàn bộ ví dụ vi phạm compliance ở Bài Tập Ngày 3. Thống nhất: deadline 23h59, nộp thread cohort, chuẩn số lượng theo giáo án.
2. **Chốt case study 1 lần cuối** — khuyến nghị: theo đúng quyết định 11/07 (RocketAI để dạy + MSX để chứng minh), vì vault demo MSX đã build; sửa Kế Hoạch Video (quay trên vault MSX thay vì "build Sen Spa trước") và cập nhật dần ví dụ trong giáo án. Nếu giữ Sen Spa làm case giảng thì phải sửa ngược [[Case Study Kép — RocketAI + MSX Group]] + INDEX — chọn 1, không để 2 hướng song song.
3. **Tạo tài sản bị treo:** `Baseline & Mục Tiêu 28 Ngày.md` + `Đánh Giá Mô Hình Kinh Doanh — [Mẫu].md` trong `00. Business Context/` vault gốc · folder `04. Resources/Prompt Library/` + nạp Template 5.1 · đóng file thật cho Template 1.0–1.4, 2.1–2.4, 3.1–3.4, 4.1–4.3, 5.2–5.3 (6.x, 7.x có thể giữ nội tuyến).
4. **Sửa lỗi nội bộ nhanh:** BMC vào rubric Ngày 1 (hoặc giảm còn 4 khối lõi) · chốt 1 định nghĩa "7 khối offer" Ngày 3 · chốt 1 bảng Journey chuẩn Ngày 2 · mapping 2 cây thư mục Ngày 4 (hoặc bỏ hẳn cây Google Drive, dồn về Vault SME) · hoà giải 3 định nghĩa Brain Ngày 6 thành 1 quyết định "bạn thuộc track nào" · archive `Checklist Review BMC — Tuần 1 1.md` vào `.trash/` · xoá ký tự "完整的", sửa ngưỡng 26→27/33.

### P1 — Trước khai giảng

5. **Giáo án Ngày 0 chính thức** (Install Pack — nội dung đã có sẵn trong Kế Hoạch Video V0.1-V0.6, chỉ cần đóng thành file giáo án).
6. **Sửa cam kết thời gian** "Core ≤2h" → "2–3h (nhanh hơn nếu dùng template điền sẵn)" + thêm hộp "Trước khi bắt đầu" Ngày 1 (tạo tài khoản AI, chia sẻ quyền Google Docs, khuyến cáo làm trên máy tính).
7. **Tách bản học viên** khỏi giáo án trainer (ít nhất Ngày 4 đang trộn 3 đối tượng đọc) — hoặc quy ước rõ "giáo án là tài liệu trainer, học viên chỉ nhận mục 5-8 + 11".
8. Quay 19 video theo kế hoạch (sau khi chốt case study ở mục 2).

## 8. SO VỚI AUDIT 11/07 — CÁI GÌ MỚI

Audit 11/07 đánh giá đúng cấu trúc vĩ mô (logic 4 tuần 8.5/10) và 5 việc x10 (vault demo, Ngày 0, bài tập T2-4, AI Grader, case KPI) — **tất cả vẫn còn nguyên giá trị**. Audit hôm nay bổ sung 3 phát hiện mà audit trước bỏ sót:

1. Nhận định *"Ngày 1-7 liên kết chặt: mỗi ngày dùng output ngày trước"* chỉ đúng cho **giáo án**; tầng **bài tập** đang lệch thế hệ toàn diện (đứt gãy #1) — nghiêm trọng hơn mọi gap từng ghi nhận vì nó phá trải nghiệm học viên ngay Tuần 1 đã "hoàn thiện".
2. Quyết định bỏ Sen Spa (chính audit 11/07 đề xuất) **chưa được lan truyền** vào 28 giáo án + kế hoạch video — tạo đứt gãy #2.
3. Danh sách tham chiếu treo cụ thể (mục 3.3) — audit trước nói "template chưa đóng gói" chung chung, nay đã có danh mục chính xác từng file để build.

---

## 🔗 Kết nối với

- [[Audit 28 Day AIOS — Logic & Khả Năng x10 — 2026-07-11]] · [[Đánh Giá Hiệu Quả Chương Trình — 2026-07-08]]
- [[_Blueprint Chuẩn — Cấu Trúc Giáo Án]] · [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]] · [[Case Study Kép — RocketAI + MSX Group]]
- [[_Kế Hoạch Video Tuần 1 — Hướng Dẫn Học Viên]] · [[Hệ Thống Chấm Chữa & Support Hàng Ngày]] · [[_MOC 28 Day AIOS]]
