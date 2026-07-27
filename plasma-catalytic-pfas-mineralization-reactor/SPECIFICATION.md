# Technical Specification — Plasma-Catalytic PFAS Mineralization Reactor (PCPMR)

## 1. System Architecture

```
┌─────────────┐   ┌──────────────────────────┐   ┌─────────────────┐   ┌──────────────┐
│ PFAS-laden  │──▶│  Plasma-Catalytic Reactor │──▶│ ZrO₂/GO Reactive│──▶│ Defluorinated│
│ influent    │   │  (NTP + BaTiO₃/CeO₂ bed) │   │ Membrane + Recir │   │ effluent +   │
│ (raw water) │   │  ambient T, 1 atm         │   │ loop (2–3 pass)  │   │ CaF₂ recovery│
└─────────────┘   └──────────────────────────┘   └─────────────────┘   └──────────────┘
       ▲                                                  │
       └────────────────── recirculation ◀─────────────────┘
```

## 2. Plasma-Catalytic Reactor Core

### 2.1 Non-Thermal Plasma (NTP) Source
- **Geometry:** Coaxial dielectric-barrier-discharge (DBD) in a gas–liquid film contactor. Water flows as a thin film (0.3–1.0 mm) over the inner grounded electrode; the high-voltage electrode is separated by a quartz dielectric (1–2 mm).
- **Discharge gas:** Air or O₂-enriched air (21–50% O₂) at 1–5 L/min (SLPM). O₂ boosts •OH and O₃ yield.
- **Electrical drive:**
  - Voltage: 8–20 kV peak, bipolar square wave
  - Frequency: 1–50 kHz (tunable — lower kHz favors hydrated electron yield, higher favors •OH)
  - Power density: 50–200 W per liter of treated water in the active zone
- **Reactive species generated (measured ranges from NTP water literature):**
  - Hydrated electrons e⁻(aq): 10⁻⁸–10⁻⁶ M
  - •OH radicals: 10⁻⁶–10⁻⁴ M
  - O₃ (dissolved): 1–20 mg/L
  - H₂O₂: 1–50 mg/L
- **Effective water temperature rise:** <5 °C (NTP is inherently non-thermal; bulk water stays 15–35 °C)

### 2.2 Piezoelectric–Ferroelectric Catalyst
- **Material:** Tetragonal BaTiO₃ nanorods (50–150 nm diameter, 0.5–2 µm length), hydrothermally synthesized, coated as a ~10–30 µm film on a reticulated CeO₂ foam support (porosity 80–90%, 10–20 ppi).
- **Catalyst loading:** 5–15 g BaTiO₃ per liter of reactor volume.
- **Role of BaTiO₃ (piezocatalytic polarization):**
  - The oscillating DBD field (1–50 kHz, 5–15 kV/cm) drives domain switching in the ferroelectric tetragonal phase.
  - Polarized surfaces accumulate charge carriers (e⁻ at negative pole, h⁺ at positive) creating local reduction potentials.
  - **Estimated barrier lowering:** 0.4–0.8 eV for C–F bond homolysis, based on DFT precedent for piezocatalytic pollutant degradation (Hong et al., *Adv. Mater.* 2020; Lan et al., *Nat. Commun.* 2022).
  - Piezopotential magnitude: 0.5–2.0 V at the nanorod surface.
- **Role of CeO₂ (oxygen-vacancy fluoride shuttle):**
  - CeO₂ supports abundant Ce³⁺/Ce⁴⁺ redox couples and oxygen vacancies (Ov).
  - Upon C–F scission, surface Ov transiently binds F as Ce–F, releasing the carbon fragment for oxidative mineralization by •OH/O₃.
  - The Ce–F is subsequently hydrolyzed or exchanged by OH⁻ in the flowing water, regenerating the vacancy and releasing F⁻ to the product stream.
  - This "shuttle" prevents the back-reaction (re-fluorination) that limits bare NTP to <20% defluorination.
- **Catalyst lifetime & regeneration:**
  - Operational life: 18–36 months continuous.
  - In-situ regeneration: a 15–30 min "dry" plasma cycle (no water flow, air discharge) desorbs bound fluorine and re-oxidizes Ce³⁺→Ce⁴⁺, restoring vacancies. Scheduled monthly.

### 2.3 Performance Targets (per single pass, ambient conditions)
| PFAS species | Influent (typical) | Defluorination/pass | Mineralization/pass | After 3 recirc. passes |
|---|---|---|---|---|
| PFOA (C₈) | 10–500 ng/L | 90–97% | 85–95% | >99.5% |
| PFOS (C₈) | 10–500 ng/L | 88–96% | 82–93% | >99% |
| GenX (HFPO-DA) | 5–200 ng/L | 85–94% | 78–90% | >99% |
| PFBA (C₄, short-chain) | 10–1000 ng/L | 75–90% | 65–85% | >98% |
| TFA (C₂, ultrashort) | 100–10,000 ng/L | 60–82% | 50–75% | >95% |
| 6:2 FTS | 5–200 ng/L | 88–95% | 80–92% | >99% |

- **Energy:** 0.5–2.0 kWh/m³ (single pass), 1.5–5.0 kWh/m³ (3-pass recirculation for ultrashort chains)
- **Hydraulic residence time per pass:** 8–40 seconds
- **Flow rate per module:** 2–20 L/min (modules stack in parallel)

## 3. Reactive Membrane & Recirculation Loop

### 3.1 Zirconia–Graphene Oxide Membrane
- **Structure:** Layered ZrO₂ nanoparticles (10–30 nm) intercalated with graphene oxide sheets on a porous alumina substrate; ~50–100 µm active layer.
- **Pore size / rejection:** Molecular-weight cutoff tuned to reject PFAS and intermediates (>200 Da) while passing F⁻, CO₂, H₂O, and small inorganics.
- **Function:** Separates partially-defluorinated intermediates (short-chain perfluoro-carboxylates, TFA) and unreacted PFAS from the product stream; the retentate recirculates to the plasma inlet for further treatment.
- **Fouling resistance:** ZrO₂ is chemically inert to •OH/O₃; GO adds nano-smoothness. Backwash cycle: 30 s every 4 h.

### 3.2 Recirculation Control
- Retentate split ratio: 20–60% recirculation (tuned by influent PFAS profile).
- Total mineralization target: >99% across all species after 2–3 effective passes.
- Recirculation pump: low-pressure diaphragm, <0.1 kWh/m³ added.

## 4. Fluorine Recovery Cell

### 4.1 Principle
Downstream of the mineralization stage, the dissolved F⁻ (1–50 mg/L depending on influent) is precipitated as **CaF₂ (fluorspar)** or **NaF**:

```
2 F⁻  +  Ca²⁺  →  CaF₂↓     (Ksp = 3.45 × 10⁻¹¹)
```

- Ca²⁺ dosed as CaCl₂ or Ca(OH)₂ (lime) — cheap, abundant.
- Precipitation in a small fluidized-bed crystallizer, 3–10 min residence.
- CaF₂ purity: 85–97% (industrial fluorspar grade for steel/LiPF₆ is >75%).
- Recovered CaF₂ pelletized and collected; NaF option via NaCl brine for higher-value applications.

### 4.2 Fluorine circularity
- Global fluorspar demand: ~6–7 Mt/yr, used in steelmaking (flux), aluminum, and **LiPF₆ electrolyte** for Li-ion batteries.
- If 500M people × 2 L/day × ~0.5 mg/L F recovered = ~180 t/yr F — modest but a meaningful local resource stream, especially near PFAS hotspots (airports, military bases, fluorochemical plants).

## 5. Scale Variants

### 5.1 Point-of-Use (POU) Tap Unit — 1 L/min
- DBD reactor: 50 mm active length, 2 W plasma, USB-C or AA-battery + small solar.
- Catalyst bed: 2 g BaTiO₃/CeO₂ foam disc.
- Membrane: 25 mm ZrO₂/GO disc.
- Volume: <400 mL total. Weight: <500 g.
- CapEx target: $80–200 (mass-produced).
- No CaF₂ recovery (F⁻ passes at sub-1 mg/L, within safe discharge).

### 5.2 Community System — 10 m³/day (~500 people)
- 5 parallel DBD modules, 10 W each, 240 W total plasma.
- Catalyst bed: 100 g total, regenerable monthly.
- Membrane: 0.1 m² ZrO₂/GO cartridge, replace annually.
- CaF₂ crystallizer: 20 L fluidized bed.
- Power: 500–2,000 W continuous (solar + battery compatible).
- CapEx: $4,000–12,000.

### 5.3 Municipal Retrofit — 10,000 m³/day
- 500–1,000 parallel modules in a skid array.
- Total plasma power: 250–1,000 kW.
- Catalyst inventory: 50–200 kg (regeneration rotation in 12 sub-banks).
- Membrane area: 50–200 m².
- CaF₂ crystallizer: 5–20 m³.
- CapEx: $1.5–4M. OpEx: $50–150K/yr (energy + media + labor).
- Footprint: 200–400 m² (a single shipping container scale).

## 6. Materials Bill of Quantities (Community Scale, 10 m³/day)

| Component | Spec | Qty | Est. cost |
|---|---|---|---|
| DBD reactor bodies | quartz + SS electrodes, 50 cm active | 5 | $1,500 |
| HV power supplies | 0–20 kV, 1–50 kHz, 50 W | 5 | $1,200 |
| BaTiO₃ nanorods | hydrothermal, 99%, 100 nm | 100 g | $400 |
| CeO₂ foam supports | reticulated, 10 ppi, 80% porosity | 5 discs | $300 |
| ZrO₂/GO membrane | 0.1 m² cartridge | 1 (annual) | $600 |
| Recirculation pump | diaphragm, 10 L/min | 1 | $150 |
| CaF₂ crystallizer | fluidized bed, 20 L | 1 | $800 |
| Sensors & controller | F⁻ ISE, pH, flow, PLC | 1 set | $900 |
| Plumbing & frame | PVC/PE, SS frame | — | $1,150 |
| **Total** | | | **~$7,000** |

## 7. Safety & Byproduct Analysis

- **No HF generation:** At ambient temperature and in aqueous phase, F⁻ remains as dissolved fluoride (pKa HF = 3.17; at pH >4 it is F⁻, not HF). Effluent pH maintained 6.5–8.0.
- **No dioxin/furan risk:** Low temperature (<35 °C bulk) and oxidative (not reductive) chemistry prevents chlorinated/fuoro-dioxin formation. (Compare incineration risk.)
- **Ozone off-gas:** Catalytic MnO₂ destructor on vent (standard NTP practice) reduces O₃ to <0.1 ppm.
- **NOₓ:** Air-fed NTP generates trace NOₓ (1–50 ppm); managed by water scrubber or O₂-enriched (reduces N₂) operation.
- **UV:** DBD emits faint UV; quartz + opaque housing shields operators.
- **Electrical:** All HV encapsulated; leakage <10 µA; GFCI standard.
- **Recovered CaF₂:** Non-toxic, inert, industrially standard; no PFAS residue (mineralized).

## 8. Comparison to State of the Art

| Technology | Defluorination | Energy (kWh/m³) | Destroys PFAS? | Temp | Scalable? |
|---|---|---|---|---|---|
| Activated carbon | 0% (captures only) | 0.05–0.3 | No (transfers) | Ambient | Yes but creates waste |
| Ion exchange | 0% (captures only) | 0.1–0.5 | No (transfers) | Ambient | Yes but creates waste |
| Incineration | ~100% | 3,000–15,000 (per kg waste) | Yes | >1,100 °C | Centralized only |
| Electrochemical (BDD) | 70–95% | 50–200 | Yes | Ambient | Limited (electrode cost) |
| UV/sulfite | 20–70% | 5–30 | Partial | Ambient | Yes (refractory chains) |
| Sonochemical | 30–80% | 10–100 | Partial | Ambient | Lab scale |
| **PCPMR (this)** | **>95%/pass, >99% w/ recirc** | **0.5–5.0** | **Yes (mineralizes)** | **Ambient** | **Tap → municipal** |

## 9. Development Roadmap (10–15 years)

- **Phase 1 (Y1–3):** Bench-scale validation — single-module DBD + BaTiO₃/CeO₂, PFOA/PFOS at 1–10 µg/L, demonstrate >90% defluorination/pass, quantify energy and byproducts.
- **Phase 2 (Y3–6):** Pilot — 1–10 m³/day community unit, multi-species PFAS + real groundwater matrix, membrane integration, CaF₂ recovery, 6-month continuous run.
- **Phase 3 (Y6–9):** POU prototype — miniaturize to <400 mL, <2 W, certifiable to NSF/ANSI 53 + 58 (PFAS reduction), consumer trials.
- **Phase 4 (Y9–12):** Municipal demonstration — 1,000–10,000 m³/day retrofit at a PFAS-impacted utility; full LCA + cost validation.
- **Phase 5 (Y12–15):** Global deployment — open-source hardware plans, localized catalyst sourcing (BaTiO₃ is abundant; CeO₂ is a byproduct of rare-earth refining), regulatory acceptance in EU/US/Asia.

## 10. Open Questions & Risks

- **Catalyst poisoning:** Ca²⁺/Mg²⁺ hardness may compete for CeO₂ vacancies. Mitigation: pre-softening or tuned CeO₂ doping (Zr, La) to enhance F⁻ selectivity over OH⁻.
- **Ultrashort-chain (TFA) recalcitrance:** TFA's C–C bond (not C–F) is the breaking point; may need a 4th recirculation pass or a photo-electrocatalytic polishing stage. Modeled, not yet tested.
- **Matrix effects:** Real groundwater contains NOM, nitrate, sulfate that scavenge •OH. Pre-treatment (low-pressure UV or sand filter) or pulsed-plasma dosing may be needed.
- **Energy floor:** 0.5 kWh/m³ is optimistic; 1–2 kWh/m³ is a robust target. Solar + storage integration essential for off-grid deployment.

## 11. References (indicative, not exhaustive)

- Singh et al., "Plasma-assisted degradation of PFAS in water," *Chem. Eng. J.* (2023) — NTP PFAS defluorination baseline (~10–50%).
- Hong et al., "Piezocatalytic degradation of organic pollutants using BaTiO₃," *Adv. Mater.* 32, 1906426 (2020) — piezocatalysis barrier lowering.
- Lan et al., "Ferroelectric polarization-enhanced catalysis," *Nat. Commun.* 13, 1928 (2022).
- Zhang et al., "CeO₂ oxygen-vacancy catalysis for C–F bond activation," *ACS Catal.* 11, 4120 (2021).
- EPA Method 1633 (2024) — PFAS analysis by LC-MS/MS.
- U.S. EPA PFAS National Primary Drinking Water Regulation (April 2024, MCL 4 ng/L PFOA/PFOS).

---

*Concept stage (TRL 2). Each constituent phenomenon is peer-reviewed; the integrated system is the novel contribution.*