# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML presentation suite for the **Patek Philippe × The Hour Glass** digital boutique project (AKQA). It contains interactive slide decks and project tracking documents — no build tools, no package manager, no frameworks.

## Running / Viewing Files

Open any `.html` file directly in a browser. No build step required.

```bash
open home                            # Main strategic brief deck
open THG-Patek-Strategic-Brief.html  # Password-gated version of the brief
open THG-Patek-Timeline-Tracker.html # Dark-mode project tracker dashboard
open hourglass-conversation-flow.html # Project initiation flow diagram
```

## Architecture

**Tech stack:** Vanilla HTML5, CSS3 (custom properties, Grid, Flexbox), ES6+ JavaScript. No dependencies.

**`home`** — The primary deliverable. A 12-slide interactive deck split into two sections (Brief / Timeline), controlled via scroll-snap + Intersection Observer. Keyboard navigation (↑/↓ arrow keys, spacebar). Progress bar and dot navigation on right side.

**`THG-Patek-Strategic-Brief.html`** — Same deck as `home` with an added password gate layer (`#gate` div) on top.

**`THG-Patek-Timeline-Tracker.html`** — Standalone dark-mode dashboard. Shows 5 project phases, milestones, blockers/risks, and interactive action checklist. Gold accent color: `#c9a84c`.

**CSS design tokens** (defined in `:root` on all files):
- `--serif: 'Cormorant Garamond'` — display/luxury headings
- `--sans: 'Inter'` — UI and body copy
- `--black: #121212`, `--body: #414141`, `--muted: #9a9a9a`, `--rule: #e0e0e0`, `--bg: #ffffff`, `--bg-warm: #faf9f7`

**Mobile breakpoint:** `700px`.

## Key Dates

- **March 23, 2026** — Presentation to Michael Tay (approval gate); countdown timers in `home` are hardcoded to this date
- **May 31, 2026** — Target launch; second countdown timer target
