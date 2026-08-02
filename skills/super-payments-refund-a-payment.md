---
name: Refund a payment
description: Find a settled payment transaction and issue a full or partial refund, then confirm it.
api: openapi/super-payments-openapi.yml
operations: [search-payment-transactions-2025-11-01, create-refund, get-refund-transaction-2025-11-01]
---

# Refund a payment

Use this flow to refund a Super Payments transaction.

## Prerequisites
- Secret API key in the `Authorization` header; base URL `https://api.superpayments.com/2026-04-01` (or the sandbox host).

## Steps
1. **`search-payment-transactions-2025-11-01`** — `GET /payments/search`. Locate the payment by reference/date/status if you do not already hold its `transactionId` (paginate with the `page` cursor + `pageSize`).
2. **`create-refund`** — `POST /refunds`. Initiate a full or partial refund against the payment transaction. (For refunds to a different payment method, `create-payout-refund` → `POST /refunds/payouts` is a **restricted** endpoint requiring support access.)
3. **`get-refund-transaction-2025-11-01`** — `GET /refunds/{transactionId}`. Poll for refund status, or consume the `refund.success` / `refund.failed` webhooks instead.

## Rules
- No idempotency-key header — guard against duplicate refunds by checking refund status before retrying.
- Handle RFC 9457 errors (`errors/super-payments-problem-types.yml`); a `409` indicates a conflicting refund state.
- Back off on `429` (20 read/s, 20 write/s).
