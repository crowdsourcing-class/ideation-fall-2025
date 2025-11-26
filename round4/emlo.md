# Round 4 Reflection: Final Project Decision

**Name**: Emily Lo
**PennKey**: emlo
**Date**: 11/4/2025

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| Kinnect  | Round 3 | Good incentives, a lot of technical limitations as is |
| Where2Go  | R2 Drop | Useful, but lacks some incentive |
| GroupMeet  | Instructor | In scope for project and definitely useful for students |

_Add more rows if needed_

**Resources I used**:
- [X] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X] V2 detailed analyses (reports/v2-analyses/)
- [X] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [X] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: Kinnect

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [X] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Emily Lo, emlo
- Original round: [R3]

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

I chose Kinnect because of its strong incentive design. The task (logging daily fitness activity) naturally aligns with what users already want to do (stay fit), and the team accountability creates powerful social pressure that actually works. 
Kinnect taps into intrinsic motivation amplified by extrinsic social dynamics (don't let your team down). 
The fitness tracking space is proven - apps like Strava and Peloton demonstrate that people will engage with these systems - but Kinnect's focus on small team challenges fills a gap that existing apps don't address well: the accountability of competing with friends rather than just against them.

However, the original proposal is overscoped with mobile development, 5 API integrations, real-time sync, and ML predictions. I'm choosing Kinnect specifically because I believe that I can execute the core social mechanic with 20% of the technical complexity by pivoting to web-only manual entry. 
The magic of Kinnect isn't the technology - it's the social dynamics of team challenges and daily check-ins. By stripping away the technical overreach and focusing on those core mechanics, I can actually prove the concept works in 5 weeks. 

**What convinced me**:
- Proven incentive structure
- Achievable with major descope
- Personal connection

**What concerns me** (and how I'll address it):
- Getting to critical mass → I'll recruit from my own networks first. If that fails by Day 3, I'll pivot to partnering with one large lecture course for extra credit.
- Manual entry creating friction/fake data → I'll use statistical outlier detection to flag suspicious entries. Social pressure within teams will discourage cheating since you'll be letting down real friends.

---

## 4. What I'm Building

**One-sentence project description**:
A web app where Penn students form teams and compete in weekly challenges with daily manual check-ins and leaderboards to create social accountability for fitness goals.

**MVP Scope** (3-4 core features only):
1. **Team Formation & Management**: Users create or join teams, see their teammates' names and current stats, with maximum 6 people per team
2. **Daily Step Logging**: Simple web form where users enter their step count for the day with timestamp to prevent backdating and optional photo upload for verification
3. **Live Team Leaderboard**: Real-time rankings showing each team's average daily steps with a progress bar, updated automatically when anyone logs steps
4. **Weekly Challenge System**: Time-boxed weekly challenges (Monday-Sunday) with clear start/end, automatic reset each week, and winner announcement with optional $25 gift card prize for winning team

**What I'm explicitly NOT building** (to keep scope realistic):
- Mobile App
- API Integrations
- ML
- Payment Integration

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: Direct messages to 10 friends asking them to recruit their own friends, message NETS 2130 class
- **When**: Monday at 10am
- **What**: "Hey! I'm building a fitness accountability app for my class where you form teams with friends and compete in weekly step challenges. You just need to log your steps daily. Let me know if you are interested!"
- **Success metric**: minimum 30 positive responses by Friday

**If Week 1 test fails, I will**:
- [ ] Pivot to: [alternative approach]
- [ ] Use MTurk/paid participants
- [X] Try different recruitment channel: Utilize other networks like reaching out to professors of large introduction CIS classes
- [ ] Simplify the task to: [easier version]
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. Caroline Cummings (carfc) - Developer
2. Alex Oh (alexoh) - Developer
3. Shivi Jain (shivij) - Developer
4. [Name] ([PennKey]) - [Primary role] _(optional)_

**Team status**:
- [X] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
I liked the Steelman analysis as well as seeing what other groups were thinking of. 

**Biggest surprise**:
I didn't expect all the ideas to be so diverse. 

**One thing I'd tell future students about Round 4**:
Be open about other ideas and see if you can use certain parts in your own project. 

---

## Commitment

**I commit to**:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

**Signature**: ____Emily Lo_____________________ **Date**: ______11/4/2025_______

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
