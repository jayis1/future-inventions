# Solar-Desiccant Paddy Dryer — Impact Analysis

**Author: jayis1. Status: illustrative scenarios, not measured outcomes or a market forecast.** The [README.md](README.md) gives the design and sources; no field trial has established safe output, loss reduction or emissions benefit.

## Basis and method

One qualifying 100 kg batch begins at 18% moisture, wet basis: 82 kg dry solids / (1 − 0.14) = 95.35 kg theoretical output at 14% moisture; 4.65 kg water must leave. This assumes no dry-solids loss and no rejected grain. A real dryer may reject a lot, and already contaminated grain is not rescued by moisture removal. Harvest weather, starting moisture, maintenance and available backup heat determine actual utilization.

For a site with B successfully processed batches/year, wet throughput = B × 0.1 tonne; theoretical dried throughput = B × 95.35 kg; water removed = B × 4.65 kg. For a *hypothetical* loss-rate difference d relative to a matched existing-dryer control, incremental saleable grain = B × 95.35 kg × d, provided the same dry-matter basis and marketability rules apply. This is one yield metric, not an additional spoilage benefit to add again. No actual d is known; rejected lots must be subtracted before applying the formula.

| Illustrative utilization | Accepted batches/year | Wet throughput | Theoretical dried output | Water removed | Assumed incremental saleable grain |
| --- | ---: | ---: | ---: | ---: | ---: |
| Conservative: no measured loss benefit | 50 | 5 t | 4.77 t | 233 kg | 0, at d = 0 |
| Central: trial hypothesis only | 100 | 10 t | 9.53 t | 465 kg | ~95 kg, at d = 1 percentage point |
| Optimistic: not a forecast | 150 | 15 t | 14.30 t | 698 kg | ~429 kg, at d = 3 percentage points |

Rounded figures assume each counted lot reaches the storage endpoint; downtime, contamination rejection, and low insolation lower them. A lost batch cannot count toward successful throughput. In each scenario the assumed d must be established with matched controls rather than inferred from a moisture reading.

## Energy, cost and emissions boundaries

The design targets ~0.24 kWh blower electricity and **30–36 MJ delivered thermal heat per complete bed reset** per 100 kg batch; these are not measured system values. At 100 batches the arithmetic budget is 24 kWh fan electricity and 3,000–3,600 MJ dock heat annually, before controls, auxiliary heat upstream of the dock, leakage, and missed regeneration. Collector output is intermittent, and solar heat must not be counted as free energy or assumed to replace a diesel dryer one-for-one. Meter actual collector heat, backup fuel/electricity and the counterfactual dryer's energy per accepted tonne. Operating emissions avoided = baseline metered emissions − project metered emissions, with emissions factors documented for each fuel and grid; embodied collector, stainless, electronics and replacement sorbent/filter emissions require a separate life-cycle inventory. The sign of net emissions is unknown.

At the stated unquoted US$1,900 equipment goal and ten-year service life, straight-line capital alone is US$190/year; the preliminary US$80/year maintenance allowance gives US$270/year before finance, installation, labor, battery, calibration, testing and heat. Dividing by successful batches yields a cost only after utilization and all omitted items are measured. No avoided-loss revenue, payback or emissions credit is claimed.

## Validation and uncertainty

Log weather, harvest-to-drying delay, initial moisture distribution, rejected lots, accepted lots, measured water balance, sensor calibration, head-rice yield and food-safety laboratory results over two seasons. Compare randomised or well-matched lots with maintained solar bubble and heated-air dryers at equivalent final moisture; report confidence intervals and separate sunny from humid-hour results. The largest unknowns are regeneration heat at scale, zeolite working capacity after repeated use, variability in crop quality and whether the baseline would have lost grain at all. If safe output or full cost is worse than existing practice, modeled throughput is not impact. IRRI guidance and the small-sample zeolite study are linked in the README's Sources section.
