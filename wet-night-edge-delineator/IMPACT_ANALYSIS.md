# Wet-Night Edge Delineator — Impact Analysis

**Author: jayis1** · Illustrative planning model, not measured safety performance or an investment case. All US$ are undiscounted, constant-price assumptions; obtain local bids and crash data before use.

## Boundary and assumptions

One eligible *road-km* denotes one treated shoulder edge, not both sides of a two-lane road. A 20-km paired pilot precedes the hypothetical 500-km deployment. No installation on travelled lanes or shoulders without adequate setback and authority approval. Five-year horizon, no salvage value; the unit's assumed five-year average life ends at the horizon. Coverage requires 100,000 units, matching the README's 200/km spacing and manufacturing volume. It does not imply 100,000 simultaneously safe sites.

| Input | Planning assumption | Status / sensitivity |
| --- | --- | --- |
| Treated edge length | 500 km × 200 units/km = 100,000 units | Hypothetical maximum at 5 m spacing; field spacing is authority-set. |
| Factory hardware | US$6/unit = US$1,200/km | Unverified 2038 high-volume target, not a quoted price. |
| Installed capital, incl. base and labor | US$30/unit = US$6,000/km | **Assumed** all-in initial installed price; includes the US$6 hardware, not additional to it. |
| Routine inspection/cleaning | US$400/km-year | Assumed; excludes extraordinary traffic-control closures. |
| Insert replacements | 10% of units/year × (US$2 insert + US$8 labor) = US$200/km-year | Assumed; US$2 is the README manufacturing target. |
| Lost/broken full units | 2% of units/year × US$30 installed = US$120/km-year | Assumed incremental replacement; avoid counting the same unit again as an insert. |
| Exposure | 2,000 vehicles/day × 500 km × 365 days = 365 million vehicle-km/year | Assumed average traffic on treated edges; not a measured count. |
| Eligible wet-night edge-related crashes | 1 event / 100 million vehicle-km | **Illustrative placeholder**, not a published or site-specific crash rate. Must be replaced with linked local police/road data. |
| Causal reduction from the unit | Low 0%; base 5%; high 15% | **Hypotheses only**; no trial establishes any of these values. |

## Cost and safety scenario arithmetic

Initial capital = 500 km × US$6,000/km = **US$3.00 million**. Annual operations = 500 km × (US$400 + US$200 + US$120)/km = **US$0.36 million/year**. Five-year gross program cost = US$3.00m + 5 × US$0.36m = **US$4.80 million**, or US$9,600/km over five years (US$1,920/km-year simple average). The US$1,200/km factory hardware is part of—not added to—the US$6,000/km installed cost. Capital renewal *after* year five is excluded; inflation, financing, extraordinary closures and disposal costs remain unpriced and would raise the estimate.

The *assumed* eligible baseline is 365m vehicle-km/year ÷ 100m × 1 = **3.65 crashes/year** across 500 km; over five years it is 18.25 expected events. Events avoided = 18.25 × assumed causal reduction. Fractional results are statistical expectations, never promises of a fraction of an actual crash.

| Five-year case | Assumed reduction | Modeled events avoided | Gross cost / modeled event avoided |
| --- | ---: | ---: | ---: |
| Low | 0% | 0 | Undefined: no demonstrated benefit |
| Base | 5% | 0.9125 | ~US$5.26m |
| High | 15% | 2.7375 | ~US$1.75m |

A zero-crash-benefit case is plausible. No fatalities, injuries or money *saved* are inferred: crash severity, attribution and effect size are unknown. The gross cost/event ratio is not a cost-effectiveness verdict. There is **no demonstrated payback**; even a financial scenario would need defensible severity-specific costs, a matched control and opportunity-cost comparison with alternative countermeasures.

## What could change the result

Traffic and the eligible crash rate scale the modeled count linearly, but more traffic may accelerate fouling and breakage. At half or double either input, the modeled benefit halves or doubles, while fixed coverage cost does not. A doubled US$30 installed price raises initial capital to US$6m; contamination or plow loss could raise operations too. Compare *bids* for approved wet-reflective tape, studs and posts over the same five-year corridor, including marking maintenance, road closures and end-of-life removal, before claiming economic advantage.

The leading measurements are wet and dry angular return in cd/lx, 50 m closed-course detection and *correct interpretation* at 40 km/h, retention/debris, and cleaning/repair hours. Those are not crash reductions. Independent matched-corridor monitoring over multiple rainy seasons must estimate the safety effect while tracking speed compensation and broader changes to lighting, traffic and road geometry. Polymer insert wear and aluminum recycling need a measured material inventory before any environmental benefit claim.
