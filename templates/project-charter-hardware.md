# Hardware Project Charter Template

> **Purpose**: Formally authorize a hardware project and empower the project manager to allocate resources  
> **When to Use**: Project initiation phase, before detailed planning begins

---

## Document Information

- **Project Name**: `[PROJECT_NAME]`
- **Project Code**: `[PROJECT_CODE]`
- **Charter Version**: `[VERSION]`
- **Date Created**: `[DATE]`
- **Last Updated**: `[DATE]`
- **Document Owner**: `[PM_NAME]`
- **Status**: `[Draft / Under Review / Approved]`

---

## Quick Navigation

- [Executive Summary](#executive-summary)
- [Project Purpose & Justification](#project-purpose--justification)
- [Project Objectives & Success Criteria](#project-objectives--success-criteria)
- [Project Scope](#project-scope)
- [Hardware Development Phases](#hardware-development-phases)
- [Timeline & Milestones](#timeline--milestones)
- [Budget & Resources](#budget--resources)
- [Project Organization](#project-organization)
- [Risks & Assumptions](#risks--assumptions)
- [Approval & Sign-off](#approval--sign-off)

---

## Executive Summary

> [!NOTE]
> 3-5 sentence high-level overview for executives and sponsors

**Project Overview**:  
[Brief description of what hardware product is being developed and why]

**Business Need**:  
[What problem does this solve? What market opportunity are we addressing?]

**Expected Outcome**:  
[What will be delivered at project completion?]

**Strategic Alignment**:  
[How does this project support company strategy and goals?]

**Investment Required**:  
- Total Budget: `$[X]M` / `€[X]M`
- Timeline: `[X]` months
- Team Size: `[X]` FTE

---

## Project Purpose & Justification

### Business Case

**Problem Statement**:  
[What specific problem are we solving? Include data/evidence]

**Market Opportunity**:  
[Market size, growth rate, competitive landscape]

**Strategic Rationale**:  
- [ ] Supports company strategy: `[Strategy name]`
- [ ] Addresses customer pain point: `[Pain point]`
- [ ] Competitive differentiation: `[How we differentiate]`
- [ ] Revenue opportunity: `$[X]` projected
- [ ] Cost reduction: `$[X]` savings expected

**Why Now?**:  
[Why is this the right time? Market timing, technology readiness, competitive pressure]

### Alignment with Organizational Goals

**Company Goals Supported**:
1. `[Company Goal 1]` - How this project contributes
2. `[Company Goal 2]` - How this project contributes
3. `[Company Goal 3]` - How this project contributes

**Success Metrics Alignment**:
- Company OKR: `[OKR]` → Project KPI: `[KPI]`
- Company OKR: `[OKR]` → Project KPI: `[KPI]`

---

## Project Objectives & Success Criteria

### Primary Objectives

**Technical Objectives**:
1. **`[Objective 1]`** - `[Measurable target]`
2. **`[Objective 2]`** - `[Measurable target]`
3. **`[Objective 3]`** - `[Measurable target]`

**Business Objectives**:
1. **`[Objective 1]`** - `[Measurable target]`
2. **`[Objective 2]`** - `[Measurable target]`
3. **`[Objective 3]`** - `[Measurable target]`

### Success Criteria

**Quantitative Criteria**:
- [ ] Product cost < `$[X]` BOM at `[Volume]` units
- [ ] Time to market: Launch by `[DATE]`
- [ ] Performance: `[Metric]` meets or exceeds `[Target]`
- [ ] Quality: Manufacturing yield > `[X]%`
- [ ] Reliability: MTBF > `[X]` hours

**Qualitative Criteria**:
- [ ] Customer satisfaction score > `[X]`/10
- [ ] Design meets brand guidelines
- [ ] Compliance: CE, FCC, RoHS, `[Other]` certified
- [ ] Manufacturing readiness: Supplier qualified, process validated

### Key Performance Indicators (KPIs)

| KPI | Target | Measurement Method | Frequency |
|-----|--------|-------------------|-----------|
| BOM Cost | `$[X]` | Cost rollup | Monthly |
| Schedule Adherence | 0% slip | Timeline vs actual | Weekly |
| Prototype Iterations | < `[X]` | Build count | Per phase |
| Defect Rate | < `[X]%` | Testing results | Per build |
| Budget Variance | ± `[X]%` | Actual vs planned | Monthly |

---

## Project Scope

### In Scope

**Hardware Development**:
- [ ] Electrical design: `[Brief description]`
- [ ] Mechanical design: `[Brief description]`
- [ ] Firmware development: `[Brief description]`
- [ ] PCB design and layout: `[Number]` boards
- [ ] Enclosure/housing design
- [ ] Prototype builds: EVT, DVT, PVT

**Testing & Validation**:
- [ ] Functional testing
- [ ] Environmental testing (temp, humidity, vibration, drop)
- [ ] EMC/EMI compliance testing
- [ ] Safety certification: `[List certifications]`
- [ ] Reliability testing: MTBF validation

**Manufacturing Preparation**:
- [ ] DFM (Design for Manufacturing) review
- [ ] Supplier selection and qualification
- [ ] Manufacturing process development
- [ ] Test fixture design
- [ ] Pilot production run: `[X]` units

**Documentation**:
- [ ] Technical specifications
- [ ] User manuals
- [ ] Manufacturing work instructions
- [ ] Test procedures
- [ ] Compliance documentation

### Out of Scope

**Explicitly NOT included in this project**:
- [ ] `[Item 1 - e.g., "Software mobile app development"]`
- [ ] `[Item 2 - e.g., "Marketing materials creation"]`
- [ ] `[Item 3 - e.g., "Full-scale production launch"]`
- [ ] `[Item 4 - e.g., "International certifications beyond CE/FCC"]`
- [ ] `[Item 5 - e.g., "Field service organization setup"]`

**Future Phase Considerations**:
- `[Feature/work item]` - Planned for Phase 2
- `[Feature/work item]` - Planned for Phase 3

### Deliverables

**Phase-Based Deliverables**:

| Phase | Key Deliverables | Quantity | Acceptance Criteria |
|-------|-----------------|----------|---------------------|
| **Concept** | PRD, feasibility study, architecture | Documentation | Approved by stakeholders |
| **EVT** | Functional prototypes | `[X]` units | Core features working |
| **DVT** | Production-intent prototypes | `[X]` units | All requirements met, DFM approved |
| **PVT** | Pilot production units | `[X]` units | Yield > `[X]%`, all tests passed |
| **MP Readiness** | Manufacturing package, qualified suppliers | Complete docs | Ready for volume production |

**Documentation Deliverables**:
- [ ] Product Requirements Document (PRD)
- [ ] Design specifications (electrical, mechanical, firmware)
- [ ] Test plans and reports
- [ ] Manufacturing work instructions
- [ ] User documentation
- [ ] Compliance certificates

---

## Hardware Development Phases

### Phase Gate Overview

```
Concept → EVT → DVT → PVT → MP Readiness → Volume Production
  |        |      |      |         |              |
Feasibility Proto Valid  Pilot   Qualified    Scale
           Design  Mfg             Production
```

### Phase Details

**Phase 1: Concept** (`[Start]` - `[End]`, `[X]` weeks)
- **Goal**: Validate feasibility and define requirements
- **Key Activities**: Market research, PRD creation, architecture design, cost analysis
- **Gate Criteria**: PRD approved, technology feasibility proven, business case validated
- **Deliverables**: PRD, architecture document, feasibility report, budget estimate

**Phase 2: EVT - Engineering Validation Test** (`[Start]` - `[End]`, `[X]` weeks)
- **Goal**: Prove core technology and functionality
- **Key Activities**: First prototypes (`[X]` units), functional testing, architecture validation
- **Gate Criteria**: Core features working, major technical risks retired
- **Deliverables**: Working prototypes, test results, risk assessment update

**Phase 3: DVT - Design Validation Test** (`[Start]` - `[End]`, `[X]` weeks)
- **Goal**: Production-intent design validation
- **Key Activities**: Full feature prototypes (`[X]` units), compliance testing, DFM review
- **Gate Criteria**: All requirements met, design frozen, DFM approved, compliance path clear
- **Deliverables**: Production-intent prototypes, test reports, DFM report, BOM finalized

**Phase 4: PVT - Production Validation Test** (`[Start]` - `[End]`, `[X]` weeks)
- **Goal**: Validate manufacturing process
- **Key Activities**: Pilot builds (`[X]` units), yield optimization, supplier qualification
- **Gate Criteria**: Yield > `[X]%`, quality metrics met, suppliers qualified
- **Deliverables**: Pilot units, manufacturing work instructions, qualified supplier list

**Phase 5: MP Readiness** (`[Start]` - `[End]`, `[X]` weeks)
- **Goal**: Final readiness for volume production
- **Key Activities**: Final validations, process optimization, ramp planning
- **Gate Criteria**: All certifications complete, production process stable, GO decision
- **Deliverables**: Manufacturing package, certifications, production ramp plan

---

## Timeline & Milestones

### Project Schedule

**Project Start Date**: `[DATE]`  
**Project End Date**: `[DATE]`  
**Total Duration**: `[X]` months

### Major Milestones

| Milestone | Target Date | Status | Owner |
|-----------|-------------|--------|-------|
| Project Kickoff | `[DATE]` | `[Status]` | `[Owner]` |
| Concept Phase Complete | `[DATE]` | `[Status]` | `[Owner]` |
| EVT Build Complete | `[DATE]` | `[Status]` | `[Owner]` |
| EVT Testing Complete | `[DATE]` | `[Status]` | `[Owner]` |
| DVT Build Complete | `[DATE]` | `[Status]` | `[Owner]` |
| DFM Review Complete | `[DATE]` | `[Status]` | `[Owner]` |
| Compliance Testing Started | `[DATE]` | `[Status]` | `[Owner]` |
| PVT Build Complete | `[DATE]` | `[Status]` | `[Owner]` |
| Manufacturing Qualification | `[DATE]` | `[Status]` | `[Owner]` |
| Certifications Complete | `[DATE]` | `[Status]` | `[Owner]` |
| MP Readiness Review | `[DATE]` | `[Status]` | `[Owner]` |
| Volume Production Start | `[DATE]` | `[Status]` | `[Owner]` |

### Critical Path Activities

**Top 3 Critical Path Items**:
1. `[Activity]` - Longest lead time: `[X]` weeks
2. `[Activity]` - Dependency: `[Dependency]`
3. `[Activity]` - External dependency: `[Details]`

### Dependencies

**External Dependencies**:
- `[Dependency 1]` - Impact: `[Impact]` - Mitigation: `[Strategy]`
- `[Dependency 2]` - Impact: `[Impact]` - Mitigation: `[Strategy]`

**Internal Dependencies**:
- `[Dependency 1]` - Team/project: `[Name]`
- `[Dependency 2]` - Team/project: `[Name]`

---

## Budget & Resources

### Budget Summary

**Total Project Budget**: `$[X]M` / `€[X]M`

| Category | Budget | % of Total | Notes |
|----------|--------|-----------|-------|
| **Engineering Labor** | `$[X]` | `[X]%` | Hardware, firmware, mechanical |
| **Prototype Builds** | `$[X]` | `[X]%` | EVT + DVT + PVT materials |
| **Testing & Certification** | `$[X]` | `[X]%` | Compliance, environmental, reliability |
| **Tooling & Equipment** | `$[X]` | `[X]%` | Test fixtures, production tooling |
| **Manufacturing NRE** | `$[X]` | `[X]%` | Setup costs, process development |
| **Materials & Components** | `$[X]` | `[X]%` | Components for prototypes |
| **Travel & Misc** | `$[X]` | `[X]%` | Supplier visits, conferences |
| **Contingency** | `$[X]` | `[X]%` | Risk buffer (10-20% typical) |

### Resource Requirements

**Human Resources**:

| Role | Allocation | Duration | Cost |
|------|------------|----------|------|
| Project Manager | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |
| Hardware Engineer | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |
| Firmware Engineer | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |
| Mechanical Engineer | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |
| Test Engineer | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |
| Supply Chain Manager | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |
| Manufacturing Engineer | `[X]%` / `[X]` FTE | `[X]` months | `$[X]` |

**Equipment & Tools**:
- `[Equipment 1]` - Cost: `$[X]` - Purpose: `[Purpose]`
- `[Equipment 2]` - Cost: `$[X]` - Purpose: `[Purpose]`
- CAD software licenses: `$[X]`
- Testing equipment: `$[X]`

**Facilities**:
- Lab space: `[X]` sq ft
- Manufacturing space (pilot): `[X]` sq ft
- Storage for prototypes and inventory

---

## Project Organization

### Governance Structure

**Project Sponsor**: `[NAME]` - `[TITLE]`  
**Project Manager**: `[NAME]` - `[TITLE]`  
**Steering Committee**: `[NAMES]`

**Decision Authority**:
- Budget changes > `[X]%`: Sponsor approval required
- Scope changes: Steering Committee approval
- Schedule changes > `[X]` weeks: Sponsor approval
- Design decisions: Technical Lead with PM consultation

### Core Team

| Name | Role | Responsibility | Allocation |
|------|------|---------------|------------|
| `[NAME]` | Project Manager | Overall project coordination, timeline, budget | `[X]%` |
| `[NAME]` | Hardware Lead | Electrical design, PCB layout, component selection | `[X]%` |
| `[NAME]` | Firmware Lead | Embedded software, device drivers, testing | `[X]%` |
| `[NAME]` | Mechanical Lead | Enclosure design, thermal management, DFM | `[X]%` |
| `[NAME]` | Test Lead | Test planning, execution, validation | `[X]%` |
| `[NAME]` | Supply Chain Lead | Sourcing, supplier management, BOM cost | `[X]%` |
| `[NAME]` | Manufacturing Lead | Process development, yield optimization, pilot | `[X]%` |

### Extended Team / Subject Matter Experts

| Name | Role | Contribution | Involvement |
|------|------|-------------|-------------|
| `[NAME]` | Industrial Designer | Product aesthetics, user experience | Phase 1-2 |
| `[NAME]` | Compliance Engineer | Regulatory strategy, certification | Phase 2-4 |
| `[NAME]` | Quality Engineer | Quality planning, FMEA, reliability | Phase 2-5 |
| `[NAME]` | Product Manager | Requirements, customer feedback | All phases |

### Key Stakeholders

| Stakeholder | Interest | Influence | Communication Frequency |
|-------------|----------|-----------|-------------------------|
| `[NAME]` - Executive Sponsor | Strategic alignment, ROI | High | Monthly |
| `[NAME]` - Engineering VP | Technical excellence, resources | High | Bi-weekly |
| `[NAME]` - Sales/Marketing VP | Market fit, launch timing | Medium | Monthly |
| `[NAME]` - Operations VP | Manufacturing readiness | High | Bi-weekly in Phase 3-5 |
| `[NAME]` - Finance | Budget, cost targets | Medium | Monthly |

### Communication Plan

**Status Reporting**:
- **Weekly**: Team standup (30 min) - Progress, blockers, risks
- **Bi-weekly**: Steering Committee update (email/dashboard)
- **Monthly**: Executive summary to sponsor
- **Phase Gates**: Formal review meeting with all stakeholders

**Escalation Path**:
1. Issue identified → PM informed (immediate)
2. PM cannot resolve → Escalate to Sponsor (within 24 hours)
3. Sponsor decision needed → Steering Committee (within 48 hours)

---

## Risks & Assumptions

### Top Risks

| Risk | Probability | Impact | Mitigation Strategy | Owner |
|------|------------|--------|---------------------|-------|
| Component shortage/EOL | `[H/M/L]` | `[H/M/L]` | Dual-source critical parts, early procurement | `[Owner]` |
| Certification delays | `[H/M/L]` | `[H/M/L]` | Pre-compliance testing at EVT, experienced lab | `[Owner]` |
| Manufacturing yield issues | `[H/M/L]` | `[H/M/L]` | DFM review at DVT, pilot builds at PVT | `[Owner]` |
| Thermal/EMI failures | `[H/M/L]` | `[H/M/L]` | Simulation at Concept, testing at EVT | `[Owner]` |
| Supplier capacity constraints | `[H/M/L]` | `[H/M/L]` | Early supplier engagement, backup suppliers | `[Owner]` |

**Risk Assessment**: Overall project risk level: `[Low / Medium / High]`

### Assumptions

**Technical Assumptions**:
- [ ] Technology `[X]` is mature and proven at this scale
- [ ] Components with `[X]` week lead times will be available
- [ ] Team has expertise in `[Technology/domain]`
- [ ] Existing test equipment is sufficient for validation

**Business Assumptions**:
- [ ] Market demand forecast of `[X]` units/year is accurate
- [ ] Pricing at `$[X]` achieves target margin
- [ ] Competitive landscape remains stable
- [ ] Customer requirements will not change significantly

**External Assumptions**:
- [ ] Regulatory requirements (CE, FCC, RoHS) won't change
- [ ] Supplier relationships and pricing remain stable
- [ ] Currency exchange rates remain within `[X]%` range
- [ ] No major supply chain disruptions (geopolitical, pandemic, etc.)

### Constraints

**Technical Constraints**:
- BOM cost must be < `$[X]` at `[Volume]` units
- Product dimensions: Max `[X]` × `[Y]` × `[Z]` mm
- Power consumption: < `[X]` watts
- Operating temperature: `[X]°C` to `[Y]°C`

**Schedule Constraints**:
- Must launch by `[DATE]` for `[Reason - e.g., trade show, seasonal demand]`
- Prototype builds require `[X]` weeks lead time
- Certification process takes `[X]` months minimum

**Resource Constraints**:
- Budget cap: `$[X]M`
- Team size limited to `[X]` FTE
- Lab access limited to `[Hours/days]`

**Regulatory Constraints**:
- Must comply with: CE, FCC, RoHS, REACH, `[Other]`
- Safety standards: `[IEC 62368, UL 60950, etc.]`
- Environmental: IP rating `[X]`, operating altitude, humidity

---

## Approval & Sign-off

### Approval Criteria

This project charter is approved when:
- [ ] All sections are complete and reviewed
- [ ] Budget allocation confirmed by Finance
- [ ] Resource allocation confirmed by Engineering/Operations
- [ ] All key stakeholders have reviewed and provided feedback
- [ ] Project Sponsor has formally approved

### Sign-off

**I approve this project charter and authorize the project manager to proceed with project planning and execution.**

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Project Sponsor** | `[NAME]` | ________________ | `[DATE]` |
| **Project Manager** | `[NAME]` | ________________ | `[DATE]` |
| **Engineering VP** | `[NAME]` | ________________ | `[DATE]` |
| **Operations VP** | `[NAME]` | ________________ | `[DATE]` |
| **Finance** | `[NAME]` | ________________ | `[DATE]` |

---

## Document Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | `[DATE]` | `[NAME]` | Initial draft |
| 0.2 | `[DATE]` | `[NAME]` | Incorporated stakeholder feedback |
| 1.0 | `[DATE]` | `[NAME]` | Approved version |

---

## References

- [Product Requirements Document (PRD)](link-to-prd)
- [Business Case](link-to-business-case)
- [Feasibility Study](link-to-feasibility)
- [Risk Register](link-to-risk-register)
- [Phase Gate Checklist](link-to-phase-gate)

---

**Notes**:
- This charter is a living document and may be updated as the project progresses
- Major changes to scope, budget, or timeline require formal change control
- All changes must be approved by the Project Sponsor
- Refer to the [Phase Gate Checklist](../templates/phase-gate-checklist.md) for detailed gate review criteria
- Use the [Risk Register](../templates/risk-register-hardware.md) to track and manage project risks

---

*"A project charter is the project's birth certificate - it gives the project life and the PM authority."*
