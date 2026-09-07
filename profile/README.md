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

- [`POST /v2/serp/urls`](https://reserp.ai/docs/urls) returns a flat, page-ordered URL-and-text index for scraping, research, monitoring, and AI ingestion.
- [`POST /v2/serp/structured`](https://reserp.ai/docs/structured) returns typed organic, ad, image, shopping, news, video, and local results plus page features and explicit positions.

## Call v2 directly

```sh
curl --request POST 'https://api.reserp.ai/v2/serp/urls' \
  --header "Authorization: Bearer $RESERP_API_KEY" \
  --header 'Content-Type: application/json' \
  --data '{"url":"https://www.google.com/search?q=photonic+computing&gl=us&hl=en"}'
```

Search options remain in the submitted Google URL. Send `pagination.next_url` back as the next request body's `url`; do not infer an offset from a result-array length.

## Client-library status

The currently published [`@reserp/sdk`](https://github.com/reserp-ai/reserp-js) and [`reserp`](https://github.com/reserp-ai/reserp-python) packages target the legacy v1 contract. New v2 integrations should use direct HTTP and the canonical OpenAPI document until a v2-compatible client release is published.

## Resources

- [Google Search API documentation](https://reserp.ai/docs)
- [Runnable v2 examples](https://github.com/reserp-ai/reserp-examples)
- [OpenAPI 3.1 document](https://reserp.ai/openapi.json)
- [Postman API documentation](https://documenter.getpostman.com/view/57501126/2sBYArSrqS)
- [Plans and pricing](https://reserp.ai/pricing)
- [Create a Reserp account](https://reserp.ai/dashboard)
- [Reserp on LinkedIn](https://www.linkedin.com/company/reserp-ai)
- [Reserp on X](https://x.com/reserp_ai)
