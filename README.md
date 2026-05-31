# Quittly – Landingpage

Statische Marketing-Landingpage für Quittly. Kein Build-Schritt, kein Framework – reines HTML/CSS/JS. Direkt deploybar auf Cloudflare Pages.

## Struktur
```
index.html        – Hauptseite (Hero, Problem, Lösung, Für-wen, Schritte, Trust, FAQ, CTA)
impressum.html    – Pflicht-Impressum (Platzhalter ausfüllen!)
datenschutz.html  – Datenschutzerklärung (Vorlage, Platzhalter ausfüllen!)
```

## ⚠︎ Vor dem Live-Gang ausfüllen
- **`impressum.html`**: alle `[…]`-Felder (Name, Anschrift, ggf. USt-IdNr.). Pflicht in DE.
- **`datenschutz.html`**: Verantwortlicher, eingesetzte Analyse-Tools, Datum.
- **`index.html`**:
  - FAQ „Was kostet Quittly?" → konkrete Preise eintragen (Kommentar `<!-- TODO -->`).
  - `og:image` ergänzen, sobald Design-Asset (1200×630) da ist.
  - Phone-Mockup im Hero ist eine **CSS-Platzhalter-UI** → mit echtem App-Screenshot ersetzen (idealerweise EÜR- oder Scan-Screen aus dem Design-Briefing).
- **Empfehlung:** Google Fonts („Inter") lokal hosten → spart DSGVO-Drittlandtransfer. Aktuell via CDN eingebunden.

## Deploy auf Cloudflare Pages

### Variante A – Git (empfohlen)
1. Repo anlegen, z. B. `loopcraftsapp-blip/quitto-landing`, diesen Ordner pushen.
2. Cloudflare Dashboard → **Workers & Pages → Create → Pages → Connect to Git**.
3. Repo wählen. Build-Einstellungen:
   - Framework preset: **None**
   - Build command: *(leer)*
   - Output directory: **`/`** (Root)
4. Deploy. Danach Custom Domain `quittly.app` unter **Pages → Custom domains** verbinden (DNS bei Cloudflare).

### Variante B – Wrangler (direkt, ohne Git)
```bash
npm i -g wrangler
wrangler login
wrangler pages deploy . --project-name quitto-landing
```

## Domain
- `quittly.app` o. ä. prüfen/registrieren. DNS bei Cloudflare → automatisches SSL.

## Performance / SEO bereits drin
- Semantisches HTML, Meta-Description, OpenGraph, schema.org `SoftwareApplication`.
- Mobile-first responsive, kein Render-Blocking außer Fonts.
- FAQ als reines CSS/JS-Accordion (kein Framework).

## Nächste Ausbaustufe (siehe Werbung/_CLAUDE-CODE/AUFGABEN.md)
- `/ratgeber`-Blog für SEO (EÜR, Kleinunternehmergrenze).
- Cloudflare Web Analytics oder Plausible (DSGVO-freundlich) einbinden.
- Conversion-Tracking auf App-Store-Badge-Klick.
