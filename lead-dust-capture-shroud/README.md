# Lead-Dust Capture Shroud

**Author: jayis1. Status: research concept; not a certified lead-exposure control or authorization to disturb paint.**

## Problem

A trained renovator removing deteriorated paint from a reasonably flat wall needs to keep chips and dust inside the contained work area, rather than assuming that a connected vacuum is actually capturing debris. CDC estimates that about **29 million US housing units** have lead-based paint hazards, including deteriorated paint and contaminated dust; about **2.6 million** are home to young children. Renovation can generate hazardous lead dust.[1] These figures describe the housing problem, not this device's addressable market or a predicted number of people protected.

## Solution

A **hand-operated, captive-blade scraper in a transparent polycarbonate shroud** attaches through a replaceable silicone perimeter skirt and sealed 38 mm hose coupling to a **purpose-designed, properly maintained HEPA renovation vacuum**. A replaceable stainless blade protrudes only when both measured extraction flow and shroud depression are within a qualified range. A spring retracts the blade on low flow, poor seal, sensor fault or battery loss. A visible red/green indicator tells the worker to stop and inspect; the instrument does **not** measure airborne lead or certify a surface as safe. The prototype is limited to reasonably flat, accessible painted surfaces; corners, ornate trim, loose substrate and overhead work are outside its initial operating envelope.

This is an **adjunct for qualified workers**, not a substitute for work-area containment, appropriate wet methods, protective equipment, cleaning, verification/clearance, or applicable lead-safe renovation and abatement requirements. EPA requires containment and specific cleanup and verification practices under its US RRP rule.[2] No resident should use this concept as a DIY paint-removal guide.

## Key Innovation

HEPA vacuum attachments and shrouded paint-removal tools already exist; EPA describes both and warns that a shop vacuum merely retrofitted with a HEPA filter need not be properly sealed.[3] The proposed, unproven integration is **two independent operating checks at the actual scraper**: a differential-pressure measurement across a calibrated extraction-path restriction to infer flow, and a separate shroud-to-room pressure check to catch an open edge. Neither measurement alone proves capture. A spring-return captive blade makes a failed check interrupt the scraping action rather than merely displaying a number. This addresses **paint removal during renovation**, not the existing [Sealed Window Friction Cassette](../sealed-window-friction-cassette/), which isolates an installed window's recurring rubbing interface, nor the [Silica Wetwork Recovery Bench](../silica-wetwork-recovery-bench/), which manages wet stone-work slurry.

## Target Cost

**Unvalidated 2038 ex-factory target: US$120 per shroud at 10,000 units/year:** polycarbonate housing US$25; silicone skirt US$12; stainless blade and captive holder US$10; hose coupling and calibrated restriction US$15; two pressure channels, controller, indicator and replaceable cells US$25; spring-return blade actuator US$18; assembly and calibration US$15. Excludes the **purpose-designed HEPA vacuum**, hose, batteries after purchase, skirt/blade replacements, qualified labor, containment, testing, PPE, disposal, taxes and distribution. Target service life: **500 operating hours** with inspection before every use and replaceable worn parts; neither cost nor lifetime is supplier-quoted or demonstrated.

## Impact

A **laboratory development target**, not an observed reduction, is **at least 95% lower airborne lead mass collected outside the shroud** than matched unshrouded *dry* manual scraping inside a controlled test enclosure. The dry comparator is a laboratory hazard baseline, **not** a recommended field method. The more important gate is **no worse airborne lead and surface deposition than an established compliant wet/HEPA method**, under matched paint-removal rates and proper containment. Measure personal breathing-zone exposure, perimeter deposition and release during cleaning/filter service; reduced shroud-edge readings alone are not enough. A pilot of **20 qualified crews over 12 months** would compare actual compliance, faults and exposures with existing methods. Lead exposure or health benefit cannot be inferred from units sold; any 10–20-year rollout depends on independent occupational-hygiene validation, cost and local approval.

**Failure and end of life:** Clogged filters, vacuum disconnection, an unseated skirt, uneven paint, damaged housing, false-green sensor readings and power loss can defeat capture. Stop work on any alarm, visible escaped debris or poor fit; do not bypass the blade guard. Only trained personnel within containment inspect, wet-clean and bag contaminated skirts, blades and vacuum consumables following the vacuum manufacturer's instructions and local waste rules. Keep sealed contamination out of household recycling; separate clean housing/electronics for recycling only after qualified decontamination. The device contains no connectivity, identity tracking or surveillance function.

See [SPECIFICATION.md](SPECIFICATION.md) for operating assumptions, fault tests and the falsification plan.

## How It Works

A qualified renovator first establishes the required work-area containment and selects a flat, sound painted surface that accepts continuous skirt contact. With the captive blade retracted, the operator checks the transparent polycarbonate shell and silicone skirt, connects the sealed 38 mm hose to an approved purpose-designed HEPA renovation vacuum, and performs the prescribed pre-shift flow/pressure checks. The vacuum draws displaced chips and dust from the scraper cavity through the cleanable extraction neck and hose into its sealed collection and filtration system; the shroud is a local capture interface, **not** the filter or the work-area containment.[2][3]

The blade can protrude only while a calibrated restriction indicates sufficient *flow* and a separate sensor indicates shroud depression. The specification's **≥60 L/min** neck flow and **≥10 Pa** depression are tentative development settings, not validated capture velocities or exposure limits. Flow can look adequate across a lifted edge; pressure can look adequate behind a pinched hose. Both must be tested together against actual leakage. A failed check, disconnected vacuum, depleted battery or sensor fault calls for spring retraction and a red stop-work indicator. If the guard fails to retract, or any debris escapes, stop the task and use an approved alternative; never bypass it. Withdraw the blade with extraction running, then trained personnel wet-clean and seal contaminated replaceables within containment. The vacuum's sealed bag/filter service and waste disposal follow its manufacturer's instructions and local rules.[2][3]

## Technical Architecture

**Proposed, not demonstrated:** (1) clear polycarbonate housing and replaceable silicone contact skirt; (2) manual stainless captive blade and spring-return actuator; (3) cleanable 38 mm extraction neck with calibrated flow restriction and two pressure taps; (4) separate shroud-to-room pressure channel; (5) battery/controller with self-test and red/green indication; (6) approved sealed HEPA vacuum, hose and collection consumables. Controller logic permits blade extension only when both independent pressure channels, cell voltage and self-test remain in their *qualified* bands. No connectivity or worker tracking is required.

Material accounting must include paint removed, debris retained in the shroud or vacuum, dust deposited on surrounding surfaces, airborne lead escaping the work zone, and waste released during service. A HEPA filter's media rating cannot substitute for whole-system capture or personal sampling. Record hose length, filter loading, seal condition, airflow, pressure and fault transitions alongside every trial. Only independent testing can establish whether this architecture improves on a competent wet/manual or wet-plus-HEPA method.

## Performance Benchmarks

| Metric | Current reference or comparator | Unvalidated development gate | Measured result |
| --- | --- | --- | --- |
| Airborne lead outside shroud | Matched unshrouded **dry** hand scraping in a controlled laboratory only; not a field method | ≥95% lower mass per matched paint-removal task and per gram removed, as specified | Not yet measured |
| Exposure against existing practice | Professionally specified wet/manual or wet-plus-HEPA scraping | No practically material worsening of personal breathing-zone lead, post-cleaning wipes or service exposure; margin/power agreed with hygienist before testing | Not yet measured |
| Extraction | Calibrated neck flow and shroud-to-room differential under approved hose/vacuum combinations | Initial ≥60 L/min and ≥10 Pa, to be revised or rejected if lifted-edge trials escape detection | Not yet measured |
| Fault response | ≥100 randomized induced-fault trials in the specification | 100/100 retractions for gross disconnect/power loss; ≥99% detection overall without false green, with each fault class reported | Not yet measured |
| US occupational context | OSHA construction lead action level **30 µg/m³** and permissible exposure limit **50 µg/m³**, each as an 8-hour TWA[4] | Full-shift exposure assessment as required; a ten-minute test cannot establish compliance | Not yet measured |

The independent laboratory protocol in [SPECIFICATION.md](SPECIFICATION.md) uses characterized lead-paint panels, matched removal mass, filter-based lead analysis and perimeter wipes. It must record loaded-filter and disturbed-seal conditions as well as filter/skirt changes. These are proposed acceptance tests, **not** a claim that the shroud meets occupational limits or is superior to existing controls.

## Deployment Scenarios

1. **Contained flat-wall renovation:** A trained US renovation crew uses the attachment only where the skirt seats, while retaining required isolation, PPE, cleanup and verification. The operator sees a red stop signal on extraction failure; an industrial hygienist, not the indicator, assesses exposure.[2][4]
2. **Occupied-building maintenance with occupant exclusion:** A qualified contractor schedules a limited flat-panel repair inside a properly isolated work zone, selects wet/HEPA practice as the comparison, and documents air/wipe results before considering this tool for repeat work. Residents do not use the prototype.[2]
3. **Training and controlled validation:** A laboratory or approved training facility compares scraper ergonomics, fault detection and collection against compliant work practices; hazardous lead challenge tests occur only under professional containment, not at a worksite demonstration.

## Risks & Mitigations

A lifted skirt, warped substrate, cracked cover, hose kink, loaded filter or pressure-tap contamination can produce false confidence. Test both channels across each fault, require a failed state on sensor fault, inspect the fit before work and reject uneven surfaces; even a green indication is **not** a lead measurement. A power or actuator fault must leave the blade retracted, but wear, tampering and restart behavior still need human-factors tests. An obstructed view or tiring grip could prompt bypass: evaluate transparent housing, balance and real crew behavior before scaling. Opening the vacuum or removing the skirt can re-aerosolize lead; trained staff wet-clean, seal parts and follow manufacturer and local waste rules inside containment. The shroud does not address ingestion from contaminated hands, unrelated sources of lead, or fumes from heating lead; powered abrasion and smelting are outside scope. Required assessment, protective equipment and clearance remain independent obligations.[2][4]

## Vision for 2050

If independent comparisons show an exposure benefit over established wet/HEPA practice, imagine source-capture tools that refuse operation when extraction fails and are serviced through accountable consumable take-back. Contractors would log tested capture performance alongside routine work-area containment and clearance—not sell a green light as a guarantee. If the benefit disappears under realistic maintenance or the waste chain fails, this particular design should not spread. See [ROADMAP.md](ROADMAP.md) and [IMPACT_ANALYSIS.md](IMPACT_ANALYSIS.md) for the evidence gates and conditional economics.

## Sources

[1] https://www.cdc.gov/lead-prevention/prevention/paint.html
[2] https://www.epa.gov/lead/renovation-repair-and-painting-program-work-practices
[3] https://www.epa.gov/lead/frequent-questions-about-work-practice-standards-under-rrp-rule
[4] https://www.osha.gov/laws-regs/regulations/standardnumber/1926/1926.62
