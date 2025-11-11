# Round 4 Reflection: Final Project Decision

**Name**: Brandon Yan
**PennKey**: branyan
**Date**: 11/05/2025

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| GroupMeet | Instructor | It's a promising idea for Penn student collaboration, but it's success hinges on professor collaborations and logistics with matching. |
| ProfPulse  | Instructor | The project is feasible to build with useful utility for the user, but the web scraping aspect could bring legal and also technical hurdles. |
| CrowdQA  | Instructor| Easy to implement but could potentially cause distractions. |

_Add more rows if needed_

**Resources I used**:
- [X] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X] V2 detailed analyses (reports/v2-analyses/)
- [ ] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [X] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: [Your final choice]

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [X] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Instructor
- Original round: Instructor Idea

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

After reflecting on my Round 3 project (TerraTruth) and reviewing its V2 analysis, I realized that the project’s ambition, combining geospatial pipelines, AI pre-filtering, and humanitarian crowdsourcing, made it extremely difficult to execute within a five-week course. Our rubric score (15 / 30) and faculty feedback highlighted two critical weaknesses: an oversized technical scope and an untested recruitment model. Even though I was proud of TerraTruth’s design depth and quality-control rigor, I learned firsthand how over-engineering early can block validation. We spent too long architecting complex systems before confirming we could attract users.

That experience shaped my decision to pivot to GroupMeet, an instructor-proposed project with clear technical boundaries and a directly testable crowd loop. Instead of struggling with GIS and volunteer networks, I wanted a project where every component ties directly to user action: students fill out a form, get matched, and rate the outcome. This design aligns perfectly with the NETS 2130 rubric—simple, feasible, and easy to validate. It also leverages my previous organizational experience at Penn (Spark, CIS TA networks, course Slack channels) to solve the recruitment problem that held TerraTruth back.

Ultimately, I chose GroupMeet because it lets me apply what I learned from TerraTruth: scope ruthlessly, validate early, and prove the model before layering complexity. The pivot isn’t giving up on ambition-it’s channeling it into something that can actually succeed.

**What convinced me**:
- The technical scope is realistic: a form-based matching system can be built in under two weeks.
- It directly fixes TerraTruth’s biggest issue (recruitment) by targeting a captive audience—Penn students in shared courses.
- The feedback loop is measurable and fully crowdsourced.

**What concerns me** (and how I'll address it):
- Dependence on professor or TA partnerships → I’ll seed initial users through Penn Spark Discord/Slack channels and CIS 5450 TA promortion instead of relying on official partnerships.
- Sustaining engagement after the first match → I’ll add a short “rate-your-group” form and optional weekly re-matching to generate continuous participation and fresh data.

---

## 4. What I'm Building

**One-sentence project description**:
GroupMeet is a lightweight web platform that matches Penn students into study groups based on class enrollment, availability, and learning preferences, then gathers quick feedback to improve future matches.

**MVP Scope** (3-4 core features only):

1. **Class & Availability Form**: Simple submission form where students select their course (e.g., CIS 1200), preferred study times, and group size preference.
2. **Matching Algorithm**: Backend script that automatically groups students based on overlapping classes and time slots using straightforward logic.
3. **Match Results Page**: Each user receives their assigned group with names and contact info displayed in a clean, single-page dashboard.
4. **[Feedback Form - OPTIONAL]**: After a study session, users can submit a one-minute rating of group usefulness or participation quality, feeding into future iterations.

**What I'm explicitly NOT building** (to keep scope realistic):
- Complex matching optimization or machine-learning recommendation systems.
- In-app chat, real-time notifications, or integrated calendars.
- Multi-course or cross-semester matching.

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: r/UPenn subreddit (main post and comment bump); 
Penn Spark internal Slack (#general and #project-discussion); CIS 5450 Announcements channel on Canvas (with instructor/TA permission)
- **When**: Monday, November 10th at 10:00 AM for Reddit and Slack posts; CIS 5450 announcement scheduled for Monday afternoon after class
- **What**: I’ll post a short recruitment message linking a 1-minute Google Form prototype that collects class name, availability, and study preferences for testing GroupMeet, a study group matcher built by Penn students.
- **Success metric**: 20+ unique form submissions within 48 hours; At least 8 participants successfully matched into groups; 5+ responses to short feedback follow-up form

**If Week 1 test fails, I will**:
- [ ] Pivot to: [alternative approach]
- [ ] Use MTurk/paid participants
- [X] Try different recruitment channel: Ask friends to promote to Penn Labs, Hack4Impact, different classes across disciplines
- [ ] Simplify the task to: [easier version]
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. Brandon Yan (branyan) - Frontend Developer
2. Alexander Mehta (amehta26) - Backend Developer
3. Joshua Lee (jlee0902) - Recruitment Coordinator
4. [Name] ([PennKey]) - [Primary role] _(optional)_

**Team status**:
- [X] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
Realizing how important it is to define a realistically small, testable core loop before writing any code. The scoping exercise helped us strip GroupMeet down to just three core actions-submitting class info, matching, and giving feedback-instead of overengineering features we couldn’t validate.

**Biggest surprise**:
How much faster everything becomes when recruitment is part of the design, not an afterthought. Compared to TerraTruth, focusing on channels I personally control (Penn Spark Slack, CIS 5450, r/UPenn) made the validation plan feel immediately achievable.

**One thing I'd tell future students about Round 4**:
Treat this round as your reality check. If you can’t clearly say who’s using your app next week and how you’ll measure it, the idea is still too big. Keep only what you can test in 7 days, not what sounds exciting.

---

## Commitment

**I commit to**:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: ____Brandon Yan____ **Date**: ___11/05/2025___

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
