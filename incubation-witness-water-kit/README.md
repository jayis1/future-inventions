# Incubation-Witness Water Kit

**Author: jayis1**
**Status: research concept; not a drinking-water clearance or a certified laboratory method**

## Problem

WHO and UNICEF report that 2.1 billion people lack safely managed drinking water; this is not a count of people whose water this device could test or make safe.[2] A stored-water container or small community supply can be contaminated after collection. A delayed or improperly incubated *E. coli* culture may appear negative even when its assay conditions were invalid. Water testing needs an explicit **invalid** result rather than false reassurance, alongside source protection and treatment.

## Solution

A reusable, repairable, offline single-sample incubator holds a **sealed sterile 100 mL vessel** with a commercially validated, unit-dose enzyme-substrate assay. A trained operator collects a representative sample using the assay manufacturer's and local authority's sampling instructions, including an appropriate pre-dosed dechlorination vessel for chlorinated water. As a reference implementation, Colilert-18 uses ONPG for total coliform colour and MUG for *E. coli* fluorescence, incubated at **35 ± 0.5 °C for 18 hours**; colourless means no detected target, yellow indicates total coliforms, and yellow plus blue fluorescence under a guarded 365 nm lamp indicates *E. coli* under that method's reading criteria.[1] The prototype must use the **unchanged approved reagent and its instructions** rather than claiming that a repackaged pouch or altered medium retains approval.

A recycled-aluminium heat spreader, insulated recycled-polypropylene shell, low-voltage resistive heater, fan, two replaceable calibrated thermistors (one in an adjacent water-filled 100 mL surrogate vessel), and controller record temperature and time locally. A latching **INVALID—DO NOT INTERPRET** indicator trips on power interruption, missing sensor, out-of-envelope time/temperature, failed reference check or opened incubator. It stays latched until a new run; it cannot erase a positive culture. A keyed opaque viewing hood and interlocked UV source permit trained users to read sealed vessels without opening them. No camera, cloud, household identity or automated declaration that water is safe.

## Key Innovation

**The assay and incubator are established art.** The proposed, testable contribution is a *sample-adjacent thermal-history witness* electronically interlocked with the reading station: a culture cannot be presented as a valid negative if its surrogate and chamber record disagree or the session is incomplete. This contrasts with this repository's flood-isolating wellhead collar, which limits cap-path ingress but explicitly still requires independent water sampling; its arsenic and fluoride projects treat chemical hazards, not microbial test validity. This design does **not** improve the chemistry's intrinsic specificity, representativeness or limit of detection. Its benefit must be demonstrated against an ordinary incubator with the same assay, not inferred from the indicator alone.

## Target Cost

**Unquoted 2038 design target:** US$160 ex-workshop for one reusable incubator at 10,000/year: US$38 insulated shell/spreader, US$28 heater/fan, US$38 controller/sensors/memory, US$24 shielded lamp/interlock/indicator, US$32 assembly and test. Excludes 12 V supply or battery, sterile vessels and commercial assay reagent, control cultures, trained labour, calibration, shipping, taxes, confirmation, and regulated disposal. A **target** five-year life, annual calibration and replaceable heater/sensors must be checked in field trials; no per-test price is claimed because commercial reagent and quality-control prices vary. At a provisional 10 W average for 18 h, electricity would be 0.18 kWh/test; energy, warm-up and backup sizing are unmeasured design assumptions. A 12 V/30 Ah LiFePO4 pack (nominal 360 Wh) is an optional separately priced buffer, not a guarantee of an uninterrupted run. Recycle aluminium/PP and send electronics and failed cells to local e-waste collection; treat all incubated samples as potentially infectious.

## Impact

**Unvalidated target:** in a blinded 300-run laboratory challenge across power, sensor, timing and temperature faults, detect every deliberately injected incubation-invalid run before an operator can log a negative; record false-invalid rate and independent thermometry, and do not claim zero real-world failures from that sample. In a later supervised pilot at 20 small-supply sites, compare invalid/misread rates, operator time and total cost against a standard controlled incubator using the *same* commercial assay and representative sampling protocol. A valid negative means only **no detected *E. coli* in that tested 100 mL under that method**; it neither certifies all water nor excludes viruses, protozoa, chemical contaminants, intermittent pollution or sampling errors. A positive, doubtful or invalid result prompts immediate locally approved protective action and confirmation; the kit does not purify water. A 10–20-year route is benchtop fault injection, independent comparison with an accredited laboratory, jurisdiction-specific approval and service training, then restricted deployment if performance and total cost justify it. No avoided illness or population reached is estimated before field validation.

## Safety and validation gates

- **Controls and calibration:** Run reagent-lot positive and negative controls under qualified laboratory supervision; compare with a certified laboratory method over low-count, turbid, coloured and chlorinated samples. Challenge near single-organism levels with enough replicates to quantify false negatives and sampling variability; culture-negative controls must not be counted as proof that a source is safe. Follow manufacturer-specific storage, reading window and sample holding-time requirements; test reagent aging and humidity exposure rather than assuming shelf stability in local conditions.[1][3]
- **Invalid state:** Independently measure both sample-surrogate and chamber temperatures over warm-up and 18-hour incubation; inject brownouts, open lids, disconnected probes, drift, fan seizure, missing vessel, early/late reads and full memory. Any missing history is invalid, not negative. The indicator's latch and UV shield need independent electrical and photobiological safety review. The surrogate cannot measure every real sample's temperature: qualify the thermal mapping at different fill levels and ambient conditions before any claim.
- **Biological containment:** Never reopen a cultured vessel in a household. Train staff in spill response, keep inoculated materials sealed, and use a locally approved disinfection and disposal route; never dump cultured liquid into drinking-water storage. Do not distribute live positive-control cultures to untrained users.
- **Accessibility:** Use high-contrast text plus a tactile invalid flag; colour and fluorescence interpretation requires a trained reader and reference comparators under the assay instructions. Provide local-language guidance and an affordable confirmation/referral route. Where reliable power, reagents, qualified staff or disposal are absent, this concept is not ready to deploy.

## Sources

[1] https://www.idexx.com/en/water/water-products-services/colilert-18
[2] https://www.who.int/news/item/26-08-2025-1-in-4-people-globally-still-lack-access-to-safe-drinking-water---who--unicef
[3] https://www.epa.gov/system/files/documents/2024-02/rtcr-methods-table.pdf
