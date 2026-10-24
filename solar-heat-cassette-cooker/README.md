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
