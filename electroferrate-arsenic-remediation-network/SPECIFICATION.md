# Specification — Electroferrate Arsenic Remediation Network

## 1. Design Objective

Deliver a modular arsenic-removal platform that treats contaminated groundwater at the point of collection and consistently achieves:

- Effluent arsenic: **<5 µg/L**
- Influent tolerance: **10–1000 µg/L total As**
- As(III) oxidation: **>95% in <2 min**
- Specific energy: **0.05–0.20 kWh/m³**
- Levelized treatment cost: **$0.02–0.10/m³**
- Safe arsenic waste stabilization with **TCLP-compliant** residue

## 2. Core Architecture

```text
Contaminated well water
        │
        ▼
[Screen + flow control]
        │
        ▼
[Electroferrate oxidation chamber]
  - NiFeOx anode
  - low-carbon Fe dissolution stage
        │
        ▼
[Capture bed]
  - magnetite-laterite granules
  - electro-generated ferrihydrite coating
        │
        ▼
[Clarifier / magnetic separator]
        │
        ├──> clean water storage / tap
        │
        └──> regeneration sidestream
                 │
                 ▼
       [alkaline electro-regeneration]
                 │
                 ├──> sorbent returned to bed
                 │
                 └──> arsenic concentrate
                          │
                          ▼
             [iron-phosphate ceramic stabilization]
```

## 3. Materials

### Electrochemical stage
- **Anode:** porous nickel foam with spinel **NiFe₂O₄ / NiOOH-rich surface**
- **Counter electrode:** stainless steel 316L or graphite felt
- **Sacrificial iron source:** low-carbon steel mesh or iron pellets
- **Power electronics:** MPPT charge controller, 12–24 V DC bus

### Capture bed
- **Primary adsorbent scaffold:** sintered **magnetite-laterite granules**, 0.5–2 mm
- **Active capture phase:** electro-deposited **ferrihydrite / goethite-like FeOOH**
- **Hydraulic support:** HDPE or PP cartridge housing with gravel underdrain

### Waste stabilization
- **Binder:** FePO₄-forming phosphate additive plus kaolinite / illite clay
- **Thermal unit:** 300–600 W insulated electric kiln or solar-thermal assist kiln
- **Target pellet density:** >2.4 g/cm³

### Power and controls
- **PV:** 30–150 W mono-Si
- **Storage:** 12.8 V LiFePO₄, 10–40 Ah
- **Sensors:** ORP, pH, flow, conductivity, optional gold-microelectrode arsenic sensor, camera-assisted arsenic strip reader
- **Connectivity:** Bluetooth LE; optional LoRaWAN for community installations

## 4. Key Reactions and Mechanisms

### 4.1 Arsenite oxidation
Ferrate(VI) and high-valent iron intermediates oxidize arsenite:

```text
H3AsO3 + H2O -> HAsO4^2- + 4 H+ + 2 e-
FeO4^2- + 3 e- + 5 H2O -> Fe(OH)3 + 7 OH-
```

### 4.2 Adsorption / coprecipitation
Arsenate forms inner-sphere bidentate complexes on FeOOH surfaces. Removal is enhanced by:
- fresh ferrihydrite nucleation,
- magnetite-assisted aggregation,
- pH control in the 6.3–7.5 range,
- iron:arsenic molar ratio target of **20:1 to 80:1** depending on phosphate competition.

### 4.3 Regeneration
A pulsed alkaline desorption step removes a controllable fraction of bound arsenic while preserving the magnetic scaffold. Re-coating with fresh ferrihydrite restores high-affinity sites.

### 4.4 Ceramic immobilization
Arsenic concentrate is combined with iron and phosphate to form low-solubility iron-arsenate / iron-phosphate glass-ceramic phases after controlled heating, minimizing long-term leaching.

## 5. Quantitative Performance Targets

| Metric | Target |
|---|---:|
| Effluent arsenic | <5 µg/L |
| Removal efficiency | 99–99.7% |
| As(III) oxidation | >95% |
| Hydraulic residence time | 2–8 min |
| Iron usage | 20–120 mg/L treated |
| Specific energy | 0.05–0.20 kWh/m³ |
| Sorbent regeneration cycles | 100+ |
| Ceramic waste generated | <5–20 g/m³ treated |
| Waste leachability | Below TCLP hazardous threshold |

## 6. Deployment Modes

### Household mode
- Capacity: **20–40 L/day**
- Use case: single family tube well
- PV: 30 W
- Battery: 12.8 V, 10 Ah
- Treatment cost: ~$0.05–0.10/m³

### Community mode
- Capacity: **0.5–2 m³/day**
- Use case: school, clinic, neighborhood water kiosk
- PV: 80–150 W
- Battery: 12.8 V, 20–40 Ah
- Treatment cost: ~$0.02–0.06/m³

### Utility-fringe mode
- Capacity: **5–20 m³/day**
- Use case: peri-urban standpipes / small piped systems
- Multiple parallel capture columns with shared regeneration and ceramic stabilization module

## 7. Advantages Over Current Practice

| Challenge with existing systems | EARN response |
|---|---|
| As(III) breakthrough | On-demand ferrate oxidation converts As(III) to easily captured As(V) |
| Cartridge exhaustion | Electro-regenerated sorbent bed cuts recurring replacement |
| Chemical supply dependence | Oxidant and fresh iron surfaces generated electrically on site |
| Toxic sludge dumping | Residue immobilized as ceramic pellets |
| Weak monitoring | Built-in low-cost verification and remote logging |

## 8. Key Risks and Mitigations

- **Phosphate competition reduces adsorption capacity** → use higher Fe:As dosing ratio, dual-stage bed, and community-mode sensor verification.
- **Electrode fouling from silica or hardness** → periodic polarity reversal and weak-acid maintenance rinse.
- **Regeneration complexity at household scale** → simplify household units to swap-in micro-regeneration cartridges serviced by local entrepreneurs.
- **Kiln misuse or disposal failures** → centralize ceramic stabilization at village service hubs where household systems are aggregated.

## 9. Feasibility Horizon

All major components already exist in adjacent fields:
- ferrate electrochemistry,
- iron electrocoagulation,
- magnetite/ferrihydrite arsenic adsorption,
- ceramic toxic-metal immobilization,
- low-cost solar DC water systems.

The invention is a **10–20 year integration challenge**, not a physics breakthrough. The path to deployment is driven by electrochemical reliability, field-proof regeneration protocols, and low-cost arsenic verification.
