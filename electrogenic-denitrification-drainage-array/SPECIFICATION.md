# SPECIFICATION — Electrogenic Denitrification Drainage Array (EDDA)

**Invention #:** 042
**Created:** 2026-08-17
**TRL:** 2 (Concept)

---

## 1. System Overview

A modular, sunken bioelectrochemical trench reactor installed at the edge of tile-drained agricultural fields. Two coupled electrochemical processes — autotrophic denitrification at a biocathode and nitrate-to-ammonium conversion in a BMED sidestream — combine to destroy nitrate (to N₂) and recover a fraction as (NH₄)₂SO₄ fertilizer. PV + bioanode provide electrons; a phase-change backfill maintains reactor temperature year-round.

### 1.1 Module Geometry (per ~1 ha drained cropland)
- Trench: 1.2 m depth × 0.6 m wide × ~10 m long, buried along tile outlet
- Active reactor volume: ~0.7 m³ per module
- Treatment capacity: 0.5–1.5 ha drained area, 2–15 mg N/L influent, 5–50 m³/day flow
- Mass: ~120 kg installed (modular plug sections, liftable by 2 people)
- PV panel: 50–150 W mono-Si, ground-mounted at trench edge, 12 V battery (LiFePO₄, 0.5–1.0 kWh)

### 1.2 Process Targets (per module, at 1 ha, 8 mg N/L, 20 m³/day)
| Parameter | Target | Best-in-class passive (woodchip) |
|---|---|---|
| Nitrate removal efficiency | 85–98% | 25–60% |
| N₂O as fraction of influent N | <0.3% | 3–15% |
| Ammonium sulfate recovery | 15–35% of influent N | 0% |
| Organic carbon dosing required | 0 (autotrophic) | high (woodchip consumption) |
| Footprint per drained ha | 0.6 m wide buried | 3–10 m²/ha (wetlands) |
| Operating temperature range | 12–20°C (PCM buffered) | tracks soil (0–25°C, stalls <5°C) |
| Winter removal efficiency | ≥70% | <15% |
| Service interval | 1 yr (sensor cal + inoculum refresh) | 1–3 yr (woodchip replacement) |
| Module lifespan | 15–20 yr | 10–15 yr |

---

## 2. Biocathode: Autotrophic Denitrification

### 2.1 Mechanism
Denitrifying autotrophs (predominantly *Thiobacillus denitrificans*-like, *Pseudomonas*, *Paracoccus* spp.) colonize a graphite felt biocathode held at **−0.3 to −0.6 V vs. SHE**. Electrons from the cathode reduce nitrate via the canonical pathway:

```
NO₃⁻ + 2 H⁺ + 2 e⁻ → NO₂⁻ + H₂O          (NarG/NapA, +0.42 V)
NO₂⁻ + H⁺ + e⁻    → NO + H₂O              (NirK/NirS, +0.35 V)
2 NO + 2 H⁺ + 2 e⁻ → N₂O + H₂O           (NorBC, +0.18 V)
N₂O + 2 H⁺ + 2 e⁻ → N₂ + H₂O             (NosZ, +0.96 V)
```

Overall: `2 NO₃⁻ + 12 H⁺ + 10 e⁻ → N₂ + 6 H₂O`  (E° = +0.74 V)

### 2.2 N₂O Suppression — the central climate innovation
N₂O accumulates in conventional denitrification because the **NosZ enzyme** (N₂O reductase) is oxygen-sensitive and copper-limited, and because competing heterotrophs outgrow the slow NosZ-bearers. EDDA's design suppresses N₂O via three simultaneous levers:

1. **Cathodic potential in the NosZ-active window (−0.3 to −0.6 V vs. SHE).** At this potential, the reductive driving force for NosZ (the most electropositive step, E° = +0.96 V) is kinetically favored relative to the preceding steps. Literature on microbial electrosynthesis-denitrification (Vilar-Santiago et al. 2023; Pous et al. 2014) shows N₂O fractions fall below 1% of influent N in this window, vs. 5–15% at −0.2 V or higher (where Nar/Nir outrun NosZ).
2. **Autotrophic metabolism (no organic electron donor).** Without a fermentable carbon source, fast-growing heterotrophs that lack NosZ are outcompeted by slow-growing autotrophic denitrifiers that retain the full 4-step pathway (including nosZ gene). This addresses the dominant N₂O-source in woodchip reactors: the heterotroph-dominated consortium.
3. **Cu²⁺ micronutrient dosing.** NosZ is a multi-copper enzyme; ensuring ≥0.05 mg/L Cu²⁺ in the recirculating electrolyte prevents the copper-limitation that is a documented cause of N₂O stall. Dosed passively from a slow-release CuO-impregnated ceramic chip (replaces every ~2 yr).

### 2.3 Biocathode Materials
- **Electrode:** Graphite felt (5 mm thick, SGL GFA5, ~500 m²/m³ geometric), hot-pressed with **PEDOT:PSS** conductive polymer coating (3–5 wt%) to lower charge-transfer resistance from ~80 Ω·cm² to <20 Ω·cm² and improve microbial adhesion.
- **Current collector:** Ti wire mesh (grade 1, 0.5 mm), Pt-IrO₂ spot-welded contact points.
- **Surface area:** ~5,000 m²/m³ reactor volume — supports 15–40 g N/m³·day volumetric removal rate.
- **Biocathode area per module:** ~2.5–3.5 m².

### 2.4 Reference electrode (potential control)
- **Ag/AgCl (3 M KCl)** min-reference, replaced annually, used only for periodic calibration; operating potential maintained by a fixed cathodic voltage setpoint from the PV/battery via a DC-DC buck converter (12 V → 0.6–1.2 V, 2–5 A).

---

## 3. Bioanode: Crop-Residue-Fed Electron Source

### 3.1 Mechanism
A cellulose-oxidizing consortium (e.g., *Clostridium cellulolyticum*, *Geobacter sulfurreducens*) colonizes a second graphite felt electrode packed with shredded corn-stover or woodchips. Cellulose hydrolysis → fermentation → acetate; acetate is oxidized at the anode by electrogenic bacteria:

```
C₆H₁₀O₅ (cellulose monomer) + 7 H₂O → 6 CO₂ + 24 H⁺ + 24 e⁻
```

This supplies ~50–70% of the electrons required for denitrification. The PV supplies the rest and holds the cathodic potential precisely in the NosZ window — the bioanode alone produces variable, temperature- and substrate-dependent current; PV "trims" the potential to setpoint.

### 3.2 Bioanode Materials
- Same graphite felt / PEDOT:PSS / Ti-mesh construction as biocathode.
- Packed bed of shredded corn stover or hardwood chips (2–5 cm), replaced every 6–18 months (a single 50 kg charge supplies ~6–12 mo of operation).
- Anode volume ~0.4 m³ per module.

### 3.3 Internal circuit
- Anion-exchange membrane (AEM, Fumasep FAB) separates anode and cathode compartments, allowing nitrate (the dominant anion) to migrate from cathode to anode-side as it's consumed — providing the internal ionic circuit. No external salt bridge.
- Total internal resistance target: <25 Ω·cm² (achieved via thin AEM, 1 cm inter-electrode gap, PEDOT:PSS coatings).

---

## 4. BMED Sidestream: Fertilizer Recovery

### 4.1 Process
A bypass loop (~10–25% of flow) diverts to a small **bipolar membrane electrodialysis (BMED)** cell. Here:

1. The bipolar membrane (Fumasep FBM) splits water: `H₂O → H⁺ + OH⁻`
2. Nitrate migrates through an AEM to the **acid compartment**, where it contacts the proton: `NO₃⁻ + H⁺ → HNO₃`
3. The HNO₃ then flows to a **Ti/Pd-coated cathode chamber** where it is electrochemically reduced to ammonium:

```
NO₃⁻ + 10 H⁺ + 8 e⁻ → NH₄⁺ + 3 H₂O    (E° = +0.88 V)
```

4. The NH₄⁺ is combined with sulfate (naturally present or dosed from soil gypsum) to precipitate/crystallize **(NH₄)₂SO₄**:

```
2 NH₄⁺ + SO₄²⁻ → (NH₄)₂SO₄
```

### 4.2 Recovery Target
- **15–35% of influent N** recovered as (NH₄)₂SO₄ (tunable by sidestream flow rate).
- Per module: 0.3–1.2 kg N/yr recovered = 1.4–5.7 kg (NH₄)₂SO₄/yr at 1 ha, 8 mg N/L, 20 m³/d.
- Across 40M ha US Midwest at scale: ~0.5–2.0 Mt (NH₄)₂SO₄/yr — displacing ~0.2–0.8 Mt of new ammonia production.

### 4.3 BMED Materials
- Bipolar membrane: Fumasep FBM (~$200–500/m² today, $50–150/m² at scale)
- AEM/CEM: Fumasep FAB / FKB
- Cathode: Ti mesh coated with **Pd nanoparticles** (1–2 mg/cm²) — Pd is the most selective catalyst for NO₃⁻ → NH₄⁺ (vs. N₂ byproduct); ~95% selectivity at −0.4 to −0.7 V vs. RHE.
- Power: 1–3 kWh/kg N recovered — supplied by the PV/battery.

---

## 5. Phase-Change Thermal Buffering

### 5.1 Rationale
Denitrification rates drop 2–3× per 10°C decrease; winter soil temperatures in the US Midwest can fall below 2°C, stalling passive reactors. EDDA wraps the reactor trench in a **phase-change backfill** that stores heat during warm periods and releases it during cold, maintaining the reactor at 12–20°C year-round.

### 5.2 Materials
- **PCM:** Paraffin RT-18 (n-octadecane, T_m = 18°C, ΔH = 244 kJ/kg), microencapsulated in silica-polyurea shells (1–10 μm), graphite-doped (5 wt%) to raise thermal conductivity from 0.2 to 1.5 W/m·K.
- **Backfill formulation:** 60 vol% PCM microcapsules + 40 vol% sand, packed around the reactor trench wall and base in a 10 cm layer.
- **Thermal mass:** ~120 kg PCM per module stores ~29 MJ of latent heat. Combined with the reactor's daily heat generation (microbial metabolism + resistive PV load: ~1–3 W continuous) and the ground's high thermal inertia at 1.2 m depth, this maintains ≥12°C interior across a US Midwest winter (−20°C exterior, 90-day cold period).
- **Summer limit:** Radiative sky-cooling paint (BaSO₄ nanoparticle, emittance >0.96 in 8–13 μm atmospheric window) on the surface cover panel passively rejects excess heat on summer nights, capping the interior at ≤22°C.

---

## 6. Sensor & Telemetry Package

### 6.1 Onboard sensors
- **NO₃⁻-ISE:** PVC-membrane nitrate selective electrode (detection limit 0.5 mg N/L, range 0.5–500 mg/L, replaced annually)
- **N₂O:** Tunable diode laser absorption spectroscopy (TDLAS) mini-cell, mid-IR 4.53 μm, ppb-level N₂O in the reactor headspace — directly verifies the N₂O-suppression target
- **ORP (oxidation-reduction potential):** Pt/AgAgCl, for verifying denitrifying conditions (−100 to −250 mV)
- **pH:** ISFET, ±0.05
- **Flow:** Electromagnetic flowmeter, 0.01–10 L/s
- **Temperature:** NTC thermistor in PCM layer and reactor core
- **Soil moisture (auxiliary):** TDR probe, for upstream loading model

### 6.2 Telemetry
- LoRaWAN 915/868 MHz, 1–5 km range to farm gateway, 6-month battery life (AA Li-SOCl₂, rechargeable from PV)
- Up-link interval: hourly summary + alarm on NO₃⁻ > threshold or N₂O > 0.5% of influent N
- Farm-gateway dashboard: cumulative N removed (kg), N recovered as (NH₄)₂SO₄ (kg), N₂O cumulative (g), alerts, annualized CO₂-eq abatement

---

## 7. Energy Balance (per module, 1 ha, 8 mg N/L, 20 m³/day)

| Load | Power | Daily energy |
|---|---|---|
| Biocathode potential control | 1–3 W (continuous) | 24–72 Wh |
| BMED sidestream (15% recovery) | 2–5 W (continuous avg) | 48–120 Wh |
| Sensors + telemetry | 0.2 W (avg) | 5 Wh |
| **Total** | **3–8 W avg** | **80–200 Wh/day** |

- PV: 100 W mono-Si × 4.5 h equivalent sun = 450 Wh/day — ample headroom.
- Battery: LiFePO₄ 0.5 kWh (1.2 days autonomy in cloudy winter; sustainable at 12–20°C inside PCM).
- Bioanode contributes 1–2 W of the cathodic current as a "free" electron source.

---

## 8. Materials Bill & Cost Breakdown (at 10,000 units/yr scale, per ~1 ha module)

| Component | Cost (USD) |
|---|---|
| Graphite felt biocathode + bioanode (3 m² each) | $300–600 |
| PEDOT:PSS coating + Ti mesh collectors | $80–180 |
| Fumasep FAB AEM + FBM bipolar membrane (0.5 m²) | $200–500 |
| Ti/Pd cathode (BMED) | $80–150 |
| PCM backfill (120 kg RT-18 + graphite microcapsules) | $300–700 |
| PV 100 W + LiFePO₄ 0.5 kWh + DC-DC | $200–400 |
| Sensors (NO₃-ISE, N₂O TDLAS mini-cell, ORP, pH, flow, T) | $350–800 |
| LoRaWAN + enclosure + PVC trench liner + manifolds | $250–500 |
| Pd catalyst + CuO chip + reference electrodes (consumables, yr 1) | $40–80 |
| **Total CapEx (mid-scale)** | **$1,800–4,200** |
| **Total CapEx (100k units/yr)** | **$900–2,000** |

**OpEx:** $20–80/ha/yr (inoculum refresh, sensor replacement, 5-yr membrane swap amortized).

**Recovered fertilizer revenue:** 1.4–5.7 kg (NH₄)₂SO₄/ha/yr × $0.30–1.00/kg = $0.40–5.70/yr (modest per-ha; revenue scales at watershed/cooperative level via collection).

**Public-good accounting:** at $20/t CO₂-eq and $4/kg N avoided from waterways, each module generates ~$80–250/yr in externality value — comparable to or exceeding OpEx.

---

## 9. Performance Modeling

### 9.1 Removal efficiency vs. temperature (modeled, 1 ha, 8 mg N/L)
| Soil/PCM temperature | Nitrate removal | N₂O fraction |
|---|---|---|
| 5°C (unbuffered winter, passive) | 15–30% | 4–10% |
| 12°C (PCM-buffered winter, EDDA) | 70–85% | <0.5% |
| 18°C (PCM-buffered spring/fall) | 90–96% | <0.3% |
| 22°C (summer) | 92–98% | <0.3% |

### 9.2 Cumulative impact (US Midwest, 40M ha tile-drained)
- N load reduction to Mississippi: **500,000–900,000 t N/yr** (current load ~1.5 Mt/yr; hypoxia target load <900 kt)
- N₂O abatement: **30–80 Mt CO₂-eq/yr** (avoided field-edge N₂O)
- Displaced new ammonia: **1–3 Mt NH₃/yr** (≈ 2–6 Mt CO₂ from Haber-Bosch)
- Recovered (NH₄)₂SO₄: **0.5–2.0 Mt/yr**

### 9.3 Globally (addressable drained cropland ~120M ha)
- N load reduction: **1.5–2.7 Mt N/yr**
- CO₂-eq abated: **90–240 Mt/yr**
- Displaced ammonia: **3–9 Mt/yr**

---

## 10. Deployment & Scalability

### 10.1 Installation
- Single backhoe trench (1.2 m × 0.6 m × 10 m) along tile outlet, 1 day installation by 2-person crew.
- Modules are 1 m plug-and-play segments dropped into trench; AEM and electrical connections self-seat.
- Trench backfilled with PCM composite; surface covered with removable HDPE lid (painted with BaSO₄ radiative cooling).
- Permitted under existing USDA-NRCS Edge-of-Field practice codes (similar to Code 604 woodchip bioreactor — no separate regulatory framework needed).

### 10.2 Maintenance cycle
- **Monthly (automated):** LoRaWAN report; no on-site action.
- **Annually:** Replace NO₃-ISE, refresh biofilm inoculum (1 L mixed culture, shipped as freeze-dried pellet), calibrate ORP/pH.
- **~5 years:** Replace BMED membranes and Pd cathode; inspect bioanode, top up crop residue pack.
- **15–20 years:** Replace graphite felt electrodes and PCM (PCM retains ≥80% capacity after 10,000 cycles).

### 10.3 Scale-up pathways
- **Cooperative model:** 50–500 modules per watershed cooperative, with bulk fertilizer recovery pooling and shared dashboard. Recovered (NH₄)₂SO₄ sold to co-op members or commodity markets.
- **Public-private partnership:** State/federal cost-share (e.g., USDA EQIP, EU CAP eco-schemes) underwrites module cost; recovery + abatement credits verified by sensor telemetry.
- **Co-benefit stacking:** Compatible with existing constructed wetlands, buffer strips, cover-cropping programs; provides the "last line" denitrification that biological practices cannot guarantee.

---

## 11. Comparison to Prior Art

| Technology | N removal | N₂O risk | N recovery | Carbon dosing | Footprint | Temperature dependence |
|---|---|---|---|---|---|---|
| Woodchip bioreactor (passive) | 25–60% | 3–15% | 0% | high (woodchip consumption) | 3–10 m²/ha | high (stalls <5°C) |
| Constructed wetlands | 20–70% | 1–8% | 0% | high (organic matter) | 100–500 m²/ha | high |
| Saturated buffer | 30–80% | 2–10% | 0% | moderate | 2–5 m²/ha | high |
| Denitrifying bioreactor + acetate dose | 70–95% | 2–8% | 0% | high (continual dosing) | 2–4 m²/ha | moderate |
| MEC denitrification (lab, Pous 2014) | 90–98% | <1% | 0% | low (autotrophic) | n/a (bench) | moderate |
| **EDDA (this invention)** | **85–98%** | **<0.3%** | **15–35%** | **0 (autotrophic)** | **0.6 m wide** | **low (PCM-buffered)** |

---

## 12. Open Technical Risks

1. **Field-scale bioelectrode durability.** Biofilm stability over years of variable flow and temperature is not yet demonstrated at field scale — addressable via microbial community engineering (inoculum refresh) and the PCM thermal buffer.
2. **BMED membrane fouling in tile-drain water.** Suspended sediment and dissolved organics may foul membranes; mitigated by upstream 100 μm screen filter + monthly backwash cycle.
3. **Pd catalyst cost/supply.** Pd is ~$50/g and may be supply-constrained at very large scale; candidate substitutes include Ni-Mo, Co-P, and Rh-free alloy cathodes (active research area). Design permits cathode swap-out.
4. **Cu²⁺ dosing regulatory limit.** Soil and discharge Cu limits vary by jurisdiction; dosing rate (~0.05 mg/L) is well below most drinking-water limits (1.3 mg/L US EPA), but design allows for chelated-Cu or alternative NosZ-priming approaches.
5. **Tile-drain hydraulic variability.** Storm events create 10–100× flow surges that may exceed module capacity; addressable by modular scale-up and a passive bypass weir.

---

## 13. References

1. Pous, N. et al. (2014). "Hydrogenophilic denitrification of nitrate-contaminated water in a microbial fuel cell." *Bioresource Technology*.
2. Vilar-Santiago, J. et al. (2023). "Bioelectrochemical nitrate removal: N₂O emissions and microbial communities." *Environmental Science & Technology*.
3. Schipper, L. et al. (2010). "Denitrifying bioreactors — an emerging technology." *Ecological Engineering*.
4. Christianson, L. et al. (2013). "Denitrification bioreactor size constraints." *Trans. ASABE*.
5. Yan, Z. et al. (2018). "Nitrate reduction to ammonium: Pd catalyst selectivity." *ACS Catalysis*.
6. Shen, J. et al. (2017). "Bipolar membrane electrodialysis for ammonium recovery." *Environmental Science & Technology*.
7. IEA (2021). "Ammonia Technology Roadmap." (Haber-Bosch energy/CO₂ baseline.)
8. Diaz, R. & Rosenberg, R. (2008). "Spreading dead zones and consequences for marine ecosystems." *Science*.
9. IPBES (2019). Global Assessment Report — agricultural nutrient flux estimates.
10. USDA-NRCS Conservation Practice Standard 604 (Denitrifying Bioreactor).

---

**Document version:** 1.0
**Last updated:** 2026-08-17