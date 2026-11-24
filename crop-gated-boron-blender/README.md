# Crop-Gated Boron Blender

**Author: jayis1** · Research concept (TRL 2) · 2026-11-24

A non-potable, cooperative-scale irrigation module that removes only as much dissolved boron as a locally tested crop requires, while refusing to route unsuitable water to sensitive beds. This is an untested engineering proposal, not an approved irrigation treatment.

## Problem

Boron is necessary in trace amounts but excess in irrigation water injures sensitive crops. FAO's general interpretation puts boron below 0.7 mg/L in its no-restriction category, 0.7–3 mg/L in slight-to-moderate restriction, and above 3 mg/L in severe restriction; crop-specific tolerances and soil conditions matter.[1] Salinity and sodium hazards are separate: removing boron alone cannot make a saline source suitable for irrigation.[1] Water-stressed farms can lose access to otherwise useful sources or unknowingly accumulate boron in root zones. This is a crop and water-quality problem, not a claim that a known number of people will benefit.

## Solution

A 1 m³/day pilot diverts pre-screened irrigation water through a washable particle screen and a sealed bed of commercially available **N-methyl-D-glucamine (NMDG) functionalized resin** in a polypropylene or HDPE housing. Vicinal hydroxyl groups bind dissolved boron; selective NMDG resins and their regeneration are established art.[2] A tamper-evident manifold combines qualified treated water with untreated feed in a covered mixing tank; a normally closed, keyed batch outlet stays locked until a trained operator receives an independent passing result for the *mixed* batch against the agronomist's crop- and soil-specific boron limit. The key is held by the cooperative's quality custodian; a mechanical seal and batch ID make unauthorized opening visible, but cannot prevent deliberate bypass or a dishonest custodian. No continuous boron sensor or online claim of potability is assumed. A visible sampling ledger records inlet, post-resin and mixed-batch boron, electrical conductivity (EC), sodium adsorption ratio (SAR), pH, flow and cartridge service history. A batch failing any local irrigation-quality criterion goes to an isolated hold tank for retesting or an approved alternative use, **not** to the crop or a drain.

**Unvalidated test envelope:** 1.5 mg-B/L feed, 0.6 mg-B/L treated stream, 1.0 mg-B/L mixed-batch target for a crop whose local advisory accepts that limit; a different sensitive crop may require a much lower limit. At an assumed 50:50 blend, the arithmetic mixed concentration is 1.05 mg-B/L, which **fails** the example 1.0 mg-B/L target. The valve therefore needs at least a 56% treated fraction under those assumed concentrations, with measured confirmation before release. A 100 L treated batch removes approximately 90 mg of boron at the assumed inlet and outlet concentrations; these figures are mass-balance targets, not measured resin capacity or a promise of yield benefit. Adsorption performance depends on feed chemistry, contact time, flow, resin condition and temperature.[2]

## Key Innovation

The proposed research contribution is a **crop-specific, batch-verified blending gate** tied to both boron and EC/SAR qualification, not a new resin, general desalination method or drinking-water kiosk. Unlike the repository's fluoride-exchange-water-kiosk (fluoride drinking water, alumina) and electroferrate-arsenic-remediation-network (arsenic oxidation/iron capture), this targets boron-limited *irrigation* at the field allocation point. Unlike the photothermal-forward-osmosis-desalinator, it does not remove bulk salts or produce drinking water. The hypothesis to test is whether selective treatment plus verified blending can use less resin, regenerant and energy per cubic metre of crop-qualified water than treating all irrigation water with a maintained commercial boron-resin unit. Resin chemistry and blending are prior art; this particular integration has no demonstrated novelty or patent claim.[2]

## Target Cost

**Unquoted planning target, 2038 USD at 10,000 units/year:** US$850 ex-workshop for a 1 m³/day housing, manually operated batch gate, sampling ports and first cartridge; annual cartridge service, laboratory assays, transport, skilled operation, treatment of spent regenerant, installation, pumps and power are **excluded** and must be priced in the pilot. A go/no-go economic test is **lower audited cost per m³ of crop-qualified water** than a maintained full-flow commercial boron-resin treatment train on the same feed, counting every batch assay, operator, exchange and lawful waste handling. Daily independent laboratory release testing may make even this comparison unfavorable; the US$850 hardware target is not a delivered-water price. If testing and safe residue management dominate cost, use a suitable alternate source or change crops instead.

## Impact

At 1 m³/day and 200 operating days/year, one fully qualified module could route at most 200 m³/year to irrigation; 1,000 modules would have a *nameplate upper bound* of 200,000 m³/year, not measured safe water, avoided crop loss or a population served. A 10–20-year path is contained column tests (years 1–3), paired field trials with crop/soil monitoring and maintained commercial treatment controls (years 4–8), then regulated cooperative deployment only if quality, waste and total cost pass independent review (years 9–15). No farm-user tracking, remote connectivity or proprietary cloud is needed; housings and valves should be locally repairable.

## Safety, limits and validation

- **Before any pilot:** Characterize seasonal boron, EC, SAR, chloride, pH, microbial and site-specific contaminants; obtain local water and waste permissions. The module is **not for drinking** and does not disinfect or desalinate. Soil boron and actual crop response require agronomic monitoring; a good water sample is not proof of safe soil or improved yield.[1]
- **Breakthrough or bad assay:** Sample the outlet and mixed batch for each release using a qualified laboratory method with field duplicates and periodic independent splits. Confirm the batch *after blending*, not merely the resin outlet. Track resin volume and service life from measured breakthrough curves, never a calendar-only assumption. An invalid, delayed or failed result keeps the normally closed crop valve shut. A hand-operated valve must not bypass the sealed batch gate.
- **Power, leaks, extremes:** Gravity feed where feasible; no power should be required to close the gate. Lock closed on missing samples, blocked flow, visible leakage, broken seals or flooding. Protect resin against freezing, heat and drying; requalify after exposure. A safe backup is an independently qualified water source, not an override of the gate.
- **Waste:** Exchange sealed exhausted cartridges at a trained regional hub. Acid elution and alkaline reconditioning of NMDG resin are existing practice but require containment, PPE, rinse verification and lawful treatment/disposal of boron-rich regenerant and spent resin; do not regenerate or dump at the farm.[2] If no licensed residue route exists, do not deploy. Compare net water, chemicals, energy and lifecycle impacts against alternative crops, source blending and established treatment.
- **Falsification:** Reject the design if batch assays miss breakthrough, EC/SAR or boron remain unsuitable, the gate can be bypassed in ordinary use, seasonal operation exceeds the cost goal, or the comparator achieves equal crop-qualified delivery with less waste and lower total cost. No health, yield or environmental performance is claimed before trials.

## How It Works

The cooperative first maps each field to an agronomist-approved irrigation specification: crop and growth stage, soil boron trend, allowable mixed-water boron and separate EC/SAR limits. Source water is screened and split between a sealed NMDG-resin column and an untreated line. Operators measure each stream and choose a treated fraction using the planning balance `C_mix = f × C_treated + (1 − f) × C_feed`, with concentrations in mg of elemental B/L and `f` by measured volume. For the illustrative 1.5/0.6 mg-B/L streams, a 1.0 mg-B/L ceiling requires `f ≥ 0.556`; the 56% setting is only a starting point, not a release certificate. Mix a labeled batch, take a representative sample after mixing, and release it through the keyed gate only on a current passing laboratory result and an intact batch seal. Log total applied volume as well as concentration: at 1 mg-B/L, each cubic metre carries 1 g of boron into the field. A failed or untested batch remains isolated; stopping boron treatment does not make untreated water safe.

## Technical Architecture

The hydraulic path is `source → screen → split → resin / bypass → covered mixing tank → sample point → normally closed crop gate → assigned field`; a separate hold tank receives rejected batches. HDPE/polypropylene wetted parts, replaceable sealed resin cartridges, flow meters on both legs, a level gauge and lockable manual valves keep the research pilot serviceable without network access. The ledger binds sample IDs, source and cartridge IDs, field assignment, volumes, lab results, seal check and gate release signature. Laboratory boron analysis is the measurement of record; EC, pH and SAR qualification need their own sampling and interpretation, not a claimed online boron sensor. A crop switch, changed feed, lost record, suspect flow meter or missing residue route requires a new qualification. An operator cannot convert a failed result into a pass by changing a setpoint; independent audit must test whether the physical bypass can be misused.

## Performance Benchmarks

| Metric | Existing reference or baseline | Proposed pilot acceptance target (unverified) |
| --- | --- | --- |
| Boron suitability | FAO's general irrigation guidance: <0.7 mg/L no restriction; 0.7–3 mg/L slight/moderate; >3 mg/L severe, subject to crop and soil context.[1] | Every released batch passes its *local crop-specific* limit on the mixed sample; no universal 1.0 mg/L promise. |
| Batch accounting | Existing full-flow commercial boron-resin treatment of the same source is the trial comparator; its performance is not specified here.[2] | Reconcile inlet, treated and bypass volumes to within 5% in controlled trials; investigate every deviation. |
| Gate reliability | No measured prototype or field baseline exists for this integration. | Zero releases of deliberately failed, stale or unmatched test batches in a supervised fault-injection trial; record number of attempted faults and any bypass. |
| Cost and resources | Existing resin chemistry is established, but comparable delivered cost depends on local assays and waste handling.[2] | Lower audited cost and regenerant use per m³ of *crop-qualified* delivery than a maintained full-flow control on matched water; reject if neither advantage holds. |

These are test criteria, not achieved results. Record laboratory uncertainty, flow calibration, rejected batches, downtime and residue volumes alongside passing results; a low boron reading alone cannot establish irrigation suitability.

## Deployment Scenarios

- **Cooperative vegetable beds:** Allocate separately sampled batches to sensitive crop plots only after local agronomic approval; other crops may use a different approved specification, never a silently shared gate.
- **Brackish groundwater edge case:** Trial boron reduction only where separate EC/SAR, chloride and soil assessments already permit irrigation; otherwise use a different source or treatment train, not this cartridge as a desalination substitute.
- **Seasonal drought reserve:** A monitored cooperative can evaluate marginal water in a contained pilot when the primary source is unavailable, while holding failed batches and budgeting for laboratory turnaround and lawful cartridge return.

## Risks & Mitigations

The hardest failure is a plausible-looking certificate for the wrong batch or field. Require numbered sealed batches, independent duplicate sampling, a custodian-held key and periodic blind audit; none prevents collusion or deliberate plumbing bypass, so inspect the manifold before every release. Resin breakthrough, meter drift and variable feed chemistry can invalidate the calculated blend: sample all three points, calibrate meters and requalify after source or cartridge changes. Limited low-boron output may make a target mathematically unreachable; do not release a near-miss. Mixed crops, cumulative boron loading and poor drainage require soil monitoring and field-specific allocation, even when water passes. Pump failure, freeze damage, leaks or power loss leave the gate closed and the batch in containment. Acid/alkaline regeneration and boron-rich waste belong only at a permitted regional facility; no disposal route means no deployment. Laboratory delays and operating costs may erase the proposed advantage entirely.

## Vision for 2050

Conditional on successful independent field trials, locally governed water cooperatives could use batch-verified boron blending as one option in a broader irrigation-quality toolkit. Repairable cartridges and transparent batch ledgers might make small marginal sources usable for selected fields without treating every litre to the strictest crop limit. This is not a forecast: soil monitoring, crop-specific decisions, affordable assays, secure custody and lawful waste management remain necessary at any scale. Where those prerequisites fail, the right 2050 outcome is to choose another source or crop, not to deploy this machine.

## Sources

[1] https://www.fao.org/4/x5871e/x5871e07.htm — FAO Water quality and crop production
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC9517912 — Liu et al. 2022 boron removal review
