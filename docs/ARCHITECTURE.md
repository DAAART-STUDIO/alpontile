# Architecture

## Overview

Ristorante al Pontile is implemented as a static, client-side restaurant landing page.

The project preserves the donor's established HTML, CSS and vanilla JavaScript architecture while replacing donor-specific public content with verified Ristorante al Pontile content.

## Directory structure

```text
assets/
├── icons/
├── images/
│   └── content/
└── logo/

css/
├── components/
├── animations.css
├── base.css
├── layout.css
├── reset.css
└── tokens.css

data/
└── i18n/
    ├── de.json
    ├── en.json
    └── it.json

docs/

js/
├── modules/
├── app.js
└── config.js

index.html
robots.txt
sitemap.xml
site.webmanifest
favicon.ico
```

## HTML

`index.html` is the primary page document.

Existing structural classes, IDs, `data-*` attributes, ARIA attributes and JavaScript hooks are part of the application contract and should be preserved during content adaptation.

## CSS

CSS is organized into:

- global reset and base rules;
- design tokens;
- page layout;
- reusable components;
- section-specific components;
- animation rules.

The CSS architecture is inherited from the donor and is not to be refactored during normal content adaptation.

## JavaScript

JavaScript is organized around `js/app.js`, `js/config.js` and modules in `js/modules/`.

Modules cover functions such as:

- navigation;
- internationalization;
- header behavior;
- smooth scrolling;
- observers;
- theme switching;
- galleries and views;
- reservation UI;
- section-specific interactions.

The existing JavaScript architecture and hooks should remain unchanged unless a functional requirement explicitly requires modification.

## Assets

Static assets are grouped by role:

- `assets/images/content/` — visual content;
- `assets/logo/` — branding and favicon/PWA assets;
- `assets/icons/` — reusable SVG icon resources.

Restaurant imagery must represent the real Ristorante al Pontile location and must not retain donor-specific architecture or scenery.

## Data flow

The basic runtime flow is:

```text
index.html
    │
    ├── CSS
    │
    └── js/app.js
          │
          ├── JS modules
          │
          └── data/i18n/*.json
```

The browser loads the static page, initializes the JavaScript modules and loads the selected translation data.

## Architectural constraints

- No frontend framework is introduced.
- No unnecessary build system is introduced.
- Existing responsive behavior is preserved.
- Existing animation and interaction mechanisms are preserved.
- CSS and JavaScript are not changed merely to improve aesthetics.
