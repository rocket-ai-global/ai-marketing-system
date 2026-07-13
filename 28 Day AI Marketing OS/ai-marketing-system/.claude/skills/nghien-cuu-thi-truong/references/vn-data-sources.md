# Vietnamese Demand-Side Data Sources

Nguồn data cụ thể để đo demand cho digital product / service ở thị trường Việt Nam. Mỗi nguồn có: cách truy cập, search template, threshold đọc tín hiệu strong/weak.

## 1. Search Volume + CPC (Google Keyword Planner)

**URL:** `ads.google.com` → Tools → Planning → Keyword Planner → Discover new keywords

**Setup:**
- Tạo Google Ads account free (không cần đặt budget thật)
- Location: Vietnam | Language: Vietnamese + English (cả 2)

**Search VN tips:**
- VN audience search bằng cả tiếng Việt + tiếng Anh — luôn check cả 2
- VD: "khóa học AI" + "AI course" cùng 1 niche, volume add lại
- Cẩn thận với typo/no-tone phổ biến: "khoa hoc" cũng có volume

**Đọc volume (monthly):**

| Range | Ý nghĩa | Action |
|---|---|---|
| <500 | Micro-niche, hoặc không demand | Verify với marketplace; thường pass |
| 500-5K | Sweet spot cho solopreneur VN | Target zone, dễ rank |
| 5K-50K | Mid-market, có competition | Cần differentiation rõ |
| >50K | Mass market | Solo khó chiếm share, cần ngách hẹp |

**Đọc CPC (VND, không phải USD):**

| CPC | Commercial intent | Suggested action |
|---|---|---|
| <2K VND | Informational, hobby | Hard to monetize directly |
| 2K-10K VND | Moderate buy intent | OK cho course tier <1M |
| 10K-50K VND | Strong buy intent | Target cho course 1M+ / coaching |
| >50K VND | High-ticket / B2B | Premium positioning needed |

**Đọc Competition:**
- Low = ít advertiser bid → có thể demand yếu HOẶC B2B sales-cycle dài
- Medium = healthy demand + room for entry (zone vàng)
- High = đã saturated, vào phải có moat

## 2. Google Trends (Region: Vietnam)

**URL:** `trends.google.com` → set region: Vietnam

**Workflow:**
1. Compare 3-5 keyword cùng lúc (1 primary + 2-4 variant)
2. Time range: Past 5 years (trend direction) + Past 12 months (seasonality)
3. Check "Related queries" → tab "Rising" → tìm breakout keyword (+150% trở lên)

**Đọc signal:**

| Pattern | Verdict |
|---|---|
| Steady ↑ over 2+ năm | **Pursue** — trend bền |
| Spike rồi giữ baseline cao | **Pursue** — đã establish |
| Flat nhưng volume cao | **OK** — evergreen, cần differentiate |
| Spike rồi tụt về 0 | **Avoid** — fad đã qua |
| Steady ↓ | **Avoid** — dying |

**Seasonality (Past 12 months):**
- Ratio = Peak / Average
- >3x → time-sensitive, launch 2 tháng trước peak
- 1.5-3x → optimize cho peak, year-round content
- <1.5x → evergreen

## 3. Marketplace Course Platforms (VN-specific)

| Platform | Đặc điểm | Cách read sales |
|---|---|---|
| **unica.vn** | Course platform lớn nhất VN, mass market | Page course hiển thị "X học viên", review count, rating |
| **edumall.vn** | Cạnh tranh trực tiếp Unica | Same format, kiểm tra "Đã có X học viên đăng ký" |
| **gitiho.com** | Tech/business courses, mid-tier pricing | Hiển thị enrolled count + rating |
| **kyna.vn** | Skill courses, soft skill nhiều | Số học viên + review |
| **funix.edu.vn** | Tech focused (programming, AI) | Course pages hiển thị batch + cohort |
| **hocmai.vn** | K-12 + thi cử | Volume cao cho exam prep, market khác biệt |
| **topica.edu.vn** | English + business, premium | Pricing cao, ít course count public |

**Query template cho mỗi platform:**

```
"$NICHE site:unica.vn"
"$NICHE site:edumall.vn"
"$NICHE site:gitiho.com"
"$NICHE site:kyna.vn"
```

**Đọc tín hiệu (per top course):**

| Metric | Strong | Weak |
|---|---|---|
| Học viên (enrolled) | 500+ trên 1 course | <100 |
| Rating | 4.3+ với 50+ review | <4.0 hoặc <10 review |
| Price | 500K-3M VND tier hợp lý | <100K (commodified) hoặc >5M (niche premium) |
| Top course date | <12 tháng | >24 tháng (stale) |
| Số course trong niche | 5-30 | <3 (no market) hoặc >100 (saturated) |

**Content gap analysis:**
- Đọc review 1-2 sao của top course → recurring complaint = opportunity
- Check curriculum syllabus → missing topic = differentiation angle

## 4. Shopee / Tiki / Lazada (E-commerce)

**Khi nào dùng:** Niche có physical product hoặc digital product được sell qua marketplace (ebook, template, tool license).

**Workflow Shopee:**
1. `shopee.vn` → search keyword → filter "Đã bán nhiều nhất"
2. Top 20 listing → ghi: tên seller, "Đã bán X", giá, rating, review count
3. Filter "Có voucher 50%+" → indicator competition intense

**Đọc tín hiệu:**

| Metric | Strong demand | Weak |
|---|---|---|
| Tổng product listing | 100-500 trong category | <20 (niche too small) |
| Top seller "Đã bán" | 1K+ (12 tháng) | <100 |
| Rating top | 4.5+ với 100+ review | <4.0 |
| Price range | 100K-2M tier rõ | <50K (race to bottom) |
| Recent reviews (30 ngày) | 10+ trên top seller | <3 |

## 5. Facebook Community Signal

### 5a. FB Groups

**Query:** `facebook.com/search/groups/?q=$NICHE vietnam` hoặc Google `"$NICHE" facebook group vietnam`

**Đọc tín hiệu:**

| Metric | Strong | Weak |
|---|---|---|
| Số group active | 5+ với 1K+ thành viên mỗi cái | <2 hoặc tổng <500 |
| Post frequency | Daily posts trong top 3 group | Weekly hoặc ít hơn |
| Engagement | 10+ comments trên top posts | <3 comments |
| Buying signal | "Ai biết mua ở đâu", "tư vấn", "review" | Chỉ sharing content, không hỏi mua |

### 5b. FB Ads Library

**URL:** `facebook.com/ads/library` → Country: Vietnam → search keyword/competitor page name

**Đọc tín hiệu:**

| Metric | Strong | Weak |
|---|---|---|
| Active ads cho keyword | 20+ ads đang chạy | <5 |
| Ad duration | Nhiều ads >30 ngày | All ads <7 ngày (testing chứ chưa scale) |
| Distinct advertisers | 10+ brand khác nhau | 1-2 brand độc chiếm |
| Creative variants | Multiple angle (pain/gain/social proof) | Monoculture (chỉ 1 angle) |

**Diagnose ad longevity:** Nếu ad chạy >30 ngày = đang profitable = niche monetizable.

## 6. TikTok / YouTube Volume

### 6a. TikTok hashtag

**Query Google:** `"#$NICHE" tiktok view count` hoặc check `tiktok.com/tag/$NICHE`

| Hashtag views | Verdict |
|---|---|
| 10K-100K | Micro-community, engaged nhưng nhỏ |
| 100K-1M | Active niche, good cho VN solopreneur |
| 1M-10M | Established, cần differentiate |
| >10M | Mainstream, hard mass appeal |

### 6b. YouTube

**Query:** `"$NICHE" tiếng việt site:youtube.com`

**Đọc tín hiệu:**
- Small channel (<10K subs) getting 50K+ views = **strong demand** (algorithm boost = topic hot)
- Top channels view/sub ratio >1.0 = interest cao
- Upload frequency mỗi tuần ở top channel = topic sustained

## 7. Reddit / Quora / VN Forum

**Query:**
```
"$NICHE site:reddit.com"
"$NICHE site:reddit.com/r/vietnam"  (specifically VN sub)
"$NICHE site:vozforums.com"          (tech-leaning VN forum)
"$NICHE site:tinhte.vn"              (tech VN community)
```

**Mục đích:** Pain point + sentiment language. Copy verbatim 10 questions/complaints để dùng làm:
- Audience language cho copy/headline
- Pain mapping (link sang `vpd-customer-profile-builder`)
- Frequency analysis (pain nào lặp lại nhiều = severity cao)

## 8. Competitor Pricing & Positioning

**Workflow:**
1. List 3-5 direct competitor identified trong Step 1-3
2. WebFetch landing page mỗi competitor → extract: pricing tier, bonus stack, guarantee, positioning angle, ICP
3. Build comparison table

**Output format:**

```markdown
| Competitor | URL | Price | Positioning | ICP | Bonus stack | Guarantee | Strength | Gap |
|---|---|---|---|---|---|---|---|---|
| ... | ... | ... | ... | ... | ... | ... | ... | ... |
```

**Pricing pattern VN digital course (2026 benchmark):**
- Tripwire / low ticket: 99K-499K
- Core (course solo, no coaching): 499K-2M
- Premium (course + group coaching): 2M-10M
- Mastermind / 1-1: 10M-50M+

## 9. Source Quality Hierarchy

Khi triangulate, không phải source nào cũng nặng ký bằng nhau:

| Tier | Source type | Trust weight |
|---|---|---|
| **A — Direct evidence** | Marketplace sales count, FB Ads Library active ads, course platform enrollment | 1.0 |
| **B — Behavioral data** | Google Trends, Keyword Planner volume, hashtag views | 0.7 |
| **C — Stated preference** | Forum questions, FB group discussions, survey | 0.4 |
| **D — News/analyst** | Industry report, news article, blog estimate | 0.3 |

**Rule:** Cần ≥1 source Tier A cho mỗi major claim (demand exists, willing to pay, competition density). Tier B/C/D chỉ làm supporting evidence.

## Additional VN-specific Sources (added 2026-05-17)

### 1b. Coccoc Keyword Tool (cross-check Google Planner)

**URL:** `coccoc.com` → search bar có suggest, hoặc dùng API ads của Coccoc nếu cần exact volume.

**Tại sao quan trọng:** Coccoc giữ ~8-12% market share search VN, đặc biệt mạnh ở demo 35+ và non-tech user. Volume Coccoc có thể bù cho gap mà Google Planner under-report cho niche "older-skewing" (parenting, finance, traditional health, môi giới BĐS).

**Cách dùng:**
- Type primary keyword → đọc suggest list (semantic siblings)
- Compare với Google search suggest → tìm keyword chỉ xuất hiện ở Coccoc = signal demo Coccoc-skewed
- Nếu Coccoc suggest cho keyword nhiều variant hơn Google → niche của bạn skew sang demo 35+

**Threshold:** Nếu niche target audience 35+ và Coccoc suggest list >2x Google suggest list → đây là tín hiệu strong (rare nhưng valuable cho VN-only niche).

### 5c. Zalo OA + Zalo Group Signal

**Tại sao quan trọng:** Zalo là kênh chat dominant VN, đặc biệt cho demo 35+ và buyer journey high-touch (BĐS, bảo hiểm, khóa học cao tier, B2B SMB). Skipping Zalo = miss demand signal cho 60% audience VN >35 tuổi.

**Cách lấy data:**

| Tool | URL | Lấy gì |
|---|---|---|
| Zalo OA Discovery | `oa.zalo.me` (cần Zalo Business account) | Search OA theo keyword → đếm OA cùng niche + follower count + post engagement |
| Zalo Mini App | `zalo.me/mini-apps` directory | Tools/apps existing cho niche |
| Zalo Group (semi-public) | Search trong Zalo app theo keyword | Khó scrape, manual observe group public |

**Đọc tín hiệu:**

| Metric | Strong | Weak |
|---|---|---|
| OA cùng niche | 5+ active OA với 5K+ follower mỗi cái | <2 OA hoặc dead OA |
| OA post frequency | Weekly content, response rate >50% | Monthly hoặc dead |
| Mini App existing | 1-2 quality mini app trong niche | None (dấu hiệu niche chưa chín cho Zalo) |

**Quan trọng:** Niche skill này (digital course/digital product) thường KHÔNG cần check Zalo nặng — Zalo signal mạnh cho high-touch niche. Nếu target audience <30 tuổi tech-savvy → skip Zalo, dồn vào TikTok + FB.

### 6c. TikTok Creative Center VN (ad reverse-engineer)

**URL:** `ads.tiktok.com/business/creativecenter` → Top Ads → filter Region: Vietnam

**Tại sao quan trọng:** Top performing ads VN trên TikTok = đang convert được. Reverse-engineer creative angle + hook + CTA + offer structure của top advertiser trong niche của bạn.

**Cách dùng:**
1. Filter Region: Vietnam, Industry: relevant industry (Education / E-commerce / Beauty / Finance...)
2. Sort by "CTR" hoặc "Impressions" → top 20 ads
3. Watch + note: hook 3s đầu, structure (problem-solution-CTA / before-after / listicle), CTA wording, offer hint
4. Filter "Liked" + duration ≥30 days = sustained winner

**Đọc tín hiệu:**

| Metric | Strong | Weak |
|---|---|---|
| Top ad số lượng VN trong niche | 10+ ads ≥30 days run | <3 ads hoặc all <7 days (still testing) |
| Creative diversity | Multiple angle (pain / dream / proof) | Monoculture (chỉ 1 angle) — niche chưa optimize |
| Top creator type | Mix of brand + individual creator | Only big brand (solo khó cạnh tranh) |

**Bonus:** TikTok Creative Center có "Top Products" cho e-commerce + "Top Songs" cho viral hook → reverse-engineer thêm.

### 7b. Spiderum + Vietcetera (premium content audience)

**Tại sao quan trọng:** 2 platform này là proxy cho VN audience "willing to pay for thoughtful content" — đối lập với mass FB/TikTok. Niche của bạn target tier 1-5M course / coaching thì audience của bạn đọc 2 platform này.

| Platform | URL | Đọc gì |
|---|---|---|
| **Spiderum** | spiderum.com | Long-form post engagement (comment, share), tag/keyword cloud, top author trong niche |
| **Vietcetera** | vietcetera.com | Editorial content, audience demo skew (Gen Z + Millennial urban, đi làm văn phòng) |

**Đọc tín hiệu:**

| Metric | Strong | Weak |
|---|---|---|
| Số article Spiderum cho keyword | 5+ articles >1K view + healthy comment | <2 articles |
| Author/community trong niche | 2-3 active author build readership | None (niche chưa được "intellectualize") |
| Vietcetera coverage | Có series/topic về niche | None |

**Use case điển hình:** Niche "AI productivity cho người đi làm" — check Spiderum có 10+ article ≥2K view + Vietcetera có series về AI tools = audience tier 1-3M tồn tại + sẵn sàng đọc dài + sẵn sàng trả tiền cho insight.

---

## 10. Quick 2-hour Sprint Protocol

Khi cần validation nhanh, không phải full research:

**Hour 1 — Signal scan:**
- 15min: Keyword Planner volume + CPC cho 5-10 variant keyword
- 15min: Google Trends VN, 5-year direction + 12-month seasonality
- 15min: Unica + Edumall + Gitiho top 5 course (enrolled, price, rating)
- 15min: FB Ads Library active ads (count + duration)

**Hour 2 — Score & decide:**
- 20min: FB group + TikTok hashtag check
- 20min: Top 3 competitor positioning + pricing
- 20min: Score 100 + recommendation

**Output:** Decision với 70% confidence. Dùng cho filter trước khi full research top 1-2 candidate.
