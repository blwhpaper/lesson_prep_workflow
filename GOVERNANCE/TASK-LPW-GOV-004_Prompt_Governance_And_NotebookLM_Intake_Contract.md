# TASK-LPW-GOV-004 Prompt Governance And NotebookLM Intake Contract

## Purpose

This contract governs prompts, NotebookLM intake, NotebookLM output review, maturity labels, publication limits, and agent execution boundaries. It does not authorize lesson production or course-content generation.

## Prompt Contract

- A prompt is an input contract or working instruction for an agent, NotebookLM, or a human operator.
- A prompt is not a lesson plan, textbook, question bank, answer key, course outcome, or approved teaching artifact.
- Every reusable prompt template must declare:
  - `purpose`
  - `source_scope`
  - `forbidden_inputs`
  - `expected_output`
  - `maturity_label`
  - `review_gate`
  - `publication_boundary`
- Prompt records must state their intended tool or human workflow and must not imply source authority.

## NotebookLM Intake Contract

Every NotebookLM intake saved to the repository must record:

- source package or source bundle identity
- included input scope
- excluded input scope
- copyright status
- whether student privacy is present
- whether unauthorized textbook full text is present
- whether public release is allowed

NotebookLM output defaults to `draft`, `extracted`, and `unverified`. It may not be treated as `verified`, `reusable`, `publishable`, `source-audited`, `lesson-ready`, or `assessment-ready` by implication.

## Required Review Gate

Before NotebookLM-derived output enters the repository for governed reuse or promotion, review must record:

1. source check
2. copyright check
3. privacy check
4. pedagogical fit check
5. human promotion decision

If any gate fails or remains unknown, the artifact stays at its current level and is marked `needs human review`.

## Publication Boundary

- Do not publish copyrighted textbook full text.
- Do not publish scans, OCR dumps, or other unauthorized reproductions.
- Do not publish student personal information.
- Do not publish internal sensitive material.
- Do not publish unverified NotebookLM output.
- Do not publish prompts or outputs whose source boundary, use boundary, or maturity boundary is unclear.

## Agent-Executable Boundary

- Agents may create or revise governance contracts, templates, and review records.
- Agents may not promote NotebookLM output without recorded human review.
- Agents may not convert prompt text into approved course material by assertion alone.
- Agents must fail closed when source, copyright, privacy, output use, or publication authorization is unknown.

## Non-Goals

- No course lesson content
- No course prompt set
- No direct material-database promotion
- No GitHub publication action
