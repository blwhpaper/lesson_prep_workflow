# Classical Chinese Task Registry

| task | category | status | purpose | allowed_outputs | blocked_outputs |
|---|---|---|---|---|---|
| `TASK-CLCH-GOV-000` | governance | completed | register the standalone course line, roadmap shell, and anti-drift numbering | roadmap shell, task family definitions, governance boundary seed | lessons, slides, source promotion |
| `TASK-CLCH-GOV-001` | governance | completed | bootstrap course boundary, learner target, source boundary, maturity boundary, and non-goals | boundary contract, entry rules, forbidden-output list, next-task route | textbook excerpts, lesson prose, assignment details |
| `TASK-CLCH-GOV-002` | governance | completed | establish the cross-agent entry protocol for `TASK-CLCH-XXX 开工` execution | entry protocol, minimum read order, anti-drift rules, fail-closed checks, response footer contract | lessons, slides, question banks, papers, textbook copying |
| `TASK-CLCH-GOV-003` | governance | completed | define source-authority and copyright boundary rules before material extraction | source-authority contract, copyright boundary, locator and excerpt rules, review preconditions, mandatory source fields | lesson plans, full-text copying, material promotion without review |
| `TASK-CLCH-GOV-004` | governance | next | align task routing and naming conventions before material and design families expand | task-routing contract, naming rules, route-validation rules, task-family normalization | lesson plans, material extraction, design outputs without routing alignment |
| `TASK-CLCH-MAT-001` | material | planned | extract a governed knowledge map from the authorized source package | knowledge map, topic clusters, source-slot map, unresolved-review flags | lesson plans, weekly scripts, assessment items |
| `TASK-CLCH-MAT-002` | material | planned | produce the `16-session core material matrix` before teaching design begins | 16-session core material matrix, session-level material coverage, maturity notes | lesson-plan prose, slides, worksheets |
| `TASK-CLCH-DES-001` | design | planned | convert mature material structure into a 16-week course architecture | 16-week architecture, unit grouping, progression logic, teaching-phase map | textbook copying, question banks, full lesson scripts |
| `TASK-CLCH-DES-002` | design | planned | define the unit template and lesson design contract for later lesson drafting | lesson-design template, lesson contract, required input schema, output limits | finished 16-week lesson set, slide deck, assignment answer key |
| `TASK-CLCH-AI-001` | AI/method | planned | define the boundary for AI and vibecoding as method-layer support only | AI activity boundary, permitted method use, forbidden substitution rules, downstream activity hooks | AI-centered content ontology, replacement of Ancient Chinese knowledge core |
| `TASK-CLCH-ASSESS-001` | assessment | planned | define the assessment and assignment framework after design-stage prerequisites are met | assessment framework, assignment categories, rubric boundary, maturity preconditions | full question bank, answer bank, unaudited take-home tasks |

## Registry Rules

1. `TASK-CLCH-GOV-*` controls boundary, routing, and anti-drift governance only.
2. `TASK-CLCH-GOV-002` is the mandatory cross-agent start layer for this course line.
3. `TASK-CLCH-GOV-003` establishes the source-authority ladder `L0 -> L5`, mandatory source fields, NotebookLM non-substitution rule, and copyright boundary for this course line.
4. `TASK-CLCH-GOV-004` must complete before `TASK-CLCH-MAT-001` may begin.
5. `TASK-CLCH-MAT-*` may structure source-derived course material below lesson level, but may not generate formal lesson artifacts.
6. `TASK-CLCH-DES-*` may shape teaching architecture only after the `16-session core material matrix` exists.
7. `TASK-CLCH-AI-*` belongs to pedagogy and workflow method, never to disciplinary content substitution.
8. `TASK-CLCH-ASSESS-*` begins only after content and design boundaries are stable enough for assignment suitability review.
