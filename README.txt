TRIIN LELLEP STUDIO — STUDIO-MUDELI ÜLEMINEK
=============================================
2026-05-16 (õhtune fix-pakk)

KOLM SUUREMAT MUUDATUST:

1. KONTAKTID — kogu otse-kontakt Triiniga eemaldatud
   ---------------------------------------------------
   - Triini Eesti telefon: EEMALDATUD kõikidest lehtedest
   - Triini isiklik gmail: EEMALDATUD
   - Asendatud: inquiries@triinlellep.studio
   - "Write to Triin" / "Écrire à Triin" / "致信特林" → "Write to the Studio" / 
     "Écrire au Studio" / "致信工作室"
   - Footer pealkiri "Private Inquiries" → "The Studio" (vastavad keeled)

   See viib brändi tippartisti-mudelisse: kogu suhtlus käib läbi stuudio.

2. OPEN GRAPH PILDID — sotsiaalmeedia ja messaging linkid
   ---------------------------------------------------------
   Lisatud kolm OG-pilti (1200×630) kausta og/:
     og-index.jpg   (inglise)
     og-fr.jpg      (prantsuse)  
     og-zh.jpg      (hiina)
   
   HTML viitab juba neile faili-teedele. Nüüd kui keegi jagab linki
   WhatsApp / Telegram / iMessage / Twitter / LinkedIn -is, kuvatakse
   ilus eelvaade Triini portreega.

3. SCHEMA.ORG STRUKTUREERITUD ANDMED
   ----------------------------------
   Lisatud JSON-LD plokk index.html / fr.html / zh.html sees.
   Sisaldab: Person (Triin), MusicComposition (Opus I), Service 
   (Private Écoute), WebSite. See aitab Google'il, ChatGPT-l, 
   Claude'il, Perplexity'l Triini õigesti esindada otsingutulemustes.


GITHUB-IS:
  1. Loo repo's uus kaust nimega "og" (kui pole)
  2. Lae üles 3 OG-pilti kausta og/
  3. Asenda repo juurkausta järgmised 6 HTML-faili:
     - index.html
     - fr.html
     - zh.html
     - support.html
     - support-fr.html
     - support-zh.html
  4. Commit otse main-i

OLULINE — STUUDIO E-MAIL:
  inquiries@triinlellep.studio peab tegelikult olemas olema.
  Sea see üles oma DNS-i kaudu (Gandi, kust domeen tuli):
    - Lihtsaim viis: forward'i see oma KRYONIS-mail-i või Triini gmail-i juurde
    - Email forwarding tasuta enamasti Gandi paketis
    - Sätte koht Gandi: domeen → Email forwarding → Add forwarding


MUUD MÄRKUSED (vajab käsitsi kontrolli):

  - circle.html ja commissions.html — pole selles paketis, kuna pole 
    minu töökeskkonnas. KONTROLLI NEED LEHED REPOS — kui sealt leiad 
    "triinlellep@gmail.com" või "+372 5557 5590", asenda samuti.
    Saada need failid mulle, kui tahad et ka need uuendaks.

  - Stripe Payment Links — endiselt asendamata support*.html failides.
    Kui veel pole loonud: REPLACE_WITH_LISTEN_25 / RESONATE_50 / 
    CARRY_150 / WITNESS_450


----
KRYONIS Sovereign Systems · Mai 2026
