# Impact Analysis — Solar Steam Waste Quarantine

**Author: jayis1. Illustrative scenario model, not measured outcomes or a deployment forecast.** This model applies only to separately approved, segregated soft infectious waste. It does not count sharps, pathological or chemical waste and assumes final disposal remains regulated.

## Baseline and method

WHO reports that about 15% of healthcare waste is hazardous (not all steam-compatible) and that open burning/low-temperature incineration can emit dioxins, furans and particulates. That percentage is **not** multiplied by a speculative global tonnage here. The addressable facility count is unknown until a regional survey establishes actual waste composition, treatment access, solar exposure, staffing and lawful disposal routes. [WHO: Health-care waste](https://www.who.int/news-room/fact-sheets/detail/health-care-waste)

All figures below are **planning assumptions**, except arithmetic derived from them. The README's 4 m² collector, 5 kg batch ceiling and 200 nominal operating days/year define capacity, not efficacy. A passing batch requires load-specific cold-spot records and the locally required biological-indicator procedure. No unit is approved or operating today.

| Input | Assumption and boundary |
| --- | --- |
| Load | Up to 5 kg compatible soft waste per qualified batch; scenario assumption of sufficient segregated feedstock. |
| Operating opportunity | 200 attempted sunny-day batches per unit-year, one per such day; a cloudy or failed attempt is not treatment. |
| Qualified-batch fraction | Low 40%, base 70%, high 85% of attempts; assumed net of weather, faults and biological/record failures. |
| Displacement fraction | Low 25%, base 50%, high 70% of qualified mass would otherwise have been open-burned; survey-dependent, not a global rate. |
| Fleet in a mature illustrative year | Low 100, base 1,000, high 10,000 installed and maintained units; no adoption date implied. |
| Water and energy screening | Up to 3 kg feedwater and 3.5 kWh collected solar heat per attempted batch in the README example; condensate captured; actual makeup water, backup electricity and pumping measured in pilot. |

**Formula:** qualified tonnes/year = units × 5 kg/batch × 200 attempts/year × qualified fraction ÷ 1,000 kg/tonne. Potential open-burn-diverted tonnes/year = qualified tonnes × displacement fraction. These are not measured emissions reductions or verified prevention of infections.

| Illustrative case | Units | Qualified tonnes/year | Potential tonnes/year shifted from open burning |
| --- | ---: | ---: | ---: |
| Low | 100 | 40 | 10 |
| Base | 1,000 | 700 | 350 |
| High | 10,000 | 8,500 | 5,950 |

The base case means 0.7 qualified tonne per unit-year; the high case remains below the README's nominal 1 tonne/unit-year ceiling. If all qualified mass already went to licensed autoclaves rather than open burning, the *incremental* open-burning benefit is zero. If local rules reject the process, all qualified mass for this purpose is zero.

## Resource and cost sensitivity

At 200 attempts/year, the README's screening input is up to **600 kg feedwater and 700 kWh collector-delivered thermal energy per unit-year** under its sunny-window assumptions; these are not purchased electricity or guaranteed output. The 3.5 kWh/batch energy budget includes a 2.2–2.9 kWh estimated demand, but cloud, collector soiling and auxiliary power can eliminate its margin. Meter backup electricity, water quality and discharged/captured effluent before an environmental comparison.

**Illustrative base cost, not a price quote:** assume installed US$3,000 depreciated over 10 years (US$300/year), annual upkeep US$225 (within README range), indicators US$100, allocated labor US$200 and compliant final disposal US$150. Total US$975/year ÷ 700 qualified kg/year = **US$1.39/kg** before water, backup electricity, finance, taxes, training, downtime replacement or failed-batch transport. Doubling indicators or maintenance adds US$100 or US$225/year respectively; if qualified output halves while fixed expenses persist, unit cost doubles. Gather actual local quotes rather than extrapolating this figure to procurement decisions.

No particulate, dioxin, CO₂e or infection-count reduction is asserted: these require site-specific emissions factors, measured baseline practices, lifecycle manufacturing and replacement data, and reliable exposure/surveillance outcomes. Staff injury risk may fall or rise depending on handling and pressure incidents. The decision metric is verified safe disposal per qualified kg **including** hazardous-load backlog and final-disposal receipts, not nominal capacity or solar fraction alone.

## Decision gates

A pilot should report attempted batches, percent passing indicators, failed-load disposition, water and backup kWh per qualified kg, pressure/steam incidents and audited downstream disposal. Compare identical waste streams and full service boundaries against the licensed local alternative. Any failed biological challenge, uncontrolled vent/condensate, false release or unauthorized pressure vessel stops the pilot; read the [roadmap](./ROADMAP.md) before interpreting these scenarios as a deployment commitment.
