# Classical Chinese Task Registry

| task | category | status | purpose | allowed_outputs | blocked_outputs |
|---|---|---|---|---|---|
| `TASK-CLCH-GOV-000` | governance | completed | register the standalone course line, roadmap shell, and anti-drift numbering | roadmap shell, task family definitions, governance boundary seed | lessons, slides, source promotion |
| `TASK-CLCH-GOV-001` | governance | completed | bootstrap course boundary, learner target, source boundary, maturity boundary, and non-goals | boundary contract, entry rules, forbidden-output list, next-task route | textbook excerpts, lesson prose, assignment details |
| `TASK-CLCH-GOV-002` | governance | completed | establish the cross-agent entry protocol for `TASK-CLCH-XXX 开工` execution | entry protocol, minimum read order, anti-drift rules, fail-closed checks, response footer contract | lessons, slides, question banks, papers, textbook copying |
| `TASK-CLCH-GOV-003` | governance | completed | define source-authority and copyright boundary rules before material extraction | source-authority contract, copyright boundary, locator and excerpt rules, review preconditions, mandatory source fields | lesson plans, full-text copying, material promotion without review |
| `TASK-CLCH-GOV-004` | governance | completed | align task routing and naming conventions before material and downstream families expand | task-routing contract, naming rules, route-validation rules, task-family normalization | lesson plans, material extraction, design outputs without routing alignment |
| `TASK-CLCH-GOV-005` | governance | completed | merge the retired standalone `classical_chinese_translation` route into the formal course line as an isolated legacy archive | legacy-import archive, route-retirement contract, single-entry rule, legacy-use restrictions | legacy promotion into SoT, duplicate course entry, material extraction from legacy without authorization |
| `TASK-CLCH-GOV-SKILL-001` | governance | completed | insert a governed agent skill and fail-closed audit between `TASK-CLCH-MAT-002` and `TASK-CLCH-LESSON-001` | task-registration patch, fail-closed audit skill, minimum skill-read rule, closeout | lesson plans, slides, question banks, answer keys, lesson-architecture prose |
| `TASK-CLCH-GOV-006` | governance | completed | harden the post-architecture downstream task roadmap so lesson, assessment, AI, prompt, and review work no longer depend on ad hoc inference | downstream task roadmap, task-boundary matrix, route-order patch, operator-entry pointers, closeout | 16-week lesson body, session packages, assignments, AI activity sheets |
| `TASK-CLCH-GOV-007` | governance | completed | optimize the downstream execution order and insert the competency matrix as a mandatory boundary before lesson-package scale-up | sequence-optimization patch, competency boundary contract, updated downstream roadmap, entry-pointer updates, closeout | lesson bodies, full 16-week packages, PPT sets, question banks, translation materials |
| `TASK-CLCH-MAT-001` | material | completed | extract a governed knowledge map from the authorized source package | knowledge map, topic clusters, source-slot map, unresolved-review flags | lesson plans, weekly scripts, assessment items |
| `TASK-CLCH-MAT-002` | material | completed | produce the `16-session core material matrix` before teaching design begins | 16-session core material matrix, session-level material coverage, maturity notes | lesson-plan prose, slides, worksheets |
| `TASK-CLCH-LESSON-001` | lesson | next | convert mature material structure into a 16-week course architecture and unit progression map | 16-week architecture, unit grouping, weekly progression logic, evidence slots, course-level activity ratio, unresolved dependency list | textbook copying, session scripts, handout prose, assignment bank |
| `TASK-CLCH-COMP-001` | competency-governance | pending | define the competency matrix and assessment boundary before lesson-package scale-up | competency matrix, evidence dimensions, assessment boundary, acceptance gates | lesson prose, student-ready assessment bank, classroom materials |
| `TASK-CLCH-LESSON-002` | lesson | pending | convert the architecture into weekly unit and session blueprints | weekly unit map, session blueprint schema, objective slots, evidence hooks | full lesson prose, PPT pages, homework bodies |
| `TASK-CLCH-MAT-003` | material | pending | assign source-bounded material to each session blueprint | session-level source allocation, locator notes, source coverage map, maturity flags | handouts, translation material packets, lesson scripts |
| `TASK-CLCH-PROMPT-001` | prompt | pending | define the NotebookLM extraction prompt pack that supports, but does not replace, lesson and assessment work | prompt pack, prompt metadata, extraction template, evidence checks, failure cases, review prompt schema | prompt-only promotion into approved classroom prose, hidden source substitution |
| `TASK-CLCH-LESSON-003` | lesson | pending | validate a sample lesson package prototype before full-course batch planning | sample lesson package prototype, package schema validation, teacher-review flags | full 16-week package build, full PPT set, full question bank |
| `TASK-CLCH-WORKFLOW-001` | workflow | pending | define the teacher preparation workflow on top of the sample package shell | teacher workflow, artifact handoff order, review checkpoints, preparation sequence | mass lesson generation, student-facing package scaling, assessment bank |
| `TASK-CLCH-AI-001` | ai-method | pending | define the student AI/vibecoding task protocol as method-layer support only | AI task protocol, disclosure rule, prompt boundary, evidence rule, teacher override rule | AI-first syllabus, tool training as course core, bypassing text reading or translation practice |
| `TASK-CLCH-ASSESS-001` | assessment | pending | define the student output rubric and evidence checklist after competency and prototype boundaries exist | rubric system, evidence checklist, assessment traceability map, review flags | uncontrolled question bank, answer dump, detached assessment design |
| `TASK-CLCH-QA-001` | qa | pending | define the lesson package quality audit protocol before batch generation planning | QA protocol, release checklist, blocker rules, drift checks | new lesson drafting, silent route rewrites, scope expansion without governance patch |
| `TASK-CLCH-DELIVERY-001` | delivery-governance | pending | define the full 16-week lesson package generation plan after QA gates exist | batch-generation plan, review cadence, dependency checklist, delivery sequencing plan | direct full-course generation, PPT batch build, question bank batch build |

## Registry Rules

1. `TASK-CLCH-GOV-*` controls boundary, routing, and anti-drift governance only.
2. `TASK-CLCH-GOV-002` is the mandatory cross-agent start layer for this course line.
3. `TASK-CLCH-GOV-003` establishes the source-authority ladder `L0 -> L5`, mandatory source fields, NotebookLM non-substitution rule, and copyright boundary for this course line.
4. `TASK-CLCH-GOV-004` must complete before `TASK-CLCH-MAT-001` may begin.
5. `TASK-CLCH-GOV-005` retires the duplicate standalone route and preserves it only under `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`.
6. `TASK-CLCH-GOV-SKILL-001` inserts the mandatory fail-closed audit skill between `TASK-CLCH-MAT-002` and `TASK-CLCH-LESSON-001`.
7. `TASK-CLCH-GOV-006` hardens the first downstream sequence layer and requires future downstream tasks to use `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md` instead of ad hoc stage inference.
8. `TASK-CLCH-GOV-007` is the latest downstream execution-order interpretation layer and requires future downstream tasks to read both `DOWNSTREAM_TASK_ROADMAP.md` and `DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`.
9. Future `TASK-CLCH-*` execution after `TASK-CLCH-GOV-SKILL-001` must read `.agents/skills/classical_chinese_course_fail_closed_audit/SKILL.md` after the active task card and before acting on source-derived or stage-sensitive outputs.
10. `TASK-CLCH-MAT-*` may structure source-derived course material below lesson level, but may not generate formal lesson artifacts.
11. `TASK-CLCH-MAT-*`, `TASK-CLCH-LESSON-*`, and `TASK-CLCH-ASSESS-*` must ignore `LEGACY_IMPORTS/classical_chinese_translation` unless a future task card explicitly authorizes audited legacy use.
12. `TASK-CLCH-LESSON-001` may define course-level architecture only. It may not generate classroom-body prose, student assignments, or full session packages.
13. `TASK-CLCH-COMP-001` must complete before downstream lesson-package prototyping, workflow design, AI-task design, rubric design, QA protocol design, or delivery planning.
14. `TASK-CLCH-LESSON-002` may define weekly and session blueprints only. It may not become full teaching-script drafting.
15. `TASK-CLCH-LESSON-003` is a sample prototype validation task. It must not become full 16-week batch generation.
16. `TASK-CLCH-ASSESS-*` begins only after competency and prototype boundaries are stable enough for assessment suitability review.
17. `TASK-CLCH-AI-*` may define method-layer AI activity rules only and may not replace the course's Ancient Chinese knowledge core.
18. `TASK-CLCH-PROMPT-*` may define prompt packs and extraction workflows, but prompts alone may not become approved teaching prose.
19. `TASK-CLCH-QA-*` defines quality gates and must not silently rewrite governed outputs into released course packages.
20. `TASK-CLCH-DELIVERY-*` may plan large-scale generation only after QA gates exist and may not itself equal full lesson production.
