# TRIIN LELLEP — Private Vocal Works

Maailmaklassi staatiline veebisait. GitHub Pages-valmis.
Kolm keelt. Stripe + krüpto + pangaülekanne integreeritud.
Klikitav kalender päevavalikuga.

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

## INDEX.HTML SEKTSIOONIDE JÄRJEKORD

1. Hero
2. Negation ("It is not...")
3. Pull Quote
4. The Work — kategooria tutvustus
5. **What Happens in the Room** — konkreetne 90-minuti seletus (uus)
6. Three Formats
7. Architecture (5 liigutust)
8. The Artist (bio + portree-koht)
9. **From the Artist** — Triinu enda hääle koht (uus, esimese isikus)
10. For Hosts
11. Documentation (videod + galerii)
12. Commissions Promo
13. Invitation (Écoute Circle suunamine)
14. Footer

---

## GITHUB PAGES SEADISTUS

### 1. Loo repo
GitHub'is loo public repo (`triin-lellep`).

### 2. Lisa failid
```bash
git init
git add .
git commit -m "Update — What Happens + From the Artist sections"
git branch -M main
git remote add origin git@github.com:STEVENALBER/triin-lellep.git
git push -u origin main
```

### 3. Pages aktiveerimine
Repo Settings → Pages → Source: `main` branch, root.

### 4. Custom domeen
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
