# Operator Guide

Begin with `AGENTS.md`. Confirm task and course pointers, work only from an authorized card, and preserve source evidence through every promotion. Keep sensitive inputs local, run acceptance checks, and record unresolved uncertainty rather than guessing.

If `SOT`, task card, source evidence expectation, or state files conflict, stop and mark `needs human review`. Treat prompts as input contracts only, do not promote NotebookLM output beyond `draft` / `extracted` / `unverified`, and do not publish copyright-restricted, privacy-sensitive, or otherwise unauthorized material to a public repository.

For `COURSES/classical_chinese`, `TASK-CLCH-GOV-000` creates only the governance shell. Do not interpret that registry work as permission to generate lessons, slides, handouts, assessments, or NotebookLM-derived course material.

For later Classical Chinese execution, when the user says `TASK-CLCH-XXX 开工`, the agent must first read:

1. `COURSES/classical_chinese/COURSE_BOUNDARY.md`
2. `COURSES/classical_chinese/ROADMAP.md`
3. `COURSES/classical_chinese/TASK_REGISTRY.md`
4. the current `TASK-CLCH-*` task card
5. the previous `TASK-CLCH-*` closeout
6. the current git state via `git status --short --branch`

The agent must then confirm that the requested output matches the task stage. For this course line, the required pre-design route is:

`TASK-CLCH-MAT-001 | Knowledge Map Extraction` -> `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` -> design-stage tasks

Do not skip from boundary governance to lesson generation. AI/vibecoding belongs only to later method-layer activity design and must not replace the Ancient Chinese knowledge core.
