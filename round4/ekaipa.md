# Round 4 Reflection: Final Project Decision

**Name**: Eshaan Kaipa
**PennKey**: ekaipa
**Date**: November 4, 2025

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| CreatorScale | Round 3 (mine) | My original project - combines AI automation with crowdsourced validation, has clear technical path and feasible budget under $500. |
| PitchPeer | Round 3 (emkang) | Strong gamification model for peer feedback, but requires building from scratch and less clear recruitment strategy for founders. |
| Urban Explorer | Round 3 (kyue) | Event discovery platform with good crowd engagement model, but overlaps with existing platforms like Eventbrite and requires extensive location data. |

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)
- [x] V2 detailed analyses (reports/v2-analyses/)
- [x] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)
- [x] Group discussions
- [ ] Other

---

## 2. My Decision

**Project Name**: CreatorScale

**Decision type**:
- [x] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

**If pivoting or adopting someone's idea**:
- Original author (if applicable): N/A
- Original round: N/A

---

## 3. Why This Decision

**High-level reasoning**:

I'm staying with CreatorScale because after analyzing the project through multiple rounds and comparing it to alternatives, it represents the best combination of feasibility, technical clarity, and real-world applicability for this course.

The key factors that solidified my decision are: (1) clear technical pathway using existing APIs (Instagram, TikTok, YouTube) that reduces implementation risk, (2) well-defined crowd tasks (creators posting and reporting engagement metrics) that are simple and don't require specialized skills, (3) realistic budget at ~$350 which fits comfortably under the $500 constraint, and (4) a dual validation approach using both API verification and crowdsourced data that addresses quality concerns directly. Additionally, working with Omar since Round 2 has given us good momentum and complementary skill sets - he brings additional perspectives on the marketing and business side that strengthen the project.

The trade-off I considered was whether to pivot to a project with a more "captive" audience (like classmates), but CreatorScale's recruitment strategy through creator communities and small monetary incentives ($0.50-$1/task) is realistic and scalable. The API-based validation layer means we can start with a small pilot group (100 workers) and still get meaningful results, then scale up if successful.

**What convinced me**:
- Strong technical feasibility with existing social media APIs reducing implementation complexity
- Clear and simple human tasks (posting content, reporting metrics) that creators already do naturally
- Realistic budget and scalable model that can start small and grow
- Dual validation approach (API + crowd) addresses quality concerns effectively
- Partnership with Omar provides continuity and complementary expertise

**What concerns me** (and how I'll address it):
- Recruiting creators may be challenging initially → Start with Penn student creators and local micro-influencers, leverage small payments and gamified incentives, post in creator communities and social media groups
- API rate limits or access restrictions → Use free-tier APIs initially, implement rate limiting and caching, have backup manual validation process for flagged data
- Low participation or engagement quality → Implement reliability scoring from Week 1, use gold standard test posts (5%), provide clear instructions and examples, gamify with badges and leaderboards

---

## 4. What I'm Building

**One-sentence project description**:
CreatorScale is an AI-powered platform that automates influencer campaign setup, matches creators to brands, and uses crowdsourced engagement data verified via social media APIs to provide transparent campaign analytics.

**MVP Scope** (3-4 core features only):

1. **Creator submission interface**: Web form where creators can upload campaign posts, report engagement metrics (likes, views, comments), and link their social media accounts
2. **API verification system**: Automated validation of reported metrics using Instagram/TikTok/YouTube APIs to cross-check engagement data
3. **Brand campaign dashboard**: Simple interface where brands can view creator submissions, verified engagement metrics, and basic performance summaries
4. **Creator-brand matching (basic)**: Rule-based matching algorithm (not full AI yet) that suggests creators based on follower count, engagement rate, and content category

**What I'm explicitly NOT building** (to keep scope realistic):
- Full AI-powered matching engine (using basic rule-based matching for MVP)
- Real-time analytics dashboard with advanced visualizations (simple summary reports only)
- Mobile app (web interface only)
- Multi-platform campaign management (focusing on one platform initially - Instagram)
- Payment processing system (manual payment tracking outside the platform)
- Advanced anomaly detection ML models (basic outlier detection using statistical thresholds)

---

## 5. Week 1 Validation

**The specific test I'll run Week 1**:

- **Where**: 
  - Post in r/UPenn subreddit on Monday at 2pm
  - Post in 3-4 Penn student creator Facebook groups on Monday at 3pm
  - Direct outreach to 20-30 Penn students who are micro-influencers (found through Instagram hashtags #Penn #UPenn #PennStudent)
  - Post in class Slack/Discord channels
- **When**: Monday, Week 1, starting at 2pm
- **What**: 
  - Create a simple Google Form/Typeform: "Help test CreatorScale! Post a branded campaign (or simulate one) and report your engagement metrics. We'll verify via API and you'll earn $1-$2 per valid submission. Takes 10 minutes."
  - Include clear instructions: "1) Post content with a campaign hashtag, 2) Wait 24-48 hours, 3) Report likes/views/comments, 4) Share your post link for verification"
  - Offer $1-$2 per completed submission (budget: $50 for 25-50 submissions)
- **Success metric**: 
  - At least 15 creators sign up and complete the task (post + report metrics)
  - At least 12 submissions pass API verification (80% success rate)
  - Average time to complete task < 15 minutes
  - Creators report the task was "easy" or "very easy" (4+ out of 5 on survey)

**If Week 1 test fails, I will**:
- [x] Simplify the task to: Just screenshot and upload engagement metrics without requiring an actual post (simulate campaign data)
- [x] Try different recruitment channel: Use MTurk with $2 per HIT to recruit creators (budget: $100 for 50 workers)
- [x] Use paid participants: Increase payment to $3-$5 per submission to attract more participants
- [ ] Pivot to: Focus on brands only - recruit 3-5 small brands/startups and have them manually input creator data for testing

---

## 6. Tentative Team

**Team members**:

1. Eshaan Kaipa (ekaipa) - Technical lead (backend, APIs, system architecture)
2. Omar Pareja (pareja) - Business/marketing lead (recruitment, user research, validation)

**Team status**:
- [x] Same team from Round 3
- [ ] New team formed during Round 4
- [ ] Solo (will find teammates later)
- [ ] Joining an existing team

---

## 7. Reflection

**Most valuable part of Round 4**:
The rubric scoring and viability analysis helped me identify the concrete weaknesses in my project (recruitment strategy) and forced me to develop a very specific Week 1 validation plan. The steelman discussions with classmates also helped me see that staying with CreatorScale made sense - it has a clear technical path and the crowd tasks are genuinely simple, which many other projects struggled with.

**Biggest surprise**:
I was surprised to see how many Round 3 projects had vague recruitment strategies similar to mine initially. The push to make Week 1 validation concrete (specific channels, times, metrics) was really valuable - it made me realize I needed a much more detailed execution plan, not just a general idea.

**One thing I'd tell future students about Round 4**:
Be brutally honest about your recruitment strategy. If you're planning to "post on social media" or "reach out to people," you need to specify exactly where, when, and how many responses you'll consider success. The Week 1 validation plan should be so specific that someone else could execute it without asking questions.

---

## Commitment

**I commit to**:
- [x] Building the MVP scope above (3-4 features maximum)
- [x] Running a concrete Week 1 validation test
- [x] Pivoting if Week 1 shows <20% success
- [x] Meeting with instructor if I hit major blockers

**Signature**: Eshaan Kaipa **Date**: November 4, 2025
