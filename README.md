# Ristorante al Pontile

Landing page for **Ristorante al Pontile**, Malcesine, Lake Garda, Italy.

## Project

This repository contains the production website for Ristorante al Pontile.

- **Restaurant:** Ristorante al Pontile
- **Location:** Via Gardesana, 173, 37018 Malcesine VR, Italy
- **Website:** https://ristorantealpontile.com/
- **Repository:** https://github.com/DAAART-STUDIO/alpontile
- **Languages:** Italian, English, German

The project is based on the existing DAAART STUDIO restaurant landing-page architecture. The donor is used as a technical and visual foundation; restaurant-specific content and media are replaced during the adaptation process.

## Current status

The repository currently contains the donor-based technical structure. Restaurant content, translations, metadata, imagery, contact details, menu references and other public-facing material are adapted to Ristorante al Pontile in separate logical steps.

## Technology

The site is a static frontend consisting of:

- HTML
- CSS
- Vanilla JavaScript
- JSON-based internationalization
- static image and SVG assets

No frontend framework or build system is required by the current architecture.

## Structure

```text
Alpontile/
├── assets/
│   ├── icons/
│   ├── images/
│   └── logo/
├── css/
│   ├── components/
│   ├── animations.css
│   ├── base.css
│   ├── layout.css
│   ├── reset.css
│   └── tokens.css
├── data/
│   └── i18n/
│       ├── de.json
│       ├── en.json
│       └── it.json
├── docs/
├── js/
│   ├── modules/
│   ├── app.js
│   └── config.js
├── index.html
├── robots.txt
├── sitemap.xml
├── site.webmanifest
└── favicon.ico
```

## Local development

Open the project through a local static web server rather than directly from the filesystem.

For example:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

If the repository's existing local workflow provides another static-server command, that workflow may be used instead.

## Internationalization

Translations are stored in:

```text
data/i18n/
```

Supported languages:

- `it.json` — Italian
- `en.json` — English
- `de.json` — German

Translation keys are consumed by the existing JavaScript i18n module. Keys must remain synchronized across all three language files.

## Development rules

The project follows these principles:

1. Preserve the donor architecture unless a change is explicitly required.
2. Do not modify CSS or JavaScript for cosmetic reasons.
3. Preserve existing IDs, classes, `data-*` attributes, accessibility attributes and JavaScript hooks.
4. Do not invent restaurant facts, menu items, prices, awards, history, services or events.
5. Verify public-facing restaurant information against current official sources before publishing.
6. Use real imagery of the restaurant and its actual surroundings.
7. Keep documentation aligned with the actual repository.
8. Keep `AGENTS.md` local only; it is intentionally excluded from the production repository.

## Content verification

The primary source for restaurant information is:

https://ristorantealpontile.com/

The official menu and other authoritative restaurant materials should be checked before publishing menu-related content.

Current verified contact information includes:

- Via Gardesana, 173, 37018 Malcesine VR
- +39 045 7400022
- info@ristorantealpontile.com

## Deployment

Deployment is described in [`docs/DEPLOYMENT.md`](docs/DEPLOYMENT.md).

## Documentation

- [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md)
- [`docs/DESIGN-SYSTEM.md`](docs/DESIGN-SYSTEM.md)
- [`docs/I18N.md`](docs/I18N.md)
- [`docs/DEPLOYMENT.md`](docs/DEPLOYMENT.md)
- [`docs/README.md`](docs/README.md)
