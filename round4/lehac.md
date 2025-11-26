# Round 4 Reflection: Final Project Decision

**Name**: Leha Choppara
**PennKey**: lehac
**Date**: 11/4/2025

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| Soundscape  | Round 3 | Creative, strong differentiation but very large and unfeasible scope. |
| Where2Go  | R2 Drop | Immediately useful on campus with clear features, but needs better incentives. |
| CrowdQA | Instructor | High feasibility and obvious incentives for both users and professors. |

_Add more rows if needed_

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [x] V2 detailed analyses (reports/v2-analyses/)
- [x] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [x] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: CrowdQA

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [x] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Professor Lumbroso
- Original round: Instructor idea

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

_Explain your thought process. What made you choose this project? What were the key factors? What trade-offs did you consider?_

I chose CrowdQA because it’s immediately useful to Penn students (the first audience I can actually reach this month) and because the core benefit is obvious to both sides of the classroom. In large lectures (and even smaller talks/recitations), instructors struggle to read the room; as a CIS TA, I run into the same issue every week. A one-tap “I’m confused” signal aggregated into a live/post-hoc timeline would help me target reteaching and structure office hours. That clear value proposition plus a captive, reachable user base makes CrowdQA the strongest fit.

Feasibility within five weeks was the next filter, and CrowdQA scores high: a thin client, a simple timestamped event stream, and a heatmap view are enough for a compelling MVP. I also weighed user incentives and retention; because participation can be nudged by in-class announcements and light incentives (participation credit, extra credit, or seeing their signal reflected in real adjustments), I believe usage can be both bootstrapped and sustained. Compared to Soundscape, the Round 3 idea I worked on, CrowdQA has far fewer moving parts, fewer dependencies (no audio capture, privacy pipeline, or coverage bootstrapping), and stronger week-one validation odds.

**What convinced me**:
- Clear usefulness in my own context (as a CIS TA, I would deploy this immediately for recitation).
- High feasibility: a shippable, end-to-end MVP is realistic in Week 1–2.
- Built-in incentives: low-friction task and visible impact.

**What concerns me** (and how I'll address it):
- Real-time data pipeline/visualization must be fast and clean → Use a lean tech stack, and focus on useability and minimum features without slowing things down uneccesarily (e.g. no animations or extra features).
- Quality control and trolling risk → Apply per-session rate limits/cooldowns, basic anomaly detection (burst/outlier filters).

---

## 4. What I'm Building

**One-sentence project description**:
A tiny web tool where students click “confused” during lecture and the instructor gets a real-time + post-hoc timeline heatmap of confusion spikes to target reteaching.

**MVP Scope** (3-4 core features only):

1. **One-tap Confused Button**: logs lecture_id, user_hash, and timestamp; no text entry to minimize friction.
2. **Real-time Heatmap Timeline**: Aggregated counts per 5-second bin; live view for instructor, anonymized students.
3. **Post-Lecture Report**: Top confusion time periods, with slide indices (inputted manually for MVP, but integrated with PowerPoint end goal), CSV export for instructors.

**What I'm explicitly NOT building** (to keep scope realistic):
- Student accounts
- Anonymous Q&A
- A mobile app (this will be a web app)

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: The CIS 1200 recitation that I TA for, the chapter meeting of the club I run, and a CIS 1200 lecture if the professors approve. 
- **When**: Wednesday afternoon, Saturday afternoon and Friday morning respectively
- **What**: I will ask everyone in the room to open the web app and to click the button whenever they are confused and/or would have liked more clarification on a topic.
- **Success metric**: ≥50 unique participants; ≥3 distinct spikes that align with known tricky slides.

**If Week 1 test fails, I will**:
- [ ] Pivot to: [alternative approach]
- [ ] Use MTurk/paid participants
- [x] Try different recruitment channel: Ensure that instructions are clear so that the website can be used without prior knowledge, and outreach to professors of subjects that I am not in, in and out of Penn.
- [ ] Simplify the task to: [easier version]
- [ ] Other: [specify]

---

## 6. Reflection

**Most valuable part of Round 4**:
The rubric was really helpful. It helped me identify what exactly worked and what didn't across every project, using a common framework.

**Biggest surprise**:
How a simple crowdsourcing project with fewer features but a clear outcome can have more of an incentive. I found that it was easier to consider how I would use the Octalysis to drive engagement for smaller scoped  projects than for ones with larger scope (e.g. the one I worked on originally, SoundScape, which had multiple outputs, such as an interactive map, clickable sounds, ratings, tagging, etc. compared to the one I would like to work on now.)

**One thing I'd tell future students about Round 4**:
Pick the idea whose recruitment and MVP you can validate this week, not the one with the fanciest features.

---

## Commitment

**I commit to**:
- [x] Building the MVP scope above (3-4 features maximum)
- [x] Running a concrete Week 1 validation test
- [x] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: Leha Choppara **Date**: 11/4/2025

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
