# BCU Bank (bcu-bank)

BCU Bank is a customer-owned banking brand operated by Police & Nurses Limited (ABN 69 087 651 876), the mutual bank formed when Bananacoast Community Credit Union merged into the P&N Group. Headquartered on the New South Wales north coast, BCU serves retail and business members with everyday accounts, savings, home and personal lending, and cards. As an Authorised Deposit-taking Institution (ADI) it is a Consumer Data Right (CDR) Data Holder, exposing a public Product Reference Data API and supporting consumer data sharing to accredited data recipients under Australia's Open Banking regime.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bcu-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bcu-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Data Right
- Consumer Banking
- Mutual Bank
- Australia

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### BCU Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data (PRD) API conforming to the DSB Consumer Data Standards. `GET /banking/products` (and `/banking/products/{productId}`) returns BCU's openly available banking products — transaction and savings accounts, residential mortgages, personal loans and cards — with fees, rates and eligibility. Confirmed live (HTTP 200, `x-v` up to 5, 76 products, brand "BCU").

- **Human URL:** [https://www.bcu.com.au/consumer-data-right-policy](https://www.bcu.com.au/consumer-data-right-policy)
- **Base URL:** `https://public.cdr-api.bcu.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking Products
- Public API

#### Properties

- [Documentation](https://www.bcu.com.au/consumer-data-right-policy)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#cdr-banking-api_get-products)
- [OpenAPI](openapi/bcu-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### BCU Bank CDR Consumer Data Sharing API

Authenticated Consumer Data Right banking data-sharing surface (accounts, balances, transactions, direct debits, payees and payment scheduling) defined by the DSB Consumer Data Standards. Not public — access is restricted to CDR Accredited Data Recipients acting on explicit member consent via the CDR OAuth2/OIDC FAPI authorization and consent flow.

- **Human URL:** [https://www.bcu.com.au/consumer-data-right-policy](https://www.bcu.com.au/consumer-data-right-policy)
- **Base URL:** `https://public.cdr-api.bcu.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Consumer Data Sharing
- OIDC
- FAPI

#### Properties

- [Documentation](https://www.bcu.com.au/consumer-data-right-policy)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#cdr-banking-api)
- [OpenAPI](openapi/bcu-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.bcu.com.au/)
- [About](https://www.bcu.com.au/about/)
- [Documentation](https://www.bcu.com.au/consumer-data-right-policy)
- [LinkedIn](https://www.linkedin.com/company/bcu)
- [Blog](https://www.bcu.com.au/news-and-media/)
- [Terms of Service](https://www.bcu.com.au/important-information/terms-and-conditions/)
- [Privacy Policy](https://www.bcu.com.au/important-information/privacy/)
- [Support](https://www.bcu.com.au/help-centre/)
- [Contact](https://www.bcu.com.au/contact/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
