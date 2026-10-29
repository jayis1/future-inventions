# Snakebite Venom Triage Strip

**Author: jayis1. Status: TRL 2 concept, not a validated medical device.**

## Problem

WHO estimates 1.8–2.7 million snakebite envenomings and roughly 81,000–138,000 deaths each year. Venoms vary within and between species, and effective antivenom access depends on the local snakes and available products.[1] At an understaffed rural clinic, an unidentified bite can delay choosing an appropriate antivenom; existing clinical assessment and laboratory investigation remain essential.[2] A bite-site venom signal alone does **not** establish systemic envenoming or justify antivenom.

## Solution

A **reader-free, region-specific immunotype card** helps a trained clinic worker distinguish *locally relevant venom antigen groups*, not broad clinical syndromes such as “neurotoxic” or “haemotoxic.” A sterile swab of an accessible bite site enters a sealed buffer vial; the worker transfers a metered drop to a cellulose/nitrocellulose lateral-flow strip. Dried recombinant single-domain antibody (VHH) conjugates on colored latex beads bind selected venom antigens; distinct capture-line **positions and printed shapes** identify the groups, with a separate flow-control line. A factory-matched second path tests a fixed, pre-diluted aliquot to investigate high-dose hook effects. A high-barrier pouch carries lot/expiry markings and a passive temperature-excursion indicator; humidity ingress requires laboratory validation and any breached pouch is invalid. A sealed vial, no open venoms, no phone, no patient identifier and no network are part of the default design.

A proposed first research panel distinguishes two locally relevant immunotypes whose antivenom choices actually differ; expansion to additional groups requires *separate* binder discovery and validation. Published multiplex antibody strips have differentiated *Bothrops* and *Lachesis* venoms in spiked samples within 15 minutes, and a VHH prototype has differentiated a krait toxin from a cobra counterpart in spiked matrices; neither establishes that this proposed card works in patients.[3][4] A clinic must never substitute a panel from another region or infer that an unrepresented species is absent.

| Visible result | Worker-facing meaning (only after clinical validation) |
| --- | --- |
| One unambiguous group line with valid control | Possible antigen group; clinician checks local antivenom coverage and symptoms. |
| Multiple group lines, inconsistent dilution paths, or ambiguous line | **Indeterminate**; use clinical pathway and expert advice. |
| Control present, no group line | **No antigen detected by this panel**, not “dry bite” or “safe.” Continue clinical observation and referral. |
| No control, expired pouch, leaking vial or out-of-range storage indicator | **Invalid**; discard and follow the clinical pathway. |

**Never wait for the strip** if airway, bleeding, neuromuscular or other clinical signs demand urgent care. WHO emphasizes early treatment and access to effective antivenom; clinical signs and locally validated tests, not this concept, govern care today.[2]

## Key Innovation

Neither venom immunoassays nor VHH lateral-flow strips are new.[2][3][4] The testable integration is a **locally validated immunotype panel tied to an antivenom-coverage map**, with a parallel pre-dilution path and explicit indeterminate/no-clearance interpretation in an equipment-free package. It asks a narrow question—*which antigen group is detectable?*—rather than claiming to measure dose, severity, or need for treatment. Cross-reactivity, variable toxin expression, sample timing and interference could defeat it; binder performance and safe interpretation are the core research risks.

## Target Cost

**Unvalidated 2038 manufacturing goals at 1 million strips/year:** US$1.50–2.50 per sealed single-use card/vial pair (binder and latex reagents US$0.45–0.80; membrane/pads and printed housing US$0.35–0.55; swab/buffer/barrier pouch US$0.35–0.55; assembly, quality control and scrap US$0.35–0.60). These are planning allocations rather than supplier quotes; the ranges describe alternative builds, not an additive guaranteed quote. Add US$0.50–1.50 per test for regional stocking, training, quality surveillance and controlled disposal, excluding staff time, treatment, transport, product registration and validation. A failing binder or shelf-life programme invalidates the cost case; antivenom supply and referral capacity are much larger constraints.

## Impact

The first measurable goal is better **concordance of clinician antivenom selection with independently established local immunotype**, without delayed treatment or excess antivenom use. A planning scenario of 100,000 strips/year covers at most 100,000 testing encounters, not lives saved; clinical benefit is unproven. Intended users are trained primary-care staff, not bystanders. Printed position/shape keys, high-contrast lines, pictograms and translated instructions reduce dependence on color perception or connectivity. Regional public-health programmes could license open panel geometry and qualify local production, while retaining independent batch quality control.

## Validation, limitations and safe state

- **Targets, not results:** readable in 15 minutes; ≥95% sensitivity for each *covered immunotype* among analytically detectable, clinically sampled positive cases, ≥98% specificity against a predeclared regional off-target panel, ≤5% uninterpretable results in trained-user studies, and 18-month packaged stability at 40°C under tested humidity excursions. Report confidence intervals and every missed clinically important case; targets are go/no-go proposals, not clinical performance claims.
- **Bench gates:** test individual venoms across geographic populations and concentrations, cross-reacting nonvenomous material, blood/soil/antiseptic contamination, multiple sample times and high-dose hook effects; evaluate both dilution lanes. A control line proves flow only, **not** successful sampling or absence of venom. Reject a panel if dangerous cross-reactions or false-negative rates persist.
- **Clinical gates:** first compare blinded results with reference immunoassays and clinician decisions without changing care; then preregister a multi-site prospective trial comparing usual care with strip-assisted care, monitoring treatment delay, wrong-product selection, adverse reactions, sensitivity by species, and missed envenoming. Do not deploy as a treatment guide without local regulatory approval and demonstrated net clinical benefit. Stop the trial if clinically significant delays or excess missed cases occur.
- **Handling:** do not scrape, squeeze or cut a wound to obtain a sample. A negative swab can reflect inadequate sampling, prior washing or absent antigen at the surface. Packaging heat/humidity damage, exhausted reagents, high antigen loads and missing regional coverage must never be interpreted as reassurance. Observe and refer according to established local protocols regardless of strip result.
- **Disposal and access:** contain swab, used card and vial as potentially infectious clinical waste; do not reuse. Keep antivenom choice and care under a licensed clinician's authority. The 10–20 year pathway is binder selection, stability engineering, real-patient trials, independent assessment and regional manufacturing—not a claim of current readiness.

## Relation to other inventions

The [photoacoustic anemia screener](../photoacoustic-anemia-screener/) tests a noninvasive blood-related signal for anemia; the [thermostable vaccine patch](../thermostable-vaccine-microarray-patch/) delivers an immunization. Neither identifies locally relevant snake venom antigens. This concept is new **to this catalogue**, not a claim of first-in-world venom detection.

## How It Works

The bite-site swab is mixed in a sealed, metered buffer vial and applied to two matched capillary lanes. In each lane, aqueous sample wicks through a cellulose conjugate pad into a nitrocellulose membrane: venom antigen, if present and recognized, binds dried VHH–latex reporter and is retained at a spatially coded capture line. A separate procedural line checks that liquid migrated; it cannot verify that venom was collected. The second lane receives a factory-defined dilution to challenge a potentially saturated sandwich assay. Disagreement between lanes is indeterminate, not a corrected diagnosis. The clinician reads the card at the specified time against a region- and lot-matched key; no line, faint line or valid-looking negative establishes a dry bite, species identity or clinical severity. Only an authorized local care pathway can connect a supported antigen group to an antivenom choice.

## Technical Architecture

- **Collection and enclosure:** sterile swab, sealed buffer vial and metered transfer; no wound manipulation or open venom handling. The intended specimen is bite-site material, not interchangeable with blood or urine without new validation.
- **Signal path:** dried VHH–colored-latex conjugate on cellulose → capillary flow on nitrocellulose → two spatially distinct capture positions for the initial regional panel plus a flow-control position. Capture chemistry, antigen specificity, visual threshold and interference remain research questions; a color-blind-readable printed shape/position key is proposed.
- **Quality and decision boundary:** parallel fixed-dilution lane, printed read-time window, lot/expiry and temperature-excursion markings, barrier pouch and local antivenom-coverage card. The trained worker records result category, lot and time in the existing clinical record; the clinician interprets it alongside symptoms and locally validated investigations. No default app, identifier upload or automated treatment recommendation.

## Performance Benchmarks

| Endpoint and conditions | Published comparator / current state | This card's unmeasured design gate |
| --- | --- | --- |
| Visual read time | A research multiplex assay differentiated *Bothrops*/*Lachesis* in **15 min** in spiked plasma and urine; not a clinical bedside benchmark.[3] | Readable by a trained worker in **15 min** after applying a bite-site sample; prospective timed-user study required. |
| Analytical detection | That research assay reported **10–50 ng/mL** limits for selected venoms in spiked plasma/urine, and **50–500 ng/mL** in spiked serum; matrices and venoms differ from this swab concept.[3] | No justified swab limit of detection yet; establish a per-antigen, per-matrix threshold and high-dose performance before setting one. |
| Clinical discrimination | No patient-study sensitivity or specificity for this card; spiked-matrix analytical limits do not measure patient performance.[3][4] | **≥95% sensitivity** per covered immunotype in the specified sampled-positive population, **≥98% specificity** against a predeclared regional off-target panel and **≤5% indeterminate/invalid** in trained-user studies; report denominators and confidence intervals, and separately quantify missed envenomings. |
| Shelf life and delivered cost | No like-for-like published comparator established for this proposed swab-and-card package. | **18 months at 40 °C** after packaged stability testing; **US$1.50–2.50** ex-factory at one million units/year plus **US$0.50–1.50** for distribution/QA/disposal—planning goals, not quotes. |

These endpoints cannot be traded off against clinical safety: a faster antigen result does not measure time to effective antivenom or improved survival. Usual-care clinical assessment remains the comparator for any later outcome trial.[2]

## Deployment Scenarios

1. **Regional primary-care clinic:** after a suspected bite, trained staff begin standard assessment and referral immediately; in a future approved study, a locally validated card could add an immunotype clue while the clinician checks which stocked antivenom covers it. An unavailable antivenom or a negative card never suspends transfer.
2. **District receiving hospital:** a prospective observational pilot compares blinded strip categories with reference assays and independent clinician assessment without changing treatment. The value proposition is a measured reduction in inappropriate product selection *only if* a later controlled study shows it without additional delays or missed cases.
3. **Regional supply programme:** de-identified, aggregate counts of *validated* immunotypes could inform panel redesign and antivenom stocking after privacy and sampling-bias review. A positive swab count is not a count of systemic envenomings.

## Risks & Mitigations

| Failure mode | Design or validation response |
| --- | --- |
| Early, washed, poorly sampled or post-treatment wound yields a false negative; antigen excess masks a sandwich line | No-clearance wording; dilution-path disagreement becomes indeterminate; test across sample timing and loads; clinical signs override every strip result. |
| Related venoms cross-react or regional toxin composition shifts | Predeclare local coverage, test geographic isolates and sympatric off-targets; withdraw or redesign panels that cannot meet clinical safety gates. |
| Heat, humidity, expired reagents or lot drift degrade a card | Barrier packaging, excursion marking, stability and lot-release testing; breached/out-of-range units are invalid and replaced, never read as negative. |
| Faint lines, color-vision differences or timing errors cause disagreement | Positional/shape cues, timed pictograms and trained-user reader-agreement studies; ambiguous reads are indeterminate. |
| A valid control gives false reassurance; test use delays transport or antivenom | Control establishes flow only; monitor treatment delay and missed envenoming as stopping endpoints; prohibit clinical guidance before ethics review, local authorization and demonstrated benefit. |
| Correct antigen classification cannot fix antivenom stock-outs | Pair any deployment study with supply and referral audits; report access failures separately from assay accuracy. |

## Vision for 2050

If regional panels pass patient-level validation and health-system trials, a sealed card could become one modest piece of routine rural snakebite care: clinicians would see an additional, explicitly bounded antigen clue, while procurement teams would use privacy-preserving aggregate signals to adjust antivenom stocks. The aspirational outcome is fewer wrong-product decisions without delaying treatment—not a universal species detector, a replacement for clinical judgment, or a forecast of lives saved.

## Sources

[1] https://www.who.int/news-room/questions-and-answers/item/snakebite-envenoming
[2] https://www.who.int/teams/control-of-neglected-tropical-diseases/snakebite-envenoming/treatment
[3] https://www.nature.com/articles/s41598-024-51971-2
[4] https://www.nature.com/articles/s41598-026-73595-4
