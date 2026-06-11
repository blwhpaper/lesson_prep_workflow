# TASK-CLCH-GOV-005 | Merge Legacy Classical Chinese Translation Route Into Formal Course Route

## Objective

Retire the duplicate standalone `COURSES/classical_chinese_translation` route, move its full contents under the formal `COURSES/classical_chinese` line as an isolated legacy archive, and make `COURSES/classical_chinese` the only remaining Classical Chinese course entry before `TASK-CLCH-MAT-001`.

## Scope

- create `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation/`
- move all files from the retired standalone route into that legacy-import location
- delete the top-level `COURSES/classical_chinese_translation` entry
- create a legacy README with explicit non-authority and non-default-use rules
- update governance, boundary, registry, operator, and agent-entry files so the repository recognizes only one formal Classical Chinese route
- keep `TASK-CLCH-MAT-001 | Knowledge Map Extraction` unchanged as the next task

## In Scope Outputs

- governance task card
- governance record
- closeout record
- legacy import README
- minimal route-pointer and boundary updates
- git move of the retired route into `LEGACY_IMPORTS`

## Out Of Scope

- knowledge map extraction
- `16-session core material matrix`
- lesson plans
- PPT, DOCX, or assessment generation
- promotion of any legacy governance file into current source-of-truth status
- merging old `COURSE_SOT`, `COURSE_TASK_INDEX`, or `COURSE_TASK_STATE` into top-level governance

## Required Rules

1. `COURSES/classical_chinese` must remain the only formal Classical Chinese course route.
2. `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` must be clearly labeled as isolated legacy material only.
3. All files from the retired route must be preserved, but none of its legacy governance files may become current SoT or current task state.
4. `TASK-CLCH-MAT-001 | Knowledge Map Extraction` must remain the next task after completion.
5. `TASK-CLCH-GOV-000` through `TASK-CLCH-GOV-005` must be marked completed after this task.
6. `TASK-CLCH-MAT-*`, `TASK-CLCH-LESSON-*`, and `TASK-CLCH-ASSESS-*` must ignore the legacy import unless a future task card explicitly authorizes audited legacy use.
7. This task may modify governance and route files only; it may not generate new course content.

## Acceptance

Run at least:

- `git status --short --branch`
- `find COURSES -maxdepth 2 -type d | sort`
- `test -d COURSES/classical_chinese && echo "OK formal route exists"`
- `test ! -d COURSES/classical_chinese_translation && echo "OK legacy route removed"`
- `test -d COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation && echo "OK legacy imported under formal route"`
- `git ls-files COURSES/classical_chinese_translation | wc -l`
- `git ls-files COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation | head -n 30`
- `grep -R "COURSES/classical_chinese_translation" AGENTS.md GEMINI.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE COURSES/classical_chinese docs/OPERATOR_GUIDE.md .cursor/rules/classical-chinese-course.mdc || true`
- `grep -R "LEGACY_IMPORTS/classical_chinese_translation" COURSES/classical_chinese LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md .cursor/rules/classical-chinese-course.mdc`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`
- `git diff --check`

## Completion Condition

This task is complete only when the standalone `COURSES/classical_chinese_translation` entry no longer exists, the full legacy route is preserved under `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`, the legacy README blocks direct downstream use, route pointers show `TASK-CLCH-GOV-005` completed, and `TASK-CLCH-MAT-001` remains next.
