# Dialysis Reject Isolation Dock — Test Specification

**Author: jayis1** · Research only; not an approved dialysis or plumbing device.

## Physical boundary and materials

- The hospital RO manufacturer's reject outlet and product-water route remain untouched except for a professionally approved, vented reject-side tie-in. A dedicated visible air gap above a stainless 316 catch funnel must be dimensioned and inspected to the applicable local backflow code; its overflow cannot splash onto product-water equipment. No valve, tank, pump or pipe downstream of this gap connects to the clinical feed or product circuit.
- A spring-return, 24 V diverter defaults to a drain approved for the full reject rate. A separately powered normally closed tank-inlet valve, tested for single-fault isolation, sits in series on the reuse leg; a full-flow funnel overflow and an independent tank overflow also lead to the approved drain. The reuse line leads to a lidded 1 m³ food-grade HDPE tank, labeled **NONPOTABLE**. Use a non-interchangeable connection and dedicated nonpotable plumbing. Size vents, spill containment and drain after measured maximum plant flush rates; never put backpressure on the RO outlet.
- A calibrated flow meter counts reject admitted to the tank, another counts delivered toilet water, and the drain/overflow is independently metered during pilot trials. Conductivity and temperature flag changes, but acceptance requires a periodic laboratory panel specified by the facility (including microbiology, local salts/metals and residual cleaning chemicals). Trend alarms supplement—not replace—assays.

## Operating logic

1. Start in drain state on every power-up; the facilities operator inspects the gap, tank, drain, valve position, calibration and water-quality release record.
2. Permit tank capture only with a current approved water-quality qualification, valid RO operating-state signal, in-range calibrated readings, tank space and a commissioned drain. A missing signal, stale calibration, sensor disagreement, full tank or scheduled RO disinfection immediately returns flow to drain.
3. The nonpotable delivery pump cannot supply a clinical or potable endpoint; a distinct labeled pipe terminates at approved toilet cisterns. A low tank level shuts off that pump; a separately code-approved potable makeup path, if used, needs its own compliant air gap and must not connect directly to the tank under pressure.
4. Flush, chemical cleaning and uncertain streams always discharge to the permitted drain. Existing clinical treatment continues independently; the dock is removable without changing RO settings.

## Failure modes and tests

| Fault | Safe state | Qualification test |
|---|---|---|
| Power loss, wire break or controller freeze | Spring diverter to drain; pump off | Cut every supply under maximum measured reject flow; verify full drainage with no RO backpressure |
| Blocked drain or overflowing funnel | Stop capture; shut down dock and invoke hospital-approved RO contingency, never block clinical reject | Simulate blocked downstream route under facilities supervision; verify alarm and independent spill containment |
| Sensor drift, failed conductivity probe, stale lab qualification | Divert to drain; quarantine tank until independently sampled | Inject sensor faults and expired records; verify capture cannot restart on reboot |
| RO disinfection or unknown operating state | Divert to drain; hold previously captured batch if chemical ingress suspected | Replay all cleaning/flush states and loss of plant signal; assay tank for the site's cleaning agents |
| Valve stuck toward tank or tank overflow fault | Independently isolate tank inlet and alert staff; preserve gap and drain | Mechanically jam valve in supervised bench rig; prove independent cutoff and overflow capacity |
| Wrong pipe connection, back-siphon or tank contamination | No installation/release until inspected; quarantine and clean tank | Tracer challenge, visual pipe survey, code inspection and microbiology sampling |

No prototype may claim safe failure solely from software flags; verify all mechanical states under single-fault and maintenance conditions. An unresolved blockage can threaten the dialysis RO plant: follow its manufacturer's shutdown and clinical contingency procedure, never bypass a treatment-system alarm to save water.

## Validation and go/no-go

Bench-test with dyed water at site-matched pressure, flow and temperature before any hospital tie-in. Independent licensed plumbers and clinical engineering staff sign off the open gap, backflow protection, full-rate drainage and electrical isolation; infection prevention and the local regulator approve permitted nonpotable endpoints. Then run a drain-only shadow phase before any tank release. Compare a 10-site, one-year supervised pilot with the maintained existing drain or approved reuse arrangement, recording every diverted litre, actual mains displacement, outlet assays, energy, cleaning, failed batches and operator time. Gate wider use on demonstrated no pressure return under tested faults, compliance with each site's reuse rules, and independently verified net water benefit after all consumables and losses. If any gate fails, retain drain-only operation and redesign.
