# ORS Mix-Witness Cup

**Author: jayis1**

**Category:** Child Health & Universal Basic Services / Oral Rehydration Preparation

**Status:** Concept (TRL 2; unvalidated; not a clinical clearance device)

## Problem

WHO reports nearly 1.7 billion childhood diarrhoeal episodes annually and about 443,832 deaths among children under five. Oral rehydration solution (ORS) made with clean water is an essential treatment, alongside appropriate feeding, zinc and clinical referral when indicated.[1] A sachet labeled for one litre must not be mixed with an arbitrary water volume: dilution changes both glucose and electrolyte concentrations. A visual fill line alone cannot establish that the right packet was used, fully dissolved, or mixed with safe water. A verifier must not delay rehydration or give false assurance that water is potable.

## Solution

A washable, opaque, one-litre mixing vessel has a broad, high-contrast fill mark and tactile fill stop for people with low vision. A detachable, offline test cup takes a **small sample** after the caregiver mixes a *recognized, unflavoured, one-litre reduced-osmolarity ORS packet* into previously purified or boiled-and-cooled water according to its label.[2] A two-channel reader compares temperature-corrected electrical conductivity (ionic content) and an optical refractive-index proxy (total dissolved solutes) with locally validated ranges for that exact packet formulation and the source water. It displays only **CHECK AGAIN** or **CONSISTENT WITH THE REFERENCE MIX** in text, shape and sound; it never displays “safe to drink.” The measured sample is discarded, not returned to the vessel. A permanently marked packet-type selector and a sealed reference check prevent an unknown formulation from receiving a pass.

This is a preparation-error screen for supervised community settings, not a replacement for the packet instructions, clean water, a clinician, or an ORS supply. If the reader is unavailable, expired, dirty, gives an invalid result, or cannot identify the packet, caregivers follow standard labeled ORS preparation and seek appropriate care **without waiting for the device**. Severe dehydration, inability to drink, persistent diarrhoea or blood in stool requires urgent professional assessment under local guidance.[1]

## Key Innovation

The proposed research contribution is **formulation-specific, two-observable mixing verification with explicit abstention**, coupled to a measured-volume vessel: a conductivity measurement responds mainly to dissolved ions while refractive index responds to the combined solute load. Together they may catch gross volume, omitted-sachet and incomplete-mixing errors that a fill line misses. Neither observable uniquely identifies sodium, potassium or glucose; similar mixtures can produce the same pair of readings. Conductivity meters, refractometers and mixing cups already exist. No claim of new sensing physics or clinical accuracy is made.

Prototype: food-contact polypropylene vessel; replaceable silicone seal and stainless fill-stop pin; reusable gold-plated interdigitated electrodes behind an inert guard; molded cyclic-olefin optical window, LED and photodiode to estimate a critical-angle shift; thermistor; low-power microcontroller; two replaceable AAA cells. The test cup's 2 mL sample channel is removable for washing, and a physical reference insert checks the optical path and electrode response at each session. The reader cannot authenticate a packet or verify microbial or chemical water safety. Any fouling, unusual source-water mineral content, flavoring, packet variation, temperature out of range, or failed reference forces an **invalid/uncertain** result rather than a pass.

## Target Cost

**Unvalidated 2038 design target, not a quote:** US$24 ex-factory at 100,000 units/year: US$5 molded vessel and seal, US$4 sampling cup and electrodes, US$6 optical/electronic parts, US$3 enclosure/cells, US$6 assembly, calibration and scrap. Target a five-year reusable life and a US$3 replaceable cup/window assembly; batteries, clean water, ORS, staff time, distribution, validation and regulatory approval are excluded. A fully passive graduated vessel remains usable if electronics fail. Repairable screws, removable cells and separately recyclable polymer/electronic modules avoid treating the entire vessel as a disposable sensor. Price and durability must be measured, not assumed.

## Impact

A planning scenario of 10,000 readers used for 200 preparations per year would yield **up to 2 million screening attempts/year**, not 2 million children treated or any demonstrated deaths prevented. Run blinded bench challenges across packet brands, water mineralization, temperature, incomplete dissolution, half/double concentration and plausible counterfeit mixtures; measure false passes and false rejects against laboratory electrolyte/glucose/osmolality assays. A supervised field study must compare preparation errors, delay to first ORS dose, ability to understand the ambiguous result, and actual referrals against a labeled one-litre container alone. Any increase in treatment delay, false reassurance or unacceptably high false-pass rate defeats the concept. The device should never make ORS access contingent on owning it.

## Operating boundaries and development

UNICEF lists a reduced-osmolarity one-litre sachet containing 13.5 g glucose, 2.6 g sodium chloride, 2.9 g trisodium citrate dihydrate and 1.5 g potassium chloride, to be diluted in 1,000 mL purified or boiled-and-cooled water; the specified solution contains 75 mmol/L sodium and 75 mmol/L glucose with 245 mOsm/L osmolarity.[2] Those values describe **one product**, not a universal formulation or the accuracy of this concept. Calibration bands must be derived from manufactured lots and independently measured samples, not hard-coded from a nominal formula. A predeployment gate should demonstrate detection of at least 90% of deliberately prepared half- and double-strength mixes at a predefined maximum false-pass rate of 1% on the challenge set; these are hypotheses, not achieved performance. Real-world clinical benefit requires separate ethical review and trials. A 10–20-year development path is plausible only if the device improves on simply supplying a correctly marked mixing container and clear instructions.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/diarrhoeal-disease
[2] https://supply.unicef.org/s1561133.html
