---
name: Retrieve Teachers Mutual Bank product catalogue
description: List and inspect Teachers Mutual Bank's public banking products via the CDR Product Reference Data API — no authentication required.
api: openapi/teachers-mutual-bank-cds-banking-products-openapi.yml
operations:
- listBankingProducts
- getBankingProductDetail
---

# Retrieve Teachers Mutual Bank product catalogue

Teachers Mutual Bank publishes its full banking product catalogue through the
Australian Consumer Data Right (CDR) Product Reference Data API. It is public and
requires **no authentication, API key, or CDR accreditation**.

Base URL: `https://ob.tmbl.com.au/tmbank/cds-au/v1`

## Rules

- **Always send the `x-v` header.** Supported endpoint versions are `4` and `5`.
  Omitting it or sending an unsupported value returns HTTP `406`.
- Read-only: both operations are `GET`. No idempotency key is needed.
- Errors return the CDS `ResponseErrorListV2` envelope
  (`{ "errors": [ { "code": "<urn>", "title": "...", "detail": "..." } ] }`),
  content type `application/json` — not RFC 9457.
- Respect rate limits: responses carry `x-rate-limit-*` and `x-quota-*` headers.

## Steps

1. **List products** — call `listBankingProducts`:
   `GET /banking/products` with header `x-v: 4`. Optional query params `page`,
   `page-size`, plus product filters. Read `meta.totalRecords` (30 at time of review)
   and page via `meta.totalPages` / the `links` object.

2. **Get product detail** — for any `productId` from the list, call
   `getBankingProductDetail`: `GET /banking/products/{productId}` with header `x-v: 4`.
   The response includes `features`, `constraints`, `eligibility`, `fees`,
   `depositRates`, and `lendingRates`.

## Notes

Consumer data (accounts, balances, transactions) is a separate authenticated CDR
channel restricted to accredited data recipients using OAuth2/OIDC FAPI — not covered
by this skill.
