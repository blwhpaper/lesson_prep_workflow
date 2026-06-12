# Classical Chinese Downstream Task Sequence Optimization

This file is the latest downstream execution-order interpretation layer created by `TASK-CLCH-GOV-007`.

It does not delete the historical value of `TASK-CLCH-GOV-006`. It supersedes `TASK-CLCH-GOV-006` only for future downstream execution order, dependency interpretation, competency-matrix placement, and acceptance-boundary enforcement.

`TASK-CLCH-GOV-008` later supersedes the GOV-007 chain as the latest downstream mainline. This file remains a historical interpretation layer and must be read together with `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md` so agents do not mistake the GOV-007 chain for the current route.

## GOV-008 Override Note

- The GOV-007 11-task expanded governance chain in this file is superseded by the GOV-008 four-batch lesson build chain.
- Use `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md` for the current downstream mainline, replacement map, and folded-task interpretation.
- Keep this file as historical execution-order context rather than the active route pointer.

## Scope Statement

- The 11 tasks below define the runnable shell for downstream course generation and delivery governance.
- Completing these 11 tasks does not mean the full 16-week preparation workload is finished.
- Completing these 11 tasks means the course-generation and delivery shell reaches a governable closed loop.
- `TASK-CLCH-LESSON-001` defines only the 16-week course architecture. It does not authorize week-by-week lesson prose, full `教案`, PPT bodies, question banks, translation packets, or classroom scripts.
- The competency matrix must first become a boundary and acceptance layer before it enters lesson generation, workflow generation, assessment generation, or delivery planning.

## Final Recommended Sequence

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

## Task Classification

### Shell Governance

- `TASK-CLCH-COMP-001`
- `TASK-CLCH-WORKFLOW-001`
- `TASK-CLCH-QA-001`
- `TASK-CLCH-DELIVERY-001`

### Course Architecture

- `TASK-CLCH-LESSON-001`
- `TASK-CLCH-LESSON-002`

### Material Processing

- `TASK-CLCH-MAT-003`
- `TASK-CLCH-PROMPT-001`

### Classroom Delivery

- `TASK-CLCH-LESSON-003`
- `TASK-CLCH-AI-001`

### Assessment Loop

- `TASK-CLCH-ASSESS-001`

## Dependency And Boundary Matrix

| task | class | required inputs | output boundary | acceptance standard |
|---|---|---|---|---|
| `TASK-CLCH-LESSON-001` | course architecture | `KNOWLEDGE_MAP.md`, `CORE_MATERIAL_MATRIX_16_SESSIONS.md`, `DOWNSTREAM_TASK_ROADMAP.md`, this file, active task card, fail-closed skill | 16-week architecture, unit grouping, session count logic, progression notes, unresolved dependency list only | covers all 16 weeks, stays below lesson-body level, names unresolved evidence, and explicitly forbids full session prose |
| `TASK-CLCH-COMP-001` | shell governance | `TASK-CLCH-LESSON-001` outputs, course boundary, material maturity state, fail-closed skill | competency matrix, assessment boundary, evidence dimensions, acceptance gate definitions only | competency matrix becomes a required acceptance layer for later lesson, workflow, AI, assess, QA, and delivery tasks |
| `TASK-CLCH-LESSON-002` | course architecture | `TASK-CLCH-LESSON-001`, `TASK-CLCH-COMP-001`, material artifacts, fail-closed skill | weekly unit map, session blueprint schema, week/session objective slots, evidence hooks | converts architecture into weekly/session blueprint without writing full teaching scripts or student tasks |
| `TASK-CLCH-MAT-003` | material processing | `TASK-CLCH-LESSON-002`, `TASK-CLCH-COMP-001`, source metadata, material matrix, fail-closed skill | session-level material allocation table, source slots, locator gaps, maturity labels | every session receives source-bounded material allocation with locators or `pending verification`; no lesson prose generated |
| `TASK-CLCH-PROMPT-001` | material processing | `TASK-CLCH-MAT-003`, `TASK-CLCH-COMP-001`, NotebookLM boundary rules, fail-closed skill | extraction prompt pack, prompt metadata, prompt failure cases, review prompts | prompts remain extraction support only and cannot replace source allocation, lesson design, or classroom wording |
| `TASK-CLCH-LESSON-003` | classroom delivery | `TASK-CLCH-LESSON-002`, `TASK-CLCH-MAT-003`, `TASK-CLCH-COMP-001`, `TASK-CLCH-PROMPT-001`, fail-closed skill | one sample lesson-package prototype or sample bounded set, output schema validation, review flags | proves the package shell works without triggering full 16-week batch generation |
| `TASK-CLCH-WORKFLOW-001` | shell governance | `TASK-CLCH-LESSON-003`, `TASK-CLCH-COMP-001`, `TASK-CLCH-PROMPT-001`, fail-closed skill | teacher prep workflow, operator sequence, evidence handoff steps, review checkpoints | teacher workflow reflects actual prototype dependencies and preserves competency/evidence gates |
| `TASK-CLCH-AI-001` | classroom delivery | `TASK-CLCH-LESSON-003`, `TASK-CLCH-WORKFLOW-001`, `TASK-CLCH-COMP-001`, fail-closed skill | student AI protocol, disclosure rule, bounded AI task types, teacher override rule | AI stays method-layer only and is tied to competency boundary and lesson prototype constraints |
| `TASK-CLCH-ASSESS-001` | assessment loop | `TASK-CLCH-COMP-001`, `TASK-CLCH-LESSON-003`, `TASK-CLCH-WORKFLOW-001`, fail-closed skill | rubric system, evidence checklist, student-output review boundary, assessment traceability map | assessment rules map back to competency matrix and prototype lesson evidence rather than free-floating tasks |
| `TASK-CLCH-QA-001` | shell governance | all prior downstream governance artifacts, fail-closed skill | lesson-package QA protocol, release checklist, blocker rules, drift checks | QA protocol can reject artifacts that fail competency, source, evidence, or task-boundary checks |
| `TASK-CLCH-DELIVERY-001` | shell governance | all prior downstream artifacts, especially `TASK-CLCH-QA-001`, fail-closed skill | full 16-week generation plan, batching strategy, review cadence, dependency checklist only | produces a governed production plan, not the full 16-week course package itself |

## Sequence Logic

- First define the course shell, then define the competency and assessment boundary.
- First lock the competency matrix, then allow weekly and session blueprinting.
- First assign source material and extraction support, then validate one sample lesson package.
- First prove the teacher workflow and evidence flow, then define student AI tasks and student-output assessment.
- First define QA protocol, then authorize the full 16-week generation plan.

## Competency Matrix Boundary Rule

The competency matrix is not an optional appendix.

It must appear first as:

- a downstream boundary document
- an acceptance contract
- an evidence-mapping frame
- a rejection rule for off-scope lesson or assessment output

Only after that may competency dimensions be embedded into:

- weekly blueprint design
- session material allocation
- sample lesson package structure
- teacher workflow checkpoints
- AI task disclosure and use limits
- student-output rubric design
- QA audit checks
- 16-week generation planning

## Non-Equivalence Rule

The 11-task sequence does not equal:

- the full 16-week lesson package already written
- the full PPT package already written
- the question bank already written
- the full teacher scripts already written
- the translation material pack already written

It equals only:

- a governed downstream operating shell
- a validated sequencing logic
- a competency-bound acceptance system
- a production-ready planning loop

## Downstream Entry Rule

After `TASK-CLCH-GOV-007`, every future downstream `TASK-CLCH-LESSON-*`, `TASK-CLCH-COMP-*`, `TASK-CLCH-MAT-*`, `TASK-CLCH-PROMPT-*`, `TASK-CLCH-WORKFLOW-*`, `TASK-CLCH-AI-*`, `TASK-CLCH-ASSESS-*`, `TASK-CLCH-QA-*`, and `TASK-CLCH-DELIVERY-*` task must read both:

1. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
2. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`
