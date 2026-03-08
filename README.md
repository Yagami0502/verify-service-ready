# verify-service-ready

A Codex skill for proving a service or dashboard is actually ready before handoff.

## What it captures
- Test-first verification order
- Frontend build confirmation
- Live HTTP health checks
- Runtime state confirmation from the running service

## Install
1. Clone or download this repository.
2. Copy the repository folder into `~/.codex/skills/verify-service-ready`.
3. Start a new Codex session.

## Example prompt
- Verify that the dashboard is actually running.
- Do not stop at code changes; prove the service is ready.
