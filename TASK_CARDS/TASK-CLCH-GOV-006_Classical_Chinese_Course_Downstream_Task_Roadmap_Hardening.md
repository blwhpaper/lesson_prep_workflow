# TASK-CLCH-GOV-006 | Classical Chinese Course Downstream Task Roadmap Hardening

## Task Type

- task family: `TASK-CLCH-GOV-*`
- scope: downstream route hardening
- stage: after `TASK-CLCH-GOV-SKILL-001`, before `TASK-CLCH-LESSON-001`
- default mode: fail closed

## Task Intent

This task hardens the downstream Classical Chinese route after the governed material stage and before lesson-stage execution begins.

Its goal is to define the post-`TASK-CLCH-LESSON-001` task chain, task order, task boundaries, permitted outputs, prohibited outputs, fail-closed checks, and minimum operator-entry pointers so later agents do not rely on ad hoc inference.

This task does not authorize `TASK-CLCH-LESSON-001` execution, does not generate 16-week course-body content, and does not produce session package prose, assignment bodies, or AI activity sheets.

## Upstream Preconditions

- `TASK-CLCH-MAT-001 | Knowledge Map Extraction` is completed.
- `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` is completed.
- `TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit` is completed.
- The current branch is `task-clch-gov-006-downstream-task-roadmap-hardening`.
- `TASK-CLCH-LESSON-001` remains `next` and not started.

## Required Inputs

1. `AGENTS.md`
2. `GEMINI.md`
3. `GOVERNANCE/PLAN.md`
4. `GOVERNANCE/TASK_STATE.json`
5. `GOVERNANCE/TASK_INDEX.md`
6. `GOVERNANCE/CHANGE_LOG.md`
7. `docs/OPERATOR_GUIDE.md`
8. `COURSES/classical_chinese/ROADMAP.md`
9. `COURSES/classical_chinese/TASK_REGISTRY.md`
10. `CLOSEOUTS/TASK-CLCH-GOV-SKILL-001_Closeout.md`
11. current git state via `git status --short --branch`

## Required Outputs

- `TASK_CARDS/TASK-CLCH-GOV-006_Classical_Chinese_Course_Downstream_Task_Roadmap_Hardening.md`
- `CLOSEOUTS/TASK-CLCH-GOV-006_Closeout.md`
- synchronized route-pointer updates in `PLAN`, `TASK_STATE`, `TASK_INDEX`, `ROADMAP`, and `TASK_REGISTRY`
- a downstream route contract in `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
- minimal entry-point updates in `AGENTS.md`, `GEMINI.md`, and `docs/OPERATOR_GUIDE.md`

## Required Downstream Coverage

The hardened route must define at least these tasks:

- `TASK-CLCH-LESSON-001` | 16-Week Course Architecture
- `TASK-CLCH-LESSON-002` | Session Package Template And Evidence Contract
- `TASK-CLCH-LESSON-003` | Week 1-4 Lesson Package Build
- `TASK-CLCH-LESSON-004` | Week 5-8 Lesson Package Build
- `TASK-CLCH-LESSON-005` | Week 9-12 Lesson Package Build
- `TASK-CLCH-LESSON-006` | Week 13-16 Lesson Package Build
- `TASK-CLCH-ASSESS-001` | Assignments Rubrics And Translation Practice Assessment
- `TASK-CLCH-AI-001` | Student AI/Vibecoding Activity Protocol
- `TASK-CLCH-PROMPT-001` | NotebookLM Extraction Prompt Pack
- `TASK-CLCH-REVIEW-001` | Course Delivery Review And Fail-Closed Audit

For each downstream task, the roadmap must state:

- goal
- inputs
- outputs
- prohibited work
- acceptance standard
- whether classroom body generation is allowed
- whether student assignment generation is allowed
- whether NotebookLM evidence is required

## Allowed Changes

- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
- `docs/OPERATOR_GUIDE.md`
- `AGENTS.md`
- `GEMINI.md`
- `TASK_CARDS/TASK-CLCH-GOV-006_Classical_Chinese_Course_Downstream_Task_Roadmap_Hardening.md`
- `CLOSEOUTS/TASK-CLCH-GOV-006_Closeout.md`

## Disallowed Work

- do not execute `TASK-CLCH-LESSON-001`
- do not generate 16-week lesson prose
- do not generate session package bodies
- do not generate assignment bodies or answer keys
- do not generate AI activity content beyond governance-level route definition
- do not modify material artifacts
- do not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`

## Route Result Requirement

At closeout, the route must resolve to:

- `TASK-CLCH-GOV-006 | Classical Chinese Course Downstream Task Roadmap Hardening` = completed
- `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` = next
- `TASK-CLCH-LESSON-002` through `TASK-CLCH-REVIEW-001` = defined and pending

## Acceptance Commands

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`
- `grep -R "TASK-CLCH-GOV-006" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`
- `grep -R "TASK-CLCH-LESSON-002\\|TASK-CLCH-ASSESS-001\\|TASK-CLCH-AI-001\\|TASK-CLCH-PROMPT-001\\|TASK-CLCH-REVIEW-001" -n GOVERNANCE COURSES/classical_chinese`
- `grep -R "<<<<<<<\\|=======\\|>>>>>>>" -n . --exclude-dir=.git`
- `git diff --check`
