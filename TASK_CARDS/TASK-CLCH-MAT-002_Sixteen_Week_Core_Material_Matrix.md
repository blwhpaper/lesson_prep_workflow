# TASK-CLCH-MAT-002 | Sixteen Week Core Material Matrix

## Objective

Produce a governed `16-session core material matrix` for `COURSES/classical_chinese` by converting the existing governed knowledge map into session-level material allocation below lesson-design level.

## Scope

- create `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`
- use `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md` as the required starting artifact
- distribute `matrix_fit` knowledge points across 16 sessions for a 16-week, 2-class-hours-per-week course
- record session-level `source-backed knowledge domains`, `core material slots`, `translation/research relevance`, `AI / NotebookLM use boundary`, `maturity status`, `unresolved review flags`, and `prohibited downstream use`
- preserve `source authority`, `locator`, `copyright`, and `excerpt-risk` boundaries at matrix level
- update governance pointers so `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` becomes the next task

## In Scope Outputs

- material task card
- governed `16-session core material matrix`
- closeout record
- minimal governance pointer updates

## Out Of Scope

- lesson-plan prose
- weekly lecture script
- PPT pages or slide outline
- worksheet or exercise-answer generation
- assessment-ready question bank
- long textbook excerpt collection
- direct NotebookLM output promotion
- legacy-import extraction

## Required Rules

1. The matrix must remain a material-stage artifact and must not become a full course architecture, complete lesson plan, complete courseware, or answer-key set.
2. The matrix must begin from `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md` and may allocate only governed knowledge-map content.
3. Each session entry must cover: `session number`, `session focus`, `source-backed knowledge domains`, `core material slots`, `translation/research relevance`, `AI / NotebookLM use boundary`, `maturity status`, `unresolved review flags`, and `prohibited downstream use`.
4. The artifact must preserve `L0 -> L5` source-authority boundaries and keep locator fields at `pending verification` where exact chapter or page data is not yet attached.
5. No long copyrighted textbook text may be reproduced; only structural topic labels, slot descriptors, locator placeholders, and short draft notes are allowed.
6. `LEGACY_IMPORTS/classical_chinese_translation` remains excluded from default use.
7. The matrix must explicitly state that it is not `lesson-ready`, not `assessment-ready`, not `publication-ready`, not a `完整教案`, not a `完整课件`, and not a `题库答案`.
8. Completion of this task must advance the route to `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`.

## Acceptance

Run at least:

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `test -f TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md`
- `test -f COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`
- `test -f CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md`
- `grep -R "TASK-CLCH-MAT-002" -n TASK_CARDS GOVERNANCE COURSES/classical_chinese CLOSEOUTS`
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md`
- `grep -R "lesson-ready\\|assessment-ready\\|publication-ready\\|完整教案\\|完整课件\\|题库答案" -n COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md || true`
- `grep -R "BTC_WATCHFLOW\\|Lin Yutang\\|NESP\\|Thesis_Format_Fixer" -n COURSES/classical_chinese TASK_CARDS/TASK-CLCH-MAT-002_Sixteen_Week_Core_Material_Matrix.md CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md || true`
- `git diff --check`

## Completion Condition

This task is complete only when the `16-session core material matrix` exists, every session row stays below lesson level, boundary metadata and unresolved-review flags are explicit, and governance pointers advance from `TASK-CLCH-MAT-002` to `TASK-CLCH-LESSON-001`.
