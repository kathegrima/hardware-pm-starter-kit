# Bill of Materials (BOM) Template

> **Track components, costs, and suppliers for hardware products**

---

## Table of Contents

1. [Introduction to BOM Management](#introduction-to-bom-management)
2. [BOM Structure & Types](#bom-structure--types)
3. [BOM Template](#bom-template)
4. [BOM Fields Explained](#bom-fields-explained)
5. [BOM Evolution by Phase](#bom-evolution-by-phase)
6. [Cost Analysis & Tracking](#cost-analysis--tracking)
7. [Supplier Management](#supplier-management)
8. [Component Lifecycle Status](#component-lifecycle-status)
9. [BOM Best Practices](#bom-best-practices)
10. [Common BOM Mistakes](#common-bom-mistakes)

---

## Introduction to BOM Management

### What is a BOM?

**Bill of Materials (BOM)** = Complete list of all components, parts, and materials required to build one unit of a product.

**Purpose**:
- **Procurement**: What to buy and how much
- **Costing**: Calculate COGS (Cost of Goods Sold)
- **Manufacturing**: Assembly instructions and parts list
- **Supply Chain**: Lead time planning and inventory management
- **Change Control**: Track design changes and version history

---

### Why BOM Management Matters

**Cost Control**:
- BOM represents 60-80% of product COGS
- Small component cost increases compound at volume
- Example: €0.10 increase × 100,000 units = €10,000 margin impact

**Supply Chain Risk**:
- Single EOL component can halt production
- Lead time visibility prevents stockouts
- Dual-sourcing reduces supplier risk

**Manufacturing Efficiency**:
- Accurate BOM prevents assembly errors
- Clear part numbers reduce confusion
- AVL (Approved Vendor List) ensures quality

**Regulatory Compliance**:
- RoHS declarations required for all components
- REACH SVHC tracking (>0.1% notification required)
- Conflict minerals reporting (EU Regulation 2017/821)

---

## BOM Structure & Types

### BOM Hierarchy Levels

**1. System-Level BOM** (Top Level)
- Complete product as shipped to customer
- Includes all sub-assemblies, packaging, accessories
- Example: "SmartSense Air Quality Monitor - Complete Kit"

**2. Sub-Assembly BOM** (Mid Level)
- Major assemblies within product
- Example: "Main PCB Assembly", "Enclosure Assembly", "Battery Pack"

**3. Component-Level BOM** (Lowest Level)
- Individual components (ICs, resistors, capacitors, screws)
- Purchased parts (no further breakdown)

**Example Hierarchy**:
```
SmartSense Air Quality Monitor (System)
├── Main PCB Assembly (Sub-assembly)
│   ├── PCB (bare board)
│   ├── MCU (IC)
│   ├── CO2 Sensor Module
│   ├── Resistors (50x various values)
│   ├── Capacitors (30x various values)
│   └── Connectors (3x)
├── Enclosure Assembly (Sub-assembly)
│   ├── Top Cover (injection molded)
│   ├── Bottom Cover (injection molded)
│   ├── Screws (4x M2.5)
│   └── Rubber Feet (4x)
├── Battery Pack (Sub-assembly)
│   ├── Li-ion Cell (18650)
│   ├── Battery Holder
│   └── Protection Circuit
├── Accessories (Sub-assembly)
│   ├── USB Cable
│   ├── User Manual
│   └── Quick Start Guide
└── Packaging
    ├── Retail Box
    ├── Foam Insert
    └── Shipping Label
```

---

### BOM Types

**1. Engineering BOM (EBOM)**
- Created by engineering team during design
- Focus: Technical specifications and functionality
- Used in: EVT, DVT phases

**2. Manufacturing BOM (MBOM)**
- Optimized for production and assembly
- Includes: Assembly process steps, tooling, fixtures
- Used in: PVT, MP phases

**3. Sales BOM (SBOM)**
- What customer receives (product + accessories + packaging)
- Used for: Order fulfillment, shipping, inventory

**4. Service BOM**
- Spare parts and replacement components
- Used for: RMA, warranty repairs, field service

**This template focuses on EBOM → MBOM** (most relevant for hardware development)

---

## BOM Template

### Excel/Google Sheets Template

**Download Links**:
- Excel: [07-bom-template.xlsx](../templates/07-bom-template.xlsx)
- Google Sheets: [Make a copy](https://docs.google.com/spreadsheets/d/...)
- CSV: [07-bom-template.csv](../templates/07-bom-template.csv)

---

### BOM Template Structure

**Sheet 1: Main BOM**

| Line # | Category | Designator | Qty | Part Number | MPN | Description | Manufacturer | Supplier | Unit Cost | Ext Cost | Lead Time | Lifecycle | RoHS | Notes |
|--------|----------|------------|-----|-------------|-----|-------------|--------------|----------|-----------|----------|-----------|-----------|------|-------|
| 1 | PCB | - | 1 | PCB-001 | - | Main PCB 4-layer FR4 | [PCB Fab] | [PCB Supplier] | €8.50 | €8.50 | 2 weeks | - | Yes | 100×80mm, ENIG finish |
| 2 | IC | U1 | 1 | STM32F407VGT6 | STM32F407VGT6 | MCU ARM Cortex-M4 | STMicroelectronics | Mouser | €7.85 | €7.85 | 12 weeks | Active | Yes | 168MHz, 1MB Flash |
| 3 | Sensor | U2 | 1 | SCD40 | SCD40 | CO2 Sensor Module | Sensirion | Digi-Key | €38.00 | €38.00 | 16 weeks | Active | Yes | 400-5000ppm range |
| 4 | Resistor | R1-R10 | 10 | RC0603FR-0710KL | - | Resistor 10KΩ 1% 0603 | Yageo | LCSC | €0.01 | €0.10 | 2 weeks | Active | Yes | General purpose |
| 5 | Capacitor | C1-C5 | 5 | CL10B104KB8NNNC | - | Capacitor 100nF 50V X7R 0603 | Samsung | LCSC | €0.02 | €0.10 | 2 weeks | Active | Yes | Decoupling |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |

**Sheet 2: Cost Summary**

| Category | Total Cost | % of BOM | Notes |
|----------|------------|----------|-------|
| PCB & Assembly | €18.50 | 25% | 4-layer PCB + assembly labor |
| ICs & Modules | €52.00 | 35% | MCU, sensors, power management |
| Passives | €3.20 | 4% | Resistors, capacitors, inductors |
| Connectors | €4.50 | 6% | USB, battery, programming |
| Mechanical | €12.00 | 16% | Enclosure, screws, feet |
| Battery | €6.00 | 8% | Li-ion 18650 cell |
| Packaging | €4.00 | 6% | Box, manual, cable |
| **Total BOM Cost** | **€100.20** | **100%** | At 1K volume |

**Sheet 3: Supplier Contacts**

| Supplier | Contact | Email | Phone | Lead Time | MOQ | Payment Terms | Notes |
|----------|---------|-------|-------|-----------|-----|---------------|-------|
| Mouser | John Smith | john@mouser.com | +1-555-0100 | 12 weeks | 1 | Net 30 | Primary for ICs |
| Digi-Key | Jane Doe | jane@digikey.com | +1-555-0200 | 16 weeks | 1 | Net 30 | Backup for ICs |
| LCSC | - | support@lcsc.com | +86-xxx | 2-4 weeks | 10 | Prepay | Passives, China |

**Sheet 4: Change Log**

| Rev | Date | Author | Changes | Reason | Approved By |
|-----|------|--------|---------|--------|-------------|
| A | 2026-01-15 | John Doe | Initial BOM | EVT phase | PM |
| B | 2026-03-10 | Jane Smith | Changed R5 from 10K to 4.7K | Thermal optimization | Tech Lead |
| C | 2026-05-20 | John Doe | Added second source for U2 | Supply chain risk | PM |

---

## BOM Fields Explained

### Essential Fields

**1. Line # (Line Number)**
- Sequential number for each BOM line item
- Makes reference easy ("See line 23")
- Reset numbering with each BOM revision

**2. Category**
- Group similar components (IC, Resistor, Capacitor, Mechanical, etc.)
- Enables cost analysis by category
- Standard categories:
  - PCB (bare board)
  - IC (integrated circuits)
  - Passive (resistors, capacitors, inductors)
  - Connector
  - Mechanical (screws, enclosure, spacers)
  - Battery
  - Cable
  - Module (sensors, displays, pre-built assemblies)
  - Packaging (box, manual, accessories)

**3. Designator (Reference Designator)**
- Component location on PCB or assembly
- Standard prefixes:
  - U = IC (U1, U2, U3...)
  - R = Resistor (R1, R2, R3...)
  - C = Capacitor (C1, C2, C3...)
  - L = Inductor (L1, L2...)
  - D = Diode (D1, D2...)
  - Q = Transistor (Q1, Q2...)
  - J = Connector (J1, J2...)
  - SW = Switch (SW1, SW2...)
  - LED = LED (LED1, LED2...)
- Use ranges for identical parts: "R1-R10" (10 identical 10KΩ resistors)
- Leave blank for non-PCB items (enclosure, packaging)

**4. Qty (Quantity)**
- Number of this part per unit
- Important: This is per-unit quantity (not total order quantity)
- Example: If R1-R10 are 10 identical resistors, Qty = 10

**5. Part Number (Internal Part Number)**
- Your company's internal tracking number
- Format: [Category]-[Number] (e.g., PCB-001, RES-10K-001)
- Consistent numbering scheme across projects
- Optional but highly recommended for multi-project companies

**6. MPN (Manufacturer Part Number)**
- Exact part number from manufacturer
- Critical for procurement (no ambiguity)
- Example: STM32F407VGT6 (not "STM32 MCU")
- Copy-paste from datasheet to avoid typos

**7. Description**
- Human-readable description of part
- Include key specs:
  - Resistor: "Resistor 10KΩ 1% 0603"
  - Capacitor: "Capacitor 100nF 50V X7R 0603"
  - IC: "MCU ARM Cortex-M4 168MHz 1MB Flash LQFP100"
- Be specific (not just "capacitor" but "Capacitor 100nF 50V X7R 0603")

**8. Manufacturer**
- Component manufacturer (not distributor)
- Example: STMicroelectronics, Sensirion, Yageo, Samsung
- Important for: AVL (Approved Vendor List), quality control

**9. Supplier (Primary Supplier)**
- Where you buy the part (distributor or direct)
- Example: Mouser, Digi-Key, LCSC, Arrow, Farnell
- Include contact info in "Supplier Contacts" sheet

**10. Unit Cost**
- Price per piece at target volume (e.g., 1K, 10K units)
- Currency: € or $ (be consistent)
- Update regularly (quarterly or with each quote)
- Negotiate volume discounts

**11. Ext Cost (Extended Cost)**
- Formula: `Qty × Unit Cost`
- Total cost for this line item per unit
- Automatically calculated in Excel

**12. Lead Time**
- Time from order to delivery (in weeks)
- Critical for: Production planning, inventory management
- Update regularly (lead times fluctuate with demand)
- Flag long-lead items (>12 weeks) for early procurement

**13. Lifecycle (Lifecycle Status)**
- Component availability status
- Values:
  - **Active**: Recommended for new designs
  - **NRND**: Not Recommended for New Designs (EOL warning)
  - **EOL**: End of Life (last-time buy)
  - **Obsolete**: No longer available
- Check quarterly (especially for ICs)
- Trigger redesign if NRND or EOL

**14. RoHS (RoHS Compliant)**
- EU RoHS Directive (2011/65/EU) compliance
- Values: Yes / No / Exempt
- Critical for: EU sales, environmental compliance
- Require declaration from supplier (include in PO terms)

**15. Notes**
- Additional information:
  - Second source options: "Alt: TI TPS62160"
  - Special procurement: "Order 16 weeks before DVT"
  - Assembly notes: "Hand-solder, heat-sensitive"
  - Design notes: "Critical for thermal performance"

---

### Optional Fields (Advanced)

**16. Second Source (Alternate MPN)**
- Alternate manufacturer part number
- Pin-compatible or drop-in replacement
- Reduces supply chain risk
- Example: Primary = STM32F407VGT6, Alt = GD32F407VGT6

**17. Supplier 2 (Backup Supplier)**
- Secondary supplier for redundancy
- Example: Primary = Mouser, Backup = Digi-Key

**18. MOQ (Minimum Order Quantity)**
- Smallest quantity supplier will sell
- Important for: Small-volume projects, prototyping
- Example: IC from Digi-Key MOQ=1, LCSC MOQ=10

**19. Package (Component Package)**
- Physical package type
- Example: LQFP100, TQFP64, 0603, 0805, SOT-23
- Important for: PCB layout, assembly (hand vs machine)

**20. Datasheet Link**
- URL to manufacturer datasheet
- Critical for: Engineering reference, procurement verification
- Keep updated if manufacturer changes URL

**21. REACH SVHC (REACH Compliance)**
- Substances of Very High Concern (>0.1% notification)
- Values: None / [Substance Name] / Under Review
- Update twice yearly (SVHC list updated June & December)

**22. Country of Origin (COO)**
- Where component is manufactured
- Important for: Tariffs, trade compliance, geopolitical risk
- Example: China, Taiwan, USA, Germany

---

## BOM Evolution by Phase

### Concept Phase BOM (Week 1-4)

**Goal**: ROM (Rough Order of Magnitude) cost estimate

**Characteristics**:
- 50-70% of components identified
- Major ICs and modules selected
- Passives estimated (e.g., "~50 resistors @ €0.01 each")
- Mechanical rough estimate (enclosure material, size)
- Cost accuracy: ±50%

**Example**:
```
MCU: STM32 series, ~€7 (exact model TBD)
Sensor: CO2 sensor, ~€35-40 (3 options being evaluated)
Passives: ~€3 (estimate 100 parts @ €0.03 avg)
PCB: 4-layer, 100×80mm, ~€8
Total BOM (estimate): €80-100
```

**Action Items**:
- Identify long-lead components (>12 weeks)
- Select technology platform (MCU family, radio module)
- Rough cost allocation by category

---

### EVT Phase BOM (Week 5-16)

**Goal**: Detailed BOM for functional prototype

**Characteristics**:
- 90% of components selected (exact MPNs)
- Passives fully specified (values, tolerances, packages)
- Second sources identified for critical parts
- Cost accuracy: ±30%

**Updates from Concept**:
- Exact MPN for all ICs and modules
- Resistor/capacitor values from circuit design
- PCB stackup defined (4-layer, material, finish)
- Enclosure prototype method (3D print or CNC)

**Example Changes**:
```
Concept: "MCU: STM32 series, ~€7"
EVT:     "MCU: STM32F407VGT6, €7.85 @ 1K (Mouser)"

Concept: "Passives: ~€3 (estimate)"
EVT:     "50× Resistors (various values): €0.50
          30× Capacitors (various values): €0.60
          5× Inductors: €1.20
          Total Passives: €2.30"
```

**Action Items**:
- Order long-lead components (don't wait for EVT gate)
- Request volume quotes from suppliers (1K, 10K, 100K pricing)
- Check lifecycle status (all Active, no NRND/EOL)
- Verify RoHS compliance (request declarations)

---

### DVT Phase BOM (Week 17-32)

**Goal**: Production-intent BOM, design freeze

**Characteristics**:
- 100% of components finalized (no TBDs)
- All MPNs locked (design freeze)
- Second sources qualified (tested and approved)
- Cost accuracy: ±10%
- AVL (Approved Vendor List) established

**Updates from EVT**:
- Component optimizations (cost-downs, availability improvements)
- All second sources tested and documented
- Assembly method defined (SMT, hand-solder, etc.)
- Packaging and accessories specified

**Example Changes**:
```
EVT:  "Resistor 10KΩ 1% 0603: Yageo RC0603FR-0710KL, €0.01"
DVT:  "Resistor 10KΩ 1% 0603: 
        Primary: Yageo RC0603FR-0710KL, €0.01 (Mouser)
        Alt:     Panasonic ERJ-3EKF1002V, €0.01 (Digi-Key)
        Both tested and qualified"

EVT:  "Enclosure: 3D printed ABS, ~€15"
DVT:  "Enclosure: Injection molded ABS (UL94 V-0), €3.50 @ 10K
        Tooling: €120K (amortized over 50K units = €2.40/unit)
        Total enclosure cost: €5.90"
```

**Action Items**:
- **Design freeze**: No BOM changes without ECO process
- Place long-lead component orders for PVT build
- Negotiate volume pricing (10K, 50K, 100K+)
- Finalize AVL and supplier contracts

---

### PVT Phase BOM (Week 33-48)

**Goal**: Manufacturing BOM (MBOM), production-ready

**Characteristics**:
- Assembly process optimized (DFM improvements)
- Test points and fixtures added
- Yield losses accounted for (scrap rate)
- Cost accuracy: ±5%
- Final cost target validated

**Updates from DVT**:
- Assembly labor cost added (€1-5 per unit typical)
- Test fixture cost amortized
- Yield loss buffer (5-10% scrap allowance)
- Packaging finalized (retail or shipping packaging)

**Example Additions**:
```
BOM Line: PCB Assembly Labor
  Description: SMT assembly + hand-solder + testing
  Qty: 1
  Unit Cost: €3.50
  Notes: Based on cycle time 8 minutes @ €26/hour labor rate

BOM Line: Test Fixture (Amortized)
  Description: Functional test jig
  Total Cost: €15,000
  Units: 50,000
  Per-Unit Cost: €0.30

BOM Line: Yield Loss Buffer
  Description: 5% scrap allowance
  Calculation: Total BOM × 5% = €1.25
```

**Action Items**:
- Lock MBOM (no changes without formal ECO)
- Establish inventory management (safety stock, reorder points)
- Monitor actual costs vs BOM (track variances)

---

### MP Phase BOM (Week 49+)

**Goal**: Cost optimization, continuous improvement

**Characteristics**:
- BOM frozen (changes via ECO only)
- Cost reduction initiatives (value engineering)
- Supply chain optimization (bulk pricing, local sourcing)
- Actual cost tracking (vs budgeted)

**Ongoing Activities**:
- Quarterly cost reviews (negotiate better pricing)
- Component lifecycle monitoring (replace NRND/EOL parts)
- Supplier performance tracking (quality, delivery, cost)
- Value engineering (reduce BOM cost 5-10% annually)

---

## Cost Analysis & Tracking

### BOM Cost Breakdown

**Typical Hardware Product Cost Structure**:

| Category | % of BOM | Notes |
|----------|----------|-------|
| **PCB & Assembly** | 20-30% | Bare board + SMT assembly labor |
| **ICs & Modules** | 25-40% | MCU, sensors, power management, radio modules |
| **Passives** | 3-8% | Resistors, capacitors, inductors |
| **Connectors** | 5-10% | USB, battery, programming, I/O |
| **Mechanical** | 10-20% | Enclosure, screws, gaskets, labels |
| **Battery** | 5-15% | Li-ion, LiPo, or battery pack |
| **Packaging** | 3-8% | Box, manual, cable, accessories |

**Example BOM Cost Breakdown** (SmartSense Air Quality Monitor):
```
Total BOM: €75.00 @ 10K volume

PCB & Assembly:     €18.50 (25%)
ICs & Modules:      €26.00 (35%) ← Highest cost
Passives:           €3.20  (4%)
Connectors:         €4.50  (6%)
Mechanical:         €12.00 (16%)
Battery:            €6.00  (8%)
Packaging:          €4.80  (6%)
```

**Insight**: ICs/Modules are highest cost → focus optimization here first

---

### COGS Calculation

**COGS (Cost of Goods Sold)** = Total cost to manufacture one unit

**Formula**:
```
COGS = BOM Cost + Assembly Labor + Test Labor + Overhead + Yield Loss

Where:
- BOM Cost: Sum of all component costs
- Assembly Labor: SMT + hand-solder + final assembly (€2-5 typical)
- Test Labor: Functional test + calibration (€1-3 typical)
- Overhead: Factory overhead allocation (5-15% of labor)
- Yield Loss: Scrap allowance (5-10% of BOM+Labor)
```

**Example**:
```
BOM Cost:           €75.00
Assembly Labor:     €3.50
Test Labor:         €2.00
Overhead (10%):     €0.55
Subtotal:           €81.05
Yield Loss (5%):    €4.05
─────────────────────────
Total COGS:         €85.10
```

**Target Margin**:
- Consumer products: 40-50% margin → Sell price = €142-170
- B2B products: 50-60% margin → Sell price = €170-213
- High-volume: 30-40% margin → Sell price = €121-142

---

### Cost Tracking by Phase

| Phase | BOM Cost | Accuracy | Actions |
|-------|----------|----------|---------|
| **Concept** | €80-120 | ±50% | ROM estimate, validate feasibility |
| **EVT** | €95-115 | ±30% | Volume quotes, second source options |
| **DVT** | €100-110 | ±10% | Lock costs, negotiate contracts |
| **PVT** | €102-108 | ±5% | Validate actuals, final pricing |
| **MP** | €105 actual | Actual | Track variances, cost-down initiatives |

**Cost Trend Analysis**:
- If costs increasing phase-over-phase → Red flag (scope creep, poor estimates)
- If costs flat or decreasing → Good (design optimization working)
- Track "cost variance" per phase (Actual - Budget)

---

## Supplier Management

### Supplier Selection Criteria

**Tier 1: Critical Components** (ICs, sensors, modules)
- **Criteria**:
  - Authorized distributor (not gray market)
  - Stock availability (>1,000 units in stock)
  - Lead time <16 weeks
  - Quality reputation (branded suppliers)
  - Technical support available

**Recommended Suppliers (Europe/Global)**:
- Mouser Electronics (mouser.com)
- Digi-Key (digikey.com)
- Farnell/element14 (farnell.com)
- RS Components (rs-online.com)
- Arrow Electronics (arrow.com)

**Tier 2: Passives & Connectors**
- **Criteria**:
  - Competitive pricing (often 30-50% cheaper than Tier 1)
  - MOQ acceptable (10-100 pieces)
  - Reasonable lead time (<4 weeks)
  - RoHS compliance verified

**Recommended Suppliers**:
- LCSC (lcsc.com) - China, excellent for passives
- TME (tme.eu) - Europe-based, good shipping
- Würth Elektronik (we-online.com) - Direct for passives/connectors

**Tier 3: Mechanical & Packaging**
- **Criteria**:
  - Custom manufacturing capability (injection molding, CNC)
  - Tooling investment reasonable (€50K-200K)
  - Quality certifications (ISO 9001)
  - Communication (English proficiency, responsiveness)

**Recommended Approach**:
- Get 3 quotes for tooling
- Visit factory if >€100K investment
- Request samples before committing

---

### Approved Vendor List (AVL)

**Purpose**: Standardize suppliers for quality, cost, and compliance

**AVL Format**:

| Component Category | Primary Supplier | Backup Supplier | Notes |
|--------------------|------------------|-----------------|-------|
| ICs & Modules | Mouser | Digi-Key | All orders >€500 → Mouser discount |
| Passives (EU stock) | Farnell | RS Components | <1 week delivery |
| Passives (China) | LCSC | - | 2-4 week delivery, MOQ 10 |
| PCB Fabrication | PCBWay | JLCPCB | 4-layer, ENIG finish |
| PCB Assembly | Vendor A (Italy) | Vendor B (Germany) | ISO 9001, IPC-A-610 Class 2 |
| Enclosure Molding | Vendor C (Italy) | - | ABS, UL94 V-0, ISO 9001 |

**AVL Maintenance**:
- Review quarterly
- Add new suppliers after qualification (3 successful orders)
- Remove suppliers after quality issues (2 strikes rule)

---

### Purchase Order (PO) Best Practices

**PO Must Include**:
1. Exact MPN (Manufacturer Part Number)
2. Quantity (pieces, not reels/boxes)
3. Unit price and total price
4. Lead time and delivery date
5. Shipping terms (Incoterms: EXW, DDP, etc.)
6. Payment terms (Net 30, prepay, etc.)
7. RoHS compliance requirement
8. Packaging requirements (anti-static bags, moisture barrier)

**Example PO Line**:
```
MPN: STM32F407VGT6
Description: MCU ARM Cortex-M4 168MHz 1MB Flash LQFP100
Quantity: 1,000 pieces
Unit Price: €7.85
Total Price: €7,850.00
Lead Time: 12 weeks
Delivery Date: 2026-06-15
RoHS: Required (provide declaration)
Packaging: Tape & reel, anti-static bag, moisture barrier bag
```

---

## Component Lifecycle Status

### Lifecycle Status Definitions

| Status | Definition | Action Required |
|--------|------------|-----------------|
| **Active** | Recommended for new designs, full production | ✅ Use freely |
| **NRND** | Not Recommended for New Designs (EOL warning) | ⚠️ Find replacement ASAP |
| **EOL** | End of Life announced, last-time-buy date set | 🚨 Lifetime buy or redesign |
| **Obsolete** | No longer available from manufacturer | ❌ Must redesign |

---

### How to Check Lifecycle Status

**1. Manufacturer Website**
- Search component on manufacturer site (e.g., st.com for STM32)
- Look for "Product Status" or "Lifecycle Status"
- Active = good, NRND = warning, EOL = problem

**2. Distributor Websites**
- Mouser, Digi-Key show lifecycle status on product page
- Filter search by "Active" status only

**3. Component Database Tools**
- Octopart (octopart.com) - aggregates lifecycle data
- SiliconExpert (siliconexpert.com) - paid, comprehensive database
- FindChips (findchips.com) - free, decent coverage

**4. Supplier Alerts**
- Subscribe to PCN (Product Change Notifications) from manufacturers
- Distributors can notify you of EOL (ask your rep)

---

### Lifecycle Monitoring Schedule

**Recommended Frequency**:
- **Concept/EVT**: Check all components before selecting (one-time)
- **DVT**: Recheck all components before design freeze (one-time)
- **PVT/MP**: Check critical components (ICs, sensors) quarterly
- **Ongoing**: Subscribe to manufacturer PCN alerts

**Critical Components to Monitor**:
- ICs (MCUs, power management, sensors)
- Modules (WiFi, Bluetooth, cellular)
- High-value parts (>€10 each)
- Single-source parts (no alternate)

**Lower Priority**:
- Passives (resistors, capacitors) - easy to replace
- Commodity parts (screws, cables) - widely available

---

## BOM Best Practices

### 1. Use Standard Part Numbers

**Do**:
- MPN: STM32F407VGT6 (exact, from datasheet)
- Description: MCU ARM Cortex-M4 168MHz 1MB Flash LQFP100

**Don't**:
- MPN: STM32 (ambiguous, many variants)
- Description: Microcontroller (not specific enough)

---

### 2. Standardize Component Values

**Resistors**: Use E24 series (24 standard values per decade)
- 10Ω, 11Ω, 12Ω, 13Ω, 15Ω, 16Ω, 18Ω, 20Ω, 22Ω, 24Ω, 27Ω, 30Ω, 33Ω, 36Ω, 39Ω, 43Ω, 47Ω, 51Ω, 56Ω, 62Ω, 68Ω, 75Ω, 82Ω, 91Ω
- **Why**: Cheaper (high volume), readily available, shorter lead times

**Capacitors**: Use standard values
- 1pF, 2.2pF, 4.7pF, 10pF, 22pF, 47pF, 100pF, 220pF, 470pF, 1nF, 2.2nF, 4.7nF, 10nF, 22nF, 47nF, 100nF, 220nF, 470nF, 1µF, 2.2µF, 4.7µF, 10µF, 22µF, 47µF, 100µF

**Reduce Unique Part Count**:
- Design with 10KΩ resistors instead of 9.8KΩ (if tolerance allows)
- Standardize capacitor values (all 100nF decoupling caps same MPN)

---

### 3. Dual-Source Critical Components

**Single-Source Risk**:
- Component shortage → production halt
- Supplier quality issue → no backup
- Price increase → no negotiation leverage

**Dual-Source Strategy**:
- Identify second source during EVT
- Test and qualify alternate in DVT
- Document both MPNs in BOM (Primary + Alt columns)
- Split production orders (70/30 or 80/20) to keep both qualified

**Example**:
```
Component: 10KΩ Resistor 1% 0603
Primary:   Yageo RC0603FR-0710KL (Mouser)
Alternate: Panasonic ERJ-3EKF1002V (Digi-Key)
Notes:     Both tested and qualified at DVT phase
```

---

### 4. Version Control

**BOM Versioning Scheme**:
- **Format**: Rev [Letter] (Rev A, Rev B, Rev C...)
- **When to Rev**:
  - Major change (component added/removed, MPN change): New letter (A→B)
  - Minor change (quantity, description update): Same letter with date stamp

**Change Log** (Sheet 4 in template):
- Document every BOM change
- Include: Rev, Date, Author, Changes, Reason, Approved By
- Essential for: Traceability, root cause analysis, compliance

**Example**:
```
Rev A: 2026-01-15 - Initial BOM for EVT phase
Rev B: 2026-03-10 - Changed R5 from 10KΩ to 4.7KΩ (thermal optimization)
Rev C: 2026-05-20 - Added second source for U2 (supply chain risk mitigation)
Rev D: 2026-08-01 - Design freeze for PVT (no further changes without ECO)
```

---

### 5. Track Lead Times

**Why Lead Time Matters**:
- Long-lead components (>12 weeks) can delay entire project
- Need to order early to avoid production delays
- Lead times fluctuate (chip shortage can extend 8w → 52w overnight)

**Lead Time Tracking**:
- Update BOM quarterly (or monthly during chip shortages)
- Flag long-lead items (>12 weeks) in red
- Order long-lead components 16+ weeks before production

**Example**:
```
Component: CO2 Sensor Module (SCD40)
Lead Time: 16 weeks (as of 2026-02-01)
Action:    Order by Week 20 of DVT for Week 36 PVT build
```

---

### 6. Cost Tracking at Volume

**Volume Pricing Tiers**:
- Get quotes at multiple volumes: 100, 1K, 10K, 100K
- Unit cost decreases with volume (economies of scale)
- Example:
  ```
  STM32F407VGT6 Pricing:
  100 pieces:   €12.50/each
  1,000 pieces: €7.85/each (37% discount)
  10,000 pieces: €6.20/each (21% additional discount)
  ```

**BOM at Multiple Volumes**:
- Maintain BOM cost at target volume (e.g., 10K)
- Track cost deltas: "BOM @ 1K = €95, @ 10K = €75 (21% reduction)"
- Validate margin: "COGS @ 10K = €85, Sell Price = €150, Margin = 43%"

---

## Common BOM Mistakes

### Mistake 1: Using Generic Part Numbers

**Problem**:
```
MPN: 10K Resistor
Description: Resistor
```

**Impact**: Procurement orders wrong part (10KΩ 5% instead of 1%, 0805 instead of 0603)

**Solution**:
```
MPN: RC0603FR-0710KL
Description: Resistor 10KΩ 1% 0603 1/10W
```

---

### Mistake 2: Not Checking Lifecycle Status

**Problem**: Component marked NRND or EOL during project

**Impact**: 
- Forced redesign mid-project (2-6 month delay)
- Last-time buy (huge inventory carrying cost)
- Scrambling for alternate (may not be pin-compatible)

**Solution**:
- Check lifecycle status before selecting component (Concept phase)
- Recheck before design freeze (DVT phase)
- Subscribe to manufacturer PCN alerts

---

### Mistake 3: Single-Source Critical Components

**Problem**: No backup supplier for critical IC or sensor

**Impact**:
- Supplier shortage → production halt
- Price increase → no leverage to negotiate
- Quality issue → no alternate source

**Solution**:
- Dual-source all ICs and high-value parts
- Test and qualify alternates at DVT phase
- Split orders to keep both suppliers active

---

### Mistake 4: Ignoring Lead Times

**Problem**: Order components 2 weeks before production (lead time is 16 weeks)

**Impact**: Production delay by 14 weeks (missed lead time)

**Solution**:
- Track lead times in BOM
- Order long-lead items (>12 weeks) early (don't wait for phase gate)
- Build lead time buffer into project schedule (add 20-30%)

---

### Mistake 5: Not Tracking BOM Revisions

**Problem**: BOM changes not documented, no version history

**Impact**:
- Can't reproduce older builds
- Root cause analysis impossible (which BOM version had issue?)
- Compliance issues (can't prove what was shipped)

**Solution**:
- Use BOM versioning (Rev A, B, C...)
- Document all changes in Change Log sheet
- Archive old BOM revisions (don't delete)

---

### Mistake 6: Forgetting Hidden Costs

**Problem**: BOM only includes component costs, ignores assembly/test/yield

**Impact**: COGS much higher than expected (BOM €75 → COGS €95)

**Solution**:
- Include all costs in COGS calculation:
  - BOM cost
  - Assembly labor
  - Test labor
  - Factory overhead
  - Yield loss (5-10% scrap)
- Track actual COGS vs budget

---

## BOM Management Tools

### Spreadsheet (Excel/Google Sheets)

**Pros**:
- Simple, everyone knows how to use
- Free (Excel comes with Office, Google Sheets is free)
- Easy to customize

**Cons**:
- Manual updates (error-prone)
- No automation (can't pull live pricing/stock)
- Limited collaboration (version conflicts)

**Best For**: Small projects, startups, <100 BOM lines

**Template**: Use our template ([07-bom-template.xlsx](../templates/07-bom-template.xlsx))

---

### PLM Tools (Product Lifecycle Management)

**Examples**:
- Arena PLM (arenasolutions.com) - cloud-based, $$$
- Duro (duro.io) - modern, hardware-focused, $$
- Aligni (aligni.com) - SMB-focused, $$
- Upchain (upchain.com) - PLM + ALM, $$$

**Pros**:
- Version control built-in (no manual versioning)
- Collaboration (multiple users, no conflicts)
- Integration (CAD, ERP, suppliers)
- Automation (stock checks, cost updates)

**Cons**:
- Expensive (€100-500/user/month)
- Learning curve (1-2 weeks onboarding)
- Overkill for small projects

**Best For**: Mature companies, multiple projects, >100 BOM lines, >5 users

---

### ERP Systems (Enterprise Resource Planning)

**Examples**:
- NetSuite (netsuite.com)
- SAP (sap.com)
- Odoo (odoo.com)

**Pros**:
- End-to-end (BOM → procurement → inventory → accounting)
- Scalable (handles large volumes)
- Integration (connects all business functions)

**Cons**:
- Very expensive (€50K-500K+ implementation)
- Overkill for hardware development (designed for operations)
- Long implementation (6-12 months)

**Best For**: Large companies, post-launch operations, not development

---

## Conclusion

**BOM management is critical for hardware project success.**

**Key Takeaways**:

1. **Start Early**: Create initial BOM in Concept phase (ROM estimate)
2. **Track Everything**: MPN, lifecycle, lead time, cost, RoHS, second source
3. **Version Control**: Document every change (Rev A, B, C...)
4. **Dual-Source**: Qualify alternates for critical components
5. **Cost at Volume**: Track BOM cost at target volume (1K, 10K, 100K)
6. **Update Regularly**: Quarterly reviews (lead times, lifecycle, costs)

**BOM Evolution**:
- Concept: ±50% accuracy, ROM estimate
- EVT: ±30% accuracy, detailed BOM
- DVT: ±10% accuracy, design freeze
- PVT: ±5% accuracy, manufacturing BOM
- MP: Actual costs, continuous optimization

**Common Pitfalls to Avoid**:
- Generic part numbers → Wrong parts ordered
- No lifecycle checks → Forced redesign mid-project
- Single-source → Supply chain risk
- Ignoring lead times → Production delays
- No version control → Can't reproduce builds

**BOM is living document** - update continuously, don't "set and forget"

---

## Related Resources

- [Project Charter Template](../templates/01-project-charter.md) - Initial BOM estimate in budget section
- [Phase Gate Checklist](../templates/03-phase-gate-checklist.md) - BOM review at each gate
- [Risk Register](../templates/02-risk-register.md) - Track component EOL and supply chain risks
- [Compliance Checklist](../templates/08-compliance-checklist.md) - RoHS/REACH tracking

**External Resources**:
- Octopart (octopart.com) - Component search and lifecycle data
- Mouser (mouser.com) - Authorized distributor
- Digi-Key (digikey.com) - Authorized distributor
- LCSC (lcsc.com) - Passives and connectors (China-based)

---

**Document Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit  
**Repository**: https://github.com/kathegrima/hardware-pm-starter-kit

---

*"A well-managed BOM is the foundation of profitable hardware products."*
