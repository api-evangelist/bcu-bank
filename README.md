# BCU Bank (bcu-bank)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
