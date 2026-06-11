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

For `COURSES/classical_chinese`, source authority and copyright review must also preserve:

- source-authority level;
- locator metadata such as chapter, section, page, or equivalent location;
- extraction method and review status;
- copyright risk and classroom-use scope;
- draft labeling for any AI-generated derivative artifact.

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
  - `TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course`
  - `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary`
  - `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract`
  - `TASK-CLCH-MAT-001 | Knowledge Map Extraction`
  - `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix`
  - only then may teaching-design tasks begin
- AI/vibecoding belongs only to the method layer for this course line and must not replace Ancient Chinese knowledge ontology.

## Classical Chinese Cross-Agent Entry Rule

When the operator says `TASK-CLCH-XXX 开工`, the active agent must use the Classical Chinese entry protocol rather than a generic whole-repository scan.

- Minimum read order:
  - `AGENTS.md`
  - `LESSON_PREP_WORKFLOW_SOT.md`
  - `GOVERNANCE/PLAN.md`
  - `GOVERNANCE/TASK_STATE.json`
  - `GOVERNANCE/TASK_INDEX.md`
  - `GOVERNANCE/CHANGE_LOG.md`
  - `docs/OPERATOR_GUIDE.md`
  - `COURSES/classical_chinese/COURSE_BOUNDARY.md`
  - `COURSES/classical_chinese/ROADMAP.md`
  - `COURSES/classical_chinese/TASK_REGISTRY.md`
  - the current `TASK-CLCH-*` card
  - the previous closeout
  - `git status --short --branch`
- Fail closed when the task id, current branch, `TASK_STATE`, roadmap, or registry does not align.
- Normalize the requested task into a task family before acting:
  - `TASK-CLCH-GOV-*` = governance-only boundary, routing, protocol, index, or agent-constraint work
  - `TASK-CLCH-MAT-*` = material extraction and material mapping below lesson level
  - `TASK-CLCH-PROMPT-*` = prompt-pack and extraction-prompt workflow work
  - `TASK-CLCH-LESSON-*` = lesson design and PPT-structure work for specific lessons or units
  - `TASK-CLCH-ASSESS-*` = homework, quiz, rubric, and evaluation design
  - `TASK-CLCH-REVIEW-*` = review, retrospective, and audit work
- Use `task-clch-<type>-<number>-<kebab-title>` for Classical Chinese task branches.
- Use `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md` for Classical Chinese task-card and governance filenames.
- Use `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md` for Classical Chinese closeouts.
- Do not drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`.
- Do not generate lesson plans, slides, question banks, papers, or formal classroom materials during governance-only tasks.
- Do not generate a full course, full PPT set, or full question bank unless the active task family and task card explicitly authorize that scope.
- Textbook packages by Wang Li, Guo Xiliang, Qiu Xigui, and related authors remain governed source inputs only and may not be reproduced in long copyrighted form.
- For this course line, source-authority governance must use the ladder `L0 repo governance SoT -> L1 course boundary / roadmap / registry -> L2 textbook or reference corpus metadata -> L3 NotebookLM extraction notes -> L4 agent-generated summaries / matrices / drafts -> L5 classroom-facing deliverables`.
- If source identity, locator metadata, copyright risk, or publication scope is unclear, fail closed and keep the artifact at summary, index, or draft level only.
- Keep task pointers aligned across `TASK_REGISTRY`, `ROADMAP`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG`.
