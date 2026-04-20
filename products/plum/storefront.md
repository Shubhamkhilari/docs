# Plum — Storefront & Marketplace

## Storefront Models

Plum supports multiple storefront/marketplace models depending on how the customer wants to fund rewards and what experience end users should have.

| Model | Description | Best For |
|---|---|---|
| **Company-Funded Rewards Marketplace** | Customer funds rewards via points; users redeem points against global catalog (points have monetary value) | Loyalty programs, employee/partner marketplaces with structured rewarding and budget control |
| **Virtual Points Marketplace** | Points have no monetary value; users unlock deals/discounts and pay themselves | Engagement/gamification programs — high participation without reward liability or pre-funding |
| **Discounted Deal Store** | Users buy discounted deals using money (no points) | "Perks" programs offering value via discounts without managing a points economy |
| **Standard Storefront** | Whitelabeled/configurable storefront with catalog, banners, points rules, language, currencies | Fastest go-live with robust redemption UX and strong governance |
| **Custom Storefront** | Bespoke storefront built to customer requirements on Plum's catalog + fulfillment backend | Banks/fintech/large enterprises needing differentiated UX, curated journeys, stricter governance |

---

## Storefront Capabilities

### Branded Points Currency
Customers can brand the points currency (e.g., "ABCCoins"). Aligns with customer brand vocabulary and improves adoption — especially for loyalty and fintech ecosystems.

### Point-to-Currency Conversion Control
Admin configures conversion ratios between points and currency — globally or per category. Lets customers promote certain categories, manage margins, and tune perceived value.

### Tier-Based Catalog Visibility
Different user tiers (e.g., Gold/Platinum) see different catalog sets or reward availability. Creates differentiated benefits for high-value users; supports loyalty tier strategies.

### Wallet Recharge & Budget Tracking
Admin funds and tracks marketplace budgets. Ensures predictable spending control and reduces reward disruption due to low balance.

### Min/Max Points per Category
Admin defines minimum and maximum points usage constraints by reward category. Steers redemptions toward preferred categories and manages cost exposure.

### Minimum Points Contribution + Payment Gateway Split
Admin enforces a rule like "at least X% must be paid via points" — remaining paid by user via payment gateway. Common in fintech to drive adoption of their payment instrument while offering incentives.

### Global Catalog Depth (20+ categories)

| Region | Most Requested Categories |
|---|---|
| India | Gift cards, merchandise, prepaid cards |
| USA | Gift cards, prepaid cards, swags |
| META | Gift cards, flights, hotels, airmiles |
| SEA | Gift cards |
| UK/Europe | Gift cards, prepaid cards, wellness, gym |

| Use Case | Preferred Categories |
|---|---|
| Banking & fintech loyalty | Entire catalog across categories |
| Employee R&R | Gift cards, merchandise, swags, wellness, gym |
| Sales and channel incentives | Cashouts, prepaid cards, gift cards, travel |
| Employee gifting | Swags, merchandise, gift cards |
| Gaming rewards | Cashouts, gift cards |
| Survey rewards | Prepaid cards, gift cards |
| Client gifting | Swags, merchandise |

### Multilingual & Multi-Currency Support
Supports multiple languages and currencies for global rollouts with localized experiences.

### Personalized Reward Suggestions
Storefront shows personalized reward recommendations. Improves discovery and reduces time-to-redeem.

### RBAC (Role-Based Access Control)
Different teams (HR, marketing, finance, ops) have controlled permissions. Enforces least-privilege access.

### Approval-Based Redemption
Redemptions can be routed for approval before processing. Travel categories (flights/hotels) require special handling due to dynamic pricing.

### Admin Portal Governance
- Catalog management controls
- Maker-checker governance for sensitive catalog changes
- Real-time reporting and analytics on redemption and program performance

---

## Storefront Integration (SSO + APIs)

### How It Works End-to-End

1. Customer redirects an authenticated user into Xoxoday's hosted storefront via SSO/SAML
2. Once landed, Xoxoday calls customer's APIs to:
   - Fetch user's points/balance
   - Deduct points when user redeems
   - Validate user identity/profile at checkout
   - Credit back points if order can't be fulfilled

**Why:** Customer keeps their own points engine/ledger as the source of truth. Xoxoday provides the global multi-category storefront and handles catalog/fulfillment.

### APIs Provided by Xoxoday
| API | Purpose |
|---|---|
| SSO Redirection API | Authenticates and redirects user into storefront; creates account if doesn't exist |

### APIs Required from the Client
| API | Purpose |
|---|---|
| Get Balance API | Xoxoday fetches user's accrued points available for redemption |
| Update Redemption API | Xoxoday posts points spent when user places an order (includes order ID + order details) |
| Get Profile API | Validates user identity at checkout; can return balance if Get Balance is not called separately |
| Refund API | Xoxoday credits back points if order can't be fulfilled (tied to original Order ID) |

### Integration Documentation
- About Storefront Integration: https://developers.xoxoday.com/reference/about-marketplace-integration
- SSO Redirection API: https://developers.xoxoday.com/reference/sso-redirection-api
- Get Balance API: https://developers.xoxoday.com/reference/get-balance-api-1
- Update Redemption API: https://developers.xoxoday.com/reference/update-redemption-api
- Get Profile API: https://developers.xoxoday.com/reference/get-profile-api
- Refund API: https://developers.xoxoday.com/reference/refund-api
- Setup environment (storefront): https://developers.xoxoday.com/docs/set-up-your-environment-copy-2
- Create API key (storefront): https://developers.xoxoday.com/docs/create-your-api-key-copy-2

### Security Controls
- **IP allowlisting:** Xoxoday provides IPs used to call client APIs (staging + production)
- **Domain allowlisting:** Xoxoday provides domains used in staging and production
