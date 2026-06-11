# TASK-CLCH-GOV-002 Governance Record

## Title

`TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course`

## Purpose

Create a stable entry contract for multiple agents working inside `COURSES/classical_chinese` so explicit operator starts such as `TASK-CLCH-XXX 开工` do not drift across courses, tasks, source boundaries, or output stages.

## Protocol Contract

### Entry Trigger

- the protocol is activated when the operator says `TASK-CLCH-XXX 开工`
- only the named `TASK-CLCH-*` task may become active

### Governance Header

- course code: `CLCH`
- course line: `classical_chinese`
- task family: `TASK-CLCH-*`
- default stage for this task: governance only
- fail-closed mode: required

### Minimum Read Order

1. `AGENTS.md`
2. `LESSON_PREP_WORKFLOW_SOT.md`
3. `GOVERNANCE/PLAN.md`
4. `GOVERNANCE/TASK_STATE.json`
5. `GOVERNANCE/TASK_INDEX.md`
6. `GOVERNANCE/CHANGE_LOG.md`
7. `docs/OPERATOR_GUIDE.md`
8. `COURSES/classical_chinese/COURSE_BOUNDARY.md`
9. `COURSES/classical_chinese/ROADMAP.md`
10. `COURSES/classical_chinese/TASK_REGISTRY.md`
11. the current `TASK-CLCH-*` task card
12. the previous closeout
13. `git status --short --branch`

### Anti-Drift Rules

- do not read another course directory by default
- do not read an external repository by default
- do not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`
- use only the files needed for the active task

### Source And Copyright Rules

- Wang Li, Guo Xiliang, Qiu Xigui, and related textbooks are governed source inputs only after user upload or NotebookLM-assisted extraction support
- agents must not demand or reconstruct long copyrighted textbook passages
- NotebookLM output remains raw intake support until later review gates promote it

### Output Rules

- governance tasks may produce only governance artifacts
- do not generate lesson plans, slides, question banks, papers, or formal classroom materials in this stage
- every response must include current branch, changed files, protocol summary, acceptance results, and risks or unfinished items

### Fail-Closed Conditions

Stop and report `needs human review` if any of the following conflict:

- requested task id
- current branch
- `GOVERNANCE/TASK_STATE.json`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- requested output stage

## Route Result

`TASK-CLCH-GOV-002` completes the cross-agent entry layer and advances the next route to `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary`.
