# TASK-CLCH-GOV-SKILL-001 Closeout

## Current Branch

`task-clch-gov-skill-001-classical-chinese-course-agent-skill-and-fail-closed-audit`

## Files Added

- `TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md`
- `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md`
- `CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`

## Files Modified

- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `AGENTS.md`
- `GEMINI.md`
- `docs/OPERATOR_GUIDE.md`

## Summary

This task inserted `TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit` between `TASK-CLCH-MAT-002` and `TASK-CLCH-LESSON-001` by explicit human-operator authorization.

It first registered the task across the governance pointers so the insertion became governable. It then added a reusable Classical Chinese audit skill focused on fail-closed checks for source authority, locator honesty, copyright or excerpt risk, maturity labeling, NotebookLM boundary, legacy-import prohibition, over-promotion risk, cross-project drift, task-scope drift, and invented content.

No lesson, slide, worksheet, question-bank, `完整教案`, `完整课件`, or `题库答案` content was produced. No material-body edits were made to `KNOWLEDGE_MAP.md` or `CORE_MATERIAL_MATRIX_16_SESSIONS.md`.

## Pointer Result

- `TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit` -> completed
- `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` -> next

## Minimum Skill Rule Added

Future Classical Chinese tasks must read `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md` after the active task card and before acting on source-derived or stage-sensitive work.

## Acceptance Commands And Results

- `pwd`: passed; current directory is `/Volumes/KIOXIA_1TB/lesson_prep_workflow`
- `git status --short --branch`: passed
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`: passed
- `test -f TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md`: passed
- `test -f .agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md`: passed
- `test -f CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`: passed
- `grep -R "TASK-CLCH-GOV-SKILL-001" -n TASK_CARDS GOVERNANCE COURSES/classical_chinese CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`: passed
- `grep -R "BTC_WATCHFLOW\\|NESP\\|Lin Yutang\\|Thesis_Format_Fixer" -n TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md .agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md || true`: passed; no content drift found
- `grep -R "完整教案\\|完整课件\\|题库答案\\|lesson-ready\\|assessment-ready\\|publication-ready" -n .agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`: passed
- `git diff --check`: passed

## Risks Or Unfinished Items

- `TASK-CLCH-LESSON-001` remains not started.
- The new skill is a governance safeguard only; it does not replace task-card authorization or source audit.
- Exact `L2` locators remain pending verification in the upstream material artifacts and must still be handled fail-closed in later tasks.
