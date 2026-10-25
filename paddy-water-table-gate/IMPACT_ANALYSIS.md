# Paddy Water-Table Gate — Impact Analysis

**Author: jayis1. Illustrative conditional estimates, not observed gate performance.** One cropping season per year, eligible level plots of 0.1 ha with controlled elevated supply; five-season modeled service life. Volumes below are irrigation withdrawals, not necessarily consumptive water savings or aquifer recovery. Do not add water, methane and dollar lines together as if they are the same benefit.

## Baseline and assumptions

| Quantity | Illustrative assumption | Provenance / limitation |
| --- | --- | --- |
| Counterfactual | Continuous flooding on eligible plots | A *scenario*, not the incremental manual-AWD comparator. |
| Plot density | 10 gates/ha | 0.1 ha per gate in the README. |
| Baseline irrigation | 1,000 mm/ha/season | Hypothetical site value; meter before use. |
| AWD water saving | 20% = 200 mm = 2,000 m³/ha/season | Modeled within IRRI's reported ~30% in suitable sites; gate share unknown.[1] |
| Baseline CH₄ | 100 kg CH₄/ha/season | Hypothesis requiring chamber measurement; **not** an IRRI emission factor. |
| AWD CH₄ reduction | 40% = 40 kg/ha/season | Scenario within IRRI's 30–70% range vs flooding.[1] |
| CH₄ climate conversion | 27 kg CO₂e/kg CH₄ | Rounded modeling assumption for 100-year non-fossil methane; methodology must specify its required factor. |
| N₂O offset | 25% of CH₄-derived CO₂e benefit | Hypothetical allowance, not a measured N₂O factor; sample both gases. |
| Water economic value | US$0.05/m³ avoided delivery | Sensitivity assumption, not a farm tariff or promised saving. |
| Hardware/service | US$75/plot over five seasons = US$15/plot-season | README cost model: $35 unit + $15 fitting + $5/year × 5. |

IRRI's safe AWD guidance uses a perforated field tube and re-flooding near 15 cm below the soil surface; its published ranges describe **AWD relative to continuous flooding**, not an automatic inlet relative to a farmer already doing AWD.[1] This analysis assumes every adopted gate *enables* AWD on a plot that otherwise remained flooded. Where a farmer already practices manual AWD, set the attributable water and emissions effects to **zero until a paired trial measures an incremental difference**. No carbon-credit receipts are assumed.

## Calculation (one season)

- Water: `area (ha) × 2,000 m³/ha` = modeled avoided irrigation delivery.
- Gross CH₄ benefit: `area × 100 kg CH₄/ha × 0.40 × 27 / 1,000` = 1.08 t CO₂e/ha.
- Net after hypothetical N₂O offset: `gross × (1 − 0.25)` = **0.81 t CO₂e/ha**; soil-carbon changes and embodied hardware emissions excluded.
- Gate cost: `area × 10 plots/ha × US$15/plot-season` = **US$150/ha-season**. Water value: `area × 2,000 m³/ha × US$0.05/m³` = **US$100/ha-season**, leaving **−US$50/ha-season** before labor, pumping-energy changes, yield, transport, taxes or finance. It is *not* a demonstrated return on investment.

## Conditional adoption cases

| Adopted eligible area | Gates | Water delivery avoided/season | Gross CH₄ benefit | Net after N₂O offset | Water value less gate cost/season |
| --- | ---: | ---: | ---: | ---: | ---: |
| 10,000 ha | 100,000 | 20 million m³ | 10,800 t CO₂e | 8,100 t CO₂e | −US$0.5 million |
| 100,000 ha | 1 million | 200 million m³ | 108,000 t CO₂e | 81,000 t CO₂e | −US$5 million |
| 1 million ha | 10 million | 2 billion m³ | 1.08 million t CO₂e | 810,000 t CO₂e | −US$50 million |

These are scale multiplications, **not forecasts** that this acreage is suitable or that gates will deliver these outcomes. At 10,000 ha, changing only the hypothetical N₂O offset from 0% to 50% changes net avoided emissions from 10,800 to 5,400 t CO₂e; zero actual incremental adoption over manual AWD yields zero attributable benefit. At US$0.075/m³, the modeled water value merely matches US$150/ha-season hardware/service cost; this break-even excludes labor and yield. Pumped-system electricity/diesel savings cannot be computed without measured hydraulic head, pump efficiency and actual avoided pumping; gravity gates themselves consume no electricity. Independently sample both gases, metered irrigation, yields and contaminants over multiple seasons before any claim or credit issuance.

## Source

[1] https://ghgmitigation.irri.org/mitigation-technologies/alternate-wetting-and-drying — IRRI Alternate Wetting and Drying (AWD water, CH₄ and threshold ranges).
