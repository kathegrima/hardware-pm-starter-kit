# Phase Gate Checklist - Hardware Development 

> **Purpose**: Define clear exit criteria for each hardware development phase  
> **Usage**: Review and sign-off at each gate before advancing to next phase

---

**Navigation**: [🏠 Home](../) | [📋 All Templates](../templates/) | [📚 All Guides](../guides/)

---

## Quick Navigation

- [Concept Review](#concept-review) - Initial feasibility and requirements
- [EVT Gate](#evt-gate-engineering-validation-test) - First functional prototypes
- [DVT Gate](#dvt-gate-design-validation-test) - Production-intent design validation
- [PVT Gate](#pvt-gate-production-validation-test) - Manufacturing process validation
- [Production Launch](#production-launch-gate) - Mass production readiness

---

## Project Info

- **Project**: `[PROJECT_NAME]`
- **Current Phase**: `[PHASE]`
- **PM**: `[PM_NAME]`
- **Next Gate Review**: `[DATE]`

---

## Phase Gate Overview

```
Concept → EVT → DVT → PVT → Production Launch
   ↓       ↓      ↓      ↓          ↓
  Gate0   Gate1  Gate2  Gate3    Gate4
```

|| Phase | Purpose | Typical Quantities | Key Focus |
|-------|---------|-------------------|--------------|
| **Concept** | Validate feasibility | Proof-of-concept | Requirements, risks, business case |
| **EVT** | Prove design works | 10-50 units | Functionality, performance, first integration |
| **DVT** | Lock design | 50-200 units | Reliability, compliance, manufacturability |
| **PVT** | Validate production | 200-1,000 units | Yield, quality, production speed |
| **Production** | Mass manufacturing | Volume shipments | Scale, cost, continuous improvement |

---

## Concept Review

> [!NOTE]
> Gate 0 - Decision point to commit engineering resources to detailed design

### Business & Market

- [ ] **Market need validated** with customer interviews or market research
- [ ] **Target market size** estimated with addressable revenue potential
- [ ] **Competitive landscape** analyzed (direct and indirect competitors)
- [ ] **Value proposition** clearly defined (why customers will buy)
- [ ] **Business case** approved with ROI projections and payback period

### Technical Feasibility

- [ ] **Key technical risks** identified and mitigation strategies defined
- [ ] **Critical technologies** proven feasible (proof-of-concept demonstrations)
- [ ] **Architecture concept** defined (system-level block diagram)
- [ ] **Preliminary specifications** documented (performance targets, constraints)
- [ ] **Technology readiness** assessed (TRL level for critical subsystems)

### Requirements & Scope

- [ ] **Product requirements document (PRD)** created and approved
- [ ] **Use cases** defined with user stories
- [ ] **Performance requirements** specified (speed, accuracy, capacity, etc.)
- [ ] **Environmental requirements** defined (temp, humidity, IP rating, etc.)
- [ ] **Regulatory requirements** identified (CE, FCC, UL, industry-specific)
- [ ] **Cost targets** set (BOM cost, target selling price, margin goals)

### Project Planning

- [ ] **Project charter** completed and approved
- [ ] **High-level timeline** created with phase gate milestones
- [ ] **Budget allocated** for development phases
- [ ] **Team assembled** with roles and responsibilities defined
- [ ] **Key stakeholders** identified and engaged
- [ ] **Risk register** initiated with top 10 risks identified

### Exit Criteria - Concept to EVT

> [!WARNING]
> All critical items must be complete before advancing to EVT

**Critical:**
- ✅ PRD approved by stakeholders
- ✅ Technical feasibility demonstrated (proof-of-concept works)
- ✅ Budget and resources allocated for EVT phase
- ✅ Major technical risks have mitigation plans
- ✅ Project charter signed off

**Gate Review Attendees**: Executive sponsor, Product owner, Engineering leads, PM

---

## EVT Gate (Engineering Validation Test)

> [!NOTE]
> Gate 1 - Validate core functionality with first integrated prototypes

### Design Completion

- [ ] **Schematic design** completed and peer-reviewed
- [ ] **PCB layout** completed with DRC (Design Rule Check) passed
- [ ] **Mechanical CAD** completed (3D models of all parts)
- [ ] **Firmware architecture** defined and initial implementation complete
- [ ] **BOM (Bill of Materials)** created at 80% confidence level
- [ ] **Component sourcing** plan with lead-time analysis for long-lead items

### Prototype Build & Testing

- [ ] **EVT units built** (100-1,000 units with production-intent materials)
- [ ] **Functional testing** passed for all major features
- [ ] **Basic performance testing** completed (meets key specs)
- [ ] **Hardware-software integration** demonstrated (HW/FW working together)
- [ ] **Power budget** validated (battery life or power consumption within target)
- [ ] **Thermal testing** performed (initial temperature measurements at ambient)

### Technical Validation

- [ ] **Core functionality proven** - all major features work as designed
- [ ] **Electrical performance** validated (voltage levels, signal integrity, timing)
- [ ] **Mechanical fit** verified (all parts assemble correctly)
- [ ] **User interface** tested (buttons, displays, connectivity functional)
- [ ] **Critical subsystems** characterized (sensors, motors, communication modules)
- [ ] **Design weaknesses** identified with documented resolution plan

### Documentation

- [ ] **Test plan** created for DVT phase
- [ ] **Design review** completed with cross-functional team
- [ ] **Design documentation** updated (schematics, layouts, CAD files)
- [ ] **Known issues list** maintained with severity and priority
- [ ] **Lessons learned** captured from EVT build

### Exit Criteria - EVT to DVT

> [!WARNING]
> Design must be stable before investing in DVT hard tooling

**Critical:**
- ✅ Core functionality validated - product works as intended
- ✅ No major electrical or mechanical changes expected
- ✅ Power and thermal budgets within acceptable range (±20% of target)
- ✅ BOM cost tracking shows path to target cost
- ✅ Critical component availability confirmed (no obsolescence risk)
- ✅ Design ready for manufacturability review (DFM)

**Optional (may defer to DVT):**
- ⚠️ Full environmental testing (-10°C to +50°C)
- ⚠️ Pre-compliance EMI/EMC testing
- ⚠️ Drop testing and vibration testing

**Gate Review Attendees**: Product owner, Hardware lead, Firmware lead, Supply chain, Manufacturing eng, QA lead, PM

---

## DVT Gate (Design Validation Test)

> [!NOTE]
> Gate 2 - Lock design and validate production-readiness

### Design Finalization

- [ ] **Design freeze** - no further electrical or mechanical changes allowed
- [ ] **Final BOM** locked at 95%+ confidence
- [ ] **Hard tooling** ordered for all mechanical parts (injection molds, die-cast, etc.)
- [ ] **Production PCB** fabricated with final stackup and materials
- [ ] **Component qualification** completed for all critical parts
- [ ] **Design for Manufacturing (DFM)** review completed with CM feedback
- [ ] **Design for Test (DFT)** review completed - test points, fixtures defined

### DVT Build & Validation

- [ ] **DVT units built** (300-2,000 units from hard tools)
- [ ] **Functional yield** measured and documented (target >90%)
- [ ] **Cosmetic quality** assessed and documented
- [ ] **Assembly time** measured per unit (target production speed)
- [ ] **All test stations** operational with pass/fail limits defined
- [ ] **Pilot manufacturing line** setup and operator training completed

### Reliability & Compliance Testing

- [ ] **Environmental testing** passed (full temp range: -10°C to +50°C)
- [ ] **Thermal testing** passed (continuous operation at max ambient temp)
- [ ] **Drop testing** passed (package and product level)
- [ ] **Vibration testing** passed (MIL-STD-810G or equivalent)
- [ ] **Lifecycle testing** initiated (MTBF/longevity testing in progress)
- [ ] **EMI/EMC pre-compliance** testing completed
- [ ] **Safety testing** initiated (UL, IEC standards as applicable)
- [ ] **Regulatory submissions** prepared (FCC, CE, UL applications ready)

### Manufacturing Readiness

- [ ] **Manufacturing work instructions** created and reviewed
- [ ] **Test fixtures** designed and fabricated
- [ ] **Calibration procedures** defined for sensors/devices requiring calibration
- [ ] **Poka-yoke** (error-proofing) mechanisms implemented where needed
- [ ] **Supplier quality agreements** in place for critical components
- [ ] **Packaging design** completed and tested (drop/shipping tests)
- [ ] **Manufacturing yield analysis** completed with Pareto of failures

### Software & Firmware

- [ ] **Firmware feature-complete** with all planned functionality
- [ ] **OTA (Over-The-Air) update** mechanism tested and validated
- [ ] **Factory programming** process defined and tested
- [ ] **Diagnostic modes** implemented for manufacturing test
- [ ] **Software QA testing** completed (functional, regression, edge cases)

### Documentation

- [ ] **User manual** drafted (or final if required for certification)
- [ ] **Service manual** created for repair procedures
- [ ] **Compliance test reports** available for regulatory submissions
- [ ] **Manufacturing documentation package** delivered to CM
- [ ] **Design history file** updated (all changes, approvals, test results)

### Exit Criteria - DVT to PVT

> [!WARNING]
> Design must be fully frozen - changes at PVT are extremely costly

**Critical:**
- ✅ Design 100% frozen - all ECOs (Engineering Change Orders) closed
- ✅ All reliability testing passed (temp, drop, vibration, lifecycle)
- ✅ Regulatory compliance testing passed or in-progress with high confidence
- ✅ Manufacturing yields acceptable (functional >90%, cosmetic plan in place)
- ✅ Supply chain qualified - all vendors capable of production volumes
- ✅ Test coverage >95% - all failure modes detectable in manufacturing
- ✅ No critical open issues - all P0/P1 bugs resolved or have workarounds

**Gate Review Attendees**: Executive sponsor, Product owner, Hardware lead, Firmware lead, Supply chain, Manufacturing lead, QA lead, Compliance eng, PM

---

## PVT Gate (Production Validation Test)

> [!NOTE]
> Gate 3 - Validate mass production capability at production speeds

### PVT Build

- [ ] **PVT units built** (1K-20K units, phased as Red/Yellow/Green builds)
- [ ] **All units sellable** - intended to ship to customers if they pass testing
- [ ] **Production line validated** - units built at target line speed
- [ ] **Multiple lines qualified** (if applicable for volume requirements)
- [ ] **Operator training** completed - all assemblers certified
- [ ] **Production yield tracked** - functional yield >95%, cosmetic yield trending to target

### Process Validation

- [ ] **First article inspection (FAI)** passed for all suppliers
- [ ] **Statistical Process Control (SPC)** implemented for critical parameters
- [ ] **Process capability studies** completed (Cpk >1.33 for critical dimensions)
- [ ] **Tooling qualification** completed for all hard tools
- [ ] **Manufacturing documentation** validated on production floor
- [ ] **Line balance** optimized - no bottlenecks at target speed
- [ ] **Cycle time** measured and meets target (units per hour)

### Quality Systems

- [ ] **Incoming Quality Control (IQC)** procedures defined and active
- [ ] **In-Process Quality Control (IPQC)** checkpoints implemented
- [ ] **Final Quality Control (FQC)** procedures defined and active
- [ ] **Failure analysis process** established for RMA/returns
- [ ] **Traceability system** implemented (serial numbers, batch tracking)
- [ ] **Quality metrics dashboard** created (yield, defect rates, DPMO)

### Compliance & Certification

- [ ] **Regulatory certifications obtained** (FCC, CE, UL, etc.)
- [ ] **Compliance marks** added to product and packaging
- [ ] **Certification documentation** received and filed
- [ ] **Declaration of Conformity** signed
- [ ] **RoHS/REACH compliance** verified for all components

### Supply Chain Validation

- [ ] **Supplier capacity** validated - can deliver components for production volumes
- [ ] **Lead-time buffer** established for long-lead components
- [ ] **Inventory plan** finalized (safety stock, reorder points)
- [ ] **Alternate sourcing** qualified for single-source risk components
- [ ] **Logistics plan** validated (shipping, warehousing, fulfillment)

### Launch Readiness

- [ ] **Packaging final** - retail packaging (if applicable) approved
- [ ] **User documentation** final - manuals, quick start guides printed
- [ ] **Marketing materials** ready - product photos, specs, website content
- [ ] **Sales training** completed - sales team understands product
- [ ] **Support infrastructure** ready - customer service, RMA process, spare parts
- [ ] **Post-launch monitoring plan** defined (early field failure analysis)

### Exit Criteria - PVT to Production Launch

> [!WARNING]
> Must demonstrate consistent quality at production speeds

**Critical:**
- ✅ **Production yield targets met**:
  - First PVT run: **>70% acceptable** (with root cause analysis)
  - Second PVT run: **>85% required**
  - Pre-launch: **>92% required**
  - Volume production: **>95% functional, >90% cosmetic**
- ✅ Line speed meets target - no bottlenecks preventing volume shipment
- ✅ All regulatory certifications obtained and marked on product
- ✅ Supply chain capable of supporting 3 months of forecasted demand
- ✅ Quality systems operational - IQC, IPQC, FQC processes running
- ✅ No P0 (critical) bugs - all showstoppers resolved
- ✅ Customer support ready - RMA process, spare parts, documentation

**Gate Review Attendees**: Executive sponsor, Product owner, Hardware lead, Firmware lead, Supply chain, Manufacturing lead, QA lead, Compliance eng, Sales/Marketing, PM

---

## Production Launch Gate

> [!NOTE]
> Gate 4 - Authorization to ship products to customers at volume

### Pre-Launch Checklist

- [ ] **Launch plan approved** by executive team
- [ ] **First production run completed** - units shipped or ready to ship
- [ ] **Sales forecast** updated with current demand signal
- [ ] **Pricing finalized** - MSRP, volume discounts, channel margins set
- [ ] **Marketing campaign** launched (if consumer product)
- [ ] **Distribution channels** ready to receive inventory
- [ ] **Customer support trained** and ready to handle inquiries

### Production Monitoring

- [ ] **Daily production metrics** tracked (output, yield, DPMO)
- [ ] **Weekly quality reviews** scheduled with CM
- [ ] **Early field failure analysis (EFFA)** process active
- [ ] **Customer feedback loop** established (NPS, support tickets, returns)
- [ ] **Engineering support** allocated for production issues (FA, CA, ECO)

### Continuous Improvement

- [ ] **Cost reduction roadmap** defined (value engineering opportunities)
- [ ] **Yield improvement plan** active (Pareto of top defects targeted)
- [ ] **Supplier performance reviews** scheduled (quarterly audits)
- [ ] **Lessons learned session** conducted with full team
- [ ] **Post-launch review** scheduled for 30/60/90 days

### Exit Criteria - Production Sustaining

**Critical:**
- ✅ First 1,000 units shipped to customers
- ✅ Production yield stable >95% for 2 consecutive weeks
- ✅ No critical field failures (P0/P1 bugs in production units)
- ✅ Supply chain delivering to plan (no material shortages)
- ✅ Customer support handling inquiries (<24hr response time)

**Gate Review Attendees**: Executive sponsor, Product owner, Operations lead, Supply chain, QA lead, Sales/Marketing, Customer support, PM

---

## Phase Gate Best Practices

### Conducting Gate Reviews

1. **Schedule reviews 1 week in advance** with all required attendees
2. **Distribute checklist** 48 hours before review - mark completed items
3. **Focus on exit criteria** - don't get lost in details during review
4. **Document decisions** - minutes with action items, owners, due dates
5. **Red/Yellow/Green rating** for each section to visualize readiness

### Managing Gate Delays

> [!WARNING]
> Common reasons gates slip and how to prevent them

| Issue | Prevention Strategy |
|-------|-------------------|
| **Incomplete testing** | Start test planning at previous phase |
| **Supplier delays** | Dual-source critical components, place orders early |
| **Design issues late in phase** | Front-load risk identification, FMEA at Concept |
| **Documentation lag** | Assign tech writer early, update docs continuously |
| **Stakeholder availability** | Block gate review dates at project kickoff |

### Phase Duration Guidelines

| Phase | Typical Duration | Factors that Extend |
|-------|------------------|-------------------|
| **Concept** | 4-8 weeks | Novel technology, complex market analysis |
| **EVT** | 3-6 months | First-time technologies, extensive prototyping |
| **DVT** | 3-6 months | Reliability testing duration, compliance testing |
| **PVT** | 2-4 months | Yield ramp-up, multi-line qualification |

### Red Flags to Escalate

- 🚨 **Major functionality not working** at EVT gate
- 🚨 **Thermal failure** requiring mechanical redesign at DVT
- 🚨 **Compliance test failure** requiring re-spin at DVT
- 🚨 **Supply chain single-source risk** with no mitigation at PVT
- 🚨 **Yield <80%** at PVT gate

---

## Checklist Usage Tips

### For Project Managers

- Review checklist at project kickoff and customize for your product
- Track completion % for each phase in weekly status reports
- Use as agenda for weekly team sync meetings
- Highlight blocked items requiring escalation

### For Engineering Leads

- Assign owners to each checklist item during sprint planning
- Use checklist to define Definition of Done for phase completion
- Reference checklist when scoping work - "what do we need for DVT gate?"
- Archive completed checklists for lessons learned

### For Executives

- Use gate reviews as decision points (Go/No-Go/Pivot)
- Assess resource needs for next phase based on exit criteria
- Compare actual vs. planned progress at each gate
- Identify patterns across projects to improve process

---

## Templates & Tools

### Gate Review Template

```markdown
# [PHASE] Gate Review - [PROJECT_NAME]

**Date**: [DATE]
**Attendees**: [LIST]
**Phase Status**: 🟢 On Track | 🟡 At Risk | 🔴 Blocked

## Checklist Completion
- Section 1: [X/Y] items complete
- Section 2: [X/Y] items complete
...

## Key Accomplishments
- [Bullet list of wins]

## Outstanding Issues
| Issue | Severity | Owner | Due Date | Status |
|-------|----------|-------|----------|--------|
| [Description] | P0/P1/P2 | [Name] | [Date] | Open/Blocked/Resolved |

## Decision
- [ ] **PASS** - Advance to [NEXT PHASE]
- [ ] **CONDITIONAL PASS** - Advance with must-fix items before [DATE]
- [ ] **FAIL** - Remain in current phase, re-review [DATE]

**Approvals**:
- Executive Sponsor: ________________
- Product Owner: ________________
- Engineering Lead: ________________
```

---

**Document Version**: 1.0  
**Template**: hardware-pm-starter-kit v1.0  
**Last Updated**: `08/02/2026`

---

## Related Templates

- [Project Charter](./project-charter-hardware.md) - Define project scope and objectives
- [Risk Register](./risk-register-hardware.md) - Track phase-specific risks
- [Sprint Planning](./sprint-planning-hardware.md) - Plan work within each phase
- [Lessons Learned](./lessons-learned-template.md) - Capture insights at each gate
