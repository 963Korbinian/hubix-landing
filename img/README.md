# HUBIX · Bild-Workflow (OpenArt)

> Feste Struktur für KI-/echte Bilder auf der Marketing-Website. Owner: Chat 8 (`web:`).
> Bild-Motor: **OpenArt** (via MCP `openart`, User-Config → in allen Sessions verfügbar).

## Regeln (verbindlich)

1. **Marken-Farben immer**: Orange `#FF9F1C` · Purple `#5625a2` · Teal `#00D4BC` · Dark `#0d0a1e`.
   Prompts enthalten diese Stimmung („teal/orange glow, deep violet").
2. **🔴 Trust nie faken**: KI-Bilder nur für **Atmosphäre / Hero / Vision / Textur / Mockups** —
   NIEMALS als „echte sri-lankische Kunden/Shops" ausgeben. Echter Beweis = echte Fotos.
   (Selbe Regel wie Video-Strategie · Memory `feedback_website_theme_dark_premium` + Marketing-Strategie.)
3. **Illustrativ kennzeichnen**, wo ein Bild eine Szene andeutet (keine erkennbaren Gesichter, wo's um „echt" ginge).
4. **Marken-Stil-Konsistenz**: möglichst einen trainierten HUBIX-Stil in OpenArt nutzen, damit alles „aus einem Guss" ist.

## Ablauf (repeatable)

1. Chat 8 schreibt eine **Shot-Liste** (welche Bilder, welcher Prompt, welches Sehraster).
2. Bilder erzeugen — **Weg A**: automatisch über den OpenArt-MCP (nach OAuth) · **Weg B**: Founder generiert in OpenArt-Web und legt die Dateien hier ab.
3. Dateien in `img/` ablegen, Namensschema unten.
4. Chat 8 baut sie in `home.html` / Unterseiten ein, Screenshot → Founder-Freigabe.

## Namensschema

`hero_<thema>.webp` · `section_<name>.webp` · `bg_<name>.webp` · `og_<seite>.png` (Social-Preview).
Bevorzugt **WebP** (klein), Hero max ~1600px Breite, `loading="lazy"` außer Hero.

## OpenArt-MCP anbinden (einmalig, nur Founder)

Terminal → `claude` → `/mcp` → **openart** → **Authenticate** → mit OpenArt-Account einloggen.
Danach: „verbunden" sagen → Chat 8 testet + generiert. Status prüfen: `claude mcp get openart`.
