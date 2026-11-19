# Talk Shop website

This folder contains the new static website source. It is deliberately separate from the existing `docs/` GitHub Pages site so that the current publication is not disturbed while the new design is developed.

## Architecture

- Eleventy generates static HTML at build time.
- Page content is written in Markdown under `src/`.
- Styling and the dossier animation are CSS-only.
- No JavaScript is delivered to visitors.
- The Cloudflare Pages security headers are in `src/_headers` and are copied to the published site.

## Local preview

From this folder:

```sh
npm install
npm run build
npx @11ty/eleventy --serve
```

The local preview is normally available at http://localhost:8080.

## Cloudflare Pages settings

When ready to connect Cloudflare Pages to this GitHub repository:

- Production branch: `main`
- Root directory: `website`
- Build command: `npm run build`
- Build output directory: `_site`

Do not change the existing GitHub Pages configuration in `docs/` during this development phase.

## Editing content

- Homepage: `src/index.md`
- Individual programme pages: `src/programmes/*.md`
- Shared visual design: `src/styles/site.css`
- Shared page layouts: `src/_includes/layouts/`

Edit Markdown for wording. Edit CSS only for visual changes.
