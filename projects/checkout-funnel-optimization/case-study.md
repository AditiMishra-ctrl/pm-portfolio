# PM Case Study — Checkout Funnel Optimization for Food Delivery App
*Aditi Mishra | Growth Strategy, Conversion Analytics*

---

## 1. Problem Statement

**Why are users dropping off at the payment step of a food delivery checkout, and what product interventions will most effectively recover these orders?**

### Context *(Assumption labeled)*

> **[ASSUMPTION]** This analysis is framed for a mid-size Indian food delivery platform (comparable to Swiggy/Zomato Tier-2 expansion). All metrics are illustrative.

Food delivery apps have a multi-step checkout funnel:
```
Browse → Add to Cart → View Cart → Checkout → Payment Selection → Order Placed
```

The **Payment Selection step** is the highest drop-off point in most food delivery funnels — industry estimates suggest **15–25% of users who reach payment selection abandon before completing the order**.

### Business Impact
- At 100,000 daily orders processed, a 20% payment drop-off = 20,000 lost orders/day
- At ₹350 AOV = **₹70L daily revenue leakage**
- Even a 5pp improvement in checkout conversion = ₹17.5L/day recovered = **₹63 Cr/year**

---

## 2. Funnel Analysis

### Baseline Funnel *(Assumption — illustrative)*

| Stage | Users | Conversion Rate | Drop-Off |
|---|---|---|---|
| App Open | 1,000,000 | — | — |
| Restaurant Browse | 600,000 | 60% | 400,000 |
| Add to Cart | 280,000 | 47% | 320,000 |
| View Cart | 240,000 | 86% | 40,000 |
| Reach Checkout | 210,000 | 88% | 30,000 |
| **Payment Selection** | **168,000** | **80%** | **42,000** ⚠️ |
| Order Placed | 134,400 | 80% | 33,600 |

**Key Finding**: The biggest absolute drop-off is at Payment Selection (42,000 users). This is where we focus.

### Why the Payment Step?

Root Cause Analysis (user research simulation):

| Reason | % Users Citing |
|---|---|
| "My saved card/UPI wasn't working" | 32% |
| "Too many payment options — confusing" | 28% |
| "UPI app didn't open / failed" | 24% |
| "Session timed out, lost cart" | 18% |
| "Changed my mind about the order" | 12% |
| "Payment failed, no clear retry path" | 10% |

**Synthesis**: 84% of drop-offs are technical or UX-caused — not user intent-based. These are recoverable with product fixes.

---

## 3. Customer Journey — Payment Step Friction Map

```
CHECKOUT BEGINS
    ↓
ADDRESS CONFIRMATION (frictionless — auto-populated)
    ↓
COUPON ENTRY (friction: code doesn't work → user re-enters → frustration spike)
    ↓
PAYMENT SELECTION ← BIG DROP HERE
├── 8+ payment options shown simultaneously (cognitive overload)
├── Default is "Cash on Delivery" — user must scroll to find UPI/card
├── UPI deep-link fails on older Android versions
├── Saved cards sometimes show "authentication required" error
└── No "order summary" visible during payment (user loses context)
    ↓
OTP / AUTHENTICATION (friction: app switch breaks session)
    ↓
PAYMENT PROCESSING (loading spinner, no ETA — anxiety)
    ↓
ORDER CONFIRMATION (or failure — no clear recovery path)
```

---

## 4. Strategic Recommendations

### Intervention 1: Intelligent Payment Defaults

**Problem**: 8+ payment options create choice paralysis.

**Solution**: Show user's most-used payment method first (ML-personalized). Reduce visible options to 3 (top used + 1 alternative + COD).

**Expected Lift**: +4–6% conversion at payment step
**Effort**: Medium (requires personalization ML, UX redesign)

---

### Intervention 2: Streamlined UPI Flow

**Problem**: UPI deep-link failures and app-switch failures cause 24% of payment drop-offs.

**Solution**:
- Implement UPI Intent flow (faster, more reliable than deep-link)
- Add in-app UPI (collect flow) as fallback
- Real-time UPI app availability check before showing option

**Expected Lift**: +3–5% conversion
**Effort**: Medium (engineering-heavy but high ROI)

---

### Intervention 3: Order Summary Always Visible

**Problem**: Users lose cart context during payment step → second-guess and abandon.

**Solution**: Sticky order summary card during entire payment step (items, total, delivery time, savings).

**Expected Lift**: +2–3% conversion (reduced anxiety)
**Effort**: Low (UX change only)

---

### Intervention 4: Smart Retry & Recovery

**Problem**: Payment failure = dead end. Users don't know what to do next.

**Solution**:
- Clear failure reason (declined, bank server, UPI timeout)
- One-tap retry with different payment method
- "Try COD" as intelligent fallback suggestion
- Cart preservation for 30 minutes post-failure

**Expected Lift**: +3–4% conversion recovery
**Effort**: Low-Medium

---

### Intervention 5: Coupon Pre-validation

**Problem**: Coupon failure after reaching payment causes frustration and back-navigation.

**Solution**: Validate coupon eligibility at cart view stage (before reaching payment). Show eligible coupons proactively.

**Expected Lift**: +1–2% conversion (reduces pre-payment frustration)
**Effort**: Low

---

## 5. Prioritization (Impact vs. Effort)

| Intervention | Conv. Lift | Effort | Priority |
|---|---|---|---|
| Sticky Order Summary | +2–3% | Low | ✅ Build first (quick win) |
| Coupon Pre-validation | +1–2% | Low | ✅ Build first (quick win) |
| Smart Retry & Recovery | +3–4% | Low-Medium | ✅ Build second |
| Intelligent Payment Defaults | +4–6% | Medium | ✅ Build second |
| UPI Flow Improvement | +3–5% | High | 🔜 Build third |

**Combined potential lift**: +13–20% at payment step. At current funnel, this recovers 21,840–33,600 orders/day.

---

## 6. A/B Testing Framework

### Test 1: Intelligent Payment Defaults
- **Hypothesis**: Showing user's most-used payment first increases checkout completion
- **Control**: Current default (COD first, 8+ options)
- **Treatment**: ML-personalized top method shown first, 3 options visible
- **Primary Metric**: Payment Step Completion Rate
- **Secondary Metrics**: Order value (COD vs. prepaid mix), time on payment screen
- **Sample Size**: 50,000 users per variant (1 week)
- **Success Threshold**: >+3pp conversion rate (statistically significant, p<0.05)

### Test 2: Sticky Order Summary
- **Hypothesis**: Showing order summary during payment reduces cart abandonment
- **Control**: Current (no order summary on payment screen)
- **Treatment**: Sticky card showing items + total + delivery time
- **Primary Metric**: Payment Step Completion Rate
- **Sample Size**: 30,000 per variant (1 week)
- **Expected Lift**: +2pp

### Test 3: UPI Intent vs. Deep-Link
- **Hypothesis**: UPI Intent flow has higher success rate than deep-link
- **Control**: Current deep-link UPI
- **Treatment**: UPI Intent (NPCI standard)
- **Primary Metric**: UPI Payment Success Rate
- **Sample Size**: All UPI users for 2 weeks (holdback test)

---

## 7. KPIs & Metrics Framework

### North Star: Order Completion Rate
= Orders Placed / Users Who Reach Checkout

### Supporting Metrics

| Metric | Current | Target |
|---|---|---|
| Payment Step Conversion | 80% | 93%+ |
| UPI Success Rate | 71% | 88%+ |
| Payment Failure Recovery Rate | 12% | 35%+ |
| Cart Abandonment Rate | 20% | 8%+ |
| Time on Payment Screen | 48 sec | <30 sec |

---

## 8. Business Case Summary

| Scenario | Daily Orders Recovered | Daily Revenue | Annual Revenue |
|---|---|---|---|
| Conservative (+5pp conversion) | 8,400 orders | ₹29.4L | ~₹107 Cr |
| Base Case (+10pp conversion) | 16,800 orders | ₹58.8L | ~₹215 Cr |
| Optimistic (+15pp conversion) | 25,200 orders | ₹88.2L | ~₹322 Cr |

*At ₹350 AOV | 1M daily app opens | Assumption-labeled*

---

*See also: star-stories.md, resume-bullets.md*
