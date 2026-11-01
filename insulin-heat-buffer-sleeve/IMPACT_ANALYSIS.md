# Insulin Heat-Buffer Sleeve — Impact Analysis

**Author: jayis1**

**Scope:** hypothetical capacity and cost scenarios, not observed clinical outcomes. A qualifying trip is one within a future validated envelope *and* the exact insulin product's labeled temperature/time requirements.[1] No prototype has yet met that definition.

## Device-level assumptions

The proposed 0.30 kg paraffin insert at an assumed usable 180 kJ/kg has a modeled 54 kJ energy budget. At a hypothesized whole-sleeve resistance of 8 K/W and 40 °C air versus a 28 °C phase plateau, nominal heat ingress is 1.5 W: 43.2 kJ over eight hours, leaving 10.8 kJ for imperfect insulation and openings. These are arithmetic design inputs, **not measured transport hours**; solar load, seal bridges, incomplete freezing/solidification of the PCM, warmer starting insulin and repeated opening could exhaust the margin. The referenced research paraffin reports a phase-change enthalpy, not an independently verified usable enthalpy for this insert.[2]

## Annual deployment model

The scenarios below are illustrative procurement cohorts, **not estimates of the diabetic population**. They assume each person owns one sleeve, uses it only for short journeys compatible with the product's label, and has access to a cool room to reset it. The qualifying share is an explicit assumption, not a measured effectiveness rate. One trip per qualifying day is counted; multiple trips, vacations and clinic stock are excluded.

| Input / output | Low | Base | High |
| --- | ---: | ---: | ---: |
| Sleeves deployed (assumed users) | 10,000 | 100,000 | 1,000,000 |
| Share with a trip on a modeled day (assumed) | 25% | 50% | 80% |
| Modeled days per user-year (assumed) | 100 | 180 | 240 |
| Share of trips qualifying after label, reset and thermal checks (assumed) | 50% | 70% | 85% |
| Qualifying-trip capacity/year (calculated) | 125,000 | 6,300,000 | 163,200,000 |
| Initial paraffin required, at 0.30 kg/sleeve (calculated) | 3 t | 30 t | 300 t |
| Annualized hardware and insert cost, US$ (calculated) | $200,000 | $2,000,000 | $20,000,000 |
| Hardware/insert cost per modeled qualifying trip, US$ (calculated) | $1.60 | $0.32 | $0.12 |

Formula: qualifying trips/year = deployed sleeves × trip-day share × days/year × qualifying share. Hardware model: US$35 retail sleeve amortized over an **assumed** two years, plus a US$5 insert replacement every two years = US$20 per user-year. Rounded cost/trip = total annualized hardware and insert cost ÷ modeled qualifying trips. The US$35 and US$5 prices are unquoted targets; two-year service life and all adoption and qualification inputs are assumptions. Manufacturing yield, freight, taxes, cleaning, training, failed trips, indicator refills, logistics and pharmaceutical validation are excluded; a single-use indicator on each trip could dominate total cost. These exclusions make the apparent per-trip figures **lower bounds conditional on the model**, not a price offer.

## What is—and is not—counted

A qualified trip is a transport opportunity, **not** a pen saved from spoilage: baseline excursion incidence and the fraction of exposed products that actually fail stability testing are unknown. Avoided insulin waste, expenditure, hyperglycemia and mortality are therefore **not estimated**. Pen counts and monetary savings must wait for controlled product-specific comparisons against ordinary pouches, commercial PCM cases and evaporative wallets. The sleeve does not increase insulin supply or solve prolonged power loss; it is not a substitute for unopened-product refrigeration where the label requires it.[1]

An initial one-million-unit build would embed approximately 300 tonnes of paraffin before packaging and replacements (calculated). The aluminum, polypropylene, textiles and indicator refills add unquantified embodied energy and waste. A lifecycle comparison must measure manufacturing mass, return/reuse rates, replacement frequency and end-of-life disposal against the alternatives, rather than presuming an environmental win.

## Sensitivity and falsification

At fixed deployment, modeled trip capacity changes in direct proportion to each assumed rate. If the base cohort's qualifying share is only 35% instead of 70%, capacity halves; if no cool-room reset is possible, repeat-journey capacity can be zero. Repeated chamber failures, container temperatures outside a product's label, nonrecovering inserts, false-negative indicators, adverse stability assays, or a cheaper comparator with equal label-compliant performance would falsify the claimed transport advantage. Collect paired logger traces, lot-level durability, product-specific stability data and real invoices before revising these projections.

## Sources

[1] https://www.fda.gov/drugs/emergency-preparedness-drugs/information-regarding-insulin-storage-and-switching-between-products-emergency
[2] https://doi.org/10.1063/5.0197739
