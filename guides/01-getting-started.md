# Hardware Project Management - Getting Started Guide

> **Your comprehensive introduction to managing hardware development projects from concept to mass production**

---

## Table of Contents

1. [Introduction](#introduction)
2. [What Makes Hardware PM Different?](#what-makes-hardware-pm-different)
3. [The Hardware Development Lifecycle](#the-hardware-development-lifecycle)
4. [Critical Hardware PM Concepts](#critical-hardware-pm-concepts)
5. [Hardware PM Methodologies](#hardware-pm-methodologies)
6. [Managing Hardware Projects: Best Practices](#managing-hardware-projects-best-practices)
7. [Timeline Expectations by Industry](#timeline-expectations-by-industry)
8. [Common Pitfalls and How to Avoid Them](#common-pitfalls-and-how-to-avoid-them)
9. [Getting Started: Your First Hardware Project](#getting-started-your-first-hardware-project)
10. [Additional Resources](#additional-resources)
11. [Conclusion](#conclusion)

---

## Introduction

Welcome to the **Hardware Project Management Getting Started Guide**. If you're transitioning from software PM, leading your first hardware project, or launching a physical product, this guide will equip you with the foundational knowledge to succeed in the unique world of hardware development.

Hardware project management differs fundamentally from software PM due to the physical nature of products and long lead times. You can't patch hardware after manufacturing, changes are expensive, and every decision has lasting consequences. This guide will help you navigate these challenges.

---

## What Makes Hardware PM Different?

### Key Differences: Hardware vs Software PM

| Aspect | Software PM | Hardware PM |
|--------|-------------|-------------|
| **Iteration Speed** | Days to weeks | Months to quarters |
| **Changes After Release** | Can patch, update, rollback instantly | Cannot modify once manufactured |
| **Marginal Cost** | Near zero for updates | High - tooling, inventory, rework |
| **Timeline** | 2-4 week sprints | 4-8 week sprints |
| **Cost of Error** | Low - easy to step back | High - may require redesign of board/enclosure |
| **Risk Impact** | Bugs, performance issues | Years of warranty claims, recalls |
| **Dependencies** | APIs, libraries, cloud services | Component availability, supplier capacity, lead times |
| **Flexibility** | Highly flexible, iterative | Linear, phased, expensive to change |
| **Product Lifecycle** | Continuous development and updates | Long development (18-36 months), limited by physical wear |

### The Biggest Difference

**In software**, you pay for people's ability to create value and respond quickly to change.

**In hardware**, you pay upfront for materials, tooling, and manufacturing capacity—and once committed, changes are costly.

---

## The Hardware Development Lifecycle

Understanding the **phase-gate process** is critical for hardware PM. Unlike software's continuous deployment, hardware follows a structured, sequential process where each phase must be completed before advancing.

### The Standard Flow

```
Concept → EVT → DVT → PVT → Mass Production → Maintenance → End-of-Life
   ↓       ↓      ↓      ↓          ↓              ↓            ↓
  Idea  Prototype Valid Design  Validate  Volume Mfg    Support   Disposal
                              Production
```

### Phase Descriptions

#### 1. Concept Phase (4-8 weeks)

**Goal**: Validate feasibility and create Product Requirements Document (PRD)

**Key Activities**:
- Market research and competitive analysis
- Technical feasibility study
- Initial Bill of Materials (BOM) estimation
- Risk identification
- Business case validation

**Deliverables**:
- Product Requirements Document (PRD)
- Initial BOM with cost estimates
- Project charter with scope, timeline, budget
- Risk register

**Gate Criteria**:
- PRD approved by stakeholders
- Technical feasibility confirmed
- Business case validated (ROI, market opportunity)
- Funding secured

---

#### 2. EVT - Engineering Validation Test (8-16 weeks)

**Goal**: Prove core functionality works

**What is EVT?**
Engineering Validation Testing is the first major milestone where your prototype is tested against the product's intended functions and performance. It's all about developing "work-like" (and sometimes "work-like, look-alike") prototypes to validate, test, and refine the core functionality.

**Key Activities**:
- PCB testing and debugging
- Firmware validation and bring-up
- Electrical load testing
- Thermal testing
- Component validation
- I/O interface testing
- Multiple iterations to eliminate design flaws

**Prototype Quantities**: 5-50 units (typical: 10-20 units for effective testing across disciplines)

**Technologies Used**: 3D printing, laser cut/milled PCBs, soft tooling (silicon molds), professional hardware development kits (HDK), rapidly cut/milled parts

**Deliverables**:
- Fully functional prototype with key components performing as intended
- Validated schematic and PCB layout
- Initial firmware build
- Test results and analysis
- Updated BOM with confirmed components

**Limitations**: Prototypes may look "somewhat ugly," raw, and lack beautiful cosmetic finish. The EVT prototype can miss some non-key mechanical features such as handles, curves in enclosure, painting, etc.

**Gate Criteria**:
- Core functionality proven
- Major technical risks retired
- Performance meets key specifications
- No critical design flaws identified

**Common Failure Rate**: High failure rates are normal during initial EVT testing (10-50% depending on complexity) - this is expected as you identify and fix issues.

---

#### 3. DVT - Design Validation Test (12-20 weeks)

**Goal**: Validate design meets all specifications

**What is DVT?**
Design Validation Testing serves the need to validate the developed product's design and start implementing DFM (Design for Manufacturability). After completing EVT, you lock in the design of prototypes and enclosures that look like the final product.

**Key Activities**:
- Cosmetic and mechanical validation
- Environmental testing (temperature, humidity, vibration, drop tests)
- EMC/EMI testing (electromagnetic compatibility)
- Reliability testing
- Compliance pre-testing (CE, FCC, RoHS)
- User experience validation
- Packaging design
- DFM (Design for Manufacturability) implementation
- Finalize industrial design

**Prototype Quantities**: 20-200 units

**Purpose of Prototypes**: Certification lab tests, beta tests with early customers/testers

**Technologies Used**: 3D printed gel-coated enclosures with finish as from the factory, rapidly cut/milled parts, industrial equipment (injection molding), 1st generation tooling (quick molds)

**Deliverables**:
- Production-intent design (MVP - Minimum Viable Product)
- Complete BOM with costs and suppliers
- Design documentation package
- Environmental and compliance test reports
- Packaging design completed
- DFX (Design for X) analysis complete
- Manufacturing process plan
- Estimate mass-production yields

**Gate Criteria**:
- Design validated against all specifications
- Compliance testing passed (pre-certification)
- Reliability targets met
- Manufacturing feasibility confirmed
- Ready for tooling investment

**This is the critical "point of no return"**: After DVT, any significant design change requires returning to DVT phase, wasting time and money.

---

#### 4. PVT - Production Validation Test (8-16 weeks)

**Goal**: Validate manufacturing readiness

**What is PVT?**
Production Validation Testing is the last step before officially commencing mass production. Usually 5-10% of the production run is delivered in PVT, aiming to stabilize the quality of the manufacturable product.

**Key Activities**:
- Pilot run (small batch with production tooling)
- Manufacturing process validation
- Quality control metrics validation
- Yield analysis
- Final DFM corrections
- Test benches for PCBA tests designed
- Supply chain validation
- Packaging and logistics validation
- Final cost validation
- All components, materials, packaging, and logistics planned

**Prototype Quantities**: 50-500 units to verify mass-production yields and provide product samples

**Technologies**: Industrial technologies suitable for volume production only, 2nd generation molds for plastic parts

**Deliverables**:
- Pilot build units (also called "Beta" or "Golden Samples")
- Manufacturing process documentation
- Quality control plan and acceptance criteria
- Supply chain agreements
- Final cost breakdown
- Production readiness review

**Limitations**: Only minor changes are allowed at PVT. Any significant design change kicks the project back to DVT. The time required to design and produce custom tools is generally long (3-6 months).

**Gate Criteria**:
- Yield targets met (85-95% typical for pilot run)
- Manufacturing process stable
- Cost targets achieved
- Supply chain validated
- Quality metrics acceptable
- Ready for volume production

---

#### 5. Mass Production (MP) - Ongoing

**Goal**: Volume manufacturing and ongoing support

**Key Activities**:
- Ramp to full production volume
- Continuous quality monitoring
- Field data collection and analysis
- Supplier management
- Inventory management
- Customer support and RMA (Return Merchandise Authorization)
- Running changes (minor improvements)

**Key Metrics**:
- Production yield (target: >95% at volume)
- Defect rate (PPM - parts per million)
- On-time delivery
- Cost per unit vs target
- Customer satisfaction (NPS)
- Warranty claim rate

**Phase Duration**: Months to years, depending on product lifecycle

---

## Critical Hardware PM Concepts

### 1. Design Freeze

**Design Freeze** is a critical milestone where no further design changes are allowed without formal change control. This typically occurs:
- Before DVT phase (for medical devices - regulatory requirement)
- Before PVT phase (for consumer electronics - before tooling investment)
- Before tooling investment (for all hardware - economic imperative)

**Why it matters**: Tooling costs $50K-$150K typical (up to $500K+ for complex multi-cavity molds). Changes after tooling = expensive rework, production delays, and wasted investment.

**What it means in practice**:
- All design decisions finalized
- BOM locked (components confirmed available)
- Manufacturing process defined
- Compliance path clear
- Any change requires Change Control Board (CCB) approval

---

### 2. Tooling

**Tooling** refers to the molds, dies, jigs, and fixtures required for manufacturing.

**Soft Tooling (Prototype)**:
- 3D printed, CNC machined, low-volume
- Flexible - easy to modify
- Cost: $5K-$20K
- Lead time: 1-3 weeks
- Volume: 10-500 units

**Hard Tooling (Production)**:
- Injection molding, stamping dies, high-volume
- Inflexible - very expensive to modify
- Cost: $50K-$150K typical (up to $500K+ for complex multi-cavity molds)
- Lead time: 8-16 weeks
- Volume: 10,000+ units
- Lifetime: 100K-1M+ parts

**Decision point**: Commit to hard tooling only after DVT phase confirms design is production-ready.

---

### 3. Component Obsolescence

Electronic components have **lifecycles**. Manufacturers discontinue components ("End-of-Life" or EOL) regularly, creating risk for hardware products.

**Component Lifecycle Stages**:
1. **Active** - Component in full production, available
2. **NRND** (Not Recommended for New Designs) - Still available but phasing out
3. **EOL Announced** - Discontinuation announced, last-time-buy opportunity
4. **Obsolete** - No longer manufactured, only available from distributors/brokers

**Risk Mitigation Strategies**:
- Choose components with long lifecycle (automotive-grade, industrial-grade preferred)
- Avoid components marked "NRND" during design phase
- Design for second sources (alternate suppliers for critical components)
- Monitor component lifecycle status throughout product lifetime
- Buy "lifetime buy" inventory before EOL (if product lifetime is known)
- Maintain flexibility in design to allow component substitution

**Impact**: If a critical component goes EOL and no alternate exists, you may need to redesign the PCB—a 6-12 month setback.

---

### 4. Supply Chain Lead Times

Hardware PM must account for **long lead times** that are outside your control.

**Typical Lead Times (2026)**:
- **Standard passive components** (resistors, capacitors): 2-8 weeks
- **ICs, microcontrollers**: 16-52 weeks typical (varies by category and supplier)
- **Custom components** (connectors, displays, enclosures): 12-16 weeks
- **PCB fabrication**: 2-4 weeks (standard), 1 week (expedite, 2x cost)
- **PCB assembly**: 1-3 weeks
- **Plastic injection molding**: 8-16 weeks for tooling + 2-4 weeks per batch
- **Certifications**: 
  - CE marking (EMC + LVD + RoHS): 4-8 weeks, €8K-€25K
  - RED (if wireless): additional 4-8 weeks, €15K-€40K
  - Full EU compliance suite: 3-6 months total, €25K-€80K typical
  - Medical devices (MDR): 12-24 months, €100K-€500K+

**Buffer Strategy**: Add 20-30% time buffer for supply chain delays in your project timeline. Always have Plan B suppliers identified.

**Pro Tip**: Start long-lead-time procurement early—order critical ICs during EVT phase if lead times are long.

---

### 5. Bill of Materials (BOM)

The **Bill of Materials (BOM)** is the complete list of components, materials, and parts required to build your product.

**BOM Structure**:
- **Part Number** - Unique identifier (manufacturer PN + internal PN)
- **Description** - What the part is
- **Quantity** - How many per unit
- **Manufacturer** - Who makes it
- **Supplier** - Where to buy it (Digi-Key, Mouser, direct)
- **Unit Cost** - Price per part
- **Extended Cost** - Unit cost × Quantity
- **Lead Time** - How long to get it
- **Lifecycle Status** - Active, NRND, EOL
- **Second Source** - Alternate supplier/manufacturer

**BOM Evolution**:
- **Concept**: Rough estimate, ±50% accuracy
- **EVT**: Component selection, ±30% accuracy
- **DVT**: Locked design, ±10% accuracy
- **PVT**: Final costs, production suppliers, ±5% accuracy
- **MP**: Actual production costs

**BOM Management is Critical**: A single missing component can halt an entire production run. Always maintain accurate, up-to-date BOMs.

---

### 6. Cost Structure in Hardware

Hardware costs are upfront and capital-intensive.

**Development Costs (One-Time)**:
- Engineering design (schematic, PCB layout, firmware)
- Prototyping (EVT, DVT, PVT builds)
- Tooling (injection molds, stamping dies, jigs)
- Certifications (CE, FCC, UL, FDA)
- Testing equipment and fixtures

**Per-Unit Costs (Recurring)**:
- COGS (Cost of Goods Sold): Components + PCB + assembly + enclosure + packaging
- Manufacturing labor
- Logistics and shipping
- Inventory carrying costs
- Quality control and testing

**Hidden Costs**:
- Warranty and RMA (return merchandise authorization)
- Component obsolescence management
- Supply chain management overhead
- Field failures and product recalls

**Cost Optimization Timeline**:
- **EVT**: Focus on functionality, not cost (prototypes expensive)
- **DVT**: Cost optimization begins—negotiate with suppliers, DFM improvements
- **PVT**: Final cost validation—lock in supplier agreements
- **MP**: Continuous cost reduction—running changes, yield improvements

---

## Hardware PM Methodologies

### Waterfall vs Agile in Hardware

Hardware projects are primarily **Waterfall** because:
- Physical products require sequential phases
- High cost of error prevents "fail fast" approach
- Tooling investment creates points of no return
- Supply chain lead times prevent rapid iteration

**BUT**: Modern hardware teams use **hybrid approaches**

**Proof-of-Concept (POC) Phase**:
- Agile-like
- Use off-the-shelf components
- Rapid iteration to test uncertain assumptions
- Firmware development can start in parallel
- Focus on "unknowns" (peripheral limits, memory, CPU, new technologies)

**After POC**:
- More Waterfall
- Architecture locked
- Hardware and firmware work independently
- Integration testing after first custom PCB arrives
- Expect 2-3 iterations to get it right

**IoT/Connected Devices**: Hardware uses predictive Waterfall, while firmware/software/cloud use Agile sprints—teams synchronize at integration points.

---

### Phase-Gate Methodology

**Phase-Gate** is the dominant framework for hardware development. Each phase has:
- **Entry Criteria**: What must be true to enter this phase
- **Activities**: Work performed during the phase
- **Deliverables**: Outputs required to complete the phase
- **Exit Criteria (Gate Review)**: Decision point—advance, iterate, or cancel

**Gate Reviews** involve:
- Cross-functional team review (engineering, PM, quality, manufacturing, business)
- Review of deliverables and test results
- Risk assessment and mitigation plans
- Go/No-Go decision to proceed to next phase
- Budget and schedule review

**Benefits of Phase-Gates**:
- Structured decision-making
- Risk reduction through validation
- Clear accountability and milestones
- Prevents expensive late-stage changes
- Aligns cross-functional teams

---

## Managing Hardware Projects: Best Practices

### 1. Communication

Efficient team communication is challenging but critical.

**Communication Strategy**:
- **Team sync meetings**: 2x per week, 30 minutes (for 6-8 engineers)
- **Method selection**: Choose right tool for the task
  - Real-time (Slack/Teams): Quick questions
  - Async (Email): Formal requests, documentation
  - Face-to-face: Complex technical discussions, design reviews
- **Clarity and precision**: Vague questions → wrong answers
- **Documentation**: Write everything down—hardware decisions are expensive to change

---

### 2. Documentation

Hardware requires **rigorous documentation** because:
- Design decisions must be traceable
- Manufacturing needs complete specifications
- Compliance requires proof of validation
- Component changes need change control
- Future teams need to understand design rationale

**Essential Documents**:
- Product Requirements Document (PRD)
- Design specifications (electrical, mechanical, firmware)
- Schematics and PCB layouts
- BOM with suppliers and costs
- Test plans and test reports
- Manufacturing instructions and process documents
- Compliance test reports and certifications
- Change request history

---

### 3. Risk Management

Hardware risks are different from software:
- Longer timelines mean more uncertainty
- Physical failures have real-world consequences
- Supply chain disruptions can halt production
- Regulatory delays can miss market windows
- Component obsolescence can require redesign

**Key Hardware Risks**:
- **Technical risk**: Design doesn't meet performance requirements
- **Manufacturing risk**: Yield below targets, quality issues
- **Supply chain risk**: Component shortages, supplier bankruptcy
- **Compliance risk**: Fails certification testing
- **Cost risk**: BOM costs exceed targets
- **Schedule risk**: Delays cascade through phases

**Risk Mitigation**:
- Identify risks early (Concept and EVT phases)
- Retire technical risks in EVT phase
- Have second-source suppliers for critical components
- Start compliance testing early (pre-scans in EVT/DVT)
- Build schedule buffers (20-30% for hardware projects)
- Maintain risk register and update weekly

---

### 4. Coordination Across Disciplines

Hardware projects require coordination of many processes and people with diverse competencies.

**Typical Team Structure**:
- **Project Manager** - Timeline, budget, coordination
- **Hardware Engineer** - Schematic, PCB design
- **Firmware Engineer** - Embedded software, drivers
- **Mechanical Engineer** - Enclosure, thermal design
- **Manufacturing Engineer** - DFM, process optimization
- **Quality Engineer** - Test plans, validation
- **Regulatory/Compliance** - Certifications (CE, FCC, FDA)
- **Supply Chain** - Component sourcing, suppliers
- **Industrial Designer** - Product aesthetics, user experience

**Coordination Challenges**:
- Different timelines (mechanical vs electrical vs firmware)
- Dependencies (enclosure can't be finalized until PCB size known)
- Tooling lead times require early commitment
- Integration risks (subsystems work independently but fail together)

**Best Practices**:
- Weekly cross-functional syncs
- Clear interface definitions between subsystems
- Early integration testing (don't wait for PVT!)
- Co-located teams when possible (especially during integration)

---

## Timeline Expectations by Industry

| Industry | Typical Timeline | Why |
|----------|-----------------|-----|
| **Consumer Electronics** | 9-15 months | Fast time-to-market, competitive pressure, lower regulatory burden |
| **IoT Devices** | 12-18 months | Hardware + firmware + cloud, integration complexity |
| **Industrial Hardware** | 18-24 months | High reliability requirements, extensive validation |
| **Robotics** | 24-36 months | Complex integration (mechanical + electrical + software), safety validation |
| **Medical Devices** | 24-48 months | Regulatory approval (FDA, MDR), clinical trials, extensive testing |
| **Automotive Electronics** | 36-60 months | Zero-defect requirements, PPAP, long qualification cycles |

**Factors that extend timelines**:
- Regulatory requirements (FDA, ISO 26262)
- Safety-critical systems (medical, automotive, robotics)
- Complex integration (mechatronics, IoT)
- Custom components (long lead times)
- High reliability requirements (industrial, automotive)

**General Rule**: Hardware takes longer than software, but timelines vary significantly by industry.

---

## Common Pitfalls and How to Avoid Them

### 1. "We'll Fix It in Software"

**Mistake**: Assuming firmware can compensate for hardware design flaws.

**Reality**: Some hardware limitations cannot be overcome by software. Don't count on it.

**Solution**: Validate hardware thoroughly in EVT phase. Test corner cases and stress conditions.

---

### 2. Late Design Changes

**Mistake**: Making design changes after tooling commitment.

**Reality**: Post-tooling changes cost 10-100x more than pre-tooling changes.

**Solution**: Rigorous phase-gate reviews. Lock design at DVT. Use formal change control after design freeze.

---

### 3. Single-Source Components

**Mistake**: Designing around a component with only one supplier.

**Reality**: If that component goes EOL or supplier has shortage, you're stuck.

**Solution**: Design for second sources from the start. Evaluate alternates during EVT.

---

### 4. Underestimating Lead Times

**Mistake**: Assuming components arrive in 2 weeks.

**Reality**: Critical ICs can have 20-52 week lead times.

**Solution**: Check lead times during design phase. Order long-lead items early. Build 20-30% schedule buffer.

---

### 5. Skipping Pre-Compliance Testing

**Mistake**: Waiting until PVT to test for CE/FCC/UL compliance.

**Reality**: Failing certification at PVT means expensive design changes and delays.

**Solution**: Pre-compliance testing in EVT (basic) and DVT (full). Budget €20K-€50K for pre-testing.

---

### 6. Ignoring DFM Until PVT

**Mistake**: Designing without considering manufacturability.

**Reality**: Design that's hard to manufacture = low yields, high costs, delays.

**Solution**: Involve manufacturing engineers in DVT phase. Design reviews with CM (contract manufacturer). DFM analysis before tooling.

---

### 7. Poor BOM Management

**Mistake**: Incomplete or inaccurate BOMs.

**Reality**: Missing one component halts entire production run. Wrong costs blow up budget.

**Solution**: Maintain BOM from day 1. Update continuously. Track lifecycle status. Validate with suppliers before PVT.

---

## Getting Started: Your First Hardware Project

### Step 1: Learn the Terminology

- Understand EVT, DVT, PVT, MP phases
- Learn component terminology (passives, ICs, connectors, etc.)
- Familiarize with manufacturing terms (PCB, SMT, DFM, yields)
- Study compliance requirements for your market (CE, FCC, RoHS)

### Step 2: Use the Templates

This starter kit provides ready-to-use templates:
1. Start with **[Project Charter](../templates/01-project-charter.md)** - define scope, team, timeline, success criteria
2. Create **[Risk Register](../templates/02-risk-register.md)** - identify hardware-specific risks early
3. Plan phases using **[Phase Gate Checklist](../templates/03-phase-gate-checklist.md)** - customize for your industry
4. Adapt **[Sprint Planning Template](../templates/04-sprint-planning.md)** for 4-8 week hardware sprints
5. Track with **[BOM Template](../templates/07-bom-template.md)** and **[Test Plan Template](../templates/09-test-plan-template.md)**


### Step 3: Build Your Team

- Identify required disciplines (hardware, firmware, mechanical, etc.)
- Define roles and responsibilities clearly
- Establish communication cadence (weekly syncs, phase reviews)
- Include manufacturing and quality from the start

### Step 4: Plan for the Long Haul

- Set realistic timelines (12-24 months for most hardware)
- Budget for prototypes, tooling, certifications
- Build schedule buffers (20-30%)
- Plan cash flow (hardware costs are upfront)

### Step 5: Embrace Phase-Gates

- Define clear gate criteria for your project
- Schedule gate reviews with stakeholders
- Don't skip phases—they exist for a reason
- Learn from each phase to improve the next

---

## Additional Resources

**Learn More**:
- **[Industry Customization Guide](02-customization-guide.md)** - Adapt templates for consumer electronics, medical devices, IoT, industrial, robotics, automotive
- **[Phase Gate Deep Dive](03-phase-gate-guide.md)** - Detailed walkthrough of EVT → DVT → PVT → MP
- **[Risk Management Guide](04-risk-management-guide.md)** - Hardware-specific risk identification and mitigation
- **[Compliance Guide for EU/Italy](05-compliance-guide-eu.md)** - CE marking, RoHS, REACH, MDR

**Books**:
- *The Hardware Hacker* by Andrew "bunnie" Huang
- *Making Things Move* by Dustyn Roberts
- *Zero to One* by Peter Thiel (for startups)

**Communities**:
- [r/hwstartups](https://www.reddit.com/r/hwstartups/) - Hardware startup community
- [Electronics StackExchange](https://electronics.stackexchange.com/) - Hardware Q&A community

---

## Conclusion

Hardware project management is challenging but rewarding. The physical constraints, long timelines, and high costs demand discipline, planning, and attention to detail. But when you hold the final product in your hands—something tangible you helped create—the satisfaction is unmatched.

**Remember**:
- Hardware is unforgiving—plan carefully, validate thoroughly
- Phase-gates exist to catch problems early (when they're cheap to fix)
- Risk management is critical—identify and retire risks as early as possible
- Communication and documentation are your friends
- Build schedule and budget buffers—hardware always takes longer than expected

**You're not alone**: Use this starter kit, learn from the community, and iterate on your processes. Every hardware project teaches lessons that make the next one better.

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit

---

*"In software, you can always roll back. In hardware, you better get it right the first time."*
