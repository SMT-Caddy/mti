# SMT Caddy MTI: manual SMD tape feeder

Documentation and datasheet for the **SMT Caddy MTI**, a manual SMD tape feeder for cut tape that mounts on 35 mm DIN rail.

- Product page: https://smtcaddy.com/MTI
- Video overview: https://youtu.be/UB94PlbSV4s
- Manufacturer: SMT Caddy, a brand of Elantron, Inc., Riverside, California, USA

---

## Overview

The MTI holds a strip of cut SMD tape and presents the parts at a fixed pick zone, for hand placement with a vacuum pen, tweezers or any manual or home-built pick-and-place setup.

- **Advance:** a full press of the plunger moves the tape up to 6.0 mm. Press it with a fingertip, the body of a stylus, or the stylus tip if it is rigid enough.
- **Cover tape:** peeled automatically as the tape advances and discharged rearward, clear of the pick zone.
- **Width:** each feeder is the tape width plus 2 mm, so feeders pack side by side on the rail.
- **Widths from one base:** the base unit is configured for 8 mm tape. Extension kits convert it to 12, 16, 24 or 32 mm.
- **ESD:** molded in electrically conductive carbon-fiber LCP (tens of ohms surface resistance) and grounded through the DIN rail, so the feeder does not build up charge.
- **No motors, electronics or power.**

## Specifications

| Parameter | Value | Notes |
|---|---|---|
| Supported tape widths | 8, 12, 16, 24, 32 mm | 8 mm as shipped; others via extension kits |
| Tape type | Cut tape, paper or embossed carrier | Not for reels |
| Feeder width | W + 2 mm | 10 mm at W = 8 mm |
| Advance per full press | up to 6.0 mm | |
| Actuation | Fingertip, stylus body, or stylus tip | Stylus tip only if rigid enough |
| Max carrier pocket depth | 13 mm | |
| Cover tape handling | Auto peel, rear discharge | |
| Mounting | 35 mm DIN (top-hat) rail | |
| Housing material | Liquid crystal polymer, 30% carbon fiber (LCP-CF30) | |
| Surface resistance | Tens of ohms (< 100 Ω) | Measured, two-probe; conductive class |
| Origin | Designed, molded and assembled in the U.S. | Except one bearing |
| Warranty | 1 year from delivery | Workmanship and early failure; customer pays shipping |

### Material — typical values, LCP-CF30

| Property | Value | Test method |
|---|---|---|
| Tensile modulus | 31.8 GPa | ISO 527-2 |
| Tensile strength | 200 MPa | ISO 527-2 |
| Flexural modulus | 25.5 GPa | ISO 178 |
| Flexural strength | 300 MPa | ISO 178 |
| Compressive modulus | 33.0 GPa | ISO 604 |
| Density | 1.50 g/cm³ | ISO 1183 |
| Mold shrinkage, flow / across | 0.0 / 0.1 % | ISO 294-4 |

These are typical published values for 30% carbon-fiber reinforced LCP, not lot-specific test results. For comparison, standard engineering plastics (ABS, nylon, PP) are about 1.5 to 3 GPa, and aluminum 6061 is 69 GPa.

### Electrical / ESD

- **Conductive housing.** Measured surface resistance on molded parts is tens of ohms (under 100 Ω) with a two-probe meter; the exact reading depends on probe spacing, contact pressure and where the probes land. That is well inside the conductive class (below 1 × 10⁴ Ω, ANSI/ESD S541).
- **What it does and doesn't do.** Components never touch the MTI; only the carrier and cover tape do, and component packaging tape is already made to be static-safe. The MTI is therefore not the ESD control for your parts. Its job is not to add to the problem: tape sliding over an insulating plastic feeder can charge it by friction and leave that charge next to the parts, while a grounded conductive housing drains it.
- **Ground path** runs through the DIN rail. Use a steel rail, or on anodized aluminum rail, bare a contact point under the feeder. Bond the rail to your ESD ground.

## Why not 3D-print one?

3D printing suits a lot of shop tooling, and printed cut-tape feeders can work. The MTI is built for packing density: each feeder is 2 mm wider than its tape, so twenty 8 mm feeders fit in 200 mm of DIN rail.

A thin wall alone is not enough. A thin, stiff wall is. MTI walls are as thin as 0.6 mm, molded in LCP with 30% carbon fiber: 31.8 GPa tensile modulus.

The feeder must also be conductive or dissipative, not an insulator. The stiffest resin we found (11 GPa) is an insulator. ESD resins we found top out around 4 to 5 GPa; typical ones are about 1.9 GPa. The MTI has both: 31.8 GPa, and conductive, with a measured surface resistance under 100 Ω.

Gear teeth are accurate to under 0.01 mm, tooth to tooth and gear to gear.

Printed versions end up wider, coarser or less durable, which breaks the 2 mm budget. Specs aside, one MTI is a dozen or more parts: material, printer wear, failed prints, setup, finishing and assembly would arguably cost more than the $22 to $35 an MTI sells for.

| | MTI (molded LCP, 30% carbon fiber) | SLA resin | FDM filament |
|---|---|---|---|
| Tensile modulus | 31.8 GPa | Stiffest found: 11 GPa, insulating ([Formlabs Rigid 10K](https://formlabs.com/uk/store/rigid-10k-resin)). Stiffest ESD found: 4 to 5 GPa ([3DResyns R290D90 ESD](https://www.3dresyns.com/collections/electro-static-discharge-dissipative-esd-compliant-3d-resin-materials)). Typical ESD: about 1.9 GPa ([Formlabs ESD](https://formlabs.com/support/Using-ESD-Resin/), [Liqcreate ESD](https://www.liqcreate.com/product/esd/)) | Typical: about 2.5 GPa (ABS, nylon) |
| Conductive or dissipative? | Yes, conductive: under 100 Ω measured | ESD resins: yes, dissipative, 10⁵ to 10⁸ Ω/sq. Standard resins: no, insulating, over 2 × 10¹⁴ Ω/sq ([Formlabs](https://formlabs.com/support/Electrical-properties-of-selected-Formlabs-SLA-resins/)) | Carbon-filled ESD grades: yes, dissipative, 10⁴ to 10⁷ Ω/sq ([Polymaker](https://wiki.polymaker.com/the-basics/fun-3d-printing-facts/esd-safe-3d-printing-materials-and-how-they-work)) |
| Tooth accuracy | Under 0.01 mm | No published figure found | No published figure found |

Print-material figures are typical published values; tensile figures for the MTI are typical values for LCP-CF30. Conductive class per ANSI/ESD S541: below 10⁴ Ω.

## Compatibility

- **Works with:** most manual or home-built pick-and-place setups, including vacuum pens, tweezers and manual placement stations. Any fixture that holds a 35 mm DIN rail can carry a bank of MTIs.
- **Not compatible with:** **SMT Caddy Model A feeder banks.** Model A owners should keep using the Model A's own feeders.
- **Not for:** full reels. The MTI feeds cut tape only.

## Changing tape width (outline)

You need a screwdriver and the extension kit for the target width. The change takes about one minute and needs no special tooling.

| Target width | Kit(s) on an 8 mm base |
|---|---|
| 12 mm | one 4 mm kit |
| 16 mm | one 8 mm kit |
| 24 mm | two 8 mm kits |
| 32 mm | three 8 mm kits |

Step-by-step instructions with photos are in the **Width change how-to** on the product page: https://smtcaddy.com/products/smt-caddy-mti

**Caution:** the walls are thin to keep each feeder only 2 mm wider than the tape. Do not force the plunger. If the tape jams, clear it first.

## Planning a feeder bank on DIN rail

Each feeder takes **W + 2 mm** of rail, where W is the tape width.

**Single width:** N feeders of width W need

```
L = N × (W + 2) mm
```

**Mixed widths:** add up each feeder's footprint:

```
L = Σ (Wᵢ + 2) mm
```

Then add rail end stops, if used, and any margin for mounting screws.

| Tape width W | Rail per feeder | Feeders per 100 mm | 10 feeders | 20 feeders | 50 feeders |
|---|---|---|---|---|---|
| 8 mm | 10 mm | 10 | 100 mm | 200 mm | 500 mm |
| 12 mm | 14 mm | 7 | 140 mm | 280 mm | 700 mm |
| 16 mm | 18 mm | 5 | 180 mm | 360 mm | 900 mm |
| 24 mm | 26 mm | 3 | 260 mm | 520 mm | 1300 mm |
| 32 mm | 34 mm | 2 | 340 mm | 680 mm | 1700 mm |

**Example:** 30 × 8 mm feeders, 6 × 12 mm and 2 × 24 mm need 30×10 + 6×14 + 2×26 = 300 + 84 + 52 = **436 mm** of rail, plus end stops.

The centre-to-centre pitch between adjacent feeders of the same width is also W + 2 mm, which matters if you program a camera or jog positions for the pick zones.

The product page also has a rail planner that estimates rail length and total price.

## Ordering

- Feeders: https://smtcaddy.com/MTI
- Extension kits: https://smtcaddy.com/products/mti-extension-kit
- Feeder labels (Avery 5412): https://smtcaddy.com/products/feeder-labels
- Quotes and purchase orders (qualified U.S. organizations): https://smtcaddy.com/pages/contact

Quantity pricing (all tape widths count toward the tier), extension kits and current offers are on the product page.

## Contributing

Corrections, measurements and setup photos are welcome as issues or pull requests. For product support, email info@smtcaddy.com. We usually reply within one business day.

## License

Documentation, drawings and images in this repository are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). This license covers the documentation only. It does not license the product design, the SMT Caddy name or logo, or any trademarks.

© 2026 Elantron, Inc.
