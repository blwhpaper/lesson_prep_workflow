# Operator Guide

Begin with `AGENTS.md`. Confirm task and course pointers, work only from an authorized card, and preserve source evidence through every promotion. Keep sensitive inputs local, run acceptance checks, and record unresolved uncertainty rather than guessing.

If `SOT`, task card, source evidence expectation, or state files conflict, stop and mark `needs human review`. Treat prompts as input contracts only, do not promote NotebookLM output beyond `draft` / `extracted` / `unverified`, and do not publish copyright-restricted, privacy-sensitive, or otherwise unauthorized material to a public repository.

For `COURSES/classical_chinese`, `TASK-CLCH-GOV-000` creates only the governance shell. Do not interpret that registry work as permission to generate lessons, slides, handouts, assessments, or NotebookLM-derived course material.

For later Classical Chinese execution, when the user says `TASK-CLCH-XXX 开工`, the agent must first read:

1. `COURSES/classical_chinese/COURSE_BOUNDARY.md`
2. `COURSES/classical_chinese/ROADMAP.md`
3. `COURSES/classical_chinese/TASK_REGISTRY.md`
4. the current `TASK-CLCH-*` task card
5. `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md` for future Classical Chinese tasks after `TASK-CLCH-GOV-SKILL-001`
6. the previous `TASK-CLCH-*` closeout
7. the current git state via `git status --short --branch`

The agent must then confirm that the requested output matches the task stage. For this course line, the required pre-design route is:

The agent must then confirm that the requested output matches the task stage and that the task id, branch, `TASK_STATE`, roadmap, and registry all align. If they do not align, stop and mark `needs human review`.

The Classical Chinese governance header must remain explicit:

- course code: `CLCH`
- course line: `classical_chinese`
- task family: `TASK-CLCH-*`
- fail-closed default: `true`

The agent must normalize the requested Classical Chinese task into one of these route families before acting:

- `TASK-CLCH-GOV-*` for governance, boundary, routing, protocol, index, and agent constraints only
- `TASK-CLCH-MAT-*` for material extraction and material mapping below lesson level
- `TASK-CLCH-PROMPT-*` for NotebookLM and multi-agent prompt packs or extraction prompt workflows
- `TASK-CLCH-LESSON-*` for lesson plans, classroom activities, handouts, and PPT structure
- `TASK-CLCH-ASSESS-*` for homework, quizzes, rubrics, and student-output evaluation
- `TASK-CLCH-REVIEW-*` for retrospective, quality review, and version audit

The agent must also preserve the naming contract:

- branch format: `task-clch-<type>-<number>-<kebab-title>`
- task-card and governance filename format: `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`
- closeout filename format: `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md`

The agent must also keep reads minimal:

- read only the files required for the current `TASK-CLCH-*`
- do not scan the whole repository
- do not read another course line unless the task card explicitly authorizes it
- for the Classical Chinese line, treat `COURSES/classical_chinese` as the only formal route and treat `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` as audit-only legacy material
- do not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`

The agent must not generate lesson plans, slides, handouts, question banks, papers, or formal classroom materials during governance-only tasks.
The agent must not generate a full course, full PPT set, or full question bank unless the active task family and task card explicitly authorize that scope.

Authorized textbook packages by Wang Li, Guo Xiliang, Qiu Xigui, and related authors are source inputs only. Agents must not reproduce long copyrighted passages or treat NotebookLM output as approved course material.

For this course line, future source-derived artifacts must preserve the source-authority ladder:

`L0 repo governance SoT -> L1 course boundary / roadmap / registry -> L2 uploaded textbook or reference metadata -> L3 NotebookLM extraction notes -> L4 agent-generated summaries / matrices / drafts -> L5 classroom-facing deliverables`

Future source-derived artifacts must also preserve these fields whenever the data exists:

- `source_title`
- `source_type`
- `source_author_or_editor`
- `source_level`
- `chapter_or_section`
- `page_or_location_if_available`
- `extraction_method`
- `copyright_risk`
- `classroom_use_scope`

If source identity, locator metadata, or copyright risk is unclear, the agent must fail closed and keep output at summary, index, locator, or labeled draft level only. Any AI-generated wording must remain marked `draft`, `synthetic`, or `teacher-review-required` until human review promotes it.

For this course line, the required pre-design route is:

`TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course` -> `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary` -> `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract` -> `TASK-CLCH-GOV-005 | Merge Legacy Classical Chinese Translation Route Into Formal Course Route` -> `TASK-CLCH-MAT-001 | Knowledge Map Extraction` -> `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` -> design-stage tasks

Keep `TASK_REGISTRY`, `ROADMAP`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG` aligned. After `TASK-CLCH-GOV-005`, the next route is `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.
Before `TASK-CLCH-MAT-001` begins, ignore `LEGACY_IMPORTS/classical_chinese_translation` unless the active task card explicitly authorizes audited legacy-material use.
After `TASK-CLCH-GOV-SKILL-001`, future Classical Chinese tasks must read `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md` and use it as the minimum fail-closed audit checklist before drafting or promoting source-derived or stage-sensitive outputs.

Do not skip from boundary governance to lesson generation. AI/vibecoding belongs only to later method-layer activity design and must not replace the Ancient Chinese knowledge core.
