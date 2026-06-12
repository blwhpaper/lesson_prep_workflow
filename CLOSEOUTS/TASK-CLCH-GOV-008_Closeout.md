# TASK-CLCH-GOV-008 Closeout

## Current Branch

`task-clch-gov-008-downstream-task-registry-realignment-to-four-batch-lesson-build-plan`

## Files Added

- `TASK_CARDS/TASK-CLCH-GOV-008_Downstream_Task_Registry_Realignment_To_Four_Batch_Lesson_Build_Plan.md`
- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md`
- `CLOSEOUTS/TASK-CLCH-GOV-008_Closeout.md`

## Files Modified

- `AGENTS.md`
- `GEMINI.md`
- `docs/OPERATOR_GUIDE.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`

## Realignment Summary

This governance-only task realigned the downstream registry from the GOV-007 expanded governance chain to the governed four-batch lesson build route.

Completed realignments:

- made `TASK-CLCH-GOV-008` the latest downstream execution-order authority
- kept `TASK-CLCH-GOV-007` as a historical interpretation layer instead of deleting it
- moved the competency-matrix boundary into `TASK-CLCH-LESSON-001`
- moved the source evidence contract into `TASK-CLCH-LESSON-002`
- folded workflow constraints into `TASK-CLCH-LESSON-002` and `TASK-CLCH-REVIEW-001`
- folded QA into `TASK-CLCH-REVIEW-001`
- replaced `TASK-CLCH-DELIVERY-001` with `TASK-CLCH-LESSON-003` through `TASK-CLCH-LESSON-006`
- set the next task to `TASK-CLCH-LESSON-001 | 16-Week Course Architecture And Competency Matrix Boundary`

## GOV-008 Supersession Rule

`TASK-CLCH-GOV-008` supersedes `TASK-CLCH-GOV-007` for downstream execution order only.

- `TASK-CLCH-GOV-007` remains a historical governance record.
- future downstream agents must first read `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md`
- future downstream agents must then read `DOWNSTREAM_TASK_ROADMAP.md` and `DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`
- future downstream agents must use the GOV-008 four-batch lesson-build route as the current mainline

## Final Downstream Task List

1. `TASK-CLCH-LESSON-001｜16-Week Course Architecture And Competency Matrix Boundary`
2. `TASK-CLCH-PROMPT-001｜NotebookLM Extraction Prompt Pack`
3. `TASK-CLCH-LESSON-002｜Session Package Template, Source Evidence Contract And Build Standard`
4. `TASK-CLCH-ASSESS-001｜Assessment Framework And Translation Practice Rubrics`
5. `TASK-CLCH-AI-001｜Student AI/Vibecoding Activity Protocol`
6. `TASK-CLCH-LESSON-003｜Week 1-4 Lesson Package Build`
7. `TASK-CLCH-LESSON-004｜Week 5-8 Lesson Package Build`
8. `TASK-CLCH-LESSON-005｜Week 9-12 Lesson Package Build`
9. `TASK-CLCH-LESSON-006｜Week 13-16 Lesson Package Build`
10. `TASK-CLCH-REVIEW-001｜Course Delivery Review, Source Evidence Audit And Fail-Closed Check`

## Non-Generated Outputs

This task did not generate lesson正文, PPT, 题库, 课堂材料, 翻译材料, or student assignment bodies.

## CLAUDE.md Note

`CLAUDE.md` was not present at the repository root during this task. It was not created and was not assumed to exist.

## Acceptance Commands And Results

- `git status --short --branch`: passed; branch = `task-clch-gov-008-downstream-task-registry-realignment-to-four-batch-lesson-build-plan`; modified files and three new governed files present as expected.
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`: passed.
- `grep -R "TASK-CLCH-GOV-008" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed; registry, roadmap, state, index, change log, task card, closeout, and agent-entry files all contain `TASK-CLCH-GOV-008`.
- `grep -R "Downstream Task Registry Realignment To Four-Batch Lesson Build Plan" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed; title appears in state-aligned governance files, task card, and closeout.
- `grep -R "TASK-CLCH-LESSON-001｜16-Week Course Architecture And Competency Matrix Boundary" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed; exact fullwidth-title form appears in this closeout.
- `grep -R "TASK-CLCH-COMP-001.*latest\\|TASK-CLCH-MAT-003.*latest\\|TASK-CLCH-WORKFLOW-001.*latest\\|TASK-CLCH-QA-001.*latest\\|TASK-CLCH-DELIVERY-001.*latest" -n GOVERNANCE COURSES/classical_chinese AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md || true`: returned one non-actionable match in `DOWNSTREAM_TASK_REGISTRY_REALIGNMENT.md`; manual review confirmed superseded tasks are described as folded or historical, not as the latest downstream mainline.
- `grep -R "TASK-CLCH-LESSON-001.*completed" -n GOVERNANCE COURSES/classical_chinese || true`: passed with no matches.
- `grep -R "Week 1-4 Lesson Package Build\\|Week 5-8 Lesson Package Build\\|Week 9-12 Lesson Package Build\\|Week 13-16 Lesson Package Build" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed; four batch-build task titles appear in roadmap, task index, task card, realignment file, and closeout.
- `git diff --check`: passed.

## Next Task

`TASK-CLCH-LESSON-001｜16-Week Course Architecture And Competency Matrix Boundary`
