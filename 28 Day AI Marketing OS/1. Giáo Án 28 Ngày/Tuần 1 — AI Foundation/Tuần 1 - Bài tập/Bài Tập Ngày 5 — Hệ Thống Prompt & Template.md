---
created: 2026-07-09
tags: [project, aios, assignment, day5]
up:
  - "[[_MOC 28 Day AIOS]]"
---

# 📋 Bài Tập Ngày 5 — HỆ THỐNG PROMPT & TEMPLATE CHUẨN

> **Mục tiêu:** Xây bộ prompt chuẩn cho 4 phòng ban. Không dùng AI theo kiểu "hỏi ngẫu nhiên" — phải có hệ thống prompt như quy trình làm việc để nhân sự dùng nhất quán.

---

## 📝 BÀI NỘP (5 output — nộp trước 22:00)

### Output 1: Marketing Prompt Pack (ít nhất 10 prompt)

Mỗi prompt viết theo cấu trúc:

```markdown
**Tên prompt:** 
**Role:** (AI đóng vai gì?)
**Context:** (Bối cảnh, doanh nghiệp, ngành)
**Task:** (Nhiệm vụ cụ thể)
**Input:** (Đầu vào cần cung cấp)
**Output Format:** (Định dạng output mong muốn)
**Constraint:** (Ràng buộc — dài tối đa? giọng văn? cấm nói gì?)
**Ví dụ output mong muốn:** (1 mẫu ngắn)
```

#### 10 Prompt Marketing cần tạo:

| # | Prompt | Mục đích |
|---|--------|----------|
| 1 | Viết bài Facebook | 1 bài/ngày, giọng thân thiện, ≤300 từ |
| 2 | Viết email marketing | Gửi cho KH cũ, kêu gọi quay lại |
| 3 | Viết kịch bản video ngắn | 30-60s, có hook mạnh |
| 4 | Viết quảng cáo Facebook | 3 phiên bản A/B test |
| 5 | Tạo content calendar tuần | 7 ngày, 2 bài/ngày |
| 6 | Phân tích insight KH từ comment | Đọc 50 comment → rút ra 5 insight |
| 7 | Viết landing page | Theo cấu trúc 7 section (từ Ngày 3) |
| 8 | Viết caption Instagram/TikTok | Kèm hashtag, emoji |
| 9 | Tạo ý tưởng content theo trend | Gợi ý 5 ý tưởng dựa trên trend hiện tại |
| 10 | Viết bài SEO/blog | 800-1500 từ, có từ khoá chính |

---

### Output 2: Sales Prompt Pack (ít nhất 8 prompt)

| # | Prompt | Mục đích |
|---|--------|----------|
| 1 | Viết kịch bản tư vấn | Cho 1 KH cụ thể, dựa trên chân dung KH |
| 2 | Xử lý từ chối (Objection Handler) | Nhập câu từ chối → AI trả lời theo Objection Matrix |
| 3 | Tạo proposal/báo giá | Tự động điền báo giá từ thông tin KH |
| 4 | Viết tin nhắn follow-up | Sau 1 ngày / 3 ngày / 7 ngày |
| 5 | Phân loại lead (nóng/ấm/lạnh) | Nhập thông tin KH → AI chấm điểm 1-10 |
| 6 | Tóm tắt lịch sử tư vấn | Từ ghi chú thô → tóm tắt 3 dòng |
| 7 | Gợi ý upsell | Phân tích KH hiện tại → gợi ý SP phù hợp |
| 8 | Soạn tin nhắn chốt sale | Tạo urgency, kêu gọi hành động |

---

### Output 3: CSKH Prompt Pack (ít nhất 6 prompt)

| # | Prompt | Mục đích |
|---|--------|----------|
| 1 | Trả lời FAQ tự động | Dựa trên FAQ Database (20 câu) |
| 2 | Xử lý khiếu nại | KH phàn nàn → AI trả lời theo SOP |
| 3 | Viết tin nhắn chăm sóc | Sinh nhật, lễ Tết, kỷ niệm |
| 4 | Viết kịch bản gọi lại KH cũ | KH đã 30+ ngày không quay lại |
| 5 | Gợi ý chương trình khuyến mãi | Dựa trên mùa, tồn kho, xu hướng |
| 6 | Viết tin nhắn cảm ơn sau mua | Ấm áp, cá nhân hoá |

---

### Output 4: Quản Trị Prompt Pack (ít nhất 6 prompt)

| # | Prompt | Mục đích |
|---|--------|----------|
| 1 | Tóm tắt báo cáo tuần | Số liệu → insight → hành động |
| 2 | Phân tích dữ liệu bán hàng | Top SP, KH, nhân viên |
| 3 | Lập kế hoạch tuần | Dựa trên mục tiêu tháng |
| 4 | Đánh giá hiệu suất nhân viên | Theo KPI từng người |
| 5 | Viết SOP cho quy trình mới | Step-by-step, checklist |
| 6 | So sánh 2 phương án kinh doanh | Phân tích SWOT, đề xuất |

---

### Output 5: Prompt Usage Guide + Test 3 Prompt

```markdown
## Prompt Usage Guide (Hướng dẫn cho nhân viên)

### Trước khi dùng
1. Mở Vault SME → vào folder `Prompt Library/`
2. Chọn nhóm prompt (Marketing/Sales/CSKH/Quản trị)
3. Copy prompt mẫu
4. Thay **[TEXT IN BRACKETS]** bằng dữ liệu thực tế
5. KHÔNG thay đổi phần Role, Context, Constraint khi chưa được duyệt

### Trong khi dùng
- Luôn KIỂM TRA output trước khi gửi cho KH
- Nếu AI trả lời sai → sửa INPUT, không sửa OUTPUT
- Mỗi prompt có 1 "Ví dụ output mong muốn" — so sánh với đó

### Sau khi dùng
- Prompt nào dùng >10 lần → đánh dấu ⭐ → cuối tháng review nâng cấp
- Prompt nào không dùng trong 30 ngày → đánh dấu 🗑️ → xoá khỏi thư viện

---

## Test 3 Prompt (BẮT BUỘC)

Chọn 3 prompt bất kỳ từ 4 nhóm trên → chạy thử → ghi kết quả:

| # | Prompt đã test | Input | Output AI | Dùng được? (Y/N) | Cần sửa gì? |
|---|---------------|-------|-----------|:---:|-----------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
```

---

## 📋 TỔNG KÊ PROMPT

| Nhóm | Số prompt | Bắt buộc test? |
|------|:---:|:---:|
| Marketing | 10 | ≥1 |
| Sales | 8 | ≥1 |
| CSKH | 6 | ≥1 |
| Quản trị | 6 | ≥1 |
| Usage Guide | 1 | — |
| **Tổng** | **31** | **≥3 đã test** |

---

## ⚡ HƯỚNG DẪN NHANH (90 phút)

| Bước | Làm gì | Mất | Tip |
|:---:|--------|:---:|-----|
| 1 | Tạo 10 prompt Marketing | 25' | Mỗi prompt copy cấu trúc → điền 6 trường |
| 2 | Tạo 8 prompt Sales | 20' | Dùng Objection Matrix từ Ngày 4 làm input |
| 3 | Tạo 6 prompt CSKH | 15' | Dùng FAQ Database từ Ngày 4 |
| 4 | Tạo 6 prompt Quản trị | 15' | Prompt đơn giản, thực tế |
| 5 | Viết Usage Guide | 10' | 3 phần: Trước/Trong/Sau khi dùng |
| 6 | Test 3 prompt + điền bảng kết quả | 5' | Chọn prompt KHÁC NHÓM để test đa dạng |

> ⏱️ Tổng: **90 phút**

---

## 💡 MẸO — Lỗi thường gặp

| ❌ Lỗi | ✅ Cách sửa |
|--------|-----------|
| Prompt không có Role | Luôn bắt đầu: "Bạn là [vai trò]..." — AI cần biết nó là ai |
| Prompt chung chung | "Viết bài hay" → "Viết bài Facebook 200 từ, giọng thân thiện, cho đối tượng nữ 30-40t" |
| Không có Constraint | AI dễ lan man → thêm: "Không quá 300 từ. Không dùng từ kỹ thuật." |
| Không có ví dụ output | AI không biết "hay" là gì → đưa 1 mẫu output mong muốn |
| Copy prompt giống hệt cho mọi nhóm | Prompt Marketing ≠ Prompt Sales ≠ Prompt CSKH — mỗi nhóm role khác nhau |
| Không test prompt | Prompt chưa test = vô dụng → bắt buộc test ≥3 prompt trước khi nộp |

---

## 🎯 TIÊU CHÍ ĐẠT

| Tiêu chí | Yêu cầu |
|----------|---------|
| Số lượng | ≥30 prompt, đủ 4 nhóm |
| Cấu trúc | Mỗi prompt có Role + Context + Task + Input + Output Format + Constraint |
| Ví dụ | Mỗi prompt có ít nhất 1 ví dụ output mong muốn |
| Test được | Đã test ≥3 prompt khác nhóm — output dùng được |
| Usage Guide | Có hướng dẫn rõ ràng cho nhân viên (3 phần) |

---

## 📖 TÀI LIỆU THAM KHẢO

- [[Bài Tập Ngày 4 — Knowledge Base]] — Dùng dữ liệu KB làm input cho prompt
- [[Bài Tập Ngày 3 — Offer & Định Vị]] — Dùng Sales Message Pack làm mẫu
- **Nguyên tắc prompt tốt:** Role → Context → Task → Input → Output → Constraint → Example

---

## 🆘 CẦN HỖ TRỢ?

- **Jarvis:** "Jarvis, tạo cho tôi 1 prompt Marketing mẫu cho [ngành của bạn]"
- **Group Elite Builders:** Chia sẻ prompt → mentor góp ý
