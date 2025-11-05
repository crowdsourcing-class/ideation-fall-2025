# V2 Viability Analysis: PennPulse (Round 2 - DROPPED)

## Project Summary
**PennPulse** - A centralized, real-time feed of Penn campus events curated by students through upvoting, tagging, and live check-ins

**Authors:** Alex Oh, Shivi Jain

---

## Viability Score Assessment

### 1. Technical Feasibility: 4/5
**Score: Moderate Complexity**
- Standard CRUD app with voting/ranking system
- React frontend, AWS backend
- Reddit-style ranking algorithm (hot score based on votes and time)
- Location-check optional feature
- No complex ML, no mobile requirement
- **Reasonable for 5 weeks** with some API integration work

### 2. Crowdsourcing Viability: 2/5
**Score: Weak Value**
- Classic chicken-egg problem: need events to attract users, need users to post events
- Circular value proposition: "Students find events AND post events"
- Competes with existing channels (listservs, GroupMe, Penn Clubs) that already work
- Unclear why users would switch from existing platforms
- Depends on critical mass to be useful

### 3. Incentive Design: 2/5
**Score: Mismatch**
- No clear incentive for posting events (5-10 min task)
- "Self-sustaining" assumption not validated
- Club leaders already have channels that work (why add another?)
- Upvoting/downvoting requires attending events first (high friction)
- Students benefit from FINDING events, but little incentive to CURATE them

### 4. Scope Appropriateness: 4/5
**Score: Slight Stretch**
- 5 features listed (reasonable)
- Event posting, voting, photos, filtering, notifications
- Some wishlist items implied (notifications "based on interests/academics")
- Core loop is simple enough to build in 2 weeks
- Scope is actually reasonable IF users existed

### 5. Recruitment Strategy: 2/5
**Score: Vague Hope**
- "Around 100 to start"
- Plan: "Partner with large orgs (PEC, AWE, SWE, Wharton Council)"
- No evidence these partnerships exist or were approached
- "Cross-post their events at launch" assumes orgs will cooperate
- Classic "if you build it, they will come" thinking

### 6. Quality Control: 3/5
**Score: Basic**
- Penn email verification (PennKey)
- Majority voting mechanism
- Community flagging
- Downvote filters and "low trust scores"
- Missing specifics: What IS a "low trust score"? How many downvotes to remove?
- NLP similarity detection mentioned but not detailed

**TOTAL SCORE: 17/30**

---

## Verdict: NEEDS MAJOR REVISION

This falls in the 15-19 range: "Project has multiple serious issues. Needs significant rethinking."

---

## Why Was It Dropped?

**Likely reasons:**

1. **Two-sided marketplace problem** - Need BOTH event posters AND event seekers simultaneously
2. **Weak value proposition** - Doesn't solve a problem students don't already have solutions for
3. **No clear adoption path** - Existing channels (listservs, GroupMe, Penn Clubs) have network effects
4. **Partnership dependency** - Success depends on unconfirmed partnerships with student orgs
5. **Incentive mismatch** - Finding events is valuable, but posting/curating has no clear reward

**Evidence from proposal:**
- States "self-sustaining" but provides no evidence
- "Hopefully $0" budget suggests no plan for bootstrapping
- Recruitment section says "around 100 to start" with no specific plan
- Discussion notes: "Onboarding enough users early" was flagged as a concern but not addressed

---

## Was This the Right Decision?

**YES - This was correctly dropped.**

**Reasoning:**
- Scores only 17/30, placing it in "Needs Major Revision" territory
- The two critical weaknesses (Viability: 2/5, Incentives: 2/5) are structural, not fixable with iteration
- Circular dependency: useful only with scale, but no path to scale
- Competes with entrenched solutions (GroupMe, Sidechat, Penn Clubs) without clear differentiation
- "Self-sustaining" is an assumption, not a validated mechanism

**Similar projects that failed:**
- Every campus has tried to build "the one events platform"
- They fail because of network effects: existing channels already have the users
- PennPulse provides no compelling reason for BOTH sides to switch simultaneously

---

## Hidden Gem Potential?

**LOW - The core idea has been tried many times and typically fails**

**Why this is NOT a hidden gem:**

1. **Not a new insight** - Campus event aggregation is a solved problem (Penn Clubs exists)
2. **Network effect moat** - Existing platforms (GroupMe, listservs) are "good enough" and sticky
3. **No unique value** - Real-time feed and upvoting don't solve the core problem (discoverability)
4. **Execution wouldn't fix it** - Even with perfect execution, adoption is still the killer

**What MIGHT have made it work:**

1. **Scrape-first approach:**
   - Don't ask users to post events
   - Automatically scrape/aggregate from existing sources (listservs, Penn Clubs API, Instagram)
   - Launch with 100+ events already in system
   - Users only need to consume and vote
   - Eliminates two-sided problem

2. **Hyper-niche focus:**
   - "Free food at Penn right now" only
   - Simple, immediate value
   - Smaller scope = easier to seed and validate
   - Could prove concept before expanding

3. **Partnership-first:**
   - Actually secure commitments from 5+ major orgs BEFORE building
   - Have them agree to exclusively post on PennPulse for one month
   - Guarantees initial content

**Even with these fixes:** Still faces uphill battle against existing platforms. The problem space is crowded and the switching costs are high.

**Fundamental issue:** This is a startup idea disguised as a class project. It needs months of user acquisition and iteration, not 5 weeks of building.

**Better pivot:** Instead of a new platform, build a tool that INTEGRATES with existing channels (e.g., a browser extension that aggregates events from GroupMe/email and lets you filter/save them). Provides value without requiring mass adoption.
