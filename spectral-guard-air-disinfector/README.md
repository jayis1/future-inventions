# Spectral-Guard Air Disinfector

**Author: jayis1** · **Status: research concept (TRL 2)** · **Category: Airborne Disease Prevention / Universal Basic Services**

## Problem

Crowded clinics and classrooms can share infectious aerosols even when windows cannot be kept open. WHO estimates 10.7 million people developed tuberculosis and 1.23 million died of it in 2024; TB spreads through the air.[1] Ventilation, respiratory protection, diagnosis and treatment remain essential. Germicidal UV is a possible *additional* air-cleaning layer, but a 222 nm lamp cannot be assumed safe merely because its nominal peak is 222 nm: unwanted longer-wavelength emission, ozone and installation geometry matter.[2]

## Solution

A ceiling-mounted, repairable room fixture combines a filtered krypton-chloride (KrCl) 222 nm excimer source with a mechanically retained dielectric bandpass filter, a baffled light aperture, and a separate replaceable ozone-destruction module. A low-cost 12 V DC supply can run from a clinic battery/solar system sized separately. Germicidal photons damage nucleic acids in passing airborne microbes; room air must mix into the illuminated volume. The design **never** claims to sterilize a room, diagnose disease or replace clean outdoor air.

A factory spectral scan qualifies the complete aperture at multiple angles, not just the lamp. A service-only interlock shuts the emitter off when the filter housing opens; a paired optical reference checks *relative* transmission drift during operation. An ozone sensor at breathing height and a measured ventilation minimum are prerequisites to any occupied-room trial. Faults, sensor expiry or power loss switch the emitter off; a visible label says that the room's baseline ventilation is still required.

## Key Innovation

Filtered far-UVC lamps and UV air cleaning already exist.[2] The research contribution is a **replaceable, factory-mapped optical-and-ozone module** whose measured spectral map, spatial irradiance map and ozone-generation test travel with its serialised module, coupled to an offline fail-closed daily exposure budget for the *worst accessible position* in a specified room layout. Installation cannot enable occupied-mode irradiation until the local assessor enters a measured geometry and ventilation result; opening the optic, replacing the source or exceeding a calibrated cumulative irradiance budget invalidates that assessment. This is a testable safety architecture, not a claim of worldwide patent novelty. It does not track or identify occupants.

## Target Cost

**Research target, not a quotation:** US$450 ex-factory per 50 m³-room fixture at 10,000 units/year in 2038 (lamp/driver US$170, optic/baffle US$100, controller/sensors US$90, housing/ozone module US$90); estimated US$150–300 installation and US$80–150/year for source, filter, calibration and ozone-module service. Excludes ventilation, solar/battery system, safety certification, taxes, training and site survey. Solid-state 222 nm emitters may replace the excimer source if efficiency, lifetime and spectral purity improve; this is a research dependency, not a prerequisite for the first prototype.

## Impact

Pilot target: in a **50 m³ test room** with specified mixing and ventilation, achieve **at least 5 equivalent air changes per hour of additional airborne test-aerosol inactivation**, measured against the same room with the emitter off, while demonstrating compliant *spectrally weighted* accessible exposure and no unsafe incremental ozone or secondary pollutants. These are unproven co-targets: if either safety test fails, occupied operation is prohibited. A deployment of 10,000 qualified fixtures could cover at most 10,000 suitable rooms; infection reduction and lives saved cannot be inferred without controlled studies. Preserve ventilation, respirators where indicated, and TB case-finding and treatment. See [SPECIFICATION.md](./SPECIFICATION.md) for acceptance and failure tests.

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/tuberculosis
[2] https://pubmed.ncbi.nlm.nih.gov/?term=far+UVC+222+nm+ozone+room
