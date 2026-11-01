# Super Payments

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Super Payments is a UK payments provider offering free card and open-banking (pay-by-bank) payment processing for businesses, funded by a customer-acquisition and cash-rewards model rather than per-transaction fees. Its REST API lets merchants create payments and checkout sessions, issue refunds, manage customers and reusable payment methods, run settlements and reconciliation, create no-code payment links, and configure cash rewards. The API uses date-based URL versioning, static API-key authentication, RFC 9457 problem+json errors, cursor pagination, HMAC-signed webhooks, an embedded super-card web component and hosted payment page, and a React Native SDK. Backed by Accel and Union Square Ventures.

**Areas:** Company · Payments · Open Banking · Cash Rewards · Checkout · Fintech · United Kingdom · Pay by Bank

## Super Payments on APIs.io

Everything profiled for Super Payments is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/super-payments/](https://apis.io/providers/super-payments/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [Super Payments Checkout Sessions API](https://apis.io/apis/super-payments/super-payments-checkout-sessions-api/) — Checkout Session management
- [Super Payments Customer API](https://apis.io/apis/super-payments/super-payments-customer-api/) — The Customer API from Super Payments — 2 operation(s) for customer.
- [Super Payments Payment Links API](https://apis.io/apis/super-payments/super-payments-payment-links-api/) — Manage payment links for one-time payments
- [Super Payments Payment Methods API](https://apis.io/apis/super-payments/super-payments-payment-methods-api/) — The Payment Methods API from Super Payments — 4 operation(s) for payment methods.
- [Super Payments API](https://apis.io/apis/super-payments/super-payments-payments-api/) — Payment processing and management
- [Super Payments Refunds API](https://apis.io/apis/super-payments/super-payments-refunds-api/) — Refund management
- [Super Payments Rewards API](https://apis.io/apis/super-payments/super-payments-rewards-api/) — Rewards configuration and calculation and management
- [Super Payments Settlements API](https://apis.io/apis/super-payments/super-payments-settlements-api/) — Settlement batches, details, and reconciliation
- [Super Payments Webhooks API](https://apis.io/apis/super-payments/super-payments-webhooks-api/) — The Webhooks API from Super Payments — 0 operation(s) for webhooks.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Super Payments Webhooks](https://apis.io/asyncapis/super-payments/super-payments-webhooks-asyncapi/)

#### Event channels (9)

Individual events and webhooks the provider emits.

- [customer.payment-method.disabled](https://apis.io/channels/super-payments/customer-payment-method-disabled/)
- [customer.payment-method.enabled](https://apis.io/channels/super-payments/customer-payment-method-enabled/)
- [customer.payment-method.requires-action](https://apis.io/channels/super-payments/customer-payment-method-requires-action/)
- [payment.failed](https://apis.io/channels/super-payments/payment-failed/)
- [payment.status-update](https://apis.io/channels/super-payments/payment-status-update/)
- [payment.success](https://apis.io/channels/super-payments/payment-success/)
- [refund.failed](https://apis.io/channels/super-payments/refund-failed/)
- [refund.status-update](https://apis.io/channels/super-payments/refund-status-update/)
- [refund.success](https://apis.io/channels/super-payments/refund-success/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [super-payments](https://apis.io/servers/super-payments/super-payments/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Super Payments Agentic Access](https://apis.io/agentic-access/super-payments/super-payments-agentic-access/)

#### JSON Schema (37)

The data models the API reads and writes.

- [CreateCheckoutSessionRequestDto](https://apis.io/schemas/super-payments/super-payments-create-checkout-session-request-dto/)
- [CreateCheckoutSessionResponseDto](https://apis.io/schemas/super-payments/super-payments-create-checkout-session-response-dto/)
- [CreateCustomer20260401RequestDto](https://apis.io/schemas/super-payments/super-payments-create-customer20260401-request-dto/)
- [CreateOffSessionPaymentIntentOutput](https://apis.io/schemas/super-payments/super-payments-create-off-session-payment-intent-output/)
- [CreateOnSessionPaymentIntentOutput](https://apis.io/schemas/super-payments/super-payments-create-on-session-payment-intent-output/)
- [CreatePaymentIntentInput](https://apis.io/schemas/super-payments/super-payments-create-payment-intent-input/)
- [CreatePaymentMethodRequestDto](https://apis.io/schemas/super-payments/super-payments-create-payment-method-request-dto/)
- [Customer20260401ResponseDto](https://apis.io/schemas/super-payments/super-payments-customer20260401-response-dto/)
- [GenerateRewardCalculationInput](https://apis.io/schemas/super-payments/super-payments-generate-reward-calculation-input/)
- [GenerateRewardCalculationOutputDto](https://apis.io/schemas/super-payments/super-payments-generate-reward-calculation-output-dto/)
- [GetPaymentTransactionOutput](https://apis.io/schemas/super-payments/super-payments-get-payment-transaction-output/)
- [GetPaymentsListOutput](https://apis.io/schemas/super-payments/super-payments-get-payments-list-output/)
- [GetRefundTransactionOutput](https://apis.io/schemas/super-payments/super-payments-get-refund-transaction-output/)
- [GetRefundsListOutput](https://apis.io/schemas/super-payments/super-payments-get-refunds-list-output/)
- [InitiatePayoutRefundInputDto](https://apis.io/schemas/super-payments/super-payments-initiate-payout-refund-input-dto/)
- [InitiatePayoutRefundOutputDto](https://apis.io/schemas/super-payments/super-payments-initiate-payout-refund-output-dto/)
- [InitiateRefundInputDto](https://apis.io/schemas/super-payments/super-payments-initiate-refund-input-dto/)
- [InitiateRefundOutputDto](https://apis.io/schemas/super-payments/super-payments-initiate-refund-output-dto/)
- [LinkInputDto](https://apis.io/schemas/super-payments/super-payments-link-input-dto/)
- [LinkResponseDto](https://apis.io/schemas/super-payments/super-payments-link-response-dto/)
- [PaginatedCustomer20260401ListResponse](https://apis.io/schemas/super-payments/super-payments-paginated-customer20260401-list-response/)
- [PaginatedLinksOutput](https://apis.io/schemas/super-payments/super-payments-paginated-links-output/)
- [PaginatedPaymentMethodListOutput](https://apis.io/schemas/super-payments/super-payments-paginated-payment-method-list-output/)
- [PaymentMethodResponseDto](https://apis.io/schemas/super-payments/super-payments-payment-method-response-dto/)
- [ProceedPaymentViaCheckoutSessionRequestDto](https://apis.io/schemas/super-payments/super-payments-proceed-payment-via-checkout-session-request-dto/)
- …and 12 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Super Payments Context](https://apis.io/jsonld/super-payments/super-payments-context/)

#### Collections (16)

Postman and Open Collection request collections.

- [Super Payments Checkout Sessions API](https://apis.io/collections/super-payments/open-super-payments-checkout-sessions-api/)
- [Super Payments Checkout Sessions Customer API](https://apis.io/collections/super-payments/open-super-payments-customer-api/)
- [Super Payments Checkout Sessions Payment Links API](https://apis.io/collections/super-payments/open-super-payments-payment-links-api/)
- [Super Payments Checkout Sessions Payment Methods API](https://apis.io/collections/super-payments/open-super-payments-payment-methods-api/)
- [Super Checkout Sessions Payments API](https://apis.io/collections/super-payments/open-super-payments-payments-api/)
- [Super Payments Checkout Sessions Refunds API](https://apis.io/collections/super-payments/open-super-payments-refunds-api/)
- [Super Payments Checkout Sessions Rewards API](https://apis.io/collections/super-payments/open-super-payments-rewards-api/)
- [Super Payments Checkout Sessions Settlements API](https://apis.io/collections/super-payments/open-super-payments-settlements-api/)
- [Super Payments Checkout Sessions API](https://apis.io/collections/super-payments/postman-super-payments-checkout-sessions-api/)
- [Super Payments Checkout Sessions Customer API](https://apis.io/collections/super-payments/postman-super-payments-customer-api/)
- [Super Payments Checkout Sessions Payment Links API](https://apis.io/collections/super-payments/postman-super-payments-payment-links-api/)
- [Super Payments Checkout Sessions Payment Methods API](https://apis.io/collections/super-payments/postman-super-payments-payment-methods-api/)
- [Super Checkout Sessions Payments API](https://apis.io/collections/super-payments/postman-super-payments-payments-api/)
- [Super Payments Checkout Sessions Refunds API](https://apis.io/collections/super-payments/postman-super-payments-refunds-api/)
- [Super Payments Checkout Sessions Rewards API](https://apis.io/collections/super-payments/postman-super-payments-rewards-api/)
- [Super Payments Checkout Sessions Settlements API](https://apis.io/collections/super-payments/postman-super-payments-settlements-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Super Payments Openapi Overlay](https://apis.io/overlays/super-payments/super-payments-openapi-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Super Payments API Rules](https://apis.io/rules/super-payments/super-payments-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Super Payments Authentication](https://apis.io/security/super-payments/super-payments-authentication/)
- [Super Payments Domain Security](https://apis.io/security/super-payments/super-payments-domain-security/)

#### Plans and pricing (2)

Published plans, tiers and prices.

- [Super Payments Plans Pricing](https://apis.io/plans/super-payments/super-payments-plans-pricing/)
- [Super Payments Price Estimates](https://apis.io/plans/super-payments/super-payments-price-estimates/)

#### Rate limits (1)

Published request limits.

- [Super Payments Rate Limits](https://apis.io/rate-limits/super-payments/super-payments-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.superpayments.com/for-business)
- [Documentation](https://docs.superpayments.com/docs)
- [Getting started](https://docs.superpayments.com/docs/getting-started)
- [API reference](https://docs.superpayments.com/reference)
- [Pricing](https://www.superpayments.com/pricing)
- [Sign up](https://business.superpayments.com)
- [Support](https://support.superpayments.com/hc/en-gb)
- [Changelog](https://docs.superpayments.com/changelog)
- [Blog](https://www.superpayments.com/blog)
- [Terms of service](https://www.superpayments.com/terms-and-conditions)
- [Privacy policy](https://www.superpayments.com/privacy-policy)
- [GitHub](https://github.com/superpayments)
- [Status](https://status.superpayments.com/)

## API Evangelist rating

**Kin Score 67.5** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 76.0 |
| Contract governance | 33.3 |
| Operational transparency | 59.2 |
| Developer ergonomics | 55.4 |
| Access clarity | 76.3 |

**Agent readiness 40.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 29.5** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/super-payments/](https://apis.io/providers/super-payments/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Super Payments: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/super-payments/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
