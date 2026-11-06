# {{ project_title }}

Researcher: {{ researcher }}

This is the entry point of the lab notebook. Read `conventions.md` first.

## Goal

`<One or two sentences: the question this thesis answers.>`

## Scope

- **In scope:** `<what the study covers>`
- **Out of scope:** `<what it deliberately leaves out>`

## Hypotheses

Each hypothesis is written in `hypotheses/` before the work starts.
Status is one of `open`, `supported`, `refuted`. Keep this table in sync with the files.

| ID | Statement | Status | Registered |
|----|-----------|--------|------------|
| [H1](hypotheses/H1-short-name.md) | `<one-line statement>` | open | `<YYYY-MM-DD>` |

## Work areas

- `lab/`: work beyond code (bench work, fieldwork, surveys). Rename it to fit your study.
- `analysis-code/`: reusable pipelines and analyses. The code itself lives in a sibling repo.

Each area has `tasks/board.md`, the list of its tasks and their status.

## Where things are deposited

- **Raw data:** `<storage location, see environment.md>`
- **Code:** `<URL of the sibling code repo>`
- **Results:** `<where processed results and figures are deposited>`

## Decisions

Dated, one line each, newest last.

- `<YYYY-MM-DD>`: `<decision and why>`
