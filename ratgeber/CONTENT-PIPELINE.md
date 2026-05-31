# Quittly SEO-Blog — Content-Pipeline & Notizen

## Was hier liegt
Statischer Ratgeber-Blog unter `/ratgeber/`. Reiner HTML, Quittly-Markenstil, je Artikel: SEO-Title + Meta-Description, `schema.org/Article` + `FAQPage`, interne Verlinkung, CTA zur App, Steuer-Disclaimer.

- `index.html` — Blog-Hub
- `kleinunternehmergrenze-2026.html` — Cornerstone 1
- `euer-kleinunternehmer.html` — Cornerstone 2

## Warum dieser Kanal (kurz)
SEO **kompoundiert**: ein Artikel zu „EÜR erstellen" zieht Monat für Monat Leute mit **Kauf-Absicht** (sie sitzen gerade an ihrer Steuer). Pro Stunde nachhaltiger als TikTok. Für Steuer-Utilities der ROI-stärkste organische Kanal neben ASA.

## ⚠︎ Wichtig
- **Keyword-Volumen nicht live verifiziert** (Semrush-Plan ohne MCP). Ziel-Keywords sind aus Erfahrung gewählt (Long-Tail, hoher Intent, für kleine Seite gewinnbar). Bei Gelegenheit in Google Keyword Planner / einem ASO-Tool gegenchecken.
- **Steuer-Fakten** sind verifiziert (Kleinunternehmergrenze 25.000/100.000 € via Finanzamt-/IHK-Quellen, Mai 2026). Bei Gesetzesänderungen Artikel aktualisieren (`dateModified` mitziehen).
- Jeder Artikel hat einen **Disclaimer** „keine Steuerberatung" — bei Steuer-Content Pflicht.

## Ziel-Keywords (Cornerstones)
| Artikel | Primär | Sekundär |
|---|---|---|
| Kleinunternehmergrenze 2026 | kleinunternehmergrenze 2026 | kleinunternehmer umsatzgrenze, 25000 euro grenze, §19 grenze |
| EÜR Kleinunternehmer | eür erstellen | einnahmenüberschussrechnung kleinunternehmer, anlage eür |

## Nächste Artikel (Pipeline, je 1/Woche)
1. **„Was kann ich als Kleinunternehmer absetzen?"** — Betriebsausgaben-Liste mit Beispielen. (hoher Intent)
2. **„Rechnung schreiben als Kleinunternehmer (§19)"** — Pflichtangaben + §19-Hinweis. (knüpft an v1.1-Rechnungsfeature → starker CTA)
3. „Kleingewerbe anmelden — die 3 Schritte" (Top-of-Funnel, frische Gründer)
4. „Belege digital aufbewahren — ist das erlaubt? (GoBD)"
5. „Kleinunternehmer & Steuererklärung — welche Anlagen?"
6. „§19 vs. Regelbesteuerung — wann lohnt sich was?"

Jeder neue Artikel: in `index.html` aus „Bald" auf aktiven Card umstellen + im jeweils passenden Cornerstone intern verlinken (Topic-Cluster).

## SEO-Hygiene-Checkliste je Artikel
- [ ] Title ≤ 60 Zeichen, Primär-Keyword vorn
- [ ] Meta-Description ≤ 155 Zeichen, mit Keyword + Nutzen
- [ ] Eine H1, sinnvolle H2/H3
- [ ] Antwort auf die Suchfrage in den ersten 2 Sätzen
- [ ] FAQ-Block + `FAQPage`-Schema (gewinnt „Andere fragten auch")
- [ ] 2–3 interne Links (Cluster) + 1 CTA zur App
- [ ] Disclaimer
- [ ] Canonical-URL gesetzt

## Deploy
Die `/ratgeber/`-Dateien gehören in **dasselbe Pages-Projekt** wie die Landingpage (gleiche Domain = SEO-Autorität auf einer Domain bündeln).
- Bei meinem Redesign: schon im selben Ordner (`/Developer/quitto-landing/`).
- Bei der **bestehenden** `quittly.app`: `/ratgeber/`-Ordner ins Live-Repo legen und mit-deployen.
- **`sitemap.xml`** ergänzen (Home + beide Artikel) und in der Google Search Console einreichen — sonst dauert die Indexierung länger.
- Nach Deploy: Search Console → URL-Prüfung → Indexierung anfordern.
