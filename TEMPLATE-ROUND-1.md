# Crowdsourcing Project Idea: FactDuel

## Author
Manasi Gajjalapurna
mgajjala

## Problem Statement
Misinformation spreads 6x faster than corrections on social media, but traditional fact-checking is slow (takes days) and feels like homework rather than engagement. Existing platforms like Snopes rely on centralized expert review, which can't scale to the velocity of viral claims. People need a way to rapidly verify claims that makes research competitive and rewarding rather than tedious.

## Core Concept
**One-line pitch:** 1v1 speed research battles where players race to find the best sources proving viral claims true or false, with crowd-validated winners climbing a ranked ladder.

**Target users:** News consumers who want to verify claims quickly, Competitive individuals who enjoy debate and proving people wrong, Anyone who argues online and wants ammunition

**The crowd:** Players (researchers): compete in duels, find sources, Judges (validators): vote on whose source is better quality. Dual role: everyone plays AND judges others' matches

**The task:** For players: Given a viral claim (e.g., "Coffee cures cancer"), you have 5 minutes to find the best authoritative source proving it TRUE or FALSE. Submit link + 2-sentence explanation of why your source is credible.
For judges: Watch a completed duel replay, see both sources submitted, vote which one is: (1) more authoritative, (2) more directly relevant, (3) actually a primary source. Takes 1-2 minutes per judgment.

## Key Features
Ranked matchmaking system with ELO ratings

Bronze → Silver → Gold → Platinum → Master tiers
Win duels = gain points, lose = lose points
Matched against similarly-skilled opponents
Visible rank badge on profile


Fast-paced 5-minute research rounds (best of 3)

Claim appears on screen for both players
30 seconds to read and decide TRUE/FALSE stance
5 minutes to find best source (primary sources worth more)
Submit link + brief credibility explanation
3 rounds per match, win 2/3 to win duel


Crowd-powered judging system

After match ends, 5-7 random judges vote on winner
Judges see: claim, both sources, both explanations (no player names)
Vote on: source quality, relevance, credibility
Majority vote determines winner
Judges earn smaller points for participating


Source quality tier system

Tier 1 (best): Peer-reviewed studies, government data, primary sources
Tier 2: Reputable news citing primary sources, academic institutions
Tier 3: News aggregators, general media
Tier 4: Wikipedia, blogs, social media
System flags source tier automatically, judges can override


Daily challenges and progression

"Win 3 duels today" → bonus points
Win streak tracker (5 in a row = special badge)
Seasonal leaderboards (reset monthly)
Achievement badges: "Myth Buster", "Citation Master", "Streak Legend"

## Feasibility Check
**Data source:** Viral claims sourced from:

Twitter/X API (trending controversial claims)
Reddit API (r/WhitePeopleTwitter, r/politics top posts)
Manual curation: instructor/TAs submit 5-10 claims per week
User submissions: players can suggest claims (moderated queue)


Claim database: 50-100 pre-vetted claims for launch, grow organically

**Budget reality:** $0 core platform - intrinsic motivation (competition, ranking, skill-building)
$100-150 tournament prize pool - launch tournament: "Top 8 players after Week 1 compete for prizes" (1st: $75, 2nd: $50, 3rd: $25)
$50 judge incentives - first 20 judges get $2-3 each for validating 10+ matches (seed judging pool)
Free infrastructure - Heroku/Vercel free tier, Firebase for real-time features
Total: ~$200 budget usage

**Crowd size needed:** Minimum viable: 20-30 active players

10-15 compete regularly (3+ duels per week)
20-25 judge occasionally (5-10 judgments per week)
Each player generates ~3 duels/week = 30-45 matches needing judgment
5 judges per match = need 150-225 judgments/week
20-25 people doing ~7 judgments each = feasible


Target for strong project: 40-50 users

More competition, faster matchmaking
Better ELO distribution across ranks

**Quality control approach:** 
Source validation: Automated domain checker (flags low-quality sources like random blogs)
Judge consensus: Need 3/5 judges to agree for valid result; if split 2-3, match goes to tiebreaker judge
Judge quality scoring: Track judge agreement with consensus over time; weight votes by accuracy
Anti-cheat measures: Flag if same source appears in multiple matches (sharing answers), ban collusion
Expert validation: Instructor/TA reviews disputed matches or questionable sources weekly

## Technical Approach
Human tasks:

Research: Finding authoritative sources under time pressure (requires critical thinking, domain knowledge, research skills)
Source evaluation: Judging which source is more credible (requires media literacy, understanding of source hierarchies)
Explanation writing: 2-sentence rationale for why source is trustworthy (requires communication skills)
Claim curation: Moderators review user-submitted claims for suitability

Automated tasks:

Matchmaking: ELO algorithm pairs players of similar skill level
Timer enforcement: Countdown clocks, auto-submit when time expires
Source domain analysis: Extract domain from URL, check against whitelist/blacklist, flag tier
Vote aggregation: Count judge votes, determine winner, update ELO ratings
Leaderboard calculation: Rank players by points, track statistics (win rate, average source quality)
Achievement tracking: Monitor for streaks, milestones, award badges automatically

Aggregation method:

Judging consensus: Majority vote (3/5 judges minimum) determines match winner

If 5-0 or 4-1: Clear winner, full ELO transfer
If 3-2: Winner declared, reduced ELO transfer (close match)


Judge weighting: Experienced judges (high agreement rate) get 1.2x vote weight
Source quality scoring: Aggregate tier flags + judge overrides to build source reputation database

"nytimes.com cited 47 times, won 89% of matches → high credibility"
"randomBlog.com cited 3 times, won 0% → flag for future"


Claim difficulty: Track how often claim results in split decisions → assign difficulty ratings
Meta-analysis: After 10+ duels on same claim, establish ground truth ("This claim is FALSE based on 78% TRUE-stance losses")

## Prior Work
Similar projects:

Twitter Community Notes - Crowd fact-checks tweets with "surprising agreement" weighting (must cross partisan lines). Difference: We're competitive/gamified (1v1 duels), not collaborative. We emphasize speed and source quality over consensus across divides. Community Notes is slow (days), we're fast (5 minutes).
Kialo (debate platform) - Structured argument mapping with crowd voting on argument quality. Difference: We focus on factual claims with source-finding, not opinion debates. We're fast-paced competitive matches, not long-form discussion trees. We judge source quality, not argument persuasiveness.
Past NETS project - FactBreak (original concept) - Daily fact-checking challenges with points/streaks. Key improvement: Added competitive 1v1 matchmaking (more engaging than solo challenges), ELO ranking system (clear progression), and crowd judging layer (quality control + judges are also contributors).

**Lessons from past course projects:** 
Weak incentives doom projects: Payment or "help society" isn't enough. Solution: Competitive ranking system taps into ego/status drives (Octalysis Core Drive 2: Accomplishment, Drive 5: Social Influence). People will research to climb the ladder.
Quality control must be multi-layered: Simple voting fails. Solution: Source tier system (automated) + crowd judging (human) + expert review (backup) + judge reputation weighting (meta-layer).
Sustainability requires intrinsic motivation: Projects relying on course requirements die. Solution: Skill-building (research/media literacy) + social comparison (rankings) + achievement hunting (badges) create organic retention.

## Why This Could Work
FactDuel transforms tedious fact-checking into addictive competitive gameplay by tapping into proven engagement mechanics (ELO ranking, 1v1 competition, fast rounds) borrowed from chess.com and League of Legends. The dual-role crowd (everyone plays AND judges) solves the cold-start problem while ensuring quality control through aggregated judgments. With just 20-30 engaged students competing for ranked bragging rights and a small prize pool, the project can generate 100+ fact-checked claims with robust source validation—demonstrating sophisticated aggregation (weighted consensus, source reputation tracking) and sustainable incentive design (intrinsic motivation via competition, not payment).RetryEH
