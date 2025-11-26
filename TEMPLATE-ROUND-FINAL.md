# Final Project Proposal: [Project Title]

**Team Name**: [Your team name]  
**Submission Date**: [Date]  
**GitHub Organization**: [Link to your GitHub organization]

---

## Team Information

### Team Members

| Name | PennKey | Primary Role(s) | Secondary Skills |
|------|---------|----------------|------------------|
| [Name 1] | [pennkey1] | [e.g., Frontend Dev, UI/UX] | [e.g., Python, Data Analysis] |
| [Name 2] | [pennkey2] | [e.g., Backend Dev, API Integration] | [e.g., JavaScript, Database Design] |
| [Name 3] | [pennkey3] | [e.g., QC Module, Data Pipeline] | [e.g., Statistics, ML] |
| [Name 4] | [pennkey4] | [e.g., Aggregation, Analysis] | [e.g., R, Visualization] |

### Team Skills Inventory

**Skills we have:**
- [Skill 1]: [Who has it - names/pennkeys]
- [Skill 2]: [Who has it - names/pennkeys]
- [Skill 3]: [Who has it - names/pennkeys]
- [Skill 4]: [Who has it - names/pennkeys]

**Skills we need to learn/acquire:**
- [Skill 1]: [Why we need it] - [Who will learn it]
- [Skill 2]: [Why we need it] - [Who will learn it]
- [Skill 3]: [Why we need it] - [Who will learn it]

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

**Meeting format preference**: [In-person / Zoom / Either]

**Primary contact for scheduling**: [Name and email]

---

## Project Overview

### Project Connection to Round 4

**Round 4 Decision**: [STAYING / PIVOTING / JOINING / NEW]

**Original idea from**: [Round 1/2/3 author(s) - names/pennkeys]

**How the idea evolved**: 
_Briefly describe how your project changed from its original conception through Rounds 1-4 to this final proposal_

[2-3 sentences describing the evolution]

### Problem Statement

_Refined from your Round 4 decision_

[2-3 sentences clearly describing the problem you're solving and why it matters]

### One-Sentence Pitch

[Your project in one compelling sentence]

### Target Users

**End Users**: [Who will use/benefit from the system?]

**Crowd Workers**: [Who will contribute to the crowdsourcing tasks?]

**Scale**: [How many of each do you need for a successful demo?]

### Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
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

**Risk 1**: [Describe technical challenge/uncertainty]
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High]
- **Mitigation**: [How you'll prevent or address it]
- **Backup plan**: [What you'll do if mitigation fails]

**Risk 2**: [Describe technical challenge/uncertainty]
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High]
- **Mitigation**: [How you'll prevent or address it]
- **Backup plan**: [What you'll do if mitigation fails]

### Crowd-Related Risks

**Risk 1**: [e.g., Can't recruit enough workers]
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High]
- **Mitigation**: [How you'll prevent or address it]
- **Backup plan**: [What you'll do if mitigation fails]

**Risk 2**: [e.g., Low quality contributions]
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High]
- **Mitigation**: [How you'll prevent or address it]
- **Backup plan**: [What you'll do if mitigation fails]

### Resource Risks

**Risk 1**: [e.g., Budget overrun]
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High]
- **Mitigation**: [How you'll prevent or address it]
- **Backup plan**: [What you'll do if mitigation fails]

---

## Evaluation Plan

### What You'll Measure

**Primary metrics**:
1. [Metric 1]: [How measured, target value]
2. [Metric 2]: [How measured, target value]
3. [Metric 3]: [How measured, target value]

**Secondary metrics**:
1. [Metric 1]: [How measured]
2. [Metric 2]: [How measured]

### Analysis Approach

**What questions will your analysis answer?**
1. [Research question 1]
2. [Research question 2]
3. [Research question 3]

**What comparisons will you make?**
- [ ] Compare crowd vs. expert performance
- [ ] Compare crowd vs. automated baseline
- [ ] Compare different QC methods
- [ ] Compare different aggregation methods
- [ ] Analyze cost/quality tradeoffs
- [ ] Other: [specify]

**Data you'll collect for analysis**:
- [Data type 1]: [Why you need it]
- [Data type 2]: [Why you need it]
- [Data type 3]: [Why you need it]

**Analysis methods**:
[Describe statistical tests, visualizations, or other analysis approaches]

---

## Ethical Considerations

### Worker Treatment

**Fair compensation**: [How you ensure workers are fairly paid/compensated or derive value from what they are doing?]

**Informed consent**: [How workers understand what they're contributing to]

**Rejection policy**: [Under what circumstances would work be rejected?]

### Data Ethics

**Privacy**: [How you protect worker and user privacy]

**Consent**: [How you obtain and document consent]

**Data storage**: [Where/how data is stored, who has access]

### Potential Harms

**Could your project be misused?**: [Consider potential negative applications]

**Could it cause harm?**: [Consider who might be negatively affected]

**Mitigation**: [How you'll prevent or minimize potential harms]

---

## Documentation Standards

### Code Documentation

**Each module must include**:
- Docstrings for all functions/classes
- README in module directory
- Example usage
- Input/output format specifications

**Current documentation status**:
- [ ] QC module: [Fully documented / Partially documented / Not yet documented]
- [ ] Aggregation module: [Fully documented / Partially documented / Not yet documented]
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
[Describe your process for maintaining docs as code evolves]

---

## Questions for Teaching Staff

### Technical Questions

1. [Your question about implementation, architecture, etc.]
2. [Your question about tools, platforms, etc.]
3. [Your question about technical approach]

### Scope Questions

1. [Your question about whether something is in/out of scope]
2. [Your question about project complexity]
3. [Your question about realistic goals]

### Resource Questions

1. [Your question about budget, tools, access]
2. [Your question about recruitment, platforms]

### Other Concerns

[Any other questions, concerns, or areas where you need guidance]

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
- _________________________ [Name], [Date]

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