# Owner-Fitted Deorbit Cassette

**Author: jayis1**
**Status: concept; no flight qualification or measured performance claimed.**

## Problem

Defunct satellites left in low Earth orbit can collide and fragment, threatening the weather, navigation, communications, and climate-observation services used by billions. ESA's 2025 Space Environment Report estimates more than 1.2 million debris objects larger than 1 cm and reports that debris still grows even without additional launches. A small satellite above roughly 500 km cannot assume that natural decay will meet a five-year disposal deadline; solar activity, mass, and orientation matter [1, 2]. Removing someone else's object after failure is expensive and can become a coercive capability. Prevention should be installed by its owner before launch.

## Solution

A sealed, pre-fitted disposal cassette bolts to a consenting operator's 10–100 kg satellite. At mission end it passivates the host's stored energy, then releases a conductive aluminum-film tape on a damped reel, with a captive end mass rather than any free-flying part. Motion through Earth's magnetic field induces a voltage; when ionospheric current collection and a closed circuit are available, Lorentz force opposes orbital motion. At a lower, mission-modelled altitude, a separate spring deploys a 2 m² polyimide drag sail. Atmospheric molecules then remove orbital energy more effectively as the satellite descends. Both stages are disposal-only and cannot rendezvous with, identify, or attach to other spacecraft.

A stand-alone, redundant power reserve and operator-approved end-of-life arming prevent loss of the host computer from making disposal impossible. The cassette does **not** trigger solely because communication is lost: an armed time window, independent health checks, ground coordination, and documented collision screening gate deployment. If the tether's circuit or local plasma does not support useful current, the sail remains an independently deployable fallback; neither mode guarantees a disposal time at every orbit. A simple sail-only version is preferred wherever analysis shows it is enough.

## Key Innovation

Drag sails and electrodynamic tapes already exist: NASA records the 2022 ADEO sail deployment and describes Terminator Tape and the comparative DragRacer flight [2]. The proposed advance is **a certifiable, owner-fitted, sequential disposal architecture**: independent release paths, no released fragments, a low-altitude sail handoff rather than simultaneous large exposed structures, and a mission-specific go/no-go lifetime and conjunction-risk model. The innovation to prove is reliable *system-level disposal after host failure*, not a new force of nature. Relative to this repository's ocean-current-turbine and regenerative-freight-ropeway, this works in orbit and reduces debris rather than generating or recovering terrestrial transport energy; no existing invention here addresses satellite end-of-life.

### Design targets, not demonstrated results

- 10–100 kg host spacecraft; initially evaluate nearly circular 550–700 km low-Earth orbits. Exclude higher orbits unless a validated lifetime and collision-risk model supports them.
- 200 m aluminum-coated polyimide tape, 2 m² sail, cassette mass ≤3 kg; deployment success ≥99% across vibration, thermal-vacuum, radiation, and end-of-life electrical-fault tests. All values are engineering goals.
- Post-mission reentry within **five years in the approved reference orbit and conservative solar-density cases**; compare with the *same* bus without the cassette. This is a test criterion, not a blanket promise.
- Zero released components; independent testing of tether severing, sail tearing, electrical arcing, and additional conjunction risk before flight acceptance.

**Sanity check, not an orbital-lifetime estimate:** for an illustrative 200 m conductor carrying 0.01 A perpendicular to a 30 µT field, the *ideal upper-bound* Lorentz force is `I L B = 0.00006 N`. At 7.5 km/s the corresponding orbital-energy removal is 0.45 W. The ideal motional voltage is `v L B = 45 V`, but collection impedance, circuit closure, orientation and field projection can reduce current or braking to near zero. Separately, at an illustrative atmospheric density of 10⁻¹³ kg/m³, 2 m² area, drag coefficient 2.2 and speed 7.5 km/s, `½ ρ Cᴅ A v² ≈ 0.0000124 N`; density varies by orders of magnitude. These checks justify orbit propagation, not a five-year prediction. Orbital energy goes into electrical dissipation/plasma interactions and atmospheric heating, not free electricity.

## Target Cost

**Unvalidated 2035 manufacturing target:** US$250 per cassette at 100,000 units/year, excluding satellite integration, launch-mass cost, tracking, insurance, and licensing. Illustrative ex-factory allocation: US$45 tape/reel/end mass + US$55 sail/booms + US$65 redundant timer/reserve/arming electronics + US$45 enclosure/release hardware + US$40 assembly and acceptance test = US$250. Assuming a five-year service life, the simple hardware allocation is US$50 per satellite-year, before the excluded costs. Consumables are not replenished in orbit; the one-shot cassette and satellite reenter together. A mission that needs controlled reentry or cannot tolerate tether exposure must use a different disposal method; this price cannot be compared directly with a propulsive system offering controlled reentry.

## Impact

A planning scenario of 10,000 eligible owner-equipped satellites over ten years would give up to 10,000 spacecraft an independent disposal path **if** reliability and orbital-lifetime trials pass. This is not a prediction of collisions or lives saved. The goal is to reduce time spent as derelict collision targets while preserving shared orbital services for Earth. Fleet-scale benefit requires verified lifetimes and conjunction analysis, not merely a high number of installations.

## Safety, limits, and development path

A long conductor can create conjunction and severing hazards and cannot steer clear of another object after release. Operators must coordinate deployment, publish the predicted ephemeris and new collision cross-section to authorized traffic services, monitor its track, and demonstrate that added short-term encounter risk is outweighed by reduced derelict lifetime. A severed tape can itself become debris: captive-reel and fracture containment tests are hard release gates, not assumed solutions. The sail may fail to inflate or may worsen reentry survivability; materials and host must pass casualty-risk assessment and passivation requirements. Never deploy on an inhabited/controlled-reentry vehicle or without regulator and operator approval. No third-party attachment, inspection payload, targeting, or remote disablement capability is included.

Over 10–20 years: first bench-test the circuit/current in representative plasma and measure tape-release dynamics; then fly a consenting paired-satellite comparison, one equipped and one baseline, with independently tracked decay; finally qualify a bounded orbit/host envelope against vibration, radiation, worst-case solar activity, collision-risk, and reentry standards. The gating uncertainty is whether reliable plasma contact and safe tether deployment provide net benefit over the mature sail alone. If they do not, retire the tether stage rather than claim synergy.

## How It Works

The owner fits the sealed cassette before launch; there is no in-orbit retrofit or third-party capture. It stays mechanically inhibited through launch and mission operations. After a mission-specific authorization and independent timer/health checks, the operator screens the planned deployment with a traffic service; a dead host is not itself permission to deploy. The proposed autonomous fallback acts only inside a pre-approved disposal window after loss of heartbeat, with an independently powered clock and a second independent inhibit. Those logic paths must be tested against false activation and long-term battery decay.

The reel extends the **captive** 200 m conductive tape and retains its end mass. Orbital motion through Earth's magnetic field can induce current via ionospheric plasma; the resulting Lorentz force removes orbital energy only when geometry and circuit closure cooperate. The 2 m² sail is a separate later-stage device, released at an altitude chosen by mission propagation rather than by a universal timer. Its drag is approximately `½ ρ Cᴅ A v²`: at high altitude or low solar activity, a small sail may contribute too little. A 550–700 km, 10–100 kg mission is the *evaluation envelope*, not an assertion that every such orbit meets five years. A sail-only cassette wins whenever it meets the operator's lifetime and conjunction-risk requirements without tether exposure [2].

## Technical Architecture

- **Integration and containment:** owner-approved mechanical interface, launch locks, captive reel/end mass and fragment-retaining sail structure; optional host heartbeat is informational, not the sole power or trigger source.
- **Independent control:** isolated reserve, clock, authenticated owner configuration and two independent launch/mission inhibits. On ambiguous status, remain stowed and alert the operator when communication is possible; autonomous fallback is limited to the licensed, pre-screened window.
- **Energy removal:** current-collection/tape path first where qualified; electrically independent sail release later. Neither supplies steering or controlled reentry. Ground tracking, not a cassette GPS claim, supplies orbit estimates and evidence of decay.
- **Operations data flow:** owner sets approved orbit/time envelope → traffic service checks conjunctions → cassette arms/reports status → independent tracker updates ephemeris and measured decay → operator maintains registration, screening and disposal records. If tracking or authorization is absent, no new deployment decision is justified.

The differentiator is owner-fit integration plus a host-independent, sequential fallback, **not** invention of drag sails or electrodynamic tethers. Existing sails have flown; the combined architecture, safety logic and reliability target have not [2]. Propulsive disposal can maneuver but needs working control and propellant; a sail-only module has fewer failure modes than this two-stage design; an exposed tape brings plasma and severance uncertainties. No option universally wins.

## Performance Benchmarks

All cassette figures below are **design targets**, not measured results; comparisons are technology-class observations, not matched-orbit trials. A baseline and fitted spacecraft must be propagated with identical geometry, density history, attitude, inclination and mission end date before claiming a lifetime benefit [2].

| Metric | Present comparator | Cassette target | Basis / caveat |
| --- | --- | --- | --- |
| Host and orbit | Commercial sails span multiple spacecraft classes [2] | 10–100 kg; near-circular 550–700 km evaluation | No guarantee at 700 km; screen each orbit |
| Added hardware | NASA lists deployed ~3.6 m² ADEO-2 and 0.808 kg tape-class hardware [2] | 2 m² sail, 200 m tape, ≤3 kg total | Different missions and devices; not a like-for-like mass advantage |
| Disposal duration | Natural decay at >500 km can exceed five years [2] | ≤5 years only in approved reference cases | Must pass conservative-density propagation and on-orbit validation |
| Reliability | Component flight heritage does not validate this sequence [2] | ≥99% successful deployment in qualification campaign | Test aspiration; includes dead-host and non-activation cases |
| Unit price | No comparable installed market price asserted | US$250 ex-factory at 100,000/year by 2035 | Unvalidated scale target; integration, launch and monitoring excluded |

## Deployment Scenarios

1. **University smallsat:** a 10 kg near-circular ~550 km mission fits a pre-qualified cassette before dispenser delivery. The owner keeps independent power and a licensed end-of-life window; it compares a sail-only and two-stage design under identical solar-density cases. Value: a failure-tolerant disposal plan, not a promised reentry date.
2. **Earth-observation operator:** a 50 kg ~600 km craft can carry the ≤3 kg concept if its mass and keep-out envelopes allow it. The owner commissions per-orbit tether-current, sail-drag and conjunction simulations; if the tape raises net risk or has little Lorentz braking at that inclination, it chooses the sail-only or another method. Value: documented disposal evidence after host failure.
3. **Constellation integrator:** a fleet of 100 kg craft at ~700 km evaluates whether the five-year criterion is physically reachable under low solar activity. The cassette may be rejected in favor of propulsion or a lower operating orbit. Value: a standardized acceptance test and explicit no-go result, not automatic licensing compliance.

## Risks & Mitigations

- **Premature or unauthorized release:** it can terminate a healthy mission. Independent inhibits, authenticated configuration, anti-replay logs and a pre-approved time/orbit window are mandatory; missed heartbeats alone must never fire it. Measure false triggers separately from successful deployment.
- **Net collision risk:** the deployed sail and especially the long tape increase instantaneous encounter cross-section. Compare integrated cross-section × time along the *whole changing orbit*, plus severance and tracking uncertainty, against the no-cassette case. Reject deployments where shortened residence does not outweigh increased exposure; neither a shorter lifetime nor more area alone proves fewer collisions.
- **Non-deployment and uncertain thrust:** dormant-cell degradation, failed release, tumbling, weak plasma collection and field geometry can defeat the mechanism. Test after simulated years in vacuum/radiation, derate sail projected area for tumbling, monitor tracking-derived decay, and retain a sail-only or other approved fallback. No autonomous promise compensates for an exhausted reserve.
- **Fragments, host damage and reentry:** contain reel/end mass and sail tears, qualify launch locks against vibration and accidental release, inspect outgassing and antenna/optics clearances, and model the *whole host* plus cassette for passivation and uncontrolled-reentry casualty risk. Aluminum/polyimide help demisability but do not prove it.
- **Regulatory and operational acceptance:** owner and regulator must approve disposal and traffic coordination; the device has no right to act on another object's orbit. A cassette that cannot satisfy mission-specific licensing, screening or reentry conditions does not fly.

## Vision for 2050

If independent on-orbit measurements establish a net safety benefit, disposal evidence could become as routine as a launch manifest: each owner selects a validated sail, tape or propulsive option for its orbit, publishes the authorized end-of-life envelope, and reconciles tracked decay against the preflight model. The long-term product is not a universal orbital broom; it is a dependable and auditable *owner-installed* path that makes leaving a failed satellite in a crowded orbit less likely. This outcome remains conditional on reliability, operator adoption and independently verified safety.

## Sources and prior art

1. ESA, [Space Environment Report 2025](https://www.esa.int/Space_Safety/Space_Debris/ESA_Space_Environment_Report_2025) — debris scale, increasing congestion, mitigation context.
2. NASA, [State-of-the-Art of Small Spacecraft Technology: Deorbit Systems](https://www.nasa.gov/smallsat-institute/sst-soa/deorbit-systems/) (May 2026) — orbital-lifetime variability, five-year rules, existing sails and electromagnetic tethers. Existing devices establish component feasibility, not this proposed cassette's performance.
