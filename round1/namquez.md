# Crowdsourcing Project Idea: Game Genre Classifier From Game Clips

## Author
Nico Marquez, namquez

## Problem Statement
Players often struggle to find new games they’ll actually like because genre tags are inconsistent or vague across platforms. Short gameplay clips contain enough information to infer genre, but humans are still far better than algorithms at reading moment-to-moment gameplay context.

## Core Concept
**One-line pitch:** Users watch short gameplay clips and crowd-label what genre(s) the game belongs to.

**Target users:** Gamers + platforms that recommend games (Steam, itch.io style sites).

**The crowd:** Gamers on social media, Discord, reddit.

**The task:** Watch a 5–10 second gameplay clip and tag what genre(s) it fits into (e.g., roguelike, cozy, soulslike, FPS, builder, rhythm).

## Key Features
1. Fast clip labeling (5–10 seconds)
2. Consensus tagging that averages multiple players’ labels
3. Taxonomy / controlled vocabulary to avoid chaos genres

## Feasibility Check
**Data source:** Game clips sourced from trailers, gameplay streams, YouTube shorts, TikTok, and indie dev submissions.

**Budget reality:** Under $500 works because tagging tasks are extremely short + reward can be low or volunteer based.

**Crowd size needed:** Hundreds of workers.

**Quality control approach:** Gold standard clips inserted OR majority vote with confidence weighting.

## Technical Approach
**Human tasks:** Genre inference (because this is intuitive for humans).

**Automated tasks:** Clip slicing, deduping, taxonomy enforcement, consensus math.

**Aggregation method:** Weighted majority vote across 5+ workers per clip.

## Why This Could Work
Tagging gameplay clips is extremely fast, fun, and low cognitive load for gamers, so participation is natural and self-sustaining. Aggregation is trivial and quality control is easy with redundancy. This fits class scale comfortably.