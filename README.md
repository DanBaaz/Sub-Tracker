# Sub Tracker

https://danbaaz.github.io/Sub-Tracker/sub-tracker.html

A junior basketball substitution tracker built for sideline use during live games. Manage multiple teams, track fair court time, and get smart substitution suggestions — all from your phone, installable as a home-screen app.

## Features

- **Multi-team management** — create and switch between teams, each with its own roster, colours, and settings, saved on-device
- **Live substitution tracking** — tap a player to sub them on/off court, with on-court/off-court highlight colours
- **Smart sub suggestions** — choose between "Court Time" (most/least time played) or "Next On List" (fixed rotation order) modes, with a configurable number of suggestions that auto-scales to your active bench size
- **Countdown game clock** — quarters or halves, configurable duration, with a "time since last sub" timer
- **Sub reminder cues** — optional sound and/or vibration alerts if too long has passed since the last substitution
- **Foul tracking** — mark players fouled out; they're benched and excluded from suggestions automatically
- **Custom colour schemes** — background, player bar, on-court/off-court highlight, and sub in/out colours per team, with automatic text contrast
- **Works offline** — installs as a Progressive Web App (PWA) with a real home-screen icon, full-screen display, and offline support once installed

## Using it on your phone

1. Open the hosted URL (see below) in **Chrome on Android**
2. Tap **Install app** from the menu (⋮) or the install banner
3. Launch it from your home screen like any other app — no browser address bar, works with no signal once loaded

## Hosting this yourself (GitHub Pages)

This repo is set up to be served directly with [GitHub Pages](https://pages.github.com/):

1. Go to **Settings → Pages**
2. Under **Build and deployment**, set Source to **Deploy from a branch**
3. Choose the `main` branch and `/ (root)` folder, then **Save**
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/sub-tracker.html`

All files must stay together in the same top-level folder — the manifest, service worker, and icons all reference each other by relative path.

## Files in this repo

| File | Purpose |
|---|---|
| `sub-tracker.html` | The app itself — a single self-contained HTML/CSS/JS file |
| `manifest.json` | PWA manifest (app name, icons, standalone display mode) |
| `service-worker.js` | Caches the app for offline use; always prefers the latest version when online |
| `icon-192.png`, `icon-512.png` | Home-screen app icons |
| `icon-maskable-512.png` | Adaptive icon for Android (safe-zone padding) |
| `apple-touch-icon.png` | Home-screen icon for iOS/Safari |

## Updating

When you make changes to `sub-tracker.html` (or any file here):

1. Upload the updated file(s) to this repo (overwriting the old ones)
2. Bump the `CACHE_NAME` value in `service-worker.js` (e.g. `sub-tracker-cache-v1` → `v2`) so phones that already installed the app pick up the new version instead of serving a stale cached copy

## Data & privacy

All team data, rosters, and settings are stored locally in the browser on each device — nothing is sent to a server. Use the in-app **App Settings → Export All Teams** option to back up or move data between devices.

## Version history

See the in-app **Help → Change Log** page for a full version history.
