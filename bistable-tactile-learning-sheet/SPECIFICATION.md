# Specification — Bistable Tactile Learning Sheet

**Author:** jayis1

**Status:** Proposed engineering specification; all performance values are validation targets.

## 1. Design Objective

Provide a portable, repairable, full-page tactile display for Braille and spatial learning content at a delivered target cost below US$400, with no required cloud connection and no continuous power needed to hold a page.

## 2. System Architecture

```text
[USB-C / SD / physical controls]
              |
[local BRF/SVG/EPUB/MathML renderer]
              |
[80 x 60 active-matrix heater backplane]
              |
[shape-memory collar + silicone diaphragm sheet]
              |
[eight-sector pneumatic plenum plate]
              |
[reversible pump + accumulator + pressure sensing]
```

The controller first compares the requested page with the latched state map. It heats only pixels that must change, verifies temperature, applies positive pressure to raise or vacuum to flatten them, cools the selected collars, and confirms the pattern using pressure-decay and electrical continuity checks.

## 3. Tactile Sheet

| Parameter | Target |
|---|---:|
| Taxel array | 80 × 60 |
| Active dimensions | 240 × 180 mm |
| Center pitch | 3.0 ± 0.1 mm |
| Raised displacement | 0.7–1.0 mm |
| Raised-dot force at 0.2 mm depression | ≥0.2 N |
| Neighbor height error | ≤0.15 mm |
| User-contact temperature | ≤40°C |
| Transition zone | 43–50°C |
| Refresh error after one retry | <0.1% of commanded taxels |

The top skin is a 150–300 µm platinum-cured silicone film. Each pixel has a 2.4–2.6 mm dome supported by a 200–500 µm variable-stiffness TPU collar. A textured fluorine-free silicone overcoat reduces finger drag and can be cleaned with mild soap or 70% isopropyl alcohol after compatibility validation.

The cassette is mechanically keyed so an incompatible sheet cannot be driven. A passive temperature-coded resistor stores the cassette's allowed heater profile; no serial number or cloud authorization is required.

## 4. Selection and Heating

The active matrix uses low-voltage metal-oxide thin-film transistors on PET to switch screen-printed carbon-black resistive rings. Maximum local heater voltage is 24 VDC. Temperature is estimated from heater resistance and checked by distributed thin-film thermistors at least every 20 mm.

Control limits:

- heat pulse: 100–800 ms, calibration dependent;
- peak internal collar temperature: 55°C;
- hard user-surface trip: 40°C;
- maximum simultaneous heated area: 25% of pixels;
- two independent shutdown paths: controller limit plus non-resettable thermal fuse at the pump/heater power stage.

A failed transistor must default to unheated. A stuck-on heater causes the whole heater rail to open and blocks further refreshes while leaving the current page mechanically readable.

## 5. Pneumatic Backplane

The backplane is laser-welded recycled polycarbonate with eight independently isolated plenums. Pixel selection occurs in the heater matrix: during a positive or negative pressure pulse, only softened collars can change shape. Raising and flattening are separate passes, and each plenum is calibrated from its pressure response rather than assumed to behave identically.

| Parameter | Target |
|---|---:|
| Working pressure/vacuum | ±30–60 kPa gauge |
| Proof pressure | ±120 kPa gauge |
| Typical pump flow | 1–3 L/min |
| Typical page refresh / worst-case full inversion | <2 s / <8 s |
| Static pressure demand | none after collar relatch |
| Allowed leak | <2 kPa/min per isolated sector |
| Independently isolated sectors | 8 minimum |

Eight sectors limit a puncture to at most 12.5% of the page. Each sector has a replaceable hydrophobic particulate filter and isolation valve. The device performs a pressure-decay check at startup and after every complete refresh.

## 6. Electronics, Power, and Privacy

- RISC-V microcontroller or application processor with verified boot from owner-controlled keys.
- 32 GB removable or replaceable local storage.
- USB-C power/data, SD card, 3.5 mm audio output, and six physical controls.
- 60 Wh LiFePO4 battery with screw-fastened enclosure and replaceable protection board.
- No camera, microphone, GNSS, cellular modem, mandatory Wi-Fi, biometric input, usage telemetry, advertising identifier, or remote-disable function.
- Optional radio modules, if locally desired, must be physically removable and disabled by a hardware switch.
- All core file conversion and rendering functions operate offline using documented formats.

Power targets:

| Mode | Target |
|---|---:|
| Typical page update | 10–20 J |
| Maximum refresh power | 25 W peak |
| Latched page | <0.1 W |
| Reading with electronics asleep | <0.02 W |
| Charging input | USB-C PD, 15–45 W |

## 7. Content and Human Factors

Supported inputs at release must include BRF, Unicode Braille, plain text, SVG, tagged EPUB, and MathML. The renderer never claims semantic correctness for an untagged image. It provides adjustable simplification, line thickness, label density, and separate tactile layers.

Human-factors validation must include:

- adult and child Braille readers;
- novice and expert tactile-graphics users;
- deafblind users without dependence on audio prompts;
- users with reduced finger sensitivity or limited hand mobility;
- multiple Braille codes and right-to-left language workflows.

No safety-critical navigation or medical diagram may rely solely on automatic image conversion without human review.

## 8. Maintainability and End of Life

The tactile cassette, pump, filters, battery, controls, and main board are separately replaceable with common hand tools. Exploded diagrams, diagnostics, firmware source, file formats, and calibration procedures remain openly documented. The enclosure carries polymer identification marks; silicone/TPU cassettes are collected through regional repair centers until material recycling is validated.

Service targets:

- filter inspection: every 12 months;
- cassette calibration: automatic monthly check plus on-demand test page;
- pump life: >5,000 operating hours;
- battery: >2,000 full-equivalent cycles;
- electronics/enclosure: 10 years;
- spare modules available for at least 15 years after manufacture.

## 9. Validation Matrix

| Requirement | Verification method | Pass condition |
|---|---|---|
| Pixel geometry | Laser profilometry over five sheets | Height and pitch within Section 3 limits |
| Holding force | Instrumented 0.2 mm probe | ≥0.2 N on 99.9% of raised pixels |
| Address independence | Alternating checkerboard and single-pixel patterns | <0.1% error after one retry |
| Refresh speed | High-speed video and controller log | Typical page <2 s; worst-case full inversion <8 s |
| Durability | Accelerated raise/flatten cycling | >2 million cycles/pixel with <10% force loss |
| Thermal safety | Fault insertion and thermal imaging | Surface never exceeds 40°C |
| Leak containment | Needle puncture in each sector | Failure remains within one sector and is reported |
| Readability | Controlled participant study | Non-inferior Braille accuracy to validated embossed control |
| Diagram utility | Matched comprehension tasks | Predefined non-inferiority margin met |
| Battery endurance | Classroom duty-cycle test | Five school days at 150 updates/day |
| Repairability | Timed technician and teacher trials | Pump/battery <15 min; cassette <5 min |
| Environmental resilience | Drop, vibration, dust, humidity, and cleaning tests | No unsafe failure; calibration restored after service |

## 10. Critical Engineering Risks

1. **Pressure nonuniformity and mechanical coupling:** shared plenums may underdrive remote pixels or disturb neighboring diaphragms. Reject the shared-plenum architecture if sector geometry, pulse sequencing, and collar selectivity cannot meet the pixel-error gate.
2. **Thermal fatigue:** repeated transition cycling may embrittle or creep the collar. Screen formulations over two million cycles before selecting production chemistry.
3. **Manufacturing yield:** one defect among 4,800 pixels can matter. Design sector and pixel mapping so a bad pixel is detected, reported, and economically repairable.
4. **Tactile ambiguity:** engineering metrics do not prove readable pages. User studies are release gates, not post-launch research.
5. **Cassette waste:** replacement improves service life but creates polymer waste. Procurement includes take-back and audited recovery; claims of recyclability require actual processing trials.
6. **Affordability drift:** active-matrix yield or servicing could defeat the price goal. Compare total five-year cost against embossed materials and line displays in each deployment market.

## 11. Technology Roadmap

- **Years 1–3:** 20 × 20 and 40 × 30 arrays; characterize collar chemistry, plenum pressure uniformity, diaphragm coupling, tactile force, and skin temperature.
- **Years 3–6:** full 80 × 60 engineering sheets; automated yield mapping and two-million-cycle testing.
- **Years 6–10:** participatory design and controlled learning trials; ruggedized repairable pilot units.
- **Years 10–15:** multi-country school pilots, open content tooling, localized repair training, and safety/accessibility certification.
- **Years 15–20:** regional manufacture and public procurement, conditional on published reliability and learning-access evidence.

The invention is viable only if it meets full-page reliability and lifecycle-cost gates. If the active matrix or pneumatic manifold remains uneconomic, the program should fall back to smaller modular tiles rather than hiding failures behind software interpolation.
