# Impact Analysis — Repairable Iron-Air Outage Bank

**Author: jayis1** · Scenario arithmetic, not demonstrated performance or a sales forecast. Scope: noncritical outage loads only; no health outcome or carbon saving is claimed.

## Assumptions and boundary

- Nameplate concept: 5 kWh usable at the protected DC bus, rated 1 kW DC for five hours at 20–35 °C, with a proposed ≥40% input-to-DC-bus cycle efficiency including converter and auxiliaries. None has been measured for this design.
- For scenario arithmetic only, use exactly 40% round-trip efficiency and 90% downstream inverter efficiency: **4.5 kWh AC delivered** per full discharge, **12.5 kWh charge input** per full cycle, and **36% input-to-AC efficiency**. A DC-only load may avoid inverter loss but requires its own converter analysis. Idle losses, reserve, cold weather and aging are excluded; actual delivered energy can be lower.
- Count one *qualifying outage* as enough load to consume a full module discharge and sufficient prior charge. Fleet availability is the fraction of nominal module-outage opportunities actually met after readiness, maintenance and source limitations; assumed rather than measured. Distinct outage events are not equivalent to independent customers or days of service.

| 2050 illustration | Low | Central | High |
| --- | ---: | ---: | ---: |
| Installed modules, assumed | 100 | 1,000 | 10,000 |
| Qualifying outages per module-year, assumed | 2 | 6 | 12 |
| Available fraction, assumed | 70% | 85% | 95% |
| Installed nominal DC capacity | 0.5 MWh | 5 MWh | 50 MWh |
| Annual AC load served = modules × outages × availability × 4.5 kWh | 0.63 MWh | 22.95 MWh | 513 MWh |
| Annual charge input = AC load served ÷ 0.36 | 1.75 MWh | 63.75 MWh | 1,425 MWh |
| Initial installed module cost = modules × $2,400 | $240,000 | $2,400,000 | $24,000,000 |

For one module, a proposed 0.3 kW AC noncritical load for 12 hours needs 3.6 kWh AC; a 0.6 kW AC load for seven hours needs 4.2 kWh AC. Both fit within 4.5 kWh *only if* measured output meets the concept target and no reserve/derating is needed. A single module cannot cover a continuous 1 kW AC load for five hours or a multi-day 1 kW outage. At full charge, 10,000 units hold 50 MWh usable DC, **not** 50 MWh AC: the assumed AC maximum is 45 MWh.

## Lifetime, costs and climate limits

At the original unquoted service allowances ($100 per module-year plus $200 every five years), a ten-year accounting illustration adds $1,400 per installed unit in nominal undiscounted service, assuming two $200 events; with the $2,400 installation, that is **$3,800/module** before charging electricity, inverter, solar, taxes, financing, major replacements or recycling. Ten years of the central annual service figure would be 229.5 MWh AC across a constant 1,000-unit fleet, *if* all assumptions persist; neither ten-year calendar life nor maintenance sufficiency has been established. Annual full cycles in the scenarios are far below the proposed 1,000-cycle durability gate; idle corrosion and calendar aging may dominate.

Do not convert AC kWh served into diesel saved without metered generator displacement, actual fuel consumption and generator availability; do not claim net emissions reduction without charging-source intensity, marginal generation, manufacturing and disposal data. At 36% input-to-AC efficiency, charging losses can reverse a putative emissions benefit if the charging electricity is carbon-intensive. Report real outage-service hours, repair time, material recovery and full lifecycle cost alongside energy delivered before making an impact claim.

## Evidence boundary

A California Energy Commission report documents independently reviewed tests of a different, much larger Form Energy iron-air DC prototype: ~2.81 kW, ~306 kWh and 108–110 hours discharge; its measured round-trip efficiency was not published.[1] The 2025 NLR Annual Technology Baseline assumes 85% round-trip efficiency for commercial battery storage, not this proposed device.[4] Neither source validates this invention's capacity, cost, repairability, lifespan or deployment scenarios.

## Sources

[1] https://www.energy.ca.gov/sites/default/files/2025-11/CEC-500-2025-045.pdf
[4] https://atb.nlr.gov/electricity/2025/commercial_battery_storage — NLR 2025 ATB Commercial Battery Storage
