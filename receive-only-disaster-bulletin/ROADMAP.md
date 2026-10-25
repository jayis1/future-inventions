# Receive-Only Disaster Bulletin — Roadmap

**Author: jayis1** · Proposed milestones, not achieved deployments. Phase timing is relative to project start and depends on an alerting-authority partner. [README](README.md) supplies the design assumptions.

## Concept (years 0–2)

Co-design public-site placement, multilingual notices and stale-state wording with residents and a civil-protection authority. Threat-model the CAP ingestion and signing chain; survey lawful spectrum, existing warning channels and maintenance ownership. Gate: an authority approves a non-urgent drill protocol and user testing shows people distinguish a valid warning from a stale sign before hardware claims are made.

## Prototype (years 3–5)

Build a sealed e-paper tile with a hardware-disabled transmit path, 2 Wp panel and replaceable cell; publish the signed packet format, test vectors and key-recovery procedure. Bench-test malformed packets, forged updates/cancellations, resets, shadowing, cold-aged battery and six sunless days at the 1 Wh/day design allowance. Gate: independently reproduce receive-only RF, bounded parsing and fail-visible behavior; revise energy and cost targets from measurements.

## Pilot (years 5–10)

With a named local authority once recruited, place paired trial tiles at clinics, schools and shelters, alongside—not instead of—sirens and radio. Run at least 100 non-urgent drills, including accessibility sessions, compare issuance-to-display times and correct action against existing channels, and record transmitter and maintenance costs. Gate: covered sites achieve the README's ≥95% within-60-second target and ≥80% correct stale/current distinction without unacceptable false alerts; otherwise redesign.

## Scale (years 10–20)

Only after pilot evidence and jurisdiction-specific regulatory review, qualify repairable enclosures, key custody, replacement batteries, local translations and independent power/backhaul for transmitters. Audit the proposed US$85 factory and US$35 installation targets at 100,000 units/year rather than treating them as supplier quotes. Gate: funded multi-year upkeep, documented key rotation/revocation and verified total delivered-and-understood warning cost versus alternatives.

## Ubiquity (2050 scenario)

If repeated evaluations show incremental benefit, maintain an open, receive-only public endpoint as one layer of local warning infrastructure, not a universal substitute for personal alerts or responders. Fund periodic site inspections, accessible redesign and end-of-life recycling; publish failures and sunset tiles where radio or outreach works better. Gate: independently measured warning comprehension and action improve equitably over a maintained baseline, with privacy and physical one-way behavior intact.
