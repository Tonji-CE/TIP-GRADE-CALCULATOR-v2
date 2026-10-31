# TIP Grade Calculator — Android PWA

This folder contains the existing TIP Grade Calculator converted into an installable, offline-capable Progressive Web App (PWA).

## Files
- `index.html` — calculator website (including “Made By Tonji” and the student disclaimer)
- `manifest.webmanifest` — app name, display mode, theme, and icons
- `sw.js` — service worker that caches the app shell for offline use
- `icons/` — navy-and-gold app icons

## Publish free with GitHub Pages

1. Sign in to GitHub and create a **new public repository**, for example `tip-grade-calculator`.
2. On your computer, unzip this package.
3. Upload **the contents of this folder** to the repository's top level. Make sure `index.html`, `manifest.webmanifest`, and `sw.js` are at the repository root, and the `icons` folder is included.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch **main** and folder **/(root)**, then click **Save**.
7. Wait for GitHub Pages to publish. Your site will have an address similar to:
   `https://YOUR-USERNAME.github.io/tip-grade-calculator/`
8. Open that HTTPS address on your Android phone using **Google Chrome**. Load it once while online and wait a few seconds so the service worker can cache the app files.

GitHub Pages is free for public repositories. The URL will use your own GitHub username; no password or account credentials should be shared with anyone.

## Install on Android

1. Open the published HTTPS site in Chrome.
2. Tap Chrome's **⋮** menu.
3. Choose **Install app** (or **Add to Home screen**, depending on your Chrome version).
4. Confirm the installation. The “TIP Grades” icon should appear on your home screen/app launcher.

## Offline use

After the site has loaded online once and the service worker has installed, reopen the installed app while offline. The calculator interface and its calculations should continue to work offline. Reconnect occasionally to receive future updates.

## Updating the app

Upload replacement files to the same repository. The service worker cache name is versioned in `sw.js`; if you make a later release, change `tip-grade-calculator-v1` to `tip-grade-calculator-v2` so installed clients fetch the updated app shell.

## Important grading note

The calculator preserves the formulas and grade-equivalent brackets from the prior conversation. These have not been independently confirmed as the current official TIP Quezon City policy. Check your instructor's syllabus or TIP's current grading policy before relying on the computed results.
