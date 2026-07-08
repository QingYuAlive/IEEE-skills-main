# Language: Chinese-To-English

When the source is Chinese or strongly Chinese-influenced English, do not translate clause by clause. Convert the note into IEEE-style technical logic first.

## Workflow

1. Extract the formal propositions: task, input, output, domains, objective, protocol, evidence, and limitation.
2. Reconstruct explicit logical links: contrast, cause, mechanism, ablation, implication, and boundary.
3. Verify terminology, notation, causality, and hedging strength against the source.
4. Keep model names, dataset names, variables, losses, metrics, and statistical terms stable.
5. Apply English sentence and paragraph rules only after the technical logic is rebuilt.

## Common Chinese-Influenced Patterns To Fix

- Topic-comment chains rewritten as subject-verb technical claims.
- Strings of short clauses joined by commas split into condition, mechanism, evidence, and limitation.
- Vague generalizations converted to specific citations, protocols, or removed.
- Understated or overstated hedging recalibrated to evidence strength.
- Informal references to `this dataset`, `this method`, or `this feature` replaced with the defined notation or canonical term.

## Output Note

When making substantial structural changes, briefly explain in Chinese why the change improves IEEE reviewer defense.
