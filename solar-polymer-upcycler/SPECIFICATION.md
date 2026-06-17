# Solar-Polymer Upcycler — Technical Specification

## System Architecture

### Overall Dimensions
- **Footprint**: 12 m × 2.5 m × 2.9 m (standard 40-ft shipping container)
- **Weight**: 8,500 kg (empty); 12,000 kg (operational)
- **Throughput**: 500 kg mixed plastic waste / day (20.8 kg/hour average)
- **Solar input**: 50 m² CPC array (ground-mounted, adjacent to container)

### Subsystem 1: Feedstock Preparation
| Component | Specification |
|-----------|-------------|
| Shredder | Dual-shaft, 15 kW, 500 kg/h, output 3–5 mm flakes |
| Ultrasonic wash | 20 kHz, 2 kW, 200 L recirculating tank, >95% organic removal |
| Water recycling | Membrane filtration (0.1 µm PVDF), 98% water recovery |
| Metal/contaminant separator | Eddy-current + density separation, >99% removal |

### Subsystem 2: Photothermal Reactor
| Parameter | Value |
|-----------|-------|
| Reactor type | Multi-stage tubular flow reactor (316L SS, SiC-lined) |
| MOF catalyst | Zr₆-MOF-808 derivative with -SO₃H and -NH₂ functionalization |
| MOF loading | 120 kg (fixed bed, 4 interchangeable cartridges) |
| Enzyme sites | Engineered PHL7 variant (T₁ₘ > 85 °C), covalently anchored via glutaraldehyde linkers on MOF mesopores (2–5 nm) |
| Operating temp | Zone 1: 60–150 °C (enzymatic cascade); Zone 2: 180–250 °C (Lewis-acid catalysis) |
| Operating pressure | 1–5 bar (N₂ blanket, oxygen-free) |
| Residence time | 15–45 min (polymer-dependent) |
| CPC concentration | 20× geometric concentration, 50 m² aperture |
| Solar absorptance | >92% (300–2500 nm, MOF-coated absorber tube) |
| Thermal storage | 200 kg phase-change salt (NaNO₃-KNO₃ eutectic, m.p. 222 °C) for 4-hour buffer |

### Subsystem 3: Monomer Separation
| Component | Specification |
|-----------|-------------|
| Fractional distillation | 6-stage bubble-cap column, solar-heated reboiler |
| Gas separator | Polyimide hollow-fiber membrane (ethylene/propylene split) |
| Liquid separator | Centrifugal + gravity settling, 3 fractions |
| Solid precipitator | Continuous vacuum filter (TPA recovery, >98% purity) |
| Monomer purities | Ethylene >99.5%, Propylene >99.2%, Styrene >99.0%, TPA >99.5%, Caprolactam >98.5% |

### Subsystem 4: Catalyst Regeneration
| Cycle | Every 50–100 operating hours |
| Method | Solar-thermal oxidative purge: 300 °C, air/N₂ mix, 30 min |
| MOF stability | >500 regeneration cycles with <5% activity loss |
| Enzyme replenishment | Re-immobilization cartridge swap (every 2,000 hours) |
| In-situ monitoring | XRD (phase), FTIR (coke detection), pressure drop (bed integrity) |

### Subsystem 5: Energy & Control
| Component | Specification |
|-----------|-------------|
| PV array | 8 kW peak (bypass diodes, MPPT controller) — powers pumps, blowers, controls |
| Battery | 20 kWh LFP battery, 1-day autonomy for controls |
| Thermal buffer | 200 kg nitrate salt PCM → 4 h operation after sunset |
| Control system | Raspberry Pi 5 + custom PLC; 12 thermocouples, 6 pressure transducers, flow meters, gas analyzer (NDIR) |
| Connectivity | 4G/Starlink for remote monitoring; open-source dashboard |

## Catalyst Design: MOF-808-DP

### Structure
- **Framework**: Zr₆O₄(OH)₄ nodes + 1,3,5-benzenetricarboxylate (BTC) linkers (MOF-808 topology)
- **Modification**: 30% of BTC linkers replaced by 2-sulfoterephthalic acid (introduces -SO₃H Brønsted acid sites)
- **Post-synthetic functionalization**: Ethylenediamine grafted on open Zr sites (introduces -NH₂ Lewis-base coordination for enzyme anchoring)
- **Mesopore engineering**: Controlled defect density creates 2–5 nm mesopores for enzyme accessibility while maintaining 1.2 nm micropores for small-molecule catalysis

### Photothermal Properties
- Broadband absorption: 300–2500 nm, α > 0.92
- Photothermal conversion efficiency: η_pt > 95% at 20× solar concentration
- Thermal stability: stable to 400 °C (TGA in N₂)
- Solar-to-chemical energy efficiency: target >15% (monomer HHV / incident solar)

### Catalytic Performance (Target)
| Polymer | Conversion | Monomer Selectivity | Conditions |
|---------|-----------|-------------------|------------|
| PET | >95% | >92% TPA + EG | 150 °C, enzymatic zone |
| HDPE | >85% | >88% C₂–C₄ olefins | 230 °C, Lewis-acid zone |
| PP | >85% | >85% propylene + C₂–C₅ | 240 °C, Lewis-acid zone |
| PS | >90% | >90% styrene | 200 °C, Lewis-acid zone |
| Nylon-6 | >80% | >82% caprolactam | 250 °C, Lewis-acid zone |
| Mixed (≥3 types) | >75% | >80% separable monomers | Staged cascade |

## Materials Bill

| Material | Quantity | Unit Cost | Total |
|----------|----------|-----------|-------|
| 316L SS tubing (reactor) | 400 kg | $4/kg | $1,600 |
| SiC liner | 80 kg | $12/kg | $960 |
| MOF-808-DP catalyst | 120 kg | $50/kg* | $6,000 |
| PHL7 enzyme (bulk) | 2 kg | $200/kg* | $400 |
| CPC reflectors (Al) | 50 m² | $40/m² | $2,000 |
| PV panels (8 kW) | 32 m² | $0.30/W | $2,400 |
| LFP battery (20 kWh) | 1 unit | $150/kWh | $3,000 |
| Distillation column | 1 unit | $8,000 | $8,000 |
| Membrane separator | 1 unit | $3,500 | $3,500 |
| Shredder + washer | 1 unit | $5,000 | $5,000 |
| PCM salt (nitrate) | 200 kg | $3/kg | $600 |
| Controls + sensors | 1 set | $3,000 | $3,000 |
| Pumps, valves, piping | 1 set | $4,000 | $4,000 |
| Container + integration | 1 unit | $8,000 | $8,000 |
| **Total** | | | **~$48,460** |

*Projected costs at 10,000-unit production scale (current lab MOF costs ~$500/kg; scaling + continuous flow synthesis projected to reach $50/kg by 2035)

## Performance Benchmarks

| Metric | SPU (Target) | Pyrolysis | Mechanical Recycling | Enzymatic Only |
|--------|-------------|-----------|---------------------|----------------|
| Temperature | 150–250 °C | 400–800 °C | 200–300 °C (melt) | 60–72 °C |
| Feedstock purity required | Mixed/contaminated OK | Sorted, <5% contam. | Sorted, single-polymer | PET only |
| Monomer quality | Virgin | Low (mixed oil) | Degraded (downcycled) | Virgin (PET only) |
| Energy source | Solar | Natural gas | Electric/gas | Electric |
| CO₂ per kg recycled | 0.1–0.3 kg | 1.5–2.5 kg | 0.3–0.8 kg | 0.2–0.5 kg |
| Scale | Community (500 kg/day) | Industrial (50+ t/day) | Industrial | Lab–pilot |
| CAPEX | $80K–120K | $5M–50M | $1M–10M | N/A |
| Monomer cost/kg | $0.30–0.60 | $0.90–1.80 | $0.50–1.20 | $0.80–2.00 |

## Safety

- **Pressure relief**: Burst discs on all pressurized vessels (5 bar rating, relief at 7 bar)
- **Gas monitoring**: NDIR ethylene/propylene leak detection, auto-shutdown at 10% LEL
- **Fire suppression**: Inert gas (N₂) flooding system, activated by thermal or gas sensors
- **Noise**: <75 dB at 1 m (shredder enclosure)
- **Emissions**: Zero process emissions to atmosphere; all outputs are captured monomers or inert residue (<2% of input mass)

## Development Roadmap

### Phase 1 (2026–2028): Lab Validation
- Synthesize MOF-808-DP and characterize photothermal + catalytic properties
- Demonstrate >90% PET depolymerization with immobilized PHL7 on MOF mesopores
- Build benchtop photothermal reactor (100 g/day) with CPC simulator
- Publish results, file provisional patents

### Phase 2 (2028–2031): Pilot System
- Build 50 kg/day pilot with real mixed waste feedstock
- Achieve >75% conversion on 3+ polymer blend
- Demonstrate 100+ hour catalyst stability with in-situ regeneration
- Field test in 2 communities (coastal + inland)

### Phase 3 (2031–2034): Commercial Prototype
- Full-scale 500 kg/day containerized unit
- Achieve target monomer purities (>99% for top 3 monomers)
- 3-month continuous operation demo
- Regulatory approval (CE, UL, environmental permits)

### Phase 4 (2034–2038): Scale-Up
- 1,000 units deployed in 50+ countries
- MOF manufacturing at $50/kg scale
- Franchise model: municipality-owned, locally operated
- Open-source catalyst synthesis recipes

### Phase 5 (2038–2045): Global Impact
- 1M units deployed → 500M tonnes/year capacity
- Integration with municipal waste streams worldwide
- Closed-loop plastic economy achieved in participating regions