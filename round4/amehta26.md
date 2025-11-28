# Round 4 Reflection: Final Project Decision

**Name**: Alexander Mehta
**PennKey**: amehta26
**Date**: 11/05/2025
---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| TerraTruth  | Round 3 | The feedback from Claude was informative, I learned that the project was too ambitious. |
| GroupMeet  |  Instructor | A very simple, viable idea (22/30) with a concrete recruitment plan (professor partnership) that creates a captive audience. |
| WeTrack  |  R1 Drop | A solid idea (20/30) with a strong incentive model (peer accountability), but it has a similar "cold-start" problem to TerraTruth for forming groups. |

_Add more rows if needed_

**Resources I used**:
- [ X ] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [ X ] V2 detailed analyses (reports/v2-analyses/)
- [ X ] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [ X ] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: GroupMeet

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ X ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Instructor
- Original round: Instructor idea

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

_Explain your thought process. What made you choose this project? What were the key factors? What trade-offs did you consider?_

The decision to pivot away from TerraTruth was driven directly by the V2 analysis. The 15/30 score was a clear "Stop and Pivot" signal. The analysis correctly identified our two biggest, unsolvable problems: massive scope (PostGIS, AI pre-filtering, 10+ features) and a "fatal flaw" in recruitment (relying on vague social media campaigns and unsecured partnerships). Sticking with TerraTruth would have meant struggling for 5 weeks to build a fraction of the system, only to fail at recruitment.

I also briefly considered WeTrack, which had a much better score (20/30) and a strong incentive model. However, it suffers from a similar, though smaller, cold-start problem: the platform is only useful after accountability groups are formed. I felt that our team would spend too much time trying to coordinate friend groups rather than building and testing the system.

GroupMeet (22/30) solves both of our primary problems. First, the technical scope is drastically simpler: a basic form, a matching script, and a follow-up email. Second, and most importantly, it replaces a vague recruitment "hope" with a single, concrete validation test: partnering with a professor of a large-lecture course. This provides an immediate captive audience, which is the single biggest risk factor for any crowdsourcing project. The risk is binary and testable in Week 1, which is a much better position to be in.

**What convinced me**:
- The V2 analysis of TerraTruth (15/30) was a necessary and accurate assessment of our project's fatal flaws.
- GroupMeet has a simple, achievable MVP (a "one-class pilot") that is buildable in 2 weeks.
- The recruitment strategy is a single, testable partnership that provides a "captive audience," which is far more viable than our original plan.

**What concerns me** (and how I'll address it):
- Concern 1: The entire project hinges on getting a professor to agree to this in Week 1. → Mitigation: We will email 3-4 professors of large intro courses (CIS 1200, MATH 1400, ECON 0100) simultaneously on Day 1 to maximize our chances.
- Concern 2: Students might not fill out the form, or the matches might be low-quality. → Mitigation: We will make the preference form extremely short (3 questions) and include specific study preferences (e.g., "problem sets vs. concept review") to improve match quality.

---

## 4. What I'm Building

**One-sentence project description**:
A web app that matches students in large Penn courses into study groups based on their class, availability, and study preferences.

**MVP Scope** (3-4 core features only):

1. **Student Preference Form**: A simple web form where students select their course (from a pre-set list), their general availability (e.g., weeknights, weekends), and one key study preference.
2. **One-Time Matching Script**: A backend script that we run manually to process all form submissions and generate groups of 4-5 students.
3. **Email Distribution**: The script will automatically email the matched students to introduce them (e.g., "You've been matched! Here are the emails of your group members...").
4. **Group Quality Rating**: A follow-up email sent 5 days later with a link to a 1-question form: "Please rate your study group experience (1-5 stars)."

**What I'm explicitly NOT building** (to keep scope realistic):
- Real-time matching or a user "lobby"
- An integrated chat system (they can use GroupMe or Discord)
- A complex availability calendar (just simple time-block preferences)

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: Emailing the professors of CIS 1200, and CIS 5480 (Which I TA for), can also reach out to Profs/TAs of ENVS 1000 and CIS 1210
- **When**: Monday, Nov. 10th at 9:00 AM.
- **What**: A concise email explaining the 2-week pilot project to help their students form study groups for the upcoming final exams. We will include a link to the (already built) preference form.
- **Success metric**: At least one professor agrees to send our announcement and link to their class list or post it on the class forum (e.g., Ed, Canvas) and we receive signups from at least 15% of the class.

**If Week 1 test fails, I will**:
- [ ] Pivot to: [alternative approach]
- [ ] Use MTurk/paid participants
- [X ] Try different recruitment channel: Bypass professors. We will post the form directly in the largest unofficial class GroupMes, Slacks, and on the r/UPenn subreddit with a clear call to action.
- [ ] Simplify the task to: []
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. [Alexander Mehta] ([amehta26]) - Engagement Lead and Backend
2. [Brandon Yan] ([bdonyan]) - Frontend / UI
3. [Joshua Lee] ([jlee0902]) - Backend / Database
4. [Name] ([PennKey]) - [Primary role] _(optional)_

**Team status**:
- [ ] Same team from Round 3
- [ X ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
Reading the brutally honest V2 analysis for TerraTruth. It forced our team to confront the scope and recruitment issues that we were subconsciously ignoring. The 15/30 score was the clear signal we needed to pivot.

**Biggest surprise**:
How much simpler, yet still effective, the instructor's project ideas were. It's a great reminder that "simple but working" with real users is far better than a complex, impressive-sounding project that fails.

**One thing I'd tell future students about Round 4**:
Don't be stuck with your first idea. The "Stop and Pivot" feedback isn't a personal failure it's a lifeline to save you from 5 weeks of misery and a bad grade. Take the advice, pick something simple, and focus on recruitment.

---

## Commitment

**I commit to**:
- [ X ] Building the MVP scope above (3-4 features maximum)
- [ X ] Running a concrete Week 1 validation test
- [ X ] Pivoting if Week 1 shows <20% success
- [ X ] Meeting with instructor if I hit major blockers

**Signature**: Alexander Mehta
 **Date**: 11/5/25

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]


Notes with Professor:

Banking vs Active Learning.

For professors, forming group projects is a pain and helping with course ratings is also big.

GroupMeet could be the best place for any group. You can have student led groups or instructor started groups. 

Could add class lists from Professors
- Prof Lumbroso has a tool to extract class list from
https://github.com/jlumbroso/penn-classlist-scraper 
courses.at.upenn.edu

Ask instructors in project based classes
- What would you like to measure
- What would you like to evaluate

Convince Instructors that this is the easiest tool. 
- This will enable the fly wheel.
- Make it easy to export a csv for tracking whether students are using.
- Email Professor Lumbroso for literature about peer feedback