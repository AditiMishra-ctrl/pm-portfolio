# Interview Question Bank — Checkout Funnel Optimization
*Aditi Mishra | PM + Growth + Analytics Interview Prep*

---

## PM Interview Questions & Strong Answers

**Q1: Walk me through the checkout funnel project.**

Strong Answer: "I analyzed a food delivery checkout funnel and mapped conversion rates at every step. The payment selection step had the biggest absolute drop-off — 42,000 users per day abandoning right before ordering. I did a root cause breakdown and found that 84% of these failures were product-fixable, not intent-based. Top causes: cognitive overload from 8+ payment options, UPI deep-link failures, no order summary during payment, and no clear retry path on failure. I prioritized 5 interventions using an impact-effort matrix and designed A/B test specs for each. The base case projects ₹215 Cr in annual recovered revenue — from 16,800 additional completed orders per day."

---

**Q2: How did you decide to focus on the payment step and not earlier drop-offs?**

Strong Answer: "I looked at two things: absolute drop-off volume and fixability. The cart-to-checkout step also had drop-offs, but those are largely intent-based — users browsing, comparing, changing minds. That's hard to fix with product alone. The payment step is different — users at this stage have already chosen their food, set their address, and have clear purchase intent. A 20% drop-off here is almost entirely product friction. High volume, high fixability = highest ROI. That's why I focused there."

---

**Q3: Design an A/B test for the intelligent payment defaults feature.**

Strong Answer: "Hypothesis: showing a user's most-used payment method as the default selection reduces time-to-decision and increases checkout completion. Control: current UI — 8 payment options shown, no personalization, COD is the default. Treatment: ML-personalized top method selected by default, only 3 options visible (preferred + 1 alternative + COD), rest under 'more options.' Primary metric: payment step conversion rate. Secondary metrics: time on payment screen, and COD vs. prepaid order mix — important because prepaid orders have lower cancellation rates. Sample: 50,000 users per variant, 2-week run. Success threshold: +3pp conversion, p<0.05. I'd also watch for novelty effect by comparing week 1 vs. week 2 lift."

---

**Q4: Payment step conversion improves by 3pp in your test but AOV drops. What do you do?**

Strong Answer: "First, I'd diagnose why AOV dropped. If prepaid mix went up and COD went down, that might actually be a good business signal — COD orders have higher cancellation and return rates. If the AOV drop is from users completing orders they'd have otherwise reconsidered, that's a retention question, not a conversion problem. I'd segment the AOV change: is it uniform or concentrated in a new-user cohort? If it's new users completing lower-value first orders, that's fine — LTV of an acquired user outweighs the first-order AOV dip. I wouldn't kill the feature on AOV alone without understanding the full picture."

---

**Q5: How would you measure the success of the UPI Intent upgrade?**

Strong Answer: "The primary metric is UPI Payment Success Rate — percentage of UPI payment attempts that result in successful payment. Current baseline: 71%. Target: 88%+. I'd also track UPI App Launch Success Rate separately — did the app open? — and Payment Failure Rate for UPI-specific transactions. Since this is a technical migration, not a UX A/B test, I'd run it as a phased rollout: 5% of traffic → 20% → 50% → 100%, monitoring error rates at each stage. A regression in UPI success rate at any stage triggers a rollback. Post-full-rollout, I'd declare success at 88%+ UPI success rate sustained over 2 weeks."

---

**Q6: A PM at a competing food delivery app launches a 1-tap checkout. How do you respond?**

Strong Answer: "First, I'd understand their implementation — 1-tap usually means pre-saved card or UPI autopay with user consent. Second, measure our own gap: if their feature is genuinely reducing their checkout time from 48 seconds to 10 seconds, that's a differentiation I need to close. Third, evaluate build vs. match: can we implement UPI AutoPay (mandate-based) for our repeat users? NPCI supports this through UPI 2.0. I'd scope a 'Reorder Mode' — for a user's top 3 frequent orders, skip the full checkout and enable 1-tap with saved payment. That's a targeted response that doesn't require rebuilding the entire checkout flow."

---

## Growth / Analytics Questions

**Q7: How would you estimate the daily revenue leakage from checkout drop-offs?**

Strong Answer: "Bottom-up: Start with daily app opens — say 1 million. Of those, 21% reach checkout — that's 210,000 users. Payment step has 20% drop-off — 42,000 users abandoning. Average order value: ₹350. Daily revenue leakage: 42,000 × ₹350 = ₹1.47 Cr per day. Annual: ₹536 Cr at current drop-off. Even recovering half of this — ₹268 Cr — is significant. But we can't recover all of it, since some abandonment is intentional. Realistic recovery with product fixes: 40–50% = ₹107–215 Cr annually."

---

**Q8: Payment failure rate jumps from 12% to 28% overnight. Walk me through your diagnosis.**

Strong Answer: "That's a 16-point spike — almost certainly a technical incident, not a behavioral shift. First step: check if any code was deployed in the last 24 hours. Second: check payment gateway logs — is the failure concentrated on one payment method (e.g., only HDFC cards failing)? That points to a bank-side issue, not ours. Third: check if it's device-specific (only Android 12? Only certain UPI apps?). Fourth: check timing — is the spike sustained or was it a 2-hour window? If it's sustained and across all methods, something in our payment infrastructure changed. I'd escalate to engineering immediately if deployment-correlated, or contact the payment gateway if bank-side."

---

## Behavioral Questions (STAR)

**Q9: Tell me about a time you had to make a prioritization call under pressure.**

"When I was working through the checkout funnel project, I had 5 interventions that could all improve conversion. The instinct was to ship everything at once — but that would make it impossible to measure what was actually working. I had to make a call: Quick Wins first (sticky order summary + coupon pre-validation) because they had zero backend dependency and could ship in days, proving the concept. Then Phase 1 (payment defaults + retry flow) for the biggest lift. UPI upgrade last — high engineering effort, but I wanted validated learnings from the earlier tests before committing to the most expensive intervention. The framework I used was simple: ship what's cheapest to learn from, save the expensive bets for when you have conviction."

---

## Resume Bullets — Checkout Funnel

**APM/PM Version**:
- Analyzed end-to-end checkout funnel for a food delivery platform; identified payment selection as the highest-impact drop-off (20% abandonment, 42,000 users/day) representing ₹1.47 Cr in daily revenue leakage *(assumption-labeled)*
- Conducted root cause breakdown across 6 failure categories; found 84% of payment drop-offs are product-fixable (UX overload 28%, UPI failures 24%, no retry path 10%, session timeouts 18%)
- Prioritized 5 product interventions using impact-effort matrix; projected 13–20pp combined conversion lift at payment step = ₹107–322 Cr annual revenue recovery *(assumption-labeled)*
- Designed A/B test specifications for 4 interventions: hypothesis, control/treatment definition, primary + secondary metrics, sample size, statistical threshold, and rollback criteria
- Defined analytics instrumentation plan (14 event types) to enable full funnel tracking from checkout_started to cart_recovered

**Consulting Version**:
- Structured a checkout conversion problem using funnel analysis and root cause framework; isolated payment selection as the highest-leverage intervention point with 84% of failures being product-addressable
- Developed a phased intervention roadmap (quick wins → UX improvements → technical upgrade) with full business case: ₹107–322 Cr annual revenue recovery range *(assumption-labeled)*
- Designed 4 A/B test specifications with complete measurement frameworks; built event instrumentation plan for end-to-end funnel visibility
