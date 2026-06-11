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

## Classical Chinese Cross-Agent Entry Override

When a user explicitly says `TASK-CLCH-XXX 开工`, that request activates only the named `TASK-CLCH-*` task for the `COURSES/classical_chinese` line.

Required read order for that route:

1. `AGENTS.md`
2. `LESSON_PREP_WORKFLOW_SOT.md`
3. `GOVERNANCE/PLAN.md`
4. `GOVERNANCE/TASK_STATE.json`
5. `GOVERNANCE/TASK_INDEX.md`
6. `GOVERNANCE/CHANGE_LOG.md`
7. `docs/OPERATOR_GUIDE.md`
8. `COURSES/classical_chinese/COURSE_BOUNDARY.md`
9. `COURSES/classical_chinese/ROADMAP.md`
10. `COURSES/classical_chinese/TASK_REGISTRY.md`
11. the current `TASK-CLCH-*` task card
12. the previous closeout for the same route family when it exists
13. `git status --short --branch`

Required operating rules:

- Fail closed if the task number, current branch, `GOVERNANCE/TASK_STATE.json`, `COURSES/classical_chinese/ROADMAP.md`, and `COURSES/classical_chinese/TASK_REGISTRY.md` do not align.
- Normalize the task family before acting:
  - `TASK-CLCH-GOV-*` = governance, boundary, routing, protocol, index, and agent constraints only
  - `TASK-CLCH-MAT-*` = source-grounded material mapping, knowledge map extraction, and material matrix work below lesson level
  - `TASK-CLCH-PROMPT-*` = NotebookLM, Claude, Cursor, Codex, and related prompt packs or extraction prompt contracts
  - `TASK-CLCH-LESSON-*` = lesson plans, lesson flow, classroom activities, handouts, and PPT structure for specific lessons or units
  - `TASK-CLCH-ASSESS-*` = homework, quizzes, rubrics, and student-output evaluation
  - `TASK-CLCH-REVIEW-*` = retrospectives, quality review, version audit, and route-level review
- Branch names for this course line must use `task-clch-<type>-<number>-<kebab-title>`.
- Task-card and governance filenames for this course line must use `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`.
- Closeout filenames for this course line must use `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md`.
- Read only the files needed for the current `TASK-CLCH-*` task. Do not scan the full repository and do not read other course lines by default.
- Do not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
- Do not generate lesson plans, slides, question banks, papers, or formal classroom materials during governance-only tasks.
- Do not generate a full course, full PPT set, or full question bank unless the active task family and task card explicitly authorize that stage.
- Treat Wang Li, Guo Xiliang, Qiu Xigui, and related textbook packages as user-authorized or NotebookLM-extracted source inputs only. Do not reproduce long copyrighted passages.
- Preserve the Classical Chinese source-authority ladder `L0 repo governance -> L1 course boundary/roadmap/registry -> L2 textbook/reference metadata -> L3 NotebookLM extraction notes -> L4 agent-generated drafts -> L5 classroom-facing deliverables`.
- Require these source fields on future source-derived artifacts when available: `source_title`, `source_type`, `source_author_or_editor`, `source_level`, `chapter_or_section`, `page_or_location_if_available`, `extraction_method`, `copyright_risk`, `classroom_use_scope`.
- If source identity, locator metadata, or copyright risk is unclear, fail closed and keep output at summary, index, or draft level only. AI-generated wording must stay labeled `draft`, `synthetic`, or `teacher-review-required`.
- Keep route pointers aligned across `TASK_REGISTRY`, `ROADMAP`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG`.
- `COURSES/classical_chinese` is the only formal Classical Chinese course route.
- `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` is an isolated legacy archive only, not a course entry, and must be ignored by `TASK-CLCH-MAT-*`, `TASK-CLCH-LESSON-*`, and `TASK-CLCH-ASSESS-*` unless the active task card explicitly authorizes audited legacy use.
- After `TASK-CLCH-GOV-005`, tasks `TASK-CLCH-GOV-000` through `TASK-CLCH-GOV-005` are completed and the next route must be `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.
- End each governed task response with the current branch, changed files, protocol or rule summary, acceptance-command results, and risks or unfinished items.
