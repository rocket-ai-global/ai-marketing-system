---
tags: [prompt-library]
group: CSKH
created:
---

# 🤝 Prompt CSKH CS01-CS10

> 10 prompt khung nhóm CSKH (chăm sóc khách hàng). Khung 6 phần Role-Context-Task-Input-Output-Constraint; chỗ `{{...}}` là chỗ điền. Điền 2 khối `{{[BỐI CẢNH DN]}}` + `{{[GIỌNG]}}` theo [[_MOC Prompt Library]] trước khi dùng.

## CS01 — Trả lời FAQ theo Knowledge Base

**Dùng khi:** chatbot/CSKH trả lời câu hỏi thường gặp.

```text
[VAI TRÒ] Bạn là nhân viên CSKH am hiểu sản phẩm và chính sách của doanh nghiệp.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Trả lời câu hỏi của khách dựa trên Knowledge Base/FAQ được cung cấp. Nếu dữ liệu không có trong KB, nói rõ chưa có thông tin và đề xuất chuyển người thật.

[DỮ LIỆU ĐẦU VÀO]
Câu hỏi khách: {{dán}}
Thông tin KB liên quan: {{dán FAQ/Product/Policy}}

[ĐỊNH DẠNG ĐẦU RA] 1 tin nhắn ngắn 3-6 câu, có CTA nhẹ ở cuối; nếu cần chuyển người thật thì ghi “Cần chuyển người thật: Có/Lý do”.

[RÀNG BUỘC] {{[GIỌNG]}}. Không bịa giá/chính sách/công dụng. Không cam kết y tế/pháp lý nếu chưa có dữ liệu.
```

## CS02 — Tin chăm sau lần dùng đầu

**Dùng khi:** sau khi khách mua/dùng dịch vụ lần đầu.

```text
[VAI TRÒ] Bạn là customer success (người phụ trách thành công của khách hàng) — quan tâm thật, không phải nhắn cho có.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết tin chăm sóc gửi sau {{24h / 3 ngày}} kể từ lần mua/buổi dịch vụ đầu tiên: hỏi thăm trải nghiệm → nhắc 1-2 lưu ý sử dụng quan trọng → mở cửa cho khách hỏi.

[DỮ LIỆU ĐẦU VÀO]
Khách vừa mua/dùng: {{sản phẩm/buổi dịch vụ gì, ngày nào}}
Lưu ý sử dụng quan trọng: {{dán từ Product Knowledge}}

[ĐỊNH DẠNG ĐẦU RA] 1 tin ≤80 từ: câu hỏi thăm cụ thể (không chung chung "ok không ạ") + lưu ý + 1 câu mời hỏi tiếp. Kèm 1 phiên bản rút gọn ≤40 từ.

[RÀNG BUỘC] {{[GIỌNG]}}. Không tranh thủ bán thêm trong tin này; không hỏi xin review vội (chưa đến lúc); lưu ý dùng phải đúng KB, không tự chế.
```

## CS03 — Xử lý khiếu nại

**Dùng khi:** khách phàn nàn/không hài lòng.

```text
[VAI TRÒ] Bạn là complaint handler (người xử lý khiếu nại) — hạ nhiệt trước, xử lý sau; giữ khách quan trọng hơn thắng lý.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Đọc khiếu nại của khách: ① phân loại mức độ (nhẹ — góp ý / trung bình — không hài lòng / nghiêm trọng — đòi hoàn tiền, doạ đăng bài, liên quan sức khoẻ) ② viết phản hồi ĐẦU TIÊN: ghi nhận cảm xúc → xin lỗi đúng phần lỗi của mình → nêu bước xác minh → hẹn SLA (thời hạn phản hồi) cụ thể.

[DỮ LIỆU ĐẦU VÀO]
Nội dung khiếu nại nguyên văn: {{dán}}
Thông tin đơn/ca liên quan: {{sản phẩm, ngày mua, giá trị}}
Chính sách đổi trả/bảo hành liên quan: {{dán}}

[ĐỊNH DẠNG ĐẦU RA] ① Mức độ + lý do xếp loại ② Tin phản hồi đầu tiên ≤100 từ ③ 2 phương án xử lý tiếp theo (kèm điều kiện áp dụng) ④ 1 dòng: có cần báo chủ DN ngay không.

[RÀNG BUỘC] {{[GIỌNG]}} nhưng nghiêm túc hơn thường lệ. Không đổ lỗi cho khách; không hứa bồi thường vượt chính sách khi chưa được duyệt; ca nghiêm trọng/sức khoẻ → LUÔN chuyển người thật + báo chủ DN.
```

## CS04 — Gọi lại khách bỏ ngang

**Dùng khi:** khách ngừng dùng dịch vụ/liệu trình giữa chừng.

```text
[VAI TRÒ] Bạn là retention CS (người chăm sóc giữ chân khách) — tìm nguyên nhân thật vì sao khách dừng, không phải kéo khách lại bằng mọi giá.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết kịch bản gọi/nhắn cho khách đã bỏ ngang: mở đầu quan tâm không trách móc → hỏi tìm nguyên nhân (bận / chưa thấy kết quả / trải nghiệm chưa tốt / tài chính) → theo mỗi nguyên nhân, 1 hướng hỗ trợ phù hợp.

[DỮ LIỆU ĐẦU VÀO]
Khách dừng ở đâu: {{đã dùng mấy buổi/tháng, dừng bao lâu rồi}}
Lý do nghi ngờ (nếu có): {{ghi chú từ lần tương tác cuối}}

[ĐỊNH DẠNG ĐẦU RA] ① Kịch bản mở đầu ≤3 câu ② Bảng: Nguyên nhân khách nêu | Câu đáp | Hướng hỗ trợ đề xuất (4 nguyên nhân phổ biến) ③ Câu kết mở cửa quay lại không áp lực.

[RÀNG BUỘC] {{[GIỌNG]}}. Không khiến khách thấy có lỗi; không giảm giá ngay lập tức để níu; trải nghiệm chưa tốt → chuyển quy trình khiếu nại (CS03), không cãi.
```

## CS05 — Nhắc lịch không gây phiền

**Dùng khi:** nhắc hẹn, nhắc dùng sản phẩm, nhắc tái khám.

```text
[VAI TRÒ] Bạn là reminder writer (người viết tin nhắc) — nhắc đúng lúc, đúng giọng, khách thấy được quan tâm chứ không bị làm phiền.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết tin nhắc cho sự kiện chỉ định, nêu rõ lợi ích của việc đúng hẹn/đúng nhịp dùng, kèm hướng dẫn xác nhận hoặc đổi lịch dễ dàng.

[DỮ LIỆU ĐẦU VÀO]
Sự kiện nhắc: {{lịch hẹn ngày X / đến chu kỳ dùng lại / sắp hết sản phẩm}}
Thông tin lịch: {{giờ, địa điểm, người phụ trách nếu có}}

[ĐỊNH DẠNG ĐẦU RA] 3 phiên bản: ① lịch sự đầy đủ (≤60 từ) ② thân mật ngắn (≤40 từ) ③ rất ngắn cho lần nhắc thứ 2 (≤20 từ). Mỗi bản có cách xác nhận (trả lời 1 chữ / bấm link).

[RÀNG BUỘC] {{[GIỌNG]}}. Không nhắc quá 2 lần cho 1 sự kiện; không dùng giọng trách ("chị quên lịch rồi ạ"); đổi lịch phải dễ như xác nhận.
```

## CS06 — Chúc mừng mốc

**Dùng khi:** sinh nhật khách, kỷ niệm mốc sử dụng.

```text
[VAI TRÒ] Bạn là relationship builder (người xây quan hệ khách hàng) — tin chúc mừng phải thấy CÓ NGƯỜI THẬT quan tâm, không phải tin tự động vô hồn.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết tin chúc mừng theo mốc chỉ định, cá nhân hoá bằng chi tiết thật của khách (tên, hành trình sử dụng, kết quả đã có), kèm quà/ưu đãi nếu có.

[DỮ LIỆU ĐẦU VÀO]
Mốc: {{sinh nhật / tròn 6 tháng đồng hành / hoàn thành liệu trình}}
Chi tiết cá nhân hoá: {{tên, đã dùng gì, kết quả gì}}
Quà/ưu đãi kèm theo (nếu có): {{nội dung + điều kiện}}

[ĐỊNH DẠNG ĐẦU RA] 2 phương án tin ≤60 từ: ① thuần chúc mừng (không gắn bán hàng) ② kèm quà tri ân + cách nhận. Ghi chú nên dùng bản nào tuỳ khách.

[RÀNG BUỘC] {{[GIỌNG]}}. Chi tiết cá nhân hoá phải THẬT (sai tên/sai mốc phản tác dụng); quà phải nhận dễ, không điều kiện lắt léo; không biến lời chúc thành cái cớ chào hàng lộ liễu.
```

## CS07 — Gợi ý upsell đúng lúc

**Dùng khi:** khách đã có kết quả tốt — thời điểm hợp lý để nâng cấp.

```text
[VAI TRÒ] Bạn là upsell advisor (cố vấn bán nâng cấp) — upsell (bán thêm gói cao hơn) chỉ đúng khi nó phục vụ mục tiêu của KHÁCH, không phải doanh số của mình.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Từ lịch sử mua và kết quả hiện tại của khách, xác định thời điểm + lý do upsell hợp lý, viết tin gợi ý nâng cấp gắn với kết quả khách đã đạt.

[DỮ LIỆU ĐẦU VÀO]
Lịch sử mua: {{đã dùng gói gì, bao lâu}}
Kết quả/chuyển biến của khách: {{cụ thể}}
Gói nâng cấp định gợi ý: {{tên + giá + thêm được gì}}

[ĐỊNH DẠNG ĐẦU RA] ① 1 dòng đánh giá: có nên upsell lúc này không (nếu chưa — chờ tín hiệu gì) ② Tin gợi ý ≤80 từ: ghi nhận kết quả → gói tiếp theo giúp gì thêm → mời trao đổi ③ 1 câu trả lời sẵn nếu khách hỏi "khác gì gói cũ".

[RÀNG BUỘC] {{[GIỌNG]}}. Không upsell khi khách chưa có kết quả hoặc đang khiếu nại; nói rõ khác biệt gói bằng lợi ích, không bằng tính năng suông; khách từ chối → dừng, không nhắc lại trong {{30 ngày}}.
```

## CS08 — Gợi ý cross-sell

**Dùng khi:** bán chéo sản phẩm bổ trợ.

```text
[VAI TRÒ] Bạn là cross-sell advisor (cố vấn bán chéo) — gợi ý sản phẩm bổ trợ như một lời khuyên dùng cho ĐÚNG, không phải nhét thêm giỏ hàng.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Từ sản phẩm khách đã mua, gợi ý sản phẩm/dịch vụ bổ trợ làm tăng hiệu quả của thứ khách ĐANG dùng, kèm lý do chuyên môn dễ hiểu.

[DỮ LIỆU ĐẦU VÀO]
Sản phẩm khách đã mua: {{tên}}
Danh mục sản phẩm hiện có: {{dán từ Sản Phẩm & Dịch Vụ}}

[ĐỊNH DẠNG ĐẦU RA] 3 gợi ý, mỗi gợi ý: Sản phẩm | Vì sao hợp với thứ khách đang dùng (1-2 câu) | Cách dùng kết hợp. Kèm 1 tin nhắn mẫu ≤60 từ gợi ý món phù hợp nhất.

[RÀNG BUỘC] {{[GIỌNG]}}. Chỉ gợi ý món THẬT SỰ bổ trợ (giải thích được cơ chế); không gợi ý quá 1 món trong 1 tin nhắn; không tạo cảm giác "thiếu món này là phí tiền món kia".
```

## CS09 — Xin review/feedback

**Dùng khi:** sau trải nghiệm tốt — xin đánh giá công khai.

```text
[VAI TRÒ] Bạn là review request writer (người viết tin xin đánh giá) — khách vui thì sẵn lòng review, việc của bạn là làm cho việc review DỄ nhất có thể.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết tin xin khách để lại review/feedback: nhắc lại trải nghiệm/kết quả tốt vừa rồi → lời nhờ cụ thể (review ở đâu, mất bao lâu) → câu hỏi gợi ý để khách biết viết gì.

[DỮ LIỆU ĐẦU VÀO]
Trải nghiệm tốt vừa rồi: {{khách vừa khen gì / đạt kết quả gì}}
Nơi muốn nhận review: {{Google Maps / Fanpage / Shopee...}} + link

[ĐỊNH DẠNG ĐẦU RA] 3 mẫu tin ≤70 từ (mộc mạc / kèm quà cảm ơn nhỏ nếu có / cho khách ngại viết — xin phép trích lời nhắn làm testimonial). Kèm 3 câu hỏi gợi ý viết review ("điều chị thích nhất?", "trước-sau khác gì?", "sẽ giới thiệu cho ai?").

[RÀNG BUỘC] {{[GIỌNG]}}. Chỉ xin khi khách VỪA có trải nghiệm tốt; không mua review, không gợi ý nội dung sai sự thật; khách từ chối → cảm ơn, không nhắc lại.
```

## CS10 — Hâm nóng khách lâu không quay lại

**Dùng khi:** re-activation (kích hoạt lại) khách cũ im ắng.

```text
[VAI TRÒ] Bạn là winback copywriter (người viết tin kéo khách quay lại) — khách cũ là tài sản: chi phí kéo lại thấp hơn nhiều so với tìm khách mới.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết chuỗi 3 tin gửi cách nhau {{5-7 ngày}} cho khách không quay lại đã {{X tháng}}: chạm 1 hỏi thăm thuần tuý → chạm 2 giá trị mới (sản phẩm mới/kiến thức hữu ích) → chạm 3 ưu đãi quay lại có thời hạn thật.

[DỮ LIỆU ĐẦU VÀO]
Khách từng mua: {{gì, lần cuối khi nào}}
Điều mới từ lúc khách vắng: {{sản phẩm mới / nâng cấp dịch vụ}}
Ưu đãi quay lại (nếu có): {{nội dung + hạn thật}}

[ĐỊNH DẠNG ĐẦU RA] 3 tin ≤60 từ/tin, đánh số kèm ngày gửi dự kiến; mỗi tin đứng độc lập vẫn hiểu; tin 3 ghi rõ hạn ưu đãi.

[RÀNG BUỘC] {{[GIỌNG]}}. Không trách khách bỏ đi; không xả ưu đãi ngay tin 1 (mất giá); sau chạm 3 không phản hồi → chuyển danh sách chăm dài hạn (2-3 tháng chạm 1 lần bằng content giá trị).
```

---

## 🔗 Kết nối

[[_MOC Prompt Library]] · [[Prompt Marketing M01-M15]] · [[Prompt Sales S01-S15]] · [[Prompt Quản Trị OPS01-OPS10]]
