# Battery Depowering Cabinet

**Author: jayis1** · **117** · Concept, not a certified battery-handling product

A supervised, repairable collection-site cabinet that discharges only positively identified, externally intact, low-voltage rechargeable lithium-ion packs before transfer to a qualified recycler. It is not a household appliance and does not make a discharged battery nonhazardous.

## Problem

The Global E-waste Monitor recorded 62 million tonnes of e-waste in 2022, of which 22.3% was documented as formally collected and recycled; that figure describes all e-waste, **not** the battery-specific collection rate.[2] Discarded batteries in mixed waste can short or ignite and expose collection workers and communities to fire. EPA advises terminal isolation, separate collection, trained handling, and dedicated treatment for damaged batteries; even discharged lithium batteries can remain hazardous because of their electrolyte.[1]

Small collection points need a practical boundary between public drop-off and the licensed battery-recycling chain. The [Circular PCB Electrorefinery](../circular-pcb-electrorefinery/) processes circuit boards and diverts batteries to separate handling; this invention does **not** process PCBs, shred cells, recover metals, open packs, or claim that a battery is safe after discharge.

## Solution

At a staffed municipal collection point, a trained operator screens each loose pack for its printed chemistry, voltage, terminal geometry, casing condition and recall status. Unsupported, unlabelled, swollen, hot, leaking, punctured, corroded, recalled, or otherwise suspect packs **never enter the energized slot**; they follow a separate locally approved damaged/defective/recalled (DDR) response pathway. No member of the public connects a pack.

For accepted packs, one pack at a time is secured in a nonconductive removable carrier in an independently monitored, fire-separated bay. A current-limited, fused DC load transfers the remaining energy to an enclosed resistive heater and external heat sink, rather than claiming useful energy recovery. Independently measured voltage and two temperature channels gate start, current, and stop. A normally open contactor de-energizes the circuit on power loss, disagreement, excessive temperature or time, or loss of ventilation; failed or uncertain runs are flagged for specialist assessment, not released as safe. A trained operator then insulates the terminals and transfers the pack to a compliant recycler's accepted container and documentation chain.[1]

**Pilot envelope, not a universal specification:** only manufacturer-labelled rechargeable packs with externally accessible terminals, nominal **3.6–14.8 V**, rated at **≤50 Wh**, and matching an approved, keyed carrier. No cells inside sealed devices, unknown chemistry, primary lithium, large power-tool/EV/energy-storage packs, damaged packs, or improvised contact leads. The exact envelope and cutoff must be validated with the recycler, fire authority and local regulator before use.

## Key Innovation

A **fail-closed intake-to-handoff sequence** joins positive pack identification, single-pack electrical isolation, independently measured thermal/voltage stop gates, and documented downstream custody. Existing battery cyclers and resistive dischargers supply the underlying electrical physics; the research contribution to test is whether this constrained, operator-only workflow reduces mis-sorting and unsafe handling at modest collection sites compared with a properly run collection-and-isolation station **without** onsite discharge. If supervised discharge adds risk or no measurable benefit, the discharge stage should be omitted and the collection-only alternative preferred.

## Target Cost

**Unvalidated design targets, US dollars, at 1,000 cabinets/year by 2038:** US$1,200–1,800 ex-factory for a one-bay cabinet, including carrier, fused load, redundant sensing, contactor, and serviceable controls; US$2,000–3,500 installed, excluding site fire protection and permitting. A modelling allowance of US$250–500/year covers inspection, calibration, carrier replacement and filter/service parts; staffing, compliant packaging, transport, recycler fees, electricity and insurance are extra. A US$1,500 unit plus US$350/year service over five years implies US$650/year before those exclusions (no financing or salvage). A procurement bill of materials and local fire-engineering estimate are required to validate affordability.

## Impact

A pilot goal is **10 supervised sites × 100 eligible packs/site/month for 12 months = 12,000 pack encounters**, conditional on actual supply and approved operating hours; rejected packs are counted separately. The primary outcomes are eligible-pack sorting accuracy, fire/near-miss rate, fault detection, transport acceptance, labor per pack and total cost relative to a qualified collection-only control. **No fires prevented, tonnes recovered, lives saved, or global reach are claimed.** A viable result could extend safe, accessible collection in underserved districts, but scaled environmental benefit depends on verified handoff to licensed recyclers, not merely owning cabinets.

## Safety and validation boundary

- No salt-water discharge, pack opening, crushing, unattended operation, improvised repairs or general-public access to energized parts. The cabinet cannot certify residual hazard away; even apparently discharged packs retain chemical and thermal risk.[1]
- Site-specific fire risk assessment, ventilation, suppression/detection, operator training, emergency evacuation plan, local hazardous-waste and shipping compliance, and a recycler contract are prerequisites, not optional extras.[1]
- Prototype fault-injection must test reversed polarity, wrong chemistry/voltage, open or shorted sensor, blocked ventilation, contactor weld, mains loss, runaway heating simulation, and mislabeled packs. An independent third party must compare it with collection-only practice before field operation.
- The enclosure, carriers and replaceable parts should be repairable; failed electronics enter e-waste recycling. Spent packs never become general waste.

## Sources

[1] https://www.epa.gov/hw/lithium-ion-battery-recycling-frequently-asked-questions
[2] https://ewastemonitor.info/the-global-e-waste-monitor-2024
