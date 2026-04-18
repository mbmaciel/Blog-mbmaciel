# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Site Overview

Personal development blog at `blog.mbmaciel.com`, built with Jekyll using the `jekyll-theme-tactile` theme. Content is written in Portuguese. Deployed automatically via GitHub Pages on push to `master`.

## Local Development

No Gemfile is committed — the site relies on GitHub Pages' default Jekyll environment. To run locally, you need Ruby + Jekyll installed:

```bash
jekyll serve        # Serve at http://localhost:4000 with live reload
jekyll build        # Build static output to _site/
```

If adding gems locally, create a `Gemfile` pinned to the `github-pages` gem to match the production environment.

## Architecture

- **No `_posts/` directory** — articles are root-level Markdown files (e.g., `hibrido-nativo.md`, `melhor-linguagem.md`)
- **Theme:** `jekyll-theme-tactile` handles all layouts and styles; no custom `_layouts/`, `_sass/`, or JS assets in this repo
- **Plugin:** `jekyll-mentions` (configured in `_config.yml`) — enables `@username` mention syntax
- **Navigation and social links** are configured entirely in `_config.yml`
- `index.md` is the homepage and manually links to all articles

## Content Conventions

- Articles are standalone `.md` files at the repo root with Jekyll front matter (`layout`, `title`)
- New articles must be manually linked from `index.md`
- Content language is Portuguese (pt-BR)
