# TASK-CLCH-GOV-001 | Classical Chinese Course Boundary Bootstrap

## Objective

Establish the boundary bootstrap layer for the standalone `classical_chinese` course line so future agents can safely execute `TASK-CLCH-*` work without drifting into unauthorized content generation, source misuse, NotebookLM over-promotion, or AI-method substitution.

## Boundary

- Governance shell only.
- No formal lesson plan, 16-week lesson prose, slide deck, worksheet, assignment detail, question bank, or teaching script is generated.
- No textbook long excerpt, no unaudited NotebookLM output, and no memorized course content may be promoted as approved course material.
- No cross-course borrowing from `classical_chinese_translation`.
- No external repository or network course-content intake is authorized by this task.

## Repository And Course

- Repository: `lesson_prep_workflow`
- Active execution task for this run: `TASK-CLCH-GOV-001`
- Governed course line for this task: `COURSES/classical_chinese`
- Existing default pointer in `CURRENT_COURSE.md`: `classical_chinese_translation`
- This task authorizes the `classical_chinese` governance route by explicit task-card scope; it does not activate lesson production.

## Authorized Inputs

- `README.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `CURRENT_COURSE.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/AGENT_ENTRY_PROTOCOL.md`
- `GOVERNANCE/WORKFLOW_CONTRACT.md`
- `GOVERNANCE/FAIL_CLOSED_RULES.md`
- `GOVERNANCE/SOURCE_AUTHORITY_PROTOCOL.md`
- `GOVERNANCE/NOTEBOOKLM_WORKFLOW_PROTOCOL.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `CLOSEOUTS/TASK-CLCH-GOV-000_Closeout.md`
- `docs/OPERATOR_GUIDE.md`

## Required Outputs

- `TASK_CARDS/TASK-CLCH-GOV-001_Classical_Chinese_Course_Boundary_Bootstrap.md`
- `GOVERNANCE/TASK-CLCH-GOV-001_Classical_Chinese_Course_Boundary_Bootstrap.md`
- `CLOSEOUTS/TASK-CLCH-GOV-001_Closeout.md`
- Updates to:
  - `COURSES/classical_chinese/COURSE_BOUNDARY.md`
  - `COURSES/classical_chinese/ROADMAP.md`
  - `COURSES/classical_chinese/TASK_REGISTRY.md`
  - `LESSON_PREP_WORKFLOW_SOT.md`
  - `GOVERNANCE/PLAN.md`
  - `GOVERNANCE/TASK_STATE.json`
  - `GOVERNANCE/TASK_INDEX.md`
  - `GOVERNANCE/CHANGE_LOG.md`
  - `docs/OPERATOR_GUIDE.md`

## Required Governance Outcomes

1. Define the course identity, learner profile, source boundary, NotebookLM boundary, AI/vibecoding boundary, copyright boundary, output-maturity boundary, fail-closed rules, forbidden outputs, and allowed next outputs.
2. Confirm that future material extraction must produce a `16-session core material matrix` before teaching design begins.
3. Keep AI and vibecoding classified as method-layer support only; they must not replace Ancient Chinese knowledge ontology, philology, grammar, lexicon, or textual interpretation.
4. Keep CNKI prompt-writing as a later teaching-activity design concern, not part of this governance bootstrap.

## Forbidden Actions

- Do not generate formal teaching content.
- Do not fabricate NotebookLM extraction completion.
- Do not quote or reconstruct long textbook passages.
- Do not treat uploaded textbook titles as already extracted, audited, or lesson-ready.
- Do not leave the repository placeholder governance task as the active route pointer for this course-governance run.

## Acceptance Checks

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`
- `grep` check confirming the old placeholder governance pointer is not lingering across the governed route
- `grep -R "TASK-CLCH-GOV-001" -n README.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE COURSES docs TASK_CARDS CLOSEOUTS`
- `grep -R "TASK-CLCH-MAT-001" -n README.md LESSON_PREP_WORKFLOW_SOT.md GOVERNANCE COURSES docs TASK_CARDS CLOSEOUTS`
- `git diff --check`

## State And Closeout

- `TASK-CLCH-GOV-000` must remain completed.
- `TASK-CLCH-GOV-001` may be set to completed once all required governance files and acceptance checks pass.
- `next_task` must point to `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.
- The closeout must record branch, changed files, what was completed, what was not done, acceptance results, and the next task.

## Next Task

`TASK-CLCH-MAT-001 | Knowledge Map Extraction`
