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

## How It Works

**Proposed workflow, not a validated assay.** The technician records the product, strength, formulation, lot and card serial; a lot-traceable supplier certificate links the sealed 80% and 100% API deposits to a qualified reference material. A measured tablet extract is applied to the sample lane without touching the reference lanes. Development in the card's medicine-specific solvent moves each component through the cellulose/silica stationary phase; migration distance offers a tentative identity check, while integrated optical response offers a *hypothesis* for dose bracketing. A shared card and enclosed optical path can reduce some environmental variation, but shared solvent or matrix interference can also bias all three lanes.

After development, the reader subtracts local background, checks reference-band migration, intensity order (80% below 100%), saturation, card expiry and its calibration tile, then compares the sample only within a formulation-specific validated response window. A below-threshold or mismatched band prompts **SUSPECT—SEND FOR LABORATORY CONFIRMATION**; a failed control, overlapping bands, unsupported formulation or uncertain response prompts **INCONCLUSIVE**. No third, reassuring classification is issued. A screened tablet is consumed by testing; all remaining units follow the responsible authority's existing procedures while confirmatory testing is arranged.

## Technical Architecture

- **Traceable consumable:** sealed three-lane cellulose/silica card, printed serial/expiry, two independently quality-controlled reference deposits and a dedicated mobile-phase sachet. Reference stability under heat and humidity is an experimental gate, not a solved packaging claim.
- **Sample boundary:** single-use crushing/extraction vessel, measured solvent and fixed-volume applicator; prevent carryover with disposable contact surfaces and procedural blanks in validation runs.
- **Optical chain:** light-tight enclosure, LED, image sensor, fixed geometry and calibration tile feed a local processor. Store raw band images and calibration metadata without patient data; version the medicine-specific decision algorithm and preserve an auditable, offline export for the inspector.
- **Decision boundary:** method configuration checks API, formulation, strength, lot and control validity before calculating a blank-corrected sample-to-reference response. Preserve raw values, failure codes and uncertainty; never treat a failed check as a negative result. Laboratory HPLC or an appropriate pharmacopoeial assay—not this card—adjudicates a suspect signal.

## Performance Benchmarks

These are **unmeasured engineering targets** for a single validated tablet formulation, not reported device performance. The state-of-art comparators are established *methods*, not interchangeable guarantees: GPHF Minilab uses reference-supported TLC [3]; the laboratory evaluation of portable screens found reduced-dose discrimination harder than identifying absent or wrong API [2]. Laboratory HPLC is the proposed adjudication method, not a cost-equivalent field competitor. No defensible head-to-head price, sensitivity or runtime figure is assumed for either comparator without a matched protocol.

| Endpoint | Proposed gate (unmeasured) | Comparable baseline / measurement |
| --- | --- | --- |
| Under-strength detection | ≥90% sensitivity at ≤80% label claim | Blinded, lab-assayed 80% and 50% dose tablets; compare matched Minilab visual TLC and HPLC truth. |
| Compliant-product false alert | ≥95% specificity | Blinded compliant tablets spanning allowed formulations and excipient lots; report confidence intervals. |
| Invalid controls | ≤5% within labeled storage window | Count all expired, failed, saturated and out-of-range cards, not only readable ones. |
| Consumable / reader | US$1.20 per card / US$180 per reader at stated volumes by 2038 | Unquoted bill-of-material targets above; exclude labor, reference QA, shipping, disposal and confirmation. |
| Operational repeatability | Establish before field release; no numerical result yet | Repeat blinded samples across operators, reader units, card lots, temperatures and humidity; stratify by site. |

Pre-register decision thresholds and sample sizes, report confidence intervals and false-accept/false-reject rates per drug and formulation, and benchmark time-to-result and total cost per *valid* result in a prospective study. A visual TLC miss or HPLC disagreement is not evidence of this design's superiority until tested on the same blinded samples.

## Deployment Scenarios

1. **District pharmacy inspection:** a trained inspector samples a wholesaler lot, logs the card and medicine batch, and forwards suspect or inconclusive results to the national medicines authority with the image record. An illustrative 100 lots per site per year is a capacity assumption, not a quality estimate. The card cannot authorize seizure or release.
2. **Central medical-store intake:** a procurement quality officer screens a risk-based sample from incoming single-API tablet lots, maintains custody records, and refers discrepancies for independent HPLC before a regulator-approved stock decision. Sampling one tablet cannot establish lot-wide uniformity; a missing reference or out-of-range formulation yields no result.
3. **Supervised community pharmacy:** a technician facing a supply-chain alert screens a permitted formulation and requests a laboratory referral if flagged. The workflow must preserve access to clinically necessary treatment under local guidance; no seller-facing 'authentic' stamp or consumer pass certificate is produced.

## Risks & Mitigations

| Failure mode | Control and evidence still needed |
| --- | --- |
| Counterfeit, substituted or degraded 80%/100% reference | Supplier qualification, chain-of-custody serials, independent assay of reference lots, tamper evidence, real-time and accelerated stability; fail closed on expiry or missing controls. |
| Excipient interference, incomplete extraction, nonlinear optical signal | Validate each API/formulation/strength against HPLC across excipient lots, aged and deliberately altered samples; reject overlapping or saturated bands. |
| Missed substandard tablet or false rejection of genuine stock | Pre-register false-accept/false-reject limits, blind multi-site comparison, repeat sampling and confirmatory referral; never claim a non-flagged lot is safe. |
| Cross-contamination, operator or calibration error | Single-use wetted parts, training and competency checks, calibration tile, battery self-check, audit images and explicit inconclusive codes. |
| Solvent exposure, consumable waste and unequal access | Contained handling, local hazardous-waste route, replaceable reader components and funded referral/training capacity; quantify discarded cards and access delays in pilots. |
| Unapproved deployment or misuse of records | Obtain jurisdiction-specific quality-system and regulator review before operational use; minimize personal data and restrict offline record access. |

## Vision for 2050

If per-formulation analytical validation, independently traceable references and affordable confirmatory laboratories become routine, a pharmacy inspector could carry a compact card-and-reader kit alongside established Minilab and laboratory networks. A lot's screening record would travel with its custody record, while a suspect signal would reach a regulator and a laboratory rather than becoming a consumer-facing badge of authenticity.

Widespread use is conditional, not a forecast: reference supply, stable cards, operator competence, disposal and equitable access must all scale with the test. The enduring idea is not that a paired card proves a medicine safe; it is that a deliberately limited, controlled comparison can make some hidden quality problems easier to escalate before they disappear into a distribution chain.
