---
name: phan-tich-doi-thu
description: Phân tích đối thủ cạnh tranh cho SME Việt Nam — không cần tool SEO/backlink trả phí, chỉ dùng dữ liệu quan sát được công khai (website, Google, mạng xã hội, review), kiểm tra nhanh xem AI (ChatGPT/Gemini) có nhắc tên đối thủ không, và chấm điểm offer của đối thủ theo Phương trình giá trị (Value Equation) của Alex Hormozi dựa trên website/fanpage. Dùng skill này khi người dùng nói "phân tích đối thủ", "competitor analysis", "so sánh với công ty X", "đối thủ của tôi có gì mạnh/yếu", "offer của đối thủ có gì hay", hoặc đưa tên/URL một công ty và hỏi cách cạnh tranh lại. Ghi kết quả vào `04. Resources/Market & Competitor Research/Đối Thủ/`.
---

# Competitor Analysis — Phân tích đối thủ cạnh tranh cho SME

## Vì sao bản này khác bản gốc trên skills.sh

Skill gốc (`aaron-he-zhu/aaron-marketing-skills`) được thiết kế cho agency SEO/GEO: cần tool trả phí (Ahrefs/Semrush, AI-citation monitor), script `firecrawl.py` riêng, và một cấu trúc bộ nhớ (`memory/hot-cache.md`, `memory/open-loops.md`) không tồn tại trong vault này. Copy nguyên bản sẽ gọi vào file/script không có thật.

Bản này giữ lại **phần lõi có giá trị** — nhãn hoá chất lượng dữ liệu (Đã đo/Người cung cấp/Ước tính), bảng so sánh đối thủ, điểm mạnh-để-học/điểm yếu-để-khai-thác, kế hoạch Ngay/Ngắn hạn/Dài hạn — và thay các bước cần tool trả phí (keyword ranking, backlink profile, Core Web Vitals) bằng tín hiệu **quan sát được miễn phí**: website, Google Maps/review, mạng xã hội, và một câu hỏi thật gửi cho AI để xem đối thủ có được nhắc tên không (bản rút gọn của "GEO/AI Citation Analysis").

Cũng đã tham khảo thêm 1 mẫu subagent "competitive-analyst" (dạng agency/enterprise, tools Read/Grep/Glob/WebFetch/WebSearch) để lấy thêm 2 ý còn thiếu — **xác minh đúng pháp nhân trước khi phân tích** và **SWOT rút gọn (thêm Cơ hội/Mối đe doạ, không chỉ Mạnh/Yếu)** — nhưng cố tình bỏ phần lớn phần còn lại của mẫu đó: phân tích tài chính/doanh thu/định giá thị trường, patent tracking, và giao thức JSON điều phối đa-agent — đều không áp dụng được vì SME Việt Nam không có báo cáo tài chính công khai, hiếm khi có patent, và đây là 1 skill đơn, không phải hệ thống nhiều agent.

## Quy trình tổng quan

1. Xác định đối thủ (1-5 công ty, ưu tiên đối thủ trực tiếp)
2. Thu thập dữ liệu từng đối thủ theo 6 lát cắt bên dưới — mỗi số liệu gắn nhãn **Đã đo / Người dùng cung cấp / Ước tính**
3. Đối chiếu với "chúng tôi" qua `[[Chân Dung Doanh Nghiệp]]` — nếu file đó còn trống, đánh dấu hàng "Chúng tôi" là N/A và gợi ý chạy skill `mo-hinh-kinh-doanh` trước, đừng tự bịa định vị
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

**Xác minh đúng pháp nhân trước khi đào sâu** — tên công ty Việt Nam rất hay trùng/gần giống nhau (nhiều "Winhouse", nhiều domain cùng thương hiệu). Trước khi phân tích, đối chiếu ít nhất 2 trong số: MST qua tra cứu công khai (masothue.com, tratencongty.com), địa chỉ đăng ký kinh doanh, tên người đại diện pháp luật có khớp với "founder/CEO" nêu trên website không, hoặc dấu hiệu kỹ thuật (cùng ảnh/CDN/slogan giữa các domain nghi liên quan). Nếu 2 domain nghi là cùng 1 thương hiệu nhưng không chắc chắn 100%, ghi rõ "nhiều khả năng" thay vì khẳng định.

## Bước 2 — Thu thập dữ liệu (6 lát cắt, không cần tool trả phí)

Với mỗi đối thủ:

1. **Hồ sơ công ty** — URL, năm thành lập, MST/pháp nhân đăng ký, quy mô ước tính (nhân sự/số văn phòng), mô hình kinh doanh, đối tượng khách hàng, dịch vụ/sản phẩm chính. Lấy qua `defuddle parse <url> --md` (trang giới thiệu/về chúng tôi, đội ngũ) + WebSearch nếu website không đủ thông tin. Nếu nhiều trang con (giới thiệu, đội ngũ, hoạt động công ty...) có thông tin rải rác, đọc thêm — đừng dừng ở mỗi trang chủ.
2. **Kênh & nội dung** — kênh mạng xã hội mạnh nhất (Facebook/TikTok/YouTube/Zalo OA/Instagram/Pinterest), tần suất đăng quan sát được, chủ đề nội dung chính, có kênh video/KOL sáng lập không. Facebook/TikTok/Zalo OA thường chặn crawl tự động — thử WebFetch trực tiếp, nếu chỉ trả về tên trang mà không có số liệu thì ghi rõ "bị chặn, không lấy được số liệu"; YouTube thường lấy được số liệu thật (subscriber/số video/lượt xem) qua HTML thô trang kênh.
3. **Uy tín xã hội** — rating & số lượng review Google Maps/Facebook, 1-2 câu review nổi bật (khen và chê), số dự án/khách hàng tiêu biểu nếu họ công khai. Phân biệt rõ: số liệu **tự công bố trên chính website đối thủ** (ví dụ "2000+ hồ sơ thiết kế") khác với số liệu **có nguồn độc lập kiểm chứng** (review Google, báo chí) — cả hai đều dùng được nhưng phải ghi rõ loại nào.
4. **Trải nghiệm & giá** — website có bảng giá/gói dịch vụ công khai không (thường nằm ở bài blog SEO dạng "báo giá/đơn giá..." chứ không phải 1 trang cố định tên "bao-gia" — tìm qua WebSearch nếu trang đoán không có), mức giá cụ thể nếu công khai, tốc độ/độ chuyên nghiệp của website quan sát bằng mắt. Kèm 1 tín hiệu SEO miễn phí (không cần Ahrefs/Semrush — xem thêm ở skill `kiem-tra-seo` nếu muốn đào sâu hơn với tool trả phí): số trang được Google index qua `site:domain.com`, có blog hoạt động đều không (tần suất bài mới), và title thẻ trang chủ có chứa từ khoá dịch vụ + khu vực không.
5. **GEO / AI-citation rút gọn** — đặt 1-2 câu hỏi mà khách hàng thật sự sẽ hỏi AI (ví dụ: "gợi ý công ty [ngành] uy tín ở [khu vực]") qua WebSearch hoặc hỏi trực tiếp, ghi lại đối thủ nào được nhắc tên và vì lý do gì. Lưu ý: kết quả WebSearch trả về các bài "Top N công ty..." của bên thứ ba (thường là bài SEO/quảng cáo) — đây KHÔNG phải là AI answer engine thật, không tính là đã làm GEO check; muốn có kết luận đáng tin phải hỏi trực tiếp trên ChatGPT/Gemini.
6. **Offer theo Phương trình giá trị (Value Equation — Alex Hormozi)** — 5 lát cắt trên mô tả đối thủ *đang có gì* (giá, kênh, uy tín); lát cắt này trả lời câu hỏi khác: **offer của họ thuyết phục khách đến đâu**. Công thức:

   > Giá trị cảm nhận = (Kết quả mơ ước × Khả năng đạt được) / (Thời gian chờ đợi × Nỗ lực & hy sinh)

   Đọc kỹ trang dịch vụ/báo giá trên website (thường đủ dữ liệu) + fanpage (bài quảng cáo, ưu đãi, cam kết — nếu Facebook/TikTok chặn crawl như thường gặp, dùng nội dung xem được qua WebSearch snippet hoặc ghi rõ "cần xem thủ công trên fanpage", không bỏ qua im lặng). Với mỗi đối thủ, chấm **Cao/Trung bình/Thấp** cho từng yếu tố, luôn kèm bằng chứng cụ thể — không chấm điểm suông:
   - **Kết quả mơ ước (Dream Outcome)** — họ vẽ viễn cảnh cụ thể đến đâu? ("nhà đẹp, tối ưu công năng" chung chung, hay có hình ảnh/con số cụ thể kiểu "biệt thự 5 phòng ngủ với 2,6 tỷ")
   - **Khả năng đạt được — cảm nhận (Perceived Likelihood)** — bằng chứng khiến khách tin sẽ đạt được: bảo hành, cam kết hoàn tiền, số dự án (phân biệt tự công bố/có kiểm chứng — xem lát cắt 3), giải thưởng, chứng chỉ công nghệ, review/testimonial thật
   - **Thời gian chờ đợi (Time Delay)** — có cam kết mốc thời gian cụ thể không ("nhận bản vẽ 3D trong X ngày", "bàn giao sau Y tháng"), hay chỉ nói chung chung "nhanh chóng"
   - **Nỗ lực & hy sinh (Effort & Sacrifice)** — mô hình trọn gói (khách không phải tự tìm/phối hợp nhiều nhà thầu) hay khách phải tự lo nhiều việc; thủ tục thanh toán/hợp đồng phức tạp không

   Ghi thêm nếu quan sát được (không bắt buộc, nhưng thường xuất hiện trên fanpage hơn là website): **Bảo đảm (Guarantee)** cụ thể, **Khan hiếm/Cấp bách (Scarcity/Urgency)** (ưu đãi có hạn, số suất tư vấn miễn phí giới hạn), **Bonus đi kèm** (tặng thiết kế 3D, tặng nội thất...), và **Tên gói/offer** (họ có đặt tên riêng cho gói dịch vụ không, hay chỉ gọi chung "gói cơ bản/nâng cao") — đây là các đòn bẩy Hormozi hay dùng để tăng tử số/giảm mẫu số của công thức. Nếu muốn tự xây offer đầy đủ 6 thành phần (thay vì chỉ chấm điểm đối thủ), dùng skill `thiet-ke-offer`.

Dùng `references/mau-phan-tich.md` để có khung bảng cho từng lát cắt.

## Bước 3 — Đối chiếu với "chúng tôi"

Đọc `[[Chân Dung Doanh Nghiệp]]` (định vị, ICP, value proposition). Nếu các mục đó còn trống, KHÔNG tự suy ra định vị của người dùng — đánh dấu N/A trong bảng so sánh và nói rõ: "Chưa so sánh được vì `Chân Dung Doanh Nghiệp.md` chưa điền — chạy skill `mo-hinh-kinh-doanh` hoặc điền tay trước."

## Bước 4 — Tổng hợp

Viết theo khung `## Tổng hợp` trong `references/mau-phan-tich.md`: bảng so sánh nhanh (điểm mạnh/yếu quy về 1 hàng mỗi đối thủ), điểm mạnh-để-học (mỗi ý trích dẫn bằng chứng cụ thể — "X có rating 4.8/5 với 1.200 review nhờ...", không viết chung chung như "nội dung tốt"), điểm yếu-để-khai-thác tương tự, và kế hoạch **Ngay lập tức / Ngắn hạn / Dài hạn**.

Nếu có đủ dữ liệu ở 2+ đối thủ để nhìn ra bức tranh chung của cả ngành (không chỉ 1 đối thủ riêng lẻ), thêm 2 mục **Cơ hội** (khoảng trống cả ngành chưa ai lấp — ví dụ không đối thủ nào công khai giá theo m²) và **Mối đe doạ** (xu hướng có thể ảnh hưởng đến mình dù không phải lỗi của riêng 1 đối thủ — ví dụ 1 đối thủ đang đầu tư kênh video rất mạnh, sẽ chiếm top-of-mind của khách hàng nếu mình không phản ứng) — đây là bản SWOT rút gọn (Mạnh/Yếu của từng đối thủ + Cơ hội/Đe doạ chung của thị trường), không cần làm phân tích tài chính hay thị phần định lượng (dữ liệu đó SME Việt Nam không có sẵn để kiểm chứng).

Thêm 1 bảng so sánh riêng cho **Offer/Value Equation** (từ lát cắt 6): mỗi đối thủ 1 cột, 4 hàng Kết quả mơ ước/Khả năng đạt được/Thời gian chờ/Nỗ lực-hy sinh, chấm Cao/TB/Thấp kèm bằng chứng ngắn. Đây là input trực tiếp để viết offer của chính mình sau này — đối thủ yếu nhất ở yếu tố nào là chỗ dễ vượt qua nhất, đối thủ mạnh nhất ở yếu tố nào là chuẩn cần đạt tối thiểu để cạnh tranh ngang hàng.

**Chuẩn chất lượng**: mỗi điểm mạnh/yếu phải gắn với 1 số liệu có nhãn và 1 tên đối thủ cụ thể — không viết "có vẻ mạnh về marketing" mà không có bằng chứng.

## Bước 5 — Ghi kết quả

Mỗi đối thủ 1 file tại `04. Resources/Market & Competitor Research/Đối Thủ/[Tên đối thủ].md`, theo đúng cấu trúc của `[Ví dụ] Đối Thủ ABC.md` (đừng ghi đè file ví dụ này — nó là mẫu, không phải đối thủ thật):

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

- Nếu `Chân Dung Doanh Nghiệp.md` còn trống → gợi ý chạy `mo-hinh-kinh-doanh` trước khi so sánh được sâu.
- **Tín hiệu nên theo dõi định kỳ** (mỗi quý, hoặc ngay khi nghe tin) thay vì chỉ "quay lại xem cho có": đổi giá/gói dịch vụ, ra mắt dịch vụ mới, nhân sự chủ chốt rời đi/gia nhập, ký đối tác mới (thường thấy trong mục "hoạt động công ty"/blog PR của đối thủ), xu hướng review đổi chiều rõ rệt (nhiều review xấu dồn dập). Ghi log mới vào file đối thủ khi có, không phân tích lại từ đầu.
- Nếu phát hiện khoảng trống nội dung rõ ràng (đối thủ có mà mình chưa có) → cân nhắc thêm vào `04. Resources/Playbooks/` hoặc kênh marketing đang thử nghiệm trong `Chân Dung Doanh Nghiệp.md`.
- Nếu kế hoạch "Ngay lập tức"/"Ngắn hạn" là 1 thay đổi cụ thể có thể đo được (đổi CTA, thêm bảo đảm, đổi giá) — viết thành 1 hypothesis rõ ràng ("Vì đối thủ X có bảo hành hoàn tiền còn mình không có, ta tin thêm bảo hành sẽ tăng tỷ lệ chốt Y%") và cân nhắc chạy thử nghiệm A/B nhỏ bằng skill `thu-nghiem-ab`, thay vì áp dụng đại trà ngay rồi không biết có hiệu quả không.
- Khi triển khai phản ứng (đổi landing page, chạy content mới dựa trên khoảng trống phát hiện được), gắn UTM/event đo lường riêng cho campaign đó (skill `do-luong-tracking`) để biết phản ứng có hiệu quả hơn cách cũ không — nếu không, sẽ không biết nên tiếp tục hay dừng.
- Nếu phát hiện đối thủ có vị trí rất rõ ràng để mình vượt qua (giá, feature, cam kết) và có nhu cầu tìm kiếm thật (khách hàng hay so sánh "X vs Y" trên Google) → cân nhắc viết 1 trang so sánh/vs-page bằng skill `competitors` để vừa chiếm traffic tìm kiếm vừa hỗ trợ chốt sale.
- Nếu số đối thủ cần theo dõi nhiều (6+) hoặc cần hồ sơ rất sâu có SEO/backlink (khi đã có ngân sách cho tool trả phí) → skill `competitor-profiling` có quy trình "quick scan vs deep profile" và lưu raw data theo ngày, phù hợp khi quy mô phân tích lớn hơn những gì bản rút gọn này nhắm tới.

## Skill liên quan trong kho `marketingskills-main`

Các skill dưới đây trong `marketingskills-main/skills/` là bản gốc cho SaaS/agency (thường cần Firecrawl, DataForSEO, GA4... — xem lý do bản này không copy nguyên ở đầu file). Dùng chúng khi đã có tool/ngân sách tương ứng hoặc cần đào sâu hơn phạm vi của skill này:

| Skill | Dùng khi |
|---|---|
| `competitor-profiling` | Cần hồ sơ đối thủ rất sâu (SEO/backlink bằng DataForSEO, review mining bằng Firecrawl), theo dõi nhiều đối thủ với snapshot theo ngày |
| `competitors` | Viết trang so sánh/alternative ("X vs Y", "[đối thủ] alternative") để chiếm traffic tìm kiếm cạnh tranh |
| `thiet-ke-offer` | Tự xây offer đầy đủ 6 thành phần (deliverable, bonus, bảo đảm, khan hiếm, tên, giá) cho chính mình, không chỉ chấm điểm đối thủ |
| `kiem-tra-seo` | Audit kỹ thuật SEO đầy đủ cho website của mình (Core Web Vitals, crawlability, schema...) sau khi thấy đối thủ mạnh về SEO |
| `do-luong-tracking` | Thiết lập tracking plan/GA4/GTM đầy đủ để đo phản ứng khi hành động theo phát hiện từ phân tích đối thủ |
| `thu-nghiem-ab` | Thiết kế thử nghiệm A/B nghiêm túc (cỡ mẫu, ý nghĩa thống kê) cho các thay đổi lớn hơn rút ra từ phân tích đối thủ |

## Tài liệu tham khảo

- [Mẫu phân tích](references/mau-phan-tich.md) — khung bảng rút gọn cho từng bước (hồ sơ, kênh & nội dung, uy tín xã hội, GEO check, Offer/Value Equation, bảng tổng hợp + kế hoạch hành động)
