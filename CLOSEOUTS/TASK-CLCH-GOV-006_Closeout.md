# TASK-CLCH-GOV-006 Closeout

## Current Branch

`task-clch-gov-006-downstream-task-roadmap-hardening`

## Files Added

- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
- `TASK_CARDS/TASK-CLCH-GOV-006_Classical_Chinese_Course_Downstream_Task_Roadmap_Hardening.md`
- `CLOSEOUTS/TASK-CLCH-GOV-006_Closeout.md`

## Files Modified

- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `AGENTS.md`
- `GEMINI.md`
- `docs/OPERATOR_GUIDE.md`

## Summary

This task completed the downstream route hardening for the Classical Chinese course line after `TASK-CLCH-GOV-SKILL-001` and before `TASK-CLCH-LESSON-001`.

It registered `TASK-CLCH-GOV-006` across the governance pointers, created a dedicated downstream roadmap file, and expanded the downstream sequence through `LESSON`, `ASSESS`, `AI`, `PROMPT`, and `REVIEW` families so later agents no longer have to infer post-architecture scope from chat context.

It did not execute `TASK-CLCH-LESSON-001`, did not generate a 16-week lesson body, did not generate session package prose, and did not produce assignment bodies, answer keys, or AI activity content.

## Pointer Result

- `TASK-CLCH-GOV-006 | Classical Chinese Course Downstream Task Roadmap Hardening` -> completed
- `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` -> next
- `TASK-CLCH-LESSON-002` through `TASK-CLCH-REVIEW-001` -> defined and pending

## Downstream Hardening Result

The downstream route now explicitly defines:

- task order after `TASK-CLCH-LESSON-001`
- stage boundaries between course architecture, template definition, week-block package drafting, assessment, AI protocol, NotebookLM prompt pack, and review audit
- whether each task may generate classroom body text
- whether each task may generate student assignments
- whether NotebookLM evidence is mandatory
- fail-closed anti-drift rules against literary-history drift, pure-theory drift, AI-tools-course drift, unauthorized source bypass, governance-to-lesson leakage, and unrelated-project contamination

## Acceptance Commands And Results

- `git status --short --branch`: passed
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/tmp/task_state_check.json`: passed
- `grep -R "TASK-CLCH-GOV-006" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed
- `grep -R "TASK-CLCH-LESSON-002\\|TASK-CLCH-ASSESS-001\\|TASK-CLCH-AI-001\\|TASK-CLCH-PROMPT-001\\|TASK-CLCH-REVIEW-001" -n GOVERNANCE COURSES/classical_chinese`: passed
- `grep -R "<<<<<<<\\|=======\\|>>>>>>>" -n . --exclude-dir=.git`: passed
- `git diff --check`: passed

## Risks Or Unfinished Items

- `TASK-CLCH-LESSON-001` remains not started.
- Downstream tasks are now bounded, but individual task cards for `TASK-CLCH-LESSON-001` and later tasks still need to be created at their execution turns.
- Any later task with unclear source locators, copyright risk, or route mismatch must still fail closed.
