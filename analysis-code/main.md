# analysis-code

Reusable pipelines and analyses for `{{ project_title }}`. Rename this directory to fit.

The code itself lives in a sibling repo, not here. This directory holds only the specs
that describe it, as tasks.

## Code location

- **Repo:** `<URL of the code repo>`
- **Local path:** `<path of the sibling checkout>`
- **Default branch:** `<main>`

## Pipelines

| Pipeline | Input | Output | Serves |
|----------|-------|--------|--------|
| `<pipeline name>` | `<raw data it reads>` | `<files it writes>` | H1 |

## Rules

- Pipelines read raw data and never modify it.
- Every run is reproducible from the code version and the inputs named in its task.
- Agent tasks run in an isolated branch or worktree of the code repo.
- Analyses that conclude on a hypothesis are done by a human, on pipeline outputs.

## Dev commands

```bash
<command to set up, run and test the pipelines>
```

## Tasks

See `tasks/board.md`.
