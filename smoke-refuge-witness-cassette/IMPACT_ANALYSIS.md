# Smoke-Refuge Witness Cassette — Impact Analysis

**Author: jayis1** · Illustrative annual planning model, not a measured health or market forecast. This is a particle-only room-air cleaner, not a certified refuge. Follow local evacuation guidance and keep cooling, ventilation and CO alarms independently available.[1][2]

## Assumptions and arithmetic

- Reference room: 40 m³; proposed smoke-particle CADR 200 m³/h at full speed with correctly seated fresh filters; 35 W draw. All three are untested combined targets, not achieved performance. EPA's portable-cleaner sizing rule is smoke CADR (cfm) at least two-thirds of room area (ft²).[2]
- One *usable* unit serves at most one suitable room at a time; usable fraction folds in correct installation, servicing and access to a safe room. Each modeled day has eight operating hours. Scenarios are hypothetical adoption and utilization ranges, not observed deployment rates.
- Equivalent clean-air volume = usable units × operating days × 8 h/day × 200 m³/h; electricity = same unit-hours × 0.035 kW. These are throughput equivalents, **not** a room's measured particle removal or outdoor pollution avoided. Real filter loading, mixing and infiltration lower or alter results.
- Recurring filter allowance: US$30–60 per usable unit-year from the README's unquoted planning range; events with heavy loading can require more replacements.[1] Hardware ex-factory target is US$210 per deployed unit, excluding distribution, taxes, certification, battery replacement and disposal. Do not add recurring allowances to a claimed all-in cost.

| Scenario | Deployed units | Usable fraction | Event days at 8 h/day | Usable rooms, max | Equivalent clean-air throughput | Running electricity | Annual filter allowance |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Conservative | 1,000 | 50% | 5 | 500 | 4 million m³ | 0.7 MWh | US$15,000–30,000 |
| Base | 10,000 | 70% | 20 | 7,000 | 224 million m³ | 39.2 MWh | US$210,000–420,000 |
| Optimistic | 50,000 | 90% | 30 | 45,000 | 2.16 billion m³ | 378 MWh | US$1.35–2.7 million |

Hardware target at initial deployment is US$0.21m / US$2.1m / US$10.5m respectively, before omitted costs; these are planning expenditures, not booked revenue. Electricity figures use 35 W continuously and exclude charger losses, standby and cooling, so they are not whole-house energy estimates. A nominal 160 Wh pack offers 4.57 h at 35 W *before* losses; four hours requires at least 140 Wh usable at the relevant aged-pack condition. Failure of that test removes the outage claim.

## What would make the model credible

Independent chamber testing must establish assembled-unit CADR and bypass after repeated filter changes, under heavy smoke and humid conditions. A matched field study must record indoor/outdoor PM₂.₅, room occupancy, heat, ventilation, filter use and cleaner uptime before estimating exposure changes; no fraction of the throughput above can be converted directly into avoided illness or lives saved. Compare with an appropriately sized commercial cleaner or well-built DIY alternative rather than an unfiltered room alone.[1][2]

Access is uneven: a loaner may be unusable without a suitable cool room, electricity to recharge, reachable maintenance, accessible alarms or replacement filters. Quantify these exclusion rates in the pilot. Filter waste and battery collection need local routes and mass measurements; no lifecycle emissions or landfill-avoidance claim follows from the present data. If filter cost doubles, the annual filter allowance doubles while the modeled usable fraction may fall; measure that sensitivity rather than assuming it away.

## Sources

[1] https://www.epa.gov/emergencies-iaq/create-clean-room-protect-indoor-air-quality-during-wildfire — EPA clean-room guidance and filter replacement
[2] https://www.epa.gov/wildfires/indoor-air-filtration — EPA filtration guidance and smoke-CADR sizing
