# Owner-Fitted Deorbit Cassette — Impact Analysis

**Author: jayis1**
**Status: illustrative scenario model, not a forecast or measured flight result.** No collisions prevented, compliance approvals or insured savings are claimed. Hardware under evaluation: 10–100 kg hosts, near-circular 550–700 km LEO, 200 m captive tape, 2 m² sail and ≤3 kg cassette. The README's ≤5-year goal is conditional on an approved orbit and conservative propagation; the lifetimes below are *hypothetical inputs*, not predictions for that entire envelope.

## Assumptions and method

- Horizon: a hypothetical ten-year installation cohort of **10,000 eligible spacecraft** (1,000/year), matching the README's planning scenario. Eligibility presupposes owner consent, physical compatibility and mission-specific approval; it is not a global launch forecast.
- Adoption: low/base/high cases fit 10% / 50% / 100% of those eligible spacecraft. Fit counts are 1,000 / 5,000 / 10,000 over ten years (100 / 500 / 1,000 per year).
- Combined probability of **successful integration, safe activation and effective disposal**: 80% / 90% / 99% respectively; these are scenario assumptions, **not** measured reliabilities. The README's ≥99% *deployment-only* engineering target is distinct from end-to-end disposal success.
- Counterfactual orbital residence after mission end: 8 years without *any* disposal device; successful cassette cases: 4 years. These are deliberately assumed solely to illustrate arithmetic. A failed case retains 8 years; an already-compliant baseline, sail-only alternative or orbit with weak electrodynamic drag would reduce or erase incremental benefit.
- Conditional modeled benefit per success = `8 − 4 = 4` avoided derelict object-years. Count the full eventual residence reduction of each cohort, including years after the ten-year installation window; **do not** read this as a reduction already realized by year ten. Actual assessment requires matched-orbit propagation under solar-cycle, attitude and density uncertainty [1].
- Illustrative all-in cost for this exercise: **US$1,000 per fitted spacecraft**, or US$10 million at full uptake, including hardware/integration/monitoring as a *single assumed input*, not a vendor quote. The README's US$250 ex-factory price at 100,000 units/year is a separate unvalidated scale goal; these adoption volumes do not establish that manufacturing rate. Launch-mass premium, insurance, licensing and liability are not costed.

## Conditional outputs

| Scenario | Fitted / year | Fitted / 10 yr | End-to-end success assumption | Incrementally shortened residences | Eventual object-years avoided | Assumed fitted cost | Cost / avoided object-year |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 100 | 1,000 | 80% | 800 | 3,200 | US$1.0m | US$312.50 |
| Base | 500 | 5,000 | 90% | 4,500 | 18,000 | US$5.0m | US$277.78 |
| High | 1,000 | 10,000 | 99% | 9,900 | 39,600 | US$10.0m | US$252.53 |

Arithmetic: `fitted = 10,000 × adoption`; `shortened = fitted × combined success`; `avoided object-years = shortened × 4`; `cost = fitted × US$1,000`; last column divides cost by avoided object-years. Totals count failures' expense, but exclude failures' negative debris or reentry consequences. Object-years measure exposure duration, **not** conjunction events or collisions: an extended 200 m tape or 2 m² sail could raise encounter hazard while reducing residence time. A collision/conjunction estimate requires a time-resolved orbit, target population, cross-section, tracking accuracy and traffic-service model; no defensible percentage reduction follows from these inputs.

## Sensitivity and decision rule

If the true matched baseline lasts only 4 years, or the cassette takes 8, modeled incremental benefit is **zero** despite installations. If disposal takes longer or a severed tape creates debris, net benefit may be negative. At 700 km, low solar activity and poorly oriented tape can invalidate even the five-year disposal criterion. Require an operator-reviewed orbit-specific lifetime, conjunction-area-time comparison and whole-spacecraft reentry assessment before claiming any environmental or economic benefit. Compare against the best available alternative, not only "do nothing." Uncontrolled reentry and licensing remain operator responsibilities.

## Sources and provenance

1. NASA, [State-of-the-Art of Small Spacecraft Technology: Deorbit Systems](https://www.nasa.gov/smallsat-institute/sst-soa/deorbit-systems/) (May 2026): lifetime dependence on altitude, ballistic coefficient and solar conditions; demonstrated component classes. All adoption, success, lifetime and cost figures above are explicitly hypothetical inputs, not NASA estimates.
