# Solar Heat Cassette Cooker

**Author: jayis1. Status: research concept, not a certified cooking appliance.**

## Problem

Around **2.1 billion people** still cook with polluting fuels and technologies; WHO estimates **2.9 million deaths attributable to household air pollution in 2021**.[1] An off-grid household cooking its evening meal cannot necessarily use a midday solar cooker or rely on an intermittent grid. Improved biomass stoves still burn fuel indoors. The primary user here is a household cook who can charge a cooker in daylight and wants a small evening meal without smoke, not a restaurant requiring continuous high heat.

## Solution

A **removable, sealed thermal cassette** stores daytime photovoltaic electricity as heat in about **2.5 kg of erythritol** contained within a welded stainless-steel vessel. A **200 Wp PV panel** powers a low-voltage resistive heater through a temperature-limited charge dock; no electrochemical battery is needed for cooking. At mealtime, the user slides the cassette into a double-wall insulated, lidded pot base. A keyed mechanical shutter exposes the hot thermal interface only after the cassette is latched; an aluminum spreader and dry, spring-loaded thermal contact conduct heat into the pot. There is no fuel, combustion exhaust, radio, or user tracking. A solar panel is optional where reliable clean grid power exists.

The limited heat budget suits boiling or simmering modest meals, **not frying, a large-family banquet, or a guaranteed pressure-cooking cycle**. The pot lid must vent normally. A cold, incompletely charged cassette means use a separate clean backup where available; never infer food safety from elapsed time alone. A mechanical temperature indicator tells the user whether the cassette is charged enough for the planned recipe, but food temperature and adequate cooking remain the user's responsibility.

## Key Innovation

Neither solar electric cooking nor erythritol phase-change storage is new: published cooker experiments already report about **0.4 kWh thermal release from 2.5 kg of erythritol** under their tested cooling conditions.[2] The proposed advance is the **interchangeable, inspectable heat cartridge and charge/serve split**: a standardized shared daytime dock can charge multiple repairable cartridges, while a passive interlock prevents contact with the hot transfer face during transport. Its value over a fixed solar cooker or a battery-powered electric pressure cooker must be established by reliability and cost trials, not assumed.

Design targets for a first validated prototype: **0.25 kWh useful heat into a pot per full charge**, **≤6 h between charge and serving**, **≤0.06 kWh standby loss over those 6 h**, **≥500 charge cycles** before cartridge retirement, and an accessible surface below **50°C** in ordinary transport. These are unverified engineering targets. The PCM melts near **118°C**; realistic heat-transfer losses mean it may not hold food at a boil throughout discharge. Qualification must map heat delivered against pot temperature rather than treating latent heat as fully usable. Compared with this repo's [Phononic Thermoelectric Harvester](../phononic-thermoelectric-harvester/), which takes a few watts *from* a burning stove, this device tries to replace the cooking fire; unlike the [Radiative-Adsorption Refrigerator](../radiative-adsorption-refrigerator/), its stored heat is delivered to food rather than used to cool it.

## Target Cost

**Unvalidated US-dollar goal for 2035 at 100,000 cookers/year:** US$120 for the cooker and cassette (PCM and sealed vessel $28; insulation, latch and pot interface $35; heater/dock electronics and thermal protection $32; assembly and test $25). A dedicated **200 Wp PV panel, mounting, wiring and installation** add an estimated **US$100–140**, for **US$220–260 installed** before taxes, finance, transport, replacement cassettes, and site-specific electrical work. A shared dock might amortize charging hardware across households, but availability and fair access must be measured. Actual procurement quotes, ingress testing, food-contact approval, replacement rates, and local affordability could invalidate this price. The first 1,000 trial units would need subsidy or cooperative financing and local appliance-service partners; no monopoly consumable or subscription is intended.

## Impact

A single daily 0.25 kWh useful-heat discharge is **not a complete household energy supply**. As a sanity check, heating **1 L water from 20°C to 95°C** takes about **0.087 kWh** ideally (`1 kg × 4.18 kJ/kg/K × 75 K`), leaving roughly **0.16 kWh** for food and heat loss if the useful-heat target is met. Assuming 4 peak-sun-hours, a 200 Wp panel receives about **0.8 kWh/day nominal electrical output** before weather and system losses; charging plus storage and pot-transfer losses must be metered separately. A cloudy day or larger meal defeats the budget. The published 0.4 kWh figure is a reference point, **not a validated output for this cartridge**.[2]

In a 100-household trial, compare total fuel use, kitchen PM2.5/CO, fully cooked meals, user time, burn incidents, repair time, and costs against each household's existing stove and against a conventional electric cooker on the same supply. Measure **stove stacking**: health gains require sustained displacement of polluting combustion, not merely an additional gadget. At one million successful daily users the device could provide one million small clean cooking events a day; avoided deaths or emissions cannot be inferred without measured fuel displacement and exposure. Prototype and certification over the next **10–20 years** are plausible using existing materials; scale-up is conditional on field durability, affordability and adoption.

**Limits and safety:** Erythritol can degrade with excessive temperature and cycling; qualification must test decomposition, corrosion, expansion, leakage and food-contact isolation. A thermal fuse and independent thermostat cut charging before overheating; a failed dock remains electrically isolated when unplugged. The sealed cassette needs a pressure-relief design venting away from users inside a secondary containment tray, never into food, plus drop and transport tests. A cracked vessel, faulty latch, missing insulation, or abnormal indicator retires the cartridge immediately. External surfaces, service tools and packaging must meet local burn/electrical safety requirements. Recover stainless steel and aluminum at end of life and assess the PCM for safe local disposal; no promise of zero maintenance. Local cooks must shape ergonomics and recipes before rollout. This is not a substitute for ventilation or food-hygiene guidance.

## Sources

[1] WHO, *Household air pollution*, updated December 2025: https://www.who.int/news-room/fact-sheets/detail/household-air-pollution-and-health — global exposure and 2021 mortality estimates, not a forecast of device benefit.

[2] Osei et al., *Phase change thermal storage: Cooking with more power and versatility*, Solar Energy 220 (2021), 1065–1073: https://www.sciencedirect.com/science/article/pii/S0038092X21002280 — experimental prior art for erythritol storage, not validation of this cartridge, latch or cost.

## How It Works

At midday, a 200 Wp panel feeds a low-voltage, current-limited charge dock. The dock heats the welded stainless cartridge until its roughly 2.5 kg erythritol charge crosses the ~118°C melting region, then its independent thermostat and thermal fuse prevent uncontrolled heating. At dusk, a cook checks the mechanical hot/charged indicator, carries the insulated cartridge by its cool handle, and inserts it into a keyed, stable pot base. Latching opens the shutter; a spring loads a dry aluminum contact against the pot spreader. The lidded pot receives heat as the erythritol freezes. Unlatching closes the shutter before the cartridge can be removed. The cartridge cools before inspection or recharging; no hot cassette should be handled if its shell, latch or indicator is damaged.

The energy ledger is a **design calculation, not a test result**. A good-sun day with four equivalent peak-sun-hours yields up to `0.2 kW × 4 h = 0.8 kWh` nominal PV energy. Allowing an illustrative 50% from nominal PV output to cartridge thermal storage gives **0.4 kWh stored**; the cited experiment's 0.4 kWh release is a separate result on a different apparatus, not proof of this budget. The latent portion alone is about `2.5 kg × 340 kJ/kg ÷ 3600 = 0.236 kWh` (340 kJ/kg is a material-property approximation); the balance would require sensible heating and must be verified over an accessible discharge range. At the six-hour serving limit, **≤0.06 kWh** standby loss and an illustrative **0.09 kWh** pot-interface/unusable-heat allowance leave the **0.25 kWh pot-delivery target**. That is at most 31% of nominal PV energy under these assumptions, and only a small boiling/simmering task; it cannot supply a full day's meals. On a cloudy day, use a separately approved clean backup, not an undercharged cartridge for food that requires sustained heat.

## Technical Architecture

- **Power and charge:** PV wiring, charge controller/current limit, insulated dock and resistive heater; an independent thermal fuse cuts a thermostat failure. A grid-powered dock is possible, but its emissions depend on the grid.
- **Storage and containment:** erythritol inside a welded stainless vessel with expansion space, evaluated pressure relief directed into secondary containment, and replaceable external insulation. The pressure and relief path are engineering work, not a claim that a hermetically sealed hot vessel is safe.
- **Cook interface:** keyed shutter, positive latch, spring contact, aluminum spreader, vented cookware lid and stable anti-tip base. Food contacts the qualified pot, never the PCM; there is no pressurized food vessel.
- **Signals and service:** passive temperature indicator and serialized inspection record, without radio or user tracking. Energy flows panel → heater → PCM → spreader → pot; temperature and latch state govern access, not a software app.

Prior-art PCM cookers already store heat. This proposal's testable distinction is an **interoperable exchangeable cartridge interface**: household docks and a shared daytime charging station should accept the same safely keyed cassette without proprietary refill lock-in. Geometry, thermal contact and inspection tolerances must be standardized before claiming interchangeability.

## Performance Benchmarks

All figures below refer to different devices or test conditions and **are not head-to-head trial results**. Compare the same 1 L water load (20→95°C), 25°C ambient, specified wind and irradiance, six-hour hold and measured energy at the pot in a future controlled test. The ideal water heating requirement is 0.087 kWh before vessel and food losses.

| Metric | This cooker | Comparator / current evidence |
| --- | --- | --- |
| Thermal discharge | **Target:** 0.25 kWh to pot/full charge within 6 h | **Reported prior art:** ~0.4 kWh thermal release from 2.5 kg erythritol under different cooling conditions [2]; not pot heat or a certified benchmark |
| Storage and solar input | **Calculated scenario:** 0.4 kWh stored from at most 0.8 kWh nominal PV/day at 200 Wp, four peak-sun-hours; 0.236 kWh is the approximate latent component | Direct solar box cooker: no off-sun storage unless storage is added; battery/PV electric cooker: electrical storage or contemporaneous power required |
| Hold / lifetime / touch safety | **Targets, unmeasured:** ≤0.06 kWh loss in 6 h; ≥500 cycles; accessible shell <50°C during normal transport | No equivalent measured values for this cartridge; independent burn and cycle tests required |
| Price | **Unvalidated 2035 volume goal:** $120 cooker/cassette or $220–260 with dedicated PV installed | Local LPG, grid electricity and PV+battery prices vary; obtain local lifetime-cost quotes before declaring a winner |

The erythritol melting plateau cannot provide a 180–250°C frying surface. A conventional electric pressure cooker or LPG stove remains preferable for large, fast or high-temperature meals; a fixed solar cooker can be cheaper where daytime-only cooking fits the household. This is a time-shifted small-meal device, not universal fuel replacement.

## Deployment Scenarios

1. **Peri-urban evening meal:** a household with an exposed roof charges its cassette at midday and simmers a small pot after dark. If roofs are scarce, an inspected neighborhood dock charges interoperable cartridges and issues them like returnable bottles. The cook keeps an existing stove for frying and cloudy days; the benefit is fewer smoky small-meal events, not an implausible total stove replacement.
2. **Emergency shelter cluster:** a supervised shared PV array and charging rack schedule cassettes for vulnerable families. Shelter staff screen damaged units and train users on the hot indicator and safe food temperatures. The payoff is a limited smoke-free evening serving when charging conditions permit, without storing combustion fuel inside shelters.
3. **Off-grid school kitchen:** staff charge several cassettes from a sized PV array and use them for small batches of porridge or hot drinks, while a separate certified appliance cooks bulk lunches. Batch count is bounded by array output and the unmeasured 0.25 kWh/pot design target; the gain, if validated, is a modular, repairable supplementary heat source.

## Risks & Mitigations

| Failure or adoption risk | Design response and gate |
| --- | --- |
| Burn, tip-over or child access while the core exceeds 100°C | Keyed shutter, positive latch, guarded handle, anti-tip base and persistent hot indicator; validate shell <50°C target in worst-case transport, and run drop, misuse and child-access tests before distribution. A 50°C surface can still burn on prolonged contact. |
| Hot-vessel expansion, leakage, decomposition and food contamination | Size expansion space and pressure relief from measured thermal cycles; orient relief into secondary containment away from users and food. Thermal fuse plus independent thermostat; retire cracked or leaking units; qualify food-contact pot separately. |
| Charging faults, glare or fire | Electrically isolated low-voltage connectors, overcurrent protection, certified wiring and weatherproof mounts. This PV design has **no concentrating reflector**, hence no concentrator glare, but hot dock parts and electrical fire still need enclosure and tests. |
| Supercooling, insulation failure and inconsistent pot heat | Instrument 500 complete charge/discharge cycles, cold starts and 6-hour holds; compare actual pot energy and temperature against the 0.25 kWh target, and replace units failing inspection. Prevent undercooked food by checking food temperature, not the indicator alone. |
| Cloudy seasons, cost and cooking preferences | Preserve a clean backup, trial recipe coverage with local cooks, publish honest per-meal economics and price spare cassettes transparently. A shared dock only works with measured queue capacity and an open, interoperable cartridge standard. |

## Vision for 2050

If the safety gates, economics and adoption studies succeed, a street could have a daylight charging rack with inspected, interchangeable cartridges that families collect before dinner; homes would still keep other appliances for frying and long rainy spells. The meaningful measure would be displaced polluting cooking events and measured exposure, not the number of cassettes sold. An open interface could let local repair shops compete on service rather than locking households into one vendor. This is a conditional clean-cooking pathway, not a forecast or a claim that a prototype exists.

See the five-stage [roadmap](ROADMAP.md) and the assumption-driven [impact analysis](IMPACT_ANALYSIS.md).
