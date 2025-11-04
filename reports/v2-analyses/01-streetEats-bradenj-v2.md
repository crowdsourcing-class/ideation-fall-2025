# StreetEats - Viability Analysis (V2)

**Project Team**: bradenj, rolings, jgold23, egotian, chettyk

**Analysis Date**: 2025-11-02

**Rubric Version**: RUBRIC-PROJECT-VIABILITY.md

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Weight | Reasoning |
|-----------|-------|--------|-----------|
| **Technical Feasibility** | 4/5 | Critical | Standard web stack with one integration (Google Maps) |
| **Crowdsourcing Viability** | 2/5 | Critical | Circular value proposition, network effects required |
| **Incentive Design** | 2/5 | Critical | Over-reliance on intrinsic motivation for tedious tasks |
| **Scope Appropriateness** | 3/5 | High | 9 features with complex QC systems, borderline overscoped |
| **Recruitment Strategy** | 2/5 | Critical | Vague plan with no concrete commitments |
| **Quality Control** | 4/5 | High | Sophisticated multi-layered approach with specifics |

**TOTAL SCORE: 17/30**

**Category**: NEEDS MAJOR REVISION 🟠

---

## EXECUTIVE SUMMARY

StreetEats addresses a genuine problem with thoughtful quality control design and appropriate technical architecture, but suffers from a critical cold-start problem that threatens MVP viability. The team demonstrates strong technical thinking (sophisticated QC mechanisms, appropriate stack) but weak execution planning (empty timeline, vague recruitment, unrealistic incentive assumptions). Score of 17/30 places this in "Needs Major Revision" territory—viable concept but requires immediate intervention on recruitment and incentive design to avoid demo-day failure with 3 trucks and 12 users.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility: 4/5 ⚙️

**Score Justification**: Falls squarely in the "Moderate complexity" range. React/Node.js/PostgreSQL are standard undergraduate technologies with extensive documentation. Single external API (Google Maps) is well-documented and commonly used. Real-time updates add complexity but not insurmountable. No mobile development, ML, or GIS pipelines that would drop this to 2/5.

**Specific Strengths**:
- Appropriate stack for undergraduate timeline (lines 117-120, 145-150)
- Clear separation of concerns (frontend, backend, database, API)
- Team correctly avoids mobile development (common failure mode)
- Data schema is genuinely simpler than alternatives (trucks, locations, users, reviews)
- Aggregation strategy is well-thought-out (lines 153-154)

**Specific Weaknesses**:
- Timeline section completely empty (lines 338-342)—massive red flag showing lack of implementation planning
- "Real-time" claims (line 135) require WebSocket/polling infrastructure not mentioned in tech stack
- Confidence scoring algorithm mentioned repeatedly (lines 154, 161-162, 168, 178) but never defined
- No discussion of how to handle concurrent updates or race conditions
- "Near real time" (line 135) vs truly real-time creates ambiguity

**Concrete Recommendations**:
1. Fill in timeline with 2-week checkpoints showing what's built when
2. Define MVP as: basic CRUD operations + simple majority voting + Google Maps pins (cut notifications, reputation, advanced confidence scoring)
3. Specify how "real-time" will work (polling every 30 seconds is fine, don't build WebSockets)
4. Create data flow diagram showing exactly what happens from user report to database update
5. Build horizontal slice (one full workflow) before adding features

**Risk Level**: MEDIUM—technically achievable but poor planning increases risk

---

### 2. Crowdsourcing Viability: 2/5 👥

**Score Justification**: Classic "Weak value" scenario (score 2). Benefits require scale to be useful—users won't open the app without data, contributors won't update without users. Falls into the "Badges/points without community" trap. Not quite 1/5 because there IS eventual value once critical mass achieved, but getting there is the problem.

**Specific Strengths**:
- Problem is real and relatable (everyone has experienced this)
- Clear articulation of who the crowd is (lines 73-78)
- Recognition that both users AND owners are stakeholders
- Owner portal concept (line 68) could provide credibility
- Geographic scoping to Penn/University City is smart (line 312)

**Specific Weaknesses**:
- Circular value proposition: "the user will likely use the app for themselves" (line 91) assumes app already has value
- Minimum viable crowd of 50 active contributors (line 106) with no path to get first 10
- Network effects required for utility—app is useless with <20 active trucks
- Two-sided marketplace problem (need users AND truck data simultaneously)
- Zero consideration of "what does Week 1 look like when database is empty?"

**Concrete Recommendations**:
1. **Critical**: Get 5-10 truck owner commitments BEFORE building anything—make this Week 0 priority
2. Seed initial database with static data from Google Maps/Yelp before requesting updates
3. Lower minimum viable from 50 to 15 contributors by focusing on University City only
4. Add immediate value that doesn't require network effects (e.g., static menu aggregation from existing sources)
5. Team members should manually update every food truck in University City for 1 week to seed data

**Risk Level**: CRITICAL—this is the biggest threat to project success

---

### 3. Incentive Design: 2/5 💰

**Score Justification**: Clear "Mismatch" (score 2). Tasks are 2-5 minutes (find truck, open app, take photo, write location update, optionally write review) but incentives are purely badges/reputation in a system with no users. Intrinsic motivation (line 89-91) assumes users are already emotionally invested in a community that doesn't exist yet. Not quite 1/5 because quick check-ins could work with gamification IF there's an existing user base.

**Specific Strengths**:
- Recognition that truck owners have business incentive (lines 90-91)
- Reputation system concept is appropriate for this task type (line 174)
- Simple check-in design (line 64) reduces friction
- Acknowledgment that skills vary for reviews vs status updates (lines 86-87)
- Upvoting good reviews (line 174) adds social validation

**Specific Weaknesses**:
- "Intrinsic motivation" reasoning (lines 89-91) is circular: users motivated by seeing valid updates, but no updates without users
- Budget claims $0.00 per worker but $100 total (lines 94-98)—what's the $100 for?
- Gamification without community is ineffective (leaderboard with 5 people isn't motivating)
- No consideration of incentives during cold-start vs steady-state
- Reviews require 5-10 minutes of effort for pure reputation reward

**Concrete Recommendations**:
1. Allocate the mysterious $100 budget to micro-payments: $0.25 per verified status update, $1.00 per review with photo
2. Run paid pilot for 2 weeks to seed data, THEN transition to intrinsic/gamification
3. Partner with 2-3 trucks to offer "free item raffle" for contributors (mentioned in line 224 as backup—should be primary)
4. Make check-ins take <30 seconds: single button "truck is here" with auto-location
5. Add showcase value: feature "Contributor of the Week" profiles with photos/bios

**Task-Incentive Analysis**:
- Quick status check (30 sec) → Badges/points: ACCEPTABLE if community exists
- Location update with photo (3 min) → Reputation only: WEAK without community
- Full review with photos (10 min) → Badges only: MISMATCH, needs payment or showcase value

**Risk Level**: CRITICAL—inadequate incentives guarantee low participation

---

### 4. Scope Appropriateness: 3/5 📏

**Score Justification**: "Risky" (score 3). Nine key features listed (lines 59-68) with additional complex systems (confidence scoring, reputation, notifications, owner portal). Some could be cut but proposal doesn't distinguish must-haves from nice-to-haves. Empty timeline prevents assessment of whether team understands implementation complexity. Would be 2/5 except core loop IS simple (report truck, view map).

**Specific Strengths**:
- Core concept is simple: pins on a map with status updates
- Data model is straightforward (trucks, locations, statuses, reviews)
- Phased rollout approach (start with Penn/University City) limits geographic scope
- Technologies chosen are appropriate for timeline
- Simple check-in feature (line 64) shows understanding of friction reduction

**Specific Weaknesses**:
- Nine features PLUS complex backend systems (confidence scoring, aggregation, reputation)
- Empty timeline (lines 338-342) suggests team hasn't thought through implementation phases
- Notifications (line 63) require push notification infrastructure
- Owner portal (line 68) is essentially a separate application interface
- Quality control mechanisms (lines 164-178) are more complex than many projects' core features
- No prioritization of features into must/should/could/won't

**Scope Test Results**:
- ✅ Could build core loop in 2 weeks? YES (map + pins + basic updates)
- ❌ Could manually simulate? PARTIALLY (aggregation algorithm complex)
- ❌ Can name exactly 3-4 must-haves? NO (9 features, no prioritization)

**Concrete Recommendations**:
1. **Define MVP ruthlessly**: Map view + basic status updates + simple majority voting. STOP.
2. Cut for MVP: notifications, reputation system, confidence scoring algorithm, owner portal, filters, favorites, reviews
3. Week 1-2: Database + API + map with static pins
4. Week 3-4: User submission form + simple voting (3 yes = update)
5. Week 5: Polish, testing, recruitment push
6. Post-demo additions: everything else as nice-to-haves

**Feature Prioritization (MUST/SHOULD/COULD/WON'T)**:
- **MUST**: Map display, location pins, basic status (open/closed), user check-ins
- **SHOULD**: Photos, simple voting (3+ confirms)
- **COULD**: Reputation, filters, owner verification
- **WON'T** (for MVP): Notifications, confidence scoring, full review system, advanced aggregation

**Risk Level**: MEDIUM-HIGH—overscoped but salvageable with aggressive cuts

---

### 5. Recruitment Strategy: 2/5 🎯

**Score Justification**: "Vague hope" (score 2). Mentions "campus tabling, QR codes at trucks, local forums, truck-owner partnerships" (line 74) but provides zero specifics. No named groups, no commitments, no timeline for when recruitment happens. Not 1/5 because at least mentions specific tactics (tabling, QR codes) rather than pure "they'll find us."

**Specific Strengths**:
- Identifies appropriate target audience (Penn students, University City residents)
- Recognizes need for truck owner partnerships (lines 217-218)
- QR codes at trucks is creative and contextually appropriate
- Campus tabling is concrete tactic with access to target demographic
- Scale requirements are realistic (50 minimum, 300 target—lines 106-108)

**Specific Weaknesses**:
- Zero specific commitments: which dorms? which GroupMes? which trucks?
- Owner partnerships listed as "backup plan" (line 218) when should be PRIMARY strategy
- No timeline for recruitment (empty implementation timeline lines 338-342)
- No evidence of testing recruitment hypothesis (have they actually posted anywhere?)
- Treats 50 active contributors as achievable without explaining HOW
- No backup plan if organic recruitment fails (no MTurk budget allocation)

**Specificity Test Results**:
- ❌ Can you NAME exact groups? NO (generic "campus" and "forums")
- ❌ Have you TESTED recruitment? NO evidence
- ❌ Can you seed it yourself? Partially (team could manually update but need owner partnerships)
- ✅ Need >50 to start? NO (could work with 15-20 in small area)

**Concrete Recommendations**:
1. **Week 0 (before coding)**: Email EVERY food truck in University City with partnership proposal. Get 5 commitments minimum or pivot.
2. Create specific recruitment plan with NAMES:
   - Post in Penn Class of 2025/2026/2027/2028 Facebook groups
   - Partner with [specific Penn dining group/club]
   - Table at [specific high-foot-traffic location] on [specific days]
3. Test recruitment THIS WEEK: post in one forum and measure response
4. Set recruitment milestones: 10 users by end Week 2, 30 by end Week 4
5. Allocate $50 of budget to Facebook/Instagram ads targeting "Penn students interested in food trucks"
6. Have backup MTurk plan: if organic recruitment fails, pay workers to seed initial data

**Risk Level**: CRITICAL—vague recruitment plan is second-biggest threat after viability

---

### 6. Quality Control: 4/5 🎓

**Score Justification**: "Thoughtful" approaching "Multi-layered" (score 4). Seven QC mechanisms listed with specific details (lines 164-178): gold standard (owner-verified), majority voting (weighted by reputation), expert review (owners), attention checks (truck color/signage), reputation systems, statistical outliers (breakfast truck at 10pm), redundancy/agreement. This is genuinely sophisticated—well above average for undergraduate projects. Only weakness is complexity may be over-engineered for available data volume.

**Specific Strengths**:
- Owner-verified updates as gold standard is smart (line 166)
- Reputation-weighted voting addresses free-rider problem (line 174)
- Attention checks are contextually appropriate (verify truck color/signage—line 173)
- Statistical outlier detection has specific examples (breakfast truck at 10pm—line 176)
- Confidence scoring concept (lines 161-162) shows understanding of uncertainty
- Handling conflicting reports explicitly addressed (line 182)
- Multiple redundant mechanisms (seven total) provide defense in depth

**Specific Weaknesses**:
- Confidence scoring algorithm mentioned repeatedly but never defined
- Over-engineered for likely data volume (may have 50 total updates per week, not 5000)
- QC mechanisms add significant implementation complexity (weighted voting, reputation tracking, outlier detection)
- Time-sensitivity consideration (line 161) creates tension with waiting for consensus
- Risk of "analysis paralysis": waiting for perfect QC prevents real-time updates
- No mention of QC for review content (spam, inappropriate, etc.)

**Concrete Recommendations**:
1. **MVP QC**: Simple majority voting (3+ same update → publish). STOP. Add complexity later.
2. Define confidence score formula: C = (agree_votes / total_votes) * recency_weight, publish if C > 0.6
3. Start with equal weighting (all users count same), add reputation AFTER you have data on accuracy
4. Owner verification should override crowd (not just weight), publish immediately
5. For reviews: basic spam filter (profanity, length checks) + flag for manual review
6. Build QC dashboard to monitor: reports per truck, agreement rates, flagged users

**QC Priority for Implementation**:
- **Week 1-3**: Basic voting (3 agrees → update)
- **Week 4**: Add time decay (older reports count less)
- **Week 5**: Add simple reputation (track accuracy per user)
- **Post-demo**: Sophisticated confidence scoring, outlier detection, attention checks

**Risk Level**: LOW—strong design, main risk is over-engineering distracts from core features

---

## RISK ANALYSIS

### Top 3 Risks (Ranked by Impact × Likelihood)

#### Risk #1: Cold-Start Failure (Impact: CATASTROPHIC, Likelihood: HIGH)
**Description**: Team spends 4 weeks building infrastructure, realizes Week 5 they have zero food truck partnerships and no users. Database is empty, app demonstrates technical competence but zero crowdsourcing depth. Demo shows "it would work if people used it"—the undergraduate death sentence.

**Why It's Likely**:
- Owner partnerships treated as "backup plan" (line 218), not primary strategy
- No concrete recruitment plan beyond "campus tabling"
- Circular value proposition requires critical mass to be useful
- Empty timeline suggests recruitment planning hasn't happened
- Team focused on technical features (9 features + complex QC) rather than user acquisition

**Mitigation Strategies**:
1. **Week 0 (THIS WEEK)**: Email all University City food trucks, get 5 partnership commitments or pivot project
2. **Week 1**: Manual data seeding—team members physically visit and update every truck in University City
3. **Week 2**: Launch pilot with payment ($0.25 per update) using $50 budget to seed 200 initial data points
4. **Week 3**: Recruitment sprint—table at high-traffic locations, post in 10+ Penn groups, Instagram ads
5. **Week 4**: Partnership activation—get committed trucks to promote via QR codes, social media
6. **Contingency**: If <20 active users by Week 4, pivot to "food truck directory" with manual updates (less ambitious but shows completed project)

**Success Metric**: 5 truck partnerships + 30 active users by end of Week 3, or trigger contingency plan

---

#### Risk #2: Incentive-Participation Death Spiral (Impact: HIGH, Likelihood: HIGH)
**Description**: Users download app, see empty data, close app. The few early adopters make updates but get no validation or community response because no other users. Gamification (leaderboard, badges, reputation) is meaningless with 5 people. Contributors abandon platform, data goes stale.

**Why It's Likely**:
- Intrinsic motivation assumptions untested (line 89-91)
- Badges/reputation ineffective without community
- 2-5 minute tasks without meaningful reward
- No differentiation between cold-start incentives vs steady-state incentives

**Mitigation Strategies**:
1. **Paid pilot phase**: Use $100 budget for micro-payments during Weeks 2-3 to seed 300-500 updates
2. **Owner-driven incentives**: Get truck partners to offer "free item raffle" for contributors (mentioned line 224)
3. **Showcase value**: Feature "Contributor Spotlight" prominently in app to provide social recognition
4. **Reduce task friction**: Make updates <30 seconds (one-button check-in, auto-location)
5. **Add immediate utility**: Even with minimal data, provide value (static menus, truck ratings from external sources)
6. **Social proof**: Display "52 people updated this week" prominently to show activity

**Success Metric**: 70% of Week 2 users return in Week 3, average 2+ contributions per active user

---

#### Risk #3: Scope Creep Prevents Core Loop Completion (Impact: MEDIUM-HIGH, Likelihood: MEDIUM)
**Description**: Team spends 2 weeks on database/API, 1 week on Google Maps integration, 1 week on reputation system and confidence scoring, realizes Week 5 they don't have working user submission flow. Rush to finish results in buggy demo with beautiful architecture but incomplete features.

**Why It's Likely**:
- Nine features listed with complex backend systems
- Empty timeline suggests no implementation phases planned
- QC mechanisms alone could consume 2 weeks of development
- Notifications, owner portal each require substantial work
- Team shows "engineering mindset" (lines 153-178 have more detail than implementation timeline)

**Mitigation Strategies**:
1. **Ruthless MVP definition** (see Scope section above): Map + pins + basic updates. Nothing else Week 1-3.
2. **Two-week checkpoint**: End of Week 2, must have working core loop (submit update → view on map). If not, cut all remaining features.
3. **Feature freeze Week 4**: No new features after Week 4 starts, only polish and bug fixes
4. **Horizontal slicing**: Build ONE complete workflow before adding second feature
5. **Manual workarounds**: Owner verification via email to team, no portal; reputation tracked in spreadsheet, not code

**Success Metric**: Working end-to-end demo (user can submit, see update on map) by end of Week 2

---

## DECISION GUIDANCE

### Recommendation: NEEDS REVISION 🟠

**Rationale**: Score of 17/30 places this firmly in "Needs Major Revision" range (15-19). Project has strong technical foundation (Technical Feasibility 4/5, Quality Control 4/5) but critical failures in execution planning (Crowdsourcing Viability 2/5, Incentive Design 2/5, Recruitment Strategy 2/5). The concept is sound but requires immediate intervention to avoid predictable cold-start failure.

**Required Actions Before Proceeding**:
1. Get 5 food truck owner commitments THIS WEEK (required, not optional)
2. Define ruthless MVP (3-4 features max)
3. Fill in implementation timeline with 2-week checkpoints
4. Create specific recruitment plan with named channels and commitments
5. Allocate budget to paid pilot for data seeding

**Alternative Path**: If owner partnerships fail, pivot to "Food Truck Directory" (manual updates by team, less crowdsourcing but shows complete working system)

---

### Most Critical Change Needed

**Shift owner partnerships from "backup plan" to "Week 0 existential priority" and get 5 commitments before writing any code, or pivot to simpler concept.**

---

### Predicted Outcome If No Changes Made

**Without Changes**: Team builds technically competent infrastructure (React app, API, database, Google Maps integration) with sophisticated but unused QC systems. Week 5 panic-recruits 15 friends to test, gets 2 food truck partnerships via last-minute emails, has minimal real data. Demo shows polished UI with 3-4 trucks and sparse updates. Receives B/B+ for technical execution but loses points for lack of crowdsourcing depth and weak evaluation. Instructor comments: "Good engineering, but where's the crowd?"

**Specific Demo Day Scenario**:
- 25 registered users (mostly friends/family)
- 4 food trucks in database
- 12 status updates total (7 from team members)
- 3 reviews
- Sophisticated reputation system tracking 5 people
- Beautiful confidence scoring dashboard showing insufficient data
- Presentation focuses on "what it WOULD do" rather than results

**Grade Prediction**: B-/B range

**With Changes**: Focus shifts to user acquisition Week 0-1. Manual data seeding provides baseline. Paid pilot generates 300+ updates across 8-10 trucks. Simpler MVP (cut notifications, reputation, advanced QC) actually works by Week 3. Week 4-5 polish and genuine organic growth. Demo shows active system with real users, clear before/after metrics. Some features missing but core concept proven.

**Grade Prediction**: A-/B+ range

---

## COMPARISON TO V1 ANALYSIS

### What the Rubric Reveals That V1 Missed

**V1 Analysis Strengths**:
- Excellent narrative flow with "Case for Success / Case for Failure" structure
- Specific line-number references to proposal
- Identified all major issues (cold-start, intrinsic motivation, empty timeline)
- Strong adversarial framing helped surface problems
- Course framework application (Quinn & Benderson, Octalysis) provided theoretical grounding

**V2 Rubric Adds**:
1. **Quantified scoring** (17/30) makes severity concrete—"Needs Major Revision" is clearer than "Weak GO"
2. **Dimensional breakdown** shows WHERE the problems are: tech is fine (4/5), execution planning is broken (2s across board)
3. **Specific improvement paths**: Rubric provides concrete score-raising strategies V1 didn't
4. **Comparative assessment**: Score of 17/30 shows this is viable but struggling, not doomed
5. **Risk ranking**: V1 listed concerns, V2 ranks by impact × likelihood
6. **Success metrics**: V2 provides checkpoints (5 partnerships by Week 0, 30 users by Week 3)

### Key Insights That Changed

**V1 Assessment**: "Weak GO" with medium confidence
**V2 Assessment**: "Needs Revision" with specific intervention required

**Why the shift**: Rubric's dimensional scoring reveals this isn't a marginal project that needs monitoring (20-24 "Weak GO"), it's a troubled project needing major changes (15-19 "Needs Revision"). The scoring framework makes clear that having TWO critical dimensions at 2/5 (Viability, Incentives, Recruitment) is more serious than V1's "medium confidence" suggested.

**Biggest New Insight**: V1 correctly identified cold-start problem but didn't quantify HOW bad the incentive/recruitment issues are. Rubric scoring (2/5 on three critical dimensions) makes severity concrete: this needs intervention NOW, not just "monitoring."

### What Both Analyses Agree On

1. **Technical architecture is solid** (V1 "B", V2 "4/5")
2. **Quality control is sophisticated** (V1 green flag, V2 "4/5")
3. **Cold-start is the existential threat** (V1 "Case for Failure," V2 "Risk #1 CATASTROPHIC")
4. **Owner partnerships must be primary strategy** (both emphasize this)
5. **Empty timeline is massive red flag** (both identify lines 338-342)
6. **Predicted outcome without changes** (both predict technically competent but data-sparse demo, B range grade)

### Additional Considerations from Rubric Framework

**Scope Appropriateness** (3/5): V1 mentioned overscoping but V2 rubric quantifies with feature count (9 features + complex systems = borderline), provides specific must/should/could/won't breakdown

**Incentive Design** (2/5): V2 rubric's task-time × boredom formula makes clear that 3-minute updates for badges-only is a mismatch that V1 identified but didn't formalize

**Quality Control trade-off**: Both recognize sophistication, but V2 rubric highlights risk of over-engineering ("QC costs > contribution costs")

---

## ACTIONABLE NEXT STEPS

### Immediate (This Week):
1. ✅ Email ALL University City food trucks with partnership proposal
2. ✅ Set go/no-go decision point: 5 partnerships by Friday or pivot
3. ✅ Fill in implementation timeline (lines 338-342)
4. ✅ Define MVP feature set (max 4 features)
5. ✅ Create recruitment spreadsheet with named channels and deadlines

### Week 1:
1. Manual data seeding (team updates every truck in University City)
2. Build database schema + basic API
3. Post recruitment in 5+ Penn Facebook groups
4. Set up paid pilot budget ($50 for micro-payments)

### Week 2:
1. Frontend map view with static pins
2. User submission form (basic)
3. Launch paid pilot (recruit 20 users, pay for updates)
4. Checkpoint: working end-to-end demo or trigger feature cuts

### Week 3-4:
1. Simple voting mechanism (3 agrees → update)
2. Recruitment sprint (tabling, QR codes, ads)
3. Partnership activation (get trucks to promote)
4. Polish UI

### Week 5:
1. Feature freeze Monday
2. Testing, bug fixes only
3. Evaluation data collection
4. Demo preparation

---

## CONCLUSION

StreetEats has **strong technical bones** but **weak execution planning**. The team clearly understands crowdsourcing theory (sophisticated QC, thoughtful aggregation) but hasn't translated that understanding into concrete action plans (recruitment, incentives, timeline).

**The path to success exists**: get owner partnerships immediately, seed data manually, run paid pilot, recruit aggressively, cut scope ruthlessly. With these changes, this moves from 17/30 (Needs Revision) to 22-24/30 (Weak GO / Monitor Closely).

**Without changes**: technically competent demo with minimal crowd participation, B-/B grade, "good engineering but where's the crowd?" feedback.

**The team has 5 days to turn this around before Week 1 starts.** The question is whether they'll treat recruitment and partnerships with the same rigor they applied to quality control design.

---

**Analyst Note**: This is a classic case of "engineering mindset" students who excel at system design but underestimate human/organizational challenges. The sophistication of their QC thinking (lines 160-179) shows genuine talent—if they apply that same rigor to recruitment and incentive design, this project succeeds. If they assume "build it and they will come," it fails predictably.
