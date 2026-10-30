# Batch-Locked Gasifier Cooktop

**Author: jayis1**

**Status: Research concept (TRL 2); not a certified clean stove**

**Category: Clean Cooking & Universal Basic Services / Household Air Pollution**

## Problem

About 2.1 billion people cook with open fires or inefficient stoves using polluting fuels; WHO estimates household air pollution caused 2.9 million premature deaths in 2021.[1] A household cook preparing an evening meal may not have affordable electricity, LPG, or sufficient sunlight. Forced-draft biomass gasifiers already exist, but their emissions depend strongly on ignition, fan setting, fuel and especially how a hot bed is refuelled: tests on one pellet gasifier found refuelling was the most variable, high-emission operating condition.[2] A stove that is clean only during a carefully managed steady burn does not solve the household exposure problem.

## Solution

A **single-batch, repairable cooktop** accepts a removable perforated 304-stainless fuel basket holding a *proposed maximum* 0.5 kg of dry, locally sourced, size-screened biomass pellets. A 12 V, nominal 3 W brushless fan splits air between the lower char bed and an insulated upper secondary-combustion ring; turbulent mixing burns released wood gas under a lidded pot. A refractory clay liner retains heat, an expanded-metal pot support resists tipping, and a captive ash drawer receives cool residue. These are conventional gasifier principles, not a new fuel or a claim of zero smoke.

A mechanical **batch gate** keeps the refuelling opening covered while the basket is seated. A heat-rated bimetal element and a spring latch block basket release while the chamber is hot; a separate flame-view port helps the cook confirm extinction. Neither indicator is a CO sensor. The cook plans a batch for the meal, uses approved ignition material *without kerosene*, allows the fire to burn down, and waits for a verified cool state before changing the basket. A replaceable 12 V battery and a separately fused solar or grid charger supply the fan; no mains connection is required while cooking. If the fan stops, fuel continues to smoulder: the response is to stop feeding fuel, ventilate, keep people away, and follow the locally tested extinguishing procedure—not to assume the gate makes the air safe. An independent household CO alarm and appropriate ventilation remain essential.

## Key Innovation

Forced-draft gasifiers, batch loading and thermal latches are all prior art. The proposed research contribution is a **serviceable batch-and-cooldown interface that makes hot-bed topping-up mechanically difficult without claiming the fire itself is fail-safe**. Test it against the *same stove without the gate*, as well as against the household's current method. This differs from the repo's [Solar Heat Cassette Cooker](../solar-heat-cassette-cooker/) (stores solar heat and burns no fuel), [Phononic Thermoelectric Harvester](../phononic-thermoelectric-harvester/) (recovers electricity from an existing fire), and [Kiln Draft Balancing Retrofit](../kiln-draft-balancing-retrofit/) (industrial brick-kiln exhaust rather than household cooking). Its value depends on whether cooks can actually complete local recipes without defeating the latch or stacking another smoky stove.

**Unverified design envelope:** nominal 0.5 kg/batch of characterized dry pellets, ≥25% fuel-to-pot thermal efficiency over the full start/burn/shutdown cycle, ≤3 W fan draw over a one-hour batch, and ≥1,000 latch cycles without a stuck-open failure. Do not assume a universal moisture threshold or reliable emissions from mixed fuels. The development challenge over 10–20 years is an affordable, contamination-resistant latch and repair system that measurably reduces *real-world* high-emission events; combustion and fan hardware themselves are established.

## Target Cost

**Unquoted 2038 ex-factory goal at 100,000 units/year:** US$85 per cooktop: US$23 stamped basket and steel housing, US$15 refractory and insulation, US$17 fan and wiring, US$12 gate/latch/thermal indicator, and US$18 assembly and factory test. A battery/charger is an additional *estimated* US$30–50; trained distribution, ventilation assessment, independent CO alarm, freight, taxes, replacement fans, fuel preparation and maintenance are excluded. If the cooker lasts five years, the bare capital goal is US$17/year before those exclusions. The household must compare actual local delivered fuel and service costs with LPG/electricity and other approved clean alternatives; no proprietary pellet or subscription is intended. A cooperative could stock standardized replacement baskets and fans, but the factory cost is not an installed price.

## Impact

For an **illustrative engineering budget**, 0.5 kg of qualified pellets at an *assumed* 15 MJ/kg lower heating value contains 7.5 MJ. If the unverified 25% full-cycle pot efficiency is achieved, the pot receives 1.875 MJ or approximately 0.52 kWh; a 3 W fan for one hour draws 0.003 kWh. Neither figure proves a recipe can be cooked or that combustion emissions meet WHO clean-cooking limits. Ash and char mass, carbon monoxide, PM₂.₅, battery replacement and any pellet-processing energy must be measured and accounted for, not described as zero waste. Coal, painted wood, plastics and treated timber are excluded fuels.

**Validation gate:** Bench-test at least three eligible local fuels and moisture ranges using ISO 19867-1 methods for whole-cycle PM₂.₅, CO, cooking energy, safety and durability; the ISO field-testing framework evaluates real use, exposure and user practices.[3] In a randomized crossover pilot with 100 consenting households, compare the gated and otherwise identical ungated model over actual meals. Record hot refuelling, bypass attempts, stove stacking, fuel use, personal and kitchen PM₂.₅/CO, burns, time and user acceptability, including startup and shutdown. Targets—not measured results—are ≥80% fewer hot-refuelling events, ≥30% lower *measured personal* PM₂.₅ versus the household baseline with no increase in CO exposure, and ≥90% of intended meals completed without bypass. If the stove cannot meet applicable clean-emission criteria and exposure thresholds, do **not** market it as clean; prioritize electricity, solar, LPG or biogas where feasible.[1]

**Failure and end of life:** Wet fuel, clogged secondary jets, cracked liner, jammed latch, depleted battery, an open gate or missing ventilation can worsen smoke or CO. A latch failure must be conspicuous on pre-use inspection; retire or repair the unit rather than defeat the gate. A hot chamber stays guarded until cool, but a latch cannot prevent leaks, CO poisoning or unsafe operation. Train local repairers to clean jets and inspect the fan, bimetal and battery monthly; measure replacement intervals in field trials. Recycle steel, segregate battery waste and manage ash according to fuel analysis and local rules. No microphone, camera, identity record, network connection, surveillance or control function is included. Product safety, indoor-air and electrical requirements need independent local approval before deployment.

## How It Works

The cook sizes a meal to one 0.5 kg basket of screened, characterized dry pellets. Ignition establishes a downward-moving conversion front; limited primary air releases combustible gases, while fan-fed secondary air mixes and burns them above the bed. Heat crosses the pot base, with the refractory liner limiting side losses. The gate prevents adding fuel mid-cycle, when disturbing a hot bed can produce a smoke pulse; this is a behavioral intervention, not an emissions filter. The basket remains inaccessible until a separate cooldown check permits release. One hour is a *test assumption*, not a guaranteed burn duration: a long simmer might need another cooled batch or another cooking method. Extinction in the view port is not proof of safe CO levels or cool char. Emergency interruption, char containment and restart require supervised hazard testing; closing all air on a hot bed could increase CO rather than make it safe.

## Technical Architecture

The fuel path is basket → primary-air char bed → upper gas/secondary-air mixing ring → pot/flue; the electrical path is fused battery → 12 V fan. No network or firmware controls a safety function. The separate mechanical path is basket seat → captive gate → spring latch → heat-responsive bimetal; a visible release state is proposed, but the latch must not be represented as a calibrated thermometer. The combustion chamber is *not* a pressure vessel: its exhaust must remain open and draft obstruction must be tested, not countered by sealing the gas path. Instrumented prototypes need thermocouples, airflow and CO/PM₂.₅ sampling for diagnosis; the production concept does not silently assume those sensors exist. A power-loss condition can leave smouldering fuel behind a locked gate, so fault handling must be validated with an external CO alarm and locally appropriate ventilation before any occupied-space trial.

## Performance Benchmarks

| Metric and boundary | Current evidence / comparator | Unverified design target |
| --- | --- | --- |
| Full-cycle fuel-to-pot efficiency, qualified pellets, startup through shutdown | No measurement for this design. An ISO 19867-1 laboratory study compared a pellet semi-gasifier, fan stove and three-stone fire across high/medium/low power; its results cannot be transferred to this geometry or household use.[4] | ≥25% at 0.5 kg/batch; measure with the same pot and fuel in gated, ungated and household-baseline arms. |
| Delivered cooking heat | No prototype measurement; baseline varies by recipe and pot. | 1.875 MJ/batch (0.52 kWh) only if assumed 15 MJ/kg lower heating value and 25% efficiency hold; see engineering budget above. |
| Electricity and mechanical life | Neither fan draw nor latch life has been measured here. | ≤3 Wh per nominal one-hour batch; ≥1,000 thermal latch cycles without stuck-open failure. |
| ISO full-power-range CO tier (mg/MJ delivered basis) | In one published ISO 19867-1 lab comparison, a commercial pellet stove scored Tier 5 versus Tier 1 for a three-stone fire; tiers are device/fuel/protocol-specific, not household exposure.[4] | No tier assigned until replicated full-cycle testing; compare measured mg/MJ delivered to the relevant ISO 19867-3 thresholds. |
| Exposure and cooking behavior | WHO does not classify an untested biomass device as clean; lab emissions alone do not establish household exposure.[1] | Pilot: ≥80% fewer hot refuellings, ≥30% lower personal PM₂.₅ versus household baseline, no CO increase, ≥90% meals without bypass. |

ISO 19867-1 whole-cycle PM₂.₅ and CO in mg/MJ delivered and applicable voluntary tiers must be established with replicates, fuel moisture and pot recorded; **there is no measured emissions tier yet**. The published comparator includes startup and shutdown at each power level and reports protocol-dependent efficiency including char credit, a reminder not to equate a single high-power result with real-meal performance.[4]

## Deployment Scenarios

- **Rural pellet cooperative:** A trained cooperative screens and dries locally sourced, uncontaminated residues, distributes fuel in moisture-protected packaging, stocks fans and baskets, and installs only after a ventilation and CO-alarm assessment. Compare total delivered fuel cost and cooking time with existing methods.
- **School or community kitchen research pilot:** Supervised cooks use multiple units for discrete tasks while a separate approved appliance handles long simmering. Log batch timing, smoke/CO around startup and cooldown, burns and food throughput; do not extrapolate household safety from an open-sided kitchen.
- **Off-grid household evaluation:** In consenting homes with adequate ventilation, a replaceable battery charged from solar or grid runs the fan. Monitor stacking, skipped meals and unsafe relights against a matched ungated stove; withdraw the unit if exposure worsens. None of these scenarios is a recommendation for indoor use before independent approval.

## Risks & Mitigations

CO can peak during startup, smouldering, fan failure or shutdown even when the gate is locked; independently monitored exposure, ventilation review and a tested emergency response are prerequisites. A jammed-open or defeated latch permits dangerous refuelling, while a jammed-closed one can frustrate emergency response: use a captive guarded mechanism, observable inspection state and destructive-test-free service replacement, then cycle-test it with ash, heat and corrosion. Never make the exhaust airtight to compensate for a failed gate. Blocked jets, wet fuel and contaminated residues can increase PM₂.₅ and toxic ash; qualify local feedstocks and reject untested waste. Guard hot surfaces and pot stability, retain hot char until a validated cool state, and supply spare fans and batteries. Fuel logistics and stove stacking may erase modeled savings; track sustained use rather than sales. There is no certification, verified indoor-emission limit, carbon credit, or validated safe shutdown procedure yet.

## Vision for 2050

If independent testing establishes safe exposure and cooks prefer the batch workflow, locally repairable stoves could be one transitional option where clean electricity, biogas or LPG remains inaccessible. Cooperatives could standardize safe fuel preparation and spare parts without locking households into a proprietary cartridge. A 2050 success would mean measured sustained use and lower personal exposure—not merely millions of devices sold. Where truly clean options become affordable, this biomass concept should yield to them, not preserve a market by weakening the definition of clean cooking.

## Sources

[1] WHO, *Household air pollution* (16 December 2025): https://www.who.int/news-room/fact-sheets/detail/household-air-pollution-and-health

[2] Published gasifier operating-condition study, NSF Public Access Repository: https://par.nsf.gov/servlets/purl/10391136 — prior-art evidence on refuelling variability, not a result for this design.

[3] ISO 19869:2019, *Field testing methods for cookstoves*: https://www.iso.org/standard/66521.html

[4] *Cookstove emissions and performance evaluation using a new ISO protocol and comparison of results with previous test protocols*, open-access laboratory study: https://pmc.ncbi.nlm.nih.gov/articles/PMC8855438/ — distinct appliances and fuels, not measurements of this concept.
