# Self-Verifying Radon Vent

**Author: jayis1** · Concept (TRL 2) · 2026-10-28

A repairable, offline sub-slab radon vent that treats indoor exposure reduction—not just a running fan—as the acceptance test. This is a research concept, not an approved mitigation system or a substitute for a qualified installer.

## Problem

Radon is an invisible radioactive soil gas and a leading cause of lung cancer; WHO attributes an estimated 3–14% of lung cancers in a country to radon, depending on exposure and smoking prevalence.[1] A working fan or a pressure gauge cannot alone prove that a resident's exposure has fallen. Indoor concentration changes with weather, building use and season; WHO recommends measurements lasting at least three months to estimate the annual mean.[1] Existing mitigation needs periodic inspection and retesting, which can be missed when maintenance is unaffordable or distant.[2]

## Solution

For an eligible slab-on-grade or basement home with *measured elevated radon*, a qualified contractor installs a sealed sub-slab suction pit, solvent-welded PVC or other code-approved gas-tight riser, outdoor-rated variable-speed centrifugal fan, weather-protected discharge above the roof according to local code, and a serviceable wind cowl. Soil-gas extraction keeps pressure under the slab below the occupied room's pressure, intercepting radon before it enters; suction is not applied to indoor air. Soil depressurization, passive vents, fans and radon testing are established practice, not inventions claimed here.[1][2]

A low-voltage controller compares a sealed remote sub-slab pressure tap against indoor pressure, checks fan current and a duct-flow witness, and logs measurements locally. The cowl may assist extraction when wind is favorable, but the fan stays active at a verified minimum speed; it never assumes wind alone is adequate. The installer tests pressure-field reach at remote slab points and checks for combustion-appliance backdrafting. An independently verified indoor radon detector in the lowest occupied level supplies a slower exposure trend; a separate accredited long-term radon test determines whether mitigation actually meets the applicable local standard. No microphone, camera, occupancy record or cloud service is needed.

**Proposed design gates, not achieved results:** for suitable houses, demonstrate negative sub-slab-to-room pressure at all installer-selected remote test points across a seasonal range, no duct leakage or indoor backdrafting, and an indoor long-term average below the locally applicable action/reference level. Aim for **<100 Bq/m³** where feasible, consistent with WHO's recommended national reference level, but do not treat 100 Bq/m³ as a guaranteed safe threshold; WHO notes 300 Bq/m³ as a maximum when 100 is not achievable under national conditions.[1] If the baseline is already below the local level, do not install merely to meet a product target. Homes with crawlspaces, highly impermeable soils, multiple foundations or radon from well water need a separately engineered solution.

## Key Innovation

The proposal is a **two-timescale, fail-visible verification loop**: fast pressure-field and flow checks catch hardware faults, while an independently calibrated indoor radon trend and scheduled accredited tests detect failures that pressure cannot reveal. A wind cowl and variable-speed fan may reduce energy use only when measured pressure-field reach is preserved. EPA already recommends checking warning devices and retesting homes at least every two years; continuous radon monitors and active/passive vents also exist.[2] The unproven integration hypothesis is that a repairable, local-only controller plus paired measurements will detect unsafe *apparent success* sooner and with less wasted fan energy than a maintained conventional active system. No patent novelty or superior performance is asserted.

On pressure reversal, blocked/iced duct, leaking joint, stalled fan, bad sensor reference, lost indoor detector data or failed power, the controller shows a persistent red **UNVERIFIED—TEST RADON / CALL INSTALLER** indicator and raises a local audible alarm that a resident can silence without clearing the fault. It increases fan speed only within installer-approved pressure and noise limits; it never represents that a warning or higher speed has made the home safe. A mechanical U-tube or equivalent independent pressure witness remains readable without electronics. A failed controller cannot shut off an otherwise working fan: the fan defaults to a fixed commissioned safe speed when line power is available. On prolonged outage, residents require alternative mitigation advice and a professional inspection, not a claim that the cowl alone protects them.

## Target Cost

**Planning target in 2038 US dollars at 10,000 units/year, not a quote:** US$350–600 ex-factory for fan/cowl, controller, pressure taps, local display and one replaceable indoor monitor; US$900–2,000 installed *in addition to* diagnosis and any foundation repairs, subject to site and code. A cooperative or housing authority is the intended buyer; tenants should not be charged for unverified protection. Budget US$60–120/year for inspection, sensor comparison and consumable replacements, plus electricity and accredited post-installation and periodic radon tests at local prices. A target mean fan draw of **8–25 W** implies **0.192–0.600 kWh/day** at continuous operation; actual demand must be logged and compared against a properly sized conventional active vent in the same building. Fan, sensors and seals are replaceable; PVC, electronics and battery (if optional) go to appropriate recycling streams, not household soil. Wind-energy savings and service life remain unknown.

## Impact

A pilot of **100 homes** with baseline radon above the local action level would compare this device against professionally installed, maintained conventional active sub-slab depressurization. Prespecified outcomes: paired accredited radon tests before installation, after commissioning, and for at least one three-month period in both cold and warm seasons; time above the local reference level; time from induced fault to visible warning; measured kWh/day; total installed and service cost; and combustion safety. A planning scale of **100,000 eligible installations** represents at most 100,000 homes served, not cancers prevented or homes made safe. Fewer missed failures and lower exposure are hypotheses requiring independent, weather-adjusted trials.

The 10–20-year path is bench fault injection (years 1–3), controlled multi-home field trials including low-wind winters and power failures (years 4–8), then local code review, certification and independent replication (years 9–15). Stop if the cowl reduces pressure-field coverage, savings do not outweigh added maintenance, radon remains above the applicable threshold, alerts fail silently, or any installation causes backdrafting. Retest after building alterations and per local rules; the device does not replace accredited measurements or qualified mitigation practice.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/radon-and-health
[2] https://www.epa.gov/radon/how-do-i-know-if-my-radon-mitigation-system-working-properly
