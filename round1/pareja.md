# Crowdsourcing Project Idea: MicroProof: Crowdsourced Local Fact-Verification Network

## Author
Omar Pareja | PennKey: Pareja

## Problem Statement
Local news and social media frequently circulate unverified claims such as “bus line canceled,” “restaurant shut down,” or “road flooded.” These micro-events often go unchecked because traditional fact-checking organizations and local reporters can’t verify information at neighborhood scale. This leads to confusion, misinformation, and loss of trust within communities.

## Core Concept
**One-line pitch:** A micro-fact-checking platform where residents verify or debunk local claims with on-the-ground photo and video evidence.

**Target users:** Local community members, journalists, civic tech groups.

**The crowd:** Volunteers, commuters, and local contributors active on platforms like Reddit, Nextdoor, or campus-based communities.

**The task:** Users browse short local claims, physically verify them (e.g., by checking the bus stop, store, or street), and upload timestamped photo or video proof with a short note (“Yes, bus 34 is suspended” or “No, still running normally”). Other users can confirm, flag, or dispute the submission.

## Key Features
1. “Fact cards” that summarize each claim, its crowd-verified status, and supporting evidence.

2. Credibility scoring system that weights user reliability based on historical accuracy and agreement.

3. Interactive map and feed of recently verified or disputed local events, color-coded by verification level.

## Feasibility Check
**Data source:** User-submitted photo and video evidence, plus public claims scraped from social media (X/Twitter, Reddit, or community boards).

**Budget reality:** Under $300 using Firebase for backend storage, Google Maps API for visualization, and a simple Flask/Vercel front-end.

**Crowd size needed:** Several hundred active participants across neighborhoods to ensure continuous coverage and cross-verification.

**Quality control approach:** Geo-tag validation, EXIF timestamp checks, credibility weighting, and requirement for at least two confirmations before a claim becomes “verified.”

## Technical Approach
**Human tasks:** Identifying claims, verifying them in person, uploading media evidence, and confirming or disputing other users’ reports.

**Automated tasks:** Geo-verification, duplicate detection, spam filtering, and credibility score updates.

**Aggregation method:** Weighted consensus combining evidence count, user credibility, and time decay (recent confirmations count more).

## Prior Work
**Similar projects:** 

Fun Facts (2024) crowdsourced truth judgments but lacked evidence-based validation.
WeightIn used anonymous polling for opinions without ground-truth verification.
MicroProof uniquely connects digital claims to real-world physical verification using crowdsourced evidence and local context.

**Lessons from past course projects:** PixelPatchwork showed that good technical execution must be matched with strong user motivation.
Memory Mosaic revealed the importance of moderation and verification rather than pure content submission.
StudySphere highlighted the value of clear user roles and contribution incentives. MicroProof integrates these lessons by emphasizing credibility scoring, simple tasks, and immediate local utility.


## Why This Could Work
MicroProof is viable within course constraints because it uses simple tools and relies on readily available data sources. The concept requires only basic backend infrastructure and can be piloted on a single campus or neighborhood. It directly applies core crowdsourcing principles—aggregation, incentive design, and quality control—to a real, socially valuable problem: restoring trust in local information through collective verification.
