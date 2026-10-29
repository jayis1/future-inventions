# Sealed Pit-Emptying Shuttle — Research Specification

**Author: jayis1. All values are design targets, not measured performance or safety certification.**

## Operating envelope and material choices

- Intended feed: relatively liquid domestic pit sludge only, after site assessment; no pit entry. No assumed universal solids threshold: characterize rheology, trash size and gas atmosphere in pilot before publishing one. Refer thick or obstructed pits to equipped services.
- 50 mm bore smooth-wall replaceable hose, nominal 1.5 m static lift, guarded intake; do not insert a person or hands into the pit. Target 10 L/min with water-like test fluid; wet sludge performance is unknown.
- 20 L mechanically vacuum-rated, gasketed polypropylene vessel, marked maximum **16 L** usable fill; inspect for collapse, swelling and cracks. Vacuum pump limited by relief valve to at most 40 kPa below ambient (design target; engineering pressure certification required). A normally closed inlet valve, two independently closed dry-break ends, a mechanical float shutoff and hydrophobic pump-inlet barrier are distinct protections. Verify failure of either barrier separately.
- 24 V replaceable battery and 100 W-rated diaphragm air pump, separately guarded moving/electrical parts. Mechanical gauge needs no power. Never assume the air-exhaust barrier makes harmful gas or aerosols safe; test exhaust and choose site-specific ventilation and PPE. Do not operate in explosive or oxygen-deficient atmospheres.
- Wheeled steel or aluminum frame with removable washable guard; locally replaceable standardized hose, gasket and valve dimensions. Rated container mass is potentially more than 16 kg plus vessel mass: use a two-worker handling procedure and test ergonomic loads. Do not lift the vessel by the hose.

## Budget and physical limits

At 10 L/min, 200 L takes at least 20 minutes of net pumping and thirteen 16 L fills. A 1.5 m static lift of water is about 15 kPa of pressure head; the remaining part of a 40 kPa vacuum budget must cover hose, inlet and fluid losses. The nominal air displacement work at 40 kPa and 10 L/min is 6.7 W; a rough 30%-efficiency input estimate is 22 W. Real air leakage, viscous sludge, battery voltage sag and pump curves may prevent target flow. At a conservative 100 W electrical draw for 20 minutes of net pumping, energy is 33 Wh before swap/idle time; battery sizing requires instrumented trials and a reserve. Never use these estimates to infer worker productivity.

## Containment workflow

1. Obtain site and receiving-facility approval; check gas, pit access, structural integrity, PPE and a safe vehicle route. Establish a spill kit and exclusion zone.
2. Connect the closed vessel; inspect joints and valve position. Confirm float, vacuum gauge and barrier by a documented pre-use check before immersion.
3. Position guarded hose from the surface; open inlet only after containment check. Track vacuum and fill mass. Close inlet before the 16 L fill mark or at any anomaly.
4. Isolate power, close both dry-break ends, wipe/disinfect the outside by the approved protocol and secure the sealed vessel upright for transport. Never open it at a household to decant into an unsealed bucket.
5. A trained receiving worker connects to a compatible sealed receiving port at the authorized treatment facility. Reconcile received mass and container IDs (non-personal batch identifiers only); wash and inspect before reuse. The invention neither sanitizes nor certifies the contents.

## Bench and field validation gates

| Test | Proposed acceptance gate (not yet achieved) |
| --- | --- |
| Inlet, float or barrier single-fault challenge | With each fault imposed separately, containment remains closed or operation stops before liquid enters pump/exhaust; any escape is a design failure. |
| 100 wet connect/disconnect cycles | No visible external leak and quantified swab/contact mass no worse than a maintained sealed-container comparator. |
| 1.5 m lift on water-like simulant | ≥10 L/min at ≤100 W electrical; record full pressure-flow curves and energy per liter. |
| Diverse realistic sludge/trash pilot | Predefine eligibility; record fraction of jobs refused, clog frequency, safe clearing time and transfer volume rather than extrapolating from clean water. |
| Worker and public safety | Independent hygiene sampling, spill weighing, gas exposure assessment and ergonomic testing; no claim of safety from a leak-free bench test alone. |
| 100 eligible paired field jobs | Compare with maintained Gulper plus covered receiving vessel and available vacuum service; evaluate full-chain exposure, costs, accepted treatment mass and refused jobs. Independent ethics and worker input required. |

Reject the concept if a single float/barrier failure can release sludge to exhaust, if blocked inlet requires hand-clearing contaminated matter, if field spill/contact is no better than established practice, if receiving sites will not accept sealed vessels, or if service cost and burden make adoption impractical. Retire damaged pressure vessels; reclaim metal and clean polymer only after approved decontamination, and treat contaminated seals/barriers as regulated locally. No open biological release, worker tracking or autonomous disposal.

## Relationship to existing art

Gulper-type manual pumps and mechanized trash exclusion address extraction; vacuum carts and sealed tanks address transport. This proposal tests whether a narrow-access, swapped-vessel connection and explicit failure gate make the **whole transfer chain** safer. No component is represented as newly discovered; the comparison must establish whether integration provides any net benefit. See the [README sources](./README.md#sources) for the UN sanitation scale and current pit-emptying limitations.
