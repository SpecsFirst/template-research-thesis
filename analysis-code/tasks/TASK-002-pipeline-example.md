---
id: TASK-002
title: <pipeline example>
status: open             # open | in_progress | blocked | done | rejected
executor: agent          # human | agent
hypothesis: H1
depends_on: []
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---

# TASK-002: `<pipeline example>`

> One task = one goal. Same header as a human task; the body below is for an agent.

## Goal

`<The pipeline to build: what it reads, what it computes, what it writes.>`

## Input contract

```yaml
repo: <path of the code repo>
branch: <task branch>
inputs:
  - <raw data location, read-only>
  - <protocol or earlier task output>
scope:
  write: [<paths the agent may change>]
  read_only: [<paths it may only read>]
```

## Output contract

```yaml
artifacts:
  - <file or directory the pipeline writes>
contract:
  - <format, columns, units, naming>
returns: <the branch with its commits, and the filled Result section>
```

## Checks

- `<command that runs the pipeline on a small input>`
- `<command that runs the tests>`
- `<property the output must satisfy>`

## Result

> Filled in by the agent, always. Set `status` to `done` or `blocked`.

### Outcome

### Artifacts produced

### Opinion / concerns
