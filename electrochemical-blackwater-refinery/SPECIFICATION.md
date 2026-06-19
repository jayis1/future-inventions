# SPECIFICATION — Electrochemical Blackwater Refinery (EBR)

Technical reference for the Electrochemical Blackwater Refinery. All figures are design targets for a household-scale unit serving 6–10 persons.

---

## 1. System envelope

| Parameter | Specification |
|---|---|
| Form factor | Sealed floor-standing appliance, 0.42 × 0.42 × 1.25 m |
| Dry mass | 38 kg (28 kg wet operational) |
| Daily capacity | 6–10 person-equivalents (≈4–7 L total excreta + flush/rinse/day) |
| Batch cycle | 24–48 h (fill → treat → drain) |
| Water input | ≤0.2 L/cycle rinse water (graywater-acceptable); no potable water required |
| Power source | 30 Wₚ flexible PV + 2× TEG (4–8 W continuous) + 100 Wh LiFePO₄ buffer |
| Grid/fuel connection | None |
| Consumables | Biochar-ceramic cartridge (replace 1–2×/yr, locally produced) |
| Ventilation | Sealed vapor lock + catalytic odor oxidizer; no vented pit |
| Operating temperature | −5 °C to +50 °C ambient; internal reactor 20–45 °C during oxidation |
| Lifetime target | 10 years (electrodes 5–8 yr; LiFePO₄ 8–10 yr; cartridge 6–12 mo) |

---

## 2. Reactor subsystems

### 2.1 Collection chamber
- Sloped hopper, PTFE-coated 316L stainless / HDPE, self-draining.
- Urine-diverting optional seat insert; both streams combine in reactor (urine provides NH₄⁺/PO₄³⁻ for struvite).
- Macerator pump (12 V DC brushless, 15 W, 3,000 rpm) homogenizes solids to ≤2 mm slurry enabling electrochemical contact.

### 2.2 Stage A — Electrocoagulation + struvite precipitation
| Parameter | Value |
|---|---|
| Electrode | Sacrificial Mg (AZ31) anode + SS cathode pair |
| Active area | 0.04 m² per pair, 2 pairs |
| Current density | 10–30 A/m² |
| Cell voltage | 3–6 V |
| Duration | 30–60 min/batch |
| Energy | 0.3–0.8 Wh/L waste |
| Mg consumption | 0.3–0.8 g/L (≈0.4 kg/yr/household; anode replaceable cartridge, 12–18 mo) |
| pH shift | +1.0–1.5 units (local near-anode) to drive struvite supersaturation |
| Struvite yield | 0.5–1.5 g P/batch → **3–6 kg P₂O₅-equivalent/household/yr** |
| P recovery efficiency | **≥85%** of influent orthophosphate |
| Settling | Gravity hopper; crystals harvested via bottom valve to drying tray |

### 2.3 Stage B — Electrochemical advanced oxidation (EAOP)
| Parameter | Value |
|---|---|
| Anode | Boron-doped diamond (BDD) on Nb mesh, 0.06 m² active |
| Cathode | Stainless steel 316L mesh |
| Configuration | Undivided cell, 4 electrode pairs interleaved |
| Applied current | 2–6 A (constant current) |
| Cell voltage | 6–12 V |
| Current density | 30–100 A/m² |
| Duration | 18–36 h (COD-dependent; sensor-terminated) |
| Energy | 8–20 Wh/L waste (≈0.3–0.7 kWh/household/day) |
| Generated oxidants | •OH (anode, ≈2.8 V vs SHE), HOCl/ClO⁻ (from Cl⁻, 0.2–1 g/L active Cl), S₂O₈²⁻ (from SO₄²⁻) |
| Pathogen log reduction | **≥6-log** (bacteria, viruses, protozoa, helminth eggs) |
| COD reduction | **>90%** (mineralization to CO₂ + H₂O + inorganic salts) |
| NH₄⁺ fate | Oxidized to N₂ (via breakpoint chlorination in situ) or retained in fertilizer fraction; tunable via timing |
| Off-gas | CO₂ + trace N₂ + H₂O vapor; catalytic oxidizer (Pt/Al₂O₃, 80 °C) destroys residual VOCs/odor |
| Electrode lifetime | BDD expected 5–8 yr; periodic acid-clean (citric) every 3–6 mo |

### 2.4 Stage C — Biochar-ceramic polishing cartridge
| Parameter | Value |
|---|---|
| Media | 60% ag-waste biochar (coconut shell / rice husk) + 40% fired clay ceramic, granulated 2–6 mm, 6 kg |
| Target removal | Pharmaceuticals & hormones >85%; microplastics >95%; heavy metals (Pb, Cd, As) >90%; ARG fragments >70% |
| Flow | Downflow gravity, 0.2–0.5 L/min |
| Contact time | ≥8 min |
| Replace interval | 6–12 months (≈6 kg/cartridge) |
| End-of-life | Spent cartridge is nutrient-rich → returned to soil as amendment; carbon locked ~5–15 kg CO₂/cartridge |

### 2.5 Output streams
| Stream | Volume/day | Quality | Use |
|---|---|---|---|
| Struvite crystals | 5–15 g | >90% MgNH₄PO₄·6H₂O, dry, sterile | Slow-release P fertilizer |
| Liquid fertilizer | 3–6 L | Pathogen-free; N 0.5–1.5 g/L, K 0.3–0.8 g/L, micronutrients | Soil/foliar fertigation |
| Polished water | 0.5–1.5 L | ≤1,000 CFU/100 mL; ≤10 mg/L BOD; ≤1 NTU | Subsurface irrigation / infiltration |

---

## 3. Power & control

### 3.1 Power budget (per 24-h batch)
| Load | Energy | Notes |
|---|---|---|
| EAOP electrode drive | 50–120 Wh | Dominant; ~70% of energy |
| Electrocoagulation | 5–12 Wh | Short duration |
| Macerator + pumps | 3–8 Wh | Intermittent |
| Controls + sensors | 2–4 Wh | Continuous MCU + sensor sampling |
| Catalytic oxidizer preheat | 5–15 Wh | Duty-cycled |
| **Total** | **65–160 Wh/day** | Met by PV (avg ~120 Wh/day at 5 kWh/m²/d insolation) + TEG (≈100–190 Wh/day) + LiFePO₄ buffer |

### 3.2 Energy harvesting
- **PV**: 30 Wₚ flexible CIGS panel (0.3 m²), MPPT controller.
- **Thermoelectric**: 2× Bi₂Te₃ TEG modules (40 × 40 mm) clamped to reactor wall (hot side) finned to ambient (cold side); 4–8 W continuous average from oxidation exotherm + day–night ΔT; feeds boost converter.
- **Storage**: 100 Wh LiFePO₄ pack (12 V, 8.3 Ah), 10-yr calendar life; buffered by TEG overnight.

### 3.3 Control architecture
- **MCU**: STM32L4 (ARM Cortex-M4, ultra-low power, 8–40 µA sleep).
- **Sensors** (non-contact where possible):
  - Conductivity probe (batch ionic strength → EAOP endpoint)
  - ORP (oxidation-reduction potential, mV) → pathogen-kill proxy
  - pH (ISFET, robust)
  - Temperature (NTC ×3)
  - Liquid level (capacitive)
  - Methane/CO₂ (NDIR) off-gas monitor
- **Control logic**: Finite-state machine — Fill → Macerate → EC stage → Settle → EAOP stage (ORP-terminated) → Polish → Drain → Idle. ORP plateau + conductivity threshold confirms ≥6-log kill; fail-safe holds batch if endpoint not reached.
- **Telemetry** (optional): LoRa mesh (Semtech SX1262) for fleet monitoring, predictive maintenance, cartridge replenishment logistics — privacy-preserving (no biometric data; only operational state).
- **User interface**: 3-LED status (fill/treat/ready), single button, no app required.

---

## 4. Materials bill (indicative, 100k-unit/yr scale)

| Component | Material | Qty | Unit cost |
|---|---|---|---|
| BDD electrode stack | BDD-on-Nb mesh | 0.06 m² | $45–60 |
| Mg sacrificial anode cartridge | AZ31 Mg alloy | 0.5 kg | $4–8 |
| Biochar-ceramic cartridge (replaceable) | Biochar + clay | 6 kg | $3–6 |
| PV panel | 30 Wₚ flexible CIGS | 1 | $18–25 |
| TEG modules | Bi₂Te₃ 40×40 mm | 2 | $20–30 |
| LiFePO₄ pack | 12 V 8.3 Ah | 1 | $30–40 |
| MCU + sensors + PCB | STM32L4 + cluster | 1 | $12–20 |
| Macerator pump | 12 V brushless | 1 | $8–15 |
| Structure (HDPE shell + 316L frame) | — | — | $30–50 |
| Catalytic odor oxidizer | Pt/Al₂O₃ cartridge | 1 | $4–8 |
| Plumbing + seals + valves | — | — | $8–15 |
| **Total BOM** | | | **$182–277** |

Landed unit cost (assembly, freight, margin): **$250–350**.

---

## 5. Validation criteria (TRL advancement)

To advance from TRL 2 → 3:
- Bench EAOP on synthetic + real blackwater: confirm ≥6-log *E. coli* + MS2 + *Cryptosporidum* kill, ≥90% COD reduction, ≤20 Wh/L, at 2–10 L batch.
- Confirm struvite yield ≥85% P recovery with Mg dosing.
- Confirm biochar cartridge removal targets over ≥50 batches.

TRL 3 → 5:
- Integrated prototype, ≥500 consecutive batches, field-deployable form.
- Long-duration electrode fouling test; Mg anode life validation.

TRL 5 → 7:
- Field trial: 50 units, 3 sites (dense informal settlement; rural village; refugee camp), 12 months, independent health-impact monitoring.

---

## 6. Risks & mitigations

| Risk | Likelihood | Mitigation |
|---|---|---|
| BDD electrode fouling (Ca/Mg scale, organics) | Medium | EC-first struvite removal reduces scaling; periodic citric acid reversal clean; 5–8 yr replacement |
| Active chlorine off-gas / odor | Low | Sealed reactor + catalytic oxidizer; Cl⁻ limited to what's in waste; ORP-controlled dosing |
| Microplastics / PFAS not fully removed | Medium | Biochar + ceramic adsorption; 2-stage cartridge option for high-load contexts |
| LiFePO₄ end-of-life recycling | Low | Pack is removable, 95% recyclable; 10-yr life exceeds device service interval |
| High-salinity influent (seawater-flushed regions) | Low | EAOP tolerant; struvite yield adjusts; conductivity sensor governs cycle time |
| User acceptance (sealed unit vs. pit) | Medium | Odorless sealed operation is a feature; local co-design; fertilizer output as adoption incentive |
| Scale-up cost (BDD) | Medium→declining | BDD on learning curve; alternative PbO₂/SnO₂ electrodes as fallback at lower performance/cost |

---

## 7. References / prior art

- Gates Foundation "Reinvent the Toilet" program (2011–present); multiple EAOP and struvite toilet prototypes (Cranfield Nano-Membrane Toilet, Caltech electrochemical toilet).
- Kraft et al. (1999–ongoing): BDD electrode advanced oxidation fundamentals.
- Doyle & Parsons (2002): struvite precipitation from wastewater — nucleation & recovery.
- WHO/UNICEF JMP (2023): *Progress on household drinking water, sanitation and hygiene 2000–2022*.
- UNESCO (2024): *World Water Development Report — wastewater & nutrient recovery*.
- Hofmann et al. (2023): thermoelectric energy harvesting from sanitation reactors (concept validation).
- Phosphorus recovery consensus (ESPP, 2022): struvite as a safe, slow-release P fertilizer from waste.