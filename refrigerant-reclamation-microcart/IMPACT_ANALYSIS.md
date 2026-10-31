# Impact Analysis — Refrigerant Reclamation Microcart

**Author: jayis1**

**Status: illustrative annual scenarios, not field results or a carbon-credit claim.** The reference is a maintained certified conventional recovery kit, not deliberate venting. The cart performs recovery and custody; off-site qualified processing determines reclamation.[1][2][5]

## Boundary and method

Only **incremental reclaimer-accepted mass** above matched conventional-kit jobs is considered. The original README's 10,000-cart × 50-job × 1-kg/job example yields 500 tonnes/year *collected*; its +0.1 kg/job hypothesis yields 50 tonnes/year *incremental accepted*. Neither is a measured avoided emission. Cylinder stock changes, material rejected later and losses during transport/processing must be reconciled; adding all recovered mass to an avoided-emissions ledger would count the baseline twice.

For an explicitly hypothetical mix-weighted **100-year GWP of 1,000 kg CO₂e/kg** (not an observed refrigerant mix), and an assumed **2% downstream leakage** of the incremental accepted mass:

`incremental accepted kg/year = carts × eligible jobs/cart/year × incremental accepted kg/job`

`illustrative avoided tCO₂e/year = incremental accepted kg/year × counterfactual release fraction × (1 − 0.02) × 1,000 / 1,000`

The release fraction is the portion of *incremental* mass that otherwise would reach the atmosphere over the accounting horizon rather than remain stored or receive another lawful treatment. A study must measure it; it is not automatically 100%. The GWP input must ultimately be replaced by a mass-weighted, documented refrigerant mix and a named assessment's 100-year values. Direct refrigerant emissions alone are shown; electricity, transport, production and destruction emissions are omitted pending life-cycle data, so these figures are **not net climate benefits**.

| Scenario | Carts | Jobs/cart/year | Total collected at 1 kg/job | Increment accepted/job vs kit | Increment accepted/year | Assumed release fraction | Illustrative direct emissions avoided/year |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Conservative | 1,000 | 25 | 25 t | 0.02 kg | 0.5 t | 25% | 122.5 tCO₂e |
| Planning case | 10,000 | 50 | 500 t | 0.10 kg | 50 t | 50% | 24,500 tCO₂e |
| Stretch case | 30,000 | 75 | 2,250 t | 0.15 kg | 337.5 t | 75% | 248,062.5 tCO₂e |

These are deliberately broad sensitivity cases, **not forecasts**. At zero measured improvement over a conventional kit, or zero counterfactual release, avoided direct emissions are zero regardless of carts sold. Changing the assumed mix GWP scales the displayed CO₂e linearly; it does not change kilograms recovered. The 2% downstream leakage is a placeholder, not a demonstrated industry rate. A trial must also separately log on-site leaks; if the cart increases them, subtract those emissions from the incremental benefit.

## Operational and economic checks

The README's unquoted US$3,000 capital goal depreciated over five years plus assumed US$250/year service equals US$850/year; divided by 50 kg/year collected, that is **US$17/kg collected** before wages, power, financing, cylinder exchange and reclaimer fees. If the cart only improves accepted mass by 0.1 kg/job, 50 jobs produce 5 kg/year *incremental* per cart: the same US$850/year is **US$170/kg incremental accepted**, before all omitted costs. This is an incremental-cost ceiling test, not a sale price; sharing carts or higher utilization would alter it. A deposit, service fee or verified public-health/climate program may be needed, but no credit revenue is assumed.

Report separate ledgers for initial charge, mass entering a cylinder, mass accepted by the reclaimer, reclaimed-to-specification output, destruction/residue, stock change and measured losses. Keep identities and uncertainty ranges for scales, analyzers and counterfactual sampling. Uncertain or ineligible A2L/A3, ammonia and high-pressure CO₂ streams are outside this model; ozone benefits from eligible legacy refrigerants are not quantified. No avoided virgin refrigerant production is added to the direct-emissions figure, preventing double counting. For any claim beyond a scenario, validate recovery equipment under applicable rules and AHRI rating methods.[1][2][4]

Independently verify downstream product specifications rather than treating field drying as reclamation.[5]

## Sources

[1] https://www.epa.gov/section608/refrigerant-recovery-and-recycling-equipment-certification
[2] https://www.epa.gov/section608/stationary-refrigeration-service-practice-requirements
[4] https://www.ahrinet.org/system/files/2023-06/AHRI_Standard_740-2016_1.pdf
[5] https://www.ahrinet.org/system/files/2025-03/AHRI%20Standard%20700-2024%20SI_0.pdf
