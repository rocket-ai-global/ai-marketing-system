# TAM / SAM / SOM cho Solopreneur Việt Nam

Sizing math VN-native với worked examples. Khác bản textbook corporate ở chỗ: SOM cho solopreneur thường rất nhỏ (0.01-0.1% share), và biggest mistake là assumption quá lạc quan.

## Khái niệm — phân biệt 3 layer

```
TAM (Total)     = Toàn bộ market potential nếu mọi người có thể mua, đều mua
SAM (Servable)  = Subset của TAM mà BẠN có thể realistic serve (geo + demo + psycho filter)
SOM (Obtainable)= Subset của SAM mà BẠN realistic capture được trong Year 1-3 (sau competition)
```

**Hierarchy:** TAM > SAM > SOM. Ratio điển hình solopreneur VN:
- SAM/TAM ≈ 5-20% (sau filter)
- SOM/SAM ≈ 0.01-0.5% Year 1 (solo creator capture rất nhỏ)

## Công thức cơ bản

```
TAM = N_buyer × Avg_price
SAM = TAM × (geo% × demo% × psycho% × price_tier_fit%)
SOM_Y1 = SAM × Year1_share%
SOM_Y3 = SAM × Year3_share% (typically 3-10x Y1 cho solo với traction tốt)
```

**Filter %** typical cho VN:

| Filter | Common % |
|---|---|
| **Geographic** (đô thị 1+2: HCMC, HN, DN, Cần Thơ, HP, BD) | 40-60% population |
| **Demographic** (age 25-40, white-collar/digital native) | 25-50% |
| **Psychographic** (early adopter, willing to learn paid) | 10-30% |
| **Price tier fit** (segment match được price point bạn set) | 30-80% |

## Sanity Check (red flags)

Khi nào SOM "sai":

| Red flag | Diagnose | Action |
|---|---|---|
| **SOM Y1 < 100M VND** | Niche quá nhỏ cho solo full-time | Pivot, raise price, hoặc treat như side project |
| **SOM > 1% market share** | Over-optimistic | Dial back Y1 share % xuống 0.1% |
| **TAM/SOM > 1000x** | Market quá fragmented, hard to capture | Re-segment narrower |
| **SAM < 5% TAM** | Filter quá aggressive HOẶC niche không serviceable | Re-check filter logic |
| **SAM > 30% TAM** | Filter quá lỏng, không realistic | Tighten geo/psycho filter |

## Inputs cần lấy real (không guess)

| Input | Where to find |
|---|---|
| VN population age 25-40 | GSO (Tổng Cục Thống Kê) — gso.gov.vn |
| VN white-collar / khu vực dịch vụ | GSO labor force survey |
| Internet penetration / digital users | We Are Social VN annual report, Google e-Conomy SEA |
| Niche-specific market size USD | IMARC, Mordor Intelligence, Statista (limited free) |
| Competitor enrollment count | Course platform pages (Unica/Edumall/Gitiho) — real data |
| Pricing benchmark | Multi-competitor scrape qua WebFetch |

**Bắt buộc cite URL cho mỗi input.** Đoán = research vô giá trị.

---

## Worked Example 1: Khóa học AI tools cho freelancer VN (giá 990K)

### TAM

```
N_buyer = VN freelancer/gig workers × % interested in AI tools
        = 6M freelancer (est. 2026, ~18% of 33M labor force) × 60% interest in productivity AI
        = 3.6M people

Avg_price = 990K VND (the offer)

TAM = 3.6M × 990K = ~3,564 tỷ VND
```

**Source cần verify:**
- 6M freelancer figure: Anphabe 2026 report HOẶC Vietnam Briefing
- 18% labor share gig economy: same source
- 60% AI interest: Google e-Conomy SEA 2025 ("81% interact AI daily" — derive narrower segment)

### SAM

Filters:
- Geographic: HCMC + HN + DN = ~30% of freelancer (urban concentration)
- Demographic: age 22-40 = ~70% of freelancer pool
- Psychographic: actively want to upskill in AI = ~30% (đang search/đọc/sẵn sàng trả)
- Price tier fit: 990K = mid-market, ~70% of urban digital freelancer affordable

```
SAM = 3,564 tỷ × 30% × 70% × 30% × 70% = ~157 tỷ VND
N_addressable = 3.6M × 30% × 70% × 30% × 70% = ~159K people
```

### SOM Year 1 (solo creator, 8K FB followers, no big ad budget)

Bottom-up math:
- 8K followers × 5% engaged (writer freelancer audience trùng) = 400 warm
- + Organic reach via content (FB + maybe TikTok): 2K-3K warm reach over 6 months
- Total warm audience Y1: ~2.5K-3.5K
- Conversion (warm → buy): 1.5-3% với offer match audience pain
- Buyers: 40-100 → revenue: 40M - 100M VND
- + Optional cold ads with 1-2M budget: +20-40 buyers → +20-40M

**SOM Y1 = 60M - 140M VND (midpoint ~100M)**

### Sanity Check

| Check | Result |
|---|---|
| SOM Y1 < 100M floor? | Border — midpoint 100M, lower-bound below floor → **WARNING** |
| SOM > 1% share? | 100M / 157,000M = 0.064% → OK far below 1% |
| TAM/SOM ratio | 3,564,000M / 100M = 35,640x → very fragmented |

**Verdict:** Marginal cho mass-market 990K. Recommendations:
- Raise price tier (1.5-2M coaching add-on) để raise SOM revenue cùng số học viên
- Hoặc niche down sub-segment "AI cho freelance writer cụ thể" — sàn rộng nhưng convert cao hơn
- Hoặc accept là side income Y1 (100M = ~8M/tháng), scale Y2 khi có testimonial

---

## Worked Example 2: Khóa English giao tiếp cho người đi làm VN (giá 2.5M)

### TAM

```
N_buyer = VN white-collar workers × % motivated to improve English
        = 6M white-collar (per GSO 2025) × 50% career-motivated to learn English
        = 3M people

Avg_price = 2.5M VND

TAM = 3M × 2.5M = ~7,500 tỷ VND
```

Cross-validate: IMARC report VN digital English learning market 2026 ≈ USD 120M = ~3,000 tỷ VND for DIGITAL segment alone. Tổng English market lớn hơn (offline + digital + 1-1) → TAM 7.5K tỷ reasonable.

### SAM

Filters cho 1 solo creator cạnh tranh trong tier 2.5M:
- Geographic: 4 urban hubs (HCMC, HN, DN, BD) = ~50%
- Demographic: age 25-40 (career peak) = ~50%
- Psychographic: digital learners (open to online format, đã thử app/tool) = ~30%
- Price tier fit: 2.5M = mid-premium tier, ~50% affordable trong audience digital-ready

```
SAM = 7,500 tỷ × 50% × 50% × 30% × 50% = ~281 tỷ VND
N_addressable = 3M × 50% × 50% × 30% × 50% = ~112K people
```

### SOM Year 1 (solo, no ads budget)

Constraints:
- Heavy competition: ELSA (10M users), ZIM, Jaxtina, Topica, Prep, Hocmai
- Solo creator no brand → cold start với 0 followers gốc
- Audience build over 6-12 months organic

Bottom-up:
- Organic reach 0 → 10K followers within 12 months (aggressive but realistic với content tốt) = ~3K engaged
- Cold audience reached via FB/TikTok content: 30K-50K
- Conversion warm→buy: 0.3-0.8% (lower vì tier giá cao, English crowded)
- Buyers: 15-30 → revenue: 37.5M - 75M VND

**SOM Y1 = 30M - 75M VND**

### Sanity Check

| Check | Result |
|---|---|
| SOM Y1 < 100M floor? | YES — even upper bound 75M < 100M → **RED FLAG** |
| SOM > 1% share? | 75M / 281,000M = 0.027% → far below 1% (OK ratio) |
| Diagnose | Niche fragment quá lớn + competition quá đông cho solo no ads |

**Verdict:** Niche này KHÔNG good cho solo no-ads. Path forward:
- Niche down cực hẹp: "English cho IT engineer chuẩn bị job MNC" hoặc "English cho HR Vietnam upgrade lên global role" — narrower → có thể compete
- Hoặc raise price thành 1-1 coaching premium 8-15M để cần ít buyers hơn
- Hoặc partner với 1 brand có audience sẵn

---

## Worked Example 3: Coaching cho freelance designer VN (1-1, 8M/cohort 3 tháng)

### TAM

```
N_buyer = VN freelance designer × % needing structured coaching
        = 200K freelance designer (est. from UpWork+Behance VN data) × 30% premium-tier serious
        = 60K people

Avg_price = 8M VND/cohort

TAM = 60K × 8M = ~480 tỷ VND
```

(TAM nhỏ hơn vì niche hẹp + high-ticket, không phải mass)

### SAM

Filters:
- Geographic: HCMC + HN = ~70% of freelance designer concentration
- Demographic: 25-35 age (career middle) = ~60%
- Psychographic: actively scaling income, không hài lòng plateau = ~40%
- Price tier fit: 8M = premium, ~50% afford (designer cao tier)

```
SAM = 480 tỷ × 70% × 60% × 40% × 50% = ~40 tỷ VND
N_addressable = 60K × 70% × 60% × 40% × 50% = ~5K people
```

### SOM Y1 (solo coach, có 5K followers trong designer community)

Bottom-up:
- 5K followers × 8% engaged trong audience designer pain = 400 warm
- Conversion to high-ticket: 0.5-1.5% (luôn lower cho premium)
- Buyers: 2-6 cohort × 8M = 16M - 48M

Cohort size constraint solo coach: 5-10 người/cohort, 3-4 cohort/year max
- 3 cohort × 8 người × 8M = 192M (upper bound nếu fill được)
- 2 cohort × 5 người × 8M = 80M (realistic Y1)

**SOM Y1 = 80M - 192M VND (midpoint ~135M)**

### Sanity Check

| Check | Result |
|---|---|
| SOM Y1 < 100M floor? | Border — midpoint 135M OK, lower-bound 80M close to floor |
| SOM > 1% share? | 135M / 40,000M = 0.34% → still <1%, OK |
| TAM/SOM ratio | 480,000M / 135M = 3,555x → still fragmented but better |

**Verdict:** Tier 8M coaching khả thi cho solo nếu fill cohort. Risk: cohort fill rate. Mitigation: build waitlist > 3x cohort capacity trước launch.

---

## Quick Sizing Template (15 phút)

Khi user cần con số nhanh, không phải full research:

```markdown
## Quick Size: $NICHE @ $PRICE

**Inputs (cite source):**
- Total VN audience pool: [N] (source: ...)
- Niche interest %: [X]% (source: ...)
- Price: [P] VND

**TAM** = N × X% × P = ___ tỷ VND

**SAM** (filters):
- Geo: __% (rationale: ...)
- Demo: __% (rationale: ...)
- Psycho: __% (rationale: ...)
- Price fit: __% (rationale: ...)
- SAM = TAM × (4 filter cộng dồn) = ___ tỷ VND

**SOM Y1** (solo creator):
- Warm audience reachable Y1: __ people
- Conversion: __% (justify: tier giá X, niche Y)
- Buyers: __ × price = ___ M VND

**Sanity:** [Pass / Warning floor 100M / Warning >1% share / Warning fragmented]

**Recommendation:**
- If SOM <100M: pivot OR raise price OR accept side-income
- If SOM 100-500M: solid for solo with focused launch
- If SOM >500M: aggressive scale possible, consider ads budget
```
