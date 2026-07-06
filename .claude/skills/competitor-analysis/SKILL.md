---
name: competitor-analysis
description: Phân tích đối thủ cạnh tranh cho SME Việt Nam — không cần tool SEO/backlink trả phí, chỉ dùng dữ liệu quan sát được công khai (website, Google, mạng xã hội, review) cộng kiểm tra nhanh xem AI (ChatGPT/Gemini) có nhắc tên đối thủ không. Dùng skill này khi người dùng nói "phân tích đối thủ", "competitor analysis", "so sánh với công ty X", "đối thủ của tôi có gì mạnh/yếu", hoặc đưa tên/URL một công ty và hỏi cách cạnh tranh lại. Ghi kết quả vào `03. Resources/Market & Competitor Research/Đối Thủ/`.
---

# Competitor Analysis — Phân tích đối thủ cạnh tranh cho SME

## Vì sao bản này khác bản gốc trên skills.sh

Skill gốc (`aaron-he-zhu/aaron-marketing-skills`) được thiết kế cho agency SEO/GEO: cần tool trả phí (Ahrefs/Semrush, AI-citation monitor), script `firecrawl.py` riêng, và một cấu trúc bộ nhớ (`memory/hot-cache.md`, `memory/open-loops.md`) không tồn tại trong vault này. Copy nguyên bản sẽ gọi vào file/script không có thật.

Bản này giữ lại **phần lõi có giá trị** — nhãn hoá chất lượng dữ liệu (Đã đo/Người cung cấp/Ước tính), bảng so sánh đối thủ, điểm mạnh-để-học/điểm yếu-để-khai-thác, kế hoạch Ngay/Ngắn hạn/Dài hạn — và thay các bước cần tool trả phí (keyword ranking, backlink profile, Core Web Vitals) bằng tín hiệu **quan sát được miễn phí**: website, Google Maps/review, mạng xã hội, và một câu hỏi thật gửi cho AI để xem đối thủ có được nhắc tên không (bản rút gọn của "GEO/AI Citation Analysis").

## Quy trình tổng quan

1. Xác định đối thủ (1-5 công ty, ưu tiên đối thủ trực tiếp)
2. Thu thập dữ liệu từng đối thủ theo 5 lát cắt bên dưới — mỗi số liệu gắn nhãn **Đã đo / Người dùng cung cấp / Ước tính**
3. Đối chiếu với "chúng tôi" qua `[[Chân Dung Doanh Nghiệp]]` — nếu file đó còn trống, đánh dấu hàng "Chúng tôi" là N/A và gợi ý chạy skill `business-model-canvas` trước, đừng tự bịa định vị
4. Tổng hợp: bảng so sánh nhanh, điểm mạnh để học, điểm yếu để khai thác, kế hoạch hành động
5. Ghi file theo đúng template `Đối Thủ` có sẵn trong vault + cập nhật MOC

## Decision Gates

**Dừng lại hỏi người dùng** khi:
- Chưa có tên/URL đối thủ cụ thể và không suy ra được từ `Chân Dung Doanh Nghiệp.md`, ngành nghề đã biết, hoặc note cũ trong vault → hỏi tên 2-5 đối thủ, hoặc đề nghị tìm giúp qua từ khoá ngành (WebSearch).
- Đối thủ trùng tên với nhiều công ty khác nhau (tên chung chung) → xác nhận đúng công ty (địa chỉ/website/lĩnh vực) trước khi phân tích, tránh phân tích nhầm.

**Không dừng lại** — cứ tiếp tục và ghi rõ giới hạn — khi:
- Không có dữ liệu "chúng tôi" để so sánh (đánh dấu N/A, không suy diễn).
- Không tìm được follower/rating chính xác của đối thủ trên 1 kênh nào đó (ghi "Chưa xác định — cần kiểm tra thủ công", không đoán số).
- Chỉ tìm được 2-3 đối thủ thay vì 5 (vẫn phân tích với số lượng có, ghi chú rõ).

## Bước 1 — Xác định đối thủ

Phân loại: đối thủ trực tiếp (cùng dịch vụ, cùng khách hàng mục tiêu), đối thủ gián tiếp (giải pháp thay thế), đối thủ nội dung (không bán cùng thứ nhưng chiếm sự chú ý của cùng khách hàng trên Google/mạng xã hội).

## Bước 2 — Thu thập dữ liệu (5 lát cắt, không cần tool trả phí)

Với mỗi đối thủ:

1. **Hồ sơ công ty** — URL, năm thành lập, quy mô ước tính (nhân sự/số văn phòng), mô hình kinh doanh, đối tượng khách hàng, dịch vụ/sản phẩm chính. Lấy qua `defuddle parse <url> --md` (trang giới thiệu/về chúng tôi) + WebSearch nếu website không đủ thông tin.
2. **Kênh & nội dung** — kênh mạng xã hội mạnh nhất (Facebook/TikTok/YouTube/Zalo OA), tần suất đăng quan sát được, chủ đề nội dung chính, có kênh video/KOL sáng lập không.
3. **Uy tín xã hội** — rating & số lượng review Google Maps/Facebook, 1-2 câu review nổi bật (khen và chê), số dự án/khách hàng tiêu biểu nếu họ công khai.
4. **Trải nghiệm & giá** — website có bảng giá/gói dịch vụ công khai không, mức giá tương đối (rẻ/trung bình/cao cấp — suy ra từ định vị, không suy ra số cụ thể nếu không công khai), tốc độ/độ chuyên nghiệp của website quan sát bằng mắt.
5. **GEO / AI-citation rút gọn** — đặt 1-2 câu hỏi mà khách hàng thật sự sẽ hỏi AI (ví dụ: "gợi ý công ty [ngành] uy tín ở [khu vực]") qua WebSearch hoặc hỏi trực tiếp, ghi lại đối thủ nào được nhắc tên và vì lý do gì.

Dùng `references/mau-phan-tich.md` để có khung bảng cho từng lát cắt.

## Bước 3 — Đối chiếu với "chúng tôi"

Đọc `[[Chân Dung Doanh Nghiệp]]` (định vị, ICP, value proposition). Nếu các mục đó còn trống, KHÔNG tự suy ra định vị của người dùng — đánh dấu N/A trong bảng so sánh và nói rõ: "Chưa so sánh được vì `Chân Dung Doanh Nghiệp.md` chưa điền — chạy skill `business-model-canvas` hoặc điền tay trước."

## Bước 4 — Tổng hợp

Viết theo khung `## Tổng hợp` trong `references/mau-phan-tich.md`: bảng so sánh nhanh (điểm mạnh/yếu quy về 1 hàng mỗi đối thủ), điểm mạnh-để-học (mỗi ý trích dẫn bằng chứng cụ thể — "X có rating 4.8/5 với 1.200 review nhờ...", không viết chung chung như "nội dung tốt"), điểm yếu-để-khai-thác tương tự, và kế hoạch **Ngay lập tức / Ngắn hạn / Dài hạn**.

**Chuẩn chất lượng**: mỗi điểm mạnh/yếu phải gắn với 1 số liệu có nhãn và 1 tên đối thủ cụ thể — không viết "có vẻ mạnh về marketing" mà không có bằng chứng.

## Bước 5 — Ghi kết quả

Mỗi đối thủ 1 file tại `03. Resources/Market & Competitor Research/Đối Thủ/[Tên đối thủ].md`, theo đúng cấu trúc của `[Ví dụ] Đối Thủ ABC.md` (đừng ghi đè file ví dụ này — nó là mẫu, không phải đối thủ thật):

```yaml
---
tags: [competitor]
created: YYYY-MM-DD
up:
  - "[[_MOC Đối Thủ]]"
---
```

- `## Hồ sơ` — điền từ Bước 2, mỗi số liệu kèm nhãn chất lượng nếu không hiển nhiên.
- `## So với chúng tôi ([[Chân Dung Doanh Nghiệp]])` — từ Bước 3.
- `## Nhật ký cập nhật (thêm mới nhất lên đầu)` — log lần phân tích này dưới ngày hôm nay; **không ghi đè log cũ** nếu file đã tồn tại (đây là hồ sơ theo dõi lâu dài, xem lại mỗi quý để thấy xu hướng đổi giá/định vị/kênh).
- `## Ảnh hưởng tới chiến lược` — link tới `[[_MOC Decisions]]` nếu phát hiện dẫn tới 1 quyết định cụ thể.

Sau đó cập nhật `_MOC Đối Thủ.md`: thêm link vào "Danh sách đối thủ đang theo dõi" và 1 hàng vào bảng "So sánh nhanh".

## Bước tiếp theo gợi ý

- Nếu `Chân Dung Doanh Nghiệp.md` còn trống → gợi ý chạy `business-model-canvas` trước khi so sánh được sâu.
- Theo dõi định kỳ: quay lại đối thủ này mỗi quý, thêm log mới thay vì phân tích lại từ đầu.
- Nếu phát hiện khoảng trống nội dung rõ ràng (đối thủ có mà mình chưa có) → cân nhắc thêm vào `03. Resources/Playbooks/` hoặc kênh marketing đang thử nghiệm trong `Chân Dung Doanh Nghiệp.md`.

## Tài liệu tham khảo

- [Mẫu phân tích](references/mau-phan-tich.md) — khung bảng rút gọn cho từng bước (hồ sơ, kênh & nội dung, uy tín xã hội, GEO check, bảng tổng hợp + kế hoạch hành động)
