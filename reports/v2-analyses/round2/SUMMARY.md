# Round 2 Dropped Projects - V2 Analysis Summary

## Overview
This analysis evaluates 5 projects that were dropped after Round 2 using the NETS 2130 Project Viability Rubric. Each project was scored on 6 dimensions (out of 5 points each, total /30) and assessed for whether dropping them was the correct decision.

---

## Summary Table

| Project | Authors | Score | Verdict | Right to Drop? | Hidden Gem? |
|---------|---------|-------|---------|----------------|-------------|
| **Auralynx** | abudko et al. | 17/30 | NEEDS MAJOR REVISION | ✅ YES | 🟡 MODERATE |
| **PennPulse** | alexoh, shivij | 17/30 | NEEDS MAJOR REVISION | ✅ YES | 🔴 LOW |
| **TrashTag Tracker** | andrewpp, Eric Lee | 19/30 | NEEDS MAJOR REVISION | 🟡 MAYBE | 🟢 MODERATE-HIGH |
| **TerraTruth** | bdonyan, amehta26 | 14/30 | STOP AND PIVOT | ✅ ABSOLUTELY YES | 🔴 LOW |
| **Kinnect** | emlo, carfc | 13/30 | STOP AND PIVOT | ✅ ABSOLUTELY YES | 🔴 VERY LOW |

---

## Detailed Score Breakdown

### Auralynx (Audio Perception Platform)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | Audio ML pipeline, multiple models, complex stack |
| Crowdsourcing Viability | 3/5 | Two-sided marketplace (speakers + guessers) |
| Incentive Design | 3/5 | Gamification + small budget, but weak for speakers |
| Scope Appropriateness | 2/5 | 8 features including bias engine, research platform |
| Recruitment Strategy | 3/5 | General plan, massive scale needed (1,500+ people) |
| Quality Control | 4/5 | Gold standards, weighted voting, well-designed |
| **TOTAL** | **17/30** | **NEEDS MAJOR REVISION** |

**Why Dropped:** Audio ML too complex, overscoped for 5 weeks, research platform not class project.

**Hidden Gem Potential (MODERATE):** Core insight about perception gaps is novel. Could work if: (1) Pivoted to text/photos instead of audio, (2) Pre-ran AI predictions on fixed dataset, (3) Reduced scale 10x, (4) Team pre-recorded all clips to eliminate two-sided problem.

---

### PennPulse (Campus Event Feed)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 4/5 | Standard CRUD + voting, Reddit-style ranking |
| Crowdsourcing Viability | 2/5 | Chicken-egg problem, competes with existing channels |
| Incentive Design | 2/5 | "Self-sustaining" assumption unvalidated |
| Scope Appropriateness | 4/5 | 5 features, reasonable if users existed |
| Recruitment Strategy | 2/5 | Depends on unconfirmed org partnerships |
| Quality Control | 3/5 | Penn email, voting, flagging - basic mechanisms |
| **TOTAL** | **17/30** | **NEEDS MAJOR REVISION** |

**Why Dropped:** Two-sided marketplace with no adoption path, competes with entrenched platforms (GroupMe, Penn Clubs), weak value proposition.

**Hidden Gem Potential (LOW):** Campus event aggregation has been tried many times and typically fails due to network effects. Even with perfect execution, faces uphill battle against existing solutions. Better approach: Integration/aggregation tool rather than new platform.

---

### TrashTag Tracker (Litter Mapping)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 3/5 | Photo + GPS, mapping, duplicate detection via CV |
| Crowdsourcing Viability | 3/5 | Environmental appeal, but requires active participation |
| Incentive Design | 3/5 | Intrinsic + gamification, no immediate personal benefit |
| Scope Appropriateness | 4/5 | 5 features, core loop manageable in 2 weeks |
| Recruitment Strategy | 2/5 | Vague "social media, environmental clubs" |
| Quality Control | 4/5 | Redundant validation, reputation, outlier detection |
| **TOTAL** | **19/30** | **NEEDS MAJOR REVISION (borderline)** |

**Why Dropped:** Uncertain user motivation (relies on altruism), weak recruitment plan, verification bottleneck acknowledged but unsolved. Likely better projects scored 20+.

**Hidden Gem Potential (MODERATE-HIGH):** Best-structured of dropped projects. Could have succeeded with: (1) Hyper-local launch (Penn campus only + official Facilities backing), (2) Competitive framing (dorm vs dorm), (3) Simplified verification (no crowd verification needed), (4) Concrete recruitment (pre-secure commitments from 3-5 clubs), (5) Proof-of-concept testing Week 1 before building.

**Verdict:** Borderline call. With entrepreneurial hustle and validation, could have reached Weak GO territory.

---

### TerraTruth (Satellite Analysis for NGOs)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | GIS/satellite processing, PostGIS, complex pipeline |
| Crowdsourcing Viability | 2/5 | Requires NGO partnerships that don't exist |
| Incentive Design | 3/5 | Intrinsic + gamification + impact, altruism-only |
| Scope Appropriateness | 1/5 | 7 features, building "permanent platform" |
| Recruitment Strategy | 1/5 | Depends on non-existent partners and volunteers |
| Quality Control | 5/5 | Multi-layered, excellent QC design |
| **TOTAL** | **14/30** | **STOP AND PIVOT** |

**Why Dropped:** GIS complexity (rubric red flag), partnership-dependent, massive overscoping (startup not class project), no path to first user, competes with existing platforms (Zooniverse, Amnesty Decoders).

**Hidden Gem Potential (LOW):** Not a hidden gem - it's a miscategorization. This is a valid graduate thesis or startup idea, not a 5-week class project. Thoughtfully designed but fundamentally impossible timeline. Team described "first year" metrics and "permanent platform" - clear mismatch. Even Amnesty International discontinued their Decoders program, so market need is questionable.

**Irony:** Best QC design of any dropped project (5/5), but can't save structurally impossible scope.

---

### Kinnect (Global Fitness Challenge)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | Mobile app + fitness APIs + real-time maps |
| Crowdsourcing Viability | 2/5 | Network effects required, competes with Strava/Nike |
| Incentive Design | 2/5 | Rewards undefined, FOMO only works at scale |
| Scope Appropriateness | 2/5 | 7 features, full fitness app in 5 weeks |
| Recruitment Strategy | 2/5 | "Social media, friends" - vague |
| Quality Control | 3/5 | Device sync, outlier detection, reputation |
| **TOTAL** | **13/30** | **STOP AND PIVOT** |

**Why Dropped:** Mobile development (rubric: adds 3-4 weeks), multiple APIs, real-time features, rewards system undefined, competes in saturated market with zero differentiation. Hits nearly EVERY red flag in rubric simultaneously.

**Hidden Gem Potential (VERY LOW):** Crowded fitness app market with entrenched competitors (Strava, Nike Run Club, Apple Fitness). No unique value proposition. Technical complexity eliminates iteration time. Students already have free, good-enough options. Not a hidden gem - this is a consumer app idea that ignores market reality and timeline constraints.

---

## Analysis Insights

### Common Failure Patterns

1. **Technical Overambition (4/5 projects)**
   - Mobile apps: Kinnect (React Native)
   - Complex ML: Auralynx (audio models)
   - Specialty tech: TerraTruth (GIS/PostGIS)
   - All scored 2/5 or lower on Technical Feasibility

2. **Partnership Dependency (3/5 projects)**
   - PennPulse: Depends on student org partnerships
   - TerraTruth: Requires NGO partnerships
   - All scored 1-2/5 on Recruitment

3. **Two-Sided Marketplace (3/5 projects)**
   - Auralynx: Need speakers AND guessers
   - PennPulse: Need event posters AND attendees
   - Kinnect: Need active users AND reward partners

4. **Weak/Unvalidated Incentives (5/5 projects)**
   - All relied on assumptions (altruism, FOMO, "self-sustaining")
   - None tested incentives before proposing
   - Average Incentive score: 2.6/5

5. **Vague Recruitment (5/5 projects)**
   - All mentioned "social media" or "student groups" generically
   - None named specific channels or secured commitments
   - None tested recruitment Week 1
   - Average Recruitment score: 2.0/5 (worst dimension overall)

### Score Distribution
- **13-14 (Stop and Pivot):** 2 projects (TerraTruth, Kinnect)
- **17 (Needs Major Revision):** 2 projects (Auralynx, PennPulse)
- **19 (Needs Major Revision, borderline):** 1 project (TrashTag Tracker)

### Hidden Gem Rankings
1. **TrashTag Tracker** - MODERATE-HIGH: Well-structured, needed validation + hustle
2. **Auralynx** - MODERATE: Novel insight, could pivot modality
3. **PennPulse** - LOW: Crowded space, network effects moat
4. **TerraTruth** - LOW: Wrong project type (startup not class)
5. **Kinnect** - VERY LOW: Saturated market, no differentiation

---

## Were These the Right Decisions?

### Definitely Correct Drops (3/5)
1. **TerraTruth** - Score 14/30, GIS complexity, partnership-dependent, startup not class project
2. **Kinnect** - Score 13/30, mobile + APIs + real-time, hits all red flags, saturated market
3. **PennPulse** - Score 17/30, two-sided marketplace with no adoption path, competes with entrenched platforms

### Borderline/Debatable (1/5)
4. **TrashTag Tracker** - Score 19/30, could have reached Weak GO (20-24) with better recruitment/validation

### Could Have Been Revised (1/5)
5. **Auralynx** - Score 17/30, if willing to pivot away from audio ML to simpler modality, had potential

---

## Key Takeaways

### What Killed These Projects
1. **Technical ambition beyond timeline** (mobile, ML, GIS)
2. **No validation of core assumptions** (incentives, recruitment)
3. **Partnership/network effect dependencies**
4. **Treating class project as startup pitch**
5. **"Build it and they will come" thinking**

### What Could Have Saved Them
1. **Week 1 validation** - Test recruitment and incentives BEFORE building
2. **Extreme descoping** - Cut 50-70% of features
3. **Secure commitments** - Get partnerships/users FIRST
4. **Build for proof, not production** - MVP to test concept
5. **Match timeline to constraints** - 5 weeks is very short

### Lessons for Future Projects
- **Recruitment is hardest:** Lowest average score (2.0/5) across all projects
- **Tech feasibility is binary:** Mobile/ML/GIS usually means automatic failure
- **Validation beats vision:** Better to test ugly prototype than plan beautiful impossibility
- **Incentives need evidence:** "Self-sustaining" and "intrinsic motivation" are assumptions, not strategies
- **Scope discipline is rare:** Even dropped projects averaged 6-7 features (should be 3-4 max)

---

## Comparison to Round 3 Projects

The Round 3 projects that were selected to continue likely scored 20+/30 (Weak GO or better). These dropped projects averaged **16/30**, clearly below the threshold. The decisions to drop them appear well-calibrated to the rubric.

**Notably:** Even the highest-scoring dropped project (TrashTag at 19/30) was borderline, and the rubric states 15-19 requires "major revision." The selection process appears to have correctly identified projects with multiple structural problems rather than just execution risks.

---

# Additional Round 2 Dropped Projects - Extended Analysis

## Additional Projects Analyzed

| Project | Authors | Score | Verdict | Right to Drop? | Hidden Gem? |
|---------|---------|-------|---------|----------------|-------------|
| **FoundryMatch** | ericclee, mvalek | 11/30 | STOP AND PIVOT | ✅ ABSOLUTELY YES | 🔴 LOW (needs 90% redesign) |
| **CrowdScout** | ethanxia, connorcc | 14/30 | STOP AND PIVOT | ✅ YES | 🟢 HIGH |
| **PriceScope** | heamber | 16/30 | NEEDS MAJOR REVISION | ✅ YES/MAYBE | 🟡 MEDIUM |
| **Soundscape** | mdong126, basua | 15/30 | NEEDS MAJOR REVISION | ✅ YES | 🟢 HIGH |
| **GatherAI** | ytian27, songh8 | 18/30 | NEEDS MAJOR REVISION | ✅ YES | 🟢 HIGH (highest) |

---

## Detailed Score Breakdowns

### FoundryMatch (Startup Team Formation Platform)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | Social network + matchmaking + collaboration + market intelligence |
| Crowdsourcing Viability | 2/5 | Two-sided marketplace: problems + entrepreneurs + technical + designers |
| Incentive Design | 2/5 | High-effort creative work (30+ min) for "relatability" |
| Scope Appropriateness | 1/5 | 8 complex features including AI matching, real-time chat, market data APIs |
| Recruitment Strategy | 1/5 | "Online users" - completely vague, no specific channels |
| Quality Control | 3/5 | Weighted voting, AI moderation, expert review |
| **TOTAL** | **11/30** | **NOT FEASIBLE** |

**Why Dropped:** Building 4-5 interconnected platforms (social network + matchmaking + collaboration tool + market research). Two-sided marketplace requiring simultaneous critical mass of multiple user types. No competitive advantage over Reddit/IndieHackers/YC matching. Real-time collaboration + AI matching + market data APIs = months of startup work. Zero concrete recruitment plan.

**Hidden Gem Potential (LOW):** Would require 90% redesign to work. Could pivot to simple "Penn Startup Problem Board" - just voting, no matching, single entrepreneurship club as captive audience, manual team formation. But at that point, it's a different project.

---

### CrowdScout (TikTok-Style Sports Recruiting)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | Video hosting + CDN + ML recommendation algorithm + PyTorch + Spark |
| Crowdsourcing Viability | 2/5 | Two-sided: athletes uploading + scouts browsing, competes with Hudl |
| Incentive Design | 3/5 | Athletes get exposure (strong), casual users get gamification (weak) |
| Scope Appropriateness | 1/5 | Video platform + TikTok algorithm + weighted aggregation + API integration |
| Recruitment Strategy | 2/5 | "Social media, schools" - generic, "at least 10 athletes" (absurdly low) |
| Quality Control | 4/5 | Weighted credibility, reputation system, suspicious pattern detection |
| **TOTAL** | **14/30** | **STOP AND PIVOT** |

**Why Dropped:** Video platform infrastructure alone = major complexity and cost. "TikTok-style recommendation algorithm" = years of ML research worth billions. Video storage/CDN/encoding costs would blow through budget by 10x. Competing directly with Hudl, an established platform recruiters already use. Team fundamentally underestimated technical complexity by orders of magnitude.

**Hidden Gem Potential (HIGH):** Excellent core concept (democratizing sports recruiting) with fatal execution. Could work with 90% descope:
- YouTube/Instagram LINKS instead of hosted video (eliminate infrastructure)
- Simple voting instead of ML recommendations
- Penn IM sports only (not all recruiting)
- Partner with Penn Athletics for built-in audience
- Focus on discovery, not algorithmic ranking

With these pivots, could score 20-22/30 and succeed as B+/A- project.

---

### PriceScope (Crowdsourced Grocery Prices)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 3/5 | CRUD + OCR + GPS + product normalization - moderate complexity |
| Crowdsourcing Viability | 2/5 | Task: 5 min to photograph/submit, Value: unclear until scale |
| Incentive Design | 2/5 | 5 min task for $0.25 expected value (raffle math) |
| Scope Appropriateness | 4/5 | 5 features, core loop achievable in 2-3 weeks |
| Recruitment Strategy | 2/5 | "Local shoppers" - vague, "100-200 weekly" with no path |
| Quality Control | 3/5 | OCR, geofencing, timestamp, outlier detection |
| **TOTAL** | **16/30** | **NEEDS MAJOR REVISION** |

**Why Dropped:** Weak incentive structure (high effort for minimal value). Severe cold-start problem (early users get nothing, no price data exists). Competing with automated solutions (store apps, credit cards, Flipp). Behavior change is hard (remembering to photograph receipts every trip). No captive audience identified.

**Hidden Gem Potential (MEDIUM):** Technical scope is appropriate (unlike most dropped projects). Problem is real. Could work with significant pivots:
- Penn off-campus students as specific target
- Weekly "best deal challenge" instead of comprehensive tracking
- Quick 30-second deal submissions instead of full receipts
- Focus on 10-15 staples, not all groceries
- Gamified team competitions by dorm/building
- Make it social and fun, not just utilitarian

---

### Soundscape (Crowdsourced Audio Environment Map)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | Web + mobile + audio processing + ML clustering + map integration |
| Crowdsourcing Viability | 3/5 | Creative/exploratory appeal but unclear utility value |
| Incentive Design | 3/5 | Quick task (30 sec) + gamification + map visibility |
| Scope Appropriateness | 1/5 | 8 major features including mobile app, ML similarity, API access |
| Recruitment Strategy | 2/5 | "Philly area volunteers" - vague, needs 300-1000 users |
| Quality Control | 4/5 | Excellent audio validation, SNR checks, duplicate detection |
| **TOTAL** | **15/30** | **NEEDS MAJOR REVISION / STOP** |

**Why Dropped:** Massive technical overscope - building web + mobile + audio processing pipeline + ML clustering + gamification + analytics. Mobile requirement (for accurate geolocation) adds 3-4 weeks alone. Audio processing (normalization, feature extraction, perceptual hashing) = complex. ML-based similarity clustering = advanced. Needs 300-1000 users with no concrete recruitment plan. Unclear market demand - cool concept ≠ validated need.

**Hidden Gem Potential (HIGH):** Most technically sophisticated and well-planned proposal. Team clearly has strong skills (excellent QC design). With 80% descope could work:
- **Penn campus only** (not global) - 50-100 locations
- **Web-only** (no mobile app) - eliminates 3-4 weeks
- **Manual location dropdown** (not GPS) - "Van Pelt L2, Huntsman Hall"
- **No ML initially** - simple tagging + voting
- **Utilize problem** - "Find perfect study spot" vs. abstract soundscape exploration
- **Seed data yourself** - team records 30-50 locations

This version could score 22-24/30. Fatal flaw was trying to build production-ready platform instead of working prototype.

---

### GatherAI (AI-Powered iMessage Group Planning)
| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Feasibility | 2/5 | iMessage API (doesn't exist publicly), NLP intent detection, GPT costs |
| Crowdsourcing Viability | 3/5 | Friend groups = natural crowd, but requires full group adoption |
| Incentive Design | 4/5 | Strong intrinsic motivation (hanging out with friends), quick task |
| Scope Appropriateness | 3/5 | Moderate features, but depends on iMessage working |
| Recruitment Strategy | 3/5 | Friend groups accessible, but scaling beyond personal networks hard |
| Quality Control | 3/5 | Structured validation, reputation scoring, reasonable approach |
| **TOTAL** | **18/30** | **NEEDS MAJOR REVISION** |

**Why Dropped:** **iMessage API does NOT exist publicly** (only enterprise Messages for Business). Alternative is Twilio SMS, but then it's just a bot you text (not native integration). Without native iMessage, loses entire value proposition and becomes "just another scheduling bot" competing with Doodle/When2Meet. GPT API costs for message processing could spiral to $500-1000/month. Privacy concerns (reading all group messages). Core value proposition depends on impossible technical requirement.

**Hidden Gem Potential (HIGH - possibly highest in entire dropped set):** This is genuinely excellent concept with strong problem validation and good incentives. Fatal flaw: built on impossible technical foundation (iMessage API). With platform pivot could work:

**Pivot to Slack/Discord:**
- Both have robust, documented APIs
- Target Penn club Slacks and dorm Discords
- Slash command trigger: `/gather "brunch this weekend?"`
- Same core functionality (polls, consensus, reminders)
- Partner with 5-10 Penn clubs for distribution

This version could score 23-25/30 and succeed as A-/A project. The idea itself is excellent; just needed to validate API availability first.

---

## Combined Analysis: All 10 Dropped Round 2 Projects

### Overall Score Distribution
- **11-14 (Stop and Pivot):** 4 projects (FoundryMatch, TerraTruth, Kinnect, CrowdScout)
- **15-17 (Needs Major Revision):** 4 projects (Soundscape, PriceScope, Auralynx, PennPulse)
- **18-19 (Needs Major Revision, borderline):** 2 projects (GatherAI, TrashTag Tracker)

**Average Score:** 15.3/30 (all below "Weak GO" threshold of 20)

### Dimension Averages (All 10 Projects)
1. **Technical Feasibility:** 2.4/5 - Second worst
2. **Crowdsourcing Viability:** 2.4/5 - Tied for second worst
3. **Incentive Design:** 2.6/5 - Third worst
4. **Scope Appropriateness:** 2.3/5 - Worst dimension
5. **Recruitment Strategy:** 2.0/5 - Tied for worst
6. **Quality Control:** 3.6/5 - Only dimension averaging above 3

**Key Insight:** Projects failed primarily on **Scope** and **Recruitment** (both ~2/5). Most teams understood quality control but fundamentally misjudged what was buildable and who would use it.

---

## Updated Common Failure Patterns (All 10 Projects)

### 1. Extreme Technical Overscope (7/10 projects)
- **Video/Media Hosting:** CrowdScout (video platform), Soundscape (audio platform)
- **Mobile Development:** Kinnect (React Native), Soundscape (mobile geo-location)
- **Complex ML/AI:** Auralynx (audio ML), CrowdScout (TikTok algorithm), FoundryMatch (AI matching)
- **Advanced Tech Stacks:** TerraTruth (GIS/PostGIS), Soundscape (audio processing + ML clustering)
- **Multiple Complex Systems:** FoundryMatch (social network + matchmaking + collaboration + market intelligence)

### 2. Critical Technical Dependencies (4/10 projects)
- **Unavailable APIs:** GatherAI (iMessage API doesn't exist)
- **Expensive Infrastructure:** CrowdScout (video CDN costs), Soundscape (audio storage)
- **Partnership-Required Tech:** TerraTruth (NGO data access), PennPulse (org integrations)
- **All built concepts around unvalidated technical assumptions**

### 3. Two-Sided Marketplaces (6/10 projects)
- FoundryMatch (problems + entrepreneurs)
- CrowdScout (athletes + scouts)
- Auralynx (speakers + guessers)
- PennPulse (posters + attendees)
- Kinnect (users + reward partners)
- TerraTruth (NGOs + volunteers)
- **Cold-start problem is severe and rarely solved**

### 4. Weak Incentive Design (8/10 projects)
- High-effort tasks (15-30 min) with weak/no compensation: FoundryMatch, TerraTruth, TrashTag
- Altruism-only: TerraTruth, TrashTag, Soundscape
- Gamification for tedious work: PriceScope, Kinnect, Auralynx
- "Self-sustaining" assumptions: PennPulse
- Only 2 projects (GatherAI, CrowdScout athletes) had strong intrinsic motivation

### 5. Vague Recruitment (10/10 projects - 100%)
- **Generic channels:** "Social media," "volunteers," "online users," "student groups"
- **No specific names:** Zero projects named exact GroupMes, Slacks, subreddits, or clubs
- **No commitments:** No one had pre-secured users or partnerships
- **Partnership-dependent:** 5 projects needed partnerships they didn't have
- **Worst performing dimension:** Average 2.0/5

### 6. Feature Creep (8/10 projects)
- Average features listed: **6.8 features** (should be 3-4 max)
- 5+ features: All projects except TrashTag (5) and PriceScope (5)
- 7-8 features: FoundryMatch (8), Soundscape (8), TerraTruth (7), Kinnect (7), Auralynx (8)
- Each feature compounds integration complexity

---

## Hidden Gem Rankings (All 10 Projects)

### HIGH Potential (3 projects)
1. **GatherAI** - Excellent concept, strong incentives, just needed Slack/Discord pivot instead of iMessage
2. **Soundscape** - Strong technical planning, needed 80% descope to Penn-only web MVP
3. **CrowdScout** - Good problem, needed to avoid video hosting (use links instead)

### MODERATE-HIGH Potential (1 project)
4. **TrashTag Tracker** - Best-structured proposal, needed validation + Penn campus focus

### MODERATE Potential (2 projects)
5. **Auralynx** - Novel insight, needed modality pivot (text/photos instead of audio ML)
6. **PriceScope** - Appropriate tech scope, needed better incentives + Penn-specific gamification

### LOW Potential (3 projects)
7. **PennPulse** - Crowded space, network effects moat, many prior failures
8. **TerraTruth** - Wrong project type (graduate thesis/startup, not class project)
9. **FoundryMatch** - Would need 90% redesign, essentially different project

### VERY LOW Potential (1 project)
10. **Kinnect** - Saturated market, no differentiation, hits all rubric red flags

---

## Updated Lessons Learned

### What Consistently Killed Projects (Ranked by Frequency)

1. **No Concrete Recruitment Plan (10/10 = 100%)**
   - Not a single project named specific channels or secured commitments
   - "Social media" is not a strategy
   - Generic appeals to "volunteers" or "users" without access paths
   - **Lesson: Name exact GroupMes, Slacks, classes, clubs OR don't proceed**

2. **Massive Overscope (8/10 = 80%)**
   - Trying to build 6-8 features in 5 weeks
   - Multiple complex systems instead of one simple loop
   - "Startup pitch" mentality instead of "proof of concept"
   - **Lesson: If you can't build core loop in 2 weeks, it's overscoped**

3. **Weak/Unvalidated Incentives (8/10 = 80%)**
   - Assumptions about "intrinsic motivation" or "self-sustaining" adoption
   - Gamification for high-effort tasks
   - Altruism-only for tedious work
   - **Lesson: Test incentives Week 1, pivot if they don't work**

4. **Technical Overambition (7/10 = 70%)**
   - Mobile apps, video hosting, complex ML, GIS, audio processing
   - All rubric red flags (mobile, ML, APIs, real-time)
   - Underestimating complexity by 5-10x
   - **Lesson: If rubric lists it as red flag, just don't**

5. **Two-Sided Marketplaces (6/10 = 60%)**
   - Need simultaneous critical mass on both sides
   - Cold-start is a known hard problem
   - Rarely solvable in 5 weeks
   - **Lesson: Avoid two-sided markets OR seed one side yourself**

6. **Critical Technical Dependencies (4/10 = 40%)**
   - Building around APIs that don't exist (iMessage)
   - Partnership-dependent tech access (NGO data)
   - Expensive infrastructure (video CDN)
   - **Lesson: Validate API access and costs BEFORE designing**

### Success Factors (What Would Have Saved Them)

1. **Hyperlocal Start (Penn-Only)**
   - Every project would benefit from Penn campus focus
   - Provides captive audience and concrete recruitment channels
   - Enables validation before building

2. **Ruthless Descoping (50-70% cuts)**
   - Cut every "AI-powered" feature
   - Cut every "nice-to-have"
   - Build 1 feature perfectly, not 5 poorly

3. **Week 1 Validation**
   - Test recruitment BEFORE building
   - Test incentives with manual MVP
   - Pivot immediately if failing

4. **Manual MVP First**
   - Wizard of Oz testing
   - Prove demand exists
   - Automate only after validation

5. **Named Recruitment Channels**
   - Specific GroupMes, Slacks, classes
   - Pre-secured commitments
   - Professor/TA/club leader buy-in

6. **Avoid Rubric Red Flags**
   - No mobile (use web)
   - No ML (use manual curation)
   - No video hosting (use links)
   - No complex APIs (use simple CRUD)

---

## Final Verdict: Were These Right to Drop?

### Absolutely Correct (6/10)
1. FoundryMatch (11/30) - Not feasible
2. Kinnect (13/30) - Hits all red flags
3. TerraTruth (14/30) - Wrong project type
4. CrowdScout (14/30) - Video platform impossible
5. Soundscape (15/30) - Web + mobile + ML too much
6. PennPulse (17/30) - Two-sided market, no adoption path

### Reasonable Decision (3/10)
7. PriceScope (16/30) - Weak incentives, but close
8. Auralynx (17/30) - Could pivot, but risky
9. GatherAI (18/30) - Excellent idea, impossible tech dependency

### Borderline / Could Debate (1/10)
10. TrashTag Tracker (19/30) - Could have reached 20-24 with validation

**Average: 15.3/30 - All below 20-point "Weak GO" threshold**

The selection process correctly identified that all 10 projects had multiple structural problems, not just execution risks. Even the best-scoring project (TrashTag at 19) was borderline and would need significant improvements.

**Calibration appears excellent:** These averaged 15.3/30, presumably Round 3 selected projects score 20-25/30, creating clear separation between viable and non-viable ideas.
