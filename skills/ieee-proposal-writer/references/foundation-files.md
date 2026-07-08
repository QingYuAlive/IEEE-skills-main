# IEEE Foundation Files

Use these files to build an IEEE Transactions proposal foundation. The goal is not storytelling completeness; the goal is to make every claim mathematically defined and empirically defensible before drafting.

## 00_scope.md

Records:

- Target venue: TCYB, THMS, TNNLS, or generic IEEE Transactions.
- Task: classification, regression, diagnosis, generation, representation learning, multimodal fusion.
- Signal/data type: sEMG, EEG, IMU, industrial time series, bearing/fault signals, or other.
- OOD variable: subject, session, force, load, machine condition, dataset, modality, label noise.
- Deliverable: formal proposal, method blueprint, experiment plan, pre-submission QA, or revision.
- Current gate status: math gate, evidence gate, theory gate.

## 01_research_canon.md

Hard facts and boundaries:

- Dataset facts: sampling rate, channel count, windowing, preprocessing, labels, subjects/domains.
- Literature facts: what current CNN/RNN/Transformer, DG, IRM, GroupDRO, contrastive, or robust-learning methods assume.
- Method facts: modules, mappings, losses, training stages, inference path.
- Forbidden claims: any robustness/generalization/invariance claim not supported by OOD protocol.
- Unresolved claims: claims needing ablation, theorem, or additional experiment.

Rule: drafting cannot silently upgrade canon.

## 02_evidence_table.md

Claim-evidence map:

```text
claim | formal object | evidence/source | OOD protocol | strength | risk | status
```

Status values:

```text
formalized
evidence-backed
ablation-needed
theory-needed
unsupported
forbidden
```

## 03_argument_map.md

Theorem-Proof / Ablation-Defense architecture. It links each central claim to assumptions, objectives, proof or mechanism analysis, OOD tests, ablations, and complexity.

## 04_section_contracts.md

For each manuscript section: purpose, mathematical inputs, allowed claims, forbidden claims, required equations, required evidence, validation checklist.

## 05_style_guide.md

IEEE technical style:

- equation-first
- protocol-bound claims
- no layer-by-layer plain-English method prose
- no unsupported "robust", "invariant", "generalizable", or "state of the art"
- no visual-proof language for t-SNE/PCA/confusion matrices

## Creation Order

1. Fill `00_scope.md`.
2. Fill formal facts in `01_research_canon.md`.
3. Build `02_evidence_table.md`.
4. Build `03_argument_map.md`.
5. Build `04_section_contracts.md`.
6. Build `05_style_guide.md`.
7. Only then draft.
