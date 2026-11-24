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
