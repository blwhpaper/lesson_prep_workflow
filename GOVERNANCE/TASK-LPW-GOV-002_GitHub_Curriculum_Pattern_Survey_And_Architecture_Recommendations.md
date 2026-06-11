# TASK-LPW-GOV-002 | GitHub Curriculum Pattern Survey And Architecture Recommendations

## Purpose And Scope

This document converts the supplied GitHub curriculum-repository survey summary into repository governance guidance for `lesson_prep_workflow`. It is an architecture pattern review, not a source intake or course-content review.

External repositories and public examples considered by the survey are architecture pattern references only. They do not become course-content sources, do not establish disciplinary authority, and do not bypass source audit, reliability grading, course adaptation, assessment suitability review, copyright review, or the repository's material-maturity gates.

No large-scale web research was repeated during this closeout. Recommendations were adapted to the current uppercase repository structure:

- `GOVERNANCE/`
- `COURSES/`
- `SHARED/`
- `SKILLS/`
- `TASK_CARDS/`
- `CLOSEOUTS/`

## Survey Findings

### 1. Course Repo Template Pattern

**Pattern summary:** A reusable repository template defines common folders, contributor guidance, build conventions, and starter artifacts from which a course repository can be created.

**Typical structure:** Root documentation and contribution rules; templates for syllabus, modules, lessons, assignments, and metadata; optional automation for validation or publishing.

**Strengths:** Fast initialization, consistent navigation, repeatable governance, and lower setup cost for new courses.

**Risks:** The template can become too prescriptive, course-specific assumptions can leak into shared structure, and copied repositories can drift without an upgrade path.

**Fit for lesson_prep_workflow:** Strong conceptual fit. The repository already provides a general workflow shell while treating `COURSES/` entries as governed instances.

**What to borrow / what not to borrow:** Borrow stable root contracts, reusable templates in `SHARED/`, and explicit course bootstrap requirements. Do not flatten all courses into identical content models or copy the first course's methods into the repository definition.

### 2. Course-Instance Separation Pattern

**Pattern summary:** Shared workflow and tooling are separated from each course, cohort, semester, or delivery instance.

**Typical structure:** A governed root plus one directory per course; optional instance directories for terms, cohorts, instructors, schedules, local assessments, and delivery records.

**Strengths:** Clear ownership, reduced cross-course contamination, support for repeated delivery, and safer comparison between stable course design and term-specific execution.

**Risks:** Duplication between instances, unclear promotion rules, and accidental inheritance of outdated materials.

**Fit for lesson_prep_workflow:** Very strong fit. The existing `COURSES/` boundary and per-course SOT/state/index model should be retained.

**What to borrow / what not to borrow:** Borrow an explicit course-instance or semester-instance layer when repeated delivery begins, with provenance back to the governing course. Do not create speculative instance directories before a real delivery requires them, and do not permit instance material to silently overwrite the course SOT.

### 3. Docs-As-Code Curriculum Workflow

**Pattern summary:** Curriculum artifacts are maintained as versioned text, reviewed through task and change controls, and validated with lightweight automation.

**Typical structure:** Markdown source, structured metadata, review contracts, changelog, issue or task records, validation scripts, and optional static-site output.

**Strengths:** Auditable history, readable diffs, reproducible review, tool portability, and compatibility with Git-based collaboration.

**Risks:** Process overhead, inaccessible authoring for some contributors, false confidence from syntactic validation, and premature build-pipeline complexity.

**Fit for lesson_prep_workflow:** Strong fit. The repository already uses Markdown governance, JSON state, task cards, indexes, and closeouts.

**What to borrow / what not to borrow:** Borrow small validation commands, explicit review evidence, and consistent state transitions. Do not treat a passing build as proof of source reliability, teaching quality, copyright clearance, or assessment validity.

### 4. Assessment/Question-Bank Separation Pattern

**Pattern summary:** Reusable assessment items and question banks are governed separately from lesson narratives, student-facing tasks, and a particular delivery's assembled assessment.

**Typical structure:** Item bank with identifiers, learning targets, source provenance, difficulty or cognitive level, answer/rubric data, review state, exposure controls, and links to assembled assessments.

**Strengths:** Reuse with traceability, controlled item revision, clearer assessment suitability review, and reduced coupling between teaching sequence and evaluation inventory.

**Risks:** Item leakage, licensing or source ambiguity, over-reuse, teaching to a static bank, and uncontrolled copying of answer material.

**Fit for lesson_prep_workflow:** Good future fit, provided it remains behind the source, maturity, and assessment-suitability gates.

**What to borrow / what not to borrow:** Borrow a formal boundary between assessment-bank records and lesson artifacts, stable item identifiers, provenance, and review status. Do not build automated scoring, expose restricted answers publicly, or allow an item bank to become an unaudited source repository.

### 5. LMS/Export-Ready Markdown Source Pattern

**Pattern summary:** Platform-neutral Markdown is treated as the primary source and transformed into LMS imports, static sites, PDFs, or other delivery formats.

**Typical structure:** Canonical Markdown, front matter or structured metadata, asset directories, export profiles, and generated output excluded or clearly separated from source.

**Strengths:** Portability, readable canonical files, reduced platform lock-in, and the possibility of multiple output formats.

**Risks:** Lowest-common-denominator formatting, platform-specific metadata creep, fragile converters, accessibility regressions, and confusion between source and generated output.

**Fit for lesson_prep_workflow:** Partial fit. Markdown should remain a preferred portable source format, but no LMS integration is currently justified.

**What to borrow / what not to borrow:** Borrow clean Markdown, stable metadata fields where needed, and a strict source-versus-generated-artifact boundary. Do not implement LMS adapters, export pipelines, or platform-specific schemas until an authorized delivery requirement exists.

### 6. Governance-Heavy Public Repo Hygiene Pattern

**Pattern summary:** Public-facing curriculum repositories define publication boundaries, contribution rules, source provenance, licensing, sensitive-material handling, and pre-publication checks.

**Typical structure:** Governance and contribution documents, license and attribution records, source inventory, publication checklist, redaction or exclusion rules, and release records.

**Strengths:** Lower copyright and privacy risk, clearer contributor expectations, stronger provenance, and safer public collaboration.

**Risks:** Administrative load, checklist compliance without substantive review, and accidental publication when local/private boundaries are unclear.

**Fit for lesson_prep_workflow:** Essential if GitHub publication proceeds. Existing governance and publication protocols provide a sound base.

**What to borrow / what not to borrow:** Borrow a mandatory pre-publication copyright and source-material cleanup review, explicit exclusions, and recorded authorization. Do not assume that public availability elsewhere grants reuse rights or that attribution alone resolves copyright restrictions.

## Architecture Recommendations

### A. Immediately Keep

1. Keep the current uppercase top-level structure: `GOVERNANCE/`, `COURSES/`, `SHARED/`, `SKILLS/`, `TASK_CARDS/`, and `CLOSEOUTS/`.
2. Keep repository governance separate from course governance and preserve per-course SOT, plan/state, and task index ownership.
3. Keep fail-closed handling for unknown authority, provenance, copyright, task state, active course, and cross-repository permission.
4. Keep NotebookLM output classified as raw input rather than approved material.
5. Keep Markdown and small structured state files as the canonical docs-as-code foundation.
6. Keep publication authorization separate from curriculum development.

The existing architecture is broadly suitable and should not be reorganized wholesale.

### B. Strengthen Next

1. Add an external-source audit table that records identity, locator, access conditions, rights boundary, reliability rationale, intended use, reviewer decision, and unresolved issues.
2. Add a NotebookLM output review record that links generated claims or excerpts back to auditable sources and records acceptance, rejection, correction, or `needs human review`.
3. Define a course-instance or semester-instance layer for actual repeated deliveries, including inheritance, local overrides, archival, and promotion-back rules.
4. Define the boundary between an assessment bank and lesson artifacts, including item identifiers, provenance, answer/rubric access, exposure state, and suitability review.
5. Strengthen the public GitHub pre-publication gate with copyright review, restricted-source removal, NotebookLM-output removal or approval, secret/privacy checks, and a generated-artifact inventory.

### C. Do Not Build Yet

1. LMS platform integration.
2. Automated grading systems.
3. A large frontend curriculum platform.
4. Student account or identity systems.
5. Production-grade AI applications.

These systems add operational, privacy, security, maintenance, and platform-coupling burdens before the repository's source and review contracts are mature enough to justify them.

### D. Candidate Follow-Up Tasks

1. `TASK-LPW-GOV-003 | Architecture Hardening Patch`: incorporate the accepted recommendations into repository contracts and templates without restructuring the repository.
2. `TASK-LPW-GOV-004 | Prompt Governance And NotebookLM Intake Contract`: formalize generated-output intake, source traceability, review decisions, and fail-closed handling.
3. Add an external source-audit table template and review instructions under an authorized governance task.
4. Add a course-instance/semester-instance contract only when a real delivery use case can validate the design.
5. Add an assessment-bank boundary contract and minimal metadata schema before any reusable question bank is populated.
6. Add a public-release checklist that operationalizes `GOVERNANCE/GITHUB_PUBLICATION_PROTOCOL.md`.

## Decision

Retain the current repository architecture. Apply incremental governance hardening through existing task controls. External GitHub repositories remain pattern references only; no surveyed repository or its contents are promoted into course materials by this decision.
