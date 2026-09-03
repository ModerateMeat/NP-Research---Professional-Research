# Agent Operating Rules

These instructions apply to AI agents, coding assistants, and human-assisted automation working in this repository.

## 1. Connector first

1. Use the **GitHub connector first** for repository reads, branch creation, file changes, issues, pull requests, review comments, checks, and merges when the required connector action exists.
2. Use the **Google Drive connector first** for relevant source material already stored in Drive. Search/read the connected source instead of asking for download/re-upload or manually reconstructing it.
3. Use a terminal/local shell only when a connector cannot perform the required operation or a local validation/build step is genuinely necessary.
4. Never silently replace an available connector action with terminal commands.
5. If a connector fails, record the failure and use the narrowest safe fallback.

## 2. PR first

- Do not make substantive changes directly on `main`.
- Create a short-lived branch for each slice.
- Open a PR and keep the PR focused on one reviewable objective.
- Do not merge with unresolved review comments, failed required checks, or unmet acceptance criteria.
- Prefer squash merge unless preserving multiple commits has a clear purpose.

Suggested branch prefixes: `harness/`, `research/`, `writing/`, `docs/`, `fix/`.

## 3. Work in sprints and slices

- A **sprint** is a bounded outcome containing several reviewable slices.
- A **slice** is the smallest useful vertical unit that can be reviewed and merged independently.
- Split work before implementation when a PR would mix unrelated objectives or require a large context reconstruction to review.
- Use [`docs/SPRINTS.md`](docs/SPRINTS.md) for the sprint/slice contract.

## 4. Markdown is the durable handoff format

Long prompts, research protocols, source plans, evidence summaries, drafting briefs, acceptance criteria, and complex instructions should live in `.md` files in the repo.

Do not use terminal scrollback or a chat transcript as the only durable specification for important work.

## 5. No giant terminal pastes

Do not paste multi-page GPT output, research plans, article drafts, or large Markdown bodies into `echo`, `printf`, inline Python strings, shell heredocs, or similarly fragile terminal commands when a file/connector workflow is available.

For generated text that must be processed locally: write it to a file, verify completeness, operate on the file, and inspect the diff before commit. See [`docs/TERMINAL_AND_MARKDOWN.md`](docs/TERMINAL_AND_MARKDOWN.md).

## 6. Research integrity

- Do not cite sources that were not inspected.
- Never fabricate DOI, PMID, page number, quotation, effect size, bibliographic data, or study finding.
- Separate evidence, inference, and opinion.
- Record uncertainty, conflicts, and evidence gaps.
- Verify clinically important numbers against the underlying source before publication.
- Prefer primary literature, systematic reviews/meta-analyses, guidelines, regulators, and authoritative professional bodies over marketing or unsourced secondary summaries.

## 7. Clinical safety and privacy

- Do not commit PHI or patient-identifiable information.
- De-identify clinical examples before they enter the repository.
- Distinguish established practice from preliminary, off-label, investigational, or unapproved uses when relevant.
- Do not make diagnostic or treatment claims beyond the evidence reviewed.
- Preserve jurisdiction and scope-of-practice context when discussing NP practice rules.

## 8. AI-assisted work

AI may search, organize, synthesize, edit, and draft. Generated clinical/scientific claims are not considered verified merely because they are well written.

- Trace evidence-dependent claims to inspected sources.
- Verify citations before publication.
- Do not use chat memory as the sole source for a factual clinical claim.
- Never hide uncertainty or invent missing facts.
- Keep reproducible task instructions in repository Markdown.

## 9. Source of truth

The repository files and merged PR history are the durable project record. When chat instructions conflict with a newer approved repo rule, surface the conflict rather than silently overriding the repo.
