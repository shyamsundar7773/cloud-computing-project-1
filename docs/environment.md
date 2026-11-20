# Development environment

Last verified: 2026-11-20. This document records tool readiness, not secrets.
Recheck version numbers after upgrades; authentication and connection claims
are kept separate from service and network checks.

| Area | Verified state |
|---|---|
| Workspace | `E:\cloud-computing-project-1`; local checkout on `main` |
| Windows | Windows 11 Pro, 64-bit, build 26200; PowerShell 5.1 |
| VS Code | 1.146.0; Python, Pylance, and PostgreSQL extensions available |
| Windows Python | Python 3.14.3 selected by `py`; Python 3.13 and 3.12 also installed |
| Project environment | `.venv` exists; activation, Python execution, and `python -m pip` verified |
| Python command | `python` is available after `.venv` activation; it is not available on the unactivated system PATH |
| Windows Git | 2.56.1; GitHub CLI 2.103.3 |
| GitHub authentication | `shyamsundar7773` is the active CLI account; see the Module 0 readiness record for repository and push evidence |
| WSL | WSL 2 with Ubuntu 26.04 LTS; Ubuntu Python 3.14.4 and Git 2.53.0 verified |
| PostgreSQL client | `psql` 18.6 |
| PostgreSQL service | `postgresql-x64-18`, running with automatic startup |
| PostgreSQL readiness | `pg_isready` and TCP checks pass on `127.0.0.1:3000` |
| PostgreSQL authentication | Administrator login verified through a local password prompt; application-role authentication verified by a read-only Python query |
| ShopSphere database and role | `shopsphere` created and owned by `shopsphere_app`; role can log in and has no superuser, database-creation, or role-creation privilege |
| Python PostgreSQL driver | `psycopg` 3.3.9 installed in `.venv`; dependency pinned in `requirements.txt` |
| Network | DNS resolution for `github.com` and TCP port 443 succeed |

## Python environment

From the project root, create the environment only if it is absent:

```powershell
py -3.14 -m venv .venv
```

Activate and verify:

```powershell
.\.venv\Scripts\Activate.ps1
python --version
python -m pip --version
```

Install the pinned project dependency after activating `.venv`:

```powershell
python -m pip install -r requirements.txt
```

## Local configuration and PostgreSQL

Copy `.env.example` to `.env` only when local application settings are needed.
Replace placeholders using a local editor; never commit `.env` or paste a
password into chat. PostgreSQL is reachable at `127.0.0.1:3000`; an
administrator SQL login was verified using a local password prompt. The
`shopsphere` database is owned by the login-capable `shopsphere_app` role,
which has no elevated cluster privileges. Application-role authentication
from the project `.venv` returned the expected role, database, port, and
read-only query result. Do not change the existing service, port, or
authentication configuration for convenience.

## Editor and Linux

The project-scoped VS Code settings select
`${workspaceFolder}\\.venv\\Scripts\\python.exe`, enable terminal activation,
and use PowerShell as the Windows terminal profile. Recommended extensions are
listed in `.vscode/extensions.json`. Ubuntu under WSL is available for later
Linux practice; Windows PowerShell remains the primary project environment.

## GitHub

The local `origin` URL is the ShopSphere GitHub repository. The active CLI
identity and remote publication state are recorded in
`module-00-final-readiness.md`. Do not infer Git push access solely from a
successful `gh auth status`; verify the active account and resulting remote
commit. Token values and credentials are intentionally not documented.
