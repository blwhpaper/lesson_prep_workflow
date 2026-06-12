# TASK-CLCH-GOV-007 Closeout

## Current Branch

`task-clch-gov-007-downstream-task-sequence-optimization-and-competency-matrix-boundary-patch`

## Files Added

- `TASK_CARDS/TASK-CLCH-GOV-007_Downstream_Task_Sequence_Optimization_And_Competency_Matrix_Boundary_Patch.md`
- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`
- `CLOSEOUTS/TASK-CLCH-GOV-007_Closeout.md`

## Files Modified

- `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
- `COURSES/classical_chinese/ROADMAP.md`
- `COURSES/classical_chinese/TASK_REGISTRY.md`
- `COURSES/classical_chinese/COURSE_BOUNDARY.md`
- `GOVERNANCE/PLAN.md`
- `GOVERNANCE/TASK_STATE.json`
- `GOVERNANCE/TASK_INDEX.md`
- `GOVERNANCE/CHANGE_LOG.md`
- `docs/OPERATOR_GUIDE.md`
- `AGENTS.md`
- `GEMINI.md`

## Summary

This task completed a governance-only downstream sequence patch for the Classical Chinese course line.

It did not execute `TASK-CLCH-LESSON-001`, did not generate lesson-body prose, did not generate a 16-week full lesson package, and did not generate PPT, question-bank, translation-material, or classroom-text outputs.

## Sequence Optimization Result

The downstream route was updated from the earlier week-block package sequence into this latest execution order:

1. `TASK-CLCH-LESSON-001 | 16-Week Course Architecture`
2. `TASK-CLCH-COMP-001 | Classical Chinese Competency Matrix And Assessment Boundary`
3. `TASK-CLCH-LESSON-002 | Weekly Unit And Session Blueprint`
4. `TASK-CLCH-MAT-003 | Session-Level Source Material Allocation`
5. `TASK-CLCH-PROMPT-001 | NotebookLM Extraction Prompt Pack`
6. `TASK-CLCH-LESSON-003 | Sample Lesson Package Prototype`
7. `TASK-CLCH-WORKFLOW-001 | Teacher Preparation Workflow`
8. `TASK-CLCH-AI-001 | Student AI/Vibecoding Task Protocol`
9. `TASK-CLCH-ASSESS-001 | Student Output Rubric And Evidence Checklist`
10. `TASK-CLCH-QA-001 | Lesson Package Quality Audit Protocol`
11. `TASK-CLCH-DELIVERY-001 | Full 16-Week Lesson Package Generation Plan`

The optimization made these changes:

- moved the competency matrix ahead of all lesson-package scale-up
- replaced immediate week-block production with a sample-package validation step
- moved teacher workflow before student AI and assessment protocol finalization
- inserted QA before any full 16-week batch-generation plan
- reframed the 11-task chain as a runnable delivery shell rather than a claim that all 16-week preparation is complete

## Competency Matrix Boundary Result

The competency matrix is now written into the downstream entry layer as:

- a boundary
- an acceptance contract
- an evidence-mapping frame
- a drift-rejection rule

Future downstream tasks must read both:

1. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_ROADMAP.md`
2. `COURSES/classical_chinese/GOVERNANCE/DOWNSTREAM_TASK_SEQUENCE_OPTIMIZATION.md`

This makes `TASK-CLCH-COMP-001` a mandatory prerequisite before lesson-package prototyping, teacher workflow design, AI task protocol design, assessment rubric design, QA protocol design, and 16-week generation planning.

## CLAUDE.md Note

The operator-required `CLAUDE.md` file was not present at the repository root during this task. Execution proceeded under the stated authority order `repo current files and terminal state > CLAUDE/AGENTS/GEMINI > governance SoT > course roadmap/registry/downstream roadmap > task card/closeout > memory or inference`, with the missing file treated as absent rather than inferred.

## Acceptance Commands And Results

- `git status --short --branch`: passed
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`: passed
- `grep -R "TASK-CLCH-GOV-007" -n GOVERNANCE COURSES/classical_chinese TASK_CARDS CLOSEOUTS AGENTS.md GEMINI.md docs/OPERATOR_GUIDE.md`: passed
- `grep -R "TASK-CLCH-LESSON-001" -n GOVERNANCE COURSES/classical_chinese`: passed
- `grep -R "TASK-CLCH-LESSON-001.*completed" -n GOVERNANCE COURSES/classical_chinese || true`: passed with no matches
- `git diff --check`: passed

## Next Task

`TASK-CLCH-LESSON-001 | 16-Week Course Architecture`

## Risks Or Unfinished Items

- `TASK-CLCH-LESSON-001` has not started.
- New downstream task cards for `TASK-CLCH-COMP-001`, `TASK-CLCH-MAT-003`, `TASK-CLCH-WORKFLOW-001`, `TASK-CLCH-QA-001`, and `TASK-CLCH-DELIVERY-001` do not yet exist and must be created only at their execution turns.
- `TASK-CLCH-GOV-006` remains historical and informative; later agents must not mistakenly treat its old week-block order as the latest execution layer.
