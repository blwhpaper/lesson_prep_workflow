# Classical Chinese Task Registry

| task | category | status | purpose | dependency |
|---|---|---|---|---|
| TASK-CLCH-GOV-000 | governance | completed | register course roadmap, numbering, and anti-drift shell | repository governance protocols |
| TASK-CLCH-GOV-001 | governance | pending | bootstrap course boundary, scope, and non-goals | TASK-CLCH-GOV-000 |
| TASK-CLCH-GOV-002 | governance | planned | define NotebookLM intake, source package, and citation boundary | TASK-CLCH-GOV-001 |
| TASK-CLCH-GOV-003 | governance | planned | define cross-agent entry protocol for this course line | TASK-CLCH-GOV-002 |
| TASK-CLCH-GOV-004 | governance | planned | define artifact maturity and export contract for this course | TASK-CLCH-GOV-003 |
| TASK-CLCH-MAT-001 | material | planned | extract knowledge map from governed source scope | TASK-CLCH-GOV-004 |
| TASK-CLCH-MAT-002 | material | planned | build 16-week core material matrix at non-lesson level | TASK-CLCH-MAT-001 |
| TASK-CLCH-MAT-003 | material | planned | map textbooks and themes with traceable source slots | TASK-CLCH-MAT-002 |
| TASK-CLCH-PROMPT-001 | prompt | planned | define student CNKI prompt assignment contract | TASK-CLCH-MAT-003 |
| TASK-CLCH-LESSON-001 | lesson design | planned | draft Week 1 lesson skeleton only after materials mature | TASK-CLCH-PROMPT-001 |
| TASK-CLCH-ASSESS-001 | assessment | planned | define assessment and rubric boundary | TASK-CLCH-LESSON-001 |
| TASK-CLCH-EXPORT-001 | export | planned | define export packaging and release rules | TASK-CLCH-ASSESS-001 |

## Registry Rules

1. `TASK-CLCH-GOV-*` is for governance shell, boundary, protocol, and maturity control.
2. `TASK-CLCH-MAT-*` is for source intake, mapping, extraction, and course-core material preparation.
3. `TASK-CLCH-PROMPT-*` is for prompt contracts only, never direct teaching artifacts.
4. `TASK-CLCH-LESSON-*` begins only after the material route is mature enough for lesson use.
5. `TASK-CLCH-ASSESS-*` must not rely on material below the repository threshold for assessment use.
6. `TASK-CLCH-EXPORT-*` is last because publication and packaging are downstream of maturity and review.
