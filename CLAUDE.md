# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

Hướng dẫn cho Claude khi làm việc trong vault này. Đọc file này trước, trước cả khi chạy bất kỳ skill sale/marketing nào.

> Đây **không phải codebase phần mềm** — không có build/lint/test. Đây là vault Obsidian (Markdown + `.canvas` + `.base`). "Chạy" ở đây nghĩa là gọi skill (`/tên-skill`) để đọc/ghi note. Định dạng file: xem skill `obsidian-markdown` (wikilink, callout, frontmatter), `json-canvas` (`.canvas`), `obsidian-bases` (`.base`).

## Mục tiêu tổng thể của vault này

Vault này **không phải nơi lưu ghi chú thụ động** — mục tiêu cốt lõi là **sắp xếp toàn bộ dữ liệu doanh nghiệp (định vị, mô hình kinh doanh, brand voice, khách hàng, đối thủ, sản phẩm, pipeline...) thành cấu trúc mà AI agent đọc hiểu được ngay** — cả agent nội bộ (Hermes agent) lẫn các coding agent khác (Claude Code, v.v.) — để phục vụ trực tiếp 2 việc: **sản xuất content đúng giọng thương hiệu** và **quản lý sale & marketing** (pipeline, khách hàng, chiến dịch, đo lường). Vì vậy:

- Mọi ngữ cảnh nền tảng phải nằm ở một điểm đọc duy nhất, dễ đoán vị trí (`00. Business Context/` — xem bên dưới), không rải rác.
- Đặt tên file/thư mục nhất quán, có `tags` frontmatter rõ ràng — để agent dò tìm bằng convention thay vì phải hỏi lại người dùng.
- Khi thêm skill/tự động hoá mới, luôn trỏ về đúng các file trong `00. Business Context/` thay vì tạo thêm một nguồn ngữ cảnh song song.

## Vault này là gì

Đây là vault Obsidian PARA + AI Brain dành cho **DUY NHẤT 1 doanh nghiệp SME** — không phải nơi quản lý nhiều dự án/nhiều công ty khác nhau. Toàn bộ nội dung trong vault (khách hàng, đối thủ, sản phẩm, chiến dịch...) đều thuộc về một công ty duy nhất. Xem [[Vault SME — Hướng Dẫn]] để hiểu đầy đủ kiến trúc thư mục (`00. Business Context/`, PARA: `01. Inbox/` → `05. Archive/`, và lớp thực thể: `People/`, `Companies/`, `Meetings/`, `Decisions/`).

## Nguồn sự thật về công ty (đọc trước khi làm việc gì liên quan sale/marketing)

Các file định danh (identity) nằm trong **`00. Business Context/`** ở gốc vault — đây là **nguồn sự thật duy nhất (single source of truth)** về công ty, không phải tài liệu của một dự án con:

| File | Nội dung |
|---|---|
| `00. Business Context/Chân Dung Doanh Nghiệp.md` | Định vị, ICP (chân dung khách hàng lý tưởng) |
| `00. Business Context/Chân Dung CEO — [Tên].md` | Personal brand CEO: founder story, giá trị, chuyên môn, tuyến nội dung cá nhân, persona & ranh giới. **Chỉ quan trọng nếu SME phụ thuộc brand cá nhân CEO** — khi đó đọc trước khi viết content thay lời CEO |
| `00. Business Context/Brand Voice — Giọng Thương Hiệu.md` | Giọng nói thương hiệu: từ nên/tránh dùng, câu mẫu, do/don't khi viết content |
| `00. Business Context/Business Model Canvas — [Tên Doanh Nghiệp].md` + `Business Model Canvas.canvas` | 9 khối mô hình kinh doanh đầy đủ (Osterwalder) |
| `00. Business Context/MHKD/` | Trang chi tiết từng phân khúc khách hàng (`Phân Khúc Khách Hàng/PK*.md`) và từng giá trị cốt lõi (`Giá Trị Cốt Lõi/GT*.md`) — sinh ra khi chạy skill `mo-hinh-kinh-doanh` |
| `00. Business Context/Đánh Giá Mô Hình Kinh Doanh — [Tên Doanh Nghiệp].md` | Đánh giá tính nhất quán giữa 9 khối, tính khả thi, bằng chứng Product-Market Fit |
| `00. Business Context/AI-Sale-Assistant.md` | Vai trò & nguyên tắc phản hồi của AI trong vault này |
| `00. Business Context/Sản Phẩm & Dịch Vụ/` | Hồ sơ từng sản phẩm/gói: tính năng, giá, USP |

**Trước khi trả lời câu hỏi về khách hàng, giá trị, giá cả, kênh, hoặc trước khi chạy bất kỳ skill sale/marketing nào** (competitor-analysis, ab-testing, analytics, offers, seo-audit...), đọc các file trên trước. Nếu file nào còn là bản mẫu trống (placeholder chưa điền), báo cho người dùng biết đang thiếu ngữ cảnh đó thay vì tự bịa hoặc bỏ qua.

**Khi viết content (đặc biệt cho thương hiệu cá nhân CEO):** ngoài `Brand Voice` + `Chân Dung Doanh Nghiệp`, đọc thêm `Nhật Ký CEO/` để lấy chuyện thật, quan điểm, cách nói riêng của CEO — content mới có hồn thay vì generic. Chỉ khai thác mục có `rieng_tu: no` (bỏ qua `rieng_tu: yes`); ưu tiên đoạn gắn tag `#hat-giong-content`, `#cau-chuyen`, `#quan-diem`, `#giong-noi`.

## Cầu nối cho các skill import từ ngoài (gốc `marketingskills-main`)

Tất cả skill đều nằm trong `.claude/skills/` (không có thư mục `marketingskills-main/` trong vault — đó chỉ là **tên thư viện gốc** nơi 4 skill `thu-nghiem-ab`, `do-luong-tracking`, `thiet-ke-offer`, `kiem-tra-seo` được import về). Các skill này được viết theo quy ước riêng của thư viện gốc: chúng tìm file `.agents/product-marketing.md` (hoặc `.claude/product-marketing.md`, hoặc tên cũ `product-marketing-context.md`) để lấy ngữ cảnh doanh nghiệp trước khi hỏi người dùng. Chi tiết những gì đã chỉnh khi import (trigger tiếng Việt, bỏ mục không hợp SME VN...) xem `.claude/skills/README.md`.

**Vault này không dùng đường dẫn đó.** Khi một skill nói "check for product marketing context first" và tìm các file trên mà không thấy — đọc thay bằng bộ file trong `00. Business Context/` ở bảng trên (đặc biệt `Chân Dung Doanh Nghiệp.md` + `Business Model Canvas — [Tên Doanh Nghiệp].md` + `AI-Sale-Assistant.md`), coi chúng là tương đương. Đừng hỏi lại người dùng những thông tin đã có sẵn trong các file đó (ICP, định vị, giá trị cốt lõi, tone thương hiệu...).

## Khi nào cần chạy `/mo-hinh-kinh-doanh` và `/hoan-tat-business-context`

Nếu `Business Model Canvas — [Tên Doanh Nghiệp].md` hoặc `Chân Dung Doanh Nghiệp.md` (trong `00. Business Context/`) vẫn còn là bản mẫu trống, gợi ý người dùng chạy skill `mo-hinh-kinh-doanh` trước khi đào sâu các việc sale/marketing khác cần ngữ cảnh công ty (phan-tich-doi-thu, thiet-ke-offer, thu-nghiem-ab...) — các skill đó đều tham chiếu ngược lại các file gốc này.

Hai skill bổ trợ nhau để hoàn tất Business Context: `mo-hinh-kinh-doanh` lo **9 khối BMC + các file PK/GT trong `MHKD/`**; `hoan-tat-business-context` **audit toàn bộ `00. Business Context/` xem còn thiếu/placeholder gì** (Chân Dung Doanh Nghiệp, Brand Voice, Chân Dung CEO, AI-Sale-Assistant, Sản Phẩm & Dịch Vụ) rồi hỏi — user không biết thì phỏng vấn từng câu để lấy thông tin và lưu vào đúng file. Khi user muốn "điền nốt / kiểm tra ngữ cảnh doanh nghiệp còn thiếu gì", chạy `hoan-tat-business-context`.

Vì vault này chỉ có 1 công ty duy nhất, kết quả của skill `mo-hinh-kinh-doanh` LUÔN điền vào các file trong `00. Business Context/` kể trên (chế độ "1 công ty / root singleton") — **không** tạo thư mục dự án con kiểu `02. Projects/[Tên]/`. Chi tiết đầy đủ về 2 chế độ (1 công ty vs nhiều dự án) nằm trong `.claude/skills/mo-hinh-kinh-doanh/SKILL.md`.

## Ghi output vào đâu (write targets) — nửa còn lại của vault

`00. Business Context/` là nơi **đọc** ngữ cảnh. Kết quả **tạo ra** trong lúc làm việc phải ghi đúng chỗ dưới đây (đầy đủ cây thư mục sau 1 tháng vận hành xem `README.md` mục 5), không đổ hết vào `01. Inbox/`:

| Loại output | Ghi vào | Quy ước |
|---|---|---|
| Content đã viết/đăng | `03. Areas/Brand & Content/Content Đã Đăng/` | 1 file / 1 post, tên `YYYY-MM-DD — [Kênh] — [Tên post].md` |
| Nhật ký cá nhân CEO (story, quan điểm, giọng thật) | `Nhật Ký CEO/` | 1 file/ngày `YYYY-MM-DD — Nhật ký.md`; khác `Daily/` (nhật ký công việc). Tôn trọng `rieng_tu: yes` |
| Số liệu / báo cáo đo lường | `03. Areas/Analytics & Reporting/` — chọn đúng miền (xem dưới) | Link chéo về file content tương ứng để biết bài nào chạy tốt |
| Trạng thái deal / pipeline | `03. Areas/Sales Pipeline & CRM/` | |
| Khách/lead/đối tác thật (từng người) | `People/` | 1 file/người, ghi rõ thuộc phân khúc nào (`(PK3)` hoặc link `[[PK3 — …]]`) |
| Công ty khách/đối thủ/vendor thật | `Companies/` | |
| Biên bản sale call / discovery | `Meetings/` | Bắt buộc link tới `People/` + `Companies/` + `Projects/`/`Areas/` liên quan |
| Quyết định giá/kênh/ngân sách | `Decisions/` | Cần chủ DN xác nhận trước khi chốt |
| Chiến dịch CÓ deadline | `02. Projects/` | |
| Feedback/chứng thực khách (testimonial, review, case study, góp ý, khiếu nại) | `04. Resources/Feedback & Chứng Thực/` | 1 file/feedback, phân loại bằng frontmatter `type`; link về sản phẩm + `People/`. Ảnh/video review → `Media/` cùng thư mục |
| Hình ảnh / video của sản phẩm | `00. Business Context/Sản Phẩm & Dịch Vụ/_Media/[tên sản phẩm]/` | Hồ sơ `.md` để phẳng ở thư mục cha; media nhúng bằng `![[…]]` |
| Playbook/template/nghiên cứu tái dùng | `04. Resources/` | |

**Analytics & Reporting có 2 trục — chọn đúng chỗ ghi:**
- *Theo thời gian* (tổng hợp): `Báo Cáo Ngày/`, `Báo Cáo Tuần/`, `Báo Cáo Quý/`.
- *Theo miền đo lường* (đo sâu): `Tương Tác Mạng Xã Hội/` (on-platform reach/engagement) · `Hiệu Quả Traffic Mạng Xã Hội/` (social → click ra web → chuyển đổi) · `Hiệu Quả Quảng Cáo/` (paid: CPL/CPA/ROAS theo chiến dịch) · `Hiệu Suất Content/` (pivot theo Loại·Format·Hook) · `Chăm Sóc Khách Hàng/` (phễu chat→chốt). Báo cáo định kỳ *tổng hợp lại* từ các miền này. Mỗi thư mục có `_MOC` + file `[Mẫu]` — copy mẫu, bỏ tiền tố `[Mẫu]`, đổi kỳ. Đo hiệu suất content cần gắn `content_pillar` / `format` / `hook` vào frontmatter mỗi bài trong `Content Đã Đăng/`.

**Phân biệt bắt buộc:** *phân khúc khách hàng* (persona, ngữ cảnh nền) → `00. Business Context/MHKD/Phân Khúc Khách Hàng/`; *khách thật đang mua* (dữ liệu vận hành) → `People/`+`Companies/`. Đừng lẫn hai lớp này.

**Không note mồ côi:** mọi note vận hành phải link ra ngoài (một `Meetings/` phải link ai họp + công ty nào + project/area nào). Khi một `Project` đóng, kết quả link về `Area` tương ứng rồi mới chuyển `05. Archive/` (chuyển vào, không xoá).

## Skill → ghi kết quả vào đâu

Skill nằm trong `.claude/skills/`, gọi bằng `/tên-skill`. Skill sale/marketing đọc `00. Business Context/` trước; kết quả ghi vào:

| Skill | Ghi kết quả vào |
|---|---|
| `mo-hinh-kinh-doanh` | `00. Business Context/` (Chân Dung, BMC + `.canvas`, `MHKD/PK*` + `GT*`) — chế độ 1-công-ty |
| `phan-tich-doi-thu` | `04. Resources/Market & Competitor Research/Đối Thủ/` |
| `nghien-cuu-thi-truong` | `04. Resources/Market & Competitor Research/Nghiên Cứu Thị Trường/` (+ 1 `.canvas`) |
| `kiem-tra-seo` | `03. Areas/Marketing Channels/[YYYY-MM-DD] SEO Audit — …md` |
| `do-luong-tracking` | `03. Areas/Analytics & Reporting/Tracking Plan.md` |
| `thu-nghiem-ab` | `03. Areas/Analytics & Reporting/[YYYY-MM-DD] Thử Nghiệm — …md` |
| `thiet-ke-offer` | Offer trong `00. Business Context/Sản Phẩm & Dịch Vụ/` hoặc `04. Resources/` |
| `nghien-cuu-video-youtube`, `phan-tich-video-notebooklm` | Research cho `03. Areas/Marketing Channels/` |
| `obsidian-*`, `json-canvas`, `defuddle` | Tiện ích (định dạng note, `.canvas`, trích URL) — không có thư mục đích cố định |

## Quy ước chung khác

- Ngôn ngữ làm việc trong vault: tiếng Việt, heading dùng "tiếng Anh kèm tiếng Việt trong ngoặc" (vd `## Value Propositions (Giá trị cốt lõi)`).
- API key (Apify, Firecrawl...) chỉ lưu trong `.env` ở gốc vault (đã gitignore) — không dán key vào bất kỳ note/skill nào khác.
- Không ghi đè file identity trong `00. Business Context/` (`Chân Dung Doanh Nghiệp.md`, `AI-Sale-Assistant.md`, `Business Model Canvas — [Tên].md`, `Brand Voice — Giọng Thương Hiệu.md`...) một cách âm thầm — luôn xác nhận với người dùng nếu file đã có nội dung thật (không phải placeholder).
