# TASK-CLCH-GOV-005 Closeout

## Current Branch

`task-clch-gov-005-merge-legacy-classical-chinese-translation-route`

## Files Added

- `TASK_CARDS/TASK-CLCH-GOV-005_Merge_Legacy_Classical_Chinese_Translation_Route_Into_Formal_Course_Route.md`
- `GOVERNANCE/TASK-CLCH-GOV-005_Merge_Legacy_Classical_Chinese_Translation_Route_Into_Formal_Course_Route.md`
- `CLOSEOUTS/TASK-CLCH-GOV-005_Closeout.md`
- `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation/README.md`

## Files Modified

- `AGENTS.md`
- `GEMINI.md`
- `.cursor/rules/classical-chinese-course.mdc`
- `docs/OPERATOR_GUIDE.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`

## Files Moved

- `COURSES/classical_chinese_translation/**` -> `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation/**`

## Summary

This task retired the duplicate standalone `COURSES/classical_chinese_translation` route and preserved its full contents under `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` as quarantined legacy material.

It also updated the formal-route governance files so `COURSES/classical_chinese` is the only Classical Chinese course entry, kept the legacy route out of source-of-truth status, and preserved `TASK-CLCH-MAT-001 | Knowledge Map Extraction` as the next task.

## Legacy Isolation Rules

- `COURSES/classical_chinese` is the only formal route
- `LEGACY_IMPORTS/classical_chinese_translation` is archive-only legacy material
- old legacy governance files remain archival and do not override formal-route or top-level governance state
- downstream `MAT`, `LESSON`, and `ASSESS` tasks must ignore legacy imports unless a future task card explicitly authorizes audited use

## Acceptance Commands And Results

- `git status --short --branch`: passed
- `find COURSES -maxdepth 2 -type d | sort`: passed
- `test -d COURSES/classical_chinese && echo "OK formal route exists"`: passed
- `test ! -d COURSES/classical_chinese_translation && echo "OK legacy route removed"`: passed
- `test -d COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation && echo "OK legacy imported under formal route"`: passed
- `git ls-files COURSES/classical_chinese_translation | wc -l`: passed; result `0`
- `git ls-files COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation | head -n 30`: passed
- `grep -R "COURSES/classical_chinese_translation" AGENTS.md GEMINI.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE COURSES/classical_chinese docs/OPERATOR_GUIDE.md .cursor/rules/classical-chinese-course.mdc || true`: passed; only legacy-archive references remain
- `grep -R "LEGACY_IMPORTS/classical_chinese_translation" COURSES/classical_chinese LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md .cursor/rules/classical-chinese-course.mdc`: passed
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`: passed
- `git diff --check`: passed

## Risks Or Unfinished Items

- `TASK-CLCH-MAT-001` remains not started.
- No knowledge extraction, lesson design, PPT generation, or assessment generation was performed in this task.
