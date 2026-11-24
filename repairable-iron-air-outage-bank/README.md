# Repairable Iron-Air Outage Bank

**Author: jayis1**

**Status:** Research concept (not a certified power supply)

## Problem

Multi-day power interruptions spoil food and medicines, interrupt communications, and disable lighting and water pumps. Clinics and community shelters need storage beyond a single evening, but imported lithium packs and diesel fuel can be costly to replace or resupply. This concept targets stationary, noncritical community loads, not a life-support or medical-gas backup. Reliable service and health benefits must be measured, not inferred from storage capacity.

## Solution

A serviceable 48 V-class iron–air battery bank stores surplus solar or grid electricity in iron plates immersed in a contained aqueous alkaline electrolyte. During discharge, iron oxidizes toward iron hydroxide, releasing electrons; oxygen from filtered ambient air is reduced at a gas-diffusion electrode. Charging reverses the iron reaction by electroplating iron; a separate oxygen-evolution electrode handles charging instead of forcing the discharge air electrode to do both jobs. An isolated bidirectional power converter controls cell currents and supplies a separately protected DC bus; an inverter is optional. Air, water and electricity are inputs; heat and oxygen evolution during charging are managed by ventilation. No fuel or atmospheric carbon capture is claimed.

The design uses recyclable low-carbon iron sheet or porous iron, a polypropylene cell case and separator, replaceable nickel/iron-oxide oxygen electrodes, and a carbon/PTFE gas-diffusion discharge electrode. A bunded, lockable, spill-contained module permits trained technicians to replace individual electrodes and electrolyte; the user never opens a live cell. Include electrolyte-level, temperature, voltage and ventilation interlocks, plus independent fusing and a normally open output contactor. A disconnected or flooded module fails unavailable rather than energizing exposed contacts. An approved alternative supply must remain available for essential clinical loads.

**Prototype targets, not measured performance:** 5 kWh usable and 1 kW continuous output for five hours at 20–35 °C, with at least 40% electricity-in/electricity-out round-trip efficiency, 1,000 equivalent full cycles to 80% retained usable capacity, and a seven-day idle test. Targets assume adequate filtered airflow, periodic water makeup and replacement of degraded electrodes. Slow charging, hydrogen evolution from competing iron reactions, electrolyte carbonation, air-electrode flooding/drying, corrosion and low-temperature losses are open engineering risks. A 10–20-year engineering-development horizon is proposed, not a deployment date.

## Key Innovation

The proposed advance is a **separately serviceable iron/air/charging-electrode cassette** with a guarded charge path and a locally replaceable iron inventory: oxygen reduction and oxygen evolution do not have to share one fragile bifunctional electrode. It combines established iron–air chemistry and separate-electrode research into a field-maintainable outage module; neither the chemistry nor this performance is claimed to be novel or demonstrated. Unlike [Gravity Battery Storage](../gravity-battery-storage/), this design stores charge in reversible iron chemistry rather than lifting masses; unlike [Quantum Grid Energy Balancer](../quantum-grid-energy-balancer/), it is a physical storage device, not dispatch software.

## Target Cost

**Unquoted design estimate in US dollars at 10,000 modules/year by 2038:** $1,500 ex-factory for a nominal 5 kWh usable module ($300/kWh usable), including cells, iron, electrodes, enclosure, controls and DC converter; $2,400 installed including a provisional $900 for wiring, containment, commissioning and local service training. Solar array, inverter, taxes, transport, land, financing and certified backup are excluded. Budget $100/year for inspection and water/filter service plus $200 every five years for electrode/electrolyte service; these are planning allowances, not supplier quotes. Test actual bill of materials, energy losses and replacement interval before making an affordability claim. A low round-trip efficiency may make it unsuitable where charging energy is scarce.

## Impact

One qualified module could supply a measured 1 kW noncritical load for five hours during an outage; 10,000 fully used modules would provide at most 50 MWh of delivered outage energy per complete discharge, **not** an estimate of avoided deaths or uninterrupted care. Iron and polypropylene are widely available and replaceable, but electrode catalysts, electrolyte production and electricity still have upstream footprints. Compare lifetime cost, material recovery and full-cycle emissions against maintained lithium-iron-phosphate batteries and generators in real communities. Design for local repair rather than locked consumables; publish service instructions in local languages.

Before any deployment: bench-test energy balance and hydrogen/oxygen ventilation under faults; test leakage, enclosure corrosion, air-electrode degradation and thermal behavior; run an independent six-month field comparison with maintained alternatives. Follow applicable electrical, battery, chemical-handling, transport and building rules. Contain alkaline electrolyte; collect and neutralize or recycle it through authorized handlers, recycle iron and polypropylene separately, and never discharge spent solution to soil or drains. Do not connect to patient-critical circuits unless a certified, redundant system is independently approved.

## How It Works

1. **Charge:** A current-limited DC converter drives the iron-plating reaction in contained alkaline cells; a separate oxygen-evolution electrode releases oxygen to a monitored, outdoor-vented air path. Side reactions may generate hydrogen, so charging stops if airflow or gas sensing fails. No sealed indoor charging is permitted.
2. **Stand by:** The controller tracks cell voltage, temperature, electrolyte level and filter differential pressure. A periodic load test measures *usable* output after idle time; a state-of-charge estimate alone cannot certify outage readiness.
3. **Discharge:** Filtered air feeds the gas-diffusion electrode; reduction of oxygen pairs with oxidation of iron in the electrolyte. Cell current flows through fused series modules and a guarded DC converter to protected loads. An optional inverter serves AC loads, at additional conversion loss. At low voltage or an interlock fault, the output contactor opens and a separate approved backup takes over.
4. **Restore:** After isolation, lockout and verification of residual voltage, a qualified technician swaps a cassette, inspects seals and routes spent alkaline liquid/electrodes to authorized handlers. Recommissioning requires leak, isolation and controlled-load tests; this is **not** a hot-swappable consumer battery.

## Technical Architecture

`filtered air → discharge electrode | electrolyte/separator | iron electrode → fused DC stack → isolated bidirectional converter → protected DC bus → optional AC inverter`. Charge reverses the electrical path and vents gas through a dedicated exhaust; heat leaves through monitored ventilation. A polypropylene cell case sits in a secondary containment tray, with segregated gas and electrical compartments. Local controls read voltage/current, temperature, liquid level, leak and airflow sensors; a hardwired overcurrent device and normally open contactor remain effective without networking. Remote telemetry is diagnostic only, never the sole safety interlock.

The proposed cassette has three electrode roles (iron inventory, oxygen reduction, oxygen evolution), but electrode spacing, separator durability and actual 48 V stack configuration still require bench validation. A service bay isolates one module before opening it; hazardous electrolyte handling is reserved for trained personnel. Capacity is sized at the **DC bus**: 5 kWh usable at 1 kW permits five hours at rated output in the stated temperature range. At an assumed 90% inverter efficiency that is only 4.5 kWh AC (0.9 kW for five hours); a 1 kW AC load cannot run five hours from one module. Surge and transfer-time ratings remain unverified.

## Performance Benchmarks

| Metric and boundary | This concept: untested design target | Published comparator (different scale/duty) |
| --- | --- | --- |
| Continuous discharge | 1 kW DC for 5 h, 5 kWh usable DC at 20–35 °C | A CEC-funded Form Energy prototype delivered ~2.81 kW and ~306 kWh DC for 108–110 h; this is a **grid-scale module**, not proof of a repairable community unit.[1] |
| Round-trip electricity | ≥40% DC-input to DC-output including converter and auxiliaries; at assumed 90% inverter efficiency, ≥36% input-to-AC-output | The 2025 NLR ATB uses 85% as a representative *commercial battery storage* round-trip assumption; its commercial chemistry, duty and system boundary differ.[4] The CEC iron-air prototype did not publicly disclose its measured efficiency.[1] |
| Recharge after full discharge | At an assumed 40% DC-bus efficiency, 12.5 kWh electrical input per 5 kWh output; at 1 kW input, 12.5 h in the ideal power-limited model, longer if current limits/standby overhead intervene | The CEC iron-air prototype reported 63 h charge for a much larger, >100 h discharge module; not a normalized rate comparison.[1] |
| Durability / readiness | 1,000 equivalent full cycles to 80% capacity; pass a seven-day idle-and-discharge test; neither measured | The CEC report describes a small number of full-cycle tests, not a 1,000-cycle lifetime qualification.[1] |
| Installed cost | $2,400/5 kWh DC = $480/kWh usable, excluding inverter, generation and service; unquoted at 10,000 units/year | No like-for-like installed, field-repairable iron-air comparator is established here; do not infer cost advantage from iron price alone. |

These are acceptance gates, not product specifications. The 5-hour prototype is deliberately shorter than the multi-day iron-air grid demonstration: a single module does **not** solve a multi-day outage. For longer service, size multiple modules from measured duty cycles and verify charging opportunities, DC peak current, inverter surge capacity and transfer time before procurement.

## Deployment Scenarios

- **Rural clinic, noncritical wing:** A proposed 0.3 kW lighting/comms load for 12 h needs 3.6 kWh AC; one 4.5 kWh AC-equivalent module has little margin for aging or temperature losses. Keep medication refrigeration and patient-critical circuits on separately certified redundant supplies. Recharge from a verified solar/grid source budgeted for 12.5 kWh at an assumed 40% round-trip efficiency after a full discharge.
- **Telecom relay:** A 0.15 kW radio/router load for 24 h consumes 3.6 kWh AC, subject to inverter or DC-converter losses. Site the vent outdoors, maintain air filters and provide an alternate source for consecutive cloudy days. A commercial LFP pack may be better where quick recharge and compactness dominate.
- **Community shelter:** A proposed 0.6 kW lighting/charging load for seven hours uses 4.2 kWh AC; a single new module barely covers it, so specify reserve or multiple banks. Portable heaters and pumps need separate surge sizing; if outages span days with no charging, use more storage or a maintained generator.

## Risks & Mitigations

| Failure / uncertainty | Design response and test gate |
| --- | --- |
| Hydrogen on charge; blocked air path or drying/flooding electrode | Outdoor exhaust, airflow/gas interlocks and charge cutoff; fault-injection tests must demonstrate safe shutdown before occupied-site trials. |
| Alkaline spill, carbonation, corrosion or flooded enclosure | Secondary containment, replaceable seals, leak detection and automatic electrical isolation; chemical-compatible PPE and regulated disposal; immersion/leak tests before field service. |
| Freezing, hot operation, sensor fault or controller crash | Operate only within qualified temperature range; conservative independent fuse/contactor and local fail-open logic; cold/heat and sensor-disconnect tests. |
| Idle capacity fade, slow recharge, repeated outages | Logged seven-day capacity test, explicit reserve, recharge-energy budget and alternate certified supply; abort pilot if measured output misses critical design gates. |
| Service time, cost and material recovery | Time a qualified cassette change under lockout; publish replacement parts, verify recycling route and compare full lifecycle cost with maintained LFP and generators. |

## Vision for 2050

If the electrochemistry, safety and repair economics pass independent testing, locally serviced iron-air banks could preserve noncritical electricity at shelters and communications sites when fuel deliveries fail. A repair shop would replace a worn electrode rather than discard an entire enclosure. This is a **conditional scenario**, not an adoption forecast: in high-power, indoor or frequent-cycle applications, certified alternatives may remain superior. See [ROADMAP.md](ROADMAP.md) for gates and [IMPACT_ANALYSIS.md](IMPACT_ANALYSIS.md) for bounded projections.

## Sources

[1] https://www.energy.ca.gov/sites/default/files/2025-11/CEC-500-2025-045.pdf
[4] https://atb.nlr.gov/electricity/2025/commercial_battery_storage — NLR 2025 ATB Commercial Battery Storage
