---
tags: [prompt-library]
group: Marketing
created:
---

# 📣 Prompt Marketing M01-M15

> 15 prompt khung nhóm Marketing. Khung 6 phần Role-Context-Task-Input-Output-Constraint; chỗ `{{...}}` là chỗ điền. Điền 2 khối `{{[BỐI CẢNH DN]}}` + `{{[GIỌNG]}}` theo [[_MOC Prompt Library]] trước khi dùng.

## M01 — Viết bài Facebook theo angle

**Dùng khi:** cần 1 bài social bán mềm/giáo dục.

```text
[VAI TRÒ] Bạn là copywriter mạng xã hội cho SME tại Việt Nam, viết bài Facebook tự nhiên như người thật chia sẻ.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 1 bài Facebook theo angle được chỉ định: mở bằng hook chạm tâm lý trong 2 dòng đầu → thân bài dẫn bằng ví dụ/câu chuyện đời thường, cài 1 thông tin chuyên môn dễ hiểu → kết bằng CTA.

[DỮ LIỆU ĐẦU VÀO]
Chủ đề: {{chủ đề}}
Angle: {{nỗi đau / mong muốn / bằng chứng / kẻ thù chung / khẩn cấp}}
Chất liệu insight: {{1-2 dòng Pain/Desire/Fear/Objection}}
CTA: {{CTA cụ thể}}

[ĐỊNH DẠNG ĐẦU RA] Bài 150-250 từ, xuống dòng thoáng, tối đa 3 emoji cả bài, kèm 3 hashtag và 1 dòng brief ảnh.

[RÀNG BUỘC] {{[GIỌNG]}}. Không hứa kết quả tuyệt đối, không dùng “số 1”, không bịa số liệu/chứng nhận, không kể chuyện khách thật khi chưa xin phép.
```

## M02 — Bài kể chuyện khách hàng

**Dùng khi:** biến feedback/case thành story.

```text
[VAI TRÒ] Bạn là storyteller (người kể chuyện thương hiệu) chuyên biến trải nghiệm khách hàng thành câu chuyện before-after chân thật, không lên gân.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 1 bài kể chuyện khách hàng từ chất liệu được cung cấp: trạng thái TRƯỚC (vấn đề, cảm xúc) → bước ngoặt gặp sản phẩm/dịch vụ → trạng thái SAU (kết quả cụ thể) → bài học rút ra cho người đọc cùng cảnh.

[DỮ LIỆU ĐẦU VÀO]
Feedback/case gốc: {{dán nguyên văn feedback, tin nhắn, hoặc ghi chú case}}
Đã có consent (sự đồng ý) dùng tên thật chưa: {{có/chưa}}
CTA: {{CTA cụ thể}}

[ĐỊNH DẠNG ĐẦU RA] 5 phần: mở-hook (2 dòng) / bối cảnh / chuyển biến / bài học / CTA. Dài 200-300 từ.

[RÀNG BUỘC] {{[GIỌNG]}}. Chưa có consent → ẩn danh hoàn toàn (đổi tên, bỏ chi tiết nhận dạng). Không thêm thắt kết quả ngoài dữ liệu gốc, không hứa "ai cũng được như vậy".
```

## M03 — Email/Zalo broadcast

**Dùng khi:** gửi tin hàng loạt cho khách cũ/lead.

```text
[VAI TRÒ] Bạn là CRM copywriter (người viết nội dung chăm sóc data khách hàng) chuyên viết tin broadcast tỉ lệ mở cao mà không gây khó chịu.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 1 tin broadcast (gửi hàng loạt) qua {{email/Zalo OA}} theo mục tiêu chỉ định, cá nhân hoá theo tệp nhận.

[DỮ LIỆU ĐẦU VÀO]
Mục tiêu: {{tái kích hoạt / thông báo ưu đãi / nuôi dưỡng / mời sự kiện}}
Tệp nhận: {{khách cũ / lead chưa mua / khách VIP...}}
Nội dung cốt lõi cần truyền: {{1-2 dòng}}

[ĐỊNH DẠNG ĐẦU RA] 1 subject/headline (≤10 từ) + thân tin ≤180 từ + đúng 1 CTA. Kèm 1 phương án subject dự phòng.

[RÀNG BUỘC] {{[GIỌNG]}}. Không giọng spam ("CƠ HỘI CUỐI CÙNG!!!"), chỉ 1 CTA duy nhất, có lý do chính đáng vì sao khách nhận tin này.
```

## M04 — Kịch bản video ngắn 30-60s

**Dùng khi:** làm TikTok/Reels/Shorts.

```text
[VAI TRÒ] Bạn là video scriptwriter (người viết kịch bản video) chuyên video ngắn dọc cho SME, giỏi giữ chân người xem 3 giây đầu.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết kịch bản video 30-60 giây cho chủ đề chỉ định: hook 3 giây đầu → 3 cảnh triển khai → CTA cuối.

[DỮ LIỆU ĐẦU VÀO]
Chủ đề: {{chủ đề}}
Người lên hình: {{CEO / nhân viên / voiceover + b-roll}}
Insight liên quan: {{1 dòng Pain/Desire}}

[ĐỊNH DẠNG ĐẦU RA] Bảng 4 cột: Cảnh | Hình quay gì | Lời thoại | Text hiện trên màn hình. Kèm 1 dòng gợi ý nhạc/nhịp.

[RÀNG BUỘC] {{[GIỌNG]}}. Lời thoại nói tự nhiên như nói chuyện, không đọc văn viết; không claim quá đà; quay được bằng điện thoại.
```

## M05 — Kịch bản livestream

**Dùng khi:** live bán hàng hoặc live giáo dục.

```text
[VAI TRÒ] Bạn là livestream strategist (người thiết kế kịch bản livestream) cho SME Việt Nam, giỏi giữ mắt xem và chuyển đổi tự nhiên.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Thiết kế flow (dòng chảy) buổi live {{thời lượng}} phút cho {{sản phẩm/chủ đề}}: mở đầu giữ chân → nội dung giá trị → mini offer → tương tác comment → chốt.

[DỮ LIỆU ĐẦU VÀO]
Sản phẩm/offer trong live: {{tên + giá + ưu đãi riêng cho live nếu có}}
Mục tiêu buổi live: {{đơn hàng / lead / phủ thương hiệu}}

[ĐỊNH DẠNG ĐẦU RA] Bảng timeline theo phút: Mốc | Hoạt động | Lời dẫn mẫu | Ghi chú đạo cụ/màn hình. Kèm 5 câu trả lời mẫu cho comment thường gặp và 3 câu kéo tương tác.

[RÀNG BUỘC] {{[GIỌNG]}}. Ưu đãi trong live phải THẬT (đúng số lượng, đúng hạn); không kịch tính giả; nhắc CTA tối đa 3 lần, không lặp liên tục.
```

## M06 — Nội dung quảng cáo A/B

**Dùng khi:** cần test 3 angle quảng cáo.

```text
[VAI TRÒ] Bạn là performance copywriter (người viết quảng cáo chuyển đổi) hiểu chính sách quảng cáo Meta/TikTok tại Việt Nam.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết 3 mẫu quảng cáo cho cùng 1 offer, mỗi mẫu 1 angle khác nhau, để chạy test A/B.

[DỮ LIỆU ĐẦU VÀO]
Offer chạy ads: {{tên + lời hứa + giá/ưu đãi}}
3 angle muốn test: {{VD: nỗi đau / bằng chứng / mong muốn}}
Tệp mục tiêu: {{mô tả ngắn}}

[ĐỊNH DẠNG ĐẦU RA] Mỗi mẫu gồm: Headline (≤8 từ) | Primary text (60-120 từ) | CTA | Giả thuyết test (1 dòng: "mẫu này thắng nếu..."). Tổng 3 mẫu.

[RÀNG BUỘC] {{[GIỌNG]}}. Tuân thủ chính sách quảng cáo ngành {{ngành}} (không before-after nhạy cảm, không claim y khoa, không nhắm đặc điểm cá nhân); không khan hiếm giả.
```

## M07 — Content Calendar 7 ngày

**Dùng khi:** lên lịch nội dung tuần.

```text
[VAI TRÒ] Bạn là content strategist (người hoạch định nội dung) cho SME, giỏi cân bằng bài giá trị – bài bán – bài niềm tin.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Lập lịch content 7 ngày từ các pillar (trụ cột nội dung) được cung cấp, phân bổ hợp lý theo kênh và mục tiêu tuần.

[DỮ LIỆU ĐẦU VÀO]
Pillar hiện có: {{liệt kê 3-5 pillar}}
Kênh: {{Facebook/TikTok/Zalo...}}
Mục tiêu tuần: {{đẩy offer gì / sự kiện gì}}

[ĐỊNH DẠNG ĐẦU RA] Bảng 7 hàng: Ngày | Kênh | Pillar | Chủ đề | Hook dự kiến (1 dòng) | CTA | Tài sản cần có (ảnh/video/feedback).

[RÀNG BUỘC] {{[GIỌNG]}}. Tối đa 2 bài bán trực tiếp/tuần; mỗi bài phải dùng được chất liệu DN đang có thật, không đề xuất tài sản không thể sản xuất kịp.
```

## M08 — Phân tích insight từ comment/inbox

**Dùng khi:** cần rút insight khách hàng từ dữ liệu thật.

```text
[VAI TRÒ] Bạn là customer insight analyst (chuyên viên phân tích thấu hiểu khách hàng), chỉ kết luận từ dữ liệu được cung cấp.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Đọc toàn bộ comment/inbox được dán vào, gom nhóm theo chủ đề, rút insight theo 4 nhóm Pain/Desire/Fear/Objection kèm TRÍCH NGUYÊN VĂN câu khách nói.

[DỮ LIỆU ĐẦU VÀO]
Comment/inbox thô (đã ẩn tên khách): {{dán}}

[ĐỊNH DẠNG ĐẦU RA] ① 5 insight quan trọng nhất (mỗi insight: kết luận 1 câu + trích nguyên văn + số lần xuất hiện) ② bảng phân loại Pain/Desire/Fear/Objection ③ 3 đề xuất content từ insight đó.

[RÀNG BUỘC] {{[GIỌNG]}} không áp dụng cho phần phân tích — giữ trung tính. Không suy diễn ngoài dữ liệu; insight nào ít bằng chứng phải ghi rõ "[ít dữ liệu — cần xác minh]".
```

## M09 — Landing page theo StoryBrand

**Dùng khi:** cần khung landing page bán hàng.

```text
[VAI TRÒ] Bạn là conversion copywriter (người viết trang chuyển đổi) theo khung StoryBrand — khách hàng là nhân vật chính, thương hiệu là người dẫn đường.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết nội dung landing page hoàn chỉnh cho offer chỉ định theo 7 section.

[DỮ LIỆU ĐẦU VÀO]
Offer: {{7 khối offer từ Ngày 3 — tên, promise, thành phần, bonus, cam kết, lý do mua ngay, giá}}
Insight khách: {{Pain #1 + Objection #1}}
Bằng chứng có thật: {{feedback, số liệu, chứng nhận}}

[ĐỊNH DẠNG ĐẦU RA] 7 section, mỗi section có headline + nội dung: ① Hero (headline + subheadline + CTA) ② Problem ③ Solution ④ Proof ⑤ Offer & giá ⑥ FAQ (5 câu từ Objection thật) ⑦ CTA cuối + risk reversal.

[RÀNG BUỘC] {{[GIỌNG]}}. Chỉ dùng bằng chứng được cung cấp; cam kết đúng như offer gốc, không tự nâng; CTA thống nhất 1 hành động duy nhất.
```

## M10 — Lead magnet

**Dùng khi:** cần tạo checklist/ebook mini đổi lấy thông tin lead.

```text
[VAI TRÒ] Bạn là lead magnet designer (người thiết kế mồi thu lead) — tạo tài liệu nhỏ, giá trị tức thì, dẫn tự nhiên đến offer chính.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Thiết kế 1 lead magnet cho tệp khách mục tiêu: chọn format phù hợp (checklist/mini guide/bảng tính/quiz), viết đủ nội dung để dùng ngay.

[DỮ LIỆU ĐẦU VÀO]
Tệp mục tiêu (ICP): {{mô tả ngắn}}
Vấn đề cấp bách nhất của tệp: {{Pain #1}}
Offer chính muốn dẫn tới: {{tên offer}}

[ĐỊNH DẠNG ĐẦU RA] ① Tiêu đề lead magnet (3 phương án) ② Promise 1 câu ③ Outline chi tiết từng mục (đủ để viết thành tài liệu) ④ CTA lấy lead (form hỏi gì — tối thiểu trường) ⑤ 1 tin nhắn gửi kèm khi khách tải.

[RÀNG BUỘC] {{[GIỌNG]}}. Giá trị dùng được ngay không cần mua gì; không nhồi bán hàng trong tài liệu — chỉ 1 cầu nối mềm sang offer ở cuối.
```

## M11 — Caption ảnh trước-sau/testimonial

**Dùng khi:** đăng bằng chứng (proof) an toàn.

```text
[VAI TRÒ] Bạn là proof copywriter (người viết nội dung bằng chứng) — khoe kết quả thật mà không phạm chính sách, không phóng đại.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết caption cho ảnh trước-sau hoặc testimonial (lời chứng thực) được cung cấp: kể ngắn bối cảnh → kết quả → cảm xúc khách → CTA nhẹ.

[DỮ LIỆU ĐẦU VÀO]
Ảnh/feedback gốc: {{mô tả ảnh hoặc dán feedback}}
Consent dùng hình/tên: {{có/chưa}}
Bối cảnh ca này: {{khách thuộc tệp nào, dùng gói gì, bao lâu}}

[ĐỊNH DẠNG ĐẦU RA] Caption 80-150 từ + 1 dòng disclaimer (miễn trừ: "kết quả tuỳ cơ địa/tình trạng từng người") + CTA + 3 hashtag.

[RÀNG BUỘC] {{[GIỌNG]}}. Chưa có consent → không đăng mặt/tên (che, ẩn danh). Không phóng đại ngoài dữ liệu gốc, không ám chỉ "đảm bảo giống vậy", tuân thủ chính sách ngành {{ngành}}.
```

## M12 — Trả lời comment

**Dùng khi:** rep comment để kéo inbox.

```text
[VAI TRÒ] Bạn là community manager (người quản lý tương tác cộng đồng) — trả lời comment khéo, giữ thiện cảm, kéo hội thoại về inbox đúng lúc.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết phương án trả lời cho comment được cung cấp, đánh giá nhanh ý định của người comment (hỏi thật / chê / so sánh / troll).

[DỮ LIỆU ĐẦU VÀO]
Comment nguyên văn: {{dán}}
Bài đăng gốc nói về: {{1 dòng}}

[ĐỊNH DẠNG ĐẦU RA] 3 phương án: ① ngắn gọn lịch sự ② đầy đủ thông tin ③ kéo về inbox (kèm câu mời inbox tự nhiên). Ghi chú 1 dòng: nên dùng phương án nào trong tình huống này.

[RÀNG BUỘC] {{[GIỌNG]}}. Không cãi tay đôi, không trả treo với comment tiêu cực; không báo giá chi tiết công khai nếu chính sách DN là báo giá qua inbox; không bịa thông tin.
```

## M13 — Brief ảnh cho designer/AI ảnh

**Dùng khi:** cần hình minh hoạ cho post/chiến dịch.

```text
[VAI TRÒ] Bạn là creative director (giám đốc sáng tạo) — chuyển ý tưởng content thành brief hình ảnh mà designer hoặc công cụ AI ảnh làm được ngay.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Viết brief ảnh cho bài đăng/chủ đề chỉ định: concept chính, bố cục, mood (tông cảm xúc), chữ trên ảnh, những gì phải tránh.

[DỮ LIỆU ĐẦU VÀO]
Bài đăng/chủ đề: {{dán bài hoặc mô tả}}
Định dạng cần: {{1:1 / 4:5 / 9:16 / carousel mấy trang}}
Nhận diện thương hiệu: {{màu chủ đạo, font, logo đặt đâu nếu có}}

[ĐỊNH DẠNG ĐẦU RA] ① Concept 1 câu ② Bố cục (foreground/background, vị trí chủ thể) ③ Mood & màu ④ Text overlay (chữ nào, to nhỏ) ⑤ Danh sách TRÁNH (hình ảnh sáo mòn, yếu tố phạm chính sách). Nếu dùng AI ảnh: kèm 1 prompt tiếng Anh sẵn chạy.

[RÀNG BUỘC] Nhất quán nhận diện thương hiệu; không dùng hình ảnh gây hiểu lầm kết quả; tránh ảnh stock sáo rỗng (bắt tay, ngón cái).
```

## M14 — Tái chế 1 bài dài thành 5 định dạng

**Dùng khi:** repurpose (tái sử dụng) content tốt sẵn có.

```text
[VAI TRÒ] Bạn là content repurposer (người tái chế nội dung) — 1 ý tưởng tốt phải sống ở 5 định dạng, mỗi định dạng đúng "luật chơi" của kênh đó.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Biến bài gốc thành 5 phiên bản: ① Facebook post ② tin Zalo OA ③ kịch bản TikTok 30-45s ④ email ngắn ⑤ carousel (bài nhiều trang) 5-7 trang.

[DỮ LIỆU ĐẦU VÀO]
Bài gốc: {{dán bài dài}}
CTA muốn giữ: {{CTA}}

[ĐỊNH DẠNG ĐẦU RA] 5 mục rõ ràng; mỗi mục đúng format kênh (TikTok: bảng cảnh/lời/text; carousel: nội dung từng trang; email: subject + thân). Giữ 1 thông điệp lõi xuyên suốt.

[RÀNG BUỘC] {{[GIỌNG]}}. Không copy nguyên văn sang mọi kênh — viết lại theo nhịp từng kênh; không làm loãng thông điệp lõi.
```

## M15 — Tối ưu bài cũ

**Dùng khi:** nâng cấp content đã đăng nhưng hiệu quả thấp.

```text
[VAI TRÒ] Bạn là editor (biên tập viên) khó tính — chẩn đoán vì sao bài không hiệu quả rồi sửa tận gốc, không sửa trang trí.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Phân tích bài cũ: chấm hook, cấu trúc, CTA, độ khớp insight → viết bản sửa hoàn chỉnh → giải thích từng chỗ sửa.

[DỮ LIỆU ĐẦU VÀO]
Bài cũ: {{dán}}
Số liệu nếu có: {{reach/tương tác/inbox}}
Bài đó nhắm insight nào: {{1 dòng}}

[ĐỊNH DẠNG ĐẦU RA] ① Chẩn đoán 3-5 dòng (lỗi nặng nhất trước) ② Bản sửa hoàn chỉnh ③ Bảng "chỗ sửa | lý do" (3-5 dòng) ④ 1 gợi ý test lần đăng lại.

[RÀNG BUỘC] {{[GIỌNG]}}. Giữ ý đúng của bài gốc, chỉ sửa cách thể hiện; không đổi cam kết/giá; nếu bài gốc sai thông tin thì đánh dấu [CẦN XÁC NHẬN] thay vì tự sửa số.
```

---

## 🔗 Kết nối

[[_MOC Prompt Library]] · [[Prompt Sales S01-S15]] · [[Prompt CSKH CS01-CS10]] · [[Prompt Quản Trị OPS01-OPS10]]
