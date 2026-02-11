# Project Charter Template

> **Hardware Project Charter - Define your project before you start**

---

## Document Information

| Field | Details |
|-------|---------|
| **Project Name** | [Enter project name] |
| **Version** | [e.g., v1.0] |
| **Project Manager** | [Name] |
| **Date Created** | [YYYY-MM-DD] |
| **Last Updated** | [YYYY-MM-DD] |
| **Status** | [ ] Draft   [ ] Approved   [ ] Active   [ ] Complete |

---

## Executive Summary

**One-paragraph overview of the project**:
[Describe in 2-3 sentences: What product are we building? Why? For whom? Expected timeline and budget?]

**Example**:
*This project will develop the SmartSense Indoor Air Quality Monitor, a battery-powered sensor device for health-conscious consumers. The product will measure CO2, PM2.5, temperature, humidity, and VOCs with mobile app integration. Target launch is Q4 2026 with a 14-month development timeline and €350K total budget.*

---

## Project Objectives

### Business Objectives

**Why are we doing this project?**

- [ ] Enter new market segment: [specify]
- [ ] Revenue target: [e.g., €2.5M in Year 1]
- [ ] Market share goal: [e.g., capture 15% of EU air quality monitor market]
- [ ] Strategic positioning: [e.g., establish brand in smart home category]
- [ ] Replace legacy product: [specify which]
- [ ] Competitive response: [respond to competitor threat]
- [ ] Other: [describe]

---

### Product Objectives

**What will this product achieve?**

1. **Primary goal**: [e.g., Provide real-time indoor air quality monitoring accessible to non-technical users]
2. **Secondary goal**: [e.g., Enable proactive health management through air quality insights]
3. **Technical goal**: [e.g., Achieve >6-month battery life with <5-second response time]

---

### Success Criteria

**How will we measure success?**

| Metric | Target | Measurement Method |
|--------|--------|--------------------|
| **Time to Market** | [e.g., 14 months from kickoff to first shipment] | Project schedule tracking |
| **Product Performance** | [e.g., Battery life >6 months, sensor accuracy ±3%] | Lab testing validation |
| **Cost Target** | [e.g., COGS <€25, total NRE <€300K] | BOM costing, budget tracking |
| **Quality Target** | [e.g., <2% return rate, >95% manufacturing yield] | Quality metrics post-launch |
| **Customer Satisfaction** | [e.g., NPS >50 within 6 months of launch] | Customer surveys |
| **Business Goal** | [e.g., 50,000 units sold in Year 1] | Sales data |

---

## Project Scope

### In Scope

**What IS included in this project?**

✅ **Deliverables**:
1. Hardware design (schematic, PCB, BOM)
2. Mechanical design (enclosure, assembly drawings)
3. Firmware development (embedded software)
4. Mobile app (iOS + Android)
5. Manufacturing setup (tooling, CM qualification)
6. Certifications (CE, FCC, RoHS)
7. Packaging design
8. User documentation (quick start guide, manual)
9. Production of first 5,000 units

✅ **Phases Included**:
- [ ] Concept phase
- [ ] EVT (Engineering Validation Test)
- [ ] DVT (Design Validation Test)
- [ ] PVT (Production Validation Test)
- [ ] MP (Mass Production ramp)

---

### Out of Scope

**What IS NOT included in this project?**

❌ **Excluded**:
1. Cloud infrastructure (deferred to Phase 2)
2. Voice assistant integration (future version)
3. Multi-device sync (V2.0 feature)
4. International certifications beyond EU/US (Canada, Australia deferred)
5. Retail distribution partnerships (online-only launch)
6. Marketing campaigns (separate project)

**Rationale**: [Briefly explain why these are excluded - e.g., time constraints, budget limits, market validation needed first]

---

### Assumptions

**Key assumptions we're making**:

1. [e.g., Component lead times remain <16 weeks throughout development]
2. [e.g., Contract manufacturer has capacity for 5,000-unit pilot run in Q3 2026]
3. [e.g., Compliance testing passes on first attempt (pre-testing conducted)]
4. [e.g., Engineering team remains stable (no key personnel turnover)]
5. [e.g., Customer requirements captured in PRD remain valid]

---

### Constraints

**Known limitations and boundaries**:

1. **Budget**: [e.g., Total budget capped at €350K (€270K NRE + €80K initial production)]
2. **Timeline**: [e.g., Must launch by Q4 2026 to capture holiday season]
3. **Resources**: [e.g., 1x Hardware Engineer, 1x Firmware Engineer, 0.5x Mechanical Engineer, 1x PM]
4. **Technical**: [e.g., Must use BLE 5.0 (not BLE 5.2) due to smartphone compatibility requirements]
5. **Regulatory**: [e.g., Must achieve CE marking before any EU sales]
6. **Manufacturing**: [e.g., Limited to CMs with ISO 9001 certification]

---

## Stakeholders

### Project Team

| Role | Name | Responsibilities | Allocation |
|------|------|-----------------|------------|
| **Project Manager** | [Name] | Timeline, budget, coordination, risk management | 100% |
| **Hardware Engineer** | [Name] | Schematic, PCB design, component selection | 100% |
| **Firmware Engineer** | [Name] | Embedded software, drivers, power management | 100% |
| **Mechanical Engineer** | [Name] | Enclosure design, thermal analysis, DFM | 50% |
| **Mobile App Developer** | [Name / External] | iOS & Android app development | [TBD] |
| **Quality Engineer** | [Name] | Test plans, validation, compliance | 50% |
| **Manufacturing Engineer** | [Name / CM] | DFM review, process optimization, CM liaison | 25% |

---

### Key Stakeholders

| Stakeholder | Role | Interest / Influence | Engagement Strategy |
|-------------|------|---------------------|---------------------|
| **[Name]** | Executive Sponsor | High interest, high influence - budget approval authority | Weekly status updates, gate review participation |
| **[Name]** | Engineering Director | Medium interest, high influence - resource allocation | Bi-weekly syncs, escalation path |
| **[Name]** | Quality Director | High interest, medium influence - compliance approval | Gate reviews, test plan reviews |
| **[Name]** | Supply Chain Manager | Medium interest, medium influence - component sourcing | Monthly syncs, BOM reviews |
| **[Name]** | Marketing Lead | Low interest during dev, high at launch | Quarterly updates, launch planning in PVT |

---

### Communication Plan

**How will we keep stakeholders informed?**

| Audience | Method | Frequency | Content |
|----------|--------|-----------|---------|
| **Core Team** | Daily standup (Slack) | Daily (async) | Blockers, progress, questions |
| **Core Team** | Team sync meeting | 2x per week | Design discussions, decisions, integration |
| **Project Sponsor** | Status report | Weekly | Timeline, budget, risks, decisions needed |
| **Stakeholders** | Steering committee | Monthly | Milestone progress, budget burn, major risks |
| **Entire Company** | Demo day | After each phase gate | Show working prototypes, share learnings |

---

## Project Timeline

### High-Level Schedule

| Phase | Duration | Start Date | End Date | Key Milestone |
|-------|----------|------------|----------|---------------|
| **Concept** | 4 weeks | [YYYY-MM-DD] | [YYYY-MM-DD] | PRD approved |
| **EVT** | 12 weeks | [YYYY-MM-DD] | [YYYY-MM-DD] | Functional prototype validated |
| **DVT** | 16 weeks | [YYYY-MM-DD] | [YYYY-MM-DD] | Design freeze, compliance pre-test passed |
| **Tooling** | 10 weeks | [YYYY-MM-DD] | [YYYY-MM-DD] | Production molds complete |
| **PVT** | 10 weeks | [YYYY-MM-DD] | [YYYY-MM-DD] | Manufacturing validated, certifications complete |
| **MP Ramp** | 4 weeks | [YYYY-MM-DD] | [YYYY-MM-DD] | First 5,000 units shipped |

**Total Duration**: [e.g., 14 months from kickoff to first customer shipment]

---

### Critical Path Items

**Dependencies that could delay the entire project**:

1. **Component procurement**: [e.g., CO2 sensor has 16-week lead time - must order by Week 8]
2. **Tooling timeline**: [e.g., Injection molds take 10 weeks - must kick off after DVT freeze]
3. **Certification testing**: [e.g., FCC lab booked 6 weeks in advance - must schedule in DVT]
4. **Firmware integration**: [e.g., Hardware + firmware integration testing needs 4 weeks before PVT]

---

## Budget

### Budget Summary

| Category | Estimated Cost | Actual Cost | Variance | Notes |
|----------|----------------|-------------|----------|-------|
| **Engineering Labor** | [€80,000] | [TBD] | - | Internal team + contractors |
| **Prototyping (EVT/DVT/PVT)** | [€30,000] | [TBD] | - | PCB fab, assembly, enclosures |
| **Tooling** | [€80,000] | [TBD] | - | Injection molds, jigs, fixtures |
| **Certifications** | [€30,000] | [TBD] | - | CE, FCC, RoHS testing |
| **Mobile App Development** | [€50,000] | [TBD] | - | iOS + Android contractor |
| **First Production Run** | [€80,000] | [TBD] | - | 5,000 units @ €16 COGS (includes assembly) |
| **Contingency (15%)** | [€50,000] | [TBD] | - | Buffer for unknowns |
| **TOTAL** | **€400,000** | **[TBD]** | **-** | - |

---

### Budget Approval

- **Approved by**: [Name, Title]
- **Approval Date**: [YYYY-MM-DD]
- **Budget Authority**: [Who can approve changes to budget?]
- **Change Control**: [How are budget changes requested and approved?]

---

## Risks

### Top 5 Risks

| Risk | Probability | Impact | Mitigation Strategy | Owner |
|------|-------------|--------|---------------------|-------|
| **Component shortage or EOL** | Medium | High | Select Active-status components only, identify second sources early, order long-lead items in EVT | [HW Engineer] |
| **Certification failure at DVT** | Medium | High | Pre-compliance testing in EVT, engage test lab early for design guidance | [Quality Engineer] |
| **Battery life below target** | High | Medium | Firmware optimization for low power, prototype testing early, backup battery option | [FW Engineer] |
| **Tooling cost overrun** | Medium | Medium | Get quotes from 3 vendors, simplify mechanical design, phased tooling approach | [Mech Engineer] |
| **Schedule slip due to integration issues** | Medium | High | Early hardware-firmware integration testing, weekly cross-functional syncs | [PM] |

**Risk Management Approach**:
- Risk register updated weekly
- Risks reviewed in every team meeting
- High-impact risks escalated to sponsor immediately
- Monthly risk review with stakeholders

---

## Dependencies

### External Dependencies

**What do we need from outside our team?**

1. **Component suppliers**: [e.g., CO2 sensor from Sensirion - 16-week lead time]
2. **Contract manufacturer**: [e.g., CM capacity confirmed for Q3 2026 production slot]
3. **Test lab**: [e.g., FCC/CE testing lab availability - must book 6 weeks in advance]
4. **Mobile app developer**: [e.g., External contractor - contract signed by Week 4]
5. **Legal/regulatory**: [e.g., Trademark clearance for product name]

---

### Internal Dependencies

**What do we need from other teams?**

1. **Marketing**: [Product positioning and pricing finalized by DVT phase]
2. **Sales**: [Distribution channel strategy decided by PVT phase]
3. **IT**: [Cloud infrastructure readiness if needed for V2 features]
4. **Finance**: [Budget approval for tooling investment (€80K) before DVT complete]
5. **Legal**: [Terms of service and privacy policy for mobile app]

---

## Governance

### Decision-Making Authority

**Who decides what?**

| Decision Type | Decision Maker | Escalation Path |
|--------------|----------------|-----------------|
| **Day-to-day technical choices** | Engineering team | PM → Engineering Director |
| **Schedule adjustments <2 weeks** | PM | Sponsor |
| **Budget variance <10%** | PM | Sponsor |
| **Scope changes** | PM + Sponsor | Steering Committee |
| **Design freeze / gate advancement** | Phase Gate Review Board | Executive Sponsor |
| **Budget variance >10%** | Sponsor | CFO |

---

### Phase Gate Reviews

**Formal decision points to proceed to next phase**:

**Gate Review Board Members**:
- Project Sponsor (chair)
- Engineering Director
- Quality Director
- Manufacturing Lead
- PM (presents)

**Gate Review Process**:
1. PM prepares gate review package (2 weeks before gate)
2. Package distributed to board (1 week before gate)
3. Gate review meeting (2 hours)
4. Go/No-Go decision documented
5. Action items tracked if conditional approval

**Gate Criteria**:
- All phase deliverables complete
- Test results meet acceptance criteria
- Risks identified and mitigation plans in place
- Budget and schedule on track (or variance explained)
- Next phase plan ready

---

### Change Control

**How do we handle changes after approval?**

**Change Request Process**:
1. Anyone can submit change request (use template)
2. PM reviews for impact (timeline, budget, scope)
3. PM presents to Change Control Board (CCB) if material
4. CCB approves/rejects/defers
5. Approved changes updated in project plan and PRD

**Change Control Board (CCB)**:
- PM (facilitates)
- Engineering Lead
- Sponsor
- Quality Lead (for post-design-freeze changes)

**Change Types**:
- **Minor**: <1 week schedule impact, <€5K cost → PM approval
- **Major**: >1 week schedule impact OR >€5K cost → CCB approval
- **Critical**: Scope change, >1 month delay, >€20K cost → Sponsor + Steering Committee

---

## Success Criteria & Definition of Done

### Phase Completion Criteria

**EVT Phase Complete When**:
- [ ] Functional prototype demonstrates core features
- [ ] Key sensors validated (accuracy within spec)
- [ ] Power consumption measured and within 20% of target
- [ ] Wireless range tested (meets minimum range requirement)
- [ ] Major technical risks retired
- [ ] EVT gate review passed

**DVT Phase Complete When**:
- [ ] Production-intent design complete
- [ ] All environmental tests passed (temp, humidity, drop, vibration)
- [ ] EMC pre-compliance testing passed
- [ ] User experience validated (beta testing with 20+ users)
- [ ] Design freeze declared
- [ ] BOM costs validated (within 10% of target)
- [ ] Manufacturing DFM review complete
- [ ] DVT gate review passed
- [ ] Tooling approved and kicked off

**PVT Phase Complete When**:
- [ ] Pilot build complete (200-500 units)
- [ ] Manufacturing yield >95%
- [ ] All certifications complete (CE, FCC)
- [ ] Quality control process validated
- [ ] Packaging and logistics validated
- [ ] Final cost within 5% of target
- [ ] PVT gate review passed
- [ ] Manufacturing release approved

**Project Complete When**:
- [ ] First 5,000 units manufactured and shipped
- [ ] No critical field issues reported (first 30 days)
- [ ] Post-launch review conducted
- [ ] Lessons learned documented
- [ ] Project documentation archived
- [ ] Project closure approved by sponsor

---

## Lessons Learned (Capture Throughout Project)

**What's working well?**
- [Add items as project progresses]

**What could be improved?**
- [Add items as project progresses]

**Key decisions and rationale**:
- [Document major decisions for future reference]

**Things to do differently next time**:
- [Capture learnings to improve future projects]

---

## Approvals

### Project Charter Approval

**By signing below, stakeholders agree to the project objectives, scope, timeline, budget, and governance outlined in this charter.**

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Project Sponsor** | [Name] | _____________ | [Date] |
| **Project Manager** | [Name] | _____________ | [Date] |
| **Engineering Director** | [Name] | _____________ | [Date] |
| **Quality Director** | [Name] | _____________ | [Date] |
| **Finance Approval** | [Name] | _____________ | [Date] |

---

## Appendices

### Appendix A: Related Documents

**Supporting documentation**:
- [ ] Product Requirements Document (PRD)
- [ ] Risk Register (detailed version)
- [ ] Project Schedule (Gantt chart)
- [ ] Budget Breakdown Spreadsheet
- [ ] Organizational Chart
- [ ] Communication Plan (detailed)

---

### Appendix B: Acronyms & Definitions

- **CCB**: Change Control Board
- **CE**: Conformité Européenne (EU compliance marking)
- **CM**: Contract Manufacturer
- **COGS**: Cost of Goods Sold
- **DFM**: Design for Manufacturability
- **DVT**: Design Validation Test
- **EMC**: Electromagnetic Compatibility
- **EVT**: Engineering Validation Test
- **FCC**: Federal Communications Commission (US)
- **MP**: Mass Production
- **NPS**: Net Promoter Score
- **NRE**: Non-Recurring Engineering
- **PM**: Project Manager
- **PRD**: Product Requirements Document
- **PVT**: Production Validation Test
- **RoHS**: Restriction of Hazardous Substances

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| v0.1 | [Date] | [Name] | Initial draft |
| v1.0 | [Date] | [Name] | Approved version for project kickoff |

---

**END OF PROJECT CHARTER**

---

## How to Use This Template

1. **Complete During Concept Phase**: The Project Charter should be one of the first documents created, alongside or immediately after the PRD.

2. **Get Buy-In Early**: Circulate draft to all stakeholders and incorporate feedback before finalizing. A charter everyone agrees to prevents scope creep later.

3. **Be Realistic**: Don't lowball timelines or budgets to get approval. Unrealistic charters lead to failed projects.

4. **Update as Needed**: The charter is not set in stone. If major changes occur (scope, budget, timeline), update the charter and get re-approval.

5. **Reference Often**: Use the charter in every gate review and status meeting to ensure project stays aligned with original objectives.

6. **Lock Before EVT**: Once approved, the charter should be locked for EVT phase. Changes require formal change control process.

7. **One-Page Summary**: Create a one-page executive summary of the charter for quick reference and presentations.

---

**Template Version**: v1.0  
**Last Updated**: February 2026  
**Part of**: Hardware PM Starter Kit

---

*"A good charter aligns the team. A great charter prevents expensive misunderstandings."*
