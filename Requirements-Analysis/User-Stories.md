
# Tiimo Routines Restoration MVP - User Stories & Acceptance Criteria

## Executive Summary
This document details 12 user stories and their acceptance criteria for the Tiimo Routines Restoration MVP. The stories come from public app reviews showing routines removal as the top iPhone churn reason at 13.5% of cases. They cover creating routines with timed subtasks, visual timers, saving to library, server repeats without crashes, calendar sync, batch adds, and overlap checks. Developers can build these small pieces one sprint at a time with clear tests.

## INVEST Evaluation Summary (Phase 2 Refinement)
All 12 stories reviewed by cross-team (PM/Dev/Design)

| Story | Independent | Negotiable | Valuable | Estimable | Small | Testable |
|-------|-------------|------------|----------|-----------|-------|----------|
| US-FR01 | Yes (no deps) | Yes (workshop) | Yes (13.5% churn) | Yes (5 pts) | Yes | Yes |
| US-FR02 | Yes | Yes | Yes (80% completion) | Yes (5 pts) | Yes | Yes |
| US-FR03 | Yes | Yes | Yes (reuse reqs) | Yes (3 pts) | Yes | Yes |
| US-FR04 | Yes (backend) | Yes | Yes (99% crash-free) | Yes (5 pts) | Yes | Yes |
| US-FR05 | Yes | Yes | Yes (sync bugs) | Yes (5 pts) | Yes | Yes |
| US-FR06 | Yes | Yes | Yes (bulk bugs) | Yes (3 pts) | Yes | Yes |
| US-FR07 | Yes | Yes | Yes (planning) | Yes (3 pts) | Yes | Yes |

## Epic: EP-01 Routines Restoration
As a Tiimo Product Manager,  
I want to restore ADHD routines (create/time/save/sync ≤5 subtasks free in MVP),  
So that users hit 70% adoption, 4.5 rating, cutting churn 20% via review fixes.

## US-FR01: Routine Creation
**User Story**  
As a person with ADHD using Tiimo on iPhone,  
I want to create a new routine with up to 5 subtasks each with its own time duration,  
So that I can quickly build a visual daily flow like brushing teeth then breakfast without spending more than 2 minutes total, fixing the long setup complaints from app reviews.

**Acceptance Criteria**  
**AC1**  
Given I open the routine editor in the Tiimo app,  
When I add up to 5 subtasks and set simple durations like 2 minutes for each,  
Then the app saves the routine instantly to my library and shows it visually with colors and icons.  
**AC2**  
Given I time the full creation of a 5-subtask routine end-to-end,  
When I complete including names, durations, and save,  
Then it takes less than 2 minutes average and less than 3 minutes in 95% of tests.

## US-FR02: Visual Timer
**User Story**  
As a person with ADHD who struggles with time using Tiimo on iPhone,  
I want each subtask in my routine to show a clear countdown timer that auto-advances to the next,  
So that I can complete routines like morning prep at 80% rate or higher, as users miss this in reviews.

**Acceptance Criteria**  
**AC1**  
Given I start a routine subtask with 2-minute duration,  
When the timer runs down,  
Then it displays remaining time visually and auto-advances at zero to next subtask.  
**AC2**  
Given routine screens load on iPhone,  
When accessed,  
Then they appear in under 2 seconds for 95% of cases with no timeouts.

## US-FR03: Save to Library
**User Story**  
As a Tiimo iPhone user with ADHD,  
I want to save my routine to a library and deploy it one-tap to any day,  
So that I reuse flows like weekly clean-up without recreating, based on review requests.

**Acceptance Criteria**  
**AC1**  
Given I create a routine,  
When I save and one-tap deploy to a day,  
Then it appears correctly in library and daily view using server updates.

## US-FR04: Server Repeat Expansion
**User Story**  
As a developer and Tiimo iPhone user with ADHD routines,  
I want the app server to automatically expand repeating routines up to 14 days ahead each night without crashing the phone app,  
So that users see their weekly routines like daily chores ready each morning using small update files only, solving the repeat crash issues many users report in app reviews.

**Acceptance Criteria**  
**AC1**  
Given a routine set to repeat daily for 14 days,  
When the server runs its nightly batch job,  
Then it creates the full list of future tasks and sends only the small changes to the phone app.  
**AC2**  
Given the phone app receives the update while running repeats,  
When it applies the changes,  
Then there are no memory crashes or app freezes in 99% of tests.  
**AC3**  
Given a user opens the app after the nightly update,  
When they view tomorrow's plan,  
Then all expanded routine tasks appear correctly without needing to recreate anything.

## US-FR05: Calendar Sync
**User Story**  
As a Tiimo iPhone user who uses external calendars like Apple or Google,  
I want my routines to sync both ways with those calendars so imports stay saved and new routines add without losing data,  
So that my full weekly plan stays up to date automatically and I avoid daily re-imports as complained in many low reviews.

**Acceptance Criteria**  
**AC1**  
Given I link my external calendar and deploy a routine,  
When changes happen on either side,  
Then they sync bi-directionally keeping all details like times and notes.  
**AC2**  
Given a conflict like overlapping times between routine and calendar event,  
When sync runs,  
Then the app shows a simple choice to resolve and saves the decision.

## US-FR06: Batch Add Tasks
**User Story**  
As a Tiimo iPhone user building long routines,  
I want to safely add multiple routine tasks at once with a progress bar so nothing crashes midway,  
So that I can set up a full day routine quickly without frustration from bugs during bulk adds that users mention.

**Acceptance Criteria**  
**AC1**  
Given I select batch add for 10+ tasks in a routine repeat,  
When the app processes them,  
Then a clear progress bar shows and all tasks add fully with no crashes.

## US-FR07: Conflict Check
**User Story**  
As a Tiimo iPhone user planning routines,  
I want the app to check for time overlaps before deploying a routine and warn me or fix simple ones,  
So that my day schedule stays realistic without manual fixes, addressing planning pains from reviews.

**Acceptance Criteria**  
**AC1**  
Given I try to deploy a routine that overlaps an existing task or calendar event,  
When I confirm,  
Then the app shows a visual warning list and offers auto-shift for easy fixes.  
**AC2**  
Given a simple overlap like 5 minutes,  
When auto-resolve runs,  
Then it adjusts times smoothly and confirms before saving.

## US-SR03: NeuroInclusive Design Integration
**User Story**  
As a Design Lead integrating neuroinclusive UX into Tiimo on iPhone,
I want simplified navigation and AI-suggested routines without clutter,
So that ADHD users can access routines easily while keeping the app calm and focused, fixing the complexity complaints from app reviews.

**Acceptance Criteria**  
**AC1**  
Given I open the routines section in Tiimo,  
When I navigate to create or deploy a routine,  
Then the flow uses simplified steps with AI suggestions and no extra clutter screens.  
**AC2**  
Given neurodivergent users test the design end-to-end,  
When they rate usability on a 1-5 scale,  
Then average score is 4+ with comments on reduced overwhelm.

## US-SR08: Analytics Alignment  
**User Story**  
As a Data Analytics Team member tracking Tiimo churn on iPhone,  
I want to verify approximately 85% alignment between VOC review data and internal cohort metrics,  
So that low-rating reviews serve as reliable churn proxy for prioritization and KPI validation.  

**Acceptance Criteria**  
**AC1**  
Given VOC dataset and internal churn cohorts compared,  
When correlation analysis runs,  
Then 85%+ match confirms reviews predict churn signals.    

## US-NFR04: WCAG AA Accessible Timers  
**User Story**  
As a person with ADHD and time-blindness using Tiimo on iPhone,  
I want routine timers with high-contrast colors that are WCAG AA compliant and neuroinclusive,  
So that I can easily see remaining time even in bright light or with visual processing challenges, meeting accessibility standards while delighting users as noted in Kano analysis.  

**Acceptance Criteria**  
**AC1**  
Given routine timer displays on iPhone in various lighting,  
When tested with high-contrast mode and color-blind simulators,  
Then colors pass WCAG AA contrast ratios (4.5:1 min) and remain time-blind friendly.  
**AC2**  
Given accessibility audit tools scan timer screens,  
When run against WCAG AA guidelines,  
Then zero violations for color, text sizing, and focus indicators.  
​
## US-TR01: Routines User FAQ  
**User Story**  
As a Tiimo Support Team member helping new Routines MVP users on iPhone,  
I want an in-app and website FAQ explaining Routines vs Plans plus common issues,  
So that users resolve questions quickly without tickets, reducing post-launch churn from confusion.  

**Acceptance Criteria**  
**AC1**  
Given FAQ published in app settings and tiimo.com/support,  
When users search "routines vs plans",  
Then clear answers appear covering differences and fixes.  
**AC2**  
Given support ticket volume tracked 30 days post-launch,  
When compared to pre-MVP baseline,  
Then Routines-related tickets drop 50%.  
​

## US-TR02: Onboarding Video  
**User Story**  
As a new Tiimo iPhone user with ADHD learning Routines MVP,  
I want a 3-minute paced video tutorial for routine setup flow,  
So that I complete first routine at 80% success rate without frustration from setup complaints in reviews.  

**Acceptance Criteria**  
**AC1**  
Given video embedded in onboarding after MVP launch,  
When new users watch and follow steps,  
Then 80% create first routine successfully per analytics.  
**AC2**  
Given video tested for timing,  
When played end-to-end,  
Then total length less than or equal to 3 minutes with ADHD-friendly pacing.  
**AC3**  
Given video content reviewed,  
When step-by-step demo checked,  
Then it matches exact routine creation flow from app.  
**AC4**  
Given accessibility audit run,  
When WCAG AA criteria tested,  
Then video has captions, replay button, and passes compliance.  