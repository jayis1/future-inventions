# Technical Specification — Autonomous Kelp Forest Cultivator (AKFC)

## 1. System Architecture

### 1.1 Submersible Cultivator Unit (SCU)

| Parameter | Specification |
|-----------|---------------|
| Length | 1.8 m |
| Beam | 0.6 m |
| Dry mass | 85 kg |
| Operating depth | 2–40 m (kelp photic zone) |
| Speed | 0.5–1.5 m/s cruise; 2.0 m/s burst |
| Endurance | 12 hours submerged per charge |
| Propulsion | 4× vectored rim-driven thrusters (magnetic coupling, no shaft seals) |
| Power | 2.5 kWh LiFePO₄ battery pack; inductive charging from mothership |
| Navigation | INS + DVL + acoustic ranging + forward-looking sonar |
| Mapping | 360° multibeam echosounder + stereo cameras + hyperspectral imager (400–1000 nm) |
| Manipulator | 6-DOF soft pneumatic arm, 1.2 m reach, 5 kg payload |
| Nursery capacity | 2,000 sporophytes in rotating bioreactor drum |
| Deployment rate | 200 sporophytes/hour |
| Communications | Acoustic modem (9–14 kHz, 100 bps, 2 km range); Wi-Fi surfaced |
| Biofouling resistance | Ultrasonic hull cleaning + copper-nickel alloy skin (70/30 CuNi) |
| Buoyancy | Variable ballast (seawater/pump); +0.5 N neutral reserve |

### 1.2 Surface Mothership Platform (SMP)

| Parameter | Specification |
|-----------|---------------|
| Length | 6 m catamaran |
| Power | 800 W flexible solar + 400 W wave energy converter (oscillating water column) |
| Battery | 20 kWh LiFePO₄ |
| SCU charging | 4× inductive charge pads (simultaneous), 2-hour full recharge |
| Satellite uplink | Starlink Mini / Iridium Certus (position, health, data relay) |
| Sporophyte resupply | Via autonomous tender vessel from shore (weekly) |
| Processing | Edge AI (Intel Loihi 2 neuromorphic chip, 128 cores, 5 mW/MAC) |
| Endurance | 90+ days unattended |

## 2. Nursery Bioreactor Subsystem

### 2.1 Kelp Sporophyte Production Pipeline

**Species supported (primary):**
- *Macrocystis pyrifera* (Giant Kelp) — Pacific, up to 60 m
- *Laminaria digitata* — Atlantic
- *Saccharina latissima* (Sugar Kelp) — Atlantic/Arctic, aquaculture-proven
- *Ecklonia maxima* — South Africa, Indian Ocean

**Growth stages:**

| Stage | Duration | Conditions | Output |
|-------|----------|------------|--------|
| Zoospore release | 0–12 hrs | 10°C, dark, 1 L/min flow | 10⁶ zoospores/L |
| Gametophyte culture | 12–20 days | 15°C, 20–50 µmol/m²/s red+blue LED, sterile seawater + nitrate/phosphate enrichment | Female + male gametophytes |
| Fertilization | Day 20–21 | Mix male/female, 10°C, reduced light | Zygotes form |
| Sporophyte growth | Day 21–45 | 12–15°C, 50–100 µmol/m²/s, moderate flow | 2–5 cm sporophytes ready for deployment |

**Bioreactor design:** Rotating drum (200 rpm max), 0.5 L per culture chamber, 200 chambers per SCU. LED arrays (660 nm red + 450 nm blue) at 5 W per array. Temperature-controlled via Peltier elements (±0.5°C). Sterile seawater recirculated through 0.2 µm filter + UV sterilizer. Nutrient dosing via micro-peristaltic pumps (NaNO₃: 500 µM; NaH₂PO₄: 30 µM; Fe-EDTA: 5 µM; Mn, Zn, Co trace).

**Sporophyte quality control:** AI vision system monitors morphological development, rejects malformed/infected individuals. Target: ≥95% viability at deployment.

## 3. Substrate Anchor System

### 3.1 Mussel Foot Protein (MFP-5) Bioadhesive

**Composition:**
- Recombinant MFP-5 expressed in *Pichia pastoris* (GRAS organism)
- 30 kDa protein with 15 mol% DOPA residues
- Crosslinked with NaIO₄ (0.5 mM) triggering catechol oxidation
- Cured adhesive strength: 2.1 ± 0.3 MPa on granite, 1.8 MPa on basalt

**Delivery:** Dual-syringe micro-extruder on manipulator tip. Syringe A: MFP-5 solution (pH 3, 50 mg/mL). Syringe B: oxidant/buffer (pH 8.5, NaIO₄ + Tris). Mixing occurs at the deposition tip; curing begins within 5 seconds, full cure in 60 seconds at 12°C.

**Cost:** $0.008/anchor at projected production scale (100M units/year via precision fermentation).

### 3.2 Calcified Algae Composite Matrix

**Composition:**
- 60% crushed crustose coralline algae (*Lithothamnion* spp.) — CaCO₃ (calcite) + MgCO₃
- 25% alginate hydrogel (sodium alginate, 2% w/v)
- 10% chitosan (from crustacean shell waste, deacetylated 85%)
- 5% slow-release fertilizer granules (Fe-EDTA + silicate + trace Mn/Zn)

**Form factor:** Truncated cone, 15 mm base diameter, 8 mm top, 12 mm height. Central bore 3 mm for sporophyte insertion. Wall thickness 2–3 mm.

**Dissolution profile:**
- Days 0–30: Structural integrity maintained (>80% compressive strength)
- Days 30–90: Gradual dissolution, releasing Ca²⁺, CO₃²⁻, Fe, Si
- Days 90–180: Fully dissolved; holdfast has fused to rock surface

**Manufacturing:** Compression-molded at 80°C, 5 MPa, 30 seconds. Biodegradable mold release (rice starch). Rate: 3,000 units/hour per press.

**Cost:** $0.02/anchor at scale.

### 3.3 Herbivore Deterrent Microcapsules

**Composition:**
- 1.5% Cu²⁺ (as copper alginate) — below EPA aquaculture limit of 2%
- Alginate shell (2% sodium alginate, CaCl₂ crosslinked)
- Diameter: 500 µm
- Release rate: 0.01 mg Cu/day per capsule, 30-day effective life
- 20 capsules embedded per anchor
- Effective deterrence radius: 5 cm (covers sporophyte zone)

**Environmental safety:** Total Cu release per anchor = 0.3 mg over 30 days. At 25,000 anchors/hectare, total release = 7.5 g Cu/ha — well within natural background (8–50 mg/kg sediment). No bioaccumulation risk at these concentrations.

**Cost:** $0.005/anchor for embedded capsules.

## 4. AI Site Selection Model

### 4.1 Inputs (Real-Time Sensing)

| Input | Sensor | Resolution |
|-------|--------|------------|
| Bathymetry | Multibeam echosounder | 10 cm vertical, 50 cm lateral |
| Substrate classification | Hyperspectral imager + sonar | 5 cm pixels, 8 classes |
| Light availability (PAR) | Downwelling irradiance sensor | 1 µmol/m²/s |
| Temperature profile | Thermistor array (0–40 m) | ±0.1°C |
| Nutrients (N, P, Si) | Microfluidic colorimetric analyzer | 0.1 µM |
| Turbidity | Optical backscatter sensor | 0.1 NTU |
| Herbivore density | Stereo camera + AI (urchin, snail detection) | 1/m² |
| Existing biota | eDNA sampler (automated qPCR) | Species-level ID |

### 4.2 Prediction Model

- **Architecture:** Loihi 2 neuromorphic SNN (spiking neural network), 10M parameters
- **Training data:** 50,000+ kelp transplant records from global restoration projects (UC Santa Barbara, NOAA, CSIRO, SeaForestation)
- **Output:** Probability of sporophyte survival at 30/90/365 days, predicted canopy cover at 1/3/5 years
- **Accuracy target:** AUC ≥ 0.85 for 90-day survival prediction
- **Inference:** <100 mW on Loihi 2, <500 ms per site evaluation

### 4.3 Decision Logic

```
IF substrate = rock/boulder/cobble
AND depth 2–30 m (species-adjusted)
AND PAR > 5 mol/m²/day at deployment depth
AND temperature within species tolerance
AND urchin density < 5/m² (or deterrent planned)
AND nutrient availability N > 1 µM
AND no competing macroalgae > 30% cover
THEN site_score = weighted_sum(factors)
DEPLOY IF site_score > 0.7 (calibrated threshold)
```

## 5. Swarm Coordination Protocol

### 5.1 Communication

- **Acoustic mesh:** 9–14 kHz, chirp spread spectrum, 100 bps, 2 km range
- **Topology:** Self-organizing mesh; mothership = supernode
- **MAC:** TDMA with 100 ms slots, 10-unit swarm = 1 s frame
- **Data types:** Position (32 B), health (64 B), site map delta (≤1 KB compressed), sporophyte inventory (16 B)

### 5.2 Task Allocation

- **Area division:** Voronoi tessellation updated every 10 minutes based on unit positions and nursery load
- **Conflict resolution:** Highest-ID unit wins contested boundary cells
- **Load balancing:** Units with >80% nursery capacity prioritize planting; <20% prioritize mapping and returning to mothership

## 6. Environmental Safeguards

1. **No invasive species introduction:** AI validates target species against local registry; only native or pre-approved species deployed in each region.
2. **Biofouling control:** Ultrasonic cleaning (28 kHz, 10 W) activates every 4 hours; CuNi hull alloy. No biocide coatings.
3. **Noise:** Thruster noise < 150 dB re 1 µPa @ 1 m (below marine mammal disturbance threshold per NOAA).
4. **EMF:** DC motors only; EMF < 1 µT at 1 m (no navigational interference for marine fauna).
5. **End-of-life:** All non-biodegradable components (hull, battery, electronics) recovered by mothership for recycling. Biodegradable anchors fully dissolve.
6. **Regulatory compliance:** Designed to meet NOAA Essential Fish Habitat, EU Habitats Directive, and Australia EPBC Act requirements. Deployment requires local marine authority approval.

## 7. Development Roadmap

| Phase | Timeline | Milestones |
|-------|----------|------------|
| TRL 2–3 | 2026–2027 | Lab-scale sporophyte nursery, MFP-5 adhesive testing, anchor prototype molding, AI model training |
| TRL 4 | 2027–2028 | Integrated SCU prototype (tethered), nursery-to-deployment demo in seawater tank, adhesive cure optimization |
| TRL 5 | 2028–2029 | Untethered SCU field trials in Monterey Bay (kelp-present site), 100 sporophytes deployed, survival tracking |
| TRL 6 | 2029–2030 | 5-unit swarm trial, 10 ha restoration plot, mothership integration, 1-year survival data |
| TRL 7 | 2030–2032 | 10-unit fleet, 500 ha restoration in 3 sites (California, Tasmania, Norway), multi-species, regulatory approval |
| TRL 8–9 | 2032–2035 | Commercial deployment, 50-unit fleets, global partnership with marine authorities and indigenous communities |

## 8. Key Risk Analysis

| Risk | Likelihood | Mitigation |
|------|-----------|------------|
| Sporophyte mortality during transfer | Medium | Closed-loop nursery-to-anchor path; humidity retention sheath |
| Herbivore overwhelming deterrents | Medium | Adaptive deterrent dosing; urchin removal via partner ROVs |
| Storm damage to deployed sporophytes | Low-Medium | Site selection avoids exposed zones; anchor geometry tested to 2 m/s current |
| Biofouling reducing SCU efficiency | Medium | Ultrasonic cleaning + CuNi hull; weekly mothership hull wipe |
| Regulatory delays | High | Early engagement with marine authorities; modular species database for regional compliance |
| Scale-up of MFP-5 production | Low | Precision fermentation is well-established; *Pichia* expression at >5 g/L demonstrated |

---

*Specification v1.0 — Autonomous Kelp Forest Cultivator — 2026-06-16*