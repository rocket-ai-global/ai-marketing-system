# Skills — Vault SME Sale/Marketing

Bộ skill nền tảng cho vault SME (không chứa skill MindMirror — vault này dùng kiến trúc PARA + AI Brain riêng, xem `../../Vault SME — Hướng Dẫn.md`).

## Danh sách skills

| Skill | Mục đích |
|---|---|
| `obsidian-cli` | Đọc/tạo/search note, backlinks, properties qua Obsidian CLI |
| `obsidian-markdown` | Cú pháp Obsidian Flavored Markdown: wikilink, callout, embed, frontmatter |
| `obsidian-bases` | Tạo/sửa file `.base` — dashboard cho Sales Pipeline, Companies, Projects |
| `json-canvas` | Tạo/sửa file `.canvas` — sơ đồ pipeline, mind map, flowchart |
| `defuddle` | Trích nội dung sạch từ URL — dùng cho `04. Resources/Market & Competitor Research/` |
| `mo-hinh-kinh-doanh` | Phỏng vấn 9 ô Business Model Canvas — dùng khi làm rõ/định vị lại mô hình kinh doanh trong `00. Business Context/Chân Dung Doanh Nghiệp.md` |
| `hoan-tat-business-context` | **Bổ trợ `mo-hinh-kinh-doanh`** — audit `00. Business Context/` xem còn thiếu file identity nào, hỏi/phỏng vấn để điền nốt (Chân Dung Doanh Nghiệp, Brand Voice, Chân Dung CEO, AI-Sale-Assistant, Sản Phẩm & Dịch Vụ). BMC/PK/GT giao lại `mo-hinh-kinh-doanh` |
| `nghien-cuu-video-youtube` | Research video YouTube theo chủ đề/từ khoá — dùng cho `03. Areas/Marketing Channels/` |
| `phan-tich-video-notebooklm` | Phân tích video YouTube trong Notion database bằng NotebookLM |
| `phan-tich-doi-thu` | Phân tích đối thủ cạnh tranh không cần tool trả phí (website, Google, mạng xã hội, GEO check) — ghi vào `04. Resources/Market & Competitor Research/Đối Thủ/` |
| `thiet-ke-offer` | Xây/cải thiện offer (value stack, bonus, bảo đảm, khan hiếm, giá) theo Value Equation của Hormozi |
| `kiem-tra-seo` | Audit SEO kỹ thuật + on-page cho website (crawlability, Core Web Vitals, meta tags, E-E-A-T) |
| `do-luong-tracking` | Thiết lập/kiểm tra tracking — GA4, GTM, tracking plan, UTM, event naming |
| `thu-nghiem-ab` | Thiết kế và phân tích thử nghiệm A/B — hypothesis, cỡ mẫu, ý nghĩa thống kê, chương trình experiment liên tục |

**Lưu ý**: 4 skill trên (`thiet-ke-offer`, `kiem-tra-seo`, `do-luong-tracking`, `thu-nghiem-ab`) gốc từ `marketingskills-main` (thiết kế cho SaaS/agency), đã được chỉnh lại để phù hợp SME Việt Nam:
- Sửa tham chiếu ngữ cảnh doanh nghiệp về đúng `Chân Dung Doanh Nghiệp.md` (thay vì file `.agents/product-marketing.md` không tồn tại trong vault)
- Thêm câu trigger tiếng Việt vào `description` để dễ nhận diện hơn khi gõ tiếng Việt
- `kiem-tra-seo`: đánh dấu bỏ qua mục International SEO (không áp dụng cho site 1 ngôn ngữ), đẩy ưu tiên mục Local Business lên đầu
- `do-luong-tracking`: thêm event mẫu cho kênh chốt khách VN (phone/Zalo/Messenger click), ghi chú Nghị định 13/2023 về bảo vệ dữ liệu cá nhân, ưu tiên GTM no-code vì SME thường không có dev
- `thu-nghiem-ab`: thêm cảnh báo ngưỡng traffic tối thiểu (test cổ điển khó khả thi nếu site có traffic thấp — gợi ý phương án thay thế) và hạ kỳ vọng nhịp độ chương trình experiment cho team 1-2 người

Nội dung chi tiết (references/) vẫn giữ tiếng Anh và một số ví dụ/tool nước ngoài (USD, GA4, PostHog...) — phần framework cốt lõi vẫn dùng tốt, chỉ bỏ qua đoạn nào rõ ràng không áp dụng được (tool trả phí không có, ví dụ SaaS không liên quan).

## Cách dùng

Gọi trực tiếp bằng `/tên-skill`, hoặc mô tả việc muốn làm — Claude tự nhận diện skill phù hợp.
