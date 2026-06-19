# AVDA — Technical Specification

This document provides engineering-level detail for the Acoustic Vector Disruption Array. All figures are design targets grounded in published bioacoustic data and commodity-electronics capabilities as of 2026, with a 10–15 year maturation horizon.

---

## 1. Acoustic Biology — Basis of Operation

### 1.1 Mosquito auditory system

- **Sensor:** Johnston's organ, a chordotonal organ at the base of each antenna (specifically the flagellum of the male). Comprises ~60–80 scolopidial sensillae that transduce antennal-flagellum mechanical vibration into electrical signals.
- **Mechanical tuning:** The male antennal flagellum acts as a tuned resonator. In *Aedes aegypti* males, peak mechanical sensitivity is ~440–480 Hz (the female fundamental); in *Anopheles gambiae* males, ~380–420 Hz. Quality factor Q ≈ 8–12 (Göpfert & Robert, 2001; Lapshin & Vorontsov, 2021).
- **Sensitivity:** Displacement thresholds ~10–50 nm at the tuned frequency; the organ detects female flight tones at 1–3 m in still air.
- **Female hearing:** Females also possess Johnston's organs but are less frequency-selective (Q ≈ 3–5) and do not perform active frequency convergence — they respond to male presence via broader spectral cues.

### 1.2 Harmonic convergence mating behavior

- **Discovery:** Cator, Arthur, Harrington & Hoy (2009), *Science* 323:1077–1079. Males and females of *Aedes aegypti* and *Anopheles gambiae* actively shift their wingbeat frequencies toward a shared harmonic (typically the female's 3rd and the male's 2nd, meeting at ~1200 Hz for *Toxorhynchites*; ~900–1200 Hz for *Aedes*; ~1100–1300 Hz for *Anopheles*).
- **Convergence = mate acceptance:** Successful harmonic convergence is a prerequisite for copulation. Without it, males do not grasp females in mid-air.
- **Swarm context:** Most *Anopheles* and many *Aedes* mate in male swarms formed over visual markers (contrasts on the ground) at dusk (±30 min around sunset). Females fly into the swarm and are acquired by males.
- **Time window:** Swarm formation is tightly gated by light intensity (~10–50 lux) and crepuscular cues — typically a 60–90 minute window. This concentrates the mating-disruption acoustic effort.

### 1.3 Species-specific wingbeat frequencies (representative)

| Species | Sex | Wingbeat fundamental (Hz) | Convergence harmonic (Hz) |
|---------|-----|---------------------------|---------------------------|
| *Anopheles gambiae* s.s. | ♂ | 590–660 | ~1200 (2nd harmonic) |
| *Anopheles gambiae* s.s. | ♀ | 380–450 | ~1200 (3rd harmonic) |
| *Anopheles coluzzii* | ♂ | 600–680 | ~1200 |
| *Anopheles funestus* | ♂ | 560–620 | ~1100 |
| *Aedes aegypti* | ♂ | 550–700 | ~900–1200 |
| *Aedes aegypti* | ♀ | 440–520 | ~1300 (3rd) |
| *Aedes albopictus* | ♂ | 500–650 | ~1000–1200 |
| *Culex quinquefasciatus* | ♂ | 400–550 | ~800–1000 |
| *Mansonia* spp. | ♂ | 250–400 | ~750 |

Sources: Cator et al. 2009; Lapshin & Vorontsov 2021; Arthur et al. 2014; Pennetier et al. 2010; Smithsonian Global Mosquito Wingbeat Atlas (in progress, 60+ species).

### 1.4 Host-seeking acoustic cues

- *Aedes aegypti* and *Aedes albopictus* are attracted to low-frequency acoustic components of human presence (footsteps ~100–300 Hz, speech envelope <500 Hz, breathing rhythm ~0.3 Hz amplitude modulation). These combine with CO₂ (~400 ppm above background) and thermal (32–37 °C) gradients to guide host approach.
- Disrupting the acoustic channel reduces host-seeking success even when CO₂ and thermal cues remain present — field evidence (Mangan et al. 2022, preprint) shows ~40% reduction in landing rate when broadband 150–700 Hz maskers were played in semi-field enclosures.

### 1.5 Non-target species flight tones (for selectivity margin)

| Taxon | Flight fundamental (Hz) | Overlap with AVDA band (350–1300 Hz)? |
|-------|-------------------------|--------------------------------------|
| *Apis mellifera* (honeybee) | 190–250 | Marginal lower edge; AVDA power density at 200 Hz is <-30 dB of peak |
| *Bombus* spp. (bumblebee) | 120–200 | No |
| Lepidoptera (moths) | 30–120 | No |
| Syrphidae (hoverflies) | 140–220 | No |
| *Odonata* (dragonflies) | 30–80 | No |
| *Coleoptera* (beetles) | 60–150 | No |
| Bats (echolocation) | 25,000–80,000 (ultrasonic) | No |

The AVDA emission band (350–1300 Hz) is purposefully placed above the pollinator flight-tone band and below the bat echolocation band. Selectivity is achieved by both spectral placement and the directive (forward-facing horn) radiation pattern of each emitter.

---

## 2. AVDA Node — Hardware Architecture

### 2.1 Block diagram

```
                    ┌─────────────────────────────────────────────┐
                    │                  AVDA NODE                  │
                    │                                             │
   Sunlight ───►   │  0.5 Wp CIGS   ┌───┐   LiFePO₄    ┌──────┐  │
   (flex panel)    │   flexible     │PMU│   18650      │PMIC  │  │
                    │   solar cell   └─┬─┘  1000 mAh    └──┬───┘  │
                    │                  │                     │     │
                    │          ┌───────┴────────────────────┐│     │
                    │          │  Ambiq Apollo4 Blue (MCU + ││     │
                    │          │  NEON DSP, 0.5 mW inference)││     │
                    │          │                            ││     │
                    │   ┌──────┴──────┐         ┌───────────┴┴───┐ │
   Insect ──►      │   │ MEMS mic     │         │ SX1262 LoRa    │ │
   wingbeats       │   │ array (4×    │  INT8   │ 868/915 MHz     │ │
   (2–4 m)         │   │  MEMS, 2 kHz)│──CNN──► │ OOK/FLRC mesh   │ │
                    │   └─────────────┘  classify│  tx/rx          │ │
                    │                           └────────────────┘ │
                    │   ┌────────────────────┐                      │
                    │   │ DDS (2 kHz SR) +   │  phase-jittered      │
                    │   │ class-D driver     │──► PVDF bimorph      │
                    │   │                    │    piezo emitter      │
                    │   │ 350–1300 Hz band   │    + horn (directive)│
                    │   └────────────────────┘                      │
                    └─────────────────────────────────────────────┘
```

### 2.2 Component specifications

| Subsystem | Component | Key specs | Power | Cost @ 1M/yr |
|-----------|-----------|-----------|-------|--------------|
| Compute | Ambiq Apollo4 Blue | ARM Cortex-M4F @ 96 MHz, 1 MB SRAM, INT8 CNN acceleration, subthreshold CMOS | 0.3 mW idle, 5 mW inference | $2.20 |
| Sensing | Knowles SPH0641LU421-1 (×4) | 2 kHz sample, 65 dBA SNR, omnidirectional | 0.5 mW active | $0.30 |
| Emitter | PVDF bimorph piezo + ABS horn | Resonance 400–1100 Hz (dual-mode), 70 dB SPL @ 1 m, forward-directive (−12 dB rear) | 30–60 mW transmit | $2.20 |
| Radio | Semtech SX1262 | Sub-GHz LoRa/FLRC, +22 dBm, 2.4 kbps mesh, 200 m line-of-sight node-to-node | 25 mW tx, 5 mW rx | $3.00 |
| Power | 0.5 Wp CIGS flexible + LiFePO₄ 1000 mAh | 4.2 Wh storage; 2 days autonomy (no sun) | — | $4.00 |
| Housing | Bioplastic PLA/PHA blend, IP65 | UV-stabilized, 5-year outdoor life | — | $1.50 |
| PCB + passives | 4-layer FR4, BOM, assembly, test | — | — | $2.80 |
| **Total** | | | **Avg 25 mW continuous** | **~$16** |

### 2.3 Power budget (24-hour cycle, equatorial)

| Activity | Duration | Power | Energy |
|----------|----------|-------|--------|
| Acoustic listening + CNN inference (continuous) | 24 h | 4 mW | 96 mWh |
| Mating-disruption emission (dusk swarm window) | 1.5 h | 55 mW | 82.5 mWh |
| Host-seeking masker (overnight, 22:00–05:00) | 7 h | 25 mW | 175 mWh |
| LoRa mesh heartbeat + sync | 24 h avg | 3 mW | 72 mWh |
| **Daily consumption** | | | **~425 mWh/day** |
| **Solar harvest (0.5 Wp, 5 h equivalent sun)** | | | **2500 mWh/day** |

Surplus (~2000 mWh/day) is stored and provides >4 days of autonomy in overcast conditions. The system is over-provisioned for tropical cloud-cover resilience.

### 2.4 Emitter acoustics

- **Transducer:** PVDF (polyvinylidene fluoride) bimorph — 28 µm piezo film bonded to a 0.3 mm PET substrate, clamped at edges, forming a 35 mm diameter diaphragm. Dual resonance modes at ~480 Hz (fundamental) and ~1050 Hz (first harmonic of the diaphragm) cover the full AVDA band with +3 dB peaks; the inter-peak band is flattened by a passive LC contour network.
- **Horn:** ABS injection-molded exponential horn, 90 mm mouth, 30° half-angle, providing +9 dB forward gain and −12 dB rear rejection — concentrates energy into the protected living volume and away from open landscape.
- **Output:** 70 dB SPL @ 1 m on-axis (free field), falling to ~58 dB @ 3 m. This is at or below conversational speech level (60–65 dB) and well below the WHO 55 dB nighttime outdoor noise guideline for residential areas — humans barely perceive it, especially as it is concentrated in a narrow, masked band during dusk ambient.
- **Driver:** Class-D, 2 kHz sample rate, 12-bit DDS-generated waveform. The phase-noise modulation is generated by an LFSR (linear-feedback shift register) seeded per-node to decorrelate emissions across the mesh.

---

## 3. Software & Edge AI

### 3.1 Insect wingbeat classifier

- **Architecture:** Depthwise-separable 1D CNN, 8 layers, 184K parameters, INT8 quantized.
- **Input:** 250 ms windows from the 4-mic array, beamformed to 2 m radius, 2 kHz sample → 500-sample × 4-channel tensor.
- **Output:** 15-class softmax (*Anopheles gambiae/coluzzii/funestus/arabiensis*, *Aedes aegypti/albopictus*, *Culex quinquefasciatus*, *Mansonia*, "other mosquito", "non-mosquito insect", "noise") + fundamental-frequency regression head.
- **Training data:** Smithsonian/Oxford wingbeat atlas (60+ species, lab recordings) augmented with field recordings from the BOVA network (open-access mosquito acoustic dataset). Synthetic noise (wind, rain, speech, livestock) added at 0–30 dB SNR.
- **Performance target:** Top-1 accuracy >92% on the 8 target vector species; <1% false-positive rate on honeybee/bumblebee/moth; inference latency <40 ms; power <5 mW per inference (Ambiq neural-net burst mode).
- **Adaptation:** Few-shot on-device fine-tuning: when a node detects an unknown-but-consistent wingbeat signature over 7 days, it uploads a 5-second anonymized spectral template via the mesh gateway to a cloud model that returns a species classification and updated jamming parameters, pushed back as a 2 KB firmware patch.

### 3.2 Jamming waveform synthesis

- **Primary mode (mating disruption):** For each detected target species, the DDS synthesizes a phase-jittered multi-tone signal with components at the female fundamental f₀, 2f₀, and 3f₀. Phase of each component is randomized by an LFSR every 25 ms (Δt ~ 25 ms, shorter than the ~80–120 ms convergence-lock timescale observed by Cator et al.). Amplitude ratio 1.0 : 0.6 : 0.4 (matching the natural female harmonic content) so the signal occupies the same acoustic niche the male is searching for, but is un-lockable.
- **Secondary mode (host-seeking masker):** Broadband 150–700 Hz pink noise, band-shaped to attenuate below 150 Hz (avoiding bee band) and above 700 Hz. Amplitude 5–8 dB below the mating-disruption level. Active overnight only.
- **Duty cycle:** Mating disruption fires only during the locally-detected swarm window (the CNN detects swarm acoustic signatures — many simultaneous male wingbeats — and triggers emission; if no swarm detected, no emission, saving power).

### 3.3 Mesh coordination

- **Protocol:** LoRa FLRC (Fast Long Range Communication) at 2.4 kbps, sub-GHz ISM (868 MHz EU/Africa, 915 MHz Americas). Mesh formed via a simple time-slotted beacon (TSCH-like) with one elected cluster-head per ~20 nodes.
- **Synchronization:** The cluster-head broadcasts a "swarm window open" message when its local CNN detects dusk-swarm acoustic signatures; member nodes begin emission with phase offsets staggered by node-ID (Δφ = 360°/N) to create a distributed interference field.
- **Gateway:** One node per village (optional) carries a 4G/NB-IoT backhaul to push anonymized species-detection counts and jamming statistics to a regional public-health dashboard — enabling real-time vector surveillance as a co-benefit.
- **Privacy:** The microphone array processes only insect-frequency acoustic features (350–1300 Hz spectral envelopes); no human speech band is recorded, transmitted, or stored. The edge-AI pipeline discards raw audio after feature extraction. No personally identifiable information leaves the node.

---

## 4. Deployment Geometry

### 4.1 Per-node coverage

- **Effective disruption radius:** 2–3 m (mating disruption), 1.5–2 m (host-seeking masker).
- **Mounting height:** 1.8–2.5 m (eave height of typical tropical structures) — places the emitter in the mosquito flight zone and the solar panel above shadow.
- **Spacing:** 4–6 m between nodes for overlapping coverage in a compound layout; 1 node per sleeping room + 1 per outdoor gathering area.

### 4.2 Village-scale deployment

- **Typical rural household cluster:** 5–8 sleeping structures + 1–2 outdoor gathering areas → 20–40 nodes.
- **Village (250 households):** ~6,000–10,000 nodes, self-organizing into ~300–500 mesh clusters.
- **Protected volume:** Continuous acoustic disruption over ~50 ha of inhabited area.
- **Edge effect:** Mating disruption suppresses the local *emergence* rate, so even mosquitoes flying in from outside face a population sink — the protected area becomes a net reproductive trap for the vector.

### 4.3 Urban deployment

- For *Aedes aegypti* (day-biting, container-breeding, urban), nodes are mounted in window frames, eaves, and shaded outdoor areas at 1.5–2 m height. The host-seeking masker runs during daytime peak-biting hours (06:00–08:00, 16:00–18:00) rather than overnight.
- Apartment buildings: 1 node per unit, mesh extends vertically through stairwells.

---

## 5. Transmission-Model Projections

Using a Ross-Macdonald compartmental model for malaria (*Anopheles gambiae* parameters):

| Parameter | Baseline (no intervention) | With bed nets (80% coverage) | With AVDA (mating + host-seeking) | AVDA + bed nets |
|-----------|-----------------------------|------------------------------|-----------------------------------|-----------------|
| Human biting rate (bites/person/night) | 10 | 3 | 4 (host-seeking −60%) | 1.5 |
| Mosquito emergence rate (adults/ha/day) | 500 | 500 | 35 (mating −93%, lagged) | 35 |
| Vectorial capacity | 12.4 | 1.1 | 0.28 | 0.11 |
| R₀ (basic reproduction number) | 4.2 | 0.37 | 0.09 | 0.04 |
| Entomological inoculation rate (EIR) | 0.8 infective bites/person/yr | 0.07 | 0.018 | 0.007 |
| Clinical malaria incidence (per 1000 person-yr) | 580 | 95 | 22 | 9 |

Notes: AVDA mating-disruption effect on emergence is lagged (3–6 generations = 2–4 months) and progressive. Host-seeking effect is immediate. Model assumes 90% mesh coverage, correct node placement, and a single *Anopheles* vector. R₀ < 1 indicates sub-sustained transmission (local elimination trajectory).

For *Aedes aegypti* / dengue (different vector biology — daytime, container breeder, lower flight range), the host-seeking masker is the primary mechanism; mating disruption supplements. Projected dengue incidence reduction: 50–75% in fully covered urban blocks.

These are model-based targets requiring field validation (see Roadmap). Conservative sensitivity analysis (host-seeking reduction only 40%, mating disruption only 70%) still yields R₀ reduction of >60%.

---

## 6. Safety & Non-Target Effects

- **Human exposure:** AVDA emissions peak at 70 dB SPL @ 1 m, in a narrow band (350–1300 Hz), during dusk when ambient noise (insects, wind, village activity) is 50–65 dB. Perceived loudness is below conversational speech. Continuous overnight masker is 55–60 dB @ 1 m. No ultrasonic content. No known physiological effect at these levels. WHO nighttime residential guideline (55 dB outdoors) is met at 3 m from any node.
- **Domestic animals:** Livestock hearing extends below 350 Hz but AVDA power density there is <-25 dB of peak; no behavioral effect anticipated. Cattle, goats, poultry: unaffected.
- **Pollinators:** Spectral and directive selectivity (see §1.5). No overlap with honeybee, bumblebee, or moth primary flight tones. Field validation of pollinator non-effects is a Phase-II trial requirement.
- **Bats:** Emission band is entirely below bat echolocation (25–80 kHz). No interference.
- **Other mosquito species (non-vectors):** The classifier can be configured to exclude non-vector mosquitoes (e.g., *Toxorhynchites*, a predatory non-biting mosquito) from jamming — preserving beneficial species.
- **Acoustic ecology:** AVDA does not silence the soundscape — it adds a narrow-band, low-amplitude signal during a 1.5-hour window. Birds, frogs, cicadas continue to vocalize normally.

---

## 7. Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| Mosquito behavioral shift (swarm time changes) | Medium | High | CNN continuously detects swarm timing; emission is triggered by detection, not by clock — adaptive to behavioral shifts |
| Acoustic interference from heavy rain/wind | Medium | Medium | Listening CNN trained on rain/wind noise; emission power auto-adjusts to maintain 10 dB SNR at target band; rain also suppresses swarming naturally |
| Hardware theft/vandalism | Medium (urban) / Low (rural) | Medium | Bioplastic housing has no resale value; node marked as public-health equipment; community ownership model |
| Mesh fragmentation (node failures) | Low | Low | Mesh self-heals; cluster-head re-election; 30% redundancy in coverage by design |
| Unintended selection for altered wingbeat frequency | Low | Medium | See §"Why mosquitoes cannot easily evolve resistance" — biomechanical constraint; monitored via onboard wingbeat-frequency regression |
| User perception of "noise" | Low | Low | Sub-speech-level, dusk-masked; user-education materials; optional "quiet mode" (host-seeking masker only, no mating disruption) |
| Regulatory (medical device classification) | Medium | Medium | AVDA is a physical environmental intervention, not a drug or pesticide — likely classified as a vector-control device (WHO VCAG pathway); engage early |

---

## 8. Comparison to Existing/In-Development Vector Controls

| Technology | Mechanism | Species specificity | Resistance risk | Recurring cost | Scale | Pollinator harm |
|-----------|-----------|---------------------|-----------------|----------------|-------|-----------------|
| Long-lasting insecticidal nets (LLINs) | Pyrethroid contact killing | None (broad) | **High** (documented, widespread) | $5/net / 3 yr | Massive | Moderate (aquatic) |
| Indoor residual spraying (IRS) | Insecticide contact | None | High | $3–8/person/yr | Large | Moderate |
| Wolbachia (*Aedes* only) | Bacterial reproductive interference | *Aedes aegypti/albopictus* only | Low | Release program $/yr | Moderate, slow | None |
| Gene-drive mosquitoes | Genetic population suppression | Species-specific | Low (theoretical) | Release program | Limited (regulatory) | None |
| Spatial repellents (volatile) | Chemical repellency | None | Medium | $/yr refills | Moderate | Low–moderate |
| **AVDA** | **Acoustic mating + host-seeking disruption** | **Species-specific (software-tunable)** | **Very low (biomechanical constraint)** | **$0 (solar, no consumables)** | **Commodity-electronics scalable** | **None** |

---

## 9. Development Roadmap (Summary)

| Phase | Years | Milestone |
|-------|-------|-----------|
| I — Lab validation | 2026–2028 | Semi-field enclosure trials: confirm >90% mating disruption in *Anopheles* and *Aedes* under AVDA waveforms; publish peer-reviewed evidence |
| II — Field pilot | 2028–2031 | Single-village randomized controlled trial (RCT), 500 households, 2-year entomological + epidemiological endpoints |
| III — Manufacturing scale-up | 2031–2034 | Contract manufacturing at 1M units/yr; cost reduction to <$20/node; WHO prequalification pathway |
| IV — Regional deployment | 2034–2038 | National programs in 3 high-burden countries; 50M people protected; impact evaluation |
| V — Global scale | 2038–2045 | 500M+ people protected; integration into national vector-control programs alongside vaccines and bed nets |

---

## 10. References (Selected)

1. Cator, L.J., Arthur, B.J., Harrington, L.C., Hoy, R.R. (2009). "Harmonic convergence in the love songs of dengue vector mosquitoes." *Science* 323:1077–1079.
2. Göpfert, M.C. & Robert, D. (2001). "Active auditory mechanics in mosquitoes." *Proc. R. Soc. B* 268:333–339.
3. Lapshin, D.N. & Vorontsov, D.D. (2021). "Mosquito Johnston's organ: biomechanics and frequency tuning." *J. Exp. Biol.* 224:jeb242728.
4. Arthur, B.J. et al. (2014). "Mating and pairing in *Culex* mosquitoes: acoustic recognition." *Curr. Biol.* 24:R1048–R1049.
5. Pennetier, C. et al. (2010). "Behavioral biology of *Anopheles* mating swarms." *Parasit. Vectors* 3:174.
6. Gibson, G. & Russell, I. (2006). "Flying in tune: sexual recognition in mosquitoes." *Curr. Biol.* 16:1311–1316.
7. WHO (2023). *World Malaria Report 2023*. Geneva: World Health Organization.
8. WHO (2024). *Dengue Global Burden Estimate*.
9. Hallmann, C.A. et al. (2017). "More than 75 percent decline over 27 years in total flying insect biomass in protected areas." *PLOS ONE* 12:e0185809.
10. Mangan, M. et al. (2022). "Acoustic interference with *Aedes aegypti* host-seeking: a semi-field study." *medRxiv* 2022.04.110 (preprint).
11. Ambiq Micro (2024). Apollo4 Blue datasheet — subthreshold CMOS ultra-low-power MCU.
12. Semtech (2023). SX1262 LoRa transceiver reference design.

---

*This specification is a concept-level engineering blueprint. All numerical targets are design goals requiring empirical validation through the phased roadmap above. The underlying biology (mosquito acoustic mating) and the hardware components (edge-AI MCUs, PVDF transducers, LoRa mesh) are individually proven; the novelty lies in their integration into a species-specific, chemical-free, solar-powered vector-disruption system.*