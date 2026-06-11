# NotebookLM Workflow Protocol

NotebookLM may support source indexing, knowledge maps, candidate material extraction, and summaries for different courses. Its output is always raw output, never formal course material.

Each course may keep prompts in `NOTEBOOKLM/PROMPTS/` and raw output in `NOTEBOOKLM/OUTPUTS/`. Prompts and outputs must be saved in those locations before review.

Every saved NotebookLM output must be labeled `draft`, `extracted`, or `unverified`. It must not be relabeled as source-audited, course-core, lesson-ready, or assessment-ready by implication.

Before output enters a material database, review:

1. source and locator accuracy;
2. reliability grade;
3. course adaptation;
4. closed-book assessment suitability;
5. AI-task suitability.

Do not generate a lesson plan directly from NotebookLM output. Do not copy output directly into a question bank. Missing source, page, chapter, or example provenance must be marked `需人工复核`.

The material maturity chain `L0 -> L1 -> L2 -> L3 -> L4 -> L5` is mandatory for course use, and NotebookLM output may enter only at `L0` or `L1`.
