# Mudrex API Copilot — PM-facing header (draft)

**Telegram copilot** for developers integrating **Mudrex Futures API**: RAG over docs, scoped replies, live tools via **Mudrex MCP**, Redis caching.

---

## The problem

API support does not scale on Slack alone: repeated “how do I auth?” questions, stale examples, and hallucinated endpoints when generic LLMs answer.

---

## What we decided to build

| Decision | Why |
|----------|-----|
| Telegram as surface | Developers already in Mudrex community channels |
| RAG + query planner + semantic cache | Cost control; similar questions deduped |
| MCP client for live listings/tools | Answers with real catalog data, not only static docs |
| Off-topic guards (`pipeline.py`) | Brand scope — not a general chatbot |
| Futures listing watcher (scheduled) | Proactive “new symbol” broadcasts |

**Rejected:** Open-ended general assistant; unauthenticated trading on behalf of users.

---

## Trade-offs

- Gemini-primary — simpler ops than multi-vendor LLM routing.
- Many root markdown docs — consolidate to `docs/PRODUCT.md` for external readers.

---

## Outcomes

`TODO[JM]:` messages/week, deflection rate, cost per query — see `artifacts/outcomes-api-copilot.md`.

---

## Tech notes

Python · Qdrant · Redis · Railway. See existing README for deploy.
