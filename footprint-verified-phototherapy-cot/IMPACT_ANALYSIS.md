# Impact Analysis — Footprint-Verified Phototherapy Cot

**Author: jayis1** · Illustrative annual steady-state planning model, not measured performance, clinical evidence or a market forecast. All currency is nominal US dollars; no discounting or inflation adjustment.

## Baseline and assumptions

The baseline is a supervised, correctly maintained conventional LED phototherapy cot with a trained operator and access to bilirubin testing. Its clinical outcomes, costs and session count are **not quantified here**; the modeled addition is a repeatable empty-cot irradiance-map workflow, not a proven improvement in care. The published six-device study reports high-irradiance footprints from 67 to 1,465 cm², which motivates measuring the full footprint but does not establish this design's advantage.[4]

| Input | Low | Base | High | Status |
| --- | ---: | ---: | ---: | --- |
| Cots deployed | 1,000 | 10,000 | 10,000 | Scenario assumption, not forecast |
| Nominal supervised sessions per cot/year | 100 | 200 | 200 | Assumption; 200 matches README maximum-capacity example |
| Operational availability (staff, power, parts, referral) | 70% | 85% | 95% | Assumption, unmeasured |
| Fraction of available sessions with valid map | 80% | 90% | 95% | Assumption, unmeasured; not proof of skin exposure |
| Ex-factory cot / service life | $180 / 5 years | same | same | README engineering targets, not quotes or durability evidence |
| Shared meter / coverage / life | $400 / 20 cots / 5 years | same | same | Planning allowance within README's $300–600 range |
| Annual meter recalibration / meter | $100 | same | same | New planning assumption; obtain quotations |
| Annual repairs + batteries / cot | $20 | same | same | Planning assumption |
| Annual electricity + cleaning / cot | $10 | same | same | Planning assumption; local tariffs and use vary |

Annualized equipment and service allowance per cot = $180/5 + $400/(20 × 5) + $100/20 + $20 + $10 = **$75**. This excludes procurement margin, installation, tax, meter breakage, clinician labor/training, clinical assays, eye shields, hospital overhead, referral and regulatory costs. A $400 meter for 20 cots implies one shared meter per 20 cots; no site should rely on an unavailable meter.

## Modeled capacity and cost

Qualified-map sessions/year = cots × nominal sessions/cot/year × availability × valid-map fraction. This counts **sessions with a current empty-cot equipment map**, not infants treated successfully, measured infant dose or lives saved. Annual allowance = cots × $75; allowance/session = annual allowance ÷ qualified-map sessions. Rounded currency is illustrative.

| Scenario | Nominal sessions/year | Qualified-map sessions/year | Meters | Annual allowance | Allowance per qualified-map session |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 100,000 | 56,000 | 50 | $75,000 | $1.34 |
| Base | 2,000,000 | 1,530,000 | 500 | $750,000 | $0.49 |
| High | 2,000,000 | 1,805,000 | 500 | $750,000 | $0.42 |

The README's **2 million sessions/year** is a nominal upper capacity example at 10,000 cots × 200 sessions, before downtime and map failures; it is not the base-case qualified-map count. At 10,000 cots, each 10 percentage-point change in valid-map share at 85% availability changes the modeled count by **170,000 sessions/year**; cost/session also changes because the $750,000 allowance is fixed in this simplified model. This sensitivity is arithmetic, not evidence that mapping changes treatment outcomes.

## Evidence needed before any health-impact claim

Measure incident underexposure, false passes against an independent dense irradiance grid, interrupted treatment, time to alternative care, serial bilirubin results and adverse events against a maintained standard cot in a prospective, ethically approved comparison. Separately establish denominator, case mix, follow-up and confidence intervals before estimating avoided exchange transfusions, neurological injuries or deaths. No such prevention number or cost per health outcome can be calculated responsibly from the assumptions above. IEC safety testing, regulatory authorization, meter service and a working referral pathway remain prerequisites to clinical rollout.

## Source

[4] https://www.nature.com/articles/s41390-021-01795-x
