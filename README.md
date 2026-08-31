# fusionframe.work

Marketing site for fusionframe.work. GitHub Pages serves the repository root.

## Structure

```
index.html            ← Home page (enterprise audience)
services/index.html   ← Services firms page
redesign/             ← Redirect stubs for the old /redesign/ URLs
archive/              ← Superseded page, kept for reference
explainer/            ← Standalone explainer page
css/
  input.css           ← Tailwind source (edit this)
  output.css          ← Compiled Tailwind (generated)
site/
  css/                ← Styles for archive/
  js/                 ← Script for archive/
  images/             ← Screenshots, favicon, Open Graph image
sitemap.xml
robots.txt
CNAME
```

Both live pages hold their own custom CSS in a `<style>` block. Tailwind supplies
the utility classes. `css/input.css` lists the files that Tailwind scans. If you add
a page, add an `@source` line for it, or its classes do not compile.

## Development

Install the dependencies:

```sh
npm install
```

Serve the site:

```sh
python3 -m http.server 8080
```

Watch for CSS changes during development:

```sh
npm run dev:css
```

## Deployment

A push to `main` deploys the site. Rebuild the CSS before you push:

```sh
npm run build:css
git add css/output.css
git commit
git push
```
