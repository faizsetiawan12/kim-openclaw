# Local Markdown Issue Tracker

Keep work items under `.scratch/<feature-slug>/`.

- Store one specification at `.scratch/<feature-slug>/spec.md`.
- Store one implementation issue per file at `.scratch/<feature-slug>/issues/<NN>-<slug>.md`.
- Put `Status:` near the top of each issue and append discussion under `## Comments`.
- Use a map at `.scratch/<feature-slug>/map.md` when work has dependencies.

`.scratch/` is local planning state and is excluded from Git.
