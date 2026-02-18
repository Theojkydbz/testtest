# testtest

A [Tailwind CSS v4](https://tailwindcss.com) + [Vite](https://vite.dev) project deployed to GitHub Pages.

## Live site

**https://theojkydbz.github.io/testtest/**

> The site is automatically rebuilt and redeployed on every push to `main`.

## Local development

```bash
npm install
npm run dev
```

Then open http://localhost:5173/testtest/ in your browser.

## Build

```bash
npm run build   # outputs to dist/
npm run preview # preview the production build locally
```

## How deployment works

Pushing to `main` triggers the GitHub Actions workflow (`.github/workflows/deploy.yml`), which:

1. Installs Node 22 and runs `npm ci`
2. Runs `npm run build` — Vite compiles the app and Tailwind purges unused CSS
3. Uploads the `dist/` folder to GitHub Pages
