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

## How It Works

At enrolment, an authorized clinic checks identity and guardian authority through its normal process, explains alternatives and creates a minimal summary from records and patient-reported items. The caregiver checks the displayed scope; the issuer signs each dated entry with its clinic key. The card is not a legal consent form: a press authorizes one disclosure or proposed update, not a procedure, future access or a finding that the patient has capacity.

At a later visit, a powered reader presents a signed request listing field groups, a session nonce and its credential expiry. The card checks that credential against its locally provisioned trust store, shows a short code linked to the request, and releases only selected fields while the caregiver holds the switch. Staff match the code and requested fields on the reader screen, confirm the person's identity independently, and assess the entry's provenance and date. For a new entry, the reader shows the proposed record before a separate approval; the clinician retains a separate source record. Missing, damaged, refused, disputed or expired cards revert to ordinary clinical assessment and paper records, never denial of emergency care.

A patient can ask an issuer to correct or replace entries using its clinical record, or withdraw permission to use the card. An offline copy already disclosed cannot be recalled, and an offline reader cannot know that a credential or entry was revoked after its last trusted update. Staff must ask about current wishes and conflicting records at each encounter; short credential validity only narrows this risk. Replacement requires an authorized clinic and patient-mediated reconciliation, not a remote wipe or global identity registry.

## Technical Architecture

- **Medium and power:** proposed ISO/IEC 14443-compatible 13.56 MHz antenna, secure element, NFC-harvested controller, bistable display and recessed switch in a sealed card with a replaceable sleeve. A display update, cryptographic check and transfer under weak coupling are an engineering hypothesis: bench-test the power budget before promising the existing five-second window.
- **Record format:** bounded, versioned 1–4 kB structured payload with at most 32 requested fields, typed source (`patient-reported` versus `clinic-recorded`), issuer ID, encounter date and entry signature. A display or reader must distinguish `unknown`, `unverified` and `verified issuer signature`; none means clinically correct. Reject oversized or malformed data and never open embedded links or execute payloads.
- **Trust and flow:** issuer signs entry → encrypted card storage → clinic reader sends signed scoped request plus nonce → card verifies locally cached reader credential and requires the switch → reader checks entry signatures and shows dated, attributed data → clinician reconciles against the person and other records. The clinic controls and rotates reader credentials; issuers distribute signed trust-store and revocation updates during managed visits. A disconnected reader with an expired or untrusted credential fails closed for card disclosure, while care continues by other means. A valid signature authenticates a key, not a diagnosis, patient identity or current consent.
- **Accessibility and data handling:** reader screens offer local-language text, large type and clinician read-aloud/teach-back; no card-only pathway for people with impaired vision, dexterity or literacy. Printed exterior should carry no diagnosis. Minimize local reader retention, follow applicable clinical record rules, and use an authorized repair/take-back path on retirement. These are design requirements, not implemented guarantees.

## Performance Benchmarks

No prototype measurements or directly comparable published head-to-head results are available. The comparison is **the same clinic, patient mix and task**, testing durable paper home-based records and an existing offline-capable electronic workflow alongside this card; do not call an unmatched product number the state of the art.

| Metric and test | Current-practice comparator (to measure) | Card gate (unvalidated target) |
| --- | --- | --- |
| Retrieve and interpret dated history in a supervised visit | Median seconds and correct-source rate on paper and offline app | ≤10 s electronic read, plus separately recorded identity/clinical review time; no worse correct-source rate |
| Scoped release and write authorization | Observe unintended disclosures/updates per 1,000 test encounters for each workflow | Zero in scripted replay, malformed-request and wrong-scope adversarial tests; quantify residual field rate |
| Durability and access | Successful record retrieval after 12 months of normal handling for paper/app | ≥95% card read success after defined bend, moisture and abrasion cycles, including weak coupling |
| Comprehension and equity | Teach-back of requested fields, right to refuse and fallback by language/literacy group | ≥90% correct teach-back in each tested group, without a worse refusal experience than paper |
| Cost | Fully loaded five-year cost per enrolled person for existing paper/app | Disclose card, reader, training, service, replacement and recycling costs; adopt only if benefit justifies incremental cost |

These are proposed acceptance gates, **not measured outcomes**. Report confidence intervals and failures, including inaccessible encounters; protocol, sample size and acceptance thresholds require independent clinical and privacy review. The card is not inherently faster or cheaper than paper.

## Deployment Scenarios

1. **Mobile vaccination clinic:** a caregiver voluntarily shows dated doses on a shared offline reader; staff confirm identity, check conflicts with the paper home-based record and do not infer that a missing dose is due to missing documentation. The clinic records any new dose in its own system first.
2. **Flood-disrupted primary care:** a clinic with power but no network can inspect an attributed allergy flag and limited history. If the card or reader fails, staff use normal history-taking and emergency protocols, rather than treating `unknown` as `no allergy`.
3. **Cross-facility transfer:** participating clinics provision each other's issuer keys under a governed agreement; an unfamiliar signature remains unverified. No universal interoperability, recognition of authority or cross-border legal validity is presumed.

## Risks & Mitigations

- **Stale consent and coercion:** an offline press proves neither free choice nor capacity. Ask privately, use teach-back and honor refusal or withdrawal; past screenshots and already shared data cannot be erased. Never use the card as a liability shield or a condition of care.
- **False identity or authority:** a stolen card, copied serial, forged issuer, changed guardianship or incorrect clinical entry can mislead. Independently check identity and legal authority, separate guardian/proxy permissions from patient preferences, and label source, age and verification state. Minors and incapacity require local policy and clinician judgment.
- **Compromised readers and key updates:** reader credential expiry and offline revocation lists limit but cannot eliminate disclosure before an update arrives. Rotate keys, audit reader provisioning, isolate compromised keys and fail closed on unverifiable requests; a malicious authorized reader can still photograph a screen.
- **Privacy, loss and exclusion:** encrypted storage does not protect printed markings, coerced access or clinical copies. Minimize fields, offer paper and accessible staff assistance, provide replacement and secure recycling, and test local-language comprehension. A cheap card may still impose unaffordable training and service costs.
- **Law and clinical safety:** jurisdiction-specific consent, recordkeeping and emergency exceptions require independent legal, ethics and clinical review. If staff substitute an apparently verified record for current assessment, the design has failed even when the cryptography works.

## Vision for 2050

If comparative trials show a net benefit, patient-held cards could coexist with paper and local health records where connectivity remains unreliable: a person chooses which dated summary to show, and participating clinics reconcile their own records when online. Success means fewer unsupported assumptions at the point of care without making a card mandatory. If simpler paper or offline software performs as well with lower cost or less exclusion, the responsible 2050 outcome is to use those instead.
