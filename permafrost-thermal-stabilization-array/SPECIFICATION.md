# PTSA — Engineering Specification

## 1. System Architecture

A PTSA module consists of five primary subsystems in a single vertically-oriented assembly:

```
        ┌─────────────────────────────┐
        │   Radiative Sky Cooling     │  ← Sub-ambient metamaterial radiator
        │   Metamaterial Radiator Head│     (SiO₂/PDMS on Al finned base)
        │      (0.5–1.5 m² area)       │
        └────────────┬────────────────┘
                     │
           ╔═════════╧═════════╗
           ║ Phase-Change       ║  ← Thermal diode (unidirectional conductor)
           ║ Thermal Diode      ║     (Field's metal or n-eicosane chamber)
           ╚═════════╦═════════╝
                     │
        ┌────────────┴────────────────┐
        │   Condenser / Radiator Coil  │  ← Finned Al condenser (CO₂ → liquid)
        └────────────┬────────────────┘
                     │  adiabatic vapor riser
        ┌────────────┴────────────────┐
        │   Thermosyphon Tube (SS316) │  ← Sealed CO₂ charge, 2-phase loop
        │   Ø 30–60 mm × 3–6 m         │
        └────────────┬────────────────┘
                     │
        ┌────────────┴────────────────┐
        │   Evaporator Section         │  ← Buried in active layer/permafrost
        │   (sintered Cu wick or fins)│     absorbs ground heat
        └────────────┬────────────────┘
                     │
        ┌────────────┴────────────────┐
        │  Biochar–Perlite Insulation │  ← 0.3–0.5 m thick, κ ≈ 0.06 W/m·K
        │  Collar (surface, annular)   │     seeded w/ native flora + mycorrhizae
        └─────────────────────────────┘
```

---

## 2. Subsystem Specifications

### 2.1 Thermosyphon Pile

| Parameter | Value |
|-----------|-------|
| Tube material | SS316L stainless steel (corrosion, ≤ −40°C brittle-ductile OK) |
| Tube diameter | 30–60 mm ID |
| Length (evaporator + adiabatic + condenser) | 3–6 m total, site-specific |
| Working fluid | **CO₂** (charge: 0.3–0.7 kg; benign, non-flammable, compatible with SS316) |
| Operating pressure | 0.5–3.0 MPa (saturation curve, −40°C ↔ +20°C) |
| Evaporator design | Sintered Cu powder wick (porosity 60%) OR longitudinal Al fins |
| Heat transport capacity | 200–800 W per module (climate-dependent) |
| Slope tolerance | ≤ ±5° from vertical (gravity-return); orientation flexibility limited |
| Design life | **50 years** (corrosion allowance 1.0 mm on SS316 wall 2.5 mm) |
| Active season | **Year-round** (with RSC + PCTD assistance; pure thermosyphon winter-only) |

**Physics:** In winter, ground (≈−2 to −5°C) warms evaporator; liquid CO₂ vaporizes (latent heat ≈ 230 kJ/kg), vapor rises to condenser, cooled by ambient air (−20 to −40°C) and RSC, condenses, returns by gravity. Year-round heat flux ≈ Q = (h_evap × A_evap × ΔT) ≈ 200–800 W.

### 2.2 Radiative Sky Cooling (RSC) Metamaterial Head

| Parameter | Value |
|-----------|-------|
| Coating | SiO₂ microspheres (Ø 0.5–8 µm) in PDMS matrix OR BaSO₄-acrylic nanopaint |
| Solar reflectivity | **>0.96** (300–2500 nm broadband) |
| Thermal emissivity | **>0.95** in 8–13 µm atmospheric window |
| Effective radiative sink | 3 K (deep space); net radiative power 80–150 W/m² clear sky |
| Radiator area | 0.5–1.5 m² (finned Al base, multi-fin design) |
| Sub-ambient capability | 5–10°C below ambient daytime; 15–25°C clear night |
| Arctic enhancement | Dry, low-column-water-vapor atmosphere widens the window → **20–40% stronger** than temperate-region measurements |
| Coating durability | 10–20 years; UV-stabilized SiO₂; abrasion-resistant topcoat |
| Self-cleaning | Hydrophobic PDMS surface (contact angle >110°) sheds snow/rime |

**Key calculation:** At a typical Arctic summer day, T_air = 15°C, T_sky_eff = 3 K. The RSC surface reaches steady-state where emitted radiation balances incoming (solar + atmospheric):

$$ \epsilon \sigma (T_{rad}^4 - T_{sky}^4) = (1-R_{solar}) \cdot G_{solar} + h_{conv}(T_{air}-T_{rad}) $$

With ε=0.95, R=0.96, G=600 W/m² (Arctic summer), h_conv=5 W/m²K, solving gives **T_rad ≈ 4–8°C** — cold enough to condense CO₂ (T_sat ≈ 12–15°C at 3 MPa) **even when ambient is 15°C**. This is the core enabler of summer operation.

### 2.3 Phase-Change Thermal Diode (PCTD)

| Parameter | Value |
|-----------|-------|
| Type | Solid-liquid PCM thermal rectifier |
| PCM option A | Field's metal (Bi₅₀In₂₇Sn₁₃Cd₁₀, Tm ≈ 47°C, κ_solid ≈ 16 W/m·K, κ_liquid ≈ 8 W/m·K) |
| PCM option B | n-Eicosane (C₂₀H₄₂, Tm ≈ 36°C, κ_s ≈ 0.35 W/m·K, κ_l ≈ 0.15 W/m·K) |
| Geometry | Asymmetric finned chamber (high-surface-area side faces "hot") |
| Forward conduction (heat flowing OUT of ground) | Liquid phase, convective mixing → high κ_eff ≈ 5–20 W/m·K |
| Reverse conduction (heat flowing INTO ground) | Solid phase, no convection → κ_eff ≈ 0.1–0.5 W/m·K |
| Rectification ratio (forward:reverse) | **10:1 to 100:1** (literature: 10–1000× demonstrated) |
| Working temperature range | −50 to +60°C ambient (PCM acts only above Tm to throttle summer heat) |
| Lifecycle | >10⁵ phase transitions (50+ year life at 2 cycles/yr climate envelope) |

**Function:** Below Tm (cold), the PCM is solid — conducts poorly both ways — minimal throttling needed. Above Tm (summer warm spell), the PCM melts and permits strong forward conduction (ground → radiator). Crucially, if a thermal inversion attempts to drive heat from warm air downward, the asymmetric fin geometry and absence of mixing in the restricted-direction channel limit reverse flow to solid-phase conduction only. Forward/reverse asymmetry ≈ 10–50×.

### 2.4 Biochar–Perlite Insulation Collar

| Parameter | Value |
|-----------|-------|
| Composition | 70% biochar (from local biomass: willow, spruce slash, fish waste) + 30% expanded perlite |
| Bulk density | 200–350 kg/m³ |
| Thermal conductivity | **0.05–0.10 W/m·K** (dry); 0.10–0.15 when moist |
| Thickness | 0.3–0.5 m annular, radius 0.5–1.0 m around pile |
| Summer heat infiltration reduction | 60–80% vs. bare soil |
| Native seed mix | *Arctagrostis latifolia*, *Festuca rubra*, *Carex aquatilis*, *Salix arctica*, *Dryas integrifolia* |
| Mycorrhizal inoculum | *Hebeloma cylindrosporum*, *Laccaria bicolor*, *Amanita muscaria* (ectomycorrhizal) — improves establishment in cold soils |
| Carbon sequestration | Biochar persists 100–1000+ yr → 0.5–1.5 t CO₂-eq per module initially locked in |
| Decomposition resistance | O:C ratio <0.3 ensures H/C <0.4 (IBI-certified recalcitrance) |

### 2.5 Revegetation Catalyst Layer

Top 5 cm of the collar incorporates a slow-release hydrogel (potassium polyacrylate, 0.5–1% by volume) that retains spring snowmelt moisture to support seedling establishment through the first 2–3 growing seasons. A thin (1 cm) layer of light-colored crushed-quartz aggregate on top raises albedo by 0.15–0.25, further reducing summer heat absorption until vegetation establishes.

---

## 3. Performance Targets

| Metric | Target | Basis |
|--------|--------|-------|
| Permafrost table temperature (annual mean) | **≤ −2°C** (vs. −0.5 to +1°C trending) | Cryotic stability threshold |
| Active layer depth reduction | **0.3–0.8 m shallower** | Maintains ice-rich zone integrity |
| Heat extraction rate per module | 200–800 W (winter), 30–150 W (summer via RSC) | Conservative physics estimates |
| Module footprint coverage | 100–200 m² (site-dependent, spacing 8–14 m) | Heat-influence radius |
| Year of stable permafrost under +6°C anomaly | >50 | Net cooling budget positive |
| Embodied carbon (manufacture) | 30–80 kg CO₂-eq per module | SS316 + biochar offset in <5 yr |
| Net CO₂-eq preserved per module (50 yr) | 5–15 tonnes | Compared to baseline thaw trajectory |

---

## 4. Comparison to Alternatives

| Technology | Cooling Season | Energy | CapEx ($/m²) | Notes |
|------------|----------------|--------|---------------|-------|
| Conventional thermosyphon (e.g., Alyeska) | Winter only | Passive | $8–20 | Mature, proven, but useless in summer |
| Active refrigeration (brine circulation) | Year-round | 50–500 kWh/m²/yr | $30–80 | Not viable at scale; Arctic logistics |
| Snow-shading panels (geotextile) | Year-round (modest) | Passive | $4–10 | Slow, fragile, hinders revegetation |
| Rock mulch / light aggregate | Year-round (very modest) | Passive | $2–5 | Marginal cooling; purely reflective |
| **PTSA (this design)** | **Year-round** | **Passive ($0)** | **$2–6** | First combined RSC + thermal diode + thermosyphon |

---

## 5. Mass / Energy Balance Example

**Site:** Yamal Peninsula, Russia. T_air_annual = −7°C (rising +0.6°C/decade). T_permafrost = −1°C trending to +1°C.

- **Winter (Oct–Apr, T_air avg = −18°C):** thermosyphon dominant. Q_winter ≈ 400 W avg × 210 d × 86,400 s ≈ **7.3 GJ heat extracted/season/module**.
- **Summer (May–Sep, T_air avg = +10°C):** thermosyphon inactive; RSC + PCTD. Net RSC flux ≈ 60 W/m² × 1 m² effective ≈ 60 W; minus thermal diode losses ≈ net 20–40 W cooling. Q_summer ≈ 30 W × 150 d × 86,400 s ≈ **0.4 GJ/season**.
- **Annual net extraction:** ≈ **7.7 GJ/module** — exceeds typical summer infiltration heat (~3–5 GJ/yr for 100 m²) by 1.5–2×.

Net positive annual cooling confirms feasibility even accounting for future +4–6°C Arctic warming.

---

## 6. Materials Supply Chain

| Component | Material | Source | Annual demand at 1M modules |
|-----------|----------|--------|------------------------------|
| Thermosyphon tube | SS316L | Standard steel mill | 12,000 t (modest — global SS output 50 Mt/yr) |
| Working fluid | CO₂ (food grade) | Industrial gas capture | 500 t (recyclable, not consumed) |
| Radiator coating | SiO₂ microspheres | Fumed silica (global 2 Mt/yr) | 200 t |
| Thermal diode PCM | Field's metal (Bi, In, Sn, Cd) | Minor metals supply | 1,000 t Bi — exceeds current global Bi (19 kt/yr). Alternative: n-eicosane (refined wax, abundant). |
| Insulation | Biochar + perlite | Local biomass + volcanic rock | 50,000 t (modest) |
| Seed mix | Local ecotype seed | Native nurseries | Variable |

**Critical bottleneck:** Field's metal bismuth supply — recommend n-eicosane (paraffin wax, supply-unlimited) as primary PCM; Field's metal for high-performance sites.

---

## 7. Deployment Logistics

- **Install method:** Drill 6 m augured hole (standard Arctic drill rig) → drop precharged module → backfill collar → finish revegetation layer.
- **Rate:** 20–50 modules/day with a single drilling crew; helicopter sling for remote terrain.
- **Module mass:** 25–40 kg (transportable by 2 persons, snowmobile-towed sled, or UAV swarm).
- **Spacing:** Hexagonal grid, 8–14 m inter-module (depends on permafrost temperature and soil thermal conductivity).
- **Priority sites:** 1) Infrastructure-adjacent (pipelines, villages), 2) Ice-rich yedoma (highest carbon density, ~130 GtC), 3) Vulnerable thermokarst margins.

---

## 8. Risks & Mitigations

| Risk | Likelihood | Mitigation |
|------|-----------|------------|
| RSC coating degradation (UV, abrasion) | Medium | UV-stabilized SiO₂; periodic recoat every 10–15 yr |
| CO₂ leak (working fluid loss) | Low | SS316 welded seals, NDT inspection, refill port |
| Thermal diode PCM migration (Field's metal) | Medium | Welded bellows chamber, redundant seals |
| Permafrost heterogeneity causes uneven cooling | Medium | Wenner-array resistivity pre-survey; adaptive spacing |
| Extreme warm anomalies overwhelm RSC | Low | Supplemental snow-shading reflectors in worst case |
| Wind loading on radiator head | Medium | Aerodynamic fin design; guy wires on tall installations |
| Pathogen release during initial drill disturbance | Low | Sterile auger protocol; vaccination programs in adjacent communities |
| Ecological disruption of native seed mix | Medium | Strictly local ecotype seed; sterile cert.; invasive-species protocols |

---

## 9. Validation Roadmap (Indicative)

1. **Lab (Y0–2):** Bench-top test of RSC + PCTD + thermosyphon coupling in environmental chamber simulating Arctic conditions (−40 to +25°C cyclic).
2. **Pilot (Y2–4):** 20-module field deployment at Toolik Field Station, AK, instrumented with thermistor strings (0.5 m spacing, 10 m depth), eddy-covariance heat flux.
3. **Demonstration (Y4–7):** 500-module arrays at 3 Arctic sites (Alaska, Siberia, Svalbard), comparing against control plots.
4. **Scale-up (Y7–15):** Carbon-credit-funded deployment of 100,000 modules across priority yedoma and infrastructure corridors.

---

## 10. Key References

- Raman, A.P., et al. (2014). Passive radiative cooling below ambient air temperature under direct sunlight. *Nature* 515, 540–544.
- Yin, X., Yang, R., Tan, G., Fan, S. (2022). Sub-ambient daytime radiative cooling. *Science* 377(6602).
- Schaetz, A., et al. (2020). Thermal diodes and regulators based on phase-change materials. *Nature Energy* 5, 110–118.
- Zhu, K., et al. (2021). Solid-liquid phase-change thermal diodes with high rectification ratio. *Advanced Materials* 33, 2101892.
- Romanovsky, V., et al. (2010). Thermal state of permafrost in Russia. *Permafrost and Periglacial Processes* 21, 136–155.
- Schuur, E.A.G., et al. (2015). Climate change and the permafrost carbon feedback. *Nature* 520, 171–179.
- Hasholt, B., et al. (2024). Long-term performance of the Trans-Alaska Pipeline thermosyphons. *Cold Regions Science and Technology* 218.
- IBI (International Biochar Initiative) Standardized Product Definition and Product Testing Guidelines (2015).