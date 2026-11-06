# Conventions

## Append-only

- A hypothesis is written **before** the work it covers. Its registered part (statement,
  prediction, what would refute it, registration date) is never edited afterwards.
- Results are appended to the hypothesis file, dated, and link to the tasks they come from.
- A refuted hypothesis is kept, never deleted. A refutation is a result.
- Raw data is never modified. Corrections go in a new, dated file.
- Protocols change by adding a new dated version, so each task points at the exact
  version it used.

## Hypothesis status

`open`: registered, no conclusive result yet.
`supported`: the results match the prediction.
`refuted`: the results meet the refutation criterion. Keep the file, append the result.

## Tasks

- One task = one goal, in `<area>/tasks/TASK-<NNN>-<slug>.md`. Numbers are unique across
  the whole repo and never reused.
- Every task names its **executor** (`human` or `agent`) and the **hypothesis** it serves.
- A human task names its protocol and where its raw data goes.
- An agent task has explicit input and output contracts and checks.
- Task status: `open`, `in_progress`, `blocked`, `done`, `rejected`.
- The task file is also the record: fill in its Result section when done.

## Commits

- One logical change per commit, conventional messages (`feat:`, `docs:`, `fix:`, ...).
- Commit results with the task that produced them, and mention the task id.
- Do not rewrite history once a hypothesis is registered.

## Executors

- **human:** does bench or field work, records raw data, fills in the Result section.
- **agent:** works on code in the sibling repo, in an isolated branch or worktree, then
  fills in the Result section. A human reviews before the result updates a hypothesis.
