# Locally Repairable Terrain Wheelchair — Impact Analysis

**Author: jayis1**
**Status:** Illustrative planning model, not a measured impact study or clinical claim. See [README.md](README.md) for the design and its safety gates.

## Boundary and assumptions

Model one annual procurement cohort at hypothetical regional scale; count only individually fitted users who retain an appropriate chair. Do not extrapolate to WHO's estimated 80 million people needing a wheelchair: need is not reachable demand.[1] No reduction in falls, pressure injuries, emissions, employment barriers or poverty is assumed. Before any pilot, service teams must define local demand, the availability of an appropriate comparator, and ethics and regulatory requirements.

- Hardware target: **$220 delivered per chair**, comprising $180 ex-workshop and $40 distribution/margin allowance; this is an unquoted planning target from the README, not a market price.
- Added service allowance for this model: **$100 per delivered chair** for initial assessment, fitting and training; arbitrary illustrative budget, not a clinical cost quote or a limit on needed care.
- Routine parts and service: **$18 per chair per year**, including the in-service years considered here. This optimistic hypothesis requires field validation; nonroutine failures and user travel are excluded.
- Retention fraction is the share of delivered chairs that are fitted, accepted and continue to meet users' needs over the modeled life. All failures are conservatively counted as zero user-years, despite possible partial service.
- Modeled life is **2–4 years** for sensitivity, not a demonstrated durability figure. Procurement runs only once in this model; annual cohorts cannot be added without adjusting for overlapping users and replacements.

## Scenarios for a single procurement cohort

| Case | Delivered chairs | Retention assumption | Modeled years | Retained users | Retained user-years | Cohort spend (USD) | USD per retained user-year |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Conservative | 1,000 | 60% | 2 | 600 | 1,200 | 356,000 | 296.67 |
| Base | 5,000 | 75% | 3 | 3,750 | 11,250 | 1,870,000 | 166.22 |
| Ambitious | 10,000 | 85% | 4 | 8,500 | 34,000 | 3,920,000 | 115.29 |

Arithmetic: retained users = delivered × retention; retained user-years = retained users × modeled years; cohort spend = delivered × ($220 + $100 + $18 × modeled years); cost per retained user-year = spend / retained user-years. For the base case, 5,000 × 0.75 × 3 = 11,250 user-years and 5,000 × ($320 + $54) = $1,870,000. These figures are service-capacity scenarios, not unique lifetime beneficiaries or incremental outcomes against a comparator. The original README's $310 five-year hardware-plus-routine-service target excludes this $100 service allowance and is not directly comparable.

## Decision sensitivity and missing evidence

At fixed delivered volume and service life, a lower retention rate raises spending per useful year in inverse proportion. At fixed volume and retention, a shorter service life raises it because initial hardware/fitting costs are spread across fewer years. The pilot must measure retention and abandonment with reasons, independently verified repairs and downtime, actual fitting/cushion costs, and safety events. It must compare against an appropriately fitted locally available wheelchair with equal service support; only a randomized or otherwise credible comparison could attribute mobility or health changes to this design.

Excluded costs include complex cushions and postural support beyond the allowances, clinician follow-up beyond initial service, emergency replacement, taxes, finance, adverse-event response, local travel, and site-specific freight above the $40 allowance. If fitting or parts cost more, revise the model rather than rationing them. No CO2 or avoided-replacement estimate is credible without material mass, a verified service life and a matched comparator. Qualified local production might create repair work, but job counts and net economic benefits require a local labor survey.

## Source

[1] WHO, 2023 wheelchair provision guidelines announcement: https://www.who.int/news/item/05-06-2023-who-releases-new-wheelchair-provision-guidelines
