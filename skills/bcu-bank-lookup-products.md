---
name: Look up BCU banking products (public)
description: Read BCU's publicly available banking products and their fees, rates and eligibility from the public CDR Product Reference Data API - no authentication required.
api: openapi/bcu-bank-cds-banking-products-openapi.yml
operations:
  - listBankingProducts
  - getBankingProductDetail
---

# Look up BCU banking products

BCU's Product Reference Data (PRD) is a **public, unauthenticated** CDR endpoint. Use it to browse and compare BCU's openly available products (transaction/savings accounts, mortgages, personal loans, cards).

Base URL: `https://public.cdr-api.bcu.com.au/cds-au/v1`

## Rules

- No auth. Do **not** send a bearer token.
- Send the CDS version header `x-v: 3` (the supported version for products; the server responds with the version it served in `x-v`, and returns **406** if the requested version is unsupported). Optionally send `x-min-v`.
- Results are paginated with `page` and `page-size` (default 25, max 1000); read `meta.totalPages` / `meta.totalRecords` and follow `links.next`.
- Errors come back as `{ "errors": [ { "code", "title", "detail" } ] }` with CDR `urn:au-cds:error:*` codes (see `errors/bcu-bank-problem-types.yml`).

## Steps

1. **List products** - call `listBankingProducts` (`GET /banking/products`). Optionally filter with `product-category`, `effective`, `updated-since`, `brand`, and page with `page` / `page-size`. Iterate pages until `links.next` is null.
2. **Get product detail** - for a product of interest, call `getBankingProductDetail` (`GET /banking/products/{productId}`) using the `productId` from step 1 to retrieve full fees, rates, features, constraints and eligibility.
