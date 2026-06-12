# Classical Chinese Course Fail-Closed Audit Skill

## Purpose

Use this skill for future `COURSES/classical_chinese` tasks after `TASK-CLCH-GOV-SKILL-001`.

This skill is a mandatory fail-closed audit checklist for source-derived, maturity-sensitive, lesson-stage, assessment-stage, or publication-sensitive work.

It does not authorize lessons, assessments, or publication by itself.

## When To Read

Read this file after the active `TASK-CLCH-*` task card and before acting on:

- source-derived artifacts
- lesson-stage artifacts
- assessment-stage artifacts
- publication-sensitive artifacts
- AI-assisted or NotebookLM-assisted derivatives

## Audit Checklist

1. Source authority
   - Confirm the artifact stays within the Classical Chinese source-authority ladder `L0 -> L5`.
   - Reject any silent upgrade from `L3` NotebookLM extraction notes or `L4` agent drafts into `L5` classroom-facing deliverables.
   - If the source level is unclear, stop and mark `needs human review`.

2. Locator honesty
   - Confirm whether chapter, section, page, or equivalent locator is present.
   - If no exact locator exists, state `pending verification`.
   - Do not imply exact source backing when only topic-level or slot-level support exists.

3. Copyright and excerpt risk
   - Do not output long textbook passages.
   - Keep any excerpt short, traceable, and justified by the active task boundary.
   - If excerpt scope or classroom-use permission is unclear, output summary or index form only.

4. Maturity status
   - Preserve the current maturity label such as `draft` or `teacher-review-required`.
   - Do not relabel an artifact as `lesson-ready`, `assessment-ready`, or `publication-ready` without an authorized task and human review.
   - Treat all unresolved review flags as blocking for promotion.

5. NotebookLM output boundary
   - Keep NotebookLM output at `L3`.
   - Use NotebookLM only for extraction leads, indexing hints, uncertainty markers, or structural support.
   - Do not present NotebookLM wording as approved classroom prose.

6. Legacy imports prohibition
   - Treat `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` as prohibited by default.
   - Only touch legacy imports when the active task card explicitly authorizes audited legacy use.
   - Do not use legacy imports as silent evidence or fallback content.

7. Lesson-ready over-promotion risk
   - If the active task is not a lesson-family task with explicit authorization, do not draft lesson architecture, lesson flow, `完整教案`, or `完整课件`.
   - Material matrices, summaries, and governance artifacts must stay below lesson level.

8. Assessment-ready over-promotion risk
   - If the active task is not an assessment-family task with explicit authorization, do not draft assignments, rubrics, test items, or `题库答案`.
   - Diagnostic examples may not become student-facing assessment content by default.

9. Publication-ready over-promotion risk
   - Do not mark draft or internal artifacts as publishable.
   - Keep copyrighted, private, or unverified material out of publication-facing outputs.
   - If publication scope is unclear, keep the artifact internal and labeled draft.

10. Cross-project drift
    - Stay inside `COURSES/classical_chinese` and the active governance files.
    - Do not drift into other project lines or import unrelated content patterns.
    - If a request tries to mix projects, stop and mark `needs human review`.

11. Task-scope drift
    - Match the requested output to the active task family and task card.
    - Governance tasks may create only governance artifacts.
    - Material tasks may not produce lesson or assessment artifacts.
    - Lesson tasks may not silently jump to assessment or publication scope.

12. Source-backed versus invented content
    - Separate source-backed claims from synthetic structuring.
    - Mark AI-generated wording as `draft`, `synthetic`, or `teacher-review-required`.
    - Do not fabricate citations, locators, example pools, textbook passages, or source authority.

## Fail-Closed Triggers

Stop and mark `needs human review` when any of these conditions appears:

- task id, branch, `TASK_STATE`, `ROADMAP`, and `TASK_REGISTRY` do not align
- source identity is unclear
- source level is unclear
- locator evidence is missing but presented as exact
- copyright boundary is unclear
- NotebookLM output is being treated as final prose
- legacy imports are being used without explicit authorization
- the artifact is being promoted as `lesson-ready`, `assessment-ready`, or `publication-ready` without approval
- the request drifts outside the active task family
- the artifact includes invented source-backed claims

## Minimum Output Rule

If the audit does not pass, reduce the output to one of these forms only:

- summary
- index
- locator list
- draft
- synthetic note
- teacher-review-required note

## Response Footer Reminder

For governed Classical Chinese tasks, end with:

- current branch
- changed files
- protocol or rule summary
- acceptance-command results
- risks or unfinished items
