# Sprint Planning - Hardware Development

> **Purpose**: Plan and track hardware development sprints with long lead-time components  
> **Sprint Length**: Typically 4-8 weeks for hardware (2x software sprint length)

---

## Sprint Overview

- **Sprint Number**: `Sprint #[X]`
- **Project**: `[PROJECT_NAME]`
- **Sprint Goal**: `[One sentence sprint objective]`
- **Sprint Duration**: `[START_DATE]` to `[END_DATE]` ([X] weeks)
- **Development Phase**: `[Concept / EVT / DVT / PVT / Production]`

---

## Quick Navigation

- [Sprint Goal & Objectives](#sprint-goal--objectives)
- [Team Capacity](#team-capacity)
- [Sprint Backlog](#sprint-backlog)
- [Hardware Dependencies](#hardware-dependencies--lead-times)
- [Definition of Done](#definition-of-done)
- [Daily Standup Notes](#daily-standup-tracking)

---

## Sprint Goal & Objectives

### Primary Goal
**[Clear, concise statement of what the team aims to achieve this sprint]**

Example: *"Complete EVT prototype assembly and validate core motor control functionality"*

### Success Criteria
- [ ] [Measurable outcome 1 - e.g., "5 EVT units assembled and powered on"]
- [ ] [Measurable outcome 2 - e.g., "Motor control loop achieves ±2mm accuracy"]
- [ ] [Measurable outcome 3 - e.g., "Thermal testing shows temps <85°C at 40°C ambient"]

### Sprint Risks & Mitigation
| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| PCB delivery delayed 1 week | High | Medium | • Daily supplier check-ins<br>• Backup supplier on standby |
| Battery cells arrive out-of-spec | Medium | Low | • Incoming inspection protocol<br>• Alternative cell qualified |

---

## Team Capacity

### Team Members

| Name | Role | Availability | Capacity (hrs) | Planned (hrs) | Remaining (hrs) |
|------|------|--------------|----------------|---------------|-----------------|
| [Name] | Hardware Engineer | 100% | 80 | 0 | 80 |
| [Name] | Firmware Engineer | 80% (training) | 64 | 0 | 64 |
| [Name] | Mechanical Engineer | 100% | 80 | 0 | 80 |
| [Name] | Test Engineer | 100% | 80 | 0 | 80 |
| **TOTAL** | | | **304** | **0** | **304** |

### Notes
- [Name] out Fri for personal day
- [Name] supporting production issue Mon-Tue (16hrs)
- Holiday: [DATE] - team unavailable

---

## Sprint Backlog

### Priority Legend
- 🔴 **P0**: Blocker - must complete this sprint
- 🟠 **P1**: Critical - should complete this sprint
- 🟡 **P2**: Important - complete if capacity allows
- 🟢 **P3**: Nice-to-have - defer if needed

---

### Hardware Design Tasks

| ID | User Story / Task | Priority | Story Points | Assignee | Status | Dependencies | Notes |
|----|-------------------|----------|--------------|----------|--------|--------------|-------|
| HW-101 | As a user, I need the device to operate for 8hrs on battery | 🔴 P0 | 8 | [Name] | In Progress | Battery cells delivered | Power profiling in progress |
| HW-102 | Design motor driver PCB rev B with thermal improvements | 🔴 P0 | 13 | [Name] | To Do | EVT testing complete | Need 2 week PCB fab time |
| HW-103 | Select and qualify backup battery supplier | 🟠 P1 | 5 | [Name] | To Do | None | Risk mitigation |
| HW-104 | Update BOM with production-intent components | 🟡 P2 | 3 | [Name] | To Do | Design finalized | DVT requirement |

---

### Firmware Tasks

| ID | User Story / Task | Priority | Story Points | Assignee | Status | Dependencies | Notes |
|----|-------------------|----------|--------------|----------|--------|--------------|-------|
| FW-201 | Implement motor control PID loop with ±2mm accuracy | 🔴 P0 | 13 | [Name] | In Progress | Motors installed | Tuning on EVT hardware |
| FW-202 | Add battery fuel gauge monitoring and low-power mode | 🟠 P1 | 8 | [Name] | To Do | HW-101 complete | Needed for 8hr runtime |
| FW-203 | Implement OTA update bootloader | 🟡 P2 | 8 | [Name] | To Do | None | DVT requirement |

---

### Mechanical Tasks

| ID | User Story / Task | Priority | Story Points | Assignee | Status | Dependencies | Notes |
|----|-------------------|----------|--------------|----------|--------|--------------|-------|
| ME-301 | Design enclosure with ventilation for thermal management | 🔴 P0 | 13 | [Name] | In Progress | Thermal sim complete | Iteration 3 in progress |
| ME-302 | Create assembly jigs for motor mounting | 🟠 P1 | 5 | [Name] | To Do | Design freeze | Needed for DVT build |

---

### Testing & Validation Tasks

| ID | User Story / Task | Priority | Story Points | Assignee | Status | Dependencies | Notes |
|----|-------------------|----------|--------------|----------|--------|--------------|-------|
| QA-401 | Execute thermal chamber testing (-10°C to +50°C) | 🔴 P0 | 8 | [Name] | Blocked | EVT units ready | Chamber booked Thurs |
| QA-402 | Develop automated functional test script | 🟠 P1 | 8 | [Name] | To Do | Test points defined | DVT requirement |
| QA-403 | Drop testing (1.2m onto concrete, 6 orientations) | 🟡 P2 | 5 | [Name] | To Do | Enclosure final | DVT requirement |

---

### Integration Tasks

| ID | User Story / Task | Priority | Story Points | Assignee | Status | Dependencies | Notes |
|----|-------------------|----------|--------------|----------|--------|--------------|-------|
| INT-501 | Integrate motor driver HW with control FW | 🔴 P0 | 8 | HW+FW team | In Progress | HW-102, FW-201 | Daily pair sessions |
| INT-502 | System-level power budget validation | 🟠 P1 | 5 | HW+FW team | To Do | HW-101, FW-202 | Test with actual loads |

---

## Hardware Dependencies & Lead Times

> [!WARNING]
> Track long-lead components to prevent sprint delays

### Components Arriving This Sprint

| Component | Supplier | Quantity | Order Date | Expected Arrival | Status | Risk |
|-----------|----------|----------|------------|------------------|--------|------|
| DC Motors (Model X) | Vendor A | 50 pcs | Jan 15 | **Feb 12** | 🟢 On Track | Low - confirmed |
| Battery Cells (18650) | Vendor B | 200 pcs | Jan 20 | **Feb 10** | 🟢 Delivered | None |
| Custom Connector | Vendor C | 100 pcs | Jan 10 | **Feb 8** | 🟡 Delayed 2 days | Medium - late shipment |

### Components Ordered for Future Sprints

| Component | Supplier | Quantity | Order Date | Expected Arrival | For Sprint | Notes |
|-----------|----------|----------|------------|------------------|------------|-------|
| PCB rev B | Fab House D | 25 pcs | Feb 5 | **Feb 19** | Sprint #[X+1] | 2 week turnaround |
| Injection molded case | CM E | 500 pcs | Jan 25 | **Mar 10** | Sprint #[X+2] | Tooling complete, production run |

### Components Needing Orders

> [!NOTE]
> Order ASAP to avoid delays in upcoming sprints

- [ ] **Pressure sensors** - 12 week lead time → Order by [DATE] for Sprint #[X+3]
- [ ] **Display modules** - 8 week lead time → Order by [DATE] for Sprint #[X+2]

---

## Sprint Ceremonies

### Sprint Planning Meeting
- **Date**: `[DATE]`
- **Duration**: 2-4 hours (hardware sprints need longer planning)
- **Attendees**: Full team + Product Owner + Scrum Master
- **Agenda**:
  1. Review sprint goal (15 min)
  2. Review hardware dependencies and lead times (15 min)
  3. Team capacity planning (15 min)
  4. Backlog refinement and task breakdown (90 min)
  5. Commitment and final capacity check (15 min)

### Daily Standup
- **Time**: `[TIME]` daily
- **Duration**: 15 minutes (max)
- **Format**: 
  - What did I complete yesterday?
  - What will I work on today?
  - What blockers do I have? (especially component delays)

### Sprint Review / Demo
- **Date**: `[END_DATE]`
- **Duration**: 1-2 hours
- **Attendees**: Team + Stakeholders + Product Owner
- **Demo Requirements**: 
  - Working hardware prototype (not slides!)
  - Demonstrate sprint goal achievement
  - Show test results and metrics

### Sprint Retrospective
- **Date**: `[END_DATE + 1 day]`
- **Duration**: 1.5 hours
- **Format**: What went well / What didn't / Action items

---

## Definition of Done

> [!NOTE]
> A user story is DONE when all criteria are met

### For Hardware Tasks
- [ ] Design files checked into version control (Git, SVN, etc.)
- [ ] Peer review completed with sign-off
- [ ] BOM updated with part numbers and costs
- [ ] Prototype built and basic functionality verified
- [ ] Design documentation updated (README, datasheets linked)
- [ ] Known issues documented in issue tracker

### For Firmware Tasks
- [ ] Code checked into version control with meaningful commit message
- [ ] Unit tests written and passing (where applicable)
- [ ] Code review completed with approval
- [ ] Tested on actual hardware (not just simulator)
- [ ] Performance metrics documented (CPU usage, memory, power)
- [ ] User-facing documentation updated

### For Integration Tasks
- [ ] Hardware and firmware working together as expected
- [ ] System-level test executed and results documented
- [ ] No critical bugs blocking next sprint
- [ ] Demo-ready for sprint review

### For Test Tasks
- [ ] Test plan documented and reviewed
- [ ] Test executed with pass/fail results logged
- [ ] Test data saved and backed up
- [ ] Issues filed for any failures found
- [ ] Test report created (summary, photos, data plots)

---

## Daily Standup Tracking

> [!TIP]
> Update daily to track progress and identify blockers early

### Week 1

#### Monday [DATE]
| Team Member | Yesterday | Today | Blockers |
|-------------|-----------|-------|----------|
| [Name] | - | Started HW-101 power profiling | Need multimeter from lab |
| [Name] | - | Reviewing FW-201 PID algorithm | None |

#### Tuesday [DATE]
| Team Member | Yesterday | Today | Blockers |
|-------------|-----------|-------|----------|
| [Name] | Power profiling setup | Completed subsystem measurements | None |
| [Name] | FW-201 review | Started PID implementation | Waiting for motors to arrive |

#### Wednesday [DATE]
| Team Member | Yesterday | Today | Blockers |
|-------------|-----------|-------|----------|
| [Name] | Subsystem power measured | Full system power test | None |
| [Name] | PID implementation | Continue PID tuning | 🚨 Motors still not delivered! |

---

### Week 2

*[Continue pattern for remaining weeks]*

---

## Sprint Burndown

### Story Points Tracking

| Day | Planned Remaining | Actual Remaining | Notes |
|-----|-------------------|------------------|-------|
| Day 0 (Sprint Start) | 80 | 80 | Sprint kickoff |
| Day 1 | 77 | 80 | Planning buffer |
| Day 2 | 74 | 76 | HW-101 progressing |
| Day 3 | 71 | 76 | FW-201 blocked (motors) |
| Day 4 | 68 | 72 | Motors arrived! |
| Day 5 | 65 | 68 | Back on track |
| ... | ... | ... | ... |
| Day [X] (Sprint End) | 0 | [Actual] | Sprint review |

### Velocity Calculation
- **Committed Story Points**: 80
- **Completed Story Points**: [TBD]
- **Sprint Velocity**: [Completed / Committed] = [TBD]%

---

## Best Practices for Hardware Sprints

### 1. Longer Sprint Length
- Hardware sprints typically **4-8 weeks** vs 2-4 weeks for software
- Longer sprints accommodate component lead times and physical testing
- Consider **2:1 ratio** - hardware sprint = 2x software sprint length

### 2. Component Lead Time Management
- **Track lead times** in sprint backlog (separate column)
- **Order components early** - don't wait for sprint to start
- **Maintain buffer inventory** for critical long-lead items
- **Dual-source** components with >8 week lead times

### 3. Hardware-Specific Story Points
Use reference stories calibrated to hardware work:
- **1 point**: Update schematic symbol, review supplier quote
- **3 points**: Design simple circuit block, write test procedure
- **5 points**: PCB layout for one board, mechanical part design
- **8 points**: Complex circuit design, firmware module implementation
- **13 points**: Full subsystem design, multi-week integration task

### 4. Demo Requirements
- **Working prototypes required** - no slideware!
- Acceptable demo formats:
  - Video of hardware operating (if can't transport)
  - Live demo with actual hardware
  - Test data plots showing performance
- Not acceptable:
  - CAD renders without physical build
  - Simulations without hardware validation

### 5. HW/SW Team Synchronization
- **Shared interface definitions** documented and version-controlled
- **Hardware emulators** for firmware development before HW ready
- **Integration sprints** - dedicate sprints to HW+FW integration
- **Daily standups together** to catch dependency issues early

### 6. Handling Blocked Work
When hardware components are delayed:
- Move to **"Blocked" column** immediately (don't let it sit "In Progress")
- **Escalate** lead time delays to supplier daily
- **Pivot** to alternative work (documentation, test planning, future sprint prep)
- **Maintain separate backlog** for "Dependency Unresolved" work

### 7. Sprint Retrospective for Hardware
Hardware-specific retrospective questions:
- Did we accurately estimate component lead times?
- Did we order parts early enough?
- What physical testing took longer than expected?
- What tools or equipment did we lack?
- What supplier issues arose and how do we prevent them?

---

## Sprint Review Template

### Sprint #[X] Review - [PROJECT_NAME]

**Date**: [DATE]  
**Attendees**: [List]

### Sprint Goal Achievement
- **Goal**: [Restate sprint goal]
- **Achieved**: ✅ Yes / ⚠️ Partially / ❌ No
- **Evidence**: [Brief description of demo/results]

### Completed Stories

| ID | Story | Status | Notes |
|----|-------|--------|-------|
| HW-101 | Battery runtime 8hrs | ✅ Done | Actual: 8.2hrs @ typical load |
| FW-201 | Motor control accuracy | ✅ Done | Achieved ±1.5mm (better than ±2mm target) |
| QA-401 | Thermal testing | ⚠️ Partial | Passed -10°C to +40°C, failed at +50°C |

### Incomplete Stories / Carried Over

| ID | Story | Reason Not Complete | Action for Next Sprint |
|----|-------|---------------------|------------------------|
| HW-102 | PCB rev B design | Thermal issue found in QA-401 | Redesign with better cooling, carry to Sprint #[X+1] |

### Metrics
- **Planned Story Points**: 80
- **Completed Story Points**: 65
- **Sprint Velocity**: 81%
- **Burndown**: On track until Day 15, then thermal issue discovered

### Demos
- [Link to video / photos of working prototype]
- [Test data plots attached]

### Stakeholder Feedback
- [Notes from stakeholder reactions and requests]

---

## Sprint Retrospective Template

### Sprint #[X] Retrospective - [PROJECT_NAME]

**Date**: [DATE]  
**Attendees**: [Team only - no stakeholders]

### What Went Well 🎉
- Motors arrived on time and worked first try
- HW/FW integration went smoothly with daily pair sessions
- Team communication improved with standup discipline

### What Didn't Go Well 😞
- Thermal issue discovered late (Day 15 of 20)
- PCB vendor changed lead time mid-sprint without notifying us
- Test chamber was double-booked, lost 2 days

### Action Items for Next Sprint

| Action | Owner | Due Date | Priority |
|--------|-------|----------|----------|
| Schedule thermal simulation before PCB order | [Name] | Before Sprint #[X+1] planning | 🔴 P0 |
| Set up daily email alerts from PCB vendor | [Name] | This week | 🟠 P1 |
| Book test chamber 2 weeks in advance | [Name] | Sprint #[X+1] Day 1 | 🟡 P2 |

### Team Velocity Trend
- Sprint #[X-2]: 70%
- Sprint #[X-1]: 75%
- Sprint #[X]: 81%
- **Trend**: ⬆️ Improving! (Target: 85-95%)

---

## Tools & Templates

### Recommended Tools
- **Jira / Azure DevOps**: Sprint backlog and burndown tracking
- **Confluence / Notion**: Documentation and retrospective notes
- **Miro / Mural**: Virtual whiteboard for sprint planning
- **Google Sheets**: Component lead time tracker (if not in Jira)
- **Slack / Teams**: Daily standup async updates

### Story Template

```markdown
### [ID] - [User Story Title]

**As a** [user/role]  
**I need** [capability]  
**So that** [benefit/value]

**Acceptance Criteria:**
- [ ] [Specific, testable criterion 1]
- [ ] [Specific, testable criterion 2]
- [ ] [Specific, testable criterion 3]

**Hardware Dependencies:**
- [Component X] - Lead time: [Y] weeks - Order by: [DATE]

**Definition of Done:**
- [ ] [Hardware-specific DoD items]
- [ ] [Testing requirements]
- [ ] [Documentation updated]

**Story Points**: [X]  
**Priority**: [P0/P1/P2/P3]  
**Assignee**: [Name]
```

---

**Document Version**: 1.0  
**Template**: hardware-pm-starter-kit v1.0  
**Last Updated**: `11/02/2026`

---

## Related Templates

- [Project Charter](./project-charter-hardware.md) - Define project scope and objectives
- [Risk Register](./risk-register-hardware.md) - Track sprint-level risks
- [Phase Gate Checklist](./phase-gate-checklist.md) - Align sprints to phase gates
- [Lessons Learned](./lessons-learned-template.md) - Capture sprint insights
