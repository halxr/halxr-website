# halxr-website

Public marketing site for Halxr. Audience: accelerator programs and investors. Owners: Joseph diTommaso (@jditommaso1), Patrick Myers (@pmyers16). Product code is in the private `halxr/HAL` repo.

## What HAL is (the positioning the site must carry)

- HAL is a **VR learning platform**. VR is central, not a side feature: the site should feel immersive and spatial.
- Every lesson is generated for one student; the platform continuously learns how that student learns and adapts teaching in real time. It could replace or supplement the one-teacher-many-students model (teacher shortages, teaching to the middle leaves fast and slow students behind).
- The deeper value is an **information system**: learning data becomes a capability profile (the "signal") that helps employers, admissions and programs tell candidates apart now that cover letters are AI-written and GPAs aren't comparable across schools. Frame it as student-owned and shared by choice.
- Headsets aren't named; say "VR" / "immersive" / "headset".
- HAL's in-lesson AI is the **agentic teacher** (founders' term, 2026-10-21). Don't call it a tutor or voice tutor. Research about "tutors" (e.g. the VanLehn stat) keeps its original wording.

## Tone and design

- Direction: **"HAL console"** (2026-11-05). The site matches HAL's own product screens, the Main Menu and Student Portal mockups in Confluence (Product Visualizations), so the site and the product look like one thing. Clean, futuristic, professional, warm and human. Not quirky or busy.
- Look: pale field (#f6f8fa) with white rounded tiles (28px radius, 2px #d6dee5 border, soft shadow); HAL blue for selection (#1a9ee0 fills, #0f78b3 text and buttons); amber for "previous/due", green for gains. Curved top bar (sticky nav) and curved bottom dock (footer), as on the main menu. Selected/HAL tiles get a blue border plus a pale blue ring.
- Logo: the trident mark next to "HAL" (an inline SVG `<symbol id="trident">`, also the favicon). It is still a placeholder from the mockups.
- Type: same as the product mockups: Sora (headings and big numbers, 600, tracking -0.01em) and Lexend (body, labels and small numbers; uppercase labels at 0.14em tracking). No monospace font. Text colors pass WCAG AA; check new colors before using them for text.
- Hero: the headline, then a concept mockup of HAL's main menu (Learn / Assignments / Student Portal tiles and the dock) for a sample student, "Maya R." The Signal section shows a Student Portal card (radar chart, this vs last quarter). Both are labeled as concept mockups with sample data. Don't use a founder's name as the sample student.
- VR: "Inside HAL" is a light, calm explorable 360° lesson space (six stations; drag/swipe/arrow keys) with an "agentic teacher" card. Labeled as an illustration until real in-headset footage exists. Headsets aren't named.
- Earlier designs are tagged in git: `dark-design-v1`, `light-design-v2`, `learner-field-v3`.

## Code

- Static site: `index.html`, `styles.css`, `favicon.svg`, `images/`. No framework, no build step. The only JavaScript is the small inline script that runs the console clock, draws the sample student's radar charts, and drives the 360° view; keep JS minimal.
- Hosted on GitHub Pages from `main` (root), served at https://www.halxr.com. `.nojekyll` disables Jekyll processing.
- Must work at phone width (16px side gutters, no horizontal scroll) and respect `prefers-reduced-motion`.

## Content rules

- Never publish claims we can't back up (traction numbers, partners, customer logos, results). Placeholders are marked with [brackets]; mock data is labeled as a concept mockup with sample data. Every statistic links to its source (most come from the Confluence Problem Statement, Competitive Landscape and research pages). Keep the honest note that HAL has no pilot results yet until it does.
- Confluence describes an outer loop that learns across all learners in a topic. The founders' rule for the site is that both loops serve one student and no one else's curriculum changes; keep the site's wording that way unless they say otherwise.
- Draft state: the `noindex` meta tag and the "Draft" top bar stay until both founders approve. Custom domain: www.halxr.com (connected 2026-10-23; the `CNAME` file in the repo root must stay, or the domain disconnects). The bare halxr.com needs four A records at Namecheap (185.199.108-111.153); GitHub then redirects it to www.
