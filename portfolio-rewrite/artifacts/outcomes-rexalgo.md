# Outcomes — RexAlgo

> **Source:** https://github.com/DecentralizedJM/RexAlgo — product facts from README/`CONTEXT.md`; metrics **only** from you.

## Product (verified in repo)

- **What:** Algo marketplace + copy trading on **Mudrex Futures**; masters publish strategies, subscribers mirror HMAC-signed signals to their own Mudrex accounts.
- **Also:** TIA (trade ideas) auto-trade path, TradingView webhooks, master/sub-broker dashboards.
- **Stack:** Vite/React + Next.js API + Postgres (Drizzle) + optional Redis + Docker/Vercel/Railway.
- **Quality bar:** CI (`.github/workflows/ci.yml`), `docs/LOAD-TEST.md`, `SECURITY.md`, `docs/audit/` with explicit open decisions.

## Metrics (fill or write “not measured / not shared publicly”)

| Metric | Value | Period | Source |
|--------|-------|--------|--------|
| Registered users | `TODO[JM]:` | | |
| Active subscribers (copy/algo) | `TODO[JM]:` | | |
| Approved strategies (masters) | `TODO[JM]:` | | |
| Webhook signals / day | `TODO[JM]:` | | |
| Mirrored orders / day | `TODO[JM]:` | | |
| TIA auto-executions | `TODO[JM]:` | | |
| Production URL | `TODO[JM]:` e.g. rexalgo.xyz | | |
| Incidents / SEVs | `TODO[JM]:` | | |

## Qualitative outcomes

`TODO[JM]:` 2–4 bullets — e.g. review workflow for strategies, rate-limit design vs Mudrex caps, Telegram mini-app, launch on Vercel+Railway.

## Decisions worth citing (already in repo — expand in interview)

- Mudrex **futures vs wallet** rate-limit buckets (`mudrexRateLimit.ts`).
- Webhook replay window reduced to 60s (`copyWebhookHmac.ts` header comment).
- Volume ledger / master–sub-broker rollup — open decisions in `docs/audit/FINDINGS.md`.

## Evidence links

- Repo: https://github.com/DecentralizedJM/RexAlgo  
- Architecture: `docs/CONTEXT.md`, `repo/architecture.mmd`
