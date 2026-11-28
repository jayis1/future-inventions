# Impact Analysis — Nitric-Acid Tailgas Catalyst Skid

**Author: jayis1** · Illustrative scenarios, not measured performance or a deployment forecast.

## Boundary and method

A hypothetical un-abated nitric-acid line vents dry gas at normal conditions (0 °C, 1 atm; 22.414 Nm³/kmol). N₂O molecular mass is 44 kg/kmol. For normal flow Q (Nm³/h), dry inlet C (ppmv), plant operating hours H, online conversion R and skid availability U:

- Baseline N₂O (t/yr) = Q × C / 1,000,000 × 44 / 22.414 × H / 1,000.
- Avoided N₂O (t/yr) = baseline × R × U; remaining stack N₂O = baseline − avoided, **assuming untreated flow during skid outage**. Do not confuse conversion while online with annual removal.
- Climate equivalent = avoided N₂O × 273 tCO₂e/t N₂O (AR6 100-year GWP for communication, not necessarily the regulated accounting factor).[6] Gross benefit excludes lifecycle burdens until separately subtracted.

| Hypothetical case | Q Nm³/h | C ppmv dry | H h/yr | R online | U | Baseline t N₂O/yr | Avoided t N₂O/yr | Remaining t N₂O/yr | Gross tCO₂e/yr |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 8,000 | 300 | 7,000 | 80% | 85% | 33.0 | 22.4 | 10.6 | 6,122 |
| Base | 10,000 | 500 | 8,000 | 90% | 95% | 78.5 | 67.1 | 11.4 | 18,328 |
| High | 12,000 | 700 | 8,400 | 95% | 98% | 138.5 | 129.0 | 9.6 | 35,205 |

All rows are rounded only at display. The original README's ≈77 t/yr assumes 8,760 h and 100% skid availability; the base case above uses 8,000 h and 95% skid availability. Neither is a claim about a typical plant. EPA reports 88–98% reduction for a historical sample of tertiary controls; those are **different systems**, not evidence of this skid's conversion.[5]

## Additionality, energy and adoption sensitivity

An already controlled train must use **measured residual** inlet N₂O as its baseline: if an incumbent destroys 50% of the hypothetical base feed before this module, illustrative incremental savings fall to about 33.6 t N₂O/yr (9,164 tCO₂e/yr), not 67.1 t. No second credit goes to the incumbent's earlier removal. At the base Q and 300 Pa, the README's 1.39 kW/≈11.1 MWh over 8,000 h applies **only if actual hot-gas flow happens to equal 10,000 m³/h and blower efficiency is 60%**; an illustrative 0.4 tCO₂e/MWh electricity factor would subtract ≈4.4 tCO₂e/yr. Actual expander-work penalty, heating, fuel, reductant (if a different chemistry is needed), catalyst manufacturing and transport require site data; a heater can overwhelm this electrical example. The net result is therefore **unknown**.

Ten independent eligible base-case lines would yield a *gross hypothetical* 671 t N₂O/yr or ≈183,280 tCO₂e/yr, before lifecycle debits and correlated performance failures; the number of eligible/adopting lines is unknown. At fixed other inputs, annual benefit scales linearly with flow, inlet concentration, operating hours, conversion and availability. A 3–5-year catalyst-life target implies variable replacement and disposal costs, not a measured durability result; an early poison event could erase both the uptime and business case. The ex-works US$0.5–1.5m target omits installation and shutdown, so no defensible cost per tonne is available yet.

## Evidence required for a claim

A pilot must continuously reconcile dry/wet flow and N₂O inlet/outlet measurements with stack tests, report missing data and bypass hours conservatively, retain independent NOₓ compliance and quantify any incremental heat, lost expander recovery and catalyst lifecycle emissions. Use the jurisdiction's specified GWP and reporting method for official inventories rather than this illustrative AR6 conversion; EPA's nitric-acid reporting guidance is train-specific.[3] Only compare **net incremental** benefit against a documented no-project baseline. If verified emissions, permit compliance or economics fail, reject deployment.

## Sources

[3] https://www.epa.gov/system/files/documents/2024-04/v_nitricacid_infosheet_2024.pdf
[5] https://www.epa.gov/sites/default/files/2015-12/documents/nitricacid.pdf
[6] https://www.epa.gov/ghgemissions/understanding-global-warming-potentials
