# Round 4 Reflection: Final Project Decision

**Name**: Alex Chen (sample)
**PennKey**: alexchen
**Date**: November 4, 2025

---

## 1. What I Explored Today

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| MoodMap@Penn | Round 3 (mine) | Highest R3 score (19/30) but recruitment strategy is too vague and I have no concrete partnerships secured. |
| Shadow Course Eval | Instructor idea | Parallel course evaluation system that students rate courses in, can correlate with Penn Course Review data - captive audience makes recruitment trivial. |
| GatherAI | Round 2 Drop | Hidden gem that could be 23-25/30 if pivoted from iMessage to Slack/Discord, but would require learning new APIs in Week 1. |

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [x] V2 detailed analyses (reports/v2-analyses/)
- [x] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [x] Group discussions
- [ ] Other

---

## 2. My Decision

**Project Name**: Shadow Course Eval

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [x] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Instructor idea
- Original round: N/A (new instructor idea)

---

## 3. Why This Decision

**High-level reasoning**:

I'm pivoting from MoodMap@Penn (my Round 3 project) to Shadow Course Eval (instructor idea) because the viability analysis tells a clear story about recruitment risk.

The V2 analysis was brutally honest about MoodMap's biggest weakness: I scored 2/5 on Recruitment Strategy. The analyses kept pointing out that I've been planning this for 3 rounds but never actually contacted an RA or secured a dorm partnership. When group discussion asked "Do you have RA contacts?" and I said "...I'll reach out..." - that was the wake-up call. That's exactly the "documentation not execution" pattern the analyses warned about.

Shadow Course Eval solves my biggest weakness: recruitment is guaranteed because students in this class are a captive audience. The task is simple (rate courses you've taken), there's immediate value (compare to official Penn Course Review), and I can correlate results with existing class catalog data. Technical feasibility is high - it's essentially a survey + data analysis tool. It's less emotionally compelling than mental health mapping, but it's the smart choice for a course project. I can build MoodMap later as a side project when I actually have partnerships secured.

**What convinced me**:
- MoodMap's recruitment weakness (2/5 score) is fatal without concrete partnerships
- Group discussion pushed me to be pragmatic ("get the A, then build MoodMap")
- Shadow Course Eval has captive audience (this class) + can correlate with real Penn Course Review data for interesting analysis

**What concerns me** (and how I'll address it):
- Might not get enough course ratings from classmates → Incentivize with extra credit or make it part of assignment
- Data quality if students just click through → Add validation questions and filter low-effort responses
- Comparison to Penn Course Review might show nothing interesting → Focus on differences and patterns as the research question

---

## 4. What I'm Building

**One-sentence project description**:
Parallel course evaluation system where students rate courses they've taken, with analysis comparing patterns to official Penn Course Review data to identify biases, coverage gaps, or rating inflation.

**MVP Scope** (3-4 core features only):

1. **Course rating interface**: Simple form where students rate courses (difficulty, workload, teaching quality, would recommend)
2. **Penn Course Review integration**: Scrape or manually enter PCR data for courses students rated
3. **Comparison analysis**: Side-by-side comparison showing Shadow Eval ratings vs official PCR ratings
4. **Data visualization dashboard**: Charts showing rating differences, coverage gaps, and interesting patterns

**What I'm explicitly NOT building** (to keep scope realistic):
- Full course catalog integration (just courses this class has taken)
- Professor-specific ratings (course-level only to reduce complexity)
- Historical trends over multiple semesters
- Public-facing interface (internal analysis tool only)
- Mobile app (web-only)
- Anonymous comments (ratings only, no text)

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

- **Where**: NETS 2130 (this class) - classmates as initial users
- **When**: Launch Google Form by Wednesday, announce in class/forum
- **What**: "Rate 3-5 courses you've taken at Penn (difficulty, workload, quality). Takes 5 minutes. I'll share analysis comparing to Penn Course Review."
- **Success metric**: 15+ classmates respond (≥50% response rate), covering 30+ unique courses

**If Week 1 test fails, I will**:
- [x] Recruit from: Post in r/UPenn, CIS department Slack, friend group chats
- [x] Try different recruitment channel: Offer $5 Venmo for completing survey (budget: $50 for 10 responses)
- [x] Simplify the task to: Just 1 course rating instead of 3-5 to reduce friction

---

## 6. Team

**Team members**:

1. Alex Chen (alexchen) - Full-stack Developer + Project Manager
2. Sarah Park (spar) - UX Design + Data Viz _(if she wants to join from R3 team)_

**Team status**:
- [x] Solo (will find teammates later)
- [ ] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Joining an existing team

Note: Starting solo since MVP is simple enough for one person. If Sarah wants to join, great; if not, totally manageable alone.

---

## 7. Reflection

**Most valuable part of Round 4**:
The V2 detailed analyses were eye-opening. The phrase "documentation not execution" hit hard - I realized I've been perfecting MoodMap's proposal for 3 rounds without securing a single partnership. Seeing the instructor's Shadow Course Eval idea made me realize I was ignoring the captive audience right in front of me (this class).

**Biggest surprise**:
I was shocked that I spent 3 rounds obsessing over MoodMap when a simpler, more viable project was staring me in the face: use this class as the initial user base. The instructor's Shadow Course Eval idea has built-in recruitment AND interesting research questions (comparing to Penn Course Review data).

**One thing I'd tell future students about Round 4**:
"I'll reach out to..." means you haven't done it yet, and you probably won't. If you don't have concrete partnerships/contacts NOW, your recruitment strategy scores 1-2/5. Look for captive audiences you ALREADY have access to - classmates, clubs you're in, teams you're on. Sometimes the best project uses the users right in front of you.

---

## Commitment

**I commit to**:
- [x] Building the MVP scope above (4 features maximum)
- [x] Running a concrete Week 1 validation test (email 3 professors Monday 9am)
- [x] Pivoting if Week 1 shows <20% success (0 professors by Wednesday = pivot to survey version)
- [x] Meeting with instructor if I hit major blockers

**Signature**: Alex Chen **Date**: November 4, 2025

---

## Submission

1. Save as `round4/alexchen.md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
