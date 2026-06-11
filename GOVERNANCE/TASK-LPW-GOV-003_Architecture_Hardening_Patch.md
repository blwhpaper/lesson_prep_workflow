# TASK-LPW-GOV-003 Architecture Hardening Patch

## Purpose

This patch hardens repository architecture only. It does not create course content, lesson plans, question banks, assessments, or student-facing materials.

## Architecture Layers

1. Workflow governance: repository-wide authority, state, task routing, fail-closed rules, and publication boundaries.
2. Shared reusable patterns: only mature, decontextualized `L6` patterns belong in `SHARED/`.
3. Course instance scaffold: each course owns its isolated directory, state, and lifecycle.
4. Course-specific SOT: each course defines its own identity, source scope, goals, and prohibitions.
5. Material database maturity: artifacts must move through `L0 -> L1 -> L2 -> L3 -> L4 -> L5 -> L6` without bypass.
6. NotebookLM intake and review: tool output enters only as draft / extracted / unverified intake.
7. Source audit: traceability, edition, locator, reliability, and authority checks are mandatory before promotion.
8. Assessment audit: closed-book or scored use requires explicit suitability review.

## Hardening Decisions

- `TASK-LPW-GOV-003` is canonically titled `Architecture Hardening Patch`.
- Any prior drift that mislabels `TASK-LPW-GOV-003` as source audit or NotebookLM review is invalid.
- NotebookLM output may be stored, reviewed, and compared, but never promoted directly to source-audited, lesson-ready, or assessment-ready material.
- Material database maturity gates are mandatory and sequential.
- Agent entry is fail-closed when SOT, task card, evidence, or task state conflicts are missing.
- Public GitHub publication excludes copyrighted textbook full text, unauthorized scans, student privacy data, and internal sensitive materials.

## Required Repository Distinctions

- `GOVERNANCE/`: workflow governance and repository protocols
- `SHARED/`: reusable patterns only after `L6` approval
- `COURSES/<course>/`: course instance scaffold and isolated delivery lifecycle
- `COURSES/<course>/COURSE_SOT.md`: course-specific authority
- `COURSES/<course>/MATERIAL_DATABASE/`: maturity-controlled course material store
- `COURSES/<course>/NOTEBOOKLM/`: NotebookLM intake prompts and outputs
- `COURSES/<course>/SOURCES/`: source evidence and audit support
- `COURSES/<course>/ASSESSMENTS/`: assessment design and suitability review artifacts

## Non-Goals

- No lesson production
- No course expansion implementation
- No assessment bank production
- No source-content upload or copyright-risk publication
