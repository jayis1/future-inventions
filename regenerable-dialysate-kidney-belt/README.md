# Regenerable Dialysate Kidney Belt

**A wearable, low-water hemodialysis system that continuously cleans a small dialysate loop and transfers toxic ammonia into a dock-regenerated capture cartridge.**

- **Author:** jayis1
- **Status:** Concept (TRL 2)
- **Development horizon:** 10–15 years to supervised community use

## Problem

An estimated **674 million people live with chronic kidney disease**, mostly in low- and middle-income countries, and kidney failure requires dialysis or transplantation to sustain life.[1] Access remains profoundly unequal: worldwide use of kidney-replacement therapy was projected to exceed 5.4 million people by 2030, while the underlying access study found a large untreated population and called for lower-cost treatment.[2]

Conventional hemodialysis ties a person to a clinic for several hours, usually three times each week. It also depends on reliable electricity, trained staff, a water-treatment plant, and a large water supply. A conventional four-hour treatment has historically required roughly **500 L of input water**, much of it rejected by reverse osmosis rather than used as dialysate.[4] These infrastructure demands make continuous treatment difficult during disasters and place routine dialysis beyond reach in many rural and low-income regions.

Portable and wearable artificial-kidney research has shown that a small recirculating dialysate volume can replace hundreds of litres of single-pass fluid, but current sorbent trains still face hard limits: urease converts urea into more-toxic ammonium; zirconium-phosphate capture is bulky and finite; ammonia breakthrough is dangerous; and blood access, clotting, bubbles, leaks, battery failure, and infection all require fail-safe control.[3][5]

## Solution

The **Regenerable Dialysate Kidney Belt (RDKB)** is a 5–7 kg wearable hemodialysis appliance used only under nephrology supervision. Blood passes through a commercial high-flux hollow-fibre dialyzer while **2.5–3.5 L of dialysate** circulates through a sealed regeneration loop:

1. **Remove broad-spectrum toxins.** Activated carbon captures protein-bound organics and drug residues; hydrous zirconium oxide binds phosphate; a replaceable mixed-bed guard captures trace metals and oxidants.
2. **Convert urea predictably.** Immobilized urease in a physically retained enzyme cartridge hydrolyses urea into ammonium and bicarbonate. A conductivity, pH, and redundant ammonia-sensor bank measures the resulting load.
3. **Transfer ammonia instead of storing it in kilograms of sorbent.** In a chemically isolated side loop, bipolar-membrane electrodialysis generates a controlled alkaline stream. This converts NH4+ to dissolved NH3, which crosses a hydrophobic expanded-PTFE hollow-fibre membrane into a sealed citric-acid receiver. The membrane contactor never contacts blood.
4. **Fail safe.** A final zirconium-phosphate guard cartridge is sized for emergency capture, not the full daily load. Any ammonia, pressure, air, blood-leak, temperature, or conductivity fault stops the blood pump, clamps both access lines, and returns blood using stored mechanical energy.
5. **Regenerate at a community dock.** After each 8–12 hour session, a tamper-evident dock heat-disinfects the dialysate path, tests membrane integrity, rebalances electrolytes and bicarbonate, recharges the battery, and uses electrodialysis to reconcentrate citric acid. Captured nitrogen leaves as a small, traceable ammonium-salt stream for licensed fertilizer processing or wastewater treatment.

### Quantitative design targets

| Metric | Design target |
|---|---:|
| Wearable mass, including battery and fluids | 5–7 kg |
| Dialysate inventory | 2.5–3.5 L |
| Worn treatment duration | 8–12 h/day |
| Blood flow | 80–120 mL/min |
| Dialysate flow | 120–200 mL/min |
| Daily urea processing capacity | 20 g/day |
| Ammonia-equivalent transfer capacity | >=12 g/day |
| Electrical energy | <300 Wh per 12 h session |
| Fresh-water makeup | <2 L/day, excluding cleaning validation |
| Alarm-to-dual-clamp time | <1 second |
| Ammonia after final guard | <0.5 mg/L, with automatic shutdown above validated limit |
| Disposable mass | <150 g/day |

These are **research targets**, not present clinical performance. Clearance adequacy must be demonstrated by standard Kt/V, weekly clearance, electrolyte, fluid-balance, and patient-outcome measures; longer treatment is not automatically adequate treatment.

## Key Innovation

Existing wearable-dialysis concepts typically treat the ammonium made by urease as a solid-sorbent storage problem. The RDKB treats it as a **selective mass-transfer problem**. Its key innovation is a three-barrier ammonia shuttle:

- urease makes urea measurable and ionizable;
- pH-gated membrane stripping moves only volatile ammonia across an ePTFE contactor into a sealed acid receiver; and
- a small downstream zirconium-phosphate cartridge catches breakthrough while independent sensors verify safety.

Moving the daily nitrogen load into a liquid receiver makes the bulk capture medium regenerable at a shared dock instead of requiring more than a kilogram of fresh zirconium sorbent for each day of use. The belt-to-dock architecture keeps high-energy sanitation and acid/base regeneration off the patient while preserving a light, continuously operating treatment loop.

The mechanism uses established dialysis membranes, urease chemistry, gas-permeable membrane contactors, ion-exchange membranes, activated carbon, and electrodialysis. The 10–15 year challenge is not a new law of physics; it is proving selective ammonia transfer, sterile longevity, sensor reliability, hemocompatibility, and safe human-factors integration over millions of cycles.

## Target Cost

At production above 100,000 units/year:

- **Belt:** US$3,000–5,000 ex-factory, designed for five years of service.
- **Community dock:** US$15,000–25,000 serving 20–30 belts.
- **Consumables and service:** US$5–12 per treatment day, including dialyzer, anticoagulation set, enzyme/guard cartridge allocation, testing, sanitation, and battery reserve.
- **Financing target:** below US$3,000 per patient-year after equipment amortization, excluding clinical labour and vascular-access surgery.

The access model is cooperative ownership by clinics, dialysis programmes, or humanitarian networks. Patients should not be required to purchase the belt, maintain clinical software, or sell personal data. Local service centres replace pumps, batteries, seals, and cartridges using standardized modules.

## Impact

If validated and deployed to **one million people**, the system could:

- expand kidney-replacement access beyond water-intensive dialysis centres;
- enable longer, gentler treatment while patients sleep, study, work, or remain with family;
- avoid up to **78 billion L/year of conventional hemodialysis input-water demand**, using the 500 L/treatment baseline and three treatments per week as the comparator;[4]
- shrink emergency logistics from tanker water and large dialysate stocks to sterile disposables, power, and dock supplies; and
- reduce treatment disruption during droughts, floods, conflict displacement, and grid outages.

The device is intended to extend clinical care, not automate away clinicians. It records treatment chemistry and machine events locally, carries no microphone, camera, or location tracker, and has no advertising or identity-scoring function. Patients control export of their records except where immediate safety or applicable medical regulation requires otherwise.

## Safety, Access, and Limits

- **Clinical risk dominates:** Vascular access, anticoagulation, haemolysis, air embolism, infection, hypotension, electrolyte error, and ammonia breakthrough can be fatal. Initial use must be in monitored trials, followed by trained-home use only if evidence supports it.
- **No single sensor is trusted:** Ammonia, pressure, air, temperature, conductivity, blood leak, and pump position use independent sensing or physical interlocks. The final sorbent guard must safely absorb the maximum load produced during shutdown and blood return.
- **Sanitation is verified, not assumed:** The dock runs heat/chemical disinfection, leak testing, conductivity calibration, and microbiological/endotoxin sampling. A failed check locks out treatment.
- **Equity is a design input:** Controls use symbols, audio, haptics, and local languages; the belt can operate offline; consumables use globally manufacturable polymers and carbons; and battery/pump modules are field-replaceable.
- **Nitrogen is not automatically fertilizer:** The ammonia receiver is a clinical waste stream until drug residues, metals, pathogens, and local regulations permit recovery.
- **Transplantation and prevention remain preferable:** The belt does not cure kidney disease, replace transplantation, or reduce the need for prevention and early care.

See [SPECIFICATION.md](./SPECIFICATION.md) for the architecture, first-order mass balance, safety case, validation programme, and scale-up risks.

## How It Works

The RDKB separates treatment into three controlled circuits. In the blood circuit, a peristaltic pump moves 80–120 mL/min through a 0.6–1.0 m² high-flux polyethersulfone or cellulose-triacetate dialyzer. Urea, creatinine, potassium, phosphate, and water cross the membrane into counterflowing dialysate; blood never contacts a reusable pump or regeneration chemical. Independent arterial, venous, air, temperature, and blood-leak monitors supervise this life-critical path.

The 2.5–3.5 L dialysate circuit then restores that fluid for reuse. Activated coconut-shell carbon captures organics, hydrous zirconium oxide removes phosphate, and immobilized urease converts up to 20 g/day of urea into approximately 11.3 g of ammonia equivalent. A pH-gated slipstream shifts ammonium toward volatile ammonia at pH 10.5–11.2. Ammonia crosses hydrophobic ePTFE hollow fibres into 250 mL of 1.5–2.0 mol/L citric acid, while the treated dialysate is neutralized and checked before returning to the dialyzer. A 150–300 g zirconium-phosphate guard catches breakthrough during detection and shutdown.

A precision balancing chamber and dedicated ultrafiltration pump meter removed water into a sealed bag. At session end, the dock—not the wearer—performs 80–90 °C disinfection, integrity testing, sensor challenge, electrolyte rebalancing, battery charging, and receiver regeneration. Any unsafe ammonia, pH, conductivity, pressure, air, leak, temperature, or volume reading bypasses the dialyzer and triggers a hardware-backed stop, dual clamp, and controlled blood return.

## Technical Architecture

The belt is organized as five replaceable subsystems connected through explicit safety boundaries:

1. **Disposable blood module:** dialyzer, PVC-free tubing, access sensors, venous air trap, spring-closed clamps, and a mechanically reserved blood-return path.
2. **Reusable dialysate cassette:** reservoir, carbon and phosphate beds, urease reactor, 0.2 µm particle barrier, balancing chamber, ultrafiltration pump, and keyed electrolyte dosing.
3. **Ammonia-transfer module:** bipolar-membrane electrodialysis, alkaline slipstream, ePTFE contactor, double-contained citric-acid receiver, neutralization stage, and final guard cartridge.
4. **Power and control module:** 350–450 Wh LiFePO4 battery; therapy and safety processors; redundant pH, conductivity, ammonia, flow, pressure, level, and temperature channels; signed offline-capable firmware.
5. **Shared dock:** sanitation, calibration, membrane pressure-decay testing, acid/base recovery, nitrogen-waste containment, battery diagnostics, and cassette lockout.

During treatment, sensor data flows to both processors, but the safety processor alone controls hard relays, clamps, heater isolation, and pump power. Prescription software may request flow or dosing only inside mechanically and electronically enforced limits. Mass-balance data compare reservoir level, ultrafiltration volume, receiver gain, and pump displacement; disagreement quarantines the dialysate. After treatment, the dock receives maintenance and therapy logs through an authenticated physical link. Network loss cannot interrupt a session, and remote software cannot override hard safety limits.

## Performance Benchmarks

All RDKB figures below are **engineering targets, not measured clinical results**. Comparators describe established treatment classes and published wearable-artificial-kidney research; equivalence must be proven in staged trials.[3][5]

| Measure | Current comparison | RDKB development target |
|---|---|---:|
| Treatment pattern | In-centre HD commonly ~4 h, 3 times/week | 8–12 h/day, clinician prescribed |
| Blood flow | Conventional HD commonly operates at several hundred mL/min; wearable prototypes use lower flows | 80–120 mL/min |
| Dialysate supply | Single-pass HD uses a large continuous supply; historical input-water demand is ~500 L/session[4] | 2.5–3.5 L recirculating inventory; <2 L/day makeup, sanitation reported separately |
| Urea processing | Adequacy assessed by delivered clearance/Kt/V, not time alone | 20 g/day reactor load; non-inferior prescribed weekly clearance |
| Ultrafiltration | Current machines use balancing systems with clinical supervision | <30 mL cumulative error over 12 h and <0.5% of programmed volume, subject to standards review |
| Wearable mass | Research WAK systems demonstrate portability but remain investigational[3][5] | 5–7 kg including fluid and battery |
| Power | Clinic machines rely on mains power and water infrastructure | <25 W average; <300 Wh per 12 h; shutdown reserve retained |
| Safety response | Commercial machines alarm and stop under fault conditions | access disconnection to dual clamp in <1 s; independent ammonia channels |
| Consumables | Conventional care uses dialysate concentrates, water-treatment supplies, and blood sets | <150 g/day disposable mass plus regulated liquid concentrate |

The decisive benchmark is not miniaturization alone. A viable system must deliver prescribed solute and fluid removal, keep ammonia below a validated exposure limit under normal and single-fault conditions, complete at least 95% of sessions over a 12-month access trial, and show that lower water use does not shift unacceptable burden into energy, cartridges, infection risk, or hospitalization.

## Deployment Scenarios

### Supervised home and overnight therapy

A trained patient connects with remote clinical support, wears the belt for an 8–12 hour prescribed session, and returns the cassette to a clinic-managed dock each day. Longer, slower treatment could reduce peak fluid shifts and travel compared with thrice-weekly in-centre schedules, but deployment begins only after stationary and supervised ambulatory trials demonstrate safe access management, alarm response, and treatment adequacy.

### Rural community dialysis cooperative

A district clinic operates one dock for 20–30 belts, maintains spare pumps and batteries, and provides vascular-access, laboratory, and prescription services. The model substitutes modular cassettes and less than 2 L/day of treatment makeup water per patient for a large reverse-osmosis plant, while sanitation water, certified concentrates, waste handling, and trained staff remain mandatory. Offline operation supports weak connectivity without weakening clinical oversight.

### Disaster-continuity unit

Hospitals or humanitarian teams pre-position belts, sterile blood sets, charged batteries, and a containerized dock where tanker water and clinic capacity are constrained. The system is not a self-treatment shortcut: patient selection, chemistry testing, access care, consumable traceability, and a route to conventional dialysis are required. Its advantage is logistical density—hundreds of patient-sessions supported by power and compact supplies rather than continuous delivery of treated water.

## Risks & Mitigations

| Risk | Engineering and clinical mitigation |
|---|---|
| Ammonia breakthrough or wrong electrolyte composition | Diverse ammonia sensing, finite guard capacity, pH/conductivity checks, dose accounting, dialyzer bypass, physical lockout, and dock challenge tests before every release |
| Air embolism, access disconnection, blood leak, haemolysis, or clotting | Redundant pressure/air/blood-leak sensing, default-closed clamps, controlled return reserve, non-interchangeable disposables, clinician-set anticoagulation, and single-fault testing in every orientation |
| Infection, biofilm, or endotoxin | Single-use blood path, validated heat/chemical sanitation, microbial and endotoxin surveillance, sealed cassette, lot traceability, and mandatory replacement intervals |
| Membrane wetting, sorbent exhaustion, or urease loss | Differential pressure and mass-balance monitoring, retained enzyme beds, particle barriers, conservative service life, receiver-volume checks, and safe transition to conventional care |
| Excess ultrafiltration or hypotension | Independent balancing chamber, hard hourly and cumulative limits, symptom and blood-pressure checks, clinician prescription, and no autonomous optimization from consumer wearables |
| Battery, thermal, software, or cyber failure | LiFePO4 isolation, thermal fuses, shutdown-energy reserve, dual processors, signed firmware, rollback protection, offline therapy, encrypted service links, and immutable hardware limits |
| Burden, falls, dermatitis, or alarm fatigue | 5–7 kg mass ceiling, load-distributing harness, skin-safe materials, human-factors trials, graded alarms, rapid disconnect training, and patient-controlled adoption |
| False confidence or inequitable rollout | Investigational labeling, published adverse-event and uptime data, independent auditing, subsidized cooperative ownership, multilingual controls, and guaranteed conventional-care fallback |

No mitigation makes this concept ready for unsupervised use. Biocompatibility, electrical safety, EMC, sterilization, software lifecycle, risk management, usability, animal testing, and staged human trials remain hard gates—not paperwork to be deferred until scale.

## Vision for 2050

By 2050, a mature RDKB network could make dialysis infrastructure look less like a destination and more like a utility. Community docks in pharmacies, rural clinics, apartment buildings, and mobile hospitals could service standardized cassettes, while regional centres provide nephrology, laboratory monitoring, access surgery, and emergency backup. Patients who choose wearable therapy could receive slower treatment at home or during ordinary activity without surrendering three days each week to travel and a clinic chair.

At one million users, meeting the design target would replace much of the historical 500 L-per-session input-water demand—up to 78 billion L/year on the comparison assumptions already stated—while creating new obligations: reliable cartridge supply, renewable electricity, battery take-back, licensed nitrogen-waste processing, transparent algorithms, and universal reimbursement. Open interfaces and audited safety data could prevent a few vendors from turning life-support treatment into a locked subscription.

Success in this world is not measured by making clinicians disappear. It is measured by more people receiving adequate therapy, fewer missed treatments during drought or conflict, and the ability to choose where life happens. Transplantation, prevention, and regenerative medicine remain preferable; the belt becomes a resilient bridge and long-term option where those paths are unavailable.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/kidney-disease — WHO: Kidney disease
[2] https://pubmed.ncbi.nlm.nih.gov/25777665 — Worldwide access to treatment for end-stage kidney disease
[3] https://pmc.ncbi.nlm.nih.gov/articles/PMC10240485 — Portable, wearable and implantable artificial kidney systems
[4] https://pmc.ncbi.nlm.nih.gov/articles/PMC11068938 — Resource consumption of modern-day hemodialysis systems
[5] https://pmc.ncbi.nlm.nih.gov/articles/PMC4936831 — A wearable artificial kidney for patients with end-stage renal disease
