# TRIIN LELLEP — Private Vocal Works

Maailmaklassi staatiline veebisait. GitHub Pages-valmis. Kolm keelt. Stripe + krüpto + pangaülekanne integreeritud. Klikitav kalender päevavalikuga.

---

## FAILID

| Fail | Roll | Keel |
|---|---|---|
| `index.html` | Pealeht (primaarne) | Inglise |
| `fr.html` | Prantsuse versioon | Français |
| `zh.html` | Hiina versioon | 中文 |
| `circle.html` | The Écoute Circle (patroonide leht + maksed) | Inglise |
| `commissions.html` | Commissions leht — klikitav kalender + booking form | Inglise |
| `CNAME` | Custom domeen GitHub Pages jaoks (`triinlellep.studio`) | — |
| `.nojekyll` | GitHub Pages konfiguratsioon | — |

---

## ARHITEKTUUR

- **Master brand:** TRIIN LELLEP
- **Descriptor:** Composer-Soprano · Private Vocal Works
- **Format language:** Private Écoute
- **First programme:** Opus I
- **Patron layer:** The Écoute Circle (31 places)
- **Tiers:** Intime · Privé · Souverain
- **Languages:** English · Français · 中文

---

## KALENDRI KLIKITAVUS (commissions.html)

Kalendri lahtrid on nüüd klikitavad nupud. Patron klikib kuule → avaneb modal ühe selle kuu päevadega → klikib päeva → modal sulgub, vorm `Preferred Date` täidetakse, leht scrollib formile, kuupäeva väli helendab korraks kuldselt.

**Loogika:**
- **Available** kuud → kõik tulevased päevad klikitavad, kuldsed nädalavahetused esiletõstetud
- **Limited** kuud → samuti, aga modal'i pealdis hoiatab et kohti vähe
- **Held** kuud → samuti, aga vormi `Context` välja ette lisatakse `[selected from held month — please confirm availability]`
- **Booked** (Asia Chapter, juuni 2026) → mitte-klikitav, näitab et kuu on suletud
- Mineviku päevad on hägused ja klikitamatuid

**Kuude staatuste muutmiseks** muuda lihtsalt `commissions.html` failis vastavate `<button class="cal-cell ...">` blokkide `data-status` ja `cal-status` klassi.

---

## GITHUB PAGES SEADISTUS

### 1. Loo uus repo

GitHub'is loo uus public repo, näiteks `triin-lellep`.

### 2. Lisa failid

```bash
git init
git add .
git commit -m "Launch — Private Vocal Works + clickable calendar"
git branch -M main
git remote add origin git@github.com:STEVENALBER/triin-lellep.git
git push -u origin main
```

### 3. Lülita Pages sisse

Repo Settings → Pages → Source: `main` branch, root.

### 4. Custom domeen — `triinlellep.studio`

`CNAME` fail on juba kaasas. DNS-is (Gandi) sea:
- `A` records `triinlellep.studio` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `CNAME` `www` → `stevenalber.github.io`

GitHub Pages → Settings → Custom domain: `triinlellep.studio`, salvesta, ootad SSL'i (~10 min).

---

## STRIPE INTEGRATSIOON (circle.html)

Vt eraldi `STRIPE_SETUP.md` faili.

---

## DISAIN

**Palett:**
- Burgundy `#5C2E2E` · Gold `#C9A961` · Pearl `#EDE5D5` · Black `#1C1612`

**Typography:**
- Display: **Marcellus**
- Serif: **Cormorant Garamond**
- Body: **EB Garamond** + **Inter**
- Mandarin: **Noto Serif SC**

**Animatsioonid:** fadeUp staggered, scroll-aware nav, hover micro-interactions, modal backdrop blur.
**Mobiil:** Täielikult responsive, hero plokk lõplikult tsentreeritud.

---

## VORMI INTEGRATSIOON

`commissions.html` vorm kasutab FormSubmit'it: `https://formsubmit.co/triinlellep@gmail.com`

Esmakordsel saatmisel saadab FormSubmit Triinule kinnituslingi, millele tuleb klikata kontode aktiveerimiseks. Pärast seda hakkavad kõik vormi sissekanded automaatselt e-mailile saabuma.
