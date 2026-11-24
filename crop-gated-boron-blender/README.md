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

## Sources

[1] https://www.fao.org/4/x5871e/x5871e07.htm — FAO Water quality and crop production
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC9517912 — Liu et al. 2022 boron removal review
