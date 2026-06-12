# Classical Chinese Course Boundary

## course_identity

- course code: `CLCH`
- course line: `classical_chinese`
- formal course route: `COURSES/classical_chinese`
- legacy archive route: `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation`
- course title: `Classical Chinese For Translation Studies And Practice`
- course object: translation-major undergraduates
- course format: 16 weeks, 2 class hours per week
- course goal: build foundational Ancient Chinese competence that supports translation studies and translation practice
- current stage: governance boundary bootstrap only
- current stage detail: knowledge-map extraction and `16-session core material matrix` are completed; `TASK-CLCH-LESSON-001 | 16-Week Course Architecture` is next

## route_identity_rule

- `COURSES/classical_chinese` is the only formal course entry for the Classical Chinese line
- `COURSES/classical_chinese/LEGACY_IMPORTS/classical_chinese_translation` is a quarantined legacy import only
- the legacy import is not an active course route, not a source of truth, and not a valid default read target for future agents
- old files such as `COURSE_SOT`, `COURSE_TASK_INDEX`, and `COURSE_TASK_STATE` preserved inside the legacy import remain archival context only and must not be merged into top-level governance state
- `TASK-CLCH-MAT-*`, `TASK-CLCH-LESSON-*`, and `TASK-CLCH-ASSESS-*` must ignore the legacy import unless a future task card explicitly authorizes audited use

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

## source_authority_ladder

- `L0` repo governance SoT:
  - repository-level governance files define the workflow, fail-closed default, and promotion gates
- `L1` official course boundary / roadmap / task registry:
  - course-line scope, route order, and authorized task stage for `classical_chinese`
- `L2` uploaded textbook / reference corpus metadata:
  - declared textbook or reference source identity and locator metadata for user-authorized materials
- `L3` NotebookLM extraction notes:
  - raw extraction notes, indexing hints, outline fragments, and source-location leads only
- `L4` agent-generated summaries / matrices / drafts:
  - structured notes, source maps, summaries, matrices, and draft governance artifacts derived from higher levels
- `L5` classroom-facing deliverables:
  - lesson-facing, classroom-facing, or student-facing outputs allowed only after maturity gates outside this task
- promotion rule:
  - lower-authority levels may organize, summarize, or route higher-authority inputs, but may not replace them
- non-substitution rule:
  - `L3` NotebookLM notes and `L4` agent drafts must never be treated as textbook equivalents or final classroom content

## mandatory_source_fields

- `source_title`
- `source_type`
- `source_author_or_editor`
- `source_level`
- `chapter_or_section`
- `page_or_location_if_available`
- `extraction_method`
- `copyright_risk`
- `classroom_use_scope`

## source_handling_rules

- every future source-derived artifact for this course line must preserve the mandatory source fields whenever the data exists
- if chapter, section, page, or equivalent locator is missing, the artifact must carry a pending-verification marker
- `source_level` must match the source-authority ladder and may not be silently upgraded
- `extraction_method` must distinguish at least direct teacher note, manual source audit, NotebookLM extraction, or agent-generated synthesis
- any AI-generated derivative content must be marked `draft`, `synthetic`, or `teacher-review-required`

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
- task-family routing rule:
  - `TASK-CLCH-GOV-*` = governance, boundary, routing, protocol, index, and agent constraints only
  - `TASK-CLCH-MAT-*` = material mapping, knowledge map extraction, and source-grounded material matrices below lesson level
  - `TASK-CLCH-PROMPT-*` = NotebookLM, Claude, Cursor, Codex, and similar prompt-pack or extraction-prompt workflow tasks
  - `TASK-CLCH-LESSON-*` = lesson plans, handouts, classroom activities, and PPT structure for specific lessons or units
  - `TASK-CLCH-ASSESS-*` = homework, quizzes, rubrics, and student-output evaluation
  - `TASK-CLCH-REVIEW-*` = retrospective, quality review, and version audit
- naming rule:
  - branch format = `task-clch-<type>-<number>-<kebab-title>`
  - task-card or governance filename format = `TASK-CLCH-<TYPE>-<NNN>_<Title_Case_With_Underscores>.md`
  - closeout filename format = `CLOSEOUTS/TASK-CLCH-<TYPE>-<NNN>_Closeout.md`
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
- NotebookLM output belongs to `L3` in the source-authority ladder
- this task does not claim that NotebookLM extraction has been completed
- this task does not create or simulate NotebookLM output
- NotebookLM output may be used only for extraction leads, structural hints, and intermediate indexing
- NotebookLM output must not be treated as final publishable prose, formal handout text, or approved classroom-facing wording
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
- allowed handling includes short quotation, summary, paraphrase, structured index, classroom-use note, page or chapter locator, knowledge-point mapping, and teacher-only preparation draft
- forbidden handling includes large-scale copying, substitute-textbook lecture notes, downloadable reconstructed textbook packets, source-free stitched prose, and promotion of NotebookLM output as final publishable content
- when copyright risk is unclear, output may stay at summary or index level only

## output_maturity_boundary

- current task outputs are governance artifacts only
- course content maturity has not advanced through source audit, reliability grading, course adaptation, or assessment suitability review
- no artifact produced here may be labeled lesson-ready, assessment-ready, or publication-ready
- the next mature output target is not a lesson plan; the governed knowledge map now exists, and the next target is the `16-session core material matrix`
- governance tasks must not generate lesson plans, slides, question banks, papers, or formal classroom materials
- no task may generate a full course, full PPT set, or full question bank unless the active task family and task card explicitly authorize that scope
- route pointers across `TASK_REGISTRY`, `ROADMAP`, `PLAN`, `TASK_STATE`, `TASK_INDEX`, and `CHANGE_LOG` must stay aligned

## fail_closed_rules

- fail closed and record `needs human review` when any of the following is unknown or conflicting:
  - active `TASK-CLCH-*` authorization
  - exact source package or source locator boundary
  - whether NotebookLM output exists, what it contains, or whether it has been reviewed
  - whether a requested output belongs to governance, material, design, or assessment stage
  - whether an AI/vibecoding activity is method-layer support or an improper content substitute
  - whether copyright or publication permission covers the requested excerpt or export
- do not upgrade an unknown source into formal course material
- if page, chapter, section, or equivalent location is unknown, mark `pending verification` and do not present the text as source-stable
- if copyright risk is unknown, output only summary, locator, or index form and do not output long text
- AI-generated content must remain labeled `draft`, `synthetic`, or `teacher-review-required` until human review promotes it
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
- NotebookLM output presented as final classroom prose
- substitute-textbook handouts or reconstructed complete teaching packets
- cross-project governance or content drift into `BTC_WATCHFLOW`, `NESP`, `Lin Yutang paper`, `Thesis_Format_Fixer`, or `daily-review`

## allowed_next_outputs

- governed task cards and governance records
- source-authority metadata templates and review rules
- knowledge-map extraction contract
- `16-session core material matrix` contract
- unit-architecture and lesson-design contracts after material maturity gates are satisfied
- AI/vibecoding learning-activity boundary document as a downstream method-layer task
- assessment and assignment framework after design-stage prerequisites are met
