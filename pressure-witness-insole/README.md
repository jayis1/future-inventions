# Pressure-Witness Insole

**Author: jayis1**
**Category:** Foot Health & Universal Basic Services / Diabetic Foot Risk
**Status:** Concept (TRL 2; not a medical device cleared for use)

## Problem

People with diabetes and loss of protective foot sensation can repeatedly load a small region without feeling discomfort. Recurrent plantar ulcers can lead to infection and amputation. The IWGDF recommends properly fitted therapeutic footwear, and for people with healed plantar ulcers recommends footwear with a *demonstrated* pressure-relieving effect; a validated in-shoe measurement system is needed to establish that effect.[1] Yet a person wearing footwear between clinic visits has no inexpensive, battery-free way to notice a newly concentrated load. An indicator cannot diagnose tissue injury or replace foot examinations.

## Solution

A removable, thin witness layer sits **below**, not against the skin above, a clinician-selected cushioning insole. Four to six encapsulated snap-through polymer domes at clinician-selected heel and forefoot regions change a large high-contrast mark from clear to amber when a local loading event crosses a calibrated *engineering* threshold. The wearer removes the shoe at the daily foot check, reads the marks and a separate intact-seal reference, and brings a tripped insert to a trained footwear worker for fit/offloading review. The worker records the pattern, checks the foot, verifies the insert's thickness and smoothness, and resets or replaces the witness. There is no radio, battery, app, location tracking, or automatic alteration of footwear.

The layer is an adjunct to prescribed footwear and ordinary daily skin checks, not a substitute for a validated pressure map. If the witness is damaged, detached, already tripped at installation, or obscured, it reads **invalid**; the user continues prescribed footwear and seeks ordinary fitting/clinical review rather than treating an untripped mark as proof of safety.

## Key Innovation

A reusable mechanical overload *witness*, not a continuous pressure meter: each silicone or thermoplastic-polyurethane dome has a tuned snap-through instability, a captive contrasting flag, and a manual reset accessible only after removing the insert. A compliant load spreader and recessed dome housing aim to keep the sensor itself from creating a new hard pressure point; a transparent, sealed PET/TPU window prevents loose parts against the foot. Each witness is paired with a permanently visible seal/registration mark so a missing or shifted sensing element cannot masquerade as a safe result.

Pressure-sensitive film already permanently maps contact pressure and has been used for plantar assessment; instrumented insoles measure dynamic pressure. Neither mechanism is claimed as new.[2] The proposed advance to test is a **resettable, power-free, distributed visible excursion record with an invalid-condition gate** that can be read during routine footwear checks without an instrument. Unlike electronic monitoring it does not log timing or cumulative dose. The relationship between a dome trip and ulcer risk is unknown: the often-cited 200 kPa clinical footwear target applies to specific calibrated measurement conditions, *not* a universal trip point transferable to this device.[1]

## Target Cost

**Design targets, not supplier quotations:** at 100,000 inserts/year in 2038, US$12 ex-factory per pair: approximately US$3 molded elastomer domes/flags, US$2 PET/TPU barrier and window, US$2 compliant load spreaders, US$2 assembly/calibration, US$3 packaging, scrap and quality allowance. Excludes clinical fitting, footwear, distribution, training, regulatory testing and labor for follow-up; target service life one year with quarterly inspection and replacement on wear. No powered consumables. Modular mechanically retained witness pieces and the outer polymer layers should be separable for recycling where collection exists; contaminated inserts follow local medical-waste rules.

## Impact

Planning scenario: 100,000 pairs/year could provide at most 100,000 wearer-years of *indicator coverage*, assuming each pair is worn and replaced on schedule. That is reach, **not** ulcers or amputations prevented. A paired study should compare daily witness use plus standard therapeutic footwear with standard footwear alone, measuring false-negative trips against validated in-shoe pressure mapping, new pressure hotspots created by the insert, wear adherence, and clinically confirmed ulcer incidence. A bench gate before any patient trial: across shoe sizes, humidity, temperature, and repeated gait loads, the witness must maintain a worker-calibrated trip band and no greater local peak pressure than the same prescribed insole without the witness. If that gate fails, do not deploy. Human trials require ethical approval, clinician oversight, and medical-device regulatory review.

## Limits and development path

A short peak, static load, skin shear, neuropathy severity, moisture, and unnoticed non-wear all confound the indicator. Domes may creep or jam; enclosure tears and gritty debris may injure insensate feet. The first 2–3-year work is mechanical-fatigue and gait-lab comparison against calibrated sensors, then supervised usability testing; a 10–20-year horizon allows clinical evaluation and low-cost manufacturing if benefits exceed harms. Do not advertise a negative witness as safe pressure, use this for an active ulcer, or self-modify prescribed offloading. Whether a cheap snap mechanism can be both sensitive and harmless to the plantar surface is the pivotal unproven assumption.

## How It Works

The witness is a **mechanical memory of a local excursion**, not a pressure sensor reporting kilopascals continuously. During a fitting visit, a trained worker first confirms that the prescribed cushioning insole and shoe still fit, uses a validated in-shoe pressure system to identify the high-load regions, and selects four to six dome locations. The insert is secured *under* that insole. A footfall bends the compliant spreader and loads a recessed dome; above its factory-tested, worker-selected force band, the dome snaps and drives a captive amber flag into the viewing window. The flag remains visible after unloading, until the worker removes and manually resets the insert. A local dome senses force through a finite contact area: its trip cannot be equated to the skin's peak pressure without paired in-shoe testing across footwear and gait.

At shoe-off, the wearer checks the skin as usual and then looks for the high-contrast marks and intact seal/registration references. Clear and intact means **no recorded trip at the selected sites**, not that the foot is safe. Amber means arrange a footwear/clinical review; visible damage, shifted registration, unreadable marks or a pre-tripped insert means invalid and replacement or inspection. A new wound, redness, warmth or other concerning change warrants ordinary clinical assessment regardless of the flags. Only a trained worker records the site and checks fit and skin before any reset; a reset is not a treatment.

## Technical Architecture

- **Load path:** foot → prescribed cushioning insole → compliant spreader → recessed dome housing → shoe. Prototype cushioning and enclosure must be measured as an assembly; an insert that raises local peak pressure versus the prescribed insole alone fails the safety gate.
- **Witness cell:** molded silicone or TPU bistable dome, mechanically captive flag, sealed PET/TPU viewing window and an independent reference mark. Factory lot testing maps dome trip *force* in newtons over repeated loading; shoe-specific contact geometry determines the pressure relationship. Hysteresis keeps the trip legible after unloading but complicates reset and drift control.
- **Human readout and control:** four to six site labels, a clear/amber/invalid legend and a manual worker-only reset. No sampling clock, processor, wireless link or battery exists; recording and follow-up are human workflows, not automatic alerts. A failed, missing or unreadable cell invalidates the insert, not merely its one location.
- **Fit and manufacture:** size-matched die-cut layer, secured edges and recessed cells under the existing prescribed insole; no parts contact skin. Seal inspection, thickness checks and periodic replacement are mandatory. Adhesion, sweat ingress, creep, bending and temperature must be challenged before the one-year life target is credible.

## Performance Benchmarks

These are **engineering gates, not measured outcomes**. A controlled bench rig must specify contact area, loading rate, dwell, humidity and temperature; a gait lab must report results per shoe size, placement and wearer rather than converting bench force directly to clinical pressure.

| Metric | Proposed witness target (unvalidated) | Published comparator / interpretation |
| --- | --- | --- |
| Coverage and temporal detail | 4–6 latched sites per pair; no event timestamp or pressure waveform | novel pedar lists 84 or 99 sensors/insole and up to 400 Hz electronics; it measures a pressure map rather than a trip.[3] |
| Trip repeatability | Within ±15% of each cell's assigned force band on a bench rig, new and after 100,000 load cycles; report misses and spontaneous trips | pedar specifies <7% hysteresis for its pressure insoles, but this is a different quantity and test, not a direct accuracy comparison.[3] |
| On-foot safety | No increase in local peak pressure relative to prescribed footwear alone at mapped high-risk sites, across tested sizes and walking speeds | IWGDF defines demonstrated footwear offloading as ≥30% reduction against current footwear or <200 kPa using a calibrated in-shoe system with 2 cm² sensors; the witness does **not** demonstrate either condition.[1] |
| Service and cost | One-year service life with quarterly inspection; $12/pair ex-factory at 100,000 pairs/year in 2038, excluding fitting and follow-up | No validated service life or comparable whole-system price is asserted; pedar requires calibrated electronics, whereas this design has zero on-foot electrical power.[3] |

The pivotal falsification test is concordance: compare each latched site with reference pressure traces and report sensitivity to predefined excursions, false trips per wearer-week, missed unmapped hotspots and confidence intervals. Passing a repeatability bench test alone cannot establish ulcer-risk reduction.

## Deployment Scenarios

1. **Post-ulcer therapeutic-footwear follow-up:** A trained clinic maps and positions cells at previous ulcer sites after healing, checks the extra layer does not defeat prescribed offloading, and teaches shoe-off reading alongside skin inspection. An amber or invalid display triggers prompt fitting/clinical review, not a user-directed footwear modification.
2. **Community footwear service:** Where pressure mapping is available at a regional fitting center but not at every follow-up, a footwear worker checks flags, seal, wear and fit at scheduled visits. The device never substitutes for the original calibrated offloading assessment; poor referral access is a reason to limit deployment.
3. **Supervised usability research:** In an ethically approved study, users and caregivers with differing visual acuity compare high-contrast marks with ordinary checks. Investigators record non-wear, unreadable flags, false reassurance and actual referrals before considering routine service.

## Risks & Mitigations

- **False reassurance or missed events:** four to six sites cannot capture shear, ischemia, temperature, infection, cumulative load or a hotspot elsewhere. Keep daily skin checks and clinical review; measure miss rates against mapped pressure and clinical outcomes. Never label an untripped insert “safe.”
- **New harm from the device:** recessing a dome may still form a ridge or change gait; compare maps with and without the entire insert and stop a pilot on new focal peaks, abrasions or discomfort. Inspect the shoe interior for debris at each use.
- **Drift and invalid readings:** sweat, heat, polymer creep, manufacturing tolerance and repeated resets change the trip force. Use sealed cells, traceable lot calibration, pre/post-fatigue tests and a visibly invalid state; replace torn or shifted inserts rather than assuming an intact flag is reliable.
- **Human and access failures:** visual impairment, forgotten shoe-off checks and delayed referrals can erase benefit. Test large contrasting markings and caregiver workflows with intended users; log adherence and follow-up completion without requiring a connected app.
- **Evidence and regulatory uncertainty:** no ulcer reduction, diagnostic accuracy or medical clearance has been established. Claims and trial design need clinician, ethics and jurisdiction-specific regulatory review; a negative trial or new hotspots should halt scale-up.

## Vision for 2050

If independent trials establish safety, reliable interpretation and net clinical benefit, the witness could be a low-cost optional layer offered with professionally fitted therapeutic footwear. A clinic could read a simple physical trace of where loads crossed a locally calibrated band between visits without turning the shoe into a connected device. That future depends on preserved offloading, accessible follow-up and honest surveillance of failures—not on universal adoption or an assumed reduction in ulcers.

## Sources

[1] https://iwgdfguidelines.org/wp-content/uploads/2023/07/IWGDF-2023-02-Prevention-Guideline.pdf
[2] https://www.sensorprod.com/products/fujifilm-prescale-tactile-pressure-indicating-sensor-film
[3] https://novelusa.com/pedar
