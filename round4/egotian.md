# Round 4 Reflection: Final Project Decision

**Name**: Eitan Gotian
**PennKey**: egotian
**Date**: 2025-11-04

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| TerraTruth | R1 | Compelling mission, but fact-verification workload and recruitment look heavy for MVP. |
| MoodMap | R1 | Fun concept with clear UI, but data freshness and incentive alignment are challenging. |
| SoundScape | R1 | Technically feasible, yet seeding high-quality audio content is non-trivial early on. |

_Add more rows if needed_

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [x] V2 detailed analyses (reports/v2-analyses/)
- [] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [x] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: StreetEats

**Decision type**:
- [x] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): 
- Original round: 

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

StreetEats tackles a concrete, recurring pain point with a simple, demonstrable core loop (map + check-ins). Our technical stack is standard and feasible, and our quality control plan is thoughtful. Professor feedback (V1 and V2) underscores that the concept is sound; the main execution risks are recruitment and incentives during cold-start.

Staying the course lets us capitalize on strong technical feasibility while applying the feedback immediately: narrow to University City, prioritize owner partnerships from Week 0, manually seed early data, and keep the MVP ruthlessly simple. This preserves focus and momentum while directly mitigating the cold-start risk.

**What convinced me**:
- Clear user pain and daily repeat use cases
- Simple, testable core loop (pins + one-tap check-ins)
- Strong QC direction that can start simple and evolve

**What concerns me** (and how I'll address it):
- Cold-start/network effects → Owner partnerships + manual seeding first 1–2 weeks
- Incentives for early contributors → One-tap updates + partner raffle; consider micro-payments if needed
- Scope creep → Strict MVP: map, check-ins, simple consensus; cut everything else for now

---

## 4. What I'm Building

**One-sentence project description**:
Real-time, crowd-verified food truck map for University City.

**MVP Scope** (3-4 core features only):

1. **Map with truck pins and status**: Open/closed indicator with last updated timestamp.
2. **One-tap check-in with auto-location**: 30-second contribution flow.
3. **Simple consensus rule**: 3 agreeing check-ins → publish/update status.
4. **Basic truck pages (read-only)**: Hours, brief description, last updates.

**What I'm explicitly NOT building** (to keep scope realistic):
- Push notifications
- Advanced reputation/confidence scoring
- Full owner portal
- Complex filters/favorites/review system

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: Penn class Facebook groups (2025–2028), 3 course Slacks, 2 GroupMes, on-site QR codes at 5 trucks (University City)
- **When**: Mon–Wed next week at 10am and 6pm; on-site tabling/QR outreach Wed 12–2pm
- **What**: Recruit contributors to perform one-tap check-ins; promote a partner-sponsored “free item raffle” for participants
- **Success metric**: ≥20 unique contributors, ≥60 check-ins, ≥5 actively updated trucks by end of Week 1

**If Week 1 test fails, I will**:
- [x] Pivot to: Food Truck Directory (manual updates) if <20% success by end of Week 1
- [x] Use MTurk/paid participants
- [x] Try different recruitment channel: Dining-focused clubs, Instagram ads, on-site flyers at additional trucks
- [x] Simplify the task to: Check-in only (no photos/text), 1-tap flow
- [x] Other: Micro-incentives ($0.25/update) for a 2-week paid seeding pilot

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. Braden Johnson (bradenj) 
2. Simon Roling (rolings)
3. Jackson Gold (jgold23)
4. Eitan Gotian (egotian)
5. Kieran Chetty (chettyk)

**Team status**:
- [x] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
The rubric-guided V2 analysis and instructor feedback made the execution risks concrete and prioritizable.

**Biggest surprise**:
How existential owner partnerships are for Week 0—this dwarfs most technical concerns early on.

**One thing I'd tell future students about Round 4**:
Define a ruthless MVP and lock a recruitment plan before writing code; treat partnerships like features with deadlines.

---

## Commitment

**I commit to**:
- [x] Building the MVP scope above (3-4 features maximum)
- [x] Running a concrete Week 1 validation test
- [x] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: EG  **Date**: 11/4/25

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]


