# TASK-CLCH-MAT-002 Closeout

## Current Branch

`task-clch-mat-002-sixteen-week-core-material-matrix`

## Files Added

- `TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md`
- `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`
- `CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md`

## Files Modified

- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`

## Summary

This task converted the existing governed knowledge map into a `16-session core material matrix` for the formal `COURSES/classical_chinese` route. The matrix allocates session-level focus areas, keeps all entries below lesson level, and records source-backed domains, material slots, translation/research relevance, AI or NotebookLM use boundaries, maturity labels, unresolved review flags, and prohibited downstream use.

The artifact preserves the `L0 -> L5` source-authority ladder, keeps exact source locators at `pending verification` where not yet attached, excludes `LEGACY_IMPORTS`, and explicitly states that the matrix is not `lesson-ready`, not `assessment-ready`, not `publication-ready`, not a `完整教案`, not a `完整课件`, and not a `题库答案`.

## Route Result

- `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` -> completed
- `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` -> next

## Acceptance Commands And Results

- `git status --short --branch`: passed; branch is `task-clch-mat-002-sixteen-week-core-material-matrix`; expected modified and new files are present
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`: passed
- `test -f TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md`: passed
- `test -f COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`: passed
- `test -f CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md`: passed
- `grep -R "TASK-CLCH-MAT-002" -n TASK_CARDS GOVERNANCE COURSES/classical_chinese CLOSEOUTS`: passed; task card, matrix artifact, governance pointers, and closeout all resolve
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md`: passed; next-task pointer resolves across governance and course files
- `grep -R "lesson-ready\\|assessment-ready\\|publication-ready\\|完整教案\\|完整课件\\|题库答案" -n COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md || true`: passed; required non-promotion boundaries are explicit
- `grep -R "BTC_WATCHFLOW\\|Lin Yutang\\|NESP\\|Thesis_Format_Fixer" -n COURSES/classical_chinese TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md || true`: passed; hits are limited to existing anti-drift governance text and command text, not content drift
- `git diff --check`: passed

## Risks Or Unfinished Items

- Exact `L2` chapter, section, or page locators are still pending verification across session slots.
- No lesson prose, PPT structure, worksheet detail, question bank, or answer-key content was generated.
- Later lesson-stage work must still perform source audit, material selection, and maturity review before any classroom-facing artifact is drafted.
