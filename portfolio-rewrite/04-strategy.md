# Phase 5 — Portfolio strategy

**Goal:** Hire as **PM** (not SDE) at API-first / AI-native companies — with Mudrex as proof of platform + product shipping.

---

## 5a. Positioning (ranked)

| Rank | One-liner | Stop-scroll test |
|------|-----------|------------------|
| **1** | **Product Manager at Mudrex · I ship Futures API platforms (REST, WebSocket, MCP) and trading products (RexAlgo) on top of them.** | Names employer, domain, **two proof types** (platform + product). |
| 2 | Builder-PM for Mudrex Futures — SDK, realtime streams, MCP, and RexAlgo (algo + copy + advisory). | Clear; slightly long. |
| 3 | I turn Mudrex Futures APIs into integrator SDKs, AI tool surfaces (MCP), and retail trading products. | Strong wedge; less personal. |
| 4 | PM · crypto fintech · API platforms & algorithmic trading products. | Generic “PM · fintech”. |
| 5 | Full-Stack Product Builder \| Agentic-AI Builder | **Fails** — buzzwords, no user, indistinguishable. |

**Defense of #1:** A frontier PM reviewer asks “platform or app?” in 5 seconds. This line answers **both** without claiming multi-agent fantasies. It matches code: SDK/WS/MCP repos + RexAlgo monorepo.

**Retire:** “Full-Stack Product Builder | Build → Sell → Scale” and komarev/GIF/stack walls on the live profile (done in root `README.md`).

---

## 5b. Hero shortlist (portfolio story)

| # | Project | Role in story |
|---|---------|---------------|
| 1 | **RexAlgo** | “I own a shipped consumer product” — marketplace, copy, TIA, trust/safety, CI. |
| 2 | **mudrex-api-trading-python-sdk** (+ MCP) | “I define the integrator contract” — REST ergonomics, errors, agent tools. |
| 3 | **mudrex-proxy-server-websocket** | “I think about scale and cost under realtime load.” |
| 4 | **mudrex-mcp-prod-landing-page** | “I close the adoption loop for developers.” |
| 5 | **Mudrex-API-Copilot** | “I reduce support load with bounded AI on our own API.” |

**Not heroes for PM packet:** strategy bot sprawl, vendor forks (`ccxt`, `openalgo`), `workspace-monitor-bypass`.

---

## 5c. Cut list (unpin / archive / private)

| Repo | Action |
|------|--------|
| `ccxt`, `openalgo`, `awesome-llm-apps`, `evolution-api`, forks (`llm-council`, `RAG-Anything`, …) | Archive or unpublish |
| `workspace-monitor-bypass` | **Private/delete** |
| `web-design-knowledge-claude-code-skill` | Private (PDF licensing) |
| 6+ Mudrex+Bybit strategy bots | Archive all but one experimental |
| `funding-fee-farmer-v2`, `Price_alert_v5`, `BTC-HA-SuperTrend-5M-Strategy` | Archive |

---

## 5d. Gap fills (strategy B)

| Gap | Action | Status |
|-----|--------|--------|
| CI | Copy `gap-fill/ci-*.yml` to SDK + WS repos | Templates ready |
| CI RexAlgo | Already in repo | **Done** |
| Profile claims | Live `README.md` rewritten | **Done** |
| Multi-agent claim | Removed from profile | **Done** |
| Outcomes metrics | Fill `artifacts/outcomes-*.md` | `TODO[JM]` |
| RexAlgo visibility | Consider **public** readme or case study in profile for recruiters | Your call |

---

## 5e. Pin order (GitHub — 6 slots)

1. `RexAlgo`
2. `mudrex-api-trading-python-sdk`
3. `mudrex-proxy-server-websocket`
4. `mudrex-mcp-prod-landing-page`
5. `Mudrex-API-Copilot`
6. `mudrex-api-trading-SDK-registry` *(or `mudrex-trade-ideas-html-cards` if advisory story leads)*

---

## 5f. Voice rules (all drafts)

- Lead with **user + decision**, not stack.
- Metrics: real or “not measured” — never invented.
- One mermaid per hero max; profile gets one platform map.
- Tech notes at bottom of project READMEs only.
