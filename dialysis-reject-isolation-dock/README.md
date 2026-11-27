# Dialysis Reject Isolation Dock

**Author: jayis1**
**Status: Research concept (TRL 2)**

## Problem

Dialysis water plants reject a variable fraction of their incoming water while making purified water for treatment. A US hospital's 11-machine unit estimated 927,000 L of reverse-osmosis (RO) reject in a year, but that is one site's accounting, not a universal per-treatment figure.[1] In water-stressed regions, discharge of potentially reusable reject adds pressure to supplies used by patients and neighbors. Existing recovery schemes already route qualified reject to toilets and landscaping.[2] The hard retrofit problem is making that reuse demonstrably incapable of feeding water back toward a clinical RO circuit, or admitting disinfection rinse, saline flushes, and off-spec water into a reuse tank.

## Solution

A facilities-engineer-installed **isolation dock** accepts *only* the RO plant's identified reject outlet at an engineer-approved reject-side tie-in, without changing its clinical product-water path. A visible, inspectable open air gap above a catch funnel breaks any hydraulic return path. A normally de-energized spring-return diverter sends all water to the existing permitted drain by default; a separate normally closed tank-inlet valve provides an independent cutoff if the diverter sticks toward reuse. Only after a site-specific sample qualification and verified valve/air-gap commissioning may a timed batch enter a sealed, labeled **nonpotable** HDPE tank. Conductivity, temperature and flow are logged for each batch; a maintenance-cycle signal from the RO plant vetoes capture, but a missing or incorrect signal also forces drain. A tank-overflow standpipe returns to the approved drain without a pressure connection to the clinical line. A separate pump serves a physically segregated toilet-flushing loop, never a dialysis, handwashing, cleaning, drinking or food-contact outlet.

**Proposed test envelope, not established performance:** an existing 1–5 m³/day reject stream at 5–35 °C, with an installed drain able to take the entire flow even while the dock is offline. Capture target ≥50% of *site-measured, qualified* reject volume during eligible hours; exclude flushes and out-of-range batches. Water quality must meet local nonpotable-reuse rules and the actual destination's microbiological/chemical limits; conductivity alone cannot prove safety. An independent plumbing and infection-prevention review determines whether a particular site can use any water at all.

## Key Innovation

RO reject reuse is **prior art**, not a new purification process.[2][3] The research contribution is a repairable, physically inspectable **one-way reject-only boundary** paired with batch-level source accounting: an open air gap upstream of every reuse component, a de-energized-to-drain valve, and a mass-balance record separating reject, flush, overflow and delivered nonpotable water. Unlike the repository's *Regenerable Dialysate Kidney Belt*, this device never touches blood, dialysate or product water and never changes treatment settings. Unlike water-treatment kiosks, it does not claim to purify reject or make it drinkable. Whether this package improves safety or net water savings relative to a well-designed conventional reuse retrofit is an open comparative question.

## Target Cost

**Unquoted planning estimate at 1,000 docks/year by 2038:** US$2,400 ex-workshop: stainless open-gap/funnel and guarded cover $450; rated diverter, independent inlet valve and drain manifold $380; conductivity/temperature/flow instruments $430; 24 V controls and backup for safe shutdown $300; 1 m³ HDPE tank and overflow fittings $500; assembly and leak checks $340. Target installed cost ≤US$5,000 at a site with an existing suitable drain and nearby toilet loop; dedicated nonpotable plumbing, permits, site assays and structural work are extra. Budget an unvalidated US$300/year for seals, calibration and cleaning, plus local laboratory testing and licensed plumbing labor. Five-year service life is a design target; recycle steel/electronics and replace the HDPE tank when damaged. No payback claim follows from these estimates.

## Impact

At a qualifying site, the outcome is **metered mains-water displacement at a nonpotable endpoint**, not all captured reject: compare matched operating periods with the maintained existing RO/drain arrangement, measuring inlet feed, RO product, reject, flush, drain, tank overflow and actual toilet use. Report extra pump electricity, cleaning water, rejected batches, laboratory costs, outages and health incidents. A 10-site, one-year pilot target is ≥50% eligible-reject capture, zero observed cross-connections and no deterioration in site-approved reuse-water criteria; zero observed events is not proof of zero risk. Benefits cannot be generalized to clinics with little reject, unsuitable quality, no local demand or insufficient maintenance. Salts are not removed: diverted water still carries them to the sewer after toilet use. Stop capture if quality, backflow or operating records fail; retain normal dialysis operations and the original drain path. Prove the physical boundary and water savings in benchtop and supervised site trials within 10–20 years before wider adoption.

## Evidence and limits

1. [Thinking Globally, Acting Locally: Water Use in a Hospital Hemodialysis Unit](https://pmc.ncbi.nlm.nih.gov/articles/PMC12282630/), *Kidney360* (2025): measured and estimated one-hospital water accounting; site specifics matter.
2. [Sustainable Kidney Care, How-to Guide: Reverse Osmosis Water Reclaim](https://skc.ukkidney.org/static/how-to/01.%20How-to-Guide%20Reverse%20Osmosis%20Water%20Reclaim.pdf): established reuse pathways and need for local water-quality assessment.
3. [Water conservation and circular water reuse in clinical haemodialysis facilities: a scoping review](https://link.springer.com/article/10.1007/s11255-026-05378-9), *International Urology and Nephrology* (2026): reuse evidence is heterogeneous; historical reject fractions cannot be assumed for modern plants.

All performance and cost figures for this dock are unvalidated design targets, not measurements or certification.

## How It Works

The input is **RO reject**, not spent dialysate or the clinical product-water stream. A licensed installer identifies the reject-side tie-in and proves that the RO manufacturer's venting and drainage limits remain intact. Reject falls through a guarded, inspectable, code-sized open air gap into a 316 stainless funnel: no downstream tank pressure or siphon can hydraulically return across that break. The funnel and its full-flow overflow drain must pass the measured peak flush flow, not just the daily average.

On startup and whenever evidence is missing, the 24 V spring-return diverter points to the permitted drain and the independently powered tank-inlet valve stays closed. After site assays, inspection and a valid RO operating-state signal, a qualified batch may pass both valves into a labeled 1 m³ HDPE nonpotable tank. A separate low-level-protected pump feeds only approved toilet cisterns. Flow meters distinguish admitted reject, tank overflow, drain flow and water actually delivered; conductivity and temperature screen excursions but never certify microbial or chemical safety. On a lost signal, full tank or stale assay, capture stops and flow goes to drain. If the diverter jams toward the tank, the independent inlet valve closes; if the drain itself blocks, personnel follow the hospital's RO contingency plan rather than throttling the clinical reject outlet. Neither controller nor alarm is the physical isolation barrier.

## Technical Architecture

`RO reject outlet → approved vented tie-in → visible air gap → catch funnel → spring diverter → permitted drain OR normally closed inlet valve → nonpotable tank → segregated pump → approved cisterns`. Funnel and tank overflows return independently to the full-capacity permitted drain. The clinical feed, RO product and dialysate plumbing have **no downstream connection** to this path. A separately approved air-gapped potable makeup route, if needed, cannot be a pressurized tank connection.

The control layer records RO run/clean state, valve-position feedback, tank level, calibrated conductivity/temperature, flow and batch identity. Its interlock requires current laboratory qualification and all positive permissives; contradictory feedback, sensor drift or power loss removes permission. Onsite facilities staff own inspections, assays, alarms and tank quarantine; records support a reject-to-drain-to-delivery mass balance. Installation requires code review, non-interchangeable fittings, electrical isolation and supervised single-fault tests under the conditions in [SPECIFICATION.md](./SPECIFICATION.md).

## Performance Benchmarks

| Metric and comparison | Proposed acceptance target; not a measured result |
|---|---|
| Physical isolation vs ordinary direct-to-drain RO reject | No detectable tracer or pressure return across the inspected air gap during site-peak-flow, blocked-outlet and reverse-pressure bench challenges; verify gap dimensions against local code. Direct-to-drain is the safety reference, **not** an inferior reuse technology. |
| Fault response vs continuous drain baseline | Tank inlet closes and drain routing is confirmed within 5 s of power/signal loss or injected sensor fault at the site's measured maximum instantaneous reject flow; test a mechanically jammed diverter separately. A blocked drain needs the clinical contingency procedure, not a promise of uninterrupted capture. |
| Capture vs zero recovery from a site with no existing reuse | ≥50% of *eligible, site-qualified* reject reaches tank during a 10-site, one-year pilot; report eligible hours and all excluded flushing, cleaning and out-of-range volume. Compare an existing approved reuse system on equal boundaries where one exists. |
| Useful displacement vs captured volume | Meter delivered toilet water and matched-period mains makeup separately; report both, tank overflow, extra kWh, cleaning water, assays and nuisance alarms (design goal ≤1 false alarm per 100 operating hours, to be tested). |

A published 11-machine US hospital estimated **927,000 L/year** of RO reject in 2023, not a measured dock result or a transferable clinic baseline.[1] The paper's online date is 2024; the “2025” year in the existing reference above should not be used as the study's publication date. No head-to-head state-of-art advantage is established: conventional approved RO-reject reuse already exists.[2][3] Every target above requires reproducible tests and independent clinical, plumbing and infection-prevention approval before use.

## Deployment Scenarios

1. **Hospital dialysis wing:** A facility with an accessible RO reject outlet, full-flow drain and nearby permitted toilet loop runs drain-only shadow monitoring, then trials approved batches with licensed plumbing and clinical engineering sign-off. Treatment settings are unchanged.
2. **Water-stressed regional clinic:** If local nonpotable rules, assay results and staffing permit, an inspected tank can shift qualified reject to a segregated cistern loop; absent reliable testing or demand, it remains drain-only.
3. **Multi-site health system:** Standardized logs reveal which facilities actually displace mains water and which have poor reject quality, insufficient demand or excess maintenance cost. Only qualified sites proceed beyond observation.

## Risks & Mitigations

- **Wrong stream or chemical carryover:** Non-interchangeable labeled tie-ins, RO cleaning-state veto and site-specific assay panels; quarantine the tank on uncertainty. A missed cleaning signal remains a residual risk until independently challenged.
- **Backflow, leak or blockage:** Inspectable air gap, independent tank cutoff and overflow, full-flow drain sizing and spill containment; pressure/tracer and jammed-valve tests precede installation. A blocked *site drain* still threatens RO operation and invokes the manufacturer's contingency, never a bypass.
- **Microbial growth and drifting sensors:** Limit storage age to a site-validated interval, sample at the point of use, clean and calibrate on a documented schedule. Conductivity cannot establish pathogen absence; failed samples mean no reuse.
- **Economics and operations:** Dedicated plumbing, assays, labor and pump energy may exceed water value; measure actual delivery and stop or retain drain-only operation where net benefit is absent. No zero-risk claim follows from a pilot with zero observed events.

## Vision for 2050

In a conditional 2050 scenario, qualified dialysis facilities treat reject as an auditable, separately plumbed nonpotable resource rather than an automatically disposable stream. A technician can see the physical break, trace every delivered litre and safely revert to the original drain in one fault. Better RO efficiency may reduce available reject, and many sites will not qualify; success means verified water stewardship without compromising patient water, not universal installation. See [ROADMAP.md](./ROADMAP.md) and [IMPACT_ANALYSIS.md](./IMPACT_ANALYSIS.md) for gates and transparent projections.
