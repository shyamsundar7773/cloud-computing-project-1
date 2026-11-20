# ShopSphere — Cloud & Data IT Career Launch

ShopSphere is a fictional online retailer used to learn how business
applications, data systems, and cloud operations fit together. The project
grows incrementally into a Retail Business Cloud Operations & Data Platform;
planned capabilities are not claims about an implemented production system.

## Programme

Module 0 is the one-time local environment and project setup. The formal
programme has ten modules, each completed in order through four perspectives:

1. **A — Project Building**
2. **B — Technical Learning**
3. **C — Business Understanding**
4. **D — Interview Preparation**

Finish all four tracks of a module before moving to the next. The supplied
syllabus is the source of truth for module titles, phase titles, and coverage.
See [the learning programme](docs/learning-programme/README.md) for the module
map, progress tracker, evidence rules, and reusable templates.

## Current foundation

- The Windows `.venv` is configured and can be activated from this directory.
- VS Code workspace settings select the project environment and enable
  terminal activation.
- A local PostgreSQL 18 service is available on port `3000`; the
  `shopsphere` database and least-privilege `shopsphere_app` role have been
  created, and a read-only connection from the project `.venv` is verified.
- `origin` points to the intended GitHub repository. See
  [Module 0 readiness](docs/module-00-final-readiness.md) for current
  authentication and publication evidence.
- No application, data pipeline, or Azure resources have been built as part of
  setup. The local learning database is for practice, not production.

## Windows setup

Open this directory in VS Code. If the project environment does not exist,
create it with the Python launcher:

```powershell
py -3.14 -m venv .venv
```

Activate and verify it:

```powershell
.\.venv\Scripts\Activate.ps1
python --version
python -m pip --version
```

Use `deactivate` to leave the environment. The dependency manifest currently
contains only the PostgreSQL driver used for the verified local read-only
connection. Install it with `python -m pip install -r requirements.txt`; add
other dependencies only when a module requires them.

Copy `.env.example` to `.env` only when a module needs local configuration.
Replace placeholders locally, never commit `.env`, and never put credentials
in code, documentation, command transcripts, or chat. The administrator SQL
login and resource inventory were verified locally; keep the application
password in ignored local configuration only. A service-ready check alone does
not authenticate a database user.

## Project map

- `docs/` — architecture, environment, Module 0 closeout, programme and module
  workspaces
- `src/`, `tests/`, `database/`, `api/`, `cloud/` — indexed starting points for
  future work; no application code is prebuilt
- `data/` — locations and handling guidance for sample and processed data
- `operations/`, `notes/`, `assessments/`, `evidence/` — operational records
  and learner-owned evidence
- `.vscode/` — project-scoped editor settings and extension recommendations
- `.venv/` — local Python environment, excluded from Git

## Safety and scope

Use synthetic or explicitly approved data. Keep passwords, tokens, private
keys, local `.env` files, database dumps, and runtime logs out of version
control. Verify current pricing and limits before any future cloud activity;
Module 0 provisions no cloud resources. Learning phases remain incomplete
until the learner demonstrates, assesses, explains, and revises the work.
