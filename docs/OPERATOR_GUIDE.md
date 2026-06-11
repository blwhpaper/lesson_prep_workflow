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

The agent must then confirm that the requested output matches the task stage and that the task id, branch, `TASK_STATE`, roadmap, and registry all align. If they do not align, stop and mark `needs human review`.

The Classical Chinese governance header must remain explicit:

- course code: `CLCH`
- course line: `classical_chinese`
- task family: `TASK-CLCH-*`
- fail-closed default: `true`

The agent must also keep reads minimal:

- read only the files required for the current `TASK-CLCH-*`
- do not scan the whole repository
- do not read another course line unless the task card explicitly authorizes it
- do not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`

The agent must not generate lesson plans, slides, handouts, question banks, papers, or formal classroom materials during governance-only tasks.

Authorized textbook packages by Wang Li, Guo Xiliang, Qiu Xigui, and related authors are source inputs only. Agents must not reproduce long copyrighted passages or treat NotebookLM output as approved course material.

For this course line, the required pre-design route is:

`TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course` -> `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary` -> `TASK-CLCH-MAT-001 | Knowledge Map Extraction` -> `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` -> design-stage tasks

Do not skip from boundary governance to lesson generation. AI/vibecoding belongs only to later method-layer activity design and must not replace the Ancient Chinese knowledge core.
