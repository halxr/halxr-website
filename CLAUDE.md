# halxr-website

Public marketing site for Halxr. Audience: accelerator programs and investors. Owners: Joseph diTommaso (@jditommaso1), Patrick Myers (@pmyers16). Product code is in the private `halxr/HAL` repo.

## What HAL is (the positioning the site must carry)

- HAL is a **VR learning platform**. VR is central, not a side feature: the site should feel immersive and spatial.
- Every lesson is generated for one student; the platform continuously learns how that student learns and adapts teaching in real time. It could replace or supplement the one-teacher-many-students model (teacher shortages, teaching to the middle leaves fast and slow students behind).
- The deeper value is an **information system**: learning data becomes a capability profile (the "signal") that helps employers, admissions and programs tell candidates apart now that cover letters are AI-written and GPAs aren't comparable across schools. Frame it as student-owned and shared by choice.
- Headsets aren't named; say "VR" / "immersive" / "headset".
- HAL's in-lesson AI is the **agentic teacher** (founders' term, 2026-10-21). Don't call it a tutor or voice tutor. Research about "tutors" (e.g. the VanLehn stat) keeps its original wording.

## Tone and design

- Direction: **"Learner field"** (chosen 2026-10-22 after several rounds). Clean, futuristic, professional, warm and human. Not quirky, not busy, no gimmicks (no glow, floor grids, floating panels, textures, handwriting fonts).
- Avoid AI-default looks: near-black + acid green, cream + serif + terracotta, teal + orange, purple gradients, Inter/Space Grotesk/Instrument Serif/Fraunces/DM Sans. Ground design choices in HAL's subject and explain them.
- Color system: white page, ink text (#0e0f12), greys. The only color is the **learner color**: each visit picks a hue from a curated list and sets `--hue` on `:root`; `--field` (oklch L 0.52) is dark enough for white text at every hue, `--field-soft` / `--field-tint` are pale versions. Use the learner color sparingly (hero field, dots, the "now" roadmap card, chips, profile bars).
- Hero: a "learner fingerprint" field (48 dots, brighter = mastered) for an example learner, labeled illustrative, with an "Another learner" button.
- VR: "Inside HAL" is a light, calm explorable 360° lesson space (six stations; drag/swipe/arrow keys), tinted with the learner color, with an "agentic teacher" card. Labeled as an illustration until real in-headset footage exists. Headsets aren't named.
- Type: Host Grotesk (headings and body), Martian Mono at 87.5% width (labels). Headlines are tight (negative tracking), no italics.
- Earlier designs are tagged in git: `dark-design-v1`, `light-design-v2`.

## Code

- Static site: `index.html`, `styles.css`, `favicon.svg`, `images/`. No framework, no build step. The only JavaScript is the small inline script that picks the visit's learner (color + fingerprint), draws the 30-student comparison, and drives the 360° view; keep JS minimal.
- Hosted on GitHub Pages from `main` (root), served at https://www.halxr.com. `.nojekyll` disables Jekyll processing.
- Must work at phone width (16px side gutters, no horizontal scroll) and respect `prefers-reduced-motion`.

## Content rules

- Never publish claims we can't back up (traction numbers, partners, customer logos, results). Placeholders are marked with [brackets]; mock data (e.g. the capability profile) is labeled "illustrative".
- Draft state: the `noindex` meta tag and the "Draft" top bar stay until both founders approve. Custom domain: www.halxr.com (connected 2026-10-23; the `CNAME` file in the repo root must stay, or the domain disconnects). The bare halxr.com needs four A records at Namecheap (185.199.108-111.153); GitHub then redirects it to www.
