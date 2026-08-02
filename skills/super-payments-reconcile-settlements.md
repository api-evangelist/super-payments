---
name: Reconcile settlements
description: List settlement batches, fetch a settlement's detail, and pull its reconciliation rows to match payouts to payments.
api: openapi/super-payments-openapi.yml
operations: [list-settlements-2025-11-01, get-settlement-detail-2025-11-01, get-settlement-reconciliation-2025-11-01]
---

# Reconcile settlements

Use this flow to reconcile Super Payments payouts against your ledger.

## Prerequisites
- Secret API key in the `Authorization` header; base URL `https://api.superpayments.com/2026-04-01` (or sandbox).
- These endpoints support content negotiation — set the `Accept` header the docs specify (JSON, or the CSV variant) or you may receive `406`.

## Steps
1. **`list-settlements-2025-11-01`** — `GET /settlements`. List settlement batches for the merchant; paginate with the `page` cursor + `pageSize`.
2. **`get-settlement-detail-2025-11-01`** — `GET /settlements/{settlementId}`. Fetch one settlement with its payments and statistics.
3. **`get-settlement-reconciliation-2025-11-01`** — `GET /settlements/{settlementId}/reconciliation`. Pull the ledger reconciliation rows (paginated) and match each line to your own records.

## Rules
- Read-only flow — respect the 20 read/s limit and back off on `429`.
- Errors are RFC 9457 problem+json (`errors/super-payments-problem-types.yml`).
