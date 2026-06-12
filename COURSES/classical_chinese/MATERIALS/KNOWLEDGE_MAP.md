# Classical Chinese Knowledge Map

## Status

- task: `TASK-CLCH-MAT-001`
- artifact type: governed knowledge-map extraction
- maturity: `draft` / `teacher-review-required`
- source level used for this artifact: `L1` course boundary and roadmap plus `L2` source-package metadata only
- source text handling: no long copyrighted textbook text reproduced

## Course Goal Boundary

- course object: translation-major undergraduates
- course role: build Ancient Chinese competence that directly supports reading, interpretation, terminology awareness, and translation practice
- course limit: not a general Chinese culture survey
- course limit: not a pure history-of-linguistics or specialist philology sequence
- course limit: not a lesson-plan or weekly-teaching artifact

## Textbook Source Boundary

- authorized source package names only:
  - Wang Li, `古代汉语`, four volumes
  - `古代汉语常识`
  - Guo Xiliang, `古代汉语`, two volumes
  - `古代汉语语法讲稿`
  - Qiu Xigui, `文字学概要`
- allowed source reference form: book title, volume set, topic area, abstract knowledge point
- forbidden source handling: long excerpt bank, reconstructed chapter notes, substitute-textbook prose
- pending downstream dependency: later `L2` and `L3` extraction work must add chapter or page locator metadata where available

## Use Labels

- `matrix_fit`: suitable for future `16-session core material matrix`
- `teacher_background`: teacher preparation support only, not default core-session target
- `mixed`: can support matrix selection but should remain compressed or indirect in student-facing planning

## Domain Map

### 1. 文字

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 汉字构形基础：象形、指事、会意、形声 | `matrix_fit` | build script-awareness needed for meaning inference | none | introduces graph-based meaning analysis | helps infer semantic hints in unfamiliar forms | good for prompt drills on character analysis steps | mainly `文字学概要`; supported by introductory sections of `古代汉语` |
| 古今字、异体字、通假字辨识 | `matrix_fit` | supports accurate reading and avoids false modern normalization | basic character awareness | used in text annotation and variant discrimination | directly affects lexical choice and sentence interpretation | strong for error-detection prompts and comparison prompts | `古代汉语` plus `文字学概要`; specific examples need later locator verification |
| 字形演变与训释边界 | `teacher_background` | prevents overconfident etymological storytelling | basic character categories | teacher explanation control | indirect but useful for explaining why some inferences are weak | useful for prompts that test evidence vs speculation | mostly `文字学概要` and teacher review |

### 2. 词汇

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 古今词义差异 | `matrix_fit` | foundational for avoiding modern-semantic projection | basic reading ability | central in vocabulary explanation | directly affects translation accuracy | good for contrastive prompt templates | `古代汉语` and `古代汉语常识` |
| 单音词与复音词演变意识 | `matrix_fit` | helps parse classical lexical units correctly | basic sentence segmentation | supports word-boundary analysis | reduces mistranslation caused by wrong chunking | suitable for segmentation prompts | `古代汉语` and `古代汉语语法讲稿` |
| 词类活用 | `matrix_fit` | core bridge between lexicon and syntax | parts-of-speech awareness | frequent annotation focus | crucial for translating compressed classical expressions | useful for transformation and explanation prompts | `古代汉语` and `古代汉语语法讲稿` |
| 同义近义与语域差别 | `mixed` | refines interpretive nuance | basic lexical knowledge | supports comparative explanation | improves target-language choice in translation | useful for candidate-translation comparison prompts | needs topic-based extraction from core textbooks |

### 3. 语法

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 判断句、被动句、疑问句等基本句式 | `matrix_fit` | gives students a stable parsing scaffold | basic lexical recognition | high-frequency sentence-pattern teaching | directly guides sentence restructuring in translation | strong for parsing prompts and sentence-label prompts | `古代汉语` and `古代汉语语法讲稿` |
| 宾语前置、定语后置、介词结构等语序现象 | `matrix_fit` | explains non-modern order patterns | basic sentence-type knowledge | core difficulty-removal topic | key for mapping source order to target order | good for reorder-and-explain prompts | `古代汉语` and `古代汉语语法讲稿` |
| 省略与意合 | `matrix_fit` | trains students to recover implicit relations carefully | sentence parsing basics | used in close reading and translation justification | essential for coherent translation and commentary | good for prompt templates that require evidence-based filling of omitted parts | `古代汉语` and reading sections |
| 虚词系统与语气功能 | `matrix_fit` | unlocks clause relation and tone | sentence parsing basics | persistent course backbone | directly affects nuance, logic, and stance in translation | very strong for prompt-based micro-analysis | `古代汉语`, `古代汉语常识`, `古代汉语语法讲稿` |
| 语法术语体系与分析尺度控制 | `teacher_background` | keeps explanation precise without overloading learners | teacher review | helps teacher pitch depth correctly | indirect | useful for prompt calibration rules | mostly teacher-side synthesis from grammar references |

### 4. 音韵

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 反切、声母、韵部的入门概念 | `mixed` | provides minimal historical-phonology literacy | none | short orientation topic | limited direct impact but supports dictionary use and textual notes | useful for glossary-building prompts | `古代汉语常识` and relevant textbook overview sections |
| 音变与假借、通假关联意识 | `mixed` | links sound awareness to reading problems | basic variant-character awareness | helps explain some textual anomalies | moderate relevance where sound clues affect interpretation | moderate for reasoning prompts | requires cross-reference between phonology and textual examples |
| 音韵学史细部与系统重建 | `teacher_background` | preserves teacher background depth without syllabus drift | none | teacher reserve knowledge only | low direct relevance for translation undergraduates | low except for teacher prompt notes | background reference only |

### 5. 文献阅读

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 文言断句与层次划分 | `matrix_fit` | enables readable parsing before interpretation | character and lexical basics | core text-reading operation | directly affects all later translation decisions | strong for stepwise annotation prompts | `古代汉语` reading sections and future source excerpts |
| 常见文体识别：传记、论说、史传、书信等 | `matrix_fit` | builds genre expectations for reading strategy | basic sentence reading | informs passage framing | shapes translation tone and information packaging | useful for genre-aware prompt instructions | topic extraction needed from core textbooks |
| 章法与语篇衔接观察 | `mixed` | moves students beyond sentence-level parsing | sentence and clause analysis | supports deeper reading discussion | improves paragraph-level translation coherence | good for summary-with-evidence prompts | future text-level extraction required |
| 注释依赖控制与证据意识 | `matrix_fit` | teaches students not to accept any gloss uncritically | basic reading operations | key reading-method skill | supports justified translation choices | strong for prompt protocols requiring citation and uncertainty labels | depends on later source-note workflow |

### 6. 翻译实践

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 直译与意译的取舍原则 | `matrix_fit` | connects language analysis to translation decisions | lexical and syntactic basics | bridges reading and production | core practice relevance | strong for compare-two-translation prompts | teacher synthesis anchored to translation-focused course goal |
| 关键词保留、增译、减译、顺译、倒译等策略意识 | `matrix_fit` | provides an operational translation toolkit | sentence parsing and vocabulary control | practice commentary framework | direct | strong for revision prompts | strategy summaries need later text-linked examples |
| 误译类型归纳：漏译、错断、误释、风格漂移 | `matrix_fit` | improves self-correction and peer review | basic translation attempt experience | used in feedback and diagnostics | direct | very strong for critique prompts | teacher synthesis plus future passage examples |
| 文白转换与译文可读性平衡 | `mixed` | helps manage target-language readability | translation basics | supports revision stage | high but should not override source accuracy | useful for rewrite-under-constraints prompts | depends on future practice samples |

### 7. 工具书与训诂

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 常用工具书类型与检索路径 | `matrix_fit` | teaches students how to verify instead of guessing | none | method-layer orientation | direct support for reliable translation | strong for tool-selection prompts | `古代汉语常识` plus teacher tool list |
| 训诂中的本义、引申义、假借义基础 | `matrix_fit` | builds disciplined semantic reasoning | lexical basics | supports word-sense explanation | direct for disambiguation | good for explanation-chain prompts | `古代汉语` and `古代汉语常识` |
| 义项选择的证据优先级 | `matrix_fit` | discourages arbitrary gloss choice | tool-use basics | useful in annotation and translation review | direct | strong for prompts requiring ranked evidence | teacher synthesis constrained by source-authority rules |
| 专深小学材料的扩展阅读 | `teacher_background` | preserves depth without overloading main route | none | teacher reserve only | low direct relevance | low | background only |

### 8. AI 辅助学习与提示词训练

| secondary_point | placement | learning_value | prerequisite | teaching_use | translation_relevance | ai_prompt_potential | source_dependency |
|---|---|---|---|---|---|---|---|
| 用 AI 做断句、词义、句法假设生成后再人工复核 | `matrix_fit` | trains verification-first workflow | reading basics | method support for practice | indirect but useful | very strong; this is prompt-protocol core | bounded by course AI rules, not textbook text |
| 要求 AI 标注不确定性、证据链与待核点 | `matrix_fit` | prevents blind acceptance | none | course-wide AI hygiene rule | indirect but essential for trustworthy translation support | very strong for reusable prompt templates | governance and prompt-pack dependency |
| 用 AI 做误译诊断与版本比较 | `matrix_fit` | supports reflective revision | translation draft experience | feedback support | direct | very strong for critique prompts | depends on later practice materials, not textbook copying |
| 用 AI 代写译文、代替阅读或伪造出处 | `teacher_background` | negative boundary needed to prevent misuse | none | prohibition statement, not teaching target | harmful rather than helpful | should appear only as forbidden prompt examples | governance-only dependency |

## Matrix-Fit Summary

### Suitable For Future `16-Session Core Material Matrix`

- 文字：汉字构形基础；古今字、异体字、通假字辨识
- 词汇：古今词义差异；单音词与复音词演变意识；词类活用
- 语法：基本句式；语序现象；省略与意合；虚词系统与语气功能
- 音韵：反切、声母、韵部入门概念；音变与假借、通假关联意识
- 文献阅读：断句与层次划分；常见文体识别；注释依赖控制与证据意识
- 翻译实践：直译与意译取舍；常用翻译策略；误译类型归纳
- 工具书与训诂：工具书类型与检索路径；本义引申义假借义基础；义项选择证据优先级
- AI 辅助学习与提示词训练：AI 假设生成后人工复核；不确定性与证据链标注；误译诊断与版本比较

### Teacher Background Or Compressed Reserve

- 文字：字形演变与训释边界
- 语法：语法术语体系与分析尺度控制
- 音韵：音韵学史细部与系统重建
- 文献阅读：章法与语篇衔接观察
- 翻译实践：文白转换与译文可读性平衡
- 工具书与训诂：专深小学材料的扩展阅读
- AI 辅助学习与提示词训练：AI 代写译文、代替阅读或伪造出处

## Explicit Prohibitions

- do not build a copyrighted textbook excerpt repository
- do not drift the course into a generic Chinese culture survey
- do not drift a translation-major course into a pure history-of-linguistics course
- do not drift AI use into automatic ghostwriting, source fabrication, or reading substitution

## Downstream Use Boundary

- this file is a structure map only
- downstream `TASK-CLCH-MAT-002` may convert the `matrix_fit` knowledge points into a `16-session core material matrix`
- downstream lesson tasks may not begin from this file alone without the matrix stage
- any later source-linked example must add locator metadata and remain within copyright limits
