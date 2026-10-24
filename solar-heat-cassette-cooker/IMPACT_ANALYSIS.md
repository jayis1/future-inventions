# Solar Heat Cassette Cooker — Impact Analysis

**Author: jayis1.** Scenario arithmetic, not measured impact or a forecast. Device status: research concept. This model deliberately uses LPG as a transparent **fuel-displacement baseline**, even though LPG is already a cleaner cooking fuel; displacement of biomass could affect smoke exposure but requires separate measured fuel and exposure data. The 200 displaced small-meal events/year base case already discounts cloudy days, unsuitable meals and stove stacking; do not multiply by an additional adoption factor.

## Inputs and boundaries

| Input | Scenario value | Basis / status |
| --- | --- | --- |
| Usable pot energy per charge | 0.25 kWh | Unmeasured prototype target in [README](README.md); not stored PCM energy |
| PV and cartridge | 200 Wp; 2.5 kg erythritol | Unvalidated design; four peak-sun-hours gives up to 0.8 kWh nominal PV/day, **not** 0.8 kWh food heat |
| LPG lower heating value | 46 MJ/kg | Approximate engineering assumption; verify local fuel composition |
| LPG-to-pot efficiency | 55% | Explicit comparison assumption; field-measure actual stove and meal |
| Direct LPG combustion emissions | 3 kg CO2/kg LPG | Rounded scenario factor; excludes upstream LPG emissions |
| Displaced events per active household per year | Low 100 / base 200 / high 250 | Scenarios after missed charges, stove stacking and noncompatible high-heat recipes; each replaces 0.25 kWh pot heat from LPG |
| Retail LPG and PV electricity | $1/kg LPG; zero marginal purchased PV electricity | Illustrative local price assumption, **not** a guarantee of free solar hardware or maintenance |
| Device cost and life | $120 cooker/cassette target; $220–260 dedicated-PV installed goal; ≥500 cycles target | Unverified; one cycle per displacement event gives 2.5 years at 200 events/year if 500 cycles are achieved; replacement and other upkeep extra |
| Scale | Active households using one cassette each, not units sold | 1 million / 10 million are hypothetical successful users, not market forecasts |

## Method

For `D` actually displaced small-meal events/year:

- Pot heat = `D × 0.25 kWh`; LPG avoided = `D × 0.25 kWh × 3.6 MJ/kWh ÷ (0.55 × 46 MJ/kg)`.
- Direct combustion CO2 avoided = `LPG avoided × 3 kg CO2/kg`; gross operational difference only. Fuel expenditure avoided = `LPG avoided × $1/kg`.
- Do **not** credit the full energy content of a cassette, assume all 365 days are usable, or treat LPG substitution as measured household-air-pollution improvement.

| Per active household annually | Low (100 events) | Base (200 events) | High (250 events) |
| --- | ---: | ---: | ---: |
| Heat delivered to pot | 25 kWh | 50 kWh | 62.5 kWh |
| LPG not burned, scenario | 3.56 kg | 7.11 kg | 8.89 kg |
| Direct combustion CO2 not emitted, scenario | 10.7 kg | 21.3 kg | 26.7 kg |
| Avoided LPG purchase at $1/kg | $3.56 | $7.11 | $8.89 |

Base case scaled linearly, **not** a global adoption forecast:

| Active households | LPG not burned/year | Direct CO2 not emitted/year | Fuel purchases avoided/year |
| ---: | ---: | ---: | ---: |
| 100-household pilot | ~0.71 metric tonnes | ~2.13 metric tonnes | ~$711 |
| 1 million | ~7,115 metric tonnes | ~21,344 metric tonnes | ~$7.11 million |
| 10 million | ~71,146 metric tonnes | ~213,439 metric tonnes | ~$71.15 million |

## Interpretation and falsification

This is a **small** fuel saving against $220–260 dedicated-PV installed capital plus cartridge replacement, kiosk labor, maintenance and financing. At the assumed $1/kg LPG price, fuel savings alone cannot justify the purchase without a very different measured meal size, price or benefit stream; no claim of economic competitiveness follows. If charged on a fossil-heavy grid, the electricity emissions must also be deducted; PV manufacturing, stainless/insulation manufacture, transport and end-of-life emissions must be amortized over measured lifetime before claiming **net CO2e**. Thus the table is direct CO2 only, not net greenhouse-gas abatement, and avoids an unsupported CO2e claim.

For households otherwise burning biomass, count an event as displaced only after weighing baseline and follow-up fuel and recording stove stacking, rather than transferring the LPG conversion factor. Collect personal and kitchen PM2.5/CO before and after, food-core temperatures, burn incidents and time spent gathering fuel; health outcomes, deaths avoided, and hours saved are **not quantifiable yet**. These may be the strongest eventual benefits, but zero measurement means no claimed numerical benefit. Pilot failure conditions include unsafe transport, undercooked meals, insufficient useful pot heat, high repair cost, and seasonal charge shortages.
