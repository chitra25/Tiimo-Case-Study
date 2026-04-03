# BPMN Process Redesign : Tiimo iPhone Churn Reduction Initiative

## Executive Summary

Tiimo faces 13.5% churn from Routines feature gaps, per VOC reviews. This document presents a comprehensive BPMN 2.0 process analysis for Tiimo's task creation functionality. It identifies critical failures in the current As-Is process that contribute to 22% of low-rating App Store complaints and recommends a scalable To-Be architecture. By moving repeat expansion to server-side batch processing, the solution reduces routine setup time from 15 minutes to 90 seconds and eliminates out-of-memory crashes entirely.


## As-Is Process Flow : Current Task Creation Flow

The existing process follows these steps:

1. The user begins task creation via the Start Event.
2. They input title, scroll-select time, choose emoji, and define repeat schedule (e.g., Monday/Wednesday/Friday).
3. The client application attempts to expand the repeat pattern into individual calendar instances.
4. For complex schedules, this triggers an out-of-memory crash, captured by the thick interrupting boundary event.
5. Survivors reach "Save task," but often encounter thin non-interrupting sync errors.
6. Flow terminates via End Event after an average 15-minute ordeal.


![As-Is BPMN](/Stakeholder-Engagement-And-Elicitation/Current-State-Diagram.png)


## To-Be Process Flow : Scalable Architecture

The redesigned process eliminates client burden through server intelligence:

1. User inputs routine details, defining only the repeat pattern (e.g., "M/W/F at 9AM").
2. Application sends pattern to server via "Store schedule pattern" task.
3. Server-side Timer Intermediate Event activates nightly at midnight.
4. Collapsed Subprocess "[+] Generate calendar instances" expands pattern for next 14 days.
5. Server publishes lightweight deltas ("Add 10 events") to subscribed clients.
6. Flow completes via Success End Event in 90 seconds.


![To-Be BPMN](/Requirements-Analysis-And-Prioritization/Future-State-Diagram.png)
