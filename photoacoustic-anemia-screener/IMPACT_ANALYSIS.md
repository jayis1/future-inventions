# Impact Analysis — Photoacoustic Anemia Screener

**Author: jayis1. Conditional arithmetic, not measured performance, a forecast, or a clinical recommendation.** See [README.md](./README.md) and [SPECIFICATION.md](./SPECIFICATION.md). No device has passed its clinical gates.

## Scope and baselines

The intended first model population is *encounters with women aged 15–49*; it does not extrapolate these results to pregnancy, children, neonates or all residents. WHO reports an estimated **30% anemia prevalence** in women aged 15–49 globally; actual site-specific prevalence and care access will differ ([WHO Anaemia fact sheet](https://www.who.int/news-room/fact-sheets/detail/anaemia)). A venous CBC during the same visit is the study reference. The hypothetical counterfactual below is **one blood-based screen per encounter**, not the likely status quo in every outreach setting. Repeated encounters may involve the same person.

## Explicit assumptions (not observed)

- Annual devices: low 1,000; base 10,000; high 100,000. Every device attempts **400 screens/year**; downtime and missed appointments are implicitly included in that utilization, not independently estimated. These are adoption scenarios, not predicted shipments.
- All three scenarios assume 30% prevalence among valid encounters; 10% invalid attempts; **90% sensitivity and 80% specificity** on valid attempts, *only if* the preregistered clinical gates are met in every intended group. Invalid attempts are never counted negative.
- All invalid attempts receive a blood test in this *idealized workflow*; flagged-result blood-test completion is 50% / 70% / 90% (low/base/high). In practice missed follow-up is a safety problem, not a feature. Symptoms and clinician-directed tests add draws beyond this model.
- For cost arithmetic only: US$120 capital with a five-year life and US$20/year service at the **100,000-unit/year manufacturing target**; 400 attempts/device/year makes `($120 + 5 × $20) / (5 × 400) = $0.11/attempt`. Applying this same high-volume price at 1,000/10,000 devices is an optimistic simplifying assumption, not a quote. An *illustrative*, unsourced US$1/blood test includes neither analyzer, labor, training, disposal nor transport and must be replaced with local procurement data. No clinical savings are asserted.

## Equations and modeled outputs (annual)

`attempts = devices × 400`; `valid = attempts × 0.90`; `true flags = valid × 0.30 × 0.90`; `false flags = valid × 0.70 × (1 − 0.80)`; `completed blood tests = (true flags + false flags) × follow-up + invalid attempts`; `confirmed cases from valid positive screens = true flags × follow-up`, assuming a perfect confirmatory blood test for arithmetic only. `Draws avoided = attempts − completed blood tests` relative to universal blood testing. Dollar totals are `attempts × $0.11 + completed blood tests × $1`, divided by confirmed cases for modeled dollars/confirmed case; these are **not** incremental programme costs or cost-effectiveness estimates.

| Model output per year | Low | Base | High |
| --- | ---: | ---: | ---: |
| Attempted screening encounters | 400,000 | 4,000,000 | 40,000,000 |
| Valid encounters | 360,000 | 3,600,000 | 36,000,000 |
| True flags / false flags | 97,200 / 50,400 | 972,000 / 504,000 | 9,720,000 / 5,040,000 |
| Confirmed cases from valid flags (modeled) | 48,600 | 680,400 | 8,748,000 |
| Completed confirmatory draws incl. invalids | 113,800 | 1,433,200 | 17,284,000 |
| Blood draws avoided vs universal testing | 286,200 | 2,566,800 | 22,716,000 |
| Valid-encounter anemia cases missed by screen before follow-up losses | 10,800 | 108,000 | 1,080,000 |
| Screening + illustrative blood-test expense | $157,800 | $1,873,200 | $21,684,000 |
| Illustrative dollars per confirmed case from valid flag | $3.25 | $2.75 | $2.48 |

**Interpretation:** missed cases and incomplete referrals are large even when optimistic gates are met. These are screening encounters, not distinct people or additional cases found *versus current practice*; the model says nothing about treatment uptake, lives saved, anemia prevalence reduction, or disability-adjusted life years. Avoided draws are conditional on valid classification and a universal-blood-test comparator, and do not imply that blood testing can safely be withheld. Incorrect no-flags, symptomatic cases and clinical judgment may require more confirmatory draws than modeled. Estimate added case detection and clinical benefit only after measuring baseline coverage, downstream care and outcomes in a controlled field evaluation.
