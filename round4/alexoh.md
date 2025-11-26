# Round 4 Reflection: Final Project Decision

**Name**: Alexandra Oh
**PennKey**: alexoh
**Date**: 11/04/25

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| Kinnect  | Round 3 | It has great incentive but very little feasibility with all the APIs and mobile app features|
| MoodMap  | Round 3 | Needs an engaged and committed mass of students to participate, but has great potential to inform us on student wellness trends. |
| Pitch Peer  | Round 3 | It would fill a true need on campus, but the current iteration is not feasible nor convenient for users. |

_Add more rows if needed_

**Resources I used**:
- [X ] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X ] V2 detailed analyses (reports/v2-analyses/)
- [X ] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [X ] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: Kinnect 

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [X ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): [Name/PennKey]
- Original round: [R1 / R2 / R3 / Instructor idea]

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

_Explain your thought process. What made you choose this project? What were the key factors? What trade-offs did you consider?_

The detailed V2 feedback made it clear that our team has an **A+ idea with an F scope**. The core crowdsourcing principles—the "Waze model" for fitness—are incredibly strong, scoring 5/5 on Incentive Design and 4/5 on Crowdsourcing Viability. Users want to be motivated, and using social accountability is the right way to do it. \

However, the feedback was equally clear that our original technical plan was impossible, scoring 1/5 on Technical Feasibility and 1/5 on Scope. We were trying to build a 6-month, venture-backed startup in 5 weeks. The decision to stay with Kinnect is based on the feedback's explicit, viable path forward. By cutting scope (no mobile app, no APIs, no real-time map) and focusing on a web-only, manual-logging MVP, we can save the "A+" idea. We can still solve the core problem (fitness motivation) for a small, local group (Penn students) and prove our crowdsourcing model works. I considered how useful the platform still is without the fancy features, and I believe the core loop (log activity -> see leaderboard -> feel motivated) remains intact. 

**What convinced me**:
- [Key reason 1] The 5/5 score on Incentive Design. The feedback confirmed our core loop (intrinsic motivation + gamification) is "textbook" and "ideal crowdsourcing design." 
- [Key reason 2] The clear, actionable descoped MVP provided in the feedback. It gives us a concrete blueprint: "Web app (React) + Firebase Auth + Manual logging + Simple leaderboards." 
- [Key reason 3] The "Penn Challenge" recruitment strategy was validated as smart. The idea was right even if the scale was wrong, which is not a hard fix.

**What concerns me** (and how I'll address it):
- [Concern 1] Recruitment Failure (Cold Start): This was rated a "HIGH" risk. We will need to get 30-40 committed users at the start of the project. We will also seed the leaderboard with our own team's activity for 1 week pre-launch. 
- [Concern 2] Fraud/Data Quality Collapse: Without APIs, cheating is a real risk so we will have to think of QC mechanisms to hold users accountable. 

---

## 4. What I'm Building

**One-sentence project description**:
A web-based fitness platform for the Penn community that uses team leaderboards and personal streaks to motivate daily activity through manual logging. 

**MVP Scope** (3-4 core features only):

1. **User Auth & Manual Logging**: Users can sign up for the "Penn Challenge" and manually log daily fitness activities (type, duration/distance). 
2. **Team Assignment**: Users can join a pre-set team (e.g., "Team Penn") or be assigned to one. 
3. **Simple Leaderboard**: A basic web page showing a sorted list of teams and top users by total weekly points. 
4. **Personal Streaks**: The system tracks and displays a user's consecutive days of logged activity. 

**What I'm explicitly NOT building** (to keep scope realistic):
- no React Native mobile app (web-only) 
- nO 3rd-party API integrations (HealthKit, Fitbit, Strava) 
- no Real-time Mapbox visualization 
- no ML-based fraud detection (using simple rules instead) 

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: A Google Form link posted in penn channels, groupchats, and email lists (e.g., the NETS 2130 class Slack, a large dorm GroupMe, and the Penn Running Club listserv). 
- **When**: Monday, Week 1, at 10:00 AM. 
- **What**: Post: "Sign up for the 4-week 'Penn Fitness Challenge' - a simple web app to log workouts and compete on a team leaderboard. We need 30 people to launch. Sign up here: [Google Form Link]" 
- **Success metric**: **30 unique Penn student signups** on the Google Form by Friday, Week 1. 

**If Week 1 test fails, I will**:
- [X ] Pivot to: collaborative goal instead of competitive (can all users hit 100 miles this week?)
- [ ] Use MTurk/paid participants
- [X ] Try different recruitment channel: personally message different student groups that we are not involved in
- [ ] Simplify the task to: [easier version]
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**: Potentially my same team from round 3? Shivi, Caroline, Emily if they are on board

**Team status**:
- [ X] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
The rubric-based V2 analysis. It was brutal but fair and it clearly separated good (the idea, 5/5) from bad (the scope, 1/5). Seeing the "Predicted Outcome" scenarios side-by-side made the decision to descope obvious. 

**Biggest surprise**:
How catastrophically overscoped our project was (9.5 weeks of professional work estimated!). The 1/5 technical feasibility score was a huge wake-up call that "cool features" (APIs, ML) are traps in a 5-week project. 

**One thing I'd tell future students about Round 4**:
Trust the feedback, especially on scope. Build less, finish more, and have a tangible way to get real users on it. 

---

## Commitment

**I commit to**:
- [X ] Building the MVP scope above (3-4 features maximum)
- [X ] Running a concrete Week 1 validation test
- [ X] Pivoting if Week 1 shows <20% success
- [ X] Meeting with instructor if I hit major blockers

**Signature**: _____Alexandra Oh____________________ **Date**: __11/04/2025___________
