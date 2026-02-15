# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static marketing website for "Solitaire Classic!" iOS app, hosted on GitHub Pages at `wizkidproductions.app`. Pure HTML/CSS with no build system, no JavaScript framework, and no dependencies.

## Deployment

- **Hosted on**: GitHub Pages (main branch)
- **Custom domain**: `wizkidproductions.app` (configured via CNAME file)
- **Deploy**: Push to `main` branch; GitHub Pages auto-deploys
- **Subtree sync from parent repo**: `git subtree push --prefix=website wizkid main` (see PUSH-TO-WIZKID.md)
- **Important**: Do NOT use Git LFS for images — GitHub Pages doesn't serve LFS files

## Architecture

Four standalone HTML pages with all CSS embedded inline (no external stylesheets):

- `index.html` — Landing page with features, screenshots, App Store link
- `rules.html` — Game rules and scoring modes
- `faqs.html` — Frequently asked questions
- `contact.html` — Contact/support page

Key non-HTML files:
- `SOLITAIRE.json` — Game configuration data (scoring, cards, ads, rewards)
- `app-ads.txt` — Ad network partnerships (ads.txt spec)
- `CNAME` — Custom domain config

## Styling Conventions

- CSS is duplicated inline in each HTML file (no shared stylesheet)
- Color palette: blue (#3498db), dark gray (#2c3e50), light background (#f5f5f5)
- Font stack: Segoe UI, Tahoma, Geneva, Verdana, sans-serif
- Responsive breakpoint at 768px
- When changing styles, update all four HTML files to keep them consistent

## External Links

- App Store: https://apps.apple.com/us/app/wizkidsolitaire/id1546560958
- Support email: infowizkidproductions@gmail.com
