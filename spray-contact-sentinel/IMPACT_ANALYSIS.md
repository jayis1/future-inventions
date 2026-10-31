# Spray Contact Sentinel — Impact Analysis

**Author: jayis1** · Illustrative one-year deployment scenarios, not a forecast or measured health impact. Only independently validated formulation/working-dilution combinations qualify. The coupon samples outside-cuff deposition, not absorbed dose.

## Assumptions (all hypothetical except the README's unquoted cost goal)

| Input | Scenario assumption | Meaning / uncertainty |
|---|---:|---|
| Eligible workers | 10,000 | Illustrative cohort, not an estimate of the addressable market |
| Eligible shifts per worker per year | 100 | Each used shift needs one disposable set |
| Set uptake, low / base / high | 20% / 50% / 80% | Fraction of eligible shifts equipped and used correctly |
| Valid-read fraction | 90% | Assumed after exclusion of expired, leaked and failed-control sets; untested |
| Collector challenge prevalence | 5% of valid reads | Assumed prevalence of a prespecified detectable deposit, not poisoning |
| Alert sensitivity among valid challenge reads | 95% | Exploratory scenario assumption, **not** the README's alert-or-invalid validation target or demonstrated performance |
| False-alert fraction among valid clean reads | 10% | Exploratory worst-side design scenario, not demonstrated specificity |
| Disposable ex-factory price | US$3.50/set | Unquoted target at 100,000 sets/year by 2038; volume and year differ across scenarios |
| Reusable holder | US$4/worker | Unquoted ex-factory goal; assume one per participating worker |

## Arithmetic and scenarios

Equipped shifts = 10,000 workers × 100 eligible shifts × uptake. Valid reads = equipped shifts × 0.90; invalid reads = remainder. True challenge reads = valid reads × 0.05. Illustrative challenge alerts = true challenge reads × 0.95; nuisance alerts = valid clean reads × 0.10. Disposable cost = equipped shifts × US$3.50. Rounded counts are expectation values, not promises.

| Scenario | Equipped shifts | Valid / invalid reads | Challenge alerts | Nuisance alerts | Disposable ex-factory cost |
|---|---:|---:|---:|---:|---:|
| Low, 20% uptake | 200,000 | 180,000 / 20,000 | 8,550 | 17,100 | US$700,000 |
| Base, 50% uptake | 500,000 | 450,000 / 50,000 | 21,375 | 42,750 | US$1,750,000 |
| High, 80% uptake | 800,000 | 720,000 / 80,000 | 34,200 | 68,400 | US$2,800,000 |

At 100 sets per worker-season, disposable cost is US$350/fully equipped worker-season, plus a US$4 holder if needed. In the base scenario, average disposable spend across the 10,000-worker cohort is US$175/worker-year; this is **not** cost per poisoning prevented. Holder spend could be as high as US$40,000 if all 10,000 need a new holder. Training, shipping, formulation-specific calibration, quality assurance, failed-set replacements, PPE, medical surveillance and compliant disposal add unknown costs; no total delivered cost can yet be quoted.

## Interpretation and stop conditions

Even under these assumptions, nuisance alerts outnumber challenge alerts; tighter specificity, worker training or different prevalence would substantially change the burden. An invalid read cannot be counted as a successful detection. Read validity and sensitivity may correlate with heat, formulation and worker practice, so multiplying independent rates is a simplifying assumption to test. A coupon may miss deposition elsewhere, and external residue does not measure absorbed dose. No reduction in pesticide exposure, illness, or poisoning has been demonstrated; avoided cases and cost per avoided case are **unknown**, not zero. A controlled field study with independent exposure and health outcomes is required before estimating those benefits. Monitor whether the program displaces substitution, engineering controls, PPE or access to clinical care, and halt deployment if it does.

The cohort is a hypothetical deployment denominator, not derived from global poisoning estimates; no global extrapolation, carbon claim or multiple-beneficiary counting is justified. Used sets require locally compliant pesticide-waste handling, and their material/waste footprint has not been measured.
