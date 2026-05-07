# TRIIN LELLEP — Private Vocal Works

Maailmaklassi staatiline veebisait. GitHub Pages-valmis. Kolm keelt. Stripe + krüpto + pangaülekanne integreeritud.

---

## FAILID

| Fail | Roll | Keel |
|---|---|---|
| `index.html` | Pealeht (primaarne) | Inglise |
| `fr.html` | Prantsuse versioon | Français |
| `zh.html` | Hiina versioon | 中文 |
| `circle.html` | The Écoute Circle (patroonide leht + maksed) | Inglise |
| `.nojekyll` | GitHub Pages konfiguratsioon | — |

---

## ARHITEKTUUR

- **Master brand:** TRIIN LELLEP
- **Descriptor:** Composer-Soprano · Private Vocal Works
- **Format language:** Private Écoute
- **First programme:** Opus I
- **Patron layer:** The Écoute Circle (31 places, €29,000)
- **Tiers:** Intime · Privé · Souverain
- **Languages:** English · Français · 中文

---

## GITHUB PAGES SEADISTUS

### 1. Loo uus repo

GitHub'is loo uus public repo, näiteks:
- `triin-lellep` (soovitus)
- `private-ecoute`
- `lellep`

### 2. Lisa failid

Lae üles kõik failid kausta juurest (`index.html`, `fr.html`, `zh.html`, `circle.html`, `.nojekyll`).

```bash
git init
git add .
git commit -m "Initial launch — Private Vocal Works"
git branch -M main
git remote add origin git@github.com:STEVENALBER/triin-lellep.git
git push -u origin main
```

### 3. Lülita Pages sisse

Repo Settings → Pages → Source: `main` branch, root.

Sait avaneb aadressil:
```
https://stevenalber.github.io/triin-lellep/
```

### 4. Hiljem — Triinu domeen

Kui Triin annab `triinlellep.com` auth code'i (või sa hangid eraldi domeeni nagu `triinlellep.studio`):

1. Tekita repo juurde fail `CNAME` mille sisuks ainult:
   ```
   triinlellep.com
   ```
2. DNS-is (Gandi vms) sea:
   - `A` records `triinlellep.com` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` `www` → `stevenalber.github.io`
3. GitHub Pages → Settings → Custom domain: `triinlellep.com`, salvesta, ootad SSL'i (~10 min).

---

## STRIPE INTEGRATSIOON

`circle.html` on **valmis kodeeritud** Stripe Payment Links jaoks.

### 1. Loo Stripe Payment Links

Mine: https://dashboard.stripe.com/payment-links → New payment link

Loo kolm linki:

| Tier | Hind | Toote nimi |
|---|---|---|
| Founding Friend | €250 EUR | The Écoute Circle — Founding Friend |
| Founding Member | €1,000 EUR | The Écoute Circle — Founding Member |
| Founding Patron | €3,000 EUR | The Écoute Circle — Founding Patron |

Iga lingi puhul:
- Currency: EUR
- Quantity: 1, fixed
- Collect customer info: name, email, address
- Lisa metadata: `tier=friend` / `member` / `patron`

### 2. Asenda lingid `circle.html` failis

Otsi failist:

```javascript
const STRIPE_LINKS = {
  friend:  'https://buy.stripe.com/REPLACE_WITH_FRIEND_LINK',
  member:  'https://buy.stripe.com/REPLACE_WITH_MEMBER_LINK',
  patron:  'https://buy.stripe.com/REPLACE_WITH_PATRON_LINK'
};
```

Asenda igaüks oma päris Stripe lingiga (need näevad välja umbes nii: `https://buy.stripe.com/14k5kAcDh9pKaqQfYY`).

Push GitHubisse — leht uuendub automaatselt.

### 3. Aasia maksete jaoks

Stripe Dashboard → Settings → Payment methods → lülita sisse:
- UnionPay
- Alipay
- WeChat Pay

See võimaldab Hiina patroonidel maksta otse oma kohaliku makselahendusega.

---

## PANGAÜLEKANNE

`circle.html` näitab praegu "Provided upon request" — patron klikib "Request Details" ja saadab e-posti.

**Miks request-flow on parim:**
1. Kaitseb sind spämmist
2. Loob isikliku kontakti enne suurt ülekannet
3. Sina kontrollid millise IBAN'i (EE / US / HK) saadad sõltuvalt patronist

Kui soovid IBAN'i otse näidata, otsi failist `EE__ ____ ____ ____ ____` ja asenda päris numbriga.

---

## KRÜPTOVALUUTA

Sama loogika — placeholder aadressid:
```
BTC: bc1q__provided_on_request__
ETH/USDC: 0x__provided_on_request__
```

Soovitus on jätta request-flow (KYC/AML, personaalne kontakt). Kui asendad, otsi failist need stringid.

---

## DISAIN

**Palett:**
- Burgundy `#5C2E2E` · Gold `#C9A961` · Pearl `#EDE5D5` · Black `#1C1612`

**Typography:**
- Display: **Marcellus**
- Serif: **Cormorant Garamond**
- Body: **EB Garamond**
- Mandarin: **Noto Serif SC**

**Animatsioonid:** fadeUp staggered, scroll-aware nav, hover micro-interactions.
**Mobiil:** Täielikult responsive (breakpoints 900px ja 600px).

---

## KIIRTEST ENNE LIVE'i

1. `index.html` avaneb
2. Hiina ja prantsuse versioonid töötavad (lingid navist)
3. `circle.html` avaneb
4. Stripe modaal avaneb kui klikid "Become a Friend"
5. Modal sulgub ESC-iga ja taustaklikiga
6. Mobiilis (telefonist!) navigatsioon ja layout töötavad
7. Fonts laaditakse (Google Fonts)
