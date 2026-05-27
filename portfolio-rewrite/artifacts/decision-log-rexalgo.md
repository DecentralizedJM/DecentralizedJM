# Decision log — RexAlgo (extracted; verify dates/owners)

| ID | Date | Decision | Alternatives considered | Rationale | Status |
|----|------|----------|-------------------------|-----------|--------|
| D1 | `TODO[JM]` | Mudrex-only execution | Multi-exchange | Focus, one limiter model | Accepted |
| D2 | `TODO[JM]` | Subscriber-owned API keys | Master custody | Trust + compliance | Accepted |
| D3 | `TODO[JM]` | HMAC webhook `t.body` + 60s skew default | Body secret only; 300s replay | Reduce replay surface (`copyWebhookHmac.ts` L6-10) | Accepted |
| D4 | `TODO[JM]` | `trade_volume_ledger` sidecar for volume | Rewrite `trade_logs`; double-row close | Smallest blast radius (`FINDINGS.md` Q4 rec **b**) | `TODO[JM]:` shipped? |
| D5 | `TODO[JM]` | Parallel master/sub-broker rollups (slice a) | Hierarchical rollup | Schema today (`FINDINGS.md` Q2) | Open / verify |
| D6 | `TODO[JM]` | Unify TIA HMAC window to 60s | Keep 5 min TIA window | Align with strategy/TV (`FINDINGS.md` Q5) | `TODO[JM]` |
| D7 | `TODO[JM]` | Redis-backed Mudrex limiter for multi-replica | In-memory only | Scale webhooks (`mudrexRateLimit.ts` L31-32) | Accepted when `REDIS_URL` set |

## From git / changelog

`TODO[JM]:` paste 3–5 release-defining commits from `CHANGELOG.md` with one-line decision each.
