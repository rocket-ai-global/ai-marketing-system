---
created: 2026-07-12
tags: [project, aios, template, day5, prompt-library]
up:
  - "[[Danh Mục Template Chuyển Giao]]"
---

# Template 5.1 — Prompt Library 50 Prompt Khung

> Dùng cho **Ngày 05 — Hệ Thống Prompt & Template Chuẩn**. Học viên KHÔNG viết prompt từ số 0. Học viên copy file này, điền 2 khối `[BỐI CẢNH DN]` + `[GIỌNG]`, chọn 20 prompt ưu tiên, cá nhân hoá và test 10 prompt.

## 0. Cách dùng trong 5 bước

1. Copy file này thành: `[Tên DN] — Ngày 05 — Prompt Library v1`.
2. Điền `Template 5.2 — Khối Ngữ Cảnh Chuẩn` ở đầu file: `[BỐI CẢNH DN]` + `[GIỌNG]`.
3. Chọn 20 prompt ưu tiên trong bảng 50 prompt dưới đây.
4. Với mỗi prompt đã chọn: dán 2 khối ngữ cảnh vào chỗ `{{[BỐI CẢNH DN]}}`, `{{[GIỌNG]}}`, rồi điền các chỗ `{{...}}` còn lại bằng dữ liệu thật.
5. Test ít nhất 10 prompt, ghi trạng thái vào bảng nghiệm thu cuối file.

---

## 1. Hai khối phải điền trước khi dùng prompt

### [BỐI CẢNH DN]

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

### [GIỌNG]

```text
[GIỌNG]
Xưng hô: {{em/anh/chị/mình...}}.
Tính cách giọng: {{ấm áp/thẳng thắn/chuyên gia/gần gũi...}}.
Từ/cụm từ nên dùng: {{5 cụm từ đặc trưng}}.
Điều cấm: {{từ sáo rỗng, emoji quá nhiều, cam kết quá đà, chê bai đối thủ...}}.
```

---

## 2. Cấu trúc prompt chuẩn 6 phần

```text
[VAI TRÒ] Bạn là {{vai trò chuyên gia}}.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] {{mô tả việc cần AI làm, từng bước rõ ràng}}.

[DỮ LIỆU ĐẦU VÀO] {{dữ liệu học viên cần dán mỗi lần chạy}}.

[ĐỊNH DẠNG ĐẦU RA] {{bảng/script/post/checklist, độ dài, số lượng, cấu trúc}}.

[RÀNG BUỘC] {{[GIỌNG]}}. {{điều cấm/an toàn/pháp lý/chất lượng}}.
```

---

## 3. Bảng 50 prompt khung

> Cột “Prompt đầy đủ” dùng dạng rút gọn để học viên dễ quản lý trong 1 file. Khi cần prompt dài, copy mã prompt và mở phần **4. Prompt đầy đủ mẫu** bên dưới để xem cách triển khai.

| Mã    | Nhóm      | Tên prompt                          | Dùng khi nào                          | Prompt đầy đủ khung rút gọn                                                                                                                                                                                                                                             | Test      |
| ----- | --------- | ----------------------------------- | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| M01   | Marketing | Viết bài Facebook theo angle        | Cần 1 bài social bán mềm/giáo dục     | Role: copywriter social. Context: `{{[BỐI CẢNH DN]}}`. Task: viết bài theo `{{chủ đề}}`, angle `{{nỗi đau/mong muốn/bằng chứng/kẻ thù chung}}`. Input: `{{insight/avatar/offer}}`. Output: 150-250 từ + CTA + 3 hashtag. Constraint: `{{[GIỌNG]}}`, không claim quá đà. | Chưa test |
| M02   | Marketing | Bài kể chuyện khách hàng            | Biến feedback/case thành story        | Role: storyteller. Task: viết câu chuyện before-after từ `{{feedback/case}}`. Output: mở-hook, bối cảnh, chuyển biến, bài học, CTA. Constraint: ẩn danh nếu chưa có consent.                                                                                            | Chưa test |
| M03   | Marketing | Email/Zalo broadcast                | Gửi khách cũ/lead                     | Role: CRM copywriter. Task: viết broadcast theo mục tiêu `{{mục tiêu}}`. Output: subject/headline + tin nhắn ≤180 từ + CTA. Constraint: không spam, 1 CTA.                                                                                                              | Chưa test |
| M04   | Marketing | Kịch bản video ngắn 30-60s          | Làm TikTok/Reels/Shorts               | Role: video scriptwriter. Task: viết script hook 3s + 3 cảnh + CTA cho `{{chủ đề}}`. Output: bảng cảnh/hình/lời/text. Constraint: nói tự nhiên.                                                                                                                         | Chưa test |
| M05   | Marketing | Kịch bản livestream                 | Bán/giáo dục live                     | Role: livestream strategist. Task: tạo flow live `{{thời lượng}}` cho `{{sản phẩm}}`. Output: mở đầu, nội dung, mini offer, xử lý comment, chốt.                                                                                                                        | Chưa test |
| M06   | Marketing | Nội dung quảng cáo A/B              | Test 3 angle quảng cáo                | Role: performance copywriter. Task: viết 3 ads khác angle. Output: headline, primary text, CTA, giả thuyết test. Constraint: tuân thủ chính sách ngành.                                                                                                                 | Chưa test |
| M07   | Marketing | Content Calendar 7 ngày             | Lên lịch nội dung tuần                | Role: content strategist. Task: tạo lịch 7 ngày từ `{{pillar}}`. Output: bảng ngày/kênh/chủ đề/hook/CTA/tài sản cần có.                                                                                                                                                 | Chưa test |
| M08   | Marketing | Phân tích insight từ comment/inbox  | Rút insight khách hàng                | Role: customer insight analyst. Task: gom nhóm `{{comment/inbox}}`. Output: 5 insight, pain/desire/fear/objection, đề xuất content.                                                                                                                                     | Chưa test |
| M09   | Marketing | Landing page theo StoryBrand        | Tạo khung landing bán hàng            | Role: conversion copywriter. Task: viết landing cho `{{offer}}`. Output: 7 section headline/problem/solution/proof/offer/FAQ/CTA.                                                                                                                                       | Chưa test |
| M10   | Marketing | Lead magnet                         | Tạo checklist/ebook mini              | Role: lead magnet designer. Task: tạo lead magnet cho `{{ICP}}`. Output: title, promise, outline, CTA lấy lead.                                                                                                                                                         | Chưa test |
| M11   | Marketing | Caption ảnh trước-sau/testimonial   | Đăng proof an toàn                    | Role: proof copywriter. Task: viết caption từ `{{ảnh/feedback}}`. Output: caption + disclaimer + CTA. Constraint: cần consent, không phóng đại.                                                                                                                         | Chưa test |
| M12   | Marketing | Trả lời comment                     | Rep comment để kéo inbox              | Role: community manager. Task: trả lời `{{comment}}`. Output: 3 phương án: ngắn/vừa/kéo inbox. Constraint: tự nhiên, không cãi.                                                                                                                                         | Chưa test |
| M13   | Marketing | Brief ảnh cho designer/AI ảnh       | Cần hình minh họa post                | Role: creative director. Task: tạo brief ảnh cho `{{post/chủ đề}}`. Output: concept, layout, mood, text overlay, tránh gì.                                                                                                                                              | Chưa test |
| M14   | Marketing | Tái chế 1 bài dài thành 5 định dạng | Repurpose content                     | Role: content repurposer. Task: biến `{{bài dài}}` thành FB post, Zalo, TikTok script, email, carousel.                                                                                                                                                                 | Chưa test |
| M15   | Marketing | Tối ưu bài cũ                       | Nâng cấp content đã đăng              | Role: editor. Task: phân tích `{{bài cũ}}`, sửa hook, CTA, cấu trúc. Output: bản sửa + lý do sửa.                                                                                                                                                                       | Chưa test |
| S01   | Sales     | Kịch bản tư vấn SPIN                | Sale call/inbox có cấu trúc           | Role: sales coach. Task: viết script SPIN cho `{{sản phẩm/lead}}`. Output: mở đầu, 10 câu hỏi, gợi ý offer, chốt.                                                                                                                                                       | Chưa test |
| S02   | Sales     | Mở đầu cuộc tư vấn                  | Tin nhắn đầu tiên                     | Role: tư vấn viên. Task: viết 3 tin mở đầu theo `{{nguồn lead}}`. Output: ngắn/gợi mở/chuyên gia.                                                                                                                                                                       | Chưa test |
| S03   | Sales     | Xử lý từ chối                       | Khách phản đối giá/thời gian/niềm tin | Role: objection coach. Task: chẩn đoán fear sau `{{objection}}`, viết 3 phản hồi. Output: nhẹ/bằng chứng/hành động nhỏ.                                                                                                                                                 | Chưa test |
| S04   | Sales     | Proposal/đề xuất                    | Sau discovery call                    | Role: solution consultant. Task: viết proposal cho `{{khách}}`. Output: vấn đề, giải pháp, gói, timeline, giá, bước tiếp.                                                                                                                                               | Chưa test |
| S05   | Sales     | Báo giá cá nhân hóa                 | Gửi bảng giá theo nhu cầu             | Role: sales proposal writer. Task: cá nhân hóa báo giá từ `{{gói}}`. Output: bảng gói + lý do phù hợp + CTA.                                                                                                                                                            | Chưa test |
| S06   | Sales     | Follow-up 3 chạm                    | Khách chưa phản hồi                   | Role: follow-up specialist. Task: viết tin sau 1/3/7 ngày. Output: 3 tin nhắn ngắn, không gây áp lực.                                                                                                                                                                   | Chưa test |
| S07   | Sales     | Phân loại lead nóng/ấm/lạnh         | Chấm điểm lead                        | Role: lead scoring analyst. Task: chấm lead từ `{{hội thoại}}`. Output: điểm 1-10, nhãn, lý do, bước tiếp.                                                                                                                                                              | Chưa test |
| S08   | Sales     | Tóm tắt lịch sử tư vấn              | Trước khi follow-up                   | Role: CRM assistant. Task: tóm tắt `{{ghi chú/hội thoại}}`. Output: nhu cầu, objection, đã hứa, next step.                                                                                                                                                              | Chưa test |
| S09   | Sales     | Kịch bản gọi hẹn lịch               | Gọi điện/Zalo voice                   | Role: appointment setter. Task: viết script hẹn `{{demo/soi da/tư vấn}}`. Output: mở đầu, lý do, 2 khung giờ, xử lý từ chối.                                                                                                                                            | Chưa test |
| S10   | Sales     | Tin nhắn cứu khách im lặng          | Lead ghost                            | Role: reactivation copywriter. Task: viết 3 tin cứu khách im lặng. Output: nhẹ/giá trị/câu hỏi đóng.                                                                                                                                                                    | Chưa test |
| S11   | Sales     | So sánh khéo với đối thủ            | Khách đang so sánh                    | Role: competitive sales advisor. Task: so sánh `{{mình}}` với `{{đối thủ}}`. Output: bảng khác biệt + câu trả lời khéo. Constraint: không nói xấu.                                                                                                                      | Chưa test |
| S12   | Sales     | Chốt kèm khan hiếm thật             | Có ưu đãi/số slot thật                | Role: ethical closer. Task: viết tin chốt theo `{{ưu đãi/slot/deadline thật}}`. Constraint: không tạo khan hiếm giả.                                                                                                                                                    | Chưa test |
| S13   | Sales     | Xin giới thiệu/referral             | Sau khi khách hài lòng                | Role: referral copywriter. Task: viết tin xin giới thiệu. Output: 3 mẫu ngắn, có lời cảm ơn.                                                                                                                                                                            | Chưa test |
| S14   | Sales     | Tái ký/gia hạn                      | Sắp hết gói/liệu trình                | Role: retention sales. Task: viết đề xuất gia hạn từ `{{kết quả hiện tại}}`. Output: recap, giá trị tiếp, CTA.                                                                                                                                                          | Chưa test |
| S15   | Sales     | Khảo sát nhu cầu nhanh              | Trước tư vấn                          | Role: discovery assistant. Task: tạo 7 câu hỏi khảo sát nhanh cho `{{sản phẩm}}`. Output: form câu hỏi + cách chấm.                                                                                                                                                     | Chưa test |
| CS01  | CSKH      | Trả lời FAQ theo KB                 | Chatbot/CSKH                          | Role: CSKH. Task: trả lời `{{câu hỏi}}` dựa trên `{{FAQ/KB}}`. Output: trả lời ngắn + CTA. Constraint: không bịa, chuyển người thật khi thiếu dữ liệu.                                                                                                                  | Chưa test |
| CS02  | CSKH      | Tin chăm sau lần dùng đầu           | Sau mua/sau buổi dịch vụ              | Role: customer success. Task: viết tin chăm sóc sau `{{lần dùng/buổi}}`. Output: ≤80 từ + hỏi tình trạng + nhắc lưu ý.                                                                                                                                                  | Chưa test |
| CS03  | CSKH      | Xử lý khiếu nại                     | Khách phàn nàn                        | Role: complaint handler. Task: phân loại mức độ, viết phản hồi đầu tiên. Output: xin lỗi, xác minh, hướng xử lý, SLA.                                                                                                                                                   | Chưa test |
| CS04  | CSKH      | Gọi lại khách bỏ ngang              | Khách ngừng dùng                      | Role: retention CS. Task: viết script gọi lại cho `{{lý do bỏ ngang}}`. Output: hỏi thăm, tìm nguyên nhân, offer hỗ trợ.                                                                                                                                                | Chưa test |
| CS05  | CSKH      | Nhắc lịch không gây phiền           | Nhắc hẹn/nhắc dùng                    | Role: reminder writer. Task: viết tin nhắc `{{sự kiện}}`. Output: 3 phiên bản: lịch sự/thân mật/rất ngắn.                                                                                                                                                               | Chưa test |
| CS06  | CSKH      | Chúc mừng mốc                       | Sinh nhật/mốc sử dụng                 | Role: relationship builder. Task: viết tin chúc mừng `{{mốc}}`. Output: tin nhắn cá nhân hóa + quà/CTA nếu có.                                                                                                                                                          | Chưa test |
| CS07  | CSKH      | Gợi ý upsell đúng lúc               | Khách đã có kết quả                   | Role: upsell advisor. Task: gợi ý nâng cấp từ `{{lịch sử mua}}`. Output: lý do phù hợp + 2 lựa chọn.                                                                                                                                                                    | Chưa test |
| CS08  | CSKH      | Gợi ý cross-sell                    | Bán chéo                              | Role: cross-sell advisor. Task: gợi ý sản phẩm bổ trợ từ `{{sản phẩm đã mua}}`. Output: 3 gợi ý + lý do.                                                                                                                                                                | Chưa test |
| CS09  | CSKH      | Xin review/feedback                 | Sau trải nghiệm tốt                   | Role: review request writer. Task: viết tin xin feedback/review. Output: 3 mẫu + câu hỏi gợi ý review.                                                                                                                                                                  | Chưa test |
| CS10  | CSKH      | Hâm nóng khách lâu không quay lại   | Re-activation                         | Role: winback copywriter. Task: viết chuỗi 3 tin cho khách `{{thời gian không quay lại}}`. Output: hỏi thăm/giá trị/ưu đãi.                                                                                                                                             | Chưa test |
| OPS01 | Quản trị  | Tóm tắt báo cáo tuần                | Chủ DN cần insight                    | Role: business analyst. Task: tóm tắt `{{số liệu tuần}}`. Output: KPI, insight, vấn đề, 3 hành động tuần tới.                                                                                                                                                           | Chưa test |
| OPS02 | Quản trị  | Phân tích số liệu marketing-sale    | Có data thô                           | Role: growth analyst. Task: phân tích `{{data}}`. Output: funnel, điểm nghẽn, giả thuyết, test đề xuất.                                                                                                                                                                 | Chưa test |
| OPS03 | Quản trị  | Kế hoạch tuần                       | Lập weekly plan                       | Role: COO assistant. Task: lập kế hoạch tuần từ `{{mục tiêu}}`. Output: ưu tiên, việc/người phụ trách/deadline/KPI.                                                                                                                                                     | Chưa test |
| OPS04 | Quản trị  | Đánh giá hiệu suất nhân viên        | Review KPI                            | Role: performance manager. Task: đánh giá `{{nhân sự + KPI}}`. Output: điểm mạnh/yếu/đề xuất coaching.                                                                                                                                                                  | Chưa test |
| OPS05 | Quản trị  | Viết SOP từ mô tả miệng             | Chuẩn hóa quy trình                   | Role: SOP writer. Task: biến `{{mô tả thô}}` thành SOP. Output: mục đích, input, bước, checklist, lỗi thường gặp.                                                                                                                                                       | Chưa test |
| OPS06 | Quản trị  | Đào tạo nhân viên mới               | Onboarding                            | Role: training designer. Task: tạo bài đào tạo cho `{{vai trò}}`. Output: mục tiêu, nội dung, bài tập, checklist.                                                                                                                                                       | Chưa test |
| OPS07 | Quản trị  | Biên bản & việc cần làm sau họp     | Sau meeting                           | Role: meeting secretary. Task: tóm tắt `{{transcript/notes}}`. Output: quyết định, action items, owner, deadline.                                                                                                                                                       | Chưa test |
| OPS08 | Quản trị  | Tin tuyển dụng                      | Cần tuyển người                       | Role: recruiter copywriter. Task: viết JD/tin tuyển cho `{{vị trí}}`. Output: mô tả, yêu cầu, quyền lợi, CTA.                                                                                                                                                           | Chưa test |
| OPS09 | Quản trị  | Checklist mở/đóng ca                | Vận hành hằng ngày                    | Role: operations designer. Task: tạo checklist cho `{{quy trình/ca}}`. Output: trước/trong/sau, người phụ trách, tiêu chuẩn đạt.                                                                                                                                        | Chưa test |
| OPS10 | Quản trị  | Phân tích quyết định nên/không nên  | Chủ DN phân vân                       | Role: decision analyst. Task: phân tích `{{quyết định}}`. Output: bối cảnh, options, pros/cons, rủi ro, đề xuất.                                                                                                                                                        | Chưa test |

---

## 4. Prompt đầy đủ mẫu

### M01 — Viết bài Facebook theo angle

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

### S03 — Xử lý từ chối

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

### CS01 — Trả lời FAQ theo Knowledge Base

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

### OPS01 — Tóm tắt báo cáo tuần

```text
[VAI TRÒ] Bạn là business analyst cho chủ SME, giỏi đọc số liệu marketing-sales-CSKH và chuyển thành hành động.

[BỐI CẢNH] {{[BỐI CẢNH DN]}}

[NHIỆM VỤ] Tóm tắt báo cáo tuần từ số liệu thô: tìm điểm tăng/giảm, điểm nghẽn, giả thuyết nguyên nhân và 3 hành động ưu tiên tuần tới.

[DỮ LIỆU ĐẦU VÀO]
Số liệu tuần: {{dán}}
Mục tiêu tháng: {{dán}}
Ghi chú vận hành: {{dán nếu có}}

[ĐỊNH DẠNG ĐẦU RA] Bảng KPI | nhận xét | hành động; sau bảng có “Top 3 ưu tiên tuần tới”.

[RÀNG BUỘC] {{[GIỌNG]}}. Không kết luận quá mức nếu số liệu thiếu. Đánh dấu [CẦN BỔ SUNG] cho dữ liệu thiếu.
```

---

## 5. Bảng nghiệm thu test prompt

| # | Mã prompt | Input đã dùng | Output dùng được ngay? | Cần sửa gì? | Trạng thái |
|---|---|---|:---:|---|---|
| 1 |  |  |  |  | Chưa test |
| 2 |  |  |  |  | Chưa test |
| 3 |  |  |  |  | Chưa test |
| 4 |  |  |  |  | Chưa test |
| 5 |  |  |  |  | Chưa test |
| 6 |  |  |  |  | Chưa test |
| 7 |  |  |  |  | Chưa test |
| 8 |  |  |  |  | Chưa test |
| 9 |  |  |  |  | Chưa test |
| 10 |  |  |  |  | Chưa test |

## 6. Tiêu chí đạt

- Có đủ 50 prompt khung trong file.
- Có 2 khối `[BỐI CẢNH DN]` và `[GIỌNG]` đã điền.
- Có ≥20 prompt đã cá nhân hóa.
- Có ≥10 prompt đã test, phủ ít nhất 3 nhóm.
- Prompt Chưa đạt phải có ghi chú “sửa gì” và chạy lại ít nhất 1 lần.
