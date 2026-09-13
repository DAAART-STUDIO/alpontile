# Deployment

## Production

The production project is:

```text
Ristorante al Pontile
```

Repository:

```text
https://github.com/DAAART-STUDIO/alpontile
```

Official website:

```text
https://ristorantealpontile.com/
```

## Repository model

This repository is independent from the donor repository.

The donor project was used only as a technical and visual foundation. The donor Git history and remote are not part of this repository.

The production repository must not contain the internal `AGENTS.md` workflow file.

## Deployment model

The site is a static frontend. Deployment consists of publishing the repository's production files to the configured web host.

No server-side application or build pipeline is required by the current architecture.

## Pre-deployment checks

Before every production release:

### Git

```bash
git status
git remote -v
```

Verify:

- correct repository;
- correct branch;
- no unintended files;
- no donor `.git` history;
- `AGENTS.md` is not tracked.

### Frontend

Verify:

- `index.html` loads;
- all CSS files load;
- all JavaScript modules load;
- all image paths resolve;
- favicon works;
- manifest works;
- responsive layouts work;
- language switching works;
- reservation/contact actions point to verified destinations.

### Content

Verify current:

- restaurant name;
- address;
- telephone;
- email;
- official website;
- reservation URL;
- menu;
- opening hours;
- social profiles;
- map location.

Do not publish unverified claims.

### SEO

Verify:

- `<title>`;
- meta description;
- `lang`;
- canonical, if used;
- Open Graph metadata, if used;
- `robots.txt`;
- `sitemap.xml`;
- `site.webmanifest`;
- favicon and brand assets.

## Static hosting notes

The repository includes `.nojekyll` for static-hosting compatibility.

If GitHub Pages is used for a preview environment, configure the appropriate source branch and directory in GitHub Pages settings.

The production domain remains:

```text
https://ristorantealpontile.com/
```

## Release principle

Make small logical commits.

Example:

```bash
git add README.md docs/
git commit -m "docs: adapt documentation for Ristorante al Pontile"
git push
```

Content, assets and code changes should be committed separately when practical.
