# Dry-Reset Rain Diverter — Impact Analysis

**Author: jayis1**

**Status:** Illustrative calculations and adoption scenarios, not observed benefits or a forecast. The device has no prototype field data. Collection is untreated; first-flush diversion does not make water potable [1][2].

## Reference installation and mass balance

- Catchment area `A = 100 m²`; annual rainfall `P = 600 mm/year` (scenario assumption, not a site climatology); runoff coefficient `C = 0.8` (assumed, varies with roof and storm). Since 1 mm on 1 m² is 1 L, annual roof runoff before diversion is `P × A × C = 48,000 L/year`.
- Assume `N = 40 qualifying, independently reset events/year`, each diverting `D = 25 L`. Total planned first flush is `N × D = 1,000 L/year` (2.1% of reference runoff). Events too small to fill the chamber produce **zero collected water** for that event; this simple annual estimate assumes all reference runoff occurred in qualifying events. Storm sequence, drain rate and rainfall distribution must be measured.
- Ideal post-diversion ceiling: `48,000 − 1,000 = 47,000 L/year`. Assume `f = 0.60` of that volume is actually captured and usable for an approved non-potable demand after tank overflow, outages and demand mismatch: `V = f × (P × A × C − N × D) = 28,200 L/year` or `28.2 m³/year`. This is an *illustrative upper accounting scenario*, not a water-quality or verified displacement result.
- Actual displaced mains supply is `min(usable stored volume, eligible non-potable demand)`, with an additional correction for any supply that would otherwise have been used. Do **not** add collected water to displaced mains water as two separate benefits. Tanks, gutters, installation, treatment, compliance and source-water testing are outside the ex-workshop unit cost.

## Sensitivity to climate and event pattern

Hold `A = 100 m²`, `C = 0.8`, `D = 25 L` and vary rainfall, number of qualifying resets and captured fraction. Each row assumes the specified rainfall is delivered in qualifying events; an actual dry climate with many sub-25 L showers yields less.

| Scenario | P (mm/year) | N (events/year) | f | Runoff (L/year) | Ideal after flush (L/year) | Usable non-potable bound (L/year) |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 300 | 30 | 0.40 | 24,000 | 23,250 | 9,300 |
| Reference | 600 | 40 | 0.60 | 48,000 | 47,000 | 28,200 |
| High | 900 | 50 | 0.70 | 72,000 | 70,750 | 49,525 |

For a different roof, replace `A` in the formula and resize `D` under local guidance; retaining 25 L on a larger roof is not equivalent first-flush depth. The 25 L diversion equals 0.25 mm *actual runoff* over 100 m², or 0.3125 mm incident rainfall with `C = 0.8`. At a reference 20 mm event, incident rain is 2,000 L and runoff 1,600 L; after 25 L diversion, at most 1,575 L could reach storage before overflow and other losses.

## Adoption scenarios (not forecasts)

If 1,000 suitable installations each match the reference scenario *and* have at least 28.2 m³/year of eligible non-potable demand, their aggregate upper bound is 28,200 m³/year of usable rainwater. At 10,000 installations it is 282,000 m³/year. Without verified counterfactual supply and adequate demand, neither total equals proven mains-water savings; at zero eligible demand, displacement is zero. Site variability and correlated drought make simple multiplication optimistic. These figures cannot be extrapolated to prevented illness or population health.

## Cost, maintenance and trade-offs

The README's **unquoted manufacturing targets**, not market prices, are US$42 ex-workshop per unit at 10,000/year and US$8/year for service parts. Over a hypothetical 10-year life that is `42 + 10 × 8 = US$122` before installation, labor, tank, testing, replacement, treatment and disposal. At reference yield, 10 years of usable volume would be 282 m³ only if performance remains constant; `US$122/282 m³ ≈ US$0.43/m³` covers **only** the stated manufacturing and parts goals, not full lifecycle cost or savings. Labor and additional waste from seals/screens may erase the benefit relative to an existing maintained diverter. No energy or emissions saving is claimed; operation itself has no electrical demand but manufacturing and replacement have embodied impacts.

The actual incremental benefit is the measured difference in missed-reset incidents, tank-inlet sample results and net non-potable yield **versus an equally serviced standard diverter**, minus extra service and equipment cost. Compare within matched roofs over two seasons; pre-register fault definitions and disclose failures. Abandon the extra mechanism if there is no meaningful advantage. Water-quality outcomes cannot be inferred from the mass balance [1][2].

## Sources

[1] CDC, *Collecting Rainwater and Your Health: An Overview*: https://www.cdc.gov/drinking-water/about/collecting-rainwater-and-your-health-an-overview.html — contamination and the need for treatment/testing.

[2] Australian Drinking Water Guidelines §4.2.2: https://guidelines.nhmrc.gov.au/australian-drinking-water-guidelines/part-1/chapter-4/4.2-applying-the-framework/4.2.2-preventive-measures-for-drinking-water-quality-management — existing preventive measures and maintenance; no performance figure for this proposed design.
