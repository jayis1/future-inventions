# Paddy Water-Table Gate

**Author: jayis1. Status: research concept; performance and cost are unvalidated design targets.**

## Problem

Continuously flooded irrigated rice fields emit methane from anaerobic soil; the International Rice Research Institute (IRRI) describes alternate wetting and drying (AWD) as a way to interrupt that production while saving irrigation water.[1] Its existing perforated field tube tells a farmer when the water table reaches about 15 cm below the surface, but someone must still return to open the irrigation inlet. Access to controllable water and reliable timing are barriers for small irrigated plots; rain-fed paddies and fields without a controllable inlet are not candidates. The proposed users are farmer groups managing small, level, gravity-fed rice plots, not all rice growers.

## Solution

A repairable **mechanical inlet gate** couples two water-level references without a battery or network. A screened, perforated 100 mm HDPE observation tube reaches 20 cm below grade and houses a guided polypropylene float. At a locally calibrated water-table depth of **15 cm below grade**, its linkage releases a spring-closed inlet latch. Irrigation water from an existing *elevated, controllable* canal or tank then enters through a low-head HDPE flap valve. An independent surface-water float in a protected side chamber closes and latches the valve when standing water reaches **3–5 cm above grade**; the underground float must again fall to the lower threshold before another cycle. Stainless pins, a replaceable EPDM seat, and a manual isolation handle allow a local mechanic to repair or bypass the device. The farmer still observes the field and manually holds flooding during flowering, as in established AWD guidance.[2]

The valve cannot create hydraulic head, pump water, drain a field or guarantee uniform soil moisture. It admits water only when gravity supply is available; if the canal is dry, the farmer must irrigate by the usual method. A visible inlet-flow flag and daily field-tube reading reveal a stuck gate. No electrical sensor, person-level data or remote control is included.

## Key Innovation

**AWD and its observation tube are established practice, not inventions claimed here.**[1][2] The proposed delta is a *two-threshold, mechanically interlocked and manually overridable* refill gate that separates the below-grade trigger from the above-grade stop, with a fail-closed inlet and visible fault witness. Unlike an ordinary irrigation timer it responds to the actual field water table; unlike the existing tube alone it can initiate and end an eligible gravity-fed refill. The nearest repository concepts—`atmospheric-methane-oxidation-array` and `peatland-carbon-lock-rewetting-array`—target methane after release or rewetting of peat, not rice irrigation timing. The hard research question is whether a low-cost buried float and valve avoid silt fouling and false triggering across soils and seasons better than a farmer using an ordinary AWD tube.

At a **0.1 ha** level plot, raising ponded water by **4 cm** corresponds to **40 m³** (`1,000 m² × 0.04 m`), ignoring infiltration, rainfall and field storage. At **1 L/s** net supply that increment alone takes about **11.1 hours** (`40,000 L / 3,600 L/h`); a longer refill or a larger inlet may be necessary once infiltration is measured. These are geometry and flow calculations, **not field performance**. The pilot targets lower-trigger repeatability within **±2 cm**, upper-stop within **3–5 cm**, and fewer than **one missed or uncommanded refill in 100 eligible cycles**, all under a defined water-head and silt-load envelope. No methane reduction is attributed to the mechanism until paired field measurement demonstrates it beyond ordinary AWD.

## Target Cost

**Unvalidated 2035 target at 100,000 units/year: US$35 ex-factory** per gate: HDPE tube/valve body US$11, two floats and linkage US$9, stainless springs/pins and EPDM seal US$6, screen and visible flag US$3, assembly/test US$6. Allow **US$15** for fitting and initial calibration and **US$5/year** for cleaning, gaskets and inspection; existing canal, land leveling, pump energy, water charges, transport, finance and taxes are excluded. Over five seasons the modeled hardware-plus-service cost is **US$75/plot**, or **US$15 per 0.1 ha-season** before water costs. A simple IRRI-style observation tube plus human operation is the cheaper baseline; adoption requires measured savings in labor or irrigation water exceeding this incremental cost. Components should be standardized, locally replaceable and recyclable where collection exists; no sealed proprietary cartridge.

## Impact

A proposed trial pairs **100 gate-managed 0.1 ha plots** with **100 matched manually managed AWD plots** across dry and wet seasons, with continuous-flooded plots as a contextual comparator where ethically and agronomically appropriate. Log water-table and ponded levels, flow volume, rainfall, labor, grain yield, soil/irrigation-water arsenic where relevant, and chamber-measured seasonal **CH₄ and N₂O**. IRRI reports that correctly practiced AWD can cut methane and water use, but those figures are **not additional benefits attributable to this gate**.[1][2] Advancement requires no more than **5% yield loss** against manual AWD, a statistically defensible reduction in missed refill events, and a site-specific positive net benefit after servicing. A deployment of 100,000 gates would instrument **10,000 ha of eligible 0.1 ha plots**; avoided emissions and water use cannot be inferred merely from this area.

## Limits, safety and development path

Silt, algae, rodents, debris, gasket wear, floats binding to the tube, storms and changing canal head can cause dry-out or overflow. A spring returns the inlet closed on linkage breakage; a stuck-open fault still requires an upstream manual shutoff, overflow path and daily farmer inspection. Do not use without assessing field leveling and drainage, especially in rain or near flowering; the operator can isolate and revert to normal AWD at any time. Alternating oxic/anoxic soil can increase N₂O, and mitigation varies with nitrogen inputs and site conditions; measure *both gases* rather than reporting methane alone.[2] Also check arsenic uptake and weed pressure locally. No additives, engineered organisms or disposable electronics enter the field.

Within 10–20 years: bench-test float hysteresis, pressure and silt resistance; conduct farmer-controlled paired trials against a plain tube; revise for local fabrication only if the gate beats that baseline; then assess multi-season repair costs and independent climate/yield results. If gravity head or maintenance is inadequate, abandon the gate rather than advertise automatic AWD.

## How It Works

This is a refill-only controller for a level **0.1 ha** plot with an elevated, isolatable inlet. The farmer installs the perforated tube in representative soil, checks its reading against a ruler, sets the lower linkage to **−15 cm** and verifies the independent ponded-water float at **+3–5 cm**. The farmer must also confirm that upstream water will be available when the trigger trips; the gate cannot summon canal water. IRRI's ordinary AWD tube and threshold are prior art.[1] The proposed addition is automatic, mechanically latched refill and shutoff, not a new rice-growing method.

After ponding recedes through evapotranspiration and percolation, the subsurface float descends; only at the lower threshold does it release the spring-loaded latch. Canal head pushes the HDPE flap open, and the separate surface float closes and latches it at the upper stop. That mechanical hysteresis prevents oscillation around a single water level. The flow flag indicates inlet motion, not proof that the soil reached the threshold or that water reached every corner. During flowering, the farmer uses the manual isolation/override and ordinary observation to maintain appropriate water; before harvest, isolate supply and drain through the field's existing drainage practice. A broken linkage closes the inlet, but a stuck-open seat can still flood the plot: both require inspection and an upstream shutoff.

## Technical Architecture

| Subsystem | Physical input → output | Service check |
| --- | --- | --- |
| Screened 100 mm HDPE tube and guided polypropylene float | Local below-grade water level → displacement | Remove silt and compare to a ruler reading. |
| Stainless linkage, spring and two-position latch | Displacement at −15 cm → inlet release | Exercise by hand; inspect corrosion and binding. |
| Low-head HDPE flap, replaceable EPDM seat and surface float | Available canal head → flow; +3–5 cm ponding → closure | Check seat leakage and upper-stop travel. |
| Isolation handle, inlet-flow flag and bund seal | Manual shutoff, visible flow indication and controlled penetration | Inspect erosion/overflow and compacted soil around fitting. |

The physical data path is **field-tube level → linkage/latch → flap → ponded-water float → latched stop**. No battery, telemetry, autonomous drain, or authenticated event log exists in this concept. The flag cannot substantiate carbon credits; any future measurement, reporting and verification (MRV) claim needs independent level/flow records, gas sampling, tamper controls and an accepted method. Site sizing must account for the existing **40 m³ per 4 cm** geometric refill and the **~11.1 h at 1 L/s net** calculation above; infiltration and insufficient canal head lengthen it. Installation duration, valve flow at a defined head and seal leakage remain bench-test questions.

## Performance Benchmarks

The literature comparator is **continuous flooding versus correctly practiced manual AWD**, not this untested gate versus manual AWD. IRRI reports approximately **30% irrigation-water reduction** and **30–70% methane reduction** for AWD under suitable conditions; these are not gate-specific measurements.[1] Soil, season, nitrogen practice and water access alter outcomes.

| Metric and comparator | Published/manual reference | Gate design target or current state |
| --- | --- | --- |
| Water-table re-flood trigger | IRRI tube: about −15 cm below soil.[1] | ±2 cm repeatability at calibrated local head; untested. |
| Refill shutoff | Manual operator observes field. | +3–5 cm ponding; untested. |
| Refill reliability | Site-specific manual AWD baseline to measure. | Fewer than 1 missed/uncommanded event per 100 eligible cycles; untested. |
| Irrigation-water and CH₄ savings vs continuous flooding | AWD: ~30% water, 30–70% CH₄ per IRRI.[1] | No incremental gate saving established; paired trial required. |
| Yield and net greenhouse gases vs manual AWD | Site-specific control required; N₂O can offset CH₄. | At most 5% yield loss as trial exit gate; measure CH₄ and N₂O. |
| Installed cost and energy | Manual tube cheaper; labor/site costs unknown. | US$50 installation including US$35 gate at volume; 0 electrical Wh, unvalidated. |

## Deployment Scenarios

1. **Gravity-fed smallholder cooperative:** An eligible, level 0.1 ha plot with a reliable elevated canal inlet uses one gate, upstream shutoff and overflow route. At the modeled 1 L/s net flow, a 4 cm geometric refill alone takes ~11 hours; a canal rotation shorter than that is a no-go until a larger inlet is tested.
2. **Pump-fed district with elevated header:** A shared tank or canal provides sufficient gravity head *after pumping*; the gate itself uses no electricity but does not eliminate pump energy. Compare metered irrigation volume, pump costs and repair visits against plain-tube AWD before claiming savings.
3. **Cooperative climate pilot:** Matched manual-AWD and gate plots are sampled for seasonal CH₄, N₂O, yield and water delivery. A visible flag helps spot faults but cannot certify avoided emissions; independently auditable measurements and safeguards against double counting are required before any credit revenue is projected.

## Risks & Mitigations

| Failure / consequence | Detection and mitigation; residual uncertainty |
| --- | --- |
| Mud, algae, crabs or rodents bind the float or seat; dry-out or overflow follows. | Daily ruler/flag check, removable screen and scheduled cleaning; measure fault frequency over wet and dry seasons. |
| Canal head disappears, or spring closes a damaged linkage; crop dries. | Inspect source and water table daily, isolate/bypass and irrigate normally; fail-closed protects against uncontrolled inlet flow but not drought. |
| Seat leaks, bund erodes or storm water overtops; adjacent plots flood. | Upstream shutoff, compacted collar, site-specific spillway and neighbor-agreed schedule; reject sites without safe overflow. |
| Soil permeability, uneven grading or flowering-stage drying reduces yield. | Screen soil and field level; pause AWD during sensitive stages, compare matched yields and stop trial if agronomic thresholds fail. |
| Oxic periods increase N₂O, weeds or cadmium uptake on vulnerable soils. | Measure both gases and grain contaminants where relevant, manage nitrogen/weed timing and exclude high-risk soils; effects remain site-specific. |
| Claimed climate benefit exceeds evidence or displaces manual AWD with no added benefit. | Use manual AWD as the incremental comparator; audit paired controls and never treat a flow flag as an emission meter. |

## Vision for 2050

If multi-season trials show that the latch survives mud, saves farmer time and does not sacrifice yield, a standardized, owner-serviceable gate could become a fitting on *eligible gravity-fed bunds*, not a universal paddy accessory. Farmer groups would buy repairable parts locally and coordinate supply windows rather than depend on connectivity. The value proposition would be dependable AWD where manual visits are missed; climate gains would be counted only against the practice a gate actually replaces. The conditional scale cases and their limits are in [IMPACT_ANALYSIS.md](IMPACT_ANALYSIS.md); development gates are in [ROADMAP.md](ROADMAP.md).

## Sources

[1] https://ghgmitigation.irri.org/mitigation-technologies/alternate-wetting-and-drying — IRRI Alternate Wetting and Drying
[2] https://cgspace.cgiar.org/server/api/core/bitstreams/b84fb569-3edf-4058-ba4b-73d4804d7412/content — CGIAR AWD practice brief
