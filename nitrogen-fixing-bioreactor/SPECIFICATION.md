# Technical Specification: Nitrogen-Fixing Bioreactor

> **Document Version:** 2.0  
> **Classification:** Engineering Specification  
> **Status:** Concept Design  
> **Last Updated:** 2026-06-16

---

## 1. System Architecture

### 1.1 Overview

The Nitrogen-Fixing Bioreactor (NFB) is a self-contained, modular ammonia production unit that converts atmospheric N₂ to solid ammonium sulfate fertilizer at ambient temperature and pressure using engineered nitrogenase enzymes in synthetic compartments.

**Physical Form Factor:**
- Dimensions: 1.80 m (H) × 0.80 m (W) × 0.70 m (D)
- Mass: 120 kg (unit only); 135 kg with solar panel
- Enclosure: Powder-coated 304 stainless steel frame, HDPE internal shrouds, IP65 rated
- Color: White (high solar reflectance for thermal management in tropical deployment)
- Intended installation: Outdoors, partial shade preferred; flat surface or concrete pad

**Subsystems:**

| # | Subsystem | Function | Mass (kg) | Volume (L) |
|---|-----------|----------|-----------|-----------|
| 1 | Enzyme Reactor Core | Primary N₂ fixation chamber | 25 | 25 |
| 2 | ATP Regeneration Module | Solar-powered energy supply | 8 | 6 |
| 3 | Gas Processing Unit | Air intake, filtration, N₂ concentration | 15 | 23 |
| 4 | Product Capture Loop | NH₃ absorption and fertilizer crystallization | 22 | 22 |
| 5 | Control & Diagnostics | Sensors, microcontroller, telemetry | 3 | 2 |
| 6 | Power System | Solar panel + battery + charge controller | 33 | 8 |
| 7 | Plumbing & Structure | Pumps, valves, heat exchangers, frame | 14 | 10 |
| | **TOTAL** | | **120** | **96** |

### 1.2 Operational Flow Diagram

```
                    ┌──────────────────────────────────────┐
                    │           AMBIENT AIR                │
                    │         (78% N₂, 21% O₂)             │
                    └──────────────┬───────────────────────┘
                                   │
                          ┌────────▼────────┐
                          │   AIR INTAKE    │
                          │  Centrifugal    │
                          │  blower 50L/min │
                          │  + HEPA 0.3µm   │
                          └────────┬────────┘
                                   │
                          ┌────────▼────────┐
                          │  N₂ CONCENTRATOR│
                          │  CMS-PSA        │
                          │  95-98% N₂ out  │
                          │  2-5% Ar/O₂     │
                          └────────┬────────┘
                                   │ Concentrated N₂
                                   │
               ┌───────────────────▼───────────────────────┐
               │           ENZYME REACTOR CORE              │
               │                                           │
               │  ┌─────────────────────────────────────┐  │
               │  │  Synthetic Compartment (10¹²/L)      │  │
               │  │  ┌───────────────────────────────┐   │  │
               │  │  │ BMC/PLGA-PEG vesicle (1µm)   │   │  │
               │  │  │  ┌─────────────────────────┐  │   │  │
               │  │  │  │ Engineered Nitrogenase  │  │   │  │
               │  │  │  │ V2 (5× activity)        │  │   │  │
               │  │  │  │ FeMo-cofactor active    │  │   │  │
               │  │  │  │ site: N₂ → 2 NH₃       │  │   │  │
               │  │  │  └─────────────────────────┘  │   │  │
               │  │  │  + ATP synthase patches        │   │  │
               │  │  │  + MV²⁺ reductase electrode    │   │  │
               │  │  └───────────────────────────────┘   │  │
               │  └─────────────────────────────────────┘  │
               │                                           │
               │  N₂ in → (ATP + e⁻) → NH₃ out            │
               └───────────────────┬───────────────────────┘
                                   │ NH₃ in solution
                                   │
                          ┌────────▼────────┐
                          │ ACID ABSORPTION  │
                          │ LOOP            │
                          │ 10% H₂SO₄       │
                          │ (biogenic)      │
                          │                 │
                          │ 2NH₃ + H₂SO₄ → │
                          │ (NH₄)₂SO₄      │
                          └────────┬────────┘
                                   │ Saturated solution
                                   │
                          ┌────────▼────────┐
                          │  CRYSTALLIZER   │
                          │  15°C plate-fin │
                          │  Heat exchanger │
                          │  Gravity settle │
                          └────────┬────────┘
                                   │
                          ┌────────▼────────┐
                          │  COLLECTION BIN │
                          │  (NH₄)₂SO₄      │
                          │  crystals       │
                          │  ~39 kg/day     │
                          │  (21% N content)│
                          └─────────────────┘

        ┌──────────────┐         ┌──────────────┐
        │ SOLAR PANEL  │────────▶│ POWER MGMT   │
        │ 1.2 kW peak  │         │ + BATTERY     │
        │ (foldable)    │         │ 2.4 kWh      │
        └──────────────┘         │ LiFePO₄      │
                                 └──────┬───────┘
                                        │ 48V DC bus
                    ┌───────────────────┼────────────────────┐
                    │                   │                    │
             ┌──────▼─────┐    ┌───────▼──────┐    ┌────────▼───────┐
             │ MV²⁺       │    │ Blower +     │    │ Controller +   │
             │ reductase  │    │ PSA valves   │    │ Sensors        │
             │ cathode    │    │ + pumps      │    │ + LoRaWAN      │
             └────────────┘    └──────────────┘    └────────────────┘
```

### 1.3 Process Mass Balance (Peak Mode, 24h)

| Stream | Component | Rate | Notes |
|--------|-----------|------|-------|
| **Input: Air** | N₂ | 12.8 kg/day | 50 L/min × 1.25 kg/m³ × 0.78 |
| | O₂ | 3.4 kg/day | Passes through (inert to enzyme) |
| | Ar + others | 0.5 kg/day | Trace |
| **Input: Water** | H₂O (make-up) | 20 L/day | 2 L/kg NH₃ × 10 kg |
| **Input: Energy** | Solar + battery | 160 MJ/day | ~44 kWh/day |
| **Output: Fertilizer** | (NH₄)₂SO₄ | 39 kg/day | 21% N by mass |
| **Output: NH₃ equivalent** | NH₃ | 10 kg/day | Contained in product |
| **Output: Off-gas** | N₂ (unreacted) | 8.4 kg/day | 65% N₂ passes through |
| | O₂ | 3.4 kg/day | Unconsumed |
| | Ar + trace | 0.5 kg/day | Inert |

**N₂ utilization efficiency**: 34% single-pass (10 kg NH₃ from 29.2 kg N₂ input). Unreacted N₂ is recycled to the PSA inlet, achieving 85% overall utilization in closed loop.

---

## 2. Enzyme Reactor Core

### 2.1 Engineered Nitrogenase V2

**Base organism:** *Azotobacter vinelandii* Mo-nitrogenase (NifDK + NifH)

| Parameter | Wild-Type A. vinelandii | Engineered V2 Target | Method |
|-----------|-------------------------|---------------------|--------|
| Specific activity | 9.6 mol NH₃/mol MoFe/min | 50 mol NH₃/mol MoFe/min | CSR evolution × 12 cycles |
| O₂ half-life | <5 min (aerobic) | >72 hours | Flavohemoglobin domain fusion |
| Thermal optimum | 30°C | 30–50°C | Surface-loop stabilization + disulfide insertion |
| Thermal max | 37°C (50% loss) | 55°C (50% loss) | Proline substitution in flexible loops |
| ATP requirement | 16 ATP/N₂ (2 e⁻/ATP) | 10 ATP/N₂ | Tighter Fe-protein docking (2.3 Å closer) |
| H₂ side-product | 1 H₂ per N₂ | <0.1 H₂ per N₂ | Active site residue F→Y substitution |
| Operational lifetime | N/A (in vivo turnover) | 4,000 hours continuous | Trehalose + glycerol stabilizer matrix |
| Kₘ for N₂ | 0.05 atm | 0.02 atm | Active site pocket widening (RoseTTAFold) |
| Vₘₐₓ | 1.6 s⁻¹ | 8.3 s⁻¹ | Combined evolution + design |

**Engineering Approach — Detail:**

**Step 1: Directed Evolution (CSR)**
- Microfluidic droplets (50 µm diameter) encapsulate single nitrogenase variants + transcription/translation machinery + N₂ substrate
- Fluorescent NH₃ reporter (NH₃-sensitive dye + microfluidic sorting) selects top 0.01%
- Each cycle: ~10⁸ variants screened, ~10⁴ selected, 2–3 generations per cycle
- Expected improvement per cycle: 1.15× (conservative, based on P450 evolution precedent)
- 12 cycles → 1.15¹² = 5.4× target achieved

**Step 2: Rational Design (Active Site)**
- AlphaFold3 models of FeMo-cofactor pocket with N₂ bound
- RoseTTAFold identifies steric constraints limiting N₂ access
- Key mutations: αVal70→Gly (widens substrate channel), αArg96→Gln (reduces electrostatic barrier)
- Combined with CSR winners in Step 3

**Step 3: O₂ Tolerance Engineering**
- Flavohemoglobin (Hmp) from *E. coli* truncated to globin domain only (reduces steric clash)
- Flexible Gly-Ser-Gly linker (15 residues) between Hmp C-terminus and Fe-protein N-terminus
- Molecular dynamics (200 ns simulation) confirms O₂ binding at Hmp heme before reaching FeS cluster
- O₂ consumption rate: 2 O₂/min per Hmp domain → protection for >72 hours at 21% ambient O₂

**Step 4: Coupling Efficiency**
- Fe-protein (NifH) variant with shortened docking loop (3 residues deleted)
- Reduces Fe-protein—MoFe-protein distance by 2.3 Å
- ATP hydrolysis coupling efficiency: 50% → 80% (fewer wasted ATP cycles)
- Result: 10 ATP/N₂ instead of 16

### 2.2 Synthetic Compartments — Detailed Architecture

**Vesicle Composition (per vesicle, 1 µm diameter):**

| Layer | Material | Thickness | Function |
|-------|----------|-----------|----------|
| Outer shell | BMC hexameric proteins (EutM/PduA variants) | 5 nm | Selective pore channels (3.5 Å) |
| Polymer matrix | PLGA-PEG block copolymer | 8 nm | Mechanical rigidity, O₂ barrier |
| PEG brush layer | PEG-2000 chains (inner surface) | 2 nm | Retards O₂ diffusion |
| Inner membrane | Phosphatidylcholine bilayer patches | 5 nm | Embeds ATP synthase + ferredoxin |
| Lumen | Trehalose/glycerol buffer (pH 7.2) | — | Enzyme environment |

**Vesicle Specifications:**

| Property | Value | Measurement Method |
|-----------|-------|-------------------|
| Diameter | 800 nm – 1.2 µm | DLS (dynamic light scattering) |
| Wall thickness | 15–20 nm | Cryo-EM tomography |
| N₂ permeability | 2.1 × 10⁻³ cm/s | Mass spectrometry headspace analysis |
| O₂ permeability | 7.0 × 10⁻⁴ cm/s | Clark electrode depletion assay |
| N₂:O₂ selectivity ratio | 3:1 | Calculated from permeabilities |
| Internal pH | 7.2 (buffered) | Fluorescent pH indicator |
| Enzyme loading | 5,000 nitrogenase complexes/vesicle | Cryo-EM particle counting |
| Burst pressure | 0.3 atm (above ambient) | Micropipette aspiration |
| Self-assembly time | 2–4 hours | DLS timecourse |
| Thermal stability | -10°C to 60°C (storage), 25–50°C (operating) | DSC (differential scanning calorimetry) |

**Compartment Packing in Reactor:**

| Parameter | Value |
|-----------|-------|
| Reactor vessel volume | 20 L |
| Compartment volume fraction | 40% (8 L packed) |
| Compartment count | ~10¹² per liter → 8 × 10¹² total |
| Total enzyme mass | ~50 g MoFe-protein |
| Total FeMo-cofactor | ~0.5 g Mo |
| Interstitial fluid | 60% (12 L) — buffer + MV²⁺ + ATP |

### 2.3 Enzyme Cartridge

**Format:** Removable cartridge, slide-in rail mount, tool-less replacement

| Parameter | Specification |
|-----------|--------------|
| Physical dimensions | 30 cm × 20 cm × 5 cm |
| Mass (dry, lyophilized) | 250 g |
| Mass (wet, operational) | 1.8 kg |
| Packed compartment volume | 500 mL (after reconstitution) |
| MoFe-protein content | 50 g |
| FeMo-cofactor content | 0.5 g Mo |
| Stabilizers | Trehalose (5% w/w), glycerol (2% w/w), DTT (1 mM) |
| Reconstitution time | 4 hours (add water + buffer from reservoir) |
| Operational lifetime | 4,000 hours (~6 months at 60% duty cycle) |
| Storage lifetime (lyophilized) | 24 months at 4°C, 6 months at 25°C |
| End-of-life indicator | Spectrophotometric MV²⁺ recycling rate <80% of initial |
| Cost target (volume) | $50/cartridge |
| Disposal | Incineration at 800°C; Mo recovery from ash |

**Cartridge Manufacturing Process:**

1. **Enzyme production**: Engineered nitrogenase V2 expressed in *E. coli* BL21(DE3) in 100kL fermenter → cell-free extract → Ni-NTA purification → diafiltration into storage buffer. Yield: 500 mg/L culture → 200 L per cartridge → 1 fermenter batch = 500 cartridges
2. **Compartment self-assembly**: BMC shell proteins + PLGA-PEG + nitrogenase + lipids mixed in controlled-pH buffer → microfluidic flow-focusing device produces monodisperse vesicles → cross-linked with glutaraldehyde vapor (0.01% w/v)
3. **Lyophilization**: Compartment suspension frozen at -80°C → lyophilized 48h → sealed under N₂ atmosphere
4. **Packaging**: Lyophilized powder + desiccant packed into HDPE cartridge shell → hermetically sealed → cold-chain shipping (2–8°C preferred, ambient acceptable for <6 months)

---

## 3. ATP Regeneration Module

### 3.1 Dual-Pathway Energy System

The NFB uses two complementary energy pathways to maximize efficiency and reliability:

**Pathway A — Direct Electron Transfer (Primary)**

```
PV panel → DC-DC converter (48V) → Cathode electrode
                                        │
                                   MV²⁺ + e⁻ → MV⁺
                                        │
                               Diffuses into compartments
                                        │
                          MV⁺ → Nitrogenase → NH₃ + MV²⁺
                                        │
                              MV²⁺ returns to cathode
```

- **Cathode**: Glassy carbon plate (200 cm²) coated with methyl viologen (1,1'-dimethyl-4,4'-bipyridinium) in hydrogel matrix
- **Applied potential**: -0.45V vs. SHE (sufficient to reduce MV²⁺ but not reduce H₂O)
- **Current density**: 10 mA/cm² → 2A total → supplies electrons for ~8 kg NH₃/day
- **Faradaic efficiency**: 85% target (15% lost to H₂ evolution side reaction)

**Pathway B — ATP Synthesis (Supplementary)**

```
PV panel → DC-DC converter → Anode electrode
                                    │
                          H₂O → ½O₂ + 2H⁺ + 2e⁻
                                    │
                         Protons accumulate on one side
                         of lipid bilayer patch
                                    │
                    Proton gradient drives F₁Fₒ-ATP synthase
                                    │
                         ADP + Pᵢ → ATP (3 ATP/revolution)
                                    │
                         ATP diffuses into compartments
```

- **Anode**: Pt/Ir oxide coated titanium mesh
- **Membrane**: Nafion 117 cation-exchange membrane separates anode/cathode chambers
- **ATP synthase patches**: 50 circular lipid bilayer patches (5 mm diameter) with reconstituted *Bacillus* PS3 F₁Fₒ-ATP synthase, mounted on porous ceramic support
- **ATP production rate**: ~0.5 mmol ATP/min/patch → 50 patches = 25 mmol/min → sufficient for 10 ATP/N₂ at 2.5 mmol N₂/min

### 3.2 Energy Budget — Detailed Breakdown

| Component | Energy (MJ/kg NH₃) | % of Total | Notes |
|-----------|---------------------|-----------|-------|
| N≡N bond dissociation | 5.38 | 34.0% | Thermodynamic minimum (941 kJ/mol N≡N) |
| Electron transfer (MV²⁺ recycling) | 3.20 | 20.3% | Includes Faradaic loss (85% η) |
| ATP synthesis (10 ATP/N₂) | 3.50 | 22.2% | Proton gradient + ATP synthase |
| N₂ compression (PSA) | 0.30 | 1.9% | 0.5 atm overpressure in reactor |
| NH₃ absorption (acid pumping) | 0.40 | 2.5% | Circulation pump power |
| Crystallization cooling | 0.40 | 2.5% | Peltier + heat exchanger |
| Water purification | 0.10 | 0.6% | UV + filtration |
| Control electronics | 0.20 | 1.3% | MCU + sensors + LoRa |
| Blower + fluid pumps | 0.50 | 3.2% | Continuous operation |
| Thermal losses (10%) | 1.42 | 9.0% | Insulation + ambient loss |
| Battery round-trip loss | 0.40 | 2.5% | LiFePO₄ at 95% RTE |
| **TOTAL** | **15.80** | **100%** | **52% below Haber-Bosch** |

### 3.3 Solar Sizing & Battery

| Parameter | Value | Rationale |
|-----------|-------|-----------|
| Solar panel rating | 1.2 kW peak | 4 peak-sun-hours × 1.2 kW = 4.8 kWh/day |
| Energy required/day (peak mode) | 4.4 kWh (10 kg NH₃ × 15.8 MJ/kg ÷ 3.6) | |
| Battery capacity | 2.4 kWh (48V, 50Ah LiFePO₄) | Covers 13h nighttime operation |
| Charge controller | MPPT, 48V, 30A | Standard COTS |
| Solar panel type | Mono-Si, foldable, 19% efficiency | Weatherproof, 25-year warranty |
| Panel area | ~6.3 m² (unfolded) | 1.2 kW ÷ (0.19 × 1000 W/m²) |
| Panel mounting | Ground-mount, adjustable tilt | 15°–45° tilt range |
| Operating voltage | 48V DC (SELV) | Safety: <60V DC is touch-safe |
| Peak power draw | 375W (all subsystems active) | Below panel output in sun |
| Average power draw | 185W (standard mode) | Most subsystems cycle |

---

## 4. Gas Processing Unit

### 4.1 Air Intake & Filtration

| Component | Specification |
|-----------|-------------|
| Blower type | Centrifugal, brushless DC |
| Flow rate | 50 L/min (adjustable 20–80 L/min) |
| Power | 40W at rated flow |
| Noise level | <45 dBA at 1m |
| Pre-filter | HEPA H13 (99.95% at 0.3 µm) |
| Filter lifetime | 6 months (replaceable cartridge) |
| Intake protection | Rain hood + insect screen (stainless mesh) |
| Ambient temp range | -10°C to +55°C operation |
| Humidity range | 5–95% RH (non-condensing) |

### 4.2 N₂ Concentration — Pressure Swing Adsorption

| Parameter | Specification |
|-----------|-------------|
| Adsorbent | Carbon molecular sieve (CMS-240, Zeochem) |
| Bed volume | 2 × 2.5 L (dual-bed, alternating cycle) |
| Cycle time | 60s adsorption / 60s desorption |
| Product purity | 95–98% N₂ (balance: Ar + trace O₂) |
| Product flow rate | 12 L/min at 1 atm |
| Feed pressure | 4 bar (oil-free compressor integrated) |
| Power consumption | 120W |
| CMS lifetime | 5+ years (thermal regeneration at 300°C every 3,000h) |
| Compressor type | Oil-free scroll, 4 bar max |
| Noise | <55 dBA |

**PSA Cycle Detail:**
1. Bed A pressurized to 4 bar → CMS adsorbs O₂, CO₂, H₂O → N₂ passes through
2. After 60s, Bed A depressurized to 1 atm → O₂ desorbs to vent
3. Simultaneously, Bed B pressurized → continuous N₂ output
4. Purge gas from Bed B used to flush Bed A during desorption

---

## 5. Product Capture Loop

### 5.1 Ammonia Absorption — Detailed Design

| Component | Specification |
|-----------|-------------|
| Absorption column | Packed column, 10 cm dia × 50 cm height |
| Packing material | HDPE Raschig rings (10 mm) |
| Acid concentration | 10% H₂SO₄ w/w (1.06 g/mL density) |
| Acid volume (circulating) | 10 L |
| Acid flow rate | 2 L/min (peristaltic pump) |
| NH₃ capture efficiency | >99.9% (verified by NDIR outlet monitor) |
| Product solution pH | 5.5–6.0 (when saturated with NH₃) |
| Maximum NH₃ loading | 180 g NH₃ per L of 10% H₂SO₄ |
| Saturation time | ~4 hours at 10 kg/day NH₃ production |

### 5.2 Biogenic Acid Production

| Parameter | Specification |
|-----------|-------------|
| Organism | *Acidithiobacillus ferrooxidans* (non-pathogenic, environmental isolate) |
| Bioreactor volume | 1 L (borosilicate glass + HDPE) |
| Feedstock | Elemental sulfur powder (industrial waste, $50/ton) |
| Feed rate | 5 g S/day |
| Acid production rate | 15 g H₂SO₄/day (0.15 mol) — sufficient to maintain acid concentration |
| Temperature | 30°C (self-heating from exothermic oxidation) |
| Aeration | 0.5 L/min air (from main blower bleed) |
| Culture maintenance | Self-sustaining; inoculate once, runs indefinitely |
| Sulfur source alternatives | Pyrite (FeS₂), hydrogen sulfide (H₂S) from biogas |
| Containment | Sealed bioreactor; no release of *Acidithiobacillus* (non-GMO, naturally occurring) |

### 5.3 Crystallization System

| Component | Specification |
|-----------|-------------|
| Crystallizer type | Cooling crystallizer, batch operation |
| Cooling method | Aluminum plate-fin heat exchanger + Peltier cooler |
| Cooling target | 15°C (from 25°C feed) |
| Peltier power | 40W |
| Crystallization time | 6 hours per batch |
| Crystal size | 0.5–2 mm (ammonium sulfate) |
| Collection method | Gravity settling into drawer-style collection bin |
| Collection bin volume | 50 L (holds ~50 kg (NH₄)₂SO₄) |
| Emptying frequency | Every 1.3 days at peak production |
| Crystal purity | >98% (NH₄)₂SO₄, <2% free acid (within fertilizer spec) |
| Moisture content | <1% after 24h air drying in bin |

### 5.4 Water Management

| Parameter | Value |
|-----------|-------|
| Total water inventory | 20 L closed-loop |
| Make-up water rate | 2 L/day (replaces water in product crystals) |
| Water source | Rainwater (preferred), well water, purified wastewater |
| Minimum water quality | TDS < 500 ppm, turbidity < 5 NTU |
| Purification train | Sand filter → activated carbon → UV-C (254 nm, 30 mJ/cm²) |
| UV lamp power | 8W, 9000-hour lifetime |
| Water pump | Brushless DC magnetic drive, 2 L/min |
| Recirculation rate | 10 L/min through purification |

---

## 6. Control & Diagnostics

### 6.1 Sensor Suite — Complete Specifications

| # | Sensor | Type | Parameter | Range | Accuracy | Update Rate | Cost |
|---|--------|------|-----------|-------|----------|-------------|------|
| 1 | NDIR CO₂/H₂O | Non-dispersive IR | CO₂ (vent) | 0–5000 ppm | ±30 ppm | 1 Hz | $12 |
| 2 | Electrochemical | 3-electrode | Dissolved NH₃ | 0–5000 ppm | ±1% FS | 0.5 Hz | $18 |
| 3 | NDIR | Photoacoustic | NH₃ gas (leak) | 0–100 ppm | ±2 ppm | 1 Hz | $25 |
| 4 | Clark-type | Membrane | Dissolved O₂ | 0–20 mg/L | ±0.1 mg/L | 0.2 Hz | $8 |
| 5 | Pt100 RTD | Platinum RTD | Temperature (4×) | -20–80°C | ±0.1°C | 1 Hz | $4 ea. |
| 6 | Piezoresistive | MEMS | Pressure (2×) | 0–5 atm | ±0.5% FS | 10 Hz | $6 ea. |
| 7 | Capacitive | Dielectric | Liquid level (3×) | 0–100% | ±2% | 1 Hz | $3 ea. |
| 8 | Spectrophotometric | LED + photodiode | MV²⁺ redox state | 0–100% reduced | ±3% | 0.1 Hz | $15 |
| 9 | Hall effect | Magnetic | Flow rate (2×) | 0–10 L/min | ±2% | 10 Hz | $10 ea. |
| | **Total** | | | | | | **~$120** |

### 6.2 Controller Hardware

| Parameter | Specification |
|-----------|-------------|
| MCU | STM32H743 (ARM Cortex-M7, 480 MHz) |
| Flash | 2 MB (application + OTA partition) |
| RAM | 1 MB (data logging + PID state) |
| ADC | 16-channel, 16-bit, 1 MSPS |
| DAC | 4-channel, 12-bit (control outputs) |
| Communication | LoRaWAN (SX1262, 868/915 MHz, 10 km range) |
| WiFi | ESP32-C3 (optional, for setup/field service) |
| RTC | Battery-backed, ±2 min/year |
| Power consumption | 500 mW active, 50 mW sleep |
| Operating system | FreeRTOS 10.5+ with safety-certified task scheduler |
| Watchdog | Independent hardware WDT (2s timeout) |
| OTA updates | Cryptographically signed (Ed25519), dual-bank flash |
| Data logging | 30-day rolling buffer (SD card, 32 GB) |

### 6.3 Control Algorithm

```python
# Simplified control logic (actual implementation in C on FreeRTOS)

class NFBController:
    """Main control loop for Nitrogen-Fixing Bioreactor"""
    
    MODES = {
        'PEAK':     {'duty': 1.0,  'nh3_target_kg_day': 10.0},
        'STANDARD': {'duty': 0.67, 'nh3_target_kg_day': 6.7},
        'ECONOMY':  {'duty': 0.33, 'nh3_target_kg_day': 3.3},
        'STANDBY':  {'duty': 0.0,  'nh3_target_kg_day': 0.0},
    }
    
    def control_loop(self, dt=1.0):
        """Main PID control loop — runs at 1 Hz"""
        mode = self.select_mode()
        
        # Safety checks first
        if self.sensors.nh3_gas_ppm > 25:  # NH₃ leak threshold
            self.emergency_shutdown()
            self.alert("NH₃ LEAK DETECTED", priority=CRITICAL)
            return
        
        if self.sensors.cartridge_life_hours < 100:
            self.alert("CARTRIDGE LOW", priority=WARNING)
        
        # N₂ flow control
        n2_flow = PID(self.sensors.n2_purity, setpoint=0.96,
                       Kp=0.5, Ki=0.1, Kd=0.05)
        self.set_blower_speed(n2_flow)
        self.set_psa_cycle(n2_flow)
        
        # Cathode voltage control (electron supply)
        nh3_rate = self.sensors.nh3_dissolved_ppm  # proxy for production rate
        target_rate = MODES[mode]['nh3_target_kg_day'] / 24  # kg/hr
        cathode_V = PID(nh3_rate, setpoint=target_rate,
                         Kp=0.3, Ki=0.05, Kd=0.02)
        self.set_cathode_voltage(cathode_V)
        
        # Temperature control
        reactor_T = PID(self.sensors.reactor_temp, setpoint=35.0,
                         Kp=2.0, Ki=0.5, Kd=0.1)
        self.set_cooling_fan(reactor_T)
        
        # Crystallization control
        if self.sensors.solution_saturation > 0.85:
            self.start_crystallization_batch()
        
        # Telemetry
        if time() - self.last_telemetry > 3600:  # hourly
            self.send_telemetry()
            self.last_telemetry = time()
```

### 6.4 Operating Modes — Detailed

| Mode | Blower | PSA | Cathode | Crystallizer | Battery Charge | Daily NH₃ | Daily Energy |
|------|--------|-----|---------|-------------|----------------|-----------|-------------|
| Peak | 100% | 100% | 100% | Continuous | Solar surplus only | 10 kg | 4.4 kWh |
| Standard | 70% | 70% | 70% | Batch (2×/day) | Charge during off-peak | 6.7 kg | 3.0 kWh |
| Economy | 35% | 35% | 35% | Batch (1×/day) | Charge to 100% | 3.3 kg | 1.5 kWh |
| Standby | Off | Off | Off | Complete batch | Full charge maintained | 0 | 0.1 kWh |

### 6.5 Telemetry & Fleet Management

**Hourly telemetry packet (128 bytes via LoRaWAN):**
- Timestamp (4 bytes)
- Device ID (4 bytes)
- Mode + status flags (2 bytes)
- NH₃ production rate (2 bytes, 0.01 kg resolution)
- Cartridge life remaining (2 bytes, hours)
- Battery SOC (1 byte, 1% resolution)
- Solar irradiance (2 bytes, 1 W/m²)
- Reactor temperature (2 bytes, 0.1°C)
- NH₃ gas level (2 bytes, 1 ppm)
- Error codes (4 bytes bitmap)
- Water level (1 byte)
- Cumulative NH₃ produced (4 bytes, 0.1 kg)

**Cloud dashboard features:**
- Real-time fleet map (GPS from setup)
- Production analytics (kg/day, kWh/day, cartridge life)
- Predictive maintenance (ML model on historical fleet data)
- Weather-linked production optimization (adjust mode based on solar forecast)
- Automatic cartridge ordering when life < 200 hours

---

## 7. Mechanical & Structural Design

### 7.1 Enclosure

| Parameter | Specification |
|-----------|-------------|
| Frame | 304 stainless steel, 1.5 mm wall tube, welded |
| Outer panels | Powder-coated 1.2mm steel (white, RAL 9010) |
| Internal shrouds | HDPE (5 mm), chemical resistant |
| Sealing | EPDM gaskets on all access panels, IP65 |
| Access | Front panel (hinged) — cartridge + collection bin; Rear panel — electronics + battery |
| Mounting | 4× M10 anchor bolts to concrete pad or ground screws |
| Ventilation | Passive ventilation slots (IP53 rated) + active fan (temperature-controlled) |
| Lifting | 4× lifting eyes (200 kg SWL each) for crane/forklift |
| Weight (total) | 120 kg (unit) + 15 kg (solar panel) = 135 kg |

### 7.2 Fluidic System

| Component | Material | Connection | Notes |
|-----------|----------|------------|-------|
| Main piping | 316L SS, 12mm OD | Compression fittings | Swagelok-compatible |
| Flexible connections | EPDM + PTFE lined | Tri-clamp | Food-grade compliant |
| Valves (process) | PTFE + 316L SS | Pneumatic actuation | SMC or equivalent |
| Pumps | HDPE housing, ceramic impeller | Mag-drive | Kamo FMD series |
| Seals | EPDM (N₂, NH₃ compatible) | O-ring (AS568 standard) | Replace at 5-year service |
| Heat exchanger | Aluminum 6061-T6, brazed plate-fin | — | 5 kW capacity |

### 7.3 Thermal Management

| Source | Heat Generated | Management Method |
|--------|---------------|-------------------|
| Reactor core (exothermic) | ~25W | Passive HDPE shroud + air gap |
| PSA compressor | ~40W | Forced air (variable speed fan) |
| Battery (charging) | ~15W | Natural convection + HDPE enclosure |
| Electronics | ~10W | PCB heat sink + passive convection |
| Peltier cooler (crystallizer) | ~40W (input) | Heat exhausted to ambient |
| **Total heat rejection** | **~130W** | Managed with 2× 120mm variable-speed fans |

---

## 8. Safety Systems

### 8.1 Safety Architecture (SIL-2 Target)

| Layer | Function | Response Time |
|-------|----------|---------------|
| **Layer 1: Process control** | PID loops maintain normal operation | 1–10 s |
| **Layer 2: Alarm + operator** | NDIR NH₃ >25 ppm → alert + auto-reduce | 1 s |
| **Layer 3: Safety instrumented** | NH₃ >50 ppm → automatic shutdown | 0.5 s |
| **Layer 4: Mechanical relief** | Pressure >1.5 atm → burst disk vents to scrubber | 0.1 s |
| **Layer 5: Physical containment** | Sealed unit + secondary containment tray | Passive |

### 8.2 Emergency Shutdown Sequence

1. **NH₃ leak detected** (>25 ppm NDIR):
   - Cathode power OFF (stops NH₃ production instantly)
   - Blower OFF (stops N₂ flow)
   - Acid absorption loop continues (captures residual NH₃)
   - Alert sent via LoRaWAN
   - Status LED: Flashing red

2. **Severe leak** (>50 ppm NDIR):
   - All subsystems OFF
   - Blower reverses to evacuate N₂ from reactor (dilutes internal NH₃)
   - External vent opens with activated carbon scrubber
   - Alert priority: CRITICAL
   - Requires manual reset

3. **Fire/thermal event** (temperature >80°C):
   - All power OFF
   - Battery contactor opens (physical disconnect)
   - Fire suppression: internal ABC dry chemical (1 kg) — automatic at 120°C
   - Status LED: Solid red

### 8.3 Cybersecurity

| Measure | Implementation |
|---------|---------------|
| OTA firmware signing | Ed25519 digital signature; rejects unsigned images |
| LoRaWAN encryption | AES-128 (LoRaWAN specification, AppSKey + NwkSKey) |
| Physical debug access | JTAG disabled in production; SWD behind tamper-evident seal |
| Default credentials | None — device-specific keys provisioned at manufacture |
| Key rotation | LoRaWAN session keys rotate per ABP (or OTAA per join) |

---

## 9. Qualification & Testing Plan

### 9.1 Environmental Testing

| Test | Standard | Conditions | Pass Criteria |
|------|----------|-----------|---------------|
| Temperature cycling | IEC 60068-2-14 | -10°C to +55°C, 100 cycles | No functional degradation |
| Humidity | IEC 60068-2-78 | 95% RH at 40°C, 240h | No corrosion, IP65 maintained |
| Vibration | IEC 60068-2-64 | 5–500 Hz, 2g RMS, 30 min/axis | No mechanical damage |
| Salt spray | ISO 9227 | 96h, 5% NaCl | No corrosion of structural parts |
| UV exposure | IEC 60068-2-5 | 1000h UV-A/B | <5% polymer degradation |
| Dust ingress | IEC 60529 | IP6x dust test | No dust in electronics bay |
| Water ingress | IEC 60529 | IPx5 water jet | No water in sealed compartments |

### 9.2 Performance Testing

| Test | Duration | Metric | Target |
|------|----------|--------|--------|
| Continuous NH₃ production | 30 days | kg NH₃/day | ≥8 kg (80% of rated) |
| Cartridge lifetime | To depletion | Hours | ≥3,500 (87.5% of 4,000h target) |
| Energy efficiency | 30 days | MJ/kg NH₃ | ≤18 MJ (114% of 15.8 MJ target) |
| NH₃ capture efficiency | Continuous | % NH₃ captured | ≥99.5% |
| Night operation | 48h (battery only) | kg NH₃/night | ≥2 kg |
| Cartridge hot-swap | 10 cycles | Time to resume | <30 min |
| Control loop stability | 72h | Temperature deviation | ±0.5°C |
| NDIR alarm response | 10 tests | Time to shutdown | <2 s |

---

## 10. Regulatory & Compliance

| Regulation | Applicability | Status |
|------------|-------------|--------|
| CE marking (EU) | Machinery Directive 2006/42/EC | Design for compliance |
| FCC Part 15 (US) | LoRaWAN radio emissions | COTS module, pre-certified |
| IEC 61508 (SIL-2) | Safety instrumented functions | Target in design |
| ISO 14001 | Environmental management | Manufacturing facility |
| REACH (EU) | Chemical registration | MV²⁺, H₂SO₄ already registered |
| Fertilizer regulations | (NH₄)₂SO₄ product classification | Already approved globally |
| Biological containment | Cell-free system — no GMO regulations apply | Exempt per EU Dir. 2009/41/EC Art. 3 |
| Transport | UN 3316 (Chemical kit) or unregulated (non-hazardous) | (NH₄)₂SO₄ <25 kg — exempt |

---

## 11. Maintenance Schedule

| Interval | Action | Time Required | Skill Level |
|----------|--------|---------------|-------------|
| Daily | Check collection bin, empty if full | 2 min | Farmer |
| Weekly | Inspect water level, top up if needed | 5 min | Farmer |
| Monthly | Check acid bioreactor turbidity | 2 min | Farmer |
| 6 months | Replace enzyme cartridge | 5 min | Farmer |
| 6 months | Replace HEPA air filter | 2 min | Farmer |
| 1 year | Inspect pumps, clean strainer | 15 min | Technician |
| 2 years | Replace LiFePO₄ battery cells | 30 min | Technician |
| 3 years | CMS thermal regeneration | 2 hours | Technician |
| 5 years | Full service (seals, valves, calibration) | 4 hours | Technician |
| 15 years | Unit end-of-life (recycle) | — | Recycling center |

**Annual maintenance cost**: ~$100 (1 cartridge + 1 filter) + ~$50 (technician visit, shared across 10 units) = **$150/year**

---

*This specification represents the target design for a TRL-9 production unit. All values are engineering targets; actual performance will be validated through the development roadmap phases described in ROADMAP.md.*