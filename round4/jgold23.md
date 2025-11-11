# Round 4 Reflection: Final Project Decision

**Name**: Jackson Gold  
**PennKey**: jgold23  
**Date**: 11/4/25

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| StreetEats | Round 3 | Strong technical bones and QC; success hinges on solving the cold-start with truck-owner partnerships and a ruthlessly small MVP. |
| PitchPeer | R1 | Compelling concept but a two-sided marketplace with many heavy features—would likely ship empty without drastic scope cuts. |
| SoundScape | R3 | Novel, but overscoped with weak incentives—would require a pivot to validate in course timeline. |

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [x] V2 detailed analyses (reports/v2-analyses/)
- [x] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [x] Group discussions
- [ ] Other: —

---

## 2. My Decision

**Project Name**: StreetEats — real-time, crowd-verified food-truck status around Penn/University City

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [x] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

---

## 3. Why This Decision

**High-level reasoning (2–3 paragraphs):**

StreetEats has the clearest path to a working MVP within two weeks if we cut scope and front-load partnerships. The tech and QC design are already strong; the existential risks are non-technical—recruitment, incentives, and timeline. Those are addressable with concrete outreach and a small paid pilot.  

To de-risk, I’m centering Week 0–2 on: (1) **5 owner commitments**, (2) **manual data seeding**, and (3) a **paid pilot** to seed early updates. Anything beyond the core loop (map + pins + basic updates + simple majority voting) is deferred until that loop is live with real data.

**What convinced me**:
- Concrete, prescriptive next steps and checkpoints (5 partnerships; 2-week core-loop checkpoint).
- Clear mitigation for incentives via micro-payments + owner promos.
- Strong QC can be simplified to **majority voting** for MVP, avoiding over-engineering.

**What concerns me** (and how I'll address it):
- **Cold-start / empty map** → Secure **5+ owner partnerships** and **seed data manually** before marketing.
- **Incentive mismatch** → Run a **paid pilot ($0.25/verified update)** Weeks 2–3 and pair with owner raffle perks.

---

## 4. What I'm Building

**One-sentence project description**  
A lightweight web app showing **live, crowd-verified** food-truck status around Penn, starting with owner-partner trucks and **simple majority-voted** updates.

**MVP Scope (3–4 core features only):**
1. **Map + Pins**: Google-map view of seeded trucks around University City.
2. **Basic Status Update Flow**: One-tap “here / closed / moved,” auto-location, optional photo.
3. **Simple Majority Voting**: Publish when ≥3 matching reports; owner-verified overrides.
4. **Admin/Manual Seeding (Optional)**: Team tools to pre-populate and correct truck entries in Week 1.

**What I'm explicitly NOT building** (to keep scope realistic):
- Push notifications, favorites, or a full owner portal (email/manual override is enough).
- Reputation scoring, advanced confidence metrics, or outlier dashboards for MVP.
- Anything mobile-native; web-only MVP.

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

- **Where**:  
  - On-site/email outreach to **10–12 University City trucks** (aim: ≥5 commitments).  
  - **Penn FB class groups** + NETS 2130 Slack (#general, #projects) + two dining GroupMes.
- **When**:  
  - Owner outreach **Mon–Wed (11/10–11/12)** mid-day;  
  - Student recruiting posts **Mon 11/10 10:00am**, reminder **Wed 11/12 6:00pm**.
- **What**:  
  - Prototype with **pre-seeded pins (5–8 trucks)** → users submit a single status; team manually validates.  
  - Announce **paid pilot ($0.25/verified update)** to early contributors.
- **Success metric**:  
  - **Owners**: ≥5 partnership commitments;  
  - **Product**: working **submit → publish** core loop by end of Week 1;  
  - **Crowd**: ≥30 unique users, ≥60 submissions, ≥70% agreement on published statuses.

**If Week 1 test fails, I will**:
- [x] Pivot to: **Food-Truck Directory** with team-maintained updates (ship completeness over crowdsourcing)
- [x] Use MTurk/paid participants to seed early updates
- [x] Try different recruitment channel: table near 34th & Walnut with owner-posted QR codes
- [ ] Simplify the task to: one-tap check-ins only
- [ ] Other: —

---

## 6. **Tentative** Team (Optional)

**Team members**:
1. bradenj — Full-stack / Maps  
2. rolings — Backend / Infra  
3. jgold23 — PM / Outreach & Incentives  
4. egotian — Frontend  
5. chettyk — Data & QA

**Team status**:
- [x] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**  
The rubric and V2 analyses made the problems concrete (partnerships, ruthless MVP, checkpoints) and turned them into a clear plan.

**Biggest surprise**  
The bottleneck isn’t tech—**it’s recruitment and incentives**; otherwise-strong ideas fail there.

**One thing I'd tell future students about Round 4**  
Pick the idea you can **seed next week** (owners, manual data, small paid pilot) and let features wait.

---

## Commitment

**I commit to**:
- [x] Building the MVP scope above (3–4 features maximum)
- [x] Running a concrete Week 1 validation test
- [x] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: _Jackson Gold_  **Date**: 11/4/25

---

## Submission

1. Save as `round4/jgold23.md`  
2. Submit via pull request  
3. Deadline: [Instructor will specify]
