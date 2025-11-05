# Crowdsourcing Project Idea: WeTrack  

## Author  

Name: Arriella Mafuta

Pennkey: arriella

## Problem Statement  

Many students struggle to stay accountable for personal or academic goals such as exercising, studying, or building habits. Existing productivity apps are isolating and fail to leverage the power of peer motivation. WeTrack helps students create small accountability circles where progress tracking and verification come from their peers.  

## Core Concept  

**One-line pitch:** A social accountability platform where students crowd-verify each other’s progress toward shared goals.  

**Target users:** University students seeking structure, motivation, and peer support.  

**The crowd:** Fellow students in small accountability circles (4–6 members) who log progress and verify others’ submissions.  

**The task:** Users record short daily check-ins (e.g., “completed reading” or “went to the gym”) and verify peers’ updates via quick validation prompts or photo confirmations.  

## Key Features  

1. Peer verification for daily goals (mutual accountability).  
2. Progress streaks and leaderboard to sustain engagement.  
3. Group chat or reaction system for encouragement.  

## Feasibility Check  

**Data source:** User-submitted logs and peer verifications.  

**Budget reality:** Hosting via low-cost tools (Firebase/Convex, Replit) under $100; volunteer participation, no paid crowd.  

**Crowd size needed:** Dozens to hundreds of small student groups (each self-sustaining).  

**Quality control approach:** Cross-verification — each log requires at least two peer confirmations; optional random audits for streak abuse.  

## Technical Approach  

**Human tasks:** Logging activities, verifying peers’ claims, and flagging inconsistencies.  

**Automated tasks:** Streak tracking, notification reminders, leaderboard updates, and outlier detection for false logs.  

**Aggregation method:** Weighted reliability scoring — verified logs increase a user’s accountability score; streaks validated only when majority agreement exists.  

## Prior Work  

**Similar projects:** Habitica (gamified habit app), BeReal (social proof through photos). TaskTrack differs by focusing on micro accountability within small peer circles, not public social feeds.  

**Lessons from past course projects:** Past teams often relied on payment or novelty; WeTrack uses natural social incentives and intrinsic motivation to sustain engagement.  

## Why This Could Work  

Students are already motivated to stay productive and value peer validation. The model requires no financial incentives, scales organically through social circles, and offers measurable participation metrics. Within one semester, a small working prototype could demonstrate real engagement through student study or fitness groups.