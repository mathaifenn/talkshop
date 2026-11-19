# Talk Shop website

Static HTML/CSS website generated from Markdown with Eleventy. The published pages contain no browser-side JavaScript, third-party scripts, external CSS frameworks, remote fonts or analytics.

## Edit the content
Edit the six files in `src/programmes/`. They contain each programme's title, subtitle, outcomes, ideal audience and format. Keep their front matter fields intact unless intentionally changing page metadata. The home page structure and introductory copy are in `src/_includes/layouts/home.njk`.

## Preview locally
Requires Node.js 20 or newer:
```sh
npm install
npm run serve
```
Open the local address printed by Eleventy, normally http://localhost:8080.

## Build
```sh
npm run build
```
The generated site is in `_site/`.

## Cloudflare Pages configuration
- Repository: `mathaifenn/talkshop`
- Preview branch: `website-rebuild`
- Root directory: `website`
- Build command: `npm run build`
- Build output directory: `_site`
- Production branch: `main`, only after explicit approval and merge.

The `src/_headers` file is copied into the build output and supplies baseline security headers. Revisit the CSP if external resources are intentionally introduced.

## Portrait
The design currently uses an initials placeholder. When an approved portrait is supplied, save it as `src/assets/dr_mathai_fenn.jpg` and replace the two initials placeholders in the home layout.