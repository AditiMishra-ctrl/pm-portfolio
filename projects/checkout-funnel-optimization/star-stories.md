# STAR Stories & Interview Pitches — Checkout Funnel Optimization
*Aditi Mishra | Interview Preparation*

---

## 30-Second Pitch

"I analyzed a food delivery checkout funnel and identified the payment selection step as the biggest conversion drop-off — 20% of users who reach payment abandon before completing the order. Using root cause analysis, I found that 84% of these drop-offs are product-fixable: cognitive overload from too many payment options, UPI failures, and no clear retry path. I prioritized 5 interventions by impact and effort, with a combined potential lift of 13–20% at the payment step — recovering up to ₹215 Cr annual revenue at scale."

---

## 60-Second Pitch

"Checkout funnel optimization is about recovering revenue that's almost yours. For a food delivery platform, I mapped the full checkout funnel and found that the payment selection step had the highest absolute drop-off — 42,000 users per day at the platform I analyzed.

I ran a root cause breakdown: 32% couldn't get their preferred payment method to work, 28% faced cognitive overload from 8+ payment options, 24% hit UPI deep-link failures. Critically, 84% of these failures were product-fixable — not intent-based.

My prioritized recommendations: a sticky order summary (low effort, reduces anxiety), coupon pre-validation (prevents upstream frustration), intelligent payment defaults (ML-personalized to show user's top method), a smart retry flow, and a UPI Intent upgrade.

Each comes with a defined A/B test hypothesis, success metric, and sample size. Combined lift potential: 13–20% at payment step, worth ₹107–322 Cr annually in recovered revenue."

---

## STAR Story — Funnel Analysis

**Situation**: As part of a growth analytics project on food delivery apps, I was tasked with identifying where the biggest revenue leakage occurred in the user journey and designing interventions to recover it.

**Task**: Map the full checkout funnel, isolate the highest-impact drop-off, identify root causes, and propose a prioritized set of product interventions with an A/B testing framework.

**Action**:
- Mapped the 6-step checkout funnel and quantified conversion rates at each stage
- Identified Payment Selection as the biggest absolute drop-off (20% of users abandoning)
- Performed root cause analysis across 6 failure categories; found 84% of drop-offs were product-fixable
- Developed 5 product interventions ranked by impact-effort matrix
- Designed A/B test specifications for 3 interventions (hypothesis, metrics, sample size, success threshold)
- Built a business case: conservative scenario recovers ₹107 Cr/year; base case ₹215 Cr/year

**Result**: A comprehensive funnel analysis and prioritized product roadmap targeting 13–20% conversion improvement at the payment step, grounded in structured problem-solving and data-driven prioritization.

---

## PM Interview Q&A

**Q: How would you prioritize which intervention to ship first?**

"Two quick wins first: sticky order summary (pure UX, no backend changes, 2–3pp lift) and coupon pre-validation (low effort, fixes upstream frustration). They give us fast data and stakeholder confidence. Then move to intelligent payment defaults (medium effort, 4–6pp lift — highest ROI of medium-effort interventions). UPI Intent upgrade last — high engineering effort, but critical for long-term conversion health."

**Q: How do you design an A/B test for the payment default change?**

"Hypothesis: showing user's most-used payment method first increases checkout completion. Control: current UI (COD default, 8+ options). Treatment: ML-personalized top method first, 3 options visible. Primary metric: payment step completion rate. Secondary: time on payment screen, COD vs. prepaid order mix. Sample: 50,000 per variant, 1 week. Success threshold: +3pp conversion, p<0.05. I'd also watch for novelty effects by extending to 2 weeks if numbers jump in week 1."

**Q: What if the A/B test shows no improvement?**

"First, check if there's a segmentation story — the overall result might be flat while a specific segment (e.g., new users vs. returning users) shows a significant lift. Second, audit the test setup — was the traffic split clean? Was there a holdout contamination? Third, re-examine the hypothesis — maybe personalization isn't the lever; maybe the problem is UPI reliability. I'd pivot to test the UPI Intent flow as the next hypothesis."

---

## Resume Bullets

**PM Version**:
- Conducted end-to-end checkout funnel analysis for a food delivery platform, identifying the payment selection step as the highest-impact drop-off (20% abandonment rate; 42,000 users/day); quantified ₹70L+ daily revenue leakage
- Performed root cause breakdown across 6 failure categories; found 84% of payment drop-offs are product-fixable (UX overload, UPI failures, no retry flow)
- Prioritized 5 product interventions using impact-effort matrix; projected combined conversion lift of 13–20% at payment step (₹107–322 Cr annual recovery at scale) *(assumption-labeled)*
- Designed A/B testing specifications for 3 interventions (hypotheses, primary/secondary metrics, sample size, p-value threshold); built measurement framework tracking payment step conversion, UPI success rate, and failure recovery rate

**Consulting Version**:
- Structured a checkout funnel profitability problem using conversion analysis and root cause framework; isolated payment selection as the highest-leverage intervention point
- Developed a prioritized intervention roadmap (5 initiatives) using impact-effort matrix, with business case projecting ₹107–322 Cr annual revenue recovery
- Designed A/B testing framework for hypothesis validation, converting qualitative root causes into measurable, testable product changes
