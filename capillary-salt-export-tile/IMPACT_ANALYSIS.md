# Capillary Salt-Export Tile — Impact Analysis

**Author: jayis1.** Illustrative one-season scenario, not measured performance, validated remediation or a sales forecast. See [README.md](README.md) for design and [ROADMAP.md](ROADMAP.md) for evidence gates.

## Accounting boundary

One cassette serves a nominal 10 m² fallow strip, with 0.1 m² of collector plan area. The season is at most 120 operating days in this model; a day lost to rain, drought, cleaning or wick blockage is excluded. Every scenario assumes source porewater at **5 g/L dissolved salts**, not a universal soil concentration. Gross ion input to cassette is `units × active days × L/day × 5 g/L`. Recoverable salt is input × physical collection efficiency. **Safely exported** salt additionally multiplies by the fraction delivered to a permitted final destination; material spilled, left on site or improperly disposed is not counted. These fractions are assumptions, not measured efficiencies. Even safely exported mass cannot be equated with net 0–20 cm soil improvement until paired depth-resolved inventories rule out salt resupply and lateral redistribution.

## One-season sensitivity

| Case | Units / nominal strips | Active days | Flux L/unit-day | Collection × proper-disposal fraction | Gross ion input | Safely exported illustration | Evaporated soil water |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 10 / 100 m² | 60 | 0.1 | 50% × 80% | 0.30 kg | 0.12 kg | 60 L |
| Central | 100 / 1,000 m² | 120 | 0.2 | 75% × 90% | 12 kg | 8.10 kg | 2,400 L |
| High-adoption / high-capture | 1,000 / 10,000 m² | 120 | 0.2 | 90% × 95% | 120 kg | 102.60 kg | 24,000 L |

The high case changes deployment count and collection/logistics, **not** the per-cassette maximum flux in the README: gross upper bound is 1 g/unit-day or 120 g/unit-season. A central cassette would collect 0.75 g/active day, above the README's unverified 0.5 g/day *collected* prototype gate, and safely export 0.675 g/active day, or 81 g in 120 days. A low cassette would collect 0.25 g/active day and fail the gate. No field rate has been demonstrated.

## Cost, waste and adoption constraints

At the README's **unquoted 2038 goals**, initial installed allowance is US$50/unit; annual replacement/cleaning allowance is US$8/unit. Thus low / central / high scenarios imply US$500 / US$5,000 / US$50,000 initial allowance and US$80 / US$800 / US$8,000 annual allowance, respectively, *before* laboratory assays, shipping, approved waste disposal, permits, land, surveys and monitoring. At central assumptions, initial allowance alone is about US$0.62 per safely exported gram (US$5,000 / 8,100 g), not a full-remediation cost or quote. Capture and disposal fractions multiply: a collected pile without documented legal transfer is not counted as safely exported. Actual operators must fund sealed storage and destination capacity for the *collected* material, including any co-concentrated contaminants; estimate complete waste mass by assay, not by the modeled soluble-salt fraction alone.

## Limits and go/no-go

No crop-yield, freshwater-saving, hectare-wide reclamation, climate or livelihood benefits are assigned. Groundwater recharge and irrigation can replenish removed salts; moisture depletion may harm crops; visual crust or EC changes alone do not prove net removal. Compare treated and sham 0–20 cm ion inventories (with soil bulk density, area and sampling uncertainty), groundwater and neighboring plots before attributing site impact. Compare local drainage-plus-leaching on a matched water, land, time, labor and disposal boundary: FAO describes saline drainage discharge as essential to successful leaching, but publishes no directly matched cassette benchmark.[2] Pause adoption if the soil inventory is unchanged, an uncontained spill occurs, water stress increases or waste transfer cannot be documented. All larger-area examples here are conditional arithmetic, not an adoption prediction.

## Source

[2] FAO, *Management of Salt Affected Soils*, https://www.fao.org/soils-portal/soil-management/management-of-some-problem-soils/salt-affected-soils/en/ . Context for conventional leaching and drainage, not evidence that this invention works.
