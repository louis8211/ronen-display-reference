# Air gap vs full optical bonding

Why the layer of air between a TFT panel and its cover glass matters more than most people expect, and how to decide whether to pay for optical bonding.

## The three stack-ups

| Stack | Construction | Reflection at cover interface | Field behaviour |
|---|---|---|---|
| Air gap (frame seal) | Panel — air — cover glass | ~4 % per glass surface, plus internal reflection | Cheapest, serviceable, prone to fogging and dust |
| Full bonding (OCR / OCA) | Panel — adhesive — cover glass | ~0.1–0.5 % | Best contrast and sunlight readability, hardest to rework |
| Partial bonding (edge only) | Panel bonded at perimeter, air in the centre | Intermediate | Compromise; still fogs, still reflects in the middle |

## What the air gap actually costs you

1. **Ambient reflection.** Every uncoated glass-to-air interface reflects roughly 4 % of incident light. With two surfaces (rear of cover glass, front of panel) that is about 8 % of the ambient light added to the image. Under 30 klx sunlight the reflected component can exceed the transmitted image, which is why an unbonded 300 cd/m² panel looks "grey" outdoors regardless of how bright the backlight is.
2. **Ghosting from internal reflection.** Bright objects create a dim, offset duplicate because light bounces between the panel surface and the rear of the cover glass. On a 5 mm air gap the offset is visible and grows with viewing distance.
3. **Fogging and dust.** A sealed air gap contains moisture. A temperature drop below dew point deposits it on the coldest surface — usually the inside of the cover glass, directly in the operator's line of sight.
4. **Mechanical parallax in touch designs.** In a touch stack the gap between the touch sensor and the display adds a parallax offset that shows up as a "touch lands 2 mm off" complaint at shallow viewing angles.

## What full bonding buys

- **Contrast ratio under ambient light** improves by roughly the ratio of the two reflection figures — commonly 3–5× apparent contrast in bright rooms.
- **Sunlight readability** without pushing brightness into the 1000 cd/m² range, which saves backlight power and thermal budget.
- **Rigidity.** The bonded stack is stiffer than the sum of its parts, which helps thin bezel designs and reduces panel stress from cover-glass flex.
- **No internal fogging**, because there is no air volume to hold moisture.

## What full bonding costs

- **Rework is effectively impossible.** A bonded module with a defective panel is scrap. Plan yield and spares accordingly.
- **Bubbles and voids.** Large panels (> 10.1") are sensitive to adhesive dispensing and vacuum lamination. Ask for the void inspection criterion, not just "bonded".
- **UV cure shrink.** Some OCR chemistries shrink on cure, which can pull the panel and produce mura at the edges. Silicone-based OCR has lower shrink but higher cost.
- **Thermal expansion mismatch.** Adhesive, glass and panel have different CTE. Wide-temperature designs need an adhesive whose modulus stays low at −30 °C, otherwise the bond transfers stress into the LC cell.

## A decision rule

Bond if **any** of these is true:

1. The product is read in direct sunlight or near windows (kiosk, outdoor payment terminal, agricultural controller).
2. The enclosure will see condensation cycles (cold store, vehicle, marine).
3. The design needs a thin bezel or a flush front face.
4. Touch accuracy at shallow angles is a stated requirement.

Do **not** bond if the product is indoor-only, cost-sensitive, and expected to be serviced in the field — an air gap with a desiccant and a good gasket is the pragmatic choice.

## Specifying it

State four things in the drawing: adhesive chemistry (OCR silicone vs acrylic, OCA film), the void/bubble acceptance criterion, the operating temperature range the bond must survive, and the rework policy. A supplier who cannot give you the first and third is guessing.

Further reading on odmlcd.com: [air vs optical bonding](https://odmlcd.com/solutions/air-vs-optical-bonding) and the [brightness calculator](https://odmlcd.com/tools/lcd-brightness-calculator) for ambient-to-luminance sizing.
