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

## How It Works

The novelty is not a new compressor: it is a **physical identity gate and weighed chain of custody** wrapped around established recovery hardware. At an eligible service visit, a qualified technician checks the appliance label, cylinder pressure rating and remaining fill allowance, records the cylinder tare, and samples the charge through a sealed loop. A declared refrigerant that the analyzer cannot corroborate is quarantined for a separately approved collection path; the cart cannot certify a mixture by sensing alone. For a compatible charge, short low-loss hoses feed a rated recovery module. Its compressor raises vapor pressure so the discharge can condense in the receiving cylinder as heat leaves the system; an oil separator and replaceable drier protect the path but do not turn recovered gas into reclaimed product. The operator follows the equipment's applicable evacuation endpoint, isolates the valves, weighs the sealed cylinder and accounts for line holdup. A signed paper/offline receipt follows that cylinder to a reclaimer, whose independent analysis decides whether gas can be purified to specification or needs another lawful disposition.[1][2][5]

## Technical Architecture

The material path is **appliance → low-loss manifold → sealed sample/identity gate → certified recovery module → oil separation/drier → rated cylinder**. The information path is **appliance label + analyzer result + two scale readings + cylinder ID → job receipt → reclaimer acceptance record**. A mechanical valve arrangement should prevent an unknown-gas path from entering the clean cylinder; bench testing must demonstrate that an operator cannot defeat it inadvertently. The scale interlock checks cylinder mass against its marked safe fill limit, independently of a technician's visual check; relief hardware remains part of the certified pressure design. The chassis carries replaceable steel tubing, serviceable seals and isolated waste-oil containers rather than a proprietary refrigeration cycle. Gas composition, oil carryover, moisture, acidity and noncondensables require downstream laboratory testing; AHRI 700 is a product specification, not an onboard analyzer badge.[5]

## Performance Benchmarks

**No prototype measurements exist.** The comparator is a maintained, certified conventional recovery kit used on the *same refrigerant, charge, cylinder, ambient temperature and evacuation endpoint*. AHRI 740 defines standardized ratings for recovery speed, final vacuum, refrigerant loss and trapped refrigerant; manufacturer ratings under those conditions must be obtained before a numeric state-of-art comparison is defensible.[4] The cart's proposed advantages are workflow outcomes, not an invented pump-speed advantage.

| Metric (eligible nonflammable small-appliance trial) | Current conventional-kit baseline | Microcart design target, unverified |
| --- | --- | --- |
| Initially present charge captured | Measure gravimetrically in matched tests | ≥95% where compatible with stricter applicable evacuation rules |
| Connection/transfer/disconnection loss, 1 kg bench charge | Measure with calibrated mass balance | ≤10 g |
| Extra mass accepted by reclaimer per job | Measure matched conventional-kit deliveries | +0.1 kg per eligible job as a *trial hypothesis*, not an expected result |
| Recovery time and electricity | Record min/job and kWh/kg on same refrigerant | No worse than matched kit; quantify before marketing |
| Identity errors / misrouted cylinders | Audit baseline receipts and lab samples | Zero known misroutes in a pilot; report sample size and confidence interval |

Record pressure, initial charge, refrigerant type, ambient temperature, cylinder tare/gross readings, residual charge, line holdup and scale uncertainty for every trial. A passing capture percentage alone does not establish regulatory compliance or AHRI 700 purity.[1][4][5]

## Deployment Scenarios

- **Small licensed repair shop:** one configured kit serves a specific eligible refrigerant family, with a cylinder exchange partner collecting sealed, labeled loads. At 50 one-kilogram jobs/year, the existing US$17/kg hardware-and-service planning allocation excludes labor and reclaimer fees; shops need a service fee or deposit scheme, not presumed resale profit.
- **Municipal appliance take-back site:** trained staff batch end-of-life units by declared refrigerant; uncertain or incompatible appliances wait for a qualified specialist with approved equipment. The city pays for audited collection and waste handling, not for a speculative carbon-credit receipt.
- **Cold-chain service cooperative:** a shared cart and pooled cylinder logistics reduce equipment duplication across smaller operators. Dispatch is limited by the certified module's refrigerant envelope and the availability of a reclaimer willing to accept the segregated material.

## Risks & Mitigations

| Failure signal | Required safe response / validation gate |
| --- | --- |
| Analyzer disagreement or unknown gas | Keep clean cylinder closed; label and quarantine, then use an approved compatible collection route after technician assessment. Audit identity against laboratory samples. |
| Rising cylinder mass/pressure or failed scale | Stop transfer, isolate valves and verify with independent calibrated weighing; pressure relief follows certified design, never a routine purge. Test full-cylinder and sensor-fault behavior. |
| Leak, power loss or loss of cooling | Stop machine, isolate as the certified design permits and ventilate; inspect before restart. Test transfer interruption and measure retained hose mass. |
| Oil/acid contamination or rejected shipment | Seal and track spent oil/media as regulated waste; segregate rejected cylinders and get the reclaimer's disposition record. No field purity claims. |
| Flammable, toxic or high-pressure refrigerant arrives | Decline this initial kit configuration; route to separately qualified people and equipment. This concept does not extend its certification envelope by adding a warning sticker. |

## Vision for 2050

If independent trials establish a real increment over ordinary certified kits, small service shops could make the custody receipt as routine as the service invoice. Regional cylinder exchanges would route identifiable gas to qualified reclaimers, and rejected mixtures to lawful processing, with each handoff weighed instead of assumed. Wider use is conditional on certification, affordable offtake and technicians being paid for the extra time; the 2050 ambition is verifiable end-of-life refrigerant handling, not a claim that every collected kilogram would otherwise have escaped.

## Sources

[1] https://www.epa.gov/section608/refrigerant-recovery-and-recycling-equipment-certification
[2] https://www.epa.gov/section608/stationary-refrigeration-service-practice-requirements
[3] https://doi.org/10.59117/20.500.11822/44243
[4] https://www.ahrinet.org/system/files/2023-06/AHRI_Standard_740-2016_1.pdf
[5] https://www.ahrinet.org/system/files/2025-03/AHRI%20Standard%20700-2024%20SI_0.pdf
