---
name: business-model-canvas
description: Phỏng vấn người dùng qua đủ 9 ô của Business Model Canvas / Mô hình kinh doanh 9 ô (Customer Segments, Value Propositions, Channels, Customer Relationships, Revenue Streams, Key Resources, Key Activities, Key Partnerships, Cost Structure) rồi tạo file Markdown tổng quan + sơ đồ trực quan .canvas theo đúng bố cục Osterwalder chuẩn. Dùng skill này bất cứ khi nào người dùng nói "business model canvas", "BMC", "mô hình kinh doanh 9 ô", "9 ô kinh doanh", "canvas kinh doanh", muốn "hệ thống hoá mô hình kinh doanh cho dự án X", "xây/vẽ business model", hoặc mô tả một ý tưởng/dự án kinh doanh và hỏi "mô hình này có ổn không", "giúp tôi làm rõ mô hình kinh doanh" — kể cả khi họ không gọi tên "canvas" hay "9 ô" một cách chính xác.
---

# Business Model Canvas — Phỏng vấn & Tạo File

## Vì sao theo đúng quy trình này

Business Model Canvas (khung Osterwalder) mạnh vì nó buộc người xây dự án trả lời **9 câu hỏi đúng thứ tự kể chuyện**, không phải 9 ô rời rạc. Nếu hỏi lộn xộn, người dùng dễ liệt kê "hoạt động" trước khi biết "khách hàng cần gì" — kết quả là một mô hình đẹp nhưng không ăn khớp. Vì vậy skill này luôn phỏng vấn theo thứ tự: **khách hàng trước (bên phải canvas) → hạ tầng vận hành sau (bên trái canvas) → tài chính chốt lại (dưới cùng)**.

Một mô hình mẫu rất chi tiết (dự án Rocket AI) đã tồn tại trong vault tại `4. Mint/Active/Rocket AI/Business Model Canvas — Rocket AI.md` và `.../Business Model Canvas.canvas` — có thể mở lên xem như ví dụ về độ sâu và văn phong, nhưng **đừng copy nội dung của nó cho dự án khác**, và **đừng ghi đè lên nó** — đó là phân tích thật của một dự án cụ thể, không phải template.

## Quy trình tổng quan

1. Xác định dự án (tên, thư mục lưu, có ghi đè file cũ không)
2. Phỏng vấn lần lượt 9 ô theo bộ câu hỏi chi tiết trong `references/cau-hoi-phong-van.md`
3. Tóm tắt lại toàn bộ 9 ô, cho người dùng xác nhận/sửa trước khi ghi file
4. Sinh 2 file: Markdown tổng quan + `.canvas` trực quan
5. Gợi ý bước tiếp theo (tuỳ chọn)

## Bước 1 — Xác định dự án

Hỏi gọn (không cần hỏi tách rời từng cái, có thể gộp 1 lượt):
- Tên dự án/công ty là gì?
- Mô tả 1-2 câu: đang làm gì, giai đoạn nào (ý tưởng / MVP / đã có doanh thu / đang mở rộng)?
- Lưu ở đâu? Mặc định theo quy ước vault này: `4. Mint/Active/[Tên dự án]/` (xem CLAUDE.md gốc). Nếu dự án đã có thư mục trong `4. Mint/`, dùng thư mục đó.
- Có `_MOC [Tên dự án].md` hay note tổng quan dự án nào để link `up:` trong frontmatter không?

**Luôn kiểm tra trước khi ghi file** — dùng `ls`/Read trên thư mục đích trước. Nếu `Business Model Canvas — [Tên dự án].md` hoặc `Business Model Canvas.canvas` đã tồn tại, KHÔNG ghi đè âm thầm: cho người dùng xem file cũ tồn tại và hỏi họ muốn ghi đè, tạo bản mới với tên khác, hay merge nội dung.

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

Nếu dự án có nhiều phân khúc khách hàng hoặc nhiều giá trị cốt lõi chồng lấn (ví dụ nền tảng đa mảng), hỏi người dùng có muốn **gắn nhãn ưu tiên** cho từng mục không (ví dụ 🥇 làm ngay / 🥈 kế tiếp / 🥉 dài hạn, hoặc số thứ tự 1/2/3). Chỉ gắn nhãn khi người dùng đã xác nhận có/không — đừng tự suy ra nhãn ưu tiên chỉ vì câu trả lời của họ có chữ như "làm ngay"/"để sau"; nếu câu hỏi này chưa được hỏi hoặc chưa trả lời rõ, cứ để phần đó ở dạng văn xuôi thường, không gắn 🥇🥈🥉.

## Bước 3 — Tóm tắt & xác nhận

Trước khi ghi file, tóm tắt lại toàn bộ 9 ô bằng gạch đầu dòng ngắn gọn (mỗi ô 2-5 dòng) và hỏi người dùng xác nhận hoặc sửa. File `.md` và `.canvas` khó chỉnh sửa lại bằng tay sau này (đặc biệt `.canvas` là JSON), nên tốt hơn là sửa ở bước tóm tắt trước khi ghi.

## Bước 4 — Sinh file

### File Markdown tổng quan

Đường dẫn: `[thư mục dự án]/Business Model Canvas — [Tên dự án].md`

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
- [[_MOC Tên Dự Án]]  (nếu có)
- [[Business Model Canvas.canvas|Xem sơ đồ trực quan]]
```

Viết nội dung từng ô dựa trên câu trả lời phỏng vấn thực tế — không tự thêm chi tiết người dùng chưa nói. Nếu người dùng trả lời sơ sài ở một ô, cứ viết ngắn, đừng bịa cho "đầy đủ".

### File .canvas (sơ đồ trực quan)

Đường dẫn: `[thư mục dự án]/Business Model Canvas.canvas`

Dùng `assets/canvas-layout-template.json` làm khung toạ độ — đây là bố cục chuẩn Osterwalder (Key Partnerships / Key Activities + Key Resources / Value Propositions / Customer Relationships + Channels / Customer Segments ở hàng trên, Cost Structure + Revenue Streams ở hàng dưới), đã test hiển thị đẹp trong Obsidian. Copy file này, giữ nguyên toạ độ `x/y/width/height`, chỉ thay nội dung `text` của từng node bằng bản tóm tắt 3-6 dòng của khối tương ứng (ngắn hơn nhiều so với bản Markdown — canvas là bản nhìn nhanh, không phải bản đầy đủ). Thêm 1 node tiêu đề ở trên cùng ghi tên dự án + link `[[Business Model Canvas — Tên Dự Án]]` để mở bản chi tiết.

Toạ độ trong template là điểm khởi đầu, không phải khuôn cứng: nếu một ô có nhiều phân khúc/giá trị khác nhau (ví dụ Customer Segments hoặc Value Propositions có 2-3 nhóm rõ rệt), gộp chúng thành các dòng ngắn có tiêu đề phụ trong cùng 1 node (không tạo thêm node) — và nếu nội dung thật sự cần nhiều chỗ hơn, cứ tăng `height` của node đó (và các node cùng cột nếu cần dịch xuống) thay vì nhồi nhét gây tràn chữ trong Obsidian.

Nếu cần ôn lại cú pháp JSON Canvas (node, edge, color, id), tham khảo skill `json-canvas` có sẵn trong vault.

Không cần thêm các node đánh giá/rủi ro/kế hoạch gọi vốn như file mẫu Rocket AI — đó là phần mở rộng riêng của dự án đó, không thuộc 9 ô canvas chuẩn.

## Bước 5 — Gợi ý bước tiếp theo (tuỳ chọn)

Nếu Customer Segments hoặc Value Propositions có từ **4 mục trở lên**, mỗi mục đều đủ nội dung riêng để đứng thành 1 trang (không phải chỉ 1 dòng), có thể gợi ý — không tự làm trừ khi được yêu cầu — tách thành các file con riêng theo mẫu thư mục `MHKD/` trong dự án Rocket AI (mỗi phân khúc/giá trị 1 file, `_MOC` phụ liệt kê). Dưới ngưỡng đó, 2 file chính (Markdown + canvas) là đủ, không cần đề xuất thêm.
