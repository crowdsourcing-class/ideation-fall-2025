# Round 4 Reflection: Final Project Decision

**Name**: Eric Lee
**PennKey**: ericclee
**Date**: 11/4/25

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| urbanExplorer  | Round 3 | I learned that this project can be a centralized platform for Penn activities |
| auraLynx  | R2 Drop | I learned that this project can provide a valuable asset if it collects audio for crowdsourcing purposes |
| streetEats  | Round 3 | I learned that street food such as food trucks are not readily available for reviews and hours, and student crowdsourcing can address this problem. |

**Resources I used**:
- [X] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X] V2 detailed analyses (reports/v2-analyses/)
- [X] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [ ] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: urbanExplorer

**Decision type**:
- [X] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): [Name/PennKey]
- Original round: [R1 / R2 / R3 / Instructor idea]

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

_Explain your thought process. What made you choose this project? What were the key factors? What trade-offs did you consider?_

I chose Urban Explorer because it captures the core idea of crowdsourcing in a familiar environment — Penn’s campus. The project solves a real need for students who often miss out on activities simply because they are spread across too many channels. I realized that focusing the scope on the Penn community makes the project much more viable, since it provides a built-in user base and high event density.

A centralized event map also gives value to student organizations. They can post events once instead of across multiple platforms, while students can easily find gatherings relevant to their interests. The data collected (e.g., attendance, timing, and event type) could even help clubs or event planners optimize scheduling and promotion strategies in the long run.

**What convinced me**:
- Crowdsourcing works best with dense, localized communities like Penn.
- Technically feasible web app using Next.js + PostgreSQL + Mapbox.
- Clear MVP loop (post → verify → display on map).

**What concerns me** (and how I'll address it):
- Cold-start problem → Partner with 5–10 Penn clubs to seed 50+ initial events.
- No captive audience → Introduce communities within the app (e.g., “CS events,” “Music,” “Clubs”) for personalization.

---

## 4. What I'm Building

**One-sentence project description**:
A crowdsourced, interactive web app that helps Penn students discover and share campus events on a live map.

**MVP Scope** (3-4 core features only):

1. **Event Posting**: Users can post an event with title, location, description, and time.
2. **Interactive map**: Displays events as pins that can be filtered by category or date.
3. **Verification System**: Events must be verified by 2+ users before being publicly visible.
4. **Voting/Flagging System**: Users can upvote or flag events for quality control.

**What I'm explicitly NOT building** (to keep scope realistic):
- Push notifications or email alerts.
- ML duplicate detection.
- Advanced trust/reputation system.

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: Penn Clubs Slack channels, Discord servers, and GroupMe chats (CIS, Wharton Council, Penn Spark, and club boards).
- **When**: Wednesday, Nov 12, 10am.
- **What**: Share a prototype link and ask students to submit one real event they’re attending this week.
- **Success metric**: At least **20 unique event submissions** and **50 unique map views** within 48 hours.

**If Week 1 test fails, I will**:
- [X] Pivot to: a curated version where the team manually collects and uploads events.
- [ ] Use MTurk/paid participants
- [X] Try different recruitment channel: Penn subreddit and class Slack
- [ ] Simplify the task to: pre-filled event templates

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. Eric Lee (ericclee) - [Primary role]
2. Katherine Yue (kyue) - [Primary role]
3. Andrew Park (andrewpp) - [Primary role] _(optional)_

**Team status**:
- [ ] Same team from Round 3
- [X] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
Reading the detailed V2 viability analysis helped me see how critical scope and recruitment strategies are for success. It showed that narrowing the target to Penn’s campus drastically improves the odds of achieving density and meaningful user participation.

**Biggest surprise**:
The project’s biggest weakness wasn’t technical—it was the two-sided marketplace challenge. I realized that content seeding is a product design problem, not just an engineering one.

**One thing I'd tell future students about Round 4**:
Don’t just think about what you can build—think about who will use it on Day 1 and why. Without a clear first audience, even  tech won’t matter.

---

## Commitment

**I commit to**:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

**Signature**: ____Eric Lee_____________________ **Date**: ___11/4/2025__________

---