---
up:
  - "[[Danh Mục Template Chuyển Giao]]"
created: 2026-07-15
tags: [project, aios, template]
---

# Template 12.4 — Lead Flow Map 6 Trạm

> Dùng cho **[[Ngày 12 — Landing Page & Lead Magnet]]** (Khối 5–7 + Bước 6 demo). Sơ đồ 1 trang: lead đi từ "người xem ẩn danh" đến "được chăm sóc" qua **6 trạm**. Luật duy nhất: **trạm nào không có TÊN NGƯỜI THẬT là trạm đó KHÔNG AI LÀM.** *"Nhân viên sẽ follow-up" = không ai follow-up.* Và vì lead là dữ liệu nhạy cảm → cuối trang **bắt buộc 1 dòng Data Security**.

## 1. Sơ đồ 6 trạm (khung cố định)

```text
① Người xem (bài/video có CTA)
        ↓
② Điền form  ── 6 trường, có trường phân loại
        ↓
③ Thank You + gửi quà  ── xác nhận + trao quà trong ≤5 phút
        ↓
④ Lead rơi vào Sheet/CRM  ── kèm Nguồn + Phân loại + Trạng thái + Người phụ trách
        ↓
⑤ Tin nhắn giá trị 24h  ── KHÔNG chào bán ngay
        ↓
⑥ Cập nhật trạng thái + phân loại
```

## 2. Khung điền — bảng 6 trạm (điền là xong)

```text
| # | Trạm | Ai (TÊN NGƯỜI THẬT) | Công cụ | Thời gian tối đa | Tầng |
|:-:|------|---------------------|---------|:---:|:---:|
| ① | Người xem (traffic có CTA)     | —          | {{ }} | —      | —   |
| ② | Điền form (6 trường)           | Khách      | {{ }} | —      | —   |
| ③ | Thank You + gửi quà            | {{tên}}    | {{ }} | ≤5'    | {{ }} |
| ④ | Lead vào Sheet                 | (máy)      | {{ }} | tức thì| 🟢 AUTO |
| ⑤ | Tin nhắn giá trị 24h           | {{tên}} 🔴 | {{ }} | ≤24h   | 🔴 NGƯỜI |
| ⑥ | Cập nhật trạng thái + phân loại| {{tên}}    | {{ }} | cuối ca| 🟡 ASSISTED |
```

**3 tầng tự động hoá ghi lên Map:**
- 🟢 **AUTO** (máy 100%): form → Sheet · gửi quà tự động (Hermes/Zalo OA) · Thank-you hiện sau khi gửi form.
- 🟡 **ASSISTED** (AI làm, người duyệt ≥30%): copy 9 khối · ruột lead magnet · nháp chuỗi nuôi dưỡng.
- 🔴 **NGƯỜI** (cấm tự động): **tin 24h phải người thật gửi/duyệt — không auto blast** · bằng chứng khối 7 · feedback khách.

## 3. Bản mẫu 🍵 MSX Group (điền sẵn — có tên người thật)

| # | Trạm | Ai | Công cụ | Trong bao lâu | Tầng |
|:-:|---|---|---|:---:|:---:|
| ① | Người xem (bài/video có CTA) | — | Facebook / TikTok | — | — |
| ② | Điền form (6 trường) | Khách | Google Form / Vercel | — | — |
| ③ | Thank You + gửi Bảng so sánh PDF | **Linh** (CSKH MSX) | Zalo OA 0822.928.988 | **≤5'** (ca trực 8h–22h) | 🟢 AUTO (Hermes) / 🔴 NGƯỜI (fallback) |
| ④ | Lead vào Sheet `MSX-Leads` | *(máy)* | Google Sheet | tức thì | 🟢 **AUTO** |
| ⑤ | **Tin nhắn giá trị 24h** | 🔴 **Linh — NGƯỜI THẬT gửi/duyệt** | Zalo | **≤24h** | 🔴 **NGƯỜI — cấm auto blast** |
| ⑥ | Cập nhật trạng thái + phân loại | **Linh**, chủ DN review | Google Sheet | cuối ca | 🟡 ASSISTED |

> **Nhấn:** trạm ③ hôm nay do **Linh** gửi tay (fallback); khi nối **Hermes theo dõi Sheet → nhắn Zalo** thì lên 🟢 AUTO — quà tới <1 phút kể cả 2h sáng (xem [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]]). Trạm ⑤ **mãi mãi là 🔴 NGƯỜI** — hỏi thăm thì người phải hỏi.

## 4. 🔒 Data Security (1 dòng bắt buộc cuối Map)

> **Sheet `MSX-Leads` = tầng Restricted (hạn chế).** Tên + SĐT/Zalo khách chỉ **Linh (trực lead) + chủ DN** được xem — share **theo email cụ thể**, KHÔNG bật "ai có link cũng xem". **Không** chụp màn hình SĐT khách đăng lên group/lớp/fanpage; **không** đưa SĐT vào prompt AI công cộng. Nộp bài: **che 4 số cuối** (`09xx xxx 123`).

## 5. Tiêu chí đạt

- Đủ **6 trạm**, mỗi trạm ③⑤⑥ có **TÊN NGƯỜI THẬT** (không phải "nhân viên").
- Mỗi trạm ghi rõ `[Ai | Công cụ | Thời gian tối đa]` + **tầng AUTO/ASSISTED/NGƯỜI**.
- Trạm ⑤ (tin 24h) ghi rõ **NGƯỜI THẬT gửi/duyệt — không auto blast**.
- Có **dòng Data Security**: lead = Restricted · ai được xem · lưu ở đâu · cấm đăng công khai.

> **Thích ứng ngành:** 6 trạm + luật "tên người thật" + dòng Data Security GIỮ NGUYÊN mọi ngành. B2B (🚀 RocketAI): trạm ③ đổi "gửi quà" thành "xác nhận lịch buổi demo 30'"; trạm ⑤ là founder gọi, không nhắn. Y tế/tài chính: tầng Restricted siết chặt hơn — thêm dòng ai được xoá dữ liệu.

## 🔗 Kết nối

- [[Ngày 12 — Landing Page & Lead Magnet]] · [[Bài Tập Ngày 12 — Landing Page & Lead Magnet]] · [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]]
- [[Template 12.1 — Bảng Chọn Lead Magnet]] · [[Template 12.2 — Landing Page Copy 9 Khối]] · [[Template 12.3 — Cấu Trúc Form Chuẩn + Nối Sheet]]
- Nguyên liệu: [[Template 4.1 — Knowledge Base 10 Thư Mục & Data Security Rule]] (Data Security Rule tầng Restricted)
