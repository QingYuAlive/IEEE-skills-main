# IEEE Figure Contract Summary

Use this summary when a compact checklist is enough.

## Hard Requirements

- Backend: Python with Matplotlib/Seaborn.
- Single-column width: `3.5 in`.
- Double-column width: `7.16 in`.
- Fonts: Arial, Helvetica, or Times New Roman.
- Font sizes: title `10 pt`, axis labels `9 pt`, ticks and legend `8 pt`.
- Axis font weight: normal.
- Math rendering: `rcParams["text.usetex"] = True`.
- Exports: `.pdf` and `.png` at `600 dpi`.
- Data: exact arrays, tables, or mathematical functions supplied by the user.

## Evidence Requirements

- Ablation claims require error bars and mechanism-specific labels.
- OOD claims require explicit source/target or held-out-domain protocol.
- Feature-alignment claims require quantitative embedding diagnostics.
- Efficiency claims require runtime, memory, FLOPs, parameter count, or asymptotic notation.

## Delivery Requirement

Every figure script must include `ieee_style_setup()`, validate input dimensions, avoid fabricated data, and save both vector and inspection outputs from the same figure object.
