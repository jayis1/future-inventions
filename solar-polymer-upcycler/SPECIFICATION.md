# Solar-Polymer Upcycler — Engineering Specification

**Document Version:** 2.0 (Enhanced)
**Classification:** Engineering Reference
**System Designation:** SPU-500 (500 kg/day community unit)

---

## 1. System Overview

### 1.1 Design Philosophy

The SPU-500 is designed as a **self-contained, solar-powered chemical recycling plant** in a standard 40-ft high-cube shipping container. All processing, energy, and control systems are integrated into the container shell with external CPC and PV arrays. The system requires only:
- **Feedstock**: Mixed plastic waste (any composition)
- **Solar access**: 4+ kWh/m²/day insolation (covers 90%+ of populated land area)
- **Water**: 50 L/day makeup (recirculated at 98% recovery)
- **Operators**: 2–3 trained personnel

### 1.2 Design Lifetime

| Component | Lifetime | Replacement Cycle |
|-----------|----------|-------------------|
| Container + structural | 25 years | N/A |
| Reactor vessel (316L SS, SiC-lined) | 15 years | N/A |
| MOF catalyst (MOF-808-DP) | 5 years | 500+ regen cycles; <5% activity loss |
| Enzyme cartridges | 2,000 hours | ~6 months continuous; hot-swap |
| CPC reflectors | 15 years | Recoat every 5 years |
| PV panels | 25 years | N/A |
| LFP battery | 10 years | 1 replacement in system life |
| Pumps, valves | 10 years | Seal replacement every 3 years |
| Controls electronics | 10 years | Firmware updates OTA |
| Distillation packing | 15 years | Clean every 2 years |

---

## 2. Feedstock Specifications

### 2.1 Acceptable Feedstock

| Polymer | CAS # | Density (g/cm³) | % in Typical MSW | SPU Conversion |
|---------|-------|-----------------|-------------------|----------------|
| HDPE | 9002-88-4 | 0.94–0.97 | 15–20% | >85% |
| LDPE/LLDPE | 9002-88-4 | 0.91–0.94 | 15–20% | >85% |
| PP | 9003-07-0 | 0.90–0.91 | 20–25% | >85% |
| PET | 25038-59-9 | 1.38 | 10–15% | >95% |
| PS/EPS | 9003-53-6 | 1.04–1.05 | 8–12% | >90% |
| PLA | 9006-61-1 | 1.24 | 1–3% (growing) | >90% |
| Nylon-6 | 63428-83-1 | 1.13–1.15 | 1–3% | >80% |
| Multi-layer (PE/PP/PET/foil) | Various | Various | 10–20% | >70% |

### 2.2 Contaminant Tolerance

| Contaminant | Max Acceptable Level | Removal Method |
|-------------|---------------------|----------------|
| Food residue | Up to 20% by mass | Ultrasonic wash |
| Paper/cardboard | Up to 15% by mass | Density separation (floats off) |
| Metals (Fe, Al) | Up to 5% by mass | Eddy-current + magnetic separation |
| Glass | Up to 5% by mass | Density separation |
| PVC | Up to 10% by mass | CaO dechlorination trap |
| Textiles/cloth | Up to 10% by mass | Pre-shred screening |
| Rubber/silicone | Up to 5% by mass | Inert residue (<2% of input) |
| Moisture | Up to 30% by mass | Pre-dry stage |
| Mineral fillers (CaCO₃, TiO₂) | Up to 20% in polymer | Inert; accumulates as residue |

### 2.3 Rejected Feedstock

- PET bottles >5 cm unshredded (jam shredder)
- Batteries (Li-ion risk — must be removed manually)
- Medical sharps (biohazard — must be autoclaved separately)
- Radioactive materials

---

## 3. Subsystem Specifications

### 3.1 Feedstock Preparation Module

**3.1.1 Shredder**

| Parameter | Specification |
|-----------|--------------|
| Type | Dual-shaft, slow-speed |
| Motor | 15 kW, 3-phase, 415V (or 220V single-phase option) |
| Throughput | 500 kg/h (continuous) |
| Output size | 3–5 mm flakes (screen-selected) |
| Blade material | D2 tool steel, hardened to 60 HRC |
| Blade life | 2,000 hours before resharpening |
| Noise | <75 dB at 1 m (sound-dampened enclosure) |
| Safety | Automatic reverse on jam; interlocked access door |

**3.1.2 Ultrasonic Wash**

| Parameter | Specification |
|-----------|--------------|
| Tank volume | 200 L recirculating |
| Ultrasonic frequency | 20 kHz |
| Ultrasonic power | 2 kW (4 × 500 W transducers) |
| Wash temperature | 40–50 °C (solar-preheated) |
| Residence time | 5–10 min per batch |
| Detergent | None required (cavitation cleaning) |
| Water recovery | 98% (0.1 µm PVDF crossflow membrane) |
| Makeup water | 50 L/day (4 L/tonne processed) |
| Organic removal | >95% (gravimetric) |

**3.1.3 Contaminant Separation**

| Stage | Method | Target | Efficiency |
|-------|--------|--------|------------|
| Ferrous metals | Overband magnetic separator | Fe, Ni | >99% |
| Nonferrous metals | Eddy-current separator | Al, Cu, Zn | >95% |
| Dense contaminants | Sink-float tank (water) | Glass, stone, ceramic | >90% |
| Light contaminants | Air classification | Paper, film, fiber | >85% |

**3.1.4 Pre-Dryer**

| Parameter | Specification |
|-----------|--------------|
| Type | Rotary drum, indirect-heated |
| Heat source | CPC waste heat + PV-powered heater |
| Temperature | 80–100 °C |
| Residence time | 10–15 min |
| Output moisture | <2% by mass |
| Vapor handling | Condensate recovery → wash water makeup |

### 3.2 Photothermal Reactor Module

**3.2.1 CPC Solar Concentrator**

| Parameter | Specification |
|-----------|--------------|
| Type | Compound parabolic concentrator (non-tracking) |
| Aperture area | 50 m² (5 modules × 10 m²) |
| Geometric concentration | 20× (aperture/absorber ratio) |
| Acceptance half-angle | 23.5° (accepts ±seasonal variation) |
| Reflector material | Anodized Al, 95% reflectance |
| Absorber tube | SiC-coated 316L SS, 50 mm OD |
| Absorber coating | MOF-808-DP (spray-coated, >92% α, <10% ε) |
| Working fluid | Therminol VP-1 (or mineral oil for lower cost) |
| Stagnation temperature | 320 °C (safety-limited) |
| Tracking | None (CPC design eliminates tracking requirement) |

**3.2.2 Reactor Vessel**

| Parameter | Specification |
|-----------|--------------|
| Type | Multi-zone tubular flow reactor |
| Material | 316L SS, SiC-lined (2 mm liner) |
| Tube count | 12 tubes, 50 mm ID, 6 m length |
| Zone 1 (Enzymatic) | 6 tubes, 60–150 °C |
| Zone 2 (Lewis-Acid) | 6 tubes, 180–250 °C |
| Operating pressure | 1–5 bar (N₂ blanket) |
| Design pressure | 10 bar (ASME VIII Div. 1) |
| Pressure test | 15 bar hydrostatic |
| Insulation | 100 mm calcium silicate + Al cladding |
| Heat loss | <50 W/m at design conditions |

**3.2.3 MOF-808-DP Catalyst**

| Property | Specification |
|----------|--------------|
| Framework | Zr₆O₄(OH)₄ + BTC/sulfonated-BTC linkers |
| BET surface area | >1,500 m²/g |
| Pore volume | 0.8 cm³/g (total), 0.3 cm³/g (mesopores) |
| Particle size | 100–500 µm (extruded pellet) |
| Bulk density | 0.6 g/cm³ (packed bed) |
| Total loading | 120 kg (4 × 30 kg cartridges) |
| Pellet crush strength | >10 N (sufficient for fixed bed) |
| Photothermal α | >0.92 (300–2500 nm) |
| Photothermal ε | <0.10 (2.5–25 µm, selective) |
| Thermal stability | 400 °C in N₂ (TGA onset) |
| Hydrothermal stability | >300 °C, <5% degradation after 100h steam |
| Regeneration cycles | >500 with <5% activity loss |
| Shelf life | 3 years (sealed, desiccated) |

**3.2.4 Enzyme Cartridge**

| Property | Specification |
|----------|--------------|
| Enzyme | PHL7 variant (8–12 stabilizing mutations) |
| T₁ₘ (free) | 72 °C (wild type) → 85+ °C (engineered) |
| T₁ₘ (MOF-confined) | Effective 90+ °C (scaffold stabilization) |
| Loading | 5 wt% on MOF (5 g enzyme / 100 g MOF) |
| Immobilization | Covalent via glutaraldehyde on -NH₂ sites |
| Activity (PET film) | >5 mg TPA/h/g MOF at 65 °C |
| Cartridge lifetime | 2,000 operating hours |
| Cartridge mass | 7.5 kg (30 kg MOF + enzyme) |
| Hot-swap time | 30 min (while reactor operates on Zone 2) |
| Storage | 4 °C, desiccated; 12-month shelf life |

**3.2.5 Thermal Energy Storage**

| Parameter | Specification |
|-----------|--------------|
| PCM | NaNO₃-KNO₃ eutectic (54–46 wt%) |
| Melting point | 222 °C |
| Latent heat | 100 kJ/kg |
| Mass | 200 kg |
| Energy stored | 20 MJ (5.6 kWh_thermal) |
| Buffer duration | 4 hours at Zone 2 operating temp |
| Container | 316L SS, insulated, internal heat exchanger |

**3.2.6 Dechlorination Trap (PVC Handling)**

| Parameter | Specification |
|-----------|--------------|
| Sorbent | CaO (quicklime), 50 kg cartridge |
| Capacity | ~20 kg HCl absorbed per cartridge |
| PVC capacity | ~200 kg PVC (5–7% of 3 tonnes processed) |
| Byproduct | CaCl₂ (non-hazardous, road salt grade) |
| Cartridge life | ~6 days continuous (at 5% PVC feed) |
| Replacement | Hot-swap, 15 min |

### 3.3 Monomer Separation Module

**3.3.1 Fractional Distillation Column**

| Parameter | Specification |
|-----------|--------------|
| Type | 6-stage bubble-cap |
| Material | 316L SS |
| Height | 3 m |
| Diameter | 300 mm |
| Reboiler | Solar-heated (CPC + PCM backup) |
| Condenser | Air-cooled (PV-powered fans) |
| Reflux ratio | 2:1 to 5:1 (adjustable per product) |
| Operating pressure | Atmospheric to 0.5 bar (vacuum option) |

**3.3.2 Gas Membrane Separator**

| Parameter | Specification |
|-----------|--------------|
| Type | Polyimide hollow-fiber |
| Feed | C₂–C₃ gas mixture (ethylene, propylene, methane, N₂) |
| Selectivity (C₃H₆/C₂H₄) | >3.5 |
| Operating pressure | 10–20 bar (PV-powered compressor) |
| Module size | 4″ × 30″ cartridge |
| Cartridge life | 10,000 hours |
| Product purity | C₂H₄ >99.5%, C₃H₆ >99.2% |

**3.3.3 Solid Recovery (TPA)**

| Parameter | Specification |
|-----------|--------------|
| Method | Vacuum filtration from aqueous phase |
| Filter | Continuous rotary vacuum filter, PTFE cloth |
| Wash | Deionized water (recycled) |
| Dry | Solar/air tray dryer |
| Purity | >99.5% TPA (by HPLC) |
| Yield | >95% of theoretical |

**3.3.4 Product Specifications**

| Monomer | Purity (min) | Key Impurity Limits | Storage | Market Price (2024) |
|---------|-------------|---------------------|---------|---------------------|
| Ethylene | 99.5% | C₃ <0.3%, CH₄ <0.1% | 20 bar cylinder | $0.80–1.20/kg |
| Propylene | 99.2% | C₂ <0.5%, C₄ <0.2% | 20 bar cylinder | $0.90–1.30/kg |
| Styrene | 99.0% | TBC 10–20 ppm (inhibitor) | Sealed drum, 4°C | $1.20–1.80/kg |
| TPA | 99.5% | 4-CBA <25 ppm | Sealed bag, dry | $0.80–1.10/kg |
| Caprolactam | 98.5% | Cyclohexanone oxime <0.5% | Sealed drum | $1.50–2.20/kg |
| Ethylene glycol | 99.0% | DEG <0.5% | Sealed drum | $0.50–0.80/kg |

### 3.4 Catalyst Regeneration Module

| Parameter | Specification |
|-----------|--------------|
| Trigger | Activity <90% baseline (FTIR-monitored) or 50–100 h elapsed |
| Purge | N₂ flow, 5 L/min, 10 min |
| Oxidation | Air/N₂ (5% O₂), 300 °C, 30 min |
| Cool-down | N₂ purge to <150 °C, 15 min |
| Resume | Automatic; enzyme zone bypassed during regen |
| Monitoring | In-situ XRD (Mo Kα), FTIR (coke C-H stretch), ΔP (bed integrity) |
| Cycle time | ~1 hour total |
| MOF degradation | <5% after 500 cycles |
| Energy source | CPC thermal (no external fuel) |

### 3.5 Energy & Control Module

**3.5.1 Photovoltaic System**

| Parameter | Specification |
|-----------|--------------|
| Panel type | Mono PERC, 550 W each |
| Array | 16 panels = 8.8 kWp |
| MPPT controller | 2 × 4 kW, 48 V |
| Mounting | Ground-mounted, fixed tilt (latitude angle) |
| Annual yield | 12,000–18,000 kWh (location-dependent) |

**3.5.2 Battery System**

| Parameter | Specification |
|-----------|--------------|
| Type | LFP (LiFePO₄) |
| Capacity | 20 kWh (48 V, 416 Ah) |
| Cycle life | 6,000+ at 80% DoD |
| Charging | Solar + grid (optional backup) |
| Autonomy | 24 hours for controls; 4 hours for full operation |

**3.5.3 Control System**

| Parameter | Specification |
|-----------|--------------|
| PLC | Custom shield on Raspberry Pi 5 (8 GB) |
| OS | Linux (real-time PREEMPT kernel) |
| Sensors | 12 × Type K thermocouples, 6 × 0–10 bar pressure transducers, 4 × Coriolis flow meters, 1 × NDIR gas analyzer (C₂H₄, C₃H₆, CO, CO₂) |
| Control loops | 8 PID loops (reactor temp ×2, pressure, flow ×3, distillation, wash) |
| Safety interlocks | 12 hardwired (over-temp, over-pressure, gas leak, door open) |
| Data logging | 1 Hz sampling, 30-day local buffer |
| Remote access | 4G/Starlink, VPN, encrypted |
| Dashboard | Grafana (open-source), responsive web UI |
| API | RESTful API for fleet management integration |
| OTA updates | Signed firmware updates, rollback capability |

**3.5.4 Safety System**

| Parameter | Specification |
|-----------|--------------|
| Gas detection | NDIR (ethylene, propylene), auto-shutdown at 10% LEL |
| Fire suppression | N₂ flooding (5 bar, 30 s discharge, 20 L N₂) |
| Pressure relief | Burst discs, 7 bar (all vessels) |
| Emergency stop | 3 × mushroom-head E-stops (container exterior) |
| Ventilation | Forced-air, 6 ACH, ATEX-rated fan |
| Spill containment | 200 L drip tray under reactor + separation module |
| Noise | <75 dB at 1 m (shredder enclosure, sound-dampened) |
| Access | Interlocked doors (reactor stops when opened) |

---

## 4. Process Performance

### 4.1 Mass Balance (Typical 500 kg/day Input)

| Stream | Mass (kg/day) | Composition |
|--------|---------------|-------------|
| **Input** | **500** | Mixed plastic + contaminants |
| Contaminants removed (wash/sep) | 50 | Food waste, paper, metals, glass |
| PVC (dechlorinated) | 15 | CaCl₂ (20 kg) to residue |
| **Net polymer to reactor** | **435** | PE/PP/PET/PS/nylon/others |
| Ethylene | 52 | From PE depolymerization |
| Propylene | 65 | From PP depolymerization |
| Styrene | 39 | From PS depolymerization |
| TPA | 48 | From PET depolymerization |
| Ethylene glycol | 16 | From PET depolymerization |
| Caprolactam | 9 | From nylon depolymerization |
| Lactic acid | 4 | From PLA depolymerization |
| Mixed oligomers (saleable) | 30 | Partial depolymerization products |
| Inert residue | 5 | Fillers, pigments, ash |
| Unreacted polymer | 12 | Sent to reprocess |
| **Total recovered** | **268** | **61.6% of input mass as monomers** |
| **Total saleable** | **298** | **68.5% including mixed oligomers** |

*Note: 61.6% monomer recovery from unsorted mixed waste far exceeds any existing technology. Pyrolysis yields ~30–40% usable products from mixed waste.*

### 4.2 Energy Balance (Sunny Day, 7 kWh/m²/day insolation)

| Stream | Energy (kWh/day) |
|--------|-----------------|
| **Solar thermal input (CPC)** | **700** (50 m² × 20× × 7 kWh/m² × 0.92) |
| Reactor heating | 450 |
| Distillation reboiler | 150 |
| PCM charging | 50 |
| Thermal losses | 50 |
| **Solar electric input (PV)** | **56** (8 kWp × 7 h × 1.0) |
| Shredder | 22 |
| Pumps + blowers | 15 |
| Controls + sensors | 4 |
| Compressor | 10 |
| Battery charging | 5 |
| **Total solar input** | **756** |
| **Total energy demand** | **706** |
| **Surplus** | **+50 kWh/day** (stored or exported) |

### 4.3 Water Balance

| Stream | Volume (L/day) |
|--------|---------------|
| Makeup water | 50 |
| Wash water recirculated | 9,800 (98% recovery) |
| Wash water discharged | 10 (to evaporator or sewer) |
| Pre-dryer condensate recovered | 30 |
| Net makeup required | 50 |

---

## 5. Quality Assurance

### 5.1 Product Quality Testing

| Test | Method | Frequency | Standard |
|------|--------|-----------|----------|
| Monomer purity | GC-MS (gas), HPLC (liquid) | Every 8 hours | ASTM D5307 |
| TPA purity | HPLC (4-CBA assay) | Every 8 hours | ASTM D7231 |
| Residual catalyst in product | ICP-MS (Zr) | Every 24 hours | Internal |
| Moisture content | Karl Fischer | Every 8 hours | ASTM D6304 |
| Color (styrene, EG) | APHA/Pt-Co | Every 8 hours | ASTM D1209 |

### 5.2 Catalyst Quality Testing

| Test | Method | Frequency |
|------|--------|-----------|
| BET surface area | N₂ adsorption (77 K) | Monthly |
| PXRD phase purity | Cu Kα diffraction | Monthly |
| Enzyme activity | pNPB hydrolysis assay | Per cartridge |
| Coke loading | TGA (air, 600 °C) | Post-regeneration |
| Metal leaching | ICP-MS of process stream | Monthly |

---

## 6. Installation Requirements

### 6.1 Site Requirements

| Requirement | Specification |
|-------------|--------------|
| Ground area | 150 m² (12 m × 2.5 m container + 50 m² CPC + 40 m² PV + access) |
| Foundation | Level concrete pad (12 m × 3 m, 150 mm thick) or compacted gravel |
| Solar access | No shading on CPC/PV arrays 9 AM–3 PM |
| Insolation | Min. 4 kWh/m²/day annual average |
| Water supply | 50 L/day potable or non-potable |
| Communications | 4G or satellite (Starlink) |
| Road access | Standard truck (40-ft container delivery) |
| Permits | Varies by jurisdiction; typically <5 bar operation → low-hazard classification |

### 6.2 Climate Operating Range

| Condition | Range |
|-----------|-------|
| Ambient temperature | -10 °C to +50 °C |
| Relative humidity | 0–100% (non-condensing for electronics) |
| Wind | CPC rated to 120 km/h; auto-stow at 90 km/h |
| Rain | All-weather container; IP65 electronics |
| Seismic | Zone 3 (IBC); container anchoring kit available |
| Altitude | Sea level to 2,500 m (de-rate PV output >1,500 m) |

---

## 7. Maintenance Schedule

| Interval | Task | Duration | Skill Level |
|----------|------|----------|-------------|
| Daily | Visual inspection, log readings | 15 min | Operator |
| Weekly | Check water quality, top up if needed | 30 min | Operator |
| Monthly | Clean CPC reflectors, inspect shredder blades | 2 h | Technician |
| Quarterly | Full catalyst assessment (BET, PXRD) | 4 h | Technician |
| Biannual | Replace enzyme cartridges (2× year) | 1 h | Operator |
| Annual | Full system service: pump seals, valve packing, calibrate sensors | 8 h | Technician |
| 3-year | Battery health check, major component inspection | 16 h | Engineer |
| 5-year | Replace MOF catalyst bed (if activity <80%) | 4 h | Technician |

---

## 8. Shipping & Logistics

| Parameter | Specification |
|-----------|--------------|
| Shipping configuration | Standard 40-ft HC container (loaded) |
| Gross weight | 12,000 kg (operational) |
| CPC/PV array | Packed inside container during shipping |
| Setup time | 2–3 days (2 technicians + 4 laborers) |
| Commissioning | 1 day (system check, calibration, first run) |
| Total deployment | 4–5 days from delivery to first monomer output |