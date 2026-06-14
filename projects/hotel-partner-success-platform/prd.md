# Product Requirement Document — Hotel Partner Success Platform
*Version 1.0 | Aditi Mishra | B2B Product Strategy*
*Platform: OTA Marketplace (India) | Status: Draft*

---

## 1. Product Overview

**Product Name**: Partner Success Console
**Platform**: Web (desktop-first for hotel owners/managers) + Mobile app (Android, for nudges)
**Users**: Hotel partners listed on the OTA platform — primarily independent and mid-tier properties
**Core Value Proposition**: Give hotel partners the intelligence and nudges they need to optimize pricing, inventory, and performance — turning passive listings into active revenue-generating partnerships.

---

## 2. Problem Statement

Hotel partners on OTA platforms lack:
1. **Real-time pricing intelligence** — they set rates without knowing what competitors are charging
2. **A unified performance signal** — no single metric tells them how healthy their OTA listing is
3. **Proactive operational nudges** — they miss demand spikes and leave inventory (and revenue) on the table

Result: Partner churn of 18–22% annually, inconsistent inventory quality, and preventable GMV loss for the OTA.

---

## 3. Goals

### Business Goals
- Reduce partner churn from ~20% to ~14% in 12 months
- Increase average GMV per active partner by 25%
- Improve pricing competitiveness index: 80%+ partners within market price range (vs. 62% today)

### User Goals (Hotel Partner)
- Know exactly how they're performing vs. peers at a glance
- Never miss a demand spike or pricing opportunity
- Update prices and inventory in under 60 seconds from any device

---

## 4. User Stories

### Epic 1: Dynamic Pricing Dashboard

**US-101** — As a hotel manager, I want to see my room price vs. top 5 competitors in my category right now, so I can make informed pricing decisions.
- Acceptance Criteria: Dashboard loads competitor prices in real-time (max 15-min delay); shows hotel name, star category, distance, current price; sorted by price ascending

**US-102** — As a hotel owner, I want to see a 14-day demand forecast for my location, so I can adjust prices before peaks, not after.
- Acceptance Criteria: Demand index shown (Low/Medium/High/Surge) for each date; based on OTA search volume data; visible on pricing dashboard

**US-103** — As a hotel manager, I want to update my room price directly from the pricing dashboard with one click, so I don't have to navigate to a separate pricing module.
- Acceptance Criteria: "Update Price" button visible next to recommendation; confirmation in 2 clicks; price live on platform within 5 minutes

**US-104** — As a hotel owner, I want to see the projected revenue impact before I change my price, so I know it's worth doing.
- Acceptance Criteria: Before accepting recommendation, system shows: "Estimated bookings: +2 rooms | Estimated revenue: +₹5,600"

---

### Epic 2: Partner Health Score

**US-201** — As a hotel partner, I want to see my overall Partner Health Score (0–100) on my dashboard, so I know exactly where I stand on the platform.
- Acceptance Criteria: Score visible on homepage of Partner Console; updated weekly every Monday; color-coded (Red <40, Yellow 40–59, Green 60–79, Blue 80+)

**US-202** — As a hotel partner, I want to see a breakdown of my score across all 5 dimensions, so I know exactly what to fix.
- Acceptance Criteria: Each dimension shows: current score, weight, specific metric value, and one action to improve

**US-203** — As a hotel partner, I want to see my score trend over the last 8 weeks, so I can track whether my actions are improving performance.
- Acceptance Criteria: Line chart showing weekly score history; highlight weeks where major actions were taken (e.g., price update, photos added)

**US-204** — As a Gold-tier partner, I want to know exactly what I need to do to reach Platinum, so I have a clear upgrade path.
- Acceptance Criteria: "Reach Platinum" card shown to Gold partners; lists specific actions with projected score impact; e.g., "Add 8 photos (+4 pts) → Score becomes 80 → Platinum unlocked"

---

### Epic 3: Inventory Nudge Engine

**US-301** — As a hotel manager, I want to receive an alert when search demand for my dates is unusually high, so I can open blocked rooms and capture the demand.
- Acceptance Criteria: Push notification + in-app alert when demand index for any upcoming date exceeds 2x normal; shows blocked room count and projected revenue from opening them

**US-302** — As a hotel owner, I want to open my blocked rooms with one tap directly from the notification, so I don't lose time navigating the app.
- Acceptance Criteria: Notification has "Open Rooms" CTA; tapping opens confirmation screen with room count + price suggestion; confirm = inventory live within 5 minutes

**US-303** — As a hotel manager, I want to receive an alert when I have unsold rooms within 7 days, so I can offer a last-minute discount and avoid dead inventory.
- Acceptance Criteria: Alert triggered if >2 rooms unsold with <7 days to date; shows suggested discount price + projected booking probability increase

**US-304** — As a hotel manager, I want to control which types of nudges I receive and at what times, so I'm not overwhelmed with notifications.
- Acceptance Criteria: Notification preferences page; toggles for Demand Spike / Dead Inventory / Price Recommendation / Score Change; option to set quiet hours

---

### Epic 4: Partner Tier Program

**US-401** — As a Platinum-tier hotel, I want to see my reduced commission rate clearly in my dashboard, so I can track the financial benefit of maintaining my tier.
- Acceptance Criteria: Commission rate displayed on dashboard homepage; shows standard rate vs. Platinum rate; monthly savings calculation

**US-402** — As a Gold-tier hotel, I want to understand the benefits I'm missing as a non-Platinum partner, so I'm motivated to improve.
- Acceptance Criteria: "Platinum Benefits" comparison card visible to Gold partners; shows featured placement, commission reduction, priority support access

---

## 5. Non-Functional Requirements

| Requirement | Specification |
|---|---|
| Dashboard Load Time | <3 seconds on standard broadband |
| Mobile App Size | <20 MB |
| Pricing Data Freshness | Updated every 15 minutes |
| Health Score Update Frequency | Weekly (every Monday 6 AM) |
| Notification Delivery | Within 5 minutes of trigger event |
| Uptime | 99.5% SLA |
| Data Security | Partner data encrypted at rest (AES-256); TLS in transit |
| Language | English + Hindi for UI |

---

## 6. Out of Scope (v1)

- Guest communication tools (separate product)
- Financial settlement / payout management
- Multi-property management dashboard (v2)
- AI-generated listing content
- Direct booking engine (conflict of interest with OTA model)

---

## 7. Dependencies & Assumptions

> **[ASSUMPTION]** Competitor pricing data sourced via internal OTA data (search results) — no third-party scraping needed since OTA already indexes competitor prices for traveler-facing search.

> **[ASSUMPTION]** Demand forecasting uses OTA search volume data, already collected internally — no external data purchase required.

- Engineering dependency: Real-time price sync with OTA listing system (<5 min latency)
- Legal dependency: Review required for pricing recommendation feature (avoid price-fixing perception)
- Data dependency: Historical booking data per property needed to calculate Health Score baselines

---

## 8. Release Plan

| Phase | Timeline | Scope |
|---|---|---|
| Alpha | Month 1–2 | Health Score + basic pricing dashboard; 50 beta partners |
| Beta | Month 3–4 | Inventory Nudge Engine; 500 partners; feedback loops |
| v1.0 Launch | Month 5 | Full feature set; all active partners |
| v1.5 | Month 8 | Mobile app; push notifications; tier program |
| v2.0 | Month 12 | Multi-property dashboard; AI price recommendations |

---

*See also: case-study.md, metrics.md, market-research.md*
