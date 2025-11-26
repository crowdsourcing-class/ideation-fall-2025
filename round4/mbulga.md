# Round 4 Reflection: Final Project Decision

**Name**: [Martina Bulgarelli]
**PennKey**: [mbulga]
**Date**: [11/04/2025]

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| Kinnect | Round 3 | A scalable, crowdsourced fitness platform that turns personal activity into a social, gamified team challenge—but success depends on solving early engagement and verified-data integrity to avoid a cold-start and cheating issues. |
| PitchPeer | Round 2 | A lightweight crowdsourced platform that helps founders rapidly validate startup ideas with structured feedback and optional interviews, but sustained value depends on attracting a diverse, reliable crowd and preventing low-effort responses.|
| AgriAid | Round 2| A volunteer-powered satellite-image labeling platform that strengthens climate-driven crop stress detection, though success hinges on maintaining high-quality annotations from a non-expert crowd. |

_Add more rows if needed_

**Resources I used**:
- [ ] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X] V2 detailed analyses (reports/v2-analyses/)
- [ ] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [X] Group discussions
- [ ] Other: [specify]

---

## 2. My Decision

*Project Name*: Auralynx

**Decision type**:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [X] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): Alexander Budko/abudko
- Original round: R2

---

## 3. Why This Decision

**High-level reasoning** (2-3 paragraphs):

I chose Auralynx because it hits the sweet spot between mission and practicality. 
I care about speech tech that treats people fairly—especially around accents and expression—and this project gives me a direct way to measure where machines and humans diverge on the exact same audio. 
The design is scientifically clean (human vs. frozen baseline vs. self-report on a fixed prompt), the experience is playful (“beat the baseline”), and the deliverable is tangible: a small but useful perception-gap dataset plus a clear story I can stand behind.
I also weighed scope and risk across ideas. Compared with larger, two-sided or data-hungry concepts, Auralynx is buildable in five weeks without spinning up complex ML pipelines or a creator marketplace. Freezing baselines, using a consented clip library, and keeping rounds short reduces technical uncertainty and lets me focus on data quality, agreement, and analysis. 
The trade-off is narrowing the ambition—fewer traits, simpler models, no live retraining—but that constraint makes the results defensible and the pilot realistic.

**What convinced me**:
- A tight, preregistered design (fixed prompts + frozen baselines) that I can execute and defend.
- A 90-second gameplay loop that drives engagement without cash incentives.
- Clear downstream value for fairness research: actionable perception-gap metrics, not just a demo.

**What concerns me** (and how I'll address it):
- [Ambiguous clips could depress inter-rater agreemen] → Run a fast pilot, prune the lowest-agreement ~15%, and simplify labels (e.g., collapse valence) if κ falls below target.
- [Engagement may fade after day one] → Keep rounds to 6 clips, add “Boss Rounds,” seed a captive audience (one class/club) for active leaderboards, and surface “beat-the-baseline” moments prominently.

---

## 4. What I'm Building

**One-sentence project description**:
[Auralynx is a fast-paced (≈90s) audio challenge where players estimate a speaker’s valence and confidence from short voice clips and try to outperform pre-registered baseline models.]

**MVP Scope** (3-4 core features only):

1. **[Quick Rounds with Instant Feedback]**: [Players hear 6–8 standardized clips per round, make valence and confidence judgments, and instantly see: Player vs. Baseline vs. Ground Truth.]
2. **[Pre-computed Baseline Benchmarks]**: [Tier A (rule-based prosody) and Tier B (logistic regression) predictions are shown using outputs generated offline and stored per clip.]
3. **[Built-in Data Quality and Reliability]**: [Includes gold-standard clips, repeat-item checks, and reliability-weighted scoring to ensure clean data and fair comparisons.]
4. **[Lightweight Leaderboards & Gamification]**: [Weekly rankings, streak rewards, and badges, with occasional higher-difficulty.]

**What I'm explicitly NOT building** (to keep scope realistic):
- Live ML inference, speaker ID, or demographic inference
- User audio submissions (no open recording at an event)
- Native mobile app, push notifications, advanced analytics, or open-data export

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

- *Where*:  
  1) Ed Posts   
  2)  Slackx for clubs and group chats
- *What*:  
  “Can you beat a simple AI at hearing emotion and confidence in voice? 90 seconds, 6 clips. Get your **Golden Ear** badge and see your score vs. baseline.” (one QR, instant start)
- *Success metric*:  
  **≥60 unique users in 48 hours**, **≥120 total rounds** (median ≥2), **gold-item pass rate ≥70%**, and **≥10 ‘Boss Round’ completions**.

*If Week 1 test fails, I will*:
- [X] Pivot to: valence collapsed to **{positive vs non-positive}** and 6-clip rounds
- [ ] Use MTurk/paid participants
- [X] Try different recruitment channel: 2-minute **in-class demo** + QR in one large lecture (e.g., NETS/CIS), plus **Locust Walk** IG story reposts from partner orgs
- [X] Simplify the task to: **Confidence-only** (binary) for all 6 clips in a round
- [X] Other: Replace bottom-quartile agreement clips within 24 hours; switch the default displayed baseline (Tier A ↔ Tier B)
---

## 6. **Tentative** Team (Optional, Only If You Already Have An Idea)

At this stage, you are not expected to have formed teams, however if you already have an idea of who you intend to work with, you may indicate it here.

*Team members*:

1. Alexander Budko (abudko) - PM, full-stack & analytics,
2. Sofia Kikaleishvili ( ) - UX, recording coordinator, participant ops
3. Martina Bulgarelli ( ) - Data & QC (gold items, agreement metrics)
4. Anton Bakhurov ( ) - Audio processing & baseline features (Tier A/Tier B prep)
5. Jason Gao ( ) - full-stack, audio processing & baseline features help

*Team status*:
- [ ] Same team from Round 3
- [X] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
Moving to pre-registered baselines and a fixed dataset brought necessary discipline.
Now the project has a tight and compelling scientific narrative.

**Biggest surprise**:
True 90-second rounds + simple rewards provide enough motivation without cash.

**One thing I'd tell future students about Round 4**:
Shrink your scope early—and commit to pivoting if the pilot data tells you to.

---

## Commitment

**I commit to**:
*I commit to*:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

**Signature**: Martina Bulgarelli **Date**: 11/04/2025
