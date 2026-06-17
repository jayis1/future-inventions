# APTP — Engineering Specification v2.0

## 1. System Architecture

### 1.1 Physical Enclosure

| Parameter | Specification |
|-----------|--------------|
| Form factor | 1.8 m H × 0.8 m W × 0.7 m D (standard lab refrigerator footprint) |
| Mass | 85 kg (with reagent cartridges installed) |
| Power | 500W continuous (220V AC / 110V AC / 24V DC solar input) |
| Operating temperature | 15–35°C ambient |
| Operating humidity | 20–80% RH (non-condensing) |
| Containment | ISO Class 7 (Class 10,000) HEPA-filtered internal work area; negative pressure enclosure (−15 Pa relative to room) |
| User interface | 15" capacitive touchscreen; voice-guided workflow for low-literacy settings; multi-language (20+ at launch); colorblind-accessible UI |
| Connectivity | 4G/LTE, Wi-Fi 6, Ethernet, Bluetooth LE; offline-capable with local AI inference (all critical functions operational without internet) |
| Certification targets | CE Mark (IVDR Class C), FDA 510(k) (as a combination product: device + biologic), ISO 13485 (QMS), ISO 14644 (cleanroom) |

### 1.2 Subsystem Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    APTP Enclosure (ISO 7)                    │
│                                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │ Pathogen  │  │  Phage   │  │   AI     │  │  Cell-   │  │
│  │Isolation │──│ Discovery│──│Engineering│──│Free Synth│  │
│  │  Module   │  │  Engine  │  │  Module   │  │  Module   │  │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  │
│       │                                          │         │
│       ▼                                          ▼         │
│  ┌──────────┐                            ┌──────────┐      │
│  │ Nanopore │                            │   QC &   │      │
│  │Sequencer │                            │Formulation│     │
│  └──────────┘                            └──────────┘      │
│                                                │            │
└────────────────────────────────────────────────│────────────┘
                                                 ▼
                                          ┌──────────┐
                                          │ Sterile  │
                                          │  Output  │
                                          │ Vials/   │
                                          │ Nebulizer│
                                          └──────────┘
```

### 1.3 Internal Data Bus

| Bus | Protocol | Bandwidth | Devices |
|-----|----------|-----------|---------|
| Sensor bus | I²C | 400 kHz | Temperature, pressure, pH, OD sensors |
| Sequencing bus | USB 3.0 | 5 Gbps | Nanopore Flongle × 1, MinION × 1 |
| Microfluidic control | SPI | 10 MHz | Valves, pumps, heaters |
| AI processing | PCIe Gen 4 | 16 GT/s | NVIDIA Jetson Orin |
| User interface | HDMI 2.0 | 18 Gbps | 15" touchscreen |
| Telemetry | TLS 1.3 over LTE | Variable | Cloud sync, remote audit |

---

## 2. Pathogen Isolation & Identification Module

### 2.1 Microfluidic Sample Processing

| Parameter | Specification |
|-----------|--------------|
| Input (clinical) | 100 µL patient swab eluate or 1 mL liquid sample (blood, urine, sputum, CSF) |
| Input (environmental) | 10 mL sewage, river water, soil slurry |
| Processing | Differential centrifugation (3,000 × g, 10 min) → magnetofluidic sorting (antibody-conjugated magnetic beads) → bacterial enrichment → single-cell isolation in 10,000-well microwell array |
| Enrichment factor | 100–500× (pathogen cells vs. host/benign cells) |
| Time | 1 hour from sample to isolated colony |
| Contamination rate | <0.1% cross-contamination between wells |

### 2.2 Rapid Genomic Sequencing

| Parameter | Specification |
|-----------|--------------|
| Platform | Oxford Nanopore Flongle (primary, integrated) + MinION (backup, integrated) |
| Library prep | Rapid barcoding kit (SQK-RBK004); 10-minute automated prep |
| Sequencing | 30-minute run for species/strain ID + resistome |
| Analysis | On-device basecalling (GPU-accelerated Guppy) + ML species ID (custom CNN) + AMR gene detection (PhageFormer AMR sub-model) |
| Output | Species, MLST type, resistome profile (all AMR genes with resistance phenotype predictions), virulence factor list |
| Accuracy | >99.5% species ID, >98% resistome gene detection, >95% strain-level MLST |
| Throughput | Up to 200 Mb/Flongle run (sufficient for 1 bacterial genome at 50× coverage) |

### 2.3 Target Strain Cultivation

| Parameter | Specification |
|-----------|--------------|
| Chambers | 48 parallel microfluidic growth chambers (10 µL each) |
| Atmosphere control | Aerobic / anaerobic / microaerophilic (gas mixing via MEMS valves) |
| Monitoring | Optical density (650 nm LED + photodiode) every 5 minutes; growth rate auto-detection |
| Reporter engineering | Auto-generates luciferase (luxCDABE operon) under constitutive promoter via CRISPR-based knock-in into target strain on-chip |
| Time to sufficient biomass | 4–6 hours (fast-growing organisms) to 12–16 hours (slow-growing organisms) |
| Contamination detection | 16S rRNA qPCR surveillance every 2 hours |

---

## 3. Phage Discovery Engine

### 3.1 Environmental Sample Processing

| Parameter | Specification |
|-----------|--------------|
| Input | 10 mL environmental sample (sewage, river water, soil slurry) |
| Filtration | Sequential: 5 µm (remove debris) → 0.45 µm (remove bacteria) → 0.22 µm (isolate phage-sized particles) |
| Enrichment | 4-hour enrichment culture against target strain (10 mL volume, MOI 0.01) |
| Plaque assay | High-throughput microfluidic (Section 3.2) |
| Alternative phage sources | Pre-loaded reference phage library (freeze-dried, 50 common pathogen-targeting phages); cloud-connected phage database for PhageFormer-guided selection |

### 3.2 High-Throughput Plaque Screening Chip

| Parameter | Specification |
|-----------|--------------|
| Chip material | PDMS (polydimethylsiloxane) on glass, injection-molded |
| Well count | 10,000 nanoliter wells |
| Well volume | 100 nL each (1 µL total reaction volume per well) |
| Detection | Luciferase fluorescence (real-time, >10× signal-to-noise ratio when lysis occurs; excitation 490 nm, emission 520 nm) |
| Throughput | 10,000 wells screened in 30 minutes |
| Hit rate | 0.5–5% of wells show lysis (50–500 candidate phages per run) |
| Recovery | Positive wells flushed to recovery channels via pneumatic valve actuation; phage recovered in 50 µL buffer |
| Cross-contamination prevention | Hydrophobic PDMS barriers between wells; laminar flow isolation in recovery channels |
| Cost per chip | <$1 at 100K units/year |

### 3.3 Candidate Phage Genome Sequencing

| Parameter | Specification |
|-----------|--------------|
| Platform | Oxford Nanopore MinION (dedicated, integrated) |
| Library prep | Automated on-chip DNA extraction (magnetic bead-based) + ligation |
| Sequencing | 1-hour run per batch of 50 phages |
| Assembly | On-device Flye assembler + Medaka polishing (NVIDIA Jetson GPU) |
| Time | 2 hours total from hit recovery to complete phage genome |
| Quality target | >30× coverage, Q20 consensus, >95% completeness |

---

## 4. AI-Guided Engineering Module

### 4.1 Phage Selection Model (PhageFormer)

| Parameter | Specification |
|-----------|--------------|
| Architecture | Modified ESM-2 (protein language model) + custom genome-level transformer |
| Model size | 12 layers, 768 hidden dimensions, 12 attention heads, 110M parameters |
| Training data | 50,000+ annotated phage genomes (NCBI GenBank, PhagesDB, GPD), 200,000+ phage-host interaction records, 10,000+ experimental lysis assays |
| Input | Phage genome sequence (FASTA) + target bacterium genome (FASTA) + resistome profile |
| Output | Lysis probability (calibrated), host range prediction, resistance risk score, lysogenicity prediction, safety flags |
| Performance | AUC > 0.85 on held-out species (target); >0.90 on same-species validation |
| Inference | On-device (NVIDIA Jetson Orin, 40 TOPS, 15W); <30 seconds per cocktail design |
| Cloud backup | Optional cloud inference for complex cases (encrypted, HIPAA-compliant) |
| Update cycle | Monthly model updates via encrypted channel; quarterly full retraining on new phage-host data |
| Explainability | Attention maps, SHAP values, and feature attribution for every prediction (clinician-facing UI shows top contributing genome regions) |

### 4.2 CRISPR Engineering Design

| Parameter | Specification |
|-----------|--------------|
| Target modifications | 1. Host range broadening (tail fiber/RBP domain swap); 2. Anti-resistance (anti-CRISPR proteins, depolymerase enzymes); 3. Lysogeny removal (integrase/repressor deletion); 4. Payload insertion (biofilm-degrading enzymes, sensitizing agents) |
| Design tool | In-silico CRISPR guide RNA designer (Cas12a/Cas9); homology-directed repair template generator; off-target analysis |
| Design time | <30 minutes per phage edit |
| Output | Engineering blueprint (DNA edit coordinates + synthesis plan) in SBOL 3.0 format |
| Validation | In-silico folding prediction (AlphaFold-based) for all engineered structural proteins |

### 4.3 Cocktail Optimization Algorithm

| Parameter | Specification |
|-----------|--------------|
| Objective | Maximize lysis probability × minimize resistance emergence × minimize immunogenicity |
| Constraints | 3–5 phages per cocktail; independent receptor targets; no immunogenic overlap; no lysogenicity; no toxin genes |
| Method | Multi-objective Bayesian optimization (NSGA-II) over PhageFormer predictions |
| Output | Ranked cocktail candidates with predicted clearance probability, resistance timeline, and synergy score |
| Time | <5 minutes per optimization |

---

## 5. Cell-Free Phage Synthesis (CFPS) Module

### 5.1 DNA Synthesis

| Parameter | Specification |
|-----------|--------------|
| Method | Inkjet oligonucleotide synthesis (phosphoramidite chemistry) → Gibson assembly → full phage genome |
| Platform | Custom microfluidic DNA synthesis chip (modified from Twist Bioscience silicon chip approach) |
| Capacity | Genomes up to 250 kb (covers 95% of known lytic phages; largest known lytic phage ~250 kb) |
| Synthesis time | 8–12 hours (parallel oligo synthesis + error correction + assembly) |
| Error rate | <1/10,000 bp after enzymatic error correction (ErCC) — sufficient for functional phage genome |
| Cost per genome | ~$5–10 at scale |
| Error correction | Enzymatic (T7 Endonuclease + DNA polymerase repair) + selective amplification of correct assemblies |
| Quality control | On-chip capillary electrophoresis for size verification; Nanopore spot-check for sequence verification |

### 5.2 Cell-Free Transcription-Translation (CF-Tx)

| Parameter | Specification |
|-----------|--------------|
| System | *E. coli* lysate-based (NEB PURExpress-compatible, optimized for phage protein folding) |
| Reaction volume | 5 mL per phage (standard), up to 20 mL (large tailed phages) |
| Key additives | GroEL/GroES chaperone mix (2 µM); T7 RNA polymerase (for T7-like promoters); *E. coli* σ⁷⁰ RNA polymerase (native); ATP regeneration system (creatine phosphate + creatine kinase); Trehalose (5% w/v); Mg²⁺ optimization buffer (12 mM optimal for most phage morphogenesis) |
| Incubation | 37°C, 4–6 hours for virion self-assembly |
| Yield target | 10⁸–10¹⁰ PFU/mL (current state of art: 10⁶–10⁸ PFU/mL; 100× improvement projected by 2030 with chaperone + energy optimization) |
| Quality | Virion morphology confirmed by on-device nanopore impedance spectroscopy (size/shape proxy; discriminates intact vs. malformed virions with >90% accuracy) |
| Sterilization | CF-Tx lysate is pre-cleared of bacterial cells; no endotoxin introduction from synthesis step |
| Scalability | 5–20 mL reactions per phage; 3–5 phages per cocktail = 15–100 mL total; within APTP enclosure volume |

### 5.3 Phage Amplification (Yield Boost — Backup Mode)

| Parameter | Specification |
|-----------|--------------|
| Trigger | CFPS yield < 10⁶ PFU/mL for any phage in cocktail |
| Method | Isolated target strain cultured in sealed, disposable 10 mL bioreactor pouch (single-use, gamma-sterilized) |
| Infection parameters | MOI = 0.01, 4-hour infection cycle, 2 passages maximum |
| Filtration | 0.22 µm filter removes bacterial debris before QC |
| Additional time | +12 hours |
| Endotoxin risk | Elevated (requires additional LAL testing); mitigated by polymyxin B column in QC |

---

## 6. Quality Control & Formulation Module

### 6.1 QC Tests (Automated, On-Device)

| Test | Method | Threshold | Time | Critical/Non-critical |
|------|--------|-----------|------|----------------------|
| Phage titer | Drop-plaque assay (microfluidic) | >10⁸ PFU/mL | 8 hours (concurrent) | Critical |
| Sterility | Growth in BHI broth (on-chip) | No growth at 48 hrs | 48 hrs (concurrent) | Critical |
| Endotoxin | LAL chromogenic assay | <0.5 EU/mL (IV) / <5 EU/mL (topical) | 30 min | Critical |
| pH | Micro pH electrode | 6.5–7.5 | 1 min | Non-critical |
| Osmolality | Vapor pressure osmometer | 280–320 mOsm/kg | 5 min | Non-critical |
| Residual DNA | PicoGreen fluorescence | <10 ng/mL | 15 min | Non-critical |
| Morphology | Nanopore impedance spectroscopy | Within 2σ of reference | 15 min | Non-critical |
| Protein contaminants | UV-Vis 280/260 ratio | <5% non-phage protein | 5 min | Non-critical |

**Release criteria**: All 3 critical tests must pass. Product may be released provisionally if non-critical tests fail but are within 2× threshold (with clinician override and documentation).

### 6.2 Formulation Options

| Route | Formulation | Volume | Additives | Shelf Life | Primary Indication |
|-------|------------|--------|-----------|------------|-------------------|
| Intravenous | Sterile isotonic solution (0.9% NaCl) | 10–100 mL vial | 5% trehalose, 1 mM MgSO₄ | 30 days at 4°C | Sepsis, bacteremia |
| Topical | Hydrogel dressing (1% carbopol) | 50 mL pump | N/A | 14 days at 4°C | Wound infection, burn |
| Inhalation | Nebulizer cartridge | 5 mL | 0.1% Tween 80 | 7 days at 4°C | Pneumonia, CF lung infection |
| Oral | Enteric-coated capsule | 10¹⁰ PFU | Alginate encapsulation | 60 days at 4°C | GI infection, C. difficile |
| Intravesical | Catheter-instilled solution | 50 mL | 5% trehalose | 14 days at 4°C | UTI |

### 6.3 Lot Documentation

Every APTP run generates a complete electronic batch record:
- Target pathogen species, strain (MLST), resistome
- Selected phages (genome sequences, lysis probabilities, engineering edits)
- CFPS reaction conditions and yield
- All QC test results
- Formulation details
- Patient ID (anonymized for public database)
- Timestamps for every step

---

## 7. Real-Time Monitoring & Adaptive Response

### 7.1 Post-Administration Monitoring

| Parameter | Specification |
|-----------|--------------|
| Sampling | Patient samples (blood, wound swab, sputum, urine) at 12-hour intervals for 72 hours |
| Sequencing | Nanopore Flongle (same unit) for bacterial population sequencing |
| Detection targets | (1) Phage-susceptible strain clearance (quantitative, ≥3-log reduction); (2) Escape mutant emergence (receptor mutation detection); (3) Secondary infection / dysbiosis |
| Response time | If escape mutant detected: AI redesigns cocktail in 4 hours; CFPS produces updated phages in 12 hours; new cocktail ready in **18 hours total** |
| PK/PD model | On-device model (validated against published phage therapy pharmacology data); predicts optimal dosing schedule (initial bolus + maintenance); adjusts for infection site (blood, lung, wound, urinary tract) |
| Alert thresholds | <1-log reduction at 24h: consider dose adjustment; <2-log reduction at 48h: re-engineer cocktail; emergence of new resistance: auto-trigger re-engineering loop |

### 7.2 Adaptive Dosing Protocol

| Infection Type | Initial Dose | Route | Maintenance | Duration |
|---------------|-------------|-------|-------------|-----------|
| Bacteremia / sepsis | 10⁹ PFU IV bolus | IV | 10⁸ PFU IV q8h | 5–7 days |
| Pneumonia | 10⁹ PFU nebulized | Inhaled | 10⁸ PFU nebulized q12h | 7–10 days |
| Wound infection | 10⁸ PFU/mL topical gel | Topical | Reapply q24h | 7–14 days |
| UTI | 10⁹ PFU intravesical | Catheter | Single dose or q48h | 1–3 doses |
| GI infection | 10¹⁰ PFU oral capsule | Oral | q12h | 5–7 days |

---

## 8. Consumable Cartridges

### 8.1 Patient Cartridge (Single-Use, Per-Course)

| Component | Specification | Quantity |
|-----------|--------------|----------|
| Environmental sample vial | 15 mL, sterile, screw-cap | 1 |
| Patient sample vial | 2 mL, transport medium (Amies gel) | 1 |
| CF-Tx reagent pack | 5 × 5 mL reactions (one per phage) | 1 |
| DNA synthesis chip | 1 × 250 kb capacity | 1 |
| Microfluidic screening chip | 1 × 10,000-well PDMS | 1 |
| Bioreactor pouch (backup) | 1 × 10 mL, gamma-sterilized | 1 |
| Formulation supplies | Sterile vials, labels, Luer connectors | 1 set |
| Shelf life | 18 months at 4–30°C | — |
| Cost target | $50–80 at 100K units/year | — |
| Storage | Room temperature (4–30°C); no cold chain required | — |

### 8.2 Service Cartridge (Monthly)

| Component | Specification |
|-----------|--------------|
| QC calibration standards | LAL standard, PFU reference, pH buffers, osmolality reference |
| HEPA filter replacement | ISO Class 7, 99.97% @ 0.3 µm |
| Nanopore flow cells | Flongle × 2, MinION × 1 |
| CF-Tx lysate master mix | Bulk (50 mL), stored at 4°C |
| Waste collection container | 2 L, autoclave-safe |
| DNA synthesis reagent pack | Phosphoramidite cartridges × 4 |
| Cost target | $500–800 per month |

---

## 9. Safety & Dual-Use Safeguards

### 9.1 Biosecurity Locks

| Safeguard | Implementation |
|-----------|---------------|
| DNA synthesis screening | All synthesis orders checked against curated pathogenic gene database (IWG criteria: virulence factors, toxins, AMR genes, select agent sequences); synthesis blocked for matches; database updated weekly |
| Access logging | Every cartridge, DNA synthesis, and output logged with timestamp, user ID, patient ID, target pathogen |
| Hardware interlock | Synthesis module will not operate without valid patient sample ID (linked to clinical record in hospital EHR) |
| Phage genome review | AI module flags any phage genome carrying integrase, repressor, toxin, or AMR genes for manual review; auto-rejects lysogenic candidates |
| Remote audit | Encrypted telemetry sent to public health authority (opt-in; required in some jurisdictions); quarterly audit reports |
| Kill-switch | Engineered phages carry thermolabile capsid mutations (denature above 50°C); ensures no environmental persistence in tropical waterways |
| Rate limiting | Maximum 5 phage cocktail preparations per 24-hour period per unit (prevents bulk production for misuse) |
| Geofencing | Units deployed in restricted regions have additional authentication requirements (UN security council sanctions list) |

### 9.2 Environmental Safeguards

| Safeguard | Implementation |
|-----------|---------------|
| Waste inactivation | All liquid waste heat-inactivated (85°C, 30 min) before disposal; solid waste autoclaved |
| Phage containment | All phages strictly lytic (no lysogenic phages released); narrow host range by design |
| Self-limiting persistence | Thermolabile capsid mutations ensure phages denature above 50°C (tropical waterways) and lose infectivity after 7–14 days in the environment |
| Endotoxin control | LAL testing ensures <0.5 EU/mL for IV products; polymyxin B column backup for high-endotoxin preparations |
| Antibiotic-sparing | Phage therapy reduces broad-spectrum antibiotic use; estimated 30–50% reduction in antibiotic prescriptions for MDR infections |

---

## 10. Performance Benchmarks

| Metric | APTP Target | Current Best (Manual) | Improvement Factor |
|--------|-------------|----------------------|-------------------|
| Time from sample to therapy | ≤48 hours | 2–16 weeks | 50–500× |
| Cost per course | $50–150 | $30,000–100,000 | 200–2,000× |
| Personnel required | 1 trained nurse | 5 PhDs + lab techs | 5× fewer |
| Facility requirement | District hospital | BSL-2 reference lab | Ubiquitous access |
| Phage cocktail diversity | 3–5 phages (optimized) | 1–12 (variable quality) | Consistent |
| Clinical success rate (target) | >80% clearance | 60–80% (published) | +10–20% |
| Resistance detection time | 12-hour intervals | Days to weeks | 20–50× |
| Cold chain requirement | 4–30°C storage | −80°C (frozen stocks) | Eliminated |
| Annual throughput per unit | 200–500 patients | 10–50 patients | 10–50× |
| Countries with access | Every country with a hospital | 3 (Georgia, Poland, Russia) | 60–200× |
| Time to adapt to new resistance | 18 hours | 4–12 weeks | 50–200× |

---

## 11. Materials & Supply Chain

### 11.1 Key Materials

| Material | Source | Scalability | Cost Trajectory |
|----------|--------|-------------|-----------------|
| *E. coli* CF-Tx lysate | NEB / commercial biomanufacturing | High (commodity) | $5/mL → $1/mL by 2030 |
| Phosphoramidite reagents | Sigma-Aldrich, Agilent | High | Declining (genomics drives scale) |
| PDMS microfluidic chips | Injection molding (soft lithography → mass production) | Very high at scale | <$1/chip at 100K/yr |
| Oxford Nanopore Flongle | Oxford Nanopore (commercial) | Medium | $90/flow cell |
| GroEL/GroES chaperones | Recombinant production (BL21 DE3) | High | $0.50/reaction |
| Trehalose, MgSO₄, buffers | Commodity chemicals | Very high | Negligible |
| Sterile vials/pouches | Medical packaging | Very high | $0.10–0.50/unit |
| NVIDIA Jetson Orin | NVIDIA (commercial) | High | $500/unit |

### 11.2 Manufacturing Path

| Phase | Year | Volume | Manufacturing Partner | Unit Cost |
|-------|------|--------|----------------------|-----------|
| Prototype | 2028–2030 | 10–50 units | In-house + university fab | $200,000 |
| Pilot production | 2031–2033 | 500 units | Contract manufacturer (Danaher OEM) | $50,000 |
| Clinical validation | 2033–2035 | 2,000 units | Contract manufacturer | $25,000 |
| Scale production | 2035–2038 | 10,000 units/yr | Contract manufacturer + regional assembly | $20,000 |
| Ubiquity | 2040+ | 50,000+ units/yr | Regional manufacturing (India, China, EU, US) | $15,000 |

---

## 12. Software & AI

### 12.1 PhageFormer Model

| Parameter | Specification |
|-----------|--------------|
| Training data | NCBI GenBank (all phage genomes), PhagesDB, GPD, proprietary interaction datasets from clinical phage therapy centers |
| Architecture | Modified ESM-2 (protein language model) + custom genome-level transformer |
| Parameters | 110M (12 layers, 768 hidden dim, 12 attention heads) |
| Inference | On-device (NVIDIA Jetson Orin, 40 TOPS, 15W); <30 sec per cocktail design |
| Cloud backup | Optional; encrypted (AES-256); HIPAA/GDPR compliant |
| Update cycle | Monthly model updates; quarterly full retraining |
| Explainability | Attention maps, SHAP values, feature attribution for every prediction |

### 12.2 Regulatory Intelligence Module

| Feature | Specification |
|---------|--------------|
| Database | Continuously updated phage therapy regulations by country (50+ jurisdictions) |
| Documentation | Auto-generates required submission documents for local regulatory bodies |
| Tracking | Monitors evolving FDA/EMA/WHO guidance on personalized biologics |
| Alert system | Push notifications for regulatory changes affecting deployed units |

### 12.3 Firmware & Security

| Feature | Specification |
|---------|--------------|
| OS | Linux (Yocto-based, hardened) |
| OTA updates | Signed, encrypted, incremental; rollback capability |
| Data encryption | AES-256 at rest; TLS 1.3 in transit |
| User authentication | Smart card + PIN; role-based access (nurse, physician, admin) |
| Audit trail | Immutable log of every action (blockchain-anchored hash chain) |

---

## 13. Reliability & Maintenance

| Parameter | Specification |
|-----------|--------------|
| Mean time between failures (MTBF) | >10,000 hours (design target) |
| Mean time to repair (MTTR) | <4 hours (with service cartridge + remote support) |
| Preventive maintenance | Monthly service cartridge replacement (30 min procedure) |
| Annual calibration | On-site or remote; QC standards included in service cartridge |
| Software updates | Monthly (OTA); critical security patches within 24 hours |
| Warranty | 3 years parts and labor; extended warranty available |
| End-of-life | Responsible recycling program; CFPS reagents biodegradable; electronics recycled per WEEE directive |

---

*Specification v2.0 — 2026-06-17 — Adaptive Phage Therapeutics Platform — Enhanced Edition*