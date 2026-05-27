# Phase 1 — Repository inventory

**Generated:** 2026-05-27  
**Method:** Shallow-cloned all repos listed on `https://api.github.com/users/DecentralizedJM/repos` (55 repos). LOC = non-vendor lines in common code extensions (includes markdown). Classifications from README + entry-point source review.
### Access note
- **Private repos:** Unauthenticated GitHub API returned **55 public repos, 0 private**. If you have private repos not in this list, they were **not scanned** — share names and we can extend this inventory.
- **Evidence:** Stars/forks from API. Issues/traffic/clones not available without authenticated `gh`.
- **LOC caveat:** `ccxt`, `openalgo`, `awesome-llm-apps`, `evolution-api` inflate totals — treat their LOC as vendor mirror noise.

---

| Repo | Public/Private | Last commit | Approx LOC | Primary language(s) | What it actually does (from code) | Evidence of usage | README (1–5) | Classification |
|------|----------------|-------------|------------|---------------------|-----------------------------------|-------------------|--------------|----------------|
| [AI-Intern-for-twitter-support](https://github.com/DecentralizedJM/AI-Intern-for-twitter-support) | Public | 2025-11-27 | 6,994 | md:5077, py:1615, sh:167, json:135 | Mudrex **X/Twitter support** pipeline: monitor → Gemini classify → templated reply/escalate → Slack (`twitter_monitor.py`, `gemini_handler.py`). | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [BTC-HA-SuperTrend-5M-Strategy](https://github.com/DecentralizedJM/BTC-HA-SuperTrend-5M-Strategy) | Public | 2026-05-25 | 610 | py:557, md:53 | Single-file Binance/ccxt bot; README has hardcoded `/Users/decnetralizedjm/...` paths; not Mudrex. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |
| [BTC-momentum-catcher-strategy](https://github.com/DecentralizedJM/BTC-momentum-catcher-strategy) | Public | 2026-03-07 | 819 | py:736, md:61, json:22 | TradingView port: Bybit WS + Mudrex executor (`bot.py`). | ★0 · forks 0 · original | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **EXPERIMENT** |
| [BridgeLife](https://github.com/DecentralizedJM/BridgeLife) | Public | 2026-03-28 | 13,224 | json:9488, tsx:2574, ts:548, css:309 | **LifeBridge** consumer app: multimodal → Gemini domain cards + Firestore family rooms — side project, naming drift vs PromptWar. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **EXPERIMENT** |
| [DecentralizedJM](https://github.com/DecentralizedJM/DecentralizedJM) | Public | 2026-03-19 | 61 | md:61 | GitHub **profile README** only in clone: stack walls, komarev counter, GIF — the live portfolio surface to rewrite. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SCAFFOLDING** |
| [Mudrex-API-Copilot](https://github.com/DecentralizedJM/Mudrex-API-Copilot) | Public | 2026-03-06 | 24,620 | py:13658, md:10882, json:66, sh:14 | **Telegram API copilot** for Mudrex Futures devs: RAG (Qdrant/Gemini), Redis cache, MCP market tools (`main.py`, `src/bot/telegram_bot.py`, `src/rag/pipeline.py`). | ★1 · forks 0 · original | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **HERO** |
| [Mudrex-Supertrend-ATR-Strategy-Bot](https://github.com/DecentralizedJM/Mudrex-Supertrend-ATR-Strategy-Bot) | Public | 2026-02-12 | 10,614 | py:9730, md:884 | Supertrend+ATR Mudrex bot with **vendored SDK copy** inside repo. | ★1 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **EXPERIMENT** |
| [Perp-Funding-Rate-Alert-Telegram-Bot](https://github.com/DecentralizedJM/Perp-Funding-Rate-Alert-Telegram-Bot) | Public | 2026-01-10 | 2,507 | py:2284, md:166, sh:32, yml:14 | Funding settlement/extreme alerts to Telegram. | ★0 · forks 1 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [Price_alert_v5](https://github.com/DecentralizedJM/Price_alert_v5) | Public | 2026-01-31 | 3,222 | py:3222 | **GitHub fork** of a Bybit price-alert bot; **no README** in shallow clone; not Mudrex-branded. | ★0 · forks 0 · fork · upstream fork | 1 — Missing or stub README | **ARCHIVE_OR_DELETE** |
| [RAG-Anything](https://github.com/DecentralizedJM/RAG-Anything) | Public | 2025-12-31 | 16,367 | py:12479, md:3867, yaml:21 | Fork of **HKUDS/RAG-Anything** — multimodal RAG research framework on LightRAG. | ★0 · forks 0 · fork · upstream fork | 3 — Solid technical docs; weak PM framing | **ARCHIVE_OR_DELETE** |
| [SMC-Algo-trading](https://github.com/DecentralizedJM/SMC-Algo-trading) | Public | 2026-01-08 | 1,734 | py:1607, json:60, md:52, sh:15 | ICT/SMC order-block bot — thin README. | ★0 · forks 0 · original | 2 — Install/quickstart only; no product story | **EXPERIMENT** |
| [Ultimate-Trend-Strategy](https://github.com/DecentralizedJM/Ultimate-Trend-Strategy) | Public | 2026-02-11 | 5,527 | py:5272, yaml:193, md:62 | 13+ indicator trend bot + news filter. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **EXPERIMENT** |
| [Work-Productivity-Tracker](https://github.com/DecentralizedJM/Work-Productivity-Tracker) | Public | 2025-11-24 | 883 | py:587, md:268, yaml:28 | Logseq → Gemini monthly reports. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **EXPERIMENT** |
| [XAUT-EMA-Pullback-Strategy](https://github.com/DecentralizedJM/XAUT-EMA-Pullback-Strategy) | Public | 2026-03-17 | 3,256 | py:3021, md:235 | **Quant bot:** 11-filter EMA pullback on XAUT + RF P(win) gate, Bybit klines + Mudrex execution (`bot_institutional.py`, `strategy/institutional_ml.py`). | ★1 · forks 1 · original | 4 — Strong ops/setup; long or changelog-heavy | **HERO** |
| [adk-redis](https://github.com/DecentralizedJM/adk-redis) | Public | 2026-02-01 | 11,468 | py:7891, md:2769, sh:457, json:259 | Fork of **redis-applied-ai/adk-redis** — Google ADK + Redis memory. | ★0 · forks 0 · fork · upstream fork | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |
| [almabase-auction-wire](https://github.com/DecentralizedJM/almabase-auction-wire) | Public | 2025-11-27 | 12,418 | json:7164, tsx:4455, ts:487, md:127 | Almabase Silent Auction **discovery wireframe**. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **EXPERIMENT** |
| [antigravity-claude-proxy](https://github.com/DecentralizedJM/antigravity-claude-proxy) | Public | 2025-12-30 | 7,349 | js:5422, json:1427, md:500 | Fork of **badri-s2001/antigravity-claude-proxy** — Node Antigravity→Claude proxy. | ★0 · forks 0 · fork · upstream fork | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |
| [antigravity-proxy-claude-py-sdk](https://github.com/DecentralizedJM/antigravity-proxy-claude-py-sdk) | Public | 2026-01-01 | 5,163 | py:4757, md:406 | **Your** Python SDK for Antigravity proxy (async, streaming, tool calling) — original wrapper. | ★1 · forks 0 · original | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **SUPPORTING** |
| [awesome-llm-apps](https://github.com/DecentralizedJM/awesome-llm-apps) | Public | 2025-11-21 | 113,593 | py:56772, js:19188, md:19045, yaml:6126 | Vendor/curated mirror of **Shubhamsaboo/awesome-llm-apps** — tutorial collection, not a shipped system. | ★0 · forks 0 · fork · upstream fork | 3 — Solid technical docs; weak PM framing | **ARCHIVE_OR_DELETE** |
| [bitbot](https://github.com/DecentralizedJM/bitbot) | Public | 2025-12-10 | 190 | md:97, py:93 | BTC price Telegram bot with milestone alerts. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SCAFFOLDING** |
| [ccxt](https://github.com/DecentralizedJM/ccxt) | Public | 2026-03-25 | ~5160k (vendor) | php:985758, go:817094, py:809673, cs:763775 | Vendor mirror of **ccxt/ccxt** (~5M LOC counted). Unified exchange library — not your implementation. | ★0 · forks 0 · fork · upstream fork | 2 — Install/quickstart only; no product story | **ARCHIVE_OR_DELETE** |
| [claude-code-pm-skills](https://github.com/DecentralizedJM/claude-code-pm-skills) | Public | 2026-03-18 | 1,977 | md:1977 | Fork of **Mehdibargach/claude-code-pm-skills** — 20 markdown PM slash skills; useful signal for PM targeting but not your authorship. | ★0 · forks 0 · fork · upstream fork | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **SUPPORTING** |
| [competitor-perp-volume-fetcher-bot](https://github.com/DecentralizedJM/competitor-perp-volume-fetcher-bot) | Public | 2026-02-20 | 1,436 | py:1357, md:79 | Telegram competitive perp volume (`volume_bot.py`). | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SUPPORTING** |
| [evolution-api](https://github.com/DecentralizedJM/evolution-api) | Public | 2025-10-29 | 56,544 | ts:31909, json:17630, sql:4182, md:1991 | Vendor mirror of **EvolutionAPI/evolution-api** — WhatsApp API platform. | ★0 · forks 0 · fork · upstream fork | 2 — Install/quickstart only; no product story | **ARCHIVE_OR_DELETE** |
| [free-weight-strategy-mudrex-api](https://github.com/DecentralizedJM/free-weight-strategy-mudrex-api) | Public | 2026-02-13 | 4,705 | py:4135, md:484, yaml:86 | Multi-indicator confluence bot (Bybit WS + Mudrex). | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **EXPERIMENT** |
| [freshdesk-python-scraper](https://github.com/DecentralizedJM/freshdesk-python-scraper) | Public | 2026-02-07 | 900 | py:826, md:74 | Freshdesk scrape → optional LLM filter → Excel/Telegram. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SUPPORTING** |
| [funding-fee-farmer-v2](https://github.com/DecentralizedJM/funding-fee-farmer-v2) | Public | 2026-03-07 | 2,292 | py:1415, md:877 | Older bot enters *before* settlement to collect funding fees — **superseded** by `funding-fee-farming-strategy` v4 thesis. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |
| [funding-fee-farming-strategy](https://github.com/DecentralizedJM/funding-fee-farming-strategy) | Public | 2026-03-11 | 3,807 | py:3325, md:457, yml:14, json:11 | Live strategy bot v4: **post-settlement momentum** on extreme funding (`src/strategy_engine.py`) — description still says 'farm fees'. | ★2 · forks 1 · original | 4 — Strong ops/setup; long or changelog-heavy | **EXPERIMENT** |
| [ghostlink-tracker](https://github.com/DecentralizedJM/ghostlink-tracker) | Public | 2026-03-22 | 10,823 | json:10048, js:426, css:206, md:143 | Marketing **link tracker** with geo IP + Next.js dashboard + Express/SQLite. | ★1 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [llm-council](https://github.com/DecentralizedJM/llm-council) | Public | 2025-11-22 | 6,223 | json:3788, py:818, css:597, jsx:556 | Fork of **karpathy/llm-council** — multi-model peer-review chat UI. | ★0 · forks 0 · fork · upstream fork | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |
| [mudrex-api-trading-SDK-registry](https://github.com/DecentralizedJM/mudrex-api-trading-SDK-registry) | Public | 2025-12-31 | 441 | md:441 | **Docs index only** — README matrix pointing to SDK repos; no runtime. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SUPPORTING** |
| [mudrex-api-trading-dotnet-sdk](https://github.com/DecentralizedJM/mudrex-api-trading-dotnet-sdk) | Public | 2025-12-31 | 1,565 | cs:1226, md:339 | C# Mudrex client port. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SUPPORTING** |
| [mudrex-api-trading-go-sdk](https://github.com/DecentralizedJM/mudrex-api-trading-go-sdk) | Public | 2025-12-31 | 1,331 | go:1122, md:209 | Go Mudrex REST client port (`client.go`). | ★0 · forks 0 · original | 2 — Install/quickstart only; no product story | **SUPPORTING** |
| [mudrex-api-trading-java-sdk](https://github.com/DecentralizedJM/mudrex-api-trading-java-sdk) | Public | 2025-12-31 | 1,533 | java:1320, md:213 | Java Mudrex client port. | ★0 · forks 1 · original | 2 — Install/quickstart only; no product story | **SUPPORTING** |
| [mudrex-api-trading-nodejs-sdk](https://github.com/DecentralizedJM/mudrex-api-trading-nodejs-sdk) | Public | 2025-12-31 | 1,258 | ts:802, md:389, json:67 | TypeScript Mudrex client port (`src/client.ts`). | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SUPPORTING** |
| [mudrex-api-trading-python-sdk](https://github.com/DecentralizedJM/mudrex-api-trading-python-sdk) | Public | 2026-01-20 | 9,066 | py:7395, md:1671 | **Python SDK + MCP** for Mudrex Futures REST: rate-limited `MudrexClient`, modular wallet/orders/positions (`mudrex/client.py`, `mudrex/mcp/server.py`). | ★3 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **HERO** |
| [mudrex-futures-API-papertrading-py-sdk](https://github.com/DecentralizedJM/mudrex-futures-API-papertrading-py-sdk) | Public | 2026-01-15 | 14,612 | py:12495, md:2105, yml:12 | Paper-trading fork of Python SDK + FastAPI/OpenAPI + MCP for ChatGPT demos. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SUPPORTING** |
| [mudrex-futures-volume-fees-calculator](https://github.com/DecentralizedJM/mudrex-futures-volume-fees-calculator) | Public | 2026-01-30 | 901 | py:811, md:85, sh:5 | CLI/library for futures volume + fee tier from order history. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SCAFFOLDING** |
| [mudrex-markprice-bot](https://github.com/DecentralizedJM/mudrex-markprice-bot) | Public | 2026-03-15 | 388 | py:278, md:110 | Telegram `/mark` for Bybit mark-price klines (`bot.py`, `mark_price_client.py`). | ★1 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [mudrex-mcp-prod-landing-page](https://github.com/DecentralizedJM/mudrex-mcp-prod-landing-page) | Public | 2026-05-25 | 16,731 | json:10396, tsx:5512, ts:395, css:250 | **MCP product landing** on Cloudflare: API key UX, tool catalog, Claude config (`src/routes/index.tsx`, `wrangler.jsonc`). | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **HERO** |
| [mudrex-proxy-server-websocket](https://github.com/DecentralizedJM/mudrex-proxy-server-websocket) | Public | 2026-02-09 | 4,058 | py:3395, md:659, sh:4 | **Production WS proxy:** one Bybit V5 upstream → transform to Mudrex streams → Redis pub/sub → fan-out (`app/standalone_server.py`, `app/upstream/transformer.py`). | ★0 · forks 0 · original | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **HERO** |
| [mudrex-telegram-intern](https://github.com/DecentralizedJM/mudrex-telegram-intern) | Public | 2025-11-24 | 1,866 | md:672, ts:584, tsx:491, json:73 | **Community mod bot:** Gemini structured JSON (reply/warn), 3-tier scam filter, rate limits (`bot/index.ts`, `services/geminiService.ts`). | ★0 · forks 0 · original | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **HERO** |
| [mudrex-trade-ideas-html-cards](https://github.com/DecentralizedJM/mudrex-trade-ideas-html-cards) | Public | 2026-05-27 | 2,125 | html:2021, md:104 | Plotline HTML embed widgets for trade-idea cards — integration asset. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SCAFFOLDING** |
| [night-watchman-telegram-bot](https://github.com/DecentralizedJM/night-watchman-telegram-bot) | Public | 2026-01-31 | 10,307 | py:9107, md:1200 | **Telegram moderation superbot:** regex → ML TF-IDF ensemble → Gemini → HF zero-shot; mercy/ban engine (`night_watchman.py`, `decision_engine.py`). | ★0 · forks 2 · original | 4 — Strong ops/setup; long or changelog-heavy | **HERO** |
| [openalgo](https://github.com/DecentralizedJM/openalgo) | Public | 2026-05-21 | ~506k (vendor) | py:296777, md:100794, tsx:69638, json:18130 | Vendor mirror of **marketcalls/openalgo** (~506k LOC). Indian algo-trading platform — not your product. | ★0 · forks 0 · fork · upstream fork | 3 — Solid technical docs; weak PM framing | **ARCHIVE_OR_DELETE** |
| [personal-chief-of-staff-agent](https://github.com/DecentralizedJM/personal-chief-of-staff-agent) | Public | 2025-11-24 | 8,119 | json:6566, ts:691, tsx:504, md:329 | React dashboard; Express backend **explicitly dormant**. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **EXPERIMENT** |
| [smolvlm-realtime-webcam](https://github.com/DecentralizedJM/smolvlm-realtime-webcam) | Public | 2025-05-12 | 280 | html:265, md:15 | Tiny webcam→SmolVLM demo (~280 LOC) — learning artifact. | ★0 · forks 0 · fork · upstream fork | 2 — Install/quickstart only; no product story | **ARCHIVE_OR_DELETE** |
| [station-master](https://github.com/DecentralizedJM/station-master) | Public | 2026-01-28 | 1,875 | ts:899, json:709, md:267 | **Railway error ingest** → dedupe → Claude classification → optional Telegram (`src` Hono service). | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [support-escalation-tg-bot](https://github.com/DecentralizedJM/support-escalation-tg-bot) | Public | 2025-12-11 | 1,546 | py:1415, md:131 | **Support escalation:** group `/escalate` → DM intake → Slack thread sync. | ★0 · forks 0 · original | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **SUPPORTING** |
| [taxmate-AI](https://github.com/DecentralizedJM/taxmate-AI) | Public | 2026-02-02 | 16,232 | json:7460, ts:5254, md:1549, css:762 | **Indian tax assistant** full-stack: deterministic engine + Gemini tools + Qdrant RAG; Railway-ready. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [technical-sentiment-telegram-bot](https://github.com/DecentralizedJM/technical-sentiment-telegram-bot) | Public | 2025-11-23 | 836 | py:691, md:145 | On-demand TA bot; README mentions news but code is indicators only. | ★0 · forks 0 · original | 3 — Solid technical docs; weak PM framing | **SCAFFOLDING** |
| [telegram-volume-alert-bot](https://github.com/DecentralizedJM/telegram-volume-alert-bot) | Public | 2025-12-05 | 4,208 | md:2849, py:1293, sh:47, yml:19 | Mudrex ops volume spike alerts — README >> code. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **SUPPORTING** |
| [twikit](https://github.com/DecentralizedJM/twikit) | Public | 2025-07-06 | 11,856 | py:11331, md:512, yaml:13 | Fork of **d60/twikit** — unofficial X/Twitter scraper. | ★0 · forks 0 · fork · upstream fork | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |
| [web-design-knowledge-claude-code-skill](https://github.com/DecentralizedJM/web-design-knowledge-claude-code-skill) | Public | 2026-01-06 | 2,999 | py:1779, md:687, yaml:533 | Fork + bundled design-book PDFs/Chroma index for Claude Code UX RAG — licensing/portfolio risk. | ★1 · forks 0 · fork · upstream fork | 5 — Excellent structure (diagrams, env, architecture) but may be overlong or buzzword-adjacent | **ARCHIVE_OR_DELETE** |
| [workspace-monitor-bypass](https://github.com/DecentralizedJM/workspace-monitor-bypass) | Public | 2025-11-26 | 762 | md:466, py:296 | Python script simulates mouse/keyboard to defeat idle monitoring (ProHance-style) — actively damages a senior PM narrative. | ★0 · forks 0 · original | 4 — Strong ops/setup; long or changelog-heavy | **ARCHIVE_OR_DELETE** |

---

## Summary counts

- **HERO:** 7
- **SUPPORTING:** 18
- **EXPERIMENT:** 10
- **SCAFFOLDING:** 5
- **ARCHIVE_OR_DELETE:** 15

| Classification | Count |
|---|---:|
| ARCHIVE_OR_DELETE | 15 |
| EXPERIMENT | 10 |
| HERO | 7 |
| SCAFFOLDING | 5 |
| SUPPORTING | 18 |

---

## Strongest HERO candidates (7)

### 1. `mudrex-proxy-server-websocket`
**Case:** This is the clearest “PM who ships infrastructure” story on your profile. You solved a real platform constraint—many API consumers need Mudrex-branded market streams without each client opening its own Bybit connection—by designing a single upstream, transform layer, and Redis fan-out architecture documented for Railway ops. A frontier-AI hiring manager may not care about crypto, but they will care that you reasoned about connection pooling, subscription ref-counting, rate limits, and graceful degradation under load. README quality is your best in the portfolio (honest ops runbook, not buzzwords).

### 2. `Mudrex-API-Copilot`
**Case:** Closest thing to an **AI-native developer product**: Telegram as the surface, RAG over API docs, MCP tools for live market data, Redis caching, health checks. This demonstrates product thinking for a defined user (Futures API integrators) rather than a generic chatbot demo. Risk: repo has README sprawl (many root markdown files) and no public usage metrics—case study must stay honest about adoption.

### 3. `mudrex-api-trading-python-sdk` (+ MCP)
**Case:** Anchor for a **platform PM narrative**: SDK design, rate limiting, modular API surface, and MCP exposure for agent workflows. Highest star count (★3) among originals. Pair with `mudrex-mcp-prod-landing-page` and `mudrex-api-trading-SDK-registry` as one ecosystem story in Phase 5—not six separate hero slots.

### 4. `night-watchman-telegram-bot`
**Case:** Strongest **trust & safety / ML product** artifact: layered detection (regex → classical ML → LLM → zero-shot), explicit mercy/ban policy in `decision_engine.py`, operator training via `/newscam`. More technically serious than `mudrex-telegram-intern` for reviewers who want depth. Trade-off: two moderation bots on profile looks redundant—pick one for hero, one for supporting link.

### 5. `mudrex-telegram-intern`
**Case:** Tighter **community AI moderation** story with structured Gemini JSON outputs, scam tiers, and rate limits—better “product spec in README” voice than Night Watchman’s changelog style. Proprietary license and stale React files are portfolio hygiene issues, not story killers.

### 6. `mudrex-mcp-prod-landing-page`
**Case:** Proves you can ship **GTM-facing product surfaces** (Cloudflare Workers, API key UX, tool catalog, Claude config snippets) for an MCP launch—not just backend scripts. Essential if your target role is “PM for developer tools / agents.” Less interesting if you lead with trading infra only.

### 7. `XAUT-EMA-Pullback-Strategy`
**Case:** Best **quant + judgment** repo among many similar bots: explicit filter stack, ML gate with `strategy/institutional_ml.py`, backtest/trainer artifacts. Shows iteration discipline. Risk for PM targeting: reads as quant/trader portfolio; lunar-cycle filter may invite skepticism unless framed as “explored, deprioritized.”

**Honorable mention (not HERO, but strong SUPPORTING for AI PM):** `taxmate-AI` — full-stack non-fintech AI product with deterministic tax engine + RAG; better “general intelligence” signal than crypto bots if you want breadth.

---

## Repos to archive, unpublish, or unpin (priority order)

| Repo | Why |
|------|-----|
| `ccxt`, `openalgo`, `awesome-llm-apps`, `evolution-api` | Massive **vendor mirrors**; imply you maintain upstream projects you don’t. |
| `workspace-monitor-bypass` | **Actively toxic** for PM hiring—reads as cheating workplace monitoring. |
| `web-design-knowledge-claude-code-skill` | Fork + **bundled pirated-style PDF corpus**; legal/reputation risk. |
| `RAG-Anything`, `llm-council`, `twikit`, `adk-redis`, `antigravity-claude-proxy`, `smolvlm-realtime-webcam` | **Upstream forks** with no differentiated story. |
| `Price_alert_v5` | GitHub fork, **no README**, not Mudrex-branded. |
| `funding-fee-farmer-v2` | **Superseded** by v4 strategy; contradictory thesis confuses reviewers. |
| `BTC-HA-SuperTrend-5M-Strategy` | Tiny Binance-only script with **hardcoded local paths**. |
| **Strategy sprawl** (if pinned today): `Ultimate-Trend-Strategy`, `free-weight-strategy-mudrex-api`, `SMC-Algo-trading`, `Mudrex-Supertrend-ATR-Strategy-Bot`, `BTC-momentum-catcher-strategy`, `funding-fee-farming-strategy` | Six near-duplicate “Mudrex+Bybit bot” repos dilute signal—keep **at most one** (recommend `XAUT-EMA-Pullback-Strategy` if any). |

**Current profile README (`DecentralizedJM`)** should be replaced entirely: komarev counter, animated GIF, and stack walls violate your own Phase 6 rules and read generic to senior reviewers.

---

## README quality patterns (ruthless)

- **Buzzword soup:** Profile README (“intelligent systems,” “operational architectures,” “precision”) without tying to a user or decision—score 3 at best for a *profile*, not a project.
- **Over-documentation:** `telegram-volume-alert-bot`, `Mudrex-API-Copilot`, `mudrex-telegram-intern` — README length exceeds code depth; reads like ops manuals, not product narratives.
- **Description drift:** `funding-fee-farming-strategy` GitHub description still says “farm funding fees” while v4 code does post-settlement momentum.
- **Fork noise:** 12 repos are `fork: true` on GitHub; only `claude-code-pm-skills` is worth keeping public as a **curated PM signal** if labeled as fork.

---

## Scan artifacts (local only, not for publication)

Shallow clones and `analysis.json` live in `portfolio-rewrite/.repo-scan/` for Phase 2 file/line citations. Do not commit that folder to the live profile repo without review.

---

## Appendix — RexAlgo (repo #56 — private or non-listed on public API)

| Repo | Public/Private | Last commit | Approx LOC | Primary language(s) | What it actually does | Evidence | README (1–5) | Classification |
|------|----------------|-------------|------------|---------------------|----------------------|----------|--------------|----------------|
| [RexAlgo](https://github.com/DecentralizedJM/RexAlgo) | **Private** (clone OK; absent from unauthenticated API list) | 2026-05-27 | ~large monorepo (frontend+backend+docs; ~6.7MB excl. git) | TypeScript (React + Next.js), SQL migrations | **Algo marketplace + copy trading** on Mudrex Futures: masters publish strategies, HMAC webhooks mirror trades to subscribers; TIA advisory auto-trade; TV webhooks; Postgres sessions, encrypted Mudrex keys, Redis rate limits (`docs/CONTEXT.md`, `mudrexRateLimit.ts`) | Not in public star count; **CI + 83 backend tests** per `docs/CONTEXT.md` | **5** — executive summary, mermaid index, PROD/SECURITY/LOAD-TEST | **HERO** |

Full profile: [`03-rexalgo.md`](03-rexalgo.md).

**Platform siblings:** `mudrex-api-trading-python-sdk`, `mudrex-proxy-server-websocket`, `mudrex-trade-ideas-html-cards` (Plotline embeds; RexAlgo consumes **TIA API** in-app).
