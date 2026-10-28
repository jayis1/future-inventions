# Impact Analysis — Fluoride Exchange Water Kiosk

**Author: jayis1.** Conditional engineering scenarios, not observed public-health outcomes. See [README.md](README.md) for the mechanism, safety boundary and [source links](README.md#sources). No kiosk water is certified potable; fluoride removal does not address microorganisms, arsenic or other site hazards without separate validated treatment.

## Assumptions and accounting boundary

- One kiosk is designed for 100 L per *operating* day from a screened source at 5 mg/L fluoride, with a proposed tap release criterion ≤1.0 mg/L. Assume 4 mg/L removed only for mass accounting; actual influent and effluent must be measured.
- A nominal 12 kg lead bed uses a provisional 1 mg F/g *working* capacity. The 2,000 L / 20-operating-day exchange cap corresponds to 8 g captured, two-thirds of the assumed 12 g capacity; the lag bed remains a guard. Capacity and safe interval are **not yet measured**.
- Allocate US$700 installed over five years (US$140/year), US$20 per sealed-bed exchange including modeled hub return and waste handling, and US$120/year for tests. These are unquoted 2038 USD assumptions at 10,000 units/year. Excluded: staff, power, financing, source surveys, additional treatment, taxes and backup supply. Thus the figures below are a **cost floor**, not a customer price.
- For an illustrative *drinking-only* reach proxy, divide dispensed volume by 2 L/person/day × 365 days = 730 L/person/year. This is neither a household count nor proof of safe consumption; cooking demand and unequal access reduce practical reach.
- An operating-day cap also applies when downtime occurs. Round annual exchange counts **up** to whole visits: ceiling(delivered L / 2,000 L). A calendar cap after commissioning and post-service test requirements may require extra visits or discards, increasing cost.

## One-kiosk scenarios (calculated, not measured)

| Operating fraction | Delivered L/year = 100 × 365 × fraction | Drinking-only reach proxy = L / 730 | Exchange visits = ceiling(L / 2,000) | Annual cost floor = 140 + 20 × visits + 120 | Cost floor / m³ |
| --- | ---: | ---: | ---: | ---: | ---: |
| 70% | 25,550 | 35 | 13 | US$520 | US$20.35 |
| 90% base | 32,850 | 45 | 17 | US$600 | US$18.26 |
| 100% upper duty | 36,500 | 50 | 19 | US$640 | US$17.53 |

The README's US$625/year and US$17.1/m³ at full duty are a **fractional annual accrual** (18.25 × US$20), rather than 19 indivisible service visits in the table. Neither includes the omitted costs. Real shutdown frequency, testing interval and staffing could dominate both estimates.

## Material balance and scale

At 100% duty, `(5 − 1) mg/L × 36,500 L = 146,000 mg = 146 g` fluoride captured per year per kiosk, **provided the tap really holds 1 mg/L**. At 90% duty the same calculation gives 131.4 g; at 70%, 102.2 g. This contaminant is transferred to cartridges and hub liquids, not destroyed. If *all* captured fluoride were recovered as pure CaF₂, the chemical minimum would be `146 g × 78.07 / (2 × 19.00) ≈ 300 g` dry CaF₂/year at full duty; real sludge, washwater and co-contaminants can greatly exceed it. No precipitation efficiency or disposal method is assumed: measure hub batches and use permitted handling.

At 10,000 installed and qualified kiosks, 90% operation implies `10,000 × 32,850 = 328.5 million L/year` of **potentially dispensed** water, up to 450,000 drinking-only reach equivalents if distributed evenly. At 100% duty the upper bounds are 365 million L/year and 500,000 equivalents. Neither number is a count of people with verified safe intake, a forecast of adoption, or a disease-reduction estimate. Record sampled compliant litres and actual usage before making impact claims.

## Sensitivity and comparison gate

If usable lead-bed capacity is only 0.5 mg/g, its nominal 6 g capacity cannot support the 8 g / 2,000 L plan. Keeping the original two-thirds utilization margin permits only 4 g or **1,000 L per exchange** at the same 4 mg/L removal assumption: at 90% operation, ceiling(32,850 / 1,000) = 33 visits and the modeled cost floor rises to `140 + 33 × 20 + 120 = US$920/year`, about US$28.0/m³. Validate this smaller limit with actual breakthrough tests or stop deployment; do not simply rely on the lag bed.

A fair comparison with a maintained reverse-osmosis unit, activated-alumina plant or safe alternative source requires the same source water, water-quality tests and accounting boundary: feed and compliant delivered litres, pump kWh, operator hours, reject or regenerant volume, residual disposal, outages and total local cost. No measured kiosk recovery, energy advantage or health effect exists yet. The WHO fluoride guideline and EPA activated-alumina guidance cited in the README are evidence about treatment context, **not** validation of these projections.
