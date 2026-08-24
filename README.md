# redo-san.github.io

The **user site** for `Redo-San` — it owns the host root of
[`https://redo-san.github.io/`](https://redo-san.github.io/) while the main
application lives one level deeper at
[`/RedoSan-Authenticity/`](https://redo-san.github.io/RedoSan-Authenticity/).

## Files

| File | Purpose |
|------|---------|
| `index.html` | Branded landing page: hero, tool highlights, CTA into the app, full SEO (OG, JSON-LD, canonical). |
| `404.html` | Smart fallback served by GitHub Pages for every unmatched path. Maps unknown paths onto `/RedoSan-Authenticity/<path>` so deep links survive. `noindex`. |
| `robots.txt` | Host-root robots policy (crawlers fetch robots.txt at the host root only) declaring the absolute project sitemap. |
| `sitemap.xml` | Host-root **sitemap index** pointing at the project sitemap, so tools resolving `/sitemap.xml` against the bare host get a parseable file instead of a 404. |
| `.well-known/security.txt` | RFC 9116 security contact file. |
| `favicon.ico`, `assets/logo.webp` | Brand assets served from the host root. |

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
