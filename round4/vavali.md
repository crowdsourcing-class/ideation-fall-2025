# Round 4 Reflection: Final Project Decision

**Name**: Vedha Avali
**PennKey**: vavali
**Date**: 11/04/25

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| SoundScape  | Round 3 | The main issue is that this is technically infeasible within the timeframe. |
| Where2Go |   R2 Drop | This project is slightly more feasible, but must be executed as a mobile application which is also difficult. |
| CrowdQA | Instructor | This project allows students to mark when they are confused in class, and seems technically feasible.|

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

We chose CrowdQA because it strikes the best balance between feasibility, impact, and alignment with the course goals. Compared to earlier ideas like SoundScape and Where2Go, this project is far simpler to prototype and deploy, while still demonstrating clear value to both instructors and students. The core task (clicking a “confused” button) is low friction and can be implemented with a straightforward timestamp-count system, allowing us to deliver a working MVP in about two weeks. In contrast, the other ideas required complex data collection (audio scraping, data storage, maps API connection), broader user recruitment, and higher privacy or logistical barriers.

Another major reason for this decision is the strong potential for real adoption. Our target users, students and instructors, already share a well-defined environment (the classroom), making participation easy to encourage through class credit or TA promotion. I myself teach a recitation of around 20 students, so initial deployment at this small scale would be very easy. Afterwards, I would be able to pitch it to the professor whose class I TA for. The immediate feedback loop (a real-time confusion heatmap) provides tangible benefits: instructors can adjust their teaching pace, while students feel heard without fear of embarrassment. This combination of simplicity, clear value, and built-in user base made CrowdQA the most viable and sustainable choice for our team.

We did consider trade-offs. The main limitation is the need for professor or TA cooperation to test the tool during an actual lecture(when trying to scale up past the initial users), but this is hopefully manageable since our team includes TAs for large introductory courses. Given the clear technical path, attainable scope, and meaningful educational benefit, CrowdQA emerged as the most realistic and impactful project to pursue.

**What convinced me**:
- Simplicity and clarity of the idea
- Built-in user base of students and professors with clear incentives
- Immediate, visible impact

**What concerns me** (and how I'll address it):
- Professor/TA buy-in → Some instructors may believe this adds unnecessary complication and may hesitate to add new tools at this point in the semester. To resolve this we can start by testing in a recitation section to show general feasibility before introducing it to professors.
- Low Engagement from Students → Some might forget to click or not see value. We’ll keep the interface ultra-simple (one-click, mobile-friendly) and show aggregated class results to encourage participation.

---

## 4. What I'm Building

**One-sentence project description**:
A lightweight web app where students can anonymously mark confusing moments during a lecture, allowing instructors to see a real-time heatmap of confusion levels across the class timeline.
**MVP Scope** (3-4 core features only):

1. **Confusion Button**: Students click a single button when they feel lost; the system records the timestamp.
2. **Timeline Visualization:**: Instructor dashboard displays a heatmap or line graph showing peaks of confusion across the lecture.
3. **Session Management:**: Simple login or session code to link each set of responses to a specific class lecture.
4. **[Feature 4 name - OPTIONAL]**: [1-sentence description]

**What I'm explicitly NOT building** (to keep scope realistic):
- No per-student analytics or identity tracking (anonymous by design).
- No complex feedback/comment threads — just a single click signal.
- No real-time video/audio integration with lectures in the MVP phase.

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: Poll for interest in CIS 1210 Recitation. Poll for TA/professor interest by posting message in CIS 1210 Slack
- **When**: Wednesday at 10:15 AM
- **What**: [What you'll post/ask/test]
- **Success metric**: [How will you know if it worked? Be specific with numbers]

**If Week 1 test fails, I will**:
- [x] Pivot to: reframing as a post-lecture feedback tracker rather than a live tool.
- [ ] Use MTurk/paid participants
- [ ] Try different recruitment channel: [specify]
- [ ] Simplify the task to: [easier version]
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. Vedha Avali (vavali) - TBD
2. Leha Choppara (lchoppara) - TBD
3. Emily Kang (emkang) - TBD
4. Amber He (heamber) - TBD
5. Anika Basu (basua) - TBD
6. Mingni Dong (mdong126) - TBD

**Team status**:
- [ ] Same team from Round 3
- [x] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
The most helpful part was getting clear, structured feedback that forced us to think about feasibility and user recruitment early on.
**Biggest surprise**:

We initially thought SoundScape or Where2Go would be more exciting, but the class discussions revealed how difficult real-world deployment and data collection would be.

**One thing I'd tell future students about Round 4**:
Focus on validation and simplicity, and do not feel discouraged when receiving feedback

---

## Commitment

**I commit to**:
- [x] Building the MVP scope above (3-4 features maximum)
- [x] Running a concrete Week 1 validation test
- [x] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: Vedha Avali **Date**: 11/04/2025

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
