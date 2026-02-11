# Hardware Project Management - Customization Guide

> **How to adapt the templates for different hardware industries and contexts**

---

## Introduction

This guide helps you **customize the Hardware PM Starter Kit templates** for your specific industry, product type, and organizational context. While the core principles of hardware project management remain consistent, different sectors have unique requirements, timelines, and risk profiles.

**Use this guide to**:
- Understand industry-specific considerations
- Adapt templates to your product category
- Tailor phase gates and timelines
- Adjust risk management approaches
- Modify compliance requirements

---

## Quick Navigation

- [Industry-Specific Considerations](#industry-specific-considerations)
  - [Consumer Electronics](#consumer-electronics)
  - [Medical Devices](#medical-devices)
  - [Industrial Hardware & Automation](#industrial-hardware--automation)
  - [IoT & Connected Devices](#iot--connected-devices)
  - [Robotics](#robotics)
  - [Automotive Electronics](#automotive-electronics)
- [Template Customization Matrix](#template-customization-matrix)
- [Common Adaptations](#common-adaptations)
- [Compliance Mapping](#compliance-mapping)

---

## Industry-Specific Considerations

### Consumer Electronics

> **Characteristics**: Fast time-to-market, short product lifecycles, high competition, innovation-driven

#### Key Differences from Base Templates

**Timeline Adjustments**:
- **Faster phases**: EVT (4-8 weeks), DVT (6-12 weeks), PVT (4-8 weeks)
- **Shorter product lifecycle**: 12-24 months typical
- **Multiple SKUs/variants**: Plan for color options, storage tiers, regional versions

**Risk Profile** [web:134][web:140]:
- **Speed prioritized over perfection**: "Ship and iterate" mindset acceptable
- **Lower regulatory burden**: CE, FCC, RoHS are primary (no FDA)
- **Component obsolescence**: High risk due to fast technology evolution
- **Market timing risk**: Missing launch window can be fatal

**Project Charter Customizations**:

```markdown
### Success Criteria (Consumer Electronics Focus)
- [ ] Time to market: Launch by [TRADE_SHOW/SEASON]
- [ ] Product cost < $[X] at [HIGH_VOLUME] units (100K+)
- [ ] Feature parity with competitor [COMPETITOR]
- [ ] Battery life > [X] days (for battery-powered devices)
- [ ] App ecosystem: iOS and Android apps ready at launch

### Phase Timeline (Accelerated)
- Concept: 2-4 weeks
- EVT: 4-8 weeks  
- DVT: 6-12 weeks
- PVT: 4-8 weeks
- MP Readiness: 2-4 weeks
```

**Risk Register Additions**:
- Market timing: "Competitor launches first" - High probability, High impact
- Technology obsolescence: "Component EOL before launch" - Medium probability, High impact
- Fashion/trend risk: "Design becomes outdated" - Medium probability, Medium impact

**Compliance Requirements**:
- **Europe/Italy**: CE marking (mandatory), RoHS, REACH, WEEE
- **United States**: FCC (electromagnetic emissions)
- **Global**: UL (safety), IP rating (water/dust resistance)
- **Battery safety**: UN 38.3 (if lithium batteries), IEC 62133

---

### Medical Devices

> **Characteristics**: Rigorous regulatory requirements, long development cycles, high reliability demands, risk-averse culture

#### Key Differences from Base Templates [web:134][web:137][web:143]

**Timeline Adjustments**:
- **Much longer phases**: EVT (12-20 weeks), DVT (20-32 weeks), PVT (12-20 weeks)
- **Extended certification**: Add 12-24 months for MDR regulatory approval (Notified Body involvement mandatory for Class IIa and above)
  - **Clinical evidence requirements**: Add 6-12 months for clinical evaluation/data collection
  - **Note**: MDR fully effective since May 2021, all new devices must comply (no more MDD grandfathering as of May 2024)
- **Total timeline**: 18-36 months typical (vs 9-18 months consumer)
- **Product lifecycle**: 5-10+ years (factor in long-term support)

**Risk Profile**:
- **Patient safety paramount**: Any failure can harm or kill users
- **Regulatory scrutiny**: FDA (US), MDR (EU), Health Canada, etc.
- **Liability exposure**: Multi-million dollar lawsuits possible
- **Cybersecurity critical**: HIPAA/GDPR compliance, encrypted data
- **Biocompatibility**: Materials must not cause adverse reactions

**Project Charter Customizations**:

```markdown
### Success Criteria (Medical Device Focus)
- [ ] FDA 510(k) clearance obtained (or CE Mark under MDR)
- [ ] Clinical validation: [X] patient study completed successfully
- [ ] Reliability: MTBF > [X] hours, designed for [Y] year lifetime
- [ ] Biocompatibility: ISO 10993 testing complete
- [ ] Cybersecurity: FDA premarket cybersecurity guidance compliant
- [ ] Usability: Human Factors Engineering (HFE) validation passed

### Regulatory Milestones (Add to Timeline)
- Pre-submission meeting with FDA/Notified Body: [DATE]
- Design freeze for regulatory submission: [DATE]
- Clinical trial initiation: [DATE]
- Regulatory submission: [DATE]
- Regulatory clearance/approval: [DATE]

### Medical-Specific Deliverables
- [ ] Design History File (DHF)
- [ ] Risk Management File (ISO 14971)
- [ ] Clinical Evaluation Report
- [ ] Usability Engineering File (IEC 62366)
- [ ] Software validation (if applicable - IEC 62304)
- [ ] Sterilization validation (if applicable)
```

**Risk Register - Medical Focus**:
- **Regulatory delay**: "FDA requests additional testing" - High probability, Critical impact
- **Clinical trial failure**: "Device does not meet efficacy endpoints" - Medium probability, Critical impact
- **Adverse events**: "Patient injury during testing" - Low probability, Critical impact
- **Cybersecurity breach**: "Data exposure violates HIPAA" - Medium probability, High impact

**Compliance Requirements** [web:137]:
- **Europe/Italy**: MDR (Medical Device Regulation 2017/745), CE marking via Notified Body
- **United States**: FDA Class I/II/III (510(k), PMA, or De Novo)
- **Quality System**: ISO 13485 (medical device QMS)
- **Risk Management**: ISO 14971
- **Usability**: IEC 62366 (human factors engineering)
- **Software**: IEC 62304 (if software is integral)
- **Biocompatibility**: ISO 10993 series
- **Sterilization**: ISO 11135 (EtO), ISO 11137 (radiation), ISO 17665 (steam)

**Phase Gate Additions**:
- **Design Freeze Gate** (before regulatory submission): No changes allowed without formal change control
- **Clinical Trial Readiness Gate**: Ethics approval, investigator training complete
- **Regulatory Submission Gate**: All documentation complete, ready to submit

---

### Industrial Hardware & Automation

> **Characteristics**: High reliability, harsh environments, long product lifecycles, B2B sales, service/support critical

#### Key Differences from Base Templates

**Timeline Adjustments**:
- **Extended validation**: DVT and PVT phases longer for environmental testing
- **Field trials**: Add 8-16 weeks for beta testing at customer sites
- **Product lifecycle**: 10-20 years (plan for long-term component availability)

**Risk Profile**:
- **Downtime cost**: Industrial customers lose $X/hour when equipment fails
- **Environmental extremes**: -40°C to +85°C, vibration, dust, moisture, EMI
- **Safety critical**: Machinery safety standards (IEC 61508, ISO 13849)
- **Long support obligations**: 10+ years spare parts and repairs

**Project Charter Customizations**:

```markdown
### Success Criteria (Industrial Focus)
- [ ] Reliability: MTBF > [50,000] hours, designed for [15] year lifetime
- [ ] Environmental: IP67 rating, -40°C to +85°C operating range
- [ ] Safety: SIL 2 (or SIL 3) certification (IEC 61508)
- [ ] EMC: Industrial EMC standards (IEC 61000-6-2, IEC 61000-6-4)
- [ ] Field trial: [X] months at [Y] customer sites with zero critical failures

### Industrial-Specific Phases
- **Field Trial Phase** (add between PVT and MP): 12-24 weeks
  - Goal: Validate performance in real customer environments
  - Activities: Install at 3-5 customer sites, monitor remotely, collect feedback
  - Gate Criteria: No critical failures, customer acceptance
```

**Risk Register - Industrial Focus**:
- **Harsh environment failure**: "Device fails in temperature extremes" - Medium probability, High impact
- **Customer downtime**: "Equipment failure stops production line" - Low probability, Critical impact
- **Long-term availability**: "Key component obsolete in year 5" - High probability, High impact
- **Safety incident**: "Equipment causes operator injury" - Low probability, Critical impact

**Compliance Requirements**:
- **Europe/Italy**: Machinery Directive (2006/42/EC), CE marking
- **Safety**: IEC 61508 (functional safety), ISO 13849 (machinery safety)
- **EMC**: IEC 61000-6-2 (immunity), IEC 61000-6-4 (emissions)
- **Environmental**: IP ratings (IEC 60529), operating temperature ranges
- **Hazardous locations**: ATEX (Europe), IECEx (international) if explosive atmospheres

---

### IoT & Connected Devices

> **Characteristics**: Hardware + firmware + software + cloud, interdisciplinary teams, cybersecurity critical, connectivity dependencies

#### Key Differences from Base Templates [web:135][web:138][web:141][web:144]

**Timeline Adjustments**:
- **Hybrid Agile approach**: Hardware (predictive), firmware/software (agile sprints) [web:135]
- **Parallel development**: Hardware, firmware, backend software developed concurrently
- **Integration challenges**: Add 2-4 weeks per phase for HW/FW/SW integration testing
- **Over-the-air updates**: Plan for post-launch firmware update strategy

**Risk Profile**:
- **Connectivity dependencies**: Cellular, Wi-Fi, Bluetooth, LoRaWAN - each has risks
- **Cloud infrastructure**: AWS/Azure/GCP downtime affects product functionality
- **Cybersecurity**: IoT devices are hacking targets, data breaches possible
- **Battery life**: Connected devices drain power quickly
- **Interoperability**: Must work with multiple platforms (iOS, Android, Alexa, Google Home)

**Project Charter Customizations** [web:135]:

```markdown
### Success Criteria (IoT Focus)
- [ ] Connectivity: 99.9% uptime, < [X] second latency
- [ ] Battery life: > [X] months on single charge (for battery devices)
- [ ] Cybersecurity: OWASP IoT Top 10 vulnerabilities addressed
- [ ] Data privacy: GDPR compliant (EU), encrypted data in transit and at rest
- [ ] Cloud infrastructure: Scalable to [X] million devices
- [ ] Mobile apps: iOS and Android apps with [X] star rating

### IoT-Specific Deliverables
- [ ] Unified backlog (hardware + firmware + software + cloud) [web:135]
- [ ] API documentation and versioning strategy
- [ ] Cybersecurity threat model and penetration testing
- [ ] Over-the-air (OTA) update mechanism and rollback plan
- [ ] Cloud infrastructure architecture and scaling plan
- [ ] Data retention and privacy policy

### Team Structure (Cross-Functional)
- Hardware Engineer
- Firmware Engineer (embedded)
- Backend Software Engineer (cloud/API)
- Mobile App Developer (iOS/Android)
- DevOps Engineer (cloud infrastructure)
- Cybersecurity Engineer
- Data Scientist (if analytics/ML)
```

**Risk Register - IoT Focus** [web:135][web:138]:
- **Cloud service outage**: "AWS region goes down" - Low probability, Critical impact
- **Cybersecurity breach**: "Device hacked, user data stolen" - Medium probability, Critical impact
- **Connectivity issues**: "Device can't connect in weak signal areas" - High probability, High impact
- **Battery drain**: "Firmware bug causes rapid battery drain" - Medium probability, High impact
- **Integration bugs**: "Hardware ready but firmware delayed" - High probability, Medium impact

**Best Practices** [web:135][web:138]:
1. **Unified Backlog**: Centralize HW/FW/SW requirements in single backlog for alignment [web:135]
2. **Daily Standups**: Quick sync across hardware, firmware, software teams [web:135]
3. **MVP First**: Build minimum viable hardware + firmware + cloud for early validation [web:135]
4. **Iteration Reviews**: Continuous stakeholder feedback on integrated system [web:135]
5. **Hybrid Methodology**: Agile for software/firmware, predictive for hardware [web:135]

**Compliance Requirements**:
- **Europe/Italy**: CE marking, RED (Radio Equipment Directive) for wireless
- **United States**: FCC Part 15 (Wi-Fi/Bluetooth), FCC Part 22/24 (cellular)
- **Cybersecurity (effective 2027)**: 
  - Cyber Resilience Act (Regulation EU 2024/2847) - mandatory for products with digital elements
  - ETSI EN 303 645 (EU IoT security baseline)
  - Essential cybersecurity requirements (Annex I CRA)
  - Timeline: Applies from December 2027, start planning in 2026
- **Data privacy**: GDPR (EU), CCPA (California)
- **Wireless**: Bluetooth SIG certification, Wi-Fi Alliance certification

---

### Robotics

> **Characteristics**: Complex mechatronics, software-intensive, safety-critical, high integration complexity

#### Key Differences from Base Templates

**Timeline Adjustments**:
- **Extended integration**: Add 4-8 weeks per phase for mechanical/electrical/software integration
- **Safety validation**: Add 8-12 weeks for safety testing and certification
- **Field testing**: Add 12-24 weeks for real-world validation
- **Total timeline**: 24-48 months typical for complex robots

**Risk Profile**:
- **Safety hazards**: Moving parts, high torque, pinch points can injure humans
- **Integration complexity**: Mechanical, electrical, firmware, perception, planning, control - many failure modes
- **Environmental uncertainty**: Real-world environments unpredictable
- **Human-robot interaction**: Collaborative robots must detect and avoid humans

**Project Charter Customizations**:

```markdown
### Success Criteria (Robotics Focus)
- [ ] Safety: ISO 13849 PLd or PLe, collaborative robot ISO/TS 15066 compliant
- [ ] Performance: [X] kg payload, [Y] mm repeatability, [Z] m/s max speed
- [ ] Reliability: MTBF > [X] hours, [Y] year design life
- [ ] Autonomy: Operates [X] hours unattended, < [Y]% human intervention
- [ ] Software: ROS/ROS2 integration, simulation environment validated

### Robotics-Specific Phases
- **System Integration Phase** (add after DVT): 8-12 weeks
  - Goal: Integrate mechanical, electrical, software subsystems
  - Activities: End-to-end system testing, performance validation, safety testing
  - Gate Criteria: All subsystems working together, safety requirements met

### Robotics-Specific Deliverables
- [ ] Kinematic and dynamic models
- [ ] Safety risk assessment (ISO 12100)
- [ ] Collision detection and safe stop validation
- [ ] Perception system validation (if vision/sensors)
- [ ] Motion planning algorithm validation
- [ ] Human-robot interaction study (if collaborative)
```

**Risk Register - Robotics Focus**:
- **Safety incident**: "Robot injures operator during testing" - Low probability, Critical impact
- **Integration failure**: "Mechanical and software subsystems don't work together" - High probability, High impact
- **Perception failure**: "Robot doesn't detect obstacle, collision occurs" - Medium probability, High impact
- **Software bugs**: "Control algorithm causes erratic motion" - Medium probability, High impact

**Compliance Requirements**:
- **Europe/Italy**: Machinery Directive (2006/42/EC), CE marking
- **Safety**: ISO 12100 (machinery safety), ISO 13849 (safety control systems)
- **Collaborative robots**: ISO/TS 15066 (collaborative robot safety)
- **EMC**: IEC 61000-6-2, IEC 61000-6-4
- **Software**: IEC 61508 (if safety-critical software)

---

### Automotive Electronics

> **Characteristics**: Extremely high reliability, harsh environments, long qualification cycles, safety-critical, high-volume production

#### Key Differences from Base Templates

**Timeline Adjustments**:
- **Extended validation**: DVT (24-40 weeks), PVT (20-32 weeks)
- **Automotive qualification**: Add 12-24 months for PPAP, APQP, reliability testing
- **Design life**: 15 years, 200,000 miles - extensive reliability testing required
- **Total timeline**: 36-60 months typical

**Risk Profile**:
- **Safety critical**: Failures can cause accidents, injuries, deaths
- **Environmental extremes**: -40°C to +125°C (under hood), vibration, EMI, humidity
- **Liability exposure**: Product recalls cost millions, reputational damage
- **Long supply chain**: Tier 1/2/3 supplier structure, long lead times

**Project Charter Customizations**:

```markdown
### Success Criteria (Automotive Focus)
- [ ] Reliability: Zero defects at [X] million units, < [Y] PPM failure rate
- [ ] Environmental: AEC-Q100 (ICs), AEC-Q200 (passives) qualified components
- [ ] Safety: ISO 26262 ASIL B/C/D (depending on function)
- [ ] EMC: CISPR 25 (automotive EMC standard)
- [ ] Qualification: PPAP Level 3 approved by OEM customer
- [ ] Design life: 15 years, 200,000 miles validated

### Automotive-Specific Phases
- **APQP Phase** (add before MP): 24-36 weeks
  - Advanced Product Quality Planning per AIAG APQP manual
  - Activities: FMEA, control plan, MSA, process capability studies
  - Gate Criteria: PPAP approved, Cpk > 1.33 for critical parameters

### Automotive-Specific Deliverables
- [ ] DFMEA (Design Failure Mode Effects Analysis)
- [ ] PFMEA (Process Failure Mode Effects Analysis)
- [ ] Control plan
- [ ] ISO 26262 safety case (if ASIL rated)
- [ ] PPAP documentation (PSW, dimensional results, material certs, etc.)
- [ ] DVP&R (Design Verification Plan and Report)
```

**Risk Register - Automotive Focus**:
- **Field recall**: "Component failure requires recall of [X] vehicles" - Low probability, Catastrophic impact
- **Environmental failure**: "Component fails in extreme temperature" - Medium probability, Critical impact
- **OEM rejection**: "Customer rejects PPAP submission" - Medium probability, High impact
- **Long-term reliability**: "Failure rate increases after 5 years" - Medium probability, High impact

**Compliance Requirements**:
- **Safety**: ISO 26262 (functional safety for road vehicles)
- **Quality**: IATF 16949 (automotive quality management system)
- **Environmental**: AEC-Q100 (IC qualification), AEC-Q200 (passive components)
- **EMC**: CISPR 25 (automotive EMC), ISO 11452 (immunity)
- **Materials**: RoHS, REACH, ELV Directive (End-of-Life Vehicles)

---

## Template Customization Matrix

**Which templates need customization for your industry?**

| Template | Consumer Electronics | Medical Devices | Industrial | IoT | Robotics | Automotive |
|----------|---------------------|-----------------|------------|-----|----------|------------|
| **Project Charter** | Timeline shortened | Regulatory milestones added | Field trial phase added | Unified backlog noted | Integration phase added | APQP phase added |
| **Risk Register** | Market timing risks | Patient safety risks | Downtime risks | Cybersecurity risks | Safety hazards | Recall risks |
| **Phase Gate Checklist** | Fast-track gates | Design freeze gate added | Field trial gate added | Integration gate per phase | System integration gate | PPAP gate added |
| **Sprint Planning** | 2-week sprints | 4-week sprints | 4-week sprints | Hybrid (HW 4-week, SW 2-week) | 3-4 week sprints | 4-week sprints |
| **Lessons Learned** | Competitive analysis | Regulatory lessons | Customer site learnings | Cloud/connectivity issues | Integration challenges | Qualification process |

---

## Common Adaptations

### Timeline Scaling

**General Rule**: Multiply base timeline by industry factor

| Industry | Timeline Multiplier | Example (Base: 12 months) |
|----------|---------------------|---------------------------|
| Consumer Electronics | 0.6 - 0.8x | 7-10 months |
| IoT Devices | 1.0 - 1.2x | 12-14 months |
| Industrial Hardware | 1.2 - 1.5x | 14-18 months |
| Robotics | 1.5 - 2.0x | 18-24 months |
| Medical Devices | 2.0 - 3.0x | 24-36 months |
| Automotive | 3.0 - 4.0x | 36-48 months |

### Risk Tolerance Levels

**Adjust risk assessment based on industry**:

| Industry | Risk Tolerance | Iteration Philosophy | Quality Bar |
|----------|---------------|---------------------|-------------|
| Consumer Electronics | **High** | Ship and iterate | Good enough |
| IoT Devices | **Medium-High** | Iterate firmware post-launch | High quality |
| Industrial Hardware | **Medium** | Validate extensively | Very high quality |
| Robotics | **Low** | Test thoroughly before release | Extremely high quality |
| Medical Devices | **Very Low** | Zero tolerance for defects | Perfection required |
| Automotive | **Extremely Low** | Zero defects mandated | Beyond perfection |

### Compliance Focus Areas

**Prioritize compliance based on industry**:

| Industry | Primary Compliance | Secondary Compliance | Timeline Impact |
|----------|-------------------|----------------------|-----------------|
| Consumer Electronics | CE, FCC, RoHS | UL, IP rating | +2-4 months |
| IoT Devices | CE, FCC, RED, GDPR | ETSI EN 303 645, cybersecurity | +3-6 months |
| Industrial Hardware | Machinery Directive, IEC 61508 | ATEX, EMC | +6-12 months |
| Robotics | Machinery Directive, ISO 13849 | ISO/TS 15066 (if collaborative) | +6-12 months |
| Medical Devices | FDA 510(k)/PMA, MDR (EU) | ISO 13485, ISO 14971, IEC 62366 | +12-24 months |
| Automotive | ISO 26262, IATF 16949 | CISPR 25, AEC-Q100 | +18-36 months |

---

## Compliance Mapping

### Europe / Italy Specific

**For Italian/European market, these are mandatory**:

| Compliance | Applies To | Mandatory? | Timeline | Cost |
|-----------|-----------|------------|----------|------|
| **CE Marking** | All hardware products sold in EU | ✅ Yes | 3-6 months | €5K-€50K || **RoHS** | Electronics with > 4 specific substances | ✅ Yes | 1-2 months | €5K-€15K |
| **REACH** | Products with chemicals > 0.1% threshold | ✅ Yes | 2-4 months | €10K-€30K |
| **WEEE** | Electrical/electronic equipment | ✅ Yes | 1-2 months | €5K-€10K |
| **RED** | Radio/wireless devices | ✅ If wireless | 4-8 months | €20K-€60K |
| **MDR** | Medical devices | ✅ If medical | 12-24 months | €100K-€500K+ |
| **Machinery Directive** | Machinery/robots | ✅ If machinery | 6-12 months | €30K-€100K |

### Customizing Compliance Section in Templates

**Project Charter - Compliance Section Template**:

```markdown
### Compliance Requirements ([YOUR_INDUSTRY])

**European / Italian Market** (Mandatory):
- [ ] CE Marking - [Directive] - Target: [DATE] - Budget: €[X]
- [ ] RoHS (2011/65/EU) - Target: [DATE] - Budget: €[X]
- [ ] REACH (EC 1907/2006) - Target: [DATE] - Budget: €[X]
- [ ] WEEE (2012/19/EU) - Target: [DATE] - Budget: €[X]
- [ ] [Add industry-specific EU regulations]

**Global Market** (If applicable):
- [ ] FCC (US electromagnetic emissions) - Target: [DATE] - Budget: $[X]
- [ ] [Add other global requirements]

**Industry-Specific**:
- [ ] [Add industry-specific standards: ISO 13485, ISO 26262, IEC 61508, etc.]
- [ ] [Add safety standards]
- [ ] [Add cybersecurity standards if IoT]

**Pre-Compliance Testing Strategy**:
- EVT phase: Basic [Standard] pre-scan - Budget: €[X]
- DVT phase: Full pre-compliance testing - Budget: €[X]
- Certification: Final testing at Notified Body/Test Lab - Budget: €[X]
```

---

## Step-by-Step Customization Process

### 1. Identify Your Context

**Answer these questions**:
- What industry am I in? (Consumer, Medical, Industrial, IoT, Robotics, Automotive)
- What is my risk tolerance? (High risk / Medium / Low risk / Zero tolerance)
- What is my time-to-market pressure? (Fast / Moderate / No rush)
- What is my target market? (Italy/EU / US / Global)
- What is my product complexity? (Simple / Moderate / Complex / Highly complex)

### 2. Select Base Timeline

**Choose appropriate timeline multiplier** from table above.

**Example**:
- Base timeline: 12 months
- Industry: Medical Devices (2.5x multiplier)
- Adjusted timeline: 30 months

### 3. Add Industry-Specific Phases

**Consult industry section above** and add:
- Regulatory phases (medical)
- Field trial phases (industrial)
- Integration phases (robotics, IoT)
- APQP phases (automotive)

### 4. Customize Risk Register

**Add industry-specific risks** from sections above:
- Market timing (consumer)
- Patient safety (medical)
- Cybersecurity (IoT)
- Safety hazards (robotics, automotive)

### 5. Update Compliance Requirements

**Use Compliance Mapping table** to add:
- Mandatory EU/Italian requirements
- Industry-specific standards
- Global market requirements (if applicable)

### 6. Adjust Success Criteria

**Align KPIs with industry norms**:
- Consumer: Time-to-market, cost targets
- Medical: Regulatory approval, clinical validation
- Industrial: Reliability, MTBF, environmental performance
- IoT: Connectivity uptime, cybersecurity
- Robotics: Safety certification, autonomy metrics
- Automotive: Zero defects, PPAP approval

### 7. Modify Team Structure

**Add industry-specific roles**:
- Medical: Regulatory Affairs, Clinical Engineering
- IoT: Cloud/Backend Engineers, Cybersecurity
- Robotics: Perception Engineers, Motion Planning
- Automotive: APQP Coordinator, Functional Safety Engineer

---

## Example Customizations

### Example 1: Consumer Electronics Smartwatch

**Starting Point**: Base templates  
**Industry**: Consumer Electronics  
**Timeline**: 12 months (base) × 0.7 = 8.4 months  
**Key Customizations**:

```markdown
# Project Charter Adjustments
- Timeline: Compressed to 8 months (holiday launch target)
- Success Criteria: Launch by Black Friday, BOM < $80, battery > 5 days
- Risk Focus: Component shortages, competitive launches
- Compliance: CE, FCC, RoHS, Bluetooth SIG, Wi-Fi Alliance

# Phase Gate Adjustments
- EVT: 4 weeks (minimal prototype)
- DVT: 8 weeks (production-intent)
- PVT: 6 weeks (pilot build)
- MP: 2 weeks (ramp quickly)

# Sprint Planning Adjustments
- 2-week sprints (hardware and firmware aligned)
- Co-located team for fast decisions
```

### Example 2: Medical Continuous Glucose Monitor

**Starting Point**: Base templates  
**Industry**: Medical Devices  
**Timeline**: 12 months (base) × 2.5 = 30 months  
**Key Customizations**:

```markdown
# Project Charter Adjustments
- Timeline: 30 months (includes 12 months regulatory)
- Success Criteria: FDA 510(k) clearance, CE Mark (MDR), ISO 13485 certified
- Risk Focus: Clinical validation, biocompatibility, patient safety
- Compliance: FDA 510(k), MDR (EU), ISO 13485, ISO 14971, IEC 62304, ISO 10993

# Phase Gate Adjustments
- Add Design Freeze Gate (month 18) - No changes after this without formal change control
- Add Clinical Trial Gate (month 20) - Requires ethics approval
- Add Regulatory Submission Gate (month 24) - All documentation complete
- PVT: Extended to 20 weeks for reliability testing

# Risk Register Adjustments
- Add patient safety risks (adverse events, device malfunction causing harm)
- Add regulatory risks (FDA requests additional data)
- Add clinical trial risks (efficacy endpoints not met)
```

### Example 3: Industrial Warehouse Robot

**Starting Point**: Base templates  
**Industry**: Robotics + Industrial  
**Timeline**: 12 months (base) × 1.8 = 21.6 months (≈ 22 months)  
**Key Customizations**:

```markdown
# Project Charter Adjustments
- Timeline: 22 months (includes 6 months field trials)
- Success Criteria: ISO 13849 PLd, 50,000 hour MTBF, -20°C to +50°C operation
- Risk Focus: Human-robot interaction safety, integration complexity
- Compliance: Machinery Directive, ISO 12100, ISO 13849, IP54 rating

# Phase Gate Adjustments
- Add System Integration Phase (12 weeks) after DVT
- Add Field Trial Phase (24 weeks) at 3 customer warehouse sites
- Safety validation at each gate (risk assessment updated)

# Risk Register Adjustments
- Safety hazards (pinch points, collision with humans)
- Integration failures (mechanical + electrical + software)
- Field trial issues (unexpected warehouse environments)
```

---

## Additional Resources

### Industry Standards by Sector

**Consumer Electronics**:
- IEC 60950-1 / IEC 62368-1 (product safety)
- IEC 60529 (IP ratings)
- IEC 61000 series (EMC)

**Medical Devices**:
- ISO 13485 (quality management)
- ISO 14971 (risk management)
- IEC 62304 (software lifecycle)
- IEC 62366 (usability engineering)
- ISO 10993 series (biocompatibility)

**Industrial / Robotics**:
- ISO 12100 (machinery safety)
- ISO 13849 (safety control systems)
- IEC 61508 (functional safety)
- ISO/TS 15066 (collaborative robots)

**IoT**:
- ETSI EN 303 645 (IoT security)
- OWASP IoT Top 10
- ISO/IEC 27001 (information security)

**Automotive**:
- ISO 26262 (functional safety)
- IATF 16949 (quality management)
- AEC-Q100 / AEC-Q200 (component qualification)

### European / Italian Resources

**Italian Regulatory Bodies**:
- **Ministero della Salute** - Medical devices
- **Ministero delle Imprese e del Made in Italy (MIMIT)** - CE marking, product safety

**European Resources**:
- EU Commission Product Safety: https://ec.europa.eu/info/business-economy-euro/product-safety-and-requirements_en
- European Database for Medical Devices (EUDAMED): https://ec.europa.eu/tools/eudamed
- CE Marking portal: https://single-market-economy.ec.europa.eu/single-market/ce-marking_en

---

## Questions to Ask When Customizing

**Before you customize templates, answer**:

1. **Industry Context**:
   - What industry best describes my product?
   - Are there hybrid aspects? (e.g., IoT medical device)

2. **Regulatory Landscape**:
   - What countries am I selling in?
   - What certifications are mandatory vs optional?
   - What is the regulatory timeline?

3. **Risk Profile**:
   - What is the consequence of failure? (Inconvenience / Financial loss / Injury / Death)
   - What is my risk tolerance?
   - What are the top 3 unique risks for my product?

4. **Timeline Constraints**:
   - Is there a hard deadline? (Trade show, seasonal demand, competitor launch)
   - How much flexibility do I have?
   - What phases can be compressed or extended?

5. **Team Composition**:
   - What unique roles do I need? (Regulatory, clinical, field service, etc.)
   - Do I have in-house expertise or need consultants?

6. **Business Model**:
   - B2C or B2B?
   - What is the expected product lifetime?
   - What post-launch support is required?

---

## Conclusion

**Remember**:
- **Start with base templates** - They provide solid foundation
- **Customize thoughtfully** - Add industry-specific requirements, don't just copy
- **Iterate** - Templates improve with each project
- **Share learnings** - Update templates based on lessons learned

**The goal is not perfect templates, but templates that help your team succeed.**

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit

---

## Feedback & Contributions

Found an industry we missed? Have better customization guidance?

- **GitHub Issues**: [Suggest improvements](https://github.com/kathegrima/hardware-pm-starter-kit/issues)
- **Discussions**: [Share your industry-specific insights](https://github.com/[username]/hardware-pm-starter-kit/discussions)
- **Pull Requests**: Contribute industry guides!

---

*"Good templates are universal. Great templates are customized to your context."*
