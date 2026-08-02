---
name: Save a card and charge it off-session
description: Create a customer, register a reusable payment method, set it up with the super-card component, then charge it off-session.
api: openapi/super-payments-openapi.yml
operations: [create-customer, create-payment-method, create-setup-intent, create-payment-intent]
---

# Save a card and charge it off-session

Use this flow for merchant-initiated (off-session) payments against a stored card.

## Prerequisites
- Secret API key in the `Authorization` header; a public `PUB_` key for the client-side `<super-card>` component.
- Base URL `https://api.superpayments.com/2026-04-01` (or sandbox).

## Steps
1. **`create-customer`** — `POST /customers`. Create (or reuse) the customer; you may supply your own `externalReference`. Capture the returned Super `customerId`.
2. **`create-payment-method`** — `POST /payment-methods`. Create a payment method associated with the customer for future off-session use.
3. **`create-setup-intent`** — `POST /payment-methods/{id}/setup-intents`. Returns a session token; pass it to the `<super-card>` web component (`components/super-payments-components.yml`) so the shopper sets up their card. Wait for the `customer.payment-method.enabled` webhook before charging.
4. **`create-payment-intent`** — `POST /payments`. Create an off-session payment intent against the enabled payment method. A `402` means a decline — inspect `extensions.issues.declineCode` (`errors/super-payments-decline-codes.yml`).

## Rules
- Off-session charges rely on prior customer consent captured during setup — do not charge a method still in `requires-action`.
- No idempotency-key header; reuse a client reference and verify before retrying.
- Errors are RFC 9457 problem+json; respect 20 read/s and 20 write/s limits.
- In sandbox, set up cards with Adyen test cards (`sandbox/super-payments-sandbox.yml`).
