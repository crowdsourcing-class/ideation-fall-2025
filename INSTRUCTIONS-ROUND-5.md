# NETS 2130 – Final Project Proposal – Spring 2025

## Overview

You've completed the ideation phase (Rounds 1-4) and made your project decision. Now it's time to transition from ideas to implementation. The Final Proposal bridges the gap between "what we want to build" and "how we'll build it."

**This is not just paperwork** – this document will become your project's blueprint and will force you to think through details before you're debugging at 2am wondering why nothing works.

---

## Why This Matters

In Round 4, you picked a project. Great. But "build a crowdsourced system for X" is not a plan. This proposal forces you to answer:

- **How will the pieces actually fit together?** (Flow diagram)
- **What will users actually see?** (Mockups)  
- **How will you ensure quality?** (QC module)
- **How will you combine noisy crowd data?** (Aggregation module)
- **Who's doing what, and when?** (Timeline and roles)
- **What could go wrong?** (Risks and backup plans)

By the end of this, you'll have:
1. A clear technical architecture
2. Sample data formats for all modules
3. Team coordination infrastructure
4. Realistic timeline and milestones
5. TA meeting scheduled to validate your plan

---

## What You're Submitting

### 1. Completed Final Proposal Template

Use `TEMPLATE-ROUND-FINAL.md` and complete **every section**. This includes:

#### Core Technical Components
- **Flow diagram** showing all system components
- **Mockups** for all user interfaces (crowd workers, end users, admins)
- **QC module plan** with sample input/output data
- **Aggregation module plan** with sample input/output data
- **Technical stack** and architecture decisions

#### Project Management
- **Component breakdown** with point values (15-20 total)
- **Week-by-week timeline** with specific tasks and owners
- **Risk assessment** with mitigation strategies
- **Evaluation plan** describing your analysis approach

#### Team Coordination
- **Skills inventory** (what you have, what you need)
- **Team availability** for TA meetings (specific time slots)
- **Role assignments** for all major components

### 2. GitHub Repository Setup

Your repository must have this structure:

```
your-repo/
├── README.md                    # Overview and setup instructions
├── docs/
│   ├── flow-diagram.pdf         # System architecture diagram
│   ├── mockups/                 # All UI mockups
│   │   ├── worker-interface.png
│   │   ├── end-user-interface.png
│   │   └── ...
│   └── FINAL-PROPOSAL.md        # Your completed proposal
├── data/
│   ├── raw/                     # Sample input data
│   ├── sample-qc-input/         # Example QC module input
│   ├── sample-qc-output/        # Example QC module output
│   ├── sample-agg-input/        # Example aggregation input
│   ├── sample-agg-output/       # Example aggregation output
│   └── README.md                # Data format documentation
└── src/
    ├── qc/                      # Quality control code (when ready)
    ├── aggregation/             # Aggregation code (when ready)
    └── ...
```

**Critical**: The `data/` directory must include **sample data** showing the format for QC and aggregation modules, even if you don't have code yet. Include a README explaining each sample file.

---

## The Flow Diagram

This is **required** and **non-negotiable**. Your flow diagram must show:

1. **All major system components** as boxes/nodes
2. **Data flow** between components (arrows)
3. **Where the crowd enters** the system
4. **Your QC module** (clearly labeled)
5. **Your aggregation module** (clearly labeled)
6. **What's automated vs. human** (use different colors/styles)

**Tools you can use**:
- Lucidchart, draw.io, Miro, Figma
- PowerPoint/Google Slides (yes, really)
- Hand-drawn and photographed (if legible)
- Code that generates a diagram

**Bad flow diagram**: Input → Crowd → Output  
**Good flow diagram**: Shows specific data transformations, decision points, QC steps, aggregation logic, error handling

**Where to save it**: `docs/flow-diagram.pdf` (or `.png`, `.jpg`)

---

## The Mockups

You need mockups for **every interface** a human will see:

### For Crowd Workers
- The actual task interface (HIT on MTurk, web form, mobile app, etc.)
- Instructions page
- Training/qualification interface (if applicable)

### For End Users
- Main interface
- Results display
- Any input/configuration screens

### For Admins (Your Team)
- Dashboard for monitoring progress
- Data management interface (if applicable)

**Fidelity**: These don't need to be pixel-perfect. Wireframes are fine. But they should clearly show:
- What information is displayed
- What actions users can take
- What the workflow looks like

**Tools**: Figma, Adobe XD, Balsamiq, Marvel, PowerPoint, hand-drawn

**Where to save them**: `docs/mockups/` directory with descriptive filenames

---

## Sample Data: The Critical Piece Everyone Forgets

You need **example data** showing exactly what your QC and aggregation modules will work with. This is how you discover format mismatches before they break your system.

### For QC Module

Create files showing:

**Input** (`data/sample-qc-input/`):
- What raw crowd contributions look like
- Multiple examples showing variation
- Edge cases (conflicts, missing data, outliers)

**Output** (`data/sample-qc-output/`):
- What the QC module produces
- Quality scores, flags, filtered results
- Whatever your aggregation module needs next

### For Aggregation Module

Create files showing:

**Input** (`data/sample-agg-input/`):
- What goes into aggregation (often QC output)
- Multiple responses for the same item
- Varying quality/confidence scores

**Output** (`data/sample-agg-output/`):
- Final aggregated results
- Confidence intervals, consensus, etc.
- Whatever format your end users need

### Data README

Your `data/README.md` must explain:
- Format of each file (JSON schema, CSV columns, etc.)
- How files relate to each other
- How to interpret the sample scenarios
- Any assumptions or constraints

**Example scenario to include**: Walk through one complete data flow from raw input → QC → aggregation → final output, showing the transformations at each step.

---

## Component Points: Preventing Scope Disaster

Every major component gets 1-4 points based on complexity:

- **1 point**: Simple, well-defined, straightforward
- **2 points**: Moderate complexity, some unknowns
- **3 points**: Complex, requires new learning or integration
- **4 points**: Very complex, significant technical risk

**Your project should total 15-20 points.** 

- <15 points: Too simple, won't demonstrate sufficient learning
- >20 points: Overscoped, will fail or compromise quality

**In your TA meeting**, we'll scrutinize these points. Be prepared to defend them or adjust.

**Example point distributions**:

*Underscoped (12 points)*:
- MTurk HIT (1) + Simple web form (2) + Majority voting QC (2) + Basic aggregation (2) + Results page (2) + Database (3) = **12 points** ⚠️

*Well-scoped (18 points)*:
- Custom worker interface (3) + Training module (2) + Gold standard QC (3) + Reputation system (2) + EM aggregation (4) + Admin dashboard (2) + API integration (2) = **18 points** ✓

*Overscoped (24 points)*:
- Mobile app (4) + Real-time collaboration (3) + ML-based QC (4) + Multiple aggregation methods (3) + Complex gamification (3) + Social features (3) + Analytics dashboard (4) = **24 points** ⚠️

---

## Timeline and Roles

### Week-by-Week Breakdown

For each week remaining in the semester:
1. **Milestone**: What's the main goal?
2. **Tasks**: Specific, actionable items
3. **Owners**: Who's responsible (by name)
4. **Dependencies**: What must be done first
5. **Deliverable**: What's ready by end of week

**Be specific**. Not "work on backend" but "implement user authentication API (Jane), set up PostgreSQL database (Bob), create API documentation (Alice)."

### Critical Path Analysis

Identify:
- **Blocking dependencies**: What MUST happen in sequence
- **Parallel work**: What can happen simultaneously
- **Integration points**: When separate pieces must come together

This helps you spot bottlenecks and plan around them.

---

## Skills Inventory

### What You Have

List every relevant skill on your team:
- Programming languages
- Frameworks and tools
- Platform experience (MTurk, AWS, etc.)
- Domain expertise
- Design skills
- Data analysis capabilities

**For each skill, note who has it**. This helps with task assignment.

### What You Need

Be honest about gaps:
- Technologies you'll need to learn
- Tools you'll need to figure out
- Expertise you might need to acquire

**For each gap**:
- Why you need it
- Who will learn it
- How you'll get up to speed (tutorials, documentation, TA help)
- Backup plan if learning takes too long

**External resources**: List anything you need that's outside your team:
- API access (OpenAI, Google, etc.)
- Paid services (AWS, Heroku)
- Datasets (where will you get them?)
- Domain experts (for validation)

---

## Team Availability and TA Meetings

### Your Availability

Provide **specific time slots** when your **entire team** can meet with a TA:

✅ **Good**:
- Monday: 2:00 PM - 4:00 PM
- Tuesday: 10:00 AM - 12:00 PM, 6:00 PM - 7:30 PM
- Friday: 1:00 PM - 3:00 PM

❌ **Not Helpful**:
- "We're flexible"
- "Afternoons work"
- "Sometime next week"

Include:
- Preferred meeting length (30/45/60 min)
- Format preference (in-person/Zoom/either)
- Primary contact for scheduling

### TA Meeting Purpose

This is **not a check-in**. This is a **technical review** where we:

1. Validate your scope (15-20 points)
2. Identify technical risks
3. Spot missing dependencies
4. Challenge unrealistic assumptions
5. Suggest alternatives or simplifications

**Come prepared to**:
- Walk through your flow diagram
- Explain your QC and aggregation approach
- Defend your component point assignments
- Discuss your timeline and potential blockers
- Ask specific technical questions

**Meeting structure** (example 45-min meeting):
- 0-5 min: Project overview (elevator pitch)
- 5-10 min: Walk through flow diagram
- 10-20 min: Deep dive on QC and aggregation
- 20-30 min: Timeline and risk discussion
- 30-35 min: Technical questions from you
- 35-40 min: Feedback and adjustments
- 40-45 min: Next steps and action items

---

## Common Pitfalls to Avoid

### 1. "We'll figure it out later"
❌ No data format specifications  
✅ Sample data files with documented schemas

### 2. "It's just like the demo we saw"
❌ Vague references to similar projects  
✅ Specific architectural decisions based on your context

### 3. "Quality control is just majority voting"
❌ One-line QC description  
✅ Detailed QC strategy with edge case handling

### 4. "We'll all just work on everything"
❌ No task ownership  
✅ Clear responsibilities for each component

### 5. "The crowd will come from social media"
❌ Vague recruitment plan  
✅ Specific platforms, timeline, incentive structure

### 6. "We'll use machine learning"
❌ Complexity for complexity's sake  
✅ ML only if necessary and you have the skills

### 7. Scope Creep
❌ "Also we want to add..."  
✅ "For MVP we're building X, Y, Z only"

---

## Evaluation and Success Metrics

You need to plan now for how you'll evaluate your project later.

### Define Success

**Primary metrics** (3-5):
- Accuracy (if applicable)
- Cost per result
- Time to complete
- Worker satisfaction
- Quality of output

**For each metric**:
- How will you measure it?
- What's your target value?
- What data do you need to collect?

### Analysis Plan

**Research questions**:
- What will your analysis answer?
- What comparisons will you make?
- What insights do you hope to gain?

**Data collection**:
- What data must you capture during the project?
- How will you store it?
- What might you need for analysis later?

**Start collecting metadata now**: timestamps, worker IDs, task completion times, revision history, etc. You can't go back and get this later.

---

## Ethical Considerations

### Worker Treatment

- **Fair pay**: Are workers earning at least minimum wage? Or are they getting intrinsic value from contributing to your project?
- **Informed consent**: Do they understand what they're contributing to?
- **Rejection policy**: Under what circumstances would you reject work?
- **Communication**: How will workers reach you with questions/problems?

### Data Ethics

- **Privacy**: How will you protect worker and user privacy?
- **Consent**: How will you document consent for data use?
- **Storage**: Where will data live? Who has access?
- **Retention**: How long will you keep data? What's your deletion plan?

### Potential Harms

**Ask yourself**:
- Could this project be misused?
- Who might be negatively affected?
- Are there unintended consequences?
- How will you mitigate potential harms?


---

## Questions for Teaching Staff

Use the "Questions for Teaching Staff" section to:

### Technical Questions
- Architecture decisions you're uncertain about
- Tool/platform selection
- Implementation approaches

### Scope Questions  
- "Is X in scope?"
- "Should we include Y?"
- "Is our point distribution reasonable?"

### Resource Questions
- Budget for crowd workers
- Access to tools/APIs
- Data sources

**Don't wait for the TA meeting to ask these**. Email questions ahead if possible.

---

## Submission Process

### 1. Complete the Template

Fill out `TEMPLATE-ROUND-FINAL.md` with all required sections.

### 2. Set Up Repository

Create the directory structure:
- `/docs` with flow diagram and mockups
- `/data` with sample input/output files
- `/src` (can be empty for now, but should exist)

### 3. Submit Pull Request

**File location**: `final-proposals/[team-name].md`

**PR description should include**:
- Team name and members
- Link to GitHub repository
- Confirmation that all required files are in place
- Your team's availability for TA meetings

### 4. Schedule TA Meeting

After your PR is reviewed, you'll schedule a meeting with your assigned TA/POC.

---

## Timeline

**Proposal Due**: Nov. 13, 11:59PM ET (initial draft) 
**TA Meetings**: To be booked after proposal
**Revised Proposal Due** (after TA feedback): Nov. 20, 11:59PM ET

---

## Grading Rubric

**This proposal is worth [X]% of your final grade.**

### Technical Architecture (40%)
- Flow diagram clearly shows all components and data flow
- QC module is well-defined with sample data
- Aggregation module is well-defined with sample data
- Technical stack is appropriate and justified
- Component point distribution is reasonable (15-20 total)

### Planning and Organization (30%)
- Timeline is detailed with specific tasks and owners
- Skills inventory is complete and honest
- Risk assessment identifies real concerns with mitigation
- Repository structure follows requirements

### Interfaces and User Experience (15%)
- Mockups exist for all required interfaces
- Task design is clear and well-specified
- Instructions for crowd workers are comprehensive

### Feasibility and Scope (15%)
- Project is appropriately scoped for one semester
- Evaluation plan is concrete and achievable
- Ethical considerations are thoughtfully addressed
- Team clearly understands requirements

### Penalties
- Missing required sections: -5% per section
- No flow diagram: -15%
- No mockups: -10%
- No sample data: -10%
- Late submission: Per course pollicy

---

## Getting Help

### Before You're Stuck
- Review past course projects in `/past-projects`
- Check the STEELMAN-ANALYSIS.md for ideation guidance
- Use RUBRIC-PROJECT-VIABILITY.md to self-assess

### When You're Stuck
- Email your assigned TA/POC
- Post in class Slack (without sharing project details publicly)
- Come to office hours

### Red Flags to Watch For
- "We're not sure how the QC will work yet"
- "We'll decide on the tech stack later"
- "We don't have sample data yet"
- "We're still figuring out the timeline"

If you're saying any of these, **you're not ready to submit**. That's what this proposal is for – figuring these things out now.

---

## Final Thoughts

This proposal is **not busy work**. It's your project blueprint. Teams that rush through this document struggle throughout the semester. Teams that think carefully about it catch problems early.

**The goal is not to have a perfect plan** – it's to have a well-thought-out plan that you can adapt as you learn more.

**The goal is not to predict the future** – it's to think through the technical challenges while you still have time to adjust.

**The goal is not to impress us** – it's to convince us (and yourselves) that you can actually build this in one semester.

Good luck. 🚀

---

## Resources

- `TEMPLATE-ROUND-FINAL.md` - The template you'll complete
- `past-projects/` - See what previous teams built
- `RUBRIC-PROJECT-VIABILITY.md` - Self-assessment rubric
