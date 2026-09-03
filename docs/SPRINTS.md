# Sprints and Slices

## Sprint

A sprint is a bounded outcome window containing several small, independently reviewable slices. It is not defined by ceremony; it is defined by a clear outcome and limits.

### Sprint brief

```markdown
# Sprint: <name>

## Outcome
<What should be true when this sprint is complete?>

## Scope
<Included work>

## Out of scope
<Explicit exclusions>

## Source set
<Databases, Drive folders/files, guidelines, journals, etc.>

## Risks / unknowns
<Clinical, evidence, privacy, tooling, or publication risks>

## Planned slices
1. ...
2. ...
3. ...

## Definition of done
- [ ] ...
```

## Slice

A slice is the smallest useful vertical unit that can be understood, reviewed, and merged independently.

### Slice contract

Every non-trivial slice should have:

- one primary objective;
- a bounded file set;
- explicit acceptance criteria;
- known source inputs;
- a statement of what is out of scope;
- verification appropriate to the risk.

### Research/writing progression

A typical project may use these slices:

1. Question/scope
2. Source collection
3. Evidence extraction
4. Synthesis
5. Draft
6. Fact/citation verification
7. Publication formatting

These are examples, not a requirement to create seven PRs. Combine adjacent steps only when the resulting PR remains easy to understand and verify.

## Split signals

Split a slice before implementation when:

- the PR has multiple unrelated objectives;
- reviewers would need a large context dump to understand it;
- research collection and final publication polishing are mixed together;
- a failure would make rollback ambiguous;
- acceptance criteria cannot be stated clearly;
- the task is so large that instructions risk being truncated or lost.

## Naming examples

- `research/trd-ketamine-search-scope`
- `research/trd-ketamine-evidence-extraction`
- `writing/pmhnp-post-first-draft`
- `writing/pmhnp-post-fact-check`
