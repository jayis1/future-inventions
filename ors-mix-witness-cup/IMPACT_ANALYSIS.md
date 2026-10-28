# ORS Mix-Witness Cup — Impact Analysis

**Author: jayis1.** Illustrative one-year *preparation-workflow* scenario, not a forecast, trial result, or estimate of lives saved. The comparator is the same labeled ORS sachet prepared with suitable water in a marked one-litre vessel **without** the reader. WHO identifies ORS made with clean water as a treatment for diarrhoeal dehydration; a screening attempt is not a patient treated.[1] Product composition and mixing volume depend on the actual packet; the UNICEF example is a one-litre sachet.[2]

## Model assumptions (all hypothetical except the linked existing factory target)

| Input | Low | Base | High | Boundary |
| --- | ---: | ---: | ---: | --- |
| Readers supplied | 1,000 | 10,000 | 30,000 | Planning volumes, not adoption estimates |
| Attempted preparations/reader/year when operating | 100 | 200 | 250 | One reader may screen many batches; not unique people |
| Fraction of planned preparations actually screened | 60% | 80% | 90% | Accounts jointly for use and uptime; measure in pilot |
| Baseline erroneous preparations among screened attempts | 5% | 10% | 20% | Unknown; illustrative sensitivity input, not published prevalence |
| Fraction of erroneous preparations flagged | 50% | 70% | 90% | Hypothetical field sensitivity, not the bench gate |
| Fraction of flagged erroneous batches correctly remade | 50% | 70% | 80% | Must observe actual response; no treatment delay assumed here |
| Factory cost/reader | $24 | $24 | $24 | Unvalidated 2038 target from README at 100,000/year, not a quote at these volumes |
| Service life / initial distribution / annual maintenance | 5 years / $8 / $5 | Same | Same | Hypothetical accounting inputs; ORS, water, clinical care and staff labor excluded |

Attempts = readers × preparations/reader × screened fraction. Baseline errors = attempts × assumed error prevalence. Errors flagged = baseline errors × hypothetical sensitivity. **Potential corrections** = flagged errors × successful-remake fraction; these are not verified correct ORS batches, since a remake itself needs checking. Annualized program cost = readers × ($24/5 + $8/5 + $5) = readers × $11.40/year, assuming full service life with no financing cost or replacements.

## One-year conditional outputs

| Quantity | Low | Base | High |
| --- | ---: | ---: | ---: |
| Screening attempts | 60,000 | 1,600,000 | 6,750,000 |
| Baseline errors among those attempts (modeled) | 3,000 | 160,000 | 1,350,000 |
| Erroneous batches flagged (modeled) | 1,500 | 112,000 | 1,215,000 |
| Potential successful remakes (modeled upper bound) | 750 | 78,400 | 972,000 |
| Annualized factory + distribution + maintenance cost | $11,400 | $114,000 | $342,000 |
| Cost/screening attempt, excluding staff and ORS | $0.190 | $0.07125 | $0.05067 |

The base case's 1.6 million attempts are **less** than the README's maximum 2 million annual attempts for 10,000 readers at 200 uses each because this model applies 80% effective screening. A lower-volume deployment would not necessarily achieve the assumed $24 factory price. Counting corrected batches as averted dehydration, deaths or treatment savings is unsupported; no health benefit is claimed. Incorrect packets that falsely pass, ambiguous results, time spent checking, cleaning failures and patients who never receive ORS could reverse any expected gain.

## Sensitivity, costs and falsification

Error prevalence and the probability of a flagged batch actually being remade dominate the potential-corrections result; true field sensitivity and false-pass risk matter at least as much for safety. At 0% added effectiveness over the marked-vessel baseline, incremental corrected batches are zero regardless of deployment. An honest evaluation needs paired observations of batch composition against laboratory assays, actual remediation, dosing delays, false reassurance, patient access and adverse events, with uncertainty intervals and an independently specified stop rule.

The $11.40/reader-year arithmetic excludes batteries beyond initial supply, labor, wet calibration, travel, replacement cups at the README's unvalidated $3 target, lost units, regulatory review and disposal; report these separately before procurement. The assumed five-year life means a steady-state program replaces approximately one-fifth of readers annually *if* survival is five years; failure increases material flow. The 2 mL aliquot is discarded per attempt: modeled sample waste is 120 / 3,200 / 13,500 litres per year in low / base / high cases, plus cleaning water, whose quantity is unknown. That volume does not equal the volume of ORS delivered.

A pilot showing no lower rate of laboratory-confirmed preparation errors, excess false passes, more delay to first dose, or worse access than a well-marked vessel falsifies the case for scaling this reader. See [README.md](README.md) for the sensing limits and [ROADMAP.md](ROADMAP.md) for decision gates.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/diarrhoeal-disease
[2] https://supply.unicef.org/s1561133.html
