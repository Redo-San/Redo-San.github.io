# redo-san.github.io

The **user site** for `Redo-San` — it owns the host root of
[`https://redo-san.github.io/`](https://redo-san.github.io/) while the main
application lives one level deeper at
[`/RedoSan-Authenticity/`](https://redo-san.github.io/RedoSan-Authenticity/).

## Files

| File | Purpose |
|------|---------|
| `index.html` | Branded landing page markup: hero, tool highlights, CTA into the app, full SEO (OG image + Twitter card, JSON-LD, canonical), security hardening (CSP / Referrer-Policy metas), PWA manifest + theme-colors, Google site verification, theme/language toggles. |
| `style.css` | Base styles extracted from the page: design tokens (dark/light), layout components, brand-mark theme swap, accessibility helpers. |
| `responsive.css` | Phone/tablet adaptation mirroring the main project's approach: safe-area insets, touch ergonomics (44px targets), breakpoints at ≤380 / ≤767 / landscape-short / 768–1023 / ≥1200. Deferred via the media=print pattern. |
| `404.html` | Smart fallback served by GitHub Pages for every unmatched path. Maps unknown paths onto `/RedoSan-Authenticity/<path>` so deep links survive. `noindex`. |
| `.nojekyll` | **Required**: disables Jekyll processing, which otherwise silently drops dot-folders — including `/.well-known/` (security.txt would 404). |
| `robots.txt` | Host-root robots policy (crawlers fetch robots.txt at the host root only) declaring the absolute project sitemap. |
| `sitemap.xml` | Host-root **sitemap index** (root landing pages + the project sitemap) so tools resolving `/sitemap.xml` against the bare host get a parseable file instead of a 404. |
| `root-pages.xml` | URL-set for host-root pages; referenced by the index above. |
| `.well-known/security.txt` | RFC 9116 security contact file (Contact ×2, Expires, Preferred-Languages, Canonical, Policy). |
| `manifest.webmanifest` | PWA manifest with 192/512 px icons incl. a maskable variant. |
| `icon-192.png`, `icon-512.png`, `og-image.png` | Generated brand assets (icons + 1200×630 social card). |
| `favicon.ico`, `assets/logo.webp` | Legacy favicon and hero logo served from the host root. |
| `humans.txt` | Site/team credits in the classic humans.txt format. |
| `llms.txt` | Structured summary for AI crawlers (emerging convention): tool catalog with canonical URLs. |

## Relationship to the main project

The application itself — 20+ tools across watermarking, fingerprinting,
provenance, DID and biometrics — is developed in
[RedoSan-Authenticity](https://github.com/Redo-San/RedoSan-Authenticity)
and published by its own Pages workflow to
`https://redo-san.github.io/RedoSan-Authenticity/`.
This repository only hosts the brand landing surface and host-root
discovery files; it does not build or mirror the app.

## License

Code here follows the project's GPL-2.0 licensing.
