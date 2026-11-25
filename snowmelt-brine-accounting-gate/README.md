# Snowmelt Brine Accounting Gate

**Author: jayis1**

**Status:** Research concept; not an approved stormwater treatment system or a ready-to-use deicer

## Problem

Road deicing salt dissolves and migrates into fresh water. A USGS watershed study found winter/early-spring stream chloride peaks associated with deicer runoff and later peaks associated with snow piles, soils and shallow groundwater.[1] Municipal snow-storage sites already collect meltwater, but an ordinary detention pond can delay and dilute chloride without removing its mass. The proposed deployment is a lined, permitted snow-storage yard with controlled drainage, not an uncontained roadside ditch. Benefit is bounded by the salt that actually reaches that yard; it cannot solve runoff from roads that never enters it.

## Solution

Install a **normally-to-containment, sampleable split-flow gate** between a snow-storage pad's sediment forebay and its existing permitted meltwater handling system. A screened gravity inlet, calibrated flow meter and temperature-compensated conductivity probe measure each incoming parcel. The control valve routes sufficiently saline flow into a bunded, covered HDPE brine tank; all uncertain, fouled, power-failed, or out-of-range flows go to the existing lined containment route, never directly to a stream. Low-salinity flows still need site-specific authorized treatment or discharge: conductivity alone is **not** a discharge permit or proof of ecological safety.

The distinctive feature is a **chloride-mass ledger and reuse veto**, not a new chemical process. Paired flow and grab-sample chloride assays calibrate conductivity for that particular site and deicer mixture; recorded inlet, captured and bypass volumes/concentrations reveal whether salt was actually intercepted instead of merely diluted. A trained operator tests the stored batch for chloride, sediment, metals and petroleum contamination before deciding whether it can replace some *water* in an existing, regulated road-salt brine-preparation process. Supplemental clean road salt may be needed to reach the operator's specified deicing strength; contaminated batches are managed as regulated runoff, not reused. Sediment is removed at the forebay and disposed of according to site waste rules. This device never makes potable water or removes dissolved salt by filtration.

Materials: HDPE lined 1 m³ pilot tank, polypropylene/HDPE wetted pipes, 316L stainless strainer and serviceable valve, conductivity/temperature probe, flow meter and a sealed 24 V controller with battery-backed alarm. The control power is an assumption of <10 W average, with no reliance on solar availability. Periodically clean the inlet and sensors, check valve travel, calibrate with laboratory chloride samples, inspect liner integrity and arrange licensed removal of failed or surplus batches. Site-specific frost protection and a passive overflow path to existing containment are mandatory.

**Pilot targets, not demonstrated performance:** at a *controlled pilot inlet* of up to 0.3 L/s and 0–5 °C, capture ≥60% of the incoming **chloride mass reaching this inlet** during a sampled melt season, while retaining every selected high-salinity batch in a lined tank. Verify by flow-weighted laboratory chloride analyses on both branches, including overflow, with an independently checked measurement uncertainty; the percentage is not a catchment-wide reduction. A 1 m³ tank fills in about 56 minutes at 0.3 L/s if all inflow is diverted, so larger events require an existing additional lined holding volume or safe diversion back to containment. Reject a site where that volume or an approved disposal route does not exist. This is a 10–20-year integration and validation pathway using existing components, not a claim of current certification.

## Key Innovation

Existing work has examined early, concentrated chloride release from stored snow and recycling saline runoff into road-brine production; those processes are prior art, not ours.[2][3] The testable departure is a **fail-to-containment diversion gate tied to a field-auditable chloride mass balance and contaminant-based reuse veto** at a municipal snow yard. Unlike [Capillary Salt-Export Tile](../capillary-salt-export-tile/), which wicks salinity from farm soil, this design intercepts deicer chloride in engineered snowmelt drainage before dilution. Unlike [Coastal Lens Recharge Gate](../coastal-lens-recharge-gate/), it does not manage freshwater aquifer recharge. Novelty outside this repository and patentability have not been established.

## Target Cost

**Unquoted US-dollar design estimate, 1,000 gates/year by 2038:** $2,800–4,500 ex-workshop for the valve, 24 V controller, flow and conductivity instruments, 1 m³ lined tank, bund and fittings. Assume another $1,500–4,000/site for civil tie-in, power, frost protection and commissioning **where a lined yard and permitted containment already exist**; otherwise cost is site-specific and likely much higher. Budget $350–900/site/year for calibration samples, lab chemistry, cleaning and parts, excluding operator time, recovered-brine conditioning, transport, treatment/disposal, taxes and permit fees. These are planning allowances without supplier quotes. Economics depend on avoided salt purchases and avoided permitted treatment costs, both to be measured; no payback is claimed.

## Impact

At an illustrative **1,000 L batch at 20 g/L NaCl equivalent**, the batch contains **20 kg NaCl equivalent** (about **12 kg chloride** if the dissolved salt is all NaCl). Those are incoming quantities, not guaranteed recovered product or avoided stream loading. If the pilot actually retains 60% of that batch's chloride and a permitted reuse route exists, at most roughly 7 kg chloride could be deferred from that yard's immediate wastewater stream; reuse on roads can still return that chloride to the environment later. Count only **net reduction in newly purchased and released salt** from independently recorded yard and road-application inventories, not gross brine recycled. Compare against source-side optimized salt application, which may be cheaper and more effective.

Pilot gates: (1) compare one equipped yard with its measured pre-installation or matched-yard baseline over at least two melt seasons; (2) sample flow-weighted inlet/outlet chloride, sodium, metals, suspended solids and hydrocarbons, with lab blanks and independent data audit; (3) demonstrate that probe faults, ice jams, blocked screens, power loss and full-tank events cannot create an unpermitted discharge; (4) require the permitting authority and road-maintenance operator to approve containment, contaminant thresholds, destination and deicer performance before any reuse. Stop reuse if quality fails, tank leaks or chloride mass balance does not close within a predeclared uncertainty band (pilot goal ±15%). Report habitat effects only after downstream monitoring; do not infer improved health or ecological safety from diversion alone. The tank and electronics have embodied emissions and require end-of-life recycling; contained dirty solids and brine require approved disposal.

## How It Works

1. A lined snow yard drains through a sediment forebay to the screened gate; the approved existing containment route remains hydraulically available even when the new equipment is off. A site engineer sizes that route for design-storm and ice-blockage conditions before installation. Flow, water temperature and conductivity are logged together at the inlet; a composite or scheduled grab sample provides laboratory chloride concentration for a site-specific conductivity-to-chloride calibration. A single conductivity threshold is never a pollutant clearance test.
2. The controller estimates each interval's incoming chloride as `flow (L/s) × interval (s) × laboratory-calibrated chloride (g/L)`, converted from grams to kilograms. If calibrated salinity exceeds an operator-approved capture setpoint and the tank has verified free volume, the valve directs flow to the covered, bunded tank. Otherwise flow returns to the yard's existing permitted containment/treatment path; a fault, stale reading or full tank inhibits capture and alarms the operator. Any permitted discharge remains governed by the site's authorization, not this gate.
3. At batch close, independently sampled inlet, tank and containment-branch concentrations and volumes reconcile `M_in = M_tank + M_containment + ΔM_on-site + M_unexplained` over the stated boundary and interval. Include overflow and leaks in the unexplained/escape term until measured. If the balance misses its predeclared uncertainty band, quarantine the batch and investigate. A signed operator release, contaminant assays and the receiving road-maintenance program's approval precede any reuse; record the batch's eventual destination, including disposal or later road application.

## Technical Architecture

The **hydraulic train** is lined pad → cleanable forebay/screen → accessible inlet sampling port and flow meter → temperature-compensated conductivity probe → serviceable split valve → either bunded HDPE tank or the already-permitted lined containment route. The tank has independent level indication and secondary containment; the passive overflow leads only to that existing route, subject to the site hydraulic and permit review. A de-energized valve position must be demonstrated on the actual installation, not assumed from a catalog.

The **control and evidence train** is a local 24 V controller with timestamped sensor readings, calibration versions, valve-position feedback, tank level, tamper-evident operator overrides and batch IDs. A battery-backed alarm covers loss of mains power; communications loss leaves local interlocks active and queues records for later export. Setpoint changes require authenticated local authorization, and the operator checks valve travel, blocked screens, samples and the destination ledger during winter rounds. The mass ledger records chloride; sodium and non-salt contaminants require separate assays and cannot be inferred from conductivity. Flow-meter and sample timing errors propagate into a reported uncertainty range, not a fictitious precise removal number.

## Performance Benchmarks

All figures below are **unvalidated design targets or comparison definitions**, not measured results. The relevant comparator is the same lined, permitted yard operated with its existing containment system and no gate; neither this baseline nor the prior brine-recycling work cited above establishes a universal state-of-the-art capture percentage.[2][3] Compare matched inlet mass, melt-event temperature and hydraulic loading, tank capacity, disposal route and operating time over two seasons.

| Metric and boundary | Existing-yard comparator to measure | Proposed pilot acceptance target | Evidence needed |
| --- | --- | --- | --- |
| Chloride retained in *new* isolated tank / chloride entering controlled inlet | 0% in the added tank by definition; existing yard may already retain or treat salt | ≥60% over sampled melt-season inlet mass at ≤0.3 L/s and 0–5 °C, conditional on holding capacity | Paired, flow-weighted lab chloride and all branch/overflow volumes; report confidence interval |
| Ledger closure, same inlet and period | Not normally documented as a split-flow mass ledger; measure actual yard baseline | Absolute unexplained mass ≤15% of incoming mass, pilot goal | Independent volume calibration, blanks, duplicate assays, time alignment |
| Fault routing, gate outlet | Existing site's permitted containment behavior is the safety baseline | No unpermitted direct discharge during simulated sensor, power, ice and full-tank faults | Witnessed failover and hydraulic overflow tests |
| Additional electrical load | Existing yard's metered electrical load | <10 W mean controller power, excluding any site-specific heat tracing/pumping | Winter power logging and separate frost-protection meter |

A 1 m³ tank alone cannot sustain 0.3 L/s capture beyond roughly 56 minutes; it is a test vessel, not peak-event storage. No claim of better ecology, lower total chloride release or lower lifecycle cost follows until the comparator and eventual brine disposition are measured.

## Deployment Scenarios

- **Municipal lined snow yard:** Pair the gate with an existing forebay and permitted storage/treatment basin; a roads crew samples tank batches and uses only regulator-approved, quality-tested batches in its brine-preparation operation. Reused chloride may later leave roads again, so publish both yard-retention and net-purchase inventories.
- **Airport or depot with segregated winter runoff:** First assay the actual deicer chemistry and contaminants; calcium/magnesium salts or glycol invalidate a NaCl-only conversion. Route incompatible or dirty batches to existing permitted management, never to road-brine reuse by default.
- **Regional winter-maintenance consortium:** Several small lined yards share a licensed collection and laboratory service. Each yard keeps a separate inlet-to-destination ledger; hauler manifests and disposal fees enter the economics before expanding the fleet.

## Risks & Mitigations

| Failure or trade-off | Containment and verification |
| --- | --- |
| Freezing, debris, corrosion or valve seizure | Accessible screens, compatible wetted materials, site-designed frost protection and witnessed winter valve/overflow tests; stop capture if movement or flow disagrees with command. |
| Probe drift, changing salt mixtures or unsampled pulses | Temperature compensation, site-specific lab calibration, timed composite samples and blank/duplicate checks; quarantine batches on stale or discordant readings. |
| Full tank, extreme melt or hydraulic backwater | Independent level switch and engineer-reviewed passive route to permitted containment; prohibit installations where flood-safe capacity or lawful disposal is absent. |
| Power/network loss or unauthorized override | Hardwired local interlocks, battery-backed alarm, authenticated changes and append-only operator event records; test de-energized routing in place. |
| Contaminated brine or shifted chloride burden | Test metals, sediment and petroleum before reuse; use licensed treatment/disposal if rejected. Track subsequent road application; diversion is not salt destruction. |
| Maintenance injury, cost and uncertain benefit | Traffic-safe service access, spill and electrical protection, trained operator ownership, two-season matched-yard audit and a stop/go review including source-side salt reduction. |

## Vision for 2050

If cold-weather pilots close the mass balance and regulators approve safe destinations, a 2050 snow yard could publish a traceable inventory for every liter of winter runoff: where it entered, which salts it carried, where it was held and where it ultimately went. The useful future is not thousands of unattended gates claiming to make salt disappear. It is winter maintenance that first uses less salt, then proves what happened to the remainder, with reuse only when it demonstrably displaces new inputs and does not shift exposure elsewhere.

## Sources

[1] https://pubs.usgs.gov/sir/2015/5057 — USGS: Chloride concentrations and loads in Connecticut watersheds
[2] https://doi.org/10.2166/wqrjc.2011.023 — Chloride transport at municipal snow storage facility (2011)
[3] https://doi.org/10.1002/ep.10332 — Salt-water recycling for brine production at road-salt facilities (2009)
