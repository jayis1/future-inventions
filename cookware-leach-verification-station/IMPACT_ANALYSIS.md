# Cookware Leach Verification Station — Impact Analysis

**Author: jayis1. Status: illustrative annual deployment model, not measured health impact or a prediction.** The station is an unvalidated lead-only screening concept. A negative result applies only to the tested pot and exposure protocol; laboratory confirmation and actual replacement, not test count, determine potential benefit. See the [README](README.md) for methods and sources.

## Model and inputs

One screen means one cookware item receiving the full 15-minute simmer plus 24-hour standing challenge and QC. Assume one distinct pot per screen, no repeated tests, and sufficient trained staff, safe waste collection and replacement stock; reality will lower throughput. All fractions below are scenario assumptions, **not prevalence estimates** from the published, nonrepresentative sample in README source [2].

| Variable | Low | Base | High | Basis |
| --- | ---: | ---: | ---: | --- |
| Deployed stations | 25 | 100 | 500 | Assumed funded fleet; base matches README illustration |
| Screens/station/year | 500 | 1,000 | 1,200 | Assumed throughput with an overnight dwell; requires multiple pot positions |
| Confirmed leaching pots/screens | 4% | 8% | 12% | Assumed *after* laboratory adjudication; depends on targeted sampling and local rule |
| Confirmed-pot replacement uptake | 40% | 60% | 80% | Assumed observed exchange fraction, not guaranteed prevention |
| Field operating cost/screen | US$8 | US$5 | US$4 | Assumed all-in field labor, consumables, heat and waste; supersedes README's narrower US$1.20 consumables goal |
| Fraction referred to laboratory | 10% | 15% | 20% | Assumed flagged, inconclusive and audit samples combined |
| Laboratory charge/referral | US$50 | US$50 | US$50 | Illustrative planning quote **assumption**, not a published market benchmark |
| Replacement cost/pot | US$25 | US$25 | US$25 | Assumed delivered safe alternative; suitability and supply require verification |
| Hardware | US$280/unit over 5 years | same | same | Unvalidated 2038 volume-production goal in README; no financing or discounting |

Equations: screens = stations × screens/station/year; confirmed = screens × confirmed fraction; replaced = confirmed × uptake. Annual modeled cost = screens × (field cost + laboratory referral fraction × US$50) + replaced × US$25 + stations × US$280/5. Dollars are illustrative planning dollars; the hardware/consumables targets are stated as 2038 US-dollar goals in the README, whereas service prices here are assumed constant planning dollars. This mixed-year model is **not** a valid inflation-adjusted budget; convert all inputs to one price year before investment decisions.

## Annual scenario outputs

| Outcome | Low | Base | High |
| --- | ---: | ---: | ---: |
| Screens | 12,500 | 100,000 | 600,000 |
| Lab-confirmed leaching pots | 500 | 8,000 | 72,000 |
| Confirmed pots replaced | 200 | 4,800 | 57,600 |
| Laboratory referrals | 1,250 | 15,000 | 120,000 |
| Modeled annual program cost | US$168,900 | US$1,375,600 | US$9,868,000 |
| Program cost / confirmed pot replaced | US$844.50 | US$286.58 | US$171.32 |

These are **pots**, not people protected. For an illustrative exposure upper bound only, if each replaced pot otherwise served one distinct household, the number of households with a potential source removed cannot exceed the replaced-pot row; it could be much lower if other pots or sources dominate. Children protected, blood-lead change and disability-adjusted life-years averted are **not estimated**: they require household overlap, use frequency, baseline dietary lead intake, source attribution, biomonitoring and a defensible causal comparator. No cost-per-DALY claim is possible from screen counts alone. Relative to sending all screened pots to a laboratory at the **assumed** US$50 charge, laboratory fees alone would be US$625,000 / US$5,000,000 / US$30,000,000 respectively; this is not a like-for-like economic comparison because full-vessel extraction, transport, sensitivity and follow-up differ, and the station's costs exclude accreditation and central overhead.

## Sensitivity and decision rule

At fixed 100,000 base screens and 8% lab-confirmed positives, lowering uptake from 60% to 40% yields **3,200** replaced pots; raising it to 80% yields **6,400**. This change does not demonstrate an exposure effect. Conversely, a field false negative can leave a genuinely leaching pot in use: publish blinded sensitivity with uncertainty bounds and invalid rates against matched ICP-MS extracts before using any negative for triage. If the full-method reporting limit cannot support the provisional 5 µg/L research threshold, return *inconclusive* and use the accredited laboratory route. A suspected FDA-listed product is not retested into service [README source 3].

For a defensible outcome evaluation, record anonymous pot-level disposition and a consented, ethics-reviewed household exposure study with a comparison group; publish attrition and the fraction of dietary lead plausibly attributable to cookware. Repeated use, lead from other sources, selection bias, sensor drift, replacement affordability, chemical waste and local regulatory decisions can all reverse the modeled benefit. The 2020 global childhood lead-exposure estimate in README source [1] is **not** a cookware-attributable denominator.
