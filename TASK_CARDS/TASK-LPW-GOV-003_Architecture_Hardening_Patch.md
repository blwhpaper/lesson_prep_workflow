# TASK-LPW-GOV-003 | Architecture Hardening Patch

## Objective

Harden the repository architecture and governance boundaries without generating course content, lesson plans, question banks, student-facing tasks, or assessment bodies.

## Boundary

- Repository governance only.
- No course task is advanced.
- No external repository is read.
- No NotebookLM output is promoted beyond draft / extracted / unverified status.
- No source-audited, lesson-ready, or assessment-ready claim may be created without evidence.

## Repository And Course

- Repository: `lesson_prep_workflow`
- Active governance task: `TASK-LPW-GOV-003`
- Active course pointer: `classical_chinese_translation`
- Course pointer is confirm-only and does not authorize `TASK-CLCH-*` execution.

## Authorized Inputs

- `README.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `CURRENT_COURSE.md`
- `GOVERNANCE/*.md`
- `GOVERNANCE/TASK_STATE.json`
- `TASK_CARDS/TASK_CARD_TEMPLATE.md`
- `CLOSEOUTS/TASK-LPW-GOV-002_Closeout.md`
- Active course metadata required by `AGENTS.md`

## Required Outputs

- Architecture hardening governance patch record
- Updated repository governance state and route pointers
- Strengthened governance protocols for:
  - agent entry / fail-closed entry
  - workflow architecture layers
  - source authority boundaries
  - NotebookLM intake boundaries
  - artifact maturity boundaries
  - public GitHub publication boundaries
- Task closeout for `TASK-LPW-GOV-003`

## Forbidden Actions

- Do not generate lesson plans.
- Do not expand `classical_chinese_translation` teaching content.
- Do not generate question banks, answer keys, PPTs, or student handouts.
- Do not introduce external scraped material.
- Do not treat NotebookLM output as approved source material.
- Do not implement `TASK-LPW-GOV-004`.

## Acceptance Checks

- `git status --short --branch`
- `git diff --check`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `grep -R "^<<<<<<<\\|^=======\\|^>>>>>>>" -n . --exclude-dir=.git`
- verify that no repository document mislabels `TASK-LPW-GOV-003` as source-audit or NotebookLM-review work
- `grep -R "Architecture Hardening Patch" -n GOVERNANCE TASK_CARDS CLOSEOUTS README.md LESSON_PREP_WORKFLOW_SOT.md docs`
- `test -f GOVERNANCE/TASK-LPW-GOV-003_Architecture_Hardening_Patch.md`
- `test -f CLOSEOUTS/TASK-LPW-GOV-003_Closeout.md`

## State And Closeout

- `TASK-LPW-GOV-002` must remain `completed`.
- `TASK-LPW-GOV-003` completes only when plan, state, index, changelog, task card, patch record, and closeout agree.
- After completion, the governance pointer advances to `TASK-LPW-GOV-004 | Prompt Governance And NotebookLM Intake Contract`.

## Next Task

`TASK-LPW-GOV-004 | Prompt Governance And NotebookLM Intake Contract`
