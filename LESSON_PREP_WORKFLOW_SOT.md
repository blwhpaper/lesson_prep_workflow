# Lesson Prep Workflow Source of Truth

## Repository Identity

This is the general lesson-preparation workflow repository. Its first course instance is `classical_chinese_translation`; future instances may include `modern_chinese`, `college_english`, and `gaokao_english`.

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
