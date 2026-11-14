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
