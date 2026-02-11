# 🛠️ Hardware Project Management Starter Kit

> **A comprehensive, ready-to-use toolkit for managing hardware product development from concept to mass production**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Issues](https://img.shields.io/github/issues/kathegrima/hardware-pm-starter-kit)](https://github.com/kathegrima/hardware-pm-starter-kit/issues)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/kathegrima/hardware-pm-starter-kit/pulls)

---

## 📖 What Is This?

The **Hardware Project Management Starter Kit** is an **open-source collection of templates, guides, and best practices** designed specifically for hardware product development teams. Whether you're building consumer electronics, medical devices, IoT products, or industrial hardware, this kit provides the structure you need to manage complex hardware projects successfully.

**Unlike software**, hardware development is:
- **Irreversible**: Can't patch after manufacturing
- **Costly**: Tooling, inventory, and rework are expensive
- **Long lead times**: 4-8 week sprints, months between phases
- **Highly regulated**: CE marking, FDA approval, ISO standards

This toolkit addresses these unique challenges with **battle-tested templates** adapted from real-world hardware projects across multiple industries.

---

## 🎯 Who Is This For?

This starter kit is designed for:

- **Hardware Project Managers** transitioning from software or new to hardware
- **Product Managers** leading hardware product development
- **Engineering Managers** overseeing hardware teams
- **Startup Founders** launching their first hardware product
- **Hardware Teams** at companies building physical products
- **Engineering Students** learning hardware project management

**No matter your industry**—consumer electronics, medical devices, IoT, robotics, industrial hardware, or automotive—these templates can be customized to fit your needs.

---

## ✨ What's Inside?

### 📂 Core Templates (`/templates/`)

**Project Management:**
- **[Project Charter](templates/01-project-charter.md)** - Define scope, goals, team, timeline, success criteria
- **[Risk Register](templates/02-risk-register.md)** - Identify, assess, and mitigate hardware-specific risks
- **[Phase Gate Checklist](templates/03-phase-gate-checklist.md)** - EVT, DVT, PVT gate criteria and reviews
- **[Sprint Planning Template](templates/04-sprint-planning.md)** - Adapted for 4-8 week hardware sprints
- **[Lessons Learned Template](templates/05-lessons-learned.md)** - Capture insights for future projects

**Planning & Tracking:**
- **[Product Requirements Document (PRD)](templates/06-prd-template.md)** - Technical and functional requirements
- **[Bill of Materials (BOM) Template](templates/07-bom-template.md)** - Component tracking with costs and lead times
- **[Compliance Checklist](templates/08-compliance-checklist.md)** - CE, FCC, RoHS, FDA, ISO standards
- **[Test Plan Template](templates/09-test-plan-template.md)** - Functional, reliability, and environmental testing
- **[Change Request Form](templates/10-change-request-form.md)** - Formal change control process

### 📚 Guides (`/guides/`)

- **[Getting Started Guide](guides/01-getting-started.md)** - Introduction to hardware PM fundamentals
- **[Industry Customization Guide](guides/02-customization-guide.md)** - Adapt templates for your sector (consumer electronics, medical, IoT, industrial, robotics, automotive)
- **[Phase Gate Deep Dive](guides/03-phase-gate-guide.md)** - Detailed walkthrough of EVT → DVT → PVT → MP
- **[Risk Management Guide](guides/04-risk-management-guide.md)** - Hardware-specific risk identification and mitigation
- **[Compliance Guide for EU/Italy](guides/05-compliance-guide-eu.md)** - CE marking, RoHS, REACH, MDR, Machinery Directive

### 🖼️ Visual Assets (`/assets/`)

- Project timeline diagrams
- Phase gate flowcharts
- Risk assessment matrices
- Hardware development lifecycle visuals

---

## 🚀 Quick Start

### Option 1: Clone This Repository

```bash
# Clone the repository
git clone https://github.com/kathegrima/hardware-pm-starter-kit.git

# Navigate to templates
cd hardware-pm-starter-kit/templates

# Copy and customize templates for your project
cp 01-project-charter.md ../my-project/project-charter.md
```

### Option 2: Download Individual Templates

Visit the [`/templates/`](templates/) folder and download the specific templates you need. Each template is a standalone Markdown file you can edit in any text editor.

### Option 3: Fork and Customize

**Recommended for teams**: Fork this repository to your organization's GitHub account. Customize templates to match your company's processes, then use it as your team's internal PM toolkit.

---

## 📋 How to Use This Toolkit

### Step 1: Start with the Getting Started Guide

Read **[Getting Started Guide](guides/01-getting-started.md)** to understand:
- How hardware PM differs from software PM
- The hardware development lifecycle (EVT → DVT → PVT → MP)
- Key concepts: phase gates, design freeze, tooling, compliance
- Common pitfalls and how to avoid them

### Step 2: Choose Your Industry

Review the **[Industry Customization Guide](guides/02-customization-guide.md)** to understand how to adapt templates for:
- **Consumer Electronics** - Fast time-to-market, competitive pressure
- **Medical Devices** - Regulatory compliance (FDA, MDR), long timelines
- **IoT & Connected Devices** - Hardware + firmware + cloud, cybersecurity
- **Industrial Hardware** - High reliability, harsh environments, long support
- **Robotics** - Complex integration, safety-critical systems
- **Automotive Electronics** - Zero-defect requirements, PPAP, ISO 26262

### Step 3: Kick Off Your Project

Use the **[Project Charter Template](templates/01-project-charter.md)** to:
1. Define project scope and objectives
2. Identify stakeholders and team structure
3. Set success criteria and KPIs
4. Establish timeline and budget
5. Identify major risks

### Step 4: Plan Each Phase

For each phase (EVT, DVT, PVT), use:
- **[Phase Gate Checklist](templates/03-phase-gate-checklist.md)** - Entry/exit criteria
- **[Sprint Planning Template](templates/04-sprint-planning.md)** - Sprint goals and backlog
- **[Risk Register](templates/02-risk-register.md)** - Update risks as you learn
- **[Test Plan Template](templates/09-test-plan-template.md)** - Define testing strategy

### Step 5: Track Progress and Learn

Throughout the project:
- Hold regular sprint reviews (every 4-8 weeks)
- Conduct phase gate reviews before advancing
- Update risk register and issue log weekly
- Capture lessons learned at major milestones

After project completion:
- Fill out **[Lessons Learned Template](templates/05-lessons-learned.md)**
- Update templates based on what worked/didn't work
- Share insights with your team and organization

---

## 🏭 The Hardware Development Lifecycle

Understanding the **phase-gate process** is critical for hardware PM. Here's the standard flow:

```
Concept → EVT → DVT → PVT → Mass Production → Maintenance → End-of-Life
   ↓       ↓      ↓      ↓          ↓              ↓            ↓
  Idea  Prototype Valid Design  Validate  Volume Mfg    Support   Disposal
                              Production
```

### Phase Descriptions

| Phase | Full Name | Duration | Purpose | Key Deliverables |
|-------|-----------|----------|---------|------------------|
| **Concept** | Concept Development | 4-8 weeks | Validate feasibility, create PRD | Product Requirements Document, initial BOM |
| **EVT** | Engineering Validation Test | 8-16 weeks | Prove core functionality works | Functional prototype, schematic, initial testing |
| **DVT** | Design Validation Test | 12-20 weeks | Validate design meets all specs | Production-intent design, compliance testing, reliability |
| **PVT** | Production Validation Test | 8-16 weeks | Validate manufacturing readiness | Pilot run, process validation, QC metrics |
| **MP** | Mass Production | Ongoing | Volume manufacturing | Shipping products, field data, ongoing improvements |

**Learn more**: Read the **[Phase Gate Deep Dive Guide](guides/03-phase-gate-guide.md)** for detailed criteria, common pitfalls, and decision frameworks for each phase.

---

## 🌍 European / Italian Compliance

**If you're developing hardware in Italy or for the European market**, compliance is mandatory. Key regulations:

| Requirement | Applies To | Timeline | Cost (Estimate) |
|-------------|-----------|----------|-----------------|
| **CE Marking** | All hardware products sold in EU | 3-6 months | €10K-€50K |
| **RoHS** | Electronics with restricted substances | 1-2 months | €5K-€15K |
| **REACH** | Products with chemicals > 0.1% | 2-4 months | €10K-€30K |
| **WEEE** | Electrical/electronic equipment | 1-2 months | €5K-€10K |
| **RED** | Radio/wireless devices | 4-8 months | €20K-€60K |
| **MDR** | Medical devices | 12-24 months | €100K-€500K+ |

**Learn more**: Read the **[Compliance Guide for EU/Italy](guides/05-compliance-guide-eu.md)** for detailed requirements, testing labs, Notified Bodies, and pre-compliance strategies.

---

## 🎓 Key Concepts

### Hardware vs Software PM

| Aspect | Software PM | Hardware PM |
|--------|-------------|-------------|
| **Iteration Speed** | Days to weeks | Months to quarters |
| **Changes After Release** | Can patch, update, rollback | Cannot modify once manufactured |
| **Marginal Cost** | Near zero for updates | High - tooling, inventory, rework |
| **Timeline** | 2-4 week sprints | 4-8 week sprints |
| **Risk Impact** | Bugs, performance issues | Years of cost, warranty claims |
| **Dependencies** | APIs, libraries | Component availability, supplier capacity |

### Design Freeze

**Design Freeze** is a critical milestone where no further design changes are allowed without formal change control. This typically occurs:
- Before DVT phase (for medical devices)
- Before PVT phase (for consumer electronics)
- Before tooling investment (for all hardware)

**Why it matters**: Tooling costs $50K-$500K+. Changes after tooling = expensive rework.

### Tooling

**Tooling** refers to the molds, dies, jigs, and fixtures required for manufacturing. Key facts:
- **Soft tooling** (prototype): 3D printed, CNC machined, low-volume, flexible
- **Hard tooling** (production): Injection molding, stamping dies, high-volume, expensive, inflexible
- **Lead time**: 8-16 weeks for hard tooling
- **Cost**: $50K-$500K+ depending on complexity

**Decision point**: Commit to hard tooling only after DVT phase confirms design is production-ready.

### Component Obsolescence

Electronic components have **lifecycles**. Manufacturers discontinue components ("End-of-Life" or EOL) regularly.

**Risk mitigation strategies**:
- Choose components with long lifecycle (automotive-grade, industrial-grade)
- Avoid components marked "Not Recommended for New Designs" (NRND)
- Design for second sources (alternate suppliers)
- Buy "lifetime buy" inventory before EOL (if product lifetime is known)

### Supply Chain Lead Times

Hardware PM must account for **long lead times**:
- **Standard components** (resistors, capacitors): 2-8 weeks
- **ICs, microcontrollers**: 8-20 weeks (sometimes 52+ weeks during shortages)
- **Custom components** (connectors, enclosures): 12-16 weeks
- **PCB fabrication**: 2-4 weeks (standard), 1 week (expedite)
- **PCB assembly**: 1-3 weeks

**Buffer strategy**: Add 20-30% time buffer for supply chain delays in your project timeline.

---

## 📊 Example Project Timeline

**Consumer Electronics Smartwatch** (8-month timeline):

```
Month 1-2: Concept Phase
  - Market research, PRD creation, initial BOM, feasibility study
  - Gate: PRD approved, business case validated

Month 3-4: EVT Phase (8 weeks)
  - Functional prototype, schematic design, firmware bring-up
  - Gate: Core functionality proven, major risks retired

Month 5-7: DVT Phase (12 weeks)
  - Production-intent design, compliance pre-testing, reliability testing
  - Gate: Design validated, ready for tooling

Month 7-8: PVT Phase (6 weeks)
  - Pilot build (500 units), process validation, cosmetic validation
  - Gate: Manufacturing ready, yield targets met

Month 8+: Mass Production
  - Ramp to volume, ongoing quality monitoring, field data collection
```

**Note**: This is an accelerated consumer electronics timeline. Medical devices take 24-36 months; automotive takes 36-60 months. See [Industry Customization Guide](guides/02-customization-guide.md) for timeline multipliers.

---

## 🤝 Contributing

We welcome contributions! This toolkit improves when hardware PMs share their experiences.

### How to Contribute

1. **Report Issues**: Found a template that doesn't work? [Open an issue](https://github.com/[username]/hardware-pm-starter-kit/issues)
2. **Suggest Improvements**: Have ideas for new templates or guides? [Start a discussion](https://github.com/[username]/hardware-pm-starter-kit/discussions)
3. **Submit Templates**: Created a template for a specific industry? [Submit a pull request](https://github.com/[username]/hardware-pm-starter-kit/pulls)
4. **Share Lessons Learned**: Write a case study or blog post about using these templates

**Contribution Guidelines**: See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed instructions.

---

## 📜 License

This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

**TL;DR**: You can use, modify, and distribute these templates freely, even commercially. Attribution appreciated but not required.

---

## 🙏 Acknowledgments

This toolkit was created by synthesizing best practices from:
- Industry-standard frameworks (NPI, APQP, ISO standards)
- Hardware PM practitioners across consumer electronics, medical, IoT, and industrial sectors
- Open-source project management communities
- Academic research on hardware product development

**Special thanks to**:
- Hardware PM practitioners who shared their templates and lessons learned
- Companies using phase-gate methodologies in the real world
- The open-source community for inspiration and feedback

---

## 📞 Support & Community

- **GitHub Issues**: [Report bugs or request features](https://github.com/[username]/hardware-pm-starter-kit/issues)
- **Discussions**: [Ask questions, share experiences](https://github.com/[username]/hardware-pm-starter-kit/discussions)
- **Contributing**: [Submit improvements](https://github.com/[username]/hardware-pm-starter-kit/pulls)

---

## 🗺️ Roadmap

**Current Version**: v1.0 (February 2026)

**Planned Features**:
- [ ] Video tutorials for each template
- [ ] Notion and Confluence versions of templates
- [ ] Excel/Google Sheets versions of trackers
- [ ] Gantt chart templates for project timelines
- [ ] Cost estimation calculators
- [ ] Supply chain tracking templates
- [ ] More industry-specific guides (aerospace, defense, wearables)
- [ ] Integration guides for tools (Jira, Asana, Monday.com)
- [ ] Case studies from real hardware projects

**Want to contribute to the roadmap?** [Join the discussion](https://github.com/[username]/hardware-pm-starter-kit/discussions)

---

## 📚 Recommended Resources

**Books**:
- *The Hardware Hacker* by Andrew "bunnie" Huang
- *Making Things Move* by Dustyn Roberts
- *Zero to One* by Peter Thiel (for startups)

**Websites**:
- [Instrumental Blog](https://instrumental.com/blog/) - Hardware manufacturing insights
- [Bolt Blog](https://www.bolt.io/blog/) - Hardware startup resources
- [Dragon Innovation Resources](https://www.dragoninnovation.com/resources) - Manufacturing guides

**Communities**:
- [r/hwstartups](https://www.reddit.com/r/hwstartups/) - Hardware startup community
- [Hardware Developers Slack](https://hardwaredevelopers.slack.com/) - Hardware PM discussions

---

## ⭐ Star This Repository

If you find this toolkit useful, **please star this repository** to help others discover it!

[![GitHub stars](https://img.shields.io/github/stars/[username]/hardware-pm-starter-kit?style=social)](https://github.com/[username]/hardware-pm-starter-kit)

---

## 📝 Changelog

### v1.0 (February 2026)
- Initial release
- 10 core templates covering project management, planning, and tracking
- 5 comprehensive guides (getting started, customization, phase gates, risk, compliance)
- Industry-specific customization for 6 sectors
- European/Italian compliance guidance

---

**Built with ❤️ for the hardware community**

*"Good templates are universal. Great templates are customized to your context."*

---

## Quick Links

- [📂 Templates](/templates/) - Ready-to-use PM templates
- [📚 Guides](/guides/) - In-depth guides and best practices
- [🎯 Getting Started](/guides/01-getting-started.md) - Start here if you're new
- [🌍 EU Compliance](/guides/05-compliance-guide-eu.md) - CE marking, RoHS, MDR
- [🏭 Industry Customization](/guides/02-customization-guide.md) - Adapt for your sector
- [🤝 Contributing](/CONTRIBUTING.md) - Help improve this toolkit
- [📜 License](/LICENSE) - MIT License

---

**Have questions?** [Open an issue](https://github.com/[username]/hardware-pm-starter-kit/issues) or [start a discussion](https://github.com/[username]/hardware-pm-starter-kit/discussions).
