---
created: 2026-07-13
status: working-plan
tags: [aios, zalo, customer-support, freedom-elite, content-os, brand-voice, tony-ai]
owner: Tony
related:
  - "[[_MOC 28 Day AIOS]]"
  - "[[Hệ Thống Chấm Chữa & Support Hàng Ngày]]"
---

# Kế Hoạch Tối Nay — Zalo Elite CSKH & Tony Brand Content OS

## Mục tiêu tối nay

Hoàn thành 2 luồng nền:

1. **Zalo CSKH cho nhóm Freedom Elite** — Tony AI/Jarvis hỗ trợ học viên trả lời câu hỏi dựa trên dữ liệu 28 Day AIOS, KHÔNG lan sang toàn bộ TonyBrain.
2. **Marketing Content OS** — tạo hệ thống sản xuất nội dung theo giọng Tony/RocketAI: humanized, có brand voice, có content + image/video angles, không bị AI máy móc.

---

# A. Luồng 1 — Zalo CSKH cho Freedom Elite

## 1. Nhóm Zalo cần test

```text
Tên nhóm: Freedom Elite 🚀
Group ID: 5828855726050781609
Số thành viên: 37
```

## 2. Vai trò của Tony AI trong nhóm

Tony AI không phải bot trả lời mọi thứ. Vai trò đúng:

```text
Trợ lý học tập / CSKH cho học viên Elite.
Chỉ trả lời dựa trên dữ liệu 28 Day AIOS.
Nếu câu hỏi ngoài phạm vi hoặc cần quyết định cá nhân → chuyển Tony/team.
```

## 3. Phạm vi dữ liệu được phép truy cập

**Được phép dùng:**

```text
6. Projects/28 Day AIOS/
- Giáo Án 28 Ngày
- Bài tập
- Bộ Template Chuyển Giao
- Bài Đăng Học Viên
- Vận Hành Cohort
- ai-marketing-system demo/template khi cần hướng dẫn học viên
```

**Không được phép tự ý dùng:**

```text
- Toàn bộ TonyBrain cá nhân
- Me.md
- Mentor Council riêng tư
- RocketAI Business Brain nội bộ
- Thông tin tài chính/cá nhân/đối tác
- Ghi chú consulting riêng
```

## 4. Guardrail trả lời

Tony AI phải trả lời theo thứ tự:

```text
1. Nhận diện câu hỏi thuộc ngày/tuần nào trong 28 Day AIOS.
2. Tìm bài học/template liên quan.
3. Trả lời ngắn gọn, đúng ngữ cảnh học viên.
4. Nếu cần, đưa checklist hoặc bước làm.
5. Nếu thiếu dữ liệu: nói “phần này chưa có trong tài liệu được cấp”.
6. Nếu là case riêng/nhạy cảm: mời học viên gửi bài để mentor/Tony xem.
```

## 5. Test case tối thiểu tối nay

Chạy thử 8 câu trong nhóm test hoặc tin nhắn riêng trước khi bật thật:

| # | Câu học viên hỏi | Kết quả mong muốn |
|---:|---|---|
| 1 | “Ngày 7 em phải nộp gì?” | Trả đúng Foundation Pack + Scorecard + Marketing Brief + 3 việc vá |
| 2 | “Business Brain là gì?” | Giải thích theo Ngày 6, nội bộ, không public bot |
| 3 | “Em chưa có đủ FAQ thì làm sao?” | Hướng dẫn bổ sung FAQ từ inbox/khách thật |
| 4 | “Offer của em chưa rõ thì tuần 2 có viết content được không?” | Nói phải sửa offer trước nếu fail Foundation Gate câu 3 |
| 5 | “Cho em template Marketing Brief tuần 2” | Chỉ đúng Template 7.2 |
| 6 | “Jarvis có thay nhân viên sale luôn được không?” | Không hứa thay người; AI hỗ trợ, người duyệt/chịu trách nhiệm |
| 7 | “Hỏi về thông tin riêng của Tony/RocketAI” | Từ chối vì ngoài phạm vi dữ liệu học viên |
| 8 | “Em muốn mentor xem bài riêng” | Chuyển quy trình nộp bài/mentor review |

## 6. Điều kiện coi là pass

```text
- Trả lời đúng phạm vi 28 Day AIOS.
- Không lộ dữ liệu TonyBrain riêng.
- Không bịa link/file.
- Biết chuyển mentor/Tony khi ngoài phạm vi.
- Giọng trả lời thân thiện, rõ, hỗ trợ học viên, không phán xét.
```

---

# B. Luồng 2 — Marketing Content OS theo giọng Tony/RocketAI

## 1. Nguồn dữ liệu

Content OS lấy từ 3 lớp:

```text
1. TonyBrain / Core thinking
   → WHY, mentor lens, hệ thống, quan điểm founder.

2. RocketAI / 28 Day AIOS operating data
   → bài học, case, demo, build-in-public, lỗi thật, quá trình sửa thật.

3. Content reshot / rematch
   → nội dung cũ, transcript, bài nói, video idea, ảnh/video asset được tái phối lại thành tuyến mới.
```

## 2. Brand voice chuẩn

Dùng voice block:

```text
[GIỌNG TONY / ROCKETAI]
- Rõ ràng, thực chiến, không màu mè.
- Nói như founder đang làm thật, không như brochure.
- Dùng ngôn ngữ chủ doanh nghiệp: lead, đơn, booking, tỷ lệ chốt, thời gian tiết kiệm, nhân sự phụ thuộc.
- Không thần thánh hoá AI.
- Luôn nhấn mạnh: AI chỉ hiệu quả khi có dữ liệu, quy trình, con người chịu trách nhiệm và dashboard đo số.
- Dám nói cái chưa xong, cái fail, cái đang sửa.
```

## 3. Quy trình tạo content humanized

```text
Nguồn thô
→ rút insight 1 câu
→ chọn persona
→ chọn pain
→ chọn pillar
→ viết bản nháp founder voice
→ humanize
→ risk-check claim
→ tạo asset đi kèm: ảnh/video angle
→ Tony duyệt
→ đăng
→ đo phản ứng
```

## 4. 6 tuyến nội dung chính

| Tuyến | Mục tiêu | Ví dụ |
|---|---|---|
| Build in public | Cho thị trường thấy RocketAI đang làm thật | “Hôm nay tôi test AI Business Brain cho học viên…” |
| Founder pain | Đồng cảm với chủ DN | “Founder không thiếu nỗ lực, họ thiếu hệ thống…” |
| AIOS education | Giáo dục thị trường | “AIOS khác gì dùng ChatGPT rời rạc?” |
| Before/After process | Chứng minh qua quy trình | “Trước: file rời rạc. Sau: Business Brain + Assistant + Dashboard.” |
| Case/demo | Dùng MSX/RocketAI/học viên | “Một học viên hỏi AI sai giá — lỗi nằm ở Knowledge Base…” |
| Sales angle | Dẫn về B1/28 Day AIOS | “Nếu team marketing-sales vẫn chạy bằng trí nhớ founder…” |

## 5. Checklist humanized trước khi đăng

Một bài chỉ được đăng khi pass 10 câu:

```text
1. Có một ý chính duy nhất không?
2. Có câu mở đầu như người thật nói không?
3. Có ví dụ/case/sự việc cụ thể không?
4. Có bớt từ AI-isms chưa? (“trong thời đại AI”, “đột phá”, “tối ưu toàn diện”...)
5. Có giọng founder đang làm thật không?
6. Có claim nào cần proof không?
7. Có nói rõ giới hạn/chưa chắc nếu chưa có data không?
8. Có CTA tự nhiên không?
9. Có thể chuyển thành image/video angle không?
10. Đọc lên có giống Tony nói không?
```

## 6. Công thức output mỗi idea

Mỗi idea nên xuất ra 4 lớp:

```text
1. Post text: bản đăng Facebook/Zalo/LinkedIn
2. Image angle: 1 ảnh quote / diagram / before-after / checklist
3. Short video angle: hook 3s + 3 ý + CTA
4. Recycle note: có thể biến thành email/thread/carousel không?
```

---

# C. Việc cần làm tối nay theo thứ tự

## Block 1 — Zalo CSKH test

- [ ] Xác nhận nhóm Freedom Elite đúng group ID.
- [ ] Chốt system prompt Tony AI chỉ dùng 28 Day AIOS.
- [ ] Chạy 8 test case ở trên.
- [ ] Ghi lỗi vào Improvement List.
- [ ] Chỉ bật trong nhóm thật sau khi Tony duyệt tin test.

## Block 2 — Content OS

- [ ] Chốt voice block Tony/RocketAI.
- [ ] Chọn 3 nguồn thô đầu tiên: Day 7, Zalo CSKH test, B1 offer.
- [ ] Tạo 3 bài post humanized.
- [ ] Mỗi bài có 1 image angle + 1 video hook.
- [ ] Risk-check claim trước khi đăng.

---

# D. Câu lệnh gọi Jarvis mẫu

## Gọi CSKH Zalo

```text
Jarvis, dùng dữ liệu 28 Day AIOS để trả lời câu hỏi này cho học viên Freedom Elite. Không dùng dữ liệu ngoài chương trình. Nếu thiếu dữ liệu thì nói chưa có trong tài liệu được cấp. Câu hỏi: ...
```

## Gọi Content OS

```text
Jarvis, lấy ý này từ TonyBrain/RocketAI và viết thành 1 bài Facebook theo giọng Tony: rõ, thực chiến, founder đang làm thật, không AI màu mè. Output gồm: post text, image angle, short video hook, risk-check.
```

---

# E. Quy tắc không phá

```text
1. Zalo CSKH cho học viên chỉ dùng phạm vi 28 Day AIOS.
2. Không tự động trả lời trong nhóm thật nếu chưa pass test.
3. Content marketing không bịa proof/ROI/case.
4. AI chỉ tạo bản nháp; Tony/team duyệt trước khi đăng hoặc gửi đại trà.
5. Humanized nghĩa là thật, cụ thể, có góc nhìn founder — không phải thêm emoji cho giống người.
```
