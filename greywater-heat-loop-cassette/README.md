# Greywater Heat-Loop Cassette

**Author: jayis1. Status: research concept; not a certified plumbing product.**

## Problem

Hot shower water is commonly discarded while new cold water must be heated. Water heating is a material household energy expense: the IEA reports that space and water heating together account for roughly 70% of home energy in advanced economies, but that combined statistic is **not** a drain-heat-recovery opportunity estimate.[1] Millions of residents of multi-unit buildings cannot easily retrofit the long, uninterrupted vertical drain required by many conventional drain-water heat recovery (DWHR) coils. Hair, soap and scale also make an inaccessible drain-side heat-transfer surface difficult to maintain. The intended user is a building owner or cooperative with a qualified plumber and an accessible shower-drain service bay, not a tenant asked to modify potable plumbing.

## Solution

Install a compact, **gravity-drained shower-greywater exchanger** in a reachable service bay. Shower water flows over a lift-out, smooth 316L stainless drain-side cassette and then to the normal drain. Incoming potable cold water flows through a **stationary, pressure-rated copper/stainless heat-exchanger assembly** on the other side of a separately certified double-wall barrier with an open, visible leak-indication channel. It is routed **only to the water heater inlet** unless local code and independent hygiene review permit another arrangement. The cassette geometry spreads greywater into a thin film; a plumber can isolate and remove only the drain-side wetted insert for brushing without opening the potable circuit. A full-bore gravity bypass accepts drain water if the cassette clogs; its fail-open configuration must be demonstrated under hair and soap loading. No pump, electrical supply, radio or occupant tracking is required.

A maintenance worker checks the visible leak outlet and bypass path, opens the drain-side access hatch, lifts the insert, brushes it, rinses to an approved drain and reseats it. A leak or damaged barrier means **take the potable-side exchanger out of service and have a plumber replace it**; never plug the telltale or attempt to clean the potable circuit through the drain hatch. This is heat recovery, not water reuse or disinfection.

## Key Innovation

Vertical falling-film copper coils, shower-tray exchangers and double-wall separation are existing technology.[2][3] The proposed advance is a **potable-side-sealed, drain-side-only replaceable heat-transfer interface with a visible inter-wall leak path and a gravity bypass** in a compact service bay. That combination is an engineering hypothesis, not a claim of patent novelty or superior efficiency. It should be compared head-to-head with a code-approved conventional vertical DWHR coil and a cleanable shower-tray exchanger under the same inlet temperatures and flows. A service interface that sacrifices too much heat transfer, accumulates biofilm or cannot be approved locally fails the concept.

**Unverified design targets:** at 9 L/min simultaneous shower and cold-water flow, 35°C drain inlet, 15°C potable inlet and 20°C ambient, cool the drain by **at least 3°C** during a steady five-minute interval after startup; keep added shower-drain head below **20 mm water column** at that flow; clear a deliberately hair-loaded drain via the bypass without floor overflow; and complete drain-side cassette removal, cleaning and reseating in **under 10 minutes** without potable-side disconnection. Cold-water pressure loss, potable-side stagnation and leak-channel visibility must meet the applicable plumbing approval, not an invented universal threshold. The 3°C target is conditional on enough simultaneous warm drain flow and a sufficiently cold inlet; batch laundry discharge alone cannot preheat a later shower without storage.

## Target Cost

**Unvalidated 2038 ex-factory goal at 10,000 units/year: US$180/unit**: drain-side insert and hatch $38; certified double-wall exchanger and telltale $88; bypass and seals $24; housing, assembly and pressure/leak testing $30. These are planning allowances, not supplier quotes. Qualified installation, drain rerouting, permits, access panel and commissioning could add **US$150–500 per eligible site**; cleaning labor, replacement seals, end-of-life handling and any retrofit of a cramped building are additional. Where a service bay cannot fit or the required alteration is costly, conventional DWHR or no retrofit may be better. No proprietary subscription or consumable is intended.

## Impact

A bounded energy example: 9 L/min over five minutes is 45 L. If the validated unit cools that drain flow by 4°C, the recovered heat would be approximately **0.209 kWh** (`45 kg × 4.18 kJ/kg/K × 4 K ÷ 3600`), before any distribution or heater losses. The **3°C minimum target** corresponds to less heat; neither figure is an observed saving or a whole-home percentage. Annual value depends on shower frequency, source-water temperature, overlap between drain and cold supply, heater efficiency and fuel price. At 10,000 eligible units, the opportunity is many small reductions in water-heating demand; no emissions or bill-saving total is claimed before metered field trials. Low-flow showers, lukewarm drains, irregular occupancy and non-overlapping laundry use reduce or eliminate the gain.[2]

Test 30 matched installations over a year against approved standard DWHR and no-exchanger baselines, recording inlet/outlet temperatures, flow, heater input, cleaning hours, blockages, leak indications and occupant complaints **without retaining household schedules or identities**. Stop deployment if a cross-connection occurs, a blocked drain floods, or measured net savings do not offset maintenance and installed cost. Inspect for biofilm, corrosion and cleaning-chemical compatibility; use locally approved potable materials, backflow protection, pressure testing and third-party plumbing-code certification before connection. Do not bypass safe water-heater temperature settings to chase efficiency: preheated-water hygiene and Legionella risks depend on plumbing configuration.[2] Recover metals and replace damaged seals at end of life. Prototype and approval work is plausible within 10–20 years, but broad adoption is contingent on independent safety and field-cost evidence.

## How It Works

During a shower, warm drain flow and cold heater feed overlap. Gravity spreads the drain stream across the removable 316L insert; heat crosses the stationary, pressure-rated double-wall exchanger into the cold feed, which then enters the water heater. The open inter-wall channel drains a barrier leak to a visible telltale rather than into either water stream. A hair screen and full-bore gravity bypass protect the drain when the insert fouls; the original trap and water seal remain in place. The cassette stores neither wastewater nor warmed potable water. For a delayed bath discharge, overlap approaches zero and so does recovery. Heat exchange does **not** disinfect or recycle greywater.

## Technical Architecture

- **Wet path:** shower trap → upstream strainer → accessible film cassette (or fail-open bypass) → sewer. Verify head loss and overflow clearance with hair/soap loading.
- **Potable path:** cold supply → stationary, independently approved double-wall heat-transfer assembly → water-heater inlet. A plumber pressure-tests this sealed circuit; drain-side cleaning never opens it.
- **Safety and observability:** vented telltale between walls, accessible hatch and bypass inspection point; no sensors, pump or wireless telemetry are necessary. A visible leak or failed barrier requires isolating the exchanger and professional repair, not sealing the telltale.
- **Energy boundary:** for water density near 1 kg/L, recovered thermal energy is approximately `flow × time × 4.18 kJ/kg/K × drain cooling ÷ 3600`; actual heater-input savings also depend on overlap, heat loss and heater efficiency.

## Performance Benchmarks

| Metric at 9 L/min, drain 35°C, inlet 15°C | No recovery | Established vertical DWHR reference | Cassette concept target |
| --- | --- | --- | --- |
| Drain cooling over steady five minutes | 0°C | Measure a code-approved unit in the same rig; no comparable value claimed here | ≥3°C; **unmeasured** |
| Thermal recovery over that interval | 0 kWh | To be measured on the same flows | ≥0.157 kWh from 45 kg × 4.18 × 3 / 3600; **calculated target** |
| Added drain head; drain-side service | 0 mm; ordinary trap cleaning | Measure installed reference | <20 mm; cassette clean/reseat <10 min; **unmeasured** |
| Cross-leak and cold-side pressure loss | Not applicable | Approval/test report for selected reference | Visible, vented leak path; loss subject to local approval; **unmeasured** |

Vertical falling-film DWHR is the relevant commercial state of the art, not an invented prototype baseline.[2][3] The 3°C target represents 15% of the stated 20°C inlet temperature difference **only under equal 9 L/min streams**; it is not a certified effectiveness rating or a promise of annual savings. Run equal-flow calorimetry, pressure/leak tests and repeated fouling/cleaning cycles before comparing products. Current cassette state: paper concept, **zero validated bench results**.

## Deployment Scenarios

1. **Service-bay apartment retrofit:** a building owner with accessible shower drainage and a permitted potable-water connection can preheat the heater feed without a long vertical drain run; cramped slabs or inaccessible traps are disqualifiers.
2. **Dormitory or hostel bathing block:** recurring showers give the exchanger more operating hours, but a caretaker must clear hair screens and record bypass events; meter energy and cleaning labor against a no-exchanger control.
3. **Off-grid clinic shower:** lowering water-heater demand could reduce backup energy, provided the drain remains safe on power loss and a licensed plumber can inspect the leak path; never substitute this device for sanitation treatment.

## Risks & Mitigations

| Failure mode | Mitigation and validation gate |
| --- | --- |
| Hair, soap and biofilm clog the film path or cause odors | Strainer, removable smooth insert and full-bore bypass; test with loaded hair/soap and reject any floor overflow or trap-seal loss. |
| Pressure-side breach contaminates drinking water | Approved double wall with open telltale, backflow controls and pressure/leak testing; isolate on indication and obtain local plumbing approval before use. |
| Warm preheat stagnates or users alter heater settings | Direct feed to the heater, no warm buffer tank; verify stagnation and Legionella control against local hygiene guidance without lowering heater safety settings.[2] |
| Low source temperature or noncoincident flows destroy the economics | Select sites with metered simultaneous showers; reject where measured net savings cannot cover cleaning and installed cost. |
| Corrosion, cleaning chemicals or seal failure shorten life | Test 316L, potable-rated alloys and elastomers against actual chemistry; replace failed parts and recover metals at end of life. |

## Vision for 2050

If independent safety testing, code approval and field metering support the concept, shower-drain service bays could be designed with an inspectable heat-recovery slot as routinely as a trap cleanout. Buildings would buy less water-heating energy while retaining ordinary safe drainage and potable-water protections. This is a conditional adoption scenario, not a forecast: where maintenance access, temperature lift or economics fail, a conventional exchanger or no recovery remains the right choice.

## Sources

[1] IEA, *Energy Efficiency 2025: Buildings*: https://www.iea.org/reports/energy-efficiency-2025/buildings — combined space- and water-heating context in advanced economies, not a claim about global shower savings.

[2] Manouchehri and Collins, *Investigating the Impact of Plumbing Configuration on Energy Savings for Falling-Film Drain Water Heat Recovery Systems*, Energies 15(3), 1141 (2022): https://www.mdpi.com/1996-1073/15/3/1141 — DWHR prior art, flow/configuration dependence and potable-water hygiene constraints.

[3] US National Renewable Energy Laboratory, *Standard Work Specifications: Drain Heat Recovery*: https://sws.nlr.gov/spec/703013 — installation, simultaneous flow and plumbing guidance; not certification for this device.
