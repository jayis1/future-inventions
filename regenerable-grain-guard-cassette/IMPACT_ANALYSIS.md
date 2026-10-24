# Regenerable Grain Guard Cassette — Impact Analysis

**Author: jayis1.** Scenario model, not measured field impact or a market forecast. One cycle is 90 days of storage of initially dry (≤13% wet-basis) paddy rice in a sealed 50 kg bin; the comparator is the **same bin without a cassette**, not an open sack. The README's 100,000-bin example stores 5,000 tonnes per cycle; it does not save 5,000 tonnes. Hermetic storage already reduces insect damage, while beads have finite moisture capacity.[1][2]

## Inputs and boundaries

| Parameter | Illustrative input | Status / qualification |
| --- | ---: | --- |
| Bin fill | 0.05 tonnes dry paddy per bin-cycle | Fixed design size; shared bin cost cancels in the comparison. |
| Cassette manufacture | US$18 per unit | Unvalidated 2035 cost target; dock, meter, financing and bin excluded. |
| Amortization | 10 cycles | Planning assumption, **not demonstrated** lifetime. |
| Regeneration and inspection | US$2 per bin-cycle | Unvalidated service budget; may exclude travel and failed units. |
| Incremental total | US$3.80/bin-cycle = US$76/tonne-cycle | US$18/10 + US$2; excludes dock/meter capital and spoilage testing. |
| Paddy value | US$400/tonne | Illustrative local saleable-grain value, **not a market quote**. |
| Incremental loss reduction vs matched bin | 0.5%, 2%, 8% of initial grain mass | Scenario assumptions only; not measured and not total postharvest loss. |
| Adoption / treated bins per cycle | 10,000 / 100,000 / 1,000,000 | Low/base/high hypothetical deployment, not installed base or annual adoption. |

The modeled extra marketable mass is `bins × 0.05 tonnes/bin × incremental loss-rate reduction`; gross retained-grain value is that mass times US$400/tonne. Net incremental grain-only value subtracts `bins × US$3.80`. Do **not** add quality premiums, avoided purchases, and the same recovered grain's sale proceeds together: that would double count. The scenario assumes every bin completes one cycle, all retained grain is marketable, and there is no displacement or rebound; failed seals and spoilage testing could make reality worse.

| Case, one 90-day cycle | Bins | Protected tonnes | Extra saleable tonnes vs same plain bin | Gross retained-grain value | Added cassette/service cost | Net grain-only value |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Low (0.5 pp reduction) | 10,000 | 500 | 2.5 | US$1,000 | US$38,000 | **−US$37,000** |
| Base (2 pp reduction) | 100,000 | 5,000 | 100 | US$40,000 | US$380,000 | **−US$340,000** |
| High (8 pp reduction) | 1,000,000 | 50,000 | 4,000 | US$1,600,000 | US$3,800,000 | **−US$2,200,000** |

Here “pp” means percentage points of **incremental marketable-mass loss avoided**, not percent of already lost grain. Even the optimistic case loses money at the modeled price. Break-even on grain mass alone requires `US$3.80 / (0.05 tonnes × US$400/tonne) = 0.19`, or a **19-percentage-point** improvement over the sealed-bin control. At US$200/tonne that rises to 38 pp; at US$800/tonne it falls to 9.5 pp, still demanding. At 20 cycles and unchanged US$2 service, unit cost becomes US$2.90 per bin-cycle; at US$0.25 service and 20 cycles it becomes US$1.15, requiring 5.75 pp at US$400/tonne—each is a counterfactual, not a validated cost reduction. A premium for independently proven quality or avoided lot rejection would need a separate measured valuation; neither is booked above.

## Physical and environmental checks

A 1 kg cassette with the **assumed** 8 wt% usable capacity holds at most 0.08 kg water under the design envelope, with 18 g budgeted for a 0.2 g/day leak over 90 days, 40 g for grain/headspace redistribution and 22 g reserve. That is not a harvest dryer. At the published **lab bead-system** reference of 4.86 MJ per kg water removed,[2] desorbing the full 0.08 kg corresponds to ~0.39 MJ (~0.11 kWh) of reference heat; whole-dock heat losses, electricity or fuel, transport and cassette manufacture must be measured before claiming energy or greenhouse-gas savings. Captured water is exhausted outdoors during off-bin service, not returned to grain.

No numeric CO₂e credit, aflatoxin exposure reduction, health benefit, or avoided-land-use figure is booked: these require matched-control attribution, a lifecycle inventory and local food-safety measurements. Grain preserved in a warehouse does not automatically displace production, and drying does not remove toxin already formed. A go/no-go pilot must measure incremental saleable mass, toxin levels, dock energy, replacement rate, labor and seal repairs together; if net benefit remains negative, distribute repaired plain hermetic bins instead.

## Sources

[1] https://pmc.ncbi.nlm.nih.gov/articles/PMC5296677/ — Kumar and Kalita, *Foods* (2017), grain-storage and hermetic-system review.
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC11391545/ — Ying et al., *ACS Omega* (2024), laboratory energy performance of zeolite drying beads for paddy; does not validate this cassette or a field dock.
