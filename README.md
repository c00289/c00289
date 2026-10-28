# Roy Mendoza

Functional safety engineer. Capgemini contractor on the ASI Robotics Wheel Loader programme, where
the job is the platform safety lifecycle: safety plan, STPA, HARA, functional safety concept, and
the evidence that ties them together.

I build small, honest tools for that work. Each one is named after a person whose life's work is
the job the tool does, and each follows the same rules: a database is the single source of truth,
every file it produces is a regenerated view, and everything a human can do through a window an
agent can do through the same command.

## The ASI FuSa tools

| Repository | What it does |
|---|---|
| [asi_fusa_tools](https://github.com/c00289/asi_fusa_tools/blob/master/README.md) | The charter: the family's conventions, version ladder and plans, in one document. |
| [asi_kletz](https://github.com/c00289/asi_kletz/blob/main/README.md) | The Safety Plan and the Weekly Activity Tracker: deliverables across the ten lifecycle phases, sprints of ten points, the status text built back out of the database. CLI, desktop window, SQLite, JSON and Excel views. |
| [asi_dewey](https://github.com/c00289/asi_dewey/blob/main/README.md) | The working-knowledge base of the programme: tasks, facts, links, people, QMS documents. Same shape as Kletz, never the same code. |
| [asi_escher](https://github.com/c00289/asi_escher/blob/main/README.md) | Pure-Python diagrams: activity, flowchart, state and SysML block diagrams to PNG, SVG, DOT and Mermaid, with a layout check. |
| [asi_gutenberg](https://github.com/c00289/asi_gutenberg/blob/main/README.md) | Pure-Python documents: specs, reports, plans, procedures and minutes to Markdown, PDF and Word from one model, figures included. |
| [asi_hopper](https://github.com/c00289/asi_hopper/blob/main/README.md) | A read-only, audited, replayable door into Jira Cloud, with a fixture-replay gateway so tests never touch the network. |
| [asi_onboarding](https://github.com/c00289/asi_onboarding/blob/main/README.md) | The onboarding sessions turned into work products: a corpus, 64 diagrams and ten decks. |

How they fit: the two primary tools (Kletz, Dewey) own a database, a command vocabulary, a CLI and
a window; the generators (Escher, Gutenberg) take plain data and produce files; the gateway
(Hopper) reads an external system and hands plain records up. Primary tools use every generator
and the gateway; nothing flows back down; the siblings share conventions, never code.

## How I work

- Trevor Kletz asked of every line of a plan what could go wrong. The tools are built to make that
  question cheap to ask.
- Nothing invented, nothing bent to fit: a claim in a document points at the row, the recording
  time or the ticket it came from.
- Scripts that assert an exact match before they change anything, and a test suite that runs
  against the real generators.

Standards I work to: IEC 61508, ISO 25119, ISO 13849, STPA for hazard analysis.
