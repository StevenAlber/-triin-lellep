# Stripe Payment Setup — The Écoute Circle

The patron page (`circle.html`) is wired for Stripe Payment Links.
By default the links are placeholders — they need to be replaced with real
Stripe links before going live.

## Step-by-step setup

### 1. Create a Stripe account
- Go to [stripe.com](https://stripe.com), register
- Account in Triin's name (or registered company)
- Verify identity (passport / ID + bank account)

### 2. Generate three Payment Links

Stripe Dashboard → Payment Links → New

#### Founding Friend
- Product name: The Écoute Circle — Founding Friend
- Price: €1,000.00 EUR · One-time
- Description: Founding Friend of The Écoute Circle. Triin Lellep — Private Vocal Works.
- Collect: Customer name, email
- Confirmation: "Thank you. You are now a Founding Friend of The Écoute Circle. Triin will write to you personally within 7 days."

#### Founding Member
- Product name: The Écoute Circle — Founding Member
- Price: €5,000.00 EUR · One-time
- Description: Founding Member of The Écoute Circle.

#### Founding Patron
- Product name: The Écoute Circle — Founding Patron
- Price: €15,000.00 EUR · One-time
- Description: Founding Patron of The Écoute Circle.

### 3. Replace placeholder URLs in circle.html

Find this block near the bottom:

```javascript
const STRIPE_LINKS = {
  friend:  'https://buy.stripe.com/REPLACE_WITH_FRIEND_LINK',
  member:  'https://buy.stripe.com/REPLACE_WITH_MEMBER_LINK',
  patron:  'https://buy.stripe.com/REPLACE_WITH_PATRON_LINK'
};
```

Replace with real URLs from step 2, commit and push.

## Crypto

For BTC / ETH / USDC, the page currently shows placeholders.
Replace `bc1q__provided_on_request__` and `0x__provided_on_request__`
in circle.html with Triin's wallet addresses (Kraken Pro recommended,
see Krypto_Juhend_Triinule.pdf).

## Bank transfer

Page already shows full IBAN (EE06 2200 0011 0527 2211, Swedbank, HABAEE2X).
Patrons make transfer themselves and email confirmation.

## Closing date

Page states circle closes 31 May 2026 or when full. To close:
1. Archive Stripe Payment Links (Dashboard → Payment Links → ⋯ → Archive)
2. Update circle.html — change buttons to "Circle Closed" or remove
3. Send final email to every patron
