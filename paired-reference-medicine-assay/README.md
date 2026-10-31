# Paired-Reference Medicine Assay

**Author: jayis1**

**Category:** Medicine Quality & Universal Basic Services / Pharmacy Screening

**Status:** Concept (TRL 2; neither validated nor authorized for medicine-release decisions)

## Problem

The WHO estimates that at least one in ten medicines in low- and middle-income countries is substandard or falsified; this is an estimate across surveyed products, not a risk estimate for any particular pharmacy or drug.[1] A medicine may contain the right active pharmaceutical ingredient (API) but too little of it. In a laboratory comparison of twelve portable screening devices, simple paper color tests reliably identified absent or wrong APIs but missed reduced-dose samples; quantitative screening remained substantially harder.[2] Patients and procurement teams need affordable, *supervised* early warnings without a false certificate of safety.

## Solution

A trained pharmacy technician crushes one randomly sampled solid-dose tablet from a lot, extracts it into a measured volume of validated low-hazard aqueous ethanol, and applies a fixed-volume aliquot to a **sealed, single-use microchromatography card**. Three parallel lanes on cellulose/silica-coated paper carry sample, a lot-traceable 80%-of-label API reference and a 100%-of-label reference. A medicine-specific mobile-phase sachet drives separation; a reusable, battery-powered enclosed LED reader images the developed bands with a fixed optical path and local calibration target. The offline reader compares band migration and *blank-corrected integrated response* to both standards; it displays only **SUSPECT—SEND FOR LABORATORY CONFIRMATION** or **INCONCLUSIVE**, never “safe” or “authentic.” A tested lot does not certify unsampled units. No patient identifier, cloud account or remote control is needed.

Initially restrict the research to one well-characterized, single-API, immediate-release tablet formulation with an independently validated extraction, separation, optical response and stability window. Other APIs or formulations require their own methods; do not apply one universal solvent or threshold. Any damaged card, missing control band, aged reference, saturated signal, failed battery check or out-of-range migration is inconclusive. Suspected lots go through existing regulatory/clinical referral, not ad-hoc withdrawal or substitute dispensing by the device.

## Key Innovation

Thin-layer chromatography and GPHF Minilab screening already exist; the Minilab supplies reference standards and covers many compounds, but is a laboratory-style kit, not this sealed, medicine-specific card.[3] Paper analytical devices likewise already identify absent or substituted ingredients but were not designed to quantify under-strength products reliably.[2] The proposed research delta is **paired on-card dose bracketing plus mandatory control validity in a closed extraction-to-read workflow**. It asks whether known near-threshold references and deliberate *inconclusive* outputs can improve reduced-dose triage relative to existing low-cost visual TLC, without sacrificing specificity. It is not a claim that chromatography, optical reading, or on-card references are unprecedented. Optical response may not scale with concentration; if matrix effects or humidity defeat bracketing, the design fails.

## Target Cost

**Unquoted 2038 design target at 100,000 cards and 10,000 readers/year:** US$1.20 per disposable test (US$0.35 patterned substrate and laminate, US$0.35 traceable reference loading/QC, US$0.25 sealed solvent and extraction consumables, US$0.25 packaging/assembly) and US$180 per reusable reader (US$45 optics/LED, US$45 enclosure, US$35 sensor/controller, US$25 replaceable battery, US$30 assembly and calibration). These are planning allowances, not bids. Budget approximately US$30/reader-year for calibration and battery/optical service and at least US$5 per confirmatory referral specimen *as a placeholder*, not a claimed lab price. Sampling labor, controls procurement, stability testing, shipping, quality-system certification, disposal, customs and confirmatory HPLC are excluded. Never subsidize a cheap card by hiding the cost of regulatory-grade references or laboratory confirmation.

## Impact

A planning scenario of 1,000 supervised pharmacies screening 100 lots/year would create **100,000 lot-screening opportunities/year**, not 100,000 safe lots or lives saved. If 5% are suspect/inconclusive and all are referred, that is 5,000 laboratory referrals/year; actual rates will vary by market and method. Compare against well-run Minilab TLC and laboratory HPLC on blinded good-quality, 80%-dose, 50%-dose, absent-API, wrong-API and aged/matrix-interference samples. Proposed pilot gates: ≥90% sensitivity for ≤80%-dose samples, ≥95% specificity for compliant samples, ≤5% invalid controls under labeled storage, all with prespecified confidence intervals and site-level stratification. These are *unmeasured targets*, not clinical or regulatory guarantees. Do not deploy unless confirmatory capacity, trained operators, a safe procurement response and local authorization exist. A 10–20-year path is analytical development, accelerated and real-time stability, independent multi-site blinded validation, workflow/health-economic trials, and jurisdiction-specific quality-system review.

## Limits and safety

- **False reassurance:** even a visually normal band cannot establish content uniformity, dissolution, impurities, sterility or absence of toxic contaminants. A result is a screening observation about one sampled tablet only. Routine supply-chain quality assurance and regulator-approved assays remain necessary.
- **False alerts:** excipients, degradation and camera/lighting variation may mimic a low dose. Use blinded HPLC comparison, fixed optics, paired controls and an inconclusive state; do not auto-reject entire stock.
- **Handling:** use trained staff, gloves and a contained ventilation-compatible extraction protocol; select a validated solvent per API, prohibit open flames, contain sharp/crushed-tablet debris and send solvent/reagent waste through local hazardous-waste channels. Do not promise benign effluent from unspecified chemistry.
- **Loss of function:** no valid reader calibration, control or electricity means no reading; the medicine still follows ordinary clinical and regulatory procedures, not a device-generated approval. Replaceable LED/battery and locally serviceable housing reduce reader waste; consumable cards remain a burden to audit.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/substandard-and-falsified-medical-products — WHO substandard and falsified medical products
[2] https://journals.plos.org/plosntds/article?id=10.1371/journal.pntd.0009360 — Laboratory evaluation of twelve portable devices
[3] https://www.gphf.org/en/minilab/factsheet.htm — GPHF Minilab fact sheet
