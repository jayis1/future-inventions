# Mycoremediation Living Filter — Technical Specification

## 1. System Architecture

### 1.1 Reactor Design

```
┌─────────────────────────────────────────────────────┐
│                    MLF REACTOR                       │
│                                                      │
│  ┌──────────┐  ┌───────────┐  ┌──────────┐          │
│  │  Inlet    │  │  Mycelial │  │ Fluoride  │  →  Out │
│  │  Diffuser │→ │  Matrix   │→ │  Trap     │  │      │
│  │           │  │  (3-stage)│  │ (Ca(OH)₂) │  │      │
│  └──────────┘  └───────────┘  └──────────┘          │
│       ↑              ↑               ↑               │
│   Flow sensor   V_app = 0.5-1.2V   pH monitor       │
│   Temp sensor    I < 50 mA/m³      F⁻ sensor        │
│                                                      │
│  ┌──────────────────────────────────────────────┐    │
│  │  Bioelectrochemical Controller (MCU + FET)   │    │
│  │  - Quorum-sensing feedback loop              │    │
│  │  - Adaptive voltage optimization             │    │
│  │  - Remote telemetry (LoRa/NB-IoT)            │    │
│  └──────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────┘
```

### 1.2 Mycelial Matrix Specifications

| Parameter | Value |
|-----------|-------|
| Matrix composition | *P. chrysosporium* (70%) + *P. ostreatus* (30%) hyphae on lignocellulosic scaffold |
| Scaffold material | Spent brewery grain + hemp hurds (compostable) |
| Matrix porosity | 90–95% |
| Hydraulic conductivity | 1.0–5.0 × 10⁻³ m/s |
| Specific surface area | ~500 m²/m³ (effective enzymatic surface) |
| Channel diameter | 0.5–2.0 mm (tunable via growth conditions) |
| Matrix lifespan | Self-sustaining 10+ years; nutrient top-up every 6–12 months |
| Operating temperature | 15–35°C (optimal: 25–30°C) |
| pH range | 5.5–8.0 (optimal: 6.0–7.0) |

### 1.3 Scale Variants

| Variant | Throughput | Reactor Volume | Footprint | Capital Cost Target |
|---------|-----------|----------------|-----------|-------------------|
| Household (MLF-H) | 10–50 L/day | 5 L | 0.02 m² | $200–500 |
| Community (MLF-C) | 1,000 m³/day | 20 m³ | 10 m² | $250K–500K |
| Municipal (MLF-M) | 100,000 m³/day | 2,000 m³ | 500 m² | $2–5M |

## 2. Biochemical Engine

### 2.1 Engineered Defluorinase Enzymes

Three enzyme classes work in concert to progressively mineralize PFAS:

**Stage 1: Reductive Defluorination (C–F cleavage)**
- Enzyme: **Evolved Perfluoroalkyl Reductive Dehalogenase (ePRD)**
- Origin: Evolved from reductive dehalogenases of *Sphingomonas* sp. and *Dehalococcoides* sp. via PACE
- Mechanism: Cobalamin (B₁₂)-dependent reductive defluorination; electron transfer from reduced flavin mononucleotide (FMNH₂)
- k_cat: 5–20 s⁻¹ (evolved), vs. 0.001–0.05 s⁻¹ (naturally occurring)
- K_M: 10–100 μM for C6–C10 PFAAs
- Expressed from: Fungal-optimized synthetic operon under a constitutive gpdA promoter

**Stage 2: Oxidative Chain Shortening**
- Enzyme: **Lignin Peroxidase (LiP) + Manganese Peroxidase (MnP)** (natively expressed by *P. chrysosporium*)
- Mechanism: Free-radical-mediated C–C bond oxidation of defluorinated intermediates
- Enhanced by: Low applied voltage increasing H₂O₂ availability at cathodic biofilm zones

**Stage 3: Terminal Mineralization**
- Enzyme: **Fluoroacetate Dehalogenase (FAcD)** (from *Pseudomonas* sp., codon-optimized for fungal expression)
- Converts: Fluoroacetate and short-chain fluorinated acids → glycolate + F⁻
- k_cat: 50–100 s⁻¹ (natural enzyme, highly efficient)

### 2.2 Bioelectrochemical Enhancement

| Parameter | Value |
|-----------|-------|
| Applied voltage | 0.5–1.2 V (vs. Ag/AgCl reference) |
| Current density | 0.1–1.0 A/m³ reactor volume |
| Anode material | Graphite fiber brush (biofilm-compatible) |
| Cathode material | Carbon felt (oxygen reduction reaction) |
| Electron mediator | Self-produced by *Geobacter/Shewanella* (riboflavin, flavins) |
| Power consumption | < 0.5 kWh/m³ treated water |
| Enhancement factor | 10–50× increase in PFAS degradation rate vs. biological alone |

**Mechanism of Enhancement:**
The applied voltage polarizes the *Geobacter* biofilm on the anode, driving extracellular electron transfer via conductive pili (nanowires). This maintains the cobalamin cofactor of ePRD in its reduced Co(I) state, which is the catalytically active species for reductive defluorination. Without the applied voltage, the Co(I) state decays to Co(II) with a half-life of ~30 seconds, severely limiting turnover. The electrochemical drive extends this to >10 minutes, enabling the 10–50× rate enhancement.

### 2.3 Quorum-Sensing Regulation

The consortium uses a synthetic quorum-sensing circuit based on *Pseudomonas aeruginosa* LasI/LasR system, modified to:

1. **Detect pollutant load**: F⁻-responsive riboswitch activates when fluoride release rate exceeds threshold, signaling incomplete mineralization
2. **Upregulate enzyme expression**: QS signal auto-induction triggers a 3–5× increase in ePRD and FAcD transcription when pollutant concentration exceeds 10 μg/L
3. **Modulate mycelial growth**: Hyphal extension rate increases 2× under high-pollutant conditions to maximize catalytic surface area
4. **Adaptive voltage request**: MCU receives QS-derived signal and adjusts applied voltage to optimize degradation rate for current pollutant profile

## 3. Materials & Manufacturing

### 3.1 Lignocellulosic Scaffold

- **Primary**: Spent brewery grain (barley husks) — industrial waste stream, effectively free
- **Secondary**: Hemp hurds — renewable, fast-growing, excellent hyphal attachment
- **Binding**: Mycelium self-binds during colonization phase (2-week grow-in period)
- **Form factor**: 30 cm diameter discs, 5 cm thick, stacked in reactor column

### 3.2 Electrode Materials

- **Anode**: Graphite fiber brush (commercially available, $5–15/m²)
- **Cathode**: Carbon felt with MnO₂ catalyst (enhances ORR kinetics)
- **Reference**: Ag/AgCl (embedded, replaceable annual)
- **Current collector**: Titanium wire mesh (corrosion-resistant, minimal cost)

### 3.3 Fluoride Trap

Downstream calcium hydroxide (Ca(OH)₂) packed bed:
- Converts F⁻ → CaF₂ (fluorite, insoluble, non-hazardous)
- Capacity: 1 kg Ca(OH)₂ per 100,000 L treated (at 100 μg/L PFAS inlet)
- CaF₂ is a commercially useful mineral (metallurgy flux, optics grade)
- Replacement interval: 6–12 months for household; 1–3 months for municipal

## 4. Performance Targets

### 4.1 Contaminant Destruction

| Contaminant Class | Inlet Concentration | Target Effluent | Removal Efficiency | Residence Time |
|-------------------|--------------------|-----------------|--------------------|----------------|
| PFOA (C8) | 100 μg/L | < 4 ppt (0.004 μg/L) | >99.99% | 6 hours |
| PFOS (C8) | 100 μg/L | < 4 ppt | >99.99% | 6 hours |
| PFHxS (C6) | 100 μg/L | < 10 ppt | >99.99% | 4 hours |
| GenX (HFPO-DA) | 50 μg/L | < 10 ppt | >99.98% | 5 hours |
| Diclofenac (pharmaceutical) | 10 μg/L | < 10 ng/L | >99.9% | 2 hours |
| Atrazine (pesticide) | 5 μg/L | < 0.1 μg/L | >98% | 3 hours |
| TCE (solvent) | 50 μg/L | < 5 μg/L | >90% | 4 hours |

### 4.2 Fluoride Mass Balance

For 1 m³ of water at 100 μg/L PFOA (C₈HF₁₅O₂):
- Moles PFOA destroyed per m³: ~0.24 mmol
- Moles F⁻ released: ~3.6 mmol (15 F atoms per PFOA molecule)
- Mass F⁻ released: ~68 mg/m³
- CaF₂ precipitate generated: ~141 mg/m³
- **Verified mineralization** by measuring F⁻ in effluent (should equal F⁻ from destroyed PFAS within 95–105% recovery)

## 5. Control & Monitoring

### 5.1 Sensors (embedded)

| Sensor | Type | Purpose |
|--------|------|---------|
| PFAS | Aptamer-based electrochemical | Real-time inlet/effluent PFAS concentration |
| Fluoride ion | Ion-selective electrode | Mineralization verification |
| pH | Glass electrode | Process control (6.0–7.0 optimal) |
| Dissolved oxygen | Optical (luminescence) | Aerobic/anaerobic zone management |
| Temperature | PT100 RTD | Biological activity monitoring |
| Flow rate | Ultrasonic | Hydraulic residence time control |

### 5.2 Bioelectrochemical Controller

- **MCU**: ARM Cortex-M4 (low power, ~50 mW)
- **Algorithm**: PID-controlled voltage adjustment based on PFAS sensor feedback
- **Communication**: LoRa (rural/community) or NB-IoT (municipal) for remote monitoring
- **Data logging**: Onboard SD card + cloud upload (MQTT protocol)
- **Alerts**: Automatic notification when: F⁻ recovery drops <90%, voltage exceeds threshold, pH drifts

## 6. Development Roadmap

| Phase | Duration | Milestones |
|-------|----------|-----------|
| **Phase 1: Enzyme Engineering** | Years 1–3 | PACE evolution of ePRD variants; k_cat > 5 s⁻¹ on C6–C10 PFAAs; express in *P. chrysosporium* |
| **Phase 2: Consortium Development** | Years 2–4 | Stable fungal-bacterial co-culture; quorum-sensing circuit validated; 90% PFAS removal in bench-scale |
| **Phase 3: Pilot Reactor** | Years 3–5 | 1 m³/day pilot; field testing with contaminated groundwater; >99% PFAS destruction demonstrated |
| **Phase 4: Scale-up** | Years 5–7 | 100 m³/day demonstration plant; regulatory approval pathway; cost target <$1/m³ validated |
| **Phase 5: Deployment** | Years 7–10 | Household units <$500; municipal units at scale; technology transfer to water utilities globally |

## 7. Risk Analysis

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Enzyme evolution fails to achieve target k_cat | Medium | High | Alternative: combinatorial active-site saturation mutagenesis + computational enzyme design (AlphaFold3/RFDiffusion) |
| Fungal-bacterial consortium instability | Medium | Medium | Engineered mutualism via cross-feeding (fungal glucose → bacterial electron donors); backup: pure fungal system with exogenous mediators |
| Biofouling of flow channels | Low | Medium | Hyphal self-regeneration; periodic backwash protocol; UV pre-treatment to reduce non-target biomass |
| Temperature sensitivity in cold climates | Low | Low | Insulated reactor housing; exothermic bioactivity provides 2–5°C self-heating; supplemental heater in extreme cold |
| Regulatory approval for engineered organism release | Medium | High | Containment strategy: organisms cannot survive outside reactor (amino acid auxotrophy + kill-switch); contained system, not environmental release |

---

*Technical Specification v1.0 — Mycoremediation Living Filter — 2026-06-16*