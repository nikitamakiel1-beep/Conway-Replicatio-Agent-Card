# x402 buyer flow example

Use this as a protocol pattern, not as a source of hard-coded prices or recipients.

```bash
ORIGIN='https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev'

curl -i -X POST "$ORIGIN/api/x402/markdown" \
  -H 'content-type: application/json' \
  --data '{"url":"https://example.com/"}'
```

Expected first result: HTTP `402 Payment Required` with the live x402 payment requirement.

A buyer must validate the returned requirement before authorizing payment. At minimum verify the intended resource/method, x402 version, `exact` scheme, Base mainnet CAIP-2 network `eip155:8453`, token/asset, amount, pay-to address and expiry/timeout.

Then use a compatible x402 client to satisfy the exact challenge and retry the same application request with the required payment proof/header.

Do not copy a historical payment header into automation. Do not reuse a payment proof outside the resource/idempotency semantics authorized by the live challenge.

A successful settlement is not enough to call the purchase successful: validate that the application response is successful and schema-valid. Conway likewise does not recognize machine-service revenue until unrelated external settlement and successful fulfilment are both evidenced.