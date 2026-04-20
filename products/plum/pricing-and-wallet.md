# Plum — Pricing, Wallet & Invoicing

## Wallet Model

Plum follows a **pre-funding model**. Before issuing any rewards, customers must maintain sufficient funds in their Plum wallet. Postpaid wallet credits are given on selective criteria only.

### Single Base-Currency Wallet Per Account
Every Plum account has one wallet with a single base currency (e.g., USD/GBP/INR). All funding and wallet debits happen in this base currency.

### Multi-Currency (Multi-Account Approach)
If a customer needs multiple currencies, Plum supports multiple accounts — each with its own base currency wallet. Users mapped to multiple accounts select which account to access after login verification.

> **Note:** Only Super Admin can manage wallet funding and invoices.

---

## Funding Methods

### Online (Instant)
Super Admin enters an amount and recharges the wallet using online payment methods (card/UPI/netbanking depending on geography).

### Offline (Proforma Invoice)
Super Admin generates a Proforma Invoice from the portal and completes payment offline via bank transfer/ACH. Required in enterprise procurement processes needing invoice documentation and internal approvals.

**Advanced options:**
- Add PO number and PO date on proforma invoices
- View invoice records and transaction history
- Only Super Admin can generate invoices, view transaction history, and manage invoice workflows

---

## Pricing Models

Plum uses a mix of pricing strategies depending on geography and client type.

### 1. On-Generation Model ✅ (Preferred by Xoxoday)
Wallet is deducted at the time of reward distribution/issuance.

- **How it works:** Client adds funds to wallet (e.g., $10,000 USD). Balance deducts as rewards are sent. Client is charged the full value added regardless of redemption.
- **Xoxoday earns:** Unredeemed rewards (expiry) + margin on redeemed rewards (~5%) + SaaS/implementation fees
- **Example:**
  - Client purchases $10,000 USD in rewards
  - $5,000 USD unredeemed → Xoxoday keeps $5,000
  - $5,000 USD redeemed → Xoxoday earns ~5% margin = $250
  - **Net Xoxoday revenue = $5,250 + any SaaS fees**
- **Why preferred:** Xoxoday gets money upfront; improves cash flows

### 2. On-Redemption Model (Not preferred)
Wallet is deducted only when the end user actually redeems a reward.

- **How it works:** Client is charged only on value actually redeemed. No expiry revenue for Xoxoday.
- **Xoxoday earns:** Margin on redeemed rewards + SaaS/implementation fees
- **Example:**
  - Client purchases $10,000 USD; $8,000 USD redeemed
  - Xoxoday earns ~5% margin on $8,000 = $400 + SaaS fees
- **Why not preferred:** Cash flow challenges; Xoxoday gets money only after redemption

### 3. Brand Gift Cards / Direct Categories
If client purchases specific brand gift cards or categories directly:
- Xoxoday earns margin (~4%) on the purchase value
- Client may request additional discounts on bulk purchases
- Xoxoday can charge surcharges over vendor margins (important for low-margin categories: jewellery, utilities, prepaid cards, cash cards, Amazon gift cards)

### 4. Storefront / Marketplace
- Annual SaaS + Annual maintenance
- Premium for heavy custom UI/features
- Xoxoday earns ~5% margin on redemption + surcharges on low-margin categories

### 5. Offers / Perks / Discount Marketplace
Structure options:
- Pass entire discount to client or end user → Xoxoday charges Annual SaaS + AMC
- Pass partial discount to end user only
- Pass partial to end user + partial to client
- Xoxoday earns: AMC + Annual SaaS + margin on discount purchases

---

## Pricing by Region

| Region | Standard | Custom |
|---|---|---|
| India | Margin + expiry | — |
| USA | $0–10K SaaS + margins | $10K–50K SaaS + margins |
| META/Saudi/Africa | $0–10K SaaS + margins | $10K–100K SaaS + margins |
| SEA | $0–5K SaaS + margins | $5K–50K SaaS + margins |
| UK/EU | $0–10K SaaS + margins | $10K–100K SaaS + margins |

---

## Pricing Sensitivities

Topics that commonly stall deals:
- Catalog discounts (depth and margins)
- Setup or annual costs
- Surcharge on rewards
- Expiry of unredeemed rewards
