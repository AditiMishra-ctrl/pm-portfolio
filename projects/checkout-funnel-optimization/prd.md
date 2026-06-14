# Product Requirement Document — Checkout Funnel Optimization
*Version 1.0 | Aditi Mishra | Growth PM Project*
*Platform: Food Delivery App (Android + iOS) | Status: Draft*

---

## 1. Product Overview

**Product Area**: Checkout & Payment Experience
**Platform**: Mobile App (Android + iOS)
**Goal**: Reduce payment step abandonment from 20% to 7% through targeted UX and technical improvements
**Core Value Proposition**: Make completing a food order as frictionless as tapping "Pay Now" — no failed UPI, no confusion, no lost cart.

---

## 2. Problem Statement

Users who reach the payment step have already chosen their food, set their address, and have clear intent to order. A 20% drop-off at this stage is almost entirely product-caused — not intent-based. Root cause analysis shows:
- Cognitive overload from 8+ payment options
- UPI deep-link failures on older Android devices
- No order summary visible during payment (users second-guess)
- No clear recovery path when payment fails
- Coupon failures discovered too late (at payment, not at cart)

---

## 3. Goals

### Business Goals
- Recover ₹107–215 Cr annual revenue (conservative to base case)
- Improve payment step conversion from 80% to 90%+
- Reduce UPI failure rate from 29% to <12%

### User Goals
- Complete food order in under 60 seconds from checkout
- Never lose their cart due to payment failure
- Always know what payment method will work before tapping Pay

---

## 4. User Stories

### Epic 1: Intelligent Payment Defaults

**US-001** — As a returning user, I want to see my most-used payment method highlighted at the top of the payment screen, so I don't have to scroll through 8 options to find it.
- Acceptance Criteria: Top payment method (by last 5 order history) shown as default selection; other options collapsed under "More payment options"; user can expand and change

**US-002** — As a user, I want to see only 3 payment options upfront (my preferred + 1 alternative + COD), so I'm not overwhelmed with choices.
- Acceptance Criteria: Max 3 options visible by default; "See all payment methods" expander available; A/B tested against current 8-option layout

**US-003** — As a user, I want the payment screen to remember my last-used payment method, so I never have to re-select it.
- Acceptance Criteria: Last-used payment method auto-selected on next checkout; user can override any time

---

### Epic 2: Sticky Order Summary

**US-010** — As a user on the payment screen, I want to see a compact summary of my order (items, total, delivery time) at the top of the screen, so I feel confident before paying.
- Acceptance Criteria: Sticky card showing: restaurant name, item count, order total, estimated delivery time; visible without scrolling; does not cover payment options

**US-011** — As a user, I want to be able to tap the order summary to expand and review full item list, so I can quickly verify before paying.
- Acceptance Criteria: Collapsed by default (shows total + item count); tap expands to full item list; tap again collapses

---

### Epic 3: UPI Flow Improvement

**US-020** — As a user paying via UPI, I want the UPI app to open reliably every time I tap "Pay via UPI", so I don't have to retry multiple times.
- Acceptance Criteria: UPI Intent flow implemented (replaces deep-link); 95%+ UPI app launch success rate; tested on Android 9, 10, 11, 12, 13

**US-021** — As a user whose UPI app fails to open, I want to see a clear message with an alternative payment option immediately, so I'm not stuck on a broken screen.
- Acceptance Criteria: If UPI Intent fails within 5 seconds, show: "UPI didn't open. Try [Card/COD] instead?" with one-tap switch; no full page reload required

**US-022** — As a user, I want to see which UPI apps are installed on my device highlighted, so I know which ones will actually work.
- Acceptance Criteria: Real-time check of installed UPI apps; GPay/PhonePe/Paytm shown with colored icon if installed, greyed out if not; shown before user taps

---

### Epic 4: Smart Payment Retry & Recovery

**US-030** — As a user whose payment failed, I want to understand immediately why it failed and what to do next, so I don't give up and abandon my order.
- Acceptance Criteria: Failure screen shows: specific reason (Bank declined / UPI timeout / Card authentication failed); suggested alternative (e.g., "Try COD instead"); one-tap retry with same method; one-tap switch to different method

**US-031** — As a user whose payment failed, I want my cart to be preserved for at least 30 minutes, so I can retry without re-building my order.
- Acceptance Criteria: Cart state preserved 30 minutes post-failure; user returns to exact same order on retry; restaurant availability re-validated on return

**US-032** — As a user, I want to receive a push notification if my payment is processing for more than 30 seconds, so I know it hasn't disappeared.
- Acceptance Criteria: If payment API call takes >30 seconds with no response, show in-app banner: "Your payment is processing — please don't close the app"; notification sent if app is backgrounded

---

### Epic 5: Coupon Pre-validation

**US-040** — As a user with a coupon code, I want to know if my coupon is valid for my current cart before I reach the payment screen, so I'm not surprised with an error at checkout.
- Acceptance Criteria: Coupon validation triggered at cart view stage; eligible coupons auto-shown as chips; invalid coupons show reason immediately (expired / minimum order not met / restaurant not eligible)

**US-041** — As a user on the cart screen, I want to see applicable coupons proactively without having to remember or enter a code, so I never miss a discount I'm eligible for.
- Acceptance Criteria: "Available offers" section in cart; shows top 3 eligible coupons; one-tap to apply

---

## 5. Non-Functional Requirements

| Requirement | Spec |
|---|---|
| Payment Screen Load Time | <1.5 seconds |
| UPI Intent Launch Time | <3 seconds |
| Cart Preservation | 30 minutes post-failure |
| Payment API Timeout | Show spinner; notify user at 30 seconds |
| Crash Rate on Payment Screen | <0.1% sessions |
| UPI Success Rate Target | >88% (from current 71%) |

---

## 6. Out of Scope (v1)

- New payment method integrations (BNPL, CBDC)
- Subscription/recurring payment for repeat orders
- Payment splitting (pay for others)
- International payment methods

---

## 7. Release Plan

| Phase | Timeline | Scope |
|---|---|---|
| Quick Wins | Week 1–2 | Sticky order summary + coupon pre-validation (no backend) |
| Phase 1 | Week 3–6 | Smart retry flow + intelligent payment defaults (A/B test) |
| Phase 2 | Week 7–12 | UPI Intent upgrade + installed app detection |
| Measurement | Ongoing | A/B test results, funnel tracking, churn analysis |

---

*See also: case-study.md, metrics.md, star-stories.md*
