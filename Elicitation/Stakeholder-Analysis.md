# Stakeholder Analysis Report: Tiimo iPhone Churn Reduction Initiative 
 
**Scope**: Stakeholder identification and prioritization for Routines MVP implementation based on Voice of Customer(VOC) analysis of 113 Iphone app reviews

## Executive Summary

This stakeholder analysis supports the strategic recommendation to prioritize Routines feature restoration as the primary initiative to address iPhone user churn. Analysis of 113 Voice of Customer(VOC) reviews reveals Routines complaints represent 23% of total feedback volume, the highest of any issue category while exhibiting a 19.2% churn rate among affected users.

This report operationalizes the above recommendation by identifying decision-makers required for Routines MVP validation and execution.

**Key Finding**: 15 stakeholders have been identified, categorized, and prioritized using the BABOK Guide v3 Power-Interest framework. Phase 1 of elicitation resource allocation focus, centers on 5  high-power, high-interest stakeholders (Product Management, Executive Leadership, Development Lead, Design, and QA teams) who collectively control roadmap decisions, technical feasibility, and resource allocation.

---

## Methodology

### 1. Stakeholder Identification
- **BABOK Technique**: Stakeholder List, Map, and Personas checklist
- **Data Sources**: 
  - Tiimo Case Study Excel workbook (113 reviews: App Store US/UK/AU/NZ, Nolt, Reddit, Blogs)
  - Tiimo public information (website, Apple Award announcement)

- **Categories**: Customers, Internal Strategy, Internal Delivery, External parties

### 2. Power-Interest Scoring
- **Power (1-10)**: Decision-making authority, resource control, organizational influence
- **Interest (1-10)**: Solution impact on stakeholder, engagement level, problem ownership
- **Composite Score**: Power x Interest -> Quadrant assignment

### 3. Elicitation Prioritization
- **Phase 1 (80% elicitation resource allocation)**: Manage Closely stakeholders driving roadmap descisions
- **Phase 2 (15% elicitation resource allocation)**: Delivery teams supporting execution
- **Phase 3 (5% elicitation resource allocation)**: Monitoring and informational updates


## Stakeholder Identification Matrix

![Power-Interest Grid](Screenshot-2026-02-19-at-1.20.34-PM.jpg)


## Quadrant Distribution

### **Manage Closely** (High Power, High Interest)
**Stakeholders**: Product Managers, Executive Management, Development Lead and Teams, Design Lead and Teams, QA Team  
**Engagement**: Weekly touchpoints, collaborative decision-making, solution co-creation  
**Elicitation Priority**: Phase 1 (80% effort)

**Why Critical**: These stakeholders control roadmap, budget, and technical implementation. VOC data shows Routines feature restoration is the top priority, requiring Product to Dev to Design alignment.

### **Keep Informed** (Low Power, High Interest)
**Stakeholders**: Neurodivergent Users, Regular Users, Data Analytics Team, Support Team and Influencers 
**Engagement**: Updates whenever required, feedback loops, metrics dashboards  
**Elicitation Priority**: Phase 3 

**Why Important**: High-interest parties require consistent communication to maintain alignment and gather ongoing input. Neurodivergent users, representing the core target market, provide critical VOC validation through review monitoring and surveys. Support and Analytics teams contribute operational insights via ticket trends and churn metrics.

### **Keep Satisfied** (High Power, Low Interest)
**Stakeholders**: Apple App Store Team  
**Engagement**: Compliance-focused, minimal friction  
**Elicitation Priority**: Phase 3

**Why Necessary**: Regulatory stakeholders demand compliance without deep solution involvement. Engagement focuses on App Store guideline adherence and optimization updates rather than feature-level collaboration.

### **Monitor** (Low Power, Low Interest)
**Stakeholders**: Competitors, Review Platforms 
**Engagement**: Passive monitoring, quarterly reviews  
**Elicitation Priority**: Phase 3 

**Why Monitor**: Competitors inform benchmarking for Routines alternatives, while review platforms enable sentiment tracking to measure post-implementation impact.

---

## Phase 1 Elicitation Plan (80% elicitation resource allocation)

### 1. Product Managers
**Power: 9 | Interest: 10**

**Elicitation Techniques**:
- **Interviews**: Understand product vision, roadmap constraints, competitive positioning
- **Workshops**: Joint RICE/MoSCoW prioritization sessions using VOC data
- **Document Analysis**: Review internal roadmaps, feature backlogs, user research

**Key Questions**:
1. Why was Routines removed in 2025? (22% of reviews cite this)
2. What technical/strategic constraints prevent restoration?
3. How does VOC data (25 Routines requests) align with internal metrics?
4. What ROI threshold justifies Routines MVP?
5. "Does Routines restoration align with 2026 roadmap?"
6. "What's ARR impact of 22% Routines churn rate?"

---

### 2. Executive Management
**Power: 10 | Interest: 10**

**Why Phase 1**:
- Final budget and resource approval
- Set strategic direction for churn reduction
- Define success metrics (ARR retention, App Store rating)

**Elicitation Techniques**:
- **Presentations**: VOC findings, churn analysis, ROI projections
- **Strategic Reviews**: Quarterly business case updates
- **Document Analysis**: Company goals, OKRs, financial targets

**Key Questions**:
1. What churn rate threshold triggers action? (Current: 32.7%)
2. How does iPhone churn impact overall business goals?
3. What budget is available for feature restoration?
4. How does Iphone App of the Year award (2025) factor into strategy?

**VOC Relevance**: 37/113 reviews (32.7%) signal churn—direct impact on revenue and retention KPIs.

---

### 3. Development Lead (Lead Engineer)
**Power: 8 | Interest: 10**

**Why Phase 1**:
- Technical feasibility assessment for Routines MVP
- Architecture decisions, sprint planning, velocity estimates
- Critical for understanding "why" Routines feature was removed

**Elicitation Techniques**:
- **Interviews**: Technical constraints, effort estimates, refactoring needs
- **Workshops**: Solution brainstorming, prototype reviews
- **Observation**: Review existing codebase, architecture docs

**Key Questions**:
1. What technical debt caused Routines removal?
2. Effort and time estimate to restore Routines?
3. Can Routines be MVP'd (subtasks + timers only)?
4. What bugs are quick wins?
5. "Is Routines MVP feasible in 4 sprints?"


---


### 4. Design Lead (Lead UI/UX Designer)
**Power: 8 | InterestL 10**

**Why Phase 1**:
- Critical to interpret VOC/UI complaints into concrete UX problems (clutter, setup friction, loss of routines). 
- Needed to ensure the Routines MVP is neurodivergent‑friendly, not just technically feasible.
- Helps avoid repeating the UX mistakes that triggered churn when routines were removed.

**Elicitation Techniques**: 
- **Interviews**: Past design rationale for removing routines, constraints around complexity, accessibility considerations.
- **Workshops**: Co‑design Routines MVP flows, information architecture, and visual hierarchy using VOC examples.
- **Observation**: Walkthrough of current app (onboarding, planning, AI, calendar) plus review of legacy routines designs and design system.

**Key Questions**:
1. What UX problems was the team trying to solve by removing or changing Routines?
2. How did users actually use old routines (flows, entry points, visual timer) vs what the new design expects?
3. What is the smallest, clearest Routines MVP that still feels neuroinclusive?
4. How can we reduce setup friction and clutter called out in VOC while re‑introducing routines?
5. How should Routines integrate into existing navigation and AI/plans so the experience feels coherent, not bolted on?
6. From a UX standpoint, “Is a usable, testable Routines MVP feasible in 4 sprints?” and what trade‑offs are acceptable?


---

### 5. Competitors (Structured, Llama Life, TickTick)
**Power: 3 | Interest: 3 | Score: 9**

**Why Phase 1 (Monitor)**:
- Benchmarking for Routines alternative implementations
- Understand migration patterns (users explicitly mention switching)
- Validate that Routines restoration is competitive necessity

**Elicitation Techniques**:
- **Competitive Analysis**: Feature parity review (Routines = table stakes?)
- **Document Analysis**: Reddit threads comparing Tiimo to alternatives
- **Market Research**: Pricing, user reviews, feature roadmaps

---


## Assumptions and Limitations

### Assumptions
1. 113 low‑rating Apple device specific reviews are treated as a proxy for dissatisfied paying users, not the full user base. Public data confirms Tiimo has 50k+ paying subscribers and 500k+ free users as of Aug 2024, so VOC is a small but directionally useful sample.
2. VOC tagging shows ~22% of low‑rating issues are Routines related, making it the largest single complaint theme in this sample. Public App Store reviews also repeatedly cite routines removal as a reason to cancel or switch apps, supporting this assumption qualitatively.
3. Where Tiimo’s internal churn is unknown, industry benchmarks for consumer subscription apps (high yearly churn, especially on short plans) are used to build scenarios, not to claim Tiimo’s actual rates.
4. In a real engagement, Product, Design, Engineering, and Data teams are assumed to be accessible for interviews and for validating VOC‑based hypotheses with internal metrics.
5. It is assumed that restoring a limited Routines MVP (saved routines, subtasks with durations, visual timer) is technically and UX‑wise feasible, pending confirmation with Dev and Design Leads.
6. iPhone is treated as the primary platform for this case (aligned with App Store Award 2025 and current product focus), with Android considered secondary due to app removal and limited, fragmented feedback.


### Limitations
1. **No Direct Access to Internal Data**:
The study relies on public information + VOC; there is no access to Tiimo’s internal churn, cohort, or feature usage analytics, so all churn/ARR figures are scenario‑based, not measured.
2. **Consumer‑Skewed VOC**: 
VOC sources (App Stores, Reddit, Nolt) mostly represent individual consumers and neurodivergent self‑users, so team/enterprise or institutional use cases (schools, clinics) are underrepresented.
3. **Platform and Segment Bias**: 
  - The dataset is iPhone‑heavy; Android issues appear in a few reviews (e.g., app removed from Play Store) but are not systematically analyzed.
  - ​English‑language feedback dominates, which may miss regional UX/paywall nuances.
4. **Temporal Lag and Event Clustering**: 
Reviews span 2025–2026, including post‑award and major UX changes (routines removal, AI focus). This captures medium‑term sentiment but not real‑time funnel behavior or the exact timing of churn spikes.
5. **Scenario‑Based Financial Modeling**: 
All user counts, churn rates, and ARR impacts in the business case are explicit scenarios anchored to public user numbers and industry benchmarks, not Tiimo’s actual financials.

---

### Risks

| Risk | Impact | Likelihood | Mitigation (Live Engagement) |
|------|--------|------------|------------------------------|
| Internal analytics contradict VOC (e.g., Routines not top churn driver or over/under‑weighted vs other issues) | High | Medium | Phase 1: Compare VOC issue tags vs. internal churn drivers and feature‑usage data with Data/Analytics team; adjust priorities if internal signals diverge. |
| Technical or UX constraints limit Routines MVP (e.g., architecture, performance, accessibility) | High | Medium | Phase 1: Joint feasibility spike with Dev and Design Leads to define a minimal, neuroinclusive Routines MVP before committing roadmap scope. |
| Budget and capacity insufficient to deliver meaningful Routines MVP | Medium | Low–Medium | Phase 1: Present quantified ARR‑uplift and retention scenarios to Execs, framed against Tiimo’s paying base and subscription benchmarks, to justify investment and phase features if needed. |
| Stakeholder misalignment on priorities (Routines vs AI vs Android vs calendar/bug fixes) | Medium | Medium | Phase 1: Run a cross‑functional RICE/impact workshop using VOC + internal data, explicitly including Android and accessibility considerations, to reach ranked, shared priorities. |
| Platform focus misjudged (e.g., Android or B2B segments become higher priority than iOS routines) | Medium | Medium | Phase 1: Validate platform and segment revenue mix with internal data; if Android or B2B revenue exposure is high, extend analysis to those cohorts and adjust MVP roadmap accordingly. |