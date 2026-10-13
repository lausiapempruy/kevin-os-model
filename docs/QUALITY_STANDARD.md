# Resource quality standard

A resource is ready to publish when it is understandable, testable, and honest about its limits. More files do not automatically mean a better resource.

## Required checks

- [ ] **Purpose:** The resource solves a clearly named problem.
- [ ] **Scope:** It says when to use it and when not to.
- [ ] **Instructions:** Steps are actionable, ordered, and free of contradictions.
- [ ] **Accuracy:** It does not invent facts, citations, capabilities, or test results.
- [ ] **Portability:** Product-specific assumptions are marked rather than presented as universal.
- [ ] **Examples:** At least one useful example exists when the resource changes output or behavior.
- [ ] **Evaluation:** Important behavior has repeatable test cases.
- [ ] **Limits:** Known failure modes and uncertainty are documented.
- [ ] **Maintenance:** Version, owner/maintainer, and meaningful changes are recorded where appropriate.
- [ ] **Licensing:** The source and third-party assets are compatible with the stated license.

## Suggested review rubric

Score each area from 0 to 2:

| Area | 0 | 1 | 2 |
|---|---|---|---|
| Clarity | Ambiguous | Mostly clear | Direct and actionable |
| Correctness | Unsupported or wrong | Some uncertainty remains | Claims are supported and scoped |
| Usefulness | Hard to apply | Useful in common cases | Useful with clear workflow and examples |
| Robustness | No failure handling | Some edge cases covered | Edge cases and limitations are explicit |
| Evaluation | No tests | Informal examples | Repeatable cases with expected outcomes |

Maximum: 10 points. A score is a review aid, not proof of quality. Any serious factual error, unsafe instruction, or misleading guarantee blocks publication regardless of score.

## Before merging

Prefer a small, tested resource over a large, repetitive one. Remove placeholder sections, duplicated rules, and decorative complexity that does not help the user. Never claim an evaluation passed unless it was actually run and its outcome recorded.
