# Self-Verifying Radon Vent — Impact Analysis

**Author: jayis1.** Illustrative 10-year deployment scenarios, not demand forecasts, measured performance or prevented-cancer estimates. The starting cohort is **100,000 hypothetical eligible homes with elevated measured radon**; eligibility, affordability and occupancy would have to be verified. This analysis concerns the proposed device *as a mitigation installation*, not the incremental benefit over a correctly maintained conventional active vent.

## Inputs and accounting

| Assumption | Low | Base | High | Meaning |
| --- | ---: | ---: | ---: | --- |
| Cumulative installed homes by year 10 | 10,000 | 50,000 | 100,000 | Hypothetical adoption; upper bound is cohort size. |
| Operational and maintained fraction at year 10 | 80% | 90% | 95% | Scenario assumption, not observed uptime. |
| Independently confirmed below applicable local reference level among operational installations | 60% | 75% | 85% | Scenario assumption; requires accredited testing, not controller telemetry. |
| Mean continuous fan power | 25 W | 16 W | 8 W | Design range only; not a measured baseline or savings. |
| Installed cost per home | $2,000 | $1,450 | $900 | Planning values from README, excluding diagnosis/foundation repairs. |
| Annual service per home | $120 | $90 | $60 | Planning values from README; excludes electricity and accredited tests. |

The year-10 result is **installed × operational fraction × confirmed fraction**. These fractions should ultimately be estimated from separately audited maintenance and independent radon tests; their product does not prove that the device outperforms a standard system. Operational means a powered, maintained fan with usable evidence, not merely a green display.

| Year-10 scenario output | Low | Base | High |
| --- | ---: | ---: | ---: |
| Operational installations (homes) | 8,000 | 45,000 | 95,000 |
| Operational **and** confirmed below local level (homes) | 4,800 | 33,750 | 80,750 |
| Continuous fan electricity if **all installed units run all year** (kWh/year) | 2,190,000 | 7,008,000 | 7,008,000 |
| Install plus ten years of scheduled service, with all units assumed installed at start (US$) | 32,000,000 | 117,500,000 | 150,000,000 |

Electricity = installed units × W × 8,760 h/year ÷ 1,000. The ten-year cost illustration = installed units × (installed cost + 10 × annual service); it deliberately overstates service years for a gradual rollout, while **omitting** power tariffs, diagnostic work, foundation repairs, accredited testing, fan/sensor replacement beyond the service allowance, financing and inflation. The fan-energy row is a full-operation upper accounting case, not expected usage under outages. It is **not energy saved**: savings require a measured, properly sized conventional comparator in the same building.

## Exposure and sensitivity

A concentration example, *not a trial result*: a home measured at 200 Bq/m³ before and 100 Bq/m³ after independently tested mitigation would have an observed difference of 100 Bq/m³ under those particular test conditions. WHO recommends at least three months of measurement to estimate an annual mean because readings vary substantially day to day; paired seasonal measurements, placement and protocol matter.[1] There is no defensible fleet-average concentration reduction in the current evidence, so this analysis multiplies **homes verified below a threshold**, not Bq/m³ avoided. A home below a reference level is not guaranteed risk-free.

For the base 50,000-installation case, every **10 percentage-point** change in either assumed fraction changes the verified count by **3,750 homes** if the other fraction stays at 75% (operational sensitivity), or **4,500 homes** if it stays at 90% (confirmation sensitivity). These are arithmetic sensitivities, not confidence intervals. Loss of power, missed service, site exclusions and nonresponse could reduce real counts; priority for affordable access and paid inspections is necessary to avoid selecting only easy homes.

No deaths averted, clinical outcomes, certification, or incremental benefit versus conventional mitigation is projected. WHO describes exposure-related lung-cancer risk, but converting a hypothetical device cohort into avoided cases would require baseline exposure distributions, smoking prevalence, occupancy, latency and comparative field data.[1] The 100-home pilot in the README is the first opportunity to replace these assumptions with measured inputs.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/radon-and-health
