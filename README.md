# fusionframe.work

Marketing site for fusionframe.work — AI-augmented delivery that actually ships.

## Structure

```
docs/           ← Static site served by GitHub Pages
  index.html
  css/
    input.css   ← Tailwind source (edit this)
    output.css  ← Compiled Tailwind (generated)
    style.css   ← Custom styles
  js/
    main.js
  images/
package.json    ← Build scripts
```

## Development

Install dependencies:

```sh
npm install
```

Watch for CSS changes during development:

```sh
npm run dev:css
```

Build minified CSS for production:

```sh
npm run build:css
```

## Deployment

The `docs/` directory is deployed to GitHub Pages. After editing HTML or adding Tailwind classes, rebuild CSS before pushing:

```sh
npm run build:css
git add docs/css/output.css
git commit
git push
```
