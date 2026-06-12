# Classical Chinese Downstream Task Roadmap

This file is the downstream scope contract created by `TASK-CLCH-GOV-006` and updated by `TASK-CLCH-GOV-007`.

`TASK-CLCH-GOV-006` retains historical value as the first downstream hardening pass.
`TASK-CLCH-GOV-007` is the latest execution-order interpretation layer for all future downstream work.

Future downstream tasks must read this file together with `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`.

## Status Layer

- `TASK-CLCH-GOV-006` = historical downstream hardening baseline
- `TASK-CLCH-GOV-007` = latest downstream sequence optimization and competency-matrix boundary patch
- next executable downstream route = `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`

## Latest Downstream Sequence

1. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture | `next`
2. `TASK-CLCH-COMP-001` | Classical Chinese Competency Matrix And Assessment Boundary | `pending`
3. `TASK-CLCH-LESSON-002` | Weekly Unit And Session Blueprint | `pending`
4. `TASK-CLCH-MAT-003` | Session-Level Source Material Allocation | `pending`
5. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack | `pending`
6. `TASK-CLCH-LESSON-003` | Sample Lesson Package Prototype | `pending`
7. `TASK-CLCH-WORKFLOW-001` | Teacher Preparation Workflow | `pending`
8. `TASK-CLCH-AI-001` | Student AI/Vibecoding Task Protocol | `pending`
9. `TASK-CLCH-ASSESS-001` | Student Output Rubric And Evidence Checklist | `pending`
10. `TASK-CLCH-QA-001` | Lesson Package Quality Audit Protocol | `pending`
11. `TASK-CLCH-DELIVERY-001` | Full 16-Week Lesson Package Generation Plan | `pending`

## Historical Route Note

The earlier `TASK-CLCH-GOV-006` sequence used:

- `TASK-CLCH-LESSON-002` as session package template hardening
- `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006` as four week-block package-build tasks
- `TASK-CLCH-REVIEW-001` as the final route audit

Those definitions remain historically informative. They are no longer the preferred first execution order after `TASK-CLCH-GOV-007`.

## Boundary Matrix

| task | task class | goal | required inputs | expected outputs | not allowed | acceptance standard |
|---|---|---|---|---|---|---|
| `TASK-CLCH-LESSON-001` | course architecture | define the 16-week architecture and progression logic | `KNOWLEDGE_MAP.md`, `CORE_MATERIAL_MATRIX_16_SESSIONS.md`, route pointers, active task card, fail-closed skill, this roadmap, sequence optimization file | course architecture doc, unit map, weekly progression table, unresolved dependency list | no full lesson prose, no PPT body, no handout prose, no assignments, no translations pack | architecture covers all 16 weeks, stays source-bounded, and remains architecture-only |
| `TASK-CLCH-COMP-001` | shell governance | define competency matrix and assessment boundary before lesson-body generation | `TASK-CLCH-LESSON-001`, course boundary, material artifacts, fail-closed skill | competency matrix, performance dimensions, assessment boundary, evidence gate definitions | no lesson prose, no rubric bank for students yet, no session package bodies | competency matrix becomes a boundary and acceptance layer for all later tasks |
| `TASK-CLCH-LESSON-002` | course architecture | convert architecture into weekly and session blueprints | `TASK-CLCH-LESSON-001`, `TASK-CLCH-COMP-001`, material artifacts, fail-closed skill | weekly unit framework, session blueprint schema, objective slots, evidence hooks | no classroom-ready script, no PPT pages, no homework bodies | blueprint fully maps to architecture and competency boundary without dropping into full lesson prose |
| `TASK-CLCH-MAT-003` | material processing | assign source-bounded material to each session blueprint | `TASK-CLCH-LESSON-002`, `TASK-CLCH-COMP-001`, source metadata, material matrix, fail-closed skill | session-level source allocation table, locator notes, source coverage map, maturity flags | no source-free summaries pretending to be lessons, no handouts, no translation materials | every session has governed material slots and unresolved locator gaps are visible |
| `TASK-CLCH-PROMPT-001` | material processing | define NotebookLM extraction prompts that support source allocation and later package drafting | `TASK-CLCH-MAT-003`, `TASK-CLCH-COMP-001`, NotebookLM boundary rules, fail-closed skill | prompt pack, metadata, extraction templates, failure cases, review prompts | no prompt-only lesson generation, no classroom-ready wording, no hidden source substitution | prompts stay extraction-support only and reinforce evidence capture |
| `TASK-CLCH-LESSON-003` | classroom delivery | validate one sample lesson package before any batch generation | `TASK-CLCH-LESSON-002`, `TASK-CLCH-MAT-003`, `TASK-CLCH-COMP-001`, `TASK-CLCH-PROMPT-001`, fail-closed skill | sample lesson package prototype, package schema validation notes, teacher-review flags | no full 16-week batch generation, no full question bank, no full PPT set | the lesson shell proves runnable on a sample basis without overproducing the course |
| `TASK-CLCH-WORKFLOW-001` | shell governance | define teacher preparation workflow on top of the sample package | `TASK-CLCH-LESSON-003`, `TASK-CLCH-COMP-001`, `TASK-CLCH-PROMPT-001`, fail-closed skill | teacher workflow, prep steps, artifact handoff order, review checkpoints | no student-facing package generation at scale, no assessment bank | workflow reflects real prototype dependencies and keeps competency/evidence gates visible |
| `TASK-CLCH-AI-001` | classroom delivery | define bounded student AI tasks as method-layer support | `TASK-CLCH-LESSON-003`, `TASK-CLCH-WORKFLOW-001`, `TASK-CLCH-COMP-001`, fail-closed skill | AI task protocol, disclosure rule, teacher override rule, allowed task types | no AI-first syllabus, no AI substitution for reading, no tool course drift | AI remains subordinate to course competencies and lesson boundaries |
| `TASK-CLCH-ASSESS-001` | assessment loop | define student-output rubric and evidence checklist | `TASK-CLCH-COMP-001`, `TASK-CLCH-LESSON-003`, `TASK-CLCH-WORKFLOW-001`, fail-closed skill | rubric system, evidence checklist, assessment traceability notes | no uncontrolled question bank, no answer dump, no detached assessment tasks | assessment rules map directly back to competency matrix and lesson evidence |
| `TASK-CLCH-QA-001` | shell governance | define lesson-package quality audit protocol | all prior downstream artifacts, fail-closed skill | QA protocol, blocker checklist, drift checks, release gate rules | no new lesson drafting, no silent route rewrites, no scope expansion | QA protocol can block outputs that violate source, competency, evidence, or maturity gates |
| `TASK-CLCH-DELIVERY-001` | shell governance | define the governed plan for later 16-week package generation | all prior downstream artifacts, especially `TASK-CLCH-QA-001`, fail-closed skill | batch-generation plan, review cadence, dependency checklist, delivery sequencing plan | no full 16-week lesson package, no full PPT build, no full question bank | outputs a production plan only, not the final course package |

## Competency Matrix Boundary

After `TASK-CLCH-GOV-007`, the competency matrix must appear before any lesson package prototype, teacher workflow, AI task protocol, rubric, QA protocol, or 16-week generation plan.

It must function as:

- a boundary
- an acceptance contract
- an evidence-mapping rule
- a drift-rejection layer

It must not be postponed to the end of lesson generation.

## Route Class Rule

- shell governance: `COMP`, `WORKFLOW`, `QA`, `DELIVERY`
- course architecture: `LESSON-001`, `LESSON-002`
- material processing: `MAT-003`, `PROMPT-001`
- classroom delivery: `LESSON-003`, `AI-001`
- assessment loop: `ASSESS-001`

## Non-Equivalence Rule

Finishing these 11 tasks does not mean the 16-week preparation workload is fully complete.

It means only that:

- the downstream production shell is defined
- the competency boundary is enforceable
- the workflow and QA loop are governable
- the later 16-week production phase can begin under protocol

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
