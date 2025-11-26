# Crowdsourcing Project Idea: CreatorScale

## Authors

**Original Author:** Eshaan Kaipa (ekaipa)

**Round 2 Contributor:** Omar Pareja (pareja)

**Round 3 Contributors:** N/A

## Problem Statement

Brands struggle to manage influencer campaigns, verify engagement, and match creators to goals. Existing tools are manual and unreliable. CreatorScale automates campaign management and crowdsources verified engagement data from creators.

## Target Audience

**End Users:** Brands, marketing teams, and creators running campaigns.

**Crowd Workers:** Micro-influencers and social media users posting and tracking campaign content.

**Stakeholders:** Brands, agencies, and creators relying on verified engagement data.

## Description

CreatorScale is an AI-powered platform that automates influencer campaign setup, creator matching, and performance tracking. Creators post sponsored content and upload engagement metrics, which the system verifies via social media APIs. It aggregates results to provide brands with transparent campaign analytics and optimized creator recommendations.

## Project Type

_Select the primary category:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [X] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 8-10 key features or capabilities of your system:_

1. AI creator-brand matching
2. Automated campaign creation
3. Creator-submitted engagement data
4. API-based engagement validation
5. Real-time analytics dashboard
6. Gamified creator incentives
7. Anomaly detection for data accuracy
8. Aggregated campaign performance reports
9. Reliability scoring for creators
10. API integration with Instagram/TikTok/YouTube

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Social media users and influencers recruited through online creator communities.

**What will they provide?**
Engagement metrics (likes, views, comments).

**What skills do they need?**
Basic social media and data-sharing ability.

**Do skills vary widely? How?**
Experienced influencers provide more consistent data; system scores reliability.

**How will you incentivize participation?**
Small payments ($0.50–$1/task), badges, exposure opportunities.

**Budget & Cost Analysis:**
- Estimated cost per task: $0.75
- Estimated cost per worker: $5–$10
- Number of tasks needed: ~400
- Total estimated budget: ~$350
- Justification: Fits under $500 using small-scale pilot and API automation.

**Where will your data come from?**
Social media APIs (Instagram, TikTok, YouTube) and creator uploads.

**How many crowd workers do you need?**
- Minimum viable: 100 workers
- Target: 250–300 workers
- Scalable to: 1,000+ creators

## Technical Architecture

**System Components:**
- Frontend: React web interface
- Backend: Python (Flask)
- Database: PostgreSQL
- ML: scikit-learn / OpenAI API
- External APIs: Instagram, TikTok, YouTube

**Workflow:**
1. Brand uploads campaign.
2. AI recommends creators.
3. Creators post and report metrics.
4. System verifies via APIs and anomaly checks.
5. Aggregated report delivered to brand.

**Human vs Automated Tasks:**

| Task | Performed By | Why |
|------|-------------|-----|
| Post campaign | Human | Requires human creativity |
| Report metrics | Human | Data collection from creators |
| Verify engagement | Automated | API-based validation |
| Analyze performance | Automated | Data aggregation + ML |

**Technologies & Tools:**
- Frontend: React
- Backend: Flask
- Database: PostgreSQL
- ML/AI: scikit-learn, OpenAI API
- Crowdsourcing Platform: Custom web interface
- Hosting: AWS

**Aggregation Method:** Weighted averaging using creator reliability scores.

## Quality Control

**Strategy:** Combine automated API checks with human cross-verification.

**QC Mechanisms:**
- Gold standard test posts (5%)
- Majority checks for consistent data
- API verification for all metrics
- Reputation scoring for each creator
- Outlier detection (engagement spikes)
- Retasking for flagged entries

**Handling Low-Quality Work:** Re-task flagged data and reduce worker score; repeated low-quality reports lead to removal.

## Evaluation & Success Metrics

**Primary Metrics:**
- Engagement verification accuracy ≥ 90%
- ≥ 100 creators onboarded
- <$500 total cost

**Evaluation:** Compare reported vs. verified engagement. Measure system accuracy and completion rate.

**Baseline:** Manual campaign management systems.

**Success Criteria:**
- Minimum: Working prototype
- Target: Accurate, usable analytics
- Stretch: Scalable AI automation

## Challenges & Mitigation Strategies

1. False engagement reports → API verification + anomaly detection
2. Low participation → Incentives + gamification
3. Scaling system → Modular infrastructure + API automation

## Prior Work & Related Projects

**Grin:** Manual influencer management tool — lacks API-verified data.

**Aspire:** Campaign tool — no crowdsourced validation.

**CreatorScale difference:** Combines AI matching + crowd-verified engagement.

**Lessons from past projects:** Keep human tasks simple and use automation for verification and aggregation.

## Ethical Considerations

**Issues:**
- Data privacy from creator analytics
- Fair compensation for creators
- Misuse of engagement data

**Mitigation:**
- Use anonymized analytics
- Transparent pay model
- API-only data validation

**IRB Considerations:** Not required; no sensitive personal data collected.

## Business Viability

**Revenue Model:** Subscription for brands + transaction fee per campaign.

**Market Size:** Brands using influencer marketing ($21B industry).

**Competitive Advantage:** Automated validation + AI creator matching.

**Sustainability:** Scalable through APIs and low-cost cloud infrastructure.

## Steel-Man Discussion (Round 3)

**Idea A Steel-Man:** AI marketing automation tool — scalable, reduces manual work.

**Idea B Steel-Man:** Creator engagement tracker — crowd-based, low cost.

**Why We Chose This Idea:** Combines automation + crowdsourcing effectively and is achievable under course scope.

**What We Agreed On:** Feasible with current APIs and realistic incentives.

**Concerns:** Maintaining reliable crowd participation.

**Key Insights:** Automation plus crowd input ensures both scalability and authenticity.

## Implementation Timeline (Optional)

- Week 1–2: Design + data setup
- Week 3–4: Build creator interface + API integration
- Week 5–6: Pilot test with small creator set
- Week 7–8: Analyze data + finalize prototype
