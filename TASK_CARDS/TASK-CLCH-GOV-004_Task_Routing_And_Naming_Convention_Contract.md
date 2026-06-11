# TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract

## Objective

Establish the Classical Chinese governance layer for task routing, task-family recognition, naming conventions, and route-pointer consistency so future agents can reliably interpret `TASK-CLCH-XXX 开工` without drifting into the wrong stage, file pattern, or project line.

## Scope

- define the `TASK-CLCH-*` namespace
- define the task-family prefixes `GOV`, `MAT`, `PROMPT`, `LESSON`, `ASSESS`, and `REVIEW`
- define branch, task-card, governance-record, and closeout naming conventions
- define which task families may remain governance-only and which may enter materials, prompts, lessons, assessment, or review
- define cross-file pointer consistency rules for `ROADMAP`, `TASK_REGISTRY`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG`
- update the Classical Chinese boundary and entry files so the contract becomes normal execution behavior

## In Scope Outputs

- governance task card
- governance record
- closeout record
- task-family routing contract
- naming convention rules
- route-validation rules
- minimal updates to course boundary, roadmap, registry, SoT, operator guide, and agent-entry files

## Out Of Scope

- lesson plans
- slides or slide outlines
- handouts
- question banks
- source extraction output
- `TASK-CLCH-MAT-001`
- `16-session core material matrix`
- concrete Classical Chinese teaching content
- PDF, PPT, or DOCX creation

## Required Rules

1. The Classical Chinese task namespace must remain `TASK-CLCH-*`.
2. Task-family meanings must be explicit:
   - `TASK-CLCH-GOV-*` = governance, boundary, routing, protocol, index, and agent constraints only
   - `TASK-CLCH-MAT-*` =教材材料, knowledge map extraction, topic clustering, text or grammar or训诂or文字学 material mapping below lesson level
   - `TASK-CLCH-PROMPT-*` = NotebookLM, Claude, Cursor, Codex, and similar prompt packs or extraction prompt contracts
   - `TASK-CLCH-LESSON-*` = lesson plans, classroom activities, handouts, and PPT structure for specific lessons or units
   - `TASK-CLCH-ASSESS-*` = homework, quizzes, rubrics, and student-output evaluation
   - `TASK-CLCH-REVIEW-*` = retrospectives, quality review, and version audit
3. Branch naming must use `task-clch-<type>-<number>-<kebab-title>`.
4. Task-card and governance filenames must use `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`.
5. Closeout filenames must use `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md`.
6. Governance tasks may create only governance shells, contracts, boundaries, routes, indexes, or protocol artifacts.
7. Material tasks may structure source-derived content below lesson level, but may not jump to full lesson writing.
8. Prompt tasks may define prompt packs and extraction workflows, but may not promote prompts into approved classroom prose by themselves.
9. Lesson, assessment, and review tasks may begin only when the roadmap and registry show that their prerequisites are satisfied.
10. No task may directly generate a full course, full PPT set, or full question bank unless the active task family and task card explicitly authorize that output scope.
11. Agents must not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
12. After completion, the next route must be `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.
13. Route pointers must align across `TASK_REGISTRY`, `ROADMAP`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG`.

## Acceptance

Run at least:

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`
- `grep -R "TASK-CLCH-GOV-004" TASK_CARDS GOVERNANCE CLOSEOUTS COURSES/classical_chinese LESSON_PREP_WORKFLOW_SOT.md AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md .cursor/rules/classical-chinese-course.mdc`
- `grep -R "TASK-CLCH-MAT-001" COURSES/classical_chinese GOVERNANCE LESSON_PREP_WORKFLOW_SOT.md`
- `grep -R "TASK-BTC\\|EDU-NESP\\|Lin Yutang\\|Thesis_Format_Fixer\\|DAILY_REVIEW" TASK_CARDS/TASK-CLCH-GOV-004_Task_Routing_And_Naming_Convention_Contract.md GOVERNANCE/TASK-CLCH-GOV-004_Task_Routing_And_Naming_Convention_Contract.md CLOSEOUTS/TASK-CLCH-GOV-004_Closeout.md || true`
- `git diff --check`

## Completion Condition

This task is complete only when the governance artifacts exist, the Classical Chinese boundary and entry-protocol files include the routing and naming contract, the route advances to `TASK-CLCH-MAT-001`, and all acceptance checks pass.
