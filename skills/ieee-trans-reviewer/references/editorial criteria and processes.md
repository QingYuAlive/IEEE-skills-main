# IEEE Transactions Review Criteria And Processes

This local file replaces the previous venue-specific editorial source with IEEE Transactions-style review criteria used by this skill.

## Technical Review Criteria

An IEEE Transactions manuscript is treated as high risk when:

- the learning problem is not formalized;
- notation is incomplete or inconsistent;
- equations do not match the implemented network or algorithm;
- theoretical claims lack assumptions, proof, bound, or convergence statement;
- experiments do not match the claimed protocol;
- baselines are weak, outdated, unfair, or missing;
- ablations do not isolate the claimed mechanism;
- complexity is omitted despite added modules or deployment claims;
- claims exceed evidence.

## Expected Manuscript Evidence

For machine-learning and neural-network papers, the review expects:

- problem definition with `$\mathcal{X}$`, `$\mathcal{Y}$`, domains, and predictor;
- formal objective and all auxiliary loss terms;
- algorithmic training schedule and inference path;
- theorem or bound when theory is claimed;
- strict held-out target protocol for DG and OOD claims;
- baseline tiers including recent relevant methods;
- ablations for modules, losses, stages, pair construction, and hyperparameters;
- statistical reporting or repeated-fold metrics where appropriate;
- time and memory complexity plus measured cost when efficiency is claimed.

## Review Process Used By This Skill

1. Extract claims and evidence from the supplied manuscript.
2. Attack the mathematical formulation.
3. Attack the empirical protocol.
4. Attack the claim wording.
5. Classify issues by severity.
6. Return actionable directives required before submission.

## Boundary

This file is not an official IEEE policy document. It is a local review standard derived from the shared IEEE Transactions guidelines bundled in this repository.
