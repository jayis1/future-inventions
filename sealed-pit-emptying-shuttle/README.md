# Sealed Pit-Emptying Shuttle

**Author: jayis1. Status: research concept; not a certified sanitation service or a substitute for trained workers and approved treatment.**

## Problem

In 2024, 3.4 billion people lacked safely managed sanitation; that figure is the scale of the wider sanitation gap, **not** the addressable market for this device.[1] In narrow settlements a vacuum truck may not reach a wet pit. Existing hand-operated Gulpers can move wet sludge from the surface, but a contaminated open discharge, blockage and transfer into transport containers remain exposure points.[2] Trash and fibrous material make mechanical pit emptying particularly difficult; studies of trash-excluding systems still report limits with thick sludge and fibers.[3] Workers today may have to handle contaminated material manually, which this concept is intended to avoid, not normalize.[3]

## Solution

A two-worker, wheeled **vacuum-transfer shuttle for accessible, relatively liquid pit contents**: a guarded, removable 50 mm suction hose leads to a 20 L rigid polypropylene collection vessel rated for vacuum. A 24 V, 100 W-rated diaphragm **air** pump evacuates the vessel through a hydrophobic aerosol barrier and an independent mechanical overfill float; the pump never intentionally passes sludge. An upstream coarse inlet guard reduces large-debris entry. A spring-closed inlet valve and two keyed, normally closed dry-break couplings seal the full vessel before it is disconnected; a separate closable receiving port transfers it at an authorized treatment depot. A mechanical vacuum gauge and a weighed fill check provide local, offline feedback. No identity, location, or operator telemetry is collected.

The worker inspects access, pit integrity, gas hazards and the downstream disposal route before starting; never enters a pit. The device is **not** for dry, consolidated or high-trash pits, chemical/industrial waste, or explosive atmospheres. If the inlet clogs, the vessel nears its marked fill limit, the gauge fails, the containment path leaks or the treatment outlet is unavailable, stop, close valves and refer the job to an appropriately equipped service. No high-pressure backflush into the pit, open-air decanting or hand-clearing of a contaminated blockage. PPE, hand hygiene, decontamination, transport licensing and treatment remain essential.

## Key Innovation

Vacuum carts, Gulpers, removable canisters, floats and dry-break fittings already exist. The proposed advance is a **small-access, vessel-swap workflow whose normally closed connections, independent overfill barrier and fill accounting make both transport and failed emptying visibly containable**. Unlike this repository's [Electrochemical Blackwater Refinery](../electrochemical-blackwater-refinery/), it does not treat toilet waste or generate fertilizer; it moves a constrained fraction of existing wet pit contents to a licensed treatment service. Whether it actually reduces splashes, exposure and cost versus maintained Gulper-plus-sealed-container or vacuum services is the central unproven claim. A 10–20-year path allows design validation and local repair, not new pump physics or a claim of patent novelty.

## Target Cost

**Unvalidated goal: US$600 ex-factory per shuttle at 10,000/year in 2038**, including one vessel. Planning allowances: wheeled frame and guard $110; vacuum-rated vessel and closures $100; pump, 24 V replaceable battery and charger $150; hose, inlet guard, valves and dry-breaks $120; gauge, overfill float and exhaust barrier $45; assembly/leak test $75. Additional swappable vessels: **US$60 each** as a target, not a quotation. A model using 100 service jobs/year and five years of hardware life gives US$120/year amortized hardware plus US$80/year assumed maintenance, or US$2/job before labor, transport, cleaning, PPE, power, waste fees and finance. If each job serves a different five-person household, this limited hardware-and-maintenance allocation is US$0.40/person-year; actual paid service must include the exclusions and may be much higher. Locally replaceable hoses, gaskets and standard-size valves are preferred; the fouled aerosol barrier and residues require controlled disposal.

## Impact

**Pilot targets only:** ≥10 L/min on a defined water-like simulant through a 1.5 m vertical lift, ≤16 L usable volume per 20 L vessel, no visible joint leaks in 100 wet coupling cycles, and lower measured worker contact and spill mass than a maintained Gulper-to-covered-container comparator over 100 eligible emptying jobs. Thirteen 16 L loads are needed for 200 L; that is a logistical ceiling scenario, not a promise that any pit can be completely emptied. At 10 L/min, the fluid transfer alone takes at least 20 minutes for 200 L, excluding swaps, access, cleaning and transport. For a nominal 40 kPa pressure difference and 10 L/min flow, the air-flow work scale is about 6.7 W; at 30% total efficiency, about 22 W before fouling, startup and friction. The 100 W pump rating is headroom, not demonstrated throughput; air leakage and sludge rheology can invalidate this simple estimate. See [SPECIFICATION.md](./SPECIFICATION.md) for gates.

A 100-job/year pilot could serve at most 500 distinct people under the five-person-household assumption; repeat jobs reduce that number. Count **delivered and accepted waste at the treatment facility**, not just volume extracted. Measure contamination on gloves and surfaces, spills by mass, injuries, failed jobs, energy and total service cost. No disease or emissions reduction is claimed without comparative field and downstream treatment evidence. The receiving depot, worker cooperative or municipality maintains the shuttle; without a legal treatment route, it must not operate.

## Sources

[1] https://unstats.un.org/sdgs/report/2025/Goal-06
[2] https://washresources.cawst.org/en/resources/e93b3358/pit-latrine-emptying-technology-review-the-gulper1
[3] https://doi.org/10.1039/d1ew00383f

## How It Works

The customer buys a **contained transfer to an authorized receiver**, not a pit treatment. Two trained workers first verify an accessible, structurally sound opening, relatively liquid domestic waste, a safe working atmosphere and an available receiving slot. They refuse consolidated bottoms, heavy trash, unknown chemicals, unstable slabs or unsafe gas readings; nobody enters the pit. With PPE and a spill kit in place, they check the gasketed 20 L vacuum-rated vessel, inlet closure, independent float, hydrophobic pump-inlet barrier and mechanical gauge. The guarded 50 mm hose is placed from the surface, not by hand-clearing an obstruction.

The 24 V diaphragm pump removes **air** from the vessel; the resulting pressure difference draws liquid up the hose, rather than pumping sludge through the motor. A relief valve is intended to limit vacuum to 40 kPa below ambient. The 1.5 m water lift alone uses approximately 15 kPa of pressure head; viscous losses and leaks consume the rest. Monitor the gauge and vessel mass, stop before the **16 L** usable mark, and close the spring-closed inlet. For a swap, isolate power, close both independently sealing dry-break ends, wipe the exterior under an approved protocol, and secure the vessel upright. Loss of power should leave the inlet closed, but that fail-safe behavior must be proven under wet, worn and obstructed conditions.

A 200 L eligible job entails at least **13 vessel fills**, not one convenient cartload. Provide enough approved vessels, repeated sealed depot runs or another licensed collection service; plan two-person handling because a filled vessel can exceed 16 kg plus its own mass. At the authorized depot, a trained receiver mates the separate closed discharge port, records non-personal vessel IDs and received mass, and sends the waste into approved treatment. Contain wash water and spent barriers as contaminated waste. There is no on-site open decant, no pit entry, no automatic disinfection and no claim that the exhaust barrier removes toxic gases.

## Technical Architecture

| Boundary / subsystem | Proposed function and observable check |
| --- | --- |
| Site and intake | Worker eligibility assessment; guarded replaceable 50 mm hose and coarse inlet guard reduce, but cannot eliminate, debris intake. Refuse rather than hand-clear a blocked inlet. |
| Vacuum and vessel | 24 V battery drives a 100 W-rated diaphragm air pump; relief valve, mechanical gauge and mechanically vacuum-rated 20 L polypropylene vessel constrain suction. Verify actual pressure-flow behavior and vessel rating. |
| Independent containment | Spring-closed inlet, paired normally closed keyed dry-breaks, 16 L fill mark, float shutoff and hydrophobic pump-inlet barrier protect different failure paths. Challenge each single fault separately; inspect and retire damaged seals/vessels. |
| Gas and electrical interface | Test the pump exhaust for aerosol escape and gas hazards; ventilation and an assessed atmosphere remain necessary. Do not run in explosive or oxygen-deficient conditions; battery isolation cannot substitute for a safe site. |
| Logistics and receipt | Upright secured vessels travel by approved route to a compatible sealed receiver. Local, offline ID/mass reconciliation compares collected and accepted material; no person or location telemetry is required. |

Physical flow is **pit → guarded hose → closed inlet → vessel → sealed transport → authorized receiver → treatment**. The air path is **vessel headspace → independent float → hydrophobic barrier → diaphragm pump → assessed exhaust**; the barrier is not a gas scrubber. Operational information flows from site checklist and fill mass to an offline handoff ledger and receipt. A leak, failed gauge, full vessel, clog, gas alarm or unavailable receiver means isolate, keep closures shut, secure the load and refer the job. Field protocols must test whether that stop state is achievable without spilling or exposing a worker.

## Performance Benchmarks

**No prototype or field performance has been measured.** The comparator is a *maintained* Gulper pumping into a covered vessel, plus an available vacuum service where access allows; neither an open bucket nor an unmaintained truck is a fair state-of-art baseline. Published Gulper limitations and trash-handling challenges are summarized in [2] and [3] above; neither source establishes comparable numerical throughput for this exact pit. The table separates specified targets and calculations from data that a paired trial must collect.

| Metric and test condition | Shuttle target / calculation (unvalidated) | Current-practice comparison and measurement |
| --- | --- | --- |
| Net extraction, water-like simulant, 1.5 m lift, 50 mm hose | ≥10 L/min at ≤100 W electrical; plot pressure/flow, fouling and Wh/L | Measure maintained Gulper and available vacuum equipment at the same lift and feed; wet sludge rate unknown. |
| 200 L eligible extraction, excluding setup and trips | ≥20 min net pumping and ≥13 fills of up to 16 L | Time complete jobs for all methods, including access, swaps, cleaning and receiver handoff; no claimed speed advantage. |
| Wet couplings and overfill, 100 connect/disconnect cycles | No visible external leaks; single-fault float/barrier tests must prevent liquid reaching pump/exhaust | Weigh spill mass and swab contact surfaces against covered-container transfers; visible cleanliness alone does not prove pathogen containment. |
| Worker exposure and treatment delivery, 100 eligible paired jobs | Lower measured contact/spill mass **and** documented accepted receiver mass; target, not outcome | Record PPE contamination, gas readings, refused jobs, receipt rate, injuries and full-chain cost for each comparator. |
| Eligible pit type / site access | Relatively liquid domestic sludge, accessible opening, safe atmosphere and viable depot logistics | Document geometry, debris loading, rheology, lift, hose length, operator count and full duty cycle; report refusals, not only successful jobs. |

The nominal 40 kPa × 10 L/min calculation in the original Impact section is a rough liquid-flow work scale, **not** a measured diaphragm-air-pump draw or a valid air-pump sizing curve. At a full 100 W electrical draw, 20 minutes of net pumping would use about **33 Wh per 200 L job**, excluding idle, transport, charging loss and cleaning. Actual wet-sludge throughput and service economics require instrumented trials. The comparators' rates, prices and safety outcomes remain **not established for matched conditions** rather than fabricated as a universal baseline.

## Deployment Scenarios

1. **Narrow-access settlement:** a licensed worker cooperative rents vessels and shuttle, with households or a utility paying per completed service. Assess pit stability, wetness and gas before accepting; arrange repeated sealed trips through lanes a vacuum tanker cannot enter. A municipal transfer station must book capacity, weigh receipts and handle wash water; otherwise do not offer the service. Compare total price and worker exposure with a maintained Gulper/covered-container team.
2. **Peri-urban scheduled route:** a utility equips a two-worker crew for inspected, accessible school or household pits and provides a secure intermediate staging point only if locally permitted. Plan for at least 13 fills for a 200 L request, avoid lifting a full vessel alone, and return each batch to an authorized treatment site. The utility pays for maintenance, PPE and disposal and records refused thick pits for a larger service—not as failed workers.
3. **Flood-affected site:** an emergency sanitation operator deploys only after an assessment shows sound access and nonhazardous atmosphere; inundation can make slabs unstable and waste routes impassable. Reserve receiving and decontamination capacity before mobilization. If the site cannot keep vessels upright and transport them legally, defer to an equipped emergency service rather than creating stockpiled, contaminated containers.

## Risks & Mitigations

| Failure / consequence | Prevention, detection and safe response | Residual validation question |
| --- | --- | --- |
| H₂S, methane, low oxygen or unstable pit | Trained pre-entry-free site assessment, appropriate gas testing, ventilation assessment and stop-work rule; never enter or run electrical equipment in an unsafe atmosphere. | Barrier does not scrub gas; test exhaust and actual operator exposure under local safety rules. |
| Blockage from bags, grit, fibers or hardpan | Guard intake; screen eligibility; on abnormal gauge reading close inlet and refer to equipped service. No hand-clearing, high-pressure backflush or unauthorized pit disturbance. | Determine refusal rate and whether safe off-site cleaning is practical. |
| Seal leak, hose disconnection, overfill or rupture | Pre-use inspection; rated vessel, relief valve, normally closed couplings, separate float/barrier, fill weighing and upright restraint; stop, isolate and follow spill-response protocol. | Challenge wet, abraded seals and single-fault combinations; retire damaged vessels. |
| Power loss or contaminated maintenance | Spring-closed inlet and mechanical gauge; isolate power, close each connection and take fouled components to a controlled wash area with PPE. | Prove fail-closed operation and wash-water treatment; locally available spares are not guaranteed. |
| Untreated dumping or unaffordable service | Pre-book licensed receiving, reconcile vessel mass/IDs and audit exceptions; pilot rental/utility subsidy and measure full cost per empty. | The device cannot create treatment capacity, legal recognition for informal workers or household willingness to pay. |

A failed containment test, unsafe clearing method or worse measured exposure than maintained alternatives is a **stop/redesign gate**, not a marketing caveat. Compliance with local worker-safety, transport and sanitation requirements must be established before deployment; this concept has no certification.

## Vision for 2050

If repeated independent trials show a safer and affordable full chain, small-access emptiers could operate like recognized utility contractors: an inspected pit gets a contained pickup, each vessel has a reconciled receiving receipt, and the customer can see that waste reached treatment rather than a drain. Local workshops would replace standard hoses and seals; municipalities would fund receiving capacity and worker protections alongside collection. By 2050, the successful outcome would be fewer unsafe transfers and more **verified treatment**, not more gadgets or an invented count of diseases averted. Where dense sludge, unstable pits or poor economics defeat the shuttle, other sanitation services should remain the answer.
