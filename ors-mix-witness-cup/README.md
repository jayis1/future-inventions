# ORS Mix-Witness Cup

**Author: jayis1**

**Category:** Child Health & Universal Basic Services / Oral Rehydration Preparation

**Status:** Concept (TRL 2; unvalidated; not a clinical clearance device)

## Problem

WHO reports nearly 1.7 billion childhood diarrhoeal episodes annually and about 443,832 deaths among children under five. Oral rehydration solution (ORS) made with clean water is an essential treatment, alongside appropriate feeding, zinc and clinical referral when indicated.[1] A sachet labeled for one litre must not be mixed with an arbitrary water volume: dilution changes both glucose and electrolyte concentrations. A visual fill line alone cannot establish that the right packet was used, fully dissolved, or mixed with safe water. A verifier must not delay rehydration or give false assurance that water is potable.

## Solution

A washable, opaque, one-litre mixing vessel has a broad, high-contrast fill mark and tactile fill stop for people with low vision. A detachable, offline test cup takes a **small sample** after the caregiver mixes a *recognized, unflavoured, one-litre reduced-osmolarity ORS packet* into previously purified or boiled-and-cooled water according to its label.[2] A two-channel reader compares temperature-corrected electrical conductivity (ionic content) and an optical refractive-index proxy (total dissolved solutes) with locally validated ranges for that exact packet formulation and the source water. It displays only **CHECK AGAIN** or **CONSISTENT WITH THE REFERENCE MIX** in text, shape and sound; it never displays “safe to drink.” The measured sample is discarded, not returned to the vessel. A permanently marked packet-type selector and a sealed reference check prevent an unknown formulation from receiving a pass.

This is a preparation-error screen for supervised community settings, not a replacement for the packet instructions, clean water, a clinician, or an ORS supply. If the reader is unavailable, expired, dirty, gives an invalid result, or cannot identify the packet, caregivers follow standard labeled ORS preparation and seek appropriate care **without waiting for the device**. Severe dehydration, inability to drink, persistent diarrhoea or blood in stool requires urgent professional assessment under local guidance.[1]

## Key Innovation

The proposed research contribution is **formulation-specific, two-observable mixing verification with explicit abstention**, coupled to a measured-volume vessel: a conductivity measurement responds mainly to dissolved ions while refractive index responds to the combined solute load. Together they may catch gross volume, omitted-sachet and incomplete-mixing errors that a fill line misses. Neither observable uniquely identifies sodium, potassium or glucose; similar mixtures can produce the same pair of readings. Conductivity meters, refractometers and mixing cups already exist. No claim of new sensing physics or clinical accuracy is made.

Prototype: food-contact polypropylene vessel; replaceable silicone seal and stainless fill-stop pin; reusable gold-plated interdigitated electrodes behind an inert guard; molded cyclic-olefin optical window, LED and photodiode to estimate a critical-angle shift; thermistor; low-power microcontroller; two replaceable AAA cells. The test cup's 2 mL sample channel is removable for washing, and a physical reference insert checks the optical path and electrode response at each session. The reader cannot authenticate a packet or verify microbial or chemical water safety. Any fouling, unusual source-water mineral content, flavoring, packet variation, temperature out of range, or failed reference forces an **invalid/uncertain** result rather than a pass.

## Target Cost

**Unvalidated 2038 design target, not a quote:** US$24 ex-factory at 100,000 units/year: US$5 molded vessel and seal, US$4 sampling cup and electrodes, US$6 optical/electronic parts, US$3 enclosure/cells, US$6 assembly, calibration and scrap. Target a five-year reusable life and a US$3 replaceable cup/window assembly; batteries, clean water, ORS, staff time, distribution, validation and regulatory approval are excluded. A fully passive graduated vessel remains usable if electronics fail. Repairable screws, removable cells and separately recyclable polymer/electronic modules avoid treating the entire vessel as a disposable sensor. Price and durability must be measured, not assumed.

## Impact

A planning scenario of 10,000 readers used for 200 preparations per year would yield **up to 2 million screening attempts/year**, not 2 million children treated or any demonstrated deaths prevented. Run blinded bench challenges across packet brands, water mineralization, temperature, incomplete dissolution, half/double concentration and plausible counterfeit mixtures; measure false passes and false rejects against laboratory electrolyte/glucose/osmolality assays. A supervised field study must compare preparation errors, delay to first ORS dose, ability to understand the ambiguous result, and actual referrals against a labeled one-litre container alone. Any increase in treatment delay, false reassurance or unacceptably high false-pass rate defeats the concept. The device should never make ORS access contingent on owning it.

## Operating boundaries and development

UNICEF lists a reduced-osmolarity one-litre sachet containing 13.5 g glucose, 2.6 g sodium chloride, 2.9 g trisodium citrate dihydrate and 1.5 g potassium chloride, to be diluted in 1,000 mL purified or boiled-and-cooled water; the specified solution contains 75 mmol/L sodium and 75 mmol/L glucose with 245 mOsm/L osmolarity.[2] Those values describe **one product**, not a universal formulation or the accuracy of this concept. Calibration bands must be derived from manufactured lots and independently measured samples, not hard-coded from a nominal formula. A predeployment gate should demonstrate detection of at least 90% of deliberately prepared half- and double-strength mixes at a predefined maximum false-pass rate of 1% on the challenge set; these are hypotheses, not achieved performance. Real-world clinical benefit requires separate ethical review and trials. A 10–20-year development path is plausible only if the device improves on simply supplying a correctly marked mixing container and clear instructions.

## How It Works

1. A trained preparer checks the actual packet label, selects the matching validated formulation, and fills the one-litre vessel to its tactile/high-contrast stop with water suitable for ORS under local guidance. The vessel checks *volume*, not water quality or packet identity. An unmatched packet is outside the reader's scope.
2. Add the **entire** packet as labeled, mix until no visible solids remain, then withdraw a roughly 2 mL sample. A partial packet, nonstandard homemade recipe, flavored product or unrecognized sachet must not be certified by this reader. Stir and resample if dissolution is uncertain.
3. The thermistor records sample temperature. The electrodes measure ionic conductivity; the LED/photodiode optical path estimates a refractive-index response to total dissolved material. Firmware compares both signals with experimentally established bands for that packet and source-water range, after session reference checks. A sample taken from only one location cannot prove the entire vessel was mixed uniformly.
4. The interface reports either **CONSISTENT WITH THE REFERENCE MIX** or **CHECK AGAIN**; out-of-range temperature, dirty optics, failed checks and overlapping/ambiguous readings must produce the latter or an explicit invalid indication, never an affirmative result. Under-strength and over-strength mixtures are *both* reasons to check again; the instrument must not instruct users to adjust an unknown mixture by eye. Remake it according to the packet label if volume or contents cannot be confidently established. Discard the sample and wash the detachable channel after use.

## Technical Architecture

| Subsystem | Proposed implementation | Signal or failure boundary |
| --- | --- | --- |
| Volume and contact path | Molded food-contact polypropylene one-litre vessel, tactile stop, removable 2 mL test channel and cleanable cyclic-olefin window | Known fill geometry and isolated sample; scratches, residue and leaks invalidate the read |
| Ionic channel | Guarded gold-plated electrodes driven with alternating excitation to limit polarization | Conductivity depends on ionic species, temperature and background mineral content; glucose contributes little directly |
| Solute channel | LED/photodiode critical-angle optics plus thermistor | Refractive-index proxy depends on *all* solutes and temperature, not glucose alone; turbidity/bubbles may corrupt it |
| Decision and feedback | Low-power MCU, packet-selector interlock, non-color-only text/shape/audio status, replaceable AAA cells | Reference check → sample → temperature compensation → two-channel bands → pass/abstain; no network or patient record |

The reference insert is a session self-check, **not** a substitute for wet calibration against traceable laboratory measurements. Prototype work must define electrode geometry, optical window aging limits, lot-specific bands, cleaning procedure and expiry/recalibration intervals. No sensor material should leach into a drinkable batch: the measured aliquot is discarded, and food-contact and cleaning compatibility require testing.

## Performance Benchmarks

The current practical comparator is a sachet prepared with the labeled water volume in a marked container, plus instructions—not an unverified sensor. WHO describes ORS made with clean water as treatment for diarrhoeal dehydration; the referenced UNICEF one-litre sachet specifies 1,000 mL water and a nominal 245 mOsm/L product.[1][2] These are **published preparation/product specifications**, not measured accuracy of this cup.

| Metric, under supervised test conditions | Marked vessel + packet instructions (baseline) | Cup **design target**, not demonstrated |
| --- | --- | --- |
| Volume witness | Marked 1 L fill, user reads line; no solute test | Tactile and visual stop; measure fill deviation across operators and lighting; target within ±20 mL at 20 °C |
| Gross half-/double-strength challenge detection | Cannot directly measure finished liquid | ≥90% detected over specified source-water/temperature matrix, with false-pass ≤1% on predefined challenge set; report confidence intervals |
| Specificity for sugar/salt substitutions | Cannot assay mixture | No guaranteed discrimination: both observables are non-unique; quantify misses in blinded challenge panel |
| Read time and availability | No electronic delay or batteries | Target ≤15 s after sample loading; report invalid rate, battery life and any treatment delay |
| Factory price | Container price varies; no defensible single benchmark | US$24/reader at 100,000 units/year in 2038, excluding operation and validation (existing unverified target) |

Test at proposed 10–40 °C, at least three characterized water-mineralization levels and multiple packet lots, comparing each aliquot with laboratory sodium, glucose and osmolality assays. The 20 mL and 15 s figures are proposed engineering gates, **not observed performance**. A 1% false-pass estimate requires a sufficiently large, prespecified challenge sample and uncertainty bounds; simply passing a few demonstrations is insufficient. If the added reader performs no better than the marked vessel on meaningful preparation errors or delays ORS, do not deploy it.

## Deployment Scenarios

- **Community health-worker station:** A worker preparing the *supported* sachet in a shared clinic uses the marked vessel first, then samples a finished batch before distribution. Training covers clean water, label matching, reference checks, sanitation, and immediate fallback to normal labeled preparation when the reader is unavailable; treatment must not wait for a sensor.
- **Supervised outbreak-response mixing table:** Trained volunteers label vessels and source-water batches, log invalid readings separately, and remake a batch whose contents cannot be verified. Bulk formulations or container sizes other than the validated one-litre packet require their own protocol; a 2 mL aliquot is not a microbiological test or a substitute for clinical triage.
- **Pharmacy demonstration:** Staff teach packet-specific mixing with a cup and show the non-color-only status as an *educational cross-check*. Home use is not implied until untrained caregivers can reliably interpret invalid results without delaying care; the ordinary marked container and label remain the fallback.

## Risks & Mitigations

- **False reassurance:** Two measurements cannot establish ingredient identity, sterility, chemical potability or clinical suitability. Incompatible packets, unusually mineralized/turbid water, counterfeits and a glucose-for-salt substitution may evade a proxy. Limit approvals to validated packet/water combinations; challenge plausible substitutions, print the limitation on the vessel, and never label a result “safe.”
- **Drift and contamination:** Temperature, bubbles, residual ORS, scratched windows, electrode fouling, UV aging, hot water and cleaning agents can move either reading. Restrict operation to a validated temperature range, require a session self-check and scheduled wet calibration, discard ambiguous samples, and replace failed parts. Test migration and food-contact compatibility on the assembled device, not just raw polymers.
- **Human factors:** A low-vision user, a child, poor light, an incomplete sachet or a mistaken selector can produce a misleading workflow. Use tactile markings and distinct shapes/audio; lock unknown packets out; test comprehension with intended users and require an invalid/fail response to trigger label-based remake or staff help—not improvised dilution.
- **Access and oversight:** Batteries, cleaning and a US$24 factory target may be too costly relative to a simple marked container. Evaluate cost per usable check, false passes, delayed dosing and waste in a controlled pilot; define the intended claim and obtain jurisdiction-specific regulatory and ethics review before any clinical marketing.

## Vision for 2050

If independent trials show net benefit over the marked-container baseline, a durable, locally calibrated witness could become one optional checkpoint at community preparation sites. The point is not to make families depend on electronics: it is to make uncertain mixtures visible while safe water, affordable ORS, readable packet instructions and timely care remain primary. A failed trial should instead lead to better vessel markings and training, not a compulsory sensor.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/diarrhoeal-disease
[2] https://supply.unicef.org/s1561133.html
