# Phase 3 — PM artifact audit

**Generated:** 2026-05-27  
**Gap-close strategy (Phase 2):** **B** — add small, real commits/repos to substantiate claims (see `gap-fill/README.md`).  
**PM focus:** API (REST), WebSocket, MCP, algo trading, advisory — not hero-repo selection (you’ll attach those).  
**Method:** Searched cloned repos under `portfolio-rewrite/.repo-scan/` for PRD-shaped docs, decision logs, metrics, user-facing copy, roadmaps, post-mortems.

---

## Executive summary

| Artifact type | Found? | Quality for PM portfolio |
|---------------|--------|---------------------------|
| Formal PRD | **No** | — |
| ADR / decision log | **No** (named) | — |
| Design doc (product) | **Partial** | Copilot plans/analyses; not customer-facing spec |
| Post-mortem | **No** | — |
| User research / interviews | **No** | — |
| Roadmap / OKR / RICE | **No** (in product repos) | Only in fork `claude-code-pm-skills` |
| Metrics / before–after dashboards | **Partial** | Token cost math in plans; **no live usage metrics** |
| Changelog / release notes | **Yes** | SDK `CHANGELOG.md`; Copilot implicit in many MDs |
| In-app / GTM copy | **Partial** | MCP landing, trade-idea widgets, Telegram strings |
| Implementation / ops docs | **Strong** | READMEs, MCP setup, Railway, troubleshooting |

**Bottom line:** You have **strong builder documentation** and **implicit product reasoning** buried in engineering notes. What’s missing for a senior PM application is **decision records with alternatives rejected**, **user evidence**, and **honest outcome numbers** — those must be **authored by you** (Phase 7 templates), not inferred.

---

## Inventory by artifact type

### 1. PRDs (product requirements)

| Status | Location | Notes |
|--------|----------|-------|
| **Not found** | — | No `PRD.md`, `docs/prd/`, or requirements sections with user stories + acceptance criteria in API/WS/MCP/algo repos. |
| **Nearest substitute** | `Mudrex-API-Copilot/REDIS_CACHING_PLAN.md` | Problem/solution/cost analysis — reads as **engineering proposal**, not PRD. |
| **Nearest substitute** | `Mudrex-API-Copilot/MCP_INTEGRATION_BENEFITS.md` | Before/after user flows — good **raw material** for a PRD appendix. |
| **Nearest substitute** | `mudrex-api-trading-python-sdk/MCP_IMPLEMENTATION_SUMMARY.md` | Implementation retrospective, Jan 2026 — tool catalog, not user discovery. |

**Must-create-before-applying:** PRD for MCP launch, WS proxy (integrator persona), API Copilot (developer support), advisory trade-idea surface.

---

### 2. Decision logs / ADRs

| Status | Location | Notes |
|--------|----------|-------|
| **Not found** | — | No `docs/adr/`, `DECISIONS.md`, or “Decision / Status / Consequences” blocks. |
| **Implicit decisions in prose** | `mudrex-proxy-server-websocket/README.md` | Architecture (single Bybit upstream, Redis fan-out) — **not recorded as decisions with rejected alternatives**. |
| **Implicit** | `Mudrex-API-Copilot/GROUP_ONLY_CHANGES.md`, `GENERIC_BOT_CLARIFICATION.md` | Product scope changes — changelog style, not ADR. |
| **Git history** | All focus repos | Commit messages may contain decisions — **Phase 7** can extract via `decision-log-*.md` scaffolds. |

**Must-create-before-applying:** ADRs for: (1) MCP vs OpenAPI-only, (2) WS proxy vs client-direct Bybit, (3) Gemini-only copilot vs multi-LLM, (4) paper trading sandbox scope.

---

### 3. Design docs

| Repo | File | PM value |
|------|------|----------|
| `Mudrex-API-Copilot` | `CONTEXT_AWARENESS_ANALYSIS.md`, `CONTEXT_AWARENESS_IMPLEMENTATION.md` | Feature design for conversation context — **internal**. |
| `Mudrex-API-Copilot` | `RAG_HALLUCINATION_ANALYSIS.md`, `RAG_KNOWLEDGE_EXPLAINED.md` | Quality/safety design for doc bot — strong for **trust & safety** narrative. |
| `Mudrex-API-Copilot` | `SMART_RESPONSE_BEHAVIOR.md` | Trigger logic (tag vs API-keyword) — **product behavior spec**; cite in portfolio. |
| `Mudrex-API-Copilot` | `OUT_OF_CONTEXT_IMPROVEMENTS.md` | Scope boundaries — aligns with `pipeline.py` off-topic guard. |
| `mudrex-proxy-server-websocket` | `README.md` (mermaid) | System design — engineering doc, not UX design. |
| `mudrex-mcp-prod-landing-page` | `README.md` + `src/routes/index.tsx` | **GTM / information architecture** — closest to product design doc. |
| `mudrex-trade-ideas-html-cards` | `README.md` | Integration contract + Plotline states — **advisory UX spec (light)**. |

**Usable as-is (with rewrite):** `SMART_RESPONSE_BEHAVIOR.md`, `MCP_INTEGRATION_BENEFITS.md`, MCP landing structure.

---

### 4. Post-mortems

| Status | Notes |
|--------|-------|
| **Not found** | No incident write-ups, SEV timelines, or “what broke in prod” docs in focus repos. |
| **Near-miss** | `Mudrex-API-Copilot/RAG_HALLUCINATION_ANALYSIS.md` — quality incident **analysis**, not post-mortem format. |
| `mudrex-api-trading-python-sdk` | `BUG_FIXES.md`, `SDK_FIXES_SUMMARY.md`, `PAGINATION_FIX.md` | Fix logs — could be mined for **learning** sections, not formal PM post-mortems. |

**Must-create-before-applying:** One post-mortem you’re willing to share (WS outage, copilot bad answer, API incident) — anonymized.

---

### 5. User research / interview summaries

| Status | Notes |
|--------|-------|
| **Not found** | No interview notes, survey results, or “5 developers said…” in repo. |
| **Proxy evidence** | `Mudrex-API-Copilot/TROUBLESHOOTING.md`, `WHAT_BOT_CAN_FETCH.md` | Suggests **support-driven** requirements — source unknown in git. |

**Must-create-before-applying:** 1–2 paragraphs per product: who you talked to (role), what pain, what you shipped — **only if true**.

---

### 6. Roadmaps / strategy

| Status | Notes |
|--------|-------|
| **Not found** in Mudrex platform repos | |
| **Fork only** | `claude-code-pm-skills` — RICE/OKR **templates**, not your roadmap. |
| **Planning doc** | `Mudrex-API-Copilot/REDIS_CACHING_PLAN.md` | Cost-reduction roadmap — engineering-led. |

**Must-create-before-applying:** One-quarter roadmap snippet (MCP v2, WS streams, advisory) — even bullet form.

---

### 7. Metrics / before–after analyses

| Location | What it contains | Portfolio-ready? |
|----------|------------------|------------------|
| `Mudrex-API-Copilot/REDIS_CACHING_PLAN.md` | Estimated tokens/query, $/day **assumptions** (e.g. 1000 queries/day) | **Hypothetical** — label as model, not measured. |
| `Mudrex-API-Copilot/MCP_INTEGRATION_BENEFITS.md` | Qualitative before/after flows | Good narrative; **no numbers**. |
| GitHub API | Stars/forks on SDK, bots | Weak usage signal (★3 on python SDK). |
| **Absent** | DAU, messages/day, WS connections, error rates, support ticket deflection | **Critical gap** for PM credibility |

**Must-create-before-applying:** `outcomes-*.md` per product (Phase 7) — you fill real numbers or “not measured.”

---

### 8. User-facing copy & changelog

| Repo | Artifact | Type |
|------|----------|------|
| `mudrex-api-trading-python-sdk` | `CHANGELOG.md` | Release changelog (Keep a Changelog) — **MCP launch Jan 2026** |
| `mudrex-api-trading-python-sdk` | `MCP_SETUP.md`, `MCP_QUICK_REFERENCE.md` | Developer onboarding copy |
| `mudrex-api-trading-SDK-registry` | `README.md` | Multi-SDK positioning, install matrix |
| `mudrex-mcp-prod-landing-page` | `src/routes/index.tsx` | Hero, FAQ, Claude config snippets, API key UX |
| `mudrex-trade-ideas-html-cards` | Widget HTML + README | Risk pill, milestone labels, CTA deeplink copy |
| `Mudrex-API-Copilot` | `src/rag/pipeline.py` L74, L62–75 | Bot redirect strings (“ask me about the API”) |
| `Mudrex-API-Copilot` | `TROUBLESHOOTING.md` | Support macros / error explanations |
| `telegram-volume-alert-bot` | `README.md` (long) | Ops alert copy — support domain, not API core |

---

## Focus-repo matrix (API / WS / MCP / algo / advisory)

| Repo | PRD | ADR | Design | Metrics | Changelog | Copy/GTM | Overall |
|------|-----|-----|--------|-----------|-----------|----------|---------|
| `mudrex-api-trading-python-sdk` | — | — | — | — | ✓ | ✓ README/MCP | **Eng docs** |
| `mudrex-proxy-server-websocket` | — | — | ✓ README arch | — | — | ✓ ops | **Eng docs** |
| `mudrex-mcp-prod-landing-page` | — | — | ✓ UI | — | — | ✓✓ | **Best GTM artifact** |
| `Mudrex-API-Copilot` | ~plan | — | ✓✓ many MDs | ~estimated | — | ✓ behavior | ** Richest, messy** |
| `mudrex-futures-API-papertrading-py-sdk` | — | — | — | — | — | ✓ OpenAPI desc | **Demo surface** |
| `mudrex-api-trading-SDK-registry` | — | — | — | — | — | ✓ index | **Meta only** |
| `mudrex-trade-ideas-html-cards` | — | — | ✓ widget states | — | — | ✓ | **Advisory UI** |
| `XAUT-EMA-Pullback-Strategy` | — | — | ✓ README filters | — | — | — | **Algo spec in README** |
| `free-weight-strategy-mudrex-api` | — | — | ✓ mermaid | — | — | — | **Algo** |
| `funding-fee-farming-strategy` | — | — | partial | — | — | — | **Thesis drift risk** |

---

## Copilot doc sprawl (21 root markdown files)

**Problem for PM reviewers:** `Mudrex-API-Copilot` reads like an **internal wiki**, not a curated product story.

| File | Suggested portfolio use |
|------|-------------------------|
| `MCP_INTEGRATION_BENEFITS.md` | **Keep** → PRD appendix (before/after) |
| `SMART_RESPONSE_BEHAVIOR.md` | **Keep** → behavior spec |
| `REDIS_CACHING_PLAN.md` | **Summarize** → cost/performance decision (verify numbers) |
| `RAG_HALLUCINATION_ANALYSIS.md` | **Keep** → quality/risk section |
| `RAILWAY_*.md`, `ACTUAL_SETUP.md`, `QUICK_SETUP_GUIDE.md` | **Hide** from portfolio → ops only |
| `PULL_REQUEST.md` | **Internal** — not for hiring packet |

**Recommendation:** Publish one `docs/PRODUCT.md` in that repo (or link from portfolio) that **links** to 3–4 of the above; archive the rest from pinned view.

---

## Must-create-before-applying (prioritized)

Aligned with **B** (real commits) + your PM domains:

| Priority | Artifact | Target product | Action |
|----------|----------|----------------|--------|
| P0 | **Outcomes sheet** | MCP + WS + SDK | Fill `artifacts/outcomes-*.md` (Phase 7) with real or “not measured” |
| P0 | **ADR-001** | WS proxy | Why single upstream + Redis, not per-client Bybit |
| P0 | **ADR-002** | MCP | Why MCP tools vs docs-only copilot |
| P1 | **PRD excerpt** | API Copilot | User: Futures API integrator; jobs-to-be-done |
| P1 | **PRD excerpt** | Advisory widgets | User: mobile app reader; Plotline embed |
| P1 | **CI workflow** | SDK + proxy | `gap-fill/` templates → commit to product repos |
| P2 | **Post-mortem** | Any prod incident | One page, anonymized |
| P2 | **Profile README** | `DecentralizedJM` | Remove false claims per `01-skill-map.md` Table B |

---

## What you can promote without inventing

These exist today and are **honest** if framed correctly:

1. **MCP launch narrative** — `CHANGELOG.md` + `MCP_IMPLEMENTATION_SUMMARY.md` (Jan 2026, 20 tools).  
2. **Integrator before/after** — `MCP_INTEGRATION_BENEFITS.md` (qualitative).  
3. **Support bot behavior spec** — `SMART_RESPONSE_BEHAVIOR.md` + code guard in `src/rag/pipeline.py`.  
4. **Cost-awareness** — `REDIS_CACHING_PLAN.md` (**label as estimate**).  
5. **Advisory embed contract** — `mudrex-trade-ideas-html-cards/README.md` (TIA JSON → widget states).  
6. **Platform index** — `mudrex-api-trading-SDK-registry/README.md`.

---

## Phase 3 question (one)

For your **API / WebSocket / MCP / algo / advisory** work at Mudrex, which products can you supply **real PM artifacts** from private notes or memory (even rough)?

Reply with any combination, e.g.:

- `SDK + MCP launch` — PRD + launch metrics  
- `WS proxy` — ADR + connection counts  
- `API Copilot` — support interviews + deflection rate  
- `Trade ideas / advisory` — stakeholder brief + adoption  
- `Algo` — strategy mandate + risk limits (not PnL unless you’re willing)

Anything you list, Phase 7 will format into `artifacts/prd-*.md`, `decision-log-*.md`, `outcomes-*.md` with `TODO[JM]:` blocks only where you must fill facts.
