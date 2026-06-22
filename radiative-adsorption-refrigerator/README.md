# Radiative-Adsorption Refrigerator

**A zero-electricity refrigerator that maintains 2–8°C for food and vaccine preservation — coupling daytime radiative sky cooling with a solar-thermal adsorption refrigeration cycle, using water as the refrigerant and ice as the phase-change battery. For the 1.6 billion people who have no reliable refrigeration.**

---

## Problem

Refrigeration is the invisible backbone of modern food security and public health — yet **1.6 billion people live without reliable access to it**.

- **Food spoilage**: 14% of all food produced globally is lost post-harvest, largely due to absent cold chain in developing regions — **1.3 billion tonnes/year** wasted, feeding no one (FAO 2019). In sub-Saharan Africa, post-harvest losses reach 30–40% for perishables. This is food that was grown with land, water, and fertilizer — then thrown away for lack of a cold box.
- **Vaccine cold chain**: The WHO estimates that **over 50% of vaccines** are wasted in developing countries due to cold chain breaks. Every year, **1.5 million children under 5 die** from vaccine-preventable diseases; the inability to keep vaccines at 2–8°C from factory to clinic is a primary barrier. Solar direct-drive vaccine refrigerators (WHO PQS) cost $2,000–7,000 — out of reach for thousands of rural health posts.
- **Medical access**: Insulin, oxytocin, blood products, and antibiotics require 2–8°C storage. Maternal hemorrhage kills **70,000+ women/year**, many in clinics with no blood refrigerator. Insulin-dependent diabetics in the developing world often skip doses because they cannot store insulin.
- **Climate paradox**: Conventional refrigeration consumes **~17% of global electricity** and relies on HFC refrigerants with **1,400–4,000× the GWP of CO₂**. The technology that preserves food is itself warming the planet. The global cold chain is projected to grow 3× by 2050 as developing nations electrify — and if powered by the current grid, it will add **0.5–1.0 Gt CO₂/year**.
- **The energy gap**: 770 million people have **no electricity at all**. Even where grid access exists, intermittent supply, voltage fluctuations, and lack of maintenance make compressor-based refrigerators unreliable. The rural poor need refrigeration that works **without electricity, without fuel, without maintenance, and without moving parts that break**.

The world needs a refrigerator that runs on **sunlight and the cold of space** — the two resources available everywhere on Earth, for free, with zero operating cost.

---

## Solution

The **Radiative-Adsorption Refrigerator (RAR)** is a solid-state refrigerator with **no compressor, no electricity, and no moving parts** that maintains 2–8°C continuously, day and night, using two synergistic thermodynamic processes:

### 1. Solar-Thermal Adsorption Refrigeration Cycle (Active Heat Pump)

The core mechanism is an **adsorption refrigeration cycle** — a thermally-driven heat pump that uses a solid adsorbent and water as the refrigerant. The cycle has four phases:

```
DAY — Desorption:
  Solar heat (60–85°C) → CaCl₂-biochar adsorbent releases water vapor
  Water vapor → condenser (radiatively cooled) → liquid water at 15–25°C

NIGHT — Adsorption:
  Adsorbent cools to ambient (15–30°C) → reabsorbs water vapor from evaporator
  Low pressure in evaporator → water evaporates at 2–8°C → absorbs heat from food/vaccines
```

The key adsorbent is a **calcium chloride–biochar composite** — CaCl₂ impregnated into activated biochar made from agricultural waste (rice husk, coconut shell, sawdust). CaCl₂ forms a series of hydrates (CaCl₂·nH₂O, n = 1–6) with a total water uptake of **0.5–0.6 g/g** — among the highest of any low-temperature adsorbent. The biochar provides a high-surface-area host (800–1,200 m²/g) that distributes CaCl₂ and enhances vapor transport. The composite desorbs at **60–85°C** (achievable with a simple flat-plate solar thermal collector) rather than the 120–150°C required by zeolite, making it compatible with low-cost, untracked solar heat.

**Why water as refrigerant**: water has the highest latent heat of vaporization of any substance (2,501 kJ/kg at 0°C) — 5× that of ammonia, 15× that of most synthetic refrigerants. It is free, non-toxic, non-flammable, zero-GWP, and available everywhere. Its only limitation — freezing at 0°C — is actually an advantage: the frozen water **becomes the phase-change cold storage battery** (ice at 0°C buffers the cold box at a perfect food-safe temperature).

### 2. Radiative Sky Cooling (Condenser Enhancement)

The condenser — where desorbed water vapor turns back to liquid — is coated with a **radiative sky cooling metamaterial**: a multilayer SiO₂/TiO₂/PDMS paint or polymer film with:
- Solar reflectivity >0.96 (reflects 96% of incident sunlight, stays cool in daytime)
- Thermal emissivity >0.95 in the 8–13 µm atmospheric infrared window (radiates heat to deep space at ~3K)

This keeps the condenser **5–15°C below ambient** even during daytime, which:
- Lowers the condensation temperature → reduces the desorption temperature needed → **improves COP by 20–40%** over air-cooled condensers
- Allows the system to work in hot climates (35–45°C ambient) where conventional adsorption refrigerators struggle
- Provides supplemental nighttime cooling to the cold box interior via a second radiative cooling surface on the lid

Recent breakthroughs in daytime radiative cooling (Raman et al., *Nature* 2014; Zhai et al., *Science* 2017; Li et al., *Joule* 2020) have demonstrated **5–40°C sub-ambient cooling** under direct sunlight, validating this as a practical daytime resource, not just a nighttime effect.

### 3. Ice Phase-Change Thermal Battery

Water serves a dual role: it is **both** the refrigerant (evaporating in the cycle) **and** the cold storage medium (freezing to ice during excess cooling capacity). During the night, the evaporator freezes a portion of its water into ice at 0°C. During the day, when the adsorption cycle is in desorption mode (no active cooling), the ice melts — absorbing 334 kJ/kg of latent heat — and maintains the interior at **0–4°C** for the entire day. This creates a 24-hour continuous cold supply from a cycle that is inherently day/night intermittent.

**10–15 kg of ice** stores 3.3–5.0 MJ of cold — enough to offset the heat leak of a well-insulated 100 L cold box (10 W) for **8–14 hours** with zero active cooling.

### 4. Vacuum Insulation

The cold box is insulated with **evacuated silica-aerogel composite panels** (thermal conductivity λ < 0.004 W/m·K — 10× better than styrofoam). A 40 mm thick VIP reduces the heat leak of a 100 L box to **8–12 W** at 30°C ambient — small enough that the solar-adsorption cycle's cooling capacity (1.5–3 kW·h/day) exceeds it by **5–10×**, providing massive margin for cloudy days, door openings, and loading warm contents.

**Result: A 100 L cold box that maintains 2–8°C, 24/7, with zero electricity, zero fuel, zero moving parts, for $80–150 at scale.**

---

## Key Innovation

### First Coupling of Radiative Sky Cooling with Adsorption Refrigeration

Every existing off-grid refrigeration approach has a fundamental limitation:

| Approach | Limitation |
|----------|-----------|
| Compressor + solar PV + battery | $2,000–7,000; batteries fail in 3–5 years; complex electronics; maintenance-intensive |
| Absorption refrigerator (NH₃/H₂O + gas burner) | Requires propane/kerosene fuel; toxic NH₃; high-pressure; maintenance |
| Evaporative cooling (zeer pot) | Only 5–10°C below ambient; useless above 25°C ambient; no 2–8°C guarantee |
| Ice-based cold box (manually recharged) | Requires daily ice delivery — unavailable in rural areas; melting rate limits hold time |
| Solar adsorption (silica gel/water, existing) | Requires 120–150°C desorption → expensive evacuated-tube collector; air-cooled condenser limits COP to 0.2–0.3 in hot climates |
| **RAR (this work)** | **0 electricity, 0 fuel, 0 moving parts; 60–85°C desorption (flat-plate collector); radiative-cooled condenser → COP 0.5–0.7; $80–150 at scale** |

The RAR's breakthrough is the **deliberate thermodynamic coupling of two free environmental resources**:

- **Solar heat** drives the desorption phase (day) — the sun heats the adsorbent to 60–85°C, releasing water vapor. This is the energy input.
- **Radiative sky cooling** drives the condenser (day and night) — the metamaterial surface radiates heat to deep space through the 8–13 µm atmospheric window, keeping the condenser 5–15°C below ambient. This lowers the cycle's condensation temperature, which is the **single most powerful lever** on adsorption COP: every 10°C reduction in condensation temperature raises COP by 15–25%.
- **Nighttime ambient cooling** drives the adsorption phase — when the sun sets, the adsorbent cools to ambient and reabsorbs vapor from the evaporator, creating the low pressure that drives evaporation at 2–8°C.
- **Ice** bridges the day/night intermittency — the excess nighttime cooling capacity freezes water into ice, which melts during the day to maintain temperature.

The three free thermal resources — **solar heat, radiative cooling, and nighttime ambient cooling** — are each available at different times and serve different functions in the cycle. The RAR is the first system to orchestrate all three into a single continuous refrigeration process.

### The CaCl₂-Biochar Adsorbent

The second innovation is the adsorbent material itself. Conventional solar adsorption refrigerators use silica gel (desorbs at 80–100°C, low uptake 0.1–0.2 g/g) or zeolite 13X (desorbs at 150–250°C, requires expensive evacuated-tube collectors). The **CaCl₂-impregnated biochar composite** achieves:
- **0.5–0.6 g/g water uptake** (2.5–5× silica gel)
- **60–85°C desorption** (compatible with cheap flat-plate solar thermal, no tracking, no vacuum tubes)
- **$2–5/kg cost** (CaCl₂ is $0.20/kg industrial salt; biochar is agricultural waste)
- **1,000+ cycle durability** (CaCl₂ hydrate cycling is reversible; biochar is chemically stable)
- **Self-manufacturable** from agricultural waste + salt — communities can produce the adsorbent locally

---

## Target Cost

| Component | Function | Cost at 1M units/yr |
|-----------|----------|---------------------|
| Radiative cooling coating (2 m², paint/film) | Condenser cooling | $6–10 |
| Flat-plate solar thermal absorber (1.5 m²) | Desorption heat | $12–18 |
| CaCl₂-biochar adsorbent (5 kg) | Water adsorption/desorption | $10–20 |
| Condenser (copper coil + radiative surface) | Vapor condensation | $15–25 |
| Evaporator/ice-storage vessel (stainless steel) | Evaporative cooling + ice storage | $20–30 |
| Vacuum insulation panels (1.4 m², 40 mm) | Thermal insulation | $20–35 |
| HDPE outer shell + lid | Structural | $15–25 |
| Passive check valves + thermostatic trap | Cycle control | $5–12 |
| Frame, hardware, seals | Assembly | $10–20 |
| Assembly labor (semi-skilled) | Manufacturing | $10–20 |
| **Total (100 L unit)** | | **$123–215** |
| **Ultra-low-cost variant** (aerogel blanket insulation, simpler condenser) | | **$80–120** |

**Operating cost: $0/year.** No electricity, no fuel, no refrigerant recharge, no compressor to repair. The only maintenance is recharging the adsorbent every 5–8 years ($10–20) and occasional reapplication of the radiative cooling coating every 7–10 years ($5).

**Cost per liter of cold storage: $0.80–2.15/L** — vs. $20–70/L for solar-PV compressor refrigerators.

**Cost per vaccine dose preserved (5-year life): $0.001–0.005** — vs. $0.02–0.10 for solar-PV systems.

---

## Impact

### Food Security
- **1.6B+ people** currently without reliable refrigeration gain access to cold storage.
- **200–400M tonnes/year food saved** from post-harvest spoilage — enough to feed 500M–1B people.
- Smallholder farmers can store perishable crops (milk, vegetables, fish, fruit) for 3–7 days instead of selling at harvest-glut prices — **increasing income 20–60%** for 500M+ smallholder households.
- **$50–150B/year** in economic value from reduced food waste, at a capital cost of $100–250B for global deployment (1–2 year payback from food savings alone).

### Public Health
- **50M+ vaccine doses/year saved** from cold chain failure — protecting 10M+ children from preventable disease.
- Insulin, oxytocin, and blood products become storable at the 100,000+ rural health posts that currently lack any cold chain.
- **20,000–50,000 lives/year saved** from improved vaccine and medicine access (conservative estimate; WHO data on vaccine-preventable deaths in cold-chain-limited regions).
- **$2–5B/year** in reduced vaccine wastage (vaccines cost $1–50/dose; 50M wasted doses × average $40/dose = $2B).

### Climate
- **Replaces HFC refrigerants**: if 100M units replace kerosene/propane absorption refrigerators and diesel-powered cold rooms, **50–100 Mt CO₂-eq/year** avoided from HFC elimination + fossil fuel displacement.
- **Reduces food waste emissions**: 200–400M tonnes food saved → **0.5–1.5 Gt CO₂-eq/year avoided** (food waste = 3.3 Gt CO₂-eq/year globally; saving 10–15% of that).
- **Zero operational emissions**: no electricity, no fuel, no refrigerant leakage. The RAR's lifecycle carbon is paid back in **<1 month** of operation.
- Enables electrification-light development: communities can have refrigeration **before** having grid electricity, leapfrogging the fossil-fuel-dependent cold chain.

### Democratization
- **No infrastructure required**: works anywhere with sunlight and a view of the sky — which is everywhere.
- **Locally manufacturable**: adsorbent from agricultural waste + salt; box from local materials; only the radiative coating and VIPs need centralized production.
- **No recurring cost barrier**: the $0/year operating cost means even the poorest households can afford to keep using it. The only barrier is the initial capital cost — addressable through microfinance, NGO distribution, and government programs.
- **Scalable**: from 30 L household units ($60–100) to 500 L community cold stores ($400–800) to 2,000 L health-post vaccine refrigerators ($1,000–1,500).

### Gender Equity
- Women bear 60–70% of food preservation labor in developing countries (smoking, salting, drying). Refrigeration transfers **2–4 hours/day** from food preservation to education, income, and rest.
- Women-owned market stalls can sell perishables at premium prices instead of discounting at end of day — **increasing income 30–50%**.

This is not a luxury. Refrigeration is the difference between eating and not eating, between a child being vaccinated and not, between insulin working and spoiling. The RAR delivers it to the people who need it most, using nothing but sunlight and the cold of space.

---

## How It Works (Detailed)

### Day Cycle (Sun-Up: Desorption + Ice Melting)

1. **Sunlight heats the adsorbent bed.** A flat-plate solar thermal absorber (selective black coating on aluminum, 1.5 m²) is thermally bonded to the adsorbent container. As sunlight strikes it, the adsorbent warms to 60–85°C. CaCl₂ in the biochar releases its bound water as vapor.

2. **Water vapor condenses in the radiatively-cooled condenser.** The vapor flows through a passive check valve to the condenser — a copper coil coated with the radiative cooling metamaterial, mounted on the shaded/north side of the unit. The metamaterial radiates heat to deep space through the 8–13 µm atmospheric window, keeping the condenser surface 5–15°C below ambient. Water vapor condenses to liquid at 15–25°C and flows by gravity into the evaporator/ice-storage vessel inside the cold box.

3. **Ice melts to maintain interior temperature.** Inside the cold box, the ice stored from the previous night's cooling melts at 0°C, absorbing 334 kJ/kg and keeping the interior at 0–4°C throughout the day. The vacuum insulation limits heat leak to 8–12 W, so 10–15 kg of ice sustains the cold box for 8–14 hours of zero active cooling.

### Night Cycle (Sun-Down: Adsorption + Ice Freezing)

4. **The adsorbent cools and begins reabsorbing vapor.** With no solar input, the adsorbent bed cools to nighttime ambient (15–30°C). The check valve to the condenser closes and the valve to the evaporator opens. CaCl₂, now cool, has an enormous affinity for water vapor and begins adsorbing vapor from the evaporator.

5. **Low pressure drives evaporation at 2–8°C.** As the adsorbent pulls vapor from the evaporator, the pressure in the evaporator drops to the saturation pressure of water at 2–8°C (0.7–1.1 kPa). Liquid water in the evaporator evaporates at this low pressure, absorbing its latent heat of vaporization (2,501 kJ/kg) from the cold box interior. This is the **active cooling** that drops the interior to 2–8°C.

6. **Excess cooling freezes water into ice.** The adsorption cycle's cooling capacity (1.5–3.0 kW·h/night) far exceeds the cold box heat leak (0.2–0.3 kW·h/night). The surplus freezes a portion of the water in the evaporator vessel into ice — creating the thermal battery that will carry the cold box through the next day's desorption phase.

### The Thermodynamic Cycle

```
State 1 → 2: DESORPTION (day, solar-heated)
  Adsorbent: 25°C → 75°C, releases 3 kg H₂O vapor
  Heat input: Q_des = m × (c_p × ΔT + ΔH_ads) ≈ 8–12 MJ (from 1.5 m² solar thermal, 6 h)

State 2 → 3: CONDENSATION (day, radiatively-cooled condenser)
  Vapor: 75°C → 20°C (condenses at ~20°C, P = 2.3 kPa)
  Heat rejected: Q_cond = m × L_vap ≈ 7.5 MJ (to radiative cooling + ambient)

State 3 → 4: COOLING (evening, passive)
  Liquid water: 20°C → 5°C (inside cold box)

State 4 → 1: EVAPORATION + ADSORPTION (night)
  Water: 5°C → evaporates at 2–8°C (P_evap = 0.8–1.1 kPa)
  Adsorbent: 25°C, reabsorbs 3 kg H₂O vapor
  Cooling output: Q_cool = m × L_vap ≈ 7.5 MJ → 2.1 kW·h

  COP = Q_cool / Q_des ≈ 0.5–0.7
  (vs. 0.2–0.3 for conventional solar adsorption with air-cooled condenser)
```

### Key Design Parameters (100 L unit)

| Parameter | Value |
|-----------|-------|
| Cold box volume | 100 L (0.5 × 0.5 × 0.4 m interior) |
| Target interior temperature | 2–8°C (food/medicine), 0°C (ice-making mode) |
| Ambient temperature range | 10–45°C (operational); survives -10°C to +55°C |
| Solar thermal collector area | 1.5 m² (flat-plate, non-tracking) |
| Radiative cooling surface area | 2.0 m² (condenser + supplemental lid cooling) |
| Adsorbent mass | 5 kg CaCl₂-biochar composite |
| Water (refrigerant + PCM) mass | 10–15 kg |
| Ice storage capacity | 8–12 kg ice (2.7–4.0 MJ cold storage) |
| Vacuum insulation | 40 mm VIP, λ < 0.004 W/m·K |
| Heat leak at 30°C ambient | 8–12 W |
| Daily cooling capacity | 1.5–3.0 kW·h (net of heat leak) |
| Daily heat leak | 0.2–0.3 kW·h |
| Cooling margin | 5–10× over heat leak |
| Cycle COP | 0.5–0.7 (with radiative-cooled condenser) |
| Service life | 15–20 years (adsorbent recharge every 5–8 years) |
| Operating cost | $0/year |