# TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary

## Objective

Establish the Classical Chinese governance layer for source authority and copyright boundary so future agents can distinguish official governance, course boundary files, textbook metadata, NotebookLM extraction notes, agent-generated drafts, and any later classroom-facing outputs without promoting the wrong layer.

## Scope

- define the Classical Chinese source-authority ladder from `L0` through `L5`
- define the copyright boundary for textbook, reference, NotebookLM, and agent-derived material handling
- define mandatory source fields for future source-derived artifacts
- define NotebookLM non-substitution rules
- define fail-closed rules for unclear source, locator, or copyright conditions
- update course, governance, and agent-entry documents so this boundary becomes part of normal task execution

## In Scope Outputs

- governance task card
- governance record
- closeout record
- source-authority ladder
- mandatory source-field contract
- copyright handling rules
- fail-closed promotion rules
- minimal updates to course boundary, roadmap, registry, operator guide, and agent entry files

## Out Of Scope

- lesson plans
- slides or slide outlines
- handouts
- question banks
- classroom content matrices
- `TASK-CLCH-MAT-001`
- `16-session core material matrix`
- textbook copying
- full NotebookLM-derived prose
- PDF, PPT, or DOCX creation

## Required Rules

1. The source-authority ladder must include:
   - `L0` repo governance SoT
   - `L1` official course boundary / roadmap / task registry
   - `L2` uploaded textbook / reference corpus metadata
   - `L3` NotebookLM extraction notes
   - `L4` agent-generated summaries / matrices / drafts
   - `L5` classroom-facing deliverables
2. `L3` NotebookLM extraction notes and `L4` agent-generated drafts may organize or summarize higher-authority inputs, but may not replace them.
3. NotebookLM output may be used only as extraction clues, structural hints, and intermediate notes. It must not be treated as final publishable prose.
4. Allowed handling includes short quotation, summary, paraphrase, structured indexing, chapter or page location, knowledge-point mapping, and teacher-only preparation drafts.
5. Forbidden handling includes large-scale textbook copying, substitute-textbook lecture notes, downloadable reconstructed textbook packets, source-free stitched prose, and treating NotebookLM output as final content.
6. Every future source-derived artifact must preserve these source fields whenever the data exists:
   - `source_title`
   - `source_type`
   - `source_author_or_editor`
   - `source_level`
   - `chapter_or_section`
   - `page_or_location_if_available`
   - `extraction_method`
   - `copyright_risk`
   - `classroom_use_scope`
7. If source identity is unclear, the artifact may not be upgraded to formal course material.
8. If chapter, section, page, or equivalent locator is unclear, the artifact must be marked `pending verification`.
9. If copyright risk is unclear, output may remain only summary, index, or locator form.
10. AI-generated content must be labeled `draft`, `synthetic`, or `teacher-review-required` until human review promotes it.
11. The next route after completion is `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract`.

## Acceptance

Run at least:

- `git status --short --branch`
- `python3 -m json.tool GOVERNANCE/TASK_STATE.json >/dev/null`
- `grep -R "TASK-CLCH-GOV-003" -n TASK_CARDS GOVERNANCE CLOSEOUTS COURSES LESSON_PREP_WORKFLOW_SOT.md docs AGENTS.md GEMINI.md .cursor/rules || true`
- `grep -R "TASK-CLCH-GOV-004" -n GOVERNANCE COURSES LESSON_PREP_WORKFLOW_SOT.md || true`
- `grep -R "NotebookLM.*final\\|替代教材\\|完整教材重构\\|大段复制" -n COURSES GOVERNANCE TASK_CARDS LESSON_PREP_WORKFLOW_SOT.md docs AGENTS.md GEMINI.md .cursor/rules || true`
- `git diff --check`

## Completion Condition

This task is complete only when the governance artifacts exist, the Classical Chinese boundary and entry-protocol files include the source-authority and copyright rules, the route advances to `TASK-CLCH-GOV-004`, and all acceptance checks pass.
