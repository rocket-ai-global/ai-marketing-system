---
name: mo-hinh-kinh-doanh
description: Phỏng vấn người dùng qua đủ 9 ô của Business Model Canvas / Mô hình kinh doanh 9 ô (Customer Segments, Value Propositions, Channels, Customer Relationships, Revenue Streams, Key Resources, Key Activities, Key Partnerships, Cost Structure) rồi tạo file Markdown tổng quan + sơ đồ trực quan .canvas theo đúng bố cục Osterwalder chuẩn. Dùng skill này bất cứ khi nào người dùng nói "business model canvas", "BMC", "mô hình kinh doanh 9 ô", "9 ô kinh doanh", "canvas kinh doanh", muốn "hệ thống hoá mô hình kinh doanh cho dự án X", "xây/vẽ business model", hoặc mô tả một ý tưởng/dự án kinh doanh và hỏi "mô hình này có ổn không", "giúp tôi làm rõ mô hình kinh doanh" — kể cả khi họ không gọi tên "canvas" hay "9 ô" một cách chính xác.
---

# Business Model Canvas — Phỏng vấn & Tạo File

## Vì sao theo đúng quy trình này

Business Model Canvas (khung Osterwalder) mạnh vì nó buộc người xây dự án trả lời **9 câu hỏi đúng thứ tự kể chuyện**, không phải 9 ô rời rạc. Nếu hỏi lộn xộn, người dùng dễ liệt kê "hoạt động" trước khi biết "khách hàng cần gì" — kết quả là một mô hình đẹp nhưng không ăn khớp. Vì vậy skill này luôn phỏng vấn theo thứ tự: **khách hàng trước (bên phải canvas) → hạ tầng vận hành sau (bên trái canvas) → tài chính chốt lại (dưới cùng)**.

Một mô hình mẫu rất chi tiết (dự án Rocket AI) đã tồn tại trong vault tại `4. Mint/Active/Rocket AI/Business Model Canvas — Rocket AI.md` và `.../Business Model Canvas.canvas` — có thể mở lên xem như ví dụ về độ sâu và văn phong, nhưng **đừng copy nội dung của nó cho dự án khác**, và **đừng ghi đè lên nó** — đó là phân tích thật của một dự án cụ thể, không phải template.

## Quy trình tổng quan

1. Xác định dự án (tên, thư mục lưu, có ghi đè file cũ không)
2. Phỏng vấn lần lượt 9 ô theo bộ câu hỏi chi tiết trong `references/cau-hoi-phong-van.md` — riêng Customer Segments và Value Propositions luôn đào sâu thêm theo phần "Đào sâu thêm để dựng trang chi tiết" của mỗi ô
3. Tóm tắt lại toàn bộ 9 ô, cho người dùng xác nhận/sửa trước khi ghi file
4. Sinh 2 file chính: Markdown tổng quan + `.canvas` trực quan
5. Sinh trang chi tiết riêng cho MỖI phân khúc khách hàng và MỖI giá trị cốt lõi (thư mục `MHKD/`) — mặc định luôn làm, không phải tuỳ chọn
6. Sinh file Đánh Giá Mô Hình Kinh Doanh
7. Gợi ý bước tiếp theo (tuỳ chọn)

## Bước 1 — Xác định dự án và chế độ vault

**Trước tiên xác định vault đang ở chế độ nào** — đây quyết định toàn bộ đường dẫn lưu file ở các bước sau:

- **Chế độ 1 công ty (root singleton)** — vault đại diện cho ĐÚNG 1 doanh nghiệp duy nhất (không phải nơi quản lý nhiều dự án/công ty khác nhau). Nhận diện bằng cách kiểm tra thư mục `00. Business Context/` ở gốc vault đã có sẵn `Chân Dung Doanh Nghiệp.md`, `AI-Sale-Assistant.md`, hoặc `Business Model Canvas — [Tên Doanh Nghiệp].md` (kể cả còn là file mẫu trống) chưa — nếu có, đây là chế độ này. `CLAUDE.md` ở gốc vault (nếu có) cũng sẽ nói rõ điều này.
  → Ở chế độ này: BMC là **thông tin dùng chung cho toàn bộ vault**, không phải tài liệu của một dự án con. Tất cả file (Markdown, `.canvas`, thư mục `MHKD/`, file đánh giá) đều nằm **trong `00. Business Context/`** ở gốc vault, không tạo thư mục dự án riêng. Nếu `Business Model Canvas — [Tên Doanh Nghiệp].md` đang là bản mẫu trống (placeholder), đây chính là file cần điền — hỏi tên công ty thật để đổi tên file placeholder, đừng tạo file mới song song.
- **Chế độ nhiều dự án (per-project subfolder)** — vault quản lý nhiều dự án/công ty khác nhau (ví dụ có cấu trúc `4. Mint/Active/[Tên dự án]/` với nhiều dự án). Ở chế độ này, mỗi lần chạy skill là cho MỘT dự án/công ty cụ thể, lưu trong thư mục riêng của dự án đó.

Nếu không chắc chế độ nào (vd vault mới, chưa có gì), hỏi thẳng người dùng: "Vault này chỉ dùng cho 1 công ty duy nhất, hay quản lý nhiều dự án/công ty khác nhau?"

Sau khi xác định chế độ, hỏi gọn (không cần hỏi tách rời từng cái, có thể gộp 1 lượt):
- Tên công ty/dự án là gì?
- Mô tả 1-2 câu: đang làm gì, giai đoạn nào (ý tưởng / MVP / đã có doanh thu / đang mở rộng)?
- **Chỉ hỏi nếu ở chế độ nhiều dự án:** lưu ở đâu? Mặc định theo quy ước `4. Mint/Active/[Tên dự án]/` (xem CLAUDE.md gốc). Nếu dự án đã có thư mục trong `4. Mint/`, dùng thư mục đó. Có `_MOC [Tên dự án].md` hay note tổng quan dự án nào để link `up:` trong frontmatter không?

**Luôn kiểm tra trước khi ghi file** — dùng `ls`/Read trên thư mục đích trước (`00. Business Context/` ở chế độ 1 công ty, hoặc thư mục dự án ở chế độ nhiều dự án). Nếu `Business Model Canvas — [Tên].md`, `Business Model Canvas.canvas`, thư mục `MHKD/`, hoặc `Đánh Giá Mô Hình Kinh Doanh — [Tên].md` đã tồn tại VÀ đã có nội dung thật (không phải file mẫu trống), KHÔNG ghi đè âm thầm: cho người dùng xem file/thư mục cũ tồn tại và hỏi họ muốn ghi đè, tạo bản mới với tên khác, hay merge nội dung. Nếu file cũ chỉ là bản mẫu trống (placeholder chưa điền), cứ điền thẳng vào đó, không cần hỏi.

## Bước 2 — Phỏng vấn 9 ô

Mở `references/cau-hoi-phong-van.md` để lấy bộ câu hỏi đầy đủ cho từng ô. Thứ tự phỏng vấn:

1. **Customer Segments** (Phân khúc khách hàng)
2. **Value Propositions** (Giá trị cốt lõi)
3. **Channels** (Kênh phân phối)
4. **Customer Relationships** (Quan hệ khách hàng)
5. **Revenue Streams** (Dòng doanh thu)
6. **Key Resources** (Nguồn lực chính)
7. **Key Activities** (Hoạt động chính)
8. **Key Partnerships** (Đối tác chính)
9. **Cost Structure** (Cơ cấu chi phí)

Cách hỏi: trình bày các câu hỏi của MỘT ô trong một lượt (đừng hỏi từng câu một rồi chờ — quá chậm), để người dùng trả lời tự do bằng đoạn văn. Các câu hỏi phụ trong file reference là để **đào sâu**, không phải checklist bắt buộc — nếu câu trả lời đầu đã đủ rõ và cụ thể, đừng ép hỏi hết mọi câu con. Chỉ hỏi thêm khi câu trả lời còn chung chung (ví dụ "khách hàng là doanh nghiệp" — hỏi thêm quy mô nào, ngành nào, ai là người ký hợp đồng).

**Ngoại lệ — Customer Segments và Value Propositions luôn cần hỏi kỹ hơn 7 ô còn lại.** Hai ô này sẽ được tách thành trang chi tiết riêng ở Bước 5 (persona, quy mô thị trường, jobs-to-be-done, hành vi mua, CAC/LTV, phản đối & rủi ro cho Customer Segments; cấu phần sản phẩm, so sánh lựa chọn thay thế, logic giá, bằng chứng, phản đối & rủi ro cho Value Propositions — xem mục "Đào sâu thêm để dựng trang chi tiết" trong file reference). Vẫn áp dụng nguyên tắc "đừng bịa nếu người dùng chưa nói" — nếu người dùng không có số liệu thị trường hay chưa nghĩ tới CAC/LTV, cứ hỏi 1 lượt rồi chấp nhận câu trả lời "chưa biết/chưa đo", đánh dấu `⚠️ giả định` khi phải tự ước lượng thay vì ép người dùng bịa số hoặc bỏ qua câu hỏi hoàn toàn.

Nếu dự án có nhiều phân khúc khách hàng hoặc nhiều giá trị cốt lõi chồng lấn (ví dụ nền tảng đa mảng), hỏi người dùng có muốn **gắn nhãn ưu tiên** cho từng mục không (ví dụ 🥇 làm ngay / 🥈 kế tiếp / 🥉 dài hạn, hoặc số thứ tự 1/2/3). Chỉ gắn nhãn khi người dùng đã xác nhận có/không — đừng tự suy ra nhãn ưu tiên chỉ vì câu trả lời của họ có chữ như "làm ngay"/"để sau"; nếu câu hỏi này chưa được hỏi hoặc chưa trả lời rõ, cứ để phần đó ở dạng văn xuôi thường, không gắn 🥇🥈🥉.

## Bước 3 — Tóm tắt & xác nhận

Trước khi ghi file, tóm tắt lại toàn bộ 9 ô bằng gạch đầu dòng ngắn gọn (mỗi ô 2-5 dòng) và hỏi người dùng xác nhận hoặc sửa. File `.md` và `.canvas` khó chỉnh sửa lại bằng tay sau này (đặc biệt `.canvas` là JSON), nên tốt hơn là sửa ở bước tóm tắt trước khi ghi.

## Bước 4 — Sinh file

### File Markdown tổng quan

**Chế độ 1 công ty:** đường dẫn `00. Business Context/Business Model Canvas — [Tên Doanh Nghiệp].md` (điền vào file placeholder có sẵn nếu đang trống, đổi `[Tên Doanh Nghiệp]` trong tên file thành tên thật).

Frontmatter (khớp quy ước file identity gốc của vault này — xem `Chân Dung Doanh Nghiệp.md` để đối chiếu):
```yaml
---
tags: [identity, business-model]
created: YYYY-MM-DD
---
```
Không có `rank`/`deadline`/`up` — đây là file định danh dùng chung cho cả vault, không phải một task/dự án có deadline hay nằm dưới một `_MOC` nào.

**Chế độ nhiều dự án:** đường dẫn `[thư mục dự án]/Business Model Canvas — [Tên dự án].md`.

Frontmatter (theo quy ước MINT của vault):
```yaml
---
tags: [mint, business-model]
rank: 3
deadline:
created: YYYY-MM-DD
up:
  - "[[_MOC Tên Dự Án]]"
---
```
(`rank` hỏi người dùng 1-5 nếu quan trọng, mặc định 3 nếu không có ý kiến; `deadline` để trống nếu chưa có hạn, chỉ điền nếu đây là việc Active có hạn cụ thể; `up` — nếu có `_MOC [Tên dự án].md` thì thêm key này với đúng link, còn nếu không có, XOÁ HẲN dòng `up:` khỏi frontmatter thay vì để trống — đừng tự bịa link, và đừng để lại một key rỗng không có tác dụng.)

Cấu trúc body — mỗi khối là 1 heading, đặt tên **tiếng Anh kèm tiếng Việt trong ngoặc** (quy ước CLAUDE.md của vault này):

```markdown
# 📊 Business Model Canvas — [Tên dự án]

> [Mô tả 1-2 câu về dự án + giai đoạn hiện tại]

---

## 👥 Customer Segments (Phân khúc khách hàng)
...

## 🎁 Value Propositions (Giá trị cốt lõi)
...

## 📢 Channels (Kênh phân phối)
...

## ❤️ Customer Relationships (Quan hệ khách hàng)
...

## 💰 Revenue Streams (Dòng doanh thu)
...

## 🧱 Key Resources (Nguồn lực chính)
...

## ⚙️ Key Activities (Hoạt động chính)
...

## 🤝 Key Partnerships (Đối tác chính)
...

## 💸 Cost Structure (Cơ cấu chi phí)
...

---

## 🔗 Kết nối với
- [[_MOC Tên Dự Án]]  (chỉ ở chế độ nhiều dự án, nếu có)
- [[Chân Dung Doanh Nghiệp]] · [[Brand Voice — Giọng Thương Hiệu]] · [[AI-Sale-Assistant]] · [[_MOC Sản Phẩm & Dịch Vụ]]  (chỉ ở chế độ 1 công ty — các file identity cùng tầng trong `00. Business Context/`)
- [[Business Model Canvas.canvas|Xem sơ đồ trực quan]]
- [[_MHKD Tên — Tổng Quan]]  (trang chi tiết Customer Segments & Value Propositions — sinh ở Bước 5)
- [[Đánh Giá Mô Hình Kinh Doanh — Tên]]  (sinh ở Bước 6)
```

Viết nội dung từng ô dựa trên câu trả lời phỏng vấn thực tế — không tự thêm chi tiết người dùng chưa nói. Nếu người dùng trả lời sơ sài ở một ô, cứ viết ngắn, đừng bịa cho "đầy đủ". Trong ô Customer Segments và Value Propositions, mỗi phân khúc/giá trị nêu tên cũng nên kèm link tới trang chi tiết tương ứng (vd `[[PK1 — Tên Phân Khúc]]`) — các trang này được tạo ở Bước 5, nên viết link trước rồi tạo file sau trong cùng lượt làm việc. Ở chế độ 1 công ty, nếu `Chân Dung Doanh Nghiệp.md` cũng đang trống, tận dụng luôn câu trả lời phỏng vấn (đặc biệt Customer Segments → ICP, Value Propositions → giá trị cốt lõi) để gợi ý điền nốt file đó — nhưng hỏi trước khi ghi đè, đừng tự ý sửa file khác ngoài phạm vi skill này.

### File .canvas (sơ đồ trực quan)

Đường dẫn: `00. Business Context/Business Model Canvas.canvas` (chế độ 1 công ty) hoặc `[thư mục dự án]/Business Model Canvas.canvas` (chế độ nhiều dự án).

Dùng `assets/canvas-layout-template.json` làm khung toạ độ — đây là bố cục chuẩn Osterwalder (Key Partnerships / Key Activities + Key Resources / Value Propositions / Customer Relationships + Channels / Customer Segments ở hàng trên, Cost Structure + Revenue Streams ở hàng dưới), đã test hiển thị đẹp trong Obsidian. Copy file này, giữ nguyên toạ độ `x/y/width/height`, chỉ thay nội dung `text` của từng node bằng bản tóm tắt 3-6 dòng của khối tương ứng (ngắn hơn nhiều so với bản Markdown — canvas là bản nhìn nhanh, không phải bản đầy đủ). Thêm 1 node tiêu đề ở trên cùng ghi tên dự án + link `[[Business Model Canvas — Tên Dự Án]]` để mở bản chi tiết.

Toạ độ trong template là điểm khởi đầu, không phải khuôn cứng: nếu một ô có nhiều phân khúc/giá trị khác nhau (ví dụ Customer Segments hoặc Value Propositions có 2-3 nhóm rõ rệt), gộp chúng thành các dòng ngắn có tiêu đề phụ trong cùng 1 node (không tạo thêm node) — và nếu nội dung thật sự cần nhiều chỗ hơn, cứ tăng `height` của node đó (và các node cùng cột nếu cần dịch xuống) thay vì nhồi nhét gây tràn chữ trong Obsidian.

Nếu cần ôn lại cú pháp JSON Canvas (node, edge, color, id), tham khảo skill `json-canvas` có sẵn trong vault.

Không cần thêm các node đánh giá/rủi ro/kế hoạch gọi vốn như file mẫu Rocket AI — đó là phần mở rộng riêng của dự án đó, không thuộc 9 ô canvas chuẩn.

## Bước 5 — Trang chi tiết Customer Segments & Value Propositions

Đây là bước **mặc định, luôn làm**, không còn là gợi ý tuỳ chọn — mỗi phân khúc khách hàng và mỗi giá trị cốt lõi đều có 1 file riêng, dựa theo cấu trúc chi tiết của dự án mẫu Rocket AI (`4. Mint/Active/Rocket AI/MHKD/`), nhưng KHÔNG copy nội dung mẫu đó, chỉ theo cấu trúc.

### Thư mục

Chế độ 1 công ty: `MHKD/` nằm trong **`00. Business Context/`**. Chế độ nhiều dự án: `MHKD/` nằm trong thư mục dự án.

```
[00. Business Context/, hoặc thư mục dự án]/MHKD/
  _MHKD [Tên] — Tổng Quan.md
  Phân Khúc Khách Hàng/
    PK1 — [Tên phân khúc 1].md
    PK2 — [Tên phân khúc 2].md
    ...
  Giá Trị Cốt Lõi/
    GT1 — [Tên giá trị 1].md
    GT2 — [Tên giá trị 2].md
    ...
```

Đánh số PK/GT theo đúng thứ tự ưu tiên đã chốt ở Bước 2 (nếu có gắn nhãn 🥇🥈🥉); nếu không có nhãn ưu tiên, đánh số theo thứ tự liệt kê tự nhiên trong lúc phỏng vấn.

**Frontmatter ở chế độ 1 công ty:** các template trong `assets/` (`mhkd-*.md`) dùng `tags: [mint, business-model, ...]` và `up: [[_MHKD {{TEN_DU_AN}} — Tổng Quan]]` — tiền tố `mint` là quy ước riêng của vault nhiều dự án (kiểu `4. Mint`), KHÔNG áp dụng ở chế độ 1 công ty. Khi điền, đổi `tags` thành `[identity, customer-segment]` / `[identity, value-proposition]` / `[identity, moc]` cho khớp quy ước file identity gốc của vault này, và bỏ hẳn `rank`/`deadline` nếu template có (các file identity không cần các trường này).

### Cách sinh từng file

- **Mỗi phân khúc:** copy `assets/mhkd-customer-segment-template.md`, điền bằng câu trả lời phỏng vấn thật (đặc biệt phần "Đào sâu thêm" của ô Customer Segments). Nếu người dùng chưa trả lời một mục nào đó (vd quy mô thị trường, CAC, LTV), **để mục đó ngắn gọn "chưa có dữ liệu" hoặc gắn `⚠️ giả định` cho phần AI tự ước lượng** — tuyệt đối không bịa số cụ thể để trông "đầy đủ".
- **Mỗi giá trị cốt lõi:** copy `assets/mhkd-value-proposition-template.md`, điền tương tự dựa trên phần "Đào sâu thêm" của ô Value Propositions, và link tới đúng phân khúc chính/phụ tương ứng.
- **File hub tổng quan:** copy `assets/mhkd-tong-quan-template.md`, điền bảng liệt kê tất cả PK/GT kèm mức ưu tiên (nếu có) và mô tả 1 dòng.
- Với dự án chỉ có 1 phân khúc và 1 giá trị cốt lõi duy nhất, vẫn tạo đủ cấu trúc trên — file sẽ ngắn hơn tương ứng với lượng thông tin thật có, không cần ép đủ 15/12 mục nếu người dùng không có gì để nói ở mục đó.
- Sau khi tạo xong, quay lại file Markdown tổng quan (Bước 4) để đảm bảo các link `[[PK1 — ...]]` / `[[GT1 — ...]]` trong ô Customer Segments/Value Propositions đã trỏ đúng tên file vừa tạo.

## Bước 6 — Đánh giá mô hình kinh doanh

Đây cũng là bước **mặc định, luôn làm** sau khi đã có đủ dữ liệu từ Bước 4 và Bước 5.

Đường dẫn: `00. Business Context/Đánh Giá Mô Hình Kinh Doanh — [Tên].md` (chế độ 1 công ty) hoặc `[thư mục dự án]/Đánh Giá Mô Hình Kinh Doanh — [Tên dự án].md` (chế độ nhiều dự án).

Copy `assets/danh-gia-mo-hinh-kinh-doanh-template.md` và điền dựa trên chính nội dung vừa dựng — đây là đánh giá về **tính nhất quán giữa 9 ô, tính khả thi, và bằng chứng Product-Market Fit**, không phải chấm điểm ý tưởng chung chung. Khác với file audit của Rocket AI (vốn so sánh nhiều tài liệu tài chính mâu thuẫn nhau — Excel, pitch deck, kế hoạch...), ở đây thường chỉ có MỘT bộ canvas vừa dựng, nên trọng tâm là:

1. Soi từng cặp ô có ăn khớp logic với nhau không (vd: Value Propositions có thực sự giải đúng pain point của Customer Segments không, Revenue Streams có khớp với hành vi mua đã mô tả không).
2. Tính khả thi tài chính thô — chỉ tính toán nếu người dùng đã cung cấp số liệu cụ thể (vốn, giá, chi phí); nếu chưa có, ghi rõ "chưa đủ dữ liệu để đánh giá" thay vì tự bịa con số.
3. Mức độ bằng chứng PMF thực tế — đa số dự án mới sẽ ở mức "giả thuyết, chưa có bằng chứng", cứ nói thẳng điều đó.
4. Chấm điểm theo bảng tiêu chí trong template, và liệt kê việc cần làm tiếp theo.

Sau khi viết xong, quay lại thêm link `[[Đánh Giá Mô Hình Kinh Doanh — Tên Dự Án]]` vào mục "Kết nối với" của file Markdown tổng quan nếu chưa có (đã có sẵn trong template ở Bước 4).

**Frontmatter ở chế độ 1 công ty:** tương tự Bước 5 — đổi `tags` của `assets/danh-gia-mo-hinh-kinh-doanh-template.md` thành `[identity, review]`, bỏ dòng `up: [[_MOC {{TEN_DU_AN}}]]` vì không có `_MOC` nào trong `00. Business Context/` ở chế độ này.

## Bước 7 — Gợi ý bước tiếp theo (tuỳ chọn)

Nếu đánh giá ở Bước 6 phát hiện rủi ro 🔴 nghiêm trọng hoặc điểm trung bình thấp, có thể gợi ý — không tự làm trừ khi được yêu cầu — các việc như: phỏng vấn sâu thêm một phân khúc cụ thể, chạy thử nghiệm để thu thập bằng chứng PMF, hoặc tách các ô còn lại (Channels, Revenue Streams...) thành file riêng nếu chúng cũng đủ phức tạp để đứng thành 1 trang.
