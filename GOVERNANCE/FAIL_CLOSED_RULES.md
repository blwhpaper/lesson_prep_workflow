# Fail-Closed Rules

Stop promotion or generation and mark `needs human review` when any of these is unknown:

- active task or active course;
- source identity, edition, page, chapter, or quotation boundary;
- copyright or publication permission;
- privacy boundary or presence of student data;
- prompt purpose, input scope, output use, or publication boundary;
- artifact maturity or review history;
- cross-course ownership;
- cross-repository authorization;
- assessment suitability.
- required SOT, task card, or state-file consistency.

Fail-closed action: preserve the artifact at its current level, record the uncertainty, avoid downstream use, and request human review. Silence and plausible inference are not approval.

NotebookLM draft / extracted / unverified output must remain below source-audited status until the required evidence chain exists.
Unknown source package, copyright status, privacy status, unauthorized-full-text status, or public-release status for NotebookLM intake also requires fail-closed handling.
