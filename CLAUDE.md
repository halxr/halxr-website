# halxr-website

Public marketing site for Halxr. Audience: accelerator programs and investors. Owners: Joseph diTommaso (@jditommaso1), Patrick Myers (@pmyers16). Product code is in the private `halxr/HAL` repo.

## What HAL is (the positioning the site must carry)

- HAL is a **VR learning platform**. VR is central, not a side feature: the site should feel immersive and spatial.
- Every lesson is generated for one student; the platform continuously learns how that student learns and adapts teaching in real time. It could replace or supplement the one-teacher-many-students model (teacher shortages, teaching to the middle leaves fast and slow students behind).
- The deeper value is an **information system**: learning data becomes a capability profile (the "signal") that helps employers, admissions and programs tell candidates apart now that cover letters are AI-written and GPAs aren't comparable across schools. Frame it as student-owned and shared by choice.
- Headsets aren't named; say "VR" / "immersive" / "headset".

## Tone and design

- Futuristic, techy, bold, intense. Never playful. It should feel like a cutting-edge AI startup site, not a pitch deck: no "market size" / "why now" / logo-wall sections.
- References the founders liked: hud.ai, mastra.ai, martini.film, browser-use.com. VR references reviewed: prismsvr.com, transfrinc.com, strivr.com, gravitysketch.com.
- VR cues are built in CSS (no footage yet): the hero's perspective floor grid and floating panels, and the explorable 360° view in "Inside HAL" (six lesson stations on a ring; drag/swipe/arrow keys to look around, HUD shows what you're facing plus a tutor line). Emphasize presence and moving around in the space; don't show split left/right-eye views (that's a recording artifact, not what users see). Replace with real in-headset footage when it exists.
- Dark-only (no light theme). Near-black background, one accent color (`--accent` in `styles.css`; change it there to re-skin), Inter Tight for headlines, JetBrains Mono for labels.
- Headline pattern: white statement + `<span class="dim">` gray continuation.
- Logo is the text "HAL" with a blinking block cursor for now.

## Code

- Static site: `index.html`, `styles.css`, `favicon.svg`, `images/`. No framework, no build step. The only JavaScript is the small inline script that cycles the hero console tabs, tilts the hero scene toward the pointer, and drives the 360° view; keep JS minimal.
- Hosted on GitHub Pages from `main` (root). `.nojekyll` disables Jekyll processing.
- Must work at phone width (16px side gutters, no horizontal scroll) and respect `prefers-reduced-motion`.

## Content rules

- Never publish claims we can't back up (traction numbers, partners, customer logos, results). Placeholders are marked with [brackets]; mock data (e.g. the capability profile) is labeled "illustrative".
- Draft state: the `noindex` meta tag and the "Draft" top bar stay until both founders approve. Custom domain (halxr.com) is not connected yet.
