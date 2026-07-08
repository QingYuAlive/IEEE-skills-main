# IEEE Red-Team Report Structure

Use this structure for the default output. Do not output multiple simulated reviewer reports. Do not include praise sections. Do not evaluate accessibility or stylistic polish.

## Default Output Contract

```text
Review Verdict
Fatal Flaws / Major Concerns
  A. Theoretical/Mathematical Loopholes
  B. Empirical/Ablation Gaps
  C. Protocol, Leakage, And Reproducibility Risks
Minor Concerns
Claim-Calibration Audit
Actionable Directives
Submission Readiness Gate
```

## Review Verdict

Include:

- `Overall risk level`: `fatal flaw`, `major revision risk`, `moderate revision risk`, or `minor revision risk`.
- `Most likely editorial outcome if submitted now`: phrase as risk, not certainty.
- `Central reason`: one or two sentences naming the dominant failure.
- `Assessment boundary`: state what was and was not provided.

## Fatal Flaws / Major Concerns

Each issue must use this format:

```text
[Severity: Fatal flaw or Major concern] [Category]
Issue: ...
Evidence from supplied material: ...
Why this threatens acceptance: ...
Required fix: ...
```

### A. Theoretical/Mathematical Loopholes

Use this group for:

- undefined variables;
- inconsistent notation;
- equations that do not match architecture;
- missing objective;
- missing proof, bound, or assumptions;
- missing convergence or complexity analysis;
- unclear inference path.

### B. Empirical/Ablation Gaps

Use this group for:

- missing recent baselines;
- unfair training budgets;
- missing ablations;
- missing sensitivity for `$\lambda$`, `$\tau$`, margin, perturbation ratio, group weight, or mix coefficient;
- missing negative sampling or positive-pair ablations;
- missing worst-domain performance;
- visualization-only evidence.

### C. Protocol, Leakage, And Reproducibility Risks

Use this group for:

- invalid random split for DG claims;
- target leakage through normalization, checkpointing, tuning, or preprocessing;
- unclear seed, fold, or checkpoint rule;
- missing subject/trial/session split definition;
- incomplete preprocessing and hyperparameter reporting.

## Minor Concerns

Use concise bullets for:

- notation inconsistency that does not invalidate the claim;
- missing citations or weak positioning;
- unclear dataset or metric naming;
- local table or figure reporting issues;
- grammar or wording only when it changes technical meaning.

Do not put missing objectives, invalid protocols, or absent core ablations here.

## Claim-Calibration Audit

Create a table:

| Original claim | Problem | Required calibrated wording or evidence |
|---|---|---|
| `Our method completely solves the robustness problem.` | Universal robustness claim without OOD protocol. | Restrict to the tested held-out target protocol or add stress tests. |

Flag claims involving:

- `robust`;
- `generalizable`;
- `domain-invariant`;
- `state of the art`;
- `significant`;
- `necessary`;
- `proves`;
- `completely solves`;
- `efficient` or `real-time`.

## Actionable Directives

Write directives as mandatory author actions:

- `Provide a formal definition of the positive pair set $P(i)$ before introducing $\mathcal{L}_{\mathrm{con}}$.`
- `Run sensitivity analysis for $\lambda_{\mathrm{con}}$ and temperature $\tau$.`
- `Add a strict LODO protocol and ensure target-domain statistics are not used in normalization or checkpoint selection.`
- `Add recent baselines from the last three years and match input, backbone, and training budget.`
- `Report Big-O time and memory complexity and measured inference latency.`
- `Add removal and replacement ablations for each proposed loss term and stage.`

Group directives by priority:

1. `Must add before submission`
2. `Strongly recommended for avoiding major revision`
3. `Clarify in text or appendix`

## Submission Readiness Gate

End with one of:

- `Not submission-ready: central claim is not mathematically or empirically established.`
- `Major-revision risk: central idea may be viable, but key proof, protocol, or ablation gaps remain.`
- `Moderate risk: main evidence appears plausible, but reporting and claim calibration require repair.`
- `Low risk from provided material: no fatal technical flaw is visible, but this is bounded by the supplied excerpt.`

Never state final acceptance or rejection as a fact.

## Structured JSON Schema

Use this schema when the user requests machine-readable output:

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": [
    "review_verdict",
    "fatal_flaws_major_concerns",
    "minor_concerns",
    "claim_calibration_audit",
    "actionable_directives",
    "submission_readiness_gate"
  ],
  "properties": {
    "review_verdict": {
      "type": "object",
      "required": ["overall_risk_level", "most_likely_editorial_risk", "central_reason", "assessment_boundary"]
    },
    "fatal_flaws_major_concerns": {
      "type": "object",
      "required": ["theoretical_mathematical_loopholes", "empirical_ablation_gaps", "protocol_leakage_reproducibility_risks"]
    },
    "minor_concerns": {"type": "array", "items": {"type": "string"}},
    "claim_calibration_audit": {"type": "array", "items": {"type": "object"}},
    "actionable_directives": {"type": "array", "items": {"type": "object"}},
    "submission_readiness_gate": {"type": "string"}
  }
}
```
