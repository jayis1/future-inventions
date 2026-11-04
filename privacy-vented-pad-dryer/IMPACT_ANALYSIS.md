# Privacy-Vented Pad Dryer — Impact Analysis

**Author: jayis1**
**Status: scenario model, not observed benefit or forecast**

## Baseline and boundary

The counterfactual is a user's existing washed-pad drying method (for example, a ventilated line or screened rack), not an assumption that every cabinet displaces disposable pads. Count cabinet purchases and completed drying slots separately from any change in product choice. A cabinet alone cannot supply wash water, soap, pads, or a private washing space. Drying does not establish microbiological safety; no infection, school-attendance, carbon-saving, or disposable-waste reduction is claimed. Existing context on product choice and infrastructure is in [1] and [2] of the README.

## Transparent annual scenarios

These are invented *planning inputs*, not survey estimates. Assume four pad slots per completed batch and a one-cabinet-to-one-site relationship. Annual qualified-use days and completed batches/day already account for some weather and non-use; measure both in pilots. They do not guarantee all four pads attain the mass endpoint.

| Case | Cabinets in service | Qualified days/year | Completed batches/day/cabinet | Batches/year | Maximum pad drying slots/year |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 1,000 | 60 | 0.3 | 18,000 | 72,000 |
| Base | 10,000 | 100 | 0.5 | 500,000 | 2,000,000 |
| High | 50,000 | 150 | 0.7 | 5,250,000 | 21,000,000 |

Formula: cabinets × qualified days × completed batches per day = batches; multiply by four for *maximum* pad slots. A partly filled batch or an incompletely dried pad reduces realized completion. The README's 40,000 pads per batch at 10,000 cabinets is simultaneous nameplate capacity, not annual throughput.

## Energy, cost, and waste boundaries

The passive cabinet has zero operational electricity by design, but its embodied materials, transport, maintenance, and washing burden are not zero. An optional continuously running 5 W PV fan for six hours uses 0.03 kWh/batch; if *every* modeled batch uses it, annual fan demand is 540 / 15,000 / 157,500 kWh in the low / base / high cases. These are upper scenario totals under that usage assumption, not grid purchases: PV generation may be inadequate in cloudy weather, and battery or grid backup is not included. Existing laundry energy and water should be measured against controls rather than credited to the dryer.

At the unquoted US$18 ex-workshop target, initial cabinet hardware is US$18,000 / US$180,000 / US$900,000 for low / base / high fleet sizes. At an assumed five-year service life, simple hardware-only annual allocation is US$3.60 per cabinet; this excludes optional fan, shipping, installation, washing supplies, cleaning labor, replacement cards, financing and end-of-life. Supplier quotes, observed life and maintenance logs must replace this model before an affordability claim.

Avoided disposable products and waste: **unknown**. Estimate only after comparing the *same users*' purchases before and after adoption with a control group, accounting for seasonality, other reusable products, and whether pads were already being line-dried. Do not convert drying slots into displaced pads, kilograms of waste, emissions, or medical outcomes. Manufacturing impacts require a bill of materials and local end-of-life data; disposal paths for PP, aluminium, and cards vary by location.

## Evidence gates

Instrument 30 units over two seasons for mass-based dryness, weather, thermal and privacy failure rates, and matched line/rack performance. Follow with a 100-user consenting pilot that records qualified days, actual fill, alternatives, costs, cleaning burden and user preference. Publish denominator, sample size and uncertainty before replacing any scenario input with an estimate; independently review hygiene before any health-effect study.
