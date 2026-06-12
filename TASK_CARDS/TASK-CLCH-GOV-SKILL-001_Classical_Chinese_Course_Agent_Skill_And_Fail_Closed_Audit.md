# TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit

## Task Type

- task family: `TASK-CLCH-GOV-*`
- scope: governance insertion patch
- stage: between `TASK-CLCH-MAT-002` and `TASK-CLCH-LESSON-001`
- default mode: fail closed

## Task Intent

This task is an explicitly authorized governance insertion between the completed material route and the not-yet-started lesson route.

Its first goal is to register `TASK-CLCH-GOV-SKILL-001` across the Classical Chinese governance system so the task becomes governable.

Its second goal is to create a reusable agent skill that audits fail-closed risk before later Classical Chinese tasks act on source-derived or stage-sensitive material.

This task does not authorize any `TASK-CLCH-LESSON-*` content generation and does not advance lesson prose, slide structure, worksheet detail, assessment content, or answer keys.

## Upstream Preconditions

- `TASK-CLCH-MAT-001 | Knowledge Map Extraction` is completed.
- `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` is completed.
- `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md` remains unchanged in this task.
- `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md` remains unchanged in this task.
- `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` remains prohibited as a working input.

## Required Inputs

1. `README.md`
2. `LESSON_PREP_WORKFLOW_SOT.md`
3. `AGENTS.md`
4. `GEMINI.md`
5. `docs/OPERATOR_GUIDE.md`
6. `GOVERNANCE/PLAN.md`
7. `GOVERNANCE/TASK_STATE.json`
8. `GOVERNANCE/TASK_INDEX.md`
9. `GOVERNANCE/CHANGE_LOG.md`
10. `COURSES/classical_chinese/COURSE_BOUNDARY.md`
11. `COURSES/classical_chinese/ROADMAP.md`
12. `COURSES/classical_chinese/TASK_REGISTRY.md`
13. `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md`
14. `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`
15. `CLOSEOUTS/TASK-CLCH-MAT-002_Closeout.md`
16. `CLOSEOUTS/TASK-LPW-GOV-005_Closeout.md`

## Required Outputs

- governance registration of `TASK-CLCH-GOV-SKILL-001` across route pointers
- `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md`
- `CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`

## Skill Scope Requirements

The skill must provide a reusable Classical Chinese fail-closed audit checklist that covers:

- source authority
- locator honesty
- copyright and excerpt risk
- maturity status
- NotebookLM output boundary
- legacy imports prohibition
- lesson-ready over-promotion risk
- assessment-ready over-promotion risk
- publication-ready over-promotion risk
- cross-project drift
- task-scope drift
- source-backed versus invented content

## Allowed Changes

- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `AGENTS.md`
- `GEMINI.md`
- `docs/OPERATOR_GUIDE.md`
- `README.md` only if needed to register the skill path
- `LESSON_PREP_WORKFLOW_SOT.md` only if needed to register the skill path

## Disallowed Work

- do not generate lesson plans, lesson architecture prose, slides, handouts, question banks, papers, or answer keys
- do not modify `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md`
- do not modify `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`
- do not quote or reconstruct long textbook passages
- do not use legacy imports except as prohibited inputs
- do not drift into unrelated project lines
- do not change the GitHub remote
- do not change the local repository path

## Route Result Requirement

At closeout, the governance pointers must resolve to:

- `TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit` = completed
- `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` = next

## Acceptance Commands

- `pwd`
- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `test -f TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md`
- `test -f .agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md`
- `test -f CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`
- `grep -R "TASK-CLCH-GOV-SKILL-001" -n TASK_CARDS GOVERNANCE COURSES/classical_chinese CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`
- `grep -R "BTC_WATCHFLOW\\|NESP\\|Lin Yutang\\|Thesis_Format_Fixer" -n TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md .agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md || true`
- `grep -R "完整教案\\|完整课件\\|题库答案\\|lesson-ready\\|assessment-ready\\|publication-ready" -n .agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md TASK_CARDS/TASK-CLCH-GOV-SKILL-001_Classical_Chinese_Course_Agent_Skill_And_Fail_Closed_Audit.md CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`
- `git diff --check`
