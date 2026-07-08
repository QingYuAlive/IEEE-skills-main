# IEEE Transactions Writing Workflow

Run this workflow for every drafting, restructuring, or section-audit task.

## 1. Verify The Math Gate

Confirm that the request includes the Notation Ledger, formal task, objective, OOD protocol, mechanism map, and evidence ledger. If not, return the blocked-gate report and stop.

## 2. Build The Technical Claim Equation

Write one internal control sentence before prose:

```text
Under source domains S and unseen target protocol T, objective L_total improves metric M because mechanism A constrains representation z through operator O, and this is tested by evidence E.
```

This sentence is a drafting control, not necessarily final manuscript prose.

## 3. Lock The Notation Ledger

Extract symbols, domains, functions, losses, weights, metrics, and protocol variables. Do not introduce a new symbol in a later paragraph unless it is added to the ledger first.

## 4. Select Section Architecture

Use the requested section fragment:

| Section | Governing contract |
|---|---|
| Abstract | Four-block IEEE abstract |
| Introduction | Formal task, OOD failure, technical mechanism, categorized contributions |
| Method | Equation-first mapping engine |
| Experiments | Bulletproof analysis playbook |

For other sections, apply the same claim-evidence discipline and open the relevant fragment or reference.

## 5. Map Paragraphs To Reviewer Questions

Every paragraph must answer exactly one reviewer question:

1. What is the formal problem?
2. What fails under the stated protocol?
3. What operator, loss, or algorithm addresses the failure?
4. Why is the mechanism defensible?
5. What evidence supports the claim?
6. What boundary remains?

Split paragraphs that answer more than one question.

## 6. Draft From Equations And Protocols

Draft prose only after the controlling equations and evidence map are available. Keep equations near the prose that interprets them. Put implementation details after the mathematical role is clear.

## 7. Calibrate Claims

Replace unsupported terms using this policy:

| Risky wording | Required condition |
|---|---|
| robust | Unseen-domain protocol plus stress or perturbation evidence |
| invariant | Defined invariance criterion plus aligned objective or penalty |
| necessary | Removal or replacement ablation |
| optimal | Theorem or exhaustive search scope |
| significant | Statistical test or explicit practical significance criterion |

## 8. Run The Defense Checklist

Before returning the draft, verify:

- All symbols in prose appear in the Notation Ledger.
- Every neural module has an equation-backed role.
- Every OOD or generalization claim names the target protocol.
- Every visualization has a quantitative companion.
- Every ablation interpretation names the removed or replaced term.
- Complexity or deployment claims include measured or asymptotic cost.
- No numbers, citations, p-values, theorem assumptions, or experiments are invented.

## 9. Return Draft Plus Audit Trail

Use `static/core/output-format.md`. Include the draft, section outline, notation used, claim-evidence map, reviewer defense notes, and missing inputs.

## Revision Rule

When the user requests changes, preserve correct mathematical definitions and alter only the affected claim, paragraph, equation, or evidence mapping. If the requested change invalidates the Notation Ledger or OOD protocol, return to the math gate before rewriting.
