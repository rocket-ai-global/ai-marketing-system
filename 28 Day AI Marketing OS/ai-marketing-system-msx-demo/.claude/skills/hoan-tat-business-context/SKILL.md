---
name: hoan-tat-business-context
description: Kiểm tra và hoàn tất toàn bộ phần Business Context của vault SME — quét `00. Business Context/` xem còn thiếu file identity nào, hỏi người dùng cung cấp, nếu người dùng "không biết" thì chuyển sang phỏng vấn gợi mở rồi lưu vào đúng file. Bổ trợ cho `mo-hinh-kinh-doanh` (skill kia lo 9 ô Business Model Canvas + PK/GT; skill này lo các file identity còn lại: Chân Dung Doanh Nghiệp, Brand Voice, Chân Dung CEO, AI-Sale-Assistant, Sản Phẩm & Dịch Vụ). Dùng skill này khi người dùng nói "hoàn tất business context", "hoàn thiện hồ sơ doanh nghiệp", "business context còn thiếu gì", "điền nốt ngữ cảnh doanh nghiệp", "kiểm tra thông tin doanh nghiệp đã đủ chưa", "audit business context", "complete business context", "setup hồ sơ công ty", "vault còn thiếu context gì để AI hiểu doanh nghiệp".
---

# Hoàn Tất Business Context — Audit & Điền Nốt Hồ Sơ Doanh Nghiệp

## Skill này để làm gì

Vault này là AI Brain cho **DUY NHẤT 1 doanh nghiệp SME** (chế độ "1 công ty / root singleton"). Mọi ngữ cảnh nền tảng nằm trong **`00. Business Context/`** ở gốc vault — đó là nguồn sự thật duy nhất mà mọi skill sale/marketing khác (`phan-tich-doi-thu`, `thiet-ke-offer`, `thu-nghiem-ab`, `kiem-tra-seo`, `do-luong-tracking`...) đọc trước khi chạy. Nếu các file này còn trống, những skill đó phải hỏi lại người dùng hoặc tự bịa.

Skill này **quét trạng thái từng file identity, chỉ ra cái gì còn thiếu, rồi hỏi/phỏng vấn để điền nốt** — để phần Business Context hoàn chỉnh, các skill sau chạy trơn.

## Ranh giới với `/mo-hinh-kinh-doanh` (đọc kỹ — tránh trùng lặp)

| Việc | Skill lo |
|---|---|
| 9 ô Business Model Canvas (`Business Model Canvas — [Tên].md` + `.canvas`) | **`/mo-hinh-kinh-doanh`** |
| Trang chi tiết `MHKD/Phân Khúc Khách Hàng/PK*.md` và `MHKD/Giá Trị Cốt Lõi/GT*.md` | **`/mo-hinh-kinh-doanh`** |
| `Đánh Giá Mô Hình Kinh Doanh — [Tên].md` | **`/mo-hinh-kinh-doanh`** |
| `Chân Dung Doanh Nghiệp.md` (định vị, ICP) | **skill này** |
| `Brand Voice — Giọng Thương Hiệu.md` | **skill này** |
| `Chân Dung CEO — [Tên].md` (personal brand CEO, CÓ ĐIỀU KIỆN) | **skill này** |
| `AI-Sale-Assistant.md` | **skill này** |
| `Sản Phẩm & Dịch Vụ/` (≥1 sản phẩm thật) | **skill này** |

→ Với các mục thuộc `/mo-hinh-kinh-doanh`, skill này **KHÔNG tự phỏng vấn lại**, chỉ audit trạng thái và **hướng dẫn người dùng chạy `/mo-hinh-kinh-doanh`**. Skill này lo các file identity còn lại. (Ghi chú: `Chân Dung Doanh Nghiệp.md` có phần trùng dữ liệu với BMC — nếu người dùng vừa chạy `/mo-hinh-kinh-doanh`, tận dụng câu trả lời đó để điền, đừng bắt họ trả lời lại từ đầu.)

## Quy trình

### Bước 1 — AUDIT (luôn làm đầu tiên)

Trước khi hỏi bất cứ điều gì, quét `00. Business Context/` và chấm trạng thái từng mục. Dùng `ls`/Read để kiểm tra thực tế — **đừng đoán**. Cách chấm:

- ✅ **Đầy đủ** — file có nội dung thật, không còn placeholder trống.
- ⚠️ **Có file nhưng còn placeholder-trống** — nhận diện bằng các dấu: còn chữ `[Tên]` / `[Tên Doanh Nghiệp]` trong tên file hoặc heading; các mục gạch đầu dòng để rỗng (dòng chỉ có `-` hoặc `- <nhãn>:` không có giá trị); bảng có ô trống; câu mở đầu vẫn là hướng dẫn mẫu chưa thay bằng nội dung thật.
- ❌ **Chưa có** — file/thư mục không tồn tại.

Các mục cần chấm:

1. `Chân Dung Doanh Nghiệp.md` — định vị, ICP.
2. `Brand Voice — Giọng Thương Hiệu.md` — giọng, từ nên/tránh dùng, câu mẫu, do/don't.
3. `Chân Dung CEO — [Tên].md` — **CÓ ĐIỀU KIỆN** (xem Bước 1b). File template ĐÃ tồn tại sẵn — chỉ audit + phỏng vấn điền, **KHÔNG tạo lại**.
4. `AI-Sale-Assistant.md` — vai trò & nguyên tắc phản hồi của AI.
5. `Sản Phẩm & Dịch Vụ/` — có ≥1 file sản phẩm THẬT (không tính file `[Ví dụ] Gói Basic.md`).
6. *(BMC — giao `/mo-hinh-kinh-doanh`)* `Business Model Canvas — [Tên].md` + `Business Model Canvas.canvas`.
7. *(BMC — giao `/mo-hinh-kinh-doanh`)* `MHKD/Phân Khúc Khách Hàng/PK*.md` và `MHKD/Giá Trị Cốt Lõi/GT*.md`.
8. *(BMC — giao `/mo-hinh-kinh-doanh`)* `Đánh Giá Mô Hình Kinh Doanh — [Tên].md`.

In ra một **checklist gọn** cho người dùng, đánh dấu rõ mục nào skill này lo, mục nào giao `/mo-hinh-kinh-doanh`. Ví dụ:

```
📋 Trạng thái Business Context

Skill này lo:
  ⚠️ Chân Dung Doanh Nghiệp — có file, còn nhiều mục trống
  ❌ Brand Voice — chưa điền
  ⚠️ Chân Dung CEO — (cần xác nhận: công ty có phụ thuộc brand cá nhân không?)
  ✅ AI-Sale-Assistant — đã đủ
  ❌ Sản Phẩm & Dịch Vụ — mới chỉ có file [Ví dụ]

Giao cho /mo-hinh-kinh-doanh:
  ❌ Business Model Canvas (9 ô) + .canvas
  ❌ MHKD/ (trang chi tiết PK/GT)
  ❌ Đánh Giá Mô Hình Kinh Doanh
```

### Bước 1b — Xác nhận có cần Chân Dung CEO không

`Chân Dung CEO` chỉ **bắt buộc nếu công ty phụ thuộc brand cá nhân của CEO/founder** (khách mua vì tin con người trước khi tin công ty). **Trước khi coi nó là "thiếu", HỎI người dùng:** "Thương hiệu của bạn có gắn liền với cá nhân người sáng lập/CEO không (khách biết đến qua Facebook/TikTok cá nhân, mua vì tin CEO)?"

- Nếu **có** → coi `Chân Dung CEO` là mục cần hoàn tất, phỏng vấn như các file khác.
- Nếu **không** → đánh dấu "không áp dụng (N/A)", bỏ qua, không tính là thiếu.

### Bước 2 — Chọn thứ tự & xác nhận với người dùng

Sau khi in checklist, hỏi người dùng muốn bắt đầu từ mục nào. Nếu họ không có ý kiến, đề xuất thứ tự ưu tiên: **Chân Dung Doanh Nghiệp → Sản Phẩm & Dịch Vụ → Brand Voice → (Chân Dung CEO nếu áp dụng) → AI-Sale-Assistant** (AI-Sale-Assistant thường đã có sẵn nội dung mặc định hợp lý, sửa sau cùng). Làm **từng mục một**, không dồn tất cả câu hỏi vào một lượt.

### Bước 3 — HỎI & PHỎNG VẤN từng mục

Với mỗi mục ⚠️/❌: **hỏi thẳng người dùng cung cấp thông tin trước** (họ có thể đã biết sẵn, trả lời nhanh gọn hơn là bị phỏng vấn).

**Nếu người dùng nói "không biết" / mơ hồ / "bạn hỏi tôi đi"** → chuyển sang **chế độ phỏng vấn**: mở `references/cau-hoi-phong-van.md`, lấy đúng bộ câu hỏi gợi mở của mục đó, hỏi **từng cụm nhỏ** (2-4 câu/lượt), để người dùng trả lời tự do, rồi mới tổng hợp thành nội dung file. Đừng đọc nguyên văn cả danh sách câu hỏi một lúc.

Nguyên tắc khi phỏng vấn:
- Không bịa. Nếu người dùng thật sự chưa có (vd chưa có case study, chưa có số liệu), để mục đó ngắn gọn hoặc ghi "chưa có" — đừng nhồi cho "đầy đủ".
- Với `Sản Phẩm & Dịch Vụ`: mỗi sản phẩm/gói thật là 1 file riêng (copy cấu trúc file `[Ví dụ] Gói Basic.md`), đặt phẳng trong thư mục, cập nhật danh mục trong `_MOC Sản Phẩm & Dịch Vụ.md`. Đừng xoá/ghi đè file `[Ví dụ]` — nó là mẫu tham chiếu.

### Bước 4 — LƯU AN TOÀN (tuân thủ CLAUDE.md)

- Chế độ **singleton**: điền thẳng vào file trong `00. Business Context/`. **KHÔNG** tạo `02. Projects/[Tên]/` hay nguồn ngữ cảnh song song.
- Nếu file chỉ là **placeholder trống** → điền trực tiếp.
- Nếu file đã có **nội dung THẬT** (không phải placeholder) → **KHÔNG ghi đè âm thầm**: cho người dùng xem nội dung cũ, hỏi họ muốn ghi đè / bổ sung / giữ nguyên.
- Nếu tên file còn `[Tên]` / `[Tên Doanh Nghiệp]` và đã biết tên công ty/CEO thật → đổi tên file placeholder thành tên thật (dùng `git mv` để giữ lịch sử), đừng tạo file mới song song.
- Giữ nguyên `tags` trong frontmatter và heading song ngữ "English (Tiếng Việt)" đúng quy ước vault.

### Bước 5 — KẾT THÚC

- In lại **checklist đã cập nhật** (mục nào giờ ✅).
- Nếu BMC / MHKD / Đánh Giá vẫn còn thiếu → nhắc người dùng chạy **`/mo-hinh-kinh-doanh`** để hoàn tất nốt phần mô hình kinh doanh.
- Nếu vẫn còn mục identity ⚠️/❌ mà người dùng chưa muốn làm hôm nay → ghi rõ còn thiếu gì để lần sau tiếp tục.

## Ghi chú

- Bộ câu hỏi phỏng vấn chi tiết theo từng file: `references/cau-hoi-phong-van.md`.
- Ngôn ngữ làm việc: tiếng Việt; heading dùng "English (Tiếng Việt)".
- API key chỉ nằm trong `.env` gốc vault — không dán vào note.
