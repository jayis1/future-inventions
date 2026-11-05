# Batch-Witness Chlorination Kiosk — Impact Analysis

**Author: jayis1** · Scenario model, not measured water safety, health impact, regulatory approval or a market forecast. The device remains a TRL 2 concept. The existing README's WHO/UNICEF population estimate is not its addressable market.[1]

## Model and baselines

One unit holds 40 L; the design schedule is two batches per staffed day. Nominal output = 40 L/batch × 2 batches/day × 365 days/year = **29,200 L/year** at perfect availability and acceptance. Compliant output = nominal output × staffed-day fraction × source-suitability fraction × batch-pass fraction. These factors are modeled independent for arithmetic convenience, not empirically independent; measure joint distributions in a pilot. An ordinary staffed batch chlorinator on the *same source* is the comparator, not untreated water. Its compliance and cost are unknown; collect paired data before claiming incremental benefit.

| Scenario (illustrative assumptions, not forecasts) | Staffed days | Suitable source | Passing batches | Modeled L/year | 2 L/person/day drinking-only equivalents |
| --- | ---: | ---: | ---: | ---: | ---: |
| Constrained | 60% | 70% | 80% | 9,811 | 13.4 |
| Base | 80% | 85% | 90% | 17,870 | 24.5 |
| Favorable | 95% | 95% | 98% | 25,826 | 35.4 |

Values are rounded from the stated formula; an equivalent is a volume ratio, not a count of people with safe access. At 100 hypothetical base-case units, modeled output is 1.787 million L/year, **only if** each has the same staffing, water-quality envelope, consumables and independent safe backup. Cooking, washing, storage loss, seasonal outages and higher per-person demand lower actual reach. A failed or locked batch contributes zero to compliant output, even if water was dosed.

## Cost and resource sensitivity

The README's **US$140 ex-workshop in 2038 at 10,000 units/year** is an unquoted design target, not a purchase price. Straight-line allocation over a *target* five-year life is US$28/year per unit before replacements, financing or installation. At modeled base output this alone is about US$0.00157/L; at constrained output about US$0.00285/L. For transparent sensitivity, an illustrative US$100/year combined allowance for chemicals, cartridges, DPD controls and maintenance plus US$500/year operator labor produces annual modeled costs of US$628/unit (still excluding calibrated instruments, source assays, rejected-batch disposal, shipping, financing, certification and backup supply). That is approximately US$0.035/L at base output, US$0.064/L constrained and US$0.024/L favorable. These dollar allowances are invented scenario inputs, **not quotes**: substitute site invoices and measured person-hours. A doubled US$100 consumables/maintenance allowance adds about US$0.0056/L at base utilization; a 50% cut in passing volume doubles cost per compliant litre. Compare all-in delivered costs, including conventional operator labor and backup water, in the same currency and year.

## What must be demonstrated

A 200-batch paired study can estimate counts of premature releases and false lockouts, but zero observed unsafe releases does not imply zero risk. Independent laboratories should test indicators, chlorine residual, byproducts and stored-water quality at the relevant source conditions; compare to local drinking-water criteria and the conventional comparator. Record cartridge and reagent consumption, rejected litres, staff minutes, leaks, valve cycles, downtime and backup-water use. Attribute impact only to the measured *difference* in compliant delivered water and all-in cost, with uncertainty intervals. Do not translate modeled litres into prevented disease or deaths. If chemical contaminants, chlorine-resistant organisms or unsafe containers dominate, the kiosk may have no net benefit and must not be deployed without another validated barrier.[5][6]

## Sources

[1] WHO/UNICEF, 2025 JMP update: https://www.who.int/news/item/26-08-2025-1-in-4-people-globally-still-lack-access-to-safe-drinking-water---who--unicef
[5] CDC, *Water Disinfection for Travelers*: https://www.cdc.gov/yellow-book/hcp/preparing-international-travelers/water-disinfection-for-travelers.html
[6] CDC, *How to Make Water Safe in an Emergency*: https://www.cdc.gov/water-emergency/about/
