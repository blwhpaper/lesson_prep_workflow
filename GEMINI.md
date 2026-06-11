# Gemini Entry Notes

For `COURSES/classical_chinese`, when the operator says `TASK-CLCH-XXX 开工`, follow the Classical Chinese cross-agent entry protocol exactly.

Minimum read order:

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
11. the active `TASK-CLCH-*` card
12. the previous closeout
13. `git status --short --branch`

Hard rules:

- Fail closed on any mismatch between task number, branch, `TASK_STATE`, roadmap, and registry.
- Normalize the task family before acting:
  - `TASK-CLCH-GOV-*` = governance, boundary, routing, protocol, index, and agent constraints only
  - `TASK-CLCH-MAT-*` = material mapping, knowledge map extraction, and material matrix work below lesson level
  - `TASK-CLCH-PROMPT-*` = NotebookLM, Claude, Cursor, Codex, and similar prompt packs or extraction prompt contracts
  - `TASK-CLCH-LESSON-*` = lesson plans, classroom activities, handouts, and PPT structure
  - `TASK-CLCH-ASSESS-*` = homework, quizzes, rubrics, and student-output evaluation
  - `TASK-CLCH-REVIEW-*` = retrospectives, quality review, and version audit
- Use branch names in the form `task-clch-<type>-<number>-<kebab-title>`.
- Use task-card and governance filenames in the form `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`.
- Use closeout filenames in the form `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md`.
- Stay inside the Classical Chinese course line unless the task card explicitly allows a read-only cross-repository reference.
- Do not mix in `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
- Governance tasks may create only governance artifacts, not lessons, slides, handouts, question banks, papers, or other formal teaching outputs.
- Do not generate a full course, full PPT set, or full question bank unless the active task family and task card explicitly authorize that output scope.
- Do not quote long copyrighted textbook passages.
- Preserve the Classical Chinese source-authority ladder `L0 -> L5`, keep NotebookLM output at `L3`, and do not treat it as final classroom prose.
- Require source fields when available: `source_title`, `source_type`, `source_author_or_editor`, `source_level`, `chapter_or_section`, `page_or_location_if_available`, `extraction_method`, `copyright_risk`, `classroom_use_scope`.
- If source, locator metadata, or copyright risk is unclear, fail closed and output only summary, locator, index, or labeled draft content.
- Keep `TASK_REGISTRY`, `ROADMAP`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG` aligned.
- `COURSES/classical_chinese` is the only formal course route for this line.
- `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` is isolated legacy material only and must not be treated as an active course line or source of record without explicit task-card authorization plus source audit.
- After `TASK-CLCH-GOV-005`, tasks `TASK-CLCH-GOV-000` through `TASK-CLCH-GOV-005` are completed, and the next route is `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.
- Return branch, modified files, summary, acceptance checks, and remaining risks.
