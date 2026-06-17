# CCAP — Technical Specification

## 1. System Architecture

### 1.1 Platform Overview

The Coral Calcification Acceleration Platform (CCAP) is a 4 × 4 m autonomous floating unit with the following major subsystems:

| Subsystem | Mass (kg) | Power (W avg) | Function |
|-----------|----------|---------------|----------|
| BMED Stack + Plumbing | 180 | 800–1,200 | Alkalinity generation |
| Solar Array (2.4 kWp) | 45 | — | Primary energy |
| Battery Bank (20 kWh LFP) | 140 | — | Energy storage (night/overcast) |
| Probiotic Bioreactor | 85 | 150 | Consortium culture + dosing |
| Lattice Nursery Module | 60 | 50 | Settlement module conditioning |
| Olivine Cartridge Bay | 50 | 10 | Acid neutralization feed |
| Control + Comms | 15 | 30 | Autonomy, mesh networking |
| Hull + Mooring | 200 | — | Flotation, station-keeping |
| **Total** | **775** | **1,040–1,440** | |

### 1.2 Operational Modes

| Mode | Power (W) | Duration | Description |
|------|-----------|----------|-------------|
| Full Alkalinity | 1,200 | 6–8 h/day (daylight) | BMED at full capacity, bioreactor active |
| Probiotic-Only | 200 | 16–18 h/day (night) | BMED off, bioreactor dosing continues |
| Lattice Deploy | 150 | 2 h/event | Deploy and position settlement modules |
| Storm Safe | 50 | Continuous | All systems low-power, unit submerges to 2 m |
| Maintenance | 0 | Quarterly | Olivine cartridge swap, lattice restock |

---

## 2. BMED Alkalinity Enhancement System

### 2.1 Electrochemistry

**Cell Configuration**: 5-cell bipolar membrane electrodialysis stack

| Parameter | Value |
|-----------|-------|
| Active area per cell | 0.2 m² |
| Cell pair voltage | 1.8–2.4 V |
| Current density | 50–100 mA/cm² |
| Current efficiency | ≥85% |
| OH⁻ production rate | 0.8–1.5 mol/hr (per unit) |
| Seawater feed rate | 2–4 L/min |
| Alkaline stream pH | 9.5–10.5 (vs. 8.1 ambient) |
| Acid stream pH | 2.5–3.5 |
| Energy consumption | 3–5 kWh/kg OH⁻ |
| Membrane lifetime | 3–5 years (bipolar: Fumasep FBM, cation: Nafion 117) |

### 2.2 Alkalinity Dosing Strategy

The alkaline stream is discharged through a **perimeter diffuser ring** (24 nozzles, 360° distribution at 1–2 m depth) surrounding the CCAP unit. Dosage is calculated by onboard sensors and mesh-coordinated with neighboring units:

- **Target Ω_aragonite**: 4.5 (pre-industrial equivalent) in a 0.5–1 ha zone
- **Maximum ΔpH**: +0.3 units above ambient (to avoid local hyper-alkalinity)
- **Mixing model**: Lagrangian particle dispersion model (ROMS-based) runs on edge compute to predict alkalinity plume behavior
- **Coordination**: Acoustic mesh (2–10 kHz, 500 m range) shares dosing plans across fleet; only 60% of units dose simultaneously to prevent over-concentration

### 2.3 Olivine Acid Neutralization

| Parameter | Value |
|-----------|-------|
| Olivine composition | Mg₁.₈Fe₀.₂SiO₄ (dunite grade, 90%+ olivine) |
| Particle size | 10–50 µm (ball-milled) |
| Cartridge capacity | 50 kg |
| Cartridges per unit | 4 (200 kg total) |
| Replacement interval | 3 months |
| Acid neutralization rate | 1.1 t CO₂ captured per tonne olivine dissolved |
| Dissolution reactor | 20 L packed bed, acid stream recirculated through olivine bed at pH 3–4 |
| Effluent pH | 7.5–8.0 (safe for discharge) |
| Byproducts | Mg²⁺ (0.7 kg/day), H₄SiO₄ (0.9 kg/day) — both beneficial to reef biota |

---

## 3. Probiotic System

### 3.1 Consortium Composition

| Strain | Origin | Function | Concentration |
|--------|--------|----------|---------------|
| *Endozoicomonas* sp. RS-7 | Red Sea *Stylophora pistillata* | Antioxidant production (squalene, MAA); reduces ROS by 45–60% under +2°C thermal stress | 5 × 10⁷ CFU/mL |
| *Endozoicomonas* sp. PG-3 | Persian Gulf *Platygyra daedalea* | Nitrogen fixation; produces B₁₂ and thiamine for host nutrition | 3 × 10⁷ CFU/mL |
| *Pseudoalteromonas* sp. AC-12 | Engineered from *P. luteoviolacea* | Anti-*Vibrio* bacteriocin (pseudoalterin); colonizes mucus layer, excludes pathogens | 2 × 10⁷ CFU/mL |
| *Roseobacter* sp. RB-4 | Tropical *Acropora* mucus | DMSP cleavage → dimethyl sulfide (DMS); promotes coral Symbiodiniaceae health; UV protection via scytonemin | 1 × 10⁷ CFU/mL |

### 3.2 Bioreactor Design

- **Type**: Continuous-flow, multi-chamber photobioreactor
- **Volume**: 4 × 5 L chambers (one per strain) + 20 L mixing/settling tank
- **Lighting**: 410–460 nm blue LED (2 × 20 W per chamber) + 660 nm red LED (1 × 10 W per chamber)
- **Temperature**: 26–28°C (thermostatted)
- **Medium**: Artificial seawater + defined organic carbon (glucose 5 mM + acetate 2 mM + amino acid mix 1 mM)
- **Productivity**: 10⁸ CFU/mL at steady state; 20–50 L/day output
- **Sterility**: 0.2 µm inline filter on dosing line; UV-C purge cycle weekly

### 3.3 Dosing Protocol

- **Method**: Peristaltic pump dosing through 4-nozzle submerged manifold at 1.5 m depth
- **Rate**: 10–50 L/day (adjustable based on reef health sensor data)
- **Timing**: Continuous, with peak dosing during thermal stress events (SST > +1°C above MMM)
- **Colony persistence**: Probiotic strains persist in coral mucus for 7–21 days; weekly re-dosing recommended
- **Monitoring**: qPCR of water samples for strain-specific 16S markers; automated on-board MiniION sequencing weekly

---

## 4. Settlement Lattice System

### 4.1 Lattice Specifications

| Parameter | Value |
|-----------|-------|
| Dimensions | 30 × 30 × 10 cm |
| Mass | 2.5 kg |
| Material | 70% CaCO₃ (recycled shellfish waste), 20% Mg-calcite binder, 5% aragonite nucleation seeds, 5% slow-release pheromone microcapsules |
| Porosity | 90–95% |
| Internal surface area | 0.8 m² per module |
| Topology | Gyroid (triply periodic minimal surface), CFD-optimized |
| Pore size | 200–500 µm (crevice spacing) |
| Flow regime target | Re = 50–200 at 2–5 cm/s ambient current |
| Settlement density (lab) | 120–250 recruits/m² (vs. 30–50 on natural substrate) |

### 4.2 Bio-Printing Process

1. **Shellfish waste processing**: Oyster/crab shells cleaned, calcined at 900°C, ball-milled to 5–20 µm CaCO₃ powder
2. **Mg-calcite binder**: Synthesized by co-precipitation of CaCO₃ + MgCO₃ (15 mol% Mg) — mimics natural CCA mineralogy
3. **Ink formulation**: 65 wt% CaCO₃ powder + 20 wt% Mg-calcite binder + 5 wt% aragonite seeds + 5 wt% 5-deoxystrigol microcapsules (PLGA, 6-month release) + 5 wt% sodium alginate (binder)
4. **Printing**: Robocasting (extrusion-based 3D printing) at 25°C, 0.4 mm nozzle, 15 mm/s print speed
5. **Curing**: Immersion in 0.5 M CaCl₂ solution for 24 h (ionically crosslinks alginate, strengthens structure)
6. **CCA conditioning**: Submerge in CCA (*Porolithon onkodes*) culture tank for 14 days → biofilm formation
7. **Deployment readiness**: Store in seawater at 25°C; deploy within 30 days of conditioning

### 4.3 Deployment Protocol

- **Method**: Mechanical arm from CCAP unit places modules on reef substrate at GPS-designated positions
- **Depth**: 2–15 m (optimal coral recruitment zone)
- **Spacing**: 1 module per 4 m² (250 modules per hectare)
- **Deployment rate**: 10–15 modules/day per unit
- **Monitoring**: Underwater camera (2 MP, IR for night) on each module inspects settlement weekly; image analysis via onboard Jetson Orin Nano

---

## 5. Sensors & Control

### 5.1 Sensor Suite

| Sensor | Parameter | Range | Accuracy | Frequency |
|--------|-----------|-------|----------|-----------|
| SeapHOx pH | Seawater pH | 6.5–9.0 | ±0.01 | Continuous |
| SeaFET pCO₂ | Dissolved CO₂ | 100–2000 µatm | ±5 µatm | Continuous |
| CTD | Conductivity, temperature, depth | -2–35°C, 0–70 mS/cm | ±0.001°C, ±0.01 mS/cm | Continuous |
| PAR sensor | Photosynthetically active radiation | 0–3000 µmol/m²/s | ±5% | Continuous |
| Dissolved O₂ | Oxygen concentration | 0–14 mg/L | ±0.1 mg/L | Continuous |
| Fluorometer | Chlorophyll-a + phycocyanin | 0–500 µg/L | ±0.1 µg/L | Hourly |
| Underwater camera | Visual monitoring | 2 MP, 4608×2592 | — | Weekly + on-demand |
| Hydrophone | Acoustic modem + bio-acoustics | 2–20 kHz | — | Continuous |
| MiniION | Microbiome sequencing | 16S rRNA | Species-level | Weekly |

### 5.2 Autonomous Control

- **Processor**: NVIDIA Jetson Orin Nano (40 TOPS AI performance)
- **Software stack**: ROS 2 + custom reef-health ML model (PhytoplanktonNet-derived, AUC > 0.88 for bleaching detection)
- **Decision engine**: Rule-based + ML hybrid; adjusts alkalinity dosing, probiotic rate, and lattice deployment based on sensor data
- **Communication**: Acoustic mesh (2–10 kHz, 500 m range, 100 bps), Iridium SBD satellite backup, BLE for diver/maintenance interface
- **Fleet coordination**: Distributed consensus algorithm; no single point of failure; mesh self-heals on unit loss

---

## 6. Power System

| Component | Specification |
|-----------|--------------|
| Solar array | 2.4 kWp bifacial HJT panels, 22% efficiency, salt-water resistant coating |
| Battery | 20 kWh LFP (LiFePO₄), 6000+ cycle life, marine-grade |
| Daily energy budget | 12 kWh (day) + 4 kWh (night BMED off) = ~16 kWh |
| Peak load | 1.2 kW (BMED full power) |
| Storm survival | Unit submerges to 2 m depth via ballast tanks; solar panels fold flat |

---

## 7. Environmental Safety

### 7.1 Alkalinity Monitoring & Limits

- **Maximum local pH change**: +0.3 units above ambient (WHO marine water quality guideline)
- **Overshoot protection**: If pH > 8.7 in the dosing zone, BMED automatically throttles to 50% and alerts fleet
- **Diffusion modeling**: ROMS-based real-time plume model ensures alkalinity is distributed, not concentrated
- **Buffer chemistry**: Seawater carbonate buffer system naturally distributes OH⁻; local effect dissipates within 50–100 m of diffuser

### 7.2 Probiotic Biosafety

- All strains derived from natural coral-associated bacteria (not synthetic organisms)
- Engineered strains use **biological containment**: auxotrophic dependencies on D-alanine and diaminopimelic acid (not found in seawater); strains die within 48–72 hours without probiotic dosing
- Horizontal gene transfer mitigation: engineered traits on mini-chromosomes with toxin-antitoxin kill switches
- No antibiotic resistance markers; all selection via nutritional auxotrophy
- Regulatory pathway: EPA TSCA review + local marine authority permitting before deployment

### 7.3 Lattice Materials Safety

- CaCO₃ and Mg-calcite are natural seawater minerals; no leaching concern
- 5-deoxystrigol analog is a naturally occurring strigolactone; degrades in seawater with half-life ~14 days
- PLGA microcapsule degradation products (lactic acid, glycolic acid) are naturally occurring; total pheromone load per hectare < 1 g/year

---

## 8. Manufacturing & Supply Chain

### 8.1 Bill of Materials (per unit, at 10,000 units/year scale)

| Component | Source | Cost |
|-----------|--------|------|
| BMED stack (5-cell) | Fumatech membranes + Ti/Pt electrodes | $1,200 |
| Solar array (2.4 kWp HJT) | Standard marine-grade PV | $800 |
| LFP battery (20 kWh) | CATL or equivalent | $1,800* |
| Probiotic bioreactor | Custom: borosilicate + 316 SS | $1,200 |
| Lattice printer (robocaster) | Custom: 3-axis gantry + feed system | $800 |
| Olivine cartridge system | HDPE tanks + peristaltic pump | $300 |
| Control electronics + Jetson Orin | COTS + custom PCB | $500 |
| Acoustic modem + Iridium SBD | COTS | $300 |
| Sensors (pH, pCO₂, CTD, PAR, O₂, fluorometer) | Sea-Bird / Pro-Oceanus / custom | $600 |
| Underwater camera (2 MP) | COTS + housing | $200 |
| Hull (rotomolded HDPE) + mooring | Custom fabrication | $800 |
| Diffuser ring + plumbing | PVC/HDPE custom | $200 |
| Probiotic seed culture (quarterly) | Lab-supplied | $100/yr |
| Olivine cartridges (4/year) | Mined in Norway/Australia | $400/yr |
| Lattice feedstock (shellfish CaCO₃) | Waste stream (restaurants/aquaculture) | $100/yr |
| **Total per unit** | | **$9,100** |
| **Per ha per year (5-year amortization)** | | **$455–610** |

*Battery cost projected at $90/kWh by 2028; current LFP at $140/kWh.

### 8.2 Scalability Path

| Phase | Year | Units | Key Milestone |
|-------|------|-------|---------------|
| Lab | 2027 | 0 | BMED + probiotic + lattice integration in tanks |
| Pilot | 2029 | 10 | 1-hectare reef trial (Great Barrier Reef or Maldives) |
| Scale-1 | 2032 | 500 | 50-hectare restoration, multi-unit coordination demonstrated |
| Scale-2 | 2035 | 10,000 | Manufacturing automation, $300/ha/year achieved |
| Global | 2040 | 500,000 | Major reef systems (GBR, Caribbean, Coral Triangle) under treatment |
| Full Coverage | 2045 | 2,000,000 | All degraded reef area under active restoration |

---

## 9. Key Performance Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| Local Ω_aragonite increase | +0.5 to +1.5 units | SeapHOx pH + alkalinity titration |
| Bleaching resistance improvement | 30–50% under +1–2°C SST anomaly | Coral color score (CoralWatch) + Symbiodiniaceae density |
| Larval settlement rate | 3–5× natural substrate | Recruit counts per m² on lattice vs. control |
| Probiotic colonization rate | >80% of corals within 48 hrs | qPCR of mucus samples |
| Olvine dissolution efficiency | >70% within 3 months | Mg²⁺ release tracking |
| Fleet uptime | >95% | Remote monitoring dashboard |
| Energy self-sufficiency | 100% solar (no grid/diesel) | Power budget tracking |
| Carbon capture (olivine) | 1.1 t CO₂ / t olivine | Mass balance on Mg²⁺ + SiO₄⁴⁻ release |