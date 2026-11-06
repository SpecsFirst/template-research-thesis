# template-research-thesis

A [Copier](https://copier.readthedocs.io) template for a thesis specs repo kept as a
lab notebook. A hypothesis is written down before the work, each piece of work is a task
done by a human or an agent, and results are appended to the hypothesis they test.

It is generic: it works for any experimental thesis with bench or field work, and it
contains nothing specific to one discipline or to one agent tool.

## Use it

```bash
uv run --with copier copier copy https://github.com/SpecsFirst/template-research-thesis <name>
```

Copier asks for the project title and the researcher's name, then writes the files below
into `<name>/`. Read `main.md`, then `conventions.md`.

## What you get

```
<name>/
├── main.md                              goal, scope, table of hypotheses and their status
├── conventions.md                       append-only rule, commits, executors, statuses
├── environment.md                       storage, compute, instruments
├── hypotheses/
│   └── H1-short-name.md                 registered part, then dated results
├── lab/                                 work beyond code: bench, fieldwork (rename freely)
│   ├── protocols/
│   │   └── short-name.md
│   └── tasks/
│       ├── board.md
│       └── TASK-001-bench-example.md        executor: human
└── analysis-code/                       reusable pipelines (the code lives in a sibling repo)
    ├── main.md
    └── tasks/
        ├── board.md
        ├── TASK-002-pipeline-example.md     executor: agent
        └── TASK-003-analysis-example.md     executor: human
```

`README.md`, `LICENSE` and `copier.yml` stay in the template and are not copied.

## The method in short

- **Pre-registered hypotheses.** A hypothesis file holds a statement, a prediction, what
  would refute it and a registration date. That part is never edited. Results are
  appended, dated, and link to the tasks they come from. A refuted hypothesis is kept.
- **Tasks for humans and agents.** Every task names its executor and the hypothesis it
  serves. A human task names its protocol and where its raw data goes. An agent task has
  input and output contracts and checks.
- **Placeholders.** Examples use `<angle-bracket>` placeholders. Replace them, rename
  `lab/` and `analysis-code/` to fit your study, add as many hypotheses and tasks as you need.

## Develop the template

```bash
uv run --with copier copier copy --defaults --vcs-ref HEAD \
  --data project_title="Test" --data researcher="Test" . <empty dir>
```

Files keep their real names (`_templates_suffix: ""`), so `main.md` is readable on GitHub
and in the gallery. Only `{{ project_title }}` and `{{ researcher }}` are substituted.

## License

CC0-1.0, see `LICENSE`.
