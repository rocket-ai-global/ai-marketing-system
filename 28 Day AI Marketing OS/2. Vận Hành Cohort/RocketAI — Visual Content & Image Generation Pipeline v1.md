---
created: 2026-07-14
status: image-backend-enabled-openai-codex-gpt-image-2-medium
tags: [rocketai, content-os, image-generation, visual-strategy, approval-gate]
owner: Tony
---

# RocketAI — Visual Content & Image Generation Pipeline v1

## 1. Nguyên tắc

Không tạo ảnh theo kiểu trang trí cho đẹp. Ảnh đi kèm content phải phục vụ chiến lược:

```text
Hook bài viết → Insight chính → Visual angle → CTA → đo phản ứng
```

Mỗi bài trước khi tạo ảnh phải có:

```text
Persona | Funnel | Pillar | Insight | CTA | Visual format | Risk check
```

Nếu chưa có insight chính thì chưa tạo ảnh.

## 2. Vai trò của ảnh trong Content OS

Ảnh không thay nội dung. Ảnh có 4 nhiệm vụ:

1. Kéo mắt dừng lại trong 1-2 giây đầu.
2. Làm rõ một ý chính của bài.
3. Tăng khả năng lưu/chia sẻ nếu là checklist/framework.
4. Tạo nhận diện RocketAI/AIOS nhất quán.

## 3. 6 format ảnh chính

| Format | Dùng khi nào | Ví dụ |
|---|---|---|
| Quote card | Một insight mạnh | “AI không cứu quy trình bán hàng rối.” |
| Before/After diagram | So sánh trước/sau AIOS | Trước: prompt rời rạc → Sau: Business Brain + Pipeline |
| Checklist card | Nội dung thực dụng, lưu được | “7 câu hỏi kiểm tra DN sẵn sàng dùng AI Marketing” |
| Process map | Giải thích quy trình | Brain → Content → Lead → Sales → Dashboard |
| Build-in-public screenshot style | Show đang làm thật | Zalo bot test, dashboard, content queue |
| Offer card | BOF / kéo inbox | “28 ngày cài Phòng Marketing & Sales AI” |

## 4. Style guide đề xuất

```text
Mood: founder-led, thực chiến, modern SaaS, không màu mè.
Nền: navy/dark/white sạch.
Accent: electric blue / cyan / lime nhẹ.
Typography: chữ lớn, ít chữ, dễ đọc trên mobile.
Không dùng: ảnh AI robot sáo rỗng, người máy cầm não, ánh sáng thần thánh, claim quá đà.
```

## 5. Visual workflow

```text
Content brief
→ Chọn format ảnh
→ Tạo prompt ảnh
→ Generate 2-4 option
→ Chọn option tốt nhất
→ Nếu cần: edit lại chữ/layout bằng Canva/Figma
→ Tony duyệt
→ Gắn vào bài approved
→ Đăng/schedule
→ Đo số
```

## 6. Prompt template tạo ảnh

```text
Create a Vietnamese social media visual for RocketAI / AIOS.
Format: {{quote card / before-after diagram / checklist / process map}}
Aspect ratio: {{1:1 / 4:5 / 16:9}}
Audience: SME owners / sellers / coaches in Vietnam.
Core message: {{1 insight chính}}
Text on image: {{tối đa 8-12 từ tiếng Việt}}
Visual metaphor: {{mô tả hình}}
Style: modern SaaS, founder-led, dark navy/white background, electric blue accents, clean typography, high contrast, mobile-readable.
Avoid: robots, hype, fake futuristic cliché, crowded layout, unreadable tiny text.
```

## 7. Output contract mỗi bài

Mỗi bài trong Content Queue cần thêm các cột visual:

```text
Visual format | Image prompt | Aspect ratio | Status | Asset URL/path | Approved by | Posted link
```

Trạng thái visual:

```text
no_visual_needed → visual_brief → generating → needs_edit → approved → attached → posted
```

## 8. Image backend status

Kiểm tra thực tế ngày 2026-07-14:

```text
Hermes image_generate tool: có trong toolset.
Backend mong muốn hiện tại: FAL.ai / FLUX 2 Klein 9B.
Trạng thái chạy thử: FAILED vì thiếu FAL_KEY hoặc chưa login Nous Portal managed FAL.
```

Thông báo lỗi chính:

```text
FAL_KEY environment variable is not set.
Log in to Nous Portal to use managed FAL image generation: run `hermes model`.
```

Kết luận:

- Workflow ảnh đã thiết kế được.
- Tool tạo ảnh trong Hermes có sẵn.
- Nhưng máy hiện tại chưa bật credential/backend image generation.
- Chưa thể khẳng định đang dùng được “image2” nếu chưa cấu hình đúng provider/model.

## 9. Quyết định khuyến nghị

Không tự động tạo và đăng ảnh ngay.

Giai đoạn 1:

```text
AI tạo visual brief + prompt → Tony duyệt style → bật backend image → generate ảnh → human review → mới gắn vào bài.
```

Giai đoạn 2:

```text
Bài approved → ảnh approved → schedule/post tự động.
```

## 10. Việc cần làm để bật tạo ảnh

Một trong các hướng:

1. Set `FAL_KEY` trong Hermes env, restart gateway/session.
2. Login Nous Portal managed FAL qua `hermes model` nếu dùng billing portal.
3. Nếu muốn đúng OpenAI image2/gpt-image backend, cấu hình image_gen provider tương ứng trong Hermes tools/config nếu backend đó đã được cài.

Sau khi bật, chạy test 3 format:

1. Quote card.
2. Before/After diagram.
3. Checklist card.

Chỉ khi 3 ảnh pass style/readability mới đưa vào Content Queue.
