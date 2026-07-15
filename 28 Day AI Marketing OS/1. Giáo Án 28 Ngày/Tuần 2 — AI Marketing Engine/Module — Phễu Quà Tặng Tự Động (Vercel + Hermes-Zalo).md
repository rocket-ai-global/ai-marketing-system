---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-15
updated: 2026-07-15
tags: [project, aios, giao-an, module, funnel, tu-dong-hoa, hermes, zalo]
week: 2
plugs-into: [12, 13]
engine: "Hermes/RocketAgent (đã onboard Tuần 1) + Zalo OA — KHÔNG thêm công cụ mới"
core-output: "Phễu quà tặng tự động CHẠY THẬT: Landing page (Vercel, subdomain free) → form → Google Sheet (mầm CRM Tuần 3, tái dùng của Ngày 12) → HERMES theo dõi Sheet 24/7 → khách vừa điền là NHẬN QUÀ TỰ ĐỘNG qua ZALO trong <1 phút (link lead magnet + lời chào) → chuỗi nuôi dưỡng qua Zalo ĐÃ ĐƯỢC NGƯỜI DUYỆT (tầng ASSISTED). Nghiệm thu bằng hành động: mentor bấm link thật trên điện thoại, điền form, và QUÀ PHẢI TỚI ZALO."
---

# 🎁 Module — Phễu Quà Tặng Tự Động (Vercel + Hermes/Zalo)

> **Bản tối ưu của [[GIAO-TRINH-nha-may-pheu-CHUYEN-GIAO|"Nhà máy phễu"]] — dựng trên đúng thứ học viên ĐÃ CÓ.** Bản gốc đòi Cloudflare Worker + `wrangler` + lark-cli + SMTP + cron + mua domain, **chỉ vì máy cá nhân không luôn-bật**. Nhưng học viên đã có **Hermes chạy 24/7 từ Tuần 1** → bài toán "always-on" GIẢI SẴN. Và khách MSX **sống trên Zalo, không phải email** → trao quà qua Zalo thắng email.
>
> → **Không thêm công cụ mới nào.** Chỉ ghép: Vercel (trang đẹp) + Google Sheet (đã có N12) + Hermes/Zalo (đã có Tuần 1).

> 🔌 **Cắm vào đâu:** nâng cấp "trao quà" của **[[Ngày 12 — Landing Page & Lead Magnet|Ngày 12]]** (từ *gửi tay 3 tin nhắn* → *Hermes tự nhắn Zalo*) và "nuôi dưỡng" của **[[Ngày 13 — Phân Phối Nội Dung & Content Automation|Ngày 13]]** (chuỗi Zalo = tầng 🟡 ASSISTED của Automation Layer). KHÔNG thêm ngày — vẫn 14 ngày.

> 🎯 **Vì sao là Core bắt buộc:** đây là khoảnh khắc học viên **NHÌN THẤY hệ thống tự chạy** — khách điền form lúc 23h, Hermes nhắn quà qua Zalo ngay khi không ai trực. Chính là **luồng vàng** ([[_Chuẩn Đồng Bộ Tuần 2|Marketing Gate câu 3]]) và lời giải trực tiếp cho điểm nghẽn #1 của MSX: *inbox chậm ~3h, đêm không ai trực*.

---

## 0. Bức tranh — 4 mảnh, 0 công cụ mới

```
[KHÁCH lướt FB 21h] ── bấm CTA trên bài ──►┐
                                            ▼
┌────────────────────────────────────────────────────────────┐
│ 1) LANDING PAGE  (Vercel · *.vercel.app free · AI generate) │
│    form: Tên · SĐT/Zalo · "bạn đang cần gì?" (phân loại)     │
└───────────────────────────┬────────────────────────────────┘
                            │ ghi vào
                            ▼
┌────────────────────────────────────────────────────────────┐
│ 2) GOOGLE SHEET  "MSX — Leads"  (TÁI DÙNG của Ngày 12)      │
│    có trường phân loại = MẦM CRM Tuần 3                      │
└───────────────────────────┬────────────────────────────────┘
                            │ Hermes theo dõi 24/7
                            ▼
┌────────────────────────────────────────────────────────────┐
│ 3) HERMES / RocketAgent  (ĐÃ onboard Tuần 1, chạy 24/7)     │
│    thấy lead mới → nhắn ZALO:                                │
│      • Trao quà NGAY (<1'): link PDF + lời chào              │
│      • Chuỗi nuôi dưỡng D1…D10 qua Zalo (ĐÃ người duyệt)     │
│      • Ghi trạng thái ngược vào Sheet (đã gửi / đã đọc)      │
└───────────────────────────┬────────────────────────────────┘
                            │ link tải
                            ▼
┌────────────────────────────────────────────────────────────┐
│ 4) QUÀ = LEAD MAGNET PDF  (Google Drive · link công khai)   │
└────────────────────────────────────────────────────────────┘
```

| Mảnh | Vai trò | Học viên đã có? | Chi phí |
|---|---|:---:|:---:|
| **Vercel** | Trang công khai đẹp, subdomain `*.vercel.app` | Cài 1 lần (video) | 0đ |
| **Google Sheet** | Sổ lead + trường phân loại → CRM Tuần 3 | ✅ từ Ngày 12 | 0đ |
| **Hermes/RocketAgent** | Engine 24/7: đọc Sheet → nhắn Zalo quà + nuôi dưỡng | ✅ từ Tuần 1 | 0đ (đã có) |
| **Zalo OA** | Kênh trao quà & nuôi dưỡng (khách MSX sống ở đây) | ✅ từ Tuần 1 | 0đ |
| **Google Drive** | Host PDF quà | ✅ | 0đ |

> 💡 **Đường siêu tắt (bỏ cả Vercel):** không muốn dựng trang → dùng thẳng **Google Form của Ngày 12** làm nơi nhận lead. Hermes vẫn đọc cùng Sheet đó và nhắn Zalo y hệt. Ai muốn trang đẹp thì thêm Vercel; ai bí thì Google Form vẫn ra phễu chạy thật. **Khâu tự động (Hermes→Zalo) không đổi.**

---

## 1. ⏱ Chính sách thời gian (2 số, trung thực)

| Phần | Bản dựng sẵn | Lần đầu tự làm | Ghi chú |
|---|:---:|:---:|---|
| Setup 1 lần (Vercel + trỏ Hermes vào Sheet) | 20' | 40' | 🔴 Xem video "Setup Vercel + nối Hermes vào Sheet 15'" TRƯỚC |
| Mỗi chiến dịch (dựng phễu MSX) | 55' | 100' | Quà (PDF) làm xong ở Ngày 12 rồi mới vào đây |
| **Tổng lần đầu** | **75'** | **140'** | |

> **Luật cứu hộ:** *Phễu Core = form → Hermes nhắn quà Zalo TỚI.* Chỉ chừng đó là ĐẠT. Chuỗi 10 tin nuôi dưỡng là **Bonus** — thiếu không trừ điểm. **Nộp phễu trao quà chạy thật thắng phễu có 10 tin nhưng form chưa chạy.**

---

## 2. 🔴 Luật nhốt tự động hoá (đọc trước khi bật)

> **Tự động hoá VIỆC, không tự động hoá NIỀM TIN.** — MSX bán bằng niềm tin vào nguồn gốc. 1 tin Hermes nhắn bịa ("chữa mất ngủ" / case khách không thật) tự gửi cho 500 người = phá 5.000 khách đã có.

| Việc | Tầng | Ai chịu trách nhiệm |
|---|:---:|---|
| Trao quà ngay sau form (Hermes nhắn Zalo link PDF) | 🟢 **AUTO** | Máy — **ruột PDF do người duyệt** |
| Đọc Sheet, ghi trạng thái, đo đã đọc | 🟢 **AUTO** | Máy |
| **Chuỗi 10 tin nuôi dưỡng Zalo** | 🟡 **ASSISTED** | **AI viết → NGƯỜI DUYỆT CẢ 10 → mới nạp cho Hermes gửi.** Chưa duyệt = chưa bật |
| Chất liệu thật trong tin (chuyện khách, số thật, ảnh vùng nguyên liệu) | 🔴 **NGƯỜI** | Chỉ người |
| Khách bấm reply Zalo hỏi lại | 🔴 **NGƯỜI** (hoặc agent CSKH có người giám sát) | Chỉ người/giám sát |

> ⚖️ **Ranh giới pháp lý — chấm ở MỌI tin:** chỉ *"hỗ trợ thư giãn buổi tối"*. **CẤM:** chữa · khỏi · đặc trị · thần dược · cam kết 100% · khan hiếm giả. 1 tin vượt ranh giới = **−7đ và gỡ khỏi chuỗi ngay**. Thai/cho con bú/trẻ em/bệnh nền → khuyên hỏi bác sĩ.
> 📵 **Luật Zalo OA:** chỉ nhắn trong cửa sổ tương tác (khách vừa để lại SĐT = đã mở cửa sổ). Nhịp nuôi dưỡng theo đúng chính sách Zalo OA — Hermes đã cấu hình từ Tuần 1.

---

## 3. 🔧 SETUP 1 LẦN (tái dùng cho mọi chiến dịch)

> Xem video **"Setup Vercel + nối Hermes vào Sheet 15'"** song song. Toàn bộ là thao tác chuột.

1. **Vercel** — `vercel.com` → Sign up bằng GitHub (chưa có GitHub thì tạo, 2') → xong. *Nơi trang sống công khai.*
2. **Google Sheet "MSX — Leads"** — đã dựng ở **Ngày 12** với trường phân loại 5 lựa chọn cứng. **Không dựng lại.** Nếu chưa có, quay lại N12 làm form Google → Sheet trước.
3. **Nối Hermes vào Sheet** — bật skill/tác vụ Hermes *"theo dõi Sheet MSX-Leads → khi có dòng mới, nhắn Zalo theo kịch bản"* (Rocket đóng gói sẵn; dán ID Sheet + Zalo OA đã kết nối Tuần 1). *Đây là phần Rocket cấu hình/đóng gói — học viên chỉ trỏ đúng Sheet.*
4. **Google Drive** — sẵn sàng host PDF quà.

> **Kết quả:** Hermes đã "canh" đúng Sheet. Từ giờ mỗi chiến dịch chỉ tạo mới nội dung (quà + trang + kịch bản tin), không dựng lại đường ống.

---

## 4. 📦 MỖI CHIẾN DỊCH — 5 bước (bản mẫu MSX điền sẵn)

### Bước 1 — QUÀ (lead magnet) — *đã làm ở Ngày 12* (5')
- Quà MSX = **"Bảng so sánh trung thực 10 tiêu chí: chọn trà thảo mộc buổi tối"** (PDF, chốt ở N12 — 20/20 điểm).
  > 🔴 **Chốt tên quà 1 lần cho cả N12/N13/N14** = *"Bảng so sánh 10 tiêu chí"*. Đừng gọi thành "Cẩm nang 7 thói quen" — đó là quà #2 (Bonus).
- Upload PDF lên **Google Drive** → Share → *Anyone with the link → Viewer* → copy link (gắn vào tin Zalo trao quà).

### Bước 2 — Landing trên Vercel + form ghi vào Sheet (15')
1. Trong **AI Marketing Assistant (N6)** chạy prompt M09 cá nhân hoá: *"Xuất file `index.html` landing 9 khối cho quà [Bảng so sánh 10 tiêu chí], case MSX, dùng đúng 5 câu khách `V#`, FAQ từ `Q##`. Form 3 trường: Tên · SĐT/Zalo · phân loại (5 lựa chọn N12). Form submit ghi vào Google Sheet MSX-Leads."*
2. Cách nối form → Sheet (chọn 1, cả hai không cần code lạ):
   - **Dễ nhất:** nhúng thẳng **Google Form của Ngày 12** vào trang (iframe) → tự ghi Sheet.
   - **Đẹp hơn:** form gốc trên trang → POST vào 1 **Google Apps Script Web App** (đoạn dán sẵn Rocket cấp) → append Sheet.
3. Deploy: **github.com → New repo (Public) → Upload `index.html`** → **vercel.com → Import → Deploy**. ~30s có `https://msx-tra-toi.vercel.app`.
4. Mở link trên **điện thoại** → thấy trang + form.
> Bí quá → bỏ Bước này, dùng thẳng Google Form N12 (đường siêu tắt mục 0).

### Bước 3 — Kịch bản Hermes TRAO QUÀ qua Zalo (🟢 AUTO) (10')
Nạp cho Hermes tin trao quà (mẫu MSX, đúng ranh giới, giọng Zalo ngắn gọn):

> **Tin Zalo tự động (gửi <1' sau khi có lead):**
> Chào chị {Tên} 👋 Cảm ơn chị đã quan tâm giấc ngủ của cả nhà.
> Đây là **Bảng so sánh 10 tiêu chí** chị cần 👉 {link Drive}
> Trong đó có 3 điều ít người bán chịu nói: dấu hiệu trà nhuộm hương, cách đọc nguồn gốc vùng trồng, và vì sao giá rẻ bất thường lại đáng ngại. `PK O1`
> Chị cần tư vấn thêm cứ nhắn ngay khung này, có người của Mẫu Sơn Xanh trả lời ạ 🌿
> *(Trà Mẫu Sơn Xanh hỗ trợ thư giãn buổi tối, không thay thế thuốc; thai/cho con bú/bệnh nền nên hỏi bác sĩ.)*

→ Hermes gửi tự động, kể cả 2h sáng. Ghi trạng thái *"Đã gửi quà"* ngược vào Sheet.

### Bước 4 — Chuỗi NUÔI DƯỠNG Zalo (🟡 ASSISTED — người duyệt trước) (10' + duyệt)
1. AI viết **10 tin D1–D10** (bám Journey ⚡ J2/J6 + xử objection `O#`), ví dụ nhịp:
   D1 chuyện vùng nguyên liệu 1.541m `PK` → D3 xử "sao đắt hơn trà chợ" `O1 V3` → D5 bằng chứng khách cũ `V#` → D7 combo 1.015.000đ `OF#` → D10 lời mời cuối.
2. 🔴 **DUYỆT CẢ 10 trước khi nạp cho Hermes:** đọc từng tin, quét từ cấm (chữa/khỏi/100%), bỏ câu AI bịa. **Chưa duyệt xong = chưa bật.**
3. Nạp vào Hermes + đặt nhịp (vd cách 1–2 ngày, trong cửa sổ Zalo OA); bật **dừng chuỗi khi khách đã mua/đã trả lời**.

### Bước 5 — Sheet = mầm CRM Tuần 3 + Data Security (5')
- Cột **phân loại** (①–⑤) đã nằm trong Sheet → đúng trường Ngày 12 yêu cầu, sang Tuần 3 lọc thẳng thành tệp bán.
- 1 dòng **Data Security** (N4): *Tên + SĐT/Zalo lead = tầng Restricted — chỉ {tên người} xem; lưu ở Sheet + Hermes nội bộ, không đăng công khai.* `DS`

---

## 5. 📋 PHIẾU ĐẦU BÀI (điền rồi đưa AI) — bản mẫu MSX

```
[QUÀ]        Bảng so sánh 10 tiêu chí chọn trà tối | link Drive: drive.google.com/…
[SẢN PHẨM]   Trà Mẩy Gòm An Giấc (cửa vào 359k) → đẩy Combo 3 tặng 1 = 1.015.000đ | mausonxanh.com
[ĐỐI TƯỢNG]  chị Hương 40t, NV văn phòng HN, ~20tr/th, "giữ sức khoẻ cả nhà", Solution Aware
[MÃ NGUỒN]   V3 "sao đắt hơn trà ngoài siêu thị thế em" | O1 đắt/O2 sợ nhuộm hương | Q##…
[SHEET]      MSX — Leads (đã dựng N12) | trường phân loại ①–⑤
[TRANG]      Vercel: msx-tra-toi.vercel.app  (hoặc: dùng Google Form N12)
[ENGINE]     Hermes (đã onboard T1) theo dõi Sheet → nhắn Zalo OA 0822.928.988
[NUÔI DƯỠNG] 10 tin Zalo | nhịp 2 ngày | ĐÃ người duyệt: rồi
[RANH GIỚI]  cấm chữa/khỏi/đặc trị/100% | disclaimer: "hỗ trợ thư giãn buổi tối, không thay thuốc"
```

---

## 6. ✅ NGHIỆM THU BẰNG HÀNH ĐỘNG (luồng vàng Gate câu 3)

> Mentor **tự tay** làm trên **điện thoại (4G)**, không đọc bản nộp.

- [ ] Mở link trang → form bấm được.
- [ ] Điền form thật (tên + Zalo/SĐT mentor + chọn 1 phân loại) → thấy lời cảm ơn.
- [ ] Lead **hiện trong Google Sheet** kèm đúng cột phân loại.
- [ ] **QUÀ TỚI ZALO mentor trong <2 phút** — tin có link tải PDF mở được. ⭐ *Câu tử — quà không tới = phễu chưa chạy = không đạt.*
- [ ] (Bonus) Chuỗi nuôi dưỡng: mở kịch bản Hermes → thấy 10 tin **đã duyệt** (không còn từ cấm), nhịp đã đặt.
- [ ] Xoá lead test sau nghiệm thu.

---

## 7. 🔁 TÁI DÙNG & SỰ CỐ

**Tái dùng:** Vercel/GitHub, Sheet + trường phân loại, Hermes trỏ Sheet, Zalo OA, Drive.
**Làm mới mỗi chiến dịch:** quà PDF → trang Vercel → tin trao quà → (tùy) chuỗi nuôi dưỡng.

| Hiện tượng | Xử lý |
|---|---|
| Quà không tới Zalo | Hermes chưa trỏ đúng Sheet · hoặc Zalo OA ngoài cửa sổ tương tác · kiểm log Hermes |
| Lead không vào Sheet | Form chưa nối Sheet (kiểm iframe Google Form / endpoint Apps Script) |
| Cột phân loại rỗng | Form thiếu trường phân loại · map sai cột |
| Trang Vercel lỗi | Repo phải Public · file tên `index.html` · Deploy lại |
| Tin nuôi dưỡng bị Zalo chặn | Vượt chính sách OA/ngoài cửa sổ → giãn nhịp, đúng template OA |

---

## 8. Bảng phân vai

| Việc | AI | Người | Hermes |
|---|:---:|:---:|:---:|
| Viết ruột PDF, copy landing 9 khối, 10 tin nuôi dưỡng | ✔ | | |
| Xuất `index.html`, nối form→Sheet | ✔ | | |
| Tạo Vercel/GitHub, Deploy, upload | | ✔ | |
| **DUYỆT 10 tin trước khi bật** (nhốt niềm tin) | | ✔ 🔴 | |
| Theo dõi Sheet → nhắn Zalo quà + nuôi dưỡng 24/7 | | | ✔ |
| Nghiệm thu bằng hành động | | ✔ | |

---

## 🔗 Kết nối với

- [[Ngày 12 — Landing Page & Lead Magnet]] · [[Ngày 13 — Phân Phối Nội Dung & Content Automation]] · [[Ngày 14 — Marketing Engine Review & Demo Day 2]]
- [[_Chuẩn Đồng Bộ Tuần 2]] (mục 6 Luật tự động hoá · mục 10 Marketing Gate câu 3)
- [[Ngày 06 — AI Business Brain]] (Hermes/RocketAgent onboard) · [[GIAO-TRINH-nha-may-pheu-CHUYEN-GIAO]] (bản gốc Cloudflare — tham chiếu)
- [[_MOC 28 Day AIOS]]
