# Final Project Proposal: 

**Team Name**: TripTuner
**Submission Date**: 11/13/2025  
**GitHub Organization**: [Link to your GitHub organization]

---

## Team Information

### Team Members

| Name | PennKey | Primary Role(s) | Secondary Skills |
|------|---------|----------------|------------------|
| Jevin Ta | jevinta | Frontend Dev, UI/UX | Python, Data Analysis |
| Sadia Rahman | rsadia | Frontend Dev, Backend Dev | Python, React, MongoDB |
| Liana Veerasamy | lianav | Web Dev, Fullstack, Backend, AI Simulation | Java, Python |
| Julia Zhuo | juzhuo | Aggregation, Analysis | R, Visualization |
| Arushi Agarwal | arushiga | Frontend Dev | Python, SQL, React, Open AI API, Java |

### Team Skills Inventory

**Skills we have:**
- Frontend: arushiga, jevinta, rsadia, lianav
- Backend: rsadia, lianav
- Data / Analysis: juzhuo, jevinta
- [Skill 4]: [Who has it - names/pennkeys]

**Skills we need to learn/acquire:**
- API integration (Google Places API or Foursquare): Needed for auto-filling trip location metadata. Learners: Liana, Sadia

- Leaderboard + Metrics Computation: Needed to compute trip “wrapped” and upvote-weighted user rankings. Learners: Julia, Jevin

- Moderation/QC automation (flagging low-effort data): Needed for quality control before aggregation. Learners: Arushi

**External resources we might need:**

- Google / Foursquare Places API — pending request
- Vercel/Render hosting — free tier
- MongoDB Atlas — free tier

### Team Availability for TA Meetings

**Week of 11/16:**

_List all time slots when the ENTIRE team can meet with a TA. Use Eastern Time. Format: Day, Time-Time_

- Monday: Never
- Tuesday: 6:00 PM - 9:00 PM
- Wednesday: 6:30 PM - 9:00 PM
- Thursday: 6:00 PM - 9:00 PM
- Friday: 9:00 AM to 12:00 PM and 3:00 PM to 6:00 PM

**Preferred meeting duration**: 60 min

**Meeting format preference**: [Zoom]

**Primary contact for scheduling**: [Arushi Agarwal and arushiga@sas.upenn.edu]

---

## Project Overview

### Project Connection to Round 4

**Round 4 Decision**: STAYING

**Original idea from**: [Round 1 - Jevin Ta, jevinta]

**How the idea evolved**: 
The original plan was to have people describe full length trip ideas for other individuals who don't know what to do on their vacations. However we found that there was no incentive for people to do this significant amount of work for others, and we didn't want to have to pay them, so we decided to shift to a Penn only approach. In addition, instead of helping specific people that needed recommendations, we turned our app into a platform on which people can simply upload what they did on a previous day, in a few bullet points and key locations, as inspiration for other people to be able to draw from.

Additionally, after talking to our professor, we decided that we need there to be an intrinsic value for people to post on our app even before there are a lot of reviews. We decided that we can tackle this in 2 ways. Firstly, we will create a 'monthly wrapped' that summarizes your favorite locations of visits. Moreover, we will create a leaderboard on which people who's trips have the most upvotes can be ranked. This creates a 'clout' incentive, as users will want to post to be able to showcase that they have visited lots of places in their 'wrapped' and to have the clout of being at the top of the leaderboard.  

[2-3 sentences describing the evolution]

### Problem Statement

Individuals at Penn often do not know what they can do for fun on days that they are free, and have to rely on other applications like Tiktok or Instagram to see viral restaurants/spots to visit. 

[2-3 sentences clearly describing the problem you're solving and why it matters]

### One-Sentence Pitch

If you have ever had a moment of free time in between the business of being a UPenn student, wouldn't it be helpful to see how other people spend their days off and where they went on their day trips? 

### Target Users

**End Users**: UPenn students

**Crowd Workers**: Other UPenn students and friends that we recruit to get enough baseline trip itineraries on the website

**Scale**: ~10 of each for a base-level usable platform

### Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [X] Other: Platform to crowdsource ideas amongst students, specific to travel within Philly/on-campus

---

## System Architecture

### Flow Diagram

_Required: Include a visual flow diagram showing the major components/stages of your project_

**Flow diagram location**: [Will include soon! We wrote it out on words]

Your flow diagram MUST clearly show:
- [ ] Where/when the crowd touches the data
- [ ] Your quality control module
- [ ] Your aggregation module
- [ ] Data flow between components
- [ ] What happens before crowd involvement
- [ ] What happens after crowd contribution

**If you haven't created it yet**: Describe in words the major components and their relationships:

Over **Week 1 (Nov 14–20)**, we will finalize the system architecture and data schema, set up the backend server and MongoDB cluster, and build the basic React frontend shell, so that by the end of the week we have an app that loads core pages and connects to the database. In **Week 2 (Nov 21–27)**, we will focus on core functionality: implementing the trip submission UI for bullet-point trips and locations, creating the corresponding POST/GET endpoints, and building the QC module that filters low-effort trips and validates locations, so that users can submit trips and have them accepted or rejected by QC. During **Week 3 (Nov 28–Dec 4)**, we will implement the upvote system on both frontend and backend, build the aggregation logic that ranks trips, computes monthly “wrapped” stats, and generates the leaderboard, and integrate these into the user dashboard so that we can see preliminary rankings over sample data. In **Week 4 (Dec 5–11)**, we will recruit 20-30 Penn students as our crowd to submit trips, run QC and aggregation on real data and debug any issues, and polish the UI/UX. In the **final week**, we will focus on evaluation and packaging: complete the analysis write-up using collected data, finalize documentation and README, and prepare the final demo and presentation with the working TripTuner prototype.

### Major System Components

_List all major components with point values (1-4) indicating implementation complexity. Total should be 15-20 points._

| Component | Description | Points | Owner(s) | Dependencies |
|-----------|-------------|--------|----------|--------------|
| Trip Submission UI | Students enter bullet-point trip summaries & locations | 3 | Jevin, Arushi | Basic frontend setup |
| Trip Database + API | Store/retrieve trips (MongoDB) | 3 | Sadia, Liana | Data model finalized |
| QC Module | Quality filtering: min length, location validation, low-effort detection | 4 | Arushi, Sadia | Trip DB |
| Aggregation Module | Rank trips + compute monthly wrapped + leaderboard | 4 | Julia, Liana | QC module output |
| Upvoting / Rating System | Simple UI + backend endpoints | 4 | Jevin, Arushi | Submission UI |
| User Dashboard | Shows feed, wrapped, leaderboard | 3 | Frontend team | Aggregation module |

**Total Points**: 20

**Point allocation rationale**: 
_If teaching staff questions your point distribution, explain your reasoning here_

### Detailed Workflow

_Step-by-step description of how your system works from start to finish_

1. **[Step 1]**: User onboarding & login - A UPenn student visits TripTuner, logs in with their Penn email, and a basic user profile is created/stored by the backend (name, class year, optional interests).
2. **[Step 2]**: Trip creation & submission - The student fills out the “Add a Trip” form on the frontend (trip title, date, 3–7 bullet points describing what they did, key locations, optional tags like “food,” “nature,” “cheap”) and submits; the frontend sends this payload to the backend API.
3. **[Step 3]**: Quality control check - The backend passes the new trip to the QC module, which automatically checks for minimum effort (enough bullet points/characters), required fields, location validity (basic format/API check), and low-quality or inappropriate content; if it fails, the user receives an error message explaining what to fix.
4. **[Step 4]**: Trip storage & feed update - If the trip passes QC, it is stored in the trips collection in the database, indexed by user and location, and becomes visible in the main trip feed and searchable lists for other students to browse.
5. **[Step 5]**: Crowd interaction (upvotes & saves) - Other UPenn students browse the trip feed, filter by tags/date/location, and interact with trips by upvoting ones they find helpful or saving them to their personal “wishlist”; these interactions are recorded as engagement events in the database.
6. **[Step 6]**: Aggregation (wrapped + leaderboard computation) - The aggregation module periodically (or on each new interaction) processes QC-approved trips and their engagement data to compute per-user stats (number of trips, distinct locations, most-visited spots) for the monthly “wrapped,” and global stats (top-rated trips, most active contributors) for the leaderboard, storing these summaries in dedicated collections.
7. **[Step 7]**: User dashboard & admin monitoring - When a student opens their dashboard, the frontend pulls their personalized wrapped, saved trips, and the current leaderboard from the aggregated data; in parallel, an admin view allows the team to review flagged trips, spot QC failures, and monitor overall system health and crowd activity.

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

1. How can we have an incentive to keep people using our product? Eg, you can keep track of "bad" trips
3. [Your question about recruitment, platforms]

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

- Sadia Rahman, 11/13/2025
- Liana Veerasamy, 11/13/2025
- Jevin Ta, 11/13/2025
- Arushi Agarwal, 11/13/2025
- Julia Zhuo, 11/13/2025

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
