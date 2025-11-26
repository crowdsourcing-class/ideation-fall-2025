# Crowdsourcing Project Idea: Branch Birds

## Author
Jackson Gold (jgold23 - 25065033)

## Problem Statement
Amateur bird watchers often have problems identifing unknown birds (or ones new to them) and have trouble verifying thier identities. Branch Birds allows you to submit photos of birds and have users of the app suggest species identifications. While similar applications may currently exist (Merlin/Seek/INaturalist), Branch Birds stands out by emphasising a learning aspect for new birders to improve on their identificaiton skills while helping the community.

## Core Concept
**One-line pitch:** Helps novice bird watchers learn practice identifying birds while also generating high-quality training data for a bird classification model.

**Target users:** Novice and Expert Bird Enthusiasts

**The crowd:** Birding communities, MTurk (to get ball rolling), Orthothology experts

**The task:** Select an identification for a bird shown on their screen 

## Key Features
1. Submit photos of bird
2. Flashcard like IDing of submitted photos  

## Feasibility Check
**Data source:** Users will submit data and multichoice options  will come from Avibase

**Budget reality:** Users are incentived by their own betterment of bird knowledge

**Crowd size needed:** 1000s in order to get enough data but 10s in order to help users identify birds

**Quality control approach:** Use 'Golden Standard' checks with data from Avibase

## Technical Approach
**Human tasks:** Identifying birds in standards and odd positions

**Automated tasks:** Generating a set of potential labels for the bird

**Aggregation method:** Plurality vote on a bird will be the accepted label

## Prior Work
**Similar projects:** Merlin/INaturalists. Merlin does this but for bird sounds, helps users keep track of their birds, and has a model to ID photos of birds but does not work well. Branch Bird is focus on learning and helping others learn by gamifly practicing bird identification while simultaneously helping novices id birds they have spotted.  

**Lessons from past course projects:** That an internal incentive that involves personal betterment is important

## Why This Could Work
Since most of the data is available and users have a non-monetary incentive (learning) the project could be easily scaled and work beyond the course.
