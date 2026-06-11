# Repository Architecture

- `GOVERNANCE/`: workflow governance, state, contracts, maturity model, source rules, NotebookLM intake rules, and publication boundaries.
- `TASK_CARDS/`: executable scope definitions.
- `CLOSEOUTS/`: task evidence and handoff records.
- `COURSES/`: isolated course instance scaffolds.
- `COURSES/<course>/COURSE_SOT.md`: course-specific source of truth.
- `COURSES/<course>/MATERIAL_DATABASE/`: maturity-controlled course material store.
- `COURSES/<course>/NOTEBOOKLM/`: NotebookLM prompts, outputs, and intake review staging.
- `COURSES/<course>/SOURCES/`: source evidence and audit support.
- `COURSES/<course>/ASSESSMENTS/`: assessment audit and design artifacts.
- `SHARED/`: `L6` cross-course templates and patterns only.
- `SKILLS/`: governed agent procedures.
- `docs/`: operator-facing architecture documentation.

Authority flows from repository SOT to governance state, current-course pointer, course SOT/state, and finally the active task card.

Material maturity may not bypass `L0 -> L1 -> L2 -> L3 -> L4 -> L5 -> L6`. NotebookLM output enters only as `draft` / `extracted` / `unverified`, and public publication requires a separate boundary check.
