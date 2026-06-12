# Classical Chinese Downstream Task Roadmap

This file is the downstream scope contract created by `TASK-CLCH-GOV-006`, updated by `TASK-CLCH-GOV-007`, and realigned by `TASK-CLCH-GOV-008`.

`TASK-CLCH-GOV-006` retains historical value as the first downstream hardening pass.
`TASK-CLCH-GOV-007` retains historical value as the prior expanded-governance execution-order layer.
`TASK-CLCH-GOV-008` supersedes `TASK-CLCH-GOV-007` as the latest downstream execution order for all future downstream work.

Future downstream tasks must first read `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md`, then read this file together with `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`.

## Status Layer

- `TASK-CLCH-GOV-006` = historical downstream hardening baseline
- `TASK-CLCH-GOV-007` = historical downstream sequence optimization and competency-matrix boundary patch
- `TASK-CLCH-GOV-008` = latest downstream registry realignment to the four-batch lesson build route
- next executable downstream route = `TASK-CLCH-PROMPT-001 | NotebookLM Extraction Prompt Pack`

## Latest Downstream Sequence

1. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture And Competency Matrix Boundary | `completed`
2. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack | `next`
3. `TASK-CLCH-LESSON-002` | Session Package Template, Source Evidence Contract And Build Standard | `pending`
4. `TASK-CLCH-ASSESS-001` | Assessment Framework And Translation Practice Rubrics | `pending`
5. `TASK-CLCH-AI-001` | Student AI/Vibecoding Activity Protocol | `pending`
6. `TASK-CLCH-LESSON-003` | Week 1-4 Lesson Package Build | `pending`
7. `TASK-CLCH-LESSON-004` | Week 5-8 Lesson Package Build | `pending`
8. `TASK-CLCH-LESSON-005` | Week 9-12 Lesson Package Build | `pending`
9. `TASK-CLCH-LESSON-006` | Week 13-16 Lesson Package Build | `pending`
10. `TASK-CLCH-REVIEW-001` | Course Delivery Review, Source Evidence Audit And Fail-Closed Check | `pending`

## Historical Route Note

The earlier `TASK-CLCH-GOV-006` sequence used:

- `TASK-CLCH-LESSON-002` as session package template hardening
- `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006` as four week-block package-build tasks
- `TASK-CLCH-REVIEW-001` as the final route audit

The `TASK-CLCH-GOV-007` sequence then replaced that with the expanded governance chain centered on `COMP-001`, `MAT-003`, `WORKFLOW-001`, `QA-001`, and `DELIVERY-001`.

Those definitions remain historically informative. They are superseded and must not be treated as the current downstream mainline after `TASK-CLCH-GOV-008`.

## GOV-008 Override Note

Use `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md` as the primary registry override when interpreting downstream order, folded tasks, and superseded placeholders.

## Boundary Matrix

| task | task class | goal | required inputs | expected outputs | not allowed | acceptance standard |
|---|---|---|---|---|---|---|
| `TASK-CLCH-LESSON-001` | course architecture | define the 16-week architecture and competency boundary | `KNOWLEDGE_MAP.md`, `CORE_MATERIAL_MATRIX_16_SESSIONS.md`, route pointers, active task card, fail-closed skill, this roadmap, sequence optimization file, realignment file | course architecture doc, unit map, weekly progression table, competency boundary, unresolved dependency list | no full lesson prose, no PPT body, no handout prose, no assignments, no translations pack | architecture covers all 16 weeks, states competency boundary explicitly, and remains architecture-only |
| `TASK-CLCH-PROMPT-001` | prompt support | define NotebookLM extraction prompts that support evidence capture and later package work | `TASK-CLCH-LESSON-001`, NotebookLM boundary rules, fail-closed skill | prompt pack, metadata, extraction templates, failure cases, review prompts | no prompt-only lesson generation, no classroom-ready wording, no hidden source substitution | prompts stay extraction-support only and reinforce evidence capture |
| `TASK-CLCH-LESSON-002` | package standard | define the session package template, source evidence contract, and build standard | `TASK-CLCH-LESSON-001`, `TASK-CLCH-PROMPT-001`, material artifacts, fail-closed skill | package template, source evidence contract, build standard, teacher-use constraints | no classroom-ready full-course script, no full 16-week package, no homework bodies | template and build standard are reusable, evidence-bound, and still below full package generation |
| `TASK-CLCH-ASSESS-001` | assessment loop | define the assessment framework and translation-practice rubrics | `TASK-CLCH-LESSON-001`, `TASK-CLCH-LESSON-002`, fail-closed skill | assessment framework, rubric system, evidence checklist, assessment traceability notes | no uncontrolled question bank, no answer dump, no detached assessment tasks | assessment rules map directly back to the architecture and evidence contract |
| `TASK-CLCH-AI-001` | classroom delivery | define bounded student AI tasks as method-layer support | `TASK-CLCH-LESSON-001`, `TASK-CLCH-LESSON-002`, fail-closed skill | AI task protocol, disclosure rule, teacher override rule, allowed task types | no AI-first syllabus, no AI substitution for reading, no tool course drift | AI remains subordinate to course competencies and package boundaries |
| `TASK-CLCH-LESSON-003` | classroom delivery | build the Week 1-4 lesson package batch | `TASK-CLCH-LESSON-001`, `TASK-CLCH-PROMPT-001`, `TASK-CLCH-LESSON-002`, `TASK-CLCH-ASSESS-001`, `TASK-CLCH-AI-001`, fail-closed skill | Week 1-4 lesson package build, review flags, unresolved evidence list | no Week 5-16 generation, no full question bank, no full PPT set | the first four-week batch is buildable under the governed template without route drift |
| `TASK-CLCH-LESSON-004` | classroom delivery | build the Week 5-8 lesson package batch | `TASK-CLCH-LESSON-003` and earlier boundaries | Week 5-8 lesson package build, review flags, unresolved evidence list | no Week 9-16 generation, no cross-batch drift | the second batch preserves the same build standard and evidence contract |
| `TASK-CLCH-LESSON-005` | classroom delivery | build the Week 9-12 lesson package batch | `TASK-CLCH-LESSON-004` and earlier boundaries | Week 9-12 lesson package build, review flags, unresolved evidence list | no Week 13-16 generation, no cross-batch drift | the third batch preserves the same build standard and evidence contract |
| `TASK-CLCH-LESSON-006` | classroom delivery | build the Week 13-16 lesson package batch | `TASK-CLCH-LESSON-005` and earlier boundaries | Week 13-16 lesson package build, review flags, unresolved evidence list | no publication claim, no review bypass | the fourth batch completes the 16-week build set without bypassing final review |
| `TASK-CLCH-REVIEW-001` | review audit | run the final source evidence audit and fail-closed check | `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006`, plus all earlier boundaries and fail-closed skill | course delivery review, source evidence audit, fail-closed findings, release readiness notes | no new lesson drafting, no silent route rewrites, no scope expansion | review can block outputs that violate source, evidence, or maturity gates |

## Folded Historical Placeholders

These tasks are no longer part of the latest downstream mainline after `TASK-CLCH-GOV-008`:

- `TASK-CLCH-COMP-001` -> folded into `TASK-CLCH-LESSON-001`
- `TASK-CLCH-MAT-003` -> folded into `TASK-CLCH-LESSON-002`
- `TASK-CLCH-WORKFLOW-001` -> folded into `TASK-CLCH-LESSON-002` and `TASK-CLCH-REVIEW-001`
- `TASK-CLCH-QA-001` -> folded into `TASK-CLCH-REVIEW-001`
- `TASK-CLCH-DELIVERY-001` -> replaced by `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006`

## Non-Equivalence Rule

Finishing these 10 tasks does not mean the 16-week preparation workload is fully complete.

It means only that:

- the four-batch lesson-package route is completed
- the source evidence and fail-closed review loop is governable
- the full 16-week package set exists only after all four batch-build tasks finish and pass review

## Global Fail-Closed Rules

- Do not turn the course into a pure literary-history course.
- Do not turn the course into a pure linguistics-theory course.
- Do not turn the course into an AI tools course.
- Do not bypass Wang Li, Guo Xiliang, Qiu Xigui, and related authorized material boundaries.
- Do not move lesson-body prose into governance tasks.
- Do not skip the competency matrix boundary and then backfill it later.
- Do not mix in `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
- Do not promote NotebookLM extraction above `draft`, `synthetic`, or `teacher-review-required` without source-backed review.
- If source identity, locator metadata, copyright risk, or route pointers are unclear, stop and mark `needs human review`.
