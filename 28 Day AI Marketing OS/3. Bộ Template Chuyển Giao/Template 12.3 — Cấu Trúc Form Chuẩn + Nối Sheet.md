---
up:
  - "[[Danh Mục Template Chuyển Giao]]"
created: 2026-07-15
tags: [project, aios, template]
---

# Template 12.3 — Cấu Trúc Form Chuẩn + Nối Sheet

> Dùng cho **[[Ngày 12 — Landing Page & Lead Magnet]]** (Khối 4 + Bước 4 demo). **Form xấu mà CHẠY THẬT ăn đứt landing page đẹp còn nằm trên giấy.** Mỗi trường thêm vào = rớt ~10–20% người điền → hỏi ít thôi, hỏi thứ DÙNG ĐƯỢC. Trường quan trọng nhất không phải tên hay số — mà là **trường phân loại dạng danh sách chọn**: nó là **mầm CRM của Tuần 3**.

## 1. Khung điền — 6 trường chuẩn (điền là xong)

| # | Trường | Bắt buộc? | Câu chữ gợi ý |
|:-:|---|:---:|---|
| 1 | **Họ tên** | ✅ | *"Anh/chị tên gì ạ?"* — để tin nhắn có tên người, không "Chào bạn". |
| 2 | **Số điện thoại** | ✅ | Kênh gọi/Zalo — **thứ ta thật sự đến để lấy**. |
| 3 | **Zalo có phải số này không?** | ✅ | 1 câu Có/Không — tiết kiệm 1 vòng hỏi lại. |
| 4 | 🔴 **Trường PHÂN LOẠI (danh sách chọn)** | ✅ | *"Bạn đang quan tâm điều gì nhất?"* — **câu đắt nhất form.** Xem mục 2. |
| 5 | **Email** | ⬜ tuỳ ngành | B2C VN: bỏ được. B2B: giữ. |
| 6 | **Ghi chú** | ⬜ | Tự luận, không bắt buộc. |

> **Quy tắc sắt:** đừng hỏi ngày sinh, địa chỉ nhà, nghề nghiệp — chưa dùng đến.

## 2. 🔴 Trường phân loại = mầm CRM Tuần 3 (5 lựa chọn = 5 luồng bán)

Đây KHÔNG phải câu hỏi cho vui. Chính 5 lựa chọn này là câu **định tuyến lead** mà Tuần 3 (CRM + chatbot + kịch bản tư vấn) dùng. **Chọn sai 5 lựa chọn hôm nay = Tuần 3 làm lại từ đầu.** Bắt buộc là **danh sách chọn** (không phải ô tự luận) và **mỗi lựa chọn dẫn tới một hành động bán khác nhau**.

**🍵 Bản mẫu MSX — *"Bạn đang quan tâm điều gì nhất?"***

| Lựa chọn | Hành động bán tương ứng |
|---|---|
| ① **Khó ngủ, muốn thư giãn buổi tối** | → hộp đơn 359.000đ |
| ② **Tìm quà biếu bố mẹ** | → combo quà tặng (mua 3 tặng 1 — 1.015.000đ) |
| ③ **Muốn dùng thử trước** | → hộp đơn 359.000đ + tin trấn an |
| ④ **Đang so sánh với trà khác** | → gửi Bảng so sánh 10 tiêu chí + bằng chứng (`O1`) |
| ⑤ **Hỏi mua sỉ – đại lý** | → chuyển thẳng cho chủ DN, không để tư vấn viên xử |

> **Lead tự phân loại chính mình trước khi sale chạm vào.** Ranh giới: chỉ *"hỗ trợ thư giãn buổi tối"* — không dùng "chữa mất ngủ" trong nhãn lựa chọn.

## 3. Google Form → Sheet — 3 cài đặt sống còn + nối Sheet

**⚙️ Ba cài đặt sống còn (TẮT cả 3 — thiếu là khách thật không điền được, bạn không bao giờ biết):**
1. **TẮT** *"Thu thập địa chỉ email"* (Settings → Responses).
2. **TẮT** *"Giới hạn 1 phản hồi"* (khỏi bắt đăng nhập Google).
3. **TẮT** *"Yêu cầu đăng nhập"* / hạn chế trong tổ chức.

**Nối Sheet:**
4. Tab **Responses → Link to Sheets** → tạo Sheet `[TênDN]-Leads`.
5. **Thêm tay 4 cột quản trị:** `Nguồn | Phân loại | Trạng thái follow-up | Người phụ trách`. *(Cột Phân loại tự có từ trường phân loại — đó là lý do nó BẮT BUỘC là danh sách chọn.)*
6. Câu xác nhận sau khi gửi = **Thank You Message** (hẹn rõ: nhận quà qua kênh nào, trong bao lâu).

**🔒 Data Security ngay tại đây:** Share Sheet → **chỉ thêm email người trực lead + chủ DN**. **KHÔNG** bật "Anyone with the link". Tên + SĐT khách = tầng **Restricted** (N4).

**🔴 TEST 2 LẦN:** ① tự điền **bằng ĐIỆN THOẠI** + trình duyệt ẩn danh → lead phải hiện trong Sheet · ② nhờ 1 người thân điền từ máy họ.

## 4. ⬆️ Đường nâng cấp — trao quà TỰ ĐỘNG (form → Sheet → Hermes → Zalo)

Form + Sheet mới chỉ **hứng** lead. Muốn khách điền lúc 2h sáng vẫn **nhận quà trong <1 phút** mà không cần người trực → nối tiếp:

```text
① Landing (Vercel *.vercel.app free)  hoặc  Google Form N12
        ↓ form ghi vào
② Google Sheet "[TênDN]-Leads"  (chính Sheet ở mục 3 — có trường phân loại)
        ↓ Hermes theo dõi Sheet 24/7
③ HERMES / RocketAgent (đã onboard Tuần 1)  ── thấy lead mới → nhắn Zalo:
        • Trao quà NGAY (<1'): link PDF + lời chào   🟢 AUTO
        • Ghi trạng thái "đã gửi quà" ngược vào Sheet 🟢 AUTO
        ↓
④ Quà = Lead Magnet PDF (Google Drive, link Viewer)
```

- **Không thêm công cụ mới:** Vercel (trang) + Google Sheet (mục 3) + Hermes/Zalo (đã có Tuần 1) + Drive.
- **Đường siêu tắt:** bí thì bỏ Vercel, dùng thẳng **Google Form** ở mục 3 làm nơi nhận lead — Hermes vẫn đọc cùng Sheet đó và nhắn Zalo y hệt. **Khâu tự động không đổi.**
- 🔴 **Chuỗi nuôi dưỡng** (10 tin Zalo) là tầng **ASSISTED — người duyệt cả 10 mới bật**; trao quà mới là AUTO.
- 👉 **Toàn bộ 5 bước setup + phiếu đầu bài + nghiệm thu ở** [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]].

## 5. Thích ứng ngành — trường phân loại theo ngành

> 6 trường + 3 cài đặt sống còn + luật "phân loại phải là danh sách chọn": GIỮ NGUYÊN. Chỉ đổi 5 lựa chọn.

- **🚀 RocketAI (B2B):** thêm trường **"Quy mô nhân sự / doanh thu tháng"** → lọc lead đủ ngân sách **trước khi** đốt 30' của founder.
- **Spa:** *"Bạn đang lo điều gì nhất?"* → mụn / lão hoá / thư giãn / trị liệu chuyên sâu / hỏi giá.
- **Nha khoa:** thêm *"Tình trạng răng hiện tại"*.
- **Giáo dục:** thêm *"Lớp / tuổi của con"*.
- **Gym:** *"Mục tiêu"* → giảm cân / tăng cơ / giữ dáng / phục hồi.

## 6. Tiêu chí đạt

- Form **5–6 trường**, **có trường phân loại dạng danh sách chọn** (5 lựa chọn, mỗi lựa chọn = 1 hành động bán).
- 3 cài đặt sống còn đã TẮT; **đã test điền trên điện thoại → lead hiện trong Sheet**.
- Sheet có 4 cột quản trị; share **theo email cụ thể**, không dùng link công khai.
- (Nâng cấp) Hermes trỏ đúng Sheet → **quà tới Zalo <2 phút**.

## 🔗 Kết nối

- [[Ngày 12 — Landing Page & Lead Magnet]] · [[Bài Tập Ngày 12 — Landing Page & Lead Magnet]] · [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]]
- [[Template 12.1 — Bảng Chọn Lead Magnet]] · [[Template 12.2 — Landing Page Copy 9 Khối]] · [[Template 12.4 — Lead Flow Map 6 Trạm]]
- Nguyên liệu: [[Template 4.1 — Knowledge Base 10 Thư Mục & Data Security Rule]] (Data Security Rule)
