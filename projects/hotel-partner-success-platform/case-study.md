# PM Case Study — Hotel Partner Success Platform for OTA Marketplace
*Aditi Mishra | B2B Product Strategy, Marketplace Analytics*

---

## 1. Problem Statement

**How might an OTA platform help its hotel partners improve pricing, inventory, and booking performance — reducing partner churn and increasing platform GMV?**

### Context *(Assumption labeled)*

OTAs operate a two-sided marketplace:
- **Demand side**: Travelers searching and booking
- **Supply side**: Hotels listing inventory and setting prices

The supply side is typically under-tooled. Hotels, especially independent and mid-tier properties, lack:
- Real-time competitive pricing intelligence
- A unified view of their marketplace performance
- Proactive operational nudges during demand surges

> **[ASSUMPTION]** Based on analysis of publicly available OTA partner reports (MakeMyTrip, Booking.com partner programs) and hospitality industry research.

**Business Impact of Under-performance**:
- Partners under-price → OTA loses revenue per booking
- Partners leave inventory blocked → Conversion drops for travelers
- Partners churn → OTA must spend to recruit replacements (high CAC)

---

## 2. Stakeholder Analysis

| Stakeholder | Their Goal | Pain with Status Quo |
|---|---|---|
| **Hotel Partner** | Maximize occupancy + revenue | No visibility into competitive pricing; no performance benchmark |
| **OTA Revenue Team** | Maximize GMV + commission | High partner churn; inconsistent inventory quality |
| **OTA Product Team** | Build sticky supply-side tools | Partners use platform passively; low tool engagement |
| **Traveler (end customer)** | Best price + availability | Price inconsistencies; inventory gaps during peak |

---

## 3. Root Cause Analysis

**Why do hotel partners underperform on OTA platforms?**

Using an Issue Tree:
```
Hotel Partner Underperformance
├── PRICING PROBLEMS
│   ├── Hotels don't know competitor pricing in real-time
│   ├── Hotels set prices monthly, not dynamically
│   └── Hotels fear undercutting direct bookings
├── INVENTORY PROBLEMS
│   ├── Rooms blocked for direct bookings during high-demand periods
│   ├── Manual inventory update is tedious
│   └── No alert when inventory is low during peak demand
└── PERFORMANCE VISIBILITY PROBLEMS
    ├── No single health metric to track overall performance
    ├── Partners get piecemeal data (views, bookings) but no synthesis
    └── No benchmarking against similar properties
```

---

## 4. The Three-Component Solution

### Component 1: Dynamic Pricing Dashboard

**Problem**: Hotels set pricing based on gut feel, seasonality guesses, or copy from last year.

**Solution**: A real-time dashboard showing:
- The hotel's current price vs. top 5 competitors in the same category/location
- Demand forecast for next 7/14/30 days (based on OTA search volume)
- Pricing recommendation with projected revenue impact
- One-click price update directly from dashboard

**Key Metrics**:
- Pricing Gap Index: (Hotel price — Median competitor price) / Median competitor price
- Revenue per Available Room (RevPAR) trend vs. platform average
- Price Accept Rate: % of partner price recommendations accepted

---

### Component 2: Partner Health Score

**Problem**: Partners don't know if they're "good" or "bad" performers until they see declining bookings — too late.

**Solution**: A composite score (0–100) updated weekly, visible to partner and OTA account manager.

**Score Dimensions** (weighted):

| Dimension | Weight | Metric |
|---|---|---|
| Pricing Competitiveness | 25% | Pricing Gap Index |
| Inventory Availability | 25% | % rooms available during high-demand periods |
| Response Rate | 20% | Booking inquiry response time (OTA standard: <2 hrs) |
| Guest Review Score | 20% | Avg rating on platform (weighted recent reviews) |
| Content Completeness | 10% | % of listing fields filled (photos, amenities, description) |

**Score Bands**:
- 80–100: Platinum Partner (featured placement, reduced commission)
- 60–79: Gold Partner (standard benefits)
- 40–59: Silver Partner (improvement plan offered)
- Below 40: At-Risk (account manager outreach triggered automatically)

---

### Component 3: Inventory Nudge Engine

**Problem**: Hotel partners block inventory during peak demand periods for direct bookings, causing missed OTA conversions.

**Solution**: An automated alerting and nudge system:
- **Demand Spike Alert**: "Search volume for your dates is 3x normal — you have 2 rooms blocked. Consider opening them"
- **Dead Inventory Alert**: "5 rooms unsold in next 7 days. Suggested price drop: ₹500 (projected +40% booking probability)"
- **Last-Minute Activation**: One-tap to open blocked rooms at dynamic price from mobile notification

---

## 5. Competitive Benchmarking *(Assumption labeled)*

> **[ASSUMPTION]** Based on publicly available product documentation and partner program descriptions.

| Feature | MakeMyTrip | Booking.com | Airbnb | JustMoney OTA Platform |
|---|---|---|---|---|
| Real-time competitor pricing | Partial | Yes (Pulse tool) | Yes | Yes (enhanced) |
| Partner Health Score | No | No | No | **Yes — Unique** |
| Inventory Nudge | Basic alerts | Basic | Smart Pricing | **Yes — Proactive** |
| Mobile partner app | Yes | Yes | Yes | Yes |
| Revenue impact modeling | No | Partial | No | **Yes** |

**Differentiation**: Health Score is the unique differentiator — no major OTA currently offers a composite partner wellness metric.

---

## 6. Prioritization (2x2 Impact-Effort Matrix)

```
HIGH IMPACT
    │
    │  Dynamic Pricing     Partner Health
    │  Dashboard ✓         Score ✓
    │  (Must Build)        (Must Build)
    │
    │                      Inventory Nudge ✓
    │                      (Must Build)
    │
    │  AI Demand           Revenue
    │  Forecasting         Attribution
    │  (Future)            (Future)
LOW IMPACT
    LOW EFFORT ────────────────── HIGH EFFORT
```

All three core components fall in "High Impact, Manageable Effort" quadrant.

---

## 7. Business Case *(Assumption labeled)*

> **[ASSUMPTION]** Illustrative financials based on OTA industry benchmarks.

| Metric | Baseline | With Platform | Improvement |
|---|---|---|---|
| Partner Churn Rate | 20% annually | 14% annually | -30% |
| Avg Booking Value (per partner) | ₹2.4L/month | ₹3.1L/month | +29% |
| Platform GMV Impact (100K partners) | — | +₹700 Cr/year | Significant |
| Partner Pricing Competitiveness | 62% within market range | 81% within market range | +19pp |

**ROI Justification**: Engineering investment to build the platform estimated at ₹8–10 Cr. GMV impact of ₹700 Cr = 70x+ ROI in Year 1.

---

## 8. Implementation Roadmap *(Assumption labeled)*

| Phase | Timeline | Deliverables |
|---|---|---|
| Discovery & Design | Month 1–2 | Partner research (50 interviews), UX wireframes |
| MVP Build | Month 3–5 | Pricing Dashboard + basic Health Score |
| Beta Launch | Month 6 | 500 partner beta, feedback loops |
| Full Launch | Month 7–8 | Nudge Engine, all features, 10,000 partners |
| Optimization | Month 9–12 | ML demand forecasting, personalized nudges |

---

## 9. Key Learnings

1. **B2B products succeed when they show partners their ROI** — the Health Score makes the value proposition tangible
2. **Proactive nudges > reactive reporting** — telling a partner what to do is more valuable than showing what happened
3. **Marketplace health is supply-side health** — fixing supply unlocks demand
4. **Data moats compound** — more partners using the pricing dashboard = better data = better recommendations = stickier tool

---

*See also: strategy.md, metrics.md, prd.md, star-stories.md*
