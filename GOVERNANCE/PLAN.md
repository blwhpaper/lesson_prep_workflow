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

`TASK-CLCH-GOV-000` completed -> `TASK-CLCH-GOV-001 | Classical Chinese Course Boundary Bootstrap` completed -> `TASK-CLCH-GOV-002 | Cross-Agent Entry Protocol For Classical Chinese Course` completed -> `TASK-CLCH-GOV-003 | Classical Chinese Source Authority And Copyright Boundary` completed -> `TASK-CLCH-GOV-004 | Task Routing And Naming Convention Contract` completed -> `TASK-CLCH-GOV-005 | Merge Legacy Classical Chinese Translation Route Into Formal Course Route` completed -> `TASK-CLCH-MAT-001 | Knowledge Map Extraction` completed -> `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix` completed -> `TASK-CLCH-GOV-SKILL-001 | Classical Chinese Course Agent Skill And Fail-Closed Audit` completed -> `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` next -> `TASK-CLCH-LESSON-002 | Unit Template And Lesson Design Contract` planned -> `TASK-CLCH-PROMPT-001 | NotebookLM And Agent Prompt Pack Contract` planned -> `TASK-CLCH-ASSESS-001 | Assessment And Assignment Framework` planned -> `TASK-CLCH-REVIEW-001 | Course Retrospective And Quality Review` planned

No formal lesson production has begun for `classical_chinese`.

NotebookLM output for this course line must pass intake and citation-boundary controls before entering the material route, and the material route must produce a `16-session core material matrix` before teaching design begins.

`TASK-CLCH-GOV-002` is governance-only. It standardizes the entry contract for Codex, Cursor, Antigravity, Claude, Gemini, and similar agents, and it does not authorize lesson drafting or material extraction.

`TASK-CLCH-GOV-003` is governance-only. It defines the Classical Chinese source-authority ladder, mandatory source fields, NotebookLM non-substitution rule, copyright boundary, and fail-closed promotion limits for future source-derived artifacts.

`TASK-CLCH-GOV-004` is governance-only. It defines the Classical Chinese task-family routing contract, branch and filename conventions, anti-drift naming rules, and cross-file pointer consistency rules. The next task after it is `TASK-CLCH-MAT-001 | Knowledge Map Extraction`.

`TASK-CLCH-GOV-005` is governance-only. It merges the retired standalone `classical_chinese_translation` route into `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`, preserves the legacy files without promoting their governance state, removes the duplicate top-level course entry, and keeps `TASK-CLCH-MAT-001 | Knowledge Map Extraction` as the next task.

`TASK-CLCH-GOV-SKILL-001` is governance-only. It inserts a governed agent skill and fail-closed audit checkpoint between `TASK-CLCH-MAT-002` and `TASK-CLCH-LESSON-001`, registers the task inside the route pointers, and adds the reusable Classical Chinese audit checklist without authorizing lesson drafting.
