# Silica Wetwork Recovery Bench — Impact Analysis

**Author: jayis1. Concept-stage scenario, not observed outcomes or a forecast.** The proposed bench uses fresh water in a single pass and collects contaminated runoff; it does not recycle water or establish a silicosis reduction. See [README](README.md) and [roadmap](ROADMAP.md).

## Boundary and assumptions

Model one bench at a small stationary finishing station for one operating year. These are transparent planning assumptions, not field observations; uptake figures are illustrative installed-stock scenarios, not dated market forecasts.

| Input | Assumption | Basis / uncertainty |
| --- | --- | --- |
| Active wet-work time | 4 h/day × 250 days/year = 1,000 h/year | Scenario only; if duty halves, all flow totals halve. |
| Sheet flow | 0.5 L/min = 30 L/h | Unvalidated design target; actual duty and overspray must be metered. |
| Runoff collection | 90% of discharged water | Unvalidated target; evaporation and water retained on stone mean discharged volume may be less than feed. |
| Workers sharing one bench | 2 | Planning assumption, not two simultaneous users or proof of reduced exposure. |
| Pump electrical input | 24 W while running | Illustrative 12 V × 2 A; actual current and full-system/tool energy must be measured. |
| Ex-factory bench cost | US$650 each at 10,000 units/year in 2038 | Design goal, not an available price; assumes scale economics that smaller scenarios may not attain. |

## Illustrative annual throughput

Formula: 0.5 L/min × 60 min/h × 1,000 h/year = **30,000 L (30 m³) fresh feed per bench-year**. If *all* feed is discharged, the ≥90% target implies ≥27 m³ collected and ≤3 m³ not collected per bench-year. This is a conservative **conditional runoff accounting**, not a claim of 3 m³ released outdoors: contain and investigate any uncollected liquid. Evaporation or retention changes discharged volume; measure both independently. At 24 W for 1,000 h, assumed pump consumption is 24 kWh/bench-year, excluding tools, extraction, water supply, treatment and transport.

| Installed benches | Nominal workers sharing benches | Fresh feed (m³/year) | Conditional collected runoff at 90% (m³/year) | Conditional uncollected at 10% (m³/year) | Assumed pump electricity (kWh/year) | Goal-only ex-factory capex (US$) |
| ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| 100 (low) | 200 | 3,000 | 2,700 | 300 | 2,400 | 65,000 |
| 1,000 (base) | 2,000 | 30,000 | 27,000 | 3,000 | 24,000 | 650,000 |
| 10,000 (high) | 20,000 | 300,000 | 270,000 | 30,000 | 240,000 | 6,500,000 |

Capex simply multiplies a high-volume price goal by installed units; it is **not** a quote or realistic procurement estimate for the low/base cases. Ongoing water, energy, pail replacement, installation, PPE, exhaust, sampling, labor, sludge transport, treatment and end-of-life costs remain unquantified and could dominate. Do not mistake captured water for water saved: without a validated treatment/reuse loop, estimated **net water savings are zero** relative to an equally supplied single-pass wet station. Against a dry process, added water demand may be the full 30 m³/bench-year; neither comparison alone decides safety.

## Solids and health: measurement needed

No defensible tonnes of silica recovered can be estimated without material removal rate, mineralogy and solids mass balance. During a pilot, weigh workpieces before/after, screen chips, settled solids and retained residue; measure contaminants and drying/handling losses. Gross solids captured are not a saleable silica product or automatically avoided landfill disposal. Waste classification, discharge permissions and reuse require local analysis.

No cases of silicosis prevented or percentage exposure reduction are projected: the dose–response, worker baseline and actual breathing-zone improvement are unknown. A 20-shop paired pilot should compare full-shift personal samples and cleaning events against maintained wet tools and wet-plus-exhaust stations. The US OSHA 25 µg/m³ action level and 50 µg/m³ PEL (8-hour TWA) are jurisdiction-specific reference values, not claims that the bench meets either.[1] Findings may be null or adverse if wet operation creates mist or maintenance dust.

## Sensitivity and decision rule

At 0.25–0.75 L/min and 500–1,500 active h/year, fresh feed spans **7.5–67.5 m³/bench-year**; multiply by actual metered discharge fraction before applying collection efficiency. A missed pail exchange or failed skirt can erase containment gains. Advance only if independently reviewed paired exposure, maintenance and wastewater evidence demonstrates a net benefit relative to an appropriately maintained baseline without transferring risk to sludge handlers. The 2050 scale case remains illustrative, contingent on those gates.

## Source

[1] https://www.osha.gov/sites/default/files/publications/OSHA3902.pdf — OSHA silica guide (existing README source; check current local rules before use).
