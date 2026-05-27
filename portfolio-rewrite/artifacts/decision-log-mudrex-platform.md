# Decision log — Mudrex platform (SDK / WS / MCP)

| ID | Decision | Alternatives | Evidence |
|----|----------|--------------|----------|
| P1 | Client-side rate limit + 429 retry | Server-only docs | `mudrex/client.py` L30-205 |
| P2 | MCP as FastMCP tools on SDK | Hosted agent platform | `mudrex/mcp/server.py` |
| P3 | Single Bybit upstream + Redis fan-out | Per-client upstream | `mudrex-proxy` `pool.py`, `subscriptions.py` |
| P4 | Standalone WS server vs FastAPI hot path | Keep uvicorn stack | `standalone_server.py` header |
| P5 | Telegram + RAG for API copilot | Web-only docs | `Mudrex-API-Copilot` structure |
| P6 | Gemini primary for copilot | Multi-LLM router | `settings.py` GEMINI_* |

`TODO[JM]:` add dates and stakeholder names.
