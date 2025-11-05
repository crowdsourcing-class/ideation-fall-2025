# MoodMap@Penn - Project Viability Analysis (V2)

**Project**: MoodMap@Penn
**Authors**: Tiffany Lian (tilian), Arriella Mafuta (arriella), Veda Mantena (vmantena)
**Analysis Date**: 2025-11-02
**Proposal Version**: Round 3

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| **1. Technical Feasibility** | 4/5 | React/Next.js PWA with Firebase and Mapbox is well-scoped. Time-decay functions and geohash binning add moderate complexity but achievable. Loss of 1 point for weekly email jobs and potential analytics pipeline complexity. |
| **2. Crowdsourcing Viability** | 3/5 | Penn students are accessible audience, but value proposition is circular—heatmap only useful with critical mass, but students only participate if heatmap is valuable. Mood tracking requires consistent engagement, which is hard without immediate personal benefit. |
| **3. Incentive Design** | 3/5 | Task is quick (<2 min mood check-in), suitable for gamification. Octalysis framework applied thoughtfully with streaks, badges, and social comparison. However, intrinsic motivation may not sustain weekly participation among busy Penn students—no immediate personal utility beyond reflection. |
| **4. Scope Appropriateness** | 4/5 | Core loop (submit mood → aggregate → display heatmap) is achievable in 2 weeks. 9 features listed but most are essential. Could descope weekly emails and wellness dashboard initially. Generally well-bounded for 5 weeks. |
| **5. Recruitment Strategy** | 2/5 | Vague plan: "Partner with student orgs" and "promote during Wellness Week" without specific commitments or names. No proof of access to concrete channels. Cold-start problem unaddressed—need ~100 users to make heatmap meaningful but no forcing function to get them. |
| **6. Quality Control** | 3/5 | Penn email verification limits spam; rate-limiting and time-decay are appropriate. Statistical outlier detection mentioned but not detailed. No gold standards (correct for subjective mood data). QC is basic but probably sufficient for mood self-reports. |
| **TOTAL** | **19/30** | **Needs Major Revision** |

---

## EXECUTIVE SUMMARY

MoodMap@Penn is a well-intentioned mood-tracking platform with appropriate technical scope and thoughtful gamification design. However, the project suffers from a critical **cold-start problem**: the heatmap is only valuable if many students participate, but students will only participate if the heatmap already shows meaningful data. Recruitment strategy is vague and untested, relying on hoped-for partnerships rather than confirmed access to specific student populations. The intrinsic motivation model (streaks, badges, peer comparison) may not sustain busy Penn students beyond initial novelty. Without aggressive early recruitment or a captive audience commitment, this project risks building a polished but empty platform.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility (4/5)

**Strengths**:
- React/Next.js PWA with Firebase Firestore is a proven, well-documented stack suitable for rapid prototyping
- Mapbox integration for heatmap visualization is straightforward with existing libraries
- Core submission flow (auth → form → database → aggregation → display) is standard CRUD + visualization
- Time-decay weighting formula is clearly specified and implementable
- Firebase Cloud Functions for scheduled aggregation jobs are appropriate for this use case

**Concerns**:
- Time-decay exponential weighting (exp(-Δt/τ)) and geohash binning add moderate algorithmic complexity
- Weekly email digests via SendGrid introduce external dependency and potential edge cases
- Analytics pipeline for wellness dashboard may require additional data modeling
- Real-time updates could introduce scaling challenges if participation exceeds expectations
- Python scripts for mood trend analysis (mentioned as optional) would add tech-stack complexity

**Verdict**: Technically feasible but non-trivial. Team should focus on core loop first (submit → aggregate → display) and defer emails and analytics to later weeks if time permits.

---

### 2. Crowdsourcing Viability (3/5)

**Strengths**:
- Target audience (Penn students) is geographically accessible and defined
- Emotional well-being is a relevant topic on campus given "Penn Face" culture
- Anonymous submission removes social risk of sharing negative emotions
- Peer comparison feature ("you're not alone") could resonate if enough data exists

**Concerns**:
- **Cold-start problem**: An empty or sparse heatmap has no value, but students won't contribute to make it valuable without seeing existing value
- Mood tracking is a **passive value proposition**—users don't get immediate utility (unlike finding a study spot or reviewing food)
- Competing with existing wellness resources and mental load of yet another app
- Penn students are notoriously busy; daily mood check-ins may not be sustainable beyond initial curiosity
- No evidence of pre-launch interest or user testing of the value proposition

**Verdict**: Viable in theory but faces significant chicken-and-egg adoption barrier. Success depends entirely on recruitment execution, which is currently weak (see Dimension 5).

---

### 3. Incentive Design (3/5)

**Strengths**:
- Task is genuinely quick (<2 minutes for mood selection + optional note + location)
- Octalysis framework explicitly applied across 6 drives (meaningful, accomplishment, social, creativity, scarcity, ownership)
- Daily streaks and reflection badges are appropriate for repeated low-effort tasks
- Anonymous peer comparison provides social validation without identity exposure
- Personal mood journal creates sense of ownership over longitudinal data

**Concerns**:
- **Intrinsic motivation may not be strong enough**: Students are asked to do emotional labor (reflect on mood) daily without clear personal benefit beyond seeing their own history
- Badges and streaks work best when there's already a habit or community—without critical mass, these feel hollow
- "Fighting Penn Face" is a worthy cause but abstract; doesn't solve an immediate pain point like finding a quiet study space
- No backup extrinsic incentives (small raffle entries, Penn Wellness partnerships offering tangible rewards)
- Comparison to successful mood-tracking apps (Daylio, Moodfit) shows that personal insight and health tracking are primary motivators, not community heatmaps

**Verdict**: Gamification is well-designed on paper, but may not overcome activation energy for busy students. Task is quick enough that if motivated users exist, they'll participate—but motivation itself is the question.

---

### 4. Scope Appropriateness (4/5)

**Strengths**:
- Core loop (submit mood → store → aggregate → display heatmap) is achievable in 2 weeks
- 9 listed features, but most are essential (submission, heatmap, auth, streaks, privacy)
- Firebase stack enables rapid iteration without complex backend infrastructure
- Team has realistic implementation timeline (Weeks 1-2 setup, 3-4 build, 5-6 test, 7-8 launch)

**Concerns**:
- Weekly summary emails and wellness dashboard are "nice-to-have" features that could be cut if time is tight
- Time-decay function and geohash aggregation, while not insurmountable, add non-trivial algorithmic work
- "Community Challenges and Events" feature is vague and could expand scope unpredictably
- Python ML mood trend analysis (mentioned in tech stack) is premature optimization—should be cut

**Recommendations**:
- Build horizontal slice: full core loop (submit → display) before adding emails, challenges, or analytics
- Defer wellness dashboard until after proving student engagement
- Keep "Community Challenges" as manual (admin-created) prompts, not automated systems

**Verdict**: Generally well-scoped if team is disciplined about focusing on core functionality first. Risk of feature creep is moderate.

---

### 5. Recruitment Strategy (2/5)

**Strengths**:
- Recognizes need for critical mass (300-500 workers for "full functionality")
- Budget includes $300-400 for "small participation rewards" (raffles, Penn-themed incentives)
- Mentions specific channels: student orgs (Active Minds), Wellness Week, dorm-specific pilots

**Concerns**:
- **No concrete commitments**: "Partner with student orgs" and "advertise on social media" are aspirational, not executed
- No evidence of conversations with Active Minds, CAPS, or any student group leaders
- "Promote during Wellness Week" assumes (a) access to that platform and (b) that it happens during project timeline
- Backup plan of "targeted dorm or school-specific pilots" is mentioned but not specified (which dorm? which RA?)
- 100-300 participants needed but no specificity test passed (cannot name exact groups or commitments)
- No mention of seeding strategy (will team create initial check-ins to make map look populated?)

**Critical Gaps**:
- ❌ No named contacts or confirmed partnerships
- ❌ No user interviews or interest validation
- ❌ No plan for how to recruit first 10 users (friends? classmates? GroupMe blast?)
- ❌ No forcing function (e.g., NETS 2130 class requirement, psychology study participant pool, RA-mandated floor activity)

**Verdict**: Recruitment is the fatal flaw. Without immediate access to a captive audience or concrete promotional commitments, the project will likely fail to achieve critical mass during the 5-week window.

---

### 6. Quality Control (3/5)

**Strengths**:
- Penn email verification ensures only students can contribute, reducing external spam
- Rate-limiting (few submissions per day per user) prevents single-user manipulation
- Time-based decay reduces impact of stale data and gradual gaming
- Statistical outlier detection (sudden bursts, extreme values) is appropriate
- Acknowledges that mood is subjective, so no "gold standard" correctness checks needed

**Concerns**:
- Outlier detection is mentioned but not specified (what thresholds? what happens to flagged entries?)
- No plan for coordinated gaming (e.g., group of students intentionally skewing mood for a specific location as a prank)
- "Wellness staff may occasionally review aggregated trends" is vague and reactive, not systematic
- No attention checks to detect bots or users clicking randomly
- No redundancy mechanism (each user submits once per location per time period; no cross-validation)

**Recommendations**:
- Define specific outlier thresholds (e.g., >10 submissions in 1 hour flagged for review)
- Implement simple attention check: ask users to confirm location on map before submitting
- Add "report this entry" feature for community flagging of suspicious patterns
- Plan for manual review of first 100 submissions to calibrate automated filters

**Verdict**: QC is reasonable for subjective self-report data but lacks specificity. Adequate to prevent casual spam but vulnerable to coordinated manipulation if it becomes a target.

---

## RISK ANALYSIS

### Top 3 Risks & Mitigations

#### Risk 1: Cold-Start Failure (Critical)
**Impact**: Without 100+ active users, heatmap is sparse and value proposition collapses. Students won't participate if map looks empty.

**Likelihood**: High—recruitment strategy is currently vague and untested.

**Mitigation**:
- **Immediate action**: Secure 2-3 concrete partnerships THIS WEEK. Examples: NETS 2130 class (offer extra credit for 5 check-ins?), one dorm floor via RA contact, psychology research participant pool.
- **Seeding strategy**: Team and friends submit 50-100 check-ins across campus during week 1-2 to make initial map look populated.
- **Targeted launch**: Start with ONE high-density location (e.g., Hill College House or Engineering quad) rather than entire campus. Market as "Hill Mood Map" first, expand later.
- **Backup**: If organic recruitment fails by week 3, allocate $200 of budget to MTurk workers (Penn alumni, students from other cities) to simulate initial data.

**If unaddressed**: Week 4-5 will involve panic recruitment among friends, demo will show 30-50 total check-ins, heatmap will be too sparse to demonstrate value, project becomes a technical portfolio piece rather than crowdsourcing validation.

---

#### Risk 2: Participation Drops After Novelty Fades (High)
**Impact**: Students try the app once or twice, find streaks and badges insufficient motivation, stop checking in. Heatmap becomes stale.

**Likelihood**: High—busy students with competing demands, no immediate personal utility beyond self-reflection.

**Mitigation**:
- **Add personal value**: Emphasize personal mood journal and longitudinal tracking (you can see YOUR patterns over time) rather than community heatmap as primary value.
- **Reminder system**: Gentle push notifications or daily email reminders ("How are you feeling today?") if users opt in.
- **Social pressure**: If launching within a dorm or class, create explicit community goal ("Let's get 500 check-ins this week as a floor") to build accountability.
- **Time-limited campaigns**: "Midterm Stress Week" or "Finals Wellness Check" with specific start/end dates create urgency.
- **Lower frequency expectation**: Instead of daily check-ins, market as 2-3x per week to reduce burden.

**Backup**: If retention is low, pivot evaluation metrics from "consistent participation" to "snapshot of Penn mood during specific high-stress periods" (midterms, finals). Treat it as periodic survey rather than continuous tracking.

---

#### Risk 3: Technical Complexity Delays Launch (Medium)
**Impact**: Time spent on time-decay algorithms, geohash aggregation, and Firebase Cloud Functions delays working prototype, leaving insufficient time for user testing.

**Likelihood**: Medium—team has appropriate tech stack but features like scheduled jobs and real-time updates can have edge cases.

**Mitigation**:
- **Simplify aggregation initially**: Start with simple averaging per location (no time decay) to get working heatmap by end of week 2.
- **Add time decay later**: Once core loop works, implement exponential weighting in week 3-4 as enhancement.
- **Defer emails and analytics**: Weekly summaries and wellness dashboard are not essential for pilot; focus on submission and visualization.
- **Use Firebase SDKs extensively**: Lean on Firebase's built-in auth, real-time listeners, and Cloud Functions templates rather than custom infrastructure.
- **Manual aggregation as backup**: If scheduled jobs fail, team can run Python aggregation script manually for demo purposes.

**Backup**: If technical delays occur, demonstrate concept with static snapshots (e.g., "Here's what the heatmap looked like on [date] after collecting 100 check-ins") rather than real-time live system.

---

## DECISION GUIDANCE

### Verdict: WEAK GO / NEEDS REVISION (Score: 19/30)

**Overall Assessment**: MoodMap@Penn is a technically feasible and ethically sound project with thoughtful design, but **recruitment strategy is fatally vague** and **cold-start problem is unaddressed**. The project is currently at high risk of becoming a "beautiful empty platform" demo rather than a successful crowdsourcing validation.

---

### Critical Change Required

**Before proceeding, the team MUST**:

1. **Secure 2-3 concrete recruitment commitments** by end of Week 1:
   - Example A: "NETS 2130 class (60 students) will participate as part of course credit"
   - Example B: "Hill College House RA Sarah Chen will promote to her floor (80 residents) via GroupMe"
   - Example C: "Active Minds club (200-member mailing list) has agreed to feature us in next newsletter"

2. **Descope to targeted pilot** rather than campus-wide launch:
   - Choose ONE high-density location: specific dorm, specific school, specific club
   - Market as "[Location] Mood Map" (e.g., "Hill House Mood Map" or "Engineering Quad Mood Check")
   - 50-100 active users in concentrated area is better than 50-100 scattered across campus

3. **Implement seeding strategy**:
   - Team + friends commit to submitting 10-15 check-ins each during soft launch week
   - This creates initial data density so first "real" users see a populated map

4. **Add backup extrinsic incentive**:
   - Weekly raffle for $10-25 gift card among participants
   - Partner with CAPS/Wellness to offer co-branded participation incentive (e.g., free mindfulness workshop entry)

**If these changes are not made**, the project should pivot to:
- **Option A**: Mood journaling app with personal analytics (no crowdsourcing component)
- **Option B**: One-time mood survey with visualization (snapshot, not continuous tracking)
- **Option C**: Analyzing existing Penn wellness data (social media sentiment, CAPS utilization) rather than collecting new data

---

### Predicted Outcomes

#### Scenario A: Recruitment Strategy Improved (60% probability if changes made)
- **Week 1-2**: Team secures dorm floor or class commitment; builds core submission + heatmap
- **Week 3**: Soft launch with targeted promotion; 80-120 initial users submit 200-300 check-ins
- **Week 4**: Heatmap shows meaningful patterns; 60-70% retention for second week
- **Week 5**: Demo with 150-250 total users and 500-800 check-ins; clear mood patterns by location and time
- **Grade**: A-/B+ range—demonstrates crowdsourcing aggregation and gamification effectiveness
- **Learning**: Validated that targeted community deployment can overcome cold-start for niche social apps

#### Scenario B: Recruitment Remains Vague (70% probability without changes)
- **Week 1-3**: Team builds platform; "soft launch" gets 25-40 participants (mostly friends/teammates)
- **Week 4**: Panic recruitment via Reddit, GroupMe blasts; another 30-50 users trickle in
- **Week 5**: Demo with 60-90 total users, sparse heatmap, limited mood patterns visible
- **Grade**: B+/B range—technically competent but weak crowdsourcing demonstration
- **Learning**: Technical skills validated but crowdsourcing recruitment assumptions failed

#### Scenario C: Major Pivot Executed (30% probability if team recognizes risk early)
- **Week 1**: Team realizes recruitment is too uncertain; pivots to one of backup options above
- **Week 2-4**: Builds simplified version (personal journaling or one-time survey)
- **Week 5**: Demo with reduced scope but higher completion
- **Grade**: B range—pragmatic risk mitigation but reduced ambition

---

## COMPARISON TO V1 ANALYSIS

### What Changed from Round 2 to Round 3?

**Improvements**:
- ✅ Added Veda Mantena as Round 3 contributor (team growth)
- ✅ Expanded Octalysis incentive framework from Drive 1-2 to all 6 drives (more comprehensive)
- ✅ Added specific aggregation formula (weighted average with time decay)
- ✅ Clarified QC mechanisms (Penn email verification, rate-limiting, outlier detection)
- ✅ Specified technical workflow step-by-step (7 steps from login to weekly digest)
- ✅ Added "Community Challenges and Events" as 9th key feature

**Unresolved Issues from V1**:
- ❌ Recruitment strategy still vague ("partner with student orgs" without names or commitments)
- ❌ Cold-start problem acknowledged but not solved (backup plan is "dorm-specific pilot" without specifics)
- ❌ No evidence of user testing or validation of value proposition
- ❌ Sustainability problem (mentioned in V1) reframed but not addressed—still assumes voluntary participation will continue

**New Concerns Introduced**:
- ⚠️ Scope creep: Added "Community Challenges" and "Weekly Summary Insights" without descoping other features
- ⚠️ Python ML scripts mentioned in tech stack (new complexity not in earlier versions)

### V1 vs V2 Scoring Comparison

| Dimension | V1 Score (Implied) | V2 Score | Change | Notes |
|-----------|-------------------|----------|--------|-------|
| Technical Feasibility | ~4/5 | 4/5 | → | Remains appropriately scoped |
| Crowdsourcing Viability | ~3/5 | 3/5 | → | Cold-start problem still unaddressed |
| Incentive Design | ~3.5/5 | 3/5 | ↓ | More drives listed but still no concrete validation |
| Scope Appropriateness | ~4/5 | 4/5 | → | Slight feature creep but manageable |
| Recruitment Strategy | ~2/5 | 2/5 | → | **Critical gap remains unfixed** |
| Quality Control | ~3/5 | 3/5 | → | Slightly more specific but still basic |
| **TOTAL** | **~19-20/30** | **19/30** | → | **No meaningful improvement** |

### V1 Verdict vs V2 Verdict

**V1 Verdict**: "WEAK GO (conditional on immediate recruitment pivoting)"

**V2 Verdict**: "WEAK GO / NEEDS REVISION"

**Status**: Essentially unchanged. Round 3 added documentation and framework depth but did not address the fundamental execution risks identified in V1.

---

### Key Takeaway

**The team has done excellent academic and design work** (Octalysis framework, technical architecture, workflow specification) **but has not done the operational groundwork** (securing partnerships, testing recruitment, validating user interest). This is a classic "plan beautifully, execute vaguely" pattern common in academic projects.

**What V1 Analysis Predicted**: "Weeks 1-3 build beautiful app smoothly, week 4 'soft launch' gets 20-30 (mostly friends), heatmap sparse, value prop doesn't work without critical mass, week 5 panic recruitment."

**Current V2 Assessment**: This prediction remains accurate unless recruitment strategy is immediately operationalized. The project is better documented but not more likely to succeed without concrete partnerships.

---

## RECOMMENDATION

**This project can still succeed, but requires immediate action on recruitment**. Technical scope is fine; crowdsourcing design is fine; execution plan is weak.

**Action items for Week 1** (if team proceeds):
1. [ ] Email 3-5 student org leaders THIS WEEK for partnership commitments
2. [ ] Identify specific dorm or class for targeted pilot (not campus-wide)
3. [ ] Create seeding plan (team generates 50-100 initial check-ins)
4. [ ] Add small raffle incentive to budget ($50-100 for gift cards)
5. [ ] Build core loop (submit → display) by end of Week 2 to enable testing

**If these commitments cannot be secured by end of Week 1, strongly consider pivoting to a less recruitment-dependent crowdsourcing project.**

---

**Analysis by**: Claude Sonnet (NETS 2130 Project Evaluation)
**Viability Score**: 19/30 (Needs Major Revision)
**Recommendation**: Proceed with caution; immediate recruitment action required
