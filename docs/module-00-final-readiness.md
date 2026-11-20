# Module 0 — Final readiness record

**Audit date:** 2026-11-20
**Overall status:** **MODULE 0 COMPLETE** — environment, learning workspace,
local database, application-role connectivity, and GitHub publication are
verified.

Module 0 is onboarding and project setup, not an additional formal syllabus
module. This record distinguishes installed, configured, reachable,
authenticated, and tested states. No Module 1 lesson or deliverable has been
started.

## Evidence matrix

| Area | Test and evidence | Result | Status | Remaining action |
|---|---|---|---|---|
| Project root and repository | `Get-Location`; `git rev-parse --show-toplevel`; `git worktree list` | `E:\cloud-computing-project-1`; one registered worktree | COMPLETE | None |
| Local Git | `git branch --show-current`; `git status`; `git log -1 --oneline`; `git branch -vv` | `main`; clean; setup commit `2d9213341ac23dfa765218c7bd7f87a5a46a83d3`; tracks `origin/main` | COMPLETE | None |
| Remote configuration | `git remote -v`; `gh repo view shyamsundar7773/cloud-computing-project-1` | `origin` is the intended public repository owned by `shyamsundar7773` | COMPLETE | None |
| GitHub identity | `gh auth status -h github.com`; `gh api user --jq .login` | `shyamsundar7773` is active; token values are not recorded | COMPLETE | None |
| Repository publication | Normal `git push -u origin main`; `git ls-remote --heads origin main` | `origin/main` exists at the same commit as local `main`; upstream tracking is configured | COMPLETE | None |
| Python launcher | `py --version`; `py -0p` | Python 3.14.3 selected; 3.13 and 3.12 also installed | COMPLETE | None |
| Python virtual environment | Activate `.venv`; run `python --version`, `python -m pip --version`, and a basic Python command | `.venv` works; Python 3.14.3 and pip 25.3 execute | COMPLETE | None |
| PostgreSQL service/client | `Get-Service postgresql-x64-18`; `psql --version` | Service running/automatic; client 18.6 | COMPLETE | None |
| PostgreSQL readiness and network | `pg_isready -h 127.0.0.1 -p 3000`; TCP test; DNS and HTTPS probes | PostgreSQL accepts connections on port 3000; `github.com` resolves and port 443 is reachable | COMPLETE | None |
| PostgreSQL authentication | Local `psql -X -W` administrator session; `SELECT current_user, current_database(), inet_server_port(), version()` | Authenticated as `postgres` to PostgreSQL 18.6 on port 3000 | COMPLETE | None for administrator access |
| ShopSphere database and role | Catalog queries for role/database; role flags; `CREATE ROLE`, `\password`, `ALTER ROLE`, `CREATE DATABASE` | `shopsphere` exists, owned by login-capable `shopsphere_app`; role has no superuser, createdb, or createrole privileges | COMPLETE | None |
| Python/PostgreSQL integration | Project `.venv` Python connection with `psycopg` 3.3.9; `SELECT current_user, current_database(), inet_server_port(), 1` | Read-only query returned `shopsphere_app`, `shopsphere`, port `3000`, and `1`; password was entered only into a hidden local prompt | COMPLETE | None |
| WSL/Linux | `wsl --status`; Ubuntu version/Python/Git commands | WSL 2; Ubuntu 26.04 LTS, Python 3.14.4, Git 2.53.0 | COMPLETE | None |
| VS Code | `code --version`; extension listing; inspect `.vscode` settings | VS Code 1.146.0; Python, Pylance and PostgreSQL extensions available; workspace selects `.venv` | COMPLETE | None |
| Project networking | `Resolve-DnsName github.com`; `Test-NetConnection github.com -Port 443` | DNS and TCP 443 succeed | COMPLETE | None |
| Documentation | Review README, architecture, environment, programme guide, and module indexes | Setup and planned architecture are documented; syllabus titles/phases are mapped | COMPLETE | Keep evidence current as components are implemented |
| Ten-module workspace | Inspect `docs/modules/`, guide, and tracker | Ten syllabus-aligned module indexes and 40 phase workspaces; all phases remain NOT STARTED | COMPLETE | Begin teaching only when explicitly requested |
| Learning workflow | Review shared phase, assessment, and troubleshooting templates | Evidence, independent explanation, assessment, mistakes, and revision fields are present | COMPLETE | Learner-owned records remain to be created during lessons |
| Secret protection | `git check-ignore`; tracked-file secret-pattern scan; inspect `.gitignore` and `.env.example` | `.env`, `.env.*`, `.venv`, logs and database backups are excluded; `.env.example` is allowed and contains placeholders; targeted scan found no common secret patterns | COMPLETE | Review all staged changes before publishing |

## Environment summary

- Windows 11 Pro build 26200; PowerShell 5.1; VS Code 1.146.0.
- Windows Python 3.14.3 and a working project `.venv`; pip 25.3.
- Git 2.56.1; GitHub CLI 2.103.3.
- WSL 2 / Ubuntu 26.04 LTS; Python 3.14.4 and Git 2.53.0.
- PostgreSQL 18.6 service and client are present and reachable on local port
  3000. An administrator login was verified securely in the local terminal.
- The `shopsphere` database and login-capable, non-privileged `shopsphere_app`
  role were created and verified. Python application-role authentication and
  a read-only query were verified with `psycopg` 3.3.9 from `.venv`.
- `psycopg` 3.3.9 is installed in `.venv` and pinned in `requirements.txt`.

No passwords, tokens, connection strings, or actual environment values belong
in this record. `.env.example` contains placeholders only; the working `.env`
file must remain local and ignored.

## Scope notes

- The application, pipeline, reports, and cloud resources are intentionally
  not implemented during Module 0.
- No lesson or learner assessment has been completed; all 40 formal phase
  workspaces remain NOT STARTED.

The local environment and syllabus workspaces are ready to support the
programme. Module 1 and all other formal modules remain **NOT STARTED**; no
lesson, assessment, business requirements document, or system-context
deliverable has been completed.
