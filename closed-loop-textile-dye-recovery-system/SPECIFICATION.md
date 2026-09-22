# Closed-Loop Textile Dye Recovery System — Technical Specification

- **Author:** jayis1
- **Revision:** Concept 0.1
- **Nominal capacity:** 100 m³/day
- **Intended site:** segregated textile wet-processing wastewater

## 1. Scope and Design Principle

CTDRS recovers water and process chemicals from known dyehouse batches. It is not a universal end-of-pipe purifier and must not accept an unknown mixed industrial sewer. The control principle is **identify, segregate, recover, verify, then reuse**. If identity or quality cannot be proven, the system fails closed to quarantine.

## 2. Feed Envelope

| Parameter | Normal design range | Action outside range |
|---|---:|---|
| Flow | 25–100 m³/day | Equalize or add parallel module |
| Temperature | 20–60°C | Recover heat; cool to membrane limit |
| pH | 4–12 | Segregate; controlled neutralization |
| Conductivity | 2–80 mS/cm | Recipe-specific ED current limit |
| COD | 200–3,000 mg/L | >3,000 mg/L to high-strength hold tank |
| Suspended solids | <1,000 mg/L raw | Ceramic microfiltration pretreatment |
| Oil and grease | <50 mg/L | Above limit to oil-separation pretreatment |
| Free chlorine | <0.1 mg/L at NF | Quench before polymeric membrane |

Separate campaigns are required for reactive/direct dyes, disperse dyes, sulfur dyes, vat dyes, pigment printing, metal-complex dyes, and finishing baths. Streams containing chromium, copper, fluorinated finishes, formaldehyde resins, silicone oils, or unknown biocides remain quarantined until a validated route exists.

## 3. Process Flow

```text
Dyehouse batch manifest
        |
        v
Equalization and spectral classification
        |
        v
Heat recovery -> ceramic microfiltration -> guarded loose nanofiltration
                                             |                  |
                                      dye concentrate       salt-rich permeate
                                             |                  |
                                  qualify for reuse?       electrodialysis
                                      |       |             |            |
                                     yes      no       reusable salt   dilute water
                                      |       |             |            |
                                 blend tank   +----> oxidation cell       |
                                                       |                 |
                                                       +--> carbon polish+
                                                                         |
                                                           release analytics
                                                                |       |
                                                             reuse   quarantine
```

## 4. Subsystems and Materials

### 4.1 Equalization and classification

- Two 60 m³ glass-lined steel or HDPE tanks allow one batch to be characterized while the other feeds treatment.
- Sensors: PT100 temperature, ISFET pH, toroidal conductivity, ORP, turbidity, differential UV-visible spectrometer (200–800 nm), and total-organic-carbon or calibrated UV254 COD proxy.
- Every batch receives an immutable local identifier linked to the dye recipe. The control system stores process-chemistry records only, not worker biometrics or personal activity data.

### 4.2 Solids removal

- 100–300 µm rotary screen followed by 0.1–0.2 µm silicon-carbide or alpha-alumina crossflow ceramic membrane.
- Design flux: 80–180 L/m²/h after feed-specific pilot testing.
- Backpulse with recovered water; alkaline and enzymatic clean-in-place (CIP) selected from foulant analysis.
- Captured fibers are dewatered and characterized before recycling, energy recovery, or licensed disposal.

### 4.3 Dye/salt fractionation

- Guarded loose nanofiltration, nominal molecular-weight cutoff 500–1,000 Da.
- Membrane candidate: chemically resistant polyethersulfone support with cross-linked polyelectrolyte or polyamide selective layer; ceramic NF remains a high-temperature option.
- Operating target: 4–12 bar, 15–35 L/m²/h, 70–85% stage recovery.
- Acceptance target for qualified reactive/direct-dye feed: >99% dye rejection with <20% monovalent-salt rejection. Selection is determined by measured rejection, not membrane label.
- Diafiltration is used only when the value of dye recovery exceeds additional water and energy use.

### 4.4 Salt, acid, and base recovery

- Conventional electrodialysis first concentrates NaCl or Na2SO4 using monovalent-selective ion-exchange membranes where appropriate.
- A controlled BMED side loop uses a bipolar membrane plus cation- and anion-exchange membranes to produce dilute acid and alkali for pH control or CIP.
- Design targets: 70–85% salt recovery, >80% current efficiency, <1.5 kWh/m³ feed for the ED/BMED section under normal salinity.
- Recovered chemistry is reused only after concentration, metal, color, and organic-carbon checks.

### 4.5 Dye qualification

A recovered dye lot must pass:

1. UV-visible spectral similarity against the recipe standard;
2. HPLC or capillary-electrophoresis impurity profile;
3. conductivity, pH, TOC, and metal limits;
4. laboratory strike on standardized fabric;
5. CIELAB color difference target Delta E00 <= 1.0 after recipe correction; and
6. wash-fastness comparison to virgin-dye control.

Lots that fail are never diluted into a passing lot. They move to destruction or licensed disposal.

### 4.6 Residual oxidation and polishing

- Divided flow-through cell with Ti4O7 Magnéli-phase porous anode as the cost target; BDD-coated niobium is the durability reference.
- Stainless-steel or gas-diffusion cathode; 50–200 A/m² adjustable current density.
- Oxidation runs after NF and desalting to minimize volume and chloride concentration.
- Granular activated carbon or characterized biochar removes residual organics; exhausted media is regenerated where contaminant analysis permits.
- Automatic stop limits include excessive cell voltage, temperature, off-gas, halogen residual, or byproduct trend.

## 5. Water-Release Gate

No valve to production opens unless all required signals are valid and two independent quality layers agree.

| Measurement | Design release target |
|---|---:|
| COD | <50 mg/L or stricter local/process limit |
| Apparent color | <10 Pt-Co or process-specific limit |
| Turbidity | <1 NTU |
| Conductivity | Recipe-specific |
| pH | 6.5–8.5 or process-specific |
| Acute aquatic toxicity | No unacceptable effect at required dilution |
| Chlorate/perchlorate/AOX | Below locally applicable limits and pilot-derived reuse limits |
| Mass balance | 95–105% closure for water and tracked salts |

An automated result is provisional. Scheduled laboratory confirmation is required, with greater frequency during commissioning or chemistry changes.

## 6. Controls and Fail-Safe States

- Safety-rated PLC controls pumps, valves, current, pressure, and quarantine routing.
- The recipe optimizer may recommend settings but cannot bypass hard pressure, temperature, chemical, or release limits.
- Loss of batch identity, critical sensor disagreement, calibration expiry, power, or communication closes the reuse valve.
- Local operation remains available without internet. Remote access uses signed updates, least-privilege accounts, and an operator-controlled service window.
- Manual sampling ports are placed before and after every separation stage.

## 7. Mass and Energy Targets

Reference case per 100 m³ feed:

| Output or demand | Target range |
|---|---:|
| Reuse water | 90–95 m³ |
| Fresh-water makeup | 5–10 m³ |
| Recovered salt, relative to qualified input | 70–85% |
| Recovered dye, relative to qualified input | 60–80% |
| Residual liquid concentrate | <=3 m³ before dewatering |
| Whole-system electricity | <300 kWh (<3 kWh/m³) |
| Membrane/CIP water | included in 5–10 m³ makeup |

These values exclude unusual high-strength waste and upstream thermal energy. Every pilot report must publish boundaries and avoid crediting heat or chemicals twice.

## 8. Fouling and Maintenance

- Schedule segregated low-foulant rinses between incompatible colors.
- Use pressure-normalized permeability and salt/dye rejection trends to trigger CIP rather than a fixed calendar alone.
- Limit irreversible flux loss to <15% over 500 operating hours in the pilot gate.
- Inspect ceramic seals quarterly; verify polymeric NF integrity weekly by marker/rejection tests.
- ED polarity reversal and pulsed current reduce scaling; membrane stacks are inspected at 2,000-hour intervals during pilots.
- Electrodes are weighed and surface-characterized at 1,000-hour intervals until lifetime models are validated.

## 9. Safety and Environmental Controls

- Enclose high-voltage/current buses, interlock cabinet doors, bond wet-process equipment, and provide residual-current protection.
- Vent and monitor oxidation-cell off-gas. Never rely on odor to detect chlorine or volatile organics.
- Analyze chlorate, perchlorate, AOX, target volatile/semi-volatile byproducts, metals, and acute toxicity before reuse or discharge.
- Maintain secondary containment for all tanks and chemical-recovery vessels.
- Characterize lint, sludge, carbon, and scale under local waste rules; “recovered” is not synonymous with safe.
- Food, drinking-water, pharmaceutical, and worker-contact uses are outside scope unless separately certified.

## 10. Validation Plan

### Stage A — Bench campaigns (0.1–1 m³/day)

Test at least six dye classes and three real dyehouse matrices. Build membrane-rejection maps versus pH, ionic strength, temperature, and auxiliary chemistry. Identify oxidation byproducts with ion chromatography and high-resolution mass spectrometry.

### Stage B — Slipstream pilot (1–5 m³/day)

Operate >=2,000 hours at one dyehouse. Validate flux, CIP recovery, energy, byproducts, toxicity, and color reproducibility. No closed-loop reuse in production until release criteria remain stable.

### Stage C — Demonstration (20–30 m³/day)

Run segregated light- and dark-shade campaigns at two factories. Complete 100 recovered-dye strike tests and quantify product reject rate, membrane life, worker procedures, and residual disposal.

### Stage D — Full module (100 m³/day)

Demonstrate 12 months continuous operation at three sites using different dominant dye classes. Third parties audit water, salt, dye, energy, toxicity, and economics.

### Commercial gate

Commercial claims require all of the following: >=90% water reuse for the validated feed envelope, <3 kWh/m³ normal-feed energy, no increase in measured acute toxicity, compliant oxidation byproducts, >=80% on-stream availability, and lifecycle cost within US$1.50–3.00/m³ before recovery credits.

## 11. Known Research Questions

1. Which loose-NF surface chemistries preserve dye/salt selectivity after thousands of cleaning cycles?
2. Can inline spectroscopy predict blend quality across fluorescent and multi-component dyes without routine HPLC?
3. When is Ti4O7 preferable to BDD after electrode lifetime and byproduct formation are included?
4. What chloride threshold and current waveform minimize chlorate, perchlorate, and AOX while maintaining mineralization?
5. Which recovered-water quality tier is safe for each dyehouse operation, from first wash through light-shade dyeing?
6. Can shared industrial-cluster ownership achieve the target economics without transferring pollution to an under-regulated central site?

## 12. End of Life

The skid uses bolted stainless-steel or coated-steel frames, replaceable membrane cassettes, and separable electrical cabinets. Ceramic housings and steel are recycled; ion-exchange and polymeric membranes follow manufacturer take-back or controlled energy-recovery routes; electrodes are returned for recoating; and spent carbon, sludge, and scale are handled according to measured contaminants. No stream is marketed as a product without a specification and buyer.
