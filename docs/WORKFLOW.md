# Connector-First GitHub Workflow

## Default path

`Issue/brief -> branch -> connector-based edits -> validation -> PR -> review -> merge`

## GitHub connector rule

Use the GitHub connector for repository work whenever its action exists, including:

- reading repository files;
- creating branches;
- creating/updating files;
- opening/updating issues and PRs;
- reading changed files and review comments;
- checking CI/status information;
- merging when authorized and appropriate.

Do not default to `git`/`gh` terminal operations simply because they are familiar.

## Google Drive connector rule

When a research source, prior paper, reference document, table, or other relevant artifact already exists in connected Google Drive:

1. search Drive first;
2. read the relevant material from Drive;
3. preserve the original unless the user explicitly requests an edit;
4. record enough source metadata in the repo to reproduce the research trail;
5. do not copy sensitive or unnecessary source content into GitHub.

## Branch and PR rules

Substantive changes do not go directly to `main`.

Suggested branches:

- `harness/<slice>`
- `research/<topic-or-slice>`
- `writing/<deliverable-or-slice>`
- `docs/<change>`
- `fix/<issue>`

A PR should have one primary objective and be independently reviewable/reversible.

## PR description should answer

- What changed?
- Why is this slice needed?
- What is deliberately out of scope?
- Which sources or connected artifacts were inspected?
- What clinical/research risks or uncertainties remain?
- How was the work checked?
- What are the acceptance criteria?

## Merge rule

Do not merge when required checks fail, material review comments remain unresolved, acceptance criteria are incomplete, or the diff contains unverified clinical claims presented as settled fact.

Prefer squash merge for a clean history unless preserving commits adds useful provenance.

## Fallback rule

If a connector cannot complete an operation, document the limitation in the issue/PR and use the narrowest fallback. If terminal work is required, follow `TERMINAL_AND_MARKDOWN.md` and inspect the resulting diff before commit.
