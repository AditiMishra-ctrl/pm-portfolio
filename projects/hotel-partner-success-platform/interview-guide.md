# Interview Question Bank — Hotel Partner Success Platform
*Aditi Mishra | PM + Consulting + MBA Interview Prep*

---

## PM Interview Questions & Strong Answers

**Q1: Walk me through the Hotel Partner Success Platform.**

Strong Answer: "I identified a supply-side gap in OTA marketplaces — hotel partners, especially independent properties, have no real-time pricing intelligence, no unified performance metric, and no proactive nudges. I designed a three-component solution: a Dynamic Pricing Dashboard showing real-time competitor prices with demand forecasts, a Partner Health Score — a 0-to-100 composite metric across 5 dimensions — and an Inventory Nudge Engine that alerts partners when demand spikes or inventory is sitting dead. The differentiator is the Health Score — no major OTA currently offers a composite partner wellness metric. The business case projects a 30% reduction in partner churn, which at 100,000 partners translates to roughly ₹700 Cr incremental GMV annually."

---

**Q2: Why a composite Health Score instead of just showing individual metrics?**

Strong Answer: "Three reasons. First, cognitive load — hotel owners are busy running operations. A single number is actionable; five dashboards are not. Second, behavioral design — a score creates a goal. A partner with 74 points actively wants to hit 80 for Platinum. That motivation doesn't exist with disconnected metrics. Third, OTA alignment — the score lets our account management team prioritize intervention. A partner at 35 gets a call; a partner at 85 gets a congratulations email. The score operationalizes our partner success strategy, not just our reporting."

---

**Q3: How would you weight the 5 dimensions of the Health Score?**

Strong Answer: "I weighted Pricing Competitiveness and Inventory Availability at 25% each because they have the most direct impact on OTA booking conversion — a badly priced or unavailable room is a lost booking. Response Rate at 20% because slow response diverts confirmed demand to competitors. Guest Review Score at 20% because it drives trust for future bookings. Listing Completeness at only 10% because it has a ceiling effect — once you have good photos and description, more doesn't meaningfully move revenue. I'd revisit weights quarterly using correlation analysis: which dimension changes most correlate with actual GMV improvement?"

---

**Q4: How do you handle the pricing recommendation feature without risking price-fixing allegations?**

Strong Answer: "This is a real legal risk and I'd flag it for legal review before launch. Key mitigations: first, recommendations are suggestions, never mandatory — the partner always makes the final pricing decision. Second, the recommendation is based on market data the OTA already shows to travelers, not on private competitor business data. Third, we'd build an audit trail showing all price decisions are made by the hotel independently. Fourth, I'd model this after Booking.com's Pulse tool, which has already navigated this in multiple markets — precedent exists."

---

**Q5: A hotel partner complains their Health Score dropped from 72 to 58 overnight. Walk me through how you'd handle this.**

Strong Answer: "First, I'd look at what changed in their 5 dimension scores. The 14-point drop suggests something significant changed — likely a sharp decline in one or two dimensions, not a gradual drift. Most likely culprits: a bad review batch (Guest Score), high inventory blocking during a period we tagged as peak demand (Inventory Score), or a response rate spike if they had a busy week. Second, I'd check for data pipeline issues — did a feed fail? Are the scores reflecting stale data? Third, I'd proactively reach out through the OTA's account management team — a 14-point drop puts them from Gold into Silver, which is a Platinum-drift concern. This is exactly the use case the score was built for: early warning system."

---

**Q6: How would you measure whether the Nudge Engine is working?**

Strong Answer: "Two layers of measurement. First, engagement: what's the Nudge Action Rate — percentage of partners who act on a nudge within 2 hours? Target: >40%. And Inventory Recovery Rate — rooms opened via nudge as a percentage of rooms alerted. Target: >55%. Second, business impact: for partners who acted on the demand spike nudge vs. those who didn't, what was the difference in bookings that weekend? This is a quasi-experiment using natural variation. If nudge-actioners consistently see 25–40% more bookings on alerted dates than non-actioners, the nudge is working. I'd also track false positive rate — nudges that fire when demand didn't actually spike — to maintain signal quality."

---

## Marketplace Strategy Questions

**Q7: How do you think about the two-sided marketplace dynamics here?**

"Classic marketplace tension: supply side (hotels) and demand side (travelers) need to be served simultaneously. Our platform solves a supply-side problem, but the impact shows up on the demand side — better-priced, better-stocked hotel listings mean travelers find what they want and book. The Health Score creates a supply-quality signal that we could eventually surface to travelers: 'Platinum Partner' badge next to hotel name, similar to Booking.com's Preferred status or Airbnb Superhost. That creates a virtuous cycle — better score → better placement → more bookings → more motivated to maintain score."

---

**Q8: How would you prioritize which hotel partners to onboard first?**

"I'd target the 'Near-Platinum' segment first — partners scoring 70–79. Why? They have the highest immediate motivation (6 points from Platinum = reduced commission), the highest likelihood to act quickly, and generate the most credible success stories for wider rollout. These wins also give us proof of concept within 30–60 days, which we need to get organizational buy-in for the broader rollout. Second priority: At-Risk partners (<40 score) — intervention here prevents churn, protecting existing GMV."

---

## Consulting Questions

**Q9: Estimate the ROI of building this platform.**

"Let's work through it. Build cost: approximately ₹8–10 Cr for the full platform (engineering, design, data infrastructure). Revenue impact: there are two levers — churn reduction and GMV per partner. On churn: 100,000 partners × 20% annual churn = 20,000 partners churning. Reducing churn by 30% = 6,000 partners retained. If each retained partner generates ₹2.4L/month = ₹28,800 annual GMV × 10% OTA commission = ₹2,880 per partner = ₹17 Cr from churn reduction alone. On GMV per partner: 29% lift × ₹2.4L/month × 15,000 active users × 10% commission = ₹125 Cr additional commission annually. Total Year 1 benefit: ~₹142 Cr. Against ₹10 Cr investment: ~14x ROI. Even at 50% of projected benefit, it's a strong business case."

---

## Resume Bullets — Hotel Partner Platform

**APM/PM Version**:
- Designed a B2B Hotel Partner Success Platform for OTA marketplaces targeting the supply-side performance gap driving 18–22% annual partner churn; built 3-component solution: Dynamic Pricing Dashboard, Partner Health Score (0–100 composite across 5 dimensions — first-of-kind for OTA sector), and Inventory Nudge Engine
- Developed Partner Health Score weighting model (pricing competitiveness 25%, inventory availability 25%, response rate 20%, reviews 20%, listing completeness 10%); designed tiered partner program (Platinum/Gold/Silver/At-Risk) with differentiated benefits
- Modeled business case: 30% churn reduction + 29% GMV/partner lift = projected ₹700 Cr incremental OTA GMV; designed 3-phase GTM strategy (AM-led beta → scaled push/pull → tier lock-in) *(assumption-labeled)*
- Conducted competitive analysis of 4 OTA partner programs; identified composite Health Score as unoccupied product whitespace across MakeMyTrip, Booking.com, Airbnb, and Agoda

**Consulting Version**:
- Structured a marketplace supply-side analysis using issue tree framework; identified pricing opacity, inventory mismanagement, and performance blindness as root causes of 18–22% annual hotel partner churn on OTA platforms
- Designed a differentiated 3-component intervention with ROI modeling: ₹142 Cr projected Year 1 benefit vs. ₹10 Cr platform investment (14x ROI) *(assumption-labeled)*; prioritized rollout by partner segment using score-based risk stratification
