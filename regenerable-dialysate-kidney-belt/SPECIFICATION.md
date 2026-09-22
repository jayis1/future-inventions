# Regenerable Dialysate Kidney Belt — Technical Specification

- **Author:** jayis1
- **Revision:** Concept 0.1
- **System type:** Wearable sorbent-regenerated hemodialysis with docked sanitation
- **Intended horizon:** 10–15 years
- **Regulatory premise:** Investigational life-support medical device; prescription and clinical supervision required

## 1. System Boundary

The RDKB builds on demonstrated portable and wearable artificial-kidney research while changing the nitrogen-removal architecture.[3][5] It consists of a patient-worn belt, a single-use blood circuit and dialyzer, a reusable dialysate-regeneration cassette, a sealed ammonia receiver, and a clinic/community dock. No dialysate or regeneration chemical crosses directly into blood; transport between blood and dialysate occurs only across the qualified dialyzer membrane.

```text
PATIENT BLOOD LOOP
vascular access -> air/pressure monitors -> blood pump -> high-flux dialyzer
       ^                                                      |
       +--------- venous air trap <- emergency return <-------+
                                      ||
                            dialyzer membrane barrier
                                      ||
DIALYSATE LOOP
3 L reservoir -> carbon -> phosphate sorbent -> urease reactor
       ^                                           |
       |                                           v
release chemistry <- final NH4 guard <- ammonia-transfer module
       |
       +---------------- dialyzer counterflow -----------------+

DOCK
heat disinfection | integrity test | acid/base regeneration
battery charging  | calibration    | nitrogen concentrate removal
```

## 2. Clinical Operating Envelope

| Parameter | Target range | Hard response concept |
|---|---:|---|
| Worn session | 8–12 h | planned blood return at session limit |
| Blood flow | 80–120 mL/min | dual clamp outside validated band |
| Dialysate flow | 120–200 mL/min | bypass dialyzer and alarm |
| Blood-loop pressure | patient-specific validated envelope | stop pump, clamp, return if safe |
| Dialysate temperature | 35–38 °C at dialyzer inlet | isolate heater and dialyzer |
| Dialysate pH | 6.8–7.6 | bypass and lock out |
| Conductivity | prescription-specific, dual channel | bypass and lock out |
| Ammonia after final guard | <0.5 mg/L target | immediate bypass, clamp, controlled return |
| Total dialysate volume | 2.5–3.5 L | level mismatch triggers leak protocol |

Exact clinical limits must be established under applicable dialysis-device standards and human trials; table values are engineering starting points, not treatment instructions.

## 3. Blood Circuit

### 3.1 Disposable wetted path

- Medical-grade PVC-free thermoplastic elastomer or silicone tubing with validated low-extractable formulation.
- High-flux polyethersulfone or cellulose-triacetate hollow-fibre dialyzer, 0.6–1.0 m² initial membrane area.
- Peristaltic blood pump so reusable actuator hardware never contacts blood.
- Venous air trap, ultrasonic bubble detector, optical blood-leak detector, and two normally closed spring clamps.
- Pressure sensing at arterial access, dialyzer inlet/outlet, and venous return.

### 3.2 Emergency blood return

A preloaded spring accumulator or isolated 50–100 mL saline pouch provides controlled return if electrical power is lost. Mechanical clamps default closed. The design must demonstrate that no single electronic failure can leave both access lines open or pump air toward the patient.

### 3.3 Anticoagulation

Regional citrate and low-dose heparin are candidate modes, selected by clinicians. The device does not infer dose autonomously. Any anticoagulant pump uses independent position feedback, a hard hourly-volume limit, and a physically non-interchangeable reservoir.

## 4. Dialysate Regeneration Train

### 4.1 Carbon and middle-molecule stage

- 250–500 g steam-activated coconut-shell carbon with medical-grade low-dust coating.
- Optional macroporous polystyrene-divinylbenzene resin for selected protein-bound uraemic toxins.
- 0.2 µm downstream particle barrier and differential-pressure monitoring.

### 4.2 Phosphate and trace-ion stage

Hydrous zirconium oxide binds phosphate without releasing clinically significant counter-ions. A mixed-bed polishing layer captures oxidants, trace metals, and degradation products. Each lot is tested for leachables, endotoxin, pressure drop, capacity, and sterilization compatibility.

### 4.3 Urease stage

Urease is covalently immobilized on porous silica or cross-linked alginate-silica beads retained by two membranes. The reactor target is 20 g urea/day with less than 0.1% enzyme-carrier mass loss over the validated service interval.

Reaction:

`CO(NH2)2 + H2O -> 2 NH3 + CO2`

At dialysate pH, most product exists as NH4+. Processing 20 g of urea creates approximately 11.3 g ammonia equivalent, establishing the receiver and guard capacity floor.

## 5. Ammonia-Transfer Module

### 5.1 Principle

A secondary micro-loop takes a slipstream after the urease reactor. Bipolar-membrane electrodialysis supplies base to raise only this isolated slipstream to pH 10.5–11.2, shifting NH4+ toward volatile NH3. The liquid then passes through ePTFE or polypropylene hollow fibres. Ammonia diffuses across the hydrophobic gas-filled pores into 1.5–2.0 mol/L citric acid, where it is protonated and trapped.

The treated slipstream is neutralized and recombined only after pH, conductivity, ammonia, and volume checks. Acid and base compartments are double-contained from patient-accessible surfaces.

### 5.2 Receiver capacity

A 250 mL receiver containing 2 mol/L triprotic citric acid provides 1.5 mol of nominal proton capacity. The 20 g/day urea design case produces about 0.67 mol ammonia, leaving more than a twofold stoichiometric margin before derating for kinetics, ionic strength, and incomplete utilization.

### 5.3 Safety guard

A 150–300 g zirconium-phosphate cartridge follows the transfer module. It is sized to absorb the validated worst-case ammonia inventory during detection, shutdown, and blood return—not the full routine daily load. Two ammonia sensors use different principles where possible: an ion-selective electrode plus a gas-diffusion/optical indicator. Their signals are compared continuously.

### 5.4 Open research questions

- Selectivity and wetting resistance of the membrane contactor in protein- and surfactant-containing dialysate.
- Ammonia-transfer coefficient across temperature, flow, ionic-strength, and pH ranges.
- Bipolar-membrane current efficiency at wearable scale.
- Long-term urease activity and microbial control.
- Safe discrimination of ammonia-sensor drift from real breakthrough.

## 6. Electrolyte and Acid-Base Control

Sodium, potassium, calcium, magnesium, chloride, and bicarbonate are monitored through conductivity plus periodic ion-selective measurements. Concentrated electrolyte reservoirs are keyed, barcoded, mechanically dose-limited, and located downstream of regeneration but upstream of two mixing volumes. No software command alone can deliver more than the prescription envelope.

Bicarbonate formed by urease is included in the charge and mass balance. Excess bicarbonate and counter-ion drift are corrected at the dock or by a validated microdosing subsystem; the device must never treat conductivity as a complete surrogate for composition.

## 7. Fluid Removal

A precision balancing chamber compares dialysate sent to and returned from the dialyzer. A separate ultrafiltration pump removes prescribed plasma water into a sealed graduated bag. Target cumulative error is less than 30 mL over 12 hours and less than 0.5% of programmed ultrafiltration volume, whichever is stricter after standards review.

Patient weight, symptoms, blood pressure, and clinician prescription remain authoritative. The device does not automatically optimize fluid removal from wearable-sensor data.

## 8. Power and Mechanical Design

| Load | Average target | 12 h energy |
|---|---:|---:|
| Blood pump | 5–8 W | 60–96 Wh |
| Dialysate and side-loop pumps | 3–5 W | 36–60 Wh |
| Electrodialysis and dosing | 3–7 W | 36–84 Wh |
| Heating and insulation losses | 2–4 W | 24–48 Wh |
| Sensors, controller, alarms | 1–2 W | 12–24 Wh |
| **System target** | **<25 W average** | **<300 Wh** |

A 350–450 Wh lithium-iron-phosphate battery provides one session plus shutdown reserve. Cells are physically separated from the blood circuit, use redundant over-temperature protection, and are swapped only at the dock. Future solid-state batteries may reduce mass but are not required for feasibility.

The mass target is 5–7 kg: 2.5–3.5 kg fluid, 1.2–1.8 kg battery, 0.8–1.2 kg pumps/electronics/frame, and 0.5–1.0 kg regeneration media and disposables.

## 9. Controls, Privacy, and Cybersecurity

- Safety controller and therapy controller are separate processors with a one-way therapy-to-safety command boundary.
- Signed firmware, measured boot, rollback protection, and a physical service switch are required.
- The belt completes a safe session offline; loss of network access cannot interrupt treatment.
- Local storage contains only therapy parameters, alarms, and maintenance data. No camera, microphone, GPS, advertising identifier, or always-on cloud telemetry is fitted.
- Patients approve routine record export. Emergency and legally required reporting are minimized to necessary medical data.
- A malicious or corrupted update cannot alter hard pump, heater, anticoagulant, ammonia, or ultrafiltration limits.

## 10. Dock Architecture

One dock serves 20–30 belts and performs:

1. 80–90 °C heat disinfection where materials permit, with validated chemical fallback;
2. automated pressure-decay and membrane-integrity tests;
3. ammonia-sensor challenge and conductivity/pH calibration;
4. electrodialytic acid/base recovery from the ammonia receiver;
5. electrolyte concentrate preparation from certified inputs;
6. battery charging and health measurement;
7. nitrogen-concentrate containment and chain-of-custody logging; and
8. microbiological/endotoxin sampling at a risk-based frequency.

A failed sanitation, calibration, integrity, or traceability check physically locks the cassette and belt from use.

## 11. Failure Modes and Required Responses

| Hazard | Detection | Safe response |
|---|---|---|
| Venous air | dual ultrasonic/optical path | stop pump; close venous and arterial clamps |
| Blood leak through dialyzer | optical detector plus pressure balance | isolate dialyzer; controlled return if safe |
| Ammonia breakthrough | two independent sensors and guard-capacity model | bypass dialyzer; stop urease flow; alarm; return blood |
| High/low conductivity or pH | dual channels plus dose accounting | quarantine dialysate; no patient exposure |
| Access disconnection | pressure transient and blood/moisture patch | dual clamp in <1 second |
| Pump runaway | motor encoder plus independent flow/position limit | remove power through safety relay |
| Power loss | hardware interrupt and mechanical reserve | controlled blood return; default-closed clamps |
| Membrane-contactor wetting | differential pressure, receiver conductivity, volume balance | isolate ammonia module and end session |
| Overheating | dual temperature sensors and thermal fuse | heater isolation; bypass until safe |
| Software or network failure | watchdog and safety-controller disagreement | frozen safe prescription or controlled shutdown |

Formal hazard analysis must include FMEA, fault-tree analysis, usability engineering, cybersecurity threat modelling, and verification against applicable IEC 60601, ISO 14971, biocompatibility, haemodialysis, and sterilization standards.

## 12. Verification Programme

### Stage A — Benchtop mass balance

- Process synthetic dialysate equivalent to 5, 10, 15, and 20 g/day urea loads.
- Close carbon, nitrogen, sodium, potassium, bicarbonate, water, and electrical balances to 95–105%.
- Demonstrate ammonia receiver capacity and guard performance under deliberate sensor and membrane failures.
- Run at least 1,000 hours with drug, protein, lipid, and surfactant challenge mixtures.

### Stage B — Ex-vivo blood loop

- Verify haemolysis, clotting, complement activation, air handling, thermal control, pressure response, and extractables/leachables.
- Execute every single-fault condition with worst-case worn orientation, motion, temperature, and battery state.

### Stage C — Large-animal study

Compare 8–12 hour RDKB therapy with standard dialysis for urea, creatinine, phosphate, potassium, middle molecules, acid-base status, inflammation, coagulation, and haemodynamics. No human trial proceeds until ammonia containment remains below the validated limit under induced faults.

### Stage D — Guarded human feasibility

Begin with stationary in-clinic use, then seated mobility, supervised ambulatory use, and finally trained-home use. Endpoints include delivered clearance, ultrafiltration accuracy, serious adverse events, ammonia exposure, access complications, sleep/activity interference, device usability, and patient-reported outcomes.

### Stage E — Access demonstration

Operate community docks in at least three settings with different climates, water quality, grid reliability, languages, and service logistics. Publish downtime, cost, consumable mass, water and energy use, waste disposition, and equity outcomes.

## 13. Commercial Gates

The concept cannot be described as clinically viable until it demonstrates:

- non-inferior prescribed solute and fluid removal against the clinical comparator;
- no ammonia breakthrough under normal use and validated safe shutdown under worst-case single faults;
- at least 95% completed-session availability over 12 months;
- less than 2 L/day fresh-water makeup in routine operation, with sanitation water reported separately;
- less than 300 Wh per 12-hour session;
- less than 150 g/day disposable mass;
- five-year reusable-hardware life with field-replaceable wear components; and
- independent auditing of clinical outcomes, cybersecurity, lifecycle burden, and total cost.

## 14. End of Life

The aluminium or magnesium frame, LiFePO4 battery, motors, electronics, and membrane modules separate without destructive adhesives. The manufacturer takes back batteries, boards, pumps, and zirconium media. Blood-contact disposables follow regulated clinical-waste routes. Nitrogen receiver contents remain clinical waste unless analytical release and local law explicitly permit recovery.

## Sources

[3] https://pmc.ncbi.nlm.nih.gov/articles/PMC10240485 — Portable, wearable and implantable artificial kidney systems
[5] https://pmc.ncbi.nlm.nih.gov/articles/PMC4936831 — A wearable artificial kidney for patients with end-stage renal disease
