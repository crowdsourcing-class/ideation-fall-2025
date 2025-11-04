# TerraTruth - Project Viability Analysis (V2)

**Project**: TerraTruth - Volunteer-driven satellite imagery analysis for humanitarian causes
**Authors**: Alexander Mehta (amehta26), Brandon Yan (bdonyan), Josh Lee (jlee0902), Andrew Park (andrewpp)
**Analysis Date**: 2025-11-02
**Analyst**: NETS 2130 Course Staff

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| **1. Technical Feasibility** | 2/5 | Web app with PostGIS database, satellite data pipeline, weighted aggregation, and AI pre-filtering. Multiple complex systems (GIS, spatial queries, reputation engine, mission management). |
| **2. Crowdsourcing Viability** | 2/5 | Unpaid volunteers for humanitarian causes (intrinsic motivation) but no captive audience identified. Vague recruitment through "partner non-profits, university groups, social media" without specifics. |
| **3. Incentive Design** | 3/5 | Task time unclear (5-15 min per image tile?) with gamification + impact visibility. Intrinsic motivation appropriate for cause-driven work, but unclear if sufficient for sustained engagement. |
| **4. Scope Appropriateness** | 1/5 | 10 major features including AI pre-filtering, PostGIS database, weighted aggregation engine, partner portal, community forum. Cannot build core loop in 2 weeks. |
| **5. Recruitment Strategy** | 2/5 | General plan ("partner non-profits, university groups, social media") without specific channels named. No commitments or test recruitment. 50-500 volunteers needed. |
| **6. Quality Control** | 5/5 | Exceptional multi-layered QC: gold standard (10-15%), redundancy (3-5 workers), weighted voting by reputation, expert review (5-10%), statistical outliers, agreement metrics. |

**TOTAL SCORE: 15/30**

**Category**: **NEEDS MAJOR REVISION** (15-19 range)

---

## EXECUTIVE SUMMARY

TerraTruth is an ambitious volunteer-driven platform for analyzing satellite imagery to support humanitarian organizations. While the quality control architecture is sophisticated and the social mission compelling, the project faces critical feasibility challenges: massive technical scope for 5 weeks, unproven volunteer recruitment strategy, and fundamental expertise contradiction (untrained volunteers expected to catch "subtle signs" that automated systems miss). The team demonstrates strong technical knowledge and planning rigor, but execution within course constraints is highly unlikely without 70% descoping.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility: 2/5 - Very Risky

**What they're building:**
- React frontend with annotation tools
- Python Flask/Django backend with mission management
- PostgreSQL + PostGIS database for spatial queries
- Task management + quality control engine
- Weighted aggregation + reporting module
- AWS hosting (EC2, S3, RDS)
- AI-powered task pre-filtering module
- Gamification system with leaderboards
- Community collaboration forum
- Partner data portal with API

**Why this is risky:**
- **PostGIS complexity underestimated**: Spatial database queries, geographic data types, indexing for performance—not trivial for students unfamiliar with GIS
- **Satellite data pipeline**: Preprocessing 512×512 tiles from Sentinel-2/Landsat, handling geospatial metadata, serving through backend—2-3 weeks alone
- **Weighted aggregation engine**: Not just majority vote but reputation-weighted consensus with outlier detection—requires statistical sophistication
- **AI pre-filtering module**: Scans imagery to triage difficulty—this is computer vision ML, not a weekend feature
- **10 features total**: Even cutting the "nice-to-haves" (forum, leaderboards, AI), core loop is complex

**Red flags from rubric:**
- Multiple external APIs (Earth Engine, satellite data sources)
- GIS/geospatial pipelines (explicit red flag)
- Complex backend systems (reputation, aggregation, task routing)

**Two-week test**: Could they build working core loop (upload image → assign to worker → collect label → show result) in 2 weeks? Unlikely with PostGIS setup.

**Verdict**: Needs 3-4 week cushion. With 5-week timeline, very high risk of incomplete system.

---

### 2. Crowdsourcing Viability: 2/5 - Weak Value Proposition

**Their plan:**
- Target: "Volunteers recruited through partner non-profits, university groups, social media campaigns (targeting users interested in humanitarian/environmental causes)"
- Value proposition: Contributing to humanitarian causes + gamification + impact visibility
- Required scale: 50 minimum, 500 target

**Problems:**

**No captive audience:**
- Don't mention specific university clubs they're members of
- "Partner non-profits" (line 55) are aspirational, not secured
- No "I will post in my dorm's GroupMe" or "My club has 200 members"

**Network effects required:**
- Impact visibility depends on NGO feedback loops (takes months)
- Community forum only valuable once community exists
- Gamification (leaderboards) requires critical mass

**Task clarity concerns:**
- "Bounding boxes, object counts, damage assessments, land-use classifications"—these vary in difficulty
- Claim "no domain expertise required" but detecting "subtle" signs automation misses suggests expertise IS needed
- Training missions mentioned but effort to create these not factored into timeline

**Comparison to rubric examples:**
- Score 5: "Your class, dorm, club you're in"—they don't have this
- Score 2: "Benefits require scale OR unclear to users"—matches exactly

**Cold-start risk:**
- First 10 volunteers see empty impact dashboard (no stories yet)
- No NGO updates until partnerships formalized (Challenge 1)
- Gamification weak without community

**Verdict**: Recruitment is the Achilles heel. Without specific committed audiences, 50 volunteers is aspirational.

---

### 3. Incentive Design: 3/5 - Acceptable but Untested

**Task characteristics:**
- Time: Unclear, likely 5-15 min per image tile (annotating regions, selecting cause, confidence rating)
- Difficulty: Medium to high (visual pattern recognition, comparing features)
- Boredom: Moderate (some tiles interesting, many repetitive)

**Incentives offered:**
1. **Intrinsic**: Contributing to humanitarian causes
2. **Gamification**: Badges, leaderboards, "leveling up"
3. **Impact visibility**: "Your analysis was featured in this report"
4. **Community**: Forum for discussion

**Assessment:**

**Strengths:**
- Intrinsic motivation appropriate for cause-driven work
- Impact feedback loop (if working) is powerful motivator
- Progressive skill system keeps users engaged

**Weaknesses:**
- Impact visibility requires NGO partnerships (Challenge 1, unvalidated)
- Gamification alone insufficient for 5-15 min tasks per rubric
- Community forum only valuable at scale
- No backup if intrinsic motivation proves weak

**Rubric guidance:**
- "Task 2-10 min + tedious: Need payment or strong intrinsic motivation"
- They're betting entirely on intrinsic being "strong"
- No plan to add payment if volunteers churn

**Comparison to similar projects:**
- Zooniverse works because tasks are 30 seconds, not 5+ minutes
- Amnesty Decoders worked because time-limited campaign (urgency) + established brand
- TerraTruth has neither

**Verdict**: Incentive design reasonable on paper, but high risk without testing. No backup plan.

---

### 4. Scope Appropriateness: 1/5 - Fantasy

**Feature count:**
1. Mission-based cause selection
2. Reputation & skill system
3. Weighted aggregation engine
4. Impact visibility dashboard
5. Sensitive content filtering
6. Progressive training module
7. Partner data portal
8. AI-powered task pre-filtering
9. Gamified achievements & leaderboards
10. Community collaboration forum

**Core "must-have" features:**
Even cutting 8-10 (AI, gamification, forum), remaining 7 features are each substantial:
- Mission system: CRUD for missions, browsing, filtering
- Reputation system: Tracking accuracy against gold standard, updating scores
- Aggregation engine: Weighted voting, outlier detection, consensus logic
- Impact dashboard: Querying results, visualizations
- Content filtering: Opt-out preferences, metadata tagging
- Training module: Creating tutorials, checking answers
- Partner portal: API or export system for NGOs

**Scope test from rubric:**

1. **Two-week test**: "Could you build working demo of CORE loop in 2 weeks?"
   - Core loop: Create task → assign to worker → worker annotates → store result → aggregate
   - With PostGIS and satellite data pipeline? No.

2. **Manual simulation test**: "Could you manually simulate the system before building it?"
   - Yes, technically—Google Form with images → spreadsheet → weighted average
   - But gap between simulation and production system is enormous

3. **Must-have count**: "Can you name exactly 3-4 must-have features?"
   - They list 10, call features 1-7 essential
   - Even 7 is too many

**Technical debt not mentioned:**
- Creating gold-standard dataset (10-15% of 10,000 images = 1,000-1,500 expert-labeled tiles)
- Preprocessing satellite imagery into tiles
- Setting up PostGIS and learning spatial queries
- Building annotation UI (drawing bounding boxes, selecting categories)
- Testing aggregation algorithms with mock data

**Timeline implied:**
- Week 1: Database + backend setup
- Week 2: Frontend + annotation tools
- Week 3: QC mechanisms + aggregation
- Week 4: Recruitment + training content
- Week 5: Testing + NGO outreach

This is 10-15 person-weeks of work minimum.

**Verdict**: Scope is 3x what's feasible. Classic "building a startup in 5 weeks."

---

### 5. Recruitment Strategy: 2/5 - Vague Hope

**Their statement (line 55-56):**
"Primarily volunteers recruited through partner non-profits, university groups, social media campaigns (targeting users interested in humanitarian/environmental causes), and online volunteer portals."

**Specificity test:**

1. **Can you NAME the exact groups/places?**
   - No. "University groups" but not "Penn EcoReps" or "my environmental science class"
   - "Social media campaigns" but not "r/environment (500k subscribers)"
   - "Partner non-profits" but no partners secured

2. **Have you TESTED recruitment?**
   - No evidence of posting anywhere or getting commitments

3. **Do you need >50 people to start?**
   - Yes. Gold standard requires volume. Impact dashboard empty without scale.

4. **Can you seed it yourself?**
   - No. 10,000 images × 5 labels = 50,000 annotations. Team can't bootstrap.

**Rubric scoring:**
- Score 5: "My dorm's GroupMe (200 people), already talked to RA"
- Score 3: "Reddit communities, social media, MTurk" (their plan)
- Score 2: "Social media campaigns, word of mouth"

They're between 2-3. Calling it 2 because no specific subreddits named, no MTurk budget.

**Challenge 1 mitigation:**
- They acknowledge data partnerships take time
- Backup: Focus on public data (Landsat/Sentinel)
- But doesn't solve recruitment, just data sourcing

**Challenge 2 (volunteer engagement):**
- Mitigation: Gamification + impact dashboard + NGO updates
- Backup: Partner with university classes for "analysis drives"
- Backup is better than primary strategy (classes = captive audience)

**Critical insight:**
The backup plan (university classes, corporate CSR mapathons) should be the PRIMARY plan. These are concrete, committed audiences.

**Verdict**: Recruitment is fatal flaw. General channels without specifics or commitments = magic thinking.

---

### 6. Quality Control: 5/5 - Multi-layered and Sophisticated

**Mechanisms implemented:**

1. **Gold standard (10-15% of tasks)**
   - Randomly interspersed, workers can't distinguish
   - <70% accuracy after 20 tasks triggers retraining
   - Feeds into reputation score

2. **Redundancy (3-5 workers per task)**
   - Weighted majority voting using reputation
   - Ties (<60% agreement) requeued or flagged

3. **Expert review (5-10% random sample)**
   - Academic partners, NGO analysts, trained moderators
   - Corrections feed back to gold-standard dataset

4. **Statistical outlier detection**
   - Z-scores and inter-worker agreement variance
   - Flags anomalous annotations (e.g., 90% damaged)
   - Low-quality users excluded from aggregation

5. **Agreement metrics**
   - Cohen's kappa and Krippendorff's alpha
   - Low agreement (<0.5 kappa) → re-review

6. **Reputation system**
   - Continuous updates from gold-standard performance
   - Higher-reputation workers have more influence

7. **Weighted aggregation**
   - Numerical: weighted average by reputation
   - Categorical: weighted majority vote

**Why this scores 5/5:**
- Specific thresholds given (70% accuracy, 60% agreement, <0.5 kappa)
- Multiple layers catch different error types
- Feedback loops (expert reviews improve gold standard)
- Thoughtful handling of low-quality work (retraining vs. exclusion)
- Statistical rigor (kappa, z-scores) beyond typical projects

**Concerns:**
- Creating 1,000-1,500 gold-standard images (10-15% of 10k) is weeks of expert work—not factored into timeline
- Expert review depends on "academic partners" (not secured)
- System requires volume to work—cold-start problem

**Verdict**: QC design is excellent. Implementation depends on partnerships and scale they may not achieve.

---

## RISK ANALYSIS

### Risk 1: Recruitment Failure (Likelihood: Very High, Impact: Critical)

**Why critical:**
Without 50+ volunteers, entire system collapses. QC requires redundancy. Impact dashboard stays empty. Gamification has no community. NGOs receive no value.

**Warning signs:**
- No specific recruitment channels named
- No test posts or commitments
- No captive audience (class, club, dorm)

**Mitigation:**
1. **Week 1 action**: Post in 3 specific places with sample task
   - r/environment, r/volunteering (name them specifically)
   - Penn sustainability clubs (name which ones)
   - Measure completion rate
2. **Pivot trigger**: If <20% complete sample task, recruitment model broken
3. **Alternative**: Switch to university class partnerships (backup plan should be primary)

---

### Risk 2: Scope Overload Prevents Core System Completion (Likelihood: Very High, Impact: Critical)

**Why critical:**
If core annotation loop doesn't work by Week 4, no time for recruitment or iteration. Demo becomes mockup, not working system.

**Warning signs:**
- 10 features, 7+ marked essential
- PostGIS and satellite pipeline each multi-week tasks
- AI pre-filtering is ML project unto itself

**Mitigation:**
1. **Immediate descoping**: Cut to 3 features max
   - Feature 1: Upload image → display to worker → collect label
   - Feature 2: Redundancy (3 workers) + simple majority vote
   - Feature 3: Display aggregated result
2. **Defer everything else**: No reputation, no gamification, no AI, no forum
3. **Replace PostGIS**: Use regular PostgreSQL with lat/lng columns—spatial queries are overkill for MVP

---

### Risk 3: Expertise Mismatch Yields Low-Quality Data (Likelihood: High, Impact: High)

**Why critical:**
Fundamental contradiction: claim automated systems miss subtle signs (line 13-15) but untrained volunteers with "basic visual recognition" (line 62) will catch them. If AI misses it, humans likely will too unless trained.

**Warning signs:**
- Tasks require domain knowledge: "damage assessment," "land-use classification"
- Training missions create cognitive load, reduce participation
- Gold standard requires experts to create ground truth

**Mitigation:**
1. **Simplify tasks drastically**: Binary only (damaged/not damaged, vegetation/no vegetation)
2. **Focus on obvious signs**: "Can you see structures?" not "Is this conflict damage or construction?"
3. **Accept lower accuracy**: Aim for 70% vs. 95%—aggregate out noise with redundancy
4. **Partner with domain experts for task design**: Don't assume undergrads can replace automation

---

## DECISION GUIDANCE

### Verdict: **STOP AND PIVOT** (Score: 15/30)

Per rubric guidance for 15-19 range: "Project has multiple serious issues. Needs significant rethinking."

**Critical changes required:**

### 1. Slash Scope by 70% (Non-negotiable)

**Keep:**
- Web form for image labeling (text/radio buttons, no bounding boxes)
- Store labels in PostgreSQL (regular, not PostGIS)
- Aggregate with simple majority vote (3 workers per image)
- Display results on simple page

**Cut immediately:**
- ❌ PostGIS (use lat/lng columns)
- ❌ AI pre-filtering (manual task assignment)
- ❌ Reputation system (equal weights)
- ❌ Community forum
- ❌ Gamification beyond simple count
- ❌ Partner portal (share CSV)
- ❌ Impact dashboard (manual updates)

**Result**: Core loop buildable in 2 weeks, leaving 3 weeks for recruitment + iteration.

---

### 2. Solve Recruitment FIRST, Build Tech Second (Week 1 Priority)

**Week 1 actions (before writing code):**
1. Post sample task in 5 specific places:
   - r/environment (3M members)
   - r/volunteering (500k members)
   - Penn Climate Action
   - Penn Environmental Group
   - Anthropology/Geography department listservs
2. Measure: Do 50+ people complete sample task in 1 week?
3. Pivot trigger: If no, recruitment model broken

**If recruitment fails:**
- Option A: Partner with NETS 2130 class (classmates = captive audience)
- Option B: Pay for labels (MTurk, $0.10/image)
- Option C: Partner with ONE environmental science professor for class credit

---

### 3. Simplify Task to Match Worker Skill (Feasibility Fix)

**Current task:**
"Bounding boxes, object counts, damage assessments, land-use classifications"—requires training

**Simplified task:**
"Does this image show: (1) Healthy vegetation, (2) Damaged/stressed vegetation, (3) No vegetation"

**Rationale:**
- Binary decisions easier, faster (2 min vs. 10 min)
- Less training required
- Matches "basic visual recognition" claim
- Still provides value to NGOs

---

### Predicted Outcomes

**If no changes made (current plan):**
- **Week 1-3**: Team builds impressive backend (PostGIS, aggregation engine, satellite pipeline)
- **Week 4**: Realize no volunteers, panic recruitment via Facebook posts
- **Week 5**: Teammates + 10 friends label 200 images (40 each + 10 friends × 10 labels)
- **Demo**: Slick technical system, but crowdsourcing vestigial (most data from team)
- **Grade**: B for technical execution, C for crowdsourcing design, B overall
- **Feedback**: "Impressive system, but you didn't validate the crowd model"

**If critical changes made (pivot):**
- **Week 1**: Validate recruitment (100 sample tasks completed), prove viability
- **Week 2-3**: Build minimal annotation system (web form + majority vote)
- **Week 4**: Onboard volunteers, iterate based on feedback
- **Week 5**: Run full annotation campaign (1,000 images × 3 workers = 3,000 labels)
- **Demo**: Working system with real volunteer data, clear value
- **Grade**: A- for realistic scoping + execution, A for crowdsourcing design
- **Feedback**: "Great example of validating the model before overbuilding"

**If partial changes made (descope but don't fix recruitment):**
- **Week 1-2**: Build simple annotation system
- **Week 3-4**: Struggle with volunteer recruitment
- **Week 5**: Supplement with MTurk ($100 budget = 1,000 labels)
- **Demo**: Working system, mix of volunteers + paid workers
- **Grade**: B+ for pragmatic backup plan
- **Feedback**: "Good pivot to paid workers when volunteers lagged"

---

## COMPARISON TO V1 ANALYSIS

### What V1 Got Right:
- Identified scope as fatal flaw ("trying to build Zooniverse + GIS system")
- Called out recruitment vagueness ("50-500 volunteers from WHERE?")
- Noted expertise contradiction ("untrained volunteers spotting subtle signs")
- Praised sophisticated QC design
- Predicted outcome: impressive tech, vestigial crowdsourcing

### What V2 Adds:

**Structured rubric scoring:**
- V1 gave subjective "C+/D+" ratings
- V2 provides explicit 1-5 scores per dimension with rationale

**Actionable mitigation plans:**
- V1 said "solve recruitment FIRST" but didn't specify how
- V2 gives Week 1 action items (specific subreddits, success metrics, pivot triggers)

**Scope reduction specifics:**
- V1 said "cut 70%" generically
- V2 lists exactly what to keep vs. cut (PostGIS → regular Postgres, no AI, no forum)

**Risk likelihood + impact:**
- V1 listed flaws
- V2 prioritizes by probability × severity

**Predicted grade outcomes:**
- V1 gave single prediction
- V2 shows 3 scenarios (no change, full pivot, partial pivot) with likely grades

### Key Agreement:
Both analyses conclude **major revision required** and identify **recruitment + scope** as dual fatal flaws. V2 provides roadmap to fix them.

---

## CONCLUSION

TerraTruth demonstrates strong technical ambition and thoughtful quality control design, earning it recognition as a sophisticated project concept. However, the combination of massive scope (10 features including GIS and AI), unvalidated recruitment strategy (no specific channels or captive audience), and expertise contradictions makes successful execution within 5 weeks highly improbable.

**The core insight is sound**: Volunteers can contribute to humanitarian causes through image analysis. **The execution plan is not**: It's a 15-week project compressed into 5.

**Recommended path forward:**
1. Cut scope by 70% (simple annotation form, no GIS complexity)
2. Validate recruitment Week 1 with real test (100 completions)
3. Simplify task to binary decisions (healthy/stressed vegetation)
4. Use class partnerships as primary strategy, not backup

With these changes, TerraTruth could become an **A-level project** demonstrating validated crowdsourcing model. Without them, it will likely become a **B-level demo** of impressive but underutilized technology.

**Final Score: 15/30 - Needs Major Revision**
