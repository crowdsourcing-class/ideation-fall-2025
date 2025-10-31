## Crowdsourcing Project Idea: **Micro-Museum Curator**

## Author
Connor Cummings
connorcc

## Problem Statement

There is a huge amount of public-domain cultural material (art, historic photos, archival images) that is technically “available” but not actually *narrated* for people. Institutions can’t hand-curate every slice of history, identity, or local interest. At the same time, people enjoy lightweight curation (Pinterest boards, mood boards). This project channels that casual curation energy into building public, themed “mini exhibits” from open collections.

## Core Concept

**One-line pitch:** A collaborative micro-museum where people assemble tiny themed exhibits from public-domain images and the crowd votes the best ones to the front page.

**Target users:** Students, history/art enthusiasts, local community groups, and online culture folks who like making lists/boards.

**The crowd:** Visitors to the web app who browse the open image pool and either (a) build a new mini exhibit or (b) vote or lightly edit others’ exhibits.

**The task:** A user picks a theme (e.g. “Women in early computing,” “Philly rowhouse life,” “Portraits with dogs”), selects 4–6 public-domain items from the shared library, and writes a 1–2 sentence label for each explaining why it fits. Other users rate the exhibit on clarity, cohesion, and interest. Highly rated exhibits are promoted.

## Key Features

1. **Theme-based exhibit builder** to pick items from a public-domain pool and add micro-labels.
2. **Voting and ranking** so the most coherent/interesting exhibits rise to the top.
3. **Remix/fork exhibits** to improve an existing theme without starting over.
4. **Homepage spotlight** that auto-surfaces top exhibits per theme based on engagement.

## Feasibility Check

**Data source:** Public-domain image sets (e.g. The Met, Smithsonian Open Access, Library of Congress) preloaded into the app. User submissions (labels, themes, votes) form the core crowdsourced dataset.

**Budget reality:** Low cost if a fixed catalog is cached and we store only small text + vote records.

**Crowd size needed:** 20–40 active users is enough to create competing exhibits per theme and generate meaningful votes.

**Quality control approach:** Allow multiple exhibits per theme; use voting/ranking to surface the best. Apply simple validation (minimum items, non-empty labels) and group near-duplicates.

## Technical Approach

**Human tasks:**

* Create an exhibit: pick 5 items and write 1–2 sentence labels.
* Rate existing exhibits on clarity, relevance, and interest.
* Optionally remix an exhibit to improve it.

**Automated tasks:**

* Track engagement (views, votes, remixes).
* Promote top exhibits per theme to the homepage.
* Detect near-duplicate exhibits and group them.
* Run basic quality checks (min # items, min label length).

**Aggregation method:**

* Compute a weighted score = (upvotes – downvotes) + bonus for diverse voters + bonus for remixes.
* Cluster exhibits with similar theme names; select the highest-scoring exhibit in each cluster as the “canonical” one.
* Store label-level data for potential future suggestion/ranking.

## Prior Work

**Similar projects:** User-curated museum collections, Pinterest-style boards, social remix platforms. This project adds explicit voting and a shared public-domain pool.

**Lessons from past course projects:** Lightweight, fun tasks (select + short text + vote) get completed more than long annotations. Allowing remixing keeps content evolving and increases data volume.

## Why This Could Work

Because the task is bounded and creative, people will actually do it. Public-domain sources remove licensing friction. Even with a small crowd, repeated voting quickly reveals the best exhibits, so the system’s quality improves without needing a huge user base.
