# SAVER

**Independent factual checks for autonomous agent research and reports.**

SAVER builds machine-to-machine verification infrastructure for autonomous software. Our systems are designed to help agents verify external information with independent web evidence before they act, pay, or make consequential decisions.

## SAVER Verifier

SAVER Verifier is our production factual claim verification API for autonomous AI agents.

It combines live web search, source selection, evidence evaluation, and structured output in a single machine-readable service.

**Production:** `https://api.saververify.com`  
**Recommended endpoint:** `POST /v2/verify`  
**Original response format:** `POST /verify`  
**Price:** `0.20 USDC` per completed verification  
**Network:** Base Mainnet (`eip155:8453`)  
**Payments:** x402 v2, exact scheme

SAVER Verifier returns structured verification results including:

- verification status
- confidence
- explanation
- evidence linked to source IDs (v2)
- cited sources

It is intended as an independent evidence signal, not as a replacement for an agent's own authorization, wallet, or security policies.

New integrations should use v2. Existing `/verify` clients retain their original string-evidence response format. Confidence is model-assessed, not a calibrated probability.

## Developer access

| Resource | URL |
| --- | --- |
| Website | https://saververify.com |
| API | https://api.saververify.com |
| Public repository | https://github.com/SAVER-SI/saver-verifier |
| OpenAPI 3.1 | https://api.saververify.com/openapi.json |
| x402 discovery | https://api.saververify.com/.well-known/x402 |
| LLM discovery | https://api.saververify.com/llms.txt |
| Agent tool definition | https://api.saververify.com/agent-tool.json |
| Actual paid examples | https://saververify.com/examples/ |
| ClawHub skill v1.1.0 | https://clawhub.ai/saver-si/skills/saver-verifier |

The three published result examples are actual operator-funded purchases. Reading them is free; they are demonstrations, not an independent accuracy benchmark.

## Machine-native by design

SAVER Verifier is built for autonomous, programmatic use:

```text
discover -> inspect -> pay -> verify -> consume
```

The service exposes machine-readable discovery, an OpenAPI contract, x402 payment requirements, and structured verification responses without requiring a traditional API-key subscription workflow. Invalid requests include machine-readable correction guidance before payment. Verification uses POST with JSON; GET/HEAD returns 405 with Allow: POST.

## Repositories

- [saver-verifier](https://github.com/SAVER-SI/saver-verifier) — public developer documentation, integration examples, OpenAPI, and agent skill source
- [saver-site](https://github.com/SAVER-SI/saver-site) — official SAVER Verifier website

---

[SAVER Verifier](https://saververify.com) · [API](https://api.saververify.com) · [GitHub](https://github.com/SAVER-SI/saver-verifier)
