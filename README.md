# Quiltt (quiltt)

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

Quiltt is a fintech data platform and abstraction layer over open-banking aggregators like Plaid, MX, and Finicity. It exposes a unified GraphQL API for reading end-user financial data (profiles, connections, accounts, balances, transactions, investment holdings, statements) plus a REST Admin/Auth API for profiles, connections, session tokens, and webhooks, and an embeddable Connector UI for account linking.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/quiltt/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/quiltt/refs/heads/main/apis.yml)

## Tags

- Fintech
- Open Banking
- Financial Data
- Aggregation
- GraphQL

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### Quiltt GraphQL Data API

Single GraphQL endpoint for reading an end-user's unified financial data - Profile, Connections, Accounts, Balances, Account Owners and Numbers, Transactions, Investment Holdings, and Statements - authenticated with a Bearer session token. Supports queries, mutations, and subscriptions.

- **Human URL:** [https://www.quiltt.dev/api/graphql](https://www.quiltt.dev/api/graphql)
- **Base URL:** `https://api.quiltt.io/v1/graphql`

#### Tags

- GraphQL
- Financial Data
- Accounts
- Transactions
- Connections

#### Properties

- [Documentation](https://www.quiltt.dev/api/graphql)
- [API Reference](https://www.quiltt.dev/api-reference/graphql)
- [GraphQL](graphql/quiltt-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [GraphQL Schema](graphql/quiltt-schema.graphql) — [GraphQL Specification](https://spec.graphql.org/)

### Quiltt Profiles API

REST Admin endpoints to list, create, retrieve, update, and delete Profiles - the container for an end-user's identity (name, email, phone, birthday, address, custom metadata) and their linked financial Connections.

- **Human URL:** [https://www.quiltt.dev/api/profiles](https://www.quiltt.dev/api/profiles)
- **Base URL:** `https://api.quiltt.io/v1`

#### Tags

- Profiles
- Users
- Admin

#### Properties

- [Documentation](https://www.quiltt.dev/api/profiles)
- [OpenAPI](openapi/quiltt-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quiltt.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quiltt.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quiltt Connections API

REST Admin endpoints to list, retrieve, and manage a Profile's Connections - the links to underlying aggregator sources (Plaid Item, MX Member, Finicity Institution Login) that back the accounts and transactions surfaced through the GraphQL API.

- **Human URL:** [https://www.quiltt.dev/api/core-resources/connections](https://www.quiltt.dev/api/core-resources/connections)
- **Base URL:** `https://api.quiltt.io/v1`

#### Tags

- Connections
- Aggregators
- Admin

#### Properties

- [Documentation](https://www.quiltt.dev/api/core-resources/connections)
- [OpenAPI](openapi/quiltt-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quiltt.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quiltt.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quiltt Session Tokens API

REST Auth endpoints to issue, verify, and revoke short-lived JWT session tokens scoped to a single Profile. Session tokens authenticate the Connector and end-user calls to the GraphQL Data API.

- **Human URL:** [https://www.quiltt.dev/authentication/issuing-session-tokens](https://www.quiltt.dev/authentication/issuing-session-tokens)
- **Base URL:** `https://auth.quiltt.io/v1`

#### Tags

- Authentication
- Session Tokens
- Auth

#### Properties

- [Documentation](https://www.quiltt.dev/authentication/issuing-session-tokens)
- [Documentation](https://www.quiltt.dev/authentication/managing-session-tokens)
- [OpenAPI](openapi/quiltt-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quiltt.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quiltt.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Quiltt Webhooks API

REST Admin endpoints to create, list, retrieve, and delete webhook subscriptions that deliver real-time events such as profile.created, connection.synced.successful, and account.verified to your endpoints.

- **Human URL:** [https://www.quiltt.dev/webhooks](https://www.quiltt.dev/webhooks)
- **Base URL:** `https://api.quiltt.io/v1`

#### Tags

- Webhooks
- Events
- Real Time

#### Properties

- [Documentation](https://www.quiltt.dev/webhooks)
- [OpenAPI](openapi/quiltt-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/quiltt.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/quiltt.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/quiltt)
- [LinkedIn](https://www.linkedin.com/company/quiltt)
- [Website](https://www.quiltt.io/)
- [Documentation](https://www.quiltt.dev)
- [Plans](plans/quiltt-plans-pricing.yml)
- [Rate Limits](rate-limits/quiltt-rate-limits.yml)
- [Fin Ops](finops/quiltt-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
