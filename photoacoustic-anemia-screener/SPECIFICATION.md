# Photoacoustic Anemia Screener — Research Specification

**Author: jayis1. Concept only; no clinical-use authorization.**

## Mechanism and prototype architecture

- Use current-limited 660 nm and 850 nm pulsed LEDs behind a diffusing window; characterize emitted energy, pulse width and spectral power at the **skin surface**, and test against applicable photobiological safety limits before human contact. A short pulse deposits heat in absorbers; the initial pressure is approximately `p0 = Γ μa F`, where Γ is the local Grüneisen coefficient, μa is absorption coefficient and F is local optical fluence. Unknown fluence and blood volume mean amplitude alone **cannot** give systemic hemoglobin concentration.
- Bond a PVDF film receiver to a replaceable acoustic contact pad. Characterize bandwidth and impulse response with a tissue phantom, rather than assume a microphone can resolve superficial depth. An adjacent low-amplitude piezo reference transmitter can check acoustic coupling; this is a separate quality channel, not a hemoglobin signal. Add a pressure-limited spring mechanism with a mechanical stop and a pressure witness; qualify allowable contact force in a human-factors and skin-safety study rather than specify an arbitrary safe force.
- Acquire both wavelengths at baseline, during gentle reversible blanching, and after reperfusion. Fit an empirical blood-linked feature using depth-gated acoustic arrivals plus the acoustic coupling check; reject incomplete recovery, motion, low perfusion, detector saturation and off-calibration readings. A ratio may help cancel some nuisance variation, but oxygen saturation, wavelength-dependent melanin absorption and fluence changes remain confounders. Do not train on participant identity, demographic shortcuts, or a proxy for skin color.
- Operate offline on a rechargeable cell, encrypt or discard calibration-service logs, store no patient waveform by default, and publish the classification threshold and invalid-read rule for independent audit. A clinical validation protocol, not the prototype, determines final thresholds.

## Quantitative design gates (all unverified)

| Gate | Proposed acceptance test |
| --- | --- |
| Reference accuracy | Paired venous complete blood count (CBC) obtained during same visit; independently audited laboratory quality control |
| Clinical triage | ≥90% sensitivity and ≥80% specificity for a prespecified, population-appropriate anemia threshold; report confidence intervals |
| Equity | Each preregistered pigmentation/age/pregnancy stratum separately meets the clinical gate or the product is restricted and reworked |
| Invalid reading | Report rate and causes by stratum; target <10% of attempts, with no invalids coded as negative |
| Use time | Target <60 s including contact check and pressure-release cycle; time in observed outreach workflow |
| Service life | Five-year financial model; verify receiver, pad, LEDs and battery durability with accelerated aging and field cycles |
| Unit economics | US$100–150 at 100,000 units/year; US$20/year service, both subject to real sourcing and clinical quality cost |

Bench validation should first use tissue-mimicking phantoms varied independently in absorber concentration, scattering, pigment layer, oxygenation and flow. Then a blinded pilot with paired CBCs should establish whether systemic hemoglobin information survives these confounders at all. If not, stop rather than fit an apparently accurate but site-specific model. A multicentre prospective study must include intentionally diverse skin tones, low-perfusion conditions and pregnant patients, with an independent holdout site. Evaluate harm from missed anemia and referral burden, not just average absolute error.

## Safety and maintenance

An exposure interlock disables the LEDs when the pad is not seated; fail dark on controller, battery or calibration fault. Pressure-release mechanism must not trap a finger; use wipeable biocompatible pad materials and a locally replaceable module. Between users clean according to a validated local infection-control protocol; visually inspect window and membrane for cracks and contamination. Annual optical/acoustic phantom checks and battery inspection are planning targets; service more often if drift is found. No automatic treatment decision, patient tracking, military, surveillance, or behavioral-control functionality is included.

## Closest prior art and maturity

Photoacoustic sensing and noninvasive optical hemoglobin research already exist; the unproven contribution is the within-person pressure-perturbation protocol coupled to a contact-quality gate and honest triage abstention. See [README.md](./README.md#sources) for WHO and technical references. The 10–20 year horizon is for resolving calibration/fairness, serviceability, and medical-device approval, not an assertion that any current prototype meets these gates.
