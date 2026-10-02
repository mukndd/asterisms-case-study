# Asterisms Public Case Study Export

This folder is a standalone, recruiter-safe showcase package for the private Asterisms project. It contains public-facing HTML, CSS, screenshots captured from the current product (including the real-sky viewer), a high-level architecture diagram, and PDF-ready recruiter materials.

## Contents

- `index.html` - responsive public case study.
- `styles.css` - standalone styling for the case study.
- `assets/screenshots/` - current product screenshots captured from a local production build.
- `assets/diagrams/architecture.svg` - public-safe architecture diagram.
- `assets/logo/` - public brand assets copied from the app's public assets.
- `pdf/case-study.html` - PDF-ready one-to-two-page recruiter version.
- `pdf/case-study.pdf` - generated PDF, when available.

## Verified Audit Snapshot (2026-10-02)

Sources: the project's latest passing CI run on its default branch, the generated data report, and the live site.

- Live site: `asterisms.space` and its `/api/health` endpoint return 200; the real-sky routes (`/explore`, `/tonight`, `/seek`, `/find`, `/events`) are live.
- Data validation: passed with 88 constellations, 74 asterisms, 9,042 unique stars, zero warnings, zero hard failures.
- Tests: 347 passed, 1 skipped (77 test files).
- TypeScript, lint and production build: passed; the build generates 1,017 static pages plus dynamic routes.
- Celestial events almanac: 3,604 events covering 2025 to 2036.
- Astronomy cross-check: Moon and planet positions compared with NASA/JPL Horizons and USNO for five observers and dates (a representative sample, not an ephemeris certification).

`index.html` reads the starred figures live from the profile stats feed (`stats/data.json` in the public profile repository) and falls back to the values above if the feed is unreachable.

## Public-Safety Notes

This export intentionally excludes:

- application source code
- private repository links or remotes
- credential material, keys, connection strings, or account identifiers
- internal hostnames and private infrastructure identifiers
- screenshots of dashboards, consoles, errors, or local browser chrome
- internal incidents and recovery details

Personal context (role, timeline, motivation, usage) came directly from the project owner and is reflected in the case study; anything not confirmed stays out rather than being guessed at.
