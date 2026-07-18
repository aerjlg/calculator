# Calculator — Ae productions

Installable web app (PWA). Light theme, RocknRoll One, circular keys.

## Put it on your Android home screen

1. Create a new **public** repo on GitHub, e.g. `calculator`.
2. Upload every file in this folder to the repo root:
   `index.html`, `manifest.webmanifest`, `sw.js`,
   `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`
3. Repo **Settings → Pages → Build and deployment**:
   Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`. Save.
4. Wait ~1 minute. Your URL is:
   `https://<your-username>.github.io/calculator/`
5. Open that URL in **Chrome on Android**.
6. Chrome menu (⋮) → **Add to Home screen** / **Install app** → **Install**.

You now have an icon in the app drawer and on the home screen. It opens
full-screen with no address bar, and works offline — the service worker
caches the page, the icons and the font on first load.

## Updating it later

Edit `index.html` in the repo, then bump the cache name in `sw.js`
(`calc-v1` → `calc-v2`) and commit. Next time you open the app it will
fetch the new version. Without the bump, the old cached copy keeps showing.

## Checking it worked

In Chrome on the phone: `chrome://inspect` from a desktop, or simply turn on
flight mode and reopen the app — if it loads, caching is working.

Ae productions
