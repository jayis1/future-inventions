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

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/kidney-disease — WHO: Kidney disease
[2] https://pubmed.ncbi.nlm.nih.gov/25777665 — Worldwide access to treatment for end-stage kidney disease
[3] https://pmc.ncbi.nlm.nih.gov/articles/PMC10240485 — Portable, wearable and implantable artificial kidney systems
[4] https://pmc.ncbi.nlm.nih.gov/articles/PMC11068938 — Resource consumption of modern-day hemodialysis systems
[5] https://pmc.ncbi.nlm.nih.gov/articles/PMC4936831 — A wearable artificial kidney for patients with end-stage renal disease
