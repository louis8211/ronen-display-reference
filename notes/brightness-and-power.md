# Brightness, power & lifetime budgeting

How to budget display luminance, backlight power and service life before you freeze the mechanical and thermal design.

## Luminance (nits)

Required module luminance is driven by ambient light and by surface treatments:

- **Indoor HMI (300–500 lux):** 300–500 cd/m2 is comfortable.
- **Semi-outdoor / bright factory (≥ 10,000 lux):** direct sunlight readability wants high-bright panels (800–1,000+ cd/m2) plus anti-glare or transflective treatment.
- **Optical bonding** removes the air gap and cuts reflective losses — compare [air vs optical bonding](https://odmlcd.com/solutions/air-vs-optical-bonding).

Run the numbers with the [LCD Brightness Calculator](https://odmlcd.com/tools/lcd-brightness-calculator).

## Temperature & aging derating

Backlight LED output falls as temperature rises and as the LEDs age. Two rules of thumb:

- LED luminous flux drops roughly **0.2–0.3% per °C** above 25 °C junction reference (varies by LED bin).
- Plan for end-of-life at **L70** (70% of initial brightness) — commonly 50,000 h at 25 °C for industrial white LEDs, less at elevated temperature.

Use the [Brightness Derating Calculator](https://odmlcd.com/tools/brightness-derating-calculator) to fold both effects together and the [Backlight Lifetime Calculator](https://odmlcd.com/tools/backlight-lifetime-calculator) for L70/L50 projections.

## Power budget

Backlight is the dominant load in a display subsystem. A 7\", 500 cd/m2 LED bar can draw 1.5–3 W; high-bright 10\"+ panels run considerably higher. Size the boost/constant-current driver with margin — the [Backlight Power Calculator](https://odmlcd.com/tools/backlight-power-calculator) gives a first-pass budget, and the [Cutout & Bezel Calculator](https://odmlcd.com/tools/cutout-bezel-calculator) keeps the mechanical side consistent.

More tools: [odmlcd.com/tools](https://odmlcd.com/tools).
