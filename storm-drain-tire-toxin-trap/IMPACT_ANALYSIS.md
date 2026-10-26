# Storm-Drain Tire-Toxin Trap — Impact Analysis

**Author: jayis1** · Illustrative screening calculation, not measured performance or an ecosystem forecast.

## Scope and assumptions

One hypothetical municipality selects **1,000 eligible inlets**; each drains a notional **1,000 m²** paved catchment producing **500 m³/year** of runoff (equivalent to 0.5 m/year effective runoff depth). These are scenario inputs, **not a survey, rainfall record or literature-derived city inventory**. Loads and concentration ranges below are deliberately hypothetical and must be replaced with paired site data. The README's 0.25 L/s design flow is a capacity, not a claim that annual runoff is treated continuously. Its 60 L bed and 120 s nominal pore-water residence do not establish a media life.

| Input per inlet-year | Low | Base | High | Status |
|---|---:|---:|---:|---|
| Runoff (m³) | 500 | 500 | 500 | Assumed common scenario |
| Incoming tire-associated solids (kg) | 1 | 3 | 6 | Assumed; size distribution unknown |
| Flow-weighted incoming dissolved 6PPDQ (ng/L) | 50 | 150 | 300 | Assumed illustration, not local measurement |
| Fraction of each pollutant's annual incoming **mass** routed through bed | 0.30 | 0.60 | 0.80 | Assumed separately for each pollutant; bypass and uptime included |
| Retention within treated path, tire-associated solids | 0.30 | 0.50 | 0.70 | Assumed; size-resolved validation needed |
| Retention within treated path, dissolved 6PPDQ | 0.40 | 0.70 | 0.80 | Assumed; base matches proposed treated-flow target, not evidence |

## Calculation and projections

Whole-storm captured mass = incoming annual mass × routed mass fraction × treated-path retention. No mass in the untreated bypass is counted as captured. For dissolved 6PPDQ, incoming mass in mg = 500 m³ × 1,000 L/m³ × concentration (ng/L) / 1,000,000 ng/mg. Assumed concentration is an event-weighted annual mean, so these equations do not model individual peak storms or sorbent exhaustion.

| Output | Low | Base | High |
|---|---:|---:|---:|
| Incoming dissolved 6PPDQ per inlet (mg/year) | 25 | 75 | 150 |
| Retained tire-associated solids per inlet (kg/year) | 0.09 | 0.90 | 3.36 |
| Retained dissolved 6PPDQ per inlet (mg/year) | 3 | 31.5 | 96 |
| Retained solids at 1,000 inlets (kg/year) | 90 | 900 | 3,360 |
| Retained dissolved 6PPDQ at 1,000 inlets (g/year) | 3 | 31.5 | 96 |
| Whole-storm 6PPDQ reduction, under assumptions | 12% | 42% | 64% |

The two pollutant metrics are **not additive**: particle-associated chemical could otherwise be counted twice. Retained mass must remain below measured usable media and sump capacity over its actual service interval; no capacity measurement exists. A missed swap, desorption, bypass misrouting or higher contaminant load can reduce or reverse modeled benefit.

## Cost and interpretation

The README gives an **unverified** US$280 ex-factory unit and US$35 replacement-bed target. Assuming five-year hardware life, two beds/year and an **illustrative** US$150/inlet-year inspection and labor allowance yields **US$276/inlet-year** (280/5 + 2 × 35 + 150), or **US$276,000/year** for 1,000 inlets. This **partial modeled cost excludes** installation, permits, traffic management, laboratory sampling, collection, waste characterization, final disposal, repairs and financing. Dividing only that partial annual cost by modeled retained solids gives approximately **US$3,067/kg (low), US$307/kg (base), US$82/kg (high)**; this is not a quoted operating price or a like-for-like comparison with a bioretention cell. At base assumptions the modeled dissolved capture is only 31.5 mg per inlet-year, so media utilization and sampling costs need explicit evaluation.

There is no defensible numerical estimate here of fish saved, stream-kilometres protected, human health benefit or carbon reduction. Measure paired event-integrated influent, treated-outlet and bypass loads, hydraulic head loss, cartridge aging, leachate, crew hours and actual invoices across seasons; then compare against untreated controls and approved alternatives. Scaling these hypothetical inputs to a real city, or claiming regulatory compliance from them, would be unwarranted.
