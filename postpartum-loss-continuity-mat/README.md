# Postpartum Loss-Continuity Mat

**Author: jayis1**
**Status:** Research concept (TRL 2); not a validated clinical device or replacement for trained obstetric care.

## Problem

Postpartum haemorrhage affects an estimated 14 million women annually and causes around 70,000 deaths, according to WHO.[1] Visual blood-loss estimates can miss dangerous bleeding; WHO recommends objective measurement linked to a timely treatment bundle, not measurement alone.[4] At a change of bed, delivery position, or facility, the first blood-collection drape may be removed and the running total lost unless staff explicitly record it. The latter is a proposed workflow failure to investigate, not a measured prevalence claim.

## Solution

The **Postpartum Loss-Continuity Mat** is a disposable, graduated under-body drape with a gravity-fed outlet and two serial, transparent, detachable collection pouches. It is placed **after delivery of the baby**, where clinically appropriate, so that pre-placement amniotic fluid is not counted as postpartum blood. Each pouch is marked every 50 mL to 1,500 mL and has a mechanically closed inlet, a readable final-volume window, a write-on time/volume field, and a tear-off cumulative-volume tab. A midwife records the old pouch's final reading before sealing it; the next pouch remains attached to the same drape while care continues. For transfer, the sealed pouch and tab travel with the patient; a new mat is started with the previous measured total written on its first tab. No electronics, network, imaging, or patient identifier is required on the device.

> The device only measures liquid collected in its pouches. Blood on pads, floors, bedding, or inside gauze must be accounted for separately under local clinical protocol; fluid mixed with amniotic fluid or irrigation makes the measurement unreliable. A full, spilled, occluded, or unreadable pouch triggers immediate clinical assessment and an alternate approved measurement method, never a reassuring zero.

## Key Innovation

Calibrated postpartum drapes, reusable trays with overflow chambers, and two-bag amniotic-fluid separation already exist.[2][3] This proposal does **not** claim to invent volumetric blood measurement or to improve the proven E-MOTIVE treatment bundle. It tests a narrower integration: **a physically retained, sealed cumulative reading across pouch changes and patient transfers**, with a visible invalid-measurement state when fluid escapes. The challenge is to preserve the total without delaying clinical escalation or introducing measurement errors at handoff. Unlike this repository's footprint-verified phototherapy cot and ORS mix-witness cup, this is a maternal blood-loss collection and handoff device, not neonatal light delivery or oral-rehydration preparation.

### Design and validation targets (all unverified)

- **Materials and envelope:** heat-sealed translucent low-density polyethylene drape and pouches, polypropylene gravity outlet and captive pinch closure, water-resistant printed graduation and tab; 15–40 °C clinical-room use. No assumed chemical sensing or separation of blood from mixed fluid.
- **Volume:** each pouch 1,500 mL minimum rated capacity with a separate spill allowance to be determined in testing. Target error at the bedside within ±10% or ±50 mL, whichever is larger, for 100–1,500 mL of test fluid on a level bed; independently compare readings with a calibrated gravimetric reference using measured fluid density. Printed graduations must be tested after variable drape angles and pouch deformation.
- **Flow and changeover:** drain at least 0.5 L/min for a 0.3 m gravity head with no upstream pooling in a benchtop water test; replace a nearly full pouch without an open spout or spill in ≥95% of simulated changes. Water performance does not establish performance with clots, viscous blood, or placental tissue.
- **Handoff:** in a simulated two-pouch transfer, ≥95% of trained users should preserve the correct cumulative sum within ±50 mL without delaying the locally mandated emergency response. Compare against an ordinary calibrated drape plus written handoff, not visual estimation alone. Thresholds, observation intervals, and clinical actions come from current local/WHO protocols, not this prototype's markings.
- **Development horizon:** benchtop fluid and seal work in 2–3 years; usability, reprocessing/disposal evaluation and regulated clinical study within 5–10 years; wider adoption only after independent safety/effectiveness and procurement evaluation within 10–20 years.

## Target Cost

**Unquoted 2038 target, US$2.50 ex-factory per single-use mat at 100,000 units/year:** film and heat sealing $0.40; two pouches and graduation $0.60; closure/outlet $0.35; write-on tab and labels $0.25; packaging and quality checks $0.40; factory overhead/contingency $0.50. These are hypothetical allocations, not supplier quotes. Excludes trained staff, sterile-field supplies if indicated, any separate pads or scales, shipping, taxes, validation, regulated disposal, and maternity-service costs. Hospitals should compare the fully delivered per-birth cost, including waste treatment, with existing calibrated drapes and reusable trays.

## Impact

If validated, the device could make cumulative loss easier to carry between teams during a subset of the millions of annual births at risk of haemorrhage.[1] A pilot of 10,000 eligible births would create at most 10,000 instrumented handoffs, **not** 10,000 prevented complications. Measure missing-volume events, time to appropriate treatment, total blood-loss estimation error, spills, infection-control events, patient comfort, and clinical outcomes against current care. The E-MOTIVE trial's improvement cannot be attributed to a new drape or this device: its benefit came from a combined detection, treatment, and implementation package.[1][4]

## Failure modes and safeguards

- **Mixed fluid or incomplete capture:** place only at the appropriate clinical phase, label mixed readings invalid, and use independent assessment; never withhold treatment because the pouch reads below a threshold.
- **Clot obstruction, overfill, or transfer spill:** keep an emergency collection method ready, inspect flow continuously, seal and document each pouch before removal; if any volume is lost, flag the sum incomplete and escalate on symptoms and clinical judgement.
- **Misread graduation or wrong cumulative arithmetic:** high-contrast marks and a two-person verbal handoff in high-risk cases; train with deliberately contaminated and tilted simulations. The tab is a reminder, not an automatic calculator.
- **Infection and plastics:** single-patient use only; sealed contaminated pouches go to locally approved clinical-waste handling. No washing, open decanting, composting, or claimed recycling of contaminated contents. Study film minimization and a life-cycle comparison with reusable trays.[2]

## How It Works

After the baby is delivered, an attendant positions the disposable drape beneath the patient only if it does not interrupt established care. Gravity guides collected liquid through a polypropylene outlet into a hanging, graduated polyethylene pouch. The attendant reads the meniscus with the pouch held upright, notes the time and volume, closes the inlet, and retains the sealed pouch and written cumulative tab before opening the next pouch. At transfer, the receiving clinician reads back the recorded total and adds subsequent collected volume; the first pouch is never silently reset to zero. This is a manual accounting chain, not a blood-specific sensor: urine, irrigation, residual amniotic fluid, clots, and blood outside the drape defeat a simple volume reading. If the chain breaks, mark the total incomplete and assess clinically rather than inferring safety from a low reading. Escalation follows local obstetric protocols, regardless of the indicated volume.[1]

## Technical Architecture

The fluid path is a heat-sealed low-density polyethylene drape → molded polypropylene outlet and captive closure → two serial transparent, graduated pouches. A water-resistant write-on tab carries pouch reading, time, prior total, and invalid-reading flag between beds or facilities; it need not carry a patient name. The dry exterior of the sealed pouch can accompany the handoff subject to local infection-control policy. No software, battery, wireless link, or automated alarm exists. Qualification must test seam integrity, outlet occlusion, tilt sensitivity, legibility after handling, shelf storage, skin-contact compatibility, and local clinical-waste disposal. If a seal leaks or graduations cannot be read, use an approved alternate collection/measurement method and clinical examination. A new mat inherits only a clearly documented prior total; a missing tab is a measurement failure, not a zero.

## Performance Benchmarks

These are **unverified design targets**, not measured device performance or clinical efficacy. The appropriate comparator is a calibrated drape **with a written handoff**, since calibrated drapes already have trial evidence when paired with a treatment bundle.[1][2]

| Measure and test condition | Existing approach | Mat target (unvalidated) |
| --- | --- | --- |
| Volume reading, 100–1,500 mL on level bed | Calibrated drape: measure against the same gravimetric reference; no universal accuracy figure claimed | Within ±10% or ±50 mL, whichever is larger; test water and blood analogues across tilt angles |
| Two-pouch cumulative total, simulated transfer | Ordinary drape plus written handoff: measure in randomized usability comparison | ≥95% of trained users within ±50 mL, with no emergency-response delay |
| Drain flow at 0.3 m head, benchtop water | Comparator measured in identical fixture | ≥0.5 L/min without upstream pooling; repeat with clot analogues before clinical use |
| Ex-factory unit cost at 100,000/year | Site-specific procurement price of drapes or reusable trays must be obtained | US$2.50 hypothetical target, excluding delivery, labor and disposal |

## Deployment Scenarios

- **Midwife-led clinic:** On a crowded ward, a sealed first pouch and its tab accompany the patient to observation. The next midwife reads back the carried total before recording new loss; symptoms trigger care even if the pouch remains nearly empty.
- **District-hospital transfer:** During movement from delivery room to another bed, staff document whether spilled or absorbed blood makes the total incomplete. The receiving team uses the flagged reading alongside vitals and established haemorrhage protocol, rather than treating it as a diagnostic threshold.
- **Referral transport:** Where transport and infection-control rules allow, a closed pouch and minimal handoff tab travel with the patient; if secure transport is impossible, staff copy the reading into the existing clinical record and dispose of the pouch locally. The device does not substitute for referral or treatment.

## Risks & Mitigations

- **False reassurance:** Concealed bleeding, absorbent pads, and bypass flow are invisible to the pouch. Use symptoms, examination, and local response protocols first; conspicuously label incomplete readings.
- **Mixed fluid and posture:** Mark contaminated or tilted readings unreliable; compare against gravimetry and test placement, tilt, clots, and spill cases before any clinical claim.
- **Handoff arithmetic and workload:** Read back each prior volume and final sum; test against the existing drape-plus-chart workflow, including low light and multiple languages. Reject the design if changeover slows treatment.
- **Infection, privacy, and waste:** Single-patient disposable path; follow local handling and disposal rules. Record only the minimum needed for handoff, obtain consent under local practice, and avoid digitizing identifiable readings.
- **Incumbent cost and regulation:** Existing calibrated drapes may be cheaper and already fit protocols.[1][2] Verify net workflow benefit and total delivered cost before procurement; determine applicable regulatory classification and obtain appropriate review before clinical use.

## Vision for 2050

A plausible 2050 scenario is a birth service where every transfer retains an explicit cumulative blood-loss record, whether carried by a tested pouch, chart, or better successor. Objective measurement is paired with trained teams, supplies, timely referral, and respectful patient care—not sold as a stand-alone mortality intervention. This mat earns a place only if independent trials show a safer or more reliable handoff than the ordinary calibrated drape and chart.[1]

## Sources

[1] https://www.who.int/news/item/09-05-2023-lifesaving-solution-dramatically-reduces-severe-bleeding-after-childbirth
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC11338661
[3] https://pmc.ncbi.nlm.nih.gov/articles/PMC8133090
[4] https://iris.who.int/server/api/core/bitstreams/956e444f-3ac2-40cd-8b17-521f05770732/content
