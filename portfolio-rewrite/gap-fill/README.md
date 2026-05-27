# Gap-fill backlog (strategy B)

You chose **B**: substantiate profile claims with **small, real commits** — not README fiction.

Apply these to **product repos** (`mudrex-api-trading-python-sdk`, `mudrex-proxy-server-websocket`, etc.), not only this profile repo. Copy workflows from this folder when ready.

| Gap (from `01-skill-map.md` Table B) | Deliverable | File to copy |
|--------------------------------------|-------------|--------------|
| No CI | GitHub Action: pytest on SDK | `ci-mudrex-python-sdk.yml` → `.github/workflows/ci.yml` |
| No CI | GitHub Action: pytest on WS proxy | `ci-mudrex-ws-proxy.yml` → `.github/workflows/ci.yml` |
| CI on RexAlgo | **Already shipped** | `RexAlgo/.github/workflows/ci.yml` — cite in portfolio; no copy needed |
| Multi-agent claim | Remove from profile OR add `examples/mcp_planner_demo.py` (planner + 2 tool steps, single process) | TBD in SDK repo |
| OpenAI/Anthropic/DeepSeek on profile | Edit profile README per `profile-claims-patch.md` | `DecentralizedJM/README.md` |
| AWS/GCP on profile | Same patch — Railway / Cloudflare / Docker | `profile-claims-patch.md` |
| Async overclaim | Add `docs/ASYNC.md` in SDK: sync client + executor pattern | Draft in SDK repo |
| No outcomes | Fill Phase 7 `artifacts/outcomes-*.md` | `portfolio-rewrite/artifacts/` (Phase 7) |

**Do not** commit secrets or live API keys in any gap-fill PR.
