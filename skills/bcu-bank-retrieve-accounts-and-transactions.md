---
name: Retrieve consented accounts, balances and transactions
description: As a CDR Accredited Data Recipient, retrieve a consented customer's BCU accounts, balances and transactions over the authenticated CDR banking data-sharing surface.
api: openapi/bcu-bank-cds-banking-products-openapi.yml
operations:
  - listBankingAccounts
  - getBankingAccountDetail
  - listBankingBalancesBulk
  - getBankingBalance
  - listBankingTransactions
  - getBankingTransactionDetail
---

# Retrieve consented accounts, balances and transactions

This flow reads a consumer's BCU banking data. It is **only** usable by a CDR Accredited Data Recipient acting on an active, explicit consumer consent - not by the general public.

## Prerequisites

- A CDR consent (Authorisation) has been established for the customer, granting the required scopes (see `scopes/bcu-bank-scopes.yml`):
  `bank:accounts.basic:read`, `bank:accounts.detail:read`, `bank:transactions:read`.
- OAuth2 authorization-code + PKCE access token (bearer), OIDC identity, and **MTLS** to the resource server, per FAPI 1.0 Advanced (see `authentication/bcu-bank-authentication.yml`).
- On every call send the FAPI headers: `x-fapi-interaction-id` (a fresh UUID you generate and correlate on), `x-fapi-auth-date`, `x-fapi-customer-ip-address`, plus the CDS `x-v` version header.

## Conventions

- Pagination: `page` / `page-size`, follow `links.next`, read `meta.totalRecords`.
- Version negotiation: set `x-v`; a **406** means the requested version is unsupported.
- Errors: CDR `{ "errors": [...] }` envelope with `urn:au-cds:error:*` codes (`errors/bcu-bank-problem-types.yml`).

## Steps

1. **List accounts** - `listBankingAccounts` (`GET /banking/accounts`). Optionally filter by `product-category`, `open-status`, `is-owned`. Collect each `accountId`.
2. **Account detail** (optional) - `getBankingAccountDetail` (`GET /banking/accounts/{accountId}`) for full features, terms, fees and account-holder detail (requires `bank:accounts.detail:read`).
3. **Balances** - `listBankingBalancesBulk` (`GET /banking/accounts/balances`) for balances across all consented accounts, or `getBankingBalance` (`GET /banking/accounts/{accountId}/balance`) for one account.
4. **Transactions** - `listBankingTransactions` (`GET /banking/accounts/{accountId}/transactions`) with `oldest-time` / `newest-time` / `min-amount` / `max-amount` / `text` filters; page through results.
5. **Transaction detail** - `getBankingTransactionDetail` (`GET /banking/accounts/{accountId}/transactions/{transactionId}`) for extended detail on a specific transaction.
