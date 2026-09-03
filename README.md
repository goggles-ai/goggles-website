# goggles-website

A documentation site for Goggles, built with [VitePress](https://vitepress.dev/).

## Development

```bash
npm install
npm run docs:dev
```

This starts a local dev server (URL is printed in the terminal) with hot reload.

## Building

```bash
npm run docs:build
```

Outputs the static site to `docs/.vitepress/dist`.

## Preview a production build

```bash
npm run docs:preview
```

## Content

Pages live in `docs/` as Markdown files. Site config (nav, sidebar, theme) is in
[`docs/.vitepress/config.mts`](docs/.vitepress/config.mts).
