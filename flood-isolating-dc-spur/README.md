# Flood-Isolating DC Spur

**Author: jayis1**

**Status: TRL 2 research concept; no electrical safety certification or field validation.**

## Problem

An estimated 1.81 billion people live in locations exposed to significant 1-in-100-year flood risk; that figure describes flood exposure, **not** demand for this product.[1] Water-damaged electrical equipment can remain hazardous even after a flood recedes. VDE recommends locating distribution equipment above flood level and having specialists inspect affected equipment before re-energizing it; this concept does not weaken either recommendation.[3] Small community buildings with isolated 24 V DC lighting and charging spurs may have a low-lying cable/outlet damaged while a dry, elevated supply and other branches remain physically separate. A wet spur must not silently come back on when the water recedes.

## Solution

For **professionally designed, isolated, current-limited 24 V DC systems only**, fit an elevated, accessible distribution module above the site's surveyed flood level. Each low-lying spur has its own certified, appropriately rated overcurrent protection and a **normally open, two-pole, DC-rated disconnect** upstream of every flood-exposed cable. The 24 V supply, protective devices, disconnect, and 316L stainless contact hardware stay in the dry zone. A replaceable, individually keyed low spur terminates in a sealed service cartridge with two **low-energy wetting traces** at its lowest vulnerable connector and a separate, visible, irreversible water-exposure strip. The traces report water exposure to an isolated controller, which de-energizes that spur and latches the disconnect open. Broken trace wiring, controller fault, or loss of control power must also prevent the disconnect from closing. A manual reset is accessible only at the dry module after a qualified person inspects and, where required, replaces the wet cable, outlets, and cartridge.

This is **not** a mains-power junction, an automatic flood detector for evacuation, or a promise that water is electrically safe. Upstream AC wiring, PV and batteries need their own engineered isolation and local-code protections; flooding requires the site's normal evacuation and power-shutdown procedure. No one should enter floodwater to inspect or operate a connector.[3]

## Key Innovation

Sealed connectors, water probes, branch fuses and DC relays are established components. The testable proposal is the **paired, replaceable low-spur exposure boundary and dry-side locked-out disconnect**: the consumable visual witness makes a wet event legible after the probe dries, while continuity-checked probes prevent an open-circuit sensor from being interpreted as dry. Qualified inspection rather than a moisture reading is the only way back to service. Compare this arrangement with ordinary elevated distribution plus fused, sealed low-voltage cabling; added value is unproven. Unlike `flood-isolating-wellhead-collar`, it does not seal drinking-water infrastructure; unlike `passive-flood-door-sill`, it does not resist flood pressure at a doorway; unlike `receive-only-disaster-bulletin`, it does not convey emergency messages.

**Unverified design targets:** one 24 V DC, at most 4 A spur (96 W nominal load), with an installer-selected, DC-rated branch protective device coordinated to the cable and supply; independently verify disconnection within **0.5 s of trace wetting** in controlled tests at both minimum and maximum permitted supply voltage. Target **zero automatic reclosures** after a trip, even following power cycling, until a dry-side manual inspection/reset. This timing is not a shock-protection rating: water may reach exposed conductors first, and capacitors or secondary feeds may remain energized. The source's worst-case short-circuit capacity, interrupting duty, insulation class, protective-device coordination and jurisdictional rules are qualification gates, not assumed numbers.

## Target Cost

**Unquoted 2038 ex-workshop target at 10,000 modules/year: US$110** for a two-spur dry module and two replaceable witness cartridges: US$25 enclosed controller/supply interface, US$30 pair of DC-rated two-pole disconnects, US$16 qualified branch protection, US$14 sealed cartridge/probe/strip pair, US$25 enclosure, assembly and end-of-line test. **Target US$8 per replacement cartridge** plus qualified labor and any cable/outlet replacement. These are hypothetical manufacturing allocations, not supplier quotations. The isolated supply, elevated mounting, flood survey, cabling, permits, testing, battery protection and maintenance are excluded; total installed cost may make conventional elevation of *all* spurs cheaper and safer. No cost saving is claimed.

## Impact

A controlled **50-site pilot target**, only after laboratory and regulatory qualification, would compare matched isolated DC circuits using ordinary elevated fused distribution against this dry-side lockout arrangement. Record missed wetting, nuisance trips from condensation, disconnection latency, dry-zone water intrusion, fault-latched state after power cycling, service time and actual replacement cost. The potential benefit is a **narrower, more inspectable damaged branch**, not a quantified reduction in injuries or a promise of uninterrupted clinic power. Keep essential medical and evacuation loads on separate, qualified systems; their continuity must never depend on this prototype.

**Failure boundaries:** Saltwater, sediment, bridging debris, corrosion, a welded contact, reversed polarity, hidden alternate feeds, cable damage ahead of the wetting trace, or water above the surveyed dry-zone elevation can defeat isolation. A downstream witness cannot detect upstream ingress. A false trip sacrifices service; a missed trip is potentially dangerous. The pilot must inject each failure, inspect both poles for contact welding, and measure residual output voltage before anyone touches equipment. Any flooded or suspect installation remains off and needs qualified electrical inspection and replacement as applicable.[3] Modules should use screw-accessible parts and replaceable strips, recover steel/copper at end of life, and route contaminated components into approved electrical-waste streams. No network link, user tracking, remote switching, military or surveillance function is proposed.

## How It Works

In normal service, a qualified installer mounts the dry module above the surveyed flood elevation, sizes each branch fuse/breaker to its cable and source fault current, and connects only a single isolated 24 V DC, ≤4 A nonessential spur per two-pole disconnect. A deliberately supervised low-energy trace loop at the lowest vulnerable connector distinguishes intact/dry from wet or broken wiring; a separate irreversible strip records exposure after drying. The controller permits closure only when its self-check and trace loop pass and a qualified operator deliberately resets it. The trace design must be tested with fresh, low-conductivity, salty and dirty water: conductivity alone is not a universal flood sensor.

A wet or invalid reading removes coil drive, opens **both** supply conductors and latches the event through power cycles; no timed or automatic dry-out restart. The fuse/breaker still handles overcurrent independently. A dry-side indicator reports commanded state and any fault, **not verified absence of voltage**. Inspection starts from the upstream source under qualified lockout procedures, checks both disconnect poles, cable/outlets and witness, tests insulation and residual voltage, then replaces damaged parts before intentional reset. Water can reach a conductor before the trace, a contact can weld, and a capacitor or hidden reverse feed can retain energy; no person may infer a flooded spur is safe from the indicator.

## Technical Architecture

- **Power path:** isolated, current-limited 24 V source → source- and cable-coordinated DC overcurrent protection → independently DC-rated normally open two-pole disconnect in elevated dry enclosure → keyed low-spur cable/outlet (≤96 W nominal). Both conductors open; upstream source, protective device and any other branches remain energized unless separately isolated. No shared downstream return or alternate PV/battery feed is allowed without a separate engineered isolation design.
- **Sense/control path:** replaceable low-energy trace pair plus irreversible visual witness → isolated continuity/wetting front end → supervised lockout logic → disconnect coil. Independent feedback on each pole is a proposed diagnostic for welded contacts; it does not replace a qualified voltage test. Loss of controller power or sensor continuity inhibits coil drive, while a welded contact is a dangerous undetected or diagnosed-but-not-cleared fault requiring upstream disconnection.
- **Physical boundary:** dry module and serviceable DC protective parts above surveyed flood level; exposed cartridge at the lowest designated connector. 316L contact hardware limits corrosion but does not make immersion safe. Debris bridging, water above the dry module, condensation, or damage between module and sensor is outside the sensor's coverage. No wireless link or remote reset; logging can be local and non-identifying.

## Performance Benchmarks

There are **no measured prototype results**. Compare against the stated baseline—an elevated, fused, sealed isolated-24 V DC branch with no wetting-triggered lockout—under the *same* cable, source and water exposures. Its fuse protects against overcurrent, not necessarily a high-resistance wet connector; this is a functional distinction, not proof of superior safety. The following are **unverified engineering targets**, not industry state-of-the-art results or certified ratings:

| Metric | Proposed test/target | Baseline and limitation |
| --- | --- | --- |
| Nominal branch envelope | 24 V DC × 4 A = 96 W at nominal voltage; verify supply tolerance and worst-case source short-circuit current against selected DC interrupt ratings | Same source/cable/fuse; no claim of safe-touch voltage |
| Wetting-to-open latency | ≤0.5 s in controlled fresh/salt/dirty-water tests across qualified supply range; timestamp trace exposure and independently measured pole opening | Baseline has no moisture-triggered trip; neither design guarantees disconnection before water reaches conductors |
| Restart after wet event | 0 automatic reclosures across 100 power cycles in bench trials, followed by deliberate inspected reset | Baseline has no wet-event latch; target is a sample test, not a reliability probability |
| Fault detection and durability | Demonstrate open-probe, stuck-driver and welded-contact injection; set false-trip and missed-trip limits only after a ≥50-site matched pilot | No defensible field failure-rate comparator yet |

Before any occupied-site use, independently test actual DC interruption at maximum prospective fault current, insulation after immersion, ingress, sensor coverage, nuisance trips, contact endurance and downstream residual-energy decay. A coil command is not isolation evidence; applicable electrical approval remains mandatory.

## Deployment Scenarios

1. **Community charging kiosk:** an elevated, qualified isolated supply feeds two individually fused, low-lying 24 V phone-charging outlets. A wet outlet latches off only its branch; staff keep users away, shut down the source if the dry boundary is threatened, and arrange qualified inspection before reopening.
2. **Flood-prone workshop lighting:** nonessential task-light spurs below a surveyed high-water line use keyed cartridges, while the supply and dry controls remain above it. Separate circuits support evacuation lighting; no safety-critical lighting depends on this prototype.
3. **Seasonal river field station:** a removable 24 V instrumentation spur has an accessible dry-side reset, exposure witness and scheduled pre-season inspection. This does not protect the station's upstream mains, solar array or battery; each has its own compliant protection.

## Risks & Mitigations

| Failure / tradeoff | Proposed mitigation and residual risk |
| --- | --- |
| Low-conductivity water, fouling or an unmonitored cable segment | Test multiple water chemistries and sensor placements; a missed exposure remains possible, so maintain flood evacuation and whole-system shutdown procedures. |
| Coil/logic power loss, disconnected trace, firmware hang | Normally open device with supervised loop and watchdog inhibits closure; common-cause enclosure flooding or welded contacts can defeat this fail-safe intent. |
| DC arc, contact welding, reverse feed and charged capacitors | Select proven DC voltage/current/fault ratings, protect each branch, test both poles and residual voltage independently; isolate upstream before touching. No AC-only relay substituted. |
| Corrosion, splash nuisance trips and maintenance cost | Sealed replaceable cartridge, visible witness, scheduled checks and recorded service; false trips still interrupt useful loads. |
| Unsafe restart or unapproved installation | Latched manual reset after qualified inspection and jurisdictional approval; no safety certification or occupied-site suitability is claimed today. |

## Vision for 2050

If independent tests and field data establish a benefit over simpler elevated, fused wiring, inspectable flood-exposure boundaries could become standard options for *nonessential* isolated DC branches in flood-resilient buildings. Technicians would replace a witnessed damaged spur instead of guessing whether a dried outlet was exposed. The safer first choice would still be to elevate equipment and keep people out of floodwater; ubiquity is a scenario, not a forecast or permission to bypass electrical codes.

## Sources

[1] https://www.nature.com/articles/s41467-022-30727-4
[3] https://www.vde.com/topics-en/consumer-protection/electronics-flooding
