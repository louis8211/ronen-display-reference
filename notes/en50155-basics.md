# EN 50155 — system-level view

EN 50155 is the European standard for **electronic equipment used on rolling stock (railway vehicles)**. This note is a plain-language orientation for system designers — it is **not a certification claim** for any display module.

> Scope discipline: EN 50155 certifies a **system or piece of equipment** for rail use. A bare LCD module is a component; rail suitability depends on how it is integrated, powered and protected. Always evaluate at system level and confirm the actual test reports your supplier can provide for the assembly you are buying.

## What the standard covers

1. **Supply voltages** — nominal 24 V / 48 V / 72 V / 110 V battery systems, including brown-out and surge behaviour.
2. **Temperature classes** — e.g. TX classes from −25 °C up to +70 °C operating, with specified humidity and thermal shock.
3. **Shock & vibration** — mechanical robustness per IEC 61373 categories (body-mounted / bogie / axle equipment differ).
4. **EMC** — emissions and immunity appropriate for rail electrical environment (referenced to EN 50121-3-2 and related parts).

## Display-relevant questions to ask

- Is the **module** rated for the temperature class you need (industrial −20…+70 °C or extended)?
- Is the **backlight** derated correctly at temperature? ([derating calculator](https://odmlcd.com/tools/brightness-derating-calculator))
- Does the **FPC and bonding** survive the vibration category? ([FPC bending radius](https://odmlcd.com/tools/fpc-bending-radius-calculator))
- What test reports exist for the **complete assembly**, not just the panel?

## Reference

Free plain-language reference: [EN 50155 Reference tool](https://odmlcd.com/tools/en50155-reference) and the [Certification Checklist](https://odmlcd.com/tools/certification-checklist) at odmlcd.com.
