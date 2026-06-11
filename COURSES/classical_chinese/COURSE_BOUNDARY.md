# Classical Chinese Course Boundary

## course_identity

- course code: `CLCH`
- course line: `classical_chinese`
- course title: `Classical Chinese For Translation Studies And Practice`
- course object: translation-major undergraduates
- course format: 16 weeks, 2 class hours per week
- course goal: build foundational Ancient Chinese competence that supports translation studies and translation practice
- current stage: governance boundary bootstrap only
- current stage detail: cross-agent entry governance is required before source-authority governance and before material extraction

## learner_profile

- learners are undergraduate translation majors rather than pure philology specialists
- the course serves reading, interpretation, terminology awareness, and translation-relevant language analysis
- disciplinary depth must support translation understanding without drifting into a full specialist ancient-philology sequence
- later assignments may connect to translation research and practice, but this task does not design those assignments

## source_boundary

- governed source package for future intake is limited to the user-uploaded NotebookLM corpus:
  - Wang Li, `古代汉语` four volumes
  - `古代汉语常识`
  - Guo Xiliang, `古代汉语` two volumes
  - `古代汉语语法讲稿`
  - Qiu Xigui, `文字学概要`
- the existence of these uploads authorizes only boundary-setting in this task, not content extraction claims
- no course content may be supplemented from memory, generic internet summaries, or undeclared external repositories
- later source extraction must remain traceable by work unit, source identity, and locator metadata
- agents must not ask for or reproduce long copyrighted passages from these works

## cross_agent_entry_boundary

- the operator start phrase for this course line is `TASK-CLCH-XXX 开工`
- the required entry header is:
  - course code `CLCH`
  - course line `classical_chinese`
  - active task family `TASK-CLCH-*`
  - governance-only mode unless the active task card authorizes a later stage
  - fail-closed default `true`
- the minimum read order is:
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
  - the current task card
  - the previous closeout
  - `git status --short --branch`
- token-saving rule:
  - read only the files required for the active `TASK-CLCH-*`
  - do not scan the whole repository
  - do not read another course line unless a task card explicitly authorizes it
- forbidden drift targets:
  - `BTC_WATCHFLOW`
  - `NESP`
  - `Lin Yutang paper`
  - `Thesis_Format_Fixer`
  - `daily-review`
- required response footer:
  - current branch
  - changed files
  - protocol summary
  - acceptance-command results
  - risks or unfinished items

## NotebookLM_boundary

- NotebookLM output is raw intake support only
- this task does not claim that NotebookLM extraction has been completed
- this task does not create or simulate NotebookLM output
- future NotebookLM work must first support:
  - `TASK-CLCH-MAT-001 | Knowledge Map Extraction`
  - `TASK-CLCH-MAT-002 | 16-Session Core Material Matrix`
- the required downstream sequence is:
  - user-uploaded source package
  - NotebookLM-assisted extraction
  - `16-session core material matrix`
  - human review and maturity promotion
  - teaching design
- no agent may jump directly from NotebookLM output to 16-week lesson design

## AI_vibecoding_boundary

- AI and vibecoding belong only to the method layer of this course line
- they may later support research prompting, comparison, workflow reflection, and guided learning activities
- they must not replace Ancient Chinese knowledge ontology, textual interpretation, lexicon, grammar, phonology, exegetical awareness, or source reading
- later student activities may include topic-based prompt writing for CNKI exploration, but that belongs to downstream teaching-activity design and is not expanded in this task

## copyright_boundary

- this stage must not reproduce or publish long textbook passages
- textbook uploads authorize governed private extraction workflow only; they do not authorize public redistribution
- any future excerpt must remain short, traceable, and justified by the relevant task boundary
- unauthorized full-text reuse, scan redistribution, or implicit reconstruction of textbook chapters is forbidden

## output_maturity_boundary

- current task outputs are governance artifacts only
- course content maturity has not advanced through source audit, reliability grading, course adaptation, or assessment suitability review
- no artifact produced here may be labeled lesson-ready, assessment-ready, or publication-ready
- the next mature output target is not a lesson plan; it is a governed knowledge map and then a `16-session core material matrix`
- governance tasks must not generate lesson plans, slides, question banks, papers, or formal classroom materials

## fail_closed_rules

- fail closed and record `needs human review` when any of the following is unknown or conflicting:
  - active `TASK-CLCH-*` authorization
  - exact source package or source locator boundary
  - whether NotebookLM output exists, what it contains, or whether it has been reviewed
  - whether a requested output belongs to governance, material, design, or assessment stage
  - whether an AI/vibecoding activity is method-layer support or an improper content substitute
  - whether copyright or publication permission covers the requested excerpt or export
- when fail-closed triggers occur, preserve the artifact at governance or draft level and do not promote downstream use
- when `TASK_STATE`, `ROADMAP`, `TASK_REGISTRY`, the requested `TASK-CLCH-*`, or the current branch conflict, stop immediately and report `needs human review`

## forbidden_outputs

- formal 16-week lesson-plan prose
- lecture slides or slide outlines
- student worksheet detail
- assignment detail or answer keys
- question bank items
- direct NotebookLM excerpt bodies
- long textbook quotations
- fabricated claims that knowledge extraction is already complete
- AI/vibecoding-centered syllabus that sidelines Ancient Chinese core knowledge
- cross-project governance or content drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`

## allowed_next_outputs

- governed task cards and governance records
- knowledge-map extraction contract
- `16-session core material matrix` contract
- unit-architecture and lesson-design contracts after material maturity gates are satisfied
- AI/vibecoding learning-activity boundary document as a downstream method-layer task
- assessment and assignment framework after design-stage prerequisites are met
