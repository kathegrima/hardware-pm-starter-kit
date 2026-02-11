# Engineering Change Request (ECR) / Engineering Change Order (ECO) Template

> **Formal change control process for hardware design changes**

---

## Table of Contents

1. [Introduction](#introduction)
2. [Change Control Process Overview](#change-control-process-overview)
3. [When to Use ECR/ECO](#when-to-use-ecreco)
4. [ECR Form Template](#ecr-form-template)
5. [ECO Form Template](#eco-form-template)
6. [Change Impact Assessment](#change-impact-assessment)
7. [Change Classification](#change-classification)
8. [Approval Workflow](#approval-workflow)
9. [Implementation & Verification](#implementation--verification)
10. [Change Log & Tracking](#change-log--tracking)

---

## Introduction

### What is ECR/ECO?

**ECR (Engineering Change Request)**:
- Proposal for a design change
- Submitted by anyone (engineering, QA, manufacturing, customer support)
- Includes problem description, proposed solution, justification
- Status: Pending review and approval

**ECO (Engineering Change Order)**:
- Approved change request
- Authorized for implementation
- Includes implementation plan, verification plan, approvals
- Status: Approved → In Progress → Complete

---

### Why Change Control Matters

**Without formal change control**:
- ❌ Undocumented changes → can't reproduce older builds
- ❌ Unintended consequences → change breaks other features
- ❌ Configuration confusion → which units have which changes?
- ❌ Compliance issues → can't prove what was shipped
- ❌ Cost overruns → unplanned tooling changes, inventory obsolescence

**With formal change control**:
- ✅ Traceability → every change documented, approved, tracked
- ✅ Impact assessment → understand ripple effects before implementing
- ✅ Configuration management → know exactly what's in each build
- ✅ Compliance → audit trail for regulatory requirements
- ✅ Cost control → evaluate cost/benefit before approving changes

---

### Change Control Milestones

**Design Freeze (DVT Exit)**:
- **Before design freeze**: Informal change process OK (email, Jira ticket)
- **After design freeze**: Formal ECR/ECO process REQUIRED

**Reason**: After DVT, design is validated (tested, compliant, manufacturable). Changes risk regression, retest, recertification.

---

## Change Control Process Overview

### Process Flow

```
1. IDENTIFY NEED
   ├─ Issue found (bug, field failure, cost reduction opportunity)
   └─ Solution proposed

2. SUBMIT ECR
   ├─ Fill out ECR form
   ├─ Describe problem, proposed solution, justification
   └─ Submit to Change Control Board (CCB)

3. REVIEW ECR (CCB Meeting)
   ├─ Assess impact (technical, cost, schedule, compliance)
   ├─ Evaluate alternatives
   ├─ Decision: Approve / Reject / Defer / Request More Info
   └─ If approved → Convert ECR to ECO

4. IMPLEMENT ECO
   ├─ Update design (schematic, PCB, firmware, mechanical, BOM)
   ├─ Update documentation (manuals, test procedures, labels)
   ├─ Procure new components (if BOM change)
   └─ Build prototype with change

5. VERIFY ECO
   ├─ Test prototype (regression testing + change-specific testing)
   ├─ Verify issue resolved
   └─ Verify no new issues introduced

6. CLOSE ECO
   ├─ CCB reviews verification results
   ├─ Approve release to production
   └─ Update all affected documents and systems
```

---

### Change Control Board (CCB)

**Purpose**: Evaluate and approve/reject change requests

**Members**:
- **Project Manager** (chair) - Schedule, budget, overall impact
- **Hardware Lead** - Technical feasibility, hardware impact
- **Firmware Lead** - Firmware impact
- **Mechanical Lead** - Mechanical impact
- **Manufacturing** - Manufacturability, tooling, yield impact
- **QA/Test** - Testing impact, regression risk
- **Compliance** - Regulatory impact (retest, recertification)
- **Supply Chain** - BOM impact, lead time, cost

**Meeting Cadence**:
- **Before Design Freeze**: As needed (informal)
- **After Design Freeze**: Weekly or bi-weekly (formal)

---

## When to Use ECR/ECO

### REQUIRED (Must Use ECR/ECO)

**After Design Freeze (DVT Exit)**:
- ✅ Any change to frozen design (schematic, PCB, BOM, firmware, mechanical, labels)
- ✅ Changes affecting compliance (EMC, safety, RoHS)
- ✅ Changes affecting form/fit/function (customer-visible)
- ✅ Changes affecting manufacturing (assembly process, test procedure, tooling)

**Example Scenarios**:
- Change resistor value from 10kΩ to 4.7kΩ (affects circuit function)
- Replace component due to EOL (different MPN)
- Add test point to PCB (PCB layout change)
- Update enclosure to fix assembly issue (tooling change)
- Update firmware to fix critical bug (regression risk)

---

### OPTIONAL (Use Judgment)

**Before Design Freeze (EVT/DVT)**:
- Iterative design changes (expected during development)
- Minor tweaks (passive value changes during tuning)
- Firmware updates (separate version control typically sufficient)

**Best Practice**: Even before freeze, use ECR/ECO for major changes (e.g., swap MCU, change sensor, major mechanical redesign)

---

### NOT REQUIRED

- Firmware-only changes (use separate firmware change control)
- Documentation updates (typo fixes, formatting)
- Internal process changes (doesn't affect product)

---

## ECR Form Template

### Engineering Change Request (ECR)

**ECR Number**: ECR-[YYYY]-[XXX] (e.g., ECR-2026-042)  
**Date Submitted**: [YYYY-MM-DD]  
**Submitted By**: [Name, Title]  
**Project**: [Project Name]  
**Product**: [Product Name]  
**Current Revision**: [Hardware Rev, Firmware Version]

---

### 1. Change Request Summary

**Change Title**: [Brief description, e.g., "Replace 10kΩ resistor R5 with 4.7kΩ"]

**Change Type**: [ ] Hardware [ ] Firmware [ ] Mechanical [ ] BOM [ ] Documentation [ ] Process [ ] Other: _______

**Change Classification**: [ ] Critical [ ] Major [ ] Minor (see [Change Classification](#change-classification))

**Affected Documents/Assemblies**:
- [ ] Schematic (Rev: ___)
- [ ] PCB Layout (Rev: ___)
- [ ] BOM (Rev: ___)
- [ ] Firmware (Version: ___)
- [ ] Mechanical (Rev: ___)
- [ ] User Manual (Rev: ___)
- [ ] Test Procedures (Rev: ___)
- [ ] Other: _______________________________

---

### 2. Problem Description

**What is the problem/opportunity?**
[Describe the issue that requires this change]

**Severity**: [ ] Critical (product unusable) [ ] High (major feature broken) [ ] Medium (minor issue) [ ] Low (improvement)

**Affected Units**:
- [ ] Prototype only (EVT/DVT/PVT)
- [ ] Production units
- [ ] Serial Number Range: From _______ To _______
- [ ] Quantity Affected: _______ units

**Failure Evidence** (if applicable):
- Failure Rate: _______ % (failures / total units)
- Failure Mode: _______________________________
- Root Cause: _______________________________
- Evidence: [Link to failure analysis, photos, test data]

---

### 3. Proposed Solution

**Describe the proposed change**:
[Detailed description of what will change]

**Why this solution?**
[Justification - why is this the best approach?]

**Alternatives Considered**:
1. Alternative 1: _______________________________
   - Pros: _______________________________
   - Cons: _______________________________
   - Rejected because: _______________________________

2. Alternative 2: _______________________________
   - Pros: _______________________________
   - Cons: _______________________________
   - Rejected because: _______________________________

---

### 4. Impact Assessment (Preliminary)

**Technical Impact**:
- [ ] Hardware: _______________________________
- [ ] Firmware: _______________________________
- [ ] Mechanical: _______________________________
- [ ] Performance: _______________________________
- [ ] Compatibility (backward/forward): _______________________________

**Cost Impact**:
- NRE (Non-Recurring Engineering): €_______
  - Design time: _______ hours × €_______ = €_______
  - Prototype build: €_______
  - Testing/validation: €_______
  - Tooling changes: €_______
- Recurring Cost (per unit): €_______ → €_______ (change: €_______)
- Inventory Obsolescence: €_______ (existing stock to scrap/rework)
- **Total Cost**: €_______

**Schedule Impact**:
- Design time: _______ weeks
- Prototype build time: _______ weeks
- Testing/validation time: _______ weeks
- **Total schedule impact**: _______ weeks
- Affects launch date? [ ] Yes [ ] No (new date: _______)

**Compliance Impact**:
- [ ] No impact (change doesn't affect compliance)
- [ ] Requires retest: [ ] EMC [ ] LVD [ ] RED [ ] RoHS [ ] Other: _______
  - Estimated retest cost: €_______
  - Estimated retest time: _______ weeks
- [ ] Requires recertification (full compliance cycle)

**Manufacturing Impact**:
- [ ] No impact
- [ ] Assembly process change (describe: _______________________________)
- [ ] Tooling change (describe: _______________________________)
- [ ] Test procedure change (describe: _______________________________)
- [ ] Yield impact: Current: ____% → Expected: ____%

---

### 5. Requested Approval

**Urgency**: [ ] Critical (blocks production) [ ] High (needed soon) [ ] Medium (next build) [ ] Low (future improvement)

**Requested Effective Date**: [YYYY-MM-DD or Build #]

**Implementation Plan** (if approved):
1. [Step 1]
2. [Step 2]
3. [Step 3]
...

**Verification Plan** (if approved):
- [ ] Unit test (describe: _______________________________)
- [ ] Integration test (describe: _______________________________)
- [ ] Regression test (describe: _______________________________)
- [ ] Environmental retest (if applicable)
- [ ] Compliance retest (if applicable)

---

### 6. CCB Review (To Be Completed by CCB)

**CCB Meeting Date**: [YYYY-MM-DD]

**Decision**: [ ] Approved → Convert to ECO [ ] Rejected [ ] Deferred [ ] Request More Info

**Decision Rationale**:
[Why was this approved/rejected/deferred?]

**Conditions** (if approved):
[Any conditions or requirements for implementation]

**ECO Number Assigned** (if approved): ECO-[YYYY]-[XXX]

**Approvals**:
| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Manager | _______ | _______ | _______ |
| Hardware Lead | _______ | _______ | _______ |
| Firmware Lead | _______ | _______ | _______ |
| Mechanical Lead | _______ | _______ | _______ |
| Manufacturing | _______ | _______ | _______ |
| QA/Test | _______ | _______ | _______ |
| Compliance | _______ | _______ | _______ |

---

## ECO Form Template

### Engineering Change Order (ECO)

**ECO Number**: ECO-[YYYY]-[XXX] (e.g., ECO-2026-042)  
**ECR Number**: ECR-[YYYY]-[XXX] (source ECR)  
**Date Approved**: [YYYY-MM-DD]  
**Project**: [Project Name]  
**Product**: [Product Name]

---

### 1. ECO Summary

**Change Title**: [Same as ECR]

**Change Owner**: [Name - responsible for implementation]

**Target Completion Date**: [YYYY-MM-DD]

**Effective Date/Build**: [YYYY-MM-DD or Build #___]

**Previous Revision**: [Hardware Rev ___, Firmware Version ___, BOM Rev ___]  
**New Revision**: [Hardware Rev ___, Firmware Version ___, BOM Rev ___]

---

### 2. Change Description

[Copy from approved ECR, or refine if needed]

---

### 3. Detailed Implementation Plan

**Design Changes**:
- [ ] Schematic
  - File: _______________________________
  - Changes: _______________________________
  - Rev: ___ → ___
  - Responsible: _______ Due: _______

- [ ] PCB Layout
  - File: _______________________________
  - Changes: _______________________________
  - Rev: ___ → ___
  - Responsible: _______ Due: _______

- [ ] BOM
  - File: _______________________________
  - Changes: _______________________________
  - Rev: ___ → ___
  - Responsible: _______ Due: _______

- [ ] Firmware
  - File: _______________________________
  - Changes: _______________________________
  - Version: ___ → ___
  - Responsible: _______ Due: _______

- [ ] Mechanical
  - File: _______________________________
  - Changes: _______________________________
  - Rev: ___ → ___
  - Responsible: _______ Due: _______

**Documentation Changes**:
- [ ] User Manual (Rev: ___ → ___, Responsible: _______, Due: _______)
- [ ] Test Procedures (Rev: ___ → ___, Responsible: _______, Due: _______)
- [ ] Compliance Documents (Rev: ___ → ___, Responsible: _______, Due: _______)
- [ ] Other: _______ (Rev: ___ → ___, Responsible: _______, Due: _______)

**Procurement Changes** (if BOM change):
- [ ] Order new components: _______ (MPN: _______, Qty: _______, Lead Time: ___ weeks)
- [ ] Obsolete existing stock: _______ (Qty: _______, Value: €_______, Disposition: Scrap/Rework/Return)

**Tooling Changes** (if mechanical change):
- [ ] Update injection mold tool: _______ (Cost: €_______, Lead Time: ___ weeks)
- [ ] Update fixtures/jigs: _______ (Cost: €_______, Lead Time: ___ weeks)

---

### 4. Verification Plan

**Prototype Build**:
- [ ] Build _______ prototype units with change
- [ ] Target Date: _______
- [ ] Responsible: _______

**Testing**:
- [ ] **Unit Test** (Change-specific)
  - Test: _______________________________
  - Pass Criteria: _______________________________
  - Responsible: _______ Due: _______

- [ ] **Regression Test** (Verify no new issues)
  - Tests: [List critical tests to repeat]
  - Pass Criteria: All tests pass (same as pre-change)
  - Responsible: _______ Due: _______

- [ ] **Environmental Retest** (if applicable)
  - Tests: [ ] Temperature [ ] Humidity [ ] Drop [ ] Vibration
  - Pass Criteria: Same as original qualification
  - Responsible: _______ Due: _______

- [ ] **Compliance Retest** (if applicable)
  - Tests: [ ] EMC [ ] LVD [ ] RED [ ] RoHS
  - Cost: €_______
  - Lab: _______
  - Lead Time: _______ weeks
  - Responsible: _______ Due: _______

**Acceptance Criteria**:
- [ ] All verification tests pass
- [ ] Issue resolved (original problem fixed)
- [ ] No new issues introduced
- [ ] Performance within specification

---

### 5. Risk Assessment

**Risks**:
| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| [Risk 1] | [ ] High [ ] Med [ ] Low | [ ] High [ ] Med [ ] Low | [Mitigation plan] |
| [Risk 2] | [ ] High [ ] Med [ ] Low | [ ] High [ ] Med [ ] Low | [Mitigation plan] |
| ... | [ ] High [ ] Med [ ] Low | [ ] High [ ] Med [ ] Low | [Mitigation plan] |

**Rollback Plan** (if change fails):
[How to revert to previous design if this change doesn't work]

---

### 6. Cost Summary (Final)

| Cost Category | Estimate (ECR) | Actual | Variance |
|--------------|----------------|--------|----------|
| Design Labor | €_______ | €_______ | €_______ |
| Prototype Build | €_______ | €_______ | €_______ |
| Testing/Validation | €_______ | €_______ | €_______ |
| Tooling Changes | €_______ | €_______ | €_______ |
| Component Cost (Δ per unit) | €_______ | €_______ | €_______ |
| Inventory Obsolescence | €_______ | €_______ | €_______ |
| Compliance Retest | €_______ | €_______ | €_______ |
| **Total NRE** | **€_______** | **€_______** | **€_______** |
| **Recurring (per unit)** | **€_______** | **€_______** | **€_______** |

---

### 7. Implementation Status

**Status**: [ ] Not Started [ ] In Progress [ ] Verification [ ] Complete

**Progress Log**:
| Date | Milestone | Status | Notes |
|------|-----------|--------|-------|
| _______ | Design changes complete | [ ] Done [ ] In Progress | _______ |
| _______ | Documentation updated | [ ] Done [ ] In Progress | _______ |
| _______ | Prototype built | [ ] Done [ ] In Progress | _______ |
| _______ | Testing complete | [ ] Done [ ] In Progress | _______ |
| _______ | CCB review (closure) | [ ] Done [ ] In Progress | _______ |

**Issues/Blockers**:
[List any issues or blockers preventing completion]

---

### 8. Verification Results

**Test Results**:
| Test | Expected Result | Actual Result | Pass/Fail |
|------|----------------|---------------|-----------|
| [Test 1] | _______ | _______ | [ ] Pass [ ] Fail |
| [Test 2] | _______ | _______ | [ ] Pass [ ] Fail |
| ... | _______ | _______ | [ ] Pass [ ] Fail |

**Issue Resolution Confirmed**: [ ] Yes [ ] No (if no, explain: _______)

**New Issues Found**: [ ] None [ ] Yes (list: _______________________________)

**Verification Summary**:
[Overall assessment of verification results]

---

### 9. CCB Approval (Closure)

**CCB Review Date**: [YYYY-MM-DD]

**Decision**: [ ] Approve Release to Production [ ] Reject (revert to previous design) [ ] Request Rework

**Release Effective Date/Build**: [YYYY-MM-DD or Build #___]

**Dispositions**:
- [ ] Old revision: Scrap / Rework / Ship as-is (with deviation) / Return to supplier
- [ ] New revision: Release to production

**Final Approvals**:
| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Manager | _______ | _______ | _______ |
| Change Owner | _______ | _______ | _______ |
| Hardware Lead | _______ | _______ | _______ |
| QA/Test | _______ | _______ | _______ |
| Manufacturing | _______ | _______ | _______ |

---

### 10. Document Updates

**All affected documents updated**:
- [ ] Schematic (Rev: ___, Date: _______)
- [ ] PCB Layout (Rev: ___, Date: _______)
- [ ] BOM (Rev: ___, Date: _______)
- [ ] Firmware (Version: ___, Date: _______)
- [ ] Mechanical (Rev: ___, Date: _______)
- [ ] User Manual (Rev: ___, Date: _______)
- [ ] Test Procedures (Rev: ___, Date: _______)
- [ ] Compliance Documents (Rev: ___, Date: _______)
- [ ] ERP/PLM System updated (SKU, BOM, routing): [ ] Yes [ ] No

**Archived**:
- [ ] Old revision design files archived (location: _______________________________)
- [ ] ECR/ECO documents archived (location: _______________________________)

---

## Change Impact Assessment

### Impact Categories

**Technical Impact**:
- [ ] Hardware design (schematic, PCB, components)
- [ ] Firmware (code changes, config changes)
- [ ] Mechanical design (enclosure, mounting, dimensions)
- [ ] Performance (speed, accuracy, power consumption, battery life)
- [ ] Reliability (MTBF, failure modes)
- [ ] Electromagnetic compatibility (EMC)
- [ ] Safety (electrical, mechanical, thermal)
- [ ] User experience (UI, usability)

**Cost Impact**:
- **NRE (Non-Recurring Engineering)**: One-time cost to implement change
  - Design labor: _______ hours × €______/hr = €_______
  - Prototype build: €_______
  - Testing: €_______
  - Tooling: €_______
  - Compliance retest: €_______
- **Recurring Cost**: Per-unit cost change
  - Component cost delta: €_______
  - Assembly labor delta: €_______
  - Total per-unit delta: €_______
- **Inventory Impact**: 
  - Obsolete stock value: €_______
  - Disposition cost (scrap/rework): €_______

**Schedule Impact**:
- Design time: _______ weeks
- Procurement (if new components): _______ weeks
- Build time: _______ weeks
- Test time: _______ weeks
- Compliance retest (if applicable): _______ weeks
- **Total schedule impact**: _______ weeks
- **Launch date impact**: Delays launch by _______ weeks (new date: _______)

**Compliance Impact**:
- [ ] No impact (change doesn't affect tested configuration)
- [ ] Requires retest (specific tests, e.g., EMC radiated emissions only)
- [ ] Requires recertification (full compliance cycle, new Declaration of Conformity)

**Manufacturing Impact**:
- [ ] No impact (drop-in change)
- [ ] Assembly process change (new work instructions, training)
- [ ] Tooling change (fixtures, jigs, molds)
- [ ] Test procedure change (new test steps, equipment)
- [ ] Yield impact (expected change in first-pass yield)

**Field Impact** (if retroactive fix needed):
- [ ] No field impact (future units only)
- [ ] Field upgrade available (firmware update, service bulletin)
- [ ] Field upgrade required (safety/compliance)
- [ ] Product recall required (critical safety issue)

---

### Impact Assessment Checklist

Use this checklist to ensure all impacts are considered:

- [ ] **Hardware impact assessed** (schematic, PCB, BOM changes?)
- [ ] **Firmware impact assessed** (code changes, compatibility?)
- [ ] **Mechanical impact assessed** (enclosure, tooling changes?)
- [ ] **Cost impact calculated** (NRE + recurring + inventory)
- [ ] **Schedule impact estimated** (design, build, test time)
- [ ] **Compliance impact evaluated** (retest needed?)
- [ ] **Manufacturing impact assessed** (process, tooling, yield?)
- [ ] **Testing plan defined** (what tests needed to verify change?)
- [ ] **Risk assessment complete** (what could go wrong?)
- [ ] **Alternatives considered** (is this the best solution?)
- [ ] **Rollback plan defined** (how to revert if change fails?)

---

## Change Classification

### Critical Change

**Definition**: Change affecting safety, compliance, or core functionality

**Examples**:
- Safety-related changes (electrical, thermal, mechanical)
- Compliance-related changes (affects EMC, LVD, RED, RoHS)
- Core functionality broken (product unusable)
- Major performance degradation (>20% from spec)

**Approval Required**:
- Full CCB approval (all members must sign)
- Executive approval (if affects launch date or budget >10%)

**Testing Required**:
- Full regression testing
- Compliance retesting (if affected)
- Field trial (if feasible)

**Effective Date**:
- Immediate (if safety/compliance)
- Next build (if functionality)

---

### Major Change

**Definition**: Significant design change with moderate impact

**Examples**:
- Component substitution (not pin-compatible)
- PCB layout change (routing, layer stack)
- Mechanical design change (enclosure, mounting)
- Firmware architecture change
- Performance optimization (>10% improvement)

**Approval Required**:
- CCB approval (majority vote)
- PM approval (if schedule impact >1 week or cost >€5K)

**Testing Required**:
- Targeted testing (change-specific)
- Partial regression testing (affected subsystems)

**Effective Date**:
- Next build (typically)

---

### Minor Change

**Definition**: Small change with limited impact

**Examples**:
- Passive component value tweak (resistor, capacitor)
- Pin-compatible component substitution (second source)
- Cosmetic change (label, color)
- Documentation update (typo fix, clarification)
- Test procedure improvement

**Approval Required**:
- Change Owner + PM approval (expedited)
- CCB notification (no meeting required)

**Testing Required**:
- Basic functional test (smoke test)
- Change-specific verification only

**Effective Date**:
- Next build or ASAP

---

## Approval Workflow

### Pre-Design Freeze (EVT/DVT)

**Process**: Lightweight, email-based

1. Engineer identifies need for change
2. Engineer emails PM + Leads with description
3. PM approves (or escalates to CCB if major)
4. Engineer implements change
5. Engineer documents change in design files (commit message, revision notes)

**No formal ECR/ECO required** (unless major change)

---

### Post-Design Freeze (PVT/MP)

**Process**: Formal ECR/ECO required

1. **Submit ECR**
   - Submitter fills out ECR form
   - Submitter emails to PM (CCB chair)
   - PM adds to CCB agenda

2. **CCB Meeting** (weekly or bi-weekly)
   - Review ECR (problem, solution, impact)
   - Discuss alternatives
   - Vote: Approve / Reject / Defer / Request More Info
   - If approved → PM assigns ECO number and Change Owner

3. **Implement ECO**
   - Change Owner implements per ECO plan
   - Change Owner updates status in progress log
   - Change Owner escalates blockers to PM

4. **Verify ECO**
   - QA/Test executes verification plan
   - QA/Test documents results in ECO form

5. **Close ECO** (CCB Meeting)
   - CCB reviews verification results
   - CCB approves release to production
   - PM closes ECO, updates change log

---

### Expedited Approval (Critical Changes)

**Trigger**: Critical issue blocking production or safety/compliance risk

**Process**:
1. Submitter marks ECR as "Critical"
2. PM convenes emergency CCB meeting (within 24 hours)
3. CCB evaluates and approves/rejects immediately
4. If approved → expedited implementation (parallel design + build)
5. Verification completes ASAP (may ship with open ECO if low risk)

**Condition**: Post-implementation verification mandatory (close ECO within 2 weeks)

---

## Implementation & Verification

### Implementation Best Practices

**Design Changes**:
- [ ] Update all design files (schematic, PCB, firmware, mechanical)
- [ ] Increment revision numbers (per revision control policy)
- [ ] Add revision notes (what changed, why, ECO reference)
- [ ] Archive old revision (before overwriting)

**Documentation Changes**:
- [ ] Update all affected documents (manuals, test procedures, labels)
- [ ] Mark changes (revision bars, redline, or track changes)
- [ ] Increment document revision numbers
- [ ] Archive old revisions

**BOM Changes**:
- [ ] Update BOM spreadsheet/PLM system
- [ ] Add/remove/change components as needed
- [ ] Update AVL (Approved Vendor List) if new suppliers
- [ ] Request RoHS/REACH declarations for new components

**System Updates**:
- [ ] Update ERP/PLM system (SKU, BOM, routing)
- [ ] Update inventory system (new component stocking)
- [ ] Update manufacturing work instructions
- [ ] Update test procedures

---

### Verification Best Practices

**Change-Specific Testing**:
- Test the specific change (verify issue resolved)
- Test boundary conditions (edge cases)
- Test failure modes (what happens if change fails?)

**Regression Testing**:
- Test all critical functionality (ensure no new issues)
- Test interfaces (HW-FW, HW-mechanical, product-accessory)
- Test environmental limits (temperature, humidity if affected)

**Compliance Retesting** (if applicable):
- Identify which tests are affected by change
- Consult with test lab (may not need full retest)
- Example: Resistor value change → EMC retest, but not LVD/RED

**Verification Documentation**:
- Document all test results in ECO form
- Attach evidence (test reports, photos, data logs)
- Sign off on verification completion

---

## Change Log & Tracking

### Master Change Log

**Purpose**: Single source of truth for all changes

**Format**: Spreadsheet or PLM system

| ECR/ECO # | Date | Type | Title | Rev Change | Status | Owner | Cost | Schedule Impact |
|-----------|------|------|-------|------------|--------|-------|------|-----------------|
| ECR-2026-042 | 2026-03-15 | Hardware | Replace R5 10K→4.7K | Rev B→C | Approved (ECO-2026-042) | John Doe | €5K | 2 weeks |
| ECO-2026-042 | 2026-03-20 | Hardware | Replace R5 10K→4.7K | Rev B→C | Complete | John Doe | €4.8K | 1.5 weeks |
| ECR-2026-043 | 2026-04-01 | Mechanical | Fix screw boss crack | Rev 2→3 | In Progress (ECO-2026-043) | Jane Smith | €15K | 4 weeks |
| ... | ... | ... | ... | ... | ... | ... | ... | ... |

**Fields**:
- **ECR/ECO #**: Unique identifier
- **Date**: Submission date (ECR) or approval date (ECO)
- **Type**: Hardware / Firmware / Mechanical / BOM / Documentation
- **Title**: Brief description
- **Rev Change**: Before → After revision numbers
- **Status**: Pending / Approved / In Progress / Complete / Rejected
- **Owner**: Person responsible for implementation
- **Cost**: Total cost (NRE + recurring impact)
- **Schedule Impact**: Weeks of delay (if any)

---

### Change Log by Product Revision

**Purpose**: Quick reference - what changed in each revision?

**Example**:

**Product**: SmartSense Air Quality Monitor

**Revision C** (ECO-2026-042, Released: 2026-04-10)
- **Changed**: Resistor R5 from 10kΩ to 4.7kΩ
- **Reason**: Thermal optimization (reduce component temperature by 10°C)
- **Affected Documents**: Schematic Rev C, BOM Rev C
- **Verification**: Thermal testing passed, EMC retest passed

**Revision B** (ECO-2026-038, Released: 2026-02-15)
- **Changed**: Added second source for CO2 sensor (U2)
- **Reason**: Supply chain risk mitigation (primary supplier lead time 16 weeks)
- **Affected Documents**: BOM Rev B, AVL updated
- **Verification**: Sensor accuracy testing passed (both sources within spec)

**Revision A** (Initial Release: 2026-01-10)
- Initial production release

---

### ECR/ECO Status Tracking

**Dashboard**:

| Status | Count | Notes |
|--------|-------|-------|
| **ECR Pending Review** | 5 | Awaiting CCB meeting |
| **ECR Approved (Converting to ECO)** | 2 | ECO forms being filled out |
| **ECO In Progress** | 8 | Implementation underway |
| **ECO In Verification** | 3 | Testing in progress |
| **ECO Complete (Closed)** | 47 | Successfully implemented |
| **ECR Rejected** | 12 | Not approved by CCB |

**Aging Report** (open ECOs by age):
| ECO # | Title | Owner | Days Open | Status |
|-------|-------|-------|-----------|--------|
| ECO-2026-039 | _______ | _______ | 45 days | In Progress (blocked on component delivery) |
| ECO-2026-041 | _______ | _______ | 30 days | In Verification (retest scheduled next week) |
| ... | _______ | _______ | _______ | _______ |

---

## Best Practices & Tips

### 1. Start Change Control Early

**Don't wait until production** to establish change control. Practice during DVT so the process is smooth by PVT.

---

### 2. Assess Impact Thoroughly

**Don't rush approval**. Take time to understand ripple effects. A small change (e.g., resistor value) can have big impacts (e.g., EMC retest).

---

### 3. Document Everything

**Future you will thank you**. When debugging a field failure 6 months later, you'll need to know exactly what changed and when.

---

### 4. Version Control Integration

**Tag design files** with ECO numbers in commit messages:
```
git commit -m "ECO-2026-042: Replace R5 10K with 4.7K for thermal optimization"
```

---

### 5. Consider Timing

**Batch changes** when possible. If multiple ECOs pending, implement together in one revision (reduces retest cost/time).

---

### 6. Communicate Changes

**Notify stakeholders**: Manufacturing, QA, Sales, Support, Customers (if necessary). Changes affect everyone.

---

### 7. Track Costs

**Monitor ECO costs** against budget. Excessive ECOs = poor initial design or inadequate testing.

**Typical ECO Cost Budget**: 5-10% of total development budget

---

## Conclusion

**Formal change control is essential for mature hardware development.**

**Key Takeaways**:
1. **Design freeze = formal change control** (ECR/ECO process required)
2. **Assess impact before approving** (technical, cost, schedule, compliance)
3. **Document everything** (change log, revision history, verification results)
4. **CCB approval required** (no unauthorized changes)
5. **Verify thoroughly** (test change + regression test)

**Change control protects**:
- ✅ Product quality (no undocumented changes)
- ✅ Compliance (audit trail for regulators)
- ✅ Configuration management (know what's in each build)
- ✅ Budget and schedule (no surprise costs or delays)

**This template provides**:
- ECR form (change request)
- ECO form (approved change order)
- Impact assessment framework
- Approval workflow
- Change log tracking

**Use this template to**:
- Establish formal change control process
- Track all design changes post-freeze
- Ensure changes are evaluated, approved, implemented, and verified properly

---

## Related Resources

- [Phase Gate Checklist](../templates/03-phase-gate-checklist.md) - Design freeze gate
- [Risk Register](../templates/02-risk-register.md) - Track change-related risks
- [BOM Template](../templates/07-bom-template.md) - Update BOM with changes
- [Test Plan Template](../templates/09-test-plan-template.md) - Verification testing

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit  
**Repository**: https://github.com/kathegrima/hardware-pm-starter-kit

---

*"Change is inevitable, but chaos is optional. Formal change control brings order to hardware development."*
