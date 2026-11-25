# Snowmelt Brine Accounting Gate — Impact Analysis

**Author: jayis1** · Illustrative scenario model, not observed performance or a forecast. The [README](README.md) defines the controlled inlet, containment route and pilot tests. All concentrations below are **chloride**, not NaCl-equivalent; use laboratory-calibrated, flow-weighted samples rather than conductivity alone.

## Boundary and method

At each lined, permitted yard, count only water crossing the gate inlet. Let `N` = deployed sites, `V` = annual inlet flow per site (m³/year), `C` = flow-weighted chloride (g/L), `A` = operating availability (fraction of annual inlet chloride mass represented by validated measurements), and `F` = fraction of that available inlet chloride mass actually retained in the isolated tank (including tank-capacity and bypass losses). For a uniform illustrative concentration, `M_retained (kg chloride/year) = N × V × C × A × F`; 1 m³ = 1,000 L and 1 kg = 1,000 g. In field reports replace `V × C` with the sum of measured event volumes and concentrations, and independently reconcile inlet, tank, containment branch, overflow and escape. Availability is a **mass-weighted** share, not just uptime in hours.

| Hypothetical case | N sites | V m³/site/year | C g chloride/L | A | F | Retained chloride, kg/year | Tank volume/site/year if captured at representative C |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 10 | 300 | 1 | 0.70 | 0.40 | 840 | 84 m³ |
| Central | 100 | 1,000 | 2 | 0.85 | 0.60 | 102,000 | 510 m³ |
| High | 1,000 | 2,000 | 4 | 0.90 | 0.70 | 5,040,000 | 1,260 m³ |

These are deliberately broad, **assumed inputs**, not site measurements or a predicted adoption curve. All retained mass is a temporary inventory until a documented destination is known. A 1 m³ pilot tank therefore requires many emptying/transfer cycles or appropriately permitted additional holding capacity (for example, 510 m³ captured annually at a central-case site); it does not hold an entire season. Event peaks, winter freezing and hazardous contaminants can make any scenario infeasible.

## What counts as benefit

Tank retention is **not** permanent chloride removal. Existing permitted detention may already prevent or manage some discharge; the incremental comparison is gate-equipped yard versus the same yard's measured baseline, including overflow and lawful disposal. Report separately: (1) measured tank mass; (2) mass sent to permitted treatment or off-site disposal, with manifests and its actual end fate; (3) mass reused on roads and subsequently at risk of release; and (4) changes in newly purchased road salt, deicer application and downstream chloride. Do not add these categories together as avoided pollution. Net avoided release requires documented permanent treatment/disposal or independently measured source reduction and a compatible receiving-water boundary; no avoided-release tonnage is claimed here.

For illustration only, if **all** central-case retained chloride were reused on roads, the yard's isolated inventory would be 102 metric tonnes/year but verified permanent prevention could be **zero**. If approved disposal permanently isolates a share `D`, then potential avoided mass at the defined receiving-water boundary is at most `M_retained × D`, *less* leaks, disposal emissions/returns and any displaced baseline treatment; `D` remains unknown until destination auditing. Source-side salt optimization is an alternative comparator, not an automatic additive gain.

## Cost and adverse effects

The README's unquoted allowance is US$2,800–4,500 ex-workshop plus US$1,500–4,000 tie-in per already-lined site: **US$4,300–8,500/site** before permits or contingency, or **US$430,000–850,000 for 100 central-case sites** under identical-site assumptions. Recurring parts, calibration and laboratory allowance is US$350–900/site/year (**US$35,000–90,000/year for 100 sites**), excluding labor, power for frost protection, transport, treatment, disposal, sampling escalation and taxes. These are not bids or lifecycle-cost estimates. The <10 W controller target implies <87.6 kWh/year if held continuously; site heating or pumping could dominate. Record embodied impacts of HDPE, stainless steel, batteries and travel rather than asserting net carbon savings.

Potential harms include more chloride on roads if reuse increases application, contaminated batch spills, displaced impacts at disposal facilities, hydraulic backwater, flood exposure and maintenance injury. Lab assays for sodium, metals, solids and petroleum, containment inspection, licensed destination records and downstream monitoring are needed before attaching ecological or health claims. A two-season pilot should publish confidence intervals for flow and concentration, sampling bias, unmeasured storm events, rejected batches and missed faults; if closure exceeds the ±15% pilot goal, no scenario mass should be presented as validated.
