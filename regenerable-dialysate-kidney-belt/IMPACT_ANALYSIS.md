# Regenerable Dialysate Kidney Belt — Impact Analysis

- **Author:** jayis1
- **Status:** Scenario model for a TRL 2 concept

> All figures are transparent engineering projections, not measured clinical, environmental, or health-economic outcomes. Human benefit depends on treatment adequacy, safety, regulation, service quality, and equitable access.

## Baseline and assumptions

The model uses three adoption cases: 10,000, 100,000, and 1,000,000 active users.

- Conventional comparison: three four-hour haemodialysis sessions per week, or 156 sessions/year.
- Historical input-water comparison: 500 L/session, including reverse-osmosis reject water.[1]
- RDKB treatment makeup-water target: <2 L/user-day; sanitation water is excluded until dock testing establishes it.
- RDKB electricity target: <300 Wh per 12-hour worn session, or <110 kWh/user-year at daily use.
- Conventional travel comparison: 30–150 km round trip per session; this is a scenario range, not a global average.
- Vehicle emissions factor: 0.12–0.25 kg CO2e/km, varied by fleet and occupancy.
- Disposable target: <150 g/user-day, or <55 kg/user-year, plus separately managed receiver concentrate.
- Equipment life target: five years for the belt; one dock serves 20–30 belts.
- Cost target: US$5–12/day consumables and service; clinical labour, vascular access, laboratory testing, and complications are additional.

## Quantitative scenarios

| Metric | 10,000 users | 100,000 users | 1,000,000 users |
|---|---:|---:|---:|
| RDKB patient-sessions/year | 3.65 million | 36.5 million | 365 million |
| Maximum treatment makeup water | 7.3 million L | 73 million L | 730 million L |
| Historical comparison input water | 780 million L | 7.8 billion L | 78 billion L |
| Gross water-demand difference before dock sanitation | at least 773 million L | at least 7.73 billion L | at least 77.27 billion L |
| Worn-session electricity at 300 Wh/day | 1.10 GWh/year | 10.95 GWh/year | 109.5 GWh/year |
| Disposable mass at 150 g/day | 548 t/year | 5,475 t/year | 54,750 t/year |
| Docks required at 20–30 belts/dock | 334–500 | 3,334–5,000 | 33,334–50,000 |
| Annual service/consumable spend at US$5–12/day | US$18–44 million | US$183–438 million | US$1.83–4.38 billion |

The gross water difference is not a lifecycle saving claim. Dock sanitation, manufacture, rejected batches, upstream electricity, and local water-treatment practice must be measured and subtracted.

## Access and patient time

If wearable therapy replaces 50–90% of routine facility visits after clinical validation, each user avoids 78–140 trips/year. Across one million users, that is 78–140 million round trips avoided annually.

At 30–150 km per round trip, the same scenario avoids 2,340–21,000 km of travel per user-year. Using the stated vehicle factor gives an indicative 0.28–5.25 t CO2e/user-year before accounting for public transport, shared rides, rebound travel, dock visits, home energy, or device manufacture.

If each avoided visit saves 1–3 hours of travel and waiting beyond treatment time, the upper adoption case returns roughly 78–420 million patient-hours/year. This is a time-access scenario, not a quality-of-life or mortality estimate.

## Health-system and resilience effects

- A 20–30-user dock concentrates calibration, disinfection, battery diagnostics, and waste custody in a service point smaller than a full dialysis water plant.
- Daily, slower treatment may reduce rapid fluid shifts, but no reduction in hospitalization or mortality is counted without controlled clinical evidence.
- Offline operation and stored shutdown energy could bridge short network or grid failures; continuous dialysis still requires sterile supplies, charged batteries, trained staff, laboratory access, and conventional-care backup.
- Disaster deployment shifts logistics from tanker-scale treated water toward sterile blood sets, cartridges, power, and dock supplies. It does not eliminate cold-chain, waste, or clinical obligations.

## Environmental balance

Potential gains include lower operating water demand, fewer patient journeys, durable pumps and electronics, and recovery of selected zirconium media and batteries.

Countervailing burdens include 55 kg/user-year of target disposable mass, battery production and replacement, activated carbon and ion-exchange media, dock sanitation water and heat, ammonia-receiver waste, and failure-related emergency transport. At one million users, even the disposable target creates about 54,750 tonnes/year of regulated material, making take-back and design-for-disassembly mandatory.

Captured nitrogen remains clinical waste unless analytical release proves it free of unacceptable drugs, metals, pathogens, and other contaminants. Fertilizer recovery is a possible downstream pathway, not a default credit.

## Equity and affordability

At the target US$5–12/day, direct service and consumables equal US$1,825–4,380/user-year before clinical care. That remains unaffordable for many households; procurement by public programmes, insurers, clinics, or humanitarian networks is therefore part of the design, not an optional business model.

Equitable deployment requires multilingual and non-text controls, offline capability, local spare parts, clinician coverage, transparent eligibility rules, and publication of uptime and adverse events by income, sex, age, disability, and geography. A rollout that serves connected urban users first could widen rather than close access gaps.

## Sensitivities and breakpoints

- If makeup water rises from 2 to 10 L/day, the one-million-user requirement grows from 0.73 to 3.65 billion L/year.
- If average power rises from 300 to 500 Wh/day, annual electricity grows from 109.5 to 182.5 GWh per million users.
- If only 50% of sessions are completed, infrastructure and manufacturing impacts remain while clinical value collapses.
- If reusable hardware lasts two rather than five years, annualized belt manufacturing burden rises 2.5-fold.
- If dock utilization averages 10 rather than 20–30 belts, required dock count doubles or triples and service economics deteriorate.
- A small increase in infection, access failure, or ammonia-related hospitalization could outweigh water, travel, and cost advantages; these outcomes require prospective surveillance.

## Decision gates

Scale-up is justified only after trials establish prescribed clearance and ultrafiltration, ammonia containment under induced faults, acceptable serious-adverse-event rates, and correct alarm response. Deployment data must then verify <2 L/day treatment makeup water with sanitation separately reported, <300 Wh/day worn energy, <150 g/day disposables, ≥95% completed-session availability, five-year hardware life, and affordable conventional-care fallback.

No adoption target should override a failed safety, equity, or lifecycle gate.

## Sources

[1] https://pmc.ncbi.nlm.nih.gov/articles/PMC11068938 — Resource consumption of modern-day haemodialysis systems

[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC10240485 — Portable, wearable and implantable artificial kidney systems

[3] https://pmc.ncbi.nlm.nih.gov/articles/PMC4936831 — A wearable artificial kidney for patients with end-stage renal disease
