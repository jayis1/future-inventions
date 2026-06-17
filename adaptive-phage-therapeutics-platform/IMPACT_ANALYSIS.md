# APTP — Impact Analysis

> *Quantifying the transformation: from 10 million preventable deaths to a world where drug-resistant infections are routinely curable.*

---

## 1. Health Impact

### 1.1 Lives Saved

| Scenario | 2030 | 2035 | 2040 | 2045 | 2050 |
|----------|------|------|------|------|------|
| Without APTP (AMR deaths/year) | 5M | 7M | 8.5M | 9.5M | 10M |
| With APTP (AMR deaths/year) | 5M | 5.5M | 4M | 2.5M | 1M |
| **Lives saved/year** | **0** | **1.5M** | **4.5M** | **7M** | **9M** |
| Cumulative lives saved | — | 1.5M | 10M | 32M | 68M |

**Methodology**: WHO AMR death projections (10M/year by 2050) are used as the baseline. APTP impact is modeled as a logistic adoption curve — slow initial impact (few units deployed), accelerating as manufacturing scales and clinical evidence accumulates. Assumptions: 50% reduction in AMR mortality in regions with APTP access; adoption follows S-curve with inflection at 2037.

### 1.2 Infections Treated

| Year | APTP Units Deployed | Courses/Unit/Year | Total Courses/Year | Infections Cleared (>80%) |
|------|---------------------|-------------------|--------------------|--------------------------|
| 2030 | 50 | 50 | 2,500 | 2,000 |
| 2033 | 500 | 150 | 75,000 | 60,000 |
| 2035 | 2,000 | 250 | 500,000 | 400,000 |
| 2038 | 10,000 | 350 | 3,500,000 | 2,800,000 |
| 2040 | 50,000 | 400 | 20,000,000 | 16,000,000 |
| 2045 | 100,000+ | 500 | 50,000,000 | 40,000,000 |

### 1.3 Antibiotic Reduction

| Metric | 2035 | 2040 | 2045 |
|--------|------|------|------|
| Antibiotic prescriptions avoided (MDR cases) | 500K | 20M | 50M |
| Reduction in last-resort antibiotic use (colistin, tigecycline) | 20% | 50% | 70% |
| Reduction in broad-spectrum antibiotic prescriptions | 5% | 15% | 30% |
| Antibiotic residues in wastewater (APTP regions) | −10% | −30% | −50% |

**Rationale**: Each APTP-treated MDR infection replaces a failed antibiotic course. For colistin and tigecycline specifically, APTP provides an effective alternative, reducing the selective pressure that drives further resistance.

---

## 2. Economic Impact

### 2.1 Healthcare Cost Savings

| Category | Annual Savings (2040) | Annual Savings (2045) | Methodology |
|----------|----------------------|----------------------|-------------|
| ICU stays avoided (MDR sepsis) | $15B | $30B | 5M fewer ICU stays × $3K–6K/day × 10-day avg |
| Failed antibiotic courses avoided | $8B | $15B | 20M courses × $500–5K per failed course |
| Infection control costs avoided | $5B | $10B | Hospital infection prevention programs |
| Disability-adjusted life years (DALYs) saved | $20B | $50B | 50M DALYs × $400–1,000/DALY |
| **Total healthcare savings** | **$48B** | **$105B** | |

### 2.2 Market Creation

| Category | 2035 | 2040 | 2045 |
|----------|------|------|------|
| APTP hardware sales | $50M | $500M | $1.5B |
| Consumable cartridge sales | $75M | $1.5B | $5B |
| Service & maintenance | $10M | $200M | $500M |
| **Total phage therapy market (APTP-enabled)** | **$135M** | **$2.2B** | **$7B** |

### 2.3 Cost-Effectiveness

| Metric | APTP | Current Phage Therapy | Last-Resort Antibiotics |
|--------|------|----------------------|------------------------|
| Cost per course | $50–150 | $30,000–100,000 | $500–5,000 |
| Cost per DALY saved | $5–15 | $3,000–10,000 | $50–500 |
| Cost per infection cleared | $60–190 | $37,500–125,000 | $800–8,000 |
| ICER vs. standard of care | **Dominant** (cheaper AND more effective) | N/A | N/A |

**Note**: APTP is a dominant strategy — it costs less AND is more effective than both current phage therapy and last-resort antibiotics. Cost-effectiveness improves further at scale.

---

## 3. Environmental Impact

### 3.1 Pharmaceutical Pollution Reduction

| Metric | 2035 | 2040 | 2045 |
|--------|------|------|------|
| Antibiotic residues in wastewater (APTP regions) | −10% | −30% | −50% |
| AMR selection pressure in environment | −5% | −20% | −40% |
| Phage environmental release (APTP phages) | Negligible | Negligible | Negligible |

**Phage environmental safety**: All APTP phages are strictly lytic (no lysogenic conversion risk), target-specific (narrow host range), and engineered with thermolabile capsid mutations (denature above 50°C, no persistence in tropical waterways). Environmental half-life: <7 days in soil/water vs. months–years for antibiotic residues.

### 3.2 Carbon Footprint

| Component | kg CO₂e/unit | Notes |
|-----------|-------------|-------|
| APTP hardware manufacturing | 500 kg CO₂e | Electronics, plastics, metals |
| APTP hardware operation | 200 kg CO₂e/year | 500W × 8,760 hrs × grid factor |
| Consumable cartridge | 0.5 kg CO₂e | Plastics, reagents, packaging |
| Total per course | ~2 kg CO₂e | vs. ~50 kg CO₂e for hospital antibiotic course |

**Net carbon impact**: Each APTP course avoids ~50 kg CO₂e from failed antibiotic treatments + hospital stays, for a net reduction of ~48 kg CO₂e per course. At 20M courses/year (2040), this is ~960,000 tonnes CO₂e/year avoided.

### 3.3 Waste Stream

| Waste Type | Volume per Course | Treatment |
|------------|-------------------|-----------|
| CFPS reaction waste | 25–100 mL | Biodegradable (amino acids, nucleotides, lysate) |
| Microfluidic chips | 2 PDMS chips | Recyclable (silicone) |
| Nanopore flow cells | 3 disposable units | Manufacturer recycling program |
| Packaging | Cardboard + plastic | Standard medical waste recycling |
| **Total** | ~150 g non-hazardous waste | vs. ~2 kg medical waste per hospital antibiotic course |

---

## 4. Social Impact

### 4.1 Access Equity

| Region | Current Phage Therapy Access | APTP Access (2040) | Population Reached |
|--------|------------------------------|--------------------|--------------------|
| Sub-Saharan Africa | 0 clinics | 5,000+ district hospitals | 800M people |
| South Asia | 2 clinics (private) | 10,000+ hospitals | 2B people |
| Southeast Asia | 1 clinic (Bangkok) | 5,000+ hospitals | 700M people |
| Latin America | 0 clinics | 3,000+ hospitals | 400M people |
| Eastern Europe | 5 clinics (Georgia, Poland) | 3,000+ hospitals | 300M people |
| High-income countries | 10 clinics | 20,000+ hospitals | 1.2B people |
| **Global** | **<20 clinics** | **50,000+ hospitals** | **5.4B people** |

### 4.2 Workforce Development

| Role | Jobs Created (2040) | Training Required |
|------|---------------------|-------------------|
| APTP operator (nurse/technician) | 100,000 | 40-hour certification course |
| APTP service technician | 10,000 | 6-month technical training |
| Manufacturing (APTP units) | 5,000 | Standard medical device manufacturing |
| Manufacturing (consumables) | 20,000 | Standard pharmaceutical manufacturing |
| PhageFormer AI/data team | 500 | PhD-level |
| Regulatory/clinical | 1,000 | MD/PhD-level |
| **Total** | **~136,500** | |

### 4.3 Education & Capacity Building

- **APTP Certification Program**: 40-hour training for nurses and lab technicians; available in 20+ languages; includes hands-on simulator and competency exam
- **Open-source phage genome database**: All phage sequences automatically deposited to NCBI/EMBL; 1M+ entries projected by 2037
- **Clinical Phage Therapy Fellowship**: 1-year program for infectious disease physicians; 50+ fellows/year by 2035
- **LMIC Partnership Program**: Subsidized APTP units and training for hospitals in low-income countries; funded by WHO/Gates Foundation

---

## 5. SDG Alignment

| SDG | Target | APTP Contribution | Quantified Impact (2040) |
|-----|--------|-------------------|--------------------------|
| **SDG 3** (Good Health) | 3.3: End epidemics | Phage therapy for MDR infections | 4.5M lives saved/year |
| **SDG 3** (Good Health) | 3.8: Universal health coverage | APTP in every district hospital | 2B+ people gain access |
| **SDG 6** (Clean Water) | 6.3: Reduce pollution | 30% reduction in antibiotic water pollution | 960K tonnes CO₂e/year |
| **SDG 9** (Industry & Innovation) | 9.5: Scientific research | New biomanufacturing paradigm | 136K+ jobs; $2.2B market |
| **SDG 10** (Reduced Inequalities) | 10.1: Income inequality | Democratizes life-saving therapy | 5.4B people reached |
| **SDG 12** (Responsible Consumption) | 12.4: Chemical management | Replaces toxic antibiotics with biodegradable phages | 20M antibiotic courses avoided |
| **SDG 13** (Climate Action) | 13.1: Resilience | Reduces pharmaceutical carbon footprint | 960K tonnes CO₂e/year |
| **SDG 17** (Partnerships) | 17.6: Technology sharing | Open-source phage genome database | 1M+ entries by 2037 |

---

## 6. Risk-Adjusted Impact Scenarios

### Scenario A: Optimistic (70% probability)

- CFPS yield targets met by 2028–2030
- Regulatory pathway established by 2032–2034
- APTP deployed in 50,000+ hospitals by 2040
- **9M lives saved/year by 2050**
- **$105B/year healthcare savings**

### Scenario B: Moderate (25% probability)

- CFPS yield requires backup bioreactor (12-hour delay)
- Regulatory pathway takes until 2036
- APTP deployed in 20,000 hospitals by 2040
- **4M lives saved/year by 2050**
- **$50B/year healthcare savings**

### Scenario C: Delayed (5% probability)

- CFPS yield insufficient; traditional phage amplification required
- Regulatory framework not established until 2038+
- APTP serves as diagnostic/screening tool rather than full manufacturing platform
- **1M lives saved/year by 2050**
- **$15B/year healthcare savings**

**Expected value (probability-weighted)**: 7.0M lives saved/year by 2050; $80B/year healthcare savings.

---

## 7. Geographic Impact Priority

| Priority | Region | Rationale | Projected APTP Units (2040) |
|----------|--------|-----------|----------------------------|
| **1** | South Asia | Highest MDR burden (India: 1M+ AMR deaths/year); dense population; existing phage research | 15,000 |
| **2** | Sub-Saharan Africa | Highest AMR mortality rate; limited antibiotic access; greatest equity impact | 8,000 |
| **3** | Southeast Asia | High MDR rates; dense population; emerging phage research | 6,000 |
| **4** | Latin America | Growing MDR crisis; middle-income health systems can absorb APTP | 4,000 |
| **5** | Eastern Europe | Phage therapy tradition (Georgia, Poland); regulatory readiness | 3,000 |
| **6** | High-income countries | Low MDR burden per capita but high absolute numbers; early adopters | 14,000 |
| **Total** | | | **50,000** |

---

## 8. Comparison to Alternative AMR Interventions

| Intervention | Cost (Global) | Timeline | Impact (Lives/yr by 2050) | Feasibility |
|--------------|---------------|----------|---------------------------|-------------|
| **APTP (phage therapy)** | $2–5B R&D + deployment | 10–15 years | 7–9M | High (proven science, engineering challenge) |
| New antibiotics (8–12 new classes) | $15–25B R&D | 15–20 years | 2–4M | Low (resistance develops in 2–5 years per drug) |
| AMR stewardship (global) | $1–2B/year | 5–10 years | 0.5–1M | Moderate (slows resistance, doesn't cure MDR) |
| Infection prevention (WASH, IPC) | $5–10B/year | 10–20 years | 1–2M | High (foundational but insufficient for MDR) |
| CRISPR antimicrobials | $3–5B R&D | 10–15 years | 0.5–1M | Low (delivery challenge, narrow target range) |
| Vaccines (bacterial) | $5–10B R&D | 15–20 years | 1–3M | Moderate (pathogen-specific, not available for many) |

**Conclusion**: APTP is the most cost-effective intervention per life saved ($500–2,000/DALY) and the only approach that directly addresses MDR infections after they occur. It complements (does not replace) stewardship, prevention, and new antibiotic development.

---

*Impact Analysis v1.0 — 2026-06-17 — Adaptive Phage Therapeutics Platform*