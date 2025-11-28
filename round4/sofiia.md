# Round 4 Reflection: Final Project Decision

*Name*: Sofiia Kikaleishvili 
*PennKey*: sofiia  
*Date*: 11/11/2025

---

## 1. What I Explored Today

List the projects you seriously considered. Keep it brief.

| Project Name     | Source   | Key Takeaway (1 sentence) |
|------------------|----------|---------------------------|
| MoodMap@Penn     | Round 3  | Strong campus fit with simple tech and clear value; success hinges on securing one captive audience (e.g., a dorm floor or class) in Week 1 to beat the cold start. |
| StreetEats       | Round 3  | Viable if it pivots to Penn-only with pre-seeded content or truck partnerships; otherwise real-time tracking is a cold-start trap. |
| Auralynx         | R2 Drop  | Creative concept exploring human vs. AI perception of voices; dropped for technical overscope and dual-user dependency but still rich in experimental potential. |

Add more rows if needed

*Resources I used*:
- [ ] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [X] V2 detailed analyses (reports/v2-analyses/)
- [ ] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [ ] Group discussions
- [X] Other: Auralynx v3 pre-registration & baseline spec notes

---

## 2. My Decision

*Project Name*: Auralynx

*Decision type*:
- [ ] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [X] PIVOTING to different project
- [ ] JOINING another team's project

*If pivoting or adopting someone's idea*:
- Original author (if applicable): Alexander Budko
- Original round: R2

---

## 3. Why This Decision

*High-level reasoning* (2-3 paragraphs):

I chose Auralynx because the core question—when do humans outperform simple audio heuristics or classical models at reading **prosodic cues**—is both scientifically interesting and buildable in five weeks if we ruthlessly limit scope. The new design fixes the two biggest risks from R2: (1) no two-sided marketplace at launch (we use a **fixed, consented clip library**) and (2) no live ML (we use **frozen baselines** computed offline). The user task is short (6–8 clips/round), repeatable, and intrinsically rewarding via skill badges, streaks, and “beat-the-baseline” moments—so we don’t need cash incentives.

Technically, this is a CRUD web app with audio playback, two well-chosen labels (**Valence: positive/neutral/negative; Confidence: confident/hesitant**), and predeclared baselines: a transparent **prosody rule set** (Tier A) and a tiny **logistic regression** trained on a public corpus (Tier B). That lets us publish a clean “pre-registered” comparison and then, only after we collect enough judgments, optionally calibrate probabilities (not retrain) for analysis. Recruitment is anchored to a captive audience, which is realistic for Week 1.

*What convinced me*:
- Frozen, pre-registered baselines (Tier A heuristics + Tier B logistic regression) keep the science honest and the build simple.
- Two labels that are audibly expressed (valence, confidence) → higher agreement and faster rounds.
- Eliminating speaker uploads at launch removes privacy, pipeline, and cold-start risks.

*What concerns me* (and how I'll address it):
- Ambiguous clips could depress agreement → Pilot with 20–30 users, **prune bottom 15%** agreement clips, and collapse valence to {positive vs non-positive} if α < 0.45.
- Engagement could dip after Day 2 → **Shorten rounds to 6 clips**, surface “Boss Rounds” (hard items worth 2×), and add floor/class leaderboards.

---

## 4. What I'm Building

*One-sentence project description*:
Auralynx is a 90-second audio game where players guess **valence** and **confidence** from short speech clips and see how often they beat frozen, pre-registered baselines.

*MVP Scope* (3-4 core features only):

1. *Round Play & Instant Reveal*: Serve 6–8 standardized clips per round; user guesses valence/confidence and immediately sees “You vs. Baseline vs. Truth.”
2. *Frozen Baseline Outputs*: Display Tier A (prosody rules) and/or Tier B (logistic regression) predictions that were computed offline and stored per clip.
3. *Quality Control & Reliability*: Gold-standard items, duplicate-item checks, and reliability weighting in scoring/leaderboards.
4. *Light Leaderboard & Badges (No Money)*: Weekly leaderboard, streaks, and badges (e.g., “Golden Ear,” “Signal Whisperer”) plus optional “Boss Rounds.”

*What I'm explicitly NOT building* (to keep scope realistic):
- Real-time or multi-model ML inference, speaker identification, or demographic/region prediction.
- Public audio uploads at launch (no two-sided marketplace; clips are pre-recorded with consent).
- Mobile app, push notifications, complex analytics dashboards, or open-data export in MVP.

---

## 5. Week 1 Validation

*The specific test I'll run Week 1*:

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

## 6. *Tentative* Team (Optional, Only If You Already Have An Idea)

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

*Most valuable part of Round 4*:
Converting a “cool idea” into a **pre-registered baseline + fixed clip library** forced scope discipline and gave me a clear scientific story to tell.

*Biggest surprise*:
How far intrinsic incentives (badges, streaks, team leaderboard) go when the **round time is truly <90 seconds**—cash wasn’t necessary.

*One thing I'd tell future students about Round 4*:
Focus on downsizing the scope and be ready to pivot after the first pilot.

---

## Commitment

*I commit to*:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

*Signature: Sofiia Kikaleishvili **Date*: 11/11/2025
