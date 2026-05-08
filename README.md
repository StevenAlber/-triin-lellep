# TRIIN LELLEP — Private Vocal Works

Maailmaklassi staatiline veebisait. GitHub Pages-valmis.
Kolm keelt. Stripe + krüpto + pangaülekanne integreeritud.
Klikitav kalender päevavalikuga. OG-plaadid, favicon-pakett, PWA manifest.

---

## FAILID

| Fail | Roll | Keel |
|---|---|---|
| `index.html` | Pealeht (primaarne) | Inglise |
| `fr.html` | Prantsuse versioon | Français |
| `zh.html` | Hiina versioon | 中文 |
| `circle.html` | The Écoute Circle (patroonide leht + maksed) | Inglise |
| `commissions.html` | Commissions leht — kalender + booking form | Inglise |
| `CNAME` | Custom domeen GitHub Pages jaoks | — |
| `.nojekyll` | GitHub Pages konfiguratsioon | — |
| `site.webmanifest` | PWA manifest | — |
| `favicon.ico`, `favicon-16/32.png`, `favicon.png` | Brauseri ikoonid | — |
| `apple-touch-icon.png` | iOS Home Screen ikoon (180px) | — |
| `icon-192.png`, `icon-512.png` | PWA / Android ikoonid | — |
| `og/og-index.jpg` | OG plaat — pealeht (EN) | — |
| `og/og-fr.jpg` | OG plaat — prantsuse | — |
| `og/og-zh.jpg` | OG plaat — hiina | — |
| `og/og-circle.jpg` | OG plaat — Écoute Circle | — |

---

## ARHITEKTUUR

- **Master brand:** TRIIN LELLEP
- **Descriptor:** Composer-Soprano · Private Vocal Works
- **Format language:** Private Écoute
- **First programme:** Opus I
- **Patron layer:** The Écoute Circle (31 places, €141k)
- **Commission tiers:** Intime (€35–55k) · Privé (€75–120k) · Souverain (€180–300k)
- **Languages:** English · Français · 中文

---

## OG / SOCIAL SHARING

Iga leht (välja arvatud commissions, mis kasutab pealehe OG-plaati) saadab WhatsApp/Telegram/Slack/X jagamisel oma konkreetse OG-pildi:

- pealeht → `og-index.jpg` (TRIIN LELLEP, By Private Invitation)
- fr.html → `og-fr.jpg` (TRIIN LELLEP, Sur invitation privée)
- zh.html → `og-zh.jpg` (TRIIN LELLEP, 凭私密邀请)
- circle.html → `og-circle.jpg` (The Écoute Circle, €250 / €1,000 / €3,000)
- commissions.html → `og-index.jpg` (jagab pealehe plaati — eraldi commissions OG saab tulevikus lisada)

Twitter Card on `summary_large_image` formaadis. Canonical URL ja hreflang viited on igas keeleversioonis.

### Pärast deploy'd testi OG-plaate

- WhatsApp: saada link iseendale → peaks näitama OG-plaati
- Facebook Debugger: https://developers.facebook.com/tools/debug/?q=https://triinlellep.studio
- LinkedIn Inspector: https://www.linkedin.com/post-inspector/
- X (Twitter) Card Validator: https://cards-dev.twitter.com/validator

Kui esimese saatmise järel pilti ei näidata, kasuta debugger'i "Scrape again" nuppu, et sotsiaalmeedia cache värskendada.

---

## INDEX.HTML SEKTSIOONIDE JÄRJEKORD

1. Hero
2. Negation ("It is not...")
3. Pull Quote
4. The Work — kategooria tutvustus
5. **What Happens in the Room** — konkreetne 90-minuti seletus
6. Three Formats
7. Architecture (5 liigutust)
8. The Artist (bio + portree-koht)
9. **From the Artist** — Triinu enda hääle koht (esimese isikus)
10. For Hosts
11. Documentation (videod + galerii)
12. Commissions Promo
13. Invitation (Écoute Circle suunamine)
14. Footer

---

## GITHUB PAGES SEADISTUS

### 1. Loo repo
GitHub'is loo public repo (`triin-lellep`).

### 2. Lisa failid (säilita kausta-struktuur, eriti `og/`)
```bash
git init
git add .
git commit -m "Update — full OG + favicon pack on every page"
git branch -M main
git remote add origin git@github.com:STEVENALBER/triin-lellep.git
git push -u origin main
```

### 3. Pages aktiveerimine
Repo Settings → Pages → Source: `main` branch, root.

### 4. Custom domeen (`triinlellep.studio`)
DNS Gandi:
- A records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- CNAME `www` → `stevenalber.github.io`

GitHub Pages → Settings → Custom domain: `triinlellep.studio`. SSL ootab ~10 min.

---

## STRIPE INTEGRATSIOON
Vt `STRIPE_SETUP.md`.

---

## DISAIN

**Palett:**
- Burgundy `#5C2E2E` · Gold `#C9A961` · Pearl `#EDE5D5` · Black `#1C1612`

**Typography:**
- Display: Marcellus
- Display Large (hero): Cormorant Garamond
- Body serif: EB Garamond
- UI body: Inter
- Mandarin: Noto Serif SC

---

## VORMI INTEGRATSIOON

`commissions.html` vorm kasutab FormSubmit'it: `https://formsubmit.co/triinlellep@gmail.com`

Esmakordsel saatmisel saadab FormSubmit Triinule kinnituslingi, millele tuleb klikata. Pärast aktiveerimist hakkavad sissekanded automaatselt e-mailile saabuma.

---

## TRIIN — LISA OMA HÄÄL

`index.html`-i `from-artist` sektsioonis on praegu draft-tekst. See on **ainus koht** lehel kus tekst on esimese isikus, Triinu enda häälel.

Asukoht failis: otsi kommentaari `<!-- TRIIN — THIS SECTION IS YOURS. -->`.

Asenda lõik draft-tekst oma häälega — 1–3 lühikest paragrahvi, esimese isikus, isiklik. Kategooria `private écoute` jätta sisse — mitte alandama tagasi `recital`/`concert`-iks.
