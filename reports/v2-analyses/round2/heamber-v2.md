# V2 Viability Analysis: PriceScope

**Project:** PriceScope - Crowdsourced grocery price comparison platform

**Round:** 2 (DROPPED)

**Author:** Amber He (heamber)

---

## Viability Score

### 1. Technical Feasibility: 3/5
**Moderate Complexity:**
- Search interface (straightforward)
- Photo upload + OCR (medium complexity)
- GPS/location verification (standard mobile API)
- Database for prices + S3 for images (standard)
- Product normalization (challenging but doable)

**Challenges:**
- OCR accuracy on receipts can be finicky
- Product/brand/size normalization is complex ("Organic Valley Milk 1gal" vs. "O.V. Whole Milk 128oz")
- Geofencing requires mobile implementation or browser permissions
- AWS costs for image storage could add up

**Realistic Assessment:**
- Core CRUD app with photo upload: achievable
- OCR integration: libraries exist (Google Vision, Tesseract)
- Product matching: solvable with fuzzy matching + manual review
- **This COULD be built in 5 weeks** if descoped properly

### 2. Crowdsourcing Viability: 2/5
**Weak Value Proposition:**
- Task: "During your regular shopping, photograph receipts and manually enter prices"
- Effort: 2-5 minutes per shopping trip
- Value to user: "Find cheaper prices at other stores"

**Problems:**
- Requires significant behavior change (remembering to photograph/submit)
- Value only exists AFTER many submissions (cold-start problem)
- Competing with existing solutions (Flipp, Basket, Instacart price comparisons)
- Most people shop at the same store out of convenience, not price alone

**Who Actually Benefits:**
- Early contributors get nothing (no data yet to compare)
- Later users benefit from early contributors' work (free-rider problem)
- People on tight budgets care, but they're less likely to have time for this

### 3. Incentive Design: 2/5
**Weak Incentive Structure:**
- Primary incentive: "intrinsic savings motivation"
- Secondary: "leaderboard for top contributors"
- Raffle: "$50/month for verified submissions"

**Analysis:**
- Task effort: 3-5 minutes per shopping trip to photograph, upload, verify
- Reward: Access to price data + small raffle chance
- Leaderboard for grocery price submissions = not very compelling

**Math Doesn't Work:**
- If 200 users submit weekly, each has ~0.5% chance of winning $50/month
- Expected value per submission: ~$0.25
- Time value: 5 minutes = ~$0.25 (if you value time at minimum wage)
- **Zero net incentive for most users**

### 4. Scope Appropriateness: 4/5
**Reasonably Scoped:**
Features listed:
1. Search interface
2. Price submission form
3. Photo upload
4. Timestamp/location capture
5. Verification layer
6. Aggregation and ranking

**This is actually manageable:**
- Standard CRUD operations
- Off-the-shelf OCR
- Simple aggregation (median prices)
- Core loop could be built in 2-3 weeks

**Appropriate Scope:**
- Not overengineered
- Clear MVP: submit prices, view prices, rank stores
- Could cut photos entirely and still have working product

### 5. Recruitment Strategy: 2/5
**Vague and Unrealistic:**
- "Local shoppers, submitting grocery prices during regular (weekly maybe) store visits"
- "Around 100-200 people a week maybe"
- No specific channels mentioned
- No captive audience identified
- No partnerships with stores or community groups

**Missing:**
- Which specific communities?
- How to reach budget-conscious shoppers?
- No Penn-specific angle (Penn students don't often grocery shop)
- No clear path to first 50 users

### 6. Quality Control: 3/5
**Basic but Adequate:**
- Photo verification via OCR
- Geofencing (must be near store)
- Timestamp validation
- Reputation weighting
- Statistical outlier detection
- Rate limiting for spam

**Reasonable Approach:**
- Checks make sense for this domain
- Not over-engineered
- Majority voting for consensus
- Could work if you had enough users

---

## Total Score: 16/30

**Verdict:** NEEDS MAJOR REVISION

---

## Why Was It Dropped?

**Speculation based on quality:**

1. **Weak Value Proposition During Cold Start:**
   - First 50 users get almost zero value (insufficient data for comparison)
   - Why would someone spend 5 minutes per shopping trip to photograph receipts when they can't yet find better prices?
   - Classic chicken-and-egg: need data to provide value, need value to get data

2. **Behavior Change is Hard:**
   - Requires people to remember to photograph receipts/shelf tags every shopping trip
   - Compete with automatic solutions (store apps, credit card apps, Ibotta)
   - Most people optimize for convenience, not price, when grocery shopping

3. **Existing Competition:**
   - Flipp app aggregates store flyers (no user effort needed)
   - Instacart shows comparative prices across stores
   - Basket app does crowdsourced price tracking
   - Store apps (Target, Walmart) show in-app prices
   - **Why would users choose manual submission over automatic tracking?**

4. **Target Audience Mismatch:**
   - People most sensitive to grocery prices (low-income) often:
     - Don't have time for 5-minute submissions
     - May not have reliable smartphones/data
     - Shop at limited stores (food deserts)
   - People with time/technology tend to optimize for convenience, not price

5. **Sustainability Concerns:**
   - Relies entirely on continued voluntary submissions
   - No business model to sustain operations
   - Once users find their preferred store, motivation to contribute drops
   - Data gets stale quickly (prices change weekly)

6. **Cost Structure:**
   - "$50/month raffle + AWS costs" = $600-1000/year minimum
   - For 100-200 users = $5-10 per user per year
   - Not sustainable without revenue model

---

## Was This the Right Decision?

**YES/MAYBE - Reasonable to drop, but closer call than others.**

**Arguments for dropping:**
- 16/30 score = "Needs Major Revision"
- Weak incentive structure for sustained participation
- Cold-start problem is severe
- Existing competition has better UX (automated vs. manual)
- No clear path to critical mass of users

**Arguments it could have worked:**
- Technical scope is appropriate (unlike other dropped projects)
- Problem is real (grocery prices DO vary)
- QC mechanisms are reasonable
- Could potentially succeed in a specific niche

**Middle Ground:**
This project sits in an interesting zone - it's NOT obviously impossible (like video platform or mobile app), but it has serious structural problems around incentives and user acquisition. A more experienced team MIGHT be able to make it work, but it's risky for a course project.

---

## Hidden Gem Potential?

**YES - With significant pivots around incentives and scope**

**The Core Insight is Valid:**
- Grocery prices DO vary significantly between stores
- Price transparency benefits consumers
- Crowdsourcing COULD provide local, real-time data

**How It Could Have Worked:**

### Pivot 1: "Penn Student Grocery Game"

**Make it Penn-specific and gamified:**

1. **Target Audience:** Penn students in off-campus housing
   - Specific community: Sansom, Radian, etc.
   - GroupMe/Facebook groups for recruitment
   - 100-200 students achievable

2. **Weekly Price Challenge:**
   - "Who found the cheapest eggs this week?"
   - Submit one item per week (not whole receipt)
   - Leaderboard: "Best Deal Finder of the Week"
   - Small weekly prize ($20 gift card)

3. **Focus on Staples:**
   - Track only 10-15 common items (eggs, milk, bread, chicken, rice)
   - Much easier product normalization
   - Faster to show value

4. **Social/Competitive:**
   - "Team challenges" (by dorm/building)
   - Share your grocery haul on social media
   - Make it fun, not just utilitarian

5. **Simpler Tech:**
   - No OCR initially (manual entry is fine)
   - Photos optional for proof
   - Basic upvote/downvote on submissions
   - Winner = lowest price with photo proof

**This version could score 21-23/30:**
- Feasibility: 5/5 (much simpler)
- Viability: 4/5 (Penn students = captive audience)
- Incentives: 3/5 (still weak but gamification helps)
- Scope: 5/5 (very achievable)
- Recruitment: 4/5 (specific Penn channels)
- QC: 3/5 (simpler verification)

### Pivot 2: "Flash Deals Board"

**Instead of comprehensive price tracking, focus on deals:**

1. **Task:** "Just saw eggs for $2.99 at Acme! [photo]"
   - Quick 30-second submission
   - Only report unusually good deals, not all prices
   - Much lower effort

2. **Value:** Real-time deal alerts for nearby users
   - "Eggs on sale at Acme (0.3mi away) - expires today"
   - Immediate, actionable value

3. **Incentive:** Social recognition + karma points
   - "Thanks for the tip!" upvotes
   - Helped X people save money today

4. **Smaller Scope:**
   - Just deals, not comprehensive price database
   - Time-limited (24-48 hour visibility)
   - No complex product normalization needed

---

## Key Lessons

### What Hurt This Project:
1. **Weak Incentives for High-Effort Task:** 5 minutes per shopping trip for ~$0.25 expected value
2. **Cold-Start Problem:** Early users get minimal value
3. **Behavior Change:** Remembering to submit is hard; competing with automatic solutions
4. **No Captive Audience:** "Local shoppers" is too vague
5. **Sustainability:** Ongoing voluntary participation required forever

### What Could Have Saved It:
1. **Lower Effort:** Quick deal submissions instead of full receipt documentation
2. **Penn-Specific:** Focus on off-campus students with concrete recruitment channels
3. **Gamification:** Weekly challenges and competitions
4. **Smaller Scope:** 10-15 staple items instead of all groceries
5. **Social Elements:** Team competitions, shareability, immediate recognition

---

## Summary

PriceScope is a borderline case. Unlike FoundryMatch or CrowdScout, the technical scope is appropriate and the core problem is real. However, it has serious structural issues:

1. **Weak incentive design** for the effort required
2. **Severe cold-start problem** (early users get no value)
3. **Competes with automated solutions** (store apps, credit cards)
4. **No clear recruitment path** to critical mass

With a 16/30 score, it falls into "Needs Major Revision" - not quite as doomed as the 10-14 range, but still risky.

**Was it right to drop?** Probably yes. The incentive structure is fundamentally weak, and without a captive audience or killer app feature, it's hard to see how it reaches critical mass.

**Hidden gem potential: MEDIUM.** With significant pivots (Penn-specific, gamified, lower effort, focus on deals not comprehensive tracking), this COULD have worked as a B/B+ project. The technical scope is appropriate, which gives it an advantage over other dropped projects.

**Bottom Line:** Reasonable idea with appropriate scope, but weak on crowdsourcing fundamentals (incentives, recruitment, value proposition). Needed either stronger incentives or significantly lower task effort to work.
