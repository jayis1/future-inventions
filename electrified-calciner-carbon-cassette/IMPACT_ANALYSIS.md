# Electrified Calciner Carbon Cassette — Impact Analysis

**Author: jayis1** · Scenario arithmetic, **not** measured performance, forecast or claim of carbon removal. Functional unit: one tonne of saleable clinker from a site-qualified dry-process line. The unchanged kiln remains in both alternatives; no credit is assigned for its combustion emissions.

## Boundary and assumptions

The IPCC Tier-1 process baseline is 0.52 t CO₂/t clinker (including a kiln-dust correction); it is a default, not a measurement of this plant.[2] Replace it with a complete site-specific carbonate/dust inventory. The comparator is the same line before a cassette retrofit, at matched clinker quality and output. “Eligible share” is the fraction of this **process CO₂** generated inside the retrofit channels, *not* a plant-adoption percentage. Collection is gas delivered through the custody meter divided by process CO₂ generated in those channels, with all startups, bypasses and venting included. Only verified geological storage or durable mineralization earns a process-emissions displacement credit; account for storage leakage explicitly. Captured CO₂ is mineral-origin process CO₂ **avoided**, not atmospheric CO₂ removed.[2]

Illustrative model, in t CO₂e/t clinker:

`gross collected = 0.52 × eligible share × collection fraction`

`net avoided = gross collected + displaced calciner-fuel CO₂ − (additional electricity kWh/t × electricity kg CO₂e/kWh ÷ 1000) − other incremental CO₂e`

“Other” is a placeholder allowance for CO₂ transport/storage losses, materials and replacement, construction, and other incremental burdens. It is **not independently validated**; if measured burdens exceed it, recompute. Displaced fuel is credited only if metered fuel consumption falls versus the matched line; the kiln fuel is never credited. No second credit is given for CO₂ sale, captured mass or avoided process emissions. Gas-to-storage losses must either lower the collection fraction or appear in “other,” never both. A true lifecycle analysis must also account for displaced heat integration, compression electricity, grid marginal intensity and off-site impacts.

## Illustrative cases (inputs are hypotheses)

| Case | Eligible share | Collection | Additional electricity | Grid factor | Fuel displaced | Other incremental | Gross collected | Net avoided |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Adverse | 60% | 80% | 900 kWh/t | 0.40 kg CO₂e/kWh | 0.10 t/t | 0.04 t/t | 0.2496 t/t | **−0.0504 t/t** |
| Base | 80% | 90% | 700 kWh/t | 0.05 kg CO₂e/kWh | 0.15 t/t | 0.03 t/t | 0.3744 t/t | **0.4594 t/t** |
| Favorable | 90% | 95% | 650 kWh/t | 0.02 kg CO₂e/kWh | 0.18 t/t | 0.02 t/t | 0.4446 t/t | **0.5916 t/t** |

For example, base gross = 0.52 × 0.80 × 0.90 = 0.3744; base electricity burden = 700 × 0.05 / 1000 = 0.035; base net = 0.3744 + 0.15 − 0.035 − 0.03 = 0.4594 t CO₂e/t clinker. The adverse case **increases** emissions. The 0.52 baseline includes dust emissions that may occur outside the cassette: eligible share and collection must be established from actual carbonate/CKD accounting rather than applying 90% to all of 0.52. These scenarios are not confidence intervals.

## Deployment sensitivity, not a forecast

For an illustrative **ten** plants each with 1 Mt/year clinker nameplate and **80%** actual utilization (8 Mt/year total), the adverse/base/favorable arithmetic gives respectively **2.00 / 3.00 / 3.56 Mt/year gross collected** and **−0.40 / 3.68 / 4.73 Mt CO₂e/year net avoided**, rounded to two decimals. Ten plants at base use **5.6 TWh/year additional electricity**. If installed lines instead operate at 50% utilization, multiply all annual totals by 0.625; per-tonne assumptions remain unchanged only if cycling does not lower collection or increase kWh/t. These totals require verified storage for every tonne credited; nameplate capacity alone creates no benefit.

The roadmap's ≥8,000 annual operating-hour aspiration is stricter than the 80% utilization illustration for a continuously rated line; they are distinct tests. Before procurement, measure site-specific carbonate composition and clinker output, kiln/calciner fuel displacement, grid intensity over hourly operation, meter calibration, vent events, leakage and permanent storage records. Report error bars and reject a project if independent net avoided CO₂e is nonpositive or clinker quality fails. Existing indirect calcination has pilot precedent, but **none of this cassette's operating or impact figures is demonstrated**.[1][3]

## Sources

[1] https://www.leilac.com/technology
[2] https://www.ipcc-nggip.iges.or.jp/public/2006gl/pdf/3_Volume3/V3_2_Ch2_Mineral_Industry.pdf
[3] https://www.leilac.com/project-leilac-1
