# Crowdsourcing Project Idea: Missing Menu Mapper

## Author
Veda, vmantena

## Problem Statement
Food delivery apps often show incomplete or outdated restaurant menus. This causes customer frustration and can reduce sales for small restaurants that rely on delivery platforms. This project will crowdsource accurate, structured menu information for places that lack a reliable digital presence.

## Core Concept
**One-line pitch:** A crowdsourced system for capturing and validating up-to-date restaurant menu data.

**Target users:** Restaurant customers who rely on delivery apps, and small restaurants that need accurate menu visibility.

**The crowd:** Local diners, volunteers, and social media users visiting restaurants who are willing to upload menus and verify entries.

**The task:** Take or upload a photo of a menu or receipt, transcribe each item and price into structured form, and verify entries submitted by others.

## Key Features
1. Menu upload and transcription workflow
2. Redundancy and user-driven validation
3. Priority for restaurants flagged as outdated or missing menus

## Feasibility Check
**Data source:** Physical menu photos, screenshots from restaurant websites or Yelp, user uploads.

**Budget reality:** Primarily volunteer labor with optional low-cost MTurk validation tasks. (<$500)

**Crowd size needed:** Hundreds, since each restaurant only needs a few submissions for coverage.

**Quality control approach:** Redundant submissions, majority-vote aggregation, and gold-standard checks seeded throughout tasks.

## Technical Approach
**Human tasks:** Photo upload, manual transcription of items and prices, validation/comparison of existing fields.

**Automated tasks:** OCR to pre-fill text, duplicate detection, consistency checks, and confidence scoring.

**Aggregation method:** Per-field consensus using majority vote with weighting by worker reliability.

## Prior Work
**Similar projects:** • DataLabeler (04): Gathered structured fields from unstructured sources. My system applies this to restaurant menus with stronger validation emphasis.
• Loopify (08): Layered worker validation. My project uses a similar iterative refinement process for accuracy.

**Lessons from past course projects:** Simpler microtasks improve participation and data quality. Both DataLabeler and Loopify showed that workers stay more accurate with clear structure and feedback, which directly shapes my workflow design.

## Why This Could Work
The tasks are quick, familiar, and already common behavior for diners who photograph menus. With a focused scope and strong validation design, this system can quickly gather high-quality menu data within course constraints and budget.
