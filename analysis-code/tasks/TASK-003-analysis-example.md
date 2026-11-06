---
id: TASK-003
title: <analysis example>
status: open             # open | in_progress | blocked | done | rejected
executor: human          # human | agent
hypothesis: H1
depends_on: [TASK-002]
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---

# TASK-003: `<analysis example>`

> One task = one goal. Same header as an agent task; the body below is for a human.

## Goal

`<The question to answer from the pipeline outputs, and the hypothesis it bears on.>`

## Protocol

- **Protocol:** `<analysis plan or protocol file, version>`
- **Decision rule:** `<the criterion, taken from the hypothesis, that decides the status>`

## Raw data

- **Reads:** `<pipeline outputs from TASK-002 and where they are>`
- **Goes to:** `<location of figures, tables and notes, see ../../environment.md>`

## Done when

- [ ] `<analysis run and outputs deposited>`
- [ ] `<dated result appended to the hypothesis file>`

## Result

> Filled in by the person who did the work, always. Set `status` to `done` or `blocked`.

### Outcome

`<What the analysis shows.>`

### Effect on the hypothesis

`<supported | refuted | unchanged, with a link to the appended entry.>`
