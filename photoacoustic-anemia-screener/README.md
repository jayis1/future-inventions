# Photoacoustic Anemia Screener

**Author: jayis1. Status: TRL 2 research concept; not a diagnostic device or substitute for a blood test.**

## Problem

WHO estimates anemia affects **40% of children aged 6–59 months, 37% of pregnant women, and 30% of women aged 15–49** worldwide.[1] Screening usually needs a blood sample and trained handling; recurring lancets, cuvettes, disposal, and clinic visits complicate outreach. Hemoglobin concentration matters for triage, but anemia has many causes: this instrument would not identify iron deficiency or prescribe treatment.

## Solution

A trained community health worker places a clean fingertip against a replaceable, disinfectable optical/acoustic contact pad. Short, current-limited pulses from **660 nm and 850 nm LEDs** illuminate superficial vessels; optical exposure limits require bench verification before human use. A **PVDF piezoelectric film** receives the resulting thermoelastic pressure wave. A spring-limited, manually operated pad briefly reduces local blood volume, then releases it. The processor compares signals before, during, and after release to try to subtract static tissue absorption, while a second acoustic reference pulse tests contact quality. A screen returns either **“blood test needed,” “no flag—follow clinical screening schedule,” or “invalid—use standard test”**; it does not display a falsely precise diagnosis. No cloud, radio, camera, microphone, patient identity, or stored raw waveform is required.

The physical principle is photoacoustic conversion: absorbed optical energy causes local thermal expansion and a detectable pressure transient. **It is not established that a low-cost fingertip probe can reliably infer systemic hemoglobin concentration**: local blood volume, oxygenation, tissue scattering, nail/skin pigmentation, temperature, perfusion, and contact pressure may dominate the signal. The pressure cycle is a testable method to separate blood-dependent signal from background, not a solved calibration.

## Key Innovation

The proposed contribution is a **paired-pressure, multiwavelength photoacoustic measurement with an explicit invalid-reading gate**. Existing noninvasive optical hemoglobin proposals rely on optical absorption; photoacoustics adds depth/time information, and the pressure cycle supplies a within-person blood-volume perturbation. Neither LEDs, PVDF nor photoacoustics is new.[2] The research question is whether these measurements yield a robust blood-linked feature across real skin tones and clinical conditions at a cost that beats repeated consumables. If not, this concept fails its principal gate rather than claiming melanin independence; pigmentation can also distort photoacoustic measurements.[3]

## Target Cost

**Unvalidated 2035 target at 100,000 units/year:** US$100–150 per reusable screener, including dual LED driver and optics (US$25–35), PVDF receiver and analog front end (US$20–30), pressure-limited contact mechanism (US$10–15), controller/display/battery (US$25–40), and assembly/calibration (US$20–30). These are planning allocations, not supplier quotations; ranges are not a guaranteed additive quote. Budget **US$20/year** for cleaning, battery replacement, and calibration checks; replace the contact pad if damaged. At **2,000 screens over five years**, US$120 capital plus US$100 service is **US$0.11/screen**, excluding worker time, confirmatory blood tests, training, regulatory costs and distribution. A blood-based point-of-care test remains the accuracy comparator, not an assumed more expensive alternative. Procurement is sensible only if total referral and missed-case costs improve in trials. Local pad replacement and offline calibration transfer are required to avoid vendor lock-in.

## Impact

A district-health pilot could offer opportunistic anemia triage to people who otherwise miss routine testing; **100,000 devices × 400 screens/year = 40 million screening encounters/year** at the assumed utilization, not 40 million distinct people diagnosed or treated. Clinical benefit depends on sensitivity, specificity, follow-up capacity, and whether screening improves outcomes over existing blood-test pathways. The first measurable goal is **at least 90% sensitivity for clinically defined anemia with at least 80% specificity** against a laboratory complete blood count in a preregistered population; these are proposed go/no-go criteria, not reported results. No treatment or population-level health effect is claimed without prospective evidence.

## Safety, limitations, and validation

- The spring stop must limit pressure and exposure under applicable optical/medical-device standards; reject cracked pads, poor acoustic coupling, low battery, motion, and inadequate perfusion rather than emit a reassuring result. Test skin irritation and cleaning compatibility. No use on injured skin.
- A negative screen must not overrule symptoms, pregnancy care, or a clinician’s decision to order a blood test. False negatives are the primary hazard; confirm all flagged and symptomatic cases by established methods. A quality-control failure defaults to **invalid**, not “normal.”
- Preregister paired measurements against venous CBC in children and adults, stratified by skin pigmentation, age, pregnancy, perfusion and site; report sensitivity, specificity, error distribution and invalid-read rate separately for each stratum. Require an independently validated cohort before clinical claims. See [SPECIFICATION.md](./SPECIFICATION.md) for engineering gates.
- This is not a surveillance or control instrument: no biometric template or network identifier is collected. An optional clinic record belongs in existing consent-based health systems, not on the device. The health worker is the user; clinics/public-health programmes are deployers and payers. A 10–20 year path covers prototype signal validation, independent multicentre trials, regulatory review, and regionally serviceable manufacturing—not immediate deployment.

## Relation to prior inventions

Unlike the [thermostable vaccine microarray patch](../thermostable-vaccine-microarray-patch/), which delivers an antigen through skin, this concept measures a blood-related optical-acoustic response without penetration. Unlike the [regenerable dialysate kidney belt](../regenerable-dialysate-kidney-belt/), it is a screening tool rather than a treatment loop. No existing folder addresses anemia triage or pressure-differenced photoacoustics.

## Sources

[1] WHO, “Anaemia” fact sheet: https://www.who.int/news-room/fact-sheets/detail/anaemia

[2] Review of noninvasive hemoglobin sensing and optical limitations: https://pmc.ncbi.nlm.nih.gov/articles/PMC9346606/

[3] Experimental study of skin-tone effects on photoacoustic imaging/oximetry: https://pmc.ncbi.nlm.nih.gov/articles/PMC10732256/
