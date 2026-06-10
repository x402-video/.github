# x402-video.com

**Pay-per-call AI video generation over the [x402 payment protocol](https://docs.x402.org).**

No accounts, no API keys, no credit cards: `HTTP 402 → pay USDC on Base → generate`.
Built for developers and autonomous agents.

## How it works

```
POST /generate/seedance/5s-720p          → 402 + payment requirements
  (pay USDC via any x402 client, retry)  → { job_id, status_url }
GET  /jobs/:id                (free)     → status → video_url (24h)
```

- Prompts are screened **before** payment — rejected requests are never charged
- Live reliability stats are public: success rate, p50 generation time, total delivered
- Multiple model families behind one consistent API (Seedance today; more coming)

## Repositories

| Repo | What |
|---|---|
| [web](https://github.com/x402-video/web) | Public storefront + `llms.txt` + buyer examples |
| gateway | The payment + generation gateway (private) |

---

*Independent gateway — not affiliated with or endorsed by model vendors.*
