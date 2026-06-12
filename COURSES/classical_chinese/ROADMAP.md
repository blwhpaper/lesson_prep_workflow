# Classical Chinese Course Roadmap

## Status

`TASK-CLCH-GOV-000` created the governance shell. `TASK-CLCH-GOV-001` hardened the course boundary. `TASK-CLCH-GOV-002` established the cross-agent entry layer. `TASK-CLCH-GOV-003` hardened source authority and copyright boundaries. `TASK-CLCH-GOV-004` locked task routing and naming conventions. `TASK-CLCH-GOV-005` retired the duplicate standalone `classical_chinese_translation` route and quarantined it under `LEGACY_IMPORTS` so future agents see only one formal course entry.

This course has not yet entered approved teaching design. Governance is complete through legacy-route retirement plus the inserted fail-closed skill audit layer, and the material stage now includes both the governed knowledge map and the governed `16-session core material matrix`. The next route is `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`, and downstream work must still ignore `LEGACY_IMPORTS` unless a future task card explicitly authorizes audited legacy use.

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
10. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture | next
11. `TASK-CLCH-LESSON-002` | Unit Template And Lesson Design Contract | planned
12. `TASK-CLCH-PROMPT-001` | NotebookLM And Agent Prompt Pack Contract | planned
13. `TASK-CLCH-ASSESS-001` | Assessment And Assignment Framework | planned
14. `TASK-CLCH-REVIEW-001` | Course Retrospective And Quality Review | planned

## Sequencing Logic

- governance comes first so scope, source package, NotebookLM limits, maturity gates, and anti-drift rules exist before material extraction
- `TASK-CLCH-GOV-002` standardizes how Codex, Cursor, Antigravity, Claude, Gemini, and similar agents enter this course line with minimal reads and fail-closed checks
- `TASK-CLCH-GOV-003` locks the source-authority ladder, mandatory source fields, NotebookLM non-substitution rule, and copyright boundary before material extraction begins
- `TASK-CLCH-GOV-004` aligns task routing and naming rules before material, prompt, lesson, assessment, and review families expand
- `TASK-CLCH-GOV-005` removes the duplicate course entry, isolates old route files under `LEGACY_IMPORTS`, and blocks legacy material from downstream use unless a future task card authorizes audited intake
- `TASK-CLCH-MAT-001` maps the governed knowledge terrain without pretending lesson sequencing is already settled
- `TASK-CLCH-MAT-002` must turn that knowledge terrain into the `16-session core material matrix` before any teaching-design task can begin
- `TASK-CLCH-GOV-SKILL-001` inserts a governed fail-closed skill audit between the matrix stage and lesson architecture so later agents must check promotion risk before design begins
- design tasks follow only after material mapping becomes structured enough for a 16-week course architecture
- assessment comes after architecture and activity boundaries because assignments must depend on already bounded content and method choices
- review follows once the route has enough governed artifacts to audit

## Stage Gate

Minimum allowed route:

`governance shell -> boundary bootstrap -> cross-agent entry protocol -> source authority and copyright boundary -> task routing and naming convention contract -> legacy-route retirement and archive isolation -> knowledge map extraction -> 16-session core material matrix -> fail-closed skill audit -> 16-week course architecture -> lesson-design contract -> prompt-pack contract when needed -> assessment and assignment framework -> review route`

## NotebookLM Rule

NotebookLM output is allowed only as raw intake support from the user-uploaded textbook package. It must not be treated as completed teaching design and must flow through the material route before any lesson architecture work.

## Source Authority Rule

All downstream Classical Chinese tasks must preserve the source-authority ladder:

`L0 repo governance SoT -> L1 official course boundary / roadmap / registry -> L2 uploaded textbook or reference metadata -> L3 NotebookLM extraction notes -> L4 agent-generated summaries / matrices / drafts -> L5 classroom-facing deliverables`

`L3` and `L4` may help organize work, but they may not substitute for `L2` source evidence or bypass human review.

## Legacy Import Rule

`COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` is archival legacy material only. It is not a formal route, not a planning source of record, and not a default input for `TASK-CLCH-MAT-001`. Legacy content may be used only when a future task card explicitly authorizes source-audited import work.
