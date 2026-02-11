# Compliance Checklist Template

> **Track EU compliance requirements throughout hardware development**

---

## Table of Contents

1. [Introduction](#introduction)
2. [How to Use This Checklist](#how-to-use-this-checklist)
3. [Pre-Project Compliance Planning](#pre-project-compliance-planning)
4. [Concept Phase Checklist](#concept-phase-checklist)
5. [EVT Phase Checklist](#evt-phase-checklist)
6. [DVT Phase Checklist](#dvt-phase-checklist)
7. [PVT Phase Checklist](#pvt-phase-checklist)
8. [Pre-Launch Checklist](#pre-launch-checklist)
9. [Post-Launch Compliance](#post-launch-compliance)
10. [Compliance Status Tracking](#compliance-status-tracking)

---

## Introduction

### Purpose

This checklist ensures your hardware product meets all required EU compliance regulations before launch. Non-compliance = product seizure, fines, market bans, and legal liability.

**Key EU Directives Covered**:
- CE Marking (general requirement)
- EMC Directive (2014/30/EU) - Electromagnetic Compatibility
- Low Voltage Directive (2014/35/EU) - Electrical Safety
- RoHS Directive (2011/65/EU) - Hazardous Substances
- RED (2014/53/EU) - Radio Equipment (if wireless)
- REACH Regulation (EC 1907/2006) - Chemicals
- WEEE Directive (2012/19/EU) - Waste Electrical Equipment
- MDR (2017/745) - Medical Device Regulation (if medical)

**Italy-Specific**:
- RAEE Registration (WEEE compliance in Italy)
- Italian language requirements
- Consumer warranty requirements (2 years)

---

### Compliance Responsibility

**Who is responsible?**
- ✅ **Manufacturer** (you) - legally liable for CE declaration
- ✅ **Authorized Representative** (if non-EU manufacturer) - EU-based contact for authorities
- ✅ **Importer** (if importing from non-EU) - EU entity bringing product to market

**Key Point**: You cannot delegate legal liability. Even if test lab conducts testing, **you are responsible** for compliance declaration.

---

## How to Use This Checklist

### Checklist Format

Each item has:
- [ ] **Checkbox** - Mark complete when done
- **Task Description** - What needs to be done
- **Responsible** - Who does this (PM, Eng, QA, Compliance)
- **Deadline** - When by (phase or date)
- **Status** - Not Started / In Progress / Complete / Blocked
- **Notes** - Additional info, links, evidence

---

### Status Definitions

| Status | Icon | Definition |
|--------|------|------------|
| **Not Started** | ⬜ | Task not yet begun |
| **In Progress** | 🟡 | Task underway, not complete |
| **Complete** | ✅ | Task finished, evidence documented |
| **Blocked** | 🔴 | Task cannot proceed (dependency, issue) |
| **N/A** | ➖ | Not applicable to this product |

---

### Evidence Requirements

**For each completed item, document**:
- Date completed
- Person responsible
- Evidence (test report, declaration, certificate, photo)
- Location of evidence (file path, document number)

**Example**:
```
[✅] EMC testing complete
     Date: 2026-04-15
     Responsible: Jane Smith (QA)
     Evidence: EMC test report TR-2026-042 (Sicom Testing)
     Location: /compliance/reports/EMC-test-report-TR-2026-042.pdf
     Status: Complete
```

---

## Pre-Project Compliance Planning

**Phase**: Before project kickoff  
**Responsible**: PM + Compliance Consultant

---

### Identify Applicable Directives

- [ ] **Product classification determined**
  - Category: [ ] Consumer Electronics [ ] Medical Device [ ] Industrial [ ] Toy [ ] Other: _______
  - Notes: _______________________________________________________

- [ ] **EMC Directive (2014/30/EU) applicable?**
  - [ ] Yes (all electronic products)
  - [ ] No (non-electronic only)
  - Notes: _______________________________________________________

- [ ] **Low Voltage Directive (2014/35/EU) applicable?**
  - [ ] Yes (voltage >50V AC or >75V DC)
  - [ ] No (low voltage only)
  - Operating Voltage: _______ V AC / _______ V DC

- [ ] **RoHS Directive (2011/65/EU) applicable?**
  - [ ] Yes (all electrical/electronic equipment)
  - [ ] No (exempt category - list reason: _______________________)

- [ ] **RED (2014/53/EU) applicable?**
  - [ ] Yes (has radio transmitter: WiFi, Bluetooth, cellular, LoRa, etc.)
  - [ ] No (no wireless)
  - Radio Technology: [ ] WiFi [ ] Bluetooth [ ] Cellular [ ] LoRa [ ] Other: _______

- [ ] **REACH Regulation (EC 1907/2006) applicable?**
  - [ ] Yes (all products with chemical substances)
  - [ ] No (N/A)

- [ ] **WEEE Directive (2012/19/EU) applicable?**
  - [ ] Yes (all electrical/electronic equipment)
  - [ ] No (exempt category)

- [ ] **MDR (2017/745) applicable?**
  - [ ] Yes - Medical device (intended for medical purpose)
    - Class: [ ] I [ ] IIa [ ] IIb [ ] III
  - [ ] No (not medical device)

---

### Budget & Timeline Planning

- [ ] **Compliance budget allocated**
  - Estimated Total Cost: €____________
  - Breakdown:
    - EMC Testing: €____________
    - LVD Testing: €____________
    - RED Testing: €____________
    - RoHS Testing: €____________
    - WEEE Registration: €____________
    - Consultant Fees: €____________
    - Contingency (retest): €____________

- [ ] **Compliance timeline added to project schedule**
  - Pre-compliance (EVT): Week _______
  - Official testing (DVT): Week _______
  - Certification completion: Week _______
  - Technical file creation: Week _______

- [ ] **Test lab selected and contacted**
  - Lab Name: _______________________________
  - Contact: _______________________________
  - Quote Received: [ ] Yes [ ] No
  - Lead Time: _______ weeks

- [ ] **Compliance consultant engaged (if applicable)**
  - Consultant: _______________________________
  - Scope: [ ] Full support [ ] Design review only [ ] Testing coordination
  - Cost: €____________

---

## Concept Phase Checklist

**Phase**: Weeks 1-4  
**Objective**: Identify compliance requirements and plan strategy

---

### Design for Compliance

- [ ] **Harmonized standards identified**
  - EMC: [ ] EN 55032 (emissions) [ ] EN 55035 (immunity)
  - LVD: [ ] EN 62368-1 (IT equipment) [ ] EN 60950-1 (legacy)
  - RED: [ ] EN 300 328 (2.4GHz) [ ] EN 301 489 (EMC for radio)
  - RoHS: [ ] EN IEC 63000:2018
  - Other: _______________________________________________________

- [ ] **Compliance design guidelines reviewed**
  - [ ] PCB layout for EMC (ground planes, trace routing, filtering)
  - [ ] Creepage/clearance distances for LVD (IEC 60664)
  - [ ] RoHS-compliant components only (request supplier declarations)
  - [ ] Pre-certified radio modules considered (if wireless)

- [ ] **Component RoHS compliance strategy**
  - [ ] BOM to include only RoHS-compliant parts
  - [ ] Request RoHS declarations from all suppliers
  - [ ] Add RoHS requirement to purchase order template

- [ ] **Compliance risks identified**
  - Top 3 risks:
    1. _______________________________________________________
    2. _______________________________________________________
    3. _______________________________________________________

---

## EVT Phase Checklist

**Phase**: Weeks 5-16  
**Objective**: Pre-compliance testing and design validation

---

### Pre-Compliance Testing

- [ ] **EMC pre-compliance testing scheduled**
  - Lab: _______________________________
  - Date: _______________________________
  - Cost: €____________
  - Deliverable: Pre-scan report with margin-to-limits

- [ ] **EMC pre-compliance testing complete**
  - Date Completed: _______________________________
  - Result: [ ] Pass (>6dB margin) [ ] Pass (3-6dB margin) [ ] Fail (<3dB margin or exceeds)
  - Issues Found: _______________________________________________________
  - Mitigation Plan: _______________________________________________________
  - Evidence: _______________________________________________________

- [ ] **RF pre-compliance testing (if wireless)**
  - Lab: _______________________________
  - Date: _______________________________
  - Result: [ ] Pass [ ] Fail
  - Issues Found: _______________________________________________________

- [ ] **Thermal testing at max ambient**
  - Max Ambient: _______ °C
  - Component Temps: [ ] All <80°C [ ] Some >80°C (list: _______________)
  - Mitigation: _______________________________________________________

---

### Component Compliance

- [ ] **RoHS declarations collected from suppliers**
  - Total Components: _______
  - Declarations Received: _______ / _______
  - Missing Declarations: _______________________________________________________
  - Action Plan: _______________________________________________________

- [ ] **REACH SVHC screening initiated**
  - SVHC List Version: _______ (check twice yearly)
  - Screening Method: [ ] Supplier declarations [ ] XRF testing [ ] Both
  - SVHC Found (>0.1%): [ ] None [ ] Yes (list: _______________)

- [ ] **Conflict minerals assessment (if applicable)**
  - [ ] 3TG minerals (Tin, Tantalum, Tungsten, Gold) in product?
  - [ ] Supplier declarations requested
  - [ ] CMRT (Conflict Minerals Reporting Template) collected

---

## DVT Phase Checklist

**Phase**: Weeks 17-32  
**Objective**: Official compliance testing and design freeze

---

### Official Testing Preparation

- [ ] **Test lab booked (8-12 weeks before DVT build complete)**
  - Lab: _______________________________
  - Booking Confirmation: _______________________________
  - Test Dates: _______________________________
  - Cost: €____________
  - Payment Terms: _______________________________

- [ ] **Test samples prepared**
  - Quantity: _______ units (3-5 typical)
  - Configuration: [ ] Worst-case [ ] Typical
  - Accessories: [ ] Cables [ ] Charger [ ] Antenna [ ] Manual
  - Shipped to Lab: [ ] Yes (tracking: _______________) [ ] No

- [ ] **Test documentation prepared**
  - [ ] Product description and specifications
  - [ ] Block diagram and schematics
  - [ ] PCB layout files
  - [ ] BOM with component datasheets
  - [ ] User manual (draft)
  - [ ] Test plan (if custom testing required)

---

### EMC Testing

- [ ] **EMC testing conducted**
  - Lab: _______________________________
  - Test Standard: EN 55032 (emissions), EN 55035 (immunity)
  - Test Date: _______________________________
  - Result: [ ] Pass [ ] Fail
  - Test Report Number: _______________________________

- [ ] **EMC test results reviewed**
  - Conducted Emissions: [ ] Pass [ ] Fail (margin: ___ dB)
  - Radiated Emissions: [ ] Pass [ ] Fail (margin: ___ dB)
  - ESD Immunity: [ ] Pass [ ] Fail (level: ___ kV)
  - Radiated Immunity: [ ] Pass [ ] Fail (level: ___ V/m)
  - Burst Immunity: [ ] Pass [ ] Fail (level: ___ kV)

- [ ] **EMC failures addressed (if applicable)**
  - Failure Mode: _______________________________________________________
  - Root Cause: _______________________________________________________
  - Fix Implemented: _______________________________________________________
  - Retest Scheduled: _______________________________
  - Retest Result: [ ] Pass [ ] Fail

---

### LVD Testing (if applicable)

- [ ] **LVD testing conducted**
  - Lab: _______________________________
  - Test Standard: EN 62368-1 or EN 60950-1
  - Test Date: _______________________________
  - Result: [ ] Pass [ ] Fail
  - Test Report Number: _______________________________

- [ ] **LVD test results reviewed**
  - Leakage Current: [ ] Pass [ ] Fail (measured: ___ mA, limit: ___ mA)
  - Insulation Resistance: [ ] Pass [ ] Fail
  - Dielectric Strength: [ ] Pass [ ] Fail
  - Temperature Rise: [ ] Pass [ ] Fail (max: ___ °C)
  - Flammability: [ ] Pass [ ] Fail (rating: V-0 / V-1 / V-2)

---

### RED Testing (if wireless)

- [ ] **RED testing conducted**
  - Lab: _______________________________
  - Test Standard: EN 300 328, EN 301 489
  - Test Date: _______________________________
  - Result: [ ] Pass [ ] Fail
  - Test Report Number: _______________________________

- [ ] **RED test results reviewed**
  - RF Power Output: [ ] Pass [ ] Fail (measured: ___ dBm, limit: ___ dBm)
  - Spurious Emissions: [ ] Pass [ ] Fail
  - Receiver Blocking: [ ] Pass [ ] Fail
  - EMC (RED-specific): [ ] Pass [ ] Fail
  - SAR Testing (if <20cm from body): [ ] Pass [ ] Fail [ ] N/A

---

### RoHS Testing

- [ ] **RoHS testing conducted**
  - Lab: _______________________________
  - Test Method: [ ] XRF screening [ ] ICP-OES/MS (wet chemistry)
  - Test Date: _______________________________
  - Result: [ ] Pass [ ] Fail
  - Test Report Number: _______________________________

- [ ] **RoHS test results reviewed**
  - Lead (Pb): _______ ppm (limit: 1000 ppm)
  - Mercury (Hg): _______ ppm (limit: 1000 ppm)
  - Cadmium (Cd): _______ ppm (limit: 100 ppm)
  - Hexavalent Chromium (Cr6+): _______ ppm (limit: 1000 ppm)
  - PBB/PBDE: _______ ppm (limit: 1000 ppm each)
  - Phthalates (DEHP, BBP, DBP, DIBP): _______ ppm each (limit: 1000 ppm)

- [ ] **RoHS non-compliance addressed (if applicable)**
  - Non-Compliant Material: _______________________________________________________
  - Component: _______________________________________________________
  - Replacement Component: _______________________________________________________
  - Retest Scheduled: _______________________________

---

### Design Freeze

- [ ] **All compliance testing passed**
  - [ ] EMC: Pass
  - [ ] LVD: Pass (or N/A)
  - [ ] RED: Pass (or N/A)
  - [ ] RoHS: Pass
  - Evidence Location: _______________________________________________________

- [ ] **Design freeze declared**
  - Freeze Date: _______________________________
  - Frozen Documents:
    - [ ] Schematic (Rev: ___)
    - [ ] PCB Layout (Rev: ___)
    - [ ] Mechanical (Rev: ___)
    - [ ] Firmware (Version: ___)
    - [ ] BOM (Rev: ___)

- [ ] **ECO process established**
  - [ ] Change control board (CCB) defined
  - [ ] ECO form template created
  - [ ] Approval workflow documented

---

## PVT Phase Checklist

**Phase**: Weeks 33-48  
**Objective**: Technical file creation and final certifications

---

### Technical File Creation

- [ ] **Technical file structure created**
  - [ ] Folder created: `/compliance/technical-file/`
  - [ ] Naming convention: `[Product Name]_Technical_File_v[X].pdf`

- [ ] **Technical file contents compiled**
  - [ ] 1. General product description
  - [ ] 2. Product specifications and photos
  - [ ] 3. Design documentation (schematic, PCB, mechanical)
  - [ ] 4. Bill of Materials (BOM)
  - [ ] 5. Risk assessment
  - [ ] 6. Test reports (EMC, LVD, RED, RoHS)
  - [ ] 7. List of harmonized standards applied
  - [ ] 8. User manual (all languages including Italian)
  - [ ] 9. Labels and markings (CE mark, WEEE symbol)
  - [ ] 10. Declaration of Conformity (signed)

- [ ] **Technical file reviewed**
  - Reviewer: _______________________________
  - Review Date: _______________________________
  - Issues Found: _______________________________________________________
  - Issues Resolved: [ ] Yes [ ] No

- [ ] **Technical file approved and archived**
  - Approval Date: _______________________________
  - Approved By: _______________________________
  - Storage Location: _______________________________________________________
  - Backup Location: _______________________________________________________
  - Retention Period: 10 years after last product sold

---

### Declaration of Conformity (DoC)

- [ ] **Declaration of Conformity drafted**
  - Template Used: [ ] Standard EU DoC template
  - Product Details: Completed
  - Directives Listed: [ ] EMC [ ] LVD [ ] RED [ ] RoHS [ ] REACH [ ] WEEE
  - Standards Listed: Completed
  - Signatory Identified: _______________________________

- [ ] **Declaration of Conformity reviewed**
  - Reviewer: _______________________________
  - Review Date: _______________________________
  - Accuracy Verified: [ ] Yes [ ] No

- [ ] **Declaration of Conformity signed**
  - Signatory Name: _______________________________
  - Title: _______________________________
  - Date Signed: _______________________________
  - Signature: [ ] Original signed [ ] Digital signature
  - File Location: _______________________________________________________

---

### CE Marking

- [ ] **CE mark design created**
  - Size: Minimum 5mm height
  - Format: [ ] Black on white [ ] Other: _______
  - Notified Body Number (if applicable): CE ______
  - File Format: [ ] Vector (SVG/AI) [ ] High-res raster (PNG 300dpi)

- [ ] **CE mark placement determined**
  - Location on Product: _______________________________
  - Visible: [ ] Yes [ ] No (if no, on packaging only)
  - Permanent: [ ] Yes (molded/etched) [ ] No (label)
  - Size: _______ mm height

- [ ] **CE mark added to product**
  - Method: [ ] Molded into enclosure [ ] Laser etched [ ] Label [ ] Screen printed
  - Verified on PVT samples: [ ] Yes [ ] No
  - Photo Evidence: _______________________________________________________

- [ ] **CE mark added to packaging**
  - Location: [ ] Box exterior [ ] Box interior [ ] Label
  - Verified on packaging samples: [ ] Yes [ ] No

---

### WEEE Compliance (Italy)

- [ ] **RAEE registration initiated**
  - Registration Portal: www.cdcraee.it
  - Account Created: [ ] Yes [ ] No
  - Registration Number: _______________________________

- [ ] **RAEE registration completed**
  - Registration Date: _______________________________
  - Registration Number: _______________________________
  - Collective Scheme Selected: [ ] Ecodom [ ] Ecolight [ ] Remedia [ ] CDC RAEE [ ] Other: _______
  - Contract Signed: [ ] Yes [ ] No
  - Annual Fee: €____________

- [ ] **WEEE symbol added to product**
  - Symbol: Crossed-out wheelie bin
  - Location on Product: _______________________________
  - Size: _______ mm height
  - Method: [ ] Molded [ ] Label [ ] Screen printed

- [ ] **WEEE reporting process established**
  - Reporting Frequency: Quarterly
  - Responsible Person: _______________________________
  - First Report Due: _______________________________

---

### User Documentation

- [ ] **User manual finalized**
  - Version: _______________________________
  - Languages: [ ] English [ ] Italian [ ] German [ ] French [ ] Spanish [ ] Other: _______
  - Page Count: _______
  - Format: [ ] Printed booklet [ ] PDF [ ] Online only

- [ ] **Italian translation completed**
  - Translator: _______________________________
  - Translation Date: _______________________________
  - Native Speaker Review: [ ] Yes [ ] No
  - File Location: _______________________________________________________

- [ ] **User manual includes required content**
  - [ ] Installation instructions
  - [ ] Operating instructions
  - [ ] Safety warnings (in Italian)
  - [ ] Maintenance instructions
  - [ ] Disposal instructions (WEEE symbol reference)
  - [ ] CE mark reference
  - [ ] Warranty information (2-year EU warranty)
  - [ ] Manufacturer contact information

- [ ] **Quick start guide created (if applicable)**
  - Languages: [ ] Italian [ ] English [ ] Pictograms only
  - Format: [ ] Printed card [ ] Folded insert
  - File Location: _______________________________________________________

---

### Product Labels

- [ ] **Product label designed**
  - Content: [ ] Product name [ ] Model number [ ] Serial number [ ] CE mark [ ] WEEE symbol
  - [ ] Electrical ratings (voltage, current, power)
  - [ ] Manufacturer name and address
  - [ ] Country of origin (if required)
  - [ ] Barcode/QR code (if applicable)

- [ ] **Product label reviewed**
  - Reviewer: _______________________________
  - Italian Text Verified: [ ] Yes [ ] No
  - Compliance Verified: [ ] Yes [ ] No

- [ ] **Product label applied to PVT samples**
  - Location: [ ] Bottom of product [ ] Back panel [ ] Inside battery compartment [ ] Other: _______
  - Method: [ ] Adhesive label [ ] Laser etched [ ] Screen printed
  - Durability Test: [ ] Pass (legible after handling) [ ] Fail

---

## Pre-Launch Checklist

**Phase**: Weeks 49-52  
**Objective**: Final verification before market launch

---

### Final Compliance Verification

- [ ] **All testing complete and passed**
  - [ ] EMC testing: Pass
  - [ ] LVD testing: Pass (or N/A)
  - [ ] RED testing: Pass (or N/A)
  - [ ] RoHS testing: Pass
  - Test Reports Filed: [ ] Yes [ ] No

- [ ] **Technical file complete and archived**
  - File Completeness: [ ] 100% [ ] Incomplete (missing: _______________)
  - Archived Location: _______________________________________________________
  - Accessible Within 48h: [ ] Yes [ ] No

- [ ] **Declaration of Conformity signed and available**
  - Signed Original: [ ] Yes [ ] No
  - Digital Copy: [ ] Yes (location: _______________) [ ] No
  - Available to Customers: [ ] Yes (on website / in box) [ ] No

- [ ] **CE marking present and correct**
  - On Product: [ ] Yes [ ] No
  - On Packaging: [ ] Yes [ ] No
  - Minimum 5mm Height: [ ] Yes [ ] No
  - Notified Body Number (if applicable): [ ] Yes [ ] No [ ] N/A

- [ ] **WEEE symbol present**
  - On Product: [ ] Yes [ ] No
  - On Packaging: [ ] Yes [ ] No

- [ ] **RAEE registration active (Italy)**
  - Registration Number: _______________________________
  - Collective Scheme Active: [ ] Yes [ ] No
  - Fees Paid: [ ] Yes [ ] No

---

### Market Surveillance Preparation

- [ ] **Compliance documentation accessible**
  - [ ] Technical file location documented
  - [ ] Test reports location documented
  - [ ] Declaration of Conformity location documented
  - [ ] Responsible person designated for authority requests

- [ ] **Authority request response process established**
  - Responsible Person: _______________________________
  - Response Time: 48 hours (legal requirement)
  - Process Documented: [ ] Yes [ ] No

- [ ] **Product safety incident response plan**
  - [ ] Incident reporting process defined (RAPEX)
  - [ ] Responsible person designated: _______________________________
  - [ ] Recall plan template created (if needed)

---

### Final Pre-Launch Checks

- [ ] **Compliance costs reconciled**
  - Budgeted: €____________
  - Actual: €____________
  - Variance: €____________ (% _____)
  - Explanation for Variance: _______________________________________________________

- [ ] **Launch approval from compliance perspective**
  - Compliance Officer: _______________________________
  - Approval Date: _______________________________
  - Conditions (if any): _______________________________________________________

- [ ] **Sales and marketing materials reviewed**
  - [ ] No misleading compliance claims (e.g., "CE certified" → "CE marked")
  - [ ] Warranty terms accurate (2 years EU)
  - [ ] Return policy compliant (14 days for online sales)

---

## Post-Launch Compliance

**Phase**: Ongoing after launch  
**Objective**: Maintain compliance and respond to issues

---

### Ongoing Monitoring

- [ ] **Field failure monitoring established**
  - Return Rate Target: <2%
  - Tracking System: _______________________________
  - Review Frequency: [ ] Weekly [ ] Monthly
  - Responsible: _______________________________

- [ ] **Safety incident monitoring**
  - [ ] Customer complaint review process
  - [ ] Safety incident escalation criteria defined
  - [ ] RAPEX notification process documented

- [ ] **WEEE reporting (Italy)**
  - [ ] Q1 Report Due: _______ (volumes placed on market)
  - [ ] Q2 Report Due: _______
  - [ ] Q3 Report Due: _______
  - [ ] Q4 Report Due: _______
  - Responsible: _______________________________

- [ ] **REACH SVHC list monitoring**
  - [ ] June update reviewed (SVHC candidate list)
  - [ ] December update reviewed
  - [ ] Product re-screened if new SVHC added
  - [ ] Customer notifications sent (if SVHC >0.1%)

---

### Compliance Updates

- [ ] **Technical file maintenance**
  - [ ] ECOs documented and added to technical file
  - [ ] Test reports updated (if retesting required)
  - [ ] BOM changes tracked
  - Last Update Date: _______________________________

- [ ] **Component lifecycle monitoring**
  - Review Frequency: [ ] Quarterly [ ] Semi-annually
  - Last Review: _______________________________
  - Components at EOL/NRND: _______________________________________________________
  - Action Plan: _______________________________________________________

- [ ] **Regulatory change monitoring**
  - [ ] Subscribe to EU Commission updates
  - [ ] Subscribe to notified body newsletters
  - [ ] Compliance consultant monitoring (if engaged)
  - Last Review: _______________________________

---

## Compliance Status Tracking

### Summary Dashboard

**Project**: _______________________________  
**Product**: _______________________________  
**Last Updated**: _______________________________

---

### Directive Compliance Status

| Directive | Applicable | Status | Test Date | Report # | Notes |
|-----------|-----------|--------|-----------|----------|-------|
| **EMC (2014/30/EU)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |
| **LVD (2014/35/EU)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |
| **RED (2014/53/EU)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |
| **RoHS (2011/65/EU)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |
| **REACH (EC 1907/2006)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |
| **WEEE (2012/19/EU)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |
| **MDR (2017/745)** | [ ] Yes [ ] No | [ ] Complete [ ] In Progress [ ] Not Started | _______ | _______ | _____________ |

---

### Key Milestones

| Milestone | Target Date | Actual Date | Status | Notes |
|-----------|-------------|-------------|--------|-------|
| Compliance budget approved | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| Test lab booked | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| Pre-compliance testing (EVT) | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| Official testing (DVT) | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| All testing passed | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| Technical file complete | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| DoC signed | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| RAEE registration (Italy) | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| CE marking applied | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |
| Compliance approval for launch | _______ | _______ | [ ] Complete [ ] On Track [ ] Delayed | _____________ |

---

### Budget Tracking

| Item | Budgeted | Actual | Variance | Notes |
|------|----------|--------|----------|-------|
| EMC Testing | €_______ | €_______ | €_______ | _____________ |
| LVD Testing | €_______ | €_______ | €_______ | _____________ |
| RED Testing | €_______ | €_______ | €_______ | _____________ |
| RoHS Testing | €_______ | €_______ | €_______ | _____________ |
| WEEE Registration | €_______ | €_______ | €_______ | _____________ |
| Consultant Fees | €_______ | €_______ | €_______ | _____________ |
| Retest (contingency) | €_______ | €_______ | €_______ | _____________ |
| **Total** | **€_______** | **€_______** | **€_______** | _____________ |

---

### Risks & Issues

| Risk/Issue | Severity | Status | Mitigation/Resolution | Owner |
|------------|----------|--------|-----------------------|-------|
| _________________________ | [ ] High [ ] Med [ ] Low | [ ] Open [ ] Resolved | _________________________ | _______ |
| _________________________ | [ ] High [ ] Med [ ] Low | [ ] Open [ ] Resolved | _________________________ | _______ |
| _________________________ | [ ] High [ ] Med [ ] Low | [ ] Open [ ] Resolved | _________________________ | _______ |

---

### Overall Status

**Compliance Readiness**: [ ] 🟢 On Track [ ] 🟡 At Risk [ ] 🔴 Critical Issues

**Blocking Issues**: _______________________________________________________

**Next Actions**:
1. _______________________________________________________
2. _______________________________________________________
3. _______________________________________________________

**Approved for Launch**: [ ] Yes [ ] No [ ] Conditional (conditions: _______________)

**Approved By**: _______________________________  
**Date**: _______________________________

---

## Appendices

### Appendix A: Useful Links

**EU Compliance Resources**:
- European Commission CE Marking: https://ec.europa.eu/growth/single-market/ce-marking_en
- Notified Bodies Database: https://ec.europa.eu/growth/tools-databases/nando/
- ECHA REACH SVHC List: https://echa.europa.eu/candidate-list-table

**Italy-Specific**:
- RAEE Registration: https://www.cdcraee.it
- Registro AEE: https://www.registroaee.it
- Italian Ministry of Enterprise: https://www.mise.gov.it

**Testing Labs in Italy**:
- TÜV Italia: https://www.tuv.it
- IMQ: https://www.imq.it
- Sicom Testing: https://www.sicomtesting.com
- CSI: https://www.csi-spa.com

---

### Appendix B: Document Templates

**Available Templates**:
- Declaration of Conformity (DoC): See [Compliance Guide](../guides/05-compliance-guide-eu.md)
- Technical File Structure: See [Compliance Guide](../guides/05-compliance-guide-eu.md)
- CE Marking Specifications: EN ISO 7010

---

### Appendix C: Contact List

| Role | Name | Email | Phone | Notes |
|------|------|-------|-------|-------|
| Compliance Manager | _______ | _______ | _______ | _______ |
| Test Lab Contact | _______ | _______ | _______ | _______ |
| Consultant | _______ | _______ | _______ | _______ |
| RAEE Registration | _______ | _______ | _______ | _______ |
| Translation Service | _______ | _______ | _______ | _______ |

---

## Conclusion

**Compliance is not optional - it's a legal requirement to sell in the EU.**

**Key Reminders**:
1. **Start early** - Engage compliance at Concept phase, not PVT
2. **Test twice** - Pre-compliance at EVT prevents expensive failures at DVT
3. **Document everything** - Technical file is required for 10 years
4. **Italy specifics** - RAEE registration, Italian manual, 2-year warranty
5. **Post-launch** - Compliance doesn't end at launch (monitoring, updates, WEEE reports)

**This checklist ensures** you don't miss critical compliance steps that could delay launch or result in market bans.

---

## Related Resources

- [Compliance Guide for EU/Italy](../guides/05-compliance-guide-eu.md) - Detailed guidance on EU directives
- [Phase Gate Checklist](../templates/03-phase-gate-checklist.md) - Compliance at each gate
- [Risk Register](../templates/02-risk-register.md) - Track compliance risks
- [Project Charter](../templates/01-project-charter.md) - Budget compliance costs

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit  
**Repository**: https://github.com/kathegrima/hardware-pm-starter-kit

---

*"Compliance is the foundation of responsible hardware development. Plan early, test twice, document everything."*
