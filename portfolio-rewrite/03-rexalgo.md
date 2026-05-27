# RexAlgo — product profile (scanned)

**Repo:** https://github.com/DecentralizedJM/RexAlgo  
**Last commit (local clone):** 2026-05-27  
**Visibility:** Likely **private** (not returned in unauthenticated `DecentralizedJM` public repo list; clone succeeds with your access).  
**Classification:** **HERO** — flagship full-stack product for algo + copy trading + advisory (TIA) on Mudrex Futures.

---

## What it is (from code + README)

**RexAlgo** is a proprietary, source-available platform for:

- **Algo marketplace** — masters publish `algo` strategies; subscribers mirror signed signals into **their own** Mudrex accounts.
- **Copy trading** — `copy_trading` listings with webhook or **manual** copy (`manualCopyPoller.ts`).
- **Advisory (TIA)** — integration with **Project TIA** trade ideas (`backend/src/lib/tia/*`, `tia_active_ideas`, auto-executor).
- **TradingView** — user-owned TV webhooks → adapter → orders.

**Stack:** Vite/React SPA (`frontend/`) · Next.js API-only (`backend/`) · PostgreSQL + Drizzle · optional **Redis** (distributed rate limits) · Docker · Vercel + Railway.

**Executive summary (README L7–16):** Marketplace + copy trading on Mudrex Futures; Google OAuth (+ optional Telegram); HMAC webhooks; encrypted Mudrex API secrets; k6 load-test suite; 83 backend tests cited in `docs/CONTEXT.md`.

---

## How RexAlgo connects to your other public work

| Public repo | Relationship |
|-------------|----------------|
| `mudrex-api-trading-python-sdk` | Same Mudrex Futures API surface RexAlgo calls server-side |
| `mudrex-proxy-server-websocket` | Market-data rail (RexAlgo README emphasizes REST execution; WS proxy is platform sibling) |
| `mudrex-mcp-prod-landing-page` / MCP | Agent/developer rail; RexAlgo is **retail/master–subscriber** product |
| `mudrex-trade-ideas-html-cards` | Plotline embed widgets; RexAlgo **consumes TIA API** in-app (`tia/client.ts`) |
| Strategy bots (`XAUT-*`, `free-weight-*`, …) | Personal/experimental bots; RexAlgo is **production product** with review gates |

---

## PM-relevant evidence (file citations)

| Theme | Evidence |
|-------|----------|
| **Mudrex REST + rate limits** | `backend/src/lib/mudrexRateLimit.ts:L1-L58` — futures vs wallet tiers, sliding windows, Redis-backed option |
| **Webhook security** | `backend/src/lib/copyWebhookHmac.ts:L1-L50` — `X-RexAlgo-Signature`, replay window, env tuning |
| **Copy mirror** | `backend/src/lib/copyMirror.ts` (subscriber mirroring pipeline) |
| **Domain / data model** | `docs/CONTEXT.md:L26-L66` — strategies, subscriptions, review status, copy modes |
| **Advisory / TIA** | `backend/src/lib/tia/client.ts:L1-L40`; schema tables in `CONTEXT.md` L41-L46 |
| **Sessions & trust** | `SECURITY.md`, `docs/PROD.md`, `user_sessions` in `CONTEXT.md` |
| **CI (strategy B gap)** | `.github/workflows/ci.yml` — lint, audit, backend tests |
| **Load / prod readiness** | `docs/LOAD-TEST.md`, `npm run load:prod-readiness*` |
| **Ops / incident** | `docs/PROD.md` playbook; `docs/audit/FINDINGS.md` — explicit **decision required** items |

---

## PM artifacts found in-repo (not invented)

| Type | Found? | Where |
|------|--------|-------|
| Formal PRD | No | — |
| ADR (named) | Partial | `docs/audit/FINDINGS.md` — “Decision required” (volume ledger, rollups) |
| Design / architecture | **Strong** | `docs/CONTEXT.md`, `repo/architecture.mmd`, README mermaid index |
| Roadmap | **Yes** | `README.md#roadmap`, `repo/project.json` |
| Changelog | **Yes** | `CHANGELOG.md` |
| Security model | **Yes** | `SECURITY.md` |
| Metrics | **Partial** | Master dashboard aggregates (subscribers, volume) — **no public MAU in repo** |
| User research | No | — |

**Portfolio use:** Lead with README executive summary + `CONTEXT.md` domain table + one webhook diagram; link audit decisions as “how I document trade-offs under shipping pressure.”

---

## README quality

**Score: 5/5** for a senior reviewer — executive summary, feature matrix, diagram index, ops links, proprietary license clarity. **Risk:** length (~635 lines); portfolio should **link**, not paste.

---

## Scan checklist

| Item | Status |
|------|--------|
| GitHub repo | ✓ `DecentralizedJM/RexAlgo` |
| PM scope | Algo marketplace, copy trading, TIA advisory, Mudrex API platform consumer |
| Hero / case study | **Yes** — anchor product for “PM who ships” |
| Outcomes stub | `artifacts/outcomes-rexalgo.md` — fill metrics |
| Phase 7 PRD/decision-log | Ready to scaffold from `CONTEXT.md` + git history + `docs/audit/` |

---

## Suggested pin order (profile)

Place **RexAlgo first or second** among pins — it is the only repo that reads as a **shipped consumer product**, not a library or bot sketch.

1. `RexAlgo`  
2. `mudrex-api-trading-python-sdk` or `mudrex-mcp-prod-landing-page`  
3. `mudrex-proxy-server-websocket`  
4. `Mudrex-API-Copilot`  
5. `mudrex-trade-ideas-html-cards` (advisory surface)  
6. SDK registry or paper SDK
