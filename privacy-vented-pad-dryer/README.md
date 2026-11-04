# Privacy-Vented Pad Dryer

**Author: jayis1**
**Status: concept; no prototype or health efficacy established**

## Problem

Reusable menstrual pads require washing with soap and clean water, then complete drying in a private place before reuse; UNICEF notes that menstrual products are one option among several, not a universal replacement for disposable products or cups.[1] Privacy, water and soap access remain barriers for millions of schoolgirls; a drying device cannot solve those upstream constraints.[2] Damp folded pads in a humid room can remain uncomfortable and difficult to manage discreetly. The design addresses drying access, not infection diagnosis or sterilization.

## Solution

The **Privacy-Vented Pad Dryer** is a lockable, nontransparent, passively ventilated cabinet for **already washed** reusable pads. A shallow black-painted recycled-aluminium solar air collector, mounted outside the private compartment, warms *incoming air* without putting the pads on display. A screened lower inlet, separated vertical cotton-pad clips, and a screened high exhaust create a buoyancy-driven flow; a hinged roof blocks rain and direct sightlines. The removable slatted tray catches drips. A mechanical humidity-reference card in the exhaust and a removable dry reference swatch cue an operator to check the thickest pad by touch and mass; the card is **not** a microbial or sterility indicator. Optional small 5 W solar PV fan helps in humid/cloudy weather but must never be required to open the door or allow safe access.

**Design target, untested:** four 30 g dry-mass pads, each loaded with 30 g of retained wash water, reach ≤5% additional water mass (≤1.5 g/pad) in ≤6 hours at 25–35 °C ambient, 50–70% relative humidity and at least 500 W/m² midday solar irradiance, while pad-contact air stays <45 °C. At 90% humidity or without sun, users must expect longer drying or choose an alternative; the device must not imply readiness merely because time elapsed. These limits are hypotheses to test against indoor shade drying at the same site, not achieved performance. No disinfectant chemicals or UV exposure are proposed.

## Key Innovation

Solar air dryers and private ventilated drying bags already exist. The proposed advance is a **privacy-preserving, repairable air path with an observable dry-reference check and explicit no-ready state in unfavorable weather**, rather than a claim of new solar physics. Unlike the repository's solar steam waste quarantine, which processes clinical waste with a validated thermal exposure, this cabinet handles user-washed fabric and makes **no disinfection claim**. Unlike the magnetotactic microplastic scavenger, it does not filter washing effluent. A comparative trial must establish whether the integrated arrangement adds useful drying speed and user acceptance over a screened line or simple ventilated bag.

## Target Cost

**Unquoted planning target:** US$18 ex-workshop per cabinet at 10,000/year in 2038, before tax, delivery, installation, pad supply, washing water, soap, or labour: recycled-aluminium collector US$5; opaque recycled-PP shell and roof US$6; stainless clips/screens US$2; moisture-resistant card, seals and reference swatch US$2; fabrication and inspection US$3. Optional PV fan adds an estimated US$10–15 and must be independently serviceable. A locally made shell may lower transport expense, but neither price nor durability has supplier quotes. Budget a replacement card/swatch and cleaning as recurring costs, not zero-maintenance claims.

## Impact

A pilot of 100 consenting users could compare drying completion, user preference, water use, and maintenance over a wet and dry season. A **planning capacity** of 10,000 cabinets × four pads per six-hour batch equals at most 40,000 pads per batch under test conditions; actual reach, avoided damp reuse, school participation and health outcomes are **unknown**. Pads remain an optional choice and should not displace other preferred menstrual products. This device can support privacy and reuse only where clean washing water, soap, private facilities and acceptable pads are already available.[1]

## Safety, maintenance and validation

- **Faults:** Blocked insect screens or packed pads reduce airflow; a damp reference swatch and still-wet pad reveal this. Clean screens weekly and space pads so air reaches both faces. A detached hose/fan wire or power loss reduces drying speed, but the passive vent remains open; never claim completion from a timer.
- **Heat, weather, and misuse:** Shade/vent the collector if measured pad-contact air exceeds 45 °C or fabric-label limits. Rain intrusion or a wet tray means rewash if contaminated and dry elsewhere. Keep the roof mechanically latched against wind, with rounded edges and no hot surface reachable by children. The cabinet is for external reusable pads only, not internal menstrual cups, wounds, food, or drinking water.
- **Hygiene and end-of-life:** Clean tray and clips after each batch; inspect for visible mold or corrosion monthly, and replace damaged parts locally. Do not reuse a pad that is damp, visibly soiled, odorous, or beyond its manufacturer's care instructions. Recycle aluminium and PP separately where available; retain cards/screens out of waterways. A shared cabinet needs individual labeled clips and user-approved privacy arrangements, without names logged electronically.
- **Validation gate:** Test 30 units against shaded ventilated-line controls across two seasons, logging pad dry/wet mass, ambient and pad-contact temperature/RH, airflow and weather at 30-minute intervals. Require ≥90% of qualified test batches to reach the above moisture target within six hours, zero pad-contact excursions above 45 °C, no rainwater ingress, and no statistically worse user-reported privacy than controls before a larger pilot. Independent hygiene review is required before any claim of reduced infections; no such claim is made here.

## How It Works

After washing with soap and clean water according to the pad maker's instructions, the user squeezes out excess water and hangs up to four pads by their edges, with both faces exposed and the absorbent cores separated. Sun heats the black aluminium collector *outside* the opaque cabinet. Incoming air passes a screened, baffled lower opening, warms in the collector, rises past the pads as water evaporates, and exits through a high, sightline-baffled screen. The roof sheds rain while leaving the exhaust open. The dry-reference swatch and humidity card are prompts to inspect—not automatic completion sensors. For validation, weigh each pad against its own clean, fully dry reference mass; at the proposed 30 g dry mass, ≤1.5 g residual added water corresponds to ≤31.5 g measured mass. A household user without a scale must not treat a card color or six-hour timer as proof of that threshold: if the thickest layer remains damp, dry it longer or use a clean alternative. Neither heat nor airflow disinfects the fabric.

## Technical Architecture

The passive stack has four serviceable assemblies: (1) a black-coated, shallow recycled-aluminium solar air collector, with no pad contact; (2) an opaque recycled-polypropylene shell with light-baffled intake/exhaust, insect screens, latch, and rain roof; (3) stainless clips and a removable slatted drip tray, accessible for cleaning; and (4) a replaceable reference swatch and exhaust humidity card. The only optional electrical subsystem is a separately serviceable 5 W PV-powered fan on the air path; it cannot be needed for door release or ventilation. The physical data flow is ambient air → collector → spaced, washed pads → exhaust, with wash drips into the tray. The human decision flow is reference check → inspect the thickest pad → keep drying or remove it; no camera, wireless telemetry, user registry, or automated sterility verdict. Prototype drawings must size vents and baffles by measured flow under full loading, and isolate any fan wiring from condensate and wet hands.

## Performance Benchmarks

No prototype measurements or verified market-best comparator figures exist. The following are **test specifications**, not demonstrated improvements; compare all devices with the same four 30 g dry-mass pads, 30 g retained water per pad, 25–35 °C ambient, 50–70% RH, and measured irradiance. Weigh each pad before wetting, after wetting, and after each interval; run matched shaded ventilated-line and opaque screened-rack controls at the same site across two seasons. Report median, 90th percentile, failures and sample counts, including 90% RH and cloudy-day results separately.

| Metric | Proposed cabinet target (unvalidated) | Current comparator state |
| --- | --- | --- |
| Residual added water | ≤1.5 g per pad (≤5% of 30 g dry mass) in ≥90% of qualified batches | Unknown until matched line/rack trials; use the same mass endpoint |
| Cycle time | ≤6 h in qualified sunny conditions; no promise in wet/cloudy weather | Measure time to the same mass endpoint, not merely dry-feeling surfaces |
| Pad-contact air | <45 °C and below any lower fabric-care limit | Log the same temperature on controls; reject damaged fabric |
| Fan electricity | 0 Wh passive; ≤30 Wh per six-hour cycle if the optional 5 W fan runs continuously | Measure plug-in alternatives at the same moisture endpoint; PV output is weather-dependent |
| Privacy and maintenance | No direct pad sightline at ordinary approach angles; screens cleanable weekly | Test silhouettes, noise, access, and cleaning time against screened-rack controls |

The nominal batch removes 114 g of water to reach the target; using an *illustrative* latent heat of 2.4 MJ/kg gives about 76 Wh of evaporation heat before collector and ventilation losses. A hypothetical 0.25 m² collector exposed to 500 W/m² for six hours intercepts 750 Wh of sunlight, **not** 750 Wh of usable heat; shading, losses, humidity, airflow, and variable irradiance can erase the margin. These values are sizing arithmetic, not performance evidence. Validate the collector area and temperature with instrumented prototypes before specifying it for manufacture.

## Deployment Scenarios

- **Private household courtyard:** Mount the collector in sun and the opaque cabinet near a private washing point, with exhaust directed outdoors and the latch accessible to the pad owner. No fan is required; users need a clean backup pad for rainy days.
- **Shared school washroom:** Place several cabinets behind a consent-based privacy screen, separate labeled clips without recording names, and assign tray/screen cleaning. Staff should not infer health or attendance benefits from use counts; privacy, wash water, soap, and product choice come first.
- **Humid clinic or community laundry:** Trial the optional isolated PV fan only if intake and exhaust can remain unobstructed and electrical splash protection is verified. Log failed wet-weather cycles and provide conventional ventilated drying as a fallback rather than increasing heat indiscriminately.

## Risks & Mitigations

- **Hidden moisture or contamination:** A dry surface, swatch, or card cannot certify a pad core or microbial safety. Require pad-specific mass checks in trials, user inspection in ordinary use, validated washing instructions, and explicit no-ready guidance in damp weather. Clean clips and tray between users.
- **Heat, rain, and blocked vents:** Test at full load, blocked-screen and fan-failure conditions; add a passive overtemperature vent/shade path, inspect rain ingress, and set the pad-contact limit below both 45 °C and the manufacturer's lower care limit. A closed privacy box must never seal the air path.
- **Electrical, access, and privacy failure:** Keep the passive version wholly unpowered. For the optional PV fan, independently assess insulation, strain relief, splash/condensation exposure, and safe unplugging; do not imply certification. Test silhouettes, shadows, sound, lock accessibility and cleaning burden with consenting users, including users with limited dexterity.
- **Cost and end-of-life:** The US$18 estimate excludes installation, soap, water, replacement parts and labor. Obtain supplier quotes and local repair/recycling pathways before projecting savings or uptake. This design is only for compatible reusable external pads, never disposables.

## Vision for 2050

If seasonal trials demonstrate reliable core drying, safety, meaningful privacy, and affordability, repairable cabinets could sit beside washing facilities as one optional piece of menstrual infrastructure. A 2050 network would be locally made and maintained, with public test protocols and weather-specific no-ready guidance—not a universal replacement for other products or a substitute for water, soap, and private facilities. Uptake, avoided waste, and health outcomes remain conditional on measured behavior and independent evaluation.

## Sources

[1] https://www.unicef.org/supply/menstrual-hygiene-products — UNICEF menstrual hygiene products
[2] https://www.unicef.org/press-releases/10-fast-facts-menstrual-health-schools — UNICEF menstrual health in schools
