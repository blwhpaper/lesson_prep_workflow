# Agent Entry Protocol

Follow the sequence in `AGENTS.md` exactly. Verify that repository state, current-course pointer, course state, and task card agree before acting.

An agent may read only the active course by default. It may not broaden scope because files are available. On conflict, the narrower task-card boundary wins unless it contradicts a higher source of truth; contradictions require human review.

Entry is fail-closed. If any required SOT, state file, task card, source evidence expectation, or route pointer is missing or conflicting, stop, record `needs human review`, and do not invent the missing authority.

Prompts are executable input contracts only. Agents may draft or revise prompt templates, but may not treat prompt text as approved lesson, assessment, or course-delivery material without a separate governed promotion path.
