# PPD-Free Tread Laminate — Impact Analysis

**Author: jayis1**

**Status:** illustrative scenario arithmetic, not measured emissions, exposure, ecological benefit, or an actual fleet forecast. The [blueprint](README.md) sets independent road-safety and toxicity gates; the [roadmap](ROADMAP.md) delays deployment until they pass.

## Functional unit and comparator

One tire-kilometre on an approved, matched retread of the same casing class, load, inflation, route and service conditions. The counterfactual is the same fleet using conventional 6PPD-containing retreads. Count *tire-wide* 6PPD-quinone recovered from debris plus standardized runoff, not just the new cap. Separately count total tire wear mass, fuel/energy, cap production, casing retirement and disposal; do not add the chemical mass to the wear mass a second time.

## Explicit, unmeasured scenario inputs

| Input | Low | Base | High | Status |
| --- | ---: | ---: | ---: | --- |
| Annual retread demand in hypothetical fleet | 100,000 | 100,000 | 100,000 | Assumption, not a national/global figure |
| Candidate share of that demand | 10% | 50% | 90% | Adoption assumptions; not a forecast |
| Tire distance per service life | 50,000 km | 50,000 km | 50,000 km | Assumed equal life initially; verify on road |
| Comparator tire-wide 6PPD-quinone recovered | 0.02 mg/tire-km | 0.02 | 0.02 | **Synthetic placeholder**, not published concentration |
| Candidate tire-wide reduction | 50% | 90% | 95% | Scenario hypotheses; 90% is README's provisional gate |
| Comparator tread wear | 40 mg/tire-km | 40 | 40 | **Synthetic placeholder**; tire wear varies by route |
| Candidate wear multiplier | 1.10 | 1.00 | 0.90 | Scenarios; 1.10 is the provisional maximum extra wear |

Sources for the *motivation and protocols*, not for any numeric placeholder here: EPA describes the 6PPD-quinone concern [1]; ISO 1431-1 specifies static/dynamic ozone tests [2] and ISO 4649 describes comparative drum abrasion while warning against inferring service performance [3]. Replace every placeholder with paired field measurements before claiming an avoided mass.

## Transparent calculations

Candidate distance = 100,000 retreads × adoption share × 50,000 km/retread: **0.5 / 2.5 / 4.5 billion tire-km/year** (low/base/high). Comparator 6PPD-quinone over those same kilometres = distance × 0.02 mg/km ÷ 1,000,000 mg/kg = **10 / 50 / 90 kg/year**. Modeled reduction = baseline × hypothesized reduction fraction = **5 / 45 / 85.5 kg/year**; candidate remainder = **5 / 5 / 4.5 kg/year**. None is an observed environmental reduction: road background, uncollected particles, sidewalls and casing chemistry can move the result.

Comparator wear over adopted distance = distance × 40 mg/km ÷ 1,000,000,000 mg/tonne = **20 / 100 / 180 tonnes/year**. Candidate wear under each scenario is **22 / 100 / 162 tonnes/year**, a difference of **+2 / 0 / −18 tonnes/year** versus the *adopted-distance comparator*, not versus all roads. Wear-mass differences are not aquatic-toxicity differences. At the 100,000-cap/year planning volume, the README's ≤US$20 incremental manufacturing target implies at most **US$2 million/year** in additional cap materials/process cost if achieved, excluding casing, testing, labor, approval, logistics and disposal; it is not a saving.

## Sensitivity and break-even tests

If candidate service life is 10% shorter at fixed fleet distance, annual replacements rise by 1/0.9 ≈ **11.1%**; 100,000 baseline replacements would become about **111,111**. Production and scrap burdens may rise even if per-km chemical release falls. If tire-wide reduction is only 20% rather than the base 90%, the base adopted-distance estimate becomes **10 kg/year**, not 45 kg/year, and fails the research gate. If rolling resistance is up to the extra 5% research limit, test fuel/energy penalty on vehicles before asserting a net climate benefit. An 11.1% replacement increase would also make the base 50,000 candidate caps about 55,556 for the same distance; do not silently combine that penalty with the equal-life table.

No model here maps mg of 6PPD-quinone to stream concentration, fish survival, human health, carbon savings or global outcomes. Paired catchment sampling, exposure/response evidence, substitute-transformation-product screening, bioassays and full lifecycle inventories are required. Failure on wet grip, structural integrity, total hazard or approval is a no-go regardless of a favorable modeled reduction.

## Sources

[1] https://www.epa.gov/chemical-research/6ppd-quinone
[2] https://www.iso.org/standard/86601.html
[3] https://www.iso.org/standard/86603.html
