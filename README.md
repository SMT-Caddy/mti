# SMT Caddy MTI: manual SMD tape feeder

Documentation and datasheet for the **SMT Caddy MTI**, a manual SMD tape feeder for cut tape that mounts on 35 mm DIN rail.

- Product page: https://smtcaddy.com/MTI
- Video overview: https://youtu.be/UB94PlbSV4s
- Manufacturer: SMT Caddy, a brand of Elantron, Inc., Riverside, California, USA

---

## Overview

The MTI holds a strip of cut SMD tape and presents one component at a time at a fixed pick zone, for hand placement with a vacuum pen, tweezers or any manual or home-built pick-and-place setup.

- **Advance:** a full press of the plunger moves the tape up to 6.0 mm. You can press it with a fingertip or with the plastic body of a pickup stylus.
- **Cover tape:** peeled automatically as the tape advances and discharged rearward, clear of the pick zone.
- **Width:** each feeder is the tape width plus 2 mm, so feeders pack side by side on the rail.
- **Widths from one base:** the base unit is configured for 8 mm tape. Extension kits convert it to 12, 16, 24 or 32 mm.
- **ESD:** molded in electrically conductive carbon-fiber LCP and grounded through the DIN rail.
- **No motors, electronics or power.**

## Specifications

| Parameter | Value | Notes |
|---|---|---|
| Supported tape widths | 8, 12, 16, 24, 32 mm | 8 mm as shipped; others via extension kits |
| Tape type | Cut tape, paper or embossed carrier | Not for reels |
| Feeder width | W + 2 mm | 10 mm at W = 8 mm |
| Advance per full press | up to 6.0 mm | |
| Max carrier pocket depth | 13 mm | |
| Cover tape handling | Auto peel, rear discharge | |
| Mounting | 35 mm DIN (top-hat) rail | |
| Housing material | Liquid crystal polymer, 30% carbon fiber (LCP-CF30) | |
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

- The housing is **conductive**, not just dissipative, so charge drains away instead of building up.
- The ground path runs through the DIN rail. Use a steel rail, or on anodized aluminum rail, bare a contact point under the feeder. Bond the rail to your ESD ground.

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
