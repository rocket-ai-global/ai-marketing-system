---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 2
day: 9
core-output: "Brand Voice Guideline (THI HÀNH giọng từ Brand Guideline T8.0 của Ngày 08 — chi tiết hoá cho từng loại bài, KHÔNG định nghĩa lại cá tính/giọng) + 10 bài viết duyệt kỹ (≥4 giáo dục · ≥3 phản đối · ≥2 bán mềm · ≥1 kể chuyện, ≥80% có mã nguồn, ≥3/10 bài từ câu nói nguyên văn khách) + Content Repurpose Sheet 3 bài (trong đó ≥2 bản Zalo broadcast dùng thật cho lịch Ngày 13)"
---

# Ngày 09 — AI Content Factory

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom (tuỳ chỉnh) → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Viết bài: agent đọc giọng từ `00. Business Context/Brand Voice` + chuyện thật từ `Nhật Ký CEO/`; mỗi bài 1 file `03. Areas/Brand & Content/Content Đã Đăng/YYYY-MM-DD — [Kênh] — [Tên].md` kèm frontmatter `content_pillar/format/hook/ma_nguon` (để Ngày 23 đo được). Vault demo của lớp: `ai-marketing-system-msx-demo/`.

> 📥 **Nguyên liệu Tuần 1 dùng hôm nay** — hôm nay KHÔNG tạo mới thứ đã có. Mọi thứ dưới đây bạn đã cầm trong tay từ Tuần 1:

| Tài sản Tuần 1 | Có từ | Hôm nay dùng để làm gì |
|---|:---:|---|
| **🎨 Brand Guideline (T8.0)** | **N8** | **Nguồn nhận diện đã chốt** — archetype + cá tính + 5 nguyên tắc giọng. Hôm nay **THI HÀNH**, không định nghĩa lại. Mọi bài phải đúng giọng T8.0 |
| **Brand Voice trong Knowledge Base** | N4 | Là **bản gốc** — đã được nâng cấp vào T8.0 (N8); hôm nay chi tiết hoá thành Guideline thi hành cho từng loại bài |
| **Khối `[GIỌNG]` (≤80 từ) trong Prompt Library** | N5 | **Input bắt buộc của Prompt 1.** AI đọc khối này rồi HỎI THÊM — không phỏng vấn lại từ đầu |
| **Sales Message Pack** (1 hook chủ đạo · 3 headline · 3 CTA · 5 angle · 10 câu ads, mỗi câu đã chú thích nguồn Pain/Desire/Fear) | N3 | **KHO ĐẠN.** Hook/headline/CTA của 10 bài hôm nay **lấy từ kho này TRƯỚC**, chỉ sáng tác mới khi kho không có |
| **FAQ & Objection Database (≥30 cặp)** | N4 | Nguồn cho **3 bài xử lý phản đối** (mã `Q##`) |
| **PDFO Map + 5 câu nguyên văn khách + Journey ⚡** | N2 | Nguồn **mã nguồn** `P#/D#/F#/O#/V#/J#` cho từng bài |
| **Core Offer 7 khối** | N3 | Nguồn `OF#` cho **2 bài bán mềm** |
| **10 ý tưởng ⭐** (từ 60 ý, đã có mã nguồn) | N8 | Chính là **10 bài viết hôm nay** — không nghĩ đề tài mới |
| **AI Marketing Assistant** (đã nạp KB) | N6 | **Nơi chạy mọi prompt hôm nay** (Track A) — không dán lại ICP/Offer vào từng prompt |

> Hôm nay doanh nghiệp của bạn có một **CỖ MÁY SẢN XUẤT BÀI VIẾT**: giọng thương hiệu đóng gói thành tài liệu chạy được + dây chuyền viết bài bằng AI có kiểm định + **kho 10 bài duyệt kỹ và 3 bài đã tái sử dụng** — vừa khít 2 tuần đầu của lịch đăng Ngày 13.

---

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên CÓ trong tay:

**Core Output (bắt buộc — điều kiện qua ngày):**

- ✅ **Brand Voice Guideline (tài liệu giọng văn thương hiệu) 1 trang, 5 phần** — **THI HÀNH** archetype + 5 nguyên tắc giọng đã chốt ở **Brand Guideline T8.0 (Ngày 08)**, chi tiết hoá thành cách viết cho từng loại bài (giáo dục / phản đối / bán mềm / kể chuyện). *KHÔNG định nghĩa lại cá tính/giọng — cái đó đã chốt ở T8.0. Ai mở Prompt 1 mà không dán T8.0 + khối `[GIỌNG]` vào là làm sai bài.*
- ✅ **10 bài viết hoàn chỉnh, duyệt kỹ từng bài** từ **10 ý ⭐ của Ngày 08**. Cơ cấu bắt buộc: **≥4 bài giáo dục/niềm tin · ≥3 bài xử lý phản đối · ≥2 bài bán hàng mềm · ≥1 bài kể chuyện cá nhân**. Mỗi bài đăng được NGAY.
- ✅ **Content Repurpose Sheet (bảng tái sử dụng nội dung) cho 3 bài tốt nhất** — mỗi bài → bản Zalo + script video 45s + email/tin chăm sóc + 3 quote làm visual. **Trong đó ≥2 bản Zalo broadcast là 2 slot THẬT trong lịch 14 ngày của Ngày 13.**

**Vì sao đúng 10 bài + 2 Zalo, không hơn không kém — phép cộng phải khớp:**

| Nguồn Core | Số lượng | Vào lịch Ngày 13 |
|---|:---:|---|
| Bài Facebook — **Ngày 09** | **10** | 5 bài/tuần × 2 tuần |
| Video ngắn — Ngày 11 | 2 | 1 video/tuần × 2 tuần |
| **Zalo broadcast — Ngày 09 (Repurpose Sheet)** | **2** | 1 broadcast/tuần × 2 tuần |
| | | **= 7 nội dung/tuần × 2 tuần = 14 slot** ✅ |

> **7 nội dung/tuần chính là mục tiêu Tuần 1 của MSX: content 3 → 7 bài/tuần.** Tuần 2 không phát minh chỉ tiêu mới — nó **thực hiện chỉ tiêu đã cam kết ở Tuần 1**. Bạn chỉ làm Core vẫn xếp đủ lịch, không cần một dòng Bonus nào.

**Bonus Output (nâng cao — không bao giờ là điều kiện của Core):**

- 🎁 **20 bài batch (chạy hàng loạt)** từ 20 ý tiếp theo trong bảng 60 ý tưởng (Ngày 08) → đủ kho 30 bài. Duyệt nhanh bằng checklist 5 câu.
- 🎁 Mở rộng Repurpose Sheet đủ 10 bài.

> **Nguyên tắc phân bổ (giữ nguyên, không được đảo):** **10 bài Core duyệt kỹ TRƯỚC — 20 bài batch SAU.** 10 bài Core = "hàng thủ công có kiểm định" — bạn học được kỹ năng duyệt AI. 20 bài Bonus = "hàng dây chuyền" — batch chỉ tốt khi **10 bài đầu đã dạy AI thế nào là ĐẠT**. Đảo ngược thứ tự = 30 bài dở đều nhau.

---

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — Dây chuyền sản xuất content bằng AI (4')

- **Ý chính:** Sản xuất hàng loạt ≠ bấm 1 prompt ra 30 bài. Dây chuyền **5 trạm**: `Ý tưởng ⭐ (N8) → Lấy đạn từ kho (Sales Message Pack N3) → Bản nháp AI (theo Brand Voice) → Duyệt & cá nhân hoá 30% → Đa kênh hoá (repurpose)`.
- **Analogy (phép so sánh):** Bếp của chuỗi nhà hàng — công thức chuẩn (Brand Voice + khung bài) + nguyên liệu tươi (chuyện thật, con số thật của bạn) + **đầu bếp nếm trước khi ra món** (bước duyệt). Bỏ bước nếm = ra "cơm công nghiệp" — chính là content AI bị chê máy móc.
- **Trạm số 2 là trạm hay bị bỏ nhất:** nhiều người mở AI ra và bảo "viết cho tôi 1 bài về mất ngủ". Sai. Bạn **đã có** 1 hook chủ đạo, 3 headline, 3 CTA, 5 angle, 10 câu ads từ Ngày 03 — mỗi câu đã chú thích nguồn Pain/Desire/Fear. **Mở kho ra dùng trước, đừng sáng tác lại.**

### Khối 2 — Brand Voice: NÂNG CẤP, không dựng lại (7')

- **Ý chính:** Bạn đã có giọng rồi. Ngày 04 bạn nạp Brand Voice vào Knowledge Base. Ngày 05 bạn nén nó thành khối `[GIỌNG]` ≤80 từ để dán vào mọi prompt. Hôm nay bạn **mở nó ra thành tài liệu 1 trang, 5 phần** — đủ chi tiết để một nhân sự content mới vào đọc là viết được.
- **5 phần của Brand Voice Guideline:**
	1. **Tính cách thương hiệu** — 3 từ + 1 câu giải thích mỗi từ.
	2. **Xưng hô** — mình xưng gì, gọi khách là gì.
	3. **5 điều LUÔN làm** khi viết.
	4. **5 điều KHÔNG BAO GIỜ làm** (gồm cả ranh giới pháp lý).
	5. **Từ ngữ đặc trưng / từ CẤM + 2 đoạn văn mẫu chuẩn giọng** (1 giáo dục, 1 bán mềm).
- **Ví dụ 🍵 MSX (bản có sẵn từ KB Ngày 04 → nâng cấp hôm nay):**
	- Tính cách: *mộc mạc – tử tế – có gốc gác*.
	- Xưng hô: **"em – anh/chị"**.
	- LUÔN: mở đầu bằng hình ảnh vùng cao (*"Sương sớm trên đỉnh Mẫu Sơn…"*) · nói rõ độ cao vùng nguyên liệu 800–1.541m · nhắc người Dao/Tày/Nùng hái thủ công · đưa con số thật (5.000+ khách, OCOP 3★) · hướng dẫn dùng cụ thể (1 túi 2,5g + 150–200ml nước sôi, uống buổi tối).
	- KHÔNG BAO GIỜ: *"thần dược"* · *"chữa khỏi"* · *"cam kết 100%"* · quá 3 emoji/bài · nói sản phẩm như thuốc.
	- Từ đặc trưng: *"dược liệu vùng cao Mẫu Sơn"* · *"thảo mộc tự nhiên"* · *"đồng hành cùng thói quen mỗi ngày"* · *"lối vào cuộc sống xanh"*.
- **Cách giảng (chiếu 2 đoạn cùng nội dung):**
	- AI mặc định: *"Mất ngủ là vấn đề phổ biến của người hiện đại. Trà thảo mộc là giải pháp tự nhiên giúp bạn ngủ ngon hơn…"* → nhạt, ai viết cũng được, **và sai tệp** (chị Hương đã Solution Aware — biết trà thảo mộc rồi, không cần dạy lại).
	- Có Brand Voice + đúng mức nhận thức: *"Sương sớm trên đỉnh Mẫu Sơn, 1.541m. Chị Hằng người Dao hái mẩy gòm lúc 6h — đúng lúc lá còn ngậm sương. Anh/chị hỏi em vì sao 359k một hộp trong khi ngoài siêu thị 50k? Câu trả lời nằm ở độ cao và ở đôi tay đó."*
- 🚀 **Đối chiếu B2B (RocketAI):** giọng B2B nghiêng **phản biện + chuyên môn**, không dùng hình ảnh cảm xúc. Hook chủ đạo của RocketAI: *"4 tiếng mỗi ngày ngồi nghĩ caption — ai đang điều hành spa thay chị?"* — thẳng, đánh vào chi phí cơ hội của chủ DN, không kể chuyện vùng cao.

### Khối 3 — Khung bài viết 7 phần (5')

- **Khung chuẩn:** **Hook (câu móc) → Bối cảnh → Vấn đề → Phân tích → Giải pháp → Ví dụ → CTA (lời kêu gọi hành động)**.
- **Quy tắc từng phần:** Hook ≤2 dòng, phải khiến ICP *"đó là mình!"* — **ưu tiên lấy từ 3 headline / 10 câu ads của Sales Message Pack** · Bối cảnh dùng chuyện thật · Phân tích là nơi thể hiện chuyên môn (VÌ SAO) · Ví dụ luôn có tên viết tắt + con số · **CTA chỉ 1 hành động duy nhất** — ưu tiên lấy từ 3 CTA đã có ở Ngày 03.
- **Lưu ý:** Không phải bài nào cũng đủ 7 phần — bài checklist có thể bỏ Bối cảnh; bài bán mềm rút Phân tích. Nhưng **KHÔNG BAO GIỜ thiếu Hook và CTA**.

### Khối 4 — 4 loại bài phải có hôm nay (5')

| Loại bài | Công thức lõi | Dấu hiệu đạt | Số lượng |
|---|---|---|:---:|
| **Giáo dục / niềm tin** | Hiểu lầm phổ biến → sự thật → cách làm đúng | Khách đọc xong *"à ra thế"*, save/share | **≥4** |
| **Xử lý phản đối** | Nêu thẳng nghi ngờ (**đúng nguyên văn khách nói**) → đồng cảm → bóc tách → bằng chứng | Viết trúng câu khách hay nói: *"sao đắt hơn trà ngoài siêu thị thế em"* | **≥3** |
| **Bán hàng mềm** | Câu chuyện/kết quả → offer xuất hiện tự nhiên → CTA inbox | Không có chữ "khuyến mãi" vẫn ra inbox | **≥2** |
| **Kể chuyện cá nhân** | Tình huống thật → cảm xúc → bài học → liên hệ nghề | Có chi tiết chỉ người trong cuộc mới biết | **≥1** |

> 🍵 **Bài kể chuyện cá nhân của MSX = chuyện của founder Nguyễn Hoàng Hưng:** chuyến lên Mẫu Sơn, gặp người Dao hái thảo mộc lúc sương chưa tan, vì sao anh quyết định làm trà thay vì bán nguyên liệu thô. **Đây là bài không AI nào viết được thay bạn** — bạn phải kể, AI chỉ biên tập.

### Khối 5 — LUẬT TRUY NGUYÊN: mã nguồn cho từng bài (5')

> **Không có bài nào được sinh ra từ hư không. Bài không truy nguyên được = bài bịa = không đăng.**

Mỗi dòng trong Content Bank phải điền cột **`Mã nguồn`**:

| Mã | Nghĩa | Lấy từ |
|:---:|---|---|
| `P#` / `D#` / `F#` / `O#` | Pain / Desire / Fear / Objection | PDFO Map — Ngày 02 |
| `J#` | Giai đoạn Customer Journey (⚡ = đang bỏ trống) | Journey Map — Ngày 02 |
| `V#` | **Câu nói NGUYÊN VĂN của khách thật** | Ngày 02 |
| `Q##` | Câu hỏi thật trong FAQ & Objection Database | Ngày 04 |
| `OF#` | Khối offer ①→⑦ | Core Offer — Ngày 03 |

**Ngưỡng chấm của Ngày 09:**
- **≥80%** bài có mã nguồn hợp lệ (tức ≥8/10 bài).
- **≥3/10 bài** truy về **câu nói nguyên văn của khách thật** (`V#` hoặc `Q##`). ← đây là thứ chống "content nghe tây".
- **≥1 bài** lấp giai đoạn Journey ⚡ đang bỏ trống. 🍵 MSX: **J2** (Nhận ra vấn đề) và **J6** (Sử dụng — sau mua chưa có chuỗi hướng dẫn dùng).

**Kho mã nguồn 🍵 MSX (dùng trực tiếp hôm nay):**

| Nhóm | Nội dung |
|---|---|
| **Pain** | `P1` ngủ không sâu, sáng dậy vẫn mệt · `P2` uống trà sức khoẻ vị khó uống, bỏ dở · `P3` mua cho bố mẹ phải chắc nguồn gốc |
| **Desire** | `D1` tối uống một tách, ngủ một mạch tới sáng · `D2` thói quen chăm sức khoẻ nhẹ nhàng, tự nhiên · `D3` quà cho bố mẹ không quá phổ thông |
| **Fear** | `F1` sợ thảo mộc trôi nổi, công dụng thổi phồng · `F2` sợ không hợp cơ địa, bệnh nền dùng sai · `F3` sợ giá cao mà không khác gì trà chợ |
| **Objection** | `O1` *"sao đắt hơn trà ngoài siêu thị?"* · `O2` *"mua 1 hộp dùng thử trước được không?"* · `O3` *"có review khách thật không?"* |
| **5 câu NGUYÊN VĂN khách** | `V1` *"trà mẩy gòm này người huyết áp cao uống đc k em"* · `V2` *"chị ngủ kém lắm, uống bao lâu thì thấy đỡ"* · `V3` *"sao đắt hơn trà ngoài siêu thị thế em"* · `V4` *"cho chị mua 1 hộp dùng thử trước đc k, sợ mua nhiều uống k hợp"* · `V5` *"mua tặng mẹ thì nên lấy trà hay viên em nhỉ"* |
| **Objection trong KB (N4)** | `O01` *"Đắt hơn trà thường quá"* · `O08` *"Trà này có chữa mất ngủ không?"* |

### Khối 6 — Kiểm duyệt: checklist 5 câu + ranh giới pháp lý (5')

**Checklist 5 câu chống "máy móc"** — chạy trước khi duyệt MỌI bài:
1. Đúng insight (thấu hiểu) khách của **MÌNH** chưa?
2. Có dẫn về offer (trực tiếp hoặc gián tiếp) không?
3. Người lạ đọc có hiểu ngay không (không thuật ngữ)?
4. Có **đúng 1 CTA** rõ ràng không?
5. Che tên đi, có nhận ra là **giọng của mình** không?

**Quy tắc 30%:** một bài AI đạt chuẩn khi bạn đã **sửa/thêm ~30%** — thường là 3 việc: (a) thay ví dụ AI bịa bằng **chuyện thật**, (b) thêm **con số thật**, (c) viết lại **hook theo giọng mình**.

> 🚨 **RANH GIỚI PHÁP LÝ — dòng thứ 6 bắt buộc trong checklist duyệt bài:**
> Chỉ được nói **"hỗ trợ thư giãn buổi tối"**. **CẤM tuyệt đối:** *"chữa mất ngủ"* · *"khỏi"* · *"đặc trị"* · *"thần dược"* · *"cam kết 100%"*.
> Phụ nữ có thai / cho con bú / trẻ em / người có bệnh nền → luôn khuyên hỏi bác sĩ.
> **Vi phạm = −7đ rubric + bài KHÔNG ĐƯỢC ĐĂNG.** Một câu quá đà phá huỷ niềm tin của 5.000 khách đã có — và là rủi ro pháp lý thật với ngành thực phẩm/dược liệu, spa, nha khoa, clinic.

### Khối 7 — Repurpose: 1 bài → 4 định dạng (4')

1 bài dài Facebook → **(a)** bản **Zalo broadcast** 5–7 dòng · **(b)** script video 45 giây · **(c)** email/tin nhắn chăm sóc · **(d)** 3–5 câu quote (trích dẫn) làm visual (dùng ở Ngày 10).

> **Bản Zalo KHÔNG phải bài tập cho vui.** ≥2 bản Zalo hôm nay = **2 slot thật** trong lịch 14 ngày của Ngày 13 (1 broadcast/tuần). Viết ẩu = tuần sau thiếu nội dung để đăng. 🍵 MSX gửi qua **Zalo OA 0822.928.988**, ưu tiên tệp **khách cũ 3 tháng chưa mua lại**.

> **Thích ứng ngành khác:** **Nha khoa** — bài xử lý phản đối điển hình: *"Niềng răng 40 triệu, trả góp có đáng không?"* (ranh giới: cấm cam kết "răng đều tuyệt đối"). **Giáo dục** — bài kể chuyện cá nhân của giáo viên về 1 học sinh tiến bộ là loại bài mạnh nhất. **Gym/coaching** — bán mềm qua ảnh check-in kết quả học viên kèm story (cấm "giảm 10kg trong 1 tháng"). **Khung 7 phần + checklist 5 câu + luật truy nguyên giữ nguyên mọi ngành.**

---

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|:---:|---|---|
| **10'** | Warm-up + chữa bài Ngày 08 | Chiếu 2 bảng 60 ý tưởng tốt (khen cụ thể: **có cột Mã nguồn điền đủ**, tiêu đề cụ thể) + 1 bài mắc lỗi *"pillar = menu sản phẩm"* hoặc *"ý tưởng không có mã nguồn"* (chữa nóng 3'). |
| **25'** | Giảng kiến thức trọng tâm | 7 khối phần 2. Trọng tâm thời lượng: **Khối 2 (Brand Voice là NÂNG CẤP)** · **Khối 5 (Luật truy nguyên)** · **Khối 6 (kiểm duyệt + ranh giới pháp lý)** — 3 kỹ năng quyết định chất lượng cả tuần. |
| **30'** | **Demo live trên 🍵 MSX** | Theo kịch bản phần 4: nâng cấp Brand Voice từ khối `[GIỌNG]` → mở Sales Message Pack lấy đạn → viết 2 bài (1 giáo dục, 1 xử lý phản đối `O1+V3`) → demo batch 3 bài → repurpose 1 bài ra **bản Zalo dùng thật**. |
| **15'** | Học viên làm tại chỗ + Q&A | Học viên chạy **Prompt 1** ngay tại lớp — **kiểm tra: ai không dán khối `[GIỌNG]` cũ vào INPUT là làm sai, sửa ngay.** Trainer soát nhanh 3 bản. |
| **10'** | Giao bài tập | Chiếu phần 6 + rubric. Nhấn: *"Tối nay bắt buộc 10 bài duyệt kỹ + 2 bản Zalo. 20 bài batch là bonus — làm khi 10 bài đầu đã đạt chuẩn."* Nhắc **≥3/10 bài phải truy về câu khách nói nguyên văn**. |

---

## 4. 🎬 Kịch Bản Demo Live (🍵 MSX Group)

**Bước 1 (6') — NÂNG CẤP Brand Voice, không dựng lại.**
- Mở **AI Marketing Assistant** (Ngày 06 — đã có Knowledge Base MSX). Chạy **Prompt 1**, dán vào INPUT **khối `[GIỌNG]` ≤80 từ** của MSX (Ngày 05) + trỏ tới Brand Voice trong KB.
- AI **không** hỏi lại từ đầu. AI đọc khối `[GIỌNG]` rồi hỏi đúng **3 câu bổ sung**: (1) *"Anh Hưng kể 1 lần anh nói thật với khách dù có thể mất đơn?"* — trainer đóng vai founder: *"Có chị hỏi trà chữa mất ngủ không, em nói thẳng: trà không phải thuốc, chị mất ngủ kéo dài thì phải đi khám. Chị ấy không mua hôm đó, nhưng 2 tháng sau quay lại mua combo."* (2) *"Quảng cáo kiểu gì trong ngành khiến anh khó chịu nhất?"* — *"Trà nào cũng tự xưng thần dược."* (3) *"Dán 1 đoạn anh từng viết mà khách phản hồi tốt."*
- **Kết quả:** Brand Voice Guideline 1 trang, 5 phần. Lưu ngay vào Knowledge Base RocketAgent với tên `MSX Group — Brand Voice Guideline`.
- **Câu chốt trước lớp:** *"Từ giờ mọi prompt viết bài đều tự động mang giọng này. Bạn không nạp lại giọng vào từng prompt nữa."*

**Bước 2 (4') — MỞ KHO ĐẠN trước khi viết chữ nào.**
- Trainer mở **Sales Message Pack (Ngày 03)** của MSX lên màn hình. Chỉ vào: 1 hook chủ đạo · 3 headline · 3 CTA · 5 angle · 10 câu ads (mỗi câu có chú thích `P#/D#/F#`).
- Thông điệp: *"Trước khi bảo AI 'viết cho tôi một bài', hãy nhìn xem bạn đã có sẵn gì. Hook bài hôm nay lấy từ đây. CTA lấy từ đây. Bạn chỉ sáng tác mới khi kho không có."*

**Bước 3 (8') — Bài #1 (giáo dục), lấp Journey ⚡ J2.**
- Ý ⭐ từ Ngày 08: *"3 dấu hiệu bạn đang 'ngủ đủ giờ mà vẫn mệt' — và vì sao đó không phải do bạn lười"* · **Mã nguồn: `P1 + D1 + J2`**.
- Chạy **Prompt 2** (bản cá nhân hoá của **M01 — "viết bài Facebook theo angle"** trong Prompt Library N5). Hook lấy từ headline #2 của Sales Message Pack.
- **Duyệt live — phần quan trọng nhất của demo.** Trainer đọc to và sửa 3 chỗ:
	- Hook AI viết: *"Bạn có biết mất ngủ ảnh hưởng đến sức khoẻ như thế nào?"* → 🔴 **SAI TỆP** — chị Hương đã Solution Aware, không cần dạy "mất ngủ là gì". Sửa: *"Chị ngủ đủ 7 tiếng mà sáng dậy vẫn như chưa ngủ. Không phải chị lười — là giấc ngủ của chị nông."*
	- Ví dụ AI bịa *"một khách hàng nọ"* → thay bằng chất liệu thật: *"Chị H. (40t, kế toán ở Cầu Giấy) nhắn em lúc 22h40: 'chị ngủ kém lắm, uống bao lâu thì thấy đỡ' (`V2`)…"*
	- CTA mơ hồ *"hãy liên hệ chúng tôi"* → CTA #1 trong Sales Message Pack: *"Anh/chị đang mắc dấu hiệu số mấy? Comment con số, em gửi bản hướng dẫn 'nếp tối 30 phút' của MSX."*
- Chạy **checklist 5 câu + dòng ranh giới pháp lý** trước lớp → đạt → dán vào Content Bank, điền cột `Mã nguồn` = `P1+D1+J2` và cột `Đã sửa gì so với AI`.

**Bước 4 (7') — Bài #2 (xử lý phản đối), dùng câu khách nói nguyên văn.**
- Chạy **Prompt 3** với phản đối thật: **`O1` + `V3`** — *"sao đắt hơn trà ngoài siêu thị thế em"* + đối chiếu `O01` trong FAQ & Objection Database (N4).
- Đoạn bóc tách đáng chiếu (giữ nguyên nguyên tắc "phép tính người thường nhẩm được"): *"359.000đ / 30 túi = **khoảng 12.000đ một tối**. Bằng nửa ly cà phê. Nhưng khác biệt không nằm ở phép chia — nó nằm ở **độ cao 800–1.541m** nơi cây mẩy gòm mọc, ở đôi tay người Dao hái thủ công, và ở **chứng nhận OCOP 3★** mà trà 50k ngoài siêu thị không có. Nếu anh/chị vẫn phân vân — **cứ lấy 1 hộp dùng thử trước** (`O2`/`V4`), hợp rồi hãy tính combo."*
- 🚨 Trainer dừng lại 30 giây, chỉ vào màn hình: *"Cả bài này KHÔNG có một chữ 'chữa mất ngủ'. Đó không phải may mắn — đó là ràng buộc nằm trong prompt."*

**Bước 5 (3') — Demo batch 3 bài.**
- Chạy **Prompt 4** với 3 ý tiếp theo. Cho lớp thấy: vì Brand Voice + 2 bài đã duyệt nằm trong hội thoại, 3 bản nháp mới **ra giọng chuẩn hơn hẳn lần đầu**.
- Thông điệp: **"Batch chỉ tốt khi 10 bài đầu đã dạy AI thế nào là ĐẠT. Đó là lý do Core là 10 bài duyệt kỹ, không phải 30 bài."**

**Bước 6 (2') — Repurpose bài #1 → bản Zalo DÙNG THẬT.**
- Chạy **Prompt 5** (bản cá nhân hoá của **M14 — "biến 1 bài dài thành 5 định dạng"**, N5) → nhận bản Zalo 6 dòng + script video 45s + tin chăm sóc + 3 quote.
- Trainer chỉ vào Repurpose Sheet, cột `Trạng thái sử dụng`: **"Zalo broadcast — Tuần 1, slot thứ Tư"**. *"Đây không phải bài tập. Đây là nội dung tuần sau anh/chị bấm gửi thật qua Zalo OA."*

> 🚀 **Chỗ duy nhất mở RocketAI hôm nay (nếu lớp có học viên B2B):** bài giáo dục B2B **không kể chuyện vùng cao** mà **phản biện**: *"4 tiếng mỗi ngày ngồi nghĩ caption — ai đang điều hành spa thay chị?"* → bóc tách chi phí cơ hội → gói **OS Installed 25tr**. Avatar: chị Mai, chủ Spa ABC. Khung 7 phần + luật truy nguyên **giữ nguyên**.

---

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

> ⏱ **Tổng Core: dùng template điền sẵn 115' · lần đầu tự làm 160'.**
> Mọi prompt chạy trong **AI Marketing Assistant (Ngày 06)** — **không dán lại ICP/Offer**, KB đã có sẵn.

**Cụm A — Nâng cấp Brand Voice · ⏱ template: 20' · lần đầu tự làm: 30'**
- [ ] Mở Prompt Library (N5), **copy khối `[GIỌNG]` ≤80 từ** của DN mình.
- [ ] Chạy **Prompt 1**, **dán khối `[GIỌNG]` vào INPUT** + trỏ Brand Voice trong KB (N4). *Nếu AI bắt đầu hỏi lại từ câu "3 từ mô tả DN của bạn?" → bạn đã dán thiếu input. Dừng, dán lại.*
- [ ] Trả lời nghiêm túc **3 câu bổ sung** (lần nói thật mất đơn · quảng cáo nào khiến bạn khó chịu · 1 đoạn cũ khách phản hồi tốt) — **10 phút giá trị nhất hôm nay**.
- [ ] Sửa tay phần "2 đoạn văn mẫu" cho đúng giọng thật của bạn.
- [ ] **Kiểm tra phần "5 điều KHÔNG BAO GIỜ" có chứa đủ danh sách từ cấm ngành mình** (🍵 MSX: chữa/khỏi/đặc trị/thần dược/cam kết 100%).
- [ ] Lưu vào Knowledge Base với tên `[Tên DN] — Brand Voice Guideline`.

**Cụm B — Mở kho đạn (Sales Message Pack) · ⏱ template: 10' · lần đầu tự làm: 15'**
- [ ] Mở **Sales Message Pack (Ngày 03)**. Kẻ bảng đối chiếu: **10 ý ⭐ (N8) × hook/headline/CTA có sẵn nào dùng được cho ý đó**.
- [ ] Đánh dấu ý nào **chưa có đạn** → chỉ những ý này mới cần AI sáng tác hook mới.
- [ ] *Bỏ qua cụm này = bạn sẽ để AI sáng tác lại thứ bạn đã trả tiền và trả thời gian để làm ra tuần trước.*

**Cụm C — 10 bài Core · ⏱ template: 70' · lần đầu tự làm: 95'**
- [ ] Mở bảng 60 ý tưởng, xếp **10 ý ⭐** theo loại bài, đảm bảo cơ cấu **≥4 giáo dục / ≥3 phản đối / ≥2 bán mềm / ≥1 kể chuyện**. Lệch cơ cấu → hoán đổi với ý khác trong top 15.
- [ ] **Kiểm tra trước khi viết:** ≥3/10 ý phải gắn `V#` hoặc `Q##` (câu khách nói nguyên văn) · ≥1 ý lấp Journey ⚡ (🍵 MSX: `J2` hoặc `J6`).
- [ ] Viết theo **lô 2 bài/lượt**: **Prompt 2** (bài giáo dục/bán mềm) hoặc **Prompt 3** (bài xử lý phản đối) hoặc **Prompt 2 biến thể M02** (bài kể chuyện) → duyệt bằng **checklist 5 câu + dòng ranh giới pháp lý** → **sửa ≥30%** (hook, ví dụ thật, CTA) → dán vào **Content Bank (T9.2)**.
- [ ] Mỗi bài điền đủ: `Loại bài · Pillar · Tầng phễu · **Mã nguồn** · CTA · **Đã sửa gì so với AI** (≥2 gạch đầu dòng) · Trạng thái`.
- [ ] **Nghỉ 5' sau mỗi 4 bài** — duyệt bài mệt sẽ thành duyệt ẩu.

**Cụm D — Repurpose 3 bài (≥2 bản Zalo dùng thật) · ⏱ template: 15' · lần đầu tự làm: 20'**
- [ ] Chọn 3 bài tốt nhất → chạy **Prompt 5** cho từng bài → dán vào **Repurpose Sheet (T9.3)**.
- [ ] **Đánh dấu 2 bản Zalo broadcast** vào cột `Trạng thái sử dụng`: *"Zalo broadcast — Tuần 1"* và *"Zalo broadcast — Tuần 2"*. **Đây là 2 trong 14 slot của lịch Ngày 13.**

> 🆘 **Luật cứu hộ:** Quá giờ → làm theo thứ tự ưu tiên **A → B → C → D**. Bonus không bắt buộc, không trừ điểm. **Nộp 80% đúng hạn thắng 100% trễ 2 ngày.** Không kịp 10 bài → nộp 8 bài **đúng cơ cấu + đủ mã nguồn** vẫn được chấm (trừ điểm nhóm 1). Tuyệt đối **không** cắt cụm A hoặc cụm D.

**Bonus (45–60', chỉ làm SAU khi Core đạt):**
- [ ] Chạy **Prompt 4** theo lô 5 bài × 4 lượt = **20 bài** từ 20 ý tiếp theo.
- [ ] Duyệt nhanh mỗi bài bằng checklist 5 câu (2'/bài) — chỉ sửa bài trượt checklist.
- [ ] Cập nhật Content Bank đủ 30 bài (nhãn `[Batch]`) + mở rộng Repurpose Sheet lên 10 bài.

---

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Dựng cỗ máy viết bài cho DN của bạn: **nâng cấp** Brand Voice từ tài sản Tuần 1 → sản xuất và **DUYỆT KỸ 10 bài** từ 10 ý ⭐ (đúng cơ cấu 4 loại, đủ mã nguồn) → tái sử dụng 3 bài, trong đó **2 bản Zalo broadcast dùng thật cho lịch Ngày 13**.

**Deliverable nộp (thread cohort, deadline 23h59 hôm nay):**

1. `[Tên DN] — Ngày 09 — Brand Voice Guideline` — đủ 5 phần. **Bắt buộc ghi ở đầu file: "Nâng cấp từ khối `[GIỌNG]` (N5) + Brand Voice KB (N4)"** và dán khối `[GIỌNG]` cũ vào cuối file để mentor đối chiếu.
2. `[Tên DN] — Ngày 09 — Content Bank` (Google Sheet, template **T9.2**) — 10 bài Core đầy đủ nội dung + metadata, **cột `Mã nguồn` điền ≥8/10 bài**, **≥3 bài mang mã `V#`/`Q##`**, **≥1 bài lấp Journey ⚡**, cột `Đã sửa gì so với AI` ≥2 gạch đầu dòng/bài.
3. `[Tên DN] — Ngày 09 — Repurpose Sheet` (tab trong Sheet trên) — 3 bài × 4 phiên bản, **2 bản Zalo đã gán slot tuần**.
4. *(Bonus)* Content Bank đủ 30 bài — 20 bài batch dán nhãn `[Batch]`.

---

## 7. 📄 Template Đi Kèm

**T9.1 — Brand Voice Guideline (Google Doc, 1 trang)**
Trường chính (có **bản điền mẫu 🍵 MSX** đính kèm):
- Dòng đầu: **"Nâng cấp từ: khối `[GIỌNG]` (N5) + Brand Voice trong KB (N4)"** + dán nguyên khối `[GIỌNG]` cũ.
- ① Tính cách thương hiệu (3 từ + 1 câu/từ) · ② Xưng hô · ③ 5 điều LUÔN làm · ④ 5 điều KHÔNG BAO GIỜ (**bắt buộc chứa danh sách từ cấm ngành**) · ⑤ Từ ngữ đặc trưng + 2 đoạn văn mẫu chuẩn giọng (1 giáo dục, 1 bán mềm).

**T9.2 — Content Bank (Google Sheet)**
Cột: `STT | Tiêu đề | Loại bài (giáo dục/phản đối/bán mềm/kể chuyện) | Pillar | Tầng phễu | **Mã nguồn** (P#/D#/F#/O#/J#/V#/Q##/OF#) | Nội dung đầy đủ | CTA (lấy từ Sales Message Pack?) | **Đã sửa gì so với AI** | Ranh giới pháp lý ✅/❌ | Nhãn [Core]/[Batch] | Trạng thái (sẵn sàng/cần sửa/đã đăng) | Ngày dự kiến đăng`.
Có sẵn **2 dòng MSX mẫu** (chính là 2 bài demo live) + hàng công thức tự đếm: *% bài có mã nguồn* và *số bài mang `V#`/`Q##`*.

**T9.3 — Content Repurpose Sheet (tab trong T9.2)**
Cột: `Bài gốc (STT) | Bản Zalo broadcast (5–7 dòng) | Script video 45s (hook/thân/CTA) | Email–tin chăm sóc | 3 quote làm visual | **Trạng thái sử dụng** (Zalo Tuần 1 / Zalo Tuần 2 / Video N11 / Visual N10)`. 1 dòng MSX mẫu.

---

## 8. 🤖 Prompt Mẫu

> Cả 5 prompt là **bản cá nhân hoá của Prompt Library nhóm M (Ngày 05)**: Prompt 2 = **M01** *"viết bài Facebook theo angle"* · Prompt 2-B (kể chuyện) = **M02** · Prompt 5 = **M14** *"biến 1 bài dài thành 5 định dạng"*.
> **Track A — chạy trong AI Marketing Assistant (Ngày 06):** KB đã có ICP/Offer/Brand Voice → **không dán lại**. Track B (ChatGPT/Claude thường): dán thêm khối tóm tắt ICP + Offer.

### Prompt 1 — NÂNG CẤP Brand Voice (không phỏng vấn lại từ đầu)

```
[VAI TRÒ]
Bạn là chuyên gia xây dựng giọng thương hiệu, giỏi MỞ RỘNG một mô tả giọng
ngắn thành tài liệu hướng dẫn viết đầy đủ — KHÔNG bao giờ dựng lại từ số 0
khi khách đã có sẵn nguyên liệu.

[BỐI CẢNH]
Tôi ĐÃ CÓ giọng thương hiệu: (a) khối [GIỌNG] ≤80 từ dùng trong mọi prompt,
(b) mục Brand Voice trong Knowledge Base. Tôi KHÔNG muốn trả lời lại những
câu tôi đã trả lời tuần trước. Việc của bạn là mở rộng, không phải bắt đầu lại.

[NHIỆM VỤ]
Bước 1 — ĐỌC & PHẢN CHIẾU: đọc khối [GIỌNG] và Brand Voice trong KB, tóm tắt
lại cho tôi bằng 5 gạch đầu dòng những gì bạn ĐÃ BIẾT về giọng của tôi.
Bước 2 — CHỈ RA LỖ HỔNG: liệt kê chính xác những gì Guideline 1 trang cần mà
khối [GIỌNG] hiện CHƯA có.
Bước 3 — HỎI THÊM ĐÚNG 3 CÂU (mỗi lần 1 câu, chờ tôi trả lời):
  (1) Kể 1 lần bạn nói thật với khách dù có thể mất đơn.
  (2) Quảng cáo kiểu gì trong ngành khiến bạn khó chịu nhất?
  (3) Dán 1 đoạn bạn từng viết/nhắn mà khách phản hồi tốt.
Bước 4 — TỔNG HỢP Brand Voice Guideline 1 trang, 5 phần:
  ① Tính cách 3 từ (+1 câu giải thích mỗi từ)
  ② Xưng hô
  ③ 5 điều LUÔN làm
  ④ 5 điều KHÔNG BAO GIỜ làm (bắt buộc gồm danh sách TỪ CẤM của ngành tôi)
  ⑤ Từ ngữ đặc trưng + 2 đoạn văn mẫu chuẩn giọng (1 giáo dục, 1 bán mềm,
     mỗi đoạn 4–6 câu)

[DỮ LIỆU ĐẦU VÀO]
- Khối [GIỌNG] hiện có (Ngày 05): {{dán nguyên khối ≤80 từ}}
- Brand Voice trong KB (Ngày 04): {{dán, hoặc ghi "lấy từ Knowledge Base"}}
- Từ CẤM bắt buộc của ngành tôi: {{liệt kê}}

[ĐỊNH DẠNG ĐẦU RA]
Markdown 1 trang, tiêu đề "[Tên DN] — Brand Voice Guideline".
Dòng đầu ghi: "Nâng cấp từ khối [GIỌNG] (N5) + Brand Voice KB (N4)".

[RÀNG BUỘC]
- TUYỆT ĐỐI KHÔNG hỏi lại những gì đã có trong khối [GIỌNG]. Hỏi lại = làm sai.
- Chỉ hỏi ĐÚNG 3 câu ở Bước 3. Không hỏi câu thứ 4.
- 2 đoạn văn mẫu phải dùng chất liệu từ chính câu trả lời của tôi, không generic.
- Mục ④ phải giữ nguyên 100% các từ cấm tôi cung cấp.
```

**Ví dụ đã điền — 🍵 MSX (khối INPUT):**
```
- Khối [GIỌNG] hiện có (N5):
  "MSX xưng 'em', gọi khách 'anh/chị'. Giọng mộc mạc, tử tế, có gốc gác.
  Mở bài bằng hình ảnh vùng cao Mẫu Sơn. Từ đặc trưng: dược liệu vùng cao
  Mẫu Sơn, thảo mộc tự nhiên, đồng hành cùng thói quen mỗi ngày, lối vào
  cuộc sống xanh. Luôn nói rõ độ cao 800–1.541m, người Dao/Tày/Nùng hái
  thủ công, OCOP 3★. Không nói sản phẩm như thuốc. Tối đa 3 emoji/bài."
- Brand Voice trong KB (N4): lấy từ Knowledge Base — mục "Brand Voice" của
  Công ty CP Lối vào Mẫu Sơn Xanh.
- Từ CẤM bắt buộc: thần dược · chữa khỏi · chữa mất ngủ · đặc trị · khỏi ·
  cam kết 100% · quá 3 emoji/bài.
```

---

### Prompt 2 — Viết 1 bài hoàn chỉnh (khung 7 phần) — *cá nhân hoá của M01*

```
[VAI TRÒ]
Bạn là copywriter (người viết quảng cáo) chuyên bài Facebook cho doanh nghiệp
Việt Nam bán qua tư vấn. Bạn viết đúng Brand Voice được cung cấp, không bao
giờ dùng giọng "robot tiếp thị".

[BỐI CẢNH]
- Brand Voice Guideline: lấy từ Knowledge Base (đã nạp hôm nay).
- ICP + mức nhận thức: lấy từ Knowledge Base.
- ⚠️ Khách của tôi ở MỨC NHẬN THỨC {{số}} — {{tên mức}}. Hệ quả: KHÔNG được
  dạy lại kiến thức khách đã biết. Bài phải đi thẳng vào SO SÁNH và BẰNG CHỨNG.

[NHIỆM VỤ]
Viết 1 bài Facebook hoàn chỉnh theo khung 7 phần:
Hook (≤2 dòng) → Bối cảnh → Vấn đề → Phân tích (VÌ SAO — thể hiện chuyên môn)
→ Giải pháp → Ví dụ (người thật + con số) → CTA (đúng 1 hành động).

[DỮ LIỆU ĐẦU VÀO]
- Ý tưởng ⭐ (từ bảng 60 ý, Ngày 08): {{tiêu đề + angle + tầng phễu}}
- MÃ NGUỒN của ý này: {{ví dụ: P1 + D1 + J2}}
- Loại bài: {{giáo dục / bán hàng mềm / kể chuyện cá nhân}}
- ĐẠN CÓ SẴN từ Sales Message Pack (Ngày 03) — ƯU TIÊN DÙNG, đừng sáng tác lại:
  · Hook/headline dùng được: {{dán}}
  · CTA dùng được: {{dán}}
  · Angle dùng được: {{dán}}
- Chất liệu thật của tôi (BẮT BUỘC AI dùng, cấm bịa thêm): {{chuyện khách thật /
  con số thật / quan sát thật}}
- Từ CẤM: {{dán}}

[ĐỊNH DẠNG ĐẦU RA]
- Bài 250–400 chữ, xuống dòng thoáng (2–3 câu/đoạn), tối đa {{n}} emoji.
- Cuối bài: 3–5 hashtag + 1 dòng [Gợi ý ảnh đi kèm].
- Sau bài, ghi 1 dòng: "Mã nguồn: {{...}}" và "Đạn đã dùng từ Sales Message
  Pack: {{hook nào / CTA nào}}".
- Đề xuất 3 phương án Hook để tôi chọn — trong đó ≥1 phương án lấy TRỰC TIẾP
  từ đạn có sẵn.

[RÀNG BUỘC]
- Tuân thủ tuyệt đối mục "KHÔNG BAO GIỜ" trong Brand Voice và danh sách TỪ CẤM.
- KHÔNG bịa số liệu, KHÔNG bịa tên khách. Thiếu chất liệu → HỎI LẠI TÔI, không bịa.
- KHÔNG viết "Hãy liên hệ chúng tôi" — CTA phải cụ thể, đo được.
- Không dùng thuật ngữ chuyên ngành mà không giải thích.
```

**Ví dụ đã điền — 🍵 MSX (khối INPUT):**
```
- Ý tưởng ⭐: "3 dấu hiệu bạn đang 'ngủ đủ giờ mà vẫn mệt' — và vì sao đó
  không phải do bạn lười" — angle cảnh báo — TOF.
- MÃ NGUỒN: P1 + D1 + J2  (J2 = giai đoạn Journey đang bỏ trống ⚡)
- Loại bài: giáo dục.
- ĐẠN CÓ SẴN từ Sales Message Pack:
  · Headline #2: "Ngủ đủ 7 tiếng mà sáng dậy vẫn như chưa ngủ"
  · CTA #1: "Comment con số, em gửi bản hướng dẫn 'nếp tối 30 phút' của MSX"
  · Angle #3: so sánh giấc ngủ NÔNG vs giấc ngủ SÂU (không dạy lại "mất ngủ là gì")
- Chất liệu thật: Chị H. (40t, kế toán Cầu Giấy) nhắn lúc 22h40: "chị ngủ kém
  lắm, uống bao lâu thì thấy đỡ" (V2). Cách dùng thật: 1 túi 2,5g + 150–200ml
  nước sôi, uống buổi tối. 5.000+ khách đã dùng. OCOP 3★.
- Từ CẤM: thần dược · chữa khỏi · chữa mất ngủ · đặc trị · cam kết 100%.
  Chỉ được nói "hỗ trợ thư giãn buổi tối". Tối đa 3 emoji.
```

---

### Prompt 3 — Bài xử lý phản đối (dùng câu khách nói NGUYÊN VĂN)

```
[VAI TRÒ]
Bạn là chuyên gia tâm lý bán hàng + copywriter, giỏi viết bài gỡ nghi ngờ mà
không gây cảm giác đang bị bán hàng.

[BỐI CẢNH]
- Brand Voice + FAQ & Objection Database: lấy từ Knowledge Base.
- Khách mua qua tư vấn, quyết định chậm, hay dừng lại ở vài câu từ chối quen thuộc.

[NHIỆM VỤ]
Viết 1 bài Facebook xử lý TRỰC DIỆN một lời phản đối, theo 5 bước:
(1) Nêu thẳng lời phản đối bằng ĐÚNG NGUYÊN VĂN khách nói (không diễn giải lại
    cho "văn vẻ" — giữ nguyên cả lỗi chính tả nếu có, đặt trong ngoặc kép)
(2) Đồng cảm thật lòng, thừa nhận phần ĐÚNG của khách
(3) Bóc tách bằng logic/con số — phép tính người thường nhẩm được
(4) Bằng chứng thật (chứng nhận, nguồn gốc, số khách, case thật)
(5) CTA nhẹ, không ép — mở đường lùi cho khách (ví dụ: dùng thử 1 đơn vị nhỏ)

[DỮ LIỆU ĐẦU VÀO]
- Lời phản đối NGUYÊN VĂN của khách: {{dán V# — copy y nguyên}}
- Mã nguồn: {{O# + V# + J#}}
- Câu trả lời chuẩn đã có trong FAQ & Objection Database (Q##): {{dán}}
- Sự thật/con số dùng để bóc tách: {{giá, số đơn vị, thời gian, so sánh}}
- Bằng chứng thật: {{chứng nhận / vùng nguyên liệu / số khách / case}}
- Offer + CTA: {{1 câu}}
- Từ CẤM: {{dán}}

[ĐỊNH DẠNG ĐẦU RA]
Bài 250–350 chữ + 3 phương án hook + [Gợi ý ảnh đi kèm] + 1 dòng "Mã nguồn: …".

[RÀNG BUỘC]
- KHÔNG chê khách sai, KHÔNG mỉa mai người tiết kiệm.
- Phần bóc tách BẮT BUỘC có 1 phép tính cụ thể.
- KHÔNG hứa hẹn tuyệt đối (100% / vĩnh viễn / cam kết khỏi hẳn / đặc trị).
- Câu trả lời phải NHẤT QUÁN với FAQ & Objection Database — không tự chế
  lập luận mới trái với câu trả lời chuẩn đã duyệt.
```

**Ví dụ đã điền — 🍵 MSX (khối INPUT):**
```
- Lời phản đối NGUYÊN VĂN: "sao đắt hơn trà ngoài siêu thị thế em" (V3)
- Mã nguồn: O1 + V3 + J4 (giai đoạn So sánh)
- Câu trả lời chuẩn từ KB (O01 — "Đắt hơn trà thường quá"): MSX không định vị
  như trà phổ thông; khác biệt ở vùng nguyên liệu 800–1.541m + công thức thảo
  mộc + chứng nhận OCOP 3★; có thể bắt đầu bằng 1 hộp dùng thử.
- Sự thật/con số: 359.000đ/hộp ÷ 30 túi ≈ 12.000đ/tối. Trà siêu thị ~50k/hộp.
  Combo mua 3 tặng 1 = 1.015.000đ. Freeship đơn từ 500.000đ.
- Bằng chứng thật: OCOP 3★ · vùng Mẫu Sơn (Lạng Sơn) 800–1.541m · người Dao/
  Tày/Nùng hái thủ công · 5.000+ khách · giao qua Viettel Post.
- Offer + CTA: "Anh/chị cứ lấy 1 hộp 359k dùng thử trước (V4/O2). Hợp rồi hãy
  tính combo 3 tặng 1 — 1.015.000đ. Inbox 'MẨY GÒM' để em gửi cách pha."
- Từ CẤM: chữa mất ngủ · khỏi · đặc trị · thần dược · cam kết 100%.
  Chỉ nói "hỗ trợ thư giãn buổi tối".
```

---

### Prompt 4 — Batch 5 bài/lượt (dùng cho 20 bài Bonus)

```
[VAI TRÒ + BỐI CẢNH]
Tiếp tục CHÍNH hội thoại này. Bạn đã có Brand Voice Guideline và đã viết các
bài được tôi DUYỆT ở trên. Hãy coi các bài ĐÃ DUYỆT là chuẩn chất lượng — bắt
chước đúng nhịp câu, độ dài đoạn, cách vào hook và cách kết CTA của chúng.

[NHIỆM VỤ]
Viết 5 bài tiếp theo từ 5 ý tưởng dưới đây, mỗi bài theo đúng khung 7 phần và
đúng chuẩn chất lượng của các bài đã duyệt.

[DỮ LIỆU ĐẦU VÀO]
- 5 ý tưởng (từ bảng 60 ý, Ngày 08), mỗi ý kèm LOẠI BÀI và MÃ NGUỒN: {{dán}}
- Đạn có sẵn (Sales Message Pack) còn chưa dùng: {{dán hook/CTA/angle còn lại}}
- Chất liệu thật dùng chung (chưa dùng ở 10 bài Core): {{2–3 chuyện/con số thật}}
- Từ CẤM: {{dán}}

[ĐỊNH DẠNG ĐẦU RA]
5 bài đánh số. Mỗi bài kèm: [Gợi ý ảnh] + dòng "Mã nguồn: …".
Không cần 3 phương án hook.

[RÀNG BUỘC]
- Bài nào thiếu chất liệu thật → dùng dạng "quan sát chung" TRUNG THỰC
  ("Em để ý nhiều anh/chị…") thay vì bịa case cụ thể. TUYỆT ĐỐI không bịa tên khách.
- Mỗi bài 1 CTA khác nhau; không lặp CTA quá 2 lần trong 5 bài.
- Mọi bài đều phải qua được danh sách TỪ CẤM.
```

**Ví dụ đã điền — 🍵 MSX (5 ý tiếp theo):**
```
1. "Uống trà thảo mộc bao lâu thì thấy khác?" — xử lý phản đối — V2 + P1 + J4
2. "Mẹ 60 tuổi nên uống trà hay dùng viên?" — giáo dục — V5 + D3 + J3
3. "Một ngày của người hái mẩy gòm trên Mẫu Sơn" — kể chuyện — F1 + J2
4. "Hộp trà 359k của anh/chị đi qua bao nhiêu đôi tay?" — niềm tin — F1 + F3 + OF2
5. "Sau khi hết hộp đầu tiên: 3 việc nên làm" — giáo dục — J6 ⚡ + D2
Chất liệu thật dùng chung: founder Nguyễn Hoàng Hưng lên Mẫu Sơn gặp người Dao
hái thảo mộc lúc sương chưa tan · 5.000+ khách · OCOP 3★ · pha 1 túi 2,5g với
150–200ml nước sôi, uống buổi tối.
```

---

### Prompt 5 — Repurpose 1 bài → 4 định dạng — *cá nhân hoá của M14*

```
[VAI TRÒ]
Bạn là biên tập viên đa kênh, giỏi "cắt may" một nội dung cho đúng thói quen
đọc của từng nền tảng Việt Nam.

[NHIỆM VỤ]
Từ bài gốc dưới đây, tạo 4 phiên bản:
(1) BẢN ZALO BROADCAST: 5–7 dòng, mở đầu bằng câu hỏi, đúng 1 CTA.
    ⚠️ Bản này SẼ ĐƯỢC GỬI THẬT qua Zalo OA — viết như đang nhắn cho một
    người cụ thể, không viết như thông cáo.
(2) SCRIPT VIDEO 45 GIÂY: bảng [giây | lời thoại | hình gợi ý].
    Hook 3 giây đầu PHẢI KHÁC hook bài gốc.
(3) EMAIL / TIN NHẮN CHĂM SÓC: tiêu đề ≤8 chữ + thân 80–120 chữ + 1 CTA.
(4) 3 CÂU QUOTE (trích dẫn) ≤20 chữ/câu để làm ảnh trích dẫn (dùng ở Ngày 10).

[DỮ LIỆU ĐẦU VÀO]
- Bài gốc: {{dán toàn bộ bài}}
- Mã nguồn của bài gốc: {{dán — giữ nguyên cho cả 4 phiên bản}}
- Kênh Zalo của tôi: {{OA broadcast / nhắn 1-1}} — chỉnh giọng phù hợp.
- Tệp nhận broadcast: {{ví dụ: khách cũ 3 tháng chưa mua lại}}
- Từ CẤM: {{dán}}

[ĐỊNH DẠNG ĐẦU RA]
4 khối rõ ràng, mỗi khối có tiêu đề. Cuối cùng: 1 dòng đề xuất slot sử dụng
("Zalo broadcast tuần nào / video N11 / quote nào làm visual N10").

[RÀNG BUỘC]
- KHÔNG tóm tắt máy móc — mỗi phiên bản phải TỰ ĐỨNG ĐƯỢC một mình.
- Giữ nguyên Brand Voice và MỌI con số thật của bài gốc.
- Cả 4 phiên bản đều phải qua danh sách TỪ CẤM (kể cả quote — quote hay bị
  cắt cụt thành câu vi phạm).
```

**Ví dụ đã điền — 🍵 MSX (khối INPUT):**
```
- Bài gốc: bài #2 — "Sao đắt hơn trà ngoài siêu thị thế em?" (O1 + V3 + J4)
- Kênh Zalo: OA broadcast (Zalo OA 0822.928.988)
- Tệp nhận broadcast: khách cũ 3 tháng chưa mua lại (trong 5.000+ khách)
- Từ CẤM: chữa mất ngủ · khỏi · đặc trị · thần dược · cam kết 100%
```
**Bản Zalo mẫu (đầu ra — chính là 1 trong 2 slot thật của lịch Ngày 13):**
```
Anh/chị có bao giờ thắc mắc vì sao trà Mẩy Gòm 359k, trong khi trà ngoài siêu
thị chỉ 50k không ạ?

Câu trả lời nằm ở 3 chỗ: cây mọc ở độ cao 800–1.541m trên Mẫu Sơn · người Dao
hái thủ công lúc lá còn ngậm sương · và chứng nhận OCOP 3★.

Tính ra: 359.000đ ÷ 30 túi ≈ 12.000đ một tối — bằng nửa ly cà phê, cho một nếp
tối thư giãn hơn.

Anh/chị chưa thử bao giờ thì cứ lấy 1 hộp dùng thử ạ. Hợp rồi hãy tính combo
3 tặng 1 (1.015.000đ, freeship).

👉 Nhắn "MẨY GÒM" để em gửi cách pha đúng.
```

---

## 9. 📋 SOP Thao Tác

**SOP-09 — Nhịp sản xuất bài viết hàng tuần (sau khoá học)**

- **Khi nào:** **Sáng thứ Bảy hằng tuần, 60–90'/lần** (1 lần viết đủ nội dung cả tuần).
- **Ai làm:** chủ DN hoặc nhân sự content (sau khi được bàn giao Brand Voice Guideline + Content Bank + bộ 5 prompt này).
- **Input:** bảng 60 ý tưởng (ý chưa dùng) · Brand Voice Guideline · **Sales Message Pack** · **2–3 chất liệu thật mới trong tuần** (chuyện khách, câu hỏi inbox mới, kết quả mới).
- **Các bước:**
	1. **(10')** Chọn **7 nội dung** cho tuần tới theo **nhịp Core: 5 bài FB + 1 video + 1 Zalo broadcast**. Kiểm cơ cấu loại bài + kiểm **mã nguồn**.
	2. **(10')** Ghi nhanh chất liệu thật của tuần vào từng ý. **Câu hỏi khách mới hỏi trong tuần → nạp ngược vào FAQ & Objection Database (N4)**, thành `Q##` mới.
	3. **(25')** Chạy Prompt 4 (batch) cho bài dễ + Prompt 2/3 cho **2 bài cần duyệt sâu** (bài bán mềm, bài phản đối).
	4. **(20')** Duyệt checklist 5 câu + **dòng ranh giới pháp lý** từng bài; sửa ≥30%.
	5. **(10')** Cập nhật Content Bank + Repurpose Sheet (**bản Zalo tuần này**); chuyển trạng thái "sẵn sàng đăng"; xếp vào lịch (SOP-13, Ngày 13).
- **Output:** **7 nội dung/tuần sẵn sàng** (5 bài + 1 video + 1 Zalo) — đúng chỉ tiêu Tuần 1.
- **Tần suất:** tuần/lần. Khi bảng ý tưởng còn **<15 ý chưa dùng** → chạy **SOP-08** (Ngày 08) nạp thêm.
- **Nối tiếp:** SOP-09 xong → **SOP-10** (visual, 30–45') ngay sau đó.

---

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100đ)

| Nhóm | Điểm | Tiêu chí đo được của Ngày 09 |
|---|:---:|---|
| **Đủ tài sản Core** | **30** | Brand Voice Guideline đủ 5 phần + 2 đoạn văn mẫu + **ghi rõ "nâng cấp từ `[GIỌNG]` N5 / KB N4" và dán khối cũ để đối chiếu**: 10đ · Đủ **10 bài** trong Content Bank, đúng cơ cấu **≥4 giáo dục / ≥3 phản đối / ≥2 bán mềm / ≥1 kể chuyện**: 12đ · Repurpose Sheet đủ **3 bài × 4 phiên bản**, trong đó **≥2 bản Zalo broadcast đã gán slot tuần** trong lịch: 8đ |
| **Chất lượng & độ sâu** | **30** | **🔗 TRUY NGUYÊN:** ≥8/10 bài có `Mã nguồn` hợp lệ **(≥80%)**: 8đ · **≥3/10 bài truy về câu nói NGUYÊN VĂN của khách thật (`V#`/`Q##`)**: 6đ · **≥1 bài lấp giai đoạn Journey ⚡**: 3đ · 10/10 bài đủ **Hook + CTA**, ≥8/10 đủ khung phù hợp loại bài: 6đ · Bài phản đối trích **đúng nguyên văn** lời khách + có **phép tính** + **bằng chứng thật**: 4đ · Độ dài 200–450 chữ/bài, xuống dòng thoáng: 3đ |
| **Cá nhân hoá vào DN thật** | **25** | **Cột "Đã sửa gì so với AI" điền ≥2 gạch đầu dòng cho ≥8/10 bài** (bằng chứng của Quy tắc 30%): 10đ · ≥7/10 bài chứa chất liệu thật (tên viết tắt khách, con số thật, chuyện thật): 7đ · **Hook/CTA có truy về Sales Message Pack (N3) — không sáng tác lại thứ đã có**: 5đ · Không còn ví dụ bịa kiểu *"một khách hàng nọ"*: 3đ |
| **Dùng được ngay** | **15** | **Nghiệm thu bằng hành động:** mentor bốc ngẫu nhiên 2 bài → xác nhận *"đăng được ngay, không cần sửa"*: 7đ · Mentor đọc to **1 bản Zalo** → nghe như tin nhắn thật, không như thông cáo: 4đ · Content Bank đủ metadata (loại/pillar/phễu/mã nguồn/trạng thái) + đặt tên file, quyền link đúng quy cách: 4đ |

**Mức:** **≥80 Xuất sắc ⭐** · **60–79 Đạt ✅** · **40–59 Cần sửa 🔧** (sửa trong 24h) · **<40 Làm lại 🔴** (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**

| Lỗi | Trừ |
|---|:---:|
| 🚨 **Có tuyên bố vượt RANH GIỚI PHÁP LÝ** (*chữa mất ngủ · khỏi · đặc trị · thần dược · cam kết 100%*) | **−7đ/bài + bài KHÔNG ĐƯỢC ĐĂNG** |
| Cột `Mã nguồn` bỏ trống ở >2 bài (dưới ngưỡng 80%) | **−8đ** |
| Không có bài nào truy về câu khách nói nguyên văn (`V#`/`Q##`) | **−6đ** — *dấu hiệu content "nghe tây"* |
| Brand Voice **dựng lại từ số 0**, không dùng khối `[GIỌNG]`/KB (nộp bản mâu thuẫn với giọng cũ) | **−6đ** |
| Cột `Đã sửa gì so với AI` bỏ trống hoặc ghi *"không sửa gì"* ở ≥5 bài | **−10đ** — *dấu hiệu không duyệt* |
| 10 bài cùng 1 giọng "AI mặc định": mở bằng *"Bạn có biết…"*, kết bằng *"Hãy liên hệ…"* | **−8đ** |
| Bài **dạy lại thứ khách đã biết** (giảng "mất ngủ là gì" cho tệp Solution Aware) | **−4đ/bài** |
| Bài bán mềm hoá thành bài giảm giá cứng (*"SALE 50% CUỐI TUẦN"*) | **−5đ/bài** |
| **Chỉ có 1 hoặc 0 bản Zalo broadcast** → lịch 14 ngày Ngày 13 thiếu slot | **−5đ** |
| Nộp 30 bài batch nhưng 10 bài Core kém chất lượng | Chấm **trên 10 bài Core**; bonus **không gỡ điểm Core** |

---

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Tuần trước tôi đã làm Brand Voice rồi, sao hôm nay làm lại?**
A: **Không làm lại — nâng cấp.** Khối `[GIỌNG]` (N5) là bản ≤80 từ để dán vào prompt: đủ cho máy, **không đủ cho người**. Hôm nay bạn mở nó thành tài liệu 1 trang để (a) một nhân sự content mới vào đọc là viết được, (b) có mục "5 điều KHÔNG BAO GIỜ" + danh sách từ cấm — thứ khối 80 từ không chứa nổi. Nếu AI hỏi lại bạn *"3 từ mô tả DN của bạn?"* → bạn dán thiếu input, dừng lại và dán khối `[GIỌNG]` vào.

**Q2: Tôi viết dở, không biết sửa 30% của AI thế nào?**
A: Bạn không cần "viết hay" — chỉ cần làm **3 việc cơ học**: (1) thay ví dụ AI bịa bằng **1 chuyện thật bạn kể được ngay**, (2) thêm **1 con số thật**, (3) **đọc to hook** — nếu bạn không nói câu đó ngoài đời, sửa lại theo cách bạn nói. Ba việc này chiếm 80% giá trị của bước duyệt.

**Q3: 10 bài trong 1 tối có nhiều quá không?**
A: Phép tính thật: Brand Voice 20' + mở kho đạn 10' + mỗi bài ~7' (AI viết 1', bạn duyệt 6') × 10 = 70' + repurpose 15' ≈ **115' theo template · 160' nếu lần đầu tự làm**. Quá 2,5 tiếng → nộp **8 bài đúng cơ cấu và đủ mã nguồn** vẫn được chấm (trừ điểm nhóm 1). Đừng thức đêm làm ẩu 10 bài.

**Q4: AI cứ bịa case khách hàng, cấm thế nào?**
A: Prompt 2 và 3 đã có ràng buộc *"thiếu chất liệu → HỎI LẠI TÔI, không bịa"*. Nếu AI vẫn bịa: xoá đoạn ví dụ và ra lệnh *"Viết lại phần Ví dụ, CHỈ dùng chất liệu sau: […]"*. **Tuyệt đối không đăng case bịa.** 🍵 MSX bán bằng **niềm tin vào nguồn gốc** — một case bịa bị phát hiện phá huỷ uy tín với 5.000 khách đã có.

**Q5: Bài của tôi có chữ "chữa mất ngủ", AI tự viết ra, có sao không?**
A: **Có. Xoá ngay.** Đây không phải chuyện văn phong — đây là **ranh giới pháp lý**. Trà thảo mộc **không phải thuốc**. Chỉ được nói **"hỗ trợ thư giãn buổi tối"**. Với người mất ngủ kéo dài, câu trả lời chuẩn của MSX (đã có sẵn ở `O08` trong KB) là: *"MSX không tư vấn sản phẩm như thuốc. Đây là trà thảo mộc buổi tối, vị dịu, hỗ trợ nhịp thư giãn trước khi ngủ. Mất ngủ kéo dài anh/chị nên gặp chuyên gia y tế."* Nói thật kiểu này **mất 1 đơn hôm nay, giữ được thương hiệu 10 năm** — và trong thực tế thường khách quay lại. Rubric trừ **−7đ**, bài **không được đăng**.

**Q6: Khách của tôi đã biết trà thảo mộc rồi, vậy bài giáo dục viết gì?**
A: Chị Hương ở **Mức nhận thức 3 — Solution Aware**: đã biết trà thảo mộc là giải pháp, đang **SO SÁNH các loại**, chưa biết MSX. Nên bài giáo dục **KHÔNG** dạy *"mất ngủ là gì"*, mà đánh vào **SO SÁNH + BẰNG CHỨNG**: vì sao trà vùng cao 1.541m khác trà đồng bằng · OCOP 3★ nghĩa là gì · hái thủ công khác hái máy ra sao · giấc ngủ nông vs giấc ngủ sâu. Bài dạy lại thứ khách đã biết = **−4đ**.

**Q7: 10 ý ⭐ của tôi lệch cơ cấu (7 bài giáo dục, 0 bài phản đối) thì sao?**
A: **Hoán đổi ngay với ý khác trong top 15** của bảng 60 ý (Ngày 08). Cơ cấu quan trọng hơn thứ hạng ý tưởng, vì **3 bài xử lý phản đối là 3 bài kiếm tiền nhất** — chúng gỡ đúng những câu khách đang kẹt (`O1`/`O2`/`O3`). Nếu bảng ý tưởng không có ý phản đối nào → mở thẳng **FAQ & Objection Database (N4)**, lấy 3 câu hỏi được hỏi nhiều nhất, mỗi câu thành 1 bài.

**Q8: Nên viết trên RocketAgent hay ChatGPT/Claude?**
A: Cả hai đều được. **Ưu tiên Track A — AI Marketing Assistant (Ngày 06)**: Brand Voice + ICP + Offer + FAQ đã nằm sẵn trong Knowledge Base → prompt ngắn hơn, ít lỗi hơn, và Tuần 3–4 chatbot/agent sẽ **dùng lại đúng kho này**. Nếu hôm nay bạn viết ở ChatGPT/Claude Projects, cuối tuần nhớ tải Content Bank + Brand Voice Guideline lên Knowledge Base (việc này nằm trong checklist Ngày 14).

**Q9: Đăng bài do AI viết có bị Facebook bóp tương tác không?**
A: Facebook **không phạt "bài do AI viết"** — Facebook phạt **bài KÉM**: câu chữ spam, không ai dừng đọc. Bài qua checklist 5 câu + chất liệu thật + hook lấy từ Sales Message Pack là bài tốt. Thứ **cần tránh**: đăng 30 bài giống hệt nhau lên nhiều group cùng lúc.

**Lỗi thường gặp:**

1. **Dựng lại Brand Voice từ số 0 → mâu thuẫn với giọng cũ.** *Phát hiện:* Guideline mới xưng "chúng tôi" trong khi khối `[GIỌNG]` xưng "em". *Sửa:* chạy lại Prompt 1 với khối `[GIỌNG]` dán đúng vào INPUT.
2. **Bỏ qua kho đạn, để AI sáng tác lại hook.** *Phát hiện:* không bài nào truy về Sales Message Pack; hook nghe "lạ" so với ads đang chạy. *Sửa:* mở lại Ngày 03, gán hook/CTA có sẵn cho từng bài trước khi chạy prompt.
3. **Brand Voice làm qua loa 5 phút → 10 bài ra giọng sách giáo khoa.** *Phát hiện:* đọc 3 bài liên tiếp thấy trơn tuột, không câu nào "gai". *Sửa:* trả lời kỹ 3 câu bổ sung của Prompt 1 — đặc biệt câu *"lần nói thật dù mất đơn"*, đó là **DNA của giọng**.
4. **Mỗi bài 3–4 CTA (like, share, comment, inbox, gọi hotline).** *Phát hiện:* đếm hành động cuối bài >1. *Sửa:* chọn **1 CTA khớp tầng phễu** (TOF: comment/save · MOF: nhận tài liệu · BOF: inbox) — xoá phần còn lại.
5. **Bài xử lý phản đối viết như bài cãi nhau với khách.** *Phát hiện:* thiếu bước "đồng cảm, thừa nhận phần đúng". *Sửa:* thêm 2 câu sau hook: *"Anh/chị hỏi vậy là đúng ạ. Nếu là em, em cũng cẩn thận y như vậy."* rồi mới bóc tách.
6. **Batch 20 bài TRƯỚC khi duyệt xong 10 bài Core.** *Phát hiện:* 30 bài nộp cùng chất lượng thấp đều nhau. *Sửa:* xoá batch, duyệt xong 10 Core rồi chạy lại Prompt 4 — chất lượng batch **phụ thuộc vào bài mẫu đã duyệt nằm trong hội thoại**.
7. **Quên đánh dấu 2 bản Zalo là slot thật.** *Phát hiện:* Repurpose Sheet có bản Zalo nhưng cột `Trạng thái sử dụng` bỏ trống. *Sửa:* gán ngay *"Zalo broadcast — Tuần 1 / Tuần 2"* — Ngày 13 sẽ cần đúng 2 dòng này.

---

## 12. 🔁 Kết Nối

- **Ngày trước:** [[Ngày 08 — Chiến Lược Nội Dung & Content Pillar]] (10 ý ⭐ + 60 ý tưởng có mã nguồn = nguyên liệu đầu vào hôm nay) · **Ngày sau:** [[Ngày 10 — AI Design & Visual Asset]]
- **Trọng tài số liệu & luật:** [[_Chuẩn Đồng Bộ Tuần 2]] · **Về MOC:** [[_MOC 28 Day AIOS]]

**Tài sản Tuần 1 hôm nay đã dùng:** Brand Voice KB (N4) + khối `[GIỌNG]` (N5) → **Guideline 5 phần** · Sales Message Pack (N3) → **hook/headline/CTA** · FAQ & Objection Database (N4) → **3 bài phản đối** · PDFO + 5 câu nguyên văn khách (N2) → **mã nguồn** · Core Offer (N3) → **2 bài bán mềm** · 10 ý ⭐ (N8) → **10 bài** · AI Marketing Assistant (N6) → **nơi chạy prompt**.

**Tài sản hôm nay được dùng lại ở:**

| Tài sản Ngày 09 | Đi đâu |
|---|---|
| **10 bài Core** | 6 bài được gắn visual ở [[Ngày 10 — AI Design & Visual Asset]] (4 bài còn lại dùng **ảnh thật**) · **cả 10 bài lên lịch đăng** ở [[Ngày 13 — Phân Phối Nội Dung & Content Automation]] = 5 bài/tuần × 2 tuần |
| **≥2 bản Zalo broadcast** (Repurpose Sheet) | **2 slot THẬT** trong lịch 14 ngày Ngày 13 — 1 broadcast/tuần. *Không có 2 bản này, lịch thiếu slot.* |
| **Script video 45s** (Repurpose Sheet) | Nguyên liệu trực tiếp cho [[Ngày 11 — AI Video & Audio Factory]] (10 script · 2 video) |
| **3 quote/bài** (Repurpose Sheet) | Chữ trên visual ở [[Ngày 10 — AI Design & Visual Asset]] |
| **Brand Voice Guideline** | Dùng cho **MỌI** tài sản còn lại của khoá: landing page (Ngày 12) · chatbot tư vấn + kịch bản sale (Tuần 3) · agent chăm sóc (Tuần 4) |
| **3 bài xử lý phản đối + 2 bài bán mềm** | Chất liệu cho kịch bản tư vấn inbox ở **Tuần 3 (Ngày 16–17)** |
| **Câu hỏi khách mới phát sinh khi viết** | Nạp ngược vào **FAQ & Objection Database (N4)** → Tuần 2 làm dày Tuần 1, không bỏ rơi nó |
