# TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course

## Objective

Establish a governed cross-agent entry protocol for the `COURSES/classical_chinese` line so agents such as Codex, Cursor, Antigravity, Claude, and Gemini can safely start work when the operator says `TASK-CLCH-XXX 开工`.

## Scope

- define the trigger rule for `TASK-CLCH-XXX 开工`
- define the Classical Chinese governance header and minimum read order
- harden fail-closed checks against branch, task-state, roadmap, and registry drift
- codify source, copyright, and anti-drift boundaries for this course line
- define the required response footer and acceptance checks for governed execution

## In Scope Outputs

- governance task card
- governance record
- course-boundary updates
- roadmap and task-registry updates
- operator and agent entry instructions
- closeout record

## Out Of Scope

- lesson plans
- slides or slide outlines
- question banks
- worksheets
- assessment items
- papers
- formal classroom materials
- large copyrighted textbook excerpts
- NotebookLM output promotion

## Required Rules

1. The entry trigger is `TASK-CLCH-XXX 开工`.
2. The protocol applies only to `COURSES/classical_chinese`.
3. Agents must follow the minimum read order declared by the governance layer.
4. Agents must not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
5. Governance tasks must not generate lessons, slides, question banks, papers, or formal classroom materials.
6. Wang Li, Guo Xiliang, Qiu Xigui, and related textbooks are source inputs only after user upload or NotebookLM-supported extraction and may not be reproduced in long copyrighted blocks.
7. Agents must return current branch, changed files, protocol summary, acceptance-command results, and risks or unfinished items.
8. If task number, current branch, `TASK_STATE`, `TASK_REGISTRY`, or `ROADMAP` conflict, the agent must stop and report `needs human review`.
9. Agents must use a token-saving reading strategy and avoid whole-repo scans.
10. The next route after completion is `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary`.

## Acceptance

Run at least:

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`
- `grep -R "TASK-CLCH-GOV-002" -n TASK_CARDS GOVERNANCE CLOSEOUTS COURSES/classical_chinese LESSON_PREP_WORKFLOW_SOT.md docs/OPERATOR_GUIDE.md AGENTS.md GEMINI.md .cursor .agents 2>/dev/null || true`
- `grep -R "TASK-CLCH-GOV-003" -n GOVERNANCE/TASK_STATE.json GOVERNANCE/PLAN.md COURSES/classical_chinese/ROADMAP.md COURSES/classical_chinese/TASK_REGISTRY.md`
- `grep -R "BTC_WATCHFLOW\\|NESP\\|Lin Yutang\\|Thesis_Format_Fixer" -n COURSES/classical_chinese TASK_CARDS/TASK-CLCH-GOV-002_Cross_Agent_Entry_Protocol_For_Classical_Chinese_Course.md GOVERNANCE/TASK-CLCH-GOV-002_Cross_Agent_Entry_Protocol_For_Classical_Chinese_Course.md 2>/dev/null || true`
- `git diff --check`

## Completion Condition

This task is complete only when the protocol artifacts exist, the course boundary and operator guidance are updated, the governance route advances to `TASK-CLCH-GOV-003`, and all acceptance checks pass.
