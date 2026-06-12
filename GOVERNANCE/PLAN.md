# Repository Governance Plan

1. `TASK-LPW-GOV-001` | Lesson Prep Workflow Repository Bootstrap | in progress
2. `TASK-LPW-GOV-002` | GitHub Curriculum Pattern Survey And Architecture Recommendations | completed
3. `TASK-LPW-GOV-003` | Architecture Hardening Patch | completed
4. `TASK-LPW-GOV-004` | Prompt Governance And NotebookLM Intake Contract | completed
5. `TASK-LPW-GOV-005` | Repository Local Path Migration To KIOXIA Root | completed
6. `TASK-LPW-GOV-006` | Course Expansion Protocol Dry Run | not started

`TASK-LPW-GOV-*` governs the repository. `TASK-CLCH-*` belongs to the current course instance. `TASK-LPW-GOV-001` creates shells only and does not advance any `TASK-CLCH-*` task.

The governance route is:

`TASK-LPW-GOV-002` completed -> `TASK-LPW-GOV-003 | Architecture Hardening Patch` completed -> `TASK-LPW-GOV-004 | Prompt Governance And NotebookLM Intake Contract` completed -> `TASK-LPW-GOV-005 | Repository Local Path Migration To KIOXIA Root` completed.

`TASK-LPW-GOV-003` hardens governance architecture only. It does not advance a course task or change the active course.

`TASK-LPW-GOV-005` is governance-only. It records the completed local repository path migration to `/Volumes/KIOXIA_1TB/lesson_prep_workflow`, keeps the git remote pointed at the GitHub repository, and does not advance course content by itself.

## Classical Chinese Course Line

`TASK-CLCH-GOV-000 | Classical Chinese Course Roadmap And Task Registry` is completed as a course-governance shell for `COURSES/classical_chinese`.

This route is the only formal Classical Chinese route. The former standalone `COURSES/classical_chinese_translation` line is retired and preserved only as `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` for audit-only legacy reference.

Current course-line route:

`TASK-CLCH-GOV-000` completed -> `TASK-CLCH-GOV-001 | Classical Chinese Course Boundary Bootstrap` completed -> `TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course` completed -> `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary` completed -> `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract` completed -> `TASK-CLCH-GOV-005 | Merge Legacy Classical Chinese Translation Route Into Formal Course Route` completed -> `TASK-CLCH-MAT-001 | Knowledge Map Extraction` completed -> `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` completed -> `TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit` completed -> `TASK-CLCH-GOV-006 | Classical Chinese Course Downstream Task Roadmap Hardening` completed -> `TASK-CLCH-GOV-007 | Downstream Task Sequence Optimization And Competency Matrix Boundary Patch` completed -> `TASK-CLCH-GOV-008 | Downstream Task Registry Realignment To Four-Batch Lesson Build Plan` completed -> `TASK-CLCH-LESSON-001 | 16-Week Course Architecture And Competency Matrix Boundary` completed -> `TASK-CLCH-PROMPT-001 | NotebookLM Extraction Prompt Pack` next -> `TASK-CLCH-LESSON-002 | Session Package Template, Source Evidence Contract And Build Standard` pending -> `TASK-CLCH-ASSESS-001 | Assessment Framework And Translation Practice Rubrics` pending -> `TASK-CLCH-AI-001 | Student AI/Vibecoding Activity Protocol` pending -> `TASK-CLCH-LESSON-003 | Week 1-4 Lesson Package Build` pending -> `TASK-CLCH-LESSON-004 | Week 5-8 Lesson Package Build` pending -> `TASK-CLCH-LESSON-005 | Week 9-12 Lesson Package Build` pending -> `TASK-CLCH-LESSON-006 | Week 13-16 Lesson Package Build` pending -> `TASK-CLCH-REVIEW-001 | Course Delivery Review, Source Evidence Audit And Fail-Closed Check` pending

`TASK-CLCH-LESSON-001` is a lesson-family task with an architecture-only boundary. It creates the 16-week course architecture, unit grouping, progression logic, and competency matrix boundary, but it does not authorize session package prose, assignments, PPT bodies, or classroom-facing translation materials.

No formal lesson production has begun for `classical_chinese`.

NotebookLM output for this course line must pass intake and citation-boundary controls before entering the material route, and the material route must produce a `16-session core material matrix` before teaching design begins.

`TASK-CLCH-GOV-002` is governance-only. It standardizes the entry contract for Codex, Cursor, Antigravity, Claude, Gemini, and similar agents, and it does not authorize lesson drafting or material extraction.

`TASK-CLCH-GOV-003` is governance-only. It defines the Classical Chinese source-authority ladder, mandatory source fields, NotebookLM non-substitution rule, copyright boundary, and fail-closed promotion limits for future source-derived artifacts.

`TASK-CLCH-GOV-004` is governance-only. It defines the Classical Chinese task-family routing contract, branch and filename conventions, anti-drift naming rules, and cross-file pointer consistency rules. The next task after it is `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.

`TASK-CLCH-GOV-005` is governance-only. It merges the retired standalone `classical_chinese_translation` route into `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`, preserves the legacy files without promoting their governance state, removes the duplicate top-level course entry, and keeps `TASK-CLCH-MAT-001 | Knowledge Map Extraction` as the next task.

`TASK-CLCH-GOV-SKILL-001` is governance-only. It inserts a governed agent skill and fail-closed audit checkpoint between `TASK-CLCH-MAT-002` and `TASK-CLCH-LESSON-001`, registers the task inside the route pointers, and adds the reusable Classical Chinese audit checklist without authorizing lesson drafting.

`TASK-CLCH-GOV-006` is governance-only. It hardens the downstream task roadmap after `TASK-CLCH-LESSON-001`, defines the sequence and boundaries for lesson, assessment, AI-activity, prompt, and review tasks, and does not authorize 16-week lesson prose or package drafting by itself.

`TASK-CLCH-GOV-007` is governance-only. It optimizes the downstream execution order created by `TASK-CLCH-GOV-006`, inserts the competency matrix as a mandatory pre-generation boundary and acceptance layer, and keeps `TASK-CLCH-LESSON-001` architecture-only without authorizing lesson-body prose, PPT bodies, question banks, or classroom-facing translation material.

`TASK-CLCH-GOV-008` is governance-only. It supersedes the GOV-007 downstream mainline with the four-batch lesson build route, folds competency, source evidence, workflow, QA, and delivery-plan governance into the revised downstream chain, and keeps `TASK-CLCH-LESSON-001` architecture-and-competency-boundary-only without authorizing lesson-body prose, PPT bodies, question banks, or classroom-facing translation material.
