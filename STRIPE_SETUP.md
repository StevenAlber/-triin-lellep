# Stripe Payment Setup — The Écoute Circle

The patron page (`circle.html`) is wired for Stripe Payment Links.
By default the links are placeholders — they need to be replaced with real
Stripe links before going live.

## Why Stripe Payment Links?

- **No backend required** — works on GitHub Pages and any static host.
- **No code to write** — Stripe hosts the entire checkout flow.
- **PCI compliance** — handled entirely by Stripe.
- **International cards** — Visa, Mastercard, American Express, and most
  regional payment methods supported automatically.
- **Confirmation emails** — sent automatically by Stripe on successful payment.

## Step-by-step setup

### 1. Create a Stripe account

If Triin doesn't already have a Stripe account:
- Go to [stripe.com](https://stripe.com) and register
- The account must be in Triin's name (or a registered company)
- Verify identity (passport / national ID + bank account)

### 2. Generate three Payment Links

Go to: **Stripe Dashboard → Payment Links → New**

Create one link per tier:

#### Founding Friend
- **Product name:** The Écoute Circle — Founding Friend
- **Price:** €1,000.00 EUR · One-time
- **Description:** Founding Friend of The Écoute Circle. Triin Lellep — Private Vocal Works.
- **Collect:** Customer name, email
- **Confirmation page:** Custom message (e.g., "Thank you. You are now a Founding Friend of The Écoute Circle. Triin will write to you personally within 7 days.")

#### Founding Member
- **Product name:** The Écoute Circle — Founding Member
- **Price:** €5,000.00 EUR · One-time
- **Description:** Founding Member of The Écoute Circle.
- Same confirmation pattern.

#### Founding Patron
- **Product name:** The Écoute Circle — Founding Patron
- **Price:** €15,000.00 EUR · One-time
- **Description:** Founding Patron of The Écoute Circle.
- Same confirmation pattern.

### 3. Copy the three resulting URLs

Each link looks like: `https://buy.stripe.com/abc123XyZ...`

### 4. Edit `circle.html`

Find this block in the script section near the bottom of `circle.html`:

```javascript
const STRIPE_LINKS = {
  friend:  'https://buy.stripe.com/REPLACE_WITH_FRIEND_LINK',
  member:  'https://buy.stripe.com/REPLACE_WITH_MEMBER_LINK',
  patron:  'https://buy.stripe.com/REPLACE_WITH_PATRON_LINK'
};
```

Replace with the real URLs from step 3, then commit and push. The buttons are now live.

## Crypto wallet setup

For cryptocurrency payments (BTC / ETH / USDC), the page currently shows
placeholders that say "provided on request." This is the recommended approach —
it keeps wallet addresses private and gives Triin control over confirming
each contribution.

## Bank transfer setup

The page asks patrons to email for IBAN details. When they write, reply
with Triin's beneficiary information.

## Tracking patrons

Stripe gives Triin a dashboard with every successful payment, customer email
and name, payment date and amount. For bank transfers and crypto, keep a
simple spreadsheet tracking patron name, tier, amount, date, method, and
confirmation status.

## Closing date

The page states the circle closes **31 May 2026 or when full**. To close:
1. **Deactivate the Stripe Payment Links** (Dashboard → Payment Links → ⋯ → Archive)
2. **Update circle.html** — change the buttons to "Circle Closed" or remove them
3. **Send a final email** to every patron confirming closure
