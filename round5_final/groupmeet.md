# Final Project Proposal: GroupMeet

**Team Name**: GroupMeet 
**Submission Date**: 11/13/2025  
**GitHub Organization**: https://github.com/orgs/GroupMeet/repositories

---

## Team Information

### Team Members

| Name | PennKey | Primary Role(s) | Secondary Skills |
|------|---------|----------------|------------------|
| Alexander Mehta | amehta26 | [e.g., Frontend Dev, UI/UX] | [e.g., Python, Data Analysis] |
| Brandon Yan | bdonyan | Backend Dev, API Integration | Database Design |
| Connor Cummings | connorcc | [e.g., QC Module, Data Pipeline] | [e.g., Statistics, ML] |
| Nikki Liu | nikkiliu | [e.g., Aggregation, Analysis] | Python, Data Analysis, Visualization |

### Team Skills Inventory

**Skills we have:**
- [Skill 1]: [Who has it - names/pennkeys]
- Database design and Backend Dev: Brandon Yan/bdonyan
- [Skill 3]: [Who has it - names/pennkeys]
- Python scripting: Nikki Liu/nikkiliu

**Skills we need to learn/acquire:**
- Simple data storage (Firebase, Google Sheets API, or equivalent): Needed to store form submissions cleanly and safely - [Who will learn it]
- Basic engagement tracking (e.g., counting open rates, clickthroughs): Needed to measure match completion and validate our Week 1 test - Nikki will learn it
- Email automation or result-delivery tooling: Needed to send match results at scale via email or auto-generated dashboards - [Who will learn it]

**External resources we might need:**
- [Resource 1]: [e.g., Specific API access, dataset, tool] - [Status: requested/pending/acquired]
- [Resource 2]: [e.g., Paid service credits] - [Status and cost estimate]

### Team Availability for TA Meetings

**Week of [Date]:**

_List all time slots when the ENTIRE team can meet with a TA. Use Eastern Time. Format: Day, Time-Time_

- Monday: [e.g., 2:00 PM - 4:00 PM, 6:00 PM - 8:00 PM]
- Tuesday: [e.g., 10:00 AM - 12:00 PM]
- Wednesday: [e.g., 3:00 PM - 5:00 PM]
- Thursday: [Not available]
- Friday: [e.g., 1:00 PM - 3:00 PM]

**Preferred meeting duration**: [30 min / 45 min / 60 min]

**Meeting format preference**: Zoom

**Primary contact for scheduling**: [Name and email]

---

## Project Overview

### Project Connection to Round 4

**Round 4 Decision**: PIVOTING

**Original idea from**: Instructor-proposed project

**How the idea evolved**: 
In Rounds 1–3 I worked on TerraTruth, an ambitious humanitarian mapping project that combined geospatial pipelines, AI pre-filtering, and volunteer crowdsourcing. After seeing the viability scores and feedback, I pivoted in Round 4 to GroupMeet, an instructor idea with a much tighter scope and a directly testable crowd loop. For the final proposal, we further narrowed GroupMeet to a single-course pilot with a simple form-based matcher and lightweight feedback survey so we can validate the matching loop end-to-end within one semester.

### Problem Statement

Penn students in medium and large classes often struggle to find reliable, compatible study partners; existing tools like GroupMe, Discord, and ad-hoc Piazza posts are noisy, unstructured, and don’t account for schedule constraints or working styles. As a result, many students either work alone or end up in ineffective groups, which hurts learning outcomes and sense of belonging in the course. GroupMeet addresses this by collecting structured data about course enrollment, availability, and study preferences, then using crowdsourced feedback on each match to iteratively improve future group formation.

### One-Sentence Pitch

GroupMeet is a lightweight web platform that matches Penn students into study groups based on class, availability, and study preferences, then uses quick feedback surveys to continuously improve match quality.

### Target Users

**End Users**: Penn students enrolled in medium-to-large lecture courses who want better-matched study groups.

**Crowd Workers**: The same Penn students, acting as the crowd by submitting their course/availability information and later rating the quality of their study groups via short feedback forms.

**Scale**: For a successful demo we aim for ~30–40 student participants total, with at least 25 unique form submissions, 8–12 study groups formed, and 20+ feedback responses across one or two pilot courses.

### Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [X] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

---

## System Architecture

### Flow Diagram

_Required: Include a visual flow diagram showing the major components/stages of your project_

**Flow diagram location**: [e.g., `docs/flow-diagram.pdf` or embed image here]

Your flow diagram MUST clearly show:
- [ ] Where/when the crowd touches the data
- [ ] Your quality control module
- [ ] Your aggregation module
- [ ] Data flow between components
- [ ] What happens before crowd involvement
- [ ] What happens after crowd contribution

**If you haven't created it yet**: Describe in words the major components and their relationships:

1. [Component 1] → [Component 2] → [Component 3] ...

### Major System Components

_List all major components with point values (1-4) indicating implementation complexity. Total should be 15-20 points._

| Component | Description | Points | Owner(s) | Dependencies |
|-----------|-------------|--------|----------|--------------|
| [Component 1] | [Brief description] | [1-4] | [Name(s)] | [What must be done first] |
| [Component 2] | [Brief description] | [1-4] | [Name(s)] | [What must be done first] |
| [Component 3] | [Brief description] | [1-4] | [Name(s)] | [What must be done first] |
| [Component 4] | [Brief description] | [1-4] | [Name(s)] | [What must be done first] |
| [Component 5] | [Brief description] | [1-4] | [Name(s)] | [What must be done first] |

**Total Points**: [Sum - should be 15-20]

**Point allocation rationale**: 
_If teaching staff questions your point distribution, explain your reasoning here_

### Detailed Workflow

_Step-by-step description of how your system works from start to finish_

1. **[Step 1]**: [What happens, who/what does it]
2. **[Step 2]**: [What happens, who/what does it]
3. **[Step 3]**: [What happens, who/what does it]
4. **[Step 4]**: [What happens, who/what does it]
5. **[Step 5]**: [What happens, who/what does it]
6. **[Step 6]**: [What happens, who/what does it]
7. **[Step 7]**: [What happens, who/what does it]

_Continue as needed..._

### Human vs. Automated Tasks

| Task | Performed By | Justification |
|------|--------------|---------------|
| [Task 1] | Human | [Why human intelligence is required] |
| [Task 2] | Automated | [Why this can/should be automated] |
| [Task 3] | Human | [Why human intelligence is required] |
| [Task 4] | Automated | [Why this can/should be automated] |

---

## Quality Control Module

### QC Strategy Overview

[Describe your quality control approach in 2-3 paragraphs. Why is this approach appropriate for your project?]

### Specific QC Mechanisms

**Primary mechanism**: [e.g., Gold standard questions, Majority voting, Expert review]

**Implementation details**:
- Input format: [What does QC module receive?]
- Processing: [What does it do?]
- Output format: [What does it produce?]
- Threshold for acceptance: [How do you decide if work is "good enough"?]

**Additional mechanisms**:
- [ ] Gold standard questions
  - _How many? How distributed? Pass/fail criteria?_
- [ ] Majority voting across multiple workers
  - _How many workers per task? Tie-breaking?_
- [ ] Attention checks
  - _What types? How often?_
- [ ] Reputation system
  - _How do workers build reputation?_
- [ ] Statistical outlier detection
  - _What metrics? How handled?_
- [ ] Other: [specify and explain]

### QC Module Code Plan

**Location in repo**: [e.g., `src/qc/quality_control.py`]

**Key functions/classes**:
1. [Function/class name]: [Purpose]
2. [Function/class name]: [Purpose]
3. [Function/class name]: [Purpose]

**Input data format**: 
```
[Describe or show example of input data structure]
```

**Output data format**:
```
[Describe or show example of output data structure]
```

**Sample scenario**:
_Walk through a concrete example of your QC module in action_

[Example: "Worker A labels image as 'cat', Worker B labels as 'dog', Worker C labels as 'cat'. QC module applies majority voting, outputs 'cat' with confidence 0.67, flags disagreement for potential review."]

---

## Aggregation Module

### Aggregation Strategy Overview

[Describe your aggregation approach in 2-3 paragraphs. How will you combine multiple crowd contributions?]

### Aggregation Method

**Primary method**: [e.g., Majority voting, Weighted averaging, EM algorithm, ML-based filtering]

**Implementation details**:
- Input format: [What does aggregation module receive?]
- Processing: [What does it do?]
- Output format: [What does it produce?]
- Handling edge cases: [What if there's a tie? Not enough data? Conflicting information?]

**Why this method**:
[Justify why this aggregation approach is appropriate for your project and data type]

### Aggregation Module Code Plan

**Location in repo**: [e.g., `src/aggregation/aggregate.py`]

**Key functions/classes**:
1. [Function/class name]: [Purpose]
2. [Function/class name]: [Purpose]
3. [Function/class name]: [Purpose]

**Input data format**:
```
[Describe or show example of input data structure]
```

**Output data format**:
```
[Describe or show example of output data structure]
```

**Sample scenario**:
_Walk through a concrete example of your aggregation module in action_

[Example: "10 workers rate restaurant review sentiment. Scores: 7 positive, 2 negative, 1 neutral. Aggregation weights by worker reliability scores, outputs 0.82 positive sentiment with confidence interval."]

### Integration: QC ↔ Aggregation

**How do these modules interact?**
[Describe the relationship. Does QC happen before aggregation? After? Iteratively? Do they share data structures?]

**Data flow diagram** (if different from main flow diagram):
[Location or description]

---

## User Interface & Mockups

### Interfaces Required

_You need mockups for ALL user-facing interfaces_

**For Crowd Workers:**
- [ ] Task interface / HIT design
- [ ] Instructions page
- [ ] Training/qualification interface (if applicable)

**For End Users:**
- [ ] Main interface
- [ ] Results display
- [ ] Any configuration/input screens

**For Administrators (your team):**
- [ ] Dashboard/monitoring
- [ ] Data management interface

### Mockup Details

**Mockup location**: [e.g., `docs/mockups/` folder or links to Figma/Marvel/etc.]

**For each interface, describe**:

#### Interface 1: [Name]
- **User type**: [Crowd worker / End user / Admin]
- **Purpose**: [What is this interface for?]
- **Key elements**: [What must be visible/interactive?]
- **Mockup file**: [filename or link]
- **Notes**: [Any important design decisions or requirements]

#### Interface 2: [Name]
- **User type**: [Crowd worker / End user / Admin]
- **Purpose**: [What is this interface for?]
- **Key elements**: [What must be visible/interactive?]
- **Mockup file**: [filename or link]
- **Notes**: [Any important design decisions or requirements]

_Continue for all interfaces..._

### Task Design (for crowd workers)

**If using MTurk or similar platform:**

**HIT title**: [Your HIT title]

**HIT description**: [What workers will see in the HIT listing]

**Task instructions**: 
_Write the actual instructions workers will see. Be specific and clear._

[Your instructions here]

**Example task**:
[Show workers exactly what one complete task looks like]

**Estimated time per task**: [X minutes]

**Payment per task**: $[amount]

**Number of tasks per HIT**: [number]

**Qualifications required**: [e.g., >95% approval rate, >100 HITs, US location]

---

## Technical Stack

### Technologies

**Frontend**: [e.g., React, Vue, vanilla JS, none (MTurk only)]

**Backend**: [e.g., Python/Flask, Node.js/Express, Django]

**Database**: [e.g., PostgreSQL, MongoDB, Firebase, SQLite]

**Crowdsourcing Platform**: [e.g., MTurk, custom, social media, class volunteers]

**ML/AI Tools** (if applicable): [e.g., scikit-learn, TensorFlow, OpenAI API]

**Hosting/Deployment**: [e.g., Heroku, AWS, Vercel, local]

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

**Source**: [Where will your input data come from?]

**Format**: [File type, structure, schema]

**Sample data location**: `data/raw/` 

**Sample data description**:
[Describe what sample data you've gathered and what it represents]

**How much data do you need?**
- For testing/development: [amount]
- For your final demo/analysis: [amount]

**Data collection plan**:
[How and when will you gather the full dataset?]

### QC Module Data

**Input location**: `data/sample-qc-input/`

**Input format**:
```
[Show example structure - can be JSON, CSV, etc.]
```

**Output location**: `data/sample-qc-output/`

**Output format**:
```
[Show example structure]
```

**Sample scenario documentation**:
[In your data/ directory, include a README explaining the sample QC data]

### Aggregation Module Data

**Input location**: `data/sample-agg-input/`

**Input format**:
```
[Show example structure]
```

**Output location**: `data/sample-agg-output/`

**Output format**:
```
[Show example structure]
```

**Sample scenario documentation**:
[In your data/ directory, include a README explaining the sample aggregation data]

### Data Dependencies

**Does your QC module output feed into your aggregation module?**
[Yes/No and explain the relationship]

**Data flow between modules**:
[Describe how data moves through your system]

---

## Crowd Recruitment & Management

### Recruitment Strategy

**Where will workers come from?**
[Be specific: MTurk? Class volunteers? Social media? Where exactly?]

**How will you reach them?**
[Describe your recruitment approach]

**When will you recruit?**
[Timeline for recruitment activities]

### Worker Incentives

**Compensation model**: 
- Payment per task: $[amount]
- Estimated time per task: [X minutes]
- Effective hourly rate: $[amount/hour]

**Or alternative incentive**: [e.g., course credit, gamification, intrinsic motivation]

**Justification**: [Why this incentive structure will work]

### Scale Requirements

**For MVP/Demo**:
- Minimum workers needed: [number]
- Minimum tasks completed: [number]
- Timeline: [when you need this by]

**For Full Analysis**:
- Target workers: [number]
- Target tasks: [number]
- Timeline: [when you need this by]

### Backup Plan

**If recruitment fails or is insufficient**:
- [ ] Use MTurk/paid workers (budget: $[amount])
- [ ] Simplify task to require fewer workers
- [ ] Use simulated/synthetic data
- [ ] Other: [specify]

---

## Project Milestones & Timeline

### Week-by-Week Plan

**Week 1 (Dates: [X/X - X/X])**
- Milestone: [Major goal for this week]
- Tasks:
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
- Deliverable: [What will be done/ready by end of week]

**Week 2 (Dates: [X/X - X/X])**
- Milestone: [Major goal for this week]
- Tasks:
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
- Deliverable: [What will be done/ready by end of week]

**Week 3 (Dates: [X/X - X/X])**
- Milestone: [Major goal for this week]
- Tasks:
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
- Deliverable: [What will be done/ready by end of week]

**Week 4 (Dates: [X/X - X/X])**
- Milestone: [Major goal for this week]
- Tasks:
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
  - [ ] [Specific task] - [Owner]
- Deliverable: [What will be done/ready by end of week]

_Continue through your full timeline..._

### Critical Path

**Blocking dependencies** (what MUST be done before other work can proceed):
1. [Task A] must be done before [Task B, Task C]
2. [Task X] must be done before [Task Y]

**Parallel work** (what can be done simultaneously):
- [Person 1] can work on [X] while [Person 2] works on [Y]

**Integration points** (when pieces must come together):
- [Date]: [What components must integrate]
- [Date]: [What components must integrate]

---

## Risk Management

### Technical Risks

**Risk 1**: Matching logic produces uneven or low-quality groups (e.g., leftover students, conflicting availability).
- **Likelihood**: Medium
- **Impact**: Medium
- **Mitigation**: Keep the form extremely constrained (course, coarse availability blocks, one study preference) and test the script with small synthetic datasets before real signups.
- **Backup plan**: Allow flexible group sizes (3–6), or place unmatched students into a secondary “overflow” round instead of forcing bad matches.

**Risk 2**: Email distribution script fails or messages are flagged by university spam filters.
- **Likelihood**: Low
- **Impact**: High
- **Mitigation**: Test email-sending with internal emails first (team + friends) and send messages in small batches to avoid rate limits.
- **Backup plan**: Provide each student with a unique link to a results dashboard instead of sending the actual match details via email.

### Crowd-Related Risks

**Risk 1**: Not enough students sign up to form viable groups if no professor agrees to distribute the form.
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High]
- **Mitigation**: [How you'll prevent or address it]
- **Backup plan**: [What you'll do if mitigation fails]

**Risk 2**: Low-quality responses or participants not following through (ghosting their assigned group).
- **Likelihood**: Medium
- **Impact**: Medium
- **Mitigation**: Make the form very short and specific (e.g. max 3-5 questions, including “problem sets vs. concept review”) to increase match compatibility and reduce friction.
- **Backup plan**: Send a quick confirmation (“Still want to be matched? Yes/No”) before running the matching script to filter out passive or uncommitted participants.

### Resource Risks

**Risk 1**: Running out of time because the MVP requires more implementation effort than expected.
- **Likelihood**: Medium
- **Impact**: High
- **Mitigation**: Keep the scope tightly limited to the essentials (form, matching script, results email) and avoid adding optional features until the core pipeline works.
- **Backup plan**: If timing slips, simplify further by using a Google Form and a lightweight manual matching script to ensure the Week 1 and Week 2 tests still happen.

---

## Evaluation Plan

### What You'll Measure

**Primary metrics**:
1. Signup Rate: Percentage of students in the target class who complete the preference form. How measured: Form submissions ÷ estimated class size. Target: ≥ 15% of a large intro course (e.g., CIS 1200). 
2. Match Completion Rate: Percentage of matched students who open their results email/dashboard. How measured: Email open rates + unique page visits. Target: ≥ 70% engagement.
3. Group Quality Rating: Students’ self-reported satisfaction with their group. How measured: 1–5 star rating submitted 5 days after matching. Target: Average rating ≥ 3.5 stars.

**Secondary metrics**:
1. Form Completion Time: Measured automatically by timestamp difference; used to confirm form is short and frictionless.
2. Group Dropoff Indicators: Counts of participants who report their group never met or who request to be rematched.

### Analysis Approach

**What questions will your analysis answer?**
1. Was recruitment through professors sufficient to generate meaningful participation?
2. Did the simple matching rules (course + availability + preference) produce functional study groups?
3. What user characteristics (e.g., availability type, study preference) correlate with higher satisfaction?

**What comparisons will you make?**
- [ ] Compare crowd vs. expert performance
- [ ] Compare crowd vs. automated baseline
- [✓] Compare different QC methods
- [✓] Compare different aggregation methods
- [✓] Analyze cost/quality tradeoffs
- [ ] Other: [specify]

**Data you'll collect for analysis**:
- Form submissions: Needed to evaluate signup rate, preference distribution, and matching logic performance.
- Match engagement data: Email open rates, click-throughs, and page visits to measure completion and participation.
- Follow-up ratings: Necessary to quantify group quality and evaluate whether matching rules worked.

**Analysis methods**:
- Descriptive statistics (means, proportions) for signup rate, engagement, and ratings.
- Visualizations: bar charts of group quality ratings mainly; funnel charts of user dropoff; heatmaps of availability overlap.
- Simple correlation analysis between study preferences or availability types and satisfaction scores.
- Qualitative analysis of optional free-text feedback to identify failure cases or improvement opportunities.

---

## Ethical Considerations

### Worker Treatment

**Fair compensation**: Not applicable in the traditional “crowd worker” sense - students derive direct value (study partners) rather than monetary compensation.

**Informed consent**: The form and recruitment email clearly state the project purpose, what information is collected, and how it will be used (to create effective study groups only).

**Rejection policy**: No work is “rejected”—all submissions are accepted unless the form is incomplete or empty. Students may be notified if they cannot be matched due to incompatible availability.

### Data Ethics

**Privacy**: Only group members see each other’s emails; no sensitive data (e.g., grades, IDs) is collected. All data is stored in secure, access-controlled files.

**Consent**: Consent is obtained explicitly through the form, which states that participation is voluntary and used solely for this 2-week academic pilot.

**Data storage**: Stored in secure Google Drive or Firebase with limited access; deleted at the end of the project or anonymized for analysis.

### Potential Harms

**Could your project be misused?**: Minimal risk; the most plausible misuse is sharing student emails beyond intended group members.

**Could it cause harm?**: Potential discomfort if a student is matched into an incompatible or inactive group.

**Mitigation**: Limit shared information to first/last name and email; allow students to opt out anytime; run a confirmation step before matching; and avoid storing unnecessary data.

---

## Documentation Standards

### Code Documentation

**Each module must include**:
- Docstrings for all functions/classes
- README in module directory
- Example usage
- Input/output format specifications

**Current documentation status**:
- [ ] QC module: Not yet documented
- [ ] Aggregation module: Not yet documented
- [ ] Other modules: [List status]

### Repository README

**Your main README.md must include**:
- [ ] Project overview and goals
- [ ] Setup instructions
- [ ] How to run the system
- [ ] Where to find QC and aggregation code
- [ ] Data format specifications
- [ ] Team member contacts
- [ ] License information

### Ongoing Documentation

**How will you keep documentation current?**
- Update docstrings whenever logic changes.
- Require that any new script or feature includes a README section before merging.
- Maintain a simple “Changelog” documenting weekly updates to matching rules or form schema.

---

## Questions for Teaching Staff

### Technical Questions

1. Are simple rule-based matching algorithms sufficient for this project, or do you expect experimentation with multiple aggregation methods?
2. Is there a recommended way to track email open/click metrics within course-allowed tools (Firebase, scripts, etc.)?
3. For collecting ratings, is it acceptable to use Google Forms, or must everything be integrated into the web app?

### Scope Questions

1. Is running a pilot on one large course enough to satisfy the crowdsourcing requirement?
2. How lightweight can the results dashboard be while still meeting course standards?
3. Is it acceptable if the feedback survey is optional due to time constraints?

### Resource Questions

1. Are there any free email-sending services you recommend that won’t get flagged by university spam filters?
2. Are there guidelines for acceptable recruitment channels if professor partnership fails?

### Other Concerns

- How strictly should we limit data retention after the project ends?
- Is it okay to anonymize ratings for analysis, or is identified data preferred?

---

## Commitment

**We commit to**:
- [ ] Building a working prototype with functional QC and aggregation modules
- [ ] Creating comprehensive documentation in our GitHub repository
- [ ] Recruiting and managing a real crowd (or simulated crowd)
- [ ] Collecting sufficient data for meaningful analysis
- [ ] Meeting project milestones on schedule
- [ ] Communicating proactively if we encounter blockers
- [ ] Treating crowd workers ethically and fairly

**Team signatures**:

- _________________________ [Name], [Date]
- _________________________ [Name], [Date]
- _________________________ [Name], [Date]
- Nikki Liu, 11/13/2025

---

## Submission Checklist

This submission **is a working document**. You may not have finalized all version (of the flow diagram, the sample data, etc.), which is **acceptable**.

Before submitting this proposal, verify you have:

- [ ] Completed all sections of this template
- [ ] Provided team availability for TA meetings
- [ ] Listed team skills and learning needs
- [ ] Included point values for all components (total 15-20)
- [ ] Described detailed implementation timeline
- [ ] Identified risks and mitigation strategies
- [ ] Had all team members review and sign

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
