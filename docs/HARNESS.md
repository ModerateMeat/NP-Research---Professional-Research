# Research & Writing Harness

## Purpose

This repository is a controlled workspace for nurse-practitioner research, evidence synthesis, professional posts, educational writing, and publication-oriented drafts. The goal is reproducible, clinically responsible work with a visible review trail.

## Sources of truth

1. `AGENTS.md` — operating instructions for agents and automation.
2. `docs/` — durable policies, standards, and workflow rules.
3. Topic/project folders — scoped research and writing artifacts.
4. GitHub issues/PRs — work history, review, decisions, and acceptance.
5. Connected source systems such as Google Drive — original source artifacts when applicable.

Chat history and terminal scrollback are context, not canonical project records.

## Recommended structure

```text
research/<topic>/
  README.md
  question.md
  sources.md
  evidence-table.md
  synthesis.md

writing/<project>/
  brief.md
  draft.md
  fact-check.md
```

Create only the artifacts a project actually needs; do not create empty bureaucracy for its own sake.

## Normal lifecycle

1. Define the question, audience, deliverable, and acceptance criteria.
2. Create an issue or sprint brief when the work is more than a trivial edit.
3. Split the outcome into small vertical slices.
4. Create a branch for the current slice.
5. Retrieve sources through connected tools first.
6. Record source metadata and evidence before making strong factual claims.
7. Draft/synthesize in project Markdown.
8. Verify claims, citations, privacy, and clinical wording.
9. Open a PR that explains scope, sources, risks, and checks.
10. Review, resolve comments, then merge.

## Definition of done

A slice is done when its stated acceptance criteria are met, source-dependent claims are traceable, privacy/safety checks are complete, the diff is understandable, and the PR can be merged without relying on hidden chat context.
