# Steam-Penetration Witness Pack — Impact Analysis

**Author: jayis1** · Illustrative annual scenarios, not measured outcomes or a market forecast. Device remains an unvalidated concept; supplemental traces are neither sterile loads nor infections prevented.

## Model boundary and assumptions

- Define a **hypothetical cohort of 100 eligible sites** with approved sterilizer instrument ports and locally qualified loads. Eligibility is an assumption, not an estimate of real-world compatible sites. Time horizon: one operating year after adoption; 50 operating weeks. No growth curve is assumed.
- Low / central / high adoption: 10% / 50% / 80%, or 10 / 50 / 80 sites. Eligible cycles per adopting site per year: 500 / 1,000 / 1,500 (10 / 20 / 30 per week). Assume one indicator per supplemental test and one readable trace per eligible cycle as an **upper bound**, not observed uptime.
- Assume the README's **unquoted targets**: US$140/set amortized over five years (US$28/site-year), US$0.75 per chemical indicator/test and US$25/site-year calibration. These are not vendor prices. Exclude port installation, approved biological indicators and existing mandatory monitoring, validation/certification, software support, electricity, staff time, failed loads, taxes and financing. Any of these can dominate cost.

| Scenario | Adopting sites | Maximum supplemental traces/year | Target-only annual device + indicator + calibration cost | Cost per possible trace* |
| --- | ---: | ---: | ---: | ---: |
| Low | 10 | 5,000 | US$4,280 | US$0.856 |
| Central | 50 | 50,000 | US$40,150 | US$0.803 |
| High | 80 | 120,000 | US$94,240 | US$0.785 |

*Arithmetic: sites × cycles/site; cost = traces × US$0.75 + sites × (US$140/5 + US$25). Division assumes every cycle yields a usable trace; downtime raises actual cost per usable trace. No claim of cost savings versus existing monitors is justified without matched quotes and workflow data.

## Sensitivity and testable outcomes

- At the central 50,000 attempted cycles, 90% usable-trace yield means **45,000** readable traces; the modeled US$40,150 target-only cost becomes about **US$0.892 per usable trace**, before labor or retests. Yield is hypothetical; actual failures require measurement.
- If controlled trials establish a **2% or 5% actionable fault flag rate** at those 50,000 attempts, that would be 1,000 or 2,500 flagged cycles. These are *illustrations*, not expected detection rates or avoided infections; flags may include false alarms and faults already found by required monitoring. Investigate rather than automatically count averted harm.
- A 100 g hypothetical disposable-electronics equivalent avoided per adopting site annually would imply 1 / 5 / 8 kg less electronics in the low / central / high scenarios, but there is **no measured baseline** for that comparison. Consumable indicators, steel production, decontamination and transport may outweigh it. Do not claim net environmental benefit before lifecycle analysis.

## Evidence required before claiming benefit

Measure compatibility share, sensitivity against blinded seeded failures, false-pass and false-unverified rates, trace availability, added labor, chemical-indicator consumption, maintenance costs and wet-pack frequency by sterilizer/cycle. Compare with the site's required mechanical, chemical and biological monitoring; never subtract already-detected failures twice. Clinical infection outcomes require a separately powered causal study. The CDC references in the [README](README.md#sources) describe process practice, not efficacy of this proposal. Publish negative results and exclude unsafe configurations.
