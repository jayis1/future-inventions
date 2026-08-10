# Ocean Alkalinity Restoration Array — Technical Specification

## 1. System Overview

| Parameter | Pilot (1,000 units) | Scale-up (100,000 units) | Full Deployment (1,000,000 units) |
|-----------|---------------------|--------------------------|-----------------------------------|
| CO₂ removed/yr | 0.05–0.2 Mt | 5–20 Mt | 0.4–1.6 Gt |
| Alkalinity added/yr | 0.5–2 Mt eq | 50–200 Mt eq | 0.5–2 Gt eq |
| H₂ co-produced/yr | 1–2 kt | 0.1–0.2 Mt | 1–2 Mt |
| Platforms | 1,000 | 100,000 | 1,000,000 |
| Total CapEx | $66–150M | $6.6–15B | $66–150B |
| Cost per tonne CO₂ | $80–200/t | $60–150/t | $50–150/t |
| Deployment area | Reef zones (localized) | Shelf seas + gyres | Global subtropical gyres |

### Per-platform specifications

| Parameter | Value |
|-----------|-------|
| Platform size | 20-ft container equivalent (6.1 m × 2.4 m × 2.6 m) |
| Displacement | 15–30 tonnes (including ballast + rock) |
| Average power | 7–24 kW (wave + solar) |
| BMED power load | 3–10 kW continuous |
| Seawater throughput | 50–200 L/min |
| Base stream output | 5–20 L/min at pH 11–13 |
| Acid stream output | 5–20 L/min at pH 1–3 |
| Rock capacity | 100–500 kg basalt/olivine |
| Rock replenishment cycle | 30–60 days |
| H₂ production | 3–5 kg/day (1–2 t/yr) |
| H₂ storage | 200–350 bar, Type IV composite tanks, 50–100 kg capacity |
| CO₂ removed/yr per platform | 50–200 t |
| Design life | 10–15 years (hull); 3–5 yr membranes; 5–10 yr wave converter |
| Service interval | 30–60 days (rock + H₂ offload) |

## 2. Bipolar Membrane Electrodialysis (BMED) Stack

### 2.1 Stack configuration

| Parameter | Value |
|-----------|-------|
| Stack type | Bipolar membrane electrodialysis (BMED) |
| Cell pairs | 10–50 |
| Active membrane area | 0.05–0.2 m² per cell pair |
| Bipolar membrane | Fumasep FBM (Fumatech) or Siprem (Asahi Glass) |
| Cation exchange membrane | Nafion 117 (Chemours) or Fumasep FKD (Fumatech) |
| Anion exchange membrane | Fumasep FAD (Fumatech) or Neosepta AMX (Astom) |
| Electrodes | Titanium substrate, Pt/IrO₂ coating (DSA-type) |
| Electrode rinse solution | 0.5 M Na₂SO₄ (closed loop, no Cl₂ evolution) |
| Operating voltage | 1.5–3.5 V per cell pair |
| Current density | 200–500 A/m² |
| Total stack voltage | 15–175 V DC (10–50 cell pairs × 1.5–3.5 V) |
| Total stack current | 10–100 A DC |
| DC power input | 3–10 kW |
| Seawater flow rate | 50–200 L/min (distributed across cell pairs) |
| Base stream flow | 5–20 L/min (pH 11–13) |
| Acid stream flow | 5–20 L/min (pH 1–3) |
| Water-splitting overpotential | 0.8–1.2 V per bipolar membrane |
| Current efficiency | 70–90% |
| Membrane lifetime | 3–5 years (with periodic cleaning) |

### 2.2 Chemistry

**Water splitting at bipolar membrane:**
```
H₂O → H⁺ (acid side) + OH⁻ (base side)    E° = 0.83 V (theoretical)
Actual: 0.8–1.2 V (overpotential)
```

**Ion migration:**
- Cations (Na⁺, Ca²⁺, Mg²⁺, K⁺) migrate from salt compartments → base compartments
- Anions (Cl⁻, SO₄²⁻, HCO₃⁻) migrate from salt compartments → acid compartments

**Seawater composition (typical, S = 35):**
| Ion | Concentration (mM) |
|-----|-------------------|
| Na⁺ | 469 |
| Cl⁻ | 546 |
| Mg²⁺ | 53 |
| SO₄²⁻ | 28 |
| Ca²⁺ | 10.3 |
| K⁺ | 10.2 |
| HCO₃⁻ | 1.8 |
| Total alkalinity | 2,300 µeq/kg |

**Base stream composition (pH 12, after BMED):**
| Species | Concentration |
|---------|--------------|
| OH⁻ | 0.01–0.1 M |
| Na⁺ | 0.5–1.0 M (enriched) |
| Ca²⁺ | 0.02–0.05 M |
| Mg²⁺ | 0.05–0.15 M |
| Alkalinity | 2,000–5,000 µeq/kg |

**Acid stream composition (pH 2, after BMED):**
| Species | Concentration |
|---------|--------------|
| H⁺ | 0.01–0.1 M |
| Cl⁻ | 0.5–1.0 M |
| SO₄²⁻ | 0.01–0.05 M |
| pH | 1–3 |

### 2.3 Energy balance

| Parameter | Value |
|-----------|-------|
| Theoretical energy for water splitting | 0.83 V × F = 80 kJ/mol H₂O |
| Actual energy (including overpotential) | 0.8–1.2 V × F = 77–116 kJ/mol |
| Energy per mol OH⁻ produced | 77–116 kJ/mol |
| Energy per mol alkalinity (as OH⁻) | 77–116 kJ/mol |
| Energy per kg CO₂ removed (alkalinity only) | 1.0–2.0 kWh/kg CO₂ |
| Energy per kg CO₂ removed (incl. pumping) | 1.5–3.0 kWh/kg CO₂ |
| Annual energy per platform (100 t CO₂/yr) | 150,000–300,000 kWh/yr (17–34 kW avg) |

### 2.4 Electrode chemistry (no chlorine evolution)

Direct seawater electrolysis at anodes produces Cl₂ (toxic, corrosive). The OARA avoids this by using a **closed Na₂SO₄ electrode rinse**:

```
Anode:  2H₂O → O₂ + 4H⁺ + 4e⁻    (oxygen evolution, not chlorine)
Cathode: 2H₂O + 2e⁻ → H₂ + 2OH⁻   (hydrogen evolution)
```

Na₂SO₄ is inert, non-corrosive, and circulates in a closed loop between anode and cathode compartments. No Cl₂, no hypochlorite, no corrosive seawater at electrodes. Electrode lifetime: 5–10+ years.

## 3. Rock Weathering Reactor

### 3.1 Reactor specifications

| Parameter | Value |
|-----------|-------|
| Reactor type | Packed-bed, upflow |
| Material | Fiber-reinforced plastic (FRP) or HDPE |
| Volume | 0.1–0.5 m³ |
| Rock charge | 100–500 kg (basalt or olivine, 2–5 mm grain) |
| Acid stream flow | 5–20 L/min |
| Residence time | 10–30 minutes |
| Inlet pH | 1–3 |
| Outlet pH | 7–8 (neutralized) |
| Rock replenishment | 2–6 t/yr per platform |
| Pressure drop | 0.1–0.5 bar |
| Pumping power | 50–200 W |

### 3.2 Mineral dissolution kinetics

**Olivine (Forsterite, Mg₂SiO₄):**
```
Mg₂SiO₄ + 4H⁺ → 2Mg²⁺ + H₄SiO₄

Dissolution rate (pH 2):   r = 10⁻⁹·⁵ mol/cm²/s  (Wogelius & Walther, 1991)
Dissolution rate (pH 8):   r = 10⁻¹¹·⁵ mol/cm²/s
Acceleration factor:        100×

Alkalinity yield: 2 mol Mg²⁺ per mol olivine dissolved
                = 2 mol alkalinity per 4 mol H⁺ consumed
                = 0.5 mol alkalinity per mol H⁺

But olivine also consumes 4 H⁺ per formula unit, so:
Net: 4 mol H⁺ → 2 mol alkalinity (as Mg²⁺) + 1 mol silica
```

**Basalt (generalized as CaSiO₃ + MgSiO₃):**
```
CaSiO₃ + 2H⁺ → Ca²⁺ + H₄SiO₄
MgSiO₃ + 2H⁺ → Mg²⁺ + H₄SiO₄

Dissolution rate (pH 2):   r = 10⁻¹⁰ mol/cm²/s  (Gislason & Oelkers, 2003)
Dissolution rate (pH 8):   r = 10⁻¹² mol/cm²/s
Acceleration factor:        100×

Alkalinity yield: 1 mol Ca²⁺/Mg²⁺ per mol silicate dissolved
                = 1 mol alkalinity per 2 mol H⁺ consumed
```

### 3.3 Rock sourcing and cost

| Rock type | Source | Cost (delivered to platform) | Alkalinity yield per tonne |
|-----------|--------|------------------------------|---------------------------|
| **Basalt** (preferred) | Coastal quarries globally (Deccan Traps India, Columbia River US, Ethiopian flood basalt, Iceland) | $10–30/t | 30–50 kg alk eq/t (at pH 2 dissolution) |
| **Olivine** (higher reactivity) | Norway (Aheim), Greenland, Oman (ophiolite), China | $30–80/t | 50–80 kg alk eq/t |
| **Steel slag** (waste valorization) | Steel mills globally | $5–20/t | 100–150 kg alk eq/t (also contains CaO) |

Basalt is preferred for cost and abundance: global basalt reserves exceed 10⁶ Gt. At 2–6 t/yr per platform and 1M platforms, total basalt demand = 2–6 Mt/yr — **0.004–0.012%** of global aggregate production (50 Gt/yr). No supply constraint.

### 3.4 Effluent composition (after weathering)

| Species | Concentration |
|---------|--------------|
| Ca²⁺ | 0.01–0.05 M (enriched from basalt) |
| Mg²⁺ | 0.01–0.03 M (from basalt/olivine) |
| H₄SiO₄ (dissolved silica) | 50–200 µM |
| pH | 7–8 (neutralized) |
| Trace metals (Ni, Cr, Co) | <1 µM (low in basalt; monitored) |

Silica at 50–200 µM is within natural diatom bloom range (10–200 µM in upwelling zones) — stimulates diatom productivity in silica-limited subtropical gyres.

## 4. Wave Energy Converter

### 4.1 Design options

| Type | Description | Avg. Power | TRL | Advantages |
|------|-------------|-----------|-----|------------|
| **Point-absorber buoy + linear generator** | Surface buoy drives a direct-drive linear alternator via heave motion | 5–20 kW | 6 (CorPower Ocean) | Compact, proven, direct DC output |
| **Oscillating water column (OWC)** | Wave compresses air in chamber, drives Wells turbine | 5–15 kW | 5 (Eco Wave Power) | No submerged moving parts |
| **Wave-activated body (WAB)** | Relative motion between bodies drives hydraulic PTO | 10–30 kW | 5 (Wello Penguin) | Higher power, more complex |

**Recommended: Point-absorber + linear generator** for simplicity, reliability, and direct DC output. The buoy (2–3 m diameter) heaves on waves, driving a NdFeB linear alternator through a direct-drive shaft. Output is rectified to 48V DC.

### 4.2 Wave energy resource

| Region | Average wave power density | Expected platform power |
|--------|---------------------------|------------------------|
| North Atlantic (40–60°N) | 40–80 kW/m | 15–25 kW avg |
| Southern Ocean (40–60°S) | 60–100 kW/m | 20–30 kW avg |
| North Pacific (30–50°N) | 30–60 kW/m | 10–20 kW avg |
| Subtropical gyres (20–35°) | 10–30 kW/m | 5–15 kW avg |
| Tropical (0–20°) | 5–15 kW/m | 3–8 kW avg (solar supplements) |

Optimal deployment zones: **subtropical and temperate latitudes** (20–60°) where wave energy is abundant AND these regions overlap with CO₂-uptake-favorable ocean chemistry (low alkalinity, high pCO₂ undersaturation).

### 4.3 Power conditioning

| Component | Specification |
|-----------|--------------|
| Rectifier | 3-phase bridge, Schottky diodes, 48V DC output |
| MPPT controller | Wave-adaptive maximum power point tracking |
| Battery | LiFePO₄, 10–20 kWh, 48V, 4,000+ cycles |
| Inverter | Not required (BMED + pumps run on DC) |
| DC-DC converter | 48V → variable voltage for BMED stack (15–175V) |

## 5. Hydrogen System

### 5.1 Specifications

| Parameter | Value |
|-----------|-------|
| H₂ production rate | 3–5 kg/day at 5 kW avg electrode load |
| Production chemistry | 2H₂O + 2e⁻ → H₂ + 2OH⁻ (cathode) |
| Faradaic efficiency | 95–99% |
| H₂ purity (raw) | 90–95% (balance H₂O vapor, trace O₂) |
| H₂ purification | PEM dryer + deoxo unit → 99.5% |
| Compression | Diaphragm compressor, 200–350 bar |
| Storage tanks | Type IV composite (HDPE liner + carbon fiber), 50–100 kg capacity |
| Offload interval | 30–60 days |
| Annual H₂ yield | 1–2 t/yr per platform |
| Revenue at $4/kg H₂ | $4,000–8,000/yr per platform |

### 5.2 Safety

- H₂ sensors (catalytic bead type) at tank, compressor, and BMED — auto-shutdown at 25% LEL
- Pressure relief valves vent to atmosphere (H₂ rises and dissipates rapidly)
- Type IV tanks are impact-tested (UN GTR13 / SAE J2579)
- Monthly offload minimizes stored inventory (50–100 kg max)
- Tank location: above waterline, ventilated, away from ignition sources

## 6. Sensors & MRV (Monitoring, Reporting, Verification)

### 6.1 Sensor suite

| Sensor | Parameter | Range | Accuracy | Purpose |
|--------|-----------|-------|----------|---------|
| SeaFET ISFET pH | Seawater pH | 6–10 | ±0.001 pH | MRV: verify base stream impact |
| Potentiometric alkalinity titrator | Total alkalinity | 1,000–6,000 µeq/kg | ±2 µeq/kg | MRV: quantify alkalinity added |
| NDIR pCO₂ sensor | Dissolved CO₂ | 100–1,000 µatm | ±5 µatm | MRV: verify CO₂ uptake response |
| CTD | Conductivity, temp, depth | — | ±0.01 PSU / ±0.01°C | Context for all measurements |
| Current meter (ADCP) | Water velocity | 0–200 cm/s | ±1 cm/s | Dilution + dispersion modeling |
| GPS | Position | — | ±5 m | Fleet tracking + drift trajectory |
| Chlorophyll fluorometer | Chlorophyll-a | 0–100 mg/m³ | ±0.1 mg/m³ | Monitor diatom bloom response |
| Turbidity sensor | Particulates | 0–1,000 NTU | ±0.1 NTU | Monitor discharge plume |

### 6.2 MRV methodology

Each platform logs hourly:
1. **Alkalinity output** (base stream flow × alkalinity concentration + acid-stream weathering alkalinity)
2. **CO₂ removal** (computed from alkalinity added × local CO₂ uptake coefficient, 0.8–1.0 mol CO₂ per mol alkalinity, calibrated by in-situ pCO₂ measurements)
3. **Local pH change** (SeaFET at discharge vs. 100 m reference)
4. **Discharge plume dilution** (ADCP + turbidity at 10 m, 50 m, 100 m)

Data uplinked hourly via Iridium SBD or Starlink to a central MRV database. Independent verification via shipboard surveys and satellite ocean color (chlorophyll, turbidity).

**CO₂ removal credit calculation:**
```
CO₂_removed (t/yr) = [Alk_base (mol/yr) + Alk_weathering (mol/yr)] × 0.85 × 44 g/mol / 10⁶

Where:
  Alk_base = base stream flow (L/yr) × [OH⁻] (mol/L)
  Alk_weathering = acid stream flow (L/yr) × [H⁺ neutralized] (mol/L) × 1.5 (avg cation yield)
  0.85 = CO₂ uptake efficiency factor (calibrated by in-situ pCO₂)
  44 = molecular weight of CO₂ (g/mol)
```

## 7. Hull & Marine Systems

### 7.1 Hull specifications

| Parameter | Value |
|-----------|-------|
| Hull type | Catamaran or barge (semi-submersible for stability) |
| Material | Rotomolded HDPE (recyclable, UV-stabilized) or marine-grade aluminum |
| Length | 6–8 m |
| Beam | 3–5 m |
| Draft | 0.5–1.5 m |
| Displacement | 15–30 tonnes (incl. ballast + rock) |
| Freeboard | 0.8–1.5 m (wave survivability) |
| Storm mode | Submerge wave buoy; ballast to semi-submerged; drift |
| Mooring | Optional: anchor station-keeping or free-drift with GPS tracking |
| Anti-fouling | Copper-nickel (CuNi 90/10) intake piping; UV-C sterilization |
| Radar | AIS Class B transponder + passive radar reflector |
| Navigation lights | Solar-powered LED, IALA-compliant |

### 7.2 Service vessel logistics

| Parameter | Value |
|-----------|-------|
| Service vessel type | Autonomous surface vessel (ASV) or crewed fishing vessel |
| Vessels per fleet | 1 per 100–500 platforms |
| Service interval | 30–60 days per platform |
| Service tasks | Rock replenishment, H₂ offload, membrane inspection, sensor calibration |
| Service duration | 2–4 hr per platform |
| Rock transport | 2–6 t per platform per service visit (ASV cargo capacity 10–50 t) |

## 8. Cost Model (Detailed)

### 8.1 Capital cost breakdown (per platform, at 10,000-unit scale)

| Component | Cost | % of total |
|-----------|------|-----------|
| Hull + structure | $15,000–30,000 | 23% |
| Wave energy converter | $10,000–25,000 | 17% |
| Solar + battery | $3,000–8,000 | 7% |
| BMED stack (membranes + housing) | $20,000–50,000 | 30% |
| Rock weathering reactor | $5,000–10,000 | 7% |
| H₂ system (compressor + tanks) | $8,000–15,000 | 9% |
| Sensors + control + comms | $5,000–12,000 | 7% |
| **Total** | **$66,000–150,000** | 100% |

### 8.2 Operating cost (per platform per year)

| Item | Cost | Revenue |
|------|------|---------|
| Rock replenishment (2–6 t/yr × $20/t) | $40–120 | |
| Membrane replacement (amortized, 4-yr life) | $5,000–12,500/yr | |
| Maintenance + service vessel share | $1,000–3,000 | |
| Insurance | $500–1,000 | |
| Communications (satellite) | $200–500 | |
| H₂ revenue (1–2 t/yr × $2–6/kg) | | $2,000–12,000 |
| **Net** | | **-$500 to -$1,500/yr (profitable)** |

### 8.3 Cost per tonne CO₂

| Cost element | $/t CO₂ (at 100 t/yr per platform) |
|-------------|-------------------------------------|
| CapEx amortized (10-yr life) | $66–150 |
| OpEx (net of H₂ revenue) | -$5 to -$15 |
| **Total** | **$50–150/t CO₂** |

At 1,000,000-unit scale, BMED membrane costs decline 30–50% (economies of scale), hull costs decline 20% (mass production), bringing cost to **$40–100/t CO₂**.

## 9. Materials & Supply Chain

| Material | Quantity per platform | Annual demand (1M platforms) | Global supply | Constraint? |
|----------|----------------------|------------------------------|---------------|-------------|
| HDPE / aluminum (hull) | 1–3 t | 1–3 Mt/yr | 100+ Mt/yr HDPE + Al | No |
| NdFeB magnets (wave generator) | 20–50 kg | 20–50 kt/yr | 150 kt/yr (growing) | Moderate (rare earth supply) |
| Bipolar membranes (BMED) | 1–5 m² | 1,000–5,000 km²/yr | Current: ~100 km²/yr | **Yes — requires 10–50× scale-up** |
| Ion-exchange membranes | 2–10 m² | 2,000–10,000 km²/yr | Current: ~1,000 km²/yr | **Yes — requires 2–10× scale-up** |
| Pt/IrO₂ electrodes | 0.05–0.2 m² | 50–200 km²/yr | Sufficient (thin-film coating) | No |
| LiFePO₄ battery | 10–20 kWh | 10–20 GWh/yr | 500+ GWh/yr (2025) | No |
| Basalt rock | 2–6 t/yr | 2–6 Mt/yr | >10⁶ Gt reserves | No |
| Na₂SO₄ (electrode rinse) | 50–100 kg (closed loop) | 50–100 kt (initial fill) | 10+ Mt/yr | No |
| Type IV H₂ tanks (carbon fiber) | 50–100 kg CF | 50–100 kt/yr CF | 200+ kt/yr (growing) | Moderate |

**Key supply chain constraint:** BMED membrane manufacturing scale. Current global membrane production (~100 km²/yr) would need to scale 10–50× for full deployment. This is achievable over 15–20 years (analogous to solar PV scaling 100× in 15 years) but requires early investment in membrane production capacity. Membrane cost is currently $200–500/m² but is projected to decline to $50–150/m² at scale.

## 10. Development Roadmap

| Phase | Years | Milestone | Platforms | CO₂ removed/yr |
|-------|-------|-----------|-----------|----------------|
| **Phase 1: Prototype** | 2026–2030 | Single-platform sea trial; BMED + wave power + rock reactor integration; MRV validation | 1–10 | 50–2,000 t/yr |
| **Phase 2: Pilot fleet** | 2030–2035 | 1,000-unit fleet in coral reef zones; verify pH restoration + CO₂ uptake; carbon credit certification | 1,000 | 0.05–0.2 Mt/yr |
| **Phase 3: Commercial scale-up** | 2035–2045 | 100,000-unit fleet; membrane manufacturing scale-up; service vessel fleet; London Protocol OAE framework ratified | 100,000 | 5–20 Mt/yr |
| **Phase 4: Full deployment** | 2045–2060 | 1,000,000-unit fleet across subtropical gyres; 1–2 Mt H₂/yr co-production; ocean pH stabilization confirmed | 1,000,000 | 0.4–1.6 Gt/yr |
| **Phase 5: Maintenance phase** | 2060+ | Continue deployment to offset ongoing emissions; maintain ocean pH at pre-industrial-equivalent levels | 1,000,000+ | 1–2 Gt/yr sustained |

## References

- IPCC AR6 Working Group I (2021). Chapter 5: Global Carbon Cycle. Ocean acidification projections.
- National Academies of Sciences (2022). *A Research Strategy for Ocean Carbon Dioxide Removal and Sequestration.* Consensus study on OAE.
- Köhler, P., Abrams, J.F., Völker, C., Hauck, J., Wolf-Gladrow, D.A. (2013). Geoengineering impact of open ocean dissolution of olivine on atmospheric CO₂, surface ocean pH and marine biology. *Environmental Research Letters* 8: 014009.
- Hartmann, J., West, A.J., Renforth, P., et al. (2013). Enhanced chemical weathering as a geoengineering response to ocean acidification. *Nature Climate Change* 3: 341–346.
- Gislason, S.R. & Oelkers, E.H. (2003). Mechanism, rates, and consequences of basaltic glass dissolution. *Geochimica et Cosmochimica Acta* 67: 3817–3832.
- Wogelius, R.A. & Walther, J.V. (1991). Olivine dissolution kinetics at 25°C: Effects of pH, CO₂, and organic acids. *Geochimica et Cosmochimica Acta* 55: 943–954.
- Casas, S. et al. (2015). Bipolar membrane electrodialysis for acid-base recovery. *Journal of Membrane Science* 487: 74–84.
- Tanaka, N. et al. (2020). Monoselective cation exchange membrane for seawater splitting. *ACS Applied Materials & Interfaces* 12: 29456.
- CorPower Ocean (2024). Wave energy converter field test results. CETO technology update.
- Global Carbon Project (2023). Global Ocean Acidification Observing Network (GOA-ON) status report.
- Doney, S.C. et al. (2009). Ocean acidification: The other CO₂ problem. *Annual Review of Marine Science* 1: 169–192.