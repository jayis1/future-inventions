# Refrigerant Reclamation Microcart

**Author: jayis1**

**Status: concept (TRL 2); not certified equipment**

## Problem

Cooling protects food, medicines and people, but refrigerant lost during servicing and disposal adds avoidable climate and, for some older chemicals, ozone harm. The scale is planetary: UNEP's *Global Cooling Watch* estimates direct refrigerant releases are a substantial part of cooling's greenhouse-gas footprint.[3] Small repair businesses need a practical way to recover a charge without mixing unknown gases or losing track of the cylinder between a service visit and a certified reclaimer. This is a workflow and access problem, not a claim that recovery machines do not exist. US EPA already requires certified recovery equipment and prescribed recovery practices for covered stationary appliances.[1][2]

## Solution

A hand-cart for **trained refrigerant technicians**, limited initially to a *single certified, nonflammable, conventional-pressure refrigerant family per configured kit*. It carries a certified recovery machine, short low-loss hoses, a dry-break sample loop, a compatible rated recovery cylinder on a calibrated scale, pressure/temperature sensing, an oil separator and a sealed replaceable filter-drier. A handheld refrigerant analyzer checks a small closed-loop sample **before** the cylinder valve is opened; an uncertain identity sends the whole charge to a separately labeled mixed/unknown-refrigerant cylinder using a compatible approved recovery setup, never to the clean stream. The compressor moves vapor from the isolated appliance to the cylinder; cooling/condensation and pressure differential permit capture. A paper or offline-only receipt records appliance ID, declared refrigerant, cylinder tare and gross masses, analyzer confidence, service date, destination and responsible technician. No network, location tracking or owner registry is required.

**Design goals, not measured performance:** fit in a serviceable ~0.7 × 0.5 m footprint; capture at least 95% of the *initially present* charge in controlled small-appliance tests where a working compressor and the applicable rules permit, while always meeting the jurisdiction's more specific evacuation requirement; lose at most 10 g per eligible 1 kg bench charge across connection, transfer and disconnection. These goals must be assessed with calibrated gravimetry and retained-line measurements, not inferred from cylinder mass alone. The regulatory threshold depends on the appliance and recovery method, so 95% is not a universal compliance criterion.[1][2]

## Key Innovation

The proposed advance is a **technician-scale, identity-gated recovery and custody workflow**: closed-loop sample, physical cylinder segregation, before/after weighed inventory and a return-to-reclaimer receipt share one service procedure. Existing recovery machines, analyzers, scales and driers are prior art; the hypothesis is that making their handoffs difficult to skip will increase *verified incremental capture* at small shops. It must be tested against a well-maintained conventional recovery kit, not against venting.

**Differs from [Thermoacoustic Metamaterial Heat Pump](../thermoacoustic-metamaterial-heat-pump/):** that concept replaces the refrigerant-based cooling cycle; this cart handles refrigerant already installed in legacy equipment. It does not claim to manufacture a refrigerant-free heat pump or reclaim gas to saleable purity on site.

## Target Cost

**Unquoted planning goal for 2038 at 10,000 units/year:** US$3,000 ex-factory for the cart, excluding cylinder deposit, refrigerant analyzer calibration, certification, freight, taxes, permits and technician training. Illustrative allocation (US$): certified recovery module 900, compatible analyzer 550, cylinder and calibrated scale 300, guarded sample path 220, oil/drier module 180, hoses/valves/pressure relief 350, chassis/assembly/testing 500; total US$3,000. These are budget assumptions, **not supplier quotations** or evidence that a certified integrated unit can be sold at this price. Budget an additional unverified US$250/year for calibration, driers, seals and service, plus cylinder exchange and reclaimer fees. At 50 eligible jobs/year with 1 kg recovered/job, five-year straight-line hardware allocation plus annual service is US$17/kg before labor, electricity, financing and off-site processing; actual economics depend strongly on utilization and local cylinder logistics.

## Impact

A planning deployment of 10,000 carts performing 50 eligible jobs/year at 1 kg recovered/job would collect up to **500 tonnes/year** of refrigerant. If a matched trial shows **0.1 kg/job** more delivered to a verified reclaimer than with maintained conventional equipment, the incremental, non-double-counted outcome would be **50 tonnes/year**, not 500 tonnes of newly avoided emissions. Neither improvement nor avoided atmospheric release has been demonstrated; measure reclaimer-accepted net mass, vent/line loss and stock changes before assigning any climate benefit. No CO₂-equivalent benefit is claimed without the measured refrigerant mix and a defensible counterfactual.

## Safety, limits and validation

- **Not a DIY appliance.** Only licensed/certified technicians where required; use certified recovery equipment and follow manufacturer directions and local law. US Section 608 rules require off-site certified reclamation when recovered refrigerant changes ownership; field drying is not certified reclamation or an AHRI 700 purity test.[1][2]
- **Exclude initially:** A2L/A3 flammable blends, ammonia, high-pressure CO₂, unidentified cylinders with incompatible pressure ratings, and equipment outside the certified recovery module's envelope. Do not silently treat an analyzer's uncertain result as safe; a qualified technician must choose a compatible segregated collection route. No intentional venting, mixing, on-site resale, or automatic purge of noncondensables.
- **Fail safely:** pressure relief installed and discharged as required by the certified design and local rules (emergency relief may release refrigerant); rated hoses and cylinder, grounded electrical fittings, ventilated work area, independent scale-based fill cutoff with operator verification, manual isolation on power loss. Never defeat cylinder fill limits or run a cylinder beyond its rated conditions. Any relief or overpressure incident is reportable and requires inspection, not an ordinary operating mode.
- **Prove or reject the hypothesis:** compare matched service visits with a certified conventional kit; weigh sealed cylinders before/after on calibrated scales, independently measure residual appliance charge and hose holdup, and log actual recovery time and kWh/kg. Audit reclaimer acceptance and rejected/contaminated loads, identity errors and cylinder-misrouting rates; test deliberate sensor failure, power loss and full-cylinder conditions. A design is not deployable until a competent testing body certifies the integrated configuration for the intended refrigerants and technicians validate it in the relevant jurisdiction. Within 10–20 years, progress from bench mass-balance trials to safety certification and independent small-shop field trials; repair the cart and return spent media/oil through regulated waste channels.

## Sources

[1] https://www.epa.gov/section608/refrigerant-recovery-and-recycling-equipment-certification
[2] https://www.epa.gov/section608/stationary-refrigeration-service-practice-requirements
[3] https://doi.org/10.59117/20.500.11822/44243
