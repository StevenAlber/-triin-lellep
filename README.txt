TRIIN LELLEP STUDIO — UUENDUS 2026-05-16
=========================================

Selles paketis on uued / uuendatud failid triinlellep.studio jaoks.


1. MIS ON UUT
-------------

Kolm uut keelelist Toe-lehte (€25 / €50 / €150 / €450 ühekordsed tier'id):
  support.html       (inglise)
  support-fr.html    (prantsuse)
  support-zh.html    (hiina)

Iga Tugi-lehel on:
  - 4-lugu helipleier (Triini varasematest lugudest)
  - 4 tier'i koos Stripe-link kohaga
  - Vaikne sõnum Triinilt
  - Linke Circle ja Commissions lehtedele

Kolm uuendatud peamist lehte:
  index.html         (inglise — täielik versioon, lisatud Appearance-sektsioon
                     ja Tugi-link nav-i + footer-isse)
  fr.html            (prantsuse — sama struktuur nagu inglise, sealhulgas
                     Appearance, What Happens, From the Artist, Glimpse,
                     Documentation lightbox)
  zh.html            (hiina — sama struktuur, Noto Serif SC tüpograafia)

Uus visuaalne element — täisekraani portree:
  appearance-1200.jpg / .webp     (1200px lai)
  appearance-2000.jpg / .webp     (2000px lai, retina)
  appearance-poster-1600.jpg/webp (16:9 reserv OG-piltideks)

Uuendatud galerii-pilt (asendab vana gallery-ii):
  gallery-ii-800.jpg / .webp
  gallery-ii-1600.jpg / .webp

Helifailid (Tugi-lehe pleieri jaoks):
  track-i-ticki-ticki-tock.mp3    (3:30)
  track-ii-magic.mp3              (4:07)
  track-iii-i-walk-the-fire.mp3   (2:57)
  track-iv-mountains.mp3          (3:01)


2. KUIDAS GITHUBI ÜLES PANNA
----------------------------

Kõik failid lähevad otse repo juurkausta (StevenAlber/triinlellep.studio).

Asenda olemasolevad:
  index.html, fr.html, zh.html
  gallery-ii-800.jpg, gallery-ii-800.webp, gallery-ii-1600.jpg, gallery-ii-1600.webp

Lisa uued:
  support.html, support-fr.html, support-zh.html
  appearance-*.jpg, appearance-*.webp
  appearance-poster-*.jpg, appearance-poster-*.webp
  track-*.mp3


3. STRIPE — 12 PLATSI ASENDADA
------------------------------

Iga support*.html failis on 4 nuppu, mille href on hetkel placeholder. Loo Stripe
Dashboard-is 4 Payment Link'i (€25, €50, €150, €450) ja asenda need 4 stringi
igas 3 keele-failis (kokku 12 asendust, või sama 4 linki 3 korda).

Placeholder'id failides:
  REPLACE_WITH_LISTEN_25       → Listen / Écouter / 聆听 tier (€25)
  REPLACE_WITH_RESONATE_50     → Resonate / Résonner / 共鸣 tier (€50)
  REPLACE_WITH_CARRY_150       → Carry / Porter / 承载 tier (€150)
  REPLACE_WITH_WITNESS_450     → Witness / Témoin / 见证 tier (€450)

Otsi failidest täpselt:
  href="https://buy.stripe.com/REPLACE_WITH_LISTEN_25"
  ja asenda see oma päris Payment Link URL-iga.

Sama mudel kõigis 3 keele-failis.


4. KIIRE KONTROLL ENNE LIVE
---------------------------

  □ index.html, fr.html, zh.html avanevad eraldi keeltes
  □ Appearance-sektsioon Negation-i järel näitab portreed
  □ Tugi-link nav-is ja footer-is on nähtav
  □ support*.html avab korralikult, kõik 4 lugu mängivad
  □ Stripe-nupud viivad päris checkout'i (kui placeholder'id asendatud)
  □ Photographic Archive lightbox töötab (klikk pildil, ESC sulgeb)
  □ Glimpse "Watch with sound" modal töötab (kui video on olemas)
  □ Mobiilis navigatsioon kuvab vähem itemeid, Tugi-link säilib


5. FAILIDE NIMED, MIDA EI OLE PAKETIS (jäävad samaks)
------------------------------------------------------

Need viidatakse, kuid pole muudetud — jätke repo'sse oma kohale:
  circle.html, commissions.html
  triin-portrait-800/1600.jpg/webp
  gallery-i, gallery-iii kuni gallery-viii (kõik 800/1600 .jpg/.webp)
  triin-loop.mp4, triin-full.mp4, triin-poster.jpg
  favicon.ico, manifest, og/og-*.jpg


----
KRYONIS · Mai 2026
