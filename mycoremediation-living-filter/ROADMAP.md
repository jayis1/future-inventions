# Mycoremediation Living Filter — Development Roadmap

> *"From enzyme evolution to universal clean water: a decade-long journey to end forever chemicals."*

---

## Overview

This roadmap traces the path from laboratory concept to global deployment of the Mycoremediation Living Filter (MLF). The journey spans 10 years across 5 phases, each with defined milestones, success criteria, risk gates, and funding requirements.

**Total estimated R&D investment: $43–112M over 10 years**
**Target timeline: First household units available by Year 8, global deployment by Year 10+**

---

## Phase 1: Enzyme Engineering (Years 1–3)

**Goal:** Evolve perfluoroalkyl defluorinase enzymes that can cleave C–F bonds at catalytic rates sufficient for practical water treatment, and express them in *Phanerochaete chrysosporium*.

### Year 1: Foundation

| Quarter | Milestone | Deliverable | Success Criteria |
|---------|-----------|-------------|------------------|
| Q1 | PACE system setup | Continuous evolution reactor operational | Demonstrated evolution of model dehalogenase (C–Cl substrate) with 100× improvement |
| Q2 | Target selection | Identify 5+ candidate reductive dehalogenases with trace C–F activity | k_cat > 0.001 s⁻¹ on PFOA |
| Q3 | Evolution Round 1 | 50 rounds of PACE on top 3 candidates | k_cat > 0.1 s⁻¹ on PFOA (50× improvement) |
| Q4 | Evolution Round 2 | 100 rounds of PACE with increasingly stringent selection | k_cat > 0.5 s⁻¹ on PFOA |

**Budget:** $2M (lab equipment, PACE reactor, personnel, sequencing)
**Key Risk:** PACE system may not efficiently evolve C–F bond cleavage. **Mitigation:** Run parallel computational enzyme design (AlphaFold3 + RFDiffusion) to generate de novo candidates.

### Year 2: Optimization

| Quarter | Milestone | Deliverable | Success Criteria |
|---------|-----------|-------------|------------------|
| Q1 | Evolution Round 3 | 200 total rounds of PACE | k_cat > 2.0 s⁻¹ on PFOA |
| Q2 | C6–C10 substrate range | Test evolved enzymes on PFHxS, PFBS, GenX | k_cat > 1.0 s⁻¹ on C6 substrates |
| Q3 | Fungal expression system | Construct *P. chrysosporium* expression vector with gpdA promoter | Enzyme expression at >1% total protein |
| Q4 | Co-expression system | Express ePRD + FAcD in same fungal strain | Both enzymes active; no metabolic burden |

**Budget:** $2M (personnel, sequencing, proteomics, fermentation)
**Key Risk:** Enzyme may lose activity when expressed in fungal host. **Mitigation:** Codon optimization; alternative promoters; secretion signal screening.

### Year 3: Integration & Validation

| Quarter | Milestone | Deliverable | Success Criteria |
|---------|-----------|-------------|------------------|
| Q1 | Cell-free enzyme assay | Purified enzyme system degrading PFOA in buffer | >90% PFOA removal at 1 mg/L in 24 hours |
| Q2 | Whole-cell assay | *P. chrysosporium* (engineered) degrading PFOA in liquid culture | >80% PFOA removal at 100 μg/L in 48 hours |
| Q3 | *Geobacter/Shewanella* integration | Demonstrate bioelectrochemical rate enhancement | 10× rate increase with 0.5 V applied voltage |
| Q4 | Phase 1 Gate Review | Independent verification of enzyme activity and expression | k_cat > 5 s⁻¹; >90% PFOA removal at 1 mg/L |

**Budget:** $3M (personnel, analytical chemistry, independent verification)
**Go/No-Go Gate:** k_cat > 5 s⁻¹ on C6–C10 PFAAs. If not achieved, pivot to multi-enzyme cascade approach.

---

## Phase 2: Consortium Development (Years 2–4)

**Goal:** Establish a stable, self-regulating fungal-bacterial consortium with quorum-sensing regulation, and demonstrate >90% PFAS removal in bench-scale reactors.

### Year 2 (Overlap with Phase 1)

| Quarter | Milestone | Deliverable | Success Criteria |
|---------|-----------|-------------|------------------|
| Q3 | *Geobacter* biofilm optimization | Demonstrate stable anode biofilm on graphite fiber | >90% coulombic efficiency; stable for >30 days |
| Q4 | QS circuit design | Synthetic LasI/LasR circuit in *P. chrysosporium* | QS-activated GFP expression with >10× dynamic range |

### Year 3

| Quarter | Milestone | Deliverable | Success Criteria |
|---------|-----------|-------------|------------------|
| Q1 | Co-culture establishment | *P. chrysosporium* + *Geobacter* + *Shewanella* in same reactor | Stable populations for >60 days; no competitive exclusion |
| Q2 | QS-PFAS linkage | QS circuit activated by F⁻ release (riboswitch) | 3× increase in ePRD expression when PFAS > 10 μg/L |
| Q3 | Bench reactor (1 L) | Continuous flow reactor with all components | >90% PFOA removal at 10 μg/L influent |
| Q4 | Kill switch validation | Theophylline-withdrawal kill switch + auxotrophy | 100% kill within 6 hours outside reactor conditions |

### Year 4

| Quarter | Milestone | Deliverable | Success Criteria |
|---------|-----------|-------------|------------------|
| Q1 | Bench reactor (10 L) | Scale-up by 10× | Same performance at 10 L; >90% removal |
| Q2 | Mycelial matrix optimization | Lignocellulosic scaffold composition and colonization protocol | Matrix porosity 90–95%; k_obs > 1.0 h⁻¹ |
| Q3 | Long-term stability test | 90-day continuous operation at bench scale | >90% removal maintained; enzyme activity >80% initial |
| Q4 | Phase 2 Gate Review | Independent verification of consortium stability and PFAS removal | >90% PFAS removal; consortium stable for >90 days |

**Budget:** $5M (personnel, bioreactor equipment, analytical, sequencing, independent verification)
**Go/No-Go Gate:** >90% PFAS removal at bench scale (10 L) with 90-day stability.

---

## Phase 3: Pilot Reactor (Years 3–5)

**Goal:** Build and operate a 1 m³/day pilot reactor with real contaminated groundwater, demonstrating >99% PFAS destruction with F⁻ mass balance verification.

### Year 3 (Late) — Pilot Design

| Activity | Deliverable |
|----------|-------------|
| Pilot reactor engineering design | P&ID, PFD, mechanical drawings |
| Site selection | Partnership with 3 contaminated sites (military base, airport, industrial) |
| Regulatory pre-consultation | EPA/State regulatory pre-meeting for contained bioremediation |

### Year 4

| Quarter | Milestone | Success Criteria |
|---------|-----------|------------------|
| Q1 | Pilot reactor fabrication | 1 m³/day unit constructed and tested with clean water |
| Q2 | Installation at Site 1 (military base) | Commissioned; flow rates confirmed; sensors calibrated |
| Q3 | Operation at Site 1 | >99% PFOA removal from real groundwater (influent: 10–1000 μg/L) |
| Q4 | F⁻ mass balance verification | 95–105% fluoride recovery confirming mineralization |

### Year 5

| Quarter | Milestone | Success Criteria |
|---------|-----------|------------------|
| Q1 | 90-day continuous operation | >99% removal maintained; no matrix degradation |
| Q2 | Multi-contaminant testing | >95% removal of PFOA + PFOS + PFHxS mixture |
| Q3 | Site 2 and Site 3 deployment | Performance validated across different water chemistries |
| Q4 | Phase 3 Gate Review | Independent third-party verification of >99% PFAS destruction |

**Budget:** $15M (pilot construction, site installation, 18-month operation, analytical, regulatory)
**Go/No-Go Gate:** >99% PFAS destruction at pilot scale with real contaminated water, verified by independent third party.

---

## Phase 4: Scale-up & Regulatory Approval (Years 5–7)

**Goal:** Build and operate a 100 m³/day demonstration plant; obtain regulatory approval for contained bioremediation; validate cost target of <$1/m³.

### Year 5

| Quarter | Milestone |
|---------|-----------|
| Q3 | Demonstration plant engineering design (100 m³/day) |
| Q4 | Manufacturing process development for MLF-H and MLF-C units |

### Year 6

| Quarter | Milestone | Success Criteria |
|---------|-----------|------------------|
| Q1 | 100 m³/day demonstration plant commissioned | Flow rates confirmed; all systems operational |
| Q2 | 6-month continuous operation | >99.9% PFAS removal; cost <$1/m³; energy <0.5 kWh/m³ |
| Q3 | Regulatory submission (EPA) | Full engineering report + performance data + biocontainment validation |
| Q4 | Manufacturing scale-up | Pilot production of 100 MLF-H units and 5 MLF-C units |

### Year 7

| Quarter | Milestone | Success Criteria |
|---------|-----------|------------------|
| Q1 | Regulatory approval (anticipated) | EPA approval for contained bioremediation system |
| Q2 | Municipal partnership deployment | 3 municipal plants in PFAS-impacted communities |
| Q3 | Long-term performance validation | 2-year operational data from demonstration plant |
| Q4 | Phase 4 Gate Review | Regulatory approval + <$1/m³ cost validated at 100 m³/day |

**Budget:** $30M (demonstration plant, manufacturing, regulatory, personnel)
**Go/No-Go Gate:** Regulatory approval and <$1/m³ operating cost at demonstration scale.

---

## Phase 5: Deployment (Years 7–10)

**Goal:** Achieve household unit cost <$500; deploy 1,000+ units globally; establish technology licensing program.

### Year 8

| Milestone | Success Criteria |
|-----------|------------------|
| MLF-H household unit launch | Retail price $200–500; 100 units sold |
| MLF-C community unit launch | 10 community installations operational |
| Manufacturing scale-up | 1,000 units/year production capacity |
| International regulatory submissions | EU, Japan, Australia, Canada applications filed |

### Year 9

| Milestone | Success Criteria |
|-----------|------------------|
| MLF-M municipal unit launch | First municipal installation (100,000 m³/day) |
| Global partnerships | Technology licensing agreements with 5+ water technology companies |
| Humanitarian deployment | 100 MLF-C units deployed in developing nations (Bangladesh, India, Sub-Saharan Africa) |
| Cost reduction | MLF-H unit cost <$200; operating cost <$0.30/m³ |

### Year 10

| Milestone | Success Criteria |
|-----------|------------------|
| Ubiquity milestone | 1,000+ units deployed worldwide |
| Performance validation | 10-year operational lifetime verified on original pilot units |
| Cost target achieved | Operating cost <$0.50/m³ at all scales |
| Technology transfer | Open-source biological components (enzymes, QS circuits); commercial licensing for hardware |

**Budget:** $50M (manufacturing, deployment, marketing, humanitarian, licensing)
**Final Gate:** 1,000+ units deployed; <$0.50/m³ operating cost; 10-year lifetime validated.

---

## Key Dependencies & Critical Path

```
Year 1-3: Enzyme Engineering (CRITICAL PATH)
    │
    ├─ Year 2-4: Consortium Development (depends on Phase 1 enzymes)
    │       │
    │       ├─ Year 3-5: Pilot Reactor (depends on Phase 2 consortium)
    │       │       │
    │       │       ├─ Year 5-7: Scale-up & Approval (depends on Phase 3 pilot)
    │       │       │       │
    │       │       │       └─ Year 7-10: Deployment (depends on Phase 4 approval)
    │       │       │
    │       │       └─ Sensor development (PARALLEL)
    │       │
    │       └─ QS circuit development (PARALLEL, can start Year 2)
    │
    └─ Computational enzyme design (PARALLEL, backup for PACE)
```

**Critical path:** Enzyme engineering → Consortium development → Pilot → Scale-up → Deployment

**Long-lead items:**
- Regulatory approval (2–3 years from submission)
- Manufacturing scale-up (18 months from design to production)
- PFAS sensor development (2–3 years for ppt-level aptamer sensors)

---

## Funding Strategy

| Phase | Budget | Primary Funding Sources |
|-------|--------|------------------------|
| Phase 1 | $5–10M | NIH/NIEHS (R01/R21), NSF (CBET), DOE (BER), philanthropic foundations |
| Phase 2 | $5–7M | EPA STAR, SERDP, venture capital (seed round) |
| Phase 3 | $15M | EPA ORD, state PFAS funds, Series A venture capital |
| Phase 4 | $30M | Series B venture capital, strategic partnerships (Xylem, Veolia), EPA Superfund |
| Phase 5 | $50M | Revenue from initial deployments, international development banks (World Bank, ADB), government procurement |

**Total: $43–112M over 10 years**

**Return on Investment:**
- Global PFAS remediation market: $10–20B by 2035
- MLF addresses the full market at <$0.50/m³ vs. $3–10/m³ for alternatives
- At 0.1% market penetration by Year 10: $10–20M annual revenue
- At 1% market penetration by Year 15: $100–200M annual revenue

---

## Team Requirements

| Role | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 |
|------|---------|---------|---------|---------|---------|
| Protein Engineer | 3 | 2 | 1 | 1 | — |
| Mycologist | 1 | 2 | 2 | 1 | — |
| Electrochemical Engineer | 1 | 2 | 2 | 2 | 1 |
| Process Engineer | — | 1 | 3 | 5 | 5 |
| Regulatory Specialist | — | — | 1 | 2 | 2 |
| Sensor Engineer | 1 | 1 | 2 | 2 | 1 |
| Data Scientist | 1 | 1 | 1 | 2 | 3 |
| Manufacturing Engineer | — | — | — | 3 | 5 |
| Field Technician | — | — | 3 | 10 | 20 |
| Project Manager | 1 | 1 | 1 | 2 | 3 |
| **Total** | **8** | **10** | **16** | **30** | **40** |

---

## Intellectual Property Strategy

| Component | IP Strategy | Rationale |
|-----------|------------|-----------|
| ePRD enzyme sequences | Patent (composition of matter) | Core innovation; 20-year protection |
| QS circuit design | Patent (synthetic biology) | Protects the regulatory system |
| Bioelectrochemical system | Patent (system and method) | Protects the voltage enhancement method |
| Mycelial matrix composition | Trade secret | Difficult to reverse-engineer; no disclosure required |
| Manufacturing process | Trade secret | Process know-how |
| PFAS sensor integration | Patent (system integration) | Protects the control system |
| Biocontainment system | Patent (safety system) | Protects the kill switch/auxotrophy design |
| **Open-source components** | CCBY-SA | Academic publications, enzyme sequences after patent filing, educational materials |

**Philosophy:** Patent core innovations to enable commercial deployment and attract investment. Open-source scientific findings, educational materials, and humanitarian deployment specifications. License technology to established water treatment companies for global scale.

---

*Development Roadmap v1.0 — Mycoremediation Living Filter — 2026-06-16*