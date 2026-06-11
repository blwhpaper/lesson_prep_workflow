# TASK-CLCH-GOV-005 | Merge Legacy Classical Chinese Translation Route Into Formal Course Route

## Purpose

This governance record retires the duplicate standalone `COURSES/classical_chinese_translation` route, preserves its files as a quarantined legacy archive inside the formal `COURSES/classical_chinese` line, and removes the ambiguous second entry point before material extraction begins.

## Formal Route Rule

- `COURSES/classical_chinese` is the only formal Classical Chinese route
- it is the only valid planning, governance, and downstream task entry for `TASK-CLCH-*`
- `TASK-CLCH-MAT-001 | Knowledge Map Extraction` and later tasks must start from the formal route only

## Legacy Archive Rule

- the retired standalone route is preserved only at `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`
- the legacy archive is not a current course line, not a source of truth, and not a default read target
- archived files such as `COURSE_SOT.md`, `COURSE_TASK_INDEX.md`, and `COURSE_TASK_STATE.json` remain historical artifacts only
- no legacy governance file is merged into `LESSON_PREP_WORKFLOW_SOT.md`, `GOVERNANCE/TASK_STATE.json`, or the formal course route files

## Downstream Use Restriction

- `TASK-CLCH-MAT-*`, `TASK-CLCH-LESSON-*`, and `TASK-CLCH-ASSESS-*` must ignore the legacy archive by default
- a future task may use legacy material only when its task card explicitly authorizes that use and requires source audit
- even when authorized later, legacy content may be treated only as candidate material, never as automatic source-of-truth content

## Repository Outcome

- duplicate top-level course entry removed: `COURSES/classical_chinese_translation`
- single formal course entry retained: `COURSES/classical_chinese`
- complete legacy file set preserved under `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`
- route pointer advanced only by recording `TASK-CLCH-GOV-005` as completed
- next route unchanged: `TASK-CLCH-MAT-001 | Knowledge Map Extraction`
