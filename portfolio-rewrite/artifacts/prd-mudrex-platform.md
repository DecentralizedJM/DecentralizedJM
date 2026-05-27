# PRD scaffold — Mudrex Futures platform (SDK + WS + MCP)

> Umbrella for integrator-facing work. Split by repo when presenting.

## Problem

Teams building on Mudrex Futures need **documented, rate-safe clients**, **realtime streams**, and **agent-accessible tools** — not raw REST trial-and-error.

## Users

- Quant / bot developers at `TODO[JM]:` companies
- Internal Mudrex teams
- AI agent builders (Claude/Cursor via MCP)

## Goals

| Component | Outcome |
|-----------|---------|
| Python SDK | Default integrator path; errors + limits built-in |
| WS proxy | Mudrex-branded streams at scale |
| MCP | Tool surface = SDK capabilities |
| Landing | Adoption in <15 min with API key + config |
| API Copilot | Deflect L1 API questions in community |

## Success metrics

`TODO[JM]:` per component in `outcomes-*.md`

## Dependencies

RexAlgo and internal apps consume the same API/MCP/WS rails.
