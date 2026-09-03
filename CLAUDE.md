# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install          # install dependencies
npm run docs:dev      # start local dev server with hot reload
npm run docs:build    # build static site to docs/.vitepress/dist
npm run docs:preview  # serve the production build locally
```

There is no test suite or linter configured in this repository.

## Architecture

This is a [VitePress](https://vitepress.dev/) documentation site — a static site
generator that renders Markdown files under `docs/` into a Vue-powered site.

- `docs/*.md` — page content. Each file becomes a route (e.g. `docs/guide.md` → `/guide`).
- `docs/.vitepress/config.mts` — site-wide config: title, description, nav bar,
  sidebar, and theme options (`themeConfig`). Nav/sidebar links and page files
  must be kept in sync manually — adding a new page does not automatically add
  it to the nav or sidebar.
- `docs/.vitepress/cache` and `docs/.vitepress/dist` are build output/cache
  (gitignored) — never edit these directly.
- `docs/index.md` uses VitePress's special `layout: home` frontmatter for the
  hero landing page; other pages use the default doc layout.
