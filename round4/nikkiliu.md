# Round 4 Reflection: Final Project Decision

**Name**: Nikki Liu
**PennKey**: nikkiliu
**Date**: 11/05/2025

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| GroupMeet | Instructor | It's a straightforward and feasible project that depends on professor partnership and creates a good audience for Penn students. |
| AgriAid  | Round 1 | A key strength is the project’s clear, achievable design that directly supports a meaningful humanitarian need, while its main weakness is the risk of inconsistent volunteer labeling that could limit data quality without strong quality-control mechanisms. |
| ProfPulse  | Instructor | The project is practical to build and genuinely useful for users, but its web-scraping component may introduce both legal risks and technical challenges.
 |

_Add more rows if needed_

**Resources I used**:
- [✓] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [ ] V2 detailed analyses (reports/v2-analyses/)
- [ ] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [✓] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: GroupMeet

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [✓] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Alexander Mehta, amehta26
- Original round: Instructor idea

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

_Explain your thought process. What made you choose this project? What were the key factors? What trade-offs did you consider?_

I ultimately chose the study-group matching project over AgriAid because it aligns much more closely with what I can realistically build, test, and deploy within the course timeline. 
AgriAid, while meaningful and exciting, carries a heavy burden: sourcing large volumes of satellite imagery, designing a crowdsourcing interface that works at scale, 
implementing quality-control mechanisms, and validating labels against vegetation indices. It’s a technically ambitious pipeline with many points of failure — 
data ingestion, labeling workflow, consensus aggregation, and mapping — and most importantly, it requires hundreds of external volunteers to produce anything useful. 
In contrast, the study-group matcher is entirely self-contained: the data is easy to collect, the workflows are simple, and I can test the full system with real Penn students immediately. 
It lets me spend my time actually building and refining features, not wrestling with data infrastructure.

GroupMe (the study-group matcher) also provides a clearer and more direct path to demonstrating course concepts like incentive design, quality-control, and aggregation. 
Instead of relying on remote volunteers or specialized domain knowledge, I can run a controlled pilot with students who share context, schedules, and goals — 
meaning every part of the system is easier to measure, iterate, and improve. The project is also inherently “sticky”: students have a built-in motivation to participate 
because they want study partners, so adoption is much more reliable than asking strangers to label crop-stress images. Overall, GroupMe offers a focused, testable, 
and high-impact environment where I can build something polished and genuinely useful to my community, without the massive overhead of a global satellite-labeling initiative.


**What convinced me**:
- Building GroupMe is far more feasible within the course timeline because the data, interface, and workflow are simple and fully under my control.
- The project directly solves a real, recurring problem for Penn students, meaning participation and feedback will be easy to obtain for testing and iteration.
- It offers a clean, self-contained way to demonstrate course concepts (quality control, incentives, aggregation) without relying on a massive external volunteer base or complex data pipelines.

**What concerns me** (and how I'll address it):
- The matching algorithm may produce uneven or low-quality groups → I’ll mitigate this by collecting a small number of highly informative preferences and using follow-up ratings to adjust or refine the grouping rules.
- Students might not complete the form or respond to emails → I’ll mitigate this by keeping the form extremely short, offering clear value (“find real study partners”), and sending a single reminder nudge before running the matching script.

---

## 4. What I'm Building

**One-sentence project description**:
GroupMeet is a simple web tool that pairs Penn students into compatible study groups based on their course, availability, and study preferences, and collects quick feedback to refine future matching.

**MVP Scope** (3-4 core features only):

1. Class & Availability Form: A lightweight input form where students choose their course, indicate general availability, and specify one preference such as group size or study style.
2. Matching Algorithm: A backend script that forms groups by aligning students with overlapping courses and time windows using clear, rule-based logic.
3. Match Results Page: A clean, single-page interface where each student can view their assigned group along with names and contact information.
4. **[Feature 4 name - OPTIONAL]**: [1-sentence description]

**What I'm explicitly NOT building** (to keep scope realistic):
- Advanced optimization or any machine-learning–driven matching system.
- Built-in chat, real-time notification features, or synced calendar tools.
- Support for multi-course matching, multi-semester tracking, or ongoing dynamic rematching.

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: [Exact channels/locations]
- **When**: [Specific day and time]
- **What**: [What you'll post/ask/test]
- **Success metric**: [How will you know if it worked? Be specific with numbers]

**If Week 1 test fails, I will**:
- [ ] Pivot to: [alternative approach]
- [ ] Use MTurk/paid participants
- [ ] Try different recruitment channel: [specify]
- [ ] Simplify the task to: [easier version]
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. Brandon Yan (branyan) - Frontend Developer
2. Alexander Mehta (amehta26) - Backend Developer
3. Joshua Lee (jlee0902) - Recruitment Coordinator
4. Nikki Liu (nikkiliu) - Frontend Developer

**Team status**:
- [ ] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [✓] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
Realizing how important feasibility and testability are - comparing ideas forced me to see which project I could actually build, pilot, and evaluate within the course timeline.

**Biggest surprise**:
I didn’t expect how quickly the “scope reality check” would eliminate ideas I initially loved; once I mapped out data needs and user recruitment, the simpler project clearly became stronger.

**One thing I'd tell future students about Round 4**:
on’t pick the project that sounds the flashiest — pick the one you can meaningfully test with real users in two weeks, because that constraint ends up driving almost every good decision.

---

## Commitment

**I commit to**:
- [✓] Building the MVP scope above (3-4 features maximum)
- [✓] Running a concrete Week 1 validation test
- [✓] Pivoting if Week 1 shows <20% success
- [√] Meeting with instructor if I hit major blockers

**Signature**: Nikki Liu **Date**: 11/05/2025

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
