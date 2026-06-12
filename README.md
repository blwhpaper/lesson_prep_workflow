# Lesson Prep Workflow

A reusable, course-agnostic repository for governed lesson preparation. It separates repository governance, course instances, shared templates, source review, material maturity, lesson design, and assessment design.

Start with `AGENTS.md`, then follow the declared source-of-truth chain. The first registered course is `classical_chinese_translation`; it is an instance, not the definition of the repository.

No course artifact may bypass source and maturity gates. Sensitive source files and unreviewed NotebookLM outputs stay local or private.

The current repository governance patch is `TASK-LPW-GOV-005 | Repository Local Path Migration To KIOXIA Root`. The default local working path is `/Volumes/KIOXIA_1TB/lesson_prep_workflow`. Prompts are input contracts only and never formal lesson artifacts. NotebookLM output remains `draft` / `extracted` / `unverified` until formal review promotes it through the maturity model. Public publication must exclude copyrighted textbook full text, unauthorized scans, student privacy, internal sensitive material, and unverified NotebookLM output.

The repository also registers `TASK-CLCH-GOV-000 | Classical Chinese Course Roadmap And Task Registry` as a governance-only shell for a separate `COURSES/classical_chinese` line. That route remains pre-lesson and may not bypass NotebookLM intake, source audit, or maturity gates.
