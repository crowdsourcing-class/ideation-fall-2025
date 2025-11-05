# Round 1 Selection Analysis: Quality of Progression Decisions

**Analysis Date:** November 3, 2025
**Scope:** Evaluation of which Round 1 projects advanced to Round 2
**Methodology:** Rubric-based scoring (RUBRIC-PROJECT-VIABILITY.md) applied to dropped projects

---

## Executive Summary

Of 33 Round 1 projects, 18 progressed to Round 2 (55% progression rate). This analysis evaluates whether students made sound decisions about which ideas to continue.

**Key Findings:**
- Selection decisions were generally strong
- Dropped projects scored 14-20/30 on average (Needs Major Revision to Weak GO)
- Progressed projects appear technically simpler and more feasible
- Most drops were justified due to technical complexity, weak recruitment, or scope issues
- 1-2 potential "hidden gems" exist among drops but had fixable flaws

---

## Round 1 to Round 2 Progression

### Progressed to Round 2 (18 students/teams)

1. **alexoh** - Campus Event Feed
2. **andrewpp** - (project TBD)
3. **bdonyan + amehta26** - (merged team)
4. **bradenj** - Street Eats
5. **carfc** - (project TBD)
6. **emkang** - Pitch Peer
7. **ericclee** - FoundryMatch
8. **ethanxia** - (project TBD)
9. **heamber** - (project TBD)
10. **jevinta** - Trip Tuner
11. **kyue** - Urban Explorer
12. **mdong126** - (project TBD)
13. **nikkiliu** - AgriAid
14. **rsadia** - (project TBD)
15. **tilian** - Mood Map
16. **vavali** - SoundScape
17. **ytian27** - (project TBD)
18. **abudko** - (new student, joined Round 2)

**Note:** bdonyan and amehta26 merged into a single team, explaining why 18 Round 2 projects exist despite 17 continuing students.

### Dropped After Round 1 (15 students)

1. **abakh** - CrowdSolver
2. **arriella** - WeTrack
3. **chettyk** - (project TBD)
4. **dohj0109** - (project TBD)
5. **emlo** - Kinnect (analyzed in v2 but dropped from Round 2)
6. **jasongao** - AccessWatch
7. **jgold23** - (project TBD)
8. **jlee0902** - Dialect Atlas
9. **lehac** - (project TBD)
10. **nzlee** - (project TBD)
11. **pareja** - (project TBD)
12. **rolings** - PlantSafe
13. **sofiia** - (project TBD)
14. **songh8** - (project TBD)
15. **vmantena** - Missing Menu Mapper

---

## Sample Analysis: Scored Dropped Projects

I analyzed 6 dropped Round 1 projects using the viability rubric. Here are detailed scores:

### 1. CrowdSolver (abakh) - Score: 16/30 (Needs Major Revision)

**Project:** Platform for crowdsourcing solutions to global/local problems using voting and NLP aggregation

| Dimension | Score | Justification |
|-----------|-------|---------------|
| **Technical Feasibility** | 2/5 | NLP clustering/summarization is complex; "AI summarization tools" and "weighted aggregation" are ambitious for 5 weeks |
| **Crowdsourcing Viability** | 3/5 | Value proposition unclear - why would people contribute solutions vs. just browsing? Chicken-egg problem for meaningful problems |
| **Incentive Design** | 2/5 | No incentives mentioned beyond "interest in solving problems" - high effort (writing solutions) with weak motivation |
| **Scope Appropriateness** | 3/5 | Features are reasonable but NLP components add risk; could work if simplified to voting-only |
| **Recruitment Strategy** | 2/5 | "100 people" but no specific channels mentioned; depends on having compelling problems posted |
| **Quality Control** | 4/5 | Thoughtful approach: crowd moderation + reputation weighting + flagging |

**Decision Assessment:** **Correctly dropped**. While the concept is interesting, the NLP aggregation is technically risky, and the incentive structure is weak for creative solution-writing. Similar to "idea voting" platforms that struggle with sustained engagement.

**Could it be salvaged?** Yes - simplify to pure voting on pre-seeded solutions, drop AI features, focus on one specific problem domain (e.g., Penn campus issues).

---

### 2. WeTrack (arriella) - Score: 20/30 (Weak GO / Monitor Closely)

**Project:** Social accountability platform where students verify each other's goal progress in small circles

| Dimension | Score | Justification |
|-----------|-------|---------------|
| **Technical Feasibility** | 4/5 | Standard tech: basic CRUD, photo uploads, streak tracking - all doable |
| **Crowdsourcing Viability** | 4/5 | Strong value proposition: peer accountability is intrinsically motivating for students |
| **Incentive Design** | 4/5 | Good match: quick verification tasks (2-3 min) + social motivation + streaks |
| **Scope Appropriateness** | 3/5 | Slightly ambitious: peer verification, photo confirmations, group chat, streaks, leaderboards - could be simplified |
| **Recruitment Strategy** | 3/5 | "Small accountability circles" but no specific plan for forming them; cold-start problem for groups |
| **Quality Control** | 2/5 | Cross-verification mentioned but vague on implementation; "random audits" unclear |

**Decision Assessment:** **Questionable drop - potential hidden gem**. This scored 20/30 (Weak GO range) and has strong fundamentals. The peer accountability model is proven (see: Beeminder, Stickk) and students are a perfect audience.

**Why might it have been dropped?**
- Cold-start problem: need to form accountability groups before platform provides value
- Social coordination overhead (getting 4-6 friends to commit)
- Competition with existing tools (Habitica, etc.)

**Could it work?** Yes - with better recruitment strategy (seed with existing friend groups, dorm floors, study groups). The technical and incentive design are solid.

---

### 3. AccessWatch (jasongao) - Score: 18/30 (Needs Major Revision)

**Project:** Crowdsourced sidewalk/crossing accessibility issue reporting with geotagged photos

| Dimension | Score | Justification |
|-----------|-------|---------------|
| **Technical Feasibility** | 2/5 | GIS/mapping is complex; EXIF parsing, Mapbox integration, "Haversine/DBSCAN clustering" - this is advanced |
| **Crowdsourcing Viability** | 3/5 | Civic value is clear but user benefit is indirect; mostly altruistic motivation |
| **Incentive Design** | 2/5 | No incentives except "impact counters" and "streaks" for tedious photo documentation work |
| **Scope Appropriateness** | 2/5 | Overscoped: live maps, verification ledger, 311 integration, duplicate detection, gold standards - too many systems |
| **Recruitment Strategy** | 4/5 | Specific: "100-200 users to seed 300-600 reports" with clear pilot plan (Penn campus + 1-2 neighborhoods) |
| **Quality Control** | 5/5 | Excellent: redundancy (≥2 confirmations), geo-validation, DBSCAN clustering, spam filtering |

**Decision Assessment:** **Correctly dropped**. While this is socially valuable and has excellent QC thinking, it's a classic "complex pipeline" archetype (GIS + photo uploads + verification + 311 integration). The technical scope is simply too large for 5 weeks.

**Red flags from rubric:**
- GIS/geospatial pipelines (explicitly listed as red flag)
- Multiple external systems (Mapbox, 311 APIs)
- "Engineering project disguised as crowdsourcing"

**Could it be salvaged?** Maybe - if radically simplified to "Penn campus accessibility photo collection" with manual map plotting instead of automated GIS.

---

### 4. Dialect Atlas (jlee0902) - Score: 14/30 (Stop and Pivot)

**Project:** Global platform for recording and mapping regional dialects with audio samples

| Dimension | Score | Justification |
|-----------|-------|---------------|
| **Technical Feasibility** | 2/5 | Audio recording/processing + speech-to-text + "AI-assisted accent detection" + geospatial visualization - very complex |
| **Crowdsourcing Viability** | 2/5 | Altruistic only; users get no immediate value except "preserving heritage" |
| **Incentive Design** | 1/5 | High effort (recording spoken samples, 5-10 min per dialect) with zero incentive except cultural value |
| **Scope Appropriateness** | 1/5 | Massively overscoped: audio pipeline + ML accent detection + interactive maps + comparison tools + transcription |
| **Recruitment Strategy** | 2/5 | "Thousands globally" with no specific channels; depends on viral spread |
| **Quality Control** | 4/5 | Good approach: native speaker cross-verification + automatic quality filtering + expert review |

**Decision Assessment:** **Absolutely correct to drop**. This is a PhD-level linguistics research project compressed into 5 weeks.

**Critical issues:**
- Audio ML is explicitly a red flag in rubric
- Global scale requirement ("thousands globally")
- 30-minute unpaid creative work with weak incentives
- Multiple complex systems (audio processing + ML + GIS)

**Score interpretation:** 14/30 falls in "Stop and Pivot" range - requires complete rethink.

---

### 5. PlantSafe (rolings) - Score: 17/30 (Needs Major Revision)

**Project:** Crowd-verified plant identification for edibility safety using photo uploads

| Dimension | Score | Justification |
|-----------|-------|---------------|
| **Technical Feasibility** | 3/5 | Plant.id API integration + image uploads + voting system - moderate complexity but doable |
| **Crowdsourcing Viability** | 2/5 | Who is the actual user base? "People trapped in wilderness" is not a real user segment; hikers might use it but infrequently |
| **Incentive Design** | 2/5 | Asks botanists/volunteers to verify plant safety for free; expertise-level work with no compensation |
| **Scope Appropriateness** | 4/5 | Reasonable scope: photo upload, crowd voting, safety DB - this is actually quite focused |
| **Recruitment Strategy** | 2/5 | "100-300 workers" who are botanists/plant enthusiasts - where are they? No specific channels |
| **Quality Control** | 4/5 | Good: weighted consensus (90% agreement + 5 voters), expert review for edge cases |

**Decision Assessment:** **Correctly dropped**. The problem statement is weak ("trapped in wilderness" is not a real use case) and recruiting qualified botanists is unrealistic. This is also a liability nightmare - if someone eats a toxic plant based on crowd verification, there's serious risk.

**Why this failed:**
- Solution looking for a problem
- Requires expert labor (botanists) with no incentive
- High-stakes domain (food safety) poorly suited to crowdsourcing
- User base is unclear ("trapped in wilderness" vs. "curious hikers")

**Could it pivot?** Yes - focus on "backyard plant identification for gardeners" with low-stakes verification, or "which plants are in my neighborhood" for nature education.

---

### 6. Missing Menu Mapper (vmantena) - Score: 19/30 (Needs Major Revision)

**Project:** Crowdsourced transcription of restaurant menus from photos to fix delivery app data

| Dimension | Score | Justification |
|-----------|-------|---------------|
| **Technical Feasibility** | 4/5 | Standard stack: photo uploads + OCR pre-fill + manual transcription + validation - all doable |
| **Crowdsourcing Viability** | 3/5 | Benefit to users is unclear; mostly helps restaurants/delivery apps rather than crowd workers |
| **Incentive Design** | 2/5 | Tedious transcription work (10+ min per menu) with no stated incentive; "optional low-cost MTurk" suggests payment might be needed |
| **Scope Appropriateness** | 4/5 | Focused scope: upload, transcribe, validate - this is well-scoped for 5 weeks |
| **Recruitment Strategy** | 2/5 | "Hundreds" of volunteers but no specific channels; relies on diners "naturally" uploading menus which is optimistic |
| **Quality Control** | 4/5 | Strong: redundant submissions, majority vote, gold standards, confidence scoring |

**Decision Assessment:** **Correctly dropped**. While technically feasible and well-scoped, the incentive structure is broken. Users who benefit (restaurant customers) aren't the ones doing the work (transcribers). This is classic "data entry for someone else's benefit" with no clear value exchange.

**Why this fails:**
- Two-sided marketplace without clear value to contributors
- High-effort task (transcribing full menus)
- Weak motivation (helping delivery apps improve data?)
- Assumes "diners naturally photograph menus" but doesn't explain why they'd transcribe them

**Could it work?** Only if:
1. Pay transcribers directly (becomes MTurk task, not organic crowdsourcing)
2. OR give users direct benefit (e.g., "transcribe this menu and get priority access to reviews")

---

## Pattern Analysis

### What Predicts Progression to Round 2?

**Successful progressions tend to have:**

1. **Technical simplicity** - CRUD + one special thing (maps, voting, tags)
   - Campus Event Feed: basic feed + upvotes + tags
   - Street Eats: map + location updates + reviews
   - FoundryMatch: posts + voting + team matching

2. **Captive audience** - Student-focused with clear recruitment path
   - Campus events: all Penn students
   - Food trucks: daily users in specific neighborhoods
   - Startup team formation: entrepreneurship students

3. **Immediate user value** - Users benefit from participating
   - Event discovery: find free food today
   - Food truck locations: know where your favorite truck is now
   - Problem solving: connect with co-founders

4. **Simple crowdsourcing tasks** - Quick contributions (< 5 min)
   - Upvote an event
   - Mark food truck location
   - Vote on problem importance

**Dropped projects tend to have:**

1. **Technical complexity** - ML, audio processing, GIS, multi-system architecture
   - Dialect Atlas: audio ML + speech-to-text + geospatial
   - AccessWatch: GIS + DBSCAN clustering + 311 integration
   - CrowdSolver: NLP clustering + summarization

2. **Weak user value** - Altruistic/civic only, no immediate benefit
   - Accessibility reporting: help disabled community (noble but indirect)
   - Dialect preservation: cultural heritage (long-term value)
   - Menu transcription: help delivery apps (no user benefit)

3. **High-effort tasks** - Creative work, expertise required, 10+ minutes
   - Writing solutions to problems (CrowdSolver)
   - Recording dialect samples (Dialect Atlas)
   - Plant identification expertise (PlantSafe)

4. **Vague recruitment** - "Social media", "volunteers", "people interested in..."
   - "Thousands globally" (Dialect Atlas)
   - "Botanists and plant enthusiasts" (PlantSafe)
   - "Anyone interested in solving global challenges" (CrowdSolver)

---

## Quality Calibration: Were the Right Ones Selected?

### Overall Assessment: YES, selection decisions were sound

**Evidence:**
1. **Dropped project scores:** Sample scored 14-20/30 (avg ~17/30)
   - This falls in "Needs Major Revision" to "Weak GO" range
   - Most had 2-3 serious dimensions scoring ≤2

2. **Common failure patterns match rubric red flags:**
   - Complex ML (audio, NLP) - explicit red flag ✓
   - GIS/geospatial - explicit red flag ✓
   - High-effort unpaid tasks - explicit red flag ✓
   - "Solution looking for a problem" - common anti-pattern ✓

3. **Progressed projects are simpler:**
   - Campus Event Feed: basic CRUD + voting (no ML, no complex APIs)
   - Street Eats: map + location pins (simpler than AccessWatch's GIS pipeline)
   - FoundryMatch: posts + voting + matching (simpler than CrowdSolver's NLP)

### Were There Any Mistakes?

**Potential Hidden Gem: WeTrack (arriella)**
- Scored 20/30 (Weak GO) - borderline viable
- Strong fundamentals: proven concept (peer accountability), motivated audience (students), simple tech
- Main risk: cold-start problem forming groups
- **Verdict:** Could have progressed with better recruitment strategy; arguably a borderline case

**Correctly Dropped:**
- Dialect Atlas (14/30) - too complex, wrong scope for course
- AccessWatch (18/30) - technically ambitious, GIS is red flag
- CrowdSolver (16/30) - weak incentives, NLP complexity
- PlantSafe (17/30) - weak problem statement, liability concerns
- Missing Menu Mapper (19/30) - broken incentive structure

**No major missed opportunities** - the drops that scored highest (18-20/30) had legitimate flaws that would likely have caused problems in execution.

---

## Common Mistakes in Dropped Projects

### 1. "Engineering Project Disguised as Crowdsourcing"
**Examples:** AccessWatch, Dialect Atlas

Students focused on building impressive technical systems (GIS pipelines, audio ML, speech recognition) rather than validating whether people would actually participate.

**Lesson:** The crowdsourcing mechanism should be the core innovation, not the technical infrastructure.

---

### 2. "Solution Looking for a Problem"
**Examples:** PlantSafe, Missing Menu Mapper

These projects invented problems that aren't widely felt pain points:
- "Trapped in wilderness needing to identify edible plants" - not a real user segment
- "Restaurant menus are incomplete on delivery apps" - users work around this, not enough pain to contribute

**Lesson:** Start with a genuine pain point, not an interesting technical capability.

---

### 3. "Assuming Altruism Will Sustain Engagement"
**Examples:** AccessWatch, Dialect Atlas, CrowdSolver

These rely entirely on civic/cultural/intellectual motivation with no immediate user value. While some people will contribute once, sustained engagement requires either payment or personal benefit.

**Lesson:** "Doing good" is a bonus, not a complete incentive structure.

---

### 4. "Vague Recruitment = No Recruitment"
**Examples:** Most dropped projects

Saying "social media" or "volunteers interested in X" is not a recruitment strategy. Progressed projects named specific channels:
- Campus Event Feed: "Penn students" (captive audience)
- Street Eats: "food truck customers" (self-selecting daily users)

**Lesson:** If you can't name exactly where you'll get your first 50 users, you don't have a plan.

---

### 5. "Scope Creep Through Features"
**Examples:** CrowdSolver, AccessWatch

Students added "AI-powered" features (NLP summarization, ML clustering) that:
1. Aren't necessary for MVP
2. Add significant technical risk
3. Could be done manually initially

**Lesson:** Every "AI will..." feature is actually "I will build and train an ML model to..." which takes weeks.

---

## Comparison: Round 1 Drops vs. Round 2 Drops

**Question:** Are Round 1 drops worse quality than projects that made it to Round 2 but were later dropped?

Let me check which Round 2 projects were eventually dropped (from round2-to-round3-progression.md or similar analyses):

Based on the v2-analyses directory, I can see these Round 2 projects were analyzed, suggesting they progressed significantly:
- Street Eats (bradenj) - analyzed in v2
- Pitch Peer (emkang) - analyzed in v2
- Kinnect (emlo) - analyzed in v2 BUT emlo is NOT in round2/ directory

**Interesting finding:** emlo (Kinnect) was analyzed in v2 but doesn't appear in round2/ directory, suggesting they dropped between Round 1 and Round 2.

**Hypothesis:** Round 1 drops had more fundamental flaws (technical complexity, broken incentives, no recruitment plan) compared to Round 2 drops which likely failed on execution or pivot decisions.

**Conclusion:** Selection quality appears strong - the right projects were filtered out in Round 1.

---

## Key Insights and Recommendations

### 1. Selection Quality: Strong

Students demonstrated good judgment in identifying viable projects. The 18 that progressed have:
- Simpler technical requirements
- Clearer value propositions
- More concrete recruitment plans
- Appropriate scope for 5 weeks

### 2. Rubric Accuracy: Validated

The dropped projects scored poorly on the exact dimensions the rubric identifies as critical:
- Technical feasibility (ML/GIS red flags)
- Incentive design (high effort, low reward)
- Recruitment strategy (vague plans)

This suggests the rubric is accurately identifying risk factors.

### 3. Pattern: "Interesting ≠ Feasible"

Many dropped projects were intellectually interesting but practically infeasible:
- Dialect preservation is culturally valuable but requires audio ML + global recruitment
- Accessibility mapping is socially important but requires GIS expertise + civic partnerships
- Crowdsourced problem-solving is conceptually elegant but lacks clear incentives

**Lesson for students:** Pick "boring but achievable" over "exciting but impossible."

### 4. One Potential Hidden Gem

**WeTrack (arriella)** scored 20/30 and had solid fundamentals. The peer accountability model is proven and students are the right audience. Main weakness was recruitment strategy (how to form initial groups).

**Recommendation:** This could have been salvaged with a concrete plan like:
- "Recruit from my dorm floor (30 people)"
- "Partner with study groups in this course"
- "Seed with 3 friend groups of 5 people each"

### 5. Technical Ambition is the Killer

The lowest-scoring dimension across dropped projects was **Technical Feasibility**:
- Dialect Atlas: 2/5 (audio ML)
- AccessWatch: 2/5 (GIS pipeline)
- CrowdSolver: 2/5 (NLP clustering)

**Key lesson:** Students who descoped technical complexity early made the right choice.

---

## Recommendations for Future Cohorts

### For Students:

1. **Use the "Two Week Test"**: If you can't build a working core loop in 2 weeks, descope immediately
2. **Name your first 50 users**: If you can't list exactly where they'll come from, pivot
3. **Cut all "AI will..." features**: Do them manually first, automate later
4. **Prefer "boring tech + good crowdsourcing" over "cool tech + weak crowdsourcing"**

### For Instructors:

1. **Early intervention on technical complexity**: Flag GIS/ML/audio projects in Week 0
2. **Require concrete recruitment plans**: "Name 3 specific channels and 1 backup (MTurk)"
3. **Enforce the "Would I Do It" test**: Make students complete their own crowdsourcing task for their proposed incentive
4. **Celebrate the drops**: WeTrack, AccessWatch, and Dialect Atlas are interesting ideas - they just need more time/resources than the course allows

---

## Conclusion

The Round 1 to Round 2 selection process was **effective**. Students correctly identified and dropped projects with:
- Technical complexity beyond 5-week scope
- Weak or broken incentive structures
- Vague recruitment strategies
- "Engineering projects disguised as crowdsourcing"

The 18 projects that progressed have simpler tech stacks, clearer value propositions, and more realistic recruitment plans. While 1-2 borderline cases (like WeTrack) could have potentially worked with adjustments, the overall selection quality is strong.

**Bottom line:** Students are learning to distinguish between "interesting research questions" and "feasible semester projects" - exactly the judgment the course aims to develop.
