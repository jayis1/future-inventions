# Maternity Gas-Loss Witness — Impact Analysis

**Author: jayis1** · Illustrative planning scenarios, not measured device performance or clinical outcomes.

## Boundary and evidence

The intervention targets nitrous oxide lost *before* clinical administration in facilities whose supply audits reveal avoidable losses. It cannot reduce exhaled gas by itself or measure worker exposure. A published UK/Ireland consensus discusses substantial pre-use loss in some piped settings [1], while a hospital reports savings after switching from a manifold to portable cylinders [2]; neither establishes a representative maternity-site baseline or this cart's incremental effectiveness. Exposure control still requires separate assessment and monitoring [3].

## Scenario model (one operating year after engineer-approved action)

Define `N` as qualifying facilities that complete an audit and a verified repair/supply change, `L` as measured avoidable pre-use N₂O loss per facility before action (kg/year), and `f` as the fraction of that loss actually eliminated after action. Gross annual avoided N₂O = `N × L × f / 1,000` tonnes/year. These are **independent hypothetical inputs**, not prevalence, forecast adoption or cart-attributable savings. The cart's *incremental* effect versus existing audits remains **unknown**; count only improvements above that comparator in a trial.

| Illustrative case | N (facilities) | L (kg N₂O/site/year) | f | Gross avoidance (tonnes N₂O/year) |
| --- | ---: | ---: | ---: | ---: |
| Low | 100 | 50 | 0.50 | 2.5 |
| Planning | 1,000 | 200 | 0.50 | 100 |
| High | 3,000 | 400 | 0.50 | 600 |

The planning row matches the README's **100 kg N₂O/year per qualifying facility** (`200 × 0.50`) and 100 tonnes/year for 1,000 such sites. No evidence shows that 1,000 sites qualify or that 50% is attainable. If verified pre-use loss is zero or repairs fail, avoided loss is zero. A 50-facility comparative trial is a *study-size proposal*, not the 1,000-site scenario.

## Sensitivity, attribution and cost

For an audited site with 200 kg/year measured avoidable pre-use loss, varying `f` from 0.25 to 0.75 changes gross avoidance from 50 to 150 kg N₂O/year. Multiply by the number of *verified eligible* sites only; differences in usage, exchanges, stock changes and reporting windows must be reconciled. In a matched before/after study, subtract the contemporaneous change at comparable unaffected sites and account for unrelated demand and supply changes. Report both the net gas mass balance and its measurement uncertainty; do not claim causality if the baseline or comparator is unreliable.

The README's **unquoted** cart planning cost is US$1,800 ex-workshop plus US$250/year service. At 100 investigations/year over five years, `(1,800 + 5 × 250) / (5 × 100) = US$6.10` per test for hardware and service allocation alone. It excludes qualified engineer time, certification, hospital shutdown, adapters, repair, transport, cylinder logistics and device manufacture/maintenance emissions. No site-level payback, net life-cycle climate saving or carbon-dioxide-equivalent value is asserted until these are measured and a disclosed conversion factor and year are chosen.

## Trial reporting gate

Publish baseline/after cylinder masses and uncertainty, stock changes, clinical-use accounting method, approved repair records, test completion, misses and false calls against independent engineer findings, downtime and safety incidents. Compare with ordinary maintenance and with simpler supply redesign. An occupational-health benefit needs separate representative exposure monitoring and competent interpretation [3]; no avoided mortality or improved analgesia is inferred.

## Sources

1. UK/Ireland consensus on piped nitrous-oxide decommissioning (existing README source): https://eprints.lancs.ac.uk/id/eprint/223580/1/Consensus_on_decommissioning_piped_nitrous_oxide_from_UK_and_Ireland_operating_theatre_suites-_Accepted_Version.pdf
2. Oxford University Hospitals, "From pipes to cylinders" (8 July 2024): https://www.ouh.nhs.uk/news/articles/2097/
3. UK Health and Safety Executive, "Using nitrous oxide (gas and air) safely in maternity units": https://www.hse.gov.uk/healthservices/using-nitrous-oxide-safely.htm
