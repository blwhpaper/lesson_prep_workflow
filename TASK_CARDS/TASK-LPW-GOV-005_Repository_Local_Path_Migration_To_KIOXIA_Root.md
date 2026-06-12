# TASK-LPW-GOV-005 | Repository Local Path Migration To KIOXIA Root

## Objective

Record the completed local repository path migration from `/Volumes/KIOXIA_1TB/03_COURSE_PROJECTS/lesson_prep_workflow` to `/Volumes/KIOXIA_1TB/lesson_prep_workflow` and set the default working path for future local execution.

## Boundary

- Repository governance only.
- Do not generate course content, lesson plans, PPTs, question banks, or assessments.
- Do not modify course-material正文 or `CORE_MATERIAL_MATRIX_16_SESSIONS.md`.
- Do not rename the GitHub repository.
- Do not treat `/Volumes/KIOXIA_1TB` itself as a git repository.
- Do not modify remote URL unless verification proves it is wrong.

## Repository And Course

- Repository: `lesson_prep_workflow`
- Active governance task: `TASK-LPW-GOV-005`
- Local default working path after migration: `/Volumes/KIOXIA_1TB/lesson_prep_workflow`
- Course pointer remains confirm-only for this task and does not authorize course-content generation.

## Authorized Inputs

- `README.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- local verification commands for `pwd`, `git status`, and `git remote`

## Required Outputs

- `TASK_CARDS/TASK-LPW-GOV-005_Repository_Local_Path_Migration_To_KIOXIA_Root.md`
- `CLOSEOUTS/TASK-LPW-GOV-005_Closeout.md`
- Minimal governance updates that:
  - record the local path migration as completed
  - set `/Volumes/KIOXIA_1TB/lesson_prep_workflow` as the default local working path
  - keep repository and course route pointers aligned

## Forbidden Actions

- Do not modify course content body.
- Do not modify `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`.
- Do not generate `TASK-CLCH-LESSON-001` content.
- Do not introduce BTC, NESP, Lin Yutang paper, or `Thesis_Format_Fixer` content.
- Do not change git remotes unless validation proves them incorrect.

## Acceptance Checks

- `pwd`
- `git status --short --branch`
- `git remote -v`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `test "$(pwd)" = "/Volumes/KIOXIA_1TB/lesson_prep_workflow"`
- `grep -R "/Volumes/KIOXIA_1TB/lesson_prep_workflow" -n README.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE TASK_CARDS CLOSEOUTS`
- `grep -R "/Volumes/KIOXIA_1TB/03_COURSE_PROJECTS/lesson_prep_workflow" -n README.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE TASK_CARDS CLOSEOUTS || true`
- `git diff --check`

## State And Closeout

- `TASK-LPW-GOV-004` must remain `completed`.
- `TASK-LPW-GOV-005` completes only when task card, closeout, plan, state, index, changelog, README, and SoT all agree on the path migration record.
- The next course pointer after this repository-governance patch remains `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`.

## Next Task

`TASK-CLCH-LESSON-001 | 16-Week Course Architecture`
