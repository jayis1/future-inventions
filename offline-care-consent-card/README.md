# Offline Care Consent Card

**Author: jayis1**

**Category:** Privacy-Preserving Health & Universal Basic Services

**Status:** Concept; clinical and security performance unvalidated

## Problem

A displaced family may bring a paper vaccination card to one clinic but not the next. Paper can be lost, phones need power and connectivity, and a central registry may be unavailable or unsafe to use. WHO/UNICEF estimated **14.3 million zero-dose infants in 2024** and nearly **20 million infants missing at least one DTP dose** [1]; missing records are only one possible barrier, **not** the cause of those counts. The potential users also include millions of mobile patients whose treatment histories need to travel between providers. A card cannot substitute for outreach, vaccine supply, trusted clinicians or a lawful birth certificate.

## Solution

A caregiver holds a credit-card-size, battery-free **13.56 MHz NFC** care card. At a visit, a nurse presents an offline clinic reader; its screen names the exact fields requested in the local language. The caregiver presses and holds a recessed button on the card for the roughly **5-second** transfer window. The reader receives only a selected care summary (for example, dated vaccine doses and a patient-reported allergy flag), labels each entry's source, and shows an explicit **unknown** state for absent data. The clinician checks the patient and paper records before care; no card is required to receive treatment. A clinic can add a signed encounter only after the caregiver approves the displayed update. No cloud account, biometric, radio beyond near-field NFC, or universal identity number is needed.

The concept joins an inexpensive NFC secure element, local display, physical consent switch, and offline clinic-issued signatures. It is a **proposal for a limited portable record**, not a proven medical device or an identity credential. A patient may instead use a paper record or decline the card. Clinicians retain their normal records under local rules; the card never becomes the only copy.

## Key Innovation

The proposed advance is **transaction-bounded, field-scoped consent** on a self-custodied card: the reader sends a human-readable requested-field list, the card displays a short field-group code matched to the reader screen, and its physical switch enables only that signed request, for one session. A secure element stores encrypted entries and issuer public keys; an NFC-powered microcontroller drives a low-power bistable display and keeps the key out of the reader's reach. A signed append-only log plus revocable clinic *reader credentials* limits unauthorized writes, but does not prove that a clinical claim is true. NFC, secure elements, electronic health records and paper home-based records already exist; the unproven engineering step is making granular consent, trustworthy offline verification, low cost and usability work together across clinics.

The operating target is a **1–4 kB summary**, no more than **32 requested fields** per transfer, and **≤10 seconds** for a normal read in a powered-reader clinic. The passive card cannot power its display or release data without a reader field: **power loss or a damaged switch means no electronic read**, with normal clinical fallback. A photo of the reader screen or coercion by a person in authority cannot be prevented cryptographically; no claim of coercion-proof privacy is made.

## Target Cost

**Planning targets, not supplier quotes:** US$8–12 ex-factory per reusable card at 100,000 units/year in the mid-2030s (secure element/NFC US$2–3; bistable display and switch US$3–4; PCB, enclosure, assembly and testing US$3–5), plus US$40–70 for an offline reader or a certified clinic-phone adapter. At **five years** of use and US$2/year in replacement/service allowance, the card-only planning cost is roughly **US$4/person-year**; provision, training, clinician time, translation, repair, reader fleet, certification and data migration are excluded. Above US$15/card before distribution, compare directly against durable printed home-based records before adoption. Use a replaceable protective sleeve; sealed electronics require accredited repair/recycling rather than unsafe informal burning.

## Impact

A pilot target is **10,000 voluntary cardholders and 20 clinics** with matched paper-record comparison. Measure verified history availability, invalid/unknown reports, wrong-patient association, unauthorized disclosures, caregiver comprehension, lost-card replacement and clinical errors; do not count card issuance as averted illness. If a future programme reaches one million consenting people, it provides at most **one million portable summaries**, not one million prevented missed doses. Impact requires demonstrated benefit over paper and existing registries, privacy review, local-language accessibility and independent clinical validation.

A stolen card exposes its printed exterior but not the encrypted summary without an authorized reader and a working consent switch; a coerced owner, compromised reader, copied screen, malicious clinic, false signed entry or failed key-revocation update can still disclose or corrupt information. Reader credentials have short local expiry; a clinic unable to validate a signature displays **unverified**, not safe. Lost cards are replaced using existing clinician records and patient-mediated reconciliation, never remote tracking. No location logs, central lookup, biometric enrolment, authority-controlled remote revocation of a person's card, surveillance or access-control use. Retire failed electronics via a local take-back path.

**Development gate (10–20 years):** bench-test passive NFC power under weak coupling, switch failure and replay resistance; red-team reader and issuer compromise; compare comprehension across languages and literacy levels; then run an independently reviewed, consented clinical trial against paper and existing electronic records. Stop if false reassurance, coercive use or replacement burden exceeds demonstrated benefit.

### Evidence and prior art

1. WHO/UNICEF, “Global childhood vaccination coverage holds steady yet over 14 million infants remain unvaccinated,” 15 July 2025: https://www.who.int/news/item/15-07-2025-global-childhood-vaccination-coverage-holds-steady-yet-over-14-million-infants-remain-unvaccinated-who-unicef
2. WHO, *Digital adaptation kit for immunizations* (home-based records, offline workflows and privacy requirements): https://www.linkedimmunisation.org/wp-content/uploads/2025/07/WHO-Digital-Adaptation-Kits-for-Immunization.pdf

Unlike this repository's **Thermostable Vaccine Microarray Patch**, which addresses vaccine delivery, and **Receive-Only Disaster Bulletin**, which distributes public warnings, this proposal addresses voluntary offline access to a patient-held clinical summary. It does not claim novelty in NFC, cryptography or home-based records individually.
