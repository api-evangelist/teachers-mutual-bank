# Teachers Mutual Bank (teachers-mutual-bank)

Teachers Mutual Bank is an Australian customer-owned mutual bank and a brand of Teachers Mutual Bank Limited (TMBL), an authorised deposit-taking institution (ADI) regulated by APRA that also operates UniBank, Firefighters Mutual Bank, Health Professionals Bank and Hiver. As a member-owned bank it returns value to members rather than external shareholders. Under Australia's Consumer Data Right (CDR / Open Banking), it exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Data Standards Body (DSB) Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/teachers-mutual-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/teachers-mutual-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Mutual Bank
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Teachers Mutual Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data (PRD) API for the Teachers Mutual Bank brand of Teachers Mutual Bank Limited. Exposes `GET /banking/products` and `GET /banking/products/{productId}` under the standard CDS base path, returning the bank's full banking product catalogue (30 products at time of review) as defined by the DSB Consumer Data Standards. Confirmed live (HTTP 200) with the `x-v` header set to `4` (server advertises versions 4 and 5).

- **Human URL:** [https://www.tmbank.com.au/open-banking](https://www.tmbank.com.au/open-banking)
- **Base URL:** `https://ob.tmbl.com.au/tmbank/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Consumer Data Right

#### Properties

- [Documentation](https://www.tmbank.com.au/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#banking-apis)
- [OpenAPI](openapi/teachers-mutual-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

> **Spec provenance:** The harvested OpenAPI is the shared DSB Consumer Data Standards "CDR Banking API" swagger (OpenAPI 3.0.3, version 1.36.0), captured verbatim from the Data Standards Body. It is the standard that governs the PRD endpoints — not a Teachers Mutual Bank proprietary contract. The bank publishes no own OpenAPI.

## Common Properties

- [Website](https://www.tmbank.com.au/)
- [Developer Portal](https://www.tmbank.com.au/open-banking)
- [Documentation](https://www.tmbank.com.au/open-banking)
- [LinkedIn](https://www.linkedin.com/company/teachers-mutual-bank)
- [Privacy Policy](https://www.tmbank.com.au/privacy)
- [Security](https://www.tmbank.com.au/security)
- [Support](https://www.tmbank.com.au/contact)
- [Parent Organization](https://www.tmbl.com.au/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
