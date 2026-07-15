---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an, template]
---

# 📐 Blueprint Chuẩn — Cấu Trúc Giáo Án 28 Ngày

> Mọi giáo án `Ngày XX` trong thư mục này PHẢI theo đúng cấu trúc 12 phần dưới đây. Đây là "khuôn" để nội dung 28 ngày đồng nhất, chấm chữa được, và chuyển giao được.

## Nguyên tắc thiết kế

0. **Chuyển giao, không phải khoá học** — chương trình là **solutions chuyển giao hệ điều hành AI Marketing & Sale OS (Rocket Agent OPC / Hermes)**: framework, agent, template, hệ thống được ĐÓNG GÓI SẴN và bàn giao theo từng module mỗi ngày. Bài tập của học viên = **nạp dữ liệu DN mình → custom → test → tối ưu** module đã nhận, không xây từ số 0. Hệ điều hành sau bàn giao vận hành bằng Agent 24/7: tạo lead, tư vấn, follow-up, chăm sóc khách hàng, đo lường tăng trưởng.
1. **Không dạy lý thuyết suông** — mỗi ngày học viên phải ĐÓNG XONG một nhóm tài sản cho doanh nghiệp thật của mình (module đã custom chạy được).
2. **Case study = 2 case THẬT, 0 case bịa** (theo [[Case Study Kép — RocketAI + MSX Group]]): 🍵 **MSX Group — Mẫu Sơn Xanh** (B2C sản phẩm — **case XUYÊN SUỐT**: ví dụ chính mọi ngày, vault demo sống `ai-marketing-system-msx-demo/`, đồng thời là case CHỨNG MINH khi bán) + 🚀 **RocketAI Solutions** (B2B dịch vụ — **case ĐỐI CHIẾU**: mở ra khi B2B khác B2C rõ rệt như offer/proposal/chu kỳ chốt; avatar khách hàng là chị Mai chủ spa). Sen Spa (hư cấu) đã loại bỏ toàn bộ. Mỗi demo, prompt mẫu, template minh hoạ bằng case thật theo mapping trong [[_Chuẩn Đồng Bộ Tuần 1]], kèm ghi chú "Thích ứng ngành khác" (spa/thẩm mỹ, nha khoa, giáo dục, gym, coaching — các ngành DNA "bán qua tư vấn").
3. **Core vs Bonus** — mỗi ngày phân biệt rõ output BẮT BUỘC (Core — điều kiện qua ngày) và output NÂNG CAO (Bonus). Chủ SME chỉ có 1.5–2h/ngày ngoài giờ live.
4. **Template dựng sẵn 80%** — học viên điền 20% dữ liệu doanh nghiệp mình, không xây từ khung trống.
5. **Chấm được bằng rubric** — tiêu chí nghiệm thu phải đo được, để mentor + AI Grader chấm nhất quán (xem [[Hệ Thống Chấm Chữa & Support Hàng Ngày]]).
6. **Một nguồn sự thật thông số** — mọi con số (deadline 23h59, số FAQ/prompt/test, cấu trúc bảng, track công cụ A/B/C) theo [[_Chuẩn Đồng Bộ Tuần 1]]; khi hai tài liệu lệch nhau, file chuẩn là trọng tài.

## Cấu trúc 12 phần (bắt buộc)

```markdown
# Ngày XX — [Tên bài]

> Một câu tóm tắt "hôm nay xây gì cho doanh nghiệp".

## 1. 🎯 Mục Tiêu Ngày Học
- 3-5 bullet: cuối ngày học viên CÓ gì trong tay (tài sản, không phải "hiểu biết").
- Ghi rõ: Core Output (bắt buộc) vs Bonus Output.

## 2. 📚 Kiến Thức Trọng Tâm
- Các khối kiến thức cần giảng, mỗi khối: ý chính + cách giảng ngắn gọn (analogy, ví dụ Spa).
- Chỉ dạy kiến thức PHỤC VỤ việc làm bài tập hôm nay.

## 3. 🖥️ Agenda Buổi Live (90 phút)
Bảng: Thời lượng | Hoạt động | Chi tiết. Khung chuẩn:
- 10' — Warm-up + chữa nhanh 2-3 bài tiêu biểu hôm trước
- 25' — Giảng kiến thức trọng tâm
- 30' — Demo thực hành live (làm thật trên ví dụ Spa)
- 15' — Học viên bắt đầu làm tại chỗ, Q&A
- 10' — Giao bài tập + tiêu chí nghiệm thu + nhắc deadline

## 4. 🎬 Kịch Bản Demo (Case thật)
- Từng bước demo cụ thể trainer làm live, với dữ liệu case thật theo mapping [[_Chuẩn Đồng Bộ Tuần 1]]: 🚀 RocketAI ("Build In Public" — demo trên chính công ty người dạy) hoặc 🍵 MSX Group (demo trên vault `ai-marketing-system-msx-demo/` đã điền sẵn).
- Mỗi bước: làm gì → công cụ nào → kết quả trông như thế nào.

## 5. ✅ Checklist Thực Thi (Học viên tự làm)
- Checklist từng bước, thứ tự đúng, có ước lượng thời gian mỗi cụm.
- Tổng thời gian tự làm ≤ 2h (phần Core).

## 6. 📝 Bài Tập Về Nhà
- Đề bài rõ ràng: làm gì, trên doanh nghiệp của mình.
- **Deliverable nộp**: liệt kê chính xác file/link nộp gì, đặt tên thế nào (`[Tên DN] — Ngày XX — [Tên tài sản]`).
- Deadline: 23h59 cùng ngày. Nộp vào thread cohort.

## 7. 📄 Template Đi Kèm
- Danh sách template phát cho học viên (tên + mô tả + cấu trúc các trường chính của từng template).
- Template phải "điền là xong", có sẵn ví dụ Spa điền mẫu trong template.

## 8. 🤖 Prompt Mẫu
- 3-6 prompt HOÀN CHỈNH copy-paste được (khung Role–Context–Task–Input–Output–Constraint).
- Mỗi prompt: đặt trong code block, có chỗ `{{điền dữ liệu DN}}`, kèm 1 ví dụ đã điền bằng **case thật** (🍵 MSX mặc định; 🚀 RocketAI khi cần đối chiếu B2B — theo mapping [[_Chuẩn Đồng Bộ Tuần 1]]).

## 9. 📋 SOP Thao Tác
- Quy trình vận hành lặp lại sau khoá học (khi nào làm, ai làm, input → các bước → output, tần suất).

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm
Thang 100 điểm, 4 nhóm chuẩn (điều chỉnh tiêu chí con theo ngày):
| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | ... |
| Chất lượng & độ sâu | 30 | ... |
| Cá nhân hoá vào DN thật | 25 | ... |
| Dùng được ngay | 15 | ... |
Mức: ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).
+ 3-5 lỗi trừ điểm điển hình của ngày này.

## 11. ❓ FAQ & Lỗi Thường Gặp
- ≥5 câu hỏi thật học viên sẽ hỏi + trả lời ngắn gọn.
- ≥3 lỗi thường gặp + cách phát hiện + cách sửa.

## 12. 🔁 Kết Nối
- Ngày trước: [[Ngày XX — ...]] · Ngày sau: [[Ngày XX — ...]]
- Tài sản hôm nay được dùng lại ở ngày nào (nêu cụ thể).
```

## Frontmatter bắt buộc

```yaml
---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: <1-4>
day: <1-28>
core-output: "<liệt kê ngắn output bắt buộc>"
---
```

## Quy ước riêng cho Demo Day (Ngày 7, 14, 21, 28)

- Không dạy kiến thức mới. Agenda đổi thành: 15' tổng kết tuần → 60' học viên demo (mỗi người 5-7', theo format chuẩn) → 15' chấm điểm chéo + công bố scorecard.
- Bài tập = hoàn thiện các mục 🔧/🔴 tồn đọng trong tuần (catch-up day).
- Rubric = Scorecard tổng hợp tuần (điểm trung bình các ngày + demo).

## Ghi chú công cụ

- **Framework bàn giao: Vault SME** (`ai-marketing-system/`) — vault Obsidian PARA + AI Brain học viên cài về, là lớp NÃO của hệ thống. Mỗi giáo án có dòng `🗂️ Trong Vault SME` chỉ rõ hôm nay thao tác ở thư mục/skill nào; ánh xạ đầy đủ + module còn thiếu: [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]]. Khi vault có skill phỏng vấn tương ứng (`/mo-hinh-kinh-doanh`, `/thiet-ke-offer`, `/hoan-tat-business-context`…), demo chuẩn là chạy skill trong vault; prompt mẫu trong giáo án là phương án B.
- Nền tảng động cơ: **RocketAgent (OPC) / Hermes** — Chatbot, Automation, 5 AI Agent chạy 24/7 trên đây, ĐỌC ngữ cảnh từ `00. Business Context/` của Vault SME và GHI kết quả ngược về vault. Khi RocketAgent chưa có tính năng tương ứng, ghi rõ phương án thay thế phổ biến (ChatGPT Projects/Claude Projects, Google Sheets, Canva, CapCut, Zalo OA…) — giáo án không khoá cứng vào tool bên thứ ba.
