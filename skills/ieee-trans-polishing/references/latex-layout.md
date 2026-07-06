# IEEE LaTeX Layout And Notation Typesetting

Use this reference for typesetting requests: two-column float placement, wide tables, oversized equations, algorithm boxes, figure placement, sparse pages, overfull boxes, undefined references, or equations that do not integrate cleanly with text.

This file is about placement and notation presentation, not prose style.

## Diagnosis Workflow

1. Compile and read the log for:
   - `Float too large`;
   - `Overfull \hbox` or `Overfull \vbox`;
   - undefined references or citations;
   - equation, algorithm, or table overflow.
2. Render pages to images and inspect them visually. Do not judge layout from `.tex` alone.
3. Identify whether the problem is caused by figure aspect ratio, table width, equation length, float backlog, or section boundary placement.
4. Apply the smallest layout repair that preserves technical content.

## IEEE Two-Column Float Rules

- Use `figure` or `table` for single-column material.
- Use `figure*` or `table*` for material that genuinely needs both columns.
- Avoid forcing every float with `[H]`; it often creates page breaks and sparse pages.
- Prefer top placement `[t]` or `[!t]` for IEEE-style figures when possible.
- For wide equations, consider splitting aligned terms, defining intermediate quantities, or moving derivations to an appendix.

## Equation Presentation

- Keep inline variables in `$...$`.
- Use `align`, `aligned`, or `split` for multi-line objectives.
- Define long objectives through intermediate terms, for example define `$\mathcal{L}_{\mathrm{cls}}$` and `$\mathcal{L}_{\mathrm{con}}$` before the total objective.
- Do not shrink equations until they become unreadable. Rewrite the equation structure first.
- Place punctuation consistently with the surrounding sentence.

## Table Repair

- Use `booktabs` rules and avoid dense vertical lines.
- Use `\resizebox{\columnwidth}{!}{...}` only after reducing unnecessary columns and precision.
- For two-column summary tables, use `table*` and group columns with `\multicolumn`.
- Keep metric direction in headers, for example `Macro-F1 ↑` or `Error ↓`.
- Report mean and deviation in a compact format when space is limited.

## Figure Repair

- If a figure is wide and short, regenerate it with a taller aspect ratio rather than stretching it.
- If captions dominate the page, shorten the caption to protocol and notation essentials.
- Use consistent panel labels and reference them in order.
- Do not let a figure carry a claim that is absent from text or metrics.

## Algorithm Boxes

- Keep algorithm steps tied to variables already defined in the Method section.
- Avoid pseudocode that introduces symbols absent from the Notation Ledger.
- If the algorithm is too wide, split inputs, initialization, update, and output into separate lines.
- State which modules are used only during training and which remain at inference.

## Quick Checklist

- [ ] Compile is clean or remaining warnings are understood.
- [ ] Equations fit without unreadable scaling.
- [ ] Wide tables use appropriate two-column placement.
- [ ] Figures and algorithms appear near first discussion when possible.
- [ ] Every symbol in displayed math is defined in text or the Notation Ledger.
- [ ] Rendered pages have no avoidable sparse areas, stranded headings, or overfull boxes.
