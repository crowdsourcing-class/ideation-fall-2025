# Round 4 Reflection: Final Project Decision

**Name:** Connor Cummings
**PennKey:** connorcc
**Date:** 11/06/2025

---

## 1) What I Explored Today

| Project    | Source     | One-line takeaway                                                                                         |
| ---------- | ---------- | --------------------------------------------------------------------------------------------------------- |
| TerraTruth | Round 3    | Ambition > timeline: over-scoped (PostGIS + AI + many features) and no reliable recruitment route.        |
| GroupMeet  | Instructor | Practical, shippable (22/30) and anchored by a single concrete recruitment lever: professor distribution. |
| WeTrack    | R1 Drop    | Sensible idea (20/30) with good incentives, but still trips on group formation cold-start.                |

**Resources consulted**: ✅ Rubric, ✅ V2 analyses, ✅ Steelman pathways, ✅ Group discussions

---

## 2) My Decision

**Project:** GroupMeet

**Decision type:**

* [ ] STAY (same)
* [ ] STAY (modified)
* [ ] PIVOT
* [x] JOIN an existing team

**If adopting/pivoting:** Instructor idea (Instructor round)

---

## 3) Why This Decision

### The short version

TerraTruth’s V2 (15/30) flagged two non-negotiables: runaway scope and speculative recruitment. WeTrack reduces risk but still depends on self-assembling groups. GroupMeet eliminates both problems: tiny surface area + a binary, testable recruitment wedge via a single professor partnership.

### The longer version

* **TerraTruth**: The V2 was the needed red light. Even a heroic build would underdeliver and likely stall on users. Five weeks isn’t enough to tame both complexity and outreach uncertainty.
* **WeTrack**: Better score and incentives, but still demands social coordination before value appears. That eats the same scarce weeks we need for validation.
* **GroupMeet**: Minimal tech (form → batch match → email) and a crisp go/no-go test tied to one large lecture. It front-loads the core risk (recruitment) into Week 1, which is exactly where it belongs.

**What clinched it**

* TerraTruth’s 15/30 was a reliable “stop.”
* GroupMeet’s MVP can be piloted in ~2 weeks with real students.
* Recruitment = one explicit partnership rather than diffuse social blasts.

**Remaining worries (with mitigations)**

* **Professor says no** → Email 3–4 large-course instructors on Day 1 (CIS 1200, MATH 1400, ECON 0100) to diversify the shot.
* **Low signups / weak matches** → Keep the intake to ~3 high-signal questions and include a concrete study-style preference (e.g., “problem sets” vs “concept review”).

---

## 4) What I’m Building

**One sentence**
A lightweight web tool that groups students in large Penn courses by course, broad availability, and study style—then introduces them by email.

**MVP (only what ships)**

1. **Preference Intake**: Short form (course, weeknights/weekends, study style).
2. **Batch Matcher**: Manual script to cluster submissions into groups of 4–5.
3. **Intro Emailer**: Automatic email with group roster + contact info.
4. **Quality Pulse**: One-question follow-up (1–5 stars) ~5 days later.

**Out of scope (on purpose)**

* Live matching/lobbies
* In-app chat (use existing tools)
* Complex calendars/availability pickers

---

## 5) Week 1 Validation Plan

* **Where**: Email professors for CIS 1200 and CIS 5480 (I TA 5480), plus outreach to ENVS 1000 and CIS 1210 staff.
* **When**: Monday, Nov. 10 @ 9:00 AM.
* **What**: A tight ask for a 2-week pilot to help students form study groups pre-finals, with the live form link.
* **Success bar**: ≥1 professor shares our link **and** we capture signups from ≥15% of that class.

**If it whiffs**

* [x] Switch channel: post directly to the biggest unofficial class GroupMes/Slacks and r/UPenn with a clear CTA.
* [ ] Pivot idea
* [ ] MTurk/paid participants
* [ ] Simplify task
* [ ] Other

---

## 6) Tentative Team

1. Alexander Mehta (amehta26) — Engagement Lead & Backend
2. Brandon Yan (bdonyan) — Frontend / UI
3. Joshua Lee (jlee0902) — Backend / Database
4. Connor Cummings (connorcc) — Backend / Metrics

**Team status:**

* [ ] Same as Round 3
* [x] New team in Round 4
* [ ] Solo
* [ ] Joining an existing team

---

## 7) Reflection

**Most valuable part of Round 4**
The TerraTruth V2 forced us to drop sunk-cost bias and face the real blockers: scope and recruiting.

**Biggest surprise**
How far a simple, well-targeted wedge (professor email) can take you compared to broad social tactics.

**Advice to future students**
Treat “Stop and Pivot” as a rescue rope, not a rebuke—opt for simple + validated over grand + untested.

---

## Commitment

I commit to:

* [x] Building only the MVP above
* [x] Running the Week 1 validation exactly as stated
* [x] Pivoting if Week 1 < 20% success
* [x] Meeting with the instructor if blocked

**Signature:** Connor Cummings
**Date:** 11/6/25

