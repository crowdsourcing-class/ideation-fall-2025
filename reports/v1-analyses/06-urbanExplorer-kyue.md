# Urban Explorer - Adversarial Analysis (V1)

**Authors**: Katherine Yue (kyue), James Doh (dohj0109), Omar Pareja (pareja), Eric Lee (ericclee), Mario Valek (mvalek)

## EXECUTIVE SUMMARY
Crowdsourced event discovery platform with interactive map—"Waze for local events." Solid core concept and appropriate technical architecture, but weak incentive design, unrealistic cold-start assumptions, and chicken-and-egg problem could doom it. High friction (posting events) with low value (empty platform) creates death spiral.

## VERDICT: WEAK GO

**Main Issue**: Cold-start death spiral - need events to attract users, need users to attract event posts. Zero budget for acquisition, relying on "volunteers and social media" (magic thinking).

**Critical Flaws**:
- Vague incentive design (badges/leaderboards without community)
- Unrealistic recruitment ("post on Reddit" = not a strategy)
- Made-up 1:10 poster:attendee ratio (likely 1:100)
- Premature optimization (5 QC mechanisms before users exist)
- Technical inconsistency (React Native vs Next.js - which is it?)
- Illegal data sourcing (Facebook Events API shut down 2018)

**Strengths**:
- Modern tech stack (TanStack Query, Prisma)
- Detailed workflow with implementation details
- Multi-layered QC approach
- Geographic density strategy (campus focus)
- Backup plans for challenges

**Rating**: C+ crowdsourcing (understands theory, weak execution), C+ technical feasibility

**Most Critical Change**: Redesign incentives for cold-start (not scale). Pay for quality ($5-10/event) or give organizers dashboards/analytics or bootstrap with curation (team spends 30min/day curating campus events).

**Predicted Outcome**: Build platform weeks 1-3, post Reddit week 3 (ignored), recruit friends week 4-5, demo with 30 events (mostly team/friends). Voting works, map shows pins, but sparse. Grade: B+ for execution, feedback on weak crowdsourcing.
