


# Crowdsourcing Project Idea: GatherMessageAI

## Authors

**Original Author:**  Yuxuan Tian (ytian27)
**Round 2 Contributors:**  Hugo Song (songh8)
**Round 3 Contributors:** Ethan Xia (ethanxia), Connor Cummings (connorcc)
---
## Problem Statement
Coordinating social gatherings among friends is surprisingly difficult. Ideas like “we should grab dinner soon” often appear in group chats but rarely become real plans due to busy schedules, indecision, and lack of follow-up. The process of checking everyone’s availability and agreeing on an activity or time is tedious and often abandoned. GatherAI aims to turn casual chat intent into concrete, data-driven social plans through lightweight crowdsourcing.
---
## Target Audience
**End Users:**  
Friend groups, roommates, classmates, coworkers, and social circles that communicate primarily via iMessage or group chat but struggle to make plans efficiently.
**Crowd Workers:**  
The users themselves — each participant contributes availability, preferences, and votes that collectively determine the final plan.
**Stakeholders:**  
Messaging platforms (e.g., Apple, Meta), third-party app developers, and venue recommendation partners (restaurants, event organizers) who benefit from improved group coordination.
---
## Description
GatherAI is an AI-powered group-chat assistant that integrates directly into iMessage or similar messaging apps. When it detects planning intent (e.g., “brunch this weekend?”), it launches a quick, structured poll asking for each member’s availability, preferred activities, and locations. The system aggregates the crowd’s input using a weighted consensus algorithm to find the optimal plan and sends confirmations and calendar invites. By automating the logistics, GatherAI converts fragmented chat suggestions into real events — making social coordination effortless, democratic, and fun.
---
## Project Type
- [ ] Human computation algorithm  
- [ ] Social science experiment with the crowd  
- [x] Tool for crowdsourcing (requesters or workers)  
- [ ] Business idea using crowdsourcing  
- [ ] Other: [  ]
---
## Key Features
1. **iMessage Integration** – Seamless participation within existing chat platforms.  
2. **Intent Detection** – Uses lightweight NLP to identify when a group chat expresses a planning intent.  
3. **Crowdsourced Scheduling** – Each user contributes their availability and activity preferences.  
4. **Smart Poll Generation** – Automatically generates structured polls based on chat content.  
5. **Consensus Scoring Algorithm** – Aggregates votes using weighted availability and preference overlap.  
6. **AI-Based Recommendations** – Suggests venues, activities, and times based on past data and preferences.  
7. **Privacy-Preserving Design** – Processes chat text locally or through minimal metadata collection.  
8. **Follow-Up Automation** – Sends reminders, confirmations, and optional calendar invites.  
9. **Gamification Layer** – Badges and streaks for users who frequently organize or respond.  
10. **Analytics Dashboard (optional)** – Visualizes crowd participation and group coordination efficiency.
---
## Feasibility: Crowd & Resources
**Where will your crowd workers come from?**  
GatherAI leverages naturally occurring crowds — friends in chat groups. Recruitment occurs organically as users invite others in their social circles to join the AI thread.
**What will they provide?**  
Crowd members provide their availability, votes on activity options, and reactions to final plans (confirmations, rejections, or suggestions).
**What skills do they need?**  
Only basic texting and response skills — no technical or platform-specific expertise required.
**Do skills vary widely? How?**  
Some users are more responsive or decisive than others. GatherAI accounts for this by weighting votes based on reliability and participation history.
**How will you incentivize participation?**  
- **Intrinsic:** Users benefit directly when plans succeed.  
- **Social:** Peer visibility and social accountability drive responses.  
- **Gamified:** Badges (“Organizer,” “Quick Responder”) and streak tracking.  
- **Optional:** Integration with rewards or event discounts (future feature).
**Budget & Cost Analysis:**
- Estimated cost per task: $0 (user input is voluntary)  
- Estimated cost per worker: $0  
- Number of tasks: ~500 interactions across test groups  
- Total estimated budget: <$500  
- Justification: Free-tier APIs, minimal hosting, and optional incentives keep costs within course constraints.
**Where will your data come from?**  
User-generated data (poll responses, preferences, confirmations). Optional integration with Apple Calendar or Google Calendar APIs for scheduling metadata.
**Scale Requirements:**
- Minimum viable crowd size: 3–5 participants per group chat  
- Target crowd size: 200 users across ~40 groups  
- Potential to scale to: 10,000+ users through viral group adoption
---
## Technical Architecture
**System Components:**
1. Frontend: iMessage Extension / Web UI for non-Apple users  
2. Backend: Python (FastAPI) for API logic  
3. Database: Firebase or Supabase for storing anonymized scheduling data  
4. NLP Layer: OpenAI API for intent detection  
5. Notification System: Twilio or Apple Messages API  
6. Aggregation Engine: Custom consensus-scoring algorithm
**Detailed Workflow:**
1. The AI detects a planning intent in a chat message.  
2. The system automatically generates a quick poll (e.g., “When are you free this weekend?”).  
3. Participants reply in-chat or via a link with their preferences.  
4. The backend aggregates all responses using weighted consensus logic.  
5. GatherAI proposes the top time and activity combination.  
6. The system sends a summary with an optional calendar invite and reminder.
**Human vs. Automated Tasks:**
| Task | Performed By | Why? |
|------|---------------|------|
| Provide availability | Human | Individual schedule knowledge |
| Parse chat intent | Automated | NLP efficiency and speed |
| Aggregate results | Automated | Scale and mathematical optimization |
| Confirm plans | Human | Requires social agreement |
| Suggest activities | Hybrid | AI provides options; humans vote |
**Technologies & Tools:**
- Frontend: React (Web), iMessage Shortcuts API  
- Backend: Python (FastAPI)  
- Database: Firebase / Supabase  
- AI/NLP: OpenAI GPT API  
- Hosting: Vercel or AWS (Free Tier)  
- Notification: Twilio API / Apple Messages SDK
**Aggregation Method:**
Weighted majority voting combining availability overlap and preference scores. Reliability weighting adjusts influence based on response history (users who reply consistently are given slightly more weight).
---
## Quality Control
**Quality Control Strategy:**  
Since contributions come from small, trusted social groups, quality assurance focuses on accuracy and responsiveness rather than truthfulness. The system validates structured data formats and encourages consensus resolution through reminders.
**Specific QC Mechanisms:**
- [x] Majority voting across multiple workers  
  - _Each decision (time, activity) requires at least 3 unique responses._  
- [x] Reputation/qualification systems  
  - _Frequent, consistent responders receive higher influence weights._  
- [x] Statistical outlier detection  
  - _Extreme or conflicting inputs are down-weighted._  
- [ ] Expert review or verification  
  - _Not applicable due to social context._  
- [ ] Attention checks  
  - _Implicit via responsiveness tracking._
**Handling Low-Quality Work:**  
Unresponsive users’ inputs are excluded from aggregation after reminders. Misformatted responses trigger clarifying prompts (“Did you mean Saturday or Sunday?”).
---
## Evaluation & Success Metrics
**Primary Success Metrics:**
1. **Plan Completion Rate:** ≥75% of AI-generated plans reach consensus and occur successfully.  
2. **Response Latency:** Average response time <1 hour per user.  
3. **User Satisfaction:** ≥80% positive survey feedback after event completion.  
4. **Engagement:** ≥50% of users participate in ≥2 events per month.
**Evaluation Methodology:**
Pilot the system with 5–10 friend groups over 2 weeks. Collect data on participation rate, response times, and plan finalization. Conduct post-event surveys to assess satisfaction.
**Baseline Comparisons:**
- Compare GatherAI to manual coordination (no AI):  
  - **Baseline success:** ~30% of chat-initiated plans materialize.  
  - **Target improvement:** ≥2.5× increase in successful coordination.
**Success Criteria:**
- Minimum viable success: 3+ groups using system weekly  
- Target success: 75% plan consensus rate  
- Stretch success: 1,000+ total users coordinating via GatherAI
---
## Challenges & Mitigation Strategies
**Challenge 1:** Low user response rate  
- **Why it’s a risk:** Planning fails if people ignore polls.  
- **Mitigation strategy:** Gamify responses; add reminder pings and group-level incentives.  
- **Backup plan:** Allow plan initiators to finalize based on partial consensus.
**Challenge 2:** Privacy concerns  
- **Why it’s a risk:** Users may fear chat monitoring.  
- **Mitigation strategy:** Only parse minimal metadata; ensure opt-in; provide transparency dashboard.  
- **Backup plan:** Offer manual “/gather” command trigger instead of passive NLP detection.
**Challenge 3:** Ambiguous natural language  
- **Why it’s a risk:** AI may misinterpret casual messages.  
- **Mitigation strategy:** Use confirmation prompts (“Start a plan for brunch this weekend?”).  
- **Backup plan:** Add “undo” and edit functions for false triggers.
**Challenge 4:** Over-automation fatigue  
- **Why it’s a risk:** Users may feel overwhelmed by notifications.  
- **Mitigation strategy:** Limit to one active plan per group; configurable notification settings.  
- **Backup plan:** Fallback to manual summary message format.
---
## Prior Work & Related Projects
**1. Calendar.help (Microsoft Research)**  
- **Description:** AI-human hybrid meeting scheduler.  
- **Similarities:** Automates scheduling and availability coordination.  
- **Differences:** Geared toward professional contexts; GatherAI focuses on casual, social coordination.
**2. Reclaim.ai / Motion**  
- **Description:** AI tools that automatically schedule work tasks.  
- **Similarities:** Automate time optimization.  
- **Differences:** Single-user productivity tools; GatherAI is crowd-based and group-oriented.
**3. WeightIn (2023 Project)**  
- **Description:** Crowdsourced decision-making tool for polls.  
- **Similarities:** Collects group input for consensus.  
- **Differences:** GatherAI embeds polling directly into group chats for dynamic scheduling.
**Lessons from Past Course Projects:**  
Projects like *Loopify* and *Kinnect* demonstrate that integrating social motivation and gamification significantly improves participation. GatherAI applies this principle by making social payoff (successful plans) the intrinsic incentive.
---
## Ethical Considerations
**Potential Ethical Issues:**
- Privacy of chat data  
- Implicit consent from group members  
- AI bias in interpreting natural language intent  
**Mitigation Strategies:**
- Only parse explicit, opt-in chats  
- Local text analysis to avoid storing raw messages  
- Clear consent and transparency messages at setup  
**IRB Considerations:**  
Not required for classroom prototype since all participants are consenting adults and data is anonymized, but full deployment would require review for user data handling.
---
## Business Viability (Optional)
**Revenue Model:**  
Freemium model — free basic coordination, premium for smart suggestions or venue booking integration.
**Market Size:**  
Hundreds of millions of messaging users; large addressable market through iMessage and WhatsApp.
**Competitive Advantage:**  
No app download required; embeds directly in existing social platforms.
**Sustainability:**  
Low hosting cost, organic viral growth through group chats, and partnership potential with event/restaurant APIs.
---
## Steel-Man Discussion (Round 3)
**Idea A Steel-Man:** GatherAI — AI-driven crowdsourced coordination via group chats.  
**Idea B Steel-Man:** MoodMap — campus-wide emotional well-being heatmap.  
**Why We Chose This Idea:**  
GatherAI was more feasible within technical constraints, offered stronger real-world utility, and naturally leveraged built-in crowdsourcing through friend groups.
**What We Agreed On:**  
Low-friction design, privacy preservation, and gamified incentives are key.
**What Concerns Emerged:**  
Risk of low engagement and over-automation; needs careful UX balance.
**Key Insights from Round 3 Discussion:**  


- Crowdsourcing can exist organically within small, trusted networks — the “microcrowd” model can be powerful for coordination and social behavior studies. 
- Crowdsourcing is easier when the goal is to split a decision for a group (solves the problem of sourcing data)
- Consensus ranking is dependent on a multitude of factors, not limited to the majority opinion (may not be the best time, etc)
---
## Implementation Timeline (Optional)
**Week 1-2:** Define MVP (intent detection + poll creation).  
**Week 3-4:** Build backend API + messaging integration.  
**Week 5-6:** Pilot with small friend groups; collect data.  
**Week 7-8:** Add consensus algorithm, gamification, and analytics.
---
## Additional Notes
GatherAI has strong potential as both a research experiment in microcrowdsourcing and a viable consumer tool. Its approach bridges conversational AI, collective decision-making, and lightweight automation.
---



