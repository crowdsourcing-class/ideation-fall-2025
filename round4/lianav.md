# Round 4 Reflection: Final Project Decision

**Name**: Liana Veerasamy
**PennKey**: lianav
**Date**: 11/04/25

---

## 1. What I Explored Today
- TripTuner
- AccessWatch
- UrbanExplorer

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| TripTuner  | Round 3 | I learned that while the project had a well-structured platform and solid technical design, it failed due to a fatal incentive mismatch: mexpecting users to create time intensive itineraries for meaningless rewards like badges.  |
| AccessWatch  | R2 Drop| I learned that the concept of a crowdsourced event-discovery map was appealing but undermined by unrealistic recruitment, poor incentive design, and a cold-start “empty platform” problem.  |
| UrbanExplorer | R2 Drop | I learned that this was a thoughtful, technically strong civic-tech project with excellent crowdsourcing design, but it was likely dropped for being too complex, dependent on institutional partners, and slow to demonstrate results within a semester. |

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
- [X] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): My own
- Original round: R3

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):
I chose TripTuner because it strikes a strong balance between creativity,
practicality, and technical feasibility. The idea of using crowdsourcing
to design and rank travel itineraries feels both personally engaging and
broadly relatable—almost everyone has experienced the stress of planning 
a trip and the frustration of conflicting information online. TripTuner 
offers a community-based solution that turns that frustration into 
collaboration, allowing real travelers to share and refine authentic plans together.

Another reason I was drawn to this project is that it combines several
areas I’m interested in: user experience design, incentive structures,
and data aggregation. It’s not just about building a tool—it’s about 
understanding what motivates people to contribute meaningfully and 
how to design systems that surface high-quality information from subjective
inputs. The project provides space to explore technical aspects like ranking 
algorithms and AI moderation while still remaining grounded in a tangible, 
user-facing product.

**What convinced me**:
- The concept directly solves a common, high-friction problem in a way that feels intuitive and useful.
- It offers room to experiment with incentive design, gamification, and community engagement.
- The technical scope (React + Firebase + aggregation logic) is realistic for the timeline
  and can still yield a polished, impactful demo.

**What concerns me** (and how I'll address it):
- Low participation or weak incentives → I’ll mitigate this by seeding initial itineraries myself,
  recruiting through Reddit and travel forums, and experimenting with small tangible rewards or contests.
- High-effort creative task → I’ll reduce friction by breaking the submission process into shorter,
  guided steps and encouraging micro-contributions that build toward complete itineraries.



---

## 4. What I'm Building

**One-sentence project description**:
TripTuner is a crowdsourced travel-planning platform where users submit, 
vote on, and refine short itineraries to create a community-driven 
library of realistic, experience-based trip plans.

**MVP Scope** (3-4 core features only):

1. Itinerary Submission Form: A simple interface where users can submit short 2–3 day itineraries with fields for destination, budget, and activities.
2. Voting & Feedback System: Users can upvote their favorite itineraries and leave short comments on usefulness and realism.
3. Aggregated Ranking Dashboard: Automatically ranks itineraries using a weighted formula that combines votes, feedback sentiment, and completeness.
4. Basic Moderation & Filtering: AI-assisted text moderation and duplicate detection to maintain quality and prevent spam.
   
**What I'm explicitly NOT building** (to keep scope realistic):
- AI summarization or NLP-based itinerary merging
- Complex gamification systems (leaderboards, badges)
- Integration with booking or external travel APIs

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

_Be concrete. Not "social media" but "Post in r/UPenn and 3 class Slacks on Monday at 10am"_

- **Where**: r/solotravel, r/UPenn, and 2 Penn-related Slack channels (Travel Club and Tech & Innovation), maybe sidechat..?
- **When**: monday?
- **What**: Post a short call for participation with a link to a Google Form asking
- users to submit a “2-day budget itinerary for your favorite city” and vote on others
- **Success metric**: At least 10 unique itinerary submissions

**If Week 1 test fails, I will**:
- [X] Pivot to: reducing the task to “recommend 3 activities in X city” instead of full itineraries
- [X] Use MTurk/paid participants
- [X] Try different recruitment channel: just a diff one i already specified
- [X] Simplify the task to: one-line activity or restaurant recommendations per city
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

**Team members**:

1. [Name] ([PennKey]) - [Primary role]
2. [Name] ([PennKey]) - [Primary role]
3. [Name] ([PennKey]) - [Primary role] _(optional)_
4. [Name] ([PennKey]) - [Primary role] _(optional)_

**Team status**:
- [ ] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
[What helped you most in making this decision?]
The most valuable part was being forced to clearly define why I was 
choosing this project instead of just what sounded exciting. 
Writing out the trade-offs and constraints helped me realize how 
easy it is to overbuild early on and how important it is to focus on
one user problem that can actually be validated in a week. 

**Biggest surprise**:
My biggest surprise was maybe how harsh the LLMs were. The critique was really funny lol.

**One thing I'd tell future students about Round 4**:
I would tell students to start early and make sure to think about what project they would choose to do thoughtfully.


---

## Commitment

**I commit to**:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

**Signature**: Liana Veerasamy **Date**: Nov 5

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
