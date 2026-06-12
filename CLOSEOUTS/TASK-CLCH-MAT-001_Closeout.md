# TASK-CLCH-MAT-001 Closeout

## Current Branch

`task-clch-mat-001-knowledge-map-extraction`

## Files Added

- `TASK_CARDS/TASK-CLCH-MAT-001_Knowledge_Map_Extraction.md`
- `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md`
- `CLOSEOUTS/TASK-CLCH-MAT-001_Closeout.md`

## Files Modified

- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`

## Summary

This task created the first governed knowledge-map extraction artifact for the formal `COURSES/classical_chinese` line. The artifact stays below lesson level, names only authorized source-package titles, defines eight first-level knowledge domains, and tags second-level knowledge points by learning value, prerequisite, teaching use, translation relevance, AI prompt potential, and source dependency.

It also distinguishes future `16-session core material matrix` candidates from teacher-background-only reserve topics, and it keeps explicit anti-drift and anti-copyright rules in place.

## Route Result

- `TASK-CLCH-MAT-001 | Knowledge Map Extraction` -> completed
- `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` -> next

## Acceptance Commands And Results

- `git status --short --branch`: passed
- `find COURSES/classical_chinese -maxdepth 4 -type f | sort`: passed
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`: passed
- `grep -R "TASK-CLCH-MAT-001" -n TASK_CARDS GOVERNANCE COURSES/classical_chinese CLOSEOUTS`: passed
- `grep -R "BTC_WATCHFLOW\\|Lin Yutang\\|NESP\\|Thesis_Format_Fixer" -n COURSES/classical_chinese TASK_CARDS/TASK-CLCH-MAT-001_Knowledge_Map_Extraction.md CLOSEOUTS/TASK-CLCH-MAT-001_Closeout.md || true`: passed; hits are limited to governance anti-drift rules and command text, not content drift
- `git diff --check`: passed

## Risks Or Unfinished Items

- The knowledge map is structure-only and still requires later source-locator attachment during downstream extraction or matrix work.
- No lesson prose, PPT, weekly schedule, question bank, or textbook excerpt library was generated.
