<p align="center">
  <a href="https://reserp.ai">
    <img src="https://reserp.ai/icon-512.png" alt="Reserp Google Search API" width="112" height="112">
  </a>
</p>

<h1 align="center">Reserp</h1>

<p align="center"><strong>Google Search data, structured for scale.</strong></p>
<p align="center">A Google Search API for developers, AI agents, and high-volume recurring business workloads.</p>
<p align="center">Start for free with no credit card required.</p>

<p align="center">
  <a href="https://reserp.ai">Website</a> ·
  <a href="https://reserp.ai/docs">API documentation</a> ·
  <a href="https://reserp.ai/pricing">Pricing</a> ·
  <a href="https://reserp.ai/dashboard">Dashboard</a>
</p>

Reserp v2 turns Google Search pages into two documented JSON shapes without requiring developers to maintain search-page scrapers:

- [`POST /v2/serp/search`](https://reserp.ai/docs/search) returns flat, page-ordered, deduplicated entries in `results[]` for scraping, research, monitoring, and AI ingestion.
- [`POST /v2/serp/structured`](https://reserp.ai/docs/structured) returns typed, page-ordered SERP blocks in `blocks[]`, with explicit block and item positions.

## Call v2 directly

```sh
curl --request POST 'https://api.reserp.ai/v2/serp/search' \
  --header "Authorization: Bearer $RESERP_API_KEY" \
  --header 'Content-Type: application/json' \
  --data '{"url":"https://www.google.com/search?q=photonic+computing&gl=us&hl=en"}'
```

Search options remain in the submitted Google URL. Send `pagination.next_url` back as the next request body's `url`; do not infer an offset from a result-array length.

## Official SDKs

- [`@reserp/sdk` 0.4](https://www.npmjs.com/package/@reserp/sdk) provides typed JavaScript and TypeScript `search()` and `structured()` methods.
- [`reserp` 0.4](https://pypi.org/project/reserp/) provides synchronous and asynchronous Python `search()` and `structured()` methods.

Both SDKs target API v2, make exactly one request per call, and return their native transport response unchanged. The former `urls()` method remains as a deprecated Search alias in both packages.

## Resources

- [Google Search API documentation](https://reserp.ai/docs)
- [Runnable v2 examples](https://github.com/reserp-ai/reserp-examples)
- [OpenAPI 3.1 document](https://reserp.ai/openapi.json)
- [Postman API documentation](https://documenter.getpostman.com/view/57501126/2sBYArSrqS)
- [Plans and pricing](https://reserp.ai/pricing)
- [Create a Reserp account](https://reserp.ai/dashboard)
- [Reserp on LinkedIn](https://www.linkedin.com/company/reserp-ai)
- [Reserp on X](https://x.com/reserp_ai)
