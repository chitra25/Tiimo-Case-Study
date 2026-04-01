# Tiimo iPhone Churn Reduction: Kano Analysis Documentation

## Executive Summary

This document details the Power BI dashboard exported as [Kano-Analysis.pdf](/docs/Kano-Analysis.pdf), created to prioritize features for the Routines MVP using public VOC data from 113 low-rating iPhone reviews. As a hypothetical study without customer access, VOC themes (e.g., **Routines 22% volume, 13.5% churn signals**) served as a proxy for Kano surveys: hypotheses classified features, computed Dissatisfaction/Satisfaction % via formulas, then plotted quadrants with RICE integration for MVP scoping.

## Kano Visual Overview

![Kano Analysis Visual](/images/Kano-Analysis-Chart.png)

The visual features:
- **Scatter Plot**: Kano quadrant (Dissatisfaction → Satisfaction axes) showing 25 features colored by status (if the feature is included in MVP or not)
- **Key Metrics**: MVP count (**17**), top RICE (**60.0**), VOC-derived clusters.


## Methodology: VOC Proxy for Kano

Traditional Kano requires customer surveys (functional/dysfunctional questions), but here:

- **VOC Input**: Analyzed 113 reviews for feature sentiment.
- **Must-be**: Frequent complaints (e.g., *"routines gone"* → high dissatisfaction if absent).
- **Performance**: Linear praise/critique (e.g., *"timer crashes"*).
- **Attractive**: Unexpected delights (e.g., WCAG accessibility).
- **Indifferent**: Neutral/no mentions.

**Hypothesis & Scoring**: Assigned % based on review frequency/strength (e.g., **25 Routines reviews → high dissat** for absence).  
**RICE Overlay**: Reach (VOC freq), Impact (churn signals), Confidence (hypothesis), Effort (est dev).  
**Quadrant Plot**: Position = (Satisfaction %, **-Dissatisfaction %**).

*Hypothetical "responses" derived from review proxies.*

## Key Visuals & Data Table

**Extracted Table** (*from dashboard*):

| Feature            | Kano        | RICE Score | Dissat % | Sat % | Status      |
|---------------------|-------------|-------------|----------|--------|-------------|
| Routine Creation    | Performance | 60.0        | 78       | 49     | 🟢 MVP      |
| Visual Timer        | Must-be     | 60.0        | 79       | 50     | 🟢 MVP      |
| Crash-Free          | Must-be     | 60.0        | 77       | 47     | 🟢 MVP      |
| Save Library        | Performance | 48.6        | 67       | 48     | 🟢 MVP      |
| Video               | Performance | 51.2        | 65       | 51     | 🟢 MVP      |
| WCAG AA             | Attractive  | 57.6        | 74       | 55     | 🟢 MVP      |
| Server Exp          | Must-be     | 32.4        | 71       | 37     | 🟢 MVP      |
| ADHD Flow           | Must-be     | 36.0        | 72       | 38     | 🟢 MVP      |
| Timer Refactor      | Must-be     | 38.4        | 73       | 40     | 🟢 MVP      |
| FAQ                 | Must-be     | 42.0        | 70       | 42     | 🟢 MVP      |
| Load Performance    | Must-be     | 48.0        | 67       | 48     | 🟢 MVP      |
| Create Time         | Must-be     | 54.0        | 75       | 52     | 🟢 MVP      |
| Neuro Design        | Performance | 32.4        | 58       | 44     | 🟢 MVP      |
| Calendar Sync       | Performance | 28.8        | 69       | 37     | 🟢 MVP      |
| Conflict Check      | Performance | 29.4        | 70       | 37     | 🟢 MVP      |
| Batch Add           | Performance | 30.4        | 64       | 40     | 🟢 MVP      |
| Drag Reschedule     | Attractive  | 28.0        | 62       | 47     | 🟡 Post-MVP |
| AI Routine Gen      | Attractive  | N/A         | 50       | 70     | 🟡 Post-MVP |
| Manual Emoji Picker | Indifferent | N/A         | 20       | 27     | 🔴 Excluded |
| Rollover Sound      | Indifferent | N/A         | 18       | 30     | 🔴 Excluded |
| Subtask Color       | Indifferent | N/A         | 22       | 31     | 🔴 Excluded |

**Quadrant Insights**:
- **Must-be (8 MVP)**: Basic hygiene (e.g., no crashes)—addresses **22% Routines complaints**.
- **Performance (9 MVP)**: Linear value (e.g., faster creation **<2min**).
- **Attractive (3)**: Delighters like WCAG for retention.
- **Indifferent (3 Excluded)**: Low VOC impact.

## MVP Prioritization Outcomes

Dashboard scoped MVP to **17 features (RICE ≥28.8)**, directly traceable to reqs/tests:
- **Top**: Routine Creation/Visual Timer/Crash-Free (**60.0**) → **FR-01/FR-02/NFR-03**.
- **Projected**: **13.5% churn reduction**, **0.5-star rating uplift** via Must-be fixes.