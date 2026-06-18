# Lithium Brine Bioscavenger — Development Roadmap

**Document version:** 1.0
**Date:** 2026-06-18
**Overall timeline:** 2026 → 2045 (19 years from concept to ubiquity)

---

## Overview

The LBB development roadmap spans five phases — from concept validation to global ubiquity — with clear technical milestones, funding requirements, and go/no-go decision gates at each transition.

```
Phase 1: Concept          Phase 2: Prototype      Phase 3: Pilot
     (2026–2029)              (2029–2032)            (2032–2035)
     TRL 2 → TRL 4           TRL 4 → TRL 6          TRL 6 → TRL 7
     Lab-scale proof          Bench prototype         Field pilot

Phase 4: Scale            Phase 5: Ubiquity
    (2035–2038)              (2038–2045)
    TRL 7 → TRL 8           TRL 9
    Commercial modules      Global deployment
```

---

## Phase 1: Concept Validation (2026–2029)

**Goal:** Prove the three core biological mechanisms work individually and in combination at lab scale.
**TRL:** 2 → 4
**Budget:** $15–25M (ARPA-E, DOE SBIR, venture seed)

### Milestone 1.1 — LiATPase expression in *Rhodobacter* (Q3 2027)
- Clone codon-optimized *liuA* from *Halomonas* sp. TD01 into *R. sphaeroides* 2.4.1
- Confirm membrane localization (Western blot, immunofluorescence)
- Measure Li⁺ uptake in minimal medium (LiCl 100 mg/L, NaCl 3%): target 2–5× over wild-type
- **Go/no-go:** If Li⁺ uptake <2× wild-type → redesign transporter (try *Lentilactobacillus kefiri* LiATPase homolog)

### Milestone 1.2 — Directed evolution for selectivity (Q1 2028)
- Error-prone PCR library (10⁵ variants)
- FACS screening with LIR-FRET biosensor
- 5 rounds of evolution: target Li⁺:Na⁺ selectivity 50:1
- Validate with Li⁺/Na⁺ dual-uptake assay (AAS + Na⁺-SBFI fluorescent dye)
- **Go/no-go:** If selectivity <30:1 after 10 rounds → activate fallback (dual-transporter with MjLiT channel)

### Milestone 1.3 — Carboxysome expression + Li₂CO₃ precipitation (Q3 2028)
- Co-express CsoS1A/B/C + CsoS3 + SLC26 bicarbonate transporter in *Rhodobacter*
- Confirm carboxysome assembly (TEM imaging, size 100–400 nm)
- Confirm intracellular Li₂CO₃ granule formation (SEM-EDS, XRD of isolated granules)
- Measure intracellular Li accumulation: target 5–8% dry cell weight (initial)
- **Go/no-go:** If no granule formation → try alternative microcompartment (Pdu microcompartment from *Salmonella*) or polyphosphate co-precipitation fallback

### Milestone 1.4 — Auto-flocculation circuit (Q1 2029)
- Clone c-di-GMP flocculation circuit (DGC + EPS activator)
- Confirm Li₂CO₃-granule-triggered floc formation (settling test, floc size measurement)
- Achieve >6% solids settling in 90 min
- **Go/no-go:** If settling <4% solids → optimize EPS expression level or add chemical flocculant backup

### Milestone 1.5 — Integrated strain + lab-scale batch (Q3 2029)
- Combine all modifications into single strain (LBB-1 genotype)
- Run 1 L lab PBR batch on synthetic brine (100 mg/L Li, 5% NaCl)
- Target: 90% Li recovery, 8% Li DCW, floc settling to 6% solids
- Calcine lab batch (250°C muffle furnace), wash, re-carbonate → measure Li₂CO₃ purity
- **Go/no-go gate (TRL 4):** If integrated strain achieves >70% recovery, >5% Li DCW, and >95% Li₂CO₃ purity → proceed to Phase 2

### Phase 1 Deliverables
- Engineered LBB-1 strain with verified genotype (chromosomal integration, stable)
- Lab-scale 1 L batch data (recovery, selectivity, purity, kinetics)
- 3 peer-reviewed publications (LiATPase, carboxysome precipitation, integrated system)
- 2 patents filed (LiATPase directed evolution method; bioselective Li extraction platform)

### Phase 1 Funding
- ARPA-E OPEN (DOE): $8M
- NSF SBIR Phase II: $1.5M
- Venture seed (breakthrough energy, lowercarbonbp): $5–15M
- National lab partnerships (NREL, LBNL): in-kind ($2M)

---

## Phase 2: Prototype (2029–2032)

**Goal:** Build and operate a bench-scale prototype module (1/10 scale, 2 m³ PBR) on real brine.
**TRL:** 4 → 6
**Budget:** $40–60M (Series A + DOE demonstrations)

### Milestone 2.1 — 2 m³ bench PBR design & fabrication (Q2 2030)
- Design and build bench-scale PBR (2 m³, 1/10 module scale)
- Integrate NIR LED lighting, diaphragm pumps, sensor suite, control system
- Validate sterility, anaerobic operation, temperature/pH control

### Milestone 2.2 — Real brine testing — synthetic + geothermal (Q4 2030)
- Test on synthetic brine (100 mg/L Li, 30 g/L TDS) → confirm Phase 1 results at 2 m³ scale
- Obtain geothermal brine from Salton Sea (via CalEnergy partnership) → test on real brine
- Address brine-specific challenges: silica, B, As, temperature, competing ions
- Target: 80%+ recovery on real geothermal brine, 6%+ Li DCW

### Milestone 2.3 — Calciner + wash + re-carbonation integration (Q2 2031)
- Integrate bench-scale solar-thermal calciner (CPC + retort, 5 L batch)
- Integrate wash station + re-carbonation vessel
- Produce first battery-grade Li₂CO₃ from real brine: target >99.0% purity
- Full mass balance and energy audit

### Milestone 2.4 — Produced water testing (Q4 2031)
- Obtain produced water from Permian Basin (via operator partnership)
- Test LBB-1 strain on produced water (100 mg/L Li, 80 g/L TDS, B/Ba/Sr/Ra)
- Address produced-water-specific challenges: radionuclides, organic contaminants, scale
- Target: 75%+ recovery, product meets battery spec (including radiological screening)

### Milestone 2.5 — 100-batch continuous operation (Q2 2032)
- Run 100 consecutive batches (6 months continuous operation) on geothermal or produced water brine
- Metrics: average recovery, yield stability, culture stability (qPCR genotype verification monthly), contamination events, mechanical uptime
- Target: >80% average recovery, <5% performance degradation over 100 batches, zero culture loss
- **Go/no-go gate (TRL 6):** If 100-batch run achieves >75% average recovery, >99% product purity, stable culture, >90% mechanical uptime → proceed to Phase 3

### Phase 2 Deliverables
- Bench-scale prototype (2 m³ PBR + calciner + wash + re-carbonation)
- 100-batch continuous operation data on real brine
- First battery-grade Li₂CO₃ from biological extraction (>99% purity)
- Strain improvement: LBB-2 (thermostable, higher selectivity, higher accumulation)
- 5 peer-reviewed publications, 3 additional patents
- Regulatory engagement: EPA TSCA pre-manufacture notification for GMO use, state permits

### Phase 2 Funding
- Series A (venture capital): $25–35M
- DOE Demonstration funding (DE-FOA): $10–15M
- Industry partnerships (CalEnergy, oil/gas operator): in-kind brine access, $5–10M

---

## Phase 3: Pilot (2032–2035)

**Goal:** Deploy and operate a full-scale module (20 m³, shipping container) at a real brine site for 12+ months.
**TRL:** 6 → 7
**Budget:** $80–120M (Series B + DOE large-scale demonstration)

### Milestone 3.1 — Full-scale module fabrication (Q4 2032)
- Fabricate first production-representative 20-ft container module
- Factory acceptance test: 24-hour pressure test, sensor calibration, firmware validation
- Ship to deployment site (Salton Sea geothermal plant or Permian Basin well pad)

### Milestone 3.2 — Site installation & commissioning (Q1 2033)
- Install module at geothermal plant (Salton Sea) or oil/gas well pad (Permian)
- Connect brine supply, power (solar PV), communication (LoRaWAN)
- Commissioning: 2-week acclimatization, first batch on real brine
- Regional biofoundry established (La Paz, Bolivia OR El Paso, Texas) for inoculum supply

### Milestone 3.3 — 12-month pilot operation (Q1 2033 → Q1 2034)
- Continuous operation for 12 months, ~50 batches
- Metrics: weekly Li₂CO₃ output, recovery %, purity, culture stability, energy consumption, water consumption, uptime
- Target: 5–20 kg Li₂CO₃/week (depending on brine Li), >90% recovery, >99.5% purity, >90% uptime
- Environmental monitoring: GMO containment verification (soil sampling, brine discharge testing — zero detect)

### Milestone 3.4 — 10-module cluster demonstration (Q3 2034)
- Deploy 10 modules at pilot site
- Validate cluster operation: shared labor, inoculum supply chain, telemetry dashboard
- Target: 50–200 kg Li₂CO₃/week, operational cost data for economic validation
- First commercial product sale (battery-grade Li₂CO₃ to cathode manufacturer or battery recycler)

### Milestone 3.5 — Regulatory & safety certification (Q2 2035)
- EPA TSCA registration for engineered *Rhodobacter* use (containment verification)
- State mining/extraction permits (California, Texas, or Bolivia)
- Battery-grade product certification (independent lab: SGS, Intertek)
- Environmental impact assessment: water, land, CO₂, biodiversity
- **Go/no-go gate (TRL 7):** If pilot achieves target economics ($3–6/kg OpEx), regulatory approval, and commercial product sale → proceed to Phase 4

### Phase 3 Deliverables
- First full-scale production module, operational 12+ months
- 10-module cluster, operational 6+ months
- First commercial Li₂CO₃ sale (battery-grade, certified)
- Regulatory approvals (EPA, state, product certification)
- Techno-economic analysis validated against pilot data
- Strain LBB-3 (field-optimized, real-brine-adapted)

### Phase 3 Funding
- Series B (venture capital + strategic investors): $50–70M
- DOE Large-Scale Demonstration: $20–30M
- Industry partnerships (cathode manufacturer offtake, oil/gas operator): $10–20M

---

## Phase 4: Scale (2035–2038)

**Goal:** Manufacture 1,000 modules, deploy at 3–5 sites, achieve commercial break-even.
**TRL:** 7 → 8
**Budget:** $200–400M (Series C / pre-IPO + project finance)

### Milestone 4.1 — Manufacturing line (Q4 2035)
- Build first automated module manufacturing line (50–100 modules/year capacity)
- Target: $46K/module cost at 1,000-unit/year production scale
- Supply chain contracts: HDPE roto-molding, ETFE film, 304SS fabrication, electronics

### Milestone 4.2 — 1,000-module deployment (Q2 2036 → Q4 2037)
- Deploy modules across 3–5 sites:
  - 600 modules at Salton Sea (geothermal)
  - 300 modules at Permian Basin (produced water)
  - 100 modules at Uyuni, Bolivia (community salar)
- Target: 500–750 t Li₂CO₃/year total output
- First community-owned cooperative operational (Uyuni)

### Milestone 4.3 — Commercial break-even (Q2 2037)
- Revenue from Li₂CO₃ sales exceeds total operating cost (OpEx + amortized CapEx)
- Target: $20/kg Li₂CO₃ selling price, $4–6/kg OpEx at scale → 70–80% gross margin
- First profitable quarter

### Milestone 4.4 — Biofoundry network (Q4 2037)
- Establish 3 regional biofoundries (Americas, Europe, Asia-Pacific) for inoculum supply
- Each biofoundry: lyophilized working cell bank production, 100K vials/year capacity
- Cold-chain logistics validated (4°C, 6-month shelf life)

### Milestone 4.5 — IPO or major strategic investment (Q2 2038)
- IPO at $1–2B valuation (based on 1,000-module deployment + 10,000-module pipeline)
- OR strategic investment from major mining/battery company ($200–500M)
- **Go/no-go gate (TRL 8):** If commercial break-even achieved, 1,000 modules operational, biofoundry network established → proceed to Phase 5

### Phase 4 Deliverables
- 1,000 modules operational at 3–5 sites
- 500–750 t Li₂CO₃/year commercial output
- Automated manufacturing line (100 modules/year)
- Regional biofoundry network (3 facilities)
- Commercial break-even / profitability
- IPO or strategic investment

### Phase 4 Funding
- Series C / pre-IPO: $100–200M
- Project finance (deployment capital): $100–200M
- Strategic investors (battery manufacturers, mining companies): $50–100M

---

## Phase 5: Ubiquity (2038–2045)

**Goal:** Deploy 1,000,000 modules globally, producing 500K–1M t Li₂CO₃/year — 25–50% of world lithium demand.
**TRL:** 8 → 9
**Budget:** $20–50B (public markets, project finance, sovereign funds, development banks)

### Milestone 5.1 — Mass manufacturing (2039)
- Build 10+ automated manufacturing lines globally (10,000 modules/year each = 100K/year total)
- Target: $18–25K/module cost at 100K-unit/year production (commodity pricing)
- Manufacturing in 5 countries (US, Mexico, Bolivia, Germany, Kenya) for regional supply

### Milestone 5.2 — 100,000-module deployment (2040)
- Deploy 100K modules across 20+ countries
- Target: 50,000–100,000 t Li₂CO₃/year
- Add salar runoff, low-grade brines (10–50 mg/L Li)
- Seawater FO-LBB pilot: 100-module coastal pilot with forward-osmosis pre-concentration

### Milestone 5.3 — Seawater viability (2042)
- Validate FO-LBB coupling: seawater → FO pre-concentrate (50 mg/L Li) → LBB → Li₂CO₃
- First 1,000-module coastal array operational
- Target: 200 t Li₂CO₃/year from seawater (the ultimate resource)
- This unlocks unlimited scalability — every coastline becomes a lithium resource

### Milestone 5.4 — 1,000,000-module global network (2045)
- Deploy 1M modules across 30+ countries
- Target: 500,000–1,000,000 t Li₂CO₃/year (25–50% of 2050 global demand)
- 500 billion liters water/year saved (vs. evaporation ponds)
- 6–10 Mt CO₂/year avoided
- 500K–1M jobs created globally
- Distributed production breaks geopolitical concentration

### Milestone 5.5 — Multi-mineral LBB (2043–2045)
- Deploy multi-mineral strains (Li + Sr + REEs from same brine)
- First LBB modules producing solid-state electrolyte precursors (LLZO) directly
- Technology licensed to 10+ companies globally (open patent platform for climate impact)

### Phase 5 Deliverables
- 1,000,000 modules deployed globally
- 500K–1M t Li₂CO₃/year from stranded resources
- Seawater lithium extraction validated and commercial
- Multi-mineral extraction capability
- 500K–1M jobs, 30+ producing countries
- Lithium supply chain democratized

---

## Timeline Summary

| Year | Phase | TRL | Modules | Output (t/yr) | Key milestone |
|---|---|---|---|---|---|
| 2026 | 1 | 2 | 0 | 0 | Project start |
| 2029 | 1 | 4 | 0 | 0 | Lab-scale proof of concept |
| 2032 | 2 | 6 | 0 (bench) | 0 | 100-batch continuous operation |
| 2033 | 3 | 7 | 1 | 0.5 | First full-scale module operational |
| 2035 | 3 | 7 | 10 | 5–20 | 10-module cluster, commercial sale |
| 2037 | 4 | 8 | 1,000 | 500–750 | Commercial break-even |
| 2040 | 5 | 8 | 100,000 | 50K–100K | Mass manufacturing, 20+ countries |
| 2042 | 5 | 9 | 100,000+ | 100K+ | Seawater FO-LBB pilot |
| 2045 | 5 | 9 | 1,000,000 | 500K–1M | Global ubiquity |

---

## Funding Summary

| Phase | Timeline | Budget | Sources |
|---|---|---|---|
| 1 — Concept | 2026–2029 | $15–25M | ARPA-E, NSF SBIR, venture seed |
| 2 — Prototype | 2029–2032 | $40–60M | Series A, DOE demonstrations |
| 3 — Pilot | 2032–2035 | $80–120M | Series B, DOE large-scale demo |
| 4 — Scale | 2035–2038 | $200–400M | Series C / pre-IPO, project finance |
| 5 — Ubiquity | 2038–2045 | $20–50B | Public markets, sovereign funds, development banks |
| **Total** | | **$21–51B** | |

*Phase 5 funding is deployment capital (module manufacturing + installation), not R&D. At $20K/module (mass production cost) × 1M modules = $20B deployment capital, financed by project finance and sovereign investment against Li₂CO₃ revenue ($10–20B/year at 500K–1M t × $20/kg).*

---

## Key Risks & Decision Gates

| Gate | Year | Criterion | If FAIL |
|---|---|---|---|
| 1.1 → 1.2 | 2027 | LiATPase expressed, Li uptake >2× WT | Try alternative transporter |
| 1.3 → 1.4 | 2028 | Carboxysome + Li₂CO₃ granules confirmed | Alternative microcompartment or polyphosphate fallback |
| 1.5 → 2.1 | 2029 | Integrated strain: >70% recovery, >5% Li DCW | Redesign strain, extend Phase 1 by 1 year |
| 2.5 → 3.1 | 2032 | 100-batch: >75% recovery, >99% purity, stable | Optimize strain/brine, extend Phase 2 by 1 year |
| 3.5 → 4.1 | 2035 | Pilot: target economics, regulatory approval, commercial sale | Reassess market, seek additional funding |
| 4.5 → 5.1 | 2038 | Commercial break-even, 1,000 modules, biofoundry network | Scale slower, seek strategic partner |
| 5.3 → 5.4 | 2042 | Seawater FO-LBB viability | Continue brine-only deployment (still 500K+ t/yr from brines) |

---

*This roadmap is a planning document based on current technology readiness. Timelines may shift based on experimental results, regulatory timelines, market conditions, and funding availability. The 19-year timeline from concept to ubiquity is aggressive but consistent with historical biotechnology deployment timelines (e.g., insulin production: 1973 discovery → 1982 commercial; PCR: 1983 → 1993 ubiquitous).*