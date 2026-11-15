# Maternity Gas-Loss Witness

**Author: jayis1**

**Status: concept (TRL 2); not a medical-gas device approved for clinical use**

## Problem

Nitrous oxide/oxygen analgesia remains an option for many people in labour. At some hospitals, pre-mixed gas is lost from cylinder banks, regulators, joints or distribution pipes *before* reaching a patient. This adds climate emissions without improving care; the remaining exhaled gas also requires occupational-exposure controls. A UK/Ireland consensus reports that pre-use losses from piped pre-mixed nitrous oxide/oxygen could approach half of annual turnover in some settings, but site-specific measurement is essential.[1] Millions of births and healthcare workers globally make this a meaningful class of infrastructure problem, not a claim that all sites leak at that rate. The existing recommended response is to audit the supply system, repair leaks, right-size stock and, where appropriate, change the supply arrangement; this invention is a way to make those decisions reproducible, not a substitute for them.[1][2]

## Solution

A **service-only, non-patient-connected audit cart** records two independent views of maternity gas loss: (a) reconciled bank inventory from weighed cylinders and pressure/temperature records; and (b) staged pressure-decay traces from *out-of-service, isolated and authorised* sections of the medical-gas installation. An authorised medical-gas engineer chooses each test boundary from the site's verified schematic, attaches a certified pressure transducer through an approved test port, and compares a section with an adjacent reference and a blinded leak standard. An offline display classifies results as **unverified**, **investigate** or **eligible for engineer review**; it never labels a clinical line safe or actuates a gas valve. The local engineering/clinical team then decides whether to repair a leak, decommission an unused branch, move to point-of-care cylinders, or leave the system unchanged. Ordinary licensed maintenance procedures, continuity checks and clinical approval govern every isolation and return to service.

Physical parts: a repairable wheeled steel enclosure; two calibrated 0–10 bar pressure channels compatible with the installation's rated service envelope; surface temperature probes; a cylinder platform scale; a mechanically sealed, removable calibration reference; medical-gas-compatible 316L tubing and approved keyed fittings on the *test-only* interface; battery-backed offline recorder and paper report. All wetted materials and cleaning processes must be independently qualified for the actual gas/oxygen service. **No non-certified equipment is connected to an active patient supply.** The cart measures pressure and inventory, not gas composition, clinical demand or a person's behaviour.

**Unverified design targets:** detect a repeatable equivalent loss of 0.1 standard litres/minute from a 100 L isolated test volume over a 20-minute test under controlled temperature; limit the test-port assembly's own equivalent leakage to one-tenth of the detection threshold; complete a single authorised section test in under 45 minutes excluding isolation and recommissioning. The volume, temperature stability, sensor resolution and detection limit must be validated together; shorter traces cannot be interpreted by applying this target mechanically to every manifold.

## Key Innovation

The proposed integration is a **paired inventory-and-isolated-section witness with an explicit uncertainty budget and commissioning handoff**. Existing leak testing, cylinder weighing, gauges and portable supply are prior art.[1][2] A pressure decay alone cannot distinguish a leak from a cooling cylinder or a faulty test seal; an inventory discrepancy alone cannot locate the loss. This cart tests a known reference and its own blank, logs site temperature and cylinder exchange, then presents the two observations separately with their uncertainty. A gated report distinguishes suspected pre-use loss from clinical consumption *without claiming to measure individual patient usage*. Its value over a competent existing engineer-led audit must be demonstrated in a blinded comparison: faster localization, fewer false repair calls, and a higher fraction of cylinder losses actually reconciled after repair. No patentability or global first-of-kind claim is made.

Unlike the repository's [Biogas Breakthrough Guard](../biogas-breakthrough-guard/), this system audits loss from medical-gas infrastructure rather than removing H₂S from fuel. Unlike the [Refrigerant Reclamation Microcart](../refrigerant-reclamation-microcart/), it neither recovers gas nor processes an appliance charge. Existing volatile-anaesthetic capture devices treat *exhaust after clinical use*, not leaks before administration; activated carbon volatile-agent beds do not establish nitrous-oxide capture.[3]

## Target Cost

**Unquoted planning target for 2038 at 1,000 carts/year:** US$1,800 ex-workshop per cart: pressure channels/fittings 400; scale 280; battery and logger 220; qualified test head and calibration reference 350; enclosure 250; assembly and production checks 300. The sum is US$1,800. Excludes certification, installation/site adapters, taxes, transport, engineer labour, metrology traceability and repairs. Budget an additional **US$250/year target** for calibration, seals and battery maintenance, not a supplier quote. At 100 section investigations per year over five years, straight-line cart plus service allocation is US$6.10/test before labour and site downtime; this is not a projected hospital payback.

## Impact

A planning trial of 50 facilities will compare inventory-reconciled nitrous oxide supplied and clinically accounted for, before and after engineer-approved repairs or supply changes, with matched unaffected sites where feasible. A hypothetical facility reducing **100 kg N₂O/year** of demonstrably avoidable *pre-use* losses would avoid that gas emission, before subtracting transport, maintenance and manufacture; this is a scenario, **not a measured saving or universal baseline**. An initial network of 1,000 qualifying facilities achieving this verified increment would avoid 100 tonnes N₂O/year; do not multiply by total cylinder turnover or claim that post-use exhaled gas is also eliminated. Benefits to occupational exposure require separate representative personal monitoring and competent interpretation, not this cart's pressure readout.[2] If measured leakage is already low or point-of-use supply is simpler and safer, do not install a cart as a permanent fixture; the output may be a recommendation to eliminate the pipeline instead.

## Operating limits and validation gates

- **Care first:** only trained medical-gas engineers use the cart during an approved shutdown, on an independently confirmed isolated out-of-service section, using only the test medium and pressure specified by the authorised site procedure. The unit never controls or interrupts treatment, substitutes for the hospital's gas alarms or changes analgesia choices. Clinical staff and the authorised engineer sign off isolation, backup supply, return-to-service tests and documentation under local medical-gas standards. If an isolation cannot be proved safe, cancel the test.
- **Measurement limits:** a dropping pressure is not proof of a particular leak; temperature drift, regulator creep, cylinder inventory errors and the cart's own seal can all mimic one. Run a sealed blank and known leak reference, record uncertainty and recalibrate after any failed check. Both a false negative and a false positive trigger independent engineering confirmation. No concentration, cleanliness or patient-safety clearance follows from this test.
- **Fault state:** on power loss, calibration failure, unexpected demand, wrong fitting or missing boundary approval, record **unverified** and disconnect only under the engineer's procedure. No automatic isolation, bypass, purge or improvised adapters. Use oxygen-compatible certified components and cleanliness processes; do not introduce grease, spark-producing equipment or unapproved dead-end volumes into an oxygen-containing system.
- **Proof before procurement:** bench-test 0, 0.05, 0.1 and 0.2 standard L/min reference leaks over relevant volumes and temperature swings, then run blinded comparisons with qualified engineer-led leak audits at several hospitals. Count correct section localization, missed leaks, false positives, test time, interruption incidents and verified cylinder-mass savings over at least one annual supply cycle. Proceed to installation only after site-specific engineering approval, applicable product qualification and clinical governance; compare against simply using point-of-care cylinders or established maintenance. A 10–20-year pathway is bench metrology, supervised multi-site trials, certification, then locally serviceable production—not a present deployment claim.
- **End of life:** replace calibrated sensors, standard battery and seals separately; return gas-compatible wetted parts through medical-equipment service channels and recycle the steel enclosure and electronics appropriately. No subscription or cloud connection is required.

## How It Works

1. **Reconcile the inventory.** An authorised engineer records incoming and returned cylinder masses, fill specifications, exchanges and the measurement window. The cart keeps gross gas turnover separate from estimated clinical draw; missing or uncertain logs make the result **unverified**, not a leak estimate. A high discrepancy is a reason to investigate, not proof of a particular pipe defect.
2. **Prepare a safe test boundary.** After clinical approval, backup-supply verification and independent isolation, the engineer identifies an out-of-service section from the current schematic. Only a site-approved test medium, pressure, keyed port and qualified oxygen-compatible assembly may be used. The cart never opens a valve or connects to a live patient circuit.
3. **Run controls, then measure.** Zero and span-check both pressure channels with traceable calibration, measure a sealed blank for test-head leakage and challenge the setup with a known reference leak. Record absolute pressure and surface temperature throughout the section and adjacent-reference traces; reject data if the blank, reference, temperature stability or approved boundary fails.
4. **Correct and review.** For a fixed-volume section, compare pressure normalised by absolute temperature, since ideal-gas behaviour gives gas amount proportional to `p_abs × V / T_abs`. Propagate sensor, temperature, volume and seal uncertainties before comparing the trace to the blank and reference. The display offers **unverified**, **investigate** or **eligible for engineer review**; none means safe for patient use. A qualified engineer independently confirms any repair candidate and controls return to service.

## Technical Architecture

`Cylinder scale + exchange log → inventory reconciliation → discrepancy with uncertainty` and `approved test port → 316L test head → dual pressure channels + temperature probes → timestamped, temperature-corrected trace → blank/reference checks → engineer-facing report` are separate paths joined only in the offline decision record. The battery-backed logger stores section IDs, instrument serials, calibration validity and test-medium identity, not patient identifiers; a signed paper or local export is retained under the site's engineering policy. Software interlocks make missing approvals, invalid calibration, sensor disagreement, out-of-range pressure, lost power or a failing control invalidate the result. They do **not** replace physical isolation, mechanical pressure protection or authorised medical-gas commissioning. Pressure transducers and seals need qualification for the actual service; a 0–10 bar sensor rating alone does not establish installation compatibility.

## Performance Benchmarks

**Current-state comparator:** a qualified engineer's ordinary cylinder-accounting and isolated-section leak investigation, including approved leak-testing equipment, is the baseline—not an uninstrumented hospital and not a claim of a new sensing principle.[1] There are no prototype measurements, no universal hospital loss rate and no validated advantage over this baseline. The following are **proposed acceptance targets**, tested with an engineer-blinded standard across site-relevant section volumes and temperatures:

| Measure | Proposed target (not observed) | Comparison and gate |
| --- | --- | --- |
| Reference leak resolution | Repeatedly distinguish 0.1 standard L/min from sealed blank in a 100 L section during 20 min | Challenge with 0, 0.05, 0.1, 0.2 standard L/min; report sensitivity, misses and false calls versus existing approved method |
| Test-head blank | Equivalent leakage below 0.01 standard L/min | Measure before and after each section trace; otherwise mark unverified |
| Section test duration | Under 45 min after authorised isolation, excluding shutdown and recommissioning | Time both workflows on the same section; report the full clinical interruption separately |
| Localization and reconciliation | No assumed improvement | Blind candidate section, count confirmed repairs and compare annual cylinder-mass reconciliation with engineer-only audits |

A sanity check at roughly standard temperature and pressure: 0.1 standard L/min for 20 min removes 2 standard L; in a 100 L fixed volume this corresponds to about 0.020 bar pressure change if temperature is steady. At 4 bar absolute and about 293 K, a 1 K thermal shift alone changes pressure by about 0.014 bar. These are ideal-gas *illustrations*, not field thresholds: actual section volume, test medium, pressure, temperature gradients, compressibility and uncertainty determine whether the target is achievable. No alarm threshold or clinical clearance can be inferred from them.

## Deployment Scenarios

- **Maternity wing with a piped 50:50 gas supply:** during an approved maintenance shutdown, compare bank reconciliation with staged, isolated-branch tests. Engineering and clinical leads review the findings and choose repair, branch retirement or no change. Occupational exposure still requires separate room-level controls and competent monitoring.[2]
- **Hospital considering portable cylinders:** document actual pre-use losses and maintenance burden before deciding whether a shorter distribution path is preferable. Oxford University Hospitals reported a site-specific move from a nitrous-oxide manifold to portable cylinders after an audit; it is a precedent for evaluating options, not evidence that this cart works.[4]
- **Regional maintenance service:** a shared cart could visit several facilities with separate keyed adapters and local calibration records. Transport, approved fittings and trained staff must be funded; if a site cannot safely isolate a section, use ordinary audit methods instead.

## Risks & Mitigations

| Risk | Required control / evidence before use |
| --- | --- |
| False reassurance from missed leak or mislogged consumption | Blank and known-leak challenges, uncertainty bound and independent engineer confirmation; **unverified** when evidence is incomplete; never certify patient safety |
| False repair call from temperature, regulator creep or bad seal | Temperature-normalised paired traces, stable boundary and blinded comparison with incumbent approved tests; log false-positive rate |
| Oxygen-service ignition, contamination or connector mismatch | Qualified clean wetted materials and keyed fittings, site-approved medium and pressure, mechanical protection and authorised isolation/commissioning; no improvised live connection |
| Power loss, drift, broken probe or corrupted export | Battery and calibration checks at each session, dual-channel disagreement test, offline signed report and fail-to-unverified behaviour; maintenance interval established by pilot evidence |
| Alarm fatigue, privacy or unequal access | Engineer-only non-urgent review state, no patient records or cloud dependency, accessible paper output, shared servicing and training; measure usability and total site cost |

## Vision for 2050

If field trials justify it, maternity estates could treat pre-use nitrous-oxide losses like an auditable utility: periodic reconciliation would show where gas disappears *before* treatment, and a trained engineer would verify repair or a simpler supply design. Standardised local reports could make climate accounting credible without extracting patient data or dictating analgesia choices. This is a possible infrastructure practice, not a forecast of adoption, avoided emissions or clinical benefit.

See [ROADMAP.md](ROADMAP.md) for validation gates and [IMPACT_ANALYSIS.md](IMPACT_ANALYSIS.md) for bounded scenarios.

## Sources and prior art

1. Association-led consensus on piped nitrous-oxide decommissioning and premixed-gas loss: https://eprints.lancs.ac.uk/id/eprint/223580/1/Consensus_on_decommissioning_piped_nitrous_oxide_from_UK_and_Ireland_operating_theatre_suites-_Accepted_Version.pdf
2. UK Health and Safety Executive, maternity nitrous-oxide exposure controls and monitoring: https://www.hse.gov.uk/healthservices/using-nitrous-oxide-safely.htm
3. Review of volatile anaesthetic capture versus nitrous-oxide handling: https://doi.org/10.1111/anae.16207
4. Oxford University Hospitals example of decommissioning a leaking piped nitrous-oxide supply in favour of portable cylinders (site-specific, not transferable performance evidence): https://www.ouh.nhs.uk/news/article.aspx?id=2097&pi=0
