# Round 4 Reflection: Final Project Decision

**Name**: Emily Kang
**PennKey**: emkang
**Date**: 11/4/25

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| PitchPeer  | Round 3 (my idea) | Good incentives but ambitious implementation overreach, realistic user base|
| CrowdQA  | Instructor| 24/30 Highest Instructor Score and concrete user sourcing plans|
| Kinnect  | Round 3 | Best incentive design, clear user value, tech overreach, saturated market |

_Add more rows if needed_

**Resources I used**:
- [X] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X] V2 detailed analyses (reports/v2-analyses/)
- [X] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [X] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

**Project Name**: CrowdQA

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [X] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): N/A
- Original round: Instructor

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

I decided to continue with CrowdQA because it strikes the best balance between feasibility, user need, and potential for real classroom impact. The idea solves a clear, recurring problem: during lectures, many students get lost but hesitate to speak up. At the same time, instructors often don’t realize when confusion spikes. CrowdQA bridges this communication gap with a simple, anonymous, real-time feedback mechanism that benefits both sides.

Among my other ideas, this one stood out because it’s technically straightforward yet has strong potential for real adoption. The core functionality—a single “confused” button and timestamp tracking—can be built and tested quickly. There’s a clear path to getting users (students in a class) and a natural incentive for instructors to try it, since it directly improves their teaching feedback. The tradeoff is needing professor cooperation, but that’s manageable with good framing (“helps you teach better in real time”).

**What convinced me**:
- Solves a real, well-defined classroom problem
- Technically lightweight and testable in a week
- Easy to recruit users via existing class setups

**What concerns me** (and how I'll address it):
- Professor buy-in → I’ll start with a professor I already know or one open to teaching innovations
- Low student participation → I’ll make the interface frictionless (single-click, no login) and frame it as anonymous feedback to encourage use

---

## 4. What I'm Building

**One-sentence project description**:
A lightweight web app where students anonymously mark confusing moments during lecture, generating a real-time “confusion heatmap” for instructors.

**MVP Scope** (3-4 core features only):

1. **Confusion Button**: A simple “I’m confused” button that logs a timestamp when clicked.
2. **Lecture Timeline**: A visual timeline displaying when confusion spikes occur.
3. **Instructor View**: A basic dashboard for professors to see aggregated confusion data in real time.
4. **Anonymous Tracking**: Basic session IDs to track participation without identifying users.

**What I'm explicitly NOT building** (to keep scope realistic):
- No complex login or user accounts
- No AI or text-based explanations of confusion
- No full integration with learning management systems (e.g., Canvas)

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

I’ll test CrowdQA in a live recitation/lecture by having students use the app to mark moments of confusion, while the instructor views the real-time heatmap to see if it reflects difficult parts of the lecture.

- **Where**: In one live recitation/lecture (with instructor permission)
- **When**: Thursday at 9:00 AM (or whenever the recitation/lecture runs)
- **What**: I’ll share a short link and QR code at the start of class so students can open the app and click “confused” whenever something isn’t clear. The instructor will view the real-time confusion heatmap during the lecture.
- **Success metric**: At least 10+ students participate and the confusion timeline shows clear spikes during complex parts of the lecture (as confirmed by the instructor afterward).

**If Week 1 test fails, I will**:
- [X] Pivot to: collecting confusion data via post-lecture survey instead of live tracking
- [ ] Use MTurk/paid participants
- [X] Try different recruitment channel: smaller discussion section or a different class
- [X] Simplify the task to: a single Google Form button-click test
- [] Other: [specify]

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
- [X] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
Getting clear on feasibility and validation helped the most. I realized that even a strong idea needs a concrete, testable plan to move forward. Thinking through how I’d actually test CrowdQA in a real class made the project feel much more tangible and achievable.

**Biggest surprise**:
I was surprised by how much value a very simple prototype could deliver. Initially, I thought I’d need complex analytics or login systems, but after scoping it down, I saw that just a “confused” button and real-time timeline could already generate meaningful insights for instructors.

**One thing I'd tell future students about Round 4**:
Focus on what’s realistically buildable and testable in a week. The best project isn’t necessarily the flashiest—it’s the one you can actually validate quickly and learn from.

---

## Commitment

**I commit to**:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

**Signature**: Emily Kang **Date**: 11/4/25

---

## Submission

1. Save as `round4/[your-pennkey].md`
2. Submit via pull request
3. Deadline: [Instructor will specify]
