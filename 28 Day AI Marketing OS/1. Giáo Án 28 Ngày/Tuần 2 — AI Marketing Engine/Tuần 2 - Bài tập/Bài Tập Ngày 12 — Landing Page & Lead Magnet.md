---
up:
  - "[[Ngày 12 — Landing Page & Lead Magnet]]"
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-15
tags: [project, aios, bai-tap]
week: 2
day: 12
---

# 📋 Bài Tập Ngày 12 — Landing Page & Lead Magnet

> **Triết lý hôm nay: bạn KHÔNG viết landing page — bạn LẮP nó từ tài sản Tuần 1, rồi cắm điểm chuyển đổi vào cỗ máy tự chạy.** Việc của bạn có 4 nhịp: dựng **Form thu lead CHẠY THẬT** → **LẮP** copy 9 khối (mỗi khối có mã nguồn) → đóng gói quà **"Bảng so sánh 10 tiêu chí"** thành PDF → nối **Hermes tự nhắn quà qua Zalo**. Nghiệm thu không đọc file: *mentor bấm link trên điện thoại, điền form, và QUÀ PHẢI TỚI ZALO trong <2 phút.* Bản mẫu để đối chiếu: [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]].

---

## 1. 🎯 Hôm nay bạn tạo ra gì

**Core Output (bắt buộc — điều kiện qua ngày):**

| # | Tài sản | Chuẩn nghiệm thu |
|---|---------|------------------|
| 1 | **Form thu lead CHẠY THẬT** | 5–6 trường, **bắt buộc có trường phân loại dạng danh sách chọn** (= mầm CRM Tuần 3) → ghi thẳng vào **Google Sheet**. Test: điền trên điện thoại là lead rơi xuống Sheet |
| 2 | **Landing Page Copy 9 khối** | Bảng **có cột `Mã nguồn`** — **≥8/9 khối** truy về tài sản Tuần 1; khối 3 = `V#`, khối 9 = `Q##`, khối 8 = `OF#` (bắt buộc 100%) |
| 3 | **Lead Magnet PDF** = **"Bảng so sánh 10 tiêu chí"** | PDF 4–8 trang làm bằng AI + Canva, **trang cuối có CTA về offer thật (`OF#`)**, có ≥2 chi tiết chuyên môn thật |
| 4 | **TRAO QUÀ TỰ ĐỘNG (luồng vàng)** | Landing (Vercel *hoặc* Google Form) → Sheet → **Hermes theo dõi Sheet → tự nhắn Zalo link PDF trong <2 phút.** Fallback: người trực gửi tay |
| 5 | **Lead Flow Map 6 trạm** | 1 trang, **TÊN NGƯỜI THẬT** mỗi trạm + **1 dòng Data Security** (lead = tầng Restricted, ai xem, lưu đâu) |

> 🔴 **Nghiệm thu = HÀNH ĐỘNG, không phải file:** mentor **bấm link trên điện thoại** → **điền form** → **lead hiện trong Sheet** → **QUÀ TỚI ZALO trong <2 phút**. Quà không tới = phễu chưa chạy = phần đó 0 điểm, không tranh luận.

**Bonus Output (không bắt buộc, không trừ điểm):**
- ⭐ Landing **dựng đẹp trên Vercel** (`*.vercel.app` free) có ảnh vùng nguyên liệu + Brand Kit N10
- ⭐ **Chuỗi nuôi dưỡng Zalo D1–D10** (tầng 🟡 ASSISTED — người duyệt cả 10 trước khi bật; xem N13)
- ⭐ Lead magnet **#2** dạng khác (*Cẩm nang Trà Tối 7 ngày* cho tệp chưa so sánh)

---

## 2. 📥 Chuẩn bị

**Input từ các ngày trước (mở sẵn 4 tài liệu — landing là BẢN LẮP RÁP, không viết mới):**

| Tài liệu | Từ ngày | Dùng vào khối | Mã nguồn |
|----------|:---:|----------|:---:|
| 5 câu nguyên văn khách thật (Avatar + PDFO) | N2 | Khối 3 (Vấn đề) + hook | `V1…V5` |
| Core Offer 7 khối | N3 | Khối 8 (CTA) + trang cuối PDF | `OF1…OF7` |
| Sales Message Pack (hook/headline/CTA) | N3 | Khối 1–2 | `MSG` |
| FAQ & Objection Database ≥30 cặp | N4 | **Khối 9 — LẤY THẲNG, CẤM viết mới** | `Q##` |
| Product Knowledge (vùng nguyên liệu, quy trình) | N4 | Khối 5 + ruột PDF | `PK` |
| Data Security Rule | N4 | Lead Flow Map (lead = Restricted) | `DS` |
| Brand Voice Guideline (kế thừa T8.0) | N8/N9 | Giọng toàn trang + tin Zalo | `GIỌNG` |

**Template cần mở (wikilink):**
- [[Ngày 12 — Landing Page & Lead Magnet]] — giáo án gốc (kịch bản demo + 4 prompt đầy đủ)
- [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]] — **bản mẫu MSX + phiếu đầu bài + nghiệm thu**
- T12.1 Bảng chọn Lead Magnet · T12.2 Landing Copy 9 khối (**có cột Mã nguồn**) · T12.3 Form chuẩn + nối Sheet · T12.4 Lead Flow Map

**Track công cụ (chạy prompt ở đâu — bạn thuộc track nào thì làm trên nhánh đó):**

| Track | Chạy prompt & vận hành ở đâu |
|-------|-------------------|
| **A — RocketAgent** (mặc định) | Chạy prompt trong AI Marketing Assistant (đã nạp KB N6) — không dán lại ICP/Offer |
| **B — Claude/ChatGPT Projects** | Chạy trong Project đã upload 3 tài liệu lõi + Brand Voice |
| **C — Hermes/Jarvis** | Nhắn prompt trực tiếp cho Hermes — **và Hermes chính là engine trao quà Zalo 24/7** |

**Đường dựng phễu (chọn 1):** 🅰️ **Vercel** (trang đẹp, `*.vercel.app` free) · 🅱️ **Đường siêu tắt** — dùng thẳng **Google Form N12** làm nơi nhận lead (Hermes vẫn đọc cùng Sheet, nhắn Zalo y hệt). Bí thì đi đường 🅱️ — phễu vẫn chạy thật.

**Trong Vault SME:** copy landing lưu `04. Resources/Playbooks/`; lead đổ về `People/` (mỗi lead 1 file, ghi rõ Phân loại) — chịu **Data Security Rule tầng Restricted (N4)**.

---

## 3. ✅ Các bước

> ⏱ Mỗi cụm ghi 2 số: **dùng template điền sẵn / lần đầu tự làm**. Tổng: **110' theo template · lần đầu ~165'**.
> 🔴 **THỨ TỰ BẮT BUỘC — không đảo:** Cụm A (Form) TRƯỚC → mới tới Cụm C (PDF). *Người làm PDF trước thì 23h vẫn chỉnh màu trang bìa và chưa có form nào để nộp.* **PDF xấu vẫn giao được quà. Form chưa có là MẤT LEAD.**
> ⚙️ Setup 1 lần (Vercel + trỏ Hermes vào Sheet, ~15') làm TRƯỚC buổi theo video hướng dẫn — không tính vào 110'.

### 🔴 Cụm A — FORM CHẠY THẬT (làm ĐẦU TIÊN) (⏱ template: 25' · lần đầu: 40')

**1.** [ ] Tạo Google Form (hoặc form trên trang Vercel): **6 trường** — Họ tên · SĐT · *"Zalo có phải số này không?"* · 🔴 **trường phân loại danh sách chọn** · Email (tuỳ ngành) · Ghi chú (5')
**2.** [ ] ⚙️ Kiểm **3 cài đặt sống còn:** TẮT thu thập email · TẮT giới hạn 1 phản hồi · TẮT yêu cầu đăng nhập Google — thiếu là khách thật không điền được (3')
**3.** [ ] Liên kết form → Google Sheet `[TênDN]-Leads`; thêm tay 4 cột: `Nguồn | Phân loại | Trạng thái | Người phụ trách` (7')
**4.** [ ] 🔒 **Data Security:** share Sheet **theo email cụ thể** (người trực + chủ DN), **KHÔNG** bật "ai có link cũng xem" (3')
**5.** [ ] 🔴 **TEST 2 LẦN:** ① tự điền **bằng ĐIỆN THOẠI** + trình duyệt ẩn danh → lead phải hiện trong Sheet · ② nhờ 1 người thân điền từ máy họ (7')

> 🔴 **Trường phân loại = câu đắt nhất form = mầm CRM Tuần 3.** Mỗi lựa chọn phải dẫn tới một hành động bán khác nhau. **🍵 MSX (chốt):** *"Bạn đang quan tâm điều gì nhất?"* → ① Khó ngủ, muốn thư giãn buổi tối · ② Tìm quà biếu bố mẹ · ③ Muốn dùng thử trước · ④ Đang so sánh với trà khác · ⑤ Hỏi mua sỉ – đại lý. **Chọn sai 5 lựa chọn = Tuần 3 làm lại từ đầu.**

### Cụm B — LẮP Landing copy 9 khối (không sáng tác) (⏱ template: 25' · lần đầu: 40')

**6.** [ ] Mở sẵn 4 file: 5 câu khách (N2) · FAQ DB (N4) · Core Offer (N3) · Product Knowledge (N4) (2')
**7.** [ ] Chạy **Prompt lắp landing** — **dán 4 thứ trên vào khối INPUT** (prompt không có chúng = copy bịa) → dán vào T12.2 → **điền cột `Mã nguồn` cho TỪNG khối** (23')

```
[VAI TRÒ] Bạn là copywriter StoryBrand cho SME Việt bán qua niềm tin.
[BỐI CẢNH] Tôi KHÔNG cần bạn sáng tác. Landing này là bản LẮP RÁP từ tài
sản có sẵn của tôi. Việc của bạn: XẾP đúng chỗ và mài chữ. Avatar ở mức
nhận thức {{Solution Aware}} → đánh SO SÁNH + BẰNG CHỨNG, không dạy nhập môn.
[NHIỆM VỤ] Lắp 9 khối theo thứ tự tâm lý (chú ý→đúng bệnh→muốn→tin→hành động):
1 Headline (kết quả+cho ai, ≤14 từ) · 2 Subheadline · 3 Vấn đề (DÙNG NGUYÊN
VĂN câu khách bên dưới, KHÔNG diễn giải) · 4 Lời hứa · 5 Nội dung nhận được
(5–7 gạch từ Product Knowledge) · 6 Khác biệt · 7 Bằng chứng (CHỈ dữ liệu
thật tôi cung cấp) · 8 CTA (từ Core Offer) · 9 FAQ (LẤY THẲNG 4–5 cặp bên dưới).
[DỮ LIỆU] 5 câu khách V#: {{dán N2}} · FAQ Q##: {{dán 5 cặp N4}} · Offer
OF#: {{dán N3}} · Product Knowledge PK: {{dán N4}} · Brand Voice: {{dán N9}}.
[ĐẦU RA] Bảng 9 dòng × cột: # | Khối | Nội dung | Mã nguồn.
[RÀNG BUỘC] Câu nào không truy về nguồn tôi đưa = bôi đỏ, ghi "AI bịa".
CẤM từ: chữa/khỏi/đặc trị/thần dược/cam kết 100%/khan hiếm giả. Tiếng Việt.
```

**8.** [ ] 🔴 **Duyệt truy nguyên:** khối 3 = lời khách `V#` nguyên văn (đọc thấy "văn AI" → thay) · khối 9 = `Q##` không viết mới · khối 7 = dữ liệu thật, không placeholder · khối 8 = `OF#` (5')
**9.** [ ] ⚖️ **Soát ranh giới:** Ctrl+F các từ *chữa · khỏi · đặc trị · thần dược · cam kết 100% · "chỉ còn X suất"* → xoá sạch. Lý do mua ngay phải THẬT (freeship đơn ≥500k) (5')

### Cụm C — Lead Magnet "Bảng so sánh 10 tiêu chí" (⏱ template: 40' · lần đầu: 60' — **timebox cứng: hết 40' là dừng, xuất bản cái đang có**)

**10.** [ ] Chốt quà bằng **T12.1** (4 tiêu chí A/B/C/D, tổng ≥16/20). **🍵 MSX chốt "Bảng so sánh 10 tiêu chí" = 20/20** — vì avatar Solution Aware đang SO SÁNH, cần bảng đối chiếu trung thực, không phải cẩm nang dạy nhập môn (đừng đổi thành "Cẩm nang 7 thói quen" — đó là quà #2) (5')

**11.** [ ] Chạy **Prompt viết ruột lead magnet** — dán Product Knowledge + Offer + objection thật vào INPUT → nhận nội dung bảng so sánh + phần dẫn (20'):

```
[VAI TRÒ] Bạn là chuyên gia nội dung viết lead magnet TRAO GIÁ TRỊ THẬT để khách tin trước khi mua — không phải quảng cáo trá hình.
[BỐI CẢNH] Quà "Bảng so sánh 10 tiêu chí chọn {{sản phẩm}} buổi tối". Avatar Solution Aware (đã biết giải pháp, đang SO SÁNH) → cần bảng so sánh TRUNG THỰC, không dạy nhập môn, không thổi phồng.
[NHIỆM VỤ] Viết ruột PDF 4–8 trang: (1) bìa: tiêu đề + 1 câu lợi ích; (2) 1 đoạn dẫn "vì sao cần bảng này" — MỞ bằng 1 câu khách nguyên văn V#; (3) BẢNG 10 TIÊU CHÍ so sánh "hàng trôi nổi vs {{thương hiệu}}", mỗi tiêu chí 1 dòng, cột trung thực (KHÔNG tự khen quá); (4) 3 dấu hiệu nhận biết hàng kém (từ Product Knowledge); (5) trang cuối: CTA về offer thật + Zalo/website.
[DỮ LIỆU] Product Knowledge PK: {{dán N4}}. Core Offer OF#: {{dán N3}}. 3 objection thật O#: {{dán N2}}. 1 câu khách V#: {{dán}}.
[RÀNG BUỘC] CHỈ dữ kiện THẬT trong Product Knowledge — chỗ tôi chưa cấp ghi "[THIẾU — chủ DN điền]", KHÔNG bịa số/chứng nhận. CẤM: chữa/khỏi/đặc trị/thần dược/100%. Chỉ "hỗ trợ thư giãn buổi tối". Tiếng Việt.
```

> 🍵 **Khung 10 tiêu chí MSX (mẫu để bắt chước — ngành khác thay bằng tiêu chí của mình):** ① Nguồn gốc vùng trồng (ghi cụ thể: 800–1.541m Mẫu Sơn) · ② Chứng nhận (OCOP 3★/kiểm nghiệm) · ③ Thành phần ghi rõ % hay mập mờ · ④ Có nhuộm màu/hương tổng hợp không · ⑤ Quy trình sao–sấy minh bạch không · ⑥ Hạn dùng & cách bảo quản · ⑦ Có cảnh báo đối tượng (thai/cho con bú/bệnh nền) không · ⑧ Giá quy về **mỗi tối** · ⑨ Có review khách thật không · ⑩ Chính sách đổi trả/freeship. → **Chính sự thẳng thắn (không tự khen quá) là thứ tạo niềm tin — đó là điểm khác biệt của quà so với 1 quảng cáo.**

**12.** [ ] 🟡 **Duyệt ASSISTED + đóng PDF (3 bước Canva):** (10')
  ① **Duyệt:** nhét ≥2 chi tiết chuyên môn THẬT AI không tự nghĩ ra (MSX: *người Dao/Tày/Nùng hái tay · OCOP 3★*); xoá mọi chỗ `[THIẾU]`/AI bịa.
  ② **Canva:** mở template *"comparison / checklist"* (hoặc khổ A4 dọc) → dán nội dung → **áp đúng 3 màu + font Brand Kit N10** (không chọn mới).
  ③ **Trang cuối:** chèn **CTA về offer thật (`OF#`)** + nút Zalo/website → Export **PDF 4–8 trang** `[TênDN]-leadmagnet-bangsosanh10tieuchi-v1.pdf`.

**13.** [ ] Upload PDF lên **Google Drive** → Share *Anyone with the link → Viewer* → copy link (gắn vào tin Zalo trao quà ở Cụm D) (bù vào timebox)

### Cụm D — TRAO QUÀ TỰ ĐỘNG (Hermes→Zalo) + Lead Flow Map (⏱ template: 20' · lần đầu: 25')

**14.** [ ] 🟢 **Nạp cho Hermes tin trao quà Zalo** (gửi <1' sau khi có lead) — đúng ranh giới, giọng Zalo ngắn (10'):

```
Chào chị {Tên} 👋 Cảm ơn chị đã quan tâm giấc ngủ của cả nhà.
Đây là Bảng so sánh 10 tiêu chí chị cần 👉 {link Drive}
Trong đó có 3 điều ít người bán chịu nói: dấu hiệu trà nhuộm hương, cách
đọc nguồn gốc vùng trồng, vì sao giá rẻ bất thường lại đáng ngại. [PK O1]
Chị cần tư vấn thêm cứ nhắn khung này, có người của Mẫu Sơn Xanh trả lời ạ 🌿
(Trà hỗ trợ thư giãn buổi tối, không thay thế thuốc; thai/cho con bú/bệnh
nền nên hỏi bác sĩ.)
```

> ⛑️ **Fallback nếu chưa nối được Hermes:** người trực (tên thật) gửi tay 3 tin — Thank You + gửi quà + tin 24h — trong ca trực. **Trao quà chạy thật (dù tay) thắng automation chưa chạy.**

**15.** [ ] 🔴 Kiểm **tin 24h**: KHÔNG mở đầu bằng chào bán ("bên em đang có chương trình…") → mở bằng giá trị/câu hỏi quan tâm. Ghi rõ **NGƯỜI THẬT gửi/duyệt — không auto blast** (3')
**16.** [ ] Điền **T12.4 Lead Flow Map**: 6 trạm, mỗi trạm `[Ai | Công cụ | Thời gian tối đa]` — **TÊN NGƯỜI THẬT**, không phải "nhân viên" (5')
**17.** [ ] 🔒 Thêm **dòng Data Security** + ghi 3 tầng: 🟢 AUTO (form→Sheet, Hermes gửi quà) · 🟡 ASSISTED (copy, ruột PDF, chuỗi nuôi dưỡng) · 🔴 NGƯỜI (bằng chứng, tin 24h, feedback) (2')

### Cụm E — Nghiệm thu luồng vàng + nộp (⏱ 5')

**18.** [ ] 🔴 **Chạy luồng vàng trên ĐIỆN THOẠI (4G):** bấm link → điền form thật → lead hiện trong Sheet kèm cột phân loại → **quà TỚI Zalo trong <2 phút**. Xoá lead test. Tự chấm mục 5 → nộp link trước 23h59.

> **⛑️ Luật cứu hộ:** làm theo thứ tự **A → B → C → D**. Nếu chỉ kịp 1 thứ: **NỘP FORM CHẠY THẬT + quà tới được Zalo.** Bonus không bắt buộc, không trừ điểm. Nộp 80% đúng hạn thắng 100% trễ 2 ngày.

---

## 4. 📤 Nộp bài

| # | Tên file | Yêu cầu nghiệm thu |
|:-:|---|---|
| 1 | `[Tên DN] — Ngày 12 — Link Phễu Trao Quà` | 🔴 **Mentor BẤM LINK trên điện thoại, ĐIỀN THỬ → quà phải TỚI ZALO <2'.** Kèm ảnh Sheet ≥2 dòng test — **che 4 số cuối SĐT** (`09xx xxx 123`) |
| 2 | `[Tên DN] — Ngày 12 — Landing Page Copy` | T12.2 — đủ **9/9 khối** + cột `Mã nguồn`. Khối 3 = `V#`, khối 9 = `Q##`, khối 8 = `OF#` |
| 3 | `[Tên DN] — Ngày 12 — Lead Magnet` | PDF **4–8 trang** = "Bảng so sánh 10 tiêu chí" — trang cuối có CTA offer thật |
| 4 | `[Tên DN] — Ngày 12 — Lead Flow Map` | T12.4 — 6 trạm, tên người thật, dòng Data Security, 3 tầng AUTO/ASSISTED/NGƯỜI |
| 5 | *(Bonus)* | Link Vercel đã dựng + ảnh chuỗi nuôi dưỡng 10 tin đã duyệt |

- **Nơi nộp:** thread cohort Ngày 12 · **Deadline: 23h59 cùng ngày.**
- 🔴 **Cảnh báo:** ai nộp ảnh Sheet còn nguyên SĐT khách/người thân → gỡ ngay + trừ điểm (vi phạm Data Security N4).

---

## 5. 🔍 Tự chấm nhanh (trước khi nộp — theo rubric giáo án)

| # | Tiêu chí | Đạt? |
|---|----------|:---:|
| 1 | Form **6 trường**, có **trường phân loại danh sách chọn**, đã test điền trên điện thoại → hiện trong Sheet? |  |
| 2 | Landing đủ **9 khối**, **≥8/9 có mã nguồn hợp lệ**? Kiểm bằng Ctrl+F: khối nào cột Mã nguồn trống = chưa đạt |  |
| 3 | 🔴 **Khối 3 = `V#` nguyên văn · Khối 9 = `Q##` lấy thẳng · Khối 8 = `OF#`** (3 khối này bắt buộc 100%)? |  |
| 4 | Lead magnet trang cuối **CÓ CTA về offer thật** + ≥2 chi tiết chuyên môn AI không tự nghĩ ra? |  |
| 5 | 🔴 **Luồng vàng chạy:** bấm link → form → Sheet → **quà tới Zalo <2'** (hoặc fallback người gửi tay có tên)? |  |
| 6 | Lead Flow Map đủ **6 trạm có TÊN NGƯỜI** + **dòng Data Security** (lead = Restricted)? |  |
| 7 | ⚖️ Ctrl+F **không còn** từ *chữa/khỏi/đặc trị/thần dược/cam kết 100%/khan hiếm giả*? |  |

**Bổ sung 3 tiêu chí Tuần 2 (chấm ở mọi ngày):**
- **Truy nguyên:** ≥80% khối landing có mã nguồn; ≥30% truy về `V#`/`Q##`.
- **Ranh giới pháp lý:** 1 tuyên bố vượt ranh giới = **−7đ + không được đăng**.
- **Nhất quán nhận diện:** copy + tin Zalo đúng cá tính + giọng của **T8.0** (N8).

> Đủ 7/7 → thường ⭐ (≥80đ). Thiếu tiêu chí 5 (luồng vàng) = mất điều kiện qua ngày — Tuần 3 (CRM/sale) không có gì để chạy.

---

## 6. ⚠️ Lỗi thường gặp

| ❌ Lỗi | Hậu quả | ✅ Cách sửa |
|--------|---------|------------|
| Làm PDF đẹp trước, form để sau | 23h chưa có form nào để nộp → mất lead | Thứ tự A→C là bắt buộc: Form (25') TRƯỚC, PDF (40') SAU |
| Form bật "yêu cầu đăng nhập Google" / "giới hạn 1 phản hồi" | Khách thật không điền được, không ai biết | Tắt cả 3 cài đặt sống còn; test bằng điện thoại + trình duyệt ẩn danh |
| Khối 3 (Vấn đề) viết bằng lời AI ("Bạn đang mệt mỏi vì…") | Content "nghe tây", không chạm | Dán **nguyên văn `V3`**: *"Sao đắt hơn trà ngoài siêu thị thế em?"* |
| Khối 9 tự chế FAQ mới | Bỏ phí ≥30 câu hỏi thật đã có ở N4 | Copy thẳng 4–5 cặp từ FAQ Database `Q##` |
| Trường phân loại là ô tự luận | Tuần 3 không lọc tệp được → CRM vỡ | Phải là **danh sách chọn** 5 lựa chọn, mỗi lựa chọn = 1 hành động bán |
| Hermes nhắn Zalo tin chưa duyệt / có từ cấm | Phá niềm tin 5.000 khách + rủi ro pháp lý | Trao quà = AUTO được; **chuỗi nuôi dưỡng phải người duyệt cả 10 tin mới bật** |
| Đăng ảnh Sheet còn SĐT khách lên group để khoe | Vi phạm Data Security, trừ điểm | Che 4 số cuối; không đưa SĐT vào prompt AI công cộng |

---

## 7. 🔗 Kết nối

- **Form + trường phân loại** → mầm CRM Tuần 3: 5 lựa chọn hôm nay là câu định tuyến lead vào luồng chăm sóc.
- **Landing copy 9 khối** → nếu không lắp được từ Tuần 1 nghĩa là Tuần 1 rỗng — đi vá N2/N3/N4 trước.
- **Luồng vàng (form→Hermes→Zalo)** → chính là **Marketing Gate câu 3** (Ngày 14) — điều kiện thật vào Tuần 3.
- **Lead Flow Map + 3 tầng tự động hoá** → đầu vào trực tiếp cho **Automation Layer Ngày 13**; chuỗi nuôi dưỡng Zalo = tầng 🟡 ASSISTED.
- Giáo án: [[Ngày 12 — Landing Page & Lead Magnet]] · Module: [[Module — Phễu Quà Tặng Tự Động (Vercel + Hermes-Zalo)]] · Chuẩn: [[_Chuẩn Đồng Bộ Tuần 2]] · Tiếp: [[Ngày 13 — Phân Phối Nội Dung & Content Automation]]
