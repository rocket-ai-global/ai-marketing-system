# Mẫu output — Note Markdown + file .canvas

Bản gốc BIZ.MKT.OS xuất JSON + HTML. Vault này thay bằng **note Markdown** (nguồn sự thật, đầy đủ evidence) + **file `.canvas`** (trực quan tóm tắt điểm). Cả hai ghi vào `04. Resources/Market & Competitor Research/Nghiên Cứu Thị Trường/`, cùng basename `[Niche] <Tên niche>`.

Nhãn nguồn dùng ở mọi số liệu: **Đã đo** (URL trực tiếp) / **Người dùng cung cấp** / **Ước tính**. Không có data → "Chưa xác định — cần kiểm tra thủ công", không đoán.

---

## Phần 1 — Note Markdown (`[Niche] <Tên niche>.md`)

Copy khung dưới, điền data thật. **Không ghi đè** note cũ cho cùng niche — thêm log mới vào "Nhật ký cập nhật".

```markdown
---
tags: [market-research]
created: YYYY-MM-DD
up:
  - "[[_MOC Nghiên Cứu Thị Trường]]"
---

# [Niche] <Tên niche>

> **Scope:** <1 dòng — sản phẩm/dịch vụ + region + audience> · **Ngày:** YYYY-MM-DD · **Verdict:** <Strong Go / Solid Go / Marginal / Pass> (<total>/100)
> Trực quan điểm số: [[[Niche] <Tên niche>.canvas|Mở canvas]]

## TL;DR (Tóm tắt)
- **Verdict + evidence chính:** ...
- **Rủi ro lớn nhất:** ...
- **Next action:** ...

## Keyword Portfolio (Danh mục từ khoá)
| Keyword | Volume/tháng | CPC | Trend | Intent | Nguồn |
|---|---|---|---|---|---|
| Primary: ... | ... | ... | ↑/→/↓ | ... | Đã đo — Keyword Planner |
| Secondary 1-5 | ... | ... | ... | ... | ... |

**Tổng search volume (Vi+En):** _ /tháng

## Demand Signals (Tín hiệu cầu — quy tắc ≥3 nguồn)
| Signal | Evidence | Nguồn (URL) | Nhãn | Ngày |
|---|---|---|---|---|
| Marketplace | Shopee 247 products, top seller 1.2K sold | shopee.vn/... | Đã đo | YYYY-MM-DD |
| Course platform | Unica top course 856 học viên, 599K | unica.vn/... | Đã đo | ... |
| Community | FB group "X" 23K thành viên, daily posts | facebook.com/groups/... | Đã đo | ... |
| FB Ads | 12 active ads, avg run 30+ ngày | facebook.com/ads/library | Đã đo | ... |

## Competition Landscape (Bối cảnh cạnh tranh)
| Đối thủ | Định vị | Giá | Điểm mạnh | Khoảng trống (gap) |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |

## Niche Score (7 chiều)
| # | Dimension | Score | Evidence (1 dòng + URL) |
|---|---|---|---|
| 1 | Problem Severity | _/15 | ... |
| 2 | WTP & Unit Economics | _/20 | ... |
| 3 | Search Demand | _/12 | ... |
| 4 | Trend & Timing | _/10 | ... |
| 5 | Competition & Defensibility | _/15 | (sweet spot _/10 + moat _/5) |
| 6 | Channel-Market Fit | _/15 | ... |
| 7 | Personal Alignment | _/13 | (neo vào [[Chân Dung Doanh Nghiệp]]) |
|   | **TOTAL** | **_/100** | |

## Unit Economics
- **Gross price:** _ VND
- **Platform/payment fee:** _% · **Refund rate:** _% · **Marketing cost/sale:** _% revenue
- **Effective net per sale:** _ VND · **LTV (backend ladder):** _ VND · **CAC ceiling (LTV÷3):** _ VND

## TAM/SAM/SOM (nếu Phase 3 chạy)
- **TAM:** _ tỷ VND = _ buyers × _ VND
- **SAM:** _ tỷ VND = TAM × _% (filters: geo _ / demo _ / psycho _ / price-fit _)
- **SOM Year 1:** _ M VND (Conservative / Base / Optimistic)
- **Sanity:** [Pass / Floor warning <100M / Optimism warning >1% share / Fragmented >1000x]

## WTP Smoke Test Plan (bắt buộc nếu score 60-79)
- **Landing promise:** _ · **Traffic + cost:** _ · **Threshold:** ≥5% waitlist OR ≥1% pre-pay → proceed; <2% → kill/pivot · **Timeline:** _ ngày

## Pre-mortem — Falsification triggers (kill criteria)
Trong 90 ngày, nếu **bất kỳ 2 signal nào** xuất hiện đồng thời → kill thay vì double-down:
- [ ] Waitlist conversion <_% sau _ traffic
- [ ] 0 organic content piece đạt >_ reach trong 30 ngày
- [ ] _ large competitor cùng launch offer overlap
- [ ] Effective CAC > _% LTV cap

## So với chúng tôi ([[Chân Dung Doanh Nghiệp]])
- Niche này khớp/lệch định vị hiện tại ở đâu:
- Key resources công ty đang có đủ để làm không:
- (Nếu Business Context còn trống → ghi "Chưa neo được, cần chạy business-model-canvas trước")

## Recommendation (Khuyến nghị)
**Decision:** ... · **Rationale:** (2-3 đoạn nối evidence → score → decision) · **Top risk:** ...
**Next steps (90 ngày):**
- [ ] Tuần 1-2: WTP smoke test (landing + waitlist)
- [ ] Tuần 3-4: 10 customer interview
- [ ] Tháng 2: MVP nếu WTP pass

## Nhật ký cập nhật (thêm mới nhất lên đầu)
### YYYY-MM-DD
- Lần nghiên cứu đầu: score _/100, verdict _. Nguồn chính: ...

## Ảnh hưởng tới chiến lược
- [[_MOC Decisions]] (nếu dẫn tới 1 quyết định cụ thể)
```

---

## Phần 2 — File `.canvas` (JSON Canvas trực quan)

Obsidian đọc `.canvas` là JSON thuần. Ghi bằng Write tool. Layout: 1 title bar → hàng 7 node dimension → node TL;DR + node Decision → (optional) hàng funnel TAM/SAM/SOM.

### Quy tắc màu (Obsidian preset: "1"=đỏ, "2"=cam, "3"=vàng, "4"=xanh lá, "5"=xanh cyan, "6"=tím)

**Node dimension** — tô theo ratio = score / max:
- ratio ≥ 0.70 → `"4"` (xanh lá — mạnh)
- 0.45 ≤ ratio < 0.70 → `"3"` (vàng — trung bình)
- ratio < 0.45 → `"1"` (đỏ — yếu, chỗ cần patch)

**Title bar** — tô theo total:
- ≥80 → `"4"` · 60-79 → `"5"` · 40-59 → `"3"` · <40 → `"1"`

### Toạ độ chuẩn (dán làm khung, chỉnh text)

- Title bar: `x:0, y:-180, width:2480, height:140`
- 7 node dimension: `y:20, height:250, width:320`, `x` = 0, 360, 720, 1080, 1440, 1800, 2160
- Node TL;DR/verdict: `x:0, y:330, width:1200, height:300`
- Node Decision + pre-mortem: `x:1280, y:330, width:1200, height:300`
- Funnel (nếu có Phase 3): TAM `x:0, y:690, w:800, h:200` · SAM `x:840, y:690, w:800, h:200` · SOM `x:1680, y:690, w:800, h:200`

### Skeleton (worked example — niche "AI tools cho freelance writer VN", 69/100)

Node đầu **bắt buộc** link `[[...]]` về note .md để 2 file dính nhau. Mỗi node dimension ghi: tên, `score/max`, 1 dòng evidence ngắn.

```json
{
	"nodes":[
		{"id":"title","type":"text","x":0,"y":-180,"width":2480,"height":140,"color":"5","text":"# 🎯 NICHE SCORE — AI tools cho freelance writer VN\n**69/100 · Solid Go** · digital course, region VN, audience freelance writer · Chi tiết: [[[Niche] AI Tools Freelancer VN]]"},

		{"id":"d1","type":"text","x":0,"y":20,"width":320,"height":250,"color":"3","text":"## 1. Problem Severity\n**11 / 15**\n\n15+ post pain 'khách bỏ vì ChatGPT', income loss ≤12 tháng. Đã đo — Reddit + FB group."},
		{"id":"d2","type":"text","x":360,"y":20,"width":320,"height":250,"color":"3","text":"## 2. WTP & Unit Econ\n**14 / 20**\n\nUnica top course 1.2K enrolled; net ~45-80%; ladder coaching 5M khả thi. Đã đo."},
		{"id":"d3","type":"text","x":720,"y":20,"width":320,"height":250,"color":"4","text":"## 3. Search Demand\n**9 / 12**\n\n'AI viết content' ~3K/th + portfolio Vi+En ~12K. Đã đo — Keyword Planner."},
		{"id":"d4","type":"text","x":1080,"y":20,"width":320,"height":250,"color":"3","text":"## 4. Trend & Timing\n**7 / 10**\n\nTrends VN +200%/2 năm, Early→Early Majority. Discount fad risk. Đã đo."},
		{"id":"d5","type":"text","x":1440,"y":20,"width":320,"height":250,"color":"3","text":"## 5. Competition & Defensibility\n**8 / 15**\n\nSweet spot 7/10 (gap rõ) + moat 1/5 (dễ clone 6 tháng). Đã đo — FB Ads."},
		{"id":"d6","type":"text","x":1800,"y":20,"width":320,"height":250,"color":"4","text":"## 6. Channel-Market Fit\n**11 / 15**\n\nAudience FB+Spiderum+Threads; creator 8K FB native; CAC organic tốt. Đã đo."},
		{"id":"d7","type":"text","x":2160,"y":20,"width":320,"height":250,"color":"3","text":"## 7. Personal Alignment\n**9 / 13**\n\nNeo [[Chân Dung Doanh Nghiệp]]: 2 năm content, 8K FB cùng niche."},

		{"id":"tldr","type":"text","x":0,"y":330,"width":1200,"height":300,"color":"5","text":"## 📌 TL;DR\n\n**Verdict:** Solid Go (69/100)\n\n✅ Cầu thật: Unica 1.2K enrolled + 15 FB advertiser + trend +200%\n⚠️ Rủi ro: Defensibility chỉ 1/5 → có thể bị clone trong 6 tháng\n➡️ Next: WTP smoke test 2 tuần (waitlist 990K, 500 traffic) trước khi build"},

		{"id":"decision","type":"text","x":1280,"y":330,"width":1200,"height":300,"color":"3","text":"## ⚖️ Decision & Pre-mortem\n\n**60-79 → bắt buộc WTP smoke test + 10 interview trước >5M spend**\n\n**Kill nếu (bất kỳ 2 signal):**\n- Waitlist <3% sau 500 traffic\n- 0 content piece >5K reach trong 30 ngày\n- 2 competitor lớn cùng launch offer overlap\n\n**Patch trước launch:** xây community lock-in (private FB group) để bù moat yếu."},

		{"id":"tam","type":"text","x":0,"y":690,"width":800,"height":200,"color":"6","text":"## TAM\n**~3.564 tỷ VND**\n3.6M freelancer × 60% AI interest × 990K. Ước tính — Anphabe 2026 + Google e-Conomy SEA."},
		{"id":"sam","type":"text","x":840,"y":690,"width":800,"height":200,"color":"6","text":"## SAM\n**~157 tỷ VND**\nTAM × geo 30% × demo 70% × psycho 30% × price-fit 70% = ~159K người."},
		{"id":"som","type":"text","x":1680,"y":690,"width":800,"height":200,"color":"1","text":"## SOM Year 1\n**~60-140M VND** (midpoint 100M)\n⚠️ Border floor 100M — cân nhắc raise price 1.5-2M coaching add-on."}
	],
	"edges":[
		{"id":"e1","fromNode":"tam","fromSide":"right","toNode":"sam","toSide":"left","label":"× filters"},
		{"id":"e2","fromNode":"sam","fromSide":"right","toNode":"som","toSide":"left","label":"× share%"}
	]
}
```

### Lưu ý khi sinh canvas

- Số node dimension luôn = 7 (kể cả khi 1 chiều là 0 điểm — node đỏ chỉ ra chỗ cần patch chính là giá trị của canvas).
- Nếu **không** chạy Phase 3 (không có TAM/SAM/SOM) → bỏ 3 node funnel + 2 edge, giữ nguyên phần trên.
- Text trong node dùng Markdown: `##` heading, `**bold**`, `\n` xuống dòng. Giữ ngắn (2-4 dòng evidence) — chi tiết đầy đủ nằm ở note .md, canvas chỉ để nhìn nhanh.
- Đổi `[[[Niche] AI Tools Freelancer VN]]` ở node title thành đúng tên note .md thật.
</content>
