# Fit

A small, offline-capable workout logger. No build step, no dependencies.

## Deploy on GitHub Pages

1. Create a repository and upload everything in this folder, keeping the structure
   (`index.html`, `manifest.webmanifest`, `sw.js`, `icons/`, `.nojekyll`).
2. Repo **Settings → Pages → Build and deployment**: Source *Deploy from a branch*,
   branch `main`, folder `/ (root)`.
3. Open `https://<user>.github.io/<repo>/` after a minute.
4. On iPhone: Safari → Share → **Add to Home Screen**. On Android: menu → **Install app**.

All paths are relative, so it works under a project URL like `/<repo>/`.

## Updating

Edit `index.html`, then bump `CACHE` in `sw.js` (for example `fit-v4`). Installed copies
refresh in the background and show the new version on the next launch.

## Your data

Workouts are stored in the browser's `localStorage` on each device and are never uploaded.
Use the **Backup** tab to save a `.json` file now and then (the app reminds you after 14 days).
Clearing site data or uninstalling the home-screen app deletes your history unless you have a backup.

## Tuning exercises

Progression and slider steps are set per exercise in the `EC` table near the top of the script:
`inc` (kg added when every set hits `hi` reps), `step` (kg per slider tick), `lo`/`hi` (rep range).
