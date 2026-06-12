# Classical Chinese Course Roadmap

## Status

`TASK-CLCH-GOV-000` created the governance shell. `TASK-CLCH-GOV-001` hardened the course boundary. `TASK-CLCH-GOV-002` established the cross-agent entry layer. `TASK-CLCH-GOV-003` hardened source authority and copyright boundaries. `TASK-CLCH-GOV-004` locked task routing and naming conventions. `TASK-CLCH-GOV-005` retired the duplicate standalone `classical_chinese_translation` route and quarantined it under `LEGACY_IMPORTS` so future agents see only one formal course entry.

This course has not yet entered approved teaching design. Governance is complete through legacy-route retirement, fail-closed skill audit insertion, downstream roadmap hardening, and downstream sequence optimization with competency-matrix pre-binding. The material stage now includes both the governed knowledge map and the governed `16-session core material matrix`. The next route is `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`, and downstream work must still ignore `LEGACY_IMPORTS` unless a future task card explicitly authorizes audited legacy use.

## Route

1. `TASK-CLCH-GOV-000` | Classical Chinese Course Roadmap And Task Registry | completed
2. `TASK-CLCH-GOV-001` | Classical Chinese Course Boundary Bootstrap | completed
3. `TASK-CLCH-GOV-002` | Cross-Agent Entry Protocol For Classical Chinese Course | completed
4. `TASK-CLCH-GOV-003` | Classical Chinese Source Authority And Copyright Boundary | completed
5. `TASK-CLCH-GOV-004` | Task Routing And Naming Convention Contract | completed
6. `TASK-CLCH-GOV-005` | Merge Legacy Classical Chinese Translation Route Into Formal Course Route | completed
7. `TASK-CLCH-MAT-001` | Knowledge Map Extraction | completed
8. `TASK-CLCH-MAT-002` | 16-Session Core Material Matrix | completed
9. `TASK-CLCH-GOV-SKILL-001` | Classical Chinese Course Agent Skill And Fail-Closed Audit | completed
10. `TASK-CLCH-GOV-006` | Classical Chinese Course Downstream Task Roadmap Hardening | completed
11. `TASK-CLCH-GOV-007` | Downstream Task Sequence Optimization And Competency Matrix Boundary Patch | completed
12. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture | next
13. `TASK-CLCH-COMP-001` | Classical Chinese Competency Matrix And Assessment Boundary | pending
14. `TASK-CLCH-LESSON-002` | Weekly Unit And Session Blueprint | pending
15. `TASK-CLCH-MAT-003` | Session-Level Source Material Allocation | pending
16. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack | pending
17. `TASK-CLCH-LESSON-003` | Sample Lesson Package Prototype | pending
18. `TASK-CLCH-WORKFLOW-001` | Teacher Preparation Workflow | pending
19. `TASK-CLCH-AI-001` | Student AI/Vibecoding Task Protocol | pending
20. `TASK-CLCH-ASSESS-001` | Student Output Rubric And Evidence Checklist | pending
21. `TASK-CLCH-QA-001` | Lesson Package Quality Audit Protocol | pending
22. `TASK-CLCH-DELIVERY-001` | Full 16-Week Lesson Package Generation Plan | pending

## Sequencing Logic

- governance comes first so scope, source package, NotebookLM limits, maturity gates, and anti-drift rules exist before material extraction
- `TASK-CLCH-GOV-002` standardizes how Codex, Cursor, Antigravity, Claude, Gemini, and similar agents enter this course line with minimal reads and fail-closed checks
- `TASK-CLCH-GOV-003` locks the source-authority ladder, mandatory source fields, NotebookLM non-substitution rule, and copyright boundary before material extraction begins
- `TASK-CLCH-GOV-004` aligns task routing and naming rules before material, prompt, lesson, assessment, and review families expand
- `TASK-CLCH-GOV-005` removes the duplicate course entry, isolates old route files under `LEGACY_IMPORTS`, and blocks legacy material from downstream use unless a future task card authorizes audited intake
- `TASK-CLCH-MAT-001` maps the governed knowledge terrain without pretending lesson sequencing is already settled
- `TASK-CLCH-MAT-002` must turn that knowledge terrain into the `16-session core material matrix` before any teaching-design task can begin
- `TASK-CLCH-GOV-SKILL-001` inserts a governed fail-closed skill audit between the matrix stage and lesson architecture so later agents must check promotion risk before design begins
- `TASK-CLCH-GOV-006` created the first downstream route hardening layer
- `TASK-CLCH-GOV-007` updates that route into the latest execution order and moves the competency matrix forward as a required boundary before lesson package prototyping, workflow design, AI-task design, rubric design, QA, or batch-generation planning
- `TASK-CLCH-LESSON-001` defines the 16-week architecture only and must not drift into full lesson-body drafting
- `TASK-CLCH-COMP-001` must complete before downstream lesson-body, workflow, AI, assessment, QA, or delivery planning tasks because competency and assessment boundaries must exist before content-scale generation
- `TASK-CLCH-LESSON-002` converts the architecture into weekly and session blueprints rather than drafting lesson bodies
- `TASK-CLCH-MAT-003` assigns session-level source material before prompt support or lesson-package prototyping
- `TASK-CLCH-PROMPT-001` follows source allocation so prompts support extraction and evidence capture instead of replacing design logic
- `TASK-CLCH-LESSON-003` is a sample lesson package prototype only; it validates the shell before any batch route is planned
- `TASK-CLCH-WORKFLOW-001` defines the teacher preparation workflow after a prototype exists
- `TASK-CLCH-AI-001` comes after workflow and prototype boundaries are visible so AI remains method-layer support only
- `TASK-CLCH-ASSESS-001` comes after competency, prototype, and workflow boundaries exist so rubrics trace back to evidence
- `TASK-CLCH-QA-001` defines the quality gate before large-scale production planning
- `TASK-CLCH-DELIVERY-001` plans governed 16-week package generation only after QA rules exist

## Stage Gate

Minimum allowed route:

`governance shell -> boundary bootstrap -> cross-agent entry protocol -> source authority and copyright boundary -> task routing and naming convention contract -> legacy-route retirement and archive isolation -> knowledge map extraction -> 16-session core material matrix -> fail-closed skill audit -> downstream roadmap hardening -> downstream sequence optimization and competency-matrix boundary patch -> 16-week course architecture -> competency matrix and assessment boundary -> weekly unit and session blueprint -> session-level source material allocation -> NotebookLM extraction prompt pack -> sample lesson package prototype -> teacher preparation workflow -> student AI/vibecoding task protocol -> student output rubric and evidence checklist -> lesson package quality audit protocol -> full 16-week lesson package generation plan`

## NotebookLM Rule

NotebookLM output is allowed only as raw intake support from the user-uploaded textbook package. It must not be treated as completed teaching design and must flow through the material route before any lesson architecture work.

## Source Authority Rule

All downstream Classical Chinese tasks must preserve the source-authority ladder:

`L0 repo governance SoT -> L1 official course boundary / roadmap / registry -> L2 uploaded textbook or reference metadata -> L3 NotebookLM extraction notes -> L4 agent-generated summaries / matrices / drafts -> L5 classroom-facing deliverables`

`L3` and `L4` may help organize work, but they may not substitute for `L2` source evidence or bypass human review.

## Legacy Import Rule

`COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` is archival legacy material only. It is not a formal route, not a planning source of record, and not a default input for `TASK-CLCH-MAT-001`. Legacy content may be used only when a future task card explicitly authorizes source-audited import work.

## Downstream Hardening Rule

After `TASK-CLCH-GOV-007`, no Classical Chinese downstream task may rely on ad hoc inference for scope, order, output class, or competency placement once `TASK-CLCH-LESSON-001` begins. Agents must use both `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md` and `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md` as the current downstream interpretation layer for `LESSON`, `COMP`, `MAT`, `PROMPT`, `WORKFLOW`, `AI`, `ASSESS`, `QA`, and `DELIVERY` work.

## Anti-Drift Rule

- Do not turn the course into a pure literary-history survey.
- Do not turn the course into a pure linguistics-theory survey.
- Do not turn the course into an AI tools course.
- Do not bypass Wang Li, Guo Xiliang, Qiu Xigui, and related authorized textbook-package boundaries.
- Do not insert lesson-body prose into governance tasks.
- Do not mix in `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
