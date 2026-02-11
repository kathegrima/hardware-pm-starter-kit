# Templates Directory - README

> Quick reference guide for hardware project management templates

---

## Available Templates

| Template | Purpose | When to Use | File |
|----------|---------|-------------|------|
| **Project Charter** | Define project scope, objectives, constraints | Project kickoff | [project-charter-hardware.md](./project-charter-hardware.md) |
| **Risk Register** | Track and mitigate hardware-specific risks | Ongoing throughout project | [risk-register-hardware.md](./risk-register-hardware.md) |
| **Phase Gate Checklist** | Gate review criteria for Concept → EVT → DVT → PVT → Production | Before each phase transition | [phase-gate-checklist.md](./phase-gate-checklist.md) |
| **Sprint Planning** | Plan hardware sprints with lead-time tracking | Every 4-8 week sprint | [sprint-planning-hardware.md](./sprint-planning-hardware.md) |
| **Lessons Learned** | Capture project insights for continuous improvement | Project completion or major milestones | [lessons-learned-template.md](./lessons-learned-template.md) |

---

## Acronyms & Abbreviations

### Hardware Development Phases

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **POC** | Proof of Concept | Initial feasibility demonstration |
| **EVT** | Engineering Validation Test | First functional prototypes (100-1,000 units) |
| **DVT** | Design Validation Test | Production-intent design validation (300-2,000 units) |
| **PVT** | Production Validation Test | Manufacturing process validation (1K-20K units) |
| **MP** | Mass Production | Volume manufacturing and shipment |

### Supply Chain & Manufacturing

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **BOM** | Bill of Materials | List of components and quantities needed |
| **CM** | Contract Manufacturer | External manufacturing partner |
| **DFM** | Design for Manufacturability | Design optimized for production efficiency |
| **DFMA** | Design for Manufacturing and Assembly | Design considering both manufacturing and assembly |
| **DFT** | Design for Test | Design with testability in mind |
| **EOL** | End of Life | Component discontinued by supplier |
| **FAI** | First Article Inspection | Initial production unit inspection |
| **IQC** | Incoming Quality Control | Inspection of received components |
| **IPQC** | In-Process Quality Control | Quality checks during assembly |
| **FQC** | Final Quality Control | Final inspection before shipping |
| **JIT** | Just-In-Time | Manufacturing strategy with minimal inventory |
| **NRE** | Non-Recurring Engineering | One-time development costs |
| **PCB** | Printed Circuit Board | Electronic circuit board |
| **SPC** | Statistical Process Control | Quality control using statistics |

### Compliance & Standards

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **CE** | Conformité Européenne | European product safety certification |
| **FCC** | Federal Communications Commission | US regulatory body for electronic devices |
| **UL** | Underwriters Laboratories | Product safety certification organization |
| **EMI** | Electromagnetic Interference | Unwanted electromagnetic emissions |
| **EMC** | Electromagnetic Compatibility | Device's ability to operate without causing/suffering EMI |
| **RoHS** | Restriction of Hazardous Substances | EU directive limiting hazardous materials |
| **REACH** | Registration, Evaluation, Authorization, and Restriction of Chemicals | EU chemical safety regulation |
| **WEEE** | Waste Electrical and Electronic Equipment | EU directive on e-waste disposal |
| **IP** | Ingress Protection | Rating for protection against dust/water (e.g., IP54) |
| **IEC** | International Electrotechnical Commission | International standards organization |
| **ISO** | International Organization for Standardization | Global standards body |
| **MIL-STD** | Military Standard | US military specifications (e.g., MIL-STD-810G) |

### Testing & Quality

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **FMEA** | Failure Mode and Effect Analysis | Systematic risk analysis methodology |
| **MTBF** | Mean Time Between Failures | Reliability metric |
| **DPMO** | Defects Per Million Opportunities | Quality metric |
| **RMA** | Return Merchandise Authorization | Product return process |
| **OTA** | Over-The-Air | Wireless firmware update mechanism |
| **QA** | Quality Assurance | Quality testing and validation |
| **Cpk** | Process Capability Index | Statistical measure of process capability |
| **EFFA** | Early Field Failure Analysis | Analysis of failures in early production units |
| **NPS** | Net Promoter Score | Customer satisfaction metric |

### Project Management

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **PM** | Project Manager | Project leader |
| **PRD** | Product Requirements Document | Detailed product specification |
| **ECO** | Engineering Change Order | Formal design change request |
| **ICD** | Interface Control Document | Specification of HW/SW interfaces |
| **DoD** | Definition of Done | Criteria for task completion |
| **MVP** | Minimum Viable Product | Product with core features only |
| **ROI** | Return on Investment | Financial metric for project value |
| **TRL** | Technology Readiness Level | Scale measuring technology maturity (1-9) |

### Firmware & Software

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **FW** | Firmware | Embedded software on hardware |
| **HW** | Hardware | Physical electronic components |
| **SW** | Software | Higher-level application code |
| **MCU** | Microcontroller Unit | Small computer on single chip |
| **RTOS** | Real-Time Operating System | OS for time-critical applications |
| **GPIO** | General Purpose Input/Output | Configurable pins on MCU |
| **PWM** | Pulse Width Modulation | Signal control technique |
| **I2C** | Inter-Integrated Circuit | Serial communication protocol |
| **SPI** | Serial Peripheral Interface | Synchronous serial communication |
| **UART** | Universal Asynchronous Receiver-Transmitter | Serial communication interface |
| **PID** | Proportional-Integral-Derivative | Control loop algorithm |
| **DRC** | Design Rule Check | PCB layout validation |

### Engineering Disciplines

| Acronym | Full Term | Description |
|---------|-----------|-------------|
| **ME** | Mechanical Engineering | Mechanical design discipline |
| **EE** | Electrical Engineering | Electrical design discipline |
| **CAD** | Computer-Aided Design | Design software (e.g., SolidWorks, Altium) |
| **CFD** | Computational Fluid Dynamics | Thermal/airflow simulation |

---

## References & Bibliography

### Hardware Product Development

1. **Instrumental - EVT, DVT, PVT Stage Gate Definitions**  
   https://instrumental.com/build-better-handbook/evt-dvt-pvt  
   *Industry-standard definitions for hardware development phases*

2. **ePower - Going from EVT to DVT to PVT: Milestones to Complete**  
   https://www.epowercorp.com/single-post/going-from-evt-to-dvt-to-pvt  
   *Comprehensive guide on hardware validation stages*

3. **Formlabs - Validation Testing in Product Development**  
   https://formlabs.com/blog/validation-testing-product-development-poc-evt-dvt-pvt-mp/  
   *Best practices for hardware testing and validation*

4. **EnCata - Hardware Product Development Stages**  
   https://www.encata.net/blog/overview-of-the-hardware-product-development-stages-explained-poc-evt-dvt-pvt  
   *Overview of hardware development lifecycle*

### Risk Management

5. **ClickUp - Hardware Designers Risk Register Template**  
   https://clickup.com/templates/risk-register/hardware-designers  
   *Risk management strategies for hardware projects*

6. **PRGNPI - 7 Best Practices for Managing Hardware Development Risk**  
   https://prgnpi.com/managing-hardware-development-risk-7-best-practices/  
   *Industry best practices for hardware risk mitigation*

7. **Supply Chain Risk Register Examples**  
   https://pinf.community/blog/supply-chain-risk-register-examples  
   *Templates and examples for supply chain risk tracking*

### Agile Hardware Development

8. **LinkedIn - Six Tips to Apply Scrum in Hardware Development**  
   https://www.linkedin.com/pulse/six-tips-apply-scrum-hardware-development-shuiqing-yu-joseph  
   *Adapting Agile methodologies for hardware projects*

9. **LinkedIn - Agile Hardware Development with Scrum**  
   https://www.linkedin.com/pulse/agile-hardware-development-scrum-semyon-veber-dnokc  
   *Practical guide for implementing Scrum in hardware teams*

10. **Enrique del Sol - Agile Hardware Development on Robotics**  
    https://enriquedelsol.com/2025/07/07/agile-hardware-development-on-robotics/  
    *Case study: Hybrid Agile-Stage-Gate for robotics (20-50% faster time-to-market)*

11. **Reddit - Scrum + Hardware Projects: How to Handle Long Lead Items**  
    https://www.reddit.com/r/scrum/comments/56rp85/scrum_hardware_projects_how_to_handle_long_lead/  
    *Community discussion on managing component lead times in Agile*

### Project Management

12. **PMO365 - Lessons Learned Template**  
    https://pmo365.com/blog/lessons-learned-template  
    *Best practices for capturing and applying project insights*

13. **Smartsheet - Lessons Learned Templates**  
    https://www.smartsheet.com/content/lessons-learned-template  
    *Free templates and guides for project retrospectives*

14. **Atlassian - Lessons Learned Template**  
    https://www.atlassian.com/software/confluence/templates/lessons-learned  
    *Confluence-based template for continuous improvement*

15. **Built In - Making the Most of a Project Post-Mortem**  
    https://builtin.com/software-engineering-perspectives/project-post-mortem  
    *Guide to conducting effective post-project reviews*

16. **Google SRE - Postmortem Culture**  
    https://sre.google/sre-book/postmortem-culture/  
    *Google's approach to blameless post-mortems*

### Supply Chain & Manufacturing

17. **Smartsheet - Supply Chain Risk Assessment Templates**  
    https://www.smartsheet.com/content/supply-chain-risk-assessment-templates  
    *Free templates for supply chain risk management*

18. **Hardware Supply Chain Security Strategies**  
    https://www.opswat.com/blog/securing-the-hardware-supply-chain  
    *Best practices for supply chain security*

19. **Meegle - Component Supply Chain Risk Assessment**  
    https://www.meegle.com/en_us/advanced-templates/hardware_development_/component_supply_chain_risk_assessment_template  
    *Template for assessing component availability risks*

### Phase Gate Process

20. **Wevolver - Complete Guide to Phase Gate Approach**  
    https://www.wevolver.com/article/the-complete-guide-to-the-phase-gate-approach-to-developing-a-hardware-product  
    *Comprehensive overview of Stage-Gate methodology for hardware*

21. **Smartsheet - Ultimate Guide to Phase Gate Process**  
    https://www.smartsheet.com/phase-gate-process  
    *Templates and best practices for phase gate implementation*

22. **Foundor.ai - Stage-Gate Process for Product Development**  
    https://foundor.ai/en/blog/stage-gate-process-produktentwicklung-guide  
    *Modern approach to Stage-Gate with Agile integration*

### Hardware vs Software PM

23. **Intech House - Core Differences: Hardware vs Software PM**  
    https://intechhouse.com/blog/core-differences-in-project-management-between-hardware-and-software-projects/  
    *Key differences in managing hardware vs software projects*

24. **GeeksforGeeks - Software vs Hardware Product Management**  
    https://www.geeksforgeeks.org/software-engineering/software-product-management-vs-hardware-product-management/  
    *Comparative analysis of PM approaches*

### Design Reviews

25. **Scribd - Hardware Design Review Checklist**  
    https://www.scribd.com/document/57290384/Hardware-Design-Review-Checklist  
    *Comprehensive checklist for hardware design reviews*

26. **HILPCB - Design Review Checklist for PCB Design**  
    https://hilpcb.com/en/blog/design-review-checklist-pcb-design-basics/  
    *PCB-specific design review guidelines*

---

## Template Usage Workflow

### For New Projects

1. **Start**: [Project Charter](./project-charter-hardware.md) - Define scope and objectives
2. **Plan**: [Sprint Planning](./sprint-planning-hardware.md) - Plan first sprint
3. **Track**: [Risk Register](./risk-register-hardware.md) - Identify and track risks
4. **Review**: [Phase Gate Checklist](./phase-gate-checklist.md) - Prepare for gate reviews
5. **Improve**: [Lessons Learned](./lessons-learned-template.md) - Capture insights at completion

### For Ongoing Projects

- **Weekly**: Update Risk Register with new risks and status changes
- **Every 4-8 weeks**: Complete Sprint Planning and retrospective
- **At Phase Gates**: Review Phase Gate Checklist and conduct gate review
- **Project End**: Complete Lessons Learned template and distribute

---

## Customization Guidelines

### How to Adapt Templates

**For Consumer Electronics**:
- Add UX/industrial design requirements to Project Charter
- Include user testing in Phase Gate Checklist (DVT phase)
- Add retail packaging requirements to Risk Register

**For Industrial Hardware**:
- Emphasize safety standards (ISO 13849, IEC 61508) in compliance section
- Add field service requirements to Phase Gate Checklist
- Include MTBF targets in Project Charter success criteria

**For Robotics**:
- Add motion control requirements to Project Charter
- Include sensor calibration in Phase Gate Checklist (EVT phase)
- Add human-robot interaction risks to Risk Register

**For Medical Devices**:
- Add FDA/MDR requirements to Phase Gate Checklist
- Include biocompatibility testing in DVT phase
- Add clinical validation requirements to Risk Register

### Template Placeholders

All templates use consistent placeholder syntax:

- `[PROJECT_NAME]` - Replace with actual project name
- `[PM_NAME]` - Replace with project manager name
- `[DATE]` - Replace with actual date
- `[X]` - Replace with numerical value
- `[PHASE]` - Replace with current development phase

---

## Contributing

Found a way to improve these templates? Create an issue or pull request with:
- **Problem**: What issue does the change address?
- **Solution**: What improvement do you propose?
- **Evidence**: What data or experience supports this change?

---

## License

These templates are provided under the [MIT License](../LICENSE).

Free to use, modify, and distribute for commercial or personal projects.

---

## Support

For questions or feedback:
- **GitHub Issues**: [Create an issue](https://github.com/kathegrima/hardware-pm-starter-kit/issues)
- **Discussions**: [Join the discussion](https://github.com/kathegrima/hardware-pm-starter-kit/discussions)

---

**Template Version**: v1.0  
**Last Updated**: February 2026  
**Maintained by**: KatheGrima
