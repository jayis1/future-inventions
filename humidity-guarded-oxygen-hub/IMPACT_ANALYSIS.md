# Humidity-Guarded Oxygen Hub — Impact Analysis

**Author: jayis1.** This is a conditional planning model, not a field result, epidemiological estimate or forecast of lives saved. See the [design and source list](README.md#sources). [WHO/UNICEF guidance](https://www.who.int/publications/i/item/9789241516914) covers selection and maintenance of oxygen equipment; local baseline availability and costs must be measured before procurement.

## Boundary and assumptions

- Geography: illustrative set of staffed clinics in humid, low-resource settings; no assertion that 10,000 such sites currently exist or would adopt the hub.
- Scale/time: 10,000 hubs in a hypothetical mature deployment year; 365 days/year; each scheduled for 8 operating hours/day at 5 L/min, not continuous 24-hour service. Zero deployment means zero modeled effect.
- **Assumed**, not measured, baseline: maintained certified concentrator plus identical backup achieves qualified output during 85% of scheduled hours; proposed hub might achieve 90–95% *only if* comparative trials establish it. Qualified means outlet oxygen concentration, flow and pressure within a validated envelope; this is not oxygen delivered to a patient.
- Hardware planning cost: US$2,450/hub including optional PV, per README; excludes reserve cylinders, freight, service, battery replacements, certification, installation variants, clinical consumables and disposal. These omissions preclude a claimed net saving.
- Power upper budget: 350 W at full rated flow, 8 h/day; actual energy includes standby, charging losses and site-dependent PV generation. No emissions saving is claimed without grid mix, PV yield and equipment life-cycle analysis.

## Reproducible calculations

| Conditional scenario | Calculation | Result |
| --- | --- | --- |
| Rated gross capacity, all units operating 8 h/day | 10,000 × 5 L/min × 60 min/h × 8 h/day | 24 million L/day (nameplate, not assured output) |
| Incremental qualified machine-hours/day | 10,000 × 8 h/day × (90–95% minus 85%) | 4,000–8,000 h/day |
| Incremental qualified machine-hours/year | Previous row × 365 days | 1.46–2.92 million h/year |
| Incremental qualified outlet volume/year | Previous row × 5 L/min × 60 min/h | 438–876 million L/year, *conditional on both the flow and availability gates* |
| Initial equipment allocation | 10,000 × US$2,450 | US$24.5 million, before excluded costs |
| Rated electrical load if every unit runs as scheduled | 10,000 × 0.350 kW × 8 h/day × 365 days | 10.22 GWh/year before charging losses and PV offsets |

If the matched comparator already achieves 95% qualified availability and the hub also achieves 95%, incremental volume is **zero**. If the hub performs worse, the difference is negative. Site-specific scheduled hours, working devices, actual flow, clinical demand, backup supply and outages all reduce the real effect relative to nameplate. Gas saved from cylinders during downtime must not be counted again as new clinical supply.

## What to measure before claiming impact

A preregistered field comparison must measure each device's outlet concentration, pressure and flow continuously, downtime, fault causes, mean time to repair, filter/dryer/sieve replacement, cylinder usage, technician labour, battery renewal and total cost per qualified litre over at least 12 months. Evaluate oxygen-enrichment fire hazards, contamination and e-waste from batteries, filters and spent sieve. No patient-hours, avoided deaths, emissions reduction or economic payback can be inferred from outlet capacity alone; those require separate evidence and accounting. No clinical deployment before certification and local regulatory approval.
