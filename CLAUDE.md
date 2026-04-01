# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal academic homepage for Rui Zhao, deployed via GitHub Pages at `zhaorui.xyz`. There is no build process — all pages are hand-authored HTML files.

## No Build System

There are no build tools, package managers, or compilation steps. To preview changes, open HTML files directly in a browser or use any static file server:

```bash
python3 -m http.server 8000
```

## Site Structure

- `index.html` — main homepage (bio, current role, selected publications)
- `publications.html` — full academic publications list with BibTeX toggle
- `links.html` — professional links
- `welcome.html` — alternative landing page
- `jemdoc.css` — primary stylesheet (based on jemdoc academic site theme)
- `project.css` — supplemental styles for project pages
- `project/<name>/` — individual research project pages (HTML + PDFs + figures)
- `figures/` — profile photos and site images
- `cv_rui.pdf` — curriculum vitae

## HTML Conventions

Pages follow the jemdoc-style layout with a consistent structure:
- `<div id="layout-content">` wraps main content
- Publications use `<td class="reference">` table rows
- BibTeX entries are toggled via `showbib()`/`hidebib()` JavaScript inline on each entry
- Abstract visibility is toggled similarly with `showabs()`/`hideabs()`

## Updating Publications

Publications in `publications.html` follow a repeated HTML pattern per entry. Each entry includes:
1. Paper title (linked to PDF or project page)
2. Author list (user's name bolded as `<strong>Rui Zhao</strong>`)
3. Venue (italicized)
4. Optional links: `[PDF]`, `[Project]`, `[Code]`, `[Poster]`, `[Slides]`
5. Hidden BibTeX block toggled by a `[Bib]` link

## Deployment

Pushing to the `master` branch on GitHub automatically deploys via GitHub Pages. The domain `zhaorui.xyz` is configured via the `CNAME` file.
