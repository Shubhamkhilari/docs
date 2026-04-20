# Plum — API Guide

## Overview

Plum offers 3 REST APIs for programmatic reward management.

| API | Purpose | Best For |
|---|---|---|
| **Rewards API** | Procure and send specific rewards | Full API-led fulfillment with webhook support |
| **Reward Points API** | Distribute points programmatically | Points-based ecosystems with accumulation + redemption |
| **Reward Links API** | Generate and distribute reward links | Link-based rewarding at scale |

---

## Common Foundations (All APIs)

### Environments
- **Sandbox:** Develop and test; no real transactions
- **Production:** Live issuance tied to wallet funding + compliance readiness
- Docs: https://developers.xoxoday.com/docs/set-up-your-environment

### Authentication
- OAuth 2.0 + Bearer tokens
- Access/refresh token flows supported
- Docs: https://developers.xoxoday.com/docs/authentication-2

### API Key Creation
- Credentials created from the platform (tenant-controlled)
- Docs: https://developers.xoxoday.com/docs/create-your-api-key

### Wallet Pre-Funding
- Production API usage requires pre-funded wallet in base currency
- Insufficient balance blocks issuance

### Multi-Currency
- APIs support currency handling for global catalogs
- Docs: https://developers.xoxoday.com/docs/managing-currencies

### Error Handling & Rate Limiting
- HTTP status codes + structured error responses
- Rate limiting to protect system reliability
- Error docs: https://developers.xoxoday.com/docs/error-handling-1
- Rate limiting docs: https://developers.xoxoday.com/docs/rate-limiting

---

## 1. Rewards API

**Purpose:** Procure and send rewards (gift cards, merchandise, charity, airmiles, mobile top-up, lounge, perks) directly from your system.

**Best for:** Full API-led fulfillment where the customer wants their own UX + communications, while Plum provides catalog + fulfillment.

### Key Features
- **Multiple reward categories:** Gift cards, lounge, airmiles, charity, merchandise, mobile top-up
- **Communication ownership:** Choose to have Xoxoday send email OR handle communications yourself with voucher details from API response
- **Frontend/catalog enablement:** Filter by country, price range, category, currency to build store-like UX
- **Idempotency key (PO Number):** Prevents duplicate orders on retries
- **Metadata/tags:** Add campaign ID, employee ID, cost center, CRM object ID for reconciliation
- **Webhooks:** Async order status updates (not available for Points or Links APIs)
- **Order lifecycle:** Pending → Delivered → Cancelled

### Reports & Reconciliation
- Get order details: https://developers.xoxoday.com/reference/get-order-details-api
- Get order history: https://developers.xoxoday.com/reference/get-order-history-api
- Get payment report: https://developers.xoxoday.com/reference/get-payment-report-api

### Category Documentation
- Gift cards: https://developers.xoxoday.com/reference/giftcard-api
- Lounge: https://developers.xoxoday.com/reference/lounge
- Airmiles: https://developers.xoxoday.com/reference/airmiles-api
- Charity: https://developers.xoxoday.com/reference/charity
- Merchandise: https://developers.xoxoday.com/reference/merchandise
- Mobile top-up: https://developers.xoxoday.com/reference/mobile-top-up-api

---

## 2. Reward Points API

**Purpose:** Credit reward points to recipients programmatically.

**Best for:** Points-based ecosystems where points accumulate and are redeemed on the storefront.

### Key Features
- Automate points crediting based on product events (transactions, milestones, referrals)
- Same OAuth2/Bearer token auth model as Rewards API
- Requires KYB readiness and sufficient wallet funding in production
- **Webhooks:** Not supported — use polling/report sync patterns

### Documentation
- Landing page: https://developers.xoxoday.com/docs/reward-api
- Setup: https://developers.xoxoday.com/docs/set-up-your-environment
- Auth: https://developers.xoxoday.com/docs/authentication-2

---

## 3. Reward Links API

**Purpose:** Create and distribute reward links programmatically.

**Best for:** Link-based rewarding at scale where the customer's system controls recipient identity, business rules, and communications.

### Key Features
- Programmatic link generation and distribution through customer's own channels
- Same OAuth2/Bearer token auth model
- Requires KYB readiness and sufficient wallet funding in production
- Ledger stays with customer — Xoxoday reads balance and posts deductions/refunds
- **Webhooks:** Not supported — use reporting endpoints or polling

### Documentation
- Quick start: https://developers.xoxoday.com/docs/reward-api
- Setup: https://developers.xoxoday.com/docs/set-up-your-environment
- Send first reward: https://developers.xoxoday.com/docs/send-your-first-reward

---

## API Comparison

| Dimension | Rewards API | Reward Points API | Reward Links API |
|---|---|---|---|
| Primary purpose | Procure & fulfill rewards | Issue points programmatically | Generate & distribute links |
| Webhooks support | Yes (async order updates) | Not supported | Not supported |
| Communication ownership | Xoxoday sends OR customer sends | Customer-owned (via their UX) | Customer-owned |
| Idempotency | Yes (PO Number) | Customer-side via reference IDs | Customer-side via reference IDs |
| Catalog discovery | Filter by country, price, currency, category | Points catalog API | Campaign-linked redemption |
| When to choose | Full API-led fulfillment + status tracking | Points accumulation/redemption | Easy distribution + recipient-friendly link |

---

## Quick Start Links

| Task | URL |
|---|---|
| Rewards API quick start | https://developers.xoxoday.com/docs/reward-api |
| Setup environment | https://developers.xoxoday.com/docs/set-up-your-environment |
| Create API key | https://developers.xoxoday.com/docs/create-your-api-key |
| Send first reward | https://developers.xoxoday.com/docs/send-your-first-reward |
| Authentication concepts | https://developers.xoxoday.com/docs/authentication-2 |
| Refresh/access tokens | https://developers.xoxoday.com/docs/refresh-token-access-token |
| Managing currencies | https://developers.xoxoday.com/docs/managing-currencies |
| Implementing webhooks | https://developers.xoxoday.com/docs/implementingwebhooks |
| Securing webhooks | https://developers.xoxoday.com/docs/securing-webhooks |
