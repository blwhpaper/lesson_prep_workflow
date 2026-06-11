# TASK-CLCH-GOV-003 Closeout

## Current Branch

`task-clch-gov-003-classical-chinese-source-authority-and-copyright-boundary`

## Files Added

- `TASK_CARDS/TASK-CLCH-GOV-003_Classical_Chinese_Source_Authority_And_Copyright_Boundary.md`
- `GOVERNANCE/TASK-CLCH-GOV-003_Classical_Chinese_Source_Authority_And_Copyright_Boundary.md`
- `CLOSEOUTS/TASK-CLCH-GOV-003_Closeout.md`

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

This task formalized the Classical Chinese source-authority ladder from `L0` governance SoT through `L5` classroom-facing deliverables, established mandatory source fields for future source-derived artifacts, and locked NotebookLM into an extraction-only intermediate role rather than a publishable content role.

It also codified the copyright boundary: short quotation, summary, paraphrase, structured indexing, locator metadata, and teacher-only preparation drafts are allowed within boundary, while large-scale copying, substitute-textbook notes, reconstructed textbook packets, source-free stitched prose, and direct NotebookLM-to-final-content promotion are forbidden.

## Protocol Or Rule Summary

- preserve source level explicitly for later Classical Chinese tasks
- preserve locator metadata whenever available
- keep NotebookLM at `L3` and agent drafts at `L4`
- fail closed on unclear source, unclear locator, or unclear copyright risk
- label AI-generated wording as `draft`, `synthetic`, or `teacher-review-required`
- advance the next route to `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract`

## Acceptance Commands And Results

- `git status --short --branch`: passed; branch is `task-clch-gov-003-classical-chinese-source-authority-and-copyright-boundary`. Working tree shows the expected `TASK-CLCH-GOV-003` additions and governance-file modifications.
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`: passed.
- `grep -R "TASK-CLCH-GOV-003" -n TASK_CARDS GOVERNANCE CLOSEOUTS COURSES LESSON_PREP_WORKFLOW_SOT.md docs AGENTS.md GEMINI.md .cursor/rules || true`: passed; `TASK-CLCH-GOV-003` appears across the expected task-card, governance, closeout, course, SoT, operator, and agent-entry files.
- `grep -R "TASK-CLCH-GOV-004" -n GOVERNANCE COURSES LESSON_PREP_WORKFLOW_SOT.md || true`: passed; the next-task pointer is aligned to `TASK-CLCH-GOV-004`.
- `grep -R "NotebookLM.*final\\|替代教材\\|完整教材重构\\|大段复制" -n COURSES GOVERNANCE TASK_CARDS LESSON_PREP_WORKFLOW_SOT.md docs AGENTS.md GEMINI.md .cursor/rules || true`: passed; matches appear in the intended copyright and NotebookLM boundary rules.
- `git diff --check`: passed.

## Risks Or Unfinished Items

- `TASK-CLCH-GOV-004` is not yet created in this task and remains the next governance pointer only.
- No material extraction, lesson design, matrix generation, handout drafting, or classroom-content generation was started.
