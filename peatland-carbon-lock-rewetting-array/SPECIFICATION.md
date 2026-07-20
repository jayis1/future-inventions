# Specification — Peatland Carbon-Lock Rewetting Array

## 1. System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    CLOUD ORCHESTRATION                       │
│  • Regional rewetting planning (satellite drainage mapping)  │
│  • Carbon-credit MRV ledger (blockchain-verifiable flux data) │
│  • Weir-network hydraulic optimization (target WT contour)   │
│  • Fleet scheduling & drone swarm coordination              │
└──────────────┬──────────────────────────────┬───────────────┘
               │ LoRa-mesh / cellular backhaul │
   ┌───────────▼───────────┐   ┌──────────────▼──────────────┐
   │  SOLAR GATEWAY NODE     │   │  SOLAR GATEWAY NODE          │
   │  (1 per 200–500 ha)    │   │  (1 per 200–500 ha)         │
   │  • LoRa concentrator   │   │  • Edge flux aggregation    │
   │  • 100W PV + 5kWh LFP  │   │  • Water-table model runner │
   └───┬───────────┬────────┘   └───┬───────────┬─────────────┘
       │           │                 │           │
  ┌────▼───┐ ┌─────▼────┐       ┌────▼───┐ ┌─────▼─────┐
  │ SMART  │ │ SMART    │  ...  │ SMART  │ │ SENSOR    │
  │ WEIR 1 │ │ WEIR 2   │       │ WEIR n │ │ MESH (4/ha)│
  │ peat-  │ │ peat-    │       │ peat-  │ │ WT, CO₂,  │
  │ crete  │ │ crete    │       │ crete  │ │ CH₄, T, EC │
  │ +pump  │ │ +pump    │       │ +pump  │ │ biodegrad. │
  └────────┘ └──────────┘       └────────┘ └───────────┘
                    ▲
                    │ aerial broadcast
          ┌─────────┴─────────┐
          │ INOCULANT DRONE   │
          │ Sphagnum-methano-  │
          │ troph pellets      │
          └────────────────────┘
```

## 2. Smart Weir Module — Detailed Design

### 2.1 Physical envelope
- **Transported mass:** 3.5 kg (drone-slung)
- **Deployed weir dimensions:** 1.2 m wide × 0.6 m tall × channel-width (typical 0.5–2 m)
- **Inflation:** compressed-CO₂ cartridge (8 g) + on-site peat slurry intake (scoop arm draws channel water + peat fines)
- **Cure time:** 7–14 days to reach 0.5–1.5 MPa compressive strength (peatcrete via MICP)

### 2.2 Peatcrete formulation
| Component | Mass fraction | Role |
|-----------|---------------|------|
| Site peat fines (organic) | 55–65% | aggregate, carbon content |
| Biochar (from on-site brush) | 10–15% | CH₄ adsorbent, reinforcement, habitat |
| CaCO₃ fines (limestone powder) | 8–12% | carbonate source for MICP |
| Urea (slow-release coated) | 1–2% | substrate for ureolytic MICP bacteria |
| Indigenous ureolytic peat bacteria culture | 0.5–1% (liquid inoculum) | urease → CaCO₃ precipitation |
| Jute geotextile bladder | bladder wall | biodegradable containment, fiber reinforcement |
| Sodium alginate | 0.3–0.5% | gelling agent, sets initial shape before MICP cure |

Mechanism: ureolytic bacteria (*Sporosarcina pasteurii* indigenous analogs + enriched urease-positive peat isolates) hydrolyze urea → NH₃ + CO₂ → CO₃²⁻ → precipitates CaCO₃ in the peat-biochar matrix over 1–2 weeks, binding the slurry into a load-bearing plug. No Portland cement, no transport of heavy materials — 70–90% of weir mass comes from the site itself.

### 2.3 Active crest-tuning subsystem
- **Micro-pump:** 12V diaphragm pump, 0.5 L/min, 0.5W standby / 5W pumping
- **Reservoir:** 2L bladder; pumps water in/out of weir crest bag to raise/lower effective dam height by ±10 cm
- **Water-table target:** −5 to +2 cm above peat surface (sphagnum-optimal anaerobic window)
- **Control:** edge MPC (model predictive control) running on weir's MSP430-class MCU, with cloud-supplied target contour
- **PV:** 5W flexible CIGS panel, 18650 LFP cell (2.2 Ah) — 7-day autonomy in boreal winter

### 2.4 Telemetry
| Sensor | Type | Range | Accuracy |
|--------|------|-------|----------|
| Water level | capacitive strip | 0–2 m | ±2 mm |
| Flow rate (channel) | ultrasonic time-of-flight | 0–2 m/s | ±5% |
| Temperature | thermistor | −40 to +60 °C | ±0.5 °C |
| EC | capacitive | 0–10 mS/cm | ±3% |

LoRa-mesh: SX1262, 868/915 MHz, −137 dBm sensitivity, 2–8 km range peatland canopy, AES-128.

## 3. Sphagnum-Methanotroph Inoculant — Detailed Design

### 3.1 Strain engineering
Base consortium (naturally occurring in healthy *Sphagnum*):
- *Methylocystis* sp. (Type II methanotroph, high-affinity pMMO)
- *Methylobacter* sp. (Type I, high CH₄ flux oxidation)
- *Beijerinckia* sp. (diazotrophic endophyte, N₂ fixation)

Enhancements (within 10–15 yr feasibility):
- **Upregulated pMMO expression** via promoter engineering (pMOO promoter library, ~3–5× higher CH₄ oxidation rate at low [CH₄]).
- **sMMO (soluble MMO) gene cluster knock-in** into *Methylocystis* — enables activity at <10 ppmv CH₄ where pMMO alone is substrate-limited.
- **Biochar-affinity adhesion operon** — surface-displayed cellulose-binding domain anchors cells to biochar matrix, increasing colonization 2–3×.
- **Cryotolerance** — psychrotolerant variants for boreal peatlands (active at 2–10 °C), via cold-shock protein overexpression.
- **No engineered gene transfer** — chromosomal integration only, no plasmid borne markers, auxotrophic safeguards, dies out of bog context in 30–90 days.

All engineering confined to native peat methanotrophs (not novel organisms) using established tools (promoter swaps, chromosomal knock-in, auxotrophy) — within current synthetic-biology regulatory frameworks.

### 3.2 Inoculant pellet
| Layer | Component | Function |
|-------|-----------|----------|
| Core | freeze-dried engineered *Methylocystis*/*Methylobacter* (10⁸–10⁹ CFU) | CH₄ oxidation |
| Mid | *Beijerinckia* diazotroph (10⁷ CFU) | N₂ fixation → no fertilizer needed |
| Mid | *Sphagnum* propagules (1–3 gemmae + spores) | moss re-establishment |
| Outer | biochar fines (50–100 µm) + 2% alginate binder | CH₄ adsorbent + carrier + adhesion |
| Coat | trehalose + maltodextrin protectant | desiccation survival, 18-mo shelf life |

Pellet mass: 1.5 g, diameter 8 mm. Drone broadcast rate: 1,000–5,000 pellets/ha (site-dependent).

### 3.3 Performance targets
- CH₄ oxidation rate at surface peat (10–200 ppmv CH₄): **8–25 mg CH₄/m²/h** (vs. 2–8 mg natural)
- Methane suppression vs. naïve rewetting: **70–95% reduction** of the rewetting spike
- Time to net-cooling (CO₂ avoided > CH₄ emitted, 20-yr GWP): **1–3 years** (vs. 10–30 yr naïve)
- Sphagnum re-establishment cover: **40–70% in 3 yr, 80–95% in 5 yr**

## 4. Biodegradable Sensor Mesh

### 4.1 Substrate & electronics
- **Substrate:** cellulose acetate film (50 µm), dissolves in peat water over 5–7 yr, leaving only trace minerals.
- **Conductors:** carbon-graphite ink printed traces (no metals of concern).
- **MCU:** RFIC-tag-class ultra-low-power (nRF53 equivalent in paper-Si), 100 µA active.
- **Power:** printed Zn-air battery (biodegradable, 300 mAh, 1.4V) + small cellulose-based supercapacitor. 2–5 yr life, dissolves harmlessly.

### 4.2 Sensors
| Parameter | Method | Range | Power |
|-----------|--------|-------|-------|
| Water-table depth | capacitive cellulose tape | 0–1 m | 50 µA/smpl |
| Soil moisture | TDR cellulose probe | 0–100% | 200 µA/smpl |
| Peat temperature | thermistor print | −20–60 °C | 10 µA/smpl |
| CO₂ flux | NDIR micro-cell (LED + thermopile) | 0–5000 ppm | 1 mA/smpl |
| CH₄ flux | TDLAS micro-spectrometer (2.2 µm DFB laser, 10 cm path) | 1–100 ppm | 5 mA/smpl |
| Eh (redox) | Pt/carbon electrode | −400 to +800 mV | 10 µA/smpl |
| EC | 4-electrode carbon | 0–10 mS/cm | 50 µA/smpl |

Sampling cadence: hourly; LoRa uplink every 6 h. 1–4 sensors/ha → $20–60/ha.

## 5. Deployment Drones

### 5.1 Weir-deployment drone (amphibious)
- **Type:** quad-tilt-rotor amphibious, floats on channel water to deploy weir
- **Payload:** 1 weir (3.5 kg) + 30 g CO₂ cartridge + peat slurry scoop
- **Endurance:** 40 min flight + 8 deployments/charge (1.2 kWh Li-S pack)
- **PV recharge:** 200W foldable wing panel, 90 min recharge
- **Throughput:** 50–200 weirs/day per drone (channel density dependent)
- **Cost target:** $3,000–8,000/drone

### 5.2 Inoculant-broadcast drone
- **Type:** heavy-lift multirotor, 10 kg pellet payload (5,000–6,000 pellets)
- **Broadcast:** centrifugal spreader, 5–10 m swath, 1,000–5,000 pellets/ha
- **Throughput:** 30–80 ha/charge
- **Cost target:** $4,000–10,000/drone

### 5.3 Navigation
- RTK-GNSS (2 cm) + peatland drainage canal map (satellite-derived) + onboard LiDAR for obstacle/water detection. Operates BVLOS under regional rewetting permits.

## 6. Cloud Orchestration

### 6.1 Drainage mapping
- Sentinel-2 + SAR (Sentinel-1) drainage network extraction → candidate weir placement optimization (graph-theoretic min-cut to block maximal flow with minimal weirs).
- Updates monthly; re-plans weir network as rewetting progresses.

### 6.2 Hydraulic optimization
- 2D shallow-water model of the peatland cell with weir network as boundary conditions; solves for individual weir crest heights that maintain target WT contour (±5 cm) across the cell under seasonal rainfall variation.
- Recomputes weekly; pushes setpoints to weir MCUs.

### 6.3 MRV ledger
- Continuous CO₂/CH₄ flux from sensor mesh → eddy-covariance-validated gap-filled time series → blockchain-verifiable carbon credit ledger (Verra/Plan Vivo compatible).
- Eliminates 5–25 $/ha/yr third-party audit cost and the multi-year verification lag.

## 7. Performance Benchmarks

| Metric | Manual rewetting | This system |
|--------|-------------------|-------------|
| Weir cost (deployed) | $500–5,000 | $30–80 |
| Rewetting cost/ha | $3,000–20,000 | $300–1,000 |
| Weirs/day (per crew/drone) | 2–10 | 50–200 |
| Methane spike (yr 1–5) | +0.5–3 t CO₂-eq/ha/yr | +0.05–0.3 (70–95% ↓) |
| Time to net-cooling | 10–30 yr | 1–3 yr |
| Cost/t CO₂-eq avoided | $15–80 | $2–8 |
| MRV cost/ha/yr | $5–25 | included |
| Subsidence halted | 2–5 yr after WT restored | same, but verified |
| Weir service life | 5–15 yr (timber) | 30+ yr (peatcrete self-heals) |
| Residual waste | timber/cement debris | none (biodegradable) |

## 8. Deployment Scenarios

### 8.1 Tropical peat — Central Kalimantan, Indonesia (2M ha)
- Drainage canals from 1990s Mega-Rice Project; 1.5M ha drained, fires annual.
- ~500K weirs, 1,000 drones, 3–5 yr to rewet.
- CO₂ avoided: 80–120 Mt/yr; CH₄ spike suppressed; fire risk ↓90%.
- Carbon credits @ $20/t: $1.6–2.4B/yr — finances full program with surplus.

### 8.2 Boreal peat — Western Siberian Lowland (10M ha)
- Drained for oil/gas access roads; vast remote extent → only autonomous system viable.
- 2M weirs, 4,000 drones, 8–10 yr.
- Cold-tolerant methanotroph strains essential; solar gateway sized for −40 °C winter.

### 8.3 Temperate raised bog — UK & Ireland (200K ha)
- Extraction-damaged; community-led restoration; open-source weir designs enable volunteer fabrication.
- Methane suppression critical in densely populated NW Europe (regulatory CH₄ limits).

## 9. Risks & Mitigations

| # | Risk | Likelihood | Severity | Mitigation |
|---|------|-----------|----------|------------|
| 1 | Engineered methanotroph fails to establish | Med | High | Use native strains; biochar matrix boosts colonization 2–3×; fail-safe = natural consortium still suppresses 50–70% |
| 2 | Peatcrete MICP cure fails (low ureolytic count) | Med | Med | Pre-seeded ureolytic inoculant in bladder; backup Portland-free lime binder |
| 3 | Weir network over-impounds, floods adjacent land | Low | High | Edge MPC with hard crest-lowering fail-safe; satellite WT monitoring; manual override |
| 4 | Sensor mesh dissolves too fast | Low | Med | Cellulose-acetate film thickness tuned for 5–7 yr; replaceable in 2nd cycle |
| 5 | Drone operations in remote boreal regions | Med | Low | Solar-recharge autonomy; BVLOS permits; fail-safe landings |
| 6 | Invasive Sphagnum outcompetes native | Low | Med | Use region-native Sphagnum species in each inoculant batch |
| 7 | Carbon credit market volatility | Med | Low | Diversify revenue (biodiversity credits, water services, fire-prevention premiums) |
| 8 | Induced seismicity from rewetting | Very low | Low | Rewetting is surface hydrology, not injection; no seismic risk |
| 9 | Methanotroph horizontal gene transfer | Low | Med | Chromosomal-only integration, no plasmids; auxotrophic safeguards; dies out-of-context |
| 10 | Extreme drought overwhelms weirs | Med | Med | Weir network tuned to maximize retention; biochar mulch reduces evaporation 20–40% |

## 10. Roadmap

| Phase | Years | Milestones |
|-------|-------|------------|
| 1 — Component validation | 2026–2028 | Peatcrete MICP formulation; methanotroph strain engineering; biodegradable sensor prototype; 1-ha pilot (UK) |
| 2 — Integrated pilot | 2028–2031 | 100–500 ha pilot in Kalimantan + boreal Canada; verify methane suppression and MRV; first carbon credits issued |
| 3 — Regional scale | 2031–2037 | 50K–500K ha regions (Kalimantan 2M ha; Siberia 1M ha); 10K-drone fleets; cost < $500/ha |
| 4 — Planetary scale | 2037–2045 | 50M ha; 50K drones; 50M weirs; 1.5–2.3 Gt CO₂-eq/yr avoided |
| 5 — Maintenance & expansion | 2045–2055 | Self-renewing weir network; Sphagnum self-sustaining; system transitions from active restoration to stewardship |

## 11. References

- Page, S.E. et al. (2011) "Review of peatland fire, carbon and haze in Southeast Asia." *Global Change Biology* 17(3): 798–818.
- Joosten, H. (2015) *Peatlands worldwide*. In: Björk, *The Biology of Peatlands*.
- Limpens, J. et al. (2008) "Peatlands and the global carbon cycle." *Nature Geoscience* 1: 668–673.
- Kip, N. et al. (2010) "Methanotrophic activity in *Sphagnum*." *PNAS* 107(31): 13806–13811.
- Whalen, M. (2005) "Biogeochemistry of methane exchange between natural wetlands and the atmosphere." *Environmental Engineering Science* 22(1).
- Whiticar, M. & Eckard, F. (2015) "Methane oxidation in Sphagnum-dominated peatlands." *Biogeochemistry*.
- DeJong, J. et al. (2006) "Microbially induced cementation." *J. Geotech. Geoenviron. Eng.* 132(11) — MICP foundation.
- Minasny, B. et al. (2016) "Peatland restoration and carbon sequestration." *Geoderma*.
- Hooijer, A. et al. (2012) "Subsidence and carbon loss in drained tropical peatlands." *Biogeosciences* 9.
- Turetsky, M. et al. (2015) "Global vulnerability of peatlands to fire and carbon loss." *Nature Geoscience* 8: 11–14.