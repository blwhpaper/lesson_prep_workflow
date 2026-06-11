# TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary

## Purpose

This governance record defines how the `COURSES/classical_chinese` line must rank source authority, handle NotebookLM extraction output, preserve citation-boundary metadata, and stay inside copyright limits before any material extraction, design, or assessment work proceeds.

## Source Authority Ladder

- `L0 | repo governance SoT`
  - repository-level source of truth, workflow contract, fail-closed rules, and maturity gates
- `L1 | official course boundary / roadmap / task registry`
  - authorized course-line scope, route order, stage gates, and allowed task family behavior
- `L2 | uploaded textbook / reference corpus metadata`
  - declared source identity, author or editor, chapter or section, page or location, and other locator metadata for user-authorized sources
- `L3 | NotebookLM extraction notes`
  - raw extraction leads, outlines, snippet notes, topic traces, and structure hints derived from authorized source inputs
- `L4 | agent-generated summaries / matrices / drafts`
  - summaries, route tables, material maps, source indexes, draft matrices, and other agent-produced derivative structure
- `L5 | classroom-facing deliverables`
  - lesson-facing or classroom-facing outputs that may exist only after downstream maturity gates and human review

## Promotion Rules

- higher-authority levels govern lower-authority derivatives
- `L3` and `L4` may organize or summarize `L2`, but may not silently replace `L2`
- source level must be preserved explicitly in future source-derived artifacts
- no artifact may be promoted to classroom-facing status if its source level, locator metadata, or review status is unclear

## Mandatory Source Fields

Future source-derived artifacts for this course line must preserve these fields whenever the data exists:

- `source_title`
- `source_type`
- `source_author_or_editor`
- `source_level`
- `chapter_or_section`
- `page_or_location_if_available`
- `extraction_method`
- `copyright_risk`
- `classroom_use_scope`

## NotebookLM Rule

- NotebookLM output belongs to `L3`
- NotebookLM output is raw extraction support only
- NotebookLM output may be used for extraction clues, structure hints, source-location leads, and intermediate indexing
- NotebookLM output must not be treated as final handout prose, final lecture prose, final slide prose, or approved course text
- NotebookLM output requires human review and higher-authority source checking before any downstream promotion

## Copyright Boundary

Allowed handling:

- short quotation
- summary
- paraphrase
- structured index
- chapter or page locator
- knowledge-point mapping
- classroom-use prompting note
- teacher-only preparation draft

Forbidden handling:

- large-scale textbook copying
- substitute-textbook lecture notes
- downloadable reconstructed textbook packets
- source-free stitched prose
- direct publication of NotebookLM extraction output as final content
- long copyrighted textbook reproduction

## Fail-Closed Rules

- unknown source identity means no promotion to formal course material
- unknown chapter, section, page, or location means mark `pending verification`
- unknown copyright risk means output summary, locator, or index form only
- AI-generated wording must remain labeled `draft`, `synthetic`, or `teacher-review-required`
- unresolved ambiguity about authority, locator, or permission keeps the artifact below classroom-facing status

## Downstream Effect

- `TASK-CLCH-MAT-001` and later tasks must preserve source level, locator metadata, extraction method, copyright risk, and classroom-use scope
- no later Classical Chinese task may treat NotebookLM output as a textbook substitute
- the next governance route is `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract`
