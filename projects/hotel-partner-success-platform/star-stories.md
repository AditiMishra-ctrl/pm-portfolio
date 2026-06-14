# STAR Stories & Interview Pitches — Hotel Partner Success Platform
*Aditi Mishra | Interview Preparation*

---

## 30-Second Pitch

"I analyzed why hotel partners on OTA platforms underperform and churn — and found the root cause was lack of real-time intelligence, not motivation. I designed a three-component Partner Success Platform: a Dynamic Pricing Dashboard, a composite Partner Health Score (0–100), and an Inventory Nudge Engine. The framework targets a 30% reduction in partner churn and a 29% lift in average booking value per partner — which at scale translates to hundreds of crores in incremental OTA GMV."

---

## 60-Second Pitch

"OTAs are two-sided marketplaces. Most product investment goes to the demand side — traveler search, recommendation, UX. The supply side — hotel partners — is chronically under-tooled. I identified this gap and designed a Hotel Partner Success Platform.

The platform has three components. First, a Dynamic Pricing Dashboard that shows hotels their pricing vs. competitors in real-time with demand forecasts. Second, a Partner Health Score — a composite 0–100 metric across pricing, inventory, response rate, reviews, and content quality. No major OTA currently has this. Third, an Inventory Nudge Engine that proactively alerts partners when demand spikes or inventory is sitting dead.

The business case is strong: a 30% reduction in partner churn at 100,000 partners translates to an estimated ₹700 Cr incremental GMV annually. And the Health Score creates a data flywheel — better data, better recommendations, stickier tools."

---

## 2-Minute Deep Dive

"Let me walk you through the Hotel Partner Success Platform project.

**The Context**: Online travel is a two-sided marketplace. I noticed that OTAs invest heavily in consumer-facing products but have relatively thin tooling for hotel partners — the supply side. Bad partner tooling means bad pricing, blocked inventory, and partner churn. All of which kill GMV.

**The Problem I Defined**: Hotel partners lack three things — real-time pricing intelligence, a unified performance metric, and proactive operational nudges. Without these, they make decisions on gut feel and fall behind.

**The Framework**: I designed a three-component solution.

Component 1 — Dynamic Pricing Dashboard: Real-time comparison of a hotel's price vs. top 5 competitors in the same category, combined with 30-day demand forecasts based on OTA search volume. One-click price updates. Partners can see their revenue impact before changing price.

Component 2 — Partner Health Score: A composite 0–100 score across 5 dimensions — pricing competitiveness (25%), inventory availability (25%), response rate (20%), review score (20%), and listing content completeness (10%). This gives partners a single, actionable metric. No major OTA currently has this.

Component 3 — Inventory Nudge Engine: Proactive alerts when demand surges or inventory is sitting dead. 'Search volume is 3x — you have 2 rooms blocked. Open them?' One-tap reactivation from mobile.

**The Business Case**: Industry data suggests partner churn runs at 18–22% annually. A 30% reduction in churn plus improved pricing competitiveness projects to ~₹700 Cr incremental GMV annually for a mid-size OTA. Against an estimated ₹8–10 Cr platform build cost, the ROI is compelling.

**What I'd measure**: Partner Health Score distribution over time (goal: shift more partners into 60+ tier), pricing gap index, partner churn rate, and OTA GMV per active partner."

---

## STAR Story — Problem Framing

**Situation**: While analyzing OTA marketplace dynamics as part of a business analytics project, I identified that most OTA product investment focuses on the demand side (traveler UX, search algorithms), while the supply side (hotel partners) receives significantly less tooling support.

**Task**: Frame the supply-side problem clearly, identify the root causes of partner underperformance, and design a product solution that would improve marketplace health for the OTA business.

**Action**:
- Conducted structured market research on OTA partner programs (MakeMyTrip, Booking.com, Airbnb)
- Built an issue tree identifying 3 root cause categories: pricing, inventory, and visibility
- Designed a three-component framework (Pricing Dashboard, Health Score, Nudge Engine)
- Developed a business case with estimated GMV impact and ROI calculation
- Created a composite Health Score model with 5 weighted dimensions

**Result**: A comprehensive B2B product strategy with a quantified business case (estimated ₹700 Cr GMV impact), a phased implementation roadmap, and a differentiated Health Score feature with no direct competitor equivalent.

---

## Consulting Interview Version

**Issue Tree Structure**:
```
How should an OTA improve hotel partner performance?
├── Improve pricing competitiveness
│   ├── Real-time market intelligence (Dynamic Pricing Dashboard)
│   └── Demand forecasting integration
├── Improve inventory availability
│   ├── Proactive nudges during demand surges (Nudge Engine)
│   └── Reduce friction for inventory updates
└── Improve partner retention
    ├── Composite health metric for early warning (Health Score)
    └── Tiered partner program with differentiated benefits
```

**Recommendation**: Prioritize Health Score + Pricing Dashboard for Phase 1 — highest ROI, minimum viable supply-side intervention.

---

## PM Interview Q&A

**Q: Why build a Health Score instead of just surfacing individual metrics?**

"Individual metrics create noise. If a partner has to check 5 different dashboards, they optimize for the one they understand best and ignore the others. A composite score forces a holistic view — and more importantly, it creates a clear call-to-action. A partner with a score of 45 knows they're at-risk. A partner with a score of 78 knows they're one step from Platinum. That clarity drives behavior change more effectively than raw data."

**Q: How would you prevent partners from gaming the Health Score?**

"Good question — any scoring system can be gamed. Mitigations: (1) Weight metrics based on business outcomes, not easily manipulated inputs — e.g., 'guest review score' is hard to fake; 'response rate' is auto-tracked by the system; (2) Audit dimension weights quarterly and adjust if gaming patterns emerge; (3) Include at least 2 metrics that require genuine marketplace behavior (like actual bookings received) to score well."

**Q: How is this different from Booking.com's Pulse tool?**

"Booking.com's Pulse gives pricing intelligence — that's one dimension. Our differentiation is the Health Score — a composite metric across 5 dimensions that no major OTA currently offers. Second differentiator is the Nudge Engine's proactivity — we push the insight to the partner, rather than waiting for them to check a dashboard. Behavioral design principle: reduce the 'action gap' between insight and behavior."

---

## Resume Bullets

**Enhanced PM Version**:
- Designed a B2B Hotel Partner Success Platform for OTA marketplaces, addressing supply-side performance gaps that drive 18–22% annual partner churn and reduce marketplace GMV
- Developed a three-component framework: Dynamic Pricing Dashboard (real-time competitive intel + demand forecasting), Partner Health Score (composite 0–100 metric across 5 dimensions — first-of-kind for OTA sector), and Inventory Nudge Engine (proactive demand-spike alerts)
- Modeled business case: projected 30% churn reduction + 29% avg booking value lift = estimated ₹700 Cr incremental GMV at 100K-partner scale *(assumption-labeled)*
- Conducted competitive analysis of 4 OTA partner programs (MakeMyTrip, Booking.com, Airbnb, Goibibo); identified Health Score as unoccupied whitespace across all platforms

**Consulting Version**:
- Structured a marketplace supply-side analysis using an issue tree (pricing, inventory, visibility); identified that partner underperformance drives 18–22% annual churn and significant GMV leakage
- Designed a three-component product intervention with differentiated positioning: Partner Health Score (composite KPI), Dynamic Pricing Dashboard (real-time intelligence), and Inventory Nudge Engine (behavioral intervention)
- Built business case estimating ₹700 Cr incremental GMV with ₹8–10 Cr platform investment (70x+ ROI) for mid-size OTA *(assumption-labeled)*
