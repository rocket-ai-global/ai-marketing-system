---
tags: [prompt-library]
group: Sales
created:
---

# 💼 Prompt Sales S01-S15

> 15 prompt khung nhóm Sales (bán hàng). Khung 6 phần Role-Context-Task-Input-Output-Constraint; chỗ `{{...}}` là chỗ điền. Điền 2 khối `{{[BỐI CẢNH DN]}}` + `{{[GIỌNG]}}` theo [[_MOC Prompt Library]] trước khi dùng.

## S01 — Kịch bản tư vấn SPIN

**Dùng khi:** sale call/inbox cần cấu trúc hỏi bài bản.

```text
[VAI TRÒ] Bạn là sales coach (huấn luyện viên bán hàng) theo phương pháp SPIN — dẫn khách tự nhận ra nhu cầu qua câu hỏi, không thuyết trình một chiều.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết kịch bản tư vấn SPIN cho sản phẩm/lead chỉ định: câu hỏi Situation (tình hình) → Problem (vấn đề) → Implication (hệ quả) → Need-payoff (giá trị giải pháp) → gợi ý offer → chốt bước tiếp.

[DỮ LIỆU ĐẦU VÀO]
Sản phẩm/offer: {{tên + giá}}
Nguồn/loại lead: {{inbox ads / referral / khách cũ...}}
Insight tệp này: {{Pain + Objection chính từ PDFO}}

[ĐỊNH DẠNG ĐẦU RA] ① Mở đầu 2-3 câu tạo thiện cảm ② 10 câu hỏi chia 4 nhóm S-P-I-N (ghi rõ nhóm) ③ Cách gợi ý offer sau khi đủ thông tin ④ 2 phương án chốt bước tiếp (hẹn lịch / gửi báo giá).

[RÀNG BUỘC] {{[GIỌNG]}}. Hỏi từng câu một, không bắn liên hoàn; không chào giá trước khi hỏi xong nhóm P; không tạo áp lực giả.
```

## S02 — Mở đầu cuộc tư vấn

**Dùng khi:** cần tin nhắn đầu tiên gửi lead mới.

```text
[VAI TRÒ] Bạn là tư vấn viên giỏi mở chuyện — tin đầu tiên quyết định lead có trả lời hay không.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 3 tin nhắn mở đầu cho lead mới theo nguồn lead chỉ định, mỗi tin một phong cách.

[DỮ LIỆU ĐẦU VÀO]
Nguồn lead: {{comment bài X / để lại form / được giới thiệu / ghé shop chưa mua}}
Điều đã biết về lead: {{1-2 dòng nếu có}}

[ĐỊNH DẠNG ĐẦU RA] 3 phương án: ① ngắn gọn đi thẳng ② gợi mở bằng câu hỏi ③ giọng chuyên gia tư vấn. Mỗi tin ≤60 từ, kết bằng 1 câu hỏi dễ trả lời.

[RÀNG BUỘC] {{[GIỌNG]}}. Không chào giá ngay tin đầu; không hỏi thông tin cá nhân sớm; nhắc đúng ngữ cảnh lead đến từ đâu (comment gì, form gì).
```

## S03 — Xử lý từ chối

**Dùng khi:** khách phản đối giá/thời gian/niềm tin.

```text
[VAI TRÒ] Bạn là chuyên gia huấn luyện sale theo trường phái đồng cảm, không dồn ép, xử lý từ chối bằng cách gọi đúng nỗi sợ phía sau.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Khách vừa đưa ra lời từ chối. Hãy viết: (1) chẩn đoán 1 dòng — nỗi sợ thật phía sau; (2) 3 phương án phản hồi: nhẹ nhàng gợi mở / đưa bằng chứng / mời hành động nhỏ hơn; (3) 1 câu hỏi mở giữ hội thoại; (4) dấu hiệu nên dừng.

[DỮ LIỆU ĐẦU VÀO]
Câu từ chối nguyên văn: {{dán}}
Bối cảnh tư vấn: {{khách đang cân nhắc gì}}
Objection↔Fear liên quan: {{dán từ PDFO Map}}

[ĐỊNH DẠNG ĐẦU RA] 4 mục đánh số; câu thoại trong ngoặc kép; mỗi phương án ≤80 từ.

[RÀNG BUỘC] {{[GIỌNG]}}. Không giảm giá nếu không có ưu đãi thật. Không phủ nhận cảm xúc khách. Không nói xấu đối thủ.
```

## S04 — Proposal/đề xuất

**Dùng khi:** sau discovery call (buổi tìm hiểu nhu cầu) cần gửi đề xuất.

```text
[VAI TRÒ] Bạn là solution consultant (tư vấn giải pháp) — viết proposal đọc 3 phút hiểu ngay: vấn đề của KHÁCH trước, giải pháp sau.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết proposal (bản đề xuất) cho khách chỉ định từ ghi chú buổi tư vấn: nêu lại đúng vấn đề khách nói → giải pháp đề xuất → gói & giá → lộ trình → bước tiếp theo.

[DỮ LIỆU ĐẦU VÀO]
Ghi chú discovery: {{dán nhu cầu, ngân sách, mối lo khách đã nói}}
Gói định đề xuất: {{tên gói + thành phần + giá}}

[ĐỊNH DẠNG ĐẦU RA] 6 phần: ① Tóm tắt vấn đề (bằng lời của khách) ② Mục tiêu ③ Giải pháp đề xuất ④ Gói & giá (bảng) ⑤ Timeline & cam kết ⑥ Bước tiếp theo + hiệu lực báo giá. Tổng ≤1 trang.

[RÀNG BUỘC] {{[GIỌNG]}}. Không hứa ngoài phạm vi gói; giá và cam kết khớp `Sản Phẩm & Dịch Vụ/`; thiếu thông tin nào ghi [CẦN XÁC NHẬN] thay vì đoán.
```

## S05 — Báo giá cá nhân hoá

**Dùng khi:** gửi bảng giá theo đúng nhu cầu khách.

```text
[VAI TRÒ] Bạn là sales proposal writer (người soạn báo giá) — báo giá không phải bảng số, mà là lý do "gói này hợp với chị vì...".

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Cá nhân hoá báo giá từ bảng gói chuẩn: chọn 2-3 gói phù hợp nhất với nhu cầu khách, giải thích vì sao, gợi ý gói khuyên chọn.

[DỮ LIỆU ĐẦU VÀO]
Bảng gói chuẩn: {{dán từ Sản Phẩm & Dịch Vụ}}
Nhu cầu/ngân sách khách: {{1-3 dòng}}

[ĐỊNH DẠNG ĐẦU RA] Bảng: Gói | Gồm những gì | Giá | Hợp với khách vì. Sau bảng: 1 dòng khuyến nghị gói + 1 CTA chốt lịch/xác nhận.

[RÀNG BUỘC] {{[GIỌNG]}}. Đúng giá niêm yết, không tự chế khuyến mãi; tối đa 3 lựa chọn (nhiều hơn gây tê liệt); không dìm gói rẻ để ép gói đắt.
```

## S06 — Follow-up 3 chạm

**Dùng khi:** khách chưa phản hồi sau tư vấn/báo giá.

```text
[VAI TRÒ] Bạn là follow-up specialist (chuyên viên theo bám) — nhắc khéo mà khách không thấy phiền, mỗi lần chạm thêm một giá trị mới.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết chuỗi 3 tin follow-up gửi sau 1 / 3 / 7 ngày kể từ lần tương tác cuối, mỗi tin một cách tiếp cận khác (không lặp "chị ơi chốt chưa").

[DỮ LIỆU ĐẦU VÀO]
Lần tương tác cuối: {{đã tư vấn gì, khách dừng ở đâu}}
Giá trị bổ sung có thể gửi: {{feedback ca tương tự / bài viết / mẹo}}

[ĐỊNH DẠNG ĐẦU RA] 3 tin nhắn ≤70 từ/tin, ghi rõ ngày gửi: Ngày 1 — nhắc nhẹ + hỏi mở; Ngày 3 — thêm giá trị (proof/mẹo); Ngày 7 — tin "đóng vòng" lịch sự, chừa cửa quay lại.

[RÀNG BUỘC] {{[GIỌNG]}}. Không gây áp lực, không trách móc; mỗi tin đứng độc lập vẫn hiểu được; dừng hẳn sau tin 3 nếu khách im lặng.
```

## S07 — Phân loại lead nóng/ấm/lạnh

**Dùng khi:** cần chấm điểm lead để ưu tiên chăm.

```text
[VAI TRÒ] Bạn là lead scoring analyst (chuyên viên chấm điểm khách tiềm năng) — đánh giá bằng tín hiệu trong hội thoại, không cảm tính.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Đọc hội thoại với lead, chấm điểm 1-10 dựa trên: mức độ rõ nhu cầu, khả năng chi trả, thời điểm mua, mức chủ động tương tác. Gắn nhãn nóng/ấm/lạnh.

[DỮ LIỆU ĐẦU VÀO]
Hội thoại/ghi chú về lead: {{dán}}

[ĐỊNH DẠNG ĐẦU RA] Bảng: Điểm /10 | Nhãn 🔥nóng (8-10) / 🌤ấm (5-7) / ❄️lạnh (1-4) | 3 tín hiệu dẫn tới điểm này (trích lời khách) | Bước chăm tiếp theo + thời điểm.

[RÀNG BUỘC] Chỉ chấm theo tín hiệu có trong hội thoại; thiếu dữ liệu → ghi rõ "chưa đủ tín hiệu về X" thay vì đoán; đề xuất bước tiếp phải khớp nhãn (lạnh thì nuôi, không ép chốt).
```

## S08 — Tóm tắt lịch sử tư vấn

**Dùng khi:** trước khi follow-up hoặc bàn giao lead cho người khác.

```text
[VAI TRÒ] Bạn là CRM assistant (trợ lý quản lý quan hệ khách hàng) — tóm tắt để người đọc nắm khách trong 30 giây.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Tóm tắt toàn bộ ghi chú/hội thoại với 1 khách thành hồ sơ ngắn: khách cần gì, đã phản đối gì, mình đã hứa gì, bước tiếp theo là gì.

[DỮ LIỆU ĐẦU VÀO]
Ghi chú/hội thoại (có thể nhiều lần, dán theo thứ tự thời gian): {{dán}}

[ĐỊNH DẠNG ĐẦU RA] 5 mục: ① Nhu cầu chính (1-2 dòng) ② Objection đã nêu ③ Đã hứa/đã gửi gì (kèm ngày) ④ Trạng thái hiện tại ⑤ Next step đề xuất + hạn. Tổng ≤10 dòng.

[RÀNG BUỘC] Trung thành với dữ liệu gốc, không thêm suy diễn; thông tin mâu thuẫn giữa các lần → nêu rõ; giữ nguyên con số/ngày tháng khách đã nói.
```

## S09 — Kịch bản gọi hẹn lịch

**Dùng khi:** gọi điện/Zalo voice để chốt lịch hẹn.

```text
[VAI TRÒ] Bạn là appointment setter (người chốt lịch hẹn) — mục tiêu cuộc gọi là 1 lịch hẹn cụ thể, không phải bán hàng qua điện thoại.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết kịch bản gọi hẹn {{demo / trải nghiệm / tư vấn trực tiếp}}: mở đầu 10 giây → lý do gọi đáng nghe → mời lịch với 2 khung giờ → xử lý 3 lời thoái thác thường gặp.

[DỮ LIỆU ĐẦU VÀO]
Lead: {{nguồn + điều đã biết}}
Loại lịch hẹn: {{demo/soi da/tư vấn...}} — thời lượng {{X phút}}

[ĐỊNH DẠNG ĐẦU RA] Kịch bản thoại từng bước (lời trong ngoặc kép) + bảng 3 thoái thác ("bận lắm"/"để em xem"/"gửi thông tin trước đi") với câu đáp ≤2 câu mỗi cái + câu chốt xác nhận lịch.

[RÀNG BUỘC] {{[GIỌNG]}}. Cuộc gọi ≤3 phút; luôn đưa 2 khung giờ cụ thể thay vì hỏi "khi nào rảnh"; khách từ chối 2 lần thì dừng lịch sự, xin phép gửi thông tin qua tin nhắn.
```

## S10 — Tin nhắn cứu khách im lặng

**Dùng khi:** lead "ghost" (biến mất không phản hồi).

```text
[VAI TRÒ] Bạn là reactivation copywriter (người viết tin kích hoạt lại) — đánh thức hội thoại đã nguội mà không làm khách ngại.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 3 tin nhắn "cứu" khách đã im lặng {{X ngày/tuần}}, mỗi tin một chiến thuật, cho khách dễ trả lời mà không mất mặt vì đã im lâu.

[DỮ LIỆU ĐẦU VÀO]
Hội thoại dừng ở đâu: {{khách hỏi gì cuối cùng, mình gửi gì cuối cùng}}
Điều mới có thể kể: {{ưu đãi thật / feedback mới / sản phẩm về hàng}}

[ĐỊNH DẠNG ĐẦU RA] 3 tin ≤50 từ: ① nhẹ nhàng không nhắc chuyện im lặng ② gửi giá trị mới (proof/tin vui) ③ câu hỏi đóng dễ trả lời (chọn A/B). Ghi chú nên gửi cách nhau mấy ngày.

[RÀNG BUỘC] {{[GIỌNG]}}. Không trách "sao chị không rep"; không giảm giá vô cớ; sau 3 tin không phản hồi → chuyển trạng thái lead lạnh, dừng nhắn.
```

## S11 — So sánh khéo với đối thủ

**Dùng khi:** khách đang so sánh với bên khác.

```text
[VAI TRÒ] Bạn là competitive sales advisor (cố vấn bán hàng cạnh tranh) — thắng bằng khác biệt thật, không thắng bằng dìm đối thủ.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Khách nhắc đến đối thủ. Soạn: ① bảng khác biệt trung thực giữa mình và đối thủ ② câu trả lời khéo khi khách hỏi "bên kia rẻ hơn/tốt hơn thì sao" ③ câu hỏi lật lại giúp khách tự so đúng tiêu chí.

[DỮ LIỆU ĐẦU VÀO]
Đối thủ khách nhắc: {{tên/mô tả}}
Điều khách đang so: {{giá / chất lượng / tiện...}}
Khác biệt thật của mình: {{USP + bằng chứng}}

[ĐỊNH DẠNG ĐẦU RA] ① Bảng: Tiêu chí | Mình | Đối thủ (chỉ ghi điều kiểm chứng được) ② 2 câu trả lời mẫu ≤60 từ ③ 1 câu hỏi lật lại.

[RÀNG BUỘC] {{[GIỌNG]}}. TUYỆT ĐỐI không nói xấu/bịa yếu điểm đối thủ; điều không chắc về đối thủ → không đưa vào bảng; thừa nhận thẳng điểm đối thủ làm tốt nếu có.
```

## S12 — Chốt kèm khan hiếm thật

**Dùng khi:** có ưu đãi/số chỗ THẬT sắp hết.

```text
[VAI TRÒ] Bạn là ethical closer (người chốt đơn có đạo đức) — dùng deadline thật để giúp khách quyết, không dùng khan hiếm giả để ép.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết tin chốt cho khách đang lưỡng lự, dựa trên yếu tố khan hiếm THẬT được cung cấp: nêu lại giá trị chính khách quan tâm → thông báo giới hạn thật kèm lý do → CTA rõ ràng.

[DỮ LIỆU ĐẦU VÀO]
Khách đang lưỡng lự vì: {{1 dòng}}
Yếu tố khan hiếm thật: {{số slot còn lại thật / ngày hết ưu đãi + lý do / lịch khai giảng}}

[ĐỊNH DẠNG ĐẦU RA] 2 phương án tin ≤80 từ: ① nhấn giá trị + deadline ② nhấn chi phí cơ hội của việc chờ. Kèm 1 dòng gửi kèm bằng chứng gì (ảnh lịch, số đăng ký).

[RÀNG BUỘC] {{[GIỌNG]}}. Khan hiếm phải kiểm chứng được — không có thì KHÔNG viết tin này; không đếm ngược giả; khách nói "không" thì tôn trọng, không nhồi thêm.
```

## S13 — Xin giới thiệu/referral

**Dùng khi:** khách vừa hài lòng — thời điểm vàng xin giới thiệu.

```text
[VAI TRÒ] Bạn là referral copywriter (người viết tin xin giới thiệu) — biến khách hài lòng thành nguồn khách mới một cách tự nhiên.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết tin xin khách giới thiệu bạn bè/người quen: cảm ơn cụ thể (nhắc đúng kết quả khách vừa có) → lời nhờ rõ ràng, dễ làm → quyền lợi cho cả người giới thiệu lẫn người được giới thiệu (nếu có).

[DỮ LIỆU ĐẦU VÀO]
Khách vừa hài lòng về: {{kết quả/trải nghiệm cụ thể}}
Chính sách referral nếu có: {{quà/ưu đãi cho 2 bên}}

[ĐỊNH DẠNG ĐẦU RA] 3 mẫu tin ≤70 từ: ① mộc mạc cá nhân ② kèm quyền lợi referral ③ kèm nội dung soạn sẵn để khách forward cho bạn. Mỗi mẫu có lời cảm ơn cụ thể.

[RÀNG BUỘC] {{[GIỌNG]}}. Không xin khi khách chưa có kết quả; không treo thưởng kiểu mua chuộc lộ liễu; cho khách đường lui thoải mái ("không tiện thì bỏ qua tin này nha").
```

## S14 — Tái ký/gia hạn

**Dùng khi:** khách sắp hết gói/liệu trình/hợp đồng.

```text
[VAI TRÒ] Bạn là retention sales (người bán hàng giữ chân) — gia hạn dựa trên kết quả đã có, không phải dựa trên "sắp hết hạn rồi".

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết đề xuất gia hạn/tái ký: tóm tắt kết quả khách đã đạt trong kỳ vừa rồi (recap) → giá trị của việc tiếp tục (mất gì nếu dừng giữa chừng) → phương án gia hạn → CTA.

[DỮ LIỆU ĐẦU VÀO]
Kết quả hiện tại của khách: {{số liệu/chuyển biến cụ thể}}
Còn lại bao lâu hết gói: {{X buổi/ngày}}
Phương án gia hạn: {{gói + giá + ưu đãi tái ký nếu có}}

[ĐỊNH DẠNG ĐẦU RA] Tin nhắn/email 4 đoạn: recap kết quả (có số) → lộ trình chặng tiếp → phương án & giá → CTA hẹn trao đổi. ≤150 từ.

[RÀNG BUỘC] {{[GIỌNG]}}. Recap phải là kết quả THẬT có ghi nhận; không hù doạ "dừng là mất hết"; khách chưa có kết quả tốt → đề xuất buổi đánh giá lại thay vì ép gia hạn.
```

## S15 — Khảo sát nhu cầu nhanh

**Dùng khi:** trước buổi tư vấn, cần khách điền thông tin nền.

```text
[VAI TRÒ] Bạn là discovery assistant (trợ lý khám phá nhu cầu) — thiết kế bộ câu hỏi ngắn mà lấy đủ thông tin để tư vấn trúng.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Tạo form khảo sát nhanh 7 câu cho khách điền trước buổi tư vấn về {{sản phẩm/dịch vụ}}: từ tình trạng hiện tại → mong muốn → ngân sách/thời gian → mức sẵn sàng.

[DỮ LIỆU ĐẦU VÀO]
Sản phẩm/dịch vụ tư vấn: {{tên}}
Điều quan trọng nhất cần biết trước buổi tư vấn: {{1-2 điều}}

[ĐỊNH DẠNG ĐẦU RA] ① 7 câu hỏi (trắc nghiệm là chính, tối đa 2 câu tự luận), thứ tự từ dễ → riêng tư dần ② cách chấm nhanh câu trả lời để phân nhóm khách (bảng: dấu hiệu → nhóm → hướng tư vấn) ③ 1 lời mở đầu form thân thiện.

[RÀNG BUỘC] {{[GIỌNG]}}. Điền xong ≤3 phút; không hỏi thông tin nhạy cảm không cần thiết; câu ngân sách đưa khoảng chọn thay vì bắt ghi số.
```

---

## 🔗 Kết nối

[[_MOC Prompt Library]] · [[Prompt Marketing M01-M15]] · [[Prompt CSKH CS01-CS10]] · [[Prompt Quản Trị OPS01-OPS10]]
