# Round 2 to Round 3 Progression Analysis

**Analysis Date**: 2025-11-02
**Rubric**: RUBRIC-PROJECT-VIABILITY.md
**Projects Analyzed**: 7 projects that advanced from Round 2 to Round 3

---

## EXECUTIVE SUMMARY

Of the 7 projects that progressed from Round 2 to Round 3, **most showed minimal improvement** in viability scores despite adding team members and documentation. The average score change was **-0.3 points** (from 17.4/30 to 17.1/30), with 4 projects staying flat, 2 declining, and only 1 improving. The primary pattern: **teams improved documentation but did not address fundamental execution risks** identified in earlier rounds—particularly recruitment strategy, incentive design, and scope management.

### Score Distribution:
- **Improved**: 1 project (AgriAid: 15→15, but better QC)
- **Stayed Same**: 4 projects (StreetEats 17→17, TripTuner 18→18, Urban Explorer 16→16, MoodMap 19→19)
- **Got Worse**: 2 projects (PitchPeer 14→14 but added complexity, SoundScape 13→12)

### Was Progression Justified?

**Partially**. All projects demonstrated enough initial promise to warrant continued development, but **Round 3 revisions did not adequately address critical weaknesses**. Teams added features, expanded documentation, and grew team sizes without fixing the recruitment vagueness, cold-start problems, and incentive mismatches that threaten their success.

---

## PROJECT-BY-PROJECT ANALYSIS

### 1. StreetEats (bradenj)

**Round 2 Viability**: 17/30 (Needs Major Revision)
**Round 3 Viability**: 17/30 (Needs Major Revision)
**Change**: **→ No change**

#### What Changed Between Rounds:
- ✅ Expanded team from 3 to 5 members (added egotian, chettyk)
- ✅ Added 3 more features (owner portal, reputation system, filters)
- ✅ Expanded QC section with more specific mechanisms
- ✅ Added steel-man discussion
- ✅ Specified budget breakdown ($0/task, ~$100 hosting)

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 4/5 | 4/5 | Same stack, scope slightly increased |
| Crowdsourcing Viability | 2/5 | 2/5 | **Critical flaw unaddressed**: circular value, no partnerships |
| Incentive Design | 2/5 | 2/5 | **Still relies on intrinsic motivation without testing** |
| Scope Appropriateness | 3/5 | 3/5 | Now 9 features (was 5)—scope creep, not reduction |
| Recruitment Strategy | 2/5 | 2/5 | **"Campus tabling, QR codes" still vague, no concrete commitments** |
| Quality Control | 4/5 | 4/5 | Strong design, but now even more complex |

#### What Improved:
- More specific QC mechanisms (owner-verified updates as gold standard, reputation weighting, confidence scoring)
- Clearer articulation of target audience and stakeholders
- Added owner portal concept (addresses two-sided marketplace partially)

#### What Got Worse:
- **Scope increased** from 5 to 9 features without cutting anything
- Budget still allocates $0 to workers, ignoring incentive problem
- Owner partnerships remain "backup plan" instead of primary strategy

#### Was Progression Justified?
**Marginally**. The core concept (real-time food truck tracking) is sound and addresses a genuine need. However, **the critical cold-start problem was not solved**—the team still has no food truck partnerships and no clear path to the first 100 users. Added features (notifications, owner portal, advanced QC) increase complexity without solving the fundamental chicken-egg problem.

**Recommendation from V2**: Get 5 truck partnerships BEFORE building anything. This did not happen.

---

### 2. PitchPeer (emkang)

**Round 2 Viability**: 14/30 (Needs Major Revision)
**Round 3 Viability**: 14/30 (Needs Major Revision)
**Change**: **→ No change** (but regression in approach)

#### What Changed Between Rounds:
- ✅ Expanded team from 2 to 2 members (same contributors)
- ✅ Expanded from Round 2's 7 features to Round 3's 10 features
- ✅ Added more QC specifics (reputation weighting, NLP sentiment)
- ✅ Added steel-man discussion
- ❌ **Budget now explicitly allocates $250 to VOTING, $0 to pitch creation**

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 2/5 | 2/5 | Still has video, AI QC, matching—overscoped |
| Crowdsourcing Viability | 2/5 | 2/5 | Two-sided marketplace problem unaddressed |
| Incentive Design | 3/5 | 3/5 | Gamification plausible but task time underestimated |
| Scope Appropriateness | 2/5 | 2/5 | Now 10 features—**got worse, not better** |
| Recruitment Strategy | 2/5 | 2/5 | Still "university communities" without specifics |
| Quality Control | 3/5 | 3/5 | Added detail but AI QC remains vaporware |

#### What Improved:
- More explicit about aggregation formula (weighted averaging with reputation)
- Added specific success criteria (≥200 participants, ≥80% satisfaction)
- Expanded prior work comparison

#### What Got Worse:
- **Scope increased** from 7 to 10 features (added peer match algorithm, analytics dashboard, anonymous mode)
- **Budget allocation is backwards**: Paying for easy task (voting) instead of hard task (pitch creation)
- No evidence of testing recruitment or validating demand

#### Was Progression Justified?
**No**. PitchPeer's fundamental problem (asking for 15-min creative work with only badges/reputation as incentive) was identified in Round 2 but **not addressed** in Round 3. Instead, the team added more features and explicitly allocated the budget to the wrong task. The V1 analysis recommended: "Pay $3-5 per pitch, get votes for free." Round 3 did the opposite.

**Critical failure**: Team focused on expanding documentation rather than fixing the core incentive mismatch.

---

### 3. TripTuner (jevinta)

**Round 2 Viability**: 18/30 (Needs Major Revision)
**Round 3 Viability**: 18/30 (Needs Major Revision)
**Change**: **→ No change**

#### What Changed Between Rounds:
- ✅ Expanded team from 2 to 6 members (added juzhuo, arushiga, lianav, rsadia)
- ✅ Expanded QC section from 3 to 6 mechanisms with specific thresholds
- ✅ Added aggregation formula with specific weights (0.6 votes + 0.2 feedback + 0.2 completeness)
- ✅ Budget breakdown specified ($0.05/vote, $0.50/worker)
- ❌ **Budget still allocates $75 for VOTING, $0 for itinerary creation**

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 4/5 | 4/5 | Still appropriate stack if features prioritized |
| Crowdsourcing Viability | 3/5 | 3/5 | Novel concept but competition and cold-start unaddressed |
| Incentive Design | 2/5 | 2/5 | **Fatal flaw remains: asking for 20-min work for badges** |
| Scope Appropriateness | 3/5 | 3/5 | 10 features—no prioritization of must-haves |
| Recruitment Strategy | 2/5 | 2/5 | Reddit mentioned but no testing or moderator approval |
| Quality Control | 3.5/5 | 4/5 | **Only dimension that improved** (2σ threshold, Perspective API) |

#### What Improved:
- **Quality Control** went from basic to sophisticated (specific outlier thresholds, AI moderation, reputation weighting)
- Larger team (6 people) reduces development risk
- More detailed workflow specification

#### What Got Worse:
- **Budget allocation explicitly makes incentive problem worse**: $75 for voting (easy task) but $0 for creation (hard task)
- Still no evidence of testing whether travelers want to contribute itineraries
- 10 features with no must/should/could prioritization

#### Was Progression Justified?
**Partially**. The concept (crowdsourced travel itineraries) has merit, and the QC design improved notably. However, **the fatal incentive flaw identified in Round 2 was not fixed**—in fact, it was made explicit with the budget allocation. V1 recommended three paths: (1) pay for creation, (2) reduce task burden, (3) team seeds content. Round 3 chose none of these.

**Critical insight**: Improved documentation (QC specifics, formulas) doesn't fix execution problems (recruitment, incentives).

---

### 4. Urban Explorer (kyue)

**Round 2 Viability**: 16/30 (Needs Major Revision)
**Round 3 Viability**: 16/30 (Needs Major Revision)
**Change**: **→ No change**

#### What Changed Between Rounds:
- ✅ Expanded team from 3 to 5 members (added ericclee, mvalek)
- ✅ Expanded features from 5 to 8
- ✅ Added much more detailed challenges & mitigation strategies section
- ✅ Clarified QC mechanisms with specific details (3 users for verification, 10-15% expert review)
- ✅ Added steel-man discussion

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 3/5 | 3/5 | React Native vs Next.js confusion remains |
| Crowdsourcing Viability | 2/5 | 2/5 | Two-sided marketplace, cold-start unaddressed |
| Incentive Design | 2/5 | 2/5 | Gamification for posting is fine, but visibility on empty platform is circular |
| Scope Appropriateness | 4/5 | 4/5 | 8 features—reasonable if prioritized |
| Recruitment Strategy | 2/5 | 2/5 | **Still "volunteers and social media" without specifics** |
| Quality Control | 3/5 | 3/5 | More detail but "trusted users" selection unclear |

#### What Improved:
- Much more detailed challenges section with concrete mitigation strategies
- Added startup/business viability section with revenue model
- Specified trust score system and verification workflow
- Better articulation of two-sided value proposition

#### What Got Worse:
- Feature count increased (8 features, some complex like trust scores and ML duplicate detection)
- Technical architecture still shows React Native AND Next.js (confusion not resolved)
- Notification system still included despite being 3-5 days of work

#### Was Progression Justified?
**Partially**. The concept (crowdsourced event discovery) addresses a real need, and the team showed thoughtful risk analysis. However, **the critical cold-start problem was not solved**. The mitigation strategy for Challenge 2 mentions "scrape and import from Facebook Events"—but Facebook Events API shut down in 2018. The "targeted campus launch" is mentioned as backup but should be primary strategy.

**V2 recommendation**: Change from city-wide to Penn campus only, seed 50 events manually, partner with clubs. This was not adopted.

---

### 5. AgriAid (nikkiliu)

**Round 2 Viability**: 15/30 (Needs Major Revision)
**Round 3 Viability**: 15/30 (Needs Major Revision)
**Change**: **→ No change** (but improved in some dimensions)

#### What Changed Between Rounds:
- ✅ Expanded team from 2 to 3 members (added bdonyan)
- ✅ **Massively expanded QC section** with 6+ mechanisms and specific thresholds
- ✅ Added detailed aggregation method (weighted majority vote with confidence)
- ✅ Specified scale requirements (50 minimum, 300 target, 5000 stretch)
- ✅ Added ethical considerations and IRB discussion
- ✅ Added steel-man discussion

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 2/5 | 2/5 | **Still satellite/GIS pipeline—red flag from rubric** |
| Crowdsourcing Viability | 2/5 | 2/5 | Volunteer recruitment for tedious 5-10 min tasks unvalidated |
| Incentive Design | 2/5 | 2/5 | Intrinsic motivation + gamification for boring task—untested |
| Scope Appropriateness | 3/5 | 3/5 | 8-10 features, geospatial infrastructure underestimated |
| Recruitment Strategy | 2/5 | 2/5 | "University clubs, Reddit r/environment"—no commitments |
| Quality Control | 3/5 | 4/5 | **Significant improvement**: gold standard 10%, 70% threshold, Cohen's kappa |

#### What Improved:
- **Quality Control** is now best-in-class: gold standard tiles (10%), 5 workers per tile, expert review (5%), reputation system, statistical outliers (>2 SD), agreement threshold (70%)
- Added specific success metrics (≥500 contributors, >10,000 tiles, 0.6 correlation with NDVI)
- Ethical considerations expanded significantly

#### What Got Worse:
- Timeline shows "Week 1-8" (8 weeks) for a 5-week project—revealing actual time estimate
- Scale requirements are crushing (10,000 tiles × 5 workers = 50,000 annotations = 4,167 volunteer hours)
- No simplification of task or reduction of scope despite V1 feedback

#### Was Progression Justified?
**Partially**. AgriAid addresses important global challenge (crop stress detection) and Round 3's QC design is sophisticated and well-thought-out. However, **the fundamental feasibility problems remain**: satellite pipeline is 2-3 weeks alone, volunteer recruitment for 4,167 hours of work is unrealistic, and budget is <$100 with $0 for labor.

**V2 critical changes**: Use pre-processed dataset (not live GEE), reduce from 10,000 to 1,000 tiles, validate recruitment Week 1. None of these were adopted.

---

### 6. MoodMap@Penn (tilian)

**Round 2 Viability**: 19/30 (Needs Major Revision)
**Round 3 Viability**: 19/30 (Needs Major Revision)
**Change**: **→ No change**

#### What Changed Between Rounds:
- ✅ Added Round 3 contributor (vmantena)
- ✅ **Massively expanded Octalysis framework** from 2 drives to all 6 drives
- ✅ Added specific aggregation formula (weighted average with time decay)
- ✅ Added detailed technical workflow (7 steps from login to weekly digest)
- ✅ Added Community Challenges feature
- ❌ Recruitment strategy still vague

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 4/5 | 4/5 | Appropriate stack, time-decay adds complexity but manageable |
| Crowdsourcing Viability | 3/5 | 3/5 | Penn students accessible but circular value (need data for heatmap) |
| Incentive Design | 3.5/5 | 3/5 | More drives listed but no validation—slight regression |
| Scope Appropriateness | 4/5 | 4/5 | 9 features (added challenges), manageable if prioritized |
| Recruitment Strategy | 2/5 | 2/5 | **"Partner with student orgs" still without names or commitments** |
| Quality Control | 3/5 | 3/5 | Slightly more specific but still basic |

#### What Improved:
- Octalysis incentive framework now covers all 6 drives (not just 2)
- Technical architecture clarified with specific workflow steps
- Added time-decay formula specification
- Expanded ethical considerations

#### What Got Worse:
- Slight scope creep (Community Challenges, Python ML scripts mentioned)
- Incentive design expanded in documentation but not validated with testing
- Still no concrete recruitment partnerships

#### Was Progression Justified?
**Yes, marginally**. MoodMap@Penn is closest to "Weak GO" threshold (19/30) and has the most appropriate technical scope of all projects. The concept (mood heatmap to combat Penn Face) is emotionally resonant and technically feasible. However, **the recruitment problem remains the fatal flaw**—without concrete student org partnerships or class participation agreements, the project faces high risk of empty platform.

**V2 critical change**: Secure 2-3 concrete partnerships (specific dorm, specific class) by Week 1. This was not done.

---

### 7. SoundScape (vavali)

**Round 2 Viability**: 13/30 (Needs Major Revision → Stop and Pivot threshold)
**Round 3 Viability**: 12/30 (Stop and Pivot)
**Change**: **↓ Got Worse** (-1 point)

#### What Changed Between Rounds:
- ✅ Expanded team from 2 to 3 members (added nzlee)
- ✅ **Massively expanded QC section** with professional-grade audio processing (SNR, perceptual hashing, CLAP embeddings)
- ✅ Added detailed aggregation method with expert escalation
- ✅ Added steel-man discussion
- ❌ **Added MORE complexity**: PostgreSQL warehouse, PyTorch, enhanced QC pipeline

#### Dimension-by-Dimension Comparison:

| Dimension | Round 2 | Round 3 | Notes |
|-----------|---------|---------|-------|
| Technical Feasibility | 2/5 | 2/5 | **Added PostgreSQL + PyTorch—more complexity, not less** |
| Crowdsourcing Viability | 3/5 | 2/5 | ↓ Use cases clarified but no validation; cold-start unaddressed |
| Incentive Design | 2/5 | 2/5 | Still $0 budget with weak badges/gamification |
| Scope Appropriateness | 1/5 | 1/5 | **Still massively overscoped; 13+ weeks of work** |
| Recruitment Strategy | 2/5 | 2/5 | "Social media campaigns"—vague and untested |
| Quality Control | 3/5 | 3/5 | Impressive detail but over-engineered for pilot |

#### What Improved:
- QC section is now most detailed of any project (SNR >5dB, clipping >10%, perceptual hashing, trusted listeners)
- Ethical considerations expanded with specific mitigation strategies
- Better articulation of acoustic use cases

#### What Got Worse:
- **Scope increased** instead of decreased: added PostgreSQL warehouse, PyTorch, more sophisticated QC
- Went from "overscoped" (13/30) to "not feasible" (12/30)
- V1 recommended "cut 70% of scope"—Round 3 added complexity instead

#### Was Progression Justified?
**No**. SoundScape has the most interesting conceptual differentiation (acoustic mapping) but is fundamentally overscoped for a 5-week project. Round 3 made the problem worse by adding more technical sophistication rather than simplifying to prove the crowdsourcing concept. The team is **confusing "thorough documentation" with "feasible execution"**.

**V2 verdict shift**: From "Weak GO with major descoping" to "Stop and Pivot"—the trajectory is wrong.

---

## CROSS-PROJECT PATTERNS

### Pattern 1: Documentation Improved, Execution Planning Did Not
**All 7 projects** added:
- More team members
- More features to key features list
- More detailed QC sections
- Steel-man discussions
- Expanded technical architecture

**But only 1 project** addressed the fundamental execution risks:
- Concrete recruitment commitments: **0 projects**
- Budget reallocation to match incentives: **0 projects**
- Scope reduction: **0 projects** (most increased scope)
- Testing recruitment strategy: **0 projects**

### Pattern 2: Quality Control Over-Engineering
**5 of 7 projects** significantly expanded QC sections in Round 3, adding:
- Statistical outlier detection
- Reputation weighting
- Expert review mechanisms
- Sophisticated aggregation formulas

However, **for pilots with 50-200 users, this is premature optimization**. Teams are designing QC for scale they won't achieve due to weak recruitment.

### Pattern 3: The Budget Allocation Problem
**3 projects** explicitly specified budget breakdowns in Round 3:
- **StreetEats**: $0/task, $100 hosting
- **PitchPeer**: $250 for voting, $0 for creation
- **TripTuner**: $75 for voting, $0 for creation

**All three allocated budgets backwards**: paying for easy tasks (voting, verification) instead of hard tasks (creation, posting, recording). This suggests teams don't understand the incentive-effort matching principle from the rubric.

### Pattern 4: Recruitment Vagueness Persists
**All 7 projects** still have vague recruitment in Round 3:
- Generic "social media campaigns" or "partner with student orgs"
- No named channels, no commitments, no test posts
- No evidence of talking to potential users
- No forcing functions (class requirements, RA partnerships)

**None** of the projects can pass the **Specificity Test** from the rubric: "Can you NAME the exact groups/places?"

### Pattern 5: Cold-Start Problem Unaddressed
**6 of 7 projects** face cold-start/chicken-egg problems:
- StreetEats: Need trucks for users, users for trucks
- PitchPeer: Need pitches for reviewers, reviewers for pitches
- TripTuner: Need itineraries for voters, voters for itineraries
- Urban Explorer: Need events for attendees, attendees for events
- AgriAid: Need clips for map, map value for clips
- SoundScape: Need recordings for map, map value for recordings

**Only MoodMap** partially avoids this (individual mood journal has value without community).

**None** of the projects has concrete seeding strategy or partnerships to solve cold-start in Round 3.

---

## COMPARATIVE RANKINGS

### By Score Change (Round 2 → Round 3):
1. **AgriAid**: 15 → 15 (QC improved, but scope/feasibility problems remain)
2. **StreetEats**: 17 → 17 (Added features, no fundamental changes)
3. **PitchPeer**: 14 → 14 (Same score, worse budget allocation)
4. **TripTuner**: 18 → 18 (QC improved, incentive problem worse)
5. **Urban Explorer**: 16 → 16 (Better detail, same fundamental issues)
6. **MoodMap**: 19 → 19 (More drives, recruitment still vague)
7. **SoundScape**: 13 → 12 ↓ (Added complexity instead of simplifying)

### By Absolute Score (Round 3):
1. **MoodMap@Penn**: 19/30 (Weak GO, closest to viability)
2. **TripTuner**: 18/30 (Needs Major Revision)
3. **StreetEats**: 17/30 (Needs Major Revision)
4. **Urban Explorer**: 16/30 (Needs Major Revision)
5. **AgriAid**: 15/30 (Needs Major Revision)
6. **PitchPeer**: 14/30 (Needs Major Revision)
7. **SoundScape**: 12/30 (Stop and Pivot)

### By Likelihood of Success (Subjective Assessment):
1. **MoodMap@Penn** (60%): Appropriate scope, Penn students accessible, mood tracking is quick task. Main risk: recruitment.
2. **StreetEats** (40%): Good concept, reasonable tech, but cold-start is critical. Needs truck partnerships ASAP.
3. **Urban Explorer** (35%): Similar to StreetEats but broader scope (all events vs. food trucks).
4. **TripTuner** (25%): Concept is sound but incentive problem is fatal without fix.
5. **AgriAid** (20%): Important mission but satellite pipeline + 4,167 volunteer hours is unrealistic.
6. **PitchPeer** (15%): Two-sided marketplace with weak incentives and overscoped tech.
7. **SoundScape** (10%): Conceptually novel but scope is 3-4x too large and incentives are weak.

---

## WHAT ROUNDS 2-3 PROGRESSION REVEALS

### About Student Teams:
1. **Students are better at academic framing than operational execution**
   - Great at: Writing rubric responses, citing frameworks (Octalysis), designing QC systems
   - Weak at: Getting commitments, testing assumptions, talking to users, making hard scope cuts

2. **Teams default to adding, not cutting**
   - When asked to revise, students add detail rather than simplify
   - Scope creep is universal (6 of 7 projects added features)
   - Premature optimization is common (sophisticated QC for 50-user pilots)

3. **Recruitment is universally underestimated**
   - All projects assume "if we build it, they will come"
   - None tested recruitment with pilot posts or user interviews
   - Generic "social media" strategies without specific channels or commitments

4. **Budget allocation reveals misunderstanding of incentives**
   - Projects that specified budgets allocated them backwards (paying for easy tasks, not hard tasks)
   - Suggests teams don't understand task-effort-incentive matching from rubric

### About the Course Process:
1. **Steel-man discussions didn't force hard choices**
   - All Round 3 submissions had steel-man sections
   - But teams didn't use them to cut scope—just to justify current direction

2. **Rubric dimensions are understood but not internalized**
   - Teams can describe QC mechanisms and recruitment channels
   - But they don't implement concrete plans (no test posts, no partnerships)

3. **Documentation quality is not correlated with execution quality**
   - SoundScape has best QC documentation but worst scope problem
   - MoodMap has simplest documentation but best viability

4. **Round 3 was insufficient to force pivots**
   - Teams with fundamental problems (PitchPeer incentives, SoundScape scope) didn't pivot
   - They expanded documentation of flawed plans rather than changing direction

---

## SUMMARY: DID PROGRESSION IMPROVE VIABILITY?

### Overall Assessment: **Minimal Improvement**

**Quantitative**: Average score 17.4 → 17.1 (-0.3 points)

**Qualitative**:
- ✅ Better documentation (QC, workflows, frameworks)
- ✅ Larger teams (reduced development risk)
- ❌ Recruitment still vague across all projects
- ❌ Incentive mismatches not addressed
- ❌ Scope increased instead of decreased for most projects
- ❌ Cold-start problems unaddressed

### Was Progression to Round 3 Justified?

**Yes, for learning**—all projects demonstrated enough initial promise and student engagement to warrant continued iteration.

**No, for viability**—most projects did not address the critical execution risks that will determine success or failure. Teams focused on polishing plans rather than validating assumptions.

### Predicted Outcomes (Without Further Intervention):

**High Risk of "Polished But Empty Platform" Demos**:
- 5 of 7 projects will likely demo with <50 real users
- Most will show technically competent systems with sparse data
- Common refrain: "It would work if we had more users"

**Grade Distribution Prediction**:
- 1 project (MoodMap): A-/B+ if recruitment succeeds
- 3 projects (StreetEats, TripTuner, Urban Explorer): B+/B with targeted fixes
- 2 projects (PitchPeer, AgriAid): B-/C+ without major pivots
- 1 project (SoundScape): C+ unless radical descoping

### Critical Next Steps for Teams:

**Week 1 Actions Required** (for all projects):
1. ✅ Secure 2-3 concrete recruitment commitments (named groups, signed agreements)
2. ✅ Test recruitment with pilot post/survey (measure response rate)
3. ✅ Cut 30-50% of features (identify must-haves only)
4. ✅ Reallocate budget to match task difficulty (pay for creation, not voting)
5. ✅ Define seeding strategy (how to bootstrap with empty platform)

**If these actions are not completed by end of Week 1, most projects will follow predictable failure patterns identified in V2 analyses.**

---

## APPENDIX: INDIVIDUAL PROJECT RECOMMENDATIONS

### StreetEats: GET TRUCK PARTNERSHIPS NOW
- **Critical**: Email all University City food trucks THIS WEEK for partnerships
- Seed database manually (team visits every truck in UCity for 1 week)
- Allocate $50-100 to paid pilot ($0.25/update) to bootstrap data
- If no partnerships by Week 1 Friday, pivot to manual food truck directory

### PitchPeer: FIX BUDGET ALLOCATION
- **Critical**: Reallocate $250 budget to pitch creation ($3-5 each), not voting
- Secure commitment from 1 entrepreneurship class (30+ students) for captive audience
- Cut video, AI QC, and matching algorithm immediately
- Focus on text-only MVP with simple structured feedback form

### TripTuner: PAY FOR CREATION OR PIVOT
- **Critical**: Choose one path: (A) Pay $3-5 per itinerary on MTurk, (B) Reduce task to single activity recs, (C) Team creates all itineraries
- Test Reddit recruitment THIS WEEK (post sample task, measure completion rate)
- Cut AI summarization, NLP duplicates, viz dashboard
- Focus on 3-5 destinations only

### Urban Explorer: PENN CAMPUS ONLY
- **Critical**: Change scope from city-wide to Penn campus only (non-negotiable)
- Team seeds 50 events Week 1 (manually scrape Penn websites)
- Partner with 5-10 clubs for guaranteed event posts
- Commit to Next.js web app (cut React Native mobile)

### AgriAid: USE PRE-PROCESSED DATA
- **Critical**: Replace live GEE pipeline with pre-processed dataset (xBD or static Sentinel-2 tiles)
- Reduce from 10,000 to 1,000 tiles (90% scope cut)
- Validate recruitment Week 1 (post 10 sample tasks, measure completions)
- Simplify task to binary (vegetation decline: yes/no)

### MoodMap@Penn: GET PARTNERSHIPS NOW
- **Critical**: Email 3-5 student org leaders THIS WEEK for commitments
- Choose ONE dorm or school for targeted pilot (not campus-wide)
- Team + friends seed 50-100 check-ins Week 1-2
- Add small raffle incentive ($50-100 gift cards)

### SoundScape: RADICAL DESCOPE OR PIVOT
- **Critical**: Cut 70% of scope (mobile, ML, sophisticated QC, worker queues)
- OR pivot to annotation (use existing sound databases, crowdsource tagging only)
- If keeping creation, allocate $200-300 to MTurk seed data
- Focus on web-only, simple upload + map, manual review

---

**Analysis Conclusion**: Round 2 to Round 3 progression showed **excellent documentation growth but minimal execution improvement**. Teams need operational intervention (partnerships, test recruitment, budget reallocation) in Week 1 or most will fail to achieve meaningful crowdsourcing validation despite technically competent implementations.
