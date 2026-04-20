# Plum — Admin Portal Settings & Features

## Settings Overview

| Settings Area | What You Configure | Who Uses It |
|---|---|---|
| **Verifications** | Amazon Brand KYC, compliance verification | Super Admin + compliance/ops |
| **Storefront: Branding** | Company logo, look & feel | Super Admin, Marketing/Ops |
| **Storefront: Redemption URL** | Configure URL (e.g., `stores.xoxoday.com/siemens`) | Super Admin, IT |
| **Storefront: Catalog** | Enable/disable categories, countries, denominations, subcategories | Super Admin, Program Owners, Finance |
| **Storefront: Rename points** | Rename "points" to coins/miles/stars etc. | Super Admin, Marketing/Product |
| **Storefront: Payment gateway** | Enable/disable PG during redemption | Super Admin, Finance/Compliance |
| **Notifications: Domain auth** | Authenticate sending domain for better deliverability | Super Admin, IT |
| **Notifications: Sender name** | Configure sender display name | Super Admin, Marketing/Ops |
| **Notifications: Email footer** | Add/modify/remove email footers | Super Admin, Legal/Marketing |
| **Notifications: Redemption reminders** | Configure nudge reminders for unredeemed rewards | Super Admin, CS/Ops |
| **Admins: User management** | Add/remove admins, set roles | Super Admin |
| **Admins: Threshold governance** | Create/update spending limits, reset usage | Super Admin, Finance |
| **Admins: Visibility controls** | Control who sees wallet balance and reports | Super Admin, Finance/Compliance |

---

## Storefront Settings

### Catalog Customization
Super Admin can tailor the catalog:
- Enable/disable entire categories (Gift Cards, Merchandise, Experiences, Flights, etc.)
- Enable specific countries (region-specific catalog)
- Enable specific denominations (price-based catalog control)
- Enable specific subcategories

This aligns redemption options to program intent, internal policy/compliance, and budget/margin objectives while reducing choice overload and improving conversion.

### Rename Points System
Super Admin can rename "points" terminology (e.g., coins, miles, stars). Especially useful for loyalty and banking use cases to match customer brand language.

### Payment Gateway Control
Enable or disable payment gateway during redemption:
- Disable for strict "points-only" governance
- Enable to reduce drop-offs and allow premium redemption above reward value

---

## Notifications Settings

### Domain Authentication
Admin authenticates their sending domain by adding required DNS records. Improves deliverability and reduces spam placement — directly increasing open and redemption rates.

### Redemption Reminders
Configure nudges for users with unredeemed points/codes/links/gift cards. Improves redemption rates, reduces dissatisfaction, and increases program ROI.

---

## Admin Roles & Access

### Super Admin vs Admin

| Permission | Super Admin | Admin |
|---|---|---|
| View wallet balance | Yes | Configurable |
| Access reports | Yes | Configurable |
| Add/remove admins | Yes | No |
| Set thresholds | Yes | No |
| Manage invoices | Yes | No |
| Create/send rewards | Yes | Yes |

### Threshold Controls
- Create/update thresholds, update limits, reset "amount used"
- Prevents overspend, enables delegated budgets
- Supports safe scaling across multiple program owners

---

## Verifications (KYB)

### Amazon Brand KYC
Amazon requires verification to ensure compliant usage, prevent misuse, and validate legitimate reward distribution intent. Must be completed before accessing Amazon catalog.
