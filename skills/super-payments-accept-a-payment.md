---
name: Accept a payment via a checkout session
description: Create a Super Payments checkout session, attach order details, take the payment, and confirm the result.
api: openapi/super-payments-openapi.yml
operations: [create-checkout-session, upsert-order-details, proceed-payment-via-checkout-session, get-payment-transaction-2025-11-01]
---

# Accept a payment via a checkout session

Use this flow to charge a shopper through a Super Payments checkout session.

## Prerequisites
- A secret API key (`sk_prod_` live, `sk_test_` sandbox). Pass it raw in the `Authorization` header — no `Bearer` prefix.
- A payment initiator ID from **Integration & Tools → API Keys** in the Business Portal.
- All requests go to `https://api.superpayments.com/2026-04-01` (live) or `https://api.test.superpayments.com/2026-04-01` (sandbox). The date version segment is mandatory.

## Steps
1. **`create-checkout-session`** — `POST /checkout-sessions`. Create the session for your payment initiator; capture the returned session id.
2. **`upsert-order-details`** — `POST /checkout-sessions/{checkoutSessionId}/order-details`. Attach shipping/billing address and/or line items (at least one is required).
3. **`proceed-payment-via-checkout-session`** — `POST /checkout-sessions/{checkoutSessionId}/proceed`. Take the payment. A `402` here means the card was declined — read `extensions.issues.declineCode`/`declineReason` and honour `declineClassification` (mask `RESTRICTED` codes as a generic decline). See `errors/super-payments-decline-codes.yml`.
4. **`get-payment-transaction-2025-11-01`** — `GET /payments/{transactionId}`. Poll for the final status if you are not consuming webhooks. Prefer the `payment.success` / `payment.failed` webhooks (`asyncapi/super-payments-webhooks-asyncapi.yml`) for real-time confirmation.

## Rules
- There is no idempotency-key header. To avoid double charging, reuse your own reference and look the session/payment up before retrying (`conventions/super-payments-conventions.yml`).
- Errors are RFC 9457 `application/problem+json` (`errors/super-payments-problem-types.yml`).
- Respect rate limits: 20 read/s and 20 write/s; back off on `429`.
- In sandbox, use Adyen test cards and Yapily Mock for open banking (`sandbox/super-payments-sandbox.yml`).
