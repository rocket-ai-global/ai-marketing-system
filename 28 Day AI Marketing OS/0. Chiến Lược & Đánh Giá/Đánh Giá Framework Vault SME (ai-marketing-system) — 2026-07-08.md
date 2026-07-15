---
up:
  - "[[_MOC 28 Day AIOS]]"
created: 2026-07-08
tags: [project, aios, audit, framework]
---

# 🔍 Đánh Giá Framework Vault SME (`ai-marketing-system/`)

> Đánh giá framework hệ thống mẫu học viên **cài về chạy luôn** — vault Obsidian PARA + AI Brain cho 1 doanh nghiệp SME, kèm 16 skill tiếng Việt, thiết kế để agent (Hermes, Claude Code) đọc hiểu ngay. Đối chiếu với lời hứa của [[_MOC 28 Day AIOS]] và giáo án 28 ngày. Ánh xạ chi tiết từng ngày: [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]].

---

## 1. Định vị đúng của framework trong AIOS — kiến trúc 2 lớp

Vault SME **không phải toàn bộ AIOS** — nó là **lớp NÃO (AI Brain + bộ nhớ + đo lường)**. Phải dạy học viên phân biệt rõ ngay Ngày 0:

```
LỚP 1 — NÃO (Vault SME, cài về máy/repo)          LỚP 2 — ĐỘNG CƠ (RocketAgent/Hermes, chạy 24/7)
├─ 00. Business Context = nguồn sự thật            ├─ Chatbot tư vấn (Ngày 16)
├─ PARA: content, pipeline, đo lường 6 miền        ├─ Automation workflow (Ngày 20, 22)
├─ Entity: People/Companies/Meetings/Decisions     ├─ 5 AI Agent vận hành (Ngày 26)
└─ 16 skill phỏng vấn & phân tích                  └─ Landing/lead capture (Ngày 12)
            └────────── Agent Hermes ĐỌC vault để hành động; kết quả GHI ngược về vault ──────────┘
```

Giá trị lớn nhất: **mọi engine đều đọc chung một nguồn sự thật** — đúng tư duy "hệ điều hành", không phải bộ công cụ rời rạc.

## 2. Điểm mạnh (framework đạt chuẩn "cài về chạy luôn" cho lớp não)

| #   | Điểm mạnh                                                                                                                                                | Vì sao đáng giá cho chương trình                                                                                                    |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| 1   | **`00. Business Context/` = single source of truth** với convention đặt tên chuẩn, agent dò bằng quy ước không cần hỏi                                   | Chính là "Knowledge Base" của Ngày 04 — nhưng ở dạng sống, agent đọc trực tiếp                                                      |
| 2   | **Skill phỏng vấn tiếng Việt** (`/mo-hinh-kinh-doanh` 9 khối BMC, `/hoan-tat-business-context` audit thiếu gì hỏi nấy)                                   | Chủ DN không cần biết prompt — "custom hoá bằng phỏng vấn" là đúng mô hình chuyển giao; khớp luôn Tuần 1 bản BMC-first anh vừa chốt |
| 3   | **Vòng khép kín content → đo lường 6 miền** (tương tác / traffic / ads / hiệu suất content theo pillar-format-hook / CSKH chat) + báo cáo theo thời gian | Vượt chuẩn giáo án Ngày 23-24 — dạy thẳng trên cấu trúc này, khỏi dựng sheet mới                                                    |
| 4   | **Nhật Ký CEO tách khỏi Daily** — nguyên liệu content "có hồn", có quy tắc riêng tư `rieng_tu`                                                           | Trả lời đúng nỗi sợ lớn nhất của học viên: "AI viết content vô hồn"                                                                 |
| 5   | **Đã localize SME VN**: event Zalo/Messenger/phone click, Nghị định 13/2023, GTM no-code, cảnh báo A/B khi traffic thấp                                  | Tránh được lỗi phổ biến: dạy tool Tây cho DN Việt                                                                                   |
| 6   | **Quy tắc chống loạn vault**: 1 công ty duy nhất, không note mồ côi, archive không xoá, cấm ghi đè identity âm thầm                                      | Đây là SOP vận hành ngầm — học viên dùng sai vẫn được hệ thống "đỡ"                                                                 |
| 7   | Có **test case An Nhiên Spa** (Archive) + ví dụ Spa Thảo Mộc xuyên suốt README + case MSX/Mẫu Sơn Xanh                                                                           | Spa giữ làm bài test/ngách gốc; MSX là demo sống để bán và làm chuẩn chấm bài                                                                  |

## 3. Độ phủ so với giáo án 28 ngày

| Tuần | Độ phủ | Có sẵn trong vault | Thiếu (phải build hoặc thuộc lớp Hermes) |
|---|---|---|---|
| **1 — Foundation** | ~80% 🟢 | BMC + PK/GT (skill), Chân Dung DN/CEO, Brand Voice, offer (`/thiet-ke-offer`), AI-Sale-Assistant, CLAUDE.md = AI instruction | **Prompt Library** (Ngày 5) chưa có chỗ đứng · file **Baseline & Mục Tiêu 28 Ngày** (Ngày 0) chưa có |
| **2 — Marketing** | ~55% 🟡 | Content Đã Đăng (1 file/post + frontmatter pillar/format/hook), Content Calendar MOC, Brand Voice, `/kiem-tra-seo`, `/do-luong-tracking`, `/nghien-cuu-video-youtube` | Content Pillar/Strategy template (Ngày 8) · khung bài viết 7 dạng (Ngày 9) · visual/video factory (Ngày 10-11 — tool ngoài) · **landing page + lead magnet** (Ngày 12 — lớp Hermes/web) |
| **3 — Sales** | ~45% 🟡 | People/Companies/Meetings (mẫu sale call), Pipeline area + MOC, Decisions (mẫu quyết định giá), playbook Xử Lý Từ Chối Giá, mẫu Email Follow-up Sau Demo, `.base` dashboard (skill `obsidian-bases`) | **Chatbot** (Ngày 16 — lớp Hermes) · **Lead Scoring model** (Ngày 17) · Sales Script 10 bước đầy đủ (Ngày 18 — mới có 1 playbook) · Proposal/Báo giá (Ngày 19) · **Follow-up Sequence 14 ngày** (Ngày 20) |
| **4 — OS** | ~55% 🟡 | Analytics 6 miền + Báo Cáo Ngày/Tuần/Quý (Ngày 23-24 gần như xong), `/thu-nghiem-ab`, Customer Success area, Feedback & Chứng Thực (case study — Ngày 25, 28), `json-canvas` cho OS Map (Ngày 27) | **Automation workflow** (Ngày 22 — lớp Hermes) · **5 AI Agent + instruction pack** (Ngày 26 — lớp Hermes, tham chiếu `AI-Sale-Assistant.md`) · SOP Operating Pack (Ngày 27) · 90-Day Plan template (Ngày 28) |

**Kết luận độ phủ:** lớp não đạt ~60-65% toàn chương trình và gần đủ cho Tuần 1. Phần thiếu chia 2 loại: (a) **module vault bổ sung được ngay** (danh sách mục 4), (b) **thuộc lớp Hermes/RocketAgent** — không phải lỗi của vault, nhưng giáo án phải nói rõ "hôm nay làm ở lớp nào" (đã xử lý bằng dòng 🗂️ trong từng giáo án + [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]]).

## 4. Việc phải làm để framework khớp 100% lời hứa (ưu tiên)

1. 🔴 **Ngày 0 Install Pack** — rủi ro số 1 là learning curve: chủ spa phải cài Obsidian + Claude Code + clone vault + hiểu skill. Giải: video cài đặt 20' + mentor cài cùng buổi Ngày 0 + (gói Installed) Rocket cài sẵn giao máy chạy. Thêm file `00. Business Context/Baseline & Mục Tiêu 28 Ngày.md` vào vault gốc.
2. 🔴 **Bổ sung 6 module vault còn thiếu** (build 1 lần, mọi cohort dùng): `04. Resources/Prompt Library/` (Ngày 5) · template Content Strategy/Pillar (Ngày 8) · Lead Scoring sheet (Ngày 17) · Sales Script khung 10 bước + Proposal/Báo giá (Ngày 18-19) · Follow-up Sequence 14 ngày (Ngày 20) · SOP Operating Pack + 90-Day Plan (Ngày 27-28). → cập nhật trạng thái trong [[Danh Mục Template Chuyển Giao]].
3. 🔴 **Chốt chuẩn CRM cho Ngày 15**: mặc định dạy CRM notes-based của vault (People/Companies + Pipeline + `.base` dashboard) — đủ cho SME ≤200 lead/tháng; DN lớn hơn chuyển CRM trên RocketAgent. Giáo án phải dạy MỘT đường chính, không dạy 2 đường song song.
4. 🟠 **Cầu nối Hermes chính thức**: mỗi agent lớp 2 (chatbot, follow-up, 5 agent Ngày 26) phải có spec "đọc file nào trong vault, ghi kết quả về đâu" — mở rộng `AI-Sale-Assistant.md` thành hợp đồng giữa 2 lớp.
5. 🟠 **Đóng đủ vault demo MSX Group — Mẫu Sơn Xanh** (giữ An Nhiên Spa/Spa Thảo Mộc làm bài test riêng) — để demo live mỗi buổi và làm chuẩn so sánh khi chấm bài.
6. 🟡 Branding: đổi tên thư mục `ai-marketing-system` → tên bàn giao chính thức (VD `aios-vault-sme`) trước cohort đầu, tránh lẫn với engine.

## 5. Tác động lên nội dung giảng (đã điều chỉnh)

- **Mỗi giáo án** giờ có dòng `🗂️ Trong Vault SME` ngay đầu bài: hôm nay thao tác ở thư mục/skill nào của vault, phần nào làm trên Hermes — trainer và học viên không phải tự suy.
- **Ngày 1-4 đổi trọng tâm demo**: thay vì "AI sinh tài liệu rồi điền template", demo chuẩn là **chạy `/mo-hinh-kinh-doanh` + `/hoan-tat-business-context` ngay trong vault** — tài liệu tự sinh đúng chỗ. Prompt mẫu trong giáo án trở thành phương án B (cho học viên chưa cài xong).
- **Ngày 6 định nghĩa lại "AI Business Brain"**: không phải dựng bot mới — mà là *vault đã điền + CLAUDE.md + AI-Sale-Assistant.md*, nghiệm thu bằng cách hỏi agent 10 câu về DN và agent trả lời đúng từ vault.
- **Ngày 23-24 dạy thẳng trên cấu trúc Analytics 6 miền** của vault (copy file `[Mẫu]`, bỏ tiền tố, đổi kỳ) thay vì dựng dashboard mới.
- Chi tiết từng ngày: [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]].

## 🔗 Kết nối với

- [[_MOC 28 Day AIOS]] · [[Đánh Giá Hiệu Quả Chương Trình — 2026-07-08]] (lỗ hổng #3 — framework này chính là lời giải)
- [[Bản Đồ Vault SME ↔ Giáo Án 28 Ngày]] · [[Danh Mục Template Chuyển Giao]] · [[_Blueprint Chuẩn — Cấu Trúc Giáo Án]]
