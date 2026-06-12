# Classical Chinese Downstream Task Roadmap

This file is the downstream scope contract inserted by `TASK-CLCH-GOV-006`.

It hardens the route after `TASK-CLCH-LESSON-001` so later agents do not infer task order, input maturity, or output permissions from chat context alone.

## Downstream Sequence

1. `TASK-CLCH-LESSON-001` | 16-Week Course Architecture | `next`
2. `TASK-CLCH-LESSON-002` | Session Package Template And Evidence Contract | `pending`
3. `TASK-CLCH-LESSON-003` | Week 1-4 Lesson Package Build | `pending`
4. `TASK-CLCH-LESSON-004` | Week 5-8 Lesson Package Build | `pending`
5. `TASK-CLCH-LESSON-005` | Week 9-12 Lesson Package Build | `pending`
6. `TASK-CLCH-LESSON-006` | Week 13-16 Lesson Package Build | `pending`
7. `TASK-CLCH-ASSESS-001` | Assignments Rubrics And Translation Practice Assessment | `pending`
8. `TASK-CLCH-AI-001` | Student AI/Vibecoding Activity Protocol | `pending`
9. `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack | `pending`
10. `TASK-CLCH-REVIEW-001` | Course Delivery Review And Fail-Closed Audit | `pending`

## Task Boundary Matrix

| task | goal | required inputs | expected outputs | prohibited work | acceptance standard | classroom body allowed | student assignment allowed | NotebookLM evidence required |
|---|---|---|---|---|---|---|---|---|
| `TASK-CLCH-LESSON-001` | define the 16-week architecture and progression logic | `KNOWLEDGE_MAP.md`, `CORE_MATERIAL_MATRIX_16_SESSIONS.md`, route pointers, active task card, fail-closed skill | course architecture doc, unit map, weekly progression table, unresolved dependency list | no full lesson prose, no slides, no handouts, no assignment drafting, no answer keys | architecture covers all 16 weeks, stays source-bounded, keeps anti-drift balance, and labels unresolved evidence | `no` | `no` | `yes` |
| `TASK-CLCH-LESSON-002` | freeze the session package template and evidence contract | `TASK-CLCH-LESSON-001` outputs, material artifacts, active task card, fail-closed skill | session package template, evidence fields, file naming rules, review checklist | no week-specific package build, no full assignments, no AI protocol body | template is reusable across all 16 weeks, defines required evidence slots, and blocks promotion without review | `no` | `no` | `yes` |
| `TASK-CLCH-LESSON-003` | build packages for weeks 1-4 | `TASK-CLCH-LESSON-001`, `TASK-CLCH-LESSON-002`, material artifacts, active task card, fail-closed skill | week 1-4 package files, teacher-review-required lesson drafts, evidence links | no weeks 5-16 package work, no final assessment system, no unrelated AI courseware | four weeks are drafted under the template, evidence-linked, source-bounded, and labeled for review | `yes` | `only if the task card authorizes bounded draft homework` | `yes` |
| `TASK-CLCH-LESSON-004` | build packages for weeks 5-8 | same as `TASK-CLCH-LESSON-003` plus approved week 1-4 template learnings | week 5-8 package files, teacher-review-required lesson drafts, evidence links | no weeks 9-16 package work, no final assessment system | four weeks are drafted under the template, evidence-linked, source-bounded, and labeled for review | `yes` | `only if the task card authorizes bounded draft homework` | `yes` |
| `TASK-CLCH-LESSON-005` | build packages for weeks 9-12 | same as `TASK-CLCH-LESSON-004` | week 9-12 package files, teacher-review-required lesson drafts, evidence links | no weeks 13-16 package work, no final assessment system | four weeks are drafted under the template, evidence-linked, source-bounded, and labeled for review | `yes` | `only if the task card authorizes bounded draft homework` | `yes` |
| `TASK-CLCH-LESSON-006` | build packages for weeks 13-16 | same as `TASK-CLCH-LESSON-005` | week 13-16 package files, teacher-review-required lesson drafts, evidence links | no publication-ready course release, no final assessment answer bank | final four weeks are drafted under the template, evidence-linked, source-bounded, and labeled for review | `yes` | `only if the task card authorizes bounded draft homework` | `yes` |
| `TASK-CLCH-ASSESS-001` | define the assignment and rubric system | lesson architecture, session template, week packages, active task card, fail-closed skill | assignment framework, rubric set, translation-practice assessment map, review rules | no uncontrolled question bank, no hidden answer dump, no assessment detached from course scope | assignment system maps to lesson sequence, preserves source boundaries, and stays review-labeled | `no` | `yes` | `yes` |
| `TASK-CLCH-AI-001` | define student AI/vibecoding activity boundaries | lesson architecture, session template, assessment framework when available, active task card, fail-closed skill | AI protocol, allowed scenarios, disclosure contract, evidence rule, teacher override rule | no AI-first syllabus, no tool training as course core, no substitution for reading or translation practice | AI stays method-layer only, with explicit permitted and forbidden uses plus disclosure rules | `no` | `possible protocol-attached tasks only` | `yes` |
| `TASK-CLCH-PROMPT-001` | define NotebookLM extraction prompts that support the route | material artifacts, lesson architecture, template contract, AI protocol constraints, active task card, fail-closed skill | prompt pack, metadata, extraction prompts, review prompts, failure cases | no prompt-only lesson generation, no silent source substitution, no classroom-ready prose | prompts stay evidence-oriented, versioned, and explicitly non-authoritative for classroom final text | `no` | `no` | `yes` |
| `TASK-CLCH-REVIEW-001` | audit course delivery readiness and fail-closed risks | all governed downstream artifacts, active task card, fail-closed skill | audit report, release recommendation, unresolved risk list, pointer check | no silent rewrites of route state, no new lesson drafting, no scope expansion without governance update | audit covers route completeness, evidence integrity, drift risk, and release blocking issues | `no` | `no` | `yes` |

## Global Fail-Closed Rules

- Do not turn the course into a pure literary-history course.
- Do not turn the course into a pure linguistics-theory course.
- Do not turn the course into an AI tools course.
- Do not bypass Wang Li, Guo Xiliang, Qiu Xigui, and related authorized material boundaries.
- Do not move lesson-body prose into governance tasks.
- Do not mix in `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
- Do not promote NotebookLM extraction above `draft`, `synthetic`, or `teacher-review-required` without source-backed review.
- If source identity, locator metadata, or copyright risk is unclear, stop and mark `needs human review`.
