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

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/mycotoxins — WHO, *Mycotoxins* (2023), health risks and prevention.
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC10058786/ — Yao et al., *Toxins* (2023), portable maize fluorescence sorting and limitations.
