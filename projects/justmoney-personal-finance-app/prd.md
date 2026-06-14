# Product Requirement Document — JustMoney
*Version 1.0 | Aditi Mishra | MBA Product Strategy Project*
*Status: Draft | Last Updated: June 2026*

---

## 1. Product Overview

**Product Name**: JustMoney (जस्ट मनी)
**Platform**: Mobile (Android-first, given Tier-2 device distribution)
**Target User**: Working adults aged 22–45 in Tier-2/3 Indian cities
**Core Value Proposition**: A vernacular-first personal finance app that acts as a trusted financial mirror — showing users where their money goes and helping them save for what matters, without complexity.

---

## 2. Problem Statement

Tier-2 Indian users have adopted digital payments (UPI) but lack tools for financial management that:
- Work in their language
- Don't require financial literacy to use
- Can be trusted with sensitive bank data
- Fit their financial reality (irregular income, joint family, cash + digital mix)

---

## 3. Goals & Success Metrics

### Business Goals
- Acquire 100,000 MAU in first 12 months post-launch *(Assumption)*
- Achieve 40% D30 retention (industry avg for fintech: 25–30%)
- 15% conversion to premium in Year 1

### User Goals
- Set and track at least one financial goal within first 7 days
- Reduce "money anxiety" (self-reported) by giving clarity on spending
- Feel safe and in control

### Success Metrics (North Star)

| Metric | Definition | Target |
|---|---|---|
| **Weekly Active Users (WAU)** | Users who open app at least once/week | 55% of MAU |
| **Goal Completion Rate** | % users who hit a savings goal | 30% by Month 6 |
| **CSAT** | Post-onboarding + monthly survey | ≥ 4.2/5 |
| **Trust Score** | % who link bank account vs. only UPI | 60% link bank by Day 30 |
| **Referral Rate** | % users who refer ≥1 friend | 20% by Month 3 |

---

## 4. User Stories

### Epic 1: Onboarding & Trust

**US-001** — As a new user, I want to sign up with just my phone number (no email required) so I can get started without friction.
- Acceptance Criteria: OTP-based auth; no mandatory email; completes in <90 seconds

**US-002** — As a skeptical user, I want to understand what data the app collects and why before I link my bank account, so I feel safe.
- Acceptance Criteria: Plain-language privacy explainer shown before bank-link step; option to "try without bank" available

**US-003** — As a Hindi-speaking user, I want the entire app to work in Hindi so I don't need to translate financial terms.
- Acceptance Criteria: 100% UI coverage in Hindi; financial terms have a one-tap vernacular explainer

---

### Epic 2: Financial Dashboard

**US-010** — As a user, I want to see my total money (bank balance + UPI wallet) in one screen so I know exactly where I stand.
- Acceptance Criteria: Dashboard loads in <2 seconds; shows balance, last 5 transactions, upcoming EMIs

**US-011** — As a user, I want to see a monthly spending summary by category (food, travel, shopping) so I can identify where I overspend.
- Acceptance Criteria: Auto-categorization with 85% accuracy; user can reclassify transactions

**US-012** — As a user, I want a nudge message in Hindi at month-end summarizing my spending so I don't have to dig for it.
- Acceptance Criteria: Push notification + in-app card; personalized to user's actual spending data

---

### Epic 3: Goal-Based Savings

**US-020** — As a user, I want to create a savings "bucket" for a specific goal (e.g., "Raju ka school fee", "Diwali shopping") so I can visualize my progress.
- Acceptance Criteria: User sets goal name (custom or preset), target amount, deadline; progress bar shown

**US-021** — As a user, I want the app to suggest how much I should save monthly to hit my goal on time so I don't have to calculate it.
- Acceptance Criteria: Auto-calculation based on target, deadline, and current balance; shows in ₹/month

**US-022** — As a user, I want to mark a "quick save" transfer to my goal bucket directly from the app so saving is a one-tap action.
- Acceptance Criteria: One-tap save; confirmation with animation; links to UPI or bank transfer

---

### Epic 4: EMI & Bill Tracker

**US-030** — As a user with multiple EMIs, I want to see all upcoming EMI and bill payments in a calendar view so I never miss one.
- Acceptance Criteria: Calendar with EMIs, utility bills, insurance; 3-day and 1-day reminders

**US-031** — As a user, I want to manually add an EMI (since not all are digital) so my tracker is complete.
- Acceptance Criteria: Manual entry form with amount, frequency, start date, lender name

---

## 5. Non-Functional Requirements

| Requirement | Spec |
|---|---|
| App Size | <25MB (Tier-2 storage constraints) |
| Offline Mode | Dashboard viewable offline; transactions sync on reconnect |
| Language Support | Hindi, English, Tamil, Telugu, Bengali, Marathi |
| Accessibility | Font size adjustable; high-contrast mode |
| Data Encryption | AES-256 for stored data; TLS 1.3 for transit |
| Crash Rate | <0.5% sessions |
| App Load Time | <3 seconds on 4G; <6 seconds on 3G |

---

## 6. Out of Scope (v1)

- Stock/mutual fund trading
- Insurance marketplace
- Credit score tracking (trust barrier; v2+)
- Desktop / web version
- Business accounting features (v2+)

---

## 7. Dependencies & Assumptions

> **[ASSUMPTION]** Bank account aggregation requires Account Aggregator (AA) framework integration — available via Finvu, Onemoney, or Setu.

> **[ASSUMPTION]** UPI transaction history pulled via user-consent-based screen-scraping or AA, pending RBI API availability.

- Regulatory dependency: RBI Account Aggregator Framework compliance required
- Tech dependency: SMS parsing for transaction detection (fallback if AA not available)
- Business dependency: Partner bank for FD booking (v1.5)

---

## 8. Risks

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Low bank-linking adoption | High | High | "Try without bank" mode; gradual trust building |
| SMS permission denial (Android 12+) | Medium | High | AA framework as primary; SMS as fallback |
| Competitor replication of vernacular UI | Medium | Medium | Build community + network effects early |
| Regulatory change on AA framework | Low | High | Monitor RBI policy; maintain manual entry fallback |

---

## 9. Release Plan *(Assumption)*

| Phase | Timeline | Features |
|---|---|---|
| Alpha | Month 1–2 | Onboarding, Dashboard, Hindi UI |
| Beta | Month 3–4 | Goal Buckets, EMI Tracker, 100 user beta |
| v1.0 Launch | Month 5–6 | Full feature set, Android Play Store |
| v1.5 | Month 9 | FD booking, regional language expansion |
| v2.0 | Month 12 | Business mode, credit insights, iOS |

---

*See also: case-study.md, market-research.md, metrics.md*
