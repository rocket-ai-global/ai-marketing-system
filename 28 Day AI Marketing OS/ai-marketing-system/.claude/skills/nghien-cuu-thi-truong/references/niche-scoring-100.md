# Niche Score 100 — Full Rubric (7-dimension, revised 2026-05-17)

7 chiều, weight không đều. Mỗi điểm **bắt buộc có evidence URL + số cụ thể** — không "tôi nghĩ".

## Triết lý

Score không phải để đẹp report. Score để **force decision**:
- Score cao + Channel-Market Fit thấp = trap (xây xong không tiếp cận được buyer kinh tế)
- Score cao + Defensibility thấp = bị clone tháng 13
- Score giữa (40-79) = cần kỷ luật milestone + WTP smoke test, không cảm tính
- Score thấp + passion cao = OK proceed nhỏ, chấp nhận side income

Không tự inflate score để justify quyết định đã định sẵn. Honest score = useful score.

## Sao thay đổi từ bản cũ (5×20)?

| Vấn đề bản cũ | Fix bản mới |
|---|---|
| Search Demand + Trend Direction = 40pts cho 1 loại tín hiệu correlated | Giảm xuống 22pts (12+10) |
| Monetization chỉ đo first sale, inflate gross-revenue 3x | Tách 4 sub-score net-of-fees, LTV, price-match |
| Không có Problem Severity → niche "interesting" thắng "starving crowd" | NEW dimension 15pts |
| Không có Distribution / CAC dimension → 2 niche cùng demand 18/20 nhưng 1 lỗ 1 lãi | NEW Channel-Market Fit 15pts |
| Competition chỉ backward-looking → bị clone sau khi validate | Thêm Defensibility 5pts sub-score |
| Personal Alignment 20/100 over-weighted cho market research tool | Giảm xuống 13 |

---

## Dimension 1: Problem Severity (0-15) — Starving Crowd

**Đo cái gì:** Pain intensity × frequency × urgency × failed-attempts. Hormozi rule #1 — "starving crowd beats great offer".

**Cách lấy data:** Reddit/FB group/forum verbatim language (Tier C — direct stated preference); search intent keyword chứa pain ("không biết cách...", "làm sao để...", "X bị Y"); refund/complaint pattern trên course platform (review 1-2 sao).

| Pts | Pattern | Evidence yêu cầu |
|---|---|---|
| 15 | Pain weekly+, thiệt hại tiền/thời gian/uy tín đo được, deadline urgency, user đã try ≥2 solution thất bại | 10+ verbatim post Reddit/FB chứa pain language + 2+ existing failed solution |
| 12 | Pain weekly, gây frustration rõ, đã try ≥1 solution | 5+ verbatim post + 1 known failed solution |
| 8 | Pain monthly, annoyance level | 3+ verbatim post |
| 4 | Pain rare hoặc latent, chưa tự nhận | <3 post, mostly "would be nice if..." |
| 0 | Pure vitamin (curiosity), không có pain language | Không tìm được pain post |

**Vitamin vs Painkiller test:** User mất ngủ vì problem này? Sẵn sàng trả tiền giải quyết tuần này không phải tháng sau? Nếu không → đây là vitamin, max 8pts.

**Stated pain ≠ actual willingness to act.** Discount 30% nếu chỉ thấy pain post nhưng không thấy ai trả tiền cho solution (link sang Dimension 2).

---

## Dimension 2: WTP & Unit Economics (0-20)

**Đo cái gì:** Có evidence cụ thể người trả tiền cho problem này AT THIS PRICE POINT — và sau khi trừ chi phí, instructor có lời net không.

**Cách lấy data:** Marketplace top seller "Đã bán" + course platform "X học viên" + FB Ads Library ad duration + competitor price distribution + platform fee rates.

**4 sub-component (cộng dồn max 20):**

### 2a. Direct paid signal (max 6)

| Pts | Evidence |
|---|---|
| 6 | Top course ≥500 enrolled HOẶC Shopee top ≥1K sold HOẶC ≥10 distinct FB Ads chạy >30 ngày |
| 4 | 100-500 enrolled HOẶC 200-1K sold HOẶC 3-10 active ads |
| 2 | <100 enrolled / <200 sold / 1-2 active ads |
| 0 | Free content only, no paid signal |

### 2b. Effective net margin (max 6)

Tính net per sale sau platform fee + refund + marketing cost:

```
Net % = (1 - platform_fee% - refund_rate% - marketing_cost_per_sale%)
```

Benchmark VN 2026:

| Channel | Platform fee | Refund | Marketing | Net % |
|---|---|---|---|---|
| Own site + organic | 3-5% (Stripe/Sepay) | 5-10% | 0% (organic) | 85-92% |
| Own site + paid ads | 3-5% | 5-10% | 30-50% rev | 35-55% |
| Unica / Edumall | 30-50% | 5-12% | varied | 38-55% |
| Gitiho / Kyna | 30-40% | 5-10% | varied | 50-60% |

| Pts | Net % effective |
|---|---|
| 6 | ≥70% (own site organic) |
| 4 | 50-70% (own site + light paid) |
| 2 | 35-50% (marketplace OR heavy paid) |
| 0 | <35% (high CAC OR high refund OR commodity pricing) |

### 2c. LTV / Backend ladder (max 5)

| Pts | Pattern |
|---|---|
| 5 | Backend ladder rõ (tripwire → core → premium → recurring), LTV ≥ 3x first sale |
| 3 | 2 tier khả thi (core + upsell), LTV ~2x |
| 1 | One-time low-ticket, không có backend |
| 0 | Niche structurally one-and-done (vd ebook giải quyết 1 problem trọn vẹn) |

### 2d. Price-point match validated (max 3)

| Pts | Evidence |
|---|---|
| 3 | ≥3 competitor đang sell thành công AT YOUR PRICE TIER (±30%) với traction (≥200 enrolled / ≥30 day ad run) |
| 2 | 1-2 competitor ở tier giá tương tự |
| 1 | Competitor toàn ở tier khác (tier giá của user chưa được validate) |
| 0 | Không có competitor nào ở price tier của user |

**Pricing tier benchmark VN 2026:**
- Tripwire: 99K-499K
- Core course: 499K-2M
- Premium: 2M-10M
- Mastermind: 10M+

---

## Dimension 3: Search Demand (0-12)

**Đo cái gì:** Tổng monthly search volume cho niche keyword portfolio (primary + 5-10 secondary). Lưu ý — VN buyer 2026 đang shift discovery sang TikTok/Threads/Zalo cho nhiều niche → đừng treat search volume là tín hiệu duy nhất.

**Cách lấy data:** Google Keyword Planner (free Google Ads account) region VN, language Vi+En; cross-check Coccoc keyword tool (~10% VN search share).

| Pts | Threshold (VN-calibrated, Vi+En cộng dồn) |
|---|---|
| 12 | Primary keyword ≥2K/tháng + portfolio total ≥10K |
| 9 | Primary 800-2K + portfolio 4K-10K |
| 6 | Primary 300-800 + portfolio 1.5K-4K |
| 3 | Primary 80-300 + portfolio 400-1.5K |
| 0 | Primary <80 AND portfolio <400 |

**Edge case:**
- Niche TikTok-native (Gen Z, beauty, AI consumer) — search Google thấp nhưng TikTok hashtag >1M views = bù bằng signal kênh khác, score Search ở giữa (6-9pts) và compensate trong Channel-Market Fit.
- B2B/high-ticket — volume thấp nhưng CPC cao + LinkedIn signal mạnh → đo qua Dimension 2 thay vì ép Search Demand.

---

## Dimension 4: Trend & Timing (0-10)

**Đo cái gì:** Trajectory 5 năm + adoption curve position (Innovators / Early Adopters / Early Majority / Late Majority).

**Cách lấy data:** trends.google.com region VN, time "Past 5 years"; cross với TikTok hashtag growth rate; check "Related queries → Rising" cho breakout sub-niche.

| Pts | Pattern + Adoption position |
|---|---|
| 10 | Rising ≥50% / 2 năm + đang ở Early Adopter → Early Majority transition (chasm crossing) |
| 7 | Moderate rise 20-50% / 2 năm + Early Adopter phase (chấp nhận audience education effort) |
| 4 | Flat nhưng evergreen volume cao (mature market, cần differentiate) |
| 2 | Slight decline nhưng absolute volume vẫn lớn |
| 0 | Clear decline HOẶC fad spike rồi tụt HOẶC quá sớm (Innovator-only, không có buyer ngoài tech early adopter) |

**Timing red flag:**
- Đỉnh fad cao bất thường + breakout query rising +500% trong 6 tháng = có thể là hype peak (vd "ChatGPT prompt engineering" 2023 peak rồi tụt nhanh). Discount 2 pts nếu chưa thấy steady plateau.
- Quá sớm: niche cần 18+ tháng audience education = solo creator không sustain được, score 2-4.

---

## Dimension 5: Competition & Defensibility (0-15)

Split thành 2 sub-score:

### 5a. Competition Sweet Spot (max 10) — backward-looking

**Đo cái gì:** Có đủ competitor để validate demand, còn gap để differentiate. Goldilocks zone.

**Cách lấy data:** Đếm course trên Unica + Edumall + Gitiho + Kyna; đếm distinct advertiser FB Ads Library VN; đọc top 5 → score quality.

| Pts | Active competitor landscape (update ≤12 tháng) |
|---|---|
| 10 | 3-10 active mid-quality + clear gap (under-served sub-segment) |
| 9 | 50+ tổng nhưng top course stale >18 tháng — **saturation flip** opportunity |
| 7 | 10-20 active, một số top-tier nhưng có angle |
| 4 | 20-50 active, gap hẹp — cần moat |
| 2 | 50+ saturated AND top course vẫn fresh HOẶC <3 active (no validation) |
| 0 | Dominated 1-2 brand cố thủ HOẶC zero competitor (no market) |

**Saturation flip nuance:** Filter "active" = course update <12 tháng + last review <6 tháng. Unica/Edumall thường show 50-100 course nhưng top course 18-24 tháng tuổi, không update curriculum → de facto opportunity.

**Zero ≠ opportunity:** Zero competitor thường = no demand. Trừ khi có proprietary insight (regulatory change, tech vừa khả thi 6 tháng qua) — phải document.

### 5b. Defensibility / Moat (max 5) — forward-looking

**Đo cái gì:** 6-12 tháng nữa khi user đã build + validate, ai vào copy được? Cái gì lock buyer ở lại?

| Pts | Unfair advantage + switching cost |
|---|---|
| 5 | ≥2 trong các yếu tố: insider data / proprietary process / exclusive network / regulatory cert / audience trust ≥2 năm + lock-in sau mua (community, data, certification) |
| 3 | 1 yếu tố unfair advantage HOẶC moderate switching cost (community membership, gradual content library) |
| 1 | Brand/expertise positioning thuần tuý — có thể copy nhưng cần thời gian |
| 0 | Pure execution, có thể clone full trong 6 tháng |

**Solo creator reality check:** Most solo creator score 1-3 ở dimension này. Đó OK — không phải mọi niche cần moat khủng. Nhưng score 0 + Score 8a cao = warning "race to bottom incoming".

---

## Dimension 6: Channel-Market Fit (0-15)

**Đo cái gì:** Audience tập trung ở kênh nào + creator có content native fit không + CAC viable ở price tier nào không. LTV/CAC phải ≥ 3:1 để sustainable.

**Cách lấy data:** Audience kênh — survey + community observation (FB group 10K vs TikTok hashtag 5M views = 2 niche khác kênh). Creator fit — track record content trên kênh đó (đã có 1K+ follower / 10+ post có engagement chưa). CAC ước tính — FB Ads Library bid signal + CTR benchmark + competitor lead-magnet funnel reverse-engineer.

**3 sub-component (cộng dồn max 15):**

### 6a. Audience concentration (max 5)

| Pts | Pattern |
|---|---|
| 5 | Audience tập trung 1-2 channel rõ (vd "freelance designer VN" = FB group + Behance) |
| 3 | 2-3 channel mỗi cái có 30-50% audience |
| 1 | Scattered 4+ channel, không kênh nào dominant |
| 0 | Audience không định nghĩa được, đoán |

### 6b. Creator content native fit (max 5)

| Pts | Track record |
|---|---|
| 5 | Đã có content history trên kênh đó (≥1K follower / ≥10 post engagement tốt) |
| 3 | Đã thử kênh đó nhưng chưa có traction, hoặc có kênh adjacent |
| 1 | Phải học format mới từ đầu (vd content writer phải học TikTok dance) |
| 0 | Format khắc với personality (vd introvert phải làm livestream daily) |

### 6c. CAC viability (max 5)

LTV/CAC tính từ Dimension 2c và Dimension 6b paid-channel estimate:

| Pts | LTV / CAC ratio |
|---|---|
| 5 | ≥5:1 (organic dominant + viral coefficient) |
| 4 | 3-5:1 (sustainable paid + organic mix) |
| 2 | 1.5-3:1 (marginal, scale risk) |
| 0 | <1.5:1 (every sale loses money at scale) |

**Common pitfall:** Tier giá 199K + niche cần FB Ads với CPC 50K → CAC ~200K-400K → LTV/CAC <1 → niche này bất khả thi với paid. Phải có organic path khác hoặc pivot tier giá.

---

## Dimension 7: Personal Alignment (0-13)

**Đo cái gì:** Honest assessment khả năng sustain 2 năm + access audience + có gì để dạy.

**Bắt buộc honest — đây là dimension dễ tự lừa nhất.**

### 7a. Expertise (max 5)
| Pts | Level |
|---|---|
| 5 | Đã làm professionally 2+ năm, có result/portfolio show được |
| 3 | Intermediate 6-12 tháng, có ít evidence |
| 1 | Beginner passionate learner |
| 0 | Zero experience |

### 7b. Sustainability (max 5)
| Pts | Level |
|---|---|
| 5 | Deep passion, sustain 2+ năm dễ kể cả không kiếm tiền nhiều |
| 3 | Strong interest, sustain 1-2 năm |
| 1 | Moderate, sẽ chán sau 6 tháng nếu không profit |
| 0 | Pure tactical opportunity |

### 7c. Network Access (max 3)
| Pts | Level |
|---|---|
| 3 | Direct access target audience (đã có followers/list cùng niche) |
| 2 | Indirect (adjacent space) |
| 0 | Zero network |

**Self-honesty check:** Nếu không trả lời được "Tại sao là TÔI làm niche này thay vì ai khác?" trong 30 giây → Personal Alignment max 7.

---

## Decision Tiers (unchanged)

| Total | Verdict | Action |
|---|---|---|
| **80-100** | Strong Go | Allocate resource, fast-track — vẫn nên qua WTP smoke test |
| **60-79** | Solid Go | **Bắt buộc** WTP smoke test gate + 10 customer interview trước >5M spend |
| **40-59** | Marginal | Chỉ proceed nếu Personal Alignment ≥10 AND Channel-Market Fit ≥10, hard milestone + falsification |
| **<40** | Pass | Quay lại Phase 1 |

---

## Worked Example: "AI tools cho freelance writer VN" (re-scored với rubric 7-dim)

(Hypothetical scoring với data gather giả định 2026-05-17)

### 1. Problem Severity → **11/15**

Evidence:
- Reddit r/vietnam + Spiderum + FB group freelance writer: 15+ post chứa pain "khách bỏ vì ChatGPT làm được rồi", "rate bị ép xuống 50K/bài"
- 2 failed solution visible: thử upskill SEO không cứu (vẫn bị AI replace), thử pivot copywriting cũng bão hoà
- Frequency: post xuất hiện weekly cluster
- Urgency cao (income loss thực tế ≤12 tháng gần)
- 11 pts (cao nhưng chưa max do chưa thấy stated WTP cụ thể cho solution AI-leveraging)

### 2. WTP & Unit Economics → **14/20**

- 2a Direct paid: Unica top course "AI viết content" 1.2K enrolled → 6 pts
- 2b Net margin: nếu sell own site + organic 80% net, nếu Unica 45% net. Giả định mix → 4 pts
- 2c LTV/ladder: course 990K → upsell coaching 5M khả thi, community 199K/tháng khả thi → 3 pts
- 2d Price-match: 3 competitor tier 700K-1.2M có traction → 1 pt (phải verify trong run thật)

### 3. Search Demand → **9/12**

- "AI viết content" primary VN ~3K/tháng + portfolio Vi+En ~12K → tier 9 pts

### 4. Trend & Timing → **7/10**

- Google Trends VN rising +200% past 2 năm
- Adoption position: ở Early Adopter → Early Majority transition (chasm crossing). Mass audience starting to adopt.
- Discount nhẹ vì AI hype có fad risk → 7 pts

### 5. Competition & Defensibility → **8/15**

- 5a Sweet spot: Unica 8 active course, FB Ads ~15 advertiser, gap rõ "freelance writer keeping clients in AI age" → 7 pts
- 5b Defensibility: user có 8K FB follower (~1 pt audience trust); không có insider data/IP → 1 pt
- Total: 8

### 6. Channel-Market Fit → **11/15**

- 6a Audience concentration: freelance writer VN tập trung FB group + Spiderum + Threads → 4 pts
- 6b Creator fit: user 2 năm content + 8K FB → 5 pts native FB
- 6c CAC viability: organic FB heavy + light Ads test, LTV (990K + 30% upsell) ~ 1.3M, CAC organic ~0 → ratio strong → 2 pts (chỉ 2 vì paid CAC chưa test)
- Total: 11

### 7. Personal Alignment → **9/13**

- 7a Expertise: 2 năm content writer professional → 3 pts (chưa explicit "expert" AI tools)
- 7b Sustainability: user chưa state passion mức nào → assume 3
- 7c Network: 8K FB cùng niche → 3
- Total: 9

### **Final Score: 11 + 14 + 9 + 7 + 8 + 11 + 9 = 69/100 → Solid Go**

(Bản cũ 5×20 cho 76/100 — bản mới chặt hơn vì calls out Defensibility weak + price-match chưa verify)

**Decision:** Proceed nhưng **bắt buộc** qua WTP smoke test 2 tuần (waitlist 990K với 500 traffic) + 10 customer interview trước khi build full. Pre-mortem trigger: <3% waitlist conversion = kill.

**Top risk (vs bản cũ chỉ nêu "brand competition"):** Defensibility chỉ 1/5 → niche có thể bị clone trong 6 tháng. Cần xây community lock-in (vd private FB group only-for-students) sớm.

---

## Honest-Score Discipline

Sau khi tính, hỏi 4 câu trước khi commit:

1. **"Mỗi điểm có URL/screenshot không?"** Claim không có source — downgrade dimension đó 3 pts.
2. **"Nếu 1 friend skeptical nhìn vào, họ hoài nghi điểm nào nhất?"** Dimension cần re-verify.
3. **"Personal Alignment có bị inflate vì tôi đã commit emotional vào ý tưởng này không?"** Yes → dial down 3 pts.
4. **"Defensibility 0-1 có gì để patch không?"** Nếu score >70 nhưng defensibility 0-1, plan community/IP/data lock-in trước launch.

Score sau honesty pass thường = score thực để decide.
