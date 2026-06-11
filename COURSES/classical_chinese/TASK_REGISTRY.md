# Classical Chinese Task Registry

| task | category | status | purpose | allowed_outputs | blocked_outputs |
|---|---|---|---|---|---|
| `TASK-CLCH-GOV-000` | governance | completed | register the standalone course line, roadmap shell, and anti-drift numbering | roadmap shell, task family definitions, governance boundary seed | lessons, slides, source promotion |
| `TASK-CLCH-GOV-001` | governance | completed | bootstrap course boundary, learner target, source boundary, maturity boundary, and non-goals | boundary contract, entry rules, forbidden-output list, next-task route | textbook excerpts, lesson prose, assignment details |
| `TASK-CLCH-GOV-002` | governance | completed | establish the cross-agent entry protocol for `TASK-CLCH-XXX 开工` execution | entry protocol, minimum read order, anti-drift rules, fail-closed checks, response footer contract | lessons, slides, question banks, papers, textbook copying |
| `TASK-CLCH-GOV-003` | governance | completed | define source-authority and copyright boundary rules before material extraction | source-authority contract, copyright boundary, locator and excerpt rules, review preconditions, mandatory source fields | lesson plans, full-text copying, material promotion without review |
| `TASK-CLCH-GOV-004` | governance | completed | align task routing and naming conventions before material and downstream families expand | task-routing contract, naming rules, route-validation rules, task-family normalization | lesson plans, material extraction, design outputs without routing alignment |
| `TASK-CLCH-MAT-001` | material | next | extract a governed knowledge map from the authorized source package | knowledge map, topic clusters, source-slot map, unresolved-review flags | lesson plans, weekly scripts, assessment items |
| `TASK-CLCH-MAT-002` | material | planned | produce the `16-session core material matrix` before teaching design begins | 16-session core material matrix, session-level material coverage, maturity notes | lesson-plan prose, slides, worksheets |
| `TASK-CLCH-PROMPT-001` | prompt | planned | define the NotebookLM and multi-agent prompt-pack contract for governed extraction and review | prompt contract, prompt metadata, extraction template, review prompt schema | prompt-only promotion into approved classroom prose |
| `TASK-CLCH-LESSON-001` | lesson | planned | convert mature material structure into a 16-week course architecture | 16-week architecture, unit grouping, progression logic, teaching-phase map | textbook copying, question banks, full lesson scripts |
| `TASK-CLCH-LESSON-002` | lesson | planned | define the unit template and lesson design contract for later lesson drafting | lesson-design template, lesson contract, required input schema, output limits | finished 16-week lesson set, slide deck, assignment answer key |
| `TASK-CLCH-ASSESS-001` | assessment | planned | define the assessment and assignment framework after design-stage prerequisites are met | assessment framework, assignment categories, rubric boundary, maturity preconditions | full question bank, answer bank, unaudited take-home tasks |
| `TASK-CLCH-REVIEW-001` | review | planned | define the course retrospective and quality-review route once governed artifacts exist | route audit, quality review checklist, version review notes, risk summary | free-form scope changes without governed pointer updates |

## Registry Rules

1. `TASK-CLCH-GOV-*` controls boundary, routing, and anti-drift governance only.
2. `TASK-CLCH-GOV-002` is the mandatory cross-agent start layer for this course line.
3. `TASK-CLCH-GOV-003` establishes the source-authority ladder `L0 -> L5`, mandatory source fields, NotebookLM non-substitution rule, and copyright boundary for this course line.
4. `TASK-CLCH-GOV-004` must complete before `TASK-CLCH-MAT-001` may begin.
5. `TASK-CLCH-MAT-*` may structure source-derived course material below lesson level, but may not generate formal lesson artifacts.
6. `TASK-CLCH-PROMPT-*` may define prompt packs and extraction workflows, but prompts alone may not become approved teaching prose.
7. `TASK-CLCH-LESSON-*` may shape teaching architecture only after the `16-session core material matrix` exists and lesson-stage authorization is explicit.
8. `TASK-CLCH-ASSESS-*` begins only after content and lesson-design boundaries are stable enough for assignment suitability review.
9. `TASK-CLCH-REVIEW-*` audits governed artifacts and must not silently rewrite route state without updating the canonical pointers.
