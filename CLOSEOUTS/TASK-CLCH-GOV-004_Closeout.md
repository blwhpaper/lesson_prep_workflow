# TASK-CLCH-GOV-004 Closeout

## Current Branch

`task-clch-gov-004-task-routing-and-naming-convention-contract`

## Files Added

- `TASK_CARDS/TASK-CLCH-GOV-004_Task_Routing_And_Naming_Convention_Contract.md`
- `GOVERNANCE/TASK-CLCH-GOV-004_Task_Routing_And_Naming_Convention_Contract.md`
- `CLOSEOUTS/TASK-CLCH-GOV-004_Closeout.md`

## Files Modified

- `AGENTS.md`
- `GEMINI.md`
- `.cursor/rules/classical-chinese-course.mdc`
- `docs/OPERATOR_GUIDE.md`
- `LESSON_PREP_WORKFLOW_SOT.md`
- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`

## Summary

This task formalized the Classical Chinese task-routing and naming contract so future agents can map `TASK-CLCH-XXX 开工` into the correct task family, branch pattern, file pattern, and stage gate before any work begins.

It also locked pointer consistency across the roadmap, registry, governance plan, task state, task index, and change log, and advanced the next course-line route from governance into `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.

## Protocol Or Rule Summary

- keep the course namespace at `TASK-CLCH-*`
- classify every task into `GOV`, `MAT`, `PROMPT`, `LESSON`, `ASSESS`, or `REVIEW` before acting
- use `task-clch-<type>-<number>-<kebab-title>` for branches
- use `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md` for task-card and governance filenames
- use `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md` for closeouts
- governance tasks stay governance-only
- full course, full PPT, and full question-bank generation remain blocked unless explicitly authorized by task type and task card
- keep `ROADMAP`, `TASK_REGISTRY`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG` aligned

## Acceptance Commands And Results

- `git status --short --branch`: passed; branch is `task-clch-gov-004-task-routing-and-naming-convention-contract`. Working tree shows the expected `TASK-CLCH-GOV-004` additions and governance-file modifications.
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`: passed.
- `grep -R "TASK-CLCH-GOV-004" TASK_CARDS GOVERNANCE CLOSEOUTS COURSES/classical_chinese LESSON_PREP_WORKFLOW_SOT.md AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md .cursor/rules/classical-chinese-course.mdc`: passed; `TASK-CLCH-GOV-004` appears across the expected task-card, governance, closeout, course, SoT, operator, and agent-entry files.
- `grep -R "TASK-CLCH-MAT-001" COURSES/classical_chinese GOVERNANCE LESSON_PREP_WORKFLOW_SOT.md`: passed; the next-task pointer is aligned to `TASK-CLCH-MAT-001`.
- `grep -R "TASK-BTC\\|EDU-NESP\\|Lin Yutang\\|Thesis_Format_Fixer\\|DAILY_REVIEW" TASK_CARDS/TASK-CLCH-GOV-004_Task_Routing_And_Naming_Convention_Contract.md GOVERNANCE/TASK-CLCH-GOV-004_Task_Routing_And_Naming_Convention_Contract.md CLOSEOUTS/TASK-CLCH-GOV-004_Closeout.md || true`: passed as an informational anti-drift check; matches appear only where the contract explicitly lists forbidden drift targets.
- `git diff --check`: passed.

## Risks Or Unfinished Items

- `TASK-CLCH-MAT-001` remains not started in this closeout.
- No material extraction, prompt-pack authoring, lesson design, assessment design, or classroom-content generation was started.
