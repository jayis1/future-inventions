# Mill-Gate Maize Sorter

**Author: jayis1. Status: research concept; not a food-safety test or certification.**

## Problem

Aflatoxins in maize can cause acute poisoning and increase liver-cancer risk; mould toxins may persist through food processing.[1] A village miller receives mixed smallholder lots immediately before grinding, when bad kernels become impossible to remove individually. Dry storage prevents some new growth but does not remove toxin already present. Laboratory sampling and toxin assays are still needed to decide whether a lot meets local food limits; a low-cost screening device could reduce some exposure before milling without pretending to certify food.

## Solution

A shielded, four-channel gravity sorter handles **dry, whole maize only** before the mill hopper. A food-contact stainless-steel feed plate and adjustable recycled-HDPE singulation grooves spread kernels into four lanes. A 365 nm UV-A LED illuminates them inside an interlocked enclosure; paired filtered photodiodes per lane measure two visible emission bands, while a low-cost CMOS camera checks reflected-light damage cues. A local microcontroller tracks each kernel to a spring-return reject gate. Ambiguous images, stalled lanes, failed illumination checks, or power loss route grain to the **hold/reject bin**, never the accepted-food bin. A keyed split-bin and retained lot identifier on paper prevent accidentally remilling rejected grain. No internet, individual tracking, or cloud service.

## Key Innovation

Fluorescence sorting itself is **prior art**: Yao and colleagues demonstrated a portable fluorescence-assisted, *manually* sorted maize prototype, with strongly different toxin reductions in two challenged lots (99.3% and 40.7%).[2] This concept tests whether four inexpensive, serviceable lanes with a closed-loop reject-gate check and explicit **uncertain/hold** state can transfer such screening to a continuously fed village-mill workflow. It is not a direct aflatoxin detector: fluorescence is an imperfect fungal proxy with false positives and false negatives.[2] Unlike the repository's Regenerable Grain Guard Cassette, which buffers moisture during storage and explicitly does not remove formed toxin, this sorter acts on whole kernels immediately before grinding.

## Target Cost

**Unvalidated 2038 ex-factory target: US$280 at 10,000 units/year**, comprising optics/LED/filter US$80, camera/control/electronics US$65, four gates/sensors US$55, food-contact frame/shield US$55, assembly/test US$25. Excludes delivery, local taxes, power supply, mill integration, laboratory assays, calibration service, labor, and rejected-grain disposal. Budget **US$20/year** for LED/filter and gate maintenance, subject to supplier quotes; the assumed **five-year** life implies US$56/year capital before finance and maintenance. Shared off-grid 12 V supply or grid power is required. Repairable screws, replaceable LEDs/gates, and recyclable metal/HDPE reduce lifetime cost; segregated electronic waste still needs a licensed recycling route.

## Impact

**Design targets, not measured performance:** ≥20 kg/hour dry maize at ≤15 W operating draw; ≤5% sound-kernel rejection; and ≥50% reduction in total aflatoxin mass per matched lot after sorting, measured by accredited sampling and laboratory analysis. At an assumed 0.3 g/kernel, 20 kg/hour is about 19 kernels/second overall, or five per lane; these are engineering sizing assumptions to test, not established capacity. A 12-month multi-site pilot would blind-test naturally contaminated lots from several varieties and seasons against hand sorting and no sorting, measuring reject mass, throughput, assay uncertainty, false-negative lots, and cost per tonne. **No health benefit or safe-food claim follows from these targets.** If the accepted bin still exceeds local limits, quarantine it; never blend rejected grain into food or animal feed. A 10–20-year path is prototype → independent, lot-level validation → guarded field trials → locally repairable manufacture, contingent on food-safety approval.

## Limits and safety

A clean-looking kernel can contain toxin; mould, dust, UV aging, variety differences, and poorly sampled lots can break optical classification. Fluorescence may flag fungal by-products rather than toxin concentration.[2] Use a sealed UV enclosure with a lid interlock, an operator-visible lamp/gate test using a traceable reference tile and timed reject test at every shift, plus periodic laboratory assays of **both** bins. The tile verifies optics and actuation, **not food safety**. Clear blockages with power isolated; clean food-contact surfaces between lots; prevent dust accumulation and inhalation. Reject or quarantine suspect grain under local food rules, and do not imply that sorting treats other mycotoxins. A pilot fails if it cannot outperform manual sorting on toxin reduction across independent naturally contaminated lots at an affordable total cost, or if false reassurance rises when the device malfunctions.

## How It Works

The advantage is **where** the decision happens: a household's whole kernels are still separable at the mill gate, and the miller can keep the accepted and suspect streams accountable before grinding. This is a proposed risk-reduction workflow, not a toxin assay. The operator assigns a lot ID, weighs and checks that the maize is dry and whole, and records the starting mass; wet, broken, or heavily dusty lots go to hold for separate assessment rather than being forced through an unvalidated classifier.

A metered gravity feed distributes kernels across four recycled-HDPE grooves on the stainless plate. In a light-tight section, 365 nm illumination excites fluorescence measured in two visible bands by paired filtered photodiodes; a CMOS reflected-light image adds a damage cue. The microcontroller compares signals against locally validated reference distributions, tracks travel time to a gate, and allows the accepted path only when sensing and actuation are valid and confidence is sufficient. The fluorescence is a *proxy* for fungal-associated features, not a measurement of aflatoxin concentration.[2] Classification thresholds must be trained and challenged with local varieties and independently assayed lots; until then they are research parameters.

A spring-return gate sends suspect or uncertain kernels to a keyed hold bin. On startup and each shift, an optical reference tile, timed gate test, bin-presence check, and interlock test must pass; a fault closes the accepted path and displays a visible **HOLD—DO NOT MILL** state. The operator weighs and labels both bins, retains the paper lot record, cleans the chute between lots, and obtains representative lot-level toxin testing before claiming any food-limit compliance. Holding rejects protects against their being quietly remilled or sold as cheap food; disposition follows local rules, not an automatic feed-use shortcut.

## Technical Architecture

| Subsystem | Proposed interface and failure behavior |
| --- | --- |
| Intake and singulation | Adjustable four-lane food-contact chute meters dry whole kernels; bridges or double-fed lanes trigger hold rather than an unreliable pass. |
| Optics | Shielded 365 nm LED, emission-band photodiodes, reflected-light camera and reference tile; ambient-light leakage, dirty windows, LED drift or failed interlock inhibit acceptance. |
| Controller and gate | Offline microcontroller time-stamps lane events and drives four spring-return gates; a gate-position or timing mismatch diverts the lot and requires operator reset after inspection. |
| Power and record | Shared 12 V supply with protected low-voltage cutoff; no implied battery in the US$280 factory target. Paper lot ID, input/accepted/hold masses and fault status remain usable without network access. |

At the **20 kg/h design point**, the assumed 0.3 g/kernel gives about **19 kernels/s across four lanes**: the control problem is millisecond-scale gate timing, not simply average throughput. The ≤15 W target includes illumination, sensing, control and gates, but must be measured under peak reject activity; a compressor-based ejector is **not** in this design. A guarded, dust-managed enclosure needs electrical protection, accessible emergency stop and power-isolated servicing before a field pilot.

## Performance Benchmarks

No integrated prototype measurements exist. The published portable, fluorescence-assisted *manual* sorter reported **99.3% and 40.7%** aflatoxin reduction in two challenged lots; those are heterogeneous research outcomes, **not** a validated continuous-sorter baseline or a guaranteed effect here.[2] No like-for-like current state-of-art figure for a four-lane, low-power mill-gate unit is established; the comparison must be run rather than asserted.

| Metric | Proposed target (unmeasured) | Pilot comparison and test |
| --- | --- | --- |
| Throughput and power | ≥20 kg/h at ≤15 W on dry whole maize; ≤0.75 kWh/t at both limits | Weigh timed feeds and meter full-device power across varieties, moisture bands and reject rates; compare with hand sorting on the same lots. |
| Sorting effect | ≥50% less *total aflatoxin mass* in accepted grain versus incoming lot; ≤5% sound-kernel false rejection | Accredited, representative assays of matched input, accepted and hold fractions; report confidence intervals, false-acceptance lots and mass balance, not classifier accuracy alone. |
| Reliability | No accepted-bin discharge on loss of power, sensor self-check, lid interlock or gate feedback | Inject each fault under load, record diverted mass, downtime and cleaning time; require independently witnessed pass/fail. |
| Cost | US$280 ex-factory at 10,000/year in 2038; five-year life plus US$20/year maintenance | Supplier quotations, repair logs and total installed/assay/disposal cost alongside manual sorting; factory cost is not customer price. |

A 50% reduction in **toxin mass** is not automatically a 50% reduction in concentration if grain is rejected. Even a passing pilot lot is not certified safe: representative sampling and a suitable reference assay govern decisions under applicable local standards.[1][2]

## Deployment Scenarios

1. **Village mill, wet harvest:** A miller receives household bags, declines wet grain, sorts qualified dry maize by owner-labelled lot, and pauses milling while a suspect lot is assessed. Households retain a documented claim to their grain, but cannot reclaim held kernels into the food hopper without an authorized disposition.
2. **Smallholder cooperative:** A shared unit runs short scheduled sessions on dry whole maize, with a trained steward performing daily reference and gate tests. The cooperative batches samples for laboratory confirmation and budgets separately for power, maintenance, laboratory testing and managed reject disposal; a faulty unit reverts to hold/manual triage, not a green light.
3. **School-meal procurement point:** An aggregator uses lot mass records to flag material for confirmatory testing before grinding and distribution. Procurement acceptance remains based on representative toxin assays and local requirements, not the sorter screen; no claim is made for fumonisins or other non-validated hazards.

## Risks & Mitigations

- **False reassurance:** Non-fluorescing contaminated kernels, variable varieties and patchy contamination can survive sorting. Validate on naturally contaminated local lots across seasons and assay accepted and hold streams; quarantine a lot that fails the applicable food test. The residual risk cannot be eliminated by a clean-looking screen.[2]
- **Drift and physical failure:** Dust, moisture, double feeds, LED aging, mis-timed gates, bin removal and unstable power can invalidate a pass. Shift-start checks, guarded optics, mass balance and fail-to-hold faults are required; measure false acceptance and downtime under deliberately induced faults.
- **Reject diversion and incentives:** Families may bypass a machine that takes away food; a buyer may dump suspect kernels on a poorer market. Preserve owner-labelled hold custody, fund a locally approved non-food disposal or processing route only after assessment, and audit rejected mass. Never divert suspect grain automatically to animal feed.
- **Operator hazards and affordability:** UV exposure, grain dust, moving gates and shock require interlocks, dust control, electrical protection and isolated maintenance. The low factory-price target omits assays, installation and disposal; a pilot must demonstrate that real service cost and food loss are acceptable without weakening safety gates.

## Vision for 2050

A plausible 2050 outcome is a repairable mill-gate fitting, paired with routine lot sampling and enforceable reject custody, at mills where whole-grain sorting can reduce exposure before milling. Local technicians service the optics and gates; cooperatives can compare audited lot outcomes across harvests without collecting personal data. This is a conditional scenario, **not** a forecast of disease reduction or universal safe maize: adoption depends on independent toxin evidence, affordable testing, owner incentives and a lawful route for held grain.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/mycotoxins — WHO, *Mycotoxins* (2023), health risks and prevention.
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC10058786/ — Yao et al., *Toxins* (2023), portable maize fluorescence sorting and limitations.
