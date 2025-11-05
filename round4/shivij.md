# Round 4 Reflection: Final Project Decision
**Name**: Shivi Jain  
**PennKey**: shivij  
**Date**: 11/4/25

---

## 1. What I Explored Today
_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| StreetEats | Round 3 | Strong stakeholder alignment but requires sustained engagement and owner partnerships to overcome cold-start problem. |
| CrowdQA - Lecture Confusion Tracker | Instructor / New | Extremely simple MVP with captive audience and immediate value, but success depends entirely on professor buy-in. |
| MenuMatcher - Dining Hall Ratings | Instructor / New | Built-in user base with daily use case, but menu scraping may add technical complexity. |

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [x] V2 detailed analyses (reports/v2-analyses/)
- [x] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [ ] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision
**Project Name**: CrowdQA - Lecture Confusion Tracker

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [x] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Instructor idea
- Original round: Round 4 / Instructor suggested

---

## 3. Why This Decision
**High-level reasoning** (2-3 paragraphs):

After carefully analyzing both StreetEats (my Round 3 project) and the instructor-suggested alternatives, I decided to pivot to CrowdQA because it solves the most critical challenges I identified in StreetEats: cold-start problems, sustained engagement, and unclear Week 1 validation paths. CrowdQA has a captive audience (students already in class), immediate value for both students and instructors, and the simplest possible crowd task (a single button click). The MVP can be built in days rather than weeks, allowing me to focus on validation and iteration rather than complex technical infrastructure.

While I was passionate about StreetEats, the reality is that it requires significant groundwork—owner partnerships, initial data seeding, and critical mass of users—before it can demonstrate value. In contrast, CrowdQA can be tested in a single lecture with 20-30 students and immediately show whether the concept works. The feedback loop is instant: if students don't click the button or professors don't find the heatmap useful, I know within 50 minutes. This rapid validation aligns perfectly with the course timeline and reduces risk dramatically.

MenuMatcher was also appealing due to its daily use case and built-in user base, but the menu scraping technical challenge and the need to aggregate data across multiple meals before showing value made it less suitable for rapid iteration. CrowdQA's simplicity—both technically and conceptually—gives me the best chance of building something that works and can be validated quickly.

**What convinced me**:
- **Captive audience with zero recruitment friction**: Students are already in the classroom, no need to convince them to download an app or visit a location
- **Instant feedback loop**: Can test the entire system in a single 50-minute lecture and know immediately if it works
- **Minimal technical complexity**: Simple timestamp + counter system means I can focus on user experience and validation rather than fighting technical issues
- **Clear value proposition for both sides**: Students get better instruction, professors get actionable feedback they can't get from traditional methods

**What concerns me** (and how I'll address it):
- **Professor buy-in is make-or-break** → I'll reach out to 3-4 professors this week with a 2-minute demo video showing how it helps teaching; if all decline, I'll pivot to MenuMatcher as backup
- **Students may not engage if it's not required** → I'll propose it as optional extra credit (1-2 points) or as a required participation component; worst case, I'll run it in a GSR study session with friends
- **Privacy concerns about identifying "confused" students** → All data is aggregated and anonymous; the heatmap only shows timestamps and counts, never individual identities

---

## 4. What I'm Building
**One-sentence project description**:
A simple web app where students anonymously click a "confused" button during lectures, creating a real-time heatmap that shows instructors exactly when the class struggled to follow along.

**MVP Scope** (3-4 core features only):
1. **Confusion button**: One-click anonymous submission that timestamps the moment a student is confused (no login required, just enter a class code)
2. **Real-time heatmap visualization**: Instructor dashboard showing a timeline of the lecture with spikes indicating when multiple students marked confusion
3. **Post-lecture summary**: Simple report showing the 3-5 most confusing moments with timestamps, so professors can review those sections
4. **Optional comment field**: Students can add a brief note explaining what confused them (optional, to keep friction minimal)

**What I'm explicitly NOT building** (to keep scope realistic):
- User accounts or authentication (just session-based, enter class code)
- Integration with Canvas or other LMS systems
- Video recording or playback features
- Detailed analytics or historical tracking across multiple lectures
- Mobile app (web-only for MVP)
- AI-powered analysis or recommendations

---

## 5. Week 1 Validation
**The specific test I'll run Week 1**:
- **Where**: CIS 5210 lecture (backup: CIS 5210 office hours or study group with 8-10 classmates)
- **When**: Tuesday 11/12/25 during regular class time (or Wednesday 11/13 office hours if professor declines)
- **What**: 
  1. Send professor an email by Friday 11/8 with 2-min demo video and request to test in one lecture
  2. If approved: Display class code at start of lecture, remind students 2-3 times to use it when confused
  3. If not approved: Run it in office hours or study group as a "practice lecture" scenario
  4. After 50 minutes, show the instructor/group the heatmap and ask for feedback
- **Success metric**: 
  - **Minimum viable success**: At least 30% of attendees (6+ people in study group, 15+ in class) click the button at least once
  - **Strong success**: At least 50% engagement + professor/participants say "I would use this again"
  - **Data quality check**: Confusion spikes correlate with objectively difficult topics (professor confirms "yes, that was the hard part")

**If Week 1 test fails, I will**:
- [x] Pivot to: MenuMatcher (dining hall ratings) - has guaranteed users and simpler validation path
- [ ] Use MTurk/paid participants
- [x] Try different recruitment channel: Test in multiple small study groups (5-6 people each) across different classes to see if it's a lecture-specific issue
- [x] Simplify the task to: Add gamification (show how many others are confused in real-time) to increase engagement
- [ ] Other: [specify]

---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)
**Team members**:
1. Shivi Jain (shivij)
2. Alex Oh (alexoh)

**Team status**:
- [X ] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team


---

## 7. Reflection
**Most valuable part of Round 4**:
The rubric scoring exercise forced me to confront the cold-start and engagement issues in StreetEats that I had been avoiding. Seeing CrowdQA score higher on feasibility metrics made me realize that "passion for the idea" matters less than "can I validate this in Week 1."

**Biggest surprise**:
How much simpler the "best" projects are compared to what I initially thought was impressive. CrowdQA is literally just a button and a timeline, but that simplicity is exactly what makes it testable and valuable. I was overcomplicating things.

**One thing I'd tell future students about Round 4**:
Choose the project you can test in Week 1, not the one that sounds coolest on paper. If you can't figure out a concrete validation test with real users in the first week, you're going to struggle for the entire project. Start simple, validate fast, then expand if it works.

---

## Commitment
**I commit to**:
- [x] Building the MVP scope above (3-4 features maximum)
- [x] Running a concrete Week 1 validation test
- [x] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: Shivi Jain  
**Date**: 11/4/25

---

## Submission
1. Save as `round4/shivij.md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
