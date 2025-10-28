# Crowdsourcing Project Idea: Soundscape

## Author
Mingni Dong/ mdong126

## Problem Statement
Online maps and city guides tell you where to go, but not what it feels like. There’s no good way to explore the soundscapes of citiee, from quiet parks to bustling cafés which could help people choose better workspaces, travel destinations, or relaxation spots.

## Core Concept
**One-line pitch:** SoundScape crowdsources short ambient audio clips and tags them to build a global map of sounds.

**Target users:** Remote workers, travelers, urban planners, and people who love discovering new environments (musicians, game designers, etc.). To a more niche crowd, those with sensitivity to sounds. 

**The crowd:** Everyday users with smartphones, students, travelers, commuters.

**The task:** Record 10–30 second ambient sound clips of their surroundings (ex coffee shop, street, forest), rate others’ clips (ex “calm,” “busy,” “noisy”), and add tags or transcriptions.

## Key Features
1. Audio Upload & Tagging: Quick submissions with automatic geo-tagging.

2. Mood Map: Interactive map colored by sound vibes (quiet, lively, peaceful, pumped).

3. Daily Sound Challenges: Themed prompts (ex Record the calmest spot on campus).

## Feasibility Check
**Data source:** User-generated recordings.

**Budget reality:** Under $500 using Firebase for storage + open-source mapping (Leaflet/Mapbox free tier).

**Crowd size needed:** 100-500 contributers for initial coverage (maybe start with just the Philly area).

**Quality control approach:** 
Majority tagging consensus on mood/noise level.
Automatic noise filtering (e.g., skip silent clips).
“Trusted Listener badges for accurate raters

## Technical Approach
**Human tasks:** Recording, tagging, mood classification, verifying mislabeled clips.

**Automated tasks:** Noise-level analysis and spectrogram validation.
Clustering sounds by similarity for exploration

**Aggregation method:** Weighted voting + machine learning audio features.

## Prior Work
**Similar projects:** Geoguesser, Spotify, Soundcities
Mine is different because it is social, interactive, and focused on sound. It is also a crowdsourced, interactive project and not an art installation/statement.

**Lessons from past course projects:** People engage when they can create and compare. Contribution loops + badges are ways to keep people returning. Social from the octalysis work is a huge motivator.

## Why This Could Work
SoundScape has a built-in addiction loop. users record → see their sound appear on the map → get likes, feedback, and comparisons → earn badges → return for daily challenges.
Unlike typical crowdsourcing apps that end when data collection is done, SoundScape grows richer the more you use it. It blends personal expression, exploration, and contribution. It is also useful to both the person uploading and the people seeing the uploads. 
