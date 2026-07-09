---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, operations]
---

# 🧑‍🏫 Hệ Thống Chấm Chữa & Support Hàng Ngày

> Lời hứa "bài tập hàng ngày có chấm chữa + support hàng ngày" chỉ đứng vững khi có HỆ THỐNG — không phải khi mentor cố gắng. File này là SOP vận hành để bất kỳ ai (không cần Tony) chạy được một cohort (lớp học theo đợt) 28 ngày.
>
> **Chấm cái CHẠY, không chấm bài luận:** vì chương trình là chuyển giao solutions, bài nộp mỗi ngày = module đã đóng gói sẵn được học viên **custom + test trên chính doanh nghiệp mình**. Rubric vì thế dồn trọng số vào "Cá nhân hoá vào DN thật" (25đ) + "Dùng được ngay" (15đ).

---

## 1. Nhịp một ngày chuẩn (Daily Rhythm)

| Giờ | Hoạt động | Ai làm |
|---|---|---|
| 19h30–21h00 | **Buổi live** theo agenda giáo án (warm-up + chữa bài → giảng → demo → làm tại chỗ → giao bài) | Trainer chính |
| Sau live → 23h59 | Học viên làm bài Core (≤2h), **nộp vào thread ngày** theo format tên chuẩn | Học viên |
| 23h59 | Chốt deadline. Ai chưa nộp → bot nhắc lần 1 | Bot/Ops |
| 6h–8h sáng hôm sau | **AI Grader chấm 100% bài** theo rubric của ngày → trả điểm + 3 nhận xét cụ thể/bài | AI Grader (RocketAgent) |
| 8h–12h | Mentor review: chấm sâu toàn bộ bài 🔴/🔧 + spot-check (kiểm tra xác suất) 20% bài ✅/⭐; override điểm AI nếu lệch | Mentor (1:10) |
| 12h–13h | **Office hours** (giờ hỗ trợ trực tiếp): học viên 🔴/🔧 được gọi 1:1 15' | Mentor |
| 19h30 hôm sau | 10' đầu live: **chữa chung 2-3 bài tiêu biểu** (1 bài xuất sắc để học theo + 1-2 lỗi phổ biến) | Trainer |

**Nguyên tắc phản hồi:** mọi bài nộp đúng hạn nhận feedback trong **< 14 giờ** (trước buổi live kế tiếp). Trễ hạn = chấm gộp ở Demo Day tuần đó.

## 2. Kiến trúc chấm 3 lớp

```
Lớp 1 — AI GRADER (100% bài, <1h/đợt)
  · Chấm theo rubric 100 điểm trong giáo án từng ngày
  · Output: điểm 4 nhóm + 3 nhận xét sửa cụ thể + xếp loại ⭐/✅/🔧/🔴
  · Chạy trên RocketAgent → chính nó là DEMO SỐNG của sản phẩm đang dạy
Lớp 2 — MENTOR (~20-30% bài, có chủ đích)
  · Bắt buộc: mọi bài 🔴 + 🔧 · Spot-check 20% bài ✅/⭐ để giữ AI Grader trung thực
  · Quyền override điểm; ghi nhận lỗi AI Grader chấm sai → tinh chỉnh rubric prompt
Lớp 3 — CHỮA CHUNG (cả lớp, 10'/ngày)
  · 1 bài ⭐ (mổ xẻ vì sao tốt) + 1-2 lỗi phổ biến nhất hôm qua (ẩn danh)
```

**Xếp loại & hành động:**

| Loại | Điểm | Hành động bắt buộc |
|---|---|---|
| ⭐ Xuất sắc | ≥80 | Đưa vào kho ví dụ mẫu (xin phép) + vinh danh bảng tuần |
| ✅ Đạt | 60–79 | Qua ngày. Nhận 3 gợi ý nâng cấp |
| 🔧 Cần sửa | 40–59 | Sửa theo nhận xét, nộp lại trong 24h (chấm lại 1 lần) |
| 🔴 Làm lại | <40 | Office hours 1:1 + làm lại; chưa xong dồn về Demo Day |

## 3. Vai trò & định biên (cohort 30 học viên)

| Vai trò | Số lượng | Trách nhiệm | Thời gian/ngày |
|---|---|---|---|
| Trainer chính | 1 | Dạy live, chữa chung, giữ năng lượng cohort | 2h |
| Mentor | 3 (1:10) | Chấm lớp 2, office hours, theo sát nhóm 10 người của mình | 1.5–2h |
| Ops/Integrator | 1 | Tracker, nhắc nộp, điều phối thread, kỹ thuật RocketAgent, báo cáo số | 1–1.5h |
| AI Grader + Bot | — | Chấm lớp 1, nhắc deadline, tổng hợp điểm | tự động |

## 4. Kênh & không gian cohort

- **Nhóm Zalo/Discord cohort**: kênh `#thông-báo` · `#nộp-bài-ngày-XX` (mỗi ngày 1 thread) · `#hỏi-đáp` (SLA trả lời < 4h trong 8h-21h) · `#khoe-kết-quả` (win công khai — nuôi động lực + gom liệu case study).
- **Format nộp bài:** `[Tên DN] — Ngày XX — [Tên tài sản]` + link tài sản (Google Drive/RocketAgent workspace). Sai format = bot nhắc, không chấm cho tới khi đúng.
- **Buddy system:** ghép cặp 2 học viên khác ngành từ Ngày 0 — check-in nhau mỗi tối. Giảm rớt cohort rẻ nhất.

## 5. Ngày 0 — Onboarding & Baseline (1 tuần trước khai giảng)

Điều kiện để "cài ra chạy được luôn" + có case study:
1. **Form baseline bắt buộc** (không nộp = không vào lớp): lead/tháng · tỷ lệ inbox→booking · tỷ lệ booking→chốt · doanh thu 3 tháng gần nhất · AOV · số giờ chủ DN làm marketing/sale thủ công mỗi tuần · mục tiêu 28 ngày (1 con số chính).
2. **Cài sẵn hạ tầng:** workspace RocketAgent tạo sẵn từng học viên (Knowledge Base trống đúng cấu trúc 10 thư mục + bộ template ngày 1-7 nạp sẵn) · vào nhóm cohort · nhận lịch 28 ngày + buddy.
3. **Lọc DNA 5 gen** đã xong ở khâu tuyển sinh (xem [[Khách Hàng Mục Tiêu — AI Marketing & Sale OS]]) — Ngày 0 chỉ xác nhận lại.
4. Video 15': cách học, cách nộp bài, cam kết 2h/ngày, quy tắc cohort.

## 6. Student Success Tracker (bảng theo dõi học viên)

Một sheet duy nhất, Ops cập nhật tự động từ AI Grader — cấu trúc:

| Cột | Nội dung |
|---|---|
| Học viên / DN / ngành | Định danh |
| Baseline | 6 số Ngày 0 |
| Ngày 1→28 | Điểm từng ngày (màu theo ⭐✅🔧🔴, trống = chưa nộp) |
| Điểm TB tuần + Demo Day | Tổng hợp |
| Cờ rủi ro | 🚩 tự bật khi: 2 ngày liên tiếp không nộp HOẶC 2 bài 🔴 liên tiếp HOẶC vắng 2 live |
| Kết quả Ngày 28 vs baseline | Lead/booking/doanh thu — nguyên liệu case study |

**Quy trình cờ 🚩 (chống rớt cohort):** bật cờ → mentor gọi điện (không nhắn) trong 24h → chẩn đoán (kẹt thời gian? kẹt kỹ thuật? mất động lực?) → kê toa: gói catch-up Demo Day / buddy kèm / hạ xuống chỉ làm Core. Ops báo cáo số 🚩 mỗi tuần cho trainer.

## 7. Nhịp tuần & nghiệm thu

- **Demo Day (Ngày 7/14/21/28):** học viên demo 5-7' theo format: *Tôi đã xây gì → chạy thử sống → số liệu → 1 điều kẹt nhất*. Chấm bằng Scorecard tuần (điểm TB các ngày 60% + demo 40%).
- **Điều kiện tốt nghiệp + chứng nhận:** ≥24/28 ngày đạt Core + demo Ngày 28 có hệ thống chạy sống + nộp bộ số so với baseline.
- **Sau Ngày 28:** follow-up 30/60/90 ngày (khớp kế hoạch 90 ngày của giáo án Ngày 28) — vừa customer success, vừa gom số case study, vừa cửa upsell gói Managed/License.

## 8. KPI vận hành của chính hệ thống support (đo mỗi cohort)

| Chỉ số | Ngưỡng |
|---|---|
| % bài được feedback < 14h | ≥ 95% |
| % câu hỏi #hỏi-đáp trả lời < 4h | ≥ 90% |
| Tỷ lệ nộp bài đúng hạn trung bình | ≥ 75% |
| Số 🚩 xử lý trong 24h | 100% |
| Mentor override AI Grader | < 15% (cao hơn = rubric prompt phải sửa) |

## 🔗 Kết nối với

- [[_MOC 28 Day AIOS]] · [[Đánh Giá Hiệu Quả Chương Trình — 2026-07-08]]
- [[_Blueprint Chuẩn — Cấu Trúc Giáo Án]] (rubric từng ngày nằm trong giáo án)
- [[Danh Mục Template Chuyển Giao]]
