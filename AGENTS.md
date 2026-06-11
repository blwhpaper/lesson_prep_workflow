# Agent Entry Contract

Every agent must follow this read order before acting:

1. Read `AGENTS.md`.
2. Read `LESSON_PREP_WORKFLOW_SOT.md`.
3. Read `GOVERNANCE/TASK_STATE.json`, `GOVERNANCE/PLAN.md`, and `GOVERNANCE/TASK_INDEX.md`.
4. Read `CURRENT_COURSE.md` and confirm the active course.
5. Read that course's `COURSE_SOT.md`, `COURSE_TASK_STATE.json`, and `COURSE_TASK_INDEX.md`.
6. Read the current task card.

## Boundaries

- Do not read another course directory by default.
- Do not read an external repository by default.
- Cross-repository references require explicit task-card authorization and are read-only.
- `TASK-LPW-GOV-*` is reserved for repository governance.
- Course work uses `TASK-<COURSE_CODE>-*`; this course uses `TASK-CLCH-*`.
- Keep course-specific methods, materials, and task identifiers inside their course.
- NotebookLM output is raw input, never approved course material.
- Do not skip source audit, reliability grading, course adaptation, or assessment suitability review.
- Do not generate lesson plans before the material database reaches the required maturity.
- Unknown source, copyright boundary, task state, active course, or cross-repository permission means fail closed: stop, record `needs human review`, and do not promote the artifact.

The active task is repository governance only. Do not advance a course task unless its task card is active.
