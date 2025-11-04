# Project Viability Rubric for NETS 2130

**Purpose**: Quick self-assessment tool to evaluate if your crowdsourcing project idea is feasible for a 5-week timeline with limited budget.

**How to Use**:
1. Rate your project on each dimension (1-5 scale)
2. Calculate your total score
3. Read the interpretation and recommendations
4. Identify your biggest risks

---

## The Six Dimensions

### 1. Technical Feasibility ⚙️
**Question**: Can you build the core system in 5 weeks?

| Score | Description | Example |
|-------|-------------|---------|
| 5 | **Simple stack** - CRUD app with standard tech, no complex integrations | Basic voting/rating system with forms |
| 4 | **Moderate complexity** - One new API or moderate feature (maps, auth, basic ML) | App with Mapbox integration |
| 3 | **Challenging but doable** - 2-3 new technologies or moderate systems | Web app + ML model + external API |
| 2 | **Very risky** - Mobile development OR complex ML OR satellite/GIS | Mobile app or audio ML pipeline |
| 1 | **Impossible** - Multiple complex systems (mobile + ML + APIs) | Mobile + fitness APIs + ML + payments |

**Your Score**: 5 / 5

**Red Flags**:
- Mobile app development (add 3-4 weeks to any timeline)
- Complex ML (audio, video, satellite imagery)
- Multiple external APIs (fitness APIs, satellite data)
- Real-time features (live updates, sync)
- GIS/geospatial pipelines

---

### 2. Crowdsourcing Viability 👥
**Question**: Will people actually participate?

| Score | Description | Example |
|-------|-------------|---------|
| 5 | **Captive audience** - You have direct access to committed users | Your class, dorm, club you're in |
| 4 | **Clear value proposition** - Users get obvious benefit for participating | Review site for a service you use |
| 3 | **Moderate value** - Some benefit but requires trust or network effects | Social platform with new feature |
| 2 | **Weak value** - Benefits require scale OR unclear to users | Badges/points without community |
| 1 | **No value** - Asking strangers to do work for you for free | Complex tasks for gamification |

**Your Score**: 2 / 5

**Red Flags**:
- Depends on partnerships (food trucks, NGOs, etc.) you don't have yet
- Circular value (need users to attract users)
- High-effort tasks (15+ minutes) with low rewards
- Two-sided marketplace (need both sides simultaneously)
- "If you build it, they will come" assumption

---

### 3. Incentive Design 💰
**Question**: Do your incentives match the task difficulty?

| Score | Description | Task Type → Incentive |
|-------|-------------|----------------------|
| 5 | **Perfect match** | Quick votes (30 sec) → badges/points |
| 4 | **Good match** | Short contributions (2-5 min) → leaderboard + intrinsic |
| 3 | **Acceptable** | Moderate effort (5-10 min) → small payment + reputation |
| 2 | **Mismatch** | High effort (15+ min) → badges only |
| 1 | **Backwards** | Creative work (30 min) → unpaid with weak gamification |

**Your Score**: 4 / 5

**Quick Assessment**:
- **Task < 2 min + fun**: Gamification can work
- **Task 2-10 min + tedious**: Need payment or strong intrinsic motivation
- **Task > 10 min**: MUST pay or have captive audience
- **Creative tasks**: Requires ownership/showcase value OR payment

**Formula Check**:
```
If (Task Time × Boredom Level) > (Incentive Value),
then you have a problem.
```

---

### 4. Scope Appropriateness 📏
**Question**: Is this the right amount of work for 5 weeks?

| Score | Description | Feature Count |
|-------|-------------|---------------|
| 5 | **Perfect scope** - Core loop + 3-4 essential features | 3-5 features total |
| 4 | **Slight stretch** - Core loop + 5-6 features | 5-7 features total |
| 3 | **Risky** - Many features but some could be cut | 8-10 features with wishlist |
| 2 | **Overscoped** - Too many "essential" features | 10+ features all marked essential |
| 1 | **Fantasy** - Building a startup/product in 5 weeks | Full platform with multiple subsystems |

**Your Score**: 5 / 5

**Scope Test**:
1. Could you build a working demo of the CORE loop in 2 weeks? (If no → overscoped)
2. Could you manually simulate the system before building it? (If no → too complex)
3. Can you name exactly 3-4 must-have features? (If >5 → feature creep)

---

### 5. Recruitment Strategy 🎯
**Question**: How will you get your first 50 users/workers?

| Score | Description | Specificity |
|-------|-------------|-------------|
| 5 | **Concrete & committed** | "My dorm's GroupMe (200 people), already talked to RA" |
| 4 | **Specific channels** | "5 specific Facebook groups, 3 subreddits with mod approval" |
| 3 | **General plan** | "Reddit communities, social media, MTurk" |
| 2 | **Vague hope** | "Social media campaigns, word of mouth" |
| 1 | **Magic thinking** | "Users will find us" or depends on impossible partnerships |

**Your Score**: 4 / 5

**Specificity Test**:
- Can you NAME the exact groups/places? (If no → too vague)
- Have you TESTED recruitment (posted anywhere)? (If no → risky)
- Do you need >50 people to start? (If yes → cold-start problem)
- Can you seed it yourself (team creates initial data)? (If no → chicken-egg)

---

### 6. Quality Control 🎓
**Question**: How will you ensure quality contributions?

| Score | Description | Mechanisms |
|-------|-------------|------------|
| 5 | **Multi-layered** | Gold standard + redundancy + statistical filtering + review |
| 4 | **Thoughtful** | 2-3 mechanisms with specific thresholds/numbers |
| 3 | **Basic** | Redundancy/voting + one other mechanism |
| 2 | **Vague** | "We'll use quality control" without specifics |
| 1 | **None** | Assumes all contributions are good faith |

**Your Score**: 3 / 5

**Common Mechanisms**:
- ✅ Gold standard questions (test with known answers)
- ✅ Redundancy (multiple workers per task)
- ✅ Reputation systems (track worker history)
- ✅ Expert review (sample checking)
- ✅ Statistical outlier detection
- ✅ Attention checks

**Red Flags**:
- "AI will check quality" (if you're not implementing the AI)
- Overly complex QC for pre-product (before you have users)
- QC costs > contribution costs (paying more to check than to do)

---

## Scoring & Interpretation

### Calculate Your Total Score
**Total**: 23 / 30

### Score Ranges

#### 25-30: Strong GO ✅
**Interpretation**: Your project is well-scoped and feasible. Proceed with confidence.

**Recommendations**:
- Document your assumptions (recruitment, tech choices)
- Build core loop first, features second
- Start recruitment Week 1, don't wait for polish

**Predicted Outcome**: A-/B+ range if executed well

---

#### 20-24: Weak GO / Monitor Closely 🟡
**Interpretation**: Viable but has 1-2 significant risks that need mitigation.

**Recommendations**:
- Identify your lowest-scoring dimension (that's your biggest risk)
- Create backup plan if that dimension fails
- Consider descoping or pivoting in one area

**Example Fixes**:
- Score low on Feasibility? → Cut 50% of features NOW
- Score low on Viability? → Get commitments Week 1 or pivot
- Score low on Incentives? → Add payment budget or reduce task time

**Predicted Outcome**: B range if risks are managed, C+ if ignored

---

#### 15-19: Needs Major Revision 🟠
**Interpretation**: Project has multiple serious issues. Needs significant rethinking.

**Required Actions**:
1. Identify 2-3 dimensions scoring ≤3
2. Pick ONE to fix completely (don't spread effort)
3. Significantly descope or pivot in others
4. Meet with instructor/TA for guidance

**Common Patterns**:
- **Overambitious tech + weak recruitment** → Cut features, focus on one channel
- **Weak incentives + high-effort tasks** → Add payment OR simplify tasks dramatically
- **Poor scope + complex features** → Build 1 feature perfectly, not 10 poorly

**Predicted Outcome**: C+ range unless major changes made

---

#### 10-14: Stop and Pivot 🔴
**Interpretation**: Project is not feasible as described. Needs complete rethink.

**Immediate Actions**:
1. Meet with instructor ASAP (required, not optional)
2. Choose: Pivot idea completely OR descope by 70%
3. If pivoting: Use same domain but simpler approach
4. If descoping: Pick the ONE core feature and build only that

**Common Patterns**:
- Mobile app + complex backend + ML → Choose ONE, drop others
- Partnership-dependent + complex tech → Drop partnerships OR simplify tech
- High-effort unpaid tasks + complex system → Pay for tasks OR simplify dramatically

**Predicted Outcome**: C range unless rescued with intervention

---

#### <10: Not Feasible 🚫
**Interpretation**: This project cannot be completed in 5 weeks with available resources.

**Required Actions**:
1. **Stop immediately** - do not proceed with this idea
2. Mandatory meeting with instructor within 48 hours
3. Choose a new idea OR dramatically reimagine the approach
4. Focus on proving ONE concept, not building a platform

**You likely have**:
- Mobile app + multiple APIs + ML + payment system
- Partnerships required that take months to secure
- 30+ minute unpaid tasks with weak incentives
- No clear path to first 50 users

**Path Forward**:
- Salvage the core insight but rebuild everything else
- Example: "Travel recommendations" → Can you validate existing itineraries instead of creating new ones?
- Example: "Mobile fitness app" → Can you build web-only for one specific challenge?

---

## Design Space Analysis

### How to Improve Your Score

**If you scored low on Technical Feasibility**:
- ➡️ Cut mobile, build web only
- ➡️ Use simpler tech stack (avoid ML, GIS, satellite)
- ➡️ Reduce from 10 features to 3-4 core features
- ➡️ Focus on CRUD + one special thing
- ➡️ Ask: "What's the simplest version that proves the concept?"

**If you scored low on Crowdsourcing Viability**:
- ➡️ Identify a captive audience you have access to
- ➡️ Add immediate user value (don't require network effects)
- ➡️ Reduce friction to participate (easier tasks, faster signup)
- ➡️ Seed the system yourself (team creates initial content)
- ➡️ Ask: "Would I use this if only 10 people were on it?"

**If you scored low on Incentive Design**:
- ➡️ Match incentive to effort:
  - Quick tasks → gamification
  - Medium tasks → small payment
  - Long tasks → meaningful payment
- ➡️ Add intrinsic motivation (ownership, showcase, learning)
- ➡️ Create social incentives (team challenges, leaderboards with friends)
- ➡️ Ask: "Would I do this task for this reward?"

**If you scored low on Scope**:
- ➡️ Use "Must/Should/Could/Won't" framework
- ➡️ Cut every "AI-powered" feature (add manual version)
- ➡️ Cut every "nice-to-have" feature
- ➡️ Build horizontal slice (end-to-end core loop) not vertical (all features half-done)
- ➡️ Ask: "Can I demo the core loop in 2 weeks?"

**If you scored low on Recruitment**:
- ➡️ Name specific channels (not "social media")
- ➡️ Test recruitment THIS WEEK (post somewhere)
- ➡️ Get commitments, don't assume interest
- ➡️ Have backup plan (MTurk budget if organic fails)
- ➡️ Ask: "Have I actually talked to potential users?"

**If you scored low on Quality Control**:
- ➡️ Add redundancy (3-5 workers per task)
- ➡️ Add gold standard questions (10% of tasks)
- ➡️ Add basic reputation tracking
- ➡️ Don't over-engineer before you have data
- ➡️ Ask: "Can I detect bad actors with these mechanisms?"

---

## Quick Diagnostic Questions

Answer these honestly:

1. **The "Two Week Test"**: Could you build a working core loop in 2 weeks?
   - If NO → Technical feasibility problem

2. **The "Friend Test"**: Would your friends use this if you asked them?
   - If NO → Viability problem

3. **The "Would I Do It Test"**: Would you do the crowdsourcing task for the offered reward?
   - If NO → Incentive design problem

4. **The "Feature Count Test"**: Can you list exactly 3-4 must-have features?
   - If NO (>5 features) → Scope problem

5. **The "Specificity Test"**: Can you name exactly where you'll recruit 50 people?
   - If NO → Recruitment problem

6. **The "Bad Actor Test"**: How would you catch someone trying to game your system?
   - If "I don't know" → Quality control problem

---

## Common Project Archetypes & Their Risks

### "The Marketplace" (Two-sided platforms)
**Examples**: Peer review platforms, service matching, event discovery
**Common Score**: 18-22
**Biggest Risk**: Cold-start problem (need both sides)
**Fix**: Seed one side yourself OR focus on single side first

### "The Data Collector" (Gathering user contributions)
**Examples**: Sound libraries, photo collections, crowdsourced datasets
**Common Score**: 16-20
**Biggest Risk**: Weak incentives for tedious work
**Fix**: Pay for contributions OR make task fun/quick

### "The Validator" (Checking existing data)
**Examples**: Fact-checking, ranking, voting systems
**Common Score**: 22-26
**Biggest Risk**: Getting enough volume to matter
**Fix**: Usually more viable than creation, focus on recruitment

### "The Social Experiment" (Behavioral research)
**Examples**: Mood tracking, decision-making studies, social dynamics
**Common Score**: 20-24
**Biggest Risk**: IRB approval + participant recruitment
**Fix**: Use Penn-specific channels, keep tasks simple

### "The Complex Pipeline" (Multi-stage processing)
**Examples**: ML training workflows, satellite analysis, audio processing
**Common Score**: 12-16
**Biggest Risk**: Technical complexity prevents finishing
**Fix**: Cut ML/advanced features, do manual versions

---

## Action Items Checklist

After scoring your project, complete these:

### Week 0 (Before You Start)
- [ ] Calculate your viability score
- [ ] Identify your 2 biggest risks (lowest scores)
- [ ] Create backup plan for biggest risk
- [ ] Get instructor feedback if score <20

### Week 1 (First Week of Project)
- [ ] Build core loop (simplest version)
- [ ] Test recruitment strategy (post somewhere)
- [ ] If recruitment fails → pivot immediately
- [ ] If tech is harder than expected → descope immediately

### Week 2 (Reality Check)
- [ ] Do you have 10+ committed users? If no → pivot
- [ ] Is core loop working? If no → cut all features
- [ ] Are you on track to finish in 3 weeks? If no → meet with instructor

---

## Summary: The Three Golden Rules

### 1. Build Less, Finish More
**Cut 50% of features. If it hurts, cut 50% more.**

### 2. Recruit Early, Pivot Fast
**Test recruitment Week 1. If it fails, change strategy immediately.**

### 3. Match Effort to Incentive
**30-min unpaid tasks don't work. Quick tasks can be fun. Everything else needs payment.**

---

**Remember**: The goal is to build something that **works** and proves a **concept**, not to build a startup. A simple, working system with real users beats a complex, half-finished platform every time.

**Questions?** Use this rubric in office hours to discuss your scores and get specific advice.
