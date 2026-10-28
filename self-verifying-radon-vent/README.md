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

## How It Works

A qualified installer first measures indoor radon, maps the slab and suction-field reach, and checks combustion appliances. A fan then draws soil gas from a sealed pit through a gas-tight riser to an outdoor discharge positioned under local rules; it does not draw room air through the slab. Remote pressure taps compare slab pressure with the occupied room, while fan current and a duct-flow witness indicate whether extraction is still occurring. The wind cowl is supplemental, never the acceptance test. Pressure thresholds are commissioned per building under representative HVAC settings; wind, moisture and seasonal stack effect can change them.

The local controller records timestamped evidence and distinguishes **extracting**, **fault**, and **unverified** states. A lost sensor, stale radon reading, blocked outlet, fan stall or power loss cannot yield a green status. A line-powered fan defaults to its commissioned fixed speed if the controller fails; a mechanical pressure witness and persistent outage marker remain the independent checks. A replaceable indoor monitor shows a slow trend, but its reading is not proof of protection: a qualified post-installation radon test, followed by periodic retests, determines exposure under the applicable local protocol.[1][2]

## Technical Architecture

- **Gas path:** suction pit → sealed code-approved riser → outdoor centrifugal fan → protected roof discharge. Seal and inspect joints and penetrations; a leak can bypass the suction field or release gas into the building.
- **Evidence path:** remote slab/room differential-pressure taps, duct-flow witness and fan-current pickup → low-voltage local controller → dated log, audible alarm and readable status display. A separate indoor radon detector supplies an independent, slower outcome signal. No cloud or occupancy telemetry is required.
- **Control path:** the fan runs continuously at an installer-approved minimum; speed changes only within the commissioned envelope while remote pressure-field coverage remains demonstrated. A controller or sensor fault reverts to the fixed-speed hardware path and displays **UNVERIFIED** rather than estimating a radon concentration from pressure. Mains failure stops active extraction and must trigger an independent persistent outage indication, such as a supervised battery-backed indicator; this backup is a design requirement, not a built feature.

## Performance Benchmarks

These are proposed acceptance criteria, **not measured prototype results**. Comparators below are published guidance or the existing concept's budget, not matched head-to-head trials. Field performance depends on foundation, soil permeability, weather and HVAC operation.

| Metric and test condition | Current practice / reference | Proposed target and evidence gate |
| --- | --- | --- |
| Radon exposure in lowest occupied level | WHO recommends ≥3 months of measurement to estimate annual mean and a national reference level of 100 Bq/m³ where achievable.[1] | Independently accredited baseline and post-install tests, including ≥3 months in each of warm and cold periods; below the applicable local level, with <100 Bq/m³ an aspiration where feasible, not a safety guarantee. |
| Maintenance confirmation | EPA recommends checking a warning device regularly and retesting at least every two years.[2] | Detect a persistent induced fan-stop or blocked-flow fault locally within 60 seconds in bench testing; radon outcome still requires the longer test. False-alarm frequency to be measured over a 12-month pilot, not assumed zero. |
| Remote suction-field coverage | EPA describes soil suction and above-house discharge, but a warning-device check alone does not measure indoor radon.[2] | Negative slab-to-room pressure at every installer-selected remote point during commissioning and repeat checks across operating conditions; record test-point location and pressure in Pa. |
| Continuous fan electricity | The proposed unit has no measured draw or matched conventional-fan baseline. | Mean **8–25 W** design budget = **0.192–0.600 kWh/day**, metered over all seasons; claim savings only against a correctly sized conventional vent in the same building. |
| Ownership cost | EPA cites roughly $200–350 for fan replacement including parts and labor, not total system cost.[2] | Existing planning budget: $900–2,000 installed excluding diagnosis/repairs and $60–120/year service, plus power and accredited tests; validate with itemized pilot invoices. |

## Deployment Scenarios

1. **Basement retrofit:** a contractor tests an occupied home above its local action level, installs the suction pit and exterior fan, commissions the farthest slab test point and leaves a simple local warning display with an inspection contact.
2. **Housing cooperative:** a maintenance team owns scheduled sensor checks, accredited retests and repair tickets across multiple eligible buildings; residents see local status without transmitting indoor measurements or tenant identities to a cloud service.
3. **School wing on a suitable slab:** qualified staff test occupied rooms and evaluate HVAC schedules, after-hours pressure changes and discharge re-entry before choosing a design; one controller per suction zone does not certify the whole campus.

## Risks & Mitigations

- **False reassurance:** sensor drift, disconnected pressure tubing, stale radon samples and failed displays must produce **UNVERIFIED**. Compare/replace detectors on a documented schedule and use independent accredited tests; a green pressure trace is not a clean radon result.
- **Site interactions:** exhaust ice or condensation, slab leakage, high soil resistance and changing HVAC pressure can defeat extraction. Inspect discharge and seals, trend remote test points and retest after renovations or season changes.
- **Combustion and discharge safety:** suction changes can backdraft appliances; misplaced exhaust can re-enter openings. Require qualified combustion-safety checks and code-compliant siting; do not raise fan speed beyond the commissioned envelope to silence an alarm.
- **Outage and service burden:** without mains the fan stops; a supervised local backup may preserve a warning but cannot provide mitigation. Name an alert owner, inspection cadence and repair escalation. Budget tests, electricity and component replacement before claiming affordability.

## Vision for 2050

In the plausible success case, a building's radon record pairs a verified maintenance history with periodic independent exposure tests. Replaceable fans and pressure witnesses make repairs routine, while local-only logs help residents know when their mitigation is **unverified**. Wider adoption follows demonstrated performance across foundations and climates—not a promise that every building can use this design or that any exposure is risk-free.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/radon-and-health
[2] https://www.epa.gov/radon/how-do-i-know-if-my-radon-mitigation-system-working-properly
