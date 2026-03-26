# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Academic homepage for 王子成 (Zicheng Wang), hosted on GitHub Pages at `www.zi-c.wang`. Pure static HTML/CSS site with no build system, no framework, and no dependencies.

## Architecture

- **index.html** — Single-page site containing all content: profile, research interests, experience, publications, awards, teaching, services, and open-source projects
- **style.css** — Minimal stylesheet (~75 lines) for typography and layout
- **CNAME** — GitHub Pages custom domain configuration (`www.zi-c.wang`)
- **PDF files** — CVs (CV_EN.pdf, CV_CN.pdf) and thesis document hosted directly

## Development

No build step. Edit `index.html` directly and push to `main` branch. GitHub Pages serves the site automatically.

## Layout & Styling Conventions

- Table-based layout, fixed 840px width, centered
- Header/footer use purple background (`#6a0060`) with white text
- Content sections separated by horizontal rules or spacing rows
- Publications use reverse-chronological order with consistent formatting: authors, title in quotes, venue, year
- Author name "Zicheng Wang" is bolded in publication entries
- Google Analytics tracking is embedded (ID: G-41SYF6R2JL)
- Footer contains a "Last update" timestamp — update this when making changes

## Content Language

Bilingual site: section headers and navigation in English, some content in Chinese. Name displayed as "王子成 Zicheng Wang".
