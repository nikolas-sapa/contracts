# Security Policy

> Phase 1 of the stalled docs bulk PR #1 (Dec 2025): minimal docs/CI slice only.
> No contract changes here.

## Supported Versions

Only `main` (currently at `a8d7d2a`) receives security fixes.
Audited deployments are pinned per release; see `deployments/`.

## Audit History

All reports are versioned in [`audits/`](./audits/):

| Date | Auditor | Report |
|------|---------|--------|
| 2023-11 | CoinFabrik | [`CoinFabrik-2023-11.pdf`](./audits/CoinFabrik-2023-11.pdf) |
| 2024-11 | Clarity Alliance | [`ClarityAlliance-2024-11.pdf`](./audits/ClarityAlliance-2024-11.pdf) |
| 2025-01 | Clarity Alliance | [`ClarityAlliance-2025-01.pdf`](./audits/ClarityAlliance-2025-01.pdf) |
| 2025-06 | Clarity Alliance | [`ClarityAlliance-2025-06.pdf`](./audits/ClarityAlliance-2025-06.pdf) |

Scope notes (incl. stSTXbtc, see `feat: stSTXbtc contracts and audit`) are inside each PDF.

## Reporting a Vulnerability

**Do not open a public issue.**

1. Use GitHub **Security > Report a vulnerability** (private advisory) on
   `StackingDAO/contracts`, or contact the maintainer (`nieldeckx`) directly.
2. Include: affected contract(s) + commit hash, reproduction steps
   (`clarinet console` / `npm test` case), and impact assessment.
3. Allow reasonable time for triage — this repo has a single maintainer
   and review can be slow.

## CI

Pushes and PRs run the Clarinet/vitest suite via
[`.github/workflows/test.yml`](./.github/workflows/test.yml)
(`npm ci` + `npm test`). A green run is required before any fix merges.
