# Classical Chinese Downstream Task Registry Realignment

This governance record is created by `TASK-CLCH-GOV-008`.

`TASK-CLCH-GOV-007` remains historically valid as the prior downstream interpretation layer.
`TASK-CLCH-GOV-008` supersedes `TASK-CLCH-GOV-007` as the latest downstream execution order for future Classical Chinese downstream work.

## GOV-007 Previous Chain Summary

The `TASK-CLCH-GOV-007` chain defined an 11-task expanded governance route:

1. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture
2. `TASK-CLCH-COMP-001` | Classical Chinese Competency Matrix And Assessment Boundary
3. `TASK-CLCH-LESSON-002` | Weekly Unit And Session Blueprint
4. `TASK-CLCH-MAT-003` | Session-Level Source Material Allocation
5. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack
6. `TASK-CLCH-LESSON-003` | Sample Lesson Package Prototype
7. `TASK-CLCH-WORKFLOW-001` | Teacher Preparation Workflow
8. `TASK-CLCH-AI-001` | Student AI/Vibecoding Task Protocol
9. `TASK-CLCH-ASSESS-001` | Student Output Rubric And Evidence Checklist
10. `TASK-CLCH-QA-001` | Lesson Package Quality Audit Protocol
11. `TASK-CLCH-DELIVERY-001` | Full 16-Week Lesson Package Generation Plan

That chain remains a historical governance shell, but it is no longer the current downstream mainline.

## GOV-008 Latest Execution Order

1. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture And Competency Matrix Boundary
2. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack
3. `TASK-CLCH-LESSON-002` | Session Package Template, Source Evidence Contract And Build Standard
4. `TASK-CLCH-ASSESS-001` | Assessment Framework And Translation Practice Rubrics
5. `TASK-CLCH-AI-001` | Student AI/Vibecoding Activity Protocol
6. `TASK-CLCH-LESSON-003` | Week 1-4 Lesson Package Build
7. `TASK-CLCH-LESSON-004` | Week 5-8 Lesson Package Build
8. `TASK-CLCH-LESSON-005` | Week 9-12 Lesson Package Build
9. `TASK-CLCH-LESSON-006` | Week 13-16 Lesson Package Build
10. `TASK-CLCH-REVIEW-001` | Course Delivery Review, Source Evidence Audit And Fail-Closed Check

## Replacement Map

- `TASK-CLCH-COMP-001` -> folded into `TASK-CLCH-LESSON-001` as the competency-matrix boundary layer
- `TASK-CLCH-MAT-003` -> folded into `TASK-CLCH-LESSON-002` as the source evidence contract
- `TASK-CLCH-WORKFLOW-001` -> folded into `TASK-CLCH-LESSON-002` build standard and `TASK-CLCH-REVIEW-001` audit scope
- `TASK-CLCH-QA-001` -> folded into `TASK-CLCH-REVIEW-001`
- `TASK-CLCH-DELIVERY-001` -> replaced by `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006` four-batch lesson-package builds

## Why Four-Batch Lesson Build

- It keeps the route closer to actual delivery work by tying governance directly to four runnable week-block outputs instead of a separate generation-plan shell.
- It moves competency, evidence, and build standards into the tasks that immediately control package structure.
- It reduces handoff drift between architecture, source evidence, workflow, QA, and delivery planning by folding those constraints into fewer execution stages.
- It creates bounded acceptance points after each 4-week build instead of postponing package-level review until the end.

## Downstream Task Boundaries

| task | input dependency | output boundary | forbidden output | acceptance gate |
|---|---|---|---|---|
| `TASK-CLCH-LESSON-001` | `KNOWLEDGE_MAP.md`, `CORE_MATERIAL_MATRIX_16_SESSIONS.md`, fail-closed skill, this file, downstream roadmap, sequence optimization file, active task card | 16-week architecture, unit grouping, competency boundary, progression logic, unresolved dependency list | no per-session lesson prose, no PPT body, no question bank, no translation packet, no classroom text | covers all 16 weeks, defines competency boundary explicitly, remains architecture-only |
| `TASK-CLCH-PROMPT-001` | `TASK-CLCH-LESSON-001`, NotebookLM boundary rules, fail-closed skill | NotebookLM extraction prompt pack, prompt metadata, failure cases, evidence-capture prompts | no direct course-body generation, no prompt-only lesson production, no classroom-ready prose | prompts stay extraction-support only and preserve evidence capture plus review boundaries |
| `TASK-CLCH-LESSON-002` | `TASK-CLCH-LESSON-001`, `TASK-CLCH-PROMPT-001`, material artifacts, fail-closed skill | session package template, source evidence contract, build standard, teacher-use build constraints | no full 16-week package, no completed week packages, no classroom-body prose for all sessions | template and build standard are reusable, evidence-bound, and still below full package generation |
| `TASK-CLCH-ASSESS-001` | `TASK-CLCH-LESSON-001`, `TASK-CLCH-LESSON-002`, fail-closed skill | assessment framework, translation-practice rubric system, evidence dimensions, review flags | no uncontrolled question bank, no answer dump, no detached student-ready test bank | assessment framework maps back to competency boundary and package evidence contract |
| `TASK-CLCH-AI-001` | `TASK-CLCH-LESSON-001`, `TASK-CLCH-LESSON-002`, fail-closed skill | student AI/vibecoding activity protocol, disclosure rule, teacher override rule, bounded use cases | no AI-first syllabus, no AI substitution for reading or translation analysis, no tool-course drift | AI remains method-layer support and respects package build plus evidence rules |
| `TASK-CLCH-LESSON-003` | `TASK-CLCH-LESSON-001`, `TASK-CLCH-PROMPT-001`, `TASK-CLCH-LESSON-002`, `TASK-CLCH-ASSESS-001`, `TASK-CLCH-AI-001`, fail-closed skill | Week 1-4 lesson package build only | no Week 5-16 package generation, no whole-course batch generation | first four weeks build cleanly against evidence, rubric, and AI-use boundaries |
| `TASK-CLCH-LESSON-004` | `TASK-CLCH-LESSON-003` plus all earlier boundaries | Week 5-8 lesson package build only | no Week 1-4 rewrite drift, no Week 9-16 generation | second batch preserves the same build standard and evidence contract |
| `TASK-CLCH-LESSON-005` | `TASK-CLCH-LESSON-004` plus all earlier boundaries | Week 9-12 lesson package build only | no Week 13-16 generation, no course-wide uncontrolled rewrite | third batch stays aligned with the established build standard and assessment boundary |
| `TASK-CLCH-LESSON-006` | `TASK-CLCH-LESSON-005` plus all earlier boundaries | Week 13-16 lesson package build only | no publication claim, no bypass of final review | completes the four-batch build set but does not itself equal course release approval |
| `TASK-CLCH-REVIEW-001` | `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006`, plus earlier boundaries and fail-closed skill | course delivery review, source evidence audit, fail-closed check, release readiness finding set | no new lesson generation disguised as review, no silent source upgrades, no hidden QA bypass | verifies cross-batch consistency, evidence integrity, and fail-closed compliance before downstream promotion |

## Scope Clarifications

- All four batch-build tasks must complete before the route can claim a full 16-week lesson-package set exists.
- `TASK-CLCH-GOV-008` does not generate any lesson package.
- `TASK-CLCH-LESSON-001` defines only the 16-week architecture and competency matrix boundary. It does not generate per-session lesson bodies.
- `TASK-CLCH-PROMPT-001` defines only the NotebookLM extraction prompt pack. It does not directly generate course prose.
- `TASK-CLCH-LESSON-002` defines only the session package template, source evidence contract, and build standard. It does not generate the full lesson-package set.
- `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006` are the only tasks that generate the four lesson-package batches.
- `TASK-CLCH-REVIEW-001` is the final source evidence audit and fail-closed check for the full four-batch lesson build route.
