# Lesson Prep Workflow Source of Truth

## Repository Identity

This is the general lesson-preparation workflow repository. Its first course instance is `classical_chinese_translation`; it now also contains a governance-shell registration for `classical_chinese`. Future instances may include `modern_chinese`, `college_english`, and `gaokao_english`.

Top-level directories govern protocols, templates, cross-course reuse, and shared skills. Every course owns its own `COURSE_SOT`, `COURSE_PLAN`, `COURSE_TASK_STATE`, and `COURSE_TASK_INDEX`.

## Isolation And Reuse

- Course instances are isolated by default.
- Shared templates and mature reusable patterns belong only in `SHARED/`.
- Material from one course must not be copied into another without a governed intake and adaptation review.
- Only L6 artifacts may become cross-course shared patterns.

## Material Authority

NotebookLM output is always raw output, not formal course material. Formal material must pass:

1. source audit;
2. reliability grading;
3. course adaptation;
4. assessment suitability check.

Prompts are workflow inputs only. They are not approved lesson plans, question banks, textbooks, course outcomes, or publishable course artifacts by themselves.

## Canonical Workflow

`source intake -> source audit -> material database -> course adaptation -> lesson pathway -> lesson plan -> student task -> assessment -> course closeout/reuse`

When authority, provenance, maturity, or ownership is unclear, apply `GOVERNANCE/FAIL_CLOSED_RULES.md`.

## Architecture Boundary

The repository architecture must keep these layers distinct:

1. workflow governance;
2. shared reusable patterns;
3. course instance scaffold;
4. course-specific SOT;
5. material database maturity levels;
6. NotebookLM intake and review;
7. source audit;
8. assessment audit.

NotebookLM output begins below source-audited status and may not bypass the material maturity chain. Public publication boundaries are governed separately and must exclude copyrighted full text, unauthorized scans, student privacy, and internal sensitive artifacts.
Prompt and NotebookLM governance must also preserve input scope, forbidden-input boundaries, review gates, and publication boundaries as explicit repository metadata.

## Registered Classical Chinese Governance Route

`TASK-CLCH-GOV-000 | Classical Chinese Course Roadmap And Task Registry` establishes only the governance shell for `COURSES/classical_chinese`.

- It does not activate formal lesson production.
- NotebookLM output for this course line must first pass intake and citation-boundary review.
- Material mapping must precede lesson design, and lesson design must precede assessment/export work.

## Classical Chinese Boundary Bootstrap Entry

`TASK-CLCH-GOV-001 | Classical Chinese Course Boundary Bootstrap` is the stable entry point for governed execution of the standalone `classical_chinese` route.

- When a user explicitly starts a `TASK-CLCH-*` task, that task card defines the active course line for execution even if `CURRENT_COURSE.md` still points to another default course.
- Agents must read the Classical Chinese boundary stack before acting:
  - `COURSES/classical_chinese/COURSE_BOUNDARY.md`
  - `COURSES/classical_chinese/ROADMAP.md`
  - `COURSES/classical_chinese/TASK_REGISTRY.md`
  - the current `TASK-CLCH-*` card
  - the previous `TASK-CLCH-*` closeout
- The first material-design gate for this course is not lesson drafting. The required next route is:
  - `TASK-CLCH-MAT-001 | Knowledge Map Extraction`
  - `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix`
  - only then may teaching-design tasks begin
- AI/vibecoding belongs only to the method layer for this course line and must not replace Ancient Chinese knowledge ontology.
