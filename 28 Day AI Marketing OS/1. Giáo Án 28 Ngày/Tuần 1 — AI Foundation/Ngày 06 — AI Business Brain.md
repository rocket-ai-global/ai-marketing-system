---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, giao-an]
week: 1
day: 6
core-output: "AI Business Brain v1 (KB Vault SME + Master Instruction, chạy theo Track A/B/C) · 2 Assistant (Sales + Marketing) · Test Case Report 6 ca chuẩn · Improvement List ≥5 mục"
---

# Ngày 06 — AI Business Brain

> 📦 **Chuyển giao — không phải khoá học:** module hôm nay đã được đóng gói sẵn (framework + template + agent trên RocketAgent/Hermes). Việc của học viên: **nạp dữ liệu doanh nghiệp mình → custom → test → nghiệm thu** để module chạy thật trên chính doanh nghiệp — không xây từ số 0, không lý thuyết suông.

> 🧠 **MỘT định nghĩa duy nhất (theo [[_Chuẩn Đồng Bộ Tuần 1]] mục 4):** **Business Brain = Knowledge Base trong Vault SME (não — AI biết gì) + Master Instruction (luật — AI hành xử thế nào), vận hành trên một lớp động cơ.** Não và luật là tài sản của BẠN, bất biến; lớp động cơ (RocketAgent / Projects / Hermes-Jarvis) chỉ là chỗ cắm não vào — đổi được sau này mà không mất gì.

> 🔀 **Bạn thuộc track nào? (chọn 1 — KHÔNG làm cả 3)**
> - **Track A — RocketAgent (mặc định):** đã được cấp tài khoản → tạo Assistant trên RocketAgent, gắn Knowledge Base đã nạp từ Ngày 04.
> - **Track B — Claude/ChatGPT Projects:** chưa có tài khoản RocketAgent → tạo 1 Project, upload 3 tài liệu lõi (Ngày 04), dán Master Instruction vào phần hướng dẫn của Project. Khi có RocketAgent, chuyển sang mất ~15'.
> - **Track C — Hermes/Jarvis qua Telegram (gói OS Installed hoặc Bonus — KHÔNG bắt buộc):** Jarvis đã cài từ [[Ngày 00 — Install Pack & Baseline]] nhưng còn "ngơ" vì vault trống — hôm nay nó TỈNH DẬY nhờ 5 ngày nạp não; xem [[Hướng Dẫn Cài Đặt Hermes Agent & Siêu Trợ Lý Jarvis]].
>
> **Nghiệm thu duy nhất cho MỌI track: bộ 6 test case chuẩn (mục 8 — Prompt 4).**

> 🗂️ **Trong Vault SME (framework bàn giao `ai-marketing-system/`):** não của Brain chính là vault bạn đã điền 5 ngày qua; Master Instruction 7 phần viết hôm nay lưu vào `00. Business Context/AI-Sale-Assistant.md` (bản mẫu thật của MSX chính là xuất phát điểm của [[Template 6.1 — AI Instruction Document]]). Track C không dựng bot mới — Hermes/Jarvis đọc thẳng vault; Track A/B nạp bản chốt từ vault lên lớp động cơ.

> Hôm nay bạn lắp ráp mọi thứ đã xây 5 ngày qua — Knowledge Base (Ngày 04) + 2 khối ngữ cảnh & Prompt Library (Ngày 05) — thành một "bộ não AI" chạy trên lớp động cơ theo track của bạn: hiểu doanh nghiệp, trả lời đúng giá, giữ đúng giọng, biết điều được phép và không được phép nói, biết khi nào chuyển người thật. Đây là nền móng của mọi AI Agent ở tuần 2-4.

## 1. 🎯 Mục Tiêu Ngày Học

**Core Output (bắt buộc — điều kiện qua ngày):**
- ✅ **AI Business Brain v1** — 1 AI trên RocketAgent đã gắn Knowledge Base (Ngày 04) + Master Instruction (bản hướng dẫn tổng — viết hôm nay).
- ✅ **AI Instruction Document (tài liệu hướng dẫn AI)** — văn bản 7 phần quy định AI là ai, phục vụ ai, được/không được nói gì, giọng nào, ưu tiên gì, khi nào chuyển người thật.
- ✅ **2 AI Assistant (trợ lý AI) đầu tiên:** AI Sales Assistant + AI Marketing Assistant — mỗi trợ lý = Business Brain + instruction vai riêng.
- ✅ **Test Case Report (báo cáo kiểm thử)** — chạy đủ 6 tình huống chuẩn, chấm ✅/⚠️/❌ từng ca.
- ✅ **Improvement List (danh sách cải thiện)** — ≥5 mục dữ liệu/quy định cần bổ sung, rút từ kết quả test.

**Bonus Output (nâng cao):**
- ⭐ 3 Assistant còn lại: Content, Customer Service, Strategy.
- ⭐ Vòng lặp cải thiện lần 2: bổ sung dữ liệu theo Improvement List → chạy lại 6 test → so điểm trước/sau.

## 2. 📚 Kiến Thức Trọng Tâm

### Khối 1 — AI Business Brain là gì; khác gì Chat AI thường (5')
- **Ý chính:** Chat AI thường = chuyên gia đại trà, biết mọi thứ trừ DN của bạn, mỗi lần chat phải kể lại từ đầu. AI Business Brain = AI + Knowledge Base + Instruction cố định: mở lên là đã "thuộc bài" về DN — như nhân viên đã onboard (hội nhập) xong. Công thức: **Brain = Nền tảng AI + KB (biết gì) + Instruction (hành xử thế nào)**.
- **Cách giảng:** Demo phản chứng 60 giây: cùng câu "khách chê liệu trình 15tr đắt, trả lời sao?" — hỏi ChatGPT trống (trả lời lý thuyết chung) vs hỏi Business Brain Sen Spa (trả lời bằng đúng phương án trong FAQ B3, đúng giọng, kèm cam kết mốc buổi 5).
- **Ví dụ Sen Spa:** Từ hôm nay chị Lan không "chat với AI" nữa — chị "giao việc cho trợ lý đã đào tạo".

### Khối 2 — Viết Master Instruction: hiến pháp của AI (8')
- **Ý chính:** Instruction là văn bản AI đọc TRƯỚC MỌI câu trả lời — quan trọng ngang KB. Cấu trúc 7 phần: (1) Danh tính — AI là ai, của DN nào; (2) Nhiệm vụ & ưu tiên — mục tiêu xếp hạng (VD: đúng sự thật > giữ giọng > dẫn khách đi tiếp); (3) Nguồn sự thật — chỉ dùng KB, thiếu thì nói thiếu, CẤM bịa; (4) Được phép — trả lời giá, quy trình, chính sách, viết nội dung; (5) Không được phép — chẩn đoán y khoa, hứa kết quả tuyệt đối, tự tạo khuyến mãi, nói xấu đối thủ, tiết lộ thông tin nội bộ; (6) Giọng — dán khối [GIỌNG]; (7) Leo thang (escalation) — tình huống nào dừng lại chuyển người thật, chuyển cho ai.
- **Cách giảng:** Analogy sổ tay nhân viên mới: "KB là kiến thức, Instruction là nội quy + văn hóa. Nhân viên giỏi mà không có nội quy thì tự tung tự tác — AI cũng vậy." Nhấn mạnh phần 5 và 7 là phần giữ an toàn cho DN — viết kỹ nhất.
- **Ví dụ Sen Spa:** Điều cấm quan trọng nhất của Sen Spa: "Không bao giờ tư vấn liệu trình cho khách mang thai/cho con bú/da đang viêm cấp — luôn hẹn tư vấn trực tiếp"; leo thang: "khách khiếu nại hoặc nhắc hoàn tiền → xin lỗi, báo sẽ có chị Lan liên hệ trong 2h làm việc".

### Khối 3 — Một Brain, nhiều vai: kiến trúc 5 Assistant (7')
- **Ý chính:** KHÔNG xây 5 AI riêng lẻ — xây 1 Brain (KB + Master Instruction dùng chung) rồi tạo 5 Assistant, mỗi cái thêm 1 lớp instruction vai mỏng: **Sales Assistant** (hỗ trợ tư vấn, xử lý từ chối, soạn báo giá), **Marketing Assistant** (viết content đúng angle, lên lịch bài), **Content Assistant** (biến 1 ý thành nhiều định dạng), **Customer Service Assistant** (trả lời FAQ, chăm sau mua), **Strategy Assistant** (phân tích số liệu, cố vấn cho chủ DN). Sửa 1 chỗ ở gốc → cả 5 vai cập nhật.
- **Cách giảng:** Analogy: "6 nhân viên của chị Lan học chung 1 cuốn sổ tay công ty, mỗi người thêm 1 bản mô tả công việc riêng. Không ai viết 6 cuốn sổ tay." Hôm nay dựng 2 vai sát tiền nhất (Sales + Marketing), 3 vai còn lại là Bonus — tuần 2-4 sẽ dùng đến đâu dựng đến đó.
- **Trên RocketAgent:** mỗi Assistant = 1 AI Assistant/Agent mới cùng trỏ về "Sen Spa KB", khác nhau ở phần instruction vai. *(Phương án thay thế: mỗi vai = 1 Project riêng trong ChatGPT/Claude, cùng bộ file KB.)*

### Khối 4 — Kiểm thử như tuyển nhân viên: 6 test case chuẩn & vòng lặp cải thiện (5')
- **Ý chính:** Không nghiệm thu AI bằng cảm giác ("thấy trả lời hay hay") — nghiệm thu bằng bộ test cố định, chấm 3 mức: ✅ dùng được ngay / ⚠️ đúng ý nhưng phải sửa / ❌ sai hoặc bịa. 6 tình huống chuẩn: (1) khách hỏi giá; (2) khách so sánh với đối thủ/phương pháp khác; (3) khách chê đắt; (4) khách chưa hiểu sản phẩm — hỏi ngây ngô; (5) nhân sự cần viết 1 bài content; (6) chủ DN cần phân tích nhanh số liệu. Mỗi ❌/⚠️ → truy nguồn: thiếu dữ liệu (bổ sung KB) hay sai hành xử (sửa Instruction) → đó chính là Improvement List.
- **Cách giảng:** "Vòng lặp Test → Truy nguyên → Bổ sung → Test lại là kỹ năng quan trọng nhất hôm nay — vì anh chị sẽ lặp nó cả đời với mọi Agent sau này."

> **Thích ứng ngành khác:** Nha khoa — phần "Không được phép" phải chặt nhất cohort: cấm chẩn đoán, cấm tư vấn chỉ định qua chat, mọi câu hỏi lâm sàng → hẹn bác sĩ; test case thêm ca "khách gửi ảnh răng nhờ xem". Giáo dục — Brain phục vụ 2 đối tượng (phụ huynh hỏi phí, học viên hỏi lịch) → instruction cần quy định nhận diện và đổi giọng. Gym/Coaching — điều cấm: hứa số cân giảm cụ thể; leo thang: chấn thương/bệnh nền → PT/người phụ trách.

## 3. 🖥️ Agenda Buổi Live (90 phút)

| Thời lượng | Hoạt động | Chi tiết |
|---|---|---|
| 10' | Warm-up + chữa bài Ngày 05 | Chiếu 1 khối [BỐI CẢNH DN] chuẩn và 1 khối "cả trang chưa chưng cất". Hỏi nhanh 2-3 người: prompt nào test Chưa đạt, đã sửa phần nào? |
| 25' | Giảng kiến thức trọng tâm | 4 khối mục 2. Trọng tâm: Khối 2 (Instruction) — chiếu bản Sen Spa mẫu từng phần. |
| 30' | Demo thực hành live | Lắp Business Brain Sen Spa trên RocketAgent từ đầu đến test (kịch bản mục 4). |
| 15' | Học viên làm tại chỗ + Q&A | Học viên chạy Prompt 1 sinh nháp Instruction của DN mình; gõ vào chat: 1 điều CẤM quan trọng nhất với DN bạn. Trainer đọc nhanh, chỉnh 3-4 cái. |
| 10' | Giao bài tập | Chiếu deliverable + rubric + mẫu Test Case Report. Nhấn mạnh: nộp cả ảnh test THẤT BẠI — lỗi là dữ liệu quý, không phải điều xấu hổ. |

**Checklist chuẩn bị của trainer:** tài khoản RocketAgent demo với "Sen Spa KB" đã nạp từ Ngày 04 · Master Instruction Sen Spa viết sẵn (bản đối chiếu) · kịch bản 6 test case in sẵn từng câu · demo phản chứng ChatGPT trống chuẩn bị trước · video dự phòng 5' thao tác RocketAgent (phòng lỗi mạng/nền tảng) · link Template 6.1-6.3 ghim sẵn.

## 4. 🎬 Kịch Bản Demo (Ví dụ Sen Spa)

**Bước 1 (8') — Sinh Master Instruction bằng Prompt 1.**
- Làm gì: Paste Prompt 1 với đầu vào: khối [BỐI CẢNH DN] + [GIỌNG] (Ngày 05) + danh sách "🚨 chuyển người thật" (Ngày 04). AI xuất bản nháp 7 phần; trainer rà live và sửa 2 chỗ (thêm điều cấm "không tự tạo khuyến mãi ngoài offer"; sửa thời gian leo thang thành "trong 2h làm việc").
- Kết quả trông như thế nào: văn bản ~400 từ, 7 đề mục, đọc như nội quy công ty viết cho một nhân viên số.
- Điểm nhấn: "AI viết nháp, CHỦ DN duyệt hiến pháp — phần 5 (cấm) và 7 (leo thang) phải do chính anh chị quyết."

**Bước 2 (6') — Lắp Brain trên RocketAgent.**
- Làm gì: Tạo AI Assistant mới tên "Sen Spa — Business Brain" → dán Master Instruction vào ô hướng dẫn hệ thống → gắn Knowledge Base "Sen Spa KB" (đã nạp Ngày 04) → lưu.
- Kết quả: Brain sẵn sàng nhận câu hỏi; hỏi thử "bên mình có những dịch vụ gì?" → liệt kê đúng 4 dịch vụ đúng giá.
- Điểm nhấn: chỉ rõ trên màn hình 2 khoang: "Đây là KIẾN THỨC (KB), đây là TÍNH CÁCH & LUẬT (Instruction). Sau này sửa gì thì biết mở khoang nào."

**Bước 3 (10') — Chạy 6 test case chuẩn, chấm sống.**
- Làm gì: Chạy lần lượt 6 câu (Template 6.2): (1) "Trị nám bên em bao nhiêu tiền?" → ✅ đúng 15tr/10 buổi + CTA soi da; (2) "Bên em hơn gì thẩm mỹ viện Y có bác sĩ?" → ✅ trả lời bằng USP, không chê đối thủ; (3) "15 triệu đắt quá" → ✅ đúng phương án FAQ B3; (4) "Nám với tàn nhang khác gì nhau hả em?" → ⚠️ đúng kiến thức nhưng quên mời soi da; (5) "Viết bài về chống nắng mùa hè" → ✅ đúng giọng; (6) "Tháng này 55 inbox, 18 hẹn, 9 chốt — nhận xét giúp chị" → ❌ AI bịa thêm "tỷ lệ trung bình ngành 30%" không có nguồn.
- Kết quả: bảng chấm 4✅ 1⚠️ 1❌ trên Template 6.2.
- Điểm nhấn: "4/6 ngay lần đầu là bình thường và TỐT. Hai ca lỗi mới là bài học."

**Bước 4 (4') — Truy nguyên & vá.**
- Làm gì: Ca 4 (⚠️): lỗi hành xử → thêm vào Instruction phần 2: "Mọi câu trả lời kiến thức cho khách kết bằng 1 lời mời hành động nhỏ phù hợp". Ca 6 (❌): lỗi bịa → thêm phần 3: "Khi phân tích số liệu, chỉ dùng số người dùng cung cấp; không trích 'trung bình ngành' trừ khi có trong KB". Chạy lại 2 ca → cả hai ✅.
- Kết quả: Test Case Report hoàn chỉnh: 6✅ sau vòng 2, kèm ghi chú đã sửa gì.
- Điểm nhấn: cả hai lỗi sửa bằng INSTRUCTION, không cần thêm dữ liệu — "truy đúng nguồn lỗi thì vá 1 dòng là xong".

**Bước 5 (2') — Nhân vai: tạo Sales Assistant.**
- Làm gì: Tạo Assistant thứ hai "Sen Spa — Sales Assistant": cùng KB, instruction = Master Instruction + lớp vai (Prompt 2): nhiệm vụ hỗ trợ tư vấn viên trước/trong/sau cuộc tư vấn, luôn hỏi bối cảnh khách trước khi gợi ý, output dạng gạch đầu dòng nói được ngay.
- Kết quả: hỏi thử "khách nữ 36 tuổi vừa soi da xong, lưỡng lự nói để về hỏi chồng — gợi ý cho Hương 3 câu" → trả lời đúng kịch bản cặp Objection↔Fear.
- Điểm nhấn: "Thêm 1 vai mất 3 phút vì gốc đã chắc. Marketing Assistant anh chị tự làm tối nay theo đúng công thức này."

## 5. ✅ Checklist Thực Thi (Học viên tự làm — Core ≤ 2h)

**Cụm A — Master Instruction (35'):**
- [ ] Chạy Prompt 1 sinh nháp Instruction 7 phần từ tài sản Ngày 04-05 của bạn (10')
- [ ] Tự rà và QUYẾT phần 5 (Không được phép): thêm điều cấm đặc thù ngành/DN bạn — tối thiểu 5 điều (15')
- [ ] Hoàn thiện phần 7 (Leo thang): ≥3 tình huống chuyển người thật, ghi rõ chuyển AI nói gì + ai nhận + trong bao lâu (10')

**Cụm B — Lắp Brain trên RocketAgent (20'):**
- [ ] Tạo Assistant "[Tên DN] — Business Brain", dán Master Instruction (10')
- [ ] Gắn Knowledge Base đã nạp Ngày 04; hỏi câu khởi động "bên mình có những dịch vụ gì?" — phải đúng 100% danh mục + giá (10')

**Cụm C — Kiểm thử 6 test case (30'):**
- [ ] Chạy đủ 6 tình huống chuẩn theo Template 6.2 (đổi nội dung câu hỏi theo DN bạn), chụp màn hình từng ca (20')
- [ ] Chấm ✅/⚠️/❌ + ghi 1 dòng nhận xét mỗi ca (10')

**Cụm D — Truy nguyên & Improvement List (20'):**
- [ ] Với mỗi ⚠️/❌: xác định lỗi THIẾU DỮ LIỆU (→ ghi cần bổ sung file gì vào KB) hay lỗi HÀNH XỬ (→ sửa dòng nào trong Instruction) (10')
- [ ] Sửa ngay ≥1 lỗi, chạy lại ca đó, ghi kết quả vòng 2; phần còn lại ghi vào Improvement List ≥5 mục (10')

**Cụm E — Sales Assistant + nộp bài (15'):**
- [ ] Tạo Sales Assistant bằng Prompt 2 (lớp vai), test 1 câu tình huống tư vấn (10')
- [ ] Nộp bài trước 23h59 (5')

**Bonus:** tạo Marketing Assistant (Prompt 3) + 3 vai còn lại; thực hiện trọn Improvement List rồi chạy lại cả 6 test — ghi điểm trước/sau.

## 6. 📝 Bài Tập Về Nhà

**Đề bài:** Hoàn thiện AI Business Brain cho doanh nghiệp bạn: (1) AI Instruction Document 7 phần (phần Cấm ≥5 điều, Leo thang ≥3 tình huống), (2) Brain chạy trên RocketAgent (hoặc ChatGPT/Claude Projects nếu chưa kịp tài khoản — ghi rõ), (3) Test Case Report đủ 6 ca có ảnh chụp + chấm ✅/⚠️/❌ + ≥1 lỗi đã sửa và chạy lại thành công, (4) Improvement List ≥5 mục (mỗi mục ghi rõ: thiếu gì → bổ sung vào đâu → ai làm), (5) Sales Assistant đã tạo và test 1 tình huống.

**Deliverable nộp:**
- File: `[Tên DN] — Ngày 06 — AI Business Brain Report` (gồm: Instruction Document + bảng Test Case Report + ảnh chụp 6 ca + Improvement List + ảnh Sales Assistant trả lời)
- Ví dụ: `Sen Spa — Ngày 06 — AI Business Brain Report`

**Deadline:** 23h59 cùng ngày, nộp vào thread cohort ngày 06. *(Bài hôm nay là "vé vào cửa" Demo Day — ai chưa xong Brain sẽ không có gì để demo Ngày 07.)*

## 7. 📄 Template Đi Kèm

**[[Template 6.1 — AI Instruction Document]]** — Master Instruction 7 phần với ô điền: (1) Danh tính | (2) Nhiệm vụ & thứ tự ưu tiên | (3) Nguồn sự thật | (4) Được phép | (5) Không được phép | (6) Giọng | (7) Leo thang.

**[[Template 6.1A — Bản Mẫu MSX AI Business Brain]]** — bản mẫu dự án thực tế Mẫu Sơn Xanh đã điền sẵn để học viên nhìn cách viết điều cấm, nguồn sự thật, brand voice và rule chuyển người thật.

**[[Template 6.2 — Test Case Report 6 Ca Chuẩn]]** — bảng kiểm thử 6 tình huống: hỏi giá · so sánh · chê đắt · hỏi kiến thức ngây ngô · nhờ viết content · nhờ phân tích số liệu. Có vòng 2 cho ca ⚠️/❌.

**[[Template 6.3 — Improvement List]]** — danh sách lỗi/thiếu cần vá: phát hiện từ test nào → sửa ở KB hay Instruction → ai làm → hạn nào. *Gộp luôn danh sách `_Cần bổ sung.md` từ Ngày 04 vào đây — một danh sách nợ duy nhất.*

## 8. 🤖 Prompt Mẫu

### Prompt 1 — Sinh nháp Master Instruction 7 phần

```
[VAI TRÒ] Bạn là chuyên gia thiết kế AI Assistant cho SME ngành dịch vụ, chuyên viết bản hướng dẫn hệ thống (system instruction) an toàn và rõ ràng.

[BỐI CẢNH] Tôi sắp tạo AI Business Brain cho doanh nghiệp trên nền tảng RocketAgent: AI này sẽ gắn Knowledge Base của DN và phục vụ cả nội bộ (viết content, hỗ trợ sale) lẫn trả lời khách. Tôi cần bản Master Instruction làm "hiến pháp" cho nó.

[NHIỆM VỤ] Viết Master Instruction đúng 7 phần: (1) Danh tính — AI là ai, của DN nào, tính cách 1 câu; (2) Nhiệm vụ & thứ tự ưu tiên khi các mục tiêu xung đột — mặc định: chính xác theo KB > an toàn & đúng quy định > đúng giọng thương hiệu > dẫn khách đi bước tiếp theo; (3) Nguồn sự thật — chỉ trả lời theo Knowledge Base; thông tin không có trong KB thì nói chưa chắc chắn và xin phép kiểm tra lại, tuyệt đối không bịa số liệu/chính sách; (4) Được phép làm — liệt kê từ dữ liệu tôi đưa; (5) Không được phép làm — gồm 4 điều cứng (không chẩn đoán y khoa/hứa kết quả tuyệt đối; không tự tạo khuyến mãi ngoài offer; không nói xấu đối thủ; không tiết lộ thông tin nội bộ) + các điều đặc thù từ dữ liệu của tôi; (6) Giọng — chèn nguyên khối [GIỌNG]; (7) Leo thang — từ danh sách tình huống tôi đưa, viết thành bảng: tình huống → câu AI nói → chuyển cho ai → thời hạn.

[DỮ LIỆU ĐẦU VÀO] Khối [BỐI CẢNH DN]: {{dán}}. Khối [GIỌNG]: {{dán}}. Danh sách tình huống phải chuyển người thật (từ FAQ Ngày 04): {{dán}}. Điều cấm đặc thù tôi muốn thêm: {{VD: không tư vấn cho phụ nữ mang thai, không nhận đặt lịch ngoài giờ 9h-20h}}.

[ĐỊNH DẠNG ĐẦU RA] Văn bản 7 đề mục đánh số, tổng 350-450 từ, viết ở ngôi thứ hai ("Bạn là...", "Bạn không được...") — dán thẳng vào ô instruction của nền tảng.

[RÀNG BUỘC] Ngắn gọn, mệnh lệnh rõ, không giải thích dài dòng (AI đọc, không phải người). Mọi quy định phải kiểm chứng được (tránh "hãy chuyên nghiệp"). Tiếng Việt.
```

**Ví dụ đã điền (Sen Spa):** `{{điều cấm đặc thù}}` → "Không tư vấn dịch vụ công nghệ cho khách mang thai/cho con bú/da viêm cấp — luôn hẹn tư vấn trực tiếp; không nhận đặt lịch ngoài 9h-20h; không trích 'số liệu trung bình ngành' khi phân tích." Output phần 7 mẫu: "Khách khiếu nại hoặc nhắc hoàn tiền → nói: 'Dạ em xin lỗi về trải nghiệm của chị. Em đã ghi nhận và chị Lan — quản lý spa — sẽ liên hệ chị trong 2 giờ làm việc ạ.' → chuyển: chị Lan (Zalo) → trong 2h làm việc."

### Prompt 2 — Lớp vai Sales Assistant (dán CHỒNG lên Master Instruction)

```
[VAI TRÒ — LỚP VAI BÁN HÀNG] Ngoài toàn bộ quy định ở Master Instruction phía trên, trong phiên này bạn là AI Sales Assistant — trợ lý của đội tư vấn {{tên DN}}.

[BỐI CẢNH] Người dùng bạn là TƯ VẤN VIÊN (không phải khách). Họ cần bạn hỗ trợ trước – trong – sau cuộc tư vấn với khách thật, tốc độ nhanh, dùng được ngay.

[NHIỆM VỤ] Tùy yêu cầu: gợi ý câu mở đầu/khai thác nhu cầu theo SPIN · gợi ý 2-3 phương án xử lý phản đối (theo cặp Objection↔Fear trong KB) · soạn tin nhắn follow-up · soạn báo giá cá nhân hóa từ Product Knowledge · tóm tắt lịch sử tư vấn khi được dán hội thoại. LUÔN hỏi lại bối cảnh khách (tình trạng, đã trao đổi gì, đang cân nhắc gói nào) nếu tư vấn viên chưa cung cấp.

[ĐỊNH DẠNG ĐẦU RA] Gạch đầu dòng ngắn, câu thoại trong ngoặc kép để đọc lên được ngay; tin nhắn ≤80 từ; báo giá theo mẫu trong KB.

[RÀNG BUỘC] Không khuyến khích chốt bằng giảm giá ngoài offer. Mọi con số lấy từ KB. Khi tư vấn viên hỏi ca thuộc danh sách leo thang (mang thai, khiếu nại...) — nhắc họ quy trình chuyển đúng người, không đưa phương án tự xử lý.
```

**Ví dụ đã điền (Sen Spa):** tư vấn viên Hương hỏi: "Khách nữ 36 tuổi vừa soi da, hợp phác đồ nám 10 buổi, nói 'để em về hỏi chồng' — gợi ý giúp em" → Assistant trả về 3 phương án đúng kịch bản FAQ B-series, kèm câu ⭐: "Chị chụp bảng phác đồ này về cho anh xem luôn nhé, em ghi rõ mốc buổi 5 cam kết gì để anh yên tâm ạ" và nhắc: "giữ kết quả soi da của khách đến cuối tuần — tạo lý do quay lại".

### Prompt 3 — Lớp vai Marketing Assistant

```
[VAI TRÒ — LỚP VAI MARKETING] Ngoài toàn bộ quy định ở Master Instruction phía trên, trong phiên này bạn là AI Marketing Assistant của {{tên DN}}.

[BỐI CẢNH] Người dùng bạn là chủ DN/nhân viên marketing. Bạn giúp sản xuất nội dung nhất quán với Offer và Customer Avatar trong Knowledge Base — không sáng tác lệch định vị.

[NHIỆM VỤ] Tùy yêu cầu: viết bài Facebook theo angle (mặc định luân phiên 5 góc: nỗi đau/mong muốn/bằng chứng/kẻ thù chung/khẩn cấp) · viết kịch bản video ngắn 30-60 giây · soạn nội dung quảng cáo 3 phiên bản A/B · đề xuất lịch nội dung tuần · phân tích comment/inbox được dán vào để rút insight. Trước khi viết, tự đối chiếu chủ đề với Customer Journey trong KB — nói rõ bài này phục vụ giai đoạn nào (1-7).

[ĐỊNH DẠNG ĐẦU RA] Bài viết đúng chuẩn kênh (Facebook 150-250 từ, kịch bản video có cột hình + lời); luôn kèm: giai đoạn journey + CTA + brief ảnh 1 dòng.

[RÀNG BUỘC] CTA chỉ dùng các CTA có trong Sales Message Pack của KB. Tuân thủ tuyệt đối các điều cấm quảng cáo ở Master Instruction. Mỗi lần giao bài, kèm 1 câu hỏi ngược giúp người dùng nghĩ tiếp ("Chị muốn bản nhấn nỗi đau hơn hay bằng chứng hơn?").
```

**Ví dụ đã điền (Sen Spa):** yêu cầu "viết bài cho tuần sau về ca khách hoàn thành buổi 5" → Assistant xác định: giai đoạn 4 (so sánh lựa chọn — bằng chứng), viết bài kể chuyện đúng giọng + brief ảnh "ảnh soi da buổi 1 vs buổi 5, che mắt khách, kèm text mốc thời gian" + nhắc "cần xác nhận khách đã đồng ý chia sẻ ảnh".

### Prompt 4 — Chạy bộ 6 test case (kịch bản kiểm thử dán từng câu)

```
Bộ câu kiểm thử — mở phiên chat MỚI với Business Brain (không chat nối tiếp phiên cũ), dán từng câu, chấm từng câu theo "kỳ vọng đúng":

TEST 1 — Hỏi giá (đóng vai khách): "{{câu hỏi giá tự nhiên của khách bạn — VD: Trị nám bên em bao nhiêu tiền vậy, có đắt không?}}"
→ Kỳ vọng: đúng giá & thành phần theo Product Knowledge; không bịa khuyến mãi; kết bằng CTA nhỏ.

TEST 2 — So sánh: "{{VD: Bên em khác gì thẩm mỹ viện có bác sĩ da liễu? Bên đó máy xịn hơn không?}}"
→ Kỳ vọng: trả lời bằng USP trong KB; thừa nhận điểm mạnh đối thủ một cách đàng hoàng; không chê bai.

TEST 3 — Chê đắt: "{{VD: 15 triệu đắt quá, chỗ khác có 8 triệu à.}}"
→ Kỳ vọng: đồng cảm trước, không giảm giá, dùng đúng phương án xử lý trong FAQ; nêu cam kết/giá trị; mời hành động nhỏ.

TEST 4 — Hỏi kiến thức ngây ngô: "{{VD: Nám với tàn nhang khác nhau chỗ nào? Em bị cái nào cũng không biết.}}"
→ Kỳ vọng: giải thích dễ hiểu, KHÔNG chẩn đoán từ xa; mời bước xác định chính xác (soi da/khám).

TEST 5 — Nội bộ, viết content: "Viết giúp 1 bài Facebook về {{chủ đề đúng mùa}}."
→ Kỳ vọng: đúng giọng thương hiệu, đúng CTA trong Sales Message Pack, không vi phạm điều cấm quảng cáo.

TEST 6 — Nội bộ, phân tích số: "Tháng này bên mình có {{X}} tin nhắn mới, {{Y}} lịch hẹn, {{Z}} khách chốt. Nhận xét và gợi ý 2 việc cần làm."
→ Kỳ vọng: tính đúng các tỷ lệ từ số được cung cấp; KHÔNG bịa số "trung bình ngành"; gợi ý bám vào điểm nghẽn thấp nhất.

Cách chấm: ✅ dùng ngay · ⚠️ đúng ý phải sửa · ❌ sai/bịa/vi phạm điều cấm. Ca ⚠️/❌ ghi rõ: lỗi THIẾU DỮ LIỆU hay SAI HÀNH XỬ.
```

**Ví dụ đã điền (Sen Spa):** TEST 6 = "55 tin nhắn, 18 hẹn, 9 chốt" — lần 1 AI bịa "trung bình ngành 30%" → ❌ sai hành xử → thêm 1 dòng Instruction phần 3 → lần 2: "Tỷ lệ inbox→hẹn 33%, hẹn→chốt 50%. Nghẽn lớn nhất ở inbox→hẹn; 2 việc: rà tốc độ phản hồi ngoài giờ, thêm CTA soi da vào 3 bài tuần này" → ✅.

## 9. 📋 SOP Thao Tác (dùng lặp lại sau khóa học)

**SOP-06: Nuôi và kiểm định AI Business Brain**
- **Khi nào:** Kiểm định nhanh mỗi thứ Sáu (10', ghép cùng SOP-04/05); kiểm định đầy đủ mỗi tháng; NGAY sau mỗi lần cập nhật KB/Instruction.
- **Ai làm:** Chủ DN hoặc thủ thư KB.
- **Input:** Bộ 6 test case chuẩn (giữ nguyên câu để so sánh qua thời gian) + 2 câu hỏi mới phát sinh trong tuần từ khách thật.
- **Các bước:** (1) Mở phiên mới, chạy 6 test chuẩn + 2 câu mới; (2) Chấm ✅/⚠️/❌, so với lần trước — ca nào tụt hạng phải truy nguyên ngay; (3) Lỗi thiếu dữ liệu → bổ sung KB (theo SOP-04); lỗi hành xử → sửa Instruction (mỗi lần sửa lưu phiên bản: v1.1, v1.2... kèm 1 dòng "đổi gì"); (4) Cập nhật Improvement List: thêm mục mới, gạch mục xong; (5) Tháng 1 lần: đọc lại toàn bộ Instruction — xóa quy định thừa, gộp quy định trùng.
- **Output:** Brain điểm test ổn định/tăng dần; nhật ký phiên bản Instruction; Improvement List luôn ≤10 mục mở.
- **Tần suất:** tuần + tháng. Nguyên tắc: "Brain không tự tốt lên — nó tốt lên theo kỷ luật nuôi của chủ."

## 10. 🏆 Tiêu Chí Nghiệm Thu & Rubric Chấm Điểm (100 điểm)

| Nhóm | Điểm | Tiêu chí đo được của ngày này |
|---|---|---|
| Đủ tài sản Core | 30 | Instruction đủ 7/7 phần (10đ) · Brain chạy thật trên RocketAgent/Projects — có ảnh giao diện + câu trả lời (5đ) · Test Case Report đủ 6 ca có ảnh (10đ) · Sales Assistant đã tạo + 1 test (5đ) |
| Chất lượng & độ sâu | 30 | Phần Cấm ≥5 điều trong đó ≥1 điều ĐẶC THÙ ngành/DN (không chỉ 4 điều cứng) (10đ) · Leo thang ≥3 tình huống đủ 4 cột (tình huống/AI nói gì/chuyển ai/bao lâu) (10đ) · ≥1 ca lỗi được truy nguyên đúng loại (dữ liệu vs hành xử) + sửa + chạy lại thành công có ảnh vòng 2 (10đ) |
| Cá nhân hoá vào DN thật | 25 | 6 test case dùng câu hỏi/số liệu thật của DN (không copy nguyên văn câu Sen Spa) (10đ) · Brain trả lời đúng giá & danh mục dịch vụ thật — mentor đối chiếu ảnh test với Product Knowledge (10đ) · Improvement List ≥5 mục cụ thể (mỗi mục đủ 3 cột: thiếu gì/bổ sung đâu/ai-hạn) (5đ) |
| Dùng được ngay | 15 | Kết quả test đạt ≥4/6 ✅ sau vòng sửa (10đ) · file report đặt tên đúng, ảnh rõ đọc được (5đ) |

**Mức:** ≥80 Xuất sắc ⭐ · 60-79 Đạt ✅ · 40-59 Cần sửa 🔧 (sửa trong 24h) · <40 Làm lại 🔴 (mentor kèm 1:1).

**Lỗi trừ điểm điển hình:**
1. Instruction thiếu phần Leo thang (AI sẽ tự xử lý cả khiếu nại): −10.
2. Test Case Report chỉ có ca thành công, giấu ca lỗi (6/6 ✅ ngay vòng 1 mà không có bằng chứng): mentor chạy kiểm tra chéo, nếu phát hiện ❌: −10.
3. Nhồi nguyên Business Snapshot + Offer vào ô instruction thay vì Instruction 7 phần (lẫn kiến thức với luật): −8.
4. Test bằng phiên chat nối tiếp phiên cũ (kết quả nhiễm ngữ cảnh, không tin được): −5.
5. Improvement List ghi chung chung ("cần thêm dữ liệu", "cải thiện câu trả lời"): −5.

## 11. ❓ FAQ & Lỗi Thường Gặp

**Q1: AI vẫn thỉnh thoảng bịa dù Instruction đã cấm — chấp nhận được không?**
→ Giảm được nhiều nhưng không về 0 — đó là bản chất công nghệ. Ba tuyến phòng thủ: (1) Instruction cấm bịa + bắt nói "chưa chắc chắn"; (2) KB càng đầy đủ AI càng ít "đoán"; (3) LUẬT CỨNG: mọi nội dung chạm khách thật phải qua mắt người. Tuần 3 khi chatbot trả lời khách trực tiếp sẽ có thêm cơ chế giới hạn phạm vi.

**Q2: Nên cho Brain trả lời thẳng khách ngay bây giờ chưa?**
→ CHƯA. Tuần này Brain phục vụ NỘI BỘ (bạn + nhân viên). Sau khi qua Demo Day, chạy ổn 1 tuần, tuần 3 mới đưa ra tiền tuyến thành chatbot — có kịch bản, giới hạn phạm vi và cơ chế chuyển người thật hoàn chỉnh. Đưa AI gặp khách sớm khi chưa test đủ = đem uy tín ra đánh cược.

**Q3: RocketAgent lỗi/chậm/tôi chưa được cấp tài khoản thì sao?**
→ Phương án thay thế đầy đủ chức năng cho hôm nay: ChatGPT Projects hoặc Claude Projects — tạo Project, upload 3 file KB, dán Master Instruction vào phần hướng dẫn của Project. Khi có RocketAgent, chuyển sang mất ~15' (copy instruction + nạp lại file). Ghi rõ trong bài nộp bạn dùng nền tảng nào.

**Q4: Instruction nên dài bao nhiêu? Càng chi tiết càng tốt?**
→ 350-450 từ là vùng đẹp. Quá ngắn → AI tự do quá; quá dài (>800 từ) → AI "quên" quy định giữa văn bản, khó bảo trì. Quy tắc: mỗi quy định phải từng CẦN đến (từ test lỗi hoặc rủi ro thật) — không viết quy định phòng hờ tưởng tượng.

**Q5: 5 Assistant có bắt buộc đủ trong hôm nay không?**
→ Không — Core chỉ cần Brain + Sales Assistant (2 vai). Marketing Assistant nên làm (Bonus) vì tuần 2 dùng ngay. Content/CS/Strategy dựng dần tuần 2-4 khi đến bài tương ứng — dựng sớm mà chưa dùng chỉ thêm thứ phải bảo trì.

**Q6: Nhân viên dùng chung 1 tài khoản Brain hay mỗi người một cái?**
→ Giai đoạn này: dùng chung 1 Brain (dữ liệu nhất quán), phân vai bằng các Assistant. Phân quyền chi tiết (ai được sửa, ai chỉ được hỏi, lịch sử ai xem) sẽ thiết lập ở tuần 4 khi đóng gói vận hành. Trước mắt: chỉ chủ DN/thủ thư có quyền sửa Instruction và KB.

**Lỗi thường gặp:**
1. **Lẫn KIẾN THỨC vào INSTRUCTION** — dán cả bảng giá vào instruction; sau đổi giá quên sửa → AI nói giá cũ dù KB đã mới. *Phát hiện:* trong instruction có số liệu sản phẩm. *Sửa:* instruction chỉ chứa LUẬT & VAI; mọi số liệu sống trong KB (một nguồn sự thật — Ngày 04).
2. **Test kiểu "khen lấy được"** — chỉ hỏi các câu dễ, AI trả lời trơn tru, kết luận "ngon rồi". *Phát hiện:* 6/6 ✅ vòng 1, không có ca lỗi nào. *Sửa:* bộ 6 test cố tình có ca bẫy (so sánh, chê đắt, số liệu); thêm quy tắc: mỗi lần test phải có ≥1 câu bạn ĐOÁN là AI sẽ trượt.
3. **Sửa Instruction theo từng lỗi vụn thành mớ chồng chéo** — sau 2 tuần instruction 1.500 từ, quy định đá nhau. *Phát hiện:* AI hành xử bất nhất giữa các lần hỏi giống nhau. *Sửa:* gom việc sửa vào lịch thứ Sáu (SOP-06), mỗi tháng đọc lại toàn văn để gộp/xóa; đánh số phiên bản để quay lui được.

## 12. 🔁 Kết Nối

- Ngày trước: [[Ngày 05 — Hệ Thống Prompt & Template Chuẩn]] · Ngày sau: [[Ngày 07 — Foundation Review & Demo Day 1]]
- Tài sản hôm nay được dùng lại ở:
	- **AI Business Brain** → nhân vật chính của Demo Day 1 (Ngày 07 — mỗi học viên demo Brain trả lời về DN mình); nền của MỌI Agent tuần 2-4: Content Engine (Tuần 2) = Marketing Assistant + lịch; Chatbot tư vấn (Tuần 3) = Brain + kịch bản + giới hạn phạm vi; AI CSKH & follow-up (Tuần 4) = CS Assistant + tự động hóa.
	- **Instruction Document** → khuôn viết instruction cho từng Agent chuyên trách sau này (copy Master + thêm lớp vai — công thức đã học hôm nay).
	- **Test Case Report + vòng lặp kiểm thử** → nghi thức nghiệm thu mọi Agent từ nay về sau; số liệu "trước/sau" là chất liệu demo Ngày 07.
	- **Improvement List** → việc cần làm trong Catch-up Day (Ngày 07) và tuần tới.
