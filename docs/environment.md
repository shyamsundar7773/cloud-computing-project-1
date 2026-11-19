# Verified Environment Snapshot

Audit date: 2026-11-03

This file records observed configuration, not credentials. Dynamic values such
as available memory can change while the computer is in use.

| Area | Observed state |
|---|---|
| Workspace | `E:\cloud-computing-project-1`; initially empty |
| Windows | Windows 11 Pro, 64-bit, build 26200 |
| CPU | 12th Gen Intel Core i5-12450H, 8 cores / 12 logical processors |
| Memory | Approximately 15.7 GiB installed; approximately 1.2 GiB available at audit time |
| Storage | C: approximately 341.8 GiB total / 43.5 GiB free; E: approximately 317.4 GiB total / 132.7 GiB free |
| VS Code | 1.144.1; Python, Pylance, PostgreSQL, and other extensions are installed |
| Windows Python | Python 3.14.3 selected by `py`; Python 3.13 and 3.12 are also installed |
| Python packaging | `py -m pip` works; standalone `python` and `pip` commands were not found on PATH |
| Windows Git | 2.50.0; global `user.name` and `user.email` are configured (values intentionally omitted) |
| GitHub CLI | 2.100.0; authentication status check succeeded |
| PostgreSQL client | `psql` 18.6 |
| PostgreSQL service | `postgresql-x64-18`, running and configured for automatic start |
| PostgreSQL port | Existing configuration specifies port 3000; service configuration was not changed |
| PostgreSQL access | Local TCP and `pg_isready` succeeded on port 3000; a SQL query could not authenticate without a password |
| WSL | WSL 2; Ubuntu 26.04 LTS, x86_64 |
| Ubuntu tools | Python 3.14.4 and Git 2.53.0; Ubuntu DNS lookup for `github.com` succeeded |
| Network | Windows DNS lookup for `github.com` and TCP connection to port 443 succeeded |

The PostgreSQL server version and a successful authenticated database query
were not verified. No passwords, tokens, or connection strings are stored
here.
