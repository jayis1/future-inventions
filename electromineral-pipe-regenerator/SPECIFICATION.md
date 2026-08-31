# Specification — Electromineral Pipe Regenerator

## 1. Design Objective

Create a retrofit platform that lowers lead release from existing plumbing to **<1 ppb typical**, **<5 ppb worst-case validated**, without immediate excavation, while preserving a pathway to eventual full pipe replacement.

## 2. Core Technical Architecture

```text
[Hydraulic isolation manifold]
        -> [Recirculation pump + conductivity / pH / ORP sensing]
        -> [Electromineral conditioning reactor]
        -> [Pipe-zone treatment loop]
        -> [MnOx capacitive polishing cell]
        -> [Ferric microfloc / 0.2 um polish filter]
        -> [Lead concentrate canister]
        -> [ASV verification cell]
        -> [Safe-water return / drain / maintenance module]
```

## 3. Materials Set

- **Mineral barrier precursors:** calcium acetate or calcium bicarbonate, sodium silicate, low-dose orthophosphate or phytate-derived phosphate, dissolved inorganic carbon
- **Passivation phases targeted:** hydroxyapatite, chloropyromorphite-like lead phosphate, calcium-silicate-hydrate, amorphous silica overlayer
- **Polishing electrodes:** birnessite-type MnO2 on reticulated carbon felt; activated carbon counterelectrode
- **Sacrificial co-capture stage:** ferric hydroxide microfloc or iron-oxide granules for transient particulate lead
- **Sensors:** bismuth-film anodic stripping voltammetry microcell, pH, conductivity, oxidation-reduction potential, turbidity, flow
- **Power system:** 24–48 V DC, 200–800 W peak portable service unit; optional 20–80 W permanent module

## 4. Mechanism of Action

### 4.1 Near-wall pH control
Pulsed cathodic polarization raises pH at the pipe wall without forcing the full bulk water out of potable range. That localized supersaturation drives mineral nucleation at corrosion defects where protection is needed most.

### 4.2 Insoluble lead fixation
Released Pb2+ reacts with phosphate to form extremely low-solubility lead phosphate phases. Silicate and calcium then overcoat and densify the surface, improving adhesion and lowering defect-driven dissolution.

### 4.3 Active spike suppression
Any soluble lead escaping the pipe during treatment or later disturbances is adsorbed and electrosorbed onto MnOx/carbon surfaces. Regeneration concentrates lead into a small recoverable brine/cake stream.

## 5. Quantitative Performance Targets

| Metric | Target |
|---|---:|
| Reduction in dissolved lead after rehabilitation | 90–99.5% |
| Typical post-treatment first-draw Pb | <1 ppb |
| Worst-case validated post-treatment Pb | <5 ppb |
| Treatment time, single-family residence | 4–12 hours |
| Treatment time, school / apartment riser zone | 1–3 days |
| Mineral liner thickness | 5–50 um |
| Barrier design life before major refresh | 5–15 years |
| Maintenance refresh interval | 6–24 months |
| Lead capture during rehab | >95% of mobilized dissolved Pb |
| Water use overhead during treatment | <1.5x treated system volume |

## 6. Deployment Model

### Household / small-building service
A portable cart is brought onsite, connected to the building loop, and run through mapping, conditioning, passivation, verification, and signoff in one visit.

### Institutional deployment
Schools, clinics, and apartment blocks receive zoned treatment plus a permanent point-of-entry maintenance module for continuous verification and periodic self-healing cycles.

### Utility partnership mode
Utilities use EPR to cut exposure risk in high-priority neighborhoods while capital replacement queues catch up.

## 7. Safety Constraints

- Treated buildings stay off potable use during conditioning and are flushed and sensor-cleared before release.
- Chemistry doses remain low enough to avoid heavy residuals after final flushing.
- Lead concentrate canisters are serialized for controlled recycling or hazardous-waste handling.
- System is prohibited for pipes already structurally unsound enough to require immediate replacement.

## 8. Comparison to Current Approaches

| Approach | Strength | Limitation |
|---|---|---|
| Full pipe replacement | Permanent | Slow, expensive, disruptive |
| Utility orthophosphate dosing | Broad coverage | Indirect, chemistry-sensitive, does not rehabilitate premise plumbing |
| Faucet filters | Immediate protection | Cartridge burden, user failure mode |
| **EPR** | Building-scale rehabilitation + sensing + polishing | Transitional, not a substitute for eventual replacement |

## 9. 10–20 Year Feasibility Basis

The invention depends on combining known classes of science, not inventing new physics:

- electrochemically controlled mineral deposition
- hydroxyapatite / lead-phosphate corrosion inhibition chemistry
- manganese-oxide sorption for Pb2+
- anodic stripping voltammetry for trace-metal sensing
- portable building-scale recirculation treatment skids

The frontier work is integration, process control, and proving long-term coating durability across heterogeneous real-world plumbing.
