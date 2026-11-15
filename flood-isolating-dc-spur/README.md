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

## Sources

[1] https://www.nature.com/articles/s41467-022-30727-4
[3] https://www.vde.com/topics-en/consumer-protection/electronics-flooding
