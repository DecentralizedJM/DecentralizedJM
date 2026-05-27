# RexAlgo — portfolio slot (PM: algo + advisory)

**Status:** Added per your direction; **not present** in the Phase 1 scan of 55 public `DecentralizedJM` repos (no repo name or README mention of “RexAlgo”).  
**Next step:** Attach repo URL(s), internal doc links, or a local clone path so Phases 2–7 can cite real files.

---

## How RexAlgo fits your PM story

| Layer | Mudrex platform (scanned) | RexAlgo (you) |
|-------|---------------------------|---------------|
| **Integrators** | Futures REST SDK, MCP, WS proxy, API Copilot | — |
| **Retail / guided traders** | Trade-idea widgets, strategy bots | **RexAlgo product** (algo + advisory UX, mandates, risk) |
| **Data** | WS proxy, Bybit klines in bots | TBD — link to WS/API dependencies |

**Positioning line (draft — verify):** RexAlgo is the **consumer-facing algo / advisory product**; the GitHub platform repos are the **rails** (API, streams, MCP) that strategies and apps build on.

---

## Related public repos (adjacent, not RexAlgo core)

These may be **inputs or surfaces** for RexAlgo; do not call them “RexAlgo” unless code/docs say so.

| Repo | Relationship (hypothesis — confirm) |
|------|-------------------------------------|
| `mudrex-trade-ideas-html-cards` | Advisory UI embed; [Project TIA](https://project-tia-production.up.railway.app/docs/api) JSON → Plotline cards |
| `XAUT-EMA-Pullback-Strategy`, `free-weight-strategy-mudrex-api`, `BTC-momentum-catcher-strategy`, etc. | **Strategy implementations** on Mudrex API + Bybit data — portfolio as “builder-PM prototypes,” not necessarily production RexAlgo strategies |
| `mudrex-api-trading-python-sdk` | Execution rail for algo strategies |
| `mudrex-proxy-server-websocket` | Market-data rail |

---

## Scan checklist (when you attach RexAlgo)

| Item | `TODO[JM]` |
|------|------------|
| GitHub org/repo or private repo name | |
| One-line: who is the user? | e.g. retail futures trader, copy-trader, advisor-led |
| Your role | PM scope: roadmap, PRD, GTM, risk, partnerships |
| Stack | App (mobile/web), backend, job runners, strategy runtime |
| API/WS usage | Does RexAlgo call Mudrex REST, WS proxy, or both? |
| Advisory vs autonomous algo | Product boundary |
| Metrics you can share | MAU, AUM, strategies live, error rates, retention |
| PM artifacts you have | PRD, ADRs, research, launch retro |

---

## Artifact plan (Phase 7 — same as other products)

When RexAlgo source is available, generate:

- `artifacts/prd-rexalgo.md`
- `artifacts/decision-log-rexalgo.md` (from git history + your notes)
- `artifacts/outcomes-rexalgo.md`

Until then, use `artifacts/outcomes-rexalgo.md` stub (created in this commit) for metrics-only placeholders.

---

## Profile / README (strategy B)

Include RexAlgo in **Selected work** and **Currently** once you confirm public link or approved description. Do not invent metrics or user counts.

**Example half-line (edit):** RexAlgo — algo & advisory trading product at Mudrex *(link TBD)*.
