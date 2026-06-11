# TASK-LPW-GOV-004 | Prompt Governance And NotebookLM Intake Contract

## Objective

Establish repository-level governance for prompt creation, NotebookLM intake, output review, maturity labeling, publication boundaries, and agent-executable limits without generating any course content.

## Boundary

- Repository governance only.
- No course task is advanced.
- No lesson plan, syllabus, assessment body, or course material is generated.
- No external repository is read.
- No NotebookLM output is promoted above `draft` / `extracted` / `unverified`.
- No copyrighted full text, student privacy data, or internal sensitive material is prepared for publication.

## Repository And Course

- Repository: `lesson_prep_workflow`
- Active governance task: `TASK-LPW-GOV-004`
- Active course pointer: `classical_chinese_translation`
- Course pointer is confirm-only and does not authorize `TASK-CLCH-*` execution.

## Authorized Inputs

- `README.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `CURRENT_COURSE.md`
- `GOVERNANCE/*.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/PLAN.md`
- `TASK_CARDS/TASK_CARD_TEMPLATE.md`
- `TASK_CARDS/TASK-LPW-GOV-003_Architecture_Hardening_Patch.md`
- `CLOSEOUTS/TASK-LPW-GOV-003_Closeout.md`
- Active course metadata required by `AGENTS.md`

## Required Outputs

- `TASK_CARDS/TASK-LPW-GOV-004_Prompt_Governance_And_NotebookLM_Intake_Contract.md`
- `GOVERNANCE/TASK-LPW-GOV-004_Prompt_Governance_And_NotebookLM_Intake_Contract.md`
- `CLOSEOUTS/TASK-LPW-GOV-004_Closeout.md`
- Minimal governance updates for:
  - prompt contract fields
  - NotebookLM intake record expectations
  - review gates and fail-closed publication limits
  - maturity-label handling for prompt and NotebookLM artifacts
  - task-state and route-pointer consistency

## Forbidden Actions

- Do not generate specific course prompts, lesson plans, or question banks.
- Do not write specific `classical_chinese_translation` teaching content.
- Do not introduce NESP, BTC, Lin Yutang, or `Thesis_Format_Fixer` assumptions.
- Do not treat prompts as formal lesson artifacts.
- Do not treat NotebookLM output as approved source material.
- Do not upload or normalize copyrighted textbook full text, scans, OCR dumps, student data, or internal sensitive material.
- Do not define a full body for `TASK-LPW-GOV-005` if it remains unauthorized.

## Acceptance Checks

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `grep -R "^<<<<<<<\\|^=======\\|^>>>>>>>" -n .`
- `grep -R "Prompt Governance And NotebookLM Intake Contract" -n GOVERNANCE TASK_CARDS CLOSEOUTS README.md LESSON_PREP_WORKFLOW_SOT.md docs`
- `git diff --check`

## State And Closeout

- `TASK-LPW-GOV-003` must remain `completed`.
- `TASK-LPW-GOV-004` completes only when task card, governance contract, closeout, state, plan, index, changelog, and related protocol updates agree.
- `TASK-LPW-GOV-005` may be referenced only as the next pointer. Without an approved definition, it must remain `placeholder / needs_task_definition`.

## Next Task

`TASK-LPW-GOV-005 | placeholder / needs_task_definition`
