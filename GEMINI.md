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
- Stay inside the Classical Chinese course line unless the task card explicitly allows a read-only cross-repository reference.
- Do not mix in `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
- Governance tasks may create only governance artifacts, not lessons, slides, handouts, question banks, papers, or other formal teaching outputs.
- Do not quote long copyrighted textbook passages.
- Preserve the Classical Chinese source-authority ladder `L0 -> L5`, keep NotebookLM output at `L3`, and do not treat it as final classroom prose.
- Require source fields when available: `source_title`, `source_type`, `source_author_or_editor`, `source_level`, `chapter_or_section`, `page_or_location_if_available`, `extraction_method`, `copyright_risk`, `classroom_use_scope`.
- If source, locator metadata, or copyright risk is unclear, fail closed and output only summary, locator, index, or labeled draft content.
- Return branch, modified files, summary, acceptance checks, and remaining risks.
