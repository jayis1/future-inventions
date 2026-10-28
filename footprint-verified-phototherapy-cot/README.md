# Footprint-Verified Phototherapy Cot

**Author: jayis1**

**Category:** Newborn Health & Universal Basic Services / Supervised Jaundice Care

**Status:** Concept (TRL 2; not a cleared medical device)

## Problem

Severe neonatal jaundice can cause permanent neurological injury or death if not recognized and treated. In a Vietnamese low-resource hospital study, inadequate irradiance from aging or wrongly selected lamps was a recurring practical problem; the study compared existing LED units, including a fixed-distance double-sided cot.[5] A separate six-device study measured high-irradiance footprints ranging from 67 to 1,465 cm², with device irradiance readings ranging from 27 to 52 µW/cm²/nm.[4] A lamp that looks bright at its center may therefore leave much of the infant outside its effective footprint. Bilirubin testing, clinical assessment and available referral remain indispensable.

## Solution

A clinic-only, fixed-geometry cot combines an overhead 460–490 nm blue-green LED panel, removable washable transparent cradle, mechanical height stops, and a **nine-position reusable calibration tile** shaped like the mattress. At each shift and after cleaning or lamp replacement, a trained worker inserts the tile, checks its coded position, and scans all nine positions with a shared, wavelength-matched, traceably calibrated spectral-irradiance meter. A local display shows the measured minimum and map; a spring-return **NOT VERIFIED** placard can be held in its verified position only while the current check is valid, and releases on power loss, expiration or a detected fault. The meter is shared among cots, not replaced with an uncalibrated color sensor. A reusable wipeable record card records the test time, cot ID, location values and meter calibration due date without patient identity.

A separate hardwired light driver, fused low-voltage supply and replaceable battery buffer provide illumination when qualified. Power loss or failed map does **not** automatically interrupt clinician-selected treatment: a conspicuous local alarm demands an approved alternative device or transfer, with no false assertion of delivered dose. During treatment, caregivers still assess temperature, feeding, hydration, skin exposure and serum bilirubin according to local protocols. The proposed tile measures the *empty-cot reference plane*, not photons at every curved patch of infant skin; it cannot verify individual exposure or replace serial bilirubin tests.

## Key Innovation

Existing fixed-distance double-sided LED cots and overhead lamps already provide phototherapy; an accessible study also describes a field method for measuring the irradiance footprint.[5][4] The proposal is a **serviceable, keyed cot-to-meter acceptance workflow**: fixed geometry, nine-position mapping, explicit minimum-footprint qualification, independently traceable meter calibration and a persistent fail-visible state. It tests whether preventing unmeasured geometry, lamp aging and skipped checks improves actual treatment reliability over maintained conventional LED phototherapy. The innovation is a falsifiable operational integration, not new photochemistry or a claim that phototherapy meters do not exist. Whether the nine-point empty-cot map predicts infant-level dose well enough is unproven.

## Target Cost

**Unvalidated 2038 engineering target at 10,000 cots/year:** US$180 ex-factory per cot: US$65 LED panel and heat spreader, US$35 low-voltage driver and wiring, US$35 cot frame and cradle, US$20 battery buffer and alarm, US$10 keyed tile and placard, US$15 assembly and acceptance testing. Budget a further US$300–600 for a shared traceably calibrated spectral meter and annual recalibration; these are planning allowances, not supplier quotes. At 20 cots per meter, a US$400 meter contributes US$20/cot before recalibration. Installation, staff, bilirubin assays, eye protection, power, battery replacement, cleaning supplies, regulatory testing and referral are excluded. Design for repairable LED/driver modules and a five-year service life target; collect batteries/electronics separately and recycle the polycarbonate cradle where facilities exist. No cost-effectiveness claim follows from the BOM.

## Impact

A planning scenario of 10,000 cots operated for 200 qualified treatment sessions each year offers **at most 2 million supervised sessions/year**, not 2 million distinct newborns helped or a projected mortality reduction. Compare paired sites against correctly maintained conventional LED devices: fraction of treatments begun with a valid footprint map, map failures, treatment interruptions, time to alternative care, bilirubin response and adverse temperature or eye events. The device is worthwhile only if the incremental workflow reduces underexposure *without* delaying necessary therapy or causing unnecessary transfers. A 10–20-year development pathway is bench geometry and aging validation, human-factors trials, independent electrical/optical safety review, then prospective clinical comparison and jurisdiction-specific authorization.

## Technical and safety gates

- **Optical acceptance hypothesis:** for a cot limited initially to a clinically defined term/near-term infant size, test ≥30 µW/cm²/nm at each of nine predefined mattress-plane points in the 460–490 nm waveband, using a meter calibrated for that spectrum. This is a proposed *intensive-mode engineering gate*, not measured performance, a universal prescription or proof of skin dose. Map multiple body sizes, angles, transparent-mattress aging and partial shadowing before selecting the actual treatment footprint. The published ≥30 µW/cm²/nm footprint definition and wide measured footprint variation motivate this gate.[4]
- **Thermal/electrical controls:** LED-to-infant distance is fixed by a non-adjustable stop; a diffuser and guarded panel deny direct LED contact. Independent thermistor and thermal fuse limit panel heating; an isolated current-limited supply, fuse, strain relief and cleanable sealed enclosure require formal electrical and biocompatibility tests. Axillary temperature is checked by staff, not inferred from a lamp sensor. Eye shielding and feeding breaks follow clinical protocol.
- **Fail-visible behavior:** a missing tile, wrong tile orientation, out-of-calibration meter, partial scan, scratched cradle, low battery, panel fault or warm panel keeps **NOT VERIFIED** visible. A site must maintain a qualified backup/referral pathway; do not promise continuous treatment under an outage. Never suppress alarms remotely or retain patient identifiers.
- **Validation:** map spectral irradiance against an independent calibrated reference on a grid denser than nine points, at full and low battery, after cleaning and thermal cycling, and through LED aging. Prespecify false-pass limits and an acceptance criterion for minimum covered area, not just a bright center. Compare results with a maintained standard phototherapy cot under ethical clinical oversight. If the map does not predict safe clinical use better than routine meter checks, abandon the extra mechanism.

## How It Works

This is a proposed **pre-session equipment qualification**, not a live measurement of the infant's absorbed dose. Before a shift, a worker cleans and inspects the clear polycarbonate cradle, seats the keyed tile at the defined mattress plane, checks the meter's calibration date and spectrum setting, then measures nine labeled locations through the assembled optical path. The controller records each spectral irradiance reading (µW/cm²/nm), the lowest reading, cot identity, meter identity and check time. It rejects an incomplete, misoriented or expired scan; the spring-return placard remains **NOT VERIFIED**. The worker repeats the map after a cradle or LED change, impact, suspect reading or cleaning that alters the optical surface.

Only after a valid check does a clinician decide whether this infant needs phototherapy, place the infant with appropriate eye protection, and expose skin according to clinical protocol. The cot supplies fixed-distance light while staff check position, obstructions, temperature, feeding and bilirubin trajectory. A blanket, diaper, moved infant or soiled cradle can defeat the mapped footprint even when the empty-cot check passed. Therefore the display says **equipment map valid**, never **infant dose verified**. On mains failure the buffer may sustain light temporarily, but the verification state releases and an audible/visible alarm prompts an immediate clinical decision about backup treatment or referral; it must not silently stop treatment or falsely certify it. Requalification after restoration is mandatory.

## Technical Architecture

- **Optical and mechanical path:** narrow-band blue-green LED modules, aluminum heat spreader, diffuser and fixed mechanical height stop illuminate a defined cot plane through a removable transparent cradle. Spectral leakage, glare, degradation and cradle transmission must be characterized rather than assumed absent.
- **Measurement path:** keyed nine-location tile + shared calibrated spectral-irradiance meter measure the empty-cot plane. A denser independent reference grid in validation tests whether nine points miss dark regions between them. No camera classifies skin color or infers a body surface area from appearance.
- **Control and safety path:** local controller checks scan completeness, meter validity, temperature/reference state and elapsed time; separate fused low-voltage LED driver and thermal cutoff avoid making the display the sole light-safety control. A fail-visible placard, local alarm and paper record carry status to the caregiver without transmitting patient data.
- **Power and service:** mains supply, replaceable battery buffer, current monitoring, field-replaceable driver/LED modules and cleanable seals. Battery endurance and alarm behavior require bench testing under degraded battery and interrupted-power conditions.

Data flow: calibrated meter → nine measurements + tile/cot ID → local acceptance logic → placard/alarm + dated record → clinician review. Bilirubin assays and treatment decisions remain outside this control loop.

## Performance Benchmarks

**No prototype has been tested.** The numbers below distinguish published observations, a clinical guideline, and proposed engineering gates; comparing a measured center value with nine proposed minimum-plane values is not a like-for-like efficacy comparison.

| Metric and conditions | Current reference | Proposed cot target (unmeasured) |
| --- | --- | --- |
| Spectral irradiance | The six-device study reports device readings of 27–52 µW/cm²/nm and high-irradiance footprints of 67–1,465 cm² under its own test conditions.[4] The [AAP 2022 guideline](https://publications.aap.org/pediatrics/article/150/3/e2022058859/188726/Clinical-Practice-Guideline-Revision-Management-of) describes intensive narrow-spectrum LED phototherapy at ≥30 µW/cm²/nm near 475 nm; its recommended irradiance is measured below the light center. | ≥30 µW/cm²/nm at **each** of nine predefined empty-cot plane points through the cradle, in the 460–490 nm band; confirm spatial minimum and meter uncertainty on a dense independent grid. This deliberately stricter spatial gate is not an AAP requirement. |
| Coverage and uniformity | Published footprint areas vary widely even among phototherapy units.[4] | Declare the qualified rectangle only after body-size/position and occlusion studies; no validated body-surface coverage percentage or uniformity ratio yet. Record minimum/maximum point ratio as a diagnostic, not a pass claim. |
| Verification reliability | A single center measurement does not map the peripheral field.[4] | Target zero accepted scans with a missing point, invalid meter or expired check in fault-injection tests; prespecify and measure false-pass probability before pilot. |
| Service and cost | Existing LED cots and handheld meters are established prior art.[5][4] | Five-year service-life and US$180 ex-factory cot targets at 10,000/year; US$300–600 shared meter allowance, excluding clinical operations. No supplier bids or lifetime results yet. |

Bench reports must publish meter calibration/uncertainty, geometry, spectrum, ambient-light correction, thermal steady state, battery state, cradle aging and failures. Passing an optical gate cannot establish a bilirubin response.

## Deployment Scenarios

1. **District newborn unit:** a shift nurse maps each cot with the shared meter before use; a failed map sends the clinician to an approved backup cot, not to a lower exposure threshold. The site needs bilirubin testing, eye shields, trained staff and a meter recalibration route.
2. **Postnatal rooming-in ward:** a nurse qualifies the fixed-geometry cot and keeps the mother near the infant during supervised care. Feeding breaks and repositioning are documented; the equipment map is not treated as an uninterrupted exposure log.
3. **Rural referral hospital with unstable mains:** a technician tests alarm and battery buffer at shift start. A failing buffer or overdue meter check triggers a named backup/referral pathway; installation without that pathway is not deployment-ready. This is not an unsupervised home-treatment proposal.

## Risks & Mitigations

- **False pass or missed dark patch:** nine points can miss shadows, scratches, LED aging or cradle fouling. Validate against dense scans across infant sizes and orientations, require a calibration schedule and block stale or incomplete checks; abandon the tile if false passes remain unacceptable.
- **False reassurance about an individual infant:** the map excludes body curvature, skin occlusion, eye shield and movement. Staff inspect exposure and follow serial bilirubin measurements and escalation protocols; no displayed equipment status substitutes for a clinical response.
- **Heat, dehydration and eye exposure:** independent panel thermal protection, guarded LEDs, staff temperature/hydration checks and appropriately fitted eye protection need risk testing. A panel thermistor is not an infant thermometer.
- **Outage and alarm fatigue:** visible verification releases on lost power; a buffer supports only measured runtime. Test audible alarms in ward noise, train staff on backups, and do not make a failed measurement automatically terminate clinician-selected illumination.
- **Infection, electrical and access risks:** validate cleaning compatibility and transmission after repeated disinfection, electrical isolation and battery containment. Budget recurring meter calibration, parts and training; require applicable medical-device safety review (including IEC 60601-1 and IEC 60601-2-50) and jurisdiction-specific authorization before patient use. Neither compliance nor clinical benefit has been demonstrated.

## Vision for 2050

If the optical map proves clinically useful and maintainable, a cot's qualified footprint could become a routine check like a calibrated scale: visible to the next shift, reproducible after repairs and auditable without collecting infant identity. A ward would still use bilirubin testing, clinicians and reliable referral; the aspiration is fewer preventable gaps between a lamp being switched on and effective supervised therapy, not a machine that certifies cure. Wider use depends on evidence that the extra workflow improves care relative to a well-maintained conventional LED unit.

## Sources

[4] https://www.nature.com/articles/s41390-021-01795-x
[5] https://pmc.ncbi.nlm.nih.gov/articles/PMC6181361
