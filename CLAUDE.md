# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
pnpm dev          # start dev server at localhost:5173
pnpm build        # production build (targets Vercel)
pnpm preview      # preview production build locally
pnpm check        # type-check with svelte-check
pnpm lint         # prettier + eslint check
pnpm format       # auto-format all files
```

There are no tests in this project.

## Stack

- **SvelteKit 2** with Svelte 5, TypeScript, file-based routing
- **Tailwind CSS v4** via `@tailwindcss/vite` (imported as `@import 'tailwindcss'` in `app.css`)
- **Deployed to Vercel** via `@sveltejs/adapter-vercel`
- **Fira Mono** (`@fontsource/fira-mono`) as the global monospace font; `font-family` is set to `var(--font-mono)` globally in `app.css`

## Architecture

### Layout system

`src/routes/+layout.svelte` is the root shell. It conditionally renders a fullscreen `<img>` background (sepia-filtered, `position: fixed, z-index: -1`) on `/` and `/about` only — the archive page has its own background layer. The `Header.svelte` component (nav + title banner) renders on every page.

### Pages

Three pages, each self-contained:

- **`/` (home)** — fullscreen concert photo background + responsive title art overlaid via `Header.svelte`. Content is a `position: fixed; bottom: 0` panel anchored to the bottom of the viewport. Panel uses `max-height` so it sizes to content.
- **`/about`** — same fullscreen photo + panel pattern as home, different photo.
- **`/archive`** — no photo background; uses a CSS gradient (`radial-gradient` + `linear-gradient`) defined as `.background-fixed-layer` inside the page. Long scrollable catalog document in Courier New.

### Header / Nav

`Header.svelte` has two responsibilities that coexist in one component:

1. **Nav bar** — a single `<nav>` element styled as a trapezoid using `clip-path: polygon(...)`. No SVG elements. Active page is indicated by a CSS `::before` downward-pointing triangle.
2. **Title banner** — a `<picture>` element with three responsive image sources (`title-mobile.png`, `title-tablet.png`, `title-full.png`), positioned `absolute; z-index: -1` so it sits between the background photo and the nav.

### Styling conventions

- Page-scoped styles live in each `+page.svelte` `<style>` block (Svelte's default scoping).
- Global design tokens are CSS custom properties in `app.css` (colors, font stacks, column width).
- The archive page overrides the global font to `'Courier New'` to reinforce the typewriter/card-catalog aesthetic. Home and about panels also use Courier New locally.
- Tailwind utility classes are used sparingly (mostly `text-sm`, `text-xs`, `pb-*`, `text-center`).
