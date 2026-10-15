# Trojans BJJ Timer

Round timer for Trojans Gym. Works offline and installs to a phone home screen.

Live: https://petaisandreas.github.io/bjj-timer-trojans/

## How to use it on a phone

Open the link, then use the browser menu and **Add to Home Screen**. After that it
opens fullscreen like an app, keeps the screen awake while a round is running, and
works with no connection.

## The other timer

GT's timer is a separate project, so a change to one can never affect the other:
[bjj_timer](https://github.com/petaisandreas/bjj_timer) - https://petaisandreas.github.io/bjj_timer/

## Changing the look

- **Logo**: replace `logo.png` (a square PNG, around 500x500, works best).
- **Colour**: open `index.html`, find `:root {` near the top, and change `--accent`
  (the Start button, active badge and round dots). `--accent-text` is the text drawn
  on top of it, so keep it dark against a light accent.
- **Name shown on screen**: the `<h1 class="brand">` line in `index.html`.

After changing any file, bump `CACHE_VERSION` in `sw.js` (`-v1` to `-v2`) so phones
that already installed it pick up the new version.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app: layout, styles and timer logic |
| `sw.js` | Service worker; makes it work with no connection |
| `manifest.webmanifest` | Name and icons used when installed to a home screen |
| `logo.png` | Background watermark |
| `icon-*.png` | Home-screen icons |
| `*.mp3` | Round start, 10-second warning, round end, get-ready |
