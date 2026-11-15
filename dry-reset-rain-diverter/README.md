# Dry-Reset Rain Diverter

**Author: jayis1**

**Category:** Clean Water & Universal Basic Services / Rainwater Collection

**Status:** TRL 2 research concept; not a drinking-water treatment or a potable-water safety certification.

## Problem

Rainwater collection can help households and community facilities where reliable water supplies are limited, but roofs and gutters can carry animal waste, dust and roofing chemicals into a tank. CDC warns that clear-looking rainwater can still contain germs and chemicals and recommends testing and appropriate treatment for drinking, cooking or bathing.[1] Australian drinking-water guidance already recommends first-flush diverters and routine roof/gutter maintenance; a diverter by itself is **not** new.[2] The research problem is narrower: after a short storm or a blocked drain, a conventional chamber can remain full, so the next event may reach the tank without a fresh diversion. A visible, testable dry-reset interlock could make that particular failure harder to miss; it cannot diagnose contamination throughout a storm.

## Solution

Fit a serviceable mechanical cassette between a screened roof downpipe and an **untreated rainwater tank**, never directly to a drinking-water tap. In its spring-rest position, a three-port flap sends all incoming runoff to an approved open waste route with a visible air gap from the tank inlet. A removable opaque **25 L food-contact-qualified polypropylene first-flush chamber**, on a nominal 100 m² roof, receives the initial runoff. Its low-position float arms a captive pawl **only after the chamber drains fully**; when runoff refills the chamber and a high-position float trips, continuing flow deflects a paddle that can hold the flap in the tank position. If flow stops, the paddle spring releases the flap back to waste and disarms the pawl. A later shower cannot reopen the tank route until a real low-to-high float cycle occurs. A red/green mechanically linked inspection flag indicates waste/tank route; a separate low-float window shows whether the chamber has emptied. The chamber drains through a removable, insect-screened restrictor to a safely draining, non-potable route; both screen and drain need inspection. No electronics, battery, water-quality sensor, person tracking or network connection.

**This is a testable layout, not an installed system.** The site designer selects the diversion volume based on roof area, materials, storm pattern and local rules. The 25 L example corresponds to 0.25 mm of *actual roof runoff* from 100 m², not a universally adequate cleaning dose. A 20 mm rainfall event over that roof gives 2,000 L incident rain and, at an assumed 0.8 runoff coefficient, 1,600 L runoff before losses; diverting 25 L leaves at most 1,575 L for collection before downstream overflow and other losses. Those are mass-balance bounds, not water-quality results. Light drizzle or interrupted rain may be diverted entirely; the device must not trade safety for yield. A covered, screened tank, approved treatment and independent sampling remain separate requirements.[1][2]

## Key Innovation

The proposed research delta is **event-reset proof by physical state**, not first-flush treatment: a normally-to-waste valve needs (1) an observed empty chamber, (2) a fresh high-float transition and (3) continuing downpipe flow before it can send runoff toward a tank. A drain blockage, stuck-high float, absent paddle flow, power outage or a pause in rain defaults to diversion rather than silently treating an old, full chamber as a fresh flush. An incorrectly assembled pawl or valve leak is still possible, so the flag cannot certify water safety. Existing first-flush and detachable-downpipe approaches are the baseline.[2] Unlike [Coastal Lens Recharge Gate](../coastal-lens-recharge-gate/), which controls approved water entering a subsurface gallery and measures groundwater salinity, this cassette tests tank-inlet first-flush reset reliability. Unlike [Flood-Isolating Wellhead Collar](../flood-isolating-wellhead-collar/), it neither seals a well nor prevents floodwater ingress there. No claim of patent novelty or established superiority is made.

## Target Cost

**Unquoted 2038 manufacturing goal, US dollars, 10,000 units/year:** US$42 ex-workshop for a 25 L cassette and controls: molded chamber/lid US$12; polypropylene flap, springs and floats US$9; silicone/EPDM qualified seals and replaceable screen/drain US$6; indicator and pawl US$5; assembly and leak/sequence check US$10. Add an unquoted US$8/year for periodic screen/seal replacement and paid cleaning; roof gutters, suitable tank, site drainage, installation, water testing/treatment, certification, shipping and taxes are **excluded**. Confirm quotes and full installed lifetime cost against a standard maintained diverter or a detachable downpipe; abandon the extra mechanism if its service burden outweighs any measured reliability gain. Locally replaceable screens, snap-out chamber and tool-accessible fasteners are design targets, not proven repairability.

## Impact

A bounded 10–20-year path starts with a transparent bench model and fault injection, then a supervised **100-roof, two-rainy-season** matched comparison against maintained standard first-flush diverters. Pre-register targets of **≥99% default-to-waste transitions** across at least 1,000 simulated interrupted-rain, blocked-drain, stuck-float and reassembly fault trials, and **zero tested transitions to tank after a missed empty-state reset**; report uncertainty and every failure, not just average yield. Compare paired event samples for *E. coli*, turbidity and site-relevant dissolved chemicals at the tank inlet, plus diverted/collected volume, routine maintenance time and bypass/drain overflow. The central hypothesis fails if a common blockage still permits stale runoff to tank, the flag misrepresents valve position, or users cannot maintain it. No waterborne-disease reduction or number of beneficiaries is forecast without trials. Qualify with local drinking-water, plumbing and rainwater-harvesting authorities before any potable application; until then use approved safe drinking water and treat the tank as untreated.[1]

## Failure behavior, maintenance and lifecycle

- **Blocked screen/drain or persistent wet chamber:** do not admit to tank. An independent overflow must release rejected water to a site-approved route without pooling by buildings or neighbors; if no safe waste route exists, the installation is ineligible. Empty and clean the chamber before rearming.
- **Stuck paddle/float, spring loss, wrong assembly or valve leakage:** use keyed parts and a linked flap-position flag; inspect by a dry-run and controlled water challenge after each cleaning. The flag is not a chemical or microbiological test. Any ambiguous state requires disconnecting the tank inlet and repairing the cassette. Challenge spring corrosion, biofilm, UV exposure and seal wear in qualification tests.
- **Storms, roof chemicals or unsafe source:** first flush does not remove all pathogens, lead, pesticides, smoke fallout or dissolved hazards. Reject suspect roofs/events and consult local public-health testing and treatment guidance; never join untreated rainwater to potable plumbing.[1] The unit must be installed below an accessible leaf screen and above a protected, covered tank with its own overflow and insect barriers.[1][2]
- **End of life:** remove captured sediment without aerosolizing it; manage contaminated material under local rules. Separate metal springs for recycling and reuse/recycle qualified polypropylene where a local stream exists; replace degraded elastomers. No intentional environmental release of media or organisms.

## How It Works

1. **Dry and ready:** At rest the spring holds the flap toward waste; an empty chamber lowers the low float and arms the pawl. The flag must show waste. The roof screen intercepts leaves but does not purify runoff.
2. **First runoff:** Rain enters the 25 L chamber while the inlet remains isolated from the tank. The drain restrictor must pass less water than the design minimum *qualifying* runoff flow, or the high float will never trip; at lower flow, divert everything rather than bypass the interlock. The high float releases the armed pawl only after the chamber fills. Flow on the paddle then holds the flap toward the untreated tank. A physical travel stop and linked flag expose the commanded position, not a water-quality verdict.
3. **Pause and reset:** When runoff ceases, the paddle releases and the spring returns the flap to waste, disarming the pawl. Residual water bleeds through the screened drain. Until the low float reaches its empty datum and rearms the pawl, a second burst is rejected. A genuinely emptied chamber can rearm even within a long storm: this is a hydraulic empty-state criterion, **not** proof of a new meteorological event or clean roof. Dew, persistent humidity or a clogged drain may delay emptying; accepting lost yield is preferable to silently skipping the flush.
4. **Overflow:** The waste outlet and chamber overflow need separately sized, visible routes to approved drainage away from foundations; a full tank needs its own overflow. If debris, ice or backpressure blocks either route, stop collection and isolate the downpipe until drainage is restored. No design can guarantee fail-safe behavior with a blocked discharge or a mechanically jammed flap.

## Technical Architecture

The flow path is **roof → accessible leaf screen → downpipe/cassette inlet → first-flush chamber and waste outlet → three-port flap → untreated tank inlet**. A replaceable polypropylene chamber and lid contain the sediment-prone water; a removable screened restrictor drains it. Two mechanically independent float positions encode empty-then-full, a captive pawl stores the armed state, and a runoff-driven paddle plus return spring gate the flap. Use corrosion-resistant stainless springs, UV-protected polypropylene housing and qualified silicone/EPDM seals as material-selection *proposals*; compatibility with the actual roof runoff, UV dose and local code must be tested. The mechanically linked position flag and low-float window are inspection interfaces. There is no telemetry or electrical power.

Design verification must trace each state transition and each leak path: measure outlet flow with flap in both positions, deliberately block the drain and screen, jam each float, disable the return spring, install the chamber incorrectly, and challenge the overflow at peak site runoff. The drain-rate/float hysteresis must be selected together: a chamber that never fills at useful rainfall rates is safe but ineffective; a chamber that drains too fast during a pause can legitimately reset without the roof becoming clean. A keyed cassette and seal inspection reduce, but cannot eliminate, an internal cross-port leak. Manual cleaning and a controlled water challenge follow every service event.

## Performance Benchmarks

These are **pre-registration targets, not prototype measurements**. The current comparable practice is a maintained, fixed-volume first-flush diverter or detachable downpipe recommended in rainwater guidance [2]; no published paired reliability or reset-time figure is asserted for that baseline. Run both devices on the same screened 100 m²-equivalent rig, 25 L nominal diversion, and programmed runoff, with equal maintenance and a metered tank inlet. At 0.8 runoff coefficient, a 25 L chamber requires 0.3125 mm incident rain to fill (25 L ÷ (100 m² × 0.8 × 1 L/m²/mm)); the high-float transition and drain leakage raise the real threshold. A 20 mm event has at most 1,575 L available after this diversion, before overflow and other losses; compare measured yield against the maintained baseline, not that ideal bound.

| Metric and test | Proposed gate | Current practice comparator |
| --- | --- | --- |
| Return to waste on flow-stop, blocked-drain, stuck-float and reassembly challenges (≥1,000 aggregate trials, including aged parts) | ≥99% commanded return-to-waste transitions; **zero** tank admissions after a missed empty reset | Same fault sequence on a maintained 25 L conventional diverter; outcome not yet measured |
| Dry-reset interval after a 25 L flush at 20 °C, level mount and clear restrictor | Record distribution and seek ≤24 h to low-float datum; repeat at 5–35 °C and with biofilm/sediment | Measure chamber-empty time on the matched conventional unit; no universal baseline specified |
| Hydraulic envelope at 10, 50 and 100 mm/h on 100 m² with 0.8 runoff coefficient | Challenge approximately 0.8, 4 and 8 m³/h roof runoff respectively; no flooding at the tested peak, with an approved overflow | Same peak-runoff and loss-of-collection test on the matched installation |
| 1,000 wet–dry cycles with UV-aged seals and fouled screen | No unintended tank opening, no visible cross-port leak; quantify leakage in L/event and service time in min/event | Same cycle and maintenance log on the baseline |

Zero failures in 1,000 trials would still not prove zero real-world risk (one-sided 95% binomial upper bound is about 0.30% per tested transition). Event timing, debris, roof materials and water quality need the two-season field comparison described above; *E. coli* and chemical sampling measure outcomes, not a guarantee of potability.

## Deployment Scenarios

- **School rainwater tank in a seasonal climate:** An installer sizes the cassette from roof area and local first-flush rules; a caretaker checks both windows and empties the sediment chamber after storms. Use only for locally approved non-potable uses unless independent treatment, testing and plumbing approval are in place.
- **Community center with intermittent showers:** A dry spell may not empty the restrictor before the next shower, so the device sacrifices yield by continuing to waste. Meter both outlets for a season and compare against a serviced standard diverter before deciding whether the added mechanism is worth its upkeep.
- **Small farm outbuilding:** A protected downpipe, screened tank and correctly graded waste line can collect runoff for permitted non-potable tasks. Reject roofs with suspect coatings or chemical drift, and winterize or bypass the cassette where freeze-up can block discharge.

## Risks & Mitigations

| Risk | Mitigation and check |
| --- | --- |
| Drain clogging, insects, biofilm or back-to-back wet spells prevent reset | Removable screen and visible low-float window; log time-to-empty, clean under local hygiene rules, and never override an unarmed pawl merely to improve yield. |
| Paddle jam, tired spring, seal leak or erroneous assembly opens a tank path | Key parts, link flag to actual flap shaft, challenge with water after service, and inspect leakage after accelerated cycles. Quarantine the tank inlet on any ambiguous state. |
| Wind-driven splash, drizzle or variable roof area changes flow threshold | Calibrate drain/paddle thresholds on the installed catchment; test low-flow and crosswind events; discard runoff rather than assume sufficient flush. |
| Peak storm or blocked overflow sends water toward a building | Engineer both waste and overflow routes for local design rainfall; inspect for backpressure and provide an accessible downpipe bypass. Do not install without a lawful safe discharge. |
| Freeze, UV, corrosion and material creep shorten life | Shelter the cassette, qualify seals/springs in accelerated exposures and replace on inspection schedule; disable collection in freezing conditions until drain is free. |
| Tank water is mistaken for drinking water | Label untreated supply, keep a physical air gap and prevent potable cross-connections; follow testing/treatment and authority guidance [1][2]. |

## Vision for 2050

In a plausible 2050 deployment, buildings in water-stressed regions could pair visible, repairable reset mechanisms with covered storage and separate treatment where drinking water is intended. Operators would compare failures, water samples, maintenance hours and yield against simpler diverters before adoption. Success would mean fewer *unnoticed missed resets* without pretending that first-flush diversion makes rainwater safe; where a standard serviced device performs as well, the simpler device should win.

## Sources

[1] https://www.cdc.gov/drinking-water/about/collecting-rainwater-and-your-health-an-overview.html — CDC Collecting Rainwater and Your Health
[2] https://guidelines.nhmrc.gov.au/australian-drinking-water-guidelines/part-1/chapter-4/4.2-applying-the-framework/4.2.2-preventive-measures-for-drinking-water-quality-management — Australian Drinking Water Guidelines 4.2.2
