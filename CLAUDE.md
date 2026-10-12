# voodoovid.github.io

Personal games site, published with GitHub Pages from `main` (root). Every push to `main` goes live automatically.

## Layout
- `index.html` is the home page with one card per game.
- Each game lives in its own folder (`hangman/`, `scareisdale/`, …) as a self-contained `index.html`.
- To add a game: create its folder, add a card to `index.html`, and add the folder (plus any icons) to `PAGES` and its Google Fonts URL to `FONT_CSS` in `sw.js`.
- The site installs as one offline app ("Games" on the home screen): `manifest.webmanifest`, `icon-*.png` and `sw.js` at the root. Bump `CACHE` in `sw.js` whenever that file changes. Each game links back to `../` (the installed app has no Back button) and registers `../sw.js`.

## Conventions
- **Every program must show a version number** on screen, e.g. a `const VERSION = "v1.0"` shown as a small label. Bump it on every change pushed (patch/minor as appropriate) and mention the new version in the commit message.
- Games must fit on an iPhone 17 Pro Max screen (about 440×800 visible in Safari) without scrolling, and also work on iPad and desktop.
- Sound must start from a user tap (iOS rule) and should work with the iPhone/iPad Silent switch on.
