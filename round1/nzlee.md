# Crowdsourcing Project Idea: GroupGuide

## Author
Nathan Lee - nzlee

## Problem Statement
It can be beneficial to have a study guide for many courses, espcially as some courses may allow students to have a 1-2 paged cheat sheet for their exams. As a student, studying for exams is already a stressful process. It can be overwhelming to review lots of content while juggling the need to jot down and decide what topics/ideas are considered important and which are not for your study guide or cheat sheet.

## Core Concept
**One-line pitch:** My project crowdsources important course concepts and practice problems for a specific course that students will be able to vote on and generate a final cheat sheet automatically (with the options to customize).

**Target users:** Students of any course that offers cheat sheets for exams.

**The crowd:** Students within each specific course or students preparing for a national exam (AP Exams, SAT/ACT, MCAT, GMAT, etc.)

**The task:** Crowd workers will submit specific bulleted notes or practice problems that they think are particularly beneficial for a course. This can be customized in many ways, such as responses based on a course's specific unit, content for an upcoming midterm, etc.

## Key Features
1. Workers are able to submimt notes and practice problems.
2. Workers can upvote or downvote on submissions based on the relevance and/or quality of a submission.
3. Workers can auto-generate a cheat sheet based on the most upvoted notes/probelms.

## Feasibility Check
**Data source:** The data will come from students actively enrolled in courses who will submit relevant notes or practice problems for their specific course. Additionally, online resources like textbooks or past exam papers can supplement the data.

**Budget reality:** This project can be developed using existing platforms like MTurk or with a full-stack application developed by the team, thus the budget will not be an issue. 

**Crowd size needed:** The crowd size needed likely depends on the type of course. For university courses, it is more realistic to need 50-100 workers (or just a large portion relative to how big a course is). But it should scale to thouseands of workers for larger, national exams. 

**Quality control approach:** To ensure quality, submissions will be upvoted or downvoted by peers, and only the highest-rated content will appear in the final cheat sheet. Additionally, administrators can spot-check and flag low-quality or irrelevant submissions.

## Technical Approach
**Human tasks:** Humans will submit relevant course notes and practice problems, vote on the submissions, and provide feedback. Human intelligence will be required to understand the course material and assess the usefulness of submissions.

**Automated tasks:** Automation will handle the aggregation of the highest-rated submissions into a final cheat sheet format. Algorithms will also automatically generate personalized cheat sheets based on students' specific preferences or course content.

**Aggregation method:** The submissions will be aggregated by counting votes, and only the highest-rated notes will be included in the final cheat sheet. A weighted system can be implemented where more upvotes from users with a history of high-quality submissions count more.

## Prior Work
**Similar projects:** 

StudySoup: A platform where students upload class notes, and others can purchase or view them. GroupGuide differs by allowing crowdsourced, upvoted submissions that contribute directly to generating cheat sheets.

Quizlet: A platform where users create and share flashcards. Unlike GroupGuide, Quizlet does not focus on generating cheat sheets based on crowd consensus but rather on individual study resources.

**Lessons from past course projects:** Past projects have taught me the importance of user engagement and clear quality control mechanisms. I've learned that automatic aggregation methods (like voting) can improve data quality by focusing on the most relevant submissions.

## Why This Could Work
This project could be viable within the course constraints because it leverages existing crowdsourcing tools, involves simple automated aggregation, and uses scalable techniques like peer voting to ensure high-quality submissions. It can be implemented with minimal upfront costs using free platforms and open-source tools.
