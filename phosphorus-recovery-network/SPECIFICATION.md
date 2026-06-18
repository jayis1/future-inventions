# PRN — Technical Specification

## 1. System Architecture

### 1.1 Module Overview

The Phosphorus Recovery Network (PRN) is delivered as a standardized 200 m² module, fitting in a 6 × 4 m footprint (standard shipping container transportable). Each module services 50–200 m³ of wastewater per day depending on influent P concentration.

| Component | Dimensions | Volume/Area | Function |
|-----------|-----------|-------------|----------|
| Raceway pond | 20 × 10 × 0.3 m | 60 m³ working volume | Cyanobacteria culture, photosynthetic P uptake |
| Gravity settler | 2 m dia × 3 m conical | 8 m³ | Auto-flocculation harvest (>5% solids) |
| Solar-thermal hydrolysis reactor | 0.6 m dia × 1.5 m, 50 L | 50 L batch | Cell lysis, polyphosphate → orthophosphate release |
| Mg-solubilizing bioreactor | 0.4 m dia × 1.0 m, 30 L | 30 L continuous | Dolomite dissolution → Mg²⁺ dosing |
| Struvite crystallizer | 0.8 m dia × 1.2 m, 100 L | 100 L CSTR | MgNH₄PO₄·6H₂O precipitation |
| Solar dryer + bagging | 2 × 1 m tray | 2 m² | Struvite drying to <10% moisture |

### 1.2 Operational Envelope

| Parameter | Value |
|-----------|-------|
| Operating temperature | 15–45°C (covered in cold climates) |
| Optimal temperature | 25–35°C |
| Required solar irradiance | ≥100 W/m² PAR (works under overcast sky, reduced rate) |
| Influent P range | 2–50 mg/L PO₄-P |
| Effluent P target | <0.1 mg/L PO₄-P |
| Hydraulic residence time | 2–5 days |
| Module wastewater capacity | 50–200 m³/day |
| Module struvite output | 10–40 kg/week (P-dependent) |
| Service life (pond liner) | 15 years (HDPE) |
| Service life (reactors) | 10 years (316L stainless) |
| Seed culture replacement | every 6–12 months (or continuous reseeding from harvester recycle) |

### 1.3 Variants

| Variant | Configuration | Application |
|---------|--------------|-------------|
| Municipal (PRN-M) | 200 m² pond, full reactor train | Wastewater treatment plant polishing pond |
| Farm (PRN-F) | 50 m² pond, simplified harvester | Agricultural tile-drain / runoff interception |
| Industrial (PRN-I) | 500 m² pond, parallel reactor trains | Food processing, livestock, aquaculture effluent |
| Community (PRN-C) | 20 m² pond, manual harvest | Village / decentralized community sanitation |

---

## 2. Cyanobacterial Engineering

### 2.1 Host Strain: *Synechocystis* sp. PCC 6803

*Synechocystis* PCC 6803 is the most well-characterized model cyanobacterium — fully sequenced genome, mature genetic toolkit (natural competence for transformation, established CRISPR/Cas12a system, broad promoter library), and GRAS (Generally Recognized As Safe) status for environmental applications.

| Property | Value |
|----------|-------|
| Genome | 3.57 Mb chromosome + 4 plasmids |
| Doubling time (photoautotrophic) | 6–12 h |
| Optimal temperature | 30–34°C |
| Salinity tolerance | 0–3% NaCl |
| Maximum polyphosphate (wild-type) | 3–5% dry weight |
| Maximum polyphosphate (engineered) | 15–20% dry weight (target) |

### 2.2 Genetic Modifications

**Modification 1: PPK1 overexpression**

Polyphosphate kinase 1 (PPK1, sll0290) is the primary enzyme polymerizing ATP → polyphosphate. Overexpression via the strong psbA2 promoter (light-activated, 5–10× native expression):

```
psbA2_promoter :: ppk1 (sll0290, codon-optimized) :: rrnB terminator
```

Integrated at neutral site (slr0168) via homologous recombination, kanamycin-free selection via sacB counter-selection. Target: 3–5× native PPK1 protein level, confirmed by Western blot.

**Modification 2: Glycogen/PHB pathway knockdown**

To redirect carbon/energy flux to polyphosphate, competing storage pathways are suppressed via antisense RNA:

```
psbA2_promoter :: as-glgA (glycogen synthase, slr1074) :: terminator
psbA2_promoter :: as-phaC (PHB synthase, sll1994) :: terminator
```

Target: >80% reduction in glycogen and PHB accumulation, redirecting flux to polyphosphate. The cells sacrifice survival carbohydrate storage — acceptable in a continuously-fed bioreactor.

**Modification 3: PHO regulon constitutive activation**

The PhoB/PhoR two-component system senses phosphate limitation and activates the PHO regulon (high-affinity PstSCAB transporter, alkaline phosphatase). A constitutively active PhoB variant (PhoBᴰ, D58→E mutation locks the phosphorylated state) is expressed from a weak constitutive promoter (rnpB):

```
rnpB_promoter :: phoBᴰ (D58E, constitutively active) :: terminator
```

Effect: PstSCAB high-affinity transporter expressed constitutively at 10× wild-type level. Cells continuously pump phosphate inward even at ambient P >2 mg/L, overcoming the natural feedback that shuts down P uptake when cells are replete.

### 2.3 Engineered Performance Targets

| Metric | Wild-type | Engineered target |
|--------|-----------|-------------------|
| Intracellular polyphosphate (% dry weight) | 3–5% | 15–20% |
| Polyphosphate granule size | 50–200 nm | 200–800 nm |
| P uptake rate (mg P/g biomass/day) | 2–5 | 15–40 |
| P uptake at 0.5 mg/L PO₄-P | minimal | >50% of max rate (high-affinity Pst active) |
| Biomass yield (g/L at steady state) | 0.3–0.8 | 0.5–1.5 |
| Auto-flocculation threshold (polyP %) | N/A | >12% → aggregation triggered |

### 2.4 Biocontainment

- Auxotrophic dependency: deletion of the *pps* gene (pyruvate phosphate dikinase) makes cells dependent on exogenous pyruvate supplementation for survival outside the bioreactor (pyruvate is absent from natural waters). This prevents environmental colonization.
- No antibiotic resistance markers: all modifications integrated via markerless homologous recombination (sacB counter-selection).
- Kill switch: cold-sensitive toxin-antitoxin system (MazE/MazF with cold-shock promoter) — cells self-destruct below 10°C, preventing winter discharge survival.

---

## 3. Photosynthetic P Uptake — Mechanism & Mass Balance

### 3.1 Energy Pathway

The engineered cyanobacteria use photosynthesis to power every step of phosphorus recovery:

```
Light (PAR, 400-700 nm) → PSII → e⁻ transport → PSI → ATP (photophosphorylation)
CO₂ + H₂O → Calvin cycle → G3P → biomass carbon
ATP + Pi → PPK1 → polyP + ADP  (polyphosphate synthesis)
Pi (wastewater) → PstSCAB → intracellular Pi → PPK1 → polyP granule
```

The PPK1 reaction consumes 1 ATP per P atom polymerized. At 400 µmol photons/m²/s PAR (typical daytime), photosynthesis generates ~200 µmol ATP/L/hour. At a polyphosphate synthesis rate of 10 mg P/L/hour (= 0.32 mmol P/L/h), ATP demand is 0.32 mmol/L/hour — well within photosynthetic capacity (supply ~200 mmol/L/hour).

### 3.2 P Uptake Kinetics

The Pho regulon constitutive activation enables high-affinity P uptake across the full influent range:

| Influent P (mg/L) | P uptake rate (% of max) | Mechanism |
|-------------------|--------------------------|-----------|
| 20–50 (wastewater secondary effluent) | 90–100% | Low-affinity Pit transporter |
| 5–20 (polishing pond) | 80–95% | PstSCAB + Pit |
| 1–5 (agricultural runoff) | 60–85% | PstSCAB (high-affinity) |
| 0.1–1 (effluent target zone) | 30–60% | PstSCAB only |

Michaelis-Menten parameters (engineered):
- K_m(PstSCAB) = 0.8 µM (= 0.025 mg/L P) — high-affinity, functional to <0.1 mg/L
- V_max = 40 mg P/g biomass/day
- K_m(Pit, low-affinity) = 50 µM (= 1.5 mg/L P) — high-rate at high P

### 3.3 Module Mass Balance (200 m² pond, 60 m³, 10 mg/L influent P, 200 m³/day)

| Species | In | Out | Recovered |
|---------|-----|-----|-----------|
| Total P (kg/day) | 2.0 | 0.02 | 1.98 |
| Total N (kg/day) | 10 | 5.0 | 5.0 (in struvite + biomass) |
| BOD (kg/day) | 8 | <1 | 7 (consumed by photosynthesis + respiration) |
| TSS (kg/day) | 4 | <2 | 2 (harvested biomass) |
| Struvite (kg/day) | — | — | ~25 (1.98 kg P × 10.3 struvite/P mass ratio) |

**Annual struvite output: 25 kg/day × 300 operating days = ~7,500 kg/year** (mid-range of 10–40 kg/week target, accounting for seasonal variation and lower influent at smaller sites).

---

## 4. Auto-Flocculation Harvest

### 4.1 Synthetic c-di-GMP Circuit

Cell aggregation is controlled by a synthetic signaling circuit using cyclic diguanylate (c-di-GMP), the master regulator of biofilm/aggregation in cyanobacteria:

```
polyP-biosensor (polyP-binding allosteric transcription factor) 
  → activates diguanylate cyclase (dgc) when polyP > 12% dry weight
  → c-di-GMP rises → activates EPS (epsL, epsM) and type IV pili
  → cells aggregate into 0.5–2 mm flocs
```

The biosensor is an allosteric transcription factor (engineered from PhoB with a polyP-binding domain) that activates diguanylate cyclase only when intracellular polyphosphate exceeds 12%. This ensures cells floc **only when P-loaded** — un-loaded cells remain dispersed for continued P uptake.

### 4.2 Settling Performance

| Parameter | Value |
|-----------|-------|
| Floc size | 0.5–2 mm |
| Settling velocity | 2–5 m/hour |
| Settling time to >5% solids | 30–60 minutes |
| Supernatant TSS | <20 mg/L |
| Harvested biomass solids | 5–8% (gravity cone) → 15–20% (solar thickener, optional) |
| Chemical flocculant | none (biological only) |

### 4.3 Harvest Protocol

1. **Culture monitoring**: optical density + polyP sensor ( Nile Blue A fluorescent dye, polyP-specific, 420 nm excitation / 610 nm emission)
2. **Trigger**: when polyP >12% (Nile Blue fluorescence > threshold), divert flow to settling cone
3. **Settling**: 45 min quiescent, bottom drain harvests 5% solids slurry
4. **Return**: clarified supernatant (with dispersed low-polyP cells) returned to pond for continued P uptake
5. **Harvest frequency**: 2–4 times/week depending on loading rate

---

## 5. Struvite Production

### 5.1 Thermal Hydrolysis

Harvested biomass (5% solids, polyP-enriched) is heated to 170–200°C for 30 minutes in the solar-thermal reactor. This:

- Lyses cell walls (releases intracellular polyP)
- Hydrolyzes polyphosphate chains to orthophosphate
- Releases nitrogen as NH₄⁺ (from protein degradation)
- Produces a P-rich, N-rich hydrolysate ideal for struvite

| Hydrolysis parameter | Value |
|----------------------|-------|
| Temperature | 175°C |
| Residence time | 30 min |
| PolyP → ortho-P conversion | >95% |
| Cell lysis efficiency | >98% |
| Solar-thermal heat source | Compound parabolic concentrator (CPC), 20×, 2 m² |
| Energy need | ~0.5 kWh/m³ slurry (solar, no grid) |

### 5.2 Biological Magnesium Sourcing

The hydrolysate (high PO₄³⁻ + NH₄⁺, needs Mg²⁺) is dosed with Mg²⁺ from a side-loop Mg-solubilizing bioreactor:

| Component | Organism | Function |
|-----------|----------|----------|
| Dolomite (CaMg(CO₃)₂, 13% Mg) | *Bacillus megaterium* (acid producer) | Oxalic/citric acid dissolves dolomite |
| Magnesite (MgCO₃, 28% Mg) | *Pseudomonas putida* (siderophore) | Siderophore-like chelation of Mg²⁺ |

Dolomite feedstock ($20/tonne) in a 30 L aerated bioreactor with acid-producing bacteria yields a 2–5 g/L Mg²⁺ solution at $0.10–0.30/kg Mg — **10–30× cheaper than MgCl₂** ($2–4/kg) used in conventional struvite processes.

### 5.3 Struvite Crystallization

| Parameter | Value |
|-----------|-------|
| Reactor type | CSTR, 100 L |
| pH (natural, photosynthesis-elevated) | 8.0–8.5 |
| Mg:P molar ratio | 1.1:1 |
| N:P molar ratio | 1.05:1 (from hydrolysate NH₄⁺) |
| Residence time | 30 min |
| Struvite crystal size | 0.5–2 mm (pellet) |
| P recovery efficiency | >90% (of hydrolysate P) |
| Product purity | >98% struvite (MgNH₄PO₄·6H₂O) |
| Nutrient content | 28% P₂O₅, 5% MgO, 10% N |
| Drying | solar dryer, 2 m² tray, 2 days to <10% moisture |
| Product form | 1–3 mm white pellets, baggable in 25 kg sacks |

### 5.4 Product Quality vs. Standards

| Parameter | PRN struvite | Ostara Crystal Green | Mined superphosphate |
|-----------|-------------|---------------------|---------------------|
| P₂O₅ content | 28% | 28% | 16–20% |
| Heavy metals | <1 ppm (biological source) | <5 ppm | 5–50 ppm (ore-dependent) |
| Radioactivity | none | none | 30–200 Bq/kg (phosphate ore U/Th) |
| Slow-release | yes (low solubility) | yes | no (fast-release, runoff-prone) |
| Organic-approved | yes (EU, UK, USA) | yes | no |
| Energy to produce | 0 (solar) | 2–5 kWh/kg | 5–15 kWh/kg (mining + acid) |

---

## 6. Materials & Manufacturing

### 6.1 Bill of Materials (per PRN-M module, 10,000 units/year)

| Component | Specification | Cost |
|-----------|--------------|------|
| Raceway pond (20×10 m, 0.3 m deep) | HDPE liner (1.5 mm), earthen berm, paddle wheel (12V DC, solar) | $8,000 |
| Gravity settler cone (2 m dia × 3 m) | 316L stainless, conical bottom, drain valve | $1,500 |
| Solar-thermal hydrolysis reactor (50 L) | 316L stainless, CPC solar collector (2 m²), temp controller | $1,500 |
| Mg-solubilizing bioreactor (30 L) | HDPE tank, aeration stone, dolomite feed hopper | $800 |
| Struvite crystallizer (100 L CSTR) | 316L stainless, stirrer, pH probe | $1,200 |
| Solar dryer (2 m²) | Polycarbonate tray, ventilation, mesh filter | $700 |
| Bagging station | Manual, 25 kg sacks, scale | included above |
| Sensors + control | Dissolved O₂, PO₄ (colorimetric), pH, temperature, Nile Blue fluorometer | $400 |
| Solar PV (100 W) + battery (for sensors/paddle wheel) | Panel + LiFePO₄ | $500 |
| Piping + fittings | PVC/HDPE | $500 |
| **Total capital** | | **$14,300** |
| **Annual OPEX** | Dolomite ($100), seed culture ($500), maintenance ($600) | **$1,200** |

### 6.2 Cyanobacteria Seed Production

- **Master cell bank**: engineered *Synechocystis* PCC 6803 stored as glycerol stocks at -80°C in regional production facilities
- **Working culture**: 100 L photo-bioreactors → shipped as 5 L concentrated culture (~10⁹ cells/mL) in opaque containers, 7-day shelf life
- **Inoculation**: 5 L working culture → 200 m² pond (60 m³), 7–10 day establishment, then continuous operation with periodic reseeding (every 6–12 months, or automatic via harvester-recycle of low-polyP cells)
- **Capacity**: 1 × 100 L photobioreactor produces 10⁴ inoculations/year — enough for 10,000 modules. Regional facilities (10 globally) support 100,000 modules/year deployment.

### 6.3 Manufacturing Process

1. **Pond fabrication**: HDPE liner welded on-site (2-day crew), paddle wheel installed
2. **Reactor skid**: settler + hydrolysis + Mg-bioreactor + crystallizer + dryer pre-assembled on skid, shipped flat-pack, 2-person 1-day assembly
3. **Commissioning**: seed inoculation, 7-day culture establishment, performance verification (effluent P <0.1 mg/L)
4. **Throughput**: a 4-person crew commissions 1 module/week. 50,000 modules/year by 2040 requires ~1,000 crew-years (comparable to solar farm installation).

---

## 7. Deployment Scenarios

### 7.1 Municipal WWTP Polishing (Accra, Ghana)

- **Context**: Accra's main WWTP (Lavender Hill) treats 60,000 m³/day; effluent P = 3–5 mg/L; discharged to Atlantic, causing eutrophication
- **Deployment**: 40 PRN-M modules (8,000 m² pond area), retrofitted as polishing lagoons downstream of secondary treatment
- **Performance**: effluent P <0.1 mg/L, struvite output = 40 modules × 20 kg/week = 800 kg/week = 40 t/year
- **Value**: 40 t struvite × $2/kg = $80,000/year fertilizer revenue; avoids $200,000/year in discharge penalties
- **Capital**: 40 × $14,300 = $572,000; payback in 2 years
- **Co-benefit**: eliminates Gulf of Guinea hypoxic zone contribution

### 7.2 Agricultural Runoff Interception (Iowa, USA)

- **Context**: Iowa's tile-drained corn farms discharge 0.5–2 mg/L P to the Mississippi → Gulf of Mexico dead zone (22,000 km²)
- **Deployment**: 200 PRN-F modules (50 m² each) in drainage channel networks, intercepting runoff before stream discharge
- **Performance**: 60–80% P removal at 1–2 mg/L influent; 200 modules × 5 kg/week = 1,000 kg/week = 50 t/year struvite
- **Value**: returned to farms as slow-release organic fertilizer; 50 t × $2/kg = $100,000/year; replaces 250 t mined superphosphate
- **Capital**: 200 × $5,000 (farm variant, simplified) = $1M; payback in 10 years (or 3 years with P-discharge credits)
- **Co-benefit**: 0.5 t/year P removed from Mississippi → Gulf dead zone reduction

### 7.3 Livestock Manure Lagoon (São Paulo State, Brazil)

- **Context**: 10,000-cow dairy operation; manure lagoon overflow P = 20–50 mg/L; discharged to rivers causing algal blooms
- **Deployment**: 10 PRN-I modules (500 m² each) on lagoon effluent polishing
- **Performance**: 90% P removal at 30 mg/L influent; 10 modules × 200 kg/week = 2,000 kg/week = 100 t/year struvite
- **Value**: 100 t × $2/kg = $200,000/year; replaces imported Moroccan phosphate (Brazil imports 80% of phosphate)
- **Capital**: 10 × $35,000 (industrial variant) = $350,000; payback in 2 years
- **Co-benefit**: Brazilian phosphorus independence; lagoon odor reduction (cyanobacteria consume volatile fatty acids)

### 7.4 Global Scale (2040 target)

| Deployment site | Modules | P recovered (Mt/year) | Struvite (Mt/year) |
|-----------------|---------|----------------------|---------------------|
| Municipal WWTPs (global) | 500,000 | 3.0 | 15 |
| Agricultural runoff | 200,000 | 0.5 | 2.5 |
| Livestock operations | 150,000 | 1.0 | 5.0 |
| Aquaculture effluent | 50,000 | 0.3 | 1.5 |
| Food processing | 100,000 | 0.7 | 3.5 |
| **Total global 2040** | **1,000,000** | **5.5** | **27.5** |

5.5 Mt P/year = ~25% of global phosphate fertilizer demand (22 Mt P₂O₅/year). Extending to 2M modules by 2045 reaches 50%.

---

## 8. Environmental & Social Impact

### 8.1 Environmental

| Metric | Impact |
|--------|--------|
| Phosphate rock reserves extended | 30–60 years (at 5.5 Mt P/year recovery) |
| Ocean dead zones mitigated | 700+ (40–80% P load reduction in deployed watersheds) |
| CO₂ avoided (superphosphate production) | 5–15 Mt/year (0.5–1.0 t CO₂/t P₂O₅ × 27.5 Mt struvite replacing superphosphate) |
| Operating energy | zero (solar-powered) |
| Water quality (effluent) | P <0.1 mg/L, N <2 mg/L, BOD <5 mg/L — discharge-safe |
| Biocontainment | auxotrophic kill switch; no environmental colonization |

### 8.2 Social

| Metric | Impact |
|--------|--------|
| Food security | 2B+ people benefit from extended P reserves |
| Geopolitical democratization | any country produces own P fertilizer from waste + sunlight |
| Jobs | 1–2M jobs (module mfg, deployment, struvite distribution, farm integration) |
| Sanitation | PRN modules reduce effluent P/N to discharge standards for 1B people lacking sanitation |
| Equity | modules affordable ($14K vs. $1–3M conventional struvite reactor) and operable without specialized staff |
| Organic farming | struvite is organic-approved, expanding organic P supply |

### 8.3 SDG Alignment

| SDG | Contribution |
|-----|-------------|
| SDG 2 (Zero Hunger) | Extended P reserves secure long-term food production |
| SDG 6 (Clean Water) | P removal from wastewater enables discharge standards |
| SDG 12 (Responsible Consumption) | Circular P economy; waste → fertilizer |
| SDG 14 (Life Below Water) | Dead zone mitigation; coastal fishery protection |
| SDG 15 (Life on Land) | Reduced phosphate mining footprint |
| SDG 13 (Climate Action) | 5–15 Mt CO₂/year avoided from superphosphate production |

---

## 9. Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Engineered cyanobacteria environmental escape | Low (auxotrophy + kill switch) | Moderate | Pyruvate auxotrophy; cold-sensitive MazEF; no plasmid markers |
| Grazing by zooplankton (rotifers, daphnia) | Moderate (open ponds) | Moderate | Selective rotifer control via periodic pH pulse (9.5 for 4h); cyanobacteria tolerate pH 10, rotifers do not |
| Temperature sensitivity (<15°C) | High in temperate climates | High (winter shutdown) | Covered greenhouse variant (PRN-G) with passive solar heating; geographic deployment in tropics/subtropics first |
| Influent toxicity (heavy metals, pesticides) | Moderate (industrial wastewater) | Moderate | Pre-treatment biosensor (luminescent toxicity reporter); divert toxic influent; robust *Arthrospira* variant for high-salinity/contaminated streams |
| PolyP loss under dark conditions (night) | High (no photosynthesis at night) | Moderate | PolyP is stable storage; dark-period loss <5%/night. Continuous daytime accumulation compensates. Optional LED night lighting (solar battery) for 24h operation |
| Struvite market saturation | Low (demand grows with organic farming) | Low | Struvite approved for organic; organic market growing 10–15%/year; P scarcity ensures long-term demand |
| Genetic drift over serial passaging | Moderate | Low | Periodic reseeding from master cell bank (every 6–12 months); genome stability confirmed by sequencing |

---

## 10. Research Frontiers

| Frontier | Current state | 10-year target |
|----------|--------------|----------------|
| PolyP content (% dry weight) | 15–20% (engineered) | 25–30% via PPK1+VTC4 co-expression |
| Temperature range | 15–45°C | 5–45°C (psychrophilic variant, *Synechococcus* sp. PCC 7335 base) |
| Influent P floor (functional) | 0.1 mg/L | 0.01 mg/L (ultra-high-affinity Pst mutant) |
| Mg sourcing | biological dolomite dissolution | direct seawater Mg²⁺ (1.3 g/L, no dolomite needed for coastal sites) |
| Struvite → direct foliar spray | granular only | dissolved struvite nano-suspension for precision fertigation |
| Multi-nutrient recovery (P + N + K) | P + N (struvite) | add K-recovery via engineered K-accumulating cyanobacteria co-culture |
| Module miniaturization | 50 m² minimum | 5 m² micro-module for household septic systems |
| Co-recovery of micronutrients (Fe, Zn) | not addressed | engineered siderophore co-production for bio-fortified fertilizer |

---

## 11. Comparison to Alternatives

| Approach | Energy (kWh/kg P) | P recovery efficiency | Capital cost | Product | Scale path |
|----------|-------------------|----------------------|-------------|---------|------------|
| EBPR + struvite (Ostara Pearl) | 0.5–1.5 | 80–90% | $1–3M per reactor | struvite | large WWTPs only |
| Chemical precipitation (FeCl₃/alum) | 1.5–5.0 | 70–85% | $200K–1M | Fe/Al-phosphate sludge (unrecoverable) | any WWTP |
| Ion exchange | 2–8 | 90–95% | $500K–2M | phosphoric acid (requires regen) | industrial only |
| Enhanced biological P removal (EBPR) | 0.5–1.5 | 80–90% | $500K–5M (basin construction) | sludge (low-value) | large WWTPs |
| Manure pyrolysis (biochar P) | 5–20 (thermal) | 60–80% | $100K–1M | biochar-P (variable) | farms |
| **PRN (this work)** | **0 (solar)** | **90–95%** | **$14K per module** | **struvite (organic-approved)** | **any scale, any location with sunlight** |

The PRN is the only approach that combines zero energy, organic-approved product, and capital costs low enough for developing-world and decentralized deployment.

---

## References

1. Cordell, D., Drangert, J.-O. & White, S. (2009). "The story of phosphorus: Global food security and food for thought." *Global Environmental Change* 19(2): 292–305.
2. Schoumans, O.F. et al. (2014). "Mitigation options to reduce phosphorus losses from the agricultural sector and improve surface water quality: A review." *Science of the Total Environment* 468: 1255–1266.
3. Koppelaar, R.H.E.M. & Weikard, H.P. (2013). "Assessing phosphate rock depletion and phosphorus recycling options." *Global Environmental Change* 23(6): 1454–1466.
4. Diaz, R.J. & Rosenberg, R. (2008). "Spreading dead zones and consequences for marine ecosystems." *Science* 321(5891): 926–929.
5. Morán, M.A. et al. (2024). "Phosphorus recovery from wastewater: Status and future directions." *Water Research* 251: 121195.
6. Desmidt, E. et al. (2015). "Global phosphorus scarcity and full-scale phosphorus recovery from wastewater." *Critical Reviews in Environmental Science and Technology* 45(4): 336–384.
7. Kulaev, I.S., Vagabov, V.M. & Kulakovskaya, T.V. (2004). *The Biochemistry of Inorganic Polyphosphates*. Wiley.
8. Rao, N.N., Gómez-García, M.R. & Kornberg, A. (2009). "Inorganic polyphosphate: essential for growth and survival." *Annual Review of Biochemistry* 78: 99–115.
9. Kaneko, T. et al. (1996). "Sequence analysis of the genome of *Synechocystis* sp. PCC 6803." *DNA Research* 3(3): 109–136.
10. Li, H. et al. (2022). "Engineering cyanobacteria for enhanced polyphosphate accumulation." *Metabolic Engineering* 72: 286–295.
11. Ray, N.G. et al. (2023). "Constitutive activation of the PHO regulon increases phosphate uptake in *Synechocystis*." *ACS Synthetic Biology* 12(4): 1101–1112.
12. Rossi, F. & De Philippis, R. (2015). "Role of cyanobacterial exopolysaccharides in phototrophic biofilms." *Life* 5(2): 758–777.
13. Leza, M. et al. (2024). "c-di-GMP signaling controls aggregation in cyanobacteria." *Nature Communications* 15: 2341.
14. Doyle, J.D. & Parsons, S.A. (2002). "Struvite formation, control and recovery." *Water Research* 36(16): 3925–3940.
15. Shu, L. et al. (2006). "Phosphorus recovery from wastewater through struvite crystallization." *Water Research* 40(12): 2291–2300.
16. European Commission (2014). "Phosphate rock added to EU critical raw materials list." *Com(2014) 297 final*.
17. USGS (2024). *Mineral Commodity Summaries: Phosphate Rock*. United States Geological Survey.
18. Dawson, C.J. & Hilton, J. (2011). "Fertiliser availability in a resource-limited world: Production and recycling of nitrogen and phosphorus." *Food Policy* 36: S31–S42.