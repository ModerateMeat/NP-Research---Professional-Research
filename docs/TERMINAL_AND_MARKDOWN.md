# Terminal and Markdown Safety

## Principle

Complex instructions and long generated text are files, not shell commands.

## Do not

Do not paste multi-page GPT output, research protocols, source summaries, article drafts, or long Markdown documents into:

- giant `echo`/`printf` commands;
- shell heredocs used as a substitute for normal file operations;
- large inline Python/Node strings;
- terminal commands whose correctness depends on preserving thousands of pasted characters.

These patterns create avoidable risk of truncation, quoting corruption, accidental execution, and partial requests.

## Preferred order

1. GitHub connector file operation.
2. Appropriate connected document/source tool.
3. Local file operation only when needed.
4. Terminal command that references a verified file path.

## Safe local fallback

If generated text must be handled locally:

1. save the complete content to a `.md`, `.txt`, or appropriate source file;
2. verify that the file exists;
3. inspect beginning/end and, for important long files, size/line count;
4. operate on the file by path;
5. inspect the resulting diff;
6. commit only after completeness is confirmed.

If content appears truncated, stop. Repair the source file before running downstream steps.

## Acceptable terminal content

Short commands, branch names, file paths, one-line commit messages, small configuration values, and validation commands are acceptable.

## Markdown convention

Use Markdown for durable:

- research questions and protocols;
- sprint/slice briefs;
- task specifications and acceptance criteria;
- source lists and evidence notes;
- synthesis documents;
- writing briefs, drafts, and fact checks;
- review checklists and handoffs.

A future session should be able to reproduce the intended work by reading the repository without needing a giant pasted prompt from a prior chat.
