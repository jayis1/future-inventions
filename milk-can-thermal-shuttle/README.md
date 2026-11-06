# Milk-Can Thermal Shuttle

**Author: jayis1. Status: unvalidated research concept; not an approved dairy-processing or food-safety device.**

## Problem

Small dairy producers often move milk in cans with little or no cooling; transport time matters because milk is perishable.[1] A conventional insulated can slows warming but cannot remove the heat in milk collected warm. Spoiled or unsafe milk costs households income and can expose consumers to pathogens. This proposal addresses a **20 L farm-to-collection trip**, not long-term storage or pasteurization.

## Solution

A repairable 20 L food-grade 304 stainless milk can slides into an insulated, split-shell jacket. In the jacket, **12 kg of reusable, sealed water/ice modules** contact a removable aluminum heat spreader around the can wall. The meltwater never contacts milk. A cooperative freezes the modules using a metered grid, solar-powered, or other refrigeration service; refrigeration is an essential input, **not free cooling**. An offline, locally readable temperature logger sits in a stainless thermowell touching the milk and starts a new record for each cleaned can. A sealed, single-use tamper-evident batch tag ties the temperature trace to that can without collecting producer identities. A latched high-temperature or missing-record warning means the cooperative must segregate the lot for testing or reject it; a green trace is not proof that milk is microbiologically safe.

## Key Innovation

Ice packs, insulated cans, and electronic thermometers already exist. The proposed contribution is an **exchangeable thermal jacket plus independently checked batch-temperature custody**: a common docking geometry lets a cooperative charge and swap ice modules while individual farmers keep affordable cleanable cans. The logger flags excursions even if a cooled can arrives cold after being warm earlier; unlike a thermometer taken only at delivery, its full record can expose that gap. The jacket must demonstrate faster cooling and fewer rejected/unsafe lots than an ordinary insulated can *at the same available ice and handling conditions*; novelty and benefit are engineering hypotheses, not patent or clinical claims. Unlike the repository's [Regenerable Grain Guard Cassette](../regenerable-grain-guard-cassette/), this is active heat removal from liquid milk, not vapor buffering in dry grain; unlike the [Radiative-Adsorption Refrigerator](../radiative-adsorption-refrigerator/), it uses an externally recharged ice service rather than ambient radiative cooling.

**Unvalidated performance targets:** cool 20 L of milk from 30°C to **≤8°C within 2 h**, then keep it ≤8°C for a further 3 h at 35°C ambient, with ≤12 kg ice charged initially at −5°C and no added ice. Measure temperature at the warmest milk location, after mixing where appropriate, and log ice mass, ambient temperature, trip duration, and measured refrigeration electricity. The 8°C threshold is a **trial design limit, not a regulatory safe-storage limit**; local dairy rules may demand colder or faster handling. Milk still needs prompt processing or properly validated cooling at the destination.

## Target Cost

**Unquoted 2038 target at 10,000 jackets/year:** US$85 for split-shell insulation, spreader, closures and assembly; US$30 for reusable sealed ice modules; US$25 for offline logger and replaceable battery; **US$140 per jacket kit**, excluding the 20 L food-grade can (budget US$45), refrigeration equipment, power, ice-module freezing labor, sanitation, transport, calibration, taxes and certification. Budget an additional unvalidated US$15/year per kit for seals, batteries and logger calibration; verify local quotes and depreciation before claiming affordability. Shared refrigeration must be priced per batch and cannot be hidden as a free service. Recycle aluminum and stainless locally; replace cracked polymer insulation and retire leaking ice packs rather than releasing them into food handling.

## Impact

FAO describes uncooled milk-can transport as time-sensitive and identifies small producers' distance to markets as a logistical challenge.[1] This device would help only where a cooperative can reliably freeze and distribute clean ice modules. In a **100-farm, 60-day paired pilot**, compare this jacket with locally available insulated cans: cold-chain time/temperature traces, viable microbial counts, spoilage/rejection rates, milk losses, energy per accepted litre, cleaning time, breakage and total cost. Randomize can assignment or use matched collection routes. A 20 L can moved daily for 60 days handles **at most 1,200 L**, not 1,200 L of milk saved; health and loss reductions are unknown until measured. If validated, it could widen safe collection windows for small producers without a private app or radio tracking. A 10–20 year path is prototype heat-transfer testing, food-contact and hygiene qualification, comparative field trials, then repairable local manufacture—not a claim of current readiness.

## Thermal and operating limits

With an illustrative milk density of 1.03 kg/L and heat capacity of 3.9 kJ/(kg·K), cooling 20 L from 30°C to 8°C removes about **1.77 MJ** (`20 × 1.03 × 3.9 × 22` kJ). Twelve kg of ice has roughly **4.0 MJ** latent capacity using 334 kJ/kg; that is a theoretical ceiling before incomplete contact, ambient heat ingress, jacket warm-up, and time-to-cool losses. Actual freeze energy and cycle time must be metered at the shared dock; a hot day, partly frozen pack, or slow transfer can defeat the target even with adequate nominal latent capacity. Record a module's frozen mass and temperature before dispatch, verify shell seals, and use an independent calibrated thermometer to check the logger on arrival.

The kit **does not pasteurize milk**. Standard continuous-flow pasteurization requires a controlled hold and diversion of underheated milk; a Canadian regulator lists 72°C for 15 seconds for ordinary fluid milk, subject to product-specific requirements.[2] Cooling or a reassuring arrival temperature cannot undo prior microbial growth, contamination or toxins. Reject visibly spoiled milk, clean and sanitize the food-contact can and thermowell between batches, and test according to local rules; do not mix suspect milk into a sound lot. Power loss at the freezer, ice leakage, missing logs, a broken thermowell, logger drift, or missed cleaning must show as a quarantine/inspection state, never as an automatic safe verdict. Validate condensation control outside the can, drop resistance, cleanability, battery disposal, and food-contact materials before use; maintain a non-electronic intake-temperature check if the logger fails.

## How It Works

At the collection dock, freeze and weigh the 12 kg sealed water packs; a pack that is partly thawed is not dispatched. Clamp the dry aluminum spreader against the closed 304-stainless can, close the insulated shell, and record a fresh batch identifier and the first milk temperature. The spreader conducts heat from the milk through the can wall into the ice, while the shell slows heat entering from 35°C air. No coolant touches the milk. At delivery, read the complete trace and independently check the thermowell against a calibrated thermometer; segregate a batch with a missing trace, excursion, broken seal, or failed pack for locally required testing or rejection. Wash and sanitize the can and thermowell separately from the removable jacket; return packs to the cooperative freezer. This is a cooling-and-evidence service, not pasteurization or a substitute for milk-quality testing.

## Technical Architecture

The thermal path is milk → stainless wall → removable aluminum spreader → sealed ice packs; the parasitic path is ambient air → jacket seams and insulation → can. A closed-cell, washable polymer shell with replaceable gaskets is a **candidate**, not a certified food-contact assembly. The lid and thermowell require hygienic, inspectable seals; the spreader and ice housings stay outside the food boundary. A battery-powered offline logger samples the milk thermowell (prototype target: once per minute), stores a batch-linked trace locally, and latches a fault on a gap, calibration failure or over-limit reading. A separate dock records pack mass, charge temperature and metered freezer electricity; operators reconcile those records with the batch tag without collecting a farmer identity. The temperature sensor needs mixing/stratification tests: a single thermowell may miss the warmest pocket. The 20 L milk alone weighs about 20.6 kg under the stated density assumption; adding 12 kg ice, can and shell makes one-person lifting hazardous, so fit handles for two-person lifts or a trolley and weigh the finished assembly.

## Performance Benchmarks

These are **unmeasured prototype gates**, not comparative field results. For the stated 20 L, 30°C start and 35°C ambient, the 1.77 MJ milk cooling load implies an average **245 W extracted over two hours**, before losses. A hypothetical jacket with overall heat-leak conductance of 1 W/K and a constant 27 K gradient admits **0.49 MJ over five hours**; this is an illustrative upper-bound-style design calculation, not a measured U-value or an exact transient model. Nominal ice latent heat is 12 × 334 kJ/kg = 4.01 MJ, but adequate energy *capacity* does not establish the required heat-transfer *rate*. Instrument the wall, warmest milk point and ice core to test both.

| Matched test at 35°C ambient | Ordinary insulated can (current local-practice comparator) | Shuttle gate | Evidence needed |
| --- | --- | --- | --- |
| 30°C → ≤8°C, 20 L | Not capable of active cooling without external ice; actual trace to be measured | Within 2 h | Three milk probes, calibrated reference, repeat runs |
| Hold after cooling | Measure same route and starting conditions; no assumed duration | ≤8°C for a further 3 h | Warmest-probe time series and seal inspections |
| Recharge and energy | Record baseline equipment energy, if any | ≤12 kg ice; meter kWh per cycle, no preset savings claim | Freezer meter, freeze/thaw mass and transport logs |

Compare rejection rates and microbial counts only in randomized or matched routes with identical incoming milk, handling, available ice and intake rules. Failure to reach a locally required legal temperature/time criterion overrides these engineering gates.

## Deployment Scenarios

- **Village collection route:** a cooperative freezes packs overnight, swaps them before a roughly five-hour collection-and-delivery window, and checks logs at intake; no service if freezer uptime or pack inventory cannot be assured.
- **Remote morning pickup:** a two-person team or trolley moves sealed cans from farms to a staffed collection hub; log gaps or late arrivals trigger lot segregation, not a retrospective safe label.
- **Seasonal heat surge:** extra charged packs and shaded waiting space can be staged at a hub, but any changed ice mass or route length needs a new validated protocol rather than silently extending the five-hour target.

## Risks & Mitigations

Slow wall transfer, a warm center, partially charged ice or an open jacket can consume the thermal margin: test multiple milk locations, weigh and inspect packs, and latch excursions. Residue in a lid or thermowell and coolant leaks pose contamination risks: use cleanable removable food-contact parts, pressure/leak inspections and replacement seals, with documented sanitation and lot isolation. A freezer outage, dead battery, clock drift or lost tag can erase custody evidence: require a visible fault state, independent intake thermometer and periodic calibration; hold or reject uncertain lots under local rules. The >32.6 kg milk-plus-ice load, before hardware, needs ergonomic trials, two-person handling or a trolley. Insulation damage, condensate and worn hinges require field repair and end-of-life collection. None of these mitigations proves microbiological safety without trials and regulatory review.

## Vision for 2050

If comparative trials demonstrate safe handling, affordable refrigeration and repairable operation, a cooperative could issue charged modules like returnable crates and accept milk with a locally readable temperature history rather than an opaque app verdict. The 2050 vision is a network of accountable smallholder collection points where a failed seal or trace is visible and resolved before mixing lots. Widespread use remains conditional on local power, sanitation, dairy rules and total lifecycle costs; the technology should never turn uncertain milk into an apparently certified product.

## Sources

[1] FAO, *Milk collection and transport*: https://www.fao.org/dairy-production-products/processing/collection-and-transport/en — milk-can transport conditions and perishability.
[2] Canadian Food Inspection Agency, *HTST pasteurization systems*: https://inspection.canada.ca/en/preventive-controls/dairy-products/htst?wbdisable=false — regulatory example of temperature/hold and flow-diversion controls, not approval of this device.
