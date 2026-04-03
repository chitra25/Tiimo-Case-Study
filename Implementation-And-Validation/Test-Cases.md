# Tiimo Routines Restoration MVP - Test Cases

## Executive Summary  
This test cases document supports the Tiimo iPhone Churn Reduction case study by providing verifiable test coverage for the Routines Restoration MVP. Derived directly from seven functional user stories and acceptance criteria, it includes one primary test case per requirement, ensuring traceability to the requirements catalog.

## Detailed Test Cases

### TC-FR01-001: Routine Creation with Subtasks. 
**Description**: Verify user can create a routine with up to 5 subtasks and durations, saving instantly.   
**Preconditions**: Tiimo iPhone app open, user logged in, routine editor accessible.    

**Test Steps**:  
1. Navigate to routine editor.
2. Add 5 subtasks with names and 2-min durations.
3. Save routine.  

**Expected Result**: Routine saves instantly to library, displays visually with colors/icons, end-to-end less than 2 min avg.  
**Status**: Not Executed | **Priority**: High  

### TC-FR02-001: Visual Timer Auto-Advance   
**Description**: Confirm subtask timer shows countdown and auto-advances.  
**Preconditions**: Routine with timed subtasks exists. 

**Test Steps**:  
1. Start 2-min subtask.  
2. Monitor until zero.  

**Expected Result**: Visual countdown displays, auto-advances to next, screen loads less than 2s (95%).  
**Status**: Not Executed | **Priority**: High

### TC-FR03-001: Save and Deploy Routine  
**Description**: Ensure routine saves to library and deploys one-tap.  
**Preconditions**: New routine created, server sync enabled.

**Test Steps**:
1. Save routine to library.
2. One-tap deploy to a day.

**Expected Result**: Appears in library and daily view via server.  
**Status**: Not Executed | **Priority**: Medium

### TC-FR04-001: Server Repeat Expansion  
**Description**: Validate 14-day repeat expansion without crashes.  
**Preconditions**: Routine set daily repeat 14 days, simulate nightly job.

**Test Steps**:
1. Run server batch.
2. Receive delta in app.
3. View tomorrow's plan.

**Expected Result**: Tasks expanded; no crashes (99%), small updates only.  
**Status**: Not Executed | **Priority**: High

### TC-FR05-001: Bi-Directional Calendar Sync  
**Description**: Test sync with external calendars, including conflicts.  
**Preconditions**: Apple/Google calendar linked.

**Test Steps**:
1. Deploy routine.
2. Edit in external calendar.
3. Sync and resolve conflict.

**Expected Result**: Bi-directional sync, details preserved, simple choices shown.  
**Status**: Not Executed | **Priority**: High

### TC-FR06-001: Batch Add Routine Tasks  
**Description**: Confirm batch add with progress bar, no crashes.  
**Preconditions**: Routine editor open.

**Test Steps**:
1. Select batch add 10+ tasks.
2. Process batch.

**Expected Result**: Progress bar shows, all tasks added fully.  
**Status**: Not Executed | **Priority**: Medium

### TC-FR07-001: Routine Overlap Conflict Check  
**Description**: Verify overlap warnings and auto-resolve.  
**Preconditions**: Overlapping task/event exists.

**Test Steps**:
1. Deploy overlapping routine.
2. Confirm warnings; auto-shift 5-min overlap.

**Expected Result**: Visual list shown, times adjust smoothly.  
**Status**: Not Executed | **Priority**: Medium

### TC-SR03-001: Neuroinclusive Design Integration  
**Description**: Verify simplified nav and AI suggestions without clutter.  
**Preconditions**: Routines section open.

**Test Steps**:
1. Navigate to create/deploy routine.
2. Observe AI suggestions.

**Expected Result**: Simplified flow, no clutter.  
**Status**: Not Executed | Priority: High

### TC-SR08-001: Analytics Alignment  
**Description**: Confirm 85% VOC-internal churn match.  
**Preconditions**: VOC dataset and cohorts available.

**Test Steps**:
1. Run correlation analysis.

**Expected Result**: greater than or equal to 85% match, reviews predict churn.  
**Status**: Not Executed | Priority: Medium

### TC-NFR04-001: WCAG AA Accessible Timers  
**Description**: Validate high-contrast timers.   
**Preconditions**: Timer screen active.  

**Test Steps**:
1. Test in various lighting/color sims.
2. Run WCAG audit.

**Expected Result**: Passes 4.5:1 contrast, zero violations.  
**Status**: Not Executed | Priority: High

### TC-TR01-001: Routines User FAQ  
**Description**: Check FAQ accessibility.  
**Preconditions**: App/website post-launch.

**Test Steps**:
1. Search routines vs plans.
2. Monitor tickets 30 days.

**Expected Result**: Answers appear, tickets drop 50%.  
**Status**: Not Executed | Priority: Medium  

### TC-TR02-001: Onboarding Video  
**Description**: Verify video tutorial effectiveness.  
**Preconditions**: Onboarding flow.  

**Test Steps**:
1. Watch/play video.
2. Follow steps to create routine.
3. Audit accessibility.

**Expected Result**: less than 3 min, WCAG AA pass.  
**Status**: Not Executed | Priority: Medium