# TASK-CLCH-MAT-001 | Knowledge Map Extraction

## Objective

Produce a governed knowledge-map extraction artifact for `COURSES/classical_chinese` that defines the course-facing knowledge structure before any `16-session core material matrix`, lesson architecture, prompt pack, or classroom-facing design work begins.

## Scope

- create `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md`
- map course-goal boundary and textbook-source boundary at abstraction level only
- define first-level knowledge domains and second-level knowledge points for the Classical Chinese course line
- tag each knowledge point with `learning_value`, `prerequisite`, `teaching_use`, `translation_relevance`, `ai_prompt_potential`, and `source_dependency`
- mark which knowledge points are suitable for the future `16-session core material matrix` and which remain teacher background only
- update governance pointers so `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` becomes the next task

## In Scope Outputs

- material task card
- governed knowledge map
- closeout record
- minimal governance pointer updates

## Out Of Scope

- lesson plans
- weekly teaching schedule
- PPT, handout, worksheet, or question-bank generation
- long textbook excerpt collection
- substitute-textbook prose
- direct NotebookLM output simulation

## Required Rules

1. The output must stay inside `TASK-CLCH-MAT-*` scope and remain below lesson level.
2. The knowledge map must support translation-major undergraduates rather than a general culture survey or a pure philology-history sequence.
3. The artifact must not reproduce long copyrighted textbook text; source references may name books, volumes, topic areas, and abstract knowledge points only.
4. `LEGACY_IMPORTS/classical_chinese_translation` remains excluded from default use.
5. AI-related content must remain method-layer support for reading, prompting, checking, and reflection, not automatic ghostwriting or reading substitution.
6. Completion of this task must advance the route to `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix`.

## Acceptance

Run at least:

- `git status --short --branch`
- `find COURSES/classical_chinese -maxdepth 4 -type f | sort`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`
- `grep -R "TASK-CLCH-MAT-001" -n TASK_CARDS GOVERNANCE COURSES/classical_chinese CLOSEOUTS`
- `grep -R "BTC_WATCHFLOW\\|Lin Yutang\\|NESP\\|Thesis_Format_Fixer" -n COURSES/classical_chinese TASK_CARDS/TASK-CLCH-MAT-001_Knowledge_Map_Extraction.md CLOSEOUTS/TASK-CLCH-MAT-001_Closeout.md || true`
- `git diff --check`

## Completion Condition

This task is complete only when `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md` exists, the knowledge map includes all required domains and metadata fields, anti-drift and copyright prohibitions are explicit, and governance pointers advance from `TASK-CLCH-MAT-001` to `TASK-CLCH-MAT-002`.
