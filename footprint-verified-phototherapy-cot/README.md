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

## Sources

[4] https://www.nature.com/articles/s41390-021-01795-x
[5] https://pmc.ncbi.nlm.nih.gov/articles/PMC6181361
