# Risk Management Guide for Hardware Projects

> **Identify, assess, and mitigate risks before they become crises**

---

## Table of Contents

1. [Introduction to Hardware Risk Management](#introduction-to-hardware-risk-management)
2. [Hardware-Specific Risk Categories](#hardware-specific-risk-categories)
3. [Risk Assessment Framework](#risk-assessment-framework)
4. [Risk Mitigation Strategies](#risk-mitigation-strategies)
5. [Phase-Specific Risk Management](#phase-specific-risk-management)
6. [Common Hardware Risks & Mitigation](#common-hardware-risks--mitigation)
7. [Risk Monitoring & Tracking](#risk-monitoring--tracking)
8. [Crisis Management](#crisis-management)
9. [Risk Communication](#risk-communication)
10. [Tools & Templates](#tools--templates)

---

## Introduction to Hardware Risk Management

### Why Hardware Risk Management Is Critical

Hardware projects have **unique risk characteristics** compared to software:

**Irreversibility**: 
- Can't "patch" hardware after manufacturing
- Design flaws become permanent in shipped products
- Recalls cost millions and destroy brand reputation

**Long Lead Times**:
- Component procurement: 8-20 weeks
- Tooling: 10-16 weeks
- Certifications: 3-6 months
- One delay cascades through entire project

**High Fixed Costs**:
- Tooling investment: $50K-$500K
- Certification testing: $30K-$100K
- Inventory carrying costs: 20-30% annually
- Failed decisions are expensive to reverse

**Supply Chain Complexity**:
- 100+ components from 20+ suppliers
- Single component shortage can halt production
- Geopolitical and economic disruptions

**Regulatory Requirements**:
- CE, FCC, FDA approvals required before sales
- Compliance failures delay launch 3-6 months
- Non-compliance can result in fines or market bans

---

### Risk vs Issue

**Risk** = Something that *might* happen in the future
- Probability: 0-100% likelihood
- Impact: If it occurs, what's the damage?
- **Action**: Mitigation to prevent or reduce

**Issue** = Something that *has already* happened
- Probability: 100% (it's real)
- Impact: Damage is occurring or imminent
- **Action**: Resolution to fix or contain

**Example**:
- **Risk**: "Component X might go end-of-life" (50% probability, high impact)
- **Issue**: "Component X EOL announced, last order date in 6 weeks" (100% probability, high impact)

---

### Risk Management Process

```
┌─────────────────────────────────────────────────────────┐
│                    CONTINUOUS CYCLE                      │
│                                                          │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐         │
│  │ IDENTIFY │───▶│  ASSESS  │───▶│ MITIGATE │         │
│  │  Risks   │    │ Impact & │    │ Strategy │         │
│  └──────────┘    │Likelihood│    └──────────┘         │
│       ▲          └──────────┘         │                │
│       │                               │                │
│       │          ┌──────────┐         ▼                │
│       └──────────│ MONITOR  │◀────────┘                │
│                  │  Track   │                          │
│                  └──────────┘                          │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

**1. Identify**: Brainstorm all potential risks (team workshops, lessons learned)
**2. Assess**: Score each risk (likelihood × impact = priority score)
**3. Mitigate**: Develop strategies (avoid, reduce, transfer, accept)
**4. Monitor**: Track risks weekly, update scores as project evolves

---

## Hardware-Specific Risk Categories

### 1. Technical Risks

**Design Risks**:
- Electrical: Power integrity, signal integrity, EMI/EMC
- Mechanical: Fit, tolerance stack-up, thermal management
- Firmware: Real-time performance, memory constraints, power consumption
- Integration: Hardware-firmware-software interfaces misaligned

**Performance Risks**:
- Battery life below target (e.g., 4 months vs 6 months)
- Sensor accuracy outside spec (±5% vs ±3%)
- Processing speed insufficient for requirements
- Thermal failure at max ambient temperature

**Reliability Risks**:
- MTBF below target (20,000 hours vs 50,000 hours)
- Component wear-out (buttons, connectors, batteries)
- Environmental sensitivity (humidity, vibration, shock)
- Accelerated aging in field conditions

---

### 2. Supply Chain Risks

**Component Availability**:
- **EOL (End of Life)**: Manufacturer discontinues component
- **NRND (Not Recommended for New Designs)**: EOL warning
- **Allocation**: Supplier limits quantities to certain customers
- **Lead Time Extension**: Component lead times remain volatile post-pandemic
  - Standard passives: 4-12 weeks (vs pre-2020: 2-4 weeks)
  - ICs/MCUs: 16-52 weeks (vs pre-2020: 8-16 weeks)
  - Custom components: 16-24 weeks (vs pre-2020: 8-12 weeks)
- **Single Source**: Only one supplier for critical component
- **Allocation Risk**: Semiconductor manufacturers prioritize high-volume customers (automotive, industrial)
- **Mitigation**: Order long-lead components at EVT phase, maintain 6-12 month inventory buffer

**Supplier Risks**:
- Supplier capacity constraints (can't meet volume)
- Supplier quality issues (high defect rate)
- Supplier financial instability (bankruptcy risk)
- Geopolitical disruption (trade wars, export controls)

**Logistics Risks**:
- Shipping delays (port congestion, customs holds)
- Inventory damage (mishandling, environmental)
- Tariffs and duties (unexpected cost increases)

---

### 3. Manufacturing Risks

**Yield Risks**:
- First-pass yield below target (<90% when target is >95%)
- Defect rate higher than expected
- Rework time excessive (unit economics broken)
- Cosmetic quality issues (scratches, color mismatch)

**Process Risks**:
- Assembly time longer than planned (cycle time 2x target)
- Test coverage insufficient (escapes to customers)
- Calibration complexity (adds cost/time per unit)
- Operator training inadequate (high error rate)

**Tooling Risks**:
- Tooling cost overrun (quoted $100K, actual $200K)
- Tooling delay (10 weeks becomes 16 weeks)
- Tooling quality issues (flash, sink marks, dimensional errors)
- Tool life shorter than expected (needs replacement sooner)

---

### 4. Compliance & Regulatory Risks

**Certification Risks**:
- **FCC/CE failure**: EMI/EMC exceeds limits (redesign + retest)
- **Safety failure**: UL/IEC testing reveals hazards
- **RoHS/REACH violation**: Component contains restricted substance
- **Medical device**: FDA 510(k) or MDR approval delayed

**Regulatory Changes**:
- New regulation introduced during development
- Interpretation of existing regulation changes
- Country-specific requirements discovered late

**Documentation Risks**:
- Technical file incomplete (CE marking blocked)
- Test reports not accepted by notified body
- Label requirements not met (product seized at customs)

---

### 5. Business & Market Risks

**Market Risks**:
- Competitor launches similar product first (market advantage lost)
- Market demand lower than forecast (inventory write-off)
- Price sensitivity higher than expected (margin pressure)
- Customer requirements change mid-project (scope creep)

**Financial Risks**:
- BOM cost exceeds target (product unprofitable)
- Budget overrun (need additional funding)
- Currency fluctuation (€/$ exchange rate impact)
- Volume discount not achieved (lower margin)

**Timeline Risks**:
- Miss launch window (holiday season, trade show)
- Competitor forces early launch (unfinished product)
- Delays cascade (component → tooling → certification → launch)

---

### 6. Project Management Risks

**Team Risks**:
- Key person leaves mid-project (knowledge loss)
- Team skill gaps (no EMC expert on team)
- Resource contention (team shared across projects)
- Communication breakdowns (HW/FW misalignment)

**Scope Risks**:
- Scope creep (features added mid-development)
- Unclear requirements (ambiguous PRD)
- Stakeholder misalignment (conflicting priorities)
- Technical debt accumulation (shortcuts taken)

---

## Risk Assessment Framework

### Likelihood Scale (1-5)

| Score | Level | Probability | Description |
|-------|-------|-------------|-------------|
| **5** | Almost Certain | 70-100% | Expected to occur, strong evidence |
| **4** | Likely | 50-70% | Will probably occur, precedent exists |
| **3** | Possible | 30-50% | Might occur, some indicators present |
| **2** | Unlikely | 10-30% | Probably won't occur, low indicators |
| **1** | Rare | 0-10% | Highly unlikely, theoretical only |

**Examples**:
- **5 (Almost Certain)**: "Component with 52-week lead time will cause delay" (if not ordered early)
- **3 (Possible)**: "EMI testing might fail on first attempt" (no pre-testing done)
- **1 (Rare)**: "Earthquake destroys CM facility" (specific geography, low seismic activity)

---

### Impact Scale (1-5)

| Score | Level | Project Impact | Examples |
|-------|-------|---------------|----------|
| **5** | Critical | >3 month delay, >50% budget overrun, project cancellation, safety hazard, product recall | Complete redesign, tooling rework, certification failure |
| **4** | High | 1-3 month delay, 30-50% budget overrun, major feature cut, compliance failure | Component EOL forces redesign, thermal failure at DVT |
| **3** | Medium | 2-4 week delay, 15-30% budget overrun, performance degraded, workaround needed | Test fixture not ready for PVT, yield at 90% vs 95% |
| **2** | Low | <2 week delay, <15% budget impact, minor inconvenience, cosmetic issues | Component price increase, supplier delivers late by 3 days |
| **1** | Minimal | Negligible impact, absorbed within contingency buffer | Documentation update needed, minor BOM change |

---

### Risk Priority Score

**Formula**: `Risk Score = Likelihood (1-5) × Impact (1-5)`

**Result Range**: 1-25

| Score Range | Priority | Action Required |
|-------------|----------|-----------------|
| **20-25** | **CRITICAL** | Immediate action, weekly review, executive escalation |
| **15-19** | **HIGH** | Active mitigation in progress, bi-weekly review |
| **10-14** | **MEDIUM** | Mitigation planned, monthly review |
| **5-9** | **LOW** | Monitor, accept risk or defer mitigation |
| **1-4** | **MINIMAL** | Accept, no action needed |

**Example Calculation**:
- Risk: "Component EOL announced mid-project"
- Likelihood: 3 (Possible - happens regularly in industry)
- Impact: 5 (Critical - forces redesign, 3+ month delay)
- **Risk Score: 3 × 5 = 15 (HIGH priority)**

---

### Risk Matrix Visual

```
IMPACT
  5│ 5   10  15  20  25
   │
  4│ 4    8  12  16  20
   │
  3│ 3    6   9  12  15
   │
  2│ 2    4   6   8  10
   │
  1│ 1    2   3   4   5
   └─────────────────────
     1   2   3   4   5
         LIKELIHOOD

Legend:
■ 20-25 = CRITICAL (Red)
■ 15-19 = HIGH (Orange)
■ 10-14 = MEDIUM (Yellow)
■ 5-9  = LOW (Green)
■ 1-4  = MINIMAL (Blue)
```

---

## Risk Mitigation Strategies

### Four Risk Response Strategies

**1. AVOID** - Eliminate the risk entirely
- **When to use**: Risk is unacceptable, alternative exists
- **Example**: Don't use single-source component → select dual-source alternative
- **Cost**: Medium (design decision early)

**2. REDUCE** - Lower probability or impact
- **When to use**: Can't eliminate but can minimize
- **Example**: Pre-compliance EMI testing at EVT → reduces certification failure risk
- **Cost**: Low to Medium (incremental investment)

**3. TRANSFER** - Shift risk to another party
- **When to use**: Risk better managed by specialist
- **Example**: Purchase component shortage insurance, supplier warranties
- **Cost**: Low to Medium (insurance premium, contract terms)

**4. ACCEPT** - Acknowledge risk, monitor, no action
- **When to use**: Low priority risk, mitigation cost > impact
- **Example**: Minor cosmetic defect with 1% occurrence, low customer impact
- **Cost**: Zero upfront (may incur cost if risk materializes)

---

### Mitigation Strategy Selection

| Risk Score | Recommended Strategy | Rationale |
|------------|---------------------|-----------|
| **20-25 (Critical)** | AVOID or REDUCE aggressively | Unacceptable risk, must address |
| **15-19 (High)** | REDUCE or TRANSFER | Significant risk, active mitigation needed |
| **10-14 (Medium)** | REDUCE or ACCEPT with contingency | Manageable risk, balance cost vs benefit |
| **5-9 (Low)** | ACCEPT or REDUCE (low-cost only) | Minor risk, monitor only |
| **1-4 (Minimal)** | ACCEPT | Negligible risk, no action |

---

### Example Mitigation Strategies by Risk Type

**Component EOL Risk** (Score: 15-20):
- **Avoid**: Select components with long lifecycle (automotive-grade, industrial-grade)
- **Reduce**: Qualify second source early, design for pin compatibility
- **Transfer**: Supplier agreement for minimum availability period
- **Accept**: Low-risk component, easy to redesign (passive components)

**Thermal Failure Risk** (Score: 15-20):
- **Avoid**: Overdesign thermal solution (heatsinks, fans, thermal paste)
- **Reduce**: CFD thermal simulation at Concept phase, test at max ambient early
- **Transfer**: Component warranty for thermal failures
- **Accept**: Not applicable (critical risk)

**Certification Failure Risk** (Score: 15-20):
- **Avoid**: Pre-compliance testing at EVT, experienced EMC consultant
- **Reduce**: Design margin (3-6dB below limits), shielding, filtering
- **Transfer**: Test lab consultation during design phase
- **Accept**: Not applicable (regulatory requirement)

**Manufacturing Yield Risk** (Score: 12-16):
- **Avoid**: DFM review at DVT, simplify assembly
- **Reduce**: Pilot build at PVT (500-2000 units), process optimization
- **Transfer**: CM assumes yield risk (contract terms)
- **Accept**: Low-volume product, rework is acceptable

---

## Phase-Specific Risk Management

### Concept Phase Risks

**Top 3 Risks**:
1. **Technical feasibility unproven** (Score: 20)
   - Mitigation: Proof-of-concept prototype, technology demo
2. **Market demand uncertain** (Score: 15)
   - Mitigation: Customer interviews (20+ target users), market research
3. **Regulatory requirements unclear** (Score: 12)
   - Mitigation: Engage compliance consultant, preliminary assessment

**Risk Activities**:
- Brainstorm session: Identify 20+ potential risks
- Create initial risk register (top 10 risks prioritized)
- Assign risk owners for each high-priority risk
- Develop mitigation strategies for critical risks

---

### EVT Phase Risks

**Top 5 Risks**:
1. **Thermal management insufficient** (Score: 20)
   - Mitigation: Thermal simulation, IR camera testing, max ambient testing
2. **Component long lead time** (Score: 16)
   - Mitigation: Order long-lead items immediately, qualify alternates
3. **Hardware-firmware integration failure** (Score: 15)
   - Mitigation: Daily HW-FW standups, integration testing early
4. **Power consumption exceeds target** (Score: 12)
   - Mitigation: Subsystem power profiling, low-power firmware optimization
5. **Schedule slip** (Score: 12)
   - Mitigation: Weekly tracking, buffer in schedule, parallel activities

**Risk Activities**:
- Update risk register weekly (score changes as data emerges)
- Retire risks as testing validates design choices
- Escalate new critical risks immediately to sponsor
- Review risk register at EVT gate review

---

### DVT Phase Risks

**Top 5 Risks**:
1. **EMI/EMC certification failure** (Score: 20)
   - Mitigation: Pre-compliance testing, EMC consultant, design margin
2. **Environmental testing failure** (Score: 16)
   - Mitigation: Test at temperature extremes early, HALT testing
3. **BOM cost above target** (Score: 15)
   - Mitigation: Value engineering, alternate component quotes, volume discounts
4. **Tooling cost overrun** (Score: 12)
   - Mitigation: 3 vendor quotes, phased tooling, simplify mechanical design
5. **Design freeze delayed** (Score: 12)
   - Mitigation: Freeze criteria defined, stakeholder alignment, no scope creep

**Risk Activities**:
- All high-priority risks must have active mitigation by DVT
- No new critical risks should emerge (if so, major red flag)
- Pre-compliance testing retires EMI/EMC risk
- DFM review retires manufacturing risk

---

### PVT Phase Risks

**Top 5 Risks**:
1. **Manufacturing yield below target** (Score: 20)
   - Mitigation: Pilot build 500+ units, root cause analysis on defects
2. **Certification delays** (Score: 16)
   - Mitigation: Start certifications in DVT, expedited testing, lab relationship
3. **Component shortage** (Score: 15)
   - Mitigation: 3-6 month inventory buffer, daily supplier communication
4. **Supplier quality issues** (Score: 12)
   - Mitigation: Incoming inspection, supplier audits, dual-source
5. **Launch readiness gaps** (Score: 10)
   - Mitigation: Launch checklist, cross-functional reviews, packaging testing

**Risk Activities**:
- Yield issues become top priority (can't launch at 85% yield)
- Certification delays escalate immediately (on critical path)
- Supply chain risks monitored daily (component availability)
- No new design risks should appear (design frozen)

---

## Common Hardware Risks & Mitigation

### 1. Component End-of-Life (EOL)

**Risk Description**: Critical component discontinued by manufacturer mid-project

**Likelihood**: Medium to High (electronics industry churn rate ~10-15% annually)

**Impact**: Critical (redesign required, 2-6 month delay, tooling rework if mechanical impact)

**Mitigation Strategies**:
- **Avoid**: Select components with long lifecycle status (Active, not NRND)
- **Avoid**: Use automotive-grade or industrial-grade components (10+ year lifecycle)
- **Reduce**: Qualify second source during EVT phase
- **Reduce**: Design for pin compatibility (easy swap to alternate)
- **Reduce**: Subscribe to component lifecycle alerts (vendor notifications)
- **Transfer**: Supplier agreement for minimum availability period
- **Accept**: Low-risk component (resistors, capacitors) - easy to redesign

**Early Warning Signs**:
- Component marked "NRND" (Not Recommended for New Designs)
- Manufacturer website shows "Limited Availability"
- Lead times suddenly extend (e.g., 8 weeks → 20 weeks)
- Price increases significantly (supply/demand imbalance)

**Contingency Plan**:
- Maintain alternate component list (updated quarterly)
- Lifetime buy if EOL announced (calculate 3-5 year volume)
- Emergency redesign budget ($20K-$50K)

---

### 2. Thermal Management Failure

**Risk Description**: Components exceed max temperature at ambient operating conditions

**Likelihood**: Medium (30-40% of projects encounter thermal issues)

**Impact**: High to Critical (DVT delay 4-8 weeks, mechanical redesign, performance degradation)

**Mitigation Strategies**:
- **Avoid**: Overdesign thermal solution (heatsinks, thermal pads, fans)
- **Avoid**: Derate components (operate at 70-80% of max power)
- **Reduce**: CFD thermal simulation at Concept phase (identify hot spots)
- **Reduce**: IR camera thermal imaging at EVT (measure actual temps)
- **Reduce**: Test at max ambient early (e.g., 40°C or 50°C chamber)
- **Reduce**: Thermal relief in PCB layout (vias, copper pours)

**Early Warning Signs**:
- Components feel hot to touch during EVT testing
- Thermal simulation shows temps >85°C at 25°C ambient
- Performance degrades after extended operation (thermal throttling)

**Contingency Plan**:
- Budget 2 weeks for thermal redesign in DVT schedule
- Have mechanical engineer on standby for heatsink design
- Identify components that can be swapped for lower-power variants

---

### 3. EMI/EMC Certification Failure

**Risk Description**: Product exceeds FCC/CE emissions limits at certification testing

**Likelihood**: High (50-60% of projects fail on first attempt without pre-testing)

**Impact**: High (3-6 month delay, $50K-$100K in retesting, potential redesign)

**Mitigation Strategies**:
- **Avoid**: Pre-compliance testing at EVT phase ($5K-$10K investment)
- **Avoid**: Hire EMC consultant for design review ($5K-$15K)
- **Reduce**: Design margin (target 6dB below limits, gives redesign headroom)
- **Reduce**: Shielding, filtering, grounding best practices
- **Reduce**: PCB layout for low EMI (trace routing, ground planes)
- **Transfer**: Test lab consultation package (pre-test + cert bundle)

**Early Warning Signs**:
- Near-field probe shows hotspots (high emissions from specific circuits)
- Pre-compliance test shows <3dB margin to limits
- Similar products in market have known EMI issues

**Contingency Plan**:
- Budget $30K for retesting and mitigation (shielding cans, ferrites)
- Schedule buffer of 8 weeks for EMI fixes in DVT timeline
- Have backup design with shielding can (add if needed)

---

### 4. Battery Life Below Target

**Risk Description**: Product achieves 4 months battery life vs 6 months target

**Likelihood**: High (power consumption difficult to estimate accurately)

**Impact**: Medium to High (competitive disadvantage, customer dissatisfaction, feature cuts)

**Mitigation Strategies**:
- **Avoid**: Oversize battery capacity (2000mAh vs 1500mAh, +20% margin)
- **Reduce**: Subsystem power profiling at EVT (measure each module)
- **Reduce**: Firmware low-power optimization (sleep modes, duty cycling)
- **Reduce**: Select ultra-low-power components (MCU, sensors, radios)
- **Accept**: Adjust marketing claims (4 months is still acceptable)

**Early Warning Signs**:
- EVT power measurements 50% higher than estimates
- Firmware busy loops consuming power unnecessarily
- Sensors sampling more frequently than needed

**Contingency Plan**:
- Backup battery option (larger capacity, slightly bigger enclosure)
- Feature scaling (reduce sampling frequency, lower radio duty cycle)
- User-selectable power modes (performance vs battery life)

---

### 5. Manufacturing Yield Below Target

**Risk Description**: First-pass yield at PVT is 85% vs 95% target

**Likelihood**: Medium (common if DFM not done properly)

**Impact**: High (unit economics broken, margin destroyed, launch delay)

**Mitigation Strategies**:
- **Avoid**: DFM review at DVT with CM engineer
- **Avoid**: Simplify assembly (fewer parts, no manual soldering)
- **Reduce**: Pilot build at PVT (500-2000 units) to identify issues
- **Reduce**: Poka-yoke fixtures (prevent wrong assembly)
- **Reduce**: Operator training and work instructions
- **Transfer**: CM assumes yield risk (contract negotiation)

**Early Warning Signs**:
- DVT build has assembly issues (difficult to assemble by hand)
- High component count (>200 parts = complexity risk)
- Tight tolerances without inspection (QC gaps)

**Contingency Plan**:
- Budget 4 weeks for yield ramp-up in PVT timeline
- Root cause analysis on every defect (Pareto chart)
- Process changes (assembly sequence, tooling, inspection)

---

### 6. Schedule Slip

**Risk Description**: Project delayed by 2-6 months due to cascading issues

**Likelihood**: High (80% of hardware projects slip schedule)

**Impact**: Medium to High (miss market window, competitor advantage, cost overrun)

**Mitigation Strategies**:
- **Avoid**: Realistic schedule from start (don't lowball to get approval)
- **Reduce**: Add 20-30% buffer to hardware project timelines
- **Reduce**: Parallel activities where possible (tooling design during DVT testing)
- **Reduce**: Weekly tracking of critical path items
- **Reduce**: Order long-lead items early (don't wait for phase gate)

**Early Warning Signs**:
- Phase taking longer than planned (EVT 16 weeks vs 12 planned)
- Critical path items falling behind (component late, tooling delayed)
- Team working overtime consistently (burnout risk)

**Contingency Plan**:
- Compress non-critical activities (defer nice-to-have testing)
- Add resources (contractors, overtime, parallel teams)
- Negotiate launch date flexibility with stakeholders

---

## Risk Monitoring & Tracking

### Risk Register Maintenance

**Update Frequency**:
- **Weekly**: Update risk scores during team meeting (all active risks)
- **Bi-weekly**: Review with stakeholders (top 5 risks)
- **Monthly**: Deep dive on critical risks with sponsor
- **Phase Gates**: Complete risk register review and sign-off

**What to Update**:
- Risk score (likelihood and impact may change as project progresses)
- Mitigation status (not started, in progress, complete, ineffective)
- Risk owner (person responsible for mitigation)
- Notes (new information, test results, decisions made)

---

### Risk Escalation Triggers

**Escalate to PM immediately**:
- New critical risk discovered (score 20-25)
- Existing risk score increases to critical level
- Mitigation strategy failing (risk materializing)

**Escalate to Sponsor within 24 hours**:
- Critical risk with no effective mitigation
- Multiple high-priority risks threatening project success
- Risk impacts schedule by >1 month or budget by >10%

**Escalate to Executive Leadership**:
- Risk threatens project cancellation
- Safety or regulatory risk with legal implications
- Requires strategic decision (pivot, delay launch, cut scope)

---

### Risk Metrics

**Track these metrics monthly**:

| Metric | Definition | Target |
|--------|-----------|--------|
| **Total Risks** | Number of risks in register | Decrease over time (risks retired) |
| **Critical Risks** | Score 20-25 | Zero by DVT gate |
| **High Risks** | Score 15-19 | <3 at any time |
| **Risks Retired** | Risks mitigated and closed | Increasing trend |
| **New Risks** | Risks discovered this period | Decreasing trend (fewer surprises) |
| **Mitigation Completion** | % of mitigations on track | >90% |

**Health Indicators**:
- ✅ **Healthy**: Critical risks = 0, high risks <3, mitigation completion >90%
- ⚠️ **At Risk**: Critical risks 1-2, high risks 3-5, mitigation completion 70-90%
- ❌ **Unhealthy**: Critical risks >2, high risks >5, mitigation completion <70%

---

## Crisis Management

### When a Risk Becomes a Crisis

**Crisis Definition**: A high-impact event that requires immediate action to prevent project failure

**Examples**:
- Component EOL announced, last order date in 4 weeks
- Certification test fails with 10dB margin (major redesign needed)
- Manufacturing yield at 70% (far below 95% target)
- Key engineer quits mid-project (knowledge loss)

---

### Crisis Response Process

**Step 1: Assess (First 24 hours)**
- Gather facts: What happened? What's the impact?
- Identify root cause: Why did this happen?
- Estimate damage: Cost, schedule, scope impact?

**Step 2: Contain (First 48 hours)**
- Stop the bleeding: Prevent further damage
- Preserve options: Don't make hasty decisions
- Communicate: Inform stakeholders, no surprises

**Step 3: Plan (Days 3-7)**
- Develop options: Multiple paths forward (A, B, C)
- Evaluate trade-offs: Cost vs schedule vs scope
- Get expert input: Consult specialists
- Make decision: Choose path forward with sponsor approval

**Step 4: Execute (Ongoing)**
- Implement solution: Execute chosen path
- Monitor closely: Daily tracking, rapid iteration
- Communicate progress: Weekly updates to stakeholders
- Document lessons: Capture for future projects

---

### Crisis Communication

**Who to Inform**:
- **Immediate**: Project team, PM, direct manager
- **Within 24h**: Project sponsor, key stakeholders
- **Within 48h**: Executive leadership (if project-threatening)
- **As needed**: Customers, suppliers, partners (if external impact)

**What to Communicate**:
1. **Situation**: What happened? (facts only, no speculation)
2. **Impact**: How does this affect timeline, budget, scope?
3. **Options**: What are possible paths forward?
4. **Recommendation**: What do you recommend and why?
5. **Decision needed**: What decision do you need and by when?
6. **Next steps**: What actions are being taken now?

**Communication Template**:
```
Subject: URGENT - [Risk Name] Has Materialized

Situation:
[What happened - facts only]

Impact:
- Schedule: [e.g., 6-week delay to DVT gate]
- Budget: [e.g., $50K additional spend for redesign]
- Scope: [e.g., Feature X must be cut]

Options:
A) [Option 1 - pros/cons]
B) [Option 2 - pros/cons]
C) [Option 3 - pros/cons]

Recommendation: [Which option and why]

Decision Needed: [What decision and by when]

Next Steps: [Actions being taken now]
```

---

## Risk Communication

### Stakeholder Risk Reporting

**Weekly Team Update**:
- Top 3 risks (brief status)
- Any new high-priority risks
- Risks retired this week

**Monthly Stakeholder Review**:
- Risk register summary (total risks, top 5 by score)
- Risk trends (increasing or decreasing)
- Mitigation progress (on track or behind)
- Decisions needed from stakeholders

**Phase Gate Review**:
- Complete risk register review
- All critical risks retired or have mitigation plans
- Risk assessment for next phase
- Go/No-Go decision includes risk analysis

---

### Risk Reporting Dashboard

**Key Metrics to Display**:
- Risk score distribution (histogram: how many risks at each score level)
- Top 5 risks (ranked by score, with mitigation status)
- Risk trend over time (are risks increasing or decreasing?)
- Mitigation completion rate (% of mitigations on track)

**Traffic Light System**:
- 🟢 **Green**: All risks under control, no action needed
- 🟡 **Yellow**: 1-2 high risks, mitigation in progress
- 🔴 **Red**: Critical risks present or mitigation failing

---

## Tools & Templates

### Risk Register Template

Use the [Risk Register Template](../templates/02-risk-register.md) to track all project risks.

**Key Fields**:
- Risk ID (unique identifier)
- Risk description (clear, specific)
- Category (technical, supply chain, manufacturing, etc.)
- Likelihood (1-5)
- Impact (1-5)
- Risk score (likelihood × impact)
- Mitigation strategy (avoid, reduce, transfer, accept)
- Mitigation actions (specific steps)
- Owner (person responsible)
- Status (not started, in progress, complete)
- Target date (when mitigation will be complete)

---

### Risk Identification Techniques

**1. Brainstorming Session** (Concept phase)
- Gather team (HW, FW, ME, PM, supply chain, quality)
- Timebox: 60 minutes
- No judgment: All ideas captured
- Target: 20+ potential risks identified

**2. Lessons Learned Review** (All phases)
- Review past project retrospectives
- What went wrong? Can it happen again?
- Import risks from similar projects

**3. Expert Consultation** (Concept & EVT)
- Compliance expert: Regulatory risks
- Manufacturing engineer: Yield risks
- Supply chain: Component availability risks

**4. Pre-Mortem Exercise** (DVT phase)
- "Assume project failed. Why?"
- Team writes failure reasons on sticky notes
- Group and prioritize failure modes
- Convert to risks to mitigate

---

### Risk Management Best Practices

**1. Start Early**
- Create risk register in Concept phase
- Don't wait until problems occur

**2. Be Specific**
- ❌ Bad: "Component issues"
- ✅ Good: "MCU X123 has 20-week lead time, may cause EVT delay"

**3. Quantify Impact**
- ❌ Bad: "This will delay the project"
- ✅ Good: "This will delay DVT gate by 4-6 weeks"

**4. Assign Ownership**
- Every risk has an owner (not PM for everything)
- Owner is accountable for mitigation execution

**5. Update Regularly**
- Weekly updates during team meetings
- Don't let risk register get stale

**6. Retire Risks**
- When risk is mitigated, mark it complete
- Don't let register grow indefinitely

**7. Learn From Mistakes**
- Capture lessons learned when risks materialize
- Share with other teams to prevent recurrence

---

## Conclusion

**Risk management is not pessimism - it's preparedness.**

Hardware projects have inherent risks due to:
- Long lead times (changes take months to implement)
- High fixed costs (expensive to reverse decisions)
- Supply chain complexity (100+ components, 20+ suppliers)
- Regulatory requirements (certifications required before sales)

**The cost to fix issues increases 10x with each phase**:
- Fix in Concept: €1K
- Fix in EVT: €10K
- Fix in DVT: €100K
- Fix in PVT: €1M
- Fix in MP: €10M+

**Effective risk management**:
- Identifies risks early (when mitigation is cheap)
- Prioritizes risks by score (likelihood × impact)
- Implements mitigation strategies (avoid, reduce, transfer, accept)
- Monitors continuously (weekly updates, monthly reviews)

**Key Principle**: "Hope is not a strategy. Plan for risks, don't react to crises."

---

## Related Resources

- [Risk Register Template](../templates/02-risk-register.md) - Track and manage risks
- [Phase Gate Checklist](../templates/03-phase-gate-checklist.md) - Gate criteria includes risk assessment
- [Phase Gate Deep Dive](03-phase-gate-guide.md) - Phase-specific risks
- [Project Charter Template](../templates/01-project-charter.md) - Initial risk identification
- [Lessons Learned Template](../templates/05-lessons-learned.md) - Capture risk management lessons

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit  
**Repository**: https://github.com/kathegrima/hardware-pm-starter-kit

---

*"In hardware, risk management is the difference between a successful launch and a project post-mortem."*
