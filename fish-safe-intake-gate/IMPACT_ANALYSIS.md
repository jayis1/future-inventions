# Fish-Safe Intake Gate — Impact Analysis

**Author: jayis1**

**Status:** Scenario arithmetic for a research concept, not field results or a forecast.

**Scope:** Eligible, permitted 10 L/s gravity-fed small diversions only; exclude sites without suitable sweep flow, fish-stage protection, access or water-rights clearance. No eligible-site count is known.

## Transparent assumptions (one illustrative irrigation season)

| Variable | Assumption | Evidence status |
| --- | ---: | --- |
| Modules in illustrative cohort | 100 | Hypothetical adoption, not demand or eligible-site estimate. |
| Nominal screened capacity per module | 10 L/s = 0.010 m³/s | Design point in the README, not measured capacity. |
| Scheduled withdrawal | 8 h/day × 120 days | Illustrative operating calendar, not observed use. |
| Availability and utilization | 0–100% of schedule | Unknown; trips, low water and permits reduce delivery. |
| Clean-screen added head loss | 0–0.10 m at rated flow | Target ceiling, not a measurement; dirty-screen behavior unknown. |
| Workshop price / annual local service | US$250 / US$25 per module | Unquoted goals; exclude installation, permits, surveys and replacement panels. |

## Direct capacity and water accounting

- Simultaneous rated capacity = `100 × 0.010 m³/s = 1.0 m³/s`; 10,000 modules would represent 100 m³/s **nameplate** capacity, not withdrawal or net new water.
- Scheduled upper bound per module = `0.010 m³/s × 3,600 s/h × 8 h/day × 120 days = 34,560 m³/season`.
- Cohort scheduled upper bound = `100 × 34,560 = 3,456,000 m³/season` (3.456 million); actual delivery = this bound × measured availability/utilization and may be zero. This is water already diverted through a screen, **not** water created or saved.
- Net delivery difference versus an approved screen = measured volume through this gate minus measured volume through that comparator under matched stage, diversion entitlement and season. Report closure hours separately; do not assume zero delivery loss.

## Fish outcomes: no unsupported fish-saved total

- Define baseline `E_b` and gate `E_g` as entrained fish per 1,000 m³ for each locally protected species/life stage, sampled under matched conditions; estimate avoided entrainment as `(E_b − E_g) × measured gate-delivered m³ / 1,000`. A negative result means harm, not benefit.
- Evaluate impingement, contact injury and delayed mortality separately; do not add overlapping individuals across metrics. Compare with an approved, maintained screen *and*, only where ethically and legally permitted, a documented unscreened baseline. Neither baseline rate nor gate rate is known, so a numerical avoided-fish projection would be invented.
- Population and ecosystem gains cannot be inferred from avoided entrainment alone: survival after passing the screen, predation, altered river flows and cumulative habitat effects remain unmeasured. Independent multi-season monitoring is required.

## Energy, cost and uncertainty

- A 0.10 m head-loss ceiling at 10 L/s implies `ρgQH = 1,000 kg/m³ × 9.81 m/s² × 0.010 m³/s × 0.10 m ≈ 9.81 W` of hydraulic power at that condition. Over the illustrative 960 scheduled hours, the maximum at **constant rated flow and clean-screen target head loss** is ~9.42 kWh/module, ~942 kWh/100 modules. This is lost hydraulic potential, not measured electric use; gravity sites may have no pump, and fouling can exceed the clean-screen target before shutdown.
- Cohort workshop-price goal = `100 × US$250 = US$25,000`; annual local brush/seal service allowance = `100 × US$25 = US$2,500`. Neither is a quote or a full-system budget. Compare installed capital, maintenance labor, replacement, survey, permits and lost irrigation against the conventional alternative before claiming savings.
- Sensitivity is dominated by eligible-site count, actual operating hours, shutdown frequency, local fish density/life stages and screen maintenance. Publish measured distributions and uncertainty intervals, not just averages, after the pilot.

The sole external comparator for hydraulic framing is the U.S. Bureau of Reclamation's *Pocket Guide to Screening Small Water Diversions* [1]; its salmonid example is not a universal fish-protection threshold. All cohort values above are explicitly illustrative calculations from the README design targets.

## Sources

[1] https://www.usbr.gov/tsc/techreferences/hydraulics_lab/pubs/manuals/Small%20Screen%20Design%20Manual%20USBR.pdf
