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
