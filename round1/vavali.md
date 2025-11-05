# Crowdsourcing Project Idea: Where2Go

## Author
Vedha Avali (vavali)

## Problem Statement
Finding a clean, safe, and accessible public restroom is a daily challenge in many cities and campuses. Existing maps rarely include information on cleanliness, privacy, or accessibility. This project crowdsources bathroom ratings and reviews to help users(starting with Penn students) locate reliable restrooms across Philadelphia.

## Core Concept
**One-line pitch:** A crowdsourced map where users post, rate, and review public bathrooms based on cleanliness, safety, and accessibility.

**Target users:** Students, tourists, delivery workers, and city residents who frequently move around Philadelphia and need trustworthy bathroom information.

**The crowd:** Everyday users and volunteers, beginning with Penn students and expanding to a larger community

**The task:** Users upload photos, rate bathrooms on key attributes (cleanliness, privacy, supply levels, accessibility), and verify or comment on others’ reviews. Users can also supply bathroom access codes for public bathrooms which require them.

## Key Features
1. Bathroom rating system: cleanliness, accessibility, privacy, and supply levels.
2. Interactive map: shows nearby restrooms with crowd-sourced ratings and filters.
3. Photo and review upload: users can add images, notes,and confirm/flag innaccurate reviews.

## Feasibility Check
**Data source:** User submissions (ratings, photos, comments) and, optionally, open data sources from the City of Philadelphia for initial seeding
.
**Budget reality:** Uses free mapping APIs (Google Maps, Leaflet.js) and AWS for hosting and initial storage: estimated cost < $200 for a smaller proof of concept. Incentives can primarily be non-monetary (leaderboards, badges, or campus challenges), and small rewards (i.e. free food) can be provided to the main campus contributors.

**Crowd size needed:** Start small with 50-100 Penn students collecting and reviewing restrooms on or near campus. Once data quality and design stabilize, expand to the entire Penn community and other regions of the city (Center City, Rittenhouse, Old City, etc.) and potentially even the Philadephia community as a whole.

**Quality control approach:**
- Reputation system: verified contributors’ votes carry more weight.
- Cross-validation: multiple users must confirm new bathroom entries.
- Flagging and admin moderation for spam or false data.

## Technical Approach
**Human tasks:** Identify and review restrooms, upload photos, rate key features, and validate others’ posts.

**Automated tasks:** Compute average scores, merge duplicate entries (same coordinates), and generate visual heatmaps of restroom quality.

**Aggregation method:** Weighted averages of user ratings by reputation; entries within a small distance (e.g., 15 m) merged into a single bathroom record.

## Prior Work
**Similar projects:** Got2Go NYC - this applications reviews of bathrooms stems from the creator's TikTok account reviewing bathrooms, but is limited in scope to specifically New York Cit Got2Go NYC - this applications reviews of bathrooms stems from the creator's TikTok account reviewing bathrooms, but is limited in scope to specifically New York City. The app is also not entirely crowdsourced and depends on a single individual.

**Lessons from past course projects:**
- Define a clear, real-world need, and create an application that the majority of users can tangibly benefit from.
- Ensure verifiable outcomes (photos, coordinates, and peer confirmation).
- Use simple, engaging micro-tasks to sustain participation.
- Add instant feedback to encourage continued engagement.

## Why This Could Work
Bathroom access is a universal need, and Penn’s campus provides a contained, walkable environment ideal for pilot testing. Penn students already move frequently between libraries, academic buildings, and many are often unsure where the closest on-campus bathrooms, or when off-campus, whether there are accessible bathrooms nearby at all. A small, motivated student crowd can quickly populate the map with high-quality data, creating immediate local value. Once proven, the model can scale across Philadelphia or other campuses, all within course time and budget constraints.
