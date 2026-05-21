# CV · Abdelrahman Ahmed

Persoonlijke CV-website, gebouwd in vanilla HTML, CSS en JavaScript. Geen build-tools, geen frameworks. Eén bestand: `index.html`.

## Structuur

```
cv/
├── index.html          ← Complete site (HTML + inline CSS + inline JS)
├── README.md           ← Dit bestand
└── .gitignore          ← Mac/IDE/env exclusions
```

## Design system

Hetzelfde systeem als het portfolio (muminstudio.com), voor merkconsistentie:

- **Kleur**: navy ink `#1f2937` × terracotta accent `#b8502d`
- **Fonts**: Fraunces (display), Inter Tight (body), JetBrains Mono (labels)
- **Modes**: light en dark, met OS-fallback
- **Grid**: 8pt spacing scale

## Lokaal openen

Open `index.html` direct in een browser. Geen server nodig.

Voor live-reload tijdens werken: gebruik de "Live Server" extensie in VS Code.

## Deployen op GitHub Pages

1. Maak een repo aan op GitHub (bijvoorbeeld `cv` of `abdelrahman-cv`)
2. Push deze map naar de repo
3. In repo Settings → Pages → Source: `main` branch, root folder
4. Wacht 1-2 minuten
5. Site staat live op `https://abdelrahman-cmd.github.io/cv/` (of de naam die je kiest)

## Wijzigen

- **Tekst aanpassen**: zoek in `index.html` op de tekst zelf, vervang, sla op
- **Kleur aanpassen**: zoek `--accent:` (regel ~80) in de inline `<style>`, wijzig hex-code
- **Nieuwe rol toevoegen**: kopieer een `<article class="role">` blok, vul in
- **Sectie verbergen**: zet `<section>` tijdelijk in een HTML-comment

## Hosting

GitHub Pages is gratis en voldoende voor deze site (statisch, één bestand).
