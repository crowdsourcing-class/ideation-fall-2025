# PitchPeer - Project Viability Analysis (V2)

**Project**: PitchPeer - Peer Feedback Platform for Startup Ideas
**Authors**: Emily Kang (emkang), Manasi Gajjalapurna (mgajjala)
**Analysis Date**: 2025-11-02
**Rubric Version**: NETS 2130 Project Viability Rubric

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Weight | Rationale |
|-----------|-------|--------|-----------|
| **Technical Feasibility** | 2/5 | Critical | Complex feature set (AI, video, matching, analytics) for 5 weeks |
| **Crowdsourcing Viability** | 2/5 | Critical | Two-sided marketplace with severe cold-start problem |
| **Incentive Design** | 3/5 | High | Gamification plausible for short tasks, but feedback effort underestimated |
| **Scope Appropriateness** | 2/5 | Critical | 10 features with 5+ complex subsystems - dramatically overscoped |
| **Recruitment Strategy** | 2/5 | High | Vague channels without concrete commitments or testing |
| **Quality Control** | 3/5 | Medium | Multiple mechanisms listed but AI QC is underspecified |

### TOTAL SCORE: 14/30

**Category**: NEEDS MAJOR REVISION

---

## EXECUTIVE SUMMARY

PitchPeer is an ambitious peer-review platform for startup validation that combines gamification, AI quality control, and multi-format submissions. While the core concept of crowdsourced startup feedback addresses a real problem, the project suffers from catastrophic scope issues (10 features including video processing, AI assessment, matching algorithms, and analytics) and an unaddressed two-sided marketplace cold-start problem. The proposal conflates "building a startup" with "building a crowdsourcing experiment," treating gamification badges as sufficient motivation for 10-15 minute qualitative feedback tasks. Without dramatic descoping and concrete user recruitment, this project will likely result in a technically impressive but functionally empty platform.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility: 2/5

**Score Justification**:
The project falls squarely in the "Very Risky" category with multiple complex systems that would challenge even professional teams. The feature list includes: React frontend, Flask backend, PostgreSQL database, AI quality assessment (OpenAI API or scikit-learn), video processing, matching algorithms, analytics dashboard, and reputation systems. This represents 3-4 distinct complex systems, each requiring significant implementation time.

**Specific Strengths**:
- Standard web stack (React + Flask + PostgreSQL) is reasonable
- Team has identified specific technologies rather than vague "AI magic"
- Some features (text submission, basic voting) are straightforward CRUD operations
- Modular architecture allows for incremental development

**Specific Weaknesses**:
- **Video processing pipeline**: Accepting, storing, streaming video adds 2-3 weeks minimum
- **AI quality assessment**: "OpenAI API or scikit-learn" glosses over that these require completely different implementation approaches. NLP-based quality detection is a standalone ML project
- **Matching algorithm**: "Peer match" based on experience levels requires user profiling, preference learning, and optimization - easily 2+ weeks
- **Analytics dashboard**: Full-featured analytics is not a weekend task
- **Multiple QC mechanisms**: Reputation weighting, statistical outlier detection, attention checks each require distinct implementation

**Concrete Recommendations**:
1. **CUT IMMEDIATELY**: Video support, matching algorithm, analytics dashboard (first iteration)
2. **SIMPLIFY AI QC**: Use simple heuristics instead of ML for MVP (word count, time spent, keyword presence)
3. **REDUCE to core loop**: Text pitch submission → Random assignment to 3 reviewers → Structured form feedback → Simple aggregate display
4. **"Two Week Test"**: Could they build working text submission + simple rating in 2 weeks? Barely. Could they build current proposal? No chance.
5. **Use manual simulation**: Week 1 should be Google Forms + manual assignment to prove the feedback loop works before building anything

**Passes "Two Week Test"?**: NO for current scope, BARELY for descoped version

---

### 2. Crowdsourcing Viability: 2/5

**Score Justification**:
PitchPeer is a classic two-sided marketplace facing the cold-start problem: founders won't submit pitches without active reviewers, reviewers won't participate without pitches to review. The proposal lists recruitment sources (university communities, LinkedIn groups, forums) but provides no evidence these audiences are committed or even interested. The value proposition requires network effects to work.

**Specific Strengths**:
- Reciprocal model (submit and review) addresses some cold-start issues
- Target audience (student entrepreneurs) is somewhat accessible via university channels
- Feedback on startup ideas has inherent value to founders
- Platform could be seeded with team-submitted pitches

**Specific Weaknesses**:
- **Circular dependency**: "Users can both submit pitches and review others" requires critical mass to work
- **Unproven value**: Will entrepreneurs trust peer feedback from strangers? No validation
- **No captive audience**: Lists channels but no confirmed access or commitments
- **Network effects required**: Platform is nearly worthless with <50 active users
- **High-effort ask**: Reviewing startup pitches requires 10-15 minutes of thoughtful evaluation
- **Competitive alternatives**: Reddit r/startups, YC Startup School Forum are free and already active

**Concrete Recommendations**:
1. **SECURE captive audience NOW**: Get written commitment from one entrepreneurship class/club (min 30 people) BEFORE building
2. **Seed aggressively**: Team + collaborators create 20-30 realistic pitches to populate platform
3. **Test demand immediately**: Post in one target community this week - "Would you use a platform for peer startup feedback?" - gauge response
4. **Add immediate value**: What does user #1 get? Consider expert review for first 50 submissions as incentive
5. **Solve asymmetry**: Most want feedback, fewer want to give it. Consider requiring 2 reviews per submission or paid reviewers
6. **Backup plan**: If organic recruitment fails by Week 2, pivot to MTurk-paid reviewers or class-only deployment

**Passes "Friend Test"?**: MAYBE - depends on whether friends are entrepreneurs and if reciprocity works

---

### 3. Incentive Design: 3/5

**Score Justification**:
The incentive structure relies heavily on gamification (points, badges, leaderboards) and reputation for tasks requiring 10-15 minutes of thoughtful evaluation. This is a mismatch but not fatal - gamification CAN work for medium-effort tasks IF there's strong intrinsic motivation and community. The proposal scores in "Acceptable" range but teeters toward "Mismatch."

**Specific Strengths**:
- Multiple incentive layers: points, badges, reputation, leaderboard, networking
- Reputation-based privileges (ability to post more pitches) creates tangible value
- Target audience (entrepreneurs) may have intrinsic interest in reviewing peers
- "Top reviewer highlights" provides social recognition
- Reciprocity model creates implicit incentive (give feedback to get feedback)

**Specific Weaknesses**:
- **Task time underestimated**: Quality feedback on startup idea = 10-15 min, not the 2-5 min implied
- **Badges without community**: Points/badges are meaningless without active user base to compete with
- **Networking promise unfulfilled**: "Potential networking opportunities" is vague - how does reputation translate to connections?
- **Intrinsic motivation unproven**: Assumes entrepreneurs WANT to review others' ideas - needs validation
- **No payment budget**: $250 budget exists on paper but "focused primarily on organic participation"

**Concrete Recommendations**:
1. **Reduce task effort**: Simplify review form - 5 min max with structured questions (3-5 ratings + one text box)
2. **Make reciprocity explicit**: "Review 2 pitches to submit yours" rather than optional
3. **Test intrinsic motivation**: Survey target users - "Would you spend 5 min reviewing a peer's startup idea for badges/points?"
4. **Add showcase value**: Top reviewers get profile feature, can display expertise publicly
5. **Consider hybrid model**: First 50 reviews are paid ($5 each) to seed system, then gamification takes over
6. **Backup incentive**: If gamification fails, use class credit or small payments

**Passes "Would I Do It Test"?**: MAYBE - 5 min structured review for reputation/reciprocity is plausible, 15 min detailed review for badges is not

---

### 4. Scope Appropriateness: 2/5

**Score Justification**:
The proposal lists 10 key features, with at least 5 being complex subsystems requiring significant development. The project is firmly in the "Overscoped" category. Building video processing, AI quality assessment, matching algorithms, and analytics dashboards are each standalone projects. This is "building a startup" rather than "proving a crowdsourcing concept."

**Specific Strengths**:
- Core concept (text pitch + structured feedback + aggregation) is viable
- System architecture is modular and could be built incrementally
- Team has identified specific technologies rather than handwaving
- Some features (structured templates, majority voting) are straightforward

**Specific Weaknesses**:
- **Feature bloat**: 10 features for 5-week timeline is 2x appropriate scope
- **Complex features treated as simple**: "AI-assisted quality assessment" and "Peer match algorithm" are 2-3 week projects each
- **No Must/Should/Could prioritization**: All features presented as equally important
- **Video support**: Accepting video adds authentication, storage (S3), transcoding, streaming - 2+ weeks
- **Analytics dashboard**: "Tracking feedback and progress" implies charts, metrics, exports - 1-2 weeks
- **No MVP definition**: What's the MINIMUM to prove the concept?

**Concrete Recommendations**:
1. **IMMEDIATE DESCOPE - Cut to 3-4 features**:
   - MUST: Text pitch submission, structured review form, basic aggregation, simple display
   - SHOULD: Reviewer reputation (simple scoring), pitch listing/browsing
   - COULD: Badges/leaderboard (if time permits)
   - WON'T: Video, AI QC, matching, analytics, anonymous mode, accelerator integration
2. **Replace AI with heuristics**: Check word count (>50 words), time spent (>2 min), required fields completed
3. **Manual matching initially**: Randomly assign 3 reviewers per pitch, no optimization
4. **Simple aggregation**: Average ratings + concatenate text feedback, no NLP
5. **Build horizontal slice**: Complete end-to-end flow for text pitches before adding features
6. **Apply "Two Week Test"**: If core loop isn't working by Week 2, all other features are irrelevant

**Passes "Feature Count Test"?**: NO - has 10 features, need to cut to 3-4

---

### 5. Recruitment Strategy: 2/5

**Score Justification**:
The proposal lists multiple potential recruitment sources but lacks specificity, commitments, or testing. "University entrepreneurship communities, LinkedIn startup groups, online forums" is a general plan without named channels or proven access. This falls in the "Vague hope" category - better than magic thinking but far from concrete.

**Specific Strengths**:
- Multiple channel types identified (university, social, forums)
- Target audience (entrepreneurs, business students) is somewhat accessible
- Specific communities named (Indie Hackers, Product Hunt, r/startups)
- Plan to partner with university programs shows strategic thinking
- Scale requirements are reasonable (100 minimum, 1000 target)

**Specific Weaknesses**:
- **No named commitments**: "University entrepreneurship communities" - which ones? Have you contacted them?
- **No testing**: Has team posted recruitment message anywhere to gauge interest?
- **No backup plan**: What if LinkedIn/forums don't respond? Only vague mention of "paid campaigns"
- **Partnership dependency**: "Integration with university accelerators" is nice-to-have, not Week 1 viable
- **Two-sided problem unaddressed**: Need both pitch submitters AND reviewers simultaneously
- **No seeding plan**: Who creates initial content before users arrive?

**Concrete Recommendations**:
1. **NAME SPECIFIC CHANNELS NOW**:
   - "Penn Venture Lab's Slack workspace (150 members, already contacted admin)"
   - "Wharton Entrepreneurship Club email list (200 members, presenting at next meeting)"
   - "NETS 2130 class (30 students, offering extra credit for participation)"
2. **TEST RECRUITMENT THIS WEEK**: Post in one target community, measure response rate
3. **GET COMMITMENTS**: Email 3-5 entrepreneurship groups requesting partnership - track responses
4. **SEED PLATFORM**: Team creates 20 pitches and completes 60 reviews (3 per pitch) before launching
5. **BACKUP PLAN**: If <30 signups by Week 2, pivot to:
   - Option A: MTurk-paid reviewers for feedback quality experiment
   - Option B: Class-only deployment with synthetic pitches
   - Option C: Focus on single university accelerator cohort
6. **METRICS**: Track signup source, conversion rate, active users weekly

**Passes "Specificity Test"?**: NO - cannot name exact groups with confirmed access

---

### 6. Quality Control: 3/5

**Score Justification**:
The proposal includes multiple QC mechanisms (majority voting, expert review, attention checks, reputation, outlier detection) which shows thoughtful planning. However, the "AI-assisted feedback quality assessment" is underspecified and likely vaporware. Overall, this scores in "Basic" category - has redundancy plus other mechanisms, but lacks specific thresholds and implementation details.

**Specific Strengths**:
- Multiple QC layers proposed: redundancy, reputation, expert review, attention checks, outlier detection
- Specific redundancy: "At least 3 reviewers per pitch"
- Expert review sampling: "10% of submissions reviewed by experienced entrepreneurs"
- Reputation system creates long-term accountability
- Filters low-effort responses rather than accepting all contributions
- Uses consensus scoring (majority voting) to handle disagreement

**Specific Weaknesses**:
- **AI QC is vaporware**: "AI-assisted feedback quality assessment" with no implementation details - NLP for quality detection is complex
- **No specific thresholds**: What constitutes "low-effort"? What's outlier threshold? What happens on disagreement?
- **Expert review unsustained**: Where do "experienced entrepreneurs" come from? Can't rely on this long-term
- **Attention checks vague**: "Random prompts requiring specific keywords" - what prompts? How often?
- **Reputation cold-start**: New users have no reputation, yet system weights by reputation
- **Over-engineered for scale**: Building complex QC before having users to apply it to

**Concrete Recommendations**:
1. **SIMPLIFY AI QC FOR MVP**:
   - Don't build ML quality classifier
   - Use simple heuristics: word count >50, time spent >2 min, all required fields completed
   - Flag reviews with <30 words or completed in <60 seconds
2. **DEFINE SPECIFIC THRESHOLDS**:
   - Agreement: Flag pitch if 3 reviews have stdev >1.5 on any dimension
   - Outliers: Flag review if >2 standard deviations from mean on multiple dimensions
   - Low-effort: <50 words in text feedback OR <2 min completion time
3. **REPUTATION BOOTSTRAP**: New users start with neutral score (3.0/5), earns reputation after 5 reviews
4. **ATTENTION CHECKS**: Insert 1 attention check per 10 reviews - "To ensure quality, please type the word 'startup' in your response"
5. **EXPERT REVIEW REALISTIC**: Instructor/TA reviews 10% initially, decrease as reputation system matures
6. **START SIMPLE, ADD LATER**: Week 1-3 use basic redundancy only, add sophistication as user base grows

**Passes "Bad Actor Test"?**: PARTIALLY - has mechanisms but lacks specificity

---

## RISK ANALYSIS

### Top 3 Risks

#### RISK 1: Cold-Start Failure (CRITICAL)
**Description**: Platform launches but fails to attract sufficient users to create viable feedback ecosystem. Founders won't submit without active reviewers, reviewers won't engage without pitches to review.

**Likelihood**: HIGH (70%+)
**Impact**: CATASTROPHIC - Empty platform, project fails

**Mitigation Strategies**:
1. **Pre-launch commitments**: Secure 30+ committed users (entrepreneurship class/club) BEFORE building
2. **Aggressive seeding**: Team creates 20-30 realistic pitches and completes initial reviews
3. **Forced reciprocity**: Require 2 reviews per submission to ensure reviewer supply
4. **Week 2 checkpoint**: If <30 active users, immediately pivot to paid reviewers (MTurk) or class-only
5. **Partner with accelerator**: Deploy with single cohort (10-15 founders) as captive pilot group

**Contingency Plan**: Pivot to MTurk-paid model (quality comparison experiment) or single-cohort case study

---

#### RISK 2: Scope Collapse (CRITICAL)
**Description**: Team spends Weeks 1-3 building video processing, AI quality control, and matching algorithm, realizes Week 4 they have no users and core features don't work. End result: impressive tech demo with no validation.

**Likelihood**: VERY HIGH (80%+)
**Impact**: HIGH - Fail to prove crowdsourcing concept, mediocre grade

**Mitigation Strategies**:
1. **Descope NOW**: Cut video, AI QC, matching, analytics immediately - non-negotiable
2. **Build core loop Week 1**: Text submission + review form + display must work by end of Week 1
3. **Manual simulation first**: Use Google Forms for Week 1 to test feedback flow before coding
4. **Recruitment parallel track**: One team member recruits users while others build (don't wait for polish)
5. **Weekly scope check**: End of each week, assess if on track - cut additional features if behind

**Contingency Plan**: If Week 2 shows <50% progress on core loop, cut ALL non-essential features and focus on text-only MVP

---

#### RISK 3: Incentive Failure (HIGH)
**Description**: Gamification (badges, points, leaderboards) proves insufficient to motivate 10-15 minute thoughtful feedback tasks. Users sign up but don't contribute quality reviews, or contribute once and never return.

**Likelihood**: MEDIUM-HIGH (60%)
**Impact**: HIGH - Platform exists but feedback is low-quality or sparse

**Mitigation Strategies**:
1. **Test incentives early**: Week 1 survey of target users - "Would you review 2 pitches for badges/reputation?"
2. **Simplify task**: Reduce review to 5 min max (structured ratings + brief comment)
3. **Enforce reciprocity**: Can't submit pitch without reviewing 2 others first
4. **Add monetary backup**: Budget for $5/review payment if gamification fails (50 reviews = $250)
5. **Increase intrinsic value**: Partner with accelerator so reputation on platform becomes professional signal
6. **Monitor retention**: Track Week 2 retention rate - if <40%, pivot to paid model immediately

**Contingency Plan**: Switch to hybrid model - pay for first review ($3), gamification for repeat engagement

---

## DECISION GUIDANCE

### RECOMMENDATION: NEEDS MAJOR REVISION

**Confidence Level**: HIGH

**One-Sentence Most Critical Change Needed**:
Cut scope by 60% (drop video, AI QC, matching, analytics) and secure 30+ committed users from specific entrepreneurship class/club before writing any code.

**Predicted Outcome if NO Changes Made**:

**Week-by-Week Likely Scenario**:
- **Week 1-2**: Team builds React frontend, Flask backend, basic database - feels productive
- **Week 3**: Implements video upload to S3, starts on "AI quality assessment," realizes both are harder than expected
- **Week 4**: Scrambles to finish core features, launches to "university communities" via vague social posts
- **Week 5**: Gets 10-15 signups (mostly classmates), 20-30 total feedbacks, tries to demo with sparse data

**Final Outcome**:
- Technically functional platform with slick UI
- 10-15 total users, 5-7 pitches submitted, 20-30 reviews completed
- Demo shows system works but no meaningful validation of crowdsourcing approach
- "It would work if we had more users" defense
- **Grade Prediction: B-/C+** - Technical merit but weak crowdsourcing validation

**What Success Looks Like (If Changes Made)**:
- Descoped to text-only MVP by Day 3
- 30+ users committed from entrepreneurship class by Week 1
- 50+ pitches submitted, 150+ reviews (3 per pitch) by Week 5
- Data shows feedback quality distribution, reviewer behavior patterns, reciprocity effects
- Can make claims about peer feedback efficacy
- **Grade Prediction: A-/B+** - Solid validation with real users

---

## COMPARISON TO V1 ANALYSIS

### What Changed from V1 to V2

**V1 Analysis Verdict**: WEAK GO / NEEDS MAJOR REVISION (C+ crowdsourcing, D+ feasibility)
**V2 Analysis Verdict**: NEEDS MAJOR REVISION (14/30 total score)

**Key Differences in Approach**:

1. **Structured Scoring**: V2 provides quantified scoring across 6 dimensions vs V1's qualitative assessment, making weaknesses more concrete

2. **More Specific Recommendations**: V1 said "drastically reduce scope" - V2 specifies exactly which 6 features to cut and which 4 to keep

3. **Deeper Incentive Analysis**: V2 explores intrinsic motivation and reciprocity dynamics more thoroughly than V1's "gamification without meaningful value" critique

4. **Concrete Risk Mitigation**: V2 provides specific mitigation strategies with metrics (e.g., "Week 2 checkpoint: if <30 users, pivot to MTurk") vs V1's general warnings

5. **Recruitment Specificity**: V2 pushes harder on naming exact channels and getting commitments vs V1's identification of cold-start problem

### What V2 Reveals That V1 Missed

1. **Quality Control Depth**: V1 dismissed AI QC as "vaporware" without examining other mechanisms. V2 credits the multiple QC layers while still critiquing AI implementation

2. **Incentive Nuance**: V2 recognizes that gamification COULD work for entrepreneurs with strong intrinsic motivation (3/5 score) vs V1's blanket dismissal

3. **Partial Viability Path**: V2 identifies that a heavily descoped version (text-only with committed users) could succeed, providing clearer path forward

4. **Quantified Predictions**: V2 predicts specific outcome (10-15 users, 20-30 feedbacks) vs V1's "limited validation"

### What Both Analyses Agree On

1. **Catastrophic scope problem** - Both identify 10 features as dramatically overambitious
2. **Cold-start risk** - Both highlight two-sided marketplace dependency
3. **User recruitment vagueness** - Both critique lack of concrete commitments
4. **Predicted outcome without changes** - Both predict functional but empty platform

### Additional Insights from Rubric

1. **Numeric scoring makes tradeoffs clear**: 14/30 objectively shows project needs intervention, not just improvement

2. **Dimension-specific fixes**: Rubric reveals that fixing recruitment (2→4) and scope (2→4) would move project from "Needs Revision" (14/30) to "Weak GO" (20/30)

3. **Risk prioritization**: V2's risk analysis shows cold-start and scope are CRITICAL while QC is MEDIUM - helps prioritize fixes

4. **Actionable thresholds**: Rubric's specific tests ("Two Week Test", "Friend Test") provide concrete validation steps

### Why V2 Score (14/30) Aligns with V1 (WEAK GO)

Both analyses reach similar conclusions through different frameworks:
- V1: "C+ crowdsourcing, D+ feasibility" ≈ 2.3-2.5/5 average ≈ 14-15/30
- V2: 14/30 = "Needs Major Revision" category

**V2 advantage**: Provides structured improvement path with specific score targets per dimension

---

## FINAL SUMMARY

PitchPeer addresses a real problem (startup validation feedback) with a theoretically sound approach (peer crowdsourcing with gamification). However, the project currently conflates "building a platform" with "running a crowdsourcing experiment."

**The core insight is valuable**: Entrepreneurs may be willing to exchange peer feedback. But this needs to be TESTED with a minimal system and committed users, not assumed and over-built.

**Viability Path Forward**:
1. Cut 60% of features immediately (text-only, no AI/video/matching/analytics)
2. Secure 30+ committed users from specific group before coding
3. Build core loop in Week 1, test with real users Week 2
4. Add features ONLY if core loop works and users are engaged
5. Have backup plan (MTurk or class-only) if organic recruitment fails

**Bottom Line**: With major descoping and concrete user commitments, this could become a successful project validating peer feedback mechanisms. Without changes, it will be an impressive technical demo of an empty platform.
