# Crowdsourcing Project Idea: Campus Event Feed

## Author
Alexandra Oh

## Problem Statement
Students face significant information overload from non-centralized campus event notifications, including countless emails, newsletters, and group chat messages. This "noise" makes it difficult to discover relevant, high-value, or timely opportunities (e.g., free food, networking, guest speakers), leading to missed experiences and community disengagement. This project aims to filter this signal from the noise using community-driven curation.

## Core Concept
**One-line pitch:** A campus events platform that uses student upvotes and real-time tags to surface the most valuable happenings on campus today, and upcoming.

**Target users:** All undergraduate students looking to find events and opportunities campus.

**The crowd:** The target users themselves (students) acting as volunteer contributors. The incentive is intrinsic...by contributing, they improve the service for themselves and their peers.

**The task:** Submit: Post a new event with a title, time, location, and initial tags. Curate: Upvote or downvote events in the feed to signal quality. Tag: Add or confirm pre-defined filterable tags (e.g., #free_food, #networking, #free_merch). Verify: "Check-in" to an event when physically present to confirm it's live and as described.

## Key Features
1. Real-Time Curation Feed: A timely feed to show what's currently trending on campus.
2. Smart Tag Filtering: Users can filter the event feed by multiple tags simultaneously (e.g., Today + #free_food + #speaker).
3. Community-Based Verification: A "Verified Live" badge that appears on events after a critical mass of users "check-in," building trust and urgency.

## Feasibility Check
**Data source:** All data will be user-generated. Initial "seed" content can be sourced by the project team from existing newsletters like club listservs to kick off the process.

**Budget reality:** This project can be built using free-tier tech stack. Incentive is hopefully intrinsic so no payment mechanism is required.

**Crowd size needed:** The system needs a large group of active "browsing" users to generate enough votes for curation, even if only a smaller subset are people who submit of new content.

**Quality control approach:** Thee upvote/downvote algorithm can bury low-quality posts. A "flag for removal" button (for "Canceled," "Spam," "Wrong Info") and the "Verified Live" check-in system.

## Technical Approach
**Human tasks:** Upvoting/Downvoting, tagging, and checkin

**Automated tasks:** Querying based on user specified tags, displaying relevant events (timely)

**Aggregation method:** net score (upvote/downvote), tagging (confirmed after 3 tags), event verification

## Prior Work
**Similar projects:** Waze - real time app for traffic. Reddit - discussion forum with feed, but not specific to localized events.

**Lessons from past course projects:** There has to be incentive for both posters and event-searchers to be on  the app.

## Why This Could Work
This is a big struggle in current students lives, from both sides. Clubs and other school orgs have trouble advertising their events. Similarly, events get lost in students inboxes. This creates a centralized system.
