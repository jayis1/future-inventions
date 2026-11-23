# Solar-Desiccant Paddy Dryer

**Author: jayis1. Status: research concept; no food-safety or performance certification.**

## Problem

Wet paddy deteriorates rapidly if drying is delayed. IRRI recommends drying soon after harvest, ideally within 24 hours, and reaching at most 14% moisture (wet basis) for storage lasting weeks to a few months.[1] Open-air drying is exposed to rain; existing solar bubble dryers protect grain but can stop drying at night or in humid rain.[2] A cooperative that handles many small harvests needs a measured, repairable way to continue drying during a short humid interval—not a promise to rescue already spoiled grain.

## Solution

A **100 kg batch** of cleaned paddy at **18% initial moisture, wet basis** enters a shallow, perforated, food-contact stainless-steel tray. A guarded 24 V blower passes air through a removable **18 kg zeolite drying-bead bed**, then across the grain and to an outdoor exhaust. The beads and any bead dust never touch the grain: two inspected particle barriers separate them from the process air. Alternate between two bead beds so one can dry grain while the other regenerates in a physically separate, insulated **150–180 °C solar-thermal dock** with an outdoor vapor exhaust. A 5 m² concentrating or evacuated-tube collector, temperature-limited heat transfer circuit, and shared dock are *design options*, not established field performance. An operator uses a calibrated grain-moisture meter and recorded bed mass, outlet humidity, and temperatures to decide whether to continue, switch beds, or reject a batch. A weatherproof cover and cool-down sleeve protect isolated beds; the dryer does not depend on connectivity.

The dock must **not** exhaust into the food airflow. If its measured regeneration endpoint is not reached in cloudy weather, a metered clean-heat backup at the shared cooperative is required or the unit stops accepting wet grain. A filled dryer is not safe indefinite storage: hand off delayed batches promptly to a qualified dryer, or reject them under local food-safety rules. Do not claim that desiccation removes pre-existing mycotoxins.

## Key Innovation

Solar dryers and zeolite grain drying already exist.[2][3] This research concept combines a **mass-accounted, alternating sorbent service loop** with a grain-side humidity and moisture acceptance gate: it targets the hours when a conventional solar bubble dryer pauses in high humidity, while logging the *actual regeneration heat* rather than calling adsorption free energy. It is distinct from this repository's `regenerable-grain-guard-cassette`: that device buffers tens of grams of vapor around **already dried grain in sealed storage**; this one moves kilograms of water out of a **fresh harvest through forced airflow**, with a much larger bead inventory and regeneration heat load. The unproven advance is economical, repeatable, low-temperature field regeneration and uniform grain drying—not the existence of zeolite or sunlight.

## Engineering targets and falsification

All figures are **unvalidated targets** for a specific 100 kg batch, 18% → 14% wet-basis, at 25–35 °C ambient air and up to 85% RH. They do not apply to a 24–26% harvest without resizing and additional cycles. Dry solids are 82 kg; final mass at 14% is 82/0.86 = **95.35 kg**; required water removal is **4.65 kg**. At an assumed **0.30 kg usable uptake/kg bead** under the actual operating RH, 18 kg beads nominally hold 5.4 kg, leaving only 0.75 kg margin. Measure breakthrough and replace a bed before humidity rises; the laboratory's higher bead uptake cannot be silently assumed in a dirty field unit.[3]

- **Batch target:** ≤14% wet-basis grain moisture at multiple tray positions within 24 hours of harvest; test 18% starting moisture and compare against both an IRRI-style solar bubble dryer and a maintained heated-air dryer. Moisture readings and sample mass must agree within calibrated measurement uncertainty; reject persistent wet pockets. Seed batches need separate germination and temperature validation.
- **Air and heat target:** ~100 m³/h through the grain for up to 12 active hours with a serviceable ~20 W blower (about 0.24 kWh electricity). A measured 4 g/m³ mean increase in exhaust absolute humidity across 1,200 m³ would carry 4.8 kg water; this is an **assumption to test**, not a predicted drying rate. Keep measured grain temperature ≤42 °C; cut heat and isolate the grain if the limit or filter pressure-drop limit trips.
- **Regeneration budget:** published small-sample bead tests estimate about **4.86 MJ per kg water removed** in their particular setup, implying ~22.6 MJ for 4.65 kg *before* full-dock heat losses.[3] A planning envelope of 30–36 MJ per complete bed reset is a **target requiring calorimetry**, not a guaranteed upper bound. Five square meters receiving 5 kWh/m²/day at a hypothetical 40% delivered-heat efficiency yields 10 kWh (36 MJ) on a suitably sunny day; either lower irradiance, lower efficiency at 150–180 °C, fouling, or a second wet batch breaks the solar-only budget. Solar heat is collected during the day and stored in a regenerated bead bed, not conjured at night. A separate 24 V supply or battery must be included for the blower.
- **Failure criterion:** if paired trials do not beat the maintained solar bubble dryer in humid-hour water removal *and* cost per tonne of safely dried paddy, retire the concept. Measure inlet/exhaust humidity, air volume, grain-moisture distribution, bead mass and capacity over 100 cycles, measured thermal/electric input, head-rice yield, and mold/mycotoxins; do not infer food safety from an RH sensor alone.

## Target Cost

**Unquoted 2038 ex-workshop goal at 10,000 cooperative units/year: US$1,900** for two 18 kg bead beds, trays and enclosed ducts (US$650); collector, insulated guarded dock and heat circuit (US$800); fan, 24 V controls, filters and sensors (US$450). This is a modeled bill of materials, not a market price or a claim of superiority. Add installation, 24 V power/battery, calibrated grain meter, laboratory toxin tests, clean backup heat, shelter, land, finance, and operator labor. Budget **US$80/year** for filter, seal, fan, and bead-attrition inspection/replacement as a preliminary maintenance allowance, plus metered backup fuel or electricity. At 100 batches/year, bare equipment amortized over ten years is US$1.90 per 100 kg batch *before* finance and operating expense; compare full costs with a solar bubble dryer, which IRRI already describes as a 0.5–1 tonne machine.[2] A cooperative with insufficient throughput should not buy it.

## Impact

For a pilot cooperative processing 100 qualifying batches/year, this design handles **10 tonnes of wet paddy per year**, not 10 tonnes of avoided loss. A matched two-season trial across humid and sunny days should report the fraction of accepted batches actually reaching 14% on time, marketable yield, drying cost, and mycotoxin rejection against existing dryers. Food saved and emissions avoided remain unknown until independently measured against those comparators; collector manufacture, backup heat, bead replacement, and land use belong in lifecycle accounting. A 10–20 year development horizon allows prototype energy balance, independent food-contact and dust testing, cooperative field trials, repair training, and local approvals. Stainless trays and metal ducts are repairable/recyclable; contain and reclaim degraded beads and dispose of contaminated filters according to local rules. No military, surveillance, or coercive use is needed.

## Sources

[1] http://www.knowledgebank.irri.org/step-by-step-production/postharvest/drying — IRRI drying guidance
[2] http://www.knowledgebank.irri.org/step-by-step-production/postharvest/drying/mechanical-drying-systems/the-solar-bubble-dryer — IRRI Solar Bubble Dryer
[3] https://pmc.ncbi.nlm.nih.gov/articles/PMC11391545 — Zeolite bead regeneration study
