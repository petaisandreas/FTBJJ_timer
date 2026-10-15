# FT BJJ Timer

Round timer for FT BJJ Limassol. Works offline and installs to a phone home screen.

Live: https://petaisandreas.github.io/FTBJJ_timer/

## How to use it on a phone

Open the link, then use the browser menu and **Add to Home Screen**. After that it
opens fullscreen like an app, keeps the screen awake while a round is running, and
works with no connection.

## Changing the look

- **Logo**: replace `logo.png` (white logo on a transparent background works best).
  The file name must be all lowercase: GitHub Pages treats `logo.PNG` and `logo.png`
  as different files.
- **Colour**: open `index.html`, find `:root {` near the top, and change `--accent`
  (the Start button, active badge and round shields). `--accent-text` is the text drawn
  on top of it, so keep it dark against a light accent.
- **Name shown on screen**: the `brand-name` and `brand-sub` lines in `index.html`.

After changing any file, bump `CACHE_VERSION` in `sw.js` (`-v2` to `-v3`) so phones
that already installed it pick up the new version.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app: layout, styles and timer logic |
| `sw.js` | Service worker; makes it work with no connection |
| `manifest.webmanifest` | Name and icons used when installed to a home screen |
| `logo.png` | Header logo and background watermark |
| `icon-*.png` | Home-screen icons |
| `*.mp3` | Round start, 10-second warning, round end, get-ready |
