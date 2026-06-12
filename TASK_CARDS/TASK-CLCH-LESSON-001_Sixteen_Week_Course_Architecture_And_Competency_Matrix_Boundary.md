# TASK-CLCH-LESSON-001 | 16-Week Course Architecture And Competency Matrix Boundary

## Task Identity

- task id: `TASK-CLCH-LESSON-001`
- task family: `TASK-CLCH-LESSON-*`
- course line: `COURSES/classical_chinese`
- status at start: `next`
- required branch: `task-clch-lesson-001-sixteen-week-course-architecture-and-competency-matrix-boundary`
- maturity default: `draft` / `teacher-review-required`

## Purpose

Convert the governed knowledge structure and `16-session core material matrix` into a course-level 16-week architecture layer for the Classical Chinese course line.

This task must also fold the competency-matrix boundary into the architecture layer so later prompt, package-standard, assessment, AI-method, and batch-build tasks inherit an explicit acceptance frame.

## Required Inputs

1. `COURSES/classical_chinese/MATERIALS/KNOWLEDGE_MAP.md`
2. `COURSES/classical_chinese/MATERIALS/CORE_MATERIAL_MATRIX_16_SESSIONS.md`
3. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md`
4. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
5. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`
6. `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md`
7. route pointers in `GOVERNANCE/PLAN.md`, `GOVERNANCE/TASK_STATE.json`, and `GOVERNANCE/TASK_INDEX.md`

## Required Outputs

1. a governed course-architecture artifact for all 16 weeks
2. explicit unit grouping and weekly progression logic
3. a competency-boundary layer that later tasks must map to
4. an unresolved dependency list for later evidence capture and package work
5. aligned task-state and route-pointer updates
6. a governed closeout

## Allowed Output Scope

- 16-week architecture
- unit map
- weekly progression table
- competency domains
- competency-to-week mapping
- assessment-boundary notes
- unresolved dependency list
- fail-closed warnings

## Blocked Output Scope

- no per-session lesson-body prose
- no `完整教案`
- no PPT body
- no slide pages
- no handout prose
- no student assignment bodies
- no question bank
- no answer key
- no long textbook quotation
- no NotebookLM wording promoted as classroom prose

## Acceptance Standards

1. the architecture covers all 16 weeks
2. the artifact remains architecture-only and does not drift into lesson bodies
3. the competency boundary is explicit rather than implied
4. the competency boundary is usable by `TASK-CLCH-PROMPT-001`, `TASK-CLCH-LESSON-002`, `TASK-CLCH-ASSESS-001`, and `TASK-CLCH-AI-001`
5. unresolved evidence gaps remain visible and are not hidden
6. source-authority and copyright boundaries remain intact
7. route pointers advance from `TASK-CLCH-LESSON-001` to `TASK-CLCH-PROMPT-001`

## Fail-Closed Rules

- If the route pointers, branch, or task id do not align, stop and mark `needs human review`.
- If the output begins to look like lesson-body drafting, reduce it back to architecture or matrix level only.
- If any source claim requires an exact locator that is not present, mark `pending verification`.
- If a competency statement implies assessment readiness or publication readiness, keep it labeled `draft` / `teacher-review-required`.

## Completion Result

When complete, the route advances to:

`TASK-CLCH-PROMPT-001 | NotebookLM Extraction Prompt Pack`
