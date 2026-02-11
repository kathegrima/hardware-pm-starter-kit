# Test Plan Template

> **Comprehensive testing strategy for hardware validation**

---

## Table of Contents

1. [Introduction](#introduction)
2. [Test Plan Overview](#test-plan-overview)
3. [Test Strategy by Phase](#test-strategy-by-phase)
4. [Functional Testing](#functional-testing)
5. [Environmental Testing](#environmental-testing)
6. [Compliance Testing](#compliance-testing)
7. [Reliability Testing](#reliability-testing)
8. [Manufacturing Testing](#manufacturing-testing)
9. [Test Documentation](#test-documentation)
10. [Test Execution & Tracking](#test-execution--tracking)

---

## Introduction

### Purpose

A test plan defines **what to test, how to test, and when to test** throughout hardware development. Comprehensive testing ensures:
- Product meets requirements (functional, performance, environmental)
- Design is robust and reliable (MTBF, failure modes)
- Manufacturing is repeatable (yield, quality)
- Compliance requirements met (CE, FCC, safety)

---

### Test Plan Structure

**This template covers**:
1. **Phase-specific testing** - EVT, DVT, PVT
2. **Test types** - Functional, environmental, compliance, reliability
3. **Test procedures** - Step-by-step instructions
4. **Pass/fail criteria** - Clear acceptance criteria
5. **Test tracking** - Status, results, issues

---

### Document Information

| Field | Details |
|-------|---------|
| **Project Name** | [Enter project name] |
| **Product Name** | [Enter product name] |
| **Test Plan Version** | [e.g., v1.0] |
| **Author** | [Name] |
| **Date Created** | [YYYY-MM-DD] |
| **Last Updated** | [YYYY-MM-DD] |
| **Approver** | [Name, Title] |
| **Approval Date** | [YYYY-MM-DD] |

---

## Test Plan Overview

### Product Under Test

**Product Description**: [Brief description of product]

**Key Specifications**:
- Operating Voltage: [e.g., 5V DC]
- Power Consumption: [e.g., <500mW]
- Battery Life: [e.g., >6 months]
- Operating Temperature: [e.g., 0°C to +40°C]
- Wireless: [e.g., WiFi 2.4GHz, Bluetooth 5.0]
- Sensors: [e.g., CO2, temperature, humidity]
- Dimensions: [e.g., 100×80×30mm]
- Weight: [e.g., 150g]

---

### Test Objectives

**Primary Objectives**:
1. Validate product meets all functional requirements (PRD compliance)
2. Verify performance specifications (accuracy, speed, battery life)
3. Confirm environmental robustness (temperature, humidity, drop, vibration)
4. Demonstrate compliance with regulations (CE, FCC, RoHS)
5. Establish reliability baseline (MTBF, failure modes)
6. Validate manufacturing process (yield, quality, repeatability)

**Success Criteria**:
- [ ] All functional tests pass (100% feature coverage)
- [ ] Performance within specification (±10% tolerance)
- [ ] Environmental tests pass (no failures at extreme conditions)
- [ ] Compliance tests pass (EMC, safety, RoHS)
- [ ] Reliability target met (MTBF >50,000 hours)
- [ ] Manufacturing yield >95%

---

### Test Scope

**In Scope**:
- [ ] Hardware functional testing (all features)
- [ ] Firmware functional testing (integrated with hardware)
- [ ] Performance characterization (speed, accuracy, power)
- [ ] Environmental testing (temperature, humidity, drop, vibration)
- [ ] EMC testing (emissions, immunity)
- [ ] Safety testing (LVD if applicable)
- [ ] RoHS compliance testing
- [ ] Reliability testing (ALT, HALT, power cycling)
- [ ] User acceptance testing (beta testing)

**Out of Scope**:
- [ ] Standalone firmware testing (covered in separate SW test plan)
- [ ] Mobile app testing (separate test plan)
- [ ] Cloud infrastructure testing (separate test plan)
- [ ] Full production qualification (covered in PVT phase)

---

### Test Resources

**Equipment Required**:
| Equipment | Quantity | Purpose | Location |
|-----------|----------|---------|----------|
| Oscilloscope | 1 | Signal integrity, debugging | Lab |
| Multimeter | 2 | Voltage, current measurements | Lab |
| Power supply | 2 | Power testing, stress testing | Lab |
| Thermal chamber | 1 | Temperature testing (-10°C to +50°C) | Lab or external |
| Humidity chamber | 1 | Humidity testing (10-90% RH) | External lab |
| Vibration table | 1 | Vibration testing | External lab |
| Drop tester | 1 | Drop testing | External lab |
| EMC chamber | 1 | EMC pre-compliance | External lab |

**Personnel**:
| Role | Name | Responsibility | Allocation |
|------|------|---------------|------------|
| Test Lead | [Name] | Overall test execution, reporting | 100% |
| Hardware Engineer | [Name] | Hardware debugging, root cause analysis | 50% |
| Firmware Engineer | [Name] | Firmware debugging, test automation | 50% |
| QA Engineer | [Name] | Test execution, documentation | 100% |
| Technician | [Name] | Sample preparation, lab support | 50% |

**Test Samples**:
| Phase | Quantity | Configuration | Notes |
|-------|----------|---------------|-------|
| EVT | 10-20 units | Functional prototypes | Hand-assembled, expect issues |
| DVT | 50-100 units | Production-intent | From CM, soft-tooled enclosures |
| PVT | 200-500 units | Production units | From CM, hard-tooled, final design |

---

## Test Strategy by Phase

### EVT Phase Testing (Weeks 5-16)

**Objective**: Prove core functionality, retire major technical risks

**Testing Focus**:
- ✅ **Functional testing** - Do all features work?
- ✅ **Performance characterization** - Measure speed, accuracy, power
- ✅ **Thermal testing** - Check component temperatures at ambient
- ✅ **Basic environmental** - Test at 0°C and +40°C
- ✅ **Hardware-firmware integration** - HW+FW work together?

**Test Types**:
| Test Type | Priority | Est. Duration | Pass Criteria |
|-----------|----------|---------------|---------------|
| Functional (core features) | High | 2 weeks | All core features work |
| Power consumption | High | 1 week | Within 20% of target |
| Battery life estimate | Medium | 1 week | >4 months (target 6 months) |
| Thermal (ambient) | High | 3 days | All components <80°C at 25°C |
| Temperature extremes | Medium | 1 week | Functions at 0°C and +40°C |

**Deliverables**:
- [ ] EVT test report (functional, performance, thermal)
- [ ] Known issues list (bugs, limitations, failures)
- [ ] Risk assessment update (risks retired or elevated)

---

### DVT Phase Testing (Weeks 17-32)

**Objective**: Comprehensive validation, design freeze decision

**Testing Focus**:
- ✅ **Full functional testing** - 100% feature coverage
- ✅ **Environmental testing** - Temperature, humidity, drop, vibration
- ✅ **Compliance pre-testing** - EMC, safety (pre-cert)
- ✅ **Reliability testing** - ALT, power cycling
- ✅ **User acceptance testing** - Beta testing with 20+ users

**Test Types**:
| Test Type | Priority | Est. Duration | Pass Criteria |
|-----------|----------|---------------|---------------|
| Functional (all features) | High | 3 weeks | 100% pass rate |
| Environmental (full suite) | High | 4 weeks | All tests pass |
| EMC pre-compliance | Critical | 1 week | <6dB margin to limits |
| Reliability (ALT) | Medium | 2 weeks | No early-life failures |
| User acceptance (beta) | High | 4 weeks | NPS >50, <5% critical issues |

**Deliverables**:
- [ ] DVT test report (comprehensive, all test types)
- [ ] Environmental test report (temp, humidity, drop, vibration)
- [ ] EMC pre-compliance report (margin analysis)
- [ ] Beta testing report (user feedback, issues)
- [ ] Design freeze recommendation (Go/No-Go)

---

### PVT Phase Testing (Weeks 33-48)

**Objective**: Validate manufacturing process and final product quality

**Testing Focus**:
- ✅ **Manufacturing validation** - Yield, cycle time, quality
- ✅ **Compliance testing** - Official EMC, LVD, RED, RoHS
- ✅ **End-of-line testing** - Functional test, calibration
- ✅ **Burn-in testing** - 48-hour burn-in on sample
- ✅ **Packaging testing** - Drop test packaged units

**Test Types**:
| Test Type | Priority | Est. Duration | Pass Criteria |
|-----------|----------|---------------|---------------|
| First article inspection | Critical | 1 week | Matches DVT design |
| Manufacturing yield | Critical | 4 weeks | >95% first-pass yield |
| End-of-line test | Critical | 2 weeks | <5 minute cycle time, >95% coverage |
| Compliance (official) | Critical | 6 weeks | All tests pass (EMC, LVD, RED, RoHS) |
| Packaging drop test | Medium | 1 week | No damage after 1m drop (6 orientations) |

**Deliverables**:
- [ ] PVT test report (manufacturing validation)
- [ ] First article inspection report
- [ ] Compliance test reports (official)
- [ ] End-of-line test procedure (validated)
- [ ] Manufacturing release approval

---

## Functional Testing

### Test Case Template

**Test Case ID**: FT-XXX  
**Test Name**: [Descriptive name]  
**Objective**: [What this test validates]  
**Priority**: [ ] Critical [ ] High [ ] Medium [ ] Low  
**Test Type**: [ ] Manual [ ] Automated [ ] Semi-automated

**Prerequisites**:
- [ ] Device fully charged / powered
- [ ] Firmware version: [X.Y.Z]
- [ ] Test equipment: [List equipment needed]
- [ ] Environmental conditions: [e.g., 25°C, 50% RH]

**Test Procedure**:
1. [Step 1 - action]
2. [Step 2 - action]
3. [Step 3 - action]
...

**Expected Result**:
- [What should happen if test passes]

**Pass/Fail Criteria**:
- **Pass**: [Specific criteria for pass]
- **Fail**: [Specific criteria for fail]

**Actual Result**:
- [Record actual result during test execution]

**Status**: [ ] Not Run [ ] Pass [ ] Fail [ ] Blocked  
**Tested By**: [Name]  
**Date**: [YYYY-MM-DD]  
**Notes**: [Any observations, issues, deviations]

---

### Example Functional Tests

#### FT-001: Power On/Off

**Test Name**: Power On/Off  
**Objective**: Verify device powers on and off correctly  
**Priority**: Critical

**Test Procedure**:
1. Press power button for 2 seconds
2. Observe LED indicator and display
3. Wait 5 seconds for full boot
4. Press power button for 3 seconds to power off
5. Observe LED indicator and display turn off

**Expected Result**:
- Power on: LED blinks green, display shows boot screen, device fully boots in <5 seconds
- Power off: LED turns off, display turns off, device powers down in <3 seconds

**Pass/Fail Criteria**:
- **Pass**: Device powers on/off as expected, boot time <5s, shutdown time <3s
- **Fail**: Device doesn't respond, boot time >5s, shutdown time >3s, or unexpected behavior

---

#### FT-002: Sensor Reading Accuracy

**Test Name**: CO2 Sensor Reading Accuracy  
**Objective**: Verify CO2 sensor reads within ±5% of reference  
**Priority**: High

**Prerequisites**:
- Reference CO2 meter (calibrated, ±3% accuracy)
- Controlled environment chamber with adjustable CO2

**Test Procedure**:
1. Place device and reference meter in chamber
2. Set CO2 level to 800 ppm and stabilize for 10 minutes
3. Record device reading and reference reading
4. Repeat for 1000 ppm, 1500 ppm, 2000 ppm
5. Calculate accuracy: (Device Reading - Reference) / Reference × 100%

**Expected Result**:
- All readings within ±5% of reference

**Pass/Fail Criteria**:
- **Pass**: All readings within ±5% of reference
- **Fail**: Any reading outside ±5% of reference

**Test Data**:
| CO2 Level | Reference (ppm) | Device (ppm) | Error (%) | Pass/Fail |
|-----------|----------------|--------------|-----------|-----------|
| 800 ppm | _______ | _______ | _______ | [ ] Pass [ ] Fail |
| 1000 ppm | _______ | _______ | _______ | [ ] Pass [ ] Fail |
| 1500 ppm | _______ | _______ | _______ | [ ] Pass [ ] Fail |
| 2000 ppm | _______ | _______ | _______ | [ ] Pass [ ] Fail |

---

#### FT-003: Battery Life Test

**Test Name**: Battery Life Under Typical Use  
**Objective**: Verify battery lasts >6 months under typical use  
**Priority**: High

**Test Setup**:
- Fully charged device
- Typical use profile: Sample every 5 minutes, transmit every 30 minutes
- Ambient temperature: 25°C

**Test Procedure**:
1. Fully charge device (verify 100% charge)
2. Configure device for typical use profile
3. Monitor battery voltage every hour
4. Record time to low-battery warning (20%)
5. Record time to shutdown (5%)
6. Calculate battery life: (Time to 20%) × 1.25 = Estimated total life

**Expected Result**:
- Battery lasts >6 months (>4,320 hours)

**Pass/Fail Criteria**:
- **Pass**: Battery life >6 months
- **Fail**: Battery life <6 months

**Accelerated Testing** (if full 6-month test not feasible):
- Increase sampling frequency 10x (sample every 30 seconds)
- Run for 2 weeks (336 hours)
- Extrapolate: Measured life × 10 = Estimated actual life
- **Note**: Validate extrapolation with at least 3 units running full 6-month test

---

## Environmental Testing

### Temperature Testing

**Test Standard**: IEC 60068-2-1 (Cold), IEC 60068-2-2 (Dry Heat)

**Objective**: Verify device operates correctly at temperature extremes

**Test Conditions**:
| Test | Temperature | Duration | Cycles |
|------|-------------|----------|--------|
| Cold Storage | -20°C | 24 hours | 3 |
| Cold Operating | 0°C | 4 hours | 3 |
| Hot Storage | +60°C | 24 hours | 3 |
| Hot Operating | +50°C | 4 hours | 3 |
| Thermal Shock | -10°C to +50°C | 15 min each | 10 |

**Test Procedure**:
1. Place device in thermal chamber at test temperature
2. Stabilize for duration (storage) or operate device (operating)
3. Record any failures or anomalies
4. Return to ambient (25°C) and verify functionality
5. Repeat for all test conditions

**Pass/Fail Criteria**:
- **Pass**: Device operates correctly during and after each test, no physical damage
- **Fail**: Device fails to operate, incorrect readings, physical damage (cracking, warping)

**Test Report Template**:
| Test | Temp | Duration | Cycles | Result | Notes |
|------|------|----------|--------|--------|-------|
| Cold Storage | -20°C | 24h | 3 | [ ] Pass [ ] Fail | _______ |
| Cold Operating | 0°C | 4h | 3 | [ ] Pass [ ] Fail | _______ |
| Hot Storage | +60°C | 24h | 3 | [ ] Pass [ ] Fail | _______ |
| Hot Operating | +50°C | 4h | 3 | [ ] Pass [ ] Fail | _______ |
| Thermal Shock | -10/+50°C | 15min | 10 | [ ] Pass [ ] Fail | _______ |

---

### Humidity Testing

**Test Standard**: IEC 60068-2-30 (Damp Heat, Cyclic)

**Objective**: Verify device withstands high humidity conditions

**Test Conditions**:
- Temperature: +40°C
- Humidity: 93% RH
- Duration: 48 hours
- Cycles: 2 cycles (24 hours each)

**Test Procedure**:
1. Place device in humidity chamber (unpowered)
2. Set temperature to +40°C, humidity to 93% RH
3. Run for 48 hours (2 × 24h cycles)
4. Remove and dry at ambient for 4 hours
5. Power on and verify functionality

**Pass/Fail Criteria**:
- **Pass**: Device operates correctly after test, no condensation inside enclosure, no corrosion
- **Fail**: Device fails to operate, visible condensation, corrosion on components or connectors

---

### Drop Testing

**Test Standard**: IEC 60068-2-31 (Free Fall)

**Objective**: Verify device withstands typical drops

**Test Conditions**:
- Drop Height: 1.5 meters (simulates waist-height drop)
- Surface: Concrete or tile
- Orientations: 6 (top, bottom, 4 sides)
- Repetitions: 3 units × 6 orientations = 18 drops total

**Test Procedure**:
1. Inspect device before test (photo documentation)
2. Drop from 1.5m onto concrete in specified orientation
3. Inspect for physical damage (cracks, breaks, deformation)
4. Power on and verify functionality
5. Repeat for all 6 orientations
6. Record results for each drop

**Pass/Fail Criteria**:
- **Pass**: Device operates correctly after drops, cosmetic damage acceptable (scratches, scuffs), no cracks or structural damage
- **Fail**: Device fails to operate, enclosure cracks, internal damage (PCB crack, component detached)

**Test Report Template**:
| Unit | Orientation | Drop # | Physical Damage | Functional | Pass/Fail |
|------|-------------|--------|----------------|-----------|-----------|
| 1 | Top | 1 | _______ | [ ] Yes [ ] No | [ ] Pass [ ] Fail |
| 1 | Bottom | 2 | _______ | [ ] Yes [ ] No | [ ] Pass [ ] Fail |
| 1 | Side 1 | 3 | _______ | [ ] Yes [ ] No | [ ] Pass [ ] Fail |
| ... | ... | ... | _______ | [ ] Yes [ ] No | [ ] Pass [ ] Fail |

---

### Vibration Testing

**Test Standard**: IEC 60068-2-6 (Sinusoidal Vibration)

**Objective**: Verify device withstands shipping and handling vibration

**Test Conditions**:
- Frequency Range: 10-55 Hz
- Amplitude: 1.5 mm (peak-to-peak)
- Duration: 30 minutes per axis
- Axes: X, Y, Z (3 axes)

**Test Procedure**:
1. Mount device on vibration table
2. Apply sinusoidal vibration (10-55 Hz sweep)
3. Run for 30 minutes on X-axis
4. Repeat for Y-axis and Z-axis
5. Inspect and test functionality after each axis

**Pass/Fail Criteria**:
- **Pass**: Device operates correctly after test, no loose parts, no visible damage
- **Fail**: Device fails to operate, loose components, screws loosened, structural damage

---

## Compliance Testing

### EMC Testing

**Directive**: EMC Directive (2014/30/EU)  
**Standards**: EN 55032 (emissions), EN 55035 (immunity)

**Objective**: Verify device meets EMC emissions and immunity requirements

**Test Lab**: [Lab name, contact]  
**Test Date**: [Scheduled date]  
**Cost**: €[X,XXX]

**Emissions Tests**:
| Test | Standard | Limit | Margin Target | Result |
|------|----------|-------|---------------|--------|
| Conducted Emissions (150kHz-30MHz) | EN 55032 Class B | [Limit] | >6dB | [ ] Pass [ ] Fail |
| Radiated Emissions (30MHz-1GHz) | EN 55032 Class B | [Limit] | >6dB | [ ] Pass [ ] Fail |

**Immunity Tests**:
| Test | Standard | Level | Result |
|------|----------|-------|--------|
| ESD (Electrostatic Discharge) | EN 55035 | ±8kV contact, ±15kV air | [ ] Pass [ ] Fail |
| Radiated RF Immunity | EN 55035 | 10 V/m (80MHz-6GHz) | [ ] Pass [ ] Fail |
| Electrical Fast Transient (Burst) | EN 55035 | ±2kV | [ ] Pass [ ] Fail |
| Surge | EN 55035 | ±1kV | [ ] Pass [ ] Fail |

**Test Report**: [Link to official test report]

---

### LVD Testing (if applicable)

**Directive**: Low Voltage Directive (2014/35/EU)  
**Standards**: EN 62368-1 (IT equipment)

**Objective**: Verify device meets electrical safety requirements

**Applicable**: [ ] Yes (>50V AC or >75V DC) [ ] No

**Safety Tests**:
| Test | Standard | Limit | Result |
|------|----------|-------|--------|
| Leakage Current | EN 62368-1 | <0.5mA (handheld), <3.5mA (portable) | [ ] Pass [ ] Fail |
| Insulation Resistance | EN 62368-1 | >5MΩ | [ ] Pass [ ] Fail |
| Dielectric Strength | EN 62368-1 | 1500V AC for 1 minute | [ ] Pass [ ] Fail |
| Temperature Rise | EN 62368-1 | <65°C (external surfaces) | [ ] Pass [ ] Fail |
| Flammability | EN 62368-1 | V-0 or V-1 rating | [ ] Pass [ ] Fail |

**Test Report**: [Link to official test report]

---

### RED Testing (if wireless)

**Directive**: Radio Equipment Directive (2014/53/EU)  
**Standards**: EN 300 328 (2.4GHz), EN 301 489 (EMC for radio)

**Objective**: Verify radio performance and compliance

**Radio Tests**:
| Test | Standard | Limit/Requirement | Result |
|------|----------|------------------|--------|
| RF Power Output | EN 300 328 | <100mW EIRP (2.4GHz) | [ ] Pass [ ] Fail |
| Spurious Emissions | EN 300 328 | <1mW EIRP | [ ] Pass [ ] Fail |
| Receiver Blocking | EN 300 328 | [Level] | [ ] Pass [ ] Fail |
| EMC (Radio-specific) | EN 301 489 | [Requirements] | [ ] Pass [ ] Fail |
| SAR (if <20cm from body) | EN 50360 | <2 W/kg | [ ] Pass [ ] Fail [ ] N/A |

**Test Report**: [Link to official test report]

---

### RoHS Testing

**Directive**: RoHS Directive (2011/65/EU)  
**Standards**: EN IEC 63000:2018

**Objective**: Verify restricted substances are below limits

**Test Method**: XRF screening + ICP-OES/MS (if XRF shows high levels)

**Restricted Substances**:
| Substance | Limit (ppm) | Test Result (ppm) | Pass/Fail |
|-----------|-------------|-------------------|-----------|
| Lead (Pb) | 1000 | _______ | [ ] Pass [ ] Fail |
| Mercury (Hg) | 1000 | _______ | [ ] Pass [ ] Fail |
| Cadmium (Cd) | 100 | _______ | [ ] Pass [ ] Fail |
| Hexavalent Chromium (Cr6+) | 1000 | _______ | [ ] Pass [ ] Fail |
| PBB | 1000 | _______ | [ ] Pass [ ] Fail |
| PBDE | 1000 | _______ | [ ] Pass [ ] Fail |
| DEHP | 1000 | _______ | [ ] Pass [ ] Fail |
| BBP | 1000 | _______ | [ ] Pass [ ] Fail |
| DBP | 1000 | _______ | [ ] Pass [ ] Fail |
| DIBP | 1000 | _______ | [ ] Pass [ ] Fail |

**Test Report**: [Link to RoHS test report]

---

## Reliability Testing

### Accelerated Life Testing (ALT)

**Objective**: Estimate MTBF and identify early-life failure modes

**Test Conditions**:
- Temperature: +60°C (accelerated stress)
- Duration: 1000 hours (6 weeks continuous)
- Sample Size: 20 units
- Operating Mode: Continuous operation (worst-case duty cycle)

**Test Procedure**:
1. Select 20 units from DVT build
2. Configure for continuous operation
3. Place in thermal chamber at +60°C
4. Monitor every 24 hours for failures
5. Record failure time, failure mode, root cause
6. Calculate MTBF using Arrhenius model

**MTBF Calculation**:
```
Acceleration Factor (AF) = e^[(Ea/k) × (1/T_use - 1/T_test)]

Where:
- Ea = Activation energy (typically 0.7 eV for electronics)
- k = Boltzmann constant (8.617×10^-5 eV/K)
- T_use = Normal use temperature (298K = 25°C)
- T_test = Test temperature (333K = 60°C)

AF ≈ 4.5 (for 25°C to 60°C)

MTBF_actual = MTBF_test × AF
```

**Pass/Fail Criteria**:
- **Pass**: No failures during 1000 hours, estimated MTBF >50,000 hours
- **Fail**: >2 failures, estimated MTBF <50,000 hours

**Failure Tracking**:
| Unit | Time to Failure (hours) | Failure Mode | Root Cause | Corrective Action |
|------|------------------------|--------------|------------|-------------------|
| 1 | _______ | _______ | _______ | _______ |
| 2 | _______ | _______ | _______ | _______ |
| ... | _______ | _______ | _______ | _______ |

---

### HALT (Highly Accelerated Life Testing)

**Objective**: Find design margins and failure limits

**Test Conditions**:
- Temperature: Ramp from -40°C to +80°C (find limits)
- Vibration: 10-50 Grms (multi-axis)
- Combined stress: Temperature + vibration simultaneously

**Test Procedure**:
1. Start at ambient (25°C, no vibration)
2. Decrease temperature in 10°C steps, hold 10 minutes each
3. Increase temperature in 10°C steps, hold 10 minutes each
4. Apply vibration in 5 Grms increments
5. Combine temperature and vibration
6. Record failure points (destruct limits)

**Deliverables**:
- Operating limits (device still functions)
- Destruct limits (device fails permanently)
- Failure modes at each stress level
- Design margin analysis (operating range vs. limits)

---

### Power Cycling Test

**Objective**: Verify device withstands repeated power on/off cycles

**Test Conditions**:
- Cycles: 1000 on/off cycles
- On Time: 30 seconds
- Off Time: 30 seconds
- Sample Size: 5 units

**Test Procedure**:
1. Automate power cycling (relay or programmable power supply)
2. Run continuously for ~17 hours (1000 cycles)
3. Monitor for failures every 100 cycles
4. Record any failures or anomalies

**Pass/Fail Criteria**:
- **Pass**: All units complete 1000 cycles without failure
- **Fail**: Any unit fails before 1000 cycles

---

## Manufacturing Testing

### First Article Inspection (FAI)

**Objective**: Verify first production units match design

**Inspection Points**:
- [ ] PCB assembly matches schematic and BOM
- [ ] Component placement correct (reference designators)
- [ ] Solder joints quality (IPC-A-610 Class 2)
- [ ] Mechanical assembly correct (enclosure, screws, gaskets)
- [ ] Dimensions within tolerance (calipers, CMM)
- [ ] Weight within tolerance
- [ ] Cosmetic quality acceptable (scratches, color match)
- [ ] Labels correct (product label, CE mark, WEEE symbol)

**FAI Report**: [Link to detailed FAI report with photos]

---

### End-of-Line Test (EOL)

**Objective**: Validate every production unit before shipment

**Test Sequence**:
1. **Power-On Test** (10 seconds)
   - Verify device powers on
   - Check LED indicators
   - Verify display (if applicable)

2. **Functional Test** (2 minutes)
   - Test all sensors (verify readings in range)
   - Test wireless connectivity (WiFi/BLE)
   - Test buttons and user interface
   - Test battery charging (if rechargeable)

3. **Calibration** (1 minute, if required)
   - Sensor calibration (CO2, temperature, etc.)
   - Write calibration data to device

4. **Final Inspection** (30 seconds)
   - Visual inspection (cosmetic quality)
   - Verify labels present and correct

**Total Cycle Time**: <5 minutes per unit

**Pass/Fail Criteria**:
- **Pass**: All tests pass, unit ready to ship
- **Fail**: Any test fails → rework or scrap

**Yield Tracking**:
- First-Pass Yield (FPY): % of units passing without rework
- Target: >95%
- Track yield weekly, investigate if <95%

---

### Test Fixture Design

**Functional Test Fixture Requirements**:
- [ ] Pogo pins for PCB test points (power, UART, SWD)
- [ ] Automated test sequence (scripted, no operator intervention)
- [ ] Pass/fail indication (LED: green=pass, red=fail)
- [ ] Data logging (unit SN, test results, timestamp)
- [ ] Cycle time: <5 minutes per unit

**Fixture Specification**:
- Design: [CAD files, schematics]
- Fabrication: [Vendor, lead time, cost]
- Validation: [Tested with 100 units, >95% pass rate]

---

## Test Documentation

### Test Report Template

**Test Report Format**:

**1. Executive Summary**
- Product tested: [Name, version]
- Test phase: [EVT / DVT / PVT]
- Test date: [Start - End]
- Overall result: [ ] Pass [ ] Fail [ ] Conditional Pass
- Key findings: [Summary in 2-3 sentences]

**2. Test Scope**
- Tests conducted: [List]
- Tests deferred: [List, with reason]
- Sample size: [Number of units]

**3. Test Results**
- Summary table:
  | Test Category | Tests Run | Pass | Fail | Pass Rate |
  |--------------|-----------|------|------|-----------|
  | Functional | __ | __ | __ | __% |
  | Environmental | __ | __ | __ | __% |
  | Compliance | __ | __ | __ | __% |
  | Reliability | __ | __ | __ | __% |

**4. Detailed Results**
- Test-by-test results (see test cases)
- Failure analysis (root cause, corrective actions)

**5. Known Issues**
- Open issues: [List with severity]
- Deferred issues: [List with deferral reason]

**6. Recommendations**
- [ ] Proceed to next phase
- [ ] Fix issues and retest
- [ ] Redesign required

**7. Appendices**
- Test procedures
- Raw test data
- Photos/videos of failures
- External lab reports (EMC, LVD, etc.)

---

### Pass/Fail Criteria Summary

**Phase Gate Criteria**:

**EVT → DVT**:
- [ ] Core functionality works (all major features)
- [ ] Performance within 20% of target
- [ ] No show-stopper failures
- [ ] Thermal budget acceptable (<80°C at ambient)

**DVT → PVT**:
- [ ] 100% functional test pass rate
- [ ] All environmental tests pass
- [ ] EMC pre-compliance pass (>3dB margin)
- [ ] Reliability target on track (ALT results acceptable)
- [ ] User acceptance testing positive (NPS >50)

**PVT → MP**:
- [ ] All compliance tests pass (official EMC, LVD, RED, RoHS)
- [ ] Manufacturing yield >95%
- [ ] End-of-line test validated (<5 min cycle, >95% coverage)
- [ ] No critical issues in pilot build

---

## Test Execution & Tracking

### Test Schedule

| Phase | Test Activity | Duration | Start Week | End Week | Status |
|-------|--------------|----------|------------|----------|--------|
| **EVT** | Functional testing | 2 weeks | Week 8 | Week 10 | [ ] Not Started [ ] In Progress [ ] Complete |
| **EVT** | Performance characterization | 1 week | Week 10 | Week 11 | [ ] Not Started [ ] In Progress [ ] Complete |
| **EVT** | Thermal testing | 1 week | Week 11 | Week 12 | [ ] Not Started [ ] In Progress [ ] Complete |
| **DVT** | Full functional testing | 3 weeks | Week 22 | Week 25 | [ ] Not Started [ ] In Progress [ ] Complete |
| **DVT** | Environmental testing | 4 weeks | Week 25 | Week 29 | [ ] Not Started [ ] In Progress [ ] Complete |
| **DVT** | EMC pre-compliance | 1 week | Week 29 | Week 30 | [ ] Not Started [ ] In Progress [ ] Complete |
| **DVT** | Reliability (ALT) | 2 weeks | Week 28 | Week 30 | [ ] Not Started [ ] In Progress [ ] Complete |
| **PVT** | Manufacturing validation | 4 weeks | Week 38 | Week 42 | [ ] Not Started [ ] In Progress [ ] Complete |
| **PVT** | Compliance (official) | 6 weeks | Week 40 | Week 46 | [ ] Not Started [ ] In Progress [ ] Complete |

---

### Test Tracking Dashboard

**Overall Test Status**:
- Total Test Cases: _______
- Passed: _______ (___%)
- Failed: _______ (___%)
- Blocked: _______ (___%)
- Not Run: _______ (___%)

**Test Progress by Category**:
| Category | Total | Pass | Fail | Blocked | Not Run | % Complete |
|----------|-------|------|------|---------|---------|------------|
| Functional | __ | __ | __ | __ | __ | __% |
| Environmental | __ | __ | __ | __ | __ | __% |
| Compliance | __ | __ | __ | __ | __ | __% |
| Reliability | __ | __ | __ | __ | __ | __% |
| Manufacturing | __ | __ | __ | __ | __ | __% |

---

### Issue Tracking

**Test Issues Log**:
| Issue ID | Description | Severity | Detected Phase | Assigned To | Status | Resolution |
|----------|-------------|----------|----------------|-------------|--------|------------|
| TI-001 | _______ | [ ] Critical [ ] High [ ] Medium [ ] Low | _______ | _______ | [ ] Open [ ] In Progress [ ] Resolved | _______ |
| TI-002 | _______ | [ ] Critical [ ] High [ ] Medium [ ] Low | _______ | _______ | [ ] Open [ ] In Progress [ ] Resolved | _______ |
| ... | _______ | [ ] Critical [ ] High [ ] Medium [ ] Low | _______ | _______ | [ ] Open [ ] In Progress [ ] Resolved | _______ |

**Severity Definitions**:
- **Critical**: Blocks project, must fix immediately (e.g., device doesn't power on)
- **High**: Major feature broken, significant performance issue (e.g., sensor accuracy >10% off)
- **Medium**: Minor feature issue, workaround exists (e.g., cosmetic defect)
- **Low**: Nice-to-have, doesn't impact core functionality (e.g., UI improvement)

---

## Conclusion

**A comprehensive test plan ensures**:
- Product meets all requirements (functional, performance, environmental, compliance)
- Design is robust and manufacturable (yield, quality, reliability)
- Risk mitigation (identify issues early when fixes are cheap)

**Key Principles**:
1. **Test early, test often** - Identify issues in EVT when fixes are cheap, not PVT
2. **Document everything** - Test procedures, results, failures, root causes
3. **Track progress** - Dashboard, issue log, test schedule
4. **Clear pass/fail criteria** - No ambiguity on test results
5. **Phase-appropriate testing** - EVT=function, DVT=validation, PVT=manufacturing

**This test plan is a living document** - update as project evolves, tests are executed, and issues are found.

---

## Related Resources

- [Phase Gate Checklist](../templates/03-phase-gate-checklist.md) - Testing at each gate
- [Compliance Checklist](../templates/08-compliance-checklist.md) - Compliance testing details
- [Risk Register](../templates/02-risk-register.md) - Track testing risks
- [Lessons Learned](../templates/05-lessons-learned.md) - Capture testing lessons

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit  
**Repository**: https://github.com/kathegrima/hardware-pm-starter-kit

---

*"Test early, test often, test thoroughly - it's cheaper to find bugs in the lab than in the field."*
