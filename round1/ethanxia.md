# Crowdsourcing Project Idea: [CrowdScout]

## Author
[Ethan Xia (ethanxia)]

## Problem Statement
The NBA scouting process is generally very time and work-consuming for analysts and recruiters. There are thousands of potential players across the globe each year, and scouts do not have the resources to inspect them all. Many promising players will go unnoticed because they play in smaller leagues or lack media exposure. This project leverages the crowd to identify and evaluate rising basketball players based on highlight clips and statistics. 

## Core Concept
**One-line pitch:** We will use crowdsourced insights and highlights (similar to Instagram reels) to spot the next breakout NBA players before traditional analytics can. 

**Target users:** NBA hopefuls, scouts, data analysts, and sports media outlets. 

**The crowd:** Basketball fanalytics (Reddit/Twitter/MTurk) (can expand to other sports as more of a overarching 'social media app' for sports)

**The task:** Crowd workers will watch short highlight clips that non-NBA players post of themselves. Then, they will rank each clip based on a like/dislike system. 

## Key Features
1. Video Rating System - shorter highlight clips allow more clips to be ranked and scored easily
2. Skills tags - tagging skills (handling, shooting, defense) can help users identify what the highlight is supposed to be of.   
3. Crowd consensus dashboard / leaderboard - aggregates "ratings" per athlete profile through likes/followers and visualizes top-rated prospects. 

## Feasibility Check
**Data source:** User uploaded data and also publicly available amateur basketball highlight clips. 

**Budget reality:** using MTurk with short tasks and small payments (for content moderation). 

**Crowd size needed:** At least 10 prospect athletes (the more the better, like any media platform)

**Quality control approach:** Minimum video length, video quality, content moderation. 

## Technical Approach
**Human tasks:** Watching clips, like/dislike, rating skills, commenting, following

**Automated tasks:** Collecting and processing video data, normalizing ratings and consensus scores, and algorithmically finding the next best video to push for the user. 

**Aggregation method:** For each clip, we can count the number of total likes / comments / views and aggregate into a crowd consesus score that determines overall likability. 

## Prior Work
**Similar projects:** 
- Hudl.com: A video analysis website for recruiters to check out athlete highlights. CrowdScout is different because this is more crowd focused, rather than specifically recruiter focused. Everyone including fans, athletes, and recruiters, can use the app. Also, instead of posting videos to a specific profile, videos are pushed to a centralized "feed," similar to a social media app. 

**Lessons from past course projects:** Identifying incentives to rank is very important. If there is no incentive for app users to like/dislike a highlight, then the ranking system cannot work.  

## Why This Could Work
CrowdScout is a fun, low-cost, and low-maitenance project and relies on publicly available video data that users upload themsleves. Basketball fans (and potentially other sports too) are already eager to evaluate and scout out potential players online. Additionally, this can garner a lot of exposure for players who may play in an unknown or smaller league. CrowdSource is the future of sports recruiting. 
