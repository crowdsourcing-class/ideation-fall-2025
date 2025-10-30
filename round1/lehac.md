# Crowdsourcing Project Idea: Culinary Archive

## Author
Leha Choppara (lehac)

## Problem Statement
Families have boxes of handwritten recipes that are hard to search, share, or preserve. Culinary Archive digitizes, standardizes, and allergen-tags these recipes.

## Core Concept
**One-line pitch:** Turn photos of handwritten recipes into searchable, standardized, allergy-aware cards via the crowd.

**Target users:** Home cooks, culinary historians, families.

**The crowd:** MTurk + volunteers, drawing on those interested in cooking.

**The task:** Transcribe; standardize units; tag allergens/cuisine; verify with second pass.

## Key Features
1. Allergen/ingredient tagging
2. Printable recipe card database for satisfiably identified recipies
3. Two-pass transcription + verification

## Feasibility Check
**Data source:** User-uploaded images.

**Budget reality:** Through gamification and with MTurk, I think this could be done with $300.

**Crowd size needed:** 100s of workers needed.

**Quality control approach:** Multi-stage QC and LLM-assisted aggregation.

## Technical Approach
**Human tasks:** Transcribe; normalize; tag.

**Automated tasks:** OCR prefill; unit conversion; duplicate detection; toxicity filter for notes.

**Aggregation method:** Majority vote + LLM reconciliation.

## Prior Work
**Similar projects:** DataLabeler. It has dense text/audio labeling with layered QC. We differentiate by applying the pattern to OCR cleanup + structured tags.

**Lessons from past course projects:** We are using Memory Mosaic’s media upload pipeline, but we emphasize structured outputs rather than simple stacks.

## Why This Could Work
Clear before/after value; modular tasks; low qualifications needed for crowd workers; durable public good.
