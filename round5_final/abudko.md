
# Final Project Proposal: Auralynx

**Team Name**: Auralynx  
**Submission Date**: 11/17/2025  
**GitHub Organization**: [Link](https://github.com/Aurallynx)

---

## Team Information

### Team Members

| Name                    | PennKey | Primary Role(s)                 | Secondary Skills                           |
|-------------------------|---------|---------------------------------|--------------------------------------------|
| Alexander Budko         | abudko  | Full-Stack Dev + DevOps        | K8s, React, Python, Docker                 |
| Anton Bakhurov          | abakh   | Aggregation + Analysis         | Statistics, ML, Design                     |
| Sofiia Kikaleishvilli   | sofiia  | QC Module + Experiment Design  | Math/Econ, Statistical Modeling, Analysis  |
| Jason Gao               | jasongao| Data Pipeline + Visualizations | CS, Web Dev, React/TypeScript, APIs        |
| Martina Bulgarelli      | mbulga  | Recruitment + UX Copy          | Finance, Communication, Outreach, Figma    |

### Team Skills Inventory

**Skills we have:**
- DevOps: Alex (abudko)
- Full-Stack Development: Alex (abudko)
- Python + Data Handling: Alex (abudko), Anton (abakh), Sofiia (sofiia)
- Data Analysis + Basic ML: Anton (abakh), Sofiia (sofiia)
- Experimental / Survey Design: Anton (abakh), Sofiia (sofiia)
- Statistical & Economic Analysis: Sofiia (sofiia)
- Frontend Engineering (React/TypeScript): Jason (jasongao)
- Backend/API Engineering: Jason (jasongao), Alex (abudko)
- Data Pipeline + Visualization (dashboards/plots): Jason (jasongao), Anton (abakh)
- Canva / Visual Design: Anton (abakh)
- Finance + Metrics Storytelling: Martina (mbulga)
- Recruitment & Outreach: Martina (mbulga)
- UX Copy & Communication: Martina (mbulga)
- Project Management + Coordination: Alex & Anton

**Skills we need to learn/acquire:**
- **Data Aggregation Design** – Primary: Anton  
  Define robust schemas for storing/combining multiple guesses per clip.
- **Cursor-based Development Workflow** – Primary: Alex  
  Use AI-assisted tooling to keep velocity high with a small dev team.
- **Lightweight Audio Feature Extraction** – Primary: Jason  
  Implement simple acoustic feature extraction so we can compare crowd guesses with basic audio features (e.g., pitch range, speaking rate).

**External resources we might need:**
- Cursor – Status: Acquired, Cost: Free  
- [Optional] MTurk / Prolific account – Status: TBD, Cost: TBD  
- Class mailing list / Discord for recruitment – Status: Available, Cost: Free  

### Team Availability for TA Meetings

**Week of 11/17/2025:**

_List all time slots when the ENTIRE team can meet (Eastern Time):_

- Monday: Not available  
- Tuesday: 2:00 PM – 5:00 PM  
- Wednesday: Not available  
- Thursday: 2:00 PM – 5:00 PM  
- Friday: Not available  

**Preferred meeting duration**: 30 min  
**Meeting format preference**: Zoom  
**Primary contact for scheduling**: Sofiia Kikaleishvilli – sofiia@sas.upenn.edu  

---

## Project Overview

### Project Connection to Round 4

**Round 4 Decision**: STAYING  

**Original idea from**: Round 1/2/3 author – Alexander Budko (abudko)

**How the idea evolved**:  
The original idea was a more complex crowdsourcing platform with data augmentation and ML models layered on top of voice clips. Over Rounds 2–4, the idea shifted toward a simpler, tightly scoped aggregation tool focused on one core question: *How are speakers actually perceived by a crowd?* In this final proposal, Auralynx becomes a social voice guessing game where students record short voice memos and other students guess accent, age range, and tone. The core crowdsourcing and aggregation pieces remain, but the interface and scope are streamlined for easier deployment and more reliable evaluation.

### Problem Statement

Students who are learning languages or working on their speaking skills rarely get fun, low-pressure feedback on how they actually sound to others. Traditional speaking practice is either awkward (formal presentations, grading) or isolating (talking to an app alone), so students don’t build confidence, awareness of their accent/tone, or listening skills. We’re solving this by turning voice practice into a social guessing game that gives students instant, crowd-sourced feedback on how their accent, age, and tone are perceived.

### One-Sentence Pitch

A social voice game where students record short voice memos and classmates guess their accent, age, and tone—turning speaking practice and bias awareness into a fun daily challenge.

### Target Users

**End Users:**
- University students practicing English or other languages  
- Students in public speaking / communication classes  
- Anyone curious about how their accent and tone are perceived by peers  

**Crowd Workers:**
- Class volunteers from this course and related courses  
- Friends/peers recruited via class channels or social media  
- (Backup) Paid crowd workers via MTurk/Prolific if needed  

**Scale (for demo):**
- ~25–40 unique speakers (end users)  
- ~15–30 crowd workers  
- ~10–20 guesses per clip (~300–800 total annotations)

### Project Type

- [ ] Human computation algorithm  
- [x] Social science experiment with the crowd  
- [x] Tool for crowdsourcing (requesters or workers)  
- [ ] Business idea using crowdsourcing  
- [ ] Other: [ ]

---

## System Architecture

### Flow Diagram

**Flow diagram location**: `docs/flow-diagram.pdf` (to be added)

The flow diagram will show:

- Where/when the crowd touches the data:
  - After a clip is uploaded, before feedback is shown to the speaker.
- Quality control module:
  - Separate QC step filtering low-effort/inconsistent guesses.
- Aggregation module:
  - Combines filtered guesses into final accent/age/tone distributions.
- Data flow:
  - Speaker → Audio Upload API → Storage & Task Queue → Crowd Task UI → QC Module → Aggregation → Feedback UI → Analytics dashboard.
- Before crowd involvement:
  - Clip recording, basic validation (length, file type), anonymization.
- After crowd contribution:
  - Aggregated labels, perception summaries, bias metrics.

**If not created yet – components in words:**

1. **Speaker client (web UI / app)** → records & uploads audio + minimal metadata.  
2. **Backend ingestion service** → stores audio & creates annotation tasks.  
3. **Crowd task interface** → presents anonymized clips; collects accent/age/tone guesses + attention checks.  
4. **Quality Control module** → filters/flags low-quality or inconsistent worker responses.  
5. **Aggregation module** → computes final distributions and summary statistics per clip.  
6. **Feedback & analytics UI** → shows speakers their “perception profile” and global patterns to the team.

### Major System Components

| Component               | Description                                                          | Points | Owner(s)     | Dependencies                   |
|-------------------------|----------------------------------------------------------------------|--------|--------------|--------------------------------|
| Speaker Web UI          | Interface to record/upload clips and view feedback                  | 3      | Alex, Jason  | Backend API, aggregation       |
| Crowd Task UI           | Page where workers listen to clips and submit guesses               | 3      | Alex, Jason  | Backend API, task creation     |
| Backend API & Storage   | Handles clip upload, task assignment, and metadata storage          | 3      | Alex, Jason  | DB schema, infra               |
| QC Module               | Filters low-quality responses using attention checks & stats        | 3      | Anton, Sofiia| Labeled responses from backend |
| Aggregation + Analytics | Aggregates filtered responses, computes distributions & metrics     | 3      | Anton        | QC outputs                     |

**Total Points**: 15  

**Point allocation rationale**:  
Each component requires non-trivial logic and integration but is still manageable. UIs are moderately complex (audio + UX). Backend has to support audio plus tasks. QC and aggregation require statistical logic and data pipelines. 15 points keeps the project feasible for a small active team while leaving room for depth in QC/aggregation.

### Detailed Workflow

1. **Speaker submits clip**  
   Student opens the speaker UI, records or uploads a 10–20 second voice memo, selects language, and submits.

2. **Backend stores clip & creates task**  
   Backend validates file (duration, type), anonymizes it, stores it (e.g., `data/raw/` or cloud bucket), and creates one or more annotation tasks in the DB.

3. **Task assigned to crowd worker**  
   Crowd worker visits the task UI and is assigned a random available clip they haven’t seen yet. The system aims to balance the number of labels per clip.

4. **Worker listens and labels**  
   Worker listens to the clip and provides:
   - Accent guess  
   - Age range (e.g., `<18`, `18–22`, `23–30`, `30+`)  
   - Tone/emotion (e.g., calm, excited, nervous, sad)  
   - Optional confidence  
   - Answers attention-check questions when present  

5. **QC module evaluates responses**  
   QC receives batched responses and:
   - Computes per-worker accuracy/pass-rate on gold/attention clips  
   - Computes behavioral stats: median response time, entropy of choices, etc.  
   - Marks workers below thresholds as low-reliability  
   - Drops or down-weights their responses  
   - Optionally flags clips with very high disagreement  

6. **Aggregation module combines labels**  
   For each clip, aggregation:
   - Computes (possibly weighted) label distributions  
   - Extracts majority label per dimension  
   - Computes an agreement/uncertainty score  

7. **Feedback & analytics displayed**  
   - Speakers see a perception summary (e.g., “Most listeners heard you as non-native (Russian), 18–22, excited tone, agreement 74%”).  
   - Admin dashboard shows global statistics, distributions, and QC metrics.

### Human vs. Automated Tasks

| Task                             | Performed By          | Justification                                        |
|----------------------------------|-----------------------|------------------------------------------------------|
| Recording voice memos            | Human (speaker)       | Authentic speech must come from humans.              |
| Guessing accent/age/tone         | Human (crowd worker)  | Perception is subjective and socially constructed.   |
| Basic validation (type/length)   | Automated             | Deterministic checks can be fully automated.         |
| QC filtering & aggregation       | Automated (with rules)| Algorithms handle large-volume filtering & combining.|

---

## Quality Control Module

### QC Strategy Overview

The QC module ensures that perception data reflects genuine listening rather than random clicking. Because labels (accent, age, tone) are subjective, we cannot rely purely on “correct” answers. Instead, we combine:

- **Attention/gold clips**: Some clips have known properties or explicit instructions (e.g., “Select ‘calm’ for this clip”) to detect non-listening.  
- **Worker behavior patterns**: We examine response times, entropy of options selected, and consistency on control items.  
- **Outlier detection**: We identify responses that are extremely fast or wildly inconsistent with the rest of the crowd on control items.

This lets us filter low-effort work while preserving genuine diversity in perception.

### Specific QC Mechanisms

**Primary mechanism**: Combination of attention/gold checks, worker reliability scoring, and simple outlier rules.

**Implementation details:**

- **Input format**:  
  Batched worker responses per task, including:
  - `worker_id`  
  - `clip_id`  
  - `accent_guess`  
  - `age_range`  
  - `tone_guess`  
  - `confidence`  
  - `is_gold` flag  
  - `response_time_sec`  

- **Processing**:
  - Compute per-worker accuracy/pass-rate on gold/attention clips.  
  - Compute behavioral stats: median response time, entropy of choices, etc.  
  - Mark workers below thresholds as low-reliability.  
  - Drop or down-weight their responses.  
  - Optionally flag clips with very high disagreement.

- **Output format**:
  - Cleaned responses with `weight` for each.  
  - Worker-level reliability scores.  
  - List of flagged clips for possible review.

- **Threshold for acceptance** (example):
  - Gold/attention pass-rate ≥ 70–80%.  
  - Median response time above minimal threshold (e.g., audio length + a few seconds).  
  - Choice entropy above a small value (to avoid “always pick first option”).

**Additional mechanisms:**

- **Gold standard / control questions**: ~5–10% of tasks, with clearly defined expected answers for at least one dimension.  
- **Majority checks on gold**: workers who consistently disagree with the majority on control items are down-weighted.  
- **Attention checks**: e.g., instructions like “For this clip, select ‘calm’ regardless of what you hear.”  
- **Reputation system (optional)**: could aggregate performance across sessions.  
- **Statistical outlier detection**: identifies extremely fast or low-entropy response patterns.

### QC Module Code Plan

**Location in repo**: `src/qc/quality_control.py`

**Key functions/classes:**
1. `compute_worker_stats(responses_df)`: Computes per-worker accuracy on gold clips, median response time, and choice entropy.  
2. `flag_low_quality_workers(worker_stats, thresholds)`: Returns a set/dict of worker_ids marked as low-quality or assigns reliability scores.  
3. `filter_and_weight_responses(responses_df, worker_stats)`: Applies worker weights, drops invalid responses, and yields a cleaned dataset for aggregation.

**Input data format (JSON example):**
```json
[
  {
    "worker_id": "w_123",
    "clip_id": "c_001",
    "is_gold": true,
    "accent_guess": "US",
    "age_range": "18-22",
    "tone_guess": "excited",
    "confidence": 0.8,
    "response_time_sec": 7.2
  }
]
```

**Output data format (JSON example):**
```json
{
  "clean_responses": [
    {
      "worker_id": "w_123",
      "clip_id": "c_001",
      "accent_guess": "US",
      "age_range": "18-22",
      "tone_guess": "excited",
      "weight": 0.95
    }
  ],
  "worker_stats": {
    "w_123": {
      "gold_accuracy": 0.9,
      "median_time": 6.5,
      "choice_entropy": 1.2,
      "reliability": 0.95
    }
  },
  "flagged_clips": ["c_017", "c_042"]
}
```

**Sample scenario (short):**  
Worker A passes most attention checks, has reasonable timings, and varied choices → high reliability, high weights.  
Worker B fails most gold items, answers in <1 second, always chooses the first option → marked low-reliability, responses heavily down-weighted or dropped.

---

## Aggregation Module

### Aggregation Strategy Overview

The aggregation module converts QC-filtered responses into clip-level summaries that are interpretable for both speakers and analysis. Because labels are categorical and subjective, we focus on:

- Weighted distributions over labels (accent, age range, tone)  
- Majority labels per dimension  
- Agreement/uncertainty scores (e.g., based on entropy)

This provides more nuance than a single label and fits our perception-based setting.

### Aggregation Method

**Primary method**: Weighted majority voting + distributional summaries.

**Implementation details:**

- **Input format**: QC output: cleaned responses with weights plus optional worker reliability stats.

- **Processing per clip**:
  - Group responses by `clip_id`.  
  - For each dimension (accent, age_range, tone):
    - Compute weighted counts per category (using worker weights).  
    - Normalize to probabilities (distribution).  
    - Select argmax as majority label.  
  - Compute agreement score (e.g., `1 - normalized_entropy`).

- **Output format**: for each clip:
  - `accent_distribution`, `age_range_distribution`, `tone_distribution`  
  - `accent_majority`, `age_range_majority`, `tone_majority`  
  - `agreement_score`  
  - `num_workers`  

- **Handling edge cases**:
  - **Ties**: break using total worker reliability; if still tied, random tie-break + mark as low-confidence.  
  - **Not enough data**: if < N (e.g., 5) responses, mark as “insufficient data.”  
  - **Highly flat distributions**: highlight high uncertainty instead of claiming a strong majority.

**Why this method**:  
It is intuitive, easy to implement, and well-aligned with QC. It also shows diversity in perception rather than forcing a single “correct” answer.

### Aggregation Module Code Plan

**Location in repo**: `src/aggregation/aggregate.py`

**Key functions/classes:**
1. `aggregate_clip_labels(clean_responses, worker_stats)`: Core aggregation routine producing clip-level summaries.  
2. `compute_agreement(distribution)`: Computes an agreement/uncertainty score from a distribution (e.g., entropy-based).  
3. `build_feedback_payload(clip_summary)`: Converts internal summary format into a structure ready for display in the frontend.

**Input data format (JSON example):**
```json
{
  "clean_responses": [
    {
      "worker_id": "w_123",
      "clip_id": "c_001",
      "accent_guess": "Non-native (Russian)",
      "age_range": "18-22",
      "tone_guess": "excited",
      "weight": 0.95
    }
  ],
  "worker_stats": {
    "w_123": {"reliability": 0.95}
  }
}
```

**Output data format (JSON example):**
```json
{
  "clip_id": "c_001",
  "accent_distribution": {
    "Non-native (Russian)": 0.68,
    "US": 0.22,
    "Other": 0.10
  },
  "age_range_distribution": {
    "18-22": 0.75,
    "23-30": 0.20,
    "<18": 0.05
  },
  "tone_distribution": {
    "excited": 0.60,
    "calm": 0.25,
    "nervous": 0.15
  },
  "accent_majority": "Non-native (Russian)",
  "age_range_majority": "18-22",
  "tone_majority": "excited",
  "agreement_score": 0.72,
  "num_workers": 12
}
```

**Sample scenario (short):**  
For clip `c_010`, 15 workers respond. After QC, 3 workers are down-weighted. Aggregation yields majority tone “nervous” with high agreement, but accent is split between “US” and “Non-native (Russian)”. Feedback indicates strong consensus on tone but ambiguity on accent.

### Integration: QC ↔ Aggregation

QC runs before aggregation and passes cleaned responses and worker reliability scores to aggregation. Aggregation uses these weights but otherwise treats QC as a black box. Both share common schemas (worker_id, clip_id, label fields, weight), making it easy to re-run aggregation if QC thresholds change.

---

## User Interface & Mockups

### Interfaces Required

**For Crowd Workers:**
- [x] Task interface / HIT design  
- [x] Instructions page  
- [ ] Training/qualification interface (optional)

**For End Users (Speakers):**
- [x] Main interface (record/upload clip)  
- [x] Results display (“How the crowd heard you”)  
- [ ] Optional profile/settings page  

**For Administrators:**
- [x] Basic dashboard/monitoring  
- [ ] Data export interface (optional)

### Mockup Details

**Mockup location**: `docs/mockups/` (and/or Figma: `[TBD link]`)  

#### Interface 1: Crowd Task Page

- **User type**: Crowd worker  
- **Purpose**: Present one clip at a time and collect accent/age/tone guesses + confidence.  
- **Key elements**:
  - Audio player (play/pause, replay)  
  - Accent options (dropdown or radio buttons)  
  - Age range options  
  - Tone/emotion options  
  - Confidence slider or discrete levels  
  - Progress indicator (e.g., “Task 3 of 10”)  
- **Mockup file**: `docs/mockups/crowd_task.png`  
- **Notes**: Includes short instructions and reminders about listening fully.

#### Interface 2: Speaker Feedback Page

- **User type**: End user (speaker)  
- **Purpose**: Show how the crowd perceived their clip.  
- **Key elements**:
  - Clip info (prompt, timestamp)  
  - Majority accent, age range, and tone with percentage or bar charts  
  - Agreement/uncertainty indicator  
  - Explanation text emphasizing that this is perception, not “truth”  
- **Mockup file**: `docs/mockups/speaker_feedback.png`  
- **Notes**: Option to delete their clip and data.

#### Interface 3: Admin Dashboard

- **User type**: Admin / team  
- **Purpose**: Monitor basic system stats.  
- **Key elements**:
  - Number of clips, responses, active workers  
  - QC summary (e.g., % filtered)  
  - Simple label distribution plots  
- **Mockup file**: `docs/mockups/admin_dashboard.png`  

### Task Design (for crowd workers)

**HIT title**: Guess a speaker’s accent, age, and tone from a short voice clip

**HIT description**:  
Listen to short anonymous audio clips and guess the speaker’s accent, age range, and tone. Each task takes about 30–60 seconds and helps us understand how people’s voices are perceived.

**Task instructions (what workers see):**

> You will hear short, anonymized audio clips of people speaking.  
>  
> 1. Please listen to the **entire** clip at least once before answering.  
> 2. For each clip, select:  
>    - The accent you believe the speaker has (best guess).  
>    - The age range you think the speaker falls into.  
>    - The tone/emotional state you perceive (e.g., calm, excited, nervous).  
> 3. There are no right or wrong answers for most clips. We are interested in your honest perception.  
> 4. Some clips may include simple checks (e.g., “Please choose ‘calm’ for this one”) to ensure careful listening.  
> 5. If you are unsure, pick the closest option and adjust confidence accordingly.  
>  
> Use headphones or a quiet environment if possible.

**Example task:**
- Audio: 15-second clip of a student introducing themselves.  
- Worker responds:
  - Accent: “Non-native (Russian)”  
  - Age range: “18–22”  
  - Tone: “excited”  
  - Confidence: “Medium”

**Estimated time per task**: ~30–60 seconds per clip  

**Payment per task**:
- Class volunteers: no direct monetary payment (intrinsic / research interest).  
- Backup MTurk: ~$0.05–$0.10 per 5-clip HIT (TBD & adjusted to be fair).

**Number of tasks per HIT** (if MTurk): ~5 clips per HIT  

**Qualifications required** (if MTurk):
- >95% approval rate, >100 HITs, location = [TBD if needed].

---

## Technical Stack

### Technologies

**Frontend**: React (or React + Vite)  

**Backend**: Python (FastAPI or Flask)  

**Database**: PostgreSQL (prod), SQLite (local dev)  

**Crowdsourcing Platform**:
- Primary: Custom web app with class volunteers  
- Backup: MTurk / Prolific  

**ML/AI Tools** (if used):
- pandas, scikit-learn for analysis  
- (Optional) librosa or similar for simple audio features  

**Hosting/Deployment**:
- Backend + DB: Heroku / Render / small VM (TBD)  
- Frontend: Vercel / Netlify (TBD)  
- Local-only deployment acceptable for in-class demo if needed.

**Other tools**:
- Cursor for AI-assisted coding  
- Figma for mockups  
- GitHub Projects / Issues for project tracking  

### Repository Structure

**Planned structure:**
```text
auralynx/
├── README.md
├── docs/
│   ├── flow-diagram.pdf
│   ├── mockups/
│   │   ├── crowd_task.png
│   │   ├── speaker_feedback.png
│   │   └── admin_dashboard.png
│   └── data_notes.md
├── src/
│   ├── frontend/       # React app
│   ├── backend/        # FastAPI/Flask app
│   ├── qc/
│   │   └── quality_control.py
│   ├── aggregation/
│   │   └── aggregate.py
│   └── utils/
├── data/
│   ├── raw/
│   ├── sample-qc-input/
│   ├── sample-qc-output/
│   ├── sample-agg-input/
│   └── sample-agg-output/
└── ...
```

**Explain any deviations**:  
If tools change (e.g., Flask → FastAPI), structure may adjust slightly but `qc/` and `aggregation/` will remain separate modules with clear I/O.

---

## Data Management

### Input Data

**Source**:
- Primary: Voice memos recorded by student participants via the speaker UI.  
- Auxiliary: Team-created/test clips and gold/control clips.

**Format**:
- Audio: `.wav` / `.mp3`  
- Metadata: JSON/DB records including `clip_id`, `upload_time`, optional self-report (e.g., native language).

**Sample data location**: `data/raw/`  

**Sample data description**:  
A small set of 5–10 short clips demonstrating different accents/tones plus synthetic gold/attention-check clips.

**How much data do we need?**
- Testing/development: ~5–10 speakers, ~3–5 guesses per clip.  
- Final demo/analysis: ~25–40 speakers, ~10–20 guesses per clip.

**Data collection plan**:
- Week 1–2: Internal/test clips from team and friends.  
- Week 2–3: Main collection from class volunteers and peers.  
- Week 3–4: Top-up if some clips have too few guesses.

### QC Module Data

**Input location**: `data/sample-qc-input/`

**Input format (example CSV):**
```csv
worker_id,clip_id,is_gold,accent_guess,age_range,tone_guess,confidence,response_time_sec
w_1,c_01,True,US,18-22,calm,0.9,6.2
w_1,c_02,False,Non-native (Russian),18-22,excited,0.8,7.1
...
```

**Output location**: `data/sample-qc-output/`

**Output format (example CSV):**
```csv
worker_id,clip_id,accent_guess,age_range,tone_guess,weight,flagged
w_1,c_01,US,18-22,calm,0.95,False
...
```

**Sample scenario docs**:  
`data/sample-qc-input/README.md` will describe which workers are intentionally low-quality and expected QC behavior.

### Aggregation Module Data

**Input location**: `data/sample-agg-input/`

**Input format (example CSV):**
```csv
clip_id,worker_id,accent_guess,age_range,tone_guess,weight
c_01,w_1,US,18-22,calm,0.95
c_01,w_2,Non-native (Russian),18-22,calm,0.90
...
```

**Output location**: `data/sample-agg-output/`

**Output format (example CSV):**
```csv
clip_id,accent_majority,age_range_majority,tone_majority,agreement_score,num_workers
c_01,Non-native (Russian),18-22,calm,0.72,12
...
```

**Sample scenario docs**:  
`data/sample-agg-input/README.md` explains expected aggregated outcomes for the sample data.

### Data Dependencies

**Does QC output feed into aggregation?**  
Yes. Aggregation expects QC-filtered/weighted responses as input. Without QC, aggregated results could be biased by low-effort responses.

**Data flow between modules**:  
Raw responses → DB → exported or DataFrame → QC (`sample-qc-input` → `sample-qc-output`) → Aggregation (`sample-agg-input` → `sample-agg-output`) → Feedback/UI + analysis.

---

## Crowd Recruitment & Management

### Recruitment Strategy

**Where will workers come from?**
- Class volunteers (this course, possibly others)  
- Friends/peers via group chats and Discord  
- Backup: MTurk/Prolific if needed

**How will you reach them?**
- Announcements in class/Slack/Canvas (if allowed)  
- Posts in student chats/Discord servers  
- Direct DMs to friends with a short link + explanation

**When will you recruit?**
- Pilot: Week 2  
- Main recruitment: Week 3  
- Backup/MTurk: Week 3–4 if needed  

### Worker Incentives

**Compensation model**:

- Primary: Intrinsic motivation (helping research/classmates), possibly extra credit if approved.  
- Backup: MTurk/Prolific payment.

Example for MTurk:
- Payment per HIT: $0.05–$0.10 for 5 clips  
- Estimated time: ~3–5 min per HIT  
- Effective hourly rate: ~$6–12/hour (to be calibrated/fair)

**Justification**:  
Class volunteers are likely enough at our scale; if not, MTurk/Prolific ensures we can hit minimum annotation counts.

### Scale Requirements

**For MVP/Demo:**
- Minimum workers: ~15  
- Minimum tasks: ~200 guesses  
- Timeline: Before in-class demo date.

**For Full Analysis:**
- Target workers: ~30–50  
- Target tasks: ~500–800 guesses  
- Timeline: Before final report deadline.

### Backup Plan

If recruitment is insufficient:
- [x] Use MTurk/Prolific with a small budget  
- [x] Simplify tasks (e.g., fewer clips or fewer label dimensions)  
- [x] Use synthetic/simulated data to demonstrate pipeline if required  
- [ ] Organize a short in-class annotation session (if allowed)

---

## Project Milestones & Timeline

*(Dates are placeholders; adjust to course calendar.)*

### Week 1 (Dates: [X/X – X/X])

- **Milestone**: Core architecture + Repo skeleton
- **Tasks**:
  - [ ] Set up repo structure & CI – Alex  
  - [ ] Define DB schema for clips/responses – Alex  
  - [ ] Draft QC & aggregation design doc – Anton  
- **Deliverable**: Running “hello world” backend and static UI mock.

### Week 2 (Dates: [X/X – X/X])

- **Milestone**: End-to-end prototype (manual data)
- **Tasks**:
  - [ ] Implement speaker upload UI + API – Alex  
  - [ ] Implement basic crowd task UI – Alex  
  - [ ] Implement QC prototype on CSV data – Anton  
  - [ ] Implement simple unweighted aggregation – Anton  
- **Deliverable**: Manual pipeline: upload → label → CSV → QC → aggregation → text feedback.

### Week 3 (Dates: [X/X – X/X])

- **Milestone**: Integrated system + Pilot study
- **Tasks**:
  - [ ] Connect QC + aggregation into backend – Alex & Anton  
  - [ ] Build speaker feedback UI – Alex  
  - [ ] Run small pilot with friends/class volunteers – Anton  
  - [ ] Tune QC thresholds based on pilot – Anton  
- **Deliverable**: Working demo with pilot data + basic analytics.

### Week 4 (Dates: [X/X – X/X])

- **Milestone**: Main data collection + Analysis
- **Tasks**:
  - [ ] Main recruitment push – Martina  
  - [ ] Finalize visualizations & admin dashboard – Jason  
  - [ ] Run full analysis & draft results – Anton, Sofiia  
  - [ ] Integrate methods/results into final write-up – team  
- **Deliverable**: Final dataset, analysis code, polished demo.

### Critical Path

**Blocking dependencies**:
1. DB schema and backend routes must exist before real QC/aggregation can consume DB data.  
2. Crowd task UI must be functional before large-scale recruitment.  

**Parallel work**:
- Alex & Jason: Frontend + backend infrastructure  
- Anton & Sofiia: QC + aggregation logic, analysis on synthetic/sample data  
- Martina: Recruitment and communication materials  

**Integration points**:
- [Date 1]: QC + aggregation integrated into backend.  
- [Date 2]: Frontend (speaker + worker) fully hooked up to backend APIs.

---

## Risk Management

### Technical Risks

**Risk 1**: Browser audio recording issues  
- Likelihood: Medium  
- Impact: Medium–High  
- Mitigation: Use well-tested recording libraries; provide an upload fallback.  
- Backup: If recording is too flaky, shift to upload-only with clear instructions.

**Risk 2**: Deployment/DB performance problems  
- Likelihood: Medium  
- Impact: Medium  
- Mitigation: Start with modest scale; add logging; test early with small loads.  
- Backup: For demo, run everything locally using a pre-loaded dataset.

### Crowd-Related Risks

**Risk 1**: Not enough workers  
- Likelihood: Medium  
- Impact: High  
- Mitigation: Recruit early and widely; keep tasks short.  
- Backup: MTurk/Prolific or an in-class annotation session.

**Risk 2**: Low-quality contributions  
- Likelihood: Medium  
- Impact: Medium  
- Mitigation: QC with attention/gold checks and clear instructions.  
- Backup: Increase strictness; use high-reliability subset for main analysis.

### Resource Risks

**Risk 1**: Only two active devs initially  
- Likelihood: High  
- Impact: Medium–High  
- Mitigation: Scope tightly and prioritize: (1) pipeline, (2) basic UI, (3) nice-to-have analytics.  
- Backup: De-scope advanced UI/ML; focus on demonstrating QC + aggregation.

---

## Evaluation Plan

### What You'll Measure

**Primary metrics:**
1. **Average valid guesses per clip**:  
   Post-QC; target ≥10 per clip for main dataset.
2. **Agreement score per dimension**:  
   Tone vs accent vs age; show where the crowd is most consistent.
3. **QC rejection rate**:  
   Fraction of responses filtered; sanity check that QC is active but not overly aggressive.

**Secondary metrics:**
1. **Worker completion time distribution**:  
   Check for rushed workers and usability.  
2. **Match between self-reported and perceived labels** (where available):  
   E.g., self-reported accent vs crowd accent distribution.

### Analysis Approach

**Key questions:**
1. How consistently can a crowd agree on a speaker’s tone vs accent vs age?  
2. How much does QC change the aggregated results compared to using raw responses?  
3. Are there signs of systematic bias in perceptions (e.g., specific accents perceived as certain ages/tones)?

**Comparisons:**
- [x] Compare raw vs QC-filtered aggregation.  
- [x] Compare unweighted vs weighted aggregation (if time).  
- [x] Compare agreement across dimensions (accent vs age vs tone).  
- [ ] Compare crowd performance vs a trivial baseline (e.g., always majority class).  
- [ ] Analyze cost/quality tradeoffs if using paid workers.

**Data collected for analysis:**
- Clip-level: self-reported metadata (where available).  
- Worker-level: reliability, number of tasks.  
- Response-level: guessed labels, confidence, response time, QC flags.

**Analysis methods:**
- Descriptive stats & histograms  
- Confusion matrices (when ground truth exists)  
- Chi-square tests for distributions  
- t-tests / non-parametric comparisons for QC vs non-QC scenarios  
- Visualizations: bar charts, heatmaps, scatter plots (agreement vs number of workers)

---

## Ethical Considerations

### Worker Treatment

**Fair compensation**:  
If we pay workers (e.g., MTurk/Prolific), we will calibrate rates to reflect realistic completion times. For class volunteers, participation is voluntary, tasks are short, and we emphasize their contribution to research.

**Informed consent**:  
Workers see a short consent statement describing:
- What data is collected (their guesses + timing, not their own voice)  
- How it will be used (class project + research summary)  
- That participation is voluntary and they may stop at any time.

**Rejection policy**:  
Work is rejected (or not counted) only in clear cases of low-effort behavior: failing straightforward attention checks or obviously random clicking. This is mentioned explicitly in the instructions.

### Data Ethics

**Privacy**:
- Clips are anonymized (no names/IDs embedded in audio).  
- No personal identifiers shown to crowd workers.  
- Data stored in restricted locations (private repo, limited access).

**Consent**:
- Speakers are told their voices will be used in a perception study for this class project.  
- They may request deletion of their clip and associated data.

**Data storage**:
- Audio + metadata stored in project’s private storage and/or local machines.  
- Only the team and instructors have access as needed.

### Potential Harms

**Misuse potential**:  
Perception data of accent/age could be misused for discriminatory screening or profiling.

**Potential harms**:  
Speakers might feel judged or uncomfortable about how others perceive their accent or tone.

**Mitigation**:
- Clearly frame results as *perception*, not objective truth or ability.  
- Avoid any ranking or “score” of accents.  
- Use aggregated/report-level results and avoid releasing raw individual-level data publicly.  

---

## Documentation Standards

### Code Documentation

Each module will include:
- Docstrings for all functions/classes  
- README in the module directory (e.g., `src/qc/README.md`)  
- Example usage snippets  
- Clear I/O format descriptions  

**Current documentation status**:
- QC module: Not yet documented (will be as implementation stabilizes).  
- Aggregation module: Not yet documented.  
- Frontend/backend: Not yet documented.

### Repository README

`README.md` must include:
- [x] Project overview & goals  
- [x] Setup instructions (install, run backend/frontend)  
- [x] How to run the full system  
- [x] Where QC/aggregation code lives  
- [x] Data format specs  
- [x] Team contacts  
- [ ] License information (TBD)

### Ongoing Documentation

To keep docs current:
- Update docstrings whenever function signatures or behavior change.  
- Update module READMEs when data formats change.  
- Track breaking changes in a simple `CHANGELOG.md` or GitHub issues.

---

## Questions for Teaching Staff

### Technical Questions

1. Is the proposed QC design (attention checks + reliability scoring + outlier detection) sufficiently robust for this project’s expectations?  
2. Are there any recommended examples or libraries from previous course projects for audio-heavy web apps?  
3. Is a custom web interface for crowd workers acceptable, or would integrating directly with MTurk APIs be preferred/encouraged?

### Scope Questions

1. Is focusing on accent, age, and tone for English clips too broad, or should we narrow (e.g., only tone + accent)?  
2. Does our 15-point component breakdown seem appropriate for a team that currently has 2 active developers (with 5 total members)?  
3. What clip and guess counts are considered “enough” to support a solid final analysis?

### Resource Questions

1. Is there any departmental/course support for a small MTurk/Prolific budget, or should we assume $0 and rely entirely on volunteers?  
2. Are there restrictions on recruiting non-class participants (e.g., other Penn students)?

### Other Concerns

- Are there any IRB-related concerns given anonymized student voice data, or is this safely within standard class project boundaries?

---

## Commitment

We commit to:

- [x] Building a working prototype with functional QC and aggregation modules  
- [x] Creating comprehensive documentation in our GitHub repository  
- [x] Recruiting and managing a real (or simulated) crowd  
- [x] Collecting sufficient data for meaningful analysis  
- [x] Meeting project milestones on schedule (or proactively communicating blockers)  
- [x] Treating crowd workers ethically and fairly  

**Team signatures**:

- _________________________ [Name], [Date]  
- _________________________ [Name], [Date]  
- _________________________ [Name], [Date]  
- _________________________ [Name], [Date]  

---

## Submission Checklist

- [X] Completed all sections of this template  
- [X] Provided team availability for TA meetings  
- [X] Listed team skills and learning needs  
- [X] Included point values for all components (total 15–20)  
- [X] Described detailed implementation timeline  
- [X] Identified risks and mitigation strategies  
- [X] Had all team members review and sign  

Then:

- [ ] Set up GitHub repository with required directory structure  
- [X] Prepared questions for teaching staff  
- [ ] Created flow diagram showing QC and aggregation modules  
- [ ] Created mockups for all user-facing interfaces  
- [ ] Added sample input/output data for QC module  
- [ ] Added sample input/output data for aggregation module  

**Submission method**:
- Pull request to `ideation-fall-2025` repository, in `round5_final` folder  
- Should be in the root of your GitHub organization  

**Submission deadline**: Thursday, Nov. 13 at 11:59 PM ET
