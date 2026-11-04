# Display interfaces — LVDS / MIPI DSI / eDP / RGB

A field guide to the four interface families you will meet when selecting an industrial TFT LCD module. Written for hardware and firmware engineers doing board-level design.

## TL;DR decision table

| Interface | Typical use | Bandwidth | Cable / connector | Notes |
|---|---|---|---|---|
| RGB (DPI) | Small MCU-driven panels (≤ 5\") | Low–mid | Many traces | Simplest; needs continuous clock, eats MCU pins |
| MCU (8080/6800) | Character / small TFT | Low | Fewer than RGB | Own GRAM on panel; easy for slow UIs |
| LVDS | Medium/large industrial panels (7–21.5\") | Mid–high | Fine-pitch FPC / wire-to-board | Mature, long trace tolerance, common in medical / HMI |
| MIPI DSI | Mobile-derived panels, high resolution | High | Short FPC | Low EMI per lane, needs D-PHY host |
| eDP | Large / high-res panels (≥ 12.1\") | High | Coax-ish eDP cable | Fewer lanes than LVDS for same bandwidth, hot-plug variants |

## Design notes

1. **RGB vs LVDS at 7\":** RGB needs ~24 data + 3 sync + clock lines routed with matched length. LVDS serializes this into 3–5 differential pairs — far easier EMC story, and the usual choice once the panel gets above about 5 inches.
2. **MIPI DSI lane count:** 1 / 2 / 4 data lanes. A 1024x600 60 Hz panel is comfortable on 2 lanes; 1280x800 and above usually wants 4. Remember the D-PHY host must support the lane count the panel's firmware expects.
3. **eDP vs LVDS on new designs:** eDP wins on connector count and power for high resolution, but LVDS panel availability in industrial temperature grades is still wider. Check module availability first, route the interface second.
4. **FPC routing:** see the [FPC Bending Radius Calculator](https://odmlcd.com/tools/fpc-bending-radius-calculator) before you fix the fold geometry — copper fatigue is a top field failure.

## Pick your interface

Use the free [Display Interface Selector](https://odmlcd.com/tools/display-interface-selector) and, for RGB/MCU timing, the [MCU Timing Generator](https://odmlcd.com/tools/mcu-timing-generator).

More: [Industrial LCD datasheet decoder](https://odmlcd.com/blog/industrial-lcd-datasheet-decoder) at odmlcd.com.
