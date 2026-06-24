# Marketing Performance Analysis – DTC Fitness Supplements Brand

A data analytics project analyzing 3 months of multichannel marketing performance data (Jan–Mar 2024) for a DTC fitness supplements brand spending $1.6M/month across Facebook, Google, and TikTok — with an overall ROAS of 0.87, well below the 1.2 target.

---

## Problem Statement

The brand faced a critical performance crisis:
- ROAS declining week-over-week from **1.48 in January to 0.48 by March**
- No clarity on which platforms, creatives, or regions were driving value
- Need to **cut 30% of spend** while growing revenue by 40% next quarter

---

## Tools & Technologies

| Area | Tools |
|---|---|
| Data Cleaning & Analysis | Python, Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Dashboard | Power BI |
| Presentation | PowerPoint |

---

## Dataset Overview

- **3,240 raw rows** → 2,982 rows after cleaning
- **3 Platforms:** Facebook, Google, TikTok
- **4 Regions:** West, Northeast, South, Midwest
- **9 Campaigns**, **5 Creative Types**, **4 Product Categories**

### Data Quality Issues Addressed

| Issue | Action Taken |
|---|---|
| 20 missing Revenue values | Filled with zero |
| 2,012 missing VCR values | Left null (video-only metric) |
| 147 rows with zero clicks | CVR and CPC set to zero |
| 6 extreme spend outliers (>$59K) | Removed |

### Derived Metrics

```
CTR  = Clicks / Impressions
CPC  = Spend / Clicks
CVR  = Purchases / Clicks
ROAS = Revenue / Spend
```

---

## Key Findings

### Platform Performance
| Platform | ROAS | Notes |
|---|---|---|
| Google | 0.91 | Best performer, prioritize for scaling |
| TikTok | 0.91 | Highest spend ($1.87M), not yet profitable |
| Facebook | 0.75 | Worst performer, losing 25¢ per dollar spent |

### Creative Type Performance
| Creative | ROAS |
|---|---|
| Search | 1.12 ← only format near target |
| Video | 0.92 |
| Carousel | 0.72 |
| Display | 0.66 |
| Image | 0.62 |

> Search is **1.9x more efficient** than Display.

### Product Category Performance
| Category | ROAS |
|---|---|
| Protein | 1.08 |
| Diet | 0.91 |
| Weight Loss | 0.67 |
| Pre-workout | 0.53 |

### Regional Performance
- **West & Northeast** are highest-performing regions
- **Midwest** significantly underperforms — candidate for budget reallocation

### Ad Fatigue Analysis
- Average frequency: **3.0** | Maximum: **7.78**
- CVR drops significantly when frequency exceeds **4**
- Facebook ROAS collapsed to **0.47** in March — driven by ad fatigue, not product issues

### Competitive Events Impact
- ROAS during normal periods: **~0.88**
- ROAS during competitor promotion events: **~0.80**
- Brand is **not winning bidding wars** during competitive events

---

## Recommendations

### Immediate (Week 1–2)
- Kill Display and Image campaigns for Pre-workout (~$1M+ spend with ROAS 0.53)
- Cap Facebook ad frequency at **3 impressions/user/week**
- Shift budget toward Google Search (massively underinvested at 1.12 ROAS)
- **Reduce bids 20–30% on competitive event dates**, surge the day after

### A/B Tests Proposed

| Test | Hypothesis | Expected Impact |
|---|---|---|
| Search vs Display for Pre-workout | Failure is format, not product demand | +$350K revenue |
| Frequency capping on Facebook | Ad fatigue, not bad product, is killing ROAS | +$219K revenue |
| DR Video vs Awareness Video on TikTok | High VCR ≠ high CVR; DR creative converts better | +$355K revenue |

**Total projected upside: ~$924K**

### Long-Term Budget Reallocation
- **Northeast:** 35% ↑ (from 26%)
- **South:** 25% (maintain)
- **West:** 22% ↓ (from 27%)
- **Midwest:** 18% ↓ (from 21%)

---

## Expected Impact

| Metric | Value |
|---|---|
| Budget freed from cuts | ~$1.6M |
| Revenue upside from A/B wins | ~$924K |
| Target ROAS end of Q2 | 1.1+ (from 0.87) |

---

## Project Structure

```
├── analysis/
│   └── marketing_analysis.ipynb   # Data cleaning + EDA + KPI derivation
├── dashboard/
│   └── marketing_dashboard.pbix   # Power BI dashboard
├── presentation/
│   └── AJMedia_PPT.pdf            # Executive presentation (14 slides)
└── README.md
```
