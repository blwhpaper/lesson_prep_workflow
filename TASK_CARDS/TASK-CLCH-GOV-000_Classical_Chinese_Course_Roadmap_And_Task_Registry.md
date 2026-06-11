# TASK-CLCH-GOV-000 | Classical Chinese Course Roadmap And Task Registry

## Objective

Establish the governance shell, roadmap, task registry, numbering route, and anti-drift controls for the standalone `classical_chinese` course line without generating formal course content.

## Boundary

- Governance shell only.
- No lesson plan, lecture slide, handout, worksheet, weekly syllabus, question bank, or NotebookLM excerpt body is generated.
- No source is treated as confirmed course material unless already supported by repository files.
- Do not mix `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `Daily Review` workflows into this task.
- Do not advance `classical_chinese_translation` course work.

## Repository And Course

- Repository: `lesson_prep_workflow`
- Active execution task for this run: `TASK-CLCH-GOV-000`
- Existing pointer course in `CURRENT_COURSE.md`: `classical_chinese_translation`
- New governed course line created by this task: `COURSES/classical_chinese`
- This task registers the new course line but does not authorize lesson production.

## Authorized Inputs

- `README.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `CURRENT_COURSE.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/AGENT_ENTRY_PROTOCOL.md`
- `GOVERNANCE/WORKFLOW_CONTRACT.md`
- `GOVERNANCE/SOURCE_AUTHORITY_PROTOCOL.md`
- `GOVERNANCE/NOTEBOOKLM_WORKFLOW_PROTOCOL.md`
- `GOVERNANCE/ARTIFACT_MATURITY_MODEL.md`
- `GOVERNANCE/FAIL_CLOSED_RULES.md`
- `docs/OPERATOR_GUIDE.md`
- `CLOSEOUTS/TASK-LPW-GOV-004_Closeout.md`
- Active course metadata required by `AGENTS.md`

## Required Outputs

- `TASK_CARDS/TASK-CLCH-GOV-000_Classical_Chinese_Course_Roadmap_And_Task_Registry.md`
- `GOVERNANCE/TASK-CLCH-GOV-000_Classical_Chinese_Course_Roadmap_And_Task_Registry.md`
- `CLOSEOUTS/TASK-CLCH-GOV-000_Closeout.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- Consistent updates to repository state, plan, index, changelog, and operator-facing summaries

## Forbidden Actions

- Do not create formal course content.
- Do not fabricate NotebookLM output.
- Do not mark textbook, CNKI, or classical-Chinese knowledge points as confirmed course material without repository support.
- Do not skip source audit, citation boundary, maturity gating, or assessment suitability review.
- Do not jump directly from governance shell to lesson production.

## Acceptance Checks

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `grep -R "TASK-CLCH-GOV-000" -n README.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE/PLAN.md GOVERNANCE/TASK_STATE.json GOVERNANCE/TASK_INDEX.md COURSES/classical_chinese TASK_CARDS GOVERNANCE CLOSEOUTS`
- `grep -R "TASK-CLCH-GOV-001" -n GOVERNANCE/PLAN.md GOVERNANCE/TASK_STATE.json GOVERNANCE/TASK_INDEX.md COURSES/classical_chinese`
- `grep -R "NotebookLM" -n COURSES/classical_chinese GOVERNANCE/PLAN.md LESSON_PREP_WORKFLOW_SOT.md`
- `grep -R "<<<<<<<\\|=======\\|>>>>>>>" -n . || true`
- `git diff --check`

## State And Closeout

- `GOVERNANCE/TASK_STATE.json` must route to `TASK-CLCH-GOV-000` as completed and `TASK-CLCH-GOV-001` as the next pending task.
- `TASK_INDEX.md`, `PLAN.md`, `CHANGE_LOG.md`, and the closeout must agree.
- `CURRENT_COURSE.md` remains unchanged during this task; the new course line is registered but not activated through that pointer.

## Next Task

`TASK-CLCH-GOV-001 | Classical Chinese Course Boundary Bootstrap`
