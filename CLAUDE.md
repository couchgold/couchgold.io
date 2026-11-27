# couchgold.io – Website

## Zweck
Statische Webseite für **couchgold.io**. Sie stellt Impressum und Datenschutzerklärung
für die Apps von **Couchgold** bereit (Einzelunternehmen). Die Links aus den App-Store-Einträgen
und den Apps selbst zeigen hierher.

## Stack
- Reines HTML + CSS, kein Framework, kein Build-Schritt, kein JavaScript.
- Dateien: `index.html`, `impressum.html`, `datenschutz.html`, `css/style.css`.
- Nur Systemschriften – keine externen Fonts, Skripte, Stylesheets, Bilder oder CDNs.
  Alle Ressourcen werden lokal ausgeliefert.
- Jede Seite hat eine Content-Security-Policy per `<meta>` (`default-src 'self'`, `script-src 'none'`).
  Beim Anlegen neuer Seiten übernehmen.
- Sprache: Deutsch (`lang="de"`).

## Verbindliche Regeln
- **Keine Cookies, kein Tracking, keine Analytics, keine Tracker-Pixel, keine Einbettungen
  Dritter** (YouTube, Maps, Social-Buttons o. Ä.). Das ist Voraussetzung dafür, dass die
  Datenschutzerklärung und das Fehlen eines Cookie-Banners korrekt bleiben.
- Keine externen Requests jeglicher Art. Die CSP nicht lockern.
- Keine Formulare, die Daten an Dritte senden.

## Hosting (seit 2026-11-27)
- GitHub Pages aus dem öffentlichen Repo `couchgold/couchgold.io`, Branch `main`, Ordner `/`.
- `CNAME` enthält `couchgold.io`, `.nojekyll` schaltet Jekyll ab. Veröffentlichen = `git push`.
- Domain und DNS bleiben bei INWX. Mail (`hello@couchgold.io`) läuft über INWX-Webspace
  (MX `smtp-in0/1.prod0.webspace.bz`); MX, SPF, DMARC und den Wildcard-Eintrag `*` nicht anfassen.
- Vorher (bis 2026-11-27) lag die Seite auf dem INWX-Webspace (Upload per WebFTP).
