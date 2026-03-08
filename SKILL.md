---
name: verify-service-ready
description: Use when about to claim a dashboard, service, or code change is complete and you need evidence from tests, builds, API health checks, and running-state confirmation before handoff.
---

# Verify Service Ready

## Overview
Do not say ?done? from code inspection alone. Verify behavior from the narrowest relevant tests outward, then confirm the live service really starts and answers requests.

## Quick Reference
- Run targeted tests for the touched area first.
- Run the broader relevant suite before handoff.
- Build the frontend or package artifacts if UI code changed.
- Start the service and verify real HTTP endpoints return `200`.
- Report engine, model, and runtime state from live status data.

## Workflow
1. Run the most relevant tests that cover the changed logic.
2. Expand to the broader service or dashboard suite.
3. Build the frontend if bundles changed.
4. Start or restart the service.
5. Verify `/`, `/api/status`, and any critical API endpoints.
6. Hand back concrete evidence, not guesswork.

## Red Flags
- ?The code looks right, so it should work.?
- ?I built it once earlier, no need to rebuild.?
- ?The server probably started.?
- ?I did not check the HTTP endpoints.?

## Common Mistakes
- Claiming a fix before the service returns `200`.
- Running only unit tests when the failure is in runtime wiring.
- Forgetting to include build results in the handoff.
- Reporting a model or provider from memory instead of live status.

## Example
Use when the user says: ??????????, ?????????????, or ????????????????.
