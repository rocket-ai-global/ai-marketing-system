---
tags: [prompt-library]
created:
---

# 🗂️ _MOC Prompt Library — 50 Prompt Khung

> Thư viện 50 prompt (câu lệnh) khung cho 4 mảng vận hành của doanh nghiệp. Bạn KHÔNG viết prompt từ số 0 — bạn điền 2 khối ngữ cảnh 1 lần, rồi cá nhân hoá ≥20 prompt và test ≥10 (Ngày 05). Nguồn khung: Template 5.1 của chương trình 28 Day AIOS.

## Quy ước mã

| Mã | Nhóm | File | Số lượng |
|---|---|---|---|
| **M** | Marketing | [[Prompt Marketing M01-M15]] | 15 |
| **S** | Sales (bán hàng) | [[Prompt Sales S01-S15]] | 15 |
| **CS** | CSKH (chăm sóc khách hàng) | [[Prompt CSKH CS01-CS10]] | 10 |
| **OPS** | Quản trị (operations — vận hành) | [[Prompt Quản Trị OPS01-OPS10]] | 10 |

Mọi prompt theo **khung chuẩn 6 phần**: `[VAI TRÒ]` (Role) → `[BỐI CẢNH]` (Context) → `[NHIỆM VỤ]` (Task) → `[DỮ LIỆU ĐẦU VÀO]` (Input) → `[ĐỊNH DẠNG ĐẦU RA]` (Output) → `[RÀNG BUỘC]` (Constraint). Chỗ `{{...}}` là chỗ bạn điền.

**Quy tắc chẩn đoán khi output chưa ưng** (theo [[_Chuẩn Đồng Bộ Tuần 1]]): sai KIỂU → sửa Output/Constraint · sai NỘI DUNG → sửa Context/Input · NÔNG → sửa Role/Task.

## ⚠️ Điền 2 khối này TRƯỚC khi dùng bất kỳ prompt nào

Mọi prompt đều gọi `{{[BỐI CẢNH DN]}}` và `{{[GIỌNG]}}`. Điền 1 lần tại đây, sau đó copy-dán vào chỗ tương ứng của từng prompt — "cá nhân hoá 20 prompt" thực chất là dán 2 khối này. Chất liệu rút từ `00. Business Context/` (Business Snapshot + Brand Voice).

### [BỐI CẢNH DN] (≤130 từ)

```text
[BỐI CẢNH DN]
Doanh nghiệp: {{tên DN}}, ngành {{ngành}}, địa bàn {{địa bàn}}, quy mô {{nhân sự/doanh thu nếu có}}.
Khách mục tiêu chính: {{1-2 nhóm khách hàng quan trọng nhất}}.
Sản phẩm/offer chủ lực: {{tên sản phẩm/gói}}, giá {{giá}}, kết quả/kỳ vọng chính {{kết quả}}.
Kênh bán/marketing chính: {{Facebook/Zalo/TikTok/Website/Referral/Offline...}}.
Nỗi sợ/rào cản lớn nhất của khách: {{fear/objection chính}}.
Điểm khác biệt: {{USP quan trọng nhất}}.
Điều không bao giờ hứa/nói: {{cam kết cấm, claim y tế/pháp lý, giá chưa xác nhận...}}.
```

### [GIỌNG] (≤80 từ)

```text
[GIỌNG]
Xưng hô: {{em/anh/chị/mình...}}.
Tính cách giọng: {{ấm áp/thẳng thắn/chuyên gia/gần gũi...}}.
Từ/cụm từ nên dùng: {{5 cụm từ đặc trưng}}.
Điều cấm: {{từ sáo rỗng, emoji quá nhiều, cam kết quá đà, chê bai đối thủ...}}.
```

## Bảng nghiệm thu test (≥10 prompt, phủ ≥3 nhóm — ghi 1 dòng kết quả/prompt)

| # | Mã prompt | Input đã dùng | Output dùng được ngay? | Cần sửa gì? | Trạng thái |
|---|---|---|:---:|---|---|
| 1 | | | | | Chưa test |
| 2 | | | | | Chưa test |
| 3 | | | | | Chưa test |
| 4 | | | | | Chưa test |
| 5 | | | | | Chưa test |
| 6 | | | | | Chưa test |
| 7 | | | | | Chưa test |
| 8 | | | | | Chưa test |
| 9 | | | | | Chưa test |
| 10 | | | | | Chưa test |

## Tiêu chí đạt (Ngày 05)

- Đủ 50 prompt khung trong 4 file nhóm.
- 2 khối `[BỐI CẢNH DN]` + `[GIỌNG]` đã điền (đúng giới hạn từ).
- ≥20 prompt đã cá nhân hoá · ≥10 prompt đã test, phủ ≥3 nhóm.
- Prompt "Chưa đạt" có ghi chú "sửa gì" và chạy lại ≥1 lần.
