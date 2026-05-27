# PRD scaffold — RexAlgo (inferred from code; verify)

> **Status:** Draft for JM completion. Do not treat as historical PRD.

## Problem

`TODO[JM]:` Who cannot succeed today without RexAlgo? (masters / subscribers / Mudrex business)

Retail traders want vetted strategies on Mudrex Futures without custom infrastructure. Masters need subscriber mirroring with trust boundaries (subscriber-owned API keys).

## Users

| Persona | Job to be done |
|---------|----------------|
| **Subscriber** | Subscribe to a strategy; mirror trades safely |
| **Master** | Publish strategy; send signed signals; see aggregate stats |
| **Admin** | Review strategies before public listing |
| `TODO[JM]:` Sub-broker persona if applicable |

## Goals (from shipped product)

1. Algo marketplace + copy trading on Mudrex Futures
2. HMAC webhook ingress with idempotency
3. Strategy review workflow (`draft` → `approved`)
4. TIA trade-idea integration + optional auto-trade
5. TradingView user webhooks

## Non-goals (from `repo/project.json` roadmap.outOfScope)

- Non-Mudrex execution venues

## Requirements (evidence-backed)

| ID | Requirement | Source |
|----|-------------|--------|
| R1 | Subscriber funds stay on subscriber Mudrex account | `CONTEXT.md` domain model |
| R2 | Webhook signatures `X-RexAlgo-Signature` | `copyWebhookHmac.ts` |
| R3 | Mudrex rate limits mirrored per futures/wallet tier | `mudrexRateLimit.ts` |
| R4 | Server-backed sessions + encrypted API secrets | `SECURITY.md`, schema |
| R5 | CI + load-test gate for prod | `.github/workflows/ci.yml`, `LOAD-TEST.md` |

## Success metrics

`TODO[JM]:` all numeric targets

## Open questions (from audit)

See `docs/audit/FINDINGS.md` Q1–Q6 — ledger, rollup, leverage capture.
