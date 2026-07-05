# Proposal QA Rubric

Use this before delivering a proposal or when the user asks whether an IEEE idea is strong enough.

Score each dimension from 0 to 3.

| Dimension | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Problem formulation | Vague task | Dataset named | Domains and target split defined | Formal learning objective and assumptions defined |
| Mechanism novelty | Module list | Known combination | New pair/loss/protocol relation | Clear mechanism linked to failure mode |
| Mathematical readiness | No symbols | Partial symbols | Modules and losses defined | Full objective, training, inference, notation table |
| Experiment defense | Main accuracy only | Baselines present | Ablations and splits present | Baselines, ablations, sensitivity, stats, complexity |
| Claim calibration | Overclaims | Some hedging | Claims mostly evidence-bound | Every claim has evidence and boundary |
| IEEE fit | Generic ML | Signal/domain relevance | Strong Transactions-style method | Clear TCYB/THMS/TNNLS readership and engineering value |

Interpretation:

- `0-7`: Idea is not yet paper-shaped. Build formulation and evidence plan first.
- `8-12`: Proposal is plausible but vulnerable. Strengthen mechanism and experiments.
- `13-16`: Good draft candidate. Repair claim boundaries and section logic.
- `17-18`: Strong proposal. Move to manuscript drafting.

## Reviewer Risk Questions

1. Could a reviewer say this is only a combination of existing losses?
2. Is the target-domain setup hidden or too easy?
3. Are baselines missing the most relevant recent DG/contrastive/time-series methods?
4. Does every module have a removal and replacement ablation?
5. Is there a cost penalty that the paper does not discuss?
6. Are visualizations used to imply more than metrics support?
7. Does the introduction promise theory that the method section does not prove?

## Minimum Proposal Package

A proposal is ready for drafting only when it contains:

- One-sentence thesis.
- Notation table.
- Problem formulation.
- Architecture map.
- Objective functions.
- Training and inference protocol.
- Main comparison table plan.
- Ablation table plan.
- Sensitivity and complexity plan.
- Limitations that do not destroy the thesis.
