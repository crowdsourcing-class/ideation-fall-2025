# Final Project Proposal: Blink

**Team Name**: Team 10
**Submission Date**: 11/13/2025  
**GitHub Organization**: https://github.com/nets2130team10

---

## Team Information

### Team Members

| Name | PennKey | Primary Role(s) | Secondary Skills |
|------|---------|----------------|------------------|
| Amber He | heamber | Database & Backend integration | Databases, SQL, Python, Java |
| Anika Basu | basua | Backend | |
| Emily Kang | emkang | Frontend, UI/UX | |
| Mingni Dong | mdong126 | Backend | |

### Team Skills Inventory

**Skills we have:**
- Python: Amber, Anika, Emily
- Java: Amber, Anika, Mingni, Emily
- React: Emily, Amber, Mingni
- Databases: Amber, Mingni
- Deployment: 

**Skills we need to learn/acquire:**
- Vercel: To deploy the webapp for free - ?? backend people/Amber if needed.
- Supabase: To host database for free - Amber

**External resources we might need:**
- Maybe transcription service…?
- Free vercel and supabase

### Team Availability for TA Meetings

**Week of Monday the 17th of November:**

_List all time slots when the ENTIRE team can meet with a TA. Use Eastern Time. Format: Day, Time-Time_

https://www.when2meet.com/?33539494-rh14s 

- Monday: [e.g., 2:00 PM - 4:00 PM, 6:00 PM - 8:00 PM]
- Tuesday: [e.g., 10:00 AM - 12:00 PM]
- Wednesday: [e.g., 3:00 PM - 5:00 PM]
- Thursday: [Not available]
- Friday: [e.g., 1:00 PM - 3:00 PM]

**Preferred meeting duration**: 30 min

**Meeting format preference**: Zoom

**Primary contact for scheduling**: Amber, heamber@seas.upenn.edu

---

## Project Overview

**Original idea from**: Professor Lumbroso

**How the idea evolved**: 
_Briefly describe how your project changed from its original conception through Rounds 1-4 to this final proposal_

The original idea was centered around students being confused in lectures, and professors can figure out at what time students lost them. Then, we talked about having it being useful for professors mostly, where the webapp would record the lecture audio and maybe transcribe the audio. However, we had a discussion with Professor Lumbroso about the difficulty of recording and storing audio, and we were encouraged to think more about the scope of the project. Is timestamp confusion counts only useful for lectures? Or for business meetings. Should it only be for penn students? Or all students? Finally, we decided we want to expand the generalization of our webapp, to anything that the user wants to use it for. Any group setting where counts of button presses is useful. Whether that is an attention check, an “agree” button, a confusion button. With Blink, any group or organizer can use this simple, but useful collection of crowd feedback to accomplish whatever they want to.

### Problem Statement

_Refined from your Round 4 decision_

Sometimes during meetings/lectures, people don’t want to speak up when they’re confused because they’re shy, don’t want to interrupt, etc. With Blink, students/meeting members can voice their confusion without interrupting the speaker, and the speaker will get an idea of common confusion points. If there’s a follow-up meeting, they can then focus on clarifying those confusion areas. The use of the online button can even be extended beyond confusion, like with attention checks.

### One-Sentence Pitch

Blink is the voice of the audience in large learning settings.

### Target Users

**End Users**: Speakers and audience members

**Crowd Workers**: Members of any audience- students, employees, etc.

**Scale**: We need it to work for any number of crowd members. It shouldn’t be that there’s a smaller class/meeting and Blink says “not enough data”. The harder part will be getting enough data for smaller crowds/less check-in times. Once that’s solved, the solution will be easily extendable to larger audiences.

### Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [X] Business idea using crowdsourcing
- [ ] Other: [specify]

## System Architecture

### Flow Diagram

_Required: Include a visual flow diagram showing the major components/stages of your project_

**Flow diagram location**:



figma.com/board/FTbfCK1L9XR9Hwd4tz87yB/Blink-5-Component-User-Flow?node-id=0-1&p=f&t=Rzi4O40wmkJhzDtU-0


Your flow diagram MUST clearly show:
- [X] Where/when the crowd touches the data
- [X] Your quality control module
- [X] Your aggregation module
- [X] Data flow between components
- [X] What happens before crowd involvement
- [X] What happens after crowd contribution

**If you haven't created it yet**: Describe in words the major components and their relationships:

1. [Event Setup] → [Crowd Interface] → [Quality Control] → [Data Aggregation] → [Insights Output]

### Major System Components

_List all major components with point values (1-4) indicating implementation complexity. Total should be 15-20 points._

| Component | Description | Points | Owner(s) | Dependencies |
|-----------|-------------|--------|----------|--------------|
| [Event Setup ] | [Interface where the organizer creates a session, chooses button types (confusion, agree, attention), and generates a join link or code. Handles session metadata and initial configuration.] | [3] | [Emily, Mingni, Anika] | [This is the first step] |
| [Crowd Interface Module | [User-facing page where participants join via link/code and press buttons. Implements UI, button logic, and rate-limiting to prevent spam.] | [4] | [Emily, Mingni, Anika] | [Event Setup] |
| [Quality Control] | [Validates incoming events (e.g., user/session authenticity, rate limits, malformed events). Ensures data cleanliness before processing] | [3] | [Amber] | [Crowd Interface + Event Setup] |
| [Aggregation Module] | [Aggregates all validated button presses, attaches timestamps, and updates real-time counts. Feeds data to both storage and dashboard.] | [4] | [Amber, Mingni, Anika] | [Quality Control + Crowd Interface + Event Setup] |
| [Insights Output] | [Heatmap display of the main confusion points for the host to analyze and plan follow-ups from.] | [4] | [Name(s)] | Determine what’ll be used to generate and show the heatmap. Also determine how much information will be displayed- something additional to the heatmap? Timestamps from stored audio/video? |

**Total Points**: 18

**Point allocation rationale**: 
_If teaching staff questions your point distribution, explain your reasoning here_

### Detailed Workflow

_Step-by-step description of how your system works from start to finish_

1. **[Step 1]**: The host creates a new session for their presentation/meeting.
2. **[Step 2]**: At the beginning of the session, all attendees receive a link/QR code for it.
3. **[Step 3]**: Throughout the session, attendees mark their confusion points by pressing the “I’m confused” button. Perhaps they’ll be able to mark times of other emotions/more specific confusions if we add to the MVP.
4. **[Step 4]**: Data from all attendees are aggregated (number of confused attendees at a particular point in time, all timestamps of confusion).
5. **[Step 5]**: At the end of the session, the host receives an insights panel with a heatmap of main confusion points, and perhaps other informative displays of other statistics.


### Human vs. Automated Tasks

| Task | Performed By | Justification |
|------|--------------|---------------|
| [Clicking the confusion button] | Human | [Requires human judgment of confusion] |
| [QC filtering] | Automated | [Deterministic, can detect rate-limit violations] |
| [Aggregation of clicks] | Automated | [Purely computational] |
| [Event creation & interpretation of results] | Human | [Requires human planning & analysis] |

---

## Quality Control Module

### QC Strategy Overview

Since crowd input is simply button clicks, QC focuses on preventing spam, accidental double-clicks, or automated input. We enforce rate limits (1 click per interval), device ID checks, and timestamp sanity checks. This ensures the aggregated confusion heatmap reflects true audience reactions, not noisy or malicious data.

### Specific QC Mechanisms

**Primary mechanism**: [Rate-limit+ Identity Validation + Timestamp Filtering] 

**Implementation details**:
- Input format: [receives some data like this: {
  "sessionId": "abc123",
  "userId": "u57f92",
  "eventType": "confusion",
  "timestamp": 1731974039123,
  "deviceHash": "d91f0ac2bd"
}
]
- Processing: [Rate limiting: Enforce max 1 press every X ms (e.g., 500 ms), Reject bursts or sustained rapid-fire inputs
Duplicate-event suppression: If the user sends identical eventTypes within an interval → drop it
Timestamp sanity checks: Reject timestamps more than ±5s from server time, Prevent client-clock manipulation
Device consistency validation: Each userId must map to one stable deviceHash, Reject events if deviceHash suddenly changes mid-session (possible bot or spoofing)
Session membership verification: Reject events if the user hasn't properly joined the session, Reject eventTypes not enabled by the organizer
Basic anomaly detection: Flag users with several rejected events (spam-like behavior), Optionally ghostban: accept join but drop events silently
]
- Output format: [Something like this: ​​{
  "status": "ok",
  "sessionId": "abc123",
  "userId": "u57f92",
  "eventType": "confusion",
  "timestamp": 1731974039450   // server-corrected timestamp
}
this is if it gets rejected: 
{
  "status": "rejected",
  "reason": "rate_limit_exceeded",
  "userId": "u57f92"
}

]
- Threshold for acceptance: [It’ll be accepted if it comes from a valid session + device, it passes the rate limit, the timestamp is within the allowed drift window, the deviceHash and userId mapping is consistent, and the eventType is allowed for the session]

**Additional mechanisms**:
- [ ] Gold standard questions
  - _How many? How distributed? Pass/fail criteria?_
- [ ] Majority voting across multiple workers
  - _How many workers per task? Tie-breaking?_
- [ x] Attention checks
  - _We can include soft-attention checks to detect users who never interact after joining (maybe a bot?), detect users who press random buttons at fixed intervals(non-human activity)_
- [ x] Reputation system
  - _users w/ history of normal activity across multiple sessions = clean reputation, devices flagged repeatedly for spam get rate limits_
- [x ] Statistical outlier detection
  - _extreme outliers like 10 events in 5 seconds, uniform periodic events (this is bot like),these outliers will show warning → be dropped_
- [ ] Other: [specify and explain]

### QC Module Code Plan

**Location in repo**: [e.g., `src/qc/quality_control.py`]

**Key functions/classes**:
1. [validateEvent(event)]: [Top level QC entry point, validates a raw incoming event from the user before it reaches the aggregation module]
2. [RateLimiter]: [enforces click frequency limits per user to prevent spam or double clicks]
3. [TimeStampChecker]: [Ensures timestamps are reasonable + not manipulated]

**Input data format**: 
```
[Describe or show example of input data structure]
```
{
  "sessionId": "abc123",
  "userId": "u57f92",
  "eventType": "confusion",   // ex: "confusion", "agree", "attention"
  "timestamp": 1731974039123 
}
identifies the live event that the user is participating in, their userId, the button the user pressed, and when this user pressed the button

**Output data format**:
```
[Describe or show example of output data structure]
```
{
  "sessionId": "abc123",
  "summary": {
    "confusion": [
      { "count": 12, "timestamp": 1731974010000 },
      { "count": 18, "timestamp": 1731974075000 }
    ],
    "agree": [
      { "count": 7, "timestamp": 1731974042000 }
    ],
    "attention": [
      { "count": 4, "timestamp": 1731974098000 }
    ]
  },
  "updatedAt": 1731974100000
}
Output represents aggregated, validated, timestamped counts. each event type is an array of {count, timestamp} pairs. updatedAt marks the moment the aggregation was last computed

**Sample scenario**:
_Walk through a concrete example of your QC module in action_

[Example: "Worker A labels image as 'cat', Worker B labels as 'dog', Worker C labels as 'cat'. QC module applies majority voting, outputs 'cat' with confidence 0.67, flags disagreement for potential review."]

---

## Aggregation Module

### Aggregation Strategy Overview

When attendees press our feedback buttons- which range from “I’m confused” to “I’m paying attention”, etc.- these events will pass through quality-control code for identifying spam/trolling and blocking those users, removing accidental duplicate input, and ensuring legitimacy of input overall. These clean events are then passed on to the aggregation part.

Within the aggregation part, accumulated statistics are updated, such as the number of attendees confused at a particular point in time. From all the accumulated information at the end of the session, trends are quantitatively tracked and graphed in the output.

### Aggregation Method

**Primary method**: Bin-based time interval aggregation

**Implementation details**:
- Input format: Validated clicks
- Processing: Convert raw timestamps to interval index and increment confusion count for that interval
- Output format: Normalize values for heatmap color intensity
- Handling edge cases: 	If no clicks in interval → 0; If unusually low participation → display “Low Confidence” badge

**Why this method**:
Bin-based time interval aggregation is useful because our data is recorded at irregular times. Grouping events into fixed time bins (e.g., hourly or daily) creates consistent intervals, reduces noise, and makes trends easier to compare and analyze.

### Aggregation Module Code Plan

**Location in repo**: [e.g., `src/aggregation/aggregate.py`]

**Key functions/classes**:
1. [assign_to_bin(timestamp, bin_size)]: [Converts a raw timestamp into its corresponding bin index]
2. [aggregate_clicks(clicks, bin_size)]: [Iterates over validated clicks, assigns them to bins, and returns aggregated counts]
3. [normalize_counts(counts)]: [Scales bin totals into a 0–1 range for heatmap visualization]

**Input data format**:
```
[[
  {
    "worker_id": "W1",
    "timestamp": 12.84,
    "validated": true
  },
  {
    "worker_id": "W2",
    "timestamp": 14.02,
    "validated": true
  }
]]
```

**Output data format**:
```
[{
  "bin_size": 5,
  "bins": [
    { "interval_start": 0, "count": 3, "normalized": 0.42 },
    { "interval_start": 5, "count": 7, "normalized": 1.0 },
    { "interval_start": 10, "count": 0, "normalized": 0.0 }
  ]
}]
```

**Sample scenario**:
[Suppose 15 validated clicks come in over a 60-second clip. With a 5-second bin size, the module assigns each click to one of 12 bins. One interval (e.g., 25–30s) might accumulate 6 clicks, signaling a spike in confusion. After normalization, this becomes the brightest region in the heatmap.]

### Integration: QC ↔ Aggregation

**How do these modules interact?**
[Quality Control (QC) runs before aggregation. QC filters out invalid or low-quality clicks and outputs a clean set of validated events. The aggregation module then operates solely on these validated clicks to avoid skewed results. Both modules share the same data schema for click objects, ensuring smooth handoff. Aggregation does not modify QC outputs; it only transforms them into interval-based counts.]

**Data flow diagram** (if different from main flow diagram):
[Location or description]

---

## User Interface & Mockups

### Interfaces Required

_You need mockups for ALL user-facing interfaces_

**For Crowd Workers:**
- [x ] Task interface / HIT design
- [ x] Instructions page
- [ x] Training/qualification interface (if applicable)

**For End Users:**
- [x ] Main interface
- [ x] Results display
- [ x] Any configuration/input screens

**For Administrators (your team):**
- [ x] Dashboard/monitoring
- [x ] Data management interface

### Mockup Details

**Mockup location**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]

**For each interface, describe**:

#### Interface 1: [Crown Button Interface]
- **User type**: [Crowd worker]
- **Purpose**: [allows audience members to send reactions during a live session]
- **Key elements**: [three large colored buttons, session title, confirmation feedback ,mobile friendly layout]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [buttons should be easy to press]

#### Interface 2: [crowd instructions page]
- **User type**: [Crowd worker]
- **Purpose**: [explains what each button means + sets expectations before joining the live session]
- **Key elements**: [short explanation of each reaction type, responses are anon reassurance, join session button]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [keep text minimal, load instantly]

#### Interface 3: [organizer configuration/event setup page]
- **User type**: [end user]
- **Purpose**: [create a session + choose which reaction buttons will be enabled]
- **Key elements**: [text input for session name, checkbox/toggles for rxn types, start session button, auto generate join link/qr code]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [keep design consistent + setup should take <10 seconds]

#### Interface 4: [organizer main interface/live dashboard]
- **User type**: [end user]
- **Purpose**: [displays real time aggregated event counts during a session]
- **Key elements**: [live updating line/bar chart, timestamped spikes for each button type, session time, pause/resume feedback stream]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [must update smoothly, colors must clearly differentiate event types]

#### Interface 5: [post session results/replay view]
- **User type**: [end user]
- **Purpose**: [review confusion/engagement peaks after session ends]
- **Key elements**: [historical timeline of events, export buttons, peak detection markers, summary stats]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [similar layout to live dashboard for consistency, useful for prepping followup lectures/meetings]

#### Interface 6: [admin monitoring dashboard]
- **User type**: [admin]
- **Purpose**: [monitor real time system health + server performance]
- **Key elements**: [active sessions list, events per second throughput, QC rejection logs, server health metrics]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [only visible to developers, helps verify QC module performance during high load]

#### Interface 7: [admin data management interface]
- **User type**: [Admin]
- **Purpose**: [view, download, delete stored session data]
- **Key elements**: [table of past sessions, download buttons, delete/archive options]
- **Mockup file**: [https://www.figma.com/design/8g7lqxmlYv86yvcU8CuCET/Untitled?node-id=0-1&t=NA1iNCs0S64j9bSa-1]
- **Notes**: [only used during development, ensures compliance w/ data retention policies]



### Task Design (for crowd workers)

**If using MTurk or similar platform:**

**HIT title**: [Press Reaction Buttons During a Live Session]

**HIT description**: [Participants will join a short live session and press buttons (Confusion, Agree, Attention) at moments that match how they feel. Button presses are anonymous. There are no right or wrong answers—this is a simple behavioral feedback task.]

**Task instructions**: 
_Write the actual instructions workers will see. Be specific and clear._


**Example task**:
[For ex)Welcome to the Blink Reaction Task!
You will join a short (1–2 minute) simulated “live session” and provide simple, anonymous reactions by pressing on-screen buttons.
Please follow these steps:
Click the provided link to open the Blink reaction interface.
You will see three buttons:
🔴 Confusion – press when something seems unclear
🟢 Agree – press when you follow or agree
🟡 Attention – press when you want a recap or something stands out
During the session, press any button whenever the moment feels appropriate.
You may press multiple buttons throughout the session, but please wait ½ second between presses so the system can register them.
Once the session ends, return to this HIT page and submit the completion code.
Important:
There are no “correct answers.”
We are measuring reactions, not testing knowledge.
Please avoid spamming buttons; only press when it matches your reaction. ]

**Estimated time per task**: [1-2 minutes]
**Payment per task**: $[0]

**Number of tasks per HIT**: [1 task per HIT]

**Qualifications required**: [>95% approval rate, >100 completed HITs, US only]

---

## Technical Stack

### Technologies

**Frontend**: React

**Backend**: Node.js

**Database**: Supabase

**Crowdsourcing Platform**: Live audience members

**ML/AI Tools** (if applicable): Whisper/AssemblyAI for transcription (not yet decided)

**Hosting/Deployment**: Vercel

**Other tools**: [Any other important tools or services]

### Repository Structure

**Current structure**:
```
your-repo/
├── README.md
├── docs/
│   ├── flow-diagram.pdf
│   ├── mockups/
│   └── ...
├── src/
│   ├── qc/
│   ├── aggregation/
│   └── ...
├── data/
│   ├── raw/
│   ├── sample-qc-input/
│   ├── sample-qc-output/
│   ├── sample-agg-input/
│   └── sample-agg-output/
└── ...
```

**Explain any deviations**: [If your structure differs, explain why]

---

## Data Management

### Input Data

**Source**: Button clicks → {userId, timestamp, eventId}, audio recordings (optional)

**Format**: [JSON events sent via WebSocket,saved as.json files for analysis(one event per line)]

**Sample data location**: `data/raw/` 

**Sample data description**:
[contains synthetic button press timelines, data from small internal testing sessions, examples representing random noise (for QC testing)]

**How much data do you need?**
- For testing/development: [50-100 events (10-15 users pressing buttons during a simulated session]
- For your final demo/analysis: [300-500 events across 20-40 users]

**Data collection plan**:
[use Blink during short in class/ club demo sessions, supplement w/ synthetic event generators for stress testing, capture real sessions 1 wk before final demo to ensure fresh realistic data]

### QC Module Data

**Input location**: `data/sample-qc-input/`

**Input format**:
```
{ "sessionId": "abc123", "userId": "u1", "eventType": "confusion", "timestamp": 1731974038123, "deviceHash": "A1B2" }
{ "sessionId": "abc123", "userId": "u1", "eventType": "confusion", "timestamp": 1731974038124, "deviceHash": "A1B2" }
{ "sessionId": "abc123", "userId": "u2", "eventType": "agree",     "timestamp": 1731974039000, "deviceHash": "C9F1" }


```

**Output location**: `data/sample-qc-output/`

**Output format**:
```
{ "status": "ok", "sessionId": "abc123", "userId": "u1",
  "eventType": "confusion", "timestamp": 1731974038200 }
{ "status": "rejected", "reason": "rate_limit_exceeded", "userId": "u1" }

```

**Sample scenario documentation**:
[data/sample-qc-input/README.md explains: which events are intentionally malformed, which ones should be dropped by rate limit logic, how timestamp drift was simulated]

### Aggregation Module Data

**Input location**: `data/sample-agg-input/`

**Input format**:
```
[{ "sessionId": "abc123", "userId": "u1", "eventType": "confusion", "timestamp": 1731974038200 }
{ "sessionId": "abc123", "userId": "u2", "eventType": "agree",     "timestamp": 1731974039000 }
{ "sessionId": "abc123", "userId": "u3", "eventType": "attention", "timestamp": 1731974040200 }
]
```

**Output location**: `data/sample-agg-output/`

**Output format**:
```
[{
  "sessionId": "abc123",
  "summary": {
    "confusion": [
      { "count": 12, "timestamp": 1731974010000 },
      { "count": 18, "timestamp": 1731974075000 }
    ],
    "agree": [
      { "count": 7, "timestamp": 1731974042000 }
    ],
    "attention": [
      { "count": 4, "timestamp": 1731974098000 }
    ]
  },
  "updatedAt": 1731974100000
}

]
```

**Sample scenario documentation**:
[the README.md explains how many events were fed in, what time bins were used for aggregation, how peaks were identified]

### Data Dependencies

**Does your QC module output feed into your aggregation module?**
[Yes aggregation only runs on QC approved events bc they are timestamp corrected, rate limited, and device validated]

**Data flow between modules**:
[crown interface generates raw events → raw events → QC Module → QC outputs → clean-event-stream→cleaner events →aggregation module →aggregator produces timeline + summary data → results feed into the dashboard + replay view]

---

## Crowd Recruitment & Management

### Recruitment Strategy

**Where will workers come from?**
Workers will come directly from real classroom environments: students attending recitations, lectures, or demos. Primary sources include: TA friends’ recitations (pilot testing), professors who agree to use it in their class, and students enrolled in those sections (no account needed)

**How will you reach them?**
TA announcements at the start of recitation, professors introducing the tool at the beginning of lecture, a quick QR code or link projected on the screen that students can open on their phone, a short 10–15 second explanation of the purpose (“Press when confused so we can improve the lecture”)

**When will you recruit?**
Week 1–3 (Pilot recruitment through TA friends’ recitations), Week 4 onward (Recruitment through professors who consent to using it. Since students are already in the room, recruitment is immediate and participation is frictionless)

### Worker Incentives

**Compensation model**: 
- Payment per task: $0
- Estimated time per task: [1 minutes]
- Effective hourly rate: $[0/hour]

**Or alternative incentive**: [intrinsic motivation + lightweight gamification. Blink is designed for natural group settings like classrooms, meetings, workshops, etc. participants are motivated by wanting to actually do well/participate in whatever group setting it is. their feedback helps shape the lecture, low friction anon way to express confusion, people need to go to class anyways]

**Justification**: [this task is low effort, participants already benefit by allowing teachers to understand where in their lesson students need help, and students can anonymously express their confusion, no correctness is required, so the cognitive load is minimal]

### Scale Requirements

**For MVP/Demo**:
- Minimum workers needed: 5
- Minimum tasks completed: 3
- Timeline: By 1 week before presentation

**For Full Analysis**:
- Target workers: [30-50]
- Target tasks: [300-500 total presses]
- Timeline: [by a week before presenting this]

### Backup Plan

**If recruitment fails or is insufficient**:
- [ ] Use MTurk/paid workers (budget: $[amount])
- [X] Simplify task to require fewer workers
- [X] Use simulated/synthetic data
- [ ] Other: [specify]

---

## Project Milestones & Timeline

### Week-by-Week Plan

**Week 1 (Dates: [11/17 - 11/23])**
- Milestone: Finalize project design and create initial prototype, begin recruitment
- Tasks:
  - [ ] [Finalize Figma user flows, wireframes, and heatmap design] - [Emily]
  - [ ] [Set up initial database schema] - [Amber]
  - [ ] [Implement core backend endpoints for confusion clicks and audio upload] - [Mingni + Anika]
- Deliverable: Completed task design + working prototype + initial recruitment materials ready

**Week 2 (Dates: [11/24 - 11/30])**
- Milestone: Integrate frontend with backend and database, test prototype with mock data
- Tasks:
  - [ ] [Populate mock confusion and audio data for testing] - [All]
  - [ ] [Verify aggregation module (bin-based interval aggregation) works with mock data] - [Amber + Anika]
  - [ ] [Refine UI/UX based on testing feedback] - [Emily + Mingni]
- Deliverable: Stable integrated prototype using mock data; verified aggregation and heatmap functionality

**Week 3 (Dates: [12/1 - 12/7])**
- Milestone: Conduct pilot data collection with recruited audience and iterate
- Tasks:
  - [ ] Recruit TA friends / small group for pilot testing - [All]
  - [ ] Run pilot with real confusion clicks and optional audio recording - [All]
  - [ ] Aggregate pilot data and update heatmap visualization; implement minor fixes - [All]
- Deliverable: Pilot data collected, visualized, and system adjusted based on feedback

**Week 4 (Dates: [12/8 - 12/12])**
- Milestone: Finalize system and prepare presentation
- Tasks:
  - [ ] Final bug fixes and polish frontend/backend - [Anika + Amber]
  - [ ] Prepare presentation and system demo - [Emily + Mingni]
- Deliverable: Fully functional system with pilot data; final presentation and demo ready



### Critical Path

**Blocking dependencies** (what MUST be done before other work can proceed):
Database schema and backend endpoints must be completed before frontend integration and aggregation module testing.
Frontend UI/UX design and mock data setup must be done before pilot testing with real users.

**Parallel work** (what can be done simultaneously):
- Emily can refine UI/UX while Amber and Anika work on aggregation module verification.
- Mingni can implement additional backend features while Emily continues frontend improvements.

**Integration points** (when pieces must come together):
- 11/30: Frontend + backend + database must integrate with mock data for stable prototype testing
- 12/7: Backend + frontend + aggregation module must integrate with real pilot data for final visualization and system adjustments

---

## Risk Management

### Technical Risks

**Risk 1**: Incorrect binning or timestamp handling leads to inaccurate aggregation
- **Likelihood**: Medium
- **Impact**: High
- **Mitigation**: Add unit tests for bin calculations, validate timestamp formats, and log anomalies.
- **Backup plan**: Fall back to a simpler aggregation method (e.g., per-second counts) if binning proves unreliable.

**Risk 2**: Heatmap fails to render due to normalization or scale issues
- **Likelihood**: Low
- **Impact**: Medium
- **Mitigation**: Clamp values, add default scaling, and test on extreme cases (e.g., all zeros, sudden spikes).
- **Backup plan**: Provide a non-normalized count table or line plot as a temporary alternative visualization.

### Crowd-Related Risks

**Risk 1**: Not enough workers contribute clicks
- **Likelihood**: Medium
- **Impact**: High
- **Mitigation**: Provide incentive for participation (e.g. academic credit), offer clear instructions, and monitor participation in real time.
- **Backup plan**: Reduce the required number of clicks or supplement with synthetic test data to validate the pipeline.

**Risk 2**: Low-quality or spam clicks
- **Likelihood**: Medium
- **Impact**: High
- **Mitigation**: Implement QC filters (speed checks, duplicate clicks, obvious spam detection)
- **Backup plan**: Re-run tasks with stricter QC or require a minimum number of validated clicks before aggregation.



### Resource Risks

**Risk 1**: Budget overrun from additional task batches
- **Likelihood**: Medium
- **Impact**: Medium
- **Mitigation**: Set a spending cap, batch tasks efficiently, and monitor costs as tasks are completed.
- **Backup plan**: Reduce task size, shorten the audio segment, or run a smaller pilot version to stay within budget.

---

## Evaluation Plan

### What You'll Measure

**Primary metrics**:
1. Confusion capture rate: Percentage of confusion events accurately recorded per lecture. Measured by comparing pilot data to manual observation; target ≥90%
2. Heatmap accuracy: How well the heatmap reflects true confusion points. Measured by instructor feedback vs. actual events; target ≥85% agreement.
3. System responsiveness: Time between student click and data appearing on heatmap. Measured in seconds; target <2 seconds.

**Secondary metrics**:
1. Audio upload reliability: % of recordings successfully stored and available for download.
2. Transcription sync accuracy: How well timestamps match confusion points in transcripts (if reach goal implemented).

### Analysis Approach

**What questions will your analysis answer?**
1. Does real-time crowd feedback accurately reflect points of confusion or engagement during a session? 
2. How effective are quality control methods at reducing noise while preserving genuine data?
3. Which aggregated data display best highlights data trends?

**What comparisons will you make?**
- [ ] Compare crowd vs. expert performance
- [ ] Compare crowd vs. automated baseline
- [X] Compare different QC methods
- [X] Compare different aggregation methods
- [ ] Analyze cost/quality tradeoffs
- [ ] Other: [specify]

**Data you'll collect for analysis**:
- Timestamped button-press events: To understand when crowd reactions occur and aggregate the resulting data.
- Session metadata (topic, duration, number of attendees): To contextualize the data and control from confounding variables.
- QC flags (filtered, duplicated, invalid events): Allow comparison of different QC strategies and their impact on the final aggregated output.

**Analysis methods**:

We’ll evaluate the data using descriptive statistics (event frequency, clustering over time) and create visualizations like time-series plots, smoothed curves,and spiked detection graphs. We’ll compare QC and aggregation methods by tracking noise reduction, clarity of patterns, and signal stability. These analyses will help determine which method produces the most meaningful and interpretable insights for session organizers.

---

## Ethical Considerations

### Worker Treatment

**Fair compensation**: The attendees aren’t being forced to reveal any sensitive information, they have the choice of voicing their emotions during the session at times when they perhaps wouldn’t want to interrupt. Thus, they’re being compensated by having the opportunity to express emotions and ideas that may otherwise go amiss and having the host see their perspective.

**Informed consent**: The host can explain to the attendees that while their input is appreciated, it’s by no means mandatory. They can choose to express their emotions and ideas if they’d like.

**Rejection policy**: Work would be rejected if attendees spam (press the button multiple times unnecessarily)- we’d create a mechanism to lock them out of the system for a bit as punishment. The host might be able to (we’re still deciding on this part) block attendees from participating again if they spam, troll in the comments, etc.

### Data Ethics

**Privacy**: Only the host can see how many people were confused and at what points they were. No login/personal information is required and thus can’t be exchanged. Overall, no one can see who was confused at any point, just how many people were.

**Consent**: The host should verbally make the audience aware of what information is being exchanged. But in case they fail to adequately communicate this, we’ll add a short disclaimer at the beginning.

**Data storage**: The session insights will be stored in our backend in terms of number of confused attendees, timestamps of confusion, etc. Only the host will have access to these statistics and their corresponding displays.

### Potential Harms

**Could your project be misused?**: We don’t see a significant misuse possibility for this project. However, it could end up being counterproductive if the audience doesn’t take the effort seriously and spams/trolls.

**Could it cause harm?**: The most harm we can see our project causing is distracting people during an important learning session.

**Mitigation**: We’re trying to minimize the distraction by having the work needed for input be as small as possible.

---

## Documentation Standards

### Code Documentation

**Each module must include**:
- Docstrings for all functions/classes
- README in module directory
- Example usage
- Input/output format specifications

**Current documentation status**:
- [x ] QC module: [Fully documented / Partially documented / Not yet documented]
- [x ] Aggregation module: [Fully documented / Partially documented / Not yet documented]
- [ x] Other modules: [List status]

### Repository README

**Your main README.md must include**:
- [x ] Project overview and goals
- [x ] Setup instructions
- [ x] How to run the system
- [ x] Where to find QC and aggregation code
- [ x] Data format specifications
- [x ] Team member contacts
- [ x] License information

### Ongoing Documentation

**How will you keep documentation current?**
[We will maintain documentation as an active part of our development workflow rather than as a one-time deliverable. Our process includes: 1) documentation lives in the repo alongside the code, weekly review during class, and an update first mindset (update docs before coding the implementation)]

---

## Questions for Teaching Staff

### Technical Questions

1. Is real-time button pressing data transfer enough for especially large groups?
2. Are our plans for Supabase good given our intended architecture, or should we go harder/simpler for the MVP?
3. How much data quality control (ex: blocking users who spam/troll) is needed for a good MVP here?

### Scope Questions

1. Should we start with a single button for marking confusion, and then add features like customizable feedback? What are possible additions, and at what point would we be over-cluttering?
2. Given that the statistics dashboard is our main feature, should we focus on making it simpler and understandable for everybody, or more comprehensive and sleek?
3. Given the time we have to do this, does it make sense to generalize outside of lecture settings now, or should we only do that as an addition?

### Resource Questions

1. Should something cost us money, are we expected to pay out-of-pocket? Are there any free platforms you know of that wouldn’t compromise functionality that we could use?
2. Other than lectures and recitations- the main settings we’re considering- are there any other settings you’d recommend us testing in? Maybe somewhere outside of academia?

### Other Concerns

Is there a way more efficient than storing audiovisual data and tracking timestamps that you can think of for allowing the host to identify common confusion points?

---

## Commitment

**We commit to**:
- [X] Building a working prototype with functional QC and aggregation modules
- [X] Creating comprehensive documentation in our GitHub repository
- [X] Recruiting and managing a real crowd (or simulated crowd)
- [X] Collecting sufficient data for meaningful analysis
- [X] Meeting project milestones on schedule
- [X] Communicating proactively if we encounter blockers
- [X] Treating crowd workers ethically and fairly

**Team signatures**:

- basua [Anika Basu], [11/18/2025]
- emkang [Emily Kang], [11/18/2025]
- _________________________ [Name], [Date]
- _________________________ [Name], [Date]

---

## Submission Checklist

This submission **is a working document**. You may not have finalized all version (of the flow diagram, the sample data, etc.), which is **acceptable**.

Before submitting this proposal, verify you have:

- [X] Completed all sections of this template
- [X] Provided team availability for TA meetings
- [X] Listed team skills and learning needs
- [X] Included point values for all components (total 15-20)
- [X] Described detailed implementation timeline
- [X] Identified risks and mitigation strategies
- [X] Had all team members review and sign

Then:

- [ ] Set up GitHub repository with required directory structure
- [ ] Prepared questions for teaching staff
- [ ] Created flow diagram showing QC and aggregation modules
- [ ] Created mockups for all user-facing interfaces
- [ ] Added sample input/output data for QC module
- [ ] Added sample input/output data for aggregation module

**Submission method**:
- **You are able to make multiple successive submission to iterate, complete this proposal.**
- Pull request to `ideation-fall-2025` repository, in `round5_final` folder
- Should be in the root of your GitHub organization

**Submission deadline**: Thursday, Nov. 13 at 11:59PM ET
