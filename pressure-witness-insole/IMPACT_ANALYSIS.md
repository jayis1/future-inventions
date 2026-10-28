# Pressure-Witness Insole — Impact Analysis

**Author: jayis1.** Illustrative one-year program arithmetic, not a forecast or measured clinical effect. Functional unit: one fitted pair worn during one person-year in addition to prescribed footwear and daily foot checks. The relevant comparison is standard footwear care *without* this extra layer, not no care. Only people who have access to trained fitting and follow-up are in scope.

## Assumptions

| Input | Low | Base | High | Meaning |
| --- | ---: | ---: | ---: | --- |
| Pairs issued in one year | 10,000 | 50,000 | 100,000 | Hypothetical deployment, not market size |
| Fraction worn and checked as intended for a year | 50% | 70% | 90% | Hypothetical effective coverage; reality requires observed adherence |
| Annual ulcer probability with standard care in this illustrative cohort | 4% | 4% | 4% | **Assumed solely for sensitivity**; not an epidemiologic estimate |
| Relative change in ulcer risk from adding the witness | 0% | 5% | 10% | **Entirely unproven**; the real effect may be negative (harm) |
| Factory cost per pair | $12 | $12 | $12 | README's unvalidated 2038 target at 100,000 pairs/year; lower volumes may cost more |
| Inspection and replacement | Quarterly inspection; one-year nominal life | Same | Same | Worker time, replacement on wear and travel excluded from factory cost |

Effective wearer-years = issued pairs × adherence. Standard-care comparator cases among effective wearers = wearer-years × assumed 4% annual probability. *Conditional* cases avoided = comparator cases × hypothetical relative change; these figures are neither trial results nor a substitute for a properly powered study. An insert that increases risk by 5% relative would instead add 10 / 70 / 180 expected ulcers across low / base / high effective cohorts (4% × wearer-years × 5%). These illustrative rates should be replaced with local, ethically collected trial estimates before procurement decisions.

## One-year modeled outputs

| Quantity | Low | Base | High |
| --- | ---: | ---: | ---: |
| Effective wearer-years (pairs × adherence) | 5,000 | 35,000 | 90,000 |
| Standard-care comparator cases (wearer-years × 4%) | 200 | 1,400 | 3,600 |
| Conditional avoided cases (comparator × assumed relative reduction) | 0 | 70 | 360 |
| Factory-only expenditure (pairs × $12) | $120,000 | $600,000 | $1,200,000 |
| Factory cost per effective wearer-year | $24.00 | $17.14 | $13.33 |

The high column is a **sensitivity ceiling**, not a prediction; a 0% effect means no avoided ulcers at any deployment volume. The device is a passive event record at four to six sites: even perfect adherence would not capture off-site loading, shear or tissue changes. A clinical comparison must measure adherence, pressure redistribution, missed events, adverse skin outcomes, false reassurance, completed referrals and ulcer incidence, reporting uncertainty and negative effects. Do not convert modeled ulcers into amputations avoided or dollar savings.

## Full-cost and environmental boundaries

The $12 ex-factory target excludes the validated in-shoe mapping used at fitting, clinical and footwear-worker time, training, travel, quarterly inspections, replacement of failed inserts, follow-up, regulatory work and disposal. At one nominal pair per year the material flow is at least 10,000 / 50,000 / 100,000 pairs per year in the three scenarios, plus early failures; mass and recycling yield are not known. If each failed insert requires an additional pair, material and factory costs increase by $12 per replacement before logistics. A true cost-effectiveness and lifecycle comparison must count these inputs and any changes to standard care rather than attributing all clinical change to the insert. See [ROADMAP.md](ROADMAP.md) for test gates and [README.md](README.md) for mechanism and limitations.