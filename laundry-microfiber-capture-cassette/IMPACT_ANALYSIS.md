# Impact Analysis — Laundry Microfiber Capture Cassette

**Author:** jayis1
**Status:** illustrative scenarios only; no cassette prototype or field measurements. This is source-side wastewater diversion into managed solid waste, not plastic destruction or proven ocean-pollution reduction.

## Evidence and boundaries

Napper et al. reported 0.44 ± 0.04 g of **all** microfibers per mixed control wash, with devices reducing release by 21–78% in their detergent-free 30 °C laboratory protocol [1]. That study's 0.44 g is not a household average or an observed mass of synthetic fibers ≥100 µm long. A published 78 ± 5% XFiltra result used a powered 60 µm system [1], not this passive cassette. The model below borrows 0.44 g/wash solely as a scale illustration, then assumes an eligible synthetic/length fraction; neither the fraction nor the cassette's 70% efficiency is measured. Independent household sampling must replace them before investment or policy use.

## Reproducible model

Let W = washes per participating household-year; B = 0.44 g all fibers/wash (illustrative literature value); F = share of mass that is synthetic and ≥100 µm; C = ideal capture fraction of that eligible mass (0.70 unverified design target); U = fraction of cycles with compliant service/operational uptime; R = fraction of those cycles not lost to bypass/leakage; D = fraction of captured mass retained through handling and disposal rather than returned to wastewater or escaped. Treat factors as independent for illustration only; a field trial must use directly observed joint behavior.

Eligible baseline = W × B × F (g/household-year). Ideal eligible capture = eligible baseline × C. Modeled managed-waste retention = ideal eligible capture × U × R × D. For N participating households, metric tonnes/year = modeled g/household-year × N ÷ 1,000,000. If adoption is specified instead, N = eligible households × adoption fraction; do not count the same home twice. A bypassed wash has zero credited capture even if its 200 µm relief screen retains some lint.

| Assumption / modeled result | Conservative | Central | Optimistic |
|---|---:|---:|---:|
| W (washes/household-year; assumed) | 150 | 200 | 250 |
| F (eligible mass fraction; assumed) | 0.50 | 0.70 | 0.80 |
| C (eligible mass capture; target, not measured) | 0.70 | 0.70 | 0.70 |
| U (service/uptime fraction; assumed) | 0.75 | 0.90 | 0.95 |
| R (no-bypass/leak fraction; assumed) | 0.90 | 0.95 | 0.99 |
| D (retained during handling/disposal; assumed) | 0.80 | 0.90 | 0.95 |
| Eligible baseline (g/household-year) | 33.0 | 61.6 | 88.0 |
| Ideal eligible capture (g/household-year) | 23.1 | 43.1 | 61.6 |
| Modeled retained (g/household-year) | 12.5 | 33.2 | 55.0 |
| Modeled retained at N = 100,000 participating homes (tonnes/year) | 1.25 | 3.32 | 5.50 |

The existing [README](README.md) shows 61.6 g/household-year and 6.16 tonnes/100,000 homes by multiplying all-fiber B directly by 200 washes and 70% capture; those are **upper-bound arithmetic illustrations before eligible-fiber fraction, downtime, bypass and disposal losses**, not forecasts. The more constrained central scenario above gives 33.2 g and 3.32 tonnes of managed-waste retention. These scenarios are sensitivity examples, not statistical confidence intervals.

## What counts as benefit

Captured material in a pouch is not automatically material kept out of nature. In sewered areas, conventional wastewater treatment may already intercept some fibers into sludge; net avoided environmental release requires comparing the cassette-plus-disposal pathway with that local baseline, including downstream sludge fate. In unsewered areas, the baseline may differ, but safe drain installation still governs eligibility. No claim is made for nanoplastics, airborne fibers, carbon savings, human-health outcomes or marine stock reduction.

Before scaling, weigh incoming and discharged fibers by polymer/length with blanks, measure service and relief frequencies in an intention-to-treat home trial, track pouch fate, and compare an existing filter under matched conditions. Separately account for polypropylene housing, stainless screens, EPDM seals, pouch production, transport, cleaning labor, replacement and end-of-life leakage in a lifecycle assessment. A positive net outcome has not been demonstrated.

## Reference

1. Napper et al., “The efficiency of devices intended to reduce microfibre release during clothes washing,” *Science of the Total Environment* (2020). https://doi.org/10.1016/j.scitotenv.2020.140412
