---
name: nghien-cuu-thi-truong
description: "Nghiên cứu thị trường phía cầu (demand-side) cho digital product / dịch vụ ở Việt Nam — đo cầu thật + khả năng chi trả (WTP) + channel-market fit + defensibility qua keyword volume, marketplace sales (Shopee/Unica/Edumall/Gitiho/KyNa), community signal (FB groups, TikTok hashtag, Zalo OA), competitor pricing, unit economics — KHÔNG phải macro PESTEL. Output: keyword portfolio + Niche Score 100 điểm 7 chiều có evidence + go/no-go + falsification protocol, ghi thành note Markdown trong vault + 1 file .canvas trực quan. Bắt buộc triangulate ≥3 nguồn cho mỗi claim quan trọng. Dùng khi người dùng nói 'nghiên cứu thị trường', 'market research', 'validate niche', 'keyword research', 'demand validation', 'niche có nên làm không', 'có ai làm chưa', 'thị trường đủ lớn không', 'có lời không', 'chọn ngách', 'kiểm tra cầu', hoặc mô tả 1 ý tưởng kinh doanh cụ thể và muốn check feasibility. Ghi kết quả vào `04. Resources/Market & Competitor Research/Nghiên Cứu Thị Trường/`."
framework: "Demand Signal Triangulation + Niche Score 100 7 chiều (Problem Severity × WTP & Unit Economics × Search Demand × Trend & Timing × Competition & Defensibility × Channel-Market Fit × Personal Alignment) + TAM/SAM/SOM Vietnam + WTP Smoke Test Gate"
source: "Port từ BIZ.MKT.OS market-research skill — VN-native, demand-side; đã đổi output từ JSON/HTML sang note Markdown + .canvas theo convention vault này"
---

# Market Research (Demand-side) — Nghiên cứu thị trường phía cầu

Đo cầu thật cho 1 niche / ý tưởng kinh doanh số ở Việt Nam — bằng data triangulate qua keyword + marketplace + community, không phải opinion. Output là 1 Niche Score 100 điểm có evidence + go/no-go decision, ghi thành **note Markdown trong vault** (nguồn sự thật) kèm **1 file `.canvas`** trực quan tóm tắt điểm số.

> **Nguyên tắc đầu tiên:** Mỗi claim quan trọng (demand, competition, monetization) phải có **≥3 nguồn độc lập** support. 1 nguồn = anecdote. 2 = coincidence. 3 = signal. Nếu không triangulate được, ghi "evidence yếu" và downgrade confidence — không bịa.

## Đọc trước khi chạy (bắt buộc — theo CLAUDE.md của vault)

Vault này chỉ có **1 doanh nghiệp SME duy nhất**. Trước khi nghiên cứu, đọc `00. Business Context/` để biết công ty đang định vị ở đâu, ICP là ai, giá trị cốt lõi gì — nghiên cứu thị trường phải nối được về công ty hiện tại, không phải nghiên cứu trong chân không:

- `00. Business Context/Chân Dung Doanh Nghiệp.md` — định vị + ICP (để chấm **Personal Alignment** và **Channel-Market Fit** đúng với năng lực/audience công ty đang có, không chấm cho 1 solopreneur giả định).
- `00. Business Context/Business Model Canvas — [Tên Doanh Nghiệp].md` — customer segments, revenue streams, key resources hiện tại.
- `00. Business Context/Sản Phẩm & Dịch Vụ/` — sản phẩm/giá hiện có (để so sánh price tier khi chấm WTP).

Nếu các file trên còn là **bản mẫu trống**, báo người dùng biết đang thiếu ngữ cảnh công ty và gợi ý chạy skill `mo-hinh-kinh-doanh` trước — vẫn nghiên cứu được, nhưng đánh dấu Personal Alignment/Channel-Market Fit là "chưa neo được vào công ty thật, cần xem lại sau khi điền Business Context".

## Skill này phù hợp khi

- Người dùng đã có 1 niche ý tưởng cụ thể, muốn validate trước khi đầu tư thời gian/tiền
- Người dùng chưa có niche, cần brainstorm + pick top từ portfolio
- Cần size TAM/SAM/SOM realistic cho SME/solopreneur VN, không phải corporate-scale
- Muốn biết "ai đang làm rồi", giá bao nhiêu, định vị ở đâu

## Skill này KHÔNG làm (dùng skill khác trong vault)

| Việc cần làm | Dùng skill |
|---|---|
| Hệ thống hoá mô hình kinh doanh 9 ô, customer segments, đánh giá tính khả thi | `mo-hinh-kinh-doanh` |
| Phân tích sâu 1-5 đối thủ cụ thể (hồ sơ, kênh, offer Value Equation) | `phan-tich-doi-thu` |
| Tự đóng gói offer đầy đủ 6 thành phần theo Hormozi cho chính mình | `thiet-ke-offer` |
| Thiết kế thử nghiệm A/B để test giả định rút ra | `thu-nghiem-ab` |
| Thiết lập tracking đo phản ứng thị trường | `do-luong-tracking` |

> Skill này chỉ **đo cầu + score niche + go/no-go**. Nó feed dữ liệu vào các skill trên, không thay thế chúng.

## Workflow

### Mode A — Đã có 1 niche, cần validate (2-3h)
Skip Phase 1. Chạy Phase 2 → Phase 4. Đây là use case phổ biến nhất.

### Mode B — Chưa có niche, cần discover + pick (4-6h)
Phase 1 → 2 → 4. Bỏ Phase 3 trừ khi đã narrow xuống 1-2 candidate.

### Mode C — Đã validate, cần size TAM/SAM/SOM (1h)
Phase 3 only. Reference [tam-sam-som-vn.md](./references/tam-sam-som-vn.md).

| Phase | Mục tiêu | Output |
|---|---|---|
| **1. Discover** | Brainstorm 50+ candidate keyword/niche từ 5 nguồn | Seed list |
| **2. Signal** | Đo 4 demand signal cho mỗi candidate | Evidence table |
| **3. Size** | TAM/SAM/SOM cho top 1-2 niche | Sizing model |
| **4. Score & Decide** | Niche Score 100 + go/no-go | Decision report (note + canvas) |

## Live Research Protocol (bắt buộc dùng tools)

Model có cutoff. Search volume + competitor list + pricing thay đổi mỗi quý. Đoán = sai.

### Step 1 — Mỗi research bắt buộc chạy 6/10 query này

Thay `$NICHE` bằng keyword tiếng Việt + tiếng Anh để cross-check. Date-stamp mọi finding bằng ngày hôm nay (lấy từ context, không hardcode trong report).

```
"$NICHE khóa học vietnam"                     → Có ai đang dạy / sell course
"$NICHE shopee.vn"                            → Marketplace activity (sales, reviews)
"$NICHE unica.vn OR edumall.vn OR gitiho.vn"  → Course platform VN (số học viên, giá)
"$NICHE tiktok.com vietnam"                   → TikTok hashtag + creator (discovery #1 Gen Z VN 2026)
"$NICHE threads.net vietnam"                  → Threads VN (creator AI/tech đang shift sang, ít competition)
"$NICHE zalo OR shopee live vietnam"          → Zalo Mini App + livestream sale (kênh native VN)
"$NICHE site:reddit.com OR site:facebook.com" → Pain points + sentiment
"$NICHE facebook group vietnam"               → Community signal
"$NICHE google trends vietnam"                → Trend direction
"$NICHE giá bao nhiêu"                         → Pricing benchmark
```

**Bắt buộc:** ≥1 query phải là TikTok/Threads — kênh discovery thực tế của buyer VN 2026 đã dịch chuyển khỏi Google search cho nhiều niche (AI tool, beauty, finance, parenting). Bỏ qua = miss demand signal lớn nhất.

### Step 2 — WebFetch / defuddle để extract số chính xác

Search xong, **fetch URL cụ thể** để lấy data exact (không paraphrase). Dùng `defuddle parse <url> --md` cho trang content dài, WebFetch cho trang cần số cụ thể:
- Course page → giá, số học viên, review count, instructor credentials
- Shopee listing → "Đã bán X", price range, top seller stores
- FB Ads Library (facebook.com/ads/library, filter VN) → active ad creatives, ad spend signals
- Competitor pricing page → exact tier prices, bonuses, guarantee

### Step 3 — Manual tools (guide user nếu cần login)

| Tool | URL | Lấy gì |
|---|---|---|
| Google Trends VN | trends.google.com (region: Vietnam) | 5-year trend direction, related rising queries, geo hotspot |
| Google Keyword Planner | ads.google.com (free account) | Monthly search volume, CPC, competition level |
| FB Ads Library | facebook.com/ads/library (country: VN) | Active competitor ads, creative angles |
| Shopee Sales Filter | shopee.vn → sort by sales count | Top seller sales, price range, review patterns |

Khi cần user thao tác, output theo dạng: "Vào X, làm Y, copy data về theo template Z."

Chi tiết step-by-step + threshold đọc số: [vn-data-sources.md](./references/vn-data-sources.md)

## Niche Score 100 — 7 Dimension

7 chiều, weight không đều. Mỗi score **bắt buộc có evidence** (URL + số cụ thể), không "tôi nghĩ".

| # | Dimension | Max | Đo cái gì (1 dòng) |
|---|---|---|---|
| 1 | **Problem Severity** | 15 | Pain intensity × frequency × urgency × failed-attempts (starving crowd) |
| 2 | **WTP & Unit Economics** | 20 | Direct paid signal + net-of-fees margin + LTV / backend ladder + price-point match |
| 3 | **Search Demand** | 12 | Primary keyword + portfolio volume Vi+En cộng dồn |
| 4 | **Trend & Timing** | 10 | 5-year direction + adoption curve position |
| 5 | **Competition & Defensibility** | 15 | Sweet spot 10pts (active vs stale) + unfair advantage / moat 5pts |
| 6 | **Channel-Market Fit** | 15 | Audience kênh nào + creator content native fit + CAC viable (LTV/CAC ≥ 3) |
| 7 | **Personal Alignment** | 13 | Expertise + sustainability + network access — **chấm theo năng lực công ty trong `00. Business Context/`** |
| | **TOTAL** | **100** | |

> **VN volume note:** Threshold Search Demand thấp hơn US-mindset ~60% — VN keyword volume thường = 15-30% US cho cùng concept. Nếu audience là tech-savvy (lập trình viên, designer), volume En có thể chiếm 50-70% portfolio → cộng dồn cả 2 ngôn ngữ.
>
> **Saturation flip:** Đếm "active competitor 12 tháng gần" thay vì tổng. Unica/Edumall thường show 50+ course nhưng top course đã 18-24 tháng tuổi, instructor không update → de facto sweet spot, không phải saturated. Filter: course update <12 tháng + last review <6 tháng = "active".
>
> **Gross-to-net haircut:** Marketplace course revenue ≠ instructor take-home. Unica/Edumall share 30-50% revenue; refund rate VN online course 5-12%; FB Ads để fill course 30-60% revenue. Score Monetization theo NET, không gross.

**Decision tier:**

| Score | Verdict | Action |
|---|---|---|
| **80-100** | Strong Go | Allocate resource, fast-track — vẫn phải qua WTP smoke test gate trước build full |
| **60-79** | Solid Go | **Bắt buộc** qua WTP smoke test gate + 10 customer interview trước khi spend >5M VND build |
| **40-59** | Marginal | Chỉ proceed nếu Personal Alignment ≥10 AND Channel-Market Fit ≥10, set hard milestone + falsification trigger |
| **<40** | Pass | Quay lại Phase 1, pick niche khác |

Rubric chi tiết per dimension + worked example: [niche-scoring-100.md](./references/niche-scoring-100.md)

## WTP Smoke Test Gate (bắt buộc cho score 60-79, optional cho 80+)

Score cao nhưng chưa ai trả tiền cho **chính price-point của bạn** = giả định, chưa validate. Smoke test rẻ nhất:

1. **Build 1 landing 1-page** — chỉ promise + CTA "Đăng ký waitlist / giữ chỗ early-bird" với giá thật user định bán.
2. **Drive 200-500 warm traffic** qua organic content + 500K-2M FB Ads test.
3. **Đọc số:**
   - Waitlist signup ≥5% warm traffic = WTP signal valid → proceed MVP
   - Pre-pay/deposit ≥1% = WTP signal mạnh nhất → proceed full launch
   - <2% signup = WTP yếu → giảm giá 30-50% hoặc pivot offer hoặc kill
4. **Document số trong note** — đây là Tier A evidence mạnh hơn cả marketplace data.

## Falsification Protocol (pre-mortem — bắt buộc trong output)

Sau khi score, ép user pre-commit kill criteria trước khi spend:

> "Trong 90 ngày, nếu 3 signal nào xuất hiện thì kill niche này thay vì double-down?"

Ví dụ trigger:
- Waitlist conversion <1% sau 500 traffic = WTP fail
- 0 organic content piece đạt >5K reach trong 30 ngày = channel-market mismatch
- 2 large competitor cùng launch offer giống = window closed
- Personal cost: >40h/tuần × 90 ngày mà revenue <20M = burnout floor crossed

Pre-mortem này phải nằm trong note. Không có pre-mortem = không có decision discipline.

## TAM/SAM/SOM cho SME/solopreneur VN

```
TAM = Total potential buyers (VN)  × Average price
SAM = TAM × geo% × demo% × psycho%
SOM Year 1 = SAM × realistic share% (solo creator)
```

**Sanity check (red flags):**
- SOM Year 1 < 100M VND → niche quá nhỏ cho solo, pivot hoặc raise price
- SOM > 1% market share → quá lạc quan, dial back assumption
- TAM/SOM > 1000x → market quá fragmented, hard to capture share

Worked examples (AI course, English course, freelance coaching): [tam-sam-som-vn.md](./references/tam-sam-som-vn.md)

## Output — Note Markdown (nguồn sự thật) + file .canvas (trực quan)

**Khác với bản gốc BIZ.MKT.OS** (xuất JSON + HTML standalone): vault này là Obsidian PARA. Mỗi lần chạy skill ghi **2 file** vào `04. Resources/Market & Competitor Research/Nghiên Cứu Thị Trường/`:

1. **`[Niche] <Tên niche>.md`** — note Markdown là **nguồn sự thật duy nhất** (đầy đủ evidence, có nhãn nguồn, có link về `[[Chân Dung Doanh Nghiệp]]`). Theo đúng cấu trúc `[Ví dụ] Niche AI Tools Freelancer VN.md` có sẵn trong folder (đừng ghi đè file ví dụ đó — nó là mẫu).
2. **`[Niche] <Tên niche>.canvas`** — file JSON Canvas trực quan hoá điểm số: 1 node title (tên + total + verdict + link về note .md), 7 node dimension tô màu theo score, node TL;DR/verdict, và (nếu có Phase 3) 3 node funnel TAM/SAM/SOM. Node đầu tiên phải link `[[...]]` về note .md để 2 file luôn dính nhau.

Khung chi tiết cho cả note lẫn canvas (frontmatter, thứ tự section, toạ độ/màu node, quy tắc tô màu theo score/max): [mau-bao-cao.md](./references/mau-bao-cao.md).

### Sau khi ghi 2 file — cập nhật MOC

- Thêm link note vào `Nghiên Cứu Thị Trường/_MOC Nghiên Cứu Thị Trường.md` (danh sách niche đã nghiên cứu + 1 hàng bảng tóm tắt score/verdict).
- Nếu phát hiện xu hướng thị trường đáng theo dõi → thêm 1 dòng vào mục "Xu hướng thị trường" của `_MOC Market & Competitor Research.md`.

### Quy ước ghi file (theo CLAUDE.md vault)

- Ngôn ngữ tiếng Việt, heading dùng "tiếng Anh kèm tiếng Việt trong ngoặc".
- Frontmatter note: `tags: [market-research]`, `created: YYYY-MM-DD`, `up: ["[[_MOC Nghiên Cứu Thị Trường]]"]`.
- Không ghi đè note/canvas cũ nếu đã tồn tại cho cùng niche — **thêm log mới** vào mục "Nhật ký cập nhật" (đây là hồ sơ theo dõi lâu dài, re-score mỗi quý để thấy niche shift).
- Mỗi số liệu gắn nhãn nguồn: **Đã đo** (URL trực tiếp) / **Người dùng cung cấp** / **Ước tính**. Không có data → ghi "Chưa xác định — cần kiểm tra thủ công", không đoán đại.

## Anti-patterns thường gặp

| Anti-pattern | Vì sao sai | Cách khác |
|---|---|---|
| "Niche này hot lắm" không có URL | Opinion ≠ data. Báo cáo dạng này vô giá trị | Force ≥3 nguồn mỗi claim |
| Interest = Demand | High traffic không = willingness to pay | Check marketplace sales, CPC, paid course tồn tại |
| 1 nguồn duy nhất | Cherry-picked evidence | Triangulate (search + marketplace + community tối thiểu) |
| Audience size = revenue | 100K followers ≠ doanh thu. Conversion 0.5-2% thường thấy | Tính revenue = audience × conversion × LTV, không assume |
| Chấm Personal Alignment cho 1 solopreneur giả định | Vault này có 1 công ty thật — chấm lệch = decision sai | Neo vào `00. Business Context/Chân Dung Doanh Nghiệp.md` |
| TAM giả định 100% addressable | TAM ≠ SOM. Solo creator capture được 0.01-0.1% thường thấy | Apply geo + demo + psycho filter, document assumption |
| Stale data >12 tháng | Digital market shift quá nhanh | Prefer nguồn ≤12 tháng, date-stamp mọi finding |

## Best Practices

1. **Date-stamp mọi data point**: "Shopee 2026-05-14: 247 products, top seller 1.2K sold"
2. **URL/nguồn cho mỗi number**: kiểm tra lại được, audit được
3. **Triangulate ≥3 nguồn** cho claim demand/competition/monetization
4. **Cross-language search**: tiếng Việt + tiếng Anh — VN audience search cả 2 ngôn ngữ
5. **Timebox** mỗi phase. 80% confidence đủ để MVP
6. **Save raw search results**: screenshot, archive — markets shift, original data có thể disappear

## Reference Files

- [vn-data-sources.md](./references/vn-data-sources.md) — Danh sách nguồn data VN-specific (Shopee/Unica/Edumall/Gitiho/KyNa/FB/TikTok + Coccoc/Zalo OA/Spiderum/TikTok Creative Center), query template, threshold đọc tín hiệu strong/weak
- [niche-scoring-100.md](./references/niche-scoring-100.md) — Full rubric 7-dimension weighted với decision tree từng score band, worked example "AI tools cho freelance writer VN" 69/100
- [tam-sam-som-vn.md](./references/tam-sam-som-vn.md) — VN-native sizing math với 3 worked examples, filter % typical, sanity check thresholds
- [mau-bao-cao.md](./references/mau-bao-cao.md) — Khung note Markdown + spec file .canvas (frontmatter, section, toạ độ + màu node, quy tắc tô màu theo score)

---

**Khi user request market research:** đọc `00. Business Context/` (1-2 phút), confirm scope 1-2 câu (mode A/B/C, niche cụ thể chưa, region), rồi chạy Live Research Protocol Step 1 ngay — không hỏi nhiều trước khi có data đầu tiên. Kết thúc bằng việc ghi note .md + .canvas và cập nhật MOC.
</content>
</invoke>
