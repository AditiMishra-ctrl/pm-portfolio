# KPI Framework & Metrics — JustMoney
*Aditi Mishra | Product Analytics*

---

## North Star Metric

**Weekly Engaged Users (WEU)** — users who complete at least one meaningful financial action per week (check dashboard, update goal, log a transaction, or act on a nudge).

*Why this metric*: JustMoney succeeds only if it becomes a weekly financial habit, not a one-time download. WEU captures genuine behavior change, not vanity installs.

---

## Metric Tree

```
NORTH STAR: Weekly Engaged Users (WEU)
│
├── ACQUISITION
│   ├── App Downloads (daily/weekly)
│   ├── Organic Install Rate (vs. paid)
│   ├── Referral Coefficient (K-factor)
│   └── Cost Per Install (CPI)
│
├── ACTIVATION
│   ├── Onboarding Completion Rate (%)
│   ├── Bank/UPI Link Rate (%)
│   ├── Time to First Dashboard View
│   └── Day-1 Goal Created (%)
│
├── ENGAGEMENT (Core)
│   ├── D7 / D30 Retention (%)
│   ├── Sessions per Week per User
│   ├── Nudge Click-Through Rate (%)
│   └── Goal Update Frequency
│
├── TRUST
│   ├── Bank Link Adoption Rate (% of users)
│   ├── Privacy Explainer Read Rate (%)
│   ├── Support Ticket Rate (negative)
│   └── CSAT (monthly survey)
│
└── MONETIZATION
    ├── Free → Premium Conversion Rate (%)
    ├── Average Revenue Per User (ARPU)
    ├── Monthly Recurring Revenue (MRR)
    └── LTV:CAC Ratio
```

---

## Key Metrics with Targets

### Acquisition

| Metric | Definition | Month 3 Target | Month 12 Target |
|---|---|---|---|
| MAU | Monthly Active Users | 10,000 | 100,000 |
| Organic Install % | Installs without paid ads | 60% | 70% |
| Referral K-factor | Avg referrals per user | 0.3 | 0.5 |
| CPI (if paid) | Cost per install | <₹40 | <₹30 |

### Activation

| Metric | Definition | Target |
|---|---|---|
| Onboarding Completion | % who complete onboarding | >75% |
| Bank Link Rate | % who link bank by Day 7 | >40% |
| First Goal Created | % who create a goal in Day 1 | >50% |
| Time to Value | Time from install to first dashboard view | <3 minutes |

### Engagement & Retention

| Metric | Definition | Target |
|---|---|---|
| D7 Retention | % who return on Day 7 | >45% |
| D30 Retention | % who return on Day 30 | >35% |
| Sessions/Week | Avg sessions per active user | ≥3 |
| Nudge CTR | % who act on monthly spend nudge | >20% |
| Goal Completion Rate | % who hit a savings goal | >25% by Month 6 |

### Trust

| Metric | Definition | Target |
|---|---|---|
| CSAT | Post-onboarding survey score | ≥4.2/5.0 |
| Bank Link Adoption | % who link (not just UPI) | 55% by Month 3 |
| Uninstall Rate | D30 uninstall rate | <30% |
| Support Tickets | Per 1000 MAU | <15 |

### Monetization *(Assumption)*

| Metric | Definition | Target |
|---|---|---|
| Free→Premium Conv. | % who upgrade | 12% by Month 12 |
| ARPU | Blended avg revenue per user | ₹35/month |
| MRR | Monthly recurring revenue | ₹35L by Month 12 |
| LTV:CAC | Customer lifetime value / acquisition cost | >3:1 |

---

## A/B Testing Roadmap

### Test 1: Trust Explainer Placement
- **Hypothesis**: Showing privacy explainer *before* bank-link CTA increases bank-link rate
- **Control**: Standard bank-link screen
- **Treatment**: Privacy explainer card shown first
- **Primary Metric**: Bank Link Rate (Day 7)
- **Sample Size**: 1,000 users per variant
- **Expected Lift**: +15% bank link rate

### Test 2: Nudge Message Language
- **Hypothesis**: Hindi nudge messages generate higher CTR than English
- **Control**: English nudge ("You spent ₹4,200 on food")
- **Treatment**: Hindi nudge ("इस महीने खाने पर ₹4,200 खर्च हुए")
- **Primary Metric**: Nudge CTR
- **Expected Lift**: +25% CTR

### Test 3: Goal Bucket UI Style
- **Hypothesis**: Visual "jar" animation for goal buckets drives higher goal completion
- **Control**: Progress bar
- **Treatment**: Animated money jar filling up
- **Primary Metric**: Goal Creation Rate (Day 1) + D30 Goal Retention
- **Expected Lift**: +20% goal creation

---

## Funnel Analysis Framework

```
INSTALL
  ↓ [Target: 80% proceed]
ONBOARDING STEP 1 (Phone number + OTP)
  ↓ [Target: 90% complete]
ONBOARDING STEP 2 (Language selection)
  ↓ [Target: 85% complete]
ONBOARDING STEP 3 (Privacy explainer)
  ↓ [Target: 70% proceed to link]
BANK/UPI LINK
  ↓ [Target: 60% link at least UPI]
DASHBOARD VIEW (First time)
  ↓ [Target: 90% of linked users]
GOAL CREATION (Day 1)
  ↓ [Target: 50% of dashboard viewers]
WEEK 1 RETURN (D7)
  [Target: 45%]
```

**Current drop-off hypothesis**: Biggest drop at Bank Link step (trust barrier). That's why "Try without bank" mode is critical.

---

## Dashboard Mockup Description
*(See assets/dashboard-mockup.html for interactive version)*

**Home Screen Cards (Priority Order)**:
1. Total Balance (large, prominent)
2. This Month's Spending vs. Last Month
3. Goal Progress (top 2 goals)
4. Upcoming EMIs (next 7 days)
5. Monthly Nudge Card (animated)

---

*See also: case-study.md, prd.md, gtm.md*
