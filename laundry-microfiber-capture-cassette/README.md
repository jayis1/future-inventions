# Laundry Microfiber Capture Cassette

**Author:** jayis1
**Status:** Concept (TRL 2; no prototype measurements)
**Development horizon:** 10–15 years for a validated, widely serviceable retrofit

## Problem

Washing synthetic and blended textiles sheds fibers into household wastewater. Sewer treatment can transfer retained fibers into sludge, and households without adequate treatment discharge directly to waterways. This is a planetary pollution pathway involving millions of laundry users, not a claim that any one filter will measurably improve health. Filters and washing bags already exist: a comparison of six devices measured roughly 21–78% reduction in fiber release under its particular test conditions [1]. Retention varies with pore size, fabric, wash program, clogging and maintenance [1, 2]. A fine filter that floods a home or is routinely rinsed into a sink is not an acceptable solution.

## Solution

An externally fitted, **repairable two-stage discharge cassette** fits only washer/standpipe combinations verified against the washer maker's discharge-height and backpressure limits. A reusable molded polypropylene housing uses a removable 500 µm stainless-steel coarse screen followed by a folded **60 µm woven stainless-steel screen** (approximately 0.12 m² unfolded area), with EPDM seals and tool-free captive fasteners. The fine screen opens inside a rigid, lidded cleaning tray: the user scrapes retained lint with a supplied spatula into a dry, sealable collection pouch, never rinses it into a drain, and reassembles after checking both seals. A mechanical differential-head flag exposes rising restriction without electronics, batteries or user tracking. Screen, gaskets and flag are replaceable separately; the housing is marked with the supported installation orientation and flow range.

This is **not** a universal in-line fitting. An installer first measures peak discharge flow and verifies the appliance's allowed external restriction and drain capacity. A 200 µm emergency screen on a relief path is proposed for testing to protect the washer pump if the fine screen blinds; activation makes a visible red indicator latch and counts as a failed capture cycle. It is not a flood guarantee: the installation must retain a manufacturer-compliant standpipe and an accessible shutoff. If even the relief path restricts flow, the device is unsuitable for that washer. No electrical automatic shutoff is claimed. Users must stop washing and service the cassette when the flag trips; accumulated fibers remain contained for disposal as residual solid waste according to local rules, not compost or greywater reuse. Disposal transfers pollution to a managed waste stream rather than destroying plastic.

**Unverified engineering targets:** at the tested washer's measured peak flow up to **20 L/min**, added restriction at clean condition below the appliance-specific limit and provisionally below **5 kPa**; at least **70% reduction in discharged synthetic-fiber mass for fibers ≥100 µm long**, relative to the same unfiltered wash protocol, across predeclared mixed-fabric loads; relief activation in fewer than **1% of washes** during the prescribed service interval. No claim is made for nanoplastics or every fiber geometry. A folded screen's nominal opening is not an absolute fiber-length cutoff.

## Key Innovation

The proposed contribution is a **serviceable capture-and-containment interface with a visible, latched failure witness**: collect fibers without wash-water cleaning, document when a clogged fine stage has been bypassed, and qualify pump compatibility before installation. Fine laundry screens themselves are established art, including the 60 µm XFiltra prototype reported in [1]; superiority over it is **not** established. Unlike this repository's [Magnetotactic Microplastic Scavenger](../magnetotactic-microplastic-scavenger/), this is a source-side physical filter with no engineered organisms. Unlike [Closed-Loop Textile Dye Recovery](../closed-loop-textile-dye-recovery-system/), it serves household wastewater rather than industrial dye chemistry. The open research question is whether households actually retain the fibers over a year without bypassing, rinsing, leaking or discarding the device.

## Target Cost

**Unquoted 2038 design target, USD, at 50,000 units/year:** $28 molded housing/fittings, $19 folded stainless screens, $9 EPDM seals and witness mechanism, $12 assembly/quality inspection, $12 packaging and factory overhead = **$80 ex-factory**. An additional **$30–70 installation allowance** depends on local plumbing; target **$10/year** for seals and collection pouches, assuming screens last at least five years with appropriate cleaning. These are planning allocations, not vendor quotes or a retail price; taxes, distribution, certification, disposal charges and plumber travel are excluded. The reusable metal screens should be recycled where feasible and polymer parts separated at end of life. If replacement costs or cleaning labor make sustained use impractical, redesign rather than counting theoretical capture.

## Impact

A laboratory study reported a mean **0.44 ± 0.04 g fibers per mixed wash** under its own protocol [1], not a universal household emission factor. As an **illustrative arithmetic scenario only**, 200 washes/year at 0.44 g/wash and 70% mass capture would divert **61.6 g/year per participating household** to managed solid waste, before any bypass, downtime, wear or disposal losses. A deployment of 100,000 households at the same assumptions would divert **6.16 metric tons/year**; real impact requires measured household wash and capture distributions. This does not establish avoided human disease, total ocean emissions or net environmental benefit.

A blinded, multi-home comparative trial should weigh incoming and discharged fibers by polymer and length band, log overflow and pressure, audit sealed-waste handling, and compare matched unfiltered washes and an existing commercial filter. Report intention-to-treat capture including missed cleanings and relief cycles, not just fresh-screen efficiency. Reject or revise the concept if it increases pump failures/floods, users rinse retained lint into drains, the relief routinely opens, or lifecycle assessment shows net harm. See [Specification](SPECIFICATION.md) for test gates and failure controls.

## How It Works

The washer's own pump sends effluent through its original discharge hose to a qualified external cassette, then onward to the existing compliant standpipe; the air gap and drain geometry are not replaced. A 500 µm screen catches larger lint before the 60 µm folded stainless mesh intercepts smaller fibers. The approximately 0.12 m² unfolded mesh area spreads flow, but its effective open area shrinks as lint accumulates. No capture cutoff follows directly from the pore dimension: flexible fibers can align with openings, while larger debris forms a restrictive mat.

A differential-head flag warns of restriction without a battery. If a fine screen blinds, the proposed 200 µm screened relief route may keep discharge moving, but its latched red witness means the wash is counted as a capture failure. Relief is not certified flood protection; the user stops the washer, and an installer rejects any pairing whose pump or drain cannot tolerate the worst credible restriction. For service, the removable screen opens in a lidded tray; lint is scraped into a sealed pouch for locally permitted residual-waste disposal. No rinse-to-drain cleaning, plastic destruction, or greywater reuse is implied.

## Technical Architecture

| Subsystem | Material / role | Verification boundary |
|---|---|---|
| Hydraulic interface | Washer hose → polypropylene housing → original standpipe; EPDM seals | Measure peak flow, allowed head, hose retention, leak rate and drain capacity per machine |
| Separation stack | 500 µm stainless pre-screen → 60 µm folded stainless mesh (0.12 m² nominal) | Count and weigh polymer-identified fibers in total effluent, including loaded screens |
| Safety witness | Passive differential-head flag and proposed 200 µm relief screen with red latch | Inject lint and partial blockage; record every relief event as failed capture |
| Service loop | Captive closure, lidded tray, spatula, sealed pouch; individually replaceable seals and screens | Audit whether all collected lint reaches managed solid waste |

At 20 L/min, flow is 0.000333 m³/s and gross nominal mesh flux is about 0.00278 m/s; neither number predicts actual head loss. The provisional 5 kPa clean-condition ceiling is about 0.51 m of water head and **never** supersedes a stricter washer-maker limit. Actual pleat open area, detergent foam, temperature and end-of-interval lint loading require bench measurement. See [Specification](SPECIFICATION.md) for rejection gates.

## Performance Benchmarks

These are **targets, not measured cassette results**. Test paired mixed polyester, acrylic and blended loads with detergent, predeclared cycles and temperature, both clean and at the end of the service interval; log total discharge volume/flow, pressure, drain time and relief events. Use downstream reference filtration with contamination blanks and polymer-identification; report dry mass for synthetic fibers ≥100 µm long separately from particle counts and smaller length bands. Set the service interval only after loaded-screen testing, not by assuming an arbitrary number of washes.

| Metric | Proposed pass criterion | Published comparator / limitation |
|---|---|---|
| Discharged synthetic-fiber mass ≥100 µm long | ≥70% reduction vs matched unfiltered wash, intention-to-treat across ≥30 paired washes | Napper et al. [1] reported 21–78% reduction in **total microfiber release** for six devices under a different detergent-free protocol; not a like-for-like size-selected result |
| Peak discharge and clean restriction | Qualify up to 20 L/min; <5 kPa **and** below the appliance's stricter limit | No published pressure baseline is asserted; test loaded restriction and pump temperature too |
| Reliability | Relief in <1% of serviced washes; no attributable pump damage or significant flooding in 100-home, 12-month pilot | Proposed gate, not a certified probability or safety guarantee |
| Maintenance / resource burden | Report actual cleaning time, screen longevity, waste mass, added water and electricity | No measured device values; passive design targets zero added electrical load, not zero lifecycle burden |

The 78 ± 5% XFiltra result [1] used a powered centrifugal separator and 60 µm mesh; the proposed passive cassette has **not** matched or exceeded it. The 0.44 ± 0.04 g per wash control figure [1] is for that study's mixed load, not the mass of synthetic ≥100 µm fibers in ordinary homes.

## Deployment Scenarios

- **Eligible household washer:** A qualified installer measures the discharge envelope and standpipe capacity, documents compatibility, and trains the occupant to inspect the flag and seal lint in a pouch. Renters or incompatible pumps should not improvise an in-line fit.
- **Shared apartment laundry:** A building operator selects compatible models, keeps spare seals/screens, logs each red-latch event and supplies a closed residual-waste bin; recurring missed service ends the trial rather than being counted as successful capture.
- **Small commercial laundry pilot:** Facilities staff monitor loaded-screen head loss, detergent chemistry and wash throughput on a single instrumented line before any expansion. High flow or continuous duty may require a different certified device, not parallel unvalidated cassettes.

## Risks & Mitigations

| Risk | Mitigation and falsifiable check |
|---|---|
| Clogging, pump overload, standpipe overflow | Qualify each washer/drain pair; stage maximum lint and partial blockage in 50-cycle bench tests, monitor head, discharge time, leaks and pump temperature; reject unsafe pairs |
| Relief or housing leak quietly defeats capture | Latch visible red on relief; inspect seals after service and sample downstream effluent; count relief and leakage cycles as failures |
| Variable fiber geometry, detergent or fabric | Paired randomized loads across polymers and wash programs; publish both mass and count by length band with blanks and uncertainty |
| Incorrect reassembly, missed service or lint rinsed away | Captive fasteners, oriented seals and lidded dry-cleaning tray; audit handling in the 12-month home pilot and credit only retained fibers |
| Corrosion, seal aging or filter shedding | Cycle stainless mesh, polypropylene and EPDM with detergent, bleach and hot discharge; inspect wear and polymer background before approving lifetime |
| Landfill leakage, packaging and labor burden | Seal pouches, follow local rules, assess cradle-to-disposal materials and maintenance; redesign if net burden exceeds avoided release |

## Vision for 2050

If pump-safe compatibility, low-effort dry servicing, durable parts and independently measured net environmental benefit survive years of field trials, source-side capture could become a routine option wherever laundry effluent is otherwise released. Repair shops could stock interchangeable screens and seals, while building operators track bypass events rather than treating a filter's presence as proof of success. Better textile design, wastewater treatment and responsible solid-waste handling would still matter: this cassette transfers some fibers to a managed stream, not out of existence. See the [Roadmap](ROADMAP.md) and [Impact Analysis](IMPACT_ANALYSIS.md) for the gates and conditional arithmetic behind that vision.

## References

1. Napper et al., “The efficiency of devices intended to reduce microfibre release during clothes washing,” *Science of the Total Environment* (2020). https://doi.org/10.1016/j.scitotenv.2020.140412
2. PLOS ONE, “Pore-size and polymer affect the ability of filters for washing-machines to reduce domestic emissions of fibres to sewage” (2020). https://doi.org/10.1371/journal.pone.0234248
