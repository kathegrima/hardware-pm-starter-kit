# Hardware Risk Register

> **Purpose**: Track and mitigate risks specific to hardware product development  
> **Review**: Weekly at sprint planning + Phase gate reviews

---

**Navigation**: [🏠 Home](../) | [📋 All Templates](../templates/) | [📚 All Guides](../guides/)

---

## Quick Guide

**Risk Score** = Impact (1-5) × Likelihood (1-5)

| Priority | Score Range | Action |
|----------|-------------|--------|
| 🔴 **Critical** | 15-25 | Immediate action required |
| 🟠 **High** | 10-14 | Active mitigation in progress |
| 🟡 **Medium** | 5-9 | Monitor and plan mitigation |
| 🟢 **Low** | 1-4 | Accept and monitor |

---

## Project Info

- **Project**: `[PROJECT_NAME]`
- **PM**: `[PM_NAME]`
- **Last Update**: `[DATE]`
- **Next Review**: `[DATE]`

---

## Risk Assessment Scale

<details>
<summary><b>Click to expand Impact & Likelihood definitions</b></summary>

### Impact Scale (1-5)

| Score | Level | Description |
|:-----:|-------|-------------|
| 5 | **Critical** | Project failure, product recall, >50% budget overrun, >3mo delay, safety hazard |
| 4 | **High** | Major feature cut, 30-50% budget overrun, 1-3mo delay, compliance failure |
| 3 | **Medium** | Performance degraded, 15-30% budget overrun, 2-4wk delay, workaround needed |
| 2 | **Low** | Minor inconvenience, <15% budget impact, <2wk delay, cosmetic issues |
| 1 | **Minimal** | Negligible impact, absorbed within contingency |

### Likelihood Scale (1-5)

| Score | Level | Probability |
|:-----:|-------|-------------|
| 5 | **Almost Certain** | >70% - Expected to occur |
| 4 | **Likely** | 50-70% - Will probably occur |
| 3 | **Possible** | 30-50% - Might occur |
| 2 | **Unlikely** | 10-30% - Probably won't occur |
| 1 | **Rare** | <10% - Highly unlikely |

### Risk Priority Matrix

```
         LIKELIHOOD →
IMPACT   1    2    3    4    5
  ↓    ┌─────────────────────────┐
  5    │ 🟢  🟡  🟠  🔴  🔴  │
  4    │ 🟢  🟡  🟡  🟠  🔴  │
  3    │ 🟢  🟡  🟡  🟡  🟠  │
  2    │ 🟢  🟢  🟡  🟡  🟡  │
  1    │ 🟢  🟢  🟢  🟢  🟢  │
       └─────────────────────────┘
```

</details>

---

## 1. Supply Chain Risks

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **SC-001** | **Component EOL announced** mid-project (e.g., MCU) | 5 | 3 | **15** 🟠 | 🟡 Active | • 2nd source alternatives<br>• 6mo buffer stock<br>• Pin-compatible family | `[Name]` |
| **SC-002** | **Extended lead time** (8→16 weeks) | 4 | 4 | **16** 🔴 | 🟡 Active | • Dual-source qualification<br>• Early procurement<br>• Alternative specs | `[Name]` |
| **SC-003** | **Battery price surge** >30% | 3 | 3 | **9** 🟡 | 🟡 Active | • 12mo price lock-in<br>• Alternative chemistries<br>• 20% BOM contingency | `[Name]` |
| **SC-004** | **Single-source connector** | 5 | 2 | **10** 🟠 | 🟡 Active | • Standard alternative<br>• Extended supply agreement<br>• 12mo inventory | `[Name]` |
| **SC-005** | **PCB fab yield** drops <90% | 4 | 2 | **8** 🟡 | 🟢 Mitigated | • 2nd fab qualified<br>• Incoming QC<br>• Supplier SPC data | `[Name]` |
| **SC-006** | **Geopolitical supply disruption** | 4 | 3 | **12** 🟠 | 🟡 Active | • Diversify geography<br>• Policy monitoring<br>• Strategic inventory | `[Name]` |

<details>
<summary><b>➕ Add new supply chain risk</b></summary>

```markdown
| **SC-XXX** | [Description] | X | X | XX | 🟡 Active | • [Strategy 1]<br>• [Strategy 2] | [Owner] |
```

</details>

---

## 2. Technical Risks - Hardware

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **TH-001** | **Thermal failure**: Drivers exceed 100°C @ 40°C ambient | 5 | 4 | **20** 🔴 | 🔴 Critical | • CFD thermal sim<br>• Heatsinks + fans<br>• 80% power derate<br>• EVT thermal testing | `[Name]` |
| **TH-002** | **EMI non-compliance**: FCC fail by 8dB | 5 | 3 | **15** 🟠 | 🟡 Active | • Pre-compliance at EVT<br>• Shielding/filters<br>• PCB layout opt<br>• $15K retest budget | `[Name]` |
| **TH-003** | **Mechanical collision** (tolerance stack-up) | 4 | 3 | **12** 🟠 | 🟡 Active | • 3D tolerance analysis<br>• Extreme tolerance test<br>• +2mm clearance | `[Name]` |
| **TH-004** | **Power budget exceeded** (-25% battery life) | 4 | 4 | **16** 🔴 | 🟡 Active | • Subsystem profiling<br>• Sleep modes<br>• +20% capacity<br>• FW optimization | `[Name]` |
| **TH-005** | **Sensor drift** >10% (temp/humidity) | 3 | 3 | **9** 🟡 | 🟡 Active | • -10°C to +50°C test<br>• Calibration algo<br>• Conformal coating | `[Name]` |
| **TH-006** | **Vibration failure** (MIL-STD-810G) | 4 | 2 | **8** 🟡 | 🟢 Mitigated | • Strain relief<br>• DVT vibration test<br>• Conformal coating | `[Name]` |

---

## 3. Technical Risks - Firmware

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **TS-001** | **HW/SW integration delay** (HW late) | 5 | 4 | **20** 🔴 | 🔴 Critical | • Dev boards -4wk early<br>• HW emulation<br>• Reference platform dev | `[Name]` |
| **TS-002** | **Real-time deadline miss** (1ms loop) | 4 | 3 | **12** 🟠 | 🟡 Active | • RTOS guaranteed timing<br>• Code profiling<br>• Faster MCU option | `[Name]` |
| **TS-003** | **OTA bricking** devices | 5 | 2 | **10** 🟠 | 🟡 Active | • Dual-bank firmware<br>• Auto rollback<br>• Recovery bootloader | `[Name]` |

---

## 4. Manufacturing Risks

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **MF-001** | **Low yield** 75% vs 95% target | 5 | 3 | **15** 🟠 | 🟡 Active | • DVT DFMA review<br>• 100-unit pilot<br>• Poka-yoke fixtures<br>• Training program | `[Name]` |
| **MF-002** | **Assembly takes 2x time** | 3 | 4 | **12** 🟠 | 🟡 Active | • Time-motion study<br>• DFM simplification<br>• Assembly jigs<br>• Video training | `[Name]` |
| **MF-003** | **Test fixtures not ready** for PVT | 4 | 3 | **12** 🟠 | 🟡 Active | • Start design at DVT<br>• Parallel development<br>• $25K test budget | `[Name]` |
| **MF-004** | **Calibration adds 15min/unit** | 3 | 3 | **9** 🟡 | 🟡 Active | • Auto calibration<br>• Golden reference<br>• Self-cal firmware | `[Name]` |
| **MF-005** | **CM capacity** 1K vs 2K/mo target | 4 | 2 | **8** 🟡 | 🟢 Mitigated | • 2nd CM qualified<br>• Gradual ramp<br>• Build inventory | `[Name]` |

---

## 5. Compliance & Regulatory

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **CR-001** | **CE cert delay** (2 iterations) | 5 | 3 | **15** 🟠 | 🟡 Active | • EVT/DVT pre-test<br>• 6dB design margin<br>• Early lab consult<br>• 8wk cert window | `[Name]` |
| **CR-002** | **UL flammability fail** | 5 | 2 | **10** 🟠 | 🟡 Active | • UL V-0 materials<br>• DVT safety review<br>• Pre-test consultant | `[Name]` |
| **CR-003** | **RoHS violation** (supplier swap) | 4 | 2 | **8** 🟡 | 🟢 Mitigated | • Compliance certs in PO<br>• Incoming inspection<br>• Supplier audits | `[Name]` |
| **CR-004** | **Patent infringement claim** | 4 | 2 | **8** 🟡 | 🟡 Active | • Patent clearance<br>• Legal review<br>• Design-around ready | `[Name]` |
| **CR-005** | **Export control** (ITAR/EAR) | 3 | 2 | **6** 🟡 | 🟢 Mitigated | • Trade compliance<br>• Non-restricted alts<br>• Export license | `[Name]` |

---

## 6. Market & Business

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **MB-001** | **Competitor launches -3mo early** | 4 | 3 | **12** 🟠 | 🟡 Active | • Timeline acceleration<br>• Feature differentiation<br>• Competitor monitoring | `[Name]` |
| **MB-002** | **BOM cost +25% over target** | 4 | 3 | **12** 🟠 | 🟡 Active | • Value engineering<br>• Volume discounts<br>• MVP prioritization | `[Name]` |
| **MB-003** | **Demand -40% vs forecast** | 3 | 3 | **9** 🟡 | 🟡 Active | • Flexible CM contracts<br>• Phased ramp<br>• JIT ordering | `[Name]` |

---

## 7. Project Management

| ID | Risk | I | L | Score | Status | Mitigation | Owner |
|----|------|:-:|:-:|:-----:|:------:|------------|-------|
| **PM-001** | **Lead HW engineer leaves** @ DVT | 5 | 2 | **10** 🟠 | 🟡 Active | • Cross-training<br>• Design documentation<br>• Retention packages | `[Name]` |
| **PM-002** | **Scope creep** +3 features mid-dev | 4 | 4 | **16** 🔴 | 🟡 Active | • Change control<br>• Impact assessment<br>• Phase 2 parking lot | `[Name]` |
| **PM-003** | **HW/SW spec misalignment** | 4 | 3 | **12** 🟠 | 🟡 Active | • Weekly integration sync<br>• Interface control doc<br>• Daily standups | `[Name]` |

---

## Risk Summary

### By Priority

```
🔴 Critical (15-25):  5 risks  ⚠️  IMMEDIATE ACTION REQUIRED
🟠 High (10-14):     15 risks  →  Active mitigation in progress
🟡 Medium (5-9):      7 risks  →  Monitor regularly
🟢 Low (1-4):         0 risks  →  Accept and track
```

### By Status

- 🔴 **Critical Attention**: 2 risks (TH-001, TS-001)
- 🟡 **Active Monitoring**: 23 risks
- 🟢 **Mitigated**: 4 risks
- ⚪ **Closed**: 0 risks

### Top 5 Risks (by Score)

1. **TH-001** - Thermal management failure → **Score: 20** 🔴
2. **TS-001** - HW/SW integration delays → **Score: 20** 🔴
3. **SC-002** - Extended component lead times → **Score: 16** 🔴
4. **TH-004** - Power budget exceeded → **Score: 16** 🔴
5. **PM-002** - Scope creep → **Score: 16** 🔴

---

## Best Practices

### Risk Review Cadence

| Frequency | Scope | Participants |
|-----------|-------|--------------|
| **Daily** | 🔴 Critical risks only | PM + Risk owners |
| **Weekly** | All active risks | Full team at sprint planning |
| **Bi-weekly** | Risk register update | Cross-functional review |
| **Phase Gates** | Complete assessment | Stakeholders + leadership |

### Mitigation Strategies

| Strategy | When to Use | Example |
|----------|-------------|---------|
| **Avoid** | Eliminate risk completely | Remove single-source component from design |
| **Reduce** | Lower probability/impact | Pre-compliance testing, dual sourcing |
| **Transfer** | Shift to another party | Insurance, supplier warranties, outsourcing |
| **Accept** | Score acceptable | Monitor with contingency plan |

### Phase-Specific Focus

- **Concept**: Technical feasibility, market validation
- **EVT**: Component availability, thermal/power, HW/SW integration
- **DVT**: Compliance testing, manufacturing yield, BOM cost
- **PVT**: Production capacity, test coverage, quality metrics

### Risk Identification Sources

- FMEA (Failure Mode and Effect Analysis)
- Design reviews and technical discussions
- Supplier communications and market intelligence
- Lessons learned from past projects
- Team brainstorming sessions

---

## Status Definitions

| Icon | Status | Description | Action |
|:----:|--------|-------------|--------|
| 🔴 | **Critical** | Requires immediate escalation | Daily review, leadership involved |
| 🟡 | **Active** | Mitigation plan in progress | Regular monitoring, execute plan |
| 🟢 | **Mitigated** | Actions complete, risk acceptable | Watch for re-emergence |
| 🔵 | **Occurred** | Risk event happened | Manage impact, capture lessons |
| ⚪ | **Closed** | No longer applicable | Archive for reference |

---

## Quick Actions

### Adding a New Risk

1. Choose appropriate category (SC, TH, TS, MF, CR, MB, PM)
2. Assign next sequential ID (e.g., SC-007)
3. Score Impact × Likelihood
4. Define concrete mitigation steps
5. Assign owner and target date
6. Update summary dashboard

### Escalating a Risk

> [!WARNING]
> When risk score ≥ 15 or status changes to 🔴:

1. Alert PM and executive sponsor immediately
2. Schedule mitigation review within 24 hours
3. Allocate additional resources if needed
4. Document escalation in notes section

---

## Notes & Lessons Learned

> [!NOTE]
> Use this section to capture key insights and improve future risk management

### Key Insights
*[Document patterns, surprises, and recurring themes]*

### Early Warning Indicators
*[Track leading signals that predict risk occurrence]*

### Process Improvements
*[Capture ideas for next project]*

---

**Document Version**: 1.0  
**Template**: hardware-pm-starter-kit v1.0  
**Last Review**: `[DATE]`  
**Next Review**: `[DATE]`

---

## Related Templates

- [Project Charter](./project-charter-hardware.md) - Project scope and constraints
- [Phase Gate Checklist](./phase-gate-checklist.md) - Gate review criteria
- [Sprint Planning](./sprint-planning-hardware.md) - Hardware sprint template
- [Lessons Learned](./lessons-learned-template.md) - Post-project review
