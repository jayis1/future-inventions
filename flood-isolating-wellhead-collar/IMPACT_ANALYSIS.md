# Flood-Isolating Wellhead Collar — Impact Analysis

**Author: jayis1. Illustrative scenario model, not observed outcomes or a claim of drinking-water protection.** The relevant counterfactual is a code-compliant watertight cap and elevated vent, not an open well.[3] The collar addresses cap-path ingress only, and its incremental effectiveness versus that counterfactual is unknown.

## Scope and assumptions

All scenario entries below are **invented sensitivity assumptions**, not population estimates or published contamination rates. The horizon is one year at a mature installed fleet; each well is counted at most once per year. A flood exposure means water reaches the vulnerable cap joint *within the design envelope* (not simply that a community floods). Annual fleet size is an assumed eligible-and-installed subset, not all private wells.

| Variable | Low | Base | High | Interpretation |
| --- | ---: | ---: | ---: | --- |
| Installed eligible wells, N | 2,000 | 10,000 | 100,000 | Hypothetical program size; assumes contractor approval and upkeep. |
| Annual in-envelope joint exposure, F | 10% | 10% | 20% | Hypothetical site-specific exposure probability. |
| Cap-path ingress probability under compliant comparator, B | 10% | 20% | 30% | Hypothetical *mechanical* events per exposed well; not positive water tests. |
| Incremental fraction of those ingress events prevented, E | 10% | 25% | 40% | Purely assumed; requires paired testing against compliant controls. |
| Cost per cap-path event, C | US$100 | US$200 | US$400 | Illustrative marginal cleanup/repair cost, not measured and not medical costs. |

## Reproducible calculation

Expected exposed wells = N × F. Expected comparator cap-path ingress events = N × F × B. **Hypothetical incremental events avoided** = N × F × B × E. Illustrative *gross* annual cost avoided = avoided events × C. These are expected values, not guaranteed integer observations.

| Scenario | Exposed wells/year | Comparator cap-path events/year | Hypothetical incremental events avoided/year | Gross cost avoided/year |
| --- | ---: | ---: | ---: | ---: |
| Low | 200 | 20 | 2 | US$200 |
| Base | 1,000 | 200 | 50 | US$10,000 |
| High | 20,000 | 6,000 | 2,400 | US$960,000 |

If a matched trial finds **E = 0**, the modeled incremental benefit is zero in every case. If the collar worsens ventilation, owner testing behavior or cap integrity, the actual effect can be negative. More installations do not automatically mean more avoided contamination, and cap-path events avoided are **not** equivalent to safe wells, illnesses prevented or households spared post-flood testing. No health outcome is projected without exposure and epidemiological evidence. After suspected flooding, use safe alternative water and follow applicable inspection, disinfection and testing guidance, including chemical testing when relevant.[1]

## Cost and sensitivity boundary

The README's unvalidated **2035 ex-factory** target is US$75 per kit at 100,000 units/year and US$12 per scheduled service-parts set; neither is an installed price. Multiplying by scenario fleet sizes gives notional kit outlays of **US$150,000 / US$750,000 / US$7,500,000**, plus an illustrative **US$24,000 / US$120,000 / US$1,200,000** for *one* parts set per well. These are not validated procurement quotes; installation, survey, high-vent support, electricity, labor, testing, replacement and repairs are excluded. The gross benefit table must **not** be called net savings or compared against one-time capital expense without service life, discounting and actual incremental cost versus a standard cap.

For scale intuition, at N = 10,000 and F = 10%, B = 20%, each **10 percentage-point** change in assumed E changes the modeled result by **20 cap-path events/year**; this linear sensitivity is arithmetic, not evidence that E has that value. The pilot must measure B and E under matched hydraulic conditions, with blinded independent water samples and recorded flood exposure. It must also measure witness misses, vent pressure drop and post-flood testing adherence. Only then can an impact estimate use observed denominators and uncertainty intervals.

## Source context

[1] https://www.cdc.gov/water-emergency/about/how-to-disinfect-wells-after-an-emergency.html — post-flood caution; no scenario parameter is taken from it.
[3] https://www.epa.gov/sites/default/files/2016-12/documents/gwr_sanitary_survey_guidance.pdf — sanitary-cap/vent comparator context; no scenario parameter is taken from it.
