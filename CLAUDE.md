# halxr-website

Public marketing site for Halxr (product: personalized lesson plans and narrated lessons generated per learner; code in the private `halxr/HAL` repo). Audience: accelerator programs and investors. Owners: Joseph diTommaso (@jditommaso1), Patrick Myers (@pmyers16).

- Static site: `index.html`, `styles.css`, `favicon.svg`. No framework, no build step, no JavaScript unless needed.
- Hosted on GitHub Pages from `main` (root). `.nojekyll` disables Jekyll processing.
- Colors are CSS variables in `:root`, with a dark-mode override in `prefers-color-scheme: dark`. Keep both in sync.
- Must work at phone width (16px side gutters, no horizontal scroll).
- Never publish claims we can't back up (traction numbers, partners, results). Placeholders are marked with [brackets].
- Draft state: the `noindex` meta tag and `.draft-banner` stay until both founders approve. Custom domain (halxr.com) is not connected yet.
