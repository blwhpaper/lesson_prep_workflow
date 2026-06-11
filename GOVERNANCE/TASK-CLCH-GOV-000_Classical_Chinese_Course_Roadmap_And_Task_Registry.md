# TASK-CLCH-GOV-000 Governance Record

## Purpose

Create a standalone governance shell for `COURSES/classical_chinese` so future `TASK-CLCH-*` work can be routed safely by scope, maturity, source authority, and execution order.

## Result

This task establishes:

- a distinct Classical Chinese course line separate from `classical_chinese_translation`;
- a roadmap that keeps work in governance before material intake, and in materials before lesson design;
- a task registry that separates governance, material, lesson, prompt, assessment, and export work;
- anti-drift rules so later agents do not treat NotebookLM output, textbook knowledge, or CNKI references as approved course material by default.

## Execution Notes

- The repository active-course pointer remains `classical_chinese_translation` in `CURRENT_COURSE.md`.
- The repository governance state is updated to record `TASK-CLCH-GOV-000` as the completed active task for this run.
- The new `classical_chinese` line remains at governance-shell stage only.

## Guardrails

1. No formal lesson production before governance and material tasks complete in order.
2. NotebookLM output enters only through explicit intake and citation-boundary review.
3. Knowledge maps and material matrices remain candidate or audited material work, not lesson artifacts.
4. Assessment tasks may not consume material below the maturity threshold required by the repository model.
