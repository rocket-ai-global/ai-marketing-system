---
tags: [data-security, msx, demo]
created: 2026-07-12
---

# Data Access & Security Rule — Mẫu Sơn Xanh

## Nguyên tắc

AI chỉ được đọc dữ liệu cần thiết để tư vấn sản phẩm, content, sales và CSKH. Không đưa dữ liệu cá nhân/đơn hàng nhạy cảm vào AI nếu chưa ẩn thông tin.

| Nhóm dữ liệu | Ai được xem? | Ai được sửa? | Có nạp vào AI? |
|---|---|---|---|
| Product Knowledge, giá public | Sales, Marketing, CSKH | Chủ DN/Leader | Có |
| FAQ & Objection | Sales, CSKH, Marketing | Leader CSKH/Sales | Có |
| Brand Voice, Content | Marketing | Chủ DN/Marketing Lead | Có |
| Chính sách giao hàng/đổi trả/thanh toán | Sales, CSKH | Chủ DN/Admin | Có |
| Số điện thoại, địa chỉ khách | Sales/CSKH phụ trách | Không đưa vào AI public | Không, trừ khi ẩn định danh |
| Doanh thu, chiết khấu đại lý | Chủ DN/Kế toán/Sales Lead | Chủ DN | Hạn chế |
| Hợp đồng đại lý | Chủ DN/Sales Lead | Chủ DN/Pháp lý | Không nạp bừa |
| Khiếu nại nhạy cảm | Chủ DN/CSKH Lead | Chủ DN/CSKH Lead | Tóm tắt ẩn danh nếu cần học FAQ |

## Dữ liệu được phép dùng để demo lớp học

- Mô tả sản phẩm, giá public, FAQ public, chính sách public, content công khai.
- Persona/KPI giả lập demo đã đánh dấu rõ.

## Dữ liệu không dùng để demo lớp học

- Thông tin khách hàng thật chưa xin phép.
- Số đơn, doanh thu, hợp đồng thật nếu chưa được chủ DN cho phép.
