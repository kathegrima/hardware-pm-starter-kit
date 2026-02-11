# Product Requirements Document (PRD) Template

> **Hardware Product Requirements Document - Define what you're building before you build it**

---

**Navigation**: [🏠 Home](../) | [📋 All Templates](../templates/) | [📚 All Guides](../guides/)

---

## Document Information

| Field | Details |
|-------|---------|
| **Product Name** | [Enter product name] |
| **Version** | [e.g., v1.0 - Draft] |
| **Document Owner** | [Product Manager name] |
| **Date Created** | [YYYY-MM-DD] |
| **Last Updated** | [YYYY-MM-DD] |
| **Approval Status** | [ ] Draft   [ ] Under Review   [ ] Approved   [ ] Locked |
| **Target Launch** | [Q# YYYY] |

---

## 📋 Table of Contents

1. [Product Overview](#product-overview)
2. [Business Objectives](#business-objectives)
3. [Target Market & Users](#target-market--users)
4. [Success Metrics](#success-metrics)
5. [Product Scope](#product-scope)
6. [Functional Requirements](#functional-requirements)
   - Hardware Requirements
   - Software/Firmware Requirements
   - Mechanical Requirements
7. [Non-Functional Requirements](#non-functional-requirements)
8. [Design & Manufacturing Constraints](#design--manufacturing-constraints)
9. [Regulatory & Compliance](#regulatory--compliance)
10. [Testing & Validation](#testing--validation)
11. [Cost Targets](#cost-targets)
12. [Timeline & Milestones](#timeline--milestones)
13. [Dependencies & Risks](#dependencies--risks)
14. [Open Questions](#open-questions)
15. [Appendices](#appendices)

---

## Product Overview

### 1.1 Executive Summary

**Brief Description** (1-2 paragraphs):
[Describe your product in simple terms. What is it? What does it do? What problem does it solve?]

**Example**:
*The SmartSense Indoor Air Quality Monitor is a battery-powered sensor device that continuously measures CO2, PM2.5, temperature, humidity, and VOCs in indoor environments. Users receive real-time air quality data via a mobile app with notifications when air quality drops below healthy thresholds. The device is designed for health-conscious consumers, parents, and individuals with respiratory sensitivities.*

---

### 1.2 Problem Statement

**What problem are we solving?**
[Describe the customer pain point or market gap this product addresses]

**Who experiences this problem?**
[Primary users affected by this problem]

**Why now?**
[Market timing, trends, or regulatory changes that make this the right time]

---

### 1.3 Product Vision

**Long-term vision** (what could this product become?):
[Describe the ultimate vision for this product 2-3 years from now]

---

## Business Objectives

### 2.1 Strategic Goals

**What business objectives does this product support?**

- [ ] Enter new market segment: [specify]
- [ ] Replace aging product line: [specify which]
- [ ] Competitive response: [specify competitor/threat]
- [ ] Revenue growth: [target]
- [ ] Market share: [target %]
- [ ] Other: [describe]

---

### 2.2 Success Criteria

**How will we measure success?**

| Metric | Target | Timeframe |
|--------|--------|-----------|
| Units sold | [e.g., 50,000 units] | [Year 1] |
| Revenue | [e.g., €2.5M] | [Year 1] |
| Gross margin | [e.g., 45%] | [Ongoing] |
| Market share | [e.g., 15%] | [Year 2] |
| Customer satisfaction (NPS) | [e.g., >50] | [6 months post-launch] |
| Return rate | [e.g., <2%] | [Ongoing] |

---

## Target Market & Users

### 3.1 Target Market

**Primary Market**:
- **Geography**: [Countries/regions - e.g., EU, North America]
- **Market size**: [TAM - Total Addressable Market]
- **Market segment**: [B2C, B2B, prosumer, enterprise]

**Secondary Markets** (future expansion):
- [Additional geographies or segments]

---

### 3.2 User Personas

#### Persona 1: [Name/Title]

**Demographics**:
- Age: [range]
- Occupation: [e.g., office worker, parent, engineer]
- Income: [range]
- Tech savviness: [Low / Medium / High]

**Goals**:
- [What they want to achieve]
- [Why they would buy this product]

**Pain Points**:
- [Current frustrations or challenges]
- [What existing solutions don't address]

**Use Cases**:
1. **Use Case 1**: [Describe scenario - e.g., "Monitor air quality in child's bedroom overnight"]
2. **Use Case 2**: [Another scenario]

---

#### Persona 2: [Name/Title]

[Repeat structure above for additional personas]

---

## Success Metrics

### 4.1 Key Performance Indicators (KPIs)

**Product KPIs**:
- Battery life: [target - e.g., >6 months on single charge]
- Accuracy: [target - e.g., ±3% for CO2 readings]
- Response time: [target - e.g., <2 seconds for sensor readings]
- Reliability: [target - e.g., MTBF >50,000 hours]

**Business KPIs**:
- Cost per unit (COGS): [target - e.g., <€25]
- Manufacturing yield: [target - e.g., >95% at PVT]
- Time to market: [target - e.g., 14 months from kickoff]

**User Experience KPIs**:
- App ratings: [target - e.g., >4.5 stars]
- Daily active users: [target - e.g., 60% of owners]
- Support ticket rate: [target - e.g., <5% of units]

---

## Product Scope

### 5.1 In Scope (MVP / Version 1.0)

**What features and functionality WILL be included in this version?**

✅ **Core Features**:
1. [Feature 1 - e.g., Real-time CO2 monitoring]
2. [Feature 2 - e.g., Temperature and humidity sensing]
3. [Feature 3 - e.g., Mobile app with notifications]
4. [Feature 4 - e.g., Historical data logging (7 days)]
5. [Feature 5 - e.g., USB-C charging]

✅ **User Experience**:
- [UX element 1 - e.g., LED indicator for air quality status]
- [UX element 2 - e.g., Setup via mobile app]

✅ **Packaging & Accessories**:
- [Item 1 - e.g., Retail box with product images]
- [Item 2 - e.g., USB-C cable included]
- [Item 3 - e.g., Quick start guide]

---

### 5.2 Out of Scope (Future Versions)

**What features will NOT be included in this version?**

❌ **Deferred Features** (V2.0 or later):
1. [Feature - e.g., Voice assistant integration]
2. [Feature - e.g., Cloud data storage beyond 7 days]
3. [Feature - e.g., Multiple device sync]

**Rationale**: [Briefly explain why these are deferred - time, cost, complexity, market validation needed]

---

### 5.3 Assumptions

**Key assumptions we're making**:
- [Assumption 1 - e.g., Users have smartphones (iOS 14+ or Android 10+)]
- [Assumption 2 - e.g., WiFi available in target environments]
- [Assumption 3 - e.g., Component X available with 12-week lead time]

---

## Functional Requirements

### 6.1 Hardware Requirements

#### 6.1.1 Electronics / PCB

**Processor / MCU**:
- **Requirement**: [e.g., ARM Cortex-M4 or equivalent, >80 MHz]
- **Rationale**: [Why this spec is needed]

**Wireless Communication**:
- [ ] Bluetooth: [version - e.g., BLE 5.0]
- [ ] WiFi: [standard - e.g., 802.11 b/g/n, 2.4 GHz]
- [ ] Cellular: [if applicable]
- [ ] Other: [specify]
- **Range requirement**: [e.g., >10 meters for BLE]

**Sensors**:

| Sensor Type | Specification | Accuracy | Rationale |
|-------------|--------------|----------|-----------|
| CO2 | [e.g., NDIR sensor, 0-5000 ppm range] | [±50 ppm ±3%] | [Indoor air quality monitoring] |
| Temperature | [e.g., -10°C to +60°C] | [±0.5°C] | [Environmental comfort] |
| Humidity | [e.g., 0-100% RH] | [±3%] | [Environmental comfort] |
| PM2.5 | [e.g., Laser scattering, 0-500 μg/m³] | [±10%] | [Particulate matter detection] |

**Power Management**:
- **Power source**: [e.g., Rechargeable Li-ion battery, 3.7V, 2000mAh]
- **Battery life target**: [e.g., >6 months on single charge with 5-min sampling interval]
- **Charging**: [e.g., USB-C, 5V/1A, <4 hours full charge]
- **Low battery indicator**: [e.g., LED warning at <10%]
- **Sleep/wake behavior**: [describe]

**Display / Indicators**:
- [ ] LCD/OLED display: [size, resolution]
- [ ] LED indicators: [quantity, colors, meaning]
- [ ] E-ink display: [if applicable]
- **Requirement**: [e.g., RGB LED to show air quality status - green/yellow/red]

**User Interface**:
- [ ] Physical buttons: [quantity, function]
- [ ] Touch interface: [capacitive, resistive]
- [ ] Voice control: [if applicable]
- **Requirement**: [e.g., Single button for power on/off and pairing mode]

**Data Storage**:
- **Internal memory**: [e.g., 512 KB flash for 7 days of data logging]
- **External storage**: [e.g., microSD slot - optional]

**Connectivity Ports**:
- [ ] USB-C: [data + charging]
- [ ] Micro-USB: [charging only]
- [ ] 3.5mm audio jack: [if applicable]
- [ ] Other: [specify]

---

#### 6.1.2 Mechanical / Enclosure Requirements

**Dimensions**:
- **Target size**: [L × W × H - e.g., 80mm × 80mm × 30mm]
- **Weight**: [target - e.g., <150 grams]
- **Rationale**: [e.g., Small enough to fit on nightstand, portable]

**Materials**:
- **Primary material**: [e.g., ABS plastic]
- **Surface finish**: [e.g., Matte texture]
- **Color options**: [e.g., White, Black]
- **Rationale**: [e.g., ABS for cost, durability, and ease of molding]

**Mounting / Installation**:
- [ ] Desktop/tabletop: [freestanding]
- [ ] Wall-mount: [bracket included]
- [ ] Magnetic mount: [if applicable]
- [ ] Adhesive mount: [if applicable]
- **Requirement**: [describe mounting method and hardware]

**Durability**:
- **Drop test**: [e.g., Survive 1-meter drop onto hard surface]
- **Ingress Protection (IP) rating**: [e.g., IP42 - dust protection, splash resistant]
- **Operating temperature**: [e.g., 0°C to +40°C]
- **Storage temperature**: [e.g., -20°C to +60°C]
- **Humidity tolerance**: [e.g., 10-90% RH, non-condensing]

**Aesthetics / Industrial Design**:
- **Design language**: [e.g., Minimalist, modern, rounded edges]
- **Branding**: [logo placement, engraving vs label]
- **User-facing surfaces**: [smooth, accessible]

**Thermal Management**:
- **Heat dissipation**: [e.g., Passive cooling via vents]
- **Maximum internal temperature**: [e.g., <60°C during operation]

---

### 6.2 Software / Firmware Requirements

**Firmware (Embedded Software)**:

**Core Functionality**:
1. **Sensor data acquisition**: [e.g., Poll sensors every 5 minutes]
2. **Data processing**: [e.g., Moving average filter for noise reduction]
3. **Data storage**: [e.g., Store readings locally for 7 days]
4. **Wireless communication**: [e.g., BLE GATT profile for app connection]
5. **Power management**: [e.g., Enter deep sleep between readings]

**Firmware Updates**:
- **OTA (Over-The-Air) updates**: [Required / Not required]
- **Update mechanism**: [e.g., Via mobile app over BLE]
- **Rollback capability**: [Yes / No]

**Companion Mobile App**:

**Platforms**:
- [ ] iOS: [minimum version - e.g., iOS 14+]
- [ ] Android: [minimum version - e.g., Android 10+]

**Core Features**:
1. **Device setup**: [e.g., BLE pairing, WiFi configuration]
2. **Real-time data display**: [e.g., Current CO2, temp, humidity]
3. **Historical data**: [e.g., Charts for last 7 days]
4. **Notifications**: [e.g., Push alerts when CO2 >1000 ppm]
5. **Settings**: [e.g., Alert thresholds, units (°C/°F)]

**User Authentication** (if applicable):
- [ ] Not required (local device only)
- [ ] Optional account creation
- [ ] Required account creation
- **Rationale**: [e.g., Not required to reduce friction, all data local]

**Cloud Services** (if applicable):
- [ ] Cloud data storage
- [ ] Remote access
- [ ] Data analytics
- [ ] Multi-device management
- **Requirement**: [describe cloud backend needs]

---

## Non-Functional Requirements

### 7.1 Performance

| Aspect | Requirement | Acceptance Criteria |
|--------|-------------|---------------------|
| **Boot time** | [e.g., <5 seconds from power-on to operational] | Device ready to measure within 5 seconds |
| **Sensor response time** | [e.g., <30 seconds to detect air quality change] | CO2 reading updates within 30 seconds of air composition change |
| **App launch time** | [e.g., <2 seconds to home screen] | App displays data within 2 seconds of tap |
| **Data sync** | [e.g., <10 seconds to sync latest readings to app] | New data appears in app within 10 seconds of connection |
| **Battery efficiency** | [e.g., >6 months battery life] | Device operates for 6+ months on single charge (5-min interval sampling) |

---

### 7.2 Reliability

| Aspect | Requirement | Acceptance Criteria |
|--------|-------------|---------------------|
| **MTBF (Mean Time Between Failures)** | [e.g., >50,000 hours] | Statistical analysis shows <2% failure rate over 5 years |
| **Sensor accuracy over time** | [e.g., <5% drift per year] | Calibration remains within ±5% for 1 year |
| **Firmware stability** | [e.g., No crashes for 1000+ hours continuous operation] | Firmware testing shows zero crashes in 1000-hour stress test |

---

### 7.3 Usability

| Aspect | Requirement | Acceptance Criteria |
|--------|-------------|---------------------|
| **Setup time** | [e.g., <5 minutes from unboxing to first reading] | 9 out of 10 users complete setup in <5 minutes (user testing) |
| **User comprehension** | [e.g., >80% of users understand air quality indicators without manual] | User testing shows 80%+ correctly interpret LED colors |
| **Accessibility** | [e.g., Colorblind-friendly indicators] | LED + app use shape/text in addition to color |

---

### 7.4 Scalability

**Manufacturing scalability**:
- **Initial production run**: [e.g., 5,000 units]
- **Annual volume target**: [e.g., 50,000 units by Year 2]
- **Manufacturing location**: [e.g., Contract manufacturer in Shenzhen, China]

**Cloud scalability** (if applicable):
- **Concurrent users**: [e.g., Support 10,000 simultaneous connections]
- **Data throughput**: [e.g., Handle 1M data points per day]

---

### 7.5 Security

**Data security**:
- [ ] BLE pairing: [e.g., Secure pairing with PIN]
- [ ] WiFi: [e.g., WPA2/WPA3 encryption]
- [ ] Data transmission: [e.g., TLS 1.2+ for cloud communication]
- [ ] User data: [e.g., No personally identifiable information (PII) collected]

**Firmware security**:
- [ ] Signed firmware updates: [Required / Not required]
- [ ] Secure boot: [Required / Not required]

---

## Design & Manufacturing Constraints

### 8.1 Design for Manufacturing (DFM)

**PCB Design**:
- **Layer count**: [e.g., 4-layer PCB]
- **Board size**: [e.g., <70mm × 70mm]
- **Component density**: [e.g., Standard SMT components, no BGA if possible]
- **Assembly process**: [e.g., Reflow soldering, automated pick-and-place]

**Enclosure / Mechanical**:
- **Manufacturing process**: [e.g., Injection molding]
- **Tooling cost budget**: [e.g., <€80,000 for all molds]
- **Minimum wall thickness**: [e.g., 1.5mm for structural integrity]
- **Draft angles**: [e.g., 3° for easy demolding]
- **Snap fits vs screws**: [e.g., Snap-fit assembly to reduce cost]

---

### 8.2 Component Selection Guidelines

**Preferred suppliers**:
- [e.g., Digi-Key, Mouser, Arrow for standard components]
- [e.g., Direct from manufacturer for custom/high-volume parts]

**Lifecycle requirements**:
- [ ] All components must be Active (not NRND)
- [ ] Prefer automotive-grade or industrial-grade for longevity
- [ ] Second-source available for all critical ICs

**Lead time constraints**:
- **Maximum acceptable lead time**: [e.g., 16 weeks]
- **Long-lead items**: [list components with >12-week lead times]

---

### 8.3 Supply Chain

**Contract Manufacturer (CM)**:
- **Preferred region**: [e.g., Asia, Europe]
- **CM capabilities required**: [e.g., SMT, final assembly, testing, packaging]
- **Quality certifications**: [e.g., ISO 9001, ISO 13485 if medical]

**Logistics**:
- **Shipping method**: [e.g., Air freight for first batch, sea freight for volume]
- **Fulfillment**: [e.g., Amazon FBA, direct-to-consumer, distributor network]

---

## Regulatory & Compliance

### 9.1 Certifications Required

**By Market**:

| Market | Certifications Required | Timeline | Estimated Cost |
|--------|------------------------|----------|----------------|
| **European Union** | CE (RED), RoHS, REACH | [Q# YYYY] | [€15,000] |
| **United States** | FCC Part 15 (Class B), Energy Star (optional) | [Q# YYYY] | [€10,000] |
| **Other** | [e.g., IC (Canada), RCM (Australia)] | [Q# YYYY] | [€5,000] |

---

### 9.2 Safety Standards

**Electrical safety**:
- [ ] IEC 62368-1 (Audio/Video equipment)
- [ ] IEC 60950-1 (IT equipment)
- [ ] UL 60950-1 (US)
- **Testing**: [e.g., External lab testing required before production]

**EMC (Electromagnetic Compatibility)**:
- [ ] EN 55032 (Emissions)
- [ ] EN 55035 (Immunity)
- [ ] FCC Part 15 (Radiated emissions)
- **Pre-compliance testing**: [Required in DVT phase]

---

### 9.3 Environmental Compliance

- [ ] **RoHS** (Restriction of Hazardous Substances): No lead, mercury, cadmium, etc.
- [ ] **REACH** (EU chemical regulations): Declaration of Substances of Very High Concern (SVHC)
- [ ] **WEEE** (Waste Electrical and Electronic Equipment): Recycling symbol on product
- [ ] **California Prop 65**: Warning labels if applicable
- [ ] **Battery regulations**: UN 38.3 testing for Li-ion batteries (shipping)

---

### 9.4 Labeling & Marking

**Required markings on product**:
- [ ] CE mark (EU)
- [ ] FCC ID (US)
- [ ] Manufacturer name and address
- [ ] Model number
- [ ] Serial number or batch code
- [ ] Electrical ratings (input voltage, power)
- [ ] Safety warnings
- [ ] Recycling symbols (WEEE, battery disposal)

---

## Testing & Validation

### 10.1 Test Strategy

**EVT (Engineering Validation Test) - Phase 1**:
- **Goal**: Prove core functionality
- **Quantity**: [e.g., 10-20 prototypes]
- **Key tests**:
  1. Sensor accuracy validation
  2. Power consumption measurement
  3. Wireless range testing
  4. Firmware functionality testing

**DVT (Design Validation Test) - Phase 2**:
- **Goal**: Validate design meets all specs
- **Quantity**: [e.g., 50-100 units]
- **Key tests**:
  1. Environmental testing (temperature, humidity)
  2. Drop testing
  3. EMC pre-compliance testing
  4. User experience validation (beta testing)
  5. Battery life validation

**PVT (Production Validation Test) - Phase 3**:
- **Goal**: Validate manufacturing readiness
- **Quantity**: [e.g., 200-500 units]
- **Key tests**:
  1. Manufacturing yield analysis
  2. Final compliance testing (CE, FCC)
  3. Packaging and logistics validation
  4. Quality control process validation

---

### 10.2 Environmental Testing

| Test | Standard | Specification | Pass Criteria |
|------|----------|--------------|---------------|
| **Temperature cycling** | IEC 60068-2-14 | [e.g., -10°C to +60°C, 10 cycles] | No functional degradation |
| **Humidity** | IEC 60068-2-78 | [e.g., 85% RH, 40°C, 48 hours] | No corrosion, maintains function |
| **Vibration** | IEC 60068-2-6 | [e.g., 10-500 Hz, 1 hour per axis] | No mechanical failure |
| **Drop test** | IEC 60068-2-31 | [e.g., 1 meter drop, 6 orientations] | Operational after drops |
| **ESD (Electrostatic Discharge)** | IEC 61000-4-2 | [e.g., ±8 kV contact, ±15 kV air] | No damage, self-recovers |

---

### 10.3 Acceptance Criteria

**How do we define "pass"?**

For each requirement listed in Section 6 (Functional Requirements) and Section 7 (Non-Functional Requirements), define measurable acceptance criteria.

**Example**:
- **Requirement**: Battery life >6 months
- **Acceptance Criteria**: Device operates for >4,380 hours (6 months × 30 days × 24 hours) in continuous test with 5-minute sampling interval, temperature controlled at 23°C ±2°C

---

## Cost Targets

### 11.1 Bill of Materials (BOM) Cost

**Target COGS (Cost of Goods Sold)**:

| Component Category | Target Cost | % of Total |
|--------------------|-------------|------------|
| PCB (fabrication + assembly) | [e.g., €8.00] | [32%] |
| Electronic components | [e.g., €10.00] | [40%] |
| Enclosure (injection molded parts) | [e.g., €3.00] | [12%] |
| Battery | [e.g., €2.00] | [8%] |
| Packaging | [e.g., €1.50] | [6%] |
| Accessories (cable, manual) | [e.g., €0.50] | [2%] |
| **Total COGS** | **€25.00** | **100%** |

**Target margin**: [e.g., 45% gross margin → retail price €45]

---

### 11.2 Non-Recurring Engineering (NRE) Costs

| Item | Estimated Cost |
|------|----------------|
| Engineering design (hardware, firmware, mechanical) | [e.g., €80,000] |
| Prototyping (EVT, DVT, PVT builds) | [e.g., €30,000] |
| Tooling (injection molds, jigs, fixtures) | [e.g., €80,000] |
| Certifications (CE, FCC, testing) | [e.g., €30,000] |
| App development (iOS, Android) | [e.g., €50,000] |
| **Total NRE** | **€270,000** |

---

## Timeline & Milestones

### 12.1 Development Phases

| Phase | Duration | Start Date | End Date | Key Deliverables |
|-------|----------|------------|----------|------------------|
| **Concept** | [4 weeks] | [YYYY-MM-DD] | [YYYY-MM-DD] | PRD approved, initial BOM, feasibility confirmed |
| **EVT** | [12 weeks] | [YYYY-MM-DD] | [YYYY-MM-DD] | Functional prototype, core specs validated |
| **DVT** | [16 weeks] | [YYYY-MM-DD] | [YYYY-MM-DD] | Production-intent design, compliance pre-testing passed |
| **PVT** | [10 weeks] | [YYYY-MM-DD] | [YYYY-MM-DD] | Manufacturing validated, certifications complete |
| **MP (Mass Production)** | [Ongoing] | [YYYY-MM-DD] | [Ongoing] | First production batch shipped |

**Total timeline**: [e.g., 14 months from kickoff to first customer shipment]

---

### 12.2 Key Milestones

- [ ] **PRD Approval**: [Date]
- [ ] **EVT Build Complete**: [Date]
- [ ] **Design Freeze**: [Date] *(no changes without CCB approval after this)*
- [ ] **DVT Build Complete**: [Date]
- [ ] **Tooling Kickoff**: [Date]
- [ ] **Compliance Testing Complete**: [Date]
- [ ] **PVT Build Complete**: [Date]
- [ ] **Manufacturing Ramp**: [Date]
- [ ] **First Customer Shipment**: [Date]

---

## Dependencies & Risks

### 13.1 Dependencies

**External Dependencies**:
1. **Component availability**: [e.g., CO2 sensor lead time 16 weeks]
2. **Contract manufacturer capacity**: [e.g., CM needs 4-week notice for production slot]
3. **Certification lab availability**: [e.g., FCC testing lab booked 6 weeks in advance]
4. **App store approval**: [e.g., Apple App Store 2-week review]

**Internal Dependencies**:
1. **Firmware team bandwidth**: [e.g., Firmware engineer allocated 50% to this project]
2. **Industrial design finalization**: [e.g., ID must be locked by Week 8 for tooling]

---

### 13.2 Risk Register

| Risk | Probability | Impact | Mitigation Strategy |
|------|-------------|--------|---------------------|
| **Component goes EOL during development** | Medium | High | Select components with Active status, identify second sources early |
| **Certification testing fails at DVT** | Medium | High | Pre-compliance testing in EVT phase, engage test lab early for guidance |
| **Battery life doesn't meet target** | High | Medium | Optimize firmware for low power, test early prototypes, have backup battery option |
| **Tooling cost exceeds budget** | Medium | Medium | Get quotes from 3 mold makers, simplify mechanical design if needed |
| **Manufacturing yield <95% at PVT** | Medium | High | DFM review in DVT, close collaboration with CM, dry runs before PVT |

---

## Open Questions

**Unresolved items that need answers before proceeding**:

1. [ ] **Question**: [e.g., Do we need IP54 rating or is IP42 sufficient?]
   - **Owner**: [Name]
   - **Target Resolution Date**: [Date]

2. [ ] **Question**: [e.g., Should we support both Bluetooth and WiFi, or Bluetooth only?]
   - **Owner**: [Name]
   - **Target Resolution Date**: [Date]

3. [ ] **Question**: [e.g., What is the maximum acceptable retail price based on market research?]
   - **Owner**: [Name]
   - **Target Resolution Date**: [Date]

---

## Appendices

### Appendix A: Competitive Analysis

| Competitor | Product | Price | Key Features | Strengths | Weaknesses | Our Differentiation |
|------------|---------|-------|--------------|-----------|------------|---------------------|
| [Competitor A] | [Model X] | [€50] | [CO2, temp, humidity] | [Established brand] | [No PM2.5, poor app] | [We add PM2.5, better UX] |
| [Competitor B] | [Model Y] | [€80] | [Full sensors, cloud] | [Feature-rich] | [Expensive, complex] | [Simpler, more affordable] |

---

### Appendix B: User Research Summary

**Key findings from user interviews** (link to full report):
- [Finding 1 - e.g., 80% of users want simple LED indicator, don't check app daily]
- [Finding 2 - e.g., Battery life more important than cloud features]
- [Finding 3 - e.g., Price sensitivity: most won't pay >€50]

---

### Appendix C: Supporting Documents

**Links to additional resources**:
- [ ] Initial sketches / concept renders
- [ ] CAD files (when available)
- [ ] Component datasheets
- [ ] Market research report
- [ ] BOM spreadsheet (living document)
- [ ] Risk register (detailed version)

---

### Appendix D: Glossary

**Technical terms used in this document**:

- **BLE**: Bluetooth Low Energy
- **COGS**: Cost of Goods Sold (per-unit manufacturing cost)
- **DFM**: Design for Manufacturability
- **EMC**: Electromagnetic Compatibility
- **EVT/DVT/PVT**: Engineering/Design/Production Validation Test
- **IP Rating**: Ingress Protection (dust/water resistance)
- **MTBF**: Mean Time Between Failures
- **NDIR**: Non-Dispersive Infrared (CO2 sensor technology)
- **NRE**: Non-Recurring Engineering (one-time development costs)
- **OTA**: Over-The-Air (firmware updates)
- **PM2.5**: Particulate Matter 2.5 micrometers (air pollution metric)
- **SMT**: Surface Mount Technology (PCB assembly)
- **VOC**: Volatile Organic Compounds

---

## Document Approval

**Approval Sign-Offs**:

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Product Manager** | [Name] | _____________ | [Date] |
| **Engineering Lead** | [Name] | _____________ | [Date] |
| **Manufacturing Lead** | [Name] | _____________ | [Date] |
| **Business Owner** | [Name] | _____________ | [Date] |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| v0.1 | [Date] | [Name] | Initial draft |
| v0.5 | [Date] | [Name] | Added hardware specs after feasibility study |
| v1.0 | [Date] | [Name] | Final version for EVT kickoff - APPROVED |

---

**END OF PRD**

---

## How to Use This Template

1. **Start Early**: Begin drafting the PRD during the Concept phase, before significant engineering work begins.

2. **Be Specific**: Replace all `[bracketed placeholders]` with actual values. Vague requirements lead to expensive rework.

3. **Make it Measurable**: Every requirement should have clear acceptance criteria. "Good battery life" is not a requirement; ">6 months on single charge" is.

4. **Prioritize Ruthlessly**: Use the Scope section to clearly define what's in MVP vs future versions. You can't build everything at once.

5. **Keep it Updated**: The PRD is NOT a static document. Update it as you learn during prototyping—but use formal change control after Design Freeze.

6. **Socialize It**: Share the PRD with all stakeholders (engineering, manufacturing, quality, business, marketing) and get feedback BEFORE locking the design.

7. **Link to Details**: Don't try to fit everything in the PRD. Link to supporting documents (BOM spreadsheet, CAD files, test plans) in Appendices.

8. **Lock Before Tooling**: Once you commit to hard tooling ($50K-$500K investment), the PRD should be locked. Changes after tooling are extremely expensive.

---

**Template Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit

---

*"A good PRD prevents expensive late-stage surprises. A great PRD aligns the entire organization on what success looks like."*
