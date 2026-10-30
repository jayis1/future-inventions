# Spectral-Guard Air Disinfector

**Author: jayis1** · **Status: research concept (TRL 2)** · **Category: Airborne Disease Prevention / Universal Basic Services**

## Problem

Crowded clinics and classrooms can share infectious aerosols even when windows cannot be kept open. WHO estimates 10.7 million people developed tuberculosis and 1.23 million died of it in 2024; TB spreads through the air.[1] Ventilation, respiratory protection, diagnosis and treatment remain essential. Germicidal UV is a possible *additional* air-cleaning layer, but a 222 nm lamp cannot be assumed safe merely because its nominal peak is 222 nm: unwanted longer-wavelength emission, ozone and installation geometry matter.[2]

## Solution

A ceiling-mounted, repairable room fixture combines a filtered krypton-chloride (KrCl) 222 nm excimer source with a mechanically retained dielectric bandpass filter, a baffled light aperture, and a separate replaceable ozone-destruction module. A low-cost 12 V DC supply can run from a clinic battery/solar system sized separately. Germicidal photons damage nucleic acids in passing airborne microbes; room air must mix into the illuminated volume. The design **never** claims to sterilize a room, diagnose disease or replace clean outdoor air.

A factory spectral scan qualifies the complete aperture at multiple angles, not just the lamp. A service-only interlock shuts the emitter off when the filter housing opens; a paired optical reference checks *relative* transmission drift during operation. An ozone sensor at breathing height and a measured ventilation minimum are prerequisites to any occupied-room trial. Faults, sensor expiry or power loss switch the emitter off; a visible label says that the room's baseline ventilation is still required.

## Key Innovation

Filtered far-UVC lamps and UV air cleaning already exist.[2] The research contribution is a **replaceable, factory-mapped optical-and-ozone module** whose measured spectral map, spatial irradiance map and ozone-generation test travel with its serialised module, coupled to an offline fail-closed daily exposure budget for the *worst accessible position* in a specified room layout. Installation cannot enable occupied-mode irradiation until the local assessor enters a measured geometry and ventilation result; opening the optic, replacing the source or exceeding a calibrated cumulative irradiance budget invalidates that assessment. This is a testable safety architecture, not a claim of worldwide patent novelty. It does not track or identify occupants.

## Target Cost

**Research target, not a quotation:** US$450 ex-factory per 50 m³-room fixture at 10,000 units/year in 2038 (lamp/driver US$170, optic/baffle US$100, controller/sensors US$90, housing/ozone module US$90); estimated US$150–300 installation and US$80–150/year for source, filter, calibration and ozone-module service. Excludes ventilation, solar/battery system, safety certification, taxes, training and site survey. Solid-state 222 nm emitters may replace the excimer source if efficiency, lifetime and spectral purity improve; this is a research dependency, not a prerequisite for the first prototype.

## Impact

Pilot target: in a **50 m³ test room** with specified mixing and ventilation, achieve **at least 5 equivalent air changes per hour of additional airborne test-aerosol inactivation**, measured against the same room with the emitter off, while demonstrating compliant *spectrally weighted* accessible exposure and no unsafe incremental ozone or secondary pollutants. These are unproven co-targets: if either safety test fails, occupied operation is prohibited. A deployment of 10,000 qualified fixtures could cover at most 10,000 suitable rooms; infection reduction and lives saved cannot be inferred without controlled studies. Preserve ventilation, respirators where indicated, and TB case-finding and treatment. See [SPECIFICATION.md](./SPECIFICATION.md) for acceptance and failure tests.

## How It Works

The lamp excites krypton-chloride gas and emits near 222 nm. A multilayer dielectric stack rejects longer-wavelength leakage; the aluminium baffle limits which directions are illuminated. Aerosol-laden air must circulate through that field: photons can inactivate a microbe in flight, but do not trap the particle or remove CO₂. Unlike a duct filter, this fixture has no claimed processed airflow; room mixing, humidity, aerosol residence time and shading determine effective dose. CDC describes the same dependence on circulation for upper-room germicidal UV, a different optical design.[5]

Before commissioning, a calibrated spectroradiometer maps the assembled aperture at accessible angles, including the worst eye/skin position. A local assessor records room geometry, baseline ventilation and the applicable *spectrally weighted* exposure limit with uncertainty margin. During operation, the paired optical reference watches for relative drift, while an independently checked service interlock and local ozone monitor form part of the shutdown path. These are **proposed safeguards**, not proof of safety: a cracked optic can escape a reference sensor, and a catalyst cannot be presumed to destroy all ozone. Opening the housing, losing calibration or exceeding the assessed daily budget makes the lamp dark pending reassessment. A periodic full-field map remains necessary.

## Technical Architecture

- **Optical module:** replaceable KrCl emitter, driver, dielectric filter, retained aluminium baffle and tamper-evident enclosure; factory serial number links its spectral, angular and ozone test record to the installed module.
- **Air-quality module:** breathing-height ozone sensing plus a *candidate* manganese-oxide catalyst. Catalyst conversion, breakdown products and containment must be tested under the site's lowest allowed ventilation and representative VOC mixtures; it is not a substitute for outdoor air.
- **Offline controls and power:** 12 V DC input, normally-open service cut-off, optical drift reference, calibration clock, worst-position dose accumulator and visible out-of-service state. No camera, cloud service or occupant log. A hardware-proven interlock and independent exposure/chemistry assessment are gates before occupied use.

Factory qualification → site geometry/ventilation measurement → authorized enable → optical/ozone monitoring and dose-budget accounting → derate or *dark-lamp* fault → service and independent remapping. A power outage cannot preserve germicidal action; restart must recheck validity rather than silently assuming prior protection.

## Performance Benchmarks

**Not product test results.** Compare room-scale viable-aerosol decay, not a lamp's nominal wavelength or particle count alone. In matched 50 m³ trials with ventilation/fans unchanged, fit `C(t) = C(0) exp(-kt)` after accounting for deposition and natural decay; incremental eACH = `k_on − k_off` (rates in h⁻¹). The clean-air equivalent is `V × eACH`: **5 h⁻¹ × 50 m³ = 250 m³/h** under a well-mixed approximation. This is a research target, not an AHAM-certified particulate CADR; the device does not remove particles. Compare spatial confidence intervals under low mixing and aging, not just a single central sampler.

| Metric and conditions | Published comparator / current alternative | This design's unverified target |
|---|---|---|
| Viable-aerosol inactivation, room scale | Eadie et al. (2022): five filtered 222 nm sources reduced steady-state aerosolized *S. aureus* by 98.4% at 3 ACH ventilation in a room-sized chamber; reported 184 additional eACH. Different lamps, organism and geometry prohibit direct product comparison.[3] | ≥5 *additional* eACH in a 50 m³ room with matched emitter-off trials, multi-position sampling and uncertainty bounds. |
| Particle cleanup | EPA's portable-cleaner guidance sizes particle CADR to room area; particulate CADR is a different endpoint from viable-aerosol inactivation.[4] | No particle-CADR claim; combine with filtration if particle removal is needed. |
| Power and service | No like-for-like measured baseline for this proposed fixture. | ≤60 W DC at 12 V while active; annual calibration *goal*, revised after aging and drift trials. |
| Accessible dose and chemistry | ASHRAE 241 requires air-cleaner performance/safety testing and equivalent-clean-airflow accounting; applicability must be assessed for the site.[6] | Independently demonstrate local spectral-exposure and air-quality compliance under worst approved conditions; no universal ozone threshold asserted. |

## Deployment Scenarios

1. **Clinic waiting room:** assess a 50 m³ room and its normal ventilation first; a trained installer maps accessible irradiation and an independent laboratory checks ozone/byproducts before any occupied trial. At the 60 W input ceiling, an eight-hour shift would consume at most **0.48 kWh** excluding baseline ventilation and external battery losses. If the guard trips, keep ventilation and respiratory-protection policy in force; this is not a clinical TB-prevention claim.
2. **Cold-climate classroom:** assess ceiling height, desks and any reflective surfaces, then run matched occupied-geometry aerosol-surrogate tests *before* occupied use. The 50 m³ reference-room result cannot be applied to a larger class by scaling fixture count alone; preserve required outdoor-air supply and filtration.[4][5]
3. **Community health outpost on solar/battery:** a separately sized 12 V supply can power one fixture, but only where trained service, calibrated spectral surveys and reliable ventilation measurements are available. Otherwise prioritize maintainable ventilation/filtration; an expired sensor means dark-lamp mode, not an unsafe override.

## Risks & Mitigations

| Failure mode | Mitigation and verification gate |
|---|---|
| Filter crack, aged spectral rejection, reflection or changed room layout exposes eyes/skin | Baffle and mechanically retained optic, normally-open service switch, worst-position weighted-dose budget; independent angular spectral maps after shock, cleaning, aging and source changes. Relative optical drift sensing alone is insufficient. |
| 222 nm photochemistry increases ozone, aldehydes or secondary particles | Test emitter-on/off at breathing height with low ventilation and VOC mixtures; qualify catalyst breakthrough and dust containment. A 2024 occupied-restroom study measured a mean **5 ppb** ozone increment at 1–2 h⁻¹ ventilation, a warning rather than this fixture's predicted output.[7] |
| Poor mixing or aerosol shielding defeats chamber efficacy | Multi-position viable-surrogate sampling, matched UV-off controls and low-mixing repeat; do not extrapolate surrogate decay to infection outcomes. |
| Sensor drift, power loss, unauthorized repair or false sense of protection | Expiry and fault shut the emitter off and display out-of-service; independently test interlock, controller restart and calibration failure. Never reduce baseline ventilation to offset claimed eACH. |
| Unclear legal pathway and service affordability | Seek jurisdiction-specific photobiological/electrical assessment, air-cleaner performance testing and review of antimicrobial-device claims before sale; budget trained inspection and licensed end-of-life handling. No certification is claimed. |

## Vision for 2050

If independent safety and field trials succeed, a shared-space fixture could carry a locally auditable spectral and chemistry record much as a building carries maintenance records today. Facility managers would budget verified equivalent clean airflow alongside ventilation and filtration, and replace suspect modules instead of trusting a power-on light. That world requires enforceable installation rules and affordable service—not a promise that UV ends airborne disease. Transmission outcomes would still need separate evidence.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/tuberculosis
[2] https://pubmed.ncbi.nlm.nih.gov/?term=far+UVC+222+nm+ozone+room
[3] https://www.nature.com/articles/s41598-022-08462-z
[4] https://www.epa.gov/indoor-air-quality-iaq/guide-air-cleaners-home
[5] https://www.cdc.gov/niosh/ventilation/germicidal-ultraviolet/index.html
[6] https://www.ashrae.org/about/news/2023/ashrae-publishes-standard-241-control-of-infectious-aerosols
[7] https://pubs.rsc.org/en/content/articlelanding/2024/em/d4em00144c
