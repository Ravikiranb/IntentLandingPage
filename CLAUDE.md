# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the landing page for **Intent** — an AI-powered digital wellbeing iOS app. It is a single-file static site: one `index.html` with all CSS inlined in `<style>` and no JavaScript dependencies.

## Development

No build step. Open `index.html` directly in a browser or serve it with any static file server:

```
python3 -m http.server 8080
```

## Structure

Everything lives in `index.html`:

- **CSS custom properties** (`:root`) define the design tokens — dark background (`#000`), accent purple (`#7b5ea7`), and semantic color roles (`--text-primary`, `--text-secondary`, `--text-tertiary`).
- **Sections in order**: Nav → Hero → Phone mockup → Features grid → Stats band → How it works → Privacy → CTA → Footer.
- **Responsive breakpoint** at `768px` via a single `@media` block at the bottom of `<style>`.

## Design conventions

- Color palette: black background, purple accent (`--accent: #7b5ea7`, `--accent-light: #a07dc8`), white text.
- Cards use `var(--card)` background with `var(--card-border)` borders and hover effects (`border-color` + `translateY(-2px)`).
- The phone mockup (`.phone` / `.phone-screen`) is pure HTML/CSS — no images.
- Buttons: `.btn-primary` (white fill, black text) and `.btn-secondary` (ghost with border).
- Typography: `clamp()` for responsive `h1`/`h2` font sizes; `-apple-system` font stack.
