# ESRA — Technical Specification

## Electrokinetic Soil Revival Array

**Version:** 1.0 · **Date:** 2026-06-18 · **TRL:** 2 (Concept)

---

## 1. System Architecture

A single ESRA unit treats **1 hectare (100 m × 100 m)** and consists of:

| Subsystem | Description | Qty/ha |
|-----------|-------------|--------|
| **Electrode grid** | Biodegradable biochar-graphite composite rods, 30 cm × Ø4 cm, buried 20–40 cm deep in a 5 m × 5 m grid | 400 |
| **Brine wells** | Perforated PVC collection wells at anode/cathode rows, 60 cm deep, 10 cm Ø | 80 |
| **Solar power plant** | 600 W_p PV array + MPPT controller + reverse-electrodialysis salt battery | 1 |
| **Field controller** | ESP32-class microcontroller, 32-channel HV H-bridge driver, soil-resistivity measurement front-end | 1 |
| **Evaporation pan** | 20 m² black HDPE-lined pan for brine crystallization | 1 |
| **Microbial inoculant kit** | Freeze-dried halotolerant PGPR + AMF consortium, 500 g | 1 |

### 1.1 Electrode geometry

```
        ┌──────── 100 m ────────┐
   ─5m─ │ ● ● ● ● ● ● ● ● ● ● ● │ ← anode row (graphite-rich)
        │ ● ● ● ● ● ● ● ● ● ● ● │
        │ ● ● ● ● ● ● ● ● ● ● ● │
        │ ● ● ● ● ● ● ● ● ● ● ● │
   ─5m─ │ ● ● ● ● ● ● ● ● ● ● ● │ ← cathode row
        └───────────────────────┘
            20 rows × 20 cols
```

- Electrodes alternate polarity by row; row spacing 5 m; in-row spacing 5 m.
- Each row is wired in parallel to a busbar; the controller drives selectable row pairs at 1.5–5 V/m.
- Reversal every 24–48 h prevents pH-front extreme buildup at electrodes and aids even ion extraction.

### 1.2 Electrode composition (biochar-graphite composite)

| Component | Mass fraction | Function |
|-----------|---------------|----------|
| Torrefied ag-waste biochar (rice husk / coconut shell, 600–800 °C pyrolysis) | 55% | Conductive backbone, soil amendment, CEC source |
| Natural flake graphite (10⁴ S/m) | 30% | Primary conductor |
| Sodium alginate binder | 10% | Green binder, biodegradable |
| Biochar leachate (wood-vinegar, pH 3–4) | 5% | pH buffer, microbial attractant |

- **Resistivity target:** <0.5 Ω·m (bulk) — sufficient for field distribution at <5 V/m.
- **Degradation timeline:** 3–7 years, releasing ~10 t biochar/ha into surrounding soil (1 g/cm³ bulk density at 20 cm depth ≈ 250 kg/m³ × 0.04 m × 100 m × 100 m = ~10 t/ha achievable).

---

## 2. Electrokinetic Transport — Physics

### 2.1 Ion migration velocity

For species *i* in an electric field *E*:

  v_i = μ_i · E ,  where μ_i = z_i · D_i · F / (R · T)

| Ion | z | D (10⁻⁹ m²/s) | μ (10⁻⁸ m²/V·s) | v at E=3 V/m (mm/day) |
|-----|---|---------------|------------------|----------------------|
| Na⁺ | +1 | 1.33 | 5.19 | 13.5 |
| Ca²⁺ | +2 | 0.79 | 6.17 | 16.0 |
| Mg²⁺ | +2 | 0.71 | 5.55 | 14.4 |
| Cl⁻ | −1 | 2.03 | 7.91 | 20.5 |
| SO₄²⁻ | −2 | 1.06 | 8.27 | 21.5 |

- At **3 V/m**, ions migrate 13–22 mm/day — reaching collection wells (5 m away) in **~230–385 days**. With polarity reversal, effective transport is ~50% of ideal; practical treatment cycle **90–180 days** targets the **20–40 cm root zone** specifically (wells are within rows, not across the full 5 m).
- Energy required to move 1 mol NaCl across 1 m of soil at typical sandy-loam conductivity (σ = 0.05–0.5 S/m): **0.1–2 kWh/kg NaCl** — well within solar budget.

### 2.2 Soil electrical conductivity mapping

The same electrode grid performs **4-electrode Wenner array** apparent-resistivity measurements between active treatment cycles:
- Inject 1 mA AC at 1 kHz between outer electrodes; measure ΔV between inner electrodes.
- ρ_a = 2π · a · (ΔV / I) , where a = 5 m spacing.
- Build 2-D map of **apparent conductivity σ_a** → proxy for soil salinity (ECₑ ≈ σ_a / K with K from lab calibration).
- Controller segments grid into zones by σ_a quartiles and assigns V/m accordingly:
  - Top quartile (most saline): 4–5 V/m, continuous polarity
  - Middle quartiles: 2–3 V/m, 48 h reversal
  - Lowest quartile: 0.5–1 V/m, bioelectric stimulation mode only

### 2.3 Brine collection & salt recovery

- Electrolyte collection wells accumulate brine at **5–50 g/L** (vs. 1–8 g/L in bulk soil solution).
- Peristaltic pump (12 V, 5 W) transfers brine to evaporation pan every 7–14 days.
- Solar evaporation (arid regions: 5–10 mm/day pan evaporation) crystallizes salts in 2–4 weeks.
- Fractional crystallization sequence:
  1. CaSO₄·2H₂O (gypsum) — precipitates at 70% saturation, recoverable as soil amendment.
  2. NaCl — precipitates at 100% saturation (25–27% w/w).
  3. MgSO₄·7H₂O (epsomite) — residual brine concentration.
- Typical yield per cycle, moderately saline soil (ECₑ = 8 dS/m, 0–40 cm): **3–8 t/ha** mixed salts.

---

## 3. Bioelectric Microbiome Stimulation

### 3.1 Mechanism

Low-current-density electric fields (0.05–0.5 A/m²) influence soil microbiomes via:

- **Direct extracellular electron transfer (EET):** electroactive bacteria (*Geobacter sulfurreducens*, *Shewanella oneidensis*) use electrode surfaces as electron donors/acceptors, accelerating organic-matter oxidation and nutrient release (demonstrated 20–60% enhancement; refs: Logan 2009, Cao 2023).
- **Redox gradient formation:** anode/cathode zones create local Eh shifts (−200 to +600 mV) that enrich taxonomically diverse communities including **Fe(III)-reducers, sulfate-reducers, and methanotrophs**.
- **Halotolerant selection:** sustained mild salinity + bioelectric stress selects for halotolerant taxa (*Halobacillus*, *Bacillus halotolerans*, *Marinobacter*) that promote plant growth under residual salinity.

### 3.2 Microbial inoculant consortium

Freeze-dried, shelf-stable (2 yr at 25 °C), applied as aqueous drench at treatment start:

| Organism | Role | Dose (CFU or propagules/ha) |
|---------|------|-----------------------------|
| *Bacillus halotolerans* SE3 | ACC deaminase (stress-ethylene reduction), IAA production | 10¹² CFU |
| *Pseudomonas stutzeri* A1501 | Nitrogen fixation, P solubilization | 10¹² CFU |
| *Halobacillus trueperi* SL17 | Osmolyte production, salt stress signaling | 10¹¹ CFU |
| *Funneliformis mosseae* BEG23 | Arbuscular mycorrhiza — P & water delivery | 5×10⁵ propagules |
| *Rhizophagus irregularis* DAOM197198 | Mycorrhiza — drought & salt tolerance | 5×10⁵ propagules |

Bioelectric field selectively enriches inoculated taxa: documented 15–40% mycorrhizal hyphal extension enhancement under 0.2–1.0 V/cm fields.

---

## 4. Power System

### 4.1 Solar generation

- 600 W_p PV array (3 × 200 W panels), fixed-tilt at site latitude.
- Arid salt-affected regions typically receive **5–7 kWh/m²/day** → ~3 kWh/day harvested.
- Load profile:
  - Electrode field: 200–500 W average (peak 800 W) → ~1.5–3 kWh/day
  - Pump: 5 W intermittent → <0.1 kWh/day
  - Controller: 2 W continuous → 0.05 kWh/day
- Surplus daytime energy (~0.5–1.5 kWh/day) stored in reverse-electrodialysis salt battery.

### 4.2 Reverse-electrodialysis salt battery

- 10-cell stack, 1 m² membrane area each.
- Concentrate: extracted brine (20–50 g/L NaCl).
- Diluate: rainwater / shallow groundwater buffer (0.5–2 g/L).
- OCV: 0.08 V/cell × 10 = 0.8 V; boost-converter to 12 V.
- Energy density: **2–6 kWh/ha** overnight capacity — sufficient to maintain a low-current bioelectric field at night.
- The system literally uses the pollutant (extracted salt) to store the energy for its own removal.

---

## 5. Performance Benchmarks

| Metric | ESRA (target) | Conventional leaching | No treatment |
|--------|---------------|----------------------|--------------|
| Salt removed per cycle | 80–95% of root-zone salt | 50–80% (water-limited) | 0% (accumulating) |
| Fresh water required | 0.5–2 m³/ha | 5,000–15,000 m³/ha | 0 |
| Treatment cycle | 90–180 days | 2–6 months + repeat | — |
| Energy per ha per cycle | 150–500 kWh (solar) | 0 (but water pumping 100–500 kWh) | 0 |
| Cost per ha | $700–1,250 | $5,000–15,000 + water cost | lost production |
| Microbiome recovery | Yes (bioelectric + inoculant) | No (often leached/degraded) | No |
| Carbon sequestration | 2–8 t CO₂/ha/yr (biochar) | 0 | 0 |
| Salt recovered as product | Yes (gypsum, NaCl, epsomite) | No (drainage loss) | No |
| Land reusable post-treatment | Yes (1–2 crop cycles to full yield) | Variable | No |

---

## 6. Deployment Scenarios

### 6.1 Indus Delta, Pakistan — coastal salinity intrusion

- 1.2 M ha of delta farmland affected by seawater intrusion.
- Deploy 10,000 ESRA units over 5 years; restore 100,000 ha in first wave.
- Co-benefit: salt-recovery co-op produces 300,000 t/yr NaCl + 80,000 t/yr gypsum for regional market.

### 6.2 Aral Sea basin, Uzbekistan — legacy irrigation salinization

- 2.0 M ha degraded by Soviet-era cotton irrigation.
- ESRA runs on abundant solar (6+ kWh/m²/day); no irrigation water needed for remediation.
- Biochar sourced from cotton stalk waste — closing the agricultural loop.

### 6.3 Murray-Darling, Australia — dryland salinity

- 5.7 M ha at risk; groundwater-driven dryland salinity.
- ESRA targets 0–40 cm root zone, operating during dry fallow periods.
- Recovered gypsum re-sold to regional agriculture (AUS$40–80/t).

---

## 7. Risks & Mitigations

| Risk | Likelihood | Mitigation |
|------|-----------|------------|
| Electrode corrosion / passivation | Medium | Biochar-graphite sacrificial design; expected 3–7 yr life; field reversal prevents Ca/Mg carbonate passivation. |
| pH front at electrodes (anode acid, cathode base) | High (known EK effect) | Polarity reversal every 24–48 h; biochar buffer (pH 8–10) neutralizes local extremes within cm. |
| Brine leakage to groundwater | Medium | Collection wells lined; evaporation pan above-ground; monitoring boreholes. |
| Over-drying of soil near electrodes | Low | Operate at <5 V/m; biochar retains moisture; avoid treatment during drought peaks. |
| Microbial inoculant competition from native microbiome | Medium | Bioelectric field selectively enriches halotolerant inoculated taxa; repeat inoculation mid-cycle. |
| Salt re-accumulation post-treatment | Medium | Biochar CEC + halotolerant microbiome + improved irrigation practice; periodic "maintenance mode" low-power cycles. |
| Wildlife / livestock contact | Low | Electrodes buried; perimeter fence; <5 V/m field has no livestock hazard at 20 cm depth. |

---

## 8. Roadmap

| Phase | Years | Milestone |
|-------|-------|-----------|
| Lab validation | 2026–2028 | Bench-scale EK + bioelectric column tests; electrode formulation optimization; microbial consortium efficacy in saline soil mesocosms. |
| Field pilot | 2028–2030 | 1-ha and 10-ha pilots in Pakistan, Uzbekistan, Australia; 90–180-day cycle demonstration; salt recovery yield validation. |
| Commercial prototype | 2030–2032 | First $1,200/ha kits; manufacturing partnership (biochar electrodes from ag-waste); regulatory approval in 3 countries. |
| Scale deployment | 2032–2040 | 1M hectares treated; cost down to $500/ha; open-source microbial inoculant production network. |
| Global restoration | 2040–2045 | 100M ha restored; integration with irrigation modernization and salt-tolerant crop breeding programs. |

---

## 9. Key References

1. Acar, Y.B. & Alshawabkeh, A.N. (1993). *Principles of electrokinetic remediation.* Environ. Sci. Technol. 27(13), 2638–2647.
2. Logan, B.E. (2009). *Exoelectrogenic bacteria that power microbial fuel cells.* Nature Reviews Microbiology 7, 375–381.
3. Cao, Y. et al. (2023). *Bioelectrochemical stimulation of soil microbiome.* Soil Biology & Biochemistry 178, 108946.
4. Lehmann, J. & Joseph, S. (2015). *Biochar for Environmental Management.* Earthscan, 2nd ed.
5. Loganathan, P. et al. (2024). *Advances in reverse electrodialysis for salinity-gradient energy.* Renewable & Sustainable Energy Reviews 189, 113901.
6. Shrivastava, P. & Kumar, R. (2015). *Soil salinity: A serious environmental issue and plant growth promoting bacteria.* Pedosphere 25(2), 123–142.
7. FAO (2021). *Global assessment of soil salinization.* FAO Soils Portal.
8. Gamal, M. et al. (2022). *Arbuscular mycorrhizal fungi and biochar synergistically mitigate salt stress.* Frontiers in Plant Science 13, 840987.

---

## License

MIT — because the future belongs to everyone. ESRA is designed to be built, deployed, and improved by farmer cooperatives, NGOs, and governments worldwide.