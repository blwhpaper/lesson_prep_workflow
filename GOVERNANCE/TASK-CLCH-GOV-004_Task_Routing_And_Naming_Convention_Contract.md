# TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract

## Purpose

This governance record defines how the `COURSES/classical_chinese` line must classify task families, derive branch and file names, prevent route drift, and keep route pointers synchronized before material, prompt, lesson, assessment, or review work expands.

## Namespace

- course task namespace: `TASK-CLCH-*`
- repository governance namespace: `TASK-LPW-GOV-*`
- `TASK-CLCH-*` may not be used for other project lines

## Task Families

- `TASK-CLCH-GOV-*`
  - governance, boundary, routing, protocol, index, and agent constraints only
  - allowed outputs: governance shells, contracts, route tables, naming rules, anti-drift rules, task cards, governance records, closeouts
  - blocked outputs: lesson plans, slides, full material extraction payloads, question banks, assessment instruments, or formal classroom prose
- `TASK-CLCH-MAT-*`
  - source-grounded material mapping, knowledge maps, material matrices, text clusters, grammar clusters,训诂or文字学 structure below lesson level
  - allowed outputs: knowledge map, source-slot map, topic clusters, session material matrix, unresolved-review flags
  - blocked outputs: full lesson scripts, whole-course narrative prose, full PPT sets, student-facing assessment sets
- `TASK-CLCH-PROMPT-*`
  - NotebookLM, Claude, Cursor, Codex, and related prompt packs or extraction prompt contracts
  - allowed outputs: prompt contracts, prompt metadata, extraction templates, review prompts, prompt-routing notes
  - blocked outputs: prompt-only promotion to approved teaching content
- `TASK-CLCH-LESSON-*`
  - lesson plans, classroom activities, handouts, and PPT structure for specific lessons or units
  - prerequisite: material route and lesson-stage authorization must already exist
- `TASK-CLCH-ASSESS-*`
  - homework, quizzes, rubrics, student-output evaluation, and assessment framing
  - prerequisite: content and design boundaries must already exist
- `TASK-CLCH-REVIEW-*`
  - retrospectives, quality review, version audit, and route-level review
  - prerequisite: there must be an artifact family to review

## Naming Conventions

- branch format: `task-clch-<type>-<number>-<kebab-title>`
- task-card filename format: `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`
- governance-record filename format: `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`
- closeout filename format: `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md`

## Routing Rules

- the operator phrase `TASK-CLCH-XXX 开工` activates only the named task
- the agent must classify the requested task family before acting
- if the task family implies a later stage than the current roadmap or registry allows, fail closed
- if branch, task id, roadmap, registry, task state, or task index disagree, fail closed
- the route must stay inside `COURSES/classical_chinese` unless the task card explicitly authorizes a read-only boundary exception
- the route must not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`

## Scope Guardrails

- governance tasks may create governance artifacts only
- material tasks may not skip directly to lesson design
- prompt tasks may not substitute for source-audited material or classroom-ready prose
- lesson tasks may not expand into a full course set unless explicitly authorized
- assessment tasks may not generate a full question bank unless explicitly authorized
- no task may directly generate a full course, full PPT set, or full question bank without explicit task-card authorization

## Pointer Consistency Contract

For each active or next task, these files must point to the same route state:

- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`

## Downstream Effect

- `TASK-CLCH-GOV-004` completion advances the next route to `TASK-CLCH-MAT-001 | Knowledge Map Extraction`
- `TASK-CLCH-MAT-001` becomes the first non-governance task for the `classical_chinese` line
- later `PROMPT`, `LESSON`, `ASSESS`, and `REVIEW` work must follow the task-family gate rather than free-form user phrasing
