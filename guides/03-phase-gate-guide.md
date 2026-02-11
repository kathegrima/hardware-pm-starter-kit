# Phase Gate Deep Dive Guide

> **Master the hardware development lifecycle: EVT → DVT → PVT → MP**

---

## Table of Contents

1. [Introduction to Phase Gates](#introduction-to-phase-gates)
2. [Phase Gate Overview](#phase-gate-overview)
3. [Concept Phase](#concept-phase)
4. [EVT - Engineering Validation Test](#evt---engineering-validation-test)
5. [DVT - Design Validation Test](#dvt---design-validation-test)
6. [PVT - Production Validation Test](#pvt---production-validation-test)
7. [MP - Mass Production](#mp---mass-production)
8. [Phase Transition Best Practices](#phase-transition-best-practices)
9. [Common Pitfalls by Phase](#common-pitfalls-by-phase)
10. [Decision Framework](#decision-framework)

---

## Introduction to Phase Gates

### What Are Phase Gates?

**Phase gates** are formal decision points in hardware development where a project must meet specific criteria before advancing to the next phase. Think of them as **quality checkpoints** that prevent costly mistakes from propagating forward.

**Why Phase Gates Matter**:
- **Cost increases 10x** with each phase - fixing a $1K issue in EVT costs $10K in DVT, $100K in PVT
- **Design changes become exponentially more expensive** after tooling investment
- **Risk reduction** - retiring major risks early prevents project failure
- **Resource allocation** - ensures investment only in viable projects
- **Team alignment** - everyone understands what "done" means for each phase

---

### The Hardware Development Lifecycle

```
Concept → EVT → DVT → PVT → MP → Maintenance → EOL
   ↓       ↓      ↓      ↓      ↓        ↓         ↓
 Idea   Prototype Valid  Validate Volume  Support  Phase-out
               Design  Production  Mfg
```

**Key Principle**: Each phase answers a specific question:
- **Concept**: *Can we build it?* (Feasibility)
- **EVT**: *Does it work?* (Functionality)
- **DVT**: *Does it meet all requirements?* (Design validation)
- **PVT**: *Can we manufacture it?* (Production validation)
- **MP**: *Can we scale it?* (Volume manufacturing)

---

## Phase Gate Overview

### Phase Comparison Matrix

| Aspect | Concept | EVT | DVT | PVT | MP |
|--------|---------|-----|-----|-----|-----|
| **Duration** | 4-8 weeks | 8-16 weeks | 12-20 weeks | 8-16 weeks | Ongoing |
| **Build Quantity** | 0-5 units | 10-100 units | 100-500 units | 100-1,000 units | >5,000 units |
| **Build Method** | Breadboard, 3D print | PCB + soft tools | PCB + soft tools | Hard tooling | Production tooling |
| **Design Changes** | Frequent | Common | Minimal | Rare | None (ECO only) |
| **Cost per Unit** | Very high | High | Medium | Near-target | Target COGS |
| **Testing Depth** | Basic function | Functional | Full validation | Production QC | Ongoing reliability |
| **Primary Goal** | Feasibility | Prove concept | Validate design | Validate manufacturing | Scale & optimize |
| **Risk Level** | Very high | High | Medium | Low | Very low |
| **Team Size** | 2-5 people | 5-10 people | 10-20 people | 15-30 people | Full organization |

---

### Investment and Risk by Phase

```
Cost        │                                    ┌─────────────
Committed   │                               ┌────┘
            │                          ┌────┘
            │                     ┌────┘
            │                ┌────┘
            │           ┌────┘
            │      ┌────┘
            │ ┌────┘
            └─┴────┴────┴────┴────┴─────────────────────────>
             Concept EVT DVT PVT  MP

Risk to     │
Change      │ ████████████
            │ ████████████
            │ ████████
            │ ███
            │ █
            └─┴────┴────┴────┴────┴─────────────────────────>
             Concept EVT DVT PVT  MP
```

**Key Insight**: Make major decisions early when change is cheap. After DVT, changes become prohibitively expensive.

---

## Concept Phase

### Overview

**Duration**: 4-8 weeks  
**Team Size**: 2-5 people (PM, HW lead, FW lead, ME lead)  
**Budget**: 5-10% of total project budget  
**Prototypes**: 0-5 proof-of-concept units (optional)

**Primary Question**: *Is this project technically and commercially feasible?*

---

### Objectives

**Technical Feasibility**:
- Validate that core technology exists and is mature enough
- Identify major technical risks and feasibility blockers
- Prove critical subsystems work (proof-of-concept demos)
- Define system architecture and technology choices

**Business Feasibility**:
- Validate market demand and customer willingness to pay
- Confirm business case (revenue potential, margin targets)
- Assess competitive landscape and differentiation
- Estimate development cost and timeline

**Requirements Definition**:
- Create Product Requirements Document (PRD)
- Define success criteria and acceptance tests
- Identify regulatory requirements (CE, FCC, FDA, etc.)
- Establish BOM cost targets and volume forecasts

---

### Key Activities

**Week 1-2: Discovery**
- Market research and competitive analysis
- Customer interviews (minimum 10-20 target users)
- Technology landscape review
- Rough order of magnitude (ROM) cost estimate

**Week 3-4: Architecture & Planning**
- System architecture design (block diagram)
- Component selection (major ICs, sensors, modules)
- Risk assessment (top 10 risks identified)
- Project timeline and resource plan

**Week 5-6: Proof of Concept (Optional)**
- Build breadboard or dev-kit prototype
- Validate critical technology choices
- Test most risky subsystems
- Measure key performance metrics

**Week 7-8: Documentation & Approval**
- Finalize PRD
- Create project charter
- Prepare business case presentation
- Conduct Concept Phase Gate Review

---

### Deliverables

**Must-Have Deliverables**:
- [ ] Product Requirements Document (PRD) - approved by stakeholders
- [ ] Project Charter - approved by sponsor
- [ ] System architecture diagram (block diagram)
- [ ] Risk register (top 10+ risks with mitigation plans)
- [ ] Preliminary BOM (80% confidence on major components)
- [ ] ROM budget estimate (±50% accuracy)
- [ ] High-level project timeline (phase durations)
- [ ] Business case (revenue projections, ROI analysis)

**Optional Deliverables**:
- [ ] Proof-of-concept prototype (if high-risk technology)
- [ ] Technology feasibility report
- [ ] Competitive teardown analysis
- [ ] Customer survey results

---

### Gate Criteria - Concept to EVT

**Go/No-Go Decision**: Can we commit engineering resources to detailed design?

**Technical Criteria**:
- [ ] **Critical technologies proven feasible** - no show-stoppers identified
- [ ] **System architecture defined** - major subsystems identified and interfaces defined
- [ ] **Component availability confirmed** - no EOL or allocation risks for critical parts
- [ ] **Technical risks assessed** - top 10 risks have mitigation plans

**Business Criteria**:
- [ ] **Business case approved** - ROI meets company hurdle rate (e.g., >30% margin)
- [ ] **Market demand validated** - customer interviews confirm problem/solution fit
- [ ] **Competitive differentiation clear** - we have a defensible advantage
- [ ] **Budget allocated** - funding approved for EVT phase

**Regulatory/Compliance**:
- [ ] **Regulatory path identified** - know which certifications are required
- [ ] **Compliance timeline feasible** - certification won't block launch timeline
- [ ] **No legal blockers** - no patent conflicts or regulatory show-stoppers

**Organizational**:
- [ ] **Team committed** - key personnel allocated to project
- [ ] **Stakeholder alignment** - executive sponsor and key stakeholders support project
- [ ] **PRD approved** - all stakeholders agree on requirements

**Typical Pass Rate**: 60-70% of concepts advance to EVT (30-40% killed at this gate)

---

### Common Pitfalls - Concept Phase

**❌ Pitfall 1: Skipping customer validation**
- **Symptom**: "We know what customers want" without talking to them
- **Impact**: Building the wrong product, pivot required in DVT
- **Solution**: Interview 10-20 target users, validate problem/solution fit

**❌ Pitfall 2: Underestimating regulatory complexity**
- **Symptom**: "We'll figure out compliance later"
- **Impact**: 6-12 month delay when certification fails, costly redesign
- **Solution**: Engage compliance expert in Concept phase, budget time/money

**❌ Pitfall 3: Overly optimistic BOM cost**
- **Symptom**: "We'll negotiate better pricing at volume"
- **Impact**: Product not profitable, forced cost-down in PVT
- **Solution**: Use realistic component pricing (10K volume quotes), add 20% margin

**❌ Pitfall 4: Ignoring component availability**
- **Symptom**: Selecting cutting-edge or EOL components
- **Impact**: Supply chain crisis mid-project, forced redesign
- **Solution**: Check lifecycle status, confirm 16+ week lead times acceptable, dual-source

---

## EVT - Engineering Validation Test

### Overview

**Duration**: 8-16 weeks  
**Team Size**: 5-10 people (HW, FW, ME, test engineer)  
**Budget**: 15-25% of total project budget  
**Prototypes**: 10-100 units (hand-assembled or low-volume PCB)

**Primary Question**: *Does the design work as intended?*

---

### Objectives

**Prove Core Functionality**:
- Demonstrate all major features work
- Validate electrical performance (voltage levels, signal integrity, timing)
- Confirm mechanical fit and assembly
- Test hardware-firmware integration

**Retire Technical Risks**:
- Test highest-risk subsystems (thermal, power, EMI, mechanical stress)
- Validate critical component choices
- Prove technology readiness

**Refine Design**:
- Identify design weaknesses and failure modes
- Optimize performance (power consumption, speed, accuracy)
- Gather data for DVT design improvements

**Not Yet Required**:
- Full environmental testing (-10°C to +50°C)
- Compliance testing (EMI/EMC, safety)
- Manufacturing optimization (DFM)
- Cosmetic/industrial design perfection

---

### Key Activities

**Week 1-3: Detailed Design**
- Schematic design and peer review
- Component selection finalized (with alternates)
- PCB layout (production-intent stackup)
- Mechanical CAD design (enclosure, mounting)
- Firmware architecture defined

**Week 4-6: Prototype Build**
- PCB fabrication (2-4 week lead time)
- PCB assembly (hand assembly or low-volume CM)
- Mechanical prototypes (3D printed or CNC machined)
- Component procurement (long-lead items ordered)

**Week 7-10: Bring-Up & Testing**
- Board bring-up (power-on, smoke test)
- Firmware development and debugging
- Functional testing (all features exercised)
- Performance characterization (speed, accuracy, power)
- Hardware-firmware integration testing

**Week 11-14: Validation & Analysis**
- Thermal testing (IR camera, thermocouples)
- Basic environmental testing (temperature extremes)
- Reliability testing (power cycling, stress testing)
- Failure mode analysis (what breaks and why)

**Week 15-16: Documentation & Gate Prep**
- Test reports and data analysis
- Design review with cross-functional team
- Risk register update (risks retired or escalated)
- DVT planning (what to change, what to keep)
- EVT Gate Review presentation

---

### Deliverables

**Design Documentation**:
- [ ] Schematic diagrams (all subsystems)
- [ ] PCB layout files and Gerbers
- [ ] Mechanical CAD files (enclosure, assembly)
- [ ] Firmware source code (architecture + core modules)
- [ ] BOM (Bill of Materials) with part numbers and suppliers

**Prototypes**:
- [ ] 10-100 EVT prototype units built
- [ ] At least 5 units fully functional for testing
- [ ] Prototypes distributed to team for evaluation

**Test Results**:
- [ ] Functional test report (pass/fail for each feature)
- [ ] Performance characterization data
- [ ] Thermal analysis (max temps at ambient)
- [ ] Power consumption measurements
- [ ] Known issues list (bugs, limitations, failures)

**Planning Documents**:
- [ ] DVT design changes list (based on EVT learnings)
- [ ] Risk register update (risks retired or elevated)
- [ ] Component lead-time tracker (order dates for DVT)

---

### Gate Criteria - EVT to DVT

**Go/No-Go Decision**: Is the design ready for full validation and tooling investment?

**Technical Criteria**:
- [ ] **Core functionality proven** - all major features work as designed
- [ ] **Performance meets targets** - within 20% of spec (e.g., battery life, speed, accuracy)
- [ ] **Hardware-firmware integration successful** - HW and FW teams aligned on interfaces
- [ ] **No show-stopper failures** - no fundamental design flaws requiring complete redesign
- [ ] **Thermal budget within range** - components not exceeding max ratings at 25°C ambient

**Design Maturity**:
- [ ] **Schematic peer-reviewed** - no major errors or omissions
- [ ] **BOM 90% stable** - only minor component changes expected
- [ ] **Mechanical fit validated** - all parts assemble correctly, no interference
- [ ] **Known issues manageable** - bug list is short and all issues have fixes planned

**Risk Assessment**:
- [ ] **Major technical risks retired** - high-risk areas tested and proven
- [ ] **No new critical risks discovered** - if new risks found, mitigation plan in place
- [ ] **Component availability confirmed** - no EOL or allocation issues for DVT

**Planning Readiness**:
- [ ] **DVT plan approved** - know what to change and what to keep
- [ ] **Budget and timeline on track** - no major overruns
- [ ] **Team capacity confirmed** - resources available for DVT phase

**Typical Pass Rate**: 80-90% of EVT projects advance to DVT (10-20% require EVT rev 2 or are cancelled)

---

### Common Pitfalls - EVT Phase

**❌ Pitfall 1: Treating EVT like production hardware**
- **Symptom**: Obsessing over cosmetics, DFM, cost optimization
- **Impact**: Delayed schedule, missing the EVT goal (prove functionality)
- **Solution**: Focus on function, not form. Accept hand-assembly and high cost.

**❌ Pitfall 2: Not testing thermal performance early**
- **Symptom**: "We'll add heatsinks later if needed"
- **Impact**: 6-week delay in DVT for thermal redesign, mechanical changes
- **Solution**: IR camera thermal imaging in EVT, test at 40°C ambient minimum

**❌ Pitfall 3: Skipping hardware-firmware integration testing**
- **Symptom**: HW and FW teams working in silos until DVT
- **Impact**: Integration crisis in DVT, schedule slip
- **Solution**: Daily HW-FW standups, integration testing as soon as board boots

**❌ Pitfall 4: Ignoring known issues**
- **Symptom**: "We'll fix that in DVT" without documenting
- **Impact**: Issues forgotten, resurface in PVT
- **Solution**: Maintain detailed issue tracker, assign owner and priority to every bug

---

## DVT - Design Validation Test

### Overview

**Duration**: 12-20 weeks  
**Team Size**: 10-20 people (full cross-functional team)  
**Budget**: 30-40% of total project budget  
**Prototypes**: 100-500 units (production-intent build)

**Primary Question**: *Does the design meet ALL requirements and is it ready for tooling?*

---

### Objectives

**Validate Production-Intent Design**:
- Prove design meets all functional, performance, and regulatory requirements
- Pass full environmental testing (temperature, humidity, drop, vibration)
- Pass pre-compliance testing (EMI/EMC, safety)
- Validate user experience and industrial design

**Prepare for Manufacturing**:
- Design for Manufacturing (DFM) review with CM
- Simplify assembly and reduce manufacturing risk
- Finalize BOM with production-intent components
- Develop test fixtures and procedures

**Freeze Design**:
- Lock electrical design (no further schematic changes)
- Lock mechanical design (ready for tooling)
- Freeze firmware architecture (features complete)
- Approve tooling investment ($50K-$500K+)

**Critical Decision Point**: After DVT, design changes require formal ECO (Engineering Change Order) process and are very expensive.

---

### Key Activities

**Week 1-4: DVT Design & Build Prep**
- Implement EVT design changes (schematic updates)
- PCB layout rev 2 (production stackup and materials)
- Mechanical design updates (DFM improvements)
- Component procurement (long-lead items, production-intent parts)
- Test fixture design kickoff

**Week 5-8: DVT Build**
- PCB fabrication (production fab house)
- PCB assembly (production CM if possible)
- Mechanical prototypes (soft tooling - CNC, urethane casting)
- Firmware feature completion (all requirements implemented)
- Test fixture fabrication

**Week 9-14: Comprehensive Testing**
- Functional testing (100% feature coverage)
- Environmental testing:
  - Temperature: -10°C to +50°C (or product spec range)
  - Humidity: 10-90% RH
  - Thermal shock: rapid temp changes
  - Altitude: low pressure simulation (if applicable)
- Mechanical testing:
  - Drop test: 1.5m onto concrete (6 orientations)
  - Vibration: MIL-STD-810G or equivalent
  - Mechanical life: button presses, connector cycles
- Compliance pre-testing:
  - EMI/EMC: radiated and conducted emissions (pre-cert lab)
  - Safety: leakage current, insulation, flammability
- Reliability testing:
  - Accelerated life testing (ALT)
  - Highly Accelerated Life Testing (HALT) - optional
  - Power cycling (on/off 1000+ cycles)

**Week 15-18: DFM & Manufacturing Prep**
- DFM review with CM (design for manufacturability)
- Assembly time study (target cycle time)
- Test procedure validation (functional test, calibration)
- Tooling design and vendor selection
- Compliance testing (official certification if on critical path)

**Week 19-20: Design Freeze & Gate Prep**
- Final design review (cross-functional sign-off)
- Design freeze declaration (no changes without ECO)
- Tooling kickoff (injection molds, stamping dies, jigs)
- DVT Gate Review presentation
- PVT planning (build quantity, schedule, test plan)

---

### Deliverables

**Validated Design**:
- [ ] Production-intent schematic (frozen)
- [ ] Production-intent PCB layout (frozen)
- [ ] Production-intent mechanical design (ready for tooling)
- [ ] Firmware feature-complete (all requirements implemented)
- [ ] BOM frozen (95% confidence, production part numbers)

**Test Results**:
- [ ] Functional test report (100% pass rate on working units)
- [ ] Environmental test report (all tests passed)
- [ ] EMI/EMC pre-compliance report (margins to limits documented)
- [ ] Safety test report (meets IEC/UL standards)
- [ ] Reliability test report (MTBF estimate, failure modes)
- [ ] User acceptance testing results (if applicable)

**Manufacturing Readiness**:
- [ ] DFM report from CM (issues resolved)
- [ ] Test fixture operational (functional test, calibration)
- [ ] Manufacturing work instructions (assembly, test, QC)
- [ ] Tooling design approved (molds, dies, jigs)
- [ ] Supplier qualification complete (critical components)

**Compliance**:
- [ ] Compliance test plan (FCC, CE, UL, etc.)
- [ ] Pre-compliance testing complete (know margin to limits)
- [ ] Certification timeline confirmed (lab booked, fees quoted)

---

### Gate Criteria - DVT to PVT

**Go/No-Go Decision**: Is the design ready to commit to hard tooling and pilot production?

**Design Validation**:
- [ ] **All requirements met** - functional, performance, environmental, regulatory
- [ ] **Environmental testing passed** - temp, humidity, drop, vibration all passed
- [ ] **Pre-compliance testing passed** - EMI/EMC margins >3dB, safety margins clear
- [ ] **Reliability targets met** - MTBF estimate meets spec, no early-life failures
- [ ] **User testing validated** - beta testers (if applicable) confirm usability

**Manufacturing Readiness**:
- [ ] **DFM review complete** - CM confirms design is manufacturable at target yield
- [ ] **Assembly time acceptable** - cycle time meets production throughput target
- [ ] **Test coverage sufficient** - functional test catches >95% of defects
- [ ] **Tooling approved** - tooling design reviewed and approved by CM and ME
- [ ] **BOM cost on target** - within 10% of COGS target at production volume

**Design Freeze**:
- [ ] **Electrical design frozen** - no further schematic or layout changes
- [ ] **Mechanical design frozen** - ready for hard tooling (injection molds)
- [ ] **Firmware feature-complete** - all requirements implemented, only bug fixes remain
- [ ] **ECO process established** - formal change control for post-freeze changes

**Risk & Compliance**:
- [ ] **No critical risks remaining** - all high-risk areas validated
- [ ] **Compliance timeline clear** - know when certifications will complete
- [ ] **Supply chain stable** - no component EOL or allocation issues

**Business Approval**:
- [ ] **Tooling investment approved** - $50K-$500K+ budget allocated
- [ ] **PVT timeline approved** - schedule for pilot build and certifications
- [ ] **Business case reconfirmed** - still profitable at current BOM cost

**Typical Pass Rate**: 70-80% of DVT projects advance to PVT (20-30% require DVT rev 2 or significant changes)

**Critical**: This is the **last chance** to make design changes before expensive tooling. Scrutinize every aspect of the design.

---

### Common Pitfalls - DVT Phase

**❌ Pitfall 1: Skipping pre-compliance testing**
- **Symptom**: "We'll pass certification on the first try"
- **Impact**: $50K+ wasted on failed certification, 2-3 month delay for redesign
- **Solution**: Always pre-test EMI/EMC at DVT. Budget $10K-$20K for pre-cert lab.

**❌ Pitfall 2: Not involving CM early enough**
- **Symptom**: DFM review happens in PVT, after tooling is committed
- **Impact**: Yield issues, assembly time 2x target, costly rework
- **Solution**: DFM review in DVT with CM engineer, incorporate feedback before freeze

**❌ Pitfall 3: Declaring design freeze prematurely**
- **Symptom**: Design freeze before environmental testing complete
- **Impact**: Thermal or mechanical failure found in testing → expensive ECO
- **Solution**: Design freeze AFTER all testing complete and passed

**❌ Pitfall 4: Underestimating tooling lead time**
- **Symptom**: "We'll order molds after DVT gate review"
- **Impact**: 10-16 week tooling delay pushes PVT and launch
- **Solution**: Start tooling design in parallel with DVT testing, order immediately after gate

**❌ Pitfall 5: Ignoring certification timeline**
- **Symptom**: "We'll get certified during PVT"
- **Impact**: Certification takes 3-6 months, delays launch
- **Solution**: Start official certifications in DVT if on critical path (parallel with PVT)

---

## PVT - Production Validation Test

### Overview

**Duration**: 8-16 weeks  
**Team Size**: 15-30 people (engineering + manufacturing + quality)  
**Budget**: 20-30% of total project budget  
**Prototypes**: 500-5,000 units (pilot production run)

**Primary Question**: *Can we manufacture this design at the target cost, yield, and quality?*

---

### Objectives

**Validate Manufacturing Process**:
- Prove production line can build units at target cycle time
- Achieve target manufacturing yield (typically >95%)
- Validate test coverage (functional test, QC checks)
- Train production operators and finalize work instructions

**Validate Production Quality**:
- Statistical process control (SPC) on critical parameters
- First-pass yield (FPY) tracking and optimization
- Quality metrics meet targets (defect rates, cosmetic quality)
- Failure analysis on any defects found

**Complete Certifications**:
- Finalize compliance testing (FCC, CE, UL, FDA, etc.)
- Submit certification applications and obtain approvals
- Complete any required agency audits or inspections

**Prepare for Launch**:
- Finalize packaging and logistics
- Create end-of-line test procedure and QC checks
- Establish supply chain for volume production
- Complete user documentation and support materials

---

### Key Activities

**Week 1-4: PVT Build Preparation**
- Hard tooling delivered (injection molds, stamping dies)
- Production line setup and operator training
- Component procurement for pilot run (500-5,000 units)
- Test fixtures deployed to production line
- First article inspection (FAI) from tooling samples

**Week 5-8: Pilot Production Run**
- First builds (10-50 units) with close monitoring
- Yield tracking and defect analysis
- Process refinement (cycle time, workstation layout)
- Ramp to pilot volume (500-5,000 units)
- Cosmetic inspection and packaging validation

**Week 9-12: Testing & Certification**
- Functional testing on pilot units (sample size: 100+ units)
- Environmental stress screening (ESS) on sample
- Accelerated life testing (ALT) on sample
- Final compliance testing (if not complete in DVT)
- Certification approvals received

**Week 13-16: Launch Preparation**
- Final yield optimization (target >95%)
- Quality metrics baseline established
- Supply chain ramp for volume production
- Packaging and logistics validated (ship samples)
- Post-launch monitoring plan established
- PVT Gate Review and launch approval

---

### Deliverables

**Manufacturing Validation**:
- [ ] Pilot build complete (500-5,000 units)
- [ ] Manufacturing yield report (FPY, defect Pareto)
- [ ] Cycle time analysis (meets production throughput)
- [ ] Process capability study (Cpk >1.33 for critical parameters)
- [ ] Operator training complete and documented

**Quality Validation**:
- [ ] Test coverage report (functional test catches >95% of defects)
- [ ] Calibration procedure validated (if applicable)
- [ ] Quality control procedures finalized
- [ ] Cosmetic inspection standards (AQL levels)
- [ ] Failure analysis reports (root cause for any defects)

**Certifications Complete**:
- [ ] FCC certification (if required)
- [ ] CE marking (if required)
- [ ] UL listing (if required)
- [ ] FDA clearance (if medical device)
- [ ] RoHS, REACH, WEEE declarations
- [ ] Other regional certifications

**Launch Readiness**:
- [ ] Packaging design approved (retail or shipping packaging)
- [ ] User documentation complete (quick start guide, manual)
- [ ] Supply chain ready for volume (component inventory, CM capacity)
- [ ] Logistics validated (shipping, warehousing, distribution)
- [ ] Customer support ready (RMA process, warranty terms)

---

### Gate Criteria - PVT to MP

**Go/No-Go Decision**: Are we ready to launch and scale to volume production?

**Manufacturing Readiness**:
- [ ] **Yield targets met**:
  - First PVT run: **>70% acceptable** (all failures root-caused)
  - Second PVT run: **>85% required**
  - Pre-launch run: **>92% required**
  - Volume production: **>95%**
- [ ] **Cycle time acceptable** - meets production throughput requirements
- [ ] **Cost target achieved** - actual COGS within 5% of target
- [ ] **Test coverage validated** - functional test catches >95% of defects
- [ ] **Operator training complete** - production team can build without engineering support

**Quality Validation**:
- [ ] **Quality metrics met** - defect rate, cosmetic quality meet targets
- [ ] **Process capability proven** - Cpk >1.33 for critical parameters
- [ ] **No systemic failures** - no recurring defects or failure modes
- [ ] **Field-ready units** - pilot units meet all specs, ready to ship to customers

**Compliance Complete**:
- [ ] **All certifications obtained** - FCC, CE, UL, FDA, etc. (as applicable)
- [ ] **Compliance documentation complete** - DoC, test reports, labels
- [ ] **No regulatory blockers** - legal to sell in target markets

**Supply Chain Ready**:
- [ ] **Component inventory secured** - enough inventory for 3-6 month ramp
- [ ] **CM capacity confirmed** - production slots booked for volume ramp
- [ ] **No supplier risks** - no EOL, allocation, or single-source risks
- [ ] **Logistics validated** - packaging, shipping, distribution proven

**Business Approval**:
- [ ] **Launch plan approved** - go-to-market strategy finalized
- [ ] **Volume forecast confirmed** - sales forecast and production plan aligned
- [ ] **Post-launch support ready** - customer service, warranty, RMA process
- [ ] **Financial approval** - business case reconfirmed, ROI acceptable

**Typical Pass Rate**: 90-95% of PVT projects launch to MP (5-10% delayed for yield or compliance issues)

---

### Common Pitfalls - PVT Phase

**❌ Pitfall 1: Skipping pilot build**
- **Symptom**: "Tooling looks good, let's go straight to volume"
- **Impact**: Yield disaster at volume launch, scrambling to fix issues
- **Solution**: Always run 500-2,000 unit pilot before volume ramp

**❌ Pitfall 2: Not addressing low yield issues**
- **Symptom**: "85% yield is good enough, we'll improve it later"
- **Impact**: 15% scrap cost destroys margins, quality issues in field
- **Solution**: Don't launch until yield >95%. Root cause and fix defects.

**❌ Pitfall 3: Waiting for certifications in PVT**
- **Symptom**: Certification testing starts in PVT
- **Impact**: 3-6 month delay while waiting for approvals
- **Solution**: Start certifications in DVT (parallel with PVT build)

**❌ Pitfall 4: Not validating packaging and logistics**
- **Symptom**: Packaging designed but not tested with real units
- **Impact**: Damage during shipping, customer complaints, returns
- **Solution**: Ship pilot units to test sites, validate packaging survives

**❌ Pitfall 5: Declaring launch without post-launch monitoring plan**
- **Symptom**: "We shipped, project done!"
- **Impact**: Field failures go undetected, no feedback loop for improvements
- **Solution**: Establish field failure tracking, return rate monitoring, and continuous improvement process

---

## MP - Mass Production

### Overview

**Duration**: Ongoing (product lifetime)  
**Team Size**: Full organization (engineering, operations, support)  
**Focus**: Scale, optimize, support

**Primary Questions**: 
- *Can we scale production to meet demand?*
- *How do we continuously improve quality and reduce cost?*
- *How do we support customers and handle field issues?*

---

### Objectives

**Volume Manufacturing**:
- Ramp production to meet sales forecast
- Maintain quality and yield as volume increases
- Optimize production efficiency and reduce cost

**Continuous Improvement**:
- Monitor field performance and failure rates
- Cost reduction initiatives (value engineering)
- Process optimization and automation

**Product Support**:
- Customer support and warranty management
- RMA (Return Merchandise Authorization) process
- Field issue tracking and root cause analysis

---

### Key Activities - First 6 Months

**Month 1-2: Initial Ramp**
- Start with low volume (10-20% of target capacity)
- Daily quality checks and yield monitoring
- Close communication between CM and engineering
- Rapid response to any issues found

**Month 3-4: Volume Ramp**
- Increase production volume week by week
- Supply chain stabilization (consistent lead times)
- Operator efficiency improvements
- Field performance monitoring begins

**Month 5-6: Steady State**
- Target production volume achieved
- Quality metrics stable (defect rates, return rates)
- Cost reduction opportunities identified
- Product roadmap for next version begins

---

### Key Metrics - Mass Production

**Manufacturing Metrics**:
- **First-Pass Yield (FPY)**: >95% target
- **Cycle Time**: Meets throughput target (e.g., 1 unit per 5 minutes)
- **Defect Rate**: <1% (parts per thousand)
- **On-Time Delivery**: >98% of orders ship on time

**Quality Metrics**:
- **Field Return Rate**: <2% in first year (varies by product)
- **Customer Satisfaction (NPS)**: >50 (industry-dependent)
- **Warranty Claim Rate**: <5% in first year
- **Mean Time Between Failures (MTBF)**: Meets spec

**Supply Chain Metrics**:
- **Component Lead Time**: Predictable and within planning window
- **Inventory Turns**: 4-8 turns per year (depends on product)
- **Supplier Quality**: <0.1% defect rate from suppliers

**Financial Metrics**:
- **COGS**: Within ±5% of target
- **Gross Margin**: Meets target (e.g., 40-50%)
- **Inventory Carrying Cost**: Optimized (not overstocked)

---

### Engineering Change Orders (ECOs)

**When to Issue an ECO**:
- Critical field failure or safety issue (immediate)
- Cost reduction opportunity (planned quarterly)
- Component EOL or availability issue (as needed)
- Performance improvement (planned for next version)

**ECO Process**:
1. Identify issue or opportunity
2. Engineering assessment (impact, cost, timeline)
3. Prototype and test proposed change
4. CCB (Change Control Board) approval
5. Pilot run with change implemented
6. Validate yield and quality with change
7. Roll out to production

**ECO Cost**: Expect $10K-$50K per ECO (engineering time, prototype builds, validation testing)

---

### Product Lifecycle Management

**Early Life (0-6 months post-launch)**:
- Close monitoring of field failures
- Rapid response to any issues (weekly reviews)
- Engineering team on standby for support

**Growth Phase (6-18 months post-launch)**:
- Cost reduction initiatives (value engineering)
- Supply chain optimization
- Production automation opportunities
- Next-gen product planning

**Mature Phase (18+ months post-launch)**:
- Stable production and quality
- Incremental improvements only
- Focus shifts to next-gen product
- Begin end-of-life planning

**End of Life (EOL)**:
- Last-time-buy for components
- Final production run (lifetime buy)
- Service parts inventory secured
- Transition customers to next-gen product

---

## Phase Transition Best Practices

### General Principles

**1. Don't Skip Phases**
- Each phase serves a specific purpose
- Skipping EVT to save time = 2x the problems in DVT
- Exception: Very simple products or 2nd-gen products may compress phases

**2. Don't Rush Phase Gates**
- Gate criteria exist for a reason
- Advancing before ready = exponentially more expensive fixes later
- "We'll fix it in the next phase" usually means "We'll delay the project 3 months"

**3. Learn From Each Phase**
- Capture lessons learned at every gate review
- Update design based on test results, don't ignore data
- Known issues from EVT must be addressed in DVT

**4. Communicate Phase Transitions**
- Gate reviews should involve all stakeholders
- Everyone should understand what changed and what's next
- Celebrate phase completions - they're major milestones

---

### Phase Overlap and Parallelization

**What Can Overlap**:
- ✅ Tooling design can start during DVT testing (but don't order until design freeze)
- ✅ Certifications can start during PVT (if DVT design is frozen)
- ✅ Firmware development can continue through all phases
- ✅ Component procurement can happen in parallel with testing

**What Cannot Overlap**:
- ❌ Don't order hard tooling before DVT design freeze
- ❌ Don't start PVT until DVT testing is 100% complete
- ❌ Don't launch without certifications complete
- ❌ Don't skip pilot build and go straight to volume

---

### Decision-Making Framework

**At Each Gate Review, Ask**:

**1. Technical Completeness**:
- Did we achieve all objectives for this phase?
- Are there any open issues that would cause problems in the next phase?
- Is the design ready for the increased investment of the next phase?

**2. Risk Assessment**:
- What new risks were discovered in this phase?
- Were high-risk areas adequately tested?
- Are there any show-stoppers that would prevent success?

**3. Business Viability**:
- Is the business case still valid (cost, schedule, market)?
- Do we have the resources to proceed to the next phase?
- Are stakeholders still committed to the project?

**4. Go/No-Go Options**:
- **GO**: Proceed to next phase (all criteria met)
- **CONDITIONAL GO**: Proceed with specific action items to address (minor issues)
- **NO-GO / REDO**: Repeat phase with design changes (major issues found)
- **CANCEL**: Terminate project (fundamental flaws or business case no longer valid)

---

## Common Pitfalls by Phase

### Cross-Phase Pitfalls

**❌ Pitfall: "We're behind schedule, let's skip testing"**
- **Impact**: Undiscovered issues become 10x more expensive in next phase
- **Solution**: Compress schedule by parallelizing, not cutting corners

**❌ Pitfall: "That issue is low priority, we'll fix it later"**
- **Impact**: Small issues compound, resurface as major problems
- **Solution**: Fix all known issues before advancing, or explicitly accept risk

**❌ Pitfall: "We don't need a phase gate review, we're confident"**
- **Impact**: Misalignment, missed issues, no stakeholder buy-in
- **Solution**: Formal gate reviews catch issues and ensure alignment

**❌ Pitfall: "Let's save money by using the same prototypes for multiple phases"**
- **Impact**: Design not validated with production-intent materials/process
- **Solution**: Each phase needs prototypes built with appropriate methods for that phase

---

## Decision Framework

### Phase Advancement Decision Tree

```
Phase N Complete?
│
├─ YES → All objectives met?
│         │
│         ├─ YES → All testing passed?
│         │        │
│         │        ├─ YES → Budget & timeline on track?
│         │        │        │
│         │        │        ├─ YES → GO to Phase N+1
│         │        │        └─ NO → Escalate to sponsor
│         │        │
│         │        └─ NO → What failed?
│         │               │
│         │               ├─ Minor issue → Conditional GO (with action items)
│         │               └─ Major issue → NO-GO (repeat phase)
│         │
│         └─ NO → What's missing?
│                  │
│                  ├─ On critical path → NO-GO (repeat phase)
│                  └─ Not critical → Conditional GO (defer to next phase)
│
└─ NO → Why not?
          │
          ├─ Need more time → Extend phase (add 2-4 weeks)
          ├─ Need design changes → NO-GO (repeat phase)
          ├─ Fundamental flaw → CANCEL (terminate project)
          └─ Business case changed → REASSESS (sponsor decision)
```

---

## Conclusion

**Phase gates are not bureaucracy - they're risk mitigation.**

The cost to fix a design issue increases **10x with each phase**:
- Fix in Concept: $1K (change on paper)
- Fix in EVT: $10K (prototype rebuild)
- Fix in DVT: $100K (tooling delay + prototype rebuild)
- Fix in PVT: $1M (tooling rework + pilot scrap + schedule slip)
- Fix in MP: $10M+ (recall, warranty claims, brand damage)

**Invest time in each phase to get it right.** The phase gate process exists to prevent expensive mistakes from propagating forward.

---

## Related Resources

- [Phase Gate Checklist](../templates/03-phase-gate-checklist.md) - Detailed gate criteria and checklists
- [Project Charter Template](../templates/01-project-charter.md) - Concept phase planning
- [Risk Register](../templates/02-risk-register.md) - Track phase-specific risks
- [Lessons Learned Template](../templates/05-lessons-learned.md) - Capture insights at each phase
- [Getting Started Guide](01-getting-started.md) - Hardware PM fundamentals

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit  
**Repository**: https://github.com/kathegrima/hardware-pm-starter-kit

---

*"Phase gates slow you down to speed you up - they prevent expensive mistakes."*
