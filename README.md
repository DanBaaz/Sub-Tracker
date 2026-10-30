# Sub Tracker (v1.11)

https://danbaaz.github.io/Sub-Tracker/sub-tracker.html

A sideline substitution tracker for junior basketball — tracks on-court time per
player, suggests who to sub in/out, runs the game clock, and works fully
offline once installed on a phone.

## What's in this folder

| File                     | Purpose                                                        |
|---------------------------|-----------------------------------------------------------------|
| `sub-tracker.html`        | The app itself. All logic and styling lives in this one file.  |
| `manifest.json`           | PWA manifest — app name, icons, colours, standalone display.   |
| `service-worker.js`       | Enables offline use and caches the app for fast reloads.       |
| `icon-192.png`            | App icon (192×192), used in the manifest and browser tab.      |
| `icon-512.png`            | App icon (512×512), used for install prompts / splash screens. |
| `icon-maskable-512.png`   | Maskable variant (512×512) for adaptive Android icons.          |
| `apple-touch-icon.png`    | Home-screen icon for iOS "Add to Home Screen".                 |
| `CHANGELOG.md`            | Full version history.                                          |

## Hosting it (required for full install support)

A PWA needs to be served over **HTTPS** to install properly (offline caching,
standalone window, no browser address bar). Opening `sub-tracker.html`
directly from a phone's file system will still run the app, but skips
installability and offline caching.

The simplest free option is **GitHub Pages**:

1. Create a GitHub repo and upload all the files in this folder to it,
   keeping them in the same folder together (don't rename any of them —
   the manifest and service worker reference these exact filenames).
2. In the repo's Settings → Pages, enable Pages for the branch you uploaded to.
3. GitHub will give you a URL like
   `https://<your-username>.github.io/<repo-name>/sub-tracker.html` —
   that's the link to open on your phone.

Any other static HTTPS host (Netlify, Vercel, Cloudflare Pages, etc.) works
the same way — just upload all the files together.

## Installing on a phone

Once it's hosted over HTTPS:

- **Android (Chrome):** open the link, tap the menu (⋮), then
  "Add to Home screen" / "Install app".
- **iOS (Safari):** open the link, tap the Share icon, then
  "Add to Home Screen".

Either way you get a home-screen icon that opens full-screen, with no
browser address bar, and keeps working without a signal once it's loaded
at least once.

## Updating later

When you get a newer version of `sub-tracker.html`, just replace the file
on your host (same filename, same folder). The service worker uses a
network-first strategy — it always tries to fetch the latest version first,
and only falls back to the offline copy if there's no connection. Re-open
the app (or pull-to-refresh) to pick up the update.

If you change the **filenames** of the icons or manifest, or want to force
every device to drop its old cached copy immediately, bump the
`CACHE_NAME` value at the top of `service-worker.js` — that's the only
part of it that normally needs editing between releases.

## Data & privacy

All teams, rosters, and settings are stored locally in the browser
(`localStorage`) on whichever device you're using — nothing is sent to a
server. Use the in-app **App Settings → Export All Teams** to back up your
data, and **Import Teams** to restore it or move it to another device.
