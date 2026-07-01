# Quiltt GraphQL Data API

Quiltt is a fintech data platform that unifies open-banking aggregators (Plaid, MX, Finicity) behind a single GraphQL API. Clients query an end-user's Profile to read Connections, Accounts, Balances, Account Owners and Numbers, Transactions, Investment Holdings, and Statements exactly as needed, then subscribe to real-time updates as data syncs.

**Endpoint:** `https://api.quiltt.io/v1/graphql`
**Authentication:** `Authorization: Bearer <SESSION_TOKEN>` (Profile-scoped JWT session token), `Content-Type: application/json`
**Documentation:** https://www.quiltt.dev/api/graphql

- Reference: https://www.quiltt.dev/api-reference/graphql
- Explorer: interactive GraphQL Explorer in the Quiltt Dashboard (typed schema browser + query builder)
- Schema: https://github.com/api-evangelist/quiltt

The representative schema in `quiltt-schema.graphql` models the real GraphQL operations Quiltt exposes over a Profile's financial data: `profile`, `connection(s)`, `account(s)`, `transaction(s)`, and balances/holdings/statements, plus the `connectionDisconnect` / `connectionUpdate` mutations and the `connectionSynced` subscription.
