---
up:
  - "[[Danh Mục Template Chuyển Giao]]"
created: 2026-07-12
tags: [project, aios, template]
---

# Template 5.2 — Khối Ngữ Cảnh Chuẩn

> Dùng cho **[[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]]**. Đây là "con dấu" của doanh nghiệp: 2 khối văn bản viết MỘT lần, dán vào MỌI prompt trong [[Template 5.1 — Prompt Library 50 Prompt Khung]]. 80% phần Context (bối cảnh) và Constraint (ràng buộc) của mọi prompt giống nhau — tách ra thành 2 khối này là lý do bạn cá nhân hoá được 20 prompt trong 45 phút.

## 1. Khung [BỐI CẢNH DN] — đúng 7 dòng, ≤130 từ

> Nguyên liệu: Business Snapshot (Ngày 01) + Customer Avatar (Ngày 02) + Core Offer (Ngày 03). Tạo nhanh bằng Prompt A trong [[Bài Tập Ngày 5 — Hệ Thống Prompt & Template]] (Prompt 1 của giáo án).

```text
[BỐI CẢNH DN]
{{Dòng 1 — DN là ai, ngành gì, ở đâu, quy mô (nhân sự/doanh thu nếu có)}}.
{{Dòng 2 — Khách mục tiêu: 1 dòng nén từ avatar (ai, tuổi, đặc điểm quyết định mua)}}.
{{Dòng 3 — Sản phẩm/offer chủ lực + GIÁ + cam kết chính (đo được)}}.
{{Dòng 4 — Kênh bán & marketing chính}}.
{{Dòng 5 — Nỗi sợ/rào cản lớn nhất của khách (từ PDFO Map)}}.
{{Dòng 6 — Điểm khác biệt (USP) quan trọng nhất}}.
{{Dòng 7 — Điều KHÔNG BAO GIỜ hứa/nói (claim cấm, pháp lý, giá chưa xác nhận)}}.
```

**Tự kiểm 10 giây:** người lạ đọc khối này có trả lời được ngay 3 câu **"bán gì – cho ai – khác gì"** không? Có **≥4 con số thật** (giá, quy mô, thời hạn) không? Không → viết lại, đừng dán vội.

## 2. Khung [GIỌNG] — đúng 4 dòng, ≤80 từ

> Nguyên liệu: đặc tả giọng thương hiệu (Bonus Ngày 04) hoặc Prompt B (rút nhanh từ 3-5 văn bản bạn tự viết).

```text
[GIỌNG]
Xưng hô: {{xưng gì, gọi khách là gì, gọi thương hiệu là gì}}.
Giọng: {{2-3 đặc điểm nổi bật — phải có bằng chứng từ văn bản thật, không phán "thân thiện, chuyên nghiệp" suông}}.
Từ/cụm từ nên dùng: {{5 cụm từ đặc trưng của bạn}}.
Điều cấm: {{từ sáo rỗng, kiểu câu, mức emoji, claim quá đà}}.
```

---

## 3. Bản điền mẫu 1 — 🚀 RocketAI (B2B dịch vụ — case dạy, khớp demo mục 4 giáo án)

```text
[BỐI CẢNH DN]
RocketAI Solutions — công ty dịch vụ B2B tại Việt Nam, 4 founder, chuyên chuyển giao hệ điều hành AI Marketing & Sale cho SME.
Khách mục tiêu: chủ spa/thẩm mỹ nữ 30-45 tuổi tự điều hành (đại diện: chị Mai, 35t, Spa ABC, 10 nhân viên, ~500tr/tháng).
Sản phẩm chủ lực: AI Marketing & Sale OS™ — OS Transfer 12tr / OS Installed 25tr / OS Managed 50tr+; cam kết bằng văn bản: sau 28 ngày hệ thống không chạy → hoàn học phí.
Kênh: video Facebook của founder, buổi demo Zoom, khách cũ giới thiệu.
Nỗi sợ lớn nhất của khách: "AI phức tạp quá, tôi không rành công nghệ" — sợ mua phải khoá học lý thuyết.
Điểm khác biệt: cài hệ thống chạy thật + mentor 1:10 + RocketAgent chạy 24/7, không dạy suông.
Không bao giờ hứa: con số doanh thu/lead cụ thể, "AI thay thế hoàn toàn con người".
```

```text
[GIỌNG]
Xưng hô: "Rocket" hoặc "em" với khách, gọi "anh/chị".
Giọng: thực chiến, thẳng thắn, minh bạch — chứng minh bằng số liệu và demo, không lên gân.
Từ/cụm từ nên dùng: hệ thống chạy thật, chuyển giao, hệ điều hành AI, cam kết bằng văn bản, 10x.
Điều cấm: "thần kỳ", hứa con số doanh thu, thuật ngữ kỹ thuật không giải thích, quá 1 emoji/đoạn.
```

## 4. Bản điền mẫu 2 — 🍵 MSX Group (B2C sản phẩm — học viên thật, bản nén đúng chuẩn ≤130/≤80 từ)

> Bản đầy đủ hơn (kèm 20 prompt cá nhân hoá + 10 dòng test) xem [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]].

```text
[BỐI CẢNH DN]
MSX Group (Mẫu Sơn Xanh) — doanh nghiệp dược liệu & trà thảo mộc vùng cao Mẫu Sơn, Lạng Sơn (vùng nguyên liệu 800–1.541m, bà con Dao · Tày · Nùng).
Khách mục tiêu: người 28–55 tuổi quan tâm sức khoẻ tự nhiên; người mua quà biếu; đại lý phân phối.
Sản phẩm chủ lực: Trà Hoa Sâm Nam 369.000đ, Trà Mẩy Gòm An Giấc 359.000đ, Viên Sâm Nam Hà Thủ Ô 599.000đ; combo mua 3 tặng 1 / mua 6 tặng 2.
Kênh: website mausonxanh.com, Zalo 0822.928.988, Facebook, TikTok, hội chợ OCOP, đại lý.
Nỗi sợ lớn nhất của khách: thảo mộc trôi nổi, công dụng bị thổi phồng, không rõ nguồn gốc.
Điểm khác biệt: nguồn gốc rõ ràng, câu chuyện bản địa, OCOP 3★, quy trình chế biến sạch.
Không bao giờ hứa: chữa bệnh, hiệu quả 100%; nhóm bệnh nền/mang thai/trẻ em cần hỏi bác sĩ.
```

```text
[GIỌNG]
Xưng hô: "em" với khách, gọi "anh/chị"; thương hiệu là "MSX"/"Mẫu Sơn Xanh".
Giọng: ấm áp, bản địa, tin cậy, an lành; có chuyên môn nhưng không lên gân.
Từ/cụm từ nên dùng: dược liệu vùng cao Mẫu Sơn, thảo mộc tự nhiên, nguồn gốc rõ ràng, đồng hành mỗi ngày.
Điều cấm: "thần dược", "chữa khỏi", "cam kết 100%"; không chê đối thủ; ≤3 emoji/bài.
```

---

## 5. Hướng dẫn "đóng dấu" 2 khối vào prompt

1. **Viết MỘT lần:** hoàn thiện 2 khối ở trên (chạy Prompt A/B rồi sửa tay) — đặt chúng ở đầu file Prompt Library.
2. **Nhân bản hàng loạt:** mọi prompt khung trong [[Template 5.1 — Prompt Library 50 Prompt Khung]] đều có chỗ trống `{{[BỐI CẢNH DN]}}` (ở phần [BỐI CẢNH]) và `{{[GIỌNG]}}` (ở phần [RÀNG BUỘC]). Copy khối → tìm chỗ trống tương ứng → dán đè. KHÔNG viết lại bối cảnh cho từng prompt.
3. **Điền nốt các `{{...}}` còn lại** bằng dữ liệu thật của lần chạy (chủ đề, objection, số liệu...).
4. **Cập nhật khi DN đổi:** giá/offer/kênh thay đổi → sửa khối 1 LẦN ở đầu file rồi dán lại — theo nhịp bảo trì thứ Sáu của SOP-05 (giáo án Ngày 05, mục 9), đồng bộ với Knowledge Base (SOP-04).
5. **Đường đi tiếp:** 2 khối này là lõi của Instruction Document Ngày 06 và system prompt chatbot Tuần 3 — đầu tư kỹ hôm nay, dùng lại cả chương trình.

## 6. Tiêu chí đạt

- `[BỐI CẢNH DN]` đúng 7 dòng, ≤130 từ, chứa ≥4 con số thật, khớp tài liệu Ngày 1-4.
- `[GIỌNG]` đúng 4 dòng, ≤80 từ, đặc điểm có bằng chứng từ văn bản thật.
- Đọc khối trả lời được "bán gì – cho ai – khác gì" trong 10 giây.
- Không nhồi nguyên Snapshot (khối dài cả trang = −5đ theo rubric).

> **Thích ứng ngành:** khung 7 dòng + 4 dòng dùng chung mọi ngành. Ngành sức khoẻ/làm đẹp/y tế: dòng 7 bắt buộc có claim y khoa cấm nói. Giáo dục: dòng 2 ghi rõ "người quyết định mua là phụ huynh". B2B: dòng 2 nêu cả người đại diện (chức danh) lẫn doanh nghiệp mục tiêu.

## 🔗 Kết nối

- [[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]] · [[Bài Tập Ngày 5 — Hệ Thống Prompt & Template]]
- [[Template 5.1 — Prompt Library 50 Prompt Khung]] · [[Template 5.1A — Bản Mẫu MSX Prompt Library v1]] · [[Template 5.3 — Prompt Usage Guide]]
