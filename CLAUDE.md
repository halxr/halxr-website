# halxr-website

Public marketing site for Halxr. The product is HAL (personalized lesson plans and narrated lessons generated per learner; code in the private `halxr/HAL` repo). Audience: accelerator programs and investors. Owners: Joseph diTommaso (@jditommaso1), Patrick Myers (@pmyers16).

## Tone and design

- Futuristic, techy, bold, intense. Never playful. It should feel like a cutting-edge AI startup site, not a pitch deck: no "market size" / "why now" / logo-wall sections.
- References the founders liked: hud.ai, mastra.ai, martini.film, browser-use.com.
- Dark-only (no light theme). Near-black background, one accent color (`--accent` in `styles.css`; change it there to re-skin), Inter Tight for headlines, JetBrains Mono for labels.
- Headline pattern: white statement + `<span class="dim">` gray continuation.
- Logo is the text "HAL" with a blinking block cursor for now.

## Code

- Static site: `index.html`, `styles.css`, `favicon.svg`, `images/`. No framework, no build step. The only JavaScript is the small inline script that cycles the hero console tabs; keep JS minimal.
- Hosted on GitHub Pages from `main` (root). `.nojekyll` disables Jekyll processing.
- Must work at phone width (16px side gutters, no horizontal scroll) and respect `prefers-reduced-motion`.

## Content rules

- Never publish claims we can't back up (traction numbers, partners, customer logos, results). Placeholders are marked with [brackets].
- Draft state: the `noindex` meta tag and the "Draft" top bar stay until both founders approve. Custom domain (halxr.com) is not connected yet.
