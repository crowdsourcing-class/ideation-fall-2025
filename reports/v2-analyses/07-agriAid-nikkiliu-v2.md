# AgriAid - Project Viability Analysis (V2)

**Project**: AgriAid - Crowdsourced crop stress detection from satellite imagery
**Authors**: Nikki Liu (nikkiliu), Jevin Ta (jevinta), Brandon Yan (bdonyan)
**Analysis Date**: 2025-11-02
**Analyst**: NETS 2130 Course Staff

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| **1. Technical Feasibility** | 2/5 | Satellite data pipeline (Google Earth Engine API), NDVI computation, image preprocessing, geospatial database, and ML-ready dataset. Multiple complex systems (GIS, computer vision, statistical aggregation). |
| **2. Crowdsourcing Viability** | 2/5 | Unpaid volunteers for tedious image labeling (5-10 min tasks). No captive audience identified. Recruitment from "university clubs, social media" without specifics. Weak value proposition for volunteers. |
| **3. Incentive Design** | 2/5 | Intrinsic motivation (climate impact) + gamification (leaderboards, badges). Task is 5-10 minutes of visual comparison—rubric says this requires payment or strong intrinsic motivation. Untested assumption volunteers will sustain engagement. |
| **4. Scope Appropriateness** | 3/5 | 8 features with reasonable core (label images, aggregate, display). Some complexity (confidence scoring, dashboard, data export) but not egregious. Main concern: geospatial infrastructure underestimated. |
| **5. Recruitment Strategy** | 2/5 | Vague: "university clubs, social media (Reddit r/environment, Discord climate servers)" (line 57). Mentions specific channels but no test recruitment or commitments. Academic credit mentioned but no partnership secured. |
| **6. Quality Control** | 4/5 | Strong multi-layered QC: gold standard (10%), redundancy (5 workers), expert review (5% random sample), reputation system, statistical outliers (>2 SD), agreement metrics (70% threshold, Cohen's kappa). Specific thresholds given. |

**TOTAL SCORE: 15/30**

**Category**: **NEEDS MAJOR REVISION** (15-19 range)

---

## EXECUTIVE SUMMARY

AgriAid is a well-intentioned citizen science project targeting agricultural crisis detection through crowdsourced satellite image labeling. The social impact mission is compelling, and the quality control framework is sophisticated with specific metrics. However, the project suffers from critical feasibility challenges: massive technical complexity (satellite data pipelines, geospatial processing, NDVI correlation), unvalidated volunteer recruitment strategy, and a fundamental expertise contradiction (if automated NDVI systems miss subtle stress signs, untrained volunteers likely will too). The 10,000-tile labeling goal requires 50,000 person-annotations (5 per tile)—approximately 4,167 volunteer hours—which is unrealistic to achieve with vague recruitment plans in a 5-week timeline.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility: 2/5 - Very Risky

**What they're building:**
- Frontend: Streamlit or React for image labeling interface
- Backend: Python Flask API for task assignment
- Database: Firebase/Firestore for user profiles and labels
- Image source: Google Earth Engine API serving preprocessed tiles
- Computation: Python + NumPy + OpenCV for preprocessing, NDVI computation, consensus logic
- Visualization: Interactive world map dashboard
- Data export: ML-ready labeled dataset

**Why this is very risky:**

**Complexity 1: Satellite data pipeline (Weeks 1-2)**
- Google Earth Engine (GEE) API integration requires learning GEE's JavaScript/Python API
- Retrieving before/after Sentinel-2 tiles: querying by region, date range, cloud cover
- Preprocessing: Enhancing color/contrast, computing NDVI (Normalized Difference Vegetation Index)
- Tiling: Segmenting large images into 512×512 pixel tiles
- Storage: S3 or Cloud Storage for serving tiles
- **Estimate**: 2-3 weeks for someone unfamiliar with geospatial data

**Complexity 2: Image preprocessing + NDVI (Week 2)**
- NDVI formula: `(NIR - Red) / (NIR + Red)` where NIR = Near-Infrared band
- Requires understanding spectral bands, atmospheric correction, cloud masking
- OpenCV for color enhancement (histogram equalization, contrast adjustment)
- **Estimate**: 1-2 weeks to implement correctly

**Complexity 3: Task assignment system (Week 2-3)**
- Each tile assigned to ≥5 workers (line 103)
- Gold standard tiles (10%) interspersed randomly (line 138)
- State management: pending, in-progress, completed
- Worker eligibility: track who has labeled what (prevent self-redundancy)
- **Estimate**: 1 week

**Complexity 4: Aggregation engine (Week 3-4)**
- Weighted majority vote using inter-rater agreement + self-confidence (line 129)
- Statistical outlier detection (>2 SD from consensus, line 148)
- Agreement metrics: Cohen's kappa, Krippendorff's alpha (line 150)
- Tie-breaking for low-confidence results (<70% agreement)
- **Estimate**: 1-2 weeks

**Complexity 5: Visualization dashboard (Week 4-5)**
- Interactive world map (likely Mapbox or Leaflet)
- Overlay aggregated stress labels on regions
- Real-time updates as labels come in
- **Estimate**: 1 week

**Total estimated effort**: 6-9 weeks of full-time work for experienced geospatial engineer. Team has 5 weeks with 3 people.

**Red flags from rubric:**
- "Complex ML (audio, video, satellite imagery)"—satellite explicitly listed
- "GIS/geospatial pipelines"—explicit red flag
- "Multiple external APIs"—GEE API + mapping service

**Two-week test:**
Could they build core loop (fetch tile → display to user → collect label → store) in 2 weeks?
- **Maybe**, if GEE experience exists and cutting NDVI, aggregation, dashboard
- **Unlikely** if learning GEE from scratch

**Scope underestimation warning (line 281-283):**
"Week 1-2: Data collection & UI prototype. Week 3-4: Launch MVP + initial crowd recruitment. Week 5-6: Implement QC + aggregation dashboard. Week 7-8: Finalize visualizations + evaluation report."

This is an 8-week timeline presented as timeline, but project is 5 weeks. Either typo or revealing their true time estimate.

**Verdict**: Satellite pipeline alone is 2-3 weeks. Cannot build full system in 5 weeks without cutting 70%.

---

### 2. Crowdsourcing Viability: 2/5 - Weak Value Proposition

**Their plan:**
- **Target**: "University environmental clubs, social media (Reddit r/environment, Discord climate servers), and student science courses offering participation credit" (line 57-58)
- **Value proposition**: "Contribution to climate resilience and global food security" (intrinsic) + leaderboards/badges (gamification) + academic credit (extrinsic for some)
- **Required scale**: 50-100 minimum, 300-500 target, 5000+ stretch

**The fundamental problem: Task-incentive mismatch**

**Task characteristics:**
- **Time**: 5-10 minutes per tile (line 59 says "compare two images and detect subtle color/texture changes")
- **Cognitive load**: High—visual pattern recognition, distinguishing healthy vs. stressed vegetation, selecting cause (drought, flood, pests)
- **Boredom**: High—looking at brown/green pixels for hours
- **Skill required**: Claim "basic visual recognition" (line 63) but detecting "subtle changes" suggests training needed

**Incentives offered:**
- **Intrinsic**: Climate/food security impact
- **Gamification**: Leaderboards, badges, "Top Contributor" profiles (line 70-71)
- **Academic credit**: "Optional extra-credit participation for university volunteers" (line 71)

**Rubric assessment (Dimension 3):**
- "Task 2-10 min + tedious: Need payment or strong intrinsic motivation"
- AgriAid bets entirely on intrinsic motivation being "strong enough"
- Gamification alone insufficient for 5-10 min tasks (rubric: works for <2 min tasks)

**Comparison to successful citizen science:**

| Project | Task Time | Incentive | Success? |
|---------|-----------|-----------|----------|
| Zooniverse | 30 sec - 2 min | Discovery + badges | Yes (millions of volunteers) |
| Foldit | 15+ min | Puzzle-solving fun | Yes (dedicated community) |
| iNaturalist | 2-5 min | Personal species log | Yes (50M observations) |
| AgriAid | 5-10 min | Impact + badges | Unvalidated |

AgriAid's task is longer than Zooniverse, less intrinsically fun than Foldit, and less personally relevant than iNaturalist.

**No captive audience:**
- "University clubs"—which clubs? Are team members in them?
- "Reddit r/environment"—3M subscribers, but post success rate <1% (most posts get 0 replies)
- "Discord climate servers"—unnamed
- "Student science courses"—no partnership secured (line 71 says "offering" not "offered")

**Scale requirements are crushing:**
- 10,000 tiles × 5 workers per tile = **50,000 annotations**
- At 5 min/annotation = **4,167 volunteer hours**
- At 100 volunteers = 42 hours each (unrealistic)
- At 500 volunteers = 8 hours each (still high)

**Rubric scoring:**
- Score 5: "Captive audience—your class, dorm, club you're in"
- Score 2: "Weak value—benefits require scale OR unclear to users"
- AgriAid is Score 2: volunteers won't see their impact for months (until NGO uses data)

**Verdict**: Task too tedious, incentives too weak, no captive audience. High risk of 90% churn after 1-2 tasks.

---

### 3. Incentive Design: 2/5 - Mismatch

**Task analysis:**
- **Time**: 5-10 minutes (compare before/after satellite images, classify vegetation health, select likely cause, rate confidence)
- **Effort**: Medium to high (cognitive load of visual comparison)
- **Boredom**: High (repetitive, not inherently engaging like games or personal interest)

**Incentive structure:**

**1. Intrinsic motivation: "Climate resilience and global food security" (line 69)**
- **Strength**: Powerful for committed environmentalists
- **Weakness**: Requires volunteers to trust their work matters
- **Problem**: Feedback loop is months-long (NGOs use data → publish report → cite AgriAid)
- **During 5-week course**: No impact stories to share (Challenge 1 in TerraTruth faced same issue)

**2. Gamification: Leaderboards, badges, "Top Contributor" profiles (line 70-71)**
- **Appropriate for**: 30-sec to 2-min tasks (per rubric)
- **AgriAid task**: 5-10 min (too long for gamification alone)
- **Problem**: Leaderboards require community (first 10 volunteers see empty leaderboard)

**3. Academic credit: "Optional extra-credit participation" (line 71)**
- **Potentially strong**: Students motivated by grades
- **Problem**: Not secured—says "offering" not "arranged with Professor X"
- **Risk**: If no partnership, this incentive evaporates

**Rubric guidance:**
- "Task 5-10 min + tedious → Need small payment + reputation" (Score 3: Acceptable)
- "Task > 10 min → MUST pay or have captive audience" (Score 2: Mismatch if task takes >10 min)

AgriAid is borderline. If task is 5 min, Score 3. If task is 10+ min, Score 2.

**Formula check:**
`If (Task Time × Boredom Level) > (Incentive Value), then you have a problem.`
- Task Time: 7.5 min (average of 5-10)
- Boredom Level: 7/10 (repetitive visual comparison)
- Incentive Value: 5/10 (deferred impact + weak gamification + unvalidated academic credit)
- 7.5 × 7 = 52.5 > 5 × 10 = 50 → **Problem confirmed**

**What's missing:**

1. **No immediate feedback loop**:
   - Volunteers don't see "your label helped detect drought in Region X"
   - All feedback deferred until research published (months/years)

2. **No backup payment plan**:
   - If volunteers churn, no MTurk budget mentioned
   - Budget is "<$100 (hosting, storage, APIs)" (line 77)—assumes zero labor cost

3. **No proof of concept**:
   - Haven't tested if anyone completes even 1 tile
   - Could post 10 sample tiles on Reddit r/environment this week—haven't done so

**Verdict**: Incentive design assumes strong intrinsic motivation but hasn't validated it. High risk of volunteer churn after novelty wears off.

---

### 4. Scope Appropriateness: 3/5 - Risky

**Features listed (lines 43-52):**
1. Before/After Image Labeling
2. Multi-Class Classification (healthy, stressed, bare, cause)
3. Confidence Scoring (1-5 self-report)
4. Interactive Global Dashboard
5. Redundant Labeling & Consensus (≥5 users)
6. Gamification (leaderboards, badges)
7. Quality Control Layer (gold standard, reliability scoring)
8. Data Export for Research (ML-ready dataset)

**Core "must-have" features:**
- Feature 1 (image labeling): Display before/after images, collect classification + cause + confidence
- Feature 2 (multi-class): Dropdown or radio buttons for classification
- Feature 5 (redundancy): Task assignment logic (5 workers per tile)
- Feature 7 (QC): Gold standard checking, outlier detection

**"Should-have" features:**
- Feature 3 (confidence): Adds slider/rating to UI (1 day)
- Feature 6 (gamification): Leaderboard query + display (2 days)
- Feature 8 (data export): CSV/JSON download (1 day)

**"Could-have" features:**
- Feature 4 (dashboard): Interactive map with aggregated results (1 week)

**Scope test from rubric:**

1. **Two-week test**: "Could you build working demo of CORE loop in 2 weeks?"
   - Core loop: Fetch tile → display to user → collect label → store → aggregate
   - **With GEE pipeline**: No (pipeline is 2 weeks itself)
   - **With pre-fetched tiles**: Yes

2. **Manual simulation test**: "Could you manually simulate the system before building it?"
   - Yes—Google Form with image pairs → collect responses in Sheets → calculate majority vote
   - But gap between simulation and production is GEE pipeline (the hard part)

3. **Must-have count**: "Can you name exactly 3-4 must-have features?"
   - They list 8 features, likely 5-6 are essential
   - Slightly over ideal

**Technical debt not accounted for:**
- **Creating gold-standard dataset**: 10% of 10,000 tiles = 1,000 tiles need expert labels (line 138)
  - Estimate: 5 min/tile × 1,000 = 83 hours of expert time
  - Who are the experts? "Graduate researchers" (line 142)—are they committed?
- **NDVI ground truth**: Success metric is "≥0.6 Pearson correlation with NDVI" (line 162)
  - Must compute NDVI for all tiles to validate
  - Adds complexity to evaluation

**Timeline confusion (line 280-283):**
"Week 1-2: Data collection & UI prototype. Week 3-4: Launch MVP + initial crowd recruitment. Week 5-6: Implement QC + aggregation dashboard. Week 7-8: Finalize visualizations + evaluation report."

This is 8 weeks. Course is 5 weeks. Either:
- Typo (meant 5 weeks, miscounted)
- Revealing (true time estimate is 8 weeks)

**Verdict**: Feature list is reasonable (8 features, 5-6 essential). Real scope problem is geospatial infrastructure, not feature creep. Scores 3/5 because features are manageable if pipeline was easy—but pipeline is not.

---

### 5. Recruitment Strategy: 2/5 - Vague Hope

**Their plan (line 57-58):**
"University environmental clubs, social media (Reddit r/environment, Discord climate servers), and student science courses offering participation credit."

**Specificity test:**

1. **Can you NAME the exact groups/places?**
   - **Partially**: "Reddit r/environment" is specific (3M subscribers)
   - **Vague**: "Discord climate servers"—which ones? "University environmental clubs"—which universities, which clubs?
   - **Not committed**: "Student science courses offering credit"—no professor named, no partnership

2. **Have you TESTED recruitment?**
   - No evidence of test post
   - Could post 10 sample tiles on r/environment today—haven't done so

3. **Do you need >50 people to start?**
   - Yes. 10,000 tiles × 5 workers = 50,000 annotations. Can't bootstrap with team.

4. **Can you seed it yourself?**
   - No. 50,000 annotations at 5 min each = 4,167 hours. Team (3 people × 5 weeks × 40 hours = 600 hours) can do ~7,200 annotations max (14% of goal).

**Challenge 1 mitigation (line 181-183):**
- **Strategy**: "Gamification, progress tracking, social sharing"
- **Backup**: "Run labeling drives with university clubs"
- **Assessment**: Backup plan (labeling drives) is more concrete than primary plan. Should be reversed.

**Rubric scoring:**
- Score 5: "My dorm's GroupMe (200 people), already talked to RA"
- Score 4: "5 specific Facebook groups, 3 subreddits with mod approval"
- Score 3: "Reddit communities, social media, MTurk"
- Score 2: "Social media campaigns, word of mouth"

AgriAid is between 2-3. They name r/environment (specific) but don't mention mod approval or test post. Calling it **Score 2** because "Discord climate servers" is vague and academic credit is unconfirmed.

**Critical insight:**
"Labeling drives with university clubs" (backup plan) is the most viable strategy. Organized events with committed attendees > hoping strangers on Reddit participate.

**Scale reality check:**
- r/environment: 3M subscribers but <0.1% engagement on typical post
- Optimistic: 1,000 views → 10 click-throughs → 2 complete 10+ tiles each = 20 tiles labeled
- Need 10,000 tiles × 5 = 50,000 annotations
- Would need 2,500 successful Reddit posts (impossible)

**Verdict**: Names some specific channels (r/environment) but no test, no commitments, no realistic path to 50,000 annotations. Optimistic at best, magical thinking at worst.

---

### 6. Quality Control: 4/5 - Thoughtful

**Mechanisms listed (lines 137-152):**

1. **Gold standard (10% of tasks)**
   - Known answers from expert ground truth (line 138)
   - Workers <70% accuracy after... wait, "after 20 tasks" not specified, just "<70% accuracy" (line 138)
   - Still, clear threshold

2. **Redundancy (5 workers per task)**
   - Higher than typical (many systems use 3)
   - Appropriate for subjective visual judgments (line 140)

3. **Expert review (5% random sample)**
   - Graduate researchers review subset (line 142)
   - Corrections feed back into training—good feedback loop

4. **Reputation system**
   - "Reliability increases with consistent agreement" (line 146)
   - High-reliability workers' labels weighted more (line 129)

5. **Statistical outlier detection**
   - Removes labels >2 SD from consensus (line 148)
   - Standard statistical practice

6. **Agreement metrics**
   - 70% agreement threshold for "verified" labels (line 150)
   - Cohen's kappa mentioned (good choice for inter-rater reliability)

**Aggregation method (line 129):**
"Weighted majority vote using both inter-rater agreement and self-confidence scores."
- Sophisticated approach (not just simple majority)
- Combines objective (agreement) and subjective (confidence) signals

**Handling low-quality work (line 155):**
"Low-agreement labels are discarded and re-tasked to new users; persistent low-accuracy users lose ranking visibility."
- Reasonable approach (re-task, not punish immediately)
- "Lose ranking visibility" is soft penalty (not banned, just demoted)

**Why this scores 4/5, not 5/5:**

**Strengths:**
- Multiple layers (6 mechanisms)
- Specific thresholds (70% agreement, >2 SD outliers, 5 workers)
- Statistical rigor (Cohen's kappa, weighted voting)
- Feedback loops (expert corrections → gold standard)

**Weaknesses:**
- Gold standard creation plan vague: "Expert ground truth" but experts not secured (line 142 says "graduate researchers"—which ones?)
- Initial reputation bootstrapping unclear: New users have no reputation, so how are early labels weighted?
- 5% expert review seems low if high stakes (food security), but reasonable for research validation

**Comparison to rubric:**
- Score 5: "Multi-layered—gold standard + redundancy + statistical filtering + review"
  - AgriAid has all four ✓
  - But lacks specificity on expert partnerships and bootstrapping
- Score 4: "Thoughtful—2-3 mechanisms with specific thresholds/numbers"
  - AgriAid exceeds this (6 mechanisms)

Calling it **4/5** because nearly perfect, just missing expert commitment details.

**Verdict**: QC design is sophisticated and well-reasoned. Main risk is execution dependency (need experts to create gold standard, need volume for statistical methods to work).

---

## RISK ANALYSIS

### Risk 1: Geospatial Pipeline Complexity Prevents MVP Completion (Likelihood: Very High, Impact: Critical)

**Why critical:**
Satellite data pipeline (GEE API, NDVI computation, image preprocessing, tile generation) is 2-3 weeks of work alone. If not working by Week 3, no time for crowdsourcing phase.

**Warning signs:**
- Team timeline says "Week 1-2: Data collection & UI prototype" (line 280)—drastically underestimates GEE learning curve
- No mention of team's GEE experience
- NDVI computation requires understanding spectral bands, atmospheric correction

**Mitigation:**
1. **Week 0 action**: Validate GEE expertise
   - Does any team member have GEE experience?
   - If no, spend Week 0 (before official start) learning GEE basics
2. **Alternative data source**: Use pre-processed datasets instead of live GEE queries
   - Example: Use xBD Dataset (mentioned line 87) which is already tiled and labeled
   - Trade-off: Not "real-time" but removes 2-week pipeline dependency
3. **Pivot trigger**: If GEE pipeline not working by end of Week 2, switch to pre-processed data

---

### Risk 2: Volunteer Recruitment Failure (Likelihood: Very High, Impact: Critical)

**Why critical:**
Need 4,167 volunteer hours (50,000 annotations at 5 min each). With 100 volunteers, that's 42 hours each—unrealistic for unpaid tasks.

**Warning signs:**
- No test recruitment
- No captive audience (not team's own clubs/classes)
- Reddit r/environment: 3M subscribers but <0.1% typical engagement
- Academic credit "offered" but no partnership confirmed

**Mitigation:**
1. **Week 1 action**: Post 10 sample tasks on r/environment, r/volunteering, Discord servers
   - Measure: Do 100 people complete at least 1 task?
   - Success: 10% completion rate (10 completions) is encouraging
   - Failure: <5% completion rate → recruitment model broken
2. **Pivot option A**: Reduce scope from 10,000 tiles to 1,000 tiles (10x reduction)
   - 1,000 tiles × 5 workers = 5,000 annotations = 417 volunteer hours
   - More achievable with 50 volunteers (8 hours each)
3. **Pivot option B**: Add payment (MTurk at $0.10/annotation)
   - 5,000 annotations × $0.10 = $500 (course budget limit)
   - Trade-off: Extrinsic motivation may yield lower quality

---

### Risk 3: Expertise Contradiction Yields Low-Quality Labels (Likelihood: High, Impact: High)

**Why critical:**
Problem statement (line 15-16): "Automated satellite-monitoring systems often miss early signs of crop stress, especially in smallholder regions."
Worker skills (line 63): "Basic visual recognition; ability to compare two images and detect subtle color/texture changes."

**Contradiction**: If automated systems with NDVI/ML can't detect subtle stress, how will untrained volunteers (basic visual recognition) detect it?

**Likely reality**: Volunteers will disagree frequently (low inter-rater agreement), requiring even more redundancy (7-10 workers instead of 5), exacerbating recruitment challenge.

**Warning signs:**
- "Subtle" color/texture changes require training (not "basic" recognition)
- Task asks for cause attribution (drought vs. flood vs. pests)—requires domain knowledge
- No mention of training module specifics

**Mitigation:**
1. **Simplify task drastically**: Binary classification only (healthy vs. stressed)
   - Remove cause attribution (too expert-level)
   - Remove "bare" category (ambiguous)
   - Accept that volunteers can't outperform NDVI—just provide different signal (human perception)
2. **Add robust training**: 5-10 example pairs with explanations before real tasks
   - Example: "This field is healthy (green, uniform). This field is stressed (brown patches, uneven)."
3. **Embrace low accuracy**: Target 60% agreement instead of 70% (more realistic for subjective judgments)

---

## DECISION GUIDANCE

### Verdict: **STOP AND PIVOT** (Score: 15/30)

Per rubric guidance for 15-19 range: "Project has multiple serious issues. Needs significant rethinking."

On the border with 10-14 range ("Stop and Pivot") due to satellite pipeline complexity. Calling it 15 because with pivot, could be viable.

**Critical changes required:**

### 1. Replace Live Satellite Pipeline with Pre-Processed Dataset (Non-Negotiable)

**Why:**
GEE pipeline is 2-3 weeks of work for experienced user, 4-5 weeks for beginner. Cannot build in 5-week course.

**How:**
1. **Use existing labeled dataset**: xBD Dataset (line 87) for disaster damage detection
   - Already tiled, already has some labels
   - Can focus on vegetation/agriculture subset
2. **Or use static Sentinel-2 tiles**: Download 1,000 pre-selected tiles from STAC repository
   - Skip GEE API complexity
   - Focus on labeling interface + aggregation

**Sacrifice:**
- Not "real-time" monitoring (uses historical data)
- Not "custom" regions (uses pre-selected areas)
- Acceptable for proof-of-concept

**Result**: Removes 2-3 weeks from timeline, makes project feasible.

---

### 2. Slash Labeling Goal by 90%: 10,000 → 1,000 Tiles (Non-Negotiable)

**Why:**
10,000 tiles × 5 workers = 50,000 annotations = 4,167 hours. Impossible without massive recruitment.

**How:**
1. Target 1,000 tiles × 5 workers = 5,000 annotations = 417 volunteer hours
2. With 50 volunteers (realistic with class + club partnerships) = 8 hours each (achievable)

**Success criteria adjustment:**
- Old: "≥500 unique contributors and >10,000 tiles labeled" (line 163)
- New: "≥50 unique contributors and >1,000 tiles labeled"

**Sacrifice:**
- Smaller dataset (but still valuable for research)
- Acceptable for course project

---

### 3. Validate Recruitment Week 1 Before Building Tech (Week 1 Priority)

**Why:**
If recruitment fails, entire project collapses. Validate demand before supply.

**How:**
1. **Week 1, Day 1**: Post 10 sample image pairs on:
   - r/environment (sort by new, not hot—hot requires upvotes)
   - r/volunteering
   - Discord: Climate Action Tracker, Earth Guardians
   - Penn: Eco-Reps email list, Geography department
2. **Measure**: Do 50 people complete at least 1 label in 7 days?
3. **Pivot trigger**: If <20 completions (40% of goal), recruitment broken
4. **Alternative**: Secure professor partnership for academic credit (make commitment, not "offering")

---

### 4. Simplify Task to Binary Classification (Feasibility Fix)

**Why:**
Multi-class (healthy, stressed, bare) + cause attribution (drought, flood, pests) requires expertise. Contradicts "basic visual recognition" claim.

**How:**
- **Old task**: "Classify as healthy/stressed/bare + select cause + rate confidence"
- **New task**: "Does this image pair show vegetation decline? Yes/No"
- **Rationale**: Binary is faster (2 min vs. 5 min), requires less training, higher agreement

**Sacrifice:**
- Less rich data (no cause attribution)
- But higher completion rate, better quality

---

### Predicted Outcomes

**If no changes made (current plan):**
- **Week 1-2**: Team struggles with GEE API, NDVI computation
- **Week 3**: Basic tile display working, no aggregation yet
- **Week 4**: Panic recruitment on Reddit (10 volunteers respond, complete 5 tiles each = 50 tiles)
- **Week 5**: Team labels remaining tiles themselves (3 people × 8 hours × 12 tiles/hour = 288 tiles)
- **Demo**: 338 total tiles labeled (3% of goal), impressive GEE pipeline but no crowdsourcing
- **Grade**: B+ for technical effort, C for crowdsourcing, B overall
- **Feedback**: "Underestimated recruitment and overestimated time available"

**If critical changes made (pre-processed data, 1,000 tiles, Week 1 validation):**
- **Week 1**: Post sample tasks, get 50 completions (validation), secure professor partnership for credit
- **Week 2**: Build labeling interface (Streamlit form with image pairs)
- **Week 3**: Launch with 50 committed volunteers (class + clubs), onboard with training
- **Week 4**: 50 volunteers × 8 hours × 1.5 labels/hour = 600 annotations (12% of goal)
- **Week 5**: Push for final sprint, reach 1,200 annotations (24% of 5,000 target)
- **Demo**: Partial dataset (1,200 annotations on 240 tiles), working aggregation, real volunteers
- **Grade**: A- for realistic scoping + validation
- **Feedback**: "Excellent pivot to match constraints. Proved crowdsourcing model."

**If partial changes made (keep 10,000 tiles, use pre-processed data, no Week 1 validation):**
- **Week 1-2**: Build interface with pre-processed tiles
- **Week 3**: Launch, recruit from Reddit (weak response: 20 volunteers)
- **Week 4**: 20 volunteers complete ~5 tiles each = 100 tiles (1% of goal)
- **Week 5**: Team + friends scramble to add labels (reach 500 annotations)
- **Demo**: 500 annotations on 100 tiles (5% of goal), system works but underutilized
- **Grade**: B for execution, feedback on weak recruitment

---

## COMPARISON TO V1 ANALYSIS

### What V1 Got Right:
- Identified "fundamental expertise mismatch" (untrained volunteers spotting what automation misses)
- Called out "volunteer recruitment fantasy" (no specific plan)
- Noted "catastrophic scope underestimation" for GEE API and geospatial processing
- Calculated scale challenge: 10,000 tiles × 5 workers = 1,667 hours (V1 said 1,667 hours of work)
- Predicted outcome: team builds pipeline, labels themselves, thin crowdsourcing

### What V2 Adds:

**Structured rubric scoring:**
- V1 gave subjective grades ("C+ crowdsourcing, C technical")
- V2 provides dimension-by-dimension 1-5 scores with rationale

**Quantified recruitment math:**
- V1 said scale requirements disconnect
- V2 calculates: 50,000 annotations = 4,167 volunteer hours, 100 volunteers = 42 hours each (unrealistic)

**Alternative pivot options:**
- V1 suggested "local expert networks" or "AI flags suspicious regions"
- V2 provides concrete pivot: use pre-processed dataset (xBD) + reduce to 1,000 tiles

**Week-by-week mitigation plan:**
- V1 said "validate recruitment FIRST"
- V2 specifies: Post 10 sample tasks Day 1, measure 50 completions in 7 days, pivot if <20

**Three outcome scenarios:**
- V1 gave single prediction (team labels, grade B)
- V2 shows no-change, full-pivot, partial-pivot with estimated grades for each

### Key Agreement:
Both analyses identify **satellite pipeline complexity** and **recruitment viability** as dual fatal flaws. Both recommend drastically reducing scope.

### Where V2 Differs:
- **More optimistic on QC**: V1 noted good QC but didn't give score; V2 gives 4/5 (near-perfect design)
- **More specific on pivot**: V2 names exact dataset (xBD) and tile count (1,000) for pivot
- **Timeline discrepancy caught**: V2 notes their "Week 1-8" timeline vs. 5-week course

---

## CONCLUSION

AgriAid addresses a critical global challenge (agricultural crisis detection) with strong social impact potential and sophisticated quality control design. The team demonstrates understanding of statistical aggregation and citizen science principles. However, the project suffers from severe feasibility challenges: satellite data pipeline complexity (2-3 weeks alone), massive volunteer hour requirements (4,167 hours for 10,000 tiles), and fundamental expertise contradictions (untrained volunteers detecting what AI misses).

**The core insight has value**: Human perception can complement automated NDVI systems. **The execution plan is not viable**: It's a 10-15 week project compressed into 5 weeks.

**Recommended path forward:**
1. Replace live GEE pipeline with pre-processed dataset (xBD or static tiles)
2. Reduce from 10,000 to 1,000 tiles (90% scope cut)
3. Validate recruitment Week 1 with test posts (50 completions = proceed, <20 = pivot)
4. Simplify task to binary classification (vegetation decline: yes/no)

With these changes, AgriAid could become an **A-level project** demonstrating validated citizen science model with realistic scope. Without them, it will likely become a **B-level demo** of impressive geospatial infrastructure with token crowdsourcing.

**Final Score: 15/30 - Needs Major Revision**

*Note: With pivots above, could reach 20-22/30 (Weak GO with managed risks).*
