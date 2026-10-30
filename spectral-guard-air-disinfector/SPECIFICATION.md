# Spectral-Guard Air Disinfector — Research Specification

**Author: jayis1** · **Concept only; not approved for occupied-room use**

## Mechanism and boundary

A filtered KrCl excimer emitter produces approximately 222 nm UV-C. A multilayer dielectric filter suppresses longer-wavelength leakage; an aluminium baffle limits accessible angles. The replaceable optical assembly is sealed with tamper-evident fasteners and a normally-open cut-off switch. A separate manganese-oxide-based ozone catalyst is a *candidate* component requiring measured conversion and byproduct validation, not a presumed universal ozone solution. The lamp housing, driver and catalyst can be repaired without replacing the whole fixture; spent lamps and electronics go to licensed e-waste handling.

Filtered 222 nm systems and room ozone/secondary-chemistry studies exist; this proposal's distinction is the co-qualified module and deployment safety gate, not new photochemistry.[2]

## Provisional engineering targets

| Boundary | Research target / condition |
|---|---|
| Test room | 50 m³; occupied geometry and air mixing documented; compare matched emitter-off trials |
| Power | ≤60 W DC input at 12 V; prototype battery run time depends on separately sized storage |
| Air disinfection | ≥5 equivalent air changes/hour *additional* inactivation of a safe test aerosol; multi-position sampling with fan/ventilation unchanged |
| Spectral and exposure | Independently calibrated spectroradiometer scan at all accessible angles; worst-position, time-integrated, wavelength-weighted dose below the applicable jurisdiction's occupational/public limit with a conservative uncertainty margin |
| Chemistry | Ozone and selected oxidation byproducts measured at breathing height, emitter on/off, under the lowest approved ventilation and representative indoor VOC mixtures; no occupied operation unless local air-quality criteria are met |
| Service | Factory and post-install spectral map; optical-reference drift alarm validated against damaged, aged and incorrectly seated filters; annual recalibration target, shortened when testing requires |

No numerical exposure or ozone threshold is asserted as universally safe: standards vary by jurisdiction, wavelength, exposure duration, co-pollutants and population. Independent photobiological, electrical and air-quality assessment sets site-specific limits before human exposure.

## Validation gates

1. On the bench, map aperture spectrum and irradiance with traceable instruments after simulated shipping shocks, filter cracks, aging, cleaning and source swaps. Optical-reference monitoring alone cannot prove a crack-free field: periodically repeat the full-field scan.
2. Challenge with a non-pathogenic aerosol surrogate in a controlled 50 m³ chamber at multiple locations; estimate first-order decay with and without UV under identical ventilation, account for deposition and naturally occurring decay, and report confidence intervals and power draw. Repeat under low mixing; do not advertise a single-point result as whole-room efficacy.
3. Measure ozone and secondary species under low ventilation with representative indoor VOCs; test catalytic-media breakthrough and catalyst dust containment. A failed test cancels occupied mode; do not compensate by concealing ozone or reducing ventilation.
4. Prove that power failure, failed or expired calibration, loose filter, opened housing, faulty ozone sensor, incorrect room geometry and missing maintenance produce a *dark* lamp and visible out-of-service signal. Verify that any power-off UV-inactivation loss is not misrepresented as continued protection.
5. Only after third-party spectral exposure, air-quality and electrical certification and approval under local rules: assess human acceptability and airborne surrogate performance in eligible rooms. Infection outcome claims require separate controlled epidemiological studies.

## Limits and accessibility

No microphone, camera, person tracking, cloud service or occupancy log is needed. A trained local installer and periodic calibrated spectroradiometer access are unavoidable costs; poorly resourced sites should prefer effective ventilation/filtration over an unmaintainable lamp. UV does not remove CO₂, humidity or chemical pollutants. Some pathogens, aerosols, room geometries and poorly mixed spaces may respond differently. A dark fault must never imply that air is safe.

## Sources

[2] https://pubmed.ncbi.nlm.nih.gov/?term=far+UVC+222+nm+ozone+room
