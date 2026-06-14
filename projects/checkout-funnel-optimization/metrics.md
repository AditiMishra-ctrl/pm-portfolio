# KPI Framework & Metrics — Checkout Funnel Optimization
*Aditi Mishra | Product Analytics*

---

## North Star Metric

**Order Completion Rate** = Orders Successfully Placed / Users Who Reach Checkout

*Current: ~64% (134,400 / 210,000 checkout starts)*
*Target: ~80%+ (improvement from all interventions combined)*

---

## Metric Tree

```
NORTH STAR: Order Completion Rate
│
├── PAYMENT STEP CONVERSION
│   ├── Payment Selection → Order Placed rate (%)
│   ├── UPI Payment Success Rate (%)
│   ├── Payment Failure Rate (%)
│   └── Payment Retry Success Rate (%)
│
├── CART HEALTH
│   ├── Cart Abandonment Rate (%)
│   ├── Coupon Error Rate at Payment (%)
│   ├── Cart Recovery Rate (users who retry after failure %)
│   └── Time on Payment Screen (seconds)
│
├── UX QUALITY
│   ├── UPI App Launch Success Rate (%)
│   ├── Time to Payment Selection (seconds)
│   ├── Payment Screen Error Rate (%)
│   └── "See all payment methods" click rate (%)
│
└── BUSINESS OUTCOMES
    ├── Daily Orders Recovered (vs. baseline)
    ├── Daily GMV Recovered (₹)
    ├── COD vs. Prepaid Mix (% prepaid)
    └── Average Order Value at Payment Step
```

---

## Key Metrics with Targets

### Payment Step Metrics

| Metric | Current | Target | Intervention |
|---|---|---|---|
| Payment Step Conversion | 80% | 93%+ | All interventions combined |
| UPI Payment Success Rate | 71% | 88%+ | UPI Intent upgrade |
| Payment Failure Rate | 29% (of UPI) | <12% | UPI + retry flow |
| Retry Success Rate | 12% | 35%+ | Smart retry flow |
| Time on Payment Screen | 48 sec | <30 sec | Payment defaults |

### Cart & Coupon Metrics

| Metric | Current | Target |
|---|---|---|
| Cart Abandonment Rate | 20% | <8% |
| Coupon Error Rate at Payment | ~15% of coupon users | <3% |
| Cart Recovery Rate | ~20% | >50% |

### UX Quality

| Metric | Current | Target |
|---|---|---|
| UPI App Launch Success | ~71% | >95% |
| Time to Payment Selection | 22 sec | <10 sec |
| Payment Default Acceptance Rate | — | >70% (user keeps suggested method) |

### Business Outcomes

| Scenario | Daily Orders Recovered | Daily GMV | Annual |
|---|---|---|---|
| Conservative (+5pp) | 8,400 | ₹29.4L | ₹107 Cr |
| **Base Case (+10pp)** | **16,800** | **₹58.8L** | **₹215 Cr** |
| Optimistic (+15pp) | 25,200 | ₹88.2L | ₹322 Cr |

*At ₹350 AOV, 210,000 daily checkout starts — [ASSUMPTION]*

---

## A/B Test Tracker

### Test 1: Intelligent Payment Defaults
| | Detail |
|---|---|
| Hypothesis | Showing user's most-used method first increases checkout completion |
| Control | Current: 8 options, no personalization |
| Treatment | Top 3 options, personalized default |
| Primary Metric | Payment Step Conversion Rate |
| Secondary | Time on payment screen, COD vs. prepaid mix |
| Sample | 50,000 users/variant |
| Duration | 2 weeks |
| Success | +3pp conversion, p<0.05 |
| Status | 🟡 Planned |

### Test 2: Sticky Order Summary
| | Detail |
|---|---|
| Hypothesis | Visible order context during payment reduces anxiety and abandonment |
| Control | Current: No order summary on payment screen |
| Treatment | Sticky compact order card at top of payment screen |
| Primary Metric | Payment Step Conversion Rate |
| Secondary | Time on payment screen |
| Sample | 30,000 users/variant |
| Duration | 1 week |
| Success | +2pp conversion |
| Status | 🟡 Planned |

### Test 3: UPI Intent vs. Deep-Link
| | Detail |
|---|---|
| Hypothesis | UPI Intent flow has higher success rate than deep-link |
| Control | Current deep-link implementation |
| Treatment | UPI Intent (NPCI standard) |
| Primary Metric | UPI Payment Success Rate |
| Secondary | Payment failure rate, total order completion |
| Sample | All UPI users (no split — technical migration) |
| Duration | 4 weeks post-launch |
| Success | UPI success rate >88% |
| Status | 🔴 Requires engineering |

### Test 4: Smart Retry CTA Framing
| | Detail |
|---|---|
| Hypothesis | "Try COD" suggestion on failure screen recovers more orders than generic retry |
| Control | Current failure screen (generic "Retry" button) |
| Treatment | Failure screen with specific reason + "Try COD" CTA |
| Primary Metric | Post-failure order completion rate |
| Secondary | COD order mix, cart abandonment rate |
| Sample | All users who hit payment failure |
| Duration | 2 weeks |
| Success | +20pp post-failure completion |
| Status | 🟡 Planned |

---

## Funnel Measurement Setup

To track these metrics properly, we need the following events instrumented:

```
checkout_started          → user taps "Proceed to Checkout" from cart
payment_screen_viewed     → payment options screen loaded
payment_method_selected   → user taps a payment method
payment_attempted         → user taps "Pay Now"
payment_success           → order confirmation received
payment_failed            → failure response received
payment_retried           → user taps retry after failure
order_abandoned           → user exits app from payment screen
cart_recovered            → user returns to saved cart within 30 min
coupon_error_at_payment   → coupon invalid error shown at payment step
upi_app_launch_success    → UPI app opened successfully
upi_app_launch_failed     → UPI deep-link/intent failed
```

**Tracking tool**: Firebase Analytics / Mixpanel / internal data warehouse

---

## Reporting Cadence

| Report | Audience | Frequency |
|---|---|---|
| Payment Funnel Daily Dashboard | Growth PM + Engineering | Daily |
| A/B Test Results | Product + Data team | Weekly |
| GMV Recovery Report | Business leadership | Weekly |
| UPI Health Report | Engineering | Daily during UPI migration |

---

*See also: case-study.md, prd.md, star-stories.md*
