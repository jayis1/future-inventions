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

## Sources

[1] https://www.cdc.gov/drinking-water/about/collecting-rainwater-and-your-health-an-overview.html — CDC Collecting Rainwater and Your Health
[2] https://guidelines.nhmrc.gov.au/australian-drinking-water-guidelines/part-1/chapter-4/4.2-applying-the-framework/4.2.2-preventive-measures-for-drinking-water-quality-management — Australian Drinking Water Guidelines 4.2.2
