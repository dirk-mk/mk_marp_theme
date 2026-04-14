# MarleenKookt — Marp Presentatiethema

Officieel Marp-thema voor MarleenKookt. Alle huisstijlkleuren, logo's en typografie zijn ingebakken in één CSS-bestand. Delen = één bestand kopiëren.

---

## Installatie (2 stappen)

### Stap 1 — Kopieer het thema
Zet `themes/marleenkookt.css` op een vaste plek op je computer, bijvoorbeeld:
```
~/Documenten/marp-themes/marleenkookt.css
```

### Stap 2 — Registreer het thema in Cursor of VS Code
Open je settings (via `Cmd+Shift+P` → *Open User Settings (JSON)*) en voeg toe:

```json
"markdown.marp.themes": [
  "/absoluut/pad/naar/themes/marleenkookt.css"
],
"markdown.marp.allowLocalFiles": true
```

Of gebruik de `.vscode/settings.json` die in dit project al aanwezig is — dan werkt het direct als je deze map opent in Cursor.

Herstart Cursor daarna één keer.

---

## Nieuwe presentatie maken

Maak een `.md` bestand aan en begin met deze frontmatter:

```markdown
---
marp: true
theme: marleenkookt
paginate: true
lang: nl-NL
---
```

Zie `example.md` voor een volledig werkend voorbeeld.

---

## Slide-stijlen

| Class | Gebruik | Markdown |
|---|---|---|
| `title` | Voorblad met groot logo + dikke accentbalk | `<!-- _class: title -->` |
| `section` | Donkere tussenslide voor nieuwe sectie | `<!-- _class: section -->` |
| `quote` | Grote geciteerde uitspraak of klantreview | `<!-- _class: quote -->` |
| `cols` | Twee-kolomindeling met kopregel | `<!-- _class: cols -->` |
| *(geen)* | Standaard contentslide | — |

### Twee kolommen (`cols`)
```markdown
<!-- _class: cols -->

## Slide titel

### Linker header

Linker tekst hier.

### Rechter header

Rechter tekst hier.
```

---

## Huisstijlkleuren

| Naam | HEX | Gebruik |
|---|---|---|
| Dark olive | `#4b4910` | Hoofdkoppen, accenten |
| Olive | `#999a36` | Accentbalk, secundair |
| Moss | `#b2b360` | Lichte accenten |
| Burgundy | `#7a1b21` | Subkoppen, links, `em` |
| Taupe | `#a49c87` | Paginanummers, subtekst |
| Goud | `#e7b239` | Bullets, quote-balk, highlights |
| Offwhite | `#f8f5ee` | Achtergrond |

---

## Lettertypen

- **Koppen** — Playfair Display (serif, elegant)
- **Body** — Lato (sans-serif, leesbaar)

Worden automatisch geladen via Google Fonts. Werkt offline niet; voeg dan een lokale fallback toe.

---

## Voor AI — kopieer dit als systeemprompt

> Plak dit blok in Cursor (Rules), Claude Projects (System Prompt) of aan het begin van je gesprek. De AI weet dan precies hoe hij presentaties voor MarleenKookt moet maken.

```
Je maakt Marp-presentaties voor MarleenKookt met het thema "marleenkookt".

## Technisch
- Altijd beginnen met deze frontmatter:
  ---
  marp: true
  theme: marleenkookt
  paginate: true
  lang: nl-NL
  ---
- Slides scheiden met ---
- Slide-klassen zet je BOVEN de content: <!-- _class: title -->

## Beschikbare slide-stijlen
- title       → voorblad (h1 = hoofdtitel, h2 = subtitel, p = datum/auteur)
- section     → donkere tussenslide voor nieuwe sectie (h1 of h2)
- quote       → grote blockquote, ideaal voor klantreviews
- cols        → twee kolommen (h2 = brede titel, h3 = kolomkop, p = kolomtekst)
- (geen)      → standaard contentslide

## Tone of voice MarleenKookt
- Schrijf in ik-vorm: "Ik kook graag voor je"
- Persoonlijk en warm, maar efficiënt — geen franje
- Gebruik "jij" niet "jullie"
- Tegenwoordige tijd, actief taalgebruik
- Geen superlatieven ("werelds lekkerste")
- Concrete voordelen benoemen ("vanaf €8,75 per maaltijd")
- Sluit elke presentatie af met een duidelijke call-to-action

## Huisstijlkleuren (ter referentie, de CSS regelt dit automatisch)
- Achtergrond: #f8f5ee (offwhite)
- Koppen: #4b4910 (dark olive)
- Accenten: #7a1b21 (burgundy)
- Highlight: #e7b239 (goud)

## Structuur van een goede presentatie
1. Title slide — pakkende h1, korte h2 ondertitel
2. Kern in 3–5 contentslides — één idee per slide, max 3 bullets
3. Tussenslides (section) om blokken te scheiden
4. Quote slide — reviewcitaat of merkbelofte
5. Afsluitslide — concrete call-to-action

## Voorbeeld twee-kolommen slide
<!-- _class: cols -->

## Voordelen op een rij

### Voor jou
Elke dag een verse maaltijd zonder boodschappen doen.

### Voor je gezin
Kinderen eten mee zonder morren.
```

---

## Bestanden in dit project

```
mk_marp_theme/
├── themes/
│   └── marleenkookt.css     ← het thema (deel dit bestand)
├── assets/
│   ├── logo_marleenkookt.png        ← volledig logo (voor- en achtergrond referentie)
│   └── logo_marleenkookt_icon.png   ← icon-only logo (reguliere slides)
├── .vscode/
│   └── settings.json        ← Cursor/VS Code instellingen
├── example.md               ← voorbeeldpresentatie
└── README.md                ← deze pagina
```

---

*MarleenKookt — Minder stress. Meer tijd. Goed eten.*
