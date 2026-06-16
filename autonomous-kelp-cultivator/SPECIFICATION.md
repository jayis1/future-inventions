# Technical Specification — Autonomous Kelp Forest Cultivator (AKFC)

**Document Version:** 2.0 — Engineering Specification  
**Date:** 2026-06-16  
**Classification:** Open — For Review  

---

## 1. System Architecture Overview

### 1.1 System of Systems

The AKFC is a distributed robotic system consisting of two platform types operating in concert:

```
┌──────────────────────────────────────────────────────────────┐
│                    AKFC FLEET ARCHITECTURE                     │
│                                                               │
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐    │
│  │  SMP Alpha   │◄──►│  SMP Beta    │◄──►│  SMP Gamma   │    │
│  │  (Primary)   │    │  (Secondary) │    │  (Tertiary)  │    │
│  └──────┬───────┘    └──────┬───────┘    └──────┬───────┘    │
│         │                   │                   │             │
│    ┌────┴────┐         ┌────┴────┐         ┌────┴────┐       │
│    │ 10 SCUs │         │ 10 SCUs│         │ 10 SCUs │       │
│    └─────────┘         └─────────┘         └─────────┘       │
│                                                               │
│  Fleet Coordination: Satellite uplink → Cloud → Mission Ctrl │
│  Swarm Comms: Acoustic mesh (inter-unit) + Satellite (fleet) │
└──────────────────────────────────────────────────────────────┘
```

### 1.2 Design Philosophy

- **Autonomy-first:** All critical decisions (navigation, site selection, deployment, health monitoring) are made onboard without human intervention. Human operators set mission parameters and review alerts.
- **Bio-inspired:** Nursery design mirrors natural kelp life cycle; anchoring system mimics mussel adhesion; swarm coordination draws from fish schooling algorithms.
- **Fail-safe:** Single-unit failures do not compromise fleet operations. Lost units surface automatically via positive buoyancy. Nursery cultures are isolated to prevent cross-contamination.
- **Minimal ecological footprint:** All materials selected for marine biocompatibility. No persistent pollutants. Energy from renewable sources. Acoustic noise below marine mammal disturbance thresholds.

---

## 2. Submersible Cultivator Unit (SCU) — Detailed Specification

### 2.1 Hull & Structure

| Parameter | Specification | Rationale |
|-----------|--------------|-----------|
| Overall length | 1.8 m | Maneuverability in reef structures |
| Beam (max) | 0.6 m | Access between rocks and crevices |
| Height | 0.45 m | Low profile for current resistance |
| Dry mass | 85 kg | Neutral buoyancy with ±0.5 N reserve |
| Displacement | 92 L (seawater) | Provides ~7 kg payload margin |
| Hull material | 70/30 CuNi alloy, 1.5 mm skin | Biofouling resistance, 50+ year marine life |
| Frame | 316L SS tubing, 25 mm OD | High strength, corrosion resistant |
| Fairing | Polyurethane (PU) panels, 8 mm | Streamlined flow, acoustic damping |
| Viewports | Sapphire crystal, 4× (cameras + sensors) | Scratch resistance >10× acrylic |
| Operating depth | 2–40 m (kelp photic zone) | Covers >95% of global kelp habitat |
| Design depth | 60 m (with safety margin) | 1.5× operating depth |
| Impact resistance | 0.5 m/s collision without damage | Soft pneumatic arm absorbs impacts |
| Operating temperature | -2°C to +35°C | Arctic to tropical kelp habitats |
| Storage temperature | -10°C to +50°C | Transport and shore storage |

### 2.2 Propulsion & Maneuvering

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Type | 4× vectored rim-driven thrusters | Magnetic coupling, no shaft seals |
| Thrust (per unit) | 25 N continuous, 40 N burst | 5-minute burst limit |
| Max speed | 1.5 m/s cruise, 2.0 m/s burst | Sufficient for 2 m/s current operations |
| Efficiency | 0.35 N/W | Rim-driven = 15% better than shaft-driven |
| Acoustic signature | <150 dB re 1 µPa @ 1 m | Below NOAA marine mammal threshold (160 dB) |
| Maneuverability | 6-DOF (4× vectored + variable buoyancy) | Hover, translate, rotate in place |
| Variable buoyancy | Seawater pump, ±5 kg displacement | 0.1 kg resolution via micro-pump |
| Trim | Adjustable lead ballast weights | Set for neutral buoyancy at deployment depth |

#### Thruster Layout (Top View)
```
     Bow
      ▲
  ┌───┴───┐
  │       │
◄─┤  T1   ├─►  T1: Port bow (45° canted)
  │       │
◄─┤  T2   ├─►  T2: Starboard bow (45° canted)
  │       │
  │ SCU   │
  │ Body  │
  │       │
◄─┤  T3   ├─►  T3: Port stern (45° canted)
  │       │
◄─┤  T4   ├─►  T4: Starboard stern (45° canted)
  │       │
  └───┬───┘
      ▼
     Stern
```

### 2.3 Power System

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Battery type | LiFePO₄ (LFP) | Safest lithium chemistry, zero cobalt |
| Capacity | 2.5 kWh (50 Ah × 50.4V) | 16S configuration |
| Cycle life | 3,000+ cycles (10+ years) | LFP longevity |
| Charging | Inductive (Qi-compatible marine), 500W | 5-hour full charge |
| Charge cycle | 2 hours (from mothership) | 80% charge in 90 min |
| Endurance | 12 hours submerged per charge | At 1 m/s cruise + 4 hrs planting |
| Energy budget | | |
| — Propulsion (cruise) | 60 W | 1 m/s continuous |
| — Propulsion (planting) | 20 W | Station-keeping |
| — Nursery (continuous) | 15 W | LEDs + pumps + heating |
| — Sensors | 25 W | Multibeam + hyperspectral + cameras |
| — Compute (Loihi 2) | 5 W | Neuromorphic inference |
| — Manipulator | 30 W | During deployment only |
| — Communications | 2 W | Acoustic modem (receive) |
| — Total (planting mode) | ~157 W | Peak during active deployment |
| — Total (transit mode) | ~107 W | Cruise + navigation |
| — Total (loiter/charge nursery) | ~37 W | Nursery + minimal systems |
| Depth rating (battery) | IP68, 100 m | Oil-compensated housing |

### 2.4 Navigation & Sensing

#### Navigation Suite

| Sensor | Model/Type | Specification | Function |
|--------|-----------|---------------|----------|
| INS | MEMS 9-DOF IMU | ±0.05° heading, ±0.1° pitch/roll | Dead reckoning |
| DVL | Doppler Velocity Log | 0.3–10 m altitude, ±0.2% velocity | Bottom-lock navigation |
| Acoustic ranging | 9–14 kHz transponder | 2 km range, ±1 m accuracy | Relative positioning |
| Forward sonar | 200 kHz imaging | 30 m range, 2 cm resolution | Obstacle avoidance |
| GPS | Multi-constellation (GPS+GLONASS+Galileo) | ±1 m (surfaced) | Absolute position fix |
| Pressure depth | Piezoresistive | 0–100 m, ±0.05 m | Depth reference |

#### Mapping & Imaging Suite

| Sensor | Specification | Function |
|--------|---------------|----------|
| Multibeam echosounder | 200 kHz, 256 beams, 10 cm vertical / 50 cm lateral | Bathymetric mapping |
| Stereo cameras (2×) | 4K (3840×2160), 30 fps, global shutter | Herbivore detection, growth monitoring |
| Hyperspectral imager | 400–1000 nm, 200 bands, 5 cm GSD at 5 m | Substrate classification, kelp health |
| Downwelling irradiance | PAR sensor (400–700 nm), 1 µmol/m²/s resolution | Light availability mapping |
| Optical backscatter | 880 nm, 0.1 NTU resolution | Turbidity measurement |
| Chlorophyll fluorescence | Blue excitation (470 nm), emission 680 nm | Kelp health proxy |
| eDNA sampler | Automated water sampling + onboard micro-qPCR | Species identification |

#### Sensor Processing Pipeline

```
Raw sensor data → Edge preprocessing → Feature extraction → Loihi 2 SNN
     │                  │                    │                  │
     ├─ Multibeam → DEM │                    │                  │
     ├─ Hyperspec → PCA  │                    │                  │
     ├─ Stereo → Depth   │                    │                  │
     ├─ eDNA → Species   │                    │                  │
     └─ CTD + Nutrients  │                    │                  │
                         │                    │                  │
                         ▼                    ▼                  ▼
                    Fused Map ──────► Site Scoring ──────► Deploy/Pass Decision
```

### 2.5 Nursery Bioreactor

#### 2.5.1 Physical Design

```
┌─────────────────────────────────────────────┐
│              NURSERY BIOREACTOR              │
│  ┌─────────────────────────────────────────┐│
│  │  Rotating Drum (200 chambers, 0.5L ea) ││
│  │  ┌──┐┌──┐┌──┐┌──┐┌──┐┌──┐┌──┐┌──┐   ││
│  │  │01││02││03││04││..││..││..││200│   ││
│  │  └──┘└──┘└──┘└──┘└──┘└──┘└──┘└──┘   ││
│  │         LED arrays (660+450 nm)         ││
│  └─────────────────────────────────────────┘│
│  ┌──────────┐ ┌──────────┐ ┌────────────┐ │
│  │ Nutrient │ │ Seawater │ │  Thermal   │ │
│  │ Dosing   │ │ Filter + │ │  Control   │ │
│  │ (4 pumps)│ │ UV Ster. │ │ (Peltier)  │ │
│  └──────────┘ └──────────┘ └────────────┘ │
│  ┌──────────┐ ┌──────────────────────────┐ │
│  │ AI Vision│ │  Camera + Lighting Array  │ │
│  │ Monitor  │ │  (per 20 chambers)       │ │
│  └──────────┘ └──────────────────────────┘ │
└─────────────────────────────────────────────┘
```

#### 2.5.2 Kelp Sporophyte Production Pipeline

**Species supported (primary):**

| Species | Common Name | Range | Max Length | Growth Rate | Temperature Range |
|---------|------------|-------|------------|-------------|-------------------|
| *Macrocystis pyrifera* | Giant Kelp | Pacific (California to Peru, S. Africa, Australia) | 60 m | 60 cm/day | 6–20°C |
| *Laminaria digitata* | Oarweed | N. Atlantic (Europe, E. North America) | 3 m | 5 cm/day | 3–16°C |
| *Saccharina latissima* | Sugar Kelp | N. Atlantic/Arctic | 4 m | 4 cm/day | -1–18°C |
| *Ecklonia maxima* | Sea Bamboo | S. Africa, Indian Ocean | 12 m | 10 cm/day | 10–22°C |
| *Laminaria hyperborea* | Cuvie | NE Atlantic (Norway to Portugal) | 3.5 m | 3 cm/day | 4–16°C |
| *Lessonia nigrescens* | Black Kelp | SE Pacific (Chile/Peru) | 2 m | 3 cm/day | 8–18°C |

**Growth stages (for *Macrocystis pyrifera*):**

| Stage | Duration | Conditions | Output | Quality Check |
|-------|----------|------------|--------|---------------|
| Zoospore release | 0–12 hrs | 10°C, dark, 1 L/min flow | 10⁶ zoospores/L | Motility >90% |
| Gametophyte culture | Day 1–20 | 15°C, 20–50 µmol/m²/s (660+450 nm LED), sterile seawater + 500 µM NaNO₃ + 30 µM NaH₂PO₄ | Female (multicellular) + male (filamentous) gametophytes | AI vision: morphology scoring, >85% normal development |
| Fertilization | Day 20–21 | Mix male/female at 10°C, reduced light (10 µmol/m²/s) | Zygotes form on female gametophytes | AI vision: zygote formation confirmed in >80% of chambers |
| Sporophyte growth | Day 21–45 | 12–15°C, 50–100 µmol/m²/s, moderate flow (0.5 L/min), 500 µM NaNO₃ + 30 µM NaH₂PO₄ + 5 µM Fe-EDTA + trace Mn/Zn/Co | 2–5 cm sporophytes | AI vision: length, blade number, pigmentation (NDVI ≥ 0.6), root formation |
| Pre-deployment hardening | Day 40–45 | Gradual temperature shift to ambient seawater, increased flow (1 L/min), reduced nutrients | Acclimated sporophytes | AI vision: viability scoring, ≥95% deployment-ready |

#### 2.5.3 Bioreactor Engineering Parameters

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Chamber volume | 0.5 L per chamber | Borosilicate glass, PTFE seals |
| Number of chambers | 200 per SCU | Rotating drum mechanism |
| Total nursery volume | 100 L (200 × 0.5 L) | + 20 L recirculation system |
| Rotation rate | 0–200 rpm (programmable) | Simulates natural water motion |
| LED arrays | 660 nm (red) + 450 nm (blue), 5W per array × 10 arrays | Programmable photoperiod |
| Light intensity range | 0–200 µmol/m²/s | Adjustable for growth stage |
| Temperature control | Peltier elements, ±0.5°C, range 0–25°C | Independent per 20-chamber group |
| Filtration | 0.2 µm PES membrane + 254 nm UV-C | Sterile seawater input |
| Nutrient dosing | 4× micro-peristaltic pumps (NaNO₃, NaH₂PO₄, Fe-EDTA, trace metals) | ±5% precision |
| AI vision | 10× monochrome cameras (5 MP) + 10× LED ring lights | One camera per 20 chambers |
| Sporophyte capacity | 2,000 per full cycle (10 per chamber) | 4–6 week cycle |
| Throughput | 2,000 sporophytes / 45 days | ~44/day average after first cycle |

### 2.6 Manipulator Arm

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Type | 6-DOF soft pneumatic | Based on Harvard WHC PneuNet design |
| Reach | 1.2 m from SCU center | Accesses deployment zone beneath unit |
| Payload | 5 kg | Sufficient for anchor + adhesive system |
| Positioning accuracy | ±2 mm | At end effector |
| Force control | 0.1–50 N | Compliant contact for delicate sporophytes |
| Actuator material | Silicone elastomer (Ecoflex 00-30) + PET mesh | Durable, marine-compatible |
| Operating depth | 2–40 m (compensated) | Air-pressure compensated |
| Degrees of freedom | 6 (3 shoulder + 2 elbow + 1 wrist) | Redundant for obstacle avoidance |
| End effector | Dual function: (1) soft gripper for anchor handling, (2) dual-syringe MFP-5 extruder | Swappable during maintenance |
| Cycle time | 30 seconds per anchor deployment | Anchor pick → position → extrude → press → verify |

### 2.7 Anchor Deployment Carousel

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Capacity | 200 anchors per sortie | 2,000 sporophytes / 10 per sortie |
| Anchor dimensions | 15 mm base × 8 mm top × 12 mm height (truncated cone) | Fits in carousel slots |
| Carousel type | Rotary magazine, spring-loaded ejection | One anchor per 2 seconds |
| Loading | Automated from nursery bioreactor via transfer tube | Sporophyte inserted into anchor bore during loading |
| Adhesive system | Dual-syringe micro-extruder (Syringe A: MFP-5 @ pH 3, 50 mg/mL; Syringe B: NaIO₄ + Tris buffer @ pH 8.5) | Mixing at deposition tip |
| Adhesive volume | 0.5 mL per anchor (0.25 mL per syringe) | 100 mL total per sortie (200 deployments) |
| Syringe refills | From reservoir tanks (Syringe A: 500 mL; Syringe B: 500 mL) | Sufficient for 1,000 deployments before refill |

### 2.8 Communications

| Mode | Technology | Range | Bandwidth | Power | Function |
|------|-----------|-------|-----------|-------|----------|
| Underwater (SCU↔SCU) | Acoustic chirp spread spectrum, 9–14 kHz | 2 km | 100 bps | 2 W (TX), 0.5 W (RX) | Swarm coordination, site data |
| Underwater (SCU↔SMP) | Acoustic, 9–14 kHz | 2 km | 100 bps | 2 W (TX) | Command relay, position reports |
| Surface (SCU/SMP surfaced) | Wi-Fi 6 (802.11ax) | 100 m | 1 Gbps | 5 W | Bulk data upload |
| Surface-to-orbit | Starlink Mini + Iridium Certus | Global | 50 Mbps (Starlink), 22 Kbps (Iridium) | 30–75 W | Mission data, remote command |
| Emergency | Iridium 406 MHz beacon | Global | 0.044 bps | 0.5 W | SOS / unit recovery |

### 2.9 Biofouling Mitigation

| Method | Specification | Coverage | Maintenance |
|--------|---------------|----------|-------------|
| Hull material | 70/30 CuNi alloy skin | 95% of external surface | Passive (continuous) |
| Ultrasonic cleaning | 28 kHz, 10 W transducers × 4 | 80% of surface | 10 min every 4 hours |
| Rotating brush | Soft bristle, motor-driven | Camera/sensor viewports | Activated during surfaced charging |
| Anti-settlement coating | Foul-release silicone (Intersleek-type) on PU fairing | 100% of fairing | Reapply annually |
| Nursery | UV-C sterilization + 0.2 µm filtration + sterile seawater | 100% | Continuous |

---

## 3. Surface Mothership Platform (SMP) — Detailed Specification

### 3.1 Hull & Structure

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Type | 6 m catamaran, HDPE rotomolded hulls | Proven, low-cost, low-maintenance |
| Beam (overall) | 3.2 m | Stable platform for SCU operations |
| Draft | 0.6 m | Operates in shallow coastal waters |
| Dry mass | 800 kg | |
| Displacement | 2,500 kg (with equipment and 4 SCUs) | |
| Freeboard | 0.8 m | Sufficient for wave action |
| Seakeeping | Operates in Sea State 4 (1.25–2.5 m significant wave height) | Survival in Sea State 6 |
| Mooring | GPS anchor watch + dynamic positioning (2× azimuth thrusters) | Station-keeping within 5 m |

### 3.2 Power System

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| Solar | 800 W flexible SunPower panels (4× 200W) | 5.5 kWh/day at 70% capacity factor |
| Wave energy | 400 W oscillating water column (OWC) | 9.6 kWh/day at average wave climate |
| Total generation | ~15 kWh/day | |
| Battery | 20 kWh LiFePO₄ (400 Ah × 50.4V) | 2–3 days reserve |
| SCU charging | 4× inductive charge pads, 500W each | Simultaneous charging, 2-hr full charge |
| SCU charge throughput | 4 SCUs × 2 hrs = 8 hrs for full fleet | SCUs rotate through charging pads |
| Satellite terminal | Starlink Mini (75W) + Iridium Certus (30W) | Average 50W continuous |
| Compute | Loihi 2 + companion system | 15W average |
| Auxiliary | Navigation lights, bilge pump, weather station | 10W average |
| Total continuous load | ~75W | Leaves ~500W for SCU charging + reserve |

### 3.3 SCU Handling & Logistics

| Parameter | Specification | Notes |
|-----------|--------------|-------|
| SCU docking | 4× inductive charge pads, magnetic alignment | Automated docking (SCU surfaces and navigates to pad) |
| SCU resupply | Automated: sporophyte transfer from tender, anchor carousel refill, adhesive syringe refill | Via tender vessel (weekly) |
| Tender vessel | Autonomous surface craft (3 m, electric, solar) | Shuttles supplies from shore base |
| Sporophyte resupply | 2,000 sporophytes per tender run (weekly) | SCU nurseries produce continuously after initial seeding |
| Adhesive resupply | 2× 500 mL syringe refills per tender run | Sufficient for 1,000 deployments |
| Data download | Wi-Fi 6 bulk transfer during surface charging | Hyperspectral data, site maps, growth images |

---

## 4. Substrate Anchor System — Detailed Specification

### 4.1 Mussel Foot Protein (MFP-5) Bioadhesive

#### 4.1.1 Composition & Properties

| Property | Value | Test Method |
|----------|-------|-------------|
| Primary protein | Recombinant MFP-5 (30 kDa, 15 mol% DOPA) | SDS-PAGE, HPLC |
| Expression host | *Pichia pastoris* X-33 (GRAS) | |
| Crosslinker | NaIO₄ (0.5 mM final concentration) | |
| Buffer | Tris-HCl 50 mM, pH 8.5 | |
| Adhesion to granite | 2.1 ± 0.3 MPa | ASTM D1002 (modified for underwater) |
| Adhesion to basalt | 1.8 ± 0.2 MPa | ASTM D1002 |
| Adhesion to limestone | 1.5 ± 0.3 MPa | ASTM D1002 |
| Adhesion to CaCO₃ | 1.6 ± 0.2 MPa | ASTM D1002 |
| Cure time (12°C seawater) | <60 seconds (90% strength) | Rheometry |
| Working time (after mixing) | 5–15 seconds | Manual handling |
| Storage stability (pH 3, 4°C) | >12 months | No degradation |
| pH operating range | 6–9 | Marine pH range |
| Temperature operating range | 2–25°C | All kelp habitats |
| Toxicity | None (GRAS organism, biodegradable) | OECD 201/202/203 |

#### 4.1.2 Production Pathway

```
Gene synthesis (MFP-5 codon-optimized for Pichia)
         │
         ▼
P. pastoris expression (AOX1 promoter, methanol induction)
         │
         ▼
Fed-batch fermentation (500 L → 10,000 L → 100,000 L)
         │
         ▼
Centrifugation + 0.45 µm filtration (minimal purification)
         │
         ▼
Acidification to pH 3 + sterile packaging (1 L bags)
         │
         ▼
Cold chain shipping (4°C) → SMP resupply
```

#### 4.1.3 Cost Trajectory

| Production Volume | Yield | Cost per gram | Cost per anchor (0.5 mL = 25 mg) |
|-------------------|-------|--------------|-----------------------------------|
| Pilot (500 L) | 5 g/L | $50 | $1.25 |
| Scale-up (10,000 L) | 8 g/L | $5 | $0.125 |
| Industrial (100,000 L) | 10 g/L | $0.32 | $0.008 |

### 4.2 Calcified Algae Composite Matrix

#### 4.2.1 Composition & Properties

| Component | Percentage | Function | Source |
|-----------|-----------|----------|--------|
| Crushed crustose coralline algae (*Lithothamnion* spp.) | 60% | Structural matrix, CaCO₃ source, kelp-preferred substrate | Dredged from sustainable marine sources; waste from aquaculture |
| Sodium alginate (2% w/v) | 25% (of hydrogel phase) | Binding agent, water retention | Brown seaweed extract (commercial) |
| Chitosan (85% deacetylated) | 10% (of hydrogel phase) | Structural reinforcement, antifungal | Crustacean shell waste (commercial) |
| Fe-EDTA + silicate granules | 5% (of hydrogel phase) | Slow-release micronutrients | Commercial fertilizer-grade |

| Property | Value | Test Method |
|----------|-------|-------------|
| Form factor | Truncated cone: 15 mm base × 8 mm top × 12 mm height | Caliper measurement |
| Central bore | 3 mm diameter (sporophyte insertion) | |
| Wall thickness | 2–3 mm | |
| Compressive strength (Day 0) | 4.2 ± 0.5 MPa | ASTM D695 (underwater) |
| Compressive strength (Day 30) | >3.4 MPa (80%+ retained) | |
| Compressive strength (Day 90) | ~1.0 MPa (gradual dissolution) | |
| Complete dissolution | 120–180 days | Mass loss in flowing seawater |
| Nutrient release (total) | Ca²⁺: 15 mg, CO₃²⁻: 12 mg, Fe: 0.5 mg, Si: 0.3 mg | ICP-OES of dissolution water |
| Manufacturing | Compression molding, 80°C, 5 MPa, 30 seconds | Custom mold, biodegradable release agent |
| Production rate | 3,000 units/hour/press | 8-hour shift = 24,000 units |

#### 4.2.2 Manufacturing Process

```
Raw material preparation:
  Coralline algae → washed → dried → milled → sieved (200 µm)
  Alginate → dissolved in deionized water (2% w/v)
  Chitosan → dissolved in 1% acetic acid → precipitated → dried → milled

Mixing:
  Coralline algae powder + alginate solution + chitosan powder + Fe-EDTA/Si granules
  → planetary mixer (5 min, 500 rpm)
  → dough-like consistency

Molding:
  Compression molding machine, 80°C, 5 MPa, 30 seconds
  → biodegradable rice starch mold release
  → cooled on conveyor (2 min to room temperature)

Quality control:
  → dimensional check (±0.5 mm)
  → compressive strength test (1 per 1,000)
  → dissolution rate test (1 per 10,000, in simulated seawater)
  → sporophyte insertion test (1 per 5,000)

Packaging:
  → 200 anchors per sealed bag (nitrogen atmosphere)
  → stored at 4°C until deployment
  → shelf life: 12 months
```

### 4.3 Herbivore Deterrent Microcapsules

| Property | Value | Notes |
|----------|-------|-------|
| Shell material | Sodium alginate (2% w/v), CaCl₂ crosslinked | |
| Core | Copper alginate (1.5% Cu²⁺ by mass) | Below EPA 2% limit |
| Diameter | 500 µm ± 50 µm | Microfluidic production |
| Release rate | 0.01 mg Cu/day per capsule | Sustained release via diffusion |
| Effective life | 30 days | |
| Capsules per anchor | 20 | |
| Effective radius | 5 cm from anchor center | Covers sporophyte growth zone |
| Total Cu release per anchor | 0.3 mg over 30 days | |
| Total Cu release per hectare | 7.5 g (at 25,000 anchors/ha) | Natural sediment: 8–50 mg/kg |
| Environmental safety | Below all regulatory thresholds | No bioaccumulation risk |
| Production | Microfluidic droplet generator, 10,000 capsules/min | |

---

## 5. AI Site Selection Model — Detailed Specification

### 5.1 Model Architecture

| Parameter | Value |
|-----------|-------|
| Architecture | Spiking Neural Network (SNN) on Intel Loihi 2 |
| Parameters | 10M (1M neurons, 10M synapses) |
| Input dimensions | 8 channels × 128×128 spatial grid |
| Output dimensions | Per-pixel: survival probability at 30/90/365 days; canopy cover at 1/3/5 years |
| Inference time | <500 ms per site evaluation |
| Power consumption | <100 mW (Loihi 2 at 5 mW/MAC) |
| Training data | 50,000+ global kelp transplant records (UCSB, NOAA, CSIRO, SeaForestation) |
| Training method | Supervised (survival labels) + self-supervised (temporal satellite imagery) |
| Target AUC | ≥0.85 for 90-day survival prediction |
| Update mechanism | Federated learning across fleet; model updates via satellite uplink monthly |

### 5.2 Input Features

| Feature | Sensor | Spatial Resolution | Temporal Resolution |
|---------|--------|-------------------|---------------------|
| Bathymetry | Multibeam echosounder | 10 cm vertical, 50 cm lateral | Per sortie |
| Substrate classification | Hyperspectral + sonar | 5 cm pixels, 8 classes | Per sortie |
| Photosynthetically Active Radiation (PAR) | Downwelling irradiance sensor | 1 µmol/m²/s | Continuous |
| Temperature profile | Thermistor array (10 depths) | ±0.1°C | Continuous |
| Nutrient concentration (N, P, Si) | Microfluidic colorimetric analyzer | 0.1 µM | Per sortie |
| Turbidity | Optical backscatter | 0.1 NTU | Continuous |
| Herbivore density | Stereo camera + AI | 1/m² (urchin, snail detection) | Per sortie |
| Existing biota | eDNA sampler + micro-qPCR | Species-level ID | Per sortie |

### 5.3 Decision Logic

```python
def evaluate_deployment_site(site_data):
    """Core site selection algorithm running on Loihi 2"""
    
    # Hard constraints (must-pass)
    if site_data.substrate not in ['rock', 'boulder', 'cobble', 'reef_ball']:
        return REJECT  # Kelp cannot attach to sand/mud
    
    if not (2 <= site_data.depth <= 30):  # Species-adjusted
        return REJECT  # Outside photic zone
    
    if site_data.PAR < 5:  # mol/m²/day
        return REJECT  # Insufficient light
    
    if site_data.temperature > species.max_temp:
        return REJECT  # Thermal stress
    
    if site_data.urchin_density > 5 and not deterrent_planned:
        return CONDITIONAL  # Requires deterrent deployment
    
    if site_data.nitrogen < 1:  # µM
        return CONDITIONAL  # Nutrient supplementation needed
    
    # Soft scoring (weighted sum)
    weights = {
        'substrate_quality': 0.20,  # Rock > boulder > cobble
        'depth_optimality': 0.15,   # Species-specific optimal depth
        'PAR_sufficiency': 0.15,    # More light = better growth
        'temperature_match': 0.15,  # Within optimal range
        'nutrient_availability': 0.10,  # N, P, Si, Fe
        'herbivore_risk': 0.10,    # Lower urchin density = better
        'current_regime': 0.05,    # Moderate flow = nutrient delivery
        'existing_biota': 0.05,   # Native algae complement
        'proximity_to_forest': 0.05,  # Near existing kelp = better
    }
    
    score = sum(w * normalize(site_data[f]) for f, w in weights.items())
    
    if score > 0.7:
        return DEPLOY
    elif score > 0.5:
        return ADDITIONAL_SENSING  # Request more data
    else:
        return SKIP  # Log for future reference
```

---

## 6. Swarm Coordination Protocol

### 6.1 Communication Architecture

```
                    ┌────────────────┐
                    │  Satellite     │
                    │  (Starlink/    │
                    │   Iridium)     │
                    └───────┬────────┘
                            │
                    ┌───────┴────────┐
                    │  Cloud Mission  │
                    │  Control        │
                    └───────┬────────┘
                            │
                    ┌───────┴────────┐
                    │  SMP (Surface)  │
                    │  Supernode      │
                    └───┬───┬───┬────┘
                        │   │   │
            ┌───────────┘   │   └───────────┐
            │               │               │
        ┌───┴───┐       ┌───┴───┐       ┌───┴───┐
        │ SCU 1 │◄─────►│ SCU 2 │◄─────►│ SCU 3 │  ...
        └───┬───┘       └───────┘       └───┬───┘
            │                               │
        ┌───┴───┐                       ┌───┴───┐
        │ SCU 4 │◄─────────────────────►│ SCU 5 │  ...
        └───────┘                       └───────┘
        
        Acoustic Mesh: 9-14 kHz, Chirp Spread Spectrum
        Range: 2 km per hop
        Bandwidth: 100 bps
        MAC: TDMA, 100 ms slots, 10-unit swarm = 1 s frame
```

### 6.2 Task Allocation

| Phase | SCU Behavior | SMP Role |
|-------|-------------|----------|
| **Deployment** | High nursery load (>50%) → prioritize planting; low nursery load (<20%) → prioritize mapping and return | Coordinate area assignment; monitor fleet health |
| **Monitoring** | Return to planted sites on 30/60/90-day schedule; assess growth, detect herbivory, measure health | Aggregate monitoring data; flag intervention needs |
| **Recovery** | Low battery (<20%) → surface and return to SMP for charging; nursery depleted → surface for resupply | Manage charging queue; dispatch tender for resupply |
| **Adaptive** | Herbivory detected → deploy deterrent; nutrient stress → deploy supplement; sporophyte failure → replant | Coordinate intervention across fleet; update AI model |

### 6.3 Area Coverage Algorithm

- **Method:** Voronoi tessellation of operating area, updated every 10 minutes based on SCU positions and nursery load
- **Coverage target:** 100% of suitable substrate within operating area mapped within first 72 hours
- **Planting density:** 25,000 sporophytes/hectare (1 per 20 cm × 20 cm grid, optimized for canopy closure)
- **Conflict resolution:** Highest-ID unit wins contested boundary cells; units with overlapping coverage share data but not effort
- **Revisit scheduling:** Priority queue based on time since last visit + predicted growth stage + anomaly detection

---

## 7. Environmental Impact Assessment

### 7.1 Positive Impacts

| Impact | Quantification | Confidence |
|--------|---------------|------------|
| Carbon sequestration | 10–20 t CO₂/ha/yr | High (measured values) |
| Fishery enhancement | 5–10 t fish/ha/yr | High |
| Coastal protection | 30–70% wave energy reduction | High |
| pH buffering | +0.1–0.3 pH units in kelp shadow | Medium |
| Biodiversity support | 1,000+ species per ha | High |

### 7.2 Potential Negative Impacts & Mitigations

| Impact | Risk Level | Mitigation | Monitoring |
|--------|-----------|------------|------------|
| Copper release | Very Low (7.5 g Cu/ha total) | Below all thresholds; capsules dissolve completely | eDNA for copper-tolerant organisms; sediment Cu analysis |
| Acoustic noise | Low (<150 dB re 1 µPa @ 1 m) | Below NOAA marine mammal threshold | Passive acoustic monitoring |
| Habitat disturbance | Low | SCUs avoid sensitive areas; soft pneumatic arm | Before/after benthic surveys |
| Genetic introgression | Low (native species only) | Strict species validation; local provenance | eDNA monitoring for hybridization |
| Visual/aesthetic | Very Low | Submerged operation; surface platform is small | Community engagement |
| Entanglement risk | Very Low | No nets or lines; smooth hull; slow speed | Marine mammal observer reports |

### 7.3 End-of-Life Protocol

- **SCU hull, battery, electronics:** Recovered by mothership, shipped to recycling facility. CuNi hull recycled. LiFePO₄ battery recycled (95% material recovery). Electronics recycled via e-waste stream.
- **Biodegradable anchors:** Fully dissolve in 120–180 days. No recovery needed. Leave no persistent materials.
- **MFP-5 bioadhesive:** Biodegradable protein. Decomposes via microbial action within 6–12 months after kelp holdfast has fused to rock.
- **SMP hull:** HDPE recyclable. Solar panels: standard recycling stream. Battery: LiFePO₄ recyclable.

---

## 8. Quality Assurance & Testing Protocol

### 8.1 Anchor Adhesion Testing

| Test | Standard | Acceptance Criteria |
|------|----------|-------------------|
| Lap shear (underwater) | ASTM D1002 (modified) | >2.0 MPa on granite, >1.5 MPa on basalt |
| Tensile pull-off | ASTM D4541 | >1.5 MPa on granite |
| Cure time | Rheometry | >90% strength at 60 seconds |
| Temperature range | 2–25°C seawater | >80% strength retention |
| pH range | pH 6–9 | >80% strength retention |
| UV exposure | 30-day UV aging | >90% strength retention |
| Biofilm adhesion | 30-day marine exposure | >70% strength retention |

### 8.2 Sporophyte Viability

| Test | Acceptance Criteria |
|------|-------------------|
| Morphological scoring (AI vision) | >95% normal development at deployment |
| Chlorophyll content (SPAD) | >40 SPAD units |
| NDVI (normalized difference vegetation index) | >0.6 |
| Root/holdfast development | Visible holdfast initials >0.5 mm |
| Post-deployment survival (90-day) | >85% |

### 8.3 SCU Performance

| Test | Acceptance Criteria |
|------|-------------------|
| Deployment accuracy | ±5 mm positioning |
| Deployment rate | >150 sporophytes/hour (sustained) |
| Nursery throughput | 2,000 sporophytes / 45 days |
| Navigation accuracy | ±2 m over 1 km (surfaced GPS calibration) |
| Biofouling resistance | <10% speed reduction over 30 days |
| Communications reliability | >99% message delivery within swarm |
| Battery endurance | >10 hours submerged at 1 m/s |

---

## 9. Regulatory Compliance Matrix

| Regulation | Jurisdiction | Status | Notes |
|------------|-------------|--------|-------|
| NOAA Essential Fish Habitat | USA | Compliant by design | Kelp restoration is encouraged |
| EU Habitats Directive | EU | Requires EIA | Case-by-case assessment |
| Australia EPBC Act | Australia | Requires permit | Indigenous consultation required |
| London Convention/Protocol | International | Compliant | No persistent waste disposal |
| UNCLOS | International | Compliant | Activities within territorial waters |
| Marine Mammal Protection Act | USA | Compliant | Acoustic noise <150 dB; no entanglement risk |
| Clean Water Act (Section 404) | USA | May require permit | Copper release well below thresholds |
| IUCN Guidelines for Restoration | International | Compliant | Native species, local provenance |

---

## 10. Key Risk Analysis — Expanded

| Risk | Likelihood | Impact | Mitigation | Residual Risk | Contingency |
|------|-----------|--------|------------|---------------|-------------|
| Sporophyte mortality during transfer | Medium | High | Closed-loop transfer; humidity sheath; <4 hr deployment window | Low | Nursery redundancy (2× capacity); onshore backup nursery |
| Herbivore overwhelming deterrents | Medium | High | Adaptive Cu dosing; partner urchin removal; 3-month window bridges critical period | Medium | Deploy in areas with natural sea otter populations; install urchin exclusion cages temporarily |
| Storm damage to planted sporophytes | Low-Medium | Medium | AI avoids exposed sites; anchor tested to 2 m/s current; kelp naturally storm-resistant | Low | Replant after severe storms from reserve nursery stock |
| Biofouling reducing SCU efficiency | Medium | Medium | Ultrasonic cleaning + CuNi hull; weekly hull wipe at SMP | Low | Replace fouled units; rotate cleaning schedule |
| MFP-5 scale-up challenges | Low | High | Precision fermentation is mature; *Pichia* >5 g/L demonstrated; multiple contract manufacturers | Low | Fallback: synthetic catechol-lysine polymer (lower performance, higher cost) |
| Regulatory delays | High | Medium | Early engagement; modular species database; pilot in permissive jurisdictions; indigenous partnerships | Medium | Parallel deployment across multiple jurisdictions to maintain momentum |
| Thermal stress from ocean warming | Medium | High | Deploy heat-tolerant strains; AI selects thermal refugia; monitor and adapt species | Medium | Accept some losses at marginal sites; concentrate effort at high-probability locations |
| Entanglement with marine mammals | Low | Medium | Slow speed; soft arm; no nets; CuNi hull; acoustic noise below thresholds | Very Low | Emergency surface protocol; wildlife observer protocol |
| Invasive species introduction | Low | High | Strict species validation; native strains only; eDNA monitoring | Very Low | Immediate removal protocol if non-native species detected |
| Funding sustainability | Medium | High | Carbon credit revenue ($500–1,000/ha/yr); fishery partnerships; government grants | Medium | Diversify revenue streams; kelp harvest for bioplastics/biofuel |
| SCU loss (equipment failure) | Low-Medium | Low | Positive buoyancy failsafe; GPS beacon; mothership recovery protocol | Low | Insurance; fleet redundancy (N+2 units per SMP) |
| Data loss | Low | Low | Onboard storage (128 GB); satellite backup daily; mesh network redundancy | Very Low | Data recovery from surviving units |

---

*Specification v2.0 — Autonomous Kelp Forest Cultivator — 2026-06-16*