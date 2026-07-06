# IEEE Reviewer QA Checklist

Run this checklist before releasing a report.

## Grounding Checks

- Every issue is traceable to supplied manuscript material, missing material, or `../_shared/ieee-trans-guidelines.md`.
- No experiments, datasets, baselines, citations, line numbers, or figure details are invented.
- Missing material is explicitly labeled `not assessable from provided material`.
- The report does not assume that absent ablations or proofs exist elsewhere.

## Structure Checks

- The report contains `Review Verdict`.
- `Fatal Flaws / Major Concerns` is divided into:
  - `Theoretical/Mathematical Loopholes`;
  - `Empirical/Ablation Gaps`;
  - `Protocol, Leakage, And Reproducibility Risks`.
- The report contains `Minor Concerns`.
- The report contains `Claim-Calibration Audit`.
- The report contains `Actionable Directives`.
- The report ends with `Submission Readiness Gate`.

## Math And Theory Checks

- Undefined variables are flagged.
- Equations are checked against architecture, objective, training, and inference.
- Theoretical claims are checked for assumptions, proofs, bounds, and implementation match.
- Big-O time and memory complexity is requested when missing.
- Training-only and inference-time modules are distinguished.

## Empirical Defense Checks

- OOD, DG, robustness, and generalization claims are checked against strict held-out protocols.
- Baselines are checked for recency, relevance, fairness, and comparable budgets.
- Ablations are checked for every proposed module, loss, stage, pair rule, and hyperparameter.
- Visualizations are checked for quantitative companion metrics.
- Statistical or practical significance wording is checked for support.

## Claim-Calibration Checks

Flag unsupported uses of:

- `robust`;
- `generalizable`;
- `domain-invariant`;
- `state of the art`;
- `significant`;
- `necessary`;
- `proves`;
- `completely solves`;
- `efficient`;
- `real-time`.

## Tone And Role Checks

- No praise of prose quality, stylistic polish, accessibility, or venue fit.
- No author rebuttal language.
- No final editorial decision stated as fact.
- No fabricated reviewer identities or specialist personas.
- Tone is direct, critical, and evidence-based.
