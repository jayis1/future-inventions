# Mill-Gate Maize Sorter — Illustrative Impact Analysis

**Author: jayis1. Status: scenario model, not measured performance, regulatory approval, or a health forecast.** The research concept and its limitations are in [README.md](README.md); validation gates are in [ROADMAP.md](ROADMAP.md). Units and arithmetic below are explicit so the scenario can be replaced with pilot observations.

## Assumptions and boundary

| Variable | Low utilization | Base | High utilization | Basis |
| --- | ---: | ---: | ---: | --- |
| Units installed and operating | 100 | 100 | 100 | Illustrative adoption cohort, not a market forecast. |
| Running days/year per unit | 150 | 200 | 250 | Scenario only; excludes unavailable days. |
| Running hours/day per unit | 2 | 4 | 6 | Scenario only; continuous feed at design rate while running. |
| Input rate | 20 kg/h | 20 kg/h | 20 kg/h | Unvalidated dry-whole-maize design target, not measured throughput. |
| All-kernel held fraction by mass | 5% | 5% | 5% | **Separate assumption** from the README's ≤5% *sound-kernel* false-rejection target; actual hold fraction may be much larger. |
| Aflatoxin mass removed | 50% | 50% | 50% | Conditional design target for matched lots, **not** an observed or assured effect. |
| Device power while running | 15 W | 15 W | 15 W | Upper design target; excludes shared supply losses and laboratory work. |
| Factory device price / service life | $280 / 5 yr | $280 / 5 yr | $280 / 5 yr | Unvalidated 2038 ex-factory target, straight-line capital accounting. |
| Annual gate/LED maintenance | $20/unit | $20/unit | $20/unit | Budget estimate; excludes labor and other repairs. |

The 100 operating units are assumed deployed with working custody and sampling protocols. This does **not** imply 100% uptime, adoption among eligible mills, compliant food, or an improvement in individual exposure. The low/high cases vary utilization only, not efficacy; true safety uncertainty is substantially wider.

## Reproducible annual arithmetic

- Input tonnes = units × days × hours × 20 kg/h ÷ 1,000: **600 / 1,600 / 3,000 t** (low/base/high). Per base-case unit this is **16 t/year**.
- Held grain = input × assumed 0.05: **30 / 80 / 150 t**. Accepted mass before any assay-based quarantine = input × 0.95: **570 / 1,520 / 2,850 t**. These are flows, **not** tonnes proven compliant.
- If, and only if, the 50% toxin-mass removal target holds in a matched lot with 5% grain held, accepted-grain toxin *concentration* relative to input is (1 − 0.50) ÷ (1 − 0.05) = **0.526**, or about **47.4% lower**. This is conditional arithmetic, not a prediction of which lots will meet a legal limit; toxin heterogeneity and sampling error matter.[1][2]
- Fleet device energy = units × days × hours × 15 W ÷ 1,000: **450 / 1,200 / 2,250 kWh/year**, or **0.75 kWh/t** while the device actually runs at 20 kg/h and 15 W. Upstream supply losses, tests and disposal are omitted.
- Annualized factory capital plus specified maintenance = 100 × ($280 ÷ 5 + $20) = **$7,600/year**. Divide by input tonnes: **$12.67 / $4.75 / $2.53 per tonne**. This is a *floor-like partial device cost*, not the delivered sorting price. It omits financing, installation, power, operator time, quality assays, calibration, cleaning, custody, lost good grain, repairs beyond the budget, taxes and safe disposal; any can dominate the subtotal.

## Sensitivity, outcomes, and decision gate

If **30% of eligible grain bypasses** a base-case fleet while scheduled machine hours otherwise remain available, actual processed input falls from 1,600 to **1,120 t/year**; at the same 5% hold assumption, **56 t** are held and **1,064 t** enter the accepted stream before assays. Device capital and maintenance remain $7,600, raising that partial cost to approximately **$6.79/t processed**; electricity depends on actual running time. If bypass instead frees capacity for other households, this volume loss need not occur—measure queueing and use rather than assuming either outcome.

The **direct measurable outcomes** are input and hold mass, independently sampled toxin concentrations and mass balance, lot-limit failures, fault-driven diversion, uptime and total cost. The comparison must include no sorting and manual sorting on matched naturally contaminated lots. A toxin score or removed mass cannot be turned into avoided disease, DALYs, lives saved, revenue premiums or compliant tonnage without exposure data, a suitable dose-response model, actual market prices and representative assays. No such benefits are counted here. Lots that fail local food limits remain quarantined regardless of an apparent optical improvement; rejected kernels do not automatically become feed. If confidence intervals, false-acceptance lots, reject custody or total economics fail the pilot gates, stop deployment rather than extrapolating this scenario.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/mycotoxins — WHO, *Mycotoxins* (2023), contamination and health context.
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC10058786/ — Yao et al., *Toxins* (2023), portable fluorescence-assisted maize sorting; results are not transferable without testing.
