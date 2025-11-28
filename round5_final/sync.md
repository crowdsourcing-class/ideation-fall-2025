# Final Project Proposal: Sync

**Team Name**: Sync 
**Submission Date**: 11/13  
**GitHub Organization**: https://github.com/xiaethan/sync

---

## Team Information

### Team Members

| Name | PennKey | Primary Role(s) | Secondary Skills |
|------|---------|----------------|------------------|
| Ethan Xia | ethanxia | Python, Data Analysis, API Integration | Visualization, SQL |
| Omar Pareja | pareja | Java, SQL, Python, API Integration | JavaScript, Database Design |
| Hugo Song | songh8 | [e.g., QC Module, Data Pipeline] | [e.g., Statistics, ML] |
| Yuxuan (Daniel) Tian | ytian27 | Typescript | API Integration |
| Eshaan Kaipa | ekaipa | QC Module, Data Analysis | API Integration, UI/UX |

### Team Skills Inventory

**Skills we have:**
- Python: ethanxia, 
- UI/UX: ethanxia, 
- Data management: ethanxia, 
- ML 
- Frontend prototyping
- User research & usability testing
- Model evaluation & tuning

**Skills we need to learn/acquire:**
- ios development: Most people use some sort of apple device, so we will have to launch our app using ios. - ethanxia
- Database/Cloud infrastructure: To store user profiles, logs, and app data reliably and securely. - pareja
- Production deployment & DevOps : to deploy our backend and dashboard (e.g., on Render/Heroku), manage environment variables/keys, and monitor basic uptime and logs. - songh8

**External resources we might need:**
- OpenAI API access: Needed for parsing, intent detection, and natural-language time extraction. - Status: acquired (free credits from class + team accounts)
- Apple Developer tools (Xcode + iOS simulator) : Required for testing the iMessage integration prototype and iOS UI flows - Status: acquired (free), no cost
- Render/Heroku hosting credits: For deploying our backend, APIs, and dashboard. – Status: pending; estimated cost: $5–$15 for the project duration
- Apple Messages API / iMessage App Extensions: Needed to prototype structured message interactions and integrate our assistant into group chats. – Status: pending; requires Apple Developer setup
- Figma (Prototyping + UI/UX): For designing mockups, interface flows, dashboard sketches, and interaction screens. – Status: acquired (free student plan)

### Team Availability for TA Meetings

**Week of [Date]:**

_List all time slots when the ENTIRE team can meet with a TA. Use Eastern Time. Format: Day, Time-Time_

- Monday: 4 PM - 5 PM 
- Tuesday: Not available
- Wednesday: After 4 PM
- Thursday: Not available
- Friday: 10 AM - 2 PM

**Preferred meeting duration**: 30 min

**Meeting format preference**: Either

**Primary contact for scheduling**: Ethan Xia (ethanxia@seas.upenn.edu)

---

## Project Overview

### Project Connection to Round 4

**Round 4 Decision**: Staying

**Original idea from**: Yuxuan Tian (ytian27), Hugo Song (songh8), Ethan Xia (ethanxia)

**How the idea evolved**: 
_Briefly describe how your project changed from its original conception through Rounds 1-4 to this final proposal_

Our idea began as a pretty broad exploration of basic crowdsourcing in Round 1 in order to improve everyday decision making and dispute resolution. As we added more and more people, we discussed using AI and the purpose of crowdsourcing as a part of our app. Eventually, we settled on iMessage integration with consensus-building as the core of the final proposal. 

### Problem Statement

_Refined from your Round 4 decision_

People frequently express interest in making plans or scheduling in group chats, but these ideas rarely materialize because coordinating availability and incorporating everybody’s preferences is extremely tedious. Our project solves this by turning unstructured chats and messages into structured crowdsourced data, automatically gathering preferences from all participants and coming up with the ultimate decision. This system makes social planning faster, fairer, and more likely to succeed. 

### One-Sentence Pitch

An AI-powered iMessage assistant that crowdsources group availability and preferences, and automatically generates the optimal time / plan for social hangouts. 

### Target Users

**End Users**: Friend groups, classmates, coworkers, club groups. 

**Crowd Workers**: The members of the group chats

**Scale**: This project is easily scalable, but we will test and implement using different sized groupchats. 

### Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [x] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

---

## System Architecture

### Flow Diagram

_Required: Include a visual flow diagram showing the major components/stages of your project_

**Flow diagram location**: flow-diagram.pdf

Your flow diagram MUST clearly show:
- [x] Where/when the crowd touches the data
- [x] Your quality control module
- [x] Your aggregation module
- [x] Data flow between components
- [x] What happens before crowd involvement
- [x] What happens after crowd contribution

**If you haven't created it yet**: Describe in words the major components and their relationships:

Raw text -> Parser -> QC Module -> Aggregation -> Final recommendation -> iMessage

### Major System Components

_List all major components with point values (1-4) indicating implementation complexity. Total should be 15-20 points._

| Component | Description | Points | Owner(s) | Dependencies |
|-----------|-------------|--------|----------|--------------|
| Messaging integration layer | Handles ingestion of gc messages| 3 | Omar | Initial message schema |
| Agent Orchestration | Coordinates the pipeline and detect intent | 4 | Hugo | Messaging integration layer |
| Parsing and normalization | Cleans and structures raw texts messages | 3 | Ethan | Messaging integration layer + schema definitions|
| Aggregation and QC module | Performs quality control on crowd inputs, aggregates responses into optimal final time and plan| 5| Daniel | Parsing module output |
| Dashboard | Shows all active polls, QC flags, agg results | 3 | Eshaan | Aggregation + QC outputs|

**Total Points**: 18

**Point allocation rationale**: 
_If teaching staff questions your point distribution, explain your reasoning here_

### Detailed Workflow

_Step-by-step description of how your system works from start to finish_

1. **User expresses planning intent**: A member of the group chat says something like “when can everyone do dinner?”
2. **Agent asks for availability**: The agent generates a structured prompt asking all participants for their preferred / available times
3. **Users respond in chat (or to a separate number)**: Each participant replies with natural-language availability 
4. **Parser extracts time and location info**: Parsing module converts replies into JSON with times, constraints, preferences, locations, etc.
5. **QC validates and flags inconsistencies**: QC module checks for contradictory or malformed responses, impossible times, missing entries, etc. 
6. **Aggregation computes best slot**: combines all validated availability inputs, resolving conflicts 
7. **Agent posts recommendation**: Agent sends final recommendation back into the group chat

### Human vs. Automated Tasks

| Task | Performed By | Justification |
|------|--------------|---------------|
| Providing availability | Human | Users provide the data and times that they are available|
| Parsing | Automated | Natural-language extraction of times/dates is consistent, fast, scalable. LLMs outperform humans here.|
| Fairness judgement | Human | Human social judgement is required for group norms, fairness concerns, etc.|
| Aggregation and QC | Automated | Once structured data is available, algorithms can compute overlaps and resolve conflicts|

---

## Quality Control Module

### QC Strategy Overview

Our QC strategy combines automated, rule-based validation with targeted human review for the few cases that automation cannot reliably resolve.
First, all messages are parsed into a standardized JSON schema (user id, raw text, parsed time windows, confidence scores, etc.). The QC module then runs a series of checks: it verifies that time ranges are syntactically valid, non-empty, and within a reasonable horizon; enforces simple constraints (for example, “end time must be after start time”); ensures that each user’s responses are internally consistent; and detects entries that differ sharply from the group pattern (for example, “available 24 hours every day” when most users provide narrow windows). These checks are fully automated and appropriate here because the data is already structured, the rules are explicit, and we expect to process many availability entries per group.
For cases where the model output or user message is ambiguous, the QC module exposes an escalation path instead of silently accepting bad data. Any entry with low confidence, conflicting parses, or signals of sarcasm or mixed intent is moved into a “flagged” list and surfaced back to the requesting user or group organizer. They can either correct the entry (for example, by re-answering a simplified prompt) or explicitly confirm it. In practice, this keeps most of the workload in the automated pipeline while reserving human judgment for the small fraction of edge cases where it actually matters.


### Specific QC Mechanisms

**Primary mechanism**: Rule based validation

**Implementation details**:
- Input format: JSON data with user-id, raw message, location, times, etc.
- Processing: verifies that all of the data is valid
- Output format: a separate json with the optimal time / recommendation along with a confidence rating.
- Threshold for acceptance: We can determine a minimum confidence score as well as a checking if the algorithm passes all the rules. 

**Additional mechanisms**:
- [ ] Gold standard questions
  - _How many? How distributed? Pass/fail criteria?_
- [x] Majority voting across multiple workers
  - Used only for ambiguous parses where confidence is low. If tie, we can escalate to human review
- [ ] Attention checks
  - _What types? How often?_
- [ ] Reputation system
  - _How do workers build reputation?_
- [ ] Statistical outlier detection
  - _What metrics? How handled?_
- [ ] Other: [specify and explain]

### QC Module Code Plan

**Location in repo**: src/qc/quality_control.py

**Key functions/classes**:
1. class QCValidator: class to run rule-based checks, confidence checks, and validation
2. runMajorityVote: function to aggregate multiple parses and output slot with confidence
3. detectOutliers: function to parse out outliers and flag unusual entries 

**Input data format**: 
```
JSON file: 
{
  "group_id": "g101",
  "messages": [
    {
      "user_id": "u123",
      "raw_message": "im good after 7 or anytime tmr morning",
      "parsed_slots": [
        {"start": "19:00", "end": "23:00", "conf": 0.88},
        {"start": "08:00", "end": "12:00", "conf": 0.74}
      ]
    }
  ]
}
```

**Output data format**:
```
{
  "validated_entries": [
    {
      "user_id": "u123",
      "clean_slots": [
        {"start": "19:00", "end": "23:00"},
        {"start": "08:00", "end": "12:00"}
      ],
      "status": "valid"
    }
  ],
  "flagged_entries": []
}

```

**Sample scenario**:
_Walk through a concrete example of your QC module in action_

First, user writes, “I’m free after 5 but can’t do evenings.” Parser will output 3 choices, 17:00-19:00, 17:00-18:00, 17:00-20:00 along with a confidence score. Then we compare to other inputs that users give and trigger a majority vote. Rule check that the winning time passes all the rules and return an output json. 

---

## Aggregation Module

### Aggregation Strategy Overview

Our data aggregation strategy centers on converting many individual availability inputs into a single, data-driven recommendation for the optimal meeting time. Each user contributes one or more validated availability windows, and the aggregation module computes where these windows overlap most strongly across the group. This process is fully automated and designed to handle ambiguity, partial responses, and variations in user participation. 

The aggregator we are implementing will integrate confidences and group level coverage metrics so that the final recommendation reflects not only majority preference but also data quality. This approach will be useful since the data can be noisy but user intent is still somewhat extractable at scale. 

### Aggregation Method

**Primary method**: Weighted overlap computation and majority voting

**Implementation details**:
- Input format: A list of all validated entries
- Processing: Convert and smooth scores over, then ranking entries based on a score. 
- Output format: Output json
- Handling edge cases: We will also implement human feedback. 

**Why this method**:
Weighted overlap aggregation is ideal for informal group scheduling because it reflects group preferences while remaining tolerant of noise and incomplete data. Unlike simple majority voting, this method accounts for the quality of each user’s contribution and can transform noisy language/data into a clean and interpretable score. This approach is appropriate because generally, iMessage data is unstructured and can be uniquely random where availability ranges differ. The weighted method can adapt to all of those conditions. 

### Aggregation Module Code Plan

**Location in repo**: src/aggregation/aggregate.py

**Key functions/classes**:
1. class AvailabilityGrid: class to convert validated time windows into a scoring grid
2. compute_weighted_scores: Applies confidence and reliability via computing the availability score for each time block 
3. find_optimal_slots: Identifies contiguous high-scoring blocks and ranks them and returns the optimal slots

**Input data format**:
```
JSON: 
[
  {
    "user_id": "u789",
    "clean_slots": [
      {"start": "09:00", "end": "11:00"},
      {"start": "14:00", "end": "16:00"}
    ],
    "confidence": 0.88,
    "reliability": 0.92
  }
]
```

**Output data format**:
```
{
  "top_slots": [
    {
      "start": "10:00",
      "end": "11:00",
      "group_score": 3.41,
      "participants_available": 5
    }
  ],
  "secondary_options": [...]
}
```

**Sample scenario**:
_Walk through a concrete example of your aggregation module in action_

Five users submit availability windows. The aggregation function will convert all times into blocks and compute the weighted availability score for each block, identifying the highest-scoring window block and output the optimal result via JSON. 

### Integration: QC ↔ Aggregation

**How do these modules interact?**
QC always runs first, ensuring that all data entering the aggregator is consistent and normalized into a standard format, which will make it much easier to parse. Then the aggregation function kicks in and actually computes everything. 

**Data flow diagram** (if different from main flow diagram):
Raw text -> Parser -> QC Module -> Aggregation -> Final recommendation

---

## User Interface & Mockups

### Interfaces Required

_You need mockups for ALL user-facing interfaces_

**For Crowd Workers:**
- [x] Task interface / HIT design
- [x] Instructions page
- [x] Training/qualification interface (if applicable)

**For End Users:**
- [x] Main interface
- [x] Results display
- [x] Any configuration/input screens

**For Administrators (your team):**
- [x] Dashboard/monitoring
- [x] Data management interface

### Mockup Details

**Mockup location**: mockups/mockup.pdf

**For each interface, describe**:

#### Interface 1: End User interface
- **User type**: End User
- **Purpose**: users send group chat data. 
- **Key elements**: Raw text, proposed parsed time windows
- **Mockup file**: mockups/main_interface.png
- **Notes**: UI intentionally simple

#### Interface 2: Result interface
- **User type**: End User
- **Purpose**: display the final result
- **Key elements**: Final result and options with score (maybe a visual timeline with overlaps)
- **Mockup file**: mockups/result.png
- **Notes**: Interpretability
#### Interface 3: Admin Dashboard
- **User type**: Admin
- **Purpose**: inspect raw messages, parsed outputs, QC rejections
- **Key elements**: entire pipeline, manual override
- **Mockup file**: mockups/admin.png
- **Notes**: N/A

### Task Design (for crowd workers)

**If using MTurk or similar platform:**

**HIT title**: N/A

**HIT description**: N/A

**Task instructions**: 
_Write the actual instructions workers will see. Be specific and clear._

N/A

**Example task**:
N/A

**Estimated time per task**: N/A

**Payment per task**: $N/A

**Number of tasks per HIT**: N/A

**Qualifications required**: N/A

---

## Technical Stack

### Technologies

**Frontend**: minimal HTML dashboard

**Backend**: Python using APIs

**Database**: SQLite or Postgres

**Crowdsourcing Platform**: class volunteers / personal groupchats

**ML/AI Tools** (if applicable): OpenAI API

**Hosting/Deployment**: Render/Heroku

**Other tools**: N/A

### Repository Structure

**Current structure**:
```
your-repo/
├── README.md
├── src/
│   ├── qc/
│   ├── aggregation/
│   └── ...
├── data/
│   ├── raw/
```

**Explain any deviations**: N/A

---

## Data Management

### Input Data

**Source**: Chat logs 

**Format**: JSON 

**Sample data location**: `data/sample_data/` 

**Sample data description**:
The sample dataset consists of short iMessage conversation snippets contributed by teammates. They propose a time and a location and contain metadata fields that is close to what we want the final product to do. 

**How much data do you need?**
- For testing/development: 50-200 messages
- For your final demo/analysis: ~500 messages

**Data collection plan**:
We will run the project with establishing multiple groupchats and rolling out to friends. 

### QC Module Data

**Input location**: `data/sample_qc_input/`

**Input format**:
```
{
  "conversation_id": "thread_001",
  "messages": [
    {
      "sender": "user_12",
      "timestamp": "2025-02-05T12:41:02Z",
      "content": "I'm free after 6",
      "metadata": { "source": "iMessage" }
    },
    {
      "sender": "user_12",
      "timestamp": null,
      "content": "free after 6",
      "metadata": {}
    }
  ]
}

```

**Output location**: `data/sample_qc_output/`

**Output format**:
```
{
  "conversation_id": "thread_001",
  "validated_messages": [
    {
      "sender": "user_12",
      "timestamp": "2025-02-05T12:41:02Z",
      "normalized_content": "I'm free after 6",
      "qc_flags": []
    }
  ],
  "qc_summary": {
    "dropped_messages": 1,
    "issues_detected": ["missing_timestamp", "duplicate_content"]
  }
}
```

**Sample scenario documentation**:
A README_QC.txt directory explains each sample file, the types of issues being tested (e.g., missing timestamps, inconsistent sender IDs, duplicate entries), and the intended QC outcomes. The corresponding files in data/sample_qc_output/ show how these issues are resolved or flagged.

### Aggregation Module Data

**Input location**: `data/sample_agg_input/`

**Input format**:
```
{
  "conversation_id": "thread_001",
  "validated_messages": [
    { "sender": "user_12", "normalized_content": "I'm free after 6" },
    { "sender": "user_23", "normalized_content": "6 works for me" }
  ]
}
```

**Output location**: `data/sample_agg_output/`

**Output format**:
```
{
  "conversation_id": "thread_001",
  "aggregated_availability": {
    "6pm": {
      "count": 2,
      "participants": ["user_12", "user_23"]
    }
  },
  "confidence_score": 0.92
}
```

**Sample scenario documentation**:
The README_AGG.txt explains how the validated QC outputs map to the aggregation fields. It also outlines how ambiguous or conflicting responses are handled and how final summary outputs should be interpreted in the dashboard.


### Data Dependencies

**Does your QC module output feed into your aggregation module?**
Yes, the QC module produces cleaned and validated data/messages that serve as the required inputs for the aggregation module. 

**Data flow between modules**:
Raw chat logs enter system -> QC module reads the raw data -> aggregation module takes QC data and calculates/generates aggregated result -> final result sent back to user/groupchat.

---

## Crowd Recruitment & Management

### Recruitment Strategy

**Where will workers come from?**
Class volunteers, friends, family, existing groupchats. 

**How will you reach them?**
Ask politely

**When will you recruit?**
Right now

### Worker Incentives

**Compensation model**: 
- Payment per task: $0
- Estimated time per task: 1 Minute
- Effective hourly rate: $0/hr

**Or alternative incentive**: intrinsic motivation

**Justification**: People want to do stuff with their friends / plan with their group. Using our app can help them coordinate plans with their friends better and easily organize everything. 

### Scale Requirements

**For MVP/Demo**:
- Minimum workers needed: 2
- Minimum tasks completed: 20-40 total messages
- Timeline: Dec 2nd

**For Full Analysis**:
- Target workers: 8-12 users
- Target tasks: ~100+ messages
- Timeline: December 9th

### Backup Plan

**If recruitment fails or is insufficient**:
- [ ] Use MTurk/paid workers (budget: $[amount])
- [ ] Simplify task to require fewer workers
- [x] Use simulated/synthetic data
- [ ] Other: [specify]

---

## Project Milestones & Timeline

### Week-by-Week Plan

**Week 1 (Dates: 11/16 - 11/22)**
- Milestone: Data Parsing Module
- Tasks:
  - [ ] Generic Parser - Ethan
  - [ ] JSON Analysis / data storage - Hugo
  - [ ] Backend API - Omar
- Deliverable: Finished data parsing module and organization in file

**Week 2 (Dates: 11/23 - 11/29)**
- Milestone: QC Module
- Tasks:
  - [ ] QC algorithm - Eshaan
  - [ ] QC statistics - Daniel
  - [ ] Data storage - Ethan
- Deliverable:Finished QC module and flagging statistics

**Week 3 (Dates: 11/30 - 12/6)**
- Milestone: Aggregation Module
- Tasks:
  - [ ] Aggregation algorithm - Hugo
  - [ ] Data storage / output- Omar
  - [ ] Testing - Daniel
- Deliverable: Finished aggregation module and sample product / tests

**Week 4 (Dates: 12/7 - 12/10)**
- Milestone: Testing / Final Product
- Tasks:
  - [ ] UI/UX  - Ethan
  - [ ] Overload testing - Eshaan
  - [ ] Edge case testing- Omar
- Deliverable: Final product

_Continue through your full timeline..._

### Critical Path

**Blocking dependencies** (what MUST be done before other work can proceed):
1. Data parsing + message normalization before QC
2. QC before Agg
3. Agg before final dashboard + crowd task design

**Parallel work** (what can be done simultaneously):
- [Person 1] can work on frontend mockups and html dashboard while [Person 2] works on backend parsing and QC logic

**Integration points** (when pieces must come together):
- [Nov 25-27]: Integrate parsing -> QC module -> aggregation
- Nov 29-Dec 1: backend API -> dashboard 
- Dec 2: finalized for demo

---

## Risk Management

### Technical Risks

**Risk 1**: Natural language parsing fails on slang or messy/unclear language
- **Likelihood**: Medium
- **Impact**: High
- **Mitigation**: User rule-based fallback patterns
- **Backup plan**: allow user input

**Risk 2**: QC or aggregation logic produces inconsistent or unexpected results
- **Likelihood**: Low/Medium
- **Impact**: Medium
- **Mitigation**: test components with edge cases
- **Backup plan**: Switch to simpler heuristics

### Crowd-Related Risks

**Risk 1**: Not enough people contribute to groupchat 
- **Likelihood**: Medium
- **Impact**: Medium
- **Mitigation**: recruit earlier/more people and volunteers
- **Backup plan**: Generate synthetic worker messages using GPT

**Risk 2**: Low-quality responses
- **Likelihood**: Medium
- **Impact**: High
- **Mitigation**:QC rule based checks and discard invalid messages
- **Backup plan**: Manually filter the dataset / require re-submission of tasks

### Resource Risks

**Risk 1**: N/A
- **Likelihood**: N/A
- **Impact**: N/A
- **Mitigation**: N/A
- **Backup plan**: N/A

---

## Evaluation Plan

### What You'll Measure

**Primary metrics**:
1. Parsing accuracy: % of worker messages where parser correctly extracts start time, end time, availability type. We should aim for a 90% accuracy rate. 
2. QC Effectiveness: % of low quality / inappropriate responses filtered out / flagged. We should aim for a 90% catch rate. 
3. Aggregation correctness: % agreement between the responses and the resulting output. This is our ‘score’ metric. 

**Secondary metrics**:
1. Worker disagreement rate: Proportion of responses that contradict others (overlap, inconsistent time formats)
2. Latency/pipeline run time: Total time from receiving chat logs to final recommendation. We should aim to minimize this AMAP

### Analysis Approach

**What questions will your analysis answer?**
1. How accurately can crowdsourced availability data be parsed and normalized from informal chat messages? 
2. Does the QC module meaningfully improve the final recommendation by removing inconsistent or malformed data? 
3. What type of aggregation method / algorithm yields the most reliable meeting suggestion under realistic worker disagreement? 

**What comparisons will you make?**
- [ ] Compare crowd vs. expert performance
- [x] Compare crowd vs. automated baseline
- [x] Compare different QC methods
- [x] Compare different aggregation methods
- [ ] Analyze cost/quality tradeoffs
- [ ] Other: [specify]

**Data you'll collect for analysis**:
- Crowd messages: this is our data, we need it for everything. 
- QC flags: Benchmarking our QC module
- Aggregated outputs: we can identify pipeline improvements

**Analysis methods**:
Accuracy rate, conflict rate, etc. We can plot all times available on a bar chart or confusion matrix, but I don’t think that this will be necessary. 

---

## Ethical Considerations

### Worker Treatment

**Fair compensation**: Workers will not be paid monetarily, but rather with the benefit from the result of our project. This is a win-win scenario because our project deals with naturally occurring conversations. It wouldn’t make sense to pay them on a response basis, but rather with the incentive of getting a response that benefits the entire group chat. 

**Informed consent**: We will have an acknowledgement file so that users know what they are consenting to. 

**Rejection policy**: Work will only be rejected during the QC module, or if a response is deemed inappropriate by our AI QC module. We can filter using sentiment/context analysis. 

### Data Ethics

**Privacy**: We will create a private database and delete user data after each response is generated. Since each response is only really relevant to that particular conversation, there is no need to permanently store all data. 

**Consent**: We will create an acknowledgement file so that users know what they are consenting to. 

**Data storage**: Data is stored in raw_data folder within project. 

### Potential Harms

**Could your project be misused?**: I don’t think so. It is relatively simple and moderated. 

**Could it cause harm?**: No

**Mitigation**: Emphasize on content moderation part. 

---

## Documentation Standards

### Code Documentation

**Each module must include**:
- Docstrings for all functions/classes
- README in module directory
- Example usage
- Input/output format specifications

**Current documentation status**:
- [x] QC module: Partially documented
- [x] Aggregation module: Partially documented
- [ ] Other modules: N/A

### Repository README

**Your main README.md must include**:
- [x] Project overview and goals
- [x] Setup instructions
- [x] How to run the system
- [x] Where to find QC and aggregation code
- [x] Data format specifications
- [x] Team member contacts
- [x] License information

### Ongoing Documentation

**How will you keep documentation current?**
We will continually update the README with the current flowchart and any updated changes. 

---

## Questions for Teaching Staff

### Technical Questions

1. [Your question about implementation, architecture, etc.]
2. [Your question about tools, platforms, etc.]
3. [Your question about technical approach]

### Scope Questions

1. Is implementing this on iMessage viable/simple? Would it be easier to just do this on a more documented API like discord or slack? 
2. Penn SSO? 
3. Is it possible to have a bot live in an iMessage groupchat or does this violate apples privacy concerns? Should we just have everyone text a separate number? 

### Resource Questions

1. How easily accessible is getting the apple developer tools? 

### Other Concerns

N/A

---

## Commitment

**We commit to**:
- [x] Building a working prototype with functional QC and aggregation modules
- [x] Creating comprehensive documentation in our GitHub repository
- [x] Recruiting and managing a real crowd (or simulated crowd)
- [x] Collecting sufficient data for meaningful analysis
- [x] Meeting project milestones on schedule
- [x] Communicating proactively if we encounter blockers
- [x] Treating crowd workers ethically and fairly

**Team signatures**:

- ____Ethan Xia, 11/18
- ____Omar Pareja, 11/18
- ____Hugo Song  , 11/18
- ____Yuxuan Tian, 11/18
- ____Eshaan Kaipa, 11/18
---

## Submission Checklist

This submission **is a working document**. You may not have finalized all version (of the flow diagram, the sample data, etc.), which is **acceptable**.

Before submitting this proposal, verify you have:

- [x] Completed all sections of this template
- [x] Provided team availability for TA meetings
- [x] Listed team skills and learning needs
- [x] Included point values for all components (total 15-20)
- [x] Described detailed implementation timeline
- [x] Identified risks and mitigation strategies
- [x] Had all team members review and sign

Then:

- [x] Set up GitHub repository with required directory structure
- [x] Prepared questions for teaching staff
- [x] Created flow diagram showing QC and aggregation modules
- [x] Created mockups for all user-facing interfaces
- [x] Added sample input/output data for QC module
- [x] Added sample input/output data for aggregation module

**Submission method**:
- **You are able to make multiple successive submission to iterate, complete this proposal.**
- Pull request to `ideation-fall-2025` repository, in `round5_final` folder
- Should be in the root of your GitHub organization

**Submission deadline**: Thursday, Nov. 13 at 11:59PM ET

