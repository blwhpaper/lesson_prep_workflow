# Classical Chinese Course Roadmap

## Status

`TASK-CLCH-GOV-000` created the governance shell. `TASK-CLCH-GOV-001` hardened the course boundary. `TASK-CLCH-GOV-002` established the cross-agent entry layer. `TASK-CLCH-GOV-003` hardened source authority and copyright boundaries. `TASK-CLCH-GOV-004` locked task routing and naming conventions. `TASK-CLCH-GOV-005` retired the duplicate standalone `classical_chinese_translation` route and quarantined it under `LEGACY_IMPORTS` so future agents see only one formal course entry.

This course has not yet entered approved teaching design. Governance is complete through legacy-route retirement, fail-closed skill audit insertion, and downstream roadmap hardening, and the material stage now includes both the governed knowledge map and the governed `16-session core material matrix`. The next route is `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`, and downstream work must still ignore `LEGACY_IMPORTS` unless a future task card explicitly authorizes audited legacy use.

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
11. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture | next
12. `TASK-CLCH-LESSON-002` | Session Package Template And Evidence Contract | pending
13. `TASK-CLCH-LESSON-003` | Week 1-4 Lesson Package Build | pending
14. `TASK-CLCH-LESSON-004` | Week 5-8 Lesson Package Build | pending
15. `TASK-CLCH-LESSON-005` | Week 9-12 Lesson Package Build | pending
16. `TASK-CLCH-LESSON-006` | Week 13-16 Lesson Package Build | pending
17. `TASK-CLCH-ASSESS-001` | Assignments Rubrics And Translation Practice Assessment | pending
18. `TASK-CLCH-AI-001` | Student AI/Vibecoding Activity Protocol | pending
19. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack | pending
20. `TASK-CLCH-REVIEW-001` | Course Delivery Review And Fail-Closed Audit | pending

## Sequencing Logic

- governance comes first so scope, source package, NotebookLM limits, maturity gates, and anti-drift rules exist before material extraction
- `TASK-CLCH-GOV-002` standardizes how Codex, Cursor, Antigravity, Claude, Gemini, and similar agents enter this course line with minimal reads and fail-closed checks
- `TASK-CLCH-GOV-003` locks the source-authority ladder, mandatory source fields, NotebookLM non-substitution rule, and copyright boundary before material extraction begins
- `TASK-CLCH-GOV-004` aligns task routing and naming rules before material, prompt, lesson, assessment, and review families expand
- `TASK-CLCH-GOV-005` removes the duplicate course entry, isolates old route files under `LEGACY_IMPORTS`, and blocks legacy material from downstream use unless a future task card authorizes audited intake
- `TASK-CLCH-MAT-001` maps the governed knowledge terrain without pretending lesson sequencing is already settled
- `TASK-CLCH-MAT-002` must turn that knowledge terrain into the `16-session core material matrix` before any teaching-design task can begin
- `TASK-CLCH-GOV-SKILL-001` inserts a governed fail-closed skill audit between the matrix stage and lesson architecture so later agents must check promotion risk before design begins
- `TASK-CLCH-GOV-006` hardens the full downstream route so later agents do not have to infer task order, stage gates, or permitted outputs after `TASK-CLCH-LESSON-001`
- `TASK-CLCH-LESSON-001` defines the 16-week architecture only and must not drift into full lesson-body drafting
- `TASK-CLCH-LESSON-002` must freeze the package template, evidence contract, and output schema before any week-range package build starts
- `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006` split production into four-week blocks so lesson drafting, evidence review, and quality control remain governable
- `TASK-CLCH-ASSESS-001` comes after package structure is stable because assignments and rubrics must follow already bounded lesson scope
- `TASK-CLCH-AI-001` comes after lesson and assessment boundaries are visible so AI work stays method-layer only and does not overtake the course core
- `TASK-CLCH-PROMPT-001` comes after the lesson package and AI-activity boundaries are explicit so NotebookLM prompts remain extraction support, not a substitute design engine
- `TASK-CLCH-REVIEW-001` follows once governed architecture, packages, assessment, AI protocol, and prompt pack artifacts exist to audit

## Stage Gate

Minimum allowed route:

`governance shell -> boundary bootstrap -> cross-agent entry protocol -> source authority and copyright boundary -> task routing and naming convention contract -> legacy-route retirement and archive isolation -> knowledge map extraction -> 16-session core material matrix -> fail-closed skill audit -> downstream roadmap hardening -> 16-week course architecture -> session package template and evidence contract -> week 1-4 package build -> week 5-8 package build -> week 9-12 package build -> week 13-16 package build -> assessment and assignment system -> AI/vibecoding student activity protocol -> NotebookLM extraction prompt pack -> course delivery review route`

## NotebookLM Rule

NotebookLM output is allowed only as raw intake support from the user-uploaded textbook package. It must not be treated as completed teaching design and must flow through the material route before any lesson architecture work.

## Source Authority Rule

All downstream Classical Chinese tasks must preserve the source-authority ladder:

`L0 repo governance SoT -> L1 official course boundary / roadmap / registry -> L2 uploaded textbook or reference metadata -> L3 NotebookLM extraction notes -> L4 agent-generated summaries / matrices / drafts -> L5 classroom-facing deliverables`

`L3` and `L4` may help organize work, but they may not substitute for `L2` source evidence or bypass human review.

## Legacy Import Rule

`COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` is archival legacy material only. It is not a formal route, not a planning source of record, and not a default input for `TASK-CLCH-MAT-001`. Legacy content may be used only when a future task card explicitly authorizes source-audited import work.

## Downstream Hardening Rule

After `TASK-CLCH-GOV-006`, no Classical Chinese downstream task may rely on ad hoc inference for scope, order, or output class once `TASK-CLCH-LESSON-001` begins. Agents must use `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md` as the task-family boundary map for `LESSON`, `ASSESS`, `AI`, `PROMPT`, and `REVIEW` work.

## Anti-Drift Rule

- Do not turn the course into a pure literary-history survey.
- Do not turn the course into a pure linguistics-theory survey.
- Do not turn the course into an AI tools course.
- Do not bypass Wang Li, Guo Xiliang, Qiu Xigui, and related authorized textbook-package boundaries.
- Do not insert lesson-body prose into governance tasks.
- Do not mix in `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
