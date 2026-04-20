# Plum — Reward Types

Plum supports four reward distribution formats. Clients choose based on their program requirements.

---

## Comparison Table

| Capability | Reward Points | Reward Codes | Reward Links | Gift Cards (Direct) |
|---|---|---|---|---|
| Send individually | Yes | Yes | Yes | Yes |
| Bulk send via CSV | Yes | Yes | Yes | Yes |
| Scheduled sending | Yes | Yes | Yes | Yes |
| Channels (Email/SMS/WhatsApp) | Yes | Yes | Yes | Yes |
| Recipient must login | Yes | No | No | Per brand rules |
| Guest checkout | No | Yes | Yes | Per brand rules |
| Partial redemption | Yes | Yes | No | Per brand rules |
| Multiple instruments per checkout | Yes | Yes (up to 10 codes) | N/A | Per brand rules |
| Top-up with payment gateway | Yes | Yes | N/A | Per brand rules |
| Campaign feature | No | Yes | Yes | No |
| Category-level catalog restriction | Yes | Yes | Yes | N/A |
| Send physically (printed) | No | Yes | No | Per brand rules |
| Redemption experience customization | Yes | Yes | Yes | No |
| Email template customization | Yes | Yes | Yes | Yes |
| "Send to self" (admin distributes) | No | Yes | Yes | Yes |
| Reports & analytics | Yes | Yes | Yes | Per brand rules |
| Wallet deducted on generation | Yes | Yes | Yes | Yes |
| Wallet deducted on redemption | Yes | Yes | Yes | No |
| Transferability | No | Yes (if not domain-restricted) | Yes (if not domain-restricted) | Yes |
| Cancellation & refund | Yes (if unused) | Yes (if unused) | Yes (if unused) | Per brand rules |
| REST API support | Yes | No | Yes | Yes |

---

## 1. Reward Points (Xoxo Points)

Points allocated to recipients who redeem on the marketplace/storefront.

**Best for:**
- Repeat rewards to the same user (points accumulate)
- Programs where recipient email IDs or phone numbers are known
- Maximum security — points strongly tied to recipient login
- Login is mandatory for redemption

**Admin capabilities:**
- Send via email, SMS, WhatsApp — individually or bulk via CSV
- Schedule sends in advance
- Customize email subject, message, logo, banner, SMS/WhatsApp message, CTA
- Choose from predefined banners or upload new ones
- Access reward points reports
- Re-trigger/resend from reporting workflows
- Integrate via Reward Points APIs

---

## 2. Reward Codes (Xoxo Codes)

Value-backed alphanumeric codes (e.g., `XO234ZYT67`) that recipients redeem via guest checkout.

**Best for:**
- Lowest-friction redemption (no login required)
- High flexibility: partial redemption, combine up to 10 codes, add payment gateway for top-up
- Physical or digital distribution
- Program consistency and governance via campaign-based controls
- Transferable if not attached to email or domain

**Admin capabilities:**
- Send via email, SMS, WhatsApp — individually or bulk via CSV
- Physical distribution via PDF export (printable codes)
- Physical reward code cards (printed code + QR for scan-to-redeem)
- Eligibility control — tag to recipient email, mobile, or domain
- Expiry configuration
- Scheduled sending
- Campaign-based catalog and branding controls
- Guest checkout with or without login
- Email customization (Subject, Logo, Banner, Body, CTA)

**Redemption features:**
- Guest checkout — no login friction
- Partial redemption — use part of the value, save rest
- Combine up to 10 codes in one checkout
- Code + Payment Gateway — pay difference for items above code value

---

## 3. Reward Links (Xoxo Links)

A unique redemption link per recipient issued under a Reward Link Campaign.

**Best for:**
- Simple, unique, shareable link per recipient
- One-click redemption — minimal options, less friction
- Lightweight branding controls without custom storefront
- Recipient binding via email/mobile/domain tagging
- Scalable distribution with bulk upload and tracking

**Admin capabilities:**
- Multi-channel delivery: Email, SMS, WhatsApp
- Recipient binding to tag links to an identity
- Bulk send via CSV
- "Send to self" — admin stores links and distributes via their own channels
- Scheduled sending
- Create campaigns with single-category catalog rule (no mixing)
- Fixed denomination per campaign
- Branding — logo, background colors, email customization
- Integrate via Reward Links APIs

---

## 4. Brand Gift Cards / Direct Gifting

Send a specific brand or category voucher directly to recipients.

**Best for:**
- Programs that need to send a specific gift card or category (not the full Xoxoday catalog)
- End users redeem directly at brand website or offline store — no Xoxoday touchpoint needed

**Admin capabilities:**
- Send individually or bulk via CSV
- Select gift card product/brand, enter value and quantity
- Edit email subject, CTA, banner, body copy
- Integrate via Brand Gift Card APIs
- Track funding, transactions, and details in the Payments module
