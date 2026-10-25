# Offline Self-Fit Hearing Aid

**Author: jayis1. Status: TRL 2 concept; not a tested medical device or a substitute for ear care.**

## Problem

WHO estimates that **more than 400 million people** could benefit from hearing devices, yet fewer than **20%** of those needs are met.[1] A hearing aid is not appropriate for every cause or degree of hearing loss. In many communities, the device, fitting appointment, batteries, repairs and follow-up are separate barriers. A phone-dependent self-fitting product can exclude people without a compatible phone, data access or reliable charging.

## Solution

A repairable, behind-the-ear **air-conduction** aid for adults with perceived mild-to-moderate hearing loss combines a MEMS microphone, low-power digital signal processor, four-band compression, a vented silicone earmould or replaceable dome, and a replaceable **0.5 Wh rechargeable lithium-iron-phosphate cell** in a keyed, water-resistant compartment. A physical rotary selector and two guarded buttons run an offline fitting sequence: first a quiet-room noise check, then limited-level tones and speech samples at several bands, followed by user-selected comfort and clarity settings. The microphone checks ambient noise and detects feedback; it cannot measure a calibrated clinical audiogram in an uncontrolled room. In-ear acoustic levels, frequency response and output limit are factory-tested with an ear simulator; the firmware rejects a fitting with noise, excessive feedback or inconsistent responses. Settings remain on the device, with no radio, account, recording storage or remote adjustment.

A trained community worker can check fit, hygiene and warning symptoms, but the adult can repeat the fitting without a smartphone. This is a *candidate* service model: jurisdictions differ in medical-device rules. In the US, OTC air-conduction aids are for adults 18+ with perceived mild-to-moderate loss, and self-fitting aids are already an established regulated category.[2][3] Ear pain, drainage, sudden or one-sided loss, vertigo or unexpectedly poor speech understanding require medical assessment rather than more amplification.

## Key Innovation

Self-fitting hearing aids, DSP compression and rechargeable cells already exist.[2][3] The proposed contribution is their **phone-free, locally serviceable integration**: fitting controls that explicitly reject invalid acoustic conditions, a replaceable standard-form cell and ear interface, and a physical-controls fitting and acoustic service-check workflow usable by trained non-specialists. Unlike the repository's [ambient communication implant](../ambient-communication-implant/), this does not stimulate a nerve, translate speech, network people or augment normal hearing; it only amplifies external sound for eligible adults. Unlike [field-calibrated adjustable spectacles](../field-calibrated-adjustable-spectacles/), it treats hearing rather than refractive blur, and requires acoustic output validation rather than an acuity chart. No patent novelty is asserted. The critical unproven question is whether this integrated workflow yields safe, retained benefit at lower total cost than locally available OTC or professionally fitted alternatives.

## Target Cost

**Unverified 2038 planning target at 100,000 units/year:** US$65 ex-factory per aid, comprising US$8 microphone/receiver, US$12 DSP/PCB, US$10 cell/charge protection, US$6 housing/controls, US$5 earmould/domes, US$7 assembly, US$8 acoustic test and rejects, and US$9 manufacturing overhead. The first seven allocations total US$56; overhead brings the total to US$65. A shared USB charger is a separate **US$8–12 target**, not included in the unit price. A three-year service-life scenario at US$65 plus US$5/year for domes, cleaning and cell replacement averages approximately **US$27 per aid-year** before fitting, distribution, taxes, repairs, charger and professional referrals. These are not supplier quotes; validate against both ordinary hearing aids and cheaper assistive listening or captioning options. Community health programmes or cooperatives could buy devices and fund follow-up; affordability to users depends on that service budget, not factory cost alone.

## Impact

A deployment scenario of **100,000 aids/year** could equip at most 100,000 ears annually, not necessarily 100,000 people or successful fittings. Proposed **test targets, not measured outcomes**: at least 12 hours of use per charge after cell-aging tests; a repeatable quiet-room fitting in under 15 minutes with invalid-condition lockout; and at least 80% of eligible trial participants retaining use at six months, with self-reported communication benefit and adverse-event rates measured against a locally available comparator. Test electroacoustic output, distortion, maximum output and feedback against the applicable hearing-aid standards and regulatory limits before any human deployment. Measure benefit in speech-in-noise testing and user-reported communication, including by age, language and dexterity; do not infer restored hearing from device distribution.

A 10–20-year path is bench electroacoustics and battery abuse tests, supervised adult fitting trials with audiologist reference, independent multi-site comparisons, then regulated manufacture and local repair training. WHO's task-sharing guidance is a service precedent, not evidence that this device works.[1] A much longer-term reduction of the access gap is possible only if supply, ear care and follow-up also improve.

## Risks and limitations

- **Unsafe amplification or missed disease:** hard-limit output in hardware and firmware, log only diagnostic fault codes locally, reject fittings with feedback/noise or unstable answers, and provide red-flag referral instructions. Independent testing must establish safe output for the chosen ear coupling and meet local regulation; a comfort judgment alone is insufficient.
- **Failure and maintenance:** low battery or faulty microphone/receiver must mute output rather than emit a transient; a clogged wax guard, blocked vent, poor dome fit or moisture ingress prompts cleaning/replacement and retest. No unsupervised use for children, severe/profound loss or sudden loss. Include a one-month check and six-month follow-up in the pilot.
- **Materials and end of life:** removable cell needs short-circuit protection, fire-safe charging and approved recycling; take back the PCB and cell, and replace silicone domes hygienically. Avoid claims of zero waste or zero energy. Charging requires electricity, roughly 0.5 Wh stored per full cycle plus charger losses; solar USB is optional, not self-powering.
- **Access and autonomy:** tactile controls and translated paper pictograms should be usability-tested with low-literacy users; no microphone audio is recorded, transmitted or used for surveillance. Participation is voluntary, and users retain access to sign language, captions and clinical care regardless of device uptake.

## Sources

[1] WHO, hearing-aid service delivery in low- and middle-income settings (2024): https://www.who.int/news/item/01-03-2024-who-issues-guidance-to-improve-access-to-hearing-care-in-low--and-middle-income-settings

[2] FDA, OTC hearing aids and intended adult population: https://www.fda.gov/medical-devices/hearing-aids/otc-hearing-aids-what-you-should-know

[3] FDA, self-fitting air-conduction hearing aid classification: https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfpcd/classification.cfm?id=QUH
