# SPECIFICATION — Magnetotactic Microplastic Scavenger

## Technical Specification Document

**Document Version:** 1.0  
**Date:** 2026-06-27  
**Invention:** Magnetotactic Microplastic Scavenger (MMS)  
**Category:** Clean Water & Environmental Restoration / Circular Economy

---

## 1. System Overview

The MMS is a four-stage biological-magnetic water treatment system for microplastic removal:

```
Influent Water
    │
    ▼
┌─────────────────────────────────┐
│  STAGE 1: Contact Reactor       │  Fluidized-bed biofilm carrier
│  Engineered M. magneticum       │  HRT: 2–5 min
│  (hydrophobin + magnetosome+)    │  Velocity: 5–10 m/h (upflow)
│  → bacteria bind microplastics   │  Carrier: recycled glass beads
└──────────────┬──────────────────┘
               │ bacteria-plastic complexes in suspension
               ▼
┌─────────────────────────────────┐
│  STAGE 2: Halbach Magnetic Column│  NdFeB N52 permanent magnets
│  Permanent magnet gradient       │  Field: 1.5 T, ∇B: 50–200 T/m
│  → captures magnetic complexes  │  Capture velocity: 2–3 m/h
│  → clean water exits             │  Efficiency: >98% capture
└──────────────┬──────────────────┘
               │
       ┌───────┴───────┐
       ▼               ▼
  Clean Water      Concentrate
  (effluent)       (bacteria + plastic)
                        │
                        ▼
┌─────────────────────────────────┐
│  STAGE 3: Separation & Recycle  │  Low-gradient magnet (0.1 T)
│  → recover 70–80% bacteria       │  → return to contact reactor
│  → plastic concentrate (1000×)  │  → dewater → Solar-Polymer Upcycler
└──────────────┬──────────────────┘
               │
               ▼
┌─────────────────────────────────┐
│  STAGE 4: Regrowth Reactor      │  10–50 L aerated chemostat
│  Minimal acetate/iron medium     │  10¹⁰–10¹¹ cells/day
│  → replenishes bacterial bleed   │  DAP-dependent (auxotrophy)
└─────────────────────────────────┘
```

---

## 2. Biological Subsystem

### 2.1 Host Organism

**Species:** *Magnetospirillum magneticum* strain AMB-1 (ATCC 700264)  
**Type:** Gram-negative, microaerophilic, magnetotactic  
**Natural habitat:** freshwater sediments, low-O₂ mud  
**Optimal growth:** 25–30°C, pH 6.5–7.5, dissolved O₂ 1–3% (microaerophilic)  
**Generation time:** 5–8 hours (standard), 3–5 hours (optimized strain)  
**Cell size:** 0.5 × 1–3 µm (spirillum morphology)  
**Genome:** 4.7 Mb chromosome + 117 kb magnetosome island (MAI)

### 2.2 Magnetosome Biology

**Magnetosome:** Intracellular membrane-bounded Fe₃O₄ (magnetite) nanocrystals, arranged in a linear chain along the long cell axis.  
**Wild-type AMB-1:** 6–20 magnetosomes per cell, 30–120 nm diameter, total iron 1–2 fg/cell.  
**Engineered strain (MMS-1):** 12–30 magnetosomes per cell, 40–140 nm diameter, total iron 3–6 fg/cell.  
**Magnetic moment (wild-type):** ~1 × 10⁻¹⁵ A·m²  
**Magnetic moment (MMS-1):** ~3–5 × 10⁻¹⁵ A·m² (3–5× enhancement)

**Enhancement engineering:**
- *mamAB* operon (15 genes, core magnetosome formation): cloned under strong *tac* promoter on a low-copy plasmid (pBBR1MCS-2, 5 copies/cell). Increases magnetosome number 1.5–2×.
- *mamGFDC* operon (crystal size control): overexpressed from same plasmid. Increases crystal diameter 20–40%.
- *feoAB* operon (Fe²⁺ uptake): chromosomal integration under constitutive *mamA* promoter. Increases intracellular iron uptake 2–3×.
- *mms6* (magnetite nucleation): codon-optimized, integrated in MAI. Improves crystallinity and magnetic quality.

### 2.3 Hydrophobin Surface Display

**Display system:** Ice nucleation protein (InaZ) from *Pseudomonas syringae* as outer membrane anchor.

**Construct design:**
```
Promoter: tac (IPTG-inducible, tunable)
Signal peptide: InaZ N-terminal (Sec pathway)
Anchor: InaZ C-terminal repeats (3× 21-aa repeat → outer membrane insertion)
Fusion: InaZ N-term — Linker (GGGGS)₃ — Hydrophobin SC3 — InaZ C-term
Terminator: rrnB T1T2
Plasmid: pBBR1MCS-3 (compatible with magnetosome plasmid, 8 copies/cell)
```

**Hydrophobin choice: SC3 from *Schizophyllum commune***

- 100 aa mature protein, 8 cysteine residues (4 disulfide bridges), amphipathic
- Self-assembles at hydrophobic-hydrophilic interfaces into ~10 nm films
- Binds to polyethylene, polypropylene, polystyrene, PET, PVC, nylon with K_D ≈ 10⁻⁸–10⁻⁹ M
- Stable to pH 2–10, 4–60°C, resistant to proteolysis when assembled
- Well-characterized; recombinant production in E. coli and Pichia demonstrated
- Alternative: HFBI from *Trichoderma reesei* (75 aa, similar properties, smaller, easier to express)

**Surface density:** ~10⁴–10⁵ hydrophobin molecules per cell (limited by InaZ display capacity). This is sufficient for effective binding because hydrophobins self-assemble into patches.

### 2.4 Biocontainment

**Layer 1: Synthetic auxotrophy (dapA deletion)**
- *dapA* gene (dihydrodipicolinate synthase, DAP pathway → lysine + DAP) deleted from chromosome
- DAP is required for peptidoglycan cross-linking; without it, cell wall fails → lysis
- DAP supplied in regrowth reactor medium (0.3 mg/mL meso-DAP) only
- In the environment (no DAP): cell division fails after 2–4 generations; lysis within 24–48 h

**Layer 2: Kill switch (frmR-mazF)**
- *frmR* promoter (formaldehyde-inducible) drives *mazF* (mRNA interferase toxin)
- Threshold: 50 µM formaldehyde (environmental background is <1 µM in clean water; industrial effluent might trigger)
- Optional: chemical inducer (cumate, anhydrotetracycline) for manual activation
- Activation → MazF cleaves cellular mRNA → growth arrest + death within 4–8 h

**Layer 3: Fitness cost**
- Overexpression of *mamAB* + hydrophobin imposes 15–25% growth penalty vs. wild-type
- In competition with environmental bacteria (no DAP, no selective pressure), MMS-1 is outcompeted within 3–7 days
- Magnetosome synthesis consumes 20–30% of cellular iron budget — severe disadvantage in iron-poor natural waters

---

## 3. Contact Reactor

### 3.1 Design

- **Type:** Upflow fluidized-bed biofilm reactor
- **Volume:** 2–5 m³ (for 100–500 m³/day WWTP module); 0.5–2 L (household cartridge)
- **Carrier media:** Recycled glass beads (soda-lime glass), 2–5 mm diameter, 300 m²/m³ specific surface area, sintered for porosity (roughness factor 3–5×)
- **Bed expansion:** 30–50% at design flow (5–10 m/h upflow velocity)
- **Bacterial loading:** 10⁹–10¹⁰ cells per m² carrier surface (biofilm + planktonic)
- **Hydraulic residence time:** 2–5 minutes (sufficient for >90% binding collision probability)
- **Temperature:** 15–35°C ambient (no heating required for most climates; 5–15°C reduced efficiency 30–50%)
- **Oxygen:** microaerophilic (1–3% DO). In WWTP secondary effluent, DO is already 2–6 mg/L. In anaerobic zones, a low-rate air sparge (0.01–0.05 vvm) maintains microaerophilic conditions.

### 3.2 Binding Kinetics

**Collision rate (Smoluchowski):**
k_coll = 4π(D_b + D_p)(r_b + r_p) × N_b × N_p

Where:
- D_b, D_p = diffusion coefficients of bacterium and particle
- r_b, r_p = radii (bacterium ~0.5 µm; particle 0.5–2500 µm)
- N_b, N_p = number densities

For typical WWTP effluent (10⁶–10⁷ bacteria/cm³, 10²–10⁵ particles/cm³):
- Collision half-time: 30–120 seconds
- Binding probability on collision: 0.3–0.8 (hydrophobin-plastic contact)
- Net binding efficiency in 3 min HRT: 85–95% for >5 µm, 65–85% for 1–5 µm

### 3.3 Biofilm Management

- Fluidization prevents excessive biofilm accumulation (shear controls thickness to 50–200 µm)
- Periodic (weekly) brief aeration increase (10 min at 2× flow) sloughs excess biomass
- Biomass is captured in the Halbach column and recycled or bled

---

## 4. Magnetic Separation Column

### 4.1 Halbach Array Design

**Magnet grade:** NdFeB N52 (B_r = 1.48 T, H_c = 836 kA/m)  
**Array:** 8-segment Halbach cylinder, 10–20 cm internal diameter, 30–60 cm length  
**Field achieved:** 1.2–1.5 T on axis (interior), 0.05–0.1 T exterior (field confined)  
**Gradient:** 50–200 T/m across flow channel (radial, toward inner wall)  
**Flow:** Axial (along column length); magnetic force radial (toward wall)

### 4.2 Capture Physics

**Magnetic force on a bacterium-plastic complex:**
F_mag = (m_complex) × (∇B)

Where m_complex = n_bacteria × m_cell (for n bacteria on one particle)

**Hydrodynamic drag on a complex (Stokes):**
F_drag = 6π η r_complex v_flow

**Capture condition:** F_mag > F_drag + gravitational settling (negligible for small particles)

**Operating parameters for >98% capture:**
| Particle size | Bacteria per particle | m_complex (A·m²) | F_mag (N) | F_drag at 2 m/h (N) | Capture? |
|--------------|---------------------|-------------------|-----------|---------------------|----------|
| 1 µm | 1 | 5×10⁻¹⁵ | 5×10⁻¹³ | 2×10⁻¹³ | ✓ |
| 5 µm | 1 | 5×10⁻¹⁵ | 5×10⁻¹³ | 1×10⁻¹² | Marginal (need lower flow or more bacteria) |
| 10 µm | 2–3 | 1.5×10⁻¹⁴ | 1.5×10⁻¹² | 2×10⁻¹² | Marginal (reduce flow to 1.5 m/h in capture zone) |
| 50 µm | 5–10 | 3×10⁻¹⁴ | 3×10⁻¹² | 5×10⁻¹¹ | Need stronger gradient or slower flow |
| 100 µm | 10–20 | 6×10⁻¹⁴ | 6×10⁻¹² | 1×10⁻¹⁰ | Problematic |

**Design solution for large particles:** A two-zone column:
1. **Low-velocity zone** (first 20% of column): v = 0.5–1.0 m/h, captures all sizes >1 µm with ≥1 bacterium
2. **Main zone** (remaining 80%): v = 2–3 m/h, captures smaller complexes; larger complexes already captured

Additionally, a **pre-flocculation step** (gentle stirring in the reactor outlet) encourages bacteria-plastic-bacteria aggregation, increasing n_bacteria per particle for large particles. With 5+ bacteria on a 100 µm particle, F_mag = 2.5×10⁻¹¹ N > F_drag at 2 m/h (1×10⁻¹⁰ N — still marginal). For large particles (>50 µm), the system relies on **gravitational settling + magnetic capture synergy**: large particle complexes settle in the low-velocity zone and are scraped/collected at the bottom.

**Practical capture efficiency (modeled):**
- 1–5 µm: 95–99%
- 5–20 µm: 90–98%
- 20–100 µm: 85–95% (settling + magnetic)
- 100 µm–5 mm: 80–90% (primarily gravitational + magnetic capture in pre-zone)

### 4.3 Column Cleaning

- **Continuous:** 95% of captured material is in the low-velocity zone (first 20% of column)
- **Periodic (every 4–12 h):** Halbach array rotates 90° (motorized, 5–10 seconds) → field collapses → captured material releases → reverse flush at 3× flow for 2 minutes → concentrate to Stage 3
- **Column life:** NdFeB N52 lifetime >50 years (corrosion-protected by NiCuNi coating); no degradation expected

---

## 5. Regrowth Reactor

### 5.1 Design

- **Type:** Continuous stirred-tank reactor (CSTR), aerated, 10–50 L working volume
- **Medium:** Minimal salts medium + 20 mM sodium acetate (C source) + 50 µM FeCl₂ (magnetosome iron) + 0.3 mg/mL meso-DAP (auxotrophy rescue) + 10 µM IPTG (hydrophobin induction)
- **Inoculum:** 1 mL glycerol stock → 100 mL starter → 10–50 L production (3–4 day ramp)
- **Production rate:** 10¹⁰–10¹¹ cells/day (sufficient to replace 20–30% daily bleed from a 100 m³/day system)
- **Oxygen:** 1–3% dissolved O₂ (microaerophilic); controlled by low-rate aeration (0.01–0.1 vvm) + O₂ probe feedback
- **Temperature:** 28°C (ambient in most climates; 5–10 W heater in cold climates)
- **pH:** 6.8–7.2 (self-buffered by medium; monitored)

### 5.2 Medium Cost

| Component | Concentration | Cost per m³ medium |
|-----------|--------------|-------------------|
| Sodium acetate | 20 mM | $0.20 |
| FeCl₂·4H₂O | 50 µM | $0.003 |
| meso-DAP | 0.3 mg/mL | $0.50 |
| IPTG | 10 µM | $0.02 |
| Salts (Na, K, Mg, PO₄, trace) | Standard | $0.05 |
| **Total medium** | — | **$0.77/m³** |
| **Medium per day (50 L)** | — | **$0.04/day** |
| **Medium cost per m³ water treated** | (50 L for 100 m³/day) | **$0.0004/m³** |

---

## 6. Performance Benchmarks

### 6.1 Removal Efficiency by Particle Size

| Size range | Influent (typical WWTP effluent) | Removal % | Effluent concentration |
|-----------|-------------------------------|-----------|----------------------|
| 1–5 µm | 500–5,000 particles/L | 85–95% | 25–750 particles/L |
| 5–20 µm | 200–2,000 particles/L | 90–98% | 4–200 particles/L |
| 20–100 µm | 50–500 particles/L | 90–97% | 1.5–50 particles/L |
| 100 µm–1 mm | 5–50 particles/L | 85–95% | 0.25–7.5 particles/L |
| 1–5 mm | 0.5–5 particles/L | 80–90% | 0.05–1 particles/L |
| **Total (mass basis)** | 0.5–5 mg/L | **90–96%** | 0.02–0.5 mg/L |

### 6.2 Comparison to Alternatives

| Metric | MMS (this invention) | Membrane Bioreactor | Sand Filter | DAF | Coagulation |
|--------|---------------------|---------------------|------------|-----|-------------|
| 1–5 µm removal | 85–95% | >99% | 10–30% | <10% | <10% |
| 5–20 µm removal | 90–98% | >99% | 40–60% | 30–50% | 20–40% |
| 20–100 µm removal | 90–97% | >99% | 80–90% | 60–80% | 60–90% |
| >100 µm removal | 85–95% | >99% | 90–95% | 80–90% | 80–95% |
| Energy (kWh/m³) | 0.05–0.20 | 1.0–3.0 | 0.01–0.05 | 0.05–0.15 | 0.01–0.05 |
| CapEx ($/m³·day capacity) | 80–160 | 200–500 | 20–50 | 50–150 | 10–30 |
| OpEx ($/m³) | 0.004–0.008 | 0.15–0.40 | 0.005–0.02 | 0.02–0.08 | 0.01–0.05 |
| Consumables | Acetate/iron ($0.001/m³) | Membranes ($0.05–0.20/m³) | Sand (periodic) | Polymer ($0.02–0.05/m³) | Coagulant ($0.01–0.04/m³) |
| Self-renewing | Yes | No | No | No | No |
| Selectivity | Plastic-selective | None (size) | None (size) | None | None |
| Footprint (m²/1000 m³/day) | 2–5 | 10–30 | 15–50 | 8–20 | 5–15 |
| Maintenance frequency | Weekly (biomass bleed) | Quarterly (membrane clean) | Monthly (backwash) | Weekly (DAF maintenance) | Weekly (chemical handling) |

---

## 7. Bill of Materials (Community Module, 100 m³/day)

| Component | Spec | Qty | Unit Cost | Subtotal |
|-----------|------|-----|-----------|----------|
| Contact reactor tank | HDPE, 3 m³, 1.5 m dia × 2 m | 1 | $2,500 | $2,500 |
| Recycled glass carrier beads | 2–5 mm, sintered, 1 m³ | 1 | $200 | $200 |
| Halbach magnetic column | 8-segment NdFeB N52, 15 cm ID × 50 cm | 1 | $3,500 | $3,500 |
| Rotation motor + gearbox | 12V DC, 10 rpm, 5 Nm | 1 | $150 | $150 |
| Regrowth reactor | HDPE, 50 L, with aeration | 1 | $800 | $800 |
| Aeration pump | Diaphragm, 20 L/min, 12V | 1 | $80 | $80 |
| Peristaltic dosing pumps | 3× (medium, DAP, IPTG) | 3 | $60 | $180 |
| Flow sensors | Electromagnetic, 2–10 m³/h | 2 | $100 | $200 |
| Turbidity sensor | Inline, 0–1000 NTU | 1 | $120 | $120 |
| DO sensor | Galvanic, 0–10 mg/L | 1 | $150 | $150 |
| Controller | ESP32 + relay board + display | 1 | $50 | $50 |
| Solar PV panel | 0.5 kWp monocrystalline | 1 | $200 | $200 |
| Battery | LiFePO₄, 12V, 20 Ah | 1 | $120 | $120 |
| Piping, valves, frame, fittings | PVC/HDPE, SS hardware | 1 | $1,500 | $1,500 |
| Starter culture + plasmids | MMS-1 strain, glycerol stocks | 1 | $500 (one-time) | $500 |
| **Total** | | | | **$13,250** |

At 100K-unit production scale (cost reduction 40–50%): **$7,000–10,000**

---

## 8. Deployment Scenarios

### 8.1 Urban Wastewater Treatment Plant Retrofit

**Site:** Mumbai, India — 680 ML/day Bandra-Worli Outfall (currently no microplastic treatment)  
**Configuration:** 10 × 100 m³/day MMS modules on secondary effluent line (1.5% of flow as pilot, scaling to 100% if successful)  
**Influent:** 2,000–8,000 particles/L, 0.5–3 mg/L microplastic  
**Effluent target:** <200 particles/L, <0.1 mg/L (90–96% removal)  
**CapEx:** $80,000–160,000 for 1,000 m³/day (10 modules)  
**OpEx:** $1,500–4,000/year (acetate/iron medium, minimal power)  
**Recovered plastic:** 100–300 kg/year (concentrated, sent to local Solar-Polymer Upcycler)  
**Payback:** regulatory compliance + environmental credits, 2–4 years

### 8.2 Household Washing Machine Filter

**Site:** Global consumer market  
**Configuration:** Inline cartridge, 2 L/min, installed on washing machine drain  
**Design:** Mini contact cartridge (0.5 L fluidized bed with MMS-1 immobilized on glass beads) + small Halbach ring magnet  
**Influent:** 100,000–6,000,000 microfibers per wash (50–500 mg)  
**Effluent:** 5,000–300,000 microfibers per wash (90–95% removal)  
**Cartridge life:** 3 months (100 washes)  
**Cost:** $16–30 unit, $8–12 replacement cartridge  
**Recovered microfibers:** 5–50 g/cartridge → collected via municipal takeback → centralized upcycling

### 8.3 Drinking Water Final Polish

**Site:** Rural community well, Lagos, Nigeria  
**Configuration:** 5 m³/day MMS module after existing sand filter  
**Influent:** 50–500 particles/L (after sand filter)  
**Effluent:** 2–25 particles/L (95% removal)  
**CapEx:** $5,000–8,000 (scaled-down module)  
**OpEx:** $200–400/year  
**Beneficiaries:** 500–2,000 people per module  
**Cost per person per year:** $0.10–0.80

---

## 9. Research Frontiers

### 9.1 Nanoplastic Capture (sub-1 µm)

The current system targets 1 µm–5 mm. Nanoplastics (<1 µm, down to 10 nm) are more abundant, more bioavailable, and potentially more dangerous — but cannot be captured magnetically with a single bacterium (magnetic moment too low relative to Brownian motion). Research directions:
- **Bacterial aggregation circuits**: engineer c-di-GMP-mediated auto-aggregation to form 10–50 µm bacterial clusters with 100–500× magnetic moment, capable of trapping nanoplastics within the aggregate matrix
- **Extracellular trap proteins**: engineer secretion of hydrophobin-mucin fusion proteins that form a sticky extracellular mesh capturing nanoparticles
- **Nanomagnetite doping**: incorporate Co²⁺ or Mn²⁺ into magnetosome crystals (CoFe₂O₄, MnFe₂O₄) for 2–5× higher magnetic moment per crystal

### 9.2 Broad-Spectrum Hydrophobin Engineering

- Directed evolution of hydrophobins for higher affinity to specific polymers (e.g., PET-specific hydrophobin with K_D ~10⁻¹⁰ M)
- Multi-hydrophobin display (different hydrophobins for different polymers on the same cell)
- Fusion with plastic-binding peptides (e.g., LCI peptide for PP, Pb_1 for PE) for synergistic binding

### 9.3 In-Situ Magnetic Recovery from Open Water

- Deploy MMS bacteria in constructed wetlands or retention ponds for agricultural runoff microplastic capture
- Use drone-deployed magnetic sweep systems over sediment basins to recover bacteria-plastic complexes
- Integrate with existing water treatment infrastructure without major civil works

### 9.4 Biodegradation Pathway Integration

- Engineer MMS-1 to also express PETase/MHETase (PET-degrading enzymes) on the cell surface
- After magnetic capture, incubate the concentrate at 30°C for 24–48 h → bacteria degrade bound PET into MHET/TPA while still magnetically held → direct monomer production without separate upcycling step
- Challenge: enzyme kinetics vs. binding kinetics (binding is fast; degradation is slow); may require a two-stage bioreactor

### 9.5 Autonomous Deployment & Monitoring

- Edge-AI water quality monitoring (particle count, polymer type via Raman spectroscopy)
- Adaptive flow control based on real-time microplastic load
- Predictive maintenance for Halbach column cleaning cycles
- Cloud-connected fleet management for distributed WWTP modules

---

## 10. Risk Assessment

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|-----------|
| Bacterial escape + colonization | Low (triple containment) | Medium (ecological) | DAP auxotrophy → 24–48 h lysis; kill switch; fitness cost |
| Loss of hydrophobin expression | Medium (plasmid instability) | High (binding loss) | Chromosomal integration of hydrophobin cassette; antibiotic-free selection (DAP-dependent maintenance) |
| Magnetosome loss under stress | Low (MAI is stable) | High (magnetic capture fails) | Monitor cellular iron;定期 re-inoculate from regrowth reactor; MAI chromosomal (not plasmid) |
| Fouling of contact reactor | Medium | Medium (reduced flow) | Fluidization + periodic high-flow flush; biofilm thickness control |
| Temperature sensitivity (<10°C) | Medium (cold climates) | Medium (reduced efficiency 30–50%) | Insulation; low-rate heating (5–10 W) from solar; psychrotolerant *Magnetospirillum* strain engineering |
| Microplastic desorption | Low (hydrophobin binding is strong) | Low (some loss) | Hydrophobin-plastic K_D ~10⁻⁸ M; desorption only in surfactant wash (not present in WWTP) |
| Halbach magnet corrosion | Very Low (NiCuNi coated) | High (column failure) | NiCuNi coating + epoxy encapsulation; 50+ year design life |
| Regulatory approval (GMO release) | Medium (jurisdictional) | High (deployment delay) | Contained use within WWTP (no environmental release); dead-end system (bacteria killed before disposal); engage regulators early |
| Public perception (GMO in water) | Medium | Medium (adoption barrier) | Transparent communication; emphasize containment; no bacteria in effluent (all captured or killed) |
| Competing organisms in reactor | Medium (open system risk) | Medium (reduced MMS-1 dominance) | DAP auxotrophy gives MMS-1 selective advantage only in reactor; periodic re-inoculation; closed contact reactor (not truly open) |

---

## 11. Roadmap

| Phase | Timeline | Milestone |
|-------|----------|-----------|
| **1. Lab Validation** | 2026–2028 | Engineered MMS-1 strain constructed; hydrophobin display confirmed (Western blot + immunofluorescence); magnetosome enhancement verified (TEM + magnetic moment measurement); binding kinetics characterized (quartz crystal microbalance with all major polymers); magnetic capture demonstrated (lab-scale column, >90% removal for 1–100 µm) |
| **2. Bench Prototype** | 2028–2030 | 10 L/day pilot reactor; real WWTP effluent tested; removal efficiency >85% across size range; regrowth reactor integrated; biocontainment validated (DAP auxotrophy kill-off in environmental simulant) |
| **3. Field Pilot** | 2030–2033 | 100 m³/day pilot at operating WWTP; 6-month continuous operation; regulatory engagement (EPA, EU, India CPCB); life-cycle assessment; cost verification |
| **4. Commercial Deployment** | 2033–2038 | First commercial modules ($15–25K); 100–500 WWTP installations; household cartridge development ($30–50); washing machine manufacturer partnerships |
| **5. Global Scale** | 2038–2045 | 100K+ WWTP modules; 1B+ washing machine filters; 1–5 Mt/year microplastic recovered; integration with Solar-Polymer Upcycler network; $8K/module at scale |

---

## 12. Key Parameters Summary

| Parameter | Value |
|-----------|-------|
| Host organism | *M. magneticum* AMB-1 (engineered) |
| Magnetic moment per cell | 3–5 × 10⁻¹⁵ A·m² |
| Hydrophobin | SC3 (*S. commune*) via InaZ display |
| Binding affinity (plastic) | K_D ~10⁻⁸–10⁻⁹ M |
| Binding time | <1 second (collision + adhesion) |
| Contact reactor HRT | 2–5 min |
| Halbach field | 1.2–1.5 T, gradient 50–200 T/m |
| Capture efficiency | >95% (1–100 µm); 85–95% (100 µm–5 mm) |
| Energy consumption | 0.05–0.20 kWh/m³ |
| CapEx (100 m³/day module) | $8,000–16,000 (at scale) |
| OpEx | $0.004–0.008/m³ |
| Module footprint | 2–5 m² per 100 m³/day |
| Bacterial regrowth rate | 10¹⁰–10¹¹ cells/day (50 L reactor) |
| Biocontainment | Triple-layer (DAP auxotrophy + kill switch + fitness cost) |
| Design life | 10+ years (reactor), 50+ years (magnets) |
| Temperature range | 15–35°C optimal; 5–15°C reduced efficiency |
| Polymer coverage | PE, PP, PS, PET, PVC, PA, PU, acrylic, rubber |
| Particle size range | 1 µm–5 mm |
| Effluent target | <200 particles/L, <0.1 mg/L |