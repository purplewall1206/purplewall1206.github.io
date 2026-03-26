# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Academic homepage for 王子成 (Zicheng Wang), hosted on GitHub Pages at `www.zi-c.wang`. Pure static HTML/CSS site with no build system, no framework, and no dependencies.

## Architecture

- **index.html** — Single-page site, semantic HTML5, CSS Flexbox/Grid responsive layout
- **style.css** — Design system with CSS variables, animations, responsive breakpoints (~300 lines)
- **CNAME** — GitHub Pages custom domain configuration (`www.zi-c.wang`)
- **PDF files** — CVs (CV_EN.pdf, CV_CN.pdf) and thesis document hosted directly

## Design System

- **Typography**: DM Serif Display (headings) + DM Sans (body) + JetBrains Mono (monospace), with Noto Serif/Sans SC for Chinese fallback, loaded via Google Fonts
- **Colors**: CSS variables in `:root` — primary purple `#6a0060`, accent `#c9185c`, deep purple `#4a0042`
- **Layout**: Max-width 860px centered, responsive via `@media (max-width: 700px)`
- **Animations**: Section fade-up entrance with staggered delays
- **Components**: `.news-card` (news items), `.timeline-item` (experience), `.pub-item` (publications with auto-numbering counter), `.oss-card` (open source grid), `.simple-list` (awards/teaching/services)

## Content Sections (order in index.html)

1. Hero banner (name, title, email, links)
2. Research
3. In the News
4. Experience
5. Publications
6. Awards
7. Teaching Assistant
8. Services
9. Open Source
10. Footer (last update date)

## Content Conventions

- Publications: reverse-chronological, author name wrapped in `<span class="me">` for bold highlight
- Publication venue abbreviations in `<strong>` inside `<div class="pub-venue">`
- Notable achievements use `<span class="pub-note">` badge
- News items use `.news-card` with `.news-badge` for source tag
- Footer "Last update" date must be updated on every content change

## Content Update Workflow

When adding new content (publications, news, experience, etc.), follow this workflow:

1. **Edit `index.html`** — Add content to the appropriate section using existing HTML patterns:
   - New publication: copy a `<li class="pub-item">` block, fill in title/authors/venue
   - New news item: copy the `.news-card` block, update badge/title/meta/excerpt
   - New experience: copy a `.timeline-item` block
   - New open source project: copy an `.oss-card` block
2. **Update footer date** — Change "Last update: YYYY-MM-DD" to today's date
3. **Commit and push** — `git add index.html && git commit -m "<describe change>" && git push origin main`
4. **Wait ~30s** for GitHub Pages deployment
5. **Verify** — Fetch `https://www.zi-c.wang` to confirm the update is live

### Adding External Article/News Coverage

When given a URL to add as news:
1. Fetch the URL to extract: title, author, date, summary
2. Add a `.news-card` block in the "In the News" section
3. Follow steps 2–5 above

## Content Language

Bilingual site: section headers and navigation in English, some content in Chinese. Name displayed as "王子成 Zicheng Wang".
