# Deploy checklist · CV website

Stap voor stap van lokale map naar live URL op GitHub Pages. Eenmalige setup.

## Voor je begint

- [ ] Bestanden uitgepakt in `~/Documents/cv/` (niet in iCloud Drive)
- [ ] VS Code geinstalleerd en gekoppeld aan je GitHub account
- [ ] Git geinstalleerd (controleer met `git --version` in Terminal)

## Stap 1 · Repo aanmaken op GitHub

1. Ga naar https://github.com/new
2. Repository name: `cv`
3. Public
4. **Belangrijk**: laat "Add README" en "Add .gitignore" leeg
5. Create repository

## Stap 2 · Lokale map koppelen aan repo

In VS Code:
1. File → Open Folder → `~/Documents/cv/`
2. Source Control tab (takje-icoon)
3. Initialize Repository
4. Stage alle bestanden (klik + naast "Changes")
5. Commit message: `Initial CV website`
6. Commit (Cmd+Enter)
7. Publish Branch → kies bestaande repo `cv`

## Stap 3 · GitHub Pages aanzetten

1. Op github.com, ga naar je repo
2. Settings tab
3. Pages (linker zijbalk)
4. Source: Deploy from a branch
5. Branch: `main`, folder `/ (root)`
6. Save

Wacht 1-2 minuten. Site komt op:

```
https://abdelrahman-cmd.github.io/cv/
```

## Stap 4 · Live test checklist

Open op telefoon én laptop. Check:

- [ ] Hero laadt netjes, dark/light mode werkt
- [ ] Op telefoon: hero copy past op het scherm
- [ ] Sectie-anchors werken (klik op "Over", "Ervaring", etc. in nav)
- [ ] Klik op "Portfolio op aanvraag" → opent mailto met onderwerp
- [ ] Klik op e-mail in contact → opent mailto
- [ ] Klik op telefoonnummer op telefoon → start belapp
- [ ] Tekst is leesbaar, geen overlap of cut-off
- [ ] Geen typefouten of verkeerde namen

## Wijzigen na deploy

Elke wijziging volgt dit ritueel:

1. Edit `index.html` in VS Code
2. Source Control: stage de wijziging
3. Commit message (bijvoorbeeld: `Update Jumbo role description`)
4. Commit
5. Sync Changes (push)

Site update binnen 1-2 minuten op GitHub Pages.

## Belangrijke link aanpassen

In `index.html` regel ~1135 staat:

```html
<a class="portfolio-link" href="mailto:dhr_abdelrahman@outlook.com?subject=Portfolio%20aanvraag">
```

Wijzig deze als je een ander e-mailadres wilt gebruiken voor portfolio-aanvragen.

## Custom domein (later, optioneel)

Wanneer je een eigen domein wilt (bijvoorbeeld `cv.abdelahmed.nl`):

1. Domein registreren bij TransIP, Hostnet, of Cloudflare
2. DNS instellen: CNAME record `cv` → `abdelrahman-cmd.github.io`
3. Op GitHub: Settings → Pages → Custom domain: typ `cv.abdelahmed.nl`
4. Wacht op verificatie (kan een paar uur)
5. Enable HTTPS

## Hulp nodig

Als iets niet werkt:
- 404 op de site URL → wacht nog een minuut, eerste deploy duurt soms langer
- Lege witte pagina → check of `index.html` in de root van de repo staat, niet in een submap
- Wijzigingen worden niet zichtbaar → ctrl+shift+R (hard refresh) of incognito tab
