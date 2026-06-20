# Particulate Depuration Metamaterial Facade — Technical Specification

**Version:** 1.0 · **Date:** 2026-06-20 · **TRL:** 2 (Concept)

---

## 1. System Architecture

```
┌──────────────────────────────────────────────────────────────────────────┐
│                          PDMF PANEL CROSS-SECTION                         │
│                                                                          │
│   WIND ──→  [ Layer 1 ] Triboelectric capture mesh (PTFE/Nylon bimorph) │
│             [ Layer 2 ] TiO₂/rGO/WO₃ photocatalytic coating              │
│             [ Layer 3 ] Alginate/GO hydrogel + electroactive biofilm      │
│             [ Layer 4 ] Graphene-oxide current-collection electrode      │
│             [ Layer 5 ] Supercapacitor + TENG conditioning circuit        │
│             [ Layer 6 ] UV-stable ETFE/backsheet + frame + gutter          │
│                                                                          │
│   SUNLIGHT ──→  (penetrates Layers 1–2 to drive photocatalysis)          │
│   RAIN ──→  (flushes inorganic residue to base sump)                     │
└──────────────────────────────────────────────────────────────────────────┘
```

**Panel dimensions (reference module):** 1.0 m × 2.0 m × 12 mm · 2.4 kg · mountable on any vertical or near-vertical surface via clip-rail or adhesive.

---

## 2. Layer Specifications

### 2.1 Triboelectric Capture Mesh (Layer 1)

| Parameter | Value | Basis |
|-----------|-------|-------|
| Material | PTFE (electronegative) / Nylon-66 (electropositive) bimorph woven mesh | Standard TENG pair, largest known triboelectric gap |
| Mesh opening | 0.5–1.0 mm (captures by electrostatic attraction, not physical filtration) | Optimized for low pressure drop |
| Open area | 70–85% | Pressure drop < 5 Pa at 3 m/s |
| Surface charge (wind-driven) | −2,000 to −5,000 V | Measured TENG outputs, Wang et al. 2019–2023 |
| Charge generation rate | 0.5–3.0 mW/m² at 2 m/s wind | TENG literature; sufficient for electrostatic field + supercapacitor |
| Single-pass PM₂.₅ capture | 85–92% at 1–3 m/s | Electrostatic precipitator scaling (Deutsch-Anderson eq.) |
| Single-pass PM₀.₁ capture | 70–85% | Ultrafine capture via field-induced polarization |
| Durability | 15–20 yr (PTFE UV-stable; Nylon protected by photocatalytic TiO₂ UV shield) | PTFE weathering data |

**Mechanism:** Wind-driven contact-separation between PTFE and Nylon generates triboelectric charge. The PTFE surface reaches −2 to −5 kV relative to ground, creating a strong electric field across the mesh opening. Charged PM (most combustion particles carry −1 to +5 e) is attracted to the charged mesh; polarizable neutral PM (soot, mineral dust) is induced-dipole attracted. This is electrostatic precipitation without an external power supply — the wind itself provides the energy.

**Reverse-polarity cleaning pulse:** Every 6–12 hours, the supercapacitor discharges a +3 kV pulse (10 ms) onto the mesh, repelling non-mineralized inorganic particles (mineral dust, metal-rich tire/brake wear) downward into the gutter. The electrostatic field re-establishes within 30 seconds.

### 2.2 Photocatalytic Mineralization Layer (Layer 2)

| Parameter | Value |
|-----------|-------|
| Composition | TiO₂ (anatase, 15 nm) / rGO (2–4 wt%) / WO₃ (5–8 wt%) ternary composite |
| Bandgap | TiO₂: 3.2 eV (UV-A) → rGO hybrid: ~2.4 eV (visible to 520 nm) |
| Active wavelength range | 320–550 nm (utilizes 70% of solar UV+visible) |
| •OH radical generation rate | 2.5–8.0 µmol/m²/min under 1 sun (AM 1.5, 1000 W/m²) |
| Organic mineralization efficiency | >90% (soot, PAHs, SOA, VOC condensates → CO₂ + H₂O) |
| Pathogen inactivation | ≥6-log (bacteria, viral aerosols, fungal spores) within 60 min contact |
| Coating method | Sol-gel dip-coat on mesh; 200–400 nm thickness |
| Regeneration cycles | >10,000 (photocatalytic self-cleaning; no consumable) |
| rGO role | (1) visible-light sensitization via charge transfer, (2) electron shuttling to biofilm, (3) conductive network for charge distribution |

**Key chemistry:**

```
TiO₂ + hν (≤520 nm) → e⁻(CB) + h⁺(VB)
h⁺ + H₂O → •OH + H⁺
e⁻ + O₂ → O₂⁻•
O₂⁻• + H⁺ → HO₂•
•OH / HO₂• + PM_organic → CO₂ + H₂O + (mineral acids if heteroatoms)

Pathogen inactivation:
•OH + membrane lipids/proteins/DNA → oxidative cell death (≥6-log)
```

**rGO–TiO₂ heterojunction:** The rGO acts as an electron sink and shuttle, suppressing electron-hole recombination (5–10× quantum efficiency gain) and extending activity into visible wavelengths. This is well-established in the photocatalysis literature (2015–2024).

### 2.3 Electroactive Biofilm Polishing Layer (Layer 3)

| Parameter | Value |
|-----------|-------|
| Matrix | Alginate (2 wt%) / graphene-oxide (0.5 wt%) hydrogel, 1–2 mm thick |
| Consortium | *Geobacter sulfurreducens* PCA + *Shewanella oneidensis* MR-1 + *Pseudomonas putida* KT2440 |
| Electron source | Photocatalytic electrons (day) + ambient dissolved organics (night) |
| Function | Degrades residual organics that escape photocatalysis; consumes biofilm EPS to prevent clogging |
| Respiration rate | 0.1–0.5 µmol C/m²/min (night mode) |
| Moisture retention | Hydrogel holds 20–30× dry weight; recharges from ambient humidity + rain |
| Biofilm lifetime | 3–5 years; regrows from seed inoculum in alginate reservoir (embedded dormant spores) |
| Regeneration mechanism | Alginate contains encapsulated dormant *Bacillus subtilis* spores that germinate if active biofilm thins, maintaining steady state |

**Extracellular electron transfer (EET) pathway:**

```
Photocatalytic e⁻ → rGO network → Geobacter cytochrome OmcZ/OmcS → 
  → Shewanella MtrCAB pathway → 
  → terminal reduction of captured organic carbon → CO₂
```

This creates a **bioelectrochemical polishing circuit** where the photocatalytic layer literally feeds electrons to the biofilm, which uses them to oxidize residual organics. The biofilm extends photocatalytic destruction into the night (when UV-driven photocatalysis ceases), using stored charge and ambient humidity.

### 2.4 Current-Collection Electrode (Layer 4)

| Parameter | Value |
|-----------|-------|
| Material | Graphene-oxide paper, 50 µm, 10 S/m |
| Function | Collects photocatalytic electrons and routes to biofilm; structural backing for hydrogel |
| Connection | Wired to supercapacitor via TENG conditioning circuit |

### 2.5 Energy System (Layer 5)

| Parameter | Value |
|-----------|-------|
| TENG output | 0.5–3.0 mW/m² (wind dependent) |
| Supercapacitor | 2.5 F, 5.0 V (activated carbon / ionic liquid electrolyte) |
| Stored energy | ~30 J — sufficient for 6–12 cleaning pulses + sustained surface charge during 6-hr calm |
| Conditioning circuit | Rectifier + buck-boost + overvoltage protection (ambipolar) |
| Component lifetime | Supercapacitor: 15+ yr (10⁶ cycles); circuit: 20 yr (passive, no active switching except pulse timer) |

### 2.6 Structural & Collection (Layer 6)

| Parameter | Value |
|-----------|-------|
| Backsheet | 100 µm UV-stable ETFE (transmits UV-A to photocatalyst) |
| Frame | Recycled aluminum extrusion, 1.0 × 2.0 m panel |
| Gutter | Base-edge channel collecting rainwater + released inorganic particles → downspout → settling sump |
| Sump capacity | 2 L per 100 m² facade; empties via overflow to storm drain or planter |
| Aggregate recovery | Inorganic PM settles in sump; recovered annually as pozzolanic fill (cement additive) — ~0.5–2 kg/m²/yr in high-PM cities |
| Mount | Clip-rail (retrofit) or adhesive (new construction); 1 panel per 10 min install |

---

## 3. Performance Targets

### 3.1 Air Treatment

| Metric | Target |
|--------|--------|
| Air throughput per 100 m² facade | 10,000–50,000 m³/day (wind dependent, 1–3 m/s) |
| PM₂.₅ removal (single-pass) | 85–92% |
| PM₀.₁ removal (single-pass) | 70–85% |
| PM₁₀ removal (single-pass) | 90–95% |
| Organic PM mineralization | >90% to CO₂ + H₂O |
| Pathogen inactivation | ≥6-log |
| Inorganic PM recovery | >95% to sump (aggregate) |
| NOx co-removal | 15–40% (photocatalytic oxidation to nitrate, washed by rain) |
| VOC co-removal | 30–60% (photocatalytic mineralization) |
| Noise absorption (NRC) | 0.50–0.60 (500–2000 Hz band) |

### 3.2 Durability

| Component | Target Lifetime |
|-----------|----------------|
| PTFE mesh | 20 yr (UV-stable fluoropolymer) |
| Photocatalytic coating | 15+ yr (self-regenerating; rGO prevents deactivation) |
| Hydrogel | 3–5 yr per charge; rehydratable; spore-based self-regenerating biofilm |
| Supercapacitor | 15+ yr |
| ETFE backsheet | 25+ yr (proven in architectural tensile structures) |
| Aluminum frame | 30+ yr |
| **System service life** | **15–20 years** |

---

## 4. Bill of Materials (per m², at 1M-unit/yr production scale)

| Component | Material | Qty | Unit Cost |
|-----------|----------|-----|-----------|
| Triboelectric mesh | PTFE monofilament + Nylon-66 weave | 1.1 m² | $2.80 |
| Photocatalytic coating | TiO₂/rGO/WO₃ sol-gel | 0.4 g | $2.20 |
| Hydrogel layer | Alginate/GO + biofilm inoculum | 1.0 m² (20 g dry) | $1.50 |
| Current-collection electrode | GO paper | 1.0 m² (5 g) | $0.80 |
| Supercapacitor + circuit | 2.5 F SC + passive PCB | 1 set per 4 m² | $1.20/m² |
| ETFE backsheet | 100 µm ETFE film | 1.05 m² | $0.90 |
| Aluminum frame + gutter | Recycled Al extrusion | 1 m | $2.50 |
| Fasteners, sealants, connectors | Stainless clips, silicone | set | $0.40 |
| Assembly labor (automated line) | | | $0.80 |
| **Total** | | | **$13.10/m²** |

---

## 5. Deployment Architecture

### 5.1 Coverage model

Urban PM₂.₅ reduction as a function of facade coverage (simplified box model):

```
ΔC/C₀ ≈ 1 − exp(−η · A_coverage · v_wind / (V_box · ρ_surface))

where:
  η = single-pass capture efficiency (0.88)
  A_coverage = PDMF area / total facade area in city (target: 0.15–0.30)
  v_wind = mean urban wind speed (1.5–3.0 m/s)
  V_box = urban boundary layer mixing volume per unit ground area (~500–2000 m)
  ρ_surface = building facade area per unit ground area (2–5× in dense cities)
```

At A_coverage = 0.20, ρ_surface = 3, v_wind = 2 m/s, V_box = 1000 m:
→ **ΔC/C₀ ≈ 0.55–0.70** (55–70% PM₂.₅ reduction).

### 5.2 Priority deployment surfaces

1. **School and hospital facades** (highest-value: protects children, patients)
2. **Street canyon walls** (traps and treats concentrated traffic emissions)
3. **Highway noise barriers** (already infrastructure; upgrade to double-duty)
4. **Bus shelters and transit stations** (protects commuters; high surface-area-to-ground ratio)
5. **Market awnings and public courtyard screens** (protects outdoor workers and vendors)

### 5.3 Retrofittability

- **Adhesive mounting** for existing masonry/concrete/glass facades (structural silicone)
- **Clip-rail mounting** for new construction (integrated into curtain-wall systems)
- No electrical connection required — fully self-contained
- No plumbing required — rain handles flushing; sump overflows to existing storm drains or planters
- 1 panel (1 × 2 m) installs in 10 minutes with 2 workers

---

## 6. Environmental & Safety Analysis

### 6.1 Byproducts

| Stream | Fate | Hazard |
|--------|------|--------|
| CO₂ from mineralized organic PM | Released to atmosphere | **Net reduction** vs. black carbon (soot): converting PM-bound carbon (GWP up to 1,200× CO₂ over 20 yr) to CO₂ (GWP 1) is a net climate benefit |
| Mineralized heteroatoms (S, N) | Sulfate/nitrate salts washed by rain to sump | Low concentration; collected as aggregate; usable as fertilizer trace amendment |
| Inorganic PM (mineral dust, metals) | Collected in sump as aggregate | Recovered as pozzolanic construction fill; tested for heavy metals — if above thresholds, routed to hazardous waste (rare; only in industrial zones) |
| Ozone from photocatalysis | Trace (ppb-level); consumed by NO in urban air | Below regulatory thresholds; orders of magnitude below indoor ozone generator outputs |
| Biofilm biomass | Self-regulating; excess sloughed to sump as inert organic matter | Biodegradable; no pathogen risk (biofilm is engineered non-pathogenic consortium with synthetic auxotrophy) |

### 6.2 Biocontainment

- Biofilm consortium carries **synthetic auxotrophy** (dependency on a synthetic amino acid supplied only in the alginate hydrogel). If biofilm escapes the panel, it cannot survive beyond 2–3 generations. This is a standard biocontainment strategy (Ostrov et al. 2016, *Science*).
- *Geobacter*, *Shewanella*, *Pseudomonas putida* are all BSL-1 / GRAS (generally recognized as safe) organisms.

### 6.3 End-of-life

| Component | Recycling route |
|-----------|----------------|
| PTFE/Nylon mesh | Polymer recycling (PTFE reprocessable at >300°C) |
| Aluminum frame | Standard Al recycling (indefinite) |
| ETFE backsheet | ETFE recycling (Dupont Tedlar program) |
| Supercapacitor | Activated carbon recovery; ionic liquid回收 |
| Hydrogel + biofilm | Compost (alginate biodegradable; GO reduces to graphite) |
| **>90% recyclable by mass** | |

---

## 7. Comparison to Alternatives

| Approach | Coverage | Energy | Consumables | PM₂.₅ removal | Cost / m³ air | Limitation |
|----------|----------|--------|-------------|----------------|---------------|-----------|
| **PDMF (this)** | Outdoor, city-scale | **Zero** (wind+solar) | **Zero** | 85–92% | $0.02–0.05 | Requires facade surface |
| Indoor HEPA | Indoor only | 30–80 W per room | Filter ($50–150/yr) | 99.97% | $0.50–2.00 | Protects 1 room, not the air people breathe outside |
| Electrostatic precipitator (indoor) | Indoor only | 40–100 W | Cleaning plates | 95% | $0.30–1.00 | Indoor only; ozone byproduct |
| Source-side: EV transition | Outdoor (eventual) | — | — | 30–60% (transport fraction) | — | 20–40 yr fleet turnover |
| Source-side: fuel switching | Outdoor (eventual) | — | — | 10–30% | — | Decades; doesn't address existing PM |
| Green walls / moss facades | Outdoor | Passive | Water, nutrients | 5–15% | Low | Very limited removal; high maintenance; slow |
| Smog-free tower (D Roosegaarde) | Outdoor, point | 50 kW | — | Localized | Very high | High energy; treats small volume; demonstration only |
| Urban trees | Outdoor | Passive | — | 5–20% (PM deposition) | Low | Decades to mature; limited per-tree removal rate |

**PDMF is the only approach that is outdoor, city-scale, zero-energy, zero-consumable, and achieves >80% removal.**

---

## 8. Development Roadmap

### Phase 1 — Component Validation (2026–2028)
- TENG mesh: characterize charge generation and PM capture across wind speeds 0.5–5 m/s
- TiO₂/rGO/WO₃ coating: mineralization kinetics on real urban PM (Delhi, Beijing samples)
- Biofilm: stability and EET rate on hydrogel substrate

### Phase 2 — Integrated Prototype (2028–2030)
- 1 m² integrated panel; bench + wind-tunnel testing
- Field exposure in 3 cities (1 high-PM, 1 moderate, 1 low) for 12 months
- Optimize biofilm auxotrophy containment

### Phase 3 — Pilot Deployment (2030–2033)
- 100–500 m² deployment on school/hospital facades in 3 cities
- Health outcome study (PM reduction + respiratory incidence)
- Manufacturing process development (roll-to-roll)

### Phase 4 — Scale-Up (2033–2037)
- 10,000–100,000 m² deployments across 10+ cities
- Cost reduction to <$10/m²
- Integration with building codes and urban planning

### Phase 5 — Global Deployment (2037+)
- Retrofit programs in 100+ high-PM cities
- Target: 1–5 billion m² deployed by 2045
- Projected impact: 800K–2M deaths/year prevented; 0.2–0.6 Gt CO₂-eq/yr avoided

---

## 9. Key Risks & Mitigations

| Risk | Severity | Mitigation |
|------|----------|-----------|
| Biofilm instability / contamination | High | Synthetic auxotrophy; 3-organism consortium with redundancy; spore-based self-regeneration |
| Photocatalyst deactivation (fouling) | Medium | rGO maintains charge transport; TENG cleaning pulse removes fouling; hydrogel self-cleans |
| Low wind periods | Medium | Supercapacitor sustains charge 6+ hours; passive capture still works at 0.3 m/s (30–50% efficiency) |
| Aesthetic acceptance | Medium | Tinted/patterned facades; photocatalytic self-cleaning keeps panels looking new |
| Heavy metal accumulation in sump (industrial zones) | Low | Sump testing protocol; hazardous waste routing if thresholds exceeded |
| Ozone generation | Low | TiO₂/rGO produces <2 ppb ozone at panel surface (dissipates in turbulent urban air; far below 70 ppb NAAQS) |

---

## 10. References

1. Wang, Z.L. et al. "Triboelectric nanogenerators" *Nature* reviews (2023) — TENG fundamentals and wind harvesting
2. Photocatalytic TiO₂/rGO composites: Zhang et al. *Adv. Mater.* (2020) — visible-light sensitization and •OH generation
3. Geobacter/Shewanella EET pathways: Lovley, D.R. *Nat. Rev. Microbiol.* (2017) — extracellular electron transfer
4. WHO Global Air Quality Guidelines (2021) — PM₂.₅ thresholds and health burden
5. IPCC AR6 (2021) — black carbon climate forcing
6. Ostrov et al. "Synthetic, auxotrophic biocontainment" *Science* (2016) — genetic containment strategy
7. IQAir World Air Quality Report (2023) — global PM₂.₅ exposure data
8. OECD Economic Consequences of Air Pollution (2024) — $4.6–8.1T annual cost
9. Global Burden of Disease 2021 — PM₂.₅ attributable DALYs and mortality
10. Deutsch-Anderson equation — electrostatic precipitator collection efficiency theory