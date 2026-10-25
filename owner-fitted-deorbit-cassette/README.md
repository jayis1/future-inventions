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

## Sources and prior art

1. ESA, [Space Environment Report 2025](https://www.esa.int/Space_Safety/Space_Debris/ESA_Space_Environment_Report_2025) — debris scale, increasing congestion, mitigation context.
2. NASA, [State-of-the-Art of Small Spacecraft Technology: Deorbit Systems](https://www.nasa.gov/smallsat-institute/sst-soa/deorbit-systems/) (May 2026) — orbital-lifetime variability, five-year rules, existing sails and electromagnetic tethers. Existing devices establish component feasibility, not this proposed cassette's performance.
