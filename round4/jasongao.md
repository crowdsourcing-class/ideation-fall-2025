# Round 4 Reflection: Final Project Decision

*Name*: Jason Gao
*PennKey*: jasongao  
*Date*: 11/05/2025

---

## 1. What I Explored Today

List the projects you seriously considered. Keep it brief.

| Project Name     | Source   | Key Takeaway (1 sentence) |
|------------------|----------|---------------------------|
| Kinnect          | Round 3  | Fitness gamification with team challenges and live activity maps; technically straightforward but would need sustained engagement and wearable API integrations that could complicate the MVP. |
| TerraTruth       | Round 3  | Satellite imagery analysis for humanitarian causes with reputation systems; there's a compelling mission-driven angle but depends on partner NGOs and complex image pipelines that are risky for Week 1. |
| Auralynx         | R2 Drop  | Human-vs-AI voice perception experiment with frozen baselines; simplified from original R2 pitch by removing speaker uploads and using pre-recorded clips, making it instantly playable. |

Add more rows if needed

*Resources I used*:
- [X] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
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

What drew me to Auralynx is how it bridges a meaningful gap in voice AI research—comparing human perception against computational models—while staying technically feasible for a five-week sprint. 

I chose Auralynx because I think it bridges a clear gap in voice AI research while staying properly scoped for five weeks. The original R2 proposal was ambitious but had structural issues: requiring both speaker uploads *and* guesser participation created a chicken-and-egg problem. The redesigned approach would get rid of both bottlenecks by pre-recording a curated clip library (with full consent) and computing all baseline predictions **offline before launch**. 

From a technical standpoint, the build is surprisingly straightforward: a web app that serves audio files, collects two simple labels per clip (**Valence** and **Confidence**). The baselines themselves are  simle and transparent; Tier A would use hand-coded prosody features (pitch variance, speech rate, pauses), while Tier B is a lightweight logistic regression trained on a public emotion corpus. By freezing these models before data collection starts, we avoid the statistical pitfalls of post-hoc model tuning and create a clean "pre-registered experiment" that could actually produce publishable results.

*What convinced me*:
- The **perception-gap research angle** is unique. There are existing projects like Mozilla Common Voice collect transcriptions, but they don't compare AI vs. human judgments of *emotion* or *confidence*.
- Simplified labels (just valence + confidence) are acoustically grounded and should give us decent inter-rater agreement
- Using a fixed clip library avoids all the hard problems with this idea: real-time uploads, privacy consent flows, moderation pipelines, and cold-start bootstrapping

*What concerns me* (and how I'll address it):
- **Low inter-rater agreement** if clips are too ambiguous → Run a 20-person pilot in Week 0, compute Fleiss' kappa per clip and remove the bottom 15%; if the overall agreement is still weak then we can try to collapse valence into binary (positive vs. non-positive)
- **Drop-off after initial curiosity** → Keep rounds ultra-short (6 clips max), introduce "Boss Rounds" with harder clips worth double points, and create floor/class-based leaderboards to add social accountability.

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
Realizing that simplifying the technical architecture (fixed clips + offline baselines) actually **strengthens** the research validity rather than weakening it—pre-registration is a feature, not a limitation.

*Biggest surprise*:
How much the "two-sided marketplace" framing from R2 was masking the real value proposition. Removing speaker uploads entirely makes this feel more like a polished game and less like a data-collection chore.

*One thing I'd tell future students about Round 4*:
Complexity ≠ engineering rigor. Simplicity is the true mark of something being engineered well.

---

## Commitment

*I commit to*:
- [X] Building the MVP scope above (3-4 features maximum)
- [X] Running a concrete Week 1 validation test
- [X] Pivoting if Week 1 shows <20% success
- [X] Meeting with instructor if I hit major blockers

*Signature*: Jason Gao **Date*: 11/5/2025
