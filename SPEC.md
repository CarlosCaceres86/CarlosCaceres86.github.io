# Tokenz public website

## Objective and authorization
Create and publish a separate public GitHub Pages repository following Tokenz app aesthetics, as requested by the owner. Spanish informational site, mobile and desktop; not a second app runtime. Site URL https://carloscaceres86.github.io/; repository CarlosCaceres86/CarlosCaceres86.github.io (confirmed absent before creation). No purchase or download claims until release.

## Stack and structure
Plain semantic HTML, CSS and ES modules, no production dependencies/build step. index.html, styles.css, app.js, demo-state.mjs; privacy/index.html and help/index.html; assets for copied approved app graphics and local Nunito fonts/OFL; .nojekyll for static Pages. Site repository contains no backend, accounts, private app source, secrets or customer data.

## Design
Reuse Tokenz tokens: navy #101A43, teal #19B8A3 / dark #087F73, lavender #F1E9FF, mint #E8FAF7, background #F8FBFF, yellow #FFC928. Nunito typography, generous rounded cards, illustrated avatar/catalog/star/mascot, accessible 48px actions. Original compositions, no new generated raster assets. Hero, three steps, interactive illustrative board, FAQ, help and website privacy. No commercial checkout or live SaaS hosted by Pages.

## Commands
- Serve: python3 -m http.server 4173 --bind 127.0.0.1
- Logic tests: node --test tests/demo.test.mjs
- Static integrity: python3 scripts/check_site.py
- Browser validation: use installed Playwright in a real Chromium browser, desktop and mobile; inspect screenshots, links, console and horizontal overflow.
- Delivery: git commits, gh repo create CarlosCaceres86/CarlosCaceres86.github.io --public --source=. --push; enable Pages main/root with GitHub API after local verification; verify live HTTP and deployed browser.

## Style example
```css
.action { min-height: 48px; border-radius: 18px; background: var(--teal-dark); }
```
Use semantic buttons/links, accessible headings and visible focus. Demo state pure, render separate; named constants for norm points. No remote analytics, fonts, login, storage, user inputs or trackers.

## Testing and acceptance
Responsive layouts at 1440px, 768px, 390px and 320px without clipping; keyboard focus, native FAQ, navigation, demo completion/undo, insufficient reward, cancel, confirm and reset. Demo never changes app data and resets on reload. Every public resource/link resolves. Images and fonts load locally. No placeholder store link, invented email, business/legal entity, testimonials or unsupported therapeutic claims. Privacy page describes this website and clearly separates the pending app release policy. User can supply public contact email asynchronously.

## Boundaries
Always keep brand source provenance/OFL, validate before publication and verify HTTPS afterwards. Ask before publishing private information, buying domains or enabling paid services. Never publish credentials, live user content or fictitious signing fingerprints. Public repository does not imply licensing Tokenz artwork or app as open source. Android/iOS association files remain gated on actual certificate/team identifiers; do not publish dummy files or claim verified links.
