# Contributing

Thanks for helping improve **Digital Safety Labs**.

## Principles
- **Single-file demos**: each demo should be one HTML file (Bootstrap CDN + inline JS/CSS).
- **Offline-first**: no external network calls beyond CDNs for Bootstrap.
- **Privacy**: do not send or collect real user data.

## Conventions
- Storage key: `localStorage["DSL_<slug>_V1"]`
- Use clear events: `consent`, `subscribe`, `unsubscribe`, `phone_capture`, `tracker_ping`, `leak`, etc.
- Keep labels bilingual-ready (EN/HI) with a simple in-page dictionary.

## Workflow
1. Fork → create a feature branch → commit small, focused changes.
2. Open a PR with a short demo video or screenshots.
3. Note any strings needing translation.

## Style
- Vanilla JS only. No build step.
- Bootstrap classes for layout; minimal custom CSS.
