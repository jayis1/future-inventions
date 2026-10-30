# Solar-Swing Humidity Vent

**Author: jayis1**

**Category:** Healthy Housing & Universal Basic Services / Indoor Moisture Control

**Status:** Concept (TRL 2; not a qualified building or health product)

## Problem

Persistent dampness and mould in buildings are associated with respiratory symptoms, infections and asthma exacerbation. WHO's review estimates dampness in 10–50% of indoor environments across several studied regions, but that is not a global count and does not imply that every such building is suitable for this device.[1] Leakage, rising damp and cold thermal bridges require building repairs; a room dehumidifier alone cannot fix them. Humid-climate households with intermittent power may also be unable to run compressor dehumidifiers continuously.

## Solution

A window-mounted, serviceable ventilation module uses two alternating **silica-gel-coated aluminum honeycomb** beds, a small 12 V DC fan, a four-way damper, a glazed solar-air heater and an exterior exhaust. In adsorption mode, outdoor make-up air passes through one dry bed into the room; a separate air stream heated by sunlight passes through the other bed and vents its released water vapour **outside**. Dampers reverse the roles only after the hot bed cools. A 30 W photovoltaic panel and small replaceable battery drive the fan and damper; backup grid power is optional. Filtration and insect screens protect the air path. No data leaves the device.

The initial target is to remove **0.20 kg of water per sunny day** from the incoming air stream, conditional on sufficient humidity gradient, airflow and solar input. A paired temperature/RH sensor checks inlet and outlet *absolute humidity* rather than mistaking warm air for dry air. A separate low-cost room hygrometer helps occupants see whether the building is actually drying. The module is not for flooded rooms, structural damp, or rooms whose required ventilation rate exceeds its capacity.

## Key Innovation

Desiccant dehumidification and solar regeneration are established, not invented here. The proposed advance is a repairable, low-power **two-bed, physically separated fresh-air/regeneration-air path** in a small-window retrofit, with a measured net-moisture-removal gate: a saturated bed must not be advertised as drying the room. Unlike this repository's radiative-adsorption refrigerator (cooling a cabinet) or stabilized-earth floor kit (repairing a dry floor), this addresses humidity transported by ventilation air and exhausts the captured vapour outdoors. The comparison against existing solar-desiccant ventilators and ordinary source repair must be tested; novelty and superiority are not established.

## Target Cost

**Unvalidated 2038 ex-factory target, USD, 100,000 units/year:** US$95: US$22 coated aluminum beds and silica gel, US$14 duct/damper/seals, US$12 fan/filter/screen, US$18 solar-air collector, US$17 PV/battery/controller/sensors, US$12 assembly and test. Installation and weatherproofing are estimated separately at US$35–80 per suitable window, varying by region; taxes, distribution, replacement filter and end-of-life collection are excluded. Target filter/screen cleaning monthly, bed inspection annually, and battery replacement after its measured cycle life; preliminary service allowance US$8–15/year excludes labor and replacement battery. These are planning budgets, not quotes or a delivered-price promise.

## Impact

A **100-room paired pilot** would compare the retrofit against repaired-and-ventilated control rooms over a full wet season: logged indoor absolute humidity, hours above a locally chosen RH threshold, surface temperature, visible damp, fan energy, and occupant-reported nuisance. If 10,000 eligible rooms each reach the conditional 0.20 kg/day target for 120 sunny days, the capacity scenario is **240 tonnes of water vented outdoors per season**, not 240 tonnes of prevented mould or a measured health gain. Health outcomes, cost effectiveness and suitable-room prevalence remain unproven; source repair and adequate ventilation take priority. A 10–20-year route is laboratory moisture/energy balance, weather-exposed building-safety testing, matched field trials, then local repair training. Wider adoption by 2050 is a vision conditional on those tests, not a forecast.

## Operating envelope and rejection gates

- **Mass/energy budget (design hypothesis):** two beds with a combined 1.0 kg dry silica gel must achieve a *measured* working swing of 0.10 kg water/kg gel per usable cycle, twice per sunny day, to reach 0.20 kg/day. This is not guaranteed at all temperatures and humidities. Vaporizing/desorbing that water requires at least roughly 0.49 MJ/day at ~2.45 MJ/kg latent heat, before heating the beds, duct and exhaust air or accounting for losses. A proposed 1 m² collector must supply **at least 1.5 MJ/day useful heat** under the test condition; otherwise lower the throughput claim. Electrical target: ≤6 W average over 8 operating hours, or ≤48 Wh/day from PV/battery, to be verified at measured airflow.
- **Ventilation and failure:** target 20 m³/hour supply airflow when operating, checked by a measured commissioning flow test; this is not a whole-home ventilation guarantee. On sensor disagreement, full bed saturation, insufficient collector temperature, blocked filters, smoke ingress or failed fan, a mechanical indicator shows **not drying** and the regeneration path remains separated from the room. Never close a required code-compliant vent to install it. Maintain a manual fresh-air bypass where code permits; an indoor-air specialist must assess ventilation and combustion appliances.
- **Safety and environment:** hot regeneration surfaces and condensate/soiling need guarded access, drainable construction and electrical protection; exterior exhaust must not re-enter windows. Test for silica dust, microbial contamination, UV/weather aging, fire safety and safe fan-off behavior. Silica gel and aluminum should be recoverable; PV, battery and electronics require local e-waste handling. Reject installation where leaks, capillary rise, floodwater or condensation on cold surfaces dominate; fix these first. No diagnosis, mould-remediation or respiratory-health benefit is claimed.
- **Acceptance test:** provisional reference condition: inlet 30 °C and 75% RH, 20 m³/hour during eight hours of flow, and at least four hours of 600 W/m² sunlight on the 1 m² collector. In a controlled humid chamber, measure inlet/outlet humidity and dry-bulb temperature, flow, collector irradiance, electrical input, exhaust humidity and bed mass across repeated adsorption/regeneration cycles. Reject the design if whole-day *net* removal is below 0.20 kg at that condition or if regeneration exhaust leaks into the supply. Compare room moisture against an equal-flow conventional vent: removing moisture from incoming air is not necessarily the same as drying the room if leaks or occupants add more water. Publish measured performance at other conditions rather than a universal rating; follow with paired, independently reviewed building trials before sale.

## Sources

[1] https://www.ncbi.nlm.nih.gov/books/NBK143942 — WHO Guidelines for Indoor Air Quality: Dampness and Mould, evaluation of human health risks (2009).
[2] https://www.energystar.gov/products/dehumidifiers/key_efficiency_criteria — ENERGY STAR Dehumidifiers Key Efficiency Criteria, Version 6.0 (effective October 1, 2025).

## How It Works

1. A screened inlet and 12 V fan draw outdoor air through one cool, dry silica-gel-coated aluminum honeycomb bed. Water adsorbs onto the gel; the delivered air is warmer from adsorption heat, **not cooled**. At the provisional 20 m³/h for eight hours, removing 0.20 kg requires an average inlet-to-supply reduction of 1.25 g/m³ across 160 m³, assuming the supply flow is maintained.
2. In a sealed, separate duct, the 1 m² glazed collector warms regeneration air through the *other* bed. The released vapor leaves through an exterior exhaust positioned to prevent re-entrainment. A damper seals supply from regeneration; the controller switches beds only after the regenerated bed has cooled, avoiding a hot, humid supply pulse. Compare humidity ratio calculated from paired temperature/RH probes on both sides of the supply bed; RH alone is misleading when temperatures differ.
3. Log flow, inlet/supply humidity, bed temperatures and solar input. Count captured water by integrating airflow × (inlet − supply absolute humidity), then check against bed-mass change and regeneration exhaust. If sunlight, sorbent capacity or sensor agreement is inadequate, show **not drying**; preserve independently required ventilation via an approved bypass, not a claimed dehumidification mode. Without a dry regenerated bed the unit cannot continue removing moisture, including through a long humid night.

## Technical Architecture

The serviceable cassette separates four subsystems: (i) screened supply channel, fan and replaceable desiccant beds; (ii) glazed solar-air heater and isolated outdoor regeneration exhaust; (iii) sealed four-way damper with cool-down interlock; (iv) local 30 W PV, battery, temperature/RH/flow sensing and a plainly readable fault indicator. The 30 W nameplate is **not** a promise of eight hours at rated output. A 48 Wh/day electrical budget needs storage or grid backup when PV production falls short. Weather seals, drip edges and inspection hatches must keep rain, insects, dust and loose silica out of occupied air.

This is not the repo's passive draft-balancing kiln retrofit or a generic window opening: its testable distinction is the **measured water transfer between two isolated air paths**. A room moisture balance must also account for infiltration, occupants, leaks and surface condensation; drying *incoming air* alone cannot prove that indoor air or walls dry. No cloud connectivity or remote telemetry is required.

## Performance Benchmarks

All device figures below are **unmeasured design targets at 30 °C/75% RH inlet, 20 m³/h for 8 h, and ≥4 h at 600 W/m² incident sunlight on 1 m²**. A measured rating needs supply and regeneration exhaust balances, fan power, and the actual collector efficiency.

| Option / evidence | Moisture outcome at stated boundary | Energy boundary |
| --- | --- | --- |
| Open vent, equal 160 m³/day flow (calculated comparator) | 0 kg/day removed *from incoming air* relative to its outdoor inlet; room humidity still depends on indoor loads | No desiccant regeneration; fan energy depends on installed vent |
| This two-bed vent (target, not demonstrated) | 0.20 kg/day from incoming air, i.e. 1.25 g/m³ mean reduction; reject if whole-day test misses target | ≤48 Wh/day electric **plus** ≥1.5 MJ/day useful solar heat; 8.64 MJ incident in the reference sun window implies ≥17% useful collection before all other losses |
| ENERGY STAR certified portable compressor dehumidifier ≤25 pints/day (published certification threshold, not a matched test) | Integrated energy factor ≥1.70 L/kWh under standardized test conditions; dehumidifies *room air*, not supply air.[2] | Grid electricity; capacity, test duty and water-handling boundary differ from this vent |

The vent's target ratio is ~4.17 L/kWh of **auxiliary electricity only** (0.20 L ÷ 0.048 kWh); counting solar heat, fabrication or storage changes that comparison. No claim of outperforming a certified dehumidifier follows. Even the 0.49 MJ/day latent-heat floor already stated above excludes sensible heating and thermal losses. No measured prototype or apples-to-apples state-of-art solar-desiccant comparator exists yet for this form factor.

## Deployment Scenarios

- **Intermittently powered, humid-room retrofit:** For a hypothetical 40 m³ room, 20 m³/h is 0.5 air changes/hour *while running*, before leakage and installation losses. An installer first repairs rain ingress and checks combustion appliances; the unit can temper a limited incoming-air stream on sunny wet days, not guarantee a whole-room RH threshold. A window opening must remain safe and code compliant.
- **Clinic or community storeroom:** Use only for non-critical storage with logged inlet/supply humidity and an independent room hygrometer. Reject medicines requiring controlled humidity or temperature unless a separate qualified system meets those specifications; keep a powered backup if the required ventilation or dryness cannot pause overnight.
- **Post-repair building drying study:** After leaks are fixed, compare this vent with an equal-flow ordinary vent in matched rooms over a wet season. Record surface temperature, indoor humidity and RH-threshold hours; do not treat water transferred from supply air as measured mold prevention. Flooded structures need professional remediation, not this cassette.

## Risks & Mitigations

- **Saturation, cloudy days or humid nights:** verify capacity and cool-down before switching; flag not drying and use independent compliant ventilation, not an untested night-time moisture claim.
- **Heat, backdraft and smoke:** isolate hot regeneration ducts, prevent exhaust re-entry, and require installer review of combustion/pressure and fire-compartment rules. Stop forced operation on smoke ingress; never replace a required vent with a closed damper.
- **Clogged screens, gel dust or microbial fouling:** washable prefilter, contained coated beds, monthly screen cleaning and annual bed inspection; stop use if coating sheds or the bed stays wet.
- **Rain, freeze, insects and tampering:** screened labyrinth intake, drain and weather seal, accessible fixings and cold-weather rejection testing; do not promise universal climate suitability.
- **Damper seizure, seal leakage, sensor drift or battery aging:** interlock and leak-test air paths, cross-check probes, display a fault and design the bypass to remain independent. Establish cycle life and replacement interval in trials, not by assertion.

## Vision for 2050

If independently replicated chamber and building trials establish real indoor benefit, safe installation and viable maintenance, local repair shops could fit small solar-regenerated air cassettes to suitable rooms without continuous grid power. Their visible **not drying** signal would be as important as their sunny-day capacity: owners could distinguish functioning moisture removal from mere airflow and still prioritize leak repair, safe ventilation and adequate building envelopes. This is a conditional adoption vision, not a forecast or a substitute for health evidence.
