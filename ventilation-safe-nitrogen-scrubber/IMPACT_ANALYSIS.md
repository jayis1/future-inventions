# Ventilation-Safe Nitrogen Scrubber — Impact Analysis

**Author: jayis1.** These are **illustrative engineering projections**, not observed performance, population-health forecasts or fertilizer sales. The unit treats mechanically exhausted barn NH₃, not atmospheric N₂. Only qualified, actually treated exhaust counts; mandatory ventilation is held constant. The paired field comparator is the same fan with treatment bypassed, and any deployment decision also needs a conventional scrubber/source-control bid. See the README's [2] (Soto-Herranz et al., 2021) and [3] (Hadlocon et al., 2015) for measured but non-equivalent technologies.

## Boundary and assumptions

| Parameter | Assumption or target | Status |
| --- | --- | --- |
| Illustrative cohort | 1,000 eligible installed modules | Hypothetical, not an adoption forecast |
| Air volume and inlet | 10,000 m³/h, 20 ppmv NH₃, 25 °C per active module | Design condition; field averages vary |
| Gas conversion | 24.45 L/mol; 14 g N/mol NH₃ | Ideal-gas/atomic-mass approximation |
| Removal | 70% when treating in base case; 50% low, 80% high | 70% is the *unvalidated 30-day target*; others are sensitivities |
| Effective duty | 25% low, 50% base, 80% high of 8,760 h/year | Includes downtime, bypass and qualifying-inlet availability; assumed, not measured |
| Pressure and fan | ≤40 Pa clean-to-service target; 60% incremental fan efficiency | 0.185 kW per running module at 40 Pa; pump power unknown |
| Consumables and hardware | 98/28 kg pure H₂SO₄ per kg captured N; US$12,000 ex-factory + US$4,000 installation | Acid is stoichiometric **minimum**; costs are unvalidated 2038 volume targets |

Per module, inlet nitrogen at the stated constant condition is `10,000 m³/h × (20/1,000,000) ÷ 0.02445 m³/mol × 0.014 kg N/mol = 0.1145 kg N/h`. At 70% treatment capture, this is `0.0802 kg N/h`, or `0.702 tonne N/year` **only if continuously at that inlet, with no bypass**. The scenario equation is `1,000 modules × 0.1145 kg N/h × removal × 8,760 h/year × effective duty ÷ 1,000 kg/tonne`. Rounded values below use the unrounded formula.

## Quantitative scenarios for the illustrative cohort

| One-year outcome | Low: 50%, 25% duty | Base: 70%, 50% duty | High: 80%, 80% duty |
| --- | ---: | ---: | ---: |
| NH₃-nitrogen captured / avoided at the treated outlet, tonnes N | 125 | 351 | 642 |
| Pure-acid-equivalent theoretical minimum, tonnes H₂SO₄ | 439 | 1,229 | 2,247 |
| Dry ammonium-sulfate-equivalent maximum, tonnes | 591 | 1,655 | 3,027 |
| Incremental fan energy at 40 Pa, GWh | 0.406 | 0.811 | 1.298 |

Acid is `captured N × 98/28`; the dry-salt equivalent is `captured N × 132/28`. Both are ideal stoichiometry, **not** certified fertilizer harvest. Fan power is `40 Pa × (10,000/3,600) m³/s ÷ 0.60 = 0.185 kW` per operating module; cohort energy multiplies this by operating hours and 1,000 units. The **full** energy and environmental balance additionally needs measured recirculation-pump electricity, water, acid manufacture and transport, liquid testing, contaminated residual disposal and any fan changes outside this linear estimate.

At the 2038 volume-cost target, 1,000 modules require **US$16 million** installed hardware; straight-line division over the proposed ten-year nominal life is **US$1.6 million/year** before financing, replacements, acid, water, electricity, labor and disposal. No net operating savings, payback, avoided illness, emissions credit or carbon benefit is asserted. Product value and costs must be priced at each site; an acid-handling route is a condition of deployment, not a line item that can be omitted.

## What would invalidate the projection

Lower or variable NH₃ concentrations, unmeasured leaks, high bypass duty, demister fouling, fan-capacity losses, acid aerosol, contaminated product and expensive chemical servicing can all reverse the case. In particular, 70% **single-pass** removal when the module is active is not 70% reduction in barn workers' exposure or total farm emissions. A 10-site, 12-month paired trial must measure seasonal inlet/outlet mass flux, actual duty and solution N, audit ventilation and mist, and compare lifecycle cost and impacts with source control and proven scrubbers before any scale claim. The high case exceeds the design removal target and is a sensitivity, not a promised outcome. A 2050 deployment scenario cannot be extrapolated responsibly from these hypothetical 1,000-module figures.
