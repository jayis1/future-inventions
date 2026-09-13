# Specification — Circular PCB Electrorefinery

## 1. Design Objective

Recover reusable components and saleable material fractions from **20–100 kg/day** of printed circuit boards in a containerized plant with no routine liquid discharge, no open burning, no cyanide, and no aqua regia.

## 2. Process Architecture

```text
[Receipt + depower + XRF assay]
        -> [Low-oxygen induction desoldering + flexure]
        -> [Reusable component test / specialist fractions]
        -> [Water-submerged electrohydraulic delamination]
        -> [Density + eddy-current + screen separation]
        -> [Glycine base-metal leach]
        -> [Citrate tin loop]
        -> [Thiosulfate precious-metal loop]
        -> [Potential-stepped electrowinning]
        -> [Electrolyte regeneration + water recycle]
        -> [Glass filler / sealed resin solvolysis / residue cassette]
```

## 3. Feed Envelope

### Accepted

- Depowered rigid FR-4 and comparable glass-epoxy PCBs
- Common lead-free and legacy tin-lead solder boards after identification
- Populated boards after battery, lamp, mercury-switch, and large-capacitor removal
- Board panels up to **450 × 600 mm** after guarded size reduction

### Rejected or diverted

- Batteries and battery packs
- CRT glass, mercury lamps, toner, and liquid-containing devices
- Beryllium ceramics and components that cannot be positively identified
- Radioactive, medical-biological, explosive, or chemically contaminated electronics
- Flexible fluoropolymer-rich boards unless a validated recipe exists

## 4. Subsystems

### 4.1 Assay and safety cell

- Shielded handheld-class XRF sensor with interlocked sample chamber
- Machine-vision component segmentation
- Four-wire residual-voltage test and automated capacitor discharge
- Load cells with **±0.1%** batch-mass accuracy
- Local processing only; no storage of user data recovered from devices

### 4.2 Component liberation cell

- Nitrogen-recirculated chamber, **120–180°C** operating range
- Segmented induction coils, **5–30 kW peak**, **20–100 kHz**
- Servo flexure table, **0.5–3 Hz**, maximum board strain set below glass-fracture threshold
- Condenser, HEPA H13, alkaline halogen scrubber, and activated-carbon guard bed
- Oxygen maintained **<5%** during treatment of brominated FR-4

### 4.3 Electrohydraulic delamination

- Double-wall water vessel with replaceable spark-gap cartridge
- Pulse energy **0.5–3 kJ**, duration **1–20 µs**, repetition **0.2–2 Hz**
- Specific liberation energy target **0.15–0.6 kWh/kg**
- Closed-loop water filtration: 100 µm screen, 10 µm bag, 0.5 µm ceramic membrane
- Acoustic enclosure target **<80 dBA** at operator station

### 4.4 Hydrometallurgical loops

| Loop | Nominal chemistry | Operating window | Principal target |
|---|---|---|---|
| Base metal | Glycine **0.5–1.5 M** with oxygen or ferric mediator | pH **9–11**, **25–60°C** | Cu, Ni, Zn |
| Tin | Citrate **0.2–0.8 M** with controlled oxidation | pH **3–6**, **40–70°C** | Sn |
| Precious metal | Thiosulfate **0.1–1.0 M** with Cu/Fe redox catalyst | pH **8–10**, **20–50°C** | Au, Ag, Pd-rich residue |

Final chemistry must be selected from pilot selectivity and toxicology results. Incompatible electrolytes remain in physically separate, color-coded circuits.

### 4.5 Electrowinning and regeneration

- Modular flow-through carbon felt, titanium, and 316L electrode cassettes
- Reference-electrode-controlled cathode potential, **±10 mV** regulation target
- Current density **50–500 A/m²** according to metal and mass transfer
- Cation-, anion-, and bipolar-membrane cells for ion separation and acid/base regeneration
- Pulsed reverse-current stripping for removable powder or foil product
- Hydrogen monitoring and forced ventilation; cell headspace held below **10% of hydrogen LEL**

### 4.6 Residue finishing

- Glass-rich fraction wash to **<100 mg/kg** leachable total regulated metals, subject to local standards
- Optional geopolymer filler blending only after TCLP-equivalent leach testing
- Resin solvolysis/pyrolysis: **350–450°C**, oxygen **<1%**, sealed condenser train
- Two-stage alkaline bromide scrubber plus activated carbon
- Final nonconforming material locked into serialized UN-rated residue cassettes

## 5. Control and Mass Balance

Each batch receives a process passport containing:

- input mass and XRF composition estimate
- recipe, energy, water, and reagent additions
- dissolved-metal inventory by loop
- plated-metal mass and purity
- component, glass, organic, salt, filter, and residue outputs
- unresolved mass and alarm history

Product release requires **>99% mass-balance closure** after correcting for sampled material, evaporation, oxygen uptake, and analytical uncertainty. A failed balance locks liquid-transfer and residue-dispatch valves pending supervisor review.

## 6. Performance Targets

| Parameter | 20 kg/day unit | 100 kg/day unit |
|---|---:|---:|
| Installed footprint | 20–30 m² | 35–55 m² |
| Connected electrical load | 15–30 kW | 50–100 kW |
| Specific electricity | 2.0–4.0 kWh/kg | 1.5–3.5 kWh/kg |
| Fresh-water makeup | <0.8 L/kg | <0.5 L/kg |
| Process-water recycle | >95% | >97% |
| Copper recovery | >97% | >97% |
| Tin recovery | >95% | >95% |
| Au/Ag recovery | >95% | >95% |
| Palladium recovery | >90% | >90% |
| Routine liquid discharge | zero | zero |
| Non-recoverable hazardous residue | <5% feed | <3% feed |

## 7. Product Specifications

- **Copper:** >99.5% after one electrowinning pass; >99.9% with optional electrorefining
- **Tin:** >98%, sold to secondary refiner where local purification is unavailable
- **Gold/silver concentrate:** >95% combined recovery; final purity may be completed at a regional precious-metal refiner
- **Reusable components:** electrically screened, traceable by batch, sold with measured rather than assumed functionality
- **Glass/mineral filler:** released only after leach and bromine limits are independently met
- **Organic oil:** analyzed for bromine and persistent organic pollutants before industrial reuse; otherwise retained for licensed destruction

## 8. Safety Interlocks

The plant enters a safe, isolated state upon:

- sump liquid detection
- hydrogen above **10% LEL**
- chamber oxygen above recipe limit
- scrubber pH or halogen breakthrough alarm
- reactor overtemperature or overpressure
- electrolyte tank high-high level
- XRF shutter fault
- mass-balance discrepancy above allowed analytical uncertainty

Operators never manually pour loaded electrolyte. All chemical transfers use dry-break keyed couplings, and maintenance requiring open process contact is reserved for trained regional technicians.

## 9. Validation Gates

1. **Liberation:** >90% copper-laminate interfacial separation with <10% of feed converted to <100 µm fines.
2. **Selectivity:** demonstrate target recoveries over at least 20 representative board classes without irreversible ligand poisoning.
3. **Closure:** 100 consecutive batches at >99% mass-balance closure.
4. **Exposure:** independent monitoring below applicable occupational limits for Pb, brominated compounds, acid mist, dust, and noise.
5. **Products:** 12-month confirmation that glass filler and organic products remain within leach and emissions requirements.
6. **Economics:** positive operating margin on realistic mixed-grade feed without attributing high-grade precious-metal content to low-grade boards.

## 10. Development Constraints

- Reuse and repair take priority over material recovery.
- The unit may not process data-bearing devices until data destruction or owner-authorized recovery occurs outside the refinery.
- No discharge claim includes service events: removed electrolyte, filters, and residue remain regulated materials until verified recovery or disposal.
- The system must not shift hazardous chemistry from an informal worker to an unmonitored regional hub; downstream chain-of-custody is part of certification.

## 11. Feasibility Basis

The design integrates demonstrated unit operations—induction desoldering, pulsed-power fragmentation, amino-acid complexation, thiosulfate leaching, membrane electrolysis, electrowinning, XRF assay, and sealed polymer conversion. Research risk lies in robust selectivity, ligand lifetime, mixed-feed control, and economical miniaturization. A 10–20 year horizon is credible if development begins with a narrow certified feed envelope and expands only after independent environmental validation.
