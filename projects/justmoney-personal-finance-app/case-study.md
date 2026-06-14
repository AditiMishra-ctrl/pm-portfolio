# PM Case Study — JustMoney: Personal Finance App for Tier-2 Cities
*Aditi Mishra | Research-Driven Product Strategy*

---

## 1. Problem Statement

**How might we help working adults in Tier-2 Indian cities manage their personal finances better, without overwhelming them with complexity or jargon?**

### Context
- India has 650M smartphone users; 250M+ are in Tier-2/3 cities
- UPI has driven payment digitization, but **savings, investments, and budgeting** remain analog
- 73% of Tier-2 users do not use any dedicated financial planning app *(RBI Financial Inclusion Survey, 2023)*
- Existing apps (Groww, Zerodha, Money View) are designed for urban, English-literate users

### Root Cause Analysis
Using a 5-Whys framework:
1. Why don't Tier-2 users use finance apps? → Complex UI, English-only
2. Why does English-only matter? → Financial terms don't translate meaningfully
3. Why do complex UIs fail? → Digital literacy is lower; single feature discovery is hard
4. Why low trust? → Users don't understand how app makes money; privacy concerns
5. Why no behavior change? → No local social proof; no nudge that fits cultural context

---

## 2. Research Methodology

### Primary Research (100+ Users)
- **Interviews**: 60 in-depth interviews (30–45 min each), Varanasi, Lucknow, Allahabad, Kanpur
- **Surveys**: 45 structured surveys with 5-point Likert scale questions
- **Observation**: 15 contextual usage observations at local shops, homes
- **Prototype Testing**: 20 users tested a Figma prototype; CSAT = 4.5/5

### Recruitment Criteria
- Age: 22–45
- City: Tier-2 (pop. 5L–50L)
- Income: ₹20,000–₹80,000/month
- Smartphone literacy: basic (UPI users)
- Not current users of financial advisory apps

### Research Questions
1. How do users currently manage household finances?
2. What financial goals matter most to them?
3. What has prevented them from using finance apps before?
4. What would make them trust a new finance app?

---

## 3. User Research Findings

### Top Pain Points (Validated, Ranked by Frequency)

| # | Pain Point | % Users Who Mentioned It |
|---|---|---|
| 1 | "App is in English, I don't understand" | 78% |
| 2 | "I don't know where my money goes each month" | 71% |
| 3 | "I don't trust apps with my bank details" | 65% |
| 4 | "I can't track my EMIs and savings in one place" | 58% |
| 5 | "Too many features — I get confused" | 52% |
| 6 | "Nobody around me uses it, so why should I?" | 44% |
| 7 | "I tried once, data was wrong — never went back" | 38% |

### Key Insight
> **"Tier-2 users don't need more financial products — they need a trusted financial mirror that shows them where they stand, in their language."**

---

## 4. Personas

### Persona 1: Rajan, the Salaried Government Employee
- Age: 34 | City: Varanasi | Income: ₹42,000/month
- Uses UPI daily; no savings app
- Goals: child's education fund, house down payment in 5 years
- Frustration: "I save ₹8,000 every month but have no idea if it's enough"
- Quote: "Agar koi simple tarike se bata de ki kya karna hai, toh main zaroor karunga"

### Persona 2: Priya, the Small Business Owner
- Age: 28 | City: Kanpur | Income: ₹55,000/month (irregular)
- Runs a boutique; uses Excel for accounts
- Goals: separate business and personal finances, build emergency fund
- Frustration: "Business and personal money get mixed — big mess at tax time"

### Persona 3: Vikram, the First-Time Earner
- Age: 23 | City: Lucknow | Income: ₹22,000/month (first job)
- Never tracked finances; spends on impulse
- Goals: save for travel, buy a bike
- Frustration: "Month end mein paisa nahi rehta — pata nahi kahan jata hai"

### Persona 4: Sunita, the Homemaker with Access to Household Income
- Age: 40 | City: Allahabad | Income: Household ₹65,000/month
- Manages grocery/household cash; husband handles banking
- Goals: secret savings for family emergencies, gold purchase
- Frustration: "I have to ask every time I need money for something important"

---

## 5. Customer Journey Map (Rajan — Primary Persona)

```
STAGE         | Awareness       | Consideration   | Onboarding      | Habit Loop      | Advocacy
--------------|-----------------|-----------------|-----------------|-----------------|-----------
ACTION        | Hears about app | Downloads, opens | Links bank acct | Checks weekly   | Recommends
              | from colleague  | hesitates at    | → nervous about | dashboard →     | to friends
              |                 | bank login      | privacy         | gets nudge      |
THOUGHT       | "Might help me  | "Is it safe?    | "What will they | "Oh, I spent    | "This is
              | save better"    | Who made this?" | do with data?"  | ₹3k on eating   | actually
              |                 |                 |                 | out this month" | useful"
EMOTION       | Curious         | Skeptical       | Anxious         | Surprised       | Proud
PAIN POINT    | Low awareness   | Trust barrier   | Privacy fear    | Overwhelm risk  | Low network
OPPORTUNITY   | Word-of-mouth   | Social proof +  | Minimal perms   | Simple, 1-click | Referral
              | + employer      | transparency    | + explainer     | insights only   | incentive
```

---

## 6. Solution Design

### Core Feature Set (MoSCoW)

**Must Have**
1. **Unified Dashboard** — Aggregates UPI, bank balance, EMIs, investments in one view
2. **Vernacular First** — Full Hindi + 5 regional languages; financial terms translated contextually
3. **Goal Buckets** — Visual "piggy banks" for specific goals (child education, vacation, gadget)

**Should Have**
4. **Monthly Spend Summary** — "Aapne is mahine ₹4,200 khaane mein kharch kiye" (WhatsApp-style nudge)
5. **EMI + Bill Tracker** — Calendar view of upcoming payments with alerts
6. **Trust Layer** — Explains data usage in simple language; option to use without bank link

**Could Have**
7. **Peer Benchmarking** — "Your savings rate is better than 65% of users like you"
8. **Quick FD/RD Booking** — In-app, partner bank integration

**Won't Have (v1)**
- Stock trading
- Insurance marketplace
- Credit scoring (trust issue)

---

## 7. Prioritization Framework (RICE)

| Feature | Reach | Impact | Confidence | Effort | RICE Score |
|---|---|---|---|---|---|
| Vernacular UI | 9 | 9 | 8 | 6 | 108 |
| Unified Dashboard | 8 | 9 | 8 | 7 | 82 |
| Goal Buckets | 7 | 8 | 9 | 5 | 101 |
| Monthly Nudge | 8 | 7 | 8 | 3 | 149 |
| EMI Tracker | 6 | 8 | 9 | 4 | 108 |
| Trust Explainer | 9 | 9 | 7 | 3 | 189 |

**Top Priority by RICE**: Trust Explainer → Monthly Nudge → Vernacular UI

---

## 8. Prototype Testing Results

- **Test Group**: 20 users (Rajan persona type)
- **Method**: Task-based usability testing on Figma prototype
- **Tasks Given**: Set a savings goal, check last month's spending, track EMI
- **CSAT**: 4.5/5.0
- **Task Completion Rate**: 85% (17/20 completed all 3 tasks)
- **Key Usability Finding**: Users loved goal buckets; struggled with initial bank-linking step

**Insight from testing**: Users wanted a "try without linking bank" option first — major trust unlock.

---

## 9. Business Model *(Assumption-labeled)*

> **[ASSUMPTION]** Revenue model based on comparable fintech apps in emerging markets.

| Stream | Description | Revenue Potential |
|---|---|---|
| Freemium | Basic dashboard free; premium = advanced analytics + tax prep | ₹99/month |
| B2B2C | Employer financial wellness program | ₹50/employee/month |
| Referral Commission | FD/RD booking via partner banks | 0.5–1% commission |
| Data Insights (Anonymized) | Aggregated spending data for FMCG/retailer insights | Enterprise licensing |

---

## 10. Key Learnings

1. **Trust is the moat** in Tier-2 fintech — not features
2. **Vernacular UX** is an underinvested, high-ROI differentiator
3. **Starting small** (one financial habit) beats comprehensive feature set for adoption
4. **Social proof** (friends/family using it) is the #1 trigger for downloads

---

*See also: prd.md, market-research.md, metrics.md, gtm.md, star-stories.md*
