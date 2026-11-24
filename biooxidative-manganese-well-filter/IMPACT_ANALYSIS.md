# Biooxidative Manganese Well Filter — Impact Analysis

**Author: jayis1** · Scenario model, not measured performance or a health-benefit estimate. The device is a TRL 2 concept. WHO's provisional total-manganese guideline is 0.08 mg/L; the proposed release gate is stricter at <0.05 mg/L.[1] Other chemical and microbial hazards require independent treatment and testing.

## Unit arithmetic and assumptions

- Capacity ceiling: 5 batches/day × 20 L/batch × 365 days/year = 36,500 L/year per well at 100% uptime and all batches passing. Pump draw, backwash, testing losses and holds reduce actual delivery.
- Illustrative feed total Mn = 0.20 mg/L and passing outlet total Mn = 0.04 mg/L, both **assumptions**, giving a concentration difference of 0.16 mg/L. Actual influent varies within the proposed 0.08–0.5 mg/L trial envelope; a smaller inlet-to-outlet difference means less Mn mass captured, not necessarily a worse public-health outcome.
- Illustrative availability is the fraction of the ceiling actually released after holds, downtime and service: low 25%, base 60%, high 85%. These are hypothetical, not field observations. Calculation: sites × 36,500 L/site-year × availability; potential Mn mass difference = delivered L × 0.16 mg/L ÷ 1,000,000 mg/kg.
- Assumes one unit per eligible well, constant concentrations and 365-day operation, with all released batches independently confirmed to meet the criterion. In reality, batch samples, seasonal source chemistry, calibration and laboratory verification determine eligibility.

| Illustrative deployment after validation | Wells | Availability | Released volume, L/year | Difference in Mn mass, kg/year* |
| --- | ---: | ---: | ---: | ---: |
| Low | 10 | 25% | 91,250 | 0.0146 |
| Base | 50 | 60% | 1,095,000 | 0.1752 |
| High | 500 | 85% | 15,512,500 | 2.4820 |

*Mass difference is inlet minus outlet at the assumed concentrations; it is not a measured removal, dose reduction, or health impact. At base-case volume, 1,095,000 L × 0.16 mg/L = 175,200 mg = 0.1752 kg. Residual mass must be captured and characterized, not discharged back into a well.

## Counterfactual, costs and uncertainty

Compare against a **maintained** oxidation/filtration unit, reverse osmosis where appropriate, or an independently safe alternative well on matched water chemistry; an untreated well is not the sole comparator. WHO reports that established processes can achieve <0.05 mg/L, but does not establish this device's relative efficacy.[1] Full-scale inoculated rapid sand filters in one study needed about 17–25 weeks to reach complete removal under different feed conditions, so maturation delays could sharply lower first-year availability.[6]

The US$225/unit figure in the README is an unquoted 2038 ex-workshop target at 10,000 units/year. The hypothetical 50-unit base fleet would have US$11,250 in *target factory cost only* (50 × $225), excluding source surveys, assay meters/reagents, laboratory cross-checks, installation, operators, backup water, pumps, maintenance, waste handling and compliance. No delivered-water cost or savings can be inferred until these recurring inputs and batch rejection rates are measured. Economic and health projections are intentionally omitted.

Pilot decisions should report measured litres released, total-Mn distribution and out-of-spec releases, microbiological status, cost per confirmed litre, labor, waste mass, and the fraction of time a safe alternative was available. A failed test closes the valve; maximizing litres cannot override the release criterion. Aggregate volumes above are conditional projections, not promised access to safe drinking water.

## Sources

[1] https://cdn.who.int/media/docs/default-source/wash-documents/water-safety-and-quality/chemical-fact-sheets-2022/manganese-fact-sheet-2022.pdf
[6] https://pmc.ncbi.nlm.nih.gov/articles/PMC12070406
