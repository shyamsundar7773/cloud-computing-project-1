# Cloud Project

Cloud Project is a practical learning workspace for building foundations in
Windows, networking, Linux, Python, Git, SQL, REST APIs, Azure, cloud
operations, and data engineering. The eventual integrated example is a retail
business cloud operations and data platform.

## Learning sequence

Module 0 establishes and verifies the local project environment. Later modules
will build on that foundation; no Azure resources or paid services are part of
this initial setup.

## Workspace map

- `docs/` — project architecture and verified environment notes
- `.vscode/` — project-scoped editor and extension recommendations
- `.venv/` — local Python virtual environment (ignored by Git)

Additional source, tests, and data folders should be added when their first
module needs them rather than created as empty placeholders.

## Local setup

Open this folder in VS Code. The workspace selects `.venv` as its Python
interpreter and enables Python environment activation in the integrated
terminal. Activate it manually in PowerShell with:

```powershell
.\.venv\Scripts\Activate.ps1
```

Use `deactivate` to leave the environment. The `py` launcher can be used if
the `python` command is not available on PATH.

The existing PostgreSQL service is not managed by this project. Its current
port and authentication requirements are recorded in `docs/environment.md`.
Do not place passwords or other credentials in this repository.

## Safety

This repository is local. No changes to other projects or system services are
made by project scripts. Do not commit or publish changes without explicit
approval.
