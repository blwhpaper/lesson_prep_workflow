# Material Database Schema

Every material record uses these fields:

| field | purpose |
|---|---|
| `entry_id` | stable record identifier |
| `course_id` | owning course |
| `category` | disciplinary category |
| `source_text` | bounded excerpt or description |
| `concept_or_pattern` | knowledge represented |
| `source_reference` | traceable citation and locator |
| `source_reliability` | grade with rationale |
| `disciplinary_explanation` | domain explanation |
| `modern_reconstruction` | modern restatement where relevant |
| `teaching_judgment_point` | judgment students practice |
| `ai_explainability_point` | possible AI explanation use |
| `ai_explanation_review_point` | required verification |
| `teaching_use` | permitted teaching use |
| `assessment_use` | permitted assessment use |
| `ai_review_use` | permitted AI-review use |
| `datafication_use` | permitted structured-data use |
| `non_programming_alternative` | equivalent route |
| `difficulty` | defined difficulty grade |
| `artifact_maturity_level` | L0-L6 |
| `needs_human_review` | boolean plus reason |

No field may silently substitute for missing source evidence.
