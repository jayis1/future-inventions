# Sealed Pit-Emptying Shuttle — Impact Analysis

**Author: jayis1. Concept-stage conditional projections, not observed results or a market forecast.** This shuttle moves eligible wet pit contents; it neither treats waste nor establishes a health benefit. See [README](README.md), [specification](SPECIFICATION.md) and [roadmap](ROADMAP.md).

## Boundaries and inputs

One operating year; each *completed eligible* job is assumed to remove 200 L (0.2 m³) for one distinct five-person household. This is a deliberately optimistic job size, not a universal pit volume. Refused or partial jobs, repeats, staff availability, depot bottlenecks and growth in wet sludge viscosity can reduce all totals. Scenarios vary installed devices, annual completed jobs per device and fraction of extracted mass accepted at authorized receivers; no baseline collection or treatment rate has been measured.

| Input | Conditional value | Basis / limitation |
| --- | --- | --- |
| Vessel | 20 L nominal, **16 L** maximum usable | Specification target; 200 L requires ceil(200/16) = **13** fills, with the last fill partial. |
| Fluid rate and power | 10 L/min water-like simulant target at 1.5 m lift, ≤100 W | Unvalidated; 200 L takes at least 20 min net pumping, modeled at 100 W draw = 33.3 Wh/job. Wet-sludge flow may be lower. |
| Jobs/device-year | 50 / 100 / 150 (low/base/high) | Planning assumptions for completed eligible jobs, not observed productivity; 250 operating days imply 0.2 / 0.4 / 0.6 jobs/day/device before refusals. |
| Receiver acceptance | 80% / 90% / 95% of extracted volume | Hypothetical reconciliation fractions, **not** treatment or pollutant destruction; unattributed remainder requires investigation, never legal permission to dump. |
| Hardware | US$600 shuttle including one vessel; US$60 per extra vessel; five-year life; US$80/year maintenance | Unvalidated 2038 ex-factory and spares goals. Thirteen simultaneously staged vessels require **12 additional**, or US$720 goal-only capex, plus the US$600 shuttle. Depot shuttling with fewer vessels is an alternative, with extra trips/time. |

## Illustrative annual scenarios

Formulae: jobs = devices × completed jobs/device-year; extracted m³ = jobs × 0.2; **accepted** m³ = extracted × assumed receiver fraction; vessel fills = jobs × 13; net pumping electricity kWh = jobs × (100 W × 20/60 h)/1,000. At most five *distinct* people per completed job, and only if households never repeat; this is a reach ceiling, not a verified service population.

| Scenario | Devices | Jobs | Extracted m³ | Accepted m³ (assumed) | Vessel fills | Pump-only kWh (approx.) | Maximum distinct people |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 10 | 500 | 100 | 80 | 6,500 | 17 | 2,500 |
| Base | 100 | 10,000 | 2,000 | 1,800 | 130,000 | 333 | 50,000 |
| High | 1,000 | 150,000 | 30,000 | 28,500 | 1,950,000 | 5,000 | 750,000 |

At the base case a single device requires **1,300** vessel fills/year, or 5.2/day over 250 working days. Whether those fills can be safely transported and accepted is a logistics gate, not an automatic multiplier from pump flow. If all receipts were subsequently treated as required, the *received* volume might enter treatment; actual treated volume is unknown until the facility records accepted and processed mass. Even accepted mass is not necessarily additional to a properly operating existing service.

## Economics, safety and environment

The README's US$2/job illustrative hardware-and-maintenance allocation assumes **only one included vessel**: (US$600/5 + US$80)/100 jobs. For a 13-vessel staging fleet at target prices and the same five-year life, capital is US$1,320 and capital plus assumed maintenance is (US$1,320/5 + US$80) = US$344/year, or **US$6.88 / $3.44 / $2.29 per completed job** at 50 / 100 / 150 jobs per device-year. These figures are not full service prices. Add crew labor, PPE, gas testing, cleaning chemicals and wash-water disposal, charging, depot runs, financing, licensing, damaged-part replacement, receiver fees and costs of refused jobs before comparing with maintained Gulper or vacuum services. The 13-vessel capex assumes every vessel is needed at once; more frequent sealed trips trade lower capex for higher transport cost.

At 100 W for 20 minutes, pumping alone is about 0.033 kWh/job; the base scenario's ~333 kWh excludes transport energy, charging losses, idle time and treatment. **No net CO₂e savings** can be estimated without route distances, vehicle fuels, waste-treatment emissions and a matched baseline. No pathogen exposure events, illness cases or mortality prevented can be estimated: swab contamination, spill mass, gas exposure, worker incidents and receiver receipts must be measured in a controlled paired pilot. Reduced open transfer is a proposed mechanism, not a measured effect. Missing receipts represent an accountability problem, not a quantified environmental benefit.

## Sensitivity and go/no-go

At fixed 100 devices and 200 L/job, 50–150 completed jobs/device-year imply **1,000–3,000 m³ extracted**; with 80–95% assumed acceptance, the conditional accepted range is **800–2,850 m³/year** (paired extremes, not a confidence interval). Half-sized eligible jobs halve extracted volume but may not halve setup, travel or washing costs. Real-world refusal frequency and vessel turnaround can dominate this model. Proceed only if an independent 100-job comparison finds safely containable single faults, lower full-chain contact/spill burden, feasible cost and documented authorized treatment acceptance; otherwise redesign or discontinue.