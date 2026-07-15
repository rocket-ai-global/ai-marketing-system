---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 2
day: 12
core-output: "Lead Magnet PDF 4–8 trang (có CTA trang cuối) + Landing Page Copy 9 khối CÓ CỘT MÃ NGUỒN (lắp ráp từ tài sản Tuần 1) + Form thu lead 6 trường CHẠY THẬT (mentor điền thử → lead hiện trong Sheet, có trường phân loại dạng chọn) + Bộ 3 tin nhắn (Thank You / gửi quà / follow-up 24h do người thật gửi) + Lead Flow Map 6 trạm có tên người thật + dòng Data Security"
---

# Ngày 12 — Landing Page & Lead Magnet

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** Copy landing lưu `04. Resources/Playbooks/`; **trang landing host trên Vercel** (hoặc Google Form nếu bí) → **form ghi vào Google Sheet** → **Hermes theo dõi Sheet → tự nhắn Zalo trao quà** (kiến trúc đúng: web ở Vercel, engine ở Hermes — xem [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]]); lead đổ về `People/` (mỗi lead 1 file, ghi rõ PK) — **và chịu Data Security Rule tầng Restricted (hạn chế) của Ngày 04**.

> 🎁 **Nâng cấp Core hôm nay — trao quà TỰ ĐỘNG (thay "3 tin nhắn gửi tay"):** khách điền form → Hermes nhắn quà qua Zalo trong <1 phút, kể cả 2h sáng. Bộ 3 tin nhắn giữ lại làm **fallback** khi chưa dựng tự động. Toàn bộ 5 bước ở [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]].

> Hôm nay doanh nghiệp của bạn có **ĐIỂM CHUYỂN ĐỔI (conversion point — nơi người xem biến thành cái tên + số điện thoại)**: một tài sản miễn phí đủ hấp dẫn để khách đổi số điện thoại + một trang/form thu lead **HOẠT ĐỘNG THẬT**. Nội dung của Ngày 09–11 từ nay có nơi để "đổ về".

> 🔴 **Câu quan trọng nhất của cả ngày hôm nay:**
> **Form xấu mà CHẠY THẬT ăn đứt landing page đẹp còn nằm trên giấy.**
> Và vì thế **cách nghiệm thu cũng phải là hành động, không phải file:** *mentor sẽ **BẤM** link form của bạn, **ĐIỀN THỬ**, và lead phải **HIỆN** trong Sheet.* Không hiện = không có điểm chuyển đổi = Tuần 3 (CRM/sale) không có gì để chạy.

---

## 📥 Nguyên liệu Tuần 1 dùng hôm nay

> 🔗 **LUẬT TRUY NGUYÊN (mọi thứ phải trỏ ngược về một dòng dữ liệu thật) — hôm nay áp thẳng vào landing page.**
> **Landing page KHÔNG phải là thứ bạn viết mới hôm nay. Nó là BẢN LẮP RÁP từ tài sản Tuần 1.**
> Nếu bạn đang ngồi "nghĩ xem viết gì" → bạn đang làm sai. Bạn phải đang **đi lấy**: lấy câu khách nói ở N2, lấy câu hỏi thật ở N4, lấy khối offer ở N3. AI chỉ **xếp lại và mài chữ**. Câu nào trong landing không truy về được nguồn nào ở Tuần 1 → **đó là câu AI bịa → xoá.**

| Tài sản Tuần 1 | Ngày | Hôm nay dùng vào đâu | Mã nguồn |
|---|:---:|---|:---:|
| **5 câu nguyên văn khách thật** (Avatar + PDFO) | N2 | **Khối 3 — Vấn đề** (bắt buộc: viết bằng LỜI KHÁCH, không phải lời AI đoán) · hook đầu trang | `V1…V5` |
| **Avatar + Mức nhận thức** (chị Hương — Solution Aware) | N2 | Quyết định **giọng & trọng tâm toàn trang**: đánh SO SÁNH + BẰNG CHỨNG, không dạy lại "mất ngủ là gì" | `AV` |
| **PDFO Map** (Pain/Desire/Fear/Objection) | N2 | Khối 3 (Vấn đề) · Khối 4 (Lời hứa) · Khối 6 (Lợi ích/khác biệt) | `P# D# F# O#` |
| **Core Offer 7 khối** | N3 | **CTA trang cuối lead magnet + khối 8 (CTA landing)** — CTA không được sáng tác mới | `OF1…OF7` |
| **Sales Message Pack** (hook/headline/CTA) | N3 | Khối 1–2 (Headline/Subheadline) — lấy kho có sẵn, KHÔNG viết lại từ đầu | `MSG` |
| **FAQ & Objection Database ≥30 cặp** | N4 | **Khối 9 — FAQ: LẤY THẲNG 4–5 cặp có sẵn. CẤM viết FAQ mới.** | `Q##` |
| **Product Knowledge** (thành phần, quy trình, vùng nguyên liệu) | N4 | **Khối 5 — Nội dung nhận được** + ruột lead magnet (chi tiết chuyên môn thật) | `PK` |
| **Data Security Rule** | N4 | **Quản trị dữ liệu lead** (tên/SĐT = tầng **Restricted**) — 1 dòng bắt buộc trong Lead Flow Map | `DS` |
| **Brand Guideline T8.0** (N8) → Brand Voice Guideline (N9) | N8/N9 | Giọng + cá tính của toàn bộ copy + 3 tin nhắn — đúng T8.0 | `GIỌNG` |
| **Prompt Library nhóm M** — **M09 "viết landing page theo StoryBrand"** · **M10 "lead magnet"** | N5 | 5 prompt hôm nay là **bản cá nhân hoá của M09 + M10**, không phải prompt mới | `M09/M10` |
| **AI Marketing Assistant** (đã nạp KB) | N6 | Chạy prompt **trong Assistant này** — không dán lại ICP/Offer vào ChatGPT trắng | — |

> ✅ **Kiểm tra 30 giây trước khi bắt đầu:** mở được 5 file trên? Nếu thiếu FAQ Database (N4) hoặc 5 câu nguyên văn (N2) → **đi vá 20 phút rồi hãy quay lại**. Không có nguyên liệu thì hôm nay bạn chỉ sản xuất được văn mẫu.

---

## 1. 🎯 Mục Tiêu Ngày Học

Cuối ngày, học viên **CÓ trong tay** (tài sản, không phải hiểu biết):

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **1 Lead Magnet (mồi thu khách — tài sản miễn phí đổi lấy thông tin liên hệ)** hoàn chỉnh dạng PDF 4–8 trang, làm bằng AI + Canva, **trang cuối có CTA về offer thật (`OF#`)**.
- ✅ **Landing Page Copy (nội dung trang đích) đủ 9 khối** — **mỗi khối có cột `Mã nguồn`** trỏ về tài sản Tuần 1. Kể cả chưa dựng trang, copy này đã là tài sản dùng được cho mọi công cụ.
- ✅ **Lead Capture Form (form thu thông tin khách) HOẠT ĐỘNG THẬT** — 6 trường, **bắt buộc có trường phân loại dạng danh sách chọn**; đã test: lead điền vào là rơi xuống Google Sheet.
- ✅ **Bộ 3 tin nhắn:** Thank You Message (lời cảm ơn ngay sau khi gửi form) + tin nhắn gửi quà + **tin follow-up 24h (do NGƯỜI THẬT gửi/duyệt — không auto blast)**.
- ✅ **Lead Flow Map (sơ đồ luồng lead) 6 trạm, 1 trang** — có **TÊN NGƯỜI THẬT** ở mỗi trạm + **1 dòng Data Security** (ai được xem dữ liệu lead, lưu ở đâu).

**Bonus Output (nâng cao — KHÔNG bao giờ là điều kiện của Core):**
- 🎁 Landing page **DỰNG HOÀN CHỈNH** trên Ladipage / Canva Website / RocketAgent — đẹp, có ảnh vùng nguyên liệu, chạy được chiến dịch.
- 🎁 Zalo OA / email **xác nhận + gửi quà tự động** (🟢 AUTO — không cần người trực).
- 🎁 Lead magnet **thứ hai** dạng khác (video hướng dẫn 5' / buổi audit miễn phí).

> **Nguyên tắc bất di bất dịch của ngày hôm nay:**
> **Form xấu mà CHẠY THẬT ăn đứt landing page đẹp còn nằm trên giấy.**
> Core hôm nay ưu tiên **luồng thông suốt end-to-end (từ đầu đến cuối)**; cái đẹp là Bonus. Thứ tự làm đúng: **Form trước (30') → PDF sau (40')**. Ai làm ngược sẽ hết giờ ở trang bìa PDF và không có gì để nghiệm thu.

---

## 2. 📚 Kiến Thức Trọng Tâm (25')

### Khối 1 — Điểm chuyển đổi: mảnh ghép đang thiếu (4')

- **Ý chính:** Tuần này đã có **nội dung** (N09 — 10 bài), **hình** (N10 — 6 visual), **video** (N11 — 2 video). Nhưng người xem **đến rồi ĐI**, không để lại gì. Landing page + lead magnet = cái **phễu hứng**: biến người xem ẩn danh thành **một cái tên + một số điện thoại** mà đội sale gọi được.
- **Ví dụ 🍵 MSX Group:** MSX đã phục vụ **5.000+ khách** và fanpage có người theo dõi — nhưng chị Hương (40t, nhân viên văn phòng Hà Nội, ~20tr/tháng) đang **lướt qua bài lúc 21h–23h, gật gù, rồi ngủ**. MSX không biết chị là ai. Một **"Bảng so sánh trung thực: trà thảo mộc chuẩn vùng nguyên liệu vs trà phổ thông — tự chấm 10 tiêu chí"** đổi lấy SĐT: **ai tải về là tự giơ tay** — "tôi chính là người đang so sánh, tôi chính là khách của anh."
- **Chốt:** Marketing không có điểm chuyển đổi = **xây chợ đông người nhưng không có quầy thu ngân**.
- Nối vào Tuần 1: điểm nghẽn ② của MSX là *"lead phụ thuộc tiền ads (8tr/tháng, không tăng)"*. Lead magnet + form là **vòi lead organic (tự nhiên, không trả tiền quảng cáo)** — đây chính là thứ kéo **85 → 130 lead/tháng** mà không tăng đồng ads nào.

### Khối 2 — Lead Magnet: cho đúng thứ khách THÈM (6')

**4 tiêu chí của một lead magnet tốt (đo được, chấm 1–5):**

| # | Tiêu chí | Câu hỏi kiểm chứng |
|:-:|---|---|
| **A** | Giải quyết **1 vấn đề CỤ THỂ và CẤP** | Không phải "cẩm nang toàn tập". Một vấn đề, một lời hứa. |
| **B** | **Dùng được trong ≤15 phút** | Khách mở ra là làm được ngay, không phải để dành "khi nào rảnh". |
| **C** | **Dẫn thẳng đến offer trả phí** | Người CẦN quà này chính là người CẦN offer. Nếu không → quà sai. |
| **D** | **Thể hiện chuyên môn thật** | Đọc xong nghĩ: *"người này rành thật"* — có chi tiết chỉ người trong nghề mới viết được. |

**7 dạng lead magnet:** ebook/cẩm nang · **checklist** · mini course (khoá học ngắn) · template · file mẫu · video hướng dẫn · **audit (buổi kiểm tra/đánh giá) miễn phí**.

**Luật chọn dạng — B2C vs B2B (đây là chỗ RocketAI mở ra):**

| | 🍵 **MSX (B2C — sản phẩm)** | 🚀 **RocketAI (B2B — dịch vụ)** |
|---|---|---|
| **Dạng thắng** | **Cẩm nang / checklist PDF** — khách tự đọc, tự chấm, tự nhận ra vấn đề | **Buổi demo / audit 30 phút** — xem hệ thống chạy thật trên 1 spa có sẵn |
| **Vì sao** | Đơn giá 359k, quyết định nhanh, khách **không muốn nói chuyện với ai** ở giai đoạn này | Đơn giá cao, chu kỳ chốt dài; khách B2B **cần thấy tận mắt** mới tin; 1 buổi demo lọc lead sạch hơn 100 lượt tải PDF |
| **Landing bán gì** | Bán **cẩm nang** (không bán hộp trà) | Bán **buổi demo 30'** (KHÔNG bán gói 25tr — sai tầng phễu) |
| **Form thêm trường** | "Bạn đang quan tâm điều gì nhất?" | **"Quy mô nhân sự / doanh thu tháng"** — lọc lead đủ ngân sách trước khi tốn 30' của founder |

**🍵 Ví dụ đạt / không đạt (MSX):**
- ❌ *"Ebook 60 trang: Toàn tập về thảo dược Việt Nam"* → chung chung, không ai đọc hết, không dẫn về hộp trà nào. Rớt tiêu chí A và C.
- ✅ *"**Bảng so sánh trung thực: trà thảo mộc chuẩn vùng nguyên liệu vs trà phổ thông — tự chấm 10 tiêu chí**"* → **thắng**, vì:
  - **A** — đánh thẳng vào việc chị Hương đang làm **ngay lúc này**: SO SÁNH.
  - **B** — tự chấm 10 tiêu chí trong ~10 phút.
  - **C** — chấm xong thấy trà đang uống rớt 6/10 → muốn thứ đạt 10/10 → **CTA hộp đơn 359.000đ / Combo mua 3 tặng 1 — 1.015.000đ**.
  - **D** — chỉ MSX mới viết nổi tiêu chí *"nguyên liệu hái ở độ cao bao nhiêu"* (Mẫu Sơn **800–1.541m**), *"hái tay hay hái máy"* (người **Dao/Tày/Nùng** hái thủ công).
  - 🎯 **Nó đánh thẳng `O1`** — objection *"sao đắt hơn trà ngoài siêu thị"* (`V3`) — và **đúng khớp Mức nhận thức 3 (Solution Aware — đã biết trà thảo mộc là giải pháp, đang so sánh, chưa biết MSX)**.
- ✅ *(phương án 2, mềm hơn)* *"**Cẩm nang Trà Tối — 7 ngày xây thói quen thư giãn trước khi ngủ**"* → tốt cho tệp chưa so sánh, nhưng **yếu hơn với chị Hương** vì chị không cần được dạy thói quen — chị cần được **thuyết phục chọn ai**.

> 🎓 **Bài học chọn quà:** lead magnet phải khớp **MỨC NHẬN THỨC** của avatar. Solution Aware → cho **công cụ SO SÁNH**, đừng cho **bài giảng nhập môn**.

### Khối 3 — Landing page 9 khối = BẢN LẮP RÁP TỪ TUẦN 1 (8') 🔴 *trọng tâm*

> **Nói thẳng ở lớp:** *"Anh chị không viết landing page hôm nay. Anh chị **LẮP** nó. Mỗi khối có một cái ngăn kéo ở Tuần 1 — mở đúng ngăn, lấy đồ ra, xếp vào."*

| # | Khối | Nhiệm vụ | **Mã nguồn (BẮT BUỘC)** | 🍵 Một dòng MSX |
|:-:|---|---|:---:|---|
| 1 | **Headline** (tiêu đề chính) | Nêu **kết quả + cho ai**, ≤14 từ | `MSG` (N3) + `AV` (N2) | *"Tự chấm 10 tiêu chí: trà bạn đang uống có thật là trà vùng nguyên liệu?"* |
| 2 | **Subheadline** (tiêu đề phụ) | Làm rõ **món quà + uy tín** | `MSG` (N3) + `PK` (N4) | *"Bảng so sánh trung thực từ đội hái trà Mẫu Sơn — OCOP 3★, 5.000+ khách đã dùng"* |
| 3 | **Vấn đề** | **Gọi tên nỗi đau BẰNG LỜI KHÁCH — nguyên văn** | 🔴 **`V#` (N2) — CẤM lời AI đoán** | *"Sao đắt hơn trà ngoài siêu thị thế em?"* (`V3`) · *"Chị ngủ kém lắm, uống bao lâu thì thấy đỡ?"* (`V2`) |
| 4 | **Lời hứa kết quả** | Dùng quà xong khách **được gì** | `D#` (N2) | *"Sau 10 phút, bạn biết chính xác mình đang trả tiền cho lá trà hay cho bao bì."* |
| 5 | **Nội dung nhận được** | 5–7 gạch **cụ thể** bên trong | 🔴 **`PK` — Product Knowledge (N4)** | *"10 tiêu chí chấm · cách đọc nhãn · bảng độ cao vùng nguyên liệu · 3 dấu hiệu trà pha trộn"* |
| 6 | **Lợi ích / khác biệt** | Khác gì thứ trôi nổi trên mạng | `O#` + `F#` (N2) | *"Viết bởi người đi hái, không phải người dịch blog."* |
| 7 | **Bằng chứng** | 🔴 **DỮ LIỆU THẬT — không placeholder, không bịa** | `PK` (N4) + Snapshot (N1) | **OCOP 3★** · **5.000+ khách** · **ảnh vùng nguyên liệu Mẫu Sơn 800–1.541m** · ảnh người Dao/Tày/Nùng hái tay |
| 8 | **CTA + Form** | **1 hành động duy nhất** | 🔴 **`OF#` — Core Offer 7 khối (N3)** | *"Điền thông tin — nhận bảng so sánh qua Zalo trong 5 phút"* |
| 9 | **FAQ** | Gỡ 4–5 nghi ngờ cuối | 🔴 **`Q##` — LẤY THẲNG từ FAQ & Objection Database (N4, ≥30 cặp). CẤM VIẾT MỚI.** | *"Trà này có chất bảo quản không?"* · *"Phụ nữ có thai dùng được không?"* · *"Phí ship bao nhiêu?"* |

**Cách giảng (nói đúng câu này):**
> *"9 khối này chính là **kịch bản tư vấn được viết ra giấy** — khách tự đọc và **tự thuyết phục chính mình**. Thứ tự khối = thứ tự tâm lý: **chú ý → đúng bệnh → muốn → tin → hành động**.
> Và đây là điểm khác biệt của lớp này với mọi khoá copywriting ngoài kia: **chúng ta không sáng tác. Chúng ta LẮP RÁP.** Khối 3 là mồm khách. Khối 9 là mồm khách. Khối 7 là hồ sơ thật. Khối 5 là kho hàng thật. Khối 8 là offer thật.
> **Landing page nào không lắp được từ Tuần 1 nghĩa là Tuần 1 của bạn rỗng — chứ không phải bạn viết chưa hay.**"*

**🔍 Test truy nguyên tại lớp (30 giây, làm thật):** chiếu 1 bản copy AI vừa trả → chỉ vào từng khối → hỏi lớp: *"Câu này lấy từ đâu?"* Câu nào không ai chỉ ra được nguồn → **bôi đỏ → xoá.** (Ngưỡng chấm: **≥80% khối có mã nguồn hợp lệ**; **khối 3 và khối 9 bắt buộc 100%** truy về `V#`/`Q##`.)

### Khối 4 — Form: hỏi ít thôi, hỏi thứ DÙNG ĐƯỢC (4')

**6 trường chuẩn:**

| # | Trường | Bắt buộc? | Ghi chú |
|:-:|---|:---:|---|
| 1 | **Họ tên** | ✅ | Để tin nhắn có tên người — không "Chào bạn". |
| 2 | **Số điện thoại** | ✅ | Kênh gọi/Zalo. Đây là **thứ ta thật sự đến để lấy**. |
| 3 | **Zalo có phải số này không?** | ✅ | 1 câu Có/Không — tiết kiệm 1 vòng hỏi lại. |
| 4 | 🔴 **Trường PHÂN LOẠI (danh sách chọn)** | ✅ **BẮT BUỘC** | **Đây là câu đắt nhất của cả form.** Xem dưới. |
| 5 | **Email** | ⬜ tuỳ ngành | B2C VN: bỏ được. B2B: giữ. |
| 6 | **Ghi chú** | ⬜ | Tự luận, không bắt buộc. |

**Quy tắc sắt:** mỗi trường thêm vào = **rớt ~10–20% người điền**. Đừng hỏi ngày sinh, địa chỉ nhà, nghề nghiệp — chưa dùng đến.

🔴 **TRƯỜNG PHÂN LOẠI = MẦM CRM CỦA TUẦN 3.** Đây không phải một câu hỏi cho vui. **Chính 5 lựa chọn này là câu phân loại lead** mà Tuần 3 (CRM + chatbot + kịch bản tư vấn) sẽ dùng để **định tuyến từng lead vào đúng luồng chăm sóc**. Chọn sai 5 lựa chọn hôm nay = Tuần 3 phải làm lại từ đầu.

**🍵 Trường phân loại MSX (chốt):**
> **"Bạn đang quan tâm điều gì nhất?"**
> ① Khó ngủ, muốn thư giãn buổi tối
> ② Tìm quà biếu bố mẹ
> ③ Muốn dùng thử trước
> ④ Đang so sánh với trà khác
> ⑤ Hỏi mua sỉ – đại lý

Nhìn kỹ: **mỗi lựa chọn dẫn thẳng đến một hành động bán khác nhau** — ① → hộp đơn 359k · ② → combo quà tặng · ③ → hộp đơn 359k + tin trấn an (`V4`) · ④ → gửi bảng so sánh + bằng chứng (`O1`) · ⑤ → chuyển thẳng cho chủ DN, không để tư vấn viên xử. **Lead tự phân loại chính mình trước khi sale chạm vào.**

**🚀 RocketAI (B2B):** thêm trường **"Quy mô nhân sự / doanh thu tháng"** → lọc lead đủ ngân sách **trước khi** đốt 30 phút của founder vào một buổi demo vô ích.

### Khối 5 — Luồng sau khi điền form: 5 PHÚT VÀNG (4')

**Chuỗi chuẩn — 6 trạm:**

```
① Người xem (bài/video có CTA)
     ↓
② Điền form  ── 6 trường, có trường phân loại
     ↓
③ Thank You Message (hiện ngay) ── xác nhận + hẹn rõ: nhận quà qua kênh nào, trong bao lâu
     ↓
④ GỬI QUÀ trong ≤5 PHÚT ── Zalo/email. Tự động thì tức thì; thủ công thì PHẢI có người trực.
     ↓
⑤ Lead rơi vào Sheet/CRM ── kèm Nguồn + Phân loại + Trạng thái + Người phụ trách
     ↓
⑥ NGƯỜI THẬT nhắn tin giá trị trong ≤24h ── KHÔNG chào bán ngay
```

**Số phải nhớ:** lead được chạm trong **5 phút đầu** chuyển đổi cao **gấp nhiều lần** lead để nguội 24h. MSX hiện phản hồi inbox mất **~3 giờ** (điểm nghẽn ① của N1) — mục tiêu 28 ngày là **<15 phút**. Luồng hôm nay chính là thứ kéo con số đó xuống.

> Tuần 3 sẽ **tự động hoá** luồng này. Hôm nay ít nhất phải **RÕ: ai làm gì, trong bao lâu** — đó chính là Lead Flow Map.

### Khối 6 — 🤖 LUẬT TỰ ĐỘNG HOÁ: cái gì máy làm, cái gì NGƯỜI phải làm (4')

> **Tự động hoá VIỆC. KHÔNG tự động hoá NIỀM TIN.**

| Tầng | Ở Ngày 12 gồm những gì |
|---|---|
| 🟢 **AUTO** — máy làm 100% | **Form → đẩy lead vào Sheet** (tức thì) · **Gửi lead magnet tự động** (Zalo OA / email) · **Thank-you message** hiện sau khi gửi form · nhắc việc trực lead (Google Calendar lặp) |
| 🟡 **ASSISTED** — AI làm, **người duyệt ≥30%** | **Viết copy 9 khối** (AI xếp — người kiểm mã nguồn) · **Viết ruột lead magnet** (AI viết — người nhét chuyên môn thật vào) · soạn nháp 3 tin nhắn |
| 🔴 **NGƯỜI** — **CẤM tự động hoá** | 🔴 **Tin nhắn 24h phải do NGƯỜI THẬT gửi hoặc duyệt trước khi gửi — KHÔNG auto blast (bắn hàng loạt tự động)** · **Bằng chứng khối 7** (ảnh thật, con số thật, feedback khách thật — không AI bịa) · **xin & đăng feedback khách** · quyết định đổi offer/giá |

**Vì sao vạch đúng ở chỗ này:** MSX bán bằng **niềm tin vào nguồn gốc**. Một tin nhắn auto-blast sai tên, sai ngữ cảnh ("Chào bạn, bên em đang có chương trình…") gửi cho người vừa hỏi *"mua tặng mẹ thì nên lấy trà hay viên em nhỉ"* (`V5`) — **phá huỷ đúng thứ ta vừa xây**. Gửi quà thì máy gửi được. **Hỏi thăm thì người phải hỏi.**

### Khối 7 — 🔒 Data Security: lead là DỮ LIỆU NHẠY CẢM (2')

Áp thẳng **Data Security Rule (N4)**: **tên + số điện thoại khách = tầng Restricted (hạn chế)**.

| Câu hỏi | Trả lời phải ghi vào Lead Flow Map |
|---|---|
| **Lưu ở đâu?** | 1 Google Sheet duy nhất, chủ DN là **Owner** |
| **Ai được xem?** | Chỉ **người trực lead có tên** + chủ DN. Chia sẻ **theo email cụ thể**, KHÔNG bật "ai có link đều xem được" |
| **Ai KHÔNG được?** | Cộng tác viên content, freelancer thiết kế, người chạy ads thuê |
| **Cấm tuyệt đối** | 🔴 **Không chụp màn hình Sheet có SĐT đăng lên group/lớp/fanpage để khoe.** Nộp bài cho mentor: **che 4 số cuối** (`09xx xxx 123`). Không đưa SĐT khách vào prompt AI công cộng. |

> Nộp bài hôm nay **bắt buộc che SĐT** trong ảnh chụp Sheet. Ai đăng SĐT khách thật lên thread cohort → **trừ điểm và gỡ ngay**.

### Khối 8 — ⚖️ RANH GIỚI PHÁP LÝ trên landing page (2')

Landing page là nơi **dễ vi phạm nhất** vì áp lực chuyển đổi.

| 🔴 **CẤM tuyệt đối** | ✅ **Được nói** |
|---|---|
| "chữa mất ngủ" · "khỏi" · "đặc trị" · "thần dược" | **"hỗ trợ thư giãn buổi tối"** |
| "cam kết 100%" · "hiệu quả sau 3 ngày" | "5.000+ khách đã dùng" (con số thật) |
| 🔴 **Khan hiếm giả**: "chỉ còn 5 suất" · "giảm giá hôm nay thôi" (trong khi không có gì hết) | **Lý do mua ngay phải THẬT:** freeship đơn **≥500.000đ** · số lượng **lô hàng thật** còn lại · **lịch giao hàng thật** (Viettel Post) |
| Bỏ qua nhóm cần thận trọng | Phụ nữ có thai/cho con bú/trẻ em/bệnh nền → **khuyên tham khảo bác sĩ** |

**Chấm:** **1 tuyên bố vượt ranh giới = −7đ và KHÔNG được đăng.** Landing page có chữ "chữa mất ngủ" không phải là bài chưa hay — đó là **rủi ro pháp lý cho doanh nghiệp thật của bạn**.

> **Thích ứng ngành khác:** **Nha khoa** — lead magnet mạnh: *"Bảng giá & lộ trình niềng minh bạch"* / *"Checklist chọn nha khoa an toàn"*; form thêm trường "tình trạng răng"; ranh giới: cấm "cam kết đều răng 100%". **Giáo dục** — *"Bài test trình độ 15 phút + lộ trình gợi ý"*; form thêm lớp/tuổi của con; cấm "cam kết đỗ". **Gym/coaching** — *"Bảng tính TDEE + thực đơn 7 ngày mẫu"*; form thêm mục tiêu (giảm cân/tăng cơ); cấm "giảm 10kg trong 1 tháng". **Cấu trúc 9 khối + luật truy nguyên + luồng 5 phút vàng + form có trường phân loại: GIỮ NGUYÊN cho mọi ngành.**

---

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|:---:|---|---|
| **10'** | Warm-up + chữa bài Ngày 11 | Chiếu 2 video tốt của học viên (phát 15s hook mỗi video) + 1 lỗi phổ biến (thường: hook chậm, 3 giây đầu chưa có gì). Dẫn chuyển: *"Video kéo người ĐẾN — hôm nay ta xây cái HỨNG họ lại. Không có nó, 2 video của anh chị chỉ là giải trí miễn phí cho người lạ."* |
| **25'** | Giảng kiến thức trọng tâm | 8 khối phần 2. **Trọng tâm: Khối 2 (4 tiêu chí lead magnet) + Khối 3 (9 khối = bản lắp ráp, có mã nguồn).** Bài tập miệng 2': mỗi học viên nói to 1 ý tưởng lead magnet → lớp chấm nhanh theo 4 tiêu chí A/B/C/D. |
| **30'** | 🍵 **Demo live trên MSX Group** | Theo kịch bản phần 4 (6 bước): chọn lead magnet & chấm 4 tiêu chí trước lớp → AI viết ruột → Canva đóng gói → AI **LẮP** copy 9 khối có mã nguồn → **dựng Google Form + TEST LUỒNG THẬT** → vẽ Lead Flow Map. |
| **15'** | Học viên làm tại chỗ + Q&A | Học viên chốt ý tưởng lead magnet của mình (Prompt 1) + **tạo khung Google Form ngay tại lớp** (đừng để về nhà mới mở form). Trainer duyệt nhanh 3–4 ý tưởng theo 4 tiêu chí và **soi trường phân loại** của từng người. |
| **10'** | Giao bài tập + nghiệm thu | Chiếu phần 6 + rubric. **Nhấn nguyên văn:** *"Hôm nay tôi không đọc bài nộp của anh chị. Tôi **BẤM** link form của anh chị, tôi **ĐIỀN THỬ**, và **lead của tôi phải HIỆN trong Sheet**. Không hiện = 0 điểm phần đó, không có tranh luận."* |

---

## 4. 🎬 Kịch Bản Demo (🍵 MSX Group — 30')

> Chạy trên vault demo `ai-marketing-system-msx-demo/` đã điền sẵn Tuần 1. **Mở sẵn 4 tab trước khi demo:** FAQ & Objection Database (N4) · 5 câu nguyên văn khách (N2) · Core Offer 7 khối (N3) · Product Knowledge (N4). — *Chính hành động mở 4 tab này đã là bài giảng: hôm nay ta đi LẤY, không đi NGHĨ.*

**Bước 1 (4') — Chọn lead magnet bằng AI + chấm 4 tiêu chí TRƯỚC LỚP.**
- **Làm gì:** Chạy **Prompt 1** trong AI Marketing Assistant (N6) → AI đề xuất 5 ý từ **8 ý lead magnet trong 60 ý tưởng của Ngày 08** → **chấm live trên bảng T12.1 trước mặt cả lớp**.
- **Đối đầu 2 ứng viên (làm thật, đừng chọn sẵn):**

| Ý tưởng | A (cụ thể&cấp) | B (≤15') | C (dẫn offer) | D (chuyên môn) | Tổng |
|---|:---:|:---:|:---:|:---:|:---:|
| *"Cẩm nang Trà Tối — 7 ngày xây thói quen thư giãn trước khi ngủ"* | 4 | 3 | 3 | 4 | **14** |
| 🏆 *"**Bảng so sánh trung thực: trà thảo mộc chuẩn vùng nguyên liệu vs trà phổ thông — tự chấm 10 tiêu chí**"* | 5 | 5 | 5 | 5 | **20** |

- **Kết quả + nói rõ VÌ SAO trước lớp:** chọn **Bảng so sánh**. Vì avatar là chị Hương — **Mức nhận thức 3, Solution Aware, đang SO SÁNH**. Chị không cần học cách thư giãn; chị cần **một cái thước** để biết chọn ai. Bảng so sánh **đánh thẳng `O1`** (*"sao đắt hơn trà ngoài siêu thị thế em"* — `V3`). Cẩm nang Trà Tối hay, nhưng **đúng bài sai người** → cất vào Bonus/lead magnet #2.
- 🚀 **Đối chiếu B2B (30 giây):** RocketAI ở bước này **không chọn PDF**. Chọn **buổi demo 30 phút xem hệ thống chạy thật trên 1 spa**. Chủ DN B2B không đọc PDF — họ muốn **thấy tận mắt**.

**Bước 2 (6') — AI viết ruột lead magnet, Canva đóng gói.**
- **Làm gì:** Chạy **Prompt 2** → AI trả nội dung **6 trang**: bìa · trang mở · **bảng 10 tiêu chí tự chấm** · cách đọc nhãn · 3 dấu hiệu trà pha trộn · trang cuối CTA.
- **Duyệt live — 🟡 ASSISTED nghĩa là NGƯỜI PHẢI CHẠM VÀO:** trainer mở **Product Knowledge (N4)** và nhét vào **3 chi tiết chỉ MSX viết nổi**:
  - *Tiêu chí #3: "Nguyên liệu hái ở độ cao bao nhiêu?"* — Mẫu Sơn **800–1.541m**, chênh lệch nhiệt ngày/đêm là thứ làm nên vị.
  - *Tiêu chí #6: "Hái tay hay hái máy?"* — người **Dao/Tày/Nùng** hái thủ công, chọn từng búp.
  - *Tiêu chí #9: "Có chứng nhận nào không?"* — **OCOP 3★**.
  - → **Đây là 3 câu AI KHÔNG BAO GIỜ tự nghĩ ra.** Đây là lý do lead magnet của bạn khác lead magnet của mọi người.
- **Canva:** template "checklist ebook" → dán nội dung → màu/font theo **Visual Brand Kit (Ngày 10)** → xuất PDF `MSX-leadmagnet-bangsosanh10tieuchi-v1.pdf`.
- 🔴 **Trang cuối (đọc to trước lớp):**
  > *"Chấm dưới 7/10 điểm? Thứ bạn đang uống mỗi tối có thể chỉ là lá — không phải trà vùng nguyên liệu.
  > **Trà Mẩy Gòm An Giấc — 359.000đ/hộp** · **Combo mua 3 tặng 1 — 1.015.000đ** (freeship đơn từ 500.000đ).
  > Nhắn Zalo OA **0822.928.988** hoặc đặt tại **mausonxanh.com**."*
- **Nhấn:** *"Lead magnet không có CTA = làm từ thiện. CTA này lấy từ đâu? **Core Offer 7 khối, N3 (`OF#`)** — không sáng tác."*

**Bước 3 (7') — AI LẮP RÁP landing page copy 9 khối (khoảnh khắc "à ra thế").** 🔴
- **Làm gì:** Chạy **Prompt 3** — nhưng **trước khi chạy, trainer chiếu khối INPUT của prompt lên và nói:** *"Nhìn kỹ đây. Tôi không bảo AI 'viết cho tôi một landing page'. Tôi **dán vào 5 câu khách nói, 5 câu FAQ thật, 7 khối offer, product knowledge, brand voice**. AI chỉ có việc **XẾP**. Đây là khác biệt giữa content chạm và content nghe tây."*
- **Duyệt live 3 chỗ (làm thật, để lớp thấy AI sai ở đâu):**

| Khối | AI trả | Trainer sửa | Vì sao |
|:-:|---|---|---|
| **1 Headline** | *"Nhận ngay cẩm nang trà thảo mộc miễn phí"* | → *"**Tự chấm 10 tiêu chí: trà bạn đang uống có thật là trà vùng nguyên liệu?**"* | Bán **KẾT QUẢ**, không bán **món quà**. Cấm mở đầu bằng "Miễn phí"/"Tải ngay". |
| **3 Vấn đề** | *"Bạn đang mệt mỏi vì giấc ngủ không sâu và muốn tìm giải pháp tự nhiên?"* | → **Dán nguyên văn `V3`:** *"Sao đắt hơn trà ngoài siêu thị thế em?"* + **`V2`:** *"Chị ngủ kém lắm, uống bao lâu thì thấy đỡ?"* | 🔴 **Câu AI viết là câu KHÔNG AI TỪNG NÓI.** Câu `V3` là câu khách **thật sự gõ vào inbox MSX**. Đây chính là LUẬT TRUY NGUYÊN. |
| **9 FAQ** | AI tự chế 4 câu hỏi | → **Mở FAQ Database (N4), copy thẳng:** *"trà này có chất bảo quản không"* (→ **không, 100% tự nhiên**) · *"phụ nữ có thai dùng được không"* (→ **tham khảo bác sĩ**) · *"phí ship bao nhiêu"* (→ **freeship đơn ≥500.000đ**) · *"có COD không"* · *"nguyên liệu lấy từ đâu, có sạch không"* (→ **hái thủ công Mẫu Sơn 800–1.541m**) | **Ta có ≥30 câu hỏi THẬT rồi. Việc gì phải đoán?** |

- **Và chỉ vào khối 7 — Bằng chứng:** *"Chỗ này tôi KHÔNG cho AI viết. **OCOP 3★, 5.000+ khách, ảnh vùng nguyên liệu** — 🔴 tầng NGƯỜI. AI bịa một con số ở đây là phá 5.000 khách đã có."*
- **Kết quả:** copy 9 khối trong bảng **T12.2 — có cột `Mã nguồn` điền đủ**.

**Bước 4 (7') — Dựng Google Form + đấu nối Sheet.**
- Google Form mới → tiêu đề + mô tả **lấy từ khối 1–2 của copy** (không viết lại) → **6 trường:** Họ tên / SĐT / *"Zalo có phải số này không?"* / 🔴 **"Bạn đang quan tâm điều gì nhất?"** (5 lựa chọn: Khó ngủ, muốn thư giãn buổi tối · Tìm quà biếu bố mẹ · Muốn dùng thử trước · Đang so sánh với trà khác · Hỏi mua sỉ – đại lý) / Ghi chú.
- ⚙️ **Cài đặt sống còn (làm chậm, chiếu rõ):** **TẮT** *"Thu thập email"* / **TẮT** *"Giới hạn 1 phản hồi"* / **TẮT** yêu cầu đăng nhập Google → nếu không, **khách thật không điền được và bạn sẽ không bao giờ biết**.
- Câu xác nhận sau khi gửi = **Thank You Message (Prompt 4)**.
- **Responses → Link to Sheets** → tạo Sheet `MSX-Leads`.
- **Thêm tay 4 cột:** `Nguồn | Phân loại | Trạng thái follow-up | Người phụ trách` → *"Đây là **mầm CRM của Tuần 3**. Cột **Phân loại** tự động có sẵn từ trường phân loại — đó là lý do ta bắt buộc nó phải là **danh sách chọn**, không phải tự luận."*
- 🔒 **Data Security ngay tại đây:** Share Sheet → **chỉ thêm email của Linh (trực lead) + chủ DN**. **KHÔNG** để "Anyone with the link". Chiếu cho lớp thấy nút đó ở đâu.

**Bước 5 (3') — 🔴 TEST LUỒNG THẬT (khoảnh khắc quan trọng nhất của cả Tuần 2).**
- **Làm gì:** Trainer **mở link form trên ĐIỆN THOẠI** (không phải máy tính) → điền vai khách: *"Nguyễn Thu Hà — 09xx xxx 123 — Đang so sánh với trà khác"* → **Gửi** → chuyển màn hình sang Sheet → **dòng lead hiện ra sau 2 giây** → cả lớp nhìn thấy.
- Gửi PDF qua Zalo theo đúng kịch bản Thank You. Bấm giờ: **≤5 phút**.
- **Thông điệp (nói chậm):** *"Đây là giây phút hệ thống marketing của anh chị **CHẠM được vào khách hàng đầu tiên**. Mọi thứ 11 ngày qua — ICP, offer, KB, 10 bài, 6 visual, 2 video — đều để dẫn tới **2 giây vừa rồi**. Và tối nay tôi sẽ làm đúng việc này với form của từng người."*

**Bước 6 (3') — Vẽ Lead Flow Map, có TÊN NGƯỜI.**
- Điền **T12.4** — 6 trạm, mỗi mũi tên ghi `[Ai | Công cụ | Thời gian tối đa]`:

| # | Trạm | Ai | Công cụ | Trong bao lâu | Tầng |
|:-:|---|---|---|:---:|:---:|
| ① | Người xem (bài/video có CTA) | — | Facebook / TikTok | — | — |
| ② | Điền form (6 trường) | Khách | Google Form | — | — |
| ③ | Thank You + gửi bảng so sánh PDF | **Linh** (CSKH MSX) | Zalo OA 0822.928.988 | **≤5 phút** (ca trực 8h–22h) | 🟢 AUTO (Bonus) / 🔴 NGƯỜI (hôm nay) |
| ④ | Lead vào Sheet `MSX-Leads` | *(máy)* | Google Sheet | tức thì | 🟢 **AUTO** |
| ⑤ | **Tin nhắn giá trị 24h** | 🔴 **Linh — NGƯỜI THẬT gửi/duyệt** | Zalo | **≤24 giờ** | 🔴 **NGƯỜI — CẤM auto blast** |
| ⑥ | Cập nhật trạng thái + phân loại | **Linh**, chủ DN review | Google Sheet | cuối ca | 🟡 ASSISTED |
| 🔒 | **Data Security** | — | — | — | **Sheet `MSX-Leads` = tầng Restricted. Chỉ Linh + chủ DN xem. KHÔNG chia sẻ link công khai, KHÔNG chụp màn hình SĐT đăng lên bất cứ đâu.** |

- **Nhấn:** *"Trạm nào không có TÊN NGƯỜI là trạm đó **KHÔNG AI LÀM**. 'Nhân viên sẽ follow-up' = không ai follow-up. Viết chữ **Linh** vào."*

---

## 5. ✅ Checklist Thực Thi (Học viên tự làm)

> ⏱ **Tổng Core: dùng template điền sẵn 110' · lần đầu tự làm 165'.**
> 🔴 **THỨ TỰ LÀ BẮT BUỘC — không được đảo:** Cụm A (Form) **TRƯỚC** → rồi mới Cụm C (PDF). Đây là bài học xương máu: *người làm PDF trước thì 23h vẫn đang chỉnh màu trang bìa và **chưa có form nào để nộp**.*
> **PDF xấu vẫn giao được quà. Form chưa có là MẤT LEAD.**

**🔴 Cụm A — FORM CHẠY THẬT (làm ĐẦU TIÊN)**
`⏱ dùng template điền sẵn: 25' · lần đầu tự làm: 40'`
- [ ] Tạo Google Form (hoặc form RocketAgent/Ladipage): **6 trường**, trong đó **BẮT BUỘC** có **trường phân loại dạng danh sách chọn** (4–5 phương án + 1 "khác").
- [ ] ⚙️ Kiểm 3 cài đặt: **TẮT** thu thập email · **TẮT** giới hạn 1 phản hồi · **TẮT** yêu cầu đăng nhập Google.
- [ ] Liên kết form → Google Sheet. Thêm tay 4 cột: `Nguồn | Phân loại | Trạng thái | Người phụ trách`.
- [ ] 🔒 **Data Security:** share Sheet **theo email cụ thể** (người trực lead + chủ DN). **KHÔNG** bật "ai có link cũng xem được".
- [ ] 🔴 **TEST 2 LẦN:** ① tự điền **bằng ĐIỆN THOẠI** (không phải máy tính) + trình duyệt ẩn danh → lead phải hiện trong Sheet. ② **nhờ 1 người thân điền lần 2** từ máy của họ.

**Cụm B — Landing page copy 9 khối (LẮP RÁP, không sáng tác)**
`⏱ dùng template điền sẵn: 25' · lần đầu tự làm: 40'`
- [ ] Mở sẵn 4 file Tuần 1: **5 câu nguyên văn khách (N2)** · **FAQ Database (N4)** · **Core Offer 7 khối (N3)** · **Product Knowledge (N4)**.
- [ ] Chạy **Prompt 3** — **dán 4 thứ trên vào khối INPUT**. (Prompt nào không có chúng trong INPUT = copy bịa.)
- [ ] Dán vào **T12.2** và **ĐIỀN CỘT `Mã nguồn` CHO TỪNG KHỐI**.
- [ ] 🔴 **Duyệt truy nguyên (bắt buộc):**
  - Khối 3 (Vấn đề) = **lời khách nguyên văn `V#`** — nếu đọc lên thấy "văn AI" → **thay bằng câu khách thật**.
  - Khối 9 (FAQ) = **lấy thẳng 4–5 cặp từ FAQ Database `Q##`** — không viết mới.
  - Khối 7 (Bằng chứng) = **dữ liệu thật của bạn** — không placeholder, không bịa.
  - Khối 8 (CTA) = **từ Core Offer `OF#`**.
- [ ] ⚖️ **Soát ranh giới pháp lý:** Ctrl+F tìm các từ **chữa · khỏi · đặc trị · thần dược · cam kết 100% · "chỉ còn X suất"** → **xoá sạch**. Lý do mua ngay phải THẬT.

**Cụm C — Lead magnet PDF**
`⏱ dùng template điền sẵn: 40' · lần đầu tự làm: 60'` — **timebox cứng: hết 40' là dừng, xuất bản cái đang có.**
- [ ] Chạy **Prompt 1** → chọn 1 ý tưởng **đạt cả 4 tiêu chí** (tự chấm bảng **T12.1**, tổng ≥16/20).
- [ ] Chạy **Prompt 2** → duyệt ruột: 🟡 **nhét vào ≥2 chi tiết chuyên môn THẬT** của bạn (lấy từ **Product Knowledge N4**) — thứ AI không thể tự nghĩ ra.
- [ ] Kiểm **trang cuối CÓ CTA** về offer thật (`OF#`) + cách liên hệ (Zalo/website).
- [ ] Canva: template ebook/checklist → dán nội dung → màu/font **Visual Brand Kit (N10)** → xuất PDF **4–8 trang**, đặt tên `[TênDN]-leadmagnet-[tên]-v1.pdf`.

**Cụm D — Bộ 3 tin nhắn + Lead Flow Map**
`⏱ dùng template điền sẵn: 20' · lần đầu tự làm: 25'`
- [ ] Chạy **Prompt 4** → 3 tin: Thank You (dán vào phần xác nhận của form) · tin gửi quà · **tin follow-up 24h**.
- [ ] 🔴 Kiểm tin 24h: **KHÔNG mở đầu bằng chào bán** ("bên em đang có chương trình…") → mở bằng **giá trị hoặc câu hỏi quan tâm**. Ghi rõ: **NGƯỜI THẬT gửi/duyệt — không auto blast.**
- [ ] Điền **T12.4**: **đủ 6 trạm**, mỗi trạm có `[Ai | Công cụ | Thời gian tối đa]` — **TÊN NGƯỜI THẬT**, không phải "nhân viên".
- [ ] 🔒 Thêm **dòng Data Security** vào Lead Flow Map: Sheet lead = **Restricted** · ai được xem · **không đăng công khai / không chụp SĐT khách**.
- [ ] Ghi 3 tầng tự động hoá lên Map: 🟢 AUTO (form→Sheet, gửi quà tự động, thank-you) · 🟡 ASSISTED (copy, ruột lead magnet) · 🔴 NGƯỜI (tin 24h, bằng chứng, feedback).

> **⛑️ Luật cứu hộ (nếu quá giờ):** làm theo thứ tự **A → B → C → D**. Nộp **80% đúng hạn thắng 100% trễ 2 ngày**. Nếu chỉ kịp 1 thứ duy nhất: **NỘP FORM CHẠY THẬT.** Bonus không bắt buộc, không trừ điểm.

**Bonus (60–90'):**
- [ ] Dựng landing page thật: Ladipage / Canva Website / RocketAgent → dán copy 9 khối → ảnh thật (vùng nguyên liệu) + Brand Kit → gắn form → **test lại end-to-end trên điện thoại**.
- [ ] 🟢 Cài Zalo OA / email **gửi quà tự động** (không cần người trực) — đây là thứ kéo *"gửi quà ≤5 phút"* từ lời hứa thành sự thật kể cả lúc 23h.
- [ ] Phác **lead magnet #2** dạng khác (với MSX: *"Cẩm nang Trà Tối — 7 ngày"* cho tệp chưa so sánh; với 🚀 RocketAI: **trang đăng ký buổi demo 30 phút**).

---

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Xây **ĐIỂM CHUYỂN ĐỔI** cho doanh nghiệp của bạn — 1 lead magnet PDF, copy landing 9 khối **lắp ráp từ tài sản Tuần 1 (có mã nguồn)**, **form thu lead CHẠY THẬT đổ về Sheet**, bộ 3 tin nhắn, và Lead Flow Map có **tên người thật** + dòng Data Security.

**Deliverable nộp (thread cohort, deadline 23h59 hôm nay):**

| # | Tên file | Yêu cầu nghiệm thu |
|:-:|---|---|
| 1 | `[Tên DN] — Ngày 12 — Link Form Thu Lead` | 🔴 **Mentor sẽ BẤM LINK VÀ ĐIỀN THỬ.** Kèm ảnh chụp Sheet đã có **≥2 dòng test** — **CHE 4 SỐ CUỐI SĐT** (`09xx xxx 123`). |
| 2 | `[Tên DN] — Ngày 12 — Landing Page Copy` | Theo **T12.2** — đủ **9/9 khối** + **cột `Mã nguồn` điền đủ**. Khối 3 = `V#`, khối 9 = `Q##`, khối 8 = `OF#`. |
| 3 | `[Tên DN] — Ngày 12 — Lead Magnet` | PDF **4–8 trang** (hoặc link Drive) — **trang cuối có CTA về offer thật**. |
| 4 | `[Tên DN] — Ngày 12 — Bộ 3 Tin Nhắn` | Thank You + tin gửi quà + **tin 24h (ghi rõ AI GỬI: tên người thật)**. |
| 5 | `[Tên DN] — Ngày 12 — Lead Flow Map` | Theo **T12.4** — **6 trạm**, **tên người thật**, **dòng Data Security**, 3 tầng AUTO/ASSISTED/NGƯỜI. |
| 6 | *(Bonus)* | Link landing đã dựng + ảnh chụp Zalo/email tự động. |

> 🔴 **Cảnh báo nộp bài:** ai nộp **ảnh Sheet còn nguyên SĐT khách/người thân** → gỡ ngay + trừ điểm (vi phạm Data Security Rule N4). Che 4 số cuối.

---

## 7. 📄 Template Đi Kèm

**T12.1 — Bảng Chọn Lead Magnet (4 tiêu chí)** *(Google Sheet)*
Cột: `Ý tưởng | A. Cụ thể & cấp? (1-5) | B. Dùng ≤15'? (1-5) | C. Dẫn thẳng đến offer? (1-5) | D. Thể hiện chuyên môn? (1-5) | Tổng /20 | Chọn?`
→ **Ngưỡng chọn: ≥16/20.** Có sẵn **5 dòng MSX chấm mẫu** (gồm cặp đối đầu *Cẩm nang Trà Tối* 14 vs *Bảng so sánh 10 tiêu chí* 20) + ghi chú thích ứng ngành (spa/nha khoa/giáo dục/gym) + **hàng B2B mẫu của 🚀 RocketAI** (*buổi demo 30 phút* = 19/20).

**T12.2 — Landing Page Copy 9 Khối (CÓ CỘT MÃ NGUỒN)** *(Google Doc/Sheet)* 🔴 *template quan trọng nhất hôm nay*
Bảng 9 dòng × 4 cột: `# | Khối | Nội dung của bạn | 🔗 Mã nguồn (BẮT BUỘC)`.
Mỗi khối có **hướng dẫn 1 dòng + giới hạn độ dài**: headline ≤14 từ · vấn đề 3–4 gạch **bằng lời khách nguyên văn** · nội dung nhận được 5–7 gạch · FAQ 4–5 câu **lấy từ FAQ DB**.
Cột Mã nguồn có **gợi ý sẵn theo dòng**: khối 3 → `V#` · khối 5 → `PK` · khối 7 → dữ liệu thật N1/N4 · khối 8 → `OF#` · khối 9 → `Q##`.
Cuối template: **ô đếm truy nguyên** (`__/9 khối có mã nguồn` — **cần ≥8/9**) + **checklist ranh giới pháp lý** (6 từ cấm). Toàn bộ đã điền mẫu MSX in nghiêng để ghi đè.

**T12.3 — Cấu Trúc Form Chuẩn + hướng dẫn nối Sheet** *(1 trang)*
**6 trường** + đúng câu chữ gợi ý từng trường + **5 bộ câu phân loại theo ngành** (🍵 trà/thực phẩm · spa · nha khoa · giáo dục · gym) + **1 bộ B2B của 🚀 RocketAI** (thêm trường *quy mô nhân sự / doanh thu tháng*).
Kèm: ⚙️ **3 cài đặt sống còn** (tắt thu email / tắt giới hạn 1 phản hồi / tắt đăng nhập) · hướng dẫn liên kết Google Sheet **có ảnh chụp màn hình từng bước** · 4 cột quản trị phải thêm tay · 🔒 **hướng dẫn share Sheet an toàn** (theo email, không dùng link công khai).

**T12.4 — Lead Flow Map 6 trạm** *(Google Doc/Canva, 1 trang)*
Sơ đồ dựng sẵn: `① Nguồn traffic → ② Landing/Form → ③ Thank You + gửi quà → ④ Sheet/CRM → ⑤ Tin nhắn 24h → ⑥ Cập nhật trạng thái`.
Mỗi trạm **3 ô trống `[Ai | Công cụ | Thời gian tối đa]`** + **1 ô tầng tự động hoá** (🟢/🟡/🔴).
Cuối trang: 🔒 **dòng Data Security bắt buộc** (lead = Restricted · ai được xem · lưu ở đâu · cấm đăng công khai). Bản MSX điền mẫu (Linh — CSKH).

---

## 8. 🤖 Prompt Mẫu

> 📚 **Kế thừa Prompt Library (N5):** các prompt dưới đây là **bản CÁ NHÂN HOÁ** của **M10 — "lead magnet"** (Prompt 1, 2) và **M09 — "viết landing page theo StoryBrand"** (Prompt 3). **Không phải prompt mới.**
> ⚙️ **Chạy Ở ĐÂU:** chạy **trong AI Marketing Assistant (N6)** — nó đã có sẵn Knowledge Base (ICP, Offer, FAQ DB, Product Knowledge, Brand Voice). **Đừng mở ChatGPT trắng rồi dán lại toàn bộ Tuần 1** — vừa mất 20 phút vừa dán thiếu.

---

### Prompt 1 — Chọn lead magnet (bản cá nhân hoá của M10)

```
[VAI TRÒ]
Bạn là chuyên gia lead generation (tạo khách hàng tiềm năng) cho doanh
nghiệp Việt Nam bán qua tư vấn/niềm tin.

[BỐI CẢNH]
Khách của tôi phải TIN mới mua. Tôi cần 1 lead magnet khiến ĐÚNG ICP tự
nguyện để lại số điện thoại — và người tải về phải chính là người có khả
năng mua offer trả phí.
Mức nhận thức của avatar: {{Unaware / Problem Aware / Solution Aware /
Product Aware / Most Aware}}  ← YẾU TỐ QUYẾT ĐỊNH. Solution Aware thì
KHÔNG cho bài giảng nhập môn — phải cho CÔNG CỤ SO SÁNH.

[NHIỆM VỤ]
Từ danh sách ý tưởng dưới đây (được đề xuất thêm nếu bạn có ý hay hơn),
chấm từng ý theo 4 tiêu chí thang 1-5:
(A) Cụ thể & cấp bách  (B) Dùng được trong ≤15 phút
(C) Dẫn thẳng đến offer trả phí  (D) Thể hiện chuyên môn thật
Chọn 1 ý THẮNG (tổng ≥16/20) + 3 phương án tên gọi + giải thích vì sao
người TẢI nó chính là người MUA offer + nó đánh vào objection nào.

[DỮ LIỆU ĐẦU VÀO]
- 8 ý lead magnet từ bảng 60 ý tưởng (Ngày 08): {{dán}}
- Avatar + mức nhận thức: {{dán từ N2}}
- PDFO — đặc biệt các Objection O1..O5: {{dán từ N2}}
- Offer trả phí + giá: {{dán từ Core Offer 7 khối, N3}}
- Chuyên môn/tài sản độc quyền của tôi: {{dán từ Product Knowledge, N4}}

[ĐỊNH DẠNG ĐẦU RA]
Bảng chấm 4 tiêu chí + phần đề xuất + 1 dòng "ý này đánh vào objection nào".

[RÀNG BUỘC]
- Loại thẳng ý dạng "cẩm nang toàn tập" >15 trang.
- Tên gọi phải chứa KẾT QUẢ hoặc CON SỐ; KHÔNG chứa từ "miễn phí".
- Không đề xuất ý tưởng đòi hỏi dữ liệu tôi không có.
```

**🍵 Ví dụ đã điền — MSX Group (khối DỮ LIỆU ĐẦU VÀO):**
```
- 8 ý: cẩm nang trà tối 7 ngày; bảng so sánh trà chuẩn vùng nguyên liệu
  vs trà phổ thông (tự chấm 10 tiêu chí); ebook toàn tập thảo dược VN;
  quiz "bạn hợp loại trà nào"; lịch uống trà 28 ngày; cách đọc nhãn trà;
  video 5' hành trình hái trà Mẫu Sơn; voucher freeship.
- Avatar: chị Hương, 40t, NV văn phòng Hà Nội, ~20tr/tháng, "người giữ
  sức khoẻ của cả nhà", lướt FB 21h-23h.
  MỨC NHẬN THỨC 3 — SOLUTION AWARE: đã biết trà thảo mộc là giải pháp,
  ĐANG SO SÁNH, chưa biết MSX.
- Objection: O1 "sao đắt hơn trà ngoài siêu thị" (khách nói nguyên văn V3:
  "sao đắt hơn trà ngoài siêu thị thế em") · O2 "sợ mua nhiều uống không
  hợp" (V4) · O3 "uống bao lâu mới thấy đỡ" (V2).
- Offer: Trà Mẩy Gòm An Giấc 359.000đ/hộp · Combo mua 3 tặng 1 =
  1.015.000đ (offer chủ lực) · freeship đơn ≥500.000đ.
- Chuyên môn độc quyền: vùng nguyên liệu Mẫu Sơn 800-1.541m; người Dao/
  Tày/Nùng hái thủ công; OCOP 3★; 5.000+ khách; giao Viettel Post.
```
> **AI trả:** *Bảng so sánh 10 tiêu chí = **20/20** — thắng vì đánh thẳng O1/V3 và khớp Solution Aware (khách đang so sánh thì đưa cho họ cái THƯỚC).* · *Cẩm nang Trà Tối = 14/20 — hay nhưng sai mức nhận thức, để làm lead magnet #2.*

**🚀 Đối chiếu RocketAI (B2B):** input đổi Avatar thành *chị Mai — chủ Spa ABC*, Offer thành *gói triển khai AI*, ý tưởng thắng là **"buổi demo/audit 30 phút — xem hệ thống chạy thật trên 1 spa"** (19/20 — B2B không tải PDF, B2B muốn **THẤY**).

---

### Prompt 2 — Viết ruột lead magnet (bản cá nhân hoá của M10)

```
[VAI TRÒ]
Bạn là chuyên gia trong ngành của tôi kiêm người thiết kế tài liệu thực
hành — viết thứ người đọc DÙNG được, không phải đọc cho biết.

[BỐI CẢNH]
Brand Voice: {{lấy từ Knowledge Base / Brand Voice Guideline N09}}
Lead magnet sẽ đóng gói thành PDF 4-8 trang trong Canva.
Người đọc là {{avatar}}, mức nhận thức {{...}}.

[NHIỆM VỤ]
Viết toàn bộ nội dung theo cấu trúc:
- Trang bìa: tên tài sản + 1 câu hứa + dòng "dành cho ai".
- Trang mở: 3-4 câu đồng cảm (DÙNG ĐÚNG lời khách tôi đưa ở INPUT, không
  tự viết câu đồng cảm chung chung) + cách dùng tài liệu này.
- Phần ruột: {{ví dụ: bảng 10 tiêu chí tự chấm — mỗi tiêu chí gồm: câu
  hỏi + vì sao nó quan trọng + cách tự kiểm trong 1 phút}}.
- Phần bổ trợ: {{ví dụ: cách đọc nhãn + 3 dấu hiệu nhận biết hàng pha trộn}}.
- Trang cuối: kết luận theo thang điểm + CTA về offer + cách liên hệ.

[DỮ LIỆU ĐẦU VÀO]
- Lead magnet đã chọn: {{tên + mô tả}}
- Câu khách nói nguyên văn (V1..V5): {{dán từ N2}}
- CHUYÊN MÔN THẬT bắt buộc phải dùng (5-7 gạch, lấy từ Product Knowledge
  N4 — đây là thứ bạn KHÔNG được tự nghĩ ra): {{dán}}
- Offer + CTA trang cuối: {{dán từ Core Offer 7 khối N3}}

[ĐỊNH DẠNG ĐẦU RA]
Nội dung chia theo trang; mỗi trang kèm ghi chú [Gợi ý hình/bố cục Canva].

[RÀNG BUỘC]
- Người đọc làm theo được NGAY, không cần mua gì.
- KHÔNG bịa số liệu, chứng nhận, tên khách. Chỉ dùng dữ liệu tôi đưa.
- RANH GIỚI PHÁP LÝ: CẤM các từ "chữa", "khỏi", "đặc trị", "thần dược",
  "cam kết 100%". Chỉ được nói "hỗ trợ thư giãn buổi tối". Nhóm có thai/
  cho con bú/trẻ em/bệnh nền → khuyên tham khảo bác sĩ.
- KHÔNG tạo khan hiếm giả ("chỉ còn 5 suất"). Lý do mua ngay phải THẬT.
- Trang cuối BẮT BUỘC có CTA + cách liên hệ.
```

**🍵 Ví dụ đã điền — MSX (khối CHUYÊN MÔN THẬT):**
```
- Vùng nguyên liệu Mẫu Sơn, Lạng Sơn — độ cao 800-1.541m; chênh nhiệt
  ngày/đêm lớn → tinh dầu trong lá đậm hơn trà trồng đồng bằng.
- Người Dao/Tày/Nùng hái THỦ CÔNG, chọn từng búp — không hái máy.
- Chứng nhận OCOP 3★. 100% tự nhiên, KHÔNG chất bảo quản.
- 5.000+ khách đã dùng. Giao Viettel Post toàn quốc, freeship đơn ≥500k.
- Trà Mẩy Gòm An Giấc — 359.000đ/hộp (~25 ngày dùng).
- CTA trang cuối: "Chấm dưới 7/10? Trà Mẩy Gòm An Giấc 359.000đ/hộp ·
  Combo mua 3 tặng 1 = 1.015.000đ (freeship đơn từ 500.000đ). Zalo OA
  0822.928.988 · mausonxanh.com"
```

---

### Prompt 3 — LẮP RÁP landing page copy 9 khối (bản cá nhân hoá của M09 — StoryBrand) 🔴

> **Đây là prompt quan trọng nhất hôm nay.** Đọc kỹ khối `[DỮ LIỆU ĐẦU VÀO]`: nó **dày** — vì landing page là **bản lắp ráp**, không phải bài văn. **Prompt nào không có 5 khối input dưới đây = copy bịa.**

```
[VAI TRÒ]
Bạn là copywriter trang đích thu lead cho doanh nghiệp Việt Nam, viết
theo StoryBrand: khách là NHÂN VẬT CHÍNH, thương hiệu là NGƯỜI DẪN ĐƯỜNG.
Tâm lý đọc: chú ý → đúng bệnh → muốn → tin → hành động.

[BỐI CẢNH]
Brand Voice: {{lấy từ Knowledge Base / Brand Voice Guideline N09}}
Trang này ĐỔI LEAD MAGNET LẤY SỐ ĐIỆN THOẠI — KHÔNG bán offer trả phí
trực tiếp (sai tầng phễu).
Avatar + mức nhận thức: {{dán}} ← Solution Aware thì trang phải nghiêng
hẳn về SO SÁNH + BẰNG CHỨNG, KHÔNG dạy lại kiến thức nhập môn.
Traffic đến từ: {{bài viết/video Facebook, TikTok, Zalo}}.

[NHIỆM VỤ]
Viết đủ 9 khối. VỚI MỖI KHỐI, GHI RÕ CỘT "MÃ NGUỒN" — bạn lấy chất liệu
từ dòng dữ liệu nào tôi đưa. Khối nào bạn không truy được về input của
tôi → GHI RÕ "⚠️ TÔI TỰ VIẾT" để tôi xoá.

1. Headline ≤14 từ — nêu KẾT QUẢ + cho ai.          [nguồn: MSG/AV]
2. Subheadline — làm rõ món quà + uy tín.           [nguồn: MSG/PK]
3. Vấn đề — 3-4 gạch, BẮT BUỘC DÙNG NGUYÊN VĂN câu khách tôi đưa
   (V1..V5). CẤM bạn tự viết câu đồng cảm.          [nguồn: V#]
4. Lời hứa kết quả sau khi dùng quà.                [nguồn: D#]
5. Nội dung nhận được — 5-7 gạch, lấy từ Product Knowledge tôi đưa.
                                                     [nguồn: PK]
6. Lợi ích/khác biệt — 3 gạch, gỡ objection.        [nguồn: O#/F#]
7. Bằng chứng — CHỈ DÙNG dữ liệu thật tôi đưa. Thiếu thì ghi
   [CẦN BỔ SUNG], TUYỆT ĐỐI KHÔNG BỊA.              [nguồn: dữ liệu thật]
8. CTA + chữ trên nút + dòng trấn an dưới nút.      [nguồn: OF#]
9. FAQ — 4-5 câu, LẤY THẲNG từ FAQ & Objection Database tôi đưa.
   CẤM tự nghĩ câu hỏi mới.                          [nguồn: Q##]

[DỮ LIỆU ĐẦU VÀO]  ← 5 khối bắt buộc, thiếu 1 khối là copy bịa
(1) Lead magnet: {{tên + 1 câu mô tả}}
(2) 5 CÂU KHÁCH NÓI NGUYÊN VĂN (V1..V5, từ N2): {{dán}}
(3) FAQ & OBJECTION DATABASE — chọn 5 cặp hỏi/đáp thật (Q##, từ N4): {{dán}}
(4) PRODUCT KNOWLEDGE + BẰNG CHỨNG THẬT (từ N4/N1): {{dán}}
(5) CORE OFFER 7 KHỐI + cách nhận quà (từ N3): {{dán}}

[ĐỊNH DẠNG ĐẦU RA]
Bảng: | # | Khối | Nội dung | Mã nguồn |  → dán thẳng được vào T12.2.

[RÀNG BUỘC]
- KHÔNG bịa con số/feedback/chứng nhận. Khối 7 chỉ dùng dữ liệu tôi đưa.
- Headline KHÔNG bắt đầu bằng "Miễn phí" / "Tải ngay".
- Toàn trang CHỈ 1 hành động: điền form. Không thêm nút gọi/mua khác.
- RANH GIỚI PHÁP LÝ (tuyệt đối): CẤM "chữa", "khỏi", "đặc trị", "cam kết
  100%", "hiệu quả sau X ngày". Chỉ "hỗ trợ thư giãn buổi tối".
- CẤM khan hiếm giả ("còn 5 suất", "hôm nay là ngày cuối"). Lý do hành
  động ngay phải THẬT (freeship đơn ≥500k / lô hàng thật / lịch giao).
```

**🍵 Ví dụ đã điền — MSX (khối DỮ LIỆU ĐẦU VÀO):**
```
(1) Lead magnet: "Bảng so sánh trung thực: trà thảo mộc chuẩn vùng nguyên
    liệu vs trà phổ thông — tự chấm 10 tiêu chí" (10 phút, tự chấm, biết
    mình đang trả tiền cho lá trà hay cho bao bì).

(2) 5 CÂU KHÁCH NÓI NGUYÊN VĂN:
    V1 "trà mẩy gòm này người huyết áp cao uống đc k em"
    V2 "chị ngủ kém lắm, uống bao lâu thì thấy đỡ"
    V3 "sao đắt hơn trà ngoài siêu thị thế em"
    V4 "cho chị mua 1 hộp dùng thử trước đc k, sợ mua nhiều uống k hợp"
    V5 "mua tặng mẹ thì nên lấy trà hay viên em nhỉ"

(3) FAQ THẬT (từ FAQ & Objection Database N4):
    Q "trà này có chất bảo quản không" → A "Không. 100% tự nhiên."
    Q "phụ nữ có thai dùng được không" → A "Nên tham khảo ý kiến bác sĩ."
    Q "phí ship bao nhiêu" → A "Freeship đơn từ 500.000đ."
    Q "có COD không" → A "Có, giao Viettel Post toàn quốc."
    Q "nguyên liệu lấy từ đâu, có sạch không" → A "Hái thủ công tại Mẫu
      Sơn, độ cao 800-1.541m."

(4) BẰNG CHỨNG THẬT: OCOP 3★ · 5.000+ khách · ảnh vùng nguyên liệu Mẫu
    Sơn 800-1.541m · người Dao/Tày/Nùng hái tay · website mausonxanh.com.

(5) OFFER + NHẬN QUÀ: Trà Mẩy Gòm An Giấc 359.000đ/hộp · Combo mua 3
    tặng 1 = 1.015.000đ · freeship đơn ≥500.000đ. Quà gửi qua Zalo OA
    0822.928.988 trong 5 phút.
```

**AI trả (trích — chú ý cột Mã nguồn):**

| # | Khối | Nội dung | 🔗 Mã nguồn |
|:-:|---|---|:---:|
| 1 | Headline | *"Tự chấm 10 tiêu chí: trà bạn đang uống có thật là trà vùng nguyên liệu?"* | `MSG` + `AV` |
| 3 | Vấn đề | *"Sao đắt hơn trà ngoài siêu thị thế em?"* · *"Chị ngủ kém lắm, uống bao lâu thì thấy đỡ?"* · *"Cho chị mua 1 hộp dùng thử trước được không, sợ mua nhiều uống không hợp"* | 🔴 **`V3` `V2` `V4`** |
| 5 | Nội dung nhận được | *"10 tiêu chí chấm · bảng độ cao vùng nguyên liệu · cách đọc nhãn · 3 dấu hiệu trà pha trộn · thang kết luận theo điểm"* | `PK` |
| 7 | Bằng chứng | *"OCOP 3★ · 5.000+ khách đã dùng · ảnh vùng nguyên liệu Mẫu Sơn 800–1.541m · người Dao/Tày/Nùng hái thủ công"* | dữ liệu thật `N1/N4` |
| 8 | CTA | Nút: *"Nhận bảng so sánh qua Zalo"* · Dưới nút: *"Chỉ nhắn Zalo gửi tài liệu. Không gọi điện nếu bạn không hẹn."* | `OF#` (N3) |
| 9 | FAQ | *"Trà này có chất bảo quản không?"* · *"Phụ nữ có thai dùng được không?"* · *"Phí ship bao nhiêu?"* · *"Có COD không?"* · *"Nguyên liệu lấy từ đâu?"* | 🔴 **`Q##` (N4)** |

> ✅ **8/9 khối có mã nguồn** → đạt ngưỡng. Khối AI ghi *"⚠️ TÔI TỰ VIẾT"* → **xoá hoặc đi lấy nguồn thật về thay.**

---

### Prompt 4 — Bộ 3 tin nhắn (Thank You / gửi quà / follow-up 24h)

```
[VAI TRÒ]
Bạn là chuyên gia nurturing (nuôi dưỡng khách hàng tiềm năng), giỏi viết
tin nhắn khiến lead thấy được CHĂM chứ không bị SĂN.

[BỐI CẢNH]
Người nhận vừa để lại SĐT để nhận {{tên lead magnet}}. Họ CHƯA mua gì.
Người gửi là {{tên thật + vai trò}} — một CON NGƯỜI, không phải hệ thống.

[NHIỆM VỤ]
Viết 3 tin theo Brand Voice:
(1) THANK YOU MESSAGE (hiện ngay sau khi bấm Gửi form): xác nhận + nói rõ
    NHẬN QUÀ QUA KÊNH NÀO, TRONG BAO LÂU + 1 câu giữ kỳ vọng.
(2) TIN GỬI QUÀ (Zalo, ≤5 dòng): trao quà + 1 mẹo dùng nhanh + câu mở
    đường ("có gì thắc mắc cứ nhắn mình nhé").
(3) TIN FOLLOW-UP SAU 24H (≤5 dòng): hỏi trải nghiệm dùng quà + cho thêm
    1 giá trị nhỏ + CTA MỀM sang offer.
    Viết 3 BIẾN THỂ theo trường phân loại lead trong form.

[DỮ LIỆU ĐẦU VÀO]
- Brand Voice: {{từ KB / Brand Voice Guideline N09}}
- Lead magnet + offer: {{1 câu mỗi thứ}}
- Người gửi: {{tên thật + vai trò}}
- Các lựa chọn trong trường phân loại của form: {{dán}}

[RÀNG BUỘC]
- Tin 24h TUYỆT ĐỐI KHÔNG mở đầu bằng chào bán ("bên em đang có chương
  trình…") — mở bằng GIÁ TRỊ hoặc CÂU HỎI QUAN TÂM.
- Mỗi tin đúng 1 CTA.
- Xưng hô đúng vai (em/chị), có TÊN người gửi. Không viết như bot.
- RANH GIỚI: cấm "chữa/khỏi/đặc trị/cam kết". Chỉ "hỗ trợ thư giãn".
- Không khan hiếm giả. Lý do mua ngay phải thật (freeship đơn ≥500k).
```

**🍵 Ví dụ đã điền — MSX (người gửi: **Linh — CSKH MSX**):**
```
(1) THANK YOU: "Cảm ơn chị đã để lại thông tin! Linh sẽ gửi Bảng so sánh
    10 tiêu chí qua Zalo trong 5 phút tới (số chị vừa điền). Chị mở Zalo
    giúp em nhé — chấm xong chị sẽ biết ngay trà mình đang uống đứng ở
    đâu."

(2) TIN GỬI QUÀ (Zalo): "Chị Hương ơi, Linh gửi chị Bảng so sánh 10 tiêu
    chí đây ạ 🍵 Mẹo nhanh: chị chấm tiêu chí #3 (độ cao vùng nguyên liệu)
    trước — riêng câu đó đã lộ ra 80% sự thật rồi. Có gì thắc mắc chị cứ
    nhắn em nhé!"

(3) TIN 24H — biến thể "Đang so sánh với trà khác":
    "Chị Hương ơi, chị chấm được mấy điểm rồi ạ? 😊 Em gửi thêm chị ảnh
    vùng nguyên liệu Mẫu Sơn tụi em hái tuần rồi — chị xem độ cao và cách
    hái tay để đối chiếu với tiêu chí #3 và #6 nhé. Nếu chị muốn thử một
    hộp trước cho yên tâm thì Trà Mẩy Gòm An Giấc 359k, chị cứ nhắn em."
    → mở bằng CÂU HỎI QUAN TÂM + GIÁ TRỊ (ảnh thật), CTA mềm ở cuối. ✅
```

> 🔴 **TẦNG NGƯỜI:** tin (3) **do Linh gửi hoặc duyệt trước khi gửi**. **KHÔNG auto blast.** Một tin tự động sai ngữ cảnh gửi cho người vừa hỏi *"mua tặng mẹ thì nên lấy trà hay viên em nhỉ"* (`V5`) sẽ phá đúng thứ ta vừa xây.

---

### Prompt 5 — 🔍 AI TỰ KIỂM TRA landing page trước khi đăng *(prompt "kiểm định")*

```
[VAI TRÒ]
Bạn là mentor khó tính của chương trình 28 Day AIOS, chuyên bắt lỗi
landing page trước khi nó gây thiệt hại cho doanh nghiệp thật.

[NHIỆM VỤ]
Soi bản copy 9 khối dưới đây và trả về BẢNG LỖI theo đúng 4 nhóm:

A. TRUY NGUYÊN — chỉ ra khối nào KHÔNG truy về được nguồn Tuần 1 (đặc
   biệt: khối 3 có phải lời khách nguyên văn không? khối 9 có lấy từ FAQ
   Database không? khối 7 có phải dữ liệu thật không?). Đếm: __/9 khối
   có mã nguồn (cần ≥8/9).
B. RANH GIỚI PHÁP LÝ — liệt kê MỌI câu vi phạm: "chữa/khỏi/đặc trị/thần
   dược/cam kết 100%/hiệu quả sau X ngày" + MỌI khan hiếm giả ("còn 5
   suất", "hôm nay là ngày cuối"). Mỗi lỗi ghi rõ: câu gốc → câu thay thế.
C. TẦNG PHỄU — trang này có đang BÁN OFFER TRẢ PHÍ thay vì mời nhận quà
   không? Có nhiều hơn 1 hành động không?
D. ĐỘ DÀI & MỨC NHẬN THỨC — headline >14 từ? Có đang dạy lại kiến thức
   nhập môn cho một avatar Solution Aware (đang so sánh) không?

[DỮ LIỆU ĐẦU VÀO]
- Copy 9 khối của tôi: {{dán bảng T12.2}}
- Avatar + mức nhận thức: {{dán}}
- Nguồn Tuần 1 (V#, Q##, OF#, PK): {{dán}}

[ĐỊNH DẠNG ĐẦU RA]
Bảng: | Nhóm | Khối | Lỗi | Mức độ (🔴 chặn đăng / 🟡 nên sửa) | Câu sửa gợi ý |
Kết luận: ĐƯỢC ĐĂNG / PHẢI SỬA TRƯỚC KHI ĐĂNG.

[RÀNG BUỘC]
- Nghiêm khắc. Thà bắt nhầm còn hơn bỏ sót.
- Mọi lỗi nhóm B đều là 🔴 CHẶN ĐĂNG, không có ngoại lệ.
```

> 💡 **Dùng prompt này trước khi nộp bài.** Nó chính là **bản AI hoá của rubric phần 10** — bạn tự chấm mình trước khi mentor chấm.

---

## 9. 📋 SOP Thao Tác

### **SOP-12 — Vận hành điểm chuyển đổi (trực lead)**

- **Nhịp:** **hằng ngày 10' + hằng tuần 15'** (+ làm mới lead magnet mỗi quý).
- **Ai làm:** **người trực lead có TÊN** (🍵 MSX: **Linh — CSKH**) hằng ngày · **chủ DN** review tuần.
- **Input:** Sheet lead (`MSX-Leads`) · Lead Flow Map (T12.4) · bộ 3 tin nhắn (Prompt 4) · file lead magnet PDF.

**Các bước HẰNG NGÀY (10' — chia 2 ca: sáng 8h, tối 21h):**
1. 🟢 *(AUTO — chỉ kiểm)* Mở Sheet → lead mới có tự rơi vào không? Nếu 24h không có dòng nào mà bài vẫn đăng → **form hỏng hoặc CTA không có link** → sửa NGAY, đây là lỗi câm (im lặng làm mất lead mà không ai biết).
2. 🔴 *(NGƯỜI)* Lead mới chưa có trạng thái → **gửi quà trong ca trực** (nếu chưa tự động hoá) → cập nhật `Trạng thái = Đã gửi quà`.
3. 🔴 *(NGƯỜI)* Lead quá 24h chưa follow-up → **gửi tin 24h ĐÚNG BIẾN THỂ theo cột `Phân loại`** → cập nhật trạng thái.
   Thang trạng thái: `Mới → Đã gửi quà → Đã follow-up → Đã hẹn/Đã mua → Không phản hồi`.
4. 🔒 *(Data Security)* Không copy SĐT ra ngoài Sheet. Không chụp màn hình gửi vào group.

**Các bước HẰNG TUẦN (15' — thứ Hai 9h, ghép vào SOP-13):**
5. Đếm 4 số → ghi vào **KPI Sheet (Ngày 13)**:
   `Lượt xem link form` → `Số người điền` (**tỷ lệ chuyển đổi trang**) → `Số người phản hồi tin 24h` → `Số hẹn/đơn`.
6. **Đọc số và chỉnh đúng chỗ:**

| Triệu chứng | Nghĩa là | Sửa ở đâu |
|---|---|---|
| Tỷ lệ điền form **<10%** | Trang không thuyết phục hoặc form quá dài | Sửa **khối 1 (Headline)** + **giảm số trường** |
| Điền nhiều nhưng **không ai phản hồi tin 24h** | Quà kém hoặc tin 24h nghe như bán hàng | Sửa **tin 24h** (mở bằng giá trị) hoặc **ruột lead magnet** |
| Cột `Phân loại` toàn 1 loại | Đang hút sai tệp | Xem lại kênh phân phối (**Ngày 13**) |
| **0 lead suốt tuần dù có đăng bài** | 🔴 **Đứt luồng** | Test lại form bằng điện thoại + kiểm CTA có link không |

**Hằng quý:** làm mới lead magnet — chạy lại **Prompt 1** với dữ liệu **câu hỏi khách MỚI** (lấy từ FAQ Database đã được Tuần 2 nạp dày thêm). *Một lead magnet "mòn" sau 3–6 tháng chạy.*

- **Output:** **100% lead được chạm trong ≤24h** · số liệu chuyển đổi ghi nhận đều · dữ liệu lead luôn ở tầng Restricted.
- **Chi phí vận hành:** ~**1,5h/tuần** — một phần của tổng **~2,5–3h/tuần** vận hành cả cỗ máy Marketing Engine (so với **12h/tuần** founder MSX đang tốn).

---

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm

> 🔴 **CÁCH CHẤM CỦA NGÀY 12 — CHUẨN VÀNG CỦA CẢ CHƯƠNG TRÌNH:**
> **Mentor KHÔNG đọc bản nộp. Mentor BẤM link form của bạn, ĐIỀN THỬ, và lead phải HIỆN trong Sheet.**
> Nghiệm thu bằng **HÀNH ĐỘNG**, không bằng **FILE**. File có thể đẹp mà chết. Form thì hoặc chạy, hoặc không.

| Nhóm | Điểm | Tiêu chí đo được của Ngày 12 |
|---|:---:|---|
| **Đủ tài sản Core** | **30** | 🔴 **Form CHẠY THẬT — mentor bấm link, điền thử, thấy dòng mới trong Sheet: 10đ** *(không hiện = 0đ, không tranh luận)* · Copy đủ **9/9 khối** đúng giới hạn độ dài: 8đ · Lead magnet PDF 4–8 trang (bìa + ruột + **trang CTA**): 7đ · Lead Flow Map đủ **6 trạm**: 3đ · Bộ **3 tin nhắn** đủ: 2đ |
| **Chất lượng & độ sâu** | **30** | 🔗 **TRUY NGUYÊN — ≥8/9 khối có mã nguồn hợp lệ (cột `Mã nguồn` của T12.2): 8đ** · 🔗 **Khối 3 (Vấn đề) dùng LỜI KHÁCH NGUYÊN VĂN `V#` — không phải câu AI đoán: 6đ** · 🔗 **Khối 9 (FAQ) LẤY TỪ FAQ & Objection Database `Q##` (N4), không viết mới: 5đ** · ⚖️ **RANH GIỚI PHÁP LÝ sạch** (không "chữa/khỏi/đặc trị/cam kết 100%", **không khan hiếm giả**): 5đ · Lead magnet đạt **≥16/20** theo bảng T12.1: 4đ · Headline nêu kết quả + đối tượng, ≤14 từ: 2đ |
| **Cá nhân hoá vào DN thật** | **25** | 🔴 **Lead Flow Map có TÊN NGƯỜI THẬT ở mỗi trạm + thời gian cam kết cụ thể: 8đ** *(ghi "nhân viên sẽ follow-up" = 0đ mục này)* · Khối 7 (Bằng chứng) là **dữ liệu thật của DN** (không placeholder, không bịa): 6đ · Ruột lead magnet chứa **≥2 chi tiết chuyên môn** chỉ người trong nghề mới viết được (từ Product Knowledge N4): 6đ · 🔒 **Dòng Data Security trong Lead Flow Map** (lead = Restricted · ai được xem · lưu ở đâu) + ảnh nộp **đã che SĐT**: 5đ |
| **Dùng được ngay** | **15** | 🔴 **Trường phân loại dạng DANH SÁCH CHỌN, 4–5 phương án, phân loại được lead cho CRM Tuần 3: 5đ** *(để tự luận = 0đ)* · Luồng **end-to-end** thông: điền form → thank you → nhận quà đúng kịch bản (mentor test toàn trình): 5đ · Sheet có **4 cột quản trị** (`Nguồn/Phân loại/Trạng thái/Người phụ trách`): 3đ · 3 tầng 🟢/🟡/🔴 ghi rõ trên Map, **tin 24h nằm ở tầng NGƯỜI**: 2đ |

**Mức:** ≥80 Xuất sắc ⭐ · 60–79 Đạt ✅ · 40–59 Cần sửa 🔧 *(sửa trong 24h)* · <40 Làm lại 🔴 *(mentor kèm 1:1)*.

**Lỗi trừ điểm điển hình:**
- ❌ **Form yêu cầu đăng nhập Google / giới hạn 1 phản hồi** — khách thật không điền được (**−10đ**; mentor phát hiện ngay giây đầu khi test).
- ⚖️ ❌ **Landing viết "giúp chữa mất ngủ" / "cam kết hiệu quả" / "chỉ còn 5 suất"** — **−7đ mỗi tuyên bố VÀ KHÔNG ĐƯỢC ĐĂNG** (luật chung Tuần 2).
- 🔗 ❌ **Khối 3 (Vấn đề) là văn AI** (*"Bạn đang mệt mỏi vì giấc ngủ không sâu?"*) thay vì lời khách thật (*"sao đắt hơn trà ngoài siêu thị thế em"*) — **−6đ**. Đây là lỗi phổ biến nhất và là ranh giới giữa content chạm và content nghe tây.
- 🔗 ❌ **Khối 9 (FAQ) tự nghĩ ra** trong khi FAQ Database N4 có sẵn ≥30 cặp câu hỏi thật — **−5đ** (lãng phí tài sản Tuần 1).
- ❌ **Lead magnet không có CTA trang cuối** — quà cho không, không dẫn về offer (**−5đ**).
- ❌ **Landing bán thẳng combo 1.015.000đ** thay vì mời nhận quà — **nhầm tầng phễu** (**−5đ**).
- ❌ **Lead Flow Map ghi "nhân viên sẽ follow-up"**, không tên ai, không thời hạn (**−5đ** — *không có tên người = không ai làm*).
- 🔒 ❌ **Nộp ảnh Sheet còn nguyên SĐT khách** — vi phạm Data Security Rule (**−5đ** + gỡ ngay).
- ❌ **Form 9–10 trường** hỏi cả ngày sinh, địa chỉ nhà — lead rớt vì ngại (**−4đ**).

---

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: Tôi chưa có website/tên miền, có làm được không?**
**A:** **Được 100%.** Google Form có link chia sẻ trực tiếp — dán vào bio TikTok, nút fanpage, comment dưới bài viết, Zalo OA. Landing page đẹp có tên miền là **Bonus**, không phải điều kiện chạy. Rất nhiều DN chạy cả năm chỉ bằng **form + Zalo**. Nhớ nguyên tắc: *form xấu mà chạy thật ăn đứt landing page đẹp còn nằm trên giấy.* (MSX có sẵn `mausonxanh.com` — nhưng nếu bạn chưa có, đừng để nó chặn bạn hôm nay.)

**Q2: Khách Việt ngại để số điện thoại, làm sao tăng tỷ lệ điền?**
**A:** 5 đòn bẩy, theo thứ tự hiệu lực:
1. **Món quà phải ĐÁNG** — không ai tiếc SĐT để đổi lấy thứ họ thèm. Quà kém thì 4 đòn còn lại vô nghĩa.
2. **Giảm còn 5–6 trường.** Mỗi trường thừa = rớt 10–20%.
3. **Dòng trấn an ngay dưới nút:** *"Chỉ nhắn Zalo gửi tài liệu. Không gọi điện nếu bạn không hẹn."* — và **phải giữ đúng lời**.
4. **Giao quà qua Zalo** — người Việt xem Zalo là kênh "nhận đồ" tự nhiên, ít đề phòng hơn email.
5. **FAQ trả lời thẳng nỗi sợ:** đưa hẳn câu *"Có bị gọi điện làm phiền không?"* vào khối 9.

**Q3: Lead magnet của tôi lộ hết bí quyết, khách tự làm rồi không mua nữa?**
**A:** Nỗi sợ kinh điển — và **ngược với sự thật**. Bảng so sánh 10 tiêu chí giúp chị Hương **NHẬN RA** rằng thứ chị đang uống rớt 6/10 — **vấn đề khó hơn chị tưởng**. Người tự giải quyết được **vốn đã không phải khách của bạn**. Người làm theo mà vẫn không xong sẽ **tin bạn nhất**.
Thứ duy nhất cần giữ lại là thứ **không thể tự làm được**: với MSX là **chính lá trà hái ở 800–1.541m** (bạn có cho không cái bảng chấm thì họ cũng không hái được trà); với dịch vụ tư vấn là **phác đồ/lộ trình cá nhân hoá**. **Cho đi CÁI THƯỚC, giữ lại CÁI CÂN.**

**Q4: Nên thu lead về form hay kéo thẳng vào inbox?**
**A:** **Cả hai — tuỳ tầng phễu.** Bài BOF nóng (khách đã muốn mua) → **inbox thẳng**, ít ma sát nhất. Nội dung TOF/MOF (khách chưa sẵn sàng nói chuyện nhưng sẵn sàng nhận quà) → **form + lead magnet**.
Khác biệt cốt tử: **form cho bạn TÀI SẢN DATA** (danh sách chăm sóc dài hạn, có phân loại, dùng được suốt Tuần 3–4). **Inbox không gom lại được** — 3 tháng sau bạn không biết ai đã từng hỏi gì. Hệ thống đủ lông cánh là có **cả hai vòi**.

**Q5: Bao lâu thì có lead thật?**
**A:** Phụ thuộc **traffic** — đó là việc của **[[Ngày 13 — Phân Phối Nội Dung & Content Automation]]**. Kỳ vọng thực tế: đăng đều 2 tuần theo lịch + gắn link form vào **≥2 CTA/tuần** → lead **organic (tự nhiên, không quảng cáo)** đầu tiên trong **7–14 ngày**.
**Muốn có số ngay tối nay:** gửi lead magnet cho **khách CŨ** qua Zalo (MSX có **5.000+ khách**, trong đó tệp #1 là *khách cũ 3 tháng chưa mua lại*). Họ điền form → bạn có **mồi số liệu để test luồng** + họ **chia sẻ cho bạn bè**. Đây là cách rẻ nhất và nhanh nhất.

**Q6: Dùng Google Form hay form của RocketAgent/Ladipage?**
**A:** Luật hôm nay: **công cụ nào bạn dựng xong và TEST THÔNG trong 30 phút thì dùng cái đó.** Google Form là mặc định an toàn. Nếu **RocketAgent** có form/landing → ưu tiên, vì Tuần 3 lead sẽ **chảy thẳng vào CRM + chatbot cùng hệ** (đỡ một lần "chuyển nhà"). **Copy 9 khối dùng được cho MỌI công cụ** — nên bạn không sợ chọn sai. *Công cụ thay được. Copy là tài sản.*

**Q7: Landing page có bắt buộc phải viết mới không?** 🔴
**A:** **KHÔNG — và đây là ý quan trọng nhất hôm nay.** Landing page là **bản LẮP RÁP từ tài sản Tuần 1**: khối 3 lấy từ **5 câu khách nói (N2)** · khối 5 lấy từ **Product Knowledge (N4)** · khối 7 lấy từ **dữ liệu thật (N1/N4)** · khối 8 lấy từ **Core Offer 7 khối (N3)** · khối 9 lấy từ **FAQ Database (N4)**.
Nếu bạn thấy mình đang **NGỒI NGHĨ** thay vì **ĐI LẤY** → bạn đang viết văn, không đang lắp hệ thống. Và nếu Tuần 1 của bạn rỗng đến mức không lắp nổi → **vấn đề nằm ở Tuần 1**, không nằm ở kỹ năng copywriting.

**Q8: Tôi làm B2B, khách không tải PDF thì sao?** 🚀
**A:** Đúng — **đừng ép B2B tải PDF**. Lead magnet B2B mạnh nhất là **buổi demo/audit 30 phút**: khách **thấy tận mắt** hệ thống chạy thật. RocketAI làm đúng vậy: landing **bán buổi demo 30 phút**, **KHÔNG bán gói 25tr** (sai tầng phễu). Form thêm trường **"quy mô nhân sự / doanh thu tháng"** để lọc lead đủ ngân sách **trước khi** đốt 30 phút của founder. Cấu trúc 9 khối, luật truy nguyên, luồng 5 phút vàng: **giữ nguyên**.

---

### 🔴 Lỗi thường gặp

**1. CẦU TOÀN PDF — HẾT GIỜ CHƯA XONG FORM.** *(lỗi số 1, năm nào cũng có)*
- **Phát hiện:** 21h30 vẫn đang chỉnh **màu trang bìa** trên Canva. Chưa mở Google Form lần nào.
- **Vì sao chết:** PDF chậm 1 ngày → **không mất gì**. Form chưa có → **mọi bài đăng, video, visual của cả tuần đều không có nơi đổ về** → mất lead vĩnh viễn.
- **Sửa — THỨ TỰ ĐÚNG:** 🔴 **FORM TRƯỚC (30') → PDF SAU (40', timebox cứng).** Hết 40' là **xuất bản cái đang có**. PDF xấu vẫn giao được quà. *Form xấu mà chạy thật ăn đứt landing page đẹp còn nằm trên giấy.*

**2. Test form bằng máy tính của mình — quên điện thoại và tài khoản khác.**
- **Phát hiện:** khách nhắn *"em không mở được link"* / *"nó bắt đăng nhập"*. Hoặc mentor bấm thử → thấy màn hình "Bạn cần quyền truy cập".
- **Sửa:** **Luôn test bằng ĐIỆN THOẠI + trình duyệt ẩn danh + nhờ 1 người ngoài điền.** Kiểm 3 cài đặt: **tắt** thu thập email · **tắt** giới hạn 1 phản hồi · **tắt** yêu cầu đăng nhập Google.

**3. Khối 3 (Vấn đề) viết bằng văn AI thay vì lời khách.** 🔗
- **Phát hiện:** đọc lên nghe như bài dịch: *"Bạn đang mệt mỏi vì giấc ngủ không sâu và mong muốn tìm một giải pháp tự nhiên?"* — **không một khách hàng nào nói câu đó.**
- **Sửa:** Mở file **5 câu nguyên văn (N2)**. Dán thẳng: *"sao đắt hơn trà ngoài siêu thị thế em"* (`V3`). **Đây là ranh giới giữa content CHẠM và content NGHE TÂY.**

**4. Khối 9 (FAQ) tự nghĩ mới trong khi FAQ Database có sẵn ≥30 cặp.** 🔗
- **Phát hiện:** FAQ toàn câu hỏi "sạch đẹp" mà **không ai từng hỏi** ("Sản phẩm có nguồn gốc rõ ràng không?"), trong khi câu khách thật sự hỏi là *"trà này có chất bảo quản không"* và *"có COD không"*.
- **Sửa:** **Mở FAQ & Objection Database (N4). Copy 5 cặp. Dán vào.** Bạn đã bỏ công cả Tuần 1 để thu 30 câu hỏi thật — **dùng chúng đi.**

**5. Câu phân loại trong form để dạng TỰ LUẬN.**
- **Phát hiện:** cột "vấn đề" trong Sheet toàn câu trả lời lung tung không nhóm được: *"cũng bình thường thôi"*, *"chưa biết"*, *"...."*.
- **Vì sao chết:** **Tuần 3 (CRM) không định tuyến được lead** → phải quay lại hỏi từng người → mất 2 tuần.
- **Sửa:** đổi thành **danh sách chọn 4–5 phương án + 1 "khác"**. Dữ liệu **sạch** cho CRM Tuần 3. *Trường phân loại hôm nay = mầm CRM ngày mai.*

**6. Thank You hứa "gửi ngay trong 5 phút" nhưng không ai trực gửi.**
- **Phát hiện:** lead điền lúc 22h thứ Bảy → **thứ Hai mới nhận quà** → đã nguội, đã mua chỗ khác.
- **Sửa — chọn 1 trong 2, không có đường thứ ba:** ① **Hạ lời hứa cho khớp ca trực** (*"Linh sẽ gửi trong hôm nay, ca trực 8h–22h"*) hoặc ② **làm Bonus tự động hoá** (🟢 Zalo OA/email gửi tự động → giữ đúng lời hứa 5 phút kể cả lúc 2h sáng). **Ghi rõ ca trực vào Lead Flow Map.**

**7. Auto blast tin 24h.** 🔴
- **Phát hiện:** ai đó cài công cụ bắn tin hàng loạt → gửi cùng một tin *"bên em đang có chương trình combo 3 tặng 1"* cho cả người vừa hỏi mua sỉ lẫn người vừa hỏi *"mua tặng mẹ thì nên lấy trà hay viên em nhỉ"* (`V5`).
- **Vì sao chết:** MSX bán bằng **niềm tin vào nguồn gốc**. Một tin nhắn vô hồn phá đúng thứ ta vừa dựng.
- **Sửa:** **Tin 24h nằm ở tầng 🔴 NGƯỜI.** Máy gửi **quà** được. **Người** phải gửi **lời hỏi thăm** — hoặc ít nhất **duyệt từng tin** theo cột `Phân loại` trước khi gửi.

---

## 12. 🔁 Kết Nối

- **Ngày trước:** [[Ngày 11 — AI Video & Audio Factory]] — *video kéo người ĐẾN.*
- **Ngày sau:** [[Ngày 13 — Phân Phối Nội Dung & Content Automation]] — *lịch đăng đẩy người VÀO đây.*
- **Trọng tài thông số:** [[_Chuẩn Đồng Bộ Tuần 2]] · **Về MOC:** [[_MOC 28 Day AIOS]]

**Tài sản Ngày 12 được dùng lại ở đâu:**

| Tài sản hôm nay | Dùng lại ở |
|---|---|
| 🔗 **Link form / landing page** | **[[Ngày 13 — Phân Phối Nội Dung & Content Automation]]** — gắn vào **≥2 CTA/tuần** trong Publishing Calendar 14 ngày. *Mọi con đường nội dung đều đổ về đây.* |
| 🔗 **Luồng form → Sheet** | **Ngày 14 — Demo Day 2**: đây chính là **"luồng vàng"** phải chạy thông trước cả lớp (bấm CTA trên bài đã đăng → form → lead hiện trong Sheet). Đồng thời là **câu 3 của Marketing Gate** — *fail câu 3 = không vào được Tuần 3.* |
| 🔴 **Trường phân loại lead (5 lựa chọn)** | **Tuần 3 — CRM (Ngày 15+)**: chính là **trường phân loại của CRM**. Sheet lead hôm nay là **tiền thân trực tiếp của CRM**. |
| 🔗 **Bộ 3 tin nhắn** | **Tuần 3** — nguyên liệu cho **kịch bản tư vấn + chuỗi follow-up**; 3 biến thể theo phân loại = 3 luồng chăm sóc. |
| 🔗 **Lead magnet PDF** | **Tuần 3 — Chatbot**: dùng làm **"quà mở chuyện"** khi khách inbox. **Tuần 4** — lịch chăm sóc tái sử dụng nội dung này. |
| 🔒 **Dòng Data Security trong Lead Flow Map** | **Tuần 3** — khi lead vào CRM thật, phân quyền đã được quyết định từ hôm nay. |
| 🔗 **Copy 9 khối có mã nguồn** | **Tuần 4** — làm mới landing page/chiến dịch mà **không phải viết lại**: chỉ thay khối 3/9 bằng `V#`/`Q##` mới thu được. |
