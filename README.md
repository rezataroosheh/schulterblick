# Fahrprüfung 3D

Browser game for practising the German practical driving test (Klasse B).

- Interface in German, English, Arabic, Turkish, Persian, Ukrainian and Russian (chosen on the start screen). The examiner always speaks German, with a translation underneath.
- Single static file: `index.html` (Three.js r128 from cdnjs, fonts from Google Fonts).
- No build step. Open `index.html` or serve the folder with any static host.

## Installable app (PWA)

- `manifest.webmanifest` and `icons/` make the game installable ("Add to Home Screen"; Chrome/Edge/Android also show an install button on the start screen).
- `sw.js` caches the game for offline play. The page itself is fetched network-first, so a new deploy reaches players on their next visit. Bump `CACHE` in `sw.js` only to drop old cached files.
- Service workers need HTTPS (GitHub Pages provides it) or `localhost`; opening `index.html` as a file still works, just without offline support.

## Hosting

- GitHub Pages: Settings → Pages → Branch `main`, folder `/ (root)`.
- AWS Amplify: connect this repo, no build command, output directory `/`.
