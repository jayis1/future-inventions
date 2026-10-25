# Receive-Only Disaster Bulletin

**Author: jayis1** · Concept, not a certified public-warning system

## Problem

A warning is useful only if people can see and trust it. The ITU says roughly **one-third of the world's population** lacks early-warning-system coverage, with accessibility and connectivity barriers especially acute in marginalized and remote communities.[1] Phones, mains power and cellular service can fail together in a flood or storm. A public board at a clinic, market or shelter could serve people without a handset, but it must not quietly become a tracking or rumor-distribution device.

## Solution

Mount a weather-sealed, solar-powered **receive-only e-paper notice tile** at an accessible public entrance. A trained local maintainer installs it at an approved site, checks legibility and language with residents, and tests reception monthly. An authorized warning authority publishes a short, signed, locally translated bulletin through independently powered regional transmitters. Each tile receives the same one-to-many broadcast, verifies the signature against locally provisioned public keys, checks the message's region and expiry, and prints the actionable headline, instruction, issuing authority and last-verification time in large text. A tactile label points to an established non-digital warning channel. No phone, account, GPS, microphone, camera or uplink is required.

Materials: a reflective bistable e-paper display; a low-power sub-GHz LoRa receiver front end; a modest microcontroller with read-only verified firmware and protected public-key storage; a 2 Wp crystalline-silicon photovoltaic panel; replaceable LiFePO4 battery; recycled-aluminum frame, repairable gasket and impact-resistant cover. A receive-capable radio IC may be used only with its transmitter output physically unconnected from the antenna path and its power amplifier disabled in hardware; a compliance test must confirm that a faulty firmware image cannot radiate a packet. Where this hardware boundary cannot be certified, use a dedicated receive-only front end. Semtech lists approximately 4.6 mA active receive current for its SX1262 reference transceiver; that is a component figure, **not** a measured tile power budget.[2]

This is a **last-mile display**, not a weather sensor, prediction service, person-to-person mesh or substitute for sirens, door-to-door outreach and official radio. No tile can relay messages: each installation needs coverage from one or more authorized transmitters, which are separate infrastructure and a significant cost. A simple local status button can reveal battery and reception age on the screen without sending information anywhere.

## Key Innovation

The proposed advance is a **physically one-way, publicly readable warning endpoint with a fail-visible trust state**, rather than another two-way off-grid messenger. LoRa messaging and rebroadcast already exist in Meshtastic; it can also carry optional location data.[4] CAP already standardizes alert metadata, multilingual messages, update/cancel behavior and possible signatures.[3] The proposed integration deliberately removes the endpoint's transmit path, translates only an authority-signed, bounded CAP-derived subset at a trusted gateway, and prints **STALE / UNVERIFIED — CHECK OTHER CHANNELS** when signatures, time, region, update ordering or reception fail. This is a testable privacy and safety property, not a claim to invent LoRa, CAP, e-paper or cryptography.

The hard unanswered engineering question is whether an affordable, outdoor, receive-only sign can make its *absence of a valid warning* as legible as a valid warning across languages and disabilities. Tiles must not display an expired warning as current merely because e-paper retains an image without power. The gateway signs compact packets over the canonical fields (region, issuer, sequence, issue/expiry times, language and text); local keys are pinned during supervised installation, with signed rotations and an independent revocation procedure. If the clock is untrusted, the display downgrades to unverified; it cannot reconstruct authoritative time from an unauthenticated broadcast.

## Target Cost

**Unverified 2038 target at 100,000 tiles/year:** US$85 ex-factory per tile: US$25 display, US$15 panel and replaceable cell, US$12 radio/controller/security, US$15 enclosure/seals, US$18 assembly/test. Installation target US$35 brings one installed tile to **US$120**. Assume five years of service and US$6/year inspection, gasket/battery reserve and cleaning: **US$30/tile-year**, or **US$0.60/person-year** *only if* an average of 50 distinct residents actually reads each tile (120/5 + 6, divided by 50). The 50-reader assumption is not measured and is not equivalent to warnings received. Figures exclude regional transmitters, official feed integration, licensing, translations, site permissions, vandalism, taxes, financing and trained outreach. Existing radio and phone alerts may be cheaper where reliable; compare their actual delivered-and-understood warning cost in pilots, not merely device prices.

## Impact

**Planning capacity, not an achieved outcome:** 100,000 correctly sited tiles × 50 distinct regular readers could put notices within reach of **5 million people**; missed messages, inaccessible placement and duplicate readers reduce actual reach. A trial would compare bulletin recall, correct action and time-to-receipt against the site's existing radio, SMS, siren and community-outreach channels, including groups with limited literacy or mobility. Do not infer lives saved from display counts. Pilot first with non-urgent drill messages and then under the local authority's emergency communications protocol.

**Energy sanity check (design assumptions, not measured):** at 3.3 V and 4.6 mA continuously receiving, the radio alone consumes about **0.364 Wh/day**.[2] Allow another 0.010 W average for controller and overhead: about **0.604 Wh/day** before display refresh, losses and cold effects. Budget **1 Wh/day total** and **6 Wh usable** after battery reserve for a *six-day nominal* sunless period. A 2 Wp panel at two peak-sun-hours/day and 50% end-to-end derating would supply **2 Wh/day** in that assumed climate; shaded, winter or storm conditions require site-specific testing and possibly a larger panel. Do not advertise six-day autonomy until complete-unit cold-weather and aged-cell tests pass.

### Risks and validation

- **False, replayed or canceled alerts:** reject invalid signatures and old sequence numbers; honor signed cancel/update messages; exercise key compromise and expiry tests with the public warning authority. A receiver-only design prevents outgoing tracking by the tile, not jamming, physical tampering or malicious transmitters.
- **Silent failure:** loss of radio, battery, time or keys must visibly mark the last message stale; a dead display is still a risk, so maintainers inspect every month and after major storms. Pair with independent sirens and human outreach; never assume absence of a notice means safety.
- **Accessibility and radio regulation:** test multilingual typography, low-vision legibility and placement with local users; measure coverage and packet loss in dense housing, valleys and storms. Select only locally lawful spectrum/power and get required device approvals. Do not use person identifiers, location reports or behavioral logs.
- **Compromised keys and clocks:** a signing key can be stolen and a clock can fail. Provision multiple scoped issuers, rehearse signed revocation and supervised physical recovery, and show UNVERIFIED whenever freshness cannot be established. Never treat a replayed cancellation or power-on reset as an all-clear.
- **Human factors and fatigue:** test instructions with low-vision and low-literacy readers and local languages; provide tactile directions to an independent audio channel. Suppress duplicate display refreshes but retain valid updates. Measure false-alert confusion and whether people take the right action, not just whether packets arrive.
- **Feasibility gates:** years 0–2, build a receive-only hardware prototype and prove zero radiated uplink under fault injection; years 3–5, validate signed CAP-to-packet translation, stale-state usability and energy balance in weather chambers; years 5–10, paired community drills against current channels; years 10–20, manufacturing only where authorities fund coverage, maintenance and accessible outreach. Any unresolved false-alert or unreadable-stale-state result blocks deployment.

## How It Works

**Why receive-only?** A tile never registers to a mobile network or reports who read a warning. Its public, persistent display needs no visitor account, handset or subscription, and can run through a local grid failure if its panel and battery survive. This is not absolute privacy (a site or installer may be observed), and it cannot acknowledge receipt or summon help. Unlike a conventional radio in a private home, one maintained tile can make the *same* locally relevant notice visible at a shared entrance. NOAA's SAME receivers already provide geographic filtering and battery-backed alerts in their service area; the differentiator here is a public, signed-text display with an explicit stale state, not the invention of broadcast warnings.[5]

1. An authorized authority issues a CAP warning with issuer, area, effective/expiry times, language, instruction and update/cancel references.[3] A separately managed, backed-up gateway validates its provenance and converts only permitted fields to a bounded packet. It signs that *exact* canonical byte sequence; the transmitter repeatedly broadcasts it in locally lawful sub-GHz spectrum. CAP alone does not make an unsigned source authentic, and signing a forged upstream message would not fix it.
2. A fixed-site antenna and receive-only front end demodulate the packet. Firmware rejects oversized or malformed fields, unknown issuers, failed signatures and duplicate/replayed versions; a provisioned site-area code is matched locally, without GPS or location transmission. At a boundary, installers configure all relevant areas and verify them in drills.
3. A trusted local clock and update history determine whether the bulletin is current. Signed cancellations supersede the referenced warning; a silence button, if added, must never clear it. The e-paper shows the issuer, instruction and verification time, or prominently shows **STALE / UNVERIFIED — CHECK OTHER CHANNELS** when time, trust or reception cannot be established. A dead battery cannot drive a warning light, so visual status is not a guarantee of safety.

## Technical Architecture

`Authority CAP feed → independently operated validator/gateway → signed compact packet → backed-up regional transmitter(s) → fixed antenna/RX front end → bounded decoder → signature + clock + area + lifecycle checks → e-paper/status button`

The gateway maintains a documented mapping of CAP update, cancel, severity and multilingual fields; it must not silently change meaning to fit a narrow link.[3] The tile stores pinned issuer public keys, a monotonic update journal and the last verified bulletin. Signed rotations can travel on the same downlink, but a missed revocation needs a supervised physical service visit. Firmware updates use a local, authenticated service interface with rollback protection, not a network uplink. Signed payloads, not the LoRa modulation itself, establish provenance. Distinct transmitter power and backhaul arrangements matter: two repeaters sharing one gateway or feed are not independent redundancy.

At the component figure in the original concept, a continuously listening 3.3 V × 4.6 mA radio uses **0.364 Wh/day**; adding 10 mW average overhead gives **0.604 Wh/day** before display and losses.[2] The **1 Wh/day** system allowance, 6 Wh usable reserve and 2 Wp panel in the original budget are *unverified design assumptions*, not field results. Continuous listening avoids missing brief packets but sacrifices the microamp standby figures possible with scheduled wake windows; any duty-cycling proposal must first prove timely reception across clock drift, repeated transmissions and outages. E-paper retains a last image with no power, making a separate fail-visible inspection practice indispensable.

## Performance Benchmarks

These are proposed acceptance tests, not measurements or certification. Compare like-for-like at the same sites and alert issuance times; include transmitter outages in the denominator.

| Metric and method | Existing baseline | Tile target / decision gate |
| --- | --- | --- |
| Delivery: authority issuance to *verified* display, matched packets at a site | Measure the local NOAA SAME/radio and phone-warning channels in paired drills; their networks and message formats differ.[5] | ≥95% within 60 s at independently surveyed covered sites, across 100 non-urgent drill bulletins; no unconditional 60 s promise. |
| Relevance and trust: seeded out-of-area, tampered and replayed packets | SAME filters programmed geographic codes, but is not this project's signature scheme.[5] | Zero seeded invalid packets rendered as verified in 1,000 negative tests; measure false rejection separately. This sample cannot establish zero real-world risk. |
| Energy: full unit, aged cell, winter shade, display updates | Original component-only radio estimate: 0.364 Wh/day.[2] | ≤1 Wh/day averaged across a representative month; ≥6 days nominal without sun at 6 Wh *usable* reserve, then cold/aged-cell retest. |
| Cost and usability: audited purchase/installation and observed recall | Compare actual site costs and recall against radio, sirens and outreach, not handset price alone. | US$85 ex-factory + US$35 installation at 100,000 units/year; ≥80% correct stale/current distinction in a representative, accessible pilot before scale. |

## Deployment Scenarios

- **Floodplain clinic or market:** A local emergency office already issuing CAP messages signs short evacuation instructions for a publicly accessible tile. Staff retain radio and door-to-door plans; power, mounting height, language and antenna reception are surveyed before drills.
- **Coastal school or shelter:** A backed-up transmitter sends tsunami or storm updates while cell sites or mains are unavailable. Teachers and wardens use a signed notice as one input to their established evacuation protocol, with redundant siren or human warning.
- **Remote valley community:** Several tiles share an authority-operated downlink, with separately backed-up coverage where terrain blocks reception. Trained maintainers inspect solar harvest and readable stale states monthly; sites with no viable RF path do not get a tile marketed as protection.

## Vision for 2050

In a conditional 2050 scenario, public entrances have inexpensive, repairable bulletin tiles interoperating with local authoritative feeds, maintained alongside sirens and outreach rather than displacing them. Open alert formats, audited keys and accessible local-language templates could let one signed instruction reach visitors without registering their presence. That future depends on funded transmitters, trusted authorities, durable maintenance and demonstrated behavior change; an unpowered or stale display still means **check another channel**, never “all clear.”

## Sources

[1] https://www.itu.int/en/ITU-D/Emergency-Telecommunications/Pages/Multi-hazard-early-warning-systems.aspx
[2] https://www.semtech.com/products/wireless-rf/lora-connect/sx1262
[3] https://docs.oasis-open.org/emergency/cap/v1.2/CAP-v1.2-os.html
[4] https://meshtastic.org/docs/introduction
[5] https://www.weather.gov/nwr/usingsame
